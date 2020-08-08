---
title: 在 Microsoft 搜尋中管理縮寫詞答案
ms.author: jeffkizn
author: jeffkizn
manager: parulm
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 在 Microsoft 搜尋中建立及更新縮寫的答案
ms.openlocfilehash: 68e62884898e3aa081fc32438ad9a80068092738
ms.sourcegitcommit: b3738f5ab02bfba9dedf099e035f3850607be480
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/07/2020
ms.locfileid: "46591506"
---
# <a name="manage-acronyms-answers-in-microsoft-search"></a><span data-ttu-id="93d73-103">管理 Microsoft 搜尋中的縮寫詞答案</span><span class="sxs-lookup"><span data-stu-id="93d73-103">Manage Acronyms answers in Microsoft Search</span></span>

<span data-ttu-id="93d73-104">使用者通常會在組織或小組所用的不熟悉縮寫和縮寫中執行。</span><span class="sxs-lookup"><span data-stu-id="93d73-104">Users often run into unfamiliar acronyms and abbreviations used by their organization or team.</span></span> <span data-ttu-id="93d73-105">組織或小組特有的條款，對從一個小組移至另一個小組的人員來說可能是新的，可與內部協力廠商小組共同作業，或是組織的新功能。</span><span class="sxs-lookup"><span data-stu-id="93d73-105">Terms that are specific to organizations or teams might be new to people who move from one team to another, work with internal partner teams, or are new to the organization.</span></span>

<span data-ttu-id="93d73-106">組織不一定會有單一參考的標準術語。</span><span class="sxs-lookup"><span data-stu-id="93d73-106">Organizations don't always have a single reference for their standard terminology.</span></span> <span data-ttu-id="93d73-107">缺乏單一參考會使您很難尋找這些縮寫詞的定義或擴充。</span><span class="sxs-lookup"><span data-stu-id="93d73-107">Lack of a single reference makes it hard to find definitions or expansions for these acronyms.</span></span> <span data-ttu-id="93d73-108">Microsoft 搜尋會解決與首字的問題。</span><span class="sxs-lookup"><span data-stu-id="93d73-108">Microsoft Search solves that problem with Acronyms.</span></span>

## <a name="what-users-experience"></a><span data-ttu-id="93d73-109">使用者經驗</span><span class="sxs-lookup"><span data-stu-id="93d73-109">What users experience</span></span>

