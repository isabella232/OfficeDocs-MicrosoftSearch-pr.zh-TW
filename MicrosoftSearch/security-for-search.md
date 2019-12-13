---
title: 安全性和 Microsoft 中的搜尋 Bing 的隱私權
ms.author: anfowler
author: adefowler
manager: shohara
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 提供資訊給授權的使用者與 Microsoft Search in Bing 時保護您的公司資料和使用者
ms.openlocfilehash: d3d8822b68fc730885e973c0c24c52070d50eba8
ms.sourcegitcommit: f4cb37fdf85b895337caee827fb72b5b7fcaa8ad
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2019
ms.locfileid: "39995385"
---
# <a name="security-and-privacy-for-microsoft-search-in-bing"></a>安全性和 Microsoft 中的搜尋 Bing 的隱私權

具有增強的隱私權和安全性措施，Microsoft Search in Bing 可協助保護您的使用者與工作場所資料。

## <a name="secure-by-default"></a>預設安全性

Microsoft Search 的 Bing 要求進行透過 HTTPS。 連線是加密的端對端以增強安全性。
  
## <a name="authentication-and-authorization-with-azure-active-directory"></a>搭配 Azure Active Directory 的驗證與授權

Microsoft 中的搜尋 Bing 驗證是繫結至 Azure Active Directory。 當 Microsoft Search 使用者前往 Bing，Bing 標頭會顯示 Microsoft 帳戶以及公司或學校帳戶的登入選項。 如果 Bing 無法判斷使用者是否為合格的參與者，使用者可以移至[探索 Microsoft Search](https://www.bing.com/business/explore) 頁面，該頁面會自動將使用者重新導向至組織的登入頁面。
 
使用者僅能透過公司或學校帳戶存取 Microsoft Search。 若要登入，他們必須使用與存取 Office 365 服務 (例如 SharePoint 或 Outlook) 相同的認證。 個人 Microsoft 帳戶無法用來登入 Microsoft Search。
    
## <a name="single-sign-on"></a>單一登入

使用者已驗證與其他服務，例如 Outlook 或 SharePoint 中其公司或學校帳戶，則他們將會自動登入相同的公司或學校帳戶時他們在相同的瀏覽器中前往 Bing。 此外，當使用者已超出其公司或學校帳戶，他們將會自動登出從相同的瀏覽器中其他 Microsoft Office 服務。
  
## <a name="communicates-with-the-microsoft-cloud-from-the-browser"></a>從瀏覽器的 Microsoft 雲端進行通訊

當使用者以公司或學校帳戶登入時，Bing 會在瀏覽器中下載所需的用戶端資料庫，以取得 Microsoft Search 結果。 隨後，當他們搜尋時，瀏覽器內的程式碼會呼叫 Office 365 雲端，以取得工作結果。 若要這麼做，Microsoft Search 使用專用的 API，是層 C (SOC2 類型 1) 相容依照 Office 365 [業界標準與法規符合性架構] (https://download.microsoft.com/download/B/2/7/B27B3EF3-8849-4C18-8BA4-5AD755728620/Compliance%20Framework_customer%20guidance.pdf) （PDF 下載）。 這表示工作結果與工作資料永遠不會流經不符合規範的 Bing 系統。
  
## <a name="permissions"></a>權限

從 Office 365 工作負載 (例如 SharePoint 和商務用 OneDrive) 擷取的工作結果，都會在來源經過適當的安全性調整。 使用者無法看到像是 Word 文件或 PowerPoint 簡報這類透過 Office 365 檢視或存取的來源。 使用者只能查看自己的檔案，以及由作者在 SharePoint 中明確或隱含地 (例如透過群組資格) 與他們共用的檔案。

## <a name="microsoft-search-in-bing-protects-workplace-searches"></a>Microsoft Search in Bing 保護工作場所搜尋

當使用者在 Microsoft Bing 搜尋中，輸入搜尋查詢時，會發生兩個同時搜尋要求：

- 您的組織內部資源搜尋。
- 從 Bing.com 公開的個別搜尋結果。

因為工作場所搜尋可能是機密的所以 Microsoft Search 已實作一群說明如何處理來自 Bing.com 公用結果的個別搜尋的信任量值。

### <a name="logging"></a>記錄

<Need an intro paragraph here>

- 適用於 Microsoft Search 的 Bing 流量的所有 Bing.com 搜尋記錄會與您的工作場所身分識別解除都關聯。
- 如果符合一組限制或頻率閾值讓我們信賴查詢不是專屬於特定的組織，查詢會被視為[隱私權聲明](https://privacy.microsoft.com/privacystatement)搜尋和人工地智慧一節所述。 例如，這類查詢將用來建立模型和訓練公用功能，例如 [自動建議或相關的搜尋。
- 不符合這組限制或頻率閾值的查詢，將會與公開的非 Microsoft Search 流量分開儲存。

### <a name="advertising"></a>廣告

工作場所搜尋與 Bing.com 上顯示的廣告察覺與搜尋查詢的內容。 廣告永遠不會根據使用者的工作場所身分識別來鎖定使用者。
     
## <a name="gdpr"></a>GDPR

Microsoft 在[ 2018 年 5 月 21 日的部落格文章](https://blogs.microsoft.com/on-the-issues/2018/05/21/microsofts-commitment-to-gdpr-privacy-and-putting-customers-in-control-of-their-own-data/)反映了我們對 GDPR 規範，以及 Microsoft 會如何協助企業與組織履行 GDPR 合規性義務的承諾。 您可以在 Microsoft [信任中心常見問題集](https://www.microsoft.com/trustcenter/privacy/gdpr/gdpr-faqs)中找到其他詳細資料。 

針對客戶的內部資源執行的 Microsoft 搜尋查詢和傳回的結果會被視為客戶資料，因此也符合為反映在[信任中心常見問題集](https://www.microsoft.com/trustcenter/privacy/gdpr/gdpr-faqs)28 中所述的處理器承諾。 關於移至公用 Bing 從 Microsoft 搜尋查詢，Microsoft 遵守其 GDPR 義務資料控制者身分。

