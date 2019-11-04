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
ROBOTS: NoIndex
description: 與 Microsoft Search 系統管理入口網站中的匯入工具一次建立大量的書籤
ms.openlocfilehash: 2983a47a8761a2463b25497911024f9bfd069369
ms.sourcegitcommit: bfcab9d42e93addccd1e3875b41bc9cc1b6986cc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2019
ms.locfileid: "37948922"
---
# <a name="bulk-create-bookmarks"></a><span data-ttu-id="c90fd-103">大量建立書籤</span><span class="sxs-lookup"><span data-stu-id="c90fd-103">Bulk create bookmarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c90fd-104">本文章適用 Bing 系統管理入口網站中的 Microsoft Search。</span><span class="sxs-lookup"><span data-stu-id="c90fd-104">This article applies to the Microsoft Search in Bing admin portal.</span></span> <span data-ttu-id="c90fd-105">我們正在將入口網站移至 Microsoft 365 系統管理中心，完成之後將會移除 Bing 系統管理入口網站中的 Microsoft Search。</span><span class="sxs-lookup"><span data-stu-id="c90fd-105">We’re moving the portal to the Microsoft 365 admin center, and then the Microsoft Search in Bing portal will be removed.</span></span> <span data-ttu-id="c90fd-106">建議您使用 Microsoft 365 系統管理中心來開始。</span><span class="sxs-lookup"><span data-stu-id="c90fd-106">We recommend that you use the Microsoft 365 admin center to get started.</span></span> <span data-ttu-id="c90fd-107">[Microsoft Search 概觀](overview-microsoft-search.md)。</span><span class="sxs-lookup"><span data-stu-id="c90fd-107">[Overview of Microsoft Search](overview-microsoft-search.md).</span></span>
    
<span data-ttu-id="c90fd-108">下載並使用.csv 範本，以大量建立、 編輯及儲存的書籤。</span><span class="sxs-lookup"><span data-stu-id="c90fd-108">Download and use the .csv template to bulk create, edit, and save bookmarks.</span></span> <span data-ttu-id="c90fd-109">若要大量編輯現有的書籤，匯出系統管理員入口網站、 進行必要的編輯，然後再將它們匯。</span><span class="sxs-lookup"><span data-stu-id="c90fd-109">To bulk edit existing bookmarks, export them from the Admin portal, make the necessary edits, and then import them.</span></span>
  
