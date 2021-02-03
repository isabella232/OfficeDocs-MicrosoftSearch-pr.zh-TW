---
title: 連接器結果叢集
ms.author: manusi
author: manusi
manager: ruppala
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 連接器結果聚簇體驗的詳細資料
ms.openlocfilehash: fb29fb9c14811698fb7c5d043853b57231c76a0b
ms.sourcegitcommit: d1bc6c41ecf47584373ce57543502bed55753d0c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/02/2021
ms.locfileid: "50080835"
---
# <a name="graph-connectors-result-cluster"></a><span data-ttu-id="c7f5d-103">圖形連接器產生的聚簇</span><span class="sxs-lookup"><span data-stu-id="c7f5d-103">Graph connectors result cluster</span></span>

## <a name="overview-of-the-graph-connectors-result-cluster-preview"></a><span data-ttu-id="c7f5d-104">圖形連接器結果叢集 (預覽的概述) </span><span class="sxs-lookup"><span data-stu-id="c7f5d-104">Overview of the Graph connectors result cluster (Preview)</span></span>  

<span data-ttu-id="c7f5d-105">透過圖形連接器的結果聚簇，企業可以在其預設視圖、[ **全部** ] 索引標籤、SharePoint、Office.com 及 Microsoft Search in Bing 中搜尋協力廠商資料來源的內容。</span><span class="sxs-lookup"><span data-stu-id="c7f5d-105">With Graph connectors result clusters, enterprises can search for content from third party data sources in their default view, the **All** tab, in SharePoint, Office.com, and Microsoft Search in Bing.</span></span>

<span data-ttu-id="c7f5d-106">結果聚簇可協助使用者在一個位置探索所有協力廠商內容。</span><span class="sxs-lookup"><span data-stu-id="c7f5d-106">Result clusters help users discover all third party content in one place.</span></span> <span data-ttu-id="c7f5d-107">結果叢集中顯示的結果會根據搜尋類別設定分組在一起。</span><span class="sxs-lookup"><span data-stu-id="c7f5d-107">The results shown in a result cluster are grouped together based on the search vertical configuration.</span></span>

## <a name="how-connector-results-are-selected-and-displayed"></a><span data-ttu-id="c7f5d-108">選取及顯示連接器結果的方式</span><span class="sxs-lookup"><span data-stu-id="c7f5d-108">How connector results are selected and displayed</span></span>

<span data-ttu-id="c7f5d-109">結果叢集中所提供的連接器結果是衍生自個別的搜尋行業及連接器內容。</span><span class="sxs-lookup"><span data-stu-id="c7f5d-109">Connector results provided in the result cluster are derived from individual search verticals with connector content.</span></span> <span data-ttu-id="c7f5d-110">每個搜尋類別都會提供一組相關的結果，這些結果會變成候選結果叢集。</span><span class="sxs-lookup"><span data-stu-id="c7f5d-110">Each search vertical provides a set of relevant results which becomes a candidate result cluster.</span></span> <span data-ttu-id="c7f5d-111">根據每個專案的「title」屬性和「content」屬性，選取相關的結果。</span><span class="sxs-lookup"><span data-stu-id="c7f5d-111">Relevant results are chosen based on the "title" property and "content" property of each item.</span></span> <span data-ttu-id="c7f5d-112">Content 屬性標示為 *isContent = true* 在架構上。</span><span class="sxs-lookup"><span data-stu-id="c7f5d-112">The content property is marked as *isContent=true* on the schema.</span></span>

<span data-ttu-id="c7f5d-113">為了確保從搜尋縱向探索內容，我們建議您為專案提供有意義的標題。</span><span class="sxs-lookup"><span data-stu-id="c7f5d-113">To ensure discovery of content from the search verticals, we recommend providing meaningful titles for your items.</span></span> <span data-ttu-id="c7f5d-114">這會影響結果叢集候選項的仲裁，以及您在結果叢集中顯示內容的可能性。</span><span class="sxs-lookup"><span data-stu-id="c7f5d-114">This positively impacts the arbitration of result cluster candidates and the likelihood of your content showing up in a result cluster.</span></span> <span data-ttu-id="c7f5d-115">例如，除非您的使用者使用 IDs 尋找內容，否則請避免使用 IDs 做為屬性 "title" 的值。</span><span class="sxs-lookup"><span data-stu-id="c7f5d-115">For example, avoid the use of IDs as values for the property "title" unless your users are using IDs to look for content.</span></span>

<span data-ttu-id="c7f5d-116">結果叢集顯示的頻率會因因素而異，例如您設定的搜尋縱向的數目和內容類型。</span><span class="sxs-lookup"><span data-stu-id="c7f5d-116">How often a result cluster is shown varies on factors such as the number of search verticals that you configure and the type of content.</span></span> <span data-ttu-id="c7f5d-117">透過互動或忽略結果叢集，使用者將會以隱含方式提供提示，以調整它隨時間的觸發。</span><span class="sxs-lookup"><span data-stu-id="c7f5d-117">By either interacting or ignoring a result cluster, users will implicitly provide hints that will adjust its triggering over time.</span></span>

