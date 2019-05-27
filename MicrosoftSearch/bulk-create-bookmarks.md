---
title: 大量建立書籤
ms.author: dawholl
author: dawholl
manager: kellis
ms.date: 09/11/2018
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: def300e7-103c-4e92-a062-28ffa27561d7
description: 使用 Microsoft Search 系統管理入口網站的匯入工具一次建立許多書籤
ms.openlocfilehash: 560cda6f94060d428f2d18cc61bd2430cb31b474
ms.sourcegitcommit: 3e91a6e70b48a0100adfed1b62ba79f2fd1735d2
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/13/2019
ms.locfileid: "34425650"
---
# <a name="bulk-create-bookmarks"></a>大量建立書籤

> [!IMPORTANT]
> Bing 設定中的 Microsoft Search 現在可以在 Microsoft 365 管理中心中使用。 從系統管理中心的[指派搜尋系統管理員](https://docs.microsoft.com/zh-TW/microsoftsearch/setup-microsoft-search#step-2-assign-search-admin-and-search-editor)開始。
    
下載並使用 .csv 範本以大量建立、編輯和儲存書籤。 若要大量編輯現有的書籤，請從系統管理入口網站中匯出、進行所需編輯，然後再匯入它們。
  
1. 按一下 [書籤] 區段右上角的 [匯入]****
    
2. 按一下 [下載書籤範本 (.csv)]****
    
3. 儲存並開啟 .csv 檔案
    
4. 新增書籤內容和設定，然後儲存檔案

    您應該將 .csv 檔案儲存為 CSV UTF-8 檔案，其他檔案類型和或編碼可能造成匯入錯誤
    
5. 按一下 [書籤] 區段右上角的 [匯入]****
    
6. 在 [匯入書籤] 窗格中，按一下 [瀏覽]****，然後瀏覽至您要匯入的 .csv 檔案 
    
7. 按一下 [匯入]****

# <a name="prevent-import-errors"></a>防止匯入錯誤      
如果有任何必要資訊缺失或無效，您會收到錯誤訊息。 依據錯誤的類型，系統可能會產生一份記錄檔，其中包含哪些列或欄需要修正的詳細資訊。 進行任何所需編輯，然後再次嘗試匯入檔案。

> [!NOTE]
> 直到解決所有的錯誤之前，您無法建立或編輯任何書籤。 

若要避免錯誤，請確定您匯入的檔案的格式正確：
- 包含匯入範本中的標題列
- 包含匯入範本中的欄位
- 欄位順序與匯入範本相同
- 永不編輯這些欄位中的資料：[識別碼]、[上次修改日期]，以及 [上次修改者]
- [狀態] 欄位不能為空白，這是必要資訊  
書籤會根據 [狀態] 欄位的不同而儲存成草稿、建議、已排程或自動發佈。

同時，如果您包含現有書籤的識別碼，將會以匯入檔案中的資訊加以取代。

針對具有多個租用戶的組織，您可以從一個租用戶匯出您的書籤，並將它匯入到另一個租用戶。 但您必須在匯入之前，先移除 [識別碼] 欄位中的資料。

若要深入了解必要欄位與建議欄位，請參閱[建立書籤](create-bookmarks.md)。
