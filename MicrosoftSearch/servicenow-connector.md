---
title: Microsoft 搜尋的 ServiceNow 連接器
ms.author: kam1
author: TheKarthikeyan
manager: harshkum
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 設定 Microsoft 搜尋的 ServiceNow 連接器
ms.openlocfilehash: 5bcc0870df7c2ad418bb2ae29e9d4d999dcbdf3f
ms.sourcegitcommit: 59cdd3f0f82b7918399bf44d27d9891076090f4f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2020
ms.locfileid: "49367593"
---
# <a name="servicenow-connector"></a><span data-ttu-id="a8660-103">ServiceNow 連接器</span><span class="sxs-lookup"><span data-stu-id="a8660-103">ServiceNow connector</span></span>

<span data-ttu-id="a8660-104">使用 ServiceNow 連接器，您的組織可以為您組織內的使用者準則許可權，索引所有使用者都能看到或限制的知識庫文章。</span><span class="sxs-lookup"><span data-stu-id="a8660-104">With the ServiceNow connector, your organization can index knowledge-base articles that are visible to all users or restricted with user criteria permissions within your organization.</span></span> <span data-ttu-id="a8660-105">從 ServiceNow 設定連接器和索引內容之後，使用者可以從任何 Microsoft 搜尋用戶端搜尋這些文章。</span><span class="sxs-lookup"><span data-stu-id="a8660-105">After you configure the connector and index content from ServiceNow, end users can search for those articles from any Microsoft Search client.</span></span>  

<span data-ttu-id="a8660-106">本文適用于 Microsoft 365 系統管理員或任何設定、執行及監視 ServiceNow 連接器的人員。</span><span class="sxs-lookup"><span data-stu-id="a8660-106">This article is for Microsoft 365 administrators or anyone who configures, runs, and monitors a ServiceNow connector.</span></span> <span data-ttu-id="a8660-107">它說明如何設定連接器和連接器功能、限制及疑難排解技術。</span><span class="sxs-lookup"><span data-stu-id="a8660-107">It explains how to configure your connector and connector capabilities, limitations, and troubleshooting techniques.</span></span>

