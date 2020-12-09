---
title: Microsoft 搜尋的企業網站連接器
ms.author: monaray
author: monaray97
manager: mnirkhe
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 設定 Microsoft 搜尋的企業網站連接器
ms.openlocfilehash: 443e903e0fa371d2a056fd4bf06310eb2627b11c
ms.sourcegitcommit: 031e7c595496d9faed9038725b04f3c8b5f9ccbd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/09/2020
ms.locfileid: "49604769"
---
<!-- markdownlint-disable no-inline-html -->
# <a name="enterprise-websites-connector"></a><span data-ttu-id="d1960-103">企業網站連接器</span><span class="sxs-lookup"><span data-stu-id="d1960-103">Enterprise websites connector</span></span>

<span data-ttu-id="d1960-104">透過企業網站連接器，您的組織可以 **從其內部網站** 對文章和內容編制索引。</span><span class="sxs-lookup"><span data-stu-id="d1960-104">With the Enterprise websites connector, your organization can index articles and **content from its internal-facing websites**.</span></span> <span data-ttu-id="d1960-105">在您設定網站的連接器及同步內容之後，使用者可以從任何 Microsoft 搜尋用戶端搜尋該內容。</span><span class="sxs-lookup"><span data-stu-id="d1960-105">After you configure the connector and sync content from the website, end users can search for that content from any Microsoft Search client.</span></span>

