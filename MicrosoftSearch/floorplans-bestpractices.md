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
# <a name="best-practices-for-microsoft-search-floor-plans"></a><span data-ttu-id="8c43c-103">Microsoft 搜尋基底計畫的最佳作法</span><span class="sxs-lookup"><span data-stu-id="8c43c-103">Best practices for Microsoft Search floor plans</span></span>

<span data-ttu-id="8c43c-104">若要成功地執行 Microsoft 搜尋基底計畫，您必須協調三個數據片段：</span><span class="sxs-lookup"><span data-stu-id="8c43c-104">To successfully implement Microsoft Search floor plans, you need to coordinate three pieces of data:</span></span>

- <span data-ttu-id="8c43c-105">**建立位置資料**：何種格式及新增方式？</span><span class="sxs-lookup"><span data-stu-id="8c43c-105">**Building location data**: What format and how to add?</span></span>
- <span data-ttu-id="8c43c-106">**DWG 格式中的 Floor 平面圖地圖**：如何查看是否有最大成功的資料？</span><span class="sxs-lookup"><span data-stu-id="8c43c-106">**Floor plan map in DWG format**: How to view and what data should it contain for maximum success?</span></span>
- <span data-ttu-id="8c43c-107">**在[Azure Active Directory （azure AD）](https://azure.microsoft.com/services/active-directory/)中的員工辦公位置**：要使用的格式及新增方式？</span><span class="sxs-lookup"><span data-stu-id="8c43c-107">**Employee office location in [Azure Active Directory (Azure AD)](https://azure.microsoft.com/services/active-directory/)**: What format to use and how to add?</span></span> <br>

<span data-ttu-id="8c43c-108">在下列各節中也說明部署 Microsoft 搜尋基底計畫的最佳作法。</span><span class="sxs-lookup"><span data-stu-id="8c43c-108">The best practices for deploying Microsoft Search floor plans are also described in the following sections.</span></span>

## <a name="building-location-data"></a><span data-ttu-id="8c43c-109">建立位置資料</span><span class="sxs-lookup"><span data-stu-id="8c43c-109">Building location data</span></span>

<span data-ttu-id="8c43c-110">在您新增 floor 計畫之前，您必須將大樓新增至 Microsoft 搜尋位置。</span><span class="sxs-lookup"><span data-stu-id="8c43c-110">Before you add floor plans, you need to add your buildings to Microsoft Search locations.</span></span> <span data-ttu-id="8c43c-111">提供下列必要的建立資料：</span><span class="sxs-lookup"><span data-stu-id="8c43c-111">Provide the following required building data:</span></span>

|<span data-ttu-id="8c43c-112">必要的建立資料</span><span class="sxs-lookup"><span data-stu-id="8c43c-112">Required building data</span></span>  |<span data-ttu-id="8c43c-113">範例</span><span class="sxs-lookup"><span data-stu-id="8c43c-113">Example</span></span>  |
|---------|---------|
|<span data-ttu-id="8c43c-114">名稱</span><span class="sxs-lookup"><span data-stu-id="8c43c-114">Name</span></span>     |    <span data-ttu-id="8c43c-115">組建1，紐約州的城市</span><span class="sxs-lookup"><span data-stu-id="8c43c-115">Building 1, New York City</span></span>     |
|<span data-ttu-id="8c43c-116">街道地址</span><span class="sxs-lookup"><span data-stu-id="8c43c-116">Street address</span></span>     |     <span data-ttu-id="8c43c-117">123任何途徑，紐約州紐約市，紐約州10118</span><span class="sxs-lookup"><span data-stu-id="8c43c-117">123 Any Avenue, New York, NY 10118</span></span>  |
|<span data-ttu-id="8c43c-118">緯度-經度（選用）</span><span class="sxs-lookup"><span data-stu-id="8c43c-118">Latitude-longitude  (optional)</span></span>   |    <span data-ttu-id="8c43c-119">40.760539，-73.975341</span><span class="sxs-lookup"><span data-stu-id="8c43c-119">40.760539, -73.975341</span></span>      |
|<span data-ttu-id="8c43c-120">關鍵字</span><span class="sxs-lookup"><span data-stu-id="8c43c-120">Keywords</span></span>     |    <span data-ttu-id="8c43c-121">紐約辦事處，組建1，總公司，總公司，總部</span><span class="sxs-lookup"><span data-stu-id="8c43c-121">New York Office, Building 1, main office, headquarters</span></span>     |

<span data-ttu-id="8c43c-122">您可以使用 [**位置**] 索引標籤中的 [匯**入**] 功能（而不是一次加入一個位置），一次新增許多建築物。</span><span class="sxs-lookup"><span data-stu-id="8c43c-122">You can add many buildings at a time by using the **Import** feature in the **Locations** tab instead of adding locations one at a time.</span></span> <span data-ttu-id="8c43c-123">使用 [匯**入**] 功能，您可以指定緯度-經度。</span><span class="sxs-lookup"><span data-stu-id="8c43c-123">With the **Import** feature, you can specify the latitude-longitude.</span></span> <span data-ttu-id="8c43c-124">如需詳細資訊，請參閱[管理位置](manage-locations.md)。</span><span class="sxs-lookup"><span data-stu-id="8c43c-124">For more information, see [Manage locations](manage-locations.md).</span></span>

## <a name="floor-plan-map-in-dwg-format"></a><span data-ttu-id="8c43c-125">DWG 格式的 Floor 平面圖地圖</span><span class="sxs-lookup"><span data-stu-id="8c43c-125">Floor plan map in DWG format</span></span>

<span data-ttu-id="8c43c-126">若要在 Microsoft 搜尋中建立地圖，您需要以特定資訊上傳 DWG 格式的 floor 方案。</span><span class="sxs-lookup"><span data-stu-id="8c43c-126">To build maps in Microsoft Search, you need to upload floor plans in DWG format with specific information.</span></span> <span data-ttu-id="8c43c-127">若要瞭解如何建立及流覽 DWG 格式的檔案，請參閱[Dwg viewer](https://www.autodesk.in/products/dwg)。</span><span class="sxs-lookup"><span data-stu-id="8c43c-127">To learn how to create and view DWG-formatted files, see [DWG Viewers](https://www.autodesk.in/products/dwg).</span></span>

<span data-ttu-id="8c43c-128">Floor 平面圖地圖顯示四個元素：</span><span class="sxs-lookup"><span data-stu-id="8c43c-128">Floor plan maps display four elements:</span></span>

1. <span data-ttu-id="8c43c-129">**會議室號碼**：在下列範例中，會議室編號會定義為**B1 1001**和**b1 1002**。</span><span class="sxs-lookup"><span data-stu-id="8c43c-129">**Room numbers**: In the following example, room numbers are defined as **B1 1001** and **B1 1002**.</span></span> <span data-ttu-id="8c43c-130">**B1**是組建碼， **1001**包含第**1**層和辦公室號碼**001**。</span><span class="sxs-lookup"><span data-stu-id="8c43c-130">**B1** is the building code, and **1001** contains the floor number **1** and the office number **001**.</span></span>
1. <span data-ttu-id="8c43c-131">**會議室佈局。**：若要協助澄清多個使用者共用 office，您可以定義椅子和書桌等版面配置。</span><span class="sxs-lookup"><span data-stu-id="8c43c-131">**Room layouts.**: To help clarify details when multiple users share an office, you can define layouts like chairs and desk.</span></span>
1. <span data-ttu-id="8c43c-132">**會議室類型**：有些範例包括 office、corridor、open 區域和抽水馬桶。</span><span class="sxs-lookup"><span data-stu-id="8c43c-132">**Room types**: Some examples include office, corridor, open area, and toilet.</span></span>
1. <span data-ttu-id="8c43c-133">**資產資訊**：如果使用者位於開啟的空間中，您可以指定其所在的桌面。</span><span class="sxs-lookup"><span data-stu-id="8c43c-133">**Asset info**: If users are in an open space, you can denote which desk they sit at.</span></span> <span data-ttu-id="8c43c-134">在此範例中，辦公桌是由**TB1**和**TB2**表示。</span><span class="sxs-lookup"><span data-stu-id="8c43c-134">In this example, the desks are denoted by **TB1** and **TB2**.</span></span>

![簡單的 office 地圖，顯示如何標示會議室編號、資產和會議室類型](media/Floorplans-LayoutwithCallouts.png)

<span data-ttu-id="8c43c-136">在此圖中，房間號碼是最重要的專案。</span><span class="sxs-lookup"><span data-stu-id="8c43c-136">In this diagram, room numbers are the most important item.</span></span> <span data-ttu-id="8c43c-137">它們會對應至使用者帳戶上的辦公室位置，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="8c43c-137">They're mapped to a person’s office location on their user account as shown in the following image.</span></span>

![人員搜尋結果卡片的 [一覽表] 索引標籤顯示使用者的詳細資料，包括辦公室位置](media/floorplans-peoplecard.png)

<span data-ttu-id="8c43c-139">此資訊儲存在[AZURE AD](https://azure.microsoft.com/services/active-directory/)的**PhysicalDeliveryOfficeName**屬性中。</span><span class="sxs-lookup"><span data-stu-id="8c43c-139">This information is stored in [Azure AD](https://azure.microsoft.com/services/active-directory/) in the **PhysicalDeliveryOfficeName** property.</span></span> <span data-ttu-id="8c43c-140">在 Microsoft 365 系統[管理中心](https://admin.microsoft.com)，它稱為**Office**屬性，可在作用中**使用者**新增。</span><span class="sxs-lookup"><span data-stu-id="8c43c-140">In the Microsoft 365 [admin center](https://admin.microsoft.com), it’s called the **Office** property and can be added in **Active users**.</span></span>

### <a name="dwg-files"></a><span data-ttu-id="8c43c-141">DWG 檔案</span><span class="sxs-lookup"><span data-stu-id="8c43c-141">DWG files</span></span>

<span data-ttu-id="8c43c-142">Microsoft Search 需要 DWG 中的 floor 計畫檔案，這是[AutoCAD](https://www.autodesk.com/autocad)的繪圖格式。</span><span class="sxs-lookup"><span data-stu-id="8c43c-142">Microsoft Search requires floor plan files in DWG, which is an [AutoCAD](https://www.autodesk.com/autocad) drawing format.</span></span> <span data-ttu-id="8c43c-143">檔案必須包含**版面**配置及**標籤**資料。</span><span class="sxs-lookup"><span data-stu-id="8c43c-143">The files must contain **layout** and **label** data.</span></span> <span data-ttu-id="8c43c-144">**會議室編號**是地面方案最重要的標籤。</span><span class="sxs-lookup"><span data-stu-id="8c43c-144">**Room numbers** are the most important labels for floor plans.</span></span>

<span data-ttu-id="8c43c-145">建議您使用下表所示的完全相符方法，來建立您的 office 編號系統。</span><span class="sxs-lookup"><span data-stu-id="8c43c-145">We recommend that you create your office numbering system with the exact-match method shown in the following table.</span></span> <span data-ttu-id="8c43c-146">不過，您並不局限于該標籤。</span><span class="sxs-lookup"><span data-stu-id="8c43c-146">But you aren't limited to that labeling.</span></span> <span data-ttu-id="8c43c-147">例如，如果使用者在[AZURE AD](https://azure.microsoft.com/services/active-directory/)中的 office 位置是**B1 1001**，您可以使用下列任一選項，在 DWG 檔案中貼上房間號碼。</span><span class="sxs-lookup"><span data-stu-id="8c43c-147">For example, if the user's office location in [Azure AD](https://azure.microsoft.com/services/active-directory/) is **B1 1001**, you can label the room number in the DWG file with any of the options that follow.</span></span>

|<span data-ttu-id="8c43c-148">Match</span><span class="sxs-lookup"><span data-stu-id="8c43c-148">Match</span></span>  |<span data-ttu-id="8c43c-149">版面配置</span><span class="sxs-lookup"><span data-stu-id="8c43c-149">Layout</span></span>  |
|---------|---------|
|<span data-ttu-id="8c43c-150">完全符合 office 位置（建議）</span><span class="sxs-lookup"><span data-stu-id="8c43c-150">Exact match to office location (Recommended)</span></span> <br> <span data-ttu-id="8c43c-151">**B1 1001**</span><span class="sxs-lookup"><span data-stu-id="8c43c-151">**B1 1001**</span></span> <br> <span data-ttu-id="8c43c-152">建立程式碼： B1</span><span class="sxs-lookup"><span data-stu-id="8c43c-152">Building code: B1</span></span><br><span data-ttu-id="8c43c-153">地板：1</span><span class="sxs-lookup"><span data-stu-id="8c43c-153">Floor: 1</span></span> <br><span data-ttu-id="8c43c-154">會議室編號：001</span><span class="sxs-lookup"><span data-stu-id="8c43c-154">Room number: 001</span></span>    |    ![辦事處編號為 "B1 1001" 的單一 office 平面平面圖](media/floorplans-layoutexactmatch.png)     |
|<span data-ttu-id="8c43c-156">符合底價和房間號碼</span><span class="sxs-lookup"><span data-stu-id="8c43c-156">Match floor and room number</span></span> <br> <span data-ttu-id="8c43c-157">**1001**</span><span class="sxs-lookup"><span data-stu-id="8c43c-157">**1001**</span></span><br><span data-ttu-id="8c43c-158">地板：1</span><span class="sxs-lookup"><span data-stu-id="8c43c-158">Floor: 1</span></span> <br><span data-ttu-id="8c43c-159">會議室編號：001</span><span class="sxs-lookup"><span data-stu-id="8c43c-159">Room number: 001</span></span>    |   ![辦事處編號為 "1001" 的單一 office 平面圖](media/floorplans-layoutfloorroom.png)   |
|<span data-ttu-id="8c43c-161">只符合會議室號碼</span><span class="sxs-lookup"><span data-stu-id="8c43c-161">Match room number only</span></span> <br> <span data-ttu-id="8c43c-162">**1**</span><span class="sxs-lookup"><span data-stu-id="8c43c-162">**1**</span></span><br><span data-ttu-id="8c43c-163">會議室編號：1</span><span class="sxs-lookup"><span data-stu-id="8c43c-163">Room number: 1</span></span>        |    ![辦事處編號為 "1" 的單一 office 底價地圖](media/floorplans-layoutroomonly.png)     |

## <a name="user-account-office-location"></a><span data-ttu-id="8c43c-165">使用者帳戶辦公室位置</span><span class="sxs-lookup"><span data-stu-id="8c43c-165">User account office location</span></span>

<span data-ttu-id="8c43c-166">若要對應員工的位置，DWG 檔案中的房間號碼會對應至[AZURE AD](https://azure.microsoft.com/services/active-directory/)中使用者帳戶的 office 位置。</span><span class="sxs-lookup"><span data-stu-id="8c43c-166">To map an employee’s location, the room numbers in DWG files are mapped to office locations in the user’s account in [Azure AD](https://azure.microsoft.com/services/active-directory/).</span></span> <span data-ttu-id="8c43c-167">**Office location**屬性必須符合 DWG 檔案中的 Office 位置資訊。</span><span class="sxs-lookup"><span data-stu-id="8c43c-167">The **Office location** property needs to match the office location information in the DWG file.</span></span>

<span data-ttu-id="8c43c-168">下表說明對應位置資料的最佳作法：</span><span class="sxs-lookup"><span data-stu-id="8c43c-168">The following table explains best practices for mapping location data:</span></span>

|<span data-ttu-id="8c43c-169">最佳作法</span><span class="sxs-lookup"><span data-stu-id="8c43c-169">Best practice</span></span>  |<span data-ttu-id="8c43c-170">說明</span><span class="sxs-lookup"><span data-stu-id="8c43c-170">Explanation</span></span> |
|---------|---------|
|<span data-ttu-id="8c43c-171">包括建築物代碼、基底及房間編號。</span><span class="sxs-lookup"><span data-stu-id="8c43c-171">Include building code, floor, and room number.</span></span>     |   <span data-ttu-id="8c43c-172">這項資料可讓您取得完全符合的可能性。</span><span class="sxs-lookup"><span data-stu-id="8c43c-172">This data gives you the best chance to make exact matches.</span></span>     |
|<span data-ttu-id="8c43c-173">在建立代碼和地面後包含分隔符號。</span><span class="sxs-lookup"><span data-stu-id="8c43c-173">Include a separator after building codes and floors.</span></span>     |  <span data-ttu-id="8c43c-174">以分隔符號或空間分隔基底和房間號碼的大樓代碼，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="8c43c-174">Separate building codes from floor and room numbers with a separator or a space, as in these examples:</span></span><br> <span data-ttu-id="8c43c-175">B1 1001</span><span class="sxs-lookup"><span data-stu-id="8c43c-175">B1 1001</span></span><br> <span data-ttu-id="8c43c-176">B1/1001</span><span class="sxs-lookup"><span data-stu-id="8c43c-176">B1/1001</span></span> <br> <span data-ttu-id="8c43c-177">B1-1001。</span><span class="sxs-lookup"><span data-stu-id="8c43c-177">B1-1001.</span></span>   |
|<span data-ttu-id="8c43c-178">會議室編號永遠遵循建立程式碼、翼和地面資訊。</span><span class="sxs-lookup"><span data-stu-id="8c43c-178">Room number always follows building code, wing, and floor information.</span></span>     |  <span data-ttu-id="8c43c-179">如果會議室號碼是**1001**，請將辦公室位置設定為**b1 1001**、 **b1/1001**或**b1-1001**。</span><span class="sxs-lookup"><span data-stu-id="8c43c-179">If the room number is **1001**, then set the office location to **B1 1001**, **B1/1001**, or **B1-1001**.</span></span> <br> <span data-ttu-id="8c43c-180">如果會議室號碼是**F1-001**，請將辦公位置設定為**b1 F1-001**或**b1/F1-001**。</span><span class="sxs-lookup"><span data-stu-id="8c43c-180">If the room number is **F1-001**, then set the office location to **B1 F1-001** or **B1/F1-001**.</span></span> <br> <span data-ttu-id="8c43c-181">如果會議室編號為**1**，則將[Azure AD](https://azure.microsoft.com/services/active-directory/)位置設定為**b1 1001**、 **B1/1001**或**b1-F1-001**。</span><span class="sxs-lookup"><span data-stu-id="8c43c-181">If the room number is **1**, then set the [Azure AD](https://azure.microsoft.com/services/active-directory/) location to **B1 1001**, **B1/1001**, or **B1-F1-001**.</span></span>       |
|

## <a name="next-steps"></a><span data-ttu-id="8c43c-182">後續步驟</span><span class="sxs-lookup"><span data-stu-id="8c43c-182">Next steps</span></span>

[<span data-ttu-id="8c43c-183">管理位置</span><span class="sxs-lookup"><span data-stu-id="8c43c-183">Manage locations</span></span>](manage-locations.md)<br>
[<span data-ttu-id="8c43c-184">管理基底計畫</span><span class="sxs-lookup"><span data-stu-id="8c43c-184">Manage floor plans</span></span>](manage-floorplans.md)
