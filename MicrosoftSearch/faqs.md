---
title: 常見問題集
ms.author: dawholl
author: dawholl
manager: kellis
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
description: 取得有關企業搜尋和 Microsoft Search 常見問題的解答
ms.openlocfilehash: ed4179262dc20a441ce5e3acadc895bacb271fa9
ms.sourcegitcommit: a5fd9d4f46bbb7c539630735ac16e0c786939e5d
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/01/2019
ms.locfileid: "34425596"
---
# <a name="faqs"></a>常見問題集

這裡是組織和使用者對系統管理與使用 Microsoft Search 會有的常見問題集。
  
## <a name="whats-the-value-proposition-for-microsoft-search"></a>Microsoft Search 主張的價值是什麼？

Microsoft Search 是一種能同時安全地搜尋您工作與網路內容的方式。 只有 Microsoft 能夠提供這種跨網路與企業間的整合產品。 如需關於合規性的資訊，請參閱 [Microsoft Search 的安全性](security.md)。
  
## <a name="what-microsoft-search-features-are-available-now"></a>現在可使用 Microsoft Search 的哪些功能？

如需完整清單，請參閱 [Microsoft Search 的功能](features.md)。
  
## <a name="does-microsoft-search-support-advanced-query-understanding"></a>Microsoft Search 是否支援進階查詢理解？

是的，Microsoft Search 會從較大的片語去剖析您的查詢意圖。 此功能會使用 AI 以學習將常用多餘片語的使用者新增到查詢，但不影響使用者的搜尋意圖。 舉例來說，當使用者搜尋「告訴我如何變更密碼」，我們會截掉查詢中較不重要的字詞，並依據較相關的項目 (例如「變更密碼」) 來進行觸發。
  
此功能無法覆寫系統管理入口網站中設定的關鍵字。
  
## <a name="does-microsoft-search-search-for-files-on-premises-as-well-as-the-cloud"></a>Microsoft Search 是否會搜尋內部部署與雲端的檔案？

Microsoft Search 支援搜尋存在於 SharePoint Online、商務用 OneDrive 的文件，同時也會搜尋混合式內部部署 SharePoint 與 SharePoint Online，來尋找最常見的 Office 檔案類型。 如果您可以搜尋 SharePoint Online 中的內部部署內容，應該就能使用 Microsoft Search 尋找內部部署內容。 
  
## <a name="does-microsoft-search-replace-other-enterprise-search-experiences"></a>Microsoft Search 是否會取代其他企業搜尋體驗？

Microsoft Search 是一項能夠整合多個來源結果的互補供應項目。 如需支援檔案類型與來源的相關資訊，請查看下一個常見問題集。
  
## <a name="what-file-types-and-sources-does-microsoft-search-support"></a>Microsoft Search 支援哪些檔案類型與來源？

我們支援下列內容來源：
  
- SharePoint Online
    
- 混合式 SharePoint (內部部署 + SPO)
    
- 商務用 OneDrive
    
下列檔案類型會顯示於檔案搜尋，並會出現在 [人員] 和 [群組] 的 [檔案] 索引標籤上：
  
- Word
    
- Excel
    
- PowerPoint
    
- OneNote
    
- PDF
    
## <a name="what-compliance-and-trust-measures-are-in-place-for-microsoft-search"></a>Microsoft Search 有哪些合規性和信任措施？

如需關於合規性和信任措施的相關資訊，請參閱 [Microsoft Search 的安全性](security.md)。
  
## <a name="where-can-i-get-info-about-office-365-compliance-tierscategories"></a>我可以從哪裡獲得關於 Office 365 合規性層級/類別的資訊？

