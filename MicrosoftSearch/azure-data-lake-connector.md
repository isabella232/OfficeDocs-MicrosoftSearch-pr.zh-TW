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
# <a name="azure-data-lake-storage-gen2-connector-for-microsoft-search"></a>Microsoft Search 的 azure Data Lake 儲存 Gen2 連接器

使用[Azure Data Lake 儲存 Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction)連接器，您組織中的使用者可以搜尋的檔案和其內容。 此連接器存取儲存在 Azure Blob 容器和內 Azure Data Lake 儲存第 2 帳戶已啟用階層的資料夾中的資料。

本文適用於[Microsoft 365](https://www.microsoft.com/microsoft-365)系統管理員或人設定、 執行，並監視 Azure Data Lake 儲存 Gen2 連接器。 本文說明如何設定連接器，連接器功能、 限制和疑難排解技巧。

## <a name="connect-to-a-data-source"></a>連線至資料來源

### <a name="primary-storage-connection-string"></a>主要儲存區的連接字串 
在 [**驗證設定**] 畫面中，提供主要存放裝置連接字串。 若要允許您儲存體帳戶的存取權，才該字串。 若要尋找您的連接字串，請移至[Azure 入口網站](https://ms.portal.azure.com/#home)，並瀏覽至 [**機碼**] 區段中的[Azure Data Lake 儲存 Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction)帳戶。 複製並貼在螢幕上適當的欄位中的連接字串。

如果您不想要提供**AccountKey** （主要儲存區連接字串中的參數），您必須授與我們圖的連接器服務的讀取權限。 在您的 Azure Data Lake 儲存 Gen2 帳戶的 [**存取控制**] 索引標籤中，依照指示，授與存取權的下列應用程式] 頁面上：
* **第一方應用程式識別碼：** 56c1da01-2129-48f7-9355-af6d59d42766
* **第一方應用程式名稱：** Graph 連接器服務

### <a name="storage-account-and-queue-notifications-optional"></a>儲存體帳戶和佇列通知 （選用）
支援，以處理即時圖表連接器服務中的變更可能在未來新增。 在此情況下，我們將會監視儲存在佇列中的[Azure Data Lake 儲存 Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction)變更通知。 您需要您 Azure Data Lake 儲存 Gen2 相同的帳戶或另一個儲存體帳戶中建立佇列。

建立佇列之後，移至 [**事件**] 索引標籤上 [佇列] 頁面上，若要設定**事件訂閱**。 選擇 [所有 Blob 事件佇列將會接收，並將佇列連線到 Azure Data Lake 儲存 Gen2 帳戶]。

## <a name="manage-the-search-schema"></a>管理搜尋結構描述
**管理結構描述**在畫面上，您可以選擇變更的結構描述屬性 (**設為可查詢**、**可搜尋**，並**可擷取**) 相關聯的 managed 屬性。 這些 managed 的屬性的屬性是從您的[Azure Data Lake 儲存 Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction)帳戶編製索引的資料。

## <a name="manage-search-permissions"></a>管理搜尋的權限
在 [**管理搜尋的權限**] 畫面中，您可以選擇內嵌的存取控制清單 (Acl) 從您的儲存體帳戶。 當這些搜尋權限設定時，搜尋內容修剪根據指派給登入[Azure Active Directory](https://docs.microsoft.com/azure/active-directory/)使用者搜尋內容的權限。 或者，您可以選擇要從組織中的每個人都可以看到您儲存體帳戶編製索引的所有內容。 在此情況下，您的組織中的每個人儲存體帳戶中有存取權的所有資料。
 
## <a name="set-the-refresh-schedule"></a>設定重新整理排程
在 [**重新整理設定**] 畫面中，您可以設定的累加編目間隔及完整編目間隔。 [Azure Data Lake 儲存 Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction)連接器的預設間隔為 15 分鐘，進行累加編目和一週進行完整編目。
 
## <a name="limitations"></a>限制
目前， [Azure Data Lake 儲存 Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction)多重通訊協定存取只能在中央美國、 西中央美國、 加拿大中央、 美國東部、 東亞、 北歐、 東亞 US2、 東南亞、 西歐、 美國西部、 澳洲東亞、 日本東、 西 US2 和巴西南是可用。

更新與詳細資訊，請參閱[在 Azure Data Lake 儲存體 （預覽） 上存取的多重通訊協定](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-multi-protocol-access)。


