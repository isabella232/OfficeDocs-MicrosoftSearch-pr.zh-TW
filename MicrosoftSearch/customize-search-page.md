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
ms.openlocfilehash: 4dd3f08f6d7e3df0aa983684eb0d4f649bc409a1
ms.sourcegitcommit: 1e766e1f549c46882f47df6679f5a3cdf48d70d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/16/2021
ms.locfileid: "53463224"
---
# <a name="customize-the-search-results-page"></a><span data-ttu-id="b4b3f-103">自訂搜尋結果頁面</span><span class="sxs-lookup"><span data-stu-id="b4b3f-103">Customize the search results page</span></span>

<span data-ttu-id="b4b3f-104">您可以建立搜尋類別和結果類型，以自訂使用者在 Microsoft [SharePoint](https://sharepoint.com/)、 [Microsoft Office](https://office.com)及 Microsoft 搜尋中的[Bing](https://bing.com)搜尋時所看到的搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-104">You can create search verticals and result types to customize the search results that users see when they search in Microsoft [SharePoint](https://sharepoint.com/), [Microsoft Office](https://office.com), and Microsoft Search in [Bing](https://bing.com).</span></span> <span data-ttu-id="b4b3f-105">縱向使用者可讓使用者更輕鬆地找到他們具有查看許可權的資訊。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-105">Verticals make it easier for users to find the information that they have permission to see.</span></span> <span data-ttu-id="b4b3f-106">例如，您可以為行銷部門中的使用者建立協力廠商軟體的「行銷分析」資料的搜尋類別。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-106">For example, you could create a search vertical for marketing analysis data from third-party software for your users in the marketing department.</span></span> <span data-ttu-id="b4b3f-107">您也可以定義結果類型及自訂此資料的版面配置。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-107">You can also define result types and customize the layout for this data.</span></span>  

<span data-ttu-id="b4b3f-108">您可以在下列各層級建立縱向和結果類型：</span><span class="sxs-lookup"><span data-stu-id="b4b3f-108">You can create verticals and result types at these levels:</span></span>

- <span data-ttu-id="b4b3f-109">**組織層級**–當使用者從其 [SharePoint](https://sharepoint.com/)開始頁面、 [Office](https://office.com)或 [Bing](https://bing.com)進行搜尋時，會顯示在搜尋結果頁面上的 [組織] 層級。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-109">**Organization level** – When you add a vertical at the organization level, it appears on the search results page when users search from their [SharePoint](https://sharepoint.com/) start page, on [Office](https://office.com), or on [Bing](https://bing.com).</span></span>
- <span data-ttu-id="b4b3f-110">**網站層級**–例如，您可能想要讓客戶服務員工直接從部門的 SharePoint 網站搜尋 *嚴重性 1* 事件。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-110">**Site level** – For example, you might want to enable your customer service employees to search for *Severity 1* incidents directly from their department’s SharePoint site.</span></span>

## <a name="search-verticals-explained"></a><span data-ttu-id="b4b3f-111">說明的搜尋縱向</span><span class="sxs-lookup"><span data-stu-id="b4b3f-111">Search verticals explained</span></span>

<span data-ttu-id="b4b3f-112">在 [Microsoft 搜尋結果] 頁面的頂端，有一列索引標籤。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-112">At the top of the Microsoft Search results page, there's a row of tabs.</span></span> <span data-ttu-id="b4b3f-113">這些是搜尋行業。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-113">These are the search verticals.</span></span> <span data-ttu-id="b4b3f-114">搜尋類別只會顯示特定類型或特定內容的結果。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-114">A search vertical only shows results of a certain type or from certain content.</span></span> <span data-ttu-id="b4b3f-115">例如 **檔** 或 **新聞**。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-115">Examples are **Files** or **News**.</span></span> <span data-ttu-id="b4b3f-116">依預設，Microsoft 搜尋會顯示 **所有** 的縱向、**人員**、**檔案、\*\*\*\*網站** 和 **新聞**。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-116">By default, Microsoft Search shows the verticals **All**, **People**, **Files**, **Sites**, and **News**.</span></span>  

<span data-ttu-id="b4b3f-117">您可以新增與您組織相關的搜尋行業。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-117">You can add search verticals that are relevant to your organization.</span></span> <span data-ttu-id="b4b3f-118">這些會出現在 Microsoft 搜尋結果頁面上[SharePoint](https://sharepoint.com/)、 [Office](https://Office.com)及[Bing](https://bing.com)。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-118">These will appear on the Microsoft Search results page in [SharePoint](https://sharepoint.com/), [Office](https://Office.com), and [Bing](https://bing.com).</span></span> <span data-ttu-id="b4b3f-119">例如，您可以根據每個群組所需的資訊類型，為行銷相關的內容及另一個銷售人員建立垂直。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-119">For example, you could create a vertical for marketing-related content and another for sales, based on the type of information that each group needs.</span></span> <span data-ttu-id="b4b3f-120">您可以新增縱向，只顯示透過連接器編制索引的內容的結果。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-120">You can add verticals to show results only from content indexed via connectors.</span></span>  

### <a name="multiple-connections-in-a-vertical"></a><span data-ttu-id="b4b3f-121">垂直中的多個連接</span><span class="sxs-lookup"><span data-stu-id="b4b3f-121">Multiple connections in a vertical</span></span>

<span data-ttu-id="b4b3f-122">「搜尋類別」現在可以透過多個連接器來源呈現結果。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-122">A search vertical can now surface results from multiple connector sources.</span></span> <span data-ttu-id="b4b3f-123">這為設計搜尋結果頁面提供更大的彈性。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-123">This provides greater flexibility in designing your search result page.</span></span> <span data-ttu-id="b4b3f-124">現有的垂直安裝管理體驗可讓您在「內容來源」步驟中選取多個連接。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-124">The existing administrative experience of vertical setup allows you to select multiple connections in the "Content Source" step.</span></span>
<span data-ttu-id="b4b3f-125">如果您正確指派盡可能多的語義標籤，則會增強這種體驗。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-125">If you accurately appoint as many semantic labels as possible, this experience will be enhanced.</span></span> <span data-ttu-id="b4b3f-126">您可以在架構定義及攝取時新增語義標籤。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-126">You can add semantic labels upon schema definition and ingestion.</span></span>

<span data-ttu-id="b4b3f-127">[以下](configure-connector.md#step-5-assign-property-labels) 是如何建立及管理語義標籤的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-127">[Here](configure-connector.md#step-5-assign-property-labels) is additional information on how to create and manage semantic labels.</span></span>

> [!NOTE]
> <span data-ttu-id="b4b3f-128">垂直中的多個連線目前正在預覽中。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-128">Multiple connections in a vertical is currently in preview.</span></span> <span data-ttu-id="b4b3f-129">如需預覽的詳細資訊，請參閱 [連接器預覽功能](connectors-overview.md#what-are-the-preview-features)。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-129">For more information about preview, see [Connectors preview features](connectors-overview.md#what-are-the-preview-features).</span></span>

### <a name="things-you-should-know"></a><span data-ttu-id="b4b3f-130">您應該知道的事項</span><span class="sxs-lookup"><span data-stu-id="b4b3f-130">Things you should know</span></span>

1. <span data-ttu-id="b4b3f-131">可以將連線新增為一個垂直下方的內容來源。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-131">A connection can be added as a content source only under one vertical.</span></span> <span data-ttu-id="b4b3f-132">不允許重複使用多個行業的連線。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-132">Reusing connections under multiple verticals is not allowed.</span></span>
2. <span data-ttu-id="b4b3f-133">如果您需要為已新增多個連線來源的搜尋類別設定查詢，則應該使用一般來源屬性來建立這類查詢。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-133">If you need to set up a query for a search vertical where multiple connection sources have been added, common source properties should be used to create a such a query.</span></span>

## <a name="things-to-consider"></a><span data-ttu-id="b4b3f-134">考慮事項</span><span class="sxs-lookup"><span data-stu-id="b4b3f-134">Things to consider</span></span>

<span data-ttu-id="b4b3f-135">開始之前，請確定連接器已編制索引。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-135">Before you start, make sure that the connector has been indexed.</span></span> <span data-ttu-id="b4b3f-136">這可能需要最多48小時，視檔案大小而定。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-136">This can take up to 48 hours, depending on the file size.</span></span>

<span data-ttu-id="b4b3f-137">您無法為位於[SharePoint](https://sharepoint.com/)中的內容建立垂直。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-137">You can’t create a vertical for content that resides in [SharePoint](https://sharepoint.com/).</span></span>

<span data-ttu-id="b4b3f-138">新增垂直的三個基本步驟：</span><span class="sxs-lookup"><span data-stu-id="b4b3f-138">There are three basic steps to add a vertical:</span></span>

1. <span data-ttu-id="b4b3f-139">建立垂直。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-139">Create the vertical.</span></span> <span data-ttu-id="b4b3f-140">在這個步驟中，您會定義要搜尋之內容的直排名稱、內容來源及範圍。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-140">In this step, you define the vertical’s name, content source, and scope of the content to search.</span></span>
2. <span data-ttu-id="b4b3f-141">定義此垂直方向的結果外觀。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-141">Define what the results for this vertical will look like.</span></span>  
3. <span data-ttu-id="b4b3f-142">啟用從垂直清單頁面) 顯示的垂直 (。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-142">Enable the vertical (to be displayed) from the vertical list page.</span></span>

## <a name="step-1-create-the-search-vertical"></a><span data-ttu-id="b4b3f-143">步驟1：建立搜尋類別</span><span class="sxs-lookup"><span data-stu-id="b4b3f-143">STEP 1: Create the search vertical</span></span>

<span data-ttu-id="b4b3f-144">啟動該嚮導之後，您會逐步指導您定義要搜尋之內容的垂直名稱、內容來源及範圍。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-144">After you start the wizard, you're guided through the steps to define the vertical's name, content source, and scope of the content to search.</span></span> <span data-ttu-id="b4b3f-145">會以停用狀態建立垂直。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-145">The vertical is created in a disabled state.</span></span> <span data-ttu-id="b4b3f-146">您將在稍後啟用它。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-146">You'll enable it later.</span></span>

<span data-ttu-id="b4b3f-147">您可以使用一組有限的 [關鍵字查詢語言 (KQL) ](/sharepoint/dev/general-development/keyword-query-language-kql-syntax-reference) 來縮小範圍。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-147">You can use a limited set of [Keyword Query Language (KQL)](/sharepoint/dev/general-development/keyword-query-language-kql-syntax-reference) to narrow the scope.</span></span> <span data-ttu-id="b4b3f-148">此頁面列出可用的屬性。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-148">This page lists the properties that are available.</span></span> <span data-ttu-id="b4b3f-149">建議您使用具有 boolean 運算子的任意文字關鍵字和屬性限制，以建立 KQL。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-149">We recommend that you use free-text keywords and property restrictions with boolean operators for creating the KQL.</span></span>
<span data-ttu-id="b4b3f-150">KQL 也支援使用 [設定檔查詢變數](#profile-query-variables) ，在垂直方向微調結果。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-150">KQL also supports the use of [profile query variables](#profile-query-variables) to fine-tune results under the vertical.</span></span>

### <a name="create-a-vertical-at-the-organization-level"></a><span data-ttu-id="b4b3f-151">在組織層級建立垂直</span><span class="sxs-lookup"><span data-stu-id="b4b3f-151">Create a vertical at the organization level</span></span>

<span data-ttu-id="b4b3f-152">若要在[SharePoint](https://sharepoint.com/) home、 [Office](https://office.com)或[Bing](https://bing.com)中的 Microsoft 搜尋上建立垂直的，請遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="b4b3f-152">To create the vertical on Microsoft Search in [SharePoint](https://sharepoint.com/) home, [Office](https://office.com), or [Bing](https://bing.com), follow these steps:</span></span>

1. <span data-ttu-id="b4b3f-153">在 [Microsoft 365 系統管理中心](https://admin.microsoft.com)中，移至 [[**縱向**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/verticals)]。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-153">In the [Microsoft 365 admin center](https://admin.microsoft.com), go to [**Verticals**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/verticals).</span></span>
2. <span data-ttu-id="b4b3f-154">選取 [ **新增** ] 立即開始。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-154">Select **Add** to get started.</span></span>  

### <a name="create-a-vertical-at-the-site-level"></a><span data-ttu-id="b4b3f-155">在網站層級建立垂直</span><span class="sxs-lookup"><span data-stu-id="b4b3f-155">Create a vertical at the site level</span></span>

1. <span data-ttu-id="b4b3f-156">在您要垂直的 [SharePoint](https://sharepoint.com/)網站上，移至 **設定**。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-156">On the [SharePoint](https://sharepoint.com/) site where you want the vertical, go to **Settings**.</span></span>
2. <span data-ttu-id="b4b3f-157">選取 [ **網站資訊** ]，然後 **查看 [所有網站設定**]。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-157">Select **Site information** and then **View all site settings**.</span></span>
3. <span data-ttu-id="b4b3f-158">尋找 [ **Microsoft 搜尋**] 區段，然後 **為此網站集合選取 [設定 Microsoft 搜尋**]。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-158">Look for the **Microsoft Search** section, and then select **Configure Microsoft Search for this site collection**.</span></span>
4. <span data-ttu-id="b4b3f-159">在功能窗格中，移至 [ **自訂經驗**]，然後選取 [ **縱向** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-159">In the navigation pane, go to **Custom experience**, and then select the **Verticals** tab.</span></span>
5. <span data-ttu-id="b4b3f-160">若要新增垂直，請選取 [ **新增**]。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-160">To add a vertical, select **Add**.</span></span>
  <span data-ttu-id="b4b3f-161">或者，若要編輯垂直，請在清單中選取它。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-161">Or, to edit a vertical, select it in the list.</span></span>

<span data-ttu-id="b4b3f-162">請記住，會以停用狀態建立縱向。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-162">Remember, verticals are created in a disabled state.</span></span> <span data-ttu-id="b4b3f-163">您必須先啟用這些功能，使用者才能看到它們。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-163">They must be enabled before users can see them.</span></span>

## <a name="step-2-create-the-result-types"></a><span data-ttu-id="b4b3f-164">步驟2：建立結果類型</span><span class="sxs-lookup"><span data-stu-id="b4b3f-164">STEP 2: Create the result types</span></span>

<span data-ttu-id="b4b3f-165">您可以使用結果類型來設計版面配置，以定義結果在垂直方向上的顯示方式。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-165">You can define how results are displayed in the vertical by designing the layout using result types.</span></span> <span data-ttu-id="b4b3f-166">結果配置可讓您直接在搜尋結果中顯示重要資訊，因此使用者不必選取每個結果，即可查看其是否找到所要尋找的專案。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-166">The result layout lets you show important information directly in the search results, so users don't have to select each result to see if they found what they're looking for.</span></span>

### <a name="default-search-result-layout"></a><span data-ttu-id="b4b3f-167">預設搜尋結果版面配置</span><span class="sxs-lookup"><span data-stu-id="b4b3f-167">Default search result layout</span></span>

<span data-ttu-id="b4b3f-168">如果在設定連接器時， **標籤** 和 **內容** 屬性已正確對應至來源內容，則會針對連接器內容顯示預設的搜尋結果版面配置。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-168">A default search result layout will be shown for Connector content if **labels** and **content** property have been mapped correctly to the source properties at the time of configuring the connector.</span></span> <span data-ttu-id="b4b3f-169">標籤 **標題** 是最重要的標籤。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-169">The label **title** is the most important label.</span></span> <span data-ttu-id="b4b3f-170">**強烈建議** 您指派此標籤的屬性，以使用預設搜尋結果版面配置。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-170">It is **strongly recommended** that you have a property assigned to this label to use default search result layout.</span></span>

### <a name="create-your-own-result-type"></a><span data-ttu-id="b4b3f-171">建立您自己的結果類型</span><span class="sxs-lookup"><span data-stu-id="b4b3f-171">Create your own result type</span></span>

<span data-ttu-id="b4b3f-172">您可以決定建立您自己的搜尋結果版面配置，並透過建立 **結果類型** 來覆寫預設搜尋結果版面配置。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-172">You can decide to create your own search result layout and override the default search result layout by creating a **result type**.</span></span> <span data-ttu-id="b4b3f-173">搜尋結果類型是一種規則，會以不同方式顯示不同類型的搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-173">A search result type is a rule that causes distinct kinds of search results to be displayed in different ways.</span></span> <span data-ttu-id="b4b3f-174">其包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="b4b3f-174">It consists of the following:</span></span>

- <span data-ttu-id="b4b3f-175">**一個或多個** 比較每個搜尋結果的條件，例如搜尋結果的內容來源。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-175">**One or more conditions** to compare each search result against, such as the content source of the search result.</span></span>  
- <span data-ttu-id="b4b3f-176">用於符合條件之搜尋結果的 **結果版面** 配置。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-176">A **result layout** to use for search results that meet the conditions.</span></span> <span data-ttu-id="b4b3f-177">產生的版面配置會控制符合條件的所有結果在搜尋結果頁面上顯示和行為的方式。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-177">The resulting layout controls the way that all results that meet the conditions appear and behave on a search results page.</span></span>

<span data-ttu-id="b4b3f-178">**如果適當的對應無法顯示預設搜尋結果版面配置，您必須至少建立一個結果類型的結果，以顯示在垂直上。**</span><span class="sxs-lookup"><span data-stu-id="b4b3f-178">**If appropriate mapping is not done to show default search result layout, You must create at least one result type for results to display on the vertical.**</span></span> <span data-ttu-id="b4b3f-179">您可以為每個垂直方向建立多種結果類型，這可讓您針對不同類型的結果使用不同的版面配置。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-179">You can create multiple result types for each vertical, which allows you to use different layouts for different type of results.</span></span> <span data-ttu-id="b4b3f-180">例如，您可以自訂 *嚴重性為 1* 的事件，使其具有更醒目的色彩和更大的字型，與 *嚴重的 3* 個事件相較。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-180">For example, you can customize *Severity 1* incidents to have more prominent colors and a larger font compared to *Severity 3* incidents.</span></span>

<span data-ttu-id="b4b3f-181">啟動該嚮導之後，您會逐步指導您定義結果類型的名稱、內容來源及條件。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-181">After you start the wizard, you're guided through the steps to define the name, content source, and conditions for the result type.</span></span> <span data-ttu-id="b4b3f-182">您可以從清單視圖定義結果類型的優先順序。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-182">You can define the priority of the result type from the list view.</span></span>
  
### <a name="create-a-result-type-at-the-organization-level"></a><span data-ttu-id="b4b3f-183">在組織層級建立結果類型</span><span class="sxs-lookup"><span data-stu-id="b4b3f-183">Create a result type at the organization level</span></span>

1. <span data-ttu-id="b4b3f-184">在 [Microsoft 365 系統管理中心](https://admin.microsoft.com)中，移至 [[**結果類型**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/resulttypes)]。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-184">In the [Microsoft 365 admin center](https://admin.microsoft.com), go to [**Result types**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/resulttypes).</span></span>
2. <span data-ttu-id="b4b3f-185">若要新增 **結果類型**，請選取 [ **新增**]。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-185">To add a **Result type**, select **Add**.</span></span> <span data-ttu-id="b4b3f-186">若要編輯結果類型，請選取相關清單中的結果類型。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-186">To edit a result type, select the result type in the relevant list.</span></span>

### <a name="create-a-results-type-at-the-site-level"></a><span data-ttu-id="b4b3f-187">在網站層級建立結果類型</span><span class="sxs-lookup"><span data-stu-id="b4b3f-187">Create a results type at the site level</span></span>

1. <span data-ttu-id="b4b3f-188">在您要建立結果類型的 [SharePoint](https://sharepoint.com/)網站上，移至 **設定**。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-188">On the [SharePoint](https://sharepoint.com/) site where you want to create the result type, go to **Settings**.</span></span>
2. <span data-ttu-id="b4b3f-189">選取 [ **網站資訊** ]，然後 **查看 [所有網站設定**]。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-189">Select **Site information** and then **View all site settings**.</span></span>
3. <span data-ttu-id="b4b3f-190">尋找 [Microsoft 搜尋] 區段，然後 **為此網站集合選取 [設定 Microsoft 搜尋**]。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-190">Look for the Microsoft Search section, and then select **Configure Microsoft Search for this site collection**.</span></span>
4. <span data-ttu-id="b4b3f-191">在功能窗格中，移至 [ **自訂經驗**]，然後選取 [ **結果類型** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-191">In the navigation pane, go to **Custom experience**, and select **Result type** tab.</span></span>
5. <span data-ttu-id="b4b3f-192">若要新增結果類型，請選取 [ **新增**]。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-192">To add a result type, select **Add**.</span></span>  <span data-ttu-id="b4b3f-193">或者，若要編輯結果類型，請選取清單中的結果類型。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-193">Or, to edit a result type, select the result type in the list.</span></span>

## <a name="step-3-view-the-vertical-after-its-enabled"></a><span data-ttu-id="b4b3f-194">步驟3：在啟用垂直後查看</span><span class="sxs-lookup"><span data-stu-id="b4b3f-194">STEP 3: View the vertical after it's enabled</span></span>

<span data-ttu-id="b4b3f-195">在您啟用垂直後，您可以花幾小時的時間，才能進行查看。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-195">After you enable the vertical, it will take a few hours before you can view it.</span></span> <span data-ttu-id="b4b3f-196">如果您不想要等到啟用它之後，您可以在 [SharePoint](https://sharepoint.com/)和 [Office](https://office.com)中將 **cacheClear = true** 新增至 URL，以便立即查看垂直方向。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-196">If you don't want to wait after enabling it, you can append **cacheClear=true** to the URL in [SharePoint](https://sharepoint.com/) and [Office](https://office.com) to view the vertical immediately.</span></span> <span data-ttu-id="b4b3f-197">若為 [Bing](https://bing.com)，請將 **&功能** 新增至工作垂直 URL，以立即查看縱向。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-197">For [Bing](https://bing.com), append **&features=uncachedVerticals** to the Work vertical URL to view the verticals immediately.</span></span>

> [!NOTE]
> <span data-ttu-id="b4b3f-198">從行動網頁瀏覽器中查看時，不會在[SharePoint](https://sharepoint.com/)和[Office](https://office.com)上看到新增的縱向。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-198">Added verticals will not be visible on [SharePoint](https://sharepoint.com/) and [Office](https://office.com) when viewed from mobile web browsers.</span></span>

## <a name="profile-query-variables"></a><span data-ttu-id="b4b3f-199">設定檔查詢變數</span><span class="sxs-lookup"><span data-stu-id="b4b3f-199">Profile query variables</span></span>

<span data-ttu-id="b4b3f-200">查詢變數是用於垂直的 [KQL 查詢] 區段中，以提供動態資料做為垂直查詢的輸入。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-200">Query variables are used in the KQL query section of a vertical to provide dynamic data as an input to the query of a vertical.</span></span> <span data-ttu-id="b4b3f-201">您可以使用設定檔查詢變數，讓搜尋結果成為已登入使用者的上下文。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-201">You can use profile query variables to make the search results contextual to the signed-in user.</span></span> <span data-ttu-id="b4b3f-202">設定檔查詢變數會從已登入使用者的 [設定檔](/graph/api/resources/profile?view=graph-rest-beta)中取得值。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-202">Profile query variables fetch values from the signed-in user’s [profile](/graph/api/resources/profile?view=graph-rest-beta).</span></span>

<span data-ttu-id="b4b3f-203">例如，如果您想要建立「票據」垂直，其中登入的使用者可以搜尋其所指派的支援票證，您可以在 [管理] 頁面的 [查詢] 區段中指定下列查詢。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-203">For example, if you want to create a “Tickets” vertical where a signed-in user can search for support tickets assigned to them, you can specify the following query under the "Query" section during the vertical creation in the administration page.</span></span>  

<span data-ttu-id="b4b3f-204">**AssignedTo： {Profile。 userPrincipalName}**</span><span class="sxs-lookup"><span data-stu-id="b4b3f-204">**AssignedTo:{Profile.accounts.userPrincipalName}**</span></span>

<span data-ttu-id="b4b3f-205">這會縮小搜尋結果，以顯示受託人為執行搜尋之使用者的專案。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-205">This will narrow down the search results to show only those items where the assignee is the user performing the search.</span></span>

<span data-ttu-id="b4b3f-206">[設定檔資源](/graph/api/resources/profile?view=graph-rest-beta) 公開屬性做為集合。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-206">[Profile resource](/graph/api/resources/profile?view=graph-rest-beta) exposes properties as collections.</span></span> <span data-ttu-id="b4b3f-207">例如，電子郵件地址相關的資訊會透過電子郵件集合、工作職位集合等方式公開。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-207">For example, information related to email addresses is exposed through email collection, work positions as positions collection, and so on.</span></span> <span data-ttu-id="b4b3f-208">使用者設定檔中所有可用的屬性，都是以「AAD」為來源類型的方式公開為查詢變數。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-208">All properties available in the user profile, which have AAD as the source type, are exposed as Query variables.</span></span>

<span data-ttu-id="b4b3f-209">請考慮電子郵件集合中有三個可用電子郵件地址的使用者，如下所示。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-209">Consider a user who has 3 email addresses available in the email collection, as shown below.</span></span>

```json
"emails": [{ 

        "address": "Megan.Bowen@contoso.com",
        "id": "xyz", 
        "source": { 
            "CreatedBy": "xyz", 
            "CreatedOn": "2222", 
            "Type": "official" 
        },
        "type": "main" 
    }, { 
        "address": "meganb@hotmail.com",
        "id": "abc", 
        "source": { 
            "CreatedBy": "abc",
            "CreatedOn": "3333", 
            "Type": "non-official",
        },
        "type": "work"
    }, { 
        "address": "meganb@outlook.com",
        "id": "pqr", 
        "source": { 
            "CreatedBy": "pqr", 
            "CreatedOn": "4444", 
            "Type": "personal" 
        },
        "type": "personal" 
    } 
] 
```

- <span data-ttu-id="b4b3f-210">查詢 **MyProperty： {Profile. 電子郵件地址}** 會解析為 MyProperty： "Megan.Bowen@contoso.com"。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-210">The query **MyProperty: {Profile.emails.address}** will resolve to MyProperty: “Megan.Bowen@contoso.com”.</span></span>  

- <span data-ttu-id="b4b3f-211">如果您想要解決 address 屬性的所有值，您必須使用多重值擴充語法。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-211">If you wish to resolve all the values of the address attribute, you have to use the multi-value expansion syntax.</span></span> <span data-ttu-id="b4b3f-212">查詢 **{|MyProperty： {Profile. 電子郵件地址}}** 會解析為 ( (MyProperty： "Megan.Bowen@contoso .com" ) 或 (MyProperty： "meganb@hotmail.com" ) 或 (MyProperty： "meganb@outlook" ) ) </span><span class="sxs-lookup"><span data-stu-id="b4b3f-212">The query **{|MyProperty:{Profile.emails.address}}** will resolve to ((MyProperty:"Megan.Bowen@contoso.com") OR (MyProperty: "meganb@hotmail.com") OR (MyProperty:"meganb@outlook.com"))</span></span>  

<span data-ttu-id="b4b3f-213">"|" 運算子應該用來解析多重值變數。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-213">The “|” operator should be used for resolving multi-value variables.</span></span> <span data-ttu-id="b4b3f-214">如需設定檔擴充的更多範例，請參閱下表。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-214">For more examples on profile expansion refer to the table below.</span></span>

| #         | <span data-ttu-id="b4b3f-215">語法</span><span class="sxs-lookup"><span data-stu-id="b4b3f-215">Syntax</span></span> |  <span data-ttu-id="b4b3f-216">傳回值</span><span class="sxs-lookup"><span data-stu-id="b4b3f-216">Value returned</span></span>  |
| --------- | ------ | --- |
| <span data-ttu-id="b4b3f-217">1 </span><span class="sxs-lookup"><span data-stu-id="b4b3f-217">1</span></span>    | <span data-ttu-id="b4b3f-218">MyProperty： {設定檔. 電子郵件地址}</span><span class="sxs-lookup"><span data-stu-id="b4b3f-218">MyProperty:{Profile.emails.address}</span></span>  |   <span data-ttu-id="b4b3f-219">"Megan.Bowen@contoso.com"</span><span class="sxs-lookup"><span data-stu-id="b4b3f-219">"Megan.Bowen@contoso.com"</span></span>  |
| <span data-ttu-id="b4b3f-220">2 </span><span class="sxs-lookup"><span data-stu-id="b4b3f-220">2</span></span> | <span data-ttu-id="b4b3f-221">MyProperty： {Profile} 電子郵件}</span><span class="sxs-lookup"><span data-stu-id="b4b3f-221">MyProperty:{Profile.emails}</span></span>   |    <span data-ttu-id="b4b3f-222">因為電子郵件是物件，所以 {Profile} 電子郵件} 這不會解決。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-222">{Profile.emails} This will not resolve because emails are an object.</span></span>|
| <span data-ttu-id="b4b3f-223">3 </span><span class="sxs-lookup"><span data-stu-id="b4b3f-223">3</span></span>    | <span data-ttu-id="b4b3f-224">{?MyProperty： {Profile. 電子郵件}}</span><span class="sxs-lookup"><span data-stu-id="b4b3f-224">{?MyProperty:{Profile.emails}}</span></span>  |  <span data-ttu-id="b4b3f-225">這不會解決，因為電子郵件是物件。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-225">This will not resolve because emails is an object.</span></span> <span data-ttu-id="b4b3f-226">"？"</span><span class="sxs-lookup"><span data-stu-id="b4b3f-226">The “?”</span></span> <span data-ttu-id="b4b3f-227">運算子會忽略不會解析的查詢變數。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-227">operator ignores query variables that do not resolve.</span></span> <span data-ttu-id="b4b3f-228">在查詢堆疊上進一步傳遞時，將會移除此變數。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-228">This variable will be removed when passed further down the query stack.</span></span>   |
| <span data-ttu-id="b4b3f-229">4 </span><span class="sxs-lookup"><span data-stu-id="b4b3f-229">4</span></span> | <span data-ttu-id="b4b3f-230">{&#124;MyProperty： {Profile. Type}}</span><span class="sxs-lookup"><span data-stu-id="b4b3f-230">{&#124;MyProperty: {Profile.emails.source.Type}}</span></span>    |  <span data-ttu-id="b4b3f-231"> ( (MyProperty： "官方" ) 或 (MyProperty： "非官方" ) 或 (MyProperty： "personal" ) ) </span><span class="sxs-lookup"><span data-stu-id="b4b3f-231">((MyProperty:"official") OR (MyProperty:"non-official") OR (MyProperty:"personal"))</span></span>    |

> [!NOTE]
>
> - <span data-ttu-id="b4b3f-232">只有使用 [連接器](connectors-overview.md) 做為內容來源的自訂的行業，才支援設定檔查詢變數。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-232">Profile query variables are only supported for custom verticals using a [connector](connectors-overview.md) as a content source.</span></span>
> - <span data-ttu-id="b4b3f-233">設定檔查詢變數是在 [垂直設定處理](customize-search-page.md#step-1-create-the-search-vertical)程式的「查詢」區段中定義。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-233">Profile query variables are defined on the “Query” section of the [vertical set up process](customize-search-page.md#step-1-create-the-search-vertical).</span></span>
> - <span data-ttu-id="b4b3f-234">設定檔查詢變數目前在預覽中。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-234">Profile query variables is currently in preview.</span></span> <span data-ttu-id="b4b3f-235">如需預覽的詳細資訊，請參閱 [連接器預覽功能](connectors-overview.md#what-are-the-preview-features)。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-235">For more information about preview, see [Connectors preview features](connectors-overview.md#what-are-the-preview-features).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="b4b3f-236">疑難排解</span><span class="sxs-lookup"><span data-stu-id="b4b3f-236">Troubleshooting</span></span>

<span data-ttu-id="b4b3f-237">以下是您可能會遇到的常見問題清單，以及修正這些問題的動作。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-237">Here's a list of common issues you might encounter and actions to fix them.</span></span>

|<span data-ttu-id="b4b3f-238">錯誤</span><span class="sxs-lookup"><span data-stu-id="b4b3f-238">Error</span></span>  |<span data-ttu-id="b4b3f-239">動作</span><span class="sxs-lookup"><span data-stu-id="b4b3f-239">Action</span></span>  |
|---------|---------|
| <span data-ttu-id="b4b3f-240">在垂直上看到「發生錯誤」錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-240">I see a "Something went wrong" error message on the vertical.</span></span> | <span data-ttu-id="b4b3f-241">需要有垂直和結果類型，才可完成設定。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-241">Both the vertical and result types are needed to complete the setup.</span></span> <span data-ttu-id="b4b3f-242">請確定您已為相同的內容來源建立這兩者。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-242">Make sure you have created both for the same content source.</span></span> |
| <span data-ttu-id="b4b3f-243">我沒有看到結果版面配置，但我已經建立了它。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-243">I don't see my result layout, although I created one.</span></span> | <span data-ttu-id="b4b3f-244">因為這些設定通常會進行快取，所以需要數分鐘的時間。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-244">It takes a few minutes because these settings are generally cached.</span></span> <span data-ttu-id="b4b3f-245">請等候幾分鐘後再試一次。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-245">Wait for a few minutes and try again.</span></span>        |
| <span data-ttu-id="b4b3f-246">在 [垂直] 或 [結果類型] 頁面上沒有看到任何內容來源。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-246">I don't see any content sources on the vertical or result type page.</span></span> | <span data-ttu-id="b4b3f-247">請確定您已設定連接器和索引的資料。</span><span class="sxs-lookup"><span data-stu-id="b4b3f-247">Make sure you have configured connectors and indexed data.</span></span>   |

## <a name="next-steps"></a><span data-ttu-id="b4b3f-248">後續步驟</span><span class="sxs-lookup"><span data-stu-id="b4b3f-248">Next steps</span></span>

[<span data-ttu-id="b4b3f-249">自訂結果版面配置</span><span class="sxs-lookup"><span data-stu-id="b4b3f-249">Customize the results layout</span></span>](customize-results-layout.md)
