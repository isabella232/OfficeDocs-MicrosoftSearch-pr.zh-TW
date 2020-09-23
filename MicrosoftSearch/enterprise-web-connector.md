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
ms.openlocfilehash: b4d9f837892bcfd795421530e0571fa0509a2761
ms.sourcegitcommit: be0c64845477127d73ee24dc727e4583ced3d0e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/22/2020
ms.locfileid: "48206939"
---
<!-- markdownlint-disable no-inline-html -->
# <a name="enterprise-websites-connector"></a><span data-ttu-id="1e113-103">企業網站連接器</span><span class="sxs-lookup"><span data-stu-id="1e113-103">Enterprise websites connector</span></span>

<span data-ttu-id="1e113-104">透過企業網站連接器，您的組織可以 **從其內部網站**對文章和內容編制索引。</span><span class="sxs-lookup"><span data-stu-id="1e113-104">With the Enterprise websites connector, your organization can index articles and **content from its internal-facing websites**.</span></span> <span data-ttu-id="1e113-105">在您設定網站的連接器及同步內容之後，使用者可以從任何 Microsoft 搜尋用戶端搜尋該內容。</span><span class="sxs-lookup"><span data-stu-id="1e113-105">After you configure the connector and sync content from the website, end users can search for that content from any Microsoft Search client.</span></span>

