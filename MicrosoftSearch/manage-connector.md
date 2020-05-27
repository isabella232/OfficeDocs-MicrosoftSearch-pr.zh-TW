---
title: 管理 microsoft 搜尋的 Microsoft Graph 連接器
ms.author: mounika.narayanan
author: monaray
manager: mnirkhe
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 管理 microsoft Search 的 Microsoft Graph 連接器。
ms.openlocfilehash: 04e4635a67ea35381b95c1c753a35eb640d655d4
ms.sourcegitcommit: 1524ae5fe97350ce4294d74e381872b5b7a9f645
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/26/2020
ms.locfileid: "44371306"
---
# <a name="manage-your-connector-for-microsoft-search"></a>管理您的 Microsoft 搜尋連接器

若要存取和管理您的連接器，您必須指定為您租使用者的「搜尋管理員」。 請與您的租使用者管理員聯繫，為您提供搜尋系統管理員角色。

## <a name="get-started"></a>開始使用

1. 登入 [Microsoft 365 系統管理中心](https://admin.microsoft.com)。
2. 移至 [**設定**  >  **Microsoft 搜尋**  >  **連接器**]。

針對每個連接器類型， [Microsoft 365 系統管理中心](https://admin.microsoft.com)支援下表所示的作業：

**作業** | **Microsoft 建立的連接器** | **夥伴或自訂建立的連接器**
--- | --- | ---
新增連線 | ： heavy_check_mark：（請參閱[設定您的 Microsoft 建連接器](configure-connector.md)） | ： x：（請參閱合作夥伴或自訂的連接器系統管理員 UX）
刪除連線 | ： heavy_check_mark： | ： heavy_check_mark：
編輯已發佈的連線 | ： heavy_check_mark： Name<br></br> ： heavy_check_mark： Description<br></br> ： heavy_check_mark：外部資料源的驗證認證<br></br> ： heavy_check_mark：內部部署資料來源的閘道認證<br></br> ： heavy_check_mark：重新整理排程<br></br> | ： heavy_check_mark： Name<br></br> ： heavy_check_mark： Description
編輯拔模連接 | ： heavy_check_mark： | 軸

## <a name="monitor-your-connection-status"></a>監視您的線上狀態
在您建立連線後，已處理的專案數目會顯示在 [ **Microsoft 搜尋**] 頁面上的 [**連接器**] 索引標籤上。 在初次完整編目成功完成之後，會顯示定期增加編目的進度。 此頁面提供連接器之日常作業的相關資訊，以及記錄檔及錯誤歷程記錄的概覽。

每個連線會在 [**狀態**] 欄中顯示四個狀態：
* **同步**處理。 連接器會編目來源中的資料，以編制現有專案的索引並進行任何更新。
* **已啟用**：連線已啟用，且沒有對其執行的作用中編目。 **上次同步處理時間**表示上次成功編目的時間。 連線為最新的同步處理時間。
* 已**暫停**。 管理員會透過 pause 選項暫停編目。 下一個編目只會在手動恢復時執行。 不過，來自此連線的資料仍可供搜尋。
* **失敗**。 連接發生嚴重失敗。 此錯誤需要手動干預。 管理員需要根據所顯示的錯誤訊息採取適當的動作。 在發生錯誤之前，已編制索引的資料可供搜尋。

### <a name="monitor-errors"></a>監視錯誤
針對 [**連接器**] 索引標籤上的每個作用中**連接器**，所有的現有編目錯誤都會顯示在 [**錯誤**] 索引卷索引標籤會列出錯誤碼、每個記錄檔的計數，以及錯誤記錄下載選項。 請參閱下列影像中的範例。 選取**錯誤碼**以查看錯誤的詳細資料。

![已選取連接器的連接器清單和詳細資料窗格中顯示此連接器的3個錯誤。](media/errormonitoring1.png)

若要查看錯誤的特定詳細資料，請選取其錯誤碼。 螢幕會顯示錯誤詳細資料和連結。 最近的錯誤會出現在頂端。 請參閱下表中的範例。

![已選取連接器的連接器清單和詳細資料窗格，顯示連接器的錯誤清單。 ](media/errormonitoring2.png)

以下是針對任何連線可能會出現的不同錯誤清單。 如果這些解決方案無法運作，請聯繫我們支援人員或傳送我們（意見反應） [連接器-feedback.md]。 

**錯誤碼** | **錯誤訊息** | **解決方案**
--- | --- | ---
1000 | 無法使用資料來源。 請檢查您的網際網路連線，或確定該連接器仍可存取資料來源。 | 當資料來源由於網路問題或資料來源本身被刪除、移動或重新命名時，便會發生此錯誤。 檢查提供的資料來源詳細資料是否仍然有效。
1001 | 無法更新資料，因為資料來源正在節流連接器。 | 若要 unthrottle 資料來源，請檢查其縮放比例是否可增加，或等到一天中的流量很低的時間。
1002 | 無法使用資料來源進行驗證。 請確認與此資料來源相關聯的認證正確無誤。 | 按一下 [**編輯**] 以更新驗證認證。
1003 | 與連接器關聯的帳戶沒有存取該專案的許可權。 |  確定適當的帳戶有權存取您要編制索引的專案。
1004 | 無法到達內部部署資料閘道。 請確定閘道服務正在執行，且連線設定中已更新閘道詳細資料。 | 使用閘道檢查電腦，開啟 Power BI 閘道應用程式，並確定閘道正在執行。 確認閘道使用的是與 Microsoft 搜尋相同的系統管理員帳戶，然後確定連線設定中所有的閘道詳細資料都已更新。 
1005 | 與此資料來源相關聯的認證已過期。 更新認證並更新連線。 | 按一下 [**編輯**] 以更新驗證認證。 
1006 | 您的閘道版本已過期，且不再支援此連接器。 您將需要更新閘道。 | 請造訪[安裝內部部署資料閘道](https://docs.microsoft.com/data-integration/gateway/service-gateway-install)，以在包含閘道的機器上下載並安裝最新版本的 Power BI 閘道。
1007 | 未偵測到有效的 Power BI 授權。 您需要有效的 Power BI 授權，才能執行這種編目。 | 您需要有效的 Power BI 授權，才能執行這種編目。 檢查您的組織是否具備有效的授權。 如果是的話，請再試一次。 如果不是，請取得授權，然後再試一次。
1008 | 租使用者的配額利用率已達到其限制。 嘗試刪除連線以釋放部分配額，或調整您的攝取篩選器以引入較少的資料。 | 嘗試刪除連線以釋放部分配額，或調整您的攝取篩選器以引入較少的資料。 若未解決問題，請與 Microsoft 支援人員聯繫。
2001 | 因為佇列中的更新數目很多，所以會限制索引。 根據佇列的不同，可能需要一些時間才能完成更新。 | 請稍候，直到佇列清除為止。
2002 | 由於不支援的專案格式設定，索引失敗。 | 如需詳細資訊，請參閱連接器特有的檔。
2003 | 由於不支援的專案內容，索引失敗。 | 如需詳細資訊，請參閱連接器特有的檔。 
2004 | 檔案[大小](https://docs.microsoft.com/microsoftsearch/file-share-connector#content-requirements)太大，無法編制索引。 在處理前，其必須為 100 MB 或以下，且不大於 4 MB。 在此情況下，檔案會部分編制索引。 檔案中的一些片語可能不會傳回搜尋結果。 | 如需詳細資訊，請參閱檔案[共用特定檔](https://docs.microsoft.com/MicrosoftSearch/file-share-connector#content-requirements)。
5000 | 發生錯誤。 若繼續，請與支援人員聯繫。 | 

## <a name="preview-limitations"></a>預覽限制
* 當您**發佈**Microsoft 建立的連接器時，可能需要幾分鐘的時間來建立連線。 在這段時間內，該連線會顯示其狀態為 [擱置中]。 此外，也不會自動重新整理，所以您需要手動重新整理。
* [Microsoft 365 系統管理中心](https://admin.microsoft.com)不支援在發佈連接後，查看及編輯**搜尋架構**。 若要編輯搜尋架構，請刪除連接，然後建立新的連線。
* 當您管理連線的重新整理**排程**時，會顯示在每個會話期間同步處理的專案數。 不過，無法使用同步處理歷程記錄。
