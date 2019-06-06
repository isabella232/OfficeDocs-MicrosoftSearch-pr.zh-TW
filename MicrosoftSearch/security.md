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
# <a name="security-for-microsoft-search"></a><span data-ttu-id="360a0-103">Microsoft Search 的安全性</span><span class="sxs-lookup"><span data-stu-id="360a0-103">Security for Microsoft Search</span></span>

<span data-ttu-id="360a0-104">透過企業級的安全性，Microsoft Search 可隨時保護您的使用者與資料。</span><span class="sxs-lookup"><span data-stu-id="360a0-104">With enterprise-grade security, Microsoft Search always keeps your users and data protected.</span></span>


## <a name="secure-by-default"></a><span data-ttu-id="360a0-105">預設安全性</span><span class="sxs-lookup"><span data-stu-id="360a0-105">Secure by default</span></span>

<span data-ttu-id="360a0-106">Microsoft Search 能隨時確保提出的要求皆透過 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="360a0-106">Microsoft Search always ensures requests are made over HTTPS.</span></span> <span data-ttu-id="360a0-107">這道保護能確保連線受到端點對端點加密，強化安全性。</span><span class="sxs-lookup"><span data-stu-id="360a0-107">This safeguard ensures the connection is encrypted end-to-end for enhanced security.</span></span>
  
## <a name="authentication-and-authorization-with-azure-active-directory"></a><span data-ttu-id="360a0-108">搭配 Azure Active Directory 的驗證與授權</span><span class="sxs-lookup"><span data-stu-id="360a0-108">Authentication and authorization with Azure Active Directory</span></span>

