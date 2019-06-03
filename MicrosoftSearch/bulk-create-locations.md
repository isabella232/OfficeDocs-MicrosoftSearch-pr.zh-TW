---
title: 大量建立位置
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
ms.assetid: 15c9fada-f7a6-4210-aa6b-028b32217830
ROBOTS: NoIndex
description: 使用 Microsoft Search 系統管理入口網站的匯入工具一次新增許多位置
ms.openlocfilehash: 186f6973de1ff87b62b5f07a47eb41acdd842010
ms.sourcegitcommit: be2e837d9b087bffe6ce40d72d7ae58a8fcdf3fe
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/30/2019
ms.locfileid: "34591393"
---
# <a name="bulk-create-locations"></a>大量建立位置

> [!IMPORTANT]
> 本文章適用 Bing 系統管理入口網站中的 Microsoft Search。 我們正在將入口網站移至 Microsoft 365 系統管理中心，完成之後入口網站將會移除。 我們建議您使用 Microsoft 365 系統管理中心開始。 [Microsoft Search 概觀](overview-microsoft-search.md)。
    
下載並使用 .csv 範本以大量建立、編輯和儲存位置。 
  
1. 在 [位置] 區段右上角，按一下 [匯入]****
    
2. 按一下 [下載位置範本 (.csv)]****
    
3. 儲存並開啟 .csv 檔案
    
4. 新增位置內容，然後儲存檔案

    您應該將 .csv 檔案儲存為 CSV UTF-8 檔案，其他檔案類型和/或編碼可能會造成匯入錯誤
    
5. 在 [位置] 區段右上角，按一下 [匯入]****
    
6. 在 [匯入位置] 窗格中，按一下 [瀏覽]****，然後瀏覽至您要匯入的 .csv 檔案 
    
7. 按一下 [匯入]****

匯入和匯出位置範本中的欄位都是一樣的。 您可以匯出、大量編輯，再匯入編輯，或使用空白範本從頭開始大量建立新的位置。 若要大量編輯現有的位置，請從系統管理入口網站中匯出、進行所需編輯，然後再匯入它們。

# <a name="prevent-import-errors"></a>防止匯入錯誤  
如果有任何必要資料遺失或無效，您就會收到錯誤訊息。 依據錯誤的類型，系統可能會產生一份記錄檔，其中包含哪些列或欄需要修正的詳細資訊。 進行任何所需編輯，然後再次嘗試匯入檔案。
  
> [!NOTE]
> 直到解決所有的錯誤之前，您無法建立或編輯任何位置。 

若要避免錯誤，請確定您匯入的檔案的格式正確：
- 包含匯入範本中的標題列
- 包含匯入範本中的所有欄
- 欄順序與匯入範本相同
- 這些欄可以空白：識別碼、上次修改日期、上次修改者，以及經度/緯度  
如果經度/緯度欄位空白，我們會根據地址嘗試判斷
- [狀態] 欄不能空白，此為必要資訊  
位置會根據 [狀態] 欄位的不同而儲存成草稿、建議、已排程或自動發佈。

同時，如果您包含現有位置的識別碼，將會以匯入檔案中的資訊加以取代。

針對具有多個租用戶的組織，您可以從一個租用戶匯出您的位置，並將它匯入到另一個租用戶。 但您必須在匯入之前，先移除 [識別碼] 欄中的所有資料。
  
若要深入了解必要欄位與建議欄位，請參閱[新增位置](add-a-location.md)。

  

