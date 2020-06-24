---
title: Microsoft 搜尋的 Azure Data Lake connector
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
description: 設定 Azure Data Lake Storage Gen2 connector for Microsoft Search
ms.openlocfilehash: f8cb94e806e619d6dae7258b6c2d708d93afb9a8
ms.sourcegitcommit: 7eda9b621def0659d7e7bc8b989f8adc929cce93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2020
ms.locfileid: "44861074"
---
# <a name="azure-data-lake-storage-gen2-connector"></a>Azure Data Lake Storage Gen2 connector

透過[Azure Data Lake Storage Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) connector，您組織中的使用者便可搜尋檔案及其內容。 此連接器會存取 Azure Data Lake Storage Gen 2 帳戶內，Azure Blob 容器和已啟用階層的資料夾中儲存的資料。

本文適用于[Microsoft 365](https://www.microsoft.com/microsoft-365)系統管理員或任何設定、執行及監視 Azure Data Lake Storage Gen2 connector 的人員。 它說明如何設定連接器和連接器功能、限制及疑難排解技術。

## <a name="connect-to-a-data-source"></a>連接到資料來源

### <a name="primary-storage-connection-string"></a>主要儲存連接字串 
在 [**驗證] 和 [config** ] 畫面上，提供主要儲存連接字串。 該字串是允許存取您的儲存體帳戶所需的字串。 若要尋找您的連線字串，請移至[azure 入口網站](https://ms.portal.azure.com/#home)，並流覽至[Azure Data Lake Storage Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction)帳戶的 [機**碼**] 區段。 在螢幕上適當的欄位中複製並貼上連接字串。

如果您不想要提供**AccountKey** （主要儲存連接字串中的參數），您必須授與我們的圖形連接器服務的讀取權限。 在您 Azure Data Lake Storage Gen2 帳戶的 [**存取控制**] 索引標籤中，依照該頁面上的指示，將存取權授與下列應用程式：
* **第一方應用程式 ID:** 56c1da01-2129-48f7-9355-af6d59d42766
* **第一方應用程式名稱：** 圖形連接器服務

### <a name="storage-account-and-queue-notifications-optional"></a>儲存帳戶和佇列通知（選用）
可在未來新增圖表連接器服務中即時處理變更的支援。 在這種情況下，我們會監視[Azure Data Lake Storage Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) change 通知儲存在佇列中。 您必須使用與您的 Azure Data Lake Storage Gen2 或其他儲存體帳戶相同的帳戶建立佇列。

建立佇列之後，請移至佇列頁面上的 [**事件**] 索引標籤，以設定**事件訂閱**。 選擇佇列將要接收的所有 Blob 事件，並將該佇列連接至 Azure Data Lake Storage Gen2 帳戶。

## <a name="manage-the-search-schema"></a>管理搜尋結構描述
在 [**管理架構**] 畫面上，您可以選擇變更與 managed 屬性相關聯的架構屬性（可**查詢** **、可**搜尋及可**檢索**）。 這些 managed 屬性屬性是從[Azure Data Lake Storage Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction)帳戶編制索引的資料。

## <a name="manage-search-permissions"></a>管理搜尋許可權
在 [**管理搜尋許可權**] 畫面上，您可以選擇從您的儲存體帳戶中攝取存取控制清單（ACLs）。 當您設定這些搜尋許可權時，會根據指派給已登入之[Azure Active Directory](https://docs.microsoft.com/azure/active-directory/)使用者搜尋內容的許可權來裁切搜尋內容。 或者，您也可以選擇讓組織中的所有人都可以看到從您的儲存體帳戶索引的所有內容。 在此情況下，您組織中的每個人都可以存取您儲存體帳戶中的所有資料。
 
## <a name="set-the-refresh-schedule"></a>設定重新整理排程
在 [重新整理**設定**] 畫面上，您可以設定增量編目間隔和完整編目間隔。 針對增量編目， [Azure Data Lake Storage Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) connector 的預設間隔是15分鐘，完整編目則為一周。
 
## <a name="limitations"></a>限制
目前， [Azure Data Lake Storage Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction)多通訊協定存取只適用于美國中西部、West Us、加拿大中央、東 Us、東亞、北歐、東 US2、東南亞、西亞、西 US2 和巴西南部等的地區。

如需更新及詳細資訊，請參閱[在 Azure Data Lake Storage （預覽）上的多協定存取](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-multi-protocol-access)。


