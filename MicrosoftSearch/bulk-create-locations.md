---
title: 大量建立位置
ms.author: dawholl
author: dawholl
manager: kellis
ms.date: 12/18/2018
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: 15c9fada-f7a6-4210-aa6b-028b32217830
ROBOTS: NoIndex
description: 使用 Microsoft Search 系統管理入口網站的匯入工具一次新增許多位置
ms.openlocfilehash: 186f6973de1ff87b62b5f07a47eb41acdd842010
ms.sourcegitcommit: be2e837d9b087bffe6ce40d72d7ae58a8fcdf3fe
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/30/2019
ms.locfileid: "34591393"
---
# <a name="bulk-create-locations"></a><span data-ttu-id="639db-103">大量建立位置</span><span class="sxs-lookup"><span data-stu-id="639db-103">Bulk create locations</span></span>

> [!IMPORTANT]
> <span data-ttu-id="639db-104">本文章適用 Bing 系統管理入口網站中的 Microsoft Search。</span><span class="sxs-lookup"><span data-stu-id="639db-104">This article applies to the Microsoft Search in Bing admin portal.</span></span> <span data-ttu-id="639db-105">我們正在將入口網站移至 Microsoft 365 系統管理中心，完成之後入口網站將會移除。</span><span class="sxs-lookup"><span data-stu-id="639db-105">We’re moving the portal to the Microsoft 365 admin center, and then it will be removed.</span></span> <span data-ttu-id="639db-106">我們建議您使用 Microsoft 365 系統管理中心開始。</span><span class="sxs-lookup"><span data-stu-id="639db-106">We recommend that you use the Microsoft 365 admin center to get started.</span></span> <span data-ttu-id="639db-107">[Microsoft Search 概觀](overview-microsoft-search.md)。</span><span class="sxs-lookup"><span data-stu-id="639db-107">[Overview of Microsoft Graph](overview-microsoft-search.md)</span></span>
    
<span data-ttu-id="639db-108">下載並使用 .csv 範本以大量建立、編輯和儲存位置。</span><span class="sxs-lookup"><span data-stu-id="639db-108">Download and use the .csv template to bulk create, edit, and save locations.</span></span> 
  
1. <span data-ttu-id="639db-109">在 [位置] 區段右上角，按一下 [匯入]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="639db-109">In the upper-right corner of the Locations section, click **Import**</span></span>
    
2. <span data-ttu-id="639db-110">按一下 [下載位置範本 (.csv)]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="639db-110">Click **Download locations template (.csv)**</span></span>
    
3. <span data-ttu-id="639db-111">儲存並開啟 .csv 檔案</span><span class="sxs-lookup"><span data-stu-id="639db-111">Save and open the .csv file</span></span>
    
4. <span data-ttu-id="639db-112">新增位置內容，然後儲存檔案</span><span class="sxs-lookup"><span data-stu-id="639db-112">Add the location content and save the file</span></span>

    <span data-ttu-id="639db-113">您應該將 .csv 檔案儲存為 CSV UTF-8 檔案，其他檔案類型和/或編碼可能會造成匯入錯誤</span><span class="sxs-lookup"><span data-stu-id="639db-113">The .csv file should be saved as a CSV UTF-8 file, other file types and or encodings may cause import errors</span></span>
    
5. <span data-ttu-id="639db-114">在 [位置] 區段右上角，按一下 [匯入]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="639db-114">In the upper-right corner of the Locations section, click **Import**</span></span>
    
6. <span data-ttu-id="639db-115">在 [匯入位置] 窗格中，按一下 [瀏覽]\*\*\*\*，然後瀏覽至您要匯入的 .csv 檔案</span><span class="sxs-lookup"><span data-stu-id="639db-115">In the Import locations pane, click **Browse** and navigate to the .csv file you want to import</span></span> 
    
7. <span data-ttu-id="639db-116">按一下 [匯入]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="639db-116">Click **Import**.</span></span>

<span data-ttu-id="639db-117">匯入和匯出位置範本中的欄位都是一樣的。</span><span class="sxs-lookup"><span data-stu-id="639db-117">The fields in the import and export locations templates are the same.</span></span> <span data-ttu-id="639db-118">您可以匯出、大量編輯，再匯入編輯，或使用空白範本從頭開始大量建立新的位置。</span><span class="sxs-lookup"><span data-stu-id="639db-118">You can export, bulk edit, and import the edits, or start with an empty template to bulk create new locations.</span></span> <span data-ttu-id="639db-119">若要大量編輯現有的位置，請從系統管理入口網站中匯出、進行所需編輯，然後再匯入它們。</span><span class="sxs-lookup"><span data-stu-id="639db-119">To bulk edit existing locations, export them from the Admin portal, make the necessary edits, and then import them.</span></span>

