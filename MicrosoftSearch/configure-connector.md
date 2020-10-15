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
ms.openlocfilehash: ce2515b3eaa859a8fbb00d83c4727865ab55e174
ms.sourcegitcommit: 6aea7102c94855e9f80711c0f3d7bf5833ce8fb5
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/14/2020
ms.locfileid: "48464474"
---
<!-- markdownlint-disable no-trailing-punctuation -->

# <a name="set-up-your-microsoft-built-connector-for-microsoft-search"></a><span data-ttu-id="3aa55-103">設定 microsoft 內建的連接器以進行 Microsoft 搜尋</span><span class="sxs-lookup"><span data-stu-id="3aa55-103">Set up your Microsoft-built connector for Microsoft Search</span></span>

<span data-ttu-id="3aa55-104">本文將引導您逐步完成設定 Microsoft 內建連接器的步驟。</span><span class="sxs-lookup"><span data-stu-id="3aa55-104">This article guides you through the steps of configuring a Microsoft-built connector.</span></span> <span data-ttu-id="3aa55-105">它概述在 Microsoft 365 系統 [管理中心](https://admin.microsoft.com)中設定連線的流程。</span><span class="sxs-lookup"><span data-stu-id="3aa55-105">It outlines the flow of setting up a connection in the Microsoft 365 [admin center](https://admin.microsoft.com).</span></span> <span data-ttu-id="3aa55-106">如需如何設定特定 Microsoft 內置連接器的詳細資訊，請參閱下列文章：</span><span class="sxs-lookup"><span data-stu-id="3aa55-106">For more information on how to set up specific Microsoft-built connectors, see these articles:</span></span>

* [<span data-ttu-id="3aa55-107">Azure Data Lake Storage Gen2</span><span class="sxs-lookup"><span data-stu-id="3aa55-107">Azure Data Lake Storage Gen2</span></span>](azure-data-lake-connector.md)
* [<span data-ttu-id="3aa55-108">Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="3aa55-108">Azure DevOps</span></span>](azure-devops-connector.md)
* [<span data-ttu-id="3aa55-109">Azure SQL</span><span class="sxs-lookup"><span data-stu-id="3aa55-109">Azure SQL</span></span>](MSSQL-connector.md)
* [<span data-ttu-id="3aa55-110">企業網站</span><span class="sxs-lookup"><span data-stu-id="3aa55-110">Enterprise websites</span></span>](enterprise-web-connector.md)
* [<span data-ttu-id="3aa55-111">MediaWiki</span><span class="sxs-lookup"><span data-stu-id="3aa55-111">MediaWiki</span></span>](mediawiki-connector.md)
* [<span data-ttu-id="3aa55-112">Microsoft SQL server</span><span class="sxs-lookup"><span data-stu-id="3aa55-112">Microsoft SQL server</span></span>](MSSQL-connector.md)
* [<span data-ttu-id="3aa55-113">ServiceNow</span><span class="sxs-lookup"><span data-stu-id="3aa55-113">ServiceNow</span></span>](servicenow-connector.md)

## <a name="set-up"></a><span data-ttu-id="3aa55-114">設定</span><span class="sxs-lookup"><span data-stu-id="3aa55-114">Set up</span></span>

<span data-ttu-id="3aa55-115">完成下列步驟以設定任何 Microsoft 建立的連接器。</span><span class="sxs-lookup"><span data-stu-id="3aa55-115">Complete the following steps to configure any of the Microsoft-built connectors.</span></span>

1. <span data-ttu-id="3aa55-116">移至[Microsoft 365 系統管理中心](https://admin.microsoft.com)中的 [[連接器]](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors)索引標籤。</span><span class="sxs-lookup"><span data-stu-id="3aa55-116">Go to the [Connectors tab](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors) in the [Microsoft 365 admin center](https://admin.microsoft.com).</span></span>
2. <span data-ttu-id="3aa55-117">使用 [Microsoft 365](https://www.microsoft.com/microsoft-365) 租使用者的認證登入您的帳戶。</span><span class="sxs-lookup"><span data-stu-id="3aa55-117">Sign in to your account with the credentials for your [Microsoft 365](https://www.microsoft.com/microsoft-365) tenant.</span></span>
3. <span data-ttu-id="3aa55-118">選取 [ **新增連接器**]。</span><span class="sxs-lookup"><span data-stu-id="3aa55-118">Select **Add a connector**.</span></span>
4. <span data-ttu-id="3aa55-119">從可用的連接器清單中，選取您選擇的連接器。</span><span class="sxs-lookup"><span data-stu-id="3aa55-119">From the list of available connectors, select the connector of your choice.</span></span>

![可用的資料來源包括： Azure DevOps Connector、ServiceNow、ADLS Gen2、Enterprise 網站、MediaWiki、Microsoft SQL server 和 Azure SQL。](media/add_connector.png)

### <a name="name-the-connector"></a><span data-ttu-id="3aa55-121">命名連接器</span><span class="sxs-lookup"><span data-stu-id="3aa55-121">Name the connector</span></span>

<span data-ttu-id="3aa55-122">若要建立連接，請先指定下列屬性：</span><span class="sxs-lookup"><span data-stu-id="3aa55-122">To create a connection, first specify these attributes:</span></span>

1. <span data-ttu-id="3aa55-123">連接的名稱</span><span class="sxs-lookup"><span data-stu-id="3aa55-123">Name of the connection</span></span>
2. <span data-ttu-id="3aa55-124">連接識別碼</span><span class="sxs-lookup"><span data-stu-id="3aa55-124">Connection ID</span></span>
3. <span data-ttu-id="3aa55-125">Description (optional) </span><span class="sxs-lookup"><span data-stu-id="3aa55-125">Description (optional)</span></span>

<span data-ttu-id="3aa55-126">連接識別碼會建立連接器的隱含屬性。</span><span class="sxs-lookup"><span data-stu-id="3aa55-126">The connection ID creates implicit properties for your connector.</span></span> <span data-ttu-id="3aa55-127">它必須只包含字母數位字元，最多可以有32個字元。</span><span class="sxs-lookup"><span data-stu-id="3aa55-127">It must contain only alphanumeric characters and be a maximum of 32 characters.</span></span>

### <a name="connect-to-a-data-source"></a><span data-ttu-id="3aa55-128">連接到資料來源</span><span class="sxs-lookup"><span data-stu-id="3aa55-128">Connect to a data source</span></span>

<span data-ttu-id="3aa55-129">資料連線過程會根據連接器類型而有所不同。</span><span class="sxs-lookup"><span data-stu-id="3aa55-129">The data connection process varies based on the type of connector.</span></span> <span data-ttu-id="3aa55-130">若要深入瞭解如何連線至您的內部部署資料來源，請參閱 [安裝內部部署資料閘道](https://aka.ms/configuregateway)。</span><span class="sxs-lookup"><span data-stu-id="3aa55-130">To learn more about connecting to your on-premises data source, see [Install an on-premises data gateway](https://aka.ms/configuregateway).</span></span>

### <a name="select-source-properties"></a><span data-ttu-id="3aa55-131">選取來源屬性</span><span class="sxs-lookup"><span data-stu-id="3aa55-131">Select source properties</span></span>

<span data-ttu-id="3aa55-132">協力廠商資料來源所設定的資料欄位會在 Microsoft 搜尋中編入來源屬性。</span><span class="sxs-lookup"><span data-stu-id="3aa55-132">The data fields set by your third-party data source as source properties are indexed into Microsoft Search.</span></span> <span data-ttu-id="3aa55-133">若要修改這些屬性，請選取 [**連接器**] 頁面右邊的側欄中的 [**編輯屬性**]。</span><span class="sxs-lookup"><span data-stu-id="3aa55-133">To modify these properties, select **Edit properties** in the side bar on the right of the **Connectors** page.</span></span> <span data-ttu-id="3aa55-134">您 **最多可以選擇64來源屬性**。</span><span class="sxs-lookup"><span data-stu-id="3aa55-134">You can select **up to 64 source properties**.</span></span>

### <a name="manage-the-search-schema"></a><span data-ttu-id="3aa55-135">管理搜尋結構描述</span><span class="sxs-lookup"><span data-stu-id="3aa55-135">Manage the search schema</span></span>

#### <a name="content-property"></a><span data-ttu-id="3aa55-136">Content 屬性</span><span class="sxs-lookup"><span data-stu-id="3aa55-136">Content property</span></span>

<span data-ttu-id="3aa55-137">您可以從**content**屬性下拉式清單中選取任何 string 屬性，以選取 [**內容**] 屬性 (專案) 的全文檢索索引。</span><span class="sxs-lookup"><span data-stu-id="3aa55-137">You can select which source property is the **content** property (full-text index of the item) by selecting any string property from the **content** property dropdown.</span></span> <span data-ttu-id="3aa55-138">或者，您可以保留預設的選取屬性（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="3aa55-138">Alternatively, you can keep the default selected property if one is present.</span></span>

<span data-ttu-id="3aa55-139">請務必選取正確的屬性，因為此屬性是用於內容的全文檢索索引、搜尋結果頁面片段產生、語言偵測、HTML/文字支援、排名與相關性，以及查詢表述。</span><span class="sxs-lookup"><span data-stu-id="3aa55-139">It is especially important that the correct property is selected since this property used for full-text indexing of content, search results page snippet generation, language detection, HTML/text support, ranking and relevance, and query formulation.</span></span>

<span data-ttu-id="3aa55-140">如果您選取**內容**的屬性，當您[建立結果類型](customize-results-layout.md)時，可以選擇使用系統所產生的屬性**ResultSnippet** 。</span><span class="sxs-lookup"><span data-stu-id="3aa55-140">If you select a property for **content**, you will have the option of using the system-generated property **ResultSnippet** when you [create your result type](customize-results-layout.md).</span></span> <span data-ttu-id="3aa55-141">此屬性用作在查詢時從 **content** 屬性產生之動態程式碼片段的預留位置。</span><span class="sxs-lookup"><span data-stu-id="3aa55-141">This property serves as a placeholder for the dynamic snippets that are generated from the **content** property at query time.</span></span> <span data-ttu-id="3aa55-142">如果您在結果類型中使用此屬性，則會在搜尋結果中產生程式碼片段。</span><span class="sxs-lookup"><span data-stu-id="3aa55-142">If you use this property in your result type, snippets will be generated in your search results.</span></span>

#### <a name="search-schema-attributes"></a><span data-ttu-id="3aa55-143">搜尋架構屬性</span><span class="sxs-lookup"><span data-stu-id="3aa55-143">Search schema attributes</span></span>

<span data-ttu-id="3aa55-144">您可以設定搜尋架構屬性，以控制每個來源屬性的搜尋功能。</span><span class="sxs-lookup"><span data-stu-id="3aa55-144">You can set the search schema attributes to control search functionality of each source property.</span></span> <span data-ttu-id="3aa55-145">搜尋架構可協助決定搜尋結果頁面上顯示的結果，以及使用者可以查看和存取哪些資訊。</span><span class="sxs-lookup"><span data-stu-id="3aa55-145">A search schema helps determine what results display on the search results page and what information end users can view and access.</span></span>

<span data-ttu-id="3aa55-146">搜尋架構屬性包括可搜尋、可**查詢**及可**供\*\*\*\*檢索**的屬性。</span><span class="sxs-lookup"><span data-stu-id="3aa55-146">Search schema attributes include **searchable**, **queryable**, and **retrievable**.</span></span> <span data-ttu-id="3aa55-147">下表列出 Microsoft Graph 連接器所支援的每個屬性，並說明其功能。</span><span class="sxs-lookup"><span data-stu-id="3aa55-147">The following table lists each of the attributes that Microsoft Graph connectors support and explains their functions.</span></span>

<span data-ttu-id="3aa55-148">搜尋架構屬性</span><span class="sxs-lookup"><span data-stu-id="3aa55-148">Search schema attribute</span></span> | <span data-ttu-id="3aa55-149">函數</span><span class="sxs-lookup"><span data-stu-id="3aa55-149">Function</span></span> | <span data-ttu-id="3aa55-150">範例</span><span class="sxs-lookup"><span data-stu-id="3aa55-150">Example</span></span>
--- | --- | ---
<span data-ttu-id="3aa55-151">搜索</span><span class="sxs-lookup"><span data-stu-id="3aa55-151">SEARCHABLE</span></span> | <span data-ttu-id="3aa55-152">使屬性的文字內容可供搜尋。</span><span class="sxs-lookup"><span data-stu-id="3aa55-152">Makes the text content of a property searchable.</span></span> <span data-ttu-id="3aa55-153">屬性內容會包含在全文檢索索引中。</span><span class="sxs-lookup"><span data-stu-id="3aa55-153">Property contents are included in the full-text index.</span></span> | <span data-ttu-id="3aa55-154">若屬性為 **title**， **企業** 查詢會傳回包含 word Enterprise 的任何文字或標題中的 word **enterprise** 的查詢。</span><span class="sxs-lookup"><span data-stu-id="3aa55-154">If the property is **title**, a query for **Enterprise** returns answers that contain the word **Enterprise** in any text or title.</span></span>
<span data-ttu-id="3aa55-155">可</span><span class="sxs-lookup"><span data-stu-id="3aa55-155">QUERYABLE</span></span> | <span data-ttu-id="3aa55-156">依查詢搜尋特定屬性的相符。</span><span class="sxs-lookup"><span data-stu-id="3aa55-156">Searches by query for a match for a particular property.</span></span> <span data-ttu-id="3aa55-157">您可以在查詢中以程式設計方式或逐字方式指定屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="3aa55-157">The property name can then be specified in the query either programmatically or verbatim.</span></span> |  <span data-ttu-id="3aa55-158">若 **Title** 屬性是可查詢的，則支援查詢 **標題： Enterprise** 。</span><span class="sxs-lookup"><span data-stu-id="3aa55-158">If the **Title** property is queryable, then the query **Title: Enterprise** is supported.</span></span>
<span data-ttu-id="3aa55-159">檢索</span><span class="sxs-lookup"><span data-stu-id="3aa55-159">RETRIEVABLE</span></span> | <span data-ttu-id="3aa55-160">在結果類型中只能使用可檢索的屬性，並顯示在搜尋結果中。</span><span class="sxs-lookup"><span data-stu-id="3aa55-160">Only retrievable properties can be used in the result type and display in the search result.</span></span> |

<span data-ttu-id="3aa55-161">針對所有連接器，必須手動設定自訂類型。</span><span class="sxs-lookup"><span data-stu-id="3aa55-161">For all connectors, custom types must be set manually.</span></span> <span data-ttu-id="3aa55-162">若要啟動每個欄位的搜尋功能，您需要對應至屬性清單的搜尋架構。</span><span class="sxs-lookup"><span data-stu-id="3aa55-162">To activate search capabilities for each field, you need a search schema mapped to a list of properties.</span></span> <span data-ttu-id="3aa55-163">連接嚮導會根據您所選擇的來源屬性集，自動選取搜尋架構。</span><span class="sxs-lookup"><span data-stu-id="3aa55-163">The connection wizard automatically selects a search schema based on the set of source properties you choose.</span></span> <span data-ttu-id="3aa55-164">您可以在 [搜尋架構] 頁面中選取每個屬性和屬性的核取方塊，以修改此架構。</span><span class="sxs-lookup"><span data-stu-id="3aa55-164">You can modify this schema by selecting the check boxes for each property and attribute in the search schema page.</span></span>

![您可以新增或移除查詢、搜尋及檢索功能，以自訂連接器的架構。](media/manageschema.png)

#### <a name="restrictions-and-recommendations-for-search-schema-settings"></a><span data-ttu-id="3aa55-166">搜尋架構設定的限制與建議</span><span class="sxs-lookup"><span data-stu-id="3aa55-166">Restrictions and recommendations for search schema settings</span></span>

* <span data-ttu-id="3aa55-167">**Content**屬性僅可供搜尋。</span><span class="sxs-lookup"><span data-stu-id="3aa55-167">The **content** property is searchable only.</span></span> <span data-ttu-id="3aa55-168">在下拉式清單中選取此屬性後，就無法將此屬性標示為可 **檢索** 或可 **查詢**。</span><span class="sxs-lookup"><span data-stu-id="3aa55-168">Once selected in the dropdown, this property cannot be marked **retrievable** or **queryable**.</span></span> <span data-ttu-id="3aa55-169">使用 **content** 屬性來呈現搜尋結果時，會發生重大效能問題。</span><span class="sxs-lookup"><span data-stu-id="3aa55-169">Significant performance issues occur when search results render with the **content** property.</span></span> <span data-ttu-id="3aa55-170">範例是[ServiceNow](https://www.servicenow.com)知識文庫文章的 [**文字**內容] 欄位。</span><span class="sxs-lookup"><span data-stu-id="3aa55-170">An example is the **Text** content field for a [ServiceNow](https://www.servicenow.com) knowledge-base article.</span></span>

* <span data-ttu-id="3aa55-171">在搜尋結果中，只有標示為可檢索的屬性，而且可以用來 (MRTs) 建立新式結果類型。</span><span class="sxs-lookup"><span data-stu-id="3aa55-171">Only properties marked as retrievable render in the search results and can be used to create modern result types (MRTs).</span></span>

* <span data-ttu-id="3aa55-172">只能將字串屬性標示為可搜尋。</span><span class="sxs-lookup"><span data-stu-id="3aa55-172">Only string properties can be marked searchable.</span></span>


> [!Note]
> <span data-ttu-id="3aa55-173">建立連線之後，就 **無法** 修改架構。</span><span class="sxs-lookup"><span data-stu-id="3aa55-173">After you create a connection, you **can't** modify the schema.</span></span> <span data-ttu-id="3aa55-174">若要這麼做，您必須刪除您的連線，並建立新的連線。</span><span class="sxs-lookup"><span data-stu-id="3aa55-174">To do that, you need to delete your connection and create a new one.</span></span>

### <a name="manage-search-permissions"></a><span data-ttu-id="3aa55-175">管理搜尋許可權</span><span class="sxs-lookup"><span data-stu-id="3aa55-175">Manage search permissions</span></span>

<span data-ttu-id="3aa55-176"> (ACLs 的存取控制清單) 決定組織中的哪些使用者可以存取每個資料項目目。</span><span class="sxs-lookup"><span data-stu-id="3aa55-176">Access Control Lists (ACLs) determine which users in your organization can access each item of data.</span></span> <span data-ttu-id="3aa55-177">所有的連接器都支援所有使用者皆可看到的搜尋許可權。</span><span class="sxs-lookup"><span data-stu-id="3aa55-177">All the connectors support search permissions that are visible to all users.</span></span>

### <a name="set-the-refresh-schedule"></a><span data-ttu-id="3aa55-178">設定重新整理排程</span><span class="sxs-lookup"><span data-stu-id="3aa55-178">Set the refresh schedule</span></span>

<span data-ttu-id="3aa55-179">重新整理排程會決定您的資料與 Microsoft Graph 和 Microsoft 搜尋中的索引同步處理的頻率。</span><span class="sxs-lookup"><span data-stu-id="3aa55-179">The refresh schedule determines how often your data is synced with the index in Microsoft Graph and Microsoft Search.</span></span> <span data-ttu-id="3aa55-180">您可以透過兩種方式排程重新整理：完整編目或累加編目。</span><span class="sxs-lookup"><span data-stu-id="3aa55-180">You can schedule the refresh in two ways: full crawl or incremental crawl.</span></span>

<span data-ttu-id="3aa55-181">使用 **完整**編目時，搜尋引擎會處理及索引內容來源中的每個專案，而不論先前的編目。</span><span class="sxs-lookup"><span data-stu-id="3aa55-181">With a **full crawl**, the search engine processes and indexes every item in the content source, regardless of previous crawls.</span></span> <span data-ttu-id="3aa55-182">在下列情況下，完整編目的運作方式最為好：</span><span class="sxs-lookup"><span data-stu-id="3aa55-182">Full crawl works best in these situations:</span></span>

* <span data-ttu-id="3aa55-183">偵測資料刪除。</span><span class="sxs-lookup"><span data-stu-id="3aa55-183">Detecting deletions of data.</span></span>
* <span data-ttu-id="3aa55-184">增量式編目無法編目錯誤的內容。</span><span class="sxs-lookup"><span data-stu-id="3aa55-184">The incremental crawl failed to crawl content for errors.</span></span>
* <span data-ttu-id="3aa55-185">已修改 ACLs。</span><span class="sxs-lookup"><span data-stu-id="3aa55-185">ACLs were modified.</span></span>
* <span data-ttu-id="3aa55-186">已修改編目規則。</span><span class="sxs-lookup"><span data-stu-id="3aa55-186">Crawl rules were modified.</span></span>
* <span data-ttu-id="3aa55-187">Microsoft 搜尋的軟體更新是必要的。</span><span class="sxs-lookup"><span data-stu-id="3aa55-187">A software update for Microsoft Search is required.</span></span> <span data-ttu-id="3aa55-188">更新會修改搜尋架構。</span><span class="sxs-lookup"><span data-stu-id="3aa55-188">Updates modify the search schema.</span></span>

<span data-ttu-id="3aa55-189">使用累加編目 **時，搜尋**引擎只可以處理和編制自上次成功編目之後所建立或修改的專案。</span><span class="sxs-lookup"><span data-stu-id="3aa55-189">With an **incremental crawl**, the search engine can process and index only the items that were created or modified since the last successful crawl.</span></span> <span data-ttu-id="3aa55-190">因此，不會重新索引內容來源中的所有資料。</span><span class="sxs-lookup"><span data-stu-id="3aa55-190">Therefore, not all the data in the content source is re-indexed.</span></span> <span data-ttu-id="3aa55-191">增量式編目最適合偵測內容、中繼資料、許可權及其他更新。</span><span class="sxs-lookup"><span data-stu-id="3aa55-191">Incremental crawls work best to detect content, metadata, permission, and other updates.</span></span>

<span data-ttu-id="3aa55-192">因為未處理未變更的專案，所以增量編目的速度會比完全編目快許多。</span><span class="sxs-lookup"><span data-stu-id="3aa55-192">Incremental crawls are much faster than full crawls because unchanged items aren’t processed.</span></span> <span data-ttu-id="3aa55-193">若要維護內容來源與搜尋索引之間的準確資料同步處理，您必須定期執行這兩個編目。</span><span class="sxs-lookup"><span data-stu-id="3aa55-193">To maintain an accurate data sync between the content source and the search index, you need to run both crawls periodically.</span></span>

<span data-ttu-id="3aa55-194">每個連接器都會有一組不同的最佳重新整理排程，取決於修改資料的頻率及修改的類型。</span><span class="sxs-lookup"><span data-stu-id="3aa55-194">Each connector will have a different optimal set of refresh schedules based on how often data is modified and the type of modifications.</span></span>

![累加編目和完整編目間隔設定會顯示增量為15分鐘，在1周完全編目。](media/refreshschedule.png)

### <a name="review-connector-settings"></a><span data-ttu-id="3aa55-196">檢查連接器設定</span><span class="sxs-lookup"><span data-stu-id="3aa55-196">Review connector settings</span></span>

<span data-ttu-id="3aa55-197">設定連接器之後，系統 [管理中心](https://admin.microsoft.com) 會帶您前往可供您複查設定的頁面。</span><span class="sxs-lookup"><span data-stu-id="3aa55-197">After you configure your connector, the [admin center](https://admin.microsoft.com) takes you to a page where you can review your settings.</span></span> <span data-ttu-id="3aa55-198">您可以回到設定程式來編輯任何設定，再確認連接。</span><span class="sxs-lookup"><span data-stu-id="3aa55-198">You can go back through the configuration process to edit any setting before you confirm the connection.</span></span> <span data-ttu-id="3aa55-199">若要深入瞭解，請參閱 [管理您的連接器](manage-connector.md)。</span><span class="sxs-lookup"><span data-stu-id="3aa55-199">To learn more, see [Manage your connector](manage-connector.md).</span></span>

## <a name="next-steps-customize-the-search-results-page"></a><span data-ttu-id="3aa55-200">後續步驟：自訂搜尋結果頁面</span><span class="sxs-lookup"><span data-stu-id="3aa55-200">Next steps: Customize the search results page</span></span>

<span data-ttu-id="3aa55-201">透過 Microsoft Search 使用者介面 (UI) ，您的使用者可以從您的 [microsoft 365](https://www.microsoft.com/microsoft-365) 生產力應用程式和更廣泛的 microsoft 生態應用程式中搜尋內容。</span><span class="sxs-lookup"><span data-stu-id="3aa55-201">With the Microsoft Search user interface (UI), your end users can search content from your [Microsoft 365](https://www.microsoft.com/microsoft-365) productivity apps and the broader Microsoft ecosystem.</span></span> <span data-ttu-id="3aa55-202">搜尋類別是指使用者在 [SharePoint](https://sharepoint.com/)、 [Microsoft Office](https://Office.com)及 [Bing](https://Bing.com)中的 microsoft 搜尋中查看其搜尋結果時所顯示的索引標籤。</span><span class="sxs-lookup"><span data-stu-id="3aa55-202">A search vertical refers to the tabs that are shown when a user views their search results in [SharePoint](https://sharepoint.com/), [Microsoft Office](https://Office.com), and Microsoft Search in [Bing](https://Bing.com).</span></span> <span data-ttu-id="3aa55-203">您可以自訂搜尋範圍來縮小結果，如此只會顯示特定類型的搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="3aa55-203">You can customize search verticals to narrow down results, so that only a certain type of search results is displayed.</span></span> <span data-ttu-id="3aa55-204">這些縱向顯示為搜尋結果頁面頂端的 tab 鍵。</span><span class="sxs-lookup"><span data-stu-id="3aa55-204">These verticals appear as a tab on the top of the search results page.</span></span> <span data-ttu-id="3aa55-205"> (MRT.LOG) 的現代結果類型是指定結果呈現方式的 UI。</span><span class="sxs-lookup"><span data-stu-id="3aa55-205">A modern result type (MRT) is the UI that designates how results are presented.</span></span>

<span data-ttu-id="3aa55-206">建立您自己的行業和結果類型，讓使用者可以從新的連線中查看搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="3aa55-206">Create your own verticals and result types, so end users can view search results from new connections.</span></span> <span data-ttu-id="3aa55-207">在此步驟中，您的連線中的資料不會顯示在搜尋結果頁面上。</span><span class="sxs-lookup"><span data-stu-id="3aa55-207">Without this step, data from your connection won’t show up on the search results page.</span></span>

<span data-ttu-id="3aa55-208">若要深入瞭解如何建立您的行業和 MRTs，請參閱 [搜尋結果頁面自訂](customize-search-page.md)。</span><span class="sxs-lookup"><span data-stu-id="3aa55-208">To learn more about how to create your verticals and MRTs, see [Search results page customization](customize-search-page.md).</span></span>

## <a name="how-do-i-know-the-connection-setup-worked"></a><span data-ttu-id="3aa55-209">如何知道連線設定是否運作正常？</span><span class="sxs-lookup"><span data-stu-id="3aa55-209">How do I know the connection setup worked?</span></span>

<span data-ttu-id="3aa55-210">在系統[管理中心](https://admin.microsoft.com)的 [**連接器**] 索引標籤下，移至您發佈的連線清單。</span><span class="sxs-lookup"><span data-stu-id="3aa55-210">Go to the list of your published connections under the **Connectors** tab in the [admin center](https://admin.microsoft.com).</span></span> <span data-ttu-id="3aa55-211">若要瞭解如何進行更新和刪除，請參閱 [管理您的連接器](manage-connector.md)。</span><span class="sxs-lookup"><span data-stu-id="3aa55-211">To learn how to make updates and deletions, see [Manage your connector](manage-connector.md).</span></span>
