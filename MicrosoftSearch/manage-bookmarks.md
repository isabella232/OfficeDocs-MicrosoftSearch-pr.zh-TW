---
title: 管理書籤
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
ms.assetid: c0c814d0-f7e4-444e-b18e-09beb45c9322
description: 建立和更新用來大量編輯 Microsoft 搜尋書簽結果的書簽和方式
ms.openlocfilehash: 2c0b42e4be1307aa45e4cab3f5c923a7808375e4
ms.sourcegitcommit: 988c37610e71f9784b486660400aecaa7bed40b0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "47422872"
---
# <a name="manage-bookmarks"></a>管理書籤

只要幾個步驟，您便可以建立書籤。 每個書籤都包括標題、URL，和一組能觸發書籤的關鍵字。 您也可以將類別新增至可用於管理入口網站之排序和篩選的書簽。 一個書籤可以有多個關鍵字，數個書籤可以共用相同的關鍵字，但不能共用保留的關鍵字。 建立或修改書籤時，搜尋索引會立即重新整理，且書籤會立即可供使用者使用。

如果您的組織已在 SharePoint 中提升結果，您可以將升級後的結果匯入 **Microsoft 搜尋** 中，並讓您的使用者可以使用匯入的內容。 這是一種簡單的方法，可在您設定 **Microsoft 搜尋** 後快速填入搜尋結果，並讓使用者更有效率。 建議您使用來自 SharePoint 提升的結果做為參考，以了解如何指定和建立相關的搜尋結果。

## <a name="add-or-edit-a-single-bookmark"></a>新增或編輯單一書籤

