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
ms.openlocfilehash: 7a22fcc84f6f435bf438aa027c42c76eb8be1eaf
ms.sourcegitcommit: 39bf9f0db7f9bff2ab82c99a059b0ddcf1c98f5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/19/2021
ms.locfileid: "49905948"
---
# <a name="mediawiki-connector"></a><span data-ttu-id="30fca-103">MediaWiki 連接器</span><span class="sxs-lookup"><span data-stu-id="30fca-103">MediaWiki connector</span></span>

<span data-ttu-id="30fca-104">透過 MediaWiki 連接器，您的組織可以從使用 MediaWiki 軟體所建立的 wiki 探索和編制資料。</span><span class="sxs-lookup"><span data-stu-id="30fca-104">With the MediaWiki connector, your organization can discover and index data from a wiki created by using MediaWiki software.</span></span> <span data-ttu-id="30fca-105">此連接器會將指定的內容索引至 Microsoft 搜尋中，並支援定期編目，使索引保持在最新狀態。</span><span class="sxs-lookup"><span data-stu-id="30fca-105">This connector indexes specified content into Microsoft Search and supports periodic crawls to keep the index up to date.</span></span>

<span data-ttu-id="30fca-106">本文適用于 Microsoft 365 系統管理員或任何設定、執行及監視 MediaWiki Graph 連接器的人員。</span><span class="sxs-lookup"><span data-stu-id="30fca-106">This article is for Microsoft 365 administrators or anyone who configures, runs, and monitors a MediaWiki Graph connector.</span></span> <span data-ttu-id="30fca-107">它會補充 [設定圖形連接器](configure-connector.md) 文章中所提供的一般指示。</span><span class="sxs-lookup"><span data-stu-id="30fca-107">It supplements the general instructions provided in the [Set up your Graph connector](configure-connector.md) article.</span></span> <span data-ttu-id="30fca-108">若尚未這麼做，請閱讀整個設定圖形連接器文章，以瞭解一般的設定程式。</span><span class="sxs-lookup"><span data-stu-id="30fca-108">If you have not already done so, read the entire Set up your Graph connector article to understand the general setup process.</span></span>

