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
# <a name="security-for-microsoft-search"></a><span data-ttu-id="7f44f-103">Microsoft 搜尋產品的安全性</span><span class="sxs-lookup"><span data-stu-id="7f44f-103">Security for Microsoft Search</span></span>

<span data-ttu-id="7f44f-104">企業級安全性與 Microsoft Search 一律會持續使用者與受保護的資料。</span><span class="sxs-lookup"><span data-stu-id="7f44f-104">With enterprise-grade security, Microsoft Search always keeps your users and data protected.</span></span>
  
## <a name="secure-by-default"></a><span data-ttu-id="7f44f-105">預設會保護安全</span><span class="sxs-lookup"><span data-stu-id="7f44f-105">Secure by default</span></span>

<span data-ttu-id="7f44f-p101">Microsoft Search 一律會確保 HTTPS 上所做的要求。這可保護可確保連線加密的端對端的增強的安全性。</span><span class="sxs-lookup"><span data-stu-id="7f44f-p101">Microsoft Search always ensures requests are made over HTTPS. This safeguard ensures the connection is encrypted end-to-end for enhanced security.</span></span>
  
## <a name="authentication-and-authorization-with-azure-active-directory"></a><span data-ttu-id="7f44f-108">驗證與授權與 Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="7f44f-108">Authentication and authorization with Azure Active Directory</span></span>