1. 在 [Microsoft 365 系統管理中心](https://admin.microsoft.com)中，移至 [ [**書簽**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/bookmarks)]。
1. 若要新增書簽，請選取 [ **新增**]。
若要編輯書籤，請在相關的書籤清單中選取書籤。
1. 當您新增或編輯資訊時，預覽會自動更新。
1. 儲存變更。

## <a name="add-or-edit-bookmark-using-browser-extensions"></a>使用瀏覽器擴充功能來新增或編輯書籤

搜尋系統管理員可以使用瀏覽器擴充功能輕鬆地建立搜尋內容。 安裝瀏覽器擴充功能模組，然後移至您要新增為書籤的網站，並將網站新增為書籤。

目前提供 Edge 和 Chrome 的瀏覽器擴充功能。

- 若要下載 Edge extensions，請移至 [Microsoft Store](https://www.microsoft.com/p/microsoft-search-content-creator/9nrqdbcbwq55?activetab=pivot:overviewtab) 並下載應用程式。
- 若要下載 Chrome extensions，請移至 [chrome web store](https://chrome.google.com/webstore/detail/microsoft-search-content/nocnablpaoeecfmfnjoheefkogmleipm) 並下載應用程式。

## <a name="bulk-add-or-edit-bookmarks"></a>大量新增或編輯書籤

搜尋系統管理員可以使用匯入或匯出功能來大量建立或編輯書籤。 當系統管理員想要新增或編輯大量書籤時，此功能非常實用。

使用匯入/匯出功能，以便：

- 大量新增書籤 - 在書籤範本檔案中新增詳細資料，然後將它匯入。
- 大量編輯書籤 - 將書籤匯出至 .csv 檔案，然後編輯匯出的 .csv 檔案中書籤的詳細資料，然後匯入更新的 .csv 檔案。
- 從 SharePoint 匯入升級的網站。
- 備份書籤 - 將書籤匯出至 .csv 檔案。

若要匯入或匯出書籤：

1. 在 [書籤]**** 索引標籤的右上角，選取 [匯入]****。
選取 [匯出]**** 來下載 .csv 檔案中所有的現有書籤。
1. 在右窗格中，選擇使用 .csv 檔案或從 SharePoint 匯入的選項。
下載範本檔案以取得必要欄位的清單和詳細資料。
1. 在範本檔案中新增或編輯書籤詳細資料，然後將它儲存在您的電腦上。
1. 在 [匯入書籤]**** 窗格中，選取 [瀏覽]****，然後選取您要匯入的 .csv 檔案。
1. 選取 [匯入]****。

以下是有關範本檔案要注意的一些重點：

- 永不編輯這些欄位中的資料：*識別碼*、*上次修改日期*，以及*上次修改者*
- 如果您包含現有書籤的*識別碼*，將會以匯入檔案中的資訊加以取代。
- 如果有一個現有的書籤具有相同標題或 URL，則會以匯入檔案中的資訊更新書籤。
- 範本檔案中並非所有欄位都為必要，必要欄位則會依據書籤的狀態而改變。
- 書籤會根據 [狀態]** 欄位的不同而儲存成草稿、建議、已排程或自動發佈。
- 針對管理多個組織的合作夥伴，您可以從一個組織匯出書簽，然後將其匯入另一個組織。 但您必須在匯入之前，先移除 [識別碼]** 資料行中的資料。

### <a name="prevent-import-errors"></a>防止匯入錯誤

如果任何必要資料遺漏或無效，您會收到錯誤訊息，並且會產生記錄檔，其中包含要修正的資料列和資料行的詳細資訊。 進行所需編輯，然後再次嘗試匯入檔案。 在解決所有問題之前，您無法匯入或儲存任何書籤。

若要避免錯誤，請確定您匯入的檔案的格式正確，並且：

- 包含匯入範本中的標題列和所有資料行
- 資料行順序與匯入範本相同
- 所有資料行都有值，除了可以是空白的這三個以外：*識別碼*、*上次修改日期*，以及*上次修改者*
- [狀態]** 資料行不是空白，此為必要資訊

若要防止書簽對書簽重複錯誤，請遵循下列最佳作法：

- 請勿將重複的 URL 用於不同的書簽。 如果 URL 已指派給其他書簽，而且您是從匯入檔案中重新加入，您會收到錯誤。 這也適用于其他類型的答卷的重複 URLs。
- 更新現有的書簽時，請使用 [ *書簽識別碼* ] 欄。 您可以更新現有書簽的任何其他屬性，例如關鍵字或描述，但您應確定 *書簽識別碼* 位於匯入檔案的適當欄中。 如果 *書簽識別碼* 存在，服務就不會將它視為新增，也不會將其當作錯誤處理。

## <a name="power-apps"></a>Power Apps

將現有的 PowerApps 新增至您的書籤，協助您的使用者完成工作，例如輸入假期時間或提出支出報告。

### <a name="power-apps-explained"></a>已說明電源應用程式

電源應用程式是一種服務，可讓您建立在瀏覽器中或在電話或平板電腦上執行的商務應用程式，不需要任何的編碼經驗。 PowerApps 可以在任何瀏覽器和任何裝置上運作，不到一分鐘即可迅速新增完成。 如需 PowerApps 的詳細資訊，請參閱：

- [引導學習](https://docs.microsoft.com/learn/browse/?products=powerapps)
- [文件](https://docs.microsoft.com/powerapps/maker/canvas-apps/get-sessionid)
- [Power Apps Home](https://make.preview.powerapps.com/environments/839eace6-59ab-4243-97ec-a5b8fcc104e4/home)

### <a name="add-a-power-app-to-a-bookmark"></a>將電源 App 新增至書簽

1. 尋找您要新增之 [電源應用程式的應用程式識別碼](https://docs.microsoft.com/powerapps/maker/canvas-apps/get-sessionid#get-an-app-id) 。
1. 在 [Microsoft 365 系統管理中心](https://admin.microsoft.com)中，移至 [ [**書簽**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/bookmarks)]。
1. 新增書籤或尋找您想要新增 **PowerApp** 的現有書籤。
1. 在 [書籤設定]**** 中，選取 [PowerApp]****，然後選取 [新增 PowerApp]****。
1. 輸入或貼上**應用程式識別碼**。
    系統會自動調整高度和寬度。 書籤能夠同時支援直向和橫向的方向，但目前無法變更大小。 書籤預覽會顯示完整功能的 PowerApp，讓您輕鬆測試。
1. 選取 [發佈]**** 或 [儲存為草稿]****。
