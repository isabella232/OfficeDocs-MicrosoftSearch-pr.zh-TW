---
title: 自訂 Microsoft 搜尋頁面
ms.author: jeffkizn
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
ms.openlocfilehash: 6b6f0593a668e9c2c5c7fc5a62f7b5dd4a43a8bb
ms.sourcegitcommit: ea6905626de67090141039565282e4e0c53b43ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/07/2021
ms.locfileid: "53314017"
---
# <a name="customize-the-search-results-page"></a>自訂搜尋結果頁面

您可以建立搜尋類別和結果類型，以自訂使用者在 Microsoft [SharePoint](https://sharepoint.com/)、 [Microsoft Office](https://office.com)及 Microsoft 搜尋中的[Bing](https://bing.com)搜尋時所看到的搜尋結果。 縱向使用者可讓使用者更輕鬆地找到他們具有查看許可權的資訊。 例如，您可以為行銷部門中的使用者建立協力廠商軟體的「行銷分析」資料的搜尋類別。 您也可以定義結果類型及自訂此資料的版面配置。  

您可以在下列各層級建立縱向和結果類型：

- **組織層級**–當使用者從其 [SharePoint](https://sharepoint.com/)開始頁面、 [Office](https://office.com)或 [Bing](https://bing.com)進行搜尋時，會顯示在搜尋結果頁面上的 [組織] 層級。
- **網站層級**–例如，您可能想要讓客戶服務員工直接從部門的 SharePoint 網站搜尋 *嚴重性 1* 事件。

## <a name="search-verticals-explained"></a>說明的搜尋縱向

在 [Microsoft 搜尋結果] 頁面的頂端，有一列索引標籤。 這些是搜尋行業。 搜尋類別只會顯示特定類型或特定內容的結果。 例如 **檔** 或 **新聞**。 依預設，Microsoft 搜尋會顯示 **所有** 的縱向、**人員**、**檔案、****網站** 和 **新聞**。  

您可以新增與您組織相關的搜尋行業。 這些會出現在 Microsoft 搜尋結果頁面上[SharePoint](https://sharepoint.com/)、 [Office](https://Office.com)及[Bing](https://bing.com)。 例如，您可以根據每個群組所需的資訊類型，為行銷相關的內容及另一個銷售人員建立垂直。 您可以新增縱向，只顯示透過連接器編制索引的內容的結果。  

### <a name="multiple-connections-in-a-vertical"></a>垂直中的多個連接

「搜尋類別」現在可以透過多個連接器來源呈現結果。 這為設計搜尋結果頁面提供更大的彈性。 現有的垂直安裝管理體驗可讓您在「內容來源」步驟中選取多個連接。
如果您正確指派盡可能多的語義標籤，則會增強這種體驗。 您可以在架構定義及攝取時新增語義標籤。

[以下](configure-connector.md#step-5-assign-property-labels) 是如何建立及管理語義標籤的其他資訊。

> [!NOTE]
> 垂直中的多個連線目前正在預覽中。 如需預覽的詳細資訊，請參閱 [連接器預覽功能](connectors-overview.md#what-are-the-preview-features)。

### <a name="things-you-should-know"></a>您應該知道的事項

1. 可以將連線新增為一個垂直下方的內容來源。 不允許重複使用多個行業的連線。
2. 如果您需要為已新增多個連線來源的搜尋類別設定查詢，則應該使用一般來源屬性來建立這類查詢。

## <a name="things-to-consider"></a>考慮事項

開始之前，請確定連接器已編制索引。 這可能需要最多48小時，視檔案大小而定。

您無法為位於[SharePoint](https://sharepoint.com/)中的內容建立垂直。

新增垂直的三個基本步驟：

1. 建立垂直。 在這個步驟中，您會定義要搜尋之內容的直排名稱、內容來源及範圍。
2. 定義此垂直方向的結果外觀。  
3. 啟用從垂直清單頁面) 顯示的垂直 (。

## <a name="step-1-create-the-search-vertical"></a>步驟1：建立搜尋類別

啟動該嚮導之後，您會逐步指導您定義要搜尋之內容的垂直名稱、內容來源及範圍。 會以停用狀態建立垂直。 您將在稍後啟用它。

您可以使用一組有限的 [關鍵字查詢語言 (KQL) ](/sharepoint/dev/general-development/keyword-query-language-kql-syntax-reference) 來縮小範圍。 此頁面列出可用的屬性。 建議您使用具有 boolean 運算子的任意文字關鍵字和屬性限制，以建立 KQL。
KQL 也支援使用 [設定檔查詢變數](#profile-query-variables) ，在垂直方向微調結果。

### <a name="create-a-vertical-at-the-organization-level"></a>在組織層級建立垂直

若要在[SharePoint](https://sharepoint.com/) home、 [Office](https://office.com)或[Bing](https://bing.com)中的 Microsoft 搜尋上建立垂直的，請遵循下列步驟：

1. 在 [Microsoft 365 系統管理中心](https://admin.microsoft.com)中，移至 [[**縱向**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/verticals)]。
2. 選取 [ **新增** ] 立即開始。  

### <a name="create-a-vertical-at-the-site-level"></a>在網站層級建立垂直

1. 在您要垂直的 [SharePoint](https://sharepoint.com/)網站上，移至 **設定**。
2. 選取 [ **網站資訊** ]，然後 **查看 [所有網站設定**]。
3. 尋找 [ **Microsoft 搜尋**] 區段，然後 **為此網站集合選取 [設定 Microsoft 搜尋**]。
4. 在功能窗格中，移至 [ **自訂經驗**]，然後選取 [ **縱向** ] 索引標籤。
5. 若要新增垂直，請選取 [ **新增**]。
  或者，若要編輯垂直，請在清單中選取它。

請記住，會以停用狀態建立縱向。 您必須先啟用這些功能，使用者才能看到它們。

## <a name="step-2-create-the-result-types"></a>步驟2：建立結果類型

您可以使用結果類型來設計版面配置，以定義結果在垂直方向上的顯示方式。 結果配置可讓您直接在搜尋結果中顯示重要資訊，因此使用者不必選取每個結果，即可查看其是否找到所要尋找的專案。

### <a name="default-search-result-layout"></a>預設搜尋結果版面配置

如果在設定連接器時， **標籤** 和 **內容** 屬性已正確對應至來源內容，則會針對連接器內容顯示預設的搜尋結果版面配置。 標籤 **標題** 是最重要的標籤。 **強烈建議** 您指派此標籤的屬性，以使用預設搜尋結果版面配置。

### <a name="create-your-own-result-type"></a>建立您自己的結果類型

您可以決定建立您自己的搜尋結果版面配置，並透過建立 **結果類型** 來覆寫預設搜尋結果版面配置。 搜尋結果類型是一種規則，會以不同方式顯示不同類型的搜尋結果。 其包含下列各項：

- **一個或多個** 比較每個搜尋結果的條件，例如搜尋結果的內容來源。  
- 用於符合條件之搜尋結果的 **結果版面** 配置。 產生的版面配置會控制符合條件的所有結果在搜尋結果頁面上顯示和行為的方式。

**如果適當的對應無法顯示預設搜尋結果版面配置，您必須至少建立一個結果類型的結果，以顯示在垂直上。** 您可以為每個垂直方向建立多種結果類型，這可讓您針對不同類型的結果使用不同的版面配置。 例如，您可以自訂 *嚴重性為 1* 的事件，使其具有更醒目的色彩和更大的字型，與 *嚴重的 3* 個事件相較。

啟動該嚮導之後，您會逐步指導您定義結果類型的名稱、內容來源及條件。 您可以從清單視圖定義結果類型的優先順序。
  
### <a name="create-a-result-type-at-the-organization-level"></a>在組織層級建立結果類型

1. 在 [Microsoft 365 系統管理中心](https://admin.microsoft.com)中，移至 [[**結果類型**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/resulttypes)]。
2. 若要新增 **結果類型**，請選取 [ **新增**]。 若要編輯結果類型，請選取相關清單中的結果類型。

### <a name="create-a-results-type-at-the-site-level"></a>在網站層級建立結果類型

1. 在您要建立結果類型的 [SharePoint](https://sharepoint.com/)網站上，移至 **設定**。
2. 選取 [ **網站資訊** ]，然後 **查看 [所有網站設定**]。
3. 尋找 [Microsoft 搜尋] 區段，然後 **為此網站集合選取 [設定 Microsoft 搜尋**]。
4. 在功能窗格中，移至 [ **自訂經驗**]，然後選取 [ **結果類型** ] 索引標籤。
5. 若要新增結果類型，請選取 [ **新增**]。  或者，若要編輯結果類型，請選取清單中的結果類型。

## <a name="step-3-view-the-vertical-after-its-enabled"></a>步驟3：在啟用垂直後查看

在您啟用垂直後，您可以花幾小時的時間，才能進行查看。 如果您不想要等到啟用它之後，您可以在 [SharePoint](https://sharepoint.com/)和 [Office](https://office.com)中將 **cacheClear = true** 新增至 URL，以便立即查看垂直方向。 若為 [Bing](https://bing.com)，請將 **&功能** 新增至工作垂直 URL，以立即查看縱向。

> [!NOTE]
> 從行動網頁瀏覽器中查看時，不會在[SharePoint](https://sharepoint.com/)和[Office](https://office.com)上看到新增的縱向。

## <a name="profile-query-variables"></a>設定檔查詢變數

查詢變數是用於垂直的 [KQL 查詢] 區段中，以提供動態資料做為垂直查詢的輸入。 您可以使用設定檔查詢變數，讓搜尋結果成為已登入使用者的上下文。 設定檔查詢變數會從已登入使用者的 [設定檔](/graph/api/resources/profile?view=graph-rest-beta)中取得值。

例如，如果您想要建立「票據」垂直，其中登入的使用者可以搜尋其所指派的支援票證，您可以在 [管理] 頁面的 [查詢] 區段中指定下列查詢。  

**AssignedTo： {Profile。 userPrincipalName}**

這會縮小搜尋結果，以顯示受託人為執行搜尋之使用者的專案。

[設定檔資源](https://graph.microsoft.com/graph/api/resources/profile?view=graph-rest-beta) 公開屬性做為集合。 例如，電子郵件地址相關的資訊會透過電子郵件集合、工作職位集合等方式公開。 使用者設定檔中所有可用的屬性，都是以「AAD」為來源類型的方式公開為查詢變數。

請考慮電子郵件集合中有三個可用電子郵件地址的使用者，如下所示。

```json
"emails": [{ 

        "address": "Megan.Bowen@contoso.com",
        "id": "xyz", 
        "source": { 
            "CreatedBy": "xyz", 
            "CreatedOn": "2222", 
            "Type": "official" 
        },
        "type": "main" 
    }, { 
        "address": "meganb@hotmail.com",
        "id": "abc", 
        "source": { 
            "CreatedBy": "abc",
            "CreatedOn": "3333", 
            "Type": "non-official",
        },
        "type": "work"
    }, { 
        "address": "meganb@outlook.com",
        "id": "pqr", 
        "source": { 
            "CreatedBy": "pqr", 
            "CreatedOn": "4444", 
            "Type": "personal" 
        },
        "type": "personal" 
    } 
] 
```

- 查詢 **MyProperty： {Profile. 電子郵件地址}** 會解析為 MyProperty： "Megan.Bowen@contoso.com"。  

- 如果您想要解決 address 屬性的所有值，您必須使用多重值擴充語法。 查詢 **{|MyProperty： {Profile. 電子郵件地址}}** 會解析為 ( (MyProperty： "Megan.Bowen@contoso .com" ) 或 (MyProperty： "meganb@hotmail.com" ) 或 (MyProperty： "meganb@outlook" ) )   

"|" 運算子應該用來解析多重值變數。 如需設定檔擴充的更多範例，請參閱下表。

| #         | 語法 |  傳回值  |
| --------- | ------ | --- |
| 1     | MyProperty： {設定檔. 電子郵件地址}  |   "Megan.Bowen@contoso.com"  |
| 2  | MyProperty： {Profile} 電子郵件}   |    因為電子郵件是物件，所以 {Profile} 電子郵件} 這不會解決。|
| 3     | {?MyProperty： {Profile. 電子郵件}}  |  這不會解決，因為電子郵件是物件。 "？" 運算子會忽略不會解析的查詢變數。 在查詢堆疊上進一步傳遞時，將會移除此變數。   |
| 4  | {&#124;MyProperty： {Profile. Type}}    |   ( (MyProperty： "官方" ) 或 (MyProperty： "非官方" ) 或 (MyProperty： "personal" ) )     |

> [!NOTE]
>
> - 只有使用 [連接器](connectors-overview.md) 做為內容來源的自訂的行業，才支援設定檔查詢變數。
> - 設定檔查詢變數是在 [垂直設定處理](customize-search-page.md#step-1-create-the-search-vertical)程式的「查詢」區段中定義。
> - 設定檔查詢變數目前在預覽中。 如需預覽的詳細資訊，請參閱 [連接器預覽功能](connectors-overview.md#what-are-the-preview-features)。

## <a name="troubleshooting"></a>疑難排解

以下是您可能會遇到的常見問題清單，以及修正這些問題的動作。

|錯誤  |動作  |
|---------|---------|
| 在垂直上看到「發生錯誤」錯誤訊息。 | 需要有垂直和結果類型，才可完成設定。 請確定您已為相同的內容來源建立這兩者。 |
| 我沒有看到結果版面配置，但我已經建立了它。 | 因為這些設定通常會進行快取，所以需要數分鐘的時間。 請等候幾分鐘後再試一次。        |
| 在 [垂直] 或 [結果類型] 頁面上沒有看到任何內容來源。 | 請確定您已設定連接器和索引的資料。   |

## <a name="next-steps"></a>後續步驟

[自訂結果版面配置](customize-results-layout.md)
