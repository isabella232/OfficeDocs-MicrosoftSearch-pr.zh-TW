---
title: 在 SharePoint Online 中建立自訂搜尋結果頁面
ms.author: jeffkizn
author: jeffkizn
manager: jeffkizn
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
description: 建立您自己的 SharePoint Online 網站的搜尋結果頁面
ms.openlocfilehash: b5abb25f15795389dd8b6d5683ac336af7422e0a
ms.sourcegitcommit: 5df252e6d0bd67bb1b4c59418aceca8369f5fe42
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/23/2021
ms.locfileid: "51031636"
---
# <a name="create-a-custom-search-results-page-in-sharepoint-online"></a><span data-ttu-id="ce003-103">在 SharePoint Online 中建立自訂搜尋結果頁面</span><span class="sxs-lookup"><span data-stu-id="ce003-103">Create a custom search results page in SharePoint Online</span></span>

<span data-ttu-id="ce003-104">在 SharePoint 中自訂搜尋體驗的一種方式是建立網站的自訂搜尋結果頁面。</span><span class="sxs-lookup"><span data-stu-id="ce003-104">One way to customize the search experience in SharePoint is to create a custom search results page for a site.</span></span> <span data-ttu-id="ce003-105">這可讓您使用您建立的頁面，而不是 Microsoft 搜尋結果頁面的預設值。</span><span class="sxs-lookup"><span data-stu-id="ce003-105">This allows you to use a page that you created, rather than the default in Microsoft Search results page.</span></span> <span data-ttu-id="ce003-106">這可讓您更靈活地瞭解搜尋結果的體驗對您的使用者的外觀。</span><span class="sxs-lookup"><span data-stu-id="ce003-106">This gives you more flexibility on how the search results experience looks for your users.</span></span>

>[!NOTE]
> <span data-ttu-id="ce003-107">若要變更預設可供使用的預設 Microsoft 搜尋結果頁面，請參閱 [自訂搜尋結果頁面](customize-search-page.md)。</span><span class="sxs-lookup"><span data-stu-id="ce003-107">To make changes to the default Microsoft Search results page that is available by default, please see [Customize the search results page](customize-search-page.md).</span></span>

<span data-ttu-id="ce003-108">使用自訂結果頁面，您可以建立新的頁面，用來控制搜尋結果的版面配置及設計，以支援組織的需求。</span><span class="sxs-lookup"><span data-stu-id="ce003-108">With a custom results page you can create a new page that can be used to control the layout and design of search results to support your organization's needs.</span></span> <span data-ttu-id="ce003-109">您可以使用來自 SharePoint 模式和慣例群組的任何內建網頁元件、開啟來源搜尋網頁元件，以及您使用 SharePoint Framework 開發的任何自訂網頁元件。</span><span class="sxs-lookup"><span data-stu-id="ce003-109">You can use any built-in web parts, open-source search web parts from SharePoint Patterns and Practices community, as well as any custom web parts that you may have developed using SharePoint Framework.</span></span>

## <a name="configure-a-results-page"></a><span data-ttu-id="ce003-110">設定結果頁面</span><span class="sxs-lookup"><span data-stu-id="ce003-110">Configure a results page</span></span>

<span data-ttu-id="ce003-111">若要在 SharePoint Online 中設定自訂結果頁面，請依照下列步驟進行：</span><span class="sxs-lookup"><span data-stu-id="ce003-111">To configure a custom results page in SharePoint Online follow the steps below:</span></span>

1. <span data-ttu-id="ce003-112">流覽至您要設定自訂結果頁面的網站，然後移至 [ **網站設定 > 網站集合設定 > 搜尋設定**]。</span><span class="sxs-lookup"><span data-stu-id="ce003-112">Browse to the site where you would like to configure a custom results page and go to **Site Settings > Site Collection Settings > Search Settings**.</span></span>

2. <span data-ttu-id="ce003-113">在 [搜尋設定] 中，清除 **[選取使用與我的父代相同的結果頁面設定**]，選擇 [ **將查詢傳送至自訂結果] 頁面**，然後為 [結果] **頁面 URL:** 提供值。</span><span class="sxs-lookup"><span data-stu-id="ce003-113">In Search Settings, clear selection from **Use the same results page settings as my parent**, choose **Send queries to a custom results page**, and provide a value for **Results page URL:**.</span></span> <span data-ttu-id="ce003-114">然後，儲存您的變更。</span><span class="sxs-lookup"><span data-stu-id="ce003-114">Then, save your changes.</span></span> <span data-ttu-id="ce003-115">您在這裡使用的 URL 應針對您建立用來做為自訂結果頁面的頁面。</span><span class="sxs-lookup"><span data-stu-id="ce003-115">The URL you use here should be for the page that you created to use as your custom results page.</span></span>

>[!NOTE]
> <span data-ttu-id="ce003-116">自訂結果頁面必須與您的網站位於相同的網域，但不一定要在相同的網站集合中。</span><span class="sxs-lookup"><span data-stu-id="ce003-116">The custom results page needs to be on the same domain as your site, but it does not have to be in the same site collection.</span></span>  

