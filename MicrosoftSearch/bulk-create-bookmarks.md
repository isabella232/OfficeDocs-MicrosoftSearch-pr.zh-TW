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
ROBOTS: NoIndex
description: 與 Microsoft Search 系統管理入口網站中的匯入工具一次建立大量的書籤
ms.openlocfilehash: 2983a47a8761a2463b25497911024f9bfd069369
ms.sourcegitcommit: bfcab9d42e93addccd1e3875b41bc9cc1b6986cc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2019
ms.locfileid: "37948922"
---
# <a name="bulk-create-bookmarks"></a>大量建立書籤

> [!IMPORTANT]
> 本文章適用 Bing 系統管理入口網站中的 Microsoft Search。 我們正在將入口網站移至 Microsoft 365 系統管理中心，完成之後將會移除 Bing 系統管理入口網站中的 Microsoft Search。 建議您使用 Microsoft 365 系統管理中心來開始。 [Microsoft Search 概觀](overview-microsoft-search.md)。
    
下載並使用.csv 範本，以大量建立、 編輯及儲存的書籤。 若要大量編輯現有的書籤，匯出系統管理員入口網站、 進行必要的編輯，然後再將它們匯。
  
1. 在 [書籤] 區段中的右上角，按一下 [**匯入**
    
2. 按一下 [**下載書籤範本 (.csv)**
    
3. 儲存並開啟 .csv 檔案
    
4. 新增的書籤內容和設定，並將檔案儲存

    您應該將 .csv 檔案儲存為 CSV UTF-8 檔案，其他檔案類型和或編碼可能造成匯入錯誤
    
5. 在 [書籤] 區段中的右上角，按一下 [**匯入**
    
6. 在 [匯入的書籤] 窗格中，按一下 [**瀏覽**並瀏覽至您要匯入的.csv 檔案 
    
7. 按一下 [匯入]****

## <a name="prevent-import-errors"></a>防止匯入錯誤      
如果有任何必要資料遺失或無效，您就會收到錯誤訊息。 依據錯誤的類型，系統可能會產生一份記錄檔，其中包含哪些列或欄需要修正的詳細資訊。 進行任何所需編輯，然後再次嘗試匯入檔案。

> [!NOTE]
> 除非解決所有問題，您無法建立或編輯任何書籤。 

若要避免錯誤，請確定您匯入的檔案的格式正確：
- 包含匯入範本中的標題列
- 包含匯入範本中的所有欄
- 資料行順序與匯入範本相同
- 這些資料行可以為空白：識別碼、上次修改日期，以及上次修改者
- [狀態] 資料行不能為空白，此為必要資訊  
書籤會根據狀態欄位的不同而儲存成草稿、建議、已排程或自動發佈。

如果您加入現有的書籤的識別碼，則它會取代與匯入檔案中的資訊。

適用於負責管理多個組織的合作夥伴，您可以從一個組織匯出您的書籤，並匯入另一個。 但您必須在匯入之前，先移除 [識別碼] 資料行中的所有資料。

若要深入了解必要和建議的欄位，請參閱[建立書籤](create-bookmarks.md)。
