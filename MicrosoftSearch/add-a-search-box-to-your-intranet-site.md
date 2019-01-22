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
description: 取得相關搜尋建議並尋找更快的工作結果將 Microsoft Search 的搜尋方塊新增至內部網路網站或頁面。
ms.openlocfilehash: a27b4d79e8795cdd2749c12119709f97710061e7
ms.sourcegitcommit: bf52cc63b75f2e0324a716fe65da47702956b722
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/18/2019
ms.locfileid: "29380138"
---
# <a name="add-a-search-box-to-your-intranet-site"></a><span data-ttu-id="2614d-103">將搜尋方塊新增至您的內部網路網站</span><span class="sxs-lookup"><span data-stu-id="2614d-103">Add a search box to your intranet site</span></span>

<span data-ttu-id="2614d-104">針對快地存取相關的搜尋建議及工作結果，新增 Microsoft Search 的搜尋] 方塊中的任何內部網路網站或頁面。</span><span class="sxs-lookup"><span data-stu-id="2614d-104">For fast access to relevant search suggestions and work results, add a Microsoft Search search box to any intranet site or page.</span></span>
  
## <a name="add-a-search-box-to-an-intranet-page"></a><span data-ttu-id="2614d-105">新增至內部網路] 頁面上的搜尋方塊</span><span class="sxs-lookup"><span data-stu-id="2614d-105">Add a search box to an intranet page</span></span>

<span data-ttu-id="2614d-106">您需要將兩個項目新增至頁面： 在搜尋方塊及力量它的指令碼的容器。</span><span class="sxs-lookup"><span data-stu-id="2614d-106">You need to add two elements to the page: a container for the search box and the script that powers it.</span></span>
  
```html
<div id="bfb_searchbox"></div>
<script>
    var bfbSearchBoxConfig = {
        containerSelector: "bfb_searchbox"
    };
</script>
<script async src="https://www.bing.com/business/s?k=sb"></script>
```

<span data-ttu-id="2614d-107">在 「 SharePoint 傳統網站中的指令碼編輯器網頁組件新增並捨棄指令碼中。</span><span class="sxs-lookup"><span data-stu-id="2614d-107">On a SharePoint classic site, add a Script Editor Web Part and drop the script in it.</span></span>
  
## <a name="enable-the-search-box-for-mobile"></a><span data-ttu-id="2614d-108">啟用 [搜尋] 方塊中的行動電話</span><span class="sxs-lookup"><span data-stu-id="2614d-108">Enable the search box for mobile</span></span>

<span data-ttu-id="2614d-109">針對內部網路網站或行動裝置使用者可用的頁面，新增 [isMobile: true 是表示設定物件：</span><span class="sxs-lookup"><span data-stu-id="2614d-109">For intranet sites or pages available to mobile users, add isMobile: true to the settings object:</span></span>
  
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

## <a name="put-focus-on-the-search-box-by-default"></a><span data-ttu-id="2614d-110">預設將焦點放在搜尋方塊</span><span class="sxs-lookup"><span data-stu-id="2614d-110">Put focus on the search box by default</span></span>

<span data-ttu-id="2614d-111">若要協助使用者] 頁面上或站台載入游標放在搜尋方塊中新增焦點時，速度，搜尋： true 是表示設定物件：</span><span class="sxs-lookup"><span data-stu-id="2614d-111">To help users search faster, when the page or site loads place the cursor in the search box by adding focus: true to the settings object:</span></span>
  
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

## <a name="use-an-iframe-to-embed-a-search-box"></a><span data-ttu-id="2614d-112">使用 iFrame 內嵌在搜尋方塊</span><span class="sxs-lookup"><span data-stu-id="2614d-112">Use an iFrame to embed a search box</span></span>

<span data-ttu-id="2614d-113">如果嵌入指令碼不是網站的選項，可用於 iFrame 新增搜尋方塊：</span><span class="sxs-lookup"><span data-stu-id="2614d-113">If embedding a script isn't an option for the site, use an iFrame to add the search box:</span></span>
  
```html
<iframe width="564" height="400" src="https://www.bing.com/business/searchbox"></iframe>
```
