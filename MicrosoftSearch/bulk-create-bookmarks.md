---
title: 大量建立書籤
ms.author: dawholl
author: dawholl
manager: kellis
ms.date: 09/11/2018
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: def300e7-103c-4e92-a062-28ffa27561d7
description: 使用 Microsoft Search 系統管理入口網站的匯入工具一次建立許多書籤
ms.openlocfilehash: 560cda6f94060d428f2d18cc61bd2430cb31b474
ms.sourcegitcommit: 3e91a6e70b48a0100adfed1b62ba79f2fd1735d2
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/13/2019
ms.locfileid: "34425650"
---
# <a name="bulk-create-bookmarks"></a><span data-ttu-id="44c2f-103">大量建立書籤</span><span class="sxs-lookup"><span data-stu-id="44c2f-103">Bulk create bookmarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="44c2f-104">Bing 設定中的 Microsoft Search 現在可以在 Microsoft 365 管理中心中使用。</span><span class="sxs-lookup"><span data-stu-id="44c2f-104">Microsoft Search in Bing settings are now available in the Microsoft 365 admin center.</span></span> <span data-ttu-id="44c2f-105">從系統管理中心的[指派搜尋系統管理員](https://docs.microsoft.com/zh-TW/microsoftsearch/setup-microsoft-search#step-2-assign-search-admin-and-search-editor)開始。</span><span class="sxs-lookup"><span data-stu-id="44c2f-105">Get started by [assigning search admins](https://docs.microsoft.com/en-us/microsoftsearch/setup-microsoft-search#step-2-assign-search-admin-and-search-editor) in your admin center.</span></span>
    
<span data-ttu-id="44c2f-106">下載並使用 .csv 範本以大量建立、編輯和儲存書籤。</span><span class="sxs-lookup"><span data-stu-id="44c2f-106">Download and use the .csv template to bulk create, edit, and save bookmarks.</span></span> <span data-ttu-id="44c2f-107">若要大量編輯現有的書籤，請從系統管理入口網站中匯出、進行所需編輯，然後再匯入它們。</span><span class="sxs-lookup"><span data-stu-id="44c2f-107">To bulk edit existing bookmarks, export them from the Admin portal, make the necessary edits, and then import them.</span></span>
  
1. <span data-ttu-id="44c2f-108">按一下 [書籤] 區段右上角的 [匯入]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="44c2f-108">In the upper-right corner of the Bookmarks section, click **Import**</span></span>
    
2. <span data-ttu-id="44c2f-109">按一下 [下載書籤範本 (.csv)]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="44c2f-109">Click **Download bookmarks template (.csv)**</span></span>
    
3. <span data-ttu-id="44c2f-110">儲存並開啟 .csv 檔案</span><span class="sxs-lookup"><span data-stu-id="44c2f-110">Save and open the .csv file</span></span>
    
4. <span data-ttu-id="44c2f-111">新增書籤內容和設定，然後儲存檔案</span><span class="sxs-lookup"><span data-stu-id="44c2f-111">Add the bookmark content and settings and save the file</span></span>

    <span data-ttu-id="44c2f-112">您應該將 .csv 檔案儲存為 CSV UTF-8 檔案，其他檔案類型和或編碼可能造成匯入錯誤</span><span class="sxs-lookup"><span data-stu-id="44c2f-112">The .csv file should be saved as a CSV UTF-8 file, other file types and or encodings may cause import errors</span></span>
    
5. <span data-ttu-id="44c2f-113">按一下 [書籤] 區段右上角的 [匯入]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="44c2f-113">In the upper-right corner of the Bookmarks section, click **Import**</span></span>
    
6. <span data-ttu-id="44c2f-114">在 [匯入書籤] 窗格中，按一下 [瀏覽]\*\*\*\*，然後瀏覽至您要匯入的 .csv 檔案</span><span class="sxs-lookup"><span data-stu-id="44c2f-114">In the Import bookmarks pane, click **Browse** and navigate to the .csv file you want to import</span></span> 
    
7. <span data-ttu-id="44c2f-115">按一下 [匯入]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="44c2f-115">Click **Import**.</span></span>

