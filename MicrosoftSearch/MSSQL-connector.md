---
title: Microsoft Search 的 microsoft SQL server 和 Azure SQL connector
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
description: 設定 microsoft SQL server 或 Azure SQL connector for Microsoft Search。
ms.openlocfilehash: e664a9a6e389531f8b5735673150839a1b106ce1
ms.sourcegitcommit: 68cd28a84df120473270f27e4eb62de9eae455f9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/23/2020
ms.locfileid: "44850896"
---
# <a name="azure-sql-and-microsoft-sql-server-connectors"></a>Azure SQL 及 Microsoft SQL server 連接器

透過 Microsoft SQL server 或 Azure SQL connector，您的組織可以探索內部部署 SQL Server 資料庫中的資料，以及在雲端中裝載于 Azure SQL 實例中的資料庫。 連接器會將指定的內容索引至 Microsoft 搜尋。 若要讓索引保持在最新的來來源資料中，它支援定期完整和累加編目。 透過這些 SQL 連接器，您也可以限制特定使用者對搜尋結果的存取。

本文適用于 Microsoft 365 系統管理員或任何設定、執行及監視 Microsoft SQL server connector 的人員。 它說明如何設定連接器和連接器功能、限制及疑難排解技術。

## <a name="install-a-data-gateway-required-for-on-premises-microsoft-sql-server-connector-only"></a>安裝資料閘道（僅限內部部署 Microsoft SQL server 連接器所需）
為了存取協力廠商資料，您必須安裝和設定 Microsoft Power BI 閘道。 請參閱[安裝內部部署閘道](https://docs.microsoft.com/data-integration/gateway/service-gateway-install)以深入瞭解。  

## <a name="connect-to-a-data-source"></a>連接到資料來源
若要將 Microsoft SQL server 連接器連線至資料來源，您必須設定要編目的資料庫伺服器和內部部署閘道。 然後，您就可以使用必要的驗證方法來連接至資料庫。

針對 Azure SQL connector，您只需要指定您要連線的伺服器名稱或 IP 位址。 Azure SQL connector 只支援 Azure Active Directory 開啟識別碼 connect （OIDC）驗證，以連線至資料庫。

> [!NOTE]
> 您的資料庫必須執行 SQL server 版本2008或更新版本，Microsoft SQL server 連接器才能連線。

若要搜尋您的資料庫內容，當您設定連接器時，必須指定 SQL 查詢。 這些 SQL 查詢必須命名所有要索引的資料庫資料行（亦即來源屬性），包括要取得所有欄所需執行的任何 SQL 聯接。 若要限制存取搜尋結果，您必須在設定連接器時，指定 SQL 查詢中的存取控制清單（ACLs）。

## <a name="full-crawl-required"></a>完整編目（必要）
在這個步驟中，您會設定執行資料庫完整編目的 SQL 查詢。 完整編目會選取您想要讓其可**查詢** **、可**搜尋或可**檢索**的所有欄或屬性。 您也可以指定 ACL 欄，以限制搜尋結果對特定使用者或群組的存取。

> [!Tip]
> 若要取得所需的所有欄，您可以加入多個表格。

![腳本顯示 OrderTable 及 AclTable （含範例屬性）](media/MSSQL-fullcrawl.png)

### <a name="select-data-columns-required-and-acl-columns-optional"></a>選取資料欄（必要）和 ACL 欄（選用）
這個範例會示範五個數據列的選取範圍，其中保留搜尋的資料：「訂單」、「OrderTitle」、OrderDesc、CreatedDateTime 及 IsDeleted。 若要設定每個資料列的查看許可權，您可以選擇性地選取下列 ACL 欄： AllowedUsers、AllowedGroups、DeniedUsers 及 DeniedGroups。 所有的資料欄位都可以是可**查詢**、可搜尋或**可供****檢索**。

選取下列範例查詢所示的資料行：`SELECT OrderId, OrderTitle, OrderDesc, AllowedUsers, AllowedGroups, DeniedUsers, DeniedGroups, CreatedDateTime, IsDeleted`
 
若要管理搜尋結果的存取權，您可以在查詢中指定一或多個 ACL 欄。 SQL connector 可讓您控制每個記錄層級的存取。 您可以選擇對資料表中的所有記錄使用相同的存取控制。 如果 ACL 資訊儲存在不同的資料表中，您可能必須在查詢中使用這些資料表進行聯接。

在上述查詢中使用每個 ACL 欄的描述如下。 下列清單說明四種**存取控制機制**。 
* **AllowedUsers**：這會指定可以存取搜尋結果的使用者 IDs 清單。 在下列範例中，使用者清單為： john@contoso.com、keith@contoso.com 和 lisa@contoso.com 只有具有「訂單 Id」的記錄存取權 = 12。 
* **AllowedGroups**：這會指定可以存取搜尋結果的使用者群組。 在下列範例中，group sales-team@contoso.com 只會具有「訂單 Id = 12」的記錄存取權。
* **DeniedUsers**：**這會指定**沒有搜尋結果存取權的使用者清單。 在下列範例中，使用者 john@contoso.com 及 keith@contoso.com 無法存取具有「訂單 Id」的記錄，而其他所有人都可以存取這筆記錄。 
* **DeniedGroups**：這**會**指定沒有搜尋結果存取權的使用者群組。 在下列範例中，群組 engg-team@contoso.com 及 pm-team@contoso.com 沒有具有「訂單 Id」的記錄存取權，而其他所有人都可以存取這筆記錄。  

![](media/MSSQL-ACL1.png)

### <a name="watermark-required"></a>水位線（必要）
若要防止資料庫超載，連接器會批次並繼續完整編目的查詢。 使用 [浮水印] 資料行的值，每個後續的批次都會取得，而查詢會從最後一個檢查點繼續。 本質上，這是一種機制，用來控制完整編目的資料重新整理。

建立浮水印的查詢程式碼片段，如下列範例所示：
* `WHERE (CreatedDateTime > @watermark)`. 使用保留的關鍵字來引用浮水印欄名稱 `@watermark` 。 如果浮水印欄的排序次序是遞增的，請使用 `>` ，否則請使用 `<` 。
* `ORDER BY CreatedDateTime ASC`. 在 [浮水印] 欄上以遞增或遞減順序排序。

在下一個影像所示的設定中， `CreatedDateTime` 是選取的 [浮水印] 欄。 若要取得第一批列，請指定 [浮水印] 資料行的資料類型。 在此情況下，資料類型為 `DateTime` 。

![](media/MSSQL-watermark.png)

第一個查詢會使用： "CreatedDateTime > 1753 年1月1日，00:00:00" （DateTime 資料類型的最小值）來提取前**N**列金額。 提取第一個批次之後， `CreatedDateTime` 如果資料列是以遞增順序排序，則會將批次中傳回的最高值儲存為檢查點。 範例是 03:00:00 2019 年3月1日。 然後，在查詢中使用「CreatedDateTime > 三月份1，2019 03:00:00」提取下一批**N**列。

### <a name="skipping-soft-deleted-rows-optional"></a>略過虛刪除的列（選用）
若要排除資料庫中虛刪除的列的索引，請指定虛刪除的列名稱和值，以指出刪除列的資料行。

![虛刪除設定： "Soft delete column" 和 "soft delete 欄的值，表示已刪除的資料列"](media/MSSQL-softdelete.png)

### <a name="full-crawl-manage-search-permissions"></a>完整編目：管理搜尋許可權
按一下 [**管理許可權**]，以選取指定存取控制機制的各種存取控制（ACL）欄。 選取您在完整編目 SQL 查詢中所指定的資料行名稱。 

每個 ACL 欄都應該是多重值欄。 您可以使用分號（;)、逗號（，）等分隔符號來分隔這些多個 ID 值。 您必須在 [**值分隔符號**] 欄位中指定此分隔符號。
 
