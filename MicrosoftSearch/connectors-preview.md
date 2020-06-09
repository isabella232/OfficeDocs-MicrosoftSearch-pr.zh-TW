---
title: 連接器預覽
ms.author: mounika.narayanan
author: monaray
manager: shohara
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 瞭解 microsoft 搜尋的 Microsoft Graph 連接器預覽。
ms.openlocfilehash: 4bcd8360957be69bc701e8b356cd222de32bfc5f
ms.sourcegitcommit: 64eea81f8c1db9ee955013462a7b51612fb7d0b7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/08/2020
ms.locfileid: "44604381"
---
# <a name="microsoft-graph-connectors-preview"></a><span data-ttu-id="d8874-103">Microsoft Graph 連接器預覽</span><span class="sxs-lookup"><span data-stu-id="d8874-103">Microsoft Graph connectors preview</span></span>

<span data-ttu-id="d8874-104">Microsoft Graph 連接器和 Microsoft Search APIs （查詢和索引）目前處於預覽狀態。</span><span class="sxs-lookup"><span data-stu-id="d8874-104">Microsoft Graph connectors and Microsoft Search APIs (query and index) are currently in preview status.</span></span> <span data-ttu-id="d8874-105">若要存取連接器功能，您必須在您的租使用者中開啟 [目標版本] 選項。</span><span class="sxs-lookup"><span data-stu-id="d8874-105">To gain access to connectors functionality, you must turn on the Targeted release option in your tenant.</span></span> <span data-ttu-id="d8874-106">這是早期預覽，但沒有服務層級保證。</span><span class="sxs-lookup"><span data-stu-id="d8874-106">This is an early preview, and there's no service level guarantee.</span></span> <span data-ttu-id="d8874-107">我們鼓勵客戶嘗試連接器功能並提供意見反應。</span><span class="sxs-lookup"><span data-stu-id="d8874-107">We encourage customers to try connectors functionality and provide feedback.</span></span> <span data-ttu-id="d8874-108">在預覽期間，我們不建議使用連接器進行生產用途。</span><span class="sxs-lookup"><span data-stu-id="d8874-108">We don’t recommend using connectors for production purposes during the preview period.</span></span>

## <a name="set-up-targeted-release"></a><span data-ttu-id="d8874-109">設定目標版本</span><span class="sxs-lookup"><span data-stu-id="d8874-109">Set up Targeted release</span></span>

