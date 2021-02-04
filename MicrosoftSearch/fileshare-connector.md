---
title: Microsoft 搜尋的檔案共用圖形連接器
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
ROBOTS: NoIndex
description: 設定 Microsoft 搜尋的檔案共用圖形連接器
ms.openlocfilehash: e8a68a1c6b9c2c8a8592fb915fe9bf846a758e77
ms.sourcegitcommit: d53b91f8f52a4a96281b66831c2449bbffe2177c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/03/2021
ms.locfileid: "50097419"
---
<!---Previous ms.author: rusamai --->

# <a name="file-share-graph-connector"></a><span data-ttu-id="2e4c7-103">檔案共用圖形連接器</span><span class="sxs-lookup"><span data-stu-id="2e4c7-103">File share Graph connector</span></span>

<span data-ttu-id="2e4c7-104">檔案共用圖表連接器可讓組織中的使用者搜尋內部部署 Windows 檔案共用。</span><span class="sxs-lookup"><span data-stu-id="2e4c7-104">The File share Graph connector allows users in your organization to search on-premise Windows file shares.</span></span>

> [!NOTE]
> <span data-ttu-id="2e4c7-105">請閱讀 [**您的圖形連接器文章設定**](configure-connector.md) ，以瞭解一般圖表連接器設定程式。</span><span class="sxs-lookup"><span data-stu-id="2e4c7-105">Read the [**Setup for your Graph connector**](configure-connector.md) article to understand the general Graph connectors setup process.</span></span>

## <a name="before-you-get-started"></a><span data-ttu-id="2e4c7-106">開始之前</span><span class="sxs-lookup"><span data-stu-id="2e4c7-106">Before you get started</span></span>

### <a name="install-the-graph-connector-agent"></a><span data-ttu-id="2e4c7-107">安裝圖形連接器代理程式</span><span class="sxs-lookup"><span data-stu-id="2e4c7-107">Install the Graph connector agent</span></span>

<span data-ttu-id="2e4c7-108">若要編制 Windows 檔案共用的索引，您必須安裝並註冊 Graph 連接器代理程式。</span><span class="sxs-lookup"><span data-stu-id="2e4c7-108">To index your Windows file shares, you must install and register the Graph connector agent.</span></span> <span data-ttu-id="2e4c7-109">請參閱 [安裝 Graph connector agent](on-prem-agent.md) 以深入瞭解。</span><span class="sxs-lookup"><span data-stu-id="2e4c7-109">See [Install the Graph connector agent](on-prem-agent.md) to learn more.</span></span>  

### <a name="content-requirements"></a><span data-ttu-id="2e4c7-110">內容需求</span><span class="sxs-lookup"><span data-stu-id="2e4c7-110">Content requirements</span></span>

### <a name="file-types"></a><span data-ttu-id="2e4c7-111">檔案類型</span><span class="sxs-lookup"><span data-stu-id="2e4c7-111">File types</span></span>

<span data-ttu-id="2e4c7-112">下列格式的內容可以編制索引及搜尋： DOC，.DOCM，.DOCX，點，DOTX，.EML，GIF，HTML，JPEG，.MHT，MHTML，MSG，NWS，OBD，OBT，ODP，ODS，ODT，ONE，PDF，.POT，PPS，PPTM，XLB，XLS，.XLSX，.XLT，.xlc，XML，XPS，和 ZIP。</span><span class="sxs-lookup"><span data-stu-id="2e4c7-112">Content of the following formats can be indexed and searched: DOC, DOCM, DOCX, DOT, DOTX, EML, GIF, HTML, JPEG, MHT, MHTML, MSG, NWS, OBD, OBT, ODP, ODS, ODT, ONE, PDF, POT, PPS, PPT, PPTM, PPTX, TXT, XLB, XLC, XLSB, XLS, XLSX, XLT, XLXM, XML, XPS, and ZIP.</span></span> <span data-ttu-id="2e4c7-113">只會為這些格式的文字內容編制索引。</span><span class="sxs-lookup"><span data-stu-id="2e4c7-113">Only the textual content of these formats is indexed.</span></span> <span data-ttu-id="2e4c7-114">會忽略所有多媒體內容。</span><span class="sxs-lookup"><span data-stu-id="2e4c7-114">All multimedia content is ignored.</span></span> <span data-ttu-id="2e4c7-115">針對任何不屬於此格式的檔案，會以單獨的中繼資料來編制索引。</span><span class="sxs-lookup"><span data-stu-id="2e4c7-115">For any file that doesn't belong to this format, the metadata alone is indexed.</span></span>

