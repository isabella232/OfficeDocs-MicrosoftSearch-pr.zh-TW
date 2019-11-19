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
# <a name="frequently-asked-questions"></a><span data-ttu-id="8d7de-103">常見問題集</span><span class="sxs-lookup"><span data-stu-id="8d7de-103">Frequently asked questions</span></span>

<span data-ttu-id="8d7de-104">以下是最常見問題的清單。</span><span class="sxs-lookup"><span data-stu-id="8d7de-104">Here's a list of the most common questions.</span></span>

> [!TIP]
> <span data-ttu-id="8d7de-105">在這裡看不到您的問題獲得解答嗎？</span><span class="sxs-lookup"><span data-stu-id="8d7de-105">Don't see your question answered here?</span></span> <span data-ttu-id="8d7de-106">請在這篇文章的意見反應中提出您的問題。</span><span class="sxs-lookup"><span data-stu-id="8d7de-106">Ask your question in this article's feedback.</span></span>

## <a name="is-advanced-query-understanding-supported"></a><span data-ttu-id="8d7de-107">是否支援進階查詢理解？</span><span class="sxs-lookup"><span data-stu-id="8d7de-107">Is advanced query understanding supported?</span></span>

<span data-ttu-id="8d7de-108">是的，Microsoft Search 會從較大的片語剖析查詢意圖。</span><span class="sxs-lookup"><span data-stu-id="8d7de-108">Yes, Microsoft Search parses query intent from larger phrases.</span></span> <span data-ttu-id="8d7de-109">此功能會使用 AI 以學習將常用多餘片語的使用者新增到查詢，但不影響使用者的搜尋意圖。</span><span class="sxs-lookup"><span data-stu-id="8d7de-109">This feature uses AI to learn common superfluous phrases users add to their queries that don't impact their search intent.</span></span> <span data-ttu-id="8d7de-110">例如，當使用者搜尋*告訴我更多有關如何變更我的密碼請*我們解壓縮較重要的文字查詢和相關的項目，例如*變更密碼*為基礎的觸發程序。</span><span class="sxs-lookup"><span data-stu-id="8d7de-110">For example, when a user searches for *tell me more about how to change my password please*, we extract the less important words from the query and trigger based on the relevant ones like *change password*.</span></span>
  
