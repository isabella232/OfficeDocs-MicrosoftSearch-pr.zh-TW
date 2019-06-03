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
ROBOTS: NoIndex
description: 取得有關企業搜尋和 Microsoft Search 常見問題的解答
ms.openlocfilehash: 58fb45eec5cc354a6228fb552a3dcda28c2b2367
ms.sourcegitcommit: be2e837d9b087bffe6ce40d72d7ae58a8fcdf3fe
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/30/2019
ms.locfileid: "34591501"
---
# <a name="faqs"></a><span data-ttu-id="d8295-103">常見問題集</span><span class="sxs-lookup"><span data-stu-id="d8295-103">FAQs</span></span>

<span data-ttu-id="d8295-104">這裡是組織和使用者對系統管理與使用 Microsoft Search 會有的常見問題集。</span><span class="sxs-lookup"><span data-stu-id="d8295-104">These are the frequently asked questions that organizations and users have about administering and using Microsoft Search.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d8295-105">本文章適用 Bing 系統管理入口網站中的 Microsoft Search。</span><span class="sxs-lookup"><span data-stu-id="d8295-105">This article applies to the Microsoft Search in Bing admin portal.</span></span> <span data-ttu-id="d8295-106">我們正在將入口網站移至 Microsoft 365 系統管理中心，完成之後入口網站將會移除。</span><span class="sxs-lookup"><span data-stu-id="d8295-106">We’re moving the portal to the Microsoft 365 admin center, and then it will be removed.</span></span> <span data-ttu-id="d8295-107">我們建議您使用 Microsoft 365 系統管理中心開始。</span><span class="sxs-lookup"><span data-stu-id="d8295-107">We recommend that you use the Microsoft 365 admin center to get started.</span></span> <span data-ttu-id="d8295-108">[Microsoft Search 概觀](overview-microsoft-search.md)。</span><span class="sxs-lookup"><span data-stu-id="d8295-108">[Overview of Microsoft Graph](overview-microsoft-search.md)</span></span>
  
## <a name="whats-the-value-proposition-for-microsoft-search"></a><span data-ttu-id="d8295-109">Microsoft Search 主張的價值是什麼？</span><span class="sxs-lookup"><span data-stu-id="d8295-109">What's the value proposition for Microsoft Search?</span></span>

<span data-ttu-id="d8295-110">Microsoft Search 是一種能同時安全地搜尋您工作與網路內容的方式。</span><span class="sxs-lookup"><span data-stu-id="d8295-110">Microsoft Search is a secure way to search both your work and web content.</span></span> <span data-ttu-id="d8295-111">只有 Microsoft 能夠提供這種跨網路與企業間的整合產品。</span><span class="sxs-lookup"><span data-stu-id="d8295-111">This kind of integration across web and enterprise is only available with Microsoft.</span></span> <span data-ttu-id="d8295-112">如需關於合規性的資訊，請參閱 [Microsoft Search 的安全性](security.md)。</span><span class="sxs-lookup"><span data-stu-id="d8295-112">For compliance-related information, see [Security for Microsoft Search](security.md).</span></span>
  
## <a name="what-microsoft-search-features-are-available-now"></a><span data-ttu-id="d8295-113">現在可使用 Microsoft Search 的哪些功能？</span><span class="sxs-lookup"><span data-stu-id="d8295-113">What Microsoft Search features are available now?</span></span>

<span data-ttu-id="d8295-114">如需完整清單，請參閱 [Microsoft Search 的功能](features.md)。</span><span class="sxs-lookup"><span data-stu-id="d8295-114">For a complete list, see [Features of Microsoft Search](features.md).</span></span>
  
## <a name="does-microsoft-search-support-advanced-query-understanding"></a><span data-ttu-id="d8295-115">Microsoft Search 是否支援進階查詢理解？</span><span class="sxs-lookup"><span data-stu-id="d8295-115">Does Microsoft Search support advanced query understanding?</span></span>

