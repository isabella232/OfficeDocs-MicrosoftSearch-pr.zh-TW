---
title: 系統管理入口網站工具
ms.author: dawholl
author: dawholl
manager: kellis
ms.date: 12/18/2018
ms.audience: Admin
ms.topic: reference
ms.service: mssearch
localization_priority: Priority
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: 4a824483-2407-4bbd-8f7f-5ebb47817c7e
ROBOTS: NoIndex
description: 使用 Microsoft Search 工具建立和匯出結果、自動登入，以及從任何地方搜尋的概觀
ms.openlocfilehash: d8c725841e70dc90b5ae17fa992a933b8cb3e8c3
ms.sourcegitcommit: c2c9e66af1038efd2849d578f846680851f9e5d2
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/27/2019
ms.locfileid: "36639629"
---
# <a name="admin-portal-tools"></a><span data-ttu-id="9f85f-103">系統管理入口網站工具</span><span class="sxs-lookup"><span data-stu-id="9f85f-103">Admin portal tools</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9f85f-104">本文章適用 Bing 系統管理入口網站中的 Microsoft Search。</span><span class="sxs-lookup"><span data-stu-id="9f85f-104">This article applies to the Microsoft Search in Bing admin portal.</span></span> <span data-ttu-id="9f85f-105">我們正在將入口網站移至 Microsoft 365 系統管理中心，完成之後將會移除 Bing 系統管理入口網站中的 Microsoft Search。</span><span class="sxs-lookup"><span data-stu-id="9f85f-105">We’re moving the portal to the Microsoft 365 admin center, and then the Microsoft Search in Bing portal will be removed.</span></span> <span data-ttu-id="9f85f-106">建議您使用 Microsoft 365 系統管理中心來開始。</span><span class="sxs-lookup"><span data-stu-id="9f85f-106">We recommend that you use the Microsoft 365 admin center to get started.</span></span> <span data-ttu-id="9f85f-107">[Microsoft Search 概觀](overview-microsoft-search.md)。</span><span class="sxs-lookup"><span data-stu-id="9f85f-107">[Overview of Microsoft Graph](overview-microsoft-search.md)</span></span>
    
<span data-ttu-id="9f85f-108">Microsoft Search 系統管理入口網站含有專為系統管理員、編輯者和使用者設計的工具和資源，包括：</span><span class="sxs-lookup"><span data-stu-id="9f85f-108">The Microsoft Search Admin portal includes tools and resources designed for admins, editors, and users, including:</span></span>
  
- <span data-ttu-id="9f85f-109">內容建立者瀏覽器擴充功能</span><span class="sxs-lookup"><span data-stu-id="9f85f-109">Content creator browser extension</span></span>
    
    <span data-ttu-id="9f85f-110">適用於系統管理員和編輯者，只要移至網站或網頁就能使用 Chrome 或 Microsoft Edge 擴充功能，輕鬆[建立書籤](create-bookmarks.md)和[常見問答集](create-qas.md)。</span><span class="sxs-lookup"><span data-stu-id="9f85f-110">Available for admins and editors, use the Chrome or Edge extension to easily [create bookmarks](create-bookmarks.md) and [Q&As](create-qas.md) simply by going to a site or page.</span></span> 
    
- <span data-ttu-id="9f85f-111">Bing 中的 Microsoft Search 搜尋擴充功能</span><span class="sxs-lookup"><span data-stu-id="9f85f-111">Microsoft Search in Bing search extension</span></span>
    
    <span data-ttu-id="9f85f-112">無需離開您目前的網頁或網站，就能使用 Chrome 或 Microsoft Edge 擴充功能快速存取 Microsoft Search 企業搜尋。</span><span class="sxs-lookup"><span data-stu-id="9f85f-112">Use the Chrome or Edge extension to quickly access Microsoft Search enterprise search without leaving the page or site you're on.</span></span>
    
- <span data-ttu-id="9f85f-113">適用於 Chrome 的 Windows 10 和 AAD 登入擴充功能</span><span class="sxs-lookup"><span data-stu-id="9f85f-113">Windows 10 and AAD sign-in extension for Chrome</span></span>
    
    <span data-ttu-id="9f85f-114">在登入支援的網站 (包括 Office 365 和 Bing) 時，使用 Chrome 擴充功能可輕鬆驗證 Azure Active Directory。</span><span class="sxs-lookup"><span data-stu-id="9f85f-114">Use the Chrome extension to easily authenticate with Azure Active Directory when signing in to supported sites, including Office 365 and Bing.</span></span> <span data-ttu-id="9f85f-115">我們建議您在[測試單一登入](test-single-sign-on.md)時部署此擴充功能。</span><span class="sxs-lookup"><span data-stu-id="9f85f-115">We recommend deploying this extension when you [test single sign-on](test-single-sign-on.md).</span></span>
    
- <span data-ttu-id="9f85f-116">將熱門 SharePoint 查詢匯入為書籤</span><span class="sxs-lookup"><span data-stu-id="9f85f-116">Import top SharePoint queries as bookmarks</span></span>
    
    <span data-ttu-id="9f85f-117">系統管理員可以使用此 PowerShell 指令碼[匯入 SharePoint 熱門查詢](import-sharepoint-promoted-results-and-top-queries.md)做為草稿書籤。</span><span class="sxs-lookup"><span data-stu-id="9f85f-117">Available to admins, use this PowerShell script to [import SharePoint top queries](import-sharepoint-promoted-results-and-top-queries.md) as draft bookmarks.</span></span> <span data-ttu-id="9f85f-118">下載指令碼並開啟讀我檔案，以獲得關於需求、範例和可用參數等資訊。</span><span class="sxs-lookup"><span data-stu-id="9f85f-118">Download the script and open the README file for information about requirements, examples, and available parameters.</span></span> 
    
- <span data-ttu-id="9f85f-119">將 SharePoint 進階結果查詢規則匯入為書籤</span><span class="sxs-lookup"><span data-stu-id="9f85f-119">Import SharePoint Promoted Result Query Rules as bookmarks</span></span>
    
    <span data-ttu-id="9f85f-120">系統管理員可以[匯入 SharePoint 進階結果](import-sharepoint-promoted-results-and-top-queries.md)和熱門查詢 (亦即首選) 做為建議的書籤。</span><span class="sxs-lookup"><span data-stu-id="9f85f-120">Available to admins, [import SharePoint promoted results](import-sharepoint-promoted-results-and-top-queries.md) and top queries, or Best Bets, as suggested bookmarks.</span></span> 

  

