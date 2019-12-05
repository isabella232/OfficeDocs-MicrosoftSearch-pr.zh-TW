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
ms.openlocfilehash: bcf1c6890415fdd9ae22f28cdf6d3dec1ffcaac4
ms.sourcegitcommit: bfcab9d42e93addccd1e3875b41bc9cc1b6986cc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2019
ms.locfileid: "37948904"
---
# <a name="add-a-search-box-to-your-intranet-site"></a>將搜尋方塊新增至您的內部網路網站

若要快速存取相關的搜尋建議和工作結果，請將 Microsoft Search 的搜尋方塊新增至任何內部網路網站或頁面。
  
## <a name="add-a-search-box-to-an-intranet-page"></a>將搜尋方塊新增至內部網路頁面

您需要將兩個元件新增至頁面：搜尋方塊的容器和啟動該搜尋方塊的指令碼。
  
```html
<div id="bfb_searchbox"></div>
<script>
    var bfbSearchBoxConfig = {
        containerSelector: "bfb_searchbox"
    };
</script>
<script async src="https://www.bing.com/business/s?k=sb"></script>
```

在 SharePoint 傳統網站上，新增指令碼編輯器網頁組件並將指令碼放置在其中。
  
## <a name="enable-the-search-box-for-mobile"></a>針對行動裝置啟用搜尋方塊

若要將內部網路網站或頁面提供給行動裝置使用者，請將 isMobile: true 新增至設定物件：
  
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

## <a name="put-focus-on-the-search-box-by-default"></a>根據預設，焦點會放置在搜尋方塊中

若要協助使用者加快搜尋速度，載入頁面或網站時，請將 focus: true 新增至設定物件來將游標放置在搜尋方塊中：
  
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

## <a name="customize-the-appearance-of-the-search-box"></a>自訂搜尋方塊的外觀 

為了協助讓搜尋方塊更符合您的內部網路的樣式，您可以使用各種不同的組態選項。 您可以混搭選項來符合您的需求。

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

## <a name="use-an-iframe-to-embed-a-search-box"></a>使用 iFrame 來內嵌搜尋方塊

如果該網站沒有內嵌指令碼的選項，請使用 iFrame 來新增搜尋方塊。 您無法自訂搜尋方塊的外觀。
  
```html
<iframe width="564" height="400" src="https://www.bing.com/business/searchbox"></iframe>
```