<span data-ttu-id="d1960-106">本文適用于 [Microsoft 365](https://www.microsoft.com/microsoft-365) 系統管理員或任何設定、執行及監視企業網站連接器的人員。</span><span class="sxs-lookup"><span data-stu-id="d1960-106">This article is for [Microsoft 365](https://www.microsoft.com/microsoft-365) administrators or anyone who configures, runs, and monitors an Enterprise websites connector.</span></span> <span data-ttu-id="d1960-107">它說明如何設定連接器和連接器功能、限制及疑難排解技術。</span><span class="sxs-lookup"><span data-stu-id="d1960-107">It explains how to configure your connector and connector capabilities, limitations, and troubleshooting techniques.</span></span>  

## <a name="connection-settings"></a><span data-ttu-id="d1960-108">連接設定</span><span class="sxs-lookup"><span data-stu-id="d1960-108">Connection settings</span></span>

<span data-ttu-id="d1960-109">若要連線至您的資料來源，您必須填寫網站的根 URL、選擇編目來源，以及您想要使用的驗證類型： [無]、[基本驗證]，或 OAuth 2.0 搭配 [Azure Active Directory (AZURE AD) ](https://docs.microsoft.com/azure/active-directory/)。</span><span class="sxs-lookup"><span data-stu-id="d1960-109">To connect to your data source, you need to fill in the root URL of the website, select a crawl source, and the type of authentication you'd like to use: None, Basic Authentication, or OAuth 2.0 with [Azure Active Directory (Azure AD)](https://docs.microsoft.com/azure/active-directory/).</span></span> <span data-ttu-id="d1960-110">在您完成此資訊之後，請按一下 [測試連線] 以驗證您的設定。</span><span class="sxs-lookup"><span data-stu-id="d1960-110">After you complete this information, click Test Connection to verify your settings.</span></span>

### <a name="url"></a><span data-ttu-id="d1960-111">URL</span><span class="sxs-lookup"><span data-stu-id="d1960-111">URL</span></span>

<span data-ttu-id="d1960-112">使用 [URL] 欄位可指定您要編目之網站的根目錄。</span><span class="sxs-lookup"><span data-stu-id="d1960-112">Use the URL field to specify the root of the website that you'd like to crawl.</span></span> <span data-ttu-id="d1960-113">企業網站連接器會使用此 URL 做為開始點，並遵循此 URL 的所有連結進行編目。</span><span class="sxs-lookup"><span data-stu-id="d1960-113">The enterprise websites connector will use this URL as the starting point and follow all the links from this URL for its crawl.</span></span>

### <a name="crawl-mode-cloud-or-on-premises-preview"></a><span data-ttu-id="d1960-114">編目模式：雲端或內部部署 (預覽) </span><span class="sxs-lookup"><span data-stu-id="d1960-114">Crawl mode: Cloud or On-premises (Preview)</span></span>

<span data-ttu-id="d1960-115">編目模式會決定您要建立索引的網站類型（雲端或內部部署）。</span><span class="sxs-lookup"><span data-stu-id="d1960-115">The crawl mode determines the type of websites you want to index, either cloud or on-premises.</span></span> <span data-ttu-id="d1960-116">針對您的雲端網站，選取 **雲端** 做為編目模式。</span><span class="sxs-lookup"><span data-stu-id="d1960-116">For your cloud websites, select **Cloud** as the crawl mode.</span></span>

<span data-ttu-id="d1960-117">此外，連接器現在也支援對內部部署網站進行編目。</span><span class="sxs-lookup"><span data-stu-id="d1960-117">Also, the connector now supports crawling of on-premises websites.</span></span> <span data-ttu-id="d1960-118">此模式為預覽模式。</span><span class="sxs-lookup"><span data-stu-id="d1960-118">This mode is in preview.</span></span> <span data-ttu-id="d1960-119">若要存取您的內部部署資料，您必須先安裝及設定圖形連接器代理程式。</span><span class="sxs-lookup"><span data-stu-id="d1960-119">To access your on-premises data, you must first install and configure the Graph connector agent.</span></span> <span data-ttu-id="d1960-120">若要深入瞭解，請參閱 [Graph connector agent](https://docs.microsoft.com/microsoftsearch/on-prem-agent)。</span><span class="sxs-lookup"><span data-stu-id="d1960-120">To learn more, see [Graph connector agent](https://docs.microsoft.com/microsoftsearch/on-prem-agent).</span></span>

<span data-ttu-id="d1960-121">若為您的內部部署網站，請選取 [ **代理程式** ] 做為編目模式，並在 [部署中的 **代理程式** ] 欄位中，選擇您先前安裝及設定的圖形連接器代理程式。</span><span class="sxs-lookup"><span data-stu-id="d1960-121">For your on-premises websites, select **Agent** as the crawl mode and in the **On-Prem Agent** field, choose the Graph connector agent that you installed and configured earlier.</span></span>  

![商業網路連接器之連線設定窗格的螢幕擷取畫面](media/enterprise-web-connector/connectors-enterpriseweb-settings.png)

### <a name="authentication"></a><span data-ttu-id="d1960-123">驗證</span><span class="sxs-lookup"><span data-stu-id="d1960-123">Authentication</span></span>

<span data-ttu-id="d1960-124">基本驗證需要使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="d1960-124">Basic Authentication requires a username and password.</span></span> <span data-ttu-id="d1960-125">使用 [Microsoft 365 系統管理中心](https://admin.microsoft.com)建立此 bot 帳戶。</span><span class="sxs-lookup"><span data-stu-id="d1960-125">Create this bot account by using the [Microsoft 365 admin center](https://admin.microsoft.com).</span></span>

<span data-ttu-id="d1960-126">使用 [AZURE AD](https://docs.microsoft.com/azure/active-directory/) OAuth 2.0 需要資源識別碼、用戶端識別碼和用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="d1960-126">OAuth 2.0 with [Azure AD](https://docs.microsoft.com/azure/active-directory/) requires a resource ID, Client ID, and Client Secret.</span></span> <span data-ttu-id="d1960-127">OAuth 2.0 僅適用于雲端模式。</span><span class="sxs-lookup"><span data-stu-id="d1960-127">OAuth 2.0 only works with Cloud mode.</span></span>

<span data-ttu-id="d1960-128">如需詳細資訊，請參閱 [使用 OAuth 2.0 程式碼授與流程授權存取 Azure Active Directory web 應用程式](https://docs.microsoft.com/azure/active-directory/develop/v1-protocols-oauth-code)。</span><span class="sxs-lookup"><span data-stu-id="d1960-128">For more information, see [Authorize access to Azure Active Directory web applications using OAuth 2.0 code grant flow](https://docs.microsoft.com/azure/active-directory/develop/v1-protocols-oauth-code).</span></span> <span data-ttu-id="d1960-129">使用下列值進行註冊：</span><span class="sxs-lookup"><span data-stu-id="d1960-129">Register with the following values:</span></span>

<span data-ttu-id="d1960-130">**名稱：** Microsoft 搜尋</span><span class="sxs-lookup"><span data-stu-id="d1960-130">**Name:** Microsoft Search</span></span> <br/>
<span data-ttu-id="d1960-131">**Redirect_URI：**`https://gcs.office.com/v1.0/admin/oauth/callback`</span><span class="sxs-lookup"><span data-stu-id="d1960-131">**Redirect_URI:** `https://gcs.office.com/v1.0/admin/oauth/callback`</span></span>

<span data-ttu-id="d1960-132">若要取得資源、client_id 及 client_secret 的值，請移至 **使用授權碼以要求** 重新導向 URL 網頁上的存取權杖。</span><span class="sxs-lookup"><span data-stu-id="d1960-132">To get the values for the resource, client_id, and client_secret, go to **Use the authorization code to request an access token** on the redirect URL webpage.</span></span>

<span data-ttu-id="d1960-133">如需詳細資訊，請參閱 [快速入門：使用 Microsoft identity Platform 註冊應用程式](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app)。</span><span class="sxs-lookup"><span data-stu-id="d1960-133">For even more information, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

## <a name="support-for-robotstxt"></a><span data-ttu-id="d1960-134">robots.txt 的支援</span><span class="sxs-lookup"><span data-stu-id="d1960-134">Support for robots.txt</span></span>

<span data-ttu-id="d1960-135">連接器會檢查您的根網站是否有 robots.txt 檔案，如果有的話，則會依照該檔案中所發現的指示來查看。</span><span class="sxs-lookup"><span data-stu-id="d1960-135">The connector checks to see if there is a robots.txt file for your root site and, if one exists, it will follow and respect the directions found within that file.</span></span> <span data-ttu-id="d1960-136">如果您不想讓連接器編目網站上的某些頁面或目錄，您可以在 robots.txt 檔案中的「禁止」宣告中呼叫這些頁面或目錄。</span><span class="sxs-lookup"><span data-stu-id="d1960-136">If you do not want the connector to crawl certain pages or directories on your site, you can call out those pages or directories in the "Disallow" declarations in your robots.txt file.</span></span>

## <a name="add-urls-to-exclude"></a><span data-ttu-id="d1960-137">新增要排除的 URLs</span><span class="sxs-lookup"><span data-stu-id="d1960-137">Add URLs to exclude</span></span>

<span data-ttu-id="d1960-138">您可以選擇性地建立 **排除清單** ，以排除部分 URLs 若該內容機密或不值得編目的情況，則無法取得編目。</span><span class="sxs-lookup"><span data-stu-id="d1960-138">You can optionally create an **Exclusion list** to exclude some URLs from getting crawled if that content is sensitive or not worth crawling.</span></span> <span data-ttu-id="d1960-139">若要建立排除清單，請流覽根 URL。</span><span class="sxs-lookup"><span data-stu-id="d1960-139">To create an exclusion list, browse through the root URL.</span></span> <span data-ttu-id="d1960-140">您可以選擇在設定過程中將排除的 URLs 新增至清單。</span><span class="sxs-lookup"><span data-stu-id="d1960-140">You have the option to add the excluded URLs to the list during the configuration process.</span></span>

## <a name="manage-search-permissions"></a><span data-ttu-id="d1960-141">管理搜尋許可權</span><span class="sxs-lookup"><span data-stu-id="d1960-141">Manage search permissions</span></span>

<span data-ttu-id="d1960-142">企業網站連接器只支援 **所有人都** 能看見的搜尋許可權。</span><span class="sxs-lookup"><span data-stu-id="d1960-142">The Enterprise websites connector only supports search permissions visible to **Everyone**.</span></span> <span data-ttu-id="d1960-143">已編制索引的資料會顯示在搜尋結果中，並對組織中的所有使用者顯示。</span><span class="sxs-lookup"><span data-stu-id="d1960-143">Indexed data appears in the search results and is visible to all users in the organization.</span></span>

## <a name="assign-property-labels"></a><span data-ttu-id="d1960-144">指派屬性標籤</span><span class="sxs-lookup"><span data-stu-id="d1960-144">Assign property labels</span></span>

<span data-ttu-id="d1960-145">您可以從選項的功能表中選擇，將 source 屬性指派給每個標籤。</span><span class="sxs-lookup"><span data-stu-id="d1960-145">You can assign a source property to each label by choosing from a menu of options.</span></span> <span data-ttu-id="d1960-146">雖然這個步驟不是必要的，但具有一些屬性標籤會提升搜尋相關性，並可確保使用者更準確的搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="d1960-146">While this step is not mandatory, having some property labels will improve the search relevance and ensure more accurate search results for end users.</span></span>

## <a name="manage-schema"></a><span data-ttu-id="d1960-147">管理架構</span><span class="sxs-lookup"><span data-stu-id="d1960-147">Manage schema</span></span>

<span data-ttu-id="d1960-148">在 [**管理架構**] 畫面上，您可以選擇變更架構屬性 (可 **查詢**、**可搜尋、可\*\*\*\*檢索** 及 **可精簡搜尋**) 相關聯的屬性、新增選用的別名，然後選擇 **Content** 屬性。</span><span class="sxs-lookup"><span data-stu-id="d1960-148">On the **Manage Schema** screen, you have the option to change the schema attributes (**queryable**, **searchable**, **retrievable**, and **refinable**) associated with the properties, add optional aliases, and choose the **Content** property.</span></span>

## <a name="set-the-refresh-schedule"></a><span data-ttu-id="d1960-149">設定重新整理排程</span><span class="sxs-lookup"><span data-stu-id="d1960-149">Set the refresh schedule</span></span>

<span data-ttu-id="d1960-150">企業網站連接器只支援完整重新整理。</span><span class="sxs-lookup"><span data-stu-id="d1960-150">The Enterprise websites connector only supports a full refresh.</span></span> <span data-ttu-id="d1960-151">這表示連接器會在每次重新整理時重新編目網站的所有內容。</span><span class="sxs-lookup"><span data-stu-id="d1960-151">This means that the connector will recrawl all the website's content during every refresh.</span></span> <span data-ttu-id="d1960-152">若要確定連接器有足夠的時間來編目內容，建議您設定大型重新整理排程間隔。</span><span class="sxs-lookup"><span data-stu-id="d1960-152">To make sure the connector gets enough time to crawl the content, we recommend that you set a large refresh schedule interval.</span></span> <span data-ttu-id="d1960-153">建議您在一到兩周之間進行排程重新整理。</span><span class="sxs-lookup"><span data-stu-id="d1960-153">We recommend a scheduled refresh between one and two weeks.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="d1960-154">疑難排解</span><span class="sxs-lookup"><span data-stu-id="d1960-154">Troubleshooting</span></span>

<span data-ttu-id="d1960-155">當閱讀網站內容時，編目可能會遇到一些來源錯誤，這些錯誤是由下列詳細的錯誤碼所代表。</span><span class="sxs-lookup"><span data-stu-id="d1960-155">When reading the website's content, the crawl may encounter some source errors, which are represented by the detailed error codes below.</span></span> <span data-ttu-id="d1960-156">若要取得錯誤類型的詳細資訊，請在選取連接後，移至 [ **錯誤詳細資料** ] 頁面。</span><span class="sxs-lookup"><span data-stu-id="d1960-156">To get more information on the types of errors, go to the **error details** page after selecting the connection.</span></span> <span data-ttu-id="d1960-157">按一下 **錯誤碼** 以查看更詳細的錯誤。</span><span class="sxs-lookup"><span data-stu-id="d1960-157">Click on the **error code** to see more detailed errors.</span></span> <span data-ttu-id="d1960-158">此外，請參閱 [管理您的連接器](https://docs.microsoft.com/microsoftsearch/manage-connector) 以深入瞭解。</span><span class="sxs-lookup"><span data-stu-id="d1960-158">Also refer to [Manage your connector](https://docs.microsoft.com/microsoftsearch/manage-connector) to learn more.</span></span>

 <span data-ttu-id="d1960-159">詳細錯誤代碼</span><span class="sxs-lookup"><span data-stu-id="d1960-159">Detailed Error code</span></span> | <span data-ttu-id="d1960-160">錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="d1960-160">Error message</span></span>
 --- | ---
 <span data-ttu-id="d1960-161">6001</span><span class="sxs-lookup"><span data-stu-id="d1960-161">6001</span></span> | <span data-ttu-id="d1960-162">無法連線正在嘗試編制索引的網站</span><span class="sxs-lookup"><span data-stu-id="d1960-162">The site that is being tried to index is not reachable</span></span>
 <span data-ttu-id="d1960-163">6005</span><span class="sxs-lookup"><span data-stu-id="d1960-163">6005</span></span> | <span data-ttu-id="d1960-164">根據 robots.txt 設定，已封鎖嘗試編制索引的來源頁面。</span><span class="sxs-lookup"><span data-stu-id="d1960-164">The source page that is being tried to index has been blocked by as per robots.txt configuration.</span></span>
 <span data-ttu-id="d1960-165">6008</span><span class="sxs-lookup"><span data-stu-id="d1960-165">6008</span></span> | <span data-ttu-id="d1960-166">無法解析 DNS</span><span class="sxs-lookup"><span data-stu-id="d1960-166">Unable to resolve the DNS</span></span>
 <span data-ttu-id="d1960-167">6009</span><span class="sxs-lookup"><span data-stu-id="d1960-167">6009</span></span> | <span data-ttu-id="d1960-168">針對所有用戶端錯誤 (除 HTTP 404、408) 以外，請參閱 HTTP 4xx 錯誤碼以取得詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="d1960-168">For all client-side errors (Except HTTP 404, 408), refer to HTTP 4xx error codes for details.</span></span>
 <span data-ttu-id="d1960-169">6013</span><span class="sxs-lookup"><span data-stu-id="d1960-169">6013</span></span> | <span data-ttu-id="d1960-170">找不到嘗試編制索引的來源頁面。</span><span class="sxs-lookup"><span data-stu-id="d1960-170">The source page that is being tried to index could not be found.</span></span> <span data-ttu-id="d1960-171"> (HTTP 404 錯誤) </span><span class="sxs-lookup"><span data-stu-id="d1960-171">(HTTP 404 error)</span></span>
 <span data-ttu-id="d1960-172">6018</span><span class="sxs-lookup"><span data-stu-id="d1960-172">6018</span></span> | <span data-ttu-id="d1960-173">來源頁面沒有回應，且要求超時。 (HTTP 408 錯誤) </span><span class="sxs-lookup"><span data-stu-id="d1960-173">The source page is not responding, and the request has timed out. (HTTP 408 error)</span></span>
 <span data-ttu-id="d1960-174">6021</span><span class="sxs-lookup"><span data-stu-id="d1960-174">6021</span></span> | <span data-ttu-id="d1960-175">嘗試編制索引的來源頁面沒有頁面上的文字內容。</span><span class="sxs-lookup"><span data-stu-id="d1960-175">The source page that is being tried to index has no textual content on the page.</span></span>
 <span data-ttu-id="d1960-176">6023</span><span class="sxs-lookup"><span data-stu-id="d1960-176">6023</span></span> | <span data-ttu-id="d1960-177">嘗試編制索引的來源頁面不受支援 (不是 HTML 頁面) </span><span class="sxs-lookup"><span data-stu-id="d1960-177">The source page that is being tried to index is unsupported (not an HTML page)</span></span>
 <span data-ttu-id="d1960-178">6024</span><span class="sxs-lookup"><span data-stu-id="d1960-178">6024</span></span> | <span data-ttu-id="d1960-179">嘗試編制索引的來源頁面具有不支援的內容。</span><span class="sxs-lookup"><span data-stu-id="d1960-179">The source page that is being tried to index has unsupported content.</span></span>

* <span data-ttu-id="d1960-180">當資料來源由於網路問題或資料來源本身被刪除、移動或重新命名時，就會發生錯誤6001-6013。</span><span class="sxs-lookup"><span data-stu-id="d1960-180">Errors 6001-6013 occur when the data source is not reachable due to a network issue or when the data source itself is deleted, moved, or renamed.</span></span> <span data-ttu-id="d1960-181">檢查提供的資料來源詳細資料是否仍然有效。</span><span class="sxs-lookup"><span data-stu-id="d1960-181">Check if the data source details provided are still valid.</span></span>
* <span data-ttu-id="d1960-182">當資料來源包含頁面上的非文字內容或頁面不是 HTML 時，就會發生錯誤6021-6024。</span><span class="sxs-lookup"><span data-stu-id="d1960-182">Errors 6021-6024 occur when the data source contains non-textual content on the page or when the page is not an HTML.</span></span> <span data-ttu-id="d1960-183">請檢查資料來源，並將此頁面加入排除清單，或略過錯誤。</span><span class="sxs-lookup"><span data-stu-id="d1960-183">Check the data source and add this page in exclusion list or ignore the error.</span></span>

## <a name="limitations"></a><span data-ttu-id="d1960-184">限制</span><span class="sxs-lookup"><span data-stu-id="d1960-184">Limitations</span></span>

<span data-ttu-id="d1960-185">企業網站連接器不支援搜尋 **動態網頁** 上的資料。</span><span class="sxs-lookup"><span data-stu-id="d1960-185">The Enterprise websites connector doesn't support searching data on **dynamic webpages**.</span></span> <span data-ttu-id="d1960-186">[Confluence](https://www.atlassian.com/software/confluence)與[Unily](https://www.unily.com/)等內容管理系統中的這些網頁範例，或儲存網站內容的資料庫。</span><span class="sxs-lookup"><span data-stu-id="d1960-186">Examples of those webpages live in content management systems like [Confluence](https://www.atlassian.com/software/confluence) and [Unily](https://www.unily.com/) or databases that store website content.</span></span>

## <a name="next-steps"></a><span data-ttu-id="d1960-187">後續步驟</span><span class="sxs-lookup"><span data-stu-id="d1960-187">Next steps</span></span>

<span data-ttu-id="d1960-188">在發佈連線後，您必須自訂搜尋結果頁面。</span><span class="sxs-lookup"><span data-stu-id="d1960-188">After publishing the connection, you need to customize the search results page.</span></span> <span data-ttu-id="d1960-189">若要瞭解如何自訂搜尋結果，請參閱 [自訂搜尋結果頁面](https://docs.microsoft.com/microsoftsearch/configure-connector#next-steps-customize-the-search-results-page)。</span><span class="sxs-lookup"><span data-stu-id="d1960-189">To learn about customizing search results, see [Customize the search results page](https://docs.microsoft.com/microsoftsearch/configure-connector#next-steps-customize-the-search-results-page).</span></span>
