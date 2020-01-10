---
title: 安全性和 Microsoft 中的搜尋 Bing 的隱私權
ms.author: jeffkizn
author: jeffkizn
manager: pmanek
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 提供資訊給授權的使用者與 Microsoft Search in Bing 時保護您的公司資料和使用者
ms.openlocfilehash: 7f19327f3d62f68ed876875596610181b5f1bc0e
ms.sourcegitcommit: ac1209d11b8cc265d2224917fbe2a2bb0f65ef84
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/10/2020
ms.locfileid: "41005619"
---
# <a name="security-and-privacy-for-microsoft-search-in-bing"></a><span data-ttu-id="c7fb1-103">安全性和 Microsoft 中的搜尋 Bing 的隱私權</span><span class="sxs-lookup"><span data-stu-id="c7fb1-103">Security and Privacy for Microsoft Search in Bing</span></span>

<span data-ttu-id="c7fb1-104">具有增強的隱私權和安全性措施，Microsoft Search in Bing 可協助保護您的使用者與工作場所資料。</span><span class="sxs-lookup"><span data-stu-id="c7fb1-104">With enhanced privacy and security measures, Microsoft Search in Bing helps protect your users and workplace data.</span></span>

## <a name="secure-by-default"></a><span data-ttu-id="c7fb1-105">預設安全性</span><span class="sxs-lookup"><span data-stu-id="c7fb1-105">Secure by default</span></span>

<span data-ttu-id="c7fb1-106">Microsoft Search 的 Bing 要求進行透過 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="c7fb1-106">Microsoft Search in Bing requests are made over HTTPS.</span></span> <span data-ttu-id="c7fb1-107">連線是加密的端對端以增強安全性。</span><span class="sxs-lookup"><span data-stu-id="c7fb1-107">The connection is encrypted end-to-end for enhanced security.</span></span>
  
## <a name="authentication-and-authorization-with-azure-active-directory"></a><span data-ttu-id="c7fb1-108">搭配 Azure Active Directory 的驗證與授權</span><span class="sxs-lookup"><span data-stu-id="c7fb1-108">Authentication and authorization with Azure Active Directory</span></span>

