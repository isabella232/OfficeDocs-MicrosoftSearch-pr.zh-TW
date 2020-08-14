---
title: 自訂搜尋結果版面配置
ms.author: jypal
author: jypal6
manager: jeffkizn
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 使用適應性卡，建立配置以查看自訂的搜尋結果
ms.openlocfilehash: e31be1f9c1602fcd696c99d584388facee22df74
ms.sourcegitcommit: c22e8c3dcc53857da677db98a1a2b7d5ca2c6170
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2020
ms.locfileid: "41721775"
---
<!-- markdownlint-disable no-hard-tabs -->
# <a name="create-a-layout-to-customize-search-results"></a><span data-ttu-id="77ed5-103">建立版式以自訂搜尋結果</span><span class="sxs-lookup"><span data-stu-id="77ed5-103">Create a layout to customize search results</span></span>

<span data-ttu-id="77ed5-104">您可以使用 [搜尋版面配置設計工具]，設計自訂垂直方向的結果版面配置。</span><span class="sxs-lookup"><span data-stu-id="77ed5-104">You can design the result layout for a custom vertical using the search layout designer.</span></span> <span data-ttu-id="77ed5-105">您可以選擇版面設計工具中提供的範本，以開始設計版面配置，並在符合您的需求時加以使用。</span><span class="sxs-lookup"><span data-stu-id="77ed5-105">You can start designing the layout by choosing templates offered in the layout designer and using them if they fit your requirements.</span></span> <span data-ttu-id="77ed5-106">或者，您可以選擇以各種方式編輯這些範本，以符合您的需求。</span><span class="sxs-lookup"><span data-stu-id="77ed5-106">Or you can choose to edit these templates in various ways to fit your requirements.</span></span> <span data-ttu-id="77ed5-107">例如，新增/移除影像、新增/移除文字，以及修改文字。</span><span class="sxs-lookup"><span data-stu-id="77ed5-107">For example, add/remove images, add/remove text, and modify text.</span></span> <span data-ttu-id="77ed5-108">若所有範本都不符合您的需求，您可以選擇使用空白範本來開始設計您的版面配置。</span><span class="sxs-lookup"><span data-stu-id="77ed5-108">If none of the templates meet your requirements, you can choose to start designing your layout using a blank template.</span></span>  

