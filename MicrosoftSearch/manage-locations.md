---
title: 管理位置
ms.author: dawholl
author: dawholl
manager: kellis
ms.date: 05/30/2019
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: 8ab9aa00-cd74-405f-8410-9a1c3cfacdb9
description: 隨著時間，您可能會需要更新位置的狀態和內容以讓它保持相關。
ms.openlocfilehash: d026e518011f3b3739beb2b6aaa044f8a5e9c0d4
ms.sourcegitcommit: be2e837d9b087bffe6ce40d72d7ae58a8fcdf3fe
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/30/2019
ms.locfileid: "34591555"
---
# <a name="manage-locations"></a><span data-ttu-id="d8457-103">管理位置</span><span class="sxs-lookup"><span data-stu-id="d8457-103">Manage federated locations</span></span>

## <a name="location"></a><span data-ttu-id="d8457-104">位置</span><span class="sxs-lookup"><span data-stu-id="d8457-104">Location</span></span>
<span data-ttu-id="d8457-105">位置利用提供辦公室、校區和大樓的準確位置以及方向和導覽，可協助使用者尋找地址並找到組織的大樓。</span><span class="sxs-lookup"><span data-stu-id="d8457-105">Location helps your users find addresses and locate your organization's buildings by providing an accurate location for offices, campuses, and buildings, along with directions and navigation.</span></span> <span data-ttu-id="d8457-106">系統管理員應該新增組織的所有重要位置。</span><span class="sxs-lookup"><span data-stu-id="d8457-106">Administrators should add all important locations of your organization.</span></span> <span data-ttu-id="d8457-107">與書籤和問與答不同，索引不會立即更新，並且需要數小時的時間，新增或變更的位置才會顯示在搜尋結果中。</span><span class="sxs-lookup"><span data-stu-id="d8457-107">Unlike Bookmarks and Q&A, the index is not refreshed immediately, and it can take several hours for new or changed locations to appear in search results.</span></span>

### <a name="add-or-edit-a-single-location"></a><span data-ttu-id="d8457-108">新增或編輯單一位置</span><span class="sxs-lookup"><span data-stu-id="d8457-108">Add or edit a single location</span></span>
1. <span data-ttu-id="d8457-109">移至 **Microsoft 365 系統管理中心**。</span><span class="sxs-lookup"><span data-stu-id="d8457-109">Go to the Microsoft 365 admin center.</span></span>
1. <span data-ttu-id="d8457-110">在功能窗格中，移至 [設定]\*\*\*\*，然後選取 **Microsoft Search**。</span><span class="sxs-lookup"><span data-stu-id="d8457-110">In the navigation pane, go to **Settings** and select **Microsoft Search**.</span></span>
1. <span data-ttu-id="d8457-111">選取 [位置]\*\*\*\* 索引標籤。依預設，會在 [Microsoft Search ]\*\*\*\* 頁面上選取 [書籤]\*\*\*\* 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="d8457-111">Select **Locations** tab. By default, the **Bookmarks** tab is selected on the **Microsoft Search** page.</span></span>
1. <span data-ttu-id="d8457-112">若要新增新的位置，請選取 [新增]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="d8457-112">To add a new location, select **Add new**.</span></span>
1. <span data-ttu-id="d8457-113">若要編輯位置，請在相關的位置清單中選取該位置。</span><span class="sxs-lookup"><span data-stu-id="d8457-113">To edit a location, select the location in the relevant locations list.</span></span>
1. <span data-ttu-id="d8457-114">當您新增或編輯資訊時，預覽會自動更新。</span><span class="sxs-lookup"><span data-stu-id="d8457-114">As you add or edit the information, the preview automatically updates.</span></span>
1. <span data-ttu-id="d8457-115">儲存變更。</span><span class="sxs-lookup"><span data-stu-id="d8457-115">Save your changes.</span></span>

### <a name="bulk-add-or-edit-locations"></a><span data-ttu-id="d8457-116">大量新增或編輯位置</span><span class="sxs-lookup"><span data-stu-id="d8457-116">Bulk add or edit locations</span></span>
<span data-ttu-id="d8457-117">系統管理員可以使用匯入或匯出功能來大量新增或編輯位置。</span><span class="sxs-lookup"><span data-stu-id="d8457-117">Administrators can use the Import or Export feature to bulk add or edit locations.</span></span> 

<span data-ttu-id="d8457-118">使用匯入/匯出功能，以便：</span><span class="sxs-lookup"><span data-stu-id="d8457-118">Use the import/export feature to:</span></span>
1. <span data-ttu-id="d8457-119">大量新增位置 - 在位置範本檔案中新增詳細資料，然後將它匯入。</span><span class="sxs-lookup"><span data-stu-id="d8457-119">Bulk add location - Add details in the location template file, and then import it.</span></span> 
1. <span data-ttu-id="d8457-120">大量編輯位置 - 將位置匯出至 .csv 檔案，然後編輯匯出的 .csv 檔案中位置的詳細資料，然後匯入更新的 .csv 檔案。</span><span class="sxs-lookup"><span data-stu-id="d8457-120">Bulk edit locations - Export locations to a .csv file, then edit the location details in the exported .csv file, and then import the updated .csv file.</span></span>
1. <span data-ttu-id="d8457-121">備份位置 - 將現有位置匯出至 .csv 檔案。</span><span class="sxs-lookup"><span data-stu-id="d8457-121">Backups Locations – Export existing locations to a .csv file.</span></span>

