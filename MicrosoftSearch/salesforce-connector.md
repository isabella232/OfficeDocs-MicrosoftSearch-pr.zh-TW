---
title: Microsoft 搜尋的 Salesforce Graph 連接器
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
description: 設定 Microsoft 搜尋的 Salesforce Graph 連接器
ms.openlocfilehash: 7d73454fb909db24514c969f34158e3f2be5e34c
ms.sourcegitcommit: 6cffa2d29448be9a22514e7b4c3009c522af0860
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "52774087"
---
<!---Previous ms.author: rusamai --->

# <a name="salesforce-graph-connector-preview"></a><span data-ttu-id="0fb08-103">Salesforce Graph connector (preview) </span><span class="sxs-lookup"><span data-stu-id="0fb08-103">Salesforce Graph connector (preview)</span></span>

<span data-ttu-id="0fb08-104">salesforce Graph connector 可讓您的組織為您的 Salesforce 實例中的連絡人、商機、潛在客戶和帳戶物件編制索引。</span><span class="sxs-lookup"><span data-stu-id="0fb08-104">The Salesforce Graph connector, allows your organization to index Contacts, Opportunities, Leads, and Accounts objects in your Salesforce instance.</span></span> <span data-ttu-id="0fb08-105">從 Salesforce 設定連接器和索引內容之後，使用者可以從任何 Microsoft 搜尋用戶端搜尋這些專案。</span><span class="sxs-lookup"><span data-stu-id="0fb08-105">After you configure the connector and index content from Salesforce, end users can search for those items from any Microsoft Search client.</span></span>

> [!NOTE]
> <span data-ttu-id="0fb08-106">請閱讀 [**Graph 連接器**](configure-connector.md)文章的設定，以瞭解一般 Graph 連接器設定指示。</span><span class="sxs-lookup"><span data-stu-id="0fb08-106">Read the [**Setup for your Graph connector**](configure-connector.md) article to understand the general Graph connectors setup instructions.</span></span>