<span data-ttu-id="360a0-109">Microsoft Search 的驗證已綁定至 Azure Active Directory。</span><span class="sxs-lookup"><span data-stu-id="360a0-109">Authentication for Microsoft Search is tied to Azure Active Directory.</span></span> <span data-ttu-id="360a0-110">當 Microsoft Search 使用者前往 Bing，Bing 標頭會顯示 Microsoft 帳戶以及公司或學校帳戶的登入選項。</span><span class="sxs-lookup"><span data-stu-id="360a0-110">When Microsoft Search users go to Bing, the Bing header will show sign-in options for a Microsoft account as well as a work or school account.</span></span> <span data-ttu-id="360a0-111">如果 Bing 無法判斷使用者是否為合格的參與者，使用者可以移至[探索 Microsoft Search](https://www.bing.com/business/explore) 頁面，該頁面會自動將使用者重新導向至組織的登入頁面。</span><span class="sxs-lookup"><span data-stu-id="360a0-111">If Bing can't determine whether a user is an eligible participant, users can go to the [Explore Microsoft Search](https://www.bing.com/business/explore) page, where they'll be automatically redirected to your organization's sign-in page.</span></span> 
  
<span data-ttu-id="360a0-112">使用者僅能透過公司或學校帳戶存取 Microsoft Search。</span><span class="sxs-lookup"><span data-stu-id="360a0-112">Users can access Microsoft Search only through a work or school account.</span></span> <span data-ttu-id="360a0-113">若要登入，他們必須使用與存取 Office 365 服務 (例如 SharePoint 或 Outlook) 相同的認證。</span><span class="sxs-lookup"><span data-stu-id="360a0-113">They need to sign in with the same credentials they use to access Office 365 services such as SharePoint or Outlook.</span></span> <span data-ttu-id="360a0-114">個人 Microsoft 帳戶無法用來登入 Microsoft Search。</span><span class="sxs-lookup"><span data-stu-id="360a0-114">A personal Microsoft account can't be used to sign in to Microsoft Search.</span></span>
  
<span data-ttu-id="360a0-115">使用者無法同時使用 Microsoft 帳戶和公司或學校帳戶登入 Bing。</span><span class="sxs-lookup"><span data-stu-id="360a0-115">Users can't be signed in to Bing with both a Microsoft account and a work or school account at the same time.</span></span>
  
## <a name="single-sign-on"></a><span data-ttu-id="360a0-116">單一登入</span><span class="sxs-lookup"><span data-stu-id="360a0-116">Single sign-on</span></span>

<span data-ttu-id="360a0-117">如果使用者已在其他服務 (例如 Outlook 或 SharePoint) 中以公司或學校帳戶通過驗證，那當他們在同個瀏覽器中移至 Bing 時，系統便會自動登入 Microsoft Search。</span><span class="sxs-lookup"><span data-stu-id="360a0-117">If a user is already authenticated with their work or school account in another service, such as Outlook or SharePoint, they'll be automatically signed in to Microsoft Search when they go to Bing in the same browser.</span></span> <span data-ttu-id="360a0-118">此外，如果使用者登出 Microsoft Search，系統也會自動當他們登出其他服務。</span><span class="sxs-lookup"><span data-stu-id="360a0-118">Also, when the user signs out of Microsoft Search, they'll be automatically signed out from other services in the same browser.</span></span>
  
## <a name="communicates-with-the-trusted-cloud-from-the-browser"></a><span data-ttu-id="360a0-119">從瀏覽器使用 Trusted Cloud 進行通訊</span><span class="sxs-lookup"><span data-stu-id="360a0-119">Communicates with the Trusted Cloud from the browser</span></span>

<span data-ttu-id="360a0-120">當使用者以公司或學校帳戶登入時，Bing 會在瀏覽器中下載所需的用戶端資料庫，以取得 Microsoft Search 結果。</span><span class="sxs-lookup"><span data-stu-id="360a0-120">When a user signs in with their work or school account, Bing will download the necessary client libraries to the browser to enable Microsoft Search results.</span></span> <span data-ttu-id="360a0-121">隨後，當他們搜尋時，瀏覽器內的程式碼會呼叫 Office 365 雲端，以取得工作結果。</span><span class="sxs-lookup"><span data-stu-id="360a0-121">Then, when they search, the in-browser code calls the Office 365 cloud to get work results.</span></span> <span data-ttu-id="360a0-122">為了執行這項程序，Microsoft Search 會使用專門的 API 層級 C (SOC2 類型 1)，為[符合 Office 365 產業標準和法規的合規性架構](https://download.microsoft.com/download/B/2/7/B27B3EF3-8849-4C18-8BA4-5AD755728620/Compliance%20Framework_customer%20guidance.pdf) (下載 PDF)。</span><span class="sxs-lookup"><span data-stu-id="360a0-122">To do this, Microsoft Search uses a dedicated API that is Tier C (SOC2 Type 1) compliant pursuant to the Office 365 [Compliance Framework for Industry Standards and Regulations](https://download.microsoft.com/download/B/2/7/B27B3EF3-8849-4C18-8BA4-5AD755728620/Compliance%20Framework_customer%20guidance.pdf) (PDF download).</span></span> <span data-ttu-id="360a0-123">這表示工作結果與工作資料永遠不會流經不符合規範的 Bing 系統。</span><span class="sxs-lookup"><span data-stu-id="360a0-123">This means work results and work data never flow through non-compliant Bing systems.</span></span> 
  
## <a name="permissions"></a><span data-ttu-id="360a0-124">權限</span><span class="sxs-lookup"><span data-stu-id="360a0-124">Permissions</span></span>

<span data-ttu-id="360a0-125">從 Office 365 工作負載 (例如 SharePoint 和商務用 OneDrive) 擷取的工作結果，都會在來源經過適當的安全性調整。</span><span class="sxs-lookup"><span data-stu-id="360a0-125">Work results retrieved from Office 365 workloads such as SharePoint and OneDrive for Business are security trimmed at the source.</span></span> <span data-ttu-id="360a0-126">使用者無法看到像是 Word 文件或 PowerPoint 簡報這類透過 Office 365 檢視或存取的來源。</span><span class="sxs-lookup"><span data-stu-id="360a0-126">Users can't see resources such as Word documents or PowerPoint presentations they can't see and access through Office 365.</span></span> <span data-ttu-id="360a0-127">使用者只能查看自己的檔案，以及由作者在 SharePoint 中明確或隱含地 (例如透過群組資格) 與他們共用的檔案。</span><span class="sxs-lookup"><span data-stu-id="360a0-127">They can only see their own files and files that have been shared with them by the author explicitly or implicitly (through a group membership, for example) in SharePoint.</span></span>
  
## <a name="protects-user-queries-from-the-public-portion-of-bing"></a><span data-ttu-id="360a0-128">保護使用者查詢不列入 Bing 的公開部分</span><span class="sxs-lookup"><span data-stu-id="360a0-128">Protects user queries from the public portion of Bing</span></span>

<span data-ttu-id="360a0-129">由於工作相關的搜尋可能具敏感性質，Microsoft Search 針對 Bing 的公開網頁結果施行一套信任標準以處理這些搜尋。</span><span class="sxs-lookup"><span data-stu-id="360a0-129">Because work-related searches may be sensitive, Microsoft Search has implemented a set of trust measures for how these are handled by the public web results part of Bing.</span></span>
  
<span data-ttu-id="360a0-130">不論使用者查詢傳回的回應中是否包含一或多個工作結果，系統都會採取下列措施：</span><span class="sxs-lookup"><span data-stu-id="360a0-130">Regardless of whether a user query contains one or more work results in the returned response, the following measures are taken:</span></span>
  
- <span data-ttu-id="360a0-131">記錄</span><span class="sxs-lookup"><span data-stu-id="360a0-131">Logging on</span></span>
    
  - <span data-ttu-id="360a0-132">所有與 Microsoft Search 流量相關的搜尋記錄都會在去除身分識別後，與公開的非 Microsoft Search 流量分開儲存。</span><span class="sxs-lookup"><span data-stu-id="360a0-132">All search logs pertaining to Microsoft Search traffic are de-identified and stored separately from public, non-Microsoft Search traffic.</span></span> <span data-ttu-id="360a0-133">這些記錄會保留 18 個月，且限制為僅供偵錯之用。</span><span class="sxs-lookup"><span data-stu-id="360a0-133">They're retained for 18 months, and access is restricted for debugging purposes only.</span></span>
    
  - <span data-ttu-id="360a0-134">這些記錄中的查詢不會用來建立公開功能模型或進行訓練，例如自動建議或公開網頁的相關搜尋。</span><span class="sxs-lookup"><span data-stu-id="360a0-134">The queries in these logs are not used to model or train public features such as autosuggest or related searches for the public web.</span></span>
    
  - <span data-ttu-id="360a0-135">限制存取會透過各種安全機制來管理，包括安全性群組與工程系統中的其他層級。</span><span class="sxs-lookup"><span data-stu-id="360a0-135">Restricted access is managed via various secure mechanisms, including security groups and other layers within the engineering system.</span></span>
    
- <span data-ttu-id="360a0-136">搜尋記錄</span><span class="sxs-lookup"><span data-stu-id="360a0-136">Search history</span></span>
    
  - <span data-ttu-id="360a0-137">使用公司或學校帳戶登入時，其他電腦或裝置無法獲得該使用者的搜尋記錄。</span><span class="sxs-lookup"><span data-stu-id="360a0-137">When signed in with a work or school account, a user's search history won't be available on other computers or devices.</span></span>
    
- <span data-ttu-id="360a0-138">廣告</span><span class="sxs-lookup"><span data-stu-id="360a0-138">Advertising</span></span>
    
  - <span data-ttu-id="360a0-139">絕不會將企業搜尋查詢與廣告客戶分享或建議給廣告客戶。</span><span class="sxs-lookup"><span data-stu-id="360a0-139">Enterprise search queries are never shared with or suggested to advertisers.</span></span>
    
  - <span data-ttu-id="360a0-140">與 Microsoft Search 有關的搜尋廣告記錄會與公開流量分開儲存。</span><span class="sxs-lookup"><span data-stu-id="360a0-140">Search Ads logs pertaining to Microsoft Search are stored separately from public traffic.</span></span>
    
  - <span data-ttu-id="360a0-141">廣告永遠不會依據使用者的公司身分識別或組織進行投放。</span><span class="sxs-lookup"><span data-stu-id="360a0-141">Ads are never targeted to a user based on their work identity or organization.</span></span>
    
## <a name="gdpr"></a><span data-ttu-id="360a0-142">GDPR</span><span class="sxs-lookup"><span data-stu-id="360a0-142">GDPR</span></span>

<span data-ttu-id="360a0-143">Microsoft 在[ 2018 年 5 月 21 日的部落格文章](https://blogs.microsoft.com/on-the-issues/2018/05/21/microsofts-commitment-to-gdpr-privacy-and-putting-customers-in-control-of-their-own-data/)反映了我們對 GDPR 規範，以及 Microsoft 會如何協助企業與組織履行 GDPR 合規性義務的承諾。</span><span class="sxs-lookup"><span data-stu-id="360a0-143">The [May 21, 2018, blog post](https://blogs.microsoft.com/on-the-issues/2018/05/21/microsofts-commitment-to-gdpr-privacy-and-putting-customers-in-control-of-their-own-data/) from Microsoft reflects our commitment to GDPR compliance and how Microsoft helps businesses and organizations with their own GDPR compliance obligations.</span></span> <span data-ttu-id="360a0-144">您可以在 Microsoft [信任中心常見問題集](https://www.microsoft.com/en-us/trustcenter/privacy/gdpr/gdpr-faqs)中找到其他詳細資料。</span><span class="sxs-lookup"><span data-stu-id="360a0-144">You can find additional detail in the Microsoft [Trust Center FAQ](https://www.microsoft.com/en-us/trustcenter/privacy/gdpr/gdpr-faqs).</span></span> <span data-ttu-id="360a0-145">在線上服務中針對組織客戶的客戶資料進行 Microsoft Search 查詢，也會符合第 28 條所述的處理承諾，如[信任中心常見問題集](https://www.microsoft.com/en-us/trustcenter/privacy/gdpr/gdpr-faqs)中所反映。</span><span class="sxs-lookup"><span data-stu-id="360a0-145">Microsoft Search queries that operate against organizational customers' Customer Data within the Online Services will also meet the processor commitments outlined in Article 28 as reflected in the [Trust Center FAQ](https://www.microsoft.com/en-us/trustcenter/privacy/gdpr/gdpr-faqs).</span></span> <span data-ttu-id="360a0-146">針對移至公開 Bing 查詢 (來自 Microsoft Search)，Microsoft 為資料控制者，並會依照 GDPR 中所述，去除查詢的身分識別。</span><span class="sxs-lookup"><span data-stu-id="360a0-146">With respect to queries from Microsoft Search that go to public Bing, Microsoft is a data controller and has implemented measures to de-identify the queries as outlined under GDPR.</span></span>


