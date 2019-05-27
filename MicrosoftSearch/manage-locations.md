---
title: 管理位置
ms.author: dawholl
author: dawholl
manager: kellis
ms.date: 11/08/2018
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
ms.openlocfilehash: 0e23cf3d3d3d05fe86cdc3e09ce808e54242d670
ms.sourcegitcommit: 3e91a6e70b48a0100adfed1b62ba79f2fd1735d2
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/13/2019
ms.locfileid: "34425656"
---
# <a name="manage-locations"></a><span data-ttu-id="de478-103">管理位置</span><span class="sxs-lookup"><span data-stu-id="de478-103">Manage federated locations</span></span>

> [!IMPORTANT]
> <span data-ttu-id="de478-104">Bing 中的 Microsoft Search 設定現在可在 Microsoft 365 系統管理中心取得。</span><span class="sxs-lookup"><span data-stu-id="de478-104">Microsoft Search in Bing settings are now available in the Microsoft 365 admin center.</span></span> <span data-ttu-id="de478-105">從在系統管理中心[指派搜尋系統管理員](https://docs.microsoft.com/zh-TW/microsoftsearch/setup-microsoft-search#step-2-assign-search-admin-and-search-editor)開始。</span><span class="sxs-lookup"><span data-stu-id="de478-105">Get started by [assigning search admins](https://docs.microsoft.com/en-us/microsoftsearch/setup-microsoft-search#step-2-assign-search-admin-and-search-editor) in your admin center.</span></span>
    
<span data-ttu-id="de478-106">隨著時間，您可能會需要更新位置的狀態和內容以讓它保持相關。</span><span class="sxs-lookup"><span data-stu-id="de478-106">Over time, you may need to update a location's status and content to keep it relevant.</span></span> 
  
## <a name="filter-locations"></a><span data-ttu-id="de478-107">篩選位置</span><span class="sxs-lookup"><span data-stu-id="de478-107">Filter locations</span></span>

<span data-ttu-id="de478-108">使用位置頁面右上角的篩選選項，來依據日期與修改者尋找位置。</span><span class="sxs-lookup"><span data-stu-id="de478-108">Use the filter option in the upper-right corner of the Locations page to find locations by date and see who modified them.</span></span> <span data-ttu-id="de478-109">例如，將日期滑桿設定為 30 天，並選取系統管理員或編輯者，以查看該人員在該段期間內建立或變更的位置清單。</span><span class="sxs-lookup"><span data-stu-id="de478-109">For example, set the date slider to 30 days and select an admin or editor to see the list of locations they've created or changed during that time.</span></span>
  
## <a name="change-location-content"></a><span data-ttu-id="de478-110">變更位置內容</span><span class="sxs-lookup"><span data-stu-id="de478-110">Change location content</span></span>

1. <span data-ttu-id="de478-111">移至 Microsoft Search 系統管理入口網站</span><span class="sxs-lookup"><span data-stu-id="de478-111">Go to the Microsoft Search Admin portal</span></span>
    
2. <span data-ttu-id="de478-112">在瀏覽窗格中，按一下 [位置]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="de478-112">In the navigation pane, click **ADSI Edit**.</span></span>
    
3. <span data-ttu-id="de478-113">若要尋找位置，請搜尋、篩選或按一下位置狀態，以縮小您的結果</span><span class="sxs-lookup"><span data-stu-id="de478-113">To find a location, search, filter, or click a location status to narrow your results</span></span>
    
4. <span data-ttu-id="de478-114">若要變更或更新位置，請按一下位置名稱</span><span class="sxs-lookup"><span data-stu-id="de478-114">To change or update a location, click the location name</span></span>
    
5. <span data-ttu-id="de478-115">對內容進行任何變更或更新，並預覽其顯示方式</span><span class="sxs-lookup"><span data-stu-id="de478-115">Make any changes or updates to the content and preview how they'll appear</span></span> 
    
6. <span data-ttu-id="de478-116">按一下 [儲存]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="de478-116">Click **Save**</span></span>
    
## <a name="bulk-export-and-edit-locations"></a><span data-ttu-id="de478-117">大量匯出和編輯位置</span><span class="sxs-lookup"><span data-stu-id="de478-117">Bulk export and edit locations</span></span>

<span data-ttu-id="de478-118">請勿編輯這些欄位中的資料：</span><span class="sxs-lookup"><span data-stu-id="de478-118">Never edit data in these fields:</span></span>
  
- <span data-ttu-id="de478-119">識別碼</span><span class="sxs-lookup"><span data-stu-id="de478-119">Id</span></span>
    
- <span data-ttu-id="de478-120">上次修改日期</span><span class="sxs-lookup"><span data-stu-id="de478-120">Last modified</span></span>
    
- <span data-ttu-id="de478-121">上次修改者</span><span class="sxs-lookup"><span data-stu-id="de478-121">Last modified by</span></span>
    
<span data-ttu-id="de478-122">識別碼是每個位置的唯一識別碼，請不要編輯。</span><span class="sxs-lookup"><span data-stu-id="de478-122">Id is a unique identifier for each location and should never be edited.</span></span> <span data-ttu-id="de478-123">[上次修改日期] 和 [上次修改者] 欄位只應用來排序和尋找位置。</span><span class="sxs-lookup"><span data-stu-id="de478-123">The Last Modified and Last Modified By fields should only be used to sort and find locations.</span></span>
  
1. <span data-ttu-id="de478-124">如果您想要匯出位置的子集，請篩選它們</span><span class="sxs-lookup"><span data-stu-id="de478-124">If you want to export a subset of your locations, filter them</span></span>
    
2. <span data-ttu-id="de478-125">按一下 [位置] 頁面右上角的 [匯出]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="de478-125">In the upper-right corner of the Locations page, click **Export**</span></span>
    
3. <span data-ttu-id="de478-126">儲存或開啟 .csv 檔案</span><span class="sxs-lookup"><span data-stu-id="de478-126">Save or open the .csv file</span></span>
    
4. <span data-ttu-id="de478-127">編輯任何欄位中的資料：</span><span class="sxs-lookup"><span data-stu-id="de478-127">Edit data in any of these fields:</span></span>
    
   - <span data-ttu-id="de478-128">名稱</span><span class="sxs-lookup"><span data-stu-id="de478-128">Name</span></span>
    
   - <span data-ttu-id="de478-129">地址行 1</span><span class="sxs-lookup"><span data-stu-id="de478-129">Address Line 1, City, State/Province, ZIP/Postal Code</span></span>
    
   - <span data-ttu-id="de478-130">地址行 2</span><span class="sxs-lookup"><span data-stu-id="de478-130">Address Line 2</span></span>
    
   - <span data-ttu-id="de478-131">城市</span><span class="sxs-lookup"><span data-stu-id="de478-131">City</span></span>
    
   - <span data-ttu-id="de478-132">地址縣/市</span><span class="sxs-lookup"><span data-stu-id="de478-132">Other Address State</span></span>
    
   - <span data-ttu-id="de478-133">郵遞區號</span><span class="sxs-lookup"><span data-stu-id="de478-133">Zip or Postal Code</span></span>
    
   - <span data-ttu-id="de478-134">國家/地區</span><span class="sxs-lookup"><span data-stu-id="de478-134">Country</span></span>
    
   - <span data-ttu-id="de478-135">完整地址</span><span class="sxs-lookup"><span data-stu-id="de478-135">Full Address</span></span>
    
   - <span data-ttu-id="de478-136">緯度</span><span class="sxs-lookup"><span data-stu-id="de478-136">Residence Latitude</span></span>
    
   - <span data-ttu-id="de478-137">經度</span><span class="sxs-lookup"><span data-stu-id="de478-137">Residence Longitude</span></span>
    
   - <span data-ttu-id="de478-138">關鍵字</span><span class="sxs-lookup"><span data-stu-id="de478-138">Keywords</span></span>
    
   - <span data-ttu-id="de478-139">保留的關鍵字</span><span class="sxs-lookup"><span data-stu-id="de478-139">Reserved keywords</span></span>
    
   - <span data-ttu-id="de478-140">狀態</span><span class="sxs-lookup"><span data-stu-id="de478-140">State</span></span>
    
5. <span data-ttu-id="de478-141">儲存 .csv 檔案</span><span class="sxs-lookup"><span data-stu-id="de478-141">Save the file as a .csv or .txt file.</span></span>

    <span data-ttu-id="de478-142">您應該將 .csv 檔案儲存為 CSV UTF-8 檔案，其他檔案類型和或編碼可能造成匯入錯誤</span><span class="sxs-lookup"><span data-stu-id="de478-142">The .csv file should be saved as a CSV UTF-8 file, other file types and or encodings may cause import errors</span></span>
    
6. <span data-ttu-id="de478-143">按一下 [位置] 頁面右上角的 [匯入]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="de478-143">In the upper-right corner of the Locations page, click **Import**</span></span>
    
7. <span data-ttu-id="de478-144">在 [匯入位置] 窗格中，按一下 [瀏覽]\*\*\*\*，並選取編輯的 .csv 檔案</span><span class="sxs-lookup"><span data-stu-id="de478-144">In the Import locations pane, click **Browse** and select the edited .csv file</span></span> 
    
8. <span data-ttu-id="de478-145">按一下 [匯入]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="de478-145">Click **Import**.</span></span>

  

