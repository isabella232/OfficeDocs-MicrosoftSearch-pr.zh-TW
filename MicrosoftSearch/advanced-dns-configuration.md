---
title: 進階 DNS 設定
ms.author: dawholl
author: dawholl
manager: kellis
ms.date: 12/19/2018
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Priority
search.appverid:
- BFB160
- MOE150
- MED150
ms.assetid: 47eedbb9-6da9-47e0-aac5-078d34a7fd8f
description: 使用 CNAME 設定您的 DNS 伺服器，確保使用者登入順暢無阻
ms.openlocfilehash: 1b79db9a4cb5875b2ff3023572f0338944dfda7d
ms.sourcegitcommit: 3e91a6e70b48a0100adfed1b62ba79f2fd1735d2
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/13/2019
ms.locfileid: "34425642"
---
# <a name="advanced-dns-configuration"></a><span data-ttu-id="76e6f-103">進階 DNS 設定</span><span class="sxs-lookup"><span data-stu-id="76e6f-103">Advanced DNS configuration</span></span>

> [!IMPORTANT]
> <span data-ttu-id="76e6f-104">Bing 設定中的 Microsoft Search 現在可以在 Microsoft 365 管理中心中使用。</span><span class="sxs-lookup"><span data-stu-id="76e6f-104">Microsoft Search in Bing settings are now available in the Microsoft 365 admin center.</span></span> <span data-ttu-id="76e6f-105">從系統管理中心的[指派搜尋系統管理員](https://docs.microsoft.com/zh-TW/microsoftsearch/setup-microsoft-search#step-2-assign-search-admin-and-search-editor)開始。</span><span class="sxs-lookup"><span data-stu-id="76e6f-105">Get started by [assigning search admins](https://docs.microsoft.com/en-us/microsoftsearch/setup-microsoft-search#step-2-assign-search-admin-and-search-editor) in your admin center.</span></span>
    
<span data-ttu-id="76e6f-106">若要確保 Bing 隨時可以識別貴組織的使用者，並讓他們成功登入公司或學校帳戶，請設定您的內部 DNS 伺服器或 proxy 伺服器將 `www.bing.com` 解析為 `ms.bing.com`。</span><span class="sxs-lookup"><span data-stu-id="76e6f-106">To ensure Bing can always identify users within your organization and successfully sign them in to their work or school account, configure your internal DNS server or proxy server to resolve from `www.bing.com` to `ms.bing.com`.</span></span> <span data-ttu-id="76e6f-107">若要這麼做，請為 `www.bing.com` 建立一個 DNS 項目，以做為 `ms.bing.com` 的 CNAME。</span><span class="sxs-lookup"><span data-stu-id="76e6f-107">To do this, create a DNS entry for `www.bing.com` to be a CNAME for `ms.bing.com`.</span></span>
  
****

|<span data-ttu-id="76e6f-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="76e6f-108">**Name**</span></span>|<span data-ttu-id="76e6f-109">**Type**</span><span class="sxs-lookup"><span data-stu-id="76e6f-109">**Type**</span></span>|<span data-ttu-id="76e6f-110">**Value**</span><span class="sxs-lookup"><span data-stu-id="76e6f-110">**Value**</span></span>|
|:-----|:-----|:-----|
|`www.bing.com`  <br/> |<span data-ttu-id="76e6f-111">CNAME</span><span class="sxs-lookup"><span data-stu-id="76e6f-111">CNAME</span></span>  <br/> |`ms.bing.com`  <br/> |
   
<span data-ttu-id="76e6f-112">最好是使用 CNAME 而不是 IP 位址，因為即使 IP 位址變更，CNAME 仍然可以使用。</span><span class="sxs-lookup"><span data-stu-id="76e6f-112">Using a CNAME rather than the IP address is preferred since a CNAME will continue to work if the IP address changes.</span></span> <span data-ttu-id="76e6f-113">變更 DNS 之後，使用者仍會看到結果，就好像結果是來自 `www.bing.com`。</span><span class="sxs-lookup"><span data-stu-id="76e6f-113">After you make this DNS change, results will continue to appear to your users as if they are coming from `www.bing.com`.</span></span> 
  
<span data-ttu-id="76e6f-114">不需要在用戶端電腦上做其他設定，就能為使用者提供順暢的使用體驗。</span><span class="sxs-lookup"><span data-stu-id="76e6f-114">This requires no additional configuration on client machines and provides a seamless experience for your users.</span></span> <span data-ttu-id="76e6f-115">使用者移至 `bing.com` 後，就會更順暢地自動登入，而如果未自動登入，系統會提示使用者執行此動作。</span><span class="sxs-lookup"><span data-stu-id="76e6f-115">When they go to `bing.com`, they'll be automatically signed in more consistently, and if they can't be signed in automatically, they'll be prompted to do so.</span></span>
