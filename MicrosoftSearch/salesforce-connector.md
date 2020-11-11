---
title: Microsoft 搜尋的 Salesforce 連接器
ms.author: rusamai
author: rsamai
manager: jameslao
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
ROBOTS: NOINDEX, NOFOLLOW
description: 設定 Microsoft 搜尋的 Salesforce 連接器
ms.openlocfilehash: 8de7784cae7d430bc385889bd836360c69492591
ms.sourcegitcommit: 77ec27736f3c8434b2ac47e10897ac2606ee8a03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/11/2020
ms.locfileid: "48992868"
---
# <a name="salesforce-connector"></a><span data-ttu-id="cca9b-103">Salesforce 連接器</span><span class="sxs-lookup"><span data-stu-id="cca9b-103">Salesforce connector</span></span>

<span data-ttu-id="cca9b-104">透過 Salesforce 圖形連接器，您的組織可以為您的 Salesforce 實例中的連絡人、商機、潛在客戶和帳戶物件編制索引。</span><span class="sxs-lookup"><span data-stu-id="cca9b-104">With the Salesforce Graph connector, your organization can index Contacts, Opportunities, Leads and Accounts objects in your Salesforce instance.</span></span> <span data-ttu-id="cca9b-105">從 Salesforce 設定連接器和索引內容之後，使用者可以從任何 Microsoft Search 用戶端搜尋這些專案。</span><span class="sxs-lookup"><span data-stu-id="cca9b-105">After you configure the connector and index content from Salesforce, end users can search for those items from any Microsoft Search client</span></span>