<span data-ttu-id="8d7de-111">這項功能不會覆寫在 Microsoft 365[系統管理中心](https://admin.microsoft.com)中設定的關鍵字。</span><span class="sxs-lookup"><span data-stu-id="8d7de-111">This feature won't override keywords set in the Microsoft 365 [admin center](https://admin.microsoft.com).</span></span>
  
## <a name="can-you-search-for-files-on-premises"></a><span data-ttu-id="8d7de-112">可以搜尋內部部署檔案嗎？</span><span class="sxs-lookup"><span data-stu-id="8d7de-112">Can you search for files on-premises?</span></span>

<span data-ttu-id="8d7de-113">是。</span><span class="sxs-lookup"><span data-stu-id="8d7de-113">Yes.</span></span> <span data-ttu-id="8d7de-114">如果您有 SharePoint 的混合式部署，您可以搜尋內部部署[SharePoint](http://sharepoint.com/)檔案。</span><span class="sxs-lookup"><span data-stu-id="8d7de-114">You can search on-premises [SharePoint](http://sharepoint.com/) files if you have a hybrid deployment of SharePoint.</span></span>
  
## <a name="how-do-i-make-bing-the-default-search-engine-for-people-in-my-org"></a><span data-ttu-id="8d7de-115">如何讓 Bing 成為我的組織中人員的預設搜尋引擎？</span><span class="sxs-lookup"><span data-stu-id="8d7de-115">How do I make Bing the default search engine for people in my org?</span></span>

<span data-ttu-id="8d7de-116">以下是設定預設搜尋引擎、 預設首頁和預設的瀏覽器的指示，授與您的使用者與 Microsoft Search 的最佳經驗， [Bing](https://Bing.com)中：</span><span class="sxs-lookup"><span data-stu-id="8d7de-116">Here's the instructions for setting the default search engine, default homepage, and default browser to give your users the best experience with Microsoft Search in [Bing](https://Bing.com):</span></span>

- [<span data-ttu-id="8d7de-117">設為預設瀏覽器的 Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8d7de-117">Set Microsoft Edge as your default browser</span></span>](set-default-browser.md)
- [<span data-ttu-id="8d7de-118">讓 Bing 成為預設搜尋引擎</span><span class="sxs-lookup"><span data-stu-id="8d7de-118">Make Bing your default search engine</span></span>](set-default-search-engine.md)
- [<span data-ttu-id="8d7de-119">將 Bing.com 設為企業首頁</span><span class="sxs-lookup"><span data-stu-id="8d7de-119">Set Bing.com as your enterprise homepage</span></span>](set-default-homepage.md)

  
## <a name="how-are-my-search-results-protected"></a><span data-ttu-id="8d7de-120">如何保護我的搜尋結果？</span><span class="sxs-lookup"><span data-stu-id="8d7de-120">How are my search results protected?</span></span>

<span data-ttu-id="8d7de-121">我們需要[Azure Active Directory](https://docs.microsoft.com/azure/active-directory/)驗證以存取結果從信任雲端。</span><span class="sxs-lookup"><span data-stu-id="8d7de-121">We require [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/) authentication to access results from the Trusted Cloud.</span></span> <span data-ttu-id="8d7de-122">已驗證的使用者只會看到他們有權存取的內容。</span><span class="sxs-lookup"><span data-stu-id="8d7de-122">Authenticated users only see content they have access to.</span></span> <span data-ttu-id="8d7de-123">去除識別搜尋查詢，以及記錄檔分開的公用[Bing](https://Bing.com)搜尋流量。</span><span class="sxs-lookup"><span data-stu-id="8d7de-123">Search queries are de-identified, and logs are separated from public [Bing](https://Bing.com) search traffic.</span></span> <span data-ttu-id="8d7de-124">這種保護層級是業界唯一的。</span><span class="sxs-lookup"><span data-stu-id="8d7de-124">This level of protection is unavailable anywhere else in the industry.</span></span>

## <a name="can-i-search-across-federated-organizations"></a><span data-ttu-id="8d7de-125">可以跨同盟組織搜尋嗎？</span><span class="sxs-lookup"><span data-stu-id="8d7de-125">Can I search across federated organizations?</span></span>

<span data-ttu-id="8d7de-126">否。</span><span class="sxs-lookup"><span data-stu-id="8d7de-126">No.</span></span>

## <a name="where-can-i-get-info-about-office-365-and-microsoft-365-compliance-tiers-and-categories"></a><span data-ttu-id="8d7de-127">我可以從哪裡獲得關於 Office 365 和 Microsoft 365 合規性層級和類別的資訊？</span><span class="sxs-lookup"><span data-stu-id="8d7de-127">Where can I get info about Office 365 and Microsoft 365 compliance tiers and categories?</span></span>

<span data-ttu-id="8d7de-128">您可以在[符合產業標準和法規的合規性架構](https://download.microsoft.com/download/B/2/7/B27B3EF3-8849-4C18-8BA4-5AD755728620/Compliance%20Framework_customer%20guidance.pdf) (下載 PDF) 中找到詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8d7de-128">Details can be found in the [Compliance Framework for Industry Standards and Regulations](https://download.microsoft.com/download/B/2/7/B27B3EF3-8849-4C18-8BA4-5AD755728620/Compliance%20Framework_customer%20guidance.pdf) (PDF download).</span></span>

## <a name="can-users-earn-microsoft-rewards-points-with-their-work-or-school-account"></a><span data-ttu-id="8d7de-129">使用者能否使用其公司或學校帳戶來獲得 Microsoft Rewards 積分？</span><span class="sxs-lookup"><span data-stu-id="8d7de-129">Can users earn Microsoft Rewards points with their work or school account?</span></span>

<span data-ttu-id="8d7de-130">Microsoft Search 要求企業使用者使用公司或學校帳戶登入。</span><span class="sxs-lookup"><span data-stu-id="8d7de-130">Microsoft Search requires that enterprise users sign in with a work or school account.</span></span> <span data-ttu-id="8d7de-131">但使用者無法使用這些帳戶來加入或登入 Microsoft Rewards 方案。</span><span class="sxs-lookup"><span data-stu-id="8d7de-131">But users can’t join or sign in to the Microsoft Rewards program with those accounts.</span></span> <span data-ttu-id="8d7de-132">但有一個例子，企業使用者可能會看到 Rewards 積分累算。</span><span class="sxs-lookup"><span data-stu-id="8d7de-132">However, there is an instance when an enterprise user may see Rewards points accrue.</span></span> <span data-ttu-id="8d7de-133">當 Microsoft Search 使用者的 Rewards 帳戶是使用 <a href="https://www.microsoft.com/welcome?rtc=1">Microsoft 帳戶</a>建立時，即可能發生此情況。</span><span class="sxs-lookup"><span data-stu-id="8d7de-133">This can happen when a Microsoft Search user has a Rewards account that was created with a <a href="https://www.microsoft.com/welcome?rtc=1">Microsoft account</a>.</span></span> <span data-ttu-id="8d7de-134">(與 Microsoft 帳戶相關聯的電子郵件地址可以來自 Outlook.com、Hotmail.com、Gmail、Yahoo 或其他提供者。) 如果使用者在同一位瀏覽器工作階段中同時使用他們的公司帳戶和 Microsoft 帳戶登入，則可能會對其 Rewards 帳戶累算積分。</span><span class="sxs-lookup"><span data-stu-id="8d7de-134">(The email address associated with a Microsoft account can be from Outlook.com, Hotmail.com, Gmail, Yahoo, or other providers.) If users sign in alternately with both their work account and Microsoft account in the same browser session, they might accrue points to their Rewards account.</span></span> <span data-ttu-id="8d7de-135">使用者可以透過在使用 Microsoft Search 搜尋時清除其 Cookie 來停止累算積分。</span><span class="sxs-lookup"><span data-stu-id="8d7de-135">Users can stop accruing points while searching with Microsoft Search by clearing their cookies.</span></span> 

