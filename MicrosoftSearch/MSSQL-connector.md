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
ms.openlocfilehash: c31399e65bd4bfc154d10d2e6057fa23d11f030d
ms.sourcegitcommit: ef1eb2bdf31dccd34f0fdc4aa7a0841ebd44f211
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/02/2019
ms.locfileid: "39663155"
---
# <a name="microsoft-sql-server-connector"></a>Microsoft SQL server 連接器

Microsoft SQL server 連接器，您的組織可以探索和索引資料從內部部署 SQL Server 資料庫。 連接器索引指定成 Microsoft 搜尋的內容。 若要保留最新的來源資料的索引，它所支援定期完整和累加編目。 使用 SQL Server 連接器，您也可以限制存取搜尋結果提供給特定使用者。

本文適用於 Microsoft 365 系統管理員或人設定、 執行，並監視的 Microsoft SQL server 連接器。 本文說明如何設定連接器，連接器功能、 限制和疑難排解技巧。

## <a name="install-a-data-gateway"></a>安裝資料閘道
若要存取您的協力廠商資料，您必須安裝及設定 Microsoft Power BI 閘道。 請參閱[安裝與內部部署閘道](https://docs.microsoft.com/data-integration/gateway/service-gateway-install)若要了解更多。  

## <a name="connect-to-a-data-source"></a>連線至資料來源
若要連接您的 Microsoft SQL server 連接器至資料來源，您必須設定您要編目的資料庫伺服器和內部部署閘道。 您可以再連線到資料庫所需的驗證方法。

> [!NOTE]
> 2008 或更新版本，您的資料庫必須執行 SQL server 版本。

若要搜尋您資料庫的內容，您必須指定 SQL 查詢，當您設定連接器。 下列 SQL 查詢必須命名為所有要索引 （亦即來源的屬性），包括任何不需要執行若要取得所有的資料行的 SQL 聯結的資料庫資料行。 若要限制存取權的搜尋結果，您必須指定存取控制清單 (Acl) 與 SQL 查詢時您設定 Microsoft SQL server 連接器。

## <a name="full-crawl-required"></a>（必要） 的完整編目
在此步驟中，您可以設定執行完整編目資料庫的 SQL 查詢。 完整編目會選取所有的資料行或您想要進行的屬性**設為可查詢**、**可搜尋**，或**可擷取**。 您也可以指定限制對特定使用者或群組存取搜尋結果的 ACL 欄。

> [!Tip]
> 若要取得您需要的所有資料行，您可以加入多個資料表。

![指令碼顯示 OrderTable 和 AclTable 與範例屬性](media/MSSQL-fullcrawl.png)

### <a name="select-data-columns-required-and-acl-columns-optional"></a>選取的資料行 （必要） 和 ACL 資料行 （選用）
此範例將示範如何選取項目保留搜尋的資料的五個資料欄的： OrderId、 OrderTitle、 OrderDesc、 CreatedDateTime 及 IsDeleted。 若要設定檢視權限的每一列資料，您可以選擇性地選取這些 ACL 欄： AllowedUsers、 AllowedGroups、 DeniedUsers 及 DeniedGroups。 您可以進行所有這些資料行**設為可查詢**、**可搜尋**，或**可擷取**。

此範例會查詢中所示，請選取的資料行：`SELECT OrderId, OrderTitle, OrderDesc, AllowedUsers, AllowedGroups, DeniedUsers, DeniedGroups, CreatedDateTime, IsDeleted`
 
若要管理的存取權的搜尋結果，您可以在查詢中指定一或多個 ACL 資料行。 SQL 連接器可讓您控制每筆記錄層級的存取。 您可以選擇在資料表中有相同的存取控制的所有記錄。 如果 ACL 資訊儲存在不同的資料表中，您可能需要進行與您的查詢中的這些資料表的聯結。

使用每個以上的查詢中的 ACL 欄會如下所述。 下列清單說明 4 的**存取控制機制**。 
* **AllowedUsers**： 這會指定使用者識別碼能夠存取搜尋結果的清單。 在下列範例中，使用者清單： john@contoso.com、 keith@contoso.com，以及 lisa@contoso.com 只需要存取 OrderId 記錄 = 12。 
* **AllowedGroups**： 這會指定群組的使用者將能夠存取搜尋結果。 在下列範例中，群組 sales-team@contoso.com 只需要存取記錄與 OrderId = 12。
* **DeniedUsers**： 這會指定的使用者執行動作清單**不**具有存取權的搜尋結果。 在下列範例中，使用者 john@contoso.com 和 keith@contoso.com 沒有存取權與 OrderId 記錄 = 13，而其他人有權存取這筆記錄。 
* **DeniedGroups**： 這會指定執行動作的使用者群**不**具有存取權的搜尋結果。 在下列範例中，群組 engg-team@contoso.com 和 pm-team@contoso.com 沒有存取權與 OrderId 記錄 = 15，而其他人有權存取這筆記錄。  

![](media/MSSQL-ACL1.png)

### <a name="watermark-required"></a>浮水印 （必要）
若要防止多載資料庫，連接器批次，而且會繼續具有完整編目浮水印資料行的完整編目查詢。 藉由使用浮水印資料行的值，會擷取每一個後續的批次，並查詢從最後一個的檢查點繼續執行。 基本上，這是一種機制可控制的完整編目的資料重新整理。

建立查詢程式碼片段的浮水印，如以下範例所示：
* `WHERE (CreatedDateTime > @watermark)`. 引用浮水印資料行名稱與保留的關鍵字`@watermark`。 如果浮水印資料行的排序順序遞增，使用`>`;否則，請使用`<`。
* `ORDER BY CreatedDateTime ASC`. 浮水印欄，以遞增或遞減順序排序。

在下列影像所示設定`CreatedDateTime`是所選取的浮水印資料行。 若要擷取的資料列的第一個批次，指定浮水印欄的資料類型。 在此例中的資料類型是`DateTime`。

![](media/MSSQL-watermark.png)

第一個查詢擷取資料列的第一個**N**量使用: 「 CreatedDateTime > 1753 年 1 月 1 日 00:00:00 」 （最小值的日期時間資料類型）。 第一個批次會擷取的最高值之後`CreatedDateTime`中傳回批次會儲存為檢查點，如果資料列會以遞增順序排序。 例如，2019 年 3 月 1 日 03:00:00。 然後**N**個資料列的下一個批次會擷取使用 「 CreatedDateTime > 2019 年 3 月 1 日 03:00:00 」 在查詢中。

### <a name="skipping-soft-deleted-rows-optional"></a>略過虛刪除的資料列 （選用）
若要排除在編製索引的虛刪除資料庫中的資料列，請指定虛刪除資料行名稱和值，指出刪除資料列。

![虛刪除的設定: 「 虛刪除資料行 」 和 「 值的虛刪除會指出刪除的資料列資料行 」](media/MSSQL-softdelete.png)

### <a name="full-crawl-manage-search-permissions"></a>完整編目： 管理搜尋的權限
按一下以選取的各種不同的存取控制 (ACL) 欄這會指定存取控制機制的**管理權限**。 選取您在完整編目] 中的 SQL 查詢中指定的欄名稱。 

