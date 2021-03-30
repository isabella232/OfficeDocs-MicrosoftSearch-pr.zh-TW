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
ms.openlocfilehash: 013510da28599f41c9dc4bf74da99efa2f6c3e97
ms.sourcegitcommit: 62cb7b8c6a311760cc728f2c70a9a22ca76e977e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/29/2021
ms.locfileid: "51408712"
---
# <a name="manage-acronyms-answers-in-microsoft-search"></a><span data-ttu-id="72d1d-103">管理 Microsoft 搜尋中的縮寫詞答案</span><span class="sxs-lookup"><span data-stu-id="72d1d-103">Manage Acronyms answers in Microsoft Search</span></span>

<span data-ttu-id="72d1d-104">使用者通常會在組織或小組所用的不熟悉縮寫和縮寫中執行。</span><span class="sxs-lookup"><span data-stu-id="72d1d-104">Users often run into unfamiliar acronyms and abbreviations used by their organization or team.</span></span> <span data-ttu-id="72d1d-105">組織或小組特有的條款，對從一個小組移至另一個小組的人員來說可能是新的，可與內部協力廠商小組共同作業，或是組織的新功能。</span><span class="sxs-lookup"><span data-stu-id="72d1d-105">Terms that are specific to organizations or teams might be new to people who move from one team to another, work with internal partner teams, or are new to the organization.</span></span>

<span data-ttu-id="72d1d-106">組織不一定會有單一參考的標準術語。</span><span class="sxs-lookup"><span data-stu-id="72d1d-106">Organizations don't always have a single reference for their standard terminology.</span></span> <span data-ttu-id="72d1d-107">缺乏單一參考會使尋找這些縮寫的定義變得很困難。</span><span class="sxs-lookup"><span data-stu-id="72d1d-107">Lack of a single reference makes it hard to find definitions for these acronyms.</span></span> <span data-ttu-id="72d1d-108">Microsoft 搜尋會解決與首字的問題。</span><span class="sxs-lookup"><span data-stu-id="72d1d-108">Microsoft Search solves that problem with Acronyms.</span></span>

## <a name="what-users-experience"></a><span data-ttu-id="72d1d-109">使用者經驗</span><span class="sxs-lookup"><span data-stu-id="72d1d-109">What users experience</span></span>

<span data-ttu-id="72d1d-110">Microsoft Search 使用者可以在 [Bing](https://Bing.com)、 [SharePoint](https://products.office.com/sharepoint/collaboration)和 [Office 365](https://Office.com)中取得具有縮寫的定義。</span><span class="sxs-lookup"><span data-stu-id="72d1d-110">Microsoft Search users can get definitions with Acronyms in [Bing](https://Bing.com), [SharePoint](https://products.office.com/sharepoint/collaboration), and [Office 365](https://Office.com).</span></span> <span data-ttu-id="72d1d-111">在 [ **搜尋** ] 方塊中，使用者輸入如下範例的查詢：</span><span class="sxs-lookup"><span data-stu-id="72d1d-111">In the **Search** box, users enter queries like these examples:</span></span>

- <span data-ttu-id="72d1d-112">*何謂* DNN</span><span class="sxs-lookup"><span data-stu-id="72d1d-112">*What is* DNN</span></span>
- <span data-ttu-id="72d1d-113">*定義* DNN</span><span class="sxs-lookup"><span data-stu-id="72d1d-113">*Define* DNN</span></span>
- <span data-ttu-id="72d1d-114">DNN *定義*</span><span class="sxs-lookup"><span data-stu-id="72d1d-114">DNN *definition*</span></span>
- <span data-ttu-id="72d1d-115">*展開* DNN</span><span class="sxs-lookup"><span data-stu-id="72d1d-115">*Expand* DNN</span></span>
- <span data-ttu-id="72d1d-116">DNN *擴充*</span><span class="sxs-lookup"><span data-stu-id="72d1d-116">DNN *expansion*</span></span>
- <span data-ttu-id="72d1d-117">*的意義* DNN</span><span class="sxs-lookup"><span data-stu-id="72d1d-117">*Meaning of* DNN</span></span>
- <span data-ttu-id="72d1d-118">DNN *表示*</span><span class="sxs-lookup"><span data-stu-id="72d1d-118">DNN *means*</span></span>
- <span data-ttu-id="72d1d-119">DNN *代表*</span><span class="sxs-lookup"><span data-stu-id="72d1d-119">DNN *stands for*</span></span>

<span data-ttu-id="72d1d-120">結果會包含使用者組織中所顯示之 DNN 的所有意義。</span><span class="sxs-lookup"><span data-stu-id="72d1d-120">The result includes all the meanings of DNN that are present within the user’s organization.</span></span>

> [!NOTE]
> <span data-ttu-id="72d1d-121">使用者必須輸入包含縮寫詞所指定 *關鍵字* 的查詢，以觸發其對應的答案。</span><span class="sxs-lookup"><span data-stu-id="72d1d-121">Users must enter a query that includes the acronym’s specified *keywords* to trigger its corresponding answers.</span></span> <span data-ttu-id="72d1d-122">縮寫詞查詢不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="72d1d-122">Acronym queries are not case sensitive.</span></span>

## <a name="set-up-acronyms-answers"></a><span data-ttu-id="72d1d-123">設定縮寫詞答案</span><span class="sxs-lookup"><span data-stu-id="72d1d-123">Set up acronyms answers</span></span>

<span data-ttu-id="72d1d-124">在 [Microsoft 365 系統管理中心](https://admin.microsoft.com)中，移至 [ [**縮寫**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms)]，然後選取 [ **新增縮寫**]。</span><span class="sxs-lookup"><span data-stu-id="72d1d-124">In the [Microsoft 365 admin center](https://admin.microsoft.com), go to [**Acronyms**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms), and then select **Add acronym**.</span></span>

<span data-ttu-id="72d1d-125">Microsoft 搜尋會查詢兩個數據源，以提供使用者搜尋的縮寫答案：</span><span class="sxs-lookup"><span data-stu-id="72d1d-125">Microsoft Search queries two data sources to provide Acronyms answers to users’ searches:</span></span>

1. <span data-ttu-id="72d1d-126">**Admin-策劃**。</span><span class="sxs-lookup"><span data-stu-id="72d1d-126">**Admin-curated**.</span></span> <span data-ttu-id="72d1d-127">由系統管理員在系統管理員 [中央](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms)提供。</span><span class="sxs-lookup"><span data-stu-id="72d1d-127">Provided by IT administrators in the [admin center](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms).</span></span>
2. <span data-ttu-id="72d1d-128">**System-策劃**。</span><span class="sxs-lookup"><span data-stu-id="72d1d-128">**System-curated**.</span></span> <span data-ttu-id="72d1d-129">由 Microsoft 搜尋從使用者的電子郵件和檔，以及組織內可公開使用的資料所探索。</span><span class="sxs-lookup"><span data-stu-id="72d1d-129">Discovered by Microsoft Search from users' email and documents, as well as publicly available data within the organization.</span></span>

### <a name="set-up-admin-curated-acronyms"></a><span data-ttu-id="72d1d-130">設定系統管理員-策劃縮寫</span><span class="sxs-lookup"><span data-stu-id="72d1d-130">Set up Admin-curated acronyms</span></span>

<span data-ttu-id="72d1d-131">搜尋管理員可以在[Microsoft 搜尋系統管理中心](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch)的 [[縮寫]](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms)索引標籤上新增縮寫。</span><span class="sxs-lookup"><span data-stu-id="72d1d-131">Search administrators can add acronyms on the [Acronyms tab](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms) in the  [Microsoft Search admin center](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch).</span></span> <span data-ttu-id="72d1d-132">您可以從任何內部網站或存放庫向系統管理中心新增縮寫。</span><span class="sxs-lookup"><span data-stu-id="72d1d-132">You can add acronyms from any internal site or repository to the admin center.</span></span> <span data-ttu-id="72d1d-133">您可以將這些縮寫詞新增至 **已發佈** 或 **草稿** 的狀態：</span><span class="sxs-lookup"><span data-stu-id="72d1d-133">These acronyms can be added to **Published** or **Draft** state:</span></span>

<span data-ttu-id="72d1d-134">**發行狀態**。</span><span class="sxs-lookup"><span data-stu-id="72d1d-134">**Published state**.</span></span> <span data-ttu-id="72d1d-135">組織中的使用者可以透過 Microsoft 搜尋取得縮寫。</span><span class="sxs-lookup"><span data-stu-id="72d1d-135">Acronyms are available to the organization’s users through Microsoft Search.</span></span>

> [!NOTE]
> <span data-ttu-id="72d1d-136">最多可能需要三天的縮寫，以在 Microsoft 搜尋中加入已發佈的狀態。</span><span class="sxs-lookup"><span data-stu-id="72d1d-136">It might take up to three days for acronyms added to Published state to become available in Microsoft Search.</span></span>

<span data-ttu-id="72d1d-137">**草稿狀態**。</span><span class="sxs-lookup"><span data-stu-id="72d1d-137">**Draft state**.</span></span> <span data-ttu-id="72d1d-138">如果您想要在 Microsoft 搜尋中使用首字縮寫，您可以新增草稿狀態的縮寫。</span><span class="sxs-lookup"><span data-stu-id="72d1d-138">If you want to review an acronym before making it available in Microsoft Search, you can add the acronym in a Draft state.</span></span> <span data-ttu-id="72d1d-139">草稿狀態中的縮寫不會出現在搜尋結果中。</span><span class="sxs-lookup"><span data-stu-id="72d1d-139">Acronyms in the Draft state will not appear in search results.</span></span> <span data-ttu-id="72d1d-140">您必須將縮寫詞移至發佈的狀態，使其顯示在搜尋結果中。</span><span class="sxs-lookup"><span data-stu-id="72d1d-140">You will need to move the acronym to the Published state to make it appear in search results.</span></span>

<span data-ttu-id="72d1d-141">**排除的狀態**。</span><span class="sxs-lookup"><span data-stu-id="72d1d-141">**Excluded state**.</span></span> <span data-ttu-id="72d1d-142">如果您想要防止首字縮寫出現在 Microsoft 搜尋中，請使用 **排除縮寫詞** 加以新增。</span><span class="sxs-lookup"><span data-stu-id="72d1d-142">If you want to prevent an acronym from appearing in Microsoft Search, use **Exclude an acronym** to add it.</span></span> <span data-ttu-id="72d1d-143">若要停止排除首字縮寫，您必須刪除排除的縮寫，並新增它或在您發佈的清單中驗證。</span><span class="sxs-lookup"><span data-stu-id="72d1d-143">To stop an acronym from being excluded, you'll need to delete the excluded acronym and add it or verify it's in your published list.</span></span>

<span data-ttu-id="72d1d-144">您可以在 CSV 檔案中個別加入縮寫或大容量匯入。</span><span class="sxs-lookup"><span data-stu-id="72d1d-144">You can add acronyms individually or bulk import them in a CSV file.</span></span> <span data-ttu-id="72d1d-145">使用下表所示的欄位上載 CSV 檔案：</span><span class="sxs-lookup"><span data-stu-id="72d1d-145">Upload a CSV file with the fields shown in the following table:</span></span>

| <span data-ttu-id="72d1d-146">縮寫 (強制) </span><span class="sxs-lookup"><span data-stu-id="72d1d-146">Acronym (Mandatory)</span></span> | <span data-ttu-id="72d1d-147">代表 (強制) </span><span class="sxs-lookup"><span data-stu-id="72d1d-147">Stands for (Mandatory)</span></span> | <span data-ttu-id="72d1d-148">URL</span><span class="sxs-lookup"><span data-stu-id="72d1d-148">Url</span></span> | <span data-ttu-id="72d1d-149">描述</span><span class="sxs-lookup"><span data-stu-id="72d1d-149">Description</span></span>  | <span data-ttu-id="72d1d-150">狀態 (強制) </span><span class="sxs-lookup"><span data-stu-id="72d1d-150">State (Mandatory)</span></span> | <span data-ttu-id="72d1d-151">上次修改日期</span><span class="sxs-lookup"><span data-stu-id="72d1d-151">Last Modified</span></span> | <span data-ttu-id="72d1d-152">上次修改者</span><span class="sxs-lookup"><span data-stu-id="72d1d-152">Last Modified By</span></span> | <span data-ttu-id="72d1d-153">識別碼</span><span class="sxs-lookup"><span data-stu-id="72d1d-153">Id</span></span> |
| --------- | --------- | --------- | ---------- | --------- |--------- |--------- |--------- |
| <span data-ttu-id="72d1d-154">*Xxx*</span><span class="sxs-lookup"><span data-stu-id="72d1d-154">*XXX*</span></span> | <span data-ttu-id="72d1d-155">*拼寫縮寫*</span><span class="sxs-lookup"><span data-stu-id="72d1d-155">*Spelled out abbreviation*</span></span> | <span data-ttu-id="72d1d-156">*Source*</span><span class="sxs-lookup"><span data-stu-id="72d1d-156">*Source*</span></span> |  | <span data-ttu-id="72d1d-157">*已發佈、草稿或排除*</span><span class="sxs-lookup"><span data-stu-id="72d1d-157">*Published, Draft, or Excluded*</span></span> |  |  |  |

### <a name="csv-fields"></a><span data-ttu-id="72d1d-158">CSV 欄位</span><span class="sxs-lookup"><span data-stu-id="72d1d-158">CSV fields</span></span>

<span data-ttu-id="72d1d-159">**縮寫**。</span><span class="sxs-lookup"><span data-stu-id="72d1d-159">**Acronym**.</span></span> <span data-ttu-id="72d1d-160">包含實際的簡寫形式或縮寫。</span><span class="sxs-lookup"><span data-stu-id="72d1d-160">Contains the actual short form or acronym.</span></span> <span data-ttu-id="72d1d-161">例如， *DNN*。</span><span class="sxs-lookup"><span data-stu-id="72d1d-161">An example is *DNN*.</span></span>

<span data-ttu-id="72d1d-162">**代表**。</span><span class="sxs-lookup"><span data-stu-id="72d1d-162">**Stands for**.</span></span> <span data-ttu-id="72d1d-163">包含縮寫的定義。</span><span class="sxs-lookup"><span data-stu-id="72d1d-163">Contains the definition of the acronym.</span></span> <span data-ttu-id="72d1d-164">例如， *Deep 神經網路*。</span><span class="sxs-lookup"><span data-stu-id="72d1d-164">An example is *Deep Neural Network*.</span></span>

<span data-ttu-id="72d1d-165">**描述**。</span><span class="sxs-lookup"><span data-stu-id="72d1d-165">**Description**.</span></span> <span data-ttu-id="72d1d-166">縮寫的簡短描述，可提供使用者更多有關縮寫和其定義的資訊。</span><span class="sxs-lookup"><span data-stu-id="72d1d-166">A brief description of the acronym that gives users more info about the acronym and its definition.</span></span> <span data-ttu-id="72d1d-167">例如， *deep 神經網路是具有某一層級複雜性的神經網路，具有超過兩層的神經網路*。</span><span class="sxs-lookup"><span data-stu-id="72d1d-167">For example, *A deep neural network is a neural network with a certain level of complexity, a neural network with more than two layers*.</span></span>

<span data-ttu-id="72d1d-168">**來源**。</span><span class="sxs-lookup"><span data-stu-id="72d1d-168">**Source**.</span></span> <span data-ttu-id="72d1d-169">您要讓使用者流覽的頁面或網站 URL，以取得有關縮寫的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="72d1d-169">The URL of the page or website where you want users to go for more information about the acronym.</span></span>

<span data-ttu-id="72d1d-170">**狀態**。</span><span class="sxs-lookup"><span data-stu-id="72d1d-170">**State**.</span></span> <span data-ttu-id="72d1d-171">此欄位可以採用兩個值：</span><span class="sxs-lookup"><span data-stu-id="72d1d-171">This field can take two values:</span></span>

- <span data-ttu-id="72d1d-172">**草稿**。</span><span class="sxs-lookup"><span data-stu-id="72d1d-172">**Draft**.</span></span> <span data-ttu-id="72d1d-173">將縮寫新增至草稿狀態。</span><span class="sxs-lookup"><span data-stu-id="72d1d-173">Adds the acronym to the Draft state.</span></span>
- <span data-ttu-id="72d1d-174">**發行**。</span><span class="sxs-lookup"><span data-stu-id="72d1d-174">**Published**.</span></span> <span data-ttu-id="72d1d-175">將縮寫新增至發佈的狀態，並使其可用於 Microsoft 搜尋。</span><span class="sxs-lookup"><span data-stu-id="72d1d-175">Adds the acronym to the Published state and makes it available in Microsoft Search.</span></span>
- <span data-ttu-id="72d1d-176">**排除**。</span><span class="sxs-lookup"><span data-stu-id="72d1d-176">**Excluded**.</span></span> <span data-ttu-id="72d1d-177">新增已排除狀態的縮寫，使其不會出現在 Microsoft 搜尋中。</span><span class="sxs-lookup"><span data-stu-id="72d1d-177">Adds the acronym to the Excluded state and prevents it from appearing in Microsoft Search.</span></span>

### <a name="system-curated-acronyms"></a><span data-ttu-id="72d1d-178">系統策劃縮寫</span><span class="sxs-lookup"><span data-stu-id="72d1d-178">System-curated acronyms</span></span>

<span data-ttu-id="72d1d-179">將組織內使用的所有縮寫詞新增至答案可能是一項挑戰。</span><span class="sxs-lookup"><span data-stu-id="72d1d-179">It might be a challenge for admins to add all the acronyms used within an organization to Answers.</span></span> <span data-ttu-id="72d1d-180">這項功能可找出搜尋系統管理員甚至不會察覺的縮寫。</span><span class="sxs-lookup"><span data-stu-id="72d1d-180">This feature can find acronyms that search administrators aren’t even aware of.</span></span> <span data-ttu-id="72d1d-181">若要執行這項操作，Microsoft 搜尋還會從這些來源探索並 curates 縮寫：</span><span class="sxs-lookup"><span data-stu-id="72d1d-181">To do that work, Microsoft Search also discovers and curates acronyms from these sources:</span></span>

- <span data-ttu-id="72d1d-182">使用者的電子郵件</span><span class="sxs-lookup"><span data-stu-id="72d1d-182">Users’ emails</span></span>
- <span data-ttu-id="72d1d-183">[SharePoint](https://products.office.com/sharepoint/collaboration)、 [Microsoft OneDrive]( https://onedrive.live.com/about/)和[microsoft OneNote](https://www.onenote.com/)中的檔</span><span class="sxs-lookup"><span data-stu-id="72d1d-183">Documents in [SharePoint](https://products.office.com/sharepoint/collaboration), [Microsoft OneDrive]( https://onedrive.live.com/about/), and [Microsoft OneNote](https://www.onenote.com/)</span></span>
- <span data-ttu-id="72d1d-184">組織內使用者可以存取的公用檔 SharePoint、OneDrive 或 OneNote</span><span class="sxs-lookup"><span data-stu-id="72d1d-184">Public documents within the organization that users have access to in SharePoint, OneDrive, or OneNote</span></span>

<span data-ttu-id="72d1d-185">Microsoft 搜尋可確保只有對檔具有存取權和許可權的使用者才能看到其所探索的縮寫。</span><span class="sxs-lookup"><span data-stu-id="72d1d-185">Microsoft Search makes sure that only users with access and permissions to a document can see the acronyms that are discovered from it.</span></span> <span data-ttu-id="72d1d-186">在使用者的信箱中找到首字縮寫時，只有該使用者可以看到該縮寫。</span><span class="sxs-lookup"><span data-stu-id="72d1d-186">When an acronym is found in a user's mailbox, only that user can see that acronym.</span></span>

> [!NOTE]
> <span data-ttu-id="72d1d-187">不需要安裝策劃的首字母縮寫。</span><span class="sxs-lookup"><span data-stu-id="72d1d-187">No setup is needed for system-curated acronyms.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="72d1d-188">常見問題集</span><span class="sxs-lookup"><span data-stu-id="72d1d-188">Frequently asked questions</span></span>

<span data-ttu-id="72d1d-189">**問：系統管理員-策劃和系統策劃資料排名的方式？**</span><span class="sxs-lookup"><span data-stu-id="72d1d-189">**Q: How is admin-curated and system-curated data ranked?**</span></span>

<span data-ttu-id="72d1d-190">**A：** 結果的排名可能會隨人員而異，因為每位使用者的結果都有個人化。</span><span class="sxs-lookup"><span data-stu-id="72d1d-190">**A:** The ranking of results may vary from person to person as results are personalized for each user.</span></span> <span data-ttu-id="72d1d-191">這兩種類別都不一定優先于另一種。</span><span class="sxs-lookup"><span data-stu-id="72d1d-191">Neither of these categories will always take precedence over the other.</span></span>

<span data-ttu-id="72d1d-192">**問：在 Microsoft 搜尋中發佈後，系統管理員策劃首字母縮寫所需的時間必須多久才會顯示？**</span><span class="sxs-lookup"><span data-stu-id="72d1d-192">**Q: How long does it take for admin-curated acronyms to be visible in Microsoft Search after they’re published?**</span></span>

<span data-ttu-id="72d1d-193">**A：**  最多需要一天的縮寫，加入至已發佈的狀態，可在 Microsoft 搜尋中使用。</span><span class="sxs-lookup"><span data-stu-id="72d1d-193">**A:**  It takes up to a day for acronyms added to Published state to become available in Microsoft Search.</span></span>

<span data-ttu-id="72d1d-194">**問：使用者如何觸發縮寫詞答案？**</span><span class="sxs-lookup"><span data-stu-id="72d1d-194">**Q: How do users trigger acronyms answers?**</span></span>

<span data-ttu-id="72d1d-195">**答**：若要取得縮寫的答案，使用者必須在 [ [Bing](https://bing.com)]、[ [SharePoint](https://products.office.com/sharepoint/collaboration)] 或 [ [Office 365](https://Office.com) **搜尋** ] 方塊中輸入特定的查詢模式。</span><span class="sxs-lookup"><span data-stu-id="72d1d-195">**A**: To get acronyms answers, users must enter specific query patterns in a [Bing](https://bing.com), [SharePoint](https://products.office.com/sharepoint/collaboration), or [Office 365](https://Office.com) **Search** box.</span></span>

<span data-ttu-id="72d1d-196">**問：當您收到或傳送新的電子郵件或檔之後，系統策劃的首字母縮寫會出現多久時間？**</span><span class="sxs-lookup"><span data-stu-id="72d1d-196">**Q: How long does it take for system-curated acronyms to appear after you receive or send a new email or document?**</span></span>

<span data-ttu-id="72d1d-197">**A：** 在新的電子郵件或檔中找到的首字縮寫，會在 Microsoft 搜尋結果中長達7天。</span><span class="sxs-lookup"><span data-stu-id="72d1d-197">**A:** Acronyms found in a new email or document take up to seven days to appear in Microsoft Search results.</span></span>

<span data-ttu-id="72d1d-198">**問：若排除併發布縮寫，會發生什麼事？**</span><span class="sxs-lookup"><span data-stu-id="72d1d-198">**Q: What happens when an acronym is both excluded and published?**</span></span>

<span data-ttu-id="72d1d-199">**A：** 排除的縮寫詞會具有優先順序，並可防止發佈的縮寫出現在搜尋結果中。</span><span class="sxs-lookup"><span data-stu-id="72d1d-199">**A:** The excluded acronym is given priority and prevents the published acronym from appearing in search results.</span></span> <span data-ttu-id="72d1d-200">它不會刪除或移除已發佈的縮寫。</span><span class="sxs-lookup"><span data-stu-id="72d1d-200">It doesn't delete or remove the published acronym.</span></span>

<span data-ttu-id="72d1d-201">**問：從 Microsoft 搜尋結果中排除縮寫需要多久時間？**</span><span class="sxs-lookup"><span data-stu-id="72d1d-201">**Q: How long does it take for an acronym to be excluded from Microsoft Search results?**</span></span>

<span data-ttu-id="72d1d-202">**A**：在搜尋結果中，不會有一天的時間可用於排除的首字。</span><span class="sxs-lookup"><span data-stu-id="72d1d-202">**A**: It takes up to a day for an excluded acronym to stop appearing in search results.</span></span>

<span data-ttu-id="72d1d-203">**Q：針對系統策劃首字母縮寫，是否需要使用特定格式的檔？**</span><span class="sxs-lookup"><span data-stu-id="72d1d-203">**Q: For system-curated acronyms, do documents need to be in a specific format?**</span></span>

<span data-ttu-id="72d1d-204">**A：** 不。</span><span class="sxs-lookup"><span data-stu-id="72d1d-204">**A:** No.</span></span> <span data-ttu-id="72d1d-205">我們支援所有檔案類型，但不包括 image、folder 和 zip 檔案。</span><span class="sxs-lookup"><span data-stu-id="72d1d-205">We support all file types except image, folder, and zip files.</span></span>

<span data-ttu-id="72d1d-206">**問： Microsoft 是否會從所有語言的檔中探索縮寫？**</span><span class="sxs-lookup"><span data-stu-id="72d1d-206">**Q: Will Microsoft discover acronyms from documents in all languages?**</span></span>

<span data-ttu-id="72d1d-207">**A**： Microsoft 只支援英文、西班牙文、法文、義大利文、德文和葡萄牙文的檔中的策劃首字母縮寫。</span><span class="sxs-lookup"><span data-stu-id="72d1d-207">**A**: Microsoft only supports system-curated acronyms from documents in English, Spanish, French, Italian, German, and Portuguese.</span></span> <span data-ttu-id="72d1d-208">其他語言的支援會分階段新增。</span><span class="sxs-lookup"><span data-stu-id="72d1d-208">Support for other languages will be added in phases.</span></span>

<span data-ttu-id="72d1d-209">**問：如果我的組織不想要顯示系統策劃首字母縮寫，該怎麼辦？我是否可以在搜尋結果中停止顯示此類型的縮寫？**</span><span class="sxs-lookup"><span data-stu-id="72d1d-209">**Q: What if my organization doesn’t want to show system-curated acronyms? Can I stop showing this type of acronym in my search results?**</span></span>

<span data-ttu-id="72d1d-210">**A**：若要在搜尋結果中關閉顯示系統策劃首字母縮寫，請遵循 [商務產品的連絡人支援服務](/microsoft-365/admin/contact-support-for-business-products)中的指示，建立客戶支援票證。</span><span class="sxs-lookup"><span data-stu-id="72d1d-210">**A**: To turn off showing system-curated acronyms in search results, create a customer support ticket by following the instructions at [Contact support for business products](/microsoft-365/admin/contact-support-for-business-products).</span></span>
<span data-ttu-id="72d1d-211">在您建立支援票證後，系統策劃縮寫的最多需要48小時，以避免出現在搜尋結果中。</span><span class="sxs-lookup"><span data-stu-id="72d1d-211">After you create a support ticket, it takes up to 48 hours for system-curated acronyms to stop appearing in search results.</span></span>
