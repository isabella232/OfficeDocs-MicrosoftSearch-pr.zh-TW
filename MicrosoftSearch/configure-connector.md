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
ms.openlocfilehash: 30c60e94e8e633bce90bbc1984eee35d3ceda771
ms.sourcegitcommit: f2323c43fc732890213223efac32006df5b92c28
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/23/2020
ms.locfileid: "45387967"
---
<!-- markdownlint-disable no-trailing-punctuation -->

# <a name="set-up-your-microsoft-built-connector-for-microsoft-search"></a><span data-ttu-id="7258e-103">設定 microsoft 內建的連接器以進行 Microsoft 搜尋</span><span class="sxs-lookup"><span data-stu-id="7258e-103">Set up your Microsoft-built connector for Microsoft Search</span></span>

<span data-ttu-id="7258e-104">本文將引導您逐步完成設定 Microsoft 內建連接器的步驟。</span><span class="sxs-lookup"><span data-stu-id="7258e-104">This article guides you through the steps of configuring a Microsoft-built connector.</span></span> <span data-ttu-id="7258e-105">它概述在 Microsoft 365 系統[管理中心](https://admin.microsoft.com)中設定連線的流程。</span><span class="sxs-lookup"><span data-stu-id="7258e-105">It outlines the flow of setting up a connection in the Microsoft 365 [admin center](https://admin.microsoft.com).</span></span> <span data-ttu-id="7258e-106">如需如何設定特定 Microsoft 內置連接器的詳細資訊，請參閱下列文章：</span><span class="sxs-lookup"><span data-stu-id="7258e-106">For more information on how to set up specific Microsoft-built connectors, see these articles:</span></span>

* [<span data-ttu-id="7258e-107">Azure Data Lake Storage Gen2</span><span class="sxs-lookup"><span data-stu-id="7258e-107">Azure Data Lake Storage Gen2</span></span>](azure-data-lake-connector.md)
* [<span data-ttu-id="7258e-108">Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="7258e-108">Azure DevOps</span></span>](azure-devops-connector.md)
* [<span data-ttu-id="7258e-109">Azure SQL</span><span class="sxs-lookup"><span data-stu-id="7258e-109">Azure SQL</span></span>](MSSQL-connector.md)
* [<span data-ttu-id="7258e-110">企業網站</span><span class="sxs-lookup"><span data-stu-id="7258e-110">Enterprise websites</span></span>](enterprise-web-connector.md)
* [<span data-ttu-id="7258e-111">MediaWiki</span><span class="sxs-lookup"><span data-stu-id="7258e-111">MediaWiki</span></span>](mediawiki-connector.md)
* [<span data-ttu-id="7258e-112">Microsoft SQL server</span><span class="sxs-lookup"><span data-stu-id="7258e-112">Microsoft SQL server</span></span>](MSSQL-connector.md)
* [<span data-ttu-id="7258e-113">ServiceNow</span><span class="sxs-lookup"><span data-stu-id="7258e-113">ServiceNow</span></span>](servicenow-connector.md)

## <a name="set-up"></a><span data-ttu-id="7258e-114">設定</span><span class="sxs-lookup"><span data-stu-id="7258e-114">Set up</span></span>

<span data-ttu-id="7258e-115">完成下列步驟以設定任何 Microsoft 建立的連接器。</span><span class="sxs-lookup"><span data-stu-id="7258e-115">Complete the following steps to configure any of the Microsoft-built connectors.</span></span>

1. <span data-ttu-id="7258e-116">移至[Microsoft 365 系統管理中心](https://admin.microsoft.com)中的 [[連接器]](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors)索引標籤。</span><span class="sxs-lookup"><span data-stu-id="7258e-116">Go to the [Connectors tab](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors) in the [Microsoft 365 admin center](https://admin.microsoft.com).</span></span>
2. <span data-ttu-id="7258e-117">使用[Microsoft 365](https://www.microsoft.com/microsoft-365)租使用者的認證登入您的帳戶。</span><span class="sxs-lookup"><span data-stu-id="7258e-117">Sign in to your account with the credentials for your [Microsoft 365](https://www.microsoft.com/microsoft-365) tenant.</span></span>
3. <span data-ttu-id="7258e-118">選取 [**新增連接器**]。</span><span class="sxs-lookup"><span data-stu-id="7258e-118">Select **Add a connector**.</span></span>
4. <span data-ttu-id="7258e-119">從可用的連接器清單中，選取您選擇的連接器。</span><span class="sxs-lookup"><span data-stu-id="7258e-119">From the list of available connectors, select the connector of your choice.</span></span>

![可用的資料來源包括： Azure DevOps Connector、ServiceNow、ADLS Gen2、Enterprise 網站、MediaWiki、Microsoft SQL server 和 Azure SQL。](media/add_connector.png)

### <a name="name-the-connector"></a><span data-ttu-id="7258e-121">命名連接器</span><span class="sxs-lookup"><span data-stu-id="7258e-121">Name the connector</span></span>

<span data-ttu-id="7258e-122">若要建立連接，請先指定下列屬性：</span><span class="sxs-lookup"><span data-stu-id="7258e-122">To create a connection, first specify these attributes:</span></span>

1. <span data-ttu-id="7258e-123">連接的名稱</span><span class="sxs-lookup"><span data-stu-id="7258e-123">Name of the connection</span></span>
2. <span data-ttu-id="7258e-124">連接識別碼</span><span class="sxs-lookup"><span data-stu-id="7258e-124">Connection ID</span></span>
3. <span data-ttu-id="7258e-125">描述（選用）</span><span class="sxs-lookup"><span data-stu-id="7258e-125">Description (optional)</span></span>

<span data-ttu-id="7258e-126">連接識別碼會建立連接器的隱含屬性。</span><span class="sxs-lookup"><span data-stu-id="7258e-126">The connection ID creates implicit properties for your connector.</span></span> <span data-ttu-id="7258e-127">它必須只包含字母數位字元，最多可以有32個字元。</span><span class="sxs-lookup"><span data-stu-id="7258e-127">It must contain only alphanumeric characters and be a maximum of 32 characters.</span></span>

### <a name="connect-to-a-data-source"></a><span data-ttu-id="7258e-128">連接到資料來源</span><span class="sxs-lookup"><span data-stu-id="7258e-128">Connect to a data source</span></span>

<span data-ttu-id="7258e-129">資料連線過程會根據連接器類型而有所不同。</span><span class="sxs-lookup"><span data-stu-id="7258e-129">The data connection process varies based on the type of connector.</span></span> <span data-ttu-id="7258e-130">若要深入瞭解如何連線至您的內部部署資料來源，請參閱[安裝內部部署資料閘道](https://aka.ms/configuregateway)。</span><span class="sxs-lookup"><span data-stu-id="7258e-130">To learn more about connecting to your on-premises data source, see [Install an on-premises data gateway](https://aka.ms/configuregateway).</span></span>

### <a name="select-source-properties"></a><span data-ttu-id="7258e-131">選取來源屬性</span><span class="sxs-lookup"><span data-stu-id="7258e-131">Select source properties</span></span>

<span data-ttu-id="7258e-132">協力廠商資料來源所設定的資料欄位會在 Microsoft 搜尋中編入來源屬性。</span><span class="sxs-lookup"><span data-stu-id="7258e-132">The data fields set by your third-party data source as source properties are indexed into Microsoft Search.</span></span> <span data-ttu-id="7258e-133">若要修改這些屬性，請選取 [**連接器**] 頁面右邊的側欄中的 [**編輯屬性**]。</span><span class="sxs-lookup"><span data-stu-id="7258e-133">To modify these properties, select **Edit properties** in the side bar on the right of the **Connectors** page.</span></span> <span data-ttu-id="7258e-134">您**最多可以選擇64來源屬性**。</span><span class="sxs-lookup"><span data-stu-id="7258e-134">You can select **up to 64 source properties**.</span></span>

### <a name="manage-the-search-schema"></a><span data-ttu-id="7258e-135">管理搜尋結構描述</span><span class="sxs-lookup"><span data-stu-id="7258e-135">Manage the search schema</span></span>

<span data-ttu-id="7258e-136">系統管理員可以設定搜尋架構屬性，以控制每個來源屬性的搜尋功能。</span><span class="sxs-lookup"><span data-stu-id="7258e-136">Admins can set the search schema attributes to control search functionality of each source property.</span></span> <span data-ttu-id="7258e-137">搜尋架構可協助決定搜尋結果頁面上顯示的結果，以及使用者可以查看和存取哪些資訊。</span><span class="sxs-lookup"><span data-stu-id="7258e-137">A search schema helps determine what results display on the search results page and what information end users can view and access.</span></span>

<span data-ttu-id="7258e-138">搜尋架構屬性包括可搜尋、可**查詢**及可**供\*\*\*\*檢索**的屬性。</span><span class="sxs-lookup"><span data-stu-id="7258e-138">Search schema attributes include **searchable**, **queryable**, and **retrievable**.</span></span> <span data-ttu-id="7258e-139">下表列出 Microsoft Graph 連接器所支援的每個屬性，並說明其功能。</span><span class="sxs-lookup"><span data-stu-id="7258e-139">The following table lists each of the attributes that Microsoft Graph connectors support and explains their functions.</span></span>

<span data-ttu-id="7258e-140">搜尋架構屬性</span><span class="sxs-lookup"><span data-stu-id="7258e-140">Search schema attribute</span></span> | <span data-ttu-id="7258e-141">函數</span><span class="sxs-lookup"><span data-stu-id="7258e-141">Function</span></span> | <span data-ttu-id="7258e-142">範例</span><span class="sxs-lookup"><span data-stu-id="7258e-142">Example</span></span>
--- | --- | ---
<span data-ttu-id="7258e-143">搜索</span><span class="sxs-lookup"><span data-stu-id="7258e-143">SEARCHABLE</span></span> | <span data-ttu-id="7258e-144">使屬性的文字內容可供搜尋。</span><span class="sxs-lookup"><span data-stu-id="7258e-144">Makes the text content of a property searchable.</span></span> <span data-ttu-id="7258e-145">屬性內容會包含在全文檢索索引中。</span><span class="sxs-lookup"><span data-stu-id="7258e-145">Property contents are included in the full-text index.</span></span> | <span data-ttu-id="7258e-146">若屬性為**title**，**企業**查詢會傳回包含 word Enterprise 的任何文字或標題中的 word **enterprise**的查詢。</span><span class="sxs-lookup"><span data-stu-id="7258e-146">If the property is **title**, a query for **Enterprise** returns answers that contain the word **Enterprise** in any text or title.</span></span>
<span data-ttu-id="7258e-147">可</span><span class="sxs-lookup"><span data-stu-id="7258e-147">QUERYABLE</span></span> | <span data-ttu-id="7258e-148">依查詢搜尋特定屬性的相符。</span><span class="sxs-lookup"><span data-stu-id="7258e-148">Searches by query for a match for a particular property.</span></span> <span data-ttu-id="7258e-149">您可以在查詢中以程式設計方式或逐字方式指定屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="7258e-149">The property name can then be specified in the query either programmatically or verbatim.</span></span> |  <span data-ttu-id="7258e-150">若**Title**屬性是可查詢的，則支援查詢**標題： Enterprise** 。</span><span class="sxs-lookup"><span data-stu-id="7258e-150">If the **Title** property is queryable, then the query **Title: Enterprise** is supported.</span></span>
<span data-ttu-id="7258e-151">檢索</span><span class="sxs-lookup"><span data-stu-id="7258e-151">RETRIEVABLE</span></span> | <span data-ttu-id="7258e-152">在結果類型中只能使用可檢索的屬性，並顯示在搜尋結果中。</span><span class="sxs-lookup"><span data-stu-id="7258e-152">Only retrievable properties can be used in the result type and display in the search result.</span></span> |

<span data-ttu-id="7258e-153">針對所有連接器，必須手動設定自訂類型。</span><span class="sxs-lookup"><span data-stu-id="7258e-153">For all connectors, custom types must be set manually.</span></span> <span data-ttu-id="7258e-154">若要啟動每個欄位的搜尋功能，您需要對應至屬性清單的搜尋架構。</span><span class="sxs-lookup"><span data-stu-id="7258e-154">To activate search capabilities for each field, you need a search schema mapped to a list of properties.</span></span> <span data-ttu-id="7258e-155">連接嚮導會根據您所選擇的來源屬性集，自動選取搜尋架構。</span><span class="sxs-lookup"><span data-stu-id="7258e-155">The connection wizard automatically selects a search schema based on the set of source properties you choose.</span></span> <span data-ttu-id="7258e-156">您可以在 [搜尋架構] 頁面中選取每個屬性和屬性的核取方塊，以修改此架構。</span><span class="sxs-lookup"><span data-stu-id="7258e-156">You can modify this schema by selecting the check boxes for each property and attribute in the search schema page.</span></span>

![您可以新增或移除查詢、搜尋及檢索功能，以自訂連接器的架構。](media/manageschema.png)

<span data-ttu-id="7258e-158">這些限制和建議適用于搜尋架構設定：</span><span class="sxs-lookup"><span data-stu-id="7258e-158">These restrictions and recommendations apply to search schema settings:</span></span>

* <span data-ttu-id="7258e-159">針對索引自訂類型的連接器，建議您不要**標示包含**主要內容可**檢索**的欄位。</span><span class="sxs-lookup"><span data-stu-id="7258e-159">For connectors that index custom types, we recommend that you **do not** mark the field that contains the main content **retrievable**.</span></span> <span data-ttu-id="7258e-160">使用該搜尋屬性呈現搜尋結果時，會發生重大效能問題。</span><span class="sxs-lookup"><span data-stu-id="7258e-160">Significant performance issues occur when search results render with that search attribute.</span></span> <span data-ttu-id="7258e-161">範例是[ServiceNow](https://www.servicenow.com)知識文庫文章的 [**文字**內容] 欄位。</span><span class="sxs-lookup"><span data-stu-id="7258e-161">An example is the **Text** content field for a [ServiceNow](https://www.servicenow.com) knowledge-base article.</span></span>
* <span data-ttu-id="7258e-162">在搜尋結果中，只會標示為可檢索的屬性，並可用來建立新式的結果類型（MRTs）。</span><span class="sxs-lookup"><span data-stu-id="7258e-162">Only properties marked as retrievable render in the search results and can be used to create modern result types (MRTs).</span></span>
* <span data-ttu-id="7258e-163">只能將字串屬性標示為可搜尋。</span><span class="sxs-lookup"><span data-stu-id="7258e-163">Only string properties can be marked searchable.</span></span>

> [!Note]
> <span data-ttu-id="7258e-164">建立連線之後，就**無法**修改架構。</span><span class="sxs-lookup"><span data-stu-id="7258e-164">After you create a connection, you **can't** modify the schema.</span></span> <span data-ttu-id="7258e-165">若要這麼做，您必須刪除您的連線，並建立新的連線。</span><span class="sxs-lookup"><span data-stu-id="7258e-165">To do that, you need to delete your connection and create a new one.</span></span>

### <a name="manage-search-permissions"></a><span data-ttu-id="7258e-166">管理搜尋許可權</span><span class="sxs-lookup"><span data-stu-id="7258e-166">Manage search permissions</span></span>

<span data-ttu-id="7258e-167">存取控制清單（ACLs）決定組織中的哪些使用者可以存取每個資料項目目。</span><span class="sxs-lookup"><span data-stu-id="7258e-167">Access Control Lists (ACLs) determine which users in your organization can access each item of data.</span></span> <span data-ttu-id="7258e-168">所有的連接器都支援所有使用者皆可看到的搜尋許可權。</span><span class="sxs-lookup"><span data-stu-id="7258e-168">All the connectors support search permissions that are visible to all users.</span></span>

### <a name="set-the-refresh-schedule"></a><span data-ttu-id="7258e-169">設定重新整理排程</span><span class="sxs-lookup"><span data-stu-id="7258e-169">Set the refresh schedule</span></span>

<span data-ttu-id="7258e-170">重新整理排程會決定您的資料與 Microsoft Graph 和 Microsoft 搜尋中的索引同步處理的頻率。</span><span class="sxs-lookup"><span data-stu-id="7258e-170">The refresh schedule determines how often your data is synced with the index in Microsoft Graph and Microsoft Search.</span></span> <span data-ttu-id="7258e-171">您可以透過兩種方式排程重新整理：完整編目或累加編目。</span><span class="sxs-lookup"><span data-stu-id="7258e-171">You can schedule the refresh in two ways: full crawl or incremental crawl.</span></span>

<span data-ttu-id="7258e-172">使用**完整**編目時，搜尋引擎會處理及索引內容來源中的每個專案，而不論先前的編目。</span><span class="sxs-lookup"><span data-stu-id="7258e-172">With a **full crawl**, the search engine processes and indexes every item in the content source, regardless of previous crawls.</span></span> <span data-ttu-id="7258e-173">在下列情況下，完整編目的運作方式最為好：</span><span class="sxs-lookup"><span data-stu-id="7258e-173">Full crawl works best in these situations:</span></span>

* <span data-ttu-id="7258e-174">偵測資料刪除。</span><span class="sxs-lookup"><span data-stu-id="7258e-174">Detecting deletions of data.</span></span>
* <span data-ttu-id="7258e-175">增量式編目無法編目錯誤的內容。</span><span class="sxs-lookup"><span data-stu-id="7258e-175">The incremental crawl failed to crawl content for errors.</span></span>
* <span data-ttu-id="7258e-176">已修改 ACLs。</span><span class="sxs-lookup"><span data-stu-id="7258e-176">ACLs were modified.</span></span>
* <span data-ttu-id="7258e-177">已修改編目規則。</span><span class="sxs-lookup"><span data-stu-id="7258e-177">Crawl rules were modified.</span></span>
* <span data-ttu-id="7258e-178">Microsoft 搜尋的軟體更新是必要的。</span><span class="sxs-lookup"><span data-stu-id="7258e-178">A software update for Microsoft Search is required.</span></span> <span data-ttu-id="7258e-179">更新會修改搜尋架構。</span><span class="sxs-lookup"><span data-stu-id="7258e-179">Updates modify the search schema.</span></span>

<span data-ttu-id="7258e-180">使用累加編目**時，搜尋**引擎只可以處理和編制自上次成功編目之後所建立或修改的專案。</span><span class="sxs-lookup"><span data-stu-id="7258e-180">With an **incremental crawl**, the search engine can process and index only the items that were created or modified since the last successful crawl.</span></span> <span data-ttu-id="7258e-181">因此，不會重新索引內容來源中的所有資料。</span><span class="sxs-lookup"><span data-stu-id="7258e-181">Therefore, not all the data in the content source is re-indexed.</span></span> <span data-ttu-id="7258e-182">增量式編目最適合偵測內容、中繼資料、許可權及其他更新。</span><span class="sxs-lookup"><span data-stu-id="7258e-182">Incremental crawls work best to detect content, metadata, permission, and other updates.</span></span>

<span data-ttu-id="7258e-183">因為未處理未變更的專案，所以增量編目的速度會比完全編目快許多。</span><span class="sxs-lookup"><span data-stu-id="7258e-183">Incremental crawls are much faster than full crawls because unchanged items aren’t processed.</span></span> <span data-ttu-id="7258e-184">若要維護內容來源與搜尋索引之間的準確資料同步處理，您必須定期執行這兩個編目。</span><span class="sxs-lookup"><span data-stu-id="7258e-184">To maintain an accurate data sync between the content source and the search index, you need to run both crawls periodically.</span></span>

<span data-ttu-id="7258e-185">每個連接器都會有一組不同的最佳重新整理排程，取決於修改資料的頻率及修改的類型。</span><span class="sxs-lookup"><span data-stu-id="7258e-185">Each connector will have a different optimal set of refresh schedules based on how often data is modified and the type of modifications.</span></span>

![累加編目和完整編目間隔設定會顯示增量為15分鐘，在1周完全編目。](media/refreshschedule.png)

### <a name="review-connector-settings"></a><span data-ttu-id="7258e-187">檢查連接器設定</span><span class="sxs-lookup"><span data-stu-id="7258e-187">Review connector settings</span></span>

<span data-ttu-id="7258e-188">設定連接器之後，系統[管理中心](https://admin.microsoft.com)會帶您前往可供您複查設定的頁面。</span><span class="sxs-lookup"><span data-stu-id="7258e-188">After you configure your connector, the [admin center](https://admin.microsoft.com) takes you to a page where you can review your settings.</span></span> <span data-ttu-id="7258e-189">您可以回到設定程式來編輯任何設定，再確認連接。</span><span class="sxs-lookup"><span data-stu-id="7258e-189">You can go back through the configuration process to edit any setting before you confirm the connection.</span></span> <span data-ttu-id="7258e-190">若要深入瞭解，請參閱[管理您的連接器](manage-connector.md)。</span><span class="sxs-lookup"><span data-stu-id="7258e-190">To learn more, see [Manage your connector](manage-connector.md).</span></span>

## <a name="next-steps-customize-the-search-results-page"></a><span data-ttu-id="7258e-191">後續步驟：自訂搜尋結果頁面</span><span class="sxs-lookup"><span data-stu-id="7258e-191">Next steps: Customize the search results page</span></span>

<span data-ttu-id="7258e-192">透過 Microsoft Search 使用者介面（UI），您的使用者可以從您的[microsoft 365](https://www.microsoft.com/microsoft-365)生產力應用程式和更廣泛的 microsoft 體系中搜尋內容。</span><span class="sxs-lookup"><span data-stu-id="7258e-192">With the Microsoft Search user interface (UI), your end users can search content from your [Microsoft 365](https://www.microsoft.com/microsoft-365) productivity apps and the broader Microsoft ecosystem.</span></span> <span data-ttu-id="7258e-193">搜尋類別是指使用者在[SharePoint](https://sharepoint.com/)、 [Microsoft Office](https://Office.com)及[Bing](https://Bing.com)中的 microsoft 搜尋中查看其搜尋結果時所顯示的索引標籤。</span><span class="sxs-lookup"><span data-stu-id="7258e-193">A search vertical refers to the tabs that are shown when a user views their search results in [SharePoint](https://sharepoint.com/), [Microsoft Office](https://Office.com), and Microsoft Search in [Bing](https://Bing.com).</span></span> <span data-ttu-id="7258e-194">您可以自訂搜尋範圍來縮小結果，如此只會顯示特定類型的搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="7258e-194">You can customize search verticals to narrow down results, so that only a certain type of search results is displayed.</span></span> <span data-ttu-id="7258e-195">這些縱向顯示為搜尋結果頁面頂端的 tab 鍵。</span><span class="sxs-lookup"><span data-stu-id="7258e-195">These verticals appear as a tab on the top of the search results page.</span></span> <span data-ttu-id="7258e-196">現代結果類型（MRT.LOG）是指定結果呈現方式的 UI。</span><span class="sxs-lookup"><span data-stu-id="7258e-196">A modern result type (MRT) is the UI that designates how results are presented.</span></span>

<span data-ttu-id="7258e-197">建立您自己的行業和結果類型，讓使用者可以從新的連線中查看搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="7258e-197">Create your own verticals and result types, so end users can view search results from new connections.</span></span> <span data-ttu-id="7258e-198">在此步驟中，您的連線中的資料不會顯示在搜尋結果頁面上。</span><span class="sxs-lookup"><span data-stu-id="7258e-198">Without this step, data from your connection won’t show up on the search results page.</span></span>

<span data-ttu-id="7258e-199">若要深入瞭解如何建立您的行業和 MRTs，請參閱[搜尋結果頁面自訂](customize-search-page.md)。</span><span class="sxs-lookup"><span data-stu-id="7258e-199">To learn more about how to create your verticals and MRTs, see [Search results page customization](customize-search-page.md).</span></span>

## <a name="how-do-i-know-the-connection-setup-worked"></a><span data-ttu-id="7258e-200">如何知道連線設定是否運作正常？</span><span class="sxs-lookup"><span data-stu-id="7258e-200">How do I know the connection setup worked?</span></span>

<span data-ttu-id="7258e-201">在系統[管理中心](https://admin.microsoft.com)的 [**連接器**] 索引標籤下，移至您發佈的連線清單。</span><span class="sxs-lookup"><span data-stu-id="7258e-201">Go to the list of your published connections under the **Connectors** tab in the [admin center](https://admin.microsoft.com).</span></span> <span data-ttu-id="7258e-202">若要瞭解如何進行更新和刪除，請參閱[管理您的連接器](manage-connector.md)。</span><span class="sxs-lookup"><span data-stu-id="7258e-202">To learn how to make updates and deletions, see [Manage your connector](manage-connector.md).</span></span>
