---
title: 管理 Microsoft 搜尋中的縮略字解答
ms.author: v-pamcna
author: TrishaMc1
manager: mnirkhe
ms.date: 10/28/2019
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 建立及更新 Microsoft 搜尋中的縮略字解答
ms.openlocfilehash: 8ff48f1eaa4ef8dab83411fad2f0ee4367158cd1
ms.sourcegitcommit: bfcab9d42e93addccd1e3875b41bc9cc1b6986cc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2019
ms.locfileid: "37949708"
---
# <a name="manage-acronyms-answers-in-microsoft-search"></a>管理 Microsoft 搜尋中的縮略字解答

經常遇到不太熟悉的縮略字的員工和其組織或小組所使用的縮寫。 專用於組織或小組的字詞可能是新的人員將從一個小組移至另一個，使用內部合作夥伴小組或新員工的人。

組織不一定需要其更新標準術語的單一參照。 單一參考缺乏所以很難尋找定義或擴充這些縮略字。 Microsoft Search 求解縮略字該問題。

## <a name="what-users-experience"></a>使用者體驗
Microsoft Search 使用者可以取得與縮略字[Bing](https://Bing.com)、 [Microsoft Office 365](https://Office.com)和[Microsoft SharePoint Online](https://products.office.com/sharepoint/collaboration)中的定義。 在標頭列中的 [**搜尋**] 方塊中，在使用者輸入查詢，例如這些範例：

- *什麼是*DNN
- *定義*DNN
- DNN*定義*
- *依序展開 [* DNN
- DNN*擴充*
- *代表的意義*DNN
- DNN*表示*

建議的結果會包含所有的意義 DNN 相關使用者的組織內。

> [!NOTE]
> 使用者必須輸入的查詢，包括縮略字指定的*關鍵字*，觸發其相對的答案。  

## <a name="set-up-acronyms-answers"></a>設定縮略字解答
在 Microsoft 365[系統管理中心](https://admin.microsoft.com)中，移至 [**設定** > **Microsoft Search** >**縮略字**，然後選取 [**新增縮略字**。 

Microsoft 搜尋查詢以提供使用者搜尋的縮略字答案的兩個資料來源：

1.  **編輯縮略字**。 在[系統管理中心](https://admin.microsoft.com)中的 IT 系統管理員所提供。
2.  **Mined 縮略字**。 由 Microsoft Search mined 從使用者的個人電子郵件和文件和公開提供組織內的資料。

### <a name="set-up-editorial-acronyms"></a>設定編輯縮略字
IT 系統管理員可以設定[Microsoft 365 系統管理中心]( https://admin.microsoft.com)中的[縮略字] 索引標籤](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch)上的編輯縮略字。 系統管理中心，您可以從任何內部網站或存放庫新增縮略字。 編輯縮略字可以新增至**已發佈**] 或 [**草稿**] 狀態：

**已發佈的狀態**。 可透過 Microsoft 搜尋組織的員工的縮略字。

> [!NOTE]
> 可能需要最多三天的縮略字加入至已發佈狀態成為用於 Microsoft Search。

**草稿狀態**。 如果系統管理員想要檢閱的縮略字解答之前先用於 Microsoft Search，他們可以新增縮略字為草稿狀態。 縮略字加入至草稿狀態不會出現在 Microsoft Search。 系統管理員必須將縮寫新增至發佈狀態，以使其能。

系統管理員可以將縮略字個別或大量將它們匯入 CSV 檔案。 上傳 CSV 檔案與欄位，如下表所示：

| 縮寫 （必要） | 擴充 （必要） | 描述  | 來源 | 狀態 （必要） |
| --------- | --------- | ---------- | --------- |--------- |
| *XXX* | *拼出縮寫* |  | *URL* | *發佈或草稿* |

### <a name="csv-fields"></a>CSV 欄位
**縮略字**。 未包含實際短格式或縮略字。 例如， *DNN*。

**擴充**。 包含擴充的縮寫。 例如，*深層非線性網路*。

**描述**。 讓使用者快速深入的縮寫和其擴充什麼縮略字簡短描述。 例如，複雜性的*deep 非線性網路是複雜性的非線性一定程度，具有兩個以上的圖層的非線性網路與網路*。

**來源**。 頁面或您想要使用者前往的縮略字的詳細資訊的網站的 URL。

**狀態**。 此欄位可能需要兩個值：

- **草稿**。 將縮寫新增至 「 草稿 」 狀態。
- **發佈**。 會將縮寫新增至已發佈狀態，並使它用於 Microsoft Search。

### <a name="mined-acronyms"></a>生產縮略字
它可能是系統管理員新增解答組織內所使用的所有縮寫挑戰。 這項功能可以找到搜尋系統管理員的縮略字不即使留意。 若要執行該工作，Microsoft Search 也地雷縮略字從這些來源：

- 使用者的電子郵件。
- [SharePoint](https://products.office.com/sharepoint/collaboration)、 [Microsoft OneDrive]( https://onedrive.live.com/about/)及[Microsoft OneNote](http://www.onenote.com/)文件。
- 公用使用者可以存取 SharePoint、 OneDrive 或 OneNote 中的組織內的文件。

Microsoft Search 可確保只有存取與文件的權限的使用者可以看到 mined 從它的縮略字。 縮略字是 mined 從使用者的收件匣，並儲存在使用者晶怪。 只有該使用者可以存取使用者本身的收件匣 mined 縮略字。

> [!NOTE]
> 沒有 IT 系統管理員設定所需的生產縮略字。

## <a name="frequently-asked-questions"></a>常見問題集
**問： 如何編輯與生產資料的排名？**

**答：** 此功能目前排名上方生產縮略字編輯縮略字。

**問： 如何長多久要發佈後要顯示在 Microsoft Search 的編輯縮略字？**

**答：** 花費最多三天的縮略字加入至已發佈狀態成為用於 Microsoft Search。 

**問： 如何使用者會觸發縮略字回答？**

**A**： 若要取得的縮略字解答，使用者必須在[Bing](https://bing.com)、 [Office 365](https://Office.com)或[SharePoint](https://products.office.com/sharepoint/collaboration) **搜尋**方塊中輸入特定的查詢模式。 字詞*DNN*找到答案的查詢的範例如下所示：

- *什麼是*DNN
- *定義*DNN
- DNN*定義*
- *依序展開 [* DNN
- DNN*擴充*
- *代表的意義*DNN
- DNN*表示*

**問： 如何長多久要顯示在您接收或傳送新電子郵件或文件後的生產縮略字？**

**答：** 從新的電子郵件或文件的生產縮略字需要多達七天 Microsoft 搜尋結果中顯示。

**問： 是否需要位於採礦挑選備份的特定格式的文件？**

**答：**[否]。 我們支援影像、 資料夾及 zip 檔案以外的所有檔案類型。

**問： 將 Microsoft 採擷從文件中的所有語言的縮略字嗎？**

**A**: Microsoft 僅支援從文件的採礦以英文顯示。 將階段中新增其他語言的支援。

**問： 如果我的組織不想要顯示生產的縮略字嗎？可以停止在搜尋結果中的顯示 [mined 縮略字嗎？**

**A**： 若要關閉搜尋結果中顯示 [mined 縮略字，建立客戶支援票證遵循在[連絡商務產品的技術支援](https://docs.microsoft.com/office365/admin/contact-support-for-business-products?redirectSourcePath=%252fen-us%252farticle%252fContact-Office-365-for-business-support-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b&view=o365-worldwide&tabs=online#BKMK_call_support)的指示進行。
建立支援票證之後，所花費達 48 小時停止出現在搜尋結果的生產縮略字。 

**問： 什麼時候會看到[Office 365](https://Office.com)和[SharePoint Online](https://products.office.com/sharepoint/collaboration)中的縮略字回答？**

**A**： 縮略字解答可用目前僅在 Microsoft [Bing](https://bing.com)搜尋。 他們會被導入至 Office 365 和 SharePoint Online 中 2020年。
