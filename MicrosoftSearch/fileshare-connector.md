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
ROBOTS: NoIndex
description: 設定 Microsoft 搜尋的檔案共用連接器
ms.openlocfilehash: a95cfe90ca35a385bb9ce3a4c565c18c5a42ec80
ms.sourcegitcommit: 69a1c544cc8db364991cb58d7818d7158ff108b8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/25/2020
ms.locfileid: "49408931"
---
# <a name="file-share-connector"></a>檔共用連接器

透過檔案共用圖表連接器，您組織中的使用者便可搜尋內部部署 Windows 檔案共用。

本文適用于 Microsoft 365 系統管理員或任何設定、執行及監視檔案共用連接器的人員。 它說明如何設定連接器和連接器功能、限制及疑難排解技術。

## <a name="install-graph-connector-agent"></a>安裝圖形連接器代理程式

若要為 Windows 檔案共用編制索引，您必須安裝和註冊 [Graph 連接器代理程式](on-prem-agent.md) 軟體。

## <a name="content-requirements"></a>內容需求

### <a name="file-types"></a>檔案類型

下列格式的內容可以編制索引及搜尋： DOC，.DOCM，.DOCX，點，DOTX，.EML，GIF，HTML，JPEG，.MHT，MHTML，MSG，NWS，OBD，OBT，ODP，ODS，ODT，ONE，PDF，.POT，PPS，PPTM，XLB，XLS，.XLSX，.XLT，.xlc，XML，XPS，和 ZIP。 只會為這些格式的文字內容編制索引。 會忽略所有多媒體內容。 針對不屬於此格式的任何檔案，會為獨立的中繼資料編制索引。

### <a name="file-size-limits"></a>檔案大小限制

支援的檔案大小上限為 100 MB。 超過 100 MB 的檔案不會編制索引。 後處理的最大大小限制為 4 MB。 當檔案大小達到 4 MB 時，處理便會停止。 因此，檔案中所提供的某些片語可能無法用於搜尋。

## <a name="connect-to-a-data-source"></a>連接到資料來源

在 [連線 **至資料來源]** 頁面上，選取 [檔案 **共用** ]，並提供名稱、連線識別碼及描述。 在下一個頁面上，提供檔案共用的路徑，然後選取您先前安裝的圖形連接器代理程式。 輸入 [Microsoft Windows](https://microsoft.com/windows) 使用者帳戶的認證，該帳戶具有檔案共用中所有檔案的讀取權限。

## <a name="preserve-last-access-time"></a>保留上次存取時間

當連接器嘗試編目檔案時，會更新其中繼資料中的「最後存取時間」欄位。 如果您依賴該欄位進行任何封存與備份解決方案，而且不想要在連接器存取時加以更新，您可以在 [ **高級設定** ] 頁面中設定此選項。

## <a name="manage-search-permissions"></a>管理搜尋許可權

您可以根據共用存取控制清單或新的技術檔案系統，限制搜尋任何檔案的許可權 (NTFS) 存取控制清單。 如果您想要使用共用存取控制清單，請在 [ **高級設定** ] 頁面上選取適當的選項。 如果您想要使用 NTFS 存取控制清單，請在 [ **管理搜尋許可權** ] 頁面上選取適當的選項。

## <a name="assign-property-labels"></a>指派屬性標籤

您可以從選項的功能表中選擇，將 source 屬性指派給每個標籤。 雖然這個步驟不是必要的，但具有一些屬性標籤會提升搜尋相關性，並可確保使用者更準確的搜尋結果。

## <a name="manage-schema"></a>管理架構

在 [**管理架構**] 畫面上，您可以選擇變更架構屬性 (可 **查詢**、**可搜尋、可****檢索** 及 **可精簡搜尋**) 相關聯的屬性、新增選用的別名，然後選擇 **Content** 屬性。

## <a name="set-the-refresh-schedule"></a>設定重新整理排程

建議的預設重新整理排程間隔為15分鐘，但您可以根據喜好設定進行變更。