<span data-ttu-id="30fca-109">安裝程式中的每個步驟都會列在下表中，也就是指出應該遵循一般設定指示或僅適用于 MediaWiki Graph 連接器的其他指示。</span><span class="sxs-lookup"><span data-stu-id="30fca-109">Each step in the setup process is listed below along with either a note that indicates you should follow the general setup instructions OR other instructions that apply to only MediaWiki Graph connectors.</span></span> <span data-ttu-id="30fca-110">本文也包含 MediaWiki 圖形連接器 [限制](#limitations) 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="30fca-110">This article also includes information about [Limitations](#limitations) for MediaWiki Graph connectors.</span></span> 

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a><span data-ttu-id="30fca-111">步驟1：在 Microsoft 365 系統管理中心新增圖形連接器。</span><span class="sxs-lookup"><span data-stu-id="30fca-111">Step 1: Add a Graph connector in the Microsoft 365 admin center.</span></span>
<span data-ttu-id="30fca-112">遵循一般設定指示。</span><span class="sxs-lookup"><span data-stu-id="30fca-112">Follow the general setup instructions.</span></span>

## <a name="step-2-name-the-connection"></a><span data-ttu-id="30fca-113">步驟2：命名連線。</span><span class="sxs-lookup"><span data-stu-id="30fca-113">Step 2: Name the connection.</span></span>
<span data-ttu-id="30fca-114">遵循一般設定指示。</span><span class="sxs-lookup"><span data-stu-id="30fca-114">Follow the general setup instructions.</span></span>
 
## <a name="step-3-configure-the-connection-settings"></a><span data-ttu-id="30fca-115">步驟3：設定連接設定。</span><span class="sxs-lookup"><span data-stu-id="30fca-115">Step 3: Configure the connection settings.</span></span>
<span data-ttu-id="30fca-116">輸入您的 **WIKI URL** ，然後從下拉式功能表的 [選項] 功能表中選擇 **驗證類型** 。</span><span class="sxs-lookup"><span data-stu-id="30fca-116">Enter your **Wiki URL** and choose the **Authentication type** from the drop-down menu of options.</span></span> <span data-ttu-id="30fca-117">選項為 **None**、 **Basic** 及 **OAuth 2.0 AAD**。</span><span class="sxs-lookup"><span data-stu-id="30fca-117">The options are **None**, **Basic**, and **OAuth 2.0 AAD**.</span></span>

<span data-ttu-id="30fca-118">如果您選擇 [ **基本** ] 做為驗證類型，您將需要提供 wiki 的使用者 **名稱** 和 **密碼** 。</span><span class="sxs-lookup"><span data-stu-id="30fca-118">If you choose **Basic** as the Authentication type, you will need to provide the **Username** and **Password** for the wiki.</span></span>

<span data-ttu-id="30fca-119">如果您選擇 **OAuth 2.0 AAD** 作為驗證類型，您將需要提供 wiki 安裝的 **資源識別碼** 。</span><span class="sxs-lookup"><span data-stu-id="30fca-119">If you choose **OAuth 2.0 AAD** as the Authentication type, you will need to provide the **Resource ID** of the wiki installation.</span></span> <span data-ttu-id="30fca-120">您也需要提供在 AAD 應用程式註冊頁面上產生的 **用戶端識別碼** 和 **用戶端密碼** 。</span><span class="sxs-lookup"><span data-stu-id="30fca-120">You will also need to provide the **Client ID** and **Client secret** generated on the AAD Application registration page.</span></span> 

## <a name="step-4-manage-search-permissions"></a><span data-ttu-id="30fca-121">步驟4：管理搜尋許可權</span><span class="sxs-lookup"><span data-stu-id="30fca-121">Step 4: Manage search permissions</span></span>
<span data-ttu-id="30fca-122">MediaWiki 連接器只支援 **所有人都** 能看見的搜尋許可權。</span><span class="sxs-lookup"><span data-stu-id="30fca-122">The MediaWiki connector only supports search permissions visible to **Everyone**.</span></span> <span data-ttu-id="30fca-123">已編制索引的資料會顯示在搜尋結果中，並對組織中的所有使用者顯示。</span><span class="sxs-lookup"><span data-stu-id="30fca-123">Indexed data appears in the search results and is visible to all users in the organization.</span></span>

## <a name="step-5-assign-property-labels"></a><span data-ttu-id="30fca-124">步驟5：指派屬性標籤</span><span class="sxs-lookup"><span data-stu-id="30fca-124">Step 5: Assign property labels</span></span>
<span data-ttu-id="30fca-125">遵循一般設定指示。</span><span class="sxs-lookup"><span data-stu-id="30fca-125">Follow the general setup instructions.</span></span>

## <a name="step-6-manage-schema"></a><span data-ttu-id="30fca-126">步驟6：管理架構</span><span class="sxs-lookup"><span data-stu-id="30fca-126">Step 6: Manage schema</span></span>
<span data-ttu-id="30fca-127">遵循一般設定指示。</span><span class="sxs-lookup"><span data-stu-id="30fca-127">Follow the general setup instructions.</span></span>

## <a name="step-7-choose-refresh-settings"></a><span data-ttu-id="30fca-128">步驟7：選擇重新整理設定</span><span class="sxs-lookup"><span data-stu-id="30fca-128">Step 7: Choose refresh settings</span></span>
<span data-ttu-id="30fca-129">遵循一般設定指示。</span><span class="sxs-lookup"><span data-stu-id="30fca-129">Follow the general setup instructions.</span></span>

## <a name="step-8-review-connection"></a><span data-ttu-id="30fca-130">步驟8：檢查連線</span><span class="sxs-lookup"><span data-stu-id="30fca-130">Step 8: Review connection</span></span>
<span data-ttu-id="30fca-131">遵循一般設定指示。</span><span class="sxs-lookup"><span data-stu-id="30fca-131">Follow the general setup instructions.</span></span>

<!---## Troubleshooting-->
<!---To be added-->

## <a name="limitations"></a><span data-ttu-id="30fca-132">限制</span><span class="sxs-lookup"><span data-stu-id="30fca-132">Limitations</span></span>
<span data-ttu-id="30fca-133">MediaWiki 連接器在預覽版本中有下列限制：</span><span class="sxs-lookup"><span data-stu-id="30fca-133">The MediaWiki connector has these limitations in the preview release:</span></span>

* <span data-ttu-id="30fca-134">僅支援雲端型 wiki。</span><span class="sxs-lookup"><span data-stu-id="30fca-134">Supports only cloud-based wikis.</span></span>
* <span data-ttu-id="30fca-135">使用 Azure Active Directory 或 Azure 驗證，僅支援 Basic 或 OAuth 2.0。</span><span class="sxs-lookup"><span data-stu-id="30fca-135">Supports only Basic or OAuth 2.0 with Azure Active Directory or Azure authentication.</span></span>
* <span data-ttu-id="30fca-136">不支援索引的命名空間選取。</span><span class="sxs-lookup"><span data-stu-id="30fca-136">Doesn't support namespace selection for indexing.</span></span> <span data-ttu-id="30fca-137">僅索引主要、類別和檔案命名空間。</span><span class="sxs-lookup"><span data-stu-id="30fca-137">Indexes only Main, Category, and File namespaces.</span></span>
* <span data-ttu-id="30fca-138">不支援 (ACLs) 的存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="30fca-138">Doesn't support Access Control Lists (ACLs).</span></span> <span data-ttu-id="30fca-139">因此，組織中的所有使用者都能看到索引頁面。</span><span class="sxs-lookup"><span data-stu-id="30fca-139">Thus, indexed pages are visible to all users in the organization.</span></span>