# <a name="prevent-import-errors"></a><span data-ttu-id="639db-120">防止匯入錯誤</span><span class="sxs-lookup"><span data-stu-id="639db-120">Prevent import errors</span></span>  
<span data-ttu-id="639db-121">如果有任何必要資料遺失或無效，您就會收到錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="639db-121">You'll get an error if any required data is missing or invalid.</span></span> <span data-ttu-id="639db-122">依據錯誤的類型，系統可能會產生一份記錄檔，其中包含哪些列或欄需要修正的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="639db-122">Depending on the error, a log file may be generated with more information about the rows and columns that need to be corrected.</span></span> <span data-ttu-id="639db-123">進行任何所需編輯，然後再次嘗試匯入檔案。</span><span class="sxs-lookup"><span data-stu-id="639db-123">Make any necessary edits, and try importing the file again.</span></span>
  
> [!NOTE]
> <span data-ttu-id="639db-124">直到解決所有的錯誤之前，您無法建立或編輯任何位置。</span><span class="sxs-lookup"><span data-stu-id="639db-124">Until all errors are resolved, you can't create or edit any locations.</span></span> 

<span data-ttu-id="639db-125">若要避免錯誤，請確定您匯入的檔案的格式正確：</span><span class="sxs-lookup"><span data-stu-id="639db-125">To help prevent errors, make sure your import file is properly formatted:</span></span>
- <span data-ttu-id="639db-126">包含匯入範本中的標題列</span><span class="sxs-lookup"><span data-stu-id="639db-126">Includes the header row that was in the import template</span></span>
- <span data-ttu-id="639db-127">包含匯入範本中的所有欄</span><span class="sxs-lookup"><span data-stu-id="639db-127">Includes all columns that were in the import template</span></span>
- <span data-ttu-id="639db-128">欄順序與匯入範本相同</span><span class="sxs-lookup"><span data-stu-id="639db-128">The column order is the same as the import template</span></span>
- <span data-ttu-id="639db-129">這些欄可以空白：識別碼、上次修改日期、上次修改者，以及經度/緯度</span><span class="sxs-lookup"><span data-stu-id="639db-129">These columns can be empty: Id, Last Modified, Last Modified By, and Lat/Long</span></span>  
<span data-ttu-id="639db-130">如果經度/緯度欄位空白，我們會根據地址嘗試判斷</span><span class="sxs-lookup"><span data-stu-id="639db-130">We'll try to determine lat/long based on the address if that field is empty</span></span>
- <span data-ttu-id="639db-131">[狀態] 欄不能空白，此為必要資訊</span><span class="sxs-lookup"><span data-stu-id="639db-131">The State column can't be empty, this information is required</span></span>  
<span data-ttu-id="639db-132">位置會根據 [狀態] 欄位的不同而儲存成草稿、建議、已排程或自動發佈。</span><span class="sxs-lookup"><span data-stu-id="639db-132">Based on the State field, locations will be saved as draft, suggested, scheduled, or they will be published automatically.</span></span>

<span data-ttu-id="639db-133">同時，如果您包含現有位置的識別碼，將會以匯入檔案中的資訊加以取代。</span><span class="sxs-lookup"><span data-stu-id="639db-133">Also, if you include the Id of an existing location, it will be replaced with the information in the import file.</span></span>

<span data-ttu-id="639db-134">針對具有多個租用戶的組織，您可以從一個租用戶匯出您的位置，並將它匯入到另一個租用戶。</span><span class="sxs-lookup"><span data-stu-id="639db-134">For organizations with mulitple tenants, you can export your locations from one tenant and import it into another.</span></span> <span data-ttu-id="639db-135">但您必須在匯入之前，先移除 [識別碼] 欄中的所有資料。</span><span class="sxs-lookup"><span data-stu-id="639db-135">But you must remove all of the data in the Id column before you import.</span></span>
  
<span data-ttu-id="639db-136">若要深入了解必要欄位與建議欄位，請參閱[新增位置](add-a-location.md)。</span><span class="sxs-lookup"><span data-stu-id="639db-136">To find out more about required and recommended fields, see [Add a location](add-a-location.md).</span></span>

  

