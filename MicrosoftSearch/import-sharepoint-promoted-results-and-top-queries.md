---
title: 匯入 SharePoint 升級的結果與查詢排行榜
ms.author: dawholl
author: dawholl
manager: kellis
ms.date: 9/8/2018
ms.audience: Admin
ms.topic: reference
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: 3d2a1498-174e-4214-9cf1-8b58cce5a872
ROBOTS: NOINDEX
description: 使用 SharePoint 搜尋查詢來建立 Microsoft Search 工作結果
ms.openlocfilehash: ebfd10f8705ce5b9a36b9c13d549e28a3f1c6b91
ms.sourcegitcommit: c2c9e66af1038efd2849d578f846680851f9e5d2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/27/2019
ms.locfileid: "36639800"
---
# <a name="import-sharepoint-promoted-results-and-top-queries"></a><span data-ttu-id="c8e41-103">匯入 SharePoint 升級的結果與查詢排行榜</span><span class="sxs-lookup"><span data-stu-id="c8e41-103">Import SharePoint promoted results and top queries</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c8e41-104">本文適用於 Microsoft Search Bing 系統管理入口網站中。</span><span class="sxs-lookup"><span data-stu-id="c8e41-104">This article applies to the Microsoft Search in Bing admin portal.</span></span> <span data-ttu-id="c8e41-105">我們可以從入口網站移至 Microsoft 365 系統管理中心]，然後將移除 Microsoft Search Bing 入口網站中。</span><span class="sxs-lookup"><span data-stu-id="c8e41-105">We’re moving the portal to the Microsoft 365 admin center, and then the Microsoft Search in Bing portal will be removed.</span></span> <span data-ttu-id="c8e41-106">我們建議您若要開始使用 Microsoft 365 系統管理中心。</span><span class="sxs-lookup"><span data-stu-id="c8e41-106">We recommend that you use the Microsoft 365 admin center to get started.</span></span> <span data-ttu-id="c8e41-107">[Microsoft Search 的概觀](overview-microsoft-search.md)。</span><span class="sxs-lookup"><span data-stu-id="c8e41-107">[Overview of Microsoft Search](overview-microsoft-search.md).</span></span>
    
<span data-ttu-id="c8e41-108">若要利用使用者的查詢與您已在 SharePoint 中建立的首選，Microsoft 搜尋會包含兩個工具來匯入為建議的書籤此資訊：</span><span class="sxs-lookup"><span data-stu-id="c8e41-108">To leverage users' queries and Best Bets you've created in SharePoint, Microsoft Search includes two tools to import this information as suggested bookmarks:</span></span> 
  
## <a name="import-sharepoint-promoted-result-query-rules"></a><span data-ttu-id="c8e41-109">匯入 SharePoint 升階結果查詢規則</span><span class="sxs-lookup"><span data-stu-id="c8e41-109">Import SharePoint promoted result query rules</span></span>

<span data-ttu-id="c8e41-110">匯入這些規則，之前稱為 「 首選，以建議的書籤。</span><span class="sxs-lookup"><span data-stu-id="c8e41-110">Import these rules, previously called Best Bets, as suggested bookmarks.</span></span> <span data-ttu-id="c8e41-111">若要讓他們可以使用您的使用者，發佈它們。</span><span class="sxs-lookup"><span data-stu-id="c8e41-111">To make them available to your users, publish them.</span></span> <span data-ttu-id="c8e41-112">發佈時間而異根據您所選取的書籤的數目。</span><span class="sxs-lookup"><span data-stu-id="c8e41-112">Publishing time varies based on the number of bookmarks you select.</span></span>
  
## <a name="import-top-sharepoint-queries-using-powershell"></a><span data-ttu-id="c8e41-113">匯入使用 PowerShell 的 SharePoint 查詢排行榜</span><span class="sxs-lookup"><span data-stu-id="c8e41-113">Import top SharePoint queries using PowerShell</span></span>

- <span data-ttu-id="c8e41-114">從您的 SharePoint 下載排名最前面的查詢。</span><span class="sxs-lookup"><span data-stu-id="c8e41-114">Download the top queries from your SharePoint.</span></span> <span data-ttu-id="c8e41-115">PowerShell 指令碼會提示您輸入您的 SharePoint 系統管理員認證。</span><span class="sxs-lookup"><span data-stu-id="c8e41-115">The PowerShell script will prompt you for your SharePoint administrator credentials.</span></span>
    
- <span data-ttu-id="c8e41-116">執行 SharePoint 搜尋每個查詢排行榜來取得最上層搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="c8e41-116">Run a SharePoint search for each of the top queries to get the top search result.</span></span>
    
- <span data-ttu-id="c8e41-117">建議的書籤加入系統管理入口網站。</span><span class="sxs-lookup"><span data-stu-id="c8e41-117">Add suggested bookmarks to the Admin portal.</span></span>
    