<span data-ttu-id="cca9b-106">本文適用于 [Microsoft 365](https://www.microsoft.com/microsoft-365) 系統管理員或任何設定、執行及監視 Salesforce 連接器的人員。</span><span class="sxs-lookup"><span data-stu-id="cca9b-106">This article is for [Microsoft 365](https://www.microsoft.com/microsoft-365) administrators or anyone who configures, runs, and monitors a Salesforce connector.</span></span> <span data-ttu-id="cca9b-107">它說明如何設定連接器和連接器功能、限制及疑難排解技術。</span><span class="sxs-lookup"><span data-stu-id="cca9b-107">It explains how to configure your connector and connector capabilities, limitations, and troubleshooting techniques.</span></span>

>[!IMPORTANT]
><span data-ttu-id="cca9b-108">Salesforce 圖形連接器目前支援暑假 ' 20，春季 ' 20，冬季20，和暑假 ' 19 版本。</span><span class="sxs-lookup"><span data-stu-id="cca9b-108">The Salesforce Graph connector currently supports Summer ’20, Spring’20, Winter’20, and Summer ’19 versions.</span></span>

## <a name="connection-settings"></a><span data-ttu-id="cca9b-109">連接設定</span><span class="sxs-lookup"><span data-stu-id="cca9b-109">Connection settings</span></span>

<span data-ttu-id="cca9b-110">若要連線到您的 Salesforce 實例，您需要您的 Salesforce 實例 URL、用戶端識別碼，以及 OAuth 驗證的用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="cca9b-110">To connect to your Salesforce instance, you need your Salesforce instance URL, the Client ID, and Client Secret for OAuth authentication.</span></span> <span data-ttu-id="cca9b-111">下列步驟會說明您或您的 Salesforce 管理員如何從您的 Salesforce 帳戶取得此資訊：</span><span class="sxs-lookup"><span data-stu-id="cca9b-111">The following steps explain how you or your Salesforce administrator can get this information from your Salesforce account:</span></span>

- <span data-ttu-id="cca9b-112">登入您的 Salesforce 實例，然後移至 [設定]</span><span class="sxs-lookup"><span data-stu-id="cca9b-112">Log in to your Salesforce instance and go to Setup</span></span>

- <span data-ttu-id="cca9b-113">流覽至應用程式-> 應用程式管理員。</span><span class="sxs-lookup"><span data-stu-id="cca9b-113">Navigate to Apps -> App Manager.</span></span>

- <span data-ttu-id="cca9b-114">選取 [ **新增已連線的應用程式** ]。</span><span class="sxs-lookup"><span data-stu-id="cca9b-114">Select **New connected app**.</span></span>

- <span data-ttu-id="cca9b-115">完成 API 區段，如下所示：</span><span class="sxs-lookup"><span data-stu-id="cca9b-115">Complete the API section as follows:</span></span>

    - <span data-ttu-id="cca9b-116">選取 [ **啟用 Oauth 設定** ] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="cca9b-116">Select the checkbox for **Enable Oauth Settings**.</span></span>

    - <span data-ttu-id="cca9b-117">指定回撥 URL 做為： [https://gcs.office.com/v1.0/admin/oauth/callback](https://gcs.office.com/v1.0/admin/oauth/callback)</span><span class="sxs-lookup"><span data-stu-id="cca9b-117">Specify the Callback URL as: [https://gcs.office.com/v1.0/admin/oauth/callback](https://gcs.office.com/v1.0/admin/oauth/callback)</span></span>

    - <span data-ttu-id="cca9b-118">選取這些必要的 OAuth 範圍。</span><span class="sxs-lookup"><span data-stu-id="cca9b-118">Select these required OAuth scopes.</span></span> 

        - <span data-ttu-id="cca9b-119">存取及管理您的資料 (api) </span><span class="sxs-lookup"><span data-stu-id="cca9b-119">Access and manage your data (api)</span></span> 

        - <span data-ttu-id="cca9b-120">隨時以您的名義執行要求 (refresh_token、offline_access) </span><span class="sxs-lookup"><span data-stu-id="cca9b-120">Perform requests on your behalf at any time (refresh_token, offline_access)</span></span> 

    - <span data-ttu-id="cca9b-121">選取 [ **需要 web 伺服器流程的機密** ] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="cca9b-121">Select the checkbox for **Require secret for web server flow**.</span></span>

    - <span data-ttu-id="cca9b-122">儲存應用程式。</span><span class="sxs-lookup"><span data-stu-id="cca9b-122">Save the app.</span></span>
    
      ![在系統管理員輸入上述所有必要設定之後，Salesforce 實例中的 API 區段。](media/salesforce-connector/sf1.png)

- <span data-ttu-id="cca9b-124">複製使用者金鑰和使用者密碼。</span><span class="sxs-lookup"><span data-stu-id="cca9b-124">Copy the consumer key and the consumer secret.</span></span> <span data-ttu-id="cca9b-125">當您在 Microsoft 365 系統管理入口網站中設定圖形連接器的連線設定時，這些值會被當作用戶端識別碼和用戶端密碼使用。</span><span class="sxs-lookup"><span data-stu-id="cca9b-125">These will be used as the Client ID and the Client Secret when you configure the Connection Settings for your Graph Connector in the Microsoft 365 admin portal.</span></span>

  ![在 admin 提交所有必要設定之後，由 Salesforce 實例中 API 區段所傳回的結果。](media/salesforce-connector/clientsecret.png)
- <span data-ttu-id="cca9b-128">在關閉您的 Salesforce 實例之前，請先執行下列步驟，以確保重新整理權杖未到期：</span><span class="sxs-lookup"><span data-stu-id="cca9b-128">Before closing your Salesforce instance, perform the following steps to ensure that refresh tokens do not expire:</span></span> 
    - <span data-ttu-id="cca9b-129">移至應用程式-> 應用程式管理員</span><span class="sxs-lookup"><span data-stu-id="cca9b-129">Go to Apps -> App Manager</span></span>
    - <span data-ttu-id="cca9b-130">找到您剛才建立的應用程式，然後選取右邊的下拉式清單。</span><span class="sxs-lookup"><span data-stu-id="cca9b-130">Find the app you just created and select the drop down on the right.</span></span> <span data-ttu-id="cca9b-131">選取 [ **管理**</span><span class="sxs-lookup"><span data-stu-id="cca9b-131">Select **Manage**</span></span>
    - <span data-ttu-id="cca9b-132">選取 **編輯原則**</span><span class="sxs-lookup"><span data-stu-id="cca9b-132">Select **edit policies**</span></span>
    - <span data-ttu-id="cca9b-133">針對重新整理權杖原則，選取重新整理 **權杖有效直到撤銷**</span><span class="sxs-lookup"><span data-stu-id="cca9b-133">For refresh token policy, select **Refresh token is valid until revoked**</span></span>

  ![選取名為 "Refresh token 有效直到撤銷" 的重新整理權杖原則。](media/salesforce-connector/oauthpolicies.png)

<span data-ttu-id="cca9b-135">您現在可以使用 [M365 系統管理中心](https://admin.microsoft.com/) 完成圖形連接器的其餘設定程式。</span><span class="sxs-lookup"><span data-stu-id="cca9b-135">You can now use the [M365 Admin Center](https://admin.microsoft.com/) to complete the rest of the setup process for your Graph connector.</span></span>  

<span data-ttu-id="cca9b-136">如下所示，設定圖形連接器的連線設定：</span><span class="sxs-lookup"><span data-stu-id="cca9b-136">Configure the Connection settings for your Graph connector as follows:</span></span>

- <span data-ttu-id="cca9b-137">若為實例 URL，請使用 HTTPs：//[網域]. my .com，其中網域是您組織的 Salesforce 網域。</span><span class="sxs-lookup"><span data-stu-id="cca9b-137">For the Instance URL, use https://[domain].my.salesforce.com where domain would be the Salesforce domain for your organization.</span></span> 
- <span data-ttu-id="cca9b-138">輸入您從 Salesforce 實例取得的用戶端識別碼和用戶端密碼，然後選取 [登入]。</span><span class="sxs-lookup"><span data-stu-id="cca9b-138">Enter the Client ID and Client Secret you obtained from your Salesforce instance and select Sign in.</span></span>
- <span data-ttu-id="cca9b-139">如果這是您第一次嘗試使用這些設定來登入，您將會看到一個快顯視窗，要求您使用您的系統管理員使用者名稱和密碼登入 Salesforce。</span><span class="sxs-lookup"><span data-stu-id="cca9b-139">If this is the first time you have attempted to Sign in with these settings, you will get a pop up asking you to login to Salesforce with your admin username and password.</span></span> <span data-ttu-id="cca9b-140">下列螢幕擷取畫面顯示快顯功能表。</span><span class="sxs-lookup"><span data-stu-id="cca9b-140">The screenshot below shows the popup.</span></span> <span data-ttu-id="cca9b-141">輸入您的認證，然後選取 [登入]。</span><span class="sxs-lookup"><span data-stu-id="cca9b-141">Enter your credentials and select Log in.</span></span>

  ![登入快顯視窗要求輸入使用者名稱和密碼。](media/salesforce-connector/sf4.png)

  >[!NOTE]
  ><span data-ttu-id="cca9b-143">如果快顯視窗未出現，則可能是您的瀏覽器遭到封鎖，所以您必須允許快顯視窗和重新導向。</span><span class="sxs-lookup"><span data-stu-id="cca9b-143">If the pop up does not appear, it might be getting blocked in your browser, so you must allow pop-ups and redirects.</span></span>

  >[!NOTE]
  ><span data-ttu-id="cca9b-144">如果您的組織使用單一登入 (SSO) ，您可以在登入介面的右下角選取 [ **使用自訂網域** ]。</span><span class="sxs-lookup"><span data-stu-id="cca9b-144">If your organization uses single sign-on (SSO), you can select **Use Custom Domain** in the bottom, right-hand corner of the login interface.</span></span> <span data-ttu-id="cca9b-145">輸入網域，然後選取 [ **繼續** ]。</span><span class="sxs-lookup"><span data-stu-id="cca9b-145">Enter the domain and then select **Continue**.</span></span> <span data-ttu-id="cca9b-146">它會移至您組織的特定登入頁面，您可以在此頁面上使用 SSO 登入的選項。</span><span class="sxs-lookup"><span data-stu-id="cca9b-146">It will go to your organization specific login page where you will have an option to login with SSO.</span></span>

- <span data-ttu-id="cca9b-147">搜尋綠色橫幅（如下列螢幕擷取畫面所示）中的 [連線成功]，以檢查連線是否成功。</span><span class="sxs-lookup"><span data-stu-id="cca9b-147">Check that the connection was successful by searching for a green banner that says "Connection successful" as show in the screenshot below.</span></span>

  ![成功登入的螢幕擷取畫面。](media/salesforce-connector/sf5.png)

## <a name="manage-search-permissions"></a><span data-ttu-id="cca9b-150">管理搜尋許可權</span><span class="sxs-lookup"><span data-stu-id="cca9b-150">Manage search permissions</span></span>
<span data-ttu-id="cca9b-151">您將需要選擇哪些使用者將會看到來自此資料來源的搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="cca9b-151">You will need to choose which users will see search results from this data source.</span></span> <span data-ttu-id="cca9b-152">如果您只允許某些 Azure Active Directory (AAD) 或非 AAD 使用者看到搜尋結果，您就必須對應身分識別。</span><span class="sxs-lookup"><span data-stu-id="cca9b-152">If you allow only certain Azure Active Directory (AAD) or Non-AAD users to see the search results, you will then need to map the identities.</span></span>

### <a name="select-permissions"></a><span data-ttu-id="cca9b-153">選取許可權</span><span class="sxs-lookup"><span data-stu-id="cca9b-153">Select Permissions</span></span>
<span data-ttu-id="cca9b-154">您可以選擇從您的 Salesforce 實例中 (ACLs) 來攝取存取控制清單，也可以讓組織中的每個人都可以查看此資料來源的搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="cca9b-154">You can choose to ingest Access Control Lists (ACLs) from your Salesforce instance, or you can allow everyone in your organization to see search results from this data source.</span></span> <span data-ttu-id="cca9b-155">ACLs 可以包含 Azure Active Directory (AAD) 身分識別和/或非 AAD 身分識別。</span><span class="sxs-lookup"><span data-stu-id="cca9b-155">ACLs can include Azure Active Directory (AAD) identities, Non-AAD identities, or both.</span></span>

![選取由系統管理員已完成的 [許可權] 畫面。管理員已選取 [只有存取此資料來源的人員] 選項，而且已從識別類型的下拉式功能表中選取「AAD」。](media/salesforce-connector/sf6.png)

### <a name="map-non-aad-identities"></a><span data-ttu-id="cca9b-157">對應非 AAD 身分識別</span><span class="sxs-lookup"><span data-stu-id="cca9b-157">Map non-AAD identities</span></span> 
<span data-ttu-id="cca9b-158">如果您選擇從您的 Salesforce 實例中攝取 ACL 並為身分識別類型選取 "非 AAD"，請參閱 [Map 您的非 AZURE AD ](map-non-aad.md) 身分識別，以取得對應身分識別的指示。</span><span class="sxs-lookup"><span data-stu-id="cca9b-158">If you chose to ingest an ACL from your Salesforce instance and selected "non-AAD" for the identity type see [Map your non-Azure AD Identities ](map-non-aad.md) for instructions on mapping the identities.</span></span>

### <a name="map-aad-identities"></a><span data-ttu-id="cca9b-159">對應 AAD 身分識別</span><span class="sxs-lookup"><span data-stu-id="cca9b-159">Map AAD identities</span></span>
<span data-ttu-id="cca9b-160">如果您選擇從您的 Salesforce 實例中攝取 ACL 並為身分識別類型選取「AAD」，請參閱 [對應 AZURE AD](map-aad.md) 身分識別，以取得對應身分識別的指示。</span><span class="sxs-lookup"><span data-stu-id="cca9b-160">If you chose to ingest an ACL from your Salesforce instance and selected "AAD" for the identity type see [Map your Azure AD Identities](map-aad.md) for instructions on mapping the identities.</span></span>

## <a name="assign-property-labels"></a><span data-ttu-id="cca9b-161">指派屬性標籤</span><span class="sxs-lookup"><span data-stu-id="cca9b-161">Assign property labels</span></span> 
<span data-ttu-id="cca9b-162">您可以從選項的功能表中選擇，將 source 屬性指派給每個標籤。</span><span class="sxs-lookup"><span data-stu-id="cca9b-162">You can assign a source property to each label by choosing from a menu of options.</span></span> <span data-ttu-id="cca9b-163">雖然這個步驟不是必要的，但具有一些屬性標籤會提升搜尋相關性，並可確保使用者更準確的搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="cca9b-163">While this step is not mandatory, having some property labels will improve the search relevance and ensure more accurate search results for end users.</span></span> <span data-ttu-id="cca9b-164">根據預設，有些標籤（如 "Title"、"url" 和 "LastModifiedBy"）已被指派來源屬性。</span><span class="sxs-lookup"><span data-stu-id="cca9b-164">By default, some of the Labels like ”Title”, “url”, and  “LastModifiedBy” have already been assigned source properties.</span></span>

![[指派屬性標籤] 畫面顯示預設來源屬性。](media/salesforce-connector/sf8.png)

## <a name="manage-schema"></a><span data-ttu-id="cca9b-166">管理架構</span><span class="sxs-lookup"><span data-stu-id="cca9b-166">Manage Schema</span></span>
<span data-ttu-id="cca9b-167">您可以選取應該編制索引的來源屬性，使其可顯示在搜尋結果中。</span><span class="sxs-lookup"><span data-stu-id="cca9b-167">You can select what source properties should be indexed so that they can show up in search results.</span></span> <span data-ttu-id="cca9b-168">依預設，連接嚮導會根據一組來源屬性選取搜尋架構。</span><span class="sxs-lookup"><span data-stu-id="cca9b-168">The connection wizard by default selects a search schema based on a set of source properties.</span></span> <span data-ttu-id="cca9b-169">您可以在 [搜尋架構] 頁面中選取每個屬性和屬性的核取方塊，以加以修改。</span><span class="sxs-lookup"><span data-stu-id="cca9b-169">You can modify it by selecting the check boxes for each property and attribute in the search schema page.</span></span> <span data-ttu-id="cca9b-170">搜尋架構屬性包括搜尋、查詢、檢索及精煉。</span><span class="sxs-lookup"><span data-stu-id="cca9b-170">Search schema attributes include Search, Query, Retrieve and Refine.</span></span> <span data-ttu-id="cca9b-171">精煉功能可讓您定義以後可用作自訂精簡器或篩選搜尋體驗的屬性。</span><span class="sxs-lookup"><span data-stu-id="cca9b-171">Refine allows you to define the properties which can be later used as custom refiners or filters in the search experience.</span></span>  

![選取每個來源屬性的架構。](media/salesforce-connector/sf9.png)

## <a name="set-the-refresh-schedule"></a><span data-ttu-id="cca9b-174">設定重新整理排程</span><span class="sxs-lookup"><span data-stu-id="cca9b-174">Set the refresh schedule</span></span>

<span data-ttu-id="cca9b-175">Salesforce 連接器只支援目前完全編目的重新整理排程。</span><span class="sxs-lookup"><span data-stu-id="cca9b-175">The Salesforce connector only supports refresh schedules for full crawls currently.</span></span>

>[!IMPORTANT]
><span data-ttu-id="cca9b-176">完整編目會找到先前同步處理至 Microsoft 搜尋索引的已刪除物件和使用者。</span><span class="sxs-lookup"><span data-stu-id="cca9b-176">A full crawl finds deleted objects and users that were previously synced to the Microsoft Search index.</span></span>

<span data-ttu-id="cca9b-177">建議的排程為一周完整編目。</span><span class="sxs-lookup"><span data-stu-id="cca9b-177">The recommended schedule is one week for a full crawl.</span></span>

## <a name="limitations"></a><span data-ttu-id="cca9b-178">限制</span><span class="sxs-lookup"><span data-stu-id="cca9b-178">Limitations</span></span>

- <span data-ttu-id="cca9b-179">圖形連接器目前不支援 Apex 基礎、區域型共用和使用個人群組從 Salesforce 共用。</span><span class="sxs-lookup"><span data-stu-id="cca9b-179">The Graph connector does not currently support Apex based , territory-based sharing and sharing using personal groups from Salesforce.</span></span>
- <span data-ttu-id="cca9b-180">在 Salesforce API 中有一個已知的錯誤，圖形連接器會使用，而潛在客戶的私人組織寬預設值並不是有效的。</span><span class="sxs-lookup"><span data-stu-id="cca9b-180">There is a known bug in the Salesforce API that the Graph connector uses where the private org wide defaults for leads is not honored currently.</span></span>  
- <span data-ttu-id="cca9b-181">如果欄位具有欄位層級安全性 (FLS) 設定設定檔，圖形連接器將不會為該 Salesforce 組織中的任何設定檔攝取該欄位。因此，使用者將無法搜尋這些欄位的值，也不會顯示在結果中。</span><span class="sxs-lookup"><span data-stu-id="cca9b-181">If a field has field level security (FLS) set for a profile, the Graph connector will not ingest that field for any profiles in that Salesforce org. Users will thus not be able to search on values for those fields, nor will it  show up in the results.</span></span>  
- <span data-ttu-id="cca9b-182">在完整同步處理連接器時，將會進行任何設定的 FLS。</span><span class="sxs-lookup"><span data-stu-id="cca9b-182">Any FLS set up will be honored during the Full syncs of the connector.</span></span>
- <span data-ttu-id="cca9b-183">在 [管理架構] 畫面中，這些通用的標準屬性名稱會列出一次，而且已完成的選取範圍是以可查詢、可搜尋及可檢索的方式套用全部或無。</span><span class="sxs-lookup"><span data-stu-id="cca9b-183">In the Manage Schema screen these common standard property names are listed once and the selection done to make them queryable, searchable and retrievable apply to all or none.</span></span>
    - <span data-ttu-id="cca9b-184">Name</span><span class="sxs-lookup"><span data-stu-id="cca9b-184">Name</span></span>
    - <span data-ttu-id="cca9b-185">URL</span><span class="sxs-lookup"><span data-stu-id="cca9b-185">Url</span></span> 
    - <span data-ttu-id="cca9b-186">描述</span><span class="sxs-lookup"><span data-stu-id="cca9b-186">Description</span></span>
    - <span data-ttu-id="cca9b-187">傳真</span><span class="sxs-lookup"><span data-stu-id="cca9b-187">Fax</span></span>
    - <span data-ttu-id="cca9b-188">Phone</span><span class="sxs-lookup"><span data-stu-id="cca9b-188">Phone</span></span>
    - <span data-ttu-id="cca9b-189">MobilePhone</span><span class="sxs-lookup"><span data-stu-id="cca9b-189">MobilePhone</span></span>
    - <span data-ttu-id="cca9b-190">電子郵件</span><span class="sxs-lookup"><span data-stu-id="cca9b-190">Email</span></span>
    - <span data-ttu-id="cca9b-191">類型</span><span class="sxs-lookup"><span data-stu-id="cca9b-191">Type</span></span>
    - <span data-ttu-id="cca9b-192">職稱</span><span class="sxs-lookup"><span data-stu-id="cca9b-192">Title</span></span>
    - <span data-ttu-id="cca9b-193">AccountId</span><span class="sxs-lookup"><span data-stu-id="cca9b-193">AccountId</span></span>
    - <span data-ttu-id="cca9b-194">AccountName</span><span class="sxs-lookup"><span data-stu-id="cca9b-194">AccountName</span></span>
    - <span data-ttu-id="cca9b-195">AccountUrl</span><span class="sxs-lookup"><span data-stu-id="cca9b-195">AccountUrl</span></span>
    - <span data-ttu-id="cca9b-196">AccountOwner</span><span class="sxs-lookup"><span data-stu-id="cca9b-196">AccountOwner</span></span>
    - <span data-ttu-id="cca9b-197">AccountOwnerUrl</span><span class="sxs-lookup"><span data-stu-id="cca9b-197">AccountOwnerUrl</span></span>
    - <span data-ttu-id="cca9b-198">擁有者</span><span class="sxs-lookup"><span data-stu-id="cca9b-198">Owner</span></span>
    - <span data-ttu-id="cca9b-199">OwnerUrl</span><span class="sxs-lookup"><span data-stu-id="cca9b-199">OwnerUrl</span></span>
    - <span data-ttu-id="cca9b-200">CreatedBy</span><span class="sxs-lookup"><span data-stu-id="cca9b-200">CreatedBy</span></span> 
    - <span data-ttu-id="cca9b-201">CreatedByUrl</span><span class="sxs-lookup"><span data-stu-id="cca9b-201">CreatedByUrl</span></span> 
    - <span data-ttu-id="cca9b-202">LastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="cca9b-202">LastModifiedBy</span></span> 
    - <span data-ttu-id="cca9b-203">LastModifiedByUrl</span><span class="sxs-lookup"><span data-stu-id="cca9b-203">LastModifiedByUrl</span></span> 
    - <span data-ttu-id="cca9b-204">LastModifiedDate</span><span class="sxs-lookup"><span data-stu-id="cca9b-204">LastModifiedDate</span></span>
    - <span data-ttu-id="cca9b-205">ObjectName</span><span class="sxs-lookup"><span data-stu-id="cca9b-205">ObjectName</span></span> 
