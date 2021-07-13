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
description: Microsoft 搜尋的 Microsoft Graph 連接器的概覽
ms.openlocfilehash: 87645e32e274eb166d6ba008c4ac720667105a1f
ms.sourcegitcommit: 52129e0129a201ec056903b2461d012fda6d3636
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/12/2021
ms.locfileid: "53383481"
---
<!---Previous ms.author: monaray --->

# <a name="overview-of-microsoft-graph-connectors"></a><span data-ttu-id="6d4ac-103">Microsoft Graph 連接器的概述</span><span class="sxs-lookup"><span data-stu-id="6d4ac-103">Overview of Microsoft Graph connectors</span></span>

<span data-ttu-id="6d4ac-104">[Microsoft 搜尋](./overview-microsoft-search.md)會索引所有的[Microsoft 365](https://www.microsoft.com/microsoft-365)資料，讓使用者可供搜尋。</span><span class="sxs-lookup"><span data-stu-id="6d4ac-104">[Microsoft Search](./overview-microsoft-search.md) indexes all your [Microsoft 365](https://www.microsoft.com/microsoft-365) data to make it searchable for users.</span></span> <span data-ttu-id="6d4ac-105">透過 Microsoft Graph connector，您的組織可以為協力廠商資料編制索引，使其出現在 Microsoft 搜尋結果中。</span><span class="sxs-lookup"><span data-stu-id="6d4ac-105">With Microsoft Graph connectors, your organization can index third-party data so it appears in Microsoft Search results.</span></span> <span data-ttu-id="6d4ac-106">這項功能可展開 Microsoft 365 生產力應用程式中可搜尋的內容來源類型，以及更廣泛的 Microsoft 生態用。</span><span class="sxs-lookup"><span data-stu-id="6d4ac-106">This feature expands the types of content sources that are searchable in your Microsoft 365 productivity apps and the broader Microsoft ecosystem.</span></span> <span data-ttu-id="6d4ac-107">協力廠商資料可以位於內部部署或公用或私人雲端。</span><span class="sxs-lookup"><span data-stu-id="6d4ac-107">The third-party data can be hosted on-premises or in the public or private clouds.</span></span>

<!---link Microsoft Graph reference in line 19 when we have access to relevant documentation--->

<span data-ttu-id="6d4ac-108">本文的目的是協助 Microsoft 365 管理員找到可回答下列問題的資源：</span><span class="sxs-lookup"><span data-stu-id="6d4ac-108">This article is intended to help Microsoft 365 administrators locate the resources that are available to answer the following questions:</span></span>

* [<span data-ttu-id="6d4ac-109">哪些資料來源可以與 Microsoft 搜尋連線？</span><span class="sxs-lookup"><span data-stu-id="6d4ac-109">What data sources can be connected to Microsoft Search?</span></span>](#what-data-sources-can-be-connected-to-microsoft-search)
* [<span data-ttu-id="6d4ac-110">如何管理連線？</span><span class="sxs-lookup"><span data-stu-id="6d4ac-110">How do I manage my connections?</span></span>](#how-do-i-manage-my-connections)
* [<span data-ttu-id="6d4ac-111">Microsoft Graph 連接器的授權需求和使用條款為何？</span><span class="sxs-lookup"><span data-stu-id="6d4ac-111">What are the license requirements and terms of use for Microsoft Graph connectors?</span></span>](#what-are-the-license-requirements-and-terms-of-use-for-connectors)
* [<span data-ttu-id="6d4ac-112">預覽功能為何？</span><span class="sxs-lookup"><span data-stu-id="6d4ac-112">What are the preview features?</span></span>](#what-are-the-preview-features)
* [<span data-ttu-id="6d4ac-113">如何自訂及設定搜尋結果？</span><span class="sxs-lookup"><span data-stu-id="6d4ac-113">How do I customize and configure search results?</span></span>](#how-do-i-customize-and-configure-search-results)
* [<span data-ttu-id="6d4ac-114">如何從自訂應用程式搜尋我的連接器資料？</span><span class="sxs-lookup"><span data-stu-id="6d4ac-114">How do I search my connector data from a custom application?</span></span>](#how-do-i-search-my-connector-data-from-a-custom-application)
* [<span data-ttu-id="6d4ac-115">如何自訂搜尋結果？</span><span class="sxs-lookup"><span data-stu-id="6d4ac-115">How do I customize search results?</span></span>](#how-do-i-customize-search-results)
* [<span data-ttu-id="6d4ac-116">連接器限制是什麼</span><span class="sxs-lookup"><span data-stu-id="6d4ac-116">What are the connector limitations</span></span>](#what-are-the-connector-limitations)

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

## <a name="what-data-sources-can-be-connected-to-microsoft-search"></a><span data-ttu-id="6d4ac-117">哪些資料來源可以與 Microsoft 搜尋連線？</span><span class="sxs-lookup"><span data-stu-id="6d4ac-117">What data sources can be connected to Microsoft Search?</span></span>

<span data-ttu-id="6d4ac-118">Microsoft 提供9個連接器和我們的生態系統合作夥伴已透過100以上的連接器建立。</span><span class="sxs-lookup"><span data-stu-id="6d4ac-118">Microsoft provides 9 connectors and our ecosystem partners have created over 100 more connectors.</span></span> <span data-ttu-id="6d4ac-119">您也可以建立您自己的連接器。</span><span class="sxs-lookup"><span data-stu-id="6d4ac-119">You can also build your own connector.</span></span>

### <a name="microsoft-graph-connectors-by-microsoft"></a><span data-ttu-id="6d4ac-120">microsoft Graph 連接器</span><span class="sxs-lookup"><span data-stu-id="6d4ac-120">Microsoft Graph connectors by Microsoft</span></span>

<span data-ttu-id="6d4ac-121">您可以使用 Microsoft 所建立的連接器連線到下列資料來源：</span><span class="sxs-lookup"><span data-stu-id="6d4ac-121">You can connect to the following data sources using connectors created by Microsoft:</span></span>

<!---Add links below when new docs are created--->
* [<span data-ttu-id="6d4ac-122">Azure Data Lake Storage Gen2</span><span class="sxs-lookup"><span data-stu-id="6d4ac-122">Azure Data Lake Storage Gen2</span></span>](azure-data-lake-connector.md)
* [<span data-ttu-id="6d4ac-123">Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="6d4ac-123">Azure DevOps</span></span>](azure-devops-connector.md)
* [<span data-ttu-id="6d4ac-124">Azure SQL 和 Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="6d4ac-124">Azure SQL and Microsoft SQL Server</span></span>](MSSQL-connector.md)
* [<span data-ttu-id="6d4ac-125">企業網站</span><span class="sxs-lookup"><span data-stu-id="6d4ac-125">Enterprise websites</span></span>](enterprise-web-connector.md)
* [<span data-ttu-id="6d4ac-126">MediaWiki</span><span class="sxs-lookup"><span data-stu-id="6d4ac-126">MediaWiki</span></span>](mediawiki-connector.md)
* [<span data-ttu-id="6d4ac-127">檔案共用</span><span class="sxs-lookup"><span data-stu-id="6d4ac-127">File share</span></span>](fileshare-connector.md)
* [<span data-ttu-id="6d4ac-128">Oracle SQL</span><span class="sxs-lookup"><span data-stu-id="6d4ac-128">Oracle SQL</span></span>](OracleSQL-connector.md)
* [<span data-ttu-id="6d4ac-129">Salesforce (預覽)</span><span class="sxs-lookup"><span data-stu-id="6d4ac-129">Salesforce (preview)</span></span>](salesforce-connector.md)
* [<span data-ttu-id="6d4ac-130">ServiceNow</span><span class="sxs-lookup"><span data-stu-id="6d4ac-130">ServiceNow</span></span>](servicenow-connector.md)

<span data-ttu-id="6d4ac-131">[Microsoft Graph 連接器圖庫](https://www.microsoft.com/microsoft-search/connectors)包含每個連接器的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="6d4ac-131">The [Microsoft Graph connectors gallery](https://www.microsoft.com/microsoft-search/connectors) contains a brief description of each of these connectors.</span></span> <span data-ttu-id="6d4ac-132">如果您已準備好將其中一個資料來源連線至您的租使用者，請務必閱讀套用至資料來源之 Microsoft 安裝連接器中的 [安裝程式概述](configure-connector.md) 及其他任何文章。</span><span class="sxs-lookup"><span data-stu-id="6d4ac-132">If you're ready to connect one of these data sources to your tenant, be sure to read the [Setup overview](configure-connector.md) and any other articles in the Setup connectors by Microsoft section that apply to your data source.</span></span>

### <a name="microsoft-graph-connectors-by-our-partners"></a><span data-ttu-id="6d4ac-133">由我們的合作夥伴提供的 Microsoft Graph 連接器</span><span class="sxs-lookup"><span data-stu-id="6d4ac-133">Microsoft Graph connectors by our partners</span></span>

<span data-ttu-id="6d4ac-134">[Microsoft Graph connector 圖庫](https://www.microsoft.com/microsoft-search/connectors)包含合作夥伴所建立之每個連接器的簡短說明，以及每個夥伴網站的連結。</span><span class="sxs-lookup"><span data-stu-id="6d4ac-134">The [Microsoft Graph connectors gallery](https://www.microsoft.com/microsoft-search/connectors) includes a brief description of each of the connectors created by our partners, and a link to each partner's website.</span></span> <span data-ttu-id="6d4ac-135">若要深入瞭解，請直接與每個合作夥伴聯繫。</span><span class="sxs-lookup"><span data-stu-id="6d4ac-135">To learn more, contact each partner directly.</span></span>

### <a name="build-your-own-microsoft-graph-connector"></a><span data-ttu-id="6d4ac-136">建立您自己的 Microsoft Graph 連接器</span><span class="sxs-lookup"><span data-stu-id="6d4ac-136">Build your own Microsoft Graph connector</span></span>

<span data-ttu-id="6d4ac-137">您可以根據意願建立您自己的連接器。</span><span class="sxs-lookup"><span data-stu-id="6d4ac-137">You can build your own connector if you prefer.</span></span> <span data-ttu-id="6d4ac-138">如需建立連接器的詳細資訊，請參閱[建立第一個自訂的 Microsoft Graph 連接器](/graph/connecting-external-content-build-quickstart)。</span><span class="sxs-lookup"><span data-stu-id="6d4ac-138">For more information on building connectors, see  [Build your first custom Microsoft Graph connector](/graph/connecting-external-content-build-quickstart).</span></span>

## <a name="how-do-i-manage-my-connections"></a><span data-ttu-id="6d4ac-139">如何管理連線？</span><span class="sxs-lookup"><span data-stu-id="6d4ac-139">How do I manage my connections?</span></span>

<span data-ttu-id="6d4ac-140">您可以從[Microsoft 365 系統管理中心](https://admin.microsoft.com/)中的 [[連接器]](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors)索引標籤管理連線。</span><span class="sxs-lookup"><span data-stu-id="6d4ac-140">You can manage your connections from the [Connectors tab](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors) in the [Microsoft 365 admin center](https://admin.microsoft.com/).</span></span> <span data-ttu-id="6d4ac-141">如需管理連線的詳細資訊，請參閱： [Manage a connections](manage-connector.md)。</span><span class="sxs-lookup"><span data-stu-id="6d4ac-141">For more information about managing connections, see: [Manage your connections](manage-connector.md).</span></span>

## <a name="what-are-the-license-requirements-and-terms-of-use-for-connectors"></a><span data-ttu-id="6d4ac-142">連接器的授權需求和使用條款為何？</span><span class="sxs-lookup"><span data-stu-id="6d4ac-142">What are the license requirements and terms of use for connectors?</span></span>

<span data-ttu-id="6d4ac-143">您的組織中的使用者必須有有效的 Microsoft 365 或 Office 365 授權和足夠的連接器配額，才可在其搜尋結果中查看連接器的資料。</span><span class="sxs-lookup"><span data-stu-id="6d4ac-143">You need a valid Microsoft 365 or Office 365 license and sufficient connectors quota for users in your organization to view data from connectors in their search results.</span></span>

<span data-ttu-id="6d4ac-144">若要深入瞭解，請參閱 [授權需求和價格](licensing.md) 與 [使用條款](terms-of-use.md)。</span><span class="sxs-lookup"><span data-stu-id="6d4ac-144">To learn more, see [License requirements and pricing](licensing.md) and [Terms of use](terms-of-use.md).</span></span>

## <a name="what-are-the-preview-features"></a><span data-ttu-id="6d4ac-145">預覽功能為何？</span><span class="sxs-lookup"><span data-stu-id="6d4ac-145">What are the preview features?</span></span>

<span data-ttu-id="6d4ac-146">雖然 Microsoft Graph 連接器和 Microsoft 搜尋 APIs 現在一般可用，但預覽中有許多功能。</span><span class="sxs-lookup"><span data-stu-id="6d4ac-146">Although Microsoft Graph connectors and Microsoft Search APIs are now generally available, there are several features that are in preview.</span></span>

<span data-ttu-id="6d4ac-147">預覽中的連接器和功能組包括：</span><span class="sxs-lookup"><span data-stu-id="6d4ac-147">The set of connectors and features in preview include:</span></span>

* [<span data-ttu-id="6d4ac-148">Azure DevOps 連接器</span><span class="sxs-lookup"><span data-stu-id="6d4ac-148">Azure DevOps connector</span></span>](azure-devops-connector.md)
* [<span data-ttu-id="6d4ac-149">Salesforce 連接器</span><span class="sxs-lookup"><span data-stu-id="6d4ac-149">Salesforce connector</span></span>](salesforce-connector.md)
* <span data-ttu-id="6d4ac-150">具有使用來源 ACLs 之搜尋許可權的[ServiceNow 連接器](servicenow-connector.md)</span><span class="sxs-lookup"><span data-stu-id="6d4ac-150">[ServiceNow connector](servicenow-connector.md) with search permissions that use source ACLs</span></span>
* [<span data-ttu-id="6d4ac-151">管理結果叢集</span><span class="sxs-lookup"><span data-stu-id="6d4ac-151">Manage result cluster</span></span>](result-cluster.md)
* [<span data-ttu-id="6d4ac-152">垂直中的多個連接</span><span class="sxs-lookup"><span data-stu-id="6d4ac-152">Multiple connections in a vertical</span></span>](customize-search-page.md#multiple-connections-in-a-vertical)

## <a name="how-do-i-customize-and-configure-search-results"></a><span data-ttu-id="6d4ac-153">如何自訂及設定搜尋結果？</span><span class="sxs-lookup"><span data-stu-id="6d4ac-153">How do I customize and configure search results?</span></span>

<span data-ttu-id="6d4ac-154">有許多方式可自訂及設定搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="6d4ac-154">There are many ways to customize and configure search results.</span></span> <span data-ttu-id="6d4ac-155">若要深入瞭解，請參閱下列文章：</span><span class="sxs-lookup"><span data-stu-id="6d4ac-155">See the following articles to learn more:</span></span>

* [<span data-ttu-id="6d4ac-156">管理類別和結果類型</span><span class="sxs-lookup"><span data-stu-id="6d4ac-156">Manage verticals and result types</span></span>](customize-search-page.md)
* [<span data-ttu-id="6d4ac-157">管理搜尋結果版面配置</span><span class="sxs-lookup"><span data-stu-id="6d4ac-157">Manage search result layouts</span></span>](customize-results-layout.md)
* [<span data-ttu-id="6d4ac-158">管理結果叢集</span><span class="sxs-lookup"><span data-stu-id="6d4ac-158">Manage result cluster</span></span>](result-cluster.md)
* [<span data-ttu-id="6d4ac-159">管理自訂篩選</span><span class="sxs-lookup"><span data-stu-id="6d4ac-159">Manage custom filters</span></span>](custom-filters.md)

## <a name="how-do-i-search-my-connector-data-from-a-custom-application"></a><span data-ttu-id="6d4ac-160">如何從自訂應用程式搜尋我的連接器資料？</span><span class="sxs-lookup"><span data-stu-id="6d4ac-160">How do I search my connector data from a custom application?</span></span>

<span data-ttu-id="6d4ac-161">在索引自訂資料之後，開發人員可以 [查詢此資料](/graph/search-concept-custom-types)。</span><span class="sxs-lookup"><span data-stu-id="6d4ac-161">After custom data is indexed, developers can [query this data](/graph/search-concept-custom-types).</span></span> <span data-ttu-id="6d4ac-162">您可以在任何應用程式中查看資料。</span><span class="sxs-lookup"><span data-stu-id="6d4ac-162">You can view your data in any application.</span></span> <span data-ttu-id="6d4ac-163">如需詳細資訊，請參閱[Microsoft Graph 中的 Microsoft 搜尋 API 綜述](/graph/search-concept-overview)。</span><span class="sxs-lookup"><span data-stu-id="6d4ac-163">For more information, see the [Overview of the Microsoft Search API in Microsoft Graph](/graph/search-concept-overview).</span></span>

## <a name="how-do-i-customize-search-results"></a><span data-ttu-id="6d4ac-164">如何自訂搜尋結果？</span><span class="sxs-lookup"><span data-stu-id="6d4ac-164">How do I customize search results?</span></span>

<span data-ttu-id="6d4ac-165">下一步是自訂搜尋結果（如本文中所建議的） [如何自訂及設定搜尋結果？](#how-do-i-customize-and-configure-search-results)。</span><span class="sxs-lookup"><span data-stu-id="6d4ac-165">The next step is to customize the search results as recommended in this article [How do I customize and configure search results?](#how-do-i-customize-and-configure-search-results).</span></span> <span data-ttu-id="6d4ac-166">若要深入瞭解自訂搜尋結果，請參閱 [自訂搜尋結果頁面](customize-search-page.md)。</span><span class="sxs-lookup"><span data-stu-id="6d4ac-166">To learn more about customizing search results, see [Customize the search results page](customize-search-page.md).</span></span>

## <a name="what-are-the-connector-limitations"></a><span data-ttu-id="6d4ac-167">連接器限制為何？</span><span class="sxs-lookup"><span data-stu-id="6d4ac-167">What are the connector limitations?</span></span>

* <span data-ttu-id="6d4ac-168">當您 **發佈** Microsoft 建立的連接器時，可能需要幾分鐘的時間才能建立連線。</span><span class="sxs-lookup"><span data-stu-id="6d4ac-168">When you **publish** a Microsoft-built connector, it can take a few minutes for the connection to be created.</span></span> <span data-ttu-id="6d4ac-169">在此期間內，連接會顯示其狀態為 [擱置中]。</span><span class="sxs-lookup"><span data-stu-id="6d4ac-169">During that time, the connection will show its status as pending.</span></span>

* <span data-ttu-id="6d4ac-170">每秒大約四個專案會限制攝取輸送量。</span><span class="sxs-lookup"><span data-stu-id="6d4ac-170">Ingestion throughput is throttled at approximately four items per second.</span></span>

* <span data-ttu-id="6d4ac-171">不支援架構更新。</span><span class="sxs-lookup"><span data-stu-id="6d4ac-171">There is no support for schema updates.</span></span> <span data-ttu-id="6d4ac-172">建立連線設定後，就無法更新架構。</span><span class="sxs-lookup"><span data-stu-id="6d4ac-172">After you create a connection setup, there's no way to update the schema.</span></span> <span data-ttu-id="6d4ac-173">您只可刪除並重新建立連線。</span><span class="sxs-lookup"><span data-stu-id="6d4ac-173">You can only delete and re-create the connection.</span></span>

* <span data-ttu-id="6d4ac-174">連接限制。</span><span class="sxs-lookup"><span data-stu-id="6d4ac-174">There is a connection limit.</span></span> <span data-ttu-id="6d4ac-175">每個租使用者最多可以建立10個連接。</span><span class="sxs-lookup"><span data-stu-id="6d4ac-175">Each tenant can create up to 10 connections.</span></span>

* <span data-ttu-id="6d4ac-176">建立的連線之後，就無法進行編輯或變更。</span><span class="sxs-lookup"><span data-stu-id="6d4ac-176">You cannot edit or change a connection after it has been created.</span></span> <span data-ttu-id="6d4ac-177">如果您需要變更任何詳細資料，您必須刪除並重新建立連線。</span><span class="sxs-lookup"><span data-stu-id="6d4ac-177">If you need to change any details, you must delete and recreate the connection.</span></span>
