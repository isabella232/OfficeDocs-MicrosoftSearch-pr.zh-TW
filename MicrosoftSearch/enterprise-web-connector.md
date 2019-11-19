---
title: Microsoft Search 的企業網站連接器
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
description: 設定 Microsoft Search 企業網站連接器
ms.openlocfilehash: 14eef035f4cc054ab87582b573cb6b7e3c12d0c7
ms.sourcegitcommit: 68087149c769a7cdde80944dd9c9933d2bf4a23f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/18/2019
ms.locfileid: "38699519"
---
# <a name="enterprise-websites-connector"></a>企業網站連接器

與企業網站連接器，您的組織可以索引文件和**其內部公開網站的內容**。 設定從網站的同步處理內容與連接器之後，使用者可以搜尋任何 Microsoft 搜尋用戶端從該內容。

本文適用於[Microsoft 365](https://www.microsoft.com/microsoft-365)系統管理員或人設定、 執行，並監視企業網站連接器。 本文說明如何設定連接器，連接器功能、 限制和疑難排解技巧。  

## <a name="connect-to-a-data-source"></a>連線至資料來源 
若要連線至您的資料來源，您需要您的根 URL 和形式的驗證： 基本驗證] 或 [OAuth 2.0 與[Azure Active Directory (Azure AD)](https://docs.microsoft.com/azure/active-directory/)。

### <a name="root-url"></a>根 URL
根 URL 是什麼初始編目，並驗證所使用。 您可以從您要編目之網站的 [首頁] 頁面上取得 URL。

### <a name="authentication"></a>驗證 
基本驗證需要使用者名稱和密碼。 使用 Microsoft 365[系統管理中心](https://admin.microsoft.com)來建立此 bot 帳戶。

與[Azure AD](https://docs.microsoft.com/azure/active-directory/)的 OAuth 2.0 需要租用戶識別碼、 資源識別碼、 用戶端識別碼和用戶端密碼。
如需詳細資訊，請參閱[Azure Active Directory 的 web 應用程式的授權存取使用 OAuth 2.0 的程式碼授與流程](https://docs.microsoft.com/azure/active-directory/develop/v1-protocols-oauth-code)。 註冊使用下列值：
* **名稱：** Microsoft Search
* **Redirect_URI:**`https://gcs.office.com/v1.0/admin/oauth/callback`

若要取得具名的租用戶中的值，資源、 client_id 和 client_secret，移至**使用授權程式碼，以要求存取權杖**重新導向 URL 網頁上。

更多的資訊，請參閱[快速入門： 註冊的應用程式與 Microsoft 身份識別平台](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app)。

### <a name="reverse-proxy-url"></a>反向 proxy URL 
企業網站連接器是雲端為基礎，所以它不會存取內部部署內容。 若要提供權限，請安裝反向 proxy。 反向 proxy 提供安全且可靠的存取權的內部網站。 我們建議您[Azure 應用程式 Proxy](https://docs.microsoft.com/azure/active-directory/manage-apps/application-proxy)。

根 URL 和驗證的反向 proxy 需求是雲端式的內容，如同不同之處在於反向 proxy 伺服器所提供的根 URL 和驗證。

請參閱[用來存取遠端與 Azure AD 應用程式 Proxy 的應用程式的安全性考量](https://docs.microsoft.com/azure/active-directory/manage-apps/application-proxy-security)。

## <a name="select-the-source-properties"></a>選取 [來源屬性 
來源內容被定義為基礎的企業網站的資料格式。 不過，您可以建立**排除清單中**排除某些 Url 如果取得編目內容是敏感或不值得編目。 若要建立排除清單中，瀏覽的根 URL。 您必須將排除的 Url 新增至清單中，在設定過程的選項。

## <a name="manage-search-permissions"></a>管理搜尋的權限 
沒有存取控制清單 (Acl) 支援。 因此，我們建議您連接可看見您的組織內的任何使用者的網站。

## <a name="set-the-refresh-schedule"></a>設定重新整理排程
企業網站連接器僅支援完整編目。 這表示，連接器會讀取所有網站的內容，每個編目期間。 若要確定連接器取得足夠的時間來閱讀的內容，我們建議您設定較大的重新整理排程的時間間隔。 建議的三天之間的兩週排定重新整理。

## <a name="limitations"></a>限制 
企業網站連接器不支援在動態網頁上的搜尋資料。 範例的這些網頁存在於內容管理系統，例如[機器人學](https://www.atlassian.com/software/confluence)和[Unily](https://www.unily.com/)或儲存網站內容的資料庫中。