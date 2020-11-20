---
title: Microsoft 搜尋的 Azure DevOps 連接器
ms.author: shgrover
author: shakungrover05
manager: jeffkizn
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 設定 Microsoft 搜尋的 Azure DevOps 連接器
ms.openlocfilehash: b9c566e3e07bfca6d4d25b14915f0160f3928b15
ms.sourcegitcommit: 59cdd3f0f82b7918399bf44d27d9891076090f4f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2020
ms.locfileid: "49367548"
---
# <a name="azure-devops-connector-preview"></a>Azure DevOps connector (preview) 

透過 Azure DevOps connector，您的組織可以在其 Azure DevOps 服務實例中編制工作專案的索引。 當您從 Azure DevOps 設定連接器和索引內容之後，使用者就可以在 Microsoft 搜尋中搜尋這些專案。

本文適用于 Microsoft 365 系統管理員或任何設定、執行及監視 Azure DevOps 連接器的人員。 它說明如何設定連接器和連接器功能、限制及疑難排解技術。

>[!IMPORTANT]
>Azure DevOps 連接器只支援 Azure DevOps 雲端服務。 Azure DevOps Server 2019，tfs 2018，tfs 2017，tfs 2015，及 TFS 2013 都不受此連接器支援。 

## <a name="connect-to-a-data-source"></a>連接到資料來源

若要連線至 Azure DevOps 實例，您需要 Azure DevOps [組織](https://docs.microsoft.com/azure/devops/organizations/accounts/create-organization) 名稱、其應用程式識別碼，以及 OAuth 驗證的用戶端密碼。

### <a name="register-an-app"></a>註冊應用程式

您必須在 Azure DevOps 中註冊應用程式，Microsoft 搜尋應用程式才能存取實例。 若要深入瞭解，請參閱 Azure DevOps 檔，以瞭解如何 [註冊應用程式](https://docs.microsoft.com/azure/devops/integrate/get-started/authentication/oauth?view=azure-devops#register-your-app)。 

下表提供如何填寫 [應用程式註冊] 表單的指導方針：

 **必要欄位** | **描述**      | **建議值** 
--- | --- | --- 
| 公司名稱         | 這是您公司的名稱。 | 使用適當的值   | 
| 應用程式名稱     | 此唯一值可識別您要授權的應用程式。    | Microsoft 搜尋     | 
| 應用程式網站  | 此必要欄位是在連接器設定期間要求存取 Azure DevOps 實例之應用程式的 URL。  | <https://gcs.office.com/>                | 
| 授權回撥 URL        | 授權伺服器重新導向所需的回撥 URL。 | <https://gcs.office.com/v1.0/admin/oauth/callback>| 
| 授權範圍 | 這是應用程式的存取範圍 | 選取下列範圍： Identity (讀取) 、工作專案 (讀取) 、變數群組 (讀取) 、專案和團隊 (讀取) 、圖形 (讀取) | 

在註冊具有上述詳細資料的應用程式時，您會取得將用來設定連接器的 **應用程式識別碼** 和 **用戶端密碼** 。

>[!NOTE]
>若要撤銷對 Azure DevOps 中註冊的任何應用程式的存取權，請移至 Azure DevOps 實例右邊的 [使用者設定]。 按一下 [設定檔]，然後按一下側邊窗格 [安全性] 區段中的 [授權]。 將游標移到授權的 OAuth 應用程式上，以查看應用程式詳細資料右下角的 [撤銷] 按鈕。

### <a name="connection-settings"></a>連接設定

在使用 Azure DevOps 註冊 Microsoft Search 應用程式之後，您可以完成 [連線設定] 步驟。 輸入您的組織名稱、應用程式識別碼和用戶端密碼。

![連接應用程式設定](media/ADO_Connection_settings_2.png)

## <a name="select-projects-and-fields"></a>選取專案和欄位

您可以選擇建立整個組織或特定專案之索引的連線。

如果您選擇編制整個組織的索引，組織中所有專案中的專案將會獲得索引。 新專案和專案會在建立後的下一個編目期間編制索引。 如果您選擇個別專案，則只有那些專案中的工作專案將會編制索引。

![設定資料](media/ADO_Configure_data.png)

接下來，選取您要連線索引及預覽這些欄位中資料的欄位，然後再繼續進行。

![選擇屬性](media/ADO_choose_properties.png)

## <a name="manage-search-permissions"></a>管理搜尋許可權

Azure DevOps 連接器只支援可供  **存取此資料來源** 或 **所有人** 的使用者看到的搜尋許可權。 如果您選擇 [ **只有可存取此資料來源的人員**]，針對 Azure DevOps 中組織、專案或區域路徑層級的使用者或群組的許可權，針對其存取權的使用者，將會在搜尋結果中顯示索引的資料。 如果您選擇 [ **任何人**]，索引資料將會出現在所有使用者的搜尋結果中。

## <a name="assign-property-labels"></a>指派屬性標籤

您可以從選項的功能表中選擇，將 source 屬性指派給每個標籤。 雖然這個步驟不是必要的，但具有一些屬性標籤會提升搜尋相關性，並可確保使用者更準確的搜尋結果。

## <a name="manage-schema"></a>管理架構

在 [**管理架構**] 畫面上，您可以選擇變更架構屬性 (可 **查詢**、**可搜尋、可****檢索** 及 **可精簡搜尋**) 相關聯的屬性、新增選用的別名，然後選擇 **Content** 屬性。

## <a name="set-the-refresh-schedule"></a>設定重新整理排程

Azure DevOps 連接器支援完整和累加編目的更新排程。 完整編目會找到先前同步處理至 Microsoft 搜尋索引的已刪除工作專案。 會執行完整編目，以同步處理所有工作專案。 若要將新的工作專案和更新同步到現有的工作專案，您必須排程累加編目。

建議的排程為一小時用於增量編目，而一天則是完整編目。 