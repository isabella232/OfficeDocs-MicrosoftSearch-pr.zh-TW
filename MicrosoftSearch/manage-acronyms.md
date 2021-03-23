---
title: 在 Microsoft 搜尋中管理縮寫詞答案
ms.author: rakkum
author: rakeshMSFT
manager: jeffkizn
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 在 Microsoft 搜尋中建立及更新縮寫的答案
ms.openlocfilehash: 5677ff6915c9e43e2559964c40086cb360a05db7
ms.sourcegitcommit: 5df252e6d0bd67bb1b4c59418aceca8369f5fe42
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/23/2021
ms.locfileid: "51031366"
---
# <a name="manage-acronyms-answers-in-microsoft-search"></a><span data-ttu-id="e7127-103">管理 Microsoft 搜尋中的縮寫詞答案</span><span class="sxs-lookup"><span data-stu-id="e7127-103">Manage Acronyms answers in Microsoft Search</span></span>

<span data-ttu-id="e7127-104">使用者通常會在組織或小組所用的不熟悉縮寫和縮寫中執行。</span><span class="sxs-lookup"><span data-stu-id="e7127-104">Users often run into unfamiliar acronyms and abbreviations used by their organization or team.</span></span> <span data-ttu-id="e7127-105">組織或小組特有的條款，對從一個小組移至另一個小組的人員來說可能是新的，可與內部協力廠商小組共同作業，或是組織的新功能。</span><span class="sxs-lookup"><span data-stu-id="e7127-105">Terms that are specific to organizations or teams might be new to people who move from one team to another, work with internal partner teams, or are new to the organization.</span></span>

<span data-ttu-id="e7127-106">組織不一定會有單一參考的標準術語。</span><span class="sxs-lookup"><span data-stu-id="e7127-106">Organizations don't always have a single reference for their standard terminology.</span></span> <span data-ttu-id="e7127-107">缺乏單一參考會使您很難尋找這些縮寫詞的定義或擴充。</span><span class="sxs-lookup"><span data-stu-id="e7127-107">Lack of a single reference makes it hard to find definitions or expansions for these acronyms.</span></span> <span data-ttu-id="e7127-108">Microsoft 搜尋會解決與首字的問題。</span><span class="sxs-lookup"><span data-stu-id="e7127-108">Microsoft Search solves that problem with Acronyms.</span></span>

## <a name="what-users-experience"></a><span data-ttu-id="e7127-109">使用者經驗</span><span class="sxs-lookup"><span data-stu-id="e7127-109">What users experience</span></span>

