---
title: Microsoft Search 的 Microsoft SQL 連接器
ms.author: mounika.narayanan
author: monaray
manager: mnirkhe
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 為 Microsoft Search 設定 Microsoft SQL 連接器。
ms.openlocfilehash: a073a6d3f226e5f8b0ea297494a8889f1f50bab1
ms.sourcegitcommit: 21361af7c244ffd6ff8689fd0ff0daa359bf4129
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/14/2019
ms.locfileid: "38626754"
---
# <a name="microsoft-sql-server-connector"></a><span data-ttu-id="6fc9d-103">Microsoft SQL server 連接器</span><span class="sxs-lookup"><span data-stu-id="6fc9d-103">Microsoft SQL server connector</span></span>

<span data-ttu-id="6fc9d-104">Microsoft SQL server 連接器，您的組織可以探索和索引資料從內部部署 SQL Server 資料庫。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-104">With a Microsoft SQL server connector, your organization can discover and index data from an on-premises SQL Server database.</span></span> <span data-ttu-id="6fc9d-105">連接器索引指定成 Microsoft 搜尋的內容。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-105">The connector indexes specified content into Microsoft Search.</span></span> <span data-ttu-id="6fc9d-106">若要保留最新的來源資料的索引，它所支援定期完整和累加編目。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-106">To keep the index up to date with source data, it supports periodic full and incremental crawls.</span></span> <span data-ttu-id="6fc9d-107">使用 SQL Server 連接器，您也可以限制存取搜尋結果提供給特定使用者。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-107">With the SQL Server connector, you can also restrict access to search results for certain users.</span></span>

<span data-ttu-id="6fc9d-108">本文適用於 Microsoft 365 系統管理員或人設定、 執行，並監視的 Microsoft SQL server 連接器。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-108">This article is for Microsoft 365 administrators or anyone who configures, runs, and monitors a Microsoft SQL server connector.</span></span> <span data-ttu-id="6fc9d-109">本文說明如何設定連接器，連接器功能、 限制和疑難排解技巧。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-109">It explains how to configure your connector and connector capabilities, limitations, and troubleshooting techniques.</span></span>

