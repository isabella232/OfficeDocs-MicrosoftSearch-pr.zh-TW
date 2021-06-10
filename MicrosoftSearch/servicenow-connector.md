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
ms.openlocfilehash: 0b7e752ec67a7c14e4afc2e3bad32124694f8f39
ms.sourcegitcommit: 668930032e77a065c23551b3e8820dcc2c63c0f8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/09/2021
ms.locfileid: "52853812"
---
<!---Previous ms.author: kam1 --->


# <a name="servicenow-graph-connector"></a><span data-ttu-id="ad0b1-103">ServiceNow Graph 連接器</span><span class="sxs-lookup"><span data-stu-id="ad0b1-103">ServiceNow Graph Connector</span></span>

<span data-ttu-id="ad0b1-104">透過使用 Microsoft Graph Connector ServiceNow，您的組織可以為您組織內的使用者準則許可權，編制對所有使用者可見或限制的知識庫文章的索引。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-104">With the Microsoft Graph Connector for ServiceNow, your organization can index knowledge-base articles that are visible to all users or restricted with user criteria permissions within your organization.</span></span> <span data-ttu-id="ad0b1-105">從 ServiceNow 設定連接器和索引內容之後，使用者可以從任何 Microsoft 搜尋用戶端搜尋這些文章。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-105">After you configure the connector and index content from ServiceNow, end users can search for those articles from any Microsoft Search client.</span></span>  

<span data-ttu-id="ad0b1-106">本文適用于 Microsoft 365 系統管理員或任何設定、執行及監視 ServiceNow Graph 連接器的人員。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-106">This article is for Microsoft 365 administrators or anyone who configures, runs, and monitors a ServiceNow Graph  connector.</span></span> <span data-ttu-id="ad0b1-107">它會補充[設定 Graph 連接器](configure-connector.md)文章中提供的一般指示。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-107">It supplements the general instructions provided in the [Set up your Graph connector](configure-connector.md) article.</span></span> <span data-ttu-id="ad0b1-108">若尚未這麼做，請閱讀整個設定 Graph 連接器文章，以瞭解一般的設定程式。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-108">If you have not already done so, read the entire Set up your Graph Connector article to understand the general setup process.</span></span>