<span data-ttu-id="d8457-122">若要匯出或匯入位置：</span><span class="sxs-lookup"><span data-stu-id="d8457-122">To export or import locations:</span></span>
1. <span data-ttu-id="d8457-123">在 [位置]\*\*\*\* 索引標籤的右上角，選取 [匯入]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="d8457-123">In the upper-right corner of the **Locations** tab, select **Import**.</span></span>
<span data-ttu-id="d8457-124">選取 [匯出]\*\*\*\* 來下載 .csv 檔案中的現有位置。</span><span class="sxs-lookup"><span data-stu-id="d8457-124">Select **Export** to download the existing locations in a .csv file.</span></span>
1. <span data-ttu-id="d8457-125">在右窗格中，選擇使用 .csv 檔案匯入的選項。</span><span class="sxs-lookup"><span data-stu-id="d8457-125">In the right pane, choose the option to import using a .csv file.</span></span> <span data-ttu-id="d8457-126">下載範本檔案以取得必要欄位的清單和詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d8457-126">Download ehe template file for a list of the required fields and details.</span></span>
1. <span data-ttu-id="d8457-127">在範本檔案中新增或編輯位置詳細資料，然後將它儲存在您的電腦上。</span><span class="sxs-lookup"><span data-stu-id="d8457-127">Add or edit location details in the template file, and then save it on your computer.</span></span> 
1. <span data-ttu-id="d8457-128">在 [匯入位置]\*\*\*\* 窗格中，選取 [瀏覽]\*\*\*\*，然後選取您要匯入的 .csv 檔案。</span><span class="sxs-lookup"><span data-stu-id="d8457-128">In the **Import** locations pane, select **Browse**, and then the .csv file that you want to import.</span></span>
1. <span data-ttu-id="d8457-129">選取 [匯入]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="d8457-129">Select **Import**.</span></span>

<span data-ttu-id="d8457-130">以下是有關範本檔案的一些重點：</span><span class="sxs-lookup"><span data-stu-id="d8457-130">Here are some important points regarding the template file:</span></span>
- <span data-ttu-id="d8457-131">永不編輯這些欄位中的資料：*識別碼*、*上次修改日期*，以及*上次修改者*</span><span class="sxs-lookup"><span data-stu-id="d8457-131">Never edit data in these fields: *Id*, *Last Modified*, and *Last Modified By*</span></span>
- <span data-ttu-id="d8457-132">如果您包含現有書籤的*識別碼*，將會以匯入檔案中的資訊加以取代。</span><span class="sxs-lookup"><span data-stu-id="d8457-132">If you include the *Id* of an existing bookmark, it will be replaced with the information in the import file.</span></span>
- <span data-ttu-id="d8457-133">如果有一個現有的書籤具有相同標題或 URL，則會以匯入檔案中的資訊更新書籤。</span><span class="sxs-lookup"><span data-stu-id="d8457-133">If there is an existing bookmark with the same title or URL, the bookmark will be updated with information in the import file.</span></span>
- <span data-ttu-id="d8457-134">範本檔案中並非所有欄位都為必要，必要欄位則會依據書籤的狀態而改變。</span><span class="sxs-lookup"><span data-stu-id="d8457-134">Not all fields in the template file are required and required fields vary depending on the bookmark state.</span></span>
- <span data-ttu-id="d8457-135">書籤會根據 [狀態]\*\* 欄位的不同而儲存成草稿、建議、已排程或自動發佈。</span><span class="sxs-lookup"><span data-stu-id="d8457-135">Based on the *State* field, bookmarks will be saved as draft, suggested, scheduled, or they will be published automatically.</span></span>
- <span data-ttu-id="d8457-136">針對具有多個租用戶的組織，您可以從一個租用戶匯出您的書籤，並將它匯入到另一個租用戶。</span><span class="sxs-lookup"><span data-stu-id="d8457-136">For organizations with multiple tenants, you can export your bookmarks from one tenant and import it into another.</span></span> <span data-ttu-id="d8457-137">但您必須在匯入之前，先移除 [識別碼]\*\* 資料行中的資料。</span><span class="sxs-lookup"><span data-stu-id="d8457-137">But you must remove the data in the *Id* column before you import.</span></span>

<span data-ttu-id="d8457-138">**附註：** 如果範本檔案中有任何錯誤，您即無法匯入位置。</span><span class="sxs-lookup"><span data-stu-id="d8457-138">**Note:** You cannot import Locations if there are any errors in the template file.</span></span> <span data-ttu-id="d8457-139">若要避免錯誤，請確定您匯入的檔案的格式正確，並包含所有必要的資訊。</span><span class="sxs-lookup"><span data-stu-id="d8457-139">To prevent errors, make sure your import file is properly formatted and include all the required information.</span></span> 

<span data-ttu-id="d8457-140">如需如何避免錯誤的詳細資訊，請參閱[防止匯入錯誤](manage-bookmarks.md#prevent-import-errors)。</span><span class="sxs-lookup"><span data-stu-id="d8457-140">For more information on how to prevent error, see [Prevent import errors](manage-bookmarks.md#prevent-import-errors).</span></span>
