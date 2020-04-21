---
title: Microsoft 搜尋基底計畫的最佳作法
ms.author: jeffkizn
author: jeffkizn
manager: parulm
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: Microsoft 搜尋基底計畫的最佳作法
ms.openlocfilehash: 47eb46df48f1871f6d34d4b00787cf11ccbac1ea
ms.sourcegitcommit: 6b1c6a4e502d95b42a030a963f9452c387d8a5cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/20/2020
ms.locfileid: "43571012"
---
<!-- markdownlint-disable no-inline-html -->
# <a name="best-practices-for-microsoft-search-floor-plans"></a>Microsoft 搜尋基底計畫的最佳作法

若要成功地執行 Microsoft 搜尋基底計畫，您必須協調三個數據片段：

- **建立位置資料**：何種格式及新增方式？
- **DWG 格式中的 Floor 平面圖地圖**：如何查看是否有最大成功的資料？
- **在[Azure Active Directory （azure AD）](https://azure.microsoft.com/services/active-directory/)中的員工辦公位置**：要使用的格式及新增方式？ <br>

在下列各節中也說明部署 Microsoft 搜尋基底計畫的最佳作法。

## <a name="building-location-data"></a>建立位置資料

在您新增 floor 計畫之前，您必須將大樓新增至 Microsoft 搜尋位置。 提供下列必要的建立資料：

|必要的建立資料  |範例  |
|---------|---------|
|名稱     |    組建1，紐約州的城市     |
|街道地址     |     123任何途徑，紐約州紐約市，紐約州10118  |
|緯度-經度（選用）   |    40.760539，-73.975341      |
|關鍵字     |    紐約辦事處，組建1，總公司，總公司，總部     |

您可以使用 [**位置**] 索引標籤中的 [匯**入**] 功能（而不是一次加入一個位置），一次新增許多建築物。 使用 [匯**入**] 功能，您可以指定緯度-經度。 如需詳細資訊，請參閱[管理位置](manage-locations.md)。

## <a name="floor-plan-map-in-dwg-format"></a>DWG 格式的 Floor 平面圖地圖

若要在 Microsoft 搜尋中建立地圖，您需要以特定資訊上傳 DWG 格式的 floor 方案。 若要瞭解如何建立及流覽 DWG 格式的檔案，請參閱[Dwg viewer](https://www.autodesk.in/products/dwg)。

Floor 平面圖地圖顯示四個元素：

1. **會議室號碼**：在下列範例中，會議室編號會定義為**B1 1001**和**b1 1002**。 **B1**是組建碼， **1001**包含第**1**層和辦公室號碼**001**。
1. **會議室佈局。**：若要協助澄清多個使用者共用 office，您可以定義椅子和書桌等版面配置。
1. **會議室類型**：有些範例包括 office、corridor、open 區域和抽水馬桶。
1. **資產資訊**：如果使用者位於開啟的空間中，您可以指定其所在的桌面。 在此範例中，辦公桌是由**TB1**和**TB2**表示。

![簡單的 office 地圖，顯示如何標示會議室編號、資產和會議室類型](media/Floorplans-LayoutwithCallouts.png)

在此圖中，房間號碼是最重要的專案。 它們會對應至使用者帳戶上的辦公室位置，如下圖所示。

![人員搜尋結果卡片的 [一覽表] 索引標籤顯示使用者的詳細資料，包括辦公室位置](media/floorplans-peoplecard.png)

此資訊儲存在[AZURE AD](https://azure.microsoft.com/services/active-directory/)的**PhysicalDeliveryOfficeName**屬性中。 在 Microsoft 365 系統[管理中心](https://admin.microsoft.com)，它稱為**Office**屬性，可在作用中**使用者**新增。

### <a name="dwg-files"></a>DWG 檔案

Microsoft Search 需要 DWG 中的 floor 計畫檔案，這是[AutoCAD](https://www.autodesk.com/autocad)的繪圖格式。 檔案必須包含**版面**配置及**標籤**資料。 **會議室編號**是地面方案最重要的標籤。

建議您使用下表所示的完全相符方法，來建立您的 office 編號系統。 不過，您並不局限于該標籤。 例如，如果使用者在[AZURE AD](https://azure.microsoft.com/services/active-directory/)中的 office 位置是**B1 1001**，您可以使用下列任一選項，在 DWG 檔案中貼上房間號碼。

|Match  |版面配置  |
|---------|---------|
|完全符合 office 位置（建議） <br> **B1 1001** <br> 建立程式碼： B1<br>地板：1 <br>會議室編號：001    |    ![辦事處編號為 "B1 1001" 的單一 office 平面平面圖](media/floorplans-layoutexactmatch.png)     |
|符合底價和房間號碼 <br> **1001**<br>地板：1 <br>會議室編號：001    |   ![辦事處編號為 "1001" 的單一 office 平面圖](media/floorplans-layoutfloorroom.png)   |
|只符合會議室號碼 <br> **1**<br>會議室編號：1        |    ![辦事處編號為 "1" 的單一 office 底價地圖](media/floorplans-layoutroomonly.png)     |

## <a name="user-account-office-location"></a>使用者帳戶辦公室位置

若要對應員工的位置，DWG 檔案中的房間號碼會對應至[AZURE AD](https://azure.microsoft.com/services/active-directory/)中使用者帳戶的 office 位置。 **Office location**屬性必須符合 DWG 檔案中的 Office 位置資訊。

下表說明對應位置資料的最佳作法：

|最佳作法  |說明 |
|---------|---------|
|包括建築物代碼、基底及房間編號。     |   這項資料可讓您取得完全符合的可能性。     |
|在建立代碼和地面後包含分隔符號。     |  以分隔符號或空間分隔基底和房間號碼的大樓代碼，如下列範例所示：<br> B1 1001<br> B1/1001 <br> B1-1001。   |
|會議室編號永遠遵循建立程式碼、翼和地面資訊。     |  如果會議室號碼是**1001**，請將辦公室位置設定為**b1 1001**、 **b1/1001**或**b1-1001**。 <br> 如果會議室號碼是**F1-001**，請將辦公位置設定為**b1 F1-001**或**b1/F1-001**。 <br> 如果會議室編號為**1**，則將[Azure AD](https://azure.microsoft.com/services/active-directory/)位置設定為**b1 1001**、 **B1/1001**或**b1-F1-001**。       |
|

## <a name="next-steps"></a>後續步驟

[管理位置](manage-locations.md)<br>
[管理基底計畫](manage-floorplans.md)
