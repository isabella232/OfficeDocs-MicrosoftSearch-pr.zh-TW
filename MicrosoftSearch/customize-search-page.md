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
ms.openlocfilehash: 28e8fdc7fe7f08abe265c53772a161b8a7095503
ms.sourcegitcommit: 68087149c769a7cdde80944dd9c9933d2bf4a23f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/18/2019
ms.locfileid: "38699555"
---
# <a name="customize-the-microsoft-search-page"></a><span data-ttu-id="53aa7-103">自訂 Microsoft 搜尋] 頁面</span><span class="sxs-lookup"><span data-stu-id="53aa7-103">Customize the Microsoft Search page</span></span>

<span data-ttu-id="53aa7-104">藉由建立搜尋類別和結果類型，您可以自訂當他們中[SharePoint](http://sharepoint.com/)、 [Microsoft Office](https://Office.com)和 Microsoft Search in [Bing](https://Bing.com)搜尋時，向使用者顯示的搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="53aa7-104">By creating search verticals and result types, you can customize the search results that are shown to users when they search in [SharePoint](http://sharepoint.com/), [Microsoft Office](https://Office.com), and Microsoft Search in [Bing](https://Bing.com).</span></span> <span data-ttu-id="53aa7-105">類別，方便使用者尋找他們已取得最新產品權限，請參閱 < 的資訊。</span><span class="sxs-lookup"><span data-stu-id="53aa7-105">Verticals make it easier for users to find the information they’ve got permission to see.</span></span> <span data-ttu-id="53aa7-106">例如，您可以建立搜尋類別行銷分析資料從協力廠商軟體行銷部門中的使用者。</span><span class="sxs-lookup"><span data-stu-id="53aa7-106">For example, you can create a search vertical for marketing analysis data from third-party software for your users in the marketing department.</span></span> <span data-ttu-id="53aa7-107">您也可以定義結果類型，並自訂的版面配置，這項資料。</span><span class="sxs-lookup"><span data-stu-id="53aa7-107">You can also define result types and customize the layout for this data.</span></span>  

<span data-ttu-id="53aa7-108">您可以建立類別和結果類型，這些層級：</span><span class="sxs-lookup"><span data-stu-id="53aa7-108">You can create verticals and result types at these levels:</span></span> 

- <span data-ttu-id="53aa7-109">**組織層級**– 當您在組織層級新增垂直時，它會出現當使用者從其[SharePoint](http://sharepoint.com/)起始頁面搜尋時的搜尋結果頁面上、 [Office](https://Office.com)，以及在[Bing](https://Bing.com)上。</span><span class="sxs-lookup"><span data-stu-id="53aa7-109">**Organization level** – When you add a vertical at the organization level, it appears on the search results page when users search from their [SharePoint](http://sharepoint.com/) start page, on [Office](https://Office.com), and on [Bing](https://Bing.com).</span></span> 
- <span data-ttu-id="53aa7-110">**網站層級**– 例如，您可能要讓您的客戶服務員工搜尋直接從其部門的 SharePoint 網站的**嚴重性 1**事件。</span><span class="sxs-lookup"><span data-stu-id="53aa7-110">**Site level** – For example, you might want to allow your customer service employees to search for **Severity 1** incidents directly from their department’s SharePoint site.</span></span> 

## <a name="whats-a-search-vertical"></a><span data-ttu-id="53aa7-111">搜尋類別為何？</span><span class="sxs-lookup"><span data-stu-id="53aa7-111">What’s a search vertical?</span></span>

<span data-ttu-id="53aa7-112">頂端的 [Microsoft 搜尋結果] 頁面上會是列會搜尋類別的索引標籤。</span><span class="sxs-lookup"><span data-stu-id="53aa7-112">At the top of the Microsoft Search results page is a row of tabs that are the search verticals.</span></span> <span data-ttu-id="53aa7-113">垂直式搜尋只會顯示特定類型的或是從特定內容的結果。</span><span class="sxs-lookup"><span data-stu-id="53aa7-113">A search vertical only shows results of a certain type or from certain content.</span></span> <span data-ttu-id="53aa7-114">例如，只有 [檔案] 或 [新聞。</span><span class="sxs-lookup"><span data-stu-id="53aa7-114">An example is only files or news.</span></span> <span data-ttu-id="53aa7-115">根據預設，Microsoft Search 會顯示**所有**、**人員**、**檔案**、**網站**及**新聞**類別。</span><span class="sxs-lookup"><span data-stu-id="53aa7-115">By default, Microsoft Search shows the verticals **All**, **People**, **Files**, **Sites**, and **News**.</span></span>  

<span data-ttu-id="53aa7-116">您可以新增與您的組織相關的搜尋類別。</span><span class="sxs-lookup"><span data-stu-id="53aa7-116">You can add search verticals that are relevant to your organization.</span></span> <span data-ttu-id="53aa7-117">這些會出現在[SharePoint](http://sharepoint.com/)、[辦公室](https://Office.com)和[Bing](https://Bing.com)Microsoft 搜尋結果頁面上。</span><span class="sxs-lookup"><span data-stu-id="53aa7-117">These will appear on the Microsoft Search results page in [SharePoint](http://sharepoint.com/), [Office](https://Office.com), and [Bing](https://Bing.com).</span></span> <span data-ttu-id="53aa7-118">例如，您可以建立一個行銷相關內容的垂直與另一個銷售，類型為基礎的每個群組會想要有的資訊。</span><span class="sxs-lookup"><span data-stu-id="53aa7-118">For example, you could create one vertical for marketing-related content and another for sales, based on the type of information that each group would want to have.</span></span> <span data-ttu-id="53aa7-119">您可以新增類別以顯示結果只從透過連接器編製索引的內容。</span><span class="sxs-lookup"><span data-stu-id="53aa7-119">You can add verticals to show results only from content indexed via connectors.</span></span>  

<span data-ttu-id="53aa7-120">**免責聲明：** 類別和結果類型是目前正在預覽 Microsoft Graph 連接器預覽的一部分。</span><span class="sxs-lookup"><span data-stu-id="53aa7-120">**DISCLAIMER:** Verticals and result types are currently in preview as a part of the Microsoft Graph connectors preview.</span></span> <span data-ttu-id="53aa7-121">您無法建立內容位於[sharepoint](http://sharepoint.com/)或從內容編製索引的[檔案共用連接器](file-share-connector.md)垂直。</span><span class="sxs-lookup"><span data-stu-id="53aa7-121">You can't create a vertical for content residing in [SharePoint](http://sharepoint.com/) or from content indexed by the [file share connector](file-share-connector.md).</span></span> <span data-ttu-id="53aa7-122">若要深入了解預覽，請參閱[連接器預覽](connectors-preview.md)。</span><span class="sxs-lookup"><span data-stu-id="53aa7-122">To find out more about the preview, see [Connectors Preview](connectors-preview.md).</span></span> <span data-ttu-id="53aa7-123">若要參與預覽，您必須先將提交[Microsoft Graph 連接器預覽註冊表單](https://forms.office.com/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbRxWYgu82J_RFnMMATAS6_chUNVYwNU1CMDNZUDBSSDZKWVo2RDJDRjRLQi4u)。</span><span class="sxs-lookup"><span data-stu-id="53aa7-123">To participate in the preview, you must first submit the [Microsoft Graph Connectors Preview Signup form](https://forms.office.com/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbRxWYgu82J_RFnMMATAS6_chUNVYwNU1CMDNZUDBSSDZKWVo2RDJDRjRLQi4u).</span></span>

## <a name="things-to-consider"></a><span data-ttu-id="53aa7-124">若要考慮的事項...]</span><span class="sxs-lookup"><span data-stu-id="53aa7-124">Things to consider...</span></span>

<span data-ttu-id="53aa7-125">在您開始之前，請確定已編製索引連接器。</span><span class="sxs-lookup"><span data-stu-id="53aa7-125">Before you start, make sure the connector has been indexed.</span></span> <span data-ttu-id="53aa7-126">可能需要多達 48 小時，根據檔案大小。</span><span class="sxs-lookup"><span data-stu-id="53aa7-126">It can take up to 48 hours, depending on the file size.</span></span>

<span data-ttu-id="53aa7-127">您無法建立內容位於[sharepoint](http://sharepoint.com/)或從內容編製索引的[檔案共用連接器](file-share-connector.md)垂直。</span><span class="sxs-lookup"><span data-stu-id="53aa7-127">You can’t create a vertical for content residing in [SharePoint](http://sharepoint.com/) or from content indexed by the [file share connector](file-share-connector.md).</span></span> <span data-ttu-id="53aa7-128">了解如何[索引內容](configure-connector.md)。</span><span class="sxs-lookup"><span data-stu-id="53aa7-128">Learn how to [index content](configure-connector.md).</span></span>

<span data-ttu-id="53aa7-129">在高的層級，有新增垂直的三個主要步驟：</span><span class="sxs-lookup"><span data-stu-id="53aa7-129">At a high level, there are three main steps for adding a vertical:</span></span> 

1. <span data-ttu-id="53aa7-130">建立類別。</span><span class="sxs-lookup"><span data-stu-id="53aa7-130">Create the vertical.</span></span> <span data-ttu-id="53aa7-131">在此步驟中，您定義的類別名稱、 內容來源及要搜尋的內容的範圍。</span><span class="sxs-lookup"><span data-stu-id="53aa7-131">In this step, you define the vertical’s name, content source, and scope of the content to search.</span></span> 
2. <span data-ttu-id="53aa7-132">定義此類別的結果看起來像。</span><span class="sxs-lookup"><span data-stu-id="53aa7-132">Define what the results for this vertical will look like.</span></span>  
3. <span data-ttu-id="53aa7-133">啟用 （若要顯示） 從 [類別] 清單] 頁面上的類別。</span><span class="sxs-lookup"><span data-stu-id="53aa7-133">Enable the vertical (to be displayed) from the vertical list page.</span></span>   

## <a name="step-1-create-the-search-vertical"></a><span data-ttu-id="53aa7-134">步驟 1： 建立搜尋類別</span><span class="sxs-lookup"><span data-stu-id="53aa7-134">STEP 1: Create the search vertical</span></span>

<span data-ttu-id="53aa7-135">啟動精靈之後，要引導您定義的類別名稱、 內容來源和範圍的內容，它會搜尋的步驟。</span><span class="sxs-lookup"><span data-stu-id="53aa7-135">After you start the wizard, you're guided through the steps to define the vertical's name, content source, and scope of the content that it will search.</span></span> <span data-ttu-id="53aa7-136">垂直會建立在停用狀態。</span><span class="sxs-lookup"><span data-stu-id="53aa7-136">The vertical is created in a disabled state.</span></span> <span data-ttu-id="53aa7-137">您將稍後啟用垂直。</span><span class="sxs-lookup"><span data-stu-id="53aa7-137">You'll enable the vertical later.</span></span>

<span data-ttu-id="53aa7-138">您可以使用一組有限的[關鍵字查詢語言 (KQL)](https://docs.microsoft.com/sharepoint/dev/general-development/keyword-query-language-kql-syntax-reference)來縮小範圍，以及 [] 頁面上列出您可以使用的屬性。</span><span class="sxs-lookup"><span data-stu-id="53aa7-138">You can use a limited set of the [Keyword Query Language (KQL)](https://docs.microsoft.com/sharepoint/dev/general-development/keyword-query-language-kql-syntax-reference) to narrow down the scope, and the page lists the properties available to you.</span></span> <span data-ttu-id="53aa7-139">我們建議使用免費的文字關鍵字和屬性限制布林運算子建立 KQL。</span><span class="sxs-lookup"><span data-stu-id="53aa7-139">We recommend using free text-keywords and property restrictions with boolean operators for creating the KQL.</span></span> 

### <a name="create-a-vertical-at-the-organization-level"></a><span data-ttu-id="53aa7-140">在組織層級建立類別</span><span class="sxs-lookup"><span data-stu-id="53aa7-140">Create a vertical at the organization level</span></span>

<span data-ttu-id="53aa7-141">若要在 Microsoft Search in [SharePoint](http://sharepoint.com/)首頁、 [Office](https://Office.com)或[Bing](https://Bing.com)上建立類別，請遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="53aa7-141">To create the vertical on Microsoft Search in [SharePoint](http://sharepoint.com/) home, [Office](https://Office.com), or [Bing](https://Bing.com), follow these steps:</span></span>

1. <span data-ttu-id="53aa7-142">在 Microsoft 365 [系統管理中心](https://admin.microsoft.com)中，移至 [ **設定** > **Microsoft Search** > **類別**。</span><span class="sxs-lookup"><span data-stu-id="53aa7-142">In the Microsoft 365 [admin center](https://admin.microsoft.com), go to **Settings** > **Microsoft Search** > **Verticals**.</span></span>
1. <span data-ttu-id="53aa7-143">選取 [ **新增**若要開始。</span><span class="sxs-lookup"><span data-stu-id="53aa7-143">Select **Add** to get started.</span></span>  

### <a name="create-a-vertical-at-the-site-level"></a><span data-ttu-id="53aa7-144">在網站層級建立類別</span><span class="sxs-lookup"><span data-stu-id="53aa7-144">Create a vertical at the site level</span></span>

1. <span data-ttu-id="53aa7-145">在您要建立垂直[SharePoint](http://sharepoint.com/)網站] 移至 [**設定**。</span><span class="sxs-lookup"><span data-stu-id="53aa7-145">On the [SharePoint](http://sharepoint.com/) site where you want to create the vertical, go to **Settings**.</span></span>
1. <span data-ttu-id="53aa7-146">選取 [**站台資訊**，然後**檢視所有網站設定**]。</span><span class="sxs-lookup"><span data-stu-id="53aa7-146">Select **Site information** and then **View all site settings**.</span></span>
1. <span data-ttu-id="53aa7-147">尋找 [ **Microsoft 搜尋**] 區段，然後選取 [**此網站集合設定 Microsoft Search**。</span><span class="sxs-lookup"><span data-stu-id="53aa7-147">Look for the **Microsoft Search** section, and then select **Configure Microsoft Search for this site collection**.</span></span>
1. <span data-ttu-id="53aa7-148">在功能窗格中，移至 **自訂體驗**，，然後選取 [**類別**] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="53aa7-148">In the navigation pane, go to **Custom experience**, and then select the **Verticals** tab.</span></span>
1. <span data-ttu-id="53aa7-149">若要新增的類別，選取 [ **新增**。</span><span class="sxs-lookup"><span data-stu-id="53aa7-149">To add a vertical, select **Add**.</span></span> <br>
<span data-ttu-id="53aa7-150">OR</span><span class="sxs-lookup"><span data-stu-id="53aa7-150">OR</span></span> <br><span data-ttu-id="53aa7-151">若要編輯類別，請在清單中選取。</span><span class="sxs-lookup"><span data-stu-id="53aa7-151">To edit a vertical, select it in the list.</span></span>

<span data-ttu-id="53aa7-152">請記住，類別建立在停用狀態。</span><span class="sxs-lookup"><span data-stu-id="53aa7-152">Remember, verticals are created in a disabled state.</span></span> <span data-ttu-id="53aa7-153">您仍然需要啟用這些使用者可以瀏覽類別之前。</span><span class="sxs-lookup"><span data-stu-id="53aa7-153">You still need to enable them before users can see the verticals.</span></span>

## <a name="step-2-create-the-result-types"></a><span data-ttu-id="53aa7-154">步驟 2： 建立結果類型</span><span class="sxs-lookup"><span data-stu-id="53aa7-154">STEP 2: Create the result types</span></span>

<span data-ttu-id="53aa7-155">您可以定義結果的顯示方式垂直向內所設計使用結果類型的版面配置。</span><span class="sxs-lookup"><span data-stu-id="53aa7-155">You can define how results are displayed in the vertical by designing the layout using result types.</span></span> <span data-ttu-id="53aa7-156">結果版面配置可讓您直接在搜尋結果中，顯示重要的資訊，讓使用者不需要選取如果他們已找到他們要尋找的每個搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="53aa7-156">The result layout lets you show important information directly in the search results, so that users don't have to select each result to see if they've found what they're looking for.</span></span>

<span data-ttu-id="53aa7-p112">搜尋「結果類型」是一種規則，可讓不同類型的搜尋結果以不同方式顯示。其由下列項目組成：</span><span class="sxs-lookup"><span data-stu-id="53aa7-p112">A search result type is a rule that causes distinct kinds of search results to be displayed in different ways. It consists of the following:</span></span>

- <span data-ttu-id="53aa7-159">若要比較，針對每個搜尋結果，例如搜尋結果的內容來源的**一個或多個條件**。</span><span class="sxs-lookup"><span data-stu-id="53aa7-159">**One or more conditions** to compare each search result against, such as the content source of the search result.</span></span>  
- <span data-ttu-id="53aa7-160">使用 [搜尋結果符合條件的**結果版面配置**。</span><span class="sxs-lookup"><span data-stu-id="53aa7-160">A **result layout** to use for search results that meet the conditions.</span></span> <span data-ttu-id="53aa7-161">結果版面配置會控制所有符合條件的結果會出現和搜尋結果頁面上的行為的方式。</span><span class="sxs-lookup"><span data-stu-id="53aa7-161">The result layout controls the way in which all results that meet the conditions appear and behave on a search results page.</span></span>

<span data-ttu-id="53aa7-162">**您必須建立至少一個結果型別上垂直顯示結果。**</span><span class="sxs-lookup"><span data-stu-id="53aa7-162">**You must create at least one result type for results to display on the vertical.**</span></span> <span data-ttu-id="53aa7-163">您可以建立多個結果類型的每個類別，讓您可以使用不同的版面配置的不同類型的結果。</span><span class="sxs-lookup"><span data-stu-id="53aa7-163">You can create multiple result types for each vertical, which allows you to use different layouts for different type of results.</span></span> <span data-ttu-id="53aa7-164">例如，您可以自訂更為顯著的色彩和更大的字型，相較於**嚴重性 3**事件**嚴重性 1**事件。</span><span class="sxs-lookup"><span data-stu-id="53aa7-164">For example, you can customize **Severity 1** incidents to have more prominent colors and a larger font compared to **Severity 3** incidents.</span></span> 

<span data-ttu-id="53aa7-165">啟動精靈之後，要引導您定義的名稱、 內容來源和條件的結果類型的步驟。</span><span class="sxs-lookup"><span data-stu-id="53aa7-165">After you start the wizard, you're guided through the steps to define the name, content source, and conditions for the result type.</span></span> <span data-ttu-id="53aa7-166">您可以定義結果類型，從清單檢視的優先順序。</span><span class="sxs-lookup"><span data-stu-id="53aa7-166">You can define the priority of the result type from the list view.</span></span> 
  
### <a name="create-a-result-type-at-the-organization-level"></a><span data-ttu-id="53aa7-167">在組織層級建立結果類型</span><span class="sxs-lookup"><span data-stu-id="53aa7-167">Create a result type at the organization level</span></span>

1. <span data-ttu-id="53aa7-168">在[系統管理中心](https://admin.microsoft.com)中，前往 [**設定** > **Microsoft Search**，，然後選取 [**輸入的結果**。</span><span class="sxs-lookup"><span data-stu-id="53aa7-168">In the [admin center](https://admin.microsoft.com), go to **Setting** > **Microsoft Search**, and then select **Result type**.</span></span>
1. <span data-ttu-id="53aa7-169">若要新增**結果類型**，選取 [ **新增**。</span><span class="sxs-lookup"><span data-stu-id="53aa7-169">To add a **Result type**, select **Add**.</span></span> <span data-ttu-id="53aa7-170">若要編輯的結果類型，請在相關的清單中選取結果類型。</span><span class="sxs-lookup"><span data-stu-id="53aa7-170">To edit a result type, select the result type in the relevant list.</span></span>
 
### <a name="create-a-results-type-at-the-site-level"></a><span data-ttu-id="53aa7-171">網站層級建立結果類型</span><span class="sxs-lookup"><span data-stu-id="53aa7-171">Create a results type at the site level</span></span>

1. <span data-ttu-id="53aa7-172">在[SharePoint](http://sharepoint.com/)網站上您要建立結果類型，請移至**設定**。</span><span class="sxs-lookup"><span data-stu-id="53aa7-172">On the [SharePoint](http://sharepoint.com/) site where you want to create the result type, go to **Settings**.</span></span>
1. <span data-ttu-id="53aa7-173">選取 [**站台資訊**，然後**檢視所有網站設定**]。</span><span class="sxs-lookup"><span data-stu-id="53aa7-173">Select **Site information** and then **View all site settings**.</span></span> 
1. <span data-ttu-id="53aa7-174">尋找 [Microsoft 搜尋] 區段，然後選取 [**此網站集合設定 Microsoft Search**。</span><span class="sxs-lookup"><span data-stu-id="53aa7-174">Look for the Microsoft Search section, and then select **Configure Microsoft Search for this site collection**.</span></span>
1. <span data-ttu-id="53aa7-175">在功能窗格中，移至 **自訂體驗**，，然後選取**結果類型**] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="53aa7-175">In the navigation pane, go to **Custom experience**, and then select **Result type** tab.</span></span>
1. <span data-ttu-id="53aa7-176">若要新增結果類型，選取 [ **新增]**。</span><span class="sxs-lookup"><span data-stu-id="53aa7-176">To add a result type, select **Add**.</span></span> <br> <span data-ttu-id="53aa7-177">OR</span><span class="sxs-lookup"><span data-stu-id="53aa7-177">OR</span></span> <br><span data-ttu-id="53aa7-178">若要編輯的結果類型，請在清單中選取結果類型。</span><span class="sxs-lookup"><span data-stu-id="53aa7-178">To edit a result type, select the result type in the list.</span></span>

### <a name="view-the-vertical-after-enabling"></a><span data-ttu-id="53aa7-179">檢視在啟用之後的類別</span><span class="sxs-lookup"><span data-stu-id="53aa7-179">View the vertical after enabling</span></span>

<span data-ttu-id="53aa7-180">啟用垂直之後，它可能需要一段時間，才可以檢視。</span><span class="sxs-lookup"><span data-stu-id="53aa7-180">After you enable the vertical, it might take a while before you can view it.</span></span>
<span data-ttu-id="53aa7-181">如果您想要等候啟用它之後，您可以將附加**cacheClear = true** [SharePoint](http://sharepoint.com/)和[Office](https://Office.com)立即檢視類別中的 url。</span><span class="sxs-lookup"><span data-stu-id="53aa7-181">If you want to wait after enabling it, you can append **cacheClear=true** to the URL in [SharePoint](http://sharepoint.com/) and [Office](https://Office.com) to view the vertical immediately.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="53aa7-182">疑難排解</span><span class="sxs-lookup"><span data-stu-id="53aa7-182">Troubleshooting</span></span>

<span data-ttu-id="53aa7-183">以下是您可能會遇到的常見問題和修正它們的動作清單。</span><span class="sxs-lookup"><span data-stu-id="53aa7-183">Here's a list of common issues you might encounter and actions for fixing them.</span></span>


|<span data-ttu-id="53aa7-184">Error</span><span class="sxs-lookup"><span data-stu-id="53aa7-184">Error</span></span>  |<span data-ttu-id="53aa7-185">動作</span><span class="sxs-lookup"><span data-stu-id="53aa7-185">Action</span></span>  |
|---------|---------|
|<span data-ttu-id="53aa7-186">我在垂直看見*發生錯誤*的錯誤。</span><span class="sxs-lookup"><span data-stu-id="53aa7-186">I see a *Something went wrong* error on the vertical.</span></span> |   <span data-ttu-id="53aa7-187">這兩個類別和結果類型所需完成安裝。</span><span class="sxs-lookup"><span data-stu-id="53aa7-187">Both vertical and result types are needed to complete the setup.</span></span> <span data-ttu-id="53aa7-188">請確定您已建立兩個相同的內容來源。</span><span class="sxs-lookup"><span data-stu-id="53aa7-188">Make sure you have created both for the same content source.</span></span>      |
|<span data-ttu-id="53aa7-189">為什麼我看我結果版面配置，雖然已建立一個？</span><span class="sxs-lookup"><span data-stu-id="53aa7-189">Why don't I see my result layout, although I have created one?</span></span> | <span data-ttu-id="53aa7-190">花幾分鐘的結果類型]，以用於為這些設定通常會快取。</span><span class="sxs-lookup"><span data-stu-id="53aa7-190">It takes a few minutes for result types to be used as these settings are generally cached.</span></span> <span data-ttu-id="53aa7-191">等候幾分鐘，然後再試一次。</span><span class="sxs-lookup"><span data-stu-id="53aa7-191">Wait for a few minutes and try again.</span></span>        |
|<span data-ttu-id="53aa7-192">看不到任何垂直上的內容來源] 或 [結果類型] 頁面。</span><span class="sxs-lookup"><span data-stu-id="53aa7-192">I don't see any content sources on the vertical or result type page.</span></span>     |      <span data-ttu-id="53aa7-193">請確定您已設定連接器和編製索引的資料。</span><span class="sxs-lookup"><span data-stu-id="53aa7-193">Make sure you have configured connectors and indexed data.</span></span>   |



## <a name="next-steps"></a><span data-ttu-id="53aa7-194">後續步驟</span><span class="sxs-lookup"><span data-stu-id="53aa7-194">Next steps</span></span>
[<span data-ttu-id="53aa7-195">步驟 3： 自訂結果版面配置</span><span class="sxs-lookup"><span data-stu-id="53aa7-195">STEP 3: Customize the results layout</span></span>](customize-results-layout.md)
