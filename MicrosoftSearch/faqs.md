---
title: 常見問題集
ms.author: jeffkizn
author: jeffkizn
manager: parulm
ms.audience: Admin
ms.topic: reference
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 取得有關企業搜尋和 Microsoft Search 常見問題的解答
ms.openlocfilehash: 94161d3ac53ca72a9f8298674a53fdaa0a80caaf5ca3802d47ea693043a30530
ms.sourcegitcommit: 71ac2a38971ca4452d1bddfc773ff8f45e1ffd77
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/06/2021
ms.locfileid: "54533930"
---
<!-- markdownlint-disable no-trailing-punctuation -->
# <a name="frequently-asked-questions"></a>常見問題集

以下是最常見問題的清單。

> [!TIP]
> 在這裡看不到您的問題獲得解答嗎？ 請在這篇文章的意見反應中提出您的問題。

## <a name="is-advanced-query-understanding-supported"></a>是否支援進階查詢理解？

是的，Microsoft Search 會從較大的片語剖析查詢意圖。 此功能會使用 AI 以學習將常用多餘片語的使用者新增到查詢，但不影響使用者的搜尋意圖。 例如，當使用者搜尋有關 *如何變更密碼的詳細資訊* 時，我們會從查詢中解壓縮較不重要的字詞，並根據相關的 *變更密碼（如變更密碼*）進行觸發。
  
這項功能不會覆寫[Microsoft 365 系統管理中心](https://admin.microsoft.com)中所設定的關鍵字。
  
## <a name="can-you-search-for-files-on-premises"></a>可以搜尋內部部署檔案嗎？

是。 如果您有 SharePoint 的混合式部署，您可以搜尋內部部署[SharePoint](http://sharepoint.com/)檔案。
  
## <a name="how-do-i-make-bing-the-default-search-engine-for-people-in-my-org"></a>如何讓 Bing 成為我的組織中人員的預設搜尋引擎？

以下是設定預設搜尋引擎、預設首頁及預設瀏覽器的指示，可為使用者提供[Bing](https://Bing.com)中 Microsoft 搜尋的最佳體驗：

- [將 Microsoft Edge 設定為您的預設瀏覽器](/deployedge/edge-default-browser)
- [讓 Bing 成為預設搜尋引擎](set-default-search-engine.md)
- [將 Bing.com 設為企業首頁](set-default-homepage.md)

## <a name="how-are-my-search-results-protected"></a>如何保護我的搜尋結果？

我們需要[Azure Active Directory](/azure/active-directory/)驗證，才能存取受信任的雲端的結果。 已驗證的使用者只會看到他們有權存取的內容。 在 Bing 中使用 Microsoft 搜尋時，會解除發現搜尋查詢，並將記錄與公用[Bing](https://Bing.com)搜尋流量分開。

## <a name="can-i-search-across-federated-organizations"></a>可以跨同盟組織搜尋嗎？

否。

## <a name="where-can-i-get-info-about-office-365-security-compliance-and-privacy"></a>我可以在哪裡取得有關 Office 365 安全性、規範和隱私權的資訊？

詳細資料可在 Office 365 的[信任中心頁面](https://www.microsoft.com/TrustCenter/CloudServices/office365/default.aspx)上找到。

## <a name="can-guest-users-leverage-microsoft-search-in-my-organization"></a>來賓使用者是否可以利用組織中的 Microsoft 搜尋？

Microsoft 365 透過[來賓存取](/microsoft-365/solutions/collaborate-with-people-outside-your-organization)，與組織外部的人員進行豐富的共同作業。 這些使用者將能夠對檔、網站、群組、清單及文件庫執行搜尋作業。 不過，來賓使用者將不會收到完整、個人化、Microsoft 搜尋體驗，而且可能需要利用頁面上的 [網頁搜尋] 方塊，而不是頁首中的 [統一 Microsoft 搜尋] 方塊。