---
title: Microsoft 搜尋的 Oracle SQL Graph 連接器
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
ROBOTS: NoIndex
description: 設定適用于 Microsoft 搜尋的 Oracle SQL Graph 連接器。
ms.openlocfilehash: 901b772def7585606a090d8a7696a32ff028e2a0
ms.sourcegitcommit: f76ade4c8fed0fee9c36d067b3ca8288c6c980aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "50508893"
---
<!---Previous ms.author:vivg --->

# <a name="oracle-sql-graph-connector"></a><span data-ttu-id="5aaff-103">Oracle SQL Graph 連接器</span><span class="sxs-lookup"><span data-stu-id="5aaff-103">Oracle SQL Graph connector</span></span>

<span data-ttu-id="5aaff-104">Oracle SQL Graph 連接器可讓您的組織探索內部部署 Oracle 資料庫中的資料並為其編制索引。</span><span class="sxs-lookup"><span data-stu-id="5aaff-104">The Oracle SQL Graph connector allows your organization to discover and index data from an on-premises Oracle database.</span></span> <span data-ttu-id="5aaff-105">連接器會將指定的內容索引至 Microsoft 搜尋。</span><span class="sxs-lookup"><span data-stu-id="5aaff-105">The connector indexes specified content into Microsoft Search.</span></span> <span data-ttu-id="5aaff-106">若要讓索引保持在最新的來來源資料中，它支援定期完整和累加編目。</span><span class="sxs-lookup"><span data-stu-id="5aaff-106">To keep the index up to date with source data, it supports periodic full and incremental crawls.</span></span> <span data-ttu-id="5aaff-107">透過 Oracle SQL connector，您也可以限制特定使用者對搜尋結果的存取。</span><span class="sxs-lookup"><span data-stu-id="5aaff-107">With the Oracle SQL connector, you can also restrict access to search results for certain users.</span></span>

> [!NOTE]
> <span data-ttu-id="5aaff-108">請閱讀 [**您的圖形連接器**](configure-connector.md) 文章的設定，以瞭解一般圖表連接器設定指示。</span><span class="sxs-lookup"><span data-stu-id="5aaff-108">Read the [**Setup for your Graph connector**](configure-connector.md) article to understand the general Graph connectors setup instructions.</span></span>