<span data-ttu-id="7f44f-p102">Microsoft 搜尋產品的驗證已繫結至 Azure Active Directory。當 Microsoft Search 使用者移至 [Bing 時、 標頭會顯示為 Microsoft 帳戶的登入選項 Bing 同時讓公司或學校帳戶。如果 Bing 無法判斷使用者是否為合格的參與者，使用者可以移至 [[探索 Microsoft 搜尋](https://www.bing.com/business/explore)] 頁面上，其中他們將自動重新導向至您的組織登入頁面。</span><span class="sxs-lookup"><span data-stu-id="7f44f-p102">Authentication for Microsoft Search is tied to Azure Active Directory. When Microsoft Search users go to Bing, the Bing header will show sign-in options for a Microsoft account as well as a work or school account. If Bing can't determine whether a user is an eligible participant, users can go to the [Explore Microsoft Search](https://www.bing.com/business/explore) page, where they'll be automatically redirected to your organization's sign-in page.</span></span> 
  
<span data-ttu-id="7f44f-p103">使用者可以存取 Microsoft Search 只能透過的工時或學校帳戶。他們必須使用存取 Office 365 服務，例如 SharePoint 或 Outlook 時所用的相同認證登入。個人 Microsoft 帳戶不能用來登入 Microsoft 搜尋。</span><span class="sxs-lookup"><span data-stu-id="7f44f-p103">Users can access Microsoft Search only through a work or school account. They need to sign in with the same credentials they use to access Office 365 services such as SharePoint or Outlook. A personal Microsoft account can't be used to sign in to Microsoft Search.</span></span>
  
<span data-ttu-id="7f44f-115">使用者不能被登入 Bing 與 Microsoft 帳戶及工作或學校帳戶在同一時間。</span><span class="sxs-lookup"><span data-stu-id="7f44f-115">Users can't be signed in to Bing with both a Microsoft account and a work or school account at the same time.</span></span>
  
## <a name="single-sign-on"></a><span data-ttu-id="7f44f-116">單一登入</span><span class="sxs-lookup"><span data-stu-id="7f44f-116">Single sign-on</span></span>

<span data-ttu-id="7f44f-p104">如果與其他服務，例如 Outlook 或 SharePoint 中其工作或學校帳戶已驗證使用者他們將會自動登入 Microsoft Search 當他們移至 [Bing 在相同的瀏覽器中。此外，當使用者登出 Microsoft Search，他們將會自動登出從相同的瀏覽器中的其他服務。</span><span class="sxs-lookup"><span data-stu-id="7f44f-p104">If a user is already authenticated with their work or school account in another service, such as Outlook or SharePoint, they'll be automatically signed in to Microsoft Search when they go to Bing in the same browser. Also, when the user signs out of Microsoft Search, they'll be automatically signed out from other services in the same browser.</span></span>
  
## <a name="communicates-with-the-trusted-cloud-from-the-browser"></a><span data-ttu-id="7f44f-119">與瀏覽器信任雲端通訊</span><span class="sxs-lookup"><span data-stu-id="7f44f-119">Communicates with the Trusted Cloud from the browser</span></span>

<span data-ttu-id="7f44f-p105">當使用者登入其工作或學校帳戶，Bing 會下載必要的用戶端程式庫以啟用 Microsoft 搜尋結果的瀏覽器。然後，這些搜尋，請瀏覽器中的程式碼會呼叫 Office 365 雲端取得工作結果。若要這樣做，Microsoft Search 使用專用的 API，是層 C (SOC2 類型 1) 相容 」 Office 365[產業標準和法規符合性 Framework](https://download.microsoft.com/download/B/2/7/B27B3EF3-8849-4C18-8BA4-5AD755728620/Compliance%20Framework_customer%20guidance.pdf) （PDF 下載）。這表示透過非相容的 Bing 系統永不流程工作結果與公司資料。</span><span class="sxs-lookup"><span data-stu-id="7f44f-p105">When a user signs in with their work or school account, Bing will download the necessary client libraries to the browser to enable Microsoft Search results. Then, when they search, the in-browser code calls the Office 365 cloud to get work results. To do this, Microsoft Search uses a dedicated API that is Tier C (SOC2 Type 1) compliant pursuant to the Office 365 [Compliance Framework for Industry Standards and Regulations](https://download.microsoft.com/download/B/2/7/B27B3EF3-8849-4C18-8BA4-5AD755728620/Compliance%20Framework_customer%20guidance.pdf) (PDF download). This means work results and work data never flow through non-compliant Bing systems.</span></span> 
  
## <a name="permissions"></a><span data-ttu-id="7f44f-124">權限</span><span class="sxs-lookup"><span data-stu-id="7f44f-124">Permissions</span></span>

<span data-ttu-id="7f44f-p106">工作結果擷取自 Office 365 工作負載，例如 SharePoint 和 OneDrive for Business 都是經過安全性調整來源。使用者無法看到如 Word 文件或 PowerPoint 簡報他們無法看到和透過 Office 365 存取的資源。僅可檢視自己的檔案和已與共用其作者所明確或隱含的檔案 （透過群組成員資格，例如） SharePoint 中。</span><span class="sxs-lookup"><span data-stu-id="7f44f-p106">Work results retrieved from Office 365 workloads such as SharePoint and OneDrive for Business are security trimmed at the source. Users can't see resources such as Word documents or PowerPoint presentations they can't see and access through Office 365. They can only see their own files and files that have been shared with them by the author explicitly or implicitly (through a group membership, for example) in SharePoint.</span></span>
  
## <a name="protects-user-queries-from-the-public-portion-of-bing"></a><span data-ttu-id="7f44f-128">從公用部分 Bing 保護使用者查詢</span><span class="sxs-lookup"><span data-stu-id="7f44f-128">Protects user queries from the public portion of Bing</span></span>

<span data-ttu-id="7f44f-129">因為工作相關的搜尋可能機密、 Microsoft Search 實作一組信任量值的這些公用 web 結果組件的 Bing 的處理方式。</span><span class="sxs-lookup"><span data-stu-id="7f44f-129">Because work-related searches may be sensitive, Microsoft Search has implemented a set of trust measures for how these are handled by the public web results part of Bing.</span></span>
  
<span data-ttu-id="7f44f-130">不論是否使用者查詢會包含一或多個工作結果中傳回的回應，採取下列措施：</span><span class="sxs-lookup"><span data-stu-id="7f44f-130">Regardless of whether a user query contains one or more work results in the returned response, the following measures are taken:</span></span>
  
- <span data-ttu-id="7f44f-131">記錄</span><span class="sxs-lookup"><span data-stu-id="7f44f-131">Logging</span></span>
    
  - <span data-ttu-id="7f44f-p107">Microsoft Search 流量相關的所有搜尋記錄檔已取消識別和分開儲存公用、 非 Microsoft 搜尋流量。他們保留 18 個月內，並存取僅限於僅適用於偵錯。</span><span class="sxs-lookup"><span data-stu-id="7f44f-p107">All search logs pertaining to Microsoft Search traffic are de-identified and stored separately from public, non-Microsoft Search traffic. They're retained for 18 months, and access is restricted for debugging purposes only.</span></span>
    
  - <span data-ttu-id="7f44f-134">這些記錄檔中的查詢不用以模型或公用功能例如 [自動建議或相關的公用 web 搜尋的訓練。</span><span class="sxs-lookup"><span data-stu-id="7f44f-134">The queries in these logs are not used to model or train public features such as autosuggest or related searches for the public web.</span></span>
    
  - <span data-ttu-id="7f44f-135">透過各種安全的機制，包括安全性群組及工程系統內其他層級管理限制] 存取權。</span><span class="sxs-lookup"><span data-stu-id="7f44f-135">Restricted access is managed via various secure mechanisms, including security groups and other layers within the engineering system.</span></span>
    
- <span data-ttu-id="7f44f-136">搜尋歷程記錄</span><span class="sxs-lookup"><span data-stu-id="7f44f-136">Search history</span></span>
    
  - <span data-ttu-id="7f44f-137">登入工作或學校帳戶，當使用者搜尋歷程記錄不會是可在其他電腦或裝置。</span><span class="sxs-lookup"><span data-stu-id="7f44f-137">When signed in with a work or school account, a user's search history won't be available on other computers or devices.</span></span>
    
- <span data-ttu-id="7f44f-138">公告</span><span class="sxs-lookup"><span data-stu-id="7f44f-138">Advertising</span></span>
    
  - <span data-ttu-id="7f44f-139">企業搜尋查詢不會與共用或建議的廣告。</span><span class="sxs-lookup"><span data-stu-id="7f44f-139">Enterprise search queries are never shared with or suggested to advertisers.</span></span>
    
  - <span data-ttu-id="7f44f-140">公用流量會分開儲存到 Microsoft 搜尋相關的搜尋 Ads 記錄。</span><span class="sxs-lookup"><span data-stu-id="7f44f-140">Search Ads logs pertaining to Microsoft Search are stored separately from public traffic.</span></span>
    
  - <span data-ttu-id="7f44f-141">Ads 永遠不會針對取決於其公司身分識別或組織的使用者。</span><span class="sxs-lookup"><span data-stu-id="7f44f-141">Ads are never targeted to a user based on their work identity or organization.</span></span>
    
## <a name="gdpr"></a><span data-ttu-id="7f44f-142">GDPR</span><span class="sxs-lookup"><span data-stu-id="7f44f-142">GDPR</span></span>

<span data-ttu-id="7f44f-p108">[2018 年 5 月 21、 部落格張貼](https://blogs.microsoft.com/on-the-issues/2018/05/21/microsofts-commitment-to-gdpr-privacy-and-putting-customers-in-control-of-their-own-data/)microsoft 反映 GDPR 規範我們承諾和 Microsoft 如何協助企業和自己 GDPR 規範義務也提供組織。您可以在 Microsoft[信任中心常見問題集](https://www.microsoft.com/en-us/trustcenter/privacy/gdpr/gdpr-faqs)找到其他的詳細資訊。針對內線上服務的組織客戶的客戶資料操作的 Microsoft 搜尋查詢也將符合述反映在[信任中心常見問題集](https://www.microsoft.com/en-us/trustcenter/privacy/gdpr/gdpr-faqs)文章 28 處理器承諾。表示從 Microsoft Search 移至 [公用 Bing 的查詢，Microsoft 資料控制站與實作以取消識別查詢如底下 GDPR 所述的量值。</span><span class="sxs-lookup"><span data-stu-id="7f44f-p108">The [May 21, 2018, blog post](https://blogs.microsoft.com/on-the-issues/2018/05/21/microsofts-commitment-to-gdpr-privacy-and-putting-customers-in-control-of-their-own-data/) from Microsoft reflects our commitment to GDPR compliance and how Microsoft helps businesses and organizations with their own GDPR compliance obligations. You can find additional detail in the Microsoft [Trust Center FAQ](https://www.microsoft.com/en-us/trustcenter/privacy/gdpr/gdpr-faqs). Microsoft Search queries that operate against organizational customers' Customer Data within the Online Services will also meet the processor commitments outlined in Article 28 as reflected in the [Trust Center FAQ](https://www.microsoft.com/en-us/trustcenter/privacy/gdpr/gdpr-faqs). With respect to queries from Microsoft Search that go to public Bing, Microsoft is a data controller and has implemented measures to de-identify the queries as outlined under GDPR.</span></span>


