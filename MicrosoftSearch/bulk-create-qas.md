---
title: 大量建立問與答
ms.author: dawholl
author: dawholl
manager: kellis
ms.date: 12/18/2018
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: 7bada218-8908-4956-aae3-6ffaeef384ca
description: 在 Microsoft Search 系統管理入口網站中，使用匯入工具快速新增常見問題的解答
ms.openlocfilehash: f535cb7ae843def536976cb1f05c8601de592cbb
ms.sourcegitcommit: 3e91a6e70b48a0100adfed1b62ba79f2fd1735d2
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/13/2019
ms.locfileid: "34425655"
---
# <a name="bulk-create-qas"></a>大量建立問與答

> [!IMPORTANT]
> Bing 中的 Microsoft Search 設定現在可在 Microsoft 365 系統管理中心取得。 從在系統管理中心[指派搜尋系統管理員](https://docs.microsoft.com/zh-TW/microsoftsearch/setup-microsoft-search#step-2-assign-search-admin-and-search-editor)開始。
    
下載並使用 .csv 範本以大量建立或大量編輯問與答。 這也能輕鬆地大量儲存需要額外編輯或更新之草稿問與答的方式。 如果您需要大量編輯現有的問與答，請從系統管理入口網站中匯出、進行所需編輯，然後再加以匯入。
  
1. 按一下問與答區段右上角的 [匯入]****
    
2. 按一下 [下載問與答範本 (.csv)]****
    
3. 儲存並開啟 .csv 檔案
    
4. 新增問與答內容與設定，然後儲存檔案

    您應該將 .csv 檔案儲存為 CSV UTF-8 檔案，其他檔案類型和或編碼可能造成匯入錯誤
    
5. 在問與答區段右上角，按一下 [匯入]****
    
6. 在 [匯入問與答] 窗格中，按一下 [瀏覽]****，然後瀏覽至您要匯入的 .csv 檔案 
    
7. 按一下 [匯入]****

# <a name="prevent-import-errors"></a>防止匯入錯誤      
如果有任何必要資訊遺漏或無效，您會收到錯誤訊息。 依據錯誤的類型，系統可能會產生一份記錄檔，其中包含哪些列或欄需要修正的詳細資訊。 進行任何所需編輯，然後再次嘗試匯入檔案。

> [!NOTE]
> 直到解決所有的錯誤之前，您無法建立或編輯任何問與答。 

若要避免錯誤，請確定您匯入的檔案的格式正確：
- 包含匯入範本中的標題列
- 包含匯入範本中的所有資料行
- 資料行順序與匯入範本相同
- 這些資料行可以為空白：識別碼、上次修改日期，以及上次修改者
- [狀態] 資料行不能為空白，此為必要資訊  
問與答會根據狀態欄位不同而被儲存成草稿、建議、已排程，或者自動發佈。

同時，如果您包含現有問與答的識別碼，將會以匯入檔案中的資訊加以取代。

針對具有多個租用戶的組織，您可以從一個租用戶匯出您的問與答，並將它匯入到另一個租用戶。 但您必須在匯入之前，先移除 [識別碼] 資料行中的所有資料。

若要深入了解必要欄位與建議欄位，請參閱[建立問與答](create-qas.md)。

  

