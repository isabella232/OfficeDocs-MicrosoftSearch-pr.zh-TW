---
title: Microsoft 搜尋的 ServiceNow 連接器
ms.author: kam1
author: TheKarthikeyan
manager: harshkum
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 設定 Microsoft 搜尋的 ServiceNow 連接器
ms.openlocfilehash: f7ae05ad00a96a6f05780acfeb8c75911505ee6f
ms.sourcegitcommit: 2ce86461e845c3ea84feb215df17685d2ef705c5
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/02/2020
ms.locfileid: "48340854"
---
# <a name="servicenow-connector"></a>ServiceNow 連接器

使用 ServiceNow 連接器，您的組織可以為組織內所有使用者顯示的知識庫文章編制索引。 從 ServiceNow 設定連接器和索引內容之後，使用者可以從任何 Microsoft 搜尋用戶端搜尋這些文章。  

本文適用于 Microsoft 365 系統管理員或任何設定、執行及監視 ServiceNow 連接器的人員。 它說明如何設定連接器和連接器功能、限制及疑難排解技術。

瞭解如何存取 Microsoft 建立的連接器 [，以設定 microsoft 的連接器以進行 Microsoft 搜尋](https://docs.microsoft.com/microsoftsearch/configure-connector)。 下列文章說明 ServiceNow 連接器特定設定。

## <a name="connection-settings"></a>連接設定
若要連線至您的 ServiceNow 資料，您需要組織的 **ServiceNow 實例 URL**、此帳戶的認證，以及 OAuth 驗證的用戶端識別碼和用戶端密碼。  

組織的 **ServiceNow 實例 URL** 一般會類似 **HTTPs:// &lt; 您的組織網域> service-now.com**。 除了此 URL 之外，您還需要一個帳戶，用以設定 ServiceNow 的連線，以及允許 Microsoft 搜尋依重新整理排程，定期更新 ServiceNow 中的文章。 帳戶應具備 <em>知識</em> 角色。 [瞭解如何指派 ServiceNow 帳戶的角色](https://docs.servicenow.com/bundle/paris-platform-administration/page/administer/users-and-groups/task/t_AssignARoleToAUser.html)。

若要驗證及同步處理 ServiceNow 中的內容，請選擇下列 **其中一** 項支援的方法： 
1. 基本驗證 
2. ServiceNow OAuth (建議) 
3. Azure AD OpenID Connect

#### <a name="basic-authentication"></a>基本驗證
輸入具有 <em>知識</em> 角色的 ServiceNow 帳戶的使用者名稱和密碼，以向您的實例驗證。
#### <a name="servicenow-oauth"></a>ServiceNow OAuth

若要使用 ServiceNow OAuth 進行驗證，ServiceNow 系統管理員必須布建 ServiceNow 實例中的端點，這樣 Microsoft Search 應用程式才能存取該實例。 若要深入瞭解，請參閱在 ServiceNow 檔中 [建立用戶端存取實例的端點](https://docs.servicenow.com/bundle/newyork-platform-administration/page/administer/security/task/t_CreateEndpointforExternalClients.html) 。

下表提供如何填寫端點建立表單的指導方針：

**Field** | **描述** | **建議值**
--- | --- | ---
姓名 | 此唯一值可識別您需要 OAuth 存取的應用程式。 | Microsoft 搜尋
用戶端識別碼 | 應用程式的唯讀、自動產生的唯一識別碼。 當實例要求存取權杖時，會使用用戶端識別碼。 | NA
用戶端密碼 | 使用此共用的機密字串，ServiceNow 實例和 Microsoft 搜尋會授權彼此間的通訊。 | 請將此視為密碼，遵循安全性最佳作法。
重新導向 URL | 授權伺服器重新導向所需的回撥 URL。 | https://gcs.office.com/v1.0/admin/oauth/callback
標誌 URL | 包含應用程式標誌之圖像的 URL。 | NA
作用中 | 選取此核取方塊，讓應用程式登錄成為使用中。 | 設定為 active
重新整理權杖生命週期 | 重新整理權杖有效的秒數。 根據預設，重新整理權杖會在100天內到期 (8640000 秒) 。 | 31536000 (1 年) 
存取權杖使用壽命 | 存取權杖有效的秒數。 | 43200 (12 小時) 

輸入用戶端識別碼和用戶端密碼以連接至您的實例。 連接後，請使用 ServiceNow 帳號憑證來驗證編目的許可權。 帳戶應具備 <em>知識</em> 角色。 

#### <a name="azure-ad-openid-connect"></a>Azure AD OpenID Connect

若要使用 Azure AD OpenID Connect 以進行驗證，請遵循下列步驟。

###### <a name="step-1-register-a-new-application-in-azure-active-directory"></a>步驟1：在 Azure Active Directory 中註冊新的應用程式

若要瞭解如何在 Azure Active Directory 中註冊新的應用程式，請參閱 [註冊應用程式](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#register-an-application)。 選取 [單一承租人組織目錄]。 不需要重新導向 URI。 註冊後，請記下應用程式 (用戶端) ID 及目錄 (承租人) 識別碼。

###### <a name="step-2-create-a-client-secret"></a>步驟2：建立用戶端密碼

若要瞭解如何建立用戶端密碼，請參閱 [建立用戶端密碼](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#add-a-client-secret)。 記錄用戶端密碼。

###### <a name="step-3-retrieve-service-principal-object-identifier"></a>步驟3：取回服務主體物件識別碼

遵循下列步驟以取得服務主體物件識別碼

1. 執行 PowerShell
2. 使用下列命令安裝 Azure PowerShell
```<language>
   Install-Module -Name Az -AllowClobber -Scope CurrentUser
```
3. 連接到 Azure
```<language>
    Connect-AzAccount
```
4. 取得服務主體物件識別碼
```<language>
   Get-AzADServicePrincipal -ApplicationId "Application-ID"
```
以您在步驟1中所註冊應用程式的應用程式 (用戶端) ID (取代「應用程式識別碼」) 引號。 請注意，PowerShell 輸出中的 ID 物件的值。 它是服務主體識別碼。

現在，您已具備 Azure 入口網站所需的所有資訊。 下表提供資訊的快速摘要。

**屬性** | **描述**
--- | ---
目錄識別碼 (租使用者識別碼)  | 這是從步驟 1) 參考 Azure Active Directory 租使用者 (的唯一識別碼。
 (用戶端識別碼的應用程式識別碼)  | 這是參照步驟1中所註冊之應用程式的唯一識別碼。
用戶端密碼 | 這是步驟 2) 中應用程式 (的機密金鑰。 請將它當作密碼對待。
服務主體識別碼 | 作為服務執行之應用程式的身分識別。 步驟 3 () 

###### <a name="step-4-register-servicenow-application"></a>步驟4：註冊 ServiceNow 應用程式

在 ServiceNow 實例中，必須進行下列設定。

1. 註冊新的 OAuth OIDC 實體。 若要瞭解，請參閱 [Create a OAUTH OIDC provider](https://docs.servicenow.com/bundle/orlando-platform-administration/page/administer/security/task/add-OIDC-entity.html)。
2. 下表提供如何填寫 OIDC 提供者註冊表單的指導方針。

**Field** | **描述** | **建議值**
--- | --- | ---
姓名 | 識別 OAuth OIDC 實體的唯一名稱。 | Azure AD
用戶端識別碼 | 在協力廠商 OAuth OIDC server 中註冊之應用程式的用戶端識別碼。 實例在要求存取權杖時使用用戶端識別碼。 | 步驟1的應用程式 (用戶端) 識別碼
用戶端密碼 | 在協力廠商 OAuth OIDC server 中註冊之應用程式的用戶端密碼。 | 步驟2中的用戶端密碼

其他所有值都可以是預設值。

3. 在 OIDC 提供者註冊表單中，您必須新增新的 OIDC 提供者設定。 根據 *OAUTH OIDC 提供者* 設定] 欄位，按一下搜尋圖示，以開啟 OIDC 設定的記錄。 按一下 [新增]。
4. 下表提供如何填寫 OIDC 提供者設定表單的指導方針

**Field** | **建議值**
--- | ---
OIDC 提供者 |  Azure AD
OIDC 中繼資料 URL | 其格式必須為 HTTPs \: //login.microsoftonline.com/"tenandId"/.well-known/openid-configuration <br/>將 "tenantID" 取代為步驟 1 (不含引號) 的目錄 (租使用者) ID。
OIDC 設定快取壽命範圍 |  120
應用程式 | 全域
使用者宣告 | 子
使用者欄位 | 使用者識別碼
啟用 JTI 宣告驗證 | 停用

5. 按一下 [提交]，然後更新 OAuth OIDC 實體表單。

###### <a name="step-5-create-a-servicenow-account"></a>步驟5：建立 ServiceNow 帳戶

請參閱指示建立 ServiceNow 帳戶、 [在 ServiceNow 中建立使用者](https://docs.servicenow.com/bundle/paris-platform-administration/page/administer/users-and-groups/task/t_CreateAUser.html)。

下表提供如何填寫 ServiceNow 使用者帳戶註冊的指導方針。

**Field** | **建議值**
--- | ---
使用者識別碼 | 步驟3的服務主體識別碼
僅 Web 服務存取權 | Checked

其他所有值都可以保留預設值。

###### <a name="step-6-enable-knowledge-role-for-the-servicenow-account"></a>步驟6：啟用 ServiceNow 帳戶的知識角色

存取您用 ServiceNow 主體識別碼建立的 ServiceNow 帳戶做為使用者識別碼並指派知識角色。 您可以在這裡找到將角色指派給 ServiceNow 帳戶的指示， [將角色指派給使用者](https://docs.servicenow.com/bundle/paris-platform-administration/page/administer/users-and-groups/task/t_AssignARoleToAUser.html)。

使用應用程式識別碼做為用戶端識別碼 (從步驟 1) ，並從系統管理中心的「步驟 2) 用戶端密碼 (，以使用 Azure AD ServiceNow Connect 向您的 OpenID 實例進行驗證。

## <a name="filter-data"></a>篩選資料 
使用 ServiceNow 查詢字串，您可以指定同步處理文章的條件。 它就像是**SQL Select**語句中的**Where**子句。 例如，您可以選擇只為發佈和使用中的文章編制索引。 若要瞭解如何建立您自己的查詢字串，請參閱 [使用篩選產生編碼的查詢字串](https://docs.servicenow.com/bundle/paris-platform-user-interface/page/use/using-lists/task/t_GenEncodQueryStringFilter.html)。

## <a name="manage-the-search-schema"></a>管理搜尋結構描述
成功連接後，請設定搜尋架構對應。 您可以選擇哪些屬性可供**查詢**、可搜尋及可**供****檢索**。 若要深入瞭解管理搜尋架構，請參閱 [管理搜尋架構](https://docs.microsoft.com/microsoftsearch/configure-connector#manage-the-search-schema)。

## <a name="manage-search-permissions"></a>管理搜尋許可權
ServiceNow 連接器只支援 **所有人都**能看見的搜尋許可權。 已編制索引的資料會顯示在搜尋結果中，並對組織中的所有使用者顯示。

## <a name="set-the-refresh-schedule"></a>設定重新整理排程
ServiceNow 連接器支援完整和累加編目的更新排程。 我們建議您同時設定兩者。

完整編目排程會找到先前同步處理至 Microsoft 搜尋索引的已刪除文章，以及任何移出同步篩選的文章。 當您第一次連線至 ServiceNow 時，會執行完整編目以同步處理所有知識文庫文章。 若要同步處理新專案並進行更新，您必須排程累加編目。

建議的預設值為一天的完整編目及四小時為增量編目。
## <a name="review-and-publish"></a>審閱及發佈
設定連接器之後，即可複查及發佈連線。

## <a name="next-steps"></a>後續步驟
在發佈連線後，您必須自訂搜尋結果頁面。 若要瞭解如何自訂搜尋結果，請參閱 [自訂搜尋結果頁面](https://docs.microsoft.com/microsoftsearch/configure-connector#next-steps-customize-the-search-results-page)。
