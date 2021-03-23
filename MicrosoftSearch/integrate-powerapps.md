---
title: 整合電源應用程式
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
description: 在 Microsoft 搜尋的書簽結果中包含以瀏覽器為基礎的應用程式
ms.openlocfilehash: 52fa78c54ab6db74ef1e3679d3d32151a3f5ac10
ms.sourcegitcommit: 5df252e6d0bd67bb1b4c59418aceca8369f5fe42
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/23/2021
ms.locfileid: "51031699"
---
# <a name="integrate-power-apps-in-microsoft-search-bookmarks"></a><span data-ttu-id="7ce5b-103">整合 Microsoft 搜尋書簽中的 Power App</span><span class="sxs-lookup"><span data-stu-id="7ce5b-103">Integrate Power Apps in Microsoft Search bookmarks</span></span>
   
<span data-ttu-id="7ce5b-104">將現有的 [Microsoft Power Apps](https://products.office.com/business/microsoft-powerapps) 整合至您的 microsoft 搜尋書簽，協助您的使用者完成工作，例如輸入休假時間或報告費用。</span><span class="sxs-lookup"><span data-stu-id="7ce5b-104">Help your users complete tasks, like entering vacation time or reporting expenses, by integrating existing [Microsoft Power Apps](https://products.office.com/business/microsoft-powerapps) into your Microsoft Search bookmarks.</span></span> <span data-ttu-id="7ce5b-105">集成的 Power App 會出現在書簽結果內，不需要移至不同的網站或開啟另一個工具，以節省時間和精力。</span><span class="sxs-lookup"><span data-stu-id="7ce5b-105">Integrated Power Apps appear within a bookmark result, eliminating the need to go to a different site or open a separate tool, which saves times and effort.</span></span>
  
## <a name="what-are-power-apps"></a><span data-ttu-id="7ce5b-106">何謂電源應用程式？</span><span class="sxs-lookup"><span data-stu-id="7ce5b-106">What are Power Apps?</span></span>

<span data-ttu-id="7ce5b-107">[電源應用程式](https://products.office.com/business/microsoft-powerapps) 是一種服務，可讓您建立在瀏覽器中或在電話或平板電腦上執行的商務應用程式，不需要任何的編碼經驗。</span><span class="sxs-lookup"><span data-stu-id="7ce5b-107">[Power Apps](https://products.office.com/business/microsoft-powerapps) is a service that lets you build business apps that run in a browser or on a phone or tablet with no coding experience required.</span></span> <span data-ttu-id="7ce5b-108">深入了解：</span><span class="sxs-lookup"><span data-stu-id="7ce5b-108">Learn more:</span></span>
  
- [<span data-ttu-id="7ce5b-109">引導學習</span><span class="sxs-lookup"><span data-stu-id="7ce5b-109">Guided Learning</span></span>](/learn/browse/?products=powerapps)
    
- [<span data-ttu-id="7ce5b-110">文件</span><span class="sxs-lookup"><span data-stu-id="7ce5b-110">Documentation</span></span>](/powerapps/)
    
## <a name="add-a-power-app-to-a-bookmark"></a><span data-ttu-id="7ce5b-111">將電源 App 新增至書簽</span><span class="sxs-lookup"><span data-stu-id="7ce5b-111">Add a Power App to a bookmark</span></span>

<span data-ttu-id="7ce5b-112">[Power Apps (https://products.office.com/business/microsoft-powerapps) 可在任何瀏覽器和任何裝置上運作，而且不會有一分鐘的時間可供加入。</span><span class="sxs-lookup"><span data-stu-id="7ce5b-112">[Power Apps(https://products.office.com/business/microsoft-powerapps) work in any browser and on any device and take less than a minute to add.</span></span>
  
1. <span data-ttu-id="7ce5b-113">尋找您要整合之[電源應用程式的應用程式識別碼](/powerapps/maker/canvas-apps/get-sessionid#get-an-app-id)。</span><span class="sxs-lookup"><span data-stu-id="7ce5b-113">[Find the App ID for the Power App](/powerapps/maker/canvas-apps/get-sessionid#get-an-app-id) you want to integrate.</span></span>
    
2. <span data-ttu-id="7ce5b-114">在 Microsoft 365 系統 [管理中心](https://admin.microsoft.com)中，移至 [ **書簽**]。</span><span class="sxs-lookup"><span data-stu-id="7ce5b-114">In the Microsoft 365 [admin center](https://admin.microsoft.com), go to **Bookmarks**.</span></span>
    
3. <span data-ttu-id="7ce5b-115">新增書簽或尋找您要新增電源 App 的現有書簽。</span><span class="sxs-lookup"><span data-stu-id="7ce5b-115">Add a bookmark or find an existing bookmark that you want to add a Power App to.</span></span>
    
4. <span data-ttu-id="7ce5b-116">在 [書簽設定] 中，選取 [ **電源 app**]，然後選取 [ **新增電源 app**]。</span><span class="sxs-lookup"><span data-stu-id="7ce5b-116">In the bookmark settings, select **Power App**, and then select **Add a Power App**.</span></span>
    
5. <span data-ttu-id="7ce5b-117">輸入或貼上應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="7ce5b-117">Enter or paste the App ID.</span></span>
    
    <span data-ttu-id="7ce5b-118">會自動新增高度及寬度。</span><span class="sxs-lookup"><span data-stu-id="7ce5b-118">The height and width are automatically added.</span></span> <span data-ttu-id="7ce5b-119">書籤能夠同時支援直向和橫向的方向，但目前無法變更大小。</span><span class="sxs-lookup"><span data-stu-id="7ce5b-119">Bookmarks can support both portrait and landscape orientations, but currently the size can't be changed.</span></span>
    
6. <span data-ttu-id="7ce5b-120">[書簽預覽] 顯示超級應用程式在書簽結果中的顯示方式。</span><span class="sxs-lookup"><span data-stu-id="7ce5b-120">The bookmark preview shows how the Power App will appear in the bookmark result.</span></span>
    
    <span data-ttu-id="7ce5b-121">預覽中的 Power App 可充分運作，讓您輕鬆地進行測試和使用。</span><span class="sxs-lookup"><span data-stu-id="7ce5b-121">The Power App in the preview is fully functional to make it easy to test and use.</span></span>
    
7. <span data-ttu-id="7ce5b-122">選取 [ **發佈**]。</span><span class="sxs-lookup"><span data-stu-id="7ce5b-122">Select **Publish**.</span></span>
    
<span data-ttu-id="7ce5b-123">當授權的 Microsoft 搜尋使用者搜尋 [Bing](https://Bing.com) 的書簽的關鍵字或保留關鍵字時，會出現在書簽結果中的 Power App。</span><span class="sxs-lookup"><span data-stu-id="7ce5b-123">When an authorized Microsoft Search user searches on [Bing](https://Bing.com) for any of the bookmark's keywords or reserved keywords, the Power App will appear in the bookmark result.</span></span>