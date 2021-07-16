---
title: Enterprise Microsoft 搜尋的網站 Graph 連接器
ms.author: mecampos
author: mecampos
manager: umas
audience: Admin
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 設定 Enterprise 的網站 Graph 連接器 Microsoft 搜尋
ms.openlocfilehash: 32e38c9bef036556dae2734e23b1d26ba4fe2c27
ms.sourcegitcommit: 38a0f09596c2bca0e12bf4cada7b4c64fd4c48e4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/15/2021
ms.locfileid: "53449043"
---
<!---Previous ms.author: monaray --->

<!-- markdownlint-disable no-inline-html -->

# <a name="enterprise-websites-graph-connector"></a><span data-ttu-id="c253e-103">Enterprise 網站 Graph 連接器</span><span class="sxs-lookup"><span data-stu-id="c253e-103">Enterprise websites Graph connector</span></span>

<span data-ttu-id="c253e-104">Enterprise 網站 Graph 連接器可讓您的組織編制 **來自內部網站** 的文章和內容。</span><span class="sxs-lookup"><span data-stu-id="c253e-104">The Enterprise websites Graph connector allows your organization to index articles and **content from its internal-facing websites**.</span></span> <span data-ttu-id="c253e-105">從網站設定連接器及同步內容之後，使用者可以從任何 Microsoft 搜尋用戶端搜尋該內容。</span><span class="sxs-lookup"><span data-stu-id="c253e-105">After you configure the connector and sync content from the website, end users can search for that content from any Microsoft Search client.</span></span>

> [!NOTE]
> <span data-ttu-id="c253e-106">請閱讀 [**設定 Graph 連接器**](configure-connector.md)文章，以瞭解一般 Graph 連接器設定指示。</span><span class="sxs-lookup"><span data-stu-id="c253e-106">Read the [**Setup your Graph connector**](configure-connector.md) article to understand the general Graph connectors setup instructions.</span></span>

