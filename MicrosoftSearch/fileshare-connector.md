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

# <a name="file-share-graph-connector"></a>檔案共用圖形連接器

檔案共用圖表連接器可讓組織中的使用者搜尋內部部署 Windows 檔案共用。

> [!NOTE]
> 請閱讀 [**您的圖形連接器文章設定**](configure-connector.md) ，以瞭解一般圖表連接器設定程式。

## <a name="before-you-get-started"></a>開始之前

### <a name="install-the-graph-connector-agent"></a>安裝圖形連接器代理程式

若要編制 Windows 檔案共用的索引，您必須安裝並註冊 Graph 連接器代理程式。 請參閱 [安裝 Graph connector agent](on-prem-agent.md) 以深入瞭解。  

### <a name="content-requirements"></a>內容需求

### <a name="file-types"></a>檔案類型

下列格式的內容可以編制索引及搜尋： DOC，.DOCM，.DOCX，點，DOTX，.EML，GIF，HTML，JPEG，.MHT，MHTML，MSG，NWS，OBD，OBT，ODP，ODS，ODT，ONE，PDF，.POT，PPS，PPTM，XLB，XLS，.XLSX，.XLT，.xlc，XML，XPS，和 ZIP。 只會為這些格式的文字內容編制索引。 會忽略所有多媒體內容。 針對任何不屬於此格式的檔案，會以單獨的中繼資料來編制索引。

### <a name="file-size-limits"></a>檔案大小限制

支援的檔案大小上限為 100 MB。 超過 100 MB 的檔案不會編制索引。 後處理的最大大小限制為 4 MB。 當檔案大小達到 4 MB 時，處理便會停止。 因此，檔案中所提供的某些片語可能無法用於搜尋。

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a>步驟1：在 Microsoft 365 系統管理中心新增圖表連接器

遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-2-name-the-connection"></a>步驟2：命名連線

遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-3-configure-the-connection-settings"></a>步驟3：設定連接設定

在 [連線 **至資料來源]** 頁面上，選取 [檔案 **共用** ]，並提供名稱、連線識別碼及描述。 在下一個頁面上，提供檔案共用的路徑，然後選取您先前安裝的圖形連接器代理程式。 輸入 [Microsoft Windows](https://microsoft.com/windows) 使用者帳戶的認證，該帳戶具有檔案共用中所有檔案的讀取權限。

### <a name="preserve-last-access-time"></a>保留上次存取時間

當連接器嘗試編目檔案時，會更新其中繼資料中的「最後存取時間」欄位。 如果您依賴該欄位進行任何封存與備份解決方案，而且不想要在連接器存取時加以更新，您可以在 [ **高級設定** ] 頁面中設定此選項。

## <a name="step-4-manage-search-permissions"></a>步驟4：管理搜尋許可權

您可以根據共用存取控制清單或新的技術檔案系統，限制搜尋任何檔案的許可權 (NTFS) 存取控制清單。 如果您想要使用共用存取控制清單，請在 [ **高級設定** ] 頁面上選取適當的選項。 如果您想要使用 NTFS 存取控制清單，請在 [ **管理搜尋許可權** ] 頁面上選取適當的選項。

## <a name="step-5-assign-property-labels"></a>步驟5：指派屬性標籤

遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-6-manage-schema"></a>步驟6：管理架構

遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-7-choose-refresh-settings"></a>步驟7：選擇重新整理設定

遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-8-review-connection"></a>步驟8：檢查連線

遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup 
instructions.-->

<!---## Troubleshooting-->
<!---Insert troubleshooting recommendations for this data source-->

<!---## Limitations-->
<!---Insert limitations for this data source-->
