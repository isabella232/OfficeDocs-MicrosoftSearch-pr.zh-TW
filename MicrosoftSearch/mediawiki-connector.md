---
title: MediaWiki Graph connector Microsoft 搜尋
ms.author: mecampos
author: mecampos
manager: umas
audience: Admin
ms.audience: Admin
ms.topic: article
ms.service: mssearch
ms.localizationpriority: medium
search.appverid:
- BFB160
- MET150
- MOE150
description: 設定 Microsoft 搜尋的 MediaWiki Graph 連接器
ms.openlocfilehash: 7e1c308eb1785dd7fec23fac7e9002957a0d50ca
ms.sourcegitcommit: ca5ee826ba4f4bb9b9baabc9ae8a130011c2a3d0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/15/2021
ms.locfileid: "59375825"
---
<!---Previous ms.author: monaray --->

# <a name="mediawiki-graph-connector"></a>MediaWiki Graph 連接器

MediaWiki Graph connector 可讓您的組織從使用 MediaWiki 軟體所建立的 wiki 探索和編制索引資料。 此連接器會將指定的內容索引至 Microsoft 搜尋，並支援定期編目，使索引保持最新狀態。

> [!NOTE]
> 請閱讀 [**Graph 連接器**](configure-connector.md)文章的設定，以瞭解一般 Graph 連接器設定指示。

本文適用于設定、執行及監視 MediaWiki Graph 連接器的任何人。 它會補充一般設定程式，並顯示只適用于 MediaWiki Graph 連接器的指示。 本文也包含 [限制](#limitations)的相關資訊。

<!---## Before you get started-->

<!---Insert "Before you get started" recommendations for this data source-->

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a>步驟1：在 Microsoft 365 系統管理中心中新增 Graph 連接器

遵循一般 [設定指示](./configure-connector.md)。
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-2-name-the-connection"></a>步驟2：命名連線

遵循一般 [設定指示](./configure-connector.md)。
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-3-configure-the-connection-settings"></a>步驟3：設定連接設定

輸入您的 **WIKI URL** ，然後從下拉式功能表的 [選項] 功能表中選擇 **驗證類型** 。 選項為 **None**、 **Basic** 及 **OAuth 2.0 AAD**。

如果您選擇 [ **基本** ] 做為驗證類型，您將需要提供 wiki 的使用者 **名稱** 和 **密碼** 。

如果您選擇 **OAuth 2.0 AAD** 作為驗證類型，您將需要提供 wiki 安裝的 **資源識別碼** 。 您也需要提供在 AAD 應用程式註冊頁面上產生的 **用戶端識別碼** 和 **用戶端密碼** 。

## <a name="step-4-manage-search-permissions"></a>步驟4：管理搜尋許可權

MediaWiki 連接器只支援 **所有人都** 能看見的搜尋許可權。 已編制索引的資料會顯示在搜尋結果中，並對組織中的所有使用者顯示。

## <a name="step-5-assign-property-labels"></a>步驟5：指派屬性標籤

遵循一般 [設定指示](./configure-connector.md)。
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-6-manage-schema"></a>步驟6：管理架構

遵循一般 [設定指示](./configure-connector.md)。
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-7-choose-refresh-settings"></a>步驟7：選擇重新整理設定

遵循一般 [設定指示](./configure-connector.md)。
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-8-review-connection"></a>步驟8：檢查連線

遵循一般 [設定指示](./configure-connector.md)。
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

<!---## Troubleshooting-->
<!---To be added-->

## <a name="limitations"></a>限制

MediaWiki 連接器在預覽版本中有下列限制：

* 僅支援雲端型 wiki。
* 使用 Azure Active Directory 或 Azure 驗證，僅支援 Basic 或 OAuth 2.0。
* 不支援索引的命名空間選取。 僅索引主要、類別和檔案命名空間。
* 不支援 (ACLs) 的存取控制清單。 因此，組織中的所有使用者都能看到索引頁面。