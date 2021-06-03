---
title: 設定 microsoft 搜尋的 microsoft 內部 Graph 連接器
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
description: Microsoft Graph 連接器的安裝程式概述
ms.openlocfilehash: ef94d530af63d8b8b33dfae3c4b411164ef31feb
ms.sourcegitcommit: 1b154441f3a3abba0f2719e66a767432bc9506ca
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/02/2021
ms.locfileid: "52720941"
---
<!-- Previous ms.author: monaray -->

<!-- markdownlint-disable no-trailing-punctuation -->

# <a name="setup-overview-for-graph-connectors-by-microsoft"></a><span data-ttu-id="663de-103">Microsoft Graph 連接器的安裝程式概述</span><span class="sxs-lookup"><span data-stu-id="663de-103">Setup overview for Graph connectors by Microsoft</span></span> 

<span data-ttu-id="663de-104">本文說明在 [Microsoft 365 系統管理中心](https://admin.microsoft.com)設定 **Microsoft** 的 Graph 連接器所需的基本程式。</span><span class="sxs-lookup"><span data-stu-id="663de-104">This article shows the basic process required to set up the Graph connectors **by Microsoft** in the [Microsoft 365 admin center](https://admin.microsoft.com).</span></span> <span data-ttu-id="663de-105">基本程序包含下列步驟：</span><span class="sxs-lookup"><span data-stu-id="663de-105">The basic process includes the following steps:</span></span>  
<!---Add links to each section in the doc--->

1. [<span data-ttu-id="663de-106">在 Microsoft 365 系統管理中心新增 Graph 連接器</span><span class="sxs-lookup"><span data-stu-id="663de-106">Add a Graph connector in the Microsoft 365 admin center</span></span>](#step-1-add-a-graph-connector-in-the-microsoft-365-admin-center)
2. [<span data-ttu-id="663de-107">命名連接</span><span class="sxs-lookup"><span data-stu-id="663de-107">Name the connection</span></span>](#step-2-name-the-connection)
3. [<span data-ttu-id="663de-108">設定連接設定</span><span class="sxs-lookup"><span data-stu-id="663de-108">Configure the connection settings</span></span>](#step-3-configure-the-connection-settings)
4. [<span data-ttu-id="663de-109">管理搜尋許可權</span><span class="sxs-lookup"><span data-stu-id="663de-109">Manage search permissions</span></span>](#step-4-manage-search-permissions)
5. [<span data-ttu-id="663de-110">指派屬性標籤</span><span class="sxs-lookup"><span data-stu-id="663de-110">Assign property labels</span></span>](#step-5-assign-property-labels)
6. [<span data-ttu-id="663de-111">管理架構</span><span class="sxs-lookup"><span data-stu-id="663de-111">Manage schema</span></span>](#step-6-manage-schema)
7. [<span data-ttu-id="663de-112">重新整理設定</span><span class="sxs-lookup"><span data-stu-id="663de-112">Refresh settings</span></span>](#step-7-refresh-settings)
8. [<span data-ttu-id="663de-113">檢查連線</span><span class="sxs-lookup"><span data-stu-id="663de-113">Review connection</span></span>](#step-8-review-connection)

<span data-ttu-id="663de-114">本文也包含疑難排解、限制及後續步驟的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="663de-114">This article also includes information about troubleshooting, limitations, and next steps:</span></span>

* [<span data-ttu-id="663de-115">疑難排解</span><span class="sxs-lookup"><span data-stu-id="663de-115">Troubleshooting</span></span>](#troubleshooting)
* [<span data-ttu-id="663de-116">限制</span><span class="sxs-lookup"><span data-stu-id="663de-116">Limitations</span></span>](#limitations)
* [<span data-ttu-id="663de-117">後續步驟</span><span class="sxs-lookup"><span data-stu-id="663de-117">Next steps</span></span>](#next-steps)

> [!NOTE]
> <span data-ttu-id="663de-118">Microsoft 的所有 Graph 連接器會類似設定程式，但不完全相同。</span><span class="sxs-lookup"><span data-stu-id="663de-118">The setup process is similar for all the Graph connectors by Microsoft but is not exactly the same.</span></span> <span data-ttu-id="663de-119">**除了閱讀本文之外，請務必閱讀資料來源的連接器特定資訊。**</span><span class="sxs-lookup"><span data-stu-id="663de-119">**In addition to reading this article, be sure to read the connector-specific information for your data source.**</span></span>  

<!---## Before you get started-->

<!---Insert "Before you get started" recommendations for this data source-->

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a><span data-ttu-id="663de-120">步驟1：在 Microsoft 365 系統管理中心新增 Graph 連接器</span><span class="sxs-lookup"><span data-stu-id="663de-120">Step 1: Add a Graph connector in the Microsoft 365 admin center</span></span>

<span data-ttu-id="663de-121">完成下列步驟以設定任何 Microsoft 建立的 Graph 連接器：</span><span class="sxs-lookup"><span data-stu-id="663de-121">Complete the following steps to configure any of the Microsoft-built Graph connectors:</span></span>

1. <span data-ttu-id="663de-122">在[Microsoft 365 系統管理中心](https://admin.microsoft.com)登入您的系統管理員帳戶。</span><span class="sxs-lookup"><span data-stu-id="663de-122">Sign into your admin account in the [Microsoft 365 admin center](https://admin.microsoft.com).</span></span>

2. <span data-ttu-id="663de-123">在功能窗格中，選取 [**設定**]，然後選取 [**搜尋 & 情報**]。</span><span class="sxs-lookup"><span data-stu-id="663de-123">In the navigation pane, select **Settings**, and then select **Search & intelligence**.</span></span> <span data-ttu-id="663de-124">選取 [ [連接器]](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors)索引標籤。</span><span class="sxs-lookup"><span data-stu-id="663de-124">Select the [Connectors tab](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors).</span></span>

3. <span data-ttu-id="663de-125">選取 [ **+ 新增**]，然後從可用選項的功能表中選取您選擇的資料來源。</span><span class="sxs-lookup"><span data-stu-id="663de-125">Select **+Add**, and then select the data source of your choice from the menu of available options.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="663de-126">![可用的資料來源包括： ADLS Gen2、Enterprise 網站、Microsoft SQL server、Azure SQL、Oracle SQL 資料庫、ServiceNow、檔案共用、Azure DevOps 和 MediaWiki。](media/add-connector.png)</span><span class="sxs-lookup"><span data-stu-id="663de-126">![Data sources available include: ADLS Gen2, Enterprise websites, Microsoft SQL server, Azure SQL, Oracle SQL database, ServiceNow, File share, Azure DevOps, and MediaWiki.](media/add-connector.png)</span></span>

> [!NOTE]
> <span data-ttu-id="663de-127">每個租使用者最多可以加入10個 Graph 連接。</span><span class="sxs-lookup"><span data-stu-id="663de-127">You can add a maximum of ten Graph connections to each tenant.</span></span>

## <a name="step-2-name-the-connection"></a><span data-ttu-id="663de-128">步驟2：命名連線</span><span class="sxs-lookup"><span data-stu-id="663de-128">Step 2: Name the connection</span></span>

<span data-ttu-id="663de-129">指定下列屬性：</span><span class="sxs-lookup"><span data-stu-id="663de-129">Specify these attributes:</span></span>

* <span data-ttu-id="663de-130"> (必要的名稱) </span><span class="sxs-lookup"><span data-stu-id="663de-130">Name (required)</span></span>
* <span data-ttu-id="663de-131">需要 (連線識別碼) </span><span class="sxs-lookup"><span data-stu-id="663de-131">Connection ID (required)</span></span>
* <span data-ttu-id="663de-132">Description (optional) </span><span class="sxs-lookup"><span data-stu-id="663de-132">Description (optional)</span></span>

<span data-ttu-id="663de-133">連接識別碼會建立連接器的隱含屬性。</span><span class="sxs-lookup"><span data-stu-id="663de-133">The connection ID creates implicit properties for your connector.</span></span> <span data-ttu-id="663de-134">它必須只包含字母數位字元，最多可以有32個字元。</span><span class="sxs-lookup"><span data-stu-id="663de-134">It must contain only alphanumeric characters and be a maximum of 32 characters.</span></span>

## <a name="step-3-configure-the-connection-settings"></a><span data-ttu-id="663de-135">步驟3：設定連接設定</span><span class="sxs-lookup"><span data-stu-id="663de-135">Step 3: Configure the connection settings</span></span>

<span data-ttu-id="663de-136">設定連線設定的程式會根據資料來源的類型而有所不同。</span><span class="sxs-lookup"><span data-stu-id="663de-136">The process to configure the connection settings varies based on the type of data source.</span></span> <span data-ttu-id="663de-137">請參閱您想要新增至租使用者的資料來源類型的連接器特定資訊，以在安裝程式中完成此步驟。</span><span class="sxs-lookup"><span data-stu-id="663de-137">See the Connector-specific information for the type of data source you want to add to your tenant to complete this step in the setup process.</span></span>  

<span data-ttu-id="663de-138">若要深入瞭解連線至內部部署資料來源的詳細資訊，請參閱 [安裝內部部署資料閘道](/data-integration/gateway/service-gateway-install)。</span><span class="sxs-lookup"><span data-stu-id="663de-138">To learn more about connecting to an on-premises data source, see [Install an on-premises data gateway](/data-integration/gateway/service-gateway-install).</span></span>

## <a name="step-4-manage-search-permissions"></a><span data-ttu-id="663de-139">步驟4：管理搜尋許可權</span><span class="sxs-lookup"><span data-stu-id="663de-139">Step 4: Manage search permissions</span></span>

<span data-ttu-id="663de-140"> (ACLs 的存取控制清單) 決定組織中的哪些使用者可以存取每個資料項目目。</span><span class="sxs-lookup"><span data-stu-id="663de-140">Access Control Lists (ACLs) determine which users in your organization can access each item of data.</span></span>  

<span data-ttu-id="663de-141">某些連接器（如[Microsoft SQL](MSSQL-connector.md)和[Azure Data Lake 儲存體 Gen2](azure-data-lake-connector.md)本身支援[Azure Active Directory (Azure AD) ](/azure/active-directory/) ACLs）。</span><span class="sxs-lookup"><span data-stu-id="663de-141">Some connectors like [Microsoft SQL](MSSQL-connector.md) and [Azure Data Lake Storage Gen2](azure-data-lake-connector.md) natively support [Azure Active Directory (Azure AD)](/azure/active-directory/) ACLs.</span></span>

<span data-ttu-id="663de-142">其他連接器（如[ServiceNow](servicenow-connector.md)、 [Azure DevOps](azure-devops-connector.md)和[Salesforce](salesforce-connector.md) ）支援非 Azure AD 使用者和群組的同步處理。</span><span class="sxs-lookup"><span data-stu-id="663de-142">Other connectors like [ServiceNow](servicenow-connector.md), [Azure DevOps](azure-devops-connector.md), and [Salesforce](salesforce-connector.md) support syncing of non-Azure AD users and groups.</span></span>  

## <a name="step-5-assign-property-labels"></a><span data-ttu-id="663de-143">步驟5：指派屬性標籤</span><span class="sxs-lookup"><span data-stu-id="663de-143">Step 5: Assign property labels</span></span>

<span data-ttu-id="663de-144">您可以在 [指派屬性標籤] 頁面上，將語義標籤指派給來源屬性。</span><span class="sxs-lookup"><span data-stu-id="663de-144">You can assign semantic labels to your source properties on the "Assign property labels" page.</span></span> <span data-ttu-id="663de-145">標籤是由 Microsoft 提供的已知標記，可提供語義意義。</span><span class="sxs-lookup"><span data-stu-id="663de-145">Labels are well-known tags provided by Microsoft that provide semantic meaning.</span></span> <span data-ttu-id="663de-146">它們可讓 Microsoft 將您的連接器資料整合到 Microsoft 365 體驗，例如增強型搜尋、人員卡片、智慧探索等等。</span><span class="sxs-lookup"><span data-stu-id="663de-146">They allow Microsoft to integrate your connector data into Microsoft 365 experiences such as enhanced search, people cards, intelligent discovery, and more.</span></span>  

<span data-ttu-id="663de-147">下表列出目前支援的標籤及其描述。</span><span class="sxs-lookup"><span data-stu-id="663de-147">The following table lists the currently supported labels and their descriptions.</span></span>  

<span data-ttu-id="663de-148">標籤</span><span class="sxs-lookup"><span data-stu-id="663de-148">Label</span></span> | <span data-ttu-id="663de-149">描述</span><span class="sxs-lookup"><span data-stu-id="663de-149">Description</span></span>
--- | ---  
<span data-ttu-id="663de-150">**title**</span><span class="sxs-lookup"><span data-stu-id="663de-150">**title**</span></span> | <span data-ttu-id="663de-151">您想要顯示在搜尋和其他體驗中的專案標題</span><span class="sxs-lookup"><span data-stu-id="663de-151">The title for the item that you want shown in search and other experiences</span></span>
<span data-ttu-id="663de-152">**url**</span><span class="sxs-lookup"><span data-stu-id="663de-152">**url**</span></span> | <span data-ttu-id="663de-153">來源系統中專案的目標 url</span><span class="sxs-lookup"><span data-stu-id="663de-153">The target url of the item in the source system</span></span>
<span data-ttu-id="663de-154">**createdBy**</span><span class="sxs-lookup"><span data-stu-id="663de-154">**createdBy**</span></span> | <span data-ttu-id="663de-155">建立專案的人員名稱</span><span class="sxs-lookup"><span data-stu-id="663de-155">Name of the person who created the item</span></span>
<span data-ttu-id="663de-156">**lastModifiedBy**</span><span class="sxs-lookup"><span data-stu-id="663de-156">**lastModifiedBy**</span></span> | <span data-ttu-id="663de-157">最近編輯專案的人員名稱</span><span class="sxs-lookup"><span data-stu-id="663de-157">Name of the person who most recently edited the item</span></span>
<span data-ttu-id="663de-158">**作者**</span><span class="sxs-lookup"><span data-stu-id="663de-158">**authors**</span></span> | <span data-ttu-id="663de-159">參與或合作專案的人員名稱</span><span class="sxs-lookup"><span data-stu-id="663de-159">Name of the people who participated/collaborated on the item</span></span>
<span data-ttu-id="663de-160">**createdDateTime**</span><span class="sxs-lookup"><span data-stu-id="663de-160">**createdDateTime**</span></span> | <span data-ttu-id="663de-161">專案的建立時間</span><span class="sxs-lookup"><span data-stu-id="663de-161">When was the item created</span></span>
<span data-ttu-id="663de-162">**lastModifiedDateTime**</span><span class="sxs-lookup"><span data-stu-id="663de-162">**lastModifiedDateTime**</span></span> | <span data-ttu-id="663de-163">專案最近編輯的時間</span><span class="sxs-lookup"><span data-stu-id="663de-163">When was the item most recently edited</span></span>
<span data-ttu-id="663de-164">**檔案名**</span><span class="sxs-lookup"><span data-stu-id="663de-164">**fileName**</span></span> | <span data-ttu-id="663de-165">檔專案的名稱</span><span class="sxs-lookup"><span data-stu-id="663de-165">Name of the file item</span></span>
<span data-ttu-id="663de-166">**fileExtension**</span><span class="sxs-lookup"><span data-stu-id="663de-166">**fileExtension**</span></span> | <span data-ttu-id="663de-167">檔專案的類型，例如 .pdf 或 word。</span><span class="sxs-lookup"><span data-stu-id="663de-167">Type of file item such as .pdf or .word</span></span>

<span data-ttu-id="663de-168">此頁面上的屬性會根據您的資料來源預先選取，但是如果有其他屬性更適合特定標籤，您可以變更此選取範圍。</span><span class="sxs-lookup"><span data-stu-id="663de-168">The properties on this page are pre-selected based on your data source, but you can change this selection if there's a different property that is better suited for a particular label.</span></span>  

<span data-ttu-id="663de-169">標籤 **標題** 是最重要的標籤。</span><span class="sxs-lookup"><span data-stu-id="663de-169">The label **title** is the most important label.</span></span> <span data-ttu-id="663de-170">**強烈建議** 您將屬性指派給此標籤，以便讓連線參與 [結果叢集體驗](result-cluster.md)。</span><span class="sxs-lookup"><span data-stu-id="663de-170">It's **strongly recommended** you have a property assigned to this label in order for your connection to participate in the [result cluster experience](result-cluster.md).</span></span>

<span data-ttu-id="663de-171">不正確地對應標籤會導致 deteriorated 搜尋體驗。</span><span class="sxs-lookup"><span data-stu-id="663de-171">Incorrectly mapping labels will cause a deteriorated search experience.</span></span> <span data-ttu-id="663de-172">有些標籤不會有指派屬性。</span><span class="sxs-lookup"><span data-stu-id="663de-172">It's okay for some labels to not have a property assigned to it.</span></span>  

## <a name="step-6-manage-schema"></a><span data-ttu-id="663de-173">步驟6：管理架構</span><span class="sxs-lookup"><span data-stu-id="663de-173">Step 6: Manage schema</span></span>

### <a name="content-property"></a><span data-ttu-id="663de-174">Content 屬性</span><span class="sxs-lookup"><span data-stu-id="663de-174">Content property</span></span>

<span data-ttu-id="663de-175">建議您從選項的下拉式功能表中選取 **內容屬性** ，或保留預設值（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="663de-175">It's recommended you select a **Content Property** from the drop-down menu of options, or keep the default if one is present.</span></span> <span data-ttu-id="663de-176">此屬性用於內容、搜尋結果頁面片段產生、 [結果](result-cluster.md) 叢集加入、語言偵測、HTML/文字支援、排名與相關性及查詢表述的全文檢索索引。</span><span class="sxs-lookup"><span data-stu-id="663de-176">This property is used for full-text indexing of content, search results page snippet generation, [result cluster](result-cluster.md) participation, language detection, HTML/text support, ranking and relevance, and query formulation.</span></span>

<span data-ttu-id="663de-177">如果您選取內容屬性，當您 [建立結果類型](customize-results-layout.md)時，可以選擇使用系統所產生的屬性 **ResultSnippet** 。</span><span class="sxs-lookup"><span data-stu-id="663de-177">If you select a content property, you will have the option of using the system-generated property **ResultSnippet** when you [create your result type](customize-results-layout.md).</span></span> <span data-ttu-id="663de-178">此屬性用作在查詢時從 content 屬性產生之動態程式碼片段的預留位置。</span><span class="sxs-lookup"><span data-stu-id="663de-178">This property serves as a placeholder for the dynamic snippets that are generated from the content property at query time.</span></span> <span data-ttu-id="663de-179">如果您在結果類型中使用此屬性，則會在搜尋結果中產生程式碼片段。</span><span class="sxs-lookup"><span data-stu-id="663de-179">If you use this property in your result type, snippets will be generated in your search results.</span></span>

### <a name="creating-aliases-for-source-properties"></a><span data-ttu-id="663de-180">建立來源屬性的別名</span><span class="sxs-lookup"><span data-stu-id="663de-180">Creating aliases for source properties</span></span>

<span data-ttu-id="663de-181">您可以在「管理架構」頁面的 [別名] 欄下，新增別名至您的屬性。</span><span class="sxs-lookup"><span data-stu-id="663de-181">You can add aliases to your properties under the "Alias" column on the "Manage schema" page.</span></span> <span data-ttu-id="663de-182">別名是屬性的易記名稱，也可用於查詢和建立篩選。</span><span class="sxs-lookup"><span data-stu-id="663de-182">Aliases are friendly names for your properties, and also used in queries and in the creation of filters.</span></span> <span data-ttu-id="663de-183">它們也用來從多個連接中標準化來源屬性，使其具有相同名稱。</span><span class="sxs-lookup"><span data-stu-id="663de-183">They're also used to normalize source properties from multiple connections such that they have the same name.</span></span> <span data-ttu-id="663de-184">這樣一來，您就可以建立單一篩選，使其具有多個連線。</span><span class="sxs-lookup"><span data-stu-id="663de-184">That way you can create a single filter for a vertical with multiple connections.</span></span> <span data-ttu-id="663de-185">如需詳細資訊，請參閱 [自訂搜尋結果頁面](customize-search-page.md)。</span><span class="sxs-lookup"><span data-stu-id="663de-185">For more information, see [Customize the search results page](customize-search-page.md).</span></span>  

### <a name="search-schema-attributes"></a><span data-ttu-id="663de-186">搜尋架構屬性</span><span class="sxs-lookup"><span data-stu-id="663de-186">Search schema attributes</span></span>

<span data-ttu-id="663de-187">您可以設定搜尋架構屬性，以控制每個來源屬性的搜尋功能。</span><span class="sxs-lookup"><span data-stu-id="663de-187">You can set the search schema attributes to control search functionality of each source property.</span></span> <span data-ttu-id="663de-188">搜尋架構可協助決定搜尋結果頁面上顯示的結果，以及使用者可以查看和存取哪些資訊。</span><span class="sxs-lookup"><span data-stu-id="663de-188">A search schema helps determine what results display on the search results page and what information end users can view and access.</span></span>

<span data-ttu-id="663de-189">搜尋架構屬性包含 **查詢**、 **搜尋**、 **檢索** 及 **精煉** 的選項。</span><span class="sxs-lookup"><span data-stu-id="663de-189">Search schema attributes include options to **Query**, **Search**, **Retrieve**, and **Refine**.</span></span> <span data-ttu-id="663de-190">下表列出 Microsoft Graph 連接器支援的每個屬性，並說明其功能。</span><span class="sxs-lookup"><span data-stu-id="663de-190">The following table lists each of the attributes that Microsoft Graph connectors support and explains their functions.</span></span>

<span data-ttu-id="663de-191">搜尋架構屬性</span><span class="sxs-lookup"><span data-stu-id="663de-191">Search schema attribute</span></span> | <span data-ttu-id="663de-192">函數</span><span class="sxs-lookup"><span data-stu-id="663de-192">Function</span></span> | <span data-ttu-id="663de-193">範例</span><span class="sxs-lookup"><span data-stu-id="663de-193">Example</span></span>
--- | --- | ---
<span data-ttu-id="663de-194">搜索</span><span class="sxs-lookup"><span data-stu-id="663de-194">SEARCH</span></span> | <span data-ttu-id="663de-195">使屬性的文字內容可供搜尋。</span><span class="sxs-lookup"><span data-stu-id="663de-195">Makes the text content of a property searchable.</span></span> <span data-ttu-id="663de-196">屬性內容會包含在全文檢索索引中。</span><span class="sxs-lookup"><span data-stu-id="663de-196">Property contents are included in the full-text index.</span></span> | <span data-ttu-id="663de-197">如果屬性為 **title**， **Enterprise** 的查詢會傳回包含字 **Enterprise** 任何文字或標題的答案。</span><span class="sxs-lookup"><span data-stu-id="663de-197">If the property is **title**, a query for **Enterprise** returns answers that contain the word **Enterprise** in any text or title.</span></span>
<span data-ttu-id="663de-198">查詢</span><span class="sxs-lookup"><span data-stu-id="663de-198">QUERY</span></span> | <span data-ttu-id="663de-199">依查詢搜尋特定屬性的相符。</span><span class="sxs-lookup"><span data-stu-id="663de-199">Searches by query for a match for a particular property.</span></span> <span data-ttu-id="663de-200">您可以在查詢中以程式設計方式或逐字方式指定屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="663de-200">The property name can then be specified in the query either programmatically or verbatim.</span></span> |  <span data-ttu-id="663de-201">如果可以查詢 **title** 屬性，則支援查詢 **標題： Enterprise** 。</span><span class="sxs-lookup"><span data-stu-id="663de-201">If the **Title** property can be queried, then the query **Title: Enterprise** is supported.</span></span>
<span data-ttu-id="663de-202">檢索</span><span class="sxs-lookup"><span data-stu-id="663de-202">RETRIEVE</span></span> | <span data-ttu-id="663de-203">在結果類型中只能使用可檢索的屬性，並顯示在搜尋結果中。</span><span class="sxs-lookup"><span data-stu-id="663de-203">Only retrievable properties can be used in the result type and display in the search result.</span></span> |
<span data-ttu-id="663de-204">完善</span><span class="sxs-lookup"><span data-stu-id="663de-204">REFINE</span></span> | <span data-ttu-id="663de-205">[調整] 選項可以像在 Microsoft 搜尋結果頁面中那樣使用。</span><span class="sxs-lookup"><span data-stu-id="663de-205">The refine option can be used as in the Microsoft Search results page.</span></span> | <span data-ttu-id="663de-206">您組織中的使用者可以在 [搜尋結果] 頁面中以 **URL** [篩選](custom-filters.md)，如果在連線設定期間標示了精煉屬性</span><span class="sxs-lookup"><span data-stu-id="663de-206">Users in your organization can [filter](custom-filters.md) by **URL** in the search results page if the refine property is marked during connection setup</span></span>

<span data-ttu-id="663de-207">針對除檔案共用連接器以外的所有連接器，必須手動設定自訂類型。</span><span class="sxs-lookup"><span data-stu-id="663de-207">For all connectors except the File share connector, custom types must be set manually.</span></span> <span data-ttu-id="663de-208">若要啟動每個欄位的搜尋功能，您需要對應至屬性清單的搜尋架構。</span><span class="sxs-lookup"><span data-stu-id="663de-208">To activate search capabilities for each field, you need a search schema mapped to a list of properties.</span></span> <span data-ttu-id="663de-209">連接嚮導會根據您所選擇的來源屬性集，自動選取搜尋架構。</span><span class="sxs-lookup"><span data-stu-id="663de-209">The connection wizard automatically selects a search schema based on the set of source properties you choose.</span></span> <span data-ttu-id="663de-210">您可以在 [搜尋架構] 頁面中選取每個屬性和屬性的核取方塊，以修改此架構。</span><span class="sxs-lookup"><span data-stu-id="663de-210">You can modify this schema by selecting the check boxes for each property and attribute in the search schema page.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="663de-211">![您可以新增或移除查詢、搜尋及檢索功能，以自訂連接器的架構。](media/manageschema.png)</span><span class="sxs-lookup"><span data-stu-id="663de-211">![Schema for a connector can be customized by adding or removing Query, Search, and Retrieve functions.](media/manageschema.png)</span></span>

### <a name="restrictions-and-recommendations-for-search-schema-settings"></a><span data-ttu-id="663de-212">搜尋架構設定的限制與建議</span><span class="sxs-lookup"><span data-stu-id="663de-212">Restrictions and recommendations for search schema settings</span></span>

* <span data-ttu-id="663de-213">**Content** 屬性僅可供搜尋。</span><span class="sxs-lookup"><span data-stu-id="663de-213">The **content** property is searchable only.</span></span> <span data-ttu-id="663de-214">在下拉式清單中選取此屬性後，就無法使用 options **取回** 或 **查詢**。</span><span class="sxs-lookup"><span data-stu-id="663de-214">Once selected in the dropdown, this property cannot be used with the options **retrieve** or **query**.</span></span>

* <span data-ttu-id="663de-215">使用 **content** 屬性來呈現搜尋結果時，會發生重大效能問題。</span><span class="sxs-lookup"><span data-stu-id="663de-215">Significant performance issues occur when search results render with the **content** property.</span></span> <span data-ttu-id="663de-216">範例是 [ServiceNow](https://www.servicenow.com)知識文庫文章的 [**文字** 內容] 欄位。</span><span class="sxs-lookup"><span data-stu-id="663de-216">An example is the **Text** content field for a [ServiceNow](https://www.servicenow.com) knowledge-base article.</span></span>

* <span data-ttu-id="663de-217">在搜尋結果中，只有標示為可檢索的屬性，而且可以用來 (MRTs) 建立新式結果類型。</span><span class="sxs-lookup"><span data-stu-id="663de-217">Only properties marked as retrievable render in the search results and can be used to create modern result types (MRTs).</span></span>

* <span data-ttu-id="663de-218">只能將字串屬性標示為可搜尋。</span><span class="sxs-lookup"><span data-stu-id="663de-218">Only string properties can be marked searchable.</span></span>

> [!NOTE]
> <span data-ttu-id="663de-219">建立連線之後，就 **無法** 修改架構。</span><span class="sxs-lookup"><span data-stu-id="663de-219">After you create a connection, you **can't** modify the schema.</span></span> <span data-ttu-id="663de-220">若要這麼做，您必須刪除您的連線，並建立新的連線。</span><span class="sxs-lookup"><span data-stu-id="663de-220">To do that, you need to delete your connection and create a new one.</span></span>

## <a name="step-7-refresh-settings"></a><span data-ttu-id="663de-221">步驟7：重新整理設定</span><span class="sxs-lookup"><span data-stu-id="663de-221">Step 7: Refresh settings</span></span>

<span data-ttu-id="663de-222">[重新整理間隔] 會決定資料來源與 Microsoft 搜尋之間的同步處理頻率。</span><span class="sxs-lookup"><span data-stu-id="663de-222">The refresh interval determines how often your data is synced between the data source and Microsoft Search.</span></span> <span data-ttu-id="663de-223">每個資料來源類型都有一組不同的最佳重新整理排程，取決於修改資料的頻率及修改的類型。</span><span class="sxs-lookup"><span data-stu-id="663de-223">Each type of data source has a different set of optimal refresh schedules based on how often data is modified and the type of modifications.</span></span>

<span data-ttu-id="663de-224">有兩種重新整理間隔類型，也就是 **完整** 重新 **整理和累加** 重新整理，但是部分資料來源無法使用增量更新。</span><span class="sxs-lookup"><span data-stu-id="663de-224">There are two types of refresh intervals, which are **Full refresh** and **Incremental refresh**, but incremental refreshes aren't available for some data sources.</span></span>

<span data-ttu-id="663de-225">不論先前的編目為何，搜尋引擎都會處理並索引內容來源中已變更的專案。</span><span class="sxs-lookup"><span data-stu-id="663de-225">With a full refresh, the search engine processes and indexes the items that have changed in the content source, regardless of previous crawls.</span></span> <span data-ttu-id="663de-226">完整重新整理最適合下列情況：</span><span class="sxs-lookup"><span data-stu-id="663de-226">A full refresh works best for these situations:</span></span>

* <span data-ttu-id="663de-227">偵測資料刪除。</span><span class="sxs-lookup"><span data-stu-id="663de-227">Detecting deletions of data.</span></span>
* <span data-ttu-id="663de-228">增量式重新整理找到錯誤，但失敗。</span><span class="sxs-lookup"><span data-stu-id="663de-228">The incremental refresh found errors, and failed.</span></span>
* <span data-ttu-id="663de-229">已修改 ACLs。</span><span class="sxs-lookup"><span data-stu-id="663de-229">ACLs were modified.</span></span>
* <span data-ttu-id="663de-230">已修改編目規則。</span><span class="sxs-lookup"><span data-stu-id="663de-230">Crawl rules were modified.</span></span>
* <span data-ttu-id="663de-231">連線的架構尚未更新 (尚未支援架構更新) 。</span><span class="sxs-lookup"><span data-stu-id="663de-231">The schema for the connection has been updated (schema updates aren't yet supported).</span></span>

<span data-ttu-id="663de-232">使用 **增量** 重新整理，搜尋引擎只可以處理和編制自上次成功編目之後所建立或修改的專案。</span><span class="sxs-lookup"><span data-stu-id="663de-232">With an **Incremental refresh**, the search engine can process and index only the items that were created or modified since the last successful crawl.</span></span> <span data-ttu-id="663de-233">因此，並非內容來源中的所有資料都是重新編制索引。</span><span class="sxs-lookup"><span data-stu-id="663de-233">As a result, not all the data in the content source is reindexed.</span></span> <span data-ttu-id="663de-234">增量式重新整理最適合偵測內容、中繼資料、許可權及其他更新的工作。</span><span class="sxs-lookup"><span data-stu-id="663de-234">Incremental refreshes work best to detect content, metadata, permission, and other updates.</span></span>

<span data-ttu-id="663de-235">重新整理的速度會比完整重新整理快許多，因為未處理未變更的專案。</span><span class="sxs-lookup"><span data-stu-id="663de-235">Incremental refreshes are much faster than full refreshes because unchanged items aren't processed.</span></span> <span data-ttu-id="663de-236">不過，如果您選擇執行累加重新整理，您仍然需要定期執行完整重新整理，以維護內容來源與搜尋索引之間的正確資料同步處理。</span><span class="sxs-lookup"><span data-stu-id="663de-236">However, if you choose to run incremental refreshes, you still need to run full refreshes periodically to maintain correct data sync between the content source and the search index.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="663de-237">![累加編目和完整編目間隔設定會顯示增量為15分鐘，在1周完全編目。](media/refreshschedule.png)</span><span class="sxs-lookup"><span data-stu-id="663de-237">![Incremental crawl and full crawl interval settings showing Incremental at 15 minutes and Full crawl at 1 week.](media/refreshschedule.png)</span></span>

<!---Change screenshot for one that shows both options in new UI (try ServiceNow)--->

## <a name="step-8-review-connection"></a><span data-ttu-id="663de-238">步驟8：檢查連線</span><span class="sxs-lookup"><span data-stu-id="663de-238">Step 8: Review connection</span></span>

<span data-ttu-id="663de-239">您可以視需要複查整個設定及編輯設定，然後再完成連線。</span><span class="sxs-lookup"><span data-stu-id="663de-239">You can review your entire configuration and edit settings as needed before completing the connection.</span></span> <span data-ttu-id="663de-240">**若尚未閱讀資料來源的連接器特有資訊，請務必先將其讀取。**</span><span class="sxs-lookup"><span data-stu-id="663de-240">**Be sure to read the connector-specific information for your data source if you haven't already done so.**</span></span> <span data-ttu-id="663de-241">當您準備好完成連線時，請選取 **[完成更新]** 。</span><span class="sxs-lookup"><span data-stu-id="663de-241">Select **Finish updating** when you're ready to complete the connection.</span></span>

### <a name="confirm-if-the-connection-setup-worked"></a><span data-ttu-id="663de-242">確認連接設定是否運作正常</span><span class="sxs-lookup"><span data-stu-id="663de-242">Confirm if the connection setup worked</span></span>

<span data-ttu-id="663de-243">在系統 [管理中心](https://admin.microsoft.com)的 [**連接器**] 索引標籤下，移至您發佈的連線清單。</span><span class="sxs-lookup"><span data-stu-id="663de-243">Go to the list of your published connections under the **Connectors** tab in the [admin center](https://admin.microsoft.com).</span></span> <span data-ttu-id="663de-244">若要瞭解如何進行更新和刪除，請參閱 [管理您的連接器](manage-connector.md)。</span><span class="sxs-lookup"><span data-stu-id="663de-244">To learn how to make updates and deletions, see [Manage your connector](manage-connector.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="663de-245">疑難排解</span><span class="sxs-lookup"><span data-stu-id="663de-245">Troubleshooting</span></span>
<!---Insert troubleshooting recommendations for this data source-->
<span data-ttu-id="663de-246">閱讀資料來源的連接器特定資訊。</span><span class="sxs-lookup"><span data-stu-id="663de-246">Read the connector-specific information for your data source.</span></span> 

> [!NOTE]
> <span data-ttu-id="663de-247">並非所有連接器特有的文章都包含疑難排解建議。</span><span class="sxs-lookup"><span data-stu-id="663de-247">Not all connector-specific articles include troubleshooting recommendations at this point.</span></span>

## <a name="limitations"></a><span data-ttu-id="663de-248">限制</span><span class="sxs-lookup"><span data-stu-id="663de-248">Limitations</span></span>
<!---Insert limitations for this data source-->
<span data-ttu-id="663de-249">若要瞭解適用于所有資料來源的限制，請參閱[Microsoft Graph](connectors-overview.md) connector 文章的概述。</span><span class="sxs-lookup"><span data-stu-id="663de-249">To learn about limitations that apply to all data sources see the [Overview of Microsoft Graph connectors](connectors-overview.md) article.</span></span>

<span data-ttu-id="663de-250">請參閱資料來源連接器特有的資訊，以找出其他限制是否適用于該特定 Graph 連接器。</span><span class="sxs-lookup"><span data-stu-id="663de-250">See the connector-specific information for your data source to find out if other limitations apply to that  particular Graph connector.</span></span>

## <a name="next-steps"></a><span data-ttu-id="663de-251">後續步驟</span><span class="sxs-lookup"><span data-stu-id="663de-251">Next steps</span></span>

<span data-ttu-id="663de-252">在發佈連線後，您必須自訂搜尋結果頁面。</span><span class="sxs-lookup"><span data-stu-id="663de-252">After publishing the connection, you need to customize the search results page.</span></span> <span data-ttu-id="663de-253">若要瞭解如何自訂搜尋結果，請參閱 [自訂搜尋結果頁面](customize-search-page.md)。</span><span class="sxs-lookup"><span data-stu-id="663de-253">To learn about customizing search results, see [Customize the search results page](customize-search-page.md).</span></span>