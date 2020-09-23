---
title: Microsoft 搜尋的 ServiceNow 連接器
ms.author: mnirkhe
author: TrishaMc1
manager: mnirkhe
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 設定 Microsoft 搜尋的 ServiceNow 連接器
ms.openlocfilehash: 357722f83e7f276615d231c8d3e56016bc17ba6e
ms.sourcegitcommit: be0c64845477127d73ee24dc727e4583ced3d0e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/22/2020
ms.locfileid: "48206957"
---
# <a name="servicenow-connector"></a>ServiceNow 連接器

使用 ServiceNow 連接器，您的組織可以為組織內所有使用者顯示的知識庫文章編制索引。 從 ServiceNow 設定連接器和索引內容之後，使用者可以從任何 Microsoft 搜尋用戶端搜尋這些文章。  

本文適用于 Microsoft 365 系統管理員或任何設定、執行及監視 ServiceNow 連接器的人員。 它說明如何設定連接器和連接器功能、限制及疑難排解技術。

## <a name="connect-to-a-data-source"></a>連接到資料來源

若要連線至您的 ServiceNow 資料，您需要組織的 **ServiceNow 實例 URL**、此帳戶的認證，以及 OAuth 驗證的用戶端識別碼和用戶端密碼。  

組織的 **ServiceNow 實例 URL** 一般會類似 **HTTPs:// &lt; 您的組織網域> service-now.com**。 除了此 URL 之外，您還需要一個帳戶，用以設定 ServiceNow 的連線，以及允許 Microsoft 搜尋依重新整理排程，定期更新 ServiceNow 中的文章。

若要驗證及同步處理 ServiceNow 中的內容，請選擇兩個支援的方法之一：

 - 基本驗證
 - OAuth (建議) 

> [!Note]
> 若要使用 OAuth 進行驗證，ServiceNow 系統管理員必須布建 ServiceNow 實例中的端點，這樣 Microsoft Search 應用程式才能存取該實例。 若要深入瞭解，請參閱在 ServiceNow 檔中 [建立用戶端存取實例的端點](https://docs.servicenow.com/bundle/newyork-platform-administration/page/administer/security/task/t_CreateEndpointforExternalClients.html) 。

下表提供如何填寫端點建立表單的指導方針：

欄位 | 描述 | 建議值
--- | --- | ---
名稱 | 此唯一值可識別您需要 OAuth 存取的應用程式。 | Microsoft 搜尋
用戶端識別碼 | 應用程式的唯讀、自動產生的唯一識別碼。 當實例要求存取權杖時，會使用用戶端識別碼。 | NA
用戶端密碼 | 使用此共用的機密字串，ServiceNow 實例和 Microsoft 搜尋會授權彼此間的通訊。 | 請將此視為密碼，遵循安全性最佳作法。
重新導向 URL | 授權伺服器重新導向所需的回撥 URL。 | https://gcs.office.com/v1.0/admin/oauth/callback
標誌 URL | 包含應用程式標誌之圖像的 URL。 | NA
作用中 | 選取此核取方塊，讓應用程式登錄成為使用中。 | 設定為 active
重新整理權杖生命週期 | 重新整理權杖有效的秒數。 根據預設，重新整理權杖會在100天內到期 (8640000 秒) 。 | 31536000 (1 年) 
存取權杖使用壽命 | 存取權杖有效的秒數。 | 43200 (12 小時) 

## <a name="set-a-sync-filter"></a>設定同步篩選

使用 sync 篩選，您可以指定同步處理文章的條件。 它就像是**SQL Select**語句中的**Where**子句。 例如，您可以選擇只為發佈和使用中的文章編制索引。 [SyncNow 設定] 頁面會說明如何捕獲和設定同步處理篩選。

## <a name="manage-the-search-schema"></a>管理搜尋結構描述

成功連接後，請設定搜尋架構對應。 您可以選擇哪些屬性可供**查詢**、可搜尋及可**供****檢索**。

## <a name="manage-search-permissions"></a>管理搜尋許可權

ServiceNow 連接器只支援 **所有人都**能看見的搜尋許可權。 已編制索引的資料會顯示在搜尋結果中，並對組織中的所有使用者顯示。

## <a name="set-the-refresh-schedule"></a>設定重新整理排程

ServiceNow 連接器支援完整和累加編目的更新排程。 我們建議您同時設定兩者。

完整編目排程會找到先前同步處理至 Microsoft 搜尋索引的已刪除文章，以及任何移出同步篩選的文章。 當您第一次連線至 ServiceNow 時，會執行完整編目以同步處理所有知識文庫文章。 若要同步處理新專案並進行更新，您必須排程累加編目。

建議的預設值為一天的完整編目及四小時為增量編目。
