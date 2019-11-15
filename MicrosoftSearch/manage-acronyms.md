---
title: 管理 Microsoft 搜尋中的縮略字解答
ms.author: v-pamcna
author: TrishaMc1
manager: mnirkhe
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 建立及更新 Microsoft 搜尋中的縮略字解答
ms.openlocfilehash: 4f47d5b743709657459ccbc6b03897c29a51e109
ms.sourcegitcommit: 21361af7c244ffd6ff8689fd0ff0daa359bf4129
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/14/2019
ms.locfileid: "38626817"
---
# <a name="manage-acronyms-answers-in-microsoft-search"></a><span data-ttu-id="7395c-103">管理 Microsoft 搜尋中的縮略字解答</span><span class="sxs-lookup"><span data-stu-id="7395c-103">Manage Acronyms answers in Microsoft Search</span></span>

<span data-ttu-id="7395c-104">經常遇到不太熟悉的縮略字的員工和其組織或小組所使用的縮寫。</span><span class="sxs-lookup"><span data-stu-id="7395c-104">Employees often run into unfamiliar acronyms and abbreviations used by their organization or team.</span></span> <span data-ttu-id="7395c-105">專用於組織或小組的字詞可能是新的人員將從一個小組移至另一個，使用內部合作夥伴小組或新員工的人。</span><span class="sxs-lookup"><span data-stu-id="7395c-105">Terms that are specific to organizations or teams might be new to people who move from one team to another, those who work with internal partner teams, or new employees.</span></span>

<span data-ttu-id="7395c-106">組織不一定需要其更新標準術語的單一參照。</span><span class="sxs-lookup"><span data-stu-id="7395c-106">Organizations don't always have a single reference for their standard terminology.</span></span> <span data-ttu-id="7395c-107">單一參考缺乏所以很難尋找定義或擴充這些縮略字。</span><span class="sxs-lookup"><span data-stu-id="7395c-107">Lack of a single reference makes it hard to find definitions or expansions for these acronyms.</span></span> <span data-ttu-id="7395c-108">Microsoft Search 求解縮略字該問題。</span><span class="sxs-lookup"><span data-stu-id="7395c-108">Microsoft Search solves that problem with Acronyms.</span></span>