每個 ACL 欄預期會在多重值的資料行。 這些多個識別碼值可以由分號 （;），以逗號 （，），例如分隔符號分隔等等。 您需要的**值分隔**欄位中指定此分隔符號。
 
使用 Acl 以支援下列的識別碼類型： 
* **使用者主要名稱 (UPN)**: 使用者主要名稱 (UPN) 是電子郵件地址格式中的系統使用者的名稱。 UPN (例如： john.doe@domain.com) 組成的使用者名稱 （登入名稱）、 分隔符號 (@ 符號)，和網域名稱 （UPN 尾碼）。 
* **Azure Active Directory (AAD) 識別碼**： 在 [AAD、 每個使用者或群組具有看起來像 ' e0d3ad3d-0000-1111年-2222年-3c5f5c52ab9b' 物件識別碼 
* **Active Directory (AD) 的安全性識別碼**： 在內部部署 AD 安裝程式，每個使用者和群組具有看起來像 'S-1-5-21-3878594291-2115959936-132693609-65242'。 這不變，唯一的安全性識別碼

![](media/MSSQL-ACL2.png)

## <a name="incremental-crawl-optional"></a>累加編目 （選用）
在此選用的步驟中，提供執行累加編目資料庫的 SQL 查詢。 此查詢中，與 Microsoft SQL server 連接器任何對資料進行變更自上次的累加編目。 如同完整編目]，選取您想要進行的所有欄**設為可查詢**、**可搜尋**，或**可擷取**。 指定相同的完整編目查詢中指定的 ACL 欄集合。

下圖中的元件與類似有一個例外狀況的完整編目元件。 在此情況下，「 ModifiedDateTime 」 是所選取的浮水印資料行。 檢閱[完整編目的步驟](#full-crawl-required)，以了解如何撰寫累加編目查詢，並查看下圖為例。

![顯示可用的 OrderTable、 AclTable 及範例內容的累加編目指令碼。](media/MSSQL-incrcrawl.png)

## <a name="manage-search-permissions"></a>管理搜尋的權限 
您可以選擇使用[[完整編目] 畫面中指定的 Acl](#full-crawl-manage-search-permissions) ，或者您可以覆寫它們，讓您的內容可以看到所有人。

## <a name="limitations"></a>限制
Microsoft SQL server 連接器已在預覽中的釋放這些限制：
* 內部部署資料庫必須執行 SQL server 版本，2008年或更新版本。
* 使用使用者主要名稱 (UPN)、 Azure Active Directory (Azure AD) 或 Active Directory 安全性只支援 Acl。 
* 不支援資料庫資料行內的豐富內容編製索引。 這類內容的範例為 HTML、 JSON、 XML、 blob，與文件 parsings 在於做為內的資料庫資料行的連結。