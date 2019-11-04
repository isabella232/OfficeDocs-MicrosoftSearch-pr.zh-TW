---
title: 自訂 Microsoft 搜尋] 頁面
ms.author: anfowler
author: adefowler
manager: shohara
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 加入搜尋類別及自訂搜尋結果
ms.openlocfilehash: 87b394847281e43683f2ed9dfd42d19aa103d3e2
ms.sourcegitcommit: bfcab9d42e93addccd1e3875b41bc9cc1b6986cc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2019
ms.locfileid: "37949684"
---
# <a name="customize-the-microsoft-search-page"></a>自訂 Microsoft 搜尋] 頁面

建立搜尋類別與結果類型您可以自訂當他們中**SharePoint**、 **Office.com**和**Microsoft Search in Bing**搜尋時，向使用者顯示的搜尋結果。 類別，方便使用者尋找他們已取得最新產品權限，請參閱 < 的資訊。  例如，您可以建立搜尋類別行銷分析資料從協力廠商軟體行銷部門中的使用者。 您也可以定義結果類型，並自訂的版面配置，這項資料。  

您可以建立類別和結果類型，這些層級： 

- 組織層級 – 當您在組織層級新增垂直它會出現在搜尋結果頁面當使用者從其 SharePoint 起始頁面搜尋時，在 Office.com 上及 Bing.com。 
- 網站層級 – 例如，您可能想要允許您的客戶來直接從其部門的 SharePoint 網站的 「 嚴重性 1"事件的搜尋服務員工。 

## <a name="whats-a-search-vertical"></a>搜尋類別為何？

Microsoft 的搜尋結果頁面的頂端有一列的索引標籤，這些是搜尋類別。 垂直式搜尋只會顯示結果的特定類型，或是從特定內容，例如唯一的檔案或最新消息。 根據預設 Microsoft Search 顯示類別全部的人員，檔案、 網站及最新消息。  

您可以新增與您的組織相關的搜尋類別。 這些會出現在 SharePoint、 Office.com 和 Bing Microsoft 搜尋結果頁面上。  例如，您可以建立一個行銷相關內容的垂直與另一個銷售，根據每個群組會想要有的資訊類型。 您可以新增類別以顯示結果只從透過連接器編製索引的內容。  

**免責聲明：** 類別和結果類型是目前正在預覽 Microsoft 連接器預覽的一部分。 您無法建立內容位於 sharepoint 或從檔案共用連接器所編製索引的內容之間的垂直。 若要深入了解預覽，請參閱[連接器預覽](connectors-preview.md)。 若要參與預覽，您必須先將提交[Microsoft Graph 連接器預覽註冊表單](https://forms.office.com/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbRxWYgu82J_RFnMMATAS6_chUNVYwNU1CMDNZUDBSSDZKWVo2RDJDRjRLQi4u)。

## <a name="things-to-consider"></a>若要考慮的事項...]

在您開始之前，請確定已編製索引連接器。 可能需要多達 48 小時，根據檔案大小。

您無法建立內容位於 sharepoint 或從檔案共用連接器所編製索引的內容之間的垂直。 了解如何編製索引內容 （連接器文件的連結）。

概括來說，有三個主要步驟新增垂直。 

1. 建立垂直 – 您會在此步驟中定義的類別名稱、 內容來源及要搜尋的內容的範圍。 
2. 定義此類別的結果看起來像。  
3. 啟用 （若要顯示） 從 [類別] 清單] 頁面上的類別。   

## <a name="step-1-create-the-search-vertical"></a>步驟 1： 建立搜尋類別

一旦您啟動精靈，將引導您定義的類別名稱、 內容來源和範圍的內容，它會搜尋的步驟。 垂直會建立在停用狀態。 您將稍後啟用垂直。

