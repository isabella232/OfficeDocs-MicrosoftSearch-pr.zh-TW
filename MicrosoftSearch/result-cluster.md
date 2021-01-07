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
ms.openlocfilehash: f2355213a0b1821968c801153841c274e539d72e
ms.sourcegitcommit: 7294c953e7939e48f128656cc2f8f22705ae3f3d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "49773025"
---
# <a name="graph-connectors-result-cluster"></a>圖形連接器產生的聚簇

## <a name="overview-of-the-graph-connectors-result-cluster-preview"></a>圖形連接器結果叢集 (預覽的概述)   

透過圖形連接器的結果聚簇，企業可以在其預設視圖、[ **全部** ] 索引標籤、SharePoint、Office.com 及 Microsoft Search in Bing 中搜尋協力廠商資料來源的內容。

結果聚簇可協助使用者在一個位置探索所有協力廠商內容。 結果叢集中顯示的結果會根據搜尋類別設定分組在一起。

## <a name="how-connector-results-are-selected-and-displayed"></a>選取及顯示連接器結果的方式

結果叢集中所提供的連接器結果是衍生自個別的搜尋行業及連接器內容。 每個搜尋類別都會提供一組相關的結果，這些結果會變成候選結果叢集。 根據每個專案的「title」屬性和「content」屬性，選取相關的結果。 Content 屬性標示為 *isContent = true* 在架構上。

為了確保從搜尋縱向探索內容，我們建議您為專案提供有意義的標題。 這會影響結果叢集候選項的仲裁，以及您在結果叢集中顯示內容的可能性。 例如，除非您的使用者使用 IDs 尋找內容，否則請避免使用 IDs 做為屬性 "title" 的值。

結果叢集顯示的頻率會因因素而異，例如您設定的搜尋縱向的數目和內容類型。 透過互動或忽略結果叢集，使用者將會以隱含方式提供提示，以調整它隨時間的觸發。

結果叢集中所顯示之連接器專案的搜尋結果體驗使用您所定義的 [結果類型](https://docs.microsoft.com/microsoftsearch/customize-search-page#create-your-own-result-type) 。 如果未設定任何結果類型，則會使用 [系統產生的版面](https://docs.microsoft.com/microsoftsearch/customize-search-page#default-search-result-layout) 配置。 

建議使用 "title" 屬性做為搜尋結果標題，並使用 "content" 屬性做為搜尋描述。 這可透過準確觸發結果叢集和最相關的結果，為您的使用者提供最佳的體驗。 

## <a name="enable-result-clusters"></a>啟用結果聚簇
  
預設會關閉結果叢集體驗功能。  

請遵循下列步驟，在組織層級開啟體驗：

1. 在 [Microsoft 365 系統管理中心](https://admin.microsoft.com)中，移至 [ [**縱向**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/verticals)]。
2. 選取 [ **所有** 垂直]，然後啟用 [ **顯示連接器結果**]。 


請遵循下列步驟，在 SharePoint 網站層級開啟體驗：

1. 在您想要進行結果叢集體驗的 SharePoint 網站上，移至 [ **設定**]。
2. 移至 **網站資訊** > **查看所有網站設定**。
3. 移至 [Microsoft 搜尋] 區段，然後選取 [ **設定此網站集合的 Microsoft search**]。
4. 在功能窗格中，移至 [ **自訂經驗**]，然後選取 [ **縱向**]。
5. 選取 [ **所有** 垂直]，然後啟用 [ **顯示連接器結果**]。

## <a name="view-the-result-cluster-experience-after-it-is-enabled"></a>在啟用結果叢集體驗後查看

在您開啟結果叢集體驗後，可能需要幾分鐘的時間才能進行查看。 如果您想要立即體驗，您可以在 SharePoint 和 Office 的 URL 中附加 *cacheClear = true* 。