## <a name="install-a-data-gateway"></a><span data-ttu-id="6fc9d-110">安裝資料閘道</span><span class="sxs-lookup"><span data-stu-id="6fc9d-110">Install a data gateway</span></span>
<span data-ttu-id="6fc9d-111">若要存取您的協力廠商資料，您必須安裝及設定 Microsoft Power BI 閘道。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-111">In order to access your third-party data, you must install and configure a Microsoft Power BI gateway.</span></span> <span data-ttu-id="6fc9d-112">請參閱[安裝與內部部署閘道](https://docs.microsoft.com/data-integration/gateway/service-gateway-install)若要了解更多。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-112">See [Install and on-premises gateway](https://docs.microsoft.com/data-integration/gateway/service-gateway-install) to learn more.</span></span>  

## <a name="connect-to-a-data-source"></a><span data-ttu-id="6fc9d-113">連線至資料來源</span><span class="sxs-lookup"><span data-stu-id="6fc9d-113">Connect to a data source</span></span>
<span data-ttu-id="6fc9d-114">若要連接您的 Microsoft SQL server 連接器至資料來源，您必須設定您要編目的資料庫伺服器和內部部署閘道。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-114">To connect your Microsoft SQL server connector to a data source, you must configure the database server you want crawled and the on-premises gateway.</span></span> <span data-ttu-id="6fc9d-115">您可以再連線到資料庫所需的驗證方法。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-115">You can then connect to the database with the required authentication method.</span></span>

> [!NOTE]
> <span data-ttu-id="6fc9d-116">2008 或更新版本，您的資料庫必須執行 SQL server 版本。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-116">Your database must run SQL server version 2008 or later.</span></span>

<span data-ttu-id="6fc9d-117">若要搜尋您資料庫的內容，您必須指定 SQL 查詢，當您設定連接器。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-117">To search your database content, you must specify SQL queries when you configure the connector.</span></span> <span data-ttu-id="6fc9d-118">下列 SQL 查詢必須命名為所有要索引 （亦即來源的屬性），包括任何不需要執行若要取得所有的資料行的 SQL 聯結的資料庫資料行。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-118">These SQL queries need to name all the database columns that you want to index (i.e. source properties), including any SQL joins that need to be performed to get all the columns.</span></span> <span data-ttu-id="6fc9d-119">若要限制存取權的搜尋結果，您必須指定存取控制清單 (Acl) 與 SQL 查詢時您設定 Microsoft SQL server 連接器。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-119">To restrict access to search results, you must specify Access Control Lists (ACLs) with SQL queries when you configure the Microsoft SQL server connector.</span></span>

## <a name="full-crawl-required"></a><span data-ttu-id="6fc9d-120">（必要） 的完整編目</span><span class="sxs-lookup"><span data-stu-id="6fc9d-120">Full crawl (Required)</span></span>
<span data-ttu-id="6fc9d-121">在此步驟中，您可以設定執行完整編目資料庫的 SQL 查詢。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-121">In this step, you configure the SQL query that runs a full crawl of the database.</span></span> <span data-ttu-id="6fc9d-122">完整編目會選取所有的資料行或您想要進行的屬性**設為可查詢**、**可搜尋**，或**可擷取**。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-122">The full crawl selects all the columns or properties you want to be made **queryable**, **searchable**, or **retrievable**.</span></span> <span data-ttu-id="6fc9d-123">您也可以指定限制對特定使用者或群組存取搜尋結果的 ACL 欄。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-123">You can also specify ACL columns to restrict access of search results to specific users or groups.</span></span>

> [!Tip]
> <span data-ttu-id="6fc9d-124">若要取得您需要的所有資料行，您可以加入多個資料表。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-124">To get all the columns that you need, you can join multiple tables.</span></span>

![指令碼顯示 OrderTable 和 AclTable 與範例屬性](media/MSSQL-fullcrawl.png)

### <a name="select-data-columns-required-and-acl-columns-optional"></a><span data-ttu-id="6fc9d-126">選取的資料行 （必要） 和 ACL 資料行 （選用）</span><span class="sxs-lookup"><span data-stu-id="6fc9d-126">Select data columns (Required) and ACL columns (Optional)</span></span>
<span data-ttu-id="6fc9d-127">此範例將示範如何選取項目保留搜尋的資料的五個資料欄的： OrderId、 OrderTitle、 OrderDesc、 CreatedDateTime 及 IsDeleted。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-127">The example demonstrates selection of five data columns that hold the data for the search: OrderId, OrderTitle, OrderDesc, CreatedDateTime, and IsDeleted.</span></span> <span data-ttu-id="6fc9d-128">若要設定檢視權限的每一列資料，您可以選擇性地選取這些 ACL 欄： AllowedUsers、 AllowedGroups、 DeniedUsers 及 DeniedGroups。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-128">To set view permissions for each row of data, you can optionally select these ACL columns: AllowedUsers, AllowedGroups, DeniedUsers, and DeniedGroups.</span></span> <span data-ttu-id="6fc9d-129">您可以進行所有這些資料行**設為可查詢**、**可搜尋**，或**可擷取**。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-129">All these data columns can be made **queryable**, **searchable**, or **retrievable**.</span></span>

<span data-ttu-id="6fc9d-130">此範例會查詢中所示，請選取的資料行：`SELECT OrderId, OrderTitle, OrderDesc, AllowedUsers, AllowedGroups, DeniedUsers, DeniedGroups, CreatedDateTime, IsDeleted`</span><span class="sxs-lookup"><span data-stu-id="6fc9d-130">Select data columns as shown in this example query: `SELECT OrderId, OrderTitle, OrderDesc, AllowedUsers, AllowedGroups, DeniedUsers, DeniedGroups, CreatedDateTime, IsDeleted`</span></span>

### <a name="watermark-required"></a><span data-ttu-id="6fc9d-131">浮水印 （必要）</span><span class="sxs-lookup"><span data-stu-id="6fc9d-131">Watermark (Required)</span></span>
<span data-ttu-id="6fc9d-132">若要防止多載資料庫，連接器批次，而且會繼續具有完整編目浮水印資料行的完整編目查詢。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-132">To prevent overloading the database, the connector batches and resumes full-crawl queries with a full-crawl watermark column.</span></span> <span data-ttu-id="6fc9d-133">藉由使用浮水印資料行的值，會擷取每一個後續的批次，並查詢從最後一個的檢查點繼續執行。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-133">By using the value of the watermark column, each subsequent batch is fetched, and querying is resumed from the last checkpoint.</span></span> <span data-ttu-id="6fc9d-134">基本上，這是一種機制可控制的完整編目的資料重新整理。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-134">Essentially this is a mechanism to control data refresh for full crawls.</span></span>

<span data-ttu-id="6fc9d-135">建立查詢程式碼片段的浮水印，如以下範例所示：</span><span class="sxs-lookup"><span data-stu-id="6fc9d-135">Create query snippets for watermarks as shown in these examples:</span></span>
* <span data-ttu-id="6fc9d-136">`WHERE (CreatedDateTime > @watermark)`.</span><span class="sxs-lookup"><span data-stu-id="6fc9d-136"></span></span> <span data-ttu-id="6fc9d-137">引用浮水印資料行名稱與保留的關鍵字`@watermark`。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-137">Cite the watermark column name with the reserved keyword `@watermark`.</span></span> <span data-ttu-id="6fc9d-138">如果浮水印資料行的排序順序遞增，使用`>`;否則，請使用`<`。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-138">If the sort order of the watermark column is ascending, use `>`; otherwise, use `<`.</span></span>
* <span data-ttu-id="6fc9d-139">`ORDER BY CreatedDateTime ASC`.</span><span class="sxs-lookup"><span data-stu-id="6fc9d-139"></span></span> <span data-ttu-id="6fc9d-140">浮水印欄，以遞增或遞減順序排序。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-140">Sort on the watermark column in ascending or descending order.</span></span>

<span data-ttu-id="6fc9d-141">在下列影像所示設定`CreatedDateTime`是所選取的浮水印資料行。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-141">In the configuration shown in the following image, `CreatedDateTime` is the selected watermark column.</span></span> <span data-ttu-id="6fc9d-142">若要擷取的資料列的第一個批次，指定浮水印欄的資料類型。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-142">To fetch the first batch of rows, specify the data type of the watermark column.</span></span> <span data-ttu-id="6fc9d-143">在此例中的資料類型是`DateTime`。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-143">In this case, the data type is `DateTime`.</span></span>

![](media/MSSQL-watermark.png)

<span data-ttu-id="6fc9d-144">第一個查詢擷取資料列的第一個**N**量使用: 「 CreatedDateTime > 1753 年 1 月 1 日 00:00:00 」 （最小值的日期時間資料類型）。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-144">The first query fetches the first **N** amount of rows by using: "CreatedDateTime > January 1, 1753 00:00:00" (min value of DateTime data type).</span></span> <span data-ttu-id="6fc9d-145">第一個批次會擷取的最高值之後`CreatedDateTime`中傳回批次會儲存為檢查點，如果資料列會以遞增順序排序。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-145">After the first batch is fetched, the highest value of `CreatedDateTime` returned in the batch is saved as the checkpoint if the rows are sorted in ascending order.</span></span> <span data-ttu-id="6fc9d-146">例如，2019 年 3 月 1 日 03:00:00。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-146">An example is March 1, 2019 03:00:00.</span></span> <span data-ttu-id="6fc9d-147">然後**N**個資料列的下一個批次會擷取使用 「 CreatedDateTime > 2019 年 3 月 1 日 03:00:00 」 在查詢中。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-147">Then the next batch of **N** rows is fetched by using "CreatedDateTime > March 1, 2019 03:00:00" in the query.</span></span>

### <a name="skipping-soft-deleted-rows-optional"></a><span data-ttu-id="6fc9d-148">略過虛刪除的資料列 （選用）</span><span class="sxs-lookup"><span data-stu-id="6fc9d-148">Skipping soft-deleted rows (Optional)</span></span>
<span data-ttu-id="6fc9d-149">若要排除在編製索引的虛刪除資料庫中的資料列，請指定虛刪除資料行名稱和值，指出刪除資料列。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-149">To exclude soft-deleted rows in your database from being indexed, specify the soft-delete column name and value that indicates the row is deleted.</span></span>

![虛刪除的設定: 「 虛刪除資料行 」 和 「 值的虛刪除會指出刪除的資料列資料行 」](media/MSSQL-softdelete.png)

## <a name="incremental-crawl-optional"></a><span data-ttu-id="6fc9d-151">累加編目 （選用）</span><span class="sxs-lookup"><span data-stu-id="6fc9d-151">Incremental crawl (Optional)</span></span>
<span data-ttu-id="6fc9d-152">在此選用的步驟中，提供執行累加編目資料庫的 SQL 查詢。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-152">In this optional step, provide a SQL query to run an incremental crawl of the database.</span></span> <span data-ttu-id="6fc9d-153">此查詢中，與 Microsoft SQL server 連接器任何對資料進行變更自上次的累加編目。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-153">With this query, the Microsoft SQL server connector makes any changes to the data since the last incremental crawl.</span></span> <span data-ttu-id="6fc9d-154">如同完整編目]，選取您想要進行的所有欄**設為可查詢**、**可搜尋**，或**可擷取**。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-154">As in the full crawl, select all columns that you want to be made **queryable**, **searchable**, or **retrievable**.</span></span> <span data-ttu-id="6fc9d-155">指定相同的完整編目查詢中指定的 ACL 欄集合。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-155">Specify the same set of ACL columns that you specified in the full crawl query.</span></span>

