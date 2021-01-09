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
ms.openlocfilehash: a050921058eac50d7588f1e71f5b0f56cc8e5752
ms.sourcegitcommit: a86265684871da86562a76c4961d0a6c1869f517
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/09/2021
ms.locfileid: "49790328"
---
# <a name="manage-custom-filters"></a><span data-ttu-id="f42be-103">管理自訂篩選</span><span class="sxs-lookup"><span data-stu-id="f42be-103">Manage custom filters</span></span>

<span data-ttu-id="f42be-104">您可以使用篩選自訂 Microsoft 搜尋體驗。</span><span class="sxs-lookup"><span data-stu-id="f42be-104">You can use filters to customize the Microsoft Search experience.</span></span> <span data-ttu-id="f42be-105">篩選可讓使用者從搜尋查詢快速精煉結果集。</span><span class="sxs-lookup"><span data-stu-id="f42be-105">Filters let users quickly refine the set of results from their search query.</span></span>

<span data-ttu-id="f42be-106">自訂的篩選可以在以 connection 屬性為基礎的垂直內部建立。</span><span class="sxs-lookup"><span data-stu-id="f42be-106">A custom filter can be created inside a vertical based on a connection property.</span></span> <span data-ttu-id="f42be-107">例如，您可以在垂直方向的 ServiceNow 連接 **上建立已發佈的 On** filter。</span><span class="sxs-lookup"><span data-stu-id="f42be-107">For example, you can create a **Published On** filter for ServiceNow connection inside a vertical.</span></span>

## <a name="create-a-filter-in-an-organizational-level-vertical"></a><span data-ttu-id="f42be-108">在組織層級中建立篩選</span><span class="sxs-lookup"><span data-stu-id="f42be-108">Create a filter in an organizational level vertical</span></span>

<span data-ttu-id="f42be-109">若要在 Microsoft 搜尋上建立篩選，請遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="f42be-109">To create a filter on Microsoft search follow these steps:</span></span>

1. <span data-ttu-id="f42be-110">在 Microsoft 365 系統管理中心中，移至 [ [縱向](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/verticals)]。</span><span class="sxs-lookup"><span data-stu-id="f42be-110">In the Microsoft 365 admin center, go to [Verticals](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/verticals).</span></span>
1. <span data-ttu-id="f42be-111">建立/編輯您要建立篩選的垂直方向</span><span class="sxs-lookup"><span data-stu-id="f42be-111">Create/Edit the vertical in which you want to create the filter</span></span>
1. <span data-ttu-id="f42be-112">流覽至嚮導中的 [篩選器] 步驟</span><span class="sxs-lookup"><span data-stu-id="f42be-112">Navigate to the 'Filters' step in the wizard</span></span>
1. <span data-ttu-id="f42be-113">按一下 [新增篩選] 並開始</span><span class="sxs-lookup"><span data-stu-id="f42be-113">Click on 'Add Filter' and get started</span></span>
1. <span data-ttu-id="f42be-114">新增篩選後，您可以檢查並儲存垂直。</span><span class="sxs-lookup"><span data-stu-id="f42be-114">After adding filters, you can review and save the vertical.</span></span>

## <a name="things-to-consider"></a><span data-ttu-id="f42be-115">考慮事項</span><span class="sxs-lookup"><span data-stu-id="f42be-115">Things to consider</span></span>

