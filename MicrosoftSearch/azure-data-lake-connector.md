---
title: Microsoft 搜尋的 Azure Data Lake connector
ms.author: monaray
author: monaray97
manager: shohara
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 設定 Azure Data Lake Storage Gen2 connector for Microsoft Search
ms.openlocfilehash: 860c923c62495c7df20152fb530797e390949305
ms.sourcegitcommit: 59cdd3f0f82b7918399bf44d27d9891076090f4f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2020
ms.locfileid: "49367584"
---
# <a name="azure-data-lake-storage-gen2-connector"></a><span data-ttu-id="c06b8-103">Azure Data Lake Storage Gen2 connector</span><span class="sxs-lookup"><span data-stu-id="c06b8-103">Azure Data Lake Storage Gen2 connector</span></span>

<span data-ttu-id="c06b8-104">透過 Azure Data Lake Storage Gen2 connector，您組織中的使用者可以搜尋 [Azure Blob 儲存區](https://docs.microsoft.com/azure/storage/blobs/storage-blobs-introduction) 和 [Azure Data Lake Gen 2 儲存體](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) 帳戶中儲存的檔案。</span><span class="sxs-lookup"><span data-stu-id="c06b8-104">With the Azure Data Lake Storage Gen2 connector, users in your organization can search for files stored in [Azure Blob Storage](https://docs.microsoft.com/azure/storage/blobs/storage-blobs-introduction) and [Azure Data Lake Gen 2 Storage](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) accounts.</span></span>

<span data-ttu-id="c06b8-105">本文適用于 [Microsoft 365](https://www.microsoft.com/microsoft-365) 系統管理員或任何設定、執行及監視 Azure Data Lake Storage Gen2 connector 的人員。</span><span class="sxs-lookup"><span data-stu-id="c06b8-105">This article is for [Microsoft 365](https://www.microsoft.com/microsoft-365) administrators or anyone who configures, runs, and monitors an Azure Data Lake Storage Gen2 connector.</span></span> <span data-ttu-id="c06b8-106">它會提供連接器設定、功能、限制及疑難排解技巧的概述。</span><span class="sxs-lookup"><span data-stu-id="c06b8-106">It gives an overview of the connector configuration, capabilities, limitations, and troubleshooting techniques.</span></span> <span data-ttu-id="c06b8-107">在本文中，我們使用 *Azure Storage* 做為 [Azure Blob 儲存區](https://docs.microsoft.com/azure/storage/blobs/storage-blobs-introduction) 和 [Azure Data Lake Gen 2 儲存區](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction)的一般字詞。</span><span class="sxs-lookup"><span data-stu-id="c06b8-107">In the article, we use *Azure Storage* as a generic term for [Azure Blob Storage](https://docs.microsoft.com/azure/storage/blobs/storage-blobs-introduction) and [Azure Data Lake Gen 2 Storage](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction).</span></span>

## <a name="connect-to-a-data-source"></a><span data-ttu-id="c06b8-108">連接到資料來源</span><span class="sxs-lookup"><span data-stu-id="c06b8-108">Connect to a data source</span></span>

### <a name="primary-storage-connection-string"></a><span data-ttu-id="c06b8-109">主要儲存連接字串</span><span class="sxs-lookup"><span data-stu-id="c06b8-109">Primary storage connection string</span></span>

<span data-ttu-id="c06b8-110">在 [ **驗證] 和 [config** ] 畫面上，提供主要儲存連接字串。</span><span class="sxs-lookup"><span data-stu-id="c06b8-110">On the **Authentication and config** screen, provide the Primary Storage Connection String.</span></span> <span data-ttu-id="c06b8-111">該字串是允許存取您的儲存體帳戶所需的字串。</span><span class="sxs-lookup"><span data-stu-id="c06b8-111">That string is required to allow access to your storage account.</span></span> <span data-ttu-id="c06b8-112">若要尋找您的連線字串，請移至 [Azure 入口網站](https://ms.portal.azure.com/#home) ，並流覽至相關 Azure 儲存體帳戶的 [機 **碼** ] 區段。</span><span class="sxs-lookup"><span data-stu-id="c06b8-112">To find your connection string, go to the [Azure portal](https://ms.portal.azure.com/#home) and navigate to the **Keys** section of your relevant Azure Storage account.</span></span> <span data-ttu-id="c06b8-113">在螢幕上適當的欄位中複製並貼上連接字串。</span><span class="sxs-lookup"><span data-stu-id="c06b8-113">Copy and paste the connection string in the appropriate field on the screen.</span></span>

<span data-ttu-id="c06b8-114">如果您不想在主要儲存連接字串) 中提供 **AccountKey** (參數，您必須授與下列角色的圖形連接器服務存取權。</span><span class="sxs-lookup"><span data-stu-id="c06b8-114">If you do not prefer to provide the **AccountKey** (a parameter in the primary storage connection string), you will need to grant access to our Graph Connectors Service for the following roles.</span></span>

* <span data-ttu-id="c06b8-115">儲存體 Blob 資料讀取器</span><span class="sxs-lookup"><span data-stu-id="c06b8-115">Storage Blob Data Reader</span></span>
* <span data-ttu-id="c06b8-116">儲存佇列資料參與者</span><span class="sxs-lookup"><span data-stu-id="c06b8-116">Storage Queue Data Contributor</span></span>
* <span data-ttu-id="c06b8-117">僅適用于分層儲存體) 的儲存體 Blob Delegator (</span><span class="sxs-lookup"><span data-stu-id="c06b8-117">Storage Blob Delegator (only for hierarchical storage)</span></span>

<span data-ttu-id="c06b8-118">流覽至您的 Azure 儲存體帳戶的 [ **存取控制** ] 索引標籤，然後依照這裡的指示，將存取權授與下列應用程式：</span><span class="sxs-lookup"><span data-stu-id="c06b8-118">Navigate to the **Access Control** tab of your Azure Storage account, and follow the instructions there to grant access to the following app:</span></span>

* <span data-ttu-id="c06b8-119">**第一方應用程式 ID:** 56c1da01-2129-48f7-9355-af6d59d42766</span><span class="sxs-lookup"><span data-stu-id="c06b8-119">**First Party App ID:** 56c1da01-2129-48f7-9355-af6d59d42766</span></span>
* <span data-ttu-id="c06b8-120">**第一方應用程式名稱：** 圖形連接器服務</span><span class="sxs-lookup"><span data-stu-id="c06b8-120">**First Party App Name:** Graph Connector Service</span></span>

### <a name="storage-account-and-queue-notifications-optional"></a><span data-ttu-id="c06b8-121">儲存帳戶和佇列通知 (選用) </span><span class="sxs-lookup"><span data-stu-id="c06b8-121">Storage account and queue notifications (Optional)</span></span>

<span data-ttu-id="c06b8-122">可在未來新增圖表連接器服務中即時處理變更的支援。</span><span class="sxs-lookup"><span data-stu-id="c06b8-122">Support to process changes in real time in the Graph Connectors Service might be added in the future.</span></span> <span data-ttu-id="c06b8-123">在此情況下，我們會監視儲存在佇列中的 Azure 儲存體變更通知。</span><span class="sxs-lookup"><span data-stu-id="c06b8-123">In that case, we'll monitor Azure Storage change notifications stored in a queue.</span></span> <span data-ttu-id="c06b8-124">您必須使用與您的 Azure 儲存體帳戶相同的帳戶建立佇列。</span><span class="sxs-lookup"><span data-stu-id="c06b8-124">You'll need to create a queue in the same account as your Azure Storage account.</span></span>

<span data-ttu-id="c06b8-125">建立佇列之後，請移至佇列頁面上的 [ **事件** ] 索引標籤，以設定 **事件訂閱**。</span><span class="sxs-lookup"><span data-stu-id="c06b8-125">After you create a queue, go to the **Events** tab on the queue page to configure **Event Subscription**.</span></span> <span data-ttu-id="c06b8-126">選擇佇列將要接收的所有 Blob 事件，並將該佇列連接至 Azure 儲存體帳戶。</span><span class="sxs-lookup"><span data-stu-id="c06b8-126">Choose all the Blob events that the queue will receive, and connect the queue to the Azure Storage account.</span></span>

## <a name="manage-search-permissions"></a><span data-ttu-id="c06b8-127">管理搜尋許可權</span><span class="sxs-lookup"><span data-stu-id="c06b8-127">Manage search permissions</span></span>

### <a name="azure-data-lake-gen-2"></a><span data-ttu-id="c06b8-128">Azure Data Lake Gen 2</span><span class="sxs-lookup"><span data-stu-id="c06b8-128">Azure Data Lake Gen 2</span></span>

<span data-ttu-id="c06b8-129">在 [ **管理搜尋許可權** ] 畫面上，您可以選擇從您的 [Azure Data Lake Gen 2 儲存體](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) 帳戶中 (ACLs) 上插入存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="c06b8-129">On the **Manage search permissions** screen, you can choose to ingest the Access Control Lists (ACLs) from your [Azure Data Lake Gen 2 Storage](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) account.</span></span> <span data-ttu-id="c06b8-130">當您設定這些搜尋許可權時，會根據指派給已登入之 [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/) 使用者搜尋內容的許可權來裁切搜尋內容。</span><span class="sxs-lookup"><span data-stu-id="c06b8-130">When these search permissions are set, search content is trimmed based on the permissions assigned to the signed-in [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/) user searching the content.</span></span> <span data-ttu-id="c06b8-131">或者，您也可以選擇讓組織中的所有人都可以看到從您的儲存體帳戶索引的所有內容。</span><span class="sxs-lookup"><span data-stu-id="c06b8-131">Alternatively, you can choose to make all the content indexed from your storage account visible to everyone in your organization.</span></span> <span data-ttu-id="c06b8-132">在此情況下，您組織中的每個人都可以存取您儲存體帳戶中的所有資料。</span><span class="sxs-lookup"><span data-stu-id="c06b8-132">In this case, everyone in your organization will have access to all the data in your storage account.</span></span>

### <a name="azure-blob-storage"></a><span data-ttu-id="c06b8-133">Azure Blob 儲存體</span><span class="sxs-lookup"><span data-stu-id="c06b8-133">Azure Blob Storage</span></span>

<span data-ttu-id="c06b8-134">若要連線至 [Azure Blob 儲存](https://docs.microsoft.com/azure/storage/blobs/storage-blobs-introduction)，您組織中的所有人都會看到所有從設定之來源編制索引的內容。</span><span class="sxs-lookup"><span data-stu-id="c06b8-134">For a connection to [Azure Blob Storage](https://docs.microsoft.com/azure/storage/blobs/storage-blobs-introduction), all the content indexed from the configured source is visible to everyone in your organization.</span></span> <span data-ttu-id="c06b8-135">Azure Blob 儲存區的 Blob 層級不支援存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="c06b8-135">Access control lists are not supported at Blob level in Azure Blob Storage.</span></span>

## <a name="manage-search-permissions"></a><span data-ttu-id="c06b8-136">管理搜尋許可權</span><span class="sxs-lookup"><span data-stu-id="c06b8-136">Manage search permissions</span></span>

<span data-ttu-id="c06b8-137">Azure Data Lake Storage Gen2 connector 可讓 **所有人** 或 **只有存取此資料來源的人** 都能看到搜尋許可權。</span><span class="sxs-lookup"><span data-stu-id="c06b8-137">The Azure Data Lake Storage Gen2 connector supports search permissions visible to **Everyone** or **Only people with access to this data source**.</span></span> <span data-ttu-id="c06b8-138">在搜尋結果中顯示的索引資料，可對組織中的所有使用者或只有具有每個專案之存取權的使用者顯示。</span><span class="sxs-lookup"><span data-stu-id="c06b8-138">Indexed data that appears in the search results could be visible to all users in the organization or only to users who have access to each item.</span></span>

## <a name="assign-property-labels"></a><span data-ttu-id="c06b8-139">指派屬性標籤</span><span class="sxs-lookup"><span data-stu-id="c06b8-139">Assign property labels</span></span>

<span data-ttu-id="c06b8-140">您可以從選項的功能表中選擇，將 source 屬性指派給每個標籤。</span><span class="sxs-lookup"><span data-stu-id="c06b8-140">You can assign a source property to each label by choosing from a menu of options.</span></span> <span data-ttu-id="c06b8-141">雖然這個步驟不是必要的，但具有一些屬性標籤會提升搜尋相關性，並可確保使用者更準確的搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="c06b8-141">While this step is not mandatory, having some property labels will improve the search relevance and ensure more accurate search results for end users.</span></span>

## <a name="manage-schema"></a><span data-ttu-id="c06b8-142">管理架構</span><span class="sxs-lookup"><span data-stu-id="c06b8-142">Manage schema</span></span>

<span data-ttu-id="c06b8-143">在 [**管理架構**] 畫面上，您可以選擇變更架構屬性 (可 **查詢**、**可搜尋、可\*\*\*\*檢索** 及 **可精簡搜尋**) 相關聯的屬性、新增選用的別名，然後選擇 **Content** 屬性。</span><span class="sxs-lookup"><span data-stu-id="c06b8-143">On the **Manage Schema** screen, you have the option to change the schema attributes (**queryable**, **searchable**, **retrievable**, and **refinable**) associated with the properties, add optional aliases, and choose the **Content** property.</span></span>

## <a name="set-the-refresh-schedule"></a><span data-ttu-id="c06b8-144">設定重新整理排程</span><span class="sxs-lookup"><span data-stu-id="c06b8-144">Set the refresh schedule</span></span>

<span data-ttu-id="c06b8-145">在 [重新整理 **設定** ] 畫面上，您可以設定增量編目間隔和完整編目間隔。</span><span class="sxs-lookup"><span data-stu-id="c06b8-145">On the **Refresh Settings** screen, you can set the incremental crawl interval and the full crawl interval.</span></span> <span data-ttu-id="c06b8-146">針對增量編目，Azure Data Lake Storage Gen2 connector 的預設間隔是15分鐘，完整編目則為一周。</span><span class="sxs-lookup"><span data-stu-id="c06b8-146">The default intervals for the Azure Data Lake Storage Gen2 connector are 15 minutes for an incremental crawl and one week for a full crawl.</span></span>

## <a name="limitations"></a><span data-ttu-id="c06b8-147">限制</span><span class="sxs-lookup"><span data-stu-id="c06b8-147">Limitations</span></span>

<span data-ttu-id="c06b8-148">無法為 Azure Data Lake Storage Gen2 source 重新設定 Azure Blob 儲存的發佈連線，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="c06b8-148">A published connection for Azure Blob Storage cannot be reconfigured for Azure Data Lake Storage Gen2 source and vice-versa.</span></span> <span data-ttu-id="c06b8-149">在這種情況下，建議您設定新的連線。</span><span class="sxs-lookup"><span data-stu-id="c06b8-149">In such scenarios, it is recommended to configure a new connection.</span></span>
