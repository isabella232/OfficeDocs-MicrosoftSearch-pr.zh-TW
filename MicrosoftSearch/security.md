---
title: Microsoft Search 的安全性
ms.author: dawholl
author: dawholl
manager: kellis
ms.date: 9/12/2018
ms.audience: Admin
ms.topic: reference
ms.service: mssearch
localization_priority: Priority
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: 50461cb9-8707-46c1-935a-1b9608a98800
ROBOTS: NOINDEX
description: 在使用 Microsoft Search 提供資訊給獲授權使用者的同時，保護企業的資料與使用者
ms.openlocfilehash: 4e5e23e5e1389c95d28ede66e06707f9856a3770
ms.sourcegitcommit: fe7f3dae4edba97071a4d127e8a27bdf4fa00d81
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/05/2019
ms.locfileid: "34727937"
---
# <a name="security-for-microsoft-search"></a>Microsoft Search 的安全性

透過企業級的安全性，Microsoft Search 可隨時保護您的使用者與資料。


## <a name="secure-by-default"></a>預設安全性

Microsoft Search 能隨時確保提出的要求皆透過 HTTPS。 這道保護能確保連線受到端點對端點加密，強化安全性。
  
## <a name="authentication-and-authorization-with-azure-active-directory"></a>搭配 Azure Active Directory 的驗證與授權

Microsoft Search 的驗證已綁定至 Azure Active Directory。 當 Microsoft Search 使用者前往 Bing，Bing 標頭會顯示 Microsoft 帳戶以及公司或學校帳戶的登入選項。 如果 Bing 無法判斷使用者是否為合格的參與者，使用者可以移至[探索 Microsoft Search](https://www.bing.com/business/explore) 頁面，該頁面會自動將使用者重新導向至組織的登入頁面。 
  
使用者僅能透過公司或學校帳戶存取 Microsoft Search。 若要登入，他們必須使用與存取 Office 365 服務 (例如 SharePoint 或 Outlook) 相同的認證。 個人 Microsoft 帳戶無法用來登入 Microsoft Search。
  
使用者無法同時使用 Microsoft 帳戶和公司或學校帳戶登入 Bing。
  
## <a name="single-sign-on"></a>單一登入

如果使用者已在其他服務 (例如 Outlook 或 SharePoint) 中以公司或學校帳戶通過驗證，那當他們在同個瀏覽器中移至 Bing 時，系統便會自動登入 Microsoft Search。 此外，如果使用者登出 Microsoft Search，系統也會自動當他們登出其他服務。
  
## <a name="communicates-with-the-trusted-cloud-from-the-browser"></a>從瀏覽器使用 Trusted Cloud 進行通訊

當使用者以公司或學校帳戶登入時，Bing 會在瀏覽器中下載所需的用戶端資料庫，以取得 Microsoft Search 結果。 隨後，當他們搜尋時，瀏覽器內的程式碼會呼叫 Office 365 雲端，以取得工作結果。 為了執行這項程序，Microsoft Search 會使用專門的 API 層級 C (SOC2 類型 1)，為[符合 Office 365 產業標準和法規的合規性架構](https://download.microsoft.com/download/B/2/7/B27B3EF3-8849-4C18-8BA4-5AD755728620/Compliance%20Framework_customer%20guidance.pdf) (下載 PDF)。 這表示工作結果與工作資料永遠不會流經不符合規範的 Bing 系統。 
  
## <a name="permissions"></a>權限

從 Office 365 工作負載 (例如 SharePoint 和商務用 OneDrive) 擷取的工作結果，都會在來源經過適當的安全性調整。 使用者無法看到像是 Word 文件或 PowerPoint 簡報這類透過 Office 365 檢視或存取的來源。 使用者只能查看自己的檔案，以及由作者在 SharePoint 中明確或隱含地 (例如透過群組資格) 與他們共用的檔案。
  
## <a name="protects-user-queries-from-the-public-portion-of-bing"></a>保護使用者查詢不列入 Bing 的公開部分

由於工作相關的搜尋可能具敏感性質，Microsoft Search 針對 Bing 的公開網頁結果施行一套信任標準以處理這些搜尋。
  
不論使用者查詢傳回的回應中是否包含一或多個工作結果，系統都會採取下列措施：
  
- 記錄
    
  - 所有與 Microsoft Search 流量相關的搜尋記錄都會在去除身分識別後，與公開的非 Microsoft Search 流量分開儲存。 這些記錄會保留 18 個月，且限制為僅供偵錯之用。
    
  - 這些記錄中的查詢不會用來建立公開功能模型或進行訓練，例如自動建議或公開網頁的相關搜尋。
    
  - 限制存取會透過各種安全機制來管理，包括安全性群組與工程系統中的其他層級。
    
- 搜尋記錄
    
  - 使用公司或學校帳戶登入時，其他電腦或裝置無法獲得該使用者的搜尋記錄。
    
- 廣告
    
  - 絕不會將企業搜尋查詢與廣告客戶分享或建議給廣告客戶。
    
  - 與 Microsoft Search 有關的搜尋廣告記錄會與公開流量分開儲存。
    
  - 廣告永遠不會依據使用者的公司身分識別或組織進行投放。
    
## <a name="gdpr"></a>GDPR

Microsoft 在[ 2018 年 5 月 21 日的部落格文章](https://blogs.microsoft.com/on-the-issues/2018/05/21/microsofts-commitment-to-gdpr-privacy-and-putting-customers-in-control-of-their-own-data/)反映了我們對 GDPR 規範，以及 Microsoft 會如何協助企業與組織履行 GDPR 合規性義務的承諾。 您可以在 Microsoft [信任中心常見問題集](https://www.microsoft.com/en-us/trustcenter/privacy/gdpr/gdpr-faqs)中找到其他詳細資料。 在線上服務中針對組織客戶的客戶資料進行 Microsoft Search 查詢，也會符合第 28 條所述的處理承諾，如[信任中心常見問題集](https://www.microsoft.com/en-us/trustcenter/privacy/gdpr/gdpr-faqs)中所反映。 針對移至公開 Bing 查詢 (來自 Microsoft Search)，Microsoft 為資料控制者，並會依照 GDPR 中所述，去除查詢的身分識別。