### <a name="file-size-limits"></a><span data-ttu-id="2e4c7-116">檔案大小限制</span><span class="sxs-lookup"><span data-stu-id="2e4c7-116">File size limits</span></span>

<span data-ttu-id="2e4c7-117">支援的檔案大小上限為 100 MB。</span><span class="sxs-lookup"><span data-stu-id="2e4c7-117">The maximum supported file size is 100 MB.</span></span> <span data-ttu-id="2e4c7-118">超過 100 MB 的檔案不會編制索引。</span><span class="sxs-lookup"><span data-stu-id="2e4c7-118">Files that exceed 100 MB aren't indexed.</span></span> <span data-ttu-id="2e4c7-119">後處理的最大大小限制為 4 MB。</span><span class="sxs-lookup"><span data-stu-id="2e4c7-119">The maximum post-processed size limit is 4 MB.</span></span> <span data-ttu-id="2e4c7-120">當檔案大小達到 4 MB 時，處理便會停止。</span><span class="sxs-lookup"><span data-stu-id="2e4c7-120">Processing stops when a file's size reaches 4 MB.</span></span> <span data-ttu-id="2e4c7-121">因此，檔案中所提供的某些片語可能無法用於搜尋。</span><span class="sxs-lookup"><span data-stu-id="2e4c7-121">Therefore, some phrases present in the file might not work for search.</span></span>

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a><span data-ttu-id="2e4c7-122">步驟1：在 Microsoft 365 系統管理中心新增圖表連接器</span><span class="sxs-lookup"><span data-stu-id="2e4c7-122">Step 1: Add a Graph connector in the Microsoft 365 admin center</span></span>

<span data-ttu-id="2e4c7-123">遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。</span><span class="sxs-lookup"><span data-stu-id="2e4c7-123">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-2-name-the-connection"></a><span data-ttu-id="2e4c7-124">步驟2：命名連線</span><span class="sxs-lookup"><span data-stu-id="2e4c7-124">Step 2: Name the connection</span></span>

<span data-ttu-id="2e4c7-125">遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。</span><span class="sxs-lookup"><span data-stu-id="2e4c7-125">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-3-configure-the-connection-settings"></a><span data-ttu-id="2e4c7-126">步驟3：設定連接設定</span><span class="sxs-lookup"><span data-stu-id="2e4c7-126">Step 3: Configure the connection settings</span></span>

