---
title: 整合 PowerApps
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
ms.assetid: 1fadcba3-4a7f-4a55-8476-d4e64d49a15f
ROBOTS: NOINDEX
description: 在 Microsoft Search 的書籤結果中包括瀏覽器型應用程式
ms.openlocfilehash: 1f4cf7512ee176015537be2fbe2f59429cde6578
ms.sourcegitcommit: fe7f3dae4edba97071a4d127e8a27bdf4fa00d81
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/05/2019
ms.locfileid: "34727967"
---
# <a name="integrate-powerapps"></a><span data-ttu-id="4c3a6-103">整合 PowerApps</span><span class="sxs-lookup"><span data-stu-id="4c3a6-103">Integrate PowerApps</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4c3a6-104">本文適用於 Bing 系統管理入口網站中的 Microsoft Search。</span><span class="sxs-lookup"><span data-stu-id="4c3a6-104">This article applies to the Microsoft Search in Bing admin portal.</span></span> <span data-ttu-id="4c3a6-105">我們正在將入口網站移至 Microsoft 365 系統管理中心，完成之後入口網站將會移除。</span><span class="sxs-lookup"><span data-stu-id="4c3a6-105">We’re moving the portal to the Microsoft 365 admin center, and then it will be removed.</span></span> <span data-ttu-id="4c3a6-106">我們建議您使用 Microsoft 365 系統管理中心開始。</span><span class="sxs-lookup"><span data-stu-id="4c3a6-106">We recommend that you use the Microsoft 365 admin center to get started.</span></span> <span data-ttu-id="4c3a6-107">[Microsoft Search 概觀](overview-microsoft-search.md)。</span><span class="sxs-lookup"><span data-stu-id="4c3a6-107">[Overview of Microsoft Graph](overview-microsoft-search.md)</span></span>
    
<span data-ttu-id="4c3a6-108">將現有的 PowerApps 整合至您的書籤，協助您的使用者完成工作，例如輸入假期時間或提出支出報告。</span><span class="sxs-lookup"><span data-stu-id="4c3a6-108">Help your users complete tasks, such as entering vacation time or reporting expenses by integrating existing PowerApps into your bookmarks.</span></span> <span data-ttu-id="4c3a6-109">整合後的 PowerApps 會出現在書籤結果內，免去移至不同網站或開啟其他工具的麻煩，節省您的時間與精力。</span><span class="sxs-lookup"><span data-stu-id="4c3a6-109">Integrated PowerApps appear within a bookmark result, eliminating the need to go to a different site or open a separate tool, which saves times and effort.</span></span>
  
## <a name="what-are-powerapps"></a><span data-ttu-id="4c3a6-110">什麼是 PowerApps？</span><span class="sxs-lookup"><span data-stu-id="4c3a6-110">What are PowerApps?</span></span>

<span data-ttu-id="4c3a6-111">PowerApps 是一個服務，即使您沒有編碼經驗，也能打造在瀏覽器、手機或平板電腦上運行的商務 App。</span><span class="sxs-lookup"><span data-stu-id="4c3a6-111">PowerApps is a service that lets you build business apps that run in a browser or on a phone or tablet with no coding experience required.</span></span> <span data-ttu-id="4c3a6-112">深入了解：</span><span class="sxs-lookup"><span data-stu-id="4c3a6-112">Learn more:</span></span>
  
