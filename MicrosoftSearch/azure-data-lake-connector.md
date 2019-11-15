---
title: Microsoft Search 的 azure Data Lake 連接器
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
description: 設定 Microsoft Search Azure Data Lake 儲存 Gen2 連接器
ms.openlocfilehash: 392960a5f7e6c93442ac7e1f60245217e194b42b
ms.sourcegitcommit: 21361af7c244ffd6ff8689fd0ff0daa359bf4129
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/14/2019
ms.locfileid: "38626469"
---
# <a name="azure-data-lake-storage-gen2-connector-for-microsoft-search"></a><span data-ttu-id="814fd-103">Microsoft Search 的 azure Data Lake 儲存 Gen2 連接器</span><span class="sxs-lookup"><span data-stu-id="814fd-103">Azure Data Lake Storage Gen2 connector for Microsoft Search</span></span>

<span data-ttu-id="814fd-104">使用[Azure Data Lake 儲存 Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction)連接器，您組織中的使用者可以搜尋的檔案和其內容。</span><span class="sxs-lookup"><span data-stu-id="814fd-104">With the [Azure Data Lake Storage Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) connector, users in your organization can search for files and their content.</span></span> <span data-ttu-id="814fd-105">此連接器存取儲存在 Azure Blob 容器和內 Azure Data Lake 儲存第 2 帳戶已啟用階層的資料夾中的資料。</span><span class="sxs-lookup"><span data-stu-id="814fd-105">This connector accesses data stored in Azure Blob containers and hierarchy-enabled folders within an Azure Data Lake Storage Gen 2 account.</span></span>