您可以使用一組有限的[關鍵字查詢語言 (KQL)](https://docs.microsoft.com/sharepoint/dev/general-development/keyword-query-language-kql-syntax-reference)來縮小範圍，以及頁面上顯示列出您可以使用的屬性。 建議您針對建立 KQL 布林運算子與使用免費的文字關鍵字和屬性限制 

### <a name="create-a-vertical-at-the-organization-level"></a>在組織層級建立類別

若要在 SharePoint 中的 Microsoft Search 的垂直建立首頁，Bing 或 Office.com，請遵循下列步驟：

1. 在 Microsoft 365 系統管理中心中移至 [ **設定** > **Microsoft Search** > **類別**。
1. 選取 [ **新增**若要開始。  

### <a name="create-a-vertical-at-the-site-level"></a>在網站層級建立類別

1. 在您要建立垂直 SharePoint 網站] 移至 [**設定**。
1. 選取 [**站台資訊**，然後**檢視所有網站設定**]。
1. 尋找 [ **Microsoft 搜尋**] 區段，然後選取 [**此網站集合設定 Microsoft Search**。
1. 在功能窗格中，移至 **自訂體驗**，，然後選取 [**類別**] 索引標籤。
1. 若要新增的類別，選取 [ **新增**。 <br>
OR <br>若要編輯類別，請在清單中選取。

請記住，類別建立在停用狀態。 您仍然需要啟用這些使用者可以瀏覽類別之前。

## <a name="step-2-create-the-result-types"></a>步驟 2： 建立結果類型

您可以定義結果的顯示方式垂直向內所設計使用結果類型的版面配置。 結果版面配置可讓您直接在搜尋結果中，顯示重要的資訊，讓使用者不需要按一下 [若要查看是否他們已找到他們要尋找的每個搜尋結果]。

搜尋「結果類型」是一種規則，可讓不同類型的搜尋結果以不同方式顯示。其由下列項目組成：

- 若要比較，針對每個搜尋結果，例如搜尋結果的內容來源的*一個或多個條件*。  
- 使用 [搜尋結果符合條件的*結果版面配置*。 結果版面配置會控制所有符合條件的結果會出現和搜尋結果頁面上的行為的方式。

**您必須建立至少一個結果型別上垂直顯示結果。** 您可以建立的每個類別的多個結果類型，這可讓您可以使用不同的版面配置的不同類型的結果。 例如，您可以自訂 「 嚴重性 1 」 事件，讓更重要的色彩，而較大的字型相較於 「 嚴重性 3 」 事件。 

 一旦您啟動精靈，將會引導您定義的名稱、 內容來源及條件的結果類型的步驟。 您可以定義結果類型，從清單檢視的優先順序。 
  
### <a name="create-a-result-type-at-the-organization-level"></a>在組織層級建立結果類型

1. 在 Microsoft 365 系統管理中心中，前往 [**設定** > **Microsoft Search**，，然後選取 [**輸入的結果**。
1. 若要新增**結果類型**，選取 [ **新增**。 若要編輯的結果類型，請在相關的清單中選取結果類型。
 
### <a name="create-a-results-type-at-the-site-level"></a>網站層級建立結果類型

1. 在 SharePoint 網站上您要建立結果類型，請移至**設定**。
1. 選取 [**站台資訊**，然後**檢視所有網站設定**]。 
1. 尋找 [Microsoft 搜尋] 區段，然後選取 [**此網站集合設定 Microsoft Search**。
1. 在功能窗格中，移至 **自訂體驗**，，然後選取結果類型] 索引標籤。
1. 若要新增結果類型，選取 [ **新增]**。 <br> OR <br>若要編輯的結果類型，請在清單中選取結果類型。

### <a name="view-the-vertical-after-enabling"></a>檢視在啟用之後的類別

啟用垂直之後，它可能需要一段時間，才可以檢視。
如果您想要等候啟用它之後，您可以將附加*cacheClear = true*中立即檢視垂直的 [SharePoint 和 Office.com 的 url。

## <a name="troubleshooting"></a>疑難排解

以下是您可能會遇到的常見問題和修正它們的動作清單。


|Error  |動作  |
|---------|---------|
|在垂直上看到 '發生錯誤' 時發生錯誤|   這兩個類別和結果類型所需完成安裝。 請確定您已建立兩個相同的內容來源。      |
|為什麼我看我結果版面配置雖然已建立一個？ | 花幾分鐘的結果類型]，以用於為這些設定通常會快取。 等候幾分鐘，然後再試一次        |
|我看不到任何內容來源上垂直或結果類型] 頁面     |      請確定您已設定連接器和編製索引的資料   |



## <a name="next-steps"></a>後續步驟
[步驟 3： 自訂結果版面配置](customize-results-layout.md)
