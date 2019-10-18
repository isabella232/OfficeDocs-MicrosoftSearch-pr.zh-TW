---
title: 將搜尋方塊新增至您的內部網路網站
ms.author: dawholl
author: dawholl
manager: kellis
ms.date: 10/31/2018
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Priority
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: f980b90f-95e2-4b66-8b21-69f601ff4b50
ROBOTS: NoIndex
description: 將 Microsoft Search 的搜尋方塊新增至任何內部網路網站或頁面，以取得相關的搜尋建議並更快速尋找工作結果。
ms.openlocfilehash: ea3efc224b69ffe894104068b055efe8b5882cc1
ms.sourcegitcommit: fe7f3dae4edba97071a4d127e8a27bdf4fa00d81
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/05/2019
ms.locfileid: "34727922"
---
# <a name="add-a-search-box-to-your-intranet-site"></a><span data-ttu-id="73ff1-103">將搜尋方塊新增至您的內部網路網站</span><span class="sxs-lookup"><span data-stu-id="73ff1-103">Add a search box to your intranet site</span></span>

<span data-ttu-id="73ff1-104">若要快速存取相關的搜尋建議和工作結果，請將 Microsoft Search 的搜尋方塊新增至任何內部網路網站或頁面。</span><span class="sxs-lookup"><span data-stu-id="73ff1-104">For fast access to relevant search suggestions and work results, add a Microsoft Search search box to any intranet site or page.</span></span>
  
## <a name="add-a-search-box-to-an-intranet-page"></a><span data-ttu-id="73ff1-105">將搜尋方塊新增至內部網路頁面</span><span class="sxs-lookup"><span data-stu-id="73ff1-105">Add a search box to an intranet page</span></span>

<span data-ttu-id="73ff1-106">您需要將兩個元件新增至頁面：搜尋方塊的容器和啟動該搜尋方塊的指令碼。</span><span class="sxs-lookup"><span data-stu-id="73ff1-106">You need to add two elements to the page: a container for the search box and the script that powers it.</span></span>
  
```html
<div id="bfb_searchbox"></div>
<script>
    var bfbSearchBoxConfig = {
        containerSelector: "bfb_searchbox"
    };
</script>
<script async src="https://www.bing.com/business/s?k=sb"></script>
```

<span data-ttu-id="73ff1-107">在 SharePoint 傳統網站上，新增指令碼編輯器網頁組件並將指令碼放置在其中。</span><span class="sxs-lookup"><span data-stu-id="73ff1-107">On a SharePoint classic site, add a Script Editor Web Part and drop the script in it.</span></span>
  
## <a name="enable-the-search-box-for-mobile"></a><span data-ttu-id="73ff1-108">針對行動裝置啟用搜尋方塊</span><span class="sxs-lookup"><span data-stu-id="73ff1-108">Enable the search box for mobile</span></span>

<span data-ttu-id="73ff1-109">若要將內部網路網站或頁面提供給行動裝置使用者，請將 isMobile: true 新增至設定物件：</span><span class="sxs-lookup"><span data-stu-id="73ff1-109">For intranet sites or pages available to mobile users, add isMobile: true to the settings object:</span></span>
  
```html
<div id="bfb_searchbox"></div>
<script>
    var bfbSearchBoxConfig = {
        containerSelector: "bfb_searchbox", 
        isMobile: true
    };
</script>
<script async src="https://www.bing.com/business/s?k=sb"></script>
```

## <a name="put-focus-on-the-search-box-by-default"></a><span data-ttu-id="73ff1-110">根據預設，焦點會放置在搜尋方塊中</span><span class="sxs-lookup"><span data-stu-id="73ff1-110">Put focus on the search box by default</span></span>

<span data-ttu-id="73ff1-111">若要協助使用者加快搜尋速度，載入頁面或網站時，請將 focus: true 新增至設定物件來將游標放置在搜尋方塊中：</span><span class="sxs-lookup"><span data-stu-id="73ff1-111">To help users search faster, when the page or site loads place the cursor in the search box by adding focus: true to the settings object:</span></span>
  
```html
<div id="bfb_searchbox"></div>
<script>
    var bfbSearchBoxConfig = {
        containerSelector: "bfb_searchbox",
        focus: true
    };
</script>
<script async src="https://www.bing.com/business/s?k=sb"></script>
```

## <a name="customize-the-appearance-of-the-search-box"></a><span data-ttu-id="73ff1-112">自訂搜尋方塊的外觀</span><span class="sxs-lookup"><span data-stu-id="73ff1-112">Change the appearance of the search box</span></span> 

<span data-ttu-id="73ff1-113">為了協助讓搜尋方塊更符合您的內部網路的樣式，您可以使用各種不同的組態選項。</span><span class="sxs-lookup"><span data-stu-id="73ff1-113">To help the search box better fit with the style of your intranet, there are a variety of configuration options you can use.</span></span> <span data-ttu-id="73ff1-114">您可以混搭選項來符合您的需求。</span><span class="sxs-lookup"><span data-stu-id="73ff1-114">Mix and match options to suit your needs.</span></span>

```html
<div id="bfb_searchbox"></div>
<script>
    var bfbSearchBoxConfig = {
        containerSelector: "bfb_searchbox",
        width: 560,                             // default: 560, min: 360, max: 650
        height: 40,                             // default: 40, min: 40, max: 72
        cornerRadius: 6,                        // default: 6, min: 0, max: 25                                   
        strokeOutline: true,                    // default: true
        dropShadow: true,                       // default: true
        iconColor: "#067FA6",                   // default: #067FA6
        companyNameInGhostText: "Contoso"       // default: not specified
                                                // when absent, ghost text will be "Search work and the web"
                                                // when specified, text will be "Search the web and [Contoso]"
    };
</script>
<script async src="https://www.bing.com/business/s?k=sb"></script>
```

## <a name="use-an-iframe-to-embed-a-search-box"></a><span data-ttu-id="73ff1-115">使用 iFrame 來內嵌搜尋方塊</span><span class="sxs-lookup"><span data-stu-id="73ff1-115">Use an iFrame to embed a search box</span></span>

<span data-ttu-id="73ff1-116">如果該網站沒有內嵌指令碼的選項，請使用 iFrame 來新增搜尋方塊。</span><span class="sxs-lookup"><span data-stu-id="73ff1-116">If embedding a script isn't an option for the site, use an iFrame to add the search box.</span></span> <span data-ttu-id="73ff1-117">您無法自訂搜尋方塊的外觀。</span><span class="sxs-lookup"><span data-stu-id="73ff1-117">You won't be able to customize the appearance of the search box.</span></span>
  
```html
<iframe width="564" height="400" src="https://www.bing.com/business/searchbox"></iframe>
```