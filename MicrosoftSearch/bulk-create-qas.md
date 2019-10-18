---
title: 大量建立問與答
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
ms.assetid: 7bada218-8908-4956-aae3-6ffaeef384ca
ROBOTS: NoIndex
description: 在 Microsoft Search 系統管理入口網站中，使用匯入工具快速新增常見問題的解答
ms.openlocfilehash: c0ec4aaa0ee93e94c8569dc383456018ccc6679d
ms.sourcegitcommit: c2c9e66af1038efd2849d578f846680851f9e5d2
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/27/2019
ms.locfileid: "36639773"
---
# <a name="bulk-create-qas"></a><span data-ttu-id="669a1-103">大量建立問與答</span><span class="sxs-lookup"><span data-stu-id="669a1-103">Bulk create Q&As</span></span>

> [!IMPORTANT]
> <span data-ttu-id="669a1-104">本文章適用 Bing 系統管理入口網站中的 Microsoft Search。</span><span class="sxs-lookup"><span data-stu-id="669a1-104">This article applies to the Microsoft Search in Bing admin portal.</span></span> <span data-ttu-id="669a1-105">我們正在將入口網站移至 Microsoft 365 系統管理中心，完成之後將會移除 Bing 系統管理入口網站中的 Microsoft Search。</span><span class="sxs-lookup"><span data-stu-id="669a1-105">We’re moving the portal to the Microsoft 365 admin center, and then the Microsoft Search in Bing portal will be removed.</span></span> <span data-ttu-id="669a1-106">建議您使用 Microsoft 365 系統管理中心來開始。</span><span class="sxs-lookup"><span data-stu-id="669a1-106">We recommend that you use the Microsoft 365 admin center to get started.</span></span> <span data-ttu-id="669a1-107">[Microsoft Search 概觀](overview-microsoft-search.md)。</span><span class="sxs-lookup"><span data-stu-id="669a1-107">[Overview of Microsoft Graph](overview-microsoft-search.md)</span></span>
    
<span data-ttu-id="669a1-108">下載並使用 .csv 範本以大量建立或大量編輯問與答。</span><span class="sxs-lookup"><span data-stu-id="669a1-108">Download and use the .csv template to bulk create or bulk edit Q&As.</span></span> <span data-ttu-id="669a1-109">這也能輕鬆地大量儲存需要額外編輯或更新之草稿問與答的方式。</span><span class="sxs-lookup"><span data-stu-id="669a1-109">It's also a simple way to bulk save draft Q&As that need additional edits or updates.</span></span> <span data-ttu-id="669a1-110">如果您需要大量編輯現有的問與答，請從系統管理入口網站中匯出、進行所需編輯，然後再加以匯入。</span><span class="sxs-lookup"><span data-stu-id="669a1-110">If you need to bulk edit existing Q&As, export them from the Admin portal, make the necessary edits, and then import them.</span></span>
  
1. <span data-ttu-id="669a1-111">按一下問與答區段右上角的 [匯入]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="669a1-111">In the upper-right corner of the Q&As section, click **Import**</span></span>
    
2. <span data-ttu-id="669a1-112">按一下 [下載問與答範本 (.csv)]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="669a1-112">Click **Download Q&A template (.csv)**</span></span>
    
3. <span data-ttu-id="669a1-113">儲存並開啟 .csv 檔案</span><span class="sxs-lookup"><span data-stu-id="669a1-113">Save and open the .csv file</span></span>
    
4. <span data-ttu-id="669a1-114">新增問與答內容與設定，然後儲存檔案</span><span class="sxs-lookup"><span data-stu-id="669a1-114">Add the Q&A content and settings and save the file</span></span>

    <span data-ttu-id="669a1-115">您應該將 .csv 檔案儲存為 CSV UTF-8 檔案，其他檔案類型和或編碼可能造成匯入錯誤</span><span class="sxs-lookup"><span data-stu-id="669a1-115">The .csv file should be saved as a CSV UTF-8 file, other file types and or encodings may cause import errors</span></span>
    
5. <span data-ttu-id="669a1-116">在問與答區段右上角，按一下 [匯入]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="669a1-116">In the upper-right corner of the Q&As section, click **Import**</span></span>
    