<span data-ttu-id="a8660-108">瞭解如何存取 Microsoft 建立的連接器 [，以設定 microsoft 的連接器以進行 Microsoft 搜尋](https://docs.microsoft.com/microsoftsearch/configure-connector)。</span><span class="sxs-lookup"><span data-stu-id="a8660-108">Learn how to access Microsoft built connectors from [Set up your Microsoft-built connector for Microsoft Search](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span> <span data-ttu-id="a8660-109">下列文章說明 ServiceNow 連接器特定設定。</span><span class="sxs-lookup"><span data-stu-id="a8660-109">ServiceNow connector specific configuration is explained in the article below.</span></span>

## <a name="connection-settings"></a><span data-ttu-id="a8660-110">連接設定</span><span class="sxs-lookup"><span data-stu-id="a8660-110">Connection Settings</span></span>
<span data-ttu-id="a8660-111">若要連線至您的 ServiceNow 資料，您需要組織的 **ServiceNow 實例 URL**、此帳戶的認證，以及 OAuth 驗證的用戶端識別碼和用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="a8660-111">To connect to your ServiceNow data, you need your organization's **ServiceNow instance URL**, credentials for this account, and the Client ID and Client Secret for OAuth authentication.</span></span>  

<span data-ttu-id="a8660-112">組織的 **ServiceNow 實例 URL** 一般會類似 **HTTPs:// &lt; 您的組織網域> service-now.com**。</span><span class="sxs-lookup"><span data-stu-id="a8660-112">Your organization’s **ServiceNow instance URL** typically looks like **https://&lt;your-organization-domain>.service-now.com**.</span></span> <span data-ttu-id="a8660-113">除了此 URL 之外，您還需要一個帳戶，用以設定 ServiceNow 的連線，以及允許 Microsoft 搜尋依重新整理排程，定期更新 ServiceNow 中的文章。</span><span class="sxs-lookup"><span data-stu-id="a8660-113">Along with this URL, you will need an account for setting up the connection to ServiceNow as well as for allowing Microsoft Search to periodically update the articles from ServiceNow based on the refresh schedule.</span></span> <span data-ttu-id="a8660-114">帳戶至少應具備 <em>知識</em> 角色。</span><span class="sxs-lookup"><span data-stu-id="a8660-114">The account should at least have <em>knowledge</em> role.</span></span> <span data-ttu-id="a8660-115">[瞭解如何指派 ServiceNow 帳戶的角色](https://docs.servicenow.com/bundle/paris-platform-administration/page/administer/users-and-groups/task/t_AssignARoleToAUser.html)。</span><span class="sxs-lookup"><span data-stu-id="a8660-115">[Learn how to assign role for ServiceNow accounts](https://docs.servicenow.com/bundle/paris-platform-administration/page/administer/users-and-groups/task/t_AssignARoleToAUser.html).</span></span>

>[!NOTE]
><span data-ttu-id="a8660-116">如果您想要編目使用者和群組身分識別，以服從 Microsoft 搜尋結果中知識文章的存取權限，該帳戶應該可以存取 ServiceNow 中的下清單記錄：</span><span class="sxs-lookup"><span data-stu-id="a8660-116">If you want to crawl user and group identities to honor access permissions of knowledge articles in Microsoft Search results, the account should have access to read the following table records in ServiceNow:</span></span>
>* <span data-ttu-id="a8660-117">kb_uc_can_contribute_mtom</span><span class="sxs-lookup"><span data-stu-id="a8660-117">kb_uc_can_contribute_mtom</span></span>
>* <span data-ttu-id="a8660-118">kb_uc_can_read_mtom</span><span class="sxs-lookup"><span data-stu-id="a8660-118">kb_uc_can_read_mtom</span></span>
>* <span data-ttu-id="a8660-119">kb_uc_cannot_read_mtom</span><span class="sxs-lookup"><span data-stu-id="a8660-119">kb_uc_cannot_read_mtom</span></span>
>* <span data-ttu-id="a8660-120">kb_uc_cannot_contribute_mtom</span><span class="sxs-lookup"><span data-stu-id="a8660-120">kb_uc_cannot_contribute_mtom</span></span>
>* <span data-ttu-id="a8660-121">sys_user</span><span class="sxs-lookup"><span data-stu-id="a8660-121">sys_user</span></span>
>* <span data-ttu-id="a8660-122">sys_user_has_role</span><span class="sxs-lookup"><span data-stu-id="a8660-122">sys_user_has_role</span></span>
>* <span data-ttu-id="a8660-123">sys_user_grmember</span><span class="sxs-lookup"><span data-stu-id="a8660-123">sys_user_grmember</span></span>
>* <span data-ttu-id="a8660-124">user_criteria</span><span class="sxs-lookup"><span data-stu-id="a8660-124">user_criteria</span></span>
>* <span data-ttu-id="a8660-125">kb_knowledge_base</span><span class="sxs-lookup"><span data-stu-id="a8660-125">kb_knowledge_base</span></span>  
> <span data-ttu-id="a8660-126">您可以為您用來連線 Microsoft 搜尋的帳戶建立和指派角色。</span><span class="sxs-lookup"><span data-stu-id="a8660-126">You can create and assign a role for the account you use to connect with Microsoft Search.</span></span> <span data-ttu-id="a8660-127">可以在該角色上指派對表格的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="a8660-127">Read access to the tables can be assigned on that role.</span></span> <span data-ttu-id="a8660-128">若要瞭解如何設定表記錄的「讀取」存取權，請參閱 [保護資料表記錄](https://developer.servicenow.com/dev.do#!/learn/learning-plans/orlando/new_to_servicenow/app_store_learnv2_securingapps_orlando_creating_and_editing_access_controls)。</span><span class="sxs-lookup"><span data-stu-id="a8660-128">To learn about setting read access to table records, see [Securing Table Records](https://developer.servicenow.com/dev.do#!/learn/learning-plans/orlando/new_to_servicenow/app_store_learnv2_securingapps_orlando_creating_and_editing_access_controls).</span></span>

<span data-ttu-id="a8660-129">若要驗證及同步處理 ServiceNow 中的內容，請選擇下列 **其中一** 項支援的方法：</span><span class="sxs-lookup"><span data-stu-id="a8660-129">To authenticate and sync content from ServiceNow, choose **one of three** supported methods:</span></span> 
1. <span data-ttu-id="a8660-130">基本驗證</span><span class="sxs-lookup"><span data-stu-id="a8660-130">Basic authentication</span></span> 
2. <span data-ttu-id="a8660-131">ServiceNow OAuth (建議) </span><span class="sxs-lookup"><span data-stu-id="a8660-131">ServiceNow OAuth (recommended)</span></span>
3. <span data-ttu-id="a8660-132">Azure AD OpenID Connect</span><span class="sxs-lookup"><span data-stu-id="a8660-132">Azure AD OpenID Connect</span></span>

#### <a name="basic-authentication"></a><span data-ttu-id="a8660-133">基本驗證</span><span class="sxs-lookup"><span data-stu-id="a8660-133">Basic authentication</span></span>

<span data-ttu-id="a8660-134">輸入具有 **知識** 角色的 ServiceNow 帳戶的使用者名稱和密碼，以向您的實例驗證。</span><span class="sxs-lookup"><span data-stu-id="a8660-134">Enter the username and password of ServiceNow account with **knowledge** role to authenticate to your instance.</span></span>

#### <a name="servicenow-oauth"></a><span data-ttu-id="a8660-135">ServiceNow OAuth</span><span class="sxs-lookup"><span data-stu-id="a8660-135">ServiceNow OAuth</span></span>

<span data-ttu-id="a8660-136">若要使用 ServiceNow OAuth 進行驗證，ServiceNow 系統管理員必須布建 ServiceNow 實例中的端點，這樣 Microsoft Search 應用程式才能存取該實例。</span><span class="sxs-lookup"><span data-stu-id="a8660-136">To use ServiceNow OAuth for authentication, a ServiceNow admin needs to provision an endpoint in your ServiceNow instance, so that the Microsoft Search app can access the instance.</span></span> <span data-ttu-id="a8660-137">若要深入瞭解，請參閱在 ServiceNow 檔中 [建立用戶端存取實例的端點](https://docs.servicenow.com/bundle/newyork-platform-administration/page/administer/security/task/t_CreateEndpointforExternalClients.html) 。</span><span class="sxs-lookup"><span data-stu-id="a8660-137">To learn more, see [Create an endpoint for clients to access the instance](https://docs.servicenow.com/bundle/newyork-platform-administration/page/administer/security/task/t_CreateEndpointforExternalClients.html) in the ServiceNow documentation.</span></span>

<span data-ttu-id="a8660-138">下表提供如何填寫端點建立表單的指導方針：</span><span class="sxs-lookup"><span data-stu-id="a8660-138">The following table provides guidance on how to fill out the endpoint creation form:</span></span>

<span data-ttu-id="a8660-139">**Field**</span><span class="sxs-lookup"><span data-stu-id="a8660-139">**Field**</span></span> | <span data-ttu-id="a8660-140">**描述**</span><span class="sxs-lookup"><span data-stu-id="a8660-140">**Description**</span></span> | <span data-ttu-id="a8660-141">**建議值**</span><span class="sxs-lookup"><span data-stu-id="a8660-141">**Recommended Value**</span></span>
--- | --- | ---
<span data-ttu-id="a8660-142">姓名</span><span class="sxs-lookup"><span data-stu-id="a8660-142">Name</span></span> | <span data-ttu-id="a8660-143">此唯一值可識別您需要 OAuth 存取的應用程式。</span><span class="sxs-lookup"><span data-stu-id="a8660-143">This unique value identifies the application that you require OAuth access for.</span></span> | <span data-ttu-id="a8660-144">Microsoft 搜尋</span><span class="sxs-lookup"><span data-stu-id="a8660-144">Microsoft Search</span></span>
<span data-ttu-id="a8660-145">用戶端識別碼</span><span class="sxs-lookup"><span data-stu-id="a8660-145">Client ID</span></span> | <span data-ttu-id="a8660-146">應用程式的唯讀、自動產生的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="a8660-146">A read-only, auto-generated unique ID for the application.</span></span> <span data-ttu-id="a8660-147">當實例要求存取權杖時，會使用用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="a8660-147">The instance uses the client ID when it requests an access token.</span></span> | <span data-ttu-id="a8660-148">NA</span><span class="sxs-lookup"><span data-stu-id="a8660-148">NA</span></span>
<span data-ttu-id="a8660-149">用戶端密碼</span><span class="sxs-lookup"><span data-stu-id="a8660-149">Client secret</span></span> | <span data-ttu-id="a8660-150">使用此共用的機密字串，ServiceNow 實例和 Microsoft 搜尋會授權彼此間的通訊。</span><span class="sxs-lookup"><span data-stu-id="a8660-150">With this shared secret string, the ServiceNow instance and Microsoft Search authorize communications with each other.</span></span> | <span data-ttu-id="a8660-151">請將此視為密碼，遵循安全性最佳作法。</span><span class="sxs-lookup"><span data-stu-id="a8660-151">Follow security best-practices by treating this as a password.</span></span>
<span data-ttu-id="a8660-152">重新導向 URL</span><span class="sxs-lookup"><span data-stu-id="a8660-152">Redirect URL</span></span> | <span data-ttu-id="a8660-153">授權伺服器重新導向所需的回撥 URL。</span><span class="sxs-lookup"><span data-stu-id="a8660-153">A required callback URL that the authorization server redirects to.</span></span> | https://gcs.office.com/v1.0/admin/oauth/callback
<span data-ttu-id="a8660-154">標誌 URL</span><span class="sxs-lookup"><span data-stu-id="a8660-154">Logo URL</span></span> | <span data-ttu-id="a8660-155">包含應用程式標誌之圖像的 URL。</span><span class="sxs-lookup"><span data-stu-id="a8660-155">A URL that contains the image for the application logo.</span></span> | <span data-ttu-id="a8660-156">NA</span><span class="sxs-lookup"><span data-stu-id="a8660-156">NA</span></span>
<span data-ttu-id="a8660-157">作用中</span><span class="sxs-lookup"><span data-stu-id="a8660-157">Active</span></span> | <span data-ttu-id="a8660-158">選取此核取方塊，讓應用程式登錄成為使用中。</span><span class="sxs-lookup"><span data-stu-id="a8660-158">Select the check box to make the application registry active.</span></span> | <span data-ttu-id="a8660-159">設定為 active</span><span class="sxs-lookup"><span data-stu-id="a8660-159">Set to active</span></span>
<span data-ttu-id="a8660-160">重新整理權杖生命週期</span><span class="sxs-lookup"><span data-stu-id="a8660-160">Refresh token lifespan</span></span> | <span data-ttu-id="a8660-161">重新整理權杖有效的秒數。</span><span class="sxs-lookup"><span data-stu-id="a8660-161">The number of seconds that a refresh token is valid.</span></span> <span data-ttu-id="a8660-162">根據預設，重新整理權杖會在100天內到期 (8640000 秒) 。</span><span class="sxs-lookup"><span data-stu-id="a8660-162">By default, refresh tokens expire in 100 days (8640000 seconds).</span></span> | <span data-ttu-id="a8660-163">31536000 (1 年) </span><span class="sxs-lookup"><span data-stu-id="a8660-163">31,536,000 (1 year)</span></span>
<span data-ttu-id="a8660-164">存取權杖使用壽命</span><span class="sxs-lookup"><span data-stu-id="a8660-164">Access token lifespan</span></span> | <span data-ttu-id="a8660-165">存取權杖有效的秒數。</span><span class="sxs-lookup"><span data-stu-id="a8660-165">The number of seconds that an access token is valid.</span></span> | <span data-ttu-id="a8660-166">43200 (12 小時) </span><span class="sxs-lookup"><span data-stu-id="a8660-166">43,200 (12 hours)</span></span>

<span data-ttu-id="a8660-167">輸入用戶端識別碼和用戶端密碼以連接至您的實例。</span><span class="sxs-lookup"><span data-stu-id="a8660-167">Enter the client id and client secret to connect to your instance.</span></span> <span data-ttu-id="a8660-168">連接後，請使用 ServiceNow 帳號憑證來驗證編目的許可權。</span><span class="sxs-lookup"><span data-stu-id="a8660-168">After connecting, use a ServiceNow account credential to authenticate permission to crawl.</span></span> <span data-ttu-id="a8660-169">帳戶至少應具備 **知識** 角色。</span><span class="sxs-lookup"><span data-stu-id="a8660-169">The account should at least have **knowledge** role.</span></span>

#### <a name="azure-ad-openid-connect"></a><span data-ttu-id="a8660-170">Azure AD OpenID Connect</span><span class="sxs-lookup"><span data-stu-id="a8660-170">Azure AD OpenID Connect</span></span>

<span data-ttu-id="a8660-171">若要使用 Azure AD OpenID Connect 以進行驗證，請遵循下列步驟。</span><span class="sxs-lookup"><span data-stu-id="a8660-171">To use Azure AD OpenID Connect for authentication, follow the steps below.</span></span>

###### <a name="step-1-register-a-new-application-in-azure-active-directory"></a><span data-ttu-id="a8660-172">步驟1：在 Azure Active Directory 中註冊新的應用程式</span><span class="sxs-lookup"><span data-stu-id="a8660-172">Step 1: Register a new application in Azure Active Directory</span></span>

<span data-ttu-id="a8660-173">若要瞭解如何在 Azure Active Directory 中註冊新的應用程式，請參閱 [註冊應用程式](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#register-an-application)。</span><span class="sxs-lookup"><span data-stu-id="a8660-173">To learn about registering a new application in Azure Active Directory, see [Register an application](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#register-an-application).</span></span> <span data-ttu-id="a8660-174">選取 [單一承租人組織目錄]。</span><span class="sxs-lookup"><span data-stu-id="a8660-174">Select single tenant organizational directory.</span></span> <span data-ttu-id="a8660-175">不需要重新導向 URI。</span><span class="sxs-lookup"><span data-stu-id="a8660-175">Redirect URI is not needed.</span></span> <span data-ttu-id="a8660-176">註冊後，請記下應用程式 (用戶端) ID 及目錄 (承租人) 識別碼。</span><span class="sxs-lookup"><span data-stu-id="a8660-176">After registration, note down the Application (client) ID and Directory (tenant) ID.</span></span>

###### <a name="step-2-create-a-client-secret"></a><span data-ttu-id="a8660-177">步驟2：建立用戶端密碼</span><span class="sxs-lookup"><span data-stu-id="a8660-177">Step 2: Create a client secret</span></span>

<span data-ttu-id="a8660-178">若要瞭解如何建立用戶端密碼，請參閱 [建立用戶端密碼](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#add-a-client-secret)。</span><span class="sxs-lookup"><span data-stu-id="a8660-178">To learn about creating a client secret, see [Creating a client secret](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#add-a-client-secret).</span></span> <span data-ttu-id="a8660-179">記錄用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="a8660-179">Take a note of client secret.</span></span>

###### <a name="step-3-retrieve-service-principal-object-identifier"></a><span data-ttu-id="a8660-180">步驟3：取回服務主體物件識別碼</span><span class="sxs-lookup"><span data-stu-id="a8660-180">Step 3: Retrieve Service Principal Object Identifier</span></span>

<span data-ttu-id="a8660-181">遵循下列步驟以取得服務主體物件識別碼</span><span class="sxs-lookup"><span data-stu-id="a8660-181">Follow the steps to retrieve Service Principal Object Identifier</span></span>

1. <span data-ttu-id="a8660-182">執行 PowerShell</span><span class="sxs-lookup"><span data-stu-id="a8660-182">Run PowerShell</span></span>
2. <span data-ttu-id="a8660-183">使用下列命令安裝 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="a8660-183">Install Azure PowerShell using the following command</span></span>
```<language>
   Install-Module -Name Az -AllowClobber -Scope CurrentUser
```
3. <span data-ttu-id="a8660-184">連接到 Azure</span><span class="sxs-lookup"><span data-stu-id="a8660-184">Connect to Azure</span></span>
```<language>
    Connect-AzAccount
```
4. <span data-ttu-id="a8660-185">取得服務主體物件識別碼</span><span class="sxs-lookup"><span data-stu-id="a8660-185">Get Service Principal Object Identifier</span></span>
```<language>
   Get-AzADServicePrincipal -ApplicationId "Application-ID"
```
<span data-ttu-id="a8660-186">以您在步驟1中所註冊應用程式的應用程式 (用戶端) ID (取代「應用程式識別碼」) 引號。</span><span class="sxs-lookup"><span data-stu-id="a8660-186">Replace "Application-ID" with Application (client) ID (without quotes) of the application you registered in step 1.</span></span> <span data-ttu-id="a8660-187">請注意，PowerShell 輸出中的 ID 物件的值。</span><span class="sxs-lookup"><span data-stu-id="a8660-187">Note the value of ID object from PowerShell output.</span></span> <span data-ttu-id="a8660-188">它是服務主體識別碼。</span><span class="sxs-lookup"><span data-stu-id="a8660-188">It is the Service Principal ID.</span></span>

<span data-ttu-id="a8660-189">現在，您已具備 Azure 入口網站所需的所有資訊。</span><span class="sxs-lookup"><span data-stu-id="a8660-189">Now you have all the information required from Azure portal.</span></span> <span data-ttu-id="a8660-190">下表提供資訊的快速摘要。</span><span class="sxs-lookup"><span data-stu-id="a8660-190">A quick summary of the information is given in the table below.</span></span>

<span data-ttu-id="a8660-191">**屬性**</span><span class="sxs-lookup"><span data-stu-id="a8660-191">**Property**</span></span> | <span data-ttu-id="a8660-192">**描述**</span><span class="sxs-lookup"><span data-stu-id="a8660-192">**Description**</span></span>
--- | ---
<span data-ttu-id="a8660-193">目錄識別碼 (租使用者識別碼) </span><span class="sxs-lookup"><span data-stu-id="a8660-193">Directory ID (Tenant ID)</span></span> | <span data-ttu-id="a8660-194">這是從步驟 1) 參考 Azure Active Directory 租使用者 (的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="a8660-194">This is a unique ID referring the Azure Active Directory tenant (from step 1).</span></span>
<span data-ttu-id="a8660-195"> (用戶端識別碼的應用程式識別碼) </span><span class="sxs-lookup"><span data-stu-id="a8660-195">Application ID (Client ID)</span></span> | <span data-ttu-id="a8660-196">這是參照步驟1中所註冊之應用程式的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="a8660-196">This is a unique ID referring the application registered in step 1.</span></span>
<span data-ttu-id="a8660-197">用戶端密碼</span><span class="sxs-lookup"><span data-stu-id="a8660-197">Client Secret</span></span> | <span data-ttu-id="a8660-198">這是步驟 2) 中應用程式 (的機密金鑰。</span><span class="sxs-lookup"><span data-stu-id="a8660-198">This is the secret key of the application (from step 2).</span></span> <span data-ttu-id="a8660-199">請將它當作密碼對待。</span><span class="sxs-lookup"><span data-stu-id="a8660-199">Treat it like a password.</span></span>
<span data-ttu-id="a8660-200">服務主體識別碼</span><span class="sxs-lookup"><span data-stu-id="a8660-200">Service Principal ID</span></span> | <span data-ttu-id="a8660-201">作為服務執行之應用程式的身分識別。</span><span class="sxs-lookup"><span data-stu-id="a8660-201">An identity for the application running as a service.</span></span> <span data-ttu-id="a8660-202">步驟 3 () </span><span class="sxs-lookup"><span data-stu-id="a8660-202">(from step 3)</span></span>

###### <a name="step-4-register-servicenow-application"></a><span data-ttu-id="a8660-203">步驟4：註冊 ServiceNow 應用程式</span><span class="sxs-lookup"><span data-stu-id="a8660-203">Step 4: Register ServiceNow Application</span></span>

<span data-ttu-id="a8660-204">在 ServiceNow 實例中，必須進行下列設定。</span><span class="sxs-lookup"><span data-stu-id="a8660-204">The following configuration need to be done in the ServiceNow instance.</span></span>

1. <span data-ttu-id="a8660-205">註冊新的 OAuth OIDC 實體。</span><span class="sxs-lookup"><span data-stu-id="a8660-205">Register a new OAuth OIDC entity.</span></span> <span data-ttu-id="a8660-206">若要瞭解，請參閱 [Create a OAUTH OIDC provider](https://docs.servicenow.com/bundle/orlando-platform-administration/page/administer/security/task/add-OIDC-entity.html)。</span><span class="sxs-lookup"><span data-stu-id="a8660-206">To learn, see [Create an OAuth OIDC provider](https://docs.servicenow.com/bundle/orlando-platform-administration/page/administer/security/task/add-OIDC-entity.html).</span></span>
2. <span data-ttu-id="a8660-207">下表提供如何填寫 OIDC 提供者註冊表單的指導方針。</span><span class="sxs-lookup"><span data-stu-id="a8660-207">The following table provides guidance on how to fill out OIDC provider registration form</span></span>

<span data-ttu-id="a8660-208">**Field**</span><span class="sxs-lookup"><span data-stu-id="a8660-208">**Field**</span></span> | <span data-ttu-id="a8660-209">**描述**</span><span class="sxs-lookup"><span data-stu-id="a8660-209">**Description**</span></span> | <span data-ttu-id="a8660-210">**建議值**</span><span class="sxs-lookup"><span data-stu-id="a8660-210">**Recommended Value**</span></span>
--- | --- | ---
<span data-ttu-id="a8660-211">姓名</span><span class="sxs-lookup"><span data-stu-id="a8660-211">Name</span></span> | <span data-ttu-id="a8660-212">識別 OAuth OIDC 實體的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="a8660-212">A unique name that identifies the OAuth OIDC entity.</span></span> | <span data-ttu-id="a8660-213">Azure AD</span><span class="sxs-lookup"><span data-stu-id="a8660-213">Azure AD</span></span>
<span data-ttu-id="a8660-214">用戶端識別碼</span><span class="sxs-lookup"><span data-stu-id="a8660-214">Client ID</span></span> | <span data-ttu-id="a8660-215">在協力廠商 OAuth OIDC server 中註冊之應用程式的用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="a8660-215">The client ID of the application registered in the third-party OAuth OIDC server.</span></span> <span data-ttu-id="a8660-216">實例在要求存取權杖時使用用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="a8660-216">The instance uses the client ID when requesting an access token.</span></span> | <span data-ttu-id="a8660-217">步驟1的應用程式 (用戶端) 識別碼</span><span class="sxs-lookup"><span data-stu-id="a8660-217">Application (Client) ID from step 1</span></span>
<span data-ttu-id="a8660-218">用戶端密碼</span><span class="sxs-lookup"><span data-stu-id="a8660-218">Client Secret</span></span> | <span data-ttu-id="a8660-219">在協力廠商 OAuth OIDC server 中註冊之應用程式的用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="a8660-219">The client secret of the application registered in the third-party OAuth OIDC server.</span></span> | <span data-ttu-id="a8660-220">步驟2中的用戶端密碼</span><span class="sxs-lookup"><span data-stu-id="a8660-220">Client Secret from step 2</span></span>

<span data-ttu-id="a8660-221">其他所有值都可以是預設值。</span><span class="sxs-lookup"><span data-stu-id="a8660-221">All other values can be default.</span></span>

3. <span data-ttu-id="a8660-222">在 OIDC 提供者註冊表單中，您必須新增新的 OIDC 提供者設定。</span><span class="sxs-lookup"><span data-stu-id="a8660-222">In the OIDC provider registration form, you need to add a new OIDC provider configuration.</span></span> <span data-ttu-id="a8660-223">根據 *OAUTH OIDC 提供者* 設定] 欄位，按一下搜尋圖示，以開啟 OIDC 設定的記錄。</span><span class="sxs-lookup"><span data-stu-id="a8660-223">Click the search icon against *OAuth OIDC Provider Configuration* field to open the records of OIDC configurations.</span></span> <span data-ttu-id="a8660-224">按一下 [新增]。</span><span class="sxs-lookup"><span data-stu-id="a8660-224">Click New.</span></span>
4. <span data-ttu-id="a8660-225">下表提供如何填寫 OIDC 提供者設定表單的指導方針</span><span class="sxs-lookup"><span data-stu-id="a8660-225">The following table provides guidance on how to fill out OIDC provider configuration form</span></span>

<span data-ttu-id="a8660-226">**Field**</span><span class="sxs-lookup"><span data-stu-id="a8660-226">**Field**</span></span> | <span data-ttu-id="a8660-227">**建議值**</span><span class="sxs-lookup"><span data-stu-id="a8660-227">**Recommended Value**</span></span>
--- | ---
<span data-ttu-id="a8660-228">OIDC 提供者</span><span class="sxs-lookup"><span data-stu-id="a8660-228">OIDC Provider</span></span> |  <span data-ttu-id="a8660-229">Azure AD</span><span class="sxs-lookup"><span data-stu-id="a8660-229">Azure AD</span></span>
<span data-ttu-id="a8660-230">OIDC 中繼資料 URL</span><span class="sxs-lookup"><span data-stu-id="a8660-230">OIDC Metadata URL</span></span> | <span data-ttu-id="a8660-231">其格式必須為 HTTPs \: //login.microsoftonline.com/"tenandId"/.well-known/openid-configuration</span><span class="sxs-lookup"><span data-stu-id="a8660-231">This must be in the form https\://login.microsoftonline.com/"tenandId"/.well-known/openid-configuration</span></span> <br/><span data-ttu-id="a8660-232">將 "tenantID" 取代為步驟 1 (不含引號) 的目錄 (租使用者) ID。</span><span class="sxs-lookup"><span data-stu-id="a8660-232">Replace "tenantID" with Directory (tenant) ID from step 1 (without quotes).</span></span>
<span data-ttu-id="a8660-233">OIDC 設定快取壽命範圍</span><span class="sxs-lookup"><span data-stu-id="a8660-233">OIDC Configuration Cache Life Span</span></span> |  <span data-ttu-id="a8660-234">120</span><span class="sxs-lookup"><span data-stu-id="a8660-234">120</span></span>
<span data-ttu-id="a8660-235">應用程式</span><span class="sxs-lookup"><span data-stu-id="a8660-235">Application</span></span> | <span data-ttu-id="a8660-236">全域</span><span class="sxs-lookup"><span data-stu-id="a8660-236">Global</span></span>
<span data-ttu-id="a8660-237">使用者宣告</span><span class="sxs-lookup"><span data-stu-id="a8660-237">User Claim</span></span> | <span data-ttu-id="a8660-238">子</span><span class="sxs-lookup"><span data-stu-id="a8660-238">sub</span></span>
<span data-ttu-id="a8660-239">使用者欄位</span><span class="sxs-lookup"><span data-stu-id="a8660-239">User Field</span></span> | <span data-ttu-id="a8660-240">使用者識別碼</span><span class="sxs-lookup"><span data-stu-id="a8660-240">User ID</span></span>
<span data-ttu-id="a8660-241">啟用 JTI 宣告驗證</span><span class="sxs-lookup"><span data-stu-id="a8660-241">Enable JTI claim verification</span></span> | <span data-ttu-id="a8660-242">停用</span><span class="sxs-lookup"><span data-stu-id="a8660-242">Disabled</span></span>

5. <span data-ttu-id="a8660-243">按一下 [提交]，然後更新 OAuth OIDC 實體表單。</span><span class="sxs-lookup"><span data-stu-id="a8660-243">Click Submit and Update the OAuth OIDC Entity form.</span></span>

###### <a name="step-5-create-a-servicenow-account"></a><span data-ttu-id="a8660-244">步驟5：建立 ServiceNow 帳戶</span><span class="sxs-lookup"><span data-stu-id="a8660-244">Step 5: Create a ServiceNow account</span></span>

<span data-ttu-id="a8660-245">請參閱指示建立 ServiceNow 帳戶、 [在 ServiceNow 中建立使用者](https://docs.servicenow.com/bundle/paris-platform-administration/page/administer/users-and-groups/task/t_CreateAUser.html)。</span><span class="sxs-lookup"><span data-stu-id="a8660-245">Refer the instructions to create a ServiceNow account, [create a user in ServiceNow](https://docs.servicenow.com/bundle/paris-platform-administration/page/administer/users-and-groups/task/t_CreateAUser.html).</span></span>

<span data-ttu-id="a8660-246">下表提供如何填寫 ServiceNow 使用者帳戶註冊的指導方針。</span><span class="sxs-lookup"><span data-stu-id="a8660-246">The following table provides guidance on how to fill out the ServiceNow user account registration</span></span>

<span data-ttu-id="a8660-247">**Field**</span><span class="sxs-lookup"><span data-stu-id="a8660-247">**Field**</span></span> | <span data-ttu-id="a8660-248">**建議值**</span><span class="sxs-lookup"><span data-stu-id="a8660-248">**Recommended Value**</span></span>
--- | ---
<span data-ttu-id="a8660-249">使用者識別碼</span><span class="sxs-lookup"><span data-stu-id="a8660-249">User ID</span></span> | <span data-ttu-id="a8660-250">步驟3的服務主體識別碼</span><span class="sxs-lookup"><span data-stu-id="a8660-250">Service Principal ID from step 3</span></span>
<span data-ttu-id="a8660-251">僅 Web 服務存取權</span><span class="sxs-lookup"><span data-stu-id="a8660-251">Web service access only</span></span> | <span data-ttu-id="a8660-252">Checked</span><span class="sxs-lookup"><span data-stu-id="a8660-252">Checked</span></span>

<span data-ttu-id="a8660-253">其他所有值都可以保留預設值。</span><span class="sxs-lookup"><span data-stu-id="a8660-253">All other values can be left to default.</span></span>

###### <a name="step-6-enable-knowledge-role-for-the-servicenow-account"></a><span data-ttu-id="a8660-254">步驟6：啟用 ServiceNow 帳戶的知識角色</span><span class="sxs-lookup"><span data-stu-id="a8660-254">Step 6: Enable Knowledge role for the ServiceNow account</span></span>

<span data-ttu-id="a8660-255">存取您用 ServiceNow 主體識別碼建立的 ServiceNow 帳戶做為使用者識別碼並指派知識角色。</span><span class="sxs-lookup"><span data-stu-id="a8660-255">Access the ServiceNow account you created with ServiceNow Principal ID as User ID and assign the knowledge role.</span></span> <span data-ttu-id="a8660-256">您可以在這裡找到將角色指派給 ServiceNow 帳戶的指示， [將角色指派給使用者](https://docs.servicenow.com/bundle/paris-platform-administration/page/administer/users-and-groups/task/t_AssignARoleToAUser.html)。</span><span class="sxs-lookup"><span data-stu-id="a8660-256">Instructions to assigning a role to a ServiceNow account can be found here, [assign a role to a user](https://docs.servicenow.com/bundle/paris-platform-administration/page/administer/users-and-groups/task/t_AssignARoleToAUser.html).</span></span>

<span data-ttu-id="a8660-257">使用應用程式識別碼做為用戶端識別碼 (從步驟 1) ，並從系統管理中心的「步驟 2) 用戶端密碼 (，以使用 Azure AD ServiceNow Connect 向您的 OpenID 實例進行驗證。</span><span class="sxs-lookup"><span data-stu-id="a8660-257">Use Application ID as Client ID (from step 1), and Client secret (from step 2) in admin center configuration wizard to authenticate to your ServiceNow instance using Azure AD OpenID Connect.</span></span>

## <a name="filter-data"></a><span data-ttu-id="a8660-258">篩選資料</span><span class="sxs-lookup"><span data-stu-id="a8660-258">Filter data</span></span>

<span data-ttu-id="a8660-259">使用 ServiceNow 查詢字串，您可以指定同步處理文章的條件。</span><span class="sxs-lookup"><span data-stu-id="a8660-259">With a ServiceNow query string, you can specify conditions for syncing articles.</span></span> <span data-ttu-id="a8660-260">它就像是 **SQL Select** 語句中的 **Where** 子句。</span><span class="sxs-lookup"><span data-stu-id="a8660-260">It's like a **Where** clause in a **SQL Select** statement.</span></span> <span data-ttu-id="a8660-261">例如，您可以選擇只為發佈和使用中的文章編制索引。</span><span class="sxs-lookup"><span data-stu-id="a8660-261">For example, you can choose to index only articles that are published and active.</span></span> <span data-ttu-id="a8660-262">若要瞭解如何建立您自己的查詢字串，請參閱 [使用篩選產生編碼的查詢字串](https://docs.servicenow.com/bundle/paris-platform-user-interface/page/use/using-lists/task/t_GenEncodQueryStringFilter.html)。</span><span class="sxs-lookup"><span data-stu-id="a8660-262">To learn about creating your own query string, see [Generate an encoded query string using a filter](https://docs.servicenow.com/bundle/paris-platform-user-interface/page/use/using-lists/task/t_GenEncodQueryStringFilter.html).</span></span>

## <a name="manage-search-permissions"></a><span data-ttu-id="a8660-263">管理搜尋許可權</span><span class="sxs-lookup"><span data-stu-id="a8660-263">Manage search permissions</span></span>

<span data-ttu-id="a8660-264">ServiceNow 連接器支援 **所有人都** 可以看到的搜尋許可權，或是 **只有存取此資料來源的人員才能使用**。</span><span class="sxs-lookup"><span data-stu-id="a8660-264">The ServiceNow connector supports search permissions visible to **Everyone** or **Only people with access to this data source**.</span></span> <span data-ttu-id="a8660-265">已編制索引的資料會顯示在搜尋結果中，並可供組織中的所有使用者或分別存取這些資料的使用者看到。</span><span class="sxs-lookup"><span data-stu-id="a8660-265">Indexed data appears in the search results and is visible to all users in the organization or users who have access to them respectively.</span></span> <span data-ttu-id="a8660-266">ServiceNow 連接器支援不含高級腳本的預設使用者準則許可權。</span><span class="sxs-lookup"><span data-stu-id="a8660-266">ServiceNow Connector supports default user criteria permissions without advanced scripts.</span></span> <span data-ttu-id="a8660-267">當連接器使用 advanced script 遇到使用者準則時，搜尋結果中將不會顯示使用該使用者準則的所有資料。</span><span class="sxs-lookup"><span data-stu-id="a8660-267">When the connector encounters a user criteria with advanced script, all data using that user criteria will not be showed in search results.</span></span>

<span data-ttu-id="a8660-268">如果您只選擇可 **存取此資料來源的人員**，您需要進一步選擇您的 ServiceNow 實例是否有 Azure Active DIRECTORY (AAD) 布建使用者或非 AAD 使用者。</span><span class="sxs-lookup"><span data-stu-id="a8660-268">If you choose **Only people with access to this data source**, you need to further choose whether your ServiceNow instance has Azure Active Directory (AAD) provisioned users or Non-AAD users.</span></span>

>[!NOTE]
><span data-ttu-id="a8660-269">如果您選擇 [AAD] 做為身分識別來源的類型，請確定您在 ServiceNow 中為電子郵件目標屬性指派 UPN 來源屬性。</span><span class="sxs-lookup"><span data-stu-id="a8660-269">If you choose AAD as the type of identity source, make sure you are assigning UPN source property to email targeted property in ServiceNow.</span></span> <span data-ttu-id="a8660-270">若要驗證或變更您的對應，請參閱 [自訂使用者布建屬性-在 Azure Active Directory 中 SaaS 應用程式的對應](https://docs.microsoft.com/azure/active-directory/app-provisioning/customize-application-attributes)。</span><span class="sxs-lookup"><span data-stu-id="a8660-270">To verify or change your mappings, see [Customizing user provisioning attribute-mappings for SaaS applications in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/app-provisioning/customize-application-attributes).</span></span>

<span data-ttu-id="a8660-271">如果您選擇從 ServiceNow 實例中攝取一個 ACL，並為身分識別類型選取 "非 AAD"，請參閱 [Map 您的非 AZURE AD](map-non-aad.md) 身分識別，以取得對應身分識別的指示。</span><span class="sxs-lookup"><span data-stu-id="a8660-271">If you chose to ingest an ACL from your ServiceNow instance and selected "non-AAD" for the identity type see [Map your non-Azure AD Identities](map-non-aad.md) for instructions on mapping the identities.</span></span>

## <a name="assign-property-labels"></a><span data-ttu-id="a8660-272">指派屬性標籤</span><span class="sxs-lookup"><span data-stu-id="a8660-272">Assign property labels</span></span>

<span data-ttu-id="a8660-273">您可以從選項的功能表中選擇，將 source 屬性指派給每個標籤。</span><span class="sxs-lookup"><span data-stu-id="a8660-273">You can assign a source property to each label by choosing from a menu of options.</span></span> <span data-ttu-id="a8660-274">雖然這個步驟不是必要的，但具有一些屬性標籤會提升搜尋相關性，並可確保使用者更準確的搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="a8660-274">While this step is not mandatory, having some property labels will improve the search relevance and ensure more accurate search results for end users.</span></span>

## <a name="manage-schema"></a><span data-ttu-id="a8660-275">管理架構</span><span class="sxs-lookup"><span data-stu-id="a8660-275">Manage schema</span></span>

<span data-ttu-id="a8660-276">在 [**管理架構**] 畫面上，您可以選擇變更架構屬性 (可 **查詢**、**可搜尋、可\*\*\*\*檢索** 及 **可精簡搜尋**) 相關聯的屬性、新增選用的別名，然後選擇 **Content** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a8660-276">On the **Manage Schema** screen, you have the option to change the schema attributes (**queryable**, **searchable**, **retrievable**, and **refinable**) associated with the properties, add optional aliases, and choose the **Content** property.</span></span>

## <a name="set-the-refresh-schedule"></a><span data-ttu-id="a8660-277">設定重新整理排程</span><span class="sxs-lookup"><span data-stu-id="a8660-277">Set the refresh schedule</span></span>

<span data-ttu-id="a8660-278">ServiceNow 連接器支援完整和累加編目的更新排程。</span><span class="sxs-lookup"><span data-stu-id="a8660-278">The ServiceNow connector supports refresh schedules for both full and incremental crawls.</span></span> <span data-ttu-id="a8660-279">我們建議您同時設定兩者。</span><span class="sxs-lookup"><span data-stu-id="a8660-279">We recommend that you set both.</span></span>

<span data-ttu-id="a8660-280">完整編目排程會找到先前同步處理至 Microsoft 搜尋索引的已刪除文章，以及任何移出同步篩選的文章。</span><span class="sxs-lookup"><span data-stu-id="a8660-280">A full crawl schedule finds deleted articles that were previously synced to the Microsoft Search index and any articles that moved out of the sync filter.</span></span> <span data-ttu-id="a8660-281">當您第一次連線至 ServiceNow 時，會執行完整編目以同步處理所有知識文庫文章。</span><span class="sxs-lookup"><span data-stu-id="a8660-281">When you first connect to ServiceNow, a full crawl runs to sync all the knowledge-base articles.</span></span> <span data-ttu-id="a8660-282">若要同步處理新專案並進行更新，您必須排程累加編目。</span><span class="sxs-lookup"><span data-stu-id="a8660-282">To sync new items and make updates, you need to schedule incremental crawls.</span></span>

<span data-ttu-id="a8660-283">建議的預設值為一天的完整編目及四小時為增量編目。</span><span class="sxs-lookup"><span data-stu-id="a8660-283">The recommended default is one day for a full crawl and four hours for an incremental crawl.</span></span>
>[!NOTE]
><span data-ttu-id="a8660-284">針對身分識別，只會套用已排程的完整編目。</span><span class="sxs-lookup"><span data-stu-id="a8660-284">For identities, only full crawl scheduled will be applied.</span></span>

## <a name="review-and-publish"></a><span data-ttu-id="a8660-285">審閱及發佈</span><span class="sxs-lookup"><span data-stu-id="a8660-285">Review and publish</span></span>

<span data-ttu-id="a8660-286">設定連接器之後，即可複查及發佈連線。</span><span class="sxs-lookup"><span data-stu-id="a8660-286">After you configure your connector, you can review and publish the connection.</span></span>

## <a name="next-steps"></a><span data-ttu-id="a8660-287">後續步驟</span><span class="sxs-lookup"><span data-stu-id="a8660-287">Next steps</span></span>

<span data-ttu-id="a8660-288">在發佈連線後，您必須自訂搜尋結果頁面。</span><span class="sxs-lookup"><span data-stu-id="a8660-288">After publishing the connection, you need to customize the search results page.</span></span> <span data-ttu-id="a8660-289">若要瞭解如何自訂搜尋結果，請參閱 [自訂搜尋結果頁面](https://docs.microsoft.com/microsoftsearch/configure-connector#next-steps-customize-the-search-results-page)。</span><span class="sxs-lookup"><span data-stu-id="a8660-289">To learn about customizing search results, see [Customize the search results page](https://docs.microsoft.com/microsoftsearch/configure-connector#next-steps-customize-the-search-results-page).</span></span>