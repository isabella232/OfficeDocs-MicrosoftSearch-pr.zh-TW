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
ms.openlocfilehash: 4b9d8a8472c81c2bc647b3cef3cdb437073d36cf
ms.sourcegitcommit: 59cdd3f0f82b7918399bf44d27d9891076090f4f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2020
ms.locfileid: "49367467"
---
<!-- markdownlint-disable no-inline-html -->
# <a name="enterprise-websites-connector"></a><span data-ttu-id="b5acd-103">企業網站連接器</span><span class="sxs-lookup"><span data-stu-id="b5acd-103">Enterprise websites connector</span></span>

<span data-ttu-id="b5acd-104">透過企業網站連接器，您的組織可以 **從其內部網站** 對文章和內容編制索引。</span><span class="sxs-lookup"><span data-stu-id="b5acd-104">With the Enterprise websites connector, your organization can index articles and **content from its internal-facing websites**.</span></span> <span data-ttu-id="b5acd-105">在您設定網站的連接器及同步內容之後，使用者可以從任何 Microsoft 搜尋用戶端搜尋該內容。</span><span class="sxs-lookup"><span data-stu-id="b5acd-105">After you configure the connector and sync content from the website, end users can search for that content from any Microsoft Search client.</span></span>

<span data-ttu-id="b5acd-106">本文適用于 [Microsoft 365](https://www.microsoft.com/microsoft-365) 系統管理員或任何設定、執行及監視企業網站連接器的人員。</span><span class="sxs-lookup"><span data-stu-id="b5acd-106">This article is for [Microsoft 365](https://www.microsoft.com/microsoft-365) administrators or anyone who configures, runs, and monitors an Enterprise websites connector.</span></span> <span data-ttu-id="b5acd-107">它說明如何設定連接器和連接器功能、限制及疑難排解技術。</span><span class="sxs-lookup"><span data-stu-id="b5acd-107">It explains how to configure your connector and connector capabilities, limitations, and troubleshooting techniques.</span></span>  

## <a name="connect-to-a-data-source"></a><span data-ttu-id="b5acd-108">連接到資料來源</span><span class="sxs-lookup"><span data-stu-id="b5acd-108">Connect to a data source</span></span>

<span data-ttu-id="b5acd-109">若要連線至您的資料來源，您必須填入網站的根 URL，以及您想要使用的驗證類型： [無]、[基本驗證]，或 OAuth 2.0 搭配 [Azure Active Directory (AZURE AD) ](https://docs.microsoft.com/azure/active-directory/)]。</span><span class="sxs-lookup"><span data-stu-id="b5acd-109">To connect to your data source, you need to fill in the root URL of the website and the type of authentication you'd like to use: None, Basic Authentication, or OAuth 2.0 with [Azure Active Directory (Azure AD)](https://docs.microsoft.com/azure/active-directory/).</span></span>

### <a name="url"></a><span data-ttu-id="b5acd-110">URL</span><span class="sxs-lookup"><span data-stu-id="b5acd-110">URL</span></span>

<span data-ttu-id="b5acd-111">使用 [URL] 欄位可指定您要編目之網站的根目錄。</span><span class="sxs-lookup"><span data-stu-id="b5acd-111">Use the URL field to specify the root of the website that you'd like to crawl.</span></span> <span data-ttu-id="b5acd-112">企業網站連接器會使用此 URL 做為開始點，並遵循此 URL 的所有連結進行編目。</span><span class="sxs-lookup"><span data-stu-id="b5acd-112">The enterprise websites connector will use this URL as the starting point and follow all the links from this URL for its crawl.</span></span>

### <a name="authentication"></a><span data-ttu-id="b5acd-113">驗證</span><span class="sxs-lookup"><span data-stu-id="b5acd-113">Authentication</span></span>

<span data-ttu-id="b5acd-114">基本驗證需要使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="b5acd-114">Basic Authentication requires a username and password.</span></span> <span data-ttu-id="b5acd-115">使用 [Microsoft 365 系統管理中心](https://admin.microsoft.com)建立此 bot 帳戶。</span><span class="sxs-lookup"><span data-stu-id="b5acd-115">Create this bot account by using the [Microsoft 365 admin center](https://admin.microsoft.com).</span></span>

<span data-ttu-id="b5acd-116">使用 [AZURE AD](https://docs.microsoft.com/azure/active-directory/) OAuth 2.0 需要資源識別碼、用戶端識別碼和用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="b5acd-116">OAuth 2.0 with [Azure AD](https://docs.microsoft.com/azure/active-directory/) requires a resource ID, Client ID, and Client Secret.</span></span>

<span data-ttu-id="b5acd-117">如需詳細資訊，請參閱 [使用 OAuth 2.0 程式碼授與流程授權存取 Azure Active Directory web 應用程式](https://docs.microsoft.com/azure/active-directory/develop/v1-protocols-oauth-code)。</span><span class="sxs-lookup"><span data-stu-id="b5acd-117">For more information, see [Authorize access to Azure Active Directory web applications using OAuth 2.0 code grant flow](https://docs.microsoft.com/azure/active-directory/develop/v1-protocols-oauth-code).</span></span> <span data-ttu-id="b5acd-118">使用下列值進行註冊：</span><span class="sxs-lookup"><span data-stu-id="b5acd-118">Register with the following values:</span></span>

<span data-ttu-id="b5acd-119">**名稱：** Microsoft 搜尋</span><span class="sxs-lookup"><span data-stu-id="b5acd-119">**Name:** Microsoft Search</span></span> <br/>
<span data-ttu-id="b5acd-120">**Redirect_URI：**`https://gcs.office.com/v1.0/admin/oauth/callback`</span><span class="sxs-lookup"><span data-stu-id="b5acd-120">**Redirect_URI:** `https://gcs.office.com/v1.0/admin/oauth/callback`</span></span>

<span data-ttu-id="b5acd-121">若要取得資源、client_id 及 client_secret 的值，請移至 **使用授權碼以要求** 重新導向 URL 網頁上的存取權杖。</span><span class="sxs-lookup"><span data-stu-id="b5acd-121">To get the values for the resource, client_id, and client_secret, go to **Use the authorization code to request an access token** on the redirect URL webpage.</span></span>

<span data-ttu-id="b5acd-122">如需詳細資訊，請參閱 [快速入門：使用 Microsoft identity Platform 註冊應用程式](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app)。</span><span class="sxs-lookup"><span data-stu-id="b5acd-122">For even more information, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

## <a name="add-urls-to-exclude"></a><span data-ttu-id="b5acd-123">新增要排除的 URLs</span><span class="sxs-lookup"><span data-stu-id="b5acd-123">Add URLs to exclude</span></span>

<span data-ttu-id="b5acd-124">您可以選擇性地建立 **排除清單** ，以排除部分 URLs 若該內容機密或不值得編目的情況，則無法取得編目。</span><span class="sxs-lookup"><span data-stu-id="b5acd-124">You can optionally create an **Exclusion list** to exclude some URLs from getting crawled if that content is sensitive or not worth crawling.</span></span> <span data-ttu-id="b5acd-125">若要建立排除清單，請流覽根 URL。</span><span class="sxs-lookup"><span data-stu-id="b5acd-125">To create an exclusion list, browse through the root URL.</span></span> <span data-ttu-id="b5acd-126">您可以選擇在設定過程中將排除的 URLs 新增至清單。</span><span class="sxs-lookup"><span data-stu-id="b5acd-126">You have the option to add the excluded URLs to the list during the configuration process.</span></span>

## <a name="manage-search-permissions"></a><span data-ttu-id="b5acd-127">管理搜尋許可權</span><span class="sxs-lookup"><span data-stu-id="b5acd-127">Manage search permissions</span></span>

<span data-ttu-id="b5acd-128">企業網站連接器只支援 **所有人都** 能看見的搜尋許可權。</span><span class="sxs-lookup"><span data-stu-id="b5acd-128">The Enterprise websites connector only supports search permissions visible to **Everyone**.</span></span> <span data-ttu-id="b5acd-129">已編制索引的資料會顯示在搜尋結果中，並對組織中的所有使用者顯示。</span><span class="sxs-lookup"><span data-stu-id="b5acd-129">Indexed data appears in the search results and is visible to all users in the organization.</span></span>

## <a name="assign-property-labels"></a><span data-ttu-id="b5acd-130">指派屬性標籤</span><span class="sxs-lookup"><span data-stu-id="b5acd-130">Assign property labels</span></span>

<span data-ttu-id="b5acd-131">您可以從選項的功能表中選擇，將 source 屬性指派給每個標籤。</span><span class="sxs-lookup"><span data-stu-id="b5acd-131">You can assign a source property to each label by choosing from a menu of options.</span></span> <span data-ttu-id="b5acd-132">雖然這個步驟不是必要的，但具有一些屬性標籤會提升搜尋相關性，並可確保使用者更準確的搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="b5acd-132">While this step is not mandatory, having some property labels will improve the search relevance and ensure more accurate search results for end users.</span></span>

## <a name="manage-schema"></a><span data-ttu-id="b5acd-133">管理架構</span><span class="sxs-lookup"><span data-stu-id="b5acd-133">Manage schema</span></span>

<span data-ttu-id="b5acd-134">在 [**管理架構**] 畫面上，您可以選擇變更架構屬性 (可 **查詢**、**可搜尋、可\*\*\*\*檢索** 及 **可精簡搜尋**) 相關聯的屬性、新增選用的別名，然後選擇 **Content** 屬性。</span><span class="sxs-lookup"><span data-stu-id="b5acd-134">On the **Manage Schema** screen, you have the option to change the schema attributes (**queryable**, **searchable**, **retrievable**, and **refinable**) associated with the properties, add optional aliases, and choose the **Content** property.</span></span>

## <a name="set-the-refresh-schedule"></a><span data-ttu-id="b5acd-135">設定重新整理排程</span><span class="sxs-lookup"><span data-stu-id="b5acd-135">Set the refresh schedule</span></span>

<span data-ttu-id="b5acd-136">企業網站連接器只支援完整重新整理。</span><span class="sxs-lookup"><span data-stu-id="b5acd-136">The Enterprise websites connector only supports a full refresh.</span></span> <span data-ttu-id="b5acd-137">這表示連接器會在每次重新整理時重新編目網站的所有內容。</span><span class="sxs-lookup"><span data-stu-id="b5acd-137">This means that the connector will recrawl all the website's content during every refresh.</span></span> <span data-ttu-id="b5acd-138">若要確定連接器有足夠的時間來編目內容，建議您設定大型重新整理排程間隔。</span><span class="sxs-lookup"><span data-stu-id="b5acd-138">To make sure the connector gets enough time to crawl the content, we recommend that you set a large refresh schedule interval.</span></span> <span data-ttu-id="b5acd-139">建議您在一到兩周之間進行排程重新整理。</span><span class="sxs-lookup"><span data-stu-id="b5acd-139">We recommend a scheduled refresh between one and two weeks.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="b5acd-140">疑難排解</span><span class="sxs-lookup"><span data-stu-id="b5acd-140">Troubleshooting</span></span>

<span data-ttu-id="b5acd-141">當閱讀網站內容時，編目可能會遇到下列的詳細錯誤碼所代表的部分來源錯誤。</span><span class="sxs-lookup"><span data-stu-id="b5acd-141">When reading the website's content, the crawl may encounter some source errors which are represented by the detailed error codes below.</span></span> <span data-ttu-id="b5acd-142">若要取得錯誤類型的詳細資訊，請在選取連接後，移至 [ **錯誤詳細資料** ] 頁面。</span><span class="sxs-lookup"><span data-stu-id="b5acd-142">To get more information on the types of errors, go to the **error details** page after selecting the connection.</span></span> <span data-ttu-id="b5acd-143">按一下 **錯誤碼** 以查看更詳細的錯誤。</span><span class="sxs-lookup"><span data-stu-id="b5acd-143">Click on the **error code** to see more detailed errors.</span></span> <span data-ttu-id="b5acd-144">此外，請參閱 [管理您的連接器](https://docs.microsoft.com/microsoftsearch/manage-connector) 以深入瞭解。</span><span class="sxs-lookup"><span data-stu-id="b5acd-144">Also refer to [Manage your connector](https://docs.microsoft.com/microsoftsearch/manage-connector) to learn more.</span></span>

 <span data-ttu-id="b5acd-145">詳細錯誤代碼</span><span class="sxs-lookup"><span data-stu-id="b5acd-145">Detailed Error code</span></span> | <span data-ttu-id="b5acd-146">錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="b5acd-146">Error message</span></span>
 --- | ---
 <span data-ttu-id="b5acd-147">6001</span><span class="sxs-lookup"><span data-stu-id="b5acd-147">6001</span></span> | <span data-ttu-id="b5acd-148">無法連線正在嘗試編制索引的網站</span><span class="sxs-lookup"><span data-stu-id="b5acd-148">The site that is being tried to index is not reachable</span></span>
 <span data-ttu-id="b5acd-149">6005</span><span class="sxs-lookup"><span data-stu-id="b5acd-149">6005</span></span> | <span data-ttu-id="b5acd-150">根據 robots.txt 設定，已封鎖嘗試編制索引的來源頁面。</span><span class="sxs-lookup"><span data-stu-id="b5acd-150">The source page that is being tried to index has been blocked by as per robots.txt configuration.</span></span>
 <span data-ttu-id="b5acd-151">6008</span><span class="sxs-lookup"><span data-stu-id="b5acd-151">6008</span></span> | <span data-ttu-id="b5acd-152">無法解析 DNS</span><span class="sxs-lookup"><span data-stu-id="b5acd-152">Unable to resolve the DNS</span></span>
 <span data-ttu-id="b5acd-153">6009</span><span class="sxs-lookup"><span data-stu-id="b5acd-153">6009</span></span> | <span data-ttu-id="b5acd-154">針對所有用戶端錯誤 (除了 HTTP 404，408) 之外，請參閱 HTTP 4xx 錯誤碼以取得詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="b5acd-154">For all client side errors (Except HTTP 404, 408), please refer to HTTP 4xx error codes for details.</span></span>
 <span data-ttu-id="b5acd-155">6013</span><span class="sxs-lookup"><span data-stu-id="b5acd-155">6013</span></span> | <span data-ttu-id="b5acd-156">找不到嘗試編制索引的來源頁面。</span><span class="sxs-lookup"><span data-stu-id="b5acd-156">The source page that is being tried to index could not be found.</span></span> <span data-ttu-id="b5acd-157"> (HTTP 404 錯誤) </span><span class="sxs-lookup"><span data-stu-id="b5acd-157">(HTTP 404 error)</span></span>
 <span data-ttu-id="b5acd-158">6018</span><span class="sxs-lookup"><span data-stu-id="b5acd-158">6018</span></span> | <span data-ttu-id="b5acd-159">來源頁面沒有回應，且要求超時。 (HTTP 408 錯誤) </span><span class="sxs-lookup"><span data-stu-id="b5acd-159">The source page is not responding, and the request has timed out. (HTTP 408 error)</span></span>
 <span data-ttu-id="b5acd-160">6021</span><span class="sxs-lookup"><span data-stu-id="b5acd-160">6021</span></span> | <span data-ttu-id="b5acd-161">嘗試編制索引的來源頁面沒有頁面上的文字內容。</span><span class="sxs-lookup"><span data-stu-id="b5acd-161">The source page that is being tried to index has no textual content on the page.</span></span>
 <span data-ttu-id="b5acd-162">6023</span><span class="sxs-lookup"><span data-stu-id="b5acd-162">6023</span></span> | <span data-ttu-id="b5acd-163">嘗試編制索引的來源頁面不受支援 (不是 HTML 頁面) </span><span class="sxs-lookup"><span data-stu-id="b5acd-163">The source page that is being tried to index is unsupported (not a HTML page)</span></span>
 <span data-ttu-id="b5acd-164">6024</span><span class="sxs-lookup"><span data-stu-id="b5acd-164">6024</span></span> | <span data-ttu-id="b5acd-165">嘗試編制索引的來源頁面具有不支援的內容。</span><span class="sxs-lookup"><span data-stu-id="b5acd-165">The source page that is being tried to index has unsupported content.</span></span>

* <span data-ttu-id="b5acd-166">當資料來源由於網路問題或資料來源本身被刪除、移動或重新命名時，就會發生錯誤6001-6013。</span><span class="sxs-lookup"><span data-stu-id="b5acd-166">Errors 6001-6013 occur when the data source is not reachable due to a network issue or when the data source itself is deleted, moved, or renamed.</span></span> <span data-ttu-id="b5acd-167">檢查提供的資料來源詳細資料是否仍然有效。</span><span class="sxs-lookup"><span data-stu-id="b5acd-167">Check if the data source details provided are still valid.</span></span>
* <span data-ttu-id="b5acd-168">當資料來源包含頁面上的非文字內容或頁面不是 HTML 時，就會發生錯誤6021-6024 錯誤。</span><span class="sxs-lookup"><span data-stu-id="b5acd-168">Errors 6021-6024 error occur when the data source contains non-textual content on the page or when the page is not an HTML.</span></span> <span data-ttu-id="b5acd-169">請檢查資料來源，並將此頁面加入排除清單，或略過錯誤。</span><span class="sxs-lookup"><span data-stu-id="b5acd-169">Please check the data source and add this page in exclusion list or ignore the error.</span></span>

## <a name="limitations"></a><span data-ttu-id="b5acd-170">限制</span><span class="sxs-lookup"><span data-stu-id="b5acd-170">Limitations</span></span>

<span data-ttu-id="b5acd-171">企業網站連接器不支援搜尋 **動態網頁** 上的資料。</span><span class="sxs-lookup"><span data-stu-id="b5acd-171">The Enterprise websites connector doesn't support searching data on **dynamic webpages**.</span></span> <span data-ttu-id="b5acd-172">[Confluence](https://www.atlassian.com/software/confluence)與[Unily](https://www.unily.com/)等內容管理系統中的這些網頁範例，或儲存網站內容的資料庫。</span><span class="sxs-lookup"><span data-stu-id="b5acd-172">Examples of those webpages live in content management systems like [Confluence](https://www.atlassian.com/software/confluence) and [Unily](https://www.unily.com/) or databases that store website content.</span></span>
