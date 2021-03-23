---
title: 在 SharePoint 網站中管理搜尋方塊
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
description: 如何在 SharePoint 網站上自訂搜尋框體驗
ms.openlocfilehash: c58e7cf0a47d22fa9c6fd3abd93cc97087625690
ms.sourcegitcommit: 5df252e6d0bd67bb1b4c59418aceca8369f5fe42
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/23/2021
ms.locfileid: "51031357"
---
# <a name="search-box-settings-on-sharepoint-sites"></a><span data-ttu-id="a0ac1-103">SharePoint 網站上的搜尋方塊設定</span><span class="sxs-lookup"><span data-stu-id="a0ac1-103">Search box settings on SharePoint sites</span></span>

<span data-ttu-id="a0ac1-104">在 SharePoint 網站上可自訂的幾種方式之一，是要調整套件導覽列中的搜尋方塊在 SharePoint 網站中的運作方式，以最適合您的需求。</span><span class="sxs-lookup"><span data-stu-id="a0ac1-104">One of the several ways Microsoft Search can be customized on SharePoint sites is to tailor how the search box in the suite navigation bar works in SharePoint sites to best fit your needs.</span></span>

<span data-ttu-id="a0ac1-105">如需其他自訂選項，請參閱 [變更 Microsoft 搜尋結果頁面以新增自訂的縱向、結果類型及佈局](customize-search-page.md)，以及 [建立自訂搜尋結果頁面](create-search-results-pages.md)。</span><span class="sxs-lookup"><span data-stu-id="a0ac1-105">For other customization options, see [Changing the Microsoft Search results page to add custom verticals, result types and layouts](customize-search-page.md), and [Creating a custom search results page](create-search-results-pages.md).</span></span>

> [!NOTE]
> <span data-ttu-id="a0ac1-106">現在所有客戶都無法使用 [套件導覽列] 搜尋方塊，但這些選項仍可供設定，而且會在可用時生效。</span><span class="sxs-lookup"><span data-stu-id="a0ac1-106">The suite navigation bar search box is not available for all customers at this time, but these options can still be set now and they will take effect when it becomes available.</span></span>

<span data-ttu-id="a0ac1-107">對於下列所列的工作，您將使用 PowerShell 搭配 SharePoint PnP PowerShell 擴充。</span><span class="sxs-lookup"><span data-stu-id="a0ac1-107">For the tasks listed below, you will use PowerShell with SharePoint PnP PowerShell extensions.</span></span> <span data-ttu-id="a0ac1-108">您可以安裝並深入瞭解如何開始 [這裡](/powershell/sharepoint/sharepoint-pnp/sharepoint-pnp-cmdlets?view=sharepoint-ps)。</span><span class="sxs-lookup"><span data-stu-id="a0ac1-108">You can install and learn more about how to get started [here](/powershell/sharepoint/sharepoint-pnp/sharepoint-pnp-cmdlets?view=sharepoint-ps).</span></span> <span data-ttu-id="a0ac1-109">您將使用下列命令登入您的網站或網站集合：</span><span class="sxs-lookup"><span data-stu-id="a0ac1-109">You will sign into your site or site collection using this command:</span></span>

```powershell
Connect-PnPOnline -Url <yoursiteurl> -UseWebLogin
# this will prompt you to sign into your site. Use the site owner credentials 
```

## <a name="changing-the-scope-of-search"></a><span data-ttu-id="a0ac1-110">變更搜尋範圍</span><span class="sxs-lookup"><span data-stu-id="a0ac1-110">Changing the scope of search</span></span>

<span data-ttu-id="a0ac1-111">當您今天在 SharePoint Online 中建立新的網站，並在 [搜尋] 方塊中輸入時，您會進入 [Microsoft 搜尋結果] 頁面。</span><span class="sxs-lookup"><span data-stu-id="a0ac1-111">When you create a new site in SharePoint Online today, and type into the search box, you are taken to the Microsoft Search results page.</span></span> <span data-ttu-id="a0ac1-112">此頁面預設會顯示目前網站的結果，並可讓您將搜尋範圍擴充至目前網站 (關聯的中樞（如果有一個) 或整個組織）。</span><span class="sxs-lookup"><span data-stu-id="a0ac1-112">This page shows results from your current site by default and allows you to expand the scope of your search to the hub that the current site is associated with (if there is one), or to the whole organization.</span></span>

<span data-ttu-id="a0ac1-113">[搜尋] 方塊預設使用的範圍取決於網站類型。</span><span class="sxs-lookup"><span data-stu-id="a0ac1-113">The scope the search box uses, by default, depends on type of site.</span></span>