<span data-ttu-id="2e4c7-127">在 [連線 **至資料來源]** 頁面上，選取 [檔案 **共用** ]，並提供名稱、連線識別碼及描述。</span><span class="sxs-lookup"><span data-stu-id="2e4c7-127">On the **Connect to data source** page, select **File share** and provide the name, connection ID, and description.</span></span> <span data-ttu-id="2e4c7-128">在下一個頁面上，提供檔案共用的路徑，然後選取您先前安裝的圖形連接器代理程式。</span><span class="sxs-lookup"><span data-stu-id="2e4c7-128">On the next page, provide the path to the file share and select your previously installed Graph connector agent.</span></span> <span data-ttu-id="2e4c7-129">輸入 [Microsoft Windows](https://microsoft.com/windows) 使用者帳戶的認證，該帳戶具有檔案共用中所有檔案的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="2e4c7-129">Enter the credentials for a [Microsoft Windows](https://microsoft.com/windows) user account with read access to all the files in the file share.</span></span>

### <a name="preserve-last-access-time"></a><span data-ttu-id="2e4c7-130">保留上次存取時間</span><span class="sxs-lookup"><span data-stu-id="2e4c7-130">Preserve last access time</span></span>

<span data-ttu-id="2e4c7-131">當連接器嘗試編目檔案時，會更新其中繼資料中的「最後存取時間」欄位。</span><span class="sxs-lookup"><span data-stu-id="2e4c7-131">When the connector attempts to crawl a file, the "last access time" field in its metadata is updated.</span></span> <span data-ttu-id="2e4c7-132">如果您依賴該欄位進行任何封存與備份解決方案，而且不想要在連接器存取時加以更新，您可以在 [ **高級設定** ] 頁面中設定此選項。</span><span class="sxs-lookup"><span data-stu-id="2e4c7-132">If you depend on that field for any archiving and backup solutions and doesn't want to update it when the connector accesses it, you can configure this option in the **Advanced settings** page.</span></span>

## <a name="step-4-manage-search-permissions"></a><span data-ttu-id="2e4c7-133">步驟4：管理搜尋許可權</span><span class="sxs-lookup"><span data-stu-id="2e4c7-133">Step 4: Manage search permissions</span></span>

<span data-ttu-id="2e4c7-134">您可以根據共用存取控制清單或新的技術檔案系統，限制搜尋任何檔案的許可權 (NTFS) 存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="2e4c7-134">You can restrict the permission to search for any file based on Share Access Control Lists or New Technology File System (NTFS) Access Control Lists.</span></span> <span data-ttu-id="2e4c7-135">如果您想要使用共用存取控制清單，請在 [ **高級設定** ] 頁面上選取適當的選項。</span><span class="sxs-lookup"><span data-stu-id="2e4c7-135">If you want to use Share Access Control Lists, select the appropriate option on the **Advanced settings** page.</span></span> <span data-ttu-id="2e4c7-136">如果您想要使用 NTFS 存取控制清單，請在 [ **管理搜尋許可權** ] 頁面上選取適當的選項。</span><span class="sxs-lookup"><span data-stu-id="2e4c7-136">If you want to use NTFS Access Control Lists, select the appropriate option on the **Manage search permissions** page.</span></span>

## <a name="step-5-assign-property-labels"></a><span data-ttu-id="2e4c7-137">步驟5：指派屬性標籤</span><span class="sxs-lookup"><span data-stu-id="2e4c7-137">Step 5: Assign property labels</span></span>

<span data-ttu-id="2e4c7-138">遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。</span><span class="sxs-lookup"><span data-stu-id="2e4c7-138">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-6-manage-schema"></a><span data-ttu-id="2e4c7-139">步驟6：管理架構</span><span class="sxs-lookup"><span data-stu-id="2e4c7-139">Step 6: Manage schema</span></span>

<span data-ttu-id="2e4c7-140">遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。</span><span class="sxs-lookup"><span data-stu-id="2e4c7-140">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-7-choose-refresh-settings"></a><span data-ttu-id="2e4c7-141">步驟7：選擇重新整理設定</span><span class="sxs-lookup"><span data-stu-id="2e4c7-141">Step 7: Choose refresh settings</span></span>

<span data-ttu-id="2e4c7-142">遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。</span><span class="sxs-lookup"><span data-stu-id="2e4c7-142">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-8-review-connection"></a><span data-ttu-id="2e4c7-143">步驟8：檢查連線</span><span class="sxs-lookup"><span data-stu-id="2e4c7-143">Step 8: Review connection</span></span>

<span data-ttu-id="2e4c7-144">遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。</span><span class="sxs-lookup"><span data-stu-id="2e4c7-144">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup 
instructions.-->

<!---## Troubleshooting-->
<!---Insert troubleshooting recommendations for this data source-->

<!---## Limitations-->
<!---Insert limitations for this data source-->