<span data-ttu-id="c253e-107">本文適用于任何設定、執行及監視 Enterprise 網站連接器的人員。</span><span class="sxs-lookup"><span data-stu-id="c253e-107">This article is for anyone who configures, runs, and monitors an Enterprise websites connector.</span></span> <span data-ttu-id="c253e-108">它會補充一般設定程式，並顯示只適用于 Enterprise 網站連接器的指示。</span><span class="sxs-lookup"><span data-stu-id="c253e-108">It supplements the general setup process, and shows instructions that apply only for the Enterprise websites connector.</span></span> <span data-ttu-id="c253e-109">本文也包含 [疑難排解](#troubleshooting)的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c253e-109">This article also includes information about [Troubleshooting](#troubleshooting).</span></span>

<!---## Before you get started-->

<!---Insert "Before you get started" recommendations for this data source-->

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a><span data-ttu-id="c253e-110">步驟1：在 Microsoft 365 系統管理中心中新增 Graph 連接器</span><span class="sxs-lookup"><span data-stu-id="c253e-110">Step 1: Add a Graph connector in the Microsoft 365 admin center</span></span>

<span data-ttu-id="c253e-111">遵循一般 [設定指示](./configure-connector.md)。</span><span class="sxs-lookup"><span data-stu-id="c253e-111">Follow the general [setup instructions](./configure-connector.md).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-2-name-the-connection"></a><span data-ttu-id="c253e-112">步驟2：命名連線</span><span class="sxs-lookup"><span data-stu-id="c253e-112">Step 2: Name the connection</span></span>

<span data-ttu-id="c253e-113">遵循一般 [設定指示](./configure-connector.md)。</span><span class="sxs-lookup"><span data-stu-id="c253e-113">Follow the general [setup instructions](./configure-connector.md).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-3-configure-the-connection-settings"></a><span data-ttu-id="c253e-114">步驟3：設定連接設定</span><span class="sxs-lookup"><span data-stu-id="c253e-114">Step 3: Configure the connection settings</span></span>

<span data-ttu-id="c253e-115">若要連線至您的資料來源，請填入網站的根 URL、選擇編目來源，以及您想要使用的驗證類型： [無]、[基本驗證]，或 OAuth 2.0 搭配[Azure Active Directory (Azure AD) ](/azure/active-directory/)。</span><span class="sxs-lookup"><span data-stu-id="c253e-115">To connect to your data source, fill in the root URL of the website, select a crawl source, and the type of authentication you'd like to use: None, Basic Authentication, or OAuth 2.0 with [Azure Active Directory (Azure AD)](/azure/active-directory/).</span></span> <span data-ttu-id="c253e-116">在您完成此資訊之後，請選取 [測試連線] 以驗證您的設定。</span><span class="sxs-lookup"><span data-stu-id="c253e-116">After you complete this information, select Test Connection to verify your settings.</span></span>

### <a name="url"></a><span data-ttu-id="c253e-117">URL</span><span class="sxs-lookup"><span data-stu-id="c253e-117">URL</span></span>

<span data-ttu-id="c253e-118">使用 [URL] 欄位可指定您要編目之網站的根目錄。</span><span class="sxs-lookup"><span data-stu-id="c253e-118">Use the URL field to specify the root of the website that you'd like to crawl.</span></span> <span data-ttu-id="c253e-119">企業網站連接器會使用此 URL 做為開始點，並遵循此 URL 的所有連結進行編目。</span><span class="sxs-lookup"><span data-stu-id="c253e-119">The enterprise websites connector will use this URL as the starting point and follow all the links from this URL for its crawl.</span></span>

### <a name="crawl-websites-listed-in-the-sitemap"></a><span data-ttu-id="c253e-120">編目網站地圖中所列的網站</span><span class="sxs-lookup"><span data-stu-id="c253e-120">Crawl websites listed in the sitemap</span></span>

<span data-ttu-id="c253e-121">選取此選項時，連接器只會編目網站地圖中所列的 URLs。</span><span class="sxs-lookup"><span data-stu-id="c253e-121">When selected the connector will only crawl the URLs listed in the sitemap.</span></span> <span data-ttu-id="c253e-122">若未選取或未找到任何網站圖形，連接器將會對該網站的根 URL 所找到的所有連結進行深入編目。</span><span class="sxs-lookup"><span data-stu-id="c253e-122">If not selected or no site map is found, the connector will do a deep crawl of all the links found on the root URL of the site.</span></span>

### <a name="dynamic-site-configuration"></a><span data-ttu-id="c253e-123">動態網站設定</span><span class="sxs-lookup"><span data-stu-id="c253e-123">Dynamic site configuration</span></span>

<span data-ttu-id="c253e-124">例如，如果您的網站包含動態內容，例如 Confluence 或 Unily 等內容管理系統中的網頁，您可以啟用動態編目程式。</span><span class="sxs-lookup"><span data-stu-id="c253e-124">If your website contains dynamic content, for example, webpages that live in content management systems like Confluence or Unily, you can enable a dynamic crawler.</span></span> <span data-ttu-id="c253e-125">若要將其開啟，請選取 [ **啟用動態網站的** 編目]。</span><span class="sxs-lookup"><span data-stu-id="c253e-125">To turn it on, select **Enable crawl for dynamic sites**.</span></span> <span data-ttu-id="c253e-126">編目程式會在開始編目之前，等待動態內容進行轉譯。</span><span class="sxs-lookup"><span data-stu-id="c253e-126">The crawler will wait for dynamic content to render before it begins crawling.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="c253e-127">![Enterprise 網頁連接器之連線設定窗格的螢幕擷取畫面](media/enterprise-web-connector/connectors-enterpriseweb-connectionsettings-dynamicconfig-small.png)</span><span class="sxs-lookup"><span data-stu-id="c253e-127">![Screenshot of Connection Settings pane for Enterprise Web connector](media/enterprise-web-connector/connectors-enterpriseweb-connectionsettings-dynamicconfig-small.png)</span></span>

<span data-ttu-id="c253e-128">除了核取方塊之外，還有三個可供選用的欄位：</span><span class="sxs-lookup"><span data-stu-id="c253e-128">In addition to the check box, there are three optional fields available:</span></span>

1. <span data-ttu-id="c253e-129">**Dom 就緒**：輸入 dom 專案，編目程式應使用它做為內容完全呈現及編目應該開始的信號。</span><span class="sxs-lookup"><span data-stu-id="c253e-129">**DOM Ready**: Enter the DOM element the crawler should use as the signal that the content is fully rendered and the crawl should begin.</span></span>
1. <span data-ttu-id="c253e-130">**要新增的標頭**：指定編目程式在傳送該特定 web URL 時應包含的 HTTP 標頭。</span><span class="sxs-lookup"><span data-stu-id="c253e-130">**Headers to Add**: Specify which HTTP headers the crawler should include when sending that specific web URL.</span></span> <span data-ttu-id="c253e-131">您可以為不同的網站設定多個標頭。</span><span class="sxs-lookup"><span data-stu-id="c253e-131">You can set multiple headers for different websites.</span></span> <span data-ttu-id="c253e-132">建議包括 auth token 值。</span><span class="sxs-lookup"><span data-stu-id="c253e-132">We suggest including auth token values.</span></span>
1. <span data-ttu-id="c253e-133">**略過標頭**：指定應從動態編目要求排除的任何不必要標頭。</span><span class="sxs-lookup"><span data-stu-id="c253e-133">**Headers to Skip**: Specify any unnecessary headers that should be excluded from dynamic crawling requests.</span></span>

> [!NOTE]
> <span data-ttu-id="c253e-134">只有代理程式編目模式支援動態編目。</span><span class="sxs-lookup"><span data-stu-id="c253e-134">Dynamic crawling is only supported for Agent crawl mode.</span></span>

### <a name="crawl-mode-cloud-or-on-premises"></a><span data-ttu-id="c253e-135">編目模式：雲端或內部部署</span><span class="sxs-lookup"><span data-stu-id="c253e-135">Crawl mode: Cloud or On-premises</span></span>

<span data-ttu-id="c253e-136">編目模式會決定您要建立索引的網站類型（雲端或內部部署）。</span><span class="sxs-lookup"><span data-stu-id="c253e-136">The crawl mode determines the type of websites you want to index, either cloud or on-premises.</span></span> <span data-ttu-id="c253e-137">針對您的雲端網站，選取 **雲端** 做為編目模式。</span><span class="sxs-lookup"><span data-stu-id="c253e-137">For your cloud websites, select **Cloud** as the crawl mode.</span></span>

<span data-ttu-id="c253e-138">此外，連接器現在也支援對內部部署網站進行編目。</span><span class="sxs-lookup"><span data-stu-id="c253e-138">Also, the connector now supports crawling of on-premises websites.</span></span> <span data-ttu-id="c253e-139">若要存取您的內部部署資料，您必須先安裝及設定 Graph 連接器代理程式。</span><span class="sxs-lookup"><span data-stu-id="c253e-139">To access your on-premises data, you must first install and configure the Graph connector agent.</span></span> <span data-ttu-id="c253e-140">若要深入瞭解，請參閱[Graph connector agent](./on-prem-agent.md)。</span><span class="sxs-lookup"><span data-stu-id="c253e-140">To learn more, see [Graph connector agent](./on-prem-agent.md).</span></span>

<span data-ttu-id="c253e-141">若為您的內部部署網站，請選取 [**代理程式**] 做為編目模式，並在 [部署中的 **代理程式**] 欄位中，選擇您先前安裝及設定的 Graph 連接器代理程式。</span><span class="sxs-lookup"><span data-stu-id="c253e-141">For your on-premises websites, select **Agent** as the crawl mode and in the **On-prem Agent** field, choose the Graph connector agent that you installed and configured earlier.</span></span>  

### <a name="authentication"></a><span data-ttu-id="c253e-142">驗證</span><span class="sxs-lookup"><span data-stu-id="c253e-142">Authentication</span></span>

<span data-ttu-id="c253e-143">基本驗證需要使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="c253e-143">Basic Authentication requires a username and password.</span></span> <span data-ttu-id="c253e-144">使用[Microsoft 365 系統管理中心](https://admin.microsoft.com)建立此 bot 帳戶。</span><span class="sxs-lookup"><span data-stu-id="c253e-144">Create this bot account by using the [Microsoft 365 admin center](https://admin.microsoft.com).</span></span>

<span data-ttu-id="c253e-145">使用 [AZURE AD](/azure/active-directory/) OAuth 2.0 需要資源識別碼、用戶端識別碼和用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="c253e-145">OAuth 2.0 with [Azure AD](/azure/active-directory/) requires a resource ID, Client ID, and Client Secret.</span></span> <span data-ttu-id="c253e-146">OAuth 2.0 僅適用于雲端模式。</span><span class="sxs-lookup"><span data-stu-id="c253e-146">OAuth 2.0 only works with Cloud mode.</span></span>

<span data-ttu-id="c253e-147">如需詳細資訊，請參閱[使用 OAuth 2.0 代碼授與流程授權存取 Azure Active Directory web 應用程式](/azure/active-directory/develop/v1-protocols-oauth-code)。</span><span class="sxs-lookup"><span data-stu-id="c253e-147">For more information, see [Authorize access to Azure Active Directory web applications using OAuth 2.0 code grant flow](/azure/active-directory/develop/v1-protocols-oauth-code).</span></span> <span data-ttu-id="c253e-148">使用下列值進行註冊：</span><span class="sxs-lookup"><span data-stu-id="c253e-148">Register with the following values:</span></span>

<span data-ttu-id="c253e-149">**名稱：** Microsoft 搜尋</span><span class="sxs-lookup"><span data-stu-id="c253e-149">**Name:** Microsoft Search</span></span> <br/>
<span data-ttu-id="c253e-150">**Redirect_URI：**`https://gcs.office.com/v1.0/admin/oauth/callback`</span><span class="sxs-lookup"><span data-stu-id="c253e-150">**Redirect_URI:** `https://gcs.office.com/v1.0/admin/oauth/callback`</span></span>

<span data-ttu-id="c253e-151">若要取得資源、client_id 及 client_secret 的值，請移至 **使用授權碼以要求** 重新導向 URL 網頁上的存取權杖。</span><span class="sxs-lookup"><span data-stu-id="c253e-151">To get the values for the resource, client_id, and client_secret, go to **Use the authorization code to request an access token** on the redirect URL webpage.</span></span>

<span data-ttu-id="c253e-152">如需詳細資訊，請參閱[快速入門：使用 Microsoft 身分識別平臺註冊應用程式](/azure/active-directory/develop/quickstart-register-app)。</span><span class="sxs-lookup"><span data-stu-id="c253e-152">For even more information, see [Quickstart: Register an application with the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app).</span></span>

## <a name="step-3a-add-urls-to-exclude-optional-crawl-restrictions"></a><span data-ttu-id="c253e-153">步驟3a：新增 URLs 以排除 (選擇性編目限制) </span><span class="sxs-lookup"><span data-stu-id="c253e-153">Step 3a: Add URLs to exclude (Optional crawl restrictions)</span></span>

<span data-ttu-id="c253e-154">有兩種方式可以避免網頁進行編目：在 robots.txt 檔案中禁止這些頁面，或將其新增至排除清單。</span><span class="sxs-lookup"><span data-stu-id="c253e-154">There are two ways to prevent pages from being crawled: disallow them in your robots.txt file or add them to the Exclusion list.</span></span>

### <a name="support-for-robotstxt"></a><span data-ttu-id="c253e-155">robots.txt 的支援</span><span class="sxs-lookup"><span data-stu-id="c253e-155">Support for robots.txt</span></span>

<span data-ttu-id="c253e-156">連接器會檢查您的根網站是否有 robots.txt 檔案，如果有的話，則會依照該檔案中所發現的指示來查看。</span><span class="sxs-lookup"><span data-stu-id="c253e-156">The connector checks to see if there is a robots.txt file for your root site and, if one exists, it will follow and respect the directions found within that file.</span></span> <span data-ttu-id="c253e-157">如果您不想讓連接器編目網站上的某些頁面或目錄，您可以在 robots.txt 檔案中的「禁止」宣告中呼叫這些頁面或目錄。</span><span class="sxs-lookup"><span data-stu-id="c253e-157">If you do not want the connector to crawl certain pages or directories on your site, you can call out those pages or directories in the "Disallow" declarations in your robots.txt file.</span></span>

### <a name="add-urls-to-exclude"></a><span data-ttu-id="c253e-158">新增要排除的 URLs</span><span class="sxs-lookup"><span data-stu-id="c253e-158">Add URLs to exclude</span></span>

<span data-ttu-id="c253e-159">您可以選擇性地建立 **排除清單** ，以排除部分 URLs 若該內容機密或不值得編目的情況，則無法取得編目。</span><span class="sxs-lookup"><span data-stu-id="c253e-159">You can optionally create an **Exclusion list** to exclude some URLs from getting crawled if that content is sensitive or not worth crawling.</span></span> <span data-ttu-id="c253e-160">若要建立排除清單，請流覽根 URL。</span><span class="sxs-lookup"><span data-stu-id="c253e-160">To create an exclusion list, browse through the root URL.</span></span> <span data-ttu-id="c253e-161">您可以在設定過程中將排除的 URLs 新增至清單。</span><span class="sxs-lookup"><span data-stu-id="c253e-161">You can add the excluded URLs to the list during the configuration process.</span></span>

## <a name="step-4-assign-property-labels"></a><span data-ttu-id="c253e-162">步驟4：指派屬性標籤</span><span class="sxs-lookup"><span data-stu-id="c253e-162">Step 4: Assign property labels</span></span>

<span data-ttu-id="c253e-163">您可以從選項的功能表中選擇，將 source 屬性指派給每個標籤。</span><span class="sxs-lookup"><span data-stu-id="c253e-163">You can assign a source property to each label by choosing from a menu of options.</span></span> <span data-ttu-id="c253e-164">雖然這個步驟不是必要的，但具有一些屬性標籤會提升搜尋相關性，並確保使用者可以更精確的搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="c253e-164">While this step isn't mandatory, having some property labels will improve the search relevance and ensure more accurate search results for end users.</span></span>

## <a name="step-5-manage-schema"></a><span data-ttu-id="c253e-165">步驟5：管理架構</span><span class="sxs-lookup"><span data-stu-id="c253e-165">Step 5: Manage schema</span></span>

<span data-ttu-id="c253e-166">在 [ **管理架構** ] 畫面上，您可以變更架構屬性 (選項包括「 **查詢**」、「 **搜尋**」、「 **檢索**」及「 **精煉** 」與屬性相關聯的) 、新增選用的別名，然後選擇 **Content** 屬性。</span><span class="sxs-lookup"><span data-stu-id="c253e-166">On the **Manage Schema** screen, you can change the schema attributes (the options are **Query**, **Search**, **Retrieve**, and **Refine**) associated with the properties, add optional aliases, and choose the **Content** property.</span></span>

## <a name="step-6-manage-search-permissions"></a><span data-ttu-id="c253e-167">步驟6：管理搜尋許可權</span><span class="sxs-lookup"><span data-stu-id="c253e-167">Step 6: Manage search permissions</span></span>

<span data-ttu-id="c253e-168">Enterprise 網站連接器只支援 **所有人都** 能看見的搜尋許可權。</span><span class="sxs-lookup"><span data-stu-id="c253e-168">The Enterprise websites connector only supports search permissions visible to **Everyone**.</span></span> <span data-ttu-id="c253e-169">已編制索引的資料會顯示在搜尋結果中，並對組織中的所有使用者顯示。</span><span class="sxs-lookup"><span data-stu-id="c253e-169">Indexed data appears in the search results and is visible to all users in the organization.</span></span>

## <a name="step-7-set-the-refresh-schedule"></a><span data-ttu-id="c253e-170">步驟7：設定重新整理排程</span><span class="sxs-lookup"><span data-stu-id="c253e-170">Step 7: Set the refresh schedule</span></span>

<span data-ttu-id="c253e-171">Enterprise 網站連接器只支援完整重新整理。</span><span class="sxs-lookup"><span data-stu-id="c253e-171">The Enterprise websites connector only supports a full refresh.</span></span> <span data-ttu-id="c253e-172">這表示連接器會在每次重新整理時重新編目網站的所有內容。</span><span class="sxs-lookup"><span data-stu-id="c253e-172">This means that the connector will recrawl all the website's content during every refresh.</span></span> <span data-ttu-id="c253e-173">若要確定連接器有足夠的時間來編目內容，建議您設定大型重新整理排程間隔。</span><span class="sxs-lookup"><span data-stu-id="c253e-173">To make sure the connector gets enough time to crawl the content, we recommend that you set a large refresh schedule interval.</span></span> <span data-ttu-id="c253e-174">建議您在一到兩周之間進行排程重新整理。</span><span class="sxs-lookup"><span data-stu-id="c253e-174">We recommend a scheduled refresh between one and two weeks.</span></span>

## <a name="step-8-review-connection"></a><span data-ttu-id="c253e-175">步驟8：檢查連線</span><span class="sxs-lookup"><span data-stu-id="c253e-175">Step 8: Review connection</span></span>

<span data-ttu-id="c253e-176">遵循一般 [設定指示](./configure-connector.md)。</span><span class="sxs-lookup"><span data-stu-id="c253e-176">Follow the general [setup instructions](./configure-connector.md).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="troubleshooting"></a><span data-ttu-id="c253e-177">疑難排解</span><span class="sxs-lookup"><span data-stu-id="c253e-177">Troubleshooting</span></span>

<span data-ttu-id="c253e-178">當閱讀網站內容時，編目可能會遇到一些來源錯誤，這些錯誤是由下列詳細的錯誤碼所代表。</span><span class="sxs-lookup"><span data-stu-id="c253e-178">When reading the website's content, the crawl may encounter some source errors, which are represented by the detailed error codes below.</span></span> <span data-ttu-id="c253e-179">若要取得錯誤類型的詳細資訊，請在選取連接後，移至 [ **錯誤詳細資料** ] 頁面。</span><span class="sxs-lookup"><span data-stu-id="c253e-179">To get more information on the types of errors, go to the **error details** page after selecting the connection.</span></span> <span data-ttu-id="c253e-180">選取 **錯誤碼** 以查看更詳細的錯誤。</span><span class="sxs-lookup"><span data-stu-id="c253e-180">Select the **error code** to see more detailed errors.</span></span> <span data-ttu-id="c253e-181">此外，請參閱 [管理您的連接器](./manage-connector.md) 以深入瞭解。</span><span class="sxs-lookup"><span data-stu-id="c253e-181">Also refer to [Manage your connector](./manage-connector.md) to learn more.</span></span>

 <span data-ttu-id="c253e-182">詳細錯誤代碼</span><span class="sxs-lookup"><span data-stu-id="c253e-182">Detailed Error code</span></span> | <span data-ttu-id="c253e-183">錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="c253e-183">Error message</span></span>
 --- | ---
 <span data-ttu-id="c253e-184">6001</span><span class="sxs-lookup"><span data-stu-id="c253e-184">6001</span></span> | <span data-ttu-id="c253e-185">無法連線正在嘗試編制索引的網站</span><span class="sxs-lookup"><span data-stu-id="c253e-185">The site that is being tried to index is not reachable</span></span>
 <span data-ttu-id="c253e-186">6005</span><span class="sxs-lookup"><span data-stu-id="c253e-186">6005</span></span> | <span data-ttu-id="c253e-187">根據 robots.txt 設定，已封鎖嘗試編制索引的來源頁面。</span><span class="sxs-lookup"><span data-stu-id="c253e-187">The source page that is being tried to index has been blocked by as per robots.txt configuration.</span></span>
 <span data-ttu-id="c253e-188">6008</span><span class="sxs-lookup"><span data-stu-id="c253e-188">6008</span></span> | <span data-ttu-id="c253e-189">無法解析 DNS</span><span class="sxs-lookup"><span data-stu-id="c253e-189">Unable to resolve the DNS</span></span>
 <span data-ttu-id="c253e-190">6009</span><span class="sxs-lookup"><span data-stu-id="c253e-190">6009</span></span> | <span data-ttu-id="c253e-191">針對所有用戶端錯誤 (除 HTTP 404、408) 以外，請參閱 HTTP 4xx 錯誤碼以取得詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="c253e-191">For all client-side errors (Except HTTP 404, 408), refer to HTTP 4xx error codes for details.</span></span>
 <span data-ttu-id="c253e-192">6013</span><span class="sxs-lookup"><span data-stu-id="c253e-192">6013</span></span> | <span data-ttu-id="c253e-193">找不到嘗試編制索引的來源頁面。</span><span class="sxs-lookup"><span data-stu-id="c253e-193">The source page that is being tried to index could not be found.</span></span> <span data-ttu-id="c253e-194"> (HTTP 404 錯誤) </span><span class="sxs-lookup"><span data-stu-id="c253e-194">(HTTP 404 error)</span></span>
 <span data-ttu-id="c253e-195">6018</span><span class="sxs-lookup"><span data-stu-id="c253e-195">6018</span></span> | <span data-ttu-id="c253e-196">來源頁面沒有回應，且要求超時。 (HTTP 408 錯誤) </span><span class="sxs-lookup"><span data-stu-id="c253e-196">The source page is not responding, and the request has timed out. (HTTP 408 error)</span></span>
 <span data-ttu-id="c253e-197">6021</span><span class="sxs-lookup"><span data-stu-id="c253e-197">6021</span></span> | <span data-ttu-id="c253e-198">嘗試編制索引的來源頁面沒有頁面上的文字內容。</span><span class="sxs-lookup"><span data-stu-id="c253e-198">The source page that is being tried to index has no textual content on the page.</span></span>
 <span data-ttu-id="c253e-199">6023</span><span class="sxs-lookup"><span data-stu-id="c253e-199">6023</span></span> | <span data-ttu-id="c253e-200">嘗試編制索引的來源頁面不受支援 (不是 HTML 頁面) </span><span class="sxs-lookup"><span data-stu-id="c253e-200">The source page that is being tried to index is unsupported (not an HTML page)</span></span>
 <span data-ttu-id="c253e-201">6024</span><span class="sxs-lookup"><span data-stu-id="c253e-201">6024</span></span> | <span data-ttu-id="c253e-202">嘗試編制索引的來源頁面具有不支援的內容。</span><span class="sxs-lookup"><span data-stu-id="c253e-202">The source page that is being tried to index has unsupported content.</span></span>

* <span data-ttu-id="c253e-203">當資料來源由於網路問題或資料來源本身被刪除、移動或重新命名時，就會發生錯誤6001-6013。</span><span class="sxs-lookup"><span data-stu-id="c253e-203">Errors 6001-6013 occur when the data source is not reachable due to a network issue or when the data source itself is deleted, moved, or renamed.</span></span> <span data-ttu-id="c253e-204">檢查提供的資料來源詳細資料是否仍然有效。</span><span class="sxs-lookup"><span data-stu-id="c253e-204">Check if the data source details provided are still valid.</span></span>
* <span data-ttu-id="c253e-205">當資料來源包含頁面上的非文字內容或頁面不是 HTML 時，就會發生錯誤6021-6024。</span><span class="sxs-lookup"><span data-stu-id="c253e-205">Errors 6021-6024 occur when the data source contains non-textual content on the page or when the page is not an HTML.</span></span> <span data-ttu-id="c253e-206">請檢查資料來源，並將此頁面加入排除清單，或略過錯誤。</span><span class="sxs-lookup"><span data-stu-id="c253e-206">Check the data source and add this page in exclusion list or ignore the error.</span></span>
