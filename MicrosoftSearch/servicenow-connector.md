---
title: Microsoft 搜尋 ServiceNow Graph 連接器
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
description: 設定 Microsoft 搜尋的 ServiceNow Graph 連接器
ms.openlocfilehash: 31b581af2c51a5c26b161e778b242e396afe91fd
ms.sourcegitcommit: 6cffa2d29448be9a22514e7b4c3009c522af0860
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "52774078"
---
<!---Previous ms.author: kam1 --->

# <a name="servicenow-graph-connector"></a><span data-ttu-id="9285b-103">ServiceNow Graph 連接器</span><span class="sxs-lookup"><span data-stu-id="9285b-103">ServiceNow Graph Connector</span></span>

<span data-ttu-id="9285b-104">ServiceNow Graph 連接器可讓您的組織根據組織內的使用者準則許可權，為使用者顯示對其所看到之知識型文章的索引。</span><span class="sxs-lookup"><span data-stu-id="9285b-104">The ServiceNow Graph connector allows your organization to index knowledge-based articles visible to users according to the user criteria permissions within your organization.</span></span> <span data-ttu-id="9285b-105">從 ServiceNow 設定連接器和索引內容之後，使用者可以從任何 Microsoft 搜尋用戶端搜尋文章。</span><span class="sxs-lookup"><span data-stu-id="9285b-105">After you configure the connector and index content from ServiceNow, users can search for the articles from any Microsoft Search client.</span></span>

> [!NOTE]
> <span data-ttu-id="9285b-106">請閱讀 [**Graph 連接器**](configure-connector.md)文章的設定，以瞭解一般 Graph 連接器設定指示。</span><span class="sxs-lookup"><span data-stu-id="9285b-106">Read the [**Setup for your Graph connector**](configure-connector.md) article to understand the general Graph connectors setup instructions.</span></span>

