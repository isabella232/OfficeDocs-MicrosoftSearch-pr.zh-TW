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
ms.openlocfilehash: eb65121b53ab110b91880a65a5146d868f3a7405
ms.sourcegitcommit: d88226f9c3a99540a591dc0a26408bb9960cf39a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/19/2020
ms.locfileid: "48134165"
---
# <a name="manage-bookmarks"></a>管理書籤

只要幾個步驟，您便可以建立書籤。 每個書籤都包括標題、URL，和一組能觸發書籤的關鍵字。 您也可以將類別新增至可用於管理入口網站之排序和篩選的書簽。 書簽可以有多個關鍵字和書簽共用相同的關鍵字，但 reserved 關鍵字無法共用。 當書簽建立或修改時，搜尋索引會立即重新整理，使用者可以立即重新整理書簽。

如果您的組織在 SharePoint 中設定升級的結果，您可以將升級後的結果匯入 **Microsoft 搜尋** ，並讓您的使用者可以使用匯入的內容。 這是一種簡單的方法，可在您設定 **Microsoft 搜尋** 後快速填入搜尋結果，並讓使用者更有效率。 建議您使用從 SharePoint 升級的結果做為參考，以瞭解如何命名及建立相關的搜尋結果。

## <a name="add-or-edit-a-single-bookmark"></a>新增或編輯單一書籤

1. 在 [Microsoft 365 系統管理中心](https://admin.microsoft.com)中，移至 [ [**書簽**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/bookmarks)]。
1. 若要新增書簽，請選取 [ **新增**]。
若要編輯書籤，請在相關的書籤清單中選取書籤。
1. 當您新增或編輯資訊時，預覽會自動更新。
1. 儲存變更。

## <a name="add-or-edit-bookmark-using-browser-extensions"></a>使用瀏覽器擴充功能來新增或編輯書籤

搜尋系統管理員可以使用瀏覽器擴充功能輕鬆地建立搜尋內容。 安裝瀏覽器延伸名，移至您要新增為書簽的網站，然後新增書簽。

目前提供 Edge 和 Chrome 的瀏覽器擴充功能。

- 若要下載 Edge extensions，請移至 [Microsoft Store](https://www.microsoft.com/p/microsoft-search-content-creator/9nrqdbcbwq55?activetab=pivot:overviewtab) 並下載應用程式。
- 若要下載 Chrome extensions，請移至 [chrome web store](https://chrome.google.com/webstore/detail/microsoft-search-content/nocnablpaoeecfmfnjoheefkogmleipm) 並下載應用程式。

## <a name="bulk-add-or-edit-bookmarks"></a>大量新增或編輯書籤

使用 [匯入] 或 [匯出] 功能可大量建立或編輯書簽。 它可使新增或編輯大量的書簽更快速且更容易。 使用它來：

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

以下是範本檔案的一些重要點：

- 永遠不編輯這些欄位中的資料： *識別碼*、 *上次修改*日期和 *上次修改者*
- 如果您包括現有書簽的 *識別碼* ，它會被匯入檔案中的資訊所取代。
- 如果是具有相同職稱或 URL 的現有書簽，則會使用匯入檔案中的資訊更新書簽。
- 範本檔案中並非所有欄位都為必要，必要欄位則會依據書籤的狀態而改變。
- 根據 [ *省/州] （省/市* ）欄位，書簽將會儲存為草稿、建議、排程或會自動發行。
- 針對管理多個組織的合作夥伴，您可以從一個組織匯出書簽，然後將其匯入另一個組織。 不過，您必須先移除 [ *識別碼* ] 欄中的資料，再匯入。

### <a name="prevent-import-errors"></a>防止匯入錯誤

如果任何必要資料遺漏或無效，您會收到錯誤訊息，並且會產生記錄檔，其中包含要修正的資料列和資料行的詳細資訊。 進行所需編輯，然後再次嘗試匯入檔案。 在解決所有問題之前，您無法匯入或儲存任何書籤。

若要避免錯誤，請確定您匯入的檔案的格式正確，並且：

- 包含匯入範本中的標題列和所有資料行
- 資料行順序與匯入範本相同
- 所有的欄都有值，但三項可以是空的： *識別碼*、 *上次修改*時間及 *最後修改者*
- *State*欄不是空白的，其必要資訊

若要防止書簽書簽複製錯誤：

- 請勿將重複的 URL 用於不同的書簽。 如果將 URL 指派給其他書簽，而且嘗試從匯入檔案重新加入，您會收到錯誤。 這也適用于其他類型的答卷的重複 URLs。
- 更新現有的書簽時，請使用 [ *書簽識別碼* ] 欄。 您可以更新現有書簽的任何其他屬性，例如關鍵字或描述，但您應確定 *書簽識別碼* 位於匯入檔案的適當欄中。 如果 *書簽識別碼* 存在，則不會將它視為新的新增，也不會處理成錯誤。

## <a name="power-apps"></a>Power Apps

將現有的超級使用者新增至您的書簽，以協助您的使用者完成工作（例如輸入休假時間或報告費用）。

### <a name="power-apps-explained"></a>已說明電源應用程式

電源應用程式是一種服務，可讓您建立在瀏覽器中或在電話或平板電腦上執行的商務應用程式，不需要任何的編碼經驗。 Power App 可在任何瀏覽器和任何裝置上運作，而且不需要一分鐘就能加入。 如需有關 Power App 的詳細資訊，請參閱：

- [引導學習](https://docs.microsoft.com/learn/browse/?terms=power%20apps)
- [文件](https://docs.microsoft.com/powerapps/maker/canvas-apps/get-sessionid)
- [Power Apps Home](https://make.preview.powerapps.com/environments/839eace6-59ab-4243-97ec-a5b8fcc104e4/home)

### <a name="add-a-power-app-to-a-bookmark"></a>將電源 App 新增至書簽

1. 尋找您要新增之 [電源應用程式的應用程式識別碼](https://docs.microsoft.com/powerapps/maker/canvas-apps/get-sessionid#get-an-app-id) 。
1. 在 [Microsoft 365 系統管理中心](https://admin.microsoft.com)中，移至 [ [**書簽**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/bookmarks)]。
1. 新增書簽或尋找您要新增 **電源 App** 的現有書簽。
1. 在 [ **書簽設定**] 中，選取 [ **電源 App**]，然後輸入或貼上 **應用程式識別碼**。
    高度和寬度會根據建立電源 App 時選取的方向自動調整。 書簽支援縱向及橫向方向。 書籤預覽會顯示完整功能的 PowerApp，讓您輕鬆測試。
1. 選取 [發佈]**** 或 [儲存為草稿]****。
