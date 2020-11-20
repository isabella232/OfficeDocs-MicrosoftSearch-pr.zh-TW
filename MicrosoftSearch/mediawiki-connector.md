---
title: Microsoft 搜尋的 MediaWiki 連接器
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
description: 設定 Microsoft 搜尋的 MediaWiki 連接器
ms.openlocfilehash: 7f6b34dcafc4b82ab3778ec1d7a4921383e44a44
ms.sourcegitcommit: 59cdd3f0f82b7918399bf44d27d9891076090f4f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2020
ms.locfileid: "49367638"
---
# <a name="mediawiki-connector"></a><span data-ttu-id="b9c3d-103">MediaWiki 連接器</span><span class="sxs-lookup"><span data-stu-id="b9c3d-103">MediaWiki connector</span></span>

<span data-ttu-id="b9c3d-104">透過 MediaWiki 連接器，您的組織可以從使用 MediaWiki 軟體所建立的 wiki 探索和編制資料。</span><span class="sxs-lookup"><span data-stu-id="b9c3d-104">With the MediaWiki connector, your organization can discover and index data from a wiki created by using MediaWiki software.</span></span> <span data-ttu-id="b9c3d-105">此連接器會將指定的內容索引至 Microsoft 搜尋中，並支援定期編目，使索引保持在最新狀態。</span><span class="sxs-lookup"><span data-stu-id="b9c3d-105">This connector indexes specified content into Microsoft Search and supports periodic crawls to keep the index up to date.</span></span>

<span data-ttu-id="b9c3d-106">本文適用于 Microsoft 365 系統管理員或任何設定、執行及監視 MediaWiki 連接器的人員。</span><span class="sxs-lookup"><span data-stu-id="b9c3d-106">This article is for Microsoft 365 administrators or anyone who configures, runs, and monitors a MediaWiki connector.</span></span> <span data-ttu-id="b9c3d-107">它說明如何設定連接器和連接器功能、限制及疑難排解技術。</span><span class="sxs-lookup"><span data-stu-id="b9c3d-107">It explains how to configure your connector and connector capabilities, limitations, and troubleshooting techniques.</span></span>

## <a name="connect-to-a-data-source"></a><span data-ttu-id="b9c3d-108">連接到資料來源</span><span class="sxs-lookup"><span data-stu-id="b9c3d-108">Connect to a data source</span></span>

<span data-ttu-id="b9c3d-109">輸入您的 MediaWiki URL 和認證以驗證連線。</span><span class="sxs-lookup"><span data-stu-id="b9c3d-109">Enter your MediaWiki URL and credentials for authenticating the connection.</span></span> <span data-ttu-id="b9c3d-110">您將需要下列資訊： **租使用者識別碼**、 **資源識別碼**、 **用戶端識別碼** 和 **用戶端密碼**。</span><span class="sxs-lookup"><span data-stu-id="b9c3d-110">You'll need the following information: **Tenant ID**, **Resource ID**, **Client ID**, and the **Client Secret**.</span></span>

## <a name="manage-search-permissions"></a><span data-ttu-id="b9c3d-111">管理搜尋許可權</span><span class="sxs-lookup"><span data-stu-id="b9c3d-111">Manage search permissions</span></span>

<span data-ttu-id="b9c3d-112">MediaWiki 連接器只支援 **所有人都** 能看見的搜尋許可權。</span><span class="sxs-lookup"><span data-stu-id="b9c3d-112">The MediaWiki connector only supports search permissions visible to **Everyone**.</span></span> <span data-ttu-id="b9c3d-113">已編制索引的資料會顯示在搜尋結果中，並對組織中的所有使用者顯示。</span><span class="sxs-lookup"><span data-stu-id="b9c3d-113">Indexed data appears in the search results and is visible to all users in the organization.</span></span>

## <a name="assign-property-labels"></a><span data-ttu-id="b9c3d-114">指派屬性標籤</span><span class="sxs-lookup"><span data-stu-id="b9c3d-114">Assign property labels</span></span>

<span data-ttu-id="b9c3d-115">您可以從選項的功能表中選擇，將 source 屬性指派給每個標籤。</span><span class="sxs-lookup"><span data-stu-id="b9c3d-115">You can assign a source property to each label by choosing from a menu of options.</span></span> <span data-ttu-id="b9c3d-116">雖然這個步驟不是必要的，但具有一些屬性標籤會提升搜尋相關性，並可確保使用者更準確的搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="b9c3d-116">While this step is not mandatory, having some property labels will improve the search relevance and ensure more accurate search results for end users.</span></span>

