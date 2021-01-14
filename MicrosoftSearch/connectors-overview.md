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
# <a name="overview-of-microsoft-graph-connectors"></a><span data-ttu-id="f92f1-103">Microsoft Graph 連接器的概述</span><span class="sxs-lookup"><span data-stu-id="f92f1-103">Overview of Microsoft Graph connectors</span></span>

<span data-ttu-id="f92f1-104">[Microsoft 搜尋](https://docs.microsoft.com/microsoftsearch/overview-microsoft-search) 會索引您的所有 [Microsoft 365](https://www.microsoft.com/microsoft-365) 資料，讓其可供使用者搜尋。</span><span class="sxs-lookup"><span data-stu-id="f92f1-104">[Microsoft Search](https://docs.microsoft.com/microsoftsearch/overview-microsoft-search) indexes all your [Microsoft 365](https://www.microsoft.com/microsoft-365) data to make it searchable for users.</span></span> <span data-ttu-id="f92f1-105">透過 Microsoft Graph 連接器，您的組織可以編制協力廠商資料的索引，使其出現在 Microsoft 搜尋結果中。</span><span class="sxs-lookup"><span data-stu-id="f92f1-105">With Microsoft Graph connectors, your organization can index third-party data so it appears in Microsoft Search results.</span></span> <span data-ttu-id="f92f1-106">這可展開 Microsoft 365 生產力應用程式中可搜尋的內容來源類型，以及更廣泛的 Microsoft 生態用。</span><span class="sxs-lookup"><span data-stu-id="f92f1-106">This expands the types of content sources that are searchable in your Microsoft 365 productivity apps and the broader Microsoft ecosystem.</span></span> <span data-ttu-id="f92f1-107">協力廠商資料可以位於內部部署或公用或私人雲端。</span><span class="sxs-lookup"><span data-stu-id="f92f1-107">The third-party data can be hosted on-premises or in the public or private clouds.</span></span>

<!---link Microsoft Graph reference in line 19 when we have access to relevant documentation--->

<span data-ttu-id="f92f1-108">本文的其餘部分是為了協助 Microsoft 365 系統管理員找出可用來回答下列問題的資源：</span><span class="sxs-lookup"><span data-stu-id="f92f1-108">The rest of this article is intended to help Microsoft 365 administrators locate the resources that are available to answer the following questions:</span></span>

* [<span data-ttu-id="f92f1-109">哪些資料來源可連接至 Microsoft 搜尋？</span><span class="sxs-lookup"><span data-stu-id="f92f1-109">What data sources can be connected to Microsoft Search?</span></span>](#what-data-sources-can-be-connected-to-microsoft-search)
* [<span data-ttu-id="f92f1-110">如何管理連線？</span><span class="sxs-lookup"><span data-stu-id="f92f1-110">How do I manage my connections?</span></span>](#how-do-i-manage-my-connections)
* [<span data-ttu-id="f92f1-111">圖形連接器的授權需求和使用期限為何？</span><span class="sxs-lookup"><span data-stu-id="f92f1-111">What are the license requirements and terms of use for Graph connectors?</span></span>](#what-are-the-license-requirements-and-terms-of-use-for-graph-connectors)
* [<span data-ttu-id="f92f1-112">如何自訂及設定搜尋結果？</span><span class="sxs-lookup"><span data-stu-id="f92f1-112">How do I customize and configure search results?</span></span>](#how-do-i-customize-and-configure-search-results)
* [<span data-ttu-id="f92f1-113">如何從自訂應用程式搜尋我的連接器資料？</span><span class="sxs-lookup"><span data-stu-id="f92f1-113">How do I search my connector data from a custom application?</span></span>](#how-do-i-search-my-connector-data-from-a-custom-application)

<!---Modify to another note that is more accurate--->
> [!IMPORTANT]
> <span data-ttu-id="f92f1-114">現在一般會提供 microsoft Graph 連接器和 Microsoft Search APIs。</span><span class="sxs-lookup"><span data-stu-id="f92f1-114">Microsoft Graph connectors and Microsoft Search APIs are now generally available.</span></span> <span data-ttu-id="f92f1-115">第一次部署是針對目標版本所設定的客戶。</span><span class="sxs-lookup"><span data-stu-id="f92f1-115">The first rollouts will be to customers configured for  targeted release.</span></span> <span data-ttu-id="f92f1-116">如果您想要在租使用者中使用圖形連接器，使用者和系統管理員必須選擇已 [目標發行](https://docs.microsoft.com/office365/admin/manage/release-options-in-office-365?view=o365-worldwide&preserve-view=true)。</span><span class="sxs-lookup"><span data-stu-id="f92f1-116">If you want to use a Graph connector in your tenant, users and administrators must opt into [Targeted release](https://docs.microsoft.com/office365/admin/manage/release-options-in-office-365?view=o365-worldwide&preserve-view=true).</span></span>

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

## <a name="what-data-sources-can-be-connected-to-microsoft-search"></a><span data-ttu-id="f92f1-117">哪些資料來源可連接至 Microsoft 搜尋？</span><span class="sxs-lookup"><span data-stu-id="f92f1-117">What data sources can be connected to Microsoft Search?</span></span>

<span data-ttu-id="f92f1-118">Microsoft 提供10個圖形連接器和我們的生態系統合作夥伴已透過100其他圖形連接器建立。</span><span class="sxs-lookup"><span data-stu-id="f92f1-118">Microsoft provides ten Graph connectors and our ecosystem partners have created over 100 additional Graph connectors.</span></span> <span data-ttu-id="f92f1-119">您也可以建立自己的圖形連接器。</span><span class="sxs-lookup"><span data-stu-id="f92f1-119">You can also build your own Graph connector.</span></span> 

### <a name="graph-connectors-by-microsoft"></a><span data-ttu-id="f92f1-120">Microsoft Graph 連接器</span><span class="sxs-lookup"><span data-stu-id="f92f1-120">Graph connectors by Microsoft</span></span>

<span data-ttu-id="f92f1-121">您可以使用 Microsoft 所建立的圖形連接器，連線到下列資料來源：</span><span class="sxs-lookup"><span data-stu-id="f92f1-121">You can connect to the following data sources using Graph connectors created by Microsoft:</span></span>

<!---Need to add a few links below when docs exist--->
* [<span data-ttu-id="f92f1-122">Azure Data Lake Storage Gen2</span><span class="sxs-lookup"><span data-stu-id="f92f1-122">Azure Data Lake Storage Gen2</span></span>](azure-data-lake-connector.md)
* [<span data-ttu-id="f92f1-123">Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="f92f1-123">Azure DevOps</span></span>](azure-devops-connector.md)
* <span data-ttu-id="f92f1-124">Azure SQL</span><span class="sxs-lookup"><span data-stu-id="f92f1-124">Azure SQL</span></span>
* [<span data-ttu-id="f92f1-125">企業網站</span><span class="sxs-lookup"><span data-stu-id="f92f1-125">Enterprise websites</span></span>](enterprise-web-connector.md)
* [<span data-ttu-id="f92f1-126">MediaWiki</span><span class="sxs-lookup"><span data-stu-id="f92f1-126">MediaWiki</span></span>](mediawiki-connector.md)
* [<span data-ttu-id="f92f1-127">Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="f92f1-127">Microsoft SQL Server</span></span>](MSSQL-connector.md)
* [<span data-ttu-id="f92f1-128">檔案共用</span><span class="sxs-lookup"><span data-stu-id="f92f1-128">File share</span></span>](fileshare-connector.md)
* <span data-ttu-id="f92f1-129">Oracle (預覽) </span><span class="sxs-lookup"><span data-stu-id="f92f1-129">Oracle (preview)</span></span>
* [<span data-ttu-id="f92f1-130">Salesforce (預覽)</span><span class="sxs-lookup"><span data-stu-id="f92f1-130">Salesforce (preview)</span></span>](salesforce-connector.md)
* [<span data-ttu-id="f92f1-131">ServiceNow</span><span class="sxs-lookup"><span data-stu-id="f92f1-131">ServiceNow</span></span>](servicenow-connector.md)

<span data-ttu-id="f92f1-132">[圖形連接器圖庫](connectors-gallery.md)包含每個圖形連接器的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="f92f1-132">The [Graph connectors gallery](connectors-gallery.md) contains a brief description of each of these Graph connectors.</span></span> <span data-ttu-id="f92f1-133">如果您已準備好將其中一個資料來源連接至您的租使用者，請務必閱讀適用于資料來源之 Microsoft 安裝連接器中的 [安裝程式概述](configure-connector.md) 和任何其他文章。</span><span class="sxs-lookup"><span data-stu-id="f92f1-133">If you are ready to connect one of these data sources to your tenant, be sure to read the [Setup overview](configure-connector.md) and any other articles in the Setup connectors by Microsoft section that apply to your data source.</span></span>

### <a name="graph-connectors-by-our-partners"></a><span data-ttu-id="f92f1-134">合作夥伴的圖形連接器</span><span class="sxs-lookup"><span data-stu-id="f92f1-134">Graph connectors by our partners</span></span>

<span data-ttu-id="f92f1-135">[Microsoft Graph 連接器圖庫](connectors-gallery.md)包含合作夥伴所建立之每個圖形連接器的簡短說明，以及每個合作夥伴網站的連結。</span><span class="sxs-lookup"><span data-stu-id="f92f1-135">The [Microsoft Graph connectors gallery](connectors-gallery.md) includes a brief descriptions of each of the Graph connectors created by our partners and a link to each partner's website.</span></span> <span data-ttu-id="f92f1-136">請直接聯繫每個合作夥伴以深入瞭解。</span><span class="sxs-lookup"><span data-stu-id="f92f1-136">Contact each partner directly to learn more.</span></span>

### <a name="build-your-own-graph-connector"></a><span data-ttu-id="f92f1-137">建立您自己的圖形連接器</span><span class="sxs-lookup"><span data-stu-id="f92f1-137">Build your own Graph connector</span></span>

<span data-ttu-id="f92f1-138">如果您想要建立自己的圖形連接器，請參閱 microsoft [graph 中的 Microsoft SEARCH API 概述](https://docs.microsoft.com/graph/search-concept-overview) ，以取得詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="f92f1-138">If you plan to build your own Graph connector, see the [Overview of the Microsoft Search API in Microsoft Graph](https://docs.microsoft.com/graph/search-concept-overview) for more information.</span></span>

## <a name="how-do-i-manage-my-connections"></a><span data-ttu-id="f92f1-139">如何管理連線？</span><span class="sxs-lookup"><span data-stu-id="f92f1-139">How do I manage my connections?</span></span>

<span data-ttu-id="f92f1-140">您可以從[Microsoft 365 系統管理中心](https://admin.microsoft.com/)的 [[連接器]](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors)索引標籤管理連線。</span><span class="sxs-lookup"><span data-stu-id="f92f1-140">You can manage your connections from the [Connectors tab](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors) in the [Microsoft 365 admin center](https://admin.microsoft.com/).</span></span> <span data-ttu-id="f92f1-141">如需詳細資訊，請參閱 [Manage a connections](manage-connector.md) 。</span><span class="sxs-lookup"><span data-stu-id="f92f1-141">See [Manage your connections](manage-connector.md) for more information.</span></span>

## <a name="what-are-the-license-requirements-and-terms-of-use-for-graph-connectors"></a><span data-ttu-id="f92f1-142">圖形連接器的授權需求和使用期限為何？</span><span class="sxs-lookup"><span data-stu-id="f92f1-142">What are the license requirements and terms of use for Graph connectors?</span></span>

<span data-ttu-id="f92f1-143">您為組織中的使用者需要有效的 Microsoft 365 或 Office 365 授權和足夠的圖形連接器配額，以在其搜尋結果中查看連接器的資料。</span><span class="sxs-lookup"><span data-stu-id="f92f1-143">You need a valid Microsoft 365 or Office 365 license and sufficient Graph Connectors quota for users in your organization to view data from connectors in their search results.</span></span>

<span data-ttu-id="f92f1-144">若要深入瞭解，請參閱 [授權需求和價格](licensing.md) 與 [使用條款](terms-of-use.md)。</span><span class="sxs-lookup"><span data-stu-id="f92f1-144">To learn more, see [License requirements and pricing](licensing.md) and [Terms of use](terms-of-use.md).</span></span>

## <a name="how-do-i-customize-and-configure-search-results"></a><span data-ttu-id="f92f1-145">如何自訂及設定搜尋結果？</span><span class="sxs-lookup"><span data-stu-id="f92f1-145">How do I customize and configure search results?</span></span>

<span data-ttu-id="f92f1-146">有許多方式可自訂及設定搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="f92f1-146">There are a number of ways to customize and configure search results.</span></span> <span data-ttu-id="f92f1-147">若要深入瞭解，請參閱下列文章：</span><span class="sxs-lookup"><span data-stu-id="f92f1-147">See the following articles to learn more:</span></span>

* [<span data-ttu-id="f92f1-148">管理類別和結果類型</span><span class="sxs-lookup"><span data-stu-id="f92f1-148">Manage verticals and result types</span></span>](customize-search-page.md)
* [<span data-ttu-id="f92f1-149">管理搜尋結果版面配置</span><span class="sxs-lookup"><span data-stu-id="f92f1-149">Manage search result layouts</span></span>](customize-results-layout.md)
* [<span data-ttu-id="f92f1-150">管理結果叢集</span><span class="sxs-lookup"><span data-stu-id="f92f1-150">Manage result cluster</span></span>](result-cluster.md)
* [<span data-ttu-id="f92f1-151">管理自訂篩選</span><span class="sxs-lookup"><span data-stu-id="f92f1-151">Manage custom filters</span></span>](custom-filters.md)

## <a name="how-do-i-search-my-connector-data-from-a-custom-application"></a><span data-ttu-id="f92f1-152">如何從自訂應用程式搜尋我的連接器資料？</span><span class="sxs-lookup"><span data-stu-id="f92f1-152">How do I search my connector data from a custom application?</span></span>

<span data-ttu-id="f92f1-153">在索引自訂資料之後，開發人員可以 [查詢此資料](https://docs.microsoft.com/graph/search-concept-custom-types)。</span><span class="sxs-lookup"><span data-stu-id="f92f1-153">After custom data is indexed, developers can [query this data](https://docs.microsoft.com/graph/search-concept-custom-types).</span></span> <span data-ttu-id="f92f1-154">您可以在任何應用程式中查看資料。</span><span class="sxs-lookup"><span data-stu-id="f92f1-154">You can view your data in any application.</span></span> <span data-ttu-id="f92f1-155">如需詳細資訊，請參閱 microsoft [Graph 中的 Microsoft SEARCH API 綜述](https://docs.microsoft.com/graph/search-concept-overview)。</span><span class="sxs-lookup"><span data-stu-id="f92f1-155">For more information, see the [Overview of the Microsoft Search API in Microsoft Graph](https://docs.microsoft.com/graph/search-concept-overview).</span></span>

## <a name="limitations"></a><span data-ttu-id="f92f1-156">限制</span><span class="sxs-lookup"><span data-stu-id="f92f1-156">Limitations</span></span>

* <span data-ttu-id="f92f1-157">當您 **發佈** Microsoft 建立的連接器時，可能需要幾分鐘的時間來建立連線。</span><span class="sxs-lookup"><span data-stu-id="f92f1-157">When you **publish** a Microsoft-built connector, it might take a few minutes for the connection to be created.</span></span> <span data-ttu-id="f92f1-158">在此期間內，連接會顯示其狀態為 [擱置中]。</span><span class="sxs-lookup"><span data-stu-id="f92f1-158">During that time, the connection will show its status as pending.</span></span>

* <span data-ttu-id="f92f1-159">在發佈連接後， [Microsoft 365 系統管理中心](https://admin.microsoft.com) 不支援編輯 **搜尋架構** 。</span><span class="sxs-lookup"><span data-stu-id="f92f1-159">The [Microsoft 365 admin center](https://admin.microsoft.com) doesn't support editing the **search schema** after a connection is published.</span></span> <span data-ttu-id="f92f1-160">若要編輯搜尋架構，請刪除連接，然後建立新的連線。</span><span class="sxs-lookup"><span data-stu-id="f92f1-160">To edit the search schema, delete your connection and then create a new one.</span></span>

* <span data-ttu-id="f92f1-161">接收輸送量會限制每秒大約四個專案。</span><span class="sxs-lookup"><span data-stu-id="f92f1-161">Ingestion throughput is throttled at about four items per second.</span></span>

* <span data-ttu-id="f92f1-162">不支援架構更新。</span><span class="sxs-lookup"><span data-stu-id="f92f1-162">There is no support for schema updates.</span></span> <span data-ttu-id="f92f1-163">建立連線設定後，就無法更新架構。</span><span class="sxs-lookup"><span data-stu-id="f92f1-163">After you create a connection setup, there's no way to update the schema.</span></span> <span data-ttu-id="f92f1-164">您只可刪除並重新建立連線。</span><span class="sxs-lookup"><span data-stu-id="f92f1-164">You can only delete and re-create the connection.</span></span>

* <span data-ttu-id="f92f1-165">連接限制。</span><span class="sxs-lookup"><span data-stu-id="f92f1-165">There is a connections limit.</span></span> <span data-ttu-id="f92f1-166">每個租使用者最多可以建立10個連接。</span><span class="sxs-lookup"><span data-stu-id="f92f1-166">Each tenant can create up to 10 connections.</span></span>

* <span data-ttu-id="f92f1-167">無法使用 [編輯連線支援]。</span><span class="sxs-lookup"><span data-stu-id="f92f1-167">Edit support for connection is not available.</span></span> <span data-ttu-id="f92f1-168">建立連線後，就無法編輯或變更它。</span><span class="sxs-lookup"><span data-stu-id="f92f1-168">Once the connection has been created, you cannot edit or change it.</span></span> <span data-ttu-id="f92f1-169">如果您需要變更任何詳細資料，您必須刪除並重新建立連線。</span><span class="sxs-lookup"><span data-stu-id="f92f1-169">If you need to change any details, you must delete and recreate the connection.</span></span>
