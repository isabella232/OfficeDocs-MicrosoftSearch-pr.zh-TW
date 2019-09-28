---
title: 管理的書籤
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
description: 建立及更新書籤，而且方式來大量編輯 Microsoft Search 書籤結果
ms.openlocfilehash: 02b9bfecd97210ba8cd5b46bf3bc108bf66b6f01
ms.sourcegitcommit: 3da22a2e09830672ebf199e05a32fa89b75c083b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/27/2019
ms.locfileid: "37288971"
---
# <a name="manage-bookmarks"></a>管理的書籤

您可以只需要幾個步驟中建立書籤。 每個書籤包括標題、 URL，以及一組會觸發它的關鍵字。 書籤可以有多個關鍵字和幾個書籤可以共用相同的關鍵字，但無法共用保留的關鍵字。 建立或修改書籤時，立即重新整理搜尋索引和書籤可立即供使用者。

如果您的組織已升級的結果，在 SharePoint 中設定，您可以升級的結果匯入**Microsoft Search** ，並將匯入的內容提供給您的使用者。 這是簡單的方法，以快速填入搜尋結果，只要您設定**Microsoft 搜尋**，並讓您的使用者更有效率。 建議您為參考使用從 SharePoint 升級的結果，了解如何命名並建立相關的搜尋結果。 

## <a name="add-or-edit-a-single-bookmark"></a>新增或編輯的單一書籤
1. 移至**Microsoft 365 系統管理中心**。
1. 在功能窗格中，前往 [**設定**]，然後選取**Microsoft Search**。
根據預設，已選取 [**書籤**] 索引標籤。
1. 若要新增一個書籤，選取 [**新增新**。 若要編輯的書籤，請在相關的書籤清單中選取之書籤。 
1. 當您新增或編輯的資訊，在預覽會自動更新。
1. 儲存變更。

## <a name="add-or-edit-bookmark-using-browser-extensions"></a>新增或編輯書籤使用瀏覽器延伸模組
搜尋管理員可以輕易地建立搜尋內容，藉由使用瀏覽器延伸模組。 安裝瀏覽器延伸模組，然後移至您想要新增為書籤，並將網站新增為書籤的網站。

目前，可供 Edge 和 Chrome 瀏覽器延伸模組。 
- 若要下載 Edge 分機，請前往[Microsoft Store](https://www.microsoft.com/p/microsoft-search-content-creator/9nrqdbcbwq55?activetab=pivot:overviewtab)下載應用程式。
- 若要下載 Chrome 延伸模組，請移至[Chrome web 存放區](https://chrome.google.com/webstore/detail/microsoft-search-content/nocnablpaoeecfmfnjoheefkogmleipm)，並下載應用程式。

## <a name="bulk-add-or-edit-bookmarks"></a>大量新增或編輯書籤
搜尋管理員可以使用匯入或匯出功能，以大量建立或編輯書籤。 當系統管理員想要新增或編輯大量的書籤，這會是非常實用的功能。 

使用匯入/匯出功能：
- 大量新增書籤-詳細資料，檔案中新增的書籤範本，並再將它匯入。
- 大量編輯的書籤-將書籤匯出至.csv 檔案，然後編輯匯出的.csv 檔案中的書籤詳細資料，然後匯入更新過的.csv 檔案。
- 匯入 SharePoint 升級的網站。
- 備份的書籤-匯出至.csv 檔案的書籤。

若要匯入或匯出書籤：
1. 在右上方的**書籤**] 索引標籤上，選取 [**匯入**]。 選取 [若要下載.csv 檔案中的所有現有書籤的 [**匯出**]。
1. 在右窗格中，選擇 [匯入使用.csv 檔案的選項或從 SharePoint。
下載必要的欄位和詳細資料] 清單的範本檔案。 
1. 新增或編輯範本檔案中的書籤詳細資料，並再將它儲存在您的電腦上。 
1. 在 [**匯入的書籤**] 窗格中，選取 [**瀏覽]** ，然後您想要匯入的.csv 檔案。
1. 選取 [**匯入**。

以下是一些有關的範本檔案所述的重要事項：
- 永不編輯這些欄位中的資料：*識別碼*、*上次修改日期*，以及*上次修改者*
- 如果您加入現有的書籤的*識別碼*，則會取代匯入檔案中的資訊。
- 如果沒有相同的標題或 URL 與現有的書籤，書籤將會更新匯入檔案中的資訊。
- 並非所有範本檔案中的欄位都為必要欄位和必要的欄位而異的書籤狀態。
- 根據 [*狀態*] 欄位，書籤將會儲存為草稿，建議，排程，或他們將會自動將它發佈。
- 針對具有多個租用戶的組織，您可以從一個租用戶中匯出您的書籤，然後匯入另一個。 但是，您必須移除的資料 [*識別碼*] 欄中，匯入之前。

### <a name="prevent-import-errors"></a>防止匯入錯誤
如果任何必要的資料遺失或不正確，且在記錄檔中產生的列和欄修正的詳細資訊，您會收到錯誤。 進行必要的編輯，然後再試一次匯入檔案。 您不能匯入或儲存任何的書籤，直到解決所有問題。

若要避免錯誤，請確定您匯入檔案具有正確的格式和：
- 包含標題列和已匯入範本中的所有欄
- 資料行順序等同於匯入範本
- 所有欄都具有值，除了可以是空的三個：*識別碼*、*上次修改日期*，以及*上次修改者* 
- [*狀態*] 欄不是空的因為這是必要資訊

## <a name="powerapps"></a>PowerApps
協助您完成工作，例如輸入假期時間或報告費用，將現有的 PowerApps 新增至您的書籤的使用者。 

### <a name="what-are-powerapps"></a>PowerApps 是什麼？
PowerApps 是一種服務，可讓您建置商務應用程式，在瀏覽器中或在電話或平板電腦上執行需要任何程式碼撰寫體驗。 PowerApps 中的任何瀏覽器，以及在任何裝置上，並採取新增少於一分鐘。 如需 PowerApps 的詳細資訊，請參閱：
- [引導學習](https://docs.microsoft.com/learn/browse/?products=powerapps)
- [文件](https://docs.microsoft.com/powerapps/maker/canvas-apps/get-sessionid)
- [PowerApps 首頁](https://make.preview.powerapps.com/environments/839eace6-59ab-4243-97ec-a5b8fcc104e4/home)

### <a name="add-a-powerapp-to-a-bookmark"></a>書籤加入 PowerApp
1. 尋找您想要新增的[PowerApp 的應用程式識別碼](https://docs.microsoft.com/powerapps/maker/canvas-apps/get-sessionid#get-an-app-id)。
1. 登入，並移至**Microsoft 365 系統管理中心**。
1. 在功能窗格中，前往 [**設定**]，然後選取**Microsoft Search**。
1. 新增一個書籤或找出您想要新增至**PowerApp**現有書籤。
1. 在 [**書籤的設定**，選取 [ **Power 應用程式**，然後按一下 [**新增 Power 應用程式**]。
1. 輸入或貼上**應用程式識別碼**。
    自動調整其高度及寬度。 書籤可支援直向和橫向的顯示，但目前無法變更大小。 書籤預覽顯示，以方便測試完全正常運作 PowerApp。
1. 選取 [**發佈**或**儲存至草稿**。
