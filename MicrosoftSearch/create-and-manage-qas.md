---
title: 建立和管理問與答
ms.author: dawholl
author: dawholl
manager: kellis
ms.date: 12/18/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: b40a575d-7727-4bb0-80da-e25131315790
ROBOTS: NoIndex
description: 在 Microsoft Search 系統管理入口網站中，建立常見問題解答所有方式的概觀
ms.openlocfilehash: 2d58d8b7bdec69f2f1d5078283ee1fb939e84e32
ms.sourcegitcommit: be2e837d9b087bffe6ce40d72d7ae58a8fcdf3fe
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/30/2019
ms.locfileid: "34591447"
---
# <a name="create-and-manage-qas"></a><span data-ttu-id="784fc-103">建立和管理問與答</span><span class="sxs-lookup"><span data-stu-id="784fc-103">Create and manage terms</span></span>

> [!IMPORTANT]
> <span data-ttu-id="784fc-104">本文章適用 Bing 系統管理入口網站中的 Microsoft Search。</span><span class="sxs-lookup"><span data-stu-id="784fc-104">This article applies to the Microsoft Search in Bing admin portal.</span></span> <span data-ttu-id="784fc-105">我們正在將入口網站移至 Microsoft 365 系統管理中心，完成之後入口網站將會移除。</span><span class="sxs-lookup"><span data-stu-id="784fc-105">We’re moving the portal to the Microsoft 365 admin center, and then it will be removed.</span></span> <span data-ttu-id="784fc-106">我們建議您使用 Microsoft 365 系統管理中心開始。</span><span class="sxs-lookup"><span data-stu-id="784fc-106">We recommend that you use the Microsoft 365 admin center to get started.</span></span> <span data-ttu-id="784fc-107">[Microsoft Search 概觀](overview-microsoft-search.md)。</span><span class="sxs-lookup"><span data-stu-id="784fc-107">[Overview of Microsoft Graph](overview-microsoft-search.md)</span></span>
    
## <a name="create-qas"></a><span data-ttu-id="784fc-108">建立問與答</span><span class="sxs-lookup"><span data-stu-id="784fc-108">Create Q&As</span></span>

<span data-ttu-id="784fc-109">問與答能提供對於使用者工作相關問題最有可能的答案。</span><span class="sxs-lookup"><span data-stu-id="784fc-109">Q&As provide the best possible answer for your user's work-related questions.</span></span> <span data-ttu-id="784fc-110">使用者可以在輸入您於 Bing 相關聯的關鍵字後，輕易找到這些答案。</span><span class="sxs-lookup"><span data-stu-id="784fc-110">Users can easily discover them when they enter keywords you've associated with them on Bing.</span></span>
  
- [<span data-ttu-id="784fc-111">建立問與答</span><span class="sxs-lookup"><span data-stu-id="784fc-111">Create Q&As</span></span>](create-qas.md)
    
    <span data-ttu-id="784fc-112">新增個別問與答。</span><span class="sxs-lookup"><span data-stu-id="784fc-112">Add individual Q&As.</span></span>
    
- [<span data-ttu-id="784fc-113">大量建立與匯入問與答</span><span class="sxs-lookup"><span data-stu-id="784fc-113">Bulk create and import Q&As</span></span>](bulk-create-qas.md)
    
    <span data-ttu-id="784fc-114">在 .csv 檔案中建立問與答，並大量匯入。</span><span class="sxs-lookup"><span data-stu-id="784fc-114">Create Q&As in a .csv file and bulk import them.</span></span>
    
## <a name="manage-qas"></a><span data-ttu-id="784fc-115">管理問與答</span><span class="sxs-lookup"><span data-stu-id="784fc-115">Manage Q&As</span></span>

<span data-ttu-id="784fc-116">使用問與答狀態、篩選工具與大量匯出/匯入工具來[尋找並更新問與答內容](manage-qas.md)，包括標題、解答、關鍵字和 URL。</span><span class="sxs-lookup"><span data-stu-id="784fc-116">Use the Q&A status, filtering tools, and bulk export/import tools to [find and update Q&A content](manage-qas.md), including title, answer, keywords, and URLs.</span></span>
  
## <a name="qa-status"></a><span data-ttu-id="784fc-117">問與答狀態</span><span class="sxs-lookup"><span data-stu-id="784fc-117">Q&A status</span></span>

<span data-ttu-id="784fc-118">您可以在系統管理入口網站中，依據問與答的目前狀態來檢視：</span><span class="sxs-lookup"><span data-stu-id="784fc-118">In the Admin portal, you can view Q&As by their current status:</span></span>
  
- <span data-ttu-id="784fc-119">已發佈</span><span class="sxs-lookup"><span data-stu-id="784fc-119">Published On</span></span>
    
    <span data-ttu-id="784fc-120">已發佈的問與答會在授權使用者搜尋關鍵字時，出現在 Bing 搜尋結果中。</span><span class="sxs-lookup"><span data-stu-id="784fc-120">Published Q&As appear in Bing search results when an authorized user searches for a keyword.</span></span>
    
- <span data-ttu-id="784fc-121">草稿</span><span class="sxs-lookup"><span data-stu-id="784fc-121">Draft</span></span>
    
    <span data-ttu-id="784fc-122">如果問與答尚未要發佈，您可以將它儲存為草稿。</span><span class="sxs-lookup"><span data-stu-id="784fc-122">If a Q&A isn't ready to publish, save it as a draft.</span></span> <span data-ttu-id="784fc-123">草稿問與答不會顯示在 Bing 中。</span><span class="sxs-lookup"><span data-stu-id="784fc-123">Draft Q&As will not appear on Bing.</span></span>
    
- <span data-ttu-id="784fc-124">已排程</span><span class="sxs-lookup"><span data-stu-id="784fc-124">Scheduled</span></span>
    
    <span data-ttu-id="784fc-125">已排程的問與答會自動於未來的某個日期發佈。</span><span class="sxs-lookup"><span data-stu-id="784fc-125">Scheduled Q&As are automatically published on a future date.</span></span>
    
- <span data-ttu-id="784fc-126">已過期</span><span class="sxs-lookup"><span data-stu-id="784fc-126">Expired</span></span>
    
    <span data-ttu-id="784fc-127">已過期的問與答會由系統依據到期日從發佈內容中移除。</span><span class="sxs-lookup"><span data-stu-id="784fc-127">Expired Q&As were automatically removed from published content based on the expiration date.</span></span>
    
- <span data-ttu-id="784fc-128">建議</span><span class="sxs-lookup"><span data-stu-id="784fc-128">Suggested action</span></span>
    
    <span data-ttu-id="784fc-129">系統會根據使用者的意見反應提出建議的問與答。</span><span class="sxs-lookup"><span data-stu-id="784fc-129">Suggested Q&As are based on feedback from users.</span></span>

  

