---
title: 在 Microsoft 搜尋中管理縮寫詞答案
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
description: 在 Microsoft 搜尋中建立及更新縮寫的答案
ms.openlocfilehash: e328ecb7604a144b51f3a1483eef1b1c3a7e0bcb
ms.sourcegitcommit: 988c37610e71f9784b486660400aecaa7bed40b0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "47422944"
---
# <a name="manage-acronyms-answers-in-microsoft-search"></a>管理 Microsoft 搜尋中的縮寫詞答案

使用者通常會在組織或小組所用的不熟悉縮寫和縮寫中執行。 組織或小組特有的條款，對從一個小組移至另一個小組的人員來說可能是新的，可與內部協力廠商小組共同作業，或是組織的新功能。

組織不一定會有單一參考的標準術語。 缺乏單一參考會使您很難尋找這些縮寫詞的定義或擴充。 Microsoft 搜尋會解決與首字的問題。

## <a name="what-users-experience"></a>使用者經驗

Microsoft Search 使用者可以在 [Bing](https://Bing.com)、 [SharePoint](https://products.office.com/sharepoint/collaboration)和 [Office 365](https://Office.com)中取得具有縮寫的定義。 在 [ **搜尋** ] 方塊中，使用者輸入如下範例的查詢：

- *何謂* DNN
- *定義* DNN
- DNN *定義*
- *展開* DNN
- DNN *擴充*
- *的意義* DNN
- DNN *表示*

結果會包含使用者組織中所顯示之 DNN 的所有意義。

> [!NOTE]
> 使用者必須輸入包含縮寫詞所指定 *關鍵字* 的查詢，以觸發其對應的答案。 縮寫詞查詢不區分大小寫。

## <a name="set-up-acronyms-answers"></a>設定縮寫詞答案

在 [Microsoft 365 系統管理中心](https://admin.microsoft.com)中，移至 [ [**縮寫**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms)]，然後選取 [ **新增縮寫**]。

Microsoft 搜尋會查詢兩個數據源，以提供使用者搜尋的縮寫答案：

1. **編輯縮寫**。 由系統管理員在系統管理員 [中央](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms)提供。
2. **挖掘的縮寫**。 由 Microsoft 搜尋從使用者的個人電子郵件和檔，以及組織內可公開使用的資料進行挖掘。

### <a name="set-up-editorial-acronyms"></a>設定編輯縮寫

搜尋管理員可以在[Microsoft 搜尋系統管理中心](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch)的 [[縮寫]](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/acronyms)索引標籤上設定編輯縮寫。 您可以從任何內部網站或存放庫向系統管理中心新增縮寫。 編輯縮寫可以新增至 **已發佈** 或 **草稿** 的狀態：

**發行狀態**。 組織中的雇員可透過 Microsoft 搜尋取得縮寫。

> [!NOTE]
> 最多可能需要三天的縮寫，以在 Microsoft 搜尋中加入已發佈的狀態。

**草稿狀態**。 如果系統管理員想要在 Microsoft 搜尋中提供首字縮寫的答案，可將縮寫新增至草稿狀態。 新增至草稿狀態的縮寫詞無法在 Microsoft 搜尋中使用。 系統管理員必須將縮寫詞新增至發行的狀態，以供使用。

系統管理員可以個別新增首字縮寫或在 CSV 檔案中大量匯入。 使用下表所示的欄位上載 CSV 檔案：

| 縮寫 (強制)  | 擴充 (強制)  | 描述  | 來源 | 狀態 (強制)  |
| --------- | --------- | ---------- | --------- |--------- |
| *Xxx* | *拼寫縮寫* |  | [URL]** | *已發佈或草稿* |

### <a name="csv-fields"></a>CSV 欄位

**縮寫**。 包含實際的簡寫形式或縮寫。 例如， *DNN*。

**擴充**。 包含縮寫的擴充。 例如， *Deep 神經網路*。

**描述**。 縮寫的簡短描述，可提供使用者更多有關縮寫和其擴充的資訊。 例如， *deep 神經網路是具有某一層級複雜性的神經網路，具有超過兩層的神經網路*。

**來源**。 您要讓使用者流覽的頁面或網站 URL，以取得有關縮寫的詳細資訊。

**狀態**。 此欄位可以採用兩個值：

- **草稿**。 將縮寫新增至草稿狀態。
- **發行**。 將縮寫新增至發佈的狀態，並使其可用於 Microsoft 搜尋。

### <a name="mined-acronyms"></a>挖掘縮寫

將組織內使用的所有縮寫詞新增至答案可能是一項挑戰。 這項功能可找出搜尋系統管理員甚至不會察覺的縮寫。 若要執行這項操作，Microsoft 搜尋也會從這些來源中地雷的縮寫：

- 使用者的電子郵件。
- [SharePoint](https://products.office.com/sharepoint/collaboration)、 [Microsoft OneDrive]( https://onedrive.live.com/about/)和[microsoft OneNote](https://www.onenote.com/)中的檔。
- 組織內的公用檔，可供使用者在 SharePoint、OneDrive 或 OneNote 中存取。

Microsoft 搜尋可確保只有對檔具有存取權和許可權的使用者才能看到其所挖掘的縮寫。 從使用者的信箱中挖掘縮寫時，只有該使用者可以看到該縮寫。

> [!NOTE]
> 挖掘的縮寫不需要任何設定。

## <a name="frequently-asked-questions"></a>常見問題集

**問：如何進行編輯及挖掘的資料排名？**

**A：** 目前的功能是對已挖掘的首字母縮寫詞排名編輯縮寫。

**問：在 Microsoft 搜尋中發佈後，編輯的首字縮寫詞必須多久才會顯示？**

**A：**  已發佈的狀態最多需要三天的縮寫，以供 Microsoft 搜尋使用。

**問：使用者如何觸發縮寫詞答案？**

**答**：若要取得縮寫的答案，使用者必須在 [ [Bing](https://bing.com)]、[ [SharePoint](https://products.office.com/sharepoint/collaboration)] 或 [ [Office 365](https://Office.com) **搜尋** ] 方塊中輸入特定的查詢模式。

**問：當您收到或傳送新的電子郵件或檔之後，挖掘的首字縮寫會出現多久時間？**

**A：** 從新的電子郵件或檔中挖掘的首字母縮寫，會在 Microsoft 搜尋結果中長達7天。

**問：是否需要使用特定的挖掘格式來挑選檔？**

**A：** 不。 我們支援所有檔案類型，但不包括影像、資料夾和 ZIP 檔案。

**問： Microsoft 是否會利用所有語言的檔中的縮寫？**

**A**： Microsoft 只支援從英文檔進行挖掘。 其他語言的支援會分階段新增。

**問：如果我的組織不想要顯示挖掘的縮寫，該怎麼辦？是否可以停止在搜尋結果中顯示挖掘的縮寫？**

**A**：若要在搜尋結果中關閉顯示挖掘的縮寫，請遵循 [商務產品的連絡人支援服務](https://docs.microsoft.com/office365/admin/contact-support-for-business-products?redirectSourcePath=%252f%252farticle%252fContact-Office-365-for-business-support-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b&view=o365-worldwide&tabs=online#BKMK_call_support)中的指示，建立客戶支援憑證。
在您建立支援票證之後，挖掘的首字縮寫會花長達48小時的時間，才會出現在搜尋結果中。
