---
title: 常見問題集
ms.author: anfowler
author: adefowler
manager: shohara
ms.audience: Admin
ms.topic: reference
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 取得有關企業搜尋和 Microsoft Search 常見問題的解答
ms.openlocfilehash: edfb8346263d60184d8655afa24118ed4b3e3bca
ms.sourcegitcommit: 68087149c769a7cdde80944dd9c9933d2bf4a23f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/18/2019
ms.locfileid: "38699791"
---
# <a name="frequently-asked-questions"></a>常見問題集

以下是最常見問題的清單。

> [!TIP]
> 在這裡看不到您的問題獲得解答嗎？ 請在這篇文章的意見反應中提出您的問題。

## <a name="is-advanced-query-understanding-supported"></a>是否支援進階查詢理解？

是的，Microsoft Search 會從較大的片語剖析查詢意圖。 此功能會使用 AI 以學習將常用多餘片語的使用者新增到查詢，但不影響使用者的搜尋意圖。 例如，當使用者搜尋*告訴我更多有關如何變更我的密碼請*我們解壓縮較重要的文字查詢和相關的項目，例如*變更密碼*為基礎的觸發程序。
  
這項功能不會覆寫在 Microsoft 365[系統管理中心](https://admin.microsoft.com)中設定的關鍵字。
  
## <a name="can-you-search-for-files-on-premises"></a>可以搜尋內部部署檔案嗎？

是。 如果您有 SharePoint 的混合式部署，您可以搜尋內部部署[SharePoint](http://sharepoint.com/)檔案。
  
## <a name="how-do-i-make-bing-the-default-search-engine-for-people-in-my-org"></a>如何讓 Bing 成為我的組織中人員的預設搜尋引擎？

以下是設定預設搜尋引擎、 預設首頁和預設的瀏覽器的指示，授與您的使用者與 Microsoft Search 的最佳經驗， [Bing](https://Bing.com)中：

- [設為預設瀏覽器的 Microsoft Edge](set-default-browser.md)
- [讓 Bing 成為預設搜尋引擎](set-default-search-engine.md)
- [將 Bing.com 設為企業首頁](set-default-homepage.md)

  
## <a name="how-are-my-search-results-protected"></a>如何保護我的搜尋結果？

我們需要[Azure Active Directory](https://docs.microsoft.com/azure/active-directory/)驗證以存取結果從信任雲端。 已驗證的使用者只會看到他們有權存取的內容。 去除識別搜尋查詢，以及記錄檔分開的公用[Bing](https://Bing.com)搜尋流量。 這種保護層級是業界唯一的。

## <a name="can-i-search-across-federated-organizations"></a>可以跨同盟組織搜尋嗎？

否。

## <a name="where-can-i-get-info-about-office-365-and-microsoft-365-compliance-tiers-and-categories"></a>我可以從哪裡獲得關於 Office 365 和 Microsoft 365 合規性層級和類別的資訊？

您可以在[符合產業標準和法規的合規性架構](https://download.microsoft.com/download/B/2/7/B27B3EF3-8849-4C18-8BA4-5AD755728620/Compliance%20Framework_customer%20guidance.pdf) (下載 PDF) 中找到詳細資料。

## <a name="can-users-earn-microsoft-rewards-points-with-their-work-or-school-account"></a>使用者能否使用其公司或學校帳戶來獲得 Microsoft Rewards 積分？

Microsoft Search 要求企業使用者使用公司或學校帳戶登入。 但使用者無法使用這些帳戶來加入或登入 Microsoft Rewards 方案。 但有一個例子，企業使用者可能會看到 Rewards 積分累算。 當 Microsoft Search 使用者的 Rewards 帳戶是使用 <a href="https://www.microsoft.com/welcome?rtc=1">Microsoft 帳戶</a>建立時，即可能發生此情況。 (與 Microsoft 帳戶相關聯的電子郵件地址可以來自 Outlook.com、Hotmail.com、Gmail、Yahoo 或其他提供者。) 如果使用者在同一位瀏覽器工作階段中同時使用他們的公司帳戶和 Microsoft 帳戶登入，則可能會對其 Rewards 帳戶累算積分。 使用者可以透過在使用 Microsoft Search 搜尋時清除其 Cookie 來停止累算積分。 

