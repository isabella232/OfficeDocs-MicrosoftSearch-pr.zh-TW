---
title: 自訂 Microsoft 搜尋] 頁面
ms.author: anfowler
author: adefowler
manager: shohara
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 加入搜尋類別及自訂搜尋結果
ms.openlocfilehash: 87b394847281e43683f2ed9dfd42d19aa103d3e2
ms.sourcegitcommit: bfcab9d42e93addccd1e3875b41bc9cc1b6986cc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2019
ms.locfileid: "37949684"
---
# <a name="customize-the-microsoft-search-page"></a><span data-ttu-id="42b1a-103">自訂 Microsoft 搜尋] 頁面</span><span class="sxs-lookup"><span data-stu-id="42b1a-103">Customize the Microsoft Search page</span></span>

<span data-ttu-id="42b1a-104">建立搜尋類別與結果類型您可以自訂當他們中**SharePoint**、 **Office.com**和**Microsoft Search in Bing**搜尋時，向使用者顯示的搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="42b1a-104">By creating search verticals and result types you can customize the search results that are shown to users when they search in **SharePoint**, **Office.com** and **Microsoft Search in Bing** .</span></span> <span data-ttu-id="42b1a-105">類別，方便使用者尋找他們已取得最新產品權限，請參閱 < 的資訊。</span><span class="sxs-lookup"><span data-stu-id="42b1a-105">Verticals make it easier for users to find the information they’ve got permission to see.</span></span>  <span data-ttu-id="42b1a-106">例如，您可以建立搜尋類別行銷分析資料從協力廠商軟體行銷部門中的使用者。</span><span class="sxs-lookup"><span data-stu-id="42b1a-106">For example, you can create a search vertical for marketing analysis data from third-party software for your users in the marketing department.</span></span> <span data-ttu-id="42b1a-107">您也可以定義結果類型，並自訂的版面配置，這項資料。</span><span class="sxs-lookup"><span data-stu-id="42b1a-107">You can also define result types and customize the layout for this data.</span></span>  

<span data-ttu-id="42b1a-108">您可以建立類別和結果類型，這些層級：</span><span class="sxs-lookup"><span data-stu-id="42b1a-108">You can create verticals and result types  at these levels:</span></span> 

- <span data-ttu-id="42b1a-109">組織層級 – 當您在組織層級新增垂直它會出現在搜尋結果頁面當使用者從其 SharePoint 起始頁面搜尋時，在 Office.com 上及 Bing.com。</span><span class="sxs-lookup"><span data-stu-id="42b1a-109">Organization level – When you add a vertical at the organization level, it appears on the search results page when users search from their SharePoint start page, on Office.com and on Bing.com.</span></span> 
- <span data-ttu-id="42b1a-110">網站層級 – 例如，您可能想要允許您的客戶來直接從其部門的 SharePoint 網站的 「 嚴重性 1"事件的搜尋服務員工。</span><span class="sxs-lookup"><span data-stu-id="42b1a-110">Site level – For example, you might want to allow your customer service employees to search for “Severity 1” incidents directly from their department’s SharePoint site.</span></span> 

## <a name="whats-a-search-vertical"></a><span data-ttu-id="42b1a-111">搜尋類別為何？</span><span class="sxs-lookup"><span data-stu-id="42b1a-111">What’s a search vertical?</span></span>

<span data-ttu-id="42b1a-112">Microsoft 的搜尋結果頁面的頂端有一列的索引標籤，這些是搜尋類別。</span><span class="sxs-lookup"><span data-stu-id="42b1a-112">At the top of the Microsoft search results page there is a row of tabs, these are search verticals.</span></span> <span data-ttu-id="42b1a-113">垂直式搜尋只會顯示結果的特定類型，或是從特定內容，例如唯一的檔案或最新消息。</span><span class="sxs-lookup"><span data-stu-id="42b1a-113">A search vertical only shows results of a certain type or from certain content, for example only files or news.</span></span> <span data-ttu-id="42b1a-114">根據預設 Microsoft Search 顯示類別全部的人員，檔案、 網站及最新消息。</span><span class="sxs-lookup"><span data-stu-id="42b1a-114">By default Microsoft Search shows the verticals All, People, Files, Sites, and News.</span></span>  