<span data-ttu-id="5aaff-109">本文適用于任何設定、執行及監視 Oracle SQL Graph 連接器的人員。</span><span class="sxs-lookup"><span data-stu-id="5aaff-109">This article is for anyone who configures, runs, and monitors an Oracle SQL Graph connector.</span></span> <span data-ttu-id="5aaff-110">它會補充一般設定程式，並顯示只適用于 Oracle SQL Graph 連接器的指示。</span><span class="sxs-lookup"><span data-stu-id="5aaff-110">It supplements the general setup process, and shows instructions that apply only for the Oracle SQL Graph connector.</span></span> <span data-ttu-id="5aaff-111">本文也包含 [疑難排解](#troubleshooting) 及 [限制](#limitations)的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5aaff-111">This article also includes information about [Troubleshooting](#troubleshooting) and [Limitations](#limitations).</span></span>

## <a name="before-you-get-started"></a><span data-ttu-id="5aaff-112">開始之前</span><span class="sxs-lookup"><span data-stu-id="5aaff-112">Before you get started</span></span>

### <a name="install-the-graph-connector-agent"></a><span data-ttu-id="5aaff-113">安裝圖形連接器代理程式</span><span class="sxs-lookup"><span data-stu-id="5aaff-113">Install the Graph connector agent</span></span>

<span data-ttu-id="5aaff-114">為了存取您的內部部署協力廠商資料，您必須安裝及設定圖形連接器代理程式。</span><span class="sxs-lookup"><span data-stu-id="5aaff-114">In order to access your on-premises third-party data, you must install and configure the Graph connector agent.</span></span> <span data-ttu-id="5aaff-115">請參閱 [安裝 Graph connector agent](on-prem-agent.md) 以深入瞭解。</span><span class="sxs-lookup"><span data-stu-id="5aaff-115">See [Install the Graph connector agent](on-prem-agent.md) to learn more.</span></span>  

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a><span data-ttu-id="5aaff-116">步驟1：在 Microsoft 365 系統管理中心新增圖表連接器</span><span class="sxs-lookup"><span data-stu-id="5aaff-116">Step 1: Add a Graph connector in the Microsoft 365 admin center</span></span>

<span data-ttu-id="5aaff-117">遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。</span><span class="sxs-lookup"><span data-stu-id="5aaff-117">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-2-name-the-connection"></a><span data-ttu-id="5aaff-118">步驟2：命名連線</span><span class="sxs-lookup"><span data-stu-id="5aaff-118">Step 2: Name the connection</span></span>

<span data-ttu-id="5aaff-119">遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。</span><span class="sxs-lookup"><span data-stu-id="5aaff-119">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-3-configure-the-connection-settings"></a><span data-ttu-id="5aaff-120">步驟3：設定連接設定</span><span class="sxs-lookup"><span data-stu-id="5aaff-120">Step 3: Configure the connection settings</span></span>

<span data-ttu-id="5aaff-121">若要將 Oracle SQL 連接器連線至資料來源，您必須設定要編目的資料庫伺服器和內部部署圖形連接器代理程式。</span><span class="sxs-lookup"><span data-stu-id="5aaff-121">To connect your Oracle SQL connector to a data source, you must configure the database server you want crawled and the on-premises Graph connector agent.</span></span> <span data-ttu-id="5aaff-122">然後，您就可以使用必要的驗證方法來連接至資料庫。</span><span class="sxs-lookup"><span data-stu-id="5aaff-122">You can then connect to the database with the required authentication method.</span></span>

<span data-ttu-id="5aaff-123">對於 Oracle SQL connector，您必須指定主機名稱、埠和服務 (資料庫) 名稱，以及偏好的驗證方法、使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="5aaff-123">For Oracle SQL connector, you need to specify the Hostname, Port and Service (database) name along with the preferred authentication method, username, and password.</span></span>

> [!NOTE]
> <span data-ttu-id="5aaff-124">您的資料庫必須執行 Oracle 資料庫的11g 或更新版本，連接器才能夠連線。</span><span class="sxs-lookup"><span data-stu-id="5aaff-124">Your database must run Oracle database version 11g or later for the connector to be able to connect.</span></span> <span data-ttu-id="5aaff-125">連接器支援 Windows、Linux 和 Azure VM 平臺上的 Oracle 資料庫。</span><span class="sxs-lookup"><span data-stu-id="5aaff-125">The connector supports Oracle database hosted on Windows, Linux and Azure VM platforms.</span></span>

<span data-ttu-id="5aaff-126">若要搜尋您的資料庫內容，當您設定連接器時，必須指定 SQL 查詢。</span><span class="sxs-lookup"><span data-stu-id="5aaff-126">To search your database content, you must specify SQL queries when you configure the connector.</span></span> <span data-ttu-id="5aaff-127">這些 SQL 查詢必須命名所有要索引的資料庫資料欄 (也就是說，來源屬性) ，包括需要執行以取得所有欄的任何 SQL 聯接。</span><span class="sxs-lookup"><span data-stu-id="5aaff-127">These SQL queries need to name all the database columns that you want to index (that is, source properties), including any SQL joins that need to be performed to get all the columns.</span></span> <span data-ttu-id="5aaff-128">若要限制存取搜尋結果，您必須在設定連接器時，指定 (ACLs) 中的存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="5aaff-128">To restrict access to search results, you must specify Access Control Lists (ACLs) within SQL queries when you configure the connector.</span></span>

## <a name="step-3a-full-crawl-required"></a><span data-ttu-id="5aaff-129">步驟3a：必要的完整編目 () </span><span class="sxs-lookup"><span data-stu-id="5aaff-129">Step 3a: Full crawl (Required)</span></span>

<span data-ttu-id="5aaff-130">在這個步驟中，您會設定執行資料庫完整編目的 SQL 查詢。</span><span class="sxs-lookup"><span data-stu-id="5aaff-130">In this step, you configure the SQL query that runs a full crawl of the database.</span></span> <span data-ttu-id="5aaff-131">完整編目會選取所有欄或屬性，以選取 [ **查詢**]、[ **搜尋**] 或 [ **取得**] 選項。</span><span class="sxs-lookup"><span data-stu-id="5aaff-131">The full crawl selects all the columns or properties where you want to select the options **Query**, **Search**, or **Retrieve**.</span></span> <span data-ttu-id="5aaff-132">您也可以指定 ACL 欄，以限制搜尋結果對特定使用者或群組的存取。</span><span class="sxs-lookup"><span data-stu-id="5aaff-132">You can also specify ACL columns to restrict access of search results to specific users or groups.</span></span>

> [!Tip]
> <span data-ttu-id="5aaff-133">若要取得所需的所有欄，您可以加入多個表格。</span><span class="sxs-lookup"><span data-stu-id="5aaff-133">To get all the columns that you need, you can join multiple tables.</span></span>

![腳本顯示 OrderTable 及 AclTable （含範例屬性）](media/MSSQL-fullcrawl.png)

### <a name="select-data-columns-required-and-acl-columns-optional"></a><span data-ttu-id="5aaff-135"> (必要) 和 ACL 欄 (選用) 選取資料欄位</span><span class="sxs-lookup"><span data-stu-id="5aaff-135">Select data columns (Required) and ACL columns (Optional)</span></span>

<span data-ttu-id="5aaff-136">這個範例會示範五個數據列的選取範圍，其中保留搜尋的資料：「訂單」、「OrderTitle」、OrderDesc、CreatedDateTime 及 IsDeleted。</span><span class="sxs-lookup"><span data-stu-id="5aaff-136">The example demonstrates selection of five data columns that hold the data for the search: OrderId, OrderTitle, OrderDesc, CreatedDateTime, and IsDeleted.</span></span> <span data-ttu-id="5aaff-137">若要設定每個資料列的查看許可權，您可以選擇性地選取下列 ACL 欄： AllowedUsers、AllowedGroups、DeniedUsers 及 DeniedGroups。</span><span class="sxs-lookup"><span data-stu-id="5aaff-137">To set view permissions for each row of data, you can optionally select these ACL columns: AllowedUsers, AllowedGroups, DeniedUsers, and DeniedGroups.</span></span> <span data-ttu-id="5aaff-138">對於所有的資料行，您可以選取要 **查詢**、 **搜尋** 或 **檢索** 的選項。</span><span class="sxs-lookup"><span data-stu-id="5aaff-138">For all these data columns you can select the options to **Query**, **Search**, or **Retrieve**.</span></span>

<span data-ttu-id="5aaff-139">選取下列範例查詢所示的資料行： `SELECT OrderId, OrderTitle, OrderDesc, AllowedUsers, AllowedGroups, DeniedUsers, DeniedGroups, CreatedDateTime, IsDeleted`</span><span class="sxs-lookup"><span data-stu-id="5aaff-139">Select data columns as shown in this example query: `SELECT OrderId, OrderTitle, OrderDesc, AllowedUsers, AllowedGroups, DeniedUsers, DeniedGroups, CreatedDateTime, IsDeleted`</span></span>

<span data-ttu-id="5aaff-140">若要管理搜尋結果的存取權，您可以在查詢中指定一或多個 ACL 欄。</span><span class="sxs-lookup"><span data-stu-id="5aaff-140">To manage access to the search results, you can specify one or more ACL columns in the query.</span></span> <span data-ttu-id="5aaff-141">SQL connector 可讓您控制每個記錄層級的存取。</span><span class="sxs-lookup"><span data-stu-id="5aaff-141">The SQL connector allows you to control access at per record level.</span></span> <span data-ttu-id="5aaff-142">您可以選擇對資料表中的所有記錄使用相同的存取控制。</span><span class="sxs-lookup"><span data-stu-id="5aaff-142">You can choose to have the same access control for all records in a table.</span></span> <span data-ttu-id="5aaff-143">如果 ACL 資訊儲存在不同的資料表中，您可能必須在查詢中使用這些資料表進行聯接。</span><span class="sxs-lookup"><span data-stu-id="5aaff-143">If the ACL information is stored in a separate table, you might have to do a join with those tables in your query.</span></span>

<span data-ttu-id="5aaff-144">在上述查詢中使用每個 ACL 欄的描述如下。</span><span class="sxs-lookup"><span data-stu-id="5aaff-144">The use of each of the ACL columns in the above query is described below.</span></span> <span data-ttu-id="5aaff-145">下列清單說明四種 **存取控制機制**。</span><span class="sxs-lookup"><span data-stu-id="5aaff-145">The following list explains the four **access control mechanisms**.</span></span>

* <span data-ttu-id="5aaff-146">**AllowedUsers**：此選項會指定可以存取搜尋結果的使用者 IDs 清單。</span><span class="sxs-lookup"><span data-stu-id="5aaff-146">**AllowedUsers**: This option specifies the list of user IDs who will be able to access the search results.</span></span> <span data-ttu-id="5aaff-147">在下列範例中，使用者清單為： john@contoso.com、keith@contoso.com 和 lisa@contoso.com 只有具有「訂單 Id」的記錄存取權 = 12。</span><span class="sxs-lookup"><span data-stu-id="5aaff-147">In the following example, list of users: john@contoso.com, keith@contoso.com, and lisa@contoso.com would only have access to a record with OrderId = 12.</span></span>
* <span data-ttu-id="5aaff-148">**AllowedGroups**：此選項會指定可以存取搜尋結果的使用者群組。</span><span class="sxs-lookup"><span data-stu-id="5aaff-148">**AllowedGroups**: This option specifies the group of users who will be able to access the search results.</span></span> <span data-ttu-id="5aaff-149">在下列範例中，group sales-team@contoso.com 只會具有「訂單 Id = 12」的記錄存取權。</span><span class="sxs-lookup"><span data-stu-id="5aaff-149">In the following example, group sales-team@contoso.com would only have access to record with OrderId = 12.</span></span>
* <span data-ttu-id="5aaff-150">**DeniedUsers**：此選項會 **指定沒有搜尋** 結果存取權的使用者清單。</span><span class="sxs-lookup"><span data-stu-id="5aaff-150">**DeniedUsers**: This option specifies the list of users who do **not** have access to the search results.</span></span> <span data-ttu-id="5aaff-151">在下列範例中，使用者 john@contoso.com 及 keith@contoso.com 無法存取具有「訂單 Id」的記錄，而其他所有人都可以存取這筆記錄。</span><span class="sxs-lookup"><span data-stu-id="5aaff-151">In the following example, users john@contoso.com and keith@contoso.com do not have access to record with OrderId = 13, whereas everyone else has access to this record.</span></span>
* <span data-ttu-id="5aaff-152">**DeniedGroups**：此選項會 **指定沒有搜尋** 結果存取權的使用者群組。</span><span class="sxs-lookup"><span data-stu-id="5aaff-152">**DeniedGroups**: This option specifies the group of users who do **not** have access to the search results.</span></span> <span data-ttu-id="5aaff-153">在下列範例中，群組 engg-team@contoso.com 及 pm-team@contoso.com 沒有具有「訂單 Id」的記錄存取權，而其他所有人都可以存取這筆記錄。</span><span class="sxs-lookup"><span data-stu-id="5aaff-153">In the following example, groups engg-team@contoso.com and pm-team@contoso.com do not have access to record with OrderId = 15, whereas everyone else has access to this record.</span></span>  

![顯示 OrderTable 及 AclTable （含範例屬性）的範例資料](media/MSSQL-ACL1.png)

### <a name="supported-data-types"></a><span data-ttu-id="5aaff-155">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="5aaff-155">Supported data types</span></span>

<span data-ttu-id="5aaff-156">下表摘要 Oracle SQL 連接器支援的資料類型。</span><span class="sxs-lookup"><span data-stu-id="5aaff-156">The below table summarizes the data types that are supported by the Oracle SQL connector.</span></span> <span data-ttu-id="5aaff-157">該表也會摘要支援的 SQL 資料類型的索引資料類型。</span><span class="sxs-lookup"><span data-stu-id="5aaff-157">The table also summarizes the indexing data type for the supported SQL data type.</span></span> <span data-ttu-id="5aaff-158">若要深入瞭解 Microsoft Graph 連接器支援的索引資料類型，請參閱 [屬性資源類型](https://docs.microsoft.com/graph/api/resources/property?view=graph-rest-beta#properties&preserve-view=true)的檔。</span><span class="sxs-lookup"><span data-stu-id="5aaff-158">To learn more about Microsoft Graph connectors supported data types for indexing, refer documentation on [property resource types](https://docs.microsoft.com/graph/api/resources/property?view=graph-rest-beta#properties&preserve-view=true).</span></span>

| <span data-ttu-id="5aaff-159">類別</span><span class="sxs-lookup"><span data-stu-id="5aaff-159">Category</span></span> | <span data-ttu-id="5aaff-160">來源資料類型</span><span class="sxs-lookup"><span data-stu-id="5aaff-160">Source data type</span></span> | <span data-ttu-id="5aaff-161">索引資料類型</span><span class="sxs-lookup"><span data-stu-id="5aaff-161">Indexing data type</span></span> |
| ------------ | ------------ | ------------ |
| <span data-ttu-id="5aaff-162">數位資料類型</span><span class="sxs-lookup"><span data-stu-id="5aaff-162">Number datatype</span></span> | <span data-ttu-id="5aaff-163">數位 (p，0) </span><span class="sxs-lookup"><span data-stu-id="5aaff-163">NUMBER(p,0)</span></span> | <span data-ttu-id="5aaff-164">p <的 int64 (= 18) </span><span class="sxs-lookup"><span data-stu-id="5aaff-164">int64 (for p <= 18)</span></span> <br> <span data-ttu-id="5aaff-165">p > 18) 的雙 (</span><span class="sxs-lookup"><span data-stu-id="5aaff-165">double (for p > 18)</span></span> |
| <span data-ttu-id="5aaff-166">浮點數字資料類型</span><span class="sxs-lookup"><span data-stu-id="5aaff-166">Floating-point number datatype</span></span> | <span data-ttu-id="5aaff-167">數位 (p，s) </span><span class="sxs-lookup"><span data-stu-id="5aaff-167">NUMBER(p,s)</span></span> <br> <span data-ttu-id="5aaff-168">浮動 (p) </span><span class="sxs-lookup"><span data-stu-id="5aaff-168">FLOAT(p)</span></span> | <span data-ttu-id="5aaff-169">double</span><span class="sxs-lookup"><span data-stu-id="5aaff-169">double</span></span> |
| <span data-ttu-id="5aaff-170">Date datatype</span><span class="sxs-lookup"><span data-stu-id="5aaff-170">Date datatype</span></span> | <span data-ttu-id="5aaff-171">日期</span><span class="sxs-lookup"><span data-stu-id="5aaff-171">DATE</span></span> <br> <span data-ttu-id="5aaff-172">時間 戳</span><span class="sxs-lookup"><span data-stu-id="5aaff-172">TIMESTAMP</span></span> <br> <span data-ttu-id="5aaff-173">TIMESTAMP (n) </span><span class="sxs-lookup"><span data-stu-id="5aaff-173">TIMESTAMP(n)</span></span> | <span data-ttu-id="5aaff-174">datetime</span><span class="sxs-lookup"><span data-stu-id="5aaff-174">datetime</span></span> |
| <span data-ttu-id="5aaff-175">字元資料類型</span><span class="sxs-lookup"><span data-stu-id="5aaff-175">Character datatype</span></span> | <span data-ttu-id="5aaff-176">CHAR (n) </span><span class="sxs-lookup"><span data-stu-id="5aaff-176">CHAR(n)</span></span> <br> <span data-ttu-id="5aaff-177">VARCHAR</span><span class="sxs-lookup"><span data-stu-id="5aaff-177">VARCHAR</span></span> <br> <span data-ttu-id="5aaff-178">VARCHAR2</span><span class="sxs-lookup"><span data-stu-id="5aaff-178">VARCHAR2</span></span> <br> <span data-ttu-id="5aaff-179">長</span><span class="sxs-lookup"><span data-stu-id="5aaff-179">LONG</span></span> <br> <span data-ttu-id="5aaff-180">Clob</span><span class="sxs-lookup"><span data-stu-id="5aaff-180">CLOB</span></span> <br> <span data-ttu-id="5aaff-181">NCLOB</span><span class="sxs-lookup"><span data-stu-id="5aaff-181">NCLOB</span></span> | <span data-ttu-id="5aaff-182">string</span><span class="sxs-lookup"><span data-stu-id="5aaff-182">string</span></span> |
| <span data-ttu-id="5aaff-183">Unicode 字元資料類型</span><span class="sxs-lookup"><span data-stu-id="5aaff-183">Unicode character datatype</span></span> | <span data-ttu-id="5aaff-184">NCHAR</span><span class="sxs-lookup"><span data-stu-id="5aaff-184">NCHAR</span></span> <br> <span data-ttu-id="5aaff-185">NVARCHAR</span><span class="sxs-lookup"><span data-stu-id="5aaff-185">NVARCHAR</span></span> | <span data-ttu-id="5aaff-186">string</span><span class="sxs-lookup"><span data-stu-id="5aaff-186">string</span></span> |
| <span data-ttu-id="5aaff-187">RowID 資料類型</span><span class="sxs-lookup"><span data-stu-id="5aaff-187">RowID datatype</span></span> | <span data-ttu-id="5aaff-188">ROWID</span><span class="sxs-lookup"><span data-stu-id="5aaff-188">ROWID</span></span> <br> <span data-ttu-id="5aaff-189">UROWID</span><span class="sxs-lookup"><span data-stu-id="5aaff-189">UROWID</span></span> | <span data-ttu-id="5aaff-190">string</span><span class="sxs-lookup"><span data-stu-id="5aaff-190">string</span></span> |

<span data-ttu-id="5aaff-191">對於目前不是直接支援的任何其他資料類型，此資料行必須明確地轉換成支援的資料類型。</span><span class="sxs-lookup"><span data-stu-id="5aaff-191">For any other data type currently not directly supported, the column needs to be explicitly cast to a supported data type.</span></span>

### <a name="watermark-required"></a><span data-ttu-id="5aaff-192">浮水印 (必要) </span><span class="sxs-lookup"><span data-stu-id="5aaff-192">Watermark (Required)</span></span>

<span data-ttu-id="5aaff-193">若要防止資料庫超載，連接器會批次並繼續完整編目的查詢。</span><span class="sxs-lookup"><span data-stu-id="5aaff-193">To prevent overloading the database, the connector batches and resumes full-crawl queries with a full-crawl watermark column.</span></span> <span data-ttu-id="5aaff-194">使用 [浮水印] 資料行的值，每個後續的批次都會取得，而查詢會從最後一個檢查點繼續。</span><span class="sxs-lookup"><span data-stu-id="5aaff-194">By using the value of the watermark column, each subsequent batch is fetched, and querying is resumed from the last checkpoint.</span></span> <span data-ttu-id="5aaff-195">本質上，這是一種機制，用來控制完整編目的資料重新整理。</span><span class="sxs-lookup"><span data-stu-id="5aaff-195">Essentially this is a mechanism to control data refresh for full crawls.</span></span>

<span data-ttu-id="5aaff-196">建立浮水印的查詢程式碼片段，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="5aaff-196">Create query snippets for watermarks as shown in these examples:</span></span>

* <span data-ttu-id="5aaff-197">`WHERE (CreatedDateTime > @watermark)`.</span><span class="sxs-lookup"><span data-stu-id="5aaff-197">`WHERE (CreatedDateTime > @watermark)`.</span></span> <span data-ttu-id="5aaff-198">使用保留的關鍵字來引用浮水印欄名稱 `@watermark` 。</span><span class="sxs-lookup"><span data-stu-id="5aaff-198">Cite the watermark column name with the reserved keyword `@watermark`.</span></span> <span data-ttu-id="5aaff-199">您只能以遞增順序排序浮水印欄。</span><span class="sxs-lookup"><span data-stu-id="5aaff-199">You can only sort the watermark column in ascending order.</span></span>
* <span data-ttu-id="5aaff-200">`ORDER BY CreatedDateTime ASC`.</span><span class="sxs-lookup"><span data-stu-id="5aaff-200">`ORDER BY CreatedDateTime ASC`.</span></span> <span data-ttu-id="5aaff-201">在 [浮水印] 欄上以遞增順序排序。</span><span class="sxs-lookup"><span data-stu-id="5aaff-201">Sort on the watermark column in ascending order.</span></span>

<span data-ttu-id="5aaff-202">在下一個影像所示的設定中， `CreatedDateTime` 是選取的 [浮水印] 欄。</span><span class="sxs-lookup"><span data-stu-id="5aaff-202">In the configuration shown in the following image, `CreatedDateTime` is the selected watermark column.</span></span> <span data-ttu-id="5aaff-203">若要取得第一批列，請指定 [浮水印] 資料行的資料類型。</span><span class="sxs-lookup"><span data-stu-id="5aaff-203">To fetch the first batch of rows, specify the data type of the watermark column.</span></span> <span data-ttu-id="5aaff-204">在此情況下，資料類型為 `DateTime` 。</span><span class="sxs-lookup"><span data-stu-id="5aaff-204">In this case, the data type is `DateTime`.</span></span>

![浮水印欄設定](media/MSSQL-watermark.png)

<span data-ttu-id="5aaff-206">第 **一個查詢** 會使用： "CreatedDateTime > 1753 年1月1日，00:00:00" (最小值 DateTime 的資料類型) 。</span><span class="sxs-lookup"><span data-stu-id="5aaff-206">The first query fetches the first **N** number of rows by using: "CreatedDateTime > January 1, 1753 00:00:00" (min value of DateTime data type).</span></span> <span data-ttu-id="5aaff-207">提取第一個批次之後， `CreatedDateTime` 如果資料列是以遞增順序排序，則會將批次中傳回的最高值儲存為檢查點。</span><span class="sxs-lookup"><span data-stu-id="5aaff-207">After the first batch is fetched, the highest value of `CreatedDateTime` returned in the batch is saved as the checkpoint if the rows are sorted in ascending order.</span></span> <span data-ttu-id="5aaff-208">範例是 03:00:00 2019 年3月1日。</span><span class="sxs-lookup"><span data-stu-id="5aaff-208">An example is March 1, 2019 03:00:00.</span></span> <span data-ttu-id="5aaff-209">然後，在查詢中使用「CreatedDateTime > 三月份1，2019 03:00:00」提取下一批 **N** 列。</span><span class="sxs-lookup"><span data-stu-id="5aaff-209">Then the next batch of **N** rows is fetched by using "CreatedDateTime > March 1, 2019 03:00:00" in the query.</span></span>

### <a name="skipping-soft-deleted-rows-optional"></a><span data-ttu-id="5aaff-210">跳過虛刪除的列 (選用) </span><span class="sxs-lookup"><span data-stu-id="5aaff-210">Skipping soft-deleted rows (Optional)</span></span>

<span data-ttu-id="5aaff-211">若要排除資料庫中虛刪除的列的索引，請指定虛刪除的列名稱和值，以指出刪除列的資料行。</span><span class="sxs-lookup"><span data-stu-id="5aaff-211">To exclude soft-deleted rows in your database from being indexed, specify the soft-delete column name and value that indicates the row is deleted.</span></span>

![虛刪除設定： "Soft delete column" 和 "soft delete 欄的值，表示已刪除的資料列"](media/MSSQL-softdelete.png)

### <a name="full-crawl-manage-search-permissions"></a><span data-ttu-id="5aaff-213">完整編目：管理搜尋許可權</span><span class="sxs-lookup"><span data-stu-id="5aaff-213">Full crawl: Manage search permissions</span></span>

<span data-ttu-id="5aaff-214">選取 [ **管理許可權** ]，以選擇用來指定存取控制機制 (ACL) 欄的各種存取控制。</span><span class="sxs-lookup"><span data-stu-id="5aaff-214">Select **Manage permissions** to choose the various access control (ACL) columns that specify the access control mechanism.</span></span> <span data-ttu-id="5aaff-215">選取您在完整編目 SQL 查詢中所指定的資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="5aaff-215">Select the column name you specified in the full crawl SQL query.</span></span>

<span data-ttu-id="5aaff-216">每個 ACL 欄都應該是多重值欄。</span><span class="sxs-lookup"><span data-stu-id="5aaff-216">Each of the ACL columns is expected to be a multi-valued column.</span></span> <span data-ttu-id="5aaff-217">您可以使用分隔符號（如分號 (; ) 、逗號 (、) 等等）來分隔這些多個 ID 值。</span><span class="sxs-lookup"><span data-stu-id="5aaff-217">These multiple ID values can be separated by separators such as semicolon (;), comma (,), and so on.</span></span> <span data-ttu-id="5aaff-218">您必須在 [ **值分隔符號** ] 欄位中指定此分隔符號。</span><span class="sxs-lookup"><span data-stu-id="5aaff-218">You need to specify this separator in the **value separator** field.</span></span>

<span data-ttu-id="5aaff-219">下列識別碼類型可供使用 ACLs：</span><span class="sxs-lookup"><span data-stu-id="5aaff-219">The following ID types are supported for using as ACLs:</span></span>

* <span data-ttu-id="5aaff-220">**使用者主體名稱 (upn)**：使用者主要名稱 (upn) 是以電子郵件地址格式的系統使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="5aaff-220">**User Principal Name (UPN)**: A User Principal Name (UPN) is the name of a system user in an email address format.</span></span> <span data-ttu-id="5aaff-221">UPN (例如： john.doe@domain.com) 會包含 (登入名稱) 、分隔符號 (@ 符號) 和功能變數名稱 (UPN 尾碼) 的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="5aaff-221">A UPN (for example: john.doe@domain.com) consists of the username (logon name), separator (the @ symbol), and domain name (UPN suffix).</span></span>
* <span data-ttu-id="5aaff-222">**Azure Active Directory (AAD) 識別碼**：在 Azure AD 中，每個使用者或群組都有一個類似 ' e0d3ad3d-0000-1111-2222-3c5f5c52ab9b ' 的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="5aaff-222">**Azure Active Directory (AAD) ID**: In Azure AD, every user or group has an object ID that looks something like 'e0d3ad3d-0000-1111-2222-3c5f5c52ab9b'</span></span>
* <span data-ttu-id="5aaff-223">**Active Directory (AD) 安全性** 識別碼：在內部部署 AD 安裝程式中，每個使用者和群組都有一個無法變化的唯一安全性識別碼，看起來像是-1-5-21-3878594291-2115959936-132693609-65242。 '</span><span class="sxs-lookup"><span data-stu-id="5aaff-223">**Active Directory (AD) Security ID**: In an on-premises AD setup, every user and group have an immutable, unique security identifier that looks something like 'S-1-5-21-3878594291-2115959936-132693609-65242.'</span></span>

![設定存取控制清單的搜尋許可權設定](media/MSSQL-ACL2.png)

## <a name="step-3b-incremental-crawl-optional"></a><span data-ttu-id="5aaff-225">步驟3b：增量編目 (選用) </span><span class="sxs-lookup"><span data-stu-id="5aaff-225">Step 3b: Incremental crawl (Optional)</span></span>

<span data-ttu-id="5aaff-226">在此選用的步驟中，請提供 SQL 查詢，以執行資料庫的增量式編目。</span><span class="sxs-lookup"><span data-stu-id="5aaff-226">In this optional step, provide a SQL query to run an incremental crawl of the database.</span></span> <span data-ttu-id="5aaff-227">在此查詢中，SQL 連接器會決定自上次累加編目以來對資料所做的任何變更。</span><span class="sxs-lookup"><span data-stu-id="5aaff-227">With this query, the SQL connector determines any changes to the data since the last incremental crawl.</span></span> <span data-ttu-id="5aaff-228">在完整編目中，選取 [選項] [ **查詢**]、[ **搜尋**] 或 [ **取得**]。</span><span class="sxs-lookup"><span data-stu-id="5aaff-228">As in the full crawl, select between the options **Query**, **Search**, or **Retrieve**.</span></span> <span data-ttu-id="5aaff-229">指定您在完整編目查詢中指定的相同 ACL 欄集。</span><span class="sxs-lookup"><span data-stu-id="5aaff-229">Specify the same set of ACL columns that you specified in the full crawl query.</span></span>

<span data-ttu-id="5aaff-230">下列映射中的元件類似于完整編目元件，但有一個例外。</span><span class="sxs-lookup"><span data-stu-id="5aaff-230">The components in the following image resemble the full crawl components with one exception.</span></span> <span data-ttu-id="5aaff-231">在此情況下，"ModifiedDateTime" 是選取的浮水印欄。</span><span class="sxs-lookup"><span data-stu-id="5aaff-231">In this case, "ModifiedDateTime" is the selected watermark column.</span></span> <span data-ttu-id="5aaff-232">查看 [完整編目步驟](#step-3a-full-crawl-required) ，以瞭解如何撰寫累加編目查詢，並以範例顯示下列影像。</span><span class="sxs-lookup"><span data-stu-id="5aaff-232">Review the [full crawl steps](#step-3a-full-crawl-required) to learn how to write your incremental crawl query and see the following image as an example.</span></span>

![新增編目腳本，顯示可使用的 OrderTable、AclTable 和範例屬性。](media/MSSQL-incrcrawl.png)

## <a name="step-4-assign-property-labels"></a><span data-ttu-id="5aaff-234">步驟4：指派屬性標籤</span><span class="sxs-lookup"><span data-stu-id="5aaff-234">Step 4: Assign property labels</span></span>

<span data-ttu-id="5aaff-235">遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。</span><span class="sxs-lookup"><span data-stu-id="5aaff-235">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-5-manage-schema"></a><span data-ttu-id="5aaff-236">步驟5：管理架構</span><span class="sxs-lookup"><span data-stu-id="5aaff-236">Step 5: Manage schema</span></span>

<span data-ttu-id="5aaff-237">遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。</span><span class="sxs-lookup"><span data-stu-id="5aaff-237">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

## <a name="step-6-manage-search-permissions"></a><span data-ttu-id="5aaff-238">步驟6：管理搜尋許可權</span><span class="sxs-lookup"><span data-stu-id="5aaff-238">Step 6: Manage search permissions</span></span>

<span data-ttu-id="5aaff-239">您可以選擇使用完整編目 [畫面中所指定的 ACLs](#full-crawl-manage-search-permissions) ，也可以覆寫它們，讓每個人都能看到您的內容。</span><span class="sxs-lookup"><span data-stu-id="5aaff-239">You can choose to use the [ACLs specified in the full crawl screen](#full-crawl-manage-search-permissions) or you can override them to make your content visible to everyone.</span></span>

## <a name="step-7-choose-refresh-settings"></a><span data-ttu-id="5aaff-240">步驟7：選擇重新整理設定</span><span class="sxs-lookup"><span data-stu-id="5aaff-240">Step 7: Choose refresh settings</span></span>

<span data-ttu-id="5aaff-241">Oracle SQL connector 支援完整和累加編目的更新排程。</span><span class="sxs-lookup"><span data-stu-id="5aaff-241">The Oracle SQL connector supports refresh schedules for both full and incremental crawls.</span></span> <span data-ttu-id="5aaff-242">我們建議您同時設定兩者。</span><span class="sxs-lookup"><span data-stu-id="5aaff-242">We recommend that you set both.</span></span>

<span data-ttu-id="5aaff-243">完整編目排程會找到先前已同步處理至 Microsoft 搜尋索引的已刪除資料列，以及移出同步篩選的任何列。</span><span class="sxs-lookup"><span data-stu-id="5aaff-243">A full crawl schedule finds deleted rows that were previously synced to the Microsoft Search index and any rows that moved out of the sync filter.</span></span> <span data-ttu-id="5aaff-244">當您第一次連線至資料庫時，會執行完整編目，以同步處理所有從完整編目查詢檢索到的資料列。</span><span class="sxs-lookup"><span data-stu-id="5aaff-244">When you first connect to the database, a full crawl runs to sync all the rows retrieved from the full crawl query.</span></span> <span data-ttu-id="5aaff-245">若要同步處理新的資料列並進行更新，您必須排程累加編目。</span><span class="sxs-lookup"><span data-stu-id="5aaff-245">To sync new rows and make updates, you need to schedule incremental crawls.</span></span>

## <a name="step-8-review-connection"></a><span data-ttu-id="5aaff-246">步驟8：檢查連線</span><span class="sxs-lookup"><span data-stu-id="5aaff-246">Step 8: Review connection</span></span>

<span data-ttu-id="5aaff-247">遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。</span><span class="sxs-lookup"><span data-stu-id="5aaff-247">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup instructions.-->

<!--- ## Next steps: Customize the search results page

Create your own verticals and result types, so end users can view search results from new connections. Without this step, data from your connection won't show up on the search results page.

To learn more about how to create your verticals and MRTs, see [Search results page customization](customize-search-page.md). -->

## <a name="troubleshooting"></a><span data-ttu-id="5aaff-248">疑難排解</span><span class="sxs-lookup"><span data-stu-id="5aaff-248">Troubleshooting</span></span>

<span data-ttu-id="5aaff-249">下表是設定連接器時所觀察到的常見錯誤，以及可能的原因。</span><span class="sxs-lookup"><span data-stu-id="5aaff-249">Underneath is a list of common errors observed while configuring the connector and their possible reasons.</span></span>

| <span data-ttu-id="5aaff-250">設定步驟</span><span class="sxs-lookup"><span data-stu-id="5aaff-250">Configuration step</span></span> | <span data-ttu-id="5aaff-251">錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="5aaff-251">Error message</span></span> | <span data-ttu-id="5aaff-252">可能的原因 (s) </span><span class="sxs-lookup"><span data-stu-id="5aaff-252">Possible reason(s)</span></span> |
| ------------ | ------------ | ------------ |
| <span data-ttu-id="5aaff-253">資料庫設定</span><span class="sxs-lookup"><span data-stu-id="5aaff-253">Database settings</span></span> | <span data-ttu-id="5aaff-254">來自資料庫伺服器的錯誤：連接要求超時</span><span class="sxs-lookup"><span data-stu-id="5aaff-254">Error from database server: Connection request timed out</span></span> | <span data-ttu-id="5aaff-255">不正確主機名稱</span><span class="sxs-lookup"><span data-stu-id="5aaff-255">Invalid Hostname</span></span> <br> <span data-ttu-id="5aaff-256">無法到達主機</span><span class="sxs-lookup"><span data-stu-id="5aaff-256">Host not reachable</span></span> |
| <span data-ttu-id="5aaff-257">資料庫設定</span><span class="sxs-lookup"><span data-stu-id="5aaff-257">Database settings</span></span> | <span data-ttu-id="5aaff-258">來自資料庫伺服器的錯誤： ORA-12541： TNS：沒有攔截器</span><span class="sxs-lookup"><span data-stu-id="5aaff-258">Error from database server: ORA-12541: TNS: No listener</span></span> | <span data-ttu-id="5aaff-259">不正確埠</span><span class="sxs-lookup"><span data-stu-id="5aaff-259">Invalid Port</span></span> |
| <span data-ttu-id="5aaff-260">資料庫設定</span><span class="sxs-lookup"><span data-stu-id="5aaff-260">Database settings</span></span> | <span data-ttu-id="5aaff-261">來自資料庫伺服器的錯誤： ORA-12514： TNS：攔截器目前不知道連接器描述項中所要求的服務</span><span class="sxs-lookup"><span data-stu-id="5aaff-261">Error from database server: ORA-12514: TNS: listener does not currently know of service requested in connector descriptor</span></span> | <span data-ttu-id="5aaff-262">不正確服務 (資料庫) 名稱</span><span class="sxs-lookup"><span data-stu-id="5aaff-262">Invalid service (database) name</span></span> |
| <span data-ttu-id="5aaff-263">資料庫設定</span><span class="sxs-lookup"><span data-stu-id="5aaff-263">Database settings</span></span> | <span data-ttu-id="5aaff-264">來自資料庫伺服器的錯誤：使用者 ' ' 的登入失敗 `user` 。</span><span class="sxs-lookup"><span data-stu-id="5aaff-264">Error from database server: Login failed for user '`user`'.</span></span> | <span data-ttu-id="5aaff-265">不正確使用者名稱或密碼</span><span class="sxs-lookup"><span data-stu-id="5aaff-265">Invalid username or password</span></span> |

## <a name="limitations"></a><span data-ttu-id="5aaff-266">限制</span><span class="sxs-lookup"><span data-stu-id="5aaff-266">Limitations</span></span>

<span data-ttu-id="5aaff-267">「Oracle SQL connector」在預覽版本中有下列限制：</span><span class="sxs-lookup"><span data-stu-id="5aaff-267">The Oracle SQL connector has these limitations in the preview release:</span></span>

* <span data-ttu-id="5aaff-268">內部部署資料庫必須執行 Oracle 資料庫11g 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="5aaff-268">The on-premises database must run Oracle Database version 11g or later.</span></span>
* <span data-ttu-id="5aaff-269">只有使用使用者主要名稱 (UPN) 、Azure Active Directory (Azure AD) 或 Active Directory 安全性才能支援 ACLs。</span><span class="sxs-lookup"><span data-stu-id="5aaff-269">ACLs are only supported by using a User Principal Name (UPN), Azure Active Directory (Azure AD), or Active Directory Security.</span></span>
* <span data-ttu-id="5aaff-270">不支援在資料庫欄中編制豐富內容的索引。</span><span class="sxs-lookup"><span data-stu-id="5aaff-270">Indexing rich content inside database columns is not supported.</span></span> <span data-ttu-id="5aaff-271">這類內容的範例為 HTML、JSON、XML、blob 及檔 parsings，以資料庫資料欄中的連結形式存在。</span><span class="sxs-lookup"><span data-stu-id="5aaff-271">Examples of such content are HTML, JSON, XML, blobs, and document parsings that exist as links inside the database columns.</span></span>