<span data-ttu-id="77ed5-109">準備好版面配置之後，請使用 [自我調整卡範本語言](https://docs.microsoft.com/adaptive-cards/templating/language) 來建立結果版面 JSON，用來定義結果類型。</span><span class="sxs-lookup"><span data-stu-id="77ed5-109">After the layout is ready, use the [Adaptive Cards Template language](https://docs.microsoft.com/adaptive-cards/templating/language) to create a result layout JSON that's used to define a result type.</span></span> <span data-ttu-id="77ed5-110">您可以使用版面配置設計工具中的對應步驟，將結果屬性對應至 layout。</span><span class="sxs-lookup"><span data-stu-id="77ed5-110">You map the result properties to the layout using the Mapping step in the layout designer.</span></span>  

## <a name="create-a-layout-on-your-own"></a><span data-ttu-id="77ed5-111">自行建立版面配置</span><span class="sxs-lookup"><span data-stu-id="77ed5-111">Create a layout on your own</span></span>

<span data-ttu-id="77ed5-112">您必須瞭解 [自訂卡](https://docs.microsoft.com/adaptive-cards/authoring-cards/getting-started) 及其 [架構](https://adaptivecards.io/explorer/)，才能自行建立版面配置。</span><span class="sxs-lookup"><span data-stu-id="77ed5-112">Creating a layout on your own requires knowledge of [adaptive cards](https://docs.microsoft.com/adaptive-cards/authoring-cards/getting-started) and their [schema](https://adaptivecards.io/explorer/).</span></span> <span data-ttu-id="77ed5-113">搜尋結果版面配置使用自我調整卡所提供之元素的子集，您可以使用版面配置設計工具來瞭解支援的元素集合。</span><span class="sxs-lookup"><span data-stu-id="77ed5-113">Search result layout uses a subset of the elements offered by adaptive cards, and you can use the layout designer to learn about the supported set of elements.</span></span>  

<span data-ttu-id="77ed5-114">建立您自己的版面配置時，請使用連接器中的資料建立自我調整卡的版面配置，然後完成 layout。</span><span class="sxs-lookup"><span data-stu-id="77ed5-114">While creating your own layout, create the adaptive card layout using data from your connector, and then finalize the layout.</span></span>
<span data-ttu-id="77ed5-115">建立您自己的版面配置有兩個主要步驟：</span><span class="sxs-lookup"><span data-stu-id="77ed5-115">There are two main steps in creating your own layout:</span></span>

- <span data-ttu-id="77ed5-116">設計版面配置。</span><span class="sxs-lookup"><span data-stu-id="77ed5-116">Design the layout.</span></span>
- <span data-ttu-id="77ed5-117">將資料與範本分開。</span><span class="sxs-lookup"><span data-stu-id="77ed5-117">Separate the data from the template.</span></span>

### <a name="design-the-layout"></a><span data-ttu-id="77ed5-118">設計版面配置</span><span class="sxs-lookup"><span data-stu-id="77ed5-118">Design the layout</span></span>

<span data-ttu-id="77ed5-119">在這個範例中，我們會顯示具有頁首、連結及描述文字的版面配置。</span><span class="sxs-lookup"><span data-stu-id="77ed5-119">In this example, we show a layout with a header, link, and descriptive text.</span></span>

![具有標頭、連結及描述的版面配置範例。](media/Verts-ExampleLayout.png)

<span data-ttu-id="77ed5-121">以下是版面配置的關聯 JSON 檔案：</span><span class="sxs-lookup"><span data-stu-id="77ed5-121">And here's the layout's associated JSON file:</span></span>

```json
{
    "type": "AdaptiveCard",
    "version": "1.0",
     "body": [
{

            "type": "ColumnSet",
             "columns": [
                 {
                     "type": "Column",
                     "width": 8,
                     "items": [
                         {
                             "type": "TextBlock",
                             "text": "Contoso Marketing Analysis - Q3 FY18",
                             "color": "Accent",
                             "size": "Medium",
                             "spacing": "None",
                             "$when": "{title != \"\"}",
                             "weight": "Bolder"
                        },
                        {
                        "type": "TextBlock",  
                        "text": "https://contoso.com/hr/link",
                        "spacing": "None",  
                        "color": "Dark",
                        "weight": "Bolder"

                        },

                        {  
                        "type": "TextBlock",
                        "text": "Marketing team at Contoso.., and looking at the Contoso Marketing documents on the team site. This contains the data from FY20 and will taken over to FY21...Marketing Planning is ongoing for FY20..",  
                        "wrap": true,
                        "maxLines": 2,
                        "spacing": "Medium"
                        }
                        ],

                    "horizontalAlignment": "Center",
                    "spacing": "None"

                }

            ]

        }
        ],

    "$schema": "http://adaptivecards.io/schemas/adaptive-card.json"
}
```

### <a name="separate-the-data-from-the-layout"></a><span data-ttu-id="77ed5-122">分隔資料與版面配置</span><span class="sxs-lookup"><span data-stu-id="77ed5-122">Separate the data from the layout</span></span>

<span data-ttu-id="77ed5-123">您可以從版面配置中分隔資料，並系結資料。</span><span class="sxs-lookup"><span data-stu-id="77ed5-123">You can separate the data from the layout and bind the data.</span></span>

<span data-ttu-id="77ed5-124">以下是系結資料後的版面配置 JSON：</span><span class="sxs-lookup"><span data-stu-id="77ed5-124">Here's Layout JSON after binding the data:</span></span>

```json
{

    "type": "AdaptiveCard",
    "version": "1.0",
    "body": [
    {
    "type": "ColumnSet",
"columns": [

                {
                "type": "Column",
                "width": 8,
                "items": [
                {
                "type": "TextBlock",
                "text": "[{title}]({titleUrl})",
                "color": "Accent",
                "size": "Medium",
                "spacing": "None",
                "weight": "Bolder"

                 },
                 {
                 "type": "TextBlock",
                 "text": "{link}",
                 "spacing": "None",
                 "color": "Dark",
                 "weight": "Bolder"
                 },
                 {
                 "type": "TextBlock",
                 "text": "{description}",
                 "wrap": true,
                 "maxLines": 2,
                 "spacing": "Medium"
                 }
                 ],
                 "horizontalAlignment": "Center",
                 "spacing": "None"
                 }
                 ]

        }

    ],

    "$schema": "http://adaptivecards.io/schemas/adaptive-card.json"
}
```

<span data-ttu-id="77ed5-125">資料範例：在**預覽模式**中，指定**範例資料編輯器**中的範例資料，以查看資料繫結卡。</span><span class="sxs-lookup"><span data-stu-id="77ed5-125">Sample data: Specify sample data in the **Sample Data Editor** to view the data-bound card when in **Preview Mode**.</span></span>

```json
{

    "title": "Contoso Marketing Analysis - Q3 FY18",
    "titleUrl": "https://contoso.com/hr/link",
    "link": "https://contoso.com/hr/link",
    "description": "Marketing team, and looking at the Contoso Marketing documents on the team site. Yo can't see right...Marketing Planning presentation?"

}
```

## <a name="map-the-layout-to-the-result-properties"></a><span data-ttu-id="77ed5-126">將版面配置對應至結果屬性</span><span class="sxs-lookup"><span data-stu-id="77ed5-126">Map the layout to the result properties</span></span>

<span data-ttu-id="77ed5-127">您必須將版面配置的每個欄位對應到 result 屬性或連接器屬性，以產生結果版面配置 JSON。</span><span class="sxs-lookup"><span data-stu-id="77ed5-127">You must map each field of the layout to a result property or a connector property to generate the result layout JSON.</span></span>

![在 [搜尋版面配置設計] 頁面上，具有選取欄位及開啟屬性窗格之範例版面配置的螢幕抓入。](media/Verts-SearchLayoutDesigner.png)

<span data-ttu-id="77ed5-129">選取版面配置中的欄位，以反白顯示需要對應的變數。</span><span class="sxs-lookup"><span data-stu-id="77ed5-129">Select a field in the layout to highlight the variables that need to be mapped.</span></span> <span data-ttu-id="77ed5-130">您可以將多個變數用於單一欄位，而且所有欄位都必須對應至 result 屬性。</span><span class="sxs-lookup"><span data-stu-id="77ed5-130">You can use multiple variables for a single field, and all fields must be mapped to the result properties.</span></span>

## <a name="things-to-consider"></a><span data-ttu-id="77ed5-131">考慮事項</span><span class="sxs-lookup"><span data-stu-id="77ed5-131">Things to consider</span></span>

<span data-ttu-id="77ed5-132">開始之前，請先執行一些工作，您應該避免使用一些事項，以確保您的版面配置順利。</span><span class="sxs-lookup"><span data-stu-id="77ed5-132">Before you get started, there are a few things that you should do and a few things you should avoid to ensure that your layouts will be successful.</span></span>

### <a name="do"></a><span data-ttu-id="77ed5-133">要</span><span class="sxs-lookup"><span data-stu-id="77ed5-133">Do</span></span>

- <span data-ttu-id="77ed5-134">若要使用靜態連結的徽標和 result 屬性，請編輯範本，以在版面配置中提供標誌連結。</span><span class="sxs-lookup"><span data-stu-id="77ed5-134">Edit a template to provide the logo link in the layout if you're using static links for logos and not result properties.</span></span>
- <span data-ttu-id="77ed5-135">針對結果 JSON 中所用 result 屬性沒有傳回資料的情況，驗證結果版面配置。</span><span class="sxs-lookup"><span data-stu-id="77ed5-135">Validate the result layout for scenarios where no data is returned for a result property used in the result JSON.</span></span> <span data-ttu-id="77ed5-136">若 `$when` 屬性不包含資料，請使用條件來隱藏元素。</span><span class="sxs-lookup"><span data-stu-id="77ed5-136">Use the `$when` condition to hide an element if the property doesn't contain data.</span></span>  
- <span data-ttu-id="77ed5-137">請確定 `$when` condition 和 result 屬性的資料類型相符。</span><span class="sxs-lookup"><span data-stu-id="77ed5-137">Make sure that data types of the `$when` condition and the result property match.</span></span> <span data-ttu-id="77ed5-138">例如， `Number` `Text` 在條件中不會比較 `$when` 。</span><span class="sxs-lookup"><span data-stu-id="77ed5-138">For example, don't compare `Number` with `Text` in the `$when` condition.</span></span>  
- <span data-ttu-id="77ed5-139">設計結果版面配置時，請考慮主題需求。</span><span class="sxs-lookup"><span data-stu-id="77ed5-139">Think of theme requirements when designing a result layout.</span></span>  
- <span data-ttu-id="77ed5-140">請確定 `Textblock`   元素可以處理動態內容。</span><span class="sxs-lookup"><span data-stu-id="77ed5-140">Make sure that the `Textblock` element can handle dynamic content.</span></span> <span data-ttu-id="77ed5-141">您可以使用 `wrap` 和 `maxLines` 元素屬性來達到此目的。</span><span class="sxs-lookup"><span data-stu-id="77ed5-141">You can use the `wrap` and `maxLines` element properties for this purpose.</span></span>
- <span data-ttu-id="77ed5-142">使用在 Markdown 中時，正確地格式化日期 `{DATE()}` 。</span><span class="sxs-lookup"><span data-stu-id="77ed5-142">Properly format the date when using `{DATE()}` in Markdown.</span></span>  

### <a name="dont"></a><span data-ttu-id="77ed5-143">不要</span><span class="sxs-lookup"><span data-stu-id="77ed5-143">Don't</span></span>

- <span data-ttu-id="77ed5-144">綁定值時，請勿定義不正確資料類型。</span><span class="sxs-lookup"><span data-stu-id="77ed5-144">Don't define invalid data types when binding values.</span></span> <span data-ttu-id="77ed5-145">如需資料類型的相關資訊，請參閱 [管理搜尋架構](https://docs.microsoft.com/sharepoint/search/manage-the-search-schema)。</span><span class="sxs-lookup"><span data-stu-id="77ed5-145">For more information about data types, see [Manage the Search schema](https://docs.microsoft.com/sharepoint/search/manage-the-search-schema).</span></span>
- <span data-ttu-id="77ed5-146">請遵循結果版面 JSON 的最大高度，避免在結果頁面上裁剪結果。</span><span class="sxs-lookup"><span data-stu-id="77ed5-146">Avoid cropping the result on the result page by following the maximum height of the result layout JSON.</span></span> <span data-ttu-id="77ed5-147">如果您超出結果版面配置的最大高度，將會在結果頁面上裁剪結果。</span><span class="sxs-lookup"><span data-stu-id="77ed5-147">If you exceed the maximum height of the result layout, the result will be cropped on the result page.</span></span>
- <span data-ttu-id="77ed5-148">不使用 `px` 元素屬性中的值。</span><span class="sxs-lookup"><span data-stu-id="77ed5-148">Don't use `px` values in element properties.</span></span>

## <a name="resources"></a><span data-ttu-id="77ed5-149">資源</span><span class="sxs-lookup"><span data-stu-id="77ed5-149">Resources</span></span>

[<span data-ttu-id="77ed5-150">自訂搜尋結果頁面</span><span class="sxs-lookup"><span data-stu-id="77ed5-150">Customize search result page</span></span>](customize-search-page.md)

[<span data-ttu-id="77ed5-151">自我調整卡片</span><span class="sxs-lookup"><span data-stu-id="77ed5-151">Adaptive cards</span></span>](https://docs.microsoft.com/adaptive-cards/authoring-cards/getting-started)

[<span data-ttu-id="77ed5-152">自我調整卡片範本語言</span><span class="sxs-lookup"><span data-stu-id="77ed5-152">Adaptive Cards Template language</span></span>](https://docs.microsoft.com/adaptive-cards/templating/language)

[<span data-ttu-id="77ed5-153">自我調整卡片架構</span><span class="sxs-lookup"><span data-stu-id="77ed5-153">Adaptive card schema</span></span>](https://adaptivecards.io/explorer/)
