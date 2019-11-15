---
title: 管理問與答
ms.author: anfowler
author: adefowler
manager: mnirkhe
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: 7e3432e6-5317-4d63-90b0-52da6fddd343
description: 個別尋找並更新解答，或使用 Microsoft Search 工具以一次編輯所有項目
ms.openlocfilehash: 903aab52e8d51e45588a390b5ccdccbaae2cf04a
ms.sourcegitcommit: 21361af7c244ffd6ff8689fd0ff0daa359bf4129
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/14/2019
ms.locfileid: "38626772"
---
# <a name="manage-qas"></a>管理問與答

建立問與答的方法與建立書籤類似。 問與答可讓您回應使用者的問題，而不只是提供網頁的連結。 您可以使用可用的工具，以 RTF 格式編寫答案。 如果書籤和問與答共用相同的關鍵字，則會先顯示書籤的結果。 如同書籤，問與答索引會在新增或變更問與答後立即重新整理。 

## <a name="add-or-edit-a-single-qa"></a>新增或編輯單一問與答
1. 移至 **Microsoft 365 系統管理中心**。
1. 在功能窗格中，移至 [設定]****，然後選取 **Microsoft Search**。
1. 選取 [問與答]**** 索引標籤。預設會選取第一個索引標籤 ([書籤]****)。
1. 若要新增問與答，請選取 [新增]****。
若要編輯問與答，請在相關的問與答清單中選取問與答。
1. 當您新增或編輯資訊時，預覽會自動更新。
1. 儲存變更。

### <a name="supported-html-tags"></a>支援的 HTML 標記
您可以使用現有的 HTML 內容或新增 HTML 標記至您的解答 (描述)。 會忽略不支援的標籤。  
支援下列的 HTML 標記：
- blockquote
- div
- em
- h1、h2、h3 和 h4
- ol、ul 和 li
- p
- pre
- span
- strong
- table、thead、tbody、tr、th 和 td
- u
- a
- code
- br
- hr
- img

## <a name="bulk-add-or-edit-qas"></a>大量新增或編輯問與答
系統管理員可以使用匯入和匯出功能來大量建立或編輯問與答。 當系統管理員需要新增或編輯大量問與答時，此功能很實用。 

使用匯入/匯出功能，以便：
1. 大量新增問與答 - 在問與答範本檔案中新增詳細資料，然後將它匯入。
1. 大量編輯問與答 - 將問與答匯出至 .csv 檔案，然後編輯匯出的 .csv 檔案中問與答的詳細資料，然後匯入該 .csv 檔案。
1. 備份問與答 - 匯出問與答至 .csv 檔案。

若要匯入或匯出問與答：
1. 在 [問與答] 索引標籤的右上角，選取 [匯入]****。 選取 [匯出]**** 來下載 .csv 檔案中所有的現有問與答。
1. 在右窗格中，選擇使用 .csv 檔案匯入的選項。
下載範本檔案以取得必要欄位的清單和詳細資料。 
1. 在範本檔案中新增或編輯問與答詳細資料，並將它儲存在您的電腦上。 
1. 在 [匯入問與答]**** 窗格中，選取 [瀏覽]****，然後選取您要匯入的 .csv 檔案。
1. 選取 [匯入]****。

以下是有關範本檔案的一些重點：
- 永不編輯這些欄位中的資料：*識別碼*、*上次修改日期*，以及*上次修改者*
- 如果您包含現有書籤的*識別碼*，將會以匯入檔案中的資訊加以取代。
- 如果有一個現有的書籤具有相同標題或 URL，則會以匯入檔案中的資訊更新書籤。
- 範本檔案中並非所有欄位都為必要，必要欄位則會依據書籤的狀態而改變。
- 書籤會根據狀態欄位的不同而儲存成草稿、建議、已排程或自動發佈。
- 適用於負責管理多個組織的合作夥伴，您可以從一個組織匯出您的書籤，並匯入另一個。 但您必須在匯入之前，先移除 [識別碼]** 資料行中的資料。

**附註：** 如果範本檔案中有任何錯誤，您即無法匯入問與答。 若要避免錯誤，請確定您匯入的檔案的格式正確，並包含所有必要的資訊。 

如需如何避免錯誤的詳細資訊，請參閱[防止匯入錯誤](manage-bookmarks.md#prevent-import-errors)。