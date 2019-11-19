---
title: 匯入 SharePoint 升級的結果與查詢排行榜
ms.author: dawholl
author: dawholl
manager: kellis
ms.audience: Admin
ms.topic: reference
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: 3d2a1498-174e-4214-9cf1-8b58cce5a872
ROBOTS: NOINDEX
description: 使用 SharePoint 搜尋查詢來建立 Microsoft Search 工作結果
ms.openlocfilehash: ae3535e322c4d06505595018669d8bd87171b9a9
ms.sourcegitcommit: 68087149c769a7cdde80944dd9c9933d2bf4a23f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/18/2019
ms.locfileid: "38699869"
---
# <a name="import-sharepoint-promoted-results-and-top-queries"></a>匯入 SharePoint 升級的結果與查詢排行榜

> [!IMPORTANT]
> 本文適用於 Microsoft Search Bing 系統管理入口網站中。 我們正在將入口網站移至 Microsoft 365 系統管理中心，完成之後將會移除 Bing 系統管理入口網站中的 Microsoft Search。 建議您使用 Microsoft 365 系統管理中心來開始。 [Microsoft Search 概觀](overview-microsoft-search.md)。
    
若要利用使用者的查詢與您已在 SharePoint 中建立的首選，Microsoft 搜尋會包含兩個工具來匯入為建議的書籤此資訊： 
  
## <a name="import-sharepoint-promoted-result-query-rules"></a>匯入 SharePoint 升階結果查詢規則

匯入這些規則，之前稱為 「 首選，以建議的書籤。 若要讓他們可以使用您的使用者，發佈它們。 發佈時間而異根據您所選取的書籤的數目。
  
## <a name="import-top-sharepoint-queries-using-powershell"></a>匯入使用 PowerShell 的 SharePoint 查詢排行榜

- 從您的 SharePoint 下載排名最前面的查詢。 PowerShell 指令碼會提示您輸入您的 SharePoint 系統管理員認證。
    
- 執行 SharePoint 搜尋每個查詢排行榜來取得最上層搜尋結果。
    
- 建議的書籤加入系統管理入口網站。
    
- 排名最前面的 SharePoint 查詢限於極佳的書籤。 使用 PowerShell 指令碼來匯入為建議的書籤。 此指令碼會執行下列工作：
    - 新增建議根據 SharePoint 排行榜，以提升 Microsoft Search 書籤涵蓋範圍的書籤。 此指令碼從 SharePoint 系統管理入口網站，下載存取查詢排行榜，並再將它們上傳為系統管理員在 Microsoft 搜尋系統管理入口網站中檢閱建議書籤。
    - 根據預設，指令碼會新增建議的書籤可指定租用戶的所有可用的月數。 它會從指定的 SharePoint 系統管理員網站取得查詢排行榜，並將它們新增至 Microsoft Search 為建議的書籤。 建議的書籤時，需要系統管理員/編輯器之前發佈核准管理入口網站中。 當您執行此指令碼時，系統會提示您若要存取 Microsoft 搜尋系統管理入口網站中的認證。
    - 指令碼可讓您指定其他參數。 例如，可以新增建議的書籤可指定租用戶中每個可用的月份的前 n 個查詢。
    - 或者，您可以新增建議的書籤可指定租用戶中特定年度的月數。 這個命令會從 SharePoint 系統管理員網站指定的時間期間取得查詢排行榜，並將它們新增至 Microsoft Search 為建議的書籤。
    - 同時，有許多其他選項和命令模式： 下載排行榜從 SharePoint 至指定的資料夾，並在安全模式中，執行指令碼 Verbose 模式和偵錯模式中執行指令碼。
    - 下載指令碼[在這裡](https://www.bingforbusiness.com/distribution/SharepointTopQueryBookmarks.zip)。 

如需需求、 範例和可用的參數，下載指令碼，並檢閱讀我檔案。 PowerShell 指令碼之後執行、 系統或編輯器應該檢閱建議的書籤，和他們正在發佈前進行任何必要的編輯。