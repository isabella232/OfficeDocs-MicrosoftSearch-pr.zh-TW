---
title: 匯入 SharePoint 升級的結果和熱門查詢
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
description: 使用來自 SharePoint 的搜尋查詢建立 Microsoft 搜尋的工作結果
ms.openlocfilehash: cfd5fafd0529f537a55e436ef078800a4b9714177e04c63e65e968f16fcf322e
ms.sourcegitcommit: 71ac2a38971ca4452d1bddfc773ff8f45e1ffd77
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/06/2021
ms.locfileid: "54533822"
---
# <a name="import-sharepoint-promoted-results-and-top-queries"></a>匯入 SharePoint 升級的結果和熱門查詢

> [!IMPORTANT]
> 本文適用于 Bing 管理入口網站中的 Microsoft 搜尋。 我們正在將入口網站移至 Microsoft 365 系統管理中心，完成之後將會移除 Bing 系統管理入口網站中的 Microsoft Search。 建議您使用 Microsoft 365 系統管理中心來開始。 [Microsoft Search 概觀](overview-microsoft-search.md)。
    
為了利用您在 SharePoint 中所建立的使用者查詢和首選，Microsoft 搜尋包含兩個工具，將此資訊匯入為建議的書簽： 
  
## <a name="import-sharepoint-promoted-result-query-rules"></a>匯入 SharePoint 升級的結果查詢規則

將這些規則（先前稱為「首選」）匯入為建議的書簽。 若要讓使用者可以使用它們，請加以發佈。 發佈時間會根據您所選取的書簽數目而有所不同。
  
## <a name="import-top-sharepoint-queries-using-powershell"></a>使用 PowerShell 匯入 top SharePoint 查詢

- 從您的 SharePoint 下載最上層的查詢。 PowerShell 腳本會提示您輸入 SharePoint 系統管理員認證。
    
- 執行 SharePoint 搜尋每個熱門查詢以取得最上層搜尋結果。
    
- 將建議的書簽新增至管理入口網站。
    
- 最上層的 SharePoint 查詢是書簽的特別候選項。 使用 PowerShell 腳本，將其匯入為建議的書簽。 此腳本會執行下列工作：
    - 根據 SharePoint top 查詢新增建議書簽，以提升 Microsoft 搜尋書簽覆蓋範圍。 此腳本會下載 SharePoint 系統管理入口網站可存取的主要查詢，然後將其上傳為系統管理員的建議書簽，以供系統管理員在 Microsoft 搜尋系統管理入口網站中查看。
    - 根據預設，腳本會將建議的書簽新增至指定租使用者的所有可用月份。 它會從指定的 SharePoint 管理網站取得查詢上限，並將其新增至 Microsoft 搜尋建議的書簽。 建議的書簽需要系統管理員/編輯者在發佈之前于管理入口網站核准。 當您執行此腳本時，系統會提示您輸入認證，以存取 Microsoft 搜尋管理入口網站。
    - 腳本允許指定其他參數。 例如，您可以在每個可用月份中，將建議的書簽新增至指定租使用者的前 N 個查詢。
    - 您也可以選擇在指定的年份中，為特定承租人新增建議的書簽以取得月。 這個命令會從 SharePoint 管理網站取得指定期間內的查詢上限，並將其新增至 Microsoft 搜尋建議的書簽。
    - 此外，還有其他許多選項和命令模式：保管庫模式中 SharePoint 下載最上層查詢、在 [詳細資料] 模式中執行腳本，以及偵錯模式。
    - 下載[腳本。](https://www.bingforbusiness.com/distribution/SharepointTopQueryBookmarks.zip) 

如需要求、範例和可用參數的詳細資訊，請下載腳本，並查看讀我檔案。 PowerShell 腳本執行後，系統管理員或編輯器應查看建議的書簽，並在發佈之前做任何必要的編輯。