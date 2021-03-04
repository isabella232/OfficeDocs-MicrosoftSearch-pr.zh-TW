---
title: Microsoft 搜尋的企業網站圖表連接器
ms.author: mecampos
author: mecampos
manager: umas
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 設定 Microsoft 搜尋的企業網站圖表連接器
ms.openlocfilehash: 7d71e6e3d775c97d8916e20ab032c312c269c5f1
ms.sourcegitcommit: 6a7522d9aeaedeedaac096c485d3f343ce98d3d2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "50421097"
---
<!---Previous ms.author: monaray --->

<!-- markdownlint-disable no-inline-html -->

# <a name="enterprise-websites-graph-connector"></a><span data-ttu-id="e79bc-103">企業網站圖表連接器</span><span class="sxs-lookup"><span data-stu-id="e79bc-103">Enterprise websites Graph connector</span></span>

<span data-ttu-id="e79bc-104">企業網站圖表連接器可讓您的組織對 **來自內部網站** 的文章和內容編制索引。</span><span class="sxs-lookup"><span data-stu-id="e79bc-104">The Enterprise websites Graph connector allows your organization to index articles and **content from its internal-facing websites**.</span></span> <span data-ttu-id="e79bc-105">在您設定網站的連接器及同步內容之後，使用者可以從任何 Microsoft 搜尋用戶端搜尋該內容。</span><span class="sxs-lookup"><span data-stu-id="e79bc-105">After you configure the connector and sync content from the website, end users can search for that content from any Microsoft Search client.</span></span>

> [!NOTE]
> <span data-ttu-id="e79bc-106">請閱讀 [**您的圖形連接器文章設定**](configure-connector.md) ，以瞭解一般圖表連接器設定程式。</span><span class="sxs-lookup"><span data-stu-id="e79bc-106">Read the [**Setup your Graph connector**](configure-connector.md) article to understand the general Graph connectors setup process.</span></span>

