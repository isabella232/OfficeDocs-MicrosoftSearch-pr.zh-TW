---
title: 匯入 SharePoint 提升的結果與熱門查詢
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
description: 使用 SharePoint 的搜尋查詢以建立 Microsoft Search 工作結果
ms.openlocfilehash: 1538c57a7b4138b36fe62e3076feb58d746b2b3e
ms.sourcegitcommit: be2e837d9b087bffe6ce40d72d7ae58a8fcdf3fe
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/30/2019
ms.locfileid: "34591600"
---
# <a name="import-sharepoint-promoted-results-and-top-queries"></a><span data-ttu-id="50736-103">匯入 SharePoint 提升的結果與熱門查詢</span><span class="sxs-lookup"><span data-stu-id="50736-103">Import SharePoint promoted results and top queries</span></span>

> [!IMPORTANT]
> <span data-ttu-id="50736-104">本文適用於 Bing 系統管理入口網站中的 Microsoft Search。</span><span class="sxs-lookup"><span data-stu-id="50736-104">This article applies to the Microsoft Search in Bing admin portal.</span></span> <span data-ttu-id="50736-105">我們已將入口網站移至 Microsoft 365 管理中心，並在之後移除。</span><span class="sxs-lookup"><span data-stu-id="50736-105">We’re moving the portal to the Microsoft 365 admin center, and then it will be removed.</span></span> <span data-ttu-id="50736-106">我們建議您使用 Microsoft 365 系統管理中心以開始。</span><span class="sxs-lookup"><span data-stu-id="50736-106">We recommend that you use the Microsoft 365 admin center to get started.</span></span> <span data-ttu-id="50736-107">[Microsoft Search 概觀](overview-microsoft-search.md)。</span><span class="sxs-lookup"><span data-stu-id="50736-107">[Overview of Microsoft Graph](overview-microsoft-search.md)</span></span>
    
<span data-ttu-id="50736-108">為了有效調控使用者的查詢與您在 SharePoint 中建立的首選，Microsoft Search 納入了兩項能將此資訊匯入為建議書籤的工具：</span><span class="sxs-lookup"><span data-stu-id="50736-108">To leverage users' queries and Best Bets you've created in SharePoint, Microsoft Search includes two tools to import this information as suggested bookmarks:</span></span> 
  
## <a name="import-sharepoint-promoted-result-query-rules"></a><span data-ttu-id="50736-109">匯入 SharePoint 提升的結果查詢規則</span><span class="sxs-lookup"><span data-stu-id="50736-109">Import SharePoint promoted result query rules</span></span>

<span data-ttu-id="50736-110">將這些之前稱為首選的規則匯入為建議書籤。</span><span class="sxs-lookup"><span data-stu-id="50736-110">Import these rules, previously called Best Bets, as suggested bookmarks.</span></span> <span data-ttu-id="50736-111">若要將這些書籤提供給您的使用者，請進行發佈。</span><span class="sxs-lookup"><span data-stu-id="50736-111">To make them available to your users, publish them.</span></span> <span data-ttu-id="50736-112">發佈時間會隨您所選書籤的數量而有所不同。</span><span class="sxs-lookup"><span data-stu-id="50736-112">Publishing time varies based on the number of bookmarks you select.</span></span>
  
## <a name="import-top-sharepoint-queries-using-powershell"></a><span data-ttu-id="50736-113">使用 PowerShell 以匯入熱門 SharePoint 查詢</span><span class="sxs-lookup"><span data-stu-id="50736-113">Import top SharePoint queries using PowerShell</span></span>

- <span data-ttu-id="50736-114">從您的 SharePoint 下載熱門查詢。</span><span class="sxs-lookup"><span data-stu-id="50736-114">Download the top queries from your SharePoint.</span></span> <span data-ttu-id="50736-115">PowerShell 指令碼會提示您輸入 SharePoint 系統管理員認證。</span><span class="sxs-lookup"><span data-stu-id="50736-115">The PowerShell script will prompt you for your SharePoint administrator credentials.</span></span>
    
- <span data-ttu-id="50736-116">針對每一個熱門查詢執行 SharePoint 搜尋，以取得最佳搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="50736-116">Run a SharePoint search for each of the top queries to get the top search result.</span></span>
    
- <span data-ttu-id="50736-117">在系統管理入口網站新增建議書籤。</span><span class="sxs-lookup"><span data-stu-id="50736-117">Add suggested bookmarks to the Admin portal.</span></span>
    
- <span data-ttu-id="50736-118">您的熱門 SharePoint 查詢擁有做為書籤的最佳條件。</span><span class="sxs-lookup"><span data-stu-id="50736-118">Your top SharePoint queries are excellent candidates for bookmarks.</span></span> <span data-ttu-id="50736-119">請使用 PowerShell 指令碼以將它們匯入為建議書籤。</span><span class="sxs-lookup"><span data-stu-id="50736-119">Use the PowerShell script to import them as suggested bookmarks.</span></span> <span data-ttu-id="50736-120">此指令碼將會：</span><span class="sxs-lookup"><span data-stu-id="50736-120">This script will:</span></span>
    
<span data-ttu-id="50736-121">如需關於需求、範例和可用參數的資訊，請下載指令碼並檢閱讀我檔案。</span><span class="sxs-lookup"><span data-stu-id="50736-121">For information about requirements, examples, and available parameters, download the script and review the README file.</span></span> <span data-ttu-id="50736-122">在執行 PowerShell 指令碼之後，系統管理員或編輯者應該在先檢閱建議的書籤，並進行任何必要的編輯，之後再發佈。</span><span class="sxs-lookup"><span data-stu-id="50736-122">After the PowerShell script runs, an admin or editor should review the suggested bookmarks and make any necessary edits before they're published.</span></span>

  

