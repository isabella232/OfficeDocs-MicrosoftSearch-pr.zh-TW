---
title: 使用 Microsoft Search 讓內容易於尋找
ms.author: anfowler
author: adefowler
manager: mnirkhe
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 建立書籤、位置和問與答項目，讓組織的內容易於尋找。
ms.openlocfilehash: 0cf3152e7fb47f0cb1b1fa3fe0df43645a2536e171fd8211050a1773ec86a490
ms.sourcegitcommit: 71ac2a38971ca4452d1bddfc773ff8f45e1ffd77
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/06/2021
ms.locfileid: "54532937"
---
# <a name="make-content-easy-to-find"></a>讓內容易於尋找

Microsoft Search 可協助使用者找到相關內容。 它是一種能同時安全地搜尋您內部網路與 Web 內容的方式。 只有 Microsoft 能夠提供這類跨網路和組織的整合。 有了 Microsoft Search，系統管理員可以使用其組織的知識，讓使用者易於找到相關內容。 

## <a name="components-that-find-content"></a>尋找內容的元件
在 Microsoft 搜尋中，系統管理員會建立[書簽](manage-bookmarks.md)、 [PowerApps](integrate-powerapps.md)、 [Q&A](manage-qas.md)和[位置](manage-locations.md)，讓內容更容易尋找。 每個搜尋元件都包括標題、URL，和一組能觸發書籤的關鍵字。

## <a name="bookmarks"></a>書籤
您可以只在幾個步驟中建立 [書簽](manage-bookmarks.md) 。 每個書籤都包括標題、URL，和一組能觸發書籤的關鍵字。 書簽可以有多個關鍵字，而有些書簽可以共用相同的關鍵字。 但是保留關鍵字無法共用。 當您建立或修改書簽時，搜尋索引會重新整理，而且書簽會立即可供使用者使用。