<span data-ttu-id="9285b-107">本文適用于設定、執行及監視 ServiceNow Graph 連接器的任何人。</span><span class="sxs-lookup"><span data-stu-id="9285b-107">This article is for anyone who configures, runs, and monitors a ServiceNow Graph connector.</span></span> <span data-ttu-id="9285b-108">它會補充一般設定程式，並顯示只適用于 ServiceNow Graph 連接器的指示。</span><span class="sxs-lookup"><span data-stu-id="9285b-108">It supplements the general setup process, and shows instructions that apply to only for the ServiceNow Graph connector.</span></span> <span data-ttu-id="9285b-109">本文也包含 [疑難排解](#troubleshooting) 及 [限制](#limitations)的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9285b-109">This article also includes information about [Troubleshooting](#troubleshooting) and [Limitations](#limitations).</span></span>

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a><span data-ttu-id="9285b-110">步驟1：在 Microsoft 365 系統管理中心新增 Graph 連接器</span><span class="sxs-lookup"><span data-stu-id="9285b-110">Step 1: Add a Graph connector in the Microsoft 365 admin center</span></span>

<span data-ttu-id="9285b-111">遵循一般 [設定指示](./configure-connector.md)。</span><span class="sxs-lookup"><span data-stu-id="9285b-111">Follow the general [setup instructions](./configure-connector.md).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-2-name-the-connection"></a><span data-ttu-id="9285b-112">步驟2：命名連線</span><span class="sxs-lookup"><span data-stu-id="9285b-112">Step 2: Name the connection</span></span>

<span data-ttu-id="9285b-113">遵循一般 [設定指示](./configure-connector.md)。</span><span class="sxs-lookup"><span data-stu-id="9285b-113">Follow the general [setup instructions](./configure-connector.md).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-3-connection-settings"></a><span data-ttu-id="9285b-114">步驟3：連接設定</span><span class="sxs-lookup"><span data-stu-id="9285b-114">Step 3: Connection Settings</span></span>

<span data-ttu-id="9285b-115">若要連線至您的 ServiceNow 資料，請使用您組織的 ServiceNow 此帳戶的 **實例 URL** 認證、用戶端識別碼，以及 OAuth 驗證的用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="9285b-115">To connect to your ServiceNow data, use your organization's **ServiceNow instance URL** credentials for this account, the Client ID, and Client Secret for OAuth authentication.</span></span>  

<span data-ttu-id="9285b-116">組織的 **ServiceNow 實例 URL** 一般會類似 **HTTPs:// &lt; 您的組織網域> service-now.com**。</span><span class="sxs-lookup"><span data-stu-id="9285b-116">Your organization's **ServiceNow instance URL** typically looks like **https://&lt;your-organization-domain>.service-now.com**.</span></span> <span data-ttu-id="9285b-117">使用此 URL 時，您需要有帳戶來設定 ServiceNow 的連線，以及允許 Microsoft 搜尋依據重新整理排程從 ServiceNow 更新文章。</span><span class="sxs-lookup"><span data-stu-id="9285b-117">Along with this URL, you need an account for setting up the connection to ServiceNow and for allowing Microsoft Search to update the articles from ServiceNow based on the refresh schedule.</span></span> <span data-ttu-id="9285b-118">帳戶至少應具備 <em>知識</em> 角色。</span><span class="sxs-lookup"><span data-stu-id="9285b-118">The account should at least have <em>knowledge</em> role.</span></span> <span data-ttu-id="9285b-119">[瞭解如何指派 ServiceNow 帳戶的角色](https://docs.servicenow.com/bundle/paris-platform-administration/page/administer/users-and-groups/task/t_AssignARoleToAUser.html)。</span><span class="sxs-lookup"><span data-stu-id="9285b-119">[Learn how to assign role for ServiceNow accounts](https://docs.servicenow.com/bundle/paris-platform-administration/page/administer/users-and-groups/task/t_AssignARoleToAUser.html).</span></span>

>[!NOTE]
><span data-ttu-id="9285b-120">如果您想要編目使用者和群組身分識別，以服從 Microsoft 搜尋結果中知識文章的存取權限，該帳戶應該可以存取 ServiceNow 中的下清單記錄：</span><span class="sxs-lookup"><span data-stu-id="9285b-120">If you want to crawl user and group identities to honor access permissions of knowledge articles in Microsoft Search results, the account should have access to read the following table records in ServiceNow:</span></span>
>* <span data-ttu-id="9285b-121">kb_uc_can_contribute_mtom</span><span class="sxs-lookup"><span data-stu-id="9285b-121">kb_uc_can_contribute_mtom</span></span>
>* <span data-ttu-id="9285b-122">kb_uc_can_read_mtom</span><span class="sxs-lookup"><span data-stu-id="9285b-122">kb_uc_can_read_mtom</span></span>
>* <span data-ttu-id="9285b-123">kb_uc_cannot_read_mtom</span><span class="sxs-lookup"><span data-stu-id="9285b-123">kb_uc_cannot_read_mtom</span></span>
>* <span data-ttu-id="9285b-124">kb_uc_cannot_contribute_mtom</span><span class="sxs-lookup"><span data-stu-id="9285b-124">kb_uc_cannot_contribute_mtom</span></span>
>* <span data-ttu-id="9285b-125">sys_user</span><span class="sxs-lookup"><span data-stu-id="9285b-125">sys_user</span></span>
>* <span data-ttu-id="9285b-126">sys_user_has_role</span><span class="sxs-lookup"><span data-stu-id="9285b-126">sys_user_has_role</span></span>
>* <span data-ttu-id="9285b-127">sys_user_grmember</span><span class="sxs-lookup"><span data-stu-id="9285b-127">sys_user_grmember</span></span>
>* <span data-ttu-id="9285b-128">user_criteria</span><span class="sxs-lookup"><span data-stu-id="9285b-128">user_criteria</span></span>
>* <span data-ttu-id="9285b-129">kb_knowledge_base</span><span class="sxs-lookup"><span data-stu-id="9285b-129">kb_knowledge_base</span></span>  
> <span data-ttu-id="9285b-130">您可以為您用來連線 Microsoft 搜尋的帳戶建立和指派角色。</span><span class="sxs-lookup"><span data-stu-id="9285b-130">You can create and assign a role for the account you use to connect with Microsoft Search.</span></span> <span data-ttu-id="9285b-131">可以在該角色上指派對表格的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="9285b-131">Read access to the tables can be assigned on that role.</span></span> <span data-ttu-id="9285b-132">若要瞭解如何設定表記錄的「讀取」存取權，請參閱 [保護資料表記錄](https://developer.servicenow.com/dev.do#!/learn/learning-plans/orlando/new_to_servicenow/app_store_learnv2_securingapps_orlando_creating_and_editing_access_controls)。</span><span class="sxs-lookup"><span data-stu-id="9285b-132">To learn about setting read access to table records, see [Securing Table Records](https://developer.servicenow.com/dev.do#!/learn/learning-plans/orlando/new_to_servicenow/app_store_learnv2_securingapps_orlando_creating_and_editing_access_controls).</span></span>

<span data-ttu-id="9285b-133">若要驗證及同步處理 ServiceNow 中的內容，請選擇下列 **其中一** 項支援的方法：</span><span class="sxs-lookup"><span data-stu-id="9285b-133">To authenticate and sync content from ServiceNow, choose **one of three** supported methods:</span></span>

1. <span data-ttu-id="9285b-134">基本驗證</span><span class="sxs-lookup"><span data-stu-id="9285b-134">Basic authentication</span></span>
1. <span data-ttu-id="9285b-135">ServiceNow OAuth (建議) </span><span class="sxs-lookup"><span data-stu-id="9285b-135">ServiceNow OAuth (recommended)</span></span>
1. <span data-ttu-id="9285b-136">Azure AD OpenID 連線</span><span class="sxs-lookup"><span data-stu-id="9285b-136">Azure AD OpenID Connect</span></span>

### <a name="basic-authentication"></a><span data-ttu-id="9285b-137">基本驗證</span><span class="sxs-lookup"><span data-stu-id="9285b-137">Basic authentication</span></span>

<span data-ttu-id="9285b-138">輸入具有 **知識** 角色的 ServiceNow 帳戶的使用者名稱和密碼，以向您的實例驗證。</span><span class="sxs-lookup"><span data-stu-id="9285b-138">Enter the username and password of ServiceNow account with **knowledge** role to authenticate to your instance.</span></span>

### <a name="servicenow-oauth"></a><span data-ttu-id="9285b-139">ServiceNow OAuth</span><span class="sxs-lookup"><span data-stu-id="9285b-139">ServiceNow OAuth</span></span>

<span data-ttu-id="9285b-140">若要使用 ServiceNow OAuth 進行驗證，請在 ServiceNow 實例中布建端點。</span><span class="sxs-lookup"><span data-stu-id="9285b-140">To use ServiceNow OAuth for authentication, provision an endpoint in your ServiceNow instance.</span></span> <span data-ttu-id="9285b-141">Microsoft Search 應用程式會使用它來存取實例。</span><span class="sxs-lookup"><span data-stu-id="9285b-141">The Microsoft Search app will use it to access the instance.</span></span> <span data-ttu-id="9285b-142">若要深入瞭解，請參閱在 ServiceNow 檔中 [建立用戶端存取實例的端點](https://docs.servicenow.com/bundle/newyork-platform-administration/page/administer/security/task/t_CreateEndpointforExternalClients.html) 。</span><span class="sxs-lookup"><span data-stu-id="9285b-142">To learn more, see [Create an endpoint for clients to access the instance](https://docs.servicenow.com/bundle/newyork-platform-administration/page/administer/security/task/t_CreateEndpointforExternalClients.html) in the ServiceNow documentation.</span></span>

<span data-ttu-id="9285b-143">下表提供如何填寫端點建立表單的指導方針：</span><span class="sxs-lookup"><span data-stu-id="9285b-143">The following table provides guidance on how to fill out the endpoint creation form:</span></span>

<span data-ttu-id="9285b-144">欄位</span><span class="sxs-lookup"><span data-stu-id="9285b-144">Field</span></span> | <span data-ttu-id="9285b-145">描述</span><span class="sxs-lookup"><span data-stu-id="9285b-145">Description</span></span> | <span data-ttu-id="9285b-146">建議值</span><span class="sxs-lookup"><span data-stu-id="9285b-146">Recommended Value</span></span> 
--- | --- | ---
<span data-ttu-id="9285b-147">名稱</span><span class="sxs-lookup"><span data-stu-id="9285b-147">Name</span></span> | <span data-ttu-id="9285b-148">識別您需要 OAuth 存取之應用程式的唯一值。</span><span class="sxs-lookup"><span data-stu-id="9285b-148">Unique value that identifies the application that you require OAuth access for.</span></span> | <span data-ttu-id="9285b-149">Microsoft 搜尋</span><span class="sxs-lookup"><span data-stu-id="9285b-149">Microsoft Search</span></span>
<span data-ttu-id="9285b-150">用戶端識別碼</span><span class="sxs-lookup"><span data-stu-id="9285b-150">Client ID</span></span> | <span data-ttu-id="9285b-151">應用程式的唯讀、自動產生的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="9285b-151">A read-only, auto generated unique ID for the application.</span></span> <span data-ttu-id="9285b-152">當實例要求存取權杖時，會使用用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="9285b-152">The instance uses the client ID when it requests an access token.</span></span> | <span data-ttu-id="9285b-153">NA</span><span class="sxs-lookup"><span data-stu-id="9285b-153">NA</span></span>
<span data-ttu-id="9285b-154">用戶端密碼</span><span class="sxs-lookup"><span data-stu-id="9285b-154">Client secret</span></span> | <span data-ttu-id="9285b-155">使用此共用的機密字串，ServiceNow 實例和 Microsoft 搜尋會授權彼此間的通訊。</span><span class="sxs-lookup"><span data-stu-id="9285b-155">With this shared secret string, the ServiceNow instance and Microsoft Search authorize communications with each other.</span></span> | <span data-ttu-id="9285b-156">遵循安全性最佳作法，將密碼當做密碼對待。</span><span class="sxs-lookup"><span data-stu-id="9285b-156">Follow security best-practices by treating the secret as a password.</span></span>
<span data-ttu-id="9285b-157">重新導向 URL</span><span class="sxs-lookup"><span data-stu-id="9285b-157">Redirect URL</span></span> | <span data-ttu-id="9285b-158">授權伺服器重新導向所需的回撥 URL。</span><span class="sxs-lookup"><span data-stu-id="9285b-158">A required callback URL that the authorization server redirects to.</span></span> | https://gcs.office.com/v1.0/admin/oauth/callback
<span data-ttu-id="9285b-159">標誌 URL</span><span class="sxs-lookup"><span data-stu-id="9285b-159">Logo URL</span></span> | <span data-ttu-id="9285b-160">包含應用程式標誌之圖像的 URL。</span><span class="sxs-lookup"><span data-stu-id="9285b-160">A URL that contains the image for the application logo.</span></span> | <span data-ttu-id="9285b-161">NA</span><span class="sxs-lookup"><span data-stu-id="9285b-161">NA</span></span>
<span data-ttu-id="9285b-162">作用中</span><span class="sxs-lookup"><span data-stu-id="9285b-162">Active</span></span> | <span data-ttu-id="9285b-163">選取此核取方塊，讓應用程式登錄成為使用中。</span><span class="sxs-lookup"><span data-stu-id="9285b-163">Select the check box to make the application registry active.</span></span> | <span data-ttu-id="9285b-164">設定為 active</span><span class="sxs-lookup"><span data-stu-id="9285b-164">Set to active</span></span>
<span data-ttu-id="9285b-165">重新整理權杖生命週期</span><span class="sxs-lookup"><span data-stu-id="9285b-165">Refresh token lifespan</span></span> | <span data-ttu-id="9285b-166">重新整理權杖有效的秒數。</span><span class="sxs-lookup"><span data-stu-id="9285b-166">The number of seconds that a refresh token is valid.</span></span> <span data-ttu-id="9285b-167">根據預設，重新整理權杖會在100天內到期 (8640000 秒) 。</span><span class="sxs-lookup"><span data-stu-id="9285b-167">By default, refresh tokens expire in 100 days (8,640,000 seconds).</span></span> | <span data-ttu-id="9285b-168">31536000 (1 年) </span><span class="sxs-lookup"><span data-stu-id="9285b-168">31,536,000 (1 year)</span></span>
<span data-ttu-id="9285b-169">存取權杖使用壽命</span><span class="sxs-lookup"><span data-stu-id="9285b-169">Access token lifespan</span></span> | <span data-ttu-id="9285b-170">存取權杖有效的秒數。</span><span class="sxs-lookup"><span data-stu-id="9285b-170">The number of seconds that an access token is valid.</span></span> | <span data-ttu-id="9285b-171">43200 (12 小時) </span><span class="sxs-lookup"><span data-stu-id="9285b-171">43,200 (12 hours)</span></span>

<span data-ttu-id="9285b-172">輸入用戶端識別碼和用戶端密碼以連接至您的實例。</span><span class="sxs-lookup"><span data-stu-id="9285b-172">Enter the client ID and client secret to connect to your instance.</span></span> <span data-ttu-id="9285b-173">連接後，請使用 ServiceNow 帳號憑證來驗證編目的許可權。</span><span class="sxs-lookup"><span data-stu-id="9285b-173">After connecting, use a ServiceNow account credential to authenticate permission to crawl.</span></span> <span data-ttu-id="9285b-174">帳戶至少應具備 **知識** 角色。</span><span class="sxs-lookup"><span data-stu-id="9285b-174">The account should at least have **knowledge** role.</span></span>

### <a name="azure-ad-openid-connect"></a><span data-ttu-id="9285b-175">Azure AD OpenID 連線</span><span class="sxs-lookup"><span data-stu-id="9285b-175">Azure AD OpenID Connect</span></span>

<span data-ttu-id="9285b-176">若要使用 Azure AD OpenID 連線進行驗證，請遵循下列步驟。</span><span class="sxs-lookup"><span data-stu-id="9285b-176">To use Azure AD OpenID Connect for authentication, follow the steps below.</span></span>

## <a name="step-3a-register-a-new-application-in-azure-active-directory"></a><span data-ttu-id="9285b-177">步驟3。 a：在 Azure Active Directory 中註冊新的應用程式</span><span class="sxs-lookup"><span data-stu-id="9285b-177">Step 3.a: Register a new application in Azure Active Directory</span></span>

<span data-ttu-id="9285b-178">若要瞭解如何在 Azure Active Directory 中註冊新的應用程式，請參閱[註冊應用程式](/azure/active-directory/develop/quickstart-register-app#register-an-application)。</span><span class="sxs-lookup"><span data-stu-id="9285b-178">To learn about registering a new application in Azure Active Directory, see [Register an application](/azure/active-directory/develop/quickstart-register-app#register-an-application).</span></span> <span data-ttu-id="9285b-179">選取 [單一承租人組織目錄]。</span><span class="sxs-lookup"><span data-stu-id="9285b-179">Select single tenant organizational directory.</span></span> <span data-ttu-id="9285b-180">不需要重新導向 URI。</span><span class="sxs-lookup"><span data-stu-id="9285b-180">Redirect URI isn't needed.</span></span> <span data-ttu-id="9285b-181">註冊後，請記下應用程式 (用戶端) ID 及目錄 (承租人) 識別碼。</span><span class="sxs-lookup"><span data-stu-id="9285b-181">After registration, note down the Application (client) ID and Directory (tenant) ID.</span></span>

## <a name="step-3b-create-a-client-secret"></a><span data-ttu-id="9285b-182">步驟3：建立用戶端密碼</span><span class="sxs-lookup"><span data-stu-id="9285b-182">Step 3.b: Create a client secret</span></span>

<span data-ttu-id="9285b-183">若要瞭解如何建立用戶端密碼，請參閱 [建立用戶端密碼](/azure/active-directory/develop/quickstart-register-app#add-a-client-secret)。</span><span class="sxs-lookup"><span data-stu-id="9285b-183">To learn about creating a client secret, see [Creating a client secret](/azure/active-directory/develop/quickstart-register-app#add-a-client-secret).</span></span> <span data-ttu-id="9285b-184">記錄用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="9285b-184">Take a note of client secret.</span></span>

## <a name="step-3c-retrieve-service-principal-object-identifier"></a><span data-ttu-id="9285b-185">步驟 3 .. c：取回服務主體物件識別碼</span><span class="sxs-lookup"><span data-stu-id="9285b-185">Step 3.c: Retrieve Service Principal Object Identifier</span></span>

<span data-ttu-id="9285b-186">遵循下列步驟以取得服務主體物件識別碼</span><span class="sxs-lookup"><span data-stu-id="9285b-186">Follow the steps to retrieve Service Principal Object Identifier</span></span>

1. <span data-ttu-id="9285b-187">執行 PowerShell。</span><span class="sxs-lookup"><span data-stu-id="9285b-187">Run PowerShell.</span></span>

2. <span data-ttu-id="9285b-188">使用下列命令安裝 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="9285b-188">Install Azure PowerShell using the following command.</span></span>

   ```powershell
   Install-Module -Name Az -AllowClobber -Scope CurrentUser
   ```

3. <span data-ttu-id="9285b-189">連線 Azure。</span><span class="sxs-lookup"><span data-stu-id="9285b-189">Connect to Azure.</span></span>

   ```powershell
   Connect-AzAccount
   ```

4. <span data-ttu-id="9285b-190">取得服務主體物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="9285b-190">Get Service Principal Object Identifier.</span></span>

   ```powershell
   Get-AzADServicePrincipal -ApplicationId "Application-ID"
   ```
   <span data-ttu-id="9285b-191">將 "Application ID" 取代為您在步驟3中所註冊應用程式的應用程式 (用戶端) ID (但不) 引號。</span><span class="sxs-lookup"><span data-stu-id="9285b-191">Replace "Application-ID" with Application (client) ID (without quotes) of the application you registered in step 3.a.</span></span> <span data-ttu-id="9285b-192">請注意，PowerShell 輸出中的 ID 物件的值。</span><span class="sxs-lookup"><span data-stu-id="9285b-192">Note the value of ID object from PowerShell output.</span></span> <span data-ttu-id="9285b-193">這是服務主體識別碼。</span><span class="sxs-lookup"><span data-stu-id="9285b-193">It's the Service Principal ID.</span></span>

<span data-ttu-id="9285b-194">現在，您已具備 Azure 入口網站所需的所有資訊。</span><span class="sxs-lookup"><span data-stu-id="9285b-194">Now you have all the information required from Azure portal.</span></span> <span data-ttu-id="9285b-195">下表提供資訊的快速摘要。</span><span class="sxs-lookup"><span data-stu-id="9285b-195">A quick summary of the information is given in the table below.</span></span>

<span data-ttu-id="9285b-196">屬性	</span><span class="sxs-lookup"><span data-stu-id="9285b-196">Property</span></span> | <span data-ttu-id="9285b-197">描述</span><span class="sxs-lookup"><span data-stu-id="9285b-197">Description</span></span> 
--- | ---
<span data-ttu-id="9285b-198">目錄識別碼 (租使用者識別碼) </span><span class="sxs-lookup"><span data-stu-id="9285b-198">Directory ID (Tenant ID)</span></span> | <span data-ttu-id="9285b-199">步驟 3 Azure Active Directory 租使用者的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="9285b-199">Unique ID of the Azure Active Directory tenant, from step 3.a.</span></span>
<span data-ttu-id="9285b-200"> (用戶端識別碼的應用程式識別碼) </span><span class="sxs-lookup"><span data-stu-id="9285b-200">Application ID (Client ID)</span></span> | <span data-ttu-id="9285b-201">在步驟3中註冊之應用程式的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="9285b-201">Unique ID of the application registered in step 3.a.</span></span>
<span data-ttu-id="9285b-202">用戶端密碼</span><span class="sxs-lookup"><span data-stu-id="9285b-202">Client Secret</span></span> | <span data-ttu-id="9285b-203">從步驟 3 () 的應用程式的機密機碼。</span><span class="sxs-lookup"><span data-stu-id="9285b-203">The secret key of the application (from step 3.b).</span></span> <span data-ttu-id="9285b-204">請將它當作密碼對待。</span><span class="sxs-lookup"><span data-stu-id="9285b-204">Treat it like a password.</span></span>
<span data-ttu-id="9285b-205">服務主體識別碼</span><span class="sxs-lookup"><span data-stu-id="9285b-205">Service Principal ID</span></span> | <span data-ttu-id="9285b-206">作為服務執行之應用程式的身分識別。</span><span class="sxs-lookup"><span data-stu-id="9285b-206">An identity for the application running as a service.</span></span> <span data-ttu-id="9285b-207">步驟 3 () </span><span class="sxs-lookup"><span data-stu-id="9285b-207">(from step 3.c)</span></span>

## <a name="step-3d-register-servicenow-application"></a><span data-ttu-id="9285b-208">步驟 3 ..：註冊 ServiceNow 應用程式</span><span class="sxs-lookup"><span data-stu-id="9285b-208">Step 3.d: Register ServiceNow Application</span></span>

<span data-ttu-id="9285b-209">ServiceNow 實例需要下列設定：</span><span class="sxs-lookup"><span data-stu-id="9285b-209">The ServiceNow instance needs the following configuration:</span></span>

1. <span data-ttu-id="9285b-210">註冊新的 OAuth OIDC 實體。</span><span class="sxs-lookup"><span data-stu-id="9285b-210">Register a new OAuth OIDC entity.</span></span> <span data-ttu-id="9285b-211">若要瞭解，請參閱 [Create a OAUTH OIDC provider](https://docs.servicenow.com/bundle/orlando-platform-administration/page/administer/security/task/add-OIDC-entity.html)。</span><span class="sxs-lookup"><span data-stu-id="9285b-211">To learn, see [Create an OAuth OIDC provider](https://docs.servicenow.com/bundle/orlando-platform-administration/page/administer/security/task/add-OIDC-entity.html).</span></span>

2. <span data-ttu-id="9285b-212">下表提供如何填寫 OIDC 提供者註冊表單的指導方針。</span><span class="sxs-lookup"><span data-stu-id="9285b-212">The following table provides guidance on how to fill out OIDC provider registration form</span></span>

   <span data-ttu-id="9285b-213">欄位</span><span class="sxs-lookup"><span data-stu-id="9285b-213">Field</span></span> | <span data-ttu-id="9285b-214">描述</span><span class="sxs-lookup"><span data-stu-id="9285b-214">Description</span></span> | <span data-ttu-id="9285b-215">建議值</span><span class="sxs-lookup"><span data-stu-id="9285b-215">Recommended Value</span></span>
   --- | --- | ---
   <span data-ttu-id="9285b-216">名稱</span><span class="sxs-lookup"><span data-stu-id="9285b-216">Name</span></span> | <span data-ttu-id="9285b-217">識別 OAuth OIDC 實體的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="9285b-217">A unique name that identifies the OAuth OIDC entity.</span></span> | <span data-ttu-id="9285b-218">Azure AD</span><span class="sxs-lookup"><span data-stu-id="9285b-218">Azure AD</span></span>
   <span data-ttu-id="9285b-219">用戶端識別碼</span><span class="sxs-lookup"><span data-stu-id="9285b-219">Client ID</span></span> | <span data-ttu-id="9285b-220">在協力廠商 OAuth OIDC server 中註冊之應用程式的用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="9285b-220">The client ID of the application registered in the third-party OAuth OIDC server.</span></span> <span data-ttu-id="9285b-221">實例在要求存取權杖時使用用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="9285b-221">The instance uses the client ID when requesting an access token.</span></span> | <span data-ttu-id="9285b-222">Application (Client) ID 從步驟3。</span><span class="sxs-lookup"><span data-stu-id="9285b-222">Application (Client) ID from step 3.a</span></span>
   <span data-ttu-id="9285b-223">用戶端密碼</span><span class="sxs-lookup"><span data-stu-id="9285b-223">Client Secret</span></span> | <span data-ttu-id="9285b-224">在協力廠商 OAuth OIDC server 中註冊之應用程式的用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="9285b-224">The client secret of the application registered in the third-party OAuth OIDC server.</span></span> | <span data-ttu-id="9285b-225">步驟3的用戶端密碼。 b</span><span class="sxs-lookup"><span data-stu-id="9285b-225">Client Secret from step 3.b</span></span>

   <span data-ttu-id="9285b-226">其他所有值都可以是預設值。</span><span class="sxs-lookup"><span data-stu-id="9285b-226">All other values can be default.</span></span>

3. <span data-ttu-id="9285b-227">在 OIDC 提供者註冊表單中，您必須新增新的 OIDC 提供者設定。</span><span class="sxs-lookup"><span data-stu-id="9285b-227">In the OIDC provider registration form, you need to add a new OIDC provider configuration.</span></span> <span data-ttu-id="9285b-228">根據 *OAUTH OIDC 提供者* 設定] 欄位，選取要開啟 OIDC 設定記錄的搜尋圖示。</span><span class="sxs-lookup"><span data-stu-id="9285b-228">Select the search icon against *OAuth OIDC Provider Configuration* field to open the records of OIDC configurations.</span></span> <span data-ttu-id="9285b-229">選取 [新增]。</span><span class="sxs-lookup"><span data-stu-id="9285b-229">Select New.</span></span>

4. <span data-ttu-id="9285b-230">下表提供如何填寫 OIDC 提供者設定表單的指導方針</span><span class="sxs-lookup"><span data-stu-id="9285b-230">The following table provides guidance on how to fill out OIDC provider configuration form</span></span>

   <span data-ttu-id="9285b-231">欄位</span><span class="sxs-lookup"><span data-stu-id="9285b-231">Field</span></span> | <span data-ttu-id="9285b-232">建議值</span><span class="sxs-lookup"><span data-stu-id="9285b-232">Recommended Value</span></span>
   --- | ---
   <span data-ttu-id="9285b-233">OIDC 提供者</span><span class="sxs-lookup"><span data-stu-id="9285b-233">OIDC Provider</span></span> |  <span data-ttu-id="9285b-234">Azure AD</span><span class="sxs-lookup"><span data-stu-id="9285b-234">Azure AD</span></span>
   <span data-ttu-id="9285b-235">OIDC 中繼資料 URL</span><span class="sxs-lookup"><span data-stu-id="9285b-235">OIDC Metadata URL</span></span> | <span data-ttu-id="9285b-236">URL 的格式必須為 HTTPs \: //login.microsoftonline.com/<tenandId ">/.well-known/openid-configuration</span><span class="sxs-lookup"><span data-stu-id="9285b-236">The URL must be in the form https\://login.microsoftonline.com/<tenandId">/.well-known/openid-configuration</span></span> <br/><span data-ttu-id="9285b-237">以步驟3的目錄 (租使用者) 識別碼取代 "tenantID"。</span><span class="sxs-lookup"><span data-stu-id="9285b-237">Replace "tenantID" with Directory (tenant) ID from step 3.a.</span></span>
   <span data-ttu-id="9285b-238">OIDC 設定快取壽命範圍</span><span class="sxs-lookup"><span data-stu-id="9285b-238">OIDC Configuration Cache Life Span</span></span> |  <span data-ttu-id="9285b-239">120</span><span class="sxs-lookup"><span data-stu-id="9285b-239">120</span></span>
   <span data-ttu-id="9285b-240">應用程式</span><span class="sxs-lookup"><span data-stu-id="9285b-240">Application</span></span> | <span data-ttu-id="9285b-241">全域</span><span class="sxs-lookup"><span data-stu-id="9285b-241">Global</span></span>
   <span data-ttu-id="9285b-242">使用者宣告</span><span class="sxs-lookup"><span data-stu-id="9285b-242">User Claim</span></span> | <span data-ttu-id="9285b-243">子</span><span class="sxs-lookup"><span data-stu-id="9285b-243">sub</span></span>
   <span data-ttu-id="9285b-244">使用者欄位</span><span class="sxs-lookup"><span data-stu-id="9285b-244">User Field</span></span> | <span data-ttu-id="9285b-245">使用者識別碼</span><span class="sxs-lookup"><span data-stu-id="9285b-245">User ID</span></span>
   <span data-ttu-id="9285b-246">啟用 JTI 宣告驗證</span><span class="sxs-lookup"><span data-stu-id="9285b-246">Enable JTI claim verification</span></span> | <span data-ttu-id="9285b-247">已停用</span><span class="sxs-lookup"><span data-stu-id="9285b-247">Disabled</span></span>

5. <span data-ttu-id="9285b-248">選取 [提交並更新 OAuth OIDC 實體表單]。</span><span class="sxs-lookup"><span data-stu-id="9285b-248">Select Submit and Update the OAuth OIDC Entity form.</span></span>

## <a name="step-3e-create-a-servicenow-account"></a><span data-ttu-id="9285b-249">步驟 3 .. e：建立 ServiceNow 帳戶</span><span class="sxs-lookup"><span data-stu-id="9285b-249">Step 3.e: Create a ServiceNow account</span></span>

<span data-ttu-id="9285b-250">請參閱指示建立 ServiceNow 帳戶、 [在 ServiceNow 中建立使用者](https://docs.servicenow.com/bundle/paris-platform-administration/page/administer/users-and-groups/task/t_CreateAUser.html)。</span><span class="sxs-lookup"><span data-stu-id="9285b-250">Refer the instructions to create a ServiceNow account, [create a user in ServiceNow](https://docs.servicenow.com/bundle/paris-platform-administration/page/administer/users-and-groups/task/t_CreateAUser.html).</span></span>

<span data-ttu-id="9285b-251">下表提供如何填寫 ServiceNow 使用者帳戶註冊的指導方針。</span><span class="sxs-lookup"><span data-stu-id="9285b-251">The following table provides guidance on how to fill out the ServiceNow user account registration</span></span>

<span data-ttu-id="9285b-252">欄位</span><span class="sxs-lookup"><span data-stu-id="9285b-252">Field</span></span> | <span data-ttu-id="9285b-253">建議值</span><span class="sxs-lookup"><span data-stu-id="9285b-253">Recommended Value</span></span>
--- | ---
<span data-ttu-id="9285b-254">使用者識別碼</span><span class="sxs-lookup"><span data-stu-id="9285b-254">User ID</span></span> | <span data-ttu-id="9285b-255">步驟3中的服務主體識別碼。 c</span><span class="sxs-lookup"><span data-stu-id="9285b-255">Service Principal ID from step 3.c</span></span>
<span data-ttu-id="9285b-256">僅 Web 服務存取權</span><span class="sxs-lookup"><span data-stu-id="9285b-256">Web service access only</span></span> | <span data-ttu-id="9285b-257">Checked</span><span class="sxs-lookup"><span data-stu-id="9285b-257">Checked</span></span>

<span data-ttu-id="9285b-258">其他所有值都可以保留預設值。</span><span class="sxs-lookup"><span data-stu-id="9285b-258">All other values can be left to default.</span></span>

## <a name="step-3f-enable-knowledge-role-for-the-servicenow-account"></a><span data-ttu-id="9285b-259">步驟 3 .. f：啟用 ServiceNow 帳戶的知識角色</span><span class="sxs-lookup"><span data-stu-id="9285b-259">Step 3.f: Enable Knowledge role for the ServiceNow account</span></span>

<span data-ttu-id="9285b-260">存取您用 ServiceNow 主體識別碼建立的 ServiceNow 帳戶做為使用者識別碼，並指派知識角色。</span><span class="sxs-lookup"><span data-stu-id="9285b-260">Access the ServiceNow account you created with ServiceNow Principal ID as User ID, and assign the knowledge role.</span></span> <span data-ttu-id="9285b-261">您可以在以下位置找到將角色指派給 ServiceNow 帳戶的指示： [指派角色給使用者](https://docs.servicenow.com/bundle/paris-platform-administration/page/administer/users-and-groups/task/t_AssignARoleToAUser.html)。</span><span class="sxs-lookup"><span data-stu-id="9285b-261">Instructions to assigning a role to a ServiceNow account can be found here: [assign a role to a user](https://docs.servicenow.com/bundle/paris-platform-administration/page/administer/users-and-groups/task/t_AssignARoleToAUser.html).</span></span>

<span data-ttu-id="9285b-262">使用應用程式識別碼做為用戶端識別碼從步驟3。 a 和用戶端密碼的步驟3，使用 Azure AD OpenID 連線來驗證您的 ServiceNow 實例。</span><span class="sxs-lookup"><span data-stu-id="9285b-262">Use Application ID as Client ID from step 3.a, and Client secret from step 3.b, to authenticate to your ServiceNow instance using Azure AD OpenID Connect.</span></span>

## <a name="step-4-select-properties-and-filter-data"></a><span data-ttu-id="9285b-263">步驟4：選取屬性和篩選資料</span><span class="sxs-lookup"><span data-stu-id="9285b-263">Step 4: Select properties and filter data</span></span>

<span data-ttu-id="9285b-264">在這個步驟中，您可以從 ServiceNow 資料來源新增或移除可用屬性。</span><span class="sxs-lookup"><span data-stu-id="9285b-264">In this step, you can add or remove available properties from your ServiceNow data source.</span></span> <span data-ttu-id="9285b-265">Microsoft 365 已經預設會選取一些屬性。</span><span class="sxs-lookup"><span data-stu-id="9285b-265">Microsoft 365 has already selected few properties by default.</span></span>

<span data-ttu-id="9285b-266">使用 ServiceNow 查詢字串，您可以指定同步處理文章的條件。</span><span class="sxs-lookup"><span data-stu-id="9285b-266">With a ServiceNow query string, you can specify conditions for syncing articles.</span></span> <span data-ttu-id="9285b-267">就像 **SQL Select** 語句中的 **Where** 子句。</span><span class="sxs-lookup"><span data-stu-id="9285b-267">It's like a **Where** clause in a **SQL Select** statement.</span></span> <span data-ttu-id="9285b-268">例如，您可以選擇只為發佈和使用中的文章編制索引。</span><span class="sxs-lookup"><span data-stu-id="9285b-268">For example, you can choose to index only articles that are published and active.</span></span> <span data-ttu-id="9285b-269">若要瞭解如何建立您自己的查詢字串，請參閱 [使用篩選產生編碼的查詢字串](https://docs.servicenow.com/bundle/paris-platform-user-interface/page/use/using-lists/task/t_GenEncodQueryStringFilter.html)。</span><span class="sxs-lookup"><span data-stu-id="9285b-269">To learn about creating your own query string, see [Generate an encoded query string using a filter](https://docs.servicenow.com/bundle/paris-platform-user-interface/page/use/using-lists/task/t_GenEncodQueryStringFilter.html).</span></span>

<span data-ttu-id="9285b-270">使用 [預覽結果] 按鈕，檢查所選屬性和查詢篩選器的範例值。</span><span class="sxs-lookup"><span data-stu-id="9285b-270">Use the preview results button to verify the sample values of the selected properties and query filter.</span></span>

## <a name="step-5-manage-search-permissions"></a><span data-ttu-id="9285b-271">步驟5：管理搜尋許可權</span><span class="sxs-lookup"><span data-stu-id="9285b-271">Step 5: Manage search permissions</span></span>

<span data-ttu-id="9285b-272">ServiceNow 連接器支援 **所有人都** 可以看到的搜尋許可權，或是 **只有存取此資料來源的人員才能使用**。</span><span class="sxs-lookup"><span data-stu-id="9285b-272">The ServiceNow connector supports search permissions visible to **Everyone** or **Only people with access to this data source**.</span></span> <span data-ttu-id="9285b-273">已編制索引的資料會顯示在搜尋結果中，並可供組織中的使用者在其上分別存取。</span><span class="sxs-lookup"><span data-stu-id="9285b-273">Indexed data appears in the search results and is visible to users in the organization who have access to them respectively.</span></span> <span data-ttu-id="9285b-274">ServiceNow 連接器支援不含高級腳本的預設使用者準則許可權。</span><span class="sxs-lookup"><span data-stu-id="9285b-274">ServiceNow Connector supports default user criteria permissions without advanced scripts.</span></span> <span data-ttu-id="9285b-275">當連接器找到具有 advanced script 的使用者準則時，搜尋結果中將不會顯示使用該使用者準則的所有資料。</span><span class="sxs-lookup"><span data-stu-id="9285b-275">When the connector finds a user criteria with advanced script, all data using that user criteria won't be shown in search results.</span></span>

<span data-ttu-id="9285b-276">如果您只選取可 **存取此資料來源的人員**，您需要進一步選擇是否 ServiceNow 實例具有 Azure Active Directory (AAD) 布建使用者或非 AAD 使用者。</span><span class="sxs-lookup"><span data-stu-id="9285b-276">If you select **Only people with access to this data source**, you need to further choose whether your ServiceNow instance has Azure Active Directory (AAD) provisioned users or Non-AAD users.</span></span>

>[!NOTE]
><span data-ttu-id="9285b-277">如果您只選擇可 **存取此資料來源的人員**，則會在 **預覽** ServiceNow 連接器。</span><span class="sxs-lookup"><span data-stu-id="9285b-277">The ServiceNow connector is in **preview** if you choose **Only people with access to this data source**.</span></span>

>[!NOTE]
><span data-ttu-id="9285b-278">如果您選擇 [AAD] 做為身分識別來源的類型，請確定您在 ServiceNow 中為電子郵件目標屬性指派 UPN 來源屬性。</span><span class="sxs-lookup"><span data-stu-id="9285b-278">If you choose AAD as the type of identity source, make sure you are assigning UPN source property to email targeted property in ServiceNow.</span></span> <span data-ttu-id="9285b-279">若要驗證或變更您的對應，請參閱[自訂使用者布建屬性-Azure Active Directory 中 SaaS 應用程式的對應](/azure/active-directory/app-provisioning/customize-application-attributes)。</span><span class="sxs-lookup"><span data-stu-id="9285b-279">To verify or change your mappings, see [Customizing user provisioning attribute-mappings for SaaS applications in Azure Active Directory](/azure/active-directory/app-provisioning/customize-application-attributes).</span></span>

<span data-ttu-id="9285b-280">如果您選擇從 ServiceNow 實例中攝取 ACL，並為身分識別類型選取 "非 AAD"，請參閱 [Map 您的非 AZURE AD](map-non-aad.md) 身分識別，以取得對應身分識別的指示。</span><span class="sxs-lookup"><span data-stu-id="9285b-280">If you chose to ingest an ACL from your ServiceNow instance and selected "non-AAD" for the identity type, see [Map your non-Azure AD Identities](map-non-aad.md) for instructions on mapping the identities.</span></span>

### <a name="managing-search-permissions-in-microsoft-search"></a><span data-ttu-id="9285b-281">在 Microsoft 搜尋中管理搜尋許可權</span><span class="sxs-lookup"><span data-stu-id="9285b-281">Managing Search Permissions in Microsoft Search</span></span>

<span data-ttu-id="9285b-282">在下列影片中，您可以瞭解如何使用 Servicenow 連接器來編制知識庫文章、定義使用者準則的許可權，並無縫同步處理 ServiceNow 和 Microsoft 搜尋索引之間的變更。</span><span class="sxs-lookup"><span data-stu-id="9285b-282">In the following video you can see how to use the Servicenow connector to index knowledge articles, define user criteria permissions, and seamlessly synchronize the changes between ServiceNow and Microsoft Search index.</span></span>

> [!VIDEO https://www.youtube-nocookie.com/embed/TVSkJpk1RiE]

## <a name="step-6-assign-property-labels"></a><span data-ttu-id="9285b-283">步驟6：指派屬性標籤</span><span class="sxs-lookup"><span data-stu-id="9285b-283">Step 6: Assign property labels</span></span>

<span data-ttu-id="9285b-284">遵循一般 [設定指示](./configure-connector.md)。</span><span class="sxs-lookup"><span data-stu-id="9285b-284">Follow the general [setup instructions](./configure-connector.md).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-7-manage-schema"></a><span data-ttu-id="9285b-285">步驟7：管理架構</span><span class="sxs-lookup"><span data-stu-id="9285b-285">Step 7: Manage schema</span></span>

<span data-ttu-id="9285b-286">遵循一般 [設定指示](./configure-connector.md)。</span><span class="sxs-lookup"><span data-stu-id="9285b-286">Follow the general [setup instructions](./configure-connector.md).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-8-choose-refresh-settings"></a><span data-ttu-id="9285b-287">步驟8：選擇重新整理設定</span><span class="sxs-lookup"><span data-stu-id="9285b-287">Step 8: Choose refresh settings</span></span>

<span data-ttu-id="9285b-288">遵循一般 [設定指示](./configure-connector.md)。</span><span class="sxs-lookup"><span data-stu-id="9285b-288">Follow the general [setup instructions](./configure-connector.md).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

>[!NOTE]
><span data-ttu-id="9285b-289">針對身分識別，只會套用已排程的完整編目。</span><span class="sxs-lookup"><span data-stu-id="9285b-289">For identities, only full crawl scheduled will be applied.</span></span>

## <a name="step-9-review-connection"></a><span data-ttu-id="9285b-290">步驟9：檢查連線</span><span class="sxs-lookup"><span data-stu-id="9285b-290">Step 9: Review Connection</span></span>

<span data-ttu-id="9285b-291">遵循一般 [設定指示](./configure-connector.md)。</span><span class="sxs-lookup"><span data-stu-id="9285b-291">Follow the general [setup instructions](./configure-connector.md).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="troubleshooting"></a><span data-ttu-id="9285b-292">疑難排解</span><span class="sxs-lookup"><span data-stu-id="9285b-292">Troubleshooting</span></span>

<span data-ttu-id="9285b-293">在發佈連線後，自訂 [結果] 頁面，您可以在系統 [管理中心](https://admin.microsoft.com)的 [**連接器**] 索引標籤底下查看狀態。</span><span class="sxs-lookup"><span data-stu-id="9285b-293">After publishing your connection, customizing the results page, you can review the status under the **Connectors** tab in the [admin center](https://admin.microsoft.com).</span></span> <span data-ttu-id="9285b-294">若要瞭解如何進行更新和刪除，請參閱 [管理您的連接器](manage-connector.md)。</span><span class="sxs-lookup"><span data-stu-id="9285b-294">To learn how to make updates and deletions, see [Manage your connector](manage-connector.md).</span></span>

## <a name="limitations"></a><span data-ttu-id="9285b-295">限制</span><span class="sxs-lookup"><span data-stu-id="9285b-295">Limitations</span></span>

<span data-ttu-id="9285b-296">ServiceNow Graph 連接器在其最新版本中有下列限制：</span><span class="sxs-lookup"><span data-stu-id="9285b-296">ServiceNow Graph connector has the following limitations in its latest release:</span></span>

- <span data-ttu-id="9285b-297">組織中的每個人都可以使用的索引知識文章是一項普遍可用的功能。</span><span class="sxs-lookup"><span data-stu-id="9285b-297">Indexing knowledge articles available to everyone in an organization is a generally available feature.</span></span>
- <span data-ttu-id="9285b-298">*只有存取此資料來源功能的使用者* 才會在 [管理搜尋許可權] 步驟中使用預覽，而且只會處理 [使用者準則](https://hi.service-now.com/kb_view.do?sysparm_article=KB0550924) 許可權。</span><span class="sxs-lookup"><span data-stu-id="9285b-298">*Only people with access to this data source* feature under Manage Search permissions step is in preview and processes only [user criteria](https://hi.service-now.com/kb_view.do?sysparm_article=KB0550924) permissions.</span></span> <span data-ttu-id="9285b-299">任何其他類型的存取權限都不會套用到搜尋結果中。</span><span class="sxs-lookup"><span data-stu-id="9285b-299">Any other type of access permissions won't be applied in the search results.</span></span>
- <span data-ttu-id="9285b-300">目前的預覽版本不支援具有高級腳本的使用者準則。</span><span class="sxs-lookup"><span data-stu-id="9285b-300">User criteria with advanced scripts aren't supported in the current preview version.</span></span> <span data-ttu-id="9285b-301">具有存取限制的知識文章會以「拒絕所有人」存取的方式編制索引，而且不會顯示在搜尋結果中，直到我們支援它們為止。</span><span class="sxs-lookup"><span data-stu-id="9285b-301">Knowledge articles with an access restriction will be indexed with deny everyone access, and won't appear in search results to any user until we support them.</span></span>