<span data-ttu-id="c7f5d-118">結果叢集中所顯示之連接器專案的搜尋結果體驗使用您所定義的 [結果類型](https://docs.microsoft.com/microsoftsearch/customize-search-page#create-your-own-result-type) 。</span><span class="sxs-lookup"><span data-stu-id="c7f5d-118">The search result experience for connector items shown in your result cluster uses [result types](https://docs.microsoft.com/microsoftsearch/customize-search-page#create-your-own-result-type) defined by you.</span></span> <span data-ttu-id="c7f5d-119">如果未設定任何結果類型，則會使用 [系統產生的版面](https://docs.microsoft.com/microsoftsearch/customize-search-page#default-search-result-layout) 配置。</span><span class="sxs-lookup"><span data-stu-id="c7f5d-119">If no result type is configured, a [system generated layout](https://docs.microsoft.com/microsoftsearch/customize-search-page#default-search-result-layout) is used.</span></span> 

<span data-ttu-id="c7f5d-120">建議使用 "title" 屬性做為搜尋結果標題，並使用 "content" 屬性做為搜尋描述。</span><span class="sxs-lookup"><span data-stu-id="c7f5d-120">We recommend using the “title” property as the search result title and the "content" property as the search description.</span></span> <span data-ttu-id="c7f5d-121">這可透過準確觸發結果叢集和最相關的結果，為您的使用者提供最佳的體驗。</span><span class="sxs-lookup"><span data-stu-id="c7f5d-121">This will provide the best experience for your users through accurate triggering of the result cluster and most relevant results in the cluster.</span></span> 

## <a name="enable-result-clusters"></a><span data-ttu-id="c7f5d-122">啟用結果聚簇</span><span class="sxs-lookup"><span data-stu-id="c7f5d-122">Enable result clusters</span></span>
  
<span data-ttu-id="c7f5d-123">預設會關閉結果叢集體驗功能。</span><span class="sxs-lookup"><span data-stu-id="c7f5d-123">The result cluster experience is turned off by default.</span></span>  

<span data-ttu-id="c7f5d-124">請遵循下列步驟，在組織層級開啟體驗：</span><span class="sxs-lookup"><span data-stu-id="c7f5d-124">Follow these steps to turn on the experience at the organization level:</span></span>

1. <span data-ttu-id="c7f5d-125">在 [Microsoft 365 系統管理中心](https://admin.microsoft.com)中，移至 [ [**縱向**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/verticals)]。</span><span class="sxs-lookup"><span data-stu-id="c7f5d-125">In the [Microsoft 365 admin center](https://admin.microsoft.com), go to [**Verticals**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/verticals).</span></span>
2. <span data-ttu-id="c7f5d-126">選取 [ **所有** 垂直]，然後啟用 [ **顯示連接器結果**]。</span><span class="sxs-lookup"><span data-stu-id="c7f5d-126">Select  the **All** vertical, then enable **Show connector results**.</span></span> 


<span data-ttu-id="c7f5d-127">請遵循下列步驟，在 SharePoint 網站層級開啟體驗：</span><span class="sxs-lookup"><span data-stu-id="c7f5d-127">Follow these steps to turn on the experience at the SharePoint site level:</span></span>

1. <span data-ttu-id="c7f5d-128">在您想要進行結果叢集體驗的 SharePoint 網站上，移至 [ **設定**]。</span><span class="sxs-lookup"><span data-stu-id="c7f5d-128">On the SharePoint site where you want the result cluster experience, go to **Settings**.</span></span>
2. <span data-ttu-id="c7f5d-129">移至 **網站資訊** > **查看所有網站設定**。</span><span class="sxs-lookup"><span data-stu-id="c7f5d-129">Go to **Site information**>**View all site settings**.</span></span>
3. <span data-ttu-id="c7f5d-130">移至 [Microsoft 搜尋] 區段，然後選取 [ **設定此網站集合的 Microsoft search**]。</span><span class="sxs-lookup"><span data-stu-id="c7f5d-130">Go to the Microsoft Search section, then select **Configure Microsoft Search for this site collection**.</span></span>
4. <span data-ttu-id="c7f5d-131">在功能窗格中，移至 [ **自訂經驗**]，然後選取 [ **縱向**]。</span><span class="sxs-lookup"><span data-stu-id="c7f5d-131">In the navigation pane, go to **Custom experience**, then select **Verticals**.</span></span>
5. <span data-ttu-id="c7f5d-132">選取 [ **所有** 垂直]，然後啟用 [ **顯示連接器結果**]。</span><span class="sxs-lookup"><span data-stu-id="c7f5d-132">Select the **All** vertical, then enable **Show connector results**.</span></span>

## <a name="view-the-result-cluster-experience-after-it-is-enabled"></a><span data-ttu-id="c7f5d-133">在啟用結果叢集體驗後查看</span><span class="sxs-lookup"><span data-stu-id="c7f5d-133">View the result cluster experience after it is enabled</span></span>

<span data-ttu-id="c7f5d-134">在您開啟結果叢集體驗後，可能需要長達12小時才能進行查看。</span><span class="sxs-lookup"><span data-stu-id="c7f5d-134">After you turn on the result cluster experience, it can take up to 12 hours before you can view it.</span></span> <span data-ttu-id="c7f5d-135">如果您想要立即體驗，您可以在 SharePoint 和 Office 的 URL 中附加 *cacheClear = true* 。</span><span class="sxs-lookup"><span data-stu-id="c7f5d-135">If you want the experience immediately, you can append *cacheClear=true* to the URL in SharePoint and Office.</span></span>