- <span data-ttu-id="4c3a6-113">
  [引導學習](https://docs.microsoft.com/zh-TW/learn/browse/?products=powerapps)</span><span class="sxs-lookup"><span data-stu-id="4c3a6-113">[Guided Learning](https://docs.microsoft.com/en-us/learn/browse/?products=powerapps)</span></span>
    
- <span data-ttu-id="4c3a6-114">
  [文件](https://docs.microsoft.com/zh-TW/powerapps/)</span><span class="sxs-lookup"><span data-stu-id="4c3a6-114">[Documentation](https://docs.microsoft.com/en-us/powerapps/)</span></span>
    
## <a name="add-a-powerapp-to-a-bookmark"></a><span data-ttu-id="4c3a6-115">將 PowerApp 新增至書籤</span><span class="sxs-lookup"><span data-stu-id="4c3a6-115">Add a PowerApp to a bookmark</span></span>

<span data-ttu-id="4c3a6-116">PowerApps 可以在任何瀏覽器和任何裝置上運行，不到一分鐘即可迅速新增完畢。</span><span class="sxs-lookup"><span data-stu-id="4c3a6-116">PowerApps work in any browser and on any device and take less than a minute to add.</span></span>
  
1. <span data-ttu-id="4c3a6-117">
  [尋找您想要整合之 PowerApp 的應用程式識別碼](https://docs.microsoft.com/zh-TW/powerapps/maker/canvas-apps/get-sessionid#get-an-app-id)</span><span class="sxs-lookup"><span data-stu-id="4c3a6-117">[Find the App ID for the PowerApp](https://docs.microsoft.com/en-us/powerapps/maker/canvas-apps/get-sessionid#get-an-app-id) you want to integrate</span></span> 
    
2. <span data-ttu-id="4c3a6-118">在 Microsoft Search 系統管理入口網站中，移至 [書籤]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="4c3a6-118">In the Microsoft Search Admin portal, go to **Bookmarks**</span></span>
    
3. <span data-ttu-id="4c3a6-119">新增書籤或尋找您想要新增 PowerApp 的現有書籤</span><span class="sxs-lookup"><span data-stu-id="4c3a6-119">Add a bookmark or find an existing bookmark that you want to add a PowerApp to</span></span>
    
4. <span data-ttu-id="4c3a6-120">在書籤設定中，按一下 [Power App]\*\*\*\*，然後按一下 [新增 Power App]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="4c3a6-120">In the bookmark settings, click **Power App**, and then click **Add a Power App**</span></span>
    
5. <span data-ttu-id="4c3a6-121">輸入或貼上應用程式識別碼</span><span class="sxs-lookup"><span data-stu-id="4c3a6-121">Enter or paste the App ID</span></span>
    
    <span data-ttu-id="4c3a6-122">系統會自動新增高度和寬度。</span><span class="sxs-lookup"><span data-stu-id="4c3a6-122">The height and width are automatically added.</span></span> <span data-ttu-id="4c3a6-123">書籤能夠同時支援直向和橫向的方向，但目前無法變更大小。</span><span class="sxs-lookup"><span data-stu-id="4c3a6-123">Bookmarks can support both portrait and landscape orientations, but currently the size can't be changed.</span></span>
    
6. <span data-ttu-id="4c3a6-124">書籤預覽會顯示 PowerApp 在書籤結果中的顯示方式</span><span class="sxs-lookup"><span data-stu-id="4c3a6-124">The bookmark preview shows how the PowerApp will appear in the bookmark result</span></span>
    
    <span data-ttu-id="4c3a6-125">預覽中的 PowerApp 擁有完整功能，便於您進行測試和使用。</span><span class="sxs-lookup"><span data-stu-id="4c3a6-125">The PowerApp in the preview is fully functional to make it easy to test and use.</span></span>
    
7. <span data-ttu-id="4c3a6-126">按一下 [發佈]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="4c3a6-126">Click **Publish**.</span></span>
    
<span data-ttu-id="4c3a6-127">當授權的 Microsoft Search 使用者在 Bing 上搜尋任何書籤的關鍵字或保留的關鍵字時，PowerApp 便會出現在書籤結果中。</span><span class="sxs-lookup"><span data-stu-id="4c3a6-127">When an authorized Microsoft Search user searches on Bing for any of the bookmark's keywords or reserved keywords, the PowerApp will appear in the bookmark result.</span></span>

  