6. <span data-ttu-id="669a1-117">在 [匯入問與答] 窗格中，按一下 [瀏覽]\*\*\*\*，然後瀏覽至您要匯入的 .csv 檔案</span><span class="sxs-lookup"><span data-stu-id="669a1-117">In the Import Q&As pane, click **Browse** and navigate to the .csv file you want to import</span></span> 
    
7. <span data-ttu-id="669a1-118">按一下 [匯入]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="669a1-118">Click **Import**.</span></span>

# <a name="prevent-import-errors"></a><span data-ttu-id="669a1-119">防止匯入錯誤</span><span class="sxs-lookup"><span data-stu-id="669a1-119">Prevent import errors</span></span>      
<span data-ttu-id="669a1-120">如果有任何必要資料遺失或無效，您就會收到錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="669a1-120">You'll get an error if any required data is missing or invalid.</span></span> <span data-ttu-id="669a1-121">依據錯誤的類型，系統可能會產生一份記錄檔，其中包含哪些列或欄需要修正的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="669a1-121">Depending on the error, a log file may be generated with more information about the rows and columns that need to be corrected.</span></span> <span data-ttu-id="669a1-122">進行任何所需編輯，然後再次嘗試匯入檔案。</span><span class="sxs-lookup"><span data-stu-id="669a1-122">Make any necessary edits, and try importing the file again.</span></span>

> [!NOTE]
> <span data-ttu-id="669a1-123">直到解決所有的錯誤之前，您無法建立或編輯任何問與答。</span><span class="sxs-lookup"><span data-stu-id="669a1-123">Until all errors are resolved, you can't create or edit any Q&As.</span></span> 

<span data-ttu-id="669a1-124">若要避免錯誤，請確定您匯入的檔案的格式正確：</span><span class="sxs-lookup"><span data-stu-id="669a1-124">To help prevent errors, make sure your import file is properly formatted:</span></span>
- <span data-ttu-id="669a1-125">包含匯入範本中的標題列</span><span class="sxs-lookup"><span data-stu-id="669a1-125">Includes the header row that was in the import template</span></span>
- <span data-ttu-id="669a1-126">包含匯入範本中的所有欄</span><span class="sxs-lookup"><span data-stu-id="669a1-126">Includes all columns that were in the import template</span></span>
- <span data-ttu-id="669a1-127">資料行順序與匯入範本相同</span><span class="sxs-lookup"><span data-stu-id="669a1-127">The column order is the same as the import template</span></span>
- <span data-ttu-id="669a1-128">這些資料行可以為空白：識別碼、上次修改日期，以及上次修改者</span><span class="sxs-lookup"><span data-stu-id="669a1-128">These columns can be empty: Id, Last Modified, and Last Modified By</span></span>
- <span data-ttu-id="669a1-129">[狀態] 資料行不能為空白，此為必要資訊</span><span class="sxs-lookup"><span data-stu-id="669a1-129">The State column can't be empty, this information is required</span></span>  
<span data-ttu-id="669a1-130">問與答會根據狀態欄位不同而被儲存成草稿、建議、已排程，或者自動發佈。</span><span class="sxs-lookup"><span data-stu-id="669a1-130">Based on the State field, Q&As will be saved as draft, suggested, scheduled, or they will be published automatically.</span></span>

<span data-ttu-id="669a1-131">同時，如果您包含現有問與答的識別碼，將會以匯入檔案中的資訊加以取代。</span><span class="sxs-lookup"><span data-stu-id="669a1-131">Also, if you include the Id of an existing Q&A, it will be replaced with the information in the import file.</span></span>

<span data-ttu-id="669a1-132">針對具有多個租用戶的組織，您可以從一個租用戶匯出您的問與答，並將它匯入到另一個租用戶。</span><span class="sxs-lookup"><span data-stu-id="669a1-132">For organizations with mulitple tenants, you can export your Q&As from one tenant and import it into another.</span></span> <span data-ttu-id="669a1-133">但您必須在匯入之前，先移除 [識別碼] 資料行中的所有資料。</span><span class="sxs-lookup"><span data-stu-id="669a1-133">But you must remove all of the data in the Id column before you import.</span></span>

<span data-ttu-id="669a1-134">若要深入了解必要欄位與建議欄位，請參閱[建立問與答](create-qas.md)。</span><span class="sxs-lookup"><span data-stu-id="669a1-134">To find out more about required and recommended fields, see [Create Q&As](create-qas.md).</span></span>

  