<span data-ttu-id="e7127-110">Microsoft Search 使用者可以在 [Bing](https://Bing.com)、 [SharePoint](https://products.office.com/sharepoint/collaboration)和 [Office 365](https://Office.com)中取得具有縮寫的定義。</span><span class="sxs-lookup"><span data-stu-id="e7127-110">Microsoft Search users can get definitions with Acronyms in [Bing](https://Bing.com), [SharePoint](https://products.office.com/sharepoint/collaboration), and [Office 365](https://Office.com).</span></span> <span data-ttu-id="e7127-111">在 [ **搜尋** ] 方塊中，使用者輸入如下範例的查詢：</span><span class="sxs-lookup"><span data-stu-id="e7127-111">In the **Search** box, users enter queries like these examples:</span></span>

- <span data-ttu-id="e7127-112">*何謂* DNN</span><span class="sxs-lookup"><span data-stu-id="e7127-112">*What is* DNN</span></span>
- <span data-ttu-id="e7127-113">*定義* DNN</span><span class="sxs-lookup"><span data-stu-id="e7127-113">*Define* DNN</span></span>
- <span data-ttu-id="e7127-114">DNN *定義*</span><span class="sxs-lookup"><span data-stu-id="e7127-114">DNN *definition*</span></span>
- <span data-ttu-id="e7127-115">*展開* DNN</span><span class="sxs-lookup"><span data-stu-id="e7127-115">*Expand* DNN</span></span>
- <span data-ttu-id="e7127-116">DNN *擴充*</span><span class="sxs-lookup"><span data-stu-id="e7127-116">DNN *expansion*</span></span>
- <span data-ttu-id="e7127-117">*的意義* DNN</span><span class="sxs-lookup"><span data-stu-id="e7127-117">*Meaning of* DNN</span></span>
- <span data-ttu-id="e7127-118">DNN *表示*</span><span class="sxs-lookup"><span data-stu-id="e7127-118">DNN *means*</span></span>

<span data-ttu-id="e7127-119">結果會包含使用者組織中所顯示之 DNN 的所有意義。</span><span class="sxs-lookup"><span data-stu-id="e7127-119">The result includes all the meanings of DNN that are present within the user’s organization.</span></span>

> [!NOTE]
> <span data-ttu-id="e7127-120">使用者必須輸入包含縮寫詞所指定 *關鍵字* 的查詢，以觸發其對應的答案。</span><span class="sxs-lookup"><span data-stu-id="e7127-120">Users must enter a query that includes the acronym’s specified *keywords* to trigger its corresponding answers.</span></span> <span data-ttu-id="e7127-121">縮寫詞查詢不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="e7127-121">Acronym queries are not case sensitive.</span></span>

## <a name="set-up-acronyms-answers"></a><span data-ttu-id="e7127-122">設定縮寫詞答案</span><span class="sxs-lookup"><span data-stu-id="e7127-122">Set up acronyms answers</span></span>

<span data-ttu-id="e7127-123">在 [Microsoft 365 系統管理中心](https://admin.microsoft.com)中，移至 [ [**縮寫**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms)]，然後選取 [ **新增縮寫**]。</span><span class="sxs-lookup"><span data-stu-id="e7127-123">In the [Microsoft 365 admin center](https://admin.microsoft.com), go to [**Acronyms**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms), and then select **Add acronym**.</span></span>

<span data-ttu-id="e7127-124">Microsoft 搜尋會查詢兩個數據源，以提供使用者搜尋的縮寫答案：</span><span class="sxs-lookup"><span data-stu-id="e7127-124">Microsoft Search queries two data sources to provide Acronyms answers to users’ searches:</span></span>

1. <span data-ttu-id="e7127-125">**Admin-策劃**。</span><span class="sxs-lookup"><span data-stu-id="e7127-125">**Admin-curated**.</span></span> <span data-ttu-id="e7127-126">由系統管理員在系統管理員 [中央](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms)提供。</span><span class="sxs-lookup"><span data-stu-id="e7127-126">Provided by IT administrators in the [admin center](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms).</span></span>
2. <span data-ttu-id="e7127-127">**System-策劃**。</span><span class="sxs-lookup"><span data-stu-id="e7127-127">**System-curated**.</span></span> <span data-ttu-id="e7127-128">由 Microsoft 搜尋從使用者的電子郵件和檔，以及組織內可公開使用的資料所探索。</span><span class="sxs-lookup"><span data-stu-id="e7127-128">Discovered by Microsoft Search from users' email and documents and publicly available data within the organization.</span></span>

### <a name="set-up-admin-curated-acronyms"></a><span data-ttu-id="e7127-129">設定系統管理員-策劃縮寫</span><span class="sxs-lookup"><span data-stu-id="e7127-129">Set up Admin-curated acronyms</span></span>

<span data-ttu-id="e7127-130">搜尋管理員可以在[Microsoft 搜尋系統管理中心](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch)的 [[縮寫]](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms)索引標籤上新增縮寫。</span><span class="sxs-lookup"><span data-stu-id="e7127-130">Search administrators can add acronyms on the [Acronyms tab](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms) in the  [Microsoft Search admin center](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch).</span></span> <span data-ttu-id="e7127-131">您可以從任何內部網站或存放庫向系統管理中心新增縮寫。</span><span class="sxs-lookup"><span data-stu-id="e7127-131">You can add acronyms from any internal site or repository to the admin center.</span></span> <span data-ttu-id="e7127-132">您可以將這些縮寫詞新增至 **已發佈** 或 **草稿** 的狀態：</span><span class="sxs-lookup"><span data-stu-id="e7127-132">These acronyms can be added to **Published** or **Draft** state:</span></span>

<span data-ttu-id="e7127-133">**發行狀態**。</span><span class="sxs-lookup"><span data-stu-id="e7127-133">**Published state**.</span></span> <span data-ttu-id="e7127-134">組織中的使用者可以透過 Microsoft 搜尋取得縮寫。</span><span class="sxs-lookup"><span data-stu-id="e7127-134">Acronyms are available to the organization’s users through Microsoft Search.</span></span>

> [!NOTE]
> <span data-ttu-id="e7127-135">最多可能需要三天的縮寫，以在 Microsoft 搜尋中加入已發佈的狀態。</span><span class="sxs-lookup"><span data-stu-id="e7127-135">It might take up to three days for acronyms added to Published state to become available in Microsoft Search.</span></span>

<span data-ttu-id="e7127-136">**草稿狀態**。</span><span class="sxs-lookup"><span data-stu-id="e7127-136">**Draft state**.</span></span> <span data-ttu-id="e7127-137">如果您想要在 Microsoft 搜尋中使用首字縮寫，您可以新增草稿狀態的縮寫。</span><span class="sxs-lookup"><span data-stu-id="e7127-137">If you want to review an acronym before making it available in Microsoft Search, you can add the acronym in a Draft state.</span></span> <span data-ttu-id="e7127-138">草稿狀態中的縮寫不會出現在搜尋結果中。</span><span class="sxs-lookup"><span data-stu-id="e7127-138">Acronyms in the Draft state will not appear in search results.</span></span> <span data-ttu-id="e7127-139">您必須將縮寫詞移至發佈的狀態，使其顯示在搜尋結果中。</span><span class="sxs-lookup"><span data-stu-id="e7127-139">You will need to move the acronym to the Published state to make it appear in search results.</span></span>

<span data-ttu-id="e7127-140">您可以在 CSV 檔案中個別加入縮寫或大容量匯入。</span><span class="sxs-lookup"><span data-stu-id="e7127-140">You can add acronyms individually or bulk import them in a CSV file.</span></span> <span data-ttu-id="e7127-141">使用下表所示的欄位上載 CSV 檔案：</span><span class="sxs-lookup"><span data-stu-id="e7127-141">Upload a CSV file with the fields shown in the following table:</span></span>

| <span data-ttu-id="e7127-142">縮寫 (強制) </span><span class="sxs-lookup"><span data-stu-id="e7127-142">Acronym (Mandatory)</span></span> | <span data-ttu-id="e7127-143">擴充 (強制) </span><span class="sxs-lookup"><span data-stu-id="e7127-143">Expansion (Mandatory)</span></span> | <span data-ttu-id="e7127-144">URL</span><span class="sxs-lookup"><span data-stu-id="e7127-144">Url</span></span> | <span data-ttu-id="e7127-145">描述</span><span class="sxs-lookup"><span data-stu-id="e7127-145">Description</span></span>  | <span data-ttu-id="e7127-146">狀態 (強制) </span><span class="sxs-lookup"><span data-stu-id="e7127-146">State (Mandatory)</span></span> | <span data-ttu-id="e7127-147">上次修改日期</span><span class="sxs-lookup"><span data-stu-id="e7127-147">Last Modified</span></span> | <span data-ttu-id="e7127-148">上次修改者</span><span class="sxs-lookup"><span data-stu-id="e7127-148">Last Modified By</span></span> | <span data-ttu-id="e7127-149">識別碼</span><span class="sxs-lookup"><span data-stu-id="e7127-149">Id</span></span> |
| --------- | --------- | --------- | ---------- | --------- |--------- |--------- |--------- |
| <span data-ttu-id="e7127-150">*Xxx*</span><span class="sxs-lookup"><span data-stu-id="e7127-150">*XXX*</span></span> | <span data-ttu-id="e7127-151">*拼寫縮寫*</span><span class="sxs-lookup"><span data-stu-id="e7127-151">*Spelled out abbreviation*</span></span> | <span data-ttu-id="e7127-152">*Source*</span><span class="sxs-lookup"><span data-stu-id="e7127-152">*Source*</span></span> |  | <span data-ttu-id="e7127-153">*已發佈或草稿*</span><span class="sxs-lookup"><span data-stu-id="e7127-153">*Published or Draft*</span></span> |  |  |  |

### <a name="csv-fields"></a><span data-ttu-id="e7127-154">CSV 欄位</span><span class="sxs-lookup"><span data-stu-id="e7127-154">CSV fields</span></span>

<span data-ttu-id="e7127-155">**縮寫**。</span><span class="sxs-lookup"><span data-stu-id="e7127-155">**Acronym**.</span></span> <span data-ttu-id="e7127-156">包含實際的簡寫形式或縮寫。</span><span class="sxs-lookup"><span data-stu-id="e7127-156">Contains the actual short form or acronym.</span></span> <span data-ttu-id="e7127-157">例如， *DNN*。</span><span class="sxs-lookup"><span data-stu-id="e7127-157">An example is *DNN*.</span></span>

<span data-ttu-id="e7127-158">**擴充**。</span><span class="sxs-lookup"><span data-stu-id="e7127-158">**Expansion**.</span></span> <span data-ttu-id="e7127-159">包含縮寫的擴充。</span><span class="sxs-lookup"><span data-stu-id="e7127-159">Contains the expansion of the acronym.</span></span> <span data-ttu-id="e7127-160">例如， *Deep 神經網路*。</span><span class="sxs-lookup"><span data-stu-id="e7127-160">An example is *Deep Neural Network*.</span></span>

<span data-ttu-id="e7127-161">**描述**。</span><span class="sxs-lookup"><span data-stu-id="e7127-161">**Description**.</span></span> <span data-ttu-id="e7127-162">縮寫的簡短描述，可提供使用者更多有關縮寫和其擴充的資訊。</span><span class="sxs-lookup"><span data-stu-id="e7127-162">A brief description of the acronym that gives users more info about the acronym and its expansion.</span></span> <span data-ttu-id="e7127-163">例如， *deep 神經網路是具有某一層級複雜性的神經網路，具有超過兩層的神經網路*。</span><span class="sxs-lookup"><span data-stu-id="e7127-163">For example, *A deep neural network is a neural network with a certain level of complexity, a neural network with more than two layers*.</span></span>

<span data-ttu-id="e7127-164">**來源**。</span><span class="sxs-lookup"><span data-stu-id="e7127-164">**Source**.</span></span> <span data-ttu-id="e7127-165">您要讓使用者流覽的頁面或網站 URL，以取得有關縮寫的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="e7127-165">The URL of the page or website where you want users to go for more information about the acronym.</span></span>

<span data-ttu-id="e7127-166">**狀態**。</span><span class="sxs-lookup"><span data-stu-id="e7127-166">**State**.</span></span> <span data-ttu-id="e7127-167">此欄位可以採用兩個值：</span><span class="sxs-lookup"><span data-stu-id="e7127-167">This field can take two values:</span></span>

- <span data-ttu-id="e7127-168">**草稿**。</span><span class="sxs-lookup"><span data-stu-id="e7127-168">**Draft**.</span></span> <span data-ttu-id="e7127-169">將縮寫新增至草稿狀態。</span><span class="sxs-lookup"><span data-stu-id="e7127-169">Adds  the acronym to the Draft state.</span></span>
- <span data-ttu-id="e7127-170">**發行**。</span><span class="sxs-lookup"><span data-stu-id="e7127-170">**Published**.</span></span> <span data-ttu-id="e7127-171">將縮寫新增至發佈的狀態，並使其可用於 Microsoft 搜尋。</span><span class="sxs-lookup"><span data-stu-id="e7127-171">Adds the acronym to the Published state and makes it available in Microsoft Search.</span></span>

### <a name="system-curated-acronyms"></a><span data-ttu-id="e7127-172">系統策劃縮寫</span><span class="sxs-lookup"><span data-stu-id="e7127-172">System-curated acronyms</span></span>

<span data-ttu-id="e7127-173">將組織內使用的所有縮寫詞新增至答案可能是一項挑戰。</span><span class="sxs-lookup"><span data-stu-id="e7127-173">It might be a challenge for admins to add all the acronyms used within an organization to Answers.</span></span> <span data-ttu-id="e7127-174">這項功能可找出搜尋系統管理員甚至不會察覺的縮寫。</span><span class="sxs-lookup"><span data-stu-id="e7127-174">This feature can find acronyms that search administrators aren’t even aware of.</span></span> <span data-ttu-id="e7127-175">若要執行這項操作，Microsoft 搜尋還會從這些來源探索並 curates 縮寫：</span><span class="sxs-lookup"><span data-stu-id="e7127-175">To do that work, Microsoft Search also discovers and curates acronyms from these sources:</span></span>

- <span data-ttu-id="e7127-176">使用者的電子郵件</span><span class="sxs-lookup"><span data-stu-id="e7127-176">Users’ emails</span></span>
- <span data-ttu-id="e7127-177">[SharePoint](https://products.office.com/sharepoint/collaboration)、 [Microsoft OneDrive]( https://onedrive.live.com/about/)和[microsoft OneNote](https://www.onenote.com/)中的檔</span><span class="sxs-lookup"><span data-stu-id="e7127-177">Documents in [SharePoint](https://products.office.com/sharepoint/collaboration), [Microsoft OneDrive]( https://onedrive.live.com/about/), and [Microsoft OneNote](https://www.onenote.com/)</span></span>
- <span data-ttu-id="e7127-178">組織內使用者可以存取的公用檔 SharePoint、OneDrive 或 OneNote</span><span class="sxs-lookup"><span data-stu-id="e7127-178">Public documents within the organization that users have access to in SharePoint, OneDrive, or OneNote</span></span>

<span data-ttu-id="e7127-179">Microsoft 搜尋可確保只有對檔具有存取權和許可權的使用者才能看到其所探索的縮寫。</span><span class="sxs-lookup"><span data-stu-id="e7127-179">Microsoft Search makes sure that only users with access and permissions to a document can see the acronyms that are discovered from it.</span></span> <span data-ttu-id="e7127-180">在使用者的信箱中找到首字縮寫時，只有該使用者可以看到該縮寫。</span><span class="sxs-lookup"><span data-stu-id="e7127-180">When an acronym is found in a user's mailbox, only that user can see that acronym.</span></span>

> [!NOTE]
> <span data-ttu-id="e7127-181">系統管理員策劃首字母縮寫，不需要任何設定。</span><span class="sxs-lookup"><span data-stu-id="e7127-181">No setup is needed for admin-curated acronyms.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="e7127-182">常見問題集</span><span class="sxs-lookup"><span data-stu-id="e7127-182">Frequently asked questions</span></span>

<span data-ttu-id="e7127-183">**問：系統管理員-策劃和系統策劃資料排名的方式？**</span><span class="sxs-lookup"><span data-stu-id="e7127-183">**Q: How is admin-curated and system-curated data ranked?**</span></span>

<span data-ttu-id="e7127-184">**A：** 結果的排名可能會隨人員而異，因為每位使用者的結果都有個人化。</span><span class="sxs-lookup"><span data-stu-id="e7127-184">**A:** The ranking of results may vary from person to person as results are personalized for each user.</span></span> <span data-ttu-id="e7127-185">這兩種類別都不一定優先于另一種。</span><span class="sxs-lookup"><span data-stu-id="e7127-185">Neither of these categories will always take precedence over the other.</span></span>

<span data-ttu-id="e7127-186">**問：在 Microsoft 搜尋中發佈後，系統管理員策劃首字母縮寫所需的時間必須多久才會顯示？**</span><span class="sxs-lookup"><span data-stu-id="e7127-186">**Q: How long does it take for admin-curated acronyms to be visible in Microsoft Search after they’re published?**</span></span>

<span data-ttu-id="e7127-187">**A：**  已發佈的狀態最多需要三天的縮寫，以供 Microsoft 搜尋使用。</span><span class="sxs-lookup"><span data-stu-id="e7127-187">**A:**  It takes up to three days for acronyms added to Published state to become available in Microsoft Search.</span></span>

<span data-ttu-id="e7127-188">**問：使用者如何觸發縮寫詞答案？**</span><span class="sxs-lookup"><span data-stu-id="e7127-188">**Q: How do users trigger acronyms answers?**</span></span>

<span data-ttu-id="e7127-189">**答**：若要取得縮寫的答案，使用者必須在 [ [Bing](https://bing.com)]、[ [SharePoint](https://products.office.com/sharepoint/collaboration)] 或 [ [Office 365](https://Office.com) **搜尋** ] 方塊中輸入特定的查詢模式。</span><span class="sxs-lookup"><span data-stu-id="e7127-189">**A**: To get acronyms answers, users must enter specific query patterns in a [Bing](https://bing.com), [SharePoint](https://products.office.com/sharepoint/collaboration), or [Office 365](https://Office.com) **Search** box.</span></span>

<span data-ttu-id="e7127-190">**問：當您收到或傳送新的電子郵件或檔之後，系統策劃的首字母縮寫會出現多久時間？**</span><span class="sxs-lookup"><span data-stu-id="e7127-190">**Q: How long does it take for system-curated acronyms to appear after you receive or send a new email or document?**</span></span>

<span data-ttu-id="e7127-191">**A：** 在新的電子郵件或檔中找到的首字縮寫，會在 Microsoft 搜尋結果中長達7天。</span><span class="sxs-lookup"><span data-stu-id="e7127-191">**A:** Acronyms found in a new email or document take up to seven days to appear in Microsoft Search results.</span></span>

<span data-ttu-id="e7127-192">**問：是否需要使用特定的挖掘格式來挑選檔？**</span><span class="sxs-lookup"><span data-stu-id="e7127-192">**Q: Do documents need to be in a specific format for mining to pick them up?**</span></span>

<span data-ttu-id="e7127-193">**A：** 不。</span><span class="sxs-lookup"><span data-stu-id="e7127-193">**A:** No.</span></span> <span data-ttu-id="e7127-194">我們支援所有檔案類型，但不包括影像、資料夾和 ZIP 檔案。</span><span class="sxs-lookup"><span data-stu-id="e7127-194">We support all file types except image, folders, and zip files.</span></span>

<span data-ttu-id="e7127-195">**問： Microsoft 是否會從所有語言的檔中探索縮寫？**</span><span class="sxs-lookup"><span data-stu-id="e7127-195">**Q: Will Microsoft discover acronyms from documents in all languages?**</span></span>

<span data-ttu-id="e7127-196">**A**： Microsoft 只支援從英文檔進行挖掘。</span><span class="sxs-lookup"><span data-stu-id="e7127-196">**A**: Microsoft only supports mining from documents in English.</span></span> <span data-ttu-id="e7127-197">其他語言的支援會分階段新增。</span><span class="sxs-lookup"><span data-stu-id="e7127-197">Support for other languages will be added in phases.</span></span>

<span data-ttu-id="e7127-198">**問：如果我的組織不想要顯示系統策劃首字母縮寫，該怎麼辦？我是否可以在搜尋結果中停止顯示此類型的縮寫？**</span><span class="sxs-lookup"><span data-stu-id="e7127-198">**Q: What if my organization doesn’t want to show system-curated acronyms? Can I stop showing this type of acronym in my search results?**</span></span>

<span data-ttu-id="e7127-199">**A**：若要在搜尋結果中關閉顯示系統策劃首字母縮寫，請遵循 [商務產品的連絡人支援服務](/microsoft-365/admin/contact-support-for-business-products)中的指示，建立客戶支援票證。</span><span class="sxs-lookup"><span data-stu-id="e7127-199">**A**: To turn off showing system-curated acronyms in search results, create a customer support ticket by following the instructions at [Contact support for business products](/microsoft-365/admin/contact-support-for-business-products).</span></span>
<span data-ttu-id="e7127-200">在您建立支援票證後，系統策劃縮寫的最多需要48小時，以避免出現在搜尋結果中。</span><span class="sxs-lookup"><span data-stu-id="e7127-200">After you create a support ticket, it takes up to 48 hours for system-curated acronyms to stop appearing in search results.</span></span>