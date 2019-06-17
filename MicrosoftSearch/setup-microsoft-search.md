---
title: 設定 **Microsoft Search**
ms.author: anfowler
author: adefowler
manager: mnirkhe
ms.date: 05/30/2019
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Priority
search.appverid:
- BFB160
- MET150
- MOE150
description: 第一次設定 Microsoft Search。
ms.openlocfilehash: c95cc0d11d60e3d4d9a509dc691c01858ede7262
ms.sourcegitcommit: 9df9b1a5f83c9fbe62900df183bee239a8ea6d91
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/14/2019
ms.locfileid: "34947741"
---
# <a name="set-up-microsoft-search"></a>設定 Microsoft Search

**Microsoft Search** 透過安全地存取所有資料來源，包括電子郵件、檔案、SharePoint 檔案、OneDrive 內容和其他共用資源，以及使用者組織中的網際網路，提供對使用者友善的介面，協助使用者尋找資訊，例如檔案和文件、內部網站和商務工具、人員和群組、位置和方向、交談和解答。

若要深入了解 **Microsoft Search** 功能，請參閱 [Microsoft Search 概觀](overview-microsoft-search.md)。

## <a name="get-started"></a>開始使用

**Microsoft Search** 預設會對支援它的所有 Microsoft 應用程式開啟，成為 Microsoft 365 的一部分。 使用者只需使用公司或學校帳戶登入，並使用將 Bing 設為預設搜尋提供者的瀏覽器。

您會透過 **Microsoft 365 系統管理中心**管理 **Microsoft Search**。 使用系統管理員認證登入，然後從 Office 365 應用程式清單中選取 [系統管理員]**** 磚 (按一下應用程式清單左下角的 [應用程式啟動器]**** 圖示)。 在 [Microsoft 365 系統管理中心]****，於左側導覽面板的 [設定]**** 下選取 [Microsoft Search]****。 

**附註：** 如果您在 [Microsoft 365 系統管理員中心]**** 的 [設定]**** 下看「不」到 **Microsoft Search**，請開啟系統管理中心右上角的 [嘗試預覽版]**** 切換。 

身為系統管理員，您應該考慮可讓 **Microsoft Search** 體驗更有效且對組織中的使用者更友善的幾個事項。

## <a name="step-1-check-access-level-of-your-users"></a>步驟 1：檢查使用者的存取層級

**Microsoft Search** 會尊重內容來源的安全性設定。 使用者會在他們的搜尋結果中看到的內容取決於其權限和存取層級。 檢閱組織中使用者的存取層級，以確定使用者只會找到他們獲存取的內容。

