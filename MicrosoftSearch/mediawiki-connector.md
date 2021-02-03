---
title: Microsoft Search 的 MediaWiki Graph connector
ms.author: mecampos
author: mecampos
manager: umas
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 設定 Microsoft 搜尋的 MediaWiki 圖形連接器
ms.openlocfilehash: 9d9d7a1ef9aeaba079f8cccef1ec4a4836768e8d
ms.sourcegitcommit: d39113376db26333872d3a2c7baddc3a3a7aea61
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/03/2021
ms.locfileid: "50084981"
---
<!---Previous ms.author: monaray --->

# <a name="mediawiki-graph-connector"></a><span data-ttu-id="fdab6-103">MediaWiki Graph 連接器</span><span class="sxs-lookup"><span data-stu-id="fdab6-103">MediaWiki Graph connector</span></span>

<span data-ttu-id="fdab6-104">MediaWiki Graph 連接器可讓您的組織從使用 MediaWiki 軟體所建立的 wiki 探索和編制資料。</span><span class="sxs-lookup"><span data-stu-id="fdab6-104">The MediaWiki Graph connector allows your organization to discover and index data from a wiki created by using MediaWiki software.</span></span> <span data-ttu-id="fdab6-105">此連接器會將指定的內容索引至 Microsoft 搜尋中，並支援定期編目，使索引保持在最新狀態。</span><span class="sxs-lookup"><span data-stu-id="fdab6-105">This connector indexes specified content into Microsoft Search and supports periodic crawls to keep the index up to date.</span></span>

> [!NOTE]
> <span data-ttu-id="fdab6-106">請閱讀 [**您的圖形連接器文章設定**](configure-connector.md) ，以瞭解一般圖表連接器設定程式。</span><span class="sxs-lookup"><span data-stu-id="fdab6-106">Read the [**Setup for your Graph connector**](configure-connector.md) article to understand the general Graph connectors setup process.</span></span>