- <span data-ttu-id="c8e41-118">排名最前面的 SharePoint 查詢限於極佳的書籤。</span><span class="sxs-lookup"><span data-stu-id="c8e41-118">Your top SharePoint queries are excellent candidates for bookmarks.</span></span> <span data-ttu-id="c8e41-119">使用 PowerShell 指令碼來匯入為建議的書籤。</span><span class="sxs-lookup"><span data-stu-id="c8e41-119">Use the PowerShell script to import them as suggested bookmarks.</span></span> <span data-ttu-id="c8e41-120">此指令碼會執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="c8e41-120">This script does the following work:</span></span>
    - <span data-ttu-id="c8e41-121">新增建議根據 SharePoint 排行榜，以提升 Microsoft Search 書籤涵蓋範圍的書籤。</span><span class="sxs-lookup"><span data-stu-id="c8e41-121">Adds suggested bookmarks based on SharePoint top queries to improve Microsoft Search bookmark coverage.</span></span> <span data-ttu-id="c8e41-122">此指令碼從 SharePoint 系統管理入口網站，下載存取查詢排行榜，並再將它們上傳為系統管理員在 Microsoft 搜尋系統管理入口網站中檢閱建議書籤。</span><span class="sxs-lookup"><span data-stu-id="c8e41-122">This script downloads the top queries accessible from SharePoint admin portal, and then uploads them as suggested bookmarks for an admin to review in the Microsoft Search admin portal.</span></span>
    - <span data-ttu-id="c8e41-123">根據預設，指令碼會新增建議的書籤可指定租用戶的所有可用的月數。</span><span class="sxs-lookup"><span data-stu-id="c8e41-123">By default, the script adds suggested bookmarks to given tenant for all available months.</span></span> <span data-ttu-id="c8e41-124">它會從指定的 SharePoint 系統管理員網站取得查詢排行榜，並將它們新增至 Microsoft Search 為建議的書籤。</span><span class="sxs-lookup"><span data-stu-id="c8e41-124">It gets top queries from a given SharePoint admin website and adds them to Microsoft Search as suggested bookmarks.</span></span> <span data-ttu-id="c8e41-125">建議的書籤時，需要系統管理員/編輯器之前發佈核准管理入口網站中。</span><span class="sxs-lookup"><span data-stu-id="c8e41-125">Suggested bookmarks need an admin/editor to approve them in the admin portal before being published.</span></span> <span data-ttu-id="c8e41-126">當您執行此指令碼時，系統會提示您若要存取 Microsoft 搜尋系統管理入口網站中的認證。</span><span class="sxs-lookup"><span data-stu-id="c8e41-126">When you run this script, you are prompted for credentials to access the Microsoft Search admin portal.</span></span>
    - <span data-ttu-id="c8e41-127">指令碼可讓您指定其他參數。</span><span class="sxs-lookup"><span data-stu-id="c8e41-127">The script allows additional parameters to be specified.</span></span> <span data-ttu-id="c8e41-128">例如，可以新增建議的書籤可指定租用戶中每個可用的月份的前 n 個查詢。</span><span class="sxs-lookup"><span data-stu-id="c8e41-128">You can, for example, add suggested bookmarks to given tenant for top N queries in each of the available months.</span></span>
    - <span data-ttu-id="c8e41-129">或者，您可以新增建議的書籤可指定租用戶中特定年度的月數。</span><span class="sxs-lookup"><span data-stu-id="c8e41-129">Optionally, you can add suggested bookmarks to given tenant for months in the given year.</span></span> <span data-ttu-id="c8e41-130">這個命令會從 SharePoint 系統管理員網站指定的時間期間取得查詢排行榜，並將它們新增至 Microsoft Search 為建議的書籤。</span><span class="sxs-lookup"><span data-stu-id="c8e41-130">This command gets top queries for the given time period from SharePoint admin website and adds them to Microsoft Search as suggested bookmarks.</span></span>
    - <span data-ttu-id="c8e41-131">同時，有許多其他選項和命令模式： 下載排行榜從 SharePoint 至指定的資料夾，並在安全模式中，執行指令碼 Verbose 模式和偵錯模式中執行指令碼。</span><span class="sxs-lookup"><span data-stu-id="c8e41-131">As well, there are numerous other options and command modes: download top queries from SharePoint to a specified folder, run the script in Safe mode, run the script in Verbose mode, and a Debug mode.</span></span>
    - <span data-ttu-id="c8e41-132">下載指令碼[在這裡](https://www.bingforbusiness.com/distribution/SharepointTopQueryBookmarks.zip)。</span><span class="sxs-lookup"><span data-stu-id="c8e41-132">Download the script [here](https://www.bingforbusiness.com/distribution/SharepointTopQueryBookmarks.zip).</span></span> 

<span data-ttu-id="c8e41-133">如需需求、 範例和可用的參數，下載指令碼，並檢閱讀我檔案。</span><span class="sxs-lookup"><span data-stu-id="c8e41-133">For information about requirements, examples, and available parameters, download the script and review the README file.</span></span> <span data-ttu-id="c8e41-134">PowerShell 指令碼之後執行、 系統或編輯器應該檢閱建議的書籤，和他們正在發佈前進行任何必要的編輯。</span><span class="sxs-lookup"><span data-stu-id="c8e41-134">After the PowerShell script runs, an admin or editor should review the suggested bookmarks and make any necessary edits before they're published.</span></span>