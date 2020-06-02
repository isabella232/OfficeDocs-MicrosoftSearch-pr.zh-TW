---
title: 自訂 Microsoft 搜尋頁面
ms.author: jypal6
author: jypal
manager: jeffkizn
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 新增搜尋行業及自訂搜尋結果
ms.openlocfilehash: 44b1b9ff211a65313f5c5cf532334335994c486d
ms.sourcegitcommit: 0050e113517a36e3ca26028a04ac5c236caaf524
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/01/2020
ms.locfileid: "44470279"
---
# <a name="customize-the-search-results-page"></a>自訂搜尋結果頁面

您可以建立搜尋類別和結果類型，以自訂使用者在 Microsoft [SharePoint](https://sharepoint.com/)、 [Microsoft Office](https://office.com)和 microsoft search in [Bing](https://bing.com)中搜尋時所看到的搜尋結果。 縱向使用者可讓使用者更輕鬆地找到他們具有查看許可權的資訊。 例如，您可以為行銷部門中的使用者建立協力廠商軟體的「行銷分析」資料的搜尋類別。 您也可以定義結果類型及自訂此資料的版面配置。  

您可以在下列各層級建立縱向和結果類型：

- **組織層級**–當您在組織層級新增垂直時，當使用者從他們的[SharePoint](https://sharepoint.com/)開始頁面、 [Office](https://office.com)或[Bing](https://bing.com)進行搜尋時，它會出現在搜尋結果頁面上。
- **網站層級**–例如，您可能想要讓客戶服務員工直接從部門的 SharePoint 網站搜尋*嚴重性 1*事件。

## <a name="search-verticals-explained"></a>說明的搜尋縱向

在 [Microsoft 搜尋結果] 頁面的頂端有一列索引標籤。 這些是搜尋行業。 搜尋類別只會顯示特定類型或特定內容的結果。 例如**檔**或**新聞**。 根據預設，Microsoft 搜尋會顯示縱向**所有**的**人員**、**檔**、**網站**和**新聞**。  

您可以新增與您組織相關的搜尋行業。 這些會出現在 [ [SharePoint](https://sharepoint.com/)]、[ [Office](https://Office.com)] 及 [ [Bing](https://bing.com)] 的 [Microsoft 搜尋結果] 頁面上。 例如，您可以根據每個群組所需的資訊類型，為行銷相關的內容及另一個銷售人員建立垂直。 您可以新增縱向，只顯示透過連接器編制索引的內容的結果。  

>[!NOTE]
> 目前在預覽中的縱向和結果類型是 Microsoft Graph 連接器預覽的一部分。 如需預覽的詳細資訊，請參閱[連接器預覽](connectors-preview.md)。 若要參與預覽，您必須先提交[Microsoft Graph 連接器預覽註冊表單](https://forms.office.com/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbRxWYgu82J_RFnMMATAS6_chUNVYwNU1CMDNZUDBSSDZKWVo2RDJDRjRLQi4u)。

## <a name="things-to-consider"></a>考慮事項

開始之前，請確定連接器已編制索引。 這可能需要最多48小時，視檔案大小而定。

您無法為位於[SharePoint](https://sharepoint.com/)的內容，或從檔案[共用連接器](file-share-connector.md)編制索引的內容建立垂直。 瞭解如何為[內容編制索引](configure-connector.md)。

新增垂直的三個基本步驟：

1. 建立垂直。 在這個步驟中，您會定義要搜尋之內容的直排名稱、內容來源及範圍。
2. 定義此垂直方向的結果外觀。  
3. 從垂直清單頁面啟用垂直（顯示）。

## <a name="step-1-create-the-search-vertical"></a>步驟1：建立搜尋類別

啟動該嚮導之後，您會逐步指導您定義要搜尋之內容的垂直名稱、內容來源及範圍。 會以停用狀態建立垂直。 您將在稍後啟用它。

您可以使用一組有限的[關鍵字查詢語言（KQL）](https://docs.microsoft.com/sharepoint/dev/general-development/keyword-query-language-kql-syntax-reference)來縮小範圍。 此頁面列出可用的屬性。 建議您使用 freetext 關鍵字和屬性限制搭配 boolean 運算子來建立 KQL。

### <a name="create-a-vertical-at-the-organization-level"></a>在組織層級建立垂直

若要在[SharePoint](https://sharepoint.com/) Home、 [Office](https://office.com)或[Bing](https://bing.com)中的 Microsoft 搜尋上建立垂直，請遵循下列步驟：

1. 在 microsoft 365 系統 [管理中心](https://admin.microsoft.com)中，移至 **Settings**[   >  **microsoft 搜尋**   >  **縱向**設定]。
1. 選取 [ **新增**] 立即開始。  

### <a name="create-a-vertical-at-the-site-level"></a>在網站層級建立垂直

1. 在您要垂直的[SharePoint](https://sharepoint.com/)網站上，移至 [**設定**]。
1. 選取 [**網站資訊**]，然後**查看 [所有網站設定**]。
1. 尋找 [ **Microsoft 搜尋**] 區段，然後選取 [**設定此網站集合的 microsoft search**]。
1. 在功能窗格中，移至 [ **自訂經驗**]，然後選取 [**縱向**] 索引標籤。
1. 若要新增垂直，請選取 [ **新增**]。
  或者，若要編輯垂直，請在清單中選取它。

請記住，會以停用狀態建立縱向。 您必須先啟用這些功能，使用者才能看到它們。

## <a name="step-2-create-the-result-types"></a>步驟2：建立結果類型

您可以使用結果類型來設計版面配置，以定義結果在垂直方向上的顯示方式。 結果配置可讓您直接在搜尋結果中顯示重要資訊，因此使用者不必選取每個結果，即可查看其是否找到所要尋找的專案。

搜尋「結果類型」是一種規則，可讓不同類型的搜尋結果以不同方式顯示。其由下列項目組成：

- **一個或多個**比較每個搜尋結果的條件，例如搜尋結果的內容來源。  
- 用於符合條件之搜尋結果的**結果版面**配置。 結果版面配置會控制符合條件的所有結果在搜尋結果頁面上顯示和行為的方式。

**您必須建立至少一個結果類型的結果，才會顯示在垂直上。** 您可以為每個垂直方向建立多種結果類型，這可讓您針對不同類型的結果使用不同的版面配置。 例如，您可以自訂*嚴重性為 1*的事件，使其具有更醒目的色彩和更大的字型，與*嚴重的 3*個事件相較。

啟動該嚮導之後，您會逐步指導您定義結果類型的名稱、內容來源及條件。 您可以從清單視圖定義結果類型的優先順序。
  
### <a name="create-a-result-type-at-the-organization-level"></a>在組織層級建立結果類型

1. 在系統[管理中心](https://admin.microsoft.com)中，移至 [**設定**  >  **Microsoft 搜尋**]，然後選取 [**結果類型**]。
1. 若要新增**結果類型**，請選取 [ **新增**]。 若要編輯結果類型，請選取相關清單中的結果類型。

### <a name="create-a-results-type-at-the-site-level"></a>在網站層級建立結果類型

1. 在您要建立結果類型的[SharePoint](https://sharepoint.com/)網站上，移至 [**設定**]。
1. 選取 [**網站資訊**]，然後**查看 [所有網站設定**]。
1. 尋找 [Microsoft 搜尋] 區段，然後選取 [**設定此網站集合的 Microsoft search**]。
1. 在功能窗格中，移至 [ **自訂經驗**]，然後選取 [**結果類型**] 索引標籤。
2. 若要新增結果類型，請選取 [ **新增**]。  或者，若要編輯結果類型，請選取清單中的結果類型。

### <a name="view-the-vertical-after-its-enabled"></a>啟用垂直後查看

在您啟用垂直後，可能需要一段時間，才能進行查看。 如果您不想要等到啟用它之後，您可以在[SharePoint](https://sharepoint.com/)和[Office](https://office.com)的 URL 中附加**cacheClear = true** ，以立即查看垂直。

## <a name="troubleshooting"></a>疑難排解

以下是您可能會遇到的常見問題清單，以及修正這些問題的動作。

|錯誤  |動作  |
|---------|---------|
| 在垂直上看到「發生錯誤」錯誤訊息。 | 需要有垂直和結果類型，才可完成設定。 請確定您已為相同的內容來源建立這兩者。 |
| 我沒有看到結果版面配置，但我已經建立了它。 | 因為這些設定通常會進行快取，所以需要數分鐘的時間。 請等候幾分鐘後再試一次。        |
| 在 [垂直] 或 [結果類型] 頁面上沒有看到任何內容來源。 | 請確定您已設定連接器和索引的資料。   |

## <a name="next-steps"></a>後續步驟

[步驟3：自訂結果版面配置](customize-results-layout.md)