## <a name="what-users-experience"></a><span data-ttu-id="7395c-109">使用者體驗</span><span class="sxs-lookup"><span data-stu-id="7395c-109">What users experience</span></span>
<span data-ttu-id="7395c-110">Microsoft Search 使用者可以取得與縮略字[Bing](https://Bing.com)、 [Microsoft Office 365](https://Office.com)和[Microsoft SharePoint Online](https://products.office.com/sharepoint/collaboration)中的定義。</span><span class="sxs-lookup"><span data-stu-id="7395c-110">Microsoft Search users can get definitions with Acronyms in [Bing](https://Bing.com), [Microsoft Office 365](https://Office.com), and [Microsoft SharePoint Online](https://products.office.com/sharepoint/collaboration).</span></span> <span data-ttu-id="7395c-111">在標頭列中的 [**搜尋**] 方塊中，在使用者輸入查詢，例如這些範例：</span><span class="sxs-lookup"><span data-stu-id="7395c-111">In the **Search** boxes in the header bars, users enter queries like these examples:</span></span>

- <span data-ttu-id="7395c-112">*什麼是*DNN</span><span class="sxs-lookup"><span data-stu-id="7395c-112">*What is* DNN</span></span>
- <span data-ttu-id="7395c-113">*定義*DNN</span><span class="sxs-lookup"><span data-stu-id="7395c-113">*Define* DNN</span></span>
- <span data-ttu-id="7395c-114">DNN*定義*</span><span class="sxs-lookup"><span data-stu-id="7395c-114">DNN *definition*</span></span>
- <span data-ttu-id="7395c-115">*依序展開 [* DNN</span><span class="sxs-lookup"><span data-stu-id="7395c-115">*Expand* DNN</span></span>
- <span data-ttu-id="7395c-116">DNN*擴充*</span><span class="sxs-lookup"><span data-stu-id="7395c-116">DNN *expansion*</span></span>
- <span data-ttu-id="7395c-117">*代表的意義*DNN</span><span class="sxs-lookup"><span data-stu-id="7395c-117">*Meaning of* DNN</span></span>
- <span data-ttu-id="7395c-118">DNN*表示*</span><span class="sxs-lookup"><span data-stu-id="7395c-118">DNN *means*</span></span>

<span data-ttu-id="7395c-119">建議的結果會包含所有的意義 DNN 相關使用者的組織內。</span><span class="sxs-lookup"><span data-stu-id="7395c-119">The suggested results include all the meanings of DNN that are present within the user’s organization.</span></span>

> [!NOTE]
> <span data-ttu-id="7395c-120">使用者必須輸入的查詢，包括縮略字指定的*關鍵字*，觸發其相對的答案。</span><span class="sxs-lookup"><span data-stu-id="7395c-120">Users must enter a query that includes the acronym’s specified *keywords* to trigger its corresponding answers.</span></span>  

## <a name="set-up-acronyms-answers"></a><span data-ttu-id="7395c-121">設定縮略字解答</span><span class="sxs-lookup"><span data-stu-id="7395c-121">Set up Acronyms answers</span></span>
<span data-ttu-id="7395c-122">在 Microsoft 365[系統管理中心](https://admin.microsoft.com)中，移至 [**設定** > **Microsoft Search** >**縮略字**，然後選取 [**新增縮略字**。</span><span class="sxs-lookup"><span data-stu-id="7395c-122">In the Microsoft 365 [admin center](https://admin.microsoft.com), go to **Settings** > **Microsoft Search** >**Acronyms**, and then select **Add acronyms**.</span></span> 

<span data-ttu-id="7395c-123">Microsoft 搜尋查詢以提供使用者搜尋的縮略字答案的兩個資料來源：</span><span class="sxs-lookup"><span data-stu-id="7395c-123">Microsoft Search queries two data sources to provide Acronyms answers to users’ searches:</span></span>

1.  <span data-ttu-id="7395c-124">**編輯縮略字**。</span><span class="sxs-lookup"><span data-stu-id="7395c-124">**Editorial acronyms**.</span></span> <span data-ttu-id="7395c-125">在[系統管理中心](https://admin.microsoft.com)中的 IT 系統管理員所提供。</span><span class="sxs-lookup"><span data-stu-id="7395c-125">Provided by IT administrators in the [admin center](https://admin.microsoft.com).</span></span>
2.  <span data-ttu-id="7395c-126">**Mined 縮略字**。</span><span class="sxs-lookup"><span data-stu-id="7395c-126">**Mined acronyms**.</span></span> <span data-ttu-id="7395c-127">由 Microsoft Search mined 從使用者的個人電子郵件和文件和公開提供組織內的資料。</span><span class="sxs-lookup"><span data-stu-id="7395c-127">Mined by Microsoft Search from the user’s personal email and documents and publicly available data within the organization.</span></span>

### <a name="set-up-editorial-acronyms"></a><span data-ttu-id="7395c-128">設定編輯縮略字</span><span class="sxs-lookup"><span data-stu-id="7395c-128">Set up editorial acronyms</span></span>
<span data-ttu-id="7395c-129">IT 系統管理員可以設定[Microsoft 365 系統管理中心]( https://admin.microsoft.com)中的[縮略字] 索引標籤](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch)上的編輯縮略字。</span><span class="sxs-lookup"><span data-stu-id="7395c-129">IT admins can set up editorial acronyms on the [Acronyms tab](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch) in the  [Microsoft 365 admin center]( https://admin.microsoft.com).</span></span> <span data-ttu-id="7395c-130">系統管理中心，您可以從任何內部網站或存放庫新增縮略字。</span><span class="sxs-lookup"><span data-stu-id="7395c-130">You can add acronyms from any internal site or repository to the admin center.</span></span> <span data-ttu-id="7395c-131">編輯縮略字可以新增至**已發佈**] 或 [**草稿**] 狀態：</span><span class="sxs-lookup"><span data-stu-id="7395c-131">Editorial acronyms can be added to **Published** or **Draft** state:</span></span>

<span data-ttu-id="7395c-132">**已發佈的狀態**。</span><span class="sxs-lookup"><span data-stu-id="7395c-132">**Published state**.</span></span> <span data-ttu-id="7395c-133">可透過 Microsoft 搜尋組織的員工的縮略字。</span><span class="sxs-lookup"><span data-stu-id="7395c-133">Acronyms are available to the organization’s employees through Microsoft Search.</span></span>

> [!NOTE]
> <span data-ttu-id="7395c-134">可能需要最多三天的縮略字加入至已發佈狀態成為用於 Microsoft Search。</span><span class="sxs-lookup"><span data-stu-id="7395c-134">It might take up  to three days for acronyms added to Published state to become available in Microsoft Search.</span></span>

<span data-ttu-id="7395c-135">**草稿狀態**。</span><span class="sxs-lookup"><span data-stu-id="7395c-135">**Draft state**.</span></span> <span data-ttu-id="7395c-136">如果系統管理員想要檢閱的縮略字解答之前先用於 Microsoft Search，他們可以新增縮略字為草稿狀態。</span><span class="sxs-lookup"><span data-stu-id="7395c-136">If admins want to review Acronyms answers before making them available in Microsoft Search, they can add the acronyms to Draft state.</span></span> <span data-ttu-id="7395c-137">縮略字加入至草稿狀態不會出現在 Microsoft Search。</span><span class="sxs-lookup"><span data-stu-id="7395c-137">Acronyms added to Draft state aren’t available in Microsoft Search.</span></span> <span data-ttu-id="7395c-138">系統管理員必須將縮寫新增至發佈狀態，以使其能。</span><span class="sxs-lookup"><span data-stu-id="7395c-138">Admins need to add the acronyms to Published state to make them available.</span></span>

<span data-ttu-id="7395c-139">系統管理員可以將縮略字個別或大量將它們匯入 CSV 檔案。</span><span class="sxs-lookup"><span data-stu-id="7395c-139">Admins can add acronyms individually or bulk import them in a CSV file.</span></span> <span data-ttu-id="7395c-140">上傳 CSV 檔案與欄位，如下表所示：</span><span class="sxs-lookup"><span data-stu-id="7395c-140">Upload a CSV file with the fields shown in the following table:</span></span>

| <span data-ttu-id="7395c-141">縮寫 （必要）</span><span class="sxs-lookup"><span data-stu-id="7395c-141">Acronym (mandatory)</span></span> | <span data-ttu-id="7395c-142">擴充 （必要）</span><span class="sxs-lookup"><span data-stu-id="7395c-142">Expansion (mandatory)</span></span> | <span data-ttu-id="7395c-143">描述</span><span class="sxs-lookup"><span data-stu-id="7395c-143">Description</span></span>  | <span data-ttu-id="7395c-144">來源</span><span class="sxs-lookup"><span data-stu-id="7395c-144">Source</span></span> | <span data-ttu-id="7395c-145">狀態 （必要）</span><span class="sxs-lookup"><span data-stu-id="7395c-145">State (mandatory)</span></span> |
| --------- | --------- | ---------- | --------- |--------- |
| <span data-ttu-id="7395c-146">*XXX*</span><span class="sxs-lookup"><span data-stu-id="7395c-146">*XXX*</span></span> | <span data-ttu-id="7395c-147">*拼出縮寫*</span><span class="sxs-lookup"><span data-stu-id="7395c-147">*Spelled out abbreviation*</span></span> |  | <span data-ttu-id="7395c-148">*URL*</span><span class="sxs-lookup"><span data-stu-id="7395c-148">*URL*</span></span> | <span data-ttu-id="7395c-149">*發佈或草稿*</span><span class="sxs-lookup"><span data-stu-id="7395c-149">*Published or Draft*</span></span> |

### <a name="csv-fields"></a><span data-ttu-id="7395c-150">CSV 欄位</span><span class="sxs-lookup"><span data-stu-id="7395c-150">CSV fields</span></span>
<span data-ttu-id="7395c-151">**縮略字**。</span><span class="sxs-lookup"><span data-stu-id="7395c-151">**Acronym**.</span></span> <span data-ttu-id="7395c-152">未包含實際短格式或縮略字。</span><span class="sxs-lookup"><span data-stu-id="7395c-152">Contains the actual short form or acronym.</span></span> <span data-ttu-id="7395c-153">例如， *DNN*。</span><span class="sxs-lookup"><span data-stu-id="7395c-153">An example is *DNN*.</span></span>

<span data-ttu-id="7395c-154">**擴充**。</span><span class="sxs-lookup"><span data-stu-id="7395c-154">**Expansion**.</span></span> <span data-ttu-id="7395c-155">包含擴充的縮寫。</span><span class="sxs-lookup"><span data-stu-id="7395c-155">Contains the expansion of the acronym.</span></span> <span data-ttu-id="7395c-156">例如，*深層非線性網路*。</span><span class="sxs-lookup"><span data-stu-id="7395c-156">An example is *Deep Neural Network*.</span></span>

<span data-ttu-id="7395c-157">**描述**。</span><span class="sxs-lookup"><span data-stu-id="7395c-157">**Description**.</span></span> <span data-ttu-id="7395c-158">讓使用者快速深入的縮寫和其擴充什麼縮略字簡短描述。</span><span class="sxs-lookup"><span data-stu-id="7395c-158">A brief description of the acronym that gives users quick insight into what the acronym and its expansion mean.</span></span> <span data-ttu-id="7395c-159">例如，複雜性的*deep 非線性網路是複雜性的非線性一定程度，具有兩個以上的圖層的非線性網路與網路*。</span><span class="sxs-lookup"><span data-stu-id="7395c-159">For example, *A deep neural network is a neural network with a certain level of complexity, a neural network with more than two layers*.</span></span>

<span data-ttu-id="7395c-160">**來源**。</span><span class="sxs-lookup"><span data-stu-id="7395c-160">**Source**.</span></span> <span data-ttu-id="7395c-161">頁面或您想要使用者前往的縮略字的詳細資訊的網站的 URL。</span><span class="sxs-lookup"><span data-stu-id="7395c-161">The URL of the page or website where you want users to go for more information about the acronym.</span></span>

<span data-ttu-id="7395c-162">**狀態**。</span><span class="sxs-lookup"><span data-stu-id="7395c-162">**State**.</span></span> <span data-ttu-id="7395c-163">此欄位可能需要兩個值：</span><span class="sxs-lookup"><span data-stu-id="7395c-163">This field can take two values:</span></span>

- <span data-ttu-id="7395c-164">**草稿**。</span><span class="sxs-lookup"><span data-stu-id="7395c-164">**Draft**.</span></span> <span data-ttu-id="7395c-165">將縮寫新增至 「 草稿 」 狀態。</span><span class="sxs-lookup"><span data-stu-id="7395c-165">Adds  the acronym to the Draft state.</span></span>
- <span data-ttu-id="7395c-166">**發佈**。</span><span class="sxs-lookup"><span data-stu-id="7395c-166">**Published**.</span></span> <span data-ttu-id="7395c-167">會將縮寫新增至已發佈狀態，並使它用於 Microsoft Search。</span><span class="sxs-lookup"><span data-stu-id="7395c-167">Adds the acronym to the Published state and makes it available in Microsoft Search.</span></span>

### <a name="mined-acronyms"></a><span data-ttu-id="7395c-168">生產縮略字</span><span class="sxs-lookup"><span data-stu-id="7395c-168">Mined acronyms</span></span>
<span data-ttu-id="7395c-169">它可能是系統管理員新增解答組織內所使用的所有縮寫挑戰。</span><span class="sxs-lookup"><span data-stu-id="7395c-169">It might be a challenge for admins to add all the acronyms used within an organization to Answers.</span></span> <span data-ttu-id="7395c-170">這項功能可以找到搜尋系統管理員的縮略字不即使留意。</span><span class="sxs-lookup"><span data-stu-id="7395c-170">This feature can find acronyms that search administrators aren’t even aware of.</span></span> <span data-ttu-id="7395c-171">若要執行該工作，Microsoft Search 也地雷縮略字從這些來源：</span><span class="sxs-lookup"><span data-stu-id="7395c-171">To do that work, Microsoft Search also mines acronyms from these sources:</span></span>

- <span data-ttu-id="7395c-172">使用者的電子郵件。</span><span class="sxs-lookup"><span data-stu-id="7395c-172">Users’ emails.</span></span>
- <span data-ttu-id="7395c-173">[SharePoint](https://products.office.com/sharepoint/collaboration)、 [Microsoft OneDrive]( https://onedrive.live.com/about/)及[Microsoft OneNote](http://www.onenote.com/)文件。</span><span class="sxs-lookup"><span data-stu-id="7395c-173">Documents in [SharePoint](https://products.office.com/sharepoint/collaboration), [Microsoft OneDrive]( https://onedrive.live.com/about/) and [Microsoft OneNote](http://www.onenote.com/).</span></span>
- <span data-ttu-id="7395c-174">公用使用者可以存取 SharePoint、 OneDrive 或 OneNote 中的組織內的文件。</span><span class="sxs-lookup"><span data-stu-id="7395c-174">Public documents within the organization that users have access to in SharePoint, OneDrive, or OneNote.</span></span>

<span data-ttu-id="7395c-175">Microsoft Search 可確保只有存取與文件的權限的使用者可以看到 mined 從它的縮略字。</span><span class="sxs-lookup"><span data-stu-id="7395c-175">Microsoft Search makes sure that only users with access and permissions to a document can see the acronyms that are mined from it.</span></span> <span data-ttu-id="7395c-176">縮略字是 mined 從使用者的收件匣，並儲存在使用者晶怪。</span><span class="sxs-lookup"><span data-stu-id="7395c-176">The acronyms are mined from a user’s inbox and stored in the user shard.</span></span> <span data-ttu-id="7395c-177">只有該使用者可以存取使用者本身的收件匣 mined 縮略字。</span><span class="sxs-lookup"><span data-stu-id="7395c-177">Only the user can access the acronyms mined from the user’s own inbox.</span></span>

> [!NOTE]
> <span data-ttu-id="7395c-178">沒有 IT 系統管理員設定所需的生產縮略字。</span><span class="sxs-lookup"><span data-stu-id="7395c-178">No IT admin setup is needed for mined acronyms.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="7395c-179">常見問題集</span><span class="sxs-lookup"><span data-stu-id="7395c-179">Frequently asked questions</span></span>
<span data-ttu-id="7395c-180">**問： 如何編輯與生產資料的排名？**</span><span class="sxs-lookup"><span data-stu-id="7395c-180">**Q: How is editorial and mined data ranked?**</span></span>

<span data-ttu-id="7395c-181">**答：** 此功能目前排名上方生產縮略字編輯縮略字。</span><span class="sxs-lookup"><span data-stu-id="7395c-181">**A:** The feature currently ranks editorial acronyms above mined acronyms.</span></span>

<span data-ttu-id="7395c-182">**問： 如何長多久要發佈後要顯示在 Microsoft Search 的編輯縮略字？**</span><span class="sxs-lookup"><span data-stu-id="7395c-182">**Q: How long does it take for editorial acronyms to be visible in Microsoft Search after they’re published?**</span></span>

<span data-ttu-id="7395c-183">**答：** 花費最多三天的縮略字加入至已發佈狀態成為用於 Microsoft Search。</span><span class="sxs-lookup"><span data-stu-id="7395c-183">**A:**  It takes up  to three days for acronyms added to Published state to become available in Microsoft Search.</span></span> 

<span data-ttu-id="7395c-184">**問： 如何使用者會觸發縮略字回答？**</span><span class="sxs-lookup"><span data-stu-id="7395c-184">**Q: How do users trigger Acronyms answers?**</span></span>

<span data-ttu-id="7395c-185">**A**： 若要取得的縮略字解答，使用者必須在[Bing](https://bing.com)、 [Office 365](https://Office.com)或[SharePoint](https://products.office.com/sharepoint/collaboration) **搜尋**方塊中輸入特定的查詢模式。</span><span class="sxs-lookup"><span data-stu-id="7395c-185">**A**: To get Acronyms answers, users must enter specific query patterns in a [Bing](https://bing.com), [Office 365](https://Office.com), or [SharePoint](https://products.office.com/sharepoint/collaboration) **Search** box.</span></span> <span data-ttu-id="7395c-186">字詞*DNN*找到答案的查詢的範例如下所示：</span><span class="sxs-lookup"><span data-stu-id="7395c-186">Examples of queries that find answers for the term *DNN* are as follows:</span></span>

- <span data-ttu-id="7395c-187">*什麼是*DNN</span><span class="sxs-lookup"><span data-stu-id="7395c-187">*What is* DNN</span></span>
- <span data-ttu-id="7395c-188">*定義*DNN</span><span class="sxs-lookup"><span data-stu-id="7395c-188">*Define* DNN</span></span>
- <span data-ttu-id="7395c-189">DNN*定義*</span><span class="sxs-lookup"><span data-stu-id="7395c-189">DNN *definition*</span></span>
- <span data-ttu-id="7395c-190">*依序展開 [* DNN</span><span class="sxs-lookup"><span data-stu-id="7395c-190">*Expand* DNN</span></span>
- <span data-ttu-id="7395c-191">DNN*擴充*</span><span class="sxs-lookup"><span data-stu-id="7395c-191">DNN *expansion*</span></span>
- <span data-ttu-id="7395c-192">*代表的意義*DNN</span><span class="sxs-lookup"><span data-stu-id="7395c-192">*Meaning of* DNN</span></span>
- <span data-ttu-id="7395c-193">DNN*表示*</span><span class="sxs-lookup"><span data-stu-id="7395c-193">DNN *means*</span></span>

<span data-ttu-id="7395c-194">**問： 如何長多久要顯示在您接收或傳送新電子郵件或文件後的生產縮略字？**</span><span class="sxs-lookup"><span data-stu-id="7395c-194">**Q: How long does it take for mined acronyms to appear after you receive or send a new email or document?**</span></span>

<span data-ttu-id="7395c-195">**答：** 從新的電子郵件或文件的生產縮略字需要多達七天 Microsoft 搜尋結果中顯示。</span><span class="sxs-lookup"><span data-stu-id="7395c-195">**A:** Mined acronyms from a new email or document take up to seven days to appear in Microsoft Search results.</span></span>

<span data-ttu-id="7395c-196">**問： 是否需要位於採礦挑選備份的特定格式的文件？**</span><span class="sxs-lookup"><span data-stu-id="7395c-196">**Q: Do documents need to be in a specific format for mining to pick them up?**</span></span>

<span data-ttu-id="7395c-197">**答：**[否]。</span><span class="sxs-lookup"><span data-stu-id="7395c-197">**A:** No.</span></span> <span data-ttu-id="7395c-198">我們支援影像、 資料夾及 zip 檔案以外的所有檔案類型。</span><span class="sxs-lookup"><span data-stu-id="7395c-198">We support all file types except image, folders, and zip files.</span></span>

<span data-ttu-id="7395c-199">**問： 將 Microsoft 採擷從文件中的所有語言的縮略字嗎？**</span><span class="sxs-lookup"><span data-stu-id="7395c-199">**Q: Will Microsoft mine acronyms from documents in all languages?**</span></span>

<span data-ttu-id="7395c-200">**A**: Microsoft 僅支援從文件的採礦以英文顯示。</span><span class="sxs-lookup"><span data-stu-id="7395c-200">**A**: Microsoft only supports mining from documents in English.</span></span> <span data-ttu-id="7395c-201">將階段中新增其他語言的支援。</span><span class="sxs-lookup"><span data-stu-id="7395c-201">Support for other languages will be added in phases.</span></span>

<span data-ttu-id="7395c-202">**問： 如果我的組織不想要顯示生產的縮略字嗎？可以停止在搜尋結果中的顯示 [mined 縮略字嗎？**</span><span class="sxs-lookup"><span data-stu-id="7395c-202">**Q: What if my organization doesn’t want to show mined acronyms? Can I stop showing mined acronyms in search results?**</span></span>

<span data-ttu-id="7395c-203">**A**： 若要關閉搜尋結果中顯示 [mined 縮略字，建立客戶支援票證遵循在[連絡商務產品的技術支援](https://docs.microsoft.com/office365/admin/contact-support-for-business-products?redirectSourcePath=%252fen-us%252farticle%252fContact-Office-365-for-business-support-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b&view=o365-worldwide&tabs=online#BKMK_call_support)的指示進行。</span><span class="sxs-lookup"><span data-stu-id="7395c-203">**A**: To turn off showing mined acronyms in search results, create a customer support ticket by following the instructions at [Contact support for business products](https://docs.microsoft.com/office365/admin/contact-support-for-business-products?redirectSourcePath=%252fen-us%252farticle%252fContact-Office-365-for-business-support-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b&view=o365-worldwide&tabs=online#BKMK_call_support).</span></span>
<span data-ttu-id="7395c-204">建立支援票證之後，所花費達 48 小時停止出現在搜尋結果的生產縮略字。</span><span class="sxs-lookup"><span data-stu-id="7395c-204">After you create a support ticket, it takes up to 48 hours for mined acronyms to stop appearing in search results.</span></span> 

<span data-ttu-id="7395c-205">**問： 什麼時候會看到[Office 365](https://Office.com)和[SharePoint Online](https://products.office.com/sharepoint/collaboration)中的縮略字回答？**</span><span class="sxs-lookup"><span data-stu-id="7395c-205">**Q: When will I see Acronyms answers in [Office 365](https://Office.com) and [SharePoint Online](https://products.office.com/sharepoint/collaboration)?**</span></span>

<span data-ttu-id="7395c-206">**A**： 縮略字解答可用目前僅在 Microsoft [Bing](https://bing.com)搜尋。</span><span class="sxs-lookup"><span data-stu-id="7395c-206">**A**: Acronyms answers are currently only available in Microsoft Search in [Bing](https://bing.com).</span></span> <span data-ttu-id="7395c-207">他們會被導入至 Office 365 和 SharePoint Online 中 2020年。</span><span class="sxs-lookup"><span data-stu-id="7395c-207">They’ll be rolled out to Office 365 and SharePoint Online in 2020.</span></span>
