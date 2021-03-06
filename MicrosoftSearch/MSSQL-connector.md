---
title: Microsoft 搜尋的 Azure SQL 和 Microsoft SQL server Graph 連接器
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
description: 設定 Azure SQL 及 Microsoft SQL Graph connector 以進行 Microsoft 搜尋。
ms.openlocfilehash: 499c0fad93f97e634086ff9025d947c4f70336fb
ms.sourcegitcommit: f76ade4c8fed0fee9c36d067b3ca8288c6c980aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "50508902"
---
<!---Previous ms.author: vivg --->

# <a name="azure-sql-and-microsoft-sql-server-graph-connectors"></a><span data-ttu-id="29040-103">Azure SQL 及 Microsoft SQL server Graph 連接器</span><span class="sxs-lookup"><span data-stu-id="29040-103">Azure SQL and Microsoft SQL server Graph connectors</span></span>

<span data-ttu-id="29040-104">Microsoft SQL server 或 Azure SQL Graph 連接器可讓您的組織探索內部部署 SQL Server 資料庫中的資料，並為雲端中的 Azure SQL 實例所主控的資料庫進行索引。</span><span class="sxs-lookup"><span data-stu-id="29040-104">The Microsoft SQL server or Azure SQL Graph connector allows your organization to discover and index data from an on-premises SQL Server database, or a database hosted in your Azure SQL instance in the cloud.</span></span>
<span data-ttu-id="29040-105">圖形連接器會將指定的內容索引放入 Microsoft 搜尋中。</span><span class="sxs-lookup"><span data-stu-id="29040-105">The Graph connector indexes specified content into Microsoft Search.</span></span> <span data-ttu-id="29040-106">若要讓索引保持在最新的來來源資料中，它支援定期完整和累加編目。</span><span class="sxs-lookup"><span data-stu-id="29040-106">To keep the index up to date with source data, it supports periodic full and incremental crawls.</span></span> <span data-ttu-id="29040-107">透過這些 SQL 連接器，您也可以限制特定使用者對搜尋結果的存取。</span><span class="sxs-lookup"><span data-stu-id="29040-107">With these SQL connectors, you can also restrict access to search results for certain users.</span></span>

> [!NOTE]
> <span data-ttu-id="29040-108">請閱讀 [**您的圖形連接器文章設定**](configure-connector.md) ，以瞭解一般圖表連接器設定指示。</span><span class="sxs-lookup"><span data-stu-id="29040-108">Read the [**Setup your Graph connector**](configure-connector.md) article to understand the general Graph connectors setup instructions.</span></span>