1. <span data-ttu-id="c90fd-110">在 [書籤] 區段中的右上角，按一下 [**匯入**</span><span class="sxs-lookup"><span data-stu-id="c90fd-110">In the upper-right corner of the Bookmarks section, click **Import**</span></span>
    
2. <span data-ttu-id="c90fd-111">按一下 [**下載書籤範本 (.csv)**</span><span class="sxs-lookup"><span data-stu-id="c90fd-111">Click **Download bookmarks template (.csv)**</span></span>
    
3. <span data-ttu-id="c90fd-112">儲存並開啟 .csv 檔案</span><span class="sxs-lookup"><span data-stu-id="c90fd-112">Save and open the .csv file</span></span>
    
4. <span data-ttu-id="c90fd-113">新增的書籤內容和設定，並將檔案儲存</span><span class="sxs-lookup"><span data-stu-id="c90fd-113">Add the bookmark content and settings and save the file</span></span>

    <span data-ttu-id="c90fd-114">您應該將 .csv 檔案儲存為 CSV UTF-8 檔案，其他檔案類型和或編碼可能造成匯入錯誤</span><span class="sxs-lookup"><span data-stu-id="c90fd-114">The .csv file should be saved as a CSV UTF-8 file, other file types and or encodings may cause import errors</span></span>
    
5. <span data-ttu-id="c90fd-115">在 [書籤] 區段中的右上角，按一下 [**匯入**</span><span class="sxs-lookup"><span data-stu-id="c90fd-115">In the upper-right corner of the Bookmarks section, click **Import**</span></span>
    
6. <span data-ttu-id="c90fd-116">在 [匯入的書籤] 窗格中，按一下 [**瀏覽**並瀏覽至您要匯入的.csv 檔案</span><span class="sxs-lookup"><span data-stu-id="c90fd-116">In the Import bookmarks pane, click **Browse** and navigate to the .csv file you want to import</span></span> 
    
7. <span data-ttu-id="c90fd-117">按一下 [匯入]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="c90fd-117">Click **Import**</span></span>

## <a name="prevent-import-errors"></a><span data-ttu-id="c90fd-118">防止匯入錯誤</span><span class="sxs-lookup"><span data-stu-id="c90fd-118">Prevent import errors</span></span>      
<span data-ttu-id="c90fd-119">如果有任何必要資料遺失或無效，您就會收到錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="c90fd-119">You'll get an error if any required data is missing or invalid.</span></span> <span data-ttu-id="c90fd-120">依據錯誤的類型，系統可能會產生一份記錄檔，其中包含哪些列或欄需要修正的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="c90fd-120">Depending on the error, a log file may be generated with more information about the rows and columns that need to be corrected.</span></span> <span data-ttu-id="c90fd-121">進行任何所需編輯，然後再次嘗試匯入檔案。</span><span class="sxs-lookup"><span data-stu-id="c90fd-121">Make any necessary edits, and try importing the file again.</span></span>

> [!NOTE]
> <span data-ttu-id="c90fd-122">除非解決所有問題，您無法建立或編輯任何書籤。</span><span class="sxs-lookup"><span data-stu-id="c90fd-122">Until all errors are resolved, you can't create or edit any bookmarks.</span></span> 

<span data-ttu-id="c90fd-123">若要避免錯誤，請確定您匯入的檔案的格式正確：</span><span class="sxs-lookup"><span data-stu-id="c90fd-123">To help prevent errors, make sure your import file is properly formatted:</span></span>
- <span data-ttu-id="c90fd-124">包含匯入範本中的標題列</span><span class="sxs-lookup"><span data-stu-id="c90fd-124">Includes the header row that was in the import template</span></span>
- <span data-ttu-id="c90fd-125">包含匯入範本中的所有欄</span><span class="sxs-lookup"><span data-stu-id="c90fd-125">Includes all columns that were in the import template</span></span>
- <span data-ttu-id="c90fd-126">資料行順序與匯入範本相同</span><span class="sxs-lookup"><span data-stu-id="c90fd-126">The column order is the same as the import template</span></span>
- <span data-ttu-id="c90fd-127">這些資料行可以為空白：識別碼、上次修改日期，以及上次修改者</span><span class="sxs-lookup"><span data-stu-id="c90fd-127">These columns can be empty: Id, Last Modified, and Last Modified By</span></span>
- <span data-ttu-id="c90fd-128">[狀態] 資料行不能為空白，此為必要資訊</span><span class="sxs-lookup"><span data-stu-id="c90fd-128">The State column can't be empty, this information is required</span></span>  
<span data-ttu-id="c90fd-129">書籤會根據狀態欄位的不同而儲存成草稿、建議、已排程或自動發佈。</span><span class="sxs-lookup"><span data-stu-id="c90fd-129">Based on the State field, bookmarks will be saved as draft, suggested, scheduled, or they will be published automatically.</span></span>

<span data-ttu-id="c90fd-130">如果您加入現有的書籤的識別碼，則它會取代與匯入檔案中的資訊。</span><span class="sxs-lookup"><span data-stu-id="c90fd-130">Also, if you include the Id of an existing bookmark, it will be replaced with the information in the import file.</span></span>

<span data-ttu-id="c90fd-131">適用於負責管理多個組織的合作夥伴，您可以從一個組織匯出您的書籤，並匯入另一個。</span><span class="sxs-lookup"><span data-stu-id="c90fd-131">For partners who manage multiple organizations, you can export your bookmarks from one org and import them into another.</span></span> <span data-ttu-id="c90fd-132">但您必須在匯入之前，先移除 [識別碼] 資料行中的所有資料。</span><span class="sxs-lookup"><span data-stu-id="c90fd-132">But you must remove all of the data in the Id column before you import.</span></span>

<span data-ttu-id="c90fd-133">若要深入了解必要和建議的欄位，請參閱[建立書籤](create-bookmarks.md)。</span><span class="sxs-lookup"><span data-stu-id="c90fd-133">To find out more about required and recommended fields, see [Create bookmarks](create-bookmarks.md).</span></span>
