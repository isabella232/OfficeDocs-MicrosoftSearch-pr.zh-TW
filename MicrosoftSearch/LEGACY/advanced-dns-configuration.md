---
title: 進階 DNS 設定
ms.author: dawholl
author: dawholl
manager: kellis
ms.date: 12/19/2018
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MOE150
- MED150
ms.assetid: 47eedbb9-6da9-47e0-aac5-078d34a7fd8f
ROBOTS: NoIndex
description: 使用 CNAME 設定您的 DNS 伺服器，確保使用者登入順暢無阻
ms.openlocfilehash: 062c43cfbc8d25c263eb2402bd05191e385411b2
ms.sourcegitcommit: 6b531b2ce7253c16251c7089795dedf1d2f3fc33
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/13/2019
ms.locfileid: "38311466"
---
# <a name="advanced-dns-configuration"></a><span data-ttu-id="cfbd2-103">進階 DNS 設定</span><span class="sxs-lookup"><span data-stu-id="cfbd2-103">Advanced DNS configuration</span></span>

<span data-ttu-id="cfbd2-104">若要確保 Bing 隨時可以識別貴組織的使用者，並讓他們成功登入公司或學校帳戶，請設定您的內部 DNS 伺服器或 proxy 伺服器以將 `www.bing.com` 解析為 `ms.bing.com`。</span><span class="sxs-lookup"><span data-stu-id="cfbd2-104">To ensure Bing can always identify users within your organization and successfully sign them in to their work or school account, configure your internal DNS server or proxy server to resolve from `www.bing.com` to `ms.bing.com`.</span></span> <span data-ttu-id="cfbd2-105">若要這麼做，請為 `www.bing.com` 建立一個 DNS 項目，以做為 `ms.bing.com` 的 CNAME。</span><span class="sxs-lookup"><span data-stu-id="cfbd2-105">To do this, create a DNS entry for `www.bing.com` to be a CNAME for `ms.bing.com`.</span></span>
  
****

|<span data-ttu-id="cfbd2-106">**Name**</span><span class="sxs-lookup"><span data-stu-id="cfbd2-106">**Name**</span></span>|<span data-ttu-id="cfbd2-107">**Type**</span><span class="sxs-lookup"><span data-stu-id="cfbd2-107">**Type**</span></span>|<span data-ttu-id="cfbd2-108">**Value**</span><span class="sxs-lookup"><span data-stu-id="cfbd2-108">**Value**</span></span>|
|:-----|:-----|:-----|
|`www.bing.com`  <br/> |<span data-ttu-id="cfbd2-109">CNAME</span><span class="sxs-lookup"><span data-stu-id="cfbd2-109">CNAME</span></span>  <br/> |`ms.bing.com`  <br/> |
   
<span data-ttu-id="cfbd2-110">最好是使用 CNAME 而不是 IP 位址，因為即使 IP 位址變更，CNAME 仍然可以使用。</span><span class="sxs-lookup"><span data-stu-id="cfbd2-110">Using a CNAME rather than the IP address is preferred since a CNAME will continue to work if the IP address changes.</span></span> <span data-ttu-id="cfbd2-111">變更 DNS 之後，使用者仍會看到結果，就好像結果是來自 `www.bing.com`。</span><span class="sxs-lookup"><span data-stu-id="cfbd2-111">After you make this DNS change, results will continue to appear to your users as if they are coming from `www.bing.com`.</span></span> 
  
<span data-ttu-id="cfbd2-112">不需要在用戶端電腦上做其他設定，就能為使用者提供順暢的使用體驗。</span><span class="sxs-lookup"><span data-stu-id="cfbd2-112">This requires no additional configuration on client machines and provides a seamless experience for your users.</span></span> <span data-ttu-id="cfbd2-113">使用者移至 `bing.com` 後，就會更順暢地自動登入，而如果未自動登入，系統會提示使用者執行此動作。</span><span class="sxs-lookup"><span data-stu-id="cfbd2-113">When they go to `bing.com`, they'll be automatically signed in more consistently, and if they can't be signed in automatically, they'll be prompted to do so.</span></span>
