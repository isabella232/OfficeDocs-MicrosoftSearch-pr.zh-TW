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
ms.openlocfilehash: 5a134116c98b4feea0c04909349ce4b972c59ffe
ms.sourcegitcommit: 0b8c3c57384cecaa93c5cbaf3b3b30f8e20d1a69
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/09/2020
ms.locfileid: "48408436"
---
<!-- markdownlint-disable no-trailing-punctuation -->
# <a name="frequently-asked-questions"></a><span data-ttu-id="dd80a-103">常見問題集</span><span class="sxs-lookup"><span data-stu-id="dd80a-103">Frequently asked questions</span></span>

<span data-ttu-id="dd80a-104">以下是最常見問題的清單。</span><span class="sxs-lookup"><span data-stu-id="dd80a-104">Here's a list of the most common questions.</span></span>

> [!TIP]
> <span data-ttu-id="dd80a-105">在這裡看不到您的問題獲得解答嗎？</span><span class="sxs-lookup"><span data-stu-id="dd80a-105">Don't see your question answered here?</span></span> <span data-ttu-id="dd80a-106">請在這篇文章的意見反應中提出您的問題。</span><span class="sxs-lookup"><span data-stu-id="dd80a-106">Ask your question in this article's feedback.</span></span>

## <a name="is-advanced-query-understanding-supported"></a><span data-ttu-id="dd80a-107">是否支援進階查詢理解？</span><span class="sxs-lookup"><span data-stu-id="dd80a-107">Is advanced query understanding supported?</span></span>

<span data-ttu-id="dd80a-108">是的，Microsoft Search 會從較大的片語剖析查詢意圖。</span><span class="sxs-lookup"><span data-stu-id="dd80a-108">Yes, Microsoft Search parses query intent from larger phrases.</span></span> <span data-ttu-id="dd80a-109">此功能會使用 AI 以學習將常用多餘片語的使用者新增到查詢，但不影響使用者的搜尋意圖。</span><span class="sxs-lookup"><span data-stu-id="dd80a-109">This feature uses AI to learn common superfluous phrases users add to their queries that don't impact their search intent.</span></span> <span data-ttu-id="dd80a-110">例如，當使用者搜尋有關 *如何變更密碼的詳細資訊*時，我們會從查詢中解壓縮較不重要的字詞，並根據相關的 *變更密碼（如變更密碼*）進行觸發。</span><span class="sxs-lookup"><span data-stu-id="dd80a-110">For example, when a user searches for *tell me more about how to change my password please*, we extract the less important words from the query and trigger based on the relevant ones like *change password*.</span></span>
  