# <a name="prevent-import-errors"></a><span data-ttu-id="44c2f-116">防止匯入錯誤</span><span class="sxs-lookup"><span data-stu-id="44c2f-116">Prevent import errors</span></span>      
<span data-ttu-id="44c2f-117">如果有任何必要資訊缺失或無效，您會收到錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="44c2f-117">You'll get an error if any required data is missing or invalid.</span></span> <span data-ttu-id="44c2f-118">依據錯誤的類型，系統可能會產生一份記錄檔，其中包含哪些列或欄需要修正的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="44c2f-118">Depending on the error, a log file may be generated with more information about the rows and columns that need to be corrected.</span></span> <span data-ttu-id="44c2f-119">進行任何所需編輯，然後再次嘗試匯入檔案。</span><span class="sxs-lookup"><span data-stu-id="44c2f-119">Make any necessary edits, and try importing the file again.</span></span>

> [!NOTE]
> <span data-ttu-id="44c2f-120">直到解決所有的錯誤之前，您無法建立或編輯任何書籤。</span><span class="sxs-lookup"><span data-stu-id="44c2f-120">Until all errors are resolved, you can't create or edit any bookmarks.</span></span> 

<span data-ttu-id="44c2f-121">若要避免錯誤，請確定您匯入的檔案的格式正確：</span><span class="sxs-lookup"><span data-stu-id="44c2f-121">To help prevent errors, make sure your import file is properly formatted:</span></span>
- <span data-ttu-id="44c2f-122">包含匯入範本中的標題列</span><span class="sxs-lookup"><span data-stu-id="44c2f-122">Includes the header row that was in the import template</span></span>
- <span data-ttu-id="44c2f-123">包含匯入範本中的欄位</span><span class="sxs-lookup"><span data-stu-id="44c2f-123">Includes all columns that were in the import template</span></span>
- <span data-ttu-id="44c2f-124">欄位順序與匯入範本相同</span><span class="sxs-lookup"><span data-stu-id="44c2f-124">The column order is the same as the import template</span></span>
- <span data-ttu-id="44c2f-125">永不編輯這些欄位中的資料：[識別碼]、[上次修改日期]，以及 [上次修改者]</span><span class="sxs-lookup"><span data-stu-id="44c2f-125">These columns can be empty: Id, Last Modified, and Last Modified By</span></span>
- <span data-ttu-id="44c2f-126">[狀態] 欄位不能為空白，這是必要資訊</span><span class="sxs-lookup"><span data-stu-id="44c2f-126">The State column can't be empty, this information is required</span></span>  
<span data-ttu-id="44c2f-127">書籤會根據 [狀態] 欄位的不同而儲存成草稿、建議、已排程或自動發佈。</span><span class="sxs-lookup"><span data-stu-id="44c2f-127">Based on the State field, bookmarks will be saved as draft, suggested, scheduled, or they will be published automatically.</span></span>

<span data-ttu-id="44c2f-128">同時，如果您包含現有書籤的識別碼，將會以匯入檔案中的資訊加以取代。</span><span class="sxs-lookup"><span data-stu-id="44c2f-128">Also, if you include the Id of an existing bookmark, it will be replaced with the information in the import file.</span></span>

<span data-ttu-id="44c2f-129">針對具有多個租用戶的組織，您可以從一個租用戶匯出您的書籤，並將它匯入到另一個租用戶。</span><span class="sxs-lookup"><span data-stu-id="44c2f-129">For organizations with mulitple tenants, you can export your bookmarks from one tenant and import it into another.</span></span> <span data-ttu-id="44c2f-130">但您必須在匯入之前，先移除 [識別碼] 欄位中的資料。</span><span class="sxs-lookup"><span data-stu-id="44c2f-130">But you must remove all of the data in the Id column before you import.</span></span>

<span data-ttu-id="44c2f-131">若要深入了解必要欄位與建議欄位，請參閱[建立書籤](create-bookmarks.md)。</span><span class="sxs-lookup"><span data-stu-id="44c2f-131">To find out more about required and recommended fields, see [Create bookmarks](create-bookmarks.md).</span></span>