<span data-ttu-id="1e113-106">本文適用于 [Microsoft 365](https://www.microsoft.com/microsoft-365) 系統管理員或任何設定、執行及監視企業網站連接器的人員。</span><span class="sxs-lookup"><span data-stu-id="1e113-106">This article is for [Microsoft 365](https://www.microsoft.com/microsoft-365) administrators or anyone who configures, runs, and monitors an Enterprise websites connector.</span></span> <span data-ttu-id="1e113-107">它說明如何設定連接器和連接器功能、限制及疑難排解技術。</span><span class="sxs-lookup"><span data-stu-id="1e113-107">It explains how to configure your connector and connector capabilities, limitations, and troubleshooting techniques.</span></span>  

## <a name="connect-to-a-data-source"></a><span data-ttu-id="1e113-108">連接到資料來源</span><span class="sxs-lookup"><span data-stu-id="1e113-108">Connect to a data source</span></span>

<span data-ttu-id="1e113-109">若要連線至資料來源，您需要根 URL 和驗證格式：無、基本驗證，或使用 [Azure Active Directory (AZURE AD) ](https://docs.microsoft.com/azure/active-directory/)的 OAuth 2.0。</span><span class="sxs-lookup"><span data-stu-id="1e113-109">To connect to your data source, you need your root URL and a form of authentication: None, Basic Authentication, or OAuth 2.0 with [Azure Active Directory (Azure AD)](https://docs.microsoft.com/azure/active-directory/).</span></span>

### <a name="authentication"></a><span data-ttu-id="1e113-110">驗證</span><span class="sxs-lookup"><span data-stu-id="1e113-110">Authentication</span></span>

<span data-ttu-id="1e113-111">基本驗證需要使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="1e113-111">Basic Authentication requires a username and password.</span></span> <span data-ttu-id="1e113-112">使用 [Microsoft 365 系統管理中心](https://admin.microsoft.com)建立此 bot 帳戶。</span><span class="sxs-lookup"><span data-stu-id="1e113-112">Create this bot account by using the [Microsoft 365 admin center](https://admin.microsoft.com).</span></span>

<span data-ttu-id="1e113-113">使用 [AZURE AD](https://docs.microsoft.com/azure/active-directory/) OAuth 2.0 需要資源識別碼、用戶端識別碼和用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="1e113-113">OAuth 2.0 with [Azure AD](https://docs.microsoft.com/azure/active-directory/) requires a resource ID, Client ID, and Client Secret.</span></span>

<span data-ttu-id="1e113-114">如需詳細資訊，請參閱 [使用 OAuth 2.0 程式碼授與流程授權存取 Azure Active Directory web 應用程式](https://docs.microsoft.com/azure/active-directory/develop/v1-protocols-oauth-code)。</span><span class="sxs-lookup"><span data-stu-id="1e113-114">For more information, see [Authorize access to Azure Active Directory web applications using OAuth 2.0 code grant flow](https://docs.microsoft.com/azure/active-directory/develop/v1-protocols-oauth-code).</span></span> <span data-ttu-id="1e113-115">使用下列值進行註冊：</span><span class="sxs-lookup"><span data-stu-id="1e113-115">Register with the following values:</span></span>

<span data-ttu-id="1e113-116">**名稱：** Microsoft 搜尋</span><span class="sxs-lookup"><span data-stu-id="1e113-116">**Name:** Microsoft Search</span></span> <br/>
<span data-ttu-id="1e113-117">**Redirect_URI：**`https://gcs.office.com/v1.0/admin/oauth/callback`</span><span class="sxs-lookup"><span data-stu-id="1e113-117">**Redirect_URI:** `https://gcs.office.com/v1.0/admin/oauth/callback`</span></span>

<span data-ttu-id="1e113-118">若要取得資源、client_id 及 client_secret 的值，請移至 **使用授權碼以要求** 重新導向 URL 網頁上的存取權杖。</span><span class="sxs-lookup"><span data-stu-id="1e113-118">To get the values for the resource, client_id, and client_secret, go to **Use the authorization code to request an access token** on the redirect URL webpage.</span></span>

<span data-ttu-id="1e113-119">如需詳細資訊，請參閱 [快速入門：使用 Microsoft identity Platform 註冊應用程式](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app)。</span><span class="sxs-lookup"><span data-stu-id="1e113-119">For even more information, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

### <a name="root-url"></a><span data-ttu-id="1e113-120">根 URL</span><span class="sxs-lookup"><span data-stu-id="1e113-120">Root URL</span></span>

<span data-ttu-id="1e113-121">根 URL 會啟動編目，並用於驗證。</span><span class="sxs-lookup"><span data-stu-id="1e113-121">The root URL is what initiates the crawl and is used for authentication.</span></span> <span data-ttu-id="1e113-122">您可以從您想要編目的網站首頁取得 URL。</span><span class="sxs-lookup"><span data-stu-id="1e113-122">You can get the URL from the home page of the website you want to crawl.</span></span>

## <a name="select-the-source-properties"></a><span data-ttu-id="1e113-123">選取來源屬性</span><span class="sxs-lookup"><span data-stu-id="1e113-123">Select the source properties</span></span>

<span data-ttu-id="1e113-124">來源屬性是根據企業網站的資料格式定義。</span><span class="sxs-lookup"><span data-stu-id="1e113-124">Source properties are defined based on the data format of the enterprise website.</span></span> <span data-ttu-id="1e113-125">不過，您可以建立 **排除清單** ，以排除部分 URLs 若該內容機密或不需要編目的情況下取得編目。</span><span class="sxs-lookup"><span data-stu-id="1e113-125">However, you can create an **Exclusion list** to exclude some URLs from getting crawled if that content is sensitive or not worth crawling.</span></span> <span data-ttu-id="1e113-126">若要建立排除清單，請流覽根 URL。</span><span class="sxs-lookup"><span data-stu-id="1e113-126">To create an exclusion list, browse through the root URL.</span></span> <span data-ttu-id="1e113-127">您可以選擇在設定過程中將排除的 URLs 新增至清單。</span><span class="sxs-lookup"><span data-stu-id="1e113-127">You have the option to add the excluded URLs to the list during the configuration process.</span></span>

## <a name="manage-search-permissions"></a><span data-ttu-id="1e113-128">管理搜尋許可權</span><span class="sxs-lookup"><span data-stu-id="1e113-128">Manage search permissions</span></span>

<span data-ttu-id="1e113-129">不支援 (ACLs) 的存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="1e113-129">There's no support for Access Control Lists (ACLs).</span></span> <span data-ttu-id="1e113-130">因此，我們建議您只連接組織內任何使用者都能看見的網站。</span><span class="sxs-lookup"><span data-stu-id="1e113-130">Thus, we recommend connecting only the websites that are visible to any user within your organization.</span></span>

## <a name="set-the-refresh-schedule"></a><span data-ttu-id="1e113-131">設定重新整理排程</span><span class="sxs-lookup"><span data-stu-id="1e113-131">Set the refresh schedule</span></span>

<span data-ttu-id="1e113-132">企業網站連接器只支援完整編目。</span><span class="sxs-lookup"><span data-stu-id="1e113-132">The Enterprise websites connector only supports a full crawl.</span></span> <span data-ttu-id="1e113-133">這表示連接器會在每次編目期間讀取網站的所有內容。</span><span class="sxs-lookup"><span data-stu-id="1e113-133">This means that the connector reads all the website's content during every crawl.</span></span> <span data-ttu-id="1e113-134">若要確定連接器有足夠的時間可讀取內容，建議您設定大型重新整理排程間隔。</span><span class="sxs-lookup"><span data-stu-id="1e113-134">To make sure the connector gets enough time to read the content, we recommend that you set a large refresh schedule interval.</span></span> <span data-ttu-id="1e113-135">建議您在一到兩周之間進行排程重新整理。</span><span class="sxs-lookup"><span data-stu-id="1e113-135">We recommend a scheduled refresh between one and two weeks.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="1e113-136">疑難排解</span><span class="sxs-lookup"><span data-stu-id="1e113-136">Troubleshooting</span></span>

<span data-ttu-id="1e113-137">當閱讀網站內容時，編目可能會遇到下列的詳細錯誤碼所代表的部分來源錯誤。</span><span class="sxs-lookup"><span data-stu-id="1e113-137">When reading the website's content, the crawl may encounter some source errors which are represented by the detailed error codes below.</span></span> <span data-ttu-id="1e113-138">若要取得錯誤類型的詳細資訊，請在選取連接後，移至 [ **錯誤詳細資料** ] 頁面。</span><span class="sxs-lookup"><span data-stu-id="1e113-138">To get more information on the types of errors, go to the **error details** page after selecting the connection.</span></span> <span data-ttu-id="1e113-139">按一下 **錯誤碼** 以查看更詳細的錯誤。</span><span class="sxs-lookup"><span data-stu-id="1e113-139">Click on the **error code** to see more detailed errors.</span></span> <span data-ttu-id="1e113-140">此外，請參閱 [管理您的連接器](https://docs.microsoft.com/microsoftsearch/manage-connector) 以深入瞭解。</span><span class="sxs-lookup"><span data-stu-id="1e113-140">Also refer to [Manage your connector](https://docs.microsoft.com/microsoftsearch/manage-connector) to learn more.</span></span>

 <span data-ttu-id="1e113-141">詳細錯誤代碼</span><span class="sxs-lookup"><span data-stu-id="1e113-141">Detailed Error code</span></span> | <span data-ttu-id="1e113-142">錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="1e113-142">Error message</span></span>
 --- | ---
 <span data-ttu-id="1e113-143">6001</span><span class="sxs-lookup"><span data-stu-id="1e113-143">6001</span></span> | <span data-ttu-id="1e113-144">無法連線正在嘗試編制索引的網站</span><span class="sxs-lookup"><span data-stu-id="1e113-144">The site that is being tried to index is not reachable</span></span>
 <span data-ttu-id="1e113-145">6005</span><span class="sxs-lookup"><span data-stu-id="1e113-145">6005</span></span> | <span data-ttu-id="1e113-146">根據 robots.txt 設定，已封鎖嘗試編制索引的來源頁面。</span><span class="sxs-lookup"><span data-stu-id="1e113-146">The source page that is being tried to index has been blocked by as per robots.txt configuration.</span></span>
 <span data-ttu-id="1e113-147">6008</span><span class="sxs-lookup"><span data-stu-id="1e113-147">6008</span></span> | <span data-ttu-id="1e113-148">無法解析 DNS</span><span class="sxs-lookup"><span data-stu-id="1e113-148">Unable to resolve the DNS</span></span>
 <span data-ttu-id="1e113-149">6009</span><span class="sxs-lookup"><span data-stu-id="1e113-149">6009</span></span> | <span data-ttu-id="1e113-150">針對所有用戶端錯誤 (除了 HTTP 404，408) 之外，請參閱 HTTP 4xx 錯誤碼以取得詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="1e113-150">For all client side errors (Except HTTP 404, 408), please refer to HTTP 4xx error codes for details.</span></span>
 <span data-ttu-id="1e113-151">6013</span><span class="sxs-lookup"><span data-stu-id="1e113-151">6013</span></span> | <span data-ttu-id="1e113-152">找不到嘗試編制索引的來源頁面。</span><span class="sxs-lookup"><span data-stu-id="1e113-152">The source page that is being tried to index could not be found.</span></span> <span data-ttu-id="1e113-153"> (HTTP 404 錯誤) </span><span class="sxs-lookup"><span data-stu-id="1e113-153">(HTTP 404 error)</span></span>
 <span data-ttu-id="1e113-154">6018</span><span class="sxs-lookup"><span data-stu-id="1e113-154">6018</span></span> | <span data-ttu-id="1e113-155">來源頁面沒有回應，且要求超時。 (HTTP 408 錯誤) </span><span class="sxs-lookup"><span data-stu-id="1e113-155">The source page is not responding, and the request has timed out. (HTTP 408 error)</span></span>
 <span data-ttu-id="1e113-156">6021</span><span class="sxs-lookup"><span data-stu-id="1e113-156">6021</span></span> | <span data-ttu-id="1e113-157">嘗試編制索引的來源頁面沒有頁面上的文字內容。</span><span class="sxs-lookup"><span data-stu-id="1e113-157">The source page that is being tried to index has no textual content on the page.</span></span>
 <span data-ttu-id="1e113-158">6023</span><span class="sxs-lookup"><span data-stu-id="1e113-158">6023</span></span> | <span data-ttu-id="1e113-159">嘗試編制索引的來源頁面不受支援 (不是 HTML 頁面) </span><span class="sxs-lookup"><span data-stu-id="1e113-159">The source page that is being tried to index is unsupported (not a HTML page)</span></span>
 <span data-ttu-id="1e113-160">6024</span><span class="sxs-lookup"><span data-stu-id="1e113-160">6024</span></span> | <span data-ttu-id="1e113-161">嘗試編制索引的來源頁面具有不支援的內容。</span><span class="sxs-lookup"><span data-stu-id="1e113-161">The source page that is being tried to index has unsupported content.</span></span>

* <span data-ttu-id="1e113-162">當資料來源由於網路問題或資料來源本身被刪除、移動或重新命名時，就會發生錯誤6001-6013。</span><span class="sxs-lookup"><span data-stu-id="1e113-162">Errors 6001-6013 occur when the data source is not reachable due to a network issue or when the data source itself is deleted, moved, or renamed.</span></span> <span data-ttu-id="1e113-163">檢查提供的資料來源詳細資料是否仍然有效。</span><span class="sxs-lookup"><span data-stu-id="1e113-163">Check if the data source details provided are still valid.</span></span>
* <span data-ttu-id="1e113-164">當資料來源包含頁面上的非文字內容或頁面不是 HTML 時，就會發生錯誤6021-6024 錯誤。</span><span class="sxs-lookup"><span data-stu-id="1e113-164">Errors 6021-6024 error occur when the data source contains non-textual content on the page or when the page is not an HTML.</span></span> <span data-ttu-id="1e113-165">請檢查資料來源，並將此頁面加入排除清單，或略過錯誤。</span><span class="sxs-lookup"><span data-stu-id="1e113-165">Please check the data source and add this page in exclusion list or ignore the error.</span></span>

## <a name="limitations"></a><span data-ttu-id="1e113-166">限制</span><span class="sxs-lookup"><span data-stu-id="1e113-166">Limitations</span></span>

<span data-ttu-id="1e113-167">企業網站連接器不支援搜尋 **動態網頁**上的資料。</span><span class="sxs-lookup"><span data-stu-id="1e113-167">The Enterprise websites connector doesn't support searching data on **dynamic webpages**.</span></span> <span data-ttu-id="1e113-168">[Confluence](https://www.atlassian.com/software/confluence)與[Unily](https://www.unily.com/)等內容管理系統中的這些網頁範例，或儲存網站內容的資料庫。</span><span class="sxs-lookup"><span data-stu-id="1e113-168">Examples of those webpages live in content management systems like [Confluence](https://www.atlassian.com/software/confluence) and [Unily](https://www.unily.com/) or databases that store website content.</span></span>