## <a name="manage-schema"></a><span data-ttu-id="b9c3d-117">管理架構</span><span class="sxs-lookup"><span data-stu-id="b9c3d-117">Manage schema</span></span>

<span data-ttu-id="b9c3d-118">在 [**管理架構**] 畫面上，您可以選擇變更架構屬性 (可 **查詢**、**可搜尋、可\*\*\*\*檢索** 及 **可精簡搜尋**) 相關聯的屬性、新增選用的別名，然後選擇 **Content** 屬性。</span><span class="sxs-lookup"><span data-stu-id="b9c3d-118">On the **Manage Schema** screen, you have the option to change the schema attributes (**queryable**, **searchable**, **retrievable**, and **refinable**) associated with the properties, add optional aliases, and choose the **Content** property.</span></span>

## <a name="set-the-refresh-schedule"></a><span data-ttu-id="b9c3d-119">設定重新整理排程</span><span class="sxs-lookup"><span data-stu-id="b9c3d-119">Set the refresh schedule</span></span>

<span data-ttu-id="b9c3d-120">此排程會重新整理已編制索引的資料，因此 wiki 的變更會反映在 Microsoft 搜尋中。</span><span class="sxs-lookup"><span data-stu-id="b9c3d-120">This schedule refreshes indexed data, so changes to the wiki are reflected in Microsoft Search.</span></span> <span data-ttu-id="b9c3d-121">所有新頁面、刪除的頁面、頁面內容或中繼資料變更都會出現在搜尋結果中指定的重新整理間隔之後。</span><span class="sxs-lookup"><span data-stu-id="b9c3d-121">All new pages, deleted pages, page content, or metadata changes appear in search results after the specified refresh interval.</span></span> <span data-ttu-id="b9c3d-122">編目時間取決於 wiki 的大小。</span><span class="sxs-lookup"><span data-stu-id="b9c3d-122">The crawl time is dependent on the size of the wiki.</span></span> <span data-ttu-id="b9c3d-123">目前的連接器會在每分鐘50頁面的周圍進行編目。</span><span class="sxs-lookup"><span data-stu-id="b9c3d-123">Currently the connector crawls at around 50 pages per minute.</span></span>

## <a name="limitations"></a><span data-ttu-id="b9c3d-124">限制</span><span class="sxs-lookup"><span data-stu-id="b9c3d-124">Limitations</span></span>

<span data-ttu-id="b9c3d-125">MediaWiki 連接器在預覽版本中有下列限制：</span><span class="sxs-lookup"><span data-stu-id="b9c3d-125">The MediaWiki connector has these limitations in the preview release:</span></span>

* <span data-ttu-id="b9c3d-126">僅支援雲端型 wiki。</span><span class="sxs-lookup"><span data-stu-id="b9c3d-126">Supports only cloud-based wikis.</span></span>
* <span data-ttu-id="b9c3d-127">使用 Azure Active Directory 或 Azure 驗證，僅支援 Basic 或 OAuth 2.0。</span><span class="sxs-lookup"><span data-stu-id="b9c3d-127">Supports only Basic or OAuth 2.0 with Azure Active Directory or Azure authentication.</span></span>
* <span data-ttu-id="b9c3d-128">不支援索引的命名空間選取。</span><span class="sxs-lookup"><span data-stu-id="b9c3d-128">Doesn't support namespace selection for indexing.</span></span> <span data-ttu-id="b9c3d-129">僅索引 **主要**、 **類別** 和檔案 **命名空間** 。</span><span class="sxs-lookup"><span data-stu-id="b9c3d-129">Indexes only **Main**, **Category**, and **File** namespaces.</span></span>
* <span data-ttu-id="b9c3d-130">不支援 (ACLs) 的存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="b9c3d-130">Doesn't support Access Control Lists (ACLs).</span></span> <span data-ttu-id="b9c3d-131">因此，組織中的所有使用者都能看到索引頁面。</span><span class="sxs-lookup"><span data-stu-id="b9c3d-131">Thus, indexed pages are visible to all users in the organization.</span></span>