<span data-ttu-id="0fb08-107">本文適用于任何設定、執行及監視 Salesforce Graph 連接器的人員。</span><span class="sxs-lookup"><span data-stu-id="0fb08-107">This article is for anyone who configures, runs, and monitors a Salesforce Graph connector.</span></span> <span data-ttu-id="0fb08-108">它會補充一般設定程式，並顯示只適用于 Salesforce Graph 連接器的指示。</span><span class="sxs-lookup"><span data-stu-id="0fb08-108">It supplements the general setup process, and shows instructions that apply only for the Salesforce Graph connector.</span></span> <span data-ttu-id="0fb08-109">本文也包含 [限制](#limitations)的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0fb08-109">This article also includes information about [Limitations](#limitations).</span></span>

>[!IMPORTANT]
><span data-ttu-id="0fb08-110">Salesforce Graph 連接器目前支援暑假 ' 19 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="0fb08-110">The Salesforce Graph connector currently supports Summer '19 or later.</span></span>

## <a name="before-you-get-started"></a><span data-ttu-id="0fb08-111">開始之前</span><span class="sxs-lookup"><span data-stu-id="0fb08-111">Before you get started</span></span>

<span data-ttu-id="0fb08-112">若要連線到您的 Salesforce 實例，您需要您的 Salesforce 實例 URL、用戶端識別碼，以及 OAuth 驗證的用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="0fb08-112">To connect to your Salesforce instance, you need your Salesforce instance URL, the Client ID, and Client Secret for OAuth authentication.</span></span> <span data-ttu-id="0fb08-113">下列步驟會說明您或您的 Salesforce 管理員如何從您的 Salesforce 帳戶取得此資訊：</span><span class="sxs-lookup"><span data-stu-id="0fb08-113">The following steps explain how you or your Salesforce administrator can get this information from your Salesforce account:</span></span>

- <span data-ttu-id="0fb08-114">登入您的 Salesforce 實例，然後移至 [設定]</span><span class="sxs-lookup"><span data-stu-id="0fb08-114">Log in to your Salesforce instance and go to Setup</span></span>

- <span data-ttu-id="0fb08-115">流覽至應用程式-> 應用程式管理員。</span><span class="sxs-lookup"><span data-stu-id="0fb08-115">Navigate to Apps -> App Manager.</span></span>

- <span data-ttu-id="0fb08-116">選取 [ **新增已連線的應用程式**]。</span><span class="sxs-lookup"><span data-stu-id="0fb08-116">Select **New connected app**.</span></span>

- <span data-ttu-id="0fb08-117">完成 API 區段，如下所示：</span><span class="sxs-lookup"><span data-stu-id="0fb08-117">Complete the API section as follows:</span></span>

    - <span data-ttu-id="0fb08-118">選取 [**啟用 Oauth 設定**] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="0fb08-118">Select the checkbox for **Enable Oauth Settings**.</span></span>

    - <span data-ttu-id="0fb08-119">指定回撥 URL 做為： [https://gcs.office.com/v1.0/admin/oauth/callback](https://gcs.office.com/v1.0/admin/oauth/callback)</span><span class="sxs-lookup"><span data-stu-id="0fb08-119">Specify the Callback URL as: [https://gcs.office.com/v1.0/admin/oauth/callback](https://gcs.office.com/v1.0/admin/oauth/callback)</span></span>

    - <span data-ttu-id="0fb08-120">選取這些必要的 OAuth 範圍。</span><span class="sxs-lookup"><span data-stu-id="0fb08-120">Select these required OAuth scopes.</span></span>

        - <span data-ttu-id="0fb08-121">存取及管理您的資料 (api) </span><span class="sxs-lookup"><span data-stu-id="0fb08-121">Access and manage your data (api)</span></span>

        - <span data-ttu-id="0fb08-122">隨時以您的名義執行要求 (refresh_token、offline_access) </span><span class="sxs-lookup"><span data-stu-id="0fb08-122">Perform requests on your behalf at any time (refresh_token, offline_access)</span></span>

    - <span data-ttu-id="0fb08-123">選取 [ **需要 web 伺服器流程的機密**] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="0fb08-123">Select the checkbox for **Require secret for web server flow**.</span></span>

    - <span data-ttu-id="0fb08-124">儲存應用程式。</span><span class="sxs-lookup"><span data-stu-id="0fb08-124">Save the app.</span></span>
    
      > [!div class="mx-imgBorder"]
      > <span data-ttu-id="0fb08-125">![在系統管理員輸入上述所有必要設定之後，Salesforce 實例中的 API 區段。](media/salesforce-connector/sf1.png)</span><span class="sxs-lookup"><span data-stu-id="0fb08-125">![API section in Salesforce instance after admin has entered all required configurations listed above.](media/salesforce-connector/sf1.png)</span></span>

- <span data-ttu-id="0fb08-126">複製使用者金鑰和使用者密碼。</span><span class="sxs-lookup"><span data-stu-id="0fb08-126">Copy the consumer key and the consumer secret.</span></span> <span data-ttu-id="0fb08-127">當您在 Microsoft 365 admin 入口網站中設定 Graph 連接器的連線設定時，會使用此資訊做為用戶端識別碼和用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="0fb08-127">This information will be used as the Client ID and the Client Secret when you configure the Connection Settings for your Graph Connector in the Microsoft 365 admin portal.</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="0fb08-128">![在 admin 提交所有必要設定之後，由 Salesforce 實例中 API 區段所傳回的結果。</span><span class="sxs-lookup"><span data-stu-id="0fb08-128">![Results returned by API section in Salesforce instance after admin has submitted all required configurations.</span></span> <span data-ttu-id="0fb08-129">使用者機碼位於左欄的頂端，且使用者機密位於右列頂端。](media/salesforce-connector/clientsecret.png)</span><span class="sxs-lookup"><span data-stu-id="0fb08-129">Consumer Key is at top of left column and Consumer Secret is at top of right column.](media/salesforce-connector/clientsecret.png)</span></span>
  
- <span data-ttu-id="0fb08-130">在關閉您的 Salesforce 實例之前，請遵循下列步驟，以確保重新整理權杖不會到期：</span><span class="sxs-lookup"><span data-stu-id="0fb08-130">Before closing your Salesforce instance, follow these steps to ensure that refresh tokens don't expire:</span></span>
    - <span data-ttu-id="0fb08-131">移至應用程式-> 應用程式管理員</span><span class="sxs-lookup"><span data-stu-id="0fb08-131">Go to Apps -> App Manager</span></span>
    - <span data-ttu-id="0fb08-132">找到您已建立的應用程式，然後選取右邊的下拉式清單。</span><span class="sxs-lookup"><span data-stu-id="0fb08-132">Find the app you created and select the drop-down on the right.</span></span> <span data-ttu-id="0fb08-133">選取 [ **管理**</span><span class="sxs-lookup"><span data-stu-id="0fb08-133">Select **Manage**</span></span>
    - <span data-ttu-id="0fb08-134">選取 **編輯原則**</span><span class="sxs-lookup"><span data-stu-id="0fb08-134">Select **edit policies**</span></span>
    - <span data-ttu-id="0fb08-135">針對重新整理權杖原則，選取重新整理 **權杖有效直到撤銷**</span><span class="sxs-lookup"><span data-stu-id="0fb08-135">For refresh token policy, select **Refresh token is valid until revoked**</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="0fb08-136">![選取名為 "Refresh token 有效直到撤銷" 的重新整理權杖原則。](media/salesforce-connector/oauthpolicies.png)</span><span class="sxs-lookup"><span data-stu-id="0fb08-136">![Select the Refresh Token Policy named "Refresh token is valid until revoked "](media/salesforce-connector/oauthpolicies.png)</span></span>

<span data-ttu-id="0fb08-137">您現在可以使用[M365 系統管理中心](https://admin.microsoft.com/)完成 Graph 連接器的其餘設定程式。</span><span class="sxs-lookup"><span data-stu-id="0fb08-137">You can now use the [M365 Admin Center](https://admin.microsoft.com/) to complete the rest of the setup process for your Graph connector.</span></span>

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a><span data-ttu-id="0fb08-138">步驟1：在 Microsoft 365 系統管理中心新增 Graph 連接器</span><span class="sxs-lookup"><span data-stu-id="0fb08-138">Step 1: Add a Graph connector in the Microsoft 365 admin center</span></span>

<span data-ttu-id="0fb08-139">遵循一般 [設定指示](./configure-connector.md)。</span><span class="sxs-lookup"><span data-stu-id="0fb08-139">Follow the general [setup instructions](./configure-connector.md).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-2-name-the-connection"></a><span data-ttu-id="0fb08-140">步驟2：命名連線</span><span class="sxs-lookup"><span data-stu-id="0fb08-140">Step 2: Name the connection</span></span>

<span data-ttu-id="0fb08-141">遵循一般 [設定指示](./configure-connector.md)。</span><span class="sxs-lookup"><span data-stu-id="0fb08-141">Follow the general [setup instructions](./configure-connector.md).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-3-configure-the-connection-settings"></a><span data-ttu-id="0fb08-142">步驟3：設定連接設定</span><span class="sxs-lookup"><span data-stu-id="0fb08-142">Step 3: Configure the connection settings</span></span>

<span data-ttu-id="0fb08-143">若為實例 URL，請使用 HTTPs：//[網域]. my .com，其中網域是您組織的 Salesforce 網域。</span><span class="sxs-lookup"><span data-stu-id="0fb08-143">For the Instance URL, use https://[domain].my.salesforce.com where domain would be the Salesforce domain for your organization.</span></span>

<span data-ttu-id="0fb08-144">輸入您從 Salesforce 實例取得的用戶端識別碼和用戶端密碼，然後選取 [登入]。</span><span class="sxs-lookup"><span data-stu-id="0fb08-144">Enter the Client ID and Client Secret you obtained from your Salesforce instance and select Sign in.</span></span>

<span data-ttu-id="0fb08-145">您第一次嘗試使用這些設定登入時，您會看到一個快顯視窗，要求您使用您的系統管理員使用者名稱和密碼登入 Salesforce。</span><span class="sxs-lookup"><span data-stu-id="0fb08-145">The first time you've attempted to sign in with these settings, you'll get a pop-up asking you to log in to Salesforce with your admin username and password.</span></span> <span data-ttu-id="0fb08-146">下列螢幕擷取畫面顯示快顯功能表。</span><span class="sxs-lookup"><span data-stu-id="0fb08-146">The screenshot below shows the popup.</span></span> <span data-ttu-id="0fb08-147">輸入您的認證，然後選取 [登入]。</span><span class="sxs-lookup"><span data-stu-id="0fb08-147">Enter your credentials and select "Log In".</span></span>

  ![登入快顯視窗要求輸入使用者名稱和密碼。](media/salesforce-connector/sf4.png)

  >[!NOTE]
  ><span data-ttu-id="0fb08-149">如果快顯視窗未出現，則可能是您的瀏覽器遭到封鎖，所以您必須允許快顯視窗和重新導向。</span><span class="sxs-lookup"><span data-stu-id="0fb08-149">If the pop up does not appear, it might be getting blocked in your browser, so you must allow pop-ups and redirects.</span></span>

<span data-ttu-id="0fb08-150">搜尋綠色橫幅（如下列螢幕擷取畫面所示）中的 [連線成功]，以檢查連線是否成功。</span><span class="sxs-lookup"><span data-stu-id="0fb08-150">Check that the connection was successful by searching for a green banner that says "Connection successful" as show in the screenshot below.</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="0fb08-151">![成功登入的螢幕擷取畫面。</span><span class="sxs-lookup"><span data-stu-id="0fb08-151">![Screenshot of successful login.</span></span> <span data-ttu-id="0fb08-152">[連線成功] 的綠色旗標位於您的 Salesforce 實例 URL 的欄位底下。](media/salesforce-connector/sf5.png)</span><span class="sxs-lookup"><span data-stu-id="0fb08-152">The green banner that says "Connection successful" is located under the field for your Salesforce Instance URL](media/salesforce-connector/sf5.png)</span></span>

## <a name="step-4-manage-search-permissions"></a><span data-ttu-id="0fb08-153">步驟4：管理搜尋許可權</span><span class="sxs-lookup"><span data-stu-id="0fb08-153">Step 4: Manage search permissions</span></span>

<span data-ttu-id="0fb08-154">您必須選擇哪一使用者會看到來自此資料來源的搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="0fb08-154">You'll need to choose which users will see search results from this data source.</span></span> <span data-ttu-id="0fb08-155">如果您只允許特定 Azure Active Directory (Azure ad) 或非 Azure ad 使用者看到搜尋結果，請確定您對應的是識別碼。</span><span class="sxs-lookup"><span data-stu-id="0fb08-155">If you allow only certain Azure Active Directory (Azure AD) or Non-Azure AD users to see the search results, make sure you map the identities.</span></span>

### <a name="step-4a-select-permissions"></a><span data-ttu-id="0fb08-156">步驟4：選取許可權</span><span class="sxs-lookup"><span data-stu-id="0fb08-156">Step 4.a: Select permissions</span></span>

<span data-ttu-id="0fb08-157">您可以選擇從您的 Salesforce 實例中 (ACLs) 來攝取存取控制清單，或允許組織中的每個人都看到來自此資料來源的搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="0fb08-157">You can choose to ingest Access Control Lists (ACLs) from your Salesforce instance, or allow everyone in your organization to see search results from this data source.</span></span> <span data-ttu-id="0fb08-158">ACLs 可以包含 Azure Active Directory (AAD) 身分識別， (從 azure ad 同盟到 Salesforce) 的使用者、非 Azure ad 身分識別 (在 Azure AD) 中具有對應身分識別的原生使用者，或兩者皆有。</span><span class="sxs-lookup"><span data-stu-id="0fb08-158">ACLs can include Azure Active Directory (AAD) identities (users who are federated from Azure AD to Salesforce), non-Azure AD identities (native Salesforce users who have corresponding identities in Azure AD), or both.</span></span>

>[!NOTE]
><span data-ttu-id="0fb08-159">如果您使用的協力廠商身分識別提供者（如 Ping 識別碼或 secureAuth），則應該選取「非 AAD」做為身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="0fb08-159">If you use a third-party Identity Provider like Ping ID or secureAuth, you should select "non-AAD" as the identity type.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="0fb08-160">![選取由系統管理員已完成的 [許可權] 畫面。管理員已選取 [只有存取此資料來源的人員] 選項，而且已從識別類型的下拉式功能表中選取「AAD」。](media/salesforce-connector/sf6.png)</span><span class="sxs-lookup"><span data-stu-id="0fb08-160">![Select permissions screen that has been completed by an admin. The admin has selected the "Only people with access to this data source" option and has also selected "AAD" from a drop down menu of identity types.](media/salesforce-connector/sf6.png)</span></span>

<span data-ttu-id="0fb08-161">如果您選擇從您的 Salesforce 實例或為身分識別類型選取 "非 AAD" 的 ACL，請參閱 [Map 您的非 AZURE AD](map-non-aad.md) 身分識別，以取得對應身分識別的指示。</span><span class="sxs-lookup"><span data-stu-id="0fb08-161">If you chose to ingest an ACL from your Salesforce instance and selected "non-AAD" for the identity type, see [Map your non-Azure AD Identities](map-non-aad.md) for instructions on mapping the identities.</span></span>

### <a name="step-4b-map-aad-identities"></a><span data-ttu-id="0fb08-162">步驟4： b：對應 AAD 身分識別</span><span class="sxs-lookup"><span data-stu-id="0fb08-162">Step 4.b: Map AAD identities</span></span>

<span data-ttu-id="0fb08-163">如果您選擇從您的 Salesforce 實例中攝取 ACL 並為身分識別類型選取「AAD」，請參閱 [對應 AZURE AD](map-aad.md) 身分識別，以取得對應身分識別的指示。</span><span class="sxs-lookup"><span data-stu-id="0fb08-163">If you chose to ingest an ACL from your Salesforce instance and selected "AAD" for the identity type, see [Map your Azure AD Identities](map-aad.md) for instructions on mapping the identities.</span></span> <span data-ttu-id="0fb08-164">若要瞭解如何設定適用于 Salesforce 的 Azure AD SSO，請參閱本 [教學](/azure/active-directory/saas-apps/salesforce-tutorial)課程。</span><span class="sxs-lookup"><span data-stu-id="0fb08-164">To learn how to set up Azure AD SSO for Salesforce, see this [tutorial](/azure/active-directory/saas-apps/salesforce-tutorial).</span></span>

### <a name="apply-user-mapping-to-sync-your-salesforce-identities-to-azure-ad-identities"></a><span data-ttu-id="0fb08-165">套用使用者對應，將您的 Salesforce 身分識別同步處理至 Azure AD 身分識別</span><span class="sxs-lookup"><span data-stu-id="0fb08-165">Apply user mapping to sync your Salesforce identities to Azure AD identities</span></span>

<span data-ttu-id="0fb08-166">在此影片中，您可以看到對您的 salesforce 實例進行驗證的程式、將非 Azure Active Directory 身分同步處理至您的 Azure Active Directory 身分識別，以及套用適當的安全性 trimmings 至您的 salesforce 專案。</span><span class="sxs-lookup"><span data-stu-id="0fb08-166">In this video you can see the process to authenticate to your Salesforce instance, sync your non-Azure Active Directory identities to your Azure Active Directory identities, and apply the proper security trimmings to your Salesforce items.</span></span>

> [!VIDEO https://www.youtube-nocookie.com/embed/SZYiFxZMKcM]

## <a name="step-5-assign-property-labels"></a><span data-ttu-id="0fb08-167">步驟5：指派屬性標籤</span><span class="sxs-lookup"><span data-stu-id="0fb08-167">Step 5: Assign property labels</span></span>

<span data-ttu-id="0fb08-168">您可以從選項的功能表中選擇，將 source 屬性指派給每個標籤。</span><span class="sxs-lookup"><span data-stu-id="0fb08-168">You can assign a source property to each label by choosing from a menu of options.</span></span> <span data-ttu-id="0fb08-169">這個步驟不是必要的，具有一些屬性標籤會提升搜尋相關性，並確保使用者的更好搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="0fb08-169">While this step is not mandatory, having some property labels will improve the search relevance and ensure better search results for end users.</span></span> <span data-ttu-id="0fb08-170">根據預設，有些標籤（如 "Title"、"URL"、"CreatedBy"、"LastModifiedBy"）已被指派來源屬性。</span><span class="sxs-lookup"><span data-stu-id="0fb08-170">By default, some of the Labels like "Title," "URL," "CreatedBy," and  "LastModifiedBy" have already been assigned source properties.</span></span>

## <a name="step-6-manage-schema"></a><span data-ttu-id="0fb08-171">步驟6：管理架構</span><span class="sxs-lookup"><span data-stu-id="0fb08-171">Step 6: Manage schema</span></span>

<span data-ttu-id="0fb08-172">您可以選取應該編制索引的來源屬性，使其顯示在搜尋結果中。</span><span class="sxs-lookup"><span data-stu-id="0fb08-172">You can select what source properties should be indexed so that they show up in search results.</span></span> <span data-ttu-id="0fb08-173">依預設，連接嚮導會根據一組來源屬性選取搜尋架構。</span><span class="sxs-lookup"><span data-stu-id="0fb08-173">The connection wizard by default selects a search schema based on a set of source properties.</span></span> <span data-ttu-id="0fb08-174">您可以在 [搜尋架構] 頁面中選取每個屬性和屬性的核取方塊，以加以修改。</span><span class="sxs-lookup"><span data-stu-id="0fb08-174">You can modify it by selecting the check boxes for each property and attribute in the search schema page.</span></span> <span data-ttu-id="0fb08-175">搜尋架構屬性包括搜尋、查詢、檢索及精煉。</span><span class="sxs-lookup"><span data-stu-id="0fb08-175">Search schema attributes include Search, Query, Retrieve, and Refine.</span></span>
<span data-ttu-id="0fb08-176">精煉功能可讓您定義以後可用作自訂精簡器或篩選搜尋體驗的屬性。</span><span class="sxs-lookup"><span data-stu-id="0fb08-176">Refine allows you to define the properties that can be later used as custom refiners or filters in the search experience.</span></span>  

> [!div class="mx-imgBorder"]
> <span data-ttu-id="0fb08-177">![選取每個來源屬性的架構。</span><span class="sxs-lookup"><span data-stu-id="0fb08-177">![Select the schema for each source property.</span></span> <span data-ttu-id="0fb08-178">選項包括查詢、搜尋、檢索及精煉](media/salesforce-connector/sf9.png)</span><span class="sxs-lookup"><span data-stu-id="0fb08-178">The options are Query, Search, Retrieve, and Refine](media/salesforce-connector/sf9.png)</span></span>

## <a name="step-7-set-the-refresh-schedule"></a><span data-ttu-id="0fb08-179">步驟7：設定重新整理排程</span><span class="sxs-lookup"><span data-stu-id="0fb08-179">Step 7: Set the refresh schedule</span></span>

<span data-ttu-id="0fb08-180">Salesforce 連接器只支援目前完全編目的重新整理排程。</span><span class="sxs-lookup"><span data-stu-id="0fb08-180">The Salesforce connector only supports refresh schedules for full crawls currently.</span></span>

>[!IMPORTANT]
><span data-ttu-id="0fb08-181">完整編目會找到先前同步處理至 Microsoft 搜尋索引的已刪除物件和使用者。</span><span class="sxs-lookup"><span data-stu-id="0fb08-181">A full crawl finds deleted objects and users that were previously synced to the Microsoft Search index.</span></span>

<span data-ttu-id="0fb08-182">建議的排程為一周完整編目。</span><span class="sxs-lookup"><span data-stu-id="0fb08-182">The recommended schedule is one week for a full crawl.</span></span>

## <a name="step-8-review-connection"></a><span data-ttu-id="0fb08-183">步驟8：檢查連線</span><span class="sxs-lookup"><span data-stu-id="0fb08-183">Step 8: Review connection</span></span>

<span data-ttu-id="0fb08-184">遵循一般 [設定指示](./configure-connector.md)。</span><span class="sxs-lookup"><span data-stu-id="0fb08-184">Follow the general [setup instructions](./configure-connector.md).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

<!---## Troubleshooting-->
<!---Insert troubleshooting recommendations for this data source-->

## <a name="limitations"></a><span data-ttu-id="0fb08-185">限制</span><span class="sxs-lookup"><span data-stu-id="0fb08-185">Limitations</span></span>

- <span data-ttu-id="0fb08-186">Graph 連接器目前不支援 Apex 基礎、區域型共用及從 Salesforce 使用個人群組共用。</span><span class="sxs-lookup"><span data-stu-id="0fb08-186">The Graph connector doesn't currently support Apex based, territory-based sharing and sharing using personal groups from Salesforce.</span></span>
- <span data-ttu-id="0fb08-187">Graph 連接器所使用的 Salesforce API 有已知的缺陷，在此情況下，潛在客戶的私人組織範圍預設值目前不會生效。</span><span class="sxs-lookup"><span data-stu-id="0fb08-187">There's a known bug in the Salesforce API the Graph connector uses, where the private org-wide defaults for leads aren't honored currently.</span></span>  
- <span data-ttu-id="0fb08-188">如果欄位具有欄位層級安全性 (FLS) 設定設定檔，Graph 連接器將不會為該 Salesforce 組織中的任何設定檔攝取該欄位。因此，使用者將無法搜尋這些欄位的值，也不會顯示在結果中。</span><span class="sxs-lookup"><span data-stu-id="0fb08-188">If a field has field level security (FLS) set for a profile, the Graph connector won't ingest that field for any profiles in that Salesforce org. As a result, users won't be able to search on values for those fields, nor will it show up in the results.</span></span>  
- <span data-ttu-id="0fb08-189">在 [管理架構] 畫面中，這些通用的標準屬性名稱會列出一次，這些選項為 **查詢**、 **搜尋**、 **檢索** 及 **精煉**，並套用至 all 或 none。</span><span class="sxs-lookup"><span data-stu-id="0fb08-189">In the Manage Schema screen these common standard property names are listed once, the options are **Query**, **Search**, **Retrieve**, and **Refine**, and apply to all or none.</span></span>
    - <span data-ttu-id="0fb08-190">名稱</span><span class="sxs-lookup"><span data-stu-id="0fb08-190">Name</span></span>
    - <span data-ttu-id="0fb08-191">URL</span><span class="sxs-lookup"><span data-stu-id="0fb08-191">Url</span></span>
    - <span data-ttu-id="0fb08-192">描述</span><span class="sxs-lookup"><span data-stu-id="0fb08-192">Description</span></span>
    - <span data-ttu-id="0fb08-193">傳真</span><span class="sxs-lookup"><span data-stu-id="0fb08-193">Fax</span></span>
    - <span data-ttu-id="0fb08-194">Phone</span><span class="sxs-lookup"><span data-stu-id="0fb08-194">Phone</span></span>
    - <span data-ttu-id="0fb08-195">MobilePhone</span><span class="sxs-lookup"><span data-stu-id="0fb08-195">MobilePhone</span></span>
    - <span data-ttu-id="0fb08-196">電子郵件</span><span class="sxs-lookup"><span data-stu-id="0fb08-196">Email</span></span>
    - <span data-ttu-id="0fb08-197">類型</span><span class="sxs-lookup"><span data-stu-id="0fb08-197">Type</span></span>
    - <span data-ttu-id="0fb08-198">職稱</span><span class="sxs-lookup"><span data-stu-id="0fb08-198">Title</span></span>
    - <span data-ttu-id="0fb08-199">AccountId</span><span class="sxs-lookup"><span data-stu-id="0fb08-199">AccountId</span></span>
    - <span data-ttu-id="0fb08-200">AccountName</span><span class="sxs-lookup"><span data-stu-id="0fb08-200">AccountName</span></span>
    - <span data-ttu-id="0fb08-201">AccountUrl</span><span class="sxs-lookup"><span data-stu-id="0fb08-201">AccountUrl</span></span>
    - <span data-ttu-id="0fb08-202">AccountOwner</span><span class="sxs-lookup"><span data-stu-id="0fb08-202">AccountOwner</span></span>
    - <span data-ttu-id="0fb08-203">AccountOwnerUrl</span><span class="sxs-lookup"><span data-stu-id="0fb08-203">AccountOwnerUrl</span></span>
    - <span data-ttu-id="0fb08-204">擁有者</span><span class="sxs-lookup"><span data-stu-id="0fb08-204">Owner</span></span>
    - <span data-ttu-id="0fb08-205">OwnerUrl</span><span class="sxs-lookup"><span data-stu-id="0fb08-205">OwnerUrl</span></span>
    - <span data-ttu-id="0fb08-206">CreatedBy</span><span class="sxs-lookup"><span data-stu-id="0fb08-206">CreatedBy</span></span>
    - <span data-ttu-id="0fb08-207">CreatedByUrl</span><span class="sxs-lookup"><span data-stu-id="0fb08-207">CreatedByUrl</span></span>
    - <span data-ttu-id="0fb08-208">LastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="0fb08-208">LastModifiedBy</span></span>
    - <span data-ttu-id="0fb08-209">LastModifiedByUrl</span><span class="sxs-lookup"><span data-stu-id="0fb08-209">LastModifiedByUrl</span></span>
    - <span data-ttu-id="0fb08-210">LastModifiedDate</span><span class="sxs-lookup"><span data-stu-id="0fb08-210">LastModifiedDate</span></span>
    - <span data-ttu-id="0fb08-211">ObjectName</span><span class="sxs-lookup"><span data-stu-id="0fb08-211">ObjectName</span></span>