<span data-ttu-id="d8295-116">是的，Microsoft Search 會從較大的片語去剖析您的查詢意圖。</span><span class="sxs-lookup"><span data-stu-id="d8295-116">Yes, Microsoft Search parses query intent from larger phrases.</span></span> <span data-ttu-id="d8295-117">此功能會使用 AI 以學習將常用多餘片語的使用者新增到查詢，但不影響使用者的搜尋意圖。</span><span class="sxs-lookup"><span data-stu-id="d8295-117">This feature uses AI to learn common superfluous phrases users add to their queries that don't impact their search intent.</span></span> <span data-ttu-id="d8295-118">舉例來說，當使用者搜尋「告訴我如何變更密碼」，我們會截掉查詢中較不重要的字詞，並依據較相關的項目 (例如「變更密碼」) 來進行觸發。</span><span class="sxs-lookup"><span data-stu-id="d8295-118">For example, when a user searches for 'tell me more about how to change my password please' we extract the less important words from the query and trigger based on the relevant ones like 'change password.'</span></span>
  
<span data-ttu-id="d8295-119">此功能無法覆寫系統管理入口網站中設定的關鍵字。</span><span class="sxs-lookup"><span data-stu-id="d8295-119">This feature will not override keywords set in the Admin portal.</span></span>
  
## <a name="does-microsoft-search-search-for-files-on-premises-as-well-as-the-cloud"></a><span data-ttu-id="d8295-120">Microsoft Search 是否會搜尋內部部署與雲端的檔案？</span><span class="sxs-lookup"><span data-stu-id="d8295-120">Does Microsoft Search search for files on-premises as well as the cloud?</span></span>

<span data-ttu-id="d8295-121">Microsoft Search 支援搜尋存在於 SharePoint Online、商務用 OneDrive 的文件，同時也會搜尋混合式內部部署 SharePoint 與 SharePoint Online，來尋找最常見的 Office 檔案類型。</span><span class="sxs-lookup"><span data-stu-id="d8295-121">Microsoft Search supports searching for documents that live on SharePoint Online, OneDrive for Business, as well as over hybrid on-premises SharePoint and SharePoint Online for the most common Office file types.</span></span> <span data-ttu-id="d8295-122">如果您可以搜尋 SharePoint Online 中的內部部署內容，應該就能使用 Microsoft Search 尋找內部部署內容。</span><span class="sxs-lookup"><span data-stu-id="d8295-122">If you can search on-premises content in SharePoint Online, you should be able to find on-premises content using Microsoft Search.</span></span> 
  
## <a name="does-microsoft-search-replace-other-enterprise-search-experiences"></a><span data-ttu-id="d8295-123">Microsoft Search 是否會取代其他企業搜尋體驗？</span><span class="sxs-lookup"><span data-stu-id="d8295-123">Does Microsoft Search replace other enterprise search experiences?</span></span>

<span data-ttu-id="d8295-124">Microsoft Search 是一項能夠整合多個來源結果的互補供應項目。</span><span class="sxs-lookup"><span data-stu-id="d8295-124">Microsoft Search is a complementary offering that brings together results from multiple sources.</span></span> <span data-ttu-id="d8295-125">如需支援檔案類型與來源的相關資訊，請查看下一個常見問題集。</span><span class="sxs-lookup"><span data-stu-id="d8295-125">For more information about supported file types and sources, see the next FAQ.</span></span>
  
## <a name="what-file-types-and-sources-does-microsoft-search-support"></a><span data-ttu-id="d8295-126">Microsoft Search 支援哪些檔案類型與來源？</span><span class="sxs-lookup"><span data-stu-id="d8295-126">What file types and sources does Microsoft Search support?</span></span>

<span data-ttu-id="d8295-127">我們支援下列內容來源：</span><span class="sxs-lookup"><span data-stu-id="d8295-127">We support the following content sources:</span></span>
  
- <span data-ttu-id="d8295-128">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="d8295-128">SharePoint Online</span></span>
    
- <span data-ttu-id="d8295-129">混合式 SharePoint (內部部署 + SPO)</span><span class="sxs-lookup"><span data-stu-id="d8295-129">Hybrid SharePoint (on-premises + SPO)</span></span>
    
- <span data-ttu-id="d8295-130">商務用 OneDrive</span><span class="sxs-lookup"><span data-stu-id="d8295-130">OneDrive for Business</span></span>
    
<span data-ttu-id="d8295-131">下列檔案類型會顯示於檔案搜尋，並會出現在 [人員] 和 [群組] 的 [檔案] 索引標籤上：</span><span class="sxs-lookup"><span data-stu-id="d8295-131">The following file types are surfaced in file search and appear on the Files tab for People and Groups:</span></span>
  