* <span data-ttu-id="a0ac1-114">一般網站會搜尋目前的網站。</span><span class="sxs-lookup"><span data-stu-id="a0ac1-114">Regular sites search over the current site.</span></span>
* <span data-ttu-id="a0ac1-115">Hub sites 透過 hub 中的所有網站搜尋。</span><span class="sxs-lookup"><span data-stu-id="a0ac1-115">Hub sites search over all sites in the hub.</span></span>
* <span data-ttu-id="a0ac1-116">家庭網站搜尋所有內容。</span><span class="sxs-lookup"><span data-stu-id="a0ac1-116">Home sites search over all content.</span></span>

<span data-ttu-id="a0ac1-117">在某些情況下，您可能會想要變更這些預設值，以無條件搜尋整個組織或與網站相關聯的 hub，而不需要另外按一下。</span><span class="sxs-lookup"><span data-stu-id="a0ac1-117">In some cases, you may want to change these defaults to always search over the whole organization, or across the hub a site is associated with, without needing an additional click.</span></span>

<span data-ttu-id="a0ac1-118">網站擁有者，您可以使用下列命令變更這些預設值：</span><span class="sxs-lookup"><span data-stu-id="a0ac1-118">As a site owner, you can change these defaults using the following command:</span></span>

```powershell
Set-PnPSearchSettings -SearchScope Tenant
# DefaultScope | Hub | Site | Tenant
```

<span data-ttu-id="a0ac1-119">執行這個命令之後，以前顯示目前網站的結果的網站預設會從整個組織開始顯示結果。</span><span class="sxs-lookup"><span data-stu-id="a0ac1-119">After running this command, the site that was previously showing results from the current site by default will start to show results from the whole organization.</span></span>

<span data-ttu-id="a0ac1-120">若要回到預設設定，請使用值 "DefaultScope" 重新執行命令。</span><span class="sxs-lookup"><span data-stu-id="a0ac1-120">To go back to the default setting, run the command again with the value “DefaultScope".</span></span> <span data-ttu-id="a0ac1-121">若要在 Hub 中搜尋，請使用「Hub」做為 SearchScope 值。</span><span class="sxs-lookup"><span data-stu-id="a0ac1-121">To search across the Hub, use “Hub” as the SearchScope value.</span></span>

<span data-ttu-id="a0ac1-122">此設定適用于個別網站層級。</span><span class="sxs-lookup"><span data-stu-id="a0ac1-122">This setting applies at the individual site level.</span></span> <span data-ttu-id="a0ac1-123">網站集合沒有同等的設定。</span><span class="sxs-lookup"><span data-stu-id="a0ac1-123">There is no equivalent setting for site collections.</span></span>

## <a name="show-or-hide-the-search-box"></a><span data-ttu-id="a0ac1-124">顯示或隱藏搜尋方塊</span><span class="sxs-lookup"><span data-stu-id="a0ac1-124">Show or hide the search box</span></span>

<span data-ttu-id="a0ac1-125">如果您想要防止使用者搜尋或使用自訂搜尋框的實施，您可以選擇隱藏 [套件導覽列搜尋] 方塊。</span><span class="sxs-lookup"><span data-stu-id="a0ac1-125">You can choose to hide the suite navigation bar search box if you want to prevent your users from searching or to use a custom search box implementation.</span></span>

<span data-ttu-id="a0ac1-126">若要變更特定網站的此設定，請使用此命令：</span><span class="sxs-lookup"><span data-stu-id="a0ac1-126">To change this setting for a given site use this command:</span></span>

```powershell
Set-PnPSearchSettings -Scope Web -SearchBoxInNavBar Hidden
# Hidden | Inherit
```

<span data-ttu-id="a0ac1-127">或者，如果您想要為網站集合中的所有網站設定它，您可以使用此命令：</span><span class="sxs-lookup"><span data-stu-id="a0ac1-127">Alternately, if you want to set it for all the sites in a site collection, you can use this command:</span></span>

```powershell
Set-PnPSearchSettings -Scope Site -SearchBoxInNavBar Hidden
# Hidden | Inherit
```

<span data-ttu-id="a0ac1-128">執行這些命令之後，搜尋方塊將不再顯示在頁面頂端的導覽列中。</span><span class="sxs-lookup"><span data-stu-id="a0ac1-128">After running these commands, the search box will no longer show up in the navigation bar on top of your page.</span></span> <span data-ttu-id="a0ac1-129">若要回到顯示搜尋方塊，請使用提供給 "SearchBoxInNavBar" 參數的值，再次執行命令以「Inherit」。</span><span class="sxs-lookup"><span data-stu-id="a0ac1-129">To go back to showing the search box, run the commands again with the value provided to "SearchBoxInNavBar" parameter to “Inherit”.</span></span>

<span data-ttu-id="a0ac1-130">請考慮下列幾點：</span><span class="sxs-lookup"><span data-stu-id="a0ac1-130">There are several points to consider:</span></span>

