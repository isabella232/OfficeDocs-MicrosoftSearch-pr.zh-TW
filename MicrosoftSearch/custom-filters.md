---
title: 管理自訂篩選
ms.author: rodhb
author: rodhb
manager: jeffkizn
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 管理自訂篩選
ms.openlocfilehash: 75273035a7825683f626464df7bbc8e294b41b6f
ms.sourcegitcommit: 59435698bece013ae64ca2a68c43455ca10e3fdf
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/05/2020
ms.locfileid: "48927378"
---
# <a name="create-custom-filters"></a><span data-ttu-id="878ca-103">建立自訂篩選</span><span class="sxs-lookup"><span data-stu-id="878ca-103">Create custom Filters</span></span>

<span data-ttu-id="878ca-104">您可以建立篩選，以自訂使用者在 Microsoft [SharePoint](https://sharepoint.com/)、microsoft [Office](https://office.com)和 microsoft search in [Bing](https://bing.com)中搜尋時所看到的搜尋體驗。</span><span class="sxs-lookup"><span data-stu-id="878ca-104">You can create filters to customize the search experience that users see when they search in Microsoft [SharePoint](https://sharepoint.com/), Microsoft [Office](https://office.com), and Microsoft Search in [Bing](https://bing.com).</span></span> <span data-ttu-id="878ca-105">篩選可讓使用者從其搜尋查詢快速縮小結果的集合。</span><span class="sxs-lookup"><span data-stu-id="878ca-105">Filters lets users quickly refine the set of results from their search query.</span></span>

<span data-ttu-id="878ca-106">自訂的篩選可以在以 connection 屬性為基礎的垂直內部建立。</span><span class="sxs-lookup"><span data-stu-id="878ca-106">A custom filter can be created inside a vertical based on a connection property.</span></span> <span data-ttu-id="878ca-107">例如，您可以在自訂垂直內為 ServiceNow 連接建立 **已發佈的 On** filter。</span><span class="sxs-lookup"><span data-stu-id="878ca-107">For example, you can create a **Published On** filter for ServiceNow connection inside a custom vertical.</span></span>

## <a name="things-to-consider"></a><span data-ttu-id="878ca-108">考慮事項</span><span class="sxs-lookup"><span data-stu-id="878ca-108">Things to consider</span></span>

1. <span data-ttu-id="878ca-109">若要在線上內容來源上建立自訂篩選，還會提供一些其他功能：</span><span class="sxs-lookup"><span data-stu-id="878ca-109">For creating custom filter on connection content source, some additional capabilities are provided:</span></span>
- <span data-ttu-id="878ca-110">您也可以在 connector 來源屬性的別名上建立篩選</span><span class="sxs-lookup"><span data-stu-id="878ca-110">You can also create filter on an alias to connector source properties</span></span>
- <span data-ttu-id="878ca-111">如果您的垂直具有多個連線，您可以在這些連線建立通用篩選。</span><span class="sxs-lookup"><span data-stu-id="878ca-111">In case your vertical has multiple connections then you can create a common filter across these connections.</span></span> <span data-ttu-id="878ca-112">若要完成此工作，您可以在通用別名上建立篩選，而這些別名來源屬性會在不同的連線。</span><span class="sxs-lookup"><span data-stu-id="878ca-112">This can be done by creating the filter on an common alias which aliases source properties across across different connections.</span></span> <span data-ttu-id="878ca-113">例如，您可以建立別名 **，使其** 跨越 ServiceNow & Jira 連線，如下所示：</span><span class="sxs-lookup"><span data-stu-id="878ca-113">For example you can create an **Author** filter across a ServiceNow & a Jira connection by creating aliases as follows:</span></span>

| <span data-ttu-id="878ca-114">連線</span><span class="sxs-lookup"><span data-stu-id="878ca-114">Connection</span></span> | <span data-ttu-id="878ca-115">屬性	</span><span class="sxs-lookup"><span data-stu-id="878ca-115">Property</span></span> | <span data-ttu-id="878ca-116">別名</span><span class="sxs-lookup"><span data-stu-id="878ca-116">Alias</span></span> |
| --- | --- | --- |
| <span data-ttu-id="878ca-117">服務現在</span><span class="sxs-lookup"><span data-stu-id="878ca-117">Service Now</span></span> | <span data-ttu-id="878ca-118">擁有者</span><span class="sxs-lookup"><span data-stu-id="878ca-118">Owner</span></span> | <span data-ttu-id="878ca-119">作者</span><span class="sxs-lookup"><span data-stu-id="878ca-119">Author</span></span> |
| <span data-ttu-id="878ca-120">Jira</span><span class="sxs-lookup"><span data-stu-id="878ca-120">Jira</span></span> | <span data-ttu-id="878ca-121">發行者</span><span class="sxs-lookup"><span data-stu-id="878ca-121">Publisher</span></span> | <span data-ttu-id="878ca-122">作者</span><span class="sxs-lookup"><span data-stu-id="878ca-122">Author</span></span> |

2. <span data-ttu-id="878ca-123">篩選器存在於垂直範圍內。</span><span class="sxs-lookup"><span data-stu-id="878ca-123">Filters exist within the scope of the vertical.</span></span> <span data-ttu-id="878ca-124">因此</span><span class="sxs-lookup"><span data-stu-id="878ca-124">Hence,</span></span>  
- <span data-ttu-id="878ca-125">如果篩選是以組織層級的垂直方式建立，則篩選只會顯示在組織層級</span><span class="sxs-lookup"><span data-stu-id="878ca-125">If a filter is created in a vertical which is at organizational level, then the filter would only be visible at the organizational level</span></span>
- <span data-ttu-id="878ca-126">如果篩選是以位於網站層級的垂直方式建立，則篩選只會顯示在網站層級。</span><span class="sxs-lookup"><span data-stu-id="878ca-126">If a filter is created in a vertical which is at site level, then the filter would only be visible at the site level.</span></span>

## <a name="steps-to-create-custom-filter"></a><span data-ttu-id="878ca-127">建立自訂篩選的步驟</span><span class="sxs-lookup"><span data-stu-id="878ca-127">Steps to Create custom filter</span></span>

### <a name="create-filter-in-organizational-level-vertical"></a><span data-ttu-id="878ca-128">在組織層級中建立篩選：</span><span class="sxs-lookup"><span data-stu-id="878ca-128">Create filter in organizational level vertical:</span></span>

<span data-ttu-id="878ca-129">若要在 Microsoft 搜尋上建立篩選，請遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="878ca-129">To create a filter on Microsoft search follow these steps:</span></span>

1. <span data-ttu-id="878ca-130">在 Microsoft 365 系統管理中心中，移至 [ [縱向](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/verticals) ] 頁面。</span><span class="sxs-lookup"><span data-stu-id="878ca-130">In the Microsoft 365 admin center, go to the [Verticals](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/verticals) page.</span></span>
2. <span data-ttu-id="878ca-131">建立/編輯您要建立篩選的垂直方向</span><span class="sxs-lookup"><span data-stu-id="878ca-131">Create/Edit the vertical in which you want to create the filter</span></span>
3. <span data-ttu-id="878ca-132">流覽至嚮導中的 [篩選器] 步驟</span><span class="sxs-lookup"><span data-stu-id="878ca-132">Navigate to the 'Filters' step in the wizard</span></span>
4. <span data-ttu-id="878ca-133">按一下 [新增篩選] 並在新增篩選後開始，您可以查看並儲存該垂直。</span><span class="sxs-lookup"><span data-stu-id="878ca-133">Click on 'Add Filter' and get started After adding filters, you can review and save the vertical.</span></span>

## <a name="known-limitations"></a><span data-ttu-id="878ca-134">已知限制</span><span class="sxs-lookup"><span data-stu-id="878ca-134">Known Limitations</span></span>

1. <span data-ttu-id="878ca-135">您目前只能在 String & Date type managed 屬性上建立篩選。</span><span class="sxs-lookup"><span data-stu-id="878ca-135">You can currently create filters only on String & Date type managed properties.</span></span>
2. <span data-ttu-id="878ca-136">您無法建立分級篩選</span><span class="sxs-lookup"><span data-stu-id="878ca-136">You cannot create hierarchical filters</span></span>

## <a name="resources"></a><span data-ttu-id="878ca-137">資源</span><span class="sxs-lookup"><span data-stu-id="878ca-137">Resources</span></span>

[<span data-ttu-id="878ca-138">自訂搜尋結果頁面</span><span class="sxs-lookup"><span data-stu-id="878ca-138">Customize search result page</span></span>](customize-search-page.md)