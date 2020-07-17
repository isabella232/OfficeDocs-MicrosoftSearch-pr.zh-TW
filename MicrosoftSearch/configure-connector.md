---
title: 設定 microsoft 內置的連接器以進行 Microsoft 搜尋
ms.author: mounika.narayanan
author: monaray
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
ms.openlocfilehash: e5b40326bdd83f461e7ce9a45889ad82245e20aa
ms.sourcegitcommit: 68cd28a84df120473270f27e4eb62de9eae455f9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/23/2020
ms.locfileid: "44850887"
---
<!-- markdownlint-disable no-trailing-punctuation -->

# <a name="set-up-your-microsoft-built-connector-for-microsoft-search"></a><span data-ttu-id="109b1-103">設定 microsoft 內建的連接器以進行 Microsoft 搜尋</span><span class="sxs-lookup"><span data-stu-id="109b1-103">Set up your Microsoft-built connector for Microsoft Search</span></span>

<span data-ttu-id="109b1-104">本文將引導您逐步完成設定 Microsoft 內建連接器的步驟。</span><span class="sxs-lookup"><span data-stu-id="109b1-104">This article guides you through the steps of configuring a Microsoft-built connector.</span></span> <span data-ttu-id="109b1-105">它概述在 Microsoft 365 系統[管理中心](https://admin.microsoft.com)中設定連線的流程。</span><span class="sxs-lookup"><span data-stu-id="109b1-105">It outlines the flow of setting up a connection in the Microsoft 365 [admin center](https://admin.microsoft.com).</span></span> <span data-ttu-id="109b1-106">如需如何設定特定 Microsoft 內置連接器的詳細資訊，請參閱下列文章：</span><span class="sxs-lookup"><span data-stu-id="109b1-106">For more details on how to set up specific Microsoft-built connectors, see these articles:</span></span>

* [<span data-ttu-id="109b1-107">Azure Data Lake Storage Gen2</span><span class="sxs-lookup"><span data-stu-id="109b1-107">Azure Data Lake Storage Gen2</span></span>](azure-data-lake-connector.md)
* [<span data-ttu-id="109b1-108">Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="109b1-108">Azure DevOps</span></span>](azure-devops-connector.md)
* [<span data-ttu-id="109b1-109">Azure SQL</span><span class="sxs-lookup"><span data-stu-id="109b1-109">Azure SQL</span></span>](MSSQL-connector.md)
* [<span data-ttu-id="109b1-110">企業網站</span><span class="sxs-lookup"><span data-stu-id="109b1-110">Enterprise websites</span></span>](enterprise-web-connector.md)
* [<span data-ttu-id="109b1-111">檔案共用</span><span class="sxs-lookup"><span data-stu-id="109b1-111">File share</span></span>](file-share-connector.md)
* [<span data-ttu-id="109b1-112">MediaWiki</span><span class="sxs-lookup"><span data-stu-id="109b1-112">MediaWiki</span></span>](mediawiki-connector.md)
* [<span data-ttu-id="109b1-113">Microsoft SQL server</span><span class="sxs-lookup"><span data-stu-id="109b1-113">Microsoft SQL server</span></span>](MSSQL-connector.md)
* [<span data-ttu-id="109b1-114">ServiceNow</span><span class="sxs-lookup"><span data-stu-id="109b1-114">ServiceNow</span></span>](servicenow-connector.md)

## <a name="set-up"></a><span data-ttu-id="109b1-115">設定</span><span class="sxs-lookup"><span data-stu-id="109b1-115">Set up</span></span>

<span data-ttu-id="109b1-116">完成下列步驟以設定任何 Microsoft 建立的連接器。</span><span class="sxs-lookup"><span data-stu-id="109b1-116">Complete the following steps to configure any of the Microsoft-built connectors.</span></span>

1. <span data-ttu-id="109b1-117">移至[Microsoft 365 系統管理中心](https://admin.microsoft.com)中的 [[連接器]](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors)索引標籤。</span><span class="sxs-lookup"><span data-stu-id="109b1-117">Go to the [Connectors tab](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors) in the [Microsoft 365 admin center](https://admin.microsoft.com).</span></span>
2. <span data-ttu-id="109b1-118">使用[Microsoft 365](https://www.microsoft.com/microsoft-365)租使用者的認證登入您的帳戶。</span><span class="sxs-lookup"><span data-stu-id="109b1-118">Sign in to your account with the credentials for your [Microsoft 365](https://www.microsoft.com/microsoft-365) tenant.</span></span>
3. <span data-ttu-id="109b1-119">選取 [**新增連接器**]。</span><span class="sxs-lookup"><span data-stu-id="109b1-119">Select **Add a connector**.</span></span>
4. <span data-ttu-id="109b1-120">從可用的連接器清單中，選取您選擇的連接器。</span><span class="sxs-lookup"><span data-stu-id="109b1-120">From the list of available connectors, select the connector of your choice.</span></span>

![可用的資料來源包括： ADLS Gen2 Connector、Enterprise 網站、ServiceNow、檔案共用、Microsoft SQL server 和 MediaWiki。](media/addconnector_final.png)

### <a name="name-the-connector"></a><span data-ttu-id="109b1-122">命名連接器</span><span class="sxs-lookup"><span data-stu-id="109b1-122">Name the connector</span></span>

<span data-ttu-id="109b1-123">若要建立連接，請先指定下列屬性：</span><span class="sxs-lookup"><span data-stu-id="109b1-123">To create a connection, first specify these attributes:</span></span>

1. <span data-ttu-id="109b1-124">連接的名稱</span><span class="sxs-lookup"><span data-stu-id="109b1-124">Name of the connection</span></span>
2. <span data-ttu-id="109b1-125">連接識別碼</span><span class="sxs-lookup"><span data-stu-id="109b1-125">Connection ID</span></span>
3. <span data-ttu-id="109b1-126">描述（選用）</span><span class="sxs-lookup"><span data-stu-id="109b1-126">Description (optional)</span></span>

<span data-ttu-id="109b1-127">連接識別碼會建立連接器的隱含屬性。</span><span class="sxs-lookup"><span data-stu-id="109b1-127">The connection ID creates implicit properties for your connector.</span></span> <span data-ttu-id="109b1-128">它必須只包含字母數位字元，最多可以有32個字元。</span><span class="sxs-lookup"><span data-stu-id="109b1-128">It must contain only alphanumeric characters and be a maximum of 32 characters.</span></span>

### <a name="connect-to-a-data-source"></a><span data-ttu-id="109b1-129">連接到資料來源</span><span class="sxs-lookup"><span data-stu-id="109b1-129">Connect to a data source</span></span>

<span data-ttu-id="109b1-130">資料連線過程會根據連接器類型而有所不同。</span><span class="sxs-lookup"><span data-stu-id="109b1-130">The data connection process varies based on the type of connector.</span></span> <span data-ttu-id="109b1-131">若要深入瞭解如何連線至您的內部部署資料來源，請參閱[安裝內部部署資料閘道](https://aka.ms/configuregateway)。</span><span class="sxs-lookup"><span data-stu-id="109b1-131">To learn more about connecting to your on-premises data source, see [Install an on-premises data gateway](https://aka.ms/configuregateway).</span></span>

### <a name="select-source-properties"></a><span data-ttu-id="109b1-132">選取來源屬性</span><span class="sxs-lookup"><span data-stu-id="109b1-132">Select source properties</span></span>

<span data-ttu-id="109b1-133">協力廠商資料來源所設定的資料欄位會在 Microsoft 搜尋中編入來源屬性。</span><span class="sxs-lookup"><span data-stu-id="109b1-133">The data fields set by your third-party data source as source properties are indexed into Microsoft Search.</span></span> <span data-ttu-id="109b1-134">若要修改這些屬性，請選取 [**連接器**] 頁面右邊的側欄中的 [**編輯屬性**]。</span><span class="sxs-lookup"><span data-stu-id="109b1-134">To modify these properties, select **Edit properties** in the side bar on the right of the **Connectors** page.</span></span> <span data-ttu-id="109b1-135">您**最多可以選擇64來源屬性**。</span><span class="sxs-lookup"><span data-stu-id="109b1-135">You can select **up to 64 source properties**.</span></span>

### <a name="manage-the-search-schema"></a><span data-ttu-id="109b1-136">管理搜尋結構描述</span><span class="sxs-lookup"><span data-stu-id="109b1-136">Manage the search schema</span></span>

<span data-ttu-id="109b1-137">系統管理員可以設定搜尋架構屬性，以控制每個來源屬性的搜尋功能。</span><span class="sxs-lookup"><span data-stu-id="109b1-137">Admins can set the search schema attributes to control search functionality of each source property.</span></span> <span data-ttu-id="109b1-138">搜尋架構可協助決定搜尋結果頁面上顯示的結果，以及使用者可以查看和存取哪些資訊。</span><span class="sxs-lookup"><span data-stu-id="109b1-138">A search schema helps determine what results display on the search results page and what information end users can view and access.</span></span>

<span data-ttu-id="109b1-139">搜尋架構屬性包括可搜尋、可**查詢**及可**供\*\*\*\*檢索**的屬性。</span><span class="sxs-lookup"><span data-stu-id="109b1-139">Search schema attributes include **searchable**, **queryable**, and **retrievable**.</span></span> <span data-ttu-id="109b1-140">下表列出 Microsoft Graph 連接器所支援的每個屬性，並說明其功能。</span><span class="sxs-lookup"><span data-stu-id="109b1-140">The following table lists each of the attributes that Microsoft Graph connectors support and explains their functions.</span></span>

<span data-ttu-id="109b1-141">搜尋架構屬性</span><span class="sxs-lookup"><span data-stu-id="109b1-141">Search schema attribute</span></span> | <span data-ttu-id="109b1-142">函數</span><span class="sxs-lookup"><span data-stu-id="109b1-142">Function</span></span> | <span data-ttu-id="109b1-143">範例</span><span class="sxs-lookup"><span data-stu-id="109b1-143">Example</span></span>
--- | --- | ---
<span data-ttu-id="109b1-144">搜索</span><span class="sxs-lookup"><span data-stu-id="109b1-144">SEARCHABLE</span></span> | <span data-ttu-id="109b1-145">使屬性的文字內容可供搜尋。</span><span class="sxs-lookup"><span data-stu-id="109b1-145">Makes the text content of a property searchable.</span></span> <span data-ttu-id="109b1-146">屬性內容會包含在全文檢索索引中。</span><span class="sxs-lookup"><span data-stu-id="109b1-146">Property contents are included in the full-text index.</span></span> | <span data-ttu-id="109b1-147">若屬性為**title**，**企業**查詢會傳回包含 word Enterprise 的任何文字或標題中的 word **enterprise**的查詢。</span><span class="sxs-lookup"><span data-stu-id="109b1-147">If the property is **title**, a query for **Enterprise** returns answers that contain the word **Enterprise** in any text or title.</span></span>
<span data-ttu-id="109b1-148">可</span><span class="sxs-lookup"><span data-stu-id="109b1-148">QUERYABLE</span></span> | <span data-ttu-id="109b1-149">依查詢搜尋特定屬性的相符。</span><span class="sxs-lookup"><span data-stu-id="109b1-149">Searches by query for a match for a particular property.</span></span> <span data-ttu-id="109b1-150">您可以在查詢中以程式設計方式或逐字方式指定屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="109b1-150">The property name can then be specified in the query either programmatically or verbatim.</span></span> |  <span data-ttu-id="109b1-151">若**Title**屬性是可查詢的，則支援查詢**標題： Enterprise** 。</span><span class="sxs-lookup"><span data-stu-id="109b1-151">If the **Title** property is queryable, then the query **Title: Enterprise** is supported.</span></span>
<span data-ttu-id="109b1-152">檢索</span><span class="sxs-lookup"><span data-stu-id="109b1-152">RETRIEVABLE</span></span> | <span data-ttu-id="109b1-153">在結果類型中只能使用可檢索的屬性，並顯示在搜尋結果中。</span><span class="sxs-lookup"><span data-stu-id="109b1-153">Only retrievable properties can be used in the result type and display in the search result.</span></span> |

<span data-ttu-id="109b1-154">針對除檔案共用連接器以外的所有連接器，必須手動設定自訂類型。</span><span class="sxs-lookup"><span data-stu-id="109b1-154">For all connectors except the file share connector, custom types must be set manually.</span></span> <span data-ttu-id="109b1-155">若要啟動每個欄位的搜尋功能，您需要對應至屬性清單的搜尋架構。</span><span class="sxs-lookup"><span data-stu-id="109b1-155">To activate search capabilities for each field, you need a search schema mapped to a list of properties.</span></span> <span data-ttu-id="109b1-156">連接嚮導會根據您所選擇的來源屬性集，自動選取搜尋架構。</span><span class="sxs-lookup"><span data-stu-id="109b1-156">The connection wizard automatically selects a search schema based on the set of source properties you choose.</span></span> <span data-ttu-id="109b1-157">您可以在 [搜尋架構] 頁面中選取每個屬性和屬性的核取方塊，以修改此架構。</span><span class="sxs-lookup"><span data-stu-id="109b1-157">You can modify this schema by selecting the check boxes for each property and attribute in the search schema page.</span></span>

![您可以新增或移除查詢、搜尋及檢索功能，以自訂連接器的架構。](media/manageschema.png)

<span data-ttu-id="109b1-159">這些限制和建議適用于搜尋架構設定：</span><span class="sxs-lookup"><span data-stu-id="109b1-159">These restrictions and recommendations apply to search schema settings:</span></span>

* <span data-ttu-id="109b1-160">針對索引自訂類型的連接器，建議您不要**標示包含**主要內容可**檢索**的欄位。</span><span class="sxs-lookup"><span data-stu-id="109b1-160">For connectors that index custom types, we recommend that you **do not** mark the field that contains the main content **retrievable**.</span></span> <span data-ttu-id="109b1-161">使用該搜尋屬性呈現搜尋結果時，會發生重大效能問題。</span><span class="sxs-lookup"><span data-stu-id="109b1-161">Significant performance issues occur when search results render with that search attribute.</span></span> <span data-ttu-id="109b1-162">範例是[ServiceNow](https://www.servicenow.com)知識文庫文章的 [**文字**內容] 欄位。</span><span class="sxs-lookup"><span data-stu-id="109b1-162">An example is the **Text** content field for a [ServiceNow](https://www.servicenow.com) knowledge-base article.</span></span>
* <span data-ttu-id="109b1-163">在搜尋結果中，只會標示為可檢索的屬性，並可用來建立新式的結果類型（MRTs）。</span><span class="sxs-lookup"><span data-stu-id="109b1-163">Only properties marked as retrievable render in the search results and can be used to create modern result types (MRTs).</span></span>
* <span data-ttu-id="109b1-164">只能將字串屬性標示為可搜尋。</span><span class="sxs-lookup"><span data-stu-id="109b1-164">Only string properties can be marked searchable.</span></span>

> [!Note]
> <span data-ttu-id="109b1-165">建立連線之後，就**無法**修改架構。</span><span class="sxs-lookup"><span data-stu-id="109b1-165">After you create a connection, you **can't** modify the schema.</span></span> <span data-ttu-id="109b1-166">若要這麼做，您必須刪除您的連線，並建立新的連線。</span><span class="sxs-lookup"><span data-stu-id="109b1-166">To do that, you need to delete your connection and create a new one.</span></span>

### <a name="manage-search-permissions"></a><span data-ttu-id="109b1-167">管理搜尋許可權</span><span class="sxs-lookup"><span data-stu-id="109b1-167">Manage search permissions</span></span>

<span data-ttu-id="109b1-168">存取控制清單（ACLs）決定組織中的哪些使用者可以存取每個資料項目目。</span><span class="sxs-lookup"><span data-stu-id="109b1-168">Access Control Lists (ACLs) determine which users in your organization can access each item of data.</span></span> <span data-ttu-id="109b1-169">檔案共用連接器只支援可對應至[Azure Active Directory （AZURE AD）](https://docs.microsoft.com/azure/active-directory/)的 ACLs。</span><span class="sxs-lookup"><span data-stu-id="109b1-169">The file share connector supports only ACLs that can be mapped to [Azure Active Directory (Azure AD)](https://docs.microsoft.com/azure/active-directory/).</span></span> <span data-ttu-id="109b1-170">所有其他連接器都支援所有使用者均可看到的搜尋許可權。</span><span class="sxs-lookup"><span data-stu-id="109b1-170">All the other connectors support search permissions that are visible to all users.</span></span>

### <a name="set-the-refresh-schedule"></a><span data-ttu-id="109b1-171">設定重新整理排程</span><span class="sxs-lookup"><span data-stu-id="109b1-171">Set the refresh schedule</span></span>

<span data-ttu-id="109b1-172">重新整理排程會決定您的資料與 Microsoft Graph 和 Microsoft 搜尋中的索引同步處理的頻率。</span><span class="sxs-lookup"><span data-stu-id="109b1-172">The refresh schedule determines how often your data is synced with the index in Microsoft Graph and Microsoft Search.</span></span> <span data-ttu-id="109b1-173">您可以透過兩種方式排程重新整理：完整編目或累加編目。</span><span class="sxs-lookup"><span data-stu-id="109b1-173">You can schedule the refresh in two ways: full crawl or incremental crawl.</span></span>

<span data-ttu-id="109b1-174">使用**完整**編目時，搜尋引擎會處理及索引內容來源中的每個專案，而不論先前的編目。</span><span class="sxs-lookup"><span data-stu-id="109b1-174">With a **full crawl**, the search engine processes and indexes every item in the content source, regardless of previous crawls.</span></span> <span data-ttu-id="109b1-175">在下列情況下，完整編目的運作方式最為好：</span><span class="sxs-lookup"><span data-stu-id="109b1-175">Full crawl works best in these situations:</span></span>

* <span data-ttu-id="109b1-176">您必須偵測資料刪除。</span><span class="sxs-lookup"><span data-stu-id="109b1-176">You need to detect deletions of data.</span></span>
* <span data-ttu-id="109b1-177">增量式編目無法編目錯誤的內容。</span><span class="sxs-lookup"><span data-stu-id="109b1-177">The incremental crawl failed to crawl content for errors.</span></span>
* <span data-ttu-id="109b1-178">Microsoft 搜尋的軟體更新是必要的。</span><span class="sxs-lookup"><span data-stu-id="109b1-178">A software update for Microsoft Search is required.</span></span> <span data-ttu-id="109b1-179">更新會修改搜尋架構。</span><span class="sxs-lookup"><span data-stu-id="109b1-179">Updates modify the search schema.</span></span>
* <span data-ttu-id="109b1-180">已修改 ACLs。</span><span class="sxs-lookup"><span data-stu-id="109b1-180">ACLs were modified.</span></span>
* <span data-ttu-id="109b1-181">已修改編目規則。</span><span class="sxs-lookup"><span data-stu-id="109b1-181">Crawl rules were modified.</span></span>

<span data-ttu-id="109b1-182">使用累加編目**時，搜尋**引擎只可以處理和編制自上次成功編目之後所建立或修改的專案。</span><span class="sxs-lookup"><span data-stu-id="109b1-182">With an **incremental crawl**, the search engine can process and index only the items that were created or modified since the last successful crawl.</span></span> <span data-ttu-id="109b1-183">因此，不會重新索引內容來源中的所有資料。</span><span class="sxs-lookup"><span data-stu-id="109b1-183">Therefore, not all the data in the content source is re-indexed.</span></span> <span data-ttu-id="109b1-184">增量式編目最適合偵測內容、中繼資料、許可權及其他更新。</span><span class="sxs-lookup"><span data-stu-id="109b1-184">Incremental crawls works best to detect content, metadata, permission, and other updates.</span></span>

<span data-ttu-id="109b1-185">因為未處理未變更的專案，所以增量編目的速度會比完全編目快許多。</span><span class="sxs-lookup"><span data-stu-id="109b1-185">Incremental crawls are much faster than full crawls because unchanged items aren’t processed.</span></span> <span data-ttu-id="109b1-186">若要維護內容來源與搜尋索引之間的準確資料同步處理，您必須定期執行這兩個編目。</span><span class="sxs-lookup"><span data-stu-id="109b1-186">To maintain an accurate data sync between the content source and the search index, you need to run both crawls periodically.</span></span>

<span data-ttu-id="109b1-187">每個連接器都會有一組不同的最佳重新整理排程，取決於修改資料的頻率及修改的類型。</span><span class="sxs-lookup"><span data-stu-id="109b1-187">Each connector will have a different optimal set of refresh schedules based on how often data is modified and the type of modifications.</span></span>

![累加編目和完整編目間隔設定會顯示增量為15分鐘，在1周完全編目。](media/refreshschedule.png)

### <a name="review-connector-settings"></a><span data-ttu-id="109b1-189">檢查連接器設定</span><span class="sxs-lookup"><span data-stu-id="109b1-189">Review connector settings</span></span>

<span data-ttu-id="109b1-190">設定連接器之後，系統[管理中心](https://admin.microsoft.com)會帶您前往可供您複查設定的頁面。</span><span class="sxs-lookup"><span data-stu-id="109b1-190">After you configure your connector, the [admin center](https://admin.microsoft.com) takes you to a page where you can review your settings.</span></span> <span data-ttu-id="109b1-191">您可以回到設定程式來編輯任何設定，再確認連接。</span><span class="sxs-lookup"><span data-stu-id="109b1-191">You can go back through the configuration process to edit any setting before you confirm the connection.</span></span> <span data-ttu-id="109b1-192">若要深入瞭解，請參閱[管理您的連接器](manage-connector.md)。</span><span class="sxs-lookup"><span data-stu-id="109b1-192">To learn more, see [Manage your connector](manage-connector.md).</span></span>

## <a name="next-steps-customize-the-search-results-page"></a><span data-ttu-id="109b1-193">後續步驟：自訂搜尋結果頁面</span><span class="sxs-lookup"><span data-stu-id="109b1-193">Next steps: Customize the search results page</span></span>

<span data-ttu-id="109b1-194">透過 Microsoft Search 使用者介面（UI），您的使用者可以從您的[microsoft 365](https://www.microsoft.com/microsoft-365)生產力應用程式和更廣泛的 microsoft 體系中搜尋內容。</span><span class="sxs-lookup"><span data-stu-id="109b1-194">With the Microsoft Search user interface (UI), your end users can search content from your [Microsoft 365](https://www.microsoft.com/microsoft-365) productivity apps and the broader Microsoft ecosystem.</span></span> <span data-ttu-id="109b1-195">搜尋類別是指使用者在[SharePoint](https://sharepoint.com/)、 [Microsoft Office](https://Office.com)及[Bing](https://Bing.com)中的 microsoft 搜尋中查看其搜尋結果時所顯示的索引標籤。</span><span class="sxs-lookup"><span data-stu-id="109b1-195">A search vertical refers to the tabs that are shown when a user views their search results in [SharePoint](https://sharepoint.com/), [Microsoft Office](https://Office.com), and Microsoft Search in [Bing](https://Bing.com).</span></span> <span data-ttu-id="109b1-196">您可以自訂搜尋範圍來縮小結果，如此只會顯示特定類型的搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="109b1-196">You can customize search verticals to narrow down results, so that only a certain type of search results is displayed.</span></span> <span data-ttu-id="109b1-197">這些縱向顯示為搜尋結果頁面頂端的 tab 鍵。</span><span class="sxs-lookup"><span data-stu-id="109b1-197">These verticals appear as a tab on the top of the search results page.</span></span> <span data-ttu-id="109b1-198">現代結果類型（MRT.LOG）是指定結果呈現方式的 UI。</span><span class="sxs-lookup"><span data-stu-id="109b1-198">A modern result type (MRT) is the UI that designates how results are presented.</span></span>

<span data-ttu-id="109b1-199">您必須建立自己的行業和結果類型，讓使用者可以從新的連線中查看搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="109b1-199">You must create your own verticals and result types, so end users can view search results from new connections.</span></span> <span data-ttu-id="109b1-200">在此步驟中，您的連線中的資料不會顯示在搜尋結果頁面上。</span><span class="sxs-lookup"><span data-stu-id="109b1-200">Without this step, data from your connection won’t show up on the search results page.</span></span>

<span data-ttu-id="109b1-201">若要深入瞭解如何建立您的行業和 MRTs，請參閱[搜尋結果頁面自訂](customize-search-page.md)。</span><span class="sxs-lookup"><span data-stu-id="109b1-201">To learn more about how to create your verticals and MRTs, see [Search results page customization](customize-search-page.md).</span></span>

## <a name="how-do-i-know-this-worked"></a><span data-ttu-id="109b1-202">如何知道這是否正常運作？</span><span class="sxs-lookup"><span data-stu-id="109b1-202">How do I know this worked?</span></span>

<span data-ttu-id="109b1-203">在系統[管理中心](https://admin.microsoft.com)的 [**連接器**] 索引標籤下，移至您發佈的連線清單。</span><span class="sxs-lookup"><span data-stu-id="109b1-203">Go to the list of your published connections under the **Connectors** tab in the [admin center](https://admin.microsoft.com).</span></span> <span data-ttu-id="109b1-204">若要瞭解如何進行更新和刪除，請參閱[管理您的連接器](manage-connector.md)。</span><span class="sxs-lookup"><span data-stu-id="109b1-204">To learn how to make updates and deletions, see [Manage your connector](manage-connector.md).</span></span>
