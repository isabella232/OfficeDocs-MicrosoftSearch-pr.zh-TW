---
title: Microsoft 搜尋的 Azure Data Lake Graph 連接器
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
description: 設定 Azure Data Lake Storage Gen2 Graph connector for Microsoft Search
ms.openlocfilehash: da508694929d3c83a456c664aa4613b09a1b14a3
ms.sourcegitcommit: d39113376db26333872d3a2c7baddc3a3a7aea61
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/03/2021
ms.locfileid: "50084855"
---
<!---Previous ms.author: monaray --->

# <a name="azure-data-lake-storage-gen2-graph-connector"></a><span data-ttu-id="5ef05-103">Azure Data Lake Storage Gen2 Graph connector</span><span class="sxs-lookup"><span data-stu-id="5ef05-103">Azure Data Lake Storage Gen2 Graph connector</span></span>

<span data-ttu-id="5ef05-104">Azure Data Lake Storage Gen2 Graph connector 可讓您組織中的使用者搜尋 [Azure Blob 儲存區](https://docs.microsoft.com/azure/storage/blobs/storage-blobs-introduction) 和 [Azure Data Lake Gen 2 儲存體](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) 帳戶中儲存的檔案。</span><span class="sxs-lookup"><span data-stu-id="5ef05-104">The Azure Data Lake Storage Gen2 Graph connector allows users in your organization to search for files stored in [Azure Blob Storage](https://docs.microsoft.com/azure/storage/blobs/storage-blobs-introduction) and [Azure Data Lake Gen 2 Storage](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) accounts.</span></span>

> [!NOTE]
> <span data-ttu-id="5ef05-105">請閱讀 [**您的圖形連接器文章設定**](configure-connector.md) ，以瞭解一般圖表連接器設定程式。</span><span class="sxs-lookup"><span data-stu-id="5ef05-105">Read the [**Setup your Graph connector**](configure-connector.md) article to understand the general Graph connectors setup process.</span></span>

<span data-ttu-id="5ef05-106">本文適用于任何設定、執行及監視 Azure Data Lake Storage Gen2 connector 的人員。</span><span class="sxs-lookup"><span data-stu-id="5ef05-106">This article is for anyone who configures, runs, and monitors an Azure Data Lake Storage Gen2 connector.</span></span> <span data-ttu-id="5ef05-107">它會補充一般設定程式，並顯示只適用于 Azure Data Lake Storage Gen2 connector 的指示。</span><span class="sxs-lookup"><span data-stu-id="5ef05-107">It supplements the general setup process, and shows instructions that apply only for the Azure Data Lake Storage Gen2 connector.</span></span> <span data-ttu-id="5ef05-108">本文也包含 [限制](#limitations)的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5ef05-108">This article also includes information about [Limitations](#limitations).</span></span>

<span data-ttu-id="5ef05-109">在本文中，我們使用 *Azure Storage* 做為 [Azure Blob 儲存區](https://docs.microsoft.com/azure/storage/blobs/storage-blobs-introduction) 和 [Azure Data Lake Gen 2 儲存區](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction)的一般字詞。</span><span class="sxs-lookup"><span data-stu-id="5ef05-109">In the article, we use *Azure Storage* as a generic term for [Azure Blob Storage](https://docs.microsoft.com/azure/storage/blobs/storage-blobs-introduction) and [Azure Data Lake Gen 2 Storage](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction).</span></span>

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a><span data-ttu-id="5ef05-110">步驟1：在 Microsoft 365 系統管理中心新增圖表連接器</span><span class="sxs-lookup"><span data-stu-id="5ef05-110">Step 1: Add a Graph connector in the Microsoft 365 admin center</span></span>

<span data-ttu-id="5ef05-111">遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。</span><span class="sxs-lookup"><span data-stu-id="5ef05-111">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-2-name-the-connection"></a><span data-ttu-id="5ef05-112">步驟2：命名連線</span><span class="sxs-lookup"><span data-stu-id="5ef05-112">Step 2: Name the connection</span></span>

<span data-ttu-id="5ef05-113">遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。</span><span class="sxs-lookup"><span data-stu-id="5ef05-113">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-3-configure-the-connection-settings"></a><span data-ttu-id="5ef05-114">步驟3：設定連接設定</span><span class="sxs-lookup"><span data-stu-id="5ef05-114">Step 3: Configure the connection settings</span></span>

<span data-ttu-id="5ef05-115">輸入您的主要儲存體連接字串。</span><span class="sxs-lookup"><span data-stu-id="5ef05-115">Enter your Primary storage connection String.</span></span> <span data-ttu-id="5ef05-116">此字串是允許存取您的儲存體帳戶所需的字串。</span><span class="sxs-lookup"><span data-stu-id="5ef05-116">This string is required to allow access to your storage account.</span></span> <span data-ttu-id="5ef05-117">若要尋找您的連線字串，請移至 [Azure 入口網站](https://ms.portal.azure.com/#home) ，並流覽至相關 Azure 儲存體帳戶的 [機 **碼** ] 區段。</span><span class="sxs-lookup"><span data-stu-id="5ef05-117">To find your connection string, go to the [Azure portal](https://ms.portal.azure.com/#home) and navigate to the **Keys** section of your relevant Azure Storage account.</span></span>

<span data-ttu-id="5ef05-118">如果您不想要在主要儲存連接字串) 中提供 **AccountKey** (參數，請授與下列角色的圖形連接器服務存取權：</span><span class="sxs-lookup"><span data-stu-id="5ef05-118">If you prefer not to provide the **AccountKey** (a parameter in the primary storage connection string), grant access to our Graph Connectors Service for the following roles:</span></span>

* <span data-ttu-id="5ef05-119">儲存體 Blob 資料讀取器</span><span class="sxs-lookup"><span data-stu-id="5ef05-119">Storage Blob Data Reader</span></span>
* <span data-ttu-id="5ef05-120">儲存佇列資料參與者</span><span class="sxs-lookup"><span data-stu-id="5ef05-120">Storage Queue Data Contributor</span></span>
* <span data-ttu-id="5ef05-121">儲存 Blob Delegator</span><span class="sxs-lookup"><span data-stu-id="5ef05-121">Storage Blob Delegator</span></span>

<span data-ttu-id="5ef05-122">流覽至您的 Azure 儲存體帳戶的 [ **存取控制** ] 索引標籤，然後依照這裡的指示，將存取權授與下列應用程式：</span><span class="sxs-lookup"><span data-stu-id="5ef05-122">Navigate to the **Access Control** tab of your Azure Storage account, and follow the instructions there to grant access to the following app:</span></span>

* <span data-ttu-id="5ef05-123">**第一方應用程式 ID:** 56c1da01-2129-48f7-9355-af6d59d42766</span><span class="sxs-lookup"><span data-stu-id="5ef05-123">**First Party App ID:** 56c1da01-2129-48f7-9355-af6d59d42766</span></span>
* <span data-ttu-id="5ef05-124">**第一方應用程式名稱：** 圖形連接器服務</span><span class="sxs-lookup"><span data-stu-id="5ef05-124">**First Party App Name:** Graph Connector Service</span></span>

### <a name="storage-account-and-queue-notifications-optional"></a><span data-ttu-id="5ef05-125">儲存帳戶和佇列通知 (選用) </span><span class="sxs-lookup"><span data-stu-id="5ef05-125">Storage account and queue notifications (Optional)</span></span>

<span data-ttu-id="5ef05-126">可在未來新增圖表連接器服務中即時處理變更的支援。</span><span class="sxs-lookup"><span data-stu-id="5ef05-126">Support to process changes in real time in the Graph Connectors Service might be added in the future.</span></span> <span data-ttu-id="5ef05-127">在此情況下，我們會監視儲存在佇列中的 Azure 儲存體變更通知。</span><span class="sxs-lookup"><span data-stu-id="5ef05-127">In that case, we'll monitor Azure Storage change notifications stored in a queue.</span></span> <span data-ttu-id="5ef05-128">您必須使用與您的 Azure 儲存體帳戶相同的帳戶建立佇列。</span><span class="sxs-lookup"><span data-stu-id="5ef05-128">You'll need to create a queue in the same account as your Azure Storage account.</span></span>

<span data-ttu-id="5ef05-129">建立佇列之後，請移至佇列頁面上的 [ **事件** ] 索引標籤，以設定 **事件訂閱**。</span><span class="sxs-lookup"><span data-stu-id="5ef05-129">After you create a queue, go to the **Events** tab on the queue page to configure **Event Subscription**.</span></span> <span data-ttu-id="5ef05-130">選擇佇列將要接收的所有 Blob 事件，並將該佇列連接至 Azure 儲存體帳戶。</span><span class="sxs-lookup"><span data-stu-id="5ef05-130">Choose all the Blob events that the queue will receive, and connect the queue to the Azure Storage account.</span></span>

## <a name="step-4-assign-property-labels"></a><span data-ttu-id="5ef05-131">步驟4：指派屬性標籤</span><span class="sxs-lookup"><span data-stu-id="5ef05-131">Step 4: Assign property labels</span></span>

<span data-ttu-id="5ef05-132">您可以從選項的功能表中選擇，將 source 屬性指派給每個標籤。</span><span class="sxs-lookup"><span data-stu-id="5ef05-132">You can assign a source property to each label by choosing from a menu of options.</span></span> <span data-ttu-id="5ef05-133">這個步驟不是必要的，具有一些屬性標籤會提升搜尋相關性，並確保使用者的更好搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="5ef05-133">While this step isn't mandatory, having some property labels will improve the search relevance and ensure better search results for end users.</span></span>

## <a name="step-5-manage-schema"></a><span data-ttu-id="5ef05-134">步驟5：管理架構</span><span class="sxs-lookup"><span data-stu-id="5ef05-134">Step 5: Manage schema</span></span>

<span data-ttu-id="5ef05-135">在 [ **管理架構** ] 畫面上，您可以變更與屬性相關聯的架構屬性、選項為 **查詢**、 **搜尋**、 **檢索** 及 **精煉**。</span><span class="sxs-lookup"><span data-stu-id="5ef05-135">On the **Manage Schema** screen, you can change the schema attributes associated with the properties, the options are **Query**, **Search**, **Retrieve**, and **Refine**.</span></span> <span data-ttu-id="5ef05-136">您也可以新增選擇性別名，並選擇 **Content** 屬性。</span><span class="sxs-lookup"><span data-stu-id="5ef05-136">You also can add optional aliases, and choose the **Content** property.</span></span>

## <a name="step-6-manage-search-permissions"></a><span data-ttu-id="5ef05-137">步驟6：管理搜尋許可權</span><span class="sxs-lookup"><span data-stu-id="5ef05-137">Step 6: Manage search permissions</span></span>

### <a name="azure-data-lake-gen-2"></a><span data-ttu-id="5ef05-138">Azure Data Lake Gen 2</span><span class="sxs-lookup"><span data-stu-id="5ef05-138">Azure Data Lake Gen 2</span></span>

<span data-ttu-id="5ef05-139">您可以選擇從您的 [Azure Data Lake Gen 2 儲存體](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) 帳戶中 (ACLs) 上插入存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="5ef05-139">You can choose to ingest the Access Control Lists (ACLs) from your [Azure Data Lake Gen 2 Storage](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) account.</span></span> <span data-ttu-id="5ef05-140">當您設定這些搜尋許可權時，會根據使用者在 [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/)中簽署的許可權來裁切搜尋內容。</span><span class="sxs-lookup"><span data-stu-id="5ef05-140">When these search permissions are set, search content is trimmed based on the permissions of the user signed in [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/).</span></span> <span data-ttu-id="5ef05-141">或者，您也可以選擇讓組織中的所有人都可以看到從您的儲存體帳戶索引的所有內容。</span><span class="sxs-lookup"><span data-stu-id="5ef05-141">Alternatively, you can choose to make all the content indexed from your storage account visible to everyone in your organization.</span></span> <span data-ttu-id="5ef05-142">在此情況下，您組織中的每個人都可以存取您儲存體帳戶中的所有資料。</span><span class="sxs-lookup"><span data-stu-id="5ef05-142">In this case, everyone in your organization will have access to all the data in your storage account.</span></span>

<span data-ttu-id="5ef05-143">Azure Data Lake Storage Gen2 Graph connector 支援 **所有人都** 可以看到的搜尋許可權，或 **只有存取此資料來源的人員**。</span><span class="sxs-lookup"><span data-stu-id="5ef05-143">The Azure Data Lake Storage Gen2 Graph connector supports search permissions visible to **Everyone**, or **Only people with access to this data source**.</span></span> <span data-ttu-id="5ef05-144">可以存取每個專案的組織中的使用者看不見搜尋結果中顯示的索引資料。</span><span class="sxs-lookup"><span data-stu-id="5ef05-144">Indexed data that appears in the search results could be visible to users in the organization who have access to each item.</span></span>

### <a name="azure-blob-storage"></a><span data-ttu-id="5ef05-145">Azure Blob 儲存體</span><span class="sxs-lookup"><span data-stu-id="5ef05-145">Azure Blob Storage</span></span>

<span data-ttu-id="5ef05-146">若要連線至 [Azure Blob 儲存](https://docs.microsoft.com/azure/storage/blobs/storage-blobs-introduction)，您組織中的所有人都會看到所有從設定之來源編制索引的內容。</span><span class="sxs-lookup"><span data-stu-id="5ef05-146">For a connection to [Azure Blob Storage](https://docs.microsoft.com/azure/storage/blobs/storage-blobs-introduction), all the content indexed from the configured source is visible to everyone in your organization.</span></span> <span data-ttu-id="5ef05-147">Azure Blob 儲存區的 Blob 層級不支援存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="5ef05-147">Access control lists aren't supported at Blob level in Azure Blob Storage.</span></span>

## <a name="step-7-set-the-refresh-schedule"></a><span data-ttu-id="5ef05-148">步驟7：設定重新整理排程</span><span class="sxs-lookup"><span data-stu-id="5ef05-148">Step 7: Set the refresh schedule</span></span>

<span data-ttu-id="5ef05-149">在 [重新整理 **設定** ] 畫面上，您可以設定增量編目間隔和完整編目間隔。</span><span class="sxs-lookup"><span data-stu-id="5ef05-149">On the **Refresh Settings** screen, you can set the incremental crawl interval and the full crawl interval.</span></span> <span data-ttu-id="5ef05-150">針對增量編目，Azure Data Lake Storage Gen2 connector 的預設間隔是15分鐘，完整編目則為一周。</span><span class="sxs-lookup"><span data-stu-id="5ef05-150">The default intervals for the Azure Data Lake Storage Gen2 connector are 15 minutes for an incremental crawl and one week for a full crawl.</span></span>

## <a name="step-8-review-connection"></a><span data-ttu-id="5ef05-151">步驟8：檢查連線</span><span class="sxs-lookup"><span data-stu-id="5ef05-151">Step 8: Review connection</span></span>

<span data-ttu-id="5ef05-152">遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。</span><span class="sxs-lookup"><span data-stu-id="5ef05-152">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

<!---## Troubleshooting-->
<!---Insert troubleshooting recommendations for this data source-->

## <a name="limitations"></a><span data-ttu-id="5ef05-153">限制</span><span class="sxs-lookup"><span data-stu-id="5ef05-153">Limitations</span></span>

<span data-ttu-id="5ef05-154">無法針對 Azure Data Lake Storage Gen2 來源及另一種方式，重新設定 Azure Blob 儲存的已發佈連線。</span><span class="sxs-lookup"><span data-stu-id="5ef05-154">A published connection for Azure Blob Storage cannot be reconfigured for Azure Data Lake Storage Gen2 source and the other way around.</span></span> <span data-ttu-id="5ef05-155">在這種情況下，建議您設定新的連線。</span><span class="sxs-lookup"><span data-stu-id="5ef05-155">In such scenarios, it's recommended to configure a new connection.</span></span>

<span data-ttu-id="5ef05-156">此外，檔案的大小必須為 4 MB 或更少的時間，才能進行編目。</span><span class="sxs-lookup"><span data-stu-id="5ef05-156">Also, the size of the files needs to be 4 MB or less for it to be crawled.</span></span> <span data-ttu-id="5ef05-157">目前支援的檔案類型包括：</span><span class="sxs-lookup"><span data-stu-id="5ef05-157">File types currently supported are:</span></span>

* <span data-ttu-id="5ef05-158">Word (.docx、.docm、dotx、normal.dotm) </span><span class="sxs-lookup"><span data-stu-id="5ef05-158">Word (docx, .docm, .dotx, .dotm)</span></span>
* <span data-ttu-id="5ef05-159">PowerPoint ( pptm，.pptx，potm，potx，ppam，. ppsm，. ppsx) </span><span class="sxs-lookup"><span data-stu-id="5ef05-159">PowerPoint (.pptm, .pptx, .potm, .potx, .ppam, .ppsm, .ppsx)</span></span>
* <span data-ttu-id="5ef05-160">Excel ( .xlsx，xlsm) </span><span class="sxs-lookup"><span data-stu-id="5ef05-160">Excel (.xlsx, .xlsm)</span></span>
* <span data-ttu-id="5ef05-161">舊版 Office 格式 ( .doc、.dot 等 ) </span><span class="sxs-lookup"><span data-stu-id="5ef05-161">Legacy Office formats (.doc, .dot, etc.)</span></span>
* <span data-ttu-id="5ef05-162">Text ( .txt) </span><span class="sxs-lookup"><span data-stu-id="5ef05-162">Text (.txt)</span></span>
* <span data-ttu-id="5ef05-163">HTML</span><span class="sxs-lookup"><span data-stu-id="5ef05-163">HTML</span></span>
* <span data-ttu-id="5ef05-164">PDF</span><span class="sxs-lookup"><span data-stu-id="5ef05-164">PDF</span></span>

<span data-ttu-id="5ef05-165">不支援像影像 ( .jpg、.bmp 等 ) 等二進位檔案。</span><span class="sxs-lookup"><span data-stu-id="5ef05-165">Binary files like images (.jpg, .bmp, etc.) are not supported.</span></span> <span data-ttu-id="5ef05-166">例如，如果 .docx 檔案只包含影像，它可能會略過，因為它未傳回任何內容。</span><span class="sxs-lookup"><span data-stu-id="5ef05-166">For example, if a .docx file contains only images, it might be skipped because it didn't return any content.</span></span>
