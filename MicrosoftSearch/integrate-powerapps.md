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
description: 在 Microsoft Search 的書籤結果中包括瀏覽器型應用程式
ms.openlocfilehash: 96b409274e3fa06cef7dcc6f1c43360a3e6b9d34
ms.sourcegitcommit: 3e91a6e70b48a0100adfed1b62ba79f2fd1735d2
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/13/2019
ms.locfileid: "34425644"
---
# <a name="integrate-powerapps"></a><span data-ttu-id="9a36a-103">整合 PowerApps</span><span class="sxs-lookup"><span data-stu-id="9a36a-103">Integrate PowerApps</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9a36a-104">Bing 設定中的 Microsoft Search 現在可以在 Microsoft 365 管理中心中使用。</span><span class="sxs-lookup"><span data-stu-id="9a36a-104">Microsoft Search in Bing settings are now available in the Microsoft 365 admin center.</span></span> <span data-ttu-id="9a36a-105">從系統管理中心的[指派搜尋系統管理員](https://docs.microsoft.com/zh-TW/microsoftsearch/setup-microsoft-search#step-2-assign-search-admin-and-search-editor)開始。</span><span class="sxs-lookup"><span data-stu-id="9a36a-105">Get started by [assigning search admins](https://docs.microsoft.com/en-us/microsoftsearch/setup-microsoft-search#step-2-assign-search-admin-and-search-editor) in your admin center.</span></span>
    
<span data-ttu-id="9a36a-106">將現有的 PowerApps 整合至您的書籤，協助您的使用者完成工作，例如輸入假期時間或提出支出報告。</span><span class="sxs-lookup"><span data-stu-id="9a36a-106">Help your users complete tasks, such as entering vacation time or reporting expenses by integrating existing PowerApps into your bookmarks.</span></span> <span data-ttu-id="9a36a-107">整合後的 PowerApps 會出現在書籤結果內，免去移至不同網站或開啟其他工具的麻煩，節省您的時間與精力。</span><span class="sxs-lookup"><span data-stu-id="9a36a-107">Integrated PowerApps appear within a bookmark result, eliminating the need to go to a different site or open a separate tool, which saves times and effort.</span></span>
  
## <a name="what-are-powerapps"></a><span data-ttu-id="9a36a-108">什麼是 PowerApps？</span><span class="sxs-lookup"><span data-stu-id="9a36a-108">What are PowerApps?</span></span>

<span data-ttu-id="9a36a-109">PowerApps 是一個服務，即使您沒有編碼經驗，也能打造在瀏覽器、手機或平板電腦上運行的商務 App。</span><span class="sxs-lookup"><span data-stu-id="9a36a-109">PowerApps is a service that lets you build business apps that run in a browser or on a phone or tablet with no coding experience required.</span></span> <span data-ttu-id="9a36a-110">深入了解：</span><span class="sxs-lookup"><span data-stu-id="9a36a-110">Learn more:</span></span>
  
- <span data-ttu-id="9a36a-111">
  [引導學習](https://docs.microsoft.com/zh-TW/learn/browse/?products=powerapps)</span><span class="sxs-lookup"><span data-stu-id="9a36a-111">[Guided Learning](https://docs.microsoft.com/en-us/learn/browse/?products=powerapps)</span></span>
    
- <span data-ttu-id="9a36a-112">
  [文件](https://docs.microsoft.com/zh-TW/powerapps/)</span><span class="sxs-lookup"><span data-stu-id="9a36a-112">[Documentation](https://docs.microsoft.com/en-us/powerapps/)</span></span>
    
## <a name="add-a-powerapp-to-a-bookmark"></a><span data-ttu-id="9a36a-113">將 PowerApp 新增至書籤</span><span class="sxs-lookup"><span data-stu-id="9a36a-113">Add a PowerApp to a bookmark</span></span>

<span data-ttu-id="9a36a-114">PowerApps 可以在任何瀏覽器和任何裝置上運行，不到一分鐘即可迅速新增完畢。</span><span class="sxs-lookup"><span data-stu-id="9a36a-114">PowerApps work in any browser and on any device and take less than a minute to add.</span></span>
  
1. <span data-ttu-id="9a36a-115">
  [尋找您想要整合之 PowerApp 的應用程式識別碼](https://docs.microsoft.com/zh-TW/powerapps/maker/canvas-apps/get-sessionid#get-an-app-id)</span><span class="sxs-lookup"><span data-stu-id="9a36a-115">[Find the App ID for the PowerApp](https://docs.microsoft.com/en-us/powerapps/maker/canvas-apps/get-sessionid#get-an-app-id) you want to integrate</span></span> 
    
2. <span data-ttu-id="9a36a-116">在 Microsoft Search 系統管理入口網站中，移至 [書籤]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="9a36a-116">In the Microsoft SearchAdmin portal, go to **Bookmarks**</span></span>
    
3. <span data-ttu-id="9a36a-117">新增書籤或尋找您想要新增 PowerApp 的現有書籤</span><span class="sxs-lookup"><span data-stu-id="9a36a-117">Add a bookmark or find an existing bookmark that you want to add a PowerApp to</span></span>
    
4. <span data-ttu-id="9a36a-118">在書籤設定中，按一下 [Power App]\*\*\*\*，然後按一下 [新增 Power App]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="9a36a-118">In the bookmark settings, click **Power App**, and then click **Add a Power App**</span></span>
    
5. <span data-ttu-id="9a36a-119">輸入或貼上應用程式識別碼</span><span class="sxs-lookup"><span data-stu-id="9a36a-119">Enter or paste the App ID</span></span>
    
    <span data-ttu-id="9a36a-120">系統會自動新增高度和寬度。</span><span class="sxs-lookup"><span data-stu-id="9a36a-120">The height and width are automatically added.</span></span> <span data-ttu-id="9a36a-121">書籤能夠同時支援直向和橫向的方向，但目前無法變更大小。</span><span class="sxs-lookup"><span data-stu-id="9a36a-121">Bookmarks can support both portrait and landscape orientations, but currently the size can't be changed.</span></span>
    
6. <span data-ttu-id="9a36a-122">書籤預覽會顯示 PowerApp 在書籤結果中的顯示方式</span><span class="sxs-lookup"><span data-stu-id="9a36a-122">The bookmark preview shows how the PowerApp will appear in the bookmark result</span></span>
    
    <span data-ttu-id="9a36a-123">預覽中的 PowerApp 擁有完整功能，便於您進行測試和使用。</span><span class="sxs-lookup"><span data-stu-id="9a36a-123">The PowerApp in the preview is fully functional to make it easy to test and use.</span></span>
    
7. <span data-ttu-id="9a36a-124">按一下 [發佈]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="9a36a-124">Click **Publish**.</span></span>
    
<span data-ttu-id="9a36a-125">當授權的 Microsoft Search 使用者在 Bing 上搜尋任何書籤的關鍵字或保留的關鍵字時，PowerApp 便會出現在書籤結果中。</span><span class="sxs-lookup"><span data-stu-id="9a36a-125">When an authorized Microsoft Search user searches on Bing for any of the bookmark's keywords or reserved keywords, the PowerApp will appear in the bookmark result.</span></span>

  