<span data-ttu-id="42b1a-115">您可以新增與您的組織相關的搜尋類別。</span><span class="sxs-lookup"><span data-stu-id="42b1a-115">You can add search verticals that are relevant to your organization.</span></span> <span data-ttu-id="42b1a-116">這些會出現在 SharePoint、 Office.com 和 Bing Microsoft 搜尋結果頁面上。</span><span class="sxs-lookup"><span data-stu-id="42b1a-116">These will appear on the Microsoft search results page in SharePoint, Office.com, and Bing.</span></span>  <span data-ttu-id="42b1a-117">例如，您可以建立一個行銷相關內容的垂直與另一個銷售，根據每個群組會想要有的資訊類型。</span><span class="sxs-lookup"><span data-stu-id="42b1a-117">For example, you could create one vertical for  marketing related content and another for sales, based on the type of information that each group would want to have.</span></span> <span data-ttu-id="42b1a-118">您可以新增類別以顯示結果只從透過連接器編製索引的內容。</span><span class="sxs-lookup"><span data-stu-id="42b1a-118">You can add verticals to show results only from content indexed via Connectors.</span></span>  

<span data-ttu-id="42b1a-119">**免責聲明：** 類別和結果類型是目前正在預覽 Microsoft 連接器預覽的一部分。</span><span class="sxs-lookup"><span data-stu-id="42b1a-119">**DISCLAIMER:** Verticals and result types are currently in preview as a part of Microsoft Connectors preview.</span></span> <span data-ttu-id="42b1a-120">您無法建立內容位於 sharepoint 或從檔案共用連接器所編製索引的內容之間的垂直。</span><span class="sxs-lookup"><span data-stu-id="42b1a-120">You cannot create a vertical for content residing in SharePoint or from content indexed by the FileShare connector.</span></span> <span data-ttu-id="42b1a-121">若要深入了解預覽，請參閱[連接器預覽](connectors-preview.md)。</span><span class="sxs-lookup"><span data-stu-id="42b1a-121">To find out more about the preview, see [Connectors Preview](connectors-preview.md).</span></span> <span data-ttu-id="42b1a-122">若要參與預覽，您必須先將提交[Microsoft Graph 連接器預覽註冊表單](https://forms.office.com/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbRxWYgu82J_RFnMMATAS6_chUNVYwNU1CMDNZUDBSSDZKWVo2RDJDRjRLQi4u)。</span><span class="sxs-lookup"><span data-stu-id="42b1a-122">To participate in the preview, you must first submit the [Microsoft Graph Connectors Preview Signup form](https://forms.office.com/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbRxWYgu82J_RFnMMATAS6_chUNVYwNU1CMDNZUDBSSDZKWVo2RDJDRjRLQi4u).</span></span>

## <a name="things-to-consider"></a><span data-ttu-id="42b1a-123">若要考慮的事項...]</span><span class="sxs-lookup"><span data-stu-id="42b1a-123">Things to consider...</span></span>

<span data-ttu-id="42b1a-124">在您開始之前，請確定已編製索引連接器。</span><span class="sxs-lookup"><span data-stu-id="42b1a-124">Before you start, make sure the connector has been indexed.</span></span> <span data-ttu-id="42b1a-125">可能需要多達 48 小時，根據檔案大小。</span><span class="sxs-lookup"><span data-stu-id="42b1a-125">It can take up to 48 hours, depending on the file size.</span></span>

<span data-ttu-id="42b1a-126">您無法建立內容位於 sharepoint 或從檔案共用連接器所編製索引的內容之間的垂直。</span><span class="sxs-lookup"><span data-stu-id="42b1a-126">You can’t create a vertical for content residing in SharePoint or from content indexed by the FileShare connector .</span></span> <span data-ttu-id="42b1a-127">了解如何編製索引內容 （連接器文件的連結）。</span><span class="sxs-lookup"><span data-stu-id="42b1a-127">Learn how to index content(Link to Connector documentation).</span></span>

<span data-ttu-id="42b1a-128">概括來說，有三個主要步驟新增垂直。</span><span class="sxs-lookup"><span data-stu-id="42b1a-128">At a high-level, there are three main steps for adding a vertical.</span></span> 

1. <span data-ttu-id="42b1a-129">建立垂直 – 您會在此步驟中定義的類別名稱、 內容來源及要搜尋的內容的範圍。</span><span class="sxs-lookup"><span data-stu-id="42b1a-129">Create the vertical – In this step you will define the vertical’s name, content source, and scope of the content to search.</span></span> 
2. <span data-ttu-id="42b1a-130">定義此類別的結果看起來像。</span><span class="sxs-lookup"><span data-stu-id="42b1a-130">Define what the results for this vertical will look like.</span></span>  
3. <span data-ttu-id="42b1a-131">啟用 （若要顯示） 從 [類別] 清單] 頁面上的類別。</span><span class="sxs-lookup"><span data-stu-id="42b1a-131">Enable the vertical (to be displayed) from the vertical list page.</span></span>   

