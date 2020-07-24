---
title: 連接器概述
ms.author: mounika.narayanan
author: monaray
manager: shohara
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: Microsoft 搜尋的 Microsoft Graph 連接器概述
ms.openlocfilehash: ecedd135336f37da26cee71be06dd421cdb95f61
ms.sourcegitcommit: f2323c43fc732890213223efac32006df5b92c28
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/23/2020
ms.locfileid: "45387992"
---
# <a name="overview-of-microsoft-graph-connectors"></a>Microsoft Graph 連接器的概述

Microsoft 搜尋會索引您的所有[Microsoft 365](https://www.microsoft.com/microsoft-365)資料，讓其可供使用者搜尋。 使用 Microsoft Graph 連接器，貴組織可以將協力廠商資料編制索引顯示在 Microsoft 搜尋結果中。 協力廠商資料可以位於內部部署或公用或私人雲端。 連接器展開可在 Microsoft 365 生產力應用程式中搜尋的內容來源類型，以及更廣泛的 Microsoft 生態用。

> [!IMPORTANT]
> **免責聲明**： microsoft Graph 連接器和 microsoft Search APIs （查詢和索引）目前是針對目標版本中承租人可用的預覽狀態。 若要在 Microsoft 搜尋中使用連接器，或建立連接器，請選擇進入[目標版本](https://docs.microsoft.com/office365/admin/manage/release-options-in-office-365?view=o365-worldwide)。 若要深入瞭解預覽，請參閱[連接器預覽程式](connectors-preview.md)。

## <a name="architecture"></a>架構

Microsoft Graph 平臺的下列架構圖表顯示在[Microsoft Search](https://docs.microsoft.com/microsoftsearch/overview-microsoft-search)用戶端中，連接器內容如何透過內容索引傳送至使用者結果。 本文說明 Microsoft Graph 連接器資料流程處理常式中的每個主要組建區塊。

![圖表：內部部署和雲端式資料是由連接器所提取，並由 Microsoft Search API 編制索引，然後 Microsoft Search 服務會將結果傳遞給使用者。](media/highlevel-connectors_FINAL.png)

API 會為每個資料來源具現化一個連接。 然後，API 便會編制索引並儲存資料。 已建立的連線會與 Microsoft 搜尋互動，讓使用者可以取得搜尋結果。

您可以在 Microsoft 365 系統[管理中心](https://admin.microsoft.com)內設定所有的 microsoft 建連接器。 系統管理中心簡化了使用簡易使用者介面設定連接器的工作。

若要建立資料**源的連線**，系統管理員必須對資料和整個內容存放庫進行驗證存取。 資料會送到圖形連接器服務以編制索引。

## <a name="available-connectors"></a>可用連接器

目前有6個 Microsoft 構建的連接器，而且我們的生態系統合作夥伴可提供超過100的連接器。

若要從其中一個生態系統合作夥伴預覽連接器，請直接與他們聯繫。 如需詳細資訊，請參閱[Microsoft Graph 連接器圖庫](connectors-gallery.md)。

您也可以[建立您自己的連接器](https://docs.microsoft.com/graph/search-concept-overview)。

### <a name="connectors-by-microsoft"></a> Microsoft 連接器

Microsoft Graph 連接器預覽版本包含6個 Microsoft 建立的連接器。 您可以在系統[管理中心](https://admin.microsoft.com)進行設定，並瞭解如何[設定您的 Microsoft 建連接器](configure-connector.md)。

下列各節提供這些 Microsoft 建立連接器的簡短描述。 您可以在每個連接器的連結文章中取得詳細資訊。

- **[Azure Data Lake Storage Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction)**。 透過此 Microsoft Graph 連接器，您組織中的使用者可以搜尋 Azure Blob 容器中儲存的檔案和內容。 Azure Data Lake Storage Gen2 connector 也會為您指定的 Azure Data Lake Storage Gen2 帳戶中的已啟用階層的資料夾編制索引。
深入瞭解[Azure Data Lake Storage Gen2 connector](azure-data-lake-connector.md)。

- **[Azure DevOps](https://azure.microsoft.com/services/devops)**。 使用此 Microsoft Graph 連接器，您組織中的使用者可以搜尋 Azure DevOps 實例中的工作專案。
深入瞭解[Azure DevOps 連接器](azure-devops-connector.md)。

- **[AZURE SQL](https://azure.microsoft.com/services/sql-database)**。 透過此 Microsoft Graph 連接器，您組織中的使用者可以從 Azure SQL 資料庫搜尋資料。
深入瞭解[AZURE SQL connector](MSSQL-connector.md)。

- **企業網站**。 透過此 Microsoft Graph 連接器，您組織中的使用者可以在任何非 SharePoint 企業網站中搜尋頁面。
深入瞭解[企業網站連接器](enterprise-web-connector.md)。

- **[MediaWiki](https://www.mediawiki.org/wiki/MediaWiki)**。 使用此 Microsoft Graph 連接器，使用者可以在您的組織以 MediaWiki 所建立的 wiki 網站上搜尋知識文庫文章。
深入瞭解[MediaWiki 連接器](mediawiki-connector.md)。

- **[MICROSOFT SQL server](https://www.microsoft.com/sql-server/sql-server-2017)**。 透過此 Microsoft Graph 連接器，您組織中的使用者可以搜尋內部部署 SQL server 資料庫中的資料。
深入瞭解[MICROSOFT SQL server connector](MSSQL-connector.md)。

- **[ServiceNow](https://www.servicenow.com)**。 透過此 Microsoft Graph 連接器，您組織中的使用者可以從您的 ServiceNow 實例搜尋知識庫文章。
深入瞭解[ServiceNow 連接器](servicenow-connector.md)。

### <a name="connectors-from-our-partners"></a>合作夥伴的連接器

我們的生態系統合作夥伴可供預覽超過100個連接器。 若要從其中一個生態系統合作夥伴預覽連接器，請直接與他們聯繫。
深入瞭解[Microsoft Graph 連接器圖庫](connectors-gallery.md)中合作夥伴的連接器。

### <a name="build-your-own-connector"></a>建立您自己的連接器

若要編制自訂資料類型或檔案的索引，開發人員可以在[Microsoft Graph](https://developer.microsoft.com/graph/)中建立連接器。 連接器是[建立](https://docs.microsoft.com/graph/search-index-manage-connections)連線並將專案推入 Microsoft 搜尋索引的應用程式。 如需詳細資訊，請參閱[為 Microsoft Graph 上的應用程式擴充 Microsoft 搜尋體驗的概述](https://docs.microsoft.com/graph/search-concept-overview)。

### <a name="search-results-with-your-custom-built-connector"></a>使用自訂內置連接器的搜尋結果

在索引自訂資料之後，開發人員可以[查詢此資料](https://docs.microsoft.com/graph/search-concept-custom-types)。 您可以在任何應用程式中查看資料。 如需詳細資訊，請參閱[為 Microsoft Graph 上的應用程式擴充 Microsoft 搜尋體驗的概述](https://docs.microsoft.com/graph/search-concept-overview)。

## <a name="license-requirements"></a>授權需求

若要在搜尋結果中查看連接器的資料，使用者必須具備下列其中一項 Microsoft 365 或 Office 365 訂閱：

- [Microsoft 365 或 Office 365 企業版 E3 或 E5](https://www.microsoft.com/microsoft-365/compare-all-microsoft-365-plans)

- [Microsoft 365 或 Office 365 教育版 A3 或 A5](https://www.microsoft.com/microsoft-365/academic/compare-office-365-education-plans?activetab=tab:primaryr1)
