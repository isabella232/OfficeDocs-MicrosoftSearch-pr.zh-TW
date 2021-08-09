---
title: 管理問與答
ms.author: jeffkizn
author: jeffkizn
manager: parulm
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: 7e3432e6-5317-4d63-90b0-52da6fddd343
description: 個別尋找及更新答案，或使用 Microsoft 搜尋工具&一次即可編輯 Q。
ms.openlocfilehash: 2e54169a6196ec78bd96b33aa1ba71fc498b6ff13d8d872ad06ca0db1d9fc2c0
ms.sourcegitcommit: 71ac2a38971ca4452d1bddfc773ff8f45e1ffd77
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/06/2021
ms.locfileid: "54532864"
---
# <a name="manage-qas"></a>管理問與答

建立問與答的方法與建立書籤類似。 Q&如可讓您回答使用者的問題，而不只是提供網頁連結。 您也可以在 rtf 文字中格式化答案。 如果書簽和 Q&共用相同的關鍵字，則會先顯示書簽結果。 如同書簽，Q&會在新增或變更 Q&A 之後立即重新整理索引。

## <a name="add-or-edit-a-single-qa"></a>新增或編輯單一問與答

1. 在 [Microsoft 365 系統管理中心](https://admin.microsoft.com)中，移至 [**Q&A**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/qnas)
1. 若要在中加入 Q&，請選取 [ **新增**]。
若要編輯問與答，請在相關的問與答清單中選取問與答。 當您新增或編輯資訊時，預覽會自動更新。
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

## <a name="add-or-edit-qas-using-browser-extensions"></a>使用瀏覽器延伸名新增或編輯 Q&

搜尋系統管理員可以使用瀏覽器擴充功能輕鬆地建立搜尋內容。 安裝瀏覽器延伸名，然後移至您要從中產生 Q&的網站。 然後，您可以建立 Q&，並包含來源網站的連結。

目前，瀏覽器擴充功能可用於 Microsoft Edge 和 Chrome。

- 若要下載 Edge 的分機 (舊版) ，請移至[Microsoft Store](https://www.microsoft.com/p/microsoft-search-content-creator/9nrqdbcbwq55?activetab=pivot:overviewtab)。
- 若要下載分機鑲邊或 Edge (Chromium) ，請移至[Chrome web store](https://chrome.google.com/webstore/detail/microsoft-search-content/nocnablpaoeecfmfnjoheefkogmleipm)。

## <a name="bulk-add-or-edit-qas"></a>大量新增或編輯問與答

系統管理員可以使用匯入及匯出功能，以大容量方式建立或編輯 Q&。

使用匯入/匯出功能可：

- 在 Q&範本檔中，大量新增 Q&以新增詳細資料，然後將其匯入。
- Bulk edit Q&出口 Q&為 .csv 檔案，請編輯 Q&匯出檔案中的詳細資料，然後匯入檔案。
- 將 Q&為-Export Q&改為 .csv 檔。

若要匯入或匯出 Q&如下：

1. 在 [問與答] 索引標籤的右上角，選取 [匯入]。
選取 [ **匯出** ]，以下載 .csv 檔案中的所有現有 Q&。
1. 在右窗格中，選取要使用 .csv 檔案匯入的選項。 下載範本檔案，以取得必要欄位及詳細資料的清單。
1. 新增或編輯 Q&範本檔中的詳細資料，然後將它儲存在您的電腦上。
1. 在 [ **Import Q&** 窗格中，選取 **[流覽]**，然後選取您要匯入的 .csv 檔案。
1. 選取 [匯入]。

重要的範本檔秘訣：

- 永不編輯這些欄位中的資料：**識別碼**、**上次修改日期**，以及 **上次修改者**
- 如果您包含現有書籤的 **識別碼**，將會以匯入檔案中的資訊加以取代。
- 如果現有的書簽具有相同的標題或 URL，則會使用匯入檔案中的資訊更新書簽。
- 並非範本檔案中的所有欄位都是必要的，必要的欄位也視書簽狀態而有所不同。
- 根據 [ **省/州** ] 欄位，書簽會儲存為 *草稿*、 *建議* 或 *排程*，或是自動發行。
- 針對管理多個組織的合作夥伴：您可以從一個組織匯出書簽，然後將其匯入另一個組織。 但您必須在匯入之前，先移除 [識別碼] 資料行中的資料。

> [!NOTE]
> 您無法匯入 Q&，如同範本檔案中有任何錯誤。 若要防止錯誤，請確定您的匯入檔案格式正確，並包含所有必要的資訊。

如需避免錯誤的詳細資訊，請參閱 [防止匯入錯誤](manage-bookmarks.md#prevent-import-errors)。