<span data-ttu-id="93d73-110">Microsoft Search 使用者可以在[Bing](https://Bing.com)、 [SharePoint](https://products.office.com/sharepoint/collaboration)和[Office 365](https://Office.com)中取得具有縮寫的定義。</span><span class="sxs-lookup"><span data-stu-id="93d73-110">Microsoft Search users can get definitions with Acronyms in [Bing](https://Bing.com), [SharePoint](https://products.office.com/sharepoint/collaboration), and [Office 365](https://Office.com).</span></span> <span data-ttu-id="93d73-111">在 [**搜尋**] 方塊中，使用者輸入如下範例的查詢：</span><span class="sxs-lookup"><span data-stu-id="93d73-111">In the **Search** box, users enter queries like these examples:</span></span>

- <span data-ttu-id="93d73-112">*何謂*DNN</span><span class="sxs-lookup"><span data-stu-id="93d73-112">*What is* DNN</span></span>
- <span data-ttu-id="93d73-113">*定義*DNN</span><span class="sxs-lookup"><span data-stu-id="93d73-113">*Define* DNN</span></span>
- <span data-ttu-id="93d73-114">DNN*定義*</span><span class="sxs-lookup"><span data-stu-id="93d73-114">DNN *definition*</span></span>
- <span data-ttu-id="93d73-115">*展開*DNN</span><span class="sxs-lookup"><span data-stu-id="93d73-115">*Expand* DNN</span></span>
- <span data-ttu-id="93d73-116">DNN*擴充*</span><span class="sxs-lookup"><span data-stu-id="93d73-116">DNN *expansion*</span></span>
- <span data-ttu-id="93d73-117">*的意義*DNN</span><span class="sxs-lookup"><span data-stu-id="93d73-117">*Meaning of* DNN</span></span>
- <span data-ttu-id="93d73-118">DNN*表示*</span><span class="sxs-lookup"><span data-stu-id="93d73-118">DNN *means*</span></span>

<span data-ttu-id="93d73-119">結果會包含使用者組織中所顯示之 DNN 的所有意義。</span><span class="sxs-lookup"><span data-stu-id="93d73-119">The result includes all the meanings of DNN that are present within the user’s organization.</span></span>

> [!NOTE]
> <span data-ttu-id="93d73-120">使用者必須輸入包含縮寫詞所指定*關鍵字*的查詢，以觸發其對應的答案。</span><span class="sxs-lookup"><span data-stu-id="93d73-120">Users must enter a query that includes the acronym’s specified *keywords* to trigger its corresponding answers.</span></span> <span data-ttu-id="93d73-121">縮寫詞查詢不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="93d73-121">Acronym queries are not case sensitive.</span></span>

## <a name="set-up-acronyms-answers"></a><span data-ttu-id="93d73-122">設定縮寫詞答案</span><span class="sxs-lookup"><span data-stu-id="93d73-122">Set up Acronyms answers</span></span>

<span data-ttu-id="93d73-123">在 Microsoft 365 系統[管理中心](https://admin.microsoft.com)中，移至**Settings**[  >  **microsoft Search**  >  **解答**  >  [**縮寫**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms)] 的 [設定]，然後選取 [**新增縮寫**]。</span><span class="sxs-lookup"><span data-stu-id="93d73-123">In the Microsoft 365 [admin center](https://admin.microsoft.com), go to **Settings** > **Microsoft Search** > **Answers** > [**Acronyms**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms), and then select **Add acronyms**.</span></span>

<span data-ttu-id="93d73-124">Microsoft 搜尋會查詢兩個數據源，以提供使用者搜尋的縮寫答案：</span><span class="sxs-lookup"><span data-stu-id="93d73-124">Microsoft Search queries two data sources to provide Acronyms answers to users’ searches:</span></span>

1. <span data-ttu-id="93d73-125">**編輯縮寫**。</span><span class="sxs-lookup"><span data-stu-id="93d73-125">**Editorial acronyms**.</span></span> <span data-ttu-id="93d73-126">由系統管理員在系統管理員[中央](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms)提供。</span><span class="sxs-lookup"><span data-stu-id="93d73-126">Provided by IT administrators in the [admin center](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms).</span></span>
2. <span data-ttu-id="93d73-127">**挖掘的縮寫**。</span><span class="sxs-lookup"><span data-stu-id="93d73-127">**Mined acronyms**.</span></span> <span data-ttu-id="93d73-128">由 Microsoft 搜尋從使用者的個人電子郵件和檔，以及組織內可公開使用的資料進行挖掘。</span><span class="sxs-lookup"><span data-stu-id="93d73-128">Mined by Microsoft Search from the user’s personal email and documents and publicly available data within the organization.</span></span>

### <a name="set-up-editorial-acronyms"></a><span data-ttu-id="93d73-129">設定編輯縮寫</span><span class="sxs-lookup"><span data-stu-id="93d73-129">Set up editorial acronyms</span></span>

<span data-ttu-id="93d73-130">搜尋管理員可以在[Microsoft 搜尋系統管理中心](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch)的 [[縮寫]](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms)索引標籤上設定編輯縮寫。</span><span class="sxs-lookup"><span data-stu-id="93d73-130">Search administrators can set up editorial acronyms on the [Acronyms tab](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms) in the  [Microsoft Search admin center](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch).</span></span> <span data-ttu-id="93d73-131">您可以從任何內部網站或存放庫向系統管理中心新增縮寫。</span><span class="sxs-lookup"><span data-stu-id="93d73-131">You can add acronyms from any internal site or repository to the admin center.</span></span> <span data-ttu-id="93d73-132">編輯縮寫可以新增至**已發佈**或**草稿**的狀態：</span><span class="sxs-lookup"><span data-stu-id="93d73-132">Editorial acronyms can be added to **Published** or **Draft** state:</span></span>

<span data-ttu-id="93d73-133">**發行狀態**。</span><span class="sxs-lookup"><span data-stu-id="93d73-133">**Published state**.</span></span> <span data-ttu-id="93d73-134">組織中的雇員可透過 Microsoft 搜尋取得縮寫。</span><span class="sxs-lookup"><span data-stu-id="93d73-134">Acronyms are available to the organization’s employees through Microsoft Search.</span></span>

> [!NOTE]
> <span data-ttu-id="93d73-135">最多可能需要三天的縮寫，以在 Microsoft 搜尋中加入已發佈的狀態。</span><span class="sxs-lookup"><span data-stu-id="93d73-135">It might take up to three days for acronyms added to Published state to become available in Microsoft Search.</span></span>

<span data-ttu-id="93d73-136">**草稿狀態**。</span><span class="sxs-lookup"><span data-stu-id="93d73-136">**Draft state**.</span></span> <span data-ttu-id="93d73-137">如果系統管理員想要在 Microsoft 搜尋中提供首字縮寫的答案，可將縮寫新增至草稿狀態。</span><span class="sxs-lookup"><span data-stu-id="93d73-137">If admins want to review Acronyms answers before making them available in Microsoft Search, they can add the acronyms to Draft state.</span></span> <span data-ttu-id="93d73-138">新增至草稿狀態的縮寫詞無法在 Microsoft 搜尋中使用。</span><span class="sxs-lookup"><span data-stu-id="93d73-138">Acronyms added to Draft state aren’t available in Microsoft Search.</span></span> <span data-ttu-id="93d73-139">系統管理員必須將縮寫詞新增至發行的狀態，以供使用。</span><span class="sxs-lookup"><span data-stu-id="93d73-139">Admins need to add the acronyms to Published state to make them available.</span></span>

<span data-ttu-id="93d73-140">系統管理員可以個別新增首字縮寫或在 CSV 檔案中大量匯入。</span><span class="sxs-lookup"><span data-stu-id="93d73-140">Admins can add acronyms individually or bulk import them in a CSV file.</span></span> <span data-ttu-id="93d73-141">使用下表所示的欄位上載 CSV 檔案：</span><span class="sxs-lookup"><span data-stu-id="93d73-141">Upload a CSV file with the fields shown in the following table:</span></span>

| <span data-ttu-id="93d73-142">縮寫 (強制) </span><span class="sxs-lookup"><span data-stu-id="93d73-142">Acronym (mandatory)</span></span> | <span data-ttu-id="93d73-143">擴充 (強制) </span><span class="sxs-lookup"><span data-stu-id="93d73-143">Expansion (mandatory)</span></span> | <span data-ttu-id="93d73-144">描述</span><span class="sxs-lookup"><span data-stu-id="93d73-144">Description</span></span>  | <span data-ttu-id="93d73-145">來源</span><span class="sxs-lookup"><span data-stu-id="93d73-145">Source</span></span> | <span data-ttu-id="93d73-146">狀態 (強制) </span><span class="sxs-lookup"><span data-stu-id="93d73-146">State (mandatory)</span></span> |
| --------- | --------- | ---------- | --------- |--------- |
| <span data-ttu-id="93d73-147">*Xxx*</span><span class="sxs-lookup"><span data-stu-id="93d73-147">*XXX*</span></span> | <span data-ttu-id="93d73-148">*拼寫縮寫*</span><span class="sxs-lookup"><span data-stu-id="93d73-148">*Spelled out abbreviation*</span></span> |  | <span data-ttu-id="93d73-149">[URL]\*\*</span><span class="sxs-lookup"><span data-stu-id="93d73-149">*URL*</span></span> | <span data-ttu-id="93d73-150">*已發佈或草稿*</span><span class="sxs-lookup"><span data-stu-id="93d73-150">*Published or Draft*</span></span> |

### <a name="csv-fields"></a><span data-ttu-id="93d73-151">CSV 欄位</span><span class="sxs-lookup"><span data-stu-id="93d73-151">CSV fields</span></span>

<span data-ttu-id="93d73-152">**縮寫**。</span><span class="sxs-lookup"><span data-stu-id="93d73-152">**Acronym**.</span></span> <span data-ttu-id="93d73-153">包含實際的簡寫形式或縮寫。</span><span class="sxs-lookup"><span data-stu-id="93d73-153">Contains the actual short form or acronym.</span></span> <span data-ttu-id="93d73-154">例如， *DNN*。</span><span class="sxs-lookup"><span data-stu-id="93d73-154">An example is *DNN*.</span></span>

<span data-ttu-id="93d73-155">**擴充**。</span><span class="sxs-lookup"><span data-stu-id="93d73-155">**Expansion**.</span></span> <span data-ttu-id="93d73-156">包含縮寫的擴充。</span><span class="sxs-lookup"><span data-stu-id="93d73-156">Contains the expansion of the acronym.</span></span> <span data-ttu-id="93d73-157">例如， *Deep 神經網路*。</span><span class="sxs-lookup"><span data-stu-id="93d73-157">An example is *Deep Neural Network*.</span></span>

<span data-ttu-id="93d73-158">**描述**。</span><span class="sxs-lookup"><span data-stu-id="93d73-158">**Description**.</span></span> <span data-ttu-id="93d73-159">縮寫的簡短描述，可提供使用者更多有關縮寫和其擴充的資訊。</span><span class="sxs-lookup"><span data-stu-id="93d73-159">A brief description of the acronym that gives users more info about the acronym and its expansion.</span></span> <span data-ttu-id="93d73-160">例如， *deep 神經網路是具有某一層級複雜性的神經網路，具有超過兩層的神經網路*。</span><span class="sxs-lookup"><span data-stu-id="93d73-160">For example, *A deep neural network is a neural network with a certain level of complexity, a neural network with more than two layers*.</span></span>

<span data-ttu-id="93d73-161">**來源**。</span><span class="sxs-lookup"><span data-stu-id="93d73-161">**Source**.</span></span> <span data-ttu-id="93d73-162">您要讓使用者流覽的頁面或網站 URL，以取得有關縮寫的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="93d73-162">The URL of the page or website where you want users to go for more information about the acronym.</span></span>

<span data-ttu-id="93d73-163">**狀態**。</span><span class="sxs-lookup"><span data-stu-id="93d73-163">**State**.</span></span> <span data-ttu-id="93d73-164">此欄位可以採用兩個值：</span><span class="sxs-lookup"><span data-stu-id="93d73-164">This field can take two values:</span></span>

- <span data-ttu-id="93d73-165">**草稿**。</span><span class="sxs-lookup"><span data-stu-id="93d73-165">**Draft**.</span></span> <span data-ttu-id="93d73-166">將縮寫新增至草稿狀態。</span><span class="sxs-lookup"><span data-stu-id="93d73-166">Adds  the acronym to the Draft state.</span></span>
- <span data-ttu-id="93d73-167">**發行**。</span><span class="sxs-lookup"><span data-stu-id="93d73-167">**Published**.</span></span> <span data-ttu-id="93d73-168">將縮寫新增至發佈的狀態，並使其可用於 Microsoft 搜尋。</span><span class="sxs-lookup"><span data-stu-id="93d73-168">Adds the acronym to the Published state and makes it available in Microsoft Search.</span></span>

### <a name="mined-acronyms"></a><span data-ttu-id="93d73-169">挖掘縮寫</span><span class="sxs-lookup"><span data-stu-id="93d73-169">Mined acronyms</span></span>

<span data-ttu-id="93d73-170">將組織內使用的所有縮寫詞新增至答案可能是一項挑戰。</span><span class="sxs-lookup"><span data-stu-id="93d73-170">It might be a challenge for admins to add all the acronyms used within an organization to Answers.</span></span> <span data-ttu-id="93d73-171">這項功能可找出搜尋系統管理員甚至不會察覺的縮寫。</span><span class="sxs-lookup"><span data-stu-id="93d73-171">This feature can find acronyms that search administrators aren’t even aware of.</span></span> <span data-ttu-id="93d73-172">若要執行這項操作，Microsoft 搜尋也會從這些來源中地雷的縮寫：</span><span class="sxs-lookup"><span data-stu-id="93d73-172">To do that work, Microsoft Search also mines acronyms from these sources:</span></span>

- <span data-ttu-id="93d73-173">使用者的電子郵件。</span><span class="sxs-lookup"><span data-stu-id="93d73-173">Users’ emails.</span></span>
- <span data-ttu-id="93d73-174">[SharePoint](https://products.office.com/sharepoint/collaboration)、 [Microsoft OneDrive]( https://onedrive.live.com/about/)和[microsoft OneNote](https://www.onenote.com/)中的檔。</span><span class="sxs-lookup"><span data-stu-id="93d73-174">Documents in [SharePoint](https://products.office.com/sharepoint/collaboration), [Microsoft OneDrive]( https://onedrive.live.com/about/), and [Microsoft OneNote](https://www.onenote.com/).</span></span>
- <span data-ttu-id="93d73-175">組織內的公用檔，可供使用者在 SharePoint、OneDrive 或 OneNote 中存取。</span><span class="sxs-lookup"><span data-stu-id="93d73-175">Public documents within the organization that users have access to in SharePoint, OneDrive, or OneNote.</span></span>

<span data-ttu-id="93d73-176">Microsoft 搜尋可確保只有對檔具有存取權和許可權的使用者才能看到其所挖掘的縮寫。</span><span class="sxs-lookup"><span data-stu-id="93d73-176">Microsoft Search makes sure that only users with access and permissions to a document can see the acronyms that are mined from it.</span></span> <span data-ttu-id="93d73-177">從使用者的信箱中挖掘縮寫時，只有該使用者可以看到該縮寫。</span><span class="sxs-lookup"><span data-stu-id="93d73-177">When an acronym is mined from a user's mailbox, only that user can see that acronym.</span></span>

> [!NOTE]
> <span data-ttu-id="93d73-178">挖掘的縮寫不需要任何設定。</span><span class="sxs-lookup"><span data-stu-id="93d73-178">No setup is needed for mined acronyms.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="93d73-179">常見問題集</span><span class="sxs-lookup"><span data-stu-id="93d73-179">Frequently asked questions</span></span>

<span data-ttu-id="93d73-180">**問：如何進行編輯及挖掘的資料排名？**</span><span class="sxs-lookup"><span data-stu-id="93d73-180">**Q: How is editorial and mined data ranked?**</span></span>

<span data-ttu-id="93d73-181">**A：** 目前的功能是對已挖掘的首字母縮寫詞排名編輯縮寫。</span><span class="sxs-lookup"><span data-stu-id="93d73-181">**A:** The feature currently ranks editorial acronyms above mined acronyms.</span></span>

<span data-ttu-id="93d73-182">**問：在 Microsoft 搜尋中發佈後，編輯的首字縮寫詞必須多久才會顯示？**</span><span class="sxs-lookup"><span data-stu-id="93d73-182">**Q: How long does it take for editorial acronyms to be visible in Microsoft Search after they’re published?**</span></span>

<span data-ttu-id="93d73-183">**A：** 已發佈的狀態最多需要三天的縮寫，以供 Microsoft 搜尋使用。</span><span class="sxs-lookup"><span data-stu-id="93d73-183">**A:**  It takes up to three days for acronyms added to Published state to become available in Microsoft Search.</span></span>

<span data-ttu-id="93d73-184">**問：使用者如何觸發縮寫詞答案？**</span><span class="sxs-lookup"><span data-stu-id="93d73-184">**Q: How do users trigger Acronyms answers?**</span></span>

<span data-ttu-id="93d73-185">**答**：若要取得縮寫的答案，使用者必須在 [ [Bing](https://bing.com)]、[ [SharePoint](https://products.office.com/sharepoint/collaboration)] 或 [ [Office 365](https://Office.com) **搜尋**] 方塊中輸入特定的查詢模式。</span><span class="sxs-lookup"><span data-stu-id="93d73-185">**A**: To get Acronyms answers, users must enter specific query patterns in a [Bing](https://bing.com), [SharePoint](https://products.office.com/sharepoint/collaboration), or [Office 365](https://Office.com) **Search** box.</span></span>

<span data-ttu-id="93d73-186">**問：當您收到或傳送新的電子郵件或檔之後，挖掘的首字縮寫會出現多久時間？**</span><span class="sxs-lookup"><span data-stu-id="93d73-186">**Q: How long does it take for mined acronyms to appear after you receive or send a new email or document?**</span></span>

<span data-ttu-id="93d73-187">**A：** 從新的電子郵件或檔中挖掘的首字母縮寫，會在 Microsoft 搜尋結果中長達7天。</span><span class="sxs-lookup"><span data-stu-id="93d73-187">**A:** Mined acronyms from a new email or document take up to seven days to appear in Microsoft Search results.</span></span>

<span data-ttu-id="93d73-188">**問：是否需要使用特定的挖掘格式來挑選檔？**</span><span class="sxs-lookup"><span data-stu-id="93d73-188">**Q: Do documents need to be in a specific format for mining to pick them up?**</span></span>

<span data-ttu-id="93d73-189">**A：** 不。</span><span class="sxs-lookup"><span data-stu-id="93d73-189">**A:** No.</span></span> <span data-ttu-id="93d73-190">我們支援所有檔案類型，但不包括影像、資料夾和 ZIP 檔案。</span><span class="sxs-lookup"><span data-stu-id="93d73-190">We support all file types except image, folders, and zip files.</span></span>

<span data-ttu-id="93d73-191">**問： Microsoft 是否會利用所有語言的檔中的縮寫？**</span><span class="sxs-lookup"><span data-stu-id="93d73-191">**Q: Will Microsoft mine acronyms from documents in all languages?**</span></span>

<span data-ttu-id="93d73-192">**A**： Microsoft 只支援從英文檔進行挖掘。</span><span class="sxs-lookup"><span data-stu-id="93d73-192">**A**: Microsoft only supports mining from documents in English.</span></span> <span data-ttu-id="93d73-193">其他語言的支援會分階段新增。</span><span class="sxs-lookup"><span data-stu-id="93d73-193">Support for other languages will be added in phases.</span></span>

<span data-ttu-id="93d73-194">**問：如果我的組織不想要顯示挖掘的縮寫，該怎麼辦？是否可以停止在搜尋結果中顯示挖掘的縮寫？**</span><span class="sxs-lookup"><span data-stu-id="93d73-194">**Q: What if my organization doesn’t want to show mined acronyms? Can I stop showing mined acronyms in search results?**</span></span>

<span data-ttu-id="93d73-195">**A**：若要在搜尋結果中關閉顯示挖掘的縮寫，請遵循[商務產品的連絡人支援服務](https://docs.microsoft.com/office365/admin/contact-support-for-business-products?redirectSourcePath=%252f%252farticle%252fContact-Office-365-for-business-support-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b&view=o365-worldwide&tabs=online#BKMK_call_support)中的指示，建立客戶支援憑證。</span><span class="sxs-lookup"><span data-stu-id="93d73-195">**A**: To turn off showing mined acronyms in search results, create a customer support ticket by following the instructions at [Contact support for business products](https://docs.microsoft.com/office365/admin/contact-support-for-business-products?redirectSourcePath=%252f%252farticle%252fContact-Office-365-for-business-support-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b&view=o365-worldwide&tabs=online#BKMK_call_support).</span></span>
<span data-ttu-id="93d73-196">在您建立支援票證之後，挖掘的首字縮寫會花長達48小時的時間，才會出現在搜尋結果中。</span><span class="sxs-lookup"><span data-stu-id="93d73-196">After you create a support ticket, it takes up to 48 hours for mined acronyms to stop appearing in search results.</span></span>
