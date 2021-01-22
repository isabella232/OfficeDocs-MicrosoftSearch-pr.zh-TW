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
# <a name="azure-data-lake-storage-gen2-connector"></a>Azure Data Lake Storage Gen2 連接器

使用 Azure Data Lake Storage Gen2 連接器，貴組織的使用者可以搜尋儲存在 [Azure Blob](https://docs.microsoft.com/azure/storage/blobs/storage-blobs-introduction) 儲存體和 [Azure Data Lake Gen 2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) 儲存體帳戶中的檔案。

本文適用于 [Microsoft 365](https://www.microsoft.com/microsoft-365) 系統管理員，或任何設定、執行及監控 Azure Data Lake Storage Gen2 連接器的人。 它提供連接器組配置、功能、限制和疑難排解技巧概觀。 在本文中，我們使用 *Azure 儲存體* 做為 [Azure Blob](https://docs.microsoft.com/azure/storage/blobs/storage-blobs-introduction) 儲存體和 [Azure Data Lake Gen 2 儲存體的通用術語](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction)。

## <a name="connect-to-a-data-source"></a>連接到資料來源

### <a name="primary-storage-connection-string"></a>主要儲存空間連接字串

在驗證 **與設定檔畫面上** ，提供主要儲存空間連接字串。 需要該字串才能存取儲存空間帳戶。 若要尋找您的連接字串，請前往 [Azure 入口](https://ms.portal.azure.com/#home) 網站，然後流覽至相關 Azure 儲存體 **帳戶的金鑰** 區段。 在畫面上的適當欄位中複製並貼上連接字串。

如果您不想在主要儲存連接字串 (中提供 **AccountKey**) 參數，您必須為下列角色授予圖形連接器服務的存取權。  (只支援階層式儲存功能。 傳統的 Blob 儲存體必須提供 AccountKey.) 
* 儲存體 Blob 資料讀取程式
* 儲存佇列資料參與者
* 儲存體 Blob Delegator

流覽至 **Azure 儲存體** 帳戶的 Access Control Tab，並遵循指示以授予下列應用程式的存取權：

* **第一方應用程式識別碼** ：56c1da01-2129-48f7-9355-af6d59d42766
* **第一方應用程式名稱：** 圖形連接器服務

### <a name="storage-account-and-queue-notifications-optional"></a>儲存空間帳戶和佇列通知 (選填) 

未來可能會新增圖形連接器服務中即時處理變更的支援。 在這種情況下，我們會監視儲存在佇列中的 Azure 儲存體變更通知。 您必須在 Azure 儲存體帳戶的同一個帳戶中建立佇列。

建立佇列之後，請前往佇列頁面上的事件分頁以設定 **事件訂閱**。 選擇佇列將接收的所有 Blob 事件，將佇列連接到 Azure 儲存體帳戶。

## <a name="manage-search-permissions"></a>管理搜尋許可權

### <a name="azure-data-lake-gen-2"></a>Azure Data Lake Gen 2

在管理 **搜尋** 許可權畫面上，您可以選擇從 [Azure Data Lake Gen 2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) 儲存體帳戶 (存取控制清單) URL 清單。 設定這些搜尋許可權時，搜尋內容會根據指派給已簽署 [之 Azure Active Directory](https://docs.microsoft.com/azure/active-directory/) 使用者搜尋內容的許可權進行修剪。 或者，您可以選擇讓貴組織中所有人看到您儲存帳戶中所有已編制索引的內容。 在這種情況下，貴組織全體人員將能存取您儲存空間帳戶中的所有資料。

### <a name="azure-blob-storage"></a>Azure Blob 儲存體

若要與 [Azure Blob 儲存體](https://docs.microsoft.com/azure/storage/blobs/storage-blobs-introduction)建立連結，貴組織中所有人都能看到從已配置來源建立索引的所有內容。 Azure Blob 儲存體中的 Blob 層級不支援存取控制清單。

## <a name="search-permissions"></a>搜尋許可權

Azure Data Lake Storage Gen2 連接器支援對所有人可見 **或** 只有擁有此 **資料來源存取權的人所看見的搜尋許可權**。 組織所有使用者或只有具有每個專案存取權的使用者，才能看到出現在搜尋結果中的索引資料。

## <a name="assign-property-labels"></a>指派屬性標籤

您可以選擇選項功能表，為每個標籤指定來源屬性。 雖然這不是強制步驟，但擁有一些屬性標籤將能改善搜尋相關性，並確保使用者獲得更精確的搜尋結果。

## <a name="manage-schema"></a>管理架構

在管理架構畫面上，您可以選擇變更與屬性關聯的架構屬性 (可查詢、可搜尋、可取及可精簡 **) 、** 新增選擇性別名，然後選擇 **內容** 屬性。

## <a name="set-the-refresh-schedule"></a>設定重新更新排程

在重新 **整點設定** 畫面上，您可以設定遞增編編間隔和完整編編間隔。 Azure Data Lake Storage Gen2 連接器的預設間隔為 15 分鐘，用於進行增量爬網，以及一周進行完整爬網。

## <a name="limitations"></a>限制

無法重新針對 Azure Data Lake Storage Gen2 來源重新建立 Azure Blob 儲存體的已發佈連接，反之亦然。 在這種情況下，建議您設定新連接。
