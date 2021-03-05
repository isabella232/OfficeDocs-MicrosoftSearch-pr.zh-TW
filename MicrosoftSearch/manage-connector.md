---
title: 管理 microsoft 搜尋的 Microsoft Graph 連接器
ms.author: monaray
author: monaray97
manager: mnirkhe
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 管理 microsoft Search 的 Microsoft Graph 連接器。
ms.openlocfilehash: 488b6e9452e381f8fc64ad06c6f063aa170ca7f5
ms.sourcegitcommit: 3ed4d21510020045d25e8c5b7e168013d96c1b7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "50464038"
---
<!-- markdownlint-disable no-inline-html -->

# <a name="monitor-your-connections"></a><span data-ttu-id="5f4c9-103">監控您的連線</span><span class="sxs-lookup"><span data-stu-id="5f4c9-103">Monitor your connections</span></span>

<span data-ttu-id="5f4c9-104">若要存取和管理您的連接器，您必須指定為您租使用者的「搜尋管理員」。</span><span class="sxs-lookup"><span data-stu-id="5f4c9-104">To access and manage your connectors, you must be designated as a search administrator for your tenant.</span></span> <span data-ttu-id="5f4c9-105">請與您的租使用者管理員聯繫，為您提供搜尋系統管理員角色。</span><span class="sxs-lookup"><span data-stu-id="5f4c9-105">Contact your tenant administrator to provision you for the search administrator role.</span></span>

## <a name="connection-operations"></a><span data-ttu-id="5f4c9-106">連接作業</span><span class="sxs-lookup"><span data-stu-id="5f4c9-106">Connection Operations</span></span>