如果您的組織已在 [SharePoint](http://sharepoint.com/)中 **提升結果**，您可以將這些結果匯入 Microsoft 搜尋中。 透過升級的結果，您可以快速填入搜尋結果、將內容提供給使用者，並在設定 Microsoft 搜尋後，立即將其設為有效。 建議您使用來自 SharePoint 提升的結果做為參考，以了解如何指定和建立相關的搜尋結果。 

### <a name="add-or-edit-bookmarks-by-using-browser-extensions"></a>使用瀏覽器擴充新增或編輯書簽
搜尋系統管理員可以使用瀏覽器擴充功能輕鬆地建立搜尋內容。 若要將網站新增為書簽，請安裝瀏覽器擴充。 然後移至網站，並將其新增為書簽。 若要深入瞭解，請參閱 [管理書簽](manage-bookmarks.md)。

目前，瀏覽器擴充功能可用於[Microsoft Edge](https://www.microsoft.com/windows/microsoft-edge)和[Google Chrome](https://www.google.com)： 
- 若要下載 Edge 延長線，請移至[Microsoft Store](https://www.microsoft.com/p/microsoft-search-content-creator/9nrqdbcbwq55?activetab=pivot:overviewtab)。
- 若要下載 Chrome 分機，請移至 [chrome web store](https://chrome.google.com/webstore/detail/microsoft-search-content/nocnablpaoeecfmfnjoheefkogmleipm)。

## <a name="powerapps"></a>PowerApps

透過將現有的 [PowerApps](integrate-powerapps.md) 新增到 [書簽](manage-bookmarks.md)中，使用者就可以像輸入休假時間或報告費用等工作來完成工作。 

透過 [PowerApps](integrate-powerapps.md)，您可以在瀏覽器中或在電話或平板電腦上建立執行的商務應用程式。 不需要任何的編碼經驗。 PowerApps 可在任何瀏覽器和任何裝置上運作。 其新增時間不會超過一分鐘。 若要深入瞭解 PowerApps，請參閱下列文章：
- [引導學習](/learn/browse/?products=powerapps)
- [PowerApps 檔](/powerapps/maker/canvas-apps/get-sessionid)
- [PowerApps 首頁](https://make.preview.powerapps.com/environments/839eace6-59ab-4243-97ec-a5b8fcc104e4/home)

### <a name="add-a-powerapp-to-a-bookmark"></a>將 PowerApp 新增至書籤

1. 尋找您要新增之 PowerApp 的 [應用程式識別碼](/powerapps/maker/canvas-apps/get-sessionid#get-an-app-id) 。
1. 在 Microsoft 365 系統 [管理中心](https://admin.microsoft.com)，移至 **設定**  >  **Microsoft 搜尋**]。 
1. 新增書籤或尋找您想要新增 PowerApp 的現有書籤。
1. 在 [ **書簽設定**] 中，選取 [ **電源 App**]。 然後選取 [ **新增電源應用程式**]。
1. 輸入 **應用程式識別碼**。 自動調整高度和寬度。 [書簽](manage-bookmarks.md) 可以同時支援縱向及橫向方向，但目前的大小無法變更。 為了便於測試，書簽預覽會顯示完整運作 PowerApp。
1. 選取 [發佈] 或 [儲存為草稿]。

## <a name="qa"></a>問與答

建立 [Q&](manage-qas.md) 類似于建立 [書簽](manage-bookmarks.md)。 在 Q&A，您可以提供使用者問題的答案，而不只是網頁的連結。 您可以使用可用的工具，格式化 rtf 文字中的答案。 如果書簽和 Q&共用相同的關鍵字，則會先顯示書簽結果。 如同書簽，Q&會在您新增或變更 Q&A 之後立即重新整理索引。 

### <a name="supported-html-tags"></a>支援的 HTML 標記

您可以使用 HTML 內容或將 HTML 標籤新增至您的答案或描述。 目前支援這些 HTML 標記：
 
- blockquote
- div
- em
- h1、h2、h3 和 h4
- ol、ul 和 li
- p
- pre
- span
- strong
- table、thead、tbody、tr、th 和 td
- u
- a
- code
- br
- hr
- img

不支援的標記會被略過或顯示為文字。 確認您預覽您的卡片。

> [!Note]
> 如果範本檔案中有錯誤，則無法匯入 Q&專案。 若要防止錯誤，請確定您的匯入檔案已正確格式化，且包含所有必要的資訊。 請參閱如何 [防止匯入錯誤](#prevent-import-errors)的詳細資訊。

## <a name="locations"></a>位置

透過 [位置](manage-locations.md)，您的使用者可以尋找位址並找到您組織的大樓。 **位置** 功能可為辦公室、校園和辦公樓提供正確的位置，以及方位和導覽。 為了獲得最佳結果，系統管理員必須將其組織的所有重要位置新增至 Microsoft 搜尋。 不同于 [書簽](manage-bookmarks.md) 和 [Q&A](manage-qas.md)，位置索引不會立即重新整理。 新的或已變更的位置出現在搜尋結果中，可能需要數小時的時間。

## <a name="get-started"></a>開始使用
若要瞭解您的使用者所需的資訊，並使該資訊易於探索，請嘗試下列其中一種方法：

- 使用內部網路搜尋記錄來判斷獲得最多流量的網站與頁面。
- 判斷每天或每週使用的 App、網站和工具。
- 尋找員工福利的直接連結。
- 找出使用者需要注意的原則與程序。
- 決定使用者的連絡人以尋求支援，以及如何執行該動作。
- 以業務週期為 seasonally 或根據業務週期，取得定期所需的資訊。 例如，在尋找用來休假或每季財務更新的工具時。
- 收集區域或行動使用者的原則。 範例是因位置而異的效益。
- 決定一般 web 搜尋的內部網站和資訊。 例如流量、公開轉口資訊、當地天氣、公司合作夥伴提供的折扣以及健康和健身計畫。
- 尋找公司贊助活動、會議或退休會等資訊。
- 搜尋常用 IT、HR 與支援問題，以及常見問題集 (FAQ) 和解答。

## <a name="involve-smes-and-users"></a>涉及 Sme 和使用者
在組織中，使用者可搜尋簡單的複雜主題範圍。 簡單的範例是 office 位址和員工權益。 複雜的範例是新的工作流程、技術資訊和操作方式內容。 若要建立或尋找各種各樣的內容，您需要不同欄位、主題及技術的專業技術。 

大部分搜尋系統管理員都沒有每個主體的特定知識。 若要在外部資源無説明的情況下調整可用內容的數量，請向組織中的其他人尋求專業知識及知識。

### <a name="get-content-from-smes"></a>從 Sme 取得內容
利用組織中的主題專家 (Sme) ，包括人力資源、支援、銷售、技術及其他重要領域的專家。 當您將其新增為 Microsoft 搜尋編輯者時，sme 可以直接參與內容。 

### <a name="involve-your-users"></a>納入您的使用者
要求使用者建議要加入書籤的資源。 同時要求使用者報告破壞或無效連結等錯誤。

## <a name="set-up-components"></a>設定元件
若要新增或編輯單一或多批 [書簽](manage-bookmarks.md)、 [Q&A](manage-qas.md)和 [位置](manage-locations.md)，請採取下列各節中的步驟。 

### <a name="add-or-edit-a-single-bookmark-qa-or-location-component"></a>新增或編輯單一書簽、Q&A 或位置元件
1. 在 Microsoft 365 系統 [管理中心](https://admin.microsoft.com)，移至 **設定**  >  **Microsoft 搜尋**]。 選取元件的 [名稱] 索引標籤。預設會選取 [ **書簽** ] 索引標籤。
1. 若要新增元件，請選取 [ **新增**]。 
1. 若要編輯元件，請選取相關元件清單中的書簽。 
1. 當您新增或編輯資訊時，預覽會自動更新。

### <a name="bulk-add-or-edit-components"></a>大量新增或編輯元件
使用 [匯 **入** 及 **匯出** 功能]，「搜尋管理員」可以大量建立或編輯 [書簽](manage-bookmarks.md)、 [Q&A](manage-qas.md)] 和 [ [位置](manage-locations.md)]。 當系統管理員想要新增或編輯許多元件時，此功能非常有用。 

匯入及匯出功能可提供下列功能：
- **大量新增**。 在元件的範本檔案中新增詳細資料，然後將其匯入。
- **大量編輯**。 將元件匯出至 CSV 檔案，然後編輯匯出之 CSV 的書簽詳細資料，然後匯入更新後的 CSV。
- **從 [SharePoint](http://sharepoint.com/)匯入已升級的網站**。 此功能僅適用于 [書簽](manage-bookmarks.md)。
- **備份**。 將元件匯出至 CSV 檔案。

若要匯入或匯出元件，請執行下列步驟：
1. 在元件的 [名稱] 索引標籤的右上角，選取 [匯 **入**]。 
1. 若要下載 CSV 檔案中的所有現有元件，請選取 [ **匯出**]。
1. 在右窗格中，選擇要使用 CSV 檔案或從[SharePoint](http://sharepoint.com/)匯入的選項。
1. 若要取得必要欄位及詳細資料的清單，請下載元件的範本檔案。 
1. 新增或編輯範本檔中的元件詳細資料。 然後將它儲存到您的電腦。 
1. 在元件的 [匯 **入** ] 窗格中，選取 **[流覽**]。 然後選取所需的 CSV 檔案，然後選取 [匯 **入**]。

### <a name="template-guidelines"></a>範本指導方針
當您使用範本檔案時，請注意這些指導方針和限制：
- 永遠不要編輯這些欄位中的資料： *識別碼*、 *上次修改* 時間及 *上次修改者*。
- 如果您包括現有書簽的 *識別碼* ，它會被匯入檔案中的資訊所取代。
- 如果現有檔案中有相同標題或 URL 的書簽，則會使用匯入檔案中的資訊更新書簽。
- 不需要範本檔中的所有欄位，必要的欄位也視書簽狀態而異。
- 根據 [ *狀態* ] 欄位，書簽會儲存為 **草稿**、 **建議** 或 **排程**。 否則，會自動發佈它們。
- 如果您管理多個組織，您可以從一個組織匯出書簽，然後將其匯入另一個組織。 但您必須在匯入之前，先移除 [識別碼] 資料行中的資料。

> [!Note]
> 如果範本檔案中有錯誤，便無法匯入元件專案。 若要防止錯誤，請確定您的匯入檔案已正確格式化，且包含所有必要的資訊。

### <a name="prevent-import-errors"></a>防止匯入錯誤

如果任何必要的資料遺失或無效，就會收到錯誤訊息。 記錄檔會產生有關要更正的列和欄的詳細資訊。 進行必要的編輯，然後再次嘗試匯入檔案。 您無法匯入或儲存任何書簽，除非解決所有的錯誤。

若要防止錯誤，請確定您的匯入檔案已正確格式化，且符合這些需求：
- 會包含標題列，以及匯入範本中的所有欄。
- 欄順序與匯入範本相同。
- 所有的欄都有值，但三項可以是空的： *識別碼*、 *上次修改* 時間及 *最後修改者*。 
- [ *狀態* ] 欄不是空白的。

### <a name="titles-and-descriptions"></a>標題和描述
連接的標題和描述可協助使用者判斷結果是否會回應其搜尋查詢。 好的標題和描述反映結果的核心用途。 範例是描述的標題 **Childcare 效益***瞭解有助於支付 Childcare 成本的益處*。 透過此連接的資料，搜尋 **childcare** 的使用者可以找到相關的貨幣支援效益，並取得更多相關資訊的連結。

### <a name="keywords"></a>關鍵字
您組織中的使用者可以使用關鍵字來搜尋及尋找相關的內容。 您必須將關鍵字字詞與其相關的搜尋結果關聯。 Microsoft 搜尋會根據內容的標題及 URL 來建議關鍵字。 若要找出更多關鍵字，請取得下列問題的答案：

1. **哪些搜尋字詞可以找到您識別的資訊？** 請參閱組織中的任何現有的術語，以及相關的變化、縮寫、主題及主題。
1. **人們會利用哪些變化或字詞來討論此資訊？** 請您的支援小組提供這些關鍵字。

例如，如果您建立的結果會連結至送出度假要求的工具，關鍵字 **度假** 和送出 **假期要求** 是包括的好選項。 您組織中的使用者也可能會搜尋假期相關的資訊，以及 **公休日** 或 **下班時間**。 若要讓使用者更輕鬆地找到相關內容，請新增這些關鍵字和其他人，例如「 **提交假日要求** 」和「 **要求下班時間**」。

### <a name="reserved-keywords"></a>保留的關鍵字
 保留的關鍵字是會觸發結果的唯一字詞或片語。 與其他關鍵字不同的是，保留關鍵字只會與一個結果產生關聯。 請盡量不要使用保留的關鍵字，讓 Microsoft Search 能依據使用量進行學習。

例如，網站的書簽可用於提交您的小時數。 [！注意] 如果 **記錄時間** 是保留的關鍵字，則組織中搜尋 **記錄時間** 的使用者，請參閱該網站在 Microsoft 搜尋] 方塊中的唯一書簽。 

### <a name="group-related-content-with-keywords"></a>使用關鍵字群組相關內容
如果您想要使用者在搜尋特定字詞時找到一組相關的內容，請將相同的關鍵字指派給所有相關的內容。 例如，搜尋有關生命狀態變更的程式和工具。 若要將答案組合在一起更新權益、稅務資訊，以及名稱和別名變更，請加入關鍵字（如 **marriage**）。

### <a name="search-settings"></a>搜尋設定
使用搜尋設定，您可以量身定制您的內容，並針對特定使用者群組進行設定。 下列 Microsoft 搜尋設定會控制搜尋結果的顯示方式及可查看的使用者：

- **Date**。 若要控制何時可使用或無法使用內容，請設定開始日期和結束日期。 例如，當時間機密材料相關時，它會出現在搜尋結果中。
- **國家或地區**。 您可以選取國家或地區，所以只有那些位置的使用者可以查看特定內容。 例如，國家/地區特定資訊只會出現在那些國家/地區的搜尋結果中。
- **群組** 設定會使結果僅可供選取之群組的成員使用。 例如，如果您建立僅與 HR 部門員工相關的網站，請將此設定對應至適當的 HR 安全性群組。
- **裝置或作業系統**。 選取裝置類型或作業系統，所以只有搜尋這些裝置或使用這些系統的使用者可以看見該書簽。
- **目標變化**。 此設定會根據使用者的裝置和位置，改變書簽的內容。

## <a name="test-your-content"></a>測試您的內容
在您建立 [書簽](manage-bookmarks.md) 和 [Q&](manage-qas.md)後，請確認下列結果：
- 正確的書簽或 Q&隨即顯示。
- 以關鍵字群組在一起的所有內容都會以計畫的方式一起顯示。
- [搜尋答案] 中未出現任何意外。
- 書簽或 Q&A 具有足夠的資訊。

參與內容建立的使用者和 Sme 可協助測試及驗證搜尋結果。

## <a name="review-and-update-periodically"></a>定期複查和更新
諸如 [書簽](manage-bookmarks.md) 和 [Q&的](manage-qas.md) 權威性資訊，都必須保持新鮮。 定期採取下列步驟：
- 修正或移除中斷和不正確 URLs。
- 移除已不再相關的書簽或 Q&A。
- 檢查工具、網站名稱或小組名稱的變更。
- 請考慮書簽或 Q&A 是否具有權威性，或需要更清晰的描述。

## <a name="get-insights-about-bookmarks-qa-and-locations"></a>深入瞭解書簽、Q&A 和位置

Microsoft 搜尋會顯示發佈、排程或建議的[書簽](manage-bookmarks.md)、 [Q&A](manage-qas.md)和[位置](manage-locations.md)的數目。 [Insights 的儀表板](./usage-reports.md)會顯示書簽、Q&A，以及依狀態的位置總數：

- **已發佈︰** 供使用者使用的已發佈結果數量。
- **已排程：** 發佈管線中的已排程結果數量。
- **已建議：** 使用者的建議數量。

建議的 [書簽](manage-bookmarks.md)、 [Q&A](manage-qas.md)和 [位置](manage-locations.md) 在內容中有很好的間隙指示器。 其可協助您瞭解使用者的外觀，但不會找到。 這種資料可能表示您需要建立更多書簽、Q&A 或位置。 或者，您可能需要使用更好的關鍵字、保留關鍵字和搜尋字串更新現有內容，讓您的內容更容易探索。

### <a name="review-top-search-queries"></a>檢閱熱門搜尋查詢

若要找出最近90天內哪些搜尋產生的印象最高，請複查您的主要搜尋查詢。 「*形象*」是指在搜尋結果中查看頁面的次數。 [Insights 儀表板](./usage-reports.md)上的 **上方查詢** 卡片會顯示每個結果類型的前25位使用者搜尋、搜尋總數，以及透過點擊率 (CTR) 。 使用此報告，您可以識別搜尋查詢量，並決定具有高和低搜尋活動的查詢。

低搜尋計數可能指出使用者不滿。 任何使用者都不會尋找該內容，或是使用不同的關鍵字來尋找。 CTR 會顯示使用者選取提升結果的頻率，以及您的查詢規則和結果如何對使用者有幫助。 [低 CTR] 表示使用者找出內容，但不符合其需求。 在這種情況下，請複查內容。 若要將內容對齊至搜尋查詢，請確定其符合使用者的搜尋和更新標題、描述及關鍵字。 

### <a name="analyze-impressions-by-result-type"></a>依據結果類型分析曝光數

[Insights 儀表板](./usage-reports.md)上的 **印記散佈** 卡中易於讀取的圖形，可在不同的時間範圍顯示印記。 時間軸會顯示結果類型的每日曝光數。 透過這些圖形，您可以決定最常使用或不常使用的結果類型。 不經常使用特定結果類型並不一定表示結果類型不佳。 它只是顯示使用者如何使用搜尋結果。

 如果特定的結果類型是使用者的首選，您可以建立相同類型的更多搜尋結果。 若要確定關鍵字適當，請查看使用低使用狀況的結果類型關鍵字。 您也可以使用此報告，查看使用者行為隨時間變化的變更。