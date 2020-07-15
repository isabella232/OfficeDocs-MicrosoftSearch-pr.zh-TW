---
title: Microsoft 搜尋的企業網站連接器
ms.author: mounika.narayanan
author: monaray
manager: mnirkhe
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 設定 Microsoft 搜尋的企業網站連接器
ms.openlocfilehash: fcda5db9b294e3d70bb27879f1bb0efb43ad6936
ms.sourcegitcommit: 0b5e3764822f64532c8a8e14b8e56e35141a558d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/14/2020
ms.locfileid: "45127639"
---
# <a name="enterprise-websites-connector"></a>企業網站連接器

透過企業網站連接器，您的組織可以**從其內部網站**對文章和內容編制索引。 在您設定網站的連接器及同步內容之後，使用者可以從任何 Microsoft 搜尋用戶端搜尋該內容。

本文適用于[Microsoft 365](https://www.microsoft.com/microsoft-365)系統管理員或任何設定、執行及監視企業網站連接器的人員。 它說明如何設定連接器和連接器功能、限制及疑難排解技術。  

## <a name="connect-to-a-data-source"></a>連接到資料來源 
若要連線至資料來源，您需要根 URL 和驗證格式：無、基本驗證，或使用[Azure Active Directory （AZURE AD）](https://docs.microsoft.com/azure/active-directory/)的 OAuth 2.0。

### <a name="authentication"></a>驗證 
基本驗證需要使用者名稱和密碼。 使用 Microsoft 365 系統[管理中心](https://admin.microsoft.com)建立此 bot 帳戶。

使用[AZURE AD](https://docs.microsoft.com/azure/active-directory/) OAuth 2.0 需要資源識別碼、用戶端識別碼和用戶端密碼。

如需詳細資訊，請參閱[使用 OAuth 2.0 程式碼授與流程授權存取 Azure Active Directory web 應用程式](https://docs.microsoft.com/azure/active-directory/develop/v1-protocols-oauth-code)。 使用下列值進行註冊：

**名稱：** Microsoft 搜尋 <br/>
**Redirect_URI：**`https://gcs.office.com/v1.0/admin/oauth/callback`

若要取得資源、client_id 及 client_secret 的值，請移至**使用授權碼以要求**重新導向 URL 網頁上的存取權杖。

如需詳細資訊，請參閱[快速入門：使用 Microsoft identity Platform 註冊應用程式](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app)。

### <a name="root-url"></a>根 URL
根 URL 會啟動編目，並用於驗證。 您可以從您想要編目的網站首頁取得 URL。

## <a name="select-the-source-properties"></a>選取來源屬性 
來源屬性是根據企業網站的資料格式定義。 不過，您可以建立**排除清單**，以排除部分 URLs 若該內容機密或不需要編目的情況下取得編目。 若要建立排除清單，請流覽根 URL。 您可以選擇在設定過程中將排除的 URLs 新增至清單。

## <a name="manage-search-permissions"></a>管理搜尋許可權 
不支援存取控制清單（ACLs）。 因此，我們建議您只連接組織內任何使用者都能看見的網站。

## <a name="set-the-refresh-schedule"></a>設定重新整理排程
企業網站連接器只支援完整編目。 這表示連接器會在每次編目期間讀取網站的所有內容。 若要確定連接器有足夠的時間可讀取內容，建議您設定大型重新整理排程間隔。 建議您在一到兩周之間進行排程重新整理。

## <a name="troubleshooting"></a>疑難排解
當閱讀網站內容時，編目可能會遇到下列的詳細錯誤碼所代表的部分來源錯誤。 若要取得錯誤類型的詳細資訊，請在選取連接後，移至 [**錯誤詳細資料**] 頁面。 按一下**錯誤碼**以查看更詳細的錯誤。 此外，請參閱[管理您的連接器](https://docs.microsoft.com/microsoftsearch/manage-connector)以深入瞭解。

 詳細錯誤代碼 | 錯誤訊息
 --- | --- 
 6001   | 無法連線正在嘗試編制索引的網站 
 6005 | 根據 robots.txt 設定，已封鎖嘗試編制索引的來源頁面。
 6008 | 無法解析 DNS
 6009 | 針對所有用戶端錯誤（除 HTTP 404、408之外），請參閱 HTTP 4xx 錯誤碼以取得詳細資訊。
 6013 | 找不到嘗試編制索引的來源頁面。 （HTTP 404 錯誤）
 6018 | 來源頁面沒有回應，且要求超時。（HTTP 408 錯誤）
 6021 | 嘗試編制索引的來源頁面沒有頁面上的文字內容。
 6023 | 不支援所嘗試編制索引的來源頁面（非 HTML 頁面）
 6024 | 嘗試編制索引的來源頁面具有不支援的內容。

* 當資料來源由於網路問題或資料來源本身被刪除、移動或重新命名時，就會發生錯誤6001-6013。 檢查提供的資料來源詳細資料是否仍然有效。
* 當資料來源包含頁面上的非文字內容或頁面不是 HTML 時，就會發生錯誤6021-6024 錯誤。 請檢查資料來源，並將此頁面加入排除清單，或略過錯誤。

## <a name="limitations"></a>限制
企業網站連接器不支援搜尋**動態網頁**上的資料。 [Confluence](https://www.atlassian.com/software/confluence)與[Unily](https://www.unily.com/)等內容管理系統中的這些網頁範例，或儲存網站內容的資料庫。
