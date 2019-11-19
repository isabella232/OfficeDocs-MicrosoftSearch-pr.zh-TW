---
title: Microsoft Search 的企業網站連接器
ms.author: mounika.narayanan
author: monaray
manager: mnirkhe
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 設定 Microsoft Search 企業網站連接器
ms.openlocfilehash: 14eef035f4cc054ab87582b573cb6b7e3c12d0c7
ms.sourcegitcommit: 68087149c769a7cdde80944dd9c9933d2bf4a23f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/18/2019
ms.locfileid: "38699519"
---
# <a name="enterprise-websites-connector"></a><span data-ttu-id="711da-103">企業網站連接器</span><span class="sxs-lookup"><span data-stu-id="711da-103">Enterprise websites connector</span></span>

<span data-ttu-id="711da-104">與企業網站連接器，您的組織可以索引文件和**其內部公開網站的內容**。</span><span class="sxs-lookup"><span data-stu-id="711da-104">With the Enterprise websites connector, your organization can index articles and **content from its internal-facing websites**.</span></span> <span data-ttu-id="711da-105">設定從網站的同步處理內容與連接器之後，使用者可以搜尋任何 Microsoft 搜尋用戶端從該內容。</span><span class="sxs-lookup"><span data-stu-id="711da-105">After you configure the connector and sync content from the website, end users can search for that content from any Microsoft Search client.</span></span>

