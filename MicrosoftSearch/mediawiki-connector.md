---
title: Microsoft 搜尋的 MediaWiki 連接器
ms.author: monaray
author: monaray97
manager: mnirkhe
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 設定 Microsoft 搜尋的 MediaWiki 連接器
ms.openlocfilehash: 7a22fcc84f6f435bf438aa027c42c76eb8be1eaf
ms.sourcegitcommit: 39bf9f0db7f9bff2ab82c99a059b0ddcf1c98f5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/19/2021
ms.locfileid: "49905948"
---
# <a name="mediawiki-connector"></a>MediaWiki 連接器

透過 MediaWiki 連接器，您的組織可以從使用 MediaWiki 軟體所建立的 wiki 探索和編制資料。 此連接器會將指定的內容索引至 Microsoft 搜尋中，並支援定期編目，使索引保持在最新狀態。

本文適用于 Microsoft 365 系統管理員或任何設定、執行及監視 MediaWiki Graph 連接器的人員。 它會補充 [設定圖形連接器](configure-connector.md) 文章中所提供的一般指示。 若尚未這麼做，請閱讀整個設定圖形連接器文章，以瞭解一般的設定程式。

安裝程式中的每個步驟都會列在下表中，也就是指出應該遵循一般設定指示或僅適用于 MediaWiki Graph 連接器的其他指示。 本文也包含 MediaWiki 圖形連接器 [限制](#limitations) 的相關資訊。 

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a>步驟1：在 Microsoft 365 系統管理中心新增圖形連接器。
遵循一般設定指示。

## <a name="step-2-name-the-connection"></a>步驟2：命名連線。
遵循一般設定指示。
 
## <a name="step-3-configure-the-connection-settings"></a>步驟3：設定連接設定。
輸入您的 **WIKI URL** ，然後從下拉式功能表的 [選項] 功能表中選擇 **驗證類型** 。 選項為 **None**、 **Basic** 及 **OAuth 2.0 AAD**。

如果您選擇 [ **基本** ] 做為驗證類型，您將需要提供 wiki 的使用者 **名稱** 和 **密碼** 。

如果您選擇 **OAuth 2.0 AAD** 作為驗證類型，您將需要提供 wiki 安裝的 **資源識別碼** 。 您也需要提供在 AAD 應用程式註冊頁面上產生的 **用戶端識別碼** 和 **用戶端密碼** 。 

## <a name="step-4-manage-search-permissions"></a>步驟4：管理搜尋許可權
MediaWiki 連接器只支援 **所有人都** 能看見的搜尋許可權。 已編制索引的資料會顯示在搜尋結果中，並對組織中的所有使用者顯示。

## <a name="step-5-assign-property-labels"></a>步驟5：指派屬性標籤
遵循一般設定指示。

## <a name="step-6-manage-schema"></a>步驟6：管理架構
遵循一般設定指示。

## <a name="step-7-choose-refresh-settings"></a>步驟7：選擇重新整理設定
遵循一般設定指示。

## <a name="step-8-review-connection"></a>步驟8：檢查連線
遵循一般設定指示。

<!---## Troubleshooting-->
<!---To be added-->

## <a name="limitations"></a>限制
MediaWiki 連接器在預覽版本中有下列限制：

* 僅支援雲端型 wiki。
* 使用 Azure Active Directory 或 Azure 驗證，僅支援 Basic 或 OAuth 2.0。
* 不支援索引的命名空間選取。 僅索引主要、類別和檔案命名空間。
* 不支援 (ACLs) 的存取控制清單。 因此，組織中的所有使用者都能看到索引頁面。
