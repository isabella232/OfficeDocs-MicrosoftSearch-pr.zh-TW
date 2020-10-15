---
title: 設定 microsoft 內置的連接器以進行 Microsoft 搜尋
ms.author: monaray
author: monaray97
manager: jameslau
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 設定 microsoft 內置的連接器以進行 Microsoft 搜尋
ms.openlocfilehash: ce2515b3eaa859a8fbb00d83c4727865ab55e174
ms.sourcegitcommit: 6aea7102c94855e9f80711c0f3d7bf5833ce8fb5
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/14/2020
ms.locfileid: "48464474"
---
<!-- markdownlint-disable no-trailing-punctuation -->

# <a name="set-up-your-microsoft-built-connector-for-microsoft-search"></a>設定 microsoft 內建的連接器以進行 Microsoft 搜尋

本文將引導您逐步完成設定 Microsoft 內建連接器的步驟。 它概述在 Microsoft 365 系統 [管理中心](https://admin.microsoft.com)中設定連線的流程。 如需如何設定特定 Microsoft 內置連接器的詳細資訊，請參閱下列文章：

* [Azure Data Lake Storage Gen2](azure-data-lake-connector.md)
* [Azure DevOps](azure-devops-connector.md)
* [Azure SQL](MSSQL-connector.md)
* [企業網站](enterprise-web-connector.md)
* [MediaWiki](mediawiki-connector.md)
* [Microsoft SQL server](MSSQL-connector.md)
* [ServiceNow](servicenow-connector.md)

## <a name="set-up"></a>設定

完成下列步驟以設定任何 Microsoft 建立的連接器。

1. 移至[Microsoft 365 系統管理中心](https://admin.microsoft.com)中的 [[連接器]](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors)索引標籤。
2. 使用 [Microsoft 365](https://www.microsoft.com/microsoft-365) 租使用者的認證登入您的帳戶。
3. 選取 [ **新增連接器**]。
4. 從可用的連接器清單中，選取您選擇的連接器。

![可用的資料來源包括： Azure DevOps Connector、ServiceNow、ADLS Gen2、Enterprise 網站、MediaWiki、Microsoft SQL server 和 Azure SQL。](media/add_connector.png)

### <a name="name-the-connector"></a>命名連接器

若要建立連接，請先指定下列屬性：

1. 連接的名稱
2. 連接識別碼
3. Description (optional) 

連接識別碼會建立連接器的隱含屬性。 它必須只包含字母數位字元，最多可以有32個字元。

### <a name="connect-to-a-data-source"></a>連接到資料來源

資料連線過程會根據連接器類型而有所不同。 若要深入瞭解如何連線至您的內部部署資料來源，請參閱 [安裝內部部署資料閘道](https://aka.ms/configuregateway)。

### <a name="select-source-properties"></a>選取來源屬性

協力廠商資料來源所設定的資料欄位會在 Microsoft 搜尋中編入來源屬性。 若要修改這些屬性，請選取 [**連接器**] 頁面右邊的側欄中的 [**編輯屬性**]。 您 **最多可以選擇64來源屬性**。

### <a name="manage-the-search-schema"></a>管理搜尋結構描述

#### <a name="content-property"></a>Content 屬性

您可以從**content**屬性下拉式清單中選取任何 string 屬性，以選取 [**內容**] 屬性 (專案) 的全文檢索索引。 或者，您可以保留預設的選取屬性（如果有的話）。

請務必選取正確的屬性，因為此屬性是用於內容的全文檢索索引、搜尋結果頁面片段產生、語言偵測、HTML/文字支援、排名與相關性，以及查詢表述。

如果您選取**內容**的屬性，當您[建立結果類型](customize-results-layout.md)時，可以選擇使用系統所產生的屬性**ResultSnippet** 。 此屬性用作在查詢時從 **content** 屬性產生之動態程式碼片段的預留位置。 如果您在結果類型中使用此屬性，則會在搜尋結果中產生程式碼片段。

#### <a name="search-schema-attributes"></a>搜尋架構屬性

您可以設定搜尋架構屬性，以控制每個來源屬性的搜尋功能。 搜尋架構可協助決定搜尋結果頁面上顯示的結果，以及使用者可以查看和存取哪些資訊。

搜尋架構屬性包括可搜尋、可**查詢**及可**供****檢索**的屬性。 下表列出 Microsoft Graph 連接器所支援的每個屬性，並說明其功能。

搜尋架構屬性 | 函數 | 範例
--- | --- | ---
搜索 | 使屬性的文字內容可供搜尋。 屬性內容會包含在全文檢索索引中。 | 若屬性為 **title**， **企業** 查詢會傳回包含 word Enterprise 的任何文字或標題中的 word **enterprise** 的查詢。
可 | 依查詢搜尋特定屬性的相符。 您可以在查詢中以程式設計方式或逐字方式指定屬性名稱。 |  若 **Title** 屬性是可查詢的，則支援查詢 **標題： Enterprise** 。
檢索 | 在結果類型中只能使用可檢索的屬性，並顯示在搜尋結果中。 |

針對所有連接器，必須手動設定自訂類型。 若要啟動每個欄位的搜尋功能，您需要對應至屬性清單的搜尋架構。 連接嚮導會根據您所選擇的來源屬性集，自動選取搜尋架構。 您可以在 [搜尋架構] 頁面中選取每個屬性和屬性的核取方塊，以修改此架構。

![您可以新增或移除查詢、搜尋及檢索功能，以自訂連接器的架構。](media/manageschema.png)

#### <a name="restrictions-and-recommendations-for-search-schema-settings"></a>搜尋架構設定的限制與建議

* **Content**屬性僅可供搜尋。 在下拉式清單中選取此屬性後，就無法將此屬性標示為可 **檢索** 或可 **查詢**。 使用 **content** 屬性來呈現搜尋結果時，會發生重大效能問題。 範例是[ServiceNow](https://www.servicenow.com)知識文庫文章的 [**文字**內容] 欄位。

* 在搜尋結果中，只有標示為可檢索的屬性，而且可以用來 (MRTs) 建立新式結果類型。

* 只能將字串屬性標示為可搜尋。


> [!Note]
> 建立連線之後，就 **無法** 修改架構。 若要這麼做，您必須刪除您的連線，並建立新的連線。

### <a name="manage-search-permissions"></a>管理搜尋許可權

 (ACLs 的存取控制清單) 決定組織中的哪些使用者可以存取每個資料項目目。 所有的連接器都支援所有使用者皆可看到的搜尋許可權。

### <a name="set-the-refresh-schedule"></a>設定重新整理排程

重新整理排程會決定您的資料與 Microsoft Graph 和 Microsoft 搜尋中的索引同步處理的頻率。 您可以透過兩種方式排程重新整理：完整編目或累加編目。

使用 **完整**編目時，搜尋引擎會處理及索引內容來源中的每個專案，而不論先前的編目。 在下列情況下，完整編目的運作方式最為好：

* 偵測資料刪除。
* 增量式編目無法編目錯誤的內容。
* 已修改 ACLs。
* 已修改編目規則。
* Microsoft 搜尋的軟體更新是必要的。 更新會修改搜尋架構。

使用累加編目 **時，搜尋**引擎只可以處理和編制自上次成功編目之後所建立或修改的專案。 因此，不會重新索引內容來源中的所有資料。 增量式編目最適合偵測內容、中繼資料、許可權及其他更新。

因為未處理未變更的專案，所以增量編目的速度會比完全編目快許多。 若要維護內容來源與搜尋索引之間的準確資料同步處理，您必須定期執行這兩個編目。

每個連接器都會有一組不同的最佳重新整理排程，取決於修改資料的頻率及修改的類型。

![累加編目和完整編目間隔設定會顯示增量為15分鐘，在1周完全編目。](media/refreshschedule.png)

### <a name="review-connector-settings"></a>檢查連接器設定

設定連接器之後，系統 [管理中心](https://admin.microsoft.com) 會帶您前往可供您複查設定的頁面。 您可以回到設定程式來編輯任何設定，再確認連接。 若要深入瞭解，請參閱 [管理您的連接器](manage-connector.md)。

## <a name="next-steps-customize-the-search-results-page"></a>後續步驟：自訂搜尋結果頁面

透過 Microsoft Search 使用者介面 (UI) ，您的使用者可以從您的 [microsoft 365](https://www.microsoft.com/microsoft-365) 生產力應用程式和更廣泛的 microsoft 生態應用程式中搜尋內容。 搜尋類別是指使用者在 [SharePoint](https://sharepoint.com/)、 [Microsoft Office](https://Office.com)及 [Bing](https://Bing.com)中的 microsoft 搜尋中查看其搜尋結果時所顯示的索引標籤。 您可以自訂搜尋範圍來縮小結果，如此只會顯示特定類型的搜尋結果。 這些縱向顯示為搜尋結果頁面頂端的 tab 鍵。  (MRT.LOG) 的現代結果類型是指定結果呈現方式的 UI。

建立您自己的行業和結果類型，讓使用者可以從新的連線中查看搜尋結果。 在此步驟中，您的連線中的資料不會顯示在搜尋結果頁面上。

若要深入瞭解如何建立您的行業和 MRTs，請參閱 [搜尋結果頁面自訂](customize-search-page.md)。

## <a name="how-do-i-know-the-connection-setup-worked"></a>如何知道連線設定是否運作正常？

在系統[管理中心](https://admin.microsoft.com)的 [**連接器**] 索引標籤下，移至您發佈的連線清單。 若要瞭解如何進行更新和刪除，請參閱 [管理您的連接器](manage-connector.md)。
