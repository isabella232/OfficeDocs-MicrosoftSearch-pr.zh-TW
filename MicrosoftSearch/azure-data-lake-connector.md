---
title: Microsoft 搜尋的 Azure Data Lake connector
ms.author: monaray
author: monaray97
manager: jameslau
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 設定 Azure Data Lake Storage Gen2 connector for Microsoft Search
ms.openlocfilehash: 788b7106c15cd9773c86f46f91ba0e91e38028f3
ms.sourcegitcommit: 988c37610e71f9784b486660400aecaa7bed40b0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "47422926"
---
# <a name="azure-data-lake-storage-gen2-connector"></a>Azure Data Lake Storage Gen2 connector

透過 Azure Data Lake Storage Gen2 connector，您組織中的使用者可以搜尋 [Azure Blob 儲存區](https://docs.microsoft.com/azure/storage/blobs/storage-blobs-introduction) 和 [Azure Data Lake Gen 2 儲存體](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) 帳戶中儲存的檔案。

本文適用于 [Microsoft 365](https://www.microsoft.com/microsoft-365) 系統管理員或任何設定、執行及監視 Azure Data Lake Storage Gen2 connector 的人員。 它會提供連接器設定、功能、限制及疑難排解技巧的概述。 在本文中，我們使用 *Azure Storage* 做為 [Azure Blob 儲存區](https://docs.microsoft.com/azure/storage/blobs/storage-blobs-introduction) 和 [Azure Data Lake Gen 2 儲存區](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction)的一般字詞。

## <a name="connect-to-a-data-source"></a>連接到資料來源
### <a name="primary-storage-connection-string"></a>主要儲存連接字串 
在 [ **驗證] 和 [config** ] 畫面上，提供主要儲存連接字串。 該字串是允許存取您的儲存體帳戶所需的字串。 若要尋找您的連線字串，請移至 [Azure 入口網站](https://ms.portal.azure.com/#home) ，並流覽至相關 Azure 儲存體帳戶的 [機 **碼** ] 區段。 在螢幕上適當的欄位中複製並貼上連接字串。

如果您不想要提供 **AccountKey** (主要儲存連接字串中的參數) ，您必須授與我們的圖形連接器服務的讀取權限。 流覽至您的 Azure 儲存體帳戶的 [ **存取控制** ] 索引標籤，然後依照這裡的指示，將存取權授與下列應用程式：
* **第一方應用程式 ID:** 56c1da01-2129-48f7-9355-af6d59d42766
* **第一方應用程式名稱：** 圖形連接器服務

### <a name="storage-account-and-queue-notifications-optional"></a>儲存帳戶和佇列通知 (選用) 
可在未來新增圖表連接器服務中即時處理變更的支援。 在此情況下，我們會監視儲存在佇列中的 Azure 儲存體變更通知。 您必須使用與您的 Azure 儲存體帳戶相同的帳戶建立佇列。

建立佇列之後，請移至佇列頁面上的 [ **事件** ] 索引標籤，以設定 **事件訂閱**。 選擇佇列將要接收的所有 Blob 事件，並將該佇列連接至 Azure 儲存體帳戶。

## <a name="manage-the-search-schema"></a>管理搜尋結構描述
在 [**管理架構**] 畫面上，您可以選擇變更架構屬性 (與 managed 屬性相關**聯的可****查詢**、可搜尋及可**檢索**) 。 這些 managed 屬性屬性是從 Azure 資料儲存帳戶編制索引的資料。

## <a name="manage-search-permissions"></a>管理搜尋許可權
### <a name="azure-data-lake-gen-2"></a>Azure Data Lake Gen 2
在 [ **管理搜尋許可權** ] 畫面上，您可以選擇從您的 [Azure Data Lake Gen 2 儲存體](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) 帳戶中 (ACLs) 上插入存取控制清單。 當您設定這些搜尋許可權時，會根據指派給已登入之 [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/) 使用者搜尋內容的許可權來裁切搜尋內容。 或者，您也可以選擇讓組織中的所有人都可以看到從您的儲存體帳戶索引的所有內容。 在此情況下，您組織中的每個人都可以存取您儲存體帳戶中的所有資料。

### <a name="azure-blob-storage"></a>Azure Blob 儲存體
若要連線至 [Azure Blob 儲存](https://docs.microsoft.com/azure/storage/blobs/storage-blobs-introduction)，您組織中的所有人都會看到所有從設定之來源編制索引的內容。 Azure Blob 儲存區的 Blob 層級不支援存取控制清單。

## <a name="set-the-refresh-schedule"></a>設定重新整理排程
在 [重新整理 **設定** ] 畫面上，您可以設定增量編目間隔和完整編目間隔。 針對增量編目，Azure Data Lake Storage Gen2 connector 的預設間隔是15分鐘，完整編目則為一周。

## <a name="limitations"></a>限制
無法為 Azure Data Lake Storage Gen2 source 重新設定 Azure Blob 儲存的發佈連線，反之亦然。 在這種情況下，建議您設定新的連線。