<span data-ttu-id="814fd-106">本文適用於[Microsoft 365](https://www.microsoft.com/microsoft-365)系統管理員或人設定、 執行，並監視 Azure Data Lake 儲存 Gen2 連接器。</span><span class="sxs-lookup"><span data-stu-id="814fd-106">This article is for [Microsoft 365](https://www.microsoft.com/microsoft-365) administrators or anyone who configures, runs, and monitors an Azure Data Lake Storage Gen2 connector.</span></span> <span data-ttu-id="814fd-107">本文說明如何設定連接器，連接器功能、 限制和疑難排解技巧。</span><span class="sxs-lookup"><span data-stu-id="814fd-107">It explains how to configure your connector and connector capabilities, limitations, and troubleshooting techniques.</span></span>

## <a name="connect-to-a-data-source"></a><span data-ttu-id="814fd-108">連線至資料來源</span><span class="sxs-lookup"><span data-stu-id="814fd-108">Connect to a data source</span></span>

### <a name="primary-storage-connection-string"></a><span data-ttu-id="814fd-109">主要儲存區的連接字串</span><span class="sxs-lookup"><span data-stu-id="814fd-109">Primary storage connection string</span></span> 
<span data-ttu-id="814fd-110">在 [**驗證設定**] 畫面中，提供主要存放裝置連接字串。</span><span class="sxs-lookup"><span data-stu-id="814fd-110">On the **Authentication and config** screen, provide the Primary Storage Connection String.</span></span> <span data-ttu-id="814fd-111">若要允許您儲存體帳戶的存取權，才該字串。</span><span class="sxs-lookup"><span data-stu-id="814fd-111">That string is required to allow access to your storage account.</span></span> <span data-ttu-id="814fd-112">若要尋找您的連接字串，請移至[Azure 入口網站](https://ms.portal.azure.com/#home)，並瀏覽至 [**機碼**] 區段中的[Azure Data Lake 儲存 Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction)帳戶。</span><span class="sxs-lookup"><span data-stu-id="814fd-112">To find your connection string, go to the [Azure portal](https://ms.portal.azure.com/#home) and navigate to the **Keys** section of the [Azure Data Lake Storage Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) account.</span></span> <span data-ttu-id="814fd-113">複製並貼在螢幕上適當的欄位中的連接字串。</span><span class="sxs-lookup"><span data-stu-id="814fd-113">Copy and paste the connection string in the appropriate field on the screen.</span></span>

<span data-ttu-id="814fd-114">如果您不想要提供**AccountKey** （主要儲存區連接字串中的參數），您必須授與我們圖的連接器服務的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="814fd-114">If you don't want to provide the **AccountKey** (a parameter in the primary storage connection string), you have to grant read access to our Graph Connectors Service.</span></span> <span data-ttu-id="814fd-115">在您的 Azure Data Lake 儲存 Gen2 帳戶的 [**存取控制**] 索引標籤中，依照指示，授與存取權的下列應用程式] 頁面上：</span><span class="sxs-lookup"><span data-stu-id="814fd-115">In the **Access Control** tab of your Azure Data Lake Storage Gen2 account, follow the instructions on that page to grant access to the following app:</span></span>
* <span data-ttu-id="814fd-116">**第一方應用程式識別碼：** 56c1da01-2129-48f7-9355-af6d59d42766</span><span class="sxs-lookup"><span data-stu-id="814fd-116">**First Party App ID:** 56c1da01-2129-48f7-9355-af6d59d42766</span></span>
* <span data-ttu-id="814fd-117">**第一方應用程式名稱：** Graph 連接器服務</span><span class="sxs-lookup"><span data-stu-id="814fd-117">**First Party App Name:** Graph Connector Service</span></span>

### <a name="storage-account-and-queue-notifications-optional"></a><span data-ttu-id="814fd-118">儲存體帳戶和佇列通知 （選用）</span><span class="sxs-lookup"><span data-stu-id="814fd-118">Storage account and queue notifications (Optional)</span></span>
<span data-ttu-id="814fd-119">支援，以處理即時圖表連接器服務中的變更可能在未來新增。</span><span class="sxs-lookup"><span data-stu-id="814fd-119">Support to process changes in real time in the Graph Connectors Service might be added in the future.</span></span> <span data-ttu-id="814fd-120">在此情況下，我們將會監視儲存在佇列中的[Azure Data Lake 儲存 Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction)變更通知。</span><span class="sxs-lookup"><span data-stu-id="814fd-120">In that case, we'll monitor [Azure Data Lake Storage Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) change notifications stored in a queue.</span></span> <span data-ttu-id="814fd-121">您需要您 Azure Data Lake 儲存 Gen2 相同的帳戶或另一個儲存體帳戶中建立佇列。</span><span class="sxs-lookup"><span data-stu-id="814fd-121">You'll need to create a queue in the same account as your Azure Data Lake Storage Gen2 or in another storage account.</span></span>

<span data-ttu-id="814fd-122">建立佇列之後，移至 [**事件**] 索引標籤上 [佇列] 頁面上，若要設定**事件訂閱**。</span><span class="sxs-lookup"><span data-stu-id="814fd-122">After you create a queue, go to the **Events** tab on the queue page to configure **Event Subscription**.</span></span> <span data-ttu-id="814fd-123">選擇 [所有 Blob 事件佇列將會接收，並將佇列連線到 Azure Data Lake 儲存 Gen2 帳戶]。</span><span class="sxs-lookup"><span data-stu-id="814fd-123">Choose all the Blob events that the queue will receive, and connect the queue to the Azure Data Lake Storage Gen2 account.</span></span>

## <a name="manage-the-search-schema"></a><span data-ttu-id="814fd-124">管理搜尋結構描述</span><span class="sxs-lookup"><span data-stu-id="814fd-124">Manage the search schema</span></span>
<span data-ttu-id="814fd-125">**管理結構描述**在畫面上，您可以選擇變更的結構描述屬性 (**設為可查詢**、**可搜尋**，並**可擷取**) 相關聯的 managed 屬性。</span><span class="sxs-lookup"><span data-stu-id="814fd-125">On the **Manage Schema** screen, you have the option to change the schema attributes (**queryable**, **searchable**, and **retrievable**) associated with the managed properties.</span></span> <span data-ttu-id="814fd-126">這些 managed 的屬性的屬性是從您的[Azure Data Lake 儲存 Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction)帳戶編製索引的資料。</span><span class="sxs-lookup"><span data-stu-id="814fd-126">These managed property attributes are data indexed from your [Azure Data Lake Storage Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) account.</span></span>

## <a name="manage-search-permissions"></a><span data-ttu-id="814fd-127">管理搜尋的權限</span><span class="sxs-lookup"><span data-stu-id="814fd-127">Manage search permissions</span></span>
<span data-ttu-id="814fd-128">在 [**管理搜尋的權限**] 畫面中，您可以選擇內嵌的存取控制清單 (Acl) 從您的儲存體帳戶。</span><span class="sxs-lookup"><span data-stu-id="814fd-128">On the **Manage search permissions** screen, you can choose to ingest the Access Control Lists (ACLs) from your storage account.</span></span> <span data-ttu-id="814fd-129">當這些搜尋權限設定時，搜尋內容修剪根據指派給登入[Azure Active Directory](https://docs.microsoft.com/azure/active-directory/)使用者搜尋內容的權限。</span><span class="sxs-lookup"><span data-stu-id="814fd-129">When these search permissions are set, search content is trimmed based on the permissions assigned to the signed-in [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/) user searching the content.</span></span> <span data-ttu-id="814fd-130">或者，您可以選擇要從組織中的每個人都可以看到您儲存體帳戶編製索引的所有內容。</span><span class="sxs-lookup"><span data-stu-id="814fd-130">Alternatively, you can choose to make all the content indexed from your storage account visible to everyone in your organization.</span></span> <span data-ttu-id="814fd-131">在此情況下，您的組織中的每個人儲存體帳戶中有存取權的所有資料。</span><span class="sxs-lookup"><span data-stu-id="814fd-131">In this case, everyone in your organization will have access to all the data in your storage account.</span></span>
 
## <a name="set-the-refresh-schedule"></a><span data-ttu-id="814fd-132">設定重新整理排程</span><span class="sxs-lookup"><span data-stu-id="814fd-132">Set the refresh schedule</span></span>
<span data-ttu-id="814fd-133">在 [**重新整理設定**] 畫面中，您可以設定的累加編目間隔及完整編目間隔。</span><span class="sxs-lookup"><span data-stu-id="814fd-133">On the **Refresh Settings** screen, you can set the incremental crawl interval and the full crawl interval.</span></span> <span data-ttu-id="814fd-134">[Azure Data Lake 儲存 Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction)連接器的預設間隔為 15 分鐘，進行累加編目和一週進行完整編目。</span><span class="sxs-lookup"><span data-stu-id="814fd-134">The default intervals for the [Azure Data Lake Storage Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) connector are 15 minutes for an incremental crawl and one week for a full crawl.</span></span>
 
## <a name="limitations"></a><span data-ttu-id="814fd-135">限制</span><span class="sxs-lookup"><span data-stu-id="814fd-135">Limitations</span></span>
<span data-ttu-id="814fd-136">目前， [Azure Data Lake 儲存 Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction)多重通訊協定存取只能在中央美國、 西中央美國、 加拿大中央、 美國東部、 東亞、 北歐、 東亞 US2、 東南亞、 西歐、 美國西部、 澳洲東亞、 日本東、 西 US2 和巴西南是可用。</span><span class="sxs-lookup"><span data-stu-id="814fd-136">Currently, [Azure Data Lake Storage Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) Multi-Protocol Access is available only in the Central US, West Central US, Canada Central, East US, East Asia, North Europe, East US2, South East Asia, West Europe, West US, Australia East, Japan East, West US2, and Brazil South.</span></span>

<span data-ttu-id="814fd-137">更新與詳細資訊，請參閱[在 Azure Data Lake 儲存體 （預覽） 上存取的多重通訊協定](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-multi-protocol-access)。</span><span class="sxs-lookup"><span data-stu-id="814fd-137">For updates and more information, see  [Multi-protocol access on Azure Data Lake Storage (preview)](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-multi-protocol-access).</span></span>