下列識別碼類型可供使用 ACLs： 
* **使用者主體名稱（upn）**：使用者主要名稱（upn）是使用電子郵件地址格式的系統使用者名稱。 UPN （例如： john.doe@domain.com）包含使用者名稱（登入名稱）、分隔符號（@ 符號）和功能變數名稱（UPN 尾碼）。 
* **Azure Active Directory （AAD）識別碼**：在 AAD 中，每個使用者或群組都有一個類似 ' e0d3ad3d-0000-1111-2222-3c5f5c52ab9b ' 的物件識別碼。 
* **Active Directory （AD）安全性**識別碼：在內部部署 AD 安裝程式中，每個使用者和群組都有一個無法變化的唯一安全性識別碼，看起來像是-1-5-21-3878594291-2115959936-132693609-65242。 '

![](media/MSSQL-ACL2.png)

## <a name="incremental-crawl-optional"></a>增量式編目（選用）
在此選用的步驟中，請提供 SQL 查詢，以執行資料庫的增量式編目。 在此查詢中，SQL 連接器會決定自上次累加編目以來對資料所做的任何變更。 在完整編目中，選取您想要讓其成為可**查詢**、可搜尋或可**檢索****的所有**欄。 指定您在完整編目查詢中指定的相同 ACL 欄集。

下列映射中的元件類似于完整編目元件，但有一個例外。 在此情況下，"ModifiedDateTime" 是選取的浮水印欄。 查看[完整編目步驟](#full-crawl-required)，以瞭解如何撰寫累加編目查詢，並以範例顯示下列影像。

![新增編目腳本，顯示可使用的 OrderTable、AclTable 和範例屬性。](media/MSSQL-incrcrawl.png)

## <a name="manage-search-permissions"></a>管理搜尋許可權 
您可以選擇使用完整編目[畫面中所指定的 ACLs](#full-crawl-manage-search-permissions) ，也可以覆寫它們，讓每個人都能看到您的內容。

## <a name="limitations"></a>限制
在預覽版本中，SQL 連接器具有這些限制：
* Microsoft SQL server connector：內部部署資料庫必須執行 SQL server 版本2008或更新版本。
* 只有在使用使用者主要名稱（UPN）、Azure Active Directory （Azure AD）或 Active Directory 安全性時，才支援 ACLs。 
* 不支援在資料庫欄中編制豐富內容的索引。 這類內容的範例為 HTML、JSON、XML、blob 及檔 parsings，以資料庫資料欄中的連結形式存在。
