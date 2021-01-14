---
title: 連接器概述
ms.author: monaray
author: monaray97
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
ms.openlocfilehash: 677c91f121185faa6dc96f80c517917f429a3ab0
ms.sourcegitcommit: 469be70ad295a5837978d75babf5243115257f77
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/13/2021
ms.locfileid: "49847517"
---
# <a name="overview-of-microsoft-graph-connectors"></a>Microsoft Graph 連接器的概述

[Microsoft 搜尋](https://docs.microsoft.com/microsoftsearch/overview-microsoft-search) 會索引您的所有 [Microsoft 365](https://www.microsoft.com/microsoft-365) 資料，讓其可供使用者搜尋。 透過 Microsoft Graph 連接器，您的組織可以編制協力廠商資料的索引，使其出現在 Microsoft 搜尋結果中。 這可展開 Microsoft 365 生產力應用程式中可搜尋的內容來源類型，以及更廣泛的 Microsoft 生態用。 協力廠商資料可以位於內部部署或公用或私人雲端。

<!---link Microsoft Graph reference in line 19 when we have access to relevant documentation--->

本文的其餘部分是為了協助 Microsoft 365 系統管理員找出可用來回答下列問題的資源：

* [哪些資料來源可連接至 Microsoft 搜尋？](#what-data-sources-can-be-connected-to-microsoft-search)
* [如何管理連線？](#how-do-i-manage-my-connections)
* [圖形連接器的授權需求和使用期限為何？](#what-are-the-license-requirements-and-terms-of-use-for-graph-connectors)
* [如何自訂及設定搜尋結果？](#how-do-i-customize-and-configure-search-results)
* [如何從自訂應用程式搜尋我的連接器資料？](#how-do-i-search-my-connector-data-from-a-custom-application)

<!---Modify to another note that is more accurate--->
> [!IMPORTANT]
> 現在一般會提供 microsoft Graph 連接器和 Microsoft Search APIs。 第一次部署是針對目標版本所設定的客戶。 如果您想要在租使用者中使用圖形連接器，使用者和系統管理員必須選擇已 [目標發行](https://docs.microsoft.com/office365/admin/manage/release-options-in-office-365?view=o365-worldwide&preserve-view=true)。

<!---Add Value, scenario, example, and/or graphic in December updates--->
<!---Probably remove architecture section below
## Architecture

The following architectural diagram of the Microsoft Graph platform shows how Graph connector content flows through content indexing to user results in [Microsoft Search](https://docs.microsoft.com/microsoftsearch/overview-microsoft-search) clients. The rest of this section explains each of the key building blocks in the diagram.

![Diagram: on-premises and cloud-based data is pulled by connectors and indexed by the Microsoft Search API, and then the Microsoft Search service delivers the results to users.](media/connectors-overview/highlevel-connectors.png)
Graph connectors can pull data from cloud-based (SaaS) data sources and on-premises data stores. The above diagram shows connections to only two data sources, but you can add connections to up ten sources per tenant.

The Microsoft Graph Connectors API instantiates one connection per data source. Then, the API indexes and stores the data. Established connections interact with Microsoft Search, so users can get search results.

You can use the Microsoft 365 [admin center](https://admin.microsoft.com) to setup and manage any of the Graph connectors by Microsoft. The admin center has a simple user interface that makes it easy to establish the connection to your data source, and monitor connection status and utilization.

***Edit paragraph below**_
To create a _*connection** to a data source, admins need authenticated access to the data and the entire content repository. The data is fed to the graph connector service for indexing.--->

## <a name="what-data-sources-can-be-connected-to-microsoft-search"></a>哪些資料來源可連接至 Microsoft 搜尋？

Microsoft 提供10個圖形連接器和我們的生態系統合作夥伴已透過100其他圖形連接器建立。 您也可以建立自己的圖形連接器。 

### <a name="graph-connectors-by-microsoft"></a>Microsoft Graph 連接器

您可以使用 Microsoft 所建立的圖形連接器，連線到下列資料來源：

<!---Need to add a few links below when docs exist--->
* [Azure Data Lake Storage Gen2](azure-data-lake-connector.md)
* [Azure DevOps](azure-devops-connector.md)
* Azure SQL
* [企業網站](enterprise-web-connector.md)
* [MediaWiki](mediawiki-connector.md)
* [Microsoft SQL Server](MSSQL-connector.md)
* [檔案共用](fileshare-connector.md)
* Oracle (預覽) 
* [Salesforce (預覽)](salesforce-connector.md)
* [ServiceNow](servicenow-connector.md)

[圖形連接器圖庫](connectors-gallery.md)包含每個圖形連接器的簡短描述。 如果您已準備好將其中一個資料來源連接至您的租使用者，請務必閱讀適用于資料來源之 Microsoft 安裝連接器中的 [安裝程式概述](configure-connector.md) 和任何其他文章。

### <a name="graph-connectors-by-our-partners"></a>合作夥伴的圖形連接器

[Microsoft Graph 連接器圖庫](connectors-gallery.md)包含合作夥伴所建立之每個圖形連接器的簡短說明，以及每個合作夥伴網站的連結。 請直接聯繫每個合作夥伴以深入瞭解。

### <a name="build-your-own-graph-connector"></a>建立您自己的圖形連接器

如果您想要建立自己的圖形連接器，請參閱 microsoft [graph 中的 Microsoft SEARCH API 概述](https://docs.microsoft.com/graph/search-concept-overview) ，以取得詳細資訊。

## <a name="how-do-i-manage-my-connections"></a>如何管理連線？

您可以從[Microsoft 365 系統管理中心](https://admin.microsoft.com/)的 [[連接器]](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors)索引標籤管理連線。 如需詳細資訊，請參閱 [Manage a connections](manage-connector.md) 。

## <a name="what-are-the-license-requirements-and-terms-of-use-for-graph-connectors"></a>圖形連接器的授權需求和使用期限為何？

您為組織中的使用者需要有效的 Microsoft 365 或 Office 365 授權和足夠的圖形連接器配額，以在其搜尋結果中查看連接器的資料。

若要深入瞭解，請參閱 [授權需求和價格](licensing.md) 與 [使用條款](terms-of-use.md)。

## <a name="how-do-i-customize-and-configure-search-results"></a>如何自訂及設定搜尋結果？

有許多方式可自訂及設定搜尋結果。 若要深入瞭解，請參閱下列文章：

* [管理類別和結果類型](customize-search-page.md)
* [管理搜尋結果版面配置](customize-results-layout.md)
* [管理結果叢集](result-cluster.md)
* [管理自訂篩選](custom-filters.md)

## <a name="how-do-i-search-my-connector-data-from-a-custom-application"></a>如何從自訂應用程式搜尋我的連接器資料？

在索引自訂資料之後，開發人員可以 [查詢此資料](https://docs.microsoft.com/graph/search-concept-custom-types)。 您可以在任何應用程式中查看資料。 如需詳細資訊，請參閱 microsoft [Graph 中的 Microsoft SEARCH API 綜述](https://docs.microsoft.com/graph/search-concept-overview)。

## <a name="limitations"></a>限制

* 當您 **發佈** Microsoft 建立的連接器時，可能需要幾分鐘的時間來建立連線。 在此期間內，連接會顯示其狀態為 [擱置中]。

* 在發佈連接後， [Microsoft 365 系統管理中心](https://admin.microsoft.com) 不支援編輯 **搜尋架構** 。 若要編輯搜尋架構，請刪除連接，然後建立新的連線。

* 接收輸送量會限制每秒大約四個專案。

* 不支援架構更新。 建立連線設定後，就無法更新架構。 您只可刪除並重新建立連線。

* 連接限制。 每個租使用者最多可以建立10個連接。

* 無法使用 [編輯連線支援]。 建立連線後，就無法編輯或變更它。 如果您需要變更任何詳細資料，您必須刪除並重新建立連線。