深入了解[規劃權限](https://docs.microsoft.com/zh-TW/sharepoint/plan-your-permissions-strategy)與[建立權限層級](https://docs.microsoft.com/zh-TW/sharepoint/how-to-create-and-edit-permission-levels)。

## <a name="step-2-assign-search-admin-and-search-editor"></a>步驟 2：指定搜尋系統管理員和搜尋編輯者

**Microsoft 系統管理中心**中有兩個新角色：搜尋系統管理員和搜尋編輯者。  擁有完整權限的全域系統管理員，會指派系統管理員角色給使用者，包括搜尋系統管理員的角色。 搜尋系統管理員可以委派搜尋系統管理員或搜尋編輯者角色給其他使用者。 如需有關不同系統管理員角色的詳細資訊，請參閱[關於 Office 365 系統管理員角色](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles?view=o365-worldwide)。

**附註：** 搜尋系統管理員和搜尋編輯者這兩個新角色僅可在 **Microsoft 365 系統管理中心**取得，無法在舊版系統管理入口網站中取得。 

搜尋系統管理員會直接影響使用者的搜尋體驗。 這包括選擇想要呈現給使用者的結果類型。 由一個人針對組織中使用者所搜尋的許多不同主題選擇並建立授權內容，可能很困難。 建議您運用 SME 與其他使用者的專業技術與知識 (將他們新增為編輯者)。 

在 **Microsoft Search** 中，您可以使用兩個新角色來管理組織的搜尋設定和內容：
1. **搜尋系統管理員：** 此角色可以建立及管理搜尋結果內容，並定義查詢設定，以改善組織內的搜尋結果。 搜尋系統管理員會管理 **Microsoft Search** 組態並指定建立內容的搜尋編輯者。
2. **搜尋編輯者：** 在 Microsoft 365 系統管理中心中建立、管理並刪除 **Microsoft Search** 的內容。 此角色可以建立及管理編輯性的內容，例如：常見問題集和解答、重要的地點和位置、經常搜尋和使用的網站和應用程式等。不過他們無權管理搜尋設定。

如需指派系統管理員角色，請參閱[在商務用 Office 365 中指派系統管理員權限](https://docs.microsoft.com/zh-TW/office365/admin/add-users/assign-admin-roles?view=o365-worldwide)。

## <a name="step-3-make-content-easy-to-find"></a>步驟 3：讓內容易於尋找 

**Microsoft Search** 為系統管理員提供工具，用來為使用者建立功能強大的搜尋體驗。 在 **Microsoft Search** 中，系統管理員可建立三個不同的搜尋內容，以獲得更佳的搜尋體驗並改善內容的可尋找性：
- **書籤：** 書籤類似 SharePoint 中提升的結果，可協助將使用者查詢的最可能結果提升至搜尋結果的最上方，並讓使用者易於找到重要的內部網站。 
- **問題與解答：** 問題與解答類似於常見問題集，這些通常採用問題和解答格式。 它能提供對於使用者工作相關問題最有可能的答案。
- **位置：** 位置為可協助使用者找到組織的大樓、辦公室、校區的地址。 

您擁有的書籤、問題與解答和位置越多，可以為您的使用者增加的價值和優點越多。 不過，若有太多個，可能會增加後續的管理負荷，因為必須定期檢閱並更新，以將結果保持相關且為最新。

以下是您應該為您的使用者考慮加入書籤的一些內容範例：
- 組織或產品或服務資訊。
- 可供所有人使用的資訊內容；例如，公司的相關資訊、Windows 和 Office 應用程式的說明等。 
- 組織中的人員在日常工作中一般會搜尋的內容。 常見的工作相關搜尋包括員工福利、時間與支出報告、提交訂購單和取得 IT 服務協助等。 

若要建立及管理搜尋內容，請參閱[讓內容易於尋找](make-content-easy-to-find.md)。

## <a name="step-4-test-single-sign-on"></a>步驟 4：測試單一登入
**Microsoft Search** 會使用 Azure Active Directory (AAD) 來驗證和授權對組織資料的存取。  這表示在您登入 Office 365 應用程式或 Windows 10 時，使用者會使用您的公司或學校帳戶自動登入。

我們建議 **Microsoft Search** 使用者使用單一登入，因為它會減少系統提示使用者登入的次數。 系統管理員透過一小群使用者來測試單一登入，以協助找出任何造成阻礙的組態問題。 

針對 Windows 10 上的 Chrome 使用者，必須先安裝適用於 Chrome 的 Windows 10 和 AAD 登入擴充功能，單一登入才能運作。 安裝後，您可以使用 Chrome 擴充功能在登入支援的網站時 (包括 Office 365 和 Bing)，輕鬆地利用 AAD 進行驗證。 此功能僅供獲授權的使用者使用。 

若要下載及安裝適用於 Chrome 的 Windows 10 和 AAD 登入擴充功能，請前往 [Chrome 線上應用程式商店](https://go.microsoft.com/fwlink/?linkid=2090961)。

## <a name="step-5-training-and-communication"></a>步驟 5：訓練與溝通
建立員工可以自行輕鬆存取的自助資源。 這有助於減少您與團隊不斷出現通訊的整體負擔，並協助自我訓練和教育員工。 提供使用者通訊、常見問題集、影片和錄製的訓練或網路研討會。 以下是可以開始的一些實用連結：
- [在 Office 中使用 Microsoft Search 找到所需的內容](https://support.office.com/article/find-what-you-need-with-microsoft-search-in-office-2457d4d8-48a8-4ad4-ab89-5a0657aa8446?ui=en-US&rs=en-US&ad=US)
- [Office 365 訓練中心](https://support.office.com/office-training-center)
- 
  [Microsoft Search Center](https://support.office.com/zh-TW/article/-working-title-microsoft-search-center-b8bf5a2c-7515-40a9-9a6a-b8ed382c86bc?ui=en-US&rs=en-US&ad=US)

## <a name="trying-out-microsoft-search-in-bing"></a>在 Bing 中試用 **Microsoft Search** 
**Microsoft Search** 系統管理員可以在 Bing 中將 **Microsoft Search** 關閉。 如果關閉，使用者在 Bing 搜尋中將看不到組織內容。 依預設，Bing 中會開啟 **Microsoft Search**。 建議您在 Bing 中將 **Microsoft Search** 保持開啟，以獲得更佳的使用者體驗。 

如果您想要在測試租用戶上試用 **Microsoft Search**，或想要在提供給所有使用者使用之前測試搜尋體驗，則可以關閉 **Microsoft Search**。
若要開啟/關閉 **Microsoft Search** 中的 Bing，請移至 [Microsoft 365 系統管理中心]**** 中的 [服務與增益集]****，並將 [Bing 中的 Microsoft Search]**** 開啟/關閉。
