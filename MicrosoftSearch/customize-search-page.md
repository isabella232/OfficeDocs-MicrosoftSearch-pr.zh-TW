---
title: 自訂 Microsoft 搜尋頁面
ms.author: jypal6
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
ms.openlocfilehash: 60ab3423db0a86982df9c4332f0f22267c49dc04
ms.sourcegitcommit: 9ba062f8b632a74e56ad7ec4dffaa1d8dab57614
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/01/2020
ms.locfileid: "44996056"
---
# <a name="customize-the-search-results-page"></a><span data-ttu-id="dffb4-103">自訂搜尋結果頁面</span><span class="sxs-lookup"><span data-stu-id="dffb4-103">Customize the search results page</span></span>

<span data-ttu-id="dffb4-104">您可以建立搜尋類別和結果類型，以自訂使用者在 Microsoft [SharePoint](https://sharepoint.com/)、 [Microsoft Office](https://office.com)和 microsoft search in [Bing](https://bing.com)中搜尋時所看到的搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="dffb4-104">You can create search verticals and result types to customize the search results that users see when they search in Microsoft [SharePoint](https://sharepoint.com/), [Microsoft Office](https://office.com), and Microsoft Search in [Bing](https://bing.com).</span></span> <span data-ttu-id="dffb4-105">縱向使用者可讓使用者更輕鬆地找到他們具有查看許可權的資訊。</span><span class="sxs-lookup"><span data-stu-id="dffb4-105">Verticals make it easier for users to find the information that they have permission to see.</span></span> <span data-ttu-id="dffb4-106">例如，您可以為行銷部門中的使用者建立協力廠商軟體的「行銷分析」資料的搜尋類別。</span><span class="sxs-lookup"><span data-stu-id="dffb4-106">For example, you could create a search vertical for marketing analysis data from third-party software for your users in the marketing department.</span></span> <span data-ttu-id="dffb4-107">您也可以定義結果類型及自訂此資料的版面配置。</span><span class="sxs-lookup"><span data-stu-id="dffb4-107">You can also define result types and customize the layout for this data.</span></span>  

<span data-ttu-id="dffb4-108">您可以在下列各層級建立縱向和結果類型：</span><span class="sxs-lookup"><span data-stu-id="dffb4-108">You can create verticals and result types at these levels:</span></span>

- <span data-ttu-id="dffb4-109">**組織層級**–當您在組織層級新增垂直時，當使用者從他們的[SharePoint](https://sharepoint.com/)開始頁面、 [Office](https://office.com)或[Bing](https://bing.com)進行搜尋時，它會出現在搜尋結果頁面上。</span><span class="sxs-lookup"><span data-stu-id="dffb4-109">**Organization level** – When you add a vertical at the organization level, it appears on the search results page when users search from their [SharePoint](https://sharepoint.com/) start page, on [Office](https://office.com), or on [Bing](https://bing.com).</span></span>
- <span data-ttu-id="dffb4-110">**網站層級**–例如，您可能想要讓客戶服務員工直接從部門的 SharePoint 網站搜尋*嚴重性 1*事件。</span><span class="sxs-lookup"><span data-stu-id="dffb4-110">**Site level** – For example, you might want to enable your customer service employees to search for *Severity 1* incidents directly from their department’s SharePoint site.</span></span>

## <a name="search-verticals-explained"></a><span data-ttu-id="dffb4-111">說明的搜尋縱向</span><span class="sxs-lookup"><span data-stu-id="dffb4-111">Search verticals explained</span></span>

<span data-ttu-id="dffb4-112">在 [Microsoft 搜尋結果] 頁面的頂端有一列索引標籤。</span><span class="sxs-lookup"><span data-stu-id="dffb4-112">At the top of the Microsoft Search results page, there's a row of tabs.</span></span> <span data-ttu-id="dffb4-113">這些是搜尋行業。</span><span class="sxs-lookup"><span data-stu-id="dffb4-113">These are the search verticals.</span></span> <span data-ttu-id="dffb4-114">搜尋類別只會顯示特定類型或特定內容的結果。</span><span class="sxs-lookup"><span data-stu-id="dffb4-114">A search vertical only shows results of a certain type or from certain content.</span></span> <span data-ttu-id="dffb4-115">例如**檔**或**新聞**。</span><span class="sxs-lookup"><span data-stu-id="dffb4-115">Examples are **Files** or **News**.</span></span> <span data-ttu-id="dffb4-116">根據預設，Microsoft 搜尋會顯示縱向**所有**的**人員**、**檔**、**網站**和**新聞**。</span><span class="sxs-lookup"><span data-stu-id="dffb4-116">By default, Microsoft Search shows the verticals **All**, **People**, **Files**, **Sites**, and **News**.</span></span>  

<span data-ttu-id="dffb4-117">您可以新增與您組織相關的搜尋行業。</span><span class="sxs-lookup"><span data-stu-id="dffb4-117">You can add search verticals that are relevant to your organization.</span></span> <span data-ttu-id="dffb4-118">這些會出現在 [ [SharePoint](https://sharepoint.com/)]、[ [Office](https://Office.com)] 及 [ [Bing](https://bing.com)] 的 [Microsoft 搜尋結果] 頁面上。</span><span class="sxs-lookup"><span data-stu-id="dffb4-118">These will appear on the Microsoft Search results page in [SharePoint](https://sharepoint.com/), [Office](https://Office.com), and [Bing](https://bing.com).</span></span> <span data-ttu-id="dffb4-119">例如，您可以根據每個群組所需的資訊類型，為行銷相關的內容及另一個銷售人員建立垂直。</span><span class="sxs-lookup"><span data-stu-id="dffb4-119">For example, you could create a vertical for marketing-related content and another for sales, based on the type of information that each group needs.</span></span> <span data-ttu-id="dffb4-120">您可以新增縱向，只顯示透過連接器編制索引的內容的結果。</span><span class="sxs-lookup"><span data-stu-id="dffb4-120">You can add verticals to show results only from content indexed via connectors.</span></span>  

>[!NOTE]
> <span data-ttu-id="dffb4-121">目前在預覽中的縱向和結果類型是 Microsoft Graph 連接器預覽的一部分。</span><span class="sxs-lookup"><span data-stu-id="dffb4-121">Verticals and result types are currently in preview as a part of the Microsoft Graph connectors preview.</span></span> <span data-ttu-id="dffb4-122">如需預覽的詳細資訊，請參閱[連接器預覽](connectors-preview.md)。</span><span class="sxs-lookup"><span data-stu-id="dffb4-122">For more about the preview, see [Connectors preview](connectors-preview.md).</span></span> <span data-ttu-id="dffb4-123">若要參與預覽，您必須先提交[Microsoft Graph 連接器預覽註冊表單](https://forms.office.com/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbRxWYgu82J_RFnMMATAS6_chUNVYwNU1CMDNZUDBSSDZKWVo2RDJDRjRLQi4u)。</span><span class="sxs-lookup"><span data-stu-id="dffb4-123">To participate in the preview, you must first submit the [Microsoft Graph Connectors Preview Signup form](https://forms.office.com/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbRxWYgu82J_RFnMMATAS6_chUNVYwNU1CMDNZUDBSSDZKWVo2RDJDRjRLQi4u).</span></span>

## <a name="things-to-consider"></a><span data-ttu-id="dffb4-124">考慮事項</span><span class="sxs-lookup"><span data-stu-id="dffb4-124">Things to consider</span></span>

<span data-ttu-id="dffb4-125">開始之前，請確定連接器已編制索引。</span><span class="sxs-lookup"><span data-stu-id="dffb4-125">Before you start, make sure that the connector has been indexed.</span></span> <span data-ttu-id="dffb4-126">這可能需要最多48小時，視檔案大小而定。</span><span class="sxs-lookup"><span data-stu-id="dffb4-126">This can take up to 48 hours, depending on the file size.</span></span>

<span data-ttu-id="dffb4-127">您無法為位於[SharePoint](https://sharepoint.com/)的內容，或從檔案[共用連接器](file-share-connector.md)編制索引的內容建立垂直。</span><span class="sxs-lookup"><span data-stu-id="dffb4-127">You can’t create a vertical for content that resides in [SharePoint](https://sharepoint.com/) or from content that's indexed by the [file share connector](file-share-connector.md).</span></span> <span data-ttu-id="dffb4-128">瞭解如何為[內容編制索引](configure-connector.md)。</span><span class="sxs-lookup"><span data-stu-id="dffb4-128">Learn how to [index content](configure-connector.md).</span></span>

<span data-ttu-id="dffb4-129">新增垂直的三個基本步驟：</span><span class="sxs-lookup"><span data-stu-id="dffb4-129">There are three basic steps to add a vertical:</span></span>

1. <span data-ttu-id="dffb4-130">建立垂直。</span><span class="sxs-lookup"><span data-stu-id="dffb4-130">Create the vertical.</span></span> <span data-ttu-id="dffb4-131">在這個步驟中，您會定義要搜尋之內容的直排名稱、內容來源及範圍。</span><span class="sxs-lookup"><span data-stu-id="dffb4-131">In this step, you define the vertical’s name, content source, and scope of the content to search.</span></span>
2. <span data-ttu-id="dffb4-132">定義此垂直方向的結果外觀。</span><span class="sxs-lookup"><span data-stu-id="dffb4-132">Define what the results for this vertical will look like.</span></span>  
3. <span data-ttu-id="dffb4-133">從垂直清單頁面啟用垂直（顯示）。</span><span class="sxs-lookup"><span data-stu-id="dffb4-133">Enable the vertical (to be displayed) from the vertical list page.</span></span>

## <a name="step-1-create-the-search-vertical"></a><span data-ttu-id="dffb4-134">步驟1：建立搜尋類別</span><span class="sxs-lookup"><span data-stu-id="dffb4-134">STEP 1: Create the search vertical</span></span>

<span data-ttu-id="dffb4-135">啟動該嚮導之後，您會逐步指導您定義要搜尋之內容的垂直名稱、內容來源及範圍。</span><span class="sxs-lookup"><span data-stu-id="dffb4-135">After you start the wizard, you're guided through the steps to define the vertical's name, content source, and scope of the content to search.</span></span> <span data-ttu-id="dffb4-136">會以停用狀態建立垂直。</span><span class="sxs-lookup"><span data-stu-id="dffb4-136">The vertical is created in a disabled state.</span></span> <span data-ttu-id="dffb4-137">您將在稍後啟用它。</span><span class="sxs-lookup"><span data-stu-id="dffb4-137">You'll enable it later.</span></span>

<span data-ttu-id="dffb4-138">您可以使用一組有限的[關鍵字查詢語言（KQL）](https://docs.microsoft.com/sharepoint/dev/general-development/keyword-query-language-kql-syntax-reference)來縮小範圍。</span><span class="sxs-lookup"><span data-stu-id="dffb4-138">You can use a limited set of [Keyword Query Language (KQL)](https://docs.microsoft.com/sharepoint/dev/general-development/keyword-query-language-kql-syntax-reference) to narrow the scope.</span></span> <span data-ttu-id="dffb4-139">此頁面列出可用的屬性。</span><span class="sxs-lookup"><span data-stu-id="dffb4-139">This page lists the properties that are available.</span></span> <span data-ttu-id="dffb4-140">建議您使用 freetext 關鍵字和屬性限制搭配 boolean 運算子來建立 KQL。</span><span class="sxs-lookup"><span data-stu-id="dffb4-140">We recommend that you use freetext keywords and property restrictions with boolean operators for creating the KQL.</span></span>

### <a name="create-a-vertical-at-the-organization-level"></a><span data-ttu-id="dffb4-141">在組織層級建立垂直</span><span class="sxs-lookup"><span data-stu-id="dffb4-141">Create a vertical at the organization level</span></span>

<span data-ttu-id="dffb4-142">若要在[SharePoint](https://sharepoint.com/) Home、 [Office](https://office.com)或[Bing](https://bing.com)中的 Microsoft 搜尋上建立垂直，請遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="dffb4-142">To create the vertical on Microsoft Search in [SharePoint](https://sharepoint.com/) home, [Office](https://office.com), or [Bing](https://bing.com), follow these steps:</span></span>

1. <span data-ttu-id="dffb4-143">在 Microsoft 365 系統 [管理中心](https://admin.microsoft.com)中，移至 **Settings**[   >  **microsoft Search**   >  **自訂**  >  [**縱向**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/verticals)] [設定]。</span><span class="sxs-lookup"><span data-stu-id="dffb4-143">In the Microsoft 365 [admin center](https://admin.microsoft.com), go to **Settings** > **Microsoft Search** > **Customization** > [**Verticals**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/verticals).</span></span>
1. <span data-ttu-id="dffb4-144">選取 [ **新增**] 立即開始。</span><span class="sxs-lookup"><span data-stu-id="dffb4-144">Select **Add** to get started.</span></span>  

### <a name="create-a-vertical-at-the-site-level"></a><span data-ttu-id="dffb4-145">在網站層級建立垂直</span><span class="sxs-lookup"><span data-stu-id="dffb4-145">Create a vertical at the site level</span></span>

1. <span data-ttu-id="dffb4-146">在您要垂直的[SharePoint](https://sharepoint.com/)網站上，移至 [**設定**]。</span><span class="sxs-lookup"><span data-stu-id="dffb4-146">On the [SharePoint](https://sharepoint.com/) site where you want the vertical, go to **Settings**.</span></span>
1. <span data-ttu-id="dffb4-147">選取 [**網站資訊**]，然後**查看 [所有網站設定**]。</span><span class="sxs-lookup"><span data-stu-id="dffb4-147">Select **Site information** and then **View all site settings**.</span></span>
1. <span data-ttu-id="dffb4-148">尋找 [ **Microsoft 搜尋**] 區段，然後選取 [**設定此網站集合的 microsoft search**]。</span><span class="sxs-lookup"><span data-stu-id="dffb4-148">Look for the **Microsoft Search** section, and then select **Configure Microsoft Search for this site collection**.</span></span>
1. <span data-ttu-id="dffb4-149">在功能窗格中，移至 [ **自訂經驗**]，然後選取 [**縱向**] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="dffb4-149">In the navigation pane, go to **Custom experience**, and then select the **Verticals** tab.</span></span>
1. <span data-ttu-id="dffb4-150">若要新增垂直，請選取 [ **新增**]。</span><span class="sxs-lookup"><span data-stu-id="dffb4-150">To add a vertical, select **Add**.</span></span>
  <span data-ttu-id="dffb4-151">或者，若要編輯垂直，請在清單中選取它。</span><span class="sxs-lookup"><span data-stu-id="dffb4-151">Or, to edit a vertical, select it in the list.</span></span>

<span data-ttu-id="dffb4-152">請記住，會以停用狀態建立縱向。</span><span class="sxs-lookup"><span data-stu-id="dffb4-152">Remember, verticals are created in a disabled state.</span></span> <span data-ttu-id="dffb4-153">您必須先啟用這些功能，使用者才能看到它們。</span><span class="sxs-lookup"><span data-stu-id="dffb4-153">They must be enabled before users can see them.</span></span>

## <a name="step-2-create-the-result-types"></a><span data-ttu-id="dffb4-154">步驟2：建立結果類型</span><span class="sxs-lookup"><span data-stu-id="dffb4-154">STEP 2: Create the result types</span></span>

<span data-ttu-id="dffb4-155">您可以使用結果類型來設計版面配置，以定義結果在垂直方向上的顯示方式。</span><span class="sxs-lookup"><span data-stu-id="dffb4-155">You can define how results are displayed in the vertical by designing the layout using result types.</span></span> <span data-ttu-id="dffb4-156">結果配置可讓您直接在搜尋結果中顯示重要資訊，因此使用者不必選取每個結果，即可查看其是否找到所要尋找的專案。</span><span class="sxs-lookup"><span data-stu-id="dffb4-156">The result layout lets you show important information directly in the search results, so users don't have to select each result to see if they found what they're looking for.</span></span>

<span data-ttu-id="dffb4-157">A search result type is a rule that causes distinct kinds of search results to be displayed in different ways.</span><span class="sxs-lookup"><span data-stu-id="dffb4-157">A search result type is a rule that causes distinct kinds of search results to be displayed in different ways.</span></span> <span data-ttu-id="dffb4-158">It consists of the following:</span><span class="sxs-lookup"><span data-stu-id="dffb4-158">It consists of the following:</span></span>

- <span data-ttu-id="dffb4-159">**一個或多個**比較每個搜尋結果的條件，例如搜尋結果的內容來源。</span><span class="sxs-lookup"><span data-stu-id="dffb4-159">**One or more conditions** to compare each search result against, such as the content source of the search result.</span></span>  
- <span data-ttu-id="dffb4-160">用於符合條件之搜尋結果的**結果版面**配置。</span><span class="sxs-lookup"><span data-stu-id="dffb4-160">A **result layout** to use for search results that meet the conditions.</span></span> <span data-ttu-id="dffb4-161">結果版面配置會控制符合條件的所有結果在搜尋結果頁面上顯示和行為的方式。</span><span class="sxs-lookup"><span data-stu-id="dffb4-161">The result layout controls the way that all results that meet the conditions appear and behave on a search results page.</span></span>

<span data-ttu-id="dffb4-162">**您必須建立至少一個結果類型的結果，才會顯示在垂直上。**</span><span class="sxs-lookup"><span data-stu-id="dffb4-162">**You must create at least one result type for results to display on the vertical.**</span></span> <span data-ttu-id="dffb4-163">您可以為每個垂直方向建立多種結果類型，這可讓您針對不同類型的結果使用不同的版面配置。</span><span class="sxs-lookup"><span data-stu-id="dffb4-163">You can create multiple result types for each vertical, which allows you to use different layouts for different type of results.</span></span> <span data-ttu-id="dffb4-164">例如，您可以自訂*嚴重性為 1*的事件，使其具有更醒目的色彩和更大的字型，與*嚴重的 3*個事件相較。</span><span class="sxs-lookup"><span data-stu-id="dffb4-164">For example, you can customize *Severity 1* incidents to have more prominent colors and a larger font compared to *Severity 3* incidents.</span></span>

<span data-ttu-id="dffb4-165">啟動該嚮導之後，您會逐步指導您定義結果類型的名稱、內容來源及條件。</span><span class="sxs-lookup"><span data-stu-id="dffb4-165">After you start the wizard, you're guided through the steps to define the name, content source, and conditions for the result type.</span></span> <span data-ttu-id="dffb4-166">您可以從清單視圖定義結果類型的優先順序。</span><span class="sxs-lookup"><span data-stu-id="dffb4-166">You can define the priority of the result type from the list view.</span></span>
  
### <a name="create-a-result-type-at-the-organization-level"></a><span data-ttu-id="dffb4-167">在組織層級建立結果類型</span><span class="sxs-lookup"><span data-stu-id="dffb4-167">Create a result type at the organization level</span></span>

1. <span data-ttu-id="dffb4-168">在系統[管理中心](https://admin.microsoft.com)中，移至**設定**  >  **Microsoft Search**  >  **自訂**  >  [**結果類型**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/resulttypes)。</span><span class="sxs-lookup"><span data-stu-id="dffb4-168">In the [admin center](https://admin.microsoft.com), go to **Setting** > **Microsoft Search** > **Customizations** > [**Result types**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/resulttypes).</span></span>
1. <span data-ttu-id="dffb4-169">若要新增**結果類型**，請選取 [ **新增**]。</span><span class="sxs-lookup"><span data-stu-id="dffb4-169">To add a **Result type**, select **Add**.</span></span> <span data-ttu-id="dffb4-170">若要編輯結果類型，請選取相關清單中的結果類型。</span><span class="sxs-lookup"><span data-stu-id="dffb4-170">To edit a result type, select the result type in the relevant list.</span></span>

### <a name="create-a-results-type-at-the-site-level"></a><span data-ttu-id="dffb4-171">在網站層級建立結果類型</span><span class="sxs-lookup"><span data-stu-id="dffb4-171">Create a results type at the site level</span></span>

1. <span data-ttu-id="dffb4-172">在您要建立結果類型的[SharePoint](https://sharepoint.com/)網站上，移至 [**設定**]。</span><span class="sxs-lookup"><span data-stu-id="dffb4-172">On the [SharePoint](https://sharepoint.com/) site where you want to create the result type, go to **Settings**.</span></span>
1. <span data-ttu-id="dffb4-173">選取 [**網站資訊**]，然後**查看 [所有網站設定**]。</span><span class="sxs-lookup"><span data-stu-id="dffb4-173">Select **Site information** and then **View all site settings**.</span></span>
1. <span data-ttu-id="dffb4-174">尋找 [Microsoft 搜尋] 區段，然後選取 [**設定此網站集合的 Microsoft search**]。</span><span class="sxs-lookup"><span data-stu-id="dffb4-174">Look for the Microsoft Search section, and then select **Configure Microsoft Search for this site collection**.</span></span>
1. <span data-ttu-id="dffb4-175">在功能窗格中，移至 [ **自訂經驗**]，然後選取 [**結果類型**] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="dffb4-175">In the navigation pane, go to **Custom experience**, and select **Result type** tab.</span></span>
2. <span data-ttu-id="dffb4-176">若要新增結果類型，請選取 [ **新增**]。</span><span class="sxs-lookup"><span data-stu-id="dffb4-176">To add a result type, select **Add**.</span></span>  <span data-ttu-id="dffb4-177">或者，若要編輯結果類型，請選取清單中的結果類型。</span><span class="sxs-lookup"><span data-stu-id="dffb4-177">Or, to edit a result type, select the result type in the list.</span></span>

### <a name="view-the-vertical-after-its-enabled"></a><span data-ttu-id="dffb4-178">啟用垂直後查看</span><span class="sxs-lookup"><span data-stu-id="dffb4-178">View the vertical after it's enabled</span></span>

<span data-ttu-id="dffb4-179">在您啟用垂直後，可能需要一段時間，才能進行查看。</span><span class="sxs-lookup"><span data-stu-id="dffb4-179">After you enable the vertical, it might take a while before you can view it.</span></span> <span data-ttu-id="dffb4-180">如果您不想要等到啟用它之後，您可以在[SharePoint](https://sharepoint.com/)和[Office](https://office.com)的 URL 中附加**cacheClear = true** ，以立即查看垂直。</span><span class="sxs-lookup"><span data-stu-id="dffb4-180">If you don't want to wait after enabling it, you can append **cacheClear=true** to the URL in [SharePoint](https://sharepoint.com/) and [Office](https://office.com) to view the vertical immediately.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="dffb4-181">疑難排解</span><span class="sxs-lookup"><span data-stu-id="dffb4-181">Troubleshooting</span></span>

<span data-ttu-id="dffb4-182">以下是您可能會遇到的常見問題清單，以及修正這些問題的動作。</span><span class="sxs-lookup"><span data-stu-id="dffb4-182">Here's a list of common issues you might encounter and actions to fix them.</span></span>

|<span data-ttu-id="dffb4-183">錯誤</span><span class="sxs-lookup"><span data-stu-id="dffb4-183">Error</span></span>  |<span data-ttu-id="dffb4-184">動作</span><span class="sxs-lookup"><span data-stu-id="dffb4-184">Action</span></span>  |
|---------|---------|
| <span data-ttu-id="dffb4-185">在垂直上看到「發生錯誤」錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="dffb4-185">I see a "Something went wrong" error message on the vertical.</span></span> | <span data-ttu-id="dffb4-186">需要有垂直和結果類型，才可完成設定。</span><span class="sxs-lookup"><span data-stu-id="dffb4-186">Both the vertical and result types are needed to complete the setup.</span></span> <span data-ttu-id="dffb4-187">請確定您已為相同的內容來源建立這兩者。</span><span class="sxs-lookup"><span data-stu-id="dffb4-187">Make sure you have created both for the same content source.</span></span> |
| <span data-ttu-id="dffb4-188">我沒有看到結果版面配置，但我已經建立了它。</span><span class="sxs-lookup"><span data-stu-id="dffb4-188">I don't see my result layout, although I created one.</span></span> | <span data-ttu-id="dffb4-189">因為這些設定通常會進行快取，所以需要數分鐘的時間。</span><span class="sxs-lookup"><span data-stu-id="dffb4-189">It takes a few minutes because these settings are generally cached.</span></span> <span data-ttu-id="dffb4-190">請等候幾分鐘後再試一次。</span><span class="sxs-lookup"><span data-stu-id="dffb4-190">Wait for a few minutes and try again.</span></span>        |
| <span data-ttu-id="dffb4-191">在 [垂直] 或 [結果類型] 頁面上沒有看到任何內容來源。</span><span class="sxs-lookup"><span data-stu-id="dffb4-191">I don't see any content sources on the vertical or result type page.</span></span> | <span data-ttu-id="dffb4-192">請確定您已設定連接器和索引的資料。</span><span class="sxs-lookup"><span data-stu-id="dffb4-192">Make sure you have configured connectors and indexed data.</span></span>   |

## <a name="next-steps"></a><span data-ttu-id="dffb4-193">後續步驟</span><span class="sxs-lookup"><span data-stu-id="dffb4-193">Next steps</span></span>

[<span data-ttu-id="dffb4-194">步驟3：自訂結果版面配置</span><span class="sxs-lookup"><span data-stu-id="dffb4-194">STEP 3: Customize the results layout</span></span>](customize-results-layout.md)
