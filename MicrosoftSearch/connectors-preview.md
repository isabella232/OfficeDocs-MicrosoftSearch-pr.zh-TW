---
title: 連接器預覽
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
description: 瞭解 microsoft 搜尋的 Microsoft Graph 連接器預覽。
ms.openlocfilehash: 4bcd8360957be69bc701e8b356cd222de32bfc5f
ms.sourcegitcommit: 64eea81f8c1db9ee955013462a7b51612fb7d0b7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/08/2020
ms.locfileid: "44604381"
---
# <a name="microsoft-graph-connectors-preview"></a>Microsoft Graph 連接器預覽

Microsoft Graph 連接器和 Microsoft Search APIs （查詢和索引）目前處於預覽狀態。 若要存取連接器功能，您必須在您的租使用者中開啟 [目標版本] 選項。 這是早期預覽，但沒有服務層級保證。 我們鼓勵客戶嘗試連接器功能並提供意見反應。 在預覽期間，我們不建議使用連接器進行生產用途。

## <a name="set-up-targeted-release"></a>設定目標版本

若要嘗試連接器，您必須為組織中的所有使用者設定 [**目標發行**選項]。 若要深入瞭解目標發行選項及設定方式，請參閱[在 Office 365 中設定標準或目標發行選項](https://docs.microsoft.com/office365/admin/manage/release-options-in-office-365?view=o365-worldwide)。

## <a name="choose-a-preview-environment"></a>選擇預覽環境

若要嘗試連接器、索引 APIs 和搜尋 APIs，我們建議這兩種方法：

1. **測試租**使用者。  我們鼓勵您使用測試租使用者來嘗試使用 Microsoft Graph 連接器預覽。

2. **測試網站集合**。 如果您沒有測試租使用者，您可以建立測試網站集合以嘗試使用連接器功能。 若要顯示連接器的結果，而不影響組織中任何其他位置的搜尋頁面，請自訂僅該網站集合的搜尋體驗。

## <a name="preview-limitations"></a>預覽限制

預覽版本有下列限制：

* 接收輸送量會限制每秒大約四個專案。

* 不支援架構更新。 建立連線設定後，就無法更新架構。 您只可刪除並重新建立連線。

* 已編制索引的內容只會顯示在自訂垂直的搜尋結果頁面中。 這種限制適用于具有自訂類型的內容。

* 您在預覽期間設定的任何連線，都可能需要刪除並重新建立。 如果這些連線與改進產品所做的變更不相容，這些連線將無法運作。

* 連接限制。 每個租使用者最多可以建立10個連接。

* 來源存放庫大小。 建議您預覽具有大約200000專案來源存放庫的連接器，因為這是我們經過測試的搜尋比例限制。 我們正在努力改進搜尋效能，而且我們預計會在不久的未來支援較大的存放庫大小。

* 無法使用 [編輯連線支援]。 建立連線後，就無法編輯或變更它。 如果您需要變更任何詳細資料，您必須刪除並重新建立連線。

* 僅能在自訂的縱向搜尋連接器內容。

* 每個自訂垂直中只會顯示一個連線的連接器內容，而且需要產生結果類型。
