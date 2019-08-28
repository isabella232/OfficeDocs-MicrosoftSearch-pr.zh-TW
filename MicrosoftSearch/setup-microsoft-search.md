---
title: 設定 Microsoft Search
ms.author: anfowler
author: adefowler
manager: mnirkhe
ms.date: 08/06/2019
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Priority
search.appverid:
- BFB160
- MET150
- MOE150
description: 第一次設定 Microsoft Search。
ms.openlocfilehash: 7c80701e83fea7b9b93e4e01f98fd1eeedbfa749
ms.sourcegitcommit: c2c9e66af1038efd2849d578f846680851f9e5d2
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/27/2019
ms.locfileid: "36639496"
---
# <a name="set-up-microsoft-search"></a>設定 Microsoft Search

Microsoft Search 透過安全地存取所有資料來源，包括電子郵件、檔案、SharePoint 檔案、OneDrive 內容和其他共用資源，以及使用者組織中的網際網路，提供對使用者友善的介面，協助使用者尋找資訊，例如檔案和文件、內部網站和商務工具、人員和群組、位置和方向、交談和解答。

若要深入了解 Microsoft Search 功能，請參閱 [Microsoft Search 概觀](overview-microsoft-search.md)。

## <a name="get-started"></a>開始使用

Microsoft Search 預設會對支援它的所有 Microsoft 應用程式開啟，成為 Microsoft 365 的一部分。 使用者只需使用公司或學校帳戶登入，並使用將 Bing 設為預設搜尋提供者的瀏覽器。

您可透過 Microsoft 365 系統管理中心來管理 Microsoft Search。

1. 在 Microsoft 365 系統管理中心內，移至 [設定]**** > [Microsoft]****。

**附註：** 如果您在 [設定]**** 下「未」看到 Microsoft Search，請開啟任何系統管理中心頁面右上角的 [嘗試預覽版]**** 開關。

身為系統管理員，請考慮幾個可讓 Microsoft Search 體驗更有效且對組織使用者更友善的事項。

## <a name="step-1-check-access-level-of-your-users"></a>步驟 1：檢查使用者的存取層級

Microsoft Search 會採用內容來源的安全性設定。 使用者會在搜尋結果中看到的內容取決於其權限和存取層級。 檢閱組織中使用者的存取層級，以確定使用者只會找到他們獲存取的內容。