<span data-ttu-id="6fc9d-156">下圖中的元件與類似有一個例外狀況的完整編目元件。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-156">The components in the following image resemble the full crawl components with one exception.</span></span> <span data-ttu-id="6fc9d-157">在此情況下，「 ModifiedDateTime 」 是所選取的浮水印資料行。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-157">In this case, "ModifiedDateTime" is the selected watermark column.</span></span> <span data-ttu-id="6fc9d-158">檢閱[完整編目的步驟](#full-crawl-required)，以了解如何撰寫累加編目查詢，並查看下圖為例。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-158">Review the [full crawl steps](#full-crawl-required) to learn how to write your incremental crawl query and see the following image as an example.</span></span>

![顯示可用的 OrderTable、 AclTable 及範例內容的累加編目指令碼。](media/MSSQL-incrcrawl.png)

## <a name="limitations"></a><span data-ttu-id="6fc9d-160">限制</span><span class="sxs-lookup"><span data-stu-id="6fc9d-160">Limitations</span></span>
<span data-ttu-id="6fc9d-161">Microsoft SQL server 連接器已在預覽中的釋放這些限制：</span><span class="sxs-lookup"><span data-stu-id="6fc9d-161">The Microsoft SQL server connector has these limitations in the preview release:</span></span>
* <span data-ttu-id="6fc9d-162">內部部署資料庫必須執行 SQL server 版本，2008年或更新版本。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-162">The on-premises database must run SQL server version 2008 or later.</span></span>
* <span data-ttu-id="6fc9d-163">使用使用者主要名稱 (UPN)、 Azure Active Directory (Azure AD) 或 Active Directory 安全性只支援 Acl。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-163">ACLs are only supported by using a User Principal Name (UPN), Azure Active Directory (Azure AD), or Active Directory Security.</span></span>
* <span data-ttu-id="6fc9d-164">不支援資料庫資料行內的豐富內容編製索引。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-164">Indexing rich content inside database columns is not supported.</span></span> <span data-ttu-id="6fc9d-165">這類內容的範例為 HTML、 JSON、 XML、 blob，與文件 parsings 在於做為內的資料庫資料行的連結。</span><span class="sxs-lookup"><span data-stu-id="6fc9d-165">Examples of such content are HTML, JSON, XML, blobs, and document parsings that exist as links inside the database columns.</span></span>