- <span data-ttu-id="d8295-132">Word</span><span class="sxs-lookup"><span data-stu-id="d8295-132">Word</span></span>
    
- <span data-ttu-id="d8295-133">Excel</span><span class="sxs-lookup"><span data-stu-id="d8295-133">Excel</span></span>
    
- <span data-ttu-id="d8295-134">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="d8295-134">PowerPoint</span></span>
    
- <span data-ttu-id="d8295-135">OneNote</span><span class="sxs-lookup"><span data-stu-id="d8295-135">OneNote</span></span>
    
- <span data-ttu-id="d8295-136">PDF</span><span class="sxs-lookup"><span data-stu-id="d8295-136">PDF</span></span>
    
## <a name="what-compliance-and-trust-measures-are-in-place-for-microsoft-search"></a><span data-ttu-id="d8295-137">Microsoft Search 有哪些合規性和信任措施？</span><span class="sxs-lookup"><span data-stu-id="d8295-137">What compliance and trust measures are in place for Microsoft Search?</span></span>

<span data-ttu-id="d8295-138">如需關於合規性和信任措施的相關資訊，請參閱 [Microsoft Search 的安全性](security.md)。</span><span class="sxs-lookup"><span data-stu-id="d8295-138">For information about compliance and trust measures, see [Security for Microsoft Search](security.md).</span></span>
  
## <a name="where-can-i-get-info-about-office-365-compliance-tierscategories"></a><span data-ttu-id="d8295-139">我可以從哪裡獲得關於 Office 365 合規性層級/類別的資訊？</span><span class="sxs-lookup"><span data-stu-id="d8295-139">Where can I get info about Office 365 compliance tiers/categories?</span></span>

