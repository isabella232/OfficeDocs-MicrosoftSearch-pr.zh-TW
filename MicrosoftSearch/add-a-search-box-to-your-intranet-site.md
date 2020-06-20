---
title: 將搜尋方塊新增至您的內部網路網站
ms.author: dawholl
author: dawholl
manager: kellis
ms.date: 10/31/2018
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: f980b90f-95e2-4b66-8b21-69f601ff4b50
ROBOTS: NoIndex
description: 將 Microsoft Search 的搜尋方塊新增至任何內部網路網站或頁面，以取得相關的搜尋建議並更快速尋找工作結果。
ms.openlocfilehash: af12ce4d17c2695e196f8e4d79ccd515f002f238
ms.sourcegitcommit: 92206ea179ec00b22496f6fd2866b5406449cf40
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/18/2020
ms.locfileid: "44798223"
---
# <a name="add-a-search-box-to-your-intranet-site"></a><span data-ttu-id="a0f20-103">將搜尋方塊新增至您的內部網路網站</span><span class="sxs-lookup"><span data-stu-id="a0f20-103">Add a search box to your intranet site</span></span>

<span data-ttu-id="a0f20-104">若要讓您的使用者能夠輕鬆存取組織的結果，請在 [Bing 搜尋] 方塊中新增 Microsoft 搜尋至任何內部網路網站或頁面。</span><span class="sxs-lookup"><span data-stu-id="a0f20-104">To provide your users with easy access to results from your organization, add a Microsoft Search in Bing search box to any intranet site or page.</span></span> <span data-ttu-id="a0f20-105">以下是一些優點：</span><span class="sxs-lookup"><span data-stu-id="a0f20-105">These are some of the benefits:</span></span>

- <span data-ttu-id="a0f20-106">SharePoint 或內部網路入口網站上的搜尋方塊，提供開始搜尋的熟悉、信任的進入點。</span><span class="sxs-lookup"><span data-stu-id="a0f20-106">A search box on your SharePoint or intranet portal provides a familiar, trusted entry point to start searching</span></span>
- <span data-ttu-id="a0f20-107">支援所有主要網頁瀏覽器（包括 Google Chrome 和 Microsoft Edge）</span><span class="sxs-lookup"><span data-stu-id="a0f20-107">Supports all major web browsers, including Google Chrome and Microsoft Edge</span></span>
- <span data-ttu-id="a0f20-108">只會顯示您組織的搜尋建議，永遠不會包含 web 建議</span><span class="sxs-lookup"><span data-stu-id="a0f20-108">Only search suggestions from your organization appear, web suggestions are never included</span></span>
- <span data-ttu-id="a0f20-109">讓使用者加入 Bing 工作成果頁面中的 Microsoft 搜尋，但不包括廣告和 web 結果</span><span class="sxs-lookup"><span data-stu-id="a0f20-109">Takes users to a Microsoft Search in Bing work results page, which excludes ads and web results</span></span>
- <span data-ttu-id="a0f20-110">您可以控制搜尋方塊的外觀和行為</span><span class="sxs-lookup"><span data-stu-id="a0f20-110">You control the appearance and behavior of the search box</span></span>
  
## <a name="add-a-search-box-to-an-intranet-page"></a><span data-ttu-id="a0f20-111">將搜尋方塊新增至內部網路頁面</span><span class="sxs-lookup"><span data-stu-id="a0f20-111">Add a search box to an intranet page</span></span>

<span data-ttu-id="a0f20-112">您需要將兩個元件新增至頁面：搜尋方塊的容器和啟動該搜尋方塊的指令碼。</span><span class="sxs-lookup"><span data-stu-id="a0f20-112">You need to add two elements to the page: a container for the search box and the script that powers it.</span></span>
  
```html
<div id="bfb_searchbox"></div>
<script>
    var bfbSearchBoxConfig = {
        containerSelector: "bfb_searchbox"
    };
</script>
<script async src="https://www.bing.com/business/s?k=sb"></script>
```

<span data-ttu-id="a0f20-113">在 SharePoint 傳統網站上，新增指令碼編輯器網頁組件並將指令碼放置在其中。</span><span class="sxs-lookup"><span data-stu-id="a0f20-113">On a SharePoint classic site, add a Script Editor Web Part and drop the script in it.</span></span>
  
## <a name="enable-the-search-box-for-mobile"></a><span data-ttu-id="a0f20-114">針對行動裝置啟用搜尋方塊</span><span class="sxs-lookup"><span data-stu-id="a0f20-114">Enable the search box for mobile</span></span>

<span data-ttu-id="a0f20-115">若要將內部網路網站或頁面提供給行動裝置使用者，請將 isMobile: true 新增至設定物件：</span><span class="sxs-lookup"><span data-stu-id="a0f20-115">For intranet sites or pages available to mobile users, add isMobile: true to the settings object:</span></span>
  
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

## <a name="put-focus-on-the-search-box-by-default"></a><span data-ttu-id="a0f20-116">根據預設，焦點會放置在搜尋方塊中</span><span class="sxs-lookup"><span data-stu-id="a0f20-116">Put focus on the search box by default</span></span>

<span data-ttu-id="a0f20-117">若要協助使用者加快搜尋速度，載入頁面或網站時，請將 focus: true 新增至設定物件來將游標放置在搜尋方塊中：</span><span class="sxs-lookup"><span data-stu-id="a0f20-117">To help users search faster, when the page or site loads place the cursor in the search box by adding focus: true to the settings object:</span></span>
  
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

## <a name="customize-the-appearance-of-the-search-box"></a><span data-ttu-id="a0f20-118">自訂搜尋方塊的外觀</span><span class="sxs-lookup"><span data-stu-id="a0f20-118">Customize the appearance of the search box</span></span> 

<span data-ttu-id="a0f20-119">為了協助讓搜尋方塊更符合您的內部網路的樣式，您可以使用各種不同的組態選項。</span><span class="sxs-lookup"><span data-stu-id="a0f20-119">To help the search box better fit with the style of your intranet, there are a variety of configuration options you can use.</span></span> <span data-ttu-id="a0f20-120">您可以混搭選項來符合您的需求。</span><span class="sxs-lookup"><span data-stu-id="a0f20-120">Mix and match options to suit your needs.</span></span>

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
                                                // when absent, ghost text will be "Search work"
                                                // when specified, text will be "Search <companyNameInGhostText>"
    };
</script>
<script async src="https://www.bing.com/business/s?k=sb"></script>
```

## <a name="use-an-iframe-to-embed-a-search-box"></a><span data-ttu-id="a0f20-121">使用 iFrame 來內嵌搜尋方塊</span><span class="sxs-lookup"><span data-stu-id="a0f20-121">Use an iFrame to embed a search box</span></span>

<span data-ttu-id="a0f20-122">如果該網站沒有內嵌指令碼的選項，請使用 iFrame 來新增搜尋方塊。</span><span class="sxs-lookup"><span data-stu-id="a0f20-122">If embedding a script isn't an option for the site, use an iFrame to add the search box.</span></span> <span data-ttu-id="a0f20-123">您無法自訂搜尋方塊的外觀。</span><span class="sxs-lookup"><span data-stu-id="a0f20-123">You won't be able to customize the appearance of the search box.</span></span>
  
```html
<iframe width="564" height="400" src="https://www.bing.com/business/searchbox"></iframe>
```
