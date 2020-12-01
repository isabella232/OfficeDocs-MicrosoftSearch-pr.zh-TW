---
title: 連接器結果叢集
ms.author: manusi
author: manusi
manager: ruppala
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 連接器結果聚簇體驗的詳細資料
ms.openlocfilehash: fa6ac2dc720ed43e40454b952526734accd45ea4
ms.sourcegitcommit: a328b9764abf5cd0c1c0a8c7def0c6e334da9a1d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/30/2020
ms.locfileid: "49477111"
---
# <a name="graph-connectors-result-cluster"></a>圖形連接器產生的聚簇

## <a name="overview-of-the-graph-connectors-result-cluster-preview"></a>圖形連接器結果叢集 (預覽的概述)   

透過圖形連接器的結果聚簇，企業可以在其預設視圖中搜尋協力廠商資料來源的內容，SharePoint 和 Office.com 中的 [全部] 索引標籤)  (。

結果聚簇可協助使用者探索所有協力廠商內容 (previoulsy 系結至單一連接器和垂直) 一個位置。 結果叢集中顯示的結果會根據租使用者管理員在搜尋類別中的設定方式，將其組合在一起。  

## <a name="how-connector-results-are-selected-and-displayed"></a>選取及顯示連接器結果的方式

結果叢集中所提供的連接器結果是衍生自個別的搜尋行業及連接器內容。 每個搜尋類別都會提供一組相關的結果，這些結果會變成候選結果叢集。 根據每個專案的「title」屬性、結果程式碼片段和內容元件來選擇相關的結果。

為了確保從搜尋縱向探索內容，我們建議您為專案提供有意義的標題。 這會影響結果叢集候選項的仲裁，以及您在結果叢集中顯示內容的可能性。 例如，除非您的使用者使用 IDs 尋找內容，否則請避免使用 IDs 做為屬性 "title" 的值。

結果叢集顯示的頻率會因因素而異，例如您設定的搜尋縱向的數目和內容類型。 透過選取或忽略結果叢集結果，您將會隱含地提供提示，以調整結果叢集在一段時間內的觸發。

結果叢集中所顯示之連接器專案的搜尋結果經驗是由系統產生，不會使用自訂的結果版面配置。 如果您想要在結果叢集中顯示結果，您必須在連線註冊期間宣告 "title" 屬性和專案內容。

## <a name="enable-result-clusters"></a>啟用結果聚簇
  
預設會關閉結果叢集體驗功能。  

請遵循下列步驟，在組織層級開啟體驗：

1. 在 [Microsoft 365 系統管理中心](https://admin.microsoft.com/)中，移至 [**設定**]  >  **搜尋 & 情報**  >  **自訂**  >  **縱向**。  
2. 選取 [ **所有** 垂直]，然後啟用 [ **顯示連接器結果**]。 


請遵循下列步驟，在網站層級開啟體驗：

1. 在您想要進行結果叢集體驗的 SharePoint 網站上，移至 [ **設定**]。
2. 移至 **網站資訊** > **查看所有網站設定**。
3. 移至 [Microsoft 搜尋] 區段，然後選取 [ **設定此網站集合的 Microsoft search**]。
4. 在功能窗格中，移至 [ **自訂經驗**]，然後選取 [ **縱向**]。
5. 選取 [ **所有** 垂直]，然後啟用 [ **顯示連接器結果**]。

## <a name="view-the-result-cluster-experience-after-it-is-enabled"></a>在啟用結果叢集體驗後查看

在您開啟結果叢集體驗後，可能需要幾分鐘的時間才能進行查看。 如果您想要立即體驗，您可以在 SharePoint 和 Office 的 URL 中附加 *cacheClear = true* 。