<span data-ttu-id="5f4c9-107">流覽至[Microsoft 365 admin center](https://admin.microsoft.com)中的 [[連接器]](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors)索引標籤。</span><span class="sxs-lookup"><span data-stu-id="5f4c9-107">Navigate to the [Connectors tab](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors) in the [Microsoft 365 admin center](https://admin.microsoft.com).</span></span>

<span data-ttu-id="5f4c9-108">針對每個連接器類型， [Microsoft 365 系統管理中心](https://admin.microsoft.com) 支援下表所示的作業：</span><span class="sxs-lookup"><span data-stu-id="5f4c9-108">For each connector type, the [Microsoft 365 admin center](https://admin.microsoft.com) supports the operations shown in the following table:</span></span>

<span data-ttu-id="5f4c9-109">作業</span><span class="sxs-lookup"><span data-stu-id="5f4c9-109">Operation</span></span> | <span data-ttu-id="5f4c9-110">Microsoft 建立的連接器</span><span class="sxs-lookup"><span data-stu-id="5f4c9-110">Microsoft-built connector</span></span> | <span data-ttu-id="5f4c9-111">夥伴或自訂建立的連接器</span><span class="sxs-lookup"><span data-stu-id="5f4c9-111">Partner or custom-built connector</span></span>
--- | --- | ---
<span data-ttu-id="5f4c9-112">新增連線</span><span class="sxs-lookup"><span data-stu-id="5f4c9-112">Add a connection</span></span> | <span data-ttu-id="5f4c9-113">： heavy_check_mark： (請參閱 [設定您的 Microsoft 建連接器](configure-connector.md)) </span><span class="sxs-lookup"><span data-stu-id="5f4c9-113">:heavy_check_mark: (See [Configure your Microsoft-built connector](configure-connector.md))</span></span> | <span data-ttu-id="5f4c9-114">： x： (參照您的合作夥伴或自訂的連接器 admin UX) </span><span class="sxs-lookup"><span data-stu-id="5f4c9-114">:x: (Refer to your partner or custom-built connector admin UX)</span></span>
<span data-ttu-id="5f4c9-115">刪除連線</span><span class="sxs-lookup"><span data-stu-id="5f4c9-115">Delete a connection</span></span> | <span data-ttu-id="5f4c9-116">： heavy_check_mark：</span><span class="sxs-lookup"><span data-stu-id="5f4c9-116">:heavy_check_mark:</span></span> | <span data-ttu-id="5f4c9-117">： heavy_check_mark：</span><span class="sxs-lookup"><span data-stu-id="5f4c9-117">:heavy_check_mark:</span></span>
<span data-ttu-id="5f4c9-118">編輯已發佈的連線</span><span class="sxs-lookup"><span data-stu-id="5f4c9-118">Edit a published connection</span></span> | <span data-ttu-id="5f4c9-119">： heavy_check_mark： Name</span><span class="sxs-lookup"><span data-stu-id="5f4c9-119">:heavy_check_mark: Name</span></span><br></br> <span data-ttu-id="5f4c9-120">： heavy_check_mark： Description</span><span class="sxs-lookup"><span data-stu-id="5f4c9-120">:heavy_check_mark: Description</span></span><br></br> <span data-ttu-id="5f4c9-121">： heavy_check_mark：外部資料源的驗證認證</span><span class="sxs-lookup"><span data-stu-id="5f4c9-121">:heavy_check_mark: Authentication credentials for your external data source</span></span><br></br> <span data-ttu-id="5f4c9-122">： heavy_check_mark：內部部署資料來源的閘道認證</span><span class="sxs-lookup"><span data-stu-id="5f4c9-122">:heavy_check_mark: Gateway credentials for your on-premises data source</span></span><br></br> <span data-ttu-id="5f4c9-123">： heavy_check_mark：重新整理排程</span><span class="sxs-lookup"><span data-stu-id="5f4c9-123">:heavy_check_mark: Refresh schedule</span></span><br></br> | <span data-ttu-id="5f4c9-124">： heavy_check_mark： Name</span><span class="sxs-lookup"><span data-stu-id="5f4c9-124">:heavy_check_mark: Name</span></span><br></br> <span data-ttu-id="5f4c9-125">： heavy_check_mark： Description</span><span class="sxs-lookup"><span data-stu-id="5f4c9-125">:heavy_check_mark: Description</span></span>
<span data-ttu-id="5f4c9-126">編輯拔模連接</span><span class="sxs-lookup"><span data-stu-id="5f4c9-126">Edit a draft connection</span></span> | <span data-ttu-id="5f4c9-127">： heavy_check_mark：</span><span class="sxs-lookup"><span data-stu-id="5f4c9-127">:heavy_check_mark:</span></span> | <span data-ttu-id="5f4c9-128">軸</span><span class="sxs-lookup"><span data-stu-id="5f4c9-128">:x:</span></span>

## <a name="monitor-your-connection-status"></a><span data-ttu-id="5f4c9-129">監視您的線上狀態</span><span class="sxs-lookup"><span data-stu-id="5f4c9-129">Monitor your connection status</span></span>

<span data-ttu-id="5f4c9-130">在您建立連線後，已處理的專案數目會顯示在 [ **Microsoft 搜尋**] 頁面上的 [**連接器**] 索引標籤上。</span><span class="sxs-lookup"><span data-stu-id="5f4c9-130">After you create a connection, the number of processed items shows on the **Connectors** tab on the **Microsoft Search** page.</span></span> <span data-ttu-id="5f4c9-131">在初次完整編目成功完成之後，會顯示定期增加編目的進度。</span><span class="sxs-lookup"><span data-stu-id="5f4c9-131">After the initial full crawl completes successfully, the progress for periodic incremental crawls displays.</span></span> <span data-ttu-id="5f4c9-132">此頁面提供連接器之日常作業的相關資訊，以及記錄檔及錯誤歷程記錄的概覽。</span><span class="sxs-lookup"><span data-stu-id="5f4c9-132">This page provides information about the connector's day-to-day operations and an overview of the logs and error history.</span></span>

<span data-ttu-id="5f4c9-133">每個連線會在 [ **狀態** ] 欄中顯示四個狀態：</span><span class="sxs-lookup"><span data-stu-id="5f4c9-133">Four states show up in the **Status** column against each connection:</span></span>

* <span data-ttu-id="5f4c9-134">**同步** 處理。</span><span class="sxs-lookup"><span data-stu-id="5f4c9-134">**Syncing**.</span></span> <span data-ttu-id="5f4c9-135">連接器會編目來源中的資料，以編制現有專案的索引並進行任何更新。</span><span class="sxs-lookup"><span data-stu-id="5f4c9-135">The connector is crawling the data from the source to index the existing items and make any updates.</span></span>

* <span data-ttu-id="5f4c9-136">**已啟用**：連線已啟用，且沒有對其執行的作用中編目。</span><span class="sxs-lookup"><span data-stu-id="5f4c9-136">**Enabled**: The connection is enabled, and there's no active crawl running against it.</span></span> <span data-ttu-id="5f4c9-137">**上次同步處理時間** 表示上次成功編目的時間。</span><span class="sxs-lookup"><span data-stu-id="5f4c9-137">**Last sync time** indicates when the last successful crawl happened.</span></span> <span data-ttu-id="5f4c9-138">連線為最新的同步處理時間。</span><span class="sxs-lookup"><span data-stu-id="5f4c9-138">The connection is as fresh as the last sync time.</span></span>

* <span data-ttu-id="5f4c9-139">已 **暫停**。</span><span class="sxs-lookup"><span data-stu-id="5f4c9-139">**Paused**.</span></span> <span data-ttu-id="5f4c9-140">管理員會透過 pause 選項暫停編目。</span><span class="sxs-lookup"><span data-stu-id="5f4c9-140">The crawls are paused by the admins through the pause option.</span></span> <span data-ttu-id="5f4c9-141">下一個編目只會在手動恢復時執行。</span><span class="sxs-lookup"><span data-stu-id="5f4c9-141">The next crawl runs only when it's manually resumed.</span></span> <span data-ttu-id="5f4c9-142">不過，來自此連線的資料仍可供搜尋。</span><span class="sxs-lookup"><span data-stu-id="5f4c9-142">However, the data from this connection continues to be searchable.</span></span>

* <span data-ttu-id="5f4c9-143">**失敗**。</span><span class="sxs-lookup"><span data-stu-id="5f4c9-143">**Failed**.</span></span> <span data-ttu-id="5f4c9-144">連接發生嚴重失敗。</span><span class="sxs-lookup"><span data-stu-id="5f4c9-144">The connection had a critical failure.</span></span> <span data-ttu-id="5f4c9-145">此錯誤需要手動干預。</span><span class="sxs-lookup"><span data-stu-id="5f4c9-145">This error requires manual intervention.</span></span> <span data-ttu-id="5f4c9-146">管理員需要根據所顯示的錯誤訊息採取適當的動作。</span><span class="sxs-lookup"><span data-stu-id="5f4c9-146">The admin needs to take appropriate action based on the error message shown.</span></span> <span data-ttu-id="5f4c9-147">在發生錯誤之前，已編制索引的資料可供搜尋。</span><span class="sxs-lookup"><span data-stu-id="5f4c9-147">Data that was indexed until the error occurred is searchable.</span></span>

## <a name="monitor-your-index-quota-utilization"></a><span data-ttu-id="5f4c9-148">監視索引配額利用率</span><span class="sxs-lookup"><span data-stu-id="5f4c9-148">Monitor your index quota utilization</span></span>

<span data-ttu-id="5f4c9-149">可用的索引配額和使用量會顯示在 [連接器] 的 [登陸] 頁面上。</span><span class="sxs-lookup"><span data-stu-id="5f4c9-149">The available index quota and consumption is displayed on the connectors landing page.</span></span>

![索引配額使用量列](media/quota_utilization.png)

>[!NOTE]
><span data-ttu-id="5f4c9-151">在預覽期間內，每個嘗試繪製圖形連接器的組織，都已在所有連線中提供高達2000000專案的免費固定配額。</span><span class="sxs-lookup"><span data-stu-id="5f4c9-151">During the preview period, every organization trying out Graph connectors was provided a free fixed quota of up to 2 million items across all connections.</span></span> <span data-ttu-id="5f4c9-152">透過圖形連接器一般可用，當已在預覽中使用圖形連接器的組織，可用配額會在2021年4月1日到期。</span><span class="sxs-lookup"><span data-stu-id="5f4c9-152">With Graph connectors being generally available, the free quota will expire on April 1st, 2021 for those organizations who have been using Graph connectors in preview.</span></span>
><span data-ttu-id="5f4c9-153">以「 [預覽](connectors-preview.md) 」標示的 Microsoft 建立圖形連接器，將不會包含在您組織的總電量索引配額內。</span><span class="sxs-lookup"><span data-stu-id="5f4c9-153">Microsoft-built Graph connectors labeled as ["Preview"](connectors-preview.md) will not be included in the total charged index quota for your organization.</span></span> <span data-ttu-id="5f4c9-154">不過，它會計算您可以為您的組織設定的最大連線數目上限，以及您的組織可在連線上編制索引的最大7000000專案數目;每個連線都是限制700000個專案。</span><span class="sxs-lookup"><span data-stu-id="5f4c9-154">However, it will count towards the max number of 10 connections you can configure for your organization and the max number of 7 million items your organization can index across connections; each connection is limited 700,000 items.</span></span> 

<span data-ttu-id="5f4c9-155">[配額使用狀況] 列會根據您的組織的配額使用量，指出不同的狀態：</span><span class="sxs-lookup"><span data-stu-id="5f4c9-155">The quota utilization bar will indicate various states based on consumption of quota by your organization:</span></span>

<span data-ttu-id="5f4c9-156">狀態</span><span class="sxs-lookup"><span data-stu-id="5f4c9-156">State</span></span> | <span data-ttu-id="5f4c9-157">配額使用量</span><span class="sxs-lookup"><span data-stu-id="5f4c9-157">Quota consumption</span></span>
--- | ---
<span data-ttu-id="5f4c9-158">一般</span><span class="sxs-lookup"><span data-stu-id="5f4c9-158">Normal</span></span> | <span data-ttu-id="5f4c9-159">1-69%</span><span class="sxs-lookup"><span data-stu-id="5f4c9-159">1-69%</span></span>
<span data-ttu-id="5f4c9-160">高</span><span class="sxs-lookup"><span data-stu-id="5f4c9-160">High</span></span> | <span data-ttu-id="5f4c9-161">70-89%</span><span class="sxs-lookup"><span data-stu-id="5f4c9-161">70-89%</span></span>
<span data-ttu-id="5f4c9-162">重要</span><span class="sxs-lookup"><span data-stu-id="5f4c9-162">Critical</span></span> | <span data-ttu-id="5f4c9-163">90%-99%</span><span class="sxs-lookup"><span data-stu-id="5f4c9-163">90%-99%</span></span>
<span data-ttu-id="5f4c9-164">Full</span><span class="sxs-lookup"><span data-stu-id="5f4c9-164">Full</span></span> | <span data-ttu-id="5f4c9-165">100%</span><span class="sxs-lookup"><span data-stu-id="5f4c9-165">100%</span></span>

<span data-ttu-id="5f4c9-166">已編制索引的專案數也會顯示每個連線。</span><span class="sxs-lookup"><span data-stu-id="5f4c9-166">The number of items indexed will also be displayed with each connection.</span></span> <span data-ttu-id="5f4c9-167">每個連線編制索引的專案數會占組織可用的總配額。</span><span class="sxs-lookup"><span data-stu-id="5f4c9-167">The number of items indexed by each connection contributes to the total quota available for your organization.</span></span>

<span data-ttu-id="5f4c9-168">當您的組織超過索引配額時，所有作用中的連線將會受到影響，而且這些連線將會以 **超出限制** 的狀態運作。</span><span class="sxs-lookup"><span data-stu-id="5f4c9-168">When index quota is exceeded for your organization, all active connections will be impacted, and those connections will operate in **limit exceeded** state.</span></span> <span data-ttu-id="5f4c9-169">在此狀態下，您的使用中連接</span><span class="sxs-lookup"><span data-stu-id="5f4c9-169">In this state, your active connections</span></span>  

* <span data-ttu-id="5f4c9-170">無法新增專案。</span><span class="sxs-lookup"><span data-stu-id="5f4c9-170">Will not be able to add new items.</span></span>

* <span data-ttu-id="5f4c9-171">將能夠更新或刪除現有專案。</span><span class="sxs-lookup"><span data-stu-id="5f4c9-171">Will be able to update or delete existing items.</span></span>

<span data-ttu-id="5f4c9-172">若要修正此問題，您可以執行下列其中一項操作：</span><span class="sxs-lookup"><span data-stu-id="5f4c9-172">To fix this, you can do any of the following:</span></span>

* <span data-ttu-id="5f4c9-173">瞭解如何在 [授權需求和價格](licensing.md)購買組織的索引配額。</span><span class="sxs-lookup"><span data-stu-id="5f4c9-173">Learn how to purchase index quota for your organization at [Licensing requirements and pricing](licensing.md).</span></span>

* <span data-ttu-id="5f4c9-174">找出 ingested 過多內容的連線，並更新這些連線以編制索引較少的專案，以騰出空間做為配額。</span><span class="sxs-lookup"><span data-stu-id="5f4c9-174">Identify connections which have too much content being ingested and update them to index fewer items to make room for quota.</span></span> <span data-ttu-id="5f4c9-175">若要更新連線，您必須使用新的攝取篩選來刪除及建立新的連線，而這會帶來較少的專案。</span><span class="sxs-lookup"><span data-stu-id="5f4c9-175">To update the connection, you must delete and create a new connection with a new ingestion filter which brings in fewer items.</span></span>

* <span data-ttu-id="5f4c9-176">永久刪除一或多個連線</span><span class="sxs-lookup"><span data-stu-id="5f4c9-176">Permanently delete one or more connections</span></span>
