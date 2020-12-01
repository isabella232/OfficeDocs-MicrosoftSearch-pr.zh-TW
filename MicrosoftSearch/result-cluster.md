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
ms.openlocfilehash: fa6ac2dc720ed43e40454b952526734accd45ea4
ms.sourcegitcommit: a328b9764abf5cd0c1c0a8c7def0c6e334da9a1d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/30/2020
ms.locfileid: "49477111"
---
# <a name="graph-connectors-result-cluster"></a><span data-ttu-id="ce3f9-103">圖形連接器產生的聚簇</span><span class="sxs-lookup"><span data-stu-id="ce3f9-103">Graph connectors result cluster</span></span>

## <a name="overview-of-the-graph-connectors-result-cluster-preview"></a><span data-ttu-id="ce3f9-104">圖形連接器結果叢集 (預覽的概述) </span><span class="sxs-lookup"><span data-stu-id="ce3f9-104">Overview of the Graph connectors result cluster (Preview)</span></span>  

<span data-ttu-id="ce3f9-105">透過圖形連接器的結果聚簇，企業可以在其預設視圖中搜尋協力廠商資料來源的內容，SharePoint 和 Office.com 中的 [全部] 索引標籤)  (。</span><span class="sxs-lookup"><span data-stu-id="ce3f9-105">With Graph connectors result clusters, enterprises can search for content from third party data sources in their default view (the All tab) in SharePoint and Office.com.</span></span>

<span data-ttu-id="ce3f9-106">結果聚簇可協助使用者探索所有協力廠商內容 (previoulsy 系結至單一連接器和垂直) 一個位置。</span><span class="sxs-lookup"><span data-stu-id="ce3f9-106">Result clusters help users discover all third party content (previoulsy tied to a single connector and vertical) in one place.</span></span> <span data-ttu-id="ce3f9-107">結果叢集中顯示的結果會根據租使用者管理員在搜尋類別中的設定方式，將其組合在一起。</span><span class="sxs-lookup"><span data-stu-id="ce3f9-107">The results shown in a result cluster are grouped together based on how the tenant administrator configures them in a search vertical.</span></span>  

## <a name="how-connector-results-are-selected-and-displayed"></a><span data-ttu-id="ce3f9-108">選取及顯示連接器結果的方式</span><span class="sxs-lookup"><span data-stu-id="ce3f9-108">How connector results are selected and displayed</span></span>

<span data-ttu-id="ce3f9-109">結果叢集中所提供的連接器結果是衍生自個別的搜尋行業及連接器內容。</span><span class="sxs-lookup"><span data-stu-id="ce3f9-109">Connector results provided in the result cluster are derived from individual search verticals with connector content.</span></span> <span data-ttu-id="ce3f9-110">每個搜尋類別都會提供一組相關的結果，這些結果會變成候選結果叢集。</span><span class="sxs-lookup"><span data-stu-id="ce3f9-110">Each search vertical provides a set of relevant results which becomes a candidate result cluster.</span></span> <span data-ttu-id="ce3f9-111">根據每個專案的「title」屬性、結果程式碼片段和內容元件來選擇相關的結果。</span><span class="sxs-lookup"><span data-stu-id="ce3f9-111">Relevant results are chosen based on the "title" property, result snippet, and content component of each item.</span></span>

<span data-ttu-id="ce3f9-112">為了確保從搜尋縱向探索內容，我們建議您為專案提供有意義的標題。</span><span class="sxs-lookup"><span data-stu-id="ce3f9-112">To ensure discovery of content from the search verticals, we recommend providing meaningful titles for your items.</span></span> <span data-ttu-id="ce3f9-113">這會影響結果叢集候選項的仲裁，以及您在結果叢集中顯示內容的可能性。</span><span class="sxs-lookup"><span data-stu-id="ce3f9-113">This positively impacts the arbitration of result cluster candidates and the likelihood of your content showing up in a result cluster.</span></span> <span data-ttu-id="ce3f9-114">例如，除非您的使用者使用 IDs 尋找內容，否則請避免使用 IDs 做為屬性 "title" 的值。</span><span class="sxs-lookup"><span data-stu-id="ce3f9-114">For example, avoid the use of IDs as values for the property "title" unless your users are using IDs to look for content.</span></span>

<span data-ttu-id="ce3f9-115">結果叢集顯示的頻率會因因素而異，例如您設定的搜尋縱向的數目和內容類型。</span><span class="sxs-lookup"><span data-stu-id="ce3f9-115">How often a result cluster is shown varies on factors such as the number of search verticals that you configure and the type of content.</span></span> <span data-ttu-id="ce3f9-116">透過選取或忽略結果叢集結果，您將會隱含地提供提示，以調整結果叢集在一段時間內的觸發。</span><span class="sxs-lookup"><span data-stu-id="ce3f9-116">By either selecting or ignoring result cluster results, you will implicitly provide hints that will adjust the triggering of result clusters over time.</span></span>

<span data-ttu-id="ce3f9-117">結果叢集中所顯示之連接器專案的搜尋結果經驗是由系統產生，不會使用自訂的結果版面配置。</span><span class="sxs-lookup"><span data-stu-id="ce3f9-117">The search result experience for connector items shown in your result cluster is system generated and does not use custom result layouts.</span></span> <span data-ttu-id="ce3f9-118">如果您想要在結果叢集中顯示結果，您必須在連線註冊期間宣告 "title" 屬性和專案內容。</span><span class="sxs-lookup"><span data-stu-id="ce3f9-118">You must declare the "title" property and item content during connection registration if you want results to appear in your result cluster.</span></span>

## <a name="enable-result-clusters"></a><span data-ttu-id="ce3f9-119">啟用結果聚簇</span><span class="sxs-lookup"><span data-stu-id="ce3f9-119">Enable result clusters</span></span>
  
<span data-ttu-id="ce3f9-120">預設會關閉結果叢集體驗功能。</span><span class="sxs-lookup"><span data-stu-id="ce3f9-120">The result cluster experience is turned off by default.</span></span>  

<span data-ttu-id="ce3f9-121">請遵循下列步驟，在組織層級開啟體驗：</span><span class="sxs-lookup"><span data-stu-id="ce3f9-121">Follow these steps to turn on the experience at the organization level:</span></span>

1. <span data-ttu-id="ce3f9-122">在 [Microsoft 365 系統管理中心](https://admin.microsoft.com/)中，移至 [**設定**]  >  **搜尋 & 情報**  >  **自訂**  >  **縱向**。</span><span class="sxs-lookup"><span data-stu-id="ce3f9-122">In the [Microsoft 365 admin center](https://admin.microsoft.com/), go to **Settings** > **Search & intelligence** > **Customization** > **Verticals**.</span></span>  
2. <span data-ttu-id="ce3f9-123">選取 [ **所有** 垂直]，然後啟用 [ **顯示連接器結果**]。</span><span class="sxs-lookup"><span data-stu-id="ce3f9-123">Select  the **All** vertical, then enable **Show connector results**.</span></span> 


<span data-ttu-id="ce3f9-124">請遵循下列步驟，在網站層級開啟體驗：</span><span class="sxs-lookup"><span data-stu-id="ce3f9-124">Follow these steps to turn on the experience at the site level:</span></span>

1. <span data-ttu-id="ce3f9-125">在您想要進行結果叢集體驗的 SharePoint 網站上，移至 [ **設定**]。</span><span class="sxs-lookup"><span data-stu-id="ce3f9-125">On the SharePoint site where you want the result cluster experience, go to **Settings**.</span></span>
2. <span data-ttu-id="ce3f9-126">移至 **網站資訊** > **查看所有網站設定**。</span><span class="sxs-lookup"><span data-stu-id="ce3f9-126">Go to **Site information**>**View all site settings**.</span></span>
3. <span data-ttu-id="ce3f9-127">移至 [Microsoft 搜尋] 區段，然後選取 [ **設定此網站集合的 Microsoft search**]。</span><span class="sxs-lookup"><span data-stu-id="ce3f9-127">Go to the Microsoft Search section, then select **Configure Microsoft Search for this site collection**.</span></span>
4. <span data-ttu-id="ce3f9-128">在功能窗格中，移至 [ **自訂經驗**]，然後選取 [ **縱向**]。</span><span class="sxs-lookup"><span data-stu-id="ce3f9-128">In the navigation pane, go to **Custom experience**, then select **Verticals**.</span></span>
5. <span data-ttu-id="ce3f9-129">選取 [ **所有** 垂直]，然後啟用 [ **顯示連接器結果**]。</span><span class="sxs-lookup"><span data-stu-id="ce3f9-129">Select the **All** vertical, then enable **Show connector results**.</span></span>

## <a name="view-the-result-cluster-experience-after-it-is-enabled"></a><span data-ttu-id="ce3f9-130">在啟用結果叢集體驗後查看</span><span class="sxs-lookup"><span data-stu-id="ce3f9-130">View the result cluster experience after it is enabled</span></span>

<span data-ttu-id="ce3f9-131">在您開啟結果叢集體驗後，可能需要幾分鐘的時間才能進行查看。</span><span class="sxs-lookup"><span data-stu-id="ce3f9-131">After you turn on the result cluster experience, it might take a few minutes before you can view it.</span></span> <span data-ttu-id="ce3f9-132">如果您想要立即體驗，您可以在 SharePoint 和 Office 的 URL 中附加 *cacheClear = true* 。</span><span class="sxs-lookup"><span data-stu-id="ce3f9-132">If you want the experience immediately, you can append *cacheClear=true* to the URL in SharePoint and Office.</span></span>
