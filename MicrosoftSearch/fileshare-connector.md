---
title: 檔共用連接器
ms.author: rusamai
author: rsamai
manager: jameslau
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 設定 Microsoft 搜尋的檔案共用連接器
ms.openlocfilehash: c11c407016315e638205adddddd17d90bbe6b33d
ms.sourcegitcommit: 59cdd3f0f82b7918399bf44d27d9891076090f4f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2020
ms.locfileid: "49367722"
---
# <a name="file-share-connector"></a><span data-ttu-id="7a840-103">檔共用連接器</span><span class="sxs-lookup"><span data-stu-id="7a840-103">File share connector</span></span>

<span data-ttu-id="7a840-104">透過檔案共用圖表連接器，您組織中的使用者便可搜尋內部部署 Windows 檔案共用。</span><span class="sxs-lookup"><span data-stu-id="7a840-104">With the File share Graph connector, users in your organization can search on-premise Windows file shares.</span></span>

<span data-ttu-id="7a840-105">本文適用于 Microsoft 365 系統管理員或任何設定、執行及監視檔案共用連接器的人員。</span><span class="sxs-lookup"><span data-stu-id="7a840-105">This article is for Microsoft 365 administrators or anyone who configures, runs, and monitors a file share connector.</span></span> <span data-ttu-id="7a840-106">它說明如何設定連接器和連接器功能、限制及疑難排解技術。</span><span class="sxs-lookup"><span data-stu-id="7a840-106">It explains how to configure your connector and connector capabilities, limitations, and troubleshooting techniques.</span></span>

## <a name="install-graph-connector-agent"></a><span data-ttu-id="7a840-107">安裝圖形連接器代理程式</span><span class="sxs-lookup"><span data-stu-id="7a840-107">Install Graph connector agent</span></span>

<span data-ttu-id="7a840-108">若要為 Windows 檔案共用編制索引，您必須安裝和註冊 [Graph 連接器代理程式](on-prem-agent.md) 軟體。</span><span class="sxs-lookup"><span data-stu-id="7a840-108">In order to index your Windows file shares, you must install and register [Graph connector agent](on-prem-agent.md) software.</span></span>

## <a name="content-requirements"></a><span data-ttu-id="7a840-109">內容需求</span><span class="sxs-lookup"><span data-stu-id="7a840-109">Content requirements</span></span>

### <a name="file-types"></a><span data-ttu-id="7a840-110">檔案類型</span><span class="sxs-lookup"><span data-stu-id="7a840-110">File types</span></span>

<span data-ttu-id="7a840-111">下列格式的內容可以編制索引及搜尋： DOC，.DOCM，.DOCX，點，DOTX，.EML，GIF，HTML，JPEG，.MHT，MHTML，MSG，NWS，OBD，OBT，ODP，ODS，ODT，ONE，PDF，.POT，PPS，PPTM，XLB，XLS，.XLSX，.XLT，.xlc，XML，XPS，和 ZIP。</span><span class="sxs-lookup"><span data-stu-id="7a840-111">Content of the following formats can be indexed and searched: DOC, DOCM, DOCX, DOT, DOTX, EML, GIF, HTML, JPEG, MHT, MHTML, MSG, NWS, OBD, OBT, ODP, ODS, ODT, ONE, PDF, POT, PPS, PPT, PPTM, PPTX, TXT, XLB, XLC, XLSB, XLS, XLSX, XLT, XLXM, XML, XPS, and ZIP.</span></span> <span data-ttu-id="7a840-112">只會為這些格式的文字內容編制索引。</span><span class="sxs-lookup"><span data-stu-id="7a840-112">Only the textual content of these formats is indexed.</span></span> <span data-ttu-id="7a840-113">會忽略所有多媒體內容。</span><span class="sxs-lookup"><span data-stu-id="7a840-113">All multimedia content is ignored.</span></span> <span data-ttu-id="7a840-114">針對不屬於此格式的任何檔案，會為獨立的中繼資料編制索引。</span><span class="sxs-lookup"><span data-stu-id="7a840-114">For any file that does not belong to this format, the metadata alone is indexed.</span></span>

### <a name="file-size-limits"></a><span data-ttu-id="7a840-115">檔案大小限制</span><span class="sxs-lookup"><span data-stu-id="7a840-115">File size limits</span></span>

<span data-ttu-id="7a840-116">支援的檔案大小上限為 100 MB。</span><span class="sxs-lookup"><span data-stu-id="7a840-116">The maximum supported file size is 100 MB.</span></span> <span data-ttu-id="7a840-117">超過 100 MB 的檔案不會編制索引。</span><span class="sxs-lookup"><span data-stu-id="7a840-117">Files that exceed 100 MB are not indexed.</span></span> <span data-ttu-id="7a840-118">後處理的最大大小限制為 4 MB。</span><span class="sxs-lookup"><span data-stu-id="7a840-118">The maximum post-processed size limit is 4 MB.</span></span> <span data-ttu-id="7a840-119">當檔案大小達到 4 MB 時，處理便會停止。</span><span class="sxs-lookup"><span data-stu-id="7a840-119">Processing stops when a file's size reaches 4 MB.</span></span> <span data-ttu-id="7a840-120">因此，檔案中所提供的某些片語可能無法用於搜尋。</span><span class="sxs-lookup"><span data-stu-id="7a840-120">Therefore, some phrases present in the file might not work for search.</span></span>