<span data-ttu-id="ce003-117">或者，您也可以使用 [PnPSearchSettings SharePoint PnP PowerShell 命令](/powershell/module/sharepoint-pnp/set-pnpsearchsettings?view=sharepoint-ps) 來設定值，而不是使用 [網站設定] 頁面。</span><span class="sxs-lookup"><span data-stu-id="ce003-117">Alternatively, you can use the [Set-PnPSearchSettings SharePoint PnP PowerShell command](/powershell/module/sharepoint-pnp/set-pnpsearchsettings?view=sharepoint-ps) to set the value instead of using the Site Settings page.</span></span>

<span data-ttu-id="ce003-118">設定之後，當您使用頁面頂端的導覽列中所顯示的 [Microsoft 搜尋] 方塊進行搜尋時，就會顯示 [自訂搜尋結果] 頁面，當您從網站頁面或網站的首頁輸入搜尋時，會使用該對話方塊。</span><span class="sxs-lookup"><span data-stu-id="ce003-118">Once set, the custom search results page is displayed when you search using the Microsoft Search box that appears in the navigation bar on top of the page and is used when you enter search from site pages or the home page of the site.</span></span> <span data-ttu-id="ce003-119">當您在清單、文件庫或 [網站內容] 頁面中進行搜尋時，不會使用此功能。</span><span class="sxs-lookup"><span data-stu-id="ce003-119">It is not used when you are searching within a list, library, or the site contents page.</span></span> <span data-ttu-id="ce003-120">您可以使用連結從清單和文件庫中的搜尋結果展開搜尋，以取得自訂結果頁面。</span><span class="sxs-lookup"><span data-stu-id="ce003-120">You may use the link to expand your search from search results in lists and libraries to get to the custom results page.</span></span>

## <a name="change-the-layout-of-your-custom-results-page"></a><span data-ttu-id="ce003-121">變更自訂結果頁面的版面配置</span><span class="sxs-lookup"><span data-stu-id="ce003-121">Change the layout of your custom results page</span></span>

<span data-ttu-id="ce003-122">名為 **HeaderlessSearchResults** 的頁面配置可用於讓搜尋結果頁面看起來更接近我們的現成搜尋結果體驗。</span><span class="sxs-lookup"><span data-stu-id="ce003-122">A page layout named **HeaderlessSearchResults** can be used to make the search results page appear closer to our out of box search results experience.</span></span> <span data-ttu-id="ce003-123">只有設定為自訂搜尋結果頁面的頁面才能使用這種新的版面配置。</span><span class="sxs-lookup"><span data-stu-id="ce003-123">This new layout can only be active for the pages that are set to be the custom search results page.</span></span>

<span data-ttu-id="ce003-124">若要設定頁面配置，您可以使用 [PnPClientSidePageSharePoint PnP PowerShell 命令](/powershell/module/sharepoint-pnp/set-pnpclientsidepage?view=sharepoint-ps) 搭配-LayoutType HeaderlessSearchResults。</span><span class="sxs-lookup"><span data-stu-id="ce003-124">To set the page layout, you can use the [Set-PnPClientSidePageSharePoint PnP PowerShell command](/powershell/module/sharepoint-pnp/set-pnpclientsidepage?view=sharepoint-ps) with -LayoutType HeaderlessSearchResults.</span></span>

## <a name="use-sharepoint-framework-query-extensions"></a><span data-ttu-id="ce003-125">使用 SharePoint 架構查詢擴充</span><span class="sxs-lookup"><span data-stu-id="ce003-125">Use SharePoint Framework Query extensions</span></span>

<span data-ttu-id="ce003-126">自訂搜尋結果頁面也可以使用 [SharePoint 架構查詢延伸](/sharepoint/dev/spfx/building-search-extensions) ，在將查詢傳送至搜尋引擎之前修改查詢。</span><span class="sxs-lookup"><span data-stu-id="ce003-126">Custom search results pages can also make use of the [SharePoint Framework Query Extension](/sharepoint/dev/spfx/building-search-extensions) to modify the query before it gets sent to the search engine.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ce003-127">其他資源</span><span class="sxs-lookup"><span data-stu-id="ce003-127">Additional resources</span></span>

<span data-ttu-id="ce003-128">若要深入瞭解自訂結果頁面，請參閱我們的 [Ignite 2019 搜尋自訂和開發會話](https://myignite.techcommunity.microsoft.com/sessions/85238?source=sessions)。</span><span class="sxs-lookup"><span data-stu-id="ce003-128">To learn more about custom results page, check out our [Ignite 2019 Search Customization and Development session](https://myignite.techcommunity.microsoft.com/sessions/85238?source=sessions).</span></span>

<span data-ttu-id="ce003-129">針對「開啟來源」專案、開始使用 Microsoft 搜尋 APIs，以及更多自訂及擴充性範例，請 [在 GitHub 上流覽 Microsoft 搜尋](https://github.com/microsoft-search)。</span><span class="sxs-lookup"><span data-stu-id="ce003-129">For open source projects, getting started with our Microsoft Search APIs, and more customization and extensibility samples, visit [Microsoft Search on GitHub](https://github.com/microsoft-search).</span></span>