<span data-ttu-id="c7fb1-109">Microsoft 中的搜尋 Bing 驗證是繫結至 Azure Active Directory。</span><span class="sxs-lookup"><span data-stu-id="c7fb1-109">Authentication for Microsoft Search in Bing is tied to Azure Active Directory.</span></span> <span data-ttu-id="c7fb1-110">當 Microsoft Search 使用者前往 Bing，Bing 標頭會顯示 Microsoft 帳戶以及公司或學校帳戶的登入選項。</span><span class="sxs-lookup"><span data-stu-id="c7fb1-110">When Microsoft Search users go to Bing, the Bing header will show sign-in options for a Microsoft account as well as a work or school account.</span></span> <span data-ttu-id="c7fb1-111">如果 Bing 無法判斷使用者是否為合格的參與者，使用者可以移至[探索 Microsoft Search](https://www.bing.com/business/explore) 頁面，該頁面會自動將使用者重新導向至組織的登入頁面。</span><span class="sxs-lookup"><span data-stu-id="c7fb1-111">If Bing can't determine whether a user is an eligible participant, users can go to the [Explore Microsoft Search](https://www.bing.com/business/explore) page, where they'll be automatically redirected to your organization's sign-in page.</span></span>

<span data-ttu-id="c7fb1-112">使用者僅能透過公司或學校帳戶存取 Microsoft Search。</span><span class="sxs-lookup"><span data-stu-id="c7fb1-112">Users can access Microsoft Search only through a work or school account.</span></span> <span data-ttu-id="c7fb1-113">若要登入，他們必須使用與存取 Office 365 服務 (例如 SharePoint 或 Outlook) 相同的認證。</span><span class="sxs-lookup"><span data-stu-id="c7fb1-113">They need to sign in with the same credentials they use to access Office 365 services such as SharePoint or Outlook.</span></span> <span data-ttu-id="c7fb1-114">個人 Microsoft 帳戶無法用來登入 Microsoft Search。</span><span class="sxs-lookup"><span data-stu-id="c7fb1-114">A personal Microsoft account can't be used to sign in to Microsoft Search.</span></span>

## <a name="single-sign-on"></a><span data-ttu-id="c7fb1-115">單一登入</span><span class="sxs-lookup"><span data-stu-id="c7fb1-115">Single sign-on</span></span>

<span data-ttu-id="c7fb1-116">使用者已驗證與其他服務，例如 Outlook 或 SharePoint 中其公司或學校帳戶，則他們將會自動登入相同的公司或學校帳戶時他們在相同的瀏覽器中前往 Bing。</span><span class="sxs-lookup"><span data-stu-id="c7fb1-116">If a user is already authenticated with their work or school account in another service, such as Outlook or SharePoint, they'll be automatically signed into the same work or school account when they go to Bing in the same browser.</span></span> <span data-ttu-id="c7fb1-117">此外，當使用者已超出其公司或學校帳戶，他們將會自動登出從相同的瀏覽器中其他 Microsoft Office 服務。</span><span class="sxs-lookup"><span data-stu-id="c7fb1-117">Also, when the user signs out of their work or school account, they'll be automatically signed out from other Microsoft Office services in the same browser.</span></span>
  
## <a name="communicates-with-the-microsoft-cloud-from-the-browser"></a><span data-ttu-id="c7fb1-118">從瀏覽器的 Microsoft 雲端進行通訊</span><span class="sxs-lookup"><span data-stu-id="c7fb1-118">Communicates with the Microsoft cloud from the browser</span></span>

<span data-ttu-id="c7fb1-119">當使用者以公司或學校帳戶登入時，Bing 會在瀏覽器中下載所需的用戶端資料庫，以取得 Microsoft Search 結果。</span><span class="sxs-lookup"><span data-stu-id="c7fb1-119">When a user signs in with their work or school account, Bing will download the necessary client libraries to the browser to enable Microsoft Search results.</span></span> <span data-ttu-id="c7fb1-120">隨後，當他們搜尋時，瀏覽器內的程式碼會呼叫 Office 365 雲端，以取得工作結果。</span><span class="sxs-lookup"><span data-stu-id="c7fb1-120">Then, when they search, the in-browser code calls the Office 365 cloud to get work results.</span></span> <span data-ttu-id="c7fb1-121">為了執行這項程序，Microsoft Search 會使用專門的 API 層級 C (SOC2 類型 1)，為[符合 Office 365 產業標準和法規的合規性架構](https://download.microsoft.com/download/1/4/3/1434ABAB-B8E9-412D-8C3A-187B5FCB7A2F/Compliance%20Framework%20document.pdf) (下載 PDF)。</span><span class="sxs-lookup"><span data-stu-id="c7fb1-121">To do this, Microsoft Search uses a dedicated API that is Tier C (SOC2 Type 1) compliant pursuant to the Office 365 [Compliance Framework for Industry Standards and Regulations](https://download.microsoft.com/download/1/4/3/1434ABAB-B8E9-412D-8C3A-187B5FCB7A2F/Compliance%20Framework%20document.pdf) (PDF download).</span></span> <span data-ttu-id="c7fb1-122">這表示工作結果與工作資料永遠不會流經不符合規範的 Bing 系統。</span><span class="sxs-lookup"><span data-stu-id="c7fb1-122">This means work results and work data never flow through non-compliant Bing systems.</span></span>
  
## <a name="permissions"></a><span data-ttu-id="c7fb1-123">權限</span><span class="sxs-lookup"><span data-stu-id="c7fb1-123">Permissions</span></span>

<span data-ttu-id="c7fb1-124">從 Office 365 工作負載 (例如 SharePoint 和商務用 OneDrive) 擷取的工作結果，都會在來源經過適當的安全性調整。</span><span class="sxs-lookup"><span data-stu-id="c7fb1-124">Work results retrieved from Office 365 workloads such as SharePoint and OneDrive for Business are security trimmed at the source.</span></span> <span data-ttu-id="c7fb1-125">使用者無法看到像是 Word 文件或 PowerPoint 簡報這類透過 Office 365 檢視或存取的來源。</span><span class="sxs-lookup"><span data-stu-id="c7fb1-125">Users can't see resources such as Word documents or PowerPoint presentations they can't see and access through Office 365.</span></span> <span data-ttu-id="c7fb1-126">使用者只能查看自己的檔案，以及由作者在 SharePoint 中明確或隱含地 (例如透過群組資格) 與他們共用的檔案。</span><span class="sxs-lookup"><span data-stu-id="c7fb1-126">They can only see their own files and files that have been shared with them by the author explicitly or implicitly (through a group membership, for example) in SharePoint.</span></span>

## <a name="microsoft-search-in-bing-protects-workplace-searches"></a><span data-ttu-id="c7fb1-127">Microsoft Search in Bing 保護工作場所搜尋</span><span class="sxs-lookup"><span data-stu-id="c7fb1-127">Microsoft Search in Bing protects workplace searches</span></span>

<span data-ttu-id="c7fb1-128">當使用者在 Microsoft Bing 搜尋中，輸入搜尋查詢時，會發生兩個同時搜尋要求：</span><span class="sxs-lookup"><span data-stu-id="c7fb1-128">When a user enters a search query in Microsoft Search in Bing, two simultaneous search requests occur:</span></span>

- <span data-ttu-id="c7fb1-129">您的組織內部資源搜尋。</span><span class="sxs-lookup"><span data-stu-id="c7fb1-129">A search of your organization’s internal resources.</span></span>
- <span data-ttu-id="c7fb1-130">從 Bing.com 公開的個別搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="c7fb1-130">A separate search of public results from Bing.com.</span></span>

<span data-ttu-id="c7fb1-131">因為工作場所搜尋可能是機密的所以 Microsoft Search 已實作一群說明如何處理來自 Bing.com 公用結果的個別搜尋的信任量值。</span><span class="sxs-lookup"><span data-stu-id="c7fb1-131">Because workplace searches might be sensitive, Microsoft Search has implemented a set of trust measures that describe how the separate search of public results from Bing.com is handled.</span></span>

### <a name="logging"></a><span data-ttu-id="c7fb1-132">記錄</span><span class="sxs-lookup"><span data-stu-id="c7fb1-132">Logging</span></span>

- <span data-ttu-id="c7fb1-133">適用於 Microsoft Search 的 Bing 流量的所有 Bing.com 搜尋記錄會與您的工作場所身分識別解除都關聯。</span><span class="sxs-lookup"><span data-stu-id="c7fb1-133">All Bing.com search logs that pertain to Microsoft Search in Bing traffic are disassociated from your workplace identity.</span></span>
- <span data-ttu-id="c7fb1-134">如果符合一組限制或頻率閾值讓我們信賴查詢不是專屬於特定的組織，查詢會被視為[隱私權聲明](https://privacy.microsoft.com/privacystatement)搜尋和人工地智慧一節所述。</span><span class="sxs-lookup"><span data-stu-id="c7fb1-134">If a set of restrictions or frequency thresholds are met which give us confidence that the query is not specific to a particular organization, the query will be treated as described in the Search and artificial intelligence section of the [Privacy Statement](https://privacy.microsoft.com/privacystatement).</span></span> <span data-ttu-id="c7fb1-135">例如，這類查詢將用來建立模型和訓練公用功能，例如 [自動建議或相關的搜尋。</span><span class="sxs-lookup"><span data-stu-id="c7fb1-135">For example, such queries will be used to model and train public features, such as autosuggest or related searches.</span></span>
- <span data-ttu-id="c7fb1-136">不符合這組限制或頻率閾值的查詢，將會與公開的非 Microsoft Search 流量分開儲存。</span><span class="sxs-lookup"><span data-stu-id="c7fb1-136">Queries that do not meet the set of restrictions or frequency thresholds will be stored separately from public, non-Microsoft Search traffic.</span></span>

### <a name="advertising"></a><span data-ttu-id="c7fb1-137">廣告</span><span class="sxs-lookup"><span data-stu-id="c7fb1-137">Advertising</span></span>

<span data-ttu-id="c7fb1-138">工作場所搜尋與 Bing.com 上顯示的廣告察覺與搜尋查詢的內容。</span><span class="sxs-lookup"><span data-stu-id="c7fb1-138">Advertising shown on Bing.com in connection with workplace searches is solely related to the content of the search queries.</span></span> <span data-ttu-id="c7fb1-139">廣告永遠不會根據使用者的工作場所身分識別來鎖定使用者。</span><span class="sxs-lookup"><span data-stu-id="c7fb1-139">Ads are never targeted to users based on their workplace identity.</span></span>

## <a name="gdpr"></a><span data-ttu-id="c7fb1-140">GDPR</span><span class="sxs-lookup"><span data-stu-id="c7fb1-140">GDPR</span></span>

<span data-ttu-id="c7fb1-141">Microsoft 在[ 2018 年 5 月 21 日的部落格文章](https://blogs.microsoft.com/on-the-issues/2018/05/21/microsofts-commitment-to-gdpr-privacy-and-putting-customers-in-control-of-their-own-data/)反映了我們對 GDPR 規範，以及 Microsoft 會如何協助企業與組織履行 GDPR 合規性義務的承諾。</span><span class="sxs-lookup"><span data-stu-id="c7fb1-141">The [May 21, 2018, blog post](https://blogs.microsoft.com/on-the-issues/2018/05/21/microsofts-commitment-to-gdpr-privacy-and-putting-customers-in-control-of-their-own-data/) from Microsoft reflects our commitment to GDPR compliance and how Microsoft helps businesses and organizations with their own GDPR compliance obligations.</span></span> <span data-ttu-id="c7fb1-142">您可以在 Microsoft [信任中心常見問題集](https://www.microsoft.com/trustcenter/privacy/gdpr/gdpr-faqs)中找到其他詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c7fb1-142">You can find additional detail in the Microsoft [Trust Center FAQ](https://www.microsoft.com/trustcenter/privacy/gdpr/gdpr-faqs).</span></span>

<span data-ttu-id="c7fb1-143">針對客戶的內部資源執行的 Microsoft 搜尋查詢和傳回的結果會被視為客戶資料，因此也符合為反映在[信任中心常見問題集](https://www.microsoft.com/trustcenter/privacy/gdpr/gdpr-faqs)28 中所述的處理器承諾。</span><span class="sxs-lookup"><span data-stu-id="c7fb1-143">Microsoft Search queries executed against a customer’s internal resources and results returned are considered Customer Data and, as such, also  meet the processor commitments outlined in Article 28 as reflected in the [Trust Center FAQ](https://www.microsoft.com/trustcenter/privacy/gdpr/gdpr-faqs).</span></span> <span data-ttu-id="c7fb1-144">關於移至公用 Bing 從 Microsoft 搜尋查詢，Microsoft 遵守其 GDPR 義務資料控制者身分。</span><span class="sxs-lookup"><span data-stu-id="c7fb1-144">With respect to queries from Microsoft Search that go to public Bing, Microsoft complies with its GDPR obligations as a data controller.</span></span>
