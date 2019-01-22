---
title: 匯入 SharePoint 升級的結果與查詢排行榜
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
description: 用以從 SharePoint 搜尋查詢建立 Microsoft Search 工作結果
ms.openlocfilehash: f4fa4354fed667800c1cdcf63c86f59d736c342a
ms.sourcegitcommit: bf52cc63b75f2e0324a716fe65da47702956b722
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/18/2019
ms.locfileid: "29380061"
---
# <a name="import-sharepoint-promoted-results-and-top-queries"></a><span data-ttu-id="366df-103">匯入 SharePoint 升級的結果與查詢排行榜</span><span class="sxs-lookup"><span data-stu-id="366df-103">Import SharePoint promoted results and top queries</span></span>

<span data-ttu-id="366df-104">利用使用者的查詢與您已建立在 SharePoint 中的首選，Microsoft Search 包含兩個工具來匯入此為建議的書籤的資訊：</span><span class="sxs-lookup"><span data-stu-id="366df-104">To leverage users' queries and Best Bets you've created in SharePoint, Microsoft Search includes two tools to import this information as suggested bookmarks:</span></span> 
  
## <a name="import-sharepoint-promoted-result-query-rules"></a><span data-ttu-id="366df-105">匯入 SharePoint 升級的結果查詢規則</span><span class="sxs-lookup"><span data-stu-id="366df-105">Import SharePoint promoted result query rules</span></span>

<span data-ttu-id="366df-p101">匯入這些規則先前稱為首選，為建議的書籤。若要使其提供給您的使用者，發佈它們。發佈時間而異根據您選取的書籤的數目。</span><span class="sxs-lookup"><span data-stu-id="366df-p101">Import these rules, previously called Best Bets, as suggested bookmarks. To make them available to your users, publish them. Publishing time varies based on the number of bookmarks you select.</span></span>
  
## <a name="import-top-sharepoint-queries-using-powershell"></a><span data-ttu-id="366df-109">匯入使用 PowerShell 的 SharePoint 查詢排行榜</span><span class="sxs-lookup"><span data-stu-id="366df-109">Import top SharePoint queries using PowerShell</span></span>

- <span data-ttu-id="366df-p102">從您的 SharePoint 下載排名最前面的查詢。PowerShell 指令碼會提示您提供 SharePoint 系統管理員認證。</span><span class="sxs-lookup"><span data-stu-id="366df-p102">Download the top queries from your SharePoint. The PowerShell script will prompt you for your SharePoint administrator credentials.</span></span>
    
- <span data-ttu-id="366df-112">執行 SharePoint 搜尋每個排名最前面的查詢來取得的最上層搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="366df-112">Run a SharePoint search for each of the top queries to get the top search result.</span></span>
    
- <span data-ttu-id="366df-113">建議書籤加入系統入口網站。</span><span class="sxs-lookup"><span data-stu-id="366df-113">Add suggested bookmarks to the Admin portal.</span></span>
    
- <span data-ttu-id="366df-p103">排名最前面的 SharePoint 查詢是絕佳應徵者的書籤。使用 PowerShell 指令碼以匯入為建議的書籤。此指令碼將會：</span><span class="sxs-lookup"><span data-stu-id="366df-p103">Your top SharePoint queries are excellent candidates for bookmarks. Use the PowerShell script to import them as suggested bookmarks. This script will:</span></span>
    
<span data-ttu-id="366df-p104">如需需求、 範例和可用參數，下載指令碼並檢閱讀我檔案。PowerShell 指令碼之後執行、 系統或編輯器應該檢閱建議書籤，並進行任何必要的編輯他們正在發佈前。</span><span class="sxs-lookup"><span data-stu-id="366df-p104">For information about requirements, examples, and available parameters, download the script and review the README file. After the PowerShell script runs, an admin or editor should review the suggested bookmarks and make any necessary edits before they're published.</span></span>

  