1. <span data-ttu-id="f42be-116">線上內容上存在其他篩選功能。</span><span class="sxs-lookup"><span data-stu-id="f42be-116">Additional filter capabilities exist on connection content.</span></span>

    - <span data-ttu-id="f42be-117">您也可以在 connector 來源屬性的別名上建立篩選</span><span class="sxs-lookup"><span data-stu-id="f42be-117">You can also create filter on an alias to connector source properties</span></span>
    - <span data-ttu-id="f42be-118">如果垂直具有多個連線，您可以在這些連線建立通用篩選。</span><span class="sxs-lookup"><span data-stu-id="f42be-118">If a vertical has multiple connections, you can create a common filter across these connections.</span></span> <span data-ttu-id="f42be-119">若要執行此動作，您可以在通用別名上建立篩選，以在不同的連線中使用別名來源屬性。</span><span class="sxs-lookup"><span data-stu-id="f42be-119">This can be done by creating the filter on an common alias which aliases source properties across across the different connections.</span></span> <span data-ttu-id="f42be-120">例如，您可以建立別名 **篩選 ServiceNow** 和 Jira 連線，如下所示：</span><span class="sxs-lookup"><span data-stu-id="f42be-120">For example you can create an **Author** filter across a ServiceNow and a Jira connection by creating aliases as follows:</span></span>

    | <span data-ttu-id="f42be-121">連線</span><span class="sxs-lookup"><span data-stu-id="f42be-121">Connection</span></span> | <span data-ttu-id="f42be-122">屬性	</span><span class="sxs-lookup"><span data-stu-id="f42be-122">Property</span></span> | <span data-ttu-id="f42be-123">別名</span><span class="sxs-lookup"><span data-stu-id="f42be-123">Alias</span></span> |
    | --- | --- | --- |
    | <span data-ttu-id="f42be-124">服務現在</span><span class="sxs-lookup"><span data-stu-id="f42be-124">Service Now</span></span> | <span data-ttu-id="f42be-125">擁有者</span><span class="sxs-lookup"><span data-stu-id="f42be-125">Owner</span></span> | <span data-ttu-id="f42be-126">作者</span><span class="sxs-lookup"><span data-stu-id="f42be-126">Author</span></span> |
    | <span data-ttu-id="f42be-127">Jira</span><span class="sxs-lookup"><span data-stu-id="f42be-127">Jira</span></span> | <span data-ttu-id="f42be-128">Publisher</span><span class="sxs-lookup"><span data-stu-id="f42be-128">Publisher</span></span> | <span data-ttu-id="f42be-129">作者</span><span class="sxs-lookup"><span data-stu-id="f42be-129">Author</span></span> |

1. <span data-ttu-id="f42be-130">篩選器存在於垂直範圍內。</span><span class="sxs-lookup"><span data-stu-id="f42be-130">Filters exist within the scope of a vertical.</span></span>

    - <span data-ttu-id="f42be-131">如果篩選是以組織層級的垂直方式建立，則篩選只會顯示在組織層級</span><span class="sxs-lookup"><span data-stu-id="f42be-131">If a filter is created in a vertical which is at organizational level, then the filter would only be visible at the organizational level</span></span>
    - <span data-ttu-id="f42be-132">如果篩選是以位於網站層級的垂直方式建立，則篩選只會顯示在網站層級。</span><span class="sxs-lookup"><span data-stu-id="f42be-132">If a filter is created in a vertical which is at site level, then the filter would only be visible at the site level.</span></span>

## <a name="known-limitations"></a><span data-ttu-id="f42be-133">已知限制</span><span class="sxs-lookup"><span data-stu-id="f42be-133">Known Limitations</span></span>

1. <span data-ttu-id="f42be-134">您目前只能在 string & date type managed 屬性上建立篩選。</span><span class="sxs-lookup"><span data-stu-id="f42be-134">You can currently create filters only on string & date type managed properties.</span></span>
1. <span data-ttu-id="f42be-135">您無法建立分級篩選。</span><span class="sxs-lookup"><span data-stu-id="f42be-135">You cannot create hierarchical filters.</span></span>

## <a name="resources"></a><span data-ttu-id="f42be-136">資源</span><span class="sxs-lookup"><span data-stu-id="f42be-136">Resources</span></span>

[<span data-ttu-id="f42be-137">管理類別和結果類型</span><span class="sxs-lookup"><span data-stu-id="f42be-137">Manage verticals and result types</span></span>](customize-search-page.md)