您可以在[符合產業標準和法規的合規性架構](https://download.microsoft.com/download/B/2/7/B27B3EF3-8849-4C18-8BA4-5AD755728620/Compliance%20Framework_customer%20guidance.pdf) (下載 PDF) 中找到詳細資料。 
  
## <a name="how-does-microsoft-search-keep-results-secure"></a>Microsoft Search 如何保持結果的安全？

如需 Microsoft Search 如何保護結果安全的相關資訊，請參閱 [Microsoft Search 的安全性](security.md)。
  
## <a name="what-are-the-content-sources-for-the-people-card"></a>人員卡片的內容來源為何？

人員卡片會從 Azure Active Directory、Exchange Online 和 SharePoint Online 取得資訊。
  
## <a name="do-microsoft-search-users-earn-microsoft-rewards"></a>Microsoft Search 使用者是否會獲得 Microsoft Rewards？

Microsoft Search 的搜尋不會獲得 Rewards 點數，且絕不會與使用者的 Microsoft 帳戶關聯。
  
## <a name="does-microsoft-search-respect-existing-file-permissions"></a>Microsoft Search 是否會尊重現有的檔案權限？

Microsoft Search 會尊重來源的安全性調整。 使用者只能看到他們有權存取的資訊。
  
## <a name="how-are-user-queries-protected-from-sharing-on-the-web"></a>如何保護使用者查詢不在網路上公開？

如需使用者查詢如何受到保護的相關資訊，請參閱 [Microsoft Search 的安全性](security.md)。
  
## <a name="what-types-of-advertising-do-microsoft-search-users-see"></a>Microsoft Search 使用者會看到哪類廣告？

如需廣告的相關資訊，請參閱 [Microsoft Search 的安全性](security.md)。
  
## <a name="what-are-the-minimum-requirements-to-enable-microsoft-search"></a>必須符合哪些最低需求才能啟用 Microsoft Search？

如需有關需求的資訊，請參閱 [Microsoft Search 的需求](requirements.md)。
  
## <a name="how-does-microsoft-search-use-azure-active-directory"></a>Microsoft Search 如何使用 Azure Active Directory？

Microsoft Search 會使用 Azure Active Directory 來驗證和授權對公司資料的存取。 Microsoft Search 符合跨所有 Microsoft 產品的身分識別處理實務標準。 這表示您的使用者可以透過單一登入以自動登入。 
  
## <a name="how-do-i-set-bing-as-the-default-search-provider-for-my-users"></a>我該如何將 Bing 設定為使用者的預設搜尋提供者？

如需相關資訊，請參閱[設定預設搜尋引擎](set-default-search-engine.md)、[設定預設首頁](set-default-homepage.md)，以及[設定預設瀏覽器](set-default-browser.md)。
  
## <a name="does-microsoft-search-provide-search-results-across-tenants"></a>Microsoft Search 是否提供跨租用戶的搜尋結果？

否，我們不提供跨租用戶或共用租用戶存取。 
  
## <a name="where-can-i-get-help-with-keywords-and-reserved-keywords"></a>哪裡可以取得關鍵字與保留關鍵字的說明？

如需關鍵字與保留關鍵字的使用資訊，請參閱[規劃內容](plan-your-content.md)。
  
## <a name="which-office-365-skus-are-supported"></a>支援哪些 Office 365 SKU？

如需支援 SKU 的相關資訊，請參閱 [Microsoft Search 的需求](requirements.md)。
  
## <a name="is-microsoft-search-gdpr-compliant"></a>Microsoft Search 是否符合 GDPR 規範？

如需 GDPR 合規性的相關資訊，請參閱 [Microsoft Search 的安全性](security.md)。
  
## <a name="why-am-i-signed-into-bing-automatically"></a>為什麼我會自動登入 Bing？

Microsoft Search 會在您登入 Office 365 或 Windows 10 時，使用 AAD 單一登入以自動透過您的公司或學校帳戶登入。 您可以隨時登出。
  
## <a name="what-is-bing-for-business"></a>什麼是商務用 Bing？

Microsoft Search 先前稱為 Bing for business。
  
## <a name="how-does-microsoft-search-order-result-cards-in-the-all-results-carousel"></a>Microsoft Search 如何排序 [所有結果] 浮動切換中的結果卡片？

Microsoft Search 會依據相關性，使用智慧型排序演算法以排序卡片。

  

