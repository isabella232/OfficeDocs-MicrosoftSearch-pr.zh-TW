---
title: 管理問與答
ms.author: anfowler
author: adefowler
manager: mnirkhe
ms.date: 05/30/2019
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: 7e3432e6-5317-4d63-90b0-52da6fddd343
description: 個別尋找並更新解答，或使用 Microsoft Search 工具以一次編輯所有項目
ms.openlocfilehash: 8620842e64a40eb32467c42a289bdec3b67d303b
ms.sourcegitcommit: be2e837d9b087bffe6ce40d72d7ae58a8fcdf3fe
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/30/2019
ms.locfileid: "34591519"
---
# <a name="manage-qas"></a><span data-ttu-id="2d789-103">管理問與答</span><span class="sxs-lookup"><span data-stu-id="2d789-103">Manage Q&As</span></span>

<span data-ttu-id="2d789-104">建立問與答的方法與建立書籤類似。</span><span class="sxs-lookup"><span data-stu-id="2d789-104">Creating a Q&A is similar to creating bookmarks.</span></span> <span data-ttu-id="2d789-105">問與答可讓您回應使用者的問題，而不只是提供網頁的連結。</span><span class="sxs-lookup"><span data-stu-id="2d789-105">Q&A allows you to answer the user's question instead of just providing a link to webpage.</span></span> <span data-ttu-id="2d789-106">您可以使用可用的工具，以 RTF 格式編寫答案。</span><span class="sxs-lookup"><span data-stu-id="2d789-106">You can format the answer in rich text using the available tools.</span></span> <span data-ttu-id="2d789-107">如果書籤和問與答共用相同的關鍵字，則會先顯示書籤的結果。</span><span class="sxs-lookup"><span data-stu-id="2d789-107">If a Bookmark and a Q&A share the same keyword, the Bookmark result is shown first.</span></span> <span data-ttu-id="2d789-108">如同書籤，問與答索引會在新增或變更問與答後立即重新整理。</span><span class="sxs-lookup"><span data-stu-id="2d789-108">Like Bookmarks, the Q&A index is refreshed immediately after a Q&A is added or changed.</span></span> 

## <a name="add-or-edit-a-single-qa"></a><span data-ttu-id="2d789-109">新增或編輯單一問與答</span><span class="sxs-lookup"><span data-stu-id="2d789-109">Add or edit a single Q&A</span></span>
1. <span data-ttu-id="2d789-110">移至 **Microsoft 365 系統管理中心**。</span><span class="sxs-lookup"><span data-stu-id="2d789-110">Go to the Microsoft 365 admin center.</span></span>
1. <span data-ttu-id="2d789-111">在功能窗格中，移至 [設定]\*\*\*\*，然後選取 **Microsoft Search**。</span><span class="sxs-lookup"><span data-stu-id="2d789-111">In the navigation pane, go to **Settings** and select **Microsoft Search**.</span></span>
1. <span data-ttu-id="2d789-112">選取 [問與答]\*\*\*\* 索引標籤。預設會選取第一個索引標籤 ([書籤]\*\*\*\*)。</span><span class="sxs-lookup"><span data-stu-id="2d789-112">Select **Q&A** tab. By default, the first tab (**Bookmarks**) is selected.</span></span>
1. <span data-ttu-id="2d789-113">若要新增問與答，請選取 [新增]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="2d789-113">To add a Q&A, select **Add new**.</span></span>
<span data-ttu-id="2d789-114">若要編輯問與答，請在相關的問與答清單中選取問與答。</span><span class="sxs-lookup"><span data-stu-id="2d789-114">To edit a Q&A, select the Q&A in the relevant Q&A list.</span></span>
1. <span data-ttu-id="2d789-115">當您新增或編輯資訊時，預覽會自動更新。</span><span class="sxs-lookup"><span data-stu-id="2d789-115">As you add or edit the information, the preview automatically updates.</span></span>
1. <span data-ttu-id="2d789-116">儲存變更。</span><span class="sxs-lookup"><span data-stu-id="2d789-116">Save your changes.</span></span>

