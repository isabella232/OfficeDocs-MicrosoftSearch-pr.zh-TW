---
title: 管理問與答
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
ms.assetid: 7e3432e6-5317-4d63-90b0-52da6fddd343
description: 個別尋找並更新解答，或使用 Microsoft Search 工具以一次編輯所有項目
ms.openlocfilehash: ee239aa73d4e650289f39d33c63c3e2df4f100cc
ms.sourcegitcommit: 3e91a6e70b48a0100adfed1b62ba79f2fd1735d2
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/13/2019
ms.locfileid: "34425657"
---
# <a name="manage-qas"></a>管理問與答

> [!IMPORTANT]
> Bing 中的 Microsoft Search 設定現在可在 Microsoft 365 系統管理中心取得。 從在系統管理中心[指派搜尋系統管理員](https://docs.microsoft.com/zh-TW/microsoftsearch/setup-microsoft-search#step-2-assign-search-admin-and-search-editor)開始。
    
隨著時間，您可能會需要更新問與答的狀態和內容以讓它保持相關。
  
## <a name="filter-qas"></a>篩選問與答

使用問與答頁面右上角的篩選選項，來依據日期與修改者尋找問與答。 例如，將日期滑桿設定為 30 天，並選取系統管理員或編輯者，以查看該人員在該段期間內建立或變更的問與答清單。
  
## <a name="change-qa-content-or-settings"></a>變更問與答內容或設定

1. 移至 Microsoft Search 系統管理入口網站
    
2. 在瀏覽窗格中，按一下 [問與答]****
    
3. 若要尋找問與答，請搜尋、篩選或按一下問與答狀態，以縮小您的結果
    
4. 若要變更或更新問與答，請按一下標題
    
5. 對內容或設定進行任何變更或更新，並預覽其顯示方式
    
6. 按一下 [儲存]****
    
## <a name="bulk-export-and-edit-qas"></a>大量匯出和編輯問與答

請不要編輯這些欄位中的資料：
  
- 識別碼
    
- 上次修改日期
    
- 上次修改者
    
識別碼是每個問與答的唯一識別碼，請不要編輯。 [上次修改日期] 和 [上次修改者] 欄位只應用來排序和尋找問與答。
  
1. 如果您想要匯出問與答的子集，請篩選它們
    
2. 按一下問與答頁面右上角的 [匯出]****
    
3. 儲存或開啟 .csv 檔案
    
4. 請編輯任何欄位中的資料：
    
   - 問題
    
   - URL
      
   - 關鍵字
    
   - 狀態
    
   - 解答描述
    
   - 保留關鍵字
    
   - 開始日期
    
   - 結束日期
    
   - 國家/地區
    
   - 群組
    
   - 裝置與作業系統
    
   - 目標變化
    
5. 儲存 .csv 檔案

    您應該將 .csv 檔案儲存為 CSV UTF-8 檔案，其他檔案類型和或編碼可能造成匯入錯誤
    
6. 在問與答頁面右上角，按一下 [匯入]****
    
7. 在 [匯入問與答] 窗格中，按一下 [瀏覽]****，並選取編輯的 .csv 檔案 
    
8. 按一下 [匯入]****
    
如果有任何必要資訊缺失或無效，您會收到錯誤訊息。 依據錯誤的類型，系統可能會產生一份記錄檔，其中包含哪些列或欄需要修正的詳細資訊。 進行任何所需編輯，然後再次嘗試匯入檔案。
  
> [!NOTE]
> 直到解決所有的錯誤之前，您無法建立或編輯任何問與答。 
  
並非所有欄位都為必要，必要欄位則會依據問與答的狀態而改變。 問與答會根據狀態欄位不同而被儲存成草稿、建議、已排程，或者自動發佈。 在[建立問與答](create-qas.md)中深入了解必要欄位與建議欄位。

  

