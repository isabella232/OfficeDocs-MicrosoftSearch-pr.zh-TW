---
title: 匯入 SharePoint 提升的結果與熱門查詢
ms.author: dawholl
author: dawholl
manager: kellis
ms.date: 9/8/2018
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
description: 使用 SharePoint 的搜尋查詢以建立 Microsoft Search 工作結果
ms.openlocfilehash: 1538c57a7b4138b36fe62e3076feb58d746b2b3e
ms.sourcegitcommit: be2e837d9b087bffe6ce40d72d7ae58a8fcdf3fe
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/30/2019
ms.locfileid: "34591600"
---
# <a name="import-sharepoint-promoted-results-and-top-queries"></a>匯入 SharePoint 提升的結果與熱門查詢

> [!IMPORTANT]
> 本文適用於 Bing 系統管理入口網站中的 Microsoft Search。 我們已將入口網站移至 Microsoft 365 管理中心，並在之後移除。 我們建議您使用 Microsoft 365 系統管理中心以開始。 [Microsoft Search 概觀](overview-microsoft-search.md)。
    
為了有效調控使用者的查詢與您在 SharePoint 中建立的首選，Microsoft Search 納入了兩項能將此資訊匯入為建議書籤的工具： 
  
## <a name="import-sharepoint-promoted-result-query-rules"></a>匯入 SharePoint 提升的結果查詢規則

將這些之前稱為首選的規則匯入為建議書籤。 若要將這些書籤提供給您的使用者，請進行發佈。 發佈時間會隨您所選書籤的數量而有所不同。
  
## <a name="import-top-sharepoint-queries-using-powershell"></a>使用 PowerShell 以匯入熱門 SharePoint 查詢

- 從您的 SharePoint 下載熱門查詢。 PowerShell 指令碼會提示您輸入 SharePoint 系統管理員認證。
    
- 針對每一個熱門查詢執行 SharePoint 搜尋，以取得最佳搜尋結果。
    
- 在系統管理入口網站新增建議書籤。
    
- 您的熱門 SharePoint 查詢擁有做為書籤的最佳條件。 請使用 PowerShell 指令碼以將它們匯入為建議書籤。 此指令碼將會：
    
如需關於需求、範例和可用參數的資訊，請下載指令碼並檢閱讀我檔案。 在執行 PowerShell 指令碼之後，系統管理員或編輯者應該在先檢閱建議的書籤，並進行任何必要的編輯，之後再發佈。

  

