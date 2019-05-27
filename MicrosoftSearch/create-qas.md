---
title: 建立問與答
ms.author: dawholl
author: dawholl
manager: kellis
ms.date: 12/18/2018
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Priority
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: d432b9d9-3792-47a0-9a13-30a1a83caabc
description: 建立 Microsoft Search 工作結果常見問題集解答的方式
ms.openlocfilehash: c8244cce58615fdffb1988ffd351b991f16d3042
ms.sourcegitcommit: 3e91a6e70b48a0100adfed1b62ba79f2fd1735d2
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/13/2019
ms.locfileid: "34425680"
---
# <a name="create-qas"></a>建立問與答

> [!IMPORTANT]
> Bing 中的 Microsoft Search 設定現在可在 Microsoft 365 系統管理中心取得。 從在系統管理中心[指派搜尋系統管理員](https://docs.microsoft.com/zh-TW/microsoftsearch/setup-microsoft-search#step-2-assign-search-admin-and-search-editor)開始。
    
問與答提供答案或資訊給使用者，包括選擇性的連結。 在理想情況下，問與答會包括使用者正在尋找的所有詳細資料，因此使用者不需要前往來源。 您可以格式化問與答內容，並且放入影像、清單和表格。
  
## <a name="create-a-qa"></a>建立問與答

如需建立有效的標題、描述、關鍵字和更多項目的資訊，請參閱[規劃內容](plan-your-content.md)。
  
1. 移至 Microsoft Search 系統管理入口網站
    
2. 在瀏覽窗格中，按一下 [問與答]****
    
3. 按一下頁面頂端的 [新增問與答]****
    
    [編輯問與答] 頁面會隨即出現，並顯示問與答在 Bing 上的外觀預覽。 預覽會隨著您輸入的所需資訊而自動更新。
    
4. 輸入**標題**
    
    標題為出現在結果中的標題。 長度最多可達 120 個字元，所以我們建議您使用問題形式。
    
5. 如必要，請輸入頁面、網站或書籤連結位置的 **URL** 
    
    這可讓需要額外資訊的使用者輕鬆取得可深入閱讀的資源。
    
6. 輸入**解答描述**
    
    這應該能回答標題中提出的問題。 您可以將現有的 HTML 內容複製並貼在此處。 將忽略任何不受支援的標記。
    
7. 使用 HTML 標籤和內建選項來設定文字格式、新增影像、清單、表格等
    
    使用頁面頂端的預覽，查看您的標籤和格式設定將在 Bing 上的顯示情況。 如需以下項目的相關資訊：
    
  - HTML 標籤，請參閱以下支援的 HTML 標記清單
    
  - 內建選項，請按一下 [Markdown 指南]**** (問號圖示) 
    
8. 輸入您想觸發該問與答的**關鍵字** 
    
    就像書籤一樣，當使用者搜尋任何您輸入的關鍵字時，該問與答便會納入使用者的工作結果中。 盡量嘗試新增多種可能的關鍵字，包括該題問與答的標題。
    
9. 選取 [自動符合相似的關鍵字]**** 以展開您的關鍵字集 
    
    這可以納入符合範圍更廣的搜尋字詞，並進一步確保問與答出現在相關的工作結果中。
    
10. 輸入**保留的關鍵字**
    
    如果有關鍵字觸發多個問與答，Microsoft Search 會將最熱門的那一題顯示在最上方，其他則顯示為相關連結。 使用一或多個保留關鍵字以確保問與答永遠都會顯示為最上方的結果。 保留的關鍵字不能在問與答之間共用。 此外，我們不建議在問與答和書籤之間共用保留的關鍵字。 如果書籤和問與答共用關鍵字或保留關鍵字，系統永遠都會以書籤為優先，而問與答則不會出現。
    
## <a name="add-qa-settings"></a>新增問與答設定

問與答設定可針對問與答的顯示時間與誰能看到它提供額外控制。
  
- 日期
    
    設定開始日期，以及選用的結束日期，以控制問與答的發佈與過期時間。
    
- 國家/地區
    
    如果您選取國家/地區，那只有位於這些地方的使用者能看到該問與答。
    
- 群組
    
    使用 [群組] 設定以將問與答結果設定為只有所選群組的成員才能看到。 例如，如果您正在建立的問與答僅和 HR 部門中的員工有關，您可以將此設定對應至適當的 HR 安全性群組。
    
- 裝置與作業系統
    
    如果您選取了裝置類型或作業系統，只有在這些裝置上搜尋的使用者，或是使用這些系統的使用者，才能看到該問與答。
    
- 目標變化
    
    使用這項設定可讓您根據使用者的裝置和位置改變問與答內容。
    
## <a name="use-a-browser-extension-to-create-content"></a>使用瀏覽器擴充功能來建立內容

從系統管理入口網站的 [工具] 區段中，下載並安裝適合 Microsoft Edge 或 Chrome 的內容建立者瀏覽器擴充功能。 若要使用該擴充功能，請登入並移至您想要新增為問與答的網站或頁面。 檢閱並變更建議的內容 (包括關鍵字)，變更任何額外的內容，然後儲存問與答。
  
如果找到多題問與答，請檢閱每一題，並決定您想要發佈、儲存成草稿或全部儲存為草稿。
  
## <a name="supported-html-tags"></a>支援的 HTML 標記

您可以使用現有的 HTML 內容或新增 HTML 標籤至您的解答描述。 會忽略不支援的標籤。
  
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

  

