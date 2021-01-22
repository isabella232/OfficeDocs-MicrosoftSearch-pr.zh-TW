---
title: 適用于 Microsoft Search 的 Azure Data Lake 連接器
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
description: 為 Microsoft Search 設定 Azure Data Lake Storage Gen2 連接器
ms.openlocfilehash: 8891c9a1fdf5397c397a941b5131f014db9e7a54
ms.sourcegitcommit: 597c338bf9c1c425747ac74a9a1ae57c5e8957ce
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/21/2021
ms.locfileid: "49920720"
---
# <a name="azure-data-lake-storage-gen2-connector"></a><span data-ttu-id="20744-103">Azure Data Lake Storage Gen2 連接器</span><span class="sxs-lookup"><span data-stu-id="20744-103">Azure Data Lake Storage Gen2 connector</span></span>

<span data-ttu-id="20744-104">使用 Azure Data Lake Storage Gen2 連接器，貴組織的使用者可以搜尋儲存在 [Azure Blob](https://docs.microsoft.com/azure/storage/blobs/storage-blobs-introduction) 儲存體和 [Azure Data Lake Gen 2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) 儲存體帳戶中的檔案。</span><span class="sxs-lookup"><span data-stu-id="20744-104">With the Azure Data Lake Storage Gen2 connector, users in your organization can search for files stored in [Azure Blob Storage](https://docs.microsoft.com/azure/storage/blobs/storage-blobs-introduction) and [Azure Data Lake Gen 2 Storage](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) accounts.</span></span>

<span data-ttu-id="20744-105">本文適用于 [Microsoft 365](https://www.microsoft.com/microsoft-365) 系統管理員，或任何設定、執行及監控 Azure Data Lake Storage Gen2 連接器的人。</span><span class="sxs-lookup"><span data-stu-id="20744-105">This article is for [Microsoft 365](https://www.microsoft.com/microsoft-365) administrators or anyone who configures, runs, and monitors an Azure Data Lake Storage Gen2 connector.</span></span> <span data-ttu-id="20744-106">它提供連接器組配置、功能、限制和疑難排解技巧概觀。</span><span class="sxs-lookup"><span data-stu-id="20744-106">It gives an overview of the connector configuration, capabilities, limitations, and troubleshooting techniques.</span></span> <span data-ttu-id="20744-107">在本文中，我們使用 *Azure 儲存體* 做為 [Azure Blob](https://docs.microsoft.com/azure/storage/blobs/storage-blobs-introduction) 儲存體和 [Azure Data Lake Gen 2 儲存體的通用術語](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction)。</span><span class="sxs-lookup"><span data-stu-id="20744-107">In the article, we use *Azure Storage* as a generic term for [Azure Blob Storage](https://docs.microsoft.com/azure/storage/blobs/storage-blobs-introduction) and [Azure Data Lake Gen 2 Storage](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction).</span></span>

## <a name="connect-to-a-data-source"></a><span data-ttu-id="20744-108">連接到資料來源</span><span class="sxs-lookup"><span data-stu-id="20744-108">Connect to a data source</span></span>

### <a name="primary-storage-connection-string"></a><span data-ttu-id="20744-109">主要儲存空間連接字串</span><span class="sxs-lookup"><span data-stu-id="20744-109">Primary storage connection string</span></span>

<span data-ttu-id="20744-110">在驗證 **與設定檔畫面上** ，提供主要儲存空間連接字串。</span><span class="sxs-lookup"><span data-stu-id="20744-110">On the **Authentication and config** screen, provide the Primary Storage Connection String.</span></span> <span data-ttu-id="20744-111">需要該字串才能存取儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="20744-111">That string is required to allow access to your storage account.</span></span> <span data-ttu-id="20744-112">若要尋找您的連接字串，請前往 [Azure 入口](https://ms.portal.azure.com/#home) 網站，然後流覽至相關 Azure 儲存體 **帳戶的金鑰** 區段。</span><span class="sxs-lookup"><span data-stu-id="20744-112">To find your connection string, go to the [Azure portal](https://ms.portal.azure.com/#home) and navigate to the **Keys** section of your relevant Azure Storage account.</span></span> <span data-ttu-id="20744-113">在畫面上的適當欄位中複製並貼上連接字串。</span><span class="sxs-lookup"><span data-stu-id="20744-113">Copy and paste the connection string in the appropriate field on the screen.</span></span>

<span data-ttu-id="20744-114">如果您不想在主要儲存連接字串 (中提供 **AccountKey**) 參數，您必須為下列角色授予圖形連接器服務的存取權。</span><span class="sxs-lookup"><span data-stu-id="20744-114">If you do not prefer to provide the **AccountKey** (a parameter in the primary storage connection string), you will need to grant access to our Graph Connectors Service for the following roles.</span></span> <span data-ttu-id="20744-115"> (只支援階層式儲存功能。</span><span class="sxs-lookup"><span data-stu-id="20744-115">(This feature is only supported for hierarchical storage.</span></span> <span data-ttu-id="20744-116">傳統的 Blob 儲存體必須提供 AccountKey.) </span><span class="sxs-lookup"><span data-stu-id="20744-116">Traditional Blob storage will have to provide AccountKey.)</span></span>
* <span data-ttu-id="20744-117">儲存體 Blob 資料讀取程式</span><span class="sxs-lookup"><span data-stu-id="20744-117">Storage Blob Data Reader</span></span>
* <span data-ttu-id="20744-118">儲存佇列資料參與者</span><span class="sxs-lookup"><span data-stu-id="20744-118">Storage Queue Data Contributor</span></span>
* <span data-ttu-id="20744-119">儲存體 Blob Delegator</span><span class="sxs-lookup"><span data-stu-id="20744-119">Storage Blob Delegator</span></span>

<span data-ttu-id="20744-120">流覽至 **Azure 儲存體** 帳戶的 Access Control Tab，並遵循指示以授予下列應用程式的存取權：</span><span class="sxs-lookup"><span data-stu-id="20744-120">Navigate to the **Access Control** tab of your Azure Storage account, and follow the instructions there to grant access to the following app:</span></span>

* <span data-ttu-id="20744-121">**第一方應用程式識別碼** ：56c1da01-2129-48f7-9355-af6d59d42766</span><span class="sxs-lookup"><span data-stu-id="20744-121">**First Party App ID:** 56c1da01-2129-48f7-9355-af6d59d42766</span></span>
* <span data-ttu-id="20744-122">**第一方應用程式名稱：** 圖形連接器服務</span><span class="sxs-lookup"><span data-stu-id="20744-122">**First Party App Name:** Graph Connector Service</span></span>

### <a name="storage-account-and-queue-notifications-optional"></a><span data-ttu-id="20744-123">儲存空間帳戶和佇列通知 (選填) </span><span class="sxs-lookup"><span data-stu-id="20744-123">Storage account and queue notifications (Optional)</span></span>

<span data-ttu-id="20744-124">未來可能會新增圖形連接器服務中即時處理變更的支援。</span><span class="sxs-lookup"><span data-stu-id="20744-124">Support to process changes in real time in the Graph Connectors Service might be added in the future.</span></span> <span data-ttu-id="20744-125">在這種情況下，我們會監視儲存在佇列中的 Azure 儲存體變更通知。</span><span class="sxs-lookup"><span data-stu-id="20744-125">In that case, we'll monitor Azure Storage change notifications stored in a queue.</span></span> <span data-ttu-id="20744-126">您必須在 Azure 儲存體帳戶的同一個帳戶中建立佇列。</span><span class="sxs-lookup"><span data-stu-id="20744-126">You'll need to create a queue in the same account as your Azure Storage account.</span></span>

<span data-ttu-id="20744-127">建立佇列之後，請前往佇列頁面上的事件分頁以設定 **事件訂閱**。</span><span class="sxs-lookup"><span data-stu-id="20744-127">After you create a queue, go to the **Events** tab on the queue page to configure **Event Subscription**.</span></span> <span data-ttu-id="20744-128">選擇佇列將接收的所有 Blob 事件，將佇列連接到 Azure 儲存體帳戶。</span><span class="sxs-lookup"><span data-stu-id="20744-128">Choose all the Blob events that the queue will receive, and connect the queue to the Azure Storage account.</span></span>

## <a name="manage-search-permissions"></a><span data-ttu-id="20744-129">管理搜尋許可權</span><span class="sxs-lookup"><span data-stu-id="20744-129">Manage search permissions</span></span>

### <a name="azure-data-lake-gen-2"></a><span data-ttu-id="20744-130">Azure Data Lake Gen 2</span><span class="sxs-lookup"><span data-stu-id="20744-130">Azure Data Lake Gen 2</span></span>

<span data-ttu-id="20744-131">在管理 **搜尋** 許可權畫面上，您可以選擇從 [Azure Data Lake Gen 2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) 儲存體帳戶 (存取控制清單) URL 清單。</span><span class="sxs-lookup"><span data-stu-id="20744-131">On the **Manage search permissions** screen, you can choose to ingest the Access Control Lists (ACLs) from your [Azure Data Lake Gen 2 Storage](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) account.</span></span> <span data-ttu-id="20744-132">設定這些搜尋許可權時，搜尋內容會根據指派給已簽署 [之 Azure Active Directory](https://docs.microsoft.com/azure/active-directory/) 使用者搜尋內容的許可權進行修剪。</span><span class="sxs-lookup"><span data-stu-id="20744-132">When these search permissions are set, search content is trimmed based on the permissions assigned to the signed-in [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/) user searching the content.</span></span> <span data-ttu-id="20744-133">或者，您可以選擇讓貴組織中所有人看到您儲存帳戶中所有已編制索引的內容。</span><span class="sxs-lookup"><span data-stu-id="20744-133">Alternatively, you can choose to make all the content indexed from your storage account visible to everyone in your organization.</span></span> <span data-ttu-id="20744-134">在這種情況下，貴組織全體人員將能存取您儲存空間帳戶中的所有資料。</span><span class="sxs-lookup"><span data-stu-id="20744-134">In this case, everyone in your organization will have access to all the data in your storage account.</span></span>

### <a name="azure-blob-storage"></a><span data-ttu-id="20744-135">Azure Blob 儲存體</span><span class="sxs-lookup"><span data-stu-id="20744-135">Azure Blob Storage</span></span>

<span data-ttu-id="20744-136">若要與 [Azure Blob 儲存體](https://docs.microsoft.com/azure/storage/blobs/storage-blobs-introduction)建立連結，貴組織中所有人都能看到從已配置來源建立索引的所有內容。</span><span class="sxs-lookup"><span data-stu-id="20744-136">For a connection to [Azure Blob Storage](https://docs.microsoft.com/azure/storage/blobs/storage-blobs-introduction), all the content indexed from the configured source is visible to everyone in your organization.</span></span> <span data-ttu-id="20744-137">Azure Blob 儲存體中的 Blob 層級不支援存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="20744-137">Access control lists are not supported at Blob level in Azure Blob Storage.</span></span>

## <a name="search-permissions"></a><span data-ttu-id="20744-138">搜尋許可權</span><span class="sxs-lookup"><span data-stu-id="20744-138">Search permissions</span></span>

<span data-ttu-id="20744-139">Azure Data Lake Storage Gen2 連接器支援對所有人可見 **或** 只有擁有此 **資料來源存取權的人所看見的搜尋許可權**。</span><span class="sxs-lookup"><span data-stu-id="20744-139">The Azure Data Lake Storage Gen2 connector supports search permissions visible to **Everyone** or **Only people with access to this data source**.</span></span> <span data-ttu-id="20744-140">組織所有使用者或只有具有每個專案存取權的使用者，才能看到出現在搜尋結果中的索引資料。</span><span class="sxs-lookup"><span data-stu-id="20744-140">Indexed data that appears in the search results could be visible to all users in the organization or only to users who have access to each item.</span></span>

## <a name="assign-property-labels"></a><span data-ttu-id="20744-141">指派屬性標籤</span><span class="sxs-lookup"><span data-stu-id="20744-141">Assign property labels</span></span>

<span data-ttu-id="20744-142">您可以選擇選項功能表，為每個標籤指定來源屬性。</span><span class="sxs-lookup"><span data-stu-id="20744-142">You can assign a source property to each label by choosing from a menu of options.</span></span> <span data-ttu-id="20744-143">雖然這不是強制步驟，但擁有一些屬性標籤將能改善搜尋相關性，並確保使用者獲得更精確的搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="20744-143">While this step is not mandatory, having some property labels will improve the search relevance and ensure more accurate search results for end users.</span></span>

## <a name="manage-schema"></a><span data-ttu-id="20744-144">管理架構</span><span class="sxs-lookup"><span data-stu-id="20744-144">Manage schema</span></span>

<span data-ttu-id="20744-145">在管理架構畫面上，您可以選擇變更與屬性關聯的架構屬性 (可查詢、可搜尋、可取及可精簡 **) 、** 新增選擇性別名，然後選擇 **內容** 屬性。</span><span class="sxs-lookup"><span data-stu-id="20744-145">On the **Manage Schema** screen, you have the option to change the schema attributes (**queryable**, **searchable**, **retrievable**, and **refinable**) associated with the properties, add optional aliases, and choose the **Content** property.</span></span>

## <a name="set-the-refresh-schedule"></a><span data-ttu-id="20744-146">設定重新更新排程</span><span class="sxs-lookup"><span data-stu-id="20744-146">Set the refresh schedule</span></span>

<span data-ttu-id="20744-147">在重新 **整點設定** 畫面上，您可以設定遞增編編間隔和完整編編間隔。</span><span class="sxs-lookup"><span data-stu-id="20744-147">On the **Refresh Settings** screen, you can set the incremental crawl interval and the full crawl interval.</span></span> <span data-ttu-id="20744-148">Azure Data Lake Storage Gen2 連接器的預設間隔為 15 分鐘，用於進行增量爬網，以及一周進行完整爬網。</span><span class="sxs-lookup"><span data-stu-id="20744-148">The default intervals for the Azure Data Lake Storage Gen2 connector are 15 minutes for an incremental crawl and one week for a full crawl.</span></span>

## <a name="limitations"></a><span data-ttu-id="20744-149">限制</span><span class="sxs-lookup"><span data-stu-id="20744-149">Limitations</span></span>

<span data-ttu-id="20744-150">無法重新針對 Azure Data Lake Storage Gen2 來源重新建立 Azure Blob 儲存體的已發佈連接，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="20744-150">A published connection for Azure Blob Storage cannot be reconfigured for Azure Data Lake Storage Gen2 source and vice-versa.</span></span> <span data-ttu-id="20744-151">在這種情況下，建議您設定新連接。</span><span class="sxs-lookup"><span data-stu-id="20744-151">In such scenarios, it is recommended to configure a new connection.</span></span>