<span data-ttu-id="d8295-140">您可以在[符合產業標準和法規的合規性架構](https://download.microsoft.com/download/B/2/7/B27B3EF3-8849-4C18-8BA4-5AD755728620/Compliance%20Framework_customer%20guidance.pdf) (下載 PDF) 中找到詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d8295-140">Details can be found in the [Compliance Framework for Industry Standards and Regulations](https://download.microsoft.com/download/B/2/7/B27B3EF3-8849-4C18-8BA4-5AD755728620/Compliance%20Framework_customer%20guidance.pdf) (PDF download).</span></span> 
  
## <a name="how-does-microsoft-search-keep-results-secure"></a><span data-ttu-id="d8295-141">Microsoft Search 如何保持結果的安全？</span><span class="sxs-lookup"><span data-stu-id="d8295-141">How does Microsoft Search keep results secure?</span></span>

<span data-ttu-id="d8295-142">如需 Microsoft Search 如何保護結果安全的相關資訊，請參閱 [Microsoft Search 的安全性](security.md)。</span><span class="sxs-lookup"><span data-stu-id="d8295-142">For information about how Microsoft Search keeps your results secure, see [Security for Microsoft Search](security.md).</span></span>
  
## <a name="what-are-the-content-sources-for-the-people-card"></a><span data-ttu-id="d8295-143">人員卡片的內容來源為何？</span><span class="sxs-lookup"><span data-stu-id="d8295-143">What are the content sources for the people card?</span></span>

<span data-ttu-id="d8295-144">人員卡片會從 Azure Active Directory、Exchange Online 和 SharePoint Online 取得資訊。</span><span class="sxs-lookup"><span data-stu-id="d8295-144">The people card derives information from Azure Active Directory, Exchange Online, and SharePoint Online.</span></span>
  
## <a name="do-microsoft-search-users-earn-microsoft-rewards"></a><span data-ttu-id="d8295-145">Microsoft Search 使用者是否會獲得 Microsoft Rewards？</span><span class="sxs-lookup"><span data-stu-id="d8295-145">Do Microsoft Search users earn Microsoft Rewards?</span></span>

<span data-ttu-id="d8295-146">Microsoft Search 的搜尋不會獲得 Rewards 點數，且絕不會與使用者的 Microsoft 帳戶關聯。</span><span class="sxs-lookup"><span data-stu-id="d8295-146">Microsoft Search searches do not earn Rewards points and are never associated with a user's Microsoft account.</span></span>
  
## <a name="does-microsoft-search-respect-existing-file-permissions"></a><span data-ttu-id="d8295-147">Microsoft Search 是否會尊重現有的檔案權限？</span><span class="sxs-lookup"><span data-stu-id="d8295-147">Does Microsoft Search respect existing file permissions?</span></span>

<span data-ttu-id="d8295-148">Microsoft Search 會尊重來源的安全性調整。</span><span class="sxs-lookup"><span data-stu-id="d8295-148">Microsoft Search respects security trimming from the source.</span></span> <span data-ttu-id="d8295-149">使用者只能看到他們有權存取的資訊。</span><span class="sxs-lookup"><span data-stu-id="d8295-149">Users can only see information they have access to.</span></span>
  
## <a name="how-are-user-queries-protected-from-sharing-on-the-web"></a><span data-ttu-id="d8295-150">如何保護使用者查詢不在網路上公開？</span><span class="sxs-lookup"><span data-stu-id="d8295-150">How are user queries protected from sharing on the web?</span></span>

<span data-ttu-id="d8295-151">如需使用者查詢如何受到保護的相關資訊，請參閱 [Microsoft Search 的安全性](security.md)。</span><span class="sxs-lookup"><span data-stu-id="d8295-151">For information about how user queries are protected, see [Security for Microsoft Search](security.md).</span></span>
  
## <a name="what-types-of-advertising-do-microsoft-search-users-see"></a><span data-ttu-id="d8295-152">Microsoft Search 使用者會看到哪類廣告？</span><span class="sxs-lookup"><span data-stu-id="d8295-152">What types of advertising do Microsoft Search users see?</span></span>

<span data-ttu-id="d8295-153">如需廣告的相關資訊，請參閱 [Microsoft Search 的安全性](security.md)。</span><span class="sxs-lookup"><span data-stu-id="d8295-153">For information about advertising, see [Security for Microsoft Search](security.md).</span></span>
  
## <a name="what-are-the-minimum-requirements-to-enable-microsoft-search"></a><span data-ttu-id="d8295-154">必須符合哪些最低需求才能啟用 Microsoft Search？</span><span class="sxs-lookup"><span data-stu-id="d8295-154">What are the minimum requirements to enable Microsoft Search?</span></span>

<span data-ttu-id="d8295-155">如需有關需求的資訊，請參閱 [Microsoft Search 的需求](requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d8295-155">For information about requirements, see [Requirements for Microsoft Search](requirements.md).</span></span>
  
## <a name="how-does-microsoft-search-use-azure-active-directory"></a><span data-ttu-id="d8295-156">Microsoft Search 如何使用 Azure Active Directory？</span><span class="sxs-lookup"><span data-stu-id="d8295-156">How does Microsoft Search use Azure Active Directory?</span></span>

<span data-ttu-id="d8295-157">Microsoft Search 會使用 Azure Active Directory 來驗證和授權對公司資料的存取。</span><span class="sxs-lookup"><span data-stu-id="d8295-157">Microsoft Search uses Azure Active Directory to authenticate and authorize access to your company's data.</span></span> <span data-ttu-id="d8295-158">Microsoft Search 符合跨所有 Microsoft 產品的身分識別處理實務標準。</span><span class="sxs-lookup"><span data-stu-id="d8295-158">Microsoft Search conforms to the identity handling practices standard across all Microsoft products.</span></span> <span data-ttu-id="d8295-159">這表示您的使用者可以透過單一登入以自動登入。</span><span class="sxs-lookup"><span data-stu-id="d8295-159">This means your users may be automatically signed in through single sign-on.</span></span> 
  
## <a name="how-do-i-set-bing-as-the-default-search-provider-for-my-users"></a><span data-ttu-id="d8295-160">我該如何將 Bing 設定為使用者的預設搜尋提供者？</span><span class="sxs-lookup"><span data-stu-id="d8295-160">How do I set Bing as the default search provider for my users?</span></span>

<span data-ttu-id="d8295-161">如需相關資訊，請參閱[設定預設搜尋引擎](set-default-search-engine.md)、[設定預設首頁](set-default-homepage.md)，以及[設定預設瀏覽器](set-default-browser.md)。</span><span class="sxs-lookup"><span data-stu-id="d8295-161">For information about this, see [Set default search engine](set-default-search-engine.md), [Set default homepage](set-default-homepage.md), and [Set default browser](set-default-browser.md).</span></span>
  
## <a name="does-microsoft-search-provide-search-results-across-tenants"></a><span data-ttu-id="d8295-162">Microsoft Search 是否提供跨租用戶的搜尋結果？</span><span class="sxs-lookup"><span data-stu-id="d8295-162">Does Microsoft Search provide search results across tenants?</span></span>

<span data-ttu-id="d8295-163">否，我們不提供跨租用戶或共用租用戶存取。</span><span class="sxs-lookup"><span data-stu-id="d8295-163">No, cross tenant or shared tenant access is not supported.</span></span> 
  
## <a name="where-can-i-get-help-with-keywords-and-reserved-keywords"></a><span data-ttu-id="d8295-164">哪裡可以取得關鍵字與保留關鍵字的說明？</span><span class="sxs-lookup"><span data-stu-id="d8295-164">Where can I get help with keywords and reserved keywords?</span></span>

<span data-ttu-id="d8295-165">如需關鍵字與保留關鍵字的使用資訊，請參閱[規劃內容](plan-your-content.md)。</span><span class="sxs-lookup"><span data-stu-id="d8295-165">For information about using keywords and reserved keywords, see [Plan your content](plan-your-content.md).</span></span>
  
## <a name="which-office-365-skus-are-supported"></a><span data-ttu-id="d8295-166">支援哪些 Office 365 SKU？</span><span class="sxs-lookup"><span data-stu-id="d8295-166">Which Office 365 SKUs are supported?</span></span>

<span data-ttu-id="d8295-167">如需支援 SKU 的相關資訊，請參閱 [Microsoft Search 的需求](requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d8295-167">For information about supported SKUs, see [Requirements for Microsoft Search](requirements.md).</span></span>
  
## <a name="is-microsoft-search-gdpr-compliant"></a><span data-ttu-id="d8295-168">Microsoft Search 是否符合 GDPR 規範？</span><span class="sxs-lookup"><span data-stu-id="d8295-168">Is Microsoft Search GDPR compliant?</span></span>

<span data-ttu-id="d8295-169">如需 GDPR 合規性的相關資訊，請參閱 [Microsoft Search 的安全性](security.md)。</span><span class="sxs-lookup"><span data-stu-id="d8295-169">For information about GDPR compliance, see [Security for Microsoft Search](security.md).</span></span>
  
## <a name="why-am-i-signed-into-bing-automatically"></a><span data-ttu-id="d8295-170">為什麼我會自動登入 Bing？</span><span class="sxs-lookup"><span data-stu-id="d8295-170">Why am I signed into Bing automatically?</span></span>

<span data-ttu-id="d8295-171">Microsoft Search 會在您登入 Office 365 或 Windows 10 時，使用 AAD 單一登入以自動透過您的公司或學校帳戶登入。</span><span class="sxs-lookup"><span data-stu-id="d8295-171">Microsoft Search uses AAD single sign-on to automatically sign you in with your work or school account when you've signed in to an Office 365 app, or Windows 10.</span></span> <span data-ttu-id="d8295-172">您可以隨時登出。</span><span class="sxs-lookup"><span data-stu-id="d8295-172">You can unsubscribe at any time.</span></span>
  
## <a name="what-is-bing-for-business"></a><span data-ttu-id="d8295-173">什麼是商務用 Bing？</span><span class="sxs-lookup"><span data-stu-id="d8295-173">What is Bing for business?</span></span>

<span data-ttu-id="d8295-174">Microsoft Search 先前稱為 Bing for business。</span><span class="sxs-lookup"><span data-stu-id="d8295-174">Microsoft Search was previously called Bing for business.</span></span>
  
## <a name="how-does-microsoft-search-order-result-cards-in-the-all-results-carousel"></a><span data-ttu-id="d8295-175">Microsoft Search 如何排序 [所有結果] 浮動切換中的結果卡片？</span><span class="sxs-lookup"><span data-stu-id="d8295-175">How does Microsoft Search order result cards in the All results carousel?</span></span>

<span data-ttu-id="d8295-176">Microsoft Search 會依據相關性，使用智慧型排序演算法以排序卡片。</span><span class="sxs-lookup"><span data-stu-id="d8295-176">Microsoft Search uses intelligent ranking algorithms to order result cards based on relevance.</span></span>

  

