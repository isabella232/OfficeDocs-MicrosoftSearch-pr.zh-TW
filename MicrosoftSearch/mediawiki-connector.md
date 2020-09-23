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
ms.openlocfilehash: d8aa4a99c353a80f7d3dcf768d8287200b17fdc6
ms.sourcegitcommit: be0c64845477127d73ee24dc727e4583ced3d0e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/22/2020
ms.locfileid: "48206948"
---
# <a name="mediawiki-connector"></a><span data-ttu-id="9ffce-103">MediaWiki 連接器</span><span class="sxs-lookup"><span data-stu-id="9ffce-103">MediaWiki connector</span></span>

<span data-ttu-id="9ffce-104">透過 MediaWiki 連接器，您的組織可以從使用 MediaWiki 軟體所建立的 wiki 探索和編制資料。</span><span class="sxs-lookup"><span data-stu-id="9ffce-104">With the MediaWiki connector, your organization can discover and index data from a wiki created by using MediaWiki software.</span></span> <span data-ttu-id="9ffce-105">此連接器會將指定的內容索引至 Microsoft 搜尋中，並支援定期編目，使索引保持在最新狀態。</span><span class="sxs-lookup"><span data-stu-id="9ffce-105">This connector indexes specified content into Microsoft Search and supports periodic crawls to keep the index up to date.</span></span>

<span data-ttu-id="9ffce-106">本文適用于 Microsoft 365 系統管理員或任何設定、執行及監視 MediaWiki 連接器的人員。</span><span class="sxs-lookup"><span data-stu-id="9ffce-106">This article is for Microsoft 365 administrators or anyone who configures, runs, and monitors a MediaWiki connector.</span></span> <span data-ttu-id="9ffce-107">它說明如何設定連接器和連接器功能、限制及疑難排解技術。</span><span class="sxs-lookup"><span data-stu-id="9ffce-107">It explains how to configure your connector and connector capabilities, limitations, and troubleshooting techniques.</span></span>

## <a name="connect-to-a-data-source"></a><span data-ttu-id="9ffce-108">連接到資料來源</span><span class="sxs-lookup"><span data-stu-id="9ffce-108">Connect to a data source</span></span>

<span data-ttu-id="9ffce-109">輸入您的 MediaWiki URL 和認證以驗證連線。</span><span class="sxs-lookup"><span data-stu-id="9ffce-109">Enter your MediaWiki URL and credentials for authenticating the connection.</span></span> <span data-ttu-id="9ffce-110">您將需要下列資訊： **租使用者識別碼**、 **資源識別碼**、 **用戶端識別碼**和 **用戶端密碼**。</span><span class="sxs-lookup"><span data-stu-id="9ffce-110">You'll need the following information: **Tenant ID**, **Resource ID**, **Client ID**, and the **Client Secret**.</span></span>

## <a name="manage-the-search-schema"></a><span data-ttu-id="9ffce-111">管理搜尋結構描述</span><span class="sxs-lookup"><span data-stu-id="9ffce-111">Manage the search schema</span></span>

<span data-ttu-id="9ffce-112">成功連接後，請設定搜尋架構對應。</span><span class="sxs-lookup"><span data-stu-id="9ffce-112">After successful connection, configure the search schema mapping.</span></span> <span data-ttu-id="9ffce-113">您可以選擇哪些屬性可供**查詢**、可搜尋及可**供\*\*\*\*檢索**。</span><span class="sxs-lookup"><span data-stu-id="9ffce-113">You can choose which properties to make **queryable**, **searchable**, and **retrievable**.</span></span>

## <a name="manage-search-permissions"></a><span data-ttu-id="9ffce-114">管理搜尋許可權</span><span class="sxs-lookup"><span data-stu-id="9ffce-114">Manage search permissions</span></span>

<span data-ttu-id="9ffce-115">MediaWiki 連接器只支援 **所有人都**能看見的搜尋許可權。</span><span class="sxs-lookup"><span data-stu-id="9ffce-115">The MediaWiki connector only supports search permissions visible to **Everyone**.</span></span> <span data-ttu-id="9ffce-116">已編制索引的資料會顯示在搜尋結果中，並對組織中的所有使用者顯示。</span><span class="sxs-lookup"><span data-stu-id="9ffce-116">Indexed data appears in the search results and is visible to all users in the organization.</span></span>

## <a name="set-the-refresh-schedule"></a><span data-ttu-id="9ffce-117">設定重新整理排程</span><span class="sxs-lookup"><span data-stu-id="9ffce-117">Set the refresh schedule</span></span>

<span data-ttu-id="9ffce-118">此排程會重新整理已編制索引的資料，因此 wiki 的變更會反映在 Microsoft 搜尋中。</span><span class="sxs-lookup"><span data-stu-id="9ffce-118">This schedule refreshes indexed data, so changes to the wiki are reflected in Microsoft Search.</span></span> <span data-ttu-id="9ffce-119">所有新頁面、刪除的頁面、頁面內容或中繼資料變更都會出現在搜尋結果中指定的重新整理間隔之後。</span><span class="sxs-lookup"><span data-stu-id="9ffce-119">All new pages, deleted pages, page content, or metadata changes appear in search results after the specified refresh interval.</span></span> <span data-ttu-id="9ffce-120">編目時間取決於 wiki 的大小。</span><span class="sxs-lookup"><span data-stu-id="9ffce-120">The crawl time is dependent on the size of the wiki.</span></span> <span data-ttu-id="9ffce-121">目前的連接器會在每分鐘50頁面的周圍進行編目。</span><span class="sxs-lookup"><span data-stu-id="9ffce-121">Currently the connector crawls at around 50 pages per minute.</span></span>

## <a name="limitations"></a><span data-ttu-id="9ffce-122">限制</span><span class="sxs-lookup"><span data-stu-id="9ffce-122">Limitations</span></span>

<span data-ttu-id="9ffce-123">MediaWiki 連接器在預覽版本中有下列限制：</span><span class="sxs-lookup"><span data-stu-id="9ffce-123">The MediaWiki connector has these limitations in the preview release:</span></span>

* <span data-ttu-id="9ffce-124">僅支援雲端型 wiki。</span><span class="sxs-lookup"><span data-stu-id="9ffce-124">Supports only cloud-based wikis.</span></span>
* <span data-ttu-id="9ffce-125">使用 Azure Active Directory 或 Azure 驗證，僅支援 Basic 或 OAuth 2.0。</span><span class="sxs-lookup"><span data-stu-id="9ffce-125">Supports only Basic or OAuth 2.0 with Azure Active Directory or Azure authentication.</span></span>
* <span data-ttu-id="9ffce-126">不支援索引的命名空間選取。</span><span class="sxs-lookup"><span data-stu-id="9ffce-126">Doesn't support namespace selection for indexing.</span></span> <span data-ttu-id="9ffce-127">僅索引 **主要**、 **類別**和檔案 **命名空間** 。</span><span class="sxs-lookup"><span data-stu-id="9ffce-127">Indexes only **Main**, **Category**, and **File** namespaces.</span></span>
* <span data-ttu-id="9ffce-128">不支援 (ACLs) 的存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="9ffce-128">Doesn't support Access Control Lists (ACLs).</span></span> <span data-ttu-id="9ffce-129">因此，組織中的所有使用者都能看到索引頁面。</span><span class="sxs-lookup"><span data-stu-id="9ffce-129">Thus, indexed pages are visible to all users in the organization.</span></span>
