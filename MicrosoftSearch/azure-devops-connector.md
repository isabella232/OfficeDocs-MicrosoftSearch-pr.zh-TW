---
title: Microsoft 搜尋的 Azure DevOps 圖形連接器
ms.author: mecampos
author: mecampos
manager: umas
audience: Admin
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 設定 Microsoft 搜尋的 Azure DevOps 圖形連接器
ms.openlocfilehash: 9307aabbf5ea1565e083abfefb90c590d356ae58
ms.sourcegitcommit: f76ade4c8fed0fee9c36d067b3ca8288c6c980aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "50508858"
---
<!---Previous ms.author: shgrover --->

# <a name="azure-devops-graph-connector-preview"></a>Azure DevOps Graph connector (preview) 

Azure DevOps Graph 連接器可讓您的組織為其 Azure DevOps 服務實例中的工作專案編制索引。 當您從 Azure DevOps 設定連接器和索引內容之後，使用者就可以在 Microsoft 搜尋中搜尋這些專案。

> [!NOTE]
> 請閱讀 [**您的圖形連接器**](configure-connector.md) 文章的設定，以瞭解一般圖表連接器設定指示。

本文適用于設定、執行及監視 Azure DevOps Graph 連接器的任何人。 它會補充一般設定程式，並顯示只適用于 Azure DevOps Graph 連接器的指示。

>[!IMPORTANT]
>Azure DevOps 連接器只支援 Azure DevOps 雲端服務。 Azure DevOps Server 2019，tfs 2018，tfs 2017，tfs 2015，及 TFS 2013 都不受此連接器支援。

<!---## Before you get started-->

<!---Insert "Before you get started" recommendations for this data source-->

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a>步驟1：在 Microsoft 365 系統管理中心新增圖表連接器

遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup 
instructions.-->

## <a name="step-2-name-the-connection"></a>步驟2：命名連線

遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup 
instructions.-->

## <a name="step-3-configure-the-connection-settings"></a>步驟3：設定連接設定

若要連線至 Azure DevOps 實例，您需要 Azure DevOps [組織](https://docs.microsoft.com/azure/devops/organizations/accounts/create-organization) 名稱、其應用程式識別碼，以及 OAuth 驗證的用戶端密碼。

### <a name="register-an-app"></a>註冊應用程式

在 Azure DevOps 中註冊應用程式，以便 Microsoft 搜尋應用程式可以存取實例。 若要深入瞭解，請參閱 Azure DevOps 檔，以瞭解如何 [註冊應用程式](https://docs.microsoft.com/azure/devops/integrate/get-started/authentication/oauth?view=azure-devops#register-your-app&preserve-view=true)。

下表提供如何填寫 [應用程式註冊] 表單的指導方針：

必要欄位 | 描述 | 建議值
--- | --- | ---
| 公司名稱         | 您公司的名稱。 | 使用適當的值   |
| 應用程式名稱     | 識別您要授權之應用程式的唯一值。    | Microsoft 搜尋     |
| 應用程式網站  | 在連接器設定期間要求存取 Azure DevOps 實例之應用程式的 URL。  (必要) 。  | HTTPs://<span>gc。</span>com
| 授權回撥 URL        | 授權伺服器重新導向所需的回撥 URL。 | HTTPs://<span>gc。</span>com/v 1.0/admin/oauth/callback|
| 授權範圍 | 應用程式的存取範圍 | 選取下列範圍： Identity (讀取) 、工作專案 (讀取) 、變數群組 (讀取) 、專案和團隊 (讀取) 、圖形 (讀取) |

在註冊具有上述詳細資料的應用程式時，您會取得將用來設定連接器的 **應用程式識別碼** 和 **用戶端密碼** 。

>[!NOTE]
>若要撤銷對 Azure DevOps 中註冊的任何應用程式的存取權，請移至 Azure DevOps 實例右邊的 [使用者設定]。 選取 [設定檔]，然後選取側邊窗格的 [安全性] 區段中的 [授權]。 將游標移到授權的 OAuth 應用程式上，以查看應用程式詳細資料右下角的 [撤銷] 按鈕。

### <a name="connection-settings"></a>連接設定

在使用 Azure DevOps 註冊 Microsoft Search 應用程式之後，您可以完成 [連線設定] 步驟。 輸入您的組織名稱、應用程式識別碼和用戶端密碼。

![連接應用程式設定](media/ADO_Connection_settings_2.png)

### <a name="configure-data-select-projects-and-fields"></a>設定資料：選取專案和欄位

您可以選擇建立整個組織或特定專案之索引的連線。

如果您選擇編制整個組織的索引，組織中所有專案中的專案將會獲得索引。 新專案和專案會在建立後的下一個編目期間編制索引。

如果您選擇個別專案，則只有那些專案中的工作專案將會編制索引。

![設定資料](media/ADO_Configure_data.png)

接下來，選取您要連線索引及預覽這些欄位中資料的欄位，然後再繼續進行。

![選擇屬性](media/ADO_choose_properties.png)

## <a name="step-4-manage-search-permissions"></a>步驟4：管理搜尋許可權

Azure DevOps 連接器只支援可供  **存取此資料來源** 或 **所有人** 的使用者看到的搜尋許可權。 如果您選擇 [ **只有可存取此資料來源的人員**]，針對 Azure DevOps 中組織、專案或區域路徑層級的使用者或群組的許可權，針對其存取權的使用者，將會在搜尋結果中顯示索引的資料。 如果您選擇 [ **任何人**]，索引資料將會出現在所有使用者的搜尋結果中。

## <a name="step-5-assign-property-labels"></a>步驟5：指派屬性標籤

遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。

## <a name="step-6-manage-schema"></a>步驟6：管理架構

遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。

## <a name="step-7-choose-refresh-settings"></a>步驟7：選擇重新整理設定

Azure DevOps 連接器支援完整和累加編目的更新排程。
建議的排程為一小時用於增量編目，而一天則是完整編目。

## <a name="step-8-review-connection"></a>步驟8：檢查連線

遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup 
instructions.-->

<!---## Troubleshooting-->
<!---Insert troubleshooting recommendations for this data source-->

<!---## Limitations-->
<!---Insert limitations for this data source-->