* <span data-ttu-id="a0ac1-131">此設定僅適用于套件導覽列中的 [搜尋] 方塊。</span><span class="sxs-lookup"><span data-stu-id="a0ac1-131">This setting only applies to the search box in the suite navigation bar.</span></span> <span data-ttu-id="a0ac1-132">它不會套用到頁面中的搜尋方塊，也不會套用到傳統頁面上的搜尋方塊。</span><span class="sxs-lookup"><span data-stu-id="a0ac1-132">It does not apply to search boxes that are in the page, or to search boxes on classic pages.</span></span>

* <span data-ttu-id="a0ac1-133">當您停用導覽列中的 [搜尋] 方塊時，如果您想要在網站中搜尋功能，您必須使用自訂網頁元件或 SharePoint 架構擴充，自行提供。</span><span class="sxs-lookup"><span data-stu-id="a0ac1-133">Once you’ve disabled the search box in the navigation bar, if you want search functionality in your site, you will have to provide it yourself using a custom web part or a SharePoint Framework extension.</span></span>

* <span data-ttu-id="a0ac1-134">此方案也會從網站的清單和文件庫中移除搜尋方塊。</span><span class="sxs-lookup"><span data-stu-id="a0ac1-134">This solution will remove the search box from lists and libraries for your site as well.</span></span> <span data-ttu-id="a0ac1-135">除了整個網站搜尋之外，您的自訂搜尋解決方案也必須考慮 SharePoint 清單和文件庫的內容搜尋。</span><span class="sxs-lookup"><span data-stu-id="a0ac1-135">Your custom search solution will need to consider contextual searches for SharePoint lists and libraries, in addition to site-wide search.</span></span>

* <span data-ttu-id="a0ac1-136">如果您將設定套用至網域的根網站，則 SharePoint 開始頁面也會停止顯示搜尋方塊。</span><span class="sxs-lookup"><span data-stu-id="a0ac1-136">If you apply the setting to the root site of your domain, the SharePoint start page will also stop showing the search box.</span></span>

## <a name="changing-the-hint-displayed-in-the-search-box"></a><span data-ttu-id="a0ac1-137">變更搜尋方塊中顯示的提示</span><span class="sxs-lookup"><span data-stu-id="a0ac1-137">Changing the hint displayed in the search box</span></span>

<span data-ttu-id="a0ac1-138">您可以針對指定的網站或網站集合變更搜尋方塊所顯示的提示。</span><span class="sxs-lookup"><span data-stu-id="a0ac1-138">You can change the hint the search box shows for a given site or site collection.</span></span> <span data-ttu-id="a0ac1-139">這是在開始輸入文字之前，出現在搜尋方塊中的文字。</span><span class="sxs-lookup"><span data-stu-id="a0ac1-139">This is the text that appears in the search box before they start typing into it.</span></span> <span data-ttu-id="a0ac1-140">當您已設定自訂結果頁面或以其他方式變更搜尋行為時，這可協助您指導使用者如何進行搜尋。</span><span class="sxs-lookup"><span data-stu-id="a0ac1-140">This may help guide your users about what to expect from search if you’ve configured a custom results page or changed behavior of search in other ways.</span></span>

> [!NOTE]
> <span data-ttu-id="a0ac1-141">若要進行這項變更，您必須允許以租使用者管理員的身分在網站上執行自訂腳本，此為預設不允許的使用者。</span><span class="sxs-lookup"><span data-stu-id="a0ac1-141">To be able to make this change, you need to allow running custom scripts on the site in question as a tenant administrator, which is disallowed by default.</span></span> <span data-ttu-id="a0ac1-142">如需 https://docs.microsoft.com/sharepoint/allow-or-prevent-custom-script 詳細資訊，請參閱。</span><span class="sxs-lookup"><span data-stu-id="a0ac1-142">Please see https://docs.microsoft.com/sharepoint/allow-or-prevent-custom-script for details.</span></span> <span data-ttu-id="a0ac1-143">您可以在必要時，允許執行自訂腳本，進行變更，然後再回復至禁止網站的腳本。</span><span class="sxs-lookup"><span data-stu-id="a0ac1-143">You can allow running custom scripts, make the change, and then revert to disallowing scripts for the site if necessary.</span></span>

<span data-ttu-id="a0ac1-144">若要變更特定網站的此設定，請執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="a0ac1-144">To change this setting for a given site run the following command:</span></span>

```powershell
Set-PnPSearchSettings -Scope Web -SearchBoxPlaceholderText "my placeholder" 
```

<span data-ttu-id="a0ac1-145">或者，如果您想要為網站集合中的所有網站設定它，您可以使用此命令：</span><span class="sxs-lookup"><span data-stu-id="a0ac1-145">Alternately, if you want to set it for all the sites in a site collection, you can use this command:</span></span>

```powershell
Set-PnPSearchSettings -Scope Site -SearchBoxPlaceholderText "my placeholder" 
```

<span data-ttu-id="a0ac1-146">若要回到預設的預留位置文字，請將值設為空白 ( "" ) 。</span><span class="sxs-lookup"><span data-stu-id="a0ac1-146">To go back to the default placeholder text, set the value to be blank ("").</span></span>