<span data-ttu-id="fdab6-107">本文適用于任何設定、執行及監視 ServiceNow 圖形連接器的人員。</span><span class="sxs-lookup"><span data-stu-id="fdab6-107">This article is for anyone who configures, runs, and monitors a ServiceNow Graph connector.</span></span> <span data-ttu-id="fdab6-108">它會補充一般設定程式，並顯示只適用于 MediaWiki Graph 連接器的指示。</span><span class="sxs-lookup"><span data-stu-id="fdab6-108">It supplements the general setup process, and shows instructions that apply only for the MediaWiki Graph connector.</span></span> <span data-ttu-id="fdab6-109">本文也包含 [限制](#limitations)的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="fdab6-109">This article also includes information about [Limitations](#limitations).</span></span>

<!---## Before you get started-->

<!---Insert "Before you get started" recommendations for this data source-->

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a><span data-ttu-id="fdab6-110">步驟1：在 Microsoft 365 系統管理中心新增圖表連接器</span><span class="sxs-lookup"><span data-stu-id="fdab6-110">Step 1: Add a Graph connector in the Microsoft 365 admin center</span></span>

<span data-ttu-id="fdab6-111">遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。</span><span class="sxs-lookup"><span data-stu-id="fdab6-111">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-2-name-the-connection"></a><span data-ttu-id="fdab6-112">步驟2：命名連線</span><span class="sxs-lookup"><span data-stu-id="fdab6-112">Step 2: Name the connection</span></span>

<span data-ttu-id="fdab6-113">遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。</span><span class="sxs-lookup"><span data-stu-id="fdab6-113">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-3-configure-the-connection-settings"></a><span data-ttu-id="fdab6-114">步驟3：設定連接設定</span><span class="sxs-lookup"><span data-stu-id="fdab6-114">Step 3: Configure the connection settings</span></span>

<span data-ttu-id="fdab6-115">輸入您的 **WIKI URL** ，然後從下拉式功能表的 [選項] 功能表中選擇 **驗證類型** 。</span><span class="sxs-lookup"><span data-stu-id="fdab6-115">Enter your **Wiki URL** and choose the **Authentication type** from the drop-down menu of options.</span></span> <span data-ttu-id="fdab6-116">選項為 **None**、 **Basic** 及 **OAuth 2.0 AAD**。</span><span class="sxs-lookup"><span data-stu-id="fdab6-116">The options are **None**, **Basic**, and **OAuth 2.0 AAD**.</span></span>

<span data-ttu-id="fdab6-117">如果您選擇 [ **基本** ] 做為驗證類型，您將需要提供 wiki 的使用者 **名稱** 和 **密碼** 。</span><span class="sxs-lookup"><span data-stu-id="fdab6-117">If you choose **Basic** as the Authentication type, you will need to provide the **Username** and **Password** for the wiki.</span></span>

<span data-ttu-id="fdab6-118">如果您選擇 **OAuth 2.0 AAD** 作為驗證類型，您將需要提供 wiki 安裝的 **資源識別碼** 。</span><span class="sxs-lookup"><span data-stu-id="fdab6-118">If you choose **OAuth 2.0 AAD** as the Authentication type, you will need to provide the **Resource ID** of the wiki installation.</span></span> <span data-ttu-id="fdab6-119">您也需要提供在 AAD 應用程式註冊頁面上產生的 **用戶端識別碼** 和 **用戶端密碼** 。</span><span class="sxs-lookup"><span data-stu-id="fdab6-119">You will also need to provide the **Client ID** and **Client secret** generated on the AAD Application registration page.</span></span>

## <a name="step-4-manage-search-permissions"></a><span data-ttu-id="fdab6-120">步驟4：管理搜尋許可權</span><span class="sxs-lookup"><span data-stu-id="fdab6-120">Step 4: Manage search permissions</span></span>

<span data-ttu-id="fdab6-121">MediaWiki 連接器只支援 **所有人都** 能看見的搜尋許可權。</span><span class="sxs-lookup"><span data-stu-id="fdab6-121">The MediaWiki connector only supports search permissions visible to **Everyone**.</span></span> <span data-ttu-id="fdab6-122">已編制索引的資料會顯示在搜尋結果中，並對組織中的所有使用者顯示。</span><span class="sxs-lookup"><span data-stu-id="fdab6-122">Indexed data appears in the search results and is visible to all users in the organization.</span></span>

## <a name="step-5-assign-property-labels"></a><span data-ttu-id="fdab6-123">步驟5：指派屬性標籤</span><span class="sxs-lookup"><span data-stu-id="fdab6-123">Step 5: Assign property labels</span></span>

<span data-ttu-id="fdab6-124">遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。</span><span class="sxs-lookup"><span data-stu-id="fdab6-124">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-6-manage-schema"></a><span data-ttu-id="fdab6-125">步驟6：管理架構</span><span class="sxs-lookup"><span data-stu-id="fdab6-125">Step 6: Manage schema</span></span>

<span data-ttu-id="fdab6-126">遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。</span><span class="sxs-lookup"><span data-stu-id="fdab6-126">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-7-choose-refresh-settings"></a><span data-ttu-id="fdab6-127">步驟7：選擇重新整理設定</span><span class="sxs-lookup"><span data-stu-id="fdab6-127">Step 7: Choose refresh settings</span></span>

<span data-ttu-id="fdab6-128">遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。</span><span class="sxs-lookup"><span data-stu-id="fdab6-128">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-8-review-connection"></a><span data-ttu-id="fdab6-129">步驟8：檢查連線</span><span class="sxs-lookup"><span data-stu-id="fdab6-129">Step 8: Review connection</span></span>

<span data-ttu-id="fdab6-130">遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。</span><span class="sxs-lookup"><span data-stu-id="fdab6-130">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

<!---## Troubleshooting-->
<!---To be added-->

## <a name="limitations"></a><span data-ttu-id="fdab6-131">限制</span><span class="sxs-lookup"><span data-stu-id="fdab6-131">Limitations</span></span>

<span data-ttu-id="fdab6-132">MediaWiki 連接器在預覽版本中有下列限制：</span><span class="sxs-lookup"><span data-stu-id="fdab6-132">The MediaWiki connector has these limitations in the preview release:</span></span>

* <span data-ttu-id="fdab6-133">僅支援雲端型 wiki。</span><span class="sxs-lookup"><span data-stu-id="fdab6-133">Supports only cloud-based wikis.</span></span>
* <span data-ttu-id="fdab6-134">使用 Azure Active Directory 或 Azure 驗證，僅支援 Basic 或 OAuth 2.0。</span><span class="sxs-lookup"><span data-stu-id="fdab6-134">Supports only Basic or OAuth 2.0 with Azure Active Directory or Azure authentication.</span></span>
* <span data-ttu-id="fdab6-135">不支援索引的命名空間選取。</span><span class="sxs-lookup"><span data-stu-id="fdab6-135">Doesn't support namespace selection for indexing.</span></span> <span data-ttu-id="fdab6-136">僅索引主要、類別和檔案命名空間。</span><span class="sxs-lookup"><span data-stu-id="fdab6-136">Indexes only Main, Category, and File namespaces.</span></span>
* <span data-ttu-id="fdab6-137">不支援 (ACLs) 的存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="fdab6-137">Doesn't support Access Control Lists (ACLs).</span></span> <span data-ttu-id="fdab6-138">因此，組織中的所有使用者都能看到索引頁面。</span><span class="sxs-lookup"><span data-stu-id="fdab6-138">Thus, indexed pages are visible to all users in the organization.</span></span>