<span data-ttu-id="e79bc-107">本文適用于任何設定、執行及監視企業網站連接器的人員。</span><span class="sxs-lookup"><span data-stu-id="e79bc-107">This article is for anyone who configures, runs, and monitors an Enterprise websites connector.</span></span> <span data-ttu-id="e79bc-108">它會補充一般設定程式，並顯示只適用于企業網站連接器的指示。</span><span class="sxs-lookup"><span data-stu-id="e79bc-108">It supplements the general setup process, and shows instructions that apply only for the Enterprise websites connector.</span></span> <span data-ttu-id="e79bc-109">本文也包含 [疑難排解](#troubleshooting) 及 [限制](#limitations)的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e79bc-109">This article also includes information about [Troubleshooting](#troubleshooting) and [Limitations](#limitations).</span></span>

<!---## Before you get started-->

<!---Insert "Before you get started" recommendations for this data source-->

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a><span data-ttu-id="e79bc-110">步驟1：在 Microsoft 365 系統管理中心新增圖表連接器</span><span class="sxs-lookup"><span data-stu-id="e79bc-110">Step 1: Add a Graph connector in the Microsoft 365 admin center</span></span>

<span data-ttu-id="e79bc-111">遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。</span><span class="sxs-lookup"><span data-stu-id="e79bc-111">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-2-name-the-connection"></a><span data-ttu-id="e79bc-112">步驟2：命名連線</span><span class="sxs-lookup"><span data-stu-id="e79bc-112">Step 2: Name the connection</span></span>

<span data-ttu-id="e79bc-113">遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。</span><span class="sxs-lookup"><span data-stu-id="e79bc-113">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-3-configure-the-connection-settings"></a><span data-ttu-id="e79bc-114">步驟3：設定連接設定</span><span class="sxs-lookup"><span data-stu-id="e79bc-114">Step 3: Configure the connection settings</span></span>

<span data-ttu-id="e79bc-115">若要連線至您的資料來源，您必須填寫網站的根 URL、選擇編目來源，以及您想要使用的驗證類型： [無]、[基本驗證]，或 OAuth 2.0 搭配 [Azure Active Directory (AZURE AD) ](https://docs.microsoft.com/azure/active-directory/)。</span><span class="sxs-lookup"><span data-stu-id="e79bc-115">To connect to your data source, you need to fill in the root URL of the website, select a crawl source, and the type of authentication you'd like to use: None, Basic Authentication, or OAuth 2.0 with [Azure Active Directory (Azure AD)](https://docs.microsoft.com/azure/active-directory/).</span></span> <span data-ttu-id="e79bc-116">在您完成此資訊之後，請選取 [測試連線] 以驗證您的設定。</span><span class="sxs-lookup"><span data-stu-id="e79bc-116">After you complete this information, select Test Connection to verify your settings.</span></span>

> [!NOTE]
> <span data-ttu-id="e79bc-117">如果您要編目的網站已定義網站地圖，連接器將只會編目網站地圖中所列的 URLs。</span><span class="sxs-lookup"><span data-stu-id="e79bc-117">If the site you want to crawl has a sitemap defined, the connector will only crawl the URLs listed in the sitemap.</span></span> <span data-ttu-id="e79bc-118">若未定義網站地圖，連接器將會對該網站的根 URL 所找到的所有連結進行深入編目。</span><span class="sxs-lookup"><span data-stu-id="e79bc-118">If no sitemap is defined, the connector will do a deep crawl of all the links found on the root URL of the site.</span></span>

### <a name="url"></a><span data-ttu-id="e79bc-119">URL</span><span class="sxs-lookup"><span data-stu-id="e79bc-119">URL</span></span>

<span data-ttu-id="e79bc-120">使用 [URL] 欄位可指定您要編目之網站的根目錄。</span><span class="sxs-lookup"><span data-stu-id="e79bc-120">Use the URL field to specify the root of the website that you'd like to crawl.</span></span> <span data-ttu-id="e79bc-121">企業網站連接器會使用此 URL 做為開始點，並遵循此 URL 的所有連結進行編目。</span><span class="sxs-lookup"><span data-stu-id="e79bc-121">The enterprise websites connector will use this URL as the starting point and follow all the links from this URL for its crawl.</span></span>

### <a name="crawl-mode-cloud-or-on-premises-preview"></a><span data-ttu-id="e79bc-122">編目模式：雲端或內部部署 (預覽) </span><span class="sxs-lookup"><span data-stu-id="e79bc-122">Crawl mode: Cloud or On-premises (Preview)</span></span>

<span data-ttu-id="e79bc-123">編目模式會決定您要建立索引的網站類型（雲端或內部部署）。</span><span class="sxs-lookup"><span data-stu-id="e79bc-123">The crawl mode determines the type of websites you want to index, either cloud or on-premises.</span></span> <span data-ttu-id="e79bc-124">針對您的雲端網站，選取 **雲端** 做為編目模式。</span><span class="sxs-lookup"><span data-stu-id="e79bc-124">For your cloud websites, select **Cloud** as the crawl mode.</span></span>

<span data-ttu-id="e79bc-125">此外，連接器現在也支援對內部部署網站進行編目。</span><span class="sxs-lookup"><span data-stu-id="e79bc-125">Also, the connector now supports crawling of on-premises websites.</span></span> <span data-ttu-id="e79bc-126">此模式為預覽模式。</span><span class="sxs-lookup"><span data-stu-id="e79bc-126">This mode is in preview.</span></span> <span data-ttu-id="e79bc-127">若要存取您的內部部署資料，您必須先安裝及設定圖形連接器代理程式。</span><span class="sxs-lookup"><span data-stu-id="e79bc-127">To access your on-premises data, you must first install and configure the Graph connector agent.</span></span> <span data-ttu-id="e79bc-128">若要深入瞭解，請參閱 [Graph connector agent](https://docs.microsoft.com/microsoftsearch/on-prem-agent)。</span><span class="sxs-lookup"><span data-stu-id="e79bc-128">To learn more, see [Graph connector agent](https://docs.microsoft.com/microsoftsearch/on-prem-agent).</span></span>

<span data-ttu-id="e79bc-129">若為您的內部部署網站，請選取 [ **代理程式** ] 做為編目模式，並在 [部署中的 **代理程式** ] 欄位中，選擇您先前安裝及設定的圖形連接器代理程式。</span><span class="sxs-lookup"><span data-stu-id="e79bc-129">For your on-premises websites, select **Agent** as the crawl mode and in the **On-Prem Agent** field, choose the Graph connector agent that you installed and configured earlier.</span></span>  

> [!div class="mx-imgBorder"]
> <span data-ttu-id="e79bc-130">![商業網路連接器之連線設定窗格的螢幕擷取畫面](media/enterprise-web-connector/connectors-enterpriseweb-settings.png)</span><span class="sxs-lookup"><span data-stu-id="e79bc-130">![Screenshot of Connection Settings pane for Enterprise Web connector](media/enterprise-web-connector/connectors-enterpriseweb-settings.png)</span></span>

### <a name="authentication"></a><span data-ttu-id="e79bc-131">驗證</span><span class="sxs-lookup"><span data-stu-id="e79bc-131">Authentication</span></span>

<span data-ttu-id="e79bc-132">基本驗證需要使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="e79bc-132">Basic Authentication requires a username and password.</span></span> <span data-ttu-id="e79bc-133">使用 [Microsoft 365 系統管理中心](https://admin.microsoft.com)建立此 bot 帳戶。</span><span class="sxs-lookup"><span data-stu-id="e79bc-133">Create this bot account by using the [Microsoft 365 admin center](https://admin.microsoft.com).</span></span>

<span data-ttu-id="e79bc-134">使用 [AZURE AD](https://docs.microsoft.com/azure/active-directory/) OAuth 2.0 需要資源識別碼、用戶端識別碼和用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="e79bc-134">OAuth 2.0 with [Azure AD](https://docs.microsoft.com/azure/active-directory/) requires a resource ID, Client ID, and Client Secret.</span></span> <span data-ttu-id="e79bc-135">OAuth 2.0 僅適用于雲端模式。</span><span class="sxs-lookup"><span data-stu-id="e79bc-135">OAuth 2.0 only works with Cloud mode.</span></span>

<span data-ttu-id="e79bc-136">如需詳細資訊，請參閱 [使用 OAuth 2.0 程式碼授與流程授權存取 Azure Active Directory web 應用程式](https://docs.microsoft.com/azure/active-directory/develop/v1-protocols-oauth-code)。</span><span class="sxs-lookup"><span data-stu-id="e79bc-136">For more information, see [Authorize access to Azure Active Directory web applications using OAuth 2.0 code grant flow](https://docs.microsoft.com/azure/active-directory/develop/v1-protocols-oauth-code).</span></span> <span data-ttu-id="e79bc-137">使用下列值進行註冊：</span><span class="sxs-lookup"><span data-stu-id="e79bc-137">Register with the following values:</span></span>

<span data-ttu-id="e79bc-138">**名稱：** Microsoft 搜尋</span><span class="sxs-lookup"><span data-stu-id="e79bc-138">**Name:** Microsoft Search</span></span> <br/>
<span data-ttu-id="e79bc-139">**Redirect_URI：**`https://gcs.office.com/v1.0/admin/oauth/callback`</span><span class="sxs-lookup"><span data-stu-id="e79bc-139">**Redirect_URI:** `https://gcs.office.com/v1.0/admin/oauth/callback`</span></span>

<span data-ttu-id="e79bc-140">若要取得資源、client_id 及 client_secret 的值，請移至 **使用授權碼以要求** 重新導向 URL 網頁上的存取權杖。</span><span class="sxs-lookup"><span data-stu-id="e79bc-140">To get the values for the resource, client_id, and client_secret, go to **Use the authorization code to request an access token** on the redirect URL webpage.</span></span>

<span data-ttu-id="e79bc-141">如需詳細資訊，請參閱 [快速入門：使用 Microsoft identity Platform 註冊應用程式](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app)。</span><span class="sxs-lookup"><span data-stu-id="e79bc-141">For even more information, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

## <a name="step-3a-add-urls-to-exclude-optional-crawl-restrictions"></a><span data-ttu-id="e79bc-142">步驟3a：新增 URLs 以排除 (選擇性編目限制) </span><span class="sxs-lookup"><span data-stu-id="e79bc-142">Step 3a: Add URLs to exclude (Optional crawl restrictions)</span></span>

<span data-ttu-id="e79bc-143">有兩種方式可以避免網頁進行編目：在 robots.txt 檔案中禁止這些頁面，或將其新增至排除清單。</span><span class="sxs-lookup"><span data-stu-id="e79bc-143">There are two ways to prevent pages from being crawled: disallow them in your robots.txt file or add them to the Exclusion list.</span></span>

### <a name="support-for-robotstxt"></a><span data-ttu-id="e79bc-144">robots.txt 的支援</span><span class="sxs-lookup"><span data-stu-id="e79bc-144">Support for robots.txt</span></span>

<span data-ttu-id="e79bc-145">連接器會檢查您的根網站是否有 robots.txt 檔案，如果有的話，則會依照該檔案中所發現的指示來查看。</span><span class="sxs-lookup"><span data-stu-id="e79bc-145">The connector checks to see if there is a robots.txt file for your root site and, if one exists, it will follow and respect the directions found within that file.</span></span> <span data-ttu-id="e79bc-146">如果您不想讓連接器編目網站上的某些頁面或目錄，您可以在 robots.txt 檔案中的「禁止」宣告中呼叫這些頁面或目錄。</span><span class="sxs-lookup"><span data-stu-id="e79bc-146">If you do not want the connector to crawl certain pages or directories on your site, you can call out those pages or directories in the "Disallow" declarations in your robots.txt file.</span></span>

### <a name="add-urls-to-exclude"></a><span data-ttu-id="e79bc-147">新增要排除的 URLs</span><span class="sxs-lookup"><span data-stu-id="e79bc-147">Add URLs to exclude</span></span>

<span data-ttu-id="e79bc-148">您可以選擇性地建立 **排除清單** ，以排除部分 URLs 若該內容機密或不值得編目的情況，則無法取得編目。</span><span class="sxs-lookup"><span data-stu-id="e79bc-148">You can optionally create an **Exclusion list** to exclude some URLs from getting crawled if that content is sensitive or not worth crawling.</span></span> <span data-ttu-id="e79bc-149">若要建立排除清單，請流覽根 URL。</span><span class="sxs-lookup"><span data-stu-id="e79bc-149">To create an exclusion list, browse through the root URL.</span></span> <span data-ttu-id="e79bc-150">您可以在設定過程中將排除的 URLs 新增至清單。</span><span class="sxs-lookup"><span data-stu-id="e79bc-150">You can add the excluded URLs to the list during the configuration process.</span></span>

## <a name="step-4-assign-property-labels"></a><span data-ttu-id="e79bc-151">步驟4：指派屬性標籤</span><span class="sxs-lookup"><span data-stu-id="e79bc-151">Step 4: Assign property labels</span></span>

<span data-ttu-id="e79bc-152">您可以從選項的功能表中選擇，將 source 屬性指派給每個標籤。</span><span class="sxs-lookup"><span data-stu-id="e79bc-152">You can assign a source property to each label by choosing from a menu of options.</span></span> <span data-ttu-id="e79bc-153">雖然這個步驟不是必要的，但具有一些屬性標籤會提升搜尋相關性，並可確保使用者更準確的搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="e79bc-153">While this step is not mandatory, having some property labels will improve the search relevance and ensure more accurate search results for end users.</span></span>

## <a name="step-5-manage-schema"></a><span data-ttu-id="e79bc-154">步驟5：管理架構</span><span class="sxs-lookup"><span data-stu-id="e79bc-154">Step 5: Manage schema</span></span>

<span data-ttu-id="e79bc-155">在 [ **管理架構** ] 畫面上，您可以變更架構屬性 (選項包括「 **查詢**」、「 **搜尋**」、「 **檢索**」及「 **精煉** 」與屬性相關聯的) 、新增選用的別名，然後選擇 **Content** 屬性。</span><span class="sxs-lookup"><span data-stu-id="e79bc-155">On the **Manage Schema** screen, you can change the schema attributes (the options are **Query**, **Search**, **Retrieve**, and **Refine**) associated with the properties, add optional aliases, and choose the **Content** property.</span></span>

## <a name="step-6-manage-search-permissions"></a><span data-ttu-id="e79bc-156">步驟6：管理搜尋許可權</span><span class="sxs-lookup"><span data-stu-id="e79bc-156">Step 6: Manage search permissions</span></span>

<span data-ttu-id="e79bc-157">企業網站連接器只支援 **所有人都** 能看見的搜尋許可權。</span><span class="sxs-lookup"><span data-stu-id="e79bc-157">The Enterprise websites connector only supports search permissions visible to **Everyone**.</span></span> <span data-ttu-id="e79bc-158">已編制索引的資料會顯示在搜尋結果中，並對組織中的所有使用者顯示。</span><span class="sxs-lookup"><span data-stu-id="e79bc-158">Indexed data appears in the search results and is visible to all users in the organization.</span></span>

## <a name="step-7-set-the-refresh-schedule"></a><span data-ttu-id="e79bc-159">步驟7：設定重新整理排程</span><span class="sxs-lookup"><span data-stu-id="e79bc-159">Step 7: Set the refresh schedule</span></span>

<span data-ttu-id="e79bc-160">企業網站連接器只支援完整重新整理。</span><span class="sxs-lookup"><span data-stu-id="e79bc-160">The Enterprise websites connector only supports a full refresh.</span></span> <span data-ttu-id="e79bc-161">這表示連接器會在每次重新整理時重新編目網站的所有內容。</span><span class="sxs-lookup"><span data-stu-id="e79bc-161">This means that the connector will recrawl all the website's content during every refresh.</span></span> <span data-ttu-id="e79bc-162">若要確定連接器有足夠的時間來編目內容，建議您設定大型重新整理排程間隔。</span><span class="sxs-lookup"><span data-stu-id="e79bc-162">To make sure the connector gets enough time to crawl the content, we recommend that you set a large refresh schedule interval.</span></span> <span data-ttu-id="e79bc-163">建議您在一到兩周之間進行排程重新整理。</span><span class="sxs-lookup"><span data-stu-id="e79bc-163">We recommend a scheduled refresh between one and two weeks.</span></span>

## <a name="step-8-review-connection"></a><span data-ttu-id="e79bc-164">步驟8：檢查連線</span><span class="sxs-lookup"><span data-stu-id="e79bc-164">Step 8: Review connection</span></span>

<span data-ttu-id="e79bc-165">遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。</span><span class="sxs-lookup"><span data-stu-id="e79bc-165">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="troubleshooting"></a><span data-ttu-id="e79bc-166">疑難排解</span><span class="sxs-lookup"><span data-stu-id="e79bc-166">Troubleshooting</span></span>

<span data-ttu-id="e79bc-167">當閱讀網站內容時，編目可能會遇到一些來源錯誤，這些錯誤是由下列詳細的錯誤碼所代表。</span><span class="sxs-lookup"><span data-stu-id="e79bc-167">When reading the website's content, the crawl may encounter some source errors, which are represented by the detailed error codes below.</span></span> <span data-ttu-id="e79bc-168">若要取得錯誤類型的詳細資訊，請在選取連接後，移至 [ **錯誤詳細資料** ] 頁面。</span><span class="sxs-lookup"><span data-stu-id="e79bc-168">To get more information on the types of errors, go to the **error details** page after selecting the connection.</span></span> <span data-ttu-id="e79bc-169">選取 **錯誤碼** 以查看更詳細的錯誤。</span><span class="sxs-lookup"><span data-stu-id="e79bc-169">Select the **error code** to see more detailed errors.</span></span> <span data-ttu-id="e79bc-170">此外，請參閱 [管理您的連接器](https://docs.microsoft.com/microsoftsearch/manage-connector) 以深入瞭解。</span><span class="sxs-lookup"><span data-stu-id="e79bc-170">Also refer to [Manage your connector](https://docs.microsoft.com/microsoftsearch/manage-connector) to learn more.</span></span>

 <span data-ttu-id="e79bc-171">詳細錯誤代碼</span><span class="sxs-lookup"><span data-stu-id="e79bc-171">Detailed Error code</span></span> | <span data-ttu-id="e79bc-172">錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="e79bc-172">Error message</span></span>
 --- | ---
 <span data-ttu-id="e79bc-173">6001</span><span class="sxs-lookup"><span data-stu-id="e79bc-173">6001</span></span> | <span data-ttu-id="e79bc-174">無法連線正在嘗試編制索引的網站</span><span class="sxs-lookup"><span data-stu-id="e79bc-174">The site that is being tried to index is not reachable</span></span>
 <span data-ttu-id="e79bc-175">6005</span><span class="sxs-lookup"><span data-stu-id="e79bc-175">6005</span></span> | <span data-ttu-id="e79bc-176">根據 robots.txt 設定，已封鎖嘗試編制索引的來源頁面。</span><span class="sxs-lookup"><span data-stu-id="e79bc-176">The source page that is being tried to index has been blocked by as per robots.txt configuration.</span></span>
 <span data-ttu-id="e79bc-177">6008</span><span class="sxs-lookup"><span data-stu-id="e79bc-177">6008</span></span> | <span data-ttu-id="e79bc-178">無法解析 DNS</span><span class="sxs-lookup"><span data-stu-id="e79bc-178">Unable to resolve the DNS</span></span>
 <span data-ttu-id="e79bc-179">6009</span><span class="sxs-lookup"><span data-stu-id="e79bc-179">6009</span></span> | <span data-ttu-id="e79bc-180">針對所有用戶端錯誤 (除 HTTP 404、408) 以外，請參閱 HTTP 4xx 錯誤碼以取得詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="e79bc-180">For all client-side errors (Except HTTP 404, 408), refer to HTTP 4xx error codes for details.</span></span>
 <span data-ttu-id="e79bc-181">6013</span><span class="sxs-lookup"><span data-stu-id="e79bc-181">6013</span></span> | <span data-ttu-id="e79bc-182">找不到嘗試編制索引的來源頁面。</span><span class="sxs-lookup"><span data-stu-id="e79bc-182">The source page that is being tried to index could not be found.</span></span> <span data-ttu-id="e79bc-183"> (HTTP 404 錯誤) </span><span class="sxs-lookup"><span data-stu-id="e79bc-183">(HTTP 404 error)</span></span>
 <span data-ttu-id="e79bc-184">6018</span><span class="sxs-lookup"><span data-stu-id="e79bc-184">6018</span></span> | <span data-ttu-id="e79bc-185">來源頁面沒有回應，且要求超時。 (HTTP 408 錯誤) </span><span class="sxs-lookup"><span data-stu-id="e79bc-185">The source page is not responding, and the request has timed out. (HTTP 408 error)</span></span>
 <span data-ttu-id="e79bc-186">6021</span><span class="sxs-lookup"><span data-stu-id="e79bc-186">6021</span></span> | <span data-ttu-id="e79bc-187">嘗試編制索引的來源頁面沒有頁面上的文字內容。</span><span class="sxs-lookup"><span data-stu-id="e79bc-187">The source page that is being tried to index has no textual content on the page.</span></span>
 <span data-ttu-id="e79bc-188">6023</span><span class="sxs-lookup"><span data-stu-id="e79bc-188">6023</span></span> | <span data-ttu-id="e79bc-189">嘗試編制索引的來源頁面不受支援 (不是 HTML 頁面) </span><span class="sxs-lookup"><span data-stu-id="e79bc-189">The source page that is being tried to index is unsupported (not an HTML page)</span></span>
 <span data-ttu-id="e79bc-190">6024</span><span class="sxs-lookup"><span data-stu-id="e79bc-190">6024</span></span> | <span data-ttu-id="e79bc-191">嘗試編制索引的來源頁面具有不支援的內容。</span><span class="sxs-lookup"><span data-stu-id="e79bc-191">The source page that is being tried to index has unsupported content.</span></span>

* <span data-ttu-id="e79bc-192">當資料來源由於網路問題或資料來源本身被刪除、移動或重新命名時，就會發生錯誤6001-6013。</span><span class="sxs-lookup"><span data-stu-id="e79bc-192">Errors 6001-6013 occur when the data source is not reachable due to a network issue or when the data source itself is deleted, moved, or renamed.</span></span> <span data-ttu-id="e79bc-193">檢查提供的資料來源詳細資料是否仍然有效。</span><span class="sxs-lookup"><span data-stu-id="e79bc-193">Check if the data source details provided are still valid.</span></span>
* <span data-ttu-id="e79bc-194">當資料來源包含頁面上的非文字內容或頁面不是 HTML 時，就會發生錯誤6021-6024。</span><span class="sxs-lookup"><span data-stu-id="e79bc-194">Errors 6021-6024 occur when the data source contains non-textual content on the page or when the page is not an HTML.</span></span> <span data-ttu-id="e79bc-195">請檢查資料來源，並將此頁面加入排除清單，或略過錯誤。</span><span class="sxs-lookup"><span data-stu-id="e79bc-195">Check the data source and add this page in exclusion list or ignore the error.</span></span>

## <a name="limitations"></a><span data-ttu-id="e79bc-196">限制</span><span class="sxs-lookup"><span data-stu-id="e79bc-196">Limitations</span></span>

<span data-ttu-id="e79bc-197">企業網站連接器不支援搜尋 **動態網頁** 上的資料。</span><span class="sxs-lookup"><span data-stu-id="e79bc-197">The Enterprise websites connector doesn't support searching data on **dynamic webpages**.</span></span> <span data-ttu-id="e79bc-198">[Confluence](https://www.atlassian.com/software/confluence)與[Unily](https://www.unily.com/)等內容管理系統中的這些網頁範例，或儲存網站內容的資料庫。</span><span class="sxs-lookup"><span data-stu-id="e79bc-198">Examples of those webpages live in content management systems like [Confluence](https://www.atlassian.com/software/confluence) and [Unily](https://www.unily.com/) or databases that store website content.</span></span>