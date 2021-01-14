---
title: 線上和 Microsoft 搜尋 SharePoint 中的傳統頁面
ms.author: keremy
author: jeffkizn
manager: parulm
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 在傳統的 SharePoint 頁面上使用 Microsoft 搜尋
ms.openlocfilehash: 9a5aeb2e683297faccfb55d3407653c1791b3961
ms.sourcegitcommit: 7133d46ca9c3a5216ee9159db781febd17e5a831
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/14/2021
ms.locfileid: "49863172"
---
# <a name="classic-pages-and-microsoft-search"></a><span data-ttu-id="fe365-103">傳統頁面和 Microsoft 搜尋</span><span class="sxs-lookup"><span data-stu-id="fe365-103">Classic pages and Microsoft Search</span></span>

<span data-ttu-id="fe365-104">SharePoint 現代網站之前建立的網站使用傳統搜尋方塊和傳統搜尋結果體驗。</span><span class="sxs-lookup"><span data-stu-id="fe365-104">SharePoint sites created prior to modern sites use a classic search box and classic search results experience.</span></span> <span data-ttu-id="fe365-105">我們將推出使用 Microsoft Search 的新式搜尋體驗來開始使用預設傳統頁面的功能，其可提供具有較高相關性的個人化結果。</span><span class="sxs-lookup"><span data-stu-id="fe365-105">We will be rolling out a feature that will default classic pages to start using the modern search experience that uses Microsoft Search, which provides personalized results with higher relevance.</span></span>

<span data-ttu-id="fe365-106">針對所有網站（包括傳統）都建議使用 Microsoft Search，但是如果您的傳統網站使用自訂主版頁面和/或您已自訂傳統的搜尋結果體驗，我們將會自動偵測這些自訂，而不會切換至 Microsoft 搜尋。</span><span class="sxs-lookup"><span data-stu-id="fe365-106">Using Microsoft Search is recommended for all sites, including classic, but if your classic sites use custom master pages and/or you have customized your classic search results experience, we will auto-detect these customizations and not switch to Microsoft Search.</span></span>

## <a name="classic-sites-that-will-automatically-switch-to-microsoft-search"></a><span data-ttu-id="fe365-107">將會自動切換至 Microsoft 搜尋的傳統網站</span><span class="sxs-lookup"><span data-stu-id="fe365-107">Classic sites that will automatically switch to Microsoft Search</span></span>

<span data-ttu-id="fe365-108">當下列所有條件皆為真時，傳統網站會開始使用 Microsoft Search：</span><span class="sxs-lookup"><span data-stu-id="fe365-108">Classic sites will start using Microsoft Search if all of the following are true:</span></span>

