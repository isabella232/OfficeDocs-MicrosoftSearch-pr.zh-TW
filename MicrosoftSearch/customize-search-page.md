---
title: 自訂 Microsoft 搜尋頁面
ms.author: jeffkizn
author: jypal
manager: jeffkizn
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 新增搜尋行業及自訂搜尋結果
ms.openlocfilehash: c6104383698203fde48d217506da57941efa680f
ms.sourcegitcommit: 0aca0a5c9152b1b5e8345c91edadfae0b30f57c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/05/2021
ms.locfileid: "51587737"
---
# <a name="customize-the-search-results-page"></a><span data-ttu-id="2272e-103">自訂搜尋結果頁面</span><span class="sxs-lookup"><span data-stu-id="2272e-103">Customize the search results page</span></span>

<span data-ttu-id="2272e-104">您可以建立搜尋類別和結果類型，以自訂使用者在 Microsoft [SharePoint](https://sharepoint.com/)、 [Microsoft Office](https://office.com)和 microsoft search in [Bing](https://bing.com)中搜尋時所看到的搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="2272e-104">You can create search verticals and result types to customize the search results that users see when they search in Microsoft [SharePoint](https://sharepoint.com/), [Microsoft Office](https://office.com), and Microsoft Search in [Bing](https://bing.com).</span></span> <span data-ttu-id="2272e-105">縱向使用者可讓使用者更輕鬆地找到他們具有查看許可權的資訊。</span><span class="sxs-lookup"><span data-stu-id="2272e-105">Verticals make it easier for users to find the information that they have permission to see.</span></span> <span data-ttu-id="2272e-106">例如，您可以為行銷部門中的使用者建立協力廠商軟體的「行銷分析」資料的搜尋類別。</span><span class="sxs-lookup"><span data-stu-id="2272e-106">For example, you could create a search vertical for marketing analysis data from third-party software for your users in the marketing department.</span></span> <span data-ttu-id="2272e-107">您也可以定義結果類型及自訂此資料的版面配置。</span><span class="sxs-lookup"><span data-stu-id="2272e-107">You can also define result types and customize the layout for this data.</span></span>  

<span data-ttu-id="2272e-108">您可以在下列各層級建立縱向和結果類型：</span><span class="sxs-lookup"><span data-stu-id="2272e-108">You can create verticals and result types at these levels:</span></span>

- <span data-ttu-id="2272e-109">**組織層級** –當您在組織層級新增垂直時，當使用者從他們的 [SharePoint](https://sharepoint.com/) 開始頁面、 [Office](https://office.com)或 [Bing](https://bing.com)進行搜尋時，它會出現在搜尋結果頁面上。</span><span class="sxs-lookup"><span data-stu-id="2272e-109">**Organization level** – When you add a vertical at the organization level, it appears on the search results page when users search from their [SharePoint](https://sharepoint.com/) start page, on [Office](https://office.com), or on [Bing](https://bing.com).</span></span>
- <span data-ttu-id="2272e-110">**網站層級** –例如，您可能想要讓客戶服務員工直接從部門的 SharePoint 網站搜尋 *嚴重性 1* 事件。</span><span class="sxs-lookup"><span data-stu-id="2272e-110">**Site level** – For example, you might want to enable your customer service employees to search for *Severity 1* incidents directly from their department’s SharePoint site.</span></span>

## <a name="search-verticals-explained"></a><span data-ttu-id="2272e-111">說明的搜尋縱向</span><span class="sxs-lookup"><span data-stu-id="2272e-111">Search verticals explained</span></span>

<span data-ttu-id="2272e-112">在 [Microsoft 搜尋結果] 頁面的頂端有一列索引標籤。</span><span class="sxs-lookup"><span data-stu-id="2272e-112">At the top of the Microsoft Search results page, there's a row of tabs.</span></span> <span data-ttu-id="2272e-113">這些是搜尋行業。</span><span class="sxs-lookup"><span data-stu-id="2272e-113">These are the search verticals.</span></span> <span data-ttu-id="2272e-114">搜尋類別只會顯示特定類型或特定內容的結果。</span><span class="sxs-lookup"><span data-stu-id="2272e-114">A search vertical only shows results of a certain type or from certain content.</span></span> <span data-ttu-id="2272e-115">例如 **檔** 或 **新聞**。</span><span class="sxs-lookup"><span data-stu-id="2272e-115">Examples are **Files** or **News**.</span></span> <span data-ttu-id="2272e-116">根據預設，Microsoft 搜尋會顯示縱向 **所有** 的 **人員**、 **檔**、 **網站** 和 **新聞**。</span><span class="sxs-lookup"><span data-stu-id="2272e-116">By default, Microsoft Search shows the verticals **All**, **People**, **Files**, **Sites**, and **News**.</span></span>  

<span data-ttu-id="2272e-117">您可以新增與您組織相關的搜尋行業。</span><span class="sxs-lookup"><span data-stu-id="2272e-117">You can add search verticals that are relevant to your organization.</span></span> <span data-ttu-id="2272e-118">這些會出現在 [ [SharePoint](https://sharepoint.com/)]、[ [Office](https://Office.com)] 及 [ [Bing](https://bing.com)] 的 [Microsoft 搜尋結果] 頁面上。</span><span class="sxs-lookup"><span data-stu-id="2272e-118">These will appear on the Microsoft Search results page in [SharePoint](https://sharepoint.com/), [Office](https://Office.com), and [Bing](https://bing.com).</span></span> <span data-ttu-id="2272e-119">例如，您可以根據每個群組所需的資訊類型，為行銷相關的內容及另一個銷售人員建立垂直。</span><span class="sxs-lookup"><span data-stu-id="2272e-119">For example, you could create a vertical for marketing-related content and another for sales, based on the type of information that each group needs.</span></span> <span data-ttu-id="2272e-120">您可以新增縱向，只顯示透過連接器編制索引的內容的結果。</span><span class="sxs-lookup"><span data-stu-id="2272e-120">You can add verticals to show results only from content indexed via connectors.</span></span>  

### <a name="multiple-connections-in-a-vertical"></a><span data-ttu-id="2272e-121">垂直中的多個連接</span><span class="sxs-lookup"><span data-stu-id="2272e-121">Multiple connections in a vertical</span></span>

<span data-ttu-id="2272e-122">「搜尋類別」現在可以透過多個連接器來源呈現結果。</span><span class="sxs-lookup"><span data-stu-id="2272e-122">A search vertical can now surface results from multiple connector sources.</span></span> <span data-ttu-id="2272e-123">這為設計搜尋結果頁面提供更大的彈性。</span><span class="sxs-lookup"><span data-stu-id="2272e-123">This provides greater flexibility in designing your search result page.</span></span> <span data-ttu-id="2272e-124">現有的垂直安裝管理體驗可讓您在「內容來源」步驟中選取多個連接。</span><span class="sxs-lookup"><span data-stu-id="2272e-124">The existing administrative experience of vertical setup allows you to select multiple connections in the "Content Source" step.</span></span>
<span data-ttu-id="2272e-125">如果您正確指派盡可能多的語義標籤，則會增強這種體驗。</span><span class="sxs-lookup"><span data-stu-id="2272e-125">If you accurately appoint as many semantic labels as possible, this experience will be enhanced.</span></span> <span data-ttu-id="2272e-126">您可以在架構定義及攝取時新增語義標籤。</span><span class="sxs-lookup"><span data-stu-id="2272e-126">You can add semantic labels upon schema definition and ingestion.</span></span>

<span data-ttu-id="2272e-127">[以下](configure-connector.md#step-5-assign-property-labels) 是如何建立及管理語義標籤的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="2272e-127">[Here](configure-connector.md#step-5-assign-property-labels) is additional information on how to create and manage semantic labels.</span></span>

### <a name="things-you-should-know"></a><span data-ttu-id="2272e-128">您應該知道的事項</span><span class="sxs-lookup"><span data-stu-id="2272e-128">Things you should know</span></span>

1. <span data-ttu-id="2272e-129">可以將連線新增為一個垂直下方的內容來源。</span><span class="sxs-lookup"><span data-stu-id="2272e-129">A connection can be added as a content source only under one vertical.</span></span> <span data-ttu-id="2272e-130">不允許重複使用多個行業的連線。</span><span class="sxs-lookup"><span data-stu-id="2272e-130">Reusing connections under multiple verticals is not allowed.</span></span>
2. <span data-ttu-id="2272e-131">如果您需要為已新增多個連線來源的搜尋類別設定查詢，則應該使用一般來源屬性來建立這類查詢。</span><span class="sxs-lookup"><span data-stu-id="2272e-131">If you need to setup a query for a search vertical where multiple connection sources have been added, common source properties should be used to create a such a query.</span></span>

## <a name="things-to-consider"></a><span data-ttu-id="2272e-132">考慮事項</span><span class="sxs-lookup"><span data-stu-id="2272e-132">Things to consider</span></span>

<span data-ttu-id="2272e-133">開始之前，請確定連接器已編制索引。</span><span class="sxs-lookup"><span data-stu-id="2272e-133">Before you start, make sure that the connector has been indexed.</span></span> <span data-ttu-id="2272e-134">這可能需要最多48小時，視檔案大小而定。</span><span class="sxs-lookup"><span data-stu-id="2272e-134">This can take up to 48 hours, depending on the file size.</span></span>

<span data-ttu-id="2272e-135">您無法為位於 [SharePoint](https://sharepoint.com/)中的內容建立垂直。</span><span class="sxs-lookup"><span data-stu-id="2272e-135">You can’t create a vertical for content that resides in [SharePoint](https://sharepoint.com/).</span></span>

<span data-ttu-id="2272e-136">新增垂直的三個基本步驟：</span><span class="sxs-lookup"><span data-stu-id="2272e-136">There are three basic steps to add a vertical:</span></span>

1. <span data-ttu-id="2272e-137">建立垂直。</span><span class="sxs-lookup"><span data-stu-id="2272e-137">Create the vertical.</span></span> <span data-ttu-id="2272e-138">在這個步驟中，您會定義要搜尋之內容的直排名稱、內容來源及範圍。</span><span class="sxs-lookup"><span data-stu-id="2272e-138">In this step, you define the vertical’s name, content source, and scope of the content to search.</span></span>
2. <span data-ttu-id="2272e-139">定義此垂直方向的結果外觀。</span><span class="sxs-lookup"><span data-stu-id="2272e-139">Define what the results for this vertical will look like.</span></span>  
3. <span data-ttu-id="2272e-140">啟用從垂直清單頁面) 顯示的垂直 (。</span><span class="sxs-lookup"><span data-stu-id="2272e-140">Enable the vertical (to be displayed) from the vertical list page.</span></span>

## <a name="step-1-create-the-search-vertical"></a><span data-ttu-id="2272e-141">步驟1：建立搜尋類別</span><span class="sxs-lookup"><span data-stu-id="2272e-141">STEP 1: Create the search vertical</span></span>

<span data-ttu-id="2272e-142">啟動該嚮導之後，您會逐步指導您定義要搜尋之內容的垂直名稱、內容來源及範圍。</span><span class="sxs-lookup"><span data-stu-id="2272e-142">After you start the wizard, you're guided through the steps to define the vertical's name, content source, and scope of the content to search.</span></span> <span data-ttu-id="2272e-143">會以停用狀態建立垂直。</span><span class="sxs-lookup"><span data-stu-id="2272e-143">The vertical is created in a disabled state.</span></span> <span data-ttu-id="2272e-144">您將在稍後啟用它。</span><span class="sxs-lookup"><span data-stu-id="2272e-144">You'll enable it later.</span></span>

<span data-ttu-id="2272e-145">您可以使用一組有限的 [關鍵字查詢語言 (KQL) ](/sharepoint/dev/general-development/keyword-query-language-kql-syntax-reference) 來縮小範圍。</span><span class="sxs-lookup"><span data-stu-id="2272e-145">You can use a limited set of [Keyword Query Language (KQL)](/sharepoint/dev/general-development/keyword-query-language-kql-syntax-reference) to narrow the scope.</span></span> <span data-ttu-id="2272e-146">此頁面列出可用的屬性。</span><span class="sxs-lookup"><span data-stu-id="2272e-146">This page lists the properties that are available.</span></span> <span data-ttu-id="2272e-147">建議您使用具有 boolean 運算子的任意文字關鍵字和屬性限制，以建立 KQL。</span><span class="sxs-lookup"><span data-stu-id="2272e-147">We recommend that you use free-text keywords and property restrictions with boolean operators for creating the KQL.</span></span>

### <a name="create-a-vertical-at-the-organization-level"></a><span data-ttu-id="2272e-148">在組織層級建立垂直</span><span class="sxs-lookup"><span data-stu-id="2272e-148">Create a vertical at the organization level</span></span>

<span data-ttu-id="2272e-149">若要在 [SharePoint](https://sharepoint.com/) Home、 [Office](https://office.com)或 [Bing](https://bing.com)中的 Microsoft 搜尋上建立垂直，請遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="2272e-149">To create the vertical on Microsoft Search in [SharePoint](https://sharepoint.com/) home, [Office](https://office.com), or [Bing](https://bing.com), follow these steps:</span></span>

1. <span data-ttu-id="2272e-150">在 [Microsoft 365 系統管理中心](https://admin.microsoft.com)中，移至 [ [**縱向**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/verticals)]。</span><span class="sxs-lookup"><span data-stu-id="2272e-150">In the [Microsoft 365 admin center](https://admin.microsoft.com), go to [**Verticals**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/verticals).</span></span>
2. <span data-ttu-id="2272e-151">選取 [ **新增** ] 立即開始。</span><span class="sxs-lookup"><span data-stu-id="2272e-151">Select **Add** to get started.</span></span>  

### <a name="create-a-vertical-at-the-site-level"></a><span data-ttu-id="2272e-152">在網站層級建立垂直</span><span class="sxs-lookup"><span data-stu-id="2272e-152">Create a vertical at the site level</span></span>

1. <span data-ttu-id="2272e-153">在您要垂直的 [SharePoint](https://sharepoint.com/) 網站上，移至 [ **設定**]。</span><span class="sxs-lookup"><span data-stu-id="2272e-153">On the [SharePoint](https://sharepoint.com/) site where you want the vertical, go to **Settings**.</span></span>
2. <span data-ttu-id="2272e-154">選取 [ **網站資訊** ]，然後 **查看 [所有網站設定**]。</span><span class="sxs-lookup"><span data-stu-id="2272e-154">Select **Site information** and then **View all site settings**.</span></span>
3. <span data-ttu-id="2272e-155">尋找 [ **Microsoft 搜尋** ] 區段，然後選取 [ **設定此網站集合的 microsoft search**]。</span><span class="sxs-lookup"><span data-stu-id="2272e-155">Look for the **Microsoft Search** section, and then select **Configure Microsoft Search for this site collection**.</span></span>
4. <span data-ttu-id="2272e-156">在功能窗格中，移至 [ **自訂經驗**]，然後選取 [ **縱向** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="2272e-156">In the navigation pane, go to **Custom experience**, and then select the **Verticals** tab.</span></span>
5. <span data-ttu-id="2272e-157">若要新增垂直，請選取 [ **新增**]。</span><span class="sxs-lookup"><span data-stu-id="2272e-157">To add a vertical, select **Add**.</span></span>
  <span data-ttu-id="2272e-158">或者，若要編輯垂直，請在清單中選取它。</span><span class="sxs-lookup"><span data-stu-id="2272e-158">Or, to edit a vertical, select it in the list.</span></span>

<span data-ttu-id="2272e-159">請記住，會以停用狀態建立縱向。</span><span class="sxs-lookup"><span data-stu-id="2272e-159">Remember, verticals are created in a disabled state.</span></span> <span data-ttu-id="2272e-160">您必須先啟用這些功能，使用者才能看到它們。</span><span class="sxs-lookup"><span data-stu-id="2272e-160">They must be enabled before users can see them.</span></span>

## <a name="step-2-create-the-result-types"></a><span data-ttu-id="2272e-161">步驟2：建立結果類型</span><span class="sxs-lookup"><span data-stu-id="2272e-161">STEP 2: Create the result types</span></span>

<span data-ttu-id="2272e-162">您可以使用結果類型來設計版面配置，以定義結果在垂直方向上的顯示方式。</span><span class="sxs-lookup"><span data-stu-id="2272e-162">You can define how results are displayed in the vertical by designing the layout using result types.</span></span> <span data-ttu-id="2272e-163">結果配置可讓您直接在搜尋結果中顯示重要資訊，因此使用者不必選取每個結果，即可查看其是否找到所要尋找的專案。</span><span class="sxs-lookup"><span data-stu-id="2272e-163">The result layout lets you show important information directly in the search results, so users don't have to select each result to see if they found what they're looking for.</span></span>

### <a name="default-search-result-layout"></a><span data-ttu-id="2272e-164">預設搜尋結果版面配置</span><span class="sxs-lookup"><span data-stu-id="2272e-164">Default search result layout</span></span>

<span data-ttu-id="2272e-165">如果在設定連接器時， **標籤** 和 **內容** 屬性已正確對應至來源內容，則會針對連接器內容顯示預設的搜尋結果版面配置。</span><span class="sxs-lookup"><span data-stu-id="2272e-165">A default search result layout will be shown for Connector content if **labels** and **content** property have been mapped correctly to the source properties at the time of configuring the connector.</span></span> <span data-ttu-id="2272e-166">標籤 **標題** 是最重要的標籤。</span><span class="sxs-lookup"><span data-stu-id="2272e-166">The label **title** is the most important label.</span></span> <span data-ttu-id="2272e-167">**強烈建議** 您指派此標籤的屬性，以使用預設搜尋結果版面配置。</span><span class="sxs-lookup"><span data-stu-id="2272e-167">It is **strongly recommended** that you have a property assigned to this label to use default search result layout.</span></span>

### <a name="create-your-own-result-type"></a><span data-ttu-id="2272e-168">建立您自己的結果類型</span><span class="sxs-lookup"><span data-stu-id="2272e-168">Create your own result type</span></span>

<span data-ttu-id="2272e-169">您可以決定建立您自己的搜尋結果版面配置，並透過建立 **結果類型** 來覆寫預設搜尋結果版面配置。</span><span class="sxs-lookup"><span data-stu-id="2272e-169">You can decide to create your own search result layout and override the default search result layout by creating a **result type**.</span></span> <span data-ttu-id="2272e-170">搜尋結果類型是一種規則，會以不同方式顯示不同類型的搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="2272e-170">A search result type is a rule that causes distinct kinds of search results to be displayed in different ways.</span></span> <span data-ttu-id="2272e-171">其包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="2272e-171">It consists of the following:</span></span>

- <span data-ttu-id="2272e-172">**一個或多個** 比較每個搜尋結果的條件，例如搜尋結果的內容來源。</span><span class="sxs-lookup"><span data-stu-id="2272e-172">**One or more conditions** to compare each search result against, such as the content source of the search result.</span></span>  
- <span data-ttu-id="2272e-173">用於符合條件之搜尋結果的 **結果版面** 配置。</span><span class="sxs-lookup"><span data-stu-id="2272e-173">A **result layout** to use for search results that meet the conditions.</span></span> <span data-ttu-id="2272e-174">結果版面配置會控制符合條件的所有結果在搜尋結果頁面上顯示和行為的方式。</span><span class="sxs-lookup"><span data-stu-id="2272e-174">The result layout controls the way that all results that meet the conditions appear and behave on a search results page.</span></span>

<span data-ttu-id="2272e-175">**如果適當的對應無法顯示預設搜尋結果版面配置，您必須至少建立一個結果類型的結果，以顯示在垂直上。**</span><span class="sxs-lookup"><span data-stu-id="2272e-175">**If appropriate mapping is not done to show default search result layout, You must create at least one result type for results to display on the vertical.**</span></span> <span data-ttu-id="2272e-176">您可以為每個垂直方向建立多種結果類型，這可讓您針對不同類型的結果使用不同的版面配置。</span><span class="sxs-lookup"><span data-stu-id="2272e-176">You can create multiple result types for each vertical, which allows you to use different layouts for different type of results.</span></span> <span data-ttu-id="2272e-177">例如，您可以自訂 *嚴重性為 1* 的事件，使其具有更醒目的色彩和更大的字型，與 *嚴重的 3* 個事件相較。</span><span class="sxs-lookup"><span data-stu-id="2272e-177">For example, you can customize *Severity 1* incidents to have more prominent colors and a larger font compared to *Severity 3* incidents.</span></span>

<span data-ttu-id="2272e-178">啟動該嚮導之後，您會逐步指導您定義結果類型的名稱、內容來源及條件。</span><span class="sxs-lookup"><span data-stu-id="2272e-178">After you start the wizard, you're guided through the steps to define the name, content source, and conditions for the result type.</span></span> <span data-ttu-id="2272e-179">您可以從清單視圖定義結果類型的優先順序。</span><span class="sxs-lookup"><span data-stu-id="2272e-179">You can define the priority of the result type from the list view.</span></span>
  
### <a name="create-a-result-type-at-the-organization-level"></a><span data-ttu-id="2272e-180">在組織層級建立結果類型</span><span class="sxs-lookup"><span data-stu-id="2272e-180">Create a result type at the organization level</span></span>

1. <span data-ttu-id="2272e-181">在 [Microsoft 365 系統管理中心](https://admin.microsoft.com)中，移至 [ [**結果類型**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/resulttypes)]。</span><span class="sxs-lookup"><span data-stu-id="2272e-181">In the [Microsoft 365 admin center](https://admin.microsoft.com), go to [**Result types**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/resulttypes).</span></span>
2. <span data-ttu-id="2272e-182">若要新增 **結果類型**，請選取 [ **新增**]。</span><span class="sxs-lookup"><span data-stu-id="2272e-182">To add a **Result type**, select **Add**.</span></span> <span data-ttu-id="2272e-183">若要編輯結果類型，請選取相關清單中的結果類型。</span><span class="sxs-lookup"><span data-stu-id="2272e-183">To edit a result type, select the result type in the relevant list.</span></span>

### <a name="create-a-results-type-at-the-site-level"></a><span data-ttu-id="2272e-184">在網站層級建立結果類型</span><span class="sxs-lookup"><span data-stu-id="2272e-184">Create a results type at the site level</span></span>

1. <span data-ttu-id="2272e-185">在您要建立結果類型的 [SharePoint](https://sharepoint.com/) 網站上，移至 [ **設定**]。</span><span class="sxs-lookup"><span data-stu-id="2272e-185">On the [SharePoint](https://sharepoint.com/) site where you want to create the result type, go to **Settings**.</span></span>
2. <span data-ttu-id="2272e-186">選取 [ **網站資訊** ]，然後 **查看 [所有網站設定**]。</span><span class="sxs-lookup"><span data-stu-id="2272e-186">Select **Site information** and then **View all site settings**.</span></span>
3. <span data-ttu-id="2272e-187">尋找 [Microsoft 搜尋] 區段，然後選取 [ **設定此網站集合的 Microsoft search**]。</span><span class="sxs-lookup"><span data-stu-id="2272e-187">Look for the Microsoft Search section, and then select **Configure Microsoft Search for this site collection**.</span></span>
4. <span data-ttu-id="2272e-188">在功能窗格中，移至 [ **自訂經驗**]，然後選取 [ **結果類型** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="2272e-188">In the navigation pane, go to **Custom experience**, and select **Result type** tab.</span></span>
5. <span data-ttu-id="2272e-189">若要新增結果類型，請選取 [ **新增**]。</span><span class="sxs-lookup"><span data-stu-id="2272e-189">To add a result type, select **Add**.</span></span>  <span data-ttu-id="2272e-190">或者，若要編輯結果類型，請選取清單中的結果類型。</span><span class="sxs-lookup"><span data-stu-id="2272e-190">Or, to edit a result type, select the result type in the list.</span></span>

## <a name="step-3-view-the-vertical-after-its-enabled"></a><span data-ttu-id="2272e-191">步驟3：在啟用垂直後查看</span><span class="sxs-lookup"><span data-stu-id="2272e-191">STEP 3: View the vertical after it's enabled</span></span>

<span data-ttu-id="2272e-192">在您啟用垂直後，您可以花幾小時的時間，才能進行查看。</span><span class="sxs-lookup"><span data-stu-id="2272e-192">After you enable the vertical, it will take a few hours before you can view it.</span></span> <span data-ttu-id="2272e-193">如果您不想要等到啟用它之後，您可以在 [SharePoint](https://sharepoint.com/)和 [Office](https://office.com)的 URL 中附加 **cacheClear = true** ，以立即查看垂直。</span><span class="sxs-lookup"><span data-stu-id="2272e-193">If you don't want to wait after enabling it, you can append **cacheClear=true** to the URL in [SharePoint](https://sharepoint.com/) and [Office](https://office.com) to view the vertical immediately.</span></span> <span data-ttu-id="2272e-194">針對 [Bing](https://bing.com)，append **&features = uncachedVerticals** 至工作垂直 URL，以立即查看縱向。</span><span class="sxs-lookup"><span data-stu-id="2272e-194">For [Bing](https://bing.com), append **&features=uncachedVerticals** to the Work vertical URL to view the verticals immediately.</span></span> 

> [!NOTE]
> <span data-ttu-id="2272e-195">從行動網頁瀏覽器查看時，在 [SharePoint](https://sharepoint.com/) 和 [Office](https://office.com) 上看不到所增添的縱向。</span><span class="sxs-lookup"><span data-stu-id="2272e-195">Added verticals will not be visible on [SharePoint](https://sharepoint.com/) and [Office](https://office.com) when viewed from mobile web browsers.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="2272e-196">疑難排解</span><span class="sxs-lookup"><span data-stu-id="2272e-196">Troubleshooting</span></span>

<span data-ttu-id="2272e-197">以下是您可能會遇到的常見問題清單，以及修正這些問題的動作。</span><span class="sxs-lookup"><span data-stu-id="2272e-197">Here's a list of common issues you might encounter and actions to fix them.</span></span>

|<span data-ttu-id="2272e-198">錯誤</span><span class="sxs-lookup"><span data-stu-id="2272e-198">Error</span></span>  |<span data-ttu-id="2272e-199">動作</span><span class="sxs-lookup"><span data-stu-id="2272e-199">Action</span></span>  |
|---------|---------|
| <span data-ttu-id="2272e-200">在垂直上看到「發生錯誤」錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="2272e-200">I see a "Something went wrong" error message on the vertical.</span></span> | <span data-ttu-id="2272e-201">需要有垂直和結果類型，才可完成設定。</span><span class="sxs-lookup"><span data-stu-id="2272e-201">Both the vertical and result types are needed to complete the setup.</span></span> <span data-ttu-id="2272e-202">請確定您已為相同的內容來源建立這兩者。</span><span class="sxs-lookup"><span data-stu-id="2272e-202">Make sure you have created both for the same content source.</span></span> |
| <span data-ttu-id="2272e-203">我沒有看到結果版面配置，但我已經建立了它。</span><span class="sxs-lookup"><span data-stu-id="2272e-203">I don't see my result layout, although I created one.</span></span> | <span data-ttu-id="2272e-204">因為這些設定通常會進行快取，所以需要數分鐘的時間。</span><span class="sxs-lookup"><span data-stu-id="2272e-204">It takes a few minutes because these settings are generally cached.</span></span> <span data-ttu-id="2272e-205">請等候幾分鐘後再試一次。</span><span class="sxs-lookup"><span data-stu-id="2272e-205">Wait for a few minutes and try again.</span></span>        |
| <span data-ttu-id="2272e-206">在 [垂直] 或 [結果類型] 頁面上沒有看到任何內容來源。</span><span class="sxs-lookup"><span data-stu-id="2272e-206">I don't see any content sources on the vertical or result type page.</span></span> | <span data-ttu-id="2272e-207">請確定您已設定連接器和索引的資料。</span><span class="sxs-lookup"><span data-stu-id="2272e-207">Make sure you have configured connectors and indexed data.</span></span>   |

## <a name="next-steps"></a><span data-ttu-id="2272e-208">後續步驟</span><span class="sxs-lookup"><span data-stu-id="2272e-208">Next steps</span></span>

[<span data-ttu-id="2272e-209">自訂結果版面配置</span><span class="sxs-lookup"><span data-stu-id="2272e-209">Customize the results layout</span></span>](customize-results-layout.md)
