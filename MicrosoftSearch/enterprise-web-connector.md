---
title: Enterprise Microsoft 搜尋的網站 Graph 連接器
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
description: 設定 Enterprise 的網站 Graph 連接器 Microsoft 搜尋
ms.openlocfilehash: 32e38c9bef036556dae2734e23b1d26ba4fe2c27
ms.sourcegitcommit: 38a0f09596c2bca0e12bf4cada7b4c64fd4c48e4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/15/2021
ms.locfileid: "53449043"
---
<!---Previous ms.author: monaray --->

<!-- markdownlint-disable no-inline-html -->

# <a name="enterprise-websites-graph-connector"></a>Enterprise 網站 Graph 連接器

Enterprise 網站 Graph 連接器可讓您的組織編制 **來自內部網站** 的文章和內容。 從網站設定連接器及同步內容之後，使用者可以從任何 Microsoft 搜尋用戶端搜尋該內容。

> [!NOTE]
> 請閱讀 [**設定 Graph 連接器**](configure-connector.md)文章，以瞭解一般 Graph 連接器設定指示。

本文適用于任何設定、執行及監視 Enterprise 網站連接器的人員。 它會補充一般設定程式，並顯示只適用于 Enterprise 網站連接器的指示。 本文也包含 [疑難排解](#troubleshooting)的相關資訊。

<!---## Before you get started-->

<!---Insert "Before you get started" recommendations for this data source-->

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a>步驟1：在 Microsoft 365 系統管理中心中新增 Graph 連接器

遵循一般 [設定指示](./configure-connector.md)。
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-2-name-the-connection"></a>步驟2：命名連線

遵循一般 [設定指示](./configure-connector.md)。
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-3-configure-the-connection-settings"></a>步驟3：設定連接設定

若要連線至您的資料來源，請填入網站的根 URL、選擇編目來源，以及您想要使用的驗證類型： [無]、[基本驗證]，或 OAuth 2.0 搭配[Azure Active Directory (Azure AD) ](/azure/active-directory/)。 在您完成此資訊之後，請選取 [測試連線] 以驗證您的設定。

### <a name="url"></a>URL

使用 [URL] 欄位可指定您要編目之網站的根目錄。 企業網站連接器會使用此 URL 做為開始點，並遵循此 URL 的所有連結進行編目。

### <a name="crawl-websites-listed-in-the-sitemap"></a>編目網站地圖中所列的網站

選取此選項時，連接器只會編目網站地圖中所列的 URLs。 若未選取或未找到任何網站圖形，連接器將會對該網站的根 URL 所找到的所有連結進行深入編目。

### <a name="dynamic-site-configuration"></a>動態網站設定

例如，如果您的網站包含動態內容，例如 Confluence 或 Unily 等內容管理系統中的網頁，您可以啟用動態編目程式。 若要將其開啟，請選取 [ **啟用動態網站的** 編目]。 編目程式會在開始編目之前，等待動態內容進行轉譯。

> [!div class="mx-imgBorder"]
> ![Enterprise 網頁連接器之連線設定窗格的螢幕擷取畫面](media/enterprise-web-connector/connectors-enterpriseweb-connectionsettings-dynamicconfig-small.png)

除了核取方塊之外，還有三個可供選用的欄位：

1. **Dom 就緒**：輸入 dom 專案，編目程式應使用它做為內容完全呈現及編目應該開始的信號。
1. **要新增的標頭**：指定編目程式在傳送該特定 web URL 時應包含的 HTTP 標頭。 您可以為不同的網站設定多個標頭。 建議包括 auth token 值。
1. **略過標頭**：指定應從動態編目要求排除的任何不必要標頭。

> [!NOTE]
> 只有代理程式編目模式支援動態編目。

### <a name="crawl-mode-cloud-or-on-premises"></a>編目模式：雲端或內部部署

編目模式會決定您要建立索引的網站類型（雲端或內部部署）。 針對您的雲端網站，選取 **雲端** 做為編目模式。

此外，連接器現在也支援對內部部署網站進行編目。 若要存取您的內部部署資料，您必須先安裝及設定 Graph 連接器代理程式。 若要深入瞭解，請參閱[Graph connector agent](./on-prem-agent.md)。

若為您的內部部署網站，請選取 [**代理程式**] 做為編目模式，並在 [部署中的 **代理程式**] 欄位中，選擇您先前安裝及設定的 Graph 連接器代理程式。  

### <a name="authentication"></a>驗證

基本驗證需要使用者名稱和密碼。 使用[Microsoft 365 系統管理中心](https://admin.microsoft.com)建立此 bot 帳戶。

使用 [AZURE AD](/azure/active-directory/) OAuth 2.0 需要資源識別碼、用戶端識別碼和用戶端密碼。 OAuth 2.0 僅適用于雲端模式。

如需詳細資訊，請參閱[使用 OAuth 2.0 代碼授與流程授權存取 Azure Active Directory web 應用程式](/azure/active-directory/develop/v1-protocols-oauth-code)。 使用下列值進行註冊：

**名稱：** Microsoft 搜尋 <br/>
**Redirect_URI：**`https://gcs.office.com/v1.0/admin/oauth/callback`

若要取得資源、client_id 及 client_secret 的值，請移至 **使用授權碼以要求** 重新導向 URL 網頁上的存取權杖。

如需詳細資訊，請參閱[快速入門：使用 Microsoft 身分識別平臺註冊應用程式](/azure/active-directory/develop/quickstart-register-app)。

## <a name="step-3a-add-urls-to-exclude-optional-crawl-restrictions"></a>步驟3a：新增 URLs 以排除 (選擇性編目限制) 

有兩種方式可以避免網頁進行編目：在 robots.txt 檔案中禁止這些頁面，或將其新增至排除清單。

### <a name="support-for-robotstxt"></a>robots.txt 的支援

連接器會檢查您的根網站是否有 robots.txt 檔案，如果有的話，則會依照該檔案中所發現的指示來查看。 如果您不想讓連接器編目網站上的某些頁面或目錄，您可以在 robots.txt 檔案中的「禁止」宣告中呼叫這些頁面或目錄。

### <a name="add-urls-to-exclude"></a>新增要排除的 URLs

您可以選擇性地建立 **排除清單** ，以排除部分 URLs 若該內容機密或不值得編目的情況，則無法取得編目。 若要建立排除清單，請流覽根 URL。 您可以在設定過程中將排除的 URLs 新增至清單。

## <a name="step-4-assign-property-labels"></a>步驟4：指派屬性標籤

您可以從選項的功能表中選擇，將 source 屬性指派給每個標籤。 雖然這個步驟不是必要的，但具有一些屬性標籤會提升搜尋相關性，並確保使用者可以更精確的搜尋結果。

## <a name="step-5-manage-schema"></a>步驟5：管理架構

在 [ **管理架構** ] 畫面上，您可以變更架構屬性 (選項包括「 **查詢**」、「 **搜尋**」、「 **檢索**」及「 **精煉** 」與屬性相關聯的) 、新增選用的別名，然後選擇 **Content** 屬性。

## <a name="step-6-manage-search-permissions"></a>步驟6：管理搜尋許可權

Enterprise 網站連接器只支援 **所有人都** 能看見的搜尋許可權。 已編制索引的資料會顯示在搜尋結果中，並對組織中的所有使用者顯示。

## <a name="step-7-set-the-refresh-schedule"></a>步驟7：設定重新整理排程

Enterprise 網站連接器只支援完整重新整理。 這表示連接器會在每次重新整理時重新編目網站的所有內容。 若要確定連接器有足夠的時間來編目內容，建議您設定大型重新整理排程間隔。 建議您在一到兩周之間進行排程重新整理。

## <a name="step-8-review-connection"></a>步驟8：檢查連線

遵循一般 [設定指示](./configure-connector.md)。
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="troubleshooting"></a>疑難排解

當閱讀網站內容時，編目可能會遇到一些來源錯誤，這些錯誤是由下列詳細的錯誤碼所代表。 若要取得錯誤類型的詳細資訊，請在選取連接後，移至 [ **錯誤詳細資料** ] 頁面。 選取 **錯誤碼** 以查看更詳細的錯誤。 此外，請參閱 [管理您的連接器](./manage-connector.md) 以深入瞭解。

 詳細錯誤代碼 | 錯誤訊息
 --- | ---
 6001 | 無法連線正在嘗試編制索引的網站
 6005 | 根據 robots.txt 設定，已封鎖嘗試編制索引的來源頁面。
 6008 | 無法解析 DNS
 6009 | 針對所有用戶端錯誤 (除 HTTP 404、408) 以外，請參閱 HTTP 4xx 錯誤碼以取得詳細資訊。
 6013 | 找不到嘗試編制索引的來源頁面。  (HTTP 404 錯誤) 
 6018 | 來源頁面沒有回應，且要求超時。 (HTTP 408 錯誤) 
 6021 | 嘗試編制索引的來源頁面沒有頁面上的文字內容。
 6023 | 嘗試編制索引的來源頁面不受支援 (不是 HTML 頁面) 
 6024 | 嘗試編制索引的來源頁面具有不支援的內容。

* 當資料來源由於網路問題或資料來源本身被刪除、移動或重新命名時，就會發生錯誤6001-6013。 檢查提供的資料來源詳細資料是否仍然有效。
* 當資料來源包含頁面上的非文字內容或頁面不是 HTML 時，就會發生錯誤6021-6024。 請檢查資料來源，並將此頁面加入排除清單，或略過錯誤。