| Service         | 描述                                                                                                                                                                                                                                         |
| --------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 群組          | [在群組中新增或移除成員](https://docs.microsoft.com/office365/admin/create-groups/add-or-remove-members-from-groups)                                                                                                                     |
| 人員          | 您可以使用 [Set-User](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/set-user) Cmdlet 將 `HiddenFromAddressListEnabled` 參數設定為 `true`，來防止系統搜尋通訊清單中的特定使用者。 |
| Microsoft Teams | [管理使用者對 Microsoft Teams 的存取](https://docs.microsoft.com/microsoftteams/user-access)                                                                                                                                                      |
| OneDrive        | [管理共用](https://docs.microsoft.com/OneDrive/manage-sharing)                                                                                                                                                                                |
| SharePoint      | 
  [規劃權限](https://docs.microsoft.com/zh-TW/sharepoint/plan-your-permissions-strategy)<br> 
  [建立權限等級](https://docs.microsoft.com/zh-TW/sharepoint/how-to-create-and-edit-permission-levels)                          |
| OneNote         | 您無法在內嵌於 OneNote 的檔案上進行搜尋。 [在 OneDrive 上變更筆記本的權限](https://support.office.com/article/B9600CCF-045A-40E6-9913-4A7EB02869A5)                                                                    |
| Yammer          | [Yammer 安全性設定](https://docs.microsoft.com/Yammer/manage-security-and-compliance/yammer-security-settings)                                                                                                                               |

## <a name="step-2-assign-search-admin-and-search-editor"></a>步驟 2：指派搜尋系統管理員和搜尋編輯者

在 Microsoft Search 中，您可以藉由將這兩個角色指派給使用者來管理組織的搜尋設定和內容：

1. **搜尋系統管理員：** 此角色可以建立及管理搜尋結果內容，並定義查詢設定，以改善組織內的搜尋結果。 搜尋系統管理員負責管理 Microsoft Search 組態，並可執行搜尋編輯者所能執行的所有內容管理工作。
2. **搜尋編輯者：** 在 Microsoft 365 系統管理中心中建立、管理和刪除 Microsoft Search 的內容。 此角色可以建立及管理編輯性的內容，例如：常見問題集和解答、重要的地點和位置、經常搜尋和使用的網站與應用程式。

目前，搜尋系統管理員和搜尋編輯者角色都必須由全域系統管理員來指派。如需詳細資訊，請參閱[指派系統管理員角色](https://docs.microsoft.com/zh-TW/office365/admin/add-users/assign-admin-roles?view=o365-worldwide)。

搜尋系統管理員會直接影響使用者的搜尋體驗。 這包括選擇想要呈現給使用者的結果類型。 由一個人針對組織中使用者所搜尋的許多不同主題選擇並建立授權內容，可能很困難。 建議您運用主題專家 (SME) 與其他使用者的專業技術與知識 (將他們新增為搜尋編輯者)。

## <a name="step-3-make-content-easy-to-find"></a>步驟 3：讓內容易於尋找

Microsoft Search 會提供工具給系統管理員，讓其用來為使用者建立功能強大的搜尋體驗。 在 Microsoft Search 中，系統管理員可建立三個不同的搜尋內容，以獲得更佳的搜尋體驗並改善內容的可尋找性：

- **書籤：** 書籤類似 SharePoint 中提升的結果，可協助將使用者查詢的最可能結果提升至搜尋結果的最上方，並讓使用者易於找到重要的內部網站。
- **問題與解答：** 問題與解答類似於常見問題集，這些通常採用問題和解答格式。 它能提供對於使用者工作相關問題最有可能的答案。
- **位置：** 位置為可協助使用者找到組織的大樓、辦公室和校區的地址。

您擁有的書籤、問題與解答和位置越多，可以為您的使用者增加的價值和優點越多。 不過，若有太多個，可能會增加後續的管理負荷，因為必須定期檢閱並更新，以將結果保持相關且為最新。

以下是您應該為您的使用者考慮加入書籤的一些內容範例：

- 組織或產品或服務資訊。
- 可供所有人使用的資訊內容；例如，公司的相關資訊、Windows 和 Office 應用程式的說明等。
- 組織中的人員在日常工作中一般會搜尋的內容。 常見的工作相關搜尋包括員工福利、時間與支出報告、提交訂購單和取得 IT 服務協助等。

若要建立及管理搜尋內容，請參閱[讓內容易於尋找](make-content-easy-to-find.md)。

## <a name="step-4-training-and-communication"></a>步驟 4：訓練與溝通

建立員工可以自行輕鬆存取的自助資源。 這有助於減少您與團隊不斷出現通訊的整體負擔，並協助自我訓練和教育員工。 提供使用者通訊、常見問題集、影片和錄製的訓練或網路研討會。 以下是可以開始的一些實用連結：

- [在 Office 中使用 Microsoft Search 找到所需的內容](https://support.office.com/article/find-what-you-need-with-microsoft-search-in-office-2457d4d8-48a8-4ad4-ab89-5a0657aa8446?ui=en-US&rs=en-US&ad=US)
- [Office 365 訓練中心](https://support.office.com/office-training-center)
- 
  [Microsoft 搜尋中心](https://support.office.com/zh-TW/article/-working-title-microsoft-search-center-b8bf5a2c-7515-40a9-9a6a-b8ed382c86bc?ui=en-US&rs=en-US&ad=US)