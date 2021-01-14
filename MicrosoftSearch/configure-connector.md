---
title: 設定 microsoft 內置的連接器以進行 Microsoft 搜尋
ms.author: monaray
author: monaray97
manager: jameslau
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 設定 microsoft 內置的連接器以進行 Microsoft 搜尋
ms.openlocfilehash: 61a7d444ddc4c290b5098c327faa8e70f0ef1049
ms.sourcegitcommit: 469be70ad295a5837978d75babf5243115257f77
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/13/2021
ms.locfileid: "49847544"
---
<!-- markdownlint-disable no-trailing-punctuation -->

# <a name="setup-overview-for-graph-connectors-by-microsoft"></a><span data-ttu-id="0bad0-103">Microsoft 的圖形連接器安裝程式概述</span><span class="sxs-lookup"><span data-stu-id="0bad0-103">Setup overview for Graph connectors by Microsoft</span></span> 

<span data-ttu-id="0bad0-104">本文摘要說明使用 [microsoft 365 系統管理中心](https://admin.microsoft.com) 來設定 microsoft 的任何圖形連接器所需的基本程式。</span><span class="sxs-lookup"><span data-stu-id="0bad0-104">This article summarizes the basic process required to use the [Microsoft 365 admin center](https://admin.microsoft.com) to setup any of the Graph connectors by Microsoft.</span></span> <span data-ttu-id="0bad0-105">基本套裝程式含下列步驟：</span><span class="sxs-lookup"><span data-stu-id="0bad0-105">The basic process includes the following steps:</span></span>  
<!---Add links to each section in the doc--->

1. <span data-ttu-id="0bad0-106">在 Microsoft 365 系統管理中心新增圖表連接器。</span><span class="sxs-lookup"><span data-stu-id="0bad0-106">Add a Graph connector in the Microsoft 365 admin center.</span></span>
2. <span data-ttu-id="0bad0-107">命名連接。</span><span class="sxs-lookup"><span data-stu-id="0bad0-107">Name the connection.</span></span>
3. <span data-ttu-id="0bad0-108">設定連接設定。</span><span class="sxs-lookup"><span data-stu-id="0bad0-108">Configure the connection settings.</span></span>
4. <span data-ttu-id="0bad0-109">管理搜尋許可權。</span><span class="sxs-lookup"><span data-stu-id="0bad0-109">Manage search permissions.</span></span>
5. <span data-ttu-id="0bad0-110">指派屬性標籤。</span><span class="sxs-lookup"><span data-stu-id="0bad0-110">Assign property labels.</span></span>
6. <span data-ttu-id="0bad0-111">管理架構。</span><span class="sxs-lookup"><span data-stu-id="0bad0-111">Manage schema.</span></span>
7. <span data-ttu-id="0bad0-112">選擇 [重新整理設定]。</span><span class="sxs-lookup"><span data-stu-id="0bad0-112">Choose refresh settings.</span></span>
8. <span data-ttu-id="0bad0-113">檢查連線。</span><span class="sxs-lookup"><span data-stu-id="0bad0-113">Review the connection.</span></span>

<span data-ttu-id="0bad0-114">請務必注意，安裝程式與 Microsoft 的所有圖形連接器非常類似，但並不完全相同。</span><span class="sxs-lookup"><span data-stu-id="0bad0-114">It is important to note that the setup process is very similar for all the Graph connectors by Microsoft but is not exactly the same.</span></span> <span data-ttu-id="0bad0-115">**除了閱讀本文之外，請務必閱讀資料來源的連接器特定資訊。**</span><span class="sxs-lookup"><span data-stu-id="0bad0-115">**In addition to reading this article, be sure to read the connector-specific information for your data source.**</span></span>  

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a><span data-ttu-id="0bad0-116">步驟1：在 Microsoft 365 系統管理中心新增圖表連接器</span><span class="sxs-lookup"><span data-stu-id="0bad0-116">Step 1: Add a Graph connector in the Microsoft 365 admin center</span></span>

<span data-ttu-id="0bad0-117">完成下列步驟以設定任何 Microsoft 建立的連接器。</span><span class="sxs-lookup"><span data-stu-id="0bad0-117">Complete the following steps to configure any of the Microsoft-built connectors.</span></span>

1. <span data-ttu-id="0bad0-118">在[Microsoft 365 系統管理中心](https://admin.microsoft.com)內登入您的系統管理員帳戶</span><span class="sxs-lookup"><span data-stu-id="0bad0-118">Sign into your admin account in the [Microsoft 365 admin center](https://admin.microsoft.com)</span></span>
2. <span data-ttu-id="0bad0-119">在功能窗格中，選取 [ **設定**]，然後選取 [ **搜尋 & 情報**]。</span><span class="sxs-lookup"><span data-stu-id="0bad0-119">In the navigation pane, select **Settings**, and then select **Search & intelligence**.</span></span> <span data-ttu-id="0bad0-120">選取 [ [連接器]](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors)索引標籤。</span><span class="sxs-lookup"><span data-stu-id="0bad0-120">Select the [Connectors tab](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors).</span></span>
3. <span data-ttu-id="0bad0-121">選取 [ **+ 新增**]，然後從可用選項的功能表中選取您選擇的資料來源。</span><span class="sxs-lookup"><span data-stu-id="0bad0-121">Select **+Add**, and then select the data source of your choice from the menu of available options.</span></span>

![可用的資料來源包括： ADLS Gen2、Enterprise 網站、Microsoft SQL server、Azure SQL、Oracle SQL database、ServiceNow、檔案共用、Azure DevOps 和 MediaWiki。](media/add-connector.png)

><span data-ttu-id="0bad0-123">[!附注：] 每個租使用者最多可以新增10個圖形連線。</span><span class="sxs-lookup"><span data-stu-id="0bad0-123">[!Note:] You can add a maximum of ten Graph connections to each tenant.</span></span>

## <a name="step-2-name-the-connection"></a><span data-ttu-id="0bad0-124">步驟2：命名連線</span><span class="sxs-lookup"><span data-stu-id="0bad0-124">Step 2: Name the connection</span></span>
<span data-ttu-id="0bad0-125">您將需要指定下列屬性：</span><span class="sxs-lookup"><span data-stu-id="0bad0-125">You will need to specify these attributes:</span></span> 

* <span data-ttu-id="0bad0-126">姓名</span><span class="sxs-lookup"><span data-stu-id="0bad0-126">Name</span></span>  
* <span data-ttu-id="0bad0-127">連接識別碼</span><span class="sxs-lookup"><span data-stu-id="0bad0-127">Connection ID</span></span> 
* <span data-ttu-id="0bad0-128">Description (optional) </span><span class="sxs-lookup"><span data-stu-id="0bad0-128">Description (optional)</span></span> 

<span data-ttu-id="0bad0-129">連接識別碼會建立連接器的隱含屬性。</span><span class="sxs-lookup"><span data-stu-id="0bad0-129">The connection ID creates implicit properties for your connector.</span></span> <span data-ttu-id="0bad0-130">它必須只包含字母數位字元，最多可以有32個字元。</span><span class="sxs-lookup"><span data-stu-id="0bad0-130">It must contain only alphanumeric characters and be a maximum of 32 characters.</span></span> 

## <a name="step-3-configure-the-connection-settings"></a><span data-ttu-id="0bad0-131">步驟3：設定連接設定</span><span class="sxs-lookup"><span data-stu-id="0bad0-131">Step 3: Configure the connection settings</span></span>

<span data-ttu-id="0bad0-132">設定連線設定的程式會根據資料來源的類型而有所不同。</span><span class="sxs-lookup"><span data-stu-id="0bad0-132">The process to configure the Connection settings varies based on the type of data source.</span></span> <span data-ttu-id="0bad0-133">請參閱您想要新增至租使用者的資料來源類型的連接器特定資訊，以在安裝程式中完成此步驟。</span><span class="sxs-lookup"><span data-stu-id="0bad0-133">See the Connector-specific information for the type of data source you want to add to your tenant to complete this step in the setup process.</span></span>  

<span data-ttu-id="0bad0-134">若要深入瞭解連線至內部部署資料來源的詳細資訊，請參閱 [安裝內部部署資料閘道](https://aka.ms/configuregateway)。</span><span class="sxs-lookup"><span data-stu-id="0bad0-134">To learn more about connecting to an on-premises data source, see [Install an on-premises data gateway](https://aka.ms/configuregateway).</span></span>

## <a name="step-4-manage-search-permissions"></a><span data-ttu-id="0bad0-135">步驟4：管理搜尋許可權</span><span class="sxs-lookup"><span data-stu-id="0bad0-135">Step 4: Manage search permissions</span></span>

<span data-ttu-id="0bad0-136"> (ACLs 的存取控制清單) 決定組織中的哪些使用者可以存取每個資料項目目。</span><span class="sxs-lookup"><span data-stu-id="0bad0-136">Access Control Lists (ACLs) determine which users in your organization can access each item of data.</span></span>  

<span data-ttu-id="0bad0-137">有些連接器（例如 [MICROSOFT SQL](MSSQL-connector.md) 和 [Azure Data Lake Storage Gen2](azure-data-lake-connector.md) ）在本機上支援 [AZURE Active Directory (azure AD) ](https://docs.microsoft.com/azure/active-directory/) ACLs。</span><span class="sxs-lookup"><span data-stu-id="0bad0-137">Some connectors like [Microsoft SQL](MSSQL-connector.md) and [Azure Data Lake Storage Gen2](azure-data-lake-connector.md) natively support [Azure Active Directory (Azure AD)](https://docs.microsoft.com/azure/active-directory/) ACLs.</span></span>

<span data-ttu-id="0bad0-138">其他連接器（如 [ServiceNow](servicenow-connector.md)、 [Azure DevOps](azure-devops-connector.md)和 [SALESFORCE](salesforce-connector.md) ）支援非 Azure AD 使用者和群組的同步處理。</span><span class="sxs-lookup"><span data-stu-id="0bad0-138">Other connectors like [ServiceNow](servicenow-connector.md), [Azure DevOps](azure-devops-connector.md), and [Salesforce](salesforce-connector.md) support syncing of non-Azure AD users and groups.</span></span>  

## <a name="step-5-assign-property-labels"></a><span data-ttu-id="0bad0-139">步驟5：指派屬性標籤</span><span class="sxs-lookup"><span data-stu-id="0bad0-139">Step 5: Assign property labels</span></span>
<span data-ttu-id="0bad0-140">您可以在 [指派屬性標籤] 頁面上，將語義標籤指派給來源屬性。</span><span class="sxs-lookup"><span data-stu-id="0bad0-140">You can assign semantic labels to your source properties on the "Assign property labels" page.</span></span> <span data-ttu-id="0bad0-141">標籤是由 Microsoft 提供的已知標記，可提供語義意義。</span><span class="sxs-lookup"><span data-stu-id="0bad0-141">Labels are well known tags provided by Microsoft that provide semantic meaning.</span></span> <span data-ttu-id="0bad0-142">其允許 Microsoft 將您的連接器資料整合到 Microsoft 365 體驗，例如增強型搜尋、人員卡片、智慧探索等等。</span><span class="sxs-lookup"><span data-stu-id="0bad0-142">They allow Microsoft to integrate your connector data into Microsoft 365 experiences such as enhanced search, people cards, intelligent discovery, and more.</span></span>  

<span data-ttu-id="0bad0-143">下表列出目前支援的標籤及其描述。</span><span class="sxs-lookup"><span data-stu-id="0bad0-143">The following table lists the currently supported labels and their descriptions.</span></span>  

<span data-ttu-id="0bad0-144">標籤</span><span class="sxs-lookup"><span data-stu-id="0bad0-144">Label</span></span> | <span data-ttu-id="0bad0-145">描述</span><span class="sxs-lookup"><span data-stu-id="0bad0-145">Description</span></span>
--- | ---  
<span data-ttu-id="0bad0-146">**title**</span><span class="sxs-lookup"><span data-stu-id="0bad0-146">**title**</span></span> | <span data-ttu-id="0bad0-147">您想要顯示在搜尋和其他體驗中的專案標題</span><span class="sxs-lookup"><span data-stu-id="0bad0-147">The title for the item that you want shown in search and other experiences</span></span> 
<span data-ttu-id="0bad0-148">**url**</span><span class="sxs-lookup"><span data-stu-id="0bad0-148">**url**</span></span> | <span data-ttu-id="0bad0-149">來源系統中專案的目標 url</span><span class="sxs-lookup"><span data-stu-id="0bad0-149">The target url of the item in the source system</span></span> 
<span data-ttu-id="0bad0-150">**createdBy**</span><span class="sxs-lookup"><span data-stu-id="0bad0-150">**createdBy**</span></span> | <span data-ttu-id="0bad0-151">建立專案的人員名稱</span><span class="sxs-lookup"><span data-stu-id="0bad0-151">Name of the person who created the item</span></span> 
<span data-ttu-id="0bad0-152">**lastModifiedBy**</span><span class="sxs-lookup"><span data-stu-id="0bad0-152">**lastModifiedBy**</span></span> | <span data-ttu-id="0bad0-153">最近編輯專案的人員名稱</span><span class="sxs-lookup"><span data-stu-id="0bad0-153">Name of the person who most recently edited the item</span></span> 
<span data-ttu-id="0bad0-154">**作者**</span><span class="sxs-lookup"><span data-stu-id="0bad0-154">**authors**</span></span> | <span data-ttu-id="0bad0-155">參與或合作專案的人員名稱</span><span class="sxs-lookup"><span data-stu-id="0bad0-155">Name of the people who participated/collaborated on the item</span></span> 
<span data-ttu-id="0bad0-156">**createdDateTime**</span><span class="sxs-lookup"><span data-stu-id="0bad0-156">**createdDateTime**</span></span> | <span data-ttu-id="0bad0-157">專案的建立時間</span><span class="sxs-lookup"><span data-stu-id="0bad0-157">When was the item created</span></span> 
<span data-ttu-id="0bad0-158">**lastModifiedDateTime**</span><span class="sxs-lookup"><span data-stu-id="0bad0-158">**lastModifiedDateTime**</span></span> | <span data-ttu-id="0bad0-159">專案最近編輯的時間</span><span class="sxs-lookup"><span data-stu-id="0bad0-159">When was the item most recently edited</span></span> 
<span data-ttu-id="0bad0-160">**檔案名**</span><span class="sxs-lookup"><span data-stu-id="0bad0-160">**fileName**</span></span> | <span data-ttu-id="0bad0-161">檔專案的名稱</span><span class="sxs-lookup"><span data-stu-id="0bad0-161">Name of the file item</span></span> 
<span data-ttu-id="0bad0-162">**fileExtension**</span><span class="sxs-lookup"><span data-stu-id="0bad0-162">**fileExtension**</span></span> | <span data-ttu-id="0bad0-163">檔專案的類型（例如 .pdf 或單字）</span><span class="sxs-lookup"><span data-stu-id="0bad0-163">Type of file item such as .pdf or .word</span></span> 

<span data-ttu-id="0bad0-164">此頁面上的屬性會根據您的資料來源預先選取，但是如果有不同的屬性更適合特定標籤，您可以變更此選取範圍。</span><span class="sxs-lookup"><span data-stu-id="0bad0-164">The properties on this page are pre-selected based on your data source, but you can change this selection if there is a different property that is better suited for a particular label.</span></span>  

<span data-ttu-id="0bad0-165">標籤 **標題** 是最重要的標籤。</span><span class="sxs-lookup"><span data-stu-id="0bad0-165">The label **title** is the most important label.</span></span> <span data-ttu-id="0bad0-166">**強烈建議** 您將屬性指派給此標籤，以便讓連線參與結果叢集的 [體驗](result-cluster.md)。</span><span class="sxs-lookup"><span data-stu-id="0bad0-166">It is **strongly recommended** that you have a property assigned to this label in order for your connection to participate in the [result cluster experience](result-cluster.md).</span></span>

<span data-ttu-id="0bad0-167">不正確地對應標籤會導致 deteriorated 搜尋體驗。</span><span class="sxs-lookup"><span data-stu-id="0bad0-167">Incorrectly mapping labels will cause a deteriorated search experience.</span></span> <span data-ttu-id="0bad0-168">有些標籤不會有指派屬性。</span><span class="sxs-lookup"><span data-stu-id="0bad0-168">It is okay for some labels to not have a property assigned to it.</span></span>  

## <a name="step-6-manage-schema"></a><span data-ttu-id="0bad0-169">步驟6：管理架構</span><span class="sxs-lookup"><span data-stu-id="0bad0-169">Step 6: Manage schema</span></span>

### <a name="content-property"></a><span data-ttu-id="0bad0-170">Content 屬性</span><span class="sxs-lookup"><span data-stu-id="0bad0-170">Content property</span></span>

<span data-ttu-id="0bad0-171">強烈建議您從選項的下拉式功能表中選取 [\* \* 內容] 屬性，或保留預設值（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="0bad0-171">It is strongly recommended that you select a \*\*Content Property" from the drop-down menu of options, or keep the default if one is present.</span></span> <span data-ttu-id="0bad0-172">此屬性用於內容、搜尋結果頁面片段產生、 [結果](result-cluster.md) 叢集加入、語言偵測、HTML/文字支援、排名與相關性及查詢表述的全文檢索索引。</span><span class="sxs-lookup"><span data-stu-id="0bad0-172">This property is used for full-text indexing of content, search results page snippet generation, [result cluster](result-cluster.md) participation, language detection, HTML/text support, ranking and relevance, and query formulation.</span></span>

<span data-ttu-id="0bad0-173">如果您選取內容屬性，當您 [建立結果類型](customize-results-layout.md)時，可以選擇使用系統所產生的屬性 **ResultSnippet** 。</span><span class="sxs-lookup"><span data-stu-id="0bad0-173">If you select a content property, you will have the option of using the system-generated property **ResultSnippet** when you [create your result type](customize-results-layout.md).</span></span> <span data-ttu-id="0bad0-174">此屬性用作在查詢時從 content 屬性產生之動態程式碼片段的預留位置。</span><span class="sxs-lookup"><span data-stu-id="0bad0-174">This property serves as a placeholder for the dynamic snippets that are generated from the content property at query time.</span></span> <span data-ttu-id="0bad0-175">如果您在結果類型中使用此屬性，則會在搜尋結果中產生程式碼片段。</span><span class="sxs-lookup"><span data-stu-id="0bad0-175">If you use this property in your result type, snippets will be generated in your search results.</span></span>

### <a name="creating-aliases-for-source-properties"></a><span data-ttu-id="0bad0-176">建立來源屬性的別名</span><span class="sxs-lookup"><span data-stu-id="0bad0-176">Creating aliases for source properties</span></span>

<span data-ttu-id="0bad0-177">您可以在「管理架構」頁面的 [別名] 欄下，新增別名至您的屬性。</span><span class="sxs-lookup"><span data-stu-id="0bad0-177">You can add aliases to your properties under the "Alias" column on the "Manage schema" page.</span></span> <span data-ttu-id="0bad0-178">別名是屬性的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="0bad0-178">Aliases are friendly names for your properties.</span></span> <span data-ttu-id="0bad0-179">在查詢中和建立篩選時使用。</span><span class="sxs-lookup"><span data-stu-id="0bad0-179">They are used in queries and in the creation of filters.</span></span> <span data-ttu-id="0bad0-180">它們也用來從多個連接中標準化來源屬性，使其具有相同名稱。</span><span class="sxs-lookup"><span data-stu-id="0bad0-180">They are also used to normalize source properties from multiple connections such that they have the same name.</span></span> <span data-ttu-id="0bad0-181">這樣一來，您就可以建立單一篩選，使其具有多個連線。</span><span class="sxs-lookup"><span data-stu-id="0bad0-181">That way you can create a single filter for a vertical with multiple connections.</span></span> <span data-ttu-id="0bad0-182">如需詳細資訊，請參閱 [自訂搜尋結果頁面](customize-search-page.md) 。</span><span class="sxs-lookup"><span data-stu-id="0bad0-182">See [Customize the search results page](customize-search-page.md) for more information.</span></span>  

### <a name="search-schema-attributes"></a><span data-ttu-id="0bad0-183">搜尋架構屬性</span><span class="sxs-lookup"><span data-stu-id="0bad0-183">Search schema attributes</span></span>

<span data-ttu-id="0bad0-184">您可以設定搜尋架構屬性，以控制每個來源屬性的搜尋功能。</span><span class="sxs-lookup"><span data-stu-id="0bad0-184">You can set the search schema attributes to control search functionality of each source property.</span></span> <span data-ttu-id="0bad0-185">搜尋架構可協助決定搜尋結果頁面上顯示的結果，以及使用者可以查看和存取哪些資訊。</span><span class="sxs-lookup"><span data-stu-id="0bad0-185">A search schema helps determine what results display on the search results page and what information end users can view and access.</span></span>

<span data-ttu-id="0bad0-186">搜尋架構 **屬性包括可** 搜尋、可 **查詢**、可 **檢索** 及 **可精簡搜尋**。</span><span class="sxs-lookup"><span data-stu-id="0bad0-186">Search schema attributes include **searchable**, **queryable**, **retrievable**, and **refinable**.</span></span> <span data-ttu-id="0bad0-187">下表列出 Microsoft Graph 連接器所支援的每個屬性，並說明其功能。</span><span class="sxs-lookup"><span data-stu-id="0bad0-187">The following table lists each of the attributes that Microsoft Graph connectors support and explains their functions.</span></span>

<span data-ttu-id="0bad0-188">搜尋架構屬性</span><span class="sxs-lookup"><span data-stu-id="0bad0-188">Search schema attribute</span></span> | <span data-ttu-id="0bad0-189">函數</span><span class="sxs-lookup"><span data-stu-id="0bad0-189">Function</span></span> | <span data-ttu-id="0bad0-190">範例</span><span class="sxs-lookup"><span data-stu-id="0bad0-190">Example</span></span>
--- | --- | ---
<span data-ttu-id="0bad0-191">搜索</span><span class="sxs-lookup"><span data-stu-id="0bad0-191">SEARCHABLE</span></span> | <span data-ttu-id="0bad0-192">使屬性的文字內容可供搜尋。</span><span class="sxs-lookup"><span data-stu-id="0bad0-192">Makes the text content of a property searchable.</span></span> <span data-ttu-id="0bad0-193">屬性內容會包含在全文檢索索引中。</span><span class="sxs-lookup"><span data-stu-id="0bad0-193">Property contents are included in the full-text index.</span></span> | <span data-ttu-id="0bad0-194">若屬性為 **title**， **企業** 查詢會傳回包含 word Enterprise 的任何文字或標題中的 word **enterprise** 的查詢。</span><span class="sxs-lookup"><span data-stu-id="0bad0-194">If the property is **title**, a query for **Enterprise** returns answers that contain the word **Enterprise** in any text or title.</span></span>
<span data-ttu-id="0bad0-195">可</span><span class="sxs-lookup"><span data-stu-id="0bad0-195">QUERYABLE</span></span> | <span data-ttu-id="0bad0-196">依查詢搜尋特定屬性的相符。</span><span class="sxs-lookup"><span data-stu-id="0bad0-196">Searches by query for a match for a particular property.</span></span> <span data-ttu-id="0bad0-197">您可以在查詢中以程式設計方式或逐字方式指定屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="0bad0-197">The property name can then be specified in the query either programmatically or verbatim.</span></span> |  <span data-ttu-id="0bad0-198">若 **Title** 屬性是可查詢的，則支援查詢 **標題： Enterprise** 。</span><span class="sxs-lookup"><span data-stu-id="0bad0-198">If the **Title** property is queryable, then the query **Title: Enterprise** is supported.</span></span> 
<span data-ttu-id="0bad0-199">檢索</span><span class="sxs-lookup"><span data-stu-id="0bad0-199">RETRIEVABLE</span></span> | <span data-ttu-id="0bad0-200">在結果類型中只能使用可檢索的屬性，並顯示在搜尋結果中。</span><span class="sxs-lookup"><span data-stu-id="0bad0-200">Only retrievable properties can be used in the result type and display in the search result.</span></span> |
<span data-ttu-id="0bad0-201">可精簡搜尋</span><span class="sxs-lookup"><span data-stu-id="0bad0-201">REFINABLE</span></span> | <span data-ttu-id="0bad0-202">可精簡搜尋屬性可以像在 Microsoft 搜尋結果頁面中那樣使用。</span><span class="sxs-lookup"><span data-stu-id="0bad0-202">Refinable properties can be used as in the Microsoft Search results page.</span></span> | <span data-ttu-id="0bad0-203">您組織中的使用者可在連線設定中以 **lastModifiedDateTime** 在搜尋結果頁面中 [篩選](custom-filters.md)，如果屬性標示為可精簡搜尋</span><span class="sxs-lookup"><span data-stu-id="0bad0-203">Users in your organization can [filter](custom-filters.md) by **lastModifiedDateTime** in the search results page if the property is marked refinable during connection setup</span></span>

<span data-ttu-id="0bad0-204">針對除檔案共用連接器以外的所有連接器，必須手動設定自訂類型。</span><span class="sxs-lookup"><span data-stu-id="0bad0-204">For all connectors except the File share connector, custom types must be set manually.</span></span> <span data-ttu-id="0bad0-205">若要啟動每個欄位的搜尋功能，您需要對應至屬性清單的搜尋架構。</span><span class="sxs-lookup"><span data-stu-id="0bad0-205">To activate search capabilities for each field, you need a search schema mapped to a list of properties.</span></span> <span data-ttu-id="0bad0-206">連接嚮導會根據您所選擇的來源屬性集，自動選取搜尋架構。</span><span class="sxs-lookup"><span data-stu-id="0bad0-206">The connection wizard automatically selects a search schema based on the set of source properties you choose.</span></span> <span data-ttu-id="0bad0-207">您可以在 [搜尋架構] 頁面中選取每個屬性和屬性的核取方塊，以修改此架構。</span><span class="sxs-lookup"><span data-stu-id="0bad0-207">You can modify this schema by selecting the check boxes for each property and attribute in the search schema page.</span></span>

![您可以新增或移除查詢、搜尋及檢索功能，以自訂連接器的架構。](media/manageschema.png)
 
### <a name="restrictions-and-recommendations-for-search-schema-settings"></a><span data-ttu-id="0bad0-209">搜尋架構設定的限制與建議</span><span class="sxs-lookup"><span data-stu-id="0bad0-209">Restrictions and recommendations for search schema settings</span></span>

* <span data-ttu-id="0bad0-210">**Content** 屬性僅可供搜尋。</span><span class="sxs-lookup"><span data-stu-id="0bad0-210">The **content** property is searchable only.</span></span> <span data-ttu-id="0bad0-211">在下拉式清單中選取此屬性後，就無法將此屬性標示為可 **檢索** 或可 **查詢**。</span><span class="sxs-lookup"><span data-stu-id="0bad0-211">Once selected in the dropdown, this property cannot be marked **retrievable** or **queryable**.</span></span>

* <span data-ttu-id="0bad0-212">使用 **content** 屬性來呈現搜尋結果時，會發生重大效能問題。</span><span class="sxs-lookup"><span data-stu-id="0bad0-212">Significant performance issues occur when search results render with the **content** property.</span></span> <span data-ttu-id="0bad0-213">範例是 [ServiceNow](https://www.servicenow.com)知識文庫文章的 [**文字** 內容] 欄位。</span><span class="sxs-lookup"><span data-stu-id="0bad0-213">An example is the **Text** content field for a [ServiceNow](https://www.servicenow.com) knowledge-base article.</span></span>

* <span data-ttu-id="0bad0-214">在搜尋結果中，只有標示為可檢索的屬性，而且可以用來 (MRTs) 建立新式結果類型。</span><span class="sxs-lookup"><span data-stu-id="0bad0-214">Only properties marked as retrievable render in the search results and can be used to create modern result types (MRTs).</span></span>

* <span data-ttu-id="0bad0-215">只能將字串屬性標示為可搜尋。</span><span class="sxs-lookup"><span data-stu-id="0bad0-215">Only string properties can be marked searchable.</span></span>

> [!NOTE]
> <span data-ttu-id="0bad0-216">建立連線之後，就 **無法** 修改架構。</span><span class="sxs-lookup"><span data-stu-id="0bad0-216">After you create a connection, you **can't** modify the schema.</span></span> <span data-ttu-id="0bad0-217">若要這麼做，您必須刪除您的連線，並建立新的連線。</span><span class="sxs-lookup"><span data-stu-id="0bad0-217">To do that, you need to delete your connection and create a new one.</span></span>

## <a name="step-7-refresh-settings"></a><span data-ttu-id="0bad0-218">步驟7：重新整理設定</span><span class="sxs-lookup"><span data-stu-id="0bad0-218">Step 7: Refresh settings</span></span>

<span data-ttu-id="0bad0-219">[重新整理間隔] 會決定資料來源與 Microsoft 搜尋之間的同步處理頻率。</span><span class="sxs-lookup"><span data-stu-id="0bad0-219">The refresh interval determines how often your data is synced between the data source and Microsoft Search.</span></span> <span data-ttu-id="0bad0-220">每個資料來源類型都有一組不同的最佳重新整理排程，取決於修改資料的頻率及修改的類型。</span><span class="sxs-lookup"><span data-stu-id="0bad0-220">Each type of data source has a different set of optimal refresh schedules based on how often data is modified and the type of modifications.</span></span>

<span data-ttu-id="0bad0-221">有兩種重新整理間隔類型，也就是 **完整** 重新 **整理和累加** 重新整理，但是某些資料來源無法使用增量更新。</span><span class="sxs-lookup"><span data-stu-id="0bad0-221">There are two types of refresh intervals, which are **Full refresh** and **Incremental refresh**, but incremental refreshes are not available for some data sources.</span></span>

<span data-ttu-id="0bad0-222">使用完整重新整理時，搜尋引擎會處理及索引內容來源中的每個專案，而不論先前的編目。</span><span class="sxs-lookup"><span data-stu-id="0bad0-222">With a full refresh, the search engine processes and indexes every item in the content source, regardless of previous crawls.</span></span> <span data-ttu-id="0bad0-223">完整重新整理最適合下列情況：</span><span class="sxs-lookup"><span data-stu-id="0bad0-223">A full refresh works best for these situations:</span></span>

* <span data-ttu-id="0bad0-224">偵測資料刪除。</span><span class="sxs-lookup"><span data-stu-id="0bad0-224">Detecting deletions of data.</span></span>
* <span data-ttu-id="0bad0-225">因錯誤而導致增量重新整理更新內容失敗。</span><span class="sxs-lookup"><span data-stu-id="0bad0-225">The incremental refresh failed to update content due to errors.</span></span>
* <span data-ttu-id="0bad0-226">已修改 ACLs。</span><span class="sxs-lookup"><span data-stu-id="0bad0-226">ACLs were modified.</span></span>
* <span data-ttu-id="0bad0-227">已修改編目規則。</span><span class="sxs-lookup"><span data-stu-id="0bad0-227">Crawl rules were modified.</span></span>
* <span data-ttu-id="0bad0-228">已更新連線的架構時 (尚未支援架構更新) </span><span class="sxs-lookup"><span data-stu-id="0bad0-228">When schema for the connection has been updated (schema updates are not yet supported)</span></span>

<span data-ttu-id="0bad0-229">使用 **增量** 重新整理，搜尋引擎只可以處理和編制自上次成功編目之後所建立或修改的專案。</span><span class="sxs-lookup"><span data-stu-id="0bad0-229">With an **Incremental refresh**, the search engine can process and index only the items that were created or modified since the last successful crawl.</span></span> <span data-ttu-id="0bad0-230">因此，不會重新索引內容來源中的所有資料。</span><span class="sxs-lookup"><span data-stu-id="0bad0-230">Therefore, not all the data in the content source is re-indexed.</span></span> <span data-ttu-id="0bad0-231">增量式重新整理最適合偵測內容、中繼資料、許可權及其他更新的工作。</span><span class="sxs-lookup"><span data-stu-id="0bad0-231">Incremental refreshes work best to detect content, metadata, permission, and other updates.</span></span>

<span data-ttu-id="0bad0-232">重新整理的速度會比完整重新整理快許多，因為未處理未變更的專案。</span><span class="sxs-lookup"><span data-stu-id="0bad0-232">Incremental refreshes are much faster than full refreshes because unchanged items aren’t processed.</span></span> <span data-ttu-id="0bad0-233">不過，如果您選擇執行累加重新整理，您仍然需要定期執行完整重新整理，以維護內容來源與搜尋索引之間的準確資料同步處理。</span><span class="sxs-lookup"><span data-stu-id="0bad0-233">However, if you choose to run incremental refreshes, you will still need to run full refreshes periodically to maintain an accurate data sync between the content source and the search index.</span></span>

![累加編目和完整編目間隔設定會顯示增量為15分鐘，在1周完全編目。](media/refreshschedule.png)

<!---Change screenshot for one that shows both options in new UI (try ServiceNow)--->

## <a name="step-8-review-connection"></a><span data-ttu-id="0bad0-235">步驟8：檢查連線</span><span class="sxs-lookup"><span data-stu-id="0bad0-235">Step 8: Review connection</span></span>

<span data-ttu-id="0bad0-236">您可以視需要複查整個設定及編輯設定，然後再完成連線。</span><span class="sxs-lookup"><span data-stu-id="0bad0-236">You can review your entire configuration and edit settings as needed before completing the connection.</span></span> <span data-ttu-id="0bad0-237">**若尚未閱讀資料來源的連接器特有資訊，請務必先將其讀取。**</span><span class="sxs-lookup"><span data-stu-id="0bad0-237">**Be sure to read the connector-specific information for your data source if you have not already done so.**</span></span> <span data-ttu-id="0bad0-238">當您準備好完成連線時，請選取 **[完成更新]** 。</span><span class="sxs-lookup"><span data-stu-id="0bad0-238">Select **Finish updating** when you are ready to complete the connection.</span></span>

## <a name="how-do-i-know-the-connection-setup-worked"></a><span data-ttu-id="0bad0-239">如何知道連線設定是否運作正常？</span><span class="sxs-lookup"><span data-stu-id="0bad0-239">How do I know the connection setup worked?</span></span>

<span data-ttu-id="0bad0-240">在系統 [管理中心](https://admin.microsoft.com)的 [**連接器**] 索引標籤下，移至您發佈的連線清單。</span><span class="sxs-lookup"><span data-stu-id="0bad0-240">Go to the list of your published connections under the **Connectors** tab in the [admin center](https://admin.microsoft.com).</span></span> <span data-ttu-id="0bad0-241">若要瞭解如何進行更新和刪除，請參閱 [管理您的連接器](manage-connector.md)。</span><span class="sxs-lookup"><span data-stu-id="0bad0-241">To learn how to make updates and deletions, see [Manage your connector](manage-connector.md).</span></span>
