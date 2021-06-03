---
title: Microsoft Graph 連接器概述
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
description: microsoft 搜尋的 microsoft Graph 連接器概述
ms.openlocfilehash: 6c47d4a619122cd1efc12599eb648d840b5b86c9
ms.sourcegitcommit: 1b154441f3a3abba0f2719e66a767432bc9506ca
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/02/2021
ms.locfileid: "52720961"
---
<!---Previous ms.author: monaray --->

# <a name="overview-of-microsoft-graph-connectors"></a><span data-ttu-id="e1f05-103">Microsoft Graph 連接器的概述</span><span class="sxs-lookup"><span data-stu-id="e1f05-103">Overview of Microsoft Graph connectors</span></span>

<span data-ttu-id="e1f05-104">[Microsoft 搜尋](./overview-microsoft-search.md)會索引所有的[Microsoft 365](https://www.microsoft.com/microsoft-365)資料，使其可供使用者搜尋。</span><span class="sxs-lookup"><span data-stu-id="e1f05-104">[Microsoft Search](./overview-microsoft-search.md) indexes all your [Microsoft 365](https://www.microsoft.com/microsoft-365) data to make it searchable for users.</span></span> <span data-ttu-id="e1f05-105">透過 microsoft Graph connector，您的組織可以編制協力廠商資料的索引，使其顯示在 microsoft 搜尋結果中。</span><span class="sxs-lookup"><span data-stu-id="e1f05-105">With Microsoft Graph connectors, your organization can index third-party data so it appears in Microsoft Search results.</span></span> <span data-ttu-id="e1f05-106">這項功能可展開 Microsoft 365 生產力應用程式中可搜尋的內容來源類型，以及更廣泛的 Microsoft 生態用。</span><span class="sxs-lookup"><span data-stu-id="e1f05-106">This feature expands the types of content sources that are searchable in your Microsoft 365 productivity apps and the broader Microsoft ecosystem.</span></span> <span data-ttu-id="e1f05-107">協力廠商資料可以位於內部部署或公用或私人雲端。</span><span class="sxs-lookup"><span data-stu-id="e1f05-107">The third-party data can be hosted on-premises or in the public or private clouds.</span></span>

<!---link Microsoft Graph reference in line 19 when we have access to relevant documentation--->

<span data-ttu-id="e1f05-108">本文的目的是協助 Microsoft 365 管理員找到可回答下列問題的資源：</span><span class="sxs-lookup"><span data-stu-id="e1f05-108">This article is intended to help Microsoft 365 administrators locate the resources that are available to answer the following questions:</span></span>

* [<span data-ttu-id="e1f05-109">哪些資料來源可連接至 Microsoft 搜尋？</span><span class="sxs-lookup"><span data-stu-id="e1f05-109">What data sources can be connected to Microsoft Search?</span></span>](#what-data-sources-can-be-connected-to-microsoft-search)
* [<span data-ttu-id="e1f05-110">如何管理連線？</span><span class="sxs-lookup"><span data-stu-id="e1f05-110">How do I manage my connections?</span></span>](#how-do-i-manage-my-connections)
* [<span data-ttu-id="e1f05-111">Graph 連接器的授權需求和使用條款為何？</span><span class="sxs-lookup"><span data-stu-id="e1f05-111">What are the license requirements and terms of use for Graph connectors?</span></span>](#what-are-the-license-requirements-and-terms-of-use-for-graph-connectors)
* [<span data-ttu-id="e1f05-112">預覽功能為何？</span><span class="sxs-lookup"><span data-stu-id="e1f05-112">What are the preview features?</span></span>](#what-are-the-preview-features)
* [<span data-ttu-id="e1f05-113">如何自訂及設定搜尋結果？</span><span class="sxs-lookup"><span data-stu-id="e1f05-113">How do I customize and configure search results?</span></span>](#how-do-i-customize-and-configure-search-results)
* [<span data-ttu-id="e1f05-114">如何從自訂應用程式搜尋我的連接器資料？</span><span class="sxs-lookup"><span data-stu-id="e1f05-114">How do I search my connector data from a custom application?</span></span>](#how-do-i-search-my-connector-data-from-a-custom-application)
* [<span data-ttu-id="e1f05-115">如何自訂搜尋結果？</span><span class="sxs-lookup"><span data-stu-id="e1f05-115">How do I customize search results?</span></span>](#how-do-i-customize-search-results)
* [<span data-ttu-id="e1f05-116">連接器限制是什麼</span><span class="sxs-lookup"><span data-stu-id="e1f05-116">What are the connector limitations</span></span>](#what-are-the-connector-limitations)

<!---Modify to another note that is more accurate after rollout completion--->
> [!IMPORTANT]
> <span data-ttu-id="e1f05-117">現在，microsoft Graph 連接器和 microsoft Search APIs 一般皆可供使用。</span><span class="sxs-lookup"><span data-stu-id="e1f05-117">Microsoft Graph connectors and Microsoft Search APIs are now generally available.</span></span> <span data-ttu-id="e1f05-118">第一次部署是針對目標版本所設定的客戶。</span><span class="sxs-lookup"><span data-stu-id="e1f05-118">The first rollouts will be to customers configured for  targeted release.</span></span> <span data-ttu-id="e1f05-119">如果您想要在租使用者中使用 Graph 連接器，使用者和系統管理員必須選擇已[目標發行](/microsoft-365/admin/manage/release-options-in-office-365?preserve-view=true&view=o365-worldwide)。</span><span class="sxs-lookup"><span data-stu-id="e1f05-119">If you want to use a Graph connector in your tenant, users and administrators must opt into [Targeted release](/microsoft-365/admin/manage/release-options-in-office-365?preserve-view=true&view=o365-worldwide).</span></span>

<!---Add Value, scenario, example, and/or graphic in December updates--->
<!---Probably remove architecture section below
## Architecture

The following architectural diagram of the Microsoft Graph platform shows how Graph connector content flows through content indexing to user results in [Microsoft Search](./overview-microsoft-search.md) clients. The rest of this section explains each of the key building blocks in the diagram.

![Diagram: on-premises and cloud-based data is pulled by connectors and indexed by the Microsoft Search API, and then the Microsoft Search service delivers the results to users.](media/connectors-overview/highlevel-connectors.png)
Graph connectors can pull data from cloud-based (SaaS) data sources and on-premises data stores. The above diagram shows connections to only two data sources, but you can add connections to up ten sources per tenant.

The Microsoft Graph Connectors API instantiates one connection per data source. Then, the API indexes and stores the data. Established connections interact with Microsoft Search, so users can get search results.

You can use the Microsoft 365 [admin center](https://admin.microsoft.com) to setup and manage any of the Graph connectors by Microsoft. The admin center has a simple user interface that makes it easy to establish the connection to your data source, and monitor connection status and utilization.

***Edit paragraph below***
To create a **connection** to a data source, admins need authenticated access to the data and the entire content repository. The data is fed to the graph connector service for indexing.--->

## <a name="what-data-sources-can-be-connected-to-microsoft-search"></a><span data-ttu-id="e1f05-120">哪些資料來源可連接至 Microsoft 搜尋？</span><span class="sxs-lookup"><span data-stu-id="e1f05-120">What data sources can be connected to Microsoft Search?</span></span>

<span data-ttu-id="e1f05-121">Microsoft 提供9部 Graph 連接器和我們的生態系統合作夥伴，已建立超過100以上 Graph 連接器。</span><span class="sxs-lookup"><span data-stu-id="e1f05-121">Microsoft provides 9 Graph connectors and our ecosystem partners have created over 100 more Graph connectors.</span></span> <span data-ttu-id="e1f05-122">您也可以建立自己的 Graph 連接器。</span><span class="sxs-lookup"><span data-stu-id="e1f05-122">You can also build your own Graph connector.</span></span>

### <a name="graph-connectors-by-microsoft"></a><span data-ttu-id="e1f05-123">Microsoft Graph 連接器</span><span class="sxs-lookup"><span data-stu-id="e1f05-123">Graph connectors by Microsoft</span></span>

<span data-ttu-id="e1f05-124">您可以使用 Microsoft 所建立的 Graph 連接器，來連接至下列資料來源：</span><span class="sxs-lookup"><span data-stu-id="e1f05-124">You can connect to the following data sources using Graph connectors created by Microsoft:</span></span>

<!---Add links below when new docs are created--->
* [<span data-ttu-id="e1f05-125">Azure Data Lake Storage Gen2</span><span class="sxs-lookup"><span data-stu-id="e1f05-125">Azure Data Lake Storage Gen2</span></span>](azure-data-lake-connector.md)
* [<span data-ttu-id="e1f05-126">Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="e1f05-126">Azure DevOps</span></span>](azure-devops-connector.md)
* [<span data-ttu-id="e1f05-127">Azure SQL 和 Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="e1f05-127">Azure SQL and Microsoft SQL Server</span></span>](MSSQL-connector.md)
* [<span data-ttu-id="e1f05-128">企業網站</span><span class="sxs-lookup"><span data-stu-id="e1f05-128">Enterprise websites</span></span>](enterprise-web-connector.md)
* [<span data-ttu-id="e1f05-129">MediaWiki</span><span class="sxs-lookup"><span data-stu-id="e1f05-129">MediaWiki</span></span>](mediawiki-connector.md)
* [<span data-ttu-id="e1f05-130">檔案共用</span><span class="sxs-lookup"><span data-stu-id="e1f05-130">File share</span></span>](fileshare-connector.md)
* [<span data-ttu-id="e1f05-131">Oracle SQL</span><span class="sxs-lookup"><span data-stu-id="e1f05-131">Oracle SQL</span></span>](OracleSQL-connector.md)
* [<span data-ttu-id="e1f05-132">Salesforce (預覽)</span><span class="sxs-lookup"><span data-stu-id="e1f05-132">Salesforce (preview)</span></span>](salesforce-connector.md)
* [<span data-ttu-id="e1f05-133">ServiceNow</span><span class="sxs-lookup"><span data-stu-id="e1f05-133">ServiceNow</span></span>](servicenow-connector.md)

<span data-ttu-id="e1f05-134">[Graph 連接器圖庫](connectors-gallery.md)包含每個 Graph 連接器的簡短說明。</span><span class="sxs-lookup"><span data-stu-id="e1f05-134">The [Graph connectors gallery](connectors-gallery.md) contains a brief description of each of these Graph connectors.</span></span> <span data-ttu-id="e1f05-135">如果您已準備好將其中一個資料來源連線至您的租使用者，請務必閱讀套用至資料來源之 Microsoft 安裝連接器中的 [安裝程式概述](configure-connector.md) 及其他任何文章。</span><span class="sxs-lookup"><span data-stu-id="e1f05-135">If you're ready to connect one of these data sources to your tenant, be sure to read the [Setup overview](configure-connector.md) and any other articles in the Setup connectors by Microsoft section that apply to your data source.</span></span>

### <a name="graph-connectors-by-our-partners"></a><span data-ttu-id="e1f05-136">合作夥伴 Graph 連接器</span><span class="sxs-lookup"><span data-stu-id="e1f05-136">Graph connectors by our partners</span></span>

<span data-ttu-id="e1f05-137">[Microsoft Graph connector 圖庫](connectors-gallery.md)包含合作夥伴所建立之每個 Graph 連接器的簡短說明，以及每個夥伴網站的連結。</span><span class="sxs-lookup"><span data-stu-id="e1f05-137">The [Microsoft Graph connectors gallery](connectors-gallery.md) includes a brief description of each of the Graph connectors created by our partners, and a link to each partner's website.</span></span> <span data-ttu-id="e1f05-138">若要深入瞭解，請直接與每個合作夥伴聯繫。</span><span class="sxs-lookup"><span data-stu-id="e1f05-138">To learn more, contact each partner directly.</span></span>

### <a name="build-your-own-graph-connector"></a><span data-ttu-id="e1f05-139">建立您自己的 Graph 連接器</span><span class="sxs-lookup"><span data-stu-id="e1f05-139">Build your own Graph connector</span></span>

<span data-ttu-id="e1f05-140">您可以根據意願建立您自己的 Graph 連接器。</span><span class="sxs-lookup"><span data-stu-id="e1f05-140">You can build your own Graph connector if you prefer.</span></span> <span data-ttu-id="e1f05-141">如需建立 Graph 連接器的詳細資訊，請參閱 microsoft [Search API in microsoft Graph 中的概述](/graph/search-concept-overview)。</span><span class="sxs-lookup"><span data-stu-id="e1f05-141">For more information on building Graph connectors, see the [Overview of the Microsoft Search API in Microsoft Graph](/graph/search-concept-overview).</span></span>

## <a name="how-do-i-manage-my-connections"></a><span data-ttu-id="e1f05-142">如何管理連線？</span><span class="sxs-lookup"><span data-stu-id="e1f05-142">How do I manage my connections?</span></span>

<span data-ttu-id="e1f05-143">您可以從[Microsoft 365 系統管理中心](https://admin.microsoft.com/)的 [[連接器]](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors)索引標籤管理連線。</span><span class="sxs-lookup"><span data-stu-id="e1f05-143">You can manage your connections from the [Connectors tab](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors) in the [Microsoft 365 admin center](https://admin.microsoft.com/).</span></span> <span data-ttu-id="e1f05-144">如需管理連線的詳細資訊，請參閱： [Manage a connections](manage-connector.md)。</span><span class="sxs-lookup"><span data-stu-id="e1f05-144">For more information about managing connections, see: [Manage your connections](manage-connector.md).</span></span>

## <a name="what-are-the-license-requirements-and-terms-of-use-for-graph-connectors"></a><span data-ttu-id="e1f05-145">Graph 連接器的授權需求和使用條款為何？</span><span class="sxs-lookup"><span data-stu-id="e1f05-145">What are the license requirements and terms of use for Graph connectors?</span></span>

<span data-ttu-id="e1f05-146">您的組織中的使用者必須具備有效的 Microsoft 365 或 Office 365 授權和足夠的 Graph 連接器配額，才可在其搜尋結果中查看連接器的資料。</span><span class="sxs-lookup"><span data-stu-id="e1f05-146">You need a valid Microsoft 365 or Office 365 license and sufficient Graph Connectors quota for users in your organization to view data from connectors in their search results.</span></span>

<span data-ttu-id="e1f05-147">若要深入瞭解，請參閱 [授權需求和價格](licensing.md) 與 [使用條款](terms-of-use.md)。</span><span class="sxs-lookup"><span data-stu-id="e1f05-147">To learn more, see [License requirements and pricing](licensing.md) and [Terms of use](terms-of-use.md).</span></span>

## <a name="what-are-the-preview-features"></a><span data-ttu-id="e1f05-148">預覽功能為何？</span><span class="sxs-lookup"><span data-stu-id="e1f05-148">What are the preview features?</span></span>

<span data-ttu-id="e1f05-149">雖然 microsoft Graph 連接器和 microsoft 搜尋 APIs 現在一般可用，但預覽中有許多功能。</span><span class="sxs-lookup"><span data-stu-id="e1f05-149">Although Microsoft Graph connectors and Microsoft Search APIs are now generally available, there are several features that are in preview.</span></span>

<span data-ttu-id="e1f05-150">預覽中的連接器和功能組包括：</span><span class="sxs-lookup"><span data-stu-id="e1f05-150">The set of connectors and features in preview include:</span></span>

* [<span data-ttu-id="e1f05-151">Azure DevOps 連接器</span><span class="sxs-lookup"><span data-stu-id="e1f05-151">Azure DevOps connector</span></span>](azure-devops-connector.md)
* [<span data-ttu-id="e1f05-152">Salesforce 連接器</span><span class="sxs-lookup"><span data-stu-id="e1f05-152">Salesforce connector</span></span>](salesforce-connector.md)
* <span data-ttu-id="e1f05-153">具有使用來源 ACLs 之搜尋許可權的[ServiceNow 連接器](servicenow-connector.md)</span><span class="sxs-lookup"><span data-stu-id="e1f05-153">[ServiceNow connector](servicenow-connector.md) with search permissions that use source ACLs</span></span>
* [<span data-ttu-id="e1f05-154">管理結果叢集</span><span class="sxs-lookup"><span data-stu-id="e1f05-154">Manage result cluster</span></span>](result-cluster.md)
* [<span data-ttu-id="e1f05-155">垂直中的多個連接</span><span class="sxs-lookup"><span data-stu-id="e1f05-155">Multiple connections in a vertical</span></span>](customize-search-page.md#multiple-connections-in-a-vertical)

## <a name="how-do-i-customize-and-configure-search-results"></a><span data-ttu-id="e1f05-156">如何自訂及設定搜尋結果？</span><span class="sxs-lookup"><span data-stu-id="e1f05-156">How do I customize and configure search results?</span></span>

<span data-ttu-id="e1f05-157">有許多方式可自訂及設定搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="e1f05-157">There are many ways to customize and configure search results.</span></span> <span data-ttu-id="e1f05-158">若要深入瞭解，請參閱下列文章：</span><span class="sxs-lookup"><span data-stu-id="e1f05-158">See the following articles to learn more:</span></span>

* [<span data-ttu-id="e1f05-159">管理類別和結果類型</span><span class="sxs-lookup"><span data-stu-id="e1f05-159">Manage verticals and result types</span></span>](customize-search-page.md)
* [<span data-ttu-id="e1f05-160">管理搜尋結果版面配置</span><span class="sxs-lookup"><span data-stu-id="e1f05-160">Manage search result layouts</span></span>](customize-results-layout.md)
* [<span data-ttu-id="e1f05-161">管理結果叢集</span><span class="sxs-lookup"><span data-stu-id="e1f05-161">Manage result cluster</span></span>](result-cluster.md)
* [<span data-ttu-id="e1f05-162">管理自訂篩選</span><span class="sxs-lookup"><span data-stu-id="e1f05-162">Manage custom filters</span></span>](custom-filters.md)

## <a name="how-do-i-search-my-connector-data-from-a-custom-application"></a><span data-ttu-id="e1f05-163">如何從自訂應用程式搜尋我的連接器資料？</span><span class="sxs-lookup"><span data-stu-id="e1f05-163">How do I search my connector data from a custom application?</span></span>

<span data-ttu-id="e1f05-164">在索引自訂資料之後，開發人員可以 [查詢此資料](/graph/search-concept-custom-types)。</span><span class="sxs-lookup"><span data-stu-id="e1f05-164">After custom data is indexed, developers can [query this data](/graph/search-concept-custom-types).</span></span> <span data-ttu-id="e1f05-165">您可以在任何應用程式中查看資料。</span><span class="sxs-lookup"><span data-stu-id="e1f05-165">You can view your data in any application.</span></span> <span data-ttu-id="e1f05-166">如需詳細資訊，請參閱 microsoft [SEARCH API In microsoft Graph 中的概述](/graph/search-concept-overview)。</span><span class="sxs-lookup"><span data-stu-id="e1f05-166">For more information, see the [Overview of the Microsoft Search API in Microsoft Graph](/graph/search-concept-overview).</span></span>

## <a name="how-do-i-customize-search-results"></a><span data-ttu-id="e1f05-167">如何自訂搜尋結果？</span><span class="sxs-lookup"><span data-stu-id="e1f05-167">How do I customize search results?</span></span>

<span data-ttu-id="e1f05-168">下一步是自訂搜尋結果（如本文中所建議的） [如何自訂及設定搜尋結果？](#how-do-i-customize-and-configure-search-results)。</span><span class="sxs-lookup"><span data-stu-id="e1f05-168">The next step is to customize the search results as recommended in this article [How do I customize and configure search results?](#how-do-i-customize-and-configure-search-results).</span></span> <span data-ttu-id="e1f05-169">若要深入瞭解自訂搜尋結果，請參閱 [自訂搜尋結果頁面](customize-search-page.md)。</span><span class="sxs-lookup"><span data-stu-id="e1f05-169">To learn more about customizing search results, see [Customize the search results page](customize-search-page.md).</span></span>

## <a name="what-are-the-connector-limitations"></a><span data-ttu-id="e1f05-170">連接器限制為何？</span><span class="sxs-lookup"><span data-stu-id="e1f05-170">What are the connector limitations?</span></span>

* <span data-ttu-id="e1f05-171">當您 **發佈** Microsoft 建立的連接器時，可能需要幾分鐘的時間才能建立連線。</span><span class="sxs-lookup"><span data-stu-id="e1f05-171">When you **publish** a Microsoft-built connector, it can take a few minutes for the connection to be created.</span></span> <span data-ttu-id="e1f05-172">在此期間內，連接會顯示其狀態為 [擱置中]。</span><span class="sxs-lookup"><span data-stu-id="e1f05-172">During that time, the connection will show its status as pending.</span></span>

* <span data-ttu-id="e1f05-173">每秒大約四個專案會限制攝取輸送量。</span><span class="sxs-lookup"><span data-stu-id="e1f05-173">Ingestion throughput is throttled at approximately four items per second.</span></span>

* <span data-ttu-id="e1f05-174">不支援架構更新。</span><span class="sxs-lookup"><span data-stu-id="e1f05-174">There is no support for schema updates.</span></span> <span data-ttu-id="e1f05-175">建立連線設定後，就無法更新架構。</span><span class="sxs-lookup"><span data-stu-id="e1f05-175">After you create a connection setup, there's no way to update the schema.</span></span> <span data-ttu-id="e1f05-176">您只可刪除並重新建立連線。</span><span class="sxs-lookup"><span data-stu-id="e1f05-176">You can only delete and re-create the connection.</span></span>

* <span data-ttu-id="e1f05-177">連接限制。</span><span class="sxs-lookup"><span data-stu-id="e1f05-177">There is a connection limit.</span></span> <span data-ttu-id="e1f05-178">每個租使用者最多可以建立10個連接。</span><span class="sxs-lookup"><span data-stu-id="e1f05-178">Each tenant can create up to 10 connections.</span></span>

* <span data-ttu-id="e1f05-179">建立的連線之後，就無法進行編輯或變更。</span><span class="sxs-lookup"><span data-stu-id="e1f05-179">You cannot edit or change a connection after it has been created.</span></span> <span data-ttu-id="e1f05-180">如果您需要變更任何詳細資料，您必須刪除並重新建立連線。</span><span class="sxs-lookup"><span data-stu-id="e1f05-180">If you need to change any details, you must delete and recreate the connection.</span></span>
