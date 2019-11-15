---
title: Microsoft Search MediaWiki 連接器
ms.author: v-pamcn
author: monaray
manager: mnirkhe
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 設定 Microsoft Search MediaWiki 連接器
ms.openlocfilehash: 2aa0ef494aa42b1a7364ec68f6532dec737b9c25
ms.sourcegitcommit: 21361af7c244ffd6ff8689fd0ff0daa359bf4129
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/14/2019
ms.locfileid: "38626961"
---
# <a name="mediawiki-connector"></a><span data-ttu-id="ce6e1-103">MediaWiki 連接器</span><span class="sxs-lookup"><span data-stu-id="ce6e1-103">MediaWiki connector</span></span>

<span data-ttu-id="ce6e1-104">MediaWiki 連接器後，您的組織可以探索與索引資料從 wiki 建立使用 MediaWiki 軟體。</span><span class="sxs-lookup"><span data-stu-id="ce6e1-104">With the MediaWiki connector, your organization can discover and index data from a wiki created by using MediaWiki software.</span></span> <span data-ttu-id="ce6e1-105">此連接器索引指定成 Microsoft Search 和支援定期編目保持最新狀態索引內容。</span><span class="sxs-lookup"><span data-stu-id="ce6e1-105">This connector indexes specified content into Microsoft Search and supports periodic crawls to keep the index up to date.</span></span>

<span data-ttu-id="ce6e1-106">本文適用於 Microsoft 365 系統管理員或人設定、 執行，並監視 MediaWiki 連接器。</span><span class="sxs-lookup"><span data-stu-id="ce6e1-106">This article is for Microsoft 365 administrators or anyone who configures, runs, and monitors a MediaWiki connector.</span></span> <span data-ttu-id="ce6e1-107">本文說明如何設定連接器，連接器功能、 限制和疑難排解技巧。</span><span class="sxs-lookup"><span data-stu-id="ce6e1-107">It explains how to configure your connector and connector capabilities, limitations, and troubleshooting techniques.</span></span>

## <a name="connect-to-a-data-source"></a><span data-ttu-id="ce6e1-108">連線至資料來源</span><span class="sxs-lookup"><span data-stu-id="ce6e1-108">Connect to a data source</span></span>
<span data-ttu-id="ce6e1-109">輸入您 MediaWiki URL 與認證來驗證連線。</span><span class="sxs-lookup"><span data-stu-id="ce6e1-109">Enter your MediaWiki URL and credentials for authenticating the connection.</span></span> <span data-ttu-id="ce6e1-110">您將需要下列資訊：**租用戶識別碼**、**資源識別碼**、**用戶端識別碼**和**用戶端密碼**。</span><span class="sxs-lookup"><span data-stu-id="ce6e1-110">You'll need the following information: **Tenant ID**, **Resource ID**, **Client ID**, and the **Client Secret**.</span></span>

## <a name="manage-the-search-schema"></a><span data-ttu-id="ce6e1-111">管理搜尋結構描述</span><span class="sxs-lookup"><span data-stu-id="ce6e1-111">Manage the search schema</span></span>
<span data-ttu-id="ce6e1-112">成功連線之後，設定的搜尋結構描述對應。</span><span class="sxs-lookup"><span data-stu-id="ce6e1-112">After successful connection, configure the search schema mapping.</span></span> <span data-ttu-id="ce6e1-113">您可以選擇要讓屬性**設為可查詢**、**可搜尋**，並**可擷取**。</span><span class="sxs-lookup"><span data-stu-id="ce6e1-113">You can choose which properties to make **queryable**, **searchable**, and **retrievable**.</span></span>

## <a name="manage-search-permissions"></a><span data-ttu-id="ce6e1-114">管理搜尋的權限</span><span class="sxs-lookup"><span data-stu-id="ce6e1-114">Manage search permissions</span></span>
<span data-ttu-id="ce6e1-115">MediaWiki 連接器僅支援搜尋權限以**供其他人**。</span><span class="sxs-lookup"><span data-stu-id="ce6e1-115">The MediaWiki connector only supports search permissions visible to **Everyone**.</span></span> <span data-ttu-id="ce6e1-116">已編製索引的資料會出現在搜尋結果，並在組織中的所有使用者都都能看到。</span><span class="sxs-lookup"><span data-stu-id="ce6e1-116">Indexed data appears in the search results and is visible to all users in the organization.</span></span>

## <a name="set-the-refresh-schedule"></a><span data-ttu-id="ce6e1-117">設定重新整理排程</span><span class="sxs-lookup"><span data-stu-id="ce6e1-117">Set the refresh schedule</span></span> 
<span data-ttu-id="ce6e1-118">此排程重新整理已編製索引的資料，以便 wiki 的變更會反映在 Microsoft Search。</span><span class="sxs-lookup"><span data-stu-id="ce6e1-118">This schedule refreshes indexed data, so changes to the wiki are reflected in Microsoft Search.</span></span> <span data-ttu-id="ce6e1-119">所有新的頁面、 刪除的頁面、 頁面內容或中繼資料變更指定的重新整理間隔之後出現在搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="ce6e1-119">All new pages, deleted pages, page content, or metadata changes appear in search results after the specified refresh interval.</span></span> <span data-ttu-id="ce6e1-120">編目時間 」 是 wiki 的大小而定。</span><span class="sxs-lookup"><span data-stu-id="ce6e1-120">The crawl time is dependent on the size of the wiki.</span></span> <span data-ttu-id="ce6e1-121">目前連接器會在大約 50 頁面每分鐘編目。</span><span class="sxs-lookup"><span data-stu-id="ce6e1-121">Currently the connector crawls at around 50 pages per minute.</span></span>

## <a name="limitations"></a><span data-ttu-id="ce6e1-122">限制</span><span class="sxs-lookup"><span data-stu-id="ce6e1-122">Limitations</span></span> 
<span data-ttu-id="ce6e1-123">MediaWiki 連接器預覽版本中有這些限制：</span><span class="sxs-lookup"><span data-stu-id="ce6e1-123">The MediaWiki connector has these limitations in the preview release:</span></span>
* <span data-ttu-id="ce6e1-124">支援僅雲端式 wiki。</span><span class="sxs-lookup"><span data-stu-id="ce6e1-124">Supports only cloud-based wikis.</span></span>
* <span data-ttu-id="ce6e1-125">支援僅 [基本] 或 [使用 Azure Active Directory 或 Azure 驗證的 OAuth 2.0。</span><span class="sxs-lookup"><span data-stu-id="ce6e1-125">Supports only Basic or OAuth 2.0 with Azure Active Directory or Azure authentication.</span></span>
* <span data-ttu-id="ce6e1-126">不支援索引編製的命名空間的選取範圍。</span><span class="sxs-lookup"><span data-stu-id="ce6e1-126">Doesn't support namespace selection for indexing.</span></span> <span data-ttu-id="ce6e1-127">編製索引只有**主要**、**類別**及**檔案**的命名空間。</span><span class="sxs-lookup"><span data-stu-id="ce6e1-127">Indexes only **Main**, **Category**, and **File** namespaces.</span></span>
* <span data-ttu-id="ce6e1-128">不支援存取控制清單 (Acl)。</span><span class="sxs-lookup"><span data-stu-id="ce6e1-128">Doesn't support Access Control Lists (ACLs).</span></span> <span data-ttu-id="ce6e1-129">因此，已編製索引的頁面都可以看見組織中的所有使用者。</span><span class="sxs-lookup"><span data-stu-id="ce6e1-129">Thus, indexed pages are visible to all users in the organization.</span></span>
