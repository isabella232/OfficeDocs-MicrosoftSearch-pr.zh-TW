---
title: Microsoft 搜尋產品的安全性
ms.author: dawholl
author: dawholl
manager: kellis
ms.date: 9/12/2018
ms.audience: Admin
ms.topic: reference
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: 50461cb9-8707-46c1-935a-1b9608a98800
description: 保護您的企業資料和使用者同時授權使用者提供資訊與 Microsoft Search
ms.openlocfilehash: 65cf1d49e32edbb8061a06f8da7ba644c2145e24
ms.sourcegitcommit: bf52cc63b75f2e0324a716fe65da47702956b722
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/18/2019
ms.locfileid: "29380075"
---
# <a name="security-for-microsoft-search"></a>Microsoft 搜尋產品的安全性

企業級安全性與 Microsoft Search 一律會持續使用者與受保護的資料。
  
## <a name="secure-by-default"></a>預設會保護安全

Microsoft Search 一律會確保 HTTPS 上所做的要求。這可保護可確保連線加密的端對端的增強的安全性。
  
## <a name="authentication-and-authorization-with-azure-active-directory"></a>驗證與授權與 Azure Active Directory

Microsoft 搜尋產品的驗證已繫結至 Azure Active Directory。當 Microsoft Search 使用者移至 [Bing 時、 標頭會顯示為 Microsoft 帳戶的登入選項 Bing 同時讓公司或學校帳戶。如果 Bing 無法判斷使用者是否為合格的參與者，使用者可以移至 [[探索 Microsoft 搜尋](https://www.bing.com/business/explore)] 頁面上，其中他們將自動重新導向至您的組織登入頁面。 
  
使用者可以存取 Microsoft Search 只能透過的工時或學校帳戶。他們必須使用存取 Office 365 服務，例如 SharePoint 或 Outlook 時所用的相同認證登入。個人 Microsoft 帳戶不能用來登入 Microsoft 搜尋。
  
使用者不能被登入 Bing 與 Microsoft 帳戶及工作或學校帳戶在同一時間。
  
## <a name="single-sign-on"></a>單一登入

如果與其他服務，例如 Outlook 或 SharePoint 中其工作或學校帳戶已驗證使用者他們將會自動登入 Microsoft Search 當他們移至 [Bing 在相同的瀏覽器中。此外，當使用者登出 Microsoft Search，他們將會自動登出從相同的瀏覽器中的其他服務。
  
## <a name="communicates-with-the-trusted-cloud-from-the-browser"></a>與瀏覽器信任雲端通訊

當使用者登入其工作或學校帳戶，Bing 會下載必要的用戶端程式庫以啟用 Microsoft 搜尋結果的瀏覽器。然後，這些搜尋，請瀏覽器中的程式碼會呼叫 Office 365 雲端取得工作結果。若要這樣做，Microsoft Search 使用專用的 API，是層 C (SOC2 類型 1) 相容 」 Office 365[產業標準和法規符合性 Framework](https://download.microsoft.com/download/B/2/7/B27B3EF3-8849-4C18-8BA4-5AD755728620/Compliance%20Framework_customer%20guidance.pdf) （PDF 下載）。這表示透過非相容的 Bing 系統永不流程工作結果與公司資料。 
  
## <a name="permissions"></a>權限

工作結果擷取自 Office 365 工作負載，例如 SharePoint 和 OneDrive for Business 都是經過安全性調整來源。使用者無法看到如 Word 文件或 PowerPoint 簡報他們無法看到和透過 Office 365 存取的資源。僅可檢視自己的檔案和已與共用其作者所明確或隱含的檔案 （透過群組成員資格，例如） SharePoint 中。
  
## <a name="protects-user-queries-from-the-public-portion-of-bing"></a>從公用部分 Bing 保護使用者查詢

因為工作相關的搜尋可能機密、 Microsoft Search 實作一組信任量值的這些公用 web 結果組件的 Bing 的處理方式。
  
不論是否使用者查詢會包含一或多個工作結果中傳回的回應，採取下列措施：
  
- 記錄
    
  - Microsoft Search 流量相關的所有搜尋記錄檔已取消識別和分開儲存公用、 非 Microsoft 搜尋流量。他們保留 18 個月內，並存取僅限於僅適用於偵錯。
    
  - 這些記錄檔中的查詢不用以模型或公用功能例如 [自動建議或相關的公用 web 搜尋的訓練。
    
  - 透過各種安全的機制，包括安全性群組及工程系統內其他層級管理限制] 存取權。
    
- 搜尋歷程記錄
    
  - 登入工作或學校帳戶，當使用者搜尋歷程記錄不會是可在其他電腦或裝置。
    
- 公告
    
  - 企業搜尋查詢不會與共用或建議的廣告。
    
  - 公用流量會分開儲存到 Microsoft 搜尋相關的搜尋 Ads 記錄。
    
  - Ads 永遠不會針對取決於其公司身分識別或組織的使用者。
    
## <a name="gdpr"></a>GDPR

[2018 年 5 月 21、 部落格張貼](https://blogs.microsoft.com/on-the-issues/2018/05/21/microsofts-commitment-to-gdpr-privacy-and-putting-customers-in-control-of-their-own-data/)microsoft 反映 GDPR 規範我們承諾和 Microsoft 如何協助企業和自己 GDPR 規範義務也提供組織。您可以在 Microsoft[信任中心常見問題集](https://www.microsoft.com/en-us/trustcenter/privacy/gdpr/gdpr-faqs)找到其他的詳細資訊。針對內線上服務的組織客戶的客戶資料操作的 Microsoft 搜尋查詢也將符合述反映在[信任中心常見問題集](https://www.microsoft.com/en-us/trustcenter/privacy/gdpr/gdpr-faqs)文章 28 處理器承諾。表示從 Microsoft Search 移至 [公用 Bing 的查詢，Microsoft 資料控制站與實作以取消識別查詢如底下 GDPR 所述的量值。