### <a name="supported-html-tags"></a><span data-ttu-id="2d789-117">支援的 HTML 標記</span><span class="sxs-lookup"><span data-stu-id="2d789-117">Supported HTML tags</span></span>
<span data-ttu-id="2d789-118">您可以使用現有的 HTML 內容或新增 HTML 標記至您的解答 (描述)。</span><span class="sxs-lookup"><span data-stu-id="2d789-118">You can use existing HTML content or add HTML tags to your answer (description).</span></span> <span data-ttu-id="2d789-119">會忽略不支援的標籤。</span><span class="sxs-lookup"><span data-stu-id="2d789-119">Unsupported tags are ignored.</span></span>  
<span data-ttu-id="2d789-120">支援下列的 HTML 標記：</span><span class="sxs-lookup"><span data-stu-id="2d789-120">The following HTML tags are supported:</span></span>
- <span data-ttu-id="2d789-121">blockquote</span><span class="sxs-lookup"><span data-stu-id="2d789-121">blockquote</span></span>
- <span data-ttu-id="2d789-122">div</span><span class="sxs-lookup"><span data-stu-id="2d789-122">div</span></span>
- <span data-ttu-id="2d789-123">em</span><span class="sxs-lookup"><span data-stu-id="2d789-123">eminute, em.</span></span>
- <span data-ttu-id="2d789-124">h1、h2、h3 和 h4</span><span class="sxs-lookup"><span data-stu-id="2d789-124">h1, h2, h3, and h4</span></span>
- <span data-ttu-id="2d789-125">ol、ul 和 li</span><span class="sxs-lookup"><span data-stu-id="2d789-125">ol, ul, and li</span></span>
- <span data-ttu-id="2d789-126">p</span><span class="sxs-lookup"><span data-stu-id="2d789-126">p</span></span>
- <span data-ttu-id="2d789-127">pre</span><span class="sxs-lookup"><span data-stu-id="2d789-127">Scr pre.</span></span>
- <span data-ttu-id="2d789-128">span</span><span class="sxs-lookup"><span data-stu-id="2d789-128">Span</span></span>
- <span data-ttu-id="2d789-129">strong</span><span class="sxs-lookup"><span data-stu-id="2d789-129">Strong.</span></span>
- <span data-ttu-id="2d789-130">table、thead、tbody、tr、th 和 td</span><span class="sxs-lookup"><span data-stu-id="2d789-130">table, thead, tbody, tr, th, and td</span></span>
- <span data-ttu-id="2d789-131">u</span><span class="sxs-lookup"><span data-stu-id="2d789-131">u</span></span>
- <span data-ttu-id="2d789-132">a</span><span class="sxs-lookup"><span data-stu-id="2d789-132">a</span></span>
- <span data-ttu-id="2d789-133">code</span><span class="sxs-lookup"><span data-stu-id="2d789-133">code</span></span>
- <span data-ttu-id="2d789-134">br</span><span class="sxs-lookup"><span data-stu-id="2d789-134">br</span></span>
- <span data-ttu-id="2d789-135">hr</span><span class="sxs-lookup"><span data-stu-id="2d789-135">hr</span></span>
- <span data-ttu-id="2d789-136">img</span><span class="sxs-lookup"><span data-stu-id="2d789-136">img</span></span>

## <a name="bulk-add-or-edit-qas"></a><span data-ttu-id="2d789-137">大量新增或編輯問與答</span><span class="sxs-lookup"><span data-stu-id="2d789-137">Bulk add or edit Q&As</span></span>
<span data-ttu-id="2d789-138">系統管理員可以使用匯入和匯出功能來大量建立或編輯問與答。</span><span class="sxs-lookup"><span data-stu-id="2d789-138">Administrators can use the Import and Export features to bulk create or edit Q&A.</span></span> <span data-ttu-id="2d789-139">當系統管理員需要新增或編輯大量問與答時，此功能很實用。</span><span class="sxs-lookup"><span data-stu-id="2d789-139">This is a useful feature when administrators need to add or edit a large number of Q&A.</span></span> 

<span data-ttu-id="2d789-140">使用匯入/匯出功能，以便：</span><span class="sxs-lookup"><span data-stu-id="2d789-140">Use the import/export feature to:</span></span>
1. <span data-ttu-id="2d789-141">大量新增問與答 - 在問與答範本檔案中新增詳細資料，然後將它匯入。</span><span class="sxs-lookup"><span data-stu-id="2d789-141">Bulk add Q&A - Add details in the Q&A template file, and then import it.</span></span>
1. <span data-ttu-id="2d789-142">大量編輯問與答 - 將問與答匯出至 .csv 檔案，然後編輯匯出的 .csv 檔案中問與答的詳細資料，然後匯入該 .csv 檔案。</span><span class="sxs-lookup"><span data-stu-id="2d789-142">Bulk edit Q&A - Export Q&A to a .csv file, then edit the Q&A details in the exported .csv file, and then import the .csv file.</span></span>
1. <span data-ttu-id="2d789-143">備份問與答 - 匯出問與答至 .csv 檔案。</span><span class="sxs-lookup"><span data-stu-id="2d789-143">Backup Q&A - Export Q&A to a .csv file.</span></span>

