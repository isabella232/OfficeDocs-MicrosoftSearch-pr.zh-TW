---
title: 管理基底計畫
ms.author: rasrivas
author: rasrivas
manager: tonytha
ms.audience: Admin
ms.topic: article
ms.service: mssearch
ms.localizationpriority: medium
search.appverid:
- BFB160
- MET150
- MOE150
description: Microsoft 搜尋中的「平面圖」功能可協助使用者找出大樓中的人員、辦公室和其他功能。
ms.openlocfilehash: beeef26cc7413da654cc3ab01d92aa6cdc74e5cb
ms.sourcegitcommit: bb99601a7bd0f16dde7b271de516465d134e5bac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2021
ms.locfileid: "58973665"
---
# <a name="manage-floor-plans"></a>管理基底計畫

**Microsoft 搜尋** 中的地面計畫可協助使用者在大樓內找到人員和會議室。 平面圖的回答下列問題：

- Allan Deyoung 的 office 位於何處？
- 組建2第2地面
- 尋找2/11173

## <a name="add-floor-plans"></a>新增平面計畫

請遵循下列步驟，在 **Microsoft 搜尋** 中設定車間平面圖的答案。

### <a name="step-1-determine-your-building-codes"></a>步驟1：判斷您的大樓代碼

建立碼是用來做為使用者辦公室位置的一部分。 更新使用者設定檔時，您會使用這些代碼。 假設您的組織有在此位置的大樓： *組建2、350 5 號、紐約城、紐約州 10016*

以下是此組建程式碼的一些很好的範例：2、B2、Building2、組建2或 NYCB2。 每個組建都必須有唯一的程式碼。

### <a name="step-2-review-your-floor-plans"></a>步驟2：查看您的地面計畫

Floor 計畫檔案必須採用 DWG 格式;DWG 檔案可包含文字標籤。 當文字標籤標示房間時，它稱為會議室標籤。 DWG 檔案必須有 **至少10個** 以標籤標示的房間。 以下是具有不同標籤類型的 DWG 檔案範例：

|**包含會議室標籤的文字標籤**|**文字標籤，但沒有會議室標籤**|**無文字標籤**|
|:-----:|:-----:|:-----:|
|![floorplans-textandroomlabels.png。](media/floorplans-textandroomlabels.png)|![floorplans-textnoroomlabels.png](media/floorplans-textnoroomlabels.png)|![floorplans-nolabels.png](media/floorplans-nolabels.png)|