## <a name="step-1-create-the-search-vertical"></a><span data-ttu-id="42b1a-132">步驟 1： 建立搜尋類別</span><span class="sxs-lookup"><span data-stu-id="42b1a-132">STEP 1: Create the search vertical</span></span>

<span data-ttu-id="42b1a-133">一旦您啟動精靈，將引導您定義的類別名稱、 內容來源和範圍的內容，它會搜尋的步驟。</span><span class="sxs-lookup"><span data-stu-id="42b1a-133">Once you start the wizard, you'll be guided through the steps to define the vertical's name, content source and scope of the content that it will search.</span></span> <span data-ttu-id="42b1a-134">垂直會建立在停用狀態。</span><span class="sxs-lookup"><span data-stu-id="42b1a-134">The vertical is created in a disabled state.</span></span> <span data-ttu-id="42b1a-135">您將稍後啟用垂直。</span><span class="sxs-lookup"><span data-stu-id="42b1a-135">You will enable the vertical later.</span></span>

<span data-ttu-id="42b1a-136">您可以使用一組有限的[關鍵字查詢語言 (KQL)](https://docs.microsoft.com/sharepoint/dev/general-development/keyword-query-language-kql-syntax-reference)來縮小範圍，以及頁面上顯示列出您可以使用的屬性。</span><span class="sxs-lookup"><span data-stu-id="42b1a-136">You can use a limited set of the [Keyword Query Language (KQL)](https://docs.microsoft.com/sharepoint/dev/general-development/keyword-query-language-kql-syntax-reference) to narrow down the scope, and the page shows lists the properties available to you.</span></span> <span data-ttu-id="42b1a-137">建議您針對建立 KQL 布林運算子與使用免費的文字關鍵字和屬性限制</span><span class="sxs-lookup"><span data-stu-id="42b1a-137">We recommend using free text-keywords and property restrictions with boolean operators for creating the KQL</span></span> 

### <a name="create-a-vertical-at-the-organization-level"></a><span data-ttu-id="42b1a-138">在組織層級建立類別</span><span class="sxs-lookup"><span data-stu-id="42b1a-138">Create a vertical at the organization level</span></span>

<span data-ttu-id="42b1a-139">若要在 SharePoint 中的 Microsoft Search 的垂直建立首頁，Bing 或 Office.com，請遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="42b1a-139">To create the vertical on Microsoft Search in SharePoint home, Bing or Office.com, follow these steps:</span></span>

1. <span data-ttu-id="42b1a-140">在 Microsoft 365 系統管理中心中移至 [ **設定** > **Microsoft Search** > **類別**。</span><span class="sxs-lookup"><span data-stu-id="42b1a-140">In the Microsoft 365 admin center go to **Settings** > **Microsoft Search** > **Verticals**.</span></span>
1. <span data-ttu-id="42b1a-141">選取 [ **新增**若要開始。</span><span class="sxs-lookup"><span data-stu-id="42b1a-141">Select **Add** to get started.</span></span>  

### <a name="create-a-vertical-at-the-site-level"></a><span data-ttu-id="42b1a-142">在網站層級建立類別</span><span class="sxs-lookup"><span data-stu-id="42b1a-142">Create a vertical at the site level</span></span>

1. <span data-ttu-id="42b1a-143">在您要建立垂直 SharePoint 網站] 移至 [**設定**。</span><span class="sxs-lookup"><span data-stu-id="42b1a-143">On the SharePoint site where you want to create the vertical, go to **Settings**.</span></span>
1. <span data-ttu-id="42b1a-144">選取 [**站台資訊**，然後**檢視所有網站設定**]。</span><span class="sxs-lookup"><span data-stu-id="42b1a-144">Select **Site information**, and then **View all site settings**.</span></span>
1. <span data-ttu-id="42b1a-145">尋找 [ **Microsoft 搜尋**] 區段，然後選取 [**此網站集合設定 Microsoft Search**。</span><span class="sxs-lookup"><span data-stu-id="42b1a-145">Look for the **Microsoft Search** section, and then select **Configure Microsoft Search for this site collection**.</span></span>
1. <span data-ttu-id="42b1a-146">在功能窗格中，移至 **自訂體驗**，，然後選取 [**類別**] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="42b1a-146">In the navigation pane, go to **Custom experience**, and then select the **Verticals** tab.</span></span>
1. <span data-ttu-id="42b1a-147">若要新增的類別，選取 [ **新增**。</span><span class="sxs-lookup"><span data-stu-id="42b1a-147">To add a vertical, select **Add**.</span></span> <br>
<span data-ttu-id="42b1a-148">OR</span><span class="sxs-lookup"><span data-stu-id="42b1a-148">OR</span></span> <br><span data-ttu-id="42b1a-149">若要編輯類別，請在清單中選取。</span><span class="sxs-lookup"><span data-stu-id="42b1a-149">To edit a vertical, select it in the list.</span></span>

<span data-ttu-id="42b1a-150">請記住，類別建立在停用狀態。</span><span class="sxs-lookup"><span data-stu-id="42b1a-150">Remember, verticals are created in a disabled state.</span></span> <span data-ttu-id="42b1a-151">您仍然需要啟用這些使用者可以瀏覽類別之前。</span><span class="sxs-lookup"><span data-stu-id="42b1a-151">You'll still need to enable them before users can see the verticals.</span></span>

## <a name="step-2-create-the-result-types"></a><span data-ttu-id="42b1a-152">步驟 2： 建立結果類型</span><span class="sxs-lookup"><span data-stu-id="42b1a-152">STEP 2: Create the result types</span></span>

<span data-ttu-id="42b1a-153">您可以定義結果的顯示方式垂直向內所設計使用結果類型的版面配置。</span><span class="sxs-lookup"><span data-stu-id="42b1a-153">You can define how results are displayed in the vertical by designing the layout using result types.</span></span> <span data-ttu-id="42b1a-154">結果版面配置可讓您直接在搜尋結果中，顯示重要的資訊，讓使用者不需要按一下 [若要查看是否他們已找到他們要尋找的每個搜尋結果]。</span><span class="sxs-lookup"><span data-stu-id="42b1a-154">The result layout let you show important information directly in the search results, so that users don't have to click on each result to see if they've found what they're looking for.</span></span>

<span data-ttu-id="42b1a-p111">搜尋「結果類型」是一種規則，可讓不同類型的搜尋結果以不同方式顯示。其由下列項目組成：</span><span class="sxs-lookup"><span data-stu-id="42b1a-p111">A search result type is a rule that causes distinct kinds of search results to be displayed in different ways. It consists of the following:</span></span>

- <span data-ttu-id="42b1a-157">若要比較，針對每個搜尋結果，例如搜尋結果的內容來源的*一個或多個條件*。</span><span class="sxs-lookup"><span data-stu-id="42b1a-157">*One or more conditions* to compare each search result against, such as the content source of the search result.</span></span>  
- <span data-ttu-id="42b1a-158">使用 [搜尋結果符合條件的*結果版面配置*。</span><span class="sxs-lookup"><span data-stu-id="42b1a-158">A *result layout* to use for search results that meet the conditions.</span></span> <span data-ttu-id="42b1a-159">結果版面配置會控制所有符合條件的結果會出現和搜尋結果頁面上的行為的方式。</span><span class="sxs-lookup"><span data-stu-id="42b1a-159">The result layout controls the way in which all results that meet the conditions appear and behave on a search results page.</span></span>

<span data-ttu-id="42b1a-160">**您必須建立至少一個結果型別上垂直顯示結果。**</span><span class="sxs-lookup"><span data-stu-id="42b1a-160">**You must create at least one result type for results to display on the vertical.**</span></span> <span data-ttu-id="42b1a-161">您可以建立的每個類別的多個結果類型，這可讓您可以使用不同的版面配置的不同類型的結果。</span><span class="sxs-lookup"><span data-stu-id="42b1a-161">You can create multiple result types for each vertical, this allows you to use different layouts for different type of results.</span></span> <span data-ttu-id="42b1a-162">例如，您可以自訂 「 嚴重性 1 」 事件，讓更重要的色彩，而較大的字型相較於 「 嚴重性 3 」 事件。</span><span class="sxs-lookup"><span data-stu-id="42b1a-162">For example, you can customize “Severity 1” incidents to have more prominent colors and a larger font compared to “Severity 3” incidents.</span></span> 

 <span data-ttu-id="42b1a-163">一旦您啟動精靈，將會引導您定義的名稱、 內容來源及條件的結果類型的步驟。</span><span class="sxs-lookup"><span data-stu-id="42b1a-163">Once you start the wizard, you will be guided through the steps to define the name, content source and conditions for the result type.</span></span> <span data-ttu-id="42b1a-164">您可以定義結果類型，從清單檢視的優先順序。</span><span class="sxs-lookup"><span data-stu-id="42b1a-164">You can define the priority of the result type from the list view.</span></span> 
  
### <a name="create-a-result-type-at-the-organization-level"></a><span data-ttu-id="42b1a-165">在組織層級建立結果類型</span><span class="sxs-lookup"><span data-stu-id="42b1a-165">Create a result type at the organization level</span></span>

1. <span data-ttu-id="42b1a-166">在 Microsoft 365 系統管理中心中，前往 [**設定** > **Microsoft Search**，，然後選取 [**輸入的結果**。</span><span class="sxs-lookup"><span data-stu-id="42b1a-166">In the Microsoft 365 admin center, go to **Setting** > **Microsoft Search**, and then select **Result type**.</span></span>
1. <span data-ttu-id="42b1a-167">若要新增**結果類型**，選取 [ **新增**。</span><span class="sxs-lookup"><span data-stu-id="42b1a-167">To add a **Result type**, select **Add**.</span></span> <span data-ttu-id="42b1a-168">若要編輯的結果類型，請在相關的清單中選取結果類型。</span><span class="sxs-lookup"><span data-stu-id="42b1a-168">To edit a result type, select the result type in the relevant list.</span></span>
 
### <a name="create-a-results-type-at-the-site-level"></a><span data-ttu-id="42b1a-169">網站層級建立結果類型</span><span class="sxs-lookup"><span data-stu-id="42b1a-169">Create a results type at the site level</span></span>

1. <span data-ttu-id="42b1a-170">在 SharePoint 網站上您要建立結果類型，請移至**設定**。</span><span class="sxs-lookup"><span data-stu-id="42b1a-170">On the SharePoint site where you want to create the result type, go to **Settings**.</span></span>
1. <span data-ttu-id="42b1a-171">選取 [**站台資訊**，然後**檢視所有網站設定**]。</span><span class="sxs-lookup"><span data-stu-id="42b1a-171">Select **Site information**, and then **View all site settings**.</span></span> 
1. <span data-ttu-id="42b1a-172">尋找 [Microsoft 搜尋] 區段，然後選取 [**此網站集合設定 Microsoft Search**。</span><span class="sxs-lookup"><span data-stu-id="42b1a-172">Look for the Microsoft Search section, and then select **Configure Microsoft Search for this site collection**.</span></span>
1. <span data-ttu-id="42b1a-173">在功能窗格中，移至 **自訂體驗**，，然後選取結果類型] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="42b1a-173">In the navigation pane, go to **Custom experience**, and then select Result type tab.</span></span>
1. <span data-ttu-id="42b1a-174">若要新增結果類型，選取 [ **新增]**。</span><span class="sxs-lookup"><span data-stu-id="42b1a-174">To add a result type, select **Add**.</span></span> <br> <span data-ttu-id="42b1a-175">OR</span><span class="sxs-lookup"><span data-stu-id="42b1a-175">OR</span></span> <br><span data-ttu-id="42b1a-176">若要編輯的結果類型，請在清單中選取結果類型。</span><span class="sxs-lookup"><span data-stu-id="42b1a-176">To edit a result type, select the result type in the list.</span></span>

### <a name="view-the-vertical-after-enabling"></a><span data-ttu-id="42b1a-177">檢視在啟用之後的類別</span><span class="sxs-lookup"><span data-stu-id="42b1a-177">View the vertical after enabling</span></span>

<span data-ttu-id="42b1a-178">啟用垂直之後，它可能需要一段時間，才可以檢視。</span><span class="sxs-lookup"><span data-stu-id="42b1a-178">After you enable the vertical, it might take a while before you can view it.</span></span>
<span data-ttu-id="42b1a-179">如果您想要等候啟用它之後，您可以將附加*cacheClear = true*中立即檢視垂直的 [SharePoint 和 Office.com 的 url。</span><span class="sxs-lookup"><span data-stu-id="42b1a-179">If you want to wait after enabling it, you can append *cacheClear=true* to the URL in SharePoint and Office.com to view the vertical immediately.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="42b1a-180">疑難排解</span><span class="sxs-lookup"><span data-stu-id="42b1a-180">Troubleshooting</span></span>

<span data-ttu-id="42b1a-181">以下是您可能會遇到的常見問題和修正它們的動作清單。</span><span class="sxs-lookup"><span data-stu-id="42b1a-181">Here's a list of common issues you might encounter and actions for fixing them.</span></span>


|<span data-ttu-id="42b1a-182">Error</span><span class="sxs-lookup"><span data-stu-id="42b1a-182">Error</span></span>  |<span data-ttu-id="42b1a-183">動作</span><span class="sxs-lookup"><span data-stu-id="42b1a-183">Action</span></span>  |
|---------|---------|
|<span data-ttu-id="42b1a-184">在垂直上看到 '發生錯誤' 時發生錯誤</span><span class="sxs-lookup"><span data-stu-id="42b1a-184">I see a 'Something went wrong' error on the vertical</span></span>|   <span data-ttu-id="42b1a-185">這兩個類別和結果類型所需完成安裝。</span><span class="sxs-lookup"><span data-stu-id="42b1a-185">Both vertical and result types are needed to complete the setup.</span></span> <span data-ttu-id="42b1a-186">請確定您已建立兩個相同的內容來源。</span><span class="sxs-lookup"><span data-stu-id="42b1a-186">Make sure you have created both for the same content source.</span></span>      |
|<span data-ttu-id="42b1a-187">為什麼我看我結果版面配置雖然已建立一個？</span><span class="sxs-lookup"><span data-stu-id="42b1a-187">Why don't I see my result layout although I have created one?</span></span> | <span data-ttu-id="42b1a-188">花幾分鐘的結果類型]，以用於為這些設定通常會快取。</span><span class="sxs-lookup"><span data-stu-id="42b1a-188">It takes a few minutes for result types to be used as these settings are generally cached.</span></span> <span data-ttu-id="42b1a-189">等候幾分鐘，然後再試一次</span><span class="sxs-lookup"><span data-stu-id="42b1a-189">Wait for a few minutes and try again</span></span>        |
|<span data-ttu-id="42b1a-190">我看不到任何內容來源上垂直或結果類型] 頁面</span><span class="sxs-lookup"><span data-stu-id="42b1a-190">I don't see any content sources on the vertical or result type page</span></span>     |      <span data-ttu-id="42b1a-191">請確定您已設定連接器和編製索引的資料</span><span class="sxs-lookup"><span data-stu-id="42b1a-191">Make sure you have configured connectors and indexed data</span></span>   |



## <a name="next-steps"></a><span data-ttu-id="42b1a-192">後續步驟</span><span class="sxs-lookup"><span data-stu-id="42b1a-192">Next steps</span></span>
[<span data-ttu-id="42b1a-193">步驟 3： 自訂結果版面配置</span><span class="sxs-lookup"><span data-stu-id="42b1a-193">STEP 3: Customize the results layout</span></span>](customize-results-layout.md)