## <a name="connect-to-a-data-source"></a><span data-ttu-id="7a840-121">連接到資料來源</span><span class="sxs-lookup"><span data-stu-id="7a840-121">Connect to a data source</span></span>

<span data-ttu-id="7a840-122">在 [連線 **至資料來源]** 頁面上，選取 [檔案 **共用** ]，並提供名稱、連線識別碼及描述。</span><span class="sxs-lookup"><span data-stu-id="7a840-122">On the **Connect to data source** page, select **File share** and provide the name, connection ID, and description.</span></span> <span data-ttu-id="7a840-123">在下一個頁面上，提供檔案共用的路徑，然後選取您先前安裝的圖形連接器代理程式。</span><span class="sxs-lookup"><span data-stu-id="7a840-123">On the next page, provide the path to the file share and select your previously installed Graph connector agent.</span></span> <span data-ttu-id="7a840-124">輸入 [Microsoft Windows](https://microsoft.com/windows) 使用者帳戶的認證，該帳戶具有檔案共用中所有檔案的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="7a840-124">Enter the credentials for a [Microsoft Windows](https://microsoft.com/windows) user account with read access to all the files in the file share.</span></span>

## <a name="preserve-last-access-time"></a><span data-ttu-id="7a840-125">保留上次存取時間</span><span class="sxs-lookup"><span data-stu-id="7a840-125">Preserve last access time</span></span>

<span data-ttu-id="7a840-126">當連接器嘗試編目檔案時，會更新其中繼資料中的「最後存取時間」欄位。</span><span class="sxs-lookup"><span data-stu-id="7a840-126">When the connector attempts to crawl a file, the "last access time" field in its metadata is updated.</span></span> <span data-ttu-id="7a840-127">如果您依賴該欄位進行任何封存與備份解決方案，而且不想要在連接器存取時加以更新，您可以在 [ **高級設定** ] 頁面中設定此選項。</span><span class="sxs-lookup"><span data-stu-id="7a840-127">If you depend on that field for any archiving and backup solutions and do not want to update it when the connector accesses it, you can configure this option in the **Advanced settings** page.</span></span>

## <a name="manage-search-permissions"></a><span data-ttu-id="7a840-128">管理搜尋許可權</span><span class="sxs-lookup"><span data-stu-id="7a840-128">Manage search permissions</span></span>

<span data-ttu-id="7a840-129">您可以根據共用存取控制清單或新的技術檔案系統，限制搜尋任何檔案的許可權 (NTFS) 存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="7a840-129">You can restrict the permission to search for any file based on Share Access Control Lists or New Technology File System (NTFS) Access Control Lists.</span></span> <span data-ttu-id="7a840-130">如果您想要使用共用存取控制清單，請在 [ **高級設定** ] 頁面上選取適當的選項。</span><span class="sxs-lookup"><span data-stu-id="7a840-130">If you want to use Share Access Control Lists, select the appropriate option on the **Advanced settings** page.</span></span> <span data-ttu-id="7a840-131">如果您想要使用 NTFS 存取控制清單，請在 [ **管理搜尋許可權** ] 頁面上選取適當的選項。</span><span class="sxs-lookup"><span data-stu-id="7a840-131">If you want to use NTFS Access Control Lists, select the appropriate option on the **Manage search permissions** page.</span></span>

## <a name="assign-property-labels"></a><span data-ttu-id="7a840-132">指派屬性標籤</span><span class="sxs-lookup"><span data-stu-id="7a840-132">Assign property labels</span></span>

<span data-ttu-id="7a840-133">您可以從選項的功能表中選擇，將 source 屬性指派給每個標籤。</span><span class="sxs-lookup"><span data-stu-id="7a840-133">You can assign a source property to each label by choosing from a menu of options.</span></span> <span data-ttu-id="7a840-134">雖然這個步驟不是必要的，但具有一些屬性標籤會提升搜尋相關性，並可確保使用者更準確的搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="7a840-134">While this step is not mandatory, having some property labels will improve the search relevance and ensure more accurate search results for end users.</span></span>

## <a name="manage-schema"></a><span data-ttu-id="7a840-135">管理架構</span><span class="sxs-lookup"><span data-stu-id="7a840-135">Manage schema</span></span>

<span data-ttu-id="7a840-136">在 [**管理架構**] 畫面上，您可以選擇變更架構屬性 (可 **查詢**、**可搜尋、可\*\*\*\*檢索** 及 **可精簡搜尋**) 相關聯的屬性、新增選用的別名，然後選擇 **Content** 屬性。</span><span class="sxs-lookup"><span data-stu-id="7a840-136">On the **Manage Schema** screen, you have the option to change the schema attributes (**queryable**, **searchable**, **retrievable**, and **refinable**) associated with the properties, add optional aliases, and choose the **Content** property.</span></span>

## <a name="set-the-refresh-schedule"></a><span data-ttu-id="7a840-137">設定重新整理排程</span><span class="sxs-lookup"><span data-stu-id="7a840-137">Set the refresh schedule</span></span>

<span data-ttu-id="7a840-138">建議的預設重新整理排程間隔為15分鐘，但您可以根據喜好設定進行變更。</span><span class="sxs-lookup"><span data-stu-id="7a840-138">The recommended default refresh schedule interval is 15 minutes, but you can change it based on your preferences.</span></span>
