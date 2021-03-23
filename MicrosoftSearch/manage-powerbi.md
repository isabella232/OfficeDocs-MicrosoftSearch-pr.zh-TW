---
title: 管理 Power BI 解答
ms.author: dawholl
author: dawholl
manager: jeffkizn
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: c0c814d0-f7e4-444e-b18e-09beb45c9322
description: 管理 Power BI 報表和資料顯示在搜尋結果中的方式
ms.openlocfilehash: 3d67f79cce2392f949541690879ffb9202d79060
ms.sourcegitcommit: 5df252e6d0bd67bb1b4c59418aceca8369f5fe42
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/23/2021
ms.locfileid: "51031438"
---
# <a name="manage-power-bi-answers"></a>管理 Power BI 解答

為了讓您的使用者更容易找到所需的資料和分析，以作出合理的決策，Microsoft Search 已新增對 Power BI 儀表板和報告的支援。 以下是 Power BI 搜尋的一些優點：

* **便於使用：** 這種現成的搜尋體驗可協助使用者輕鬆且快速地找到整個組織中的 Power BI 儀表板和報告。
* **更豐富的內容：** 為了讓 Power BI 搜尋結果更有用，他們包含內容類型的重要資訊：儀表板或報告，以及擁有該專案的小組或人員。
* **內建資料保護：** 只有具備儀表板或報表存取權的使用者才會顯示 Power BI 結果。
* **整合的搜尋體驗：** 為了維持統一的體驗，Power BI 結果在所有搜尋專案點都是一致的。 不論您在哪裡搜尋，都可以使用相同的外觀與風格取得相同的結果。

## <a name="what-users-experience"></a>使用者經驗

Microsoft Search 使用者可以從 [Windows 搜尋] 方塊、[SharePoint]、[Office 365] 和 [Bing] 搜尋，以尋找 Power BI 結果。 使用者可以搜尋報表及儀表板，其查詢如下：

* Power BI 關於 `<topic>`
* Power BI for `<topic>`
* `<topic>` Power BI 儀表板或 Power BI 儀表板 `<topic>`
* `<topic>` Power BI 報表或 Power BI 報表 `<topic>`
* `<topic>` Power BI 計量或 Power BI 度量 `<topic>`
* `<topic>` Power BI 計分卡或 Power BI 計分卡 `<topic>`

`<topic>`請以上述範例取代您所要尋找的資訊，例如銷售、使用方式、容量、2021、Q1 等等，以查看 POWER BI 的相關結果。

:::image type="content" source="media/powerbi-answers/powerbi-serp.png" alt-text="使用 Power BI 解答及垂直 SERP 的螢幕擷取畫面" border="true":::

## <a name="turn-power-bi-search-on-or-off"></a>開啟或關閉 Power BI 搜尋

預設會為您的組織啟用 Power BI 結果。 您的 Power BI 系統管理員可以隨時停用這些功能。 在 Power BI 系統管理員入口網站中，移至 [租使用者設定]，並停 **用 [使用全域搜尋 POWER BI** ] 設定。 若要深入瞭解，請參閱管理 [POWER BI in admin 入口網站](/power-bi/admin/service-admin-portal#use-global-search-for-power-bi-preview)。

:::image type="content" source="media/powerbi-answers/powerbi-admin.png" alt-text="開啟或關閉 Power BI 解答設定的螢幕擷取畫面" border="true":::

## <a name="frequently-asked-questions"></a>常見問題集

**問：預設是否啟用 Power BI 搜尋？**

**A：** 是的。 預設會啟用 Microsoft Search 的 Power BI 搜尋。 此功能不是租使用者管理員所需的首次設定。

**Q：是否可以啟用或停用特定群組或使用者的 Power BI 搜尋功能？**

**A：** 目前只能為您的整個組織啟用或停用。

**問：如果停用 Power BI 搜尋，是否會隱藏 Power BI 搜尋結果頁面？**

**A：** 不。 Power BI 搜尋結果頁面會顯示一則訊息，告知使用者目前無法供其組織使用。

**問：如果我沒有 Power BI 授權，我會看到 Power BI 搜尋結果頁面嗎？**

**A：** 不。 如果搜尋使用者沒有 Power BI 授權，則 [Power BI 搜尋結果] 頁面不會出現在 Microsoft 搜尋結果中。

**問：我是否會看到我無法存取的 Power BI 搜尋結果？**

**A：** 不。 Microsoft 搜尋只會傳回您可以存取的 Power BI 結果。

**問：我可以自訂 Power BI 搜尋結果 (例如，報表類型或報表擁有人) ？**

**A：** 目前，我們不支援自訂 Power BI 搜尋結果中包含的欄位。