<span data-ttu-id="2d789-144">若要匯入或匯出問與答：</span><span class="sxs-lookup"><span data-stu-id="2d789-144">To import or export Q&A:</span></span>
1. <span data-ttu-id="2d789-145">在 [問與答] 索引標籤的右上角，選取 [匯入]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="2d789-145">In the upper-right corner of the Q&A tab, select **Import**.</span></span> <span data-ttu-id="2d789-146">選取 [匯出]\*\*\*\* 來下載 .csv 檔案中所有的現有問與答。</span><span class="sxs-lookup"><span data-stu-id="2d789-146">Select **Export** to download all the existing Q&A in a .csv file.</span></span>
1. <span data-ttu-id="2d789-147">在右窗格中，選擇使用 .csv 檔案匯入的選項。</span><span class="sxs-lookup"><span data-stu-id="2d789-147">In the right pane, choose the option to import using a .csv file.</span></span>
<span data-ttu-id="2d789-148">下載範本檔案以取得必要欄位的清單和詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2d789-148">Download the template file for a list of the required fields and details.</span></span> 
1. <span data-ttu-id="2d789-149">在範本檔案中新增或編輯問與答詳細資料，並將它儲存在您的電腦上。</span><span class="sxs-lookup"><span data-stu-id="2d789-149">Add or edit Q&A details in the template file and save it on your computer.</span></span> 
1. <span data-ttu-id="2d789-150">在 [匯入問與答]\*\*\*\* 窗格中，選取 [瀏覽]\*\*\*\*，然後選取您要匯入的 .csv 檔案。</span><span class="sxs-lookup"><span data-stu-id="2d789-150">In the **Import Q&A** pane, select **Browse**, and then the .csv file that you want to import.</span></span>
1. <span data-ttu-id="2d789-151">選取 [匯入]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="2d789-151">Select **Import**.</span></span>

<span data-ttu-id="2d789-152">以下是有關範本檔案的一些重點：</span><span class="sxs-lookup"><span data-stu-id="2d789-152">Here are some important points regarding the template file:</span></span>
- <span data-ttu-id="2d789-153">永不編輯這些欄位中的資料：*識別碼*、*上次修改日期*，以及*上次修改者*</span><span class="sxs-lookup"><span data-stu-id="2d789-153">Never edit data in these fields: *Id*, *Last Modified*, and *Last Modified By*</span></span>
- <span data-ttu-id="2d789-154">如果您包含現有書籤的*識別碼*，將會以匯入檔案中的資訊加以取代。</span><span class="sxs-lookup"><span data-stu-id="2d789-154">If you include the *Id* of an existing bookmark, it will be replaced with the information in the import file.</span></span>
- <span data-ttu-id="2d789-155">如果有一個現有的書籤具有相同標題或 URL，則會以匯入檔案中的資訊更新書籤。</span><span class="sxs-lookup"><span data-stu-id="2d789-155">If there is an existing bookmark with the same title or URL, the bookmark will be updated with information in the import file.</span></span>
- <span data-ttu-id="2d789-156">範本檔案中並非所有欄位都為必要，必要欄位則會依據書籤的狀態而改變。</span><span class="sxs-lookup"><span data-stu-id="2d789-156">Not all fields in the template file are required and required fields vary depending on the bookmark state.</span></span>
- <span data-ttu-id="2d789-157">書籤會根據狀態欄位的不同而儲存成草稿、建議、已排程或自動發佈。</span><span class="sxs-lookup"><span data-stu-id="2d789-157">Based on the State field, bookmarks will be saved as draft, suggested, scheduled, or they will be published automatically.</span></span>
- <span data-ttu-id="2d789-158">針對具有多個租用戶的組織，您可以從一個租用戶匯出您的書籤，並將它匯入到另一個租用戶。</span><span class="sxs-lookup"><span data-stu-id="2d789-158">For organizations with multiple tenants, you can export your bookmarks from one tenant and import it into another.</span></span> <span data-ttu-id="2d789-159">但您必須在匯入之前，先移除 [識別碼]\*\* 資料行中的資料。</span><span class="sxs-lookup"><span data-stu-id="2d789-159">But you must remove the data in the *Id* column before you import.</span></span>

<span data-ttu-id="2d789-160">**附註：** 如果範本檔案中有任何錯誤，您即無法匯入問與答。</span><span class="sxs-lookup"><span data-stu-id="2d789-160">**Note:** You cannot import Q&A if there are any errors in the template file.</span></span> <span data-ttu-id="2d789-161">若要避免錯誤，請確定您匯入的檔案的格式正確，並包含所有必要的資訊。</span><span class="sxs-lookup"><span data-stu-id="2d789-161">To prevent errors, make sure your import file is properly formatted and include all the required information.</span></span> 

<span data-ttu-id="2d789-162">如需如何避免錯誤的詳細資訊，請參閱[防止匯入錯誤](manage-bookmarks.md#prevent-import-errors)。</span><span class="sxs-lookup"><span data-stu-id="2d789-162">For more information on how to prevent error, see [Prevent import errors](manage-bookmarks.md#prevent-import-errors).</span></span>