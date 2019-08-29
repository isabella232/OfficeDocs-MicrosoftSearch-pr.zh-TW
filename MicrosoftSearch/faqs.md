---
title: 常見問題集
ms.author: anfowler
author: adefowler
manager: shohara
ms.date: 10/19/2018
ms.audience: Admin
ms.topic: reference
ms.service: mssearch
localization_priority: Priority
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: cd3ee09d-58ab-4b8a-8822-fa11a1399672
ROBOTS: NoIndex
description: 取得有關企業搜尋和 Microsoft Search 常見問題的解答
ms.openlocfilehash: 3b30980c76915405767381fb3b6397468bdd1b68
ms.sourcegitcommit: c2c9e66af1038efd2849d578f846680851f9e5d2
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/27/2019
ms.locfileid: "36639497"
---
# <a name="frequently-asked-questions"></a>常見問題集

以下是最常見問題的清單。

> [!TIP]
> 在這裡看不到您的問題獲得解答嗎？ 請在這篇文章的意見反應中提出您的問題。

## <a name="is-advanced-query-understanding-supported"></a>是否支援進階查詢理解？

是的，Microsoft Search 會從較大的片語剖析查詢意圖。 此功能會使用 AI 以學習將常用多餘片語的使用者新增到查詢，但不影響使用者的搜尋意圖。 舉例來說，當使用者搜尋「告訴我如何變更密碼」，我們會截掉查詢中較不重要的字詞，並依據較相關的項目 (例如「變更密碼」) 來進行觸發。
  
此功能無法覆寫系統管理中心中設定的關鍵字。
  
## <a name="can-you-search-for-files-on-premises"></a>可以搜尋內部部署檔案嗎？

是。 如果您有 SharePoint 混合式部署，則可以搜尋 SharePoint 的內部部署檔案。
  
## <a name="how-do-i-make-bing-the-default-search-engine-for-people-in-my-org"></a>如何讓 Bing 成為我的組織中人員的預設搜尋引擎？

以下是設定預設搜尋引擎、預設首頁和預設瀏覽器的指示，可讓使用者獲得 Bing 中 Microsoft Search 的最佳體驗：

- [將 Edge 設為預設瀏覽器](set-default-browser.md)
- [讓 Bing 成為預設搜尋引擎](set-default-search-engine.md)
- [將 Bing.com 設為企業首頁](set-default-homepage.md)

  
## <a name="how-are-my-search-results-protected"></a>如何保護我的搜尋結果？

我們需要 Azure Active Directory (AAD) 驗證以存取來自 Trusted Cloud 的結果。 已驗證的使用者只會看到他們有權存取的內容。 搜尋查詢會去除身分識別，且記錄檔會和公用 Bing 搜尋流量分隔。 這種保護層級是業界唯一的。

## <a name="can-i-search-across-federated-organizations"></a>可以跨同盟組織搜尋嗎？

否。

## <a name="where-can-i-get-info-about-office-365-and-microsoft-365-compliance-tiers-and-categories"></a>我可以從哪裡獲得關於 Office 365 和 Microsoft 365 合規性層級和類別的資訊？

您可以在[符合產業標準和法規的合規性架構](https://download.microsoft.com/download/B/2/7/B27B3EF3-8849-4C18-8BA4-5AD755728620/Compliance%20Framework_customer%20guidance.pdf) (下載 PDF) 中找到詳細資料。