<span data-ttu-id="711da-106">本文適用於[Microsoft 365](https://www.microsoft.com/microsoft-365)系統管理員或人設定、 執行，並監視企業網站連接器。</span><span class="sxs-lookup"><span data-stu-id="711da-106">This article is for [Microsoft 365](https://www.microsoft.com/microsoft-365) administrators or anyone who configures, runs, and monitors an Enterprise websites connector.</span></span> <span data-ttu-id="711da-107">本文說明如何設定連接器，連接器功能、 限制和疑難排解技巧。</span><span class="sxs-lookup"><span data-stu-id="711da-107">It explains how to configure your connector and connector capabilities, limitations, and troubleshooting techniques.</span></span>  

## <a name="connect-to-a-data-source"></a><span data-ttu-id="711da-108">連線至資料來源</span><span class="sxs-lookup"><span data-stu-id="711da-108">Connect to a data source</span></span> 
<span data-ttu-id="711da-109">若要連線至您的資料來源，您需要您的根 URL 和形式的驗證： 基本驗證] 或 [OAuth 2.0 與[Azure Active Directory (Azure AD)](https://docs.microsoft.com/azure/active-directory/)。</span><span class="sxs-lookup"><span data-stu-id="711da-109">To connect to your data source, you need your root URL and a form of authentication: Basic Authentication or OAuth 2.0 with [Azure Active Directory (Azure AD)](https://docs.microsoft.com/azure/active-directory/).</span></span>

### <a name="root-url"></a><span data-ttu-id="711da-110">根 URL</span><span class="sxs-lookup"><span data-stu-id="711da-110">Root URL</span></span>
<span data-ttu-id="711da-111">根 URL 是什麼初始編目，並驗證所使用。</span><span class="sxs-lookup"><span data-stu-id="711da-111">The root URL is what initiates the crawl and is used for authentication.</span></span> <span data-ttu-id="711da-112">您可以從您要編目之網站的 [首頁] 頁面上取得 URL。</span><span class="sxs-lookup"><span data-stu-id="711da-112">You can get the URL from the home page of the website you want to crawl.</span></span>

### <a name="authentication"></a><span data-ttu-id="711da-113">驗證</span><span class="sxs-lookup"><span data-stu-id="711da-113">Authentication</span></span> 
<span data-ttu-id="711da-114">基本驗證需要使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="711da-114">Basic Authentication requires a username and password.</span></span> <span data-ttu-id="711da-115">使用 Microsoft 365[系統管理中心](https://admin.microsoft.com)來建立此 bot 帳戶。</span><span class="sxs-lookup"><span data-stu-id="711da-115">Create this bot account by using the Microsoft 365 [admin center](https://admin.microsoft.com).</span></span>

<span data-ttu-id="711da-116">與[Azure AD](https://docs.microsoft.com/azure/active-directory/)的 OAuth 2.0 需要租用戶識別碼、 資源識別碼、 用戶端識別碼和用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="711da-116">OAuth 2.0 with [Azure AD](https://docs.microsoft.com/azure/active-directory/) requires a tenant ID, resource ID, Client ID, and Client Secret.</span></span>
<span data-ttu-id="711da-117">如需詳細資訊，請參閱[Azure Active Directory 的 web 應用程式的授權存取使用 OAuth 2.0 的程式碼授與流程](https://docs.microsoft.com/azure/active-directory/develop/v1-protocols-oauth-code)。</span><span class="sxs-lookup"><span data-stu-id="711da-117">For more information, see [Authorize access to Azure Active Directory web applications using OAuth 2.0 code grant flow](https://docs.microsoft.com/azure/active-directory/develop/v1-protocols-oauth-code).</span></span> <span data-ttu-id="711da-118">註冊使用下列值：</span><span class="sxs-lookup"><span data-stu-id="711da-118">Register with the following values:</span></span>
* <span data-ttu-id="711da-119">**名稱：** Microsoft Search</span><span class="sxs-lookup"><span data-stu-id="711da-119">**Name:** Microsoft Search</span></span>
* <span data-ttu-id="711da-120">**Redirect_URI:**`https://gcs.office.com/v1.0/admin/oauth/callback`</span><span class="sxs-lookup"><span data-stu-id="711da-120">**Redirect_URI:** `https://gcs.office.com/v1.0/admin/oauth/callback`</span></span>

<span data-ttu-id="711da-121">若要取得具名的租用戶中的值，資源、 client_id 和 client_secret，移至**使用授權程式碼，以要求存取權杖**重新導向 URL 網頁上。</span><span class="sxs-lookup"><span data-stu-id="711da-121">To get the values for named tenant, resource, client_id, and client_secret, go to **Use the authorization code to request an access token** on the redirect URL webpage.</span></span>

<span data-ttu-id="711da-122">更多的資訊，請參閱[快速入門： 註冊的應用程式與 Microsoft 身份識別平台](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app)。</span><span class="sxs-lookup"><span data-stu-id="711da-122">For even more information, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

### <a name="reverse-proxy-url"></a><span data-ttu-id="711da-123">反向 proxy URL</span><span class="sxs-lookup"><span data-stu-id="711da-123">Reverse proxy URL</span></span> 
<span data-ttu-id="711da-124">企業網站連接器是雲端為基礎，所以它不會存取內部部署內容。</span><span class="sxs-lookup"><span data-stu-id="711da-124">The Enterprise websites connector is cloud-based, so it doesn't access on-premises content.</span></span> <span data-ttu-id="711da-125">若要提供權限，請安裝反向 proxy。</span><span class="sxs-lookup"><span data-stu-id="711da-125">To provide that access, install a reverse proxy.</span></span> <span data-ttu-id="711da-126">反向 proxy 提供安全且可靠的存取權的內部網站。</span><span class="sxs-lookup"><span data-stu-id="711da-126">A reverse proxy provides secure, reliable access to on-premises websites.</span></span> <span data-ttu-id="711da-127">我們建議您[Azure 應用程式 Proxy](https://docs.microsoft.com/azure/active-directory/manage-apps/application-proxy)。</span><span class="sxs-lookup"><span data-stu-id="711da-127">We recommend [Azure Application Proxy](https://docs.microsoft.com/azure/active-directory/manage-apps/application-proxy).</span></span>

<span data-ttu-id="711da-128">根 URL 和驗證的反向 proxy 需求是雲端式的內容，如同不同之處在於反向 proxy 伺服器所提供的根 URL 和驗證。</span><span class="sxs-lookup"><span data-stu-id="711da-128">The reverse proxy requirement for root URL and authentication is the same as for cloud-based content, except that the root URL and authentication are provided by the reverse proxy server.</span></span>

<span data-ttu-id="711da-129">請參閱[用來存取遠端與 Azure AD 應用程式 Proxy 的應用程式的安全性考量](https://docs.microsoft.com/azure/active-directory/manage-apps/application-proxy-security)。</span><span class="sxs-lookup"><span data-stu-id="711da-129">See [Security considerations for accessing apps remotely with Azure AD Application Proxy](https://docs.microsoft.com/azure/active-directory/manage-apps/application-proxy-security).</span></span>

## <a name="select-the-source-properties"></a><span data-ttu-id="711da-130">選取 [來源屬性</span><span class="sxs-lookup"><span data-stu-id="711da-130">Select the source properties</span></span> 
<span data-ttu-id="711da-131">來源內容被定義為基礎的企業網站的資料格式。</span><span class="sxs-lookup"><span data-stu-id="711da-131">Source properties are defined based on the data format of the enterprise website.</span></span> <span data-ttu-id="711da-132">不過，您可以建立**排除清單中**排除某些 Url 如果取得編目內容是敏感或不值得編目。</span><span class="sxs-lookup"><span data-stu-id="711da-132">However, you can create an **Exclusion list** to exclude some URLs from getting crawled if that content is sensitive or not worth crawling.</span></span> <span data-ttu-id="711da-133">若要建立排除清單中，瀏覽的根 URL。</span><span class="sxs-lookup"><span data-stu-id="711da-133">To create an exclusion list, browse through the root URL.</span></span> <span data-ttu-id="711da-134">您必須將排除的 Url 新增至清單中，在設定過程的選項。</span><span class="sxs-lookup"><span data-stu-id="711da-134">You have the option to add the excluded URLs to the list during the configuration process.</span></span>

## <a name="manage-search-permissions"></a><span data-ttu-id="711da-135">管理搜尋的權限</span><span class="sxs-lookup"><span data-stu-id="711da-135">Manage search permissions</span></span> 
<span data-ttu-id="711da-136">沒有存取控制清單 (Acl) 支援。</span><span class="sxs-lookup"><span data-stu-id="711da-136">There's no support for Access Control Lists (ACLs).</span></span> <span data-ttu-id="711da-137">因此，我們建議您連接可看見您的組織內的任何使用者的網站。</span><span class="sxs-lookup"><span data-stu-id="711da-137">Thus, we recommend connecting only the websites that are visible to any user within your organization.</span></span>

## <a name="set-the-refresh-schedule"></a><span data-ttu-id="711da-138">設定重新整理排程</span><span class="sxs-lookup"><span data-stu-id="711da-138">Set the refresh schedule</span></span>
<span data-ttu-id="711da-139">企業網站連接器僅支援完整編目。</span><span class="sxs-lookup"><span data-stu-id="711da-139">The Enterprise websites connector only supports a full crawl.</span></span> <span data-ttu-id="711da-140">這表示，連接器會讀取所有網站的內容，每個編目期間。</span><span class="sxs-lookup"><span data-stu-id="711da-140">This means that the connector reads all the website's content during every crawl.</span></span> <span data-ttu-id="711da-141">若要確定連接器取得足夠的時間來閱讀的內容，我們建議您設定較大的重新整理排程的時間間隔。</span><span class="sxs-lookup"><span data-stu-id="711da-141">To make sure the connector gets enough time to read the content, we recommend that you set a large refresh schedule interval.</span></span> <span data-ttu-id="711da-142">建議的三天之間的兩週排定重新整理。</span><span class="sxs-lookup"><span data-stu-id="711da-142">We recommend a scheduled refresh between three days and two weeks.</span></span>

## <a name="limitations"></a><span data-ttu-id="711da-143">限制</span><span class="sxs-lookup"><span data-stu-id="711da-143">Limitations</span></span> 
<span data-ttu-id="711da-144">企業網站連接器不支援在動態網頁上的搜尋資料。</span><span class="sxs-lookup"><span data-stu-id="711da-144">The Enterprise websites connector doesn't support searching data on dynamic webpages.</span></span> <span data-ttu-id="711da-145">範例的這些網頁存在於內容管理系統，例如[機器人學](https://www.atlassian.com/software/confluence)和[Unily](https://www.unily.com/)或儲存網站內容的資料庫中。</span><span class="sxs-lookup"><span data-stu-id="711da-145">Examples of those webpages live in content management systems like [Confluence](https://www.atlassian.com/software/confluence) and [Unily](https://www.unily.com/) or databases that store website content.</span></span>