<span data-ttu-id="dd80a-111">這項功能不會覆寫 [Microsoft 365 系統管理中心](https://admin.microsoft.com)中的關鍵字集。</span><span class="sxs-lookup"><span data-stu-id="dd80a-111">This feature won't override keywords set in the [Microsoft 365 admin center](https://admin.microsoft.com).</span></span>
  
## <a name="can-you-search-for-files-on-premises"></a><span data-ttu-id="dd80a-112">可以搜尋內部部署檔案嗎？</span><span class="sxs-lookup"><span data-stu-id="dd80a-112">Can you search for files on-premises?</span></span>

<span data-ttu-id="dd80a-113">是。</span><span class="sxs-lookup"><span data-stu-id="dd80a-113">Yes.</span></span> <span data-ttu-id="dd80a-114">如果您有 SharePoint 的混合式部署，您可以搜尋內部部署 [SharePoint](http://sharepoint.com/) 檔案。</span><span class="sxs-lookup"><span data-stu-id="dd80a-114">You can search on-premises [SharePoint](http://sharepoint.com/) files if you have a hybrid deployment of SharePoint.</span></span>
  
## <a name="how-do-i-make-bing-the-default-search-engine-for-people-in-my-org"></a><span data-ttu-id="dd80a-115">如何讓 Bing 成為我的組織中人員的預設搜尋引擎？</span><span class="sxs-lookup"><span data-stu-id="dd80a-115">How do I make Bing the default search engine for people in my org?</span></span>

<span data-ttu-id="dd80a-116">以下是設定預設搜尋引擎、預設首頁及預設瀏覽器的指示，可讓您的使用者在 [Bing](https://Bing.com)中使用 Microsoft search 的最佳體驗：</span><span class="sxs-lookup"><span data-stu-id="dd80a-116">Here's the instructions for setting the default search engine, default homepage, and default browser to give your users the best experience with Microsoft Search in [Bing](https://Bing.com):</span></span>

- [<span data-ttu-id="dd80a-117">將 Microsoft Edge 設定為預設瀏覽器</span><span class="sxs-lookup"><span data-stu-id="dd80a-117">Set Microsoft Edge as your default browser</span></span>](set-default-browser.md)
- [<span data-ttu-id="dd80a-118">讓 Bing 成為預設搜尋引擎</span><span class="sxs-lookup"><span data-stu-id="dd80a-118">Make Bing your default search engine</span></span>](set-default-search-engine.md)
- [<span data-ttu-id="dd80a-119">將 Bing.com 設為企業首頁</span><span class="sxs-lookup"><span data-stu-id="dd80a-119">Set Bing.com as your enterprise homepage</span></span>](set-default-homepage.md)

## <a name="how-are-my-search-results-protected"></a><span data-ttu-id="dd80a-120">如何保護我的搜尋結果？</span><span class="sxs-lookup"><span data-stu-id="dd80a-120">How are my search results protected?</span></span>

<span data-ttu-id="dd80a-121">我們需要 [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/) 驗證，才能存取受信任的雲端的結果。</span><span class="sxs-lookup"><span data-stu-id="dd80a-121">We require [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/) authentication to access results from the Trusted Cloud.</span></span> <span data-ttu-id="dd80a-122">已驗證的使用者只會看到他們有權存取的內容。</span><span class="sxs-lookup"><span data-stu-id="dd80a-122">Authenticated users only see content they have access to.</span></span> <span data-ttu-id="dd80a-123">搜尋查詢會解除辨識，而且記錄會與 public [Bing](https://Bing.com) 搜尋流量分開。</span><span class="sxs-lookup"><span data-stu-id="dd80a-123">Search queries are de-identified, and logs are separated from public [Bing](https://Bing.com) search traffic.</span></span> <span data-ttu-id="dd80a-124">這種保護層級是業界唯一的。</span><span class="sxs-lookup"><span data-stu-id="dd80a-124">This level of protection is unavailable anywhere else in the industry.</span></span>

## <a name="can-i-search-across-federated-organizations"></a><span data-ttu-id="dd80a-125">可以跨同盟組織搜尋嗎？</span><span class="sxs-lookup"><span data-stu-id="dd80a-125">Can I search across federated organizations?</span></span>

<span data-ttu-id="dd80a-126">否。</span><span class="sxs-lookup"><span data-stu-id="dd80a-126">No.</span></span>

## <a name="where-can-i-get-info-about-office-365-security-compliance-and-privacy"></a><span data-ttu-id="dd80a-127">我可以在哪裡取得有關 Office 365 安全性、規範和隱私權的資訊？</span><span class="sxs-lookup"><span data-stu-id="dd80a-127">Where can I get info about Office 365 security, compliance, and privacy?</span></span>

<span data-ttu-id="dd80a-128">詳細資料可在 [Office 365 的 [信任中心] 頁面](https://www.microsoft.com/TrustCenter/CloudServices/office365/default.aspx)上找到。</span><span class="sxs-lookup"><span data-stu-id="dd80a-128">Details can be found on the [Trust Center pages for Office 365](https://www.microsoft.com/TrustCenter/CloudServices/office365/default.aspx).</span></span>

## <a name="can-users-earn-microsoft-rewards-points-with-their-work-or-school-account"></a><span data-ttu-id="dd80a-129">使用者能否使用其公司或學校帳戶來獲得 Microsoft Rewards 積分？</span><span class="sxs-lookup"><span data-stu-id="dd80a-129">Can users earn Microsoft Rewards points with their work or school account?</span></span>

<span data-ttu-id="dd80a-130">Microsoft Search 要求企業使用者使用公司或學校帳戶登入。</span><span class="sxs-lookup"><span data-stu-id="dd80a-130">Microsoft Search requires that enterprise users sign in with a work or school account.</span></span> <span data-ttu-id="dd80a-131">但使用者無法使用這些帳戶來加入或登入 Microsoft Rewards 方案。</span><span class="sxs-lookup"><span data-stu-id="dd80a-131">But users can’t join or sign in to the Microsoft Rewards program with those accounts.</span></span> <span data-ttu-id="dd80a-132">但有一個例子，企業使用者可能會看到 Rewards 積分累算。</span><span class="sxs-lookup"><span data-stu-id="dd80a-132">However, there is an instance when an enterprise user may see Rewards points accrue.</span></span> <span data-ttu-id="dd80a-133">當 Microsoft Search 使用者的 Rewards 帳戶是使用 [Microsoft 帳戶](https://www.microsoft.com/welcome?rtc=1)建立時，即可能發生此情況。</span><span class="sxs-lookup"><span data-stu-id="dd80a-133">This can happen when a Microsoft Search user has a Rewards account that was created with a [Microsoft account](https://www.microsoft.com/welcome?rtc=1).</span></span> <span data-ttu-id="dd80a-134">(與 Microsoft 帳戶相關聯的電子郵件地址可以來自 Outlook.com、Hotmail.com、Gmail、Yahoo 或其他提供者。) 如果使用者在同一位瀏覽器工作階段中同時使用他們的公司帳戶和 Microsoft 帳戶登入，則可能會對其 Rewards 帳戶累算積分。</span><span class="sxs-lookup"><span data-stu-id="dd80a-134">(The email address associated with a Microsoft account can be from Outlook.com, Hotmail.com, Gmail, Yahoo, or other providers.) If users sign in alternately with both their work account and Microsoft account in the same browser session, they might accrue points to their Rewards account.</span></span> <span data-ttu-id="dd80a-135">使用者可以透過在使用 Microsoft Search 搜尋時清除其 Cookie 來停止累算積分。</span><span class="sxs-lookup"><span data-stu-id="dd80a-135">Users can stop accruing points while searching with Microsoft Search by clearing their cookies.</span></span>

## <a name="can-guest-users-leverage-microsoft-search-in-my-organization"></a><span data-ttu-id="dd80a-136">來賓使用者是否可以在我的組織中利用 Microsoft 搜尋？</span><span class="sxs-lookup"><span data-stu-id="dd80a-136">Can guest users leverage Microsoft Search in my organization?</span></span>

<span data-ttu-id="dd80a-137">Microsoft 365 透過[來賓存取](https://docs.microsoft.com/microsoft-365/solutions/collaborate-with-people-outside-your-organization)，與組織外部的人員進行豐富的共同作業。</span><span class="sxs-lookup"><span data-stu-id="dd80a-137">Microsoft 365 enables rich collaboration with people outside of your organization through [guest access.](https://docs.microsoft.com/microsoft-365/solutions/collaborate-with-people-outside-your-organization)</span></span> <span data-ttu-id="dd80a-138">這些使用者將能夠對檔、網站、群組、清單及文件庫執行搜尋作業。</span><span class="sxs-lookup"><span data-stu-id="dd80a-138">These users will be able to perform search operations on documents, sites, groups, lists, and libraries.</span></span> <span data-ttu-id="dd80a-139">不過，來賓使用者將不會取得完整、個人化的 Microsoft 搜尋體驗，而且可能需要利用頁面中的 [頁面] 搜尋方塊，而不是在頁首中的「整合的 Microsoft 搜尋」方塊。</span><span class="sxs-lookup"><span data-stu-id="dd80a-139">However, guest users will not get the full, personalized, Microsoft Search experience and may need to leverage the on-page search box instead of the unified Microsoft Search box in the header.</span></span>