<span data-ttu-id="ad0b1-109">安裝程式中的每個步驟都會列在下面，也就是指出應該遵循一般設定指示或僅適用于 ServiceNow Graph 連接器（包括[疑難排解](#troubleshooting)及[限制](#limitations)的相關資訊）的說明。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-109">Each step in the setup process is listed below along with either a note that indicates you should follow the general setup instructions OR other instructions that apply to only ServiceNow Graph connector including information about [Troubleshooting](#troubleshooting) and [Limitations](#limitations).</span></span>  

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a><span data-ttu-id="ad0b1-110">步驟1：在 Microsoft 365 系統管理中心新增 Graph 連接器。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-110">Step 1: Add a Graph connector in the Microsoft 365 admin center.</span></span>
<span data-ttu-id="ad0b1-111">遵循一般設定指示。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-111">Follow the general setup instructions.</span></span>

## <a name="step-2-name-the-connection"></a><span data-ttu-id="ad0b1-112">步驟2：命名連線。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-112">Step 2: Name the connection.</span></span>
<span data-ttu-id="ad0b1-113">遵循一般設定指示。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-113">Follow the general setup instructions.</span></span>


## <a name="step-3-connection-settings"></a><span data-ttu-id="ad0b1-114">步驟3：連接設定</span><span class="sxs-lookup"><span data-stu-id="ad0b1-114">Step 3: Connection Settings</span></span>
<span data-ttu-id="ad0b1-115">若要連線至您的 ServiceNow 資料，您需要組織的 **ServiceNow 實例 URL**。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-115">To connect to your ServiceNow data, you need your organization's **ServiceNow instance URL**.</span></span> <span data-ttu-id="ad0b1-116">組織的 ServiceNow 實例 URL 一般會類似 **HTTPs:// &lt; 您的組織網域> service-now.com**。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-116">Your organization’s ServiceNow instance URL typically looks like **https://&lt;your-organization-domain>.service-now.com**.</span></span> 

<span data-ttu-id="ad0b1-117">除了此 URL 之外，您還需要一種 **服務帳戶** ，用以設定 ServiceNow 的連線，以及允許 Microsoft 搜尋定期更新以重新整理排程為基礎的知識文章。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-117">Along with this URL, you will need a **service account** for setting up the connection to ServiceNow as well as for allowing Microsoft Search to periodically update the knowledge articles based on the refresh schedule.</span></span> <span data-ttu-id="ad0b1-118">服務帳戶必須具有下列 **ServiceNow 表記錄** 的讀取權限，才可成功編目各種實體。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-118">The service account will need read access to the following **ServiceNow table records** to successfully crawl various entities.</span></span>

<span data-ttu-id="ad0b1-119">**功能**</span><span class="sxs-lookup"><span data-stu-id="ad0b1-119">**Feature**</span></span> | <span data-ttu-id="ad0b1-120">**讀取 access 所需的表格**</span><span class="sxs-lookup"><span data-stu-id="ad0b1-120">**Read access required tables**</span></span> | <span data-ttu-id="ad0b1-121">**描述**</span><span class="sxs-lookup"><span data-stu-id="ad0b1-121">**Description**</span></span>
--- | --- | ---
<span data-ttu-id="ad0b1-122">可供<em>所有人</em>使用的索引知識文章</span><span class="sxs-lookup"><span data-stu-id="ad0b1-122">Index knowledge articles available to <em>Everyone</em></span></span> | <span data-ttu-id="ad0b1-123">kb_knowledge</span><span class="sxs-lookup"><span data-stu-id="ad0b1-123">kb_knowledge</span></span> | <span data-ttu-id="ad0b1-124">編目知識文章</span><span class="sxs-lookup"><span data-stu-id="ad0b1-124">For crawling knowledge articles</span></span>
<span data-ttu-id="ad0b1-125">索引及支援使用者準則許可權</span><span class="sxs-lookup"><span data-stu-id="ad0b1-125">Index and support user criteria permissions</span></span> | <span data-ttu-id="ad0b1-126">kb_uc_can_read_mtom</span><span class="sxs-lookup"><span data-stu-id="ad0b1-126">kb_uc_can_read_mtom</span></span> | <span data-ttu-id="ad0b1-127">神秘可以讀取此知識庫</span><span class="sxs-lookup"><span data-stu-id="ad0b1-127">Who can read this knowledge base</span></span>
| | <span data-ttu-id="ad0b1-128">kb_uc_can_contribute_mtom</span><span class="sxs-lookup"><span data-stu-id="ad0b1-128">kb_uc_can_contribute_mtom</span></span> | <span data-ttu-id="ad0b1-129">神秘可對此知識庫做貢獻</span><span class="sxs-lookup"><span data-stu-id="ad0b1-129">Who can contribute to this knowledge base</span></span>
| | <span data-ttu-id="ad0b1-130">kb_uc_cannot_read_mtom</span><span class="sxs-lookup"><span data-stu-id="ad0b1-130">kb_uc_cannot_read_mtom</span></span> | <span data-ttu-id="ad0b1-131">神秘無法讀取此知識庫</span><span class="sxs-lookup"><span data-stu-id="ad0b1-131">Who cannot read this knowledge base</span></span>
| | <span data-ttu-id="ad0b1-132">kb_uc_cannot_contribute_mtom</span><span class="sxs-lookup"><span data-stu-id="ad0b1-132">kb_uc_cannot_contribute_mtom</span></span> | <span data-ttu-id="ad0b1-133">神秘無法參與此知識庫</span><span class="sxs-lookup"><span data-stu-id="ad0b1-133">Who cannot contribute to this knowledge base</span></span>
| | <span data-ttu-id="ad0b1-134">sys_user</span><span class="sxs-lookup"><span data-stu-id="ad0b1-134">sys_user</span></span> | <span data-ttu-id="ad0b1-135">讀取使用者表格</span><span class="sxs-lookup"><span data-stu-id="ad0b1-135">Read user table</span></span>
| | <span data-ttu-id="ad0b1-136">sys_user_has_role</span><span class="sxs-lookup"><span data-stu-id="ad0b1-136">sys_user_has_role</span></span> | <span data-ttu-id="ad0b1-137">讀取使用者的角色資訊</span><span class="sxs-lookup"><span data-stu-id="ad0b1-137">Read role information of users</span></span>
| | <span data-ttu-id="ad0b1-138">sys_user_grmember</span><span class="sxs-lookup"><span data-stu-id="ad0b1-138">sys_user_grmember</span></span> | <span data-ttu-id="ad0b1-139">使用者的讀取群組成員資格</span><span class="sxs-lookup"><span data-stu-id="ad0b1-139">Read group membership of users</span></span>
| | <span data-ttu-id="ad0b1-140">user_criteria</span><span class="sxs-lookup"><span data-stu-id="ad0b1-140">user_criteria</span></span> | <span data-ttu-id="ad0b1-141">讀取使用者準則許可權</span><span class="sxs-lookup"><span data-stu-id="ad0b1-141">Read user criteria permissions</span></span>
| | <span data-ttu-id="ad0b1-142">kb_knowledge_base</span><span class="sxs-lookup"><span data-stu-id="ad0b1-142">kb_knowledge_base</span></span> | <span data-ttu-id="ad0b1-143">閱讀知識文庫資訊</span><span class="sxs-lookup"><span data-stu-id="ad0b1-143">Read knowledge base information</span></span>

<span data-ttu-id="ad0b1-144">您可以為您用來連線 Microsoft 搜尋的服務帳戶 **建立和指派角色** 。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-144">You can **create and assign a role** for the service account you use to connect with Microsoft Search.</span></span> <span data-ttu-id="ad0b1-145">[瞭解如何指派 ServiceNow 帳戶的角色](https://docs.servicenow.com/bundle/paris-platform-administration/page/administer/users-and-groups/task/t_AssignARoleToAUser.html)。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-145">[Learn how to assign role for ServiceNow accounts](https://docs.servicenow.com/bundle/paris-platform-administration/page/administer/users-and-groups/task/t_AssignARoleToAUser.html).</span></span> <span data-ttu-id="ad0b1-146">您可以在建立的角色上指派對表格的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-146">Read access to the tables can be assigned on the created role.</span></span> <span data-ttu-id="ad0b1-147">若要瞭解如何設定表記錄的「讀取」存取權，請參閱 [保護資料表記錄](https://developer.servicenow.com/dev.do#!/learn/learning-plans/orlando/new_to_servicenow/app_store_learnv2_securingapps_orlando_creating_and_editing_access_controls)。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-147">To learn about setting read access to table records, see [Securing Table Records](https://developer.servicenow.com/dev.do#!/learn/learning-plans/orlando/new_to_servicenow/app_store_learnv2_securingapps_orlando_creating_and_editing_access_controls).</span></span> 


>[!NOTE]
> <span data-ttu-id="ad0b1-148">ServiceNow Graph 連接器可以索引不含高級腳本的知識文章和使用者準則許可權。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-148">ServiceNow Graph Connector can index knowledge articles and user criteria permissions without advanced scripts.</span></span> <span data-ttu-id="ad0b1-149">如果使用者準則包含 advanced script，所有相關的知識文章都會從搜尋結果中隱藏。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-149">If a user criteria contains advanced script all the related knowledge articles will be hidden from search results.</span></span>

<span data-ttu-id="ad0b1-150">若要驗證及同步處理 ServiceNow 中的內容，請選擇下列 **其中一** 項支援的方法：</span><span class="sxs-lookup"><span data-stu-id="ad0b1-150">To authenticate and sync content from ServiceNow, choose **one of three** supported methods:</span></span> 
 
1. <span data-ttu-id="ad0b1-151">基本驗證</span><span class="sxs-lookup"><span data-stu-id="ad0b1-151">Basic authentication</span></span> 
1. <span data-ttu-id="ad0b1-152">ServiceNow OAuth (建議) </span><span class="sxs-lookup"><span data-stu-id="ad0b1-152">ServiceNow OAuth (recommended)</span></span>
1. <span data-ttu-id="ad0b1-153">Azure AD OpenID 連線</span><span class="sxs-lookup"><span data-stu-id="ad0b1-153">Azure AD OpenID Connect</span></span>

### <a name="basic-authentication"></a><span data-ttu-id="ad0b1-154">基本驗證</span><span class="sxs-lookup"><span data-stu-id="ad0b1-154">Basic authentication</span></span>

<span data-ttu-id="ad0b1-155">輸入具有 **知識** 角色的 ServiceNow 帳戶的使用者名稱和密碼，以向您的實例驗證。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-155">Enter the username and password of ServiceNow account with **knowledge** role to authenticate to your instance.</span></span>

### <a name="servicenow-oauth"></a><span data-ttu-id="ad0b1-156">ServiceNow OAuth</span><span class="sxs-lookup"><span data-stu-id="ad0b1-156">ServiceNow OAuth</span></span>

<span data-ttu-id="ad0b1-157">若要使用 ServiceNow OAuth 進行驗證，ServiceNow 系統管理員必須布建 ServiceNow 實例中的端點，這樣 Microsoft Search 應用程式才能存取它。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-157">To use ServiceNow OAuth for authentication, a ServiceNow admin needs to provision an endpoint in your ServiceNow instance, so that the Microsoft Search app can access it.</span></span> <span data-ttu-id="ad0b1-158">若要深入瞭解，請參閱在 ServiceNow 檔中 [建立用戶端存取實例的端點](https://docs.servicenow.com/bundle/newyork-platform-administration/page/administer/security/task/t_CreateEndpointforExternalClients.html) 。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-158">To learn more, see [Create an endpoint for clients to access the instance](https://docs.servicenow.com/bundle/newyork-platform-administration/page/administer/security/task/t_CreateEndpointforExternalClients.html) in the ServiceNow documentation.</span></span>

<span data-ttu-id="ad0b1-159">下表提供如何填寫端點建立表單的指導方針：</span><span class="sxs-lookup"><span data-stu-id="ad0b1-159">The following table provides guidance on how to fill out the endpoint creation form:</span></span>

<span data-ttu-id="ad0b1-160">欄位</span><span class="sxs-lookup"><span data-stu-id="ad0b1-160">Field</span></span> | <span data-ttu-id="ad0b1-161">描述</span><span class="sxs-lookup"><span data-stu-id="ad0b1-161">Description</span></span> | <span data-ttu-id="ad0b1-162">建議值</span><span class="sxs-lookup"><span data-stu-id="ad0b1-162">Recommended Value</span></span> 
--- | --- | ---
<span data-ttu-id="ad0b1-163">名稱</span><span class="sxs-lookup"><span data-stu-id="ad0b1-163">Name</span></span> | <span data-ttu-id="ad0b1-164">識別您需要 OAuth 存取之應用程式的唯一值。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-164">Unique value that identifies the application that you require OAuth access for.</span></span> | <span data-ttu-id="ad0b1-165">Microsoft 搜尋</span><span class="sxs-lookup"><span data-stu-id="ad0b1-165">Microsoft Search</span></span>
<span data-ttu-id="ad0b1-166">用戶端識別碼</span><span class="sxs-lookup"><span data-stu-id="ad0b1-166">Client ID</span></span> | <span data-ttu-id="ad0b1-167">應用程式的唯讀、自動產生的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-167">A read-only, auto generated unique ID for the application.</span></span> <span data-ttu-id="ad0b1-168">當實例要求存取權杖時，會使用用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-168">The instance uses the client ID when it requests an access token.</span></span> | <span data-ttu-id="ad0b1-169">NA</span><span class="sxs-lookup"><span data-stu-id="ad0b1-169">NA</span></span>
<span data-ttu-id="ad0b1-170">用戶端密碼</span><span class="sxs-lookup"><span data-stu-id="ad0b1-170">Client secret</span></span> | <span data-ttu-id="ad0b1-171">使用此共用的機密字串，ServiceNow 實例和 Microsoft 搜尋會授權彼此間的通訊。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-171">With this shared secret string, the ServiceNow instance and Microsoft Search authorize communications with each other.</span></span> | <span data-ttu-id="ad0b1-172">遵循安全性最佳作法，將密碼當做密碼對待。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-172">Follow security best-practices by treating the secret as a password.</span></span>
<span data-ttu-id="ad0b1-173">重新導向 URL</span><span class="sxs-lookup"><span data-stu-id="ad0b1-173">Redirect URL</span></span> | <span data-ttu-id="ad0b1-174">授權伺服器重新導向所需的回撥 URL。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-174">A required callback URL that the authorization server redirects to.</span></span> | https://gcs.office.com/v1.0/admin/oauth/callback
<span data-ttu-id="ad0b1-175">標誌 URL</span><span class="sxs-lookup"><span data-stu-id="ad0b1-175">Logo URL</span></span> | <span data-ttu-id="ad0b1-176">包含應用程式標誌之圖像的 URL。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-176">A URL that contains the image for the application logo.</span></span> | <span data-ttu-id="ad0b1-177">NA</span><span class="sxs-lookup"><span data-stu-id="ad0b1-177">NA</span></span>
<span data-ttu-id="ad0b1-178">作用中</span><span class="sxs-lookup"><span data-stu-id="ad0b1-178">Active</span></span> | <span data-ttu-id="ad0b1-179">選取此核取方塊，讓應用程式登錄成為使用中。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-179">Select the check box to make the application registry active.</span></span> | <span data-ttu-id="ad0b1-180">設定為 active</span><span class="sxs-lookup"><span data-stu-id="ad0b1-180">Set to active</span></span>
<span data-ttu-id="ad0b1-181">重新整理權杖生命週期</span><span class="sxs-lookup"><span data-stu-id="ad0b1-181">Refresh token lifespan</span></span> | <span data-ttu-id="ad0b1-182">重新整理權杖有效的秒數。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-182">The number of seconds that a refresh token is valid.</span></span> <span data-ttu-id="ad0b1-183">根據預設，重新整理權杖會在100天內到期 (8640000 秒) 。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-183">By default, refresh tokens expire in 100 days (8,640,000 seconds).</span></span> | <span data-ttu-id="ad0b1-184">31536000 (1 年) </span><span class="sxs-lookup"><span data-stu-id="ad0b1-184">31,536,000 (1 year)</span></span>
<span data-ttu-id="ad0b1-185">存取權杖使用壽命</span><span class="sxs-lookup"><span data-stu-id="ad0b1-185">Access token lifespan</span></span> | <span data-ttu-id="ad0b1-186">存取權杖有效的秒數。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-186">The number of seconds that an access token is valid.</span></span> | <span data-ttu-id="ad0b1-187">43200 (12 小時) </span><span class="sxs-lookup"><span data-stu-id="ad0b1-187">43,200 (12 hours)</span></span>

<span data-ttu-id="ad0b1-188">輸入用戶端識別碼和用戶端密碼以連接至您的實例。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-188">Enter the client id and client secret to connect to your instance.</span></span> <span data-ttu-id="ad0b1-189">連接後，請使用 ServiceNow 帳號憑證來驗證編目的許可權。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-189">After connecting, use a ServiceNow account credential to authenticate permission to crawl.</span></span> <span data-ttu-id="ad0b1-190">帳戶至少應具備 **知識** 角色。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-190">The account should at least have **knowledge** role.</span></span> <span data-ttu-id="ad0b1-191">請參閱「 [步驟3：連線設定](#step-3-connection-settings) 」的開頭中的表格，以提供更多 ServiceNow 表記錄的讀取權，以及索引使用者準則許可權。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-191">Refer the table in the beginning of [step 3: connection settings](#step-3-connection-settings) for providing read access to more ServiceNow table records and index user criteria permissions.</span></span>

### <a name="azure-ad-openid-connect"></a><span data-ttu-id="ad0b1-192">Azure AD OpenID 連線</span><span class="sxs-lookup"><span data-stu-id="ad0b1-192">Azure AD OpenID Connect</span></span>

<span data-ttu-id="ad0b1-193">若要使用 Azure AD OpenID 連線進行驗證，請遵循下列步驟。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-193">To use Azure AD OpenID Connect for authentication, follow the steps below.</span></span>

## <a name="step-3a-register-a-new-application-in-azure-active-directory"></a><span data-ttu-id="ad0b1-194">步驟3。 a：在 Azure Active Directory 中註冊新的應用程式</span><span class="sxs-lookup"><span data-stu-id="ad0b1-194">Step 3.a: Register a new application in Azure Active Directory</span></span>

<span data-ttu-id="ad0b1-195">若要瞭解如何在 Azure Active Directory 中註冊新的應用程式，請參閱[註冊應用程式](/azure/active-directory/develop/quickstart-register-app#register-an-application)。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-195">To learn about registering a new application in Azure Active Directory, see [Register an application](/azure/active-directory/develop/quickstart-register-app#register-an-application).</span></span> <span data-ttu-id="ad0b1-196">選取 [單一承租人組織目錄]。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-196">Select single tenant organizational directory.</span></span> <span data-ttu-id="ad0b1-197">不需要重新導向 URI。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-197">Redirect URI isn't needed.</span></span> <span data-ttu-id="ad0b1-198">註冊後，請記下應用程式 (用戶端) ID 及目錄 (承租人) 識別碼。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-198">After registration, note down the Application (client) ID and Directory (tenant) ID.</span></span>

## <a name="step-3b-create-a-client-secret"></a><span data-ttu-id="ad0b1-199">步驟3：建立用戶端密碼</span><span class="sxs-lookup"><span data-stu-id="ad0b1-199">Step 3.b: Create a client secret</span></span>

<span data-ttu-id="ad0b1-200">若要瞭解如何建立用戶端密碼，請參閱 [建立用戶端密碼](/azure/active-directory/develop/quickstart-register-app#add-a-client-secret)。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-200">To learn about creating a client secret, see [Creating a client secret](/azure/active-directory/develop/quickstart-register-app#add-a-client-secret).</span></span> <span data-ttu-id="ad0b1-201">記錄用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-201">Take a note of client secret.</span></span>

## <a name="step-3c-retrieve-service-principal-object-identifier"></a><span data-ttu-id="ad0b1-202">步驟 3 .. c：取回服務主體物件識別碼</span><span class="sxs-lookup"><span data-stu-id="ad0b1-202">Step 3.c: Retrieve Service Principal Object Identifier</span></span>

<span data-ttu-id="ad0b1-203">遵循下列步驟以取得服務主體物件識別碼</span><span class="sxs-lookup"><span data-stu-id="ad0b1-203">Follow the steps to retrieve Service Principal Object Identifier</span></span>

1. <span data-ttu-id="ad0b1-204">執行 PowerShell。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-204">Run PowerShell.</span></span>

2. <span data-ttu-id="ad0b1-205">使用下列命令安裝 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-205">Install Azure PowerShell using the following command.</span></span>

   ```powershell
   Install-Module -Name Az -AllowClobber -Scope CurrentUser
   ```

3. <span data-ttu-id="ad0b1-206">連線 Azure。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-206">Connect to Azure.</span></span>

   ```powershell
   Connect-AzAccount
   ```

4. <span data-ttu-id="ad0b1-207">取得服務主體物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-207">Get Service Principal Object Identifier.</span></span>

   ```powershell
   Get-AzADServicePrincipal -ApplicationId "Application-ID"
   ```
   <span data-ttu-id="ad0b1-208">將 "Application ID" 取代為您在步驟3中所註冊應用程式的應用程式 (用戶端) ID (但不) 引號。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-208">Replace "Application-ID" with Application (client) ID (without quotes) of the application you registered in step 3.a.</span></span> <span data-ttu-id="ad0b1-209">請注意，PowerShell 輸出中的 ID 物件的值。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-209">Note the value of ID object from PowerShell output.</span></span> <span data-ttu-id="ad0b1-210">這是服務主體識別碼。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-210">It's the Service Principal ID.</span></span>

<span data-ttu-id="ad0b1-211">現在，您已具備 Azure 入口網站所需的所有資訊。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-211">Now you have all the information required from Azure portal.</span></span> <span data-ttu-id="ad0b1-212">下表提供資訊的快速摘要。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-212">A quick summary of the information is given in the table below.</span></span>

<span data-ttu-id="ad0b1-213">屬性	</span><span class="sxs-lookup"><span data-stu-id="ad0b1-213">Property</span></span> | <span data-ttu-id="ad0b1-214">說明</span><span class="sxs-lookup"><span data-stu-id="ad0b1-214">Description</span></span> 
--- | ---
<span data-ttu-id="ad0b1-215">目錄識別碼 (租使用者識別碼) </span><span class="sxs-lookup"><span data-stu-id="ad0b1-215">Directory ID (Tenant ID)</span></span> | <span data-ttu-id="ad0b1-216">步驟 3 Azure Active Directory 租使用者的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-216">Unique ID of the Azure Active Directory tenant, from step 3.a.</span></span>
<span data-ttu-id="ad0b1-217"> (用戶端識別碼的應用程式識別碼) </span><span class="sxs-lookup"><span data-stu-id="ad0b1-217">Application ID (Client ID)</span></span> | <span data-ttu-id="ad0b1-218">在步驟3中註冊之應用程式的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-218">Unique ID of the application registered in step 3.a.</span></span>
<span data-ttu-id="ad0b1-219">用戶端密碼</span><span class="sxs-lookup"><span data-stu-id="ad0b1-219">Client Secret</span></span> | <span data-ttu-id="ad0b1-220">從步驟 3 () 的應用程式的機密機碼。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-220">The secret key of the application (from step 3.b).</span></span> <span data-ttu-id="ad0b1-221">請將它當作密碼對待。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-221">Treat it like a password.</span></span>
<span data-ttu-id="ad0b1-222">服務主體識別碼</span><span class="sxs-lookup"><span data-stu-id="ad0b1-222">Service Principal ID</span></span> | <span data-ttu-id="ad0b1-223">作為服務執行之應用程式的身分識別。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-223">An identity for the application running as a service.</span></span> <span data-ttu-id="ad0b1-224">步驟 3 () </span><span class="sxs-lookup"><span data-stu-id="ad0b1-224">(from step 3.c)</span></span>

## <a name="step-3d-register-servicenow-application"></a><span data-ttu-id="ad0b1-225">步驟 3 ..：註冊 ServiceNow 應用程式</span><span class="sxs-lookup"><span data-stu-id="ad0b1-225">Step 3.d: Register ServiceNow Application</span></span>

<span data-ttu-id="ad0b1-226">ServiceNow 實例需要下列設定：</span><span class="sxs-lookup"><span data-stu-id="ad0b1-226">The ServiceNow instance needs the following configuration:</span></span>

1. <span data-ttu-id="ad0b1-227">註冊新的 OAuth OIDC 實體。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-227">Register a new OAuth OIDC entity.</span></span> <span data-ttu-id="ad0b1-228">若要瞭解，請參閱 [Create a OAUTH OIDC provider](https://docs.servicenow.com/bundle/orlando-platform-administration/page/administer/security/task/add-OIDC-entity.html)。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-228">To learn, see [Create an OAuth OIDC provider](https://docs.servicenow.com/bundle/orlando-platform-administration/page/administer/security/task/add-OIDC-entity.html).</span></span>

2. <span data-ttu-id="ad0b1-229">下表提供如何填寫 OIDC 提供者註冊表單的指導方針。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-229">The following table provides guidance on how to fill out OIDC provider registration form</span></span>

   <span data-ttu-id="ad0b1-230">欄位</span><span class="sxs-lookup"><span data-stu-id="ad0b1-230">Field</span></span> | <span data-ttu-id="ad0b1-231">描述</span><span class="sxs-lookup"><span data-stu-id="ad0b1-231">Description</span></span> | <span data-ttu-id="ad0b1-232">建議值</span><span class="sxs-lookup"><span data-stu-id="ad0b1-232">Recommended Value</span></span>
   --- | --- | ---
   <span data-ttu-id="ad0b1-233">名稱</span><span class="sxs-lookup"><span data-stu-id="ad0b1-233">Name</span></span> | <span data-ttu-id="ad0b1-234">識別 OAuth OIDC 實體的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-234">A unique name that identifies the OAuth OIDC entity.</span></span> | <span data-ttu-id="ad0b1-235">Azure AD</span><span class="sxs-lookup"><span data-stu-id="ad0b1-235">Azure AD</span></span>
   <span data-ttu-id="ad0b1-236">用戶端識別碼</span><span class="sxs-lookup"><span data-stu-id="ad0b1-236">Client ID</span></span> | <span data-ttu-id="ad0b1-237">在協力廠商 OAuth OIDC server 中註冊之應用程式的用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-237">The client ID of the application registered in the third-party OAuth OIDC server.</span></span> <span data-ttu-id="ad0b1-238">實例在要求存取權杖時使用用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-238">The instance uses the client ID when requesting an access token.</span></span> | <span data-ttu-id="ad0b1-239">Application (Client) ID 從步驟3。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-239">Application (Client) ID from step 3.a</span></span>
   <span data-ttu-id="ad0b1-240">用戶端密碼</span><span class="sxs-lookup"><span data-stu-id="ad0b1-240">Client Secret</span></span> | <span data-ttu-id="ad0b1-241">在協力廠商 OAuth OIDC server 中註冊之應用程式的用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-241">The client secret of the application registered in the third-party OAuth OIDC server.</span></span> | <span data-ttu-id="ad0b1-242">步驟3的用戶端密碼。 b</span><span class="sxs-lookup"><span data-stu-id="ad0b1-242">Client Secret from step 3.b</span></span>

   <span data-ttu-id="ad0b1-243">其他所有值都可以是預設值。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-243">All other values can be default.</span></span>

3. <span data-ttu-id="ad0b1-244">在 OIDC 提供者註冊表單中，您必須新增新的 OIDC 提供者設定。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-244">In the OIDC provider registration form, you need to add a new OIDC provider configuration.</span></span> <span data-ttu-id="ad0b1-245">根據 *OAUTH OIDC 提供者* 設定] 欄位，選取要開啟 OIDC 設定記錄的搜尋圖示。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-245">Select the search icon against *OAuth OIDC Provider Configuration* field to open the records of OIDC configurations.</span></span> <span data-ttu-id="ad0b1-246">選取 [新增]。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-246">Select New.</span></span>

4. <span data-ttu-id="ad0b1-247">下表提供如何填寫 OIDC 提供者設定表單的指導方針</span><span class="sxs-lookup"><span data-stu-id="ad0b1-247">The following table provides guidance on how to fill out OIDC provider configuration form</span></span>

   <span data-ttu-id="ad0b1-248">欄位</span><span class="sxs-lookup"><span data-stu-id="ad0b1-248">Field</span></span> | <span data-ttu-id="ad0b1-249">建議值</span><span class="sxs-lookup"><span data-stu-id="ad0b1-249">Recommended Value</span></span>
   --- | ---
   <span data-ttu-id="ad0b1-250">OIDC 提供者</span><span class="sxs-lookup"><span data-stu-id="ad0b1-250">OIDC Provider</span></span> |  <span data-ttu-id="ad0b1-251">Azure AD</span><span class="sxs-lookup"><span data-stu-id="ad0b1-251">Azure AD</span></span>
   <span data-ttu-id="ad0b1-252">OIDC 中繼資料 URL</span><span class="sxs-lookup"><span data-stu-id="ad0b1-252">OIDC Metadata URL</span></span> | <span data-ttu-id="ad0b1-253">URL 的格式必須為 HTTPs \: //login.microsoftonline.com/<tenandId ">/.well-known/openid-configuration</span><span class="sxs-lookup"><span data-stu-id="ad0b1-253">The URL must be in the form https\://login.microsoftonline.com/<tenandId">/.well-known/openid-configuration</span></span> <br/><span data-ttu-id="ad0b1-254">以步驟3的目錄 (租使用者) 識別碼取代 "tenantID"。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-254">Replace "tenantID" with Directory (tenant) ID from step 3.a.</span></span>
   <span data-ttu-id="ad0b1-255">OIDC 設定快取壽命範圍</span><span class="sxs-lookup"><span data-stu-id="ad0b1-255">OIDC Configuration Cache Life Span</span></span> |  <span data-ttu-id="ad0b1-256">120</span><span class="sxs-lookup"><span data-stu-id="ad0b1-256">120</span></span>
   <span data-ttu-id="ad0b1-257">應用程式</span><span class="sxs-lookup"><span data-stu-id="ad0b1-257">Application</span></span> | <span data-ttu-id="ad0b1-258">全域</span><span class="sxs-lookup"><span data-stu-id="ad0b1-258">Global</span></span>
   <span data-ttu-id="ad0b1-259">使用者宣告</span><span class="sxs-lookup"><span data-stu-id="ad0b1-259">User Claim</span></span> | <span data-ttu-id="ad0b1-260">子</span><span class="sxs-lookup"><span data-stu-id="ad0b1-260">sub</span></span>
   <span data-ttu-id="ad0b1-261">使用者欄位</span><span class="sxs-lookup"><span data-stu-id="ad0b1-261">User Field</span></span> | <span data-ttu-id="ad0b1-262">使用者識別碼</span><span class="sxs-lookup"><span data-stu-id="ad0b1-262">User ID</span></span>
   <span data-ttu-id="ad0b1-263">啟用 JTI 宣告驗證</span><span class="sxs-lookup"><span data-stu-id="ad0b1-263">Enable JTI claim verification</span></span> | <span data-ttu-id="ad0b1-264">停用</span><span class="sxs-lookup"><span data-stu-id="ad0b1-264">Disabled</span></span>

5. <span data-ttu-id="ad0b1-265">選取 [提交並更新 OAuth OIDC 實體表單]。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-265">Select Submit and Update the OAuth OIDC Entity form.</span></span>

## <a name="step-3e-create-a-servicenow-account"></a><span data-ttu-id="ad0b1-266">步驟 3 .. e：建立 ServiceNow 帳戶</span><span class="sxs-lookup"><span data-stu-id="ad0b1-266">Step 3.e: Create a ServiceNow account</span></span>

<span data-ttu-id="ad0b1-267">請參閱指示建立 ServiceNow 帳戶、 [在 ServiceNow 中建立使用者](https://docs.servicenow.com/bundle/paris-platform-administration/page/administer/users-and-groups/task/t_CreateAUser.html)。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-267">Refer the instructions to create a ServiceNow account, [create a user in ServiceNow](https://docs.servicenow.com/bundle/paris-platform-administration/page/administer/users-and-groups/task/t_CreateAUser.html).</span></span>

<span data-ttu-id="ad0b1-268">下表提供如何填寫 ServiceNow 使用者帳戶註冊的指導方針。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-268">The following table provides guidance on how to fill out the ServiceNow user account registration</span></span>

<span data-ttu-id="ad0b1-269">欄位</span><span class="sxs-lookup"><span data-stu-id="ad0b1-269">Field</span></span> | <span data-ttu-id="ad0b1-270">建議值</span><span class="sxs-lookup"><span data-stu-id="ad0b1-270">Recommended Value</span></span>
--- | ---
<span data-ttu-id="ad0b1-271">使用者識別碼</span><span class="sxs-lookup"><span data-stu-id="ad0b1-271">User ID</span></span> | <span data-ttu-id="ad0b1-272">步驟3中的服務主體識別碼。 c</span><span class="sxs-lookup"><span data-stu-id="ad0b1-272">Service Principal ID from step 3.c</span></span>
<span data-ttu-id="ad0b1-273">僅 Web 服務存取權</span><span class="sxs-lookup"><span data-stu-id="ad0b1-273">Web service access only</span></span> | <span data-ttu-id="ad0b1-274">Checked</span><span class="sxs-lookup"><span data-stu-id="ad0b1-274">Checked</span></span>

<span data-ttu-id="ad0b1-275">其他所有值都可以保留預設值。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-275">All other values can be left to default.</span></span>

##### <a name="step-36-enable-knowledge-role-for-the-servicenow-account"></a><span data-ttu-id="ad0b1-276">步驟3.6：啟用 ServiceNow 帳戶的知識角色</span><span class="sxs-lookup"><span data-stu-id="ad0b1-276">Step 3.6: Enable Knowledge role for the ServiceNow account</span></span>

<span data-ttu-id="ad0b1-277">存取您用 ServiceNow 主體識別碼建立的 ServiceNow 帳戶做為使用者識別碼並指派知識角色。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-277">Access the ServiceNow account you created with ServiceNow Principal ID as User ID and assign the knowledge role.</span></span> <span data-ttu-id="ad0b1-278">您可以在這裡找到將角色指派給 ServiceNow 帳戶的指示， [將角色指派給使用者](https://docs.servicenow.com/bundle/paris-platform-administration/page/administer/users-and-groups/task/t_AssignARoleToAUser.html)。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-278">Instructions to assigning a role to a ServiceNow account can be found here, [assign a role to a user](https://docs.servicenow.com/bundle/paris-platform-administration/page/administer/users-and-groups/task/t_AssignARoleToAUser.html).</span></span> <span data-ttu-id="ad0b1-279">請參閱「 [步驟3：連線設定](#step-3-connection-settings) 」的開頭中的表格，以提供更多 ServiceNow 表記錄的讀取權，以及索引使用者準則許可權。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-279">Refer the table in the beginning of [step 3: connection settings](#step-3-connection-settings) for providing read access to more ServiceNow table records and index user criteria permissions.</span></span>

<span data-ttu-id="ad0b1-280">使用應用程式識別碼做為用戶端識別碼 (從步驟3。系統管理中心) 中的) 和用戶端密碼 (，以使用 Azure AD ServiceNow OpenID 來驗證您的連線實例。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-280">Use Application ID as Client ID (from step 3.a), and Client secret (from step 3.b) in admin center configuration wizard to authenticate to your ServiceNow instance using Azure AD OpenID Connect.</span></span>

## <a name="step-4-select-properties-and-filter-data"></a><span data-ttu-id="ad0b1-281">步驟4：選取屬性和篩選資料</span><span class="sxs-lookup"><span data-stu-id="ad0b1-281">Step 4: Select properties and filter data</span></span>

<span data-ttu-id="ad0b1-282">在這個步驟中，您可以從 ServiceNow 資料來源新增或移除可用屬性。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-282">In this step, you can add or remove available properties from your ServiceNow data source.</span></span> <span data-ttu-id="ad0b1-283">Microsoft 365 已經預設會選取一些屬性。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-283">Microsoft 365 has already selected few properties by default.</span></span>

<span data-ttu-id="ad0b1-284">使用 ServiceNow 查詢字串，您可以指定同步處理文章的條件。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-284">With a ServiceNow query string, you can specify conditions for syncing articles.</span></span> <span data-ttu-id="ad0b1-285">就像 **SQL Select** 語句中的 **Where** 子句。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-285">It's like a **Where** clause in a **SQL Select** statement.</span></span> <span data-ttu-id="ad0b1-286">例如，您可以選擇只為發佈和使用中的文章編制索引。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-286">For example, you can choose to index only articles that are published and active.</span></span> <span data-ttu-id="ad0b1-287">若要瞭解如何建立您自己的查詢字串，請參閱 [使用篩選產生編碼的查詢字串](https://docs.servicenow.com/bundle/paris-platform-user-interface/page/use/using-lists/task/t_GenEncodQueryStringFilter.html)。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-287">To learn about creating your own query string, see [Generate an encoded query string using a filter](https://docs.servicenow.com/bundle/paris-platform-user-interface/page/use/using-lists/task/t_GenEncodQueryStringFilter.html).</span></span>

<span data-ttu-id="ad0b1-288">使用 [預覽結果] 按鈕，檢查所選屬性和查詢篩選器的範例值。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-288">Use the preview results button to verify the sample values of the selected properties and query filter.</span></span>

## <a name="step-5-manage-search-permissions"></a><span data-ttu-id="ad0b1-289">步驟5：管理搜尋許可權</span><span class="sxs-lookup"><span data-stu-id="ad0b1-289">Step 5: Manage search permissions</span></span>

<span data-ttu-id="ad0b1-290">ServiceNow 連接器支援 **所有人都** 可以看到的搜尋許可權，或是 **只有存取此資料來源的人員才能使用**。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-290">The ServiceNow connector supports search permissions visible to **Everyone** or **Only people with access to this data source**.</span></span> <span data-ttu-id="ad0b1-291">已編制索引的資料會顯示在搜尋結果中，並可供組織中的所有使用者或可以透過使用者準則許可權存取的使用者看到。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-291">Indexed data appears in the search results and is visible to all users in the organization or users who have access to them via user criteria permission respectively.</span></span> <span data-ttu-id="ad0b1-292">如果沒有啟用使用者準則的知識文章，它就會出現在組織中每個人的搜尋結果中。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-292">If a knowledge article is not enabled with a user criteria, it will appear in search results of everyone in the organization.</span></span>

<span data-ttu-id="ad0b1-293">ServiceNow Graph 連接器支援不含高級腳本的預設使用者準則許可權。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-293">ServiceNow Graph Connector supports default user criteria permissions without advanced scripts.</span></span> <span data-ttu-id="ad0b1-294">當連接器使用 advanced script 遇到使用者準則時，所有使用該使用者準則的資料都不會出現在搜尋結果中。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-294">When the connector encounters a user criteria with advanced script, all data using that user criteria will not appear in search results.</span></span>

>[!NOTE]
><span data-ttu-id="ad0b1-295">若要 **只選擇可存取此資料來源的人員**，請在您的租使用者上啟用目標版本更新。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-295">To choose **Only people with access to this data source**, enable targeted release updates on your tenant.</span></span> <span data-ttu-id="ad0b1-296">若要瞭解如何設定目標版本，請參閱設定 [目標版本選項。](/microsoft-365/admin/manage/release-options-in-office-365?preserve-view=true&view=o365-worldwide)</span><span class="sxs-lookup"><span data-stu-id="ad0b1-296">To learn about setting up targeted release, see [Setup Targeted release options.](/microsoft-365/admin/manage/release-options-in-office-365?preserve-view=true&view=o365-worldwide)</span></span>

<span data-ttu-id="ad0b1-297">如果您只選擇可 **存取此資料來源的人員**，您需要進一步選擇是否 ServiceNow 實例 Azure Active Directory (AAD) 已布建的使用者或非 AAD 使用者。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-297">If you choose **Only people with access to this data source**, you need to further choose whether your ServiceNow instance has Azure Active Directory (AAD) provisioned users or Non-AAD users.</span></span>

>[!NOTE]
><span data-ttu-id="ad0b1-298">如果您選擇 [AAD] 做為身分識別來源的類型，請確定您要將 UserPrincipalName (UPN) 來源屬性指派 ServiceNow 中的電子郵件目標屬性。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-298">If you choose AAD as the type of identity source, make sure you are assigning UserPrincipalName (UPN) source property to email targeted property in ServiceNow.</span></span> <span data-ttu-id="ad0b1-299">若要驗證或變更您的對應，請參閱[自訂使用者布建屬性-Azure Active Directory 中 SaaS 應用程式的對應](/azure/active-directory/app-provisioning/customize-application-attributes)。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-299">To verify or change your mappings, see [Customizing user provisioning attribute-mappings for SaaS applications in Azure Active Directory](/azure/active-directory/app-provisioning/customize-application-attributes).</span></span>

<span data-ttu-id="ad0b1-300">如果您已針對身分識別類型選擇「非 AAD」，請參閱 [對應您的非 AZURE AD](map-non-aad.md) 身分識別，以取得對應身分識別的指示。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-300">If you have elected "non-AAD" for the identity type see [Map your non-Azure AD Identities](map-non-aad.md) for instructions on mapping the identities.</span></span> 

<span data-ttu-id="ad0b1-301">您也可以參閱下列影片以深入瞭解管理搜尋許可權。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-301">You can also refer the following video to learn more about managing search permissions.</span></span>

<span data-ttu-id="ad0b1-302">[![在 Microsoft Graph Connector 中管理 ServiceNow 的搜尋許可權](https://img.youtube.com/vi/TVSkJpk1RiE/hqdefault.jpg)](https://www.youtube.com/watch?v=TVSkJpk1RiE)</span><span class="sxs-lookup"><span data-stu-id="ad0b1-302">[![Managing Search Permissions in Microsoft Graph Connector for ServiceNow](https://img.youtube.com/vi/TVSkJpk1RiE/hqdefault.jpg)](https://www.youtube.com/watch?v=TVSkJpk1RiE)</span></span>

## <a name="step-6-assign-property-labels"></a><span data-ttu-id="ad0b1-303">步驟6：指派屬性標籤</span><span class="sxs-lookup"><span data-stu-id="ad0b1-303">Step 6: Assign property labels</span></span>

<span data-ttu-id="ad0b1-304">遵循一般設定指示。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-304">Follow the general setup instructions.</span></span>

## <a name="step-7-manage-schema"></a><span data-ttu-id="ad0b1-305">步驟7：管理架構</span><span class="sxs-lookup"><span data-stu-id="ad0b1-305">Step 7: Manage schema</span></span>

<span data-ttu-id="ad0b1-306">遵循一般設定指示。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-306">Follow the general setup instructions.</span></span>

## <a name="step-8-choose-refresh-settings"></a><span data-ttu-id="ad0b1-307">步驟8：選擇重新整理設定</span><span class="sxs-lookup"><span data-stu-id="ad0b1-307">Step 8: Choose refresh settings</span></span>

<span data-ttu-id="ad0b1-308">遵循一般設定指示。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-308">Follow the general setup instructions.</span></span>

>[!NOTE]
><span data-ttu-id="ad0b1-309">針對身分識別，只會套用已排程的完整編目。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-309">For identities, only full crawl scheduled will be applied.</span></span>

## <a name="step-9-review-connection"></a><span data-ttu-id="ad0b1-310">步驟9：檢查連線</span><span class="sxs-lookup"><span data-stu-id="ad0b1-310">Step 9: Review Connection</span></span>

<span data-ttu-id="ad0b1-311">遵循一般 [設定指示](./configure-connector.md)。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-311">Follow the general [setup instructions](./configure-connector.md).</span></span>

<span data-ttu-id="ad0b1-312">ServiceNow Graph 連接器在其最新版本中有下列限制：</span><span class="sxs-lookup"><span data-stu-id="ad0b1-312">ServiceNow Graph connector has the following limitations in its latest release:</span></span>

<span data-ttu-id="ad0b1-313">在發佈連線後，您必須自訂搜尋結果頁面。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-313">After publishing the connection, you need to customize the search results page.</span></span> <span data-ttu-id="ad0b1-314">若要瞭解如何自訂搜尋結果，請參閱 [自訂搜尋結果頁面](/microsoftsearch/configure-connector#next-steps-customize-the-search-results-page)。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-314">To learn about customizing search results, see [Customize the search results page](/microsoftsearch/configure-connector#next-steps-customize-the-search-results-page).</span></span>

## <a name="limitations"></a><span data-ttu-id="ad0b1-315">限制</span><span class="sxs-lookup"><span data-stu-id="ad0b1-315">Limitations</span></span>
<span data-ttu-id="ad0b1-316">ServiceNow Graph 連接器在其最新版本中有下列限制：</span><span class="sxs-lookup"><span data-stu-id="ad0b1-316">ServiceNow Graph connector has the following limitations in its latest release:</span></span>
- <span data-ttu-id="ad0b1-317">組織中的每個人都可以使用的索引知識文章是一項普遍可用的功能。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-317">Indexing knowledge articles available to everyone in an organization is a generally available feature.</span></span>
- <span data-ttu-id="ad0b1-318">*只有存取此資料來源功能的使用者* 才會在 [管理搜尋許可權] 步驟中以「管理搜尋許可權」步驟為目標，而且只會處理 [使用者準則](https://hi.service-now.com/kb_view.do?sysparm_article=KB0550924) 許可權。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-318">*Only people with access to this data source* feature under Manage Search permissions step is in targeted release channel and processes only [user criteria](https://hi.service-now.com/kb_view.do?sysparm_article=KB0550924) permissions.</span></span> <span data-ttu-id="ad0b1-319">任何其他類型的存取權限都不會套用到搜尋結果中。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-319">Any other type of access permissions will not be applied in the search results.</span></span>
- <span data-ttu-id="ad0b1-320">目前的版本不支援具有高級腳本的使用者準則。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-320">User criteria with advanced scripts are not supported in the current version.</span></span> <span data-ttu-id="ad0b1-321">任何具有這類訪問限制的知識文章，都將會以「拒絕所有人」存取權來編制索引，也就是說，直到我們支援它們時，才會顯示在搜尋結果中。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-321">Any knowledge articles with such an access restriction will be indexed with deny everyone access i.e. they will not appear in search results to any user until we support them.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="ad0b1-322">疑難排解</span><span class="sxs-lookup"><span data-stu-id="ad0b1-322">Troubleshooting</span></span>
<span data-ttu-id="ad0b1-323">在發佈連線後，自訂 [結果] 頁面，您可以在系統 [管理中心](https://admin.microsoft.com)的 [**資料來源**] 索引標籤底下查看狀態。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-323">After publishing your connection, customizing the results page, you can review the status under the **Data Sources** tab in the [admin center](https://admin.microsoft.com).</span></span> <span data-ttu-id="ad0b1-324">若要瞭解如何進行更新和刪除，請參閱 [管理您的連接器](manage-connector.md)。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-324">To learn how to make updates and deletions, see [Manage your connector](manage-connector.md).</span></span>
<span data-ttu-id="ad0b1-325">您可以在下面找到常見問題的疑難排解步驟。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-325">You can find troubleshooting steps for commonly seen issues below.</span></span>
### <a name="1-unable-to-login-due-to-single-sign-on-enabled-servicenow-instance"></a><span data-ttu-id="ad0b1-326">1. 由於單一 Sign-On 已啟用 ServiceNow 實例而無法登入</span><span class="sxs-lookup"><span data-stu-id="ad0b1-326">1. Unable to login due to Single Sign-On enabled ServiceNow instance</span></span>

<span data-ttu-id="ad0b1-327">如果您的組織已啟用單一 Sign-On (SSO) ServiceNow，您可能無法使用服務帳戶進行記錄。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-327">If your organization has enabled Single Sign-On (SSO) to ServiceNow, you may have trouble logging in with the service account.</span></span> <span data-ttu-id="ad0b1-328">您可以新增<em> `login.do` </em>至 ServiceNow 實例 URL，以開啟使用者名稱和密碼基礎的登入。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-328">You can bring up username and password based login by adding <em> `login.do`</em> to the ServiceNow instance URL.</span></span> <span data-ttu-id="ad0b1-329">例子。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-329">Example.</span></span> `https://<your-organization-domain>.service-now.com./login.do` 

### <a name="2-unauthorized-or-forbidden-response-to-api-request"></a><span data-ttu-id="ad0b1-330">2. API 要求的未授權或已禁止回應</span><span class="sxs-lookup"><span data-stu-id="ad0b1-330">2. Unauthorized or forbidden response to API request</span></span>

#### <a name="21-check-table-access-permissions"></a><span data-ttu-id="ad0b1-331">2.1。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-331">2.1.</span></span> <span data-ttu-id="ad0b1-332">檢查表存取許可權</span><span class="sxs-lookup"><span data-stu-id="ad0b1-332">Check table access permissions</span></span>
<span data-ttu-id="ad0b1-333">如果您在線上狀態中看到禁止回應或未經授權的回應，請檢查服務帳戶是否需要存取 [步驟3：連線設定](#step-3-connection-settings)中所述的資料表。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-333">If you see forbidden or unauthorized response in connection status, check if the service account has required access to the tables mentioned in [step 3: connection settings](#step-3-connection-settings).</span></span> <span data-ttu-id="ad0b1-334">請檢查表格中的所有資料行是否都有讀取權。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-334">Please check whether all the columns in the tables have read access.</span></span>

#### <a name="22-check-if-servicenow-instance-behind-firewall"></a><span data-ttu-id="ad0b1-335">2.2。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-335">2.2.</span></span> <span data-ttu-id="ad0b1-336">檢查防火牆背後 ServiceNow 實例是否</span><span class="sxs-lookup"><span data-stu-id="ad0b1-336">Check if ServiceNow instance behind firewall</span></span>
<span data-ttu-id="ad0b1-337">Graph如果連接器位於網路防火牆之後，連接器可能無法與您的 ServiceNow 實例取得聯繫。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-337">Graph Connector may not be able to reach your ServiceNow instance if it is behind a network firewall.</span></span> <span data-ttu-id="ad0b1-338">您將需要明確允許存取 Graph Connector service。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-338">You will need explicitly allow access to Graph Connector service.</span></span> <span data-ttu-id="ad0b1-339">您可以在下表中找到 Graph 連接器服務的公用 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-339">You can find public IP address range of Graph Connector Service in the table below.</span></span> <span data-ttu-id="ad0b1-340">根據您的租使用者區域，將其新增至您的 ServiceNow 實例網路白名單。</span><span class="sxs-lookup"><span data-stu-id="ad0b1-340">Based on your tenant region, add it to your ServiceNow instance network whitelist.</span></span>

<span data-ttu-id="ad0b1-341">**環境**</span><span class="sxs-lookup"><span data-stu-id="ad0b1-341">**Environment**</span></span> | <span data-ttu-id="ad0b1-342">**地區**</span><span class="sxs-lookup"><span data-stu-id="ad0b1-342">**Region**</span></span> | <span data-ttu-id="ad0b1-343">**Range**</span><span class="sxs-lookup"><span data-stu-id="ad0b1-343">**Range**</span></span>
--- | --- | ---
<span data-ttu-id="ad0b1-344">促使</span><span class="sxs-lookup"><span data-stu-id="ad0b1-344">PROD</span></span> | <span data-ttu-id="ad0b1-345">北美</span><span class="sxs-lookup"><span data-stu-id="ad0b1-345">North America</span></span> | <span data-ttu-id="ad0b1-346">52.250.92.252/30、52.224.250.216/30</span><span class="sxs-lookup"><span data-stu-id="ad0b1-346">52.250.92.252/30, 52.224.250.216/30</span></span>
<span data-ttu-id="ad0b1-347">促使</span><span class="sxs-lookup"><span data-stu-id="ad0b1-347">PROD</span></span> | <span data-ttu-id="ad0b1-348">歐洲</span><span class="sxs-lookup"><span data-stu-id="ad0b1-348">Europe</span></span> | <span data-ttu-id="ad0b1-349">20.54.41.208/30、51.105.159.88/30</span><span class="sxs-lookup"><span data-stu-id="ad0b1-349">20.54.41.208/30, 51.105.159.88/30</span></span> 
<span data-ttu-id="ad0b1-350">促使</span><span class="sxs-lookup"><span data-stu-id="ad0b1-350">PROD</span></span> | <span data-ttu-id="ad0b1-351">亞太地區</span><span class="sxs-lookup"><span data-stu-id="ad0b1-351">Asia Pacific</span></span> | <span data-ttu-id="ad0b1-352">52.139.188.212/30、20.43.146.44/30</span><span class="sxs-lookup"><span data-stu-id="ad0b1-352">52.139.188.212/30, 20.43.146.44/30</span></span> 


<span data-ttu-id="ad0b1-353">如果您有任何其他問題，或想要提供意見反應，請寫信給我們 aka.ms/TalkToGraphConnectors</span><span class="sxs-lookup"><span data-stu-id="ad0b1-353">If you have any other issues or want to provide feedback, write to us aka.ms/TalkToGraphConnectors</span></span>
