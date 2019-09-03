---
title: 管理書籤
ms.author: anfowler
author: adefowler
manager: mnirkhe
ms.date: 05/30/2019
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: c0c814d0-f7e4-444e-b18e-09beb45c9322
description: 在 Microsoft Search 中建立、更新書籤及大量編輯書籤結果的方法
ms.openlocfilehash: 0cd37ebcd7cd3ea7bbe55064fd41a3c42b2e4725
ms.sourcegitcommit: f9760d027637cc0d2e5c3a9e47928422cb6e452a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/03/2019
ms.locfileid: "36170318"
---
# <a name="manage-bookmarks"></a>管理書籤

只要幾個步驟，您便可以建立書籤。 每個書籤都包括標題、URL，和一組能觸發書籤的關鍵字。 一個書籤可以有多個關鍵字，數個書籤可以共用相同的關鍵字，但不能共用保留的關鍵字。 建立或修改書籤時，搜尋索引會立即重新整理，且書籤會立即可供使用者使用。

如果組織已在 SharePoint 中設定升級的結果，您可以將升級的結果匯入到 **Microsoft 搜尋**，並讓您的使用者使用匯入的內容。 這是個快速填入搜尋結果的簡單方法，只要您設定 **Microsoft 搜尋**，利用它來提高使用者的工作效率。 建議您使用來自 SharePoint 提升的結果做為參考，以了解如何指定和建立相關的搜尋結果。 

## <a name="add-or-edit-a-single-bookmark"></a>新增或編輯單一書籤
1. 移至 **Microsoft 365 系統管理中心**。
1. 在功能窗格中，移至 [設定]****，然後選取 [Microsoft 搜尋]****。
預設會選取 [書籤]**** 索引標籤。
1. 若要新增書籤，請選取 [新增]****。 若要編輯書籤，請在相關的書籤清單中選取書籤。 
1. 當您新增或編輯資訊時，預覽會自動更新。
1. 儲存變更。

## <a name="add-or-edit-bookmark-using-browser-extensions"></a>使用瀏覽器擴充功能來新增或編輯書籤
搜尋系統管理員可以使用瀏覽器擴充功能輕鬆地建立搜尋內容。 安裝瀏覽器擴充功能模組，然後移至您要新增為書籤的網站，並將網站新增為書籤。

目前提供 Edge 和 Chrome 的瀏覽器擴充功能。 
- 若要下載 Edge 擴充功能，請移至 [Microsoft Store](https://www.microsoft.com/en-us/p/microsoft-search-content-creator/9nrqdbcbwq55?activetab=pivot:overviewtab) 並下載應用程式。
- 若要下載 Chrome 擴充功能，請移至 [Chrome 線上應用程式商店](https://chrome.google.com/webstore/detail/microsoft-search-content/nocnablpaoeecfmfnjoheefkogmleipm)並下載應用程式。

## <a name="bulk-add-or-edit-bookmarks"></a>大量新增或編輯書籤
搜尋系統管理員可以使用匯入或匯出功能來大量建立或編輯書籤。 當系統管理員想要新增或編輯大量書籤時，此功能非常實用。 

使用匯入/匯出功能，以便：
- 大量新增書籤 - 在書籤範本檔案中新增詳細資料，然後將它匯入。
- 大量編輯書籤 - 將書籤匯出至 .csv 檔案，然後編輯匯出的 .csv 檔案中書籤的詳細資料，然後匯入更新的 .csv 檔案。
- 從 SharePoint 匯入升級的網站。
- 備份書籤 - 將書籤匯出至 .csv 檔案。

若要匯入或匯出書籤：
1. 在 [書籤]**** 索引標籤的右上角，選取 [匯入]****。 選取 [匯出]**** 來下載 .csv 檔案中所有的現有書籤。
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
- 針對具有多個租用戶的組織，您可以從一個租用戶匯出您的書籤，並將它匯入到另一個租用戶。 但您必須在匯入之前，先移除 [識別碼]** 資料行中的資料。

### <a name="prevent-import-errors"></a>防止匯入錯誤
如果任何必要資料遺漏或無效，您會收到錯誤訊息，並且會產生記錄檔，其中包含要修正的資料列和資料行的詳細資訊。 進行所需編輯，然後再次嘗試匯入檔案。 在解決所有問題之前，您無法匯入或儲存任何書籤。

若要避免錯誤，請確定您匯入的檔案的格式正確，並且：
- 包含匯入範本中的標題列和所有資料行
- 資料行順序與匯入範本相同
- 所有資料行都有值，除了可以是空白的這三個以外：*識別碼*、*上次修改日期*，以及*上次修改者* 
- [狀態]** 資料行不是空白，此為必要資訊

## <a name="powerapps"></a>PowerApps
將現有的 PowerApps 新增至您的書籤，協助您的使用者完成工作，例如輸入假期時間或提出支出報告。 

### <a name="what-are-powerapps"></a>什麼是 PowerApps？
PowerApps 是一個服務，即使您沒有編寫程式碼經驗，也能打造在瀏覽器、手機或平板電腦上運行的商務 App。 PowerApps 可以在任何瀏覽器和任何裝置上運作，不到一分鐘即可迅速新增完成。 如需 PowerApps 的詳細資訊，請參閱：
- [引導學習](https://docs.microsoft.com/zh-TW/learn/browse/?products=powerapps)
- [文件](https://docs.microsoft.com/zh-TW/powerapps/maker/canvas-apps/get-sessionid)
- [PowerApps 首頁](https://make.preview.powerapps.com/environments/839eace6-59ab-4243-97ec-a5b8fcc104e4/home)

### <a name="add-a-powerapp-to-a-bookmark"></a>將 PowerApp 新增至書籤
1. 尋找您想要新增的 [PowerApp 的應用程式識別碼](https://docs.microsoft.com/zh-TW/powerapps/maker/canvas-apps/get-sessionid#get-an-app-id)。
1. 登入並移至 **Microsoft 365 系統管理中心**。
1. 在功能窗格中，移至 [設定]****，然後選取 **Microsoft Search**。
1. 新增書籤或尋找您想要新增 **PowerApp** 的現有書籤。
1. 在 [書籤設定]**** 中，選取 [PowerApp]****，然後選取 [新增 PowerApp]****。
1. 輸入或貼上**應用程式識別碼**。
    系統會自動調整高度和寬度。 書籤能夠同時支援直向和橫向的方向，但目前無法變更大小。 書籤預覽會顯示完整功能的 PowerApp，讓您輕鬆測試。
1. 選取 **發佈** 或 **儲存為草稿**。