如需查看和更新 DWG 檔案的詳細資訊，請參閱 [FAQ](#frequently-asked-questions) 一節。

### <a name="step-3-update-office-locations-on-user-profiles"></a>步驟3：更新使用者設定檔上的 office 位置

使用者的辦公室位置是組建程式碼和會議室標籤的組合。 例如，如果組建程式碼是 *2* ，而會議室標籤是 *1173*，則辦公室位置會是 *2/1173*。

為您組織中的每位使用者新增或更新辦公地點。 您可以在[Microsoft 365 系統管理中心](https://admin.microsoft.com)中變更使用者設定檔上的 office 位置，也可以在內部部署 Active Directory 中變更，以同步處理至 Azure Active Directory。 *PhysicalDeliveryOfficeName* 是用於 office 位置的欄位。 如果您的會議室標籤不含底價編號，請參閱秘訣的常見問題。

在此範例中，Allan 的 office 位於組建2第1座第1座的房間1173。
![floorplans-userlestview.png。](media/floorplans-userlistview.png)

> [!NOTE]
> 若要在搜尋地面計畫時查看更新的 office 位置，您必須在每個地面更新 **至少10個人** 的 office 位置。

### <a name="step-4-verify-office-location"></a>步驟4：確認辦公室位置

使用 **Microsoft 搜尋** 尋找使用者，並確認其辦公室位置是否正確顯示。 如果您只有更新的位置，您可能需要等候 **72 小時** ，更新才會出現在搜尋結果中。

![floorplans-peoplecard.png。](media/floorplans-peoplecard.png)

### <a name="step-5-add-building-locations"></a>步驟5：新增大樓位置

地面計畫使用 [位置](manage-locations.md) 來定義您的辦公樓。 在 [Microsoft 365 系統管理中心](https://admin.microsoft.com)中，移至 [[**位置**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/locations)]，然後選取 [**新增**]。 輸入組建的名稱、位址及關鍵字。 新增所需數目的辦公樓。

![floorplans-locations.png。](media/floorplans-locations.png)

如需位置的詳細資訊，請參閱 [管理位置](manage-locations.md)

### <a name="step-6-gather-and-organize-office-locations"></a>步驟6：收集和組織辦公室位置

在您可以使用基底計畫之前，必須建立 office 位置的索引。 這是一次性作業，可能需要長達48小時才能完成。 總時間將取決於您的組織的大小。

在系統 [管理中心](https://admin.microsoft.com)中，移至 [ [**Floor 方案**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/floorplans)]，然後選取 [ **開始**]。 如果您未看到此通知，表示您的組織已完成此步驟。

![floorplans_hydrationstep.png。](media/floorplans_hydrationstep.png)

### <a name="step-7-upload-floor-plans"></a>步驟7： Upload 基底計畫

1. 在系統 [管理中心](https://admin.microsoft.com)，移至 [ [**地面計畫**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/floorplans)]。
2. 選取下拉式清單中的大樓，然後選取 **[下一步]**。 如果大樓未列出，請後退並 [新增大樓位置](#step-5-add-building-locations)。
3. 選取 [ **Upload** 檔案]，然後選擇您要上傳的地面計畫。
4. 上傳完成後，您必須輸入在 floor 計畫檔案中所代表的 floor 編號。 然後選取 **[下一步]**。
5.  (選用) 如果地面上有 wings 或區域，請輸入該詳細資料。
6. 您將會看到一個 [回顧] 畫面，列出對應至地面方案的 office 位置數目。 選取 [ **詳細資料** ]，以確保對應正確。
    - 如果沒有對應的使用者，或您不滿意對應，請選取 [ **繼續對應**]。 若要發佈，請選取 [ **略過併發布**]。
7. 輸入此地面計畫的建立程式碼。 您可以在使用者的 office location 屬性找到建立程式碼。 例如，如果使用者的辦公室位置是 **2/1173**，則建立程式碼為 **2**。
8. 在 [複查] 畫面上重複步驟6，以確保對應正確。
9.  (選用) 請複查及識別所有上傳的 floor 方案的位置模式，然後選取 **[下一步]**。
10. 在 [複查] 畫面上重複步驟6，以確保對應正確。
11. 當您準備好時，請選取 [**發佈**]，以在 **Microsoft 搜尋** 中使用地面計畫。

> [!NOTE]
> **發佈平面方案需要48小時的時間。** 之後，當使用者搜尋共同工作者的辦公室時，會看到與下列類似的地面計畫結果。

![floorplans-officelocation.png。](media/floorplans-officelocation.png)

### <a name="step-8-optional-specify-location-patterns"></a>步驟8： (選用) 指定位置模式

上傳平面圖後，文字標籤會與使用者設定檔中的辦公室位置進行比較。 如果相符的專案少於10個，則會出現 [ **指定位置模式** ] 畫面。 位置模式是用來從辦公室位置提取底價、翼和會議室資訊。

![floorplans-locationpattern.png。](media/floorplans-locationpattern.png)

只需要會議室、floor 和翼是選用的，您可以視需要略過位置。

## <a name="edit-floor-plans"></a>編輯基底計畫

若要更新現有的平面圖，請選取您要變更的地面計畫，然後選取 [ **編輯**]。 進行變更並儲存。

## <a name="troubleshooting"></a>疑難排解

|**步驟**|**錯誤訊息**|**類型**|**動作**|
|:-----|:-----|:-----|:-----|
|Upload 基底計畫|無法讀取 CC_1 dwg。 請重新上傳或刪除地面計畫。|錯誤|請嘗試重新上傳檔案。 如果無法運作，請刪除檔案，然後再試一次。|
|Upload 基底計畫|有兩個檔案名為 CC_1 dwg。 請刪除其中一個名稱，或使用另一個名稱重新上傳。|錯誤|如果檔案名不正確，請新增 floor 或翼形資訊，然後重新上傳檔案，使檔案名成為唯一的。 如果您不小心新增相同的檔案兩次，請將它刪除。|
|Upload 基底計畫|找不到資料。|錯誤|請檢查您的檔案，確定其是否正確，然後重新上傳或刪除。|
|Upload 基底計畫|此檔案中缺少外部參照。 上傳 CC_1_furniture。 dwg 或刪除此檔案。|警告|Upload 外部參考檔案或刪除。|
|Upload 基底計畫|無法讀取 DWG 檔案中的會議室編號或標記。 請刪除此檔案。|警告|請檢查 DWG 檔案，確定已包含資料，然後刪除該檔案，然後再試一次。|
|連結辦公室位置|Azure Active Directory 未找到任何 office 位置。 在設定地面計畫之前，將位置資料新增至 Azure Active Directory。|錯誤|[更新使用者設定檔上的 office 位置](#step-3-update-office-locations-on-user-profiles) |

## <a name="frequently-asked-questions"></a>常見問題集

**問：** 如何查看及編輯 DWG 檔案？

**A：** 使用下列任一選項可查看 DWG 檔案：

- Upload 檔案，以 SharePoint 並加以開啟。
- 在[Microsoft Visio](https://support.office.com/article/Open-insert-convert-and-save-DWG-and-DXF-AutoCAD-drawings-60cab691-0f4c-4fc9-b775-583273c8dac5)或[Autodesk DWG TrueView](https://www.autodesk.com/products/dwg)中開啟檔案。
- 將檔案 Upload 至[Autodesk 的線上檢視器](https://viewer.autodesk.com/)。

**問：** 如何將文字標籤新增至未標記的聊天室？

**A：** 在編輯器中開啟 DWG 檔案，並 [新增會議室標籤](https://knowledge.autodesk.com/support/autocad-map-3d/learn-explore/caas/CloudHelp/cloudhelp/2019/ENU/MAP3D-Learn/files/GUID-4854F184-6279-4E0C-9487-34A4759017F6-htm.html)。

**問：** 如何建立或編輯 DWG 檔案以供測試之用？

**A：** 在 Microsoft Visio、Autodesk AutoCAD 或任何其他 DWG 編輯器中建立 DWG 檔案。 請確定檔案中已標示10個或多個會議室。

**問：** DWG 檔案中的文字標籤的最佳格式是什麼？

**A：** 為了獲得最佳結果，文字標籤應包含底價編號和房間號碼。 下列範例會使用2或 SC 做為建立程式碼。
<!-- markdownlint-disable no-inline-html -->
|會議室標籤類型|Floor|房間|範例文本標籤|建立程式碼/文字標籤 (Office 位置) |
|:-----|:-----|:-----|:-----|:-----|
|具有底價和房間號碼|1|173|1173|2/1173|
|| 21|45|21045|2/21045|
||至|萬美元|23-10 萬美元|2/23-100K|
||1|G06-07|1G06-07|2/1G06-07|
||第|1024A|02.1024 a|2/02.1024 a|
||第|1024A|02.1024 a|2/02.1024 a|
||第|105.01|2105.01|2/2105.01|
|有建立程式碼、基底及房間號碼|0|X-11-M-12|2-0-X-11-M-12|2/2-0-X-11-M-12<br/>2-0-X-11-M-12|
||第|128A|22128A|2/22128A<br/>22128A|
||1|B2-11|21-B2-11|2/21-B2-11<br/>21-B2-11|
||第|45|SC2045|SC/SC2045<br/>SC2045|

**問：** 我可以使用不含底價編號的 DWG 檔案嗎？

**A：** 是的，您可以。 當您在使用者的 Azure Active Directory 設定檔中更新辦公位置時，請將底價號碼包含在會議室號碼的一部分中，即使它在 DWG 檔案中遺失也是一樣。 上傳檔案之後，會出現 [指定位置模式] 畫面，您可以同時指出這兩個值。

例如，包含房間號碼，但沒有底價編號的 DWG 檔案，看起來可能類似如下：

![floorplans-nofloors.png。](media/floorplans-nofloors.png)

使用者設定檔中的 office 位置應該是2/1175，其中 ' 2 ' 是組建碼，' 1 ' 是底價號碼，而 ' 175 ' 是房間號碼。