<span data-ttu-id="29040-109">本文適用于任何設定、執行及監視 Azure SQL server Graph connector 的使用者。</span><span class="sxs-lookup"><span data-stu-id="29040-109">This article is for anyone who configures, runs, and monitors a Azure SQL and Microsoft SQL server Graph connector.</span></span> <span data-ttu-id="29040-110">它會補充一般設定程式，並顯示只適用于 Azure SQL 及 Microsoft SQL server Graph 連接器的指示。</span><span class="sxs-lookup"><span data-stu-id="29040-110">It supplements the general setup process, and shows instructions that apply only for the Azure SQL and Microsoft SQL server Graph connector.</span></span> <span data-ttu-id="29040-111">本文也包含 Microsoft SQL server 和 Azure SQL 連接器 [限制](#limitations) 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="29040-111">This article also includes information about [Limitations](#limitations) for the Microsoft SQL server and Azure SQL connectors.</span></span>

## <a name="before-you-get-started"></a><span data-ttu-id="29040-112">開始之前</span><span class="sxs-lookup"><span data-stu-id="29040-112">Before you get started</span></span>

### <a name="install-the-graph-connector-agent-required-for-on-premises-microsoft-sql-server-connector-only"></a><span data-ttu-id="29040-113">安裝僅限內部部署 Microsoft SQL server 連接器所需的圖形連接器代理程式 () </span><span class="sxs-lookup"><span data-stu-id="29040-113">Install the Graph connector agent (required for on-premises Microsoft SQL server connector only)</span></span>

<span data-ttu-id="29040-114">為了存取您的內部部署協力廠商資料，您必須安裝及設定圖形連接器代理程式。</span><span class="sxs-lookup"><span data-stu-id="29040-114">In order to access your on-premises third-party data, you must install and configure the Graph connector agent.</span></span> <span data-ttu-id="29040-115">請參閱 [安裝 Graph connector agent](on-prem-agent.md) 以深入瞭解。</span><span class="sxs-lookup"><span data-stu-id="29040-115">See [Install the Graph connector agent](on-prem-agent.md) to learn more.</span></span>  

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a><span data-ttu-id="29040-116">步驟1：在 Microsoft 365 系統管理中心新增圖表連接器</span><span class="sxs-lookup"><span data-stu-id="29040-116">Step 1: Add a Graph connector in the Microsoft 365 admin center</span></span>

<span data-ttu-id="29040-117">遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。</span><span class="sxs-lookup"><span data-stu-id="29040-117">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup 
instructions.-->

## <a name="step-2-name-the-connection"></a><span data-ttu-id="29040-118">步驟2：命名連線</span><span class="sxs-lookup"><span data-stu-id="29040-118">Step 2: Name the connection</span></span>

<span data-ttu-id="29040-119">遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。</span><span class="sxs-lookup"><span data-stu-id="29040-119">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup 
instructions.-->

## <a name="step-3-configure-the-connection-settings"></a><span data-ttu-id="29040-120">步驟3：設定連接設定</span><span class="sxs-lookup"><span data-stu-id="29040-120">Step 3: Configure the connection settings</span></span>

### <a name="register-an-app-for-azure-sql-connector-only"></a><span data-ttu-id="29040-121">僅針對 Azure SQL connector 註冊應用程式 () </span><span class="sxs-lookup"><span data-stu-id="29040-121">Register an app (for Azure SQL connector only)</span></span>

<span data-ttu-id="29040-122">針對 Azure SQL connector，您必須在 Azure Active Directory 中註冊應用程式，以允許 Microsoft Search 應用程式存取索引的資料。</span><span class="sxs-lookup"><span data-stu-id="29040-122">For Azure SQL connector, you must register an app in Azure Active Directory to allow Microsoft Search app to access data for indexing.</span></span> <span data-ttu-id="29040-123">若要深入瞭解如何註冊應用程式，請參閱 Microsoft Graph 檔，瞭解如何 [註冊應用程式](https://docs.microsoft.com/graph/auth-register-app-v2)。</span><span class="sxs-lookup"><span data-stu-id="29040-123">To learn more about registering an app, refer Microsoft Graph documentation on how to [register an app](https://docs.microsoft.com/graph/auth-register-app-v2).</span></span>

<span data-ttu-id="29040-124">完成應用程式註冊並記下應用程式名稱、應用程式 (用戶端) 識別碼與租使用者識別碼後，您需要 [產生新的用戶端密碼](https://docs.microsoft.com/azure/healthcare-apis/register-confidential-azure-ad-client-app#application-secret)。</span><span class="sxs-lookup"><span data-stu-id="29040-124">After completing the app registration and taking note of the app name, application (client) ID and tenant ID, you need to [generate a new client secret](https://docs.microsoft.com/azure/healthcare-apis/register-confidential-azure-ad-client-app#application-secret).</span></span> <span data-ttu-id="29040-125">用戶端密碼只會顯示一次。</span><span class="sxs-lookup"><span data-stu-id="29040-125">The client secret will only be displayed once.</span></span> <span data-ttu-id="29040-126">請記住 & 會安全地儲存用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="29040-126">Remember to note & store the client secret securely.</span></span> <span data-ttu-id="29040-127">在 Microsoft 搜尋中設定新的連線時，請使用用戶端識別碼和用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="29040-127">Use the client ID and client secret while configuring a new connection in Microsoft Search.</span></span>

<span data-ttu-id="29040-128">若要將註冊的應用程式新增至 Azure SQL 資料庫，您必須：</span><span class="sxs-lookup"><span data-stu-id="29040-128">To add the registered app to your Azure SQL Database, you need to:</span></span>

- <span data-ttu-id="29040-129">登入 Azure SQL DB</span><span class="sxs-lookup"><span data-stu-id="29040-129">Log in to your Azure SQL DB</span></span>
- <span data-ttu-id="29040-130">開啟新的查詢視窗</span><span class="sxs-lookup"><span data-stu-id="29040-130">Open a new query window</span></span>
- <span data-ttu-id="29040-131">從外部提供者執行命令「建立使用者 [app 名稱]，以建立新使用者</span><span class="sxs-lookup"><span data-stu-id="29040-131">Create a new user by running the command 'CREATE USER [app name] FROM EXTERNAL PROVIDER'</span></span>
- <span data-ttu-id="29040-132">執行命令 ' exec sp_addrolemember ' db_datareader '、[app name] 或 ' ALTER ROLE db_datareader ADD MEMBER [app name] '，將使用者新增至角色</span><span class="sxs-lookup"><span data-stu-id="29040-132">Add user to role by running command 'exec sp_addrolemember 'db_datareader', [app name]'  Or  'ALTER ROLE db_datareader ADD MEMBER [app name]'</span></span>

>[!NOTE]
><span data-ttu-id="29040-133">若要撤銷在 Azure Active Directory 中註冊的任何應用程式的存取權，請參閱 Azure 檔中關於 [移除已註冊的應用程式](https://docs.microsoft.com/azure/active-directory/develop/quickstart-remove-app)。</span><span class="sxs-lookup"><span data-stu-id="29040-133">To revoke access to any app registered in Azure Active Directory, refer the Azure documentation on [removing a registered app](https://docs.microsoft.com/azure/active-directory/develop/quickstart-remove-app).</span></span>

### <a name="connection-settings"></a><span data-ttu-id="29040-134">連接設定</span><span class="sxs-lookup"><span data-stu-id="29040-134">Connection settings</span></span>

<span data-ttu-id="29040-135">若要將 Microsoft SQL server 連接器連線至資料來源，您必須設定要編目的資料庫伺服器和部署代理程式。</span><span class="sxs-lookup"><span data-stu-id="29040-135">To connect your Microsoft SQL server connector to a data source, you must configure the database server you want crawled and the on-prem agent.</span></span> <span data-ttu-id="29040-136">然後，您就可以使用必要的驗證方法來連接至資料庫。</span><span class="sxs-lookup"><span data-stu-id="29040-136">You can then connect to the database with the required authentication method.</span></span>

> [!NOTE] 
> <span data-ttu-id="29040-137">您的資料庫必須執行 SQL server 版本2008或更新版本，Microsoft SQL server 連接器才能連線。</span><span class="sxs-lookup"><span data-stu-id="29040-137">Your database must run SQL server version 2008 or later for the Microsoft SQL server connector to be able to connect.</span></span>

<span data-ttu-id="29040-138">針對 Azure SQL connector，您只需要指定您要連線的伺服器名稱或 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="29040-138">For the Azure SQL connector, you only need to specify the server name or IP address you want to connect to.</span></span> <span data-ttu-id="29040-139">Azure SQL connector 只支援 Azure Active Directory 開啟識別碼 connect (OIDC) authentication，以連接至資料庫。</span><span class="sxs-lookup"><span data-stu-id="29040-139">Azure SQL connector only supports Azure Active Directory Open ID connect (OIDC) authentication to connect to the database.</span></span>

<span data-ttu-id="29040-140">為了增加安全性，您可以為 Azure SQL server 或資料庫設定 IP 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="29040-140">For added security, you may configure IP firewall rules for your Azure SQL server or database.</span></span> <span data-ttu-id="29040-141">若要深入瞭解設定 IP 防火牆規則，請參閱 [IP 防火牆規則](https://docs.microsoft.com/azure/azure-sql/database/firewall-configure)的檔。</span><span class="sxs-lookup"><span data-stu-id="29040-141">To learn more about setting up IP firewall rules, refer documentation on [IP firewall rules](https://docs.microsoft.com/azure/azure-sql/database/firewall-configure).</span></span> <span data-ttu-id="29040-142">在 [防火牆設定] 中新增下列用戶端 IP 範圍。</span><span class="sxs-lookup"><span data-stu-id="29040-142">Add the following client IP ranges in the firewall settings.</span></span>

| <span data-ttu-id="29040-143">地區</span><span class="sxs-lookup"><span data-stu-id="29040-143">Region</span></span> | <span data-ttu-id="29040-144">IP 範圍</span><span class="sxs-lookup"><span data-stu-id="29040-144">IP Range</span></span> |
| ------------ | ------------ |
| <span data-ttu-id="29040-145">NAM</span><span class="sxs-lookup"><span data-stu-id="29040-145">NAM</span></span> | <span data-ttu-id="29040-146">52.250.92.252/30、52.224.250.216/30</span><span class="sxs-lookup"><span data-stu-id="29040-146">52.250.92.252/30, 52.224.250.216/30</span></span> |
| <span data-ttu-id="29040-147">EUR</span><span class="sxs-lookup"><span data-stu-id="29040-147">EUR</span></span> | <span data-ttu-id="29040-148">20.54.41.208/30、51.105.159.88/30</span><span class="sxs-lookup"><span data-stu-id="29040-148">20.54.41.208/30, 51.105.159.88/30</span></span> |
| <span data-ttu-id="29040-149">APC</span><span class="sxs-lookup"><span data-stu-id="29040-149">APC</span></span> | <span data-ttu-id="29040-150">52.139.188.212/30、20.43.146.44/30</span><span class="sxs-lookup"><span data-stu-id="29040-150">52.139.188.212/30, 20.43.146.44/30</span></span> |

<span data-ttu-id="29040-151">若要搜尋您的資料庫內容，當您設定連接器時，必須指定 SQL 查詢。</span><span class="sxs-lookup"><span data-stu-id="29040-151">To search your database content, you must specify SQL queries when you configure the connector.</span></span> <span data-ttu-id="29040-152">這些 SQL 查詢必須命名所有要索引的資料庫資料欄 (也就是說，來源屬性) ，包括需要執行以取得所有欄的任何 SQL 聯接。</span><span class="sxs-lookup"><span data-stu-id="29040-152">These SQL queries need to name all the database columns that you want to index (that is, source properties), including any SQL joins that need to be performed to get all the columns.</span></span> <span data-ttu-id="29040-153">若要限制存取搜尋結果，您必須在設定連接器時，指定 (ACLs) 中的存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="29040-153">To restrict access to search results, you must specify Access Control Lists (ACLs) within SQL queries when you configure the connector.</span></span>

## <a name="step-3a-full-crawl-required"></a><span data-ttu-id="29040-154">步驟3a：必要的完整編目 () </span><span class="sxs-lookup"><span data-stu-id="29040-154">Step 3a: Full crawl (Required)</span></span>

<span data-ttu-id="29040-155">在這個步驟中，您會設定執行資料庫完整編目的 SQL 查詢。</span><span class="sxs-lookup"><span data-stu-id="29040-155">In this step, you configure the SQL query that runs a full crawl of the database.</span></span> <span data-ttu-id="29040-156">完整編目會選取所有欄或屬性，以選取 [ **查詢**]、[ **搜尋**] 或 [ **取得**] 選項。</span><span class="sxs-lookup"><span data-stu-id="29040-156">The full crawl selects all the columns or properties where you want to select the options **Query**, **Search**, or **Retrieve**.</span></span> <span data-ttu-id="29040-157">您也可以指定 ACL 欄，以限制搜尋結果對特定使用者或群組的存取。</span><span class="sxs-lookup"><span data-stu-id="29040-157">You can also specify ACL columns to restrict access of search results to specific users or groups.</span></span>

> [!Tip]
> <span data-ttu-id="29040-158">若要取得所需的所有欄，您可以加入多個表格。</span><span class="sxs-lookup"><span data-stu-id="29040-158">To get all the columns that you need, you can join multiple tables.</span></span>

![腳本顯示 OrderTable 及 AclTable （含範例屬性）](media/MSSQL-fullcrawl.png)

### <a name="select-data-columns-required-and-acl-columns-optional"></a><span data-ttu-id="29040-160"> (必要) 和 ACL 欄 (選用) 選取資料欄位</span><span class="sxs-lookup"><span data-stu-id="29040-160">Select data columns (Required) and ACL columns (Optional)</span></span>

<span data-ttu-id="29040-161">這個範例會示範五個數據列的選取範圍，其中包含搜尋的資料： [訂單 Id]、[OrderTitle]、[OrderDesc]、[CreatedDateTime] 及 [IsDeleted]。</span><span class="sxs-lookup"><span data-stu-id="29040-161">The example demonstrates a selection of five data columns that hold the data for the search: OrderId, OrderTitle, OrderDesc, CreatedDateTime, and IsDeleted.</span></span> <span data-ttu-id="29040-162">若要設定每個資料列的查看許可權，您可以選擇性地選取下列 ACL 欄： AllowedUsers、AllowedGroups、DeniedUsers 及 DeniedGroups。</span><span class="sxs-lookup"><span data-stu-id="29040-162">To set view permissions for each row of data, you can optionally select these ACL columns: AllowedUsers, AllowedGroups, DeniedUsers, and DeniedGroups.</span></span> <span data-ttu-id="29040-163">所有的資料欄位也都有 **查詢**、 **搜尋** 或 **檢索** 的選項。</span><span class="sxs-lookup"><span data-stu-id="29040-163">All these data columns also have the options to **Query**, **Search**, or **Retrieve**.</span></span>

<span data-ttu-id="29040-164">選取下列範例查詢所示的資料行： `SELECT OrderId, OrderTitle, OrderDesc, AllowedUsers, AllowedGroups, DeniedUsers, DeniedGroups, CreatedDateTime, IsDeleted`</span><span class="sxs-lookup"><span data-stu-id="29040-164">Select data columns as shown in this example query: `SELECT OrderId, OrderTitle, OrderDesc, AllowedUsers, AllowedGroups, DeniedUsers, DeniedGroups, CreatedDateTime, IsDeleted`</span></span>

<span data-ttu-id="29040-165">若要管理搜尋結果的存取權，您可以在查詢中指定一或多個 ACL 欄。</span><span class="sxs-lookup"><span data-stu-id="29040-165">To manage access to the search results, you can specify one or more ACL columns in the query.</span></span> <span data-ttu-id="29040-166">SQL connector 可讓您控制每個記錄層級的存取。</span><span class="sxs-lookup"><span data-stu-id="29040-166">The SQL connector allows you to control access at per record level.</span></span> <span data-ttu-id="29040-167">您可以選擇對資料表中的所有記錄使用相同的存取控制。</span><span class="sxs-lookup"><span data-stu-id="29040-167">You can choose to have the same access control for all records in a table.</span></span> <span data-ttu-id="29040-168">如果 ACL 資訊儲存在不同的資料表中，您可能必須在查詢中使用這些資料表進行聯接。</span><span class="sxs-lookup"><span data-stu-id="29040-168">If the ACL information is stored in a separate table, you might have to do a join with those tables in your query.</span></span>

<span data-ttu-id="29040-169">在上述查詢中使用每個 ACL 欄的描述如下。</span><span class="sxs-lookup"><span data-stu-id="29040-169">The use of each of the ACL columns in the above query is described below.</span></span> <span data-ttu-id="29040-170">下列清單說明四種 **存取控制機制**。</span><span class="sxs-lookup"><span data-stu-id="29040-170">The following list explains the four **access control mechanisms**.</span></span>

- <span data-ttu-id="29040-171">**AllowedUsers**：此欄會指定可以存取搜尋結果的使用者 IDs 清單。</span><span class="sxs-lookup"><span data-stu-id="29040-171">**AllowedUsers**: This column specifies the list of user IDs who can access the search results.</span></span> <span data-ttu-id="29040-172">在下列範例中，使用者清單為： john@contoso.com、keith@contoso.com 和 lisa@contoso.com 只有具有「訂單 Id」的記錄存取權 = 12。</span><span class="sxs-lookup"><span data-stu-id="29040-172">In the following example, list of users: john@contoso.com, keith@contoso.com, and lisa@contoso.com would only have access to a record with OrderId = 12.</span></span>
- <span data-ttu-id="29040-173">**AllowedGroups**：此欄會指定可以存取搜尋結果的使用者群組。</span><span class="sxs-lookup"><span data-stu-id="29040-173">**AllowedGroups**: This column specifies the group of users who will be able to access the search results.</span></span> <span data-ttu-id="29040-174">在下列範例中，group sales-team@contoso.com 只會具有「訂單 Id = 12」的記錄存取權。</span><span class="sxs-lookup"><span data-stu-id="29040-174">In the following example, group sales-team@contoso.com would only have access to record with OrderId = 12.</span></span>
- <span data-ttu-id="29040-175">**DeniedUsers**：此欄會 **指定沒有搜尋** 結果存取權的使用者清單。</span><span class="sxs-lookup"><span data-stu-id="29040-175">**DeniedUsers**: This column specifies the list of users who do **not** have access to the search results.</span></span> <span data-ttu-id="29040-176">在下列範例中，使用者 john@contoso.com 及 keith@contoso.com 無法存取具有「訂單 Id」的記錄，而其他所有人都可以存取這筆記錄。</span><span class="sxs-lookup"><span data-stu-id="29040-176">In the following example, users john@contoso.com and keith@contoso.com do not have access to record with OrderId = 13, whereas everyone else has access to this record.</span></span>
- <span data-ttu-id="29040-177">**DeniedGroups**：此欄 **指定沒有搜尋** 結果存取權的使用者群組。</span><span class="sxs-lookup"><span data-stu-id="29040-177">**DeniedGroups**: This column specifies the group of users who do **not** have access to the search results.</span></span> <span data-ttu-id="29040-178">在下列範例中，群組 engg-team@contoso.com 及 pm-team@contoso.com 沒有具有「訂單 Id」的記錄存取權，而其他所有人都可以存取這筆記錄。</span><span class="sxs-lookup"><span data-stu-id="29040-178">In the following example, groups engg-team@contoso.com and pm-team@contoso.com do not have access to record with OrderId = 15, whereas everyone else has access to this record.</span></span>  

![顯示 OrderTable 及 AclTable （含範例屬性）的範例資料](media/MSSQL-ACL1.png)

### <a name="supported-data-types"></a><span data-ttu-id="29040-180">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="29040-180">Supported data types</span></span>

<span data-ttu-id="29040-181">下表摘要列出 MS SQL 和 Azure SQL 連接器中支援的 SQL 資料類型。</span><span class="sxs-lookup"><span data-stu-id="29040-181">The below table summarizes the SQL data types that are supported in the MS SQL and Azure SQL connectors.</span></span> <span data-ttu-id="29040-182">該表也會摘要支援的 SQL 資料類型的索引資料類型。</span><span class="sxs-lookup"><span data-stu-id="29040-182">The table also summarizes the indexing data type for the supported SQL data type.</span></span> <span data-ttu-id="29040-183">若要深入瞭解 Microsoft Graph 連接器支援的索引資料類型，請參閱 [屬性資源類型](https://docs.microsoft.com/graph/api/resources/property?view=graph-rest-beta#properties&preserve-view=true)的檔。</span><span class="sxs-lookup"><span data-stu-id="29040-183">To learn more about Microsoft Graph connectors supported data types for indexing, refer documentation on [property resource types](https://docs.microsoft.com/graph/api/resources/property?view=graph-rest-beta#properties&preserve-view=true).</span></span>

| <span data-ttu-id="29040-184">類別</span><span class="sxs-lookup"><span data-stu-id="29040-184">Category</span></span> | <span data-ttu-id="29040-185">來源資料類型</span><span class="sxs-lookup"><span data-stu-id="29040-185">Source data type</span></span> | <span data-ttu-id="29040-186">索引資料類型</span><span class="sxs-lookup"><span data-stu-id="29040-186">Indexing data type</span></span> |
| ------------ | ------------ | ------------ |
| <span data-ttu-id="29040-187">日期和時間</span><span class="sxs-lookup"><span data-stu-id="29040-187">Date and time</span></span> | <span data-ttu-id="29040-188">date</span><span class="sxs-lookup"><span data-stu-id="29040-188">date</span></span> <br> <span data-ttu-id="29040-189">datetime</span><span class="sxs-lookup"><span data-stu-id="29040-189">datetime</span></span> <br> <span data-ttu-id="29040-190">datetime2</span><span class="sxs-lookup"><span data-stu-id="29040-190">datetime2</span></span> <br> <span data-ttu-id="29040-191">Smalldatetime</span><span class="sxs-lookup"><span data-stu-id="29040-191">smalldatetime</span></span> | <span data-ttu-id="29040-192">datetime</span><span class="sxs-lookup"><span data-stu-id="29040-192">datetime</span></span> |
| <span data-ttu-id="29040-193">完全數值</span><span class="sxs-lookup"><span data-stu-id="29040-193">Exact numeric</span></span> | <span data-ttu-id="29040-194">Bigint</span><span class="sxs-lookup"><span data-stu-id="29040-194">bigint</span></span> <br> <span data-ttu-id="29040-195">int</span><span class="sxs-lookup"><span data-stu-id="29040-195">int</span></span> <br> <span data-ttu-id="29040-196">Smallint</span><span class="sxs-lookup"><span data-stu-id="29040-196">smallint</span></span> <br> <span data-ttu-id="29040-197">Tinyint</span><span class="sxs-lookup"><span data-stu-id="29040-197">tinyint</span></span> | <span data-ttu-id="29040-198">int64</span><span class="sxs-lookup"><span data-stu-id="29040-198">int64</span></span> |
| <span data-ttu-id="29040-199">完全數值</span><span class="sxs-lookup"><span data-stu-id="29040-199">Exact numeric</span></span> | <span data-ttu-id="29040-200">位</span><span class="sxs-lookup"><span data-stu-id="29040-200">bit</span></span> | <span data-ttu-id="29040-201">布林值</span><span class="sxs-lookup"><span data-stu-id="29040-201">boolean</span></span> |
| <span data-ttu-id="29040-202">近似數值</span><span class="sxs-lookup"><span data-stu-id="29040-202">Approximate numeric</span></span> | <span data-ttu-id="29040-203">float</span><span class="sxs-lookup"><span data-stu-id="29040-203">float</span></span> <br> <span data-ttu-id="29040-204">真正</span><span class="sxs-lookup"><span data-stu-id="29040-204">real</span></span> | <span data-ttu-id="29040-205">double</span><span class="sxs-lookup"><span data-stu-id="29040-205">double</span></span> |
| <span data-ttu-id="29040-206">字元字串</span><span class="sxs-lookup"><span data-stu-id="29040-206">Character string</span></span> | <span data-ttu-id="29040-207">字元</span><span class="sxs-lookup"><span data-stu-id="29040-207">char</span></span> <br> <span data-ttu-id="29040-208">Varchar</span><span class="sxs-lookup"><span data-stu-id="29040-208">varchar</span></span> <br> <span data-ttu-id="29040-209">文字</span><span class="sxs-lookup"><span data-stu-id="29040-209">text</span></span> | <span data-ttu-id="29040-210">string</span><span class="sxs-lookup"><span data-stu-id="29040-210">string</span></span> |
| <span data-ttu-id="29040-211">Unicode 字元字串</span><span class="sxs-lookup"><span data-stu-id="29040-211">Unicode character strings</span></span> | <span data-ttu-id="29040-212">Nchar</span><span class="sxs-lookup"><span data-stu-id="29040-212">nchar</span></span> <br> <span data-ttu-id="29040-213">Nvarchar</span><span class="sxs-lookup"><span data-stu-id="29040-213">nvarchar</span></span> <br> <span data-ttu-id="29040-214">Ntext</span><span class="sxs-lookup"><span data-stu-id="29040-214">ntext</span></span> | <span data-ttu-id="29040-215">string</span><span class="sxs-lookup"><span data-stu-id="29040-215">string</span></span> |
| <span data-ttu-id="29040-216">其他資料類型</span><span class="sxs-lookup"><span data-stu-id="29040-216">Other data types</span></span> | <span data-ttu-id="29040-217">唯一</span><span class="sxs-lookup"><span data-stu-id="29040-217">uniqueidentifier</span></span> | <span data-ttu-id="29040-218">string</span><span class="sxs-lookup"><span data-stu-id="29040-218">string</span></span> |

<span data-ttu-id="29040-219">對於目前不是直接支援的任何其他資料類型，此資料行必須明確地轉換成支援的資料類型。</span><span class="sxs-lookup"><span data-stu-id="29040-219">For any other data type currently not directly supported, the column needs to be explicitly cast to a supported data type.</span></span>

### <a name="watermark-required"></a><span data-ttu-id="29040-220">浮水印 (必要) </span><span class="sxs-lookup"><span data-stu-id="29040-220">Watermark (Required)</span></span>

<span data-ttu-id="29040-221">若要防止資料庫超載，連接器會批次並繼續完整編目的查詢。</span><span class="sxs-lookup"><span data-stu-id="29040-221">To prevent overloading the database, the connector batches and resumes full-crawl queries with a full-crawl watermark column.</span></span> <span data-ttu-id="29040-222">使用 [浮水印] 資料行的值，每個後續的批次都會取得，而查詢會從最後一個檢查點繼續。</span><span class="sxs-lookup"><span data-stu-id="29040-222">By using the value of the watermark column, each subsequent batch is fetched, and querying is resumed from the last checkpoint.</span></span> <span data-ttu-id="29040-223">實質上，這種機制會控制完整編目的資料重新整理。</span><span class="sxs-lookup"><span data-stu-id="29040-223">Essentially this mechanisms controls data refresh for full crawls.</span></span>

<span data-ttu-id="29040-224">建立浮水印的查詢程式碼片段，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="29040-224">Create query snippets for watermarks as shown in these examples:</span></span>

- <span data-ttu-id="29040-225">`WHERE (CreatedDateTime > @watermark)`.</span><span class="sxs-lookup"><span data-stu-id="29040-225">`WHERE (CreatedDateTime > @watermark)`.</span></span> <span data-ttu-id="29040-226">使用保留的關鍵字來引用浮水印欄名稱 `@watermark` 。</span><span class="sxs-lookup"><span data-stu-id="29040-226">Cite the watermark column name with the reserved keyword `@watermark`.</span></span> <span data-ttu-id="29040-227">如果浮水印欄的排序次序是遞增的，請使用 `>` ，否則請使用 `<` 。</span><span class="sxs-lookup"><span data-stu-id="29040-227">If the sort order of the watermark column is ascending, use `>`; otherwise, use `<`.</span></span>
- <span data-ttu-id="29040-228">`ORDER BY CreatedDateTime ASC`.</span><span class="sxs-lookup"><span data-stu-id="29040-228">`ORDER BY CreatedDateTime ASC`.</span></span> <span data-ttu-id="29040-229">在 [浮水印] 欄上以遞增或遞減順序排序。</span><span class="sxs-lookup"><span data-stu-id="29040-229">Sort on the watermark column in ascending or descending order.</span></span>

<span data-ttu-id="29040-230">在下一個影像所示的設定中， `CreatedDateTime` 是選取的 [浮水印] 欄。</span><span class="sxs-lookup"><span data-stu-id="29040-230">In the configuration shown in the following image, `CreatedDateTime` is the selected watermark column.</span></span> <span data-ttu-id="29040-231">若要取得第一批列，請指定 [浮水印] 資料行的資料類型。</span><span class="sxs-lookup"><span data-stu-id="29040-231">To fetch the first batch of rows, specify the data type of the watermark column.</span></span> <span data-ttu-id="29040-232">在此情況下，資料類型為 `DateTime` 。</span><span class="sxs-lookup"><span data-stu-id="29040-232">In this case, the data type is `DateTime`.</span></span>

![浮水印欄設定](media/MSSQL-watermark.png)

<span data-ttu-id="29040-234">第 **一個查詢** 會使用： "CreatedDateTime > 1753 年1月1日，00:00:00" (最小值 DateTime 的資料類型) 。</span><span class="sxs-lookup"><span data-stu-id="29040-234">The first query fetches the first **N** number of rows by using: "CreatedDateTime > January 1, 1753 00:00:00" (min value of DateTime data type).</span></span> <span data-ttu-id="29040-235">提取第一個批次之後， `CreatedDateTime` 如果資料列是以遞增順序排序，則會將批次中傳回的最高值儲存為檢查點。</span><span class="sxs-lookup"><span data-stu-id="29040-235">After the first batch is fetched, the highest value of `CreatedDateTime` returned in the batch is saved as the checkpoint if the rows are sorted in ascending order.</span></span> <span data-ttu-id="29040-236">範例是 03:00:00 2019 年3月1日。</span><span class="sxs-lookup"><span data-stu-id="29040-236">An example is March 1, 2019 03:00:00.</span></span> <span data-ttu-id="29040-237">然後，在查詢中使用「CreatedDateTime > 三月份1，2019 03:00:00」提取下一批 **N** 列。</span><span class="sxs-lookup"><span data-stu-id="29040-237">Then the next batch of **N** rows is fetched by using "CreatedDateTime > March 1, 2019 03:00:00" in the query.</span></span>

### <a name="skipping-soft-deleted-rows-optional"></a><span data-ttu-id="29040-238">跳過虛刪除的列 (選用) </span><span class="sxs-lookup"><span data-stu-id="29040-238">Skipping soft-deleted rows (Optional)</span></span>

<span data-ttu-id="29040-239">若要排除資料庫中虛刪除的列的索引，請指定虛刪除的列名稱和值，以指出刪除列的資料行。</span><span class="sxs-lookup"><span data-stu-id="29040-239">To exclude soft-deleted rows in your database from being indexed, specify the soft-delete column name and value that indicates the row is deleted.</span></span>

![虛刪除設定： "Soft delete column" 和 "soft delete 欄的值，表示已刪除的資料列"](media/MSSQL-softdelete.png)

### <a name="full-crawl-manage-search-permissions"></a><span data-ttu-id="29040-241">完整編目：管理搜尋許可權</span><span class="sxs-lookup"><span data-stu-id="29040-241">Full crawl: Manage search permissions</span></span>

<span data-ttu-id="29040-242">選取 [ **管理許可權** ]，以選擇用來指定存取控制機制 (ACL) 欄的各種存取控制。</span><span class="sxs-lookup"><span data-stu-id="29040-242">Select **Manage permissions** to choose the various access control (ACL) columns that specify the access control mechanism.</span></span> <span data-ttu-id="29040-243">選取您在完整編目 SQL 查詢中所指定的資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="29040-243">Select the column name you specified in the full crawl SQL query.</span></span>

<span data-ttu-id="29040-244">每個 ACL 欄都應該是多重值欄。</span><span class="sxs-lookup"><span data-stu-id="29040-244">Each of the ACL columns is expected to be a multi-valued column.</span></span> <span data-ttu-id="29040-245">您可以使用分隔符號（如分號 (; ) 、逗號 (、) 等等）來分隔這些多個 ID 值。</span><span class="sxs-lookup"><span data-stu-id="29040-245">These multiple ID values can be separated by separators such as semicolon (;), comma (,), and so on.</span></span> <span data-ttu-id="29040-246">您必須在 [ **值分隔符號** ] 欄位中指定此分隔符號。</span><span class="sxs-lookup"><span data-stu-id="29040-246">You need to specify this separator in the **value separator** field.</span></span>

<span data-ttu-id="29040-247">下列識別碼類型可供使用 ACLs：</span><span class="sxs-lookup"><span data-stu-id="29040-247">The following ID types are supported for using as ACLs:</span></span>

- <span data-ttu-id="29040-248">**使用者主體名稱 (upn)**：使用者主要名稱 (upn) 是以電子郵件地址格式的系統使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="29040-248">**User Principal Name (UPN)**: A User Principal Name (UPN) is the name of a system user in an email address format.</span></span> <span data-ttu-id="29040-249">UPN (例如： john.doe@domain.com) 會包含 (登入名稱) 、分隔符號 (@ 符號) 和功能變數名稱 (UPN 尾碼) 的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="29040-249">A UPN (for example: john.doe@domain.com) consists of the username (logon name), separator (the @ symbol), and domain name (UPN suffix).</span></span>
- <span data-ttu-id="29040-250">**Azure Active Directory (AAD) 識別碼**：在 Azure AD 中，每個使用者或群組都有一個類似 ' e0d3ad3d-0000-1111-2222-3c5f5c52ab9b ' 的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="29040-250">**Azure Active Directory (AAD) ID**: In Azure AD, every user or group has an object ID that looks something like 'e0d3ad3d-0000-1111-2222-3c5f5c52ab9b'.</span></span>
- <span data-ttu-id="29040-251">**Active Directory (AD) 安全性** 識別碼：在內部部署 AD 安裝程式中，每個使用者和群組都有一個無法變化的唯一安全性識別碼，看起來像是-1-5-21-3878594291-2115959936-132693609-65242。 '</span><span class="sxs-lookup"><span data-stu-id="29040-251">**Active Directory (AD) Security ID**: In an on-premises AD setup, every user and group have an immutable, unique security identifier that looks something like 'S-1-5-21-3878594291-2115959936-132693609-65242.'</span></span>

![設定存取控制清單的搜尋許可權設定](media/MSSQL-ACL2.png)

## <a name="step-3b-incremental-crawl-optional"></a><span data-ttu-id="29040-253">步驟3b：增量編目 (選用) </span><span class="sxs-lookup"><span data-stu-id="29040-253">Step 3b: Incremental crawl (Optional)</span></span>

<span data-ttu-id="29040-254">在此選用的步驟中，請提供 SQL 查詢，以執行資料庫的增量式編目。</span><span class="sxs-lookup"><span data-stu-id="29040-254">In this optional step, provide a SQL query to run an incremental crawl of the database.</span></span> <span data-ttu-id="29040-255">在此查詢中，SQL 連接器會決定自上次累加編目以來對資料所做的任何變更。</span><span class="sxs-lookup"><span data-stu-id="29040-255">With this query, the SQL connector determines any changes to the data since the last incremental crawl.</span></span> <span data-ttu-id="29040-256">在完整編目中，選取 [所有欄]，以選取 [ **查詢**]、[ **搜尋**] 或 [ **取得**] 選項。</span><span class="sxs-lookup"><span data-stu-id="29040-256">As in the full crawl, select all columns where you want to select the options **Query**, **Search**, or **Retrieve**.</span></span> <span data-ttu-id="29040-257">指定您在完整編目查詢中指定的相同 ACL 欄集。</span><span class="sxs-lookup"><span data-stu-id="29040-257">Specify the same set of ACL columns that you specified in the full crawl query.</span></span>

<span data-ttu-id="29040-258">下列映射中的元件類似于完整編目元件，但有一個例外。</span><span class="sxs-lookup"><span data-stu-id="29040-258">The components in the following image resemble the full crawl components with one exception.</span></span> <span data-ttu-id="29040-259">在此情況下，"ModifiedDateTime" 是選取的浮水印欄。</span><span class="sxs-lookup"><span data-stu-id="29040-259">In this case, "ModifiedDateTime" is the selected watermark column.</span></span> <span data-ttu-id="29040-260">查看 [完整編目步驟](#step-3a-full-crawl-required) ，以瞭解如何撰寫累加編目查詢，並以範例顯示下列影像。</span><span class="sxs-lookup"><span data-stu-id="29040-260">Review the [full crawl steps](#step-3a-full-crawl-required) to learn how to write your incremental crawl query and see the following image as an example.</span></span>

![新增編目腳本，顯示可使用的 OrderTable、AclTable 和範例屬性。](media/MSSQL-incrcrawl.png)

## <a name="step-4-assign-property-labels"></a><span data-ttu-id="29040-262">步驟4：指派屬性標籤</span><span class="sxs-lookup"><span data-stu-id="29040-262">Step 4: Assign property labels</span></span>

<span data-ttu-id="29040-263">遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。</span><span class="sxs-lookup"><span data-stu-id="29040-263">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>

<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup 
instructions.-->

## <a name="step-5-manage-schema"></a><span data-ttu-id="29040-264">步驟5：管理架構</span><span class="sxs-lookup"><span data-stu-id="29040-264">Step 5: Manage schema</span></span>

<span data-ttu-id="29040-265">遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。</span><span class="sxs-lookup"><span data-stu-id="29040-265">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup 
instructions.-->

## <a name="step-6-manage-search-permissions"></a><span data-ttu-id="29040-266">步驟6：管理搜尋許可權</span><span class="sxs-lookup"><span data-stu-id="29040-266">Step 6: Manage search permissions</span></span>

<span data-ttu-id="29040-267">您可以選擇使用完整編目 [畫面中所指定的 ACLs](#full-crawl-manage-search-permissions) ，也可以覆寫它們，讓每個人都能看到您的內容。</span><span class="sxs-lookup"><span data-stu-id="29040-267">You can choose to use the [ACLs specified in the full crawl screen](#full-crawl-manage-search-permissions) or you can override them to make your content visible to everyone.</span></span>

## <a name="step-7-choose-refresh-settings"></a><span data-ttu-id="29040-268">步驟7：選擇重新整理設定</span><span class="sxs-lookup"><span data-stu-id="29040-268">Step 7: Choose refresh settings</span></span>

<span data-ttu-id="29040-269">遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。</span><span class="sxs-lookup"><span data-stu-id="29040-269">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup 
instructions.-->

## <a name="step-8-review-connection"></a><span data-ttu-id="29040-270">步驟8：檢查連線</span><span class="sxs-lookup"><span data-stu-id="29040-270">Step 8: Review connection</span></span>

<span data-ttu-id="29040-271">遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。</span><span class="sxs-lookup"><span data-stu-id="29040-271">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup 
instructions.-->

<!---## Next steps: Customize the search results page

Create your own verticals and result types, so end users can view search results from new connections. Without this step, data from your connection won't show up on the search results page.

To learn more about how to create your verticals and MRTs, see [Search results page customization](customize-search-page.md).-->

<!---## Troubleshooting-->

<!---Insert troubleshooting recommendations for this data source-->

## <a name="limitations"></a><span data-ttu-id="29040-272">限制</span><span class="sxs-lookup"><span data-stu-id="29040-272">Limitations</span></span>

<span data-ttu-id="29040-273">在預覽版本中，SQL 連接器具有這些限制：</span><span class="sxs-lookup"><span data-stu-id="29040-273">The SQL connectors have these limitations in the preview release:</span></span>

- <span data-ttu-id="29040-274">Microsoft SQL server connector：內部部署資料庫必須執行 SQL server 版本2008或更新版本。</span><span class="sxs-lookup"><span data-stu-id="29040-274">Microsoft SQL server connector: The on-premises database must run SQL server version 2008 or later.</span></span>
- <span data-ttu-id="29040-275">主控 Azure SQL database 的 M365 訂閱和 Azure 訂閱 () 必須位於相同的 Azure Active Directory 中。</span><span class="sxs-lookup"><span data-stu-id="29040-275">The M365 subscription and Azure subscription (hosting Azure SQL database) must lie within the same Azure Active Directory.</span></span>
- <span data-ttu-id="29040-276">只有使用使用者主要名稱 (UPN) 、Azure Active Directory (Azure AD) 或 Active Directory 安全性才能支援 ACLs。</span><span class="sxs-lookup"><span data-stu-id="29040-276">ACLs are only supported by using a User Principal Name (UPN), Azure Active Directory (Azure AD), or Active Directory Security.</span></span>
- <span data-ttu-id="29040-277">不支援在資料庫欄中編制豐富內容的索引。</span><span class="sxs-lookup"><span data-stu-id="29040-277">Indexing rich content inside database columns is not supported.</span></span> <span data-ttu-id="29040-278">這類內容的範例為 HTML、JSON、XML、blob 及檔 parsings，以資料庫資料欄中的連結形式存在。</span><span class="sxs-lookup"><span data-stu-id="29040-278">Examples of such content are HTML, JSON, XML, blobs, and document parsings that exist as links inside the database columns.</span></span>
