---
title: Microsoft 搜尋 ServiceNow 圖形連接器
ms.author: mecampos
author: mecampos
manager: umas
audience: Admin
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 設定 Microsoft 搜尋的 ServiceNow 圖形連接器
ms.openlocfilehash: eaf8014876b03c0b64c012cf7e83c4e4b84838b9
ms.sourcegitcommit: f76ade4c8fed0fee9c36d067b3ca8288c6c980aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "50508677"
---
<!---Previous ms.author: kam1 --->

# <a name="servicenow-graph-connector"></a>ServiceNow 圖形連接器

「ServiceNow 圖形連接器」可讓您的組織根據組織內的使用者準則許可權，為使用者顯示可看到之知識型文章的索引。 從 ServiceNow 設定連接器和索引內容之後，使用者可以從任何 Microsoft 搜尋用戶端搜尋文章。

> [!NOTE]
> 請閱讀 [**您的圖形連接器**](configure-connector.md) 文章的設定，以瞭解一般圖表連接器設定指示。

本文適用于任何設定、執行及監視 ServiceNow 圖形連接器的人員。 它會補充一般設定程式，並顯示只適用于 ServiceNow 圖形連接器的指示。 本文也包含 [疑難排解](#troubleshooting) 及 [限制](#limitations)的相關資訊。
  
## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a>步驟1：在 Microsoft 365 系統管理中心新增圖表連接器

遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-2-name-the-connection"></a>步驟2：命名連線

遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-3-connection-settings"></a>步驟3：連接設定

若要連線至您的 ServiceNow 資料，請使用您組織的 ServiceNow 此帳戶的 **實例 URL** 認證、用戶端識別碼，以及 OAuth 驗證的用戶端密碼。  

組織的 **ServiceNow 實例 URL** 一般會類似 **HTTPs:// &lt; 您的組織網域> service-now.com**。 使用此 URL 時，您需要有帳戶來設定 ServiceNow 的連線，以及允許 Microsoft 搜尋依據重新整理排程從 ServiceNow 更新文章。 帳戶至少應具備 <em>知識</em> 角色。 [瞭解如何指派 ServiceNow 帳戶的角色](https://docs.servicenow.com/bundle/paris-platform-administration/page/administer/users-and-groups/task/t_AssignARoleToAUser.html)。

>[!NOTE]
>如果您想要編目使用者和群組身分識別，以服從 Microsoft 搜尋結果中知識文章的存取權限，該帳戶應該可以存取 ServiceNow 中的下清單記錄：
>* kb_uc_can_contribute_mtom
>* kb_uc_can_read_mtom
>* kb_uc_cannot_read_mtom
>* kb_uc_cannot_contribute_mtom
>* sys_user
>* sys_user_has_role
>* sys_user_grmember
>* user_criteria
>* kb_knowledge_base  
> 您可以為您用來連線 Microsoft 搜尋的帳戶建立和指派角色。 可以在該角色上指派對表格的讀取權限。 若要瞭解如何設定表記錄的「讀取」存取權，請參閱 [保護資料表記錄](https://developer.servicenow.com/dev.do#!/learn/learning-plans/orlando/new_to_servicenow/app_store_learnv2_securingapps_orlando_creating_and_editing_access_controls)。

若要驗證及同步處理 ServiceNow 中的內容，請選擇下列 **其中一** 項支援的方法：

1. 基本驗證
1. ServiceNow OAuth (建議) 
1. Azure AD OpenID Connect

### <a name="basic-authentication"></a>基本驗證

輸入具有 **知識** 角色的 ServiceNow 帳戶的使用者名稱和密碼，以向您的實例驗證。

### <a name="servicenow-oauth"></a>ServiceNow OAuth

若要使用 ServiceNow OAuth 進行驗證，請在 ServiceNow 實例中布建端點。 Microsoft Search 應用程式會使用它來存取實例。 若要深入瞭解，請參閱在 ServiceNow 檔中 [建立用戶端存取實例的端點](https://docs.servicenow.com/bundle/newyork-platform-administration/page/administer/security/task/t_CreateEndpointforExternalClients.html) 。

下表提供如何填寫端點建立表單的指導方針：

欄位 | 描述 | 建議值 
--- | --- | ---
姓名 | 識別您需要 OAuth 存取之應用程式的唯一值。 | Microsoft 搜尋
用戶端識別碼 | 應用程式的唯讀、自動產生的唯一識別碼。 當實例要求存取權杖時，會使用用戶端識別碼。 | NA
用戶端密碼 | 使用此共用的機密字串，ServiceNow 實例和 Microsoft 搜尋會授權彼此間的通訊。 | 遵循安全性最佳作法，將密碼當做密碼對待。
重新導向 URL | 授權伺服器重新導向所需的回撥 URL。 | https://gcs.office.com/v1.0/admin/oauth/callback
標誌 URL | 包含應用程式標誌之圖像的 URL。 | NA
作用中 | 選取此核取方塊，讓應用程式登錄成為使用中。 | 設定為 active
重新整理權杖生命週期 | 重新整理權杖有效的秒數。 根據預設，重新整理權杖會在100天內到期 (8640000 秒) 。 | 31536000 (1 年) 
存取權杖使用壽命 | 存取權杖有效的秒數。 | 43200 (12 小時) 

輸入用戶端識別碼和用戶端密碼以連接至您的實例。 連接後，請使用 ServiceNow 帳號憑證來驗證編目的許可權。 帳戶至少應具備 **知識** 角色。

### <a name="azure-ad-openid-connect"></a>Azure AD OpenID Connect

若要使用 Azure AD OpenID Connect 以進行驗證，請遵循下列步驟。

## <a name="step-3a-register-a-new-application-in-azure-active-directory"></a>步驟3。 a：在 Azure Active Directory 中註冊新的應用程式

若要瞭解如何在 Azure Active Directory 中註冊新的應用程式，請參閱 [註冊應用程式](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#register-an-application)。 選取 [單一承租人組織目錄]。 不需要重新導向 URI。 註冊後，請記下應用程式 (用戶端) ID 及目錄 (承租人) 識別碼。

## <a name="step-3b-create-a-client-secret"></a>步驟3：建立用戶端密碼

若要瞭解如何建立用戶端密碼，請參閱 [建立用戶端密碼](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#add-a-client-secret)。 記錄用戶端密碼。

## <a name="step-3c-retrieve-service-principal-object-identifier"></a>步驟 3 .. c：取回服務主體物件識別碼

遵循下列步驟以取得服務主體物件識別碼

1. 執行 PowerShell。

2. 使用下列命令安裝 Azure PowerShell。

   ```powershell
   Install-Module -Name Az -AllowClobber -Scope CurrentUser
   ```

3. 連接到 Azure。

   ```powershell
   Connect-AzAccount
   ```

4. 取得服務主體物件識別碼。

   ```powershell
   Get-AzADServicePrincipal -ApplicationId "Application-ID"
   ```
   將 "Application ID" 取代為您在步驟3中所註冊應用程式的應用程式 (用戶端) ID (但不) 引號。 請注意，PowerShell 輸出中的 ID 物件的值。 這是服務主體識別碼。

現在，您已具備 Azure 入口網站所需的所有資訊。 下表提供資訊的快速摘要。

屬性	 | 描述 
--- | ---
目錄識別碼 (租使用者識別碼)  | Azure Active Directory 租使用者的唯一識別碼，從步驟3。
 (用戶端識別碼的應用程式識別碼)  | 在步驟3中註冊之應用程式的唯一識別碼。
用戶端密碼 | 從步驟 3 () 的應用程式的機密機碼。 請將它當作密碼對待。
服務主體識別碼 | 作為服務執行之應用程式的身分識別。 步驟 3 () 

## <a name="step-3d-register-servicenow-application"></a>步驟 3 ..：註冊 ServiceNow 應用程式

ServiceNow 實例需要下列設定：

1. 註冊新的 OAuth OIDC 實體。 若要瞭解，請參閱 [Create a OAUTH OIDC provider](https://docs.servicenow.com/bundle/orlando-platform-administration/page/administer/security/task/add-OIDC-entity.html)。

2. 下表提供如何填寫 OIDC 提供者註冊表單的指導方針。

   欄位 | 描述 | 建議值
   --- | --- | ---
   姓名 | 識別 OAuth OIDC 實體的唯一名稱。 | Azure AD
   用戶端識別碼 | 在協力廠商 OAuth OIDC server 中註冊之應用程式的用戶端識別碼。 實例在要求存取權杖時使用用戶端識別碼。 | Application (Client) ID 從步驟3。
   用戶端密碼 | 在協力廠商 OAuth OIDC server 中註冊之應用程式的用戶端密碼。 | 步驟3的用戶端密碼。 b

   其他所有值都可以是預設值。

3. 在 OIDC 提供者註冊表單中，您必須新增新的 OIDC 提供者設定。 根據 *OAUTH OIDC 提供者* 設定] 欄位，選取要開啟 OIDC 設定記錄的搜尋圖示。 選取 [新增]。

4. 下表提供如何填寫 OIDC 提供者設定表單的指導方針

   欄位 | 建議值
   --- | ---
   OIDC 提供者 |  Azure AD
   OIDC 中繼資料 URL | URL 的格式必須為 HTTPs \: //login.microsoftonline.com/<tenandId ">/.well-known/openid-configuration <br/>以步驟3的目錄 (租使用者) 識別碼取代 "tenantID"。
   OIDC 設定快取壽命範圍 |  120
   應用程式 | 全域
   使用者宣告 | 子
   使用者欄位 | 使用者識別碼
   啟用 JTI 宣告驗證 | 停用

5. 選取 [提交並更新 OAuth OIDC 實體表單]。

## <a name="step-3e-create-a-servicenow-account"></a>步驟 3 .. e：建立 ServiceNow 帳戶

請參閱指示建立 ServiceNow 帳戶、 [在 ServiceNow 中建立使用者](https://docs.servicenow.com/bundle/paris-platform-administration/page/administer/users-and-groups/task/t_CreateAUser.html)。

下表提供如何填寫 ServiceNow 使用者帳戶註冊的指導方針。

欄位 | 建議值
--- | ---
使用者識別碼 | 步驟3中的服務主體識別碼。 c
僅 Web 服務存取權 | Checked

其他所有值都可以保留預設值。

## <a name="step-3f-enable-knowledge-role-for-the-servicenow-account"></a>步驟 3 .. f：啟用 ServiceNow 帳戶的知識角色

存取您用 ServiceNow 主體識別碼建立的 ServiceNow 帳戶做為使用者識別碼，並指派知識角色。 您可以在以下位置找到將角色指派給 ServiceNow 帳戶的指示： [指派角色給使用者](https://docs.servicenow.com/bundle/paris-platform-administration/page/administer/users-and-groups/task/t_AssignARoleToAUser.html)。

使用應用程式識別碼做為用戶端識別碼從步驟3。 a 及用戶端密碼，以使用 Azure AD OpenID Connect 向您的 ServiceNow 實例進行驗證。

## <a name="step-4-select-properties-and-filter-data"></a>步驟4：選取屬性和篩選資料

在這個步驟中，您可以從 ServiceNow 資料來源新增或移除可用屬性。 Microsoft 365 預設已經選取一些屬性。

使用 ServiceNow 查詢字串，您可以指定同步處理文章的條件。 它就像是 **SQL Select** 語句中的 **Where** 子句。 例如，您可以選擇只為發佈和使用中的文章編制索引。 若要瞭解如何建立您自己的查詢字串，請參閱 [使用篩選產生編碼的查詢字串](https://docs.servicenow.com/bundle/paris-platform-user-interface/page/use/using-lists/task/t_GenEncodQueryStringFilter.html)。

使用 [預覽結果] 按鈕，檢查所選屬性和查詢篩選器的範例值。

## <a name="step-5-manage-search-permissions"></a>步驟5：管理搜尋許可權

ServiceNow 連接器支援 **所有人都** 可以看到的搜尋許可權，或是 **只有存取此資料來源的人員才能使用**。 已編制索引的資料會顯示在搜尋結果中，並可供組織中的使用者在其上分別存取。 ServiceNow 連接器支援不含高級腳本的預設使用者準則許可權。 當連接器找到具有 advanced script 的使用者準則時，搜尋結果中將不會顯示使用該使用者準則的所有資料。

如果您只選取可 **存取此資料來源的人員**，您需要進一步選擇 ServiceNow 實例是否有 Azure Active DIRECTORY (AAD) 布建使用者或非 AAD 使用者。

>[!NOTE]
>如果您只選擇可 **存取此資料來源的人員**，則會在 **預覽** ServiceNow 連接器。

>[!NOTE]
>如果您選擇 [AAD] 做為身分識別來源的類型，請確定您在 ServiceNow 中為電子郵件目標屬性指派 UPN 來源屬性。 若要驗證或變更您的對應，請參閱 [自訂使用者布建屬性-在 Azure Active Directory 中 SaaS 應用程式的對應](https://docs.microsoft.com/azure/active-directory/app-provisioning/customize-application-attributes)。

如果您選擇從 ServiceNow 實例中攝取 ACL，並為身分識別類型選取 "非 AAD"，請參閱 [Map 您的非 AZURE AD](map-non-aad.md) 身分識別，以取得對應身分識別的指示。

## <a name="step-6-assign-property-labels"></a>步驟6：指派屬性標籤

遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-7-manage-schema"></a>步驟7：管理架構

遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-8-choose-refresh-settings"></a>步驟8：選擇重新整理設定

遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

>[!NOTE]
>針對身分識別，只會套用已排程的完整編目。

## <a name="step-9-review-connection"></a>步驟9：檢查連線

遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="troubleshooting"></a>疑難排解

在發佈連線後，自訂 [結果] 頁面，您可以在系統 [管理中心](https://admin.microsoft.com)的 [**連接器**] 索引標籤底下查看狀態。 若要瞭解如何進行更新和刪除，請參閱 [管理您的連接器](manage-connector.md)。

## <a name="limitations"></a>限制

在最新版本中，ServiceNow 圖形連接器的限制如下：

- 組織中的每個人都可以使用的索引知識文章是一項普遍可用的功能。
- *只有存取此資料來源功能的使用者* 才會在 [管理搜尋許可權] 步驟中使用預覽，而且只會處理 [使用者準則](https://hi.service-now.com/kb_view.do?sysparm_article=KB0550924) 許可權。 任何其他類型的存取權限都不會套用到搜尋結果中。
- 目前的預覽版本不支援具有高級腳本的使用者準則。 具有存取限制的知識文章會以「拒絕所有人」存取的方式編制索引，而且不會顯示在搜尋結果中，直到我們支援它們為止。
