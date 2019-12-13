---
title: 整合 Power 應用程式
ms.author: dawholl
author: dawholl
manager: kellis
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: 1fadcba3-4a7f-4a55-8476-d4e64d49a15f
description: Microsoft Search 的書籤結果中包含瀏覽器型應用程式
ms.openlocfilehash: 7d3dd21758c63da14bbd3896ece1ce67a19c80a2
ms.sourcegitcommit: f4cb37fdf85b895337caee827fb72b5b7fcaa8ad
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2019
ms.locfileid: "39995021"
---
# <a name="integrate-power-apps-in-microsoft-search-bookmarks"></a><span data-ttu-id="3f4cd-103">在 [Microsoft Search 書籤整合 Power 應用程式</span><span class="sxs-lookup"><span data-stu-id="3f4cd-103">Integrate Power Apps in Microsoft Search bookmarks</span></span>
   
<span data-ttu-id="3f4cd-104">協助您完成工作，例如輸入假期時間或報告費用，將現有的[Microsoft Power 應用程式](https://products.office.com/business/microsoft-powerapps)整合至您的 Microsoft Search 書籤的使用者。</span><span class="sxs-lookup"><span data-stu-id="3f4cd-104">Help your users complete tasks, like entering vacation time or reporting expenses, by integrating existing [Microsoft Power Apps](https://products.office.com/business/microsoft-powerapps) into your Microsoft Search bookmarks.</span></span> <span data-ttu-id="3f4cd-105">整合式的 Power 應用程式會出現在書籤的結果，而不必移至不同的站台或開啟另外的工具，哪些節省時間和精力。</span><span class="sxs-lookup"><span data-stu-id="3f4cd-105">Integrated Power Apps appear within a bookmark result, eliminating the need to go to a different site or open a separate tool, which saves times and effort.</span></span>
  
## <a name="what-are-power-apps"></a><span data-ttu-id="3f4cd-106">什麼是 Power 應用程式？</span><span class="sxs-lookup"><span data-stu-id="3f4cd-106">What are Power Apps?</span></span>

<span data-ttu-id="3f4cd-107">[電源應用程式](https://products.office.com/business/microsoft-powerapps)是一種服務，可讓您建置商務應用程式，在瀏覽器中或在電話或平板電腦上執行需要任何程式碼撰寫體驗。</span><span class="sxs-lookup"><span data-stu-id="3f4cd-107">[Power Apps](https://products.office.com/business/microsoft-powerapps) is a service that lets you build business apps that run in a browser or on a phone or tablet with no coding experience required.</span></span> <span data-ttu-id="3f4cd-108">深入了解：</span><span class="sxs-lookup"><span data-stu-id="3f4cd-108">Learn more:</span></span>
  
- [<span data-ttu-id="3f4cd-109">引導學習</span><span class="sxs-lookup"><span data-stu-id="3f4cd-109">Guided Learning</span></span>](https://docs.microsoft.com/learn/browse/?products=powerapps)
    
- [<span data-ttu-id="3f4cd-110">文件</span><span class="sxs-lookup"><span data-stu-id="3f4cd-110">Documentation</span></span>](https://docs.microsoft.com/powerapps/)
    
## <a name="add-a-power-app-to-a-bookmark"></a><span data-ttu-id="3f4cd-111">將 Power 應用程式新增至一個書籤</span><span class="sxs-lookup"><span data-stu-id="3f4cd-111">Add a Power App to a bookmark</span></span>

<span data-ttu-id="3f4cd-112">[電源應用程式 (https://products.office.com/business/microsoft-powerapps)工作中的任何瀏覽器，以及在任何裝置上，並採取新增少於一分鐘。</span><span class="sxs-lookup"><span data-stu-id="3f4cd-112">[Power Apps(https://products.office.com/business/microsoft-powerapps) work in any browser and on any device and take less than a minute to add.</span></span>
  
1. <span data-ttu-id="3f4cd-113">[尋找 Power 應用程式的應用程式識別碼](https://docs.microsoft.com/powerapps/maker/canvas-apps/get-sessionid#get-an-app-id)您想要整合。</span><span class="sxs-lookup"><span data-stu-id="3f4cd-113">[Find the App ID for the Power App](https://docs.microsoft.com/powerapps/maker/canvas-apps/get-sessionid#get-an-app-id) you want to integrate.</span></span>
    
2. <span data-ttu-id="3f4cd-114">在 Microsoft 365[系統管理中心](https://admin.microsoft.com)中，移至**書籤**。</span><span class="sxs-lookup"><span data-stu-id="3f4cd-114">In the Microsoft 365 [admin center](https://admin.microsoft.com), go to **Bookmarks**.</span></span>
    
3. <span data-ttu-id="3f4cd-115">新增一個書籤或尋找現有的書籤，您想要新增至 Power 應用程式。</span><span class="sxs-lookup"><span data-stu-id="3f4cd-115">Add a bookmark or find an existing bookmark that you want to add a Power App to.</span></span>
    
4. <span data-ttu-id="3f4cd-116">在書籤設定] 中，選取**Power 應用程式**，，然後選取**新增 Power 應用程式**。</span><span class="sxs-lookup"><span data-stu-id="3f4cd-116">In the bookmark settings, select **Power App**, and then select **Add a Power App**.</span></span>
    
5. <span data-ttu-id="3f4cd-117">輸入或貼上應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="3f4cd-117">Enter or paste the App ID.</span></span>
    
    <span data-ttu-id="3f4cd-118">自動新增其高度及寬度。</span><span class="sxs-lookup"><span data-stu-id="3f4cd-118">The height and width are automatically added.</span></span> <span data-ttu-id="3f4cd-119">書籤能夠同時支援直向和橫向的方向，但目前無法變更大小。</span><span class="sxs-lookup"><span data-stu-id="3f4cd-119">Bookmarks can support both portrait and landscape orientations, but currently the size can't be changed.</span></span>
    
6. <span data-ttu-id="3f4cd-120">書籤預覽顯示 Power 應用程式中的書籤結果的顯示方式。</span><span class="sxs-lookup"><span data-stu-id="3f4cd-120">The bookmark preview shows how the Power App will appear in the bookmark result.</span></span>
    
    <span data-ttu-id="3f4cd-121">在預覽 Power 應用程式是完全正常運作，以方便測試和使用。</span><span class="sxs-lookup"><span data-stu-id="3f4cd-121">The Power App in the preview is fully functional to make it easy to test and use.</span></span>
    
7. <span data-ttu-id="3f4cd-122">選取 [**發佈**]。</span><span class="sxs-lookup"><span data-stu-id="3f4cd-122">Select **Publish**.</span></span>
    
<span data-ttu-id="3f4cd-123">當 [已授權的 Microsoft Search 使用者搜尋的書籤的關鍵字或保留的關鍵字任何在[Bing](https://Bing.com)上時，Power 應用程式會出現在書籤結果。</span><span class="sxs-lookup"><span data-stu-id="3f4cd-123">When an authorized Microsoft Search user searches on [Bing](https://Bing.com) for any of the bookmark's keywords or reserved keywords, the Power App will appear in the bookmark result.</span></span>