<span data-ttu-id="d8874-110">若要嘗試連接器，您必須為組織中的所有使用者設定 [**目標發行**選項]。</span><span class="sxs-lookup"><span data-stu-id="d8874-110">To try connectors, you must have the **Targeted release** option set for all users in your organization.</span></span> <span data-ttu-id="d8874-111">若要深入瞭解目標發行選項及設定方式，請參閱[在 Office 365 中設定標準或目標發行選項](https://docs.microsoft.com/office365/admin/manage/release-options-in-office-365?view=o365-worldwide)。</span><span class="sxs-lookup"><span data-stu-id="d8874-111">To learn more about the Targeted release option and how to set it, see [Set up the Standard or Targeted release options in Office 365](https://docs.microsoft.com/office365/admin/manage/release-options-in-office-365?view=o365-worldwide).</span></span>

## <a name="choose-a-preview-environment"></a><span data-ttu-id="d8874-112">選擇預覽環境</span><span class="sxs-lookup"><span data-stu-id="d8874-112">Choose a preview environment</span></span>

<span data-ttu-id="d8874-113">若要嘗試連接器、索引 APIs 和搜尋 APIs，我們建議這兩種方法：</span><span class="sxs-lookup"><span data-stu-id="d8874-113">To try connectors, indexing APIs, and search APIs, we recommend these two methods:</span></span>

1. <span data-ttu-id="d8874-114">**測試租**使用者。</span><span class="sxs-lookup"><span data-stu-id="d8874-114">**Test tenant**.</span></span>  <span data-ttu-id="d8874-115">我們鼓勵您使用測試租使用者來嘗試使用 Microsoft Graph 連接器預覽。</span><span class="sxs-lookup"><span data-stu-id="d8874-115">We encourage you to use a test tenant to try the Microsoft Graph connectors preview.</span></span>

2. <span data-ttu-id="d8874-116">**測試網站集合**。</span><span class="sxs-lookup"><span data-stu-id="d8874-116">**Test site collection**.</span></span> <span data-ttu-id="d8874-117">如果您沒有測試租使用者，您可以建立測試網站集合以嘗試使用連接器功能。</span><span class="sxs-lookup"><span data-stu-id="d8874-117">If you don't have a test tenant, you can create a test site collection to try out connectors functionality.</span></span> <span data-ttu-id="d8874-118">若要顯示連接器的結果，而不影響組織中任何其他位置的搜尋頁面，請自訂僅該網站集合的搜尋體驗。</span><span class="sxs-lookup"><span data-stu-id="d8874-118">To show results from connectors without impacting the search pages anywhere else in your organization, customize the search experience of only that site collection.</span></span>

## <a name="preview-limitations"></a><span data-ttu-id="d8874-119">預覽限制</span><span class="sxs-lookup"><span data-stu-id="d8874-119">Preview limitations</span></span>

<span data-ttu-id="d8874-120">預覽版本有下列限制：</span><span class="sxs-lookup"><span data-stu-id="d8874-120">The preview release has the following limitations:</span></span>

* <span data-ttu-id="d8874-121">接收輸送量會限制每秒大約四個專案。</span><span class="sxs-lookup"><span data-stu-id="d8874-121">Ingestion throughput is throttled at about four items per second.</span></span>

* <span data-ttu-id="d8874-122">不支援架構更新。</span><span class="sxs-lookup"><span data-stu-id="d8874-122">There's no support for schema updates.</span></span> <span data-ttu-id="d8874-123">建立連線設定後，就無法更新架構。</span><span class="sxs-lookup"><span data-stu-id="d8874-123">After you create a connection setup, there's no way to update the schema.</span></span> <span data-ttu-id="d8874-124">您只可刪除並重新建立連線。</span><span class="sxs-lookup"><span data-stu-id="d8874-124">You can only delete and re-create the connection.</span></span>

* <span data-ttu-id="d8874-125">已編制索引的內容只會顯示在自訂垂直的搜尋結果頁面中。</span><span class="sxs-lookup"><span data-stu-id="d8874-125">Indexed content only shows up in the search results page under a custom vertical.</span></span> <span data-ttu-id="d8874-126">這種限制適用于具有自訂類型的內容。</span><span class="sxs-lookup"><span data-stu-id="d8874-126">This restriction applies to content with custom types.</span></span>

* <span data-ttu-id="d8874-127">您在預覽期間設定的任何連線，都可能需要刪除並重新建立。</span><span class="sxs-lookup"><span data-stu-id="d8874-127">Any connection you set up during the preview period might need to be deleted and re-created.</span></span> <span data-ttu-id="d8874-128">如果這些連線與改進產品所做的變更不相容，這些連線將無法運作。</span><span class="sxs-lookup"><span data-stu-id="d8874-128">Those connections won't work anymore if they're incompatible with changes made to improve the product.</span></span>

* <span data-ttu-id="d8874-129">連接限制。</span><span class="sxs-lookup"><span data-stu-id="d8874-129">There's a connections limit.</span></span> <span data-ttu-id="d8874-130">每個租使用者最多可以建立10個連接。</span><span class="sxs-lookup"><span data-stu-id="d8874-130">Each tenant can create up to 10 connections.</span></span>

* <span data-ttu-id="d8874-131">來源存放庫大小。</span><span class="sxs-lookup"><span data-stu-id="d8874-131">Source repository size.</span></span> <span data-ttu-id="d8874-132">建議您預覽具有大約200000專案來源存放庫的連接器，因為這是我們經過測試的搜尋比例限制。</span><span class="sxs-lookup"><span data-stu-id="d8874-132">We recommend that you preview connectors with a source repository of about 200,000 items as this is our tested search scale limit.</span></span> <span data-ttu-id="d8874-133">我們正在努力改進搜尋效能，而且我們預計會在不久的未來支援較大的存放庫大小。</span><span class="sxs-lookup"><span data-stu-id="d8874-133">We are working on improving the performance of search, and we expect to support for larger repository sizes in the near future.</span></span>

* <span data-ttu-id="d8874-134">無法使用 [編輯連線支援]。</span><span class="sxs-lookup"><span data-stu-id="d8874-134">Edit support for connection is not available.</span></span> <span data-ttu-id="d8874-135">建立連線後，就無法編輯或變更它。</span><span class="sxs-lookup"><span data-stu-id="d8874-135">Once the connection has been created, you cannot edit or change it.</span></span> <span data-ttu-id="d8874-136">如果您需要變更任何詳細資料，您必須刪除並重新建立連線。</span><span class="sxs-lookup"><span data-stu-id="d8874-136">If you need to change any details, you must delete and recreate the connection.</span></span>

* <span data-ttu-id="d8874-137">僅能在自訂的縱向搜尋連接器內容。</span><span class="sxs-lookup"><span data-stu-id="d8874-137">Connector content can only be searched on custom verticals.</span></span>

* <span data-ttu-id="d8874-138">每個自訂垂直中只會顯示一個連線的連接器內容，而且需要產生結果類型。</span><span class="sxs-lookup"><span data-stu-id="d8874-138">Connector content from only one connection can be displayed in each custom vertical and requires result type creation.</span></span>