* <span data-ttu-id="fe365-109">網站是以小組網站範本為基礎， (例如 STS#0 和 STS # 1) 。</span><span class="sxs-lookup"><span data-stu-id="fe365-109">The site is based on the team site template (like STS#0 and STS#1).</span></span>
* <span data-ttu-id="fe365-110">網站未開啟發佈功能。</span><span class="sxs-lookup"><span data-stu-id="fe365-110">The site does not have the publishing feature turned on.</span></span>
* <span data-ttu-id="fe365-111">網站不會使用自訂主版頁面 (不同的主版頁面，而不是 oslo 或西雅圖。主圖形) 。</span><span class="sxs-lookup"><span data-stu-id="fe365-111">The site does not use a custom master page (a different master page than oslo.master or seattle.master).</span></span>
* <span data-ttu-id="fe365-112">在預設結果來源上，除了為網站、網站集合或租使用者新增升級的結果之外，還沒有任何使用中的查詢規則。</span><span class="sxs-lookup"><span data-stu-id="fe365-112">There are no active query rules other than those adding promoted results for the site, site collection or tenant on the default result source.</span></span>
* <span data-ttu-id="fe365-113">預設結果來源上沒有網站或網站集合的自訂結果類型。</span><span class="sxs-lookup"><span data-stu-id="fe365-113">There are no custom result types for the site or the site collection on the default result source.</span></span>
* <span data-ttu-id="fe365-114">使用下列所述的 *SearchBoxInNavBar* 設定，不會選擇網站或網站集合的參數。</span><span class="sxs-lookup"><span data-stu-id="fe365-114">The site or the site collection is not opted out of the switch using the *SearchBoxInNavBar* setting described below.</span></span>

<span data-ttu-id="fe365-115">切換至 Microsoft 搜尋後，網站中的傳統頁面會開始顯示套件導覽列中的 [搜尋] 方塊，並移除頁面上的 [傳統搜尋] 方塊。</span><span class="sxs-lookup"><span data-stu-id="fe365-115">After the switch to Microsoft Search, classic pages in the site will start to show the search box in the suite navigation bar and remove the classic search box from the page.</span></span> <span data-ttu-id="fe365-116">然後，當使用者搜尋字詞時，結果會以 Microsoft 搜尋的新式搜尋體驗來顯示。</span><span class="sxs-lookup"><span data-stu-id="fe365-116">Then, when a user searches for a term, the results will be displayed using the modern search experience of Microsoft Search.</span></span>

## <a name="staying-with-the-classic-search-experience"></a><span data-ttu-id="fe365-117">保持傳統搜尋體驗</span><span class="sxs-lookup"><span data-stu-id="fe365-117">Staying with the classic search experience</span></span>

<span data-ttu-id="fe365-118">如果您的網站符合以上所列的準則，但您不想要切換至 Microsoft 搜尋體驗，您可以選擇以網站或網站集合擁有者的身分使用下列命令。</span><span class="sxs-lookup"><span data-stu-id="fe365-118">If your site meets the criteria listed above, but you do not want it to switch to the Microsoft Search experience, you can opt out using the following commands, as the site or site collection owner.</span></span>

<span data-ttu-id="fe365-119">您可以在切換之前或之後的任何時間使用此命令，這樣就能輕鬆回到先前所用的搜尋體驗。</span><span class="sxs-lookup"><span data-stu-id="fe365-119">You can use this command at any time, before or after the switch happens, so it is easy to go back to the search experience you had previously.</span></span>

<span data-ttu-id="fe365-120">若要執行下列命令，您會使用 PowerShell 搭配 SharePoint PnP PowerShell 擴充。</span><span class="sxs-lookup"><span data-stu-id="fe365-120">To run the commands below, you will use PowerShell with SharePoint PnP PowerShell extensions.</span></span> <span data-ttu-id="fe365-121">您可以安裝並深入瞭解如何開始 [這裡](https://docs.microsoft.com/powershell/sharepoint/sharepoint-pnp/sharepoint-pnp-cmdlets?view=sharepoint-ps)。</span><span class="sxs-lookup"><span data-stu-id="fe365-121">You can install and learn more about how to get started [here](https://docs.microsoft.com/powershell/sharepoint/sharepoint-pnp/sharepoint-pnp-cmdlets?view=sharepoint-ps).</span></span> <span data-ttu-id="fe365-122">您將使用下列命令登入您的網站或網站集合：</span><span class="sxs-lookup"><span data-stu-id="fe365-122">You will sign in to your site or site collection using this command:</span></span>

```powershell
Connect-PnPOnline -Url <yoursiteurl> -UseWebLogin
# this will prompt you to sign in to your site. Use the site owner credentials.
```

<span data-ttu-id="fe365-123">若要保持網站的傳統搜尋體驗，請執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="fe365-123">To stay with classic search experience for a site, run the following command:</span></span>

```powershell
Set-PnPSearchSettings -Scope Web -SearchBoxInNavBar ModernOnly
# ModernOnly | Inherit
```

<span data-ttu-id="fe365-124">或者，如果您想要為網站集合中的所有網站設定它，您可以使用此命令：</span><span class="sxs-lookup"><span data-stu-id="fe365-124">Alternately, if you want to set it for all the sites in a site collection, you can use this command:</span></span>

```powershell
Set-PnPSearchSettings -Scope Site -SearchBoxInNavBar ModernOnly
# ModernOnly | Inherit
```

## <a name="opting-into-microsoft-search"></a><span data-ttu-id="fe365-125">加入 Microsoft 搜尋</span><span class="sxs-lookup"><span data-stu-id="fe365-125">Opting into Microsoft Search</span></span>

<span data-ttu-id="fe365-126">針對不符合以上列出之準則的網站，或針對選擇要保持傳統之網站集合中的特定網站，您可以手動啟用 Microsoft 搜尋體驗。</span><span class="sxs-lookup"><span data-stu-id="fe365-126">For those sites that do not meet the criteria listed above, or for specific sites in a site collection that opted to stay in classic, you can manually enable the Microsoft Search experience.</span></span>

<span data-ttu-id="fe365-127">若要變更特定網站的此設定，您可以使用此命令：</span><span class="sxs-lookup"><span data-stu-id="fe365-127">To change this setting for a specific site, you can use this command:</span></span>

```powershell
Set-PnPSearchSettings -Scope Web -SearchBoxInNavBar AllPages
# AllPages | Inherit
```

<span data-ttu-id="fe365-128">若要為網站集合中的所有網站設定它，您可以使用此命令：</span><span class="sxs-lookup"><span data-stu-id="fe365-128">If you want to set it for all the sites in a site collection, you can use this command:</span></span>

```powershell
Set-PnPSearchSettings -Scope Site -SearchBoxInNavBar AllPages
# AllPages | Inherit
```

> [!NOTE]
> <span data-ttu-id="fe365-129">您可以針對包含 "STS"、"CMSPUBLISHING"、"BLANKINTERNET" 和「GROUP」 ) 的小組網站或發佈網站 (範本識別碼，手動啟用 Microsoft Search。</span><span class="sxs-lookup"><span data-stu-id="fe365-129">You can manually enable Microsoft Search only for a Team Site or Publishing Site (template ids that contain "STS", "CMSPUBLISHING", "BLANKINTERNET" and "GROUP").</span></span>
