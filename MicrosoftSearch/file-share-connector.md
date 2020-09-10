---
title: Microsoft 搜尋的檔案共用連接器
ms.author: monaray
author: monaray97
manager: jameslau
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 設定 Microsoft 搜尋的檔案共用連接器。
ms.openlocfilehash: d497e60d7d13749b0ee3cc80a134061ac70407d8
ms.sourcegitcommit: 988c37610e71f9784b486660400aecaa7bed40b0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "47422971"
---
# <a name="file-share-connector"></a>檔共用連接器

您的組織中的使用者可以使用檔案共用連接器，來搜尋內部部署檔案共用。 這些共用的搜尋結果會合並來自 [SharePoint](http://sharepoint.com/) 和 [商務 OneDrive 公司](https://onedrive.live.com/about/business/)的結果。

本文適用于 [Microsoft 365](https://www.microsoft.com/microsoft-365) 系統管理員或任何設定、執行及監視檔案共用連接器的人員。 它說明如何設定連接器和連接器功能、限制及疑難排解技術。

## <a name="install-a-data-gateway"></a>安裝資料閘道
為了存取協力廠商資料，您必須安裝和設定 [Microsoft POWER BI](https://msit.powerbi.com/) 閘道。 請參閱 [安裝內部部署閘道](https://docs.microsoft.com/data-integration/gateway/service-gateway-install) 以深入瞭解。  

## <a name="content-requirements"></a>內容需求
**檔案類型**。 只有這些格式的檔案可以進行索引及搜尋： DOC，.DOCM，.DOCX，點，DOTX，.EML，GIF，HTML，JPEG，.MHT，MHTML，MSG，NWS，OBD，OBT，ODP，ODS，ODT，ONE，PDF，.POT，PPS，PPTM，XLB，XLS，.XLSX，.XLT，.xlc，XML，XPS，和 ZIP。 只會為這些格式的文字內容編制索引。 會忽略所有多媒體內容。
 
**檔案大小限制**。 支援的檔案大小上限為 100 MB。 從索引中略過超過 100 MB 的檔案。 後處理的最大大小限制為 4 MB。 當檔案大小達到 4 MB 時，處理便會停止。 因此，檔案中所提供的部分片語可能無法用於搜尋。

## <a name="connect-to-a-data-source"></a>連接到資料來源
在 [連線 **至資料來源]** 頁面上，選取 [檔案 **共用** ]，並提供名稱、連線識別碼及描述。 在下一個頁面上，提供檔案共用的路徑，然後選取您先前安裝的閘道。 輸入 [Microsoft Windows](https://microsoft.com/windows) 使用者帳戶的認證，該帳戶具有共用中所有檔案的讀取權限。 請移至其餘的設定，併發布連接。

## <a name="set-the-refresh-schedule"></a>設定重新整理排程
建議的預設重新整理排程間隔為15分鐘，但您可以將它變更為您想要的其他間隔。

## <a name="set-up-your-search-results-page"></a>設定您的搜尋結果頁面
若要在 [ **全部** **] 和** [檔案] 索引標籤中顯示不同的檔案連線結果，您必須設定 [SharePoint](http://sharepoint.com/) 的「搜尋引擎結果」頁面：
- [ **All** ] （全部）表格會顯示檔案連線、SharePoint 檔案、 [OneDrive](https://onedrive.live.com/about/business/) 檔案及 SharePoint 網站的合併結果。 
- **檔**會顯示所有來自您的連線、SharePoint 及 OneDrive 的檔案結果。
在 [ **全部** ] 和 [檔案] 的行業 **中，會** 將來自檔連線的結果新增至現有的結果。

若要設定搜尋結果頁面，請執行下列步驟：
1. 使用現代搜尋頁面建立 SharePoint 網站集合。

2. 安裝 [SharePoint 線上管理命令](https://www.microsoft.com/download/details.aspx?id=35588)介面。

3. 以系統管理員身分開啟 SharePoint 線上管理命令介面，然後匯入出現 **Microsoft.SharePoint.Client.dll** 模組 `C:\Windows\Microsoft.NET\assembly\GAC_MSIL\Microsoft.SharePoint.Client\v4.0_16.0.0.0__71e9bce111e9429c\Microsoft.SharePoint.Client.dll` 。

> [!NOTE]
> 所有使用者的此路徑可能並不相同。

若要匯入模組，請在 [SharePoint 線上管理命令](https://www.microsoft.com/download/details.aspx?id=35588)介面中執行下列命令：
```bash
Import-Module "C:\Windows\Microsoft.NET\assembly\GAC_MSIL\Microsoft.SharePoint.Client\v4.0_16.0.0.0__71e9bce111e9429c\Microsoft.SharePoint.Client.dll" 
```

4. 現在執行此腳本：
```bash
$orgName = Read-Host -prompt 'Please enter your org name'
$userName = Read-Host -prompt 'Enter user name'
$userCreds = Get-Credential -UserName $userName -Message "Type the password"
Connect-SPOService -Url https://$orgName-admin.sharepoint.com -Credential $userCreds

$url = Read-Host -Prompt 'Please enter the site url'
$site = Get-SPOSite -Identity $url
Set-SPOSite $url -DenyAddAndCustomizePages 0

$pwd = Read-Host -AsSecureString 'type the password'
$context = New-Object Microsoft.SharePoint.Client.ClientContext($url)
$credential = New-Object Microsoft.SharePoint.Client.SharePointOnlineCredentials($userName, $pwd)
$context.Credentials = $credential
$web = $context.Web
$context.Load($web)
$web.AllProperties["AllVerticalContent"] = "Combined"
$web.Update()
$context.ExecuteQuery()
$web.AllProperties["FilesVerticalContent"] = "ConnectorsOnly"
$web.Update()
$context.ExecuteQuery()
Set-SPOSite $url -DenyAddAndCustomizePages 1

Write-Host "Success" -ForegroundColor Cyan
Read-Host -Prompt 'Press enter to exit'
```

5. 在 [Microsoft PowerShell](https://microsoft.com/powershell)中輸入必要的值，例如組織名稱、使用者名稱、密碼和網站 URL。 **舉例來說**，如果您的系統管理員認證為 `admin@a830edad9050849823J19081300.onmicrosoft.com` ，則您的組織名稱是**a830edad9050849823J19081300**，而您的網站 URL 是 `https:// a830edad9050849823J19081300.sharepoint.com` 。

> [!NOTE]
> **AllProperties**設定只可在網站集合層級 (小組/Comms 網站) 中完成。

6. 現在您可以搜尋已編制索引的檔案 **，並在**[**全部**] 和 [檔案] 索引標籤中查看結果。

## <a name="search-for-file-share-content-in-the-search-results-page"></a>在搜尋結果頁面中搜尋檔案共用內容
若要搜尋已編制索引的內容，請移至測試租使用者的 [SharePoint](http://sharepoint.com/) 首頁。 結果會顯示在 [ **全部** **] 和** [檔案] 索引標籤中。

由於瀏覽器限制，您無法選取檔結果以查看或開啟本機檔案共用搜尋中的檔案。 若要開啟這些檔案，請複製檔結果的連結，並將其貼到系統瀏覽器的 [位址] 欄中。 若為 [windows](https://microsoft.com/windows)，請使用 windows Explorer。 然後，您就可以在系統上開啟檔案。

![使用 [複製連結] 對話方塊開啟搜尋 SharePoint。](media/fileshare-search.png)

## <a name="troubleshooting"></a>疑難排解
如果連接發生嚴重錯誤，其狀態會顯示為 [ **失敗**]。 若要取得三種錯誤類型的詳細資訊，請移至 **錯誤詳細資料** 頁面並選取失敗的連線。 請參閱 [管理您的連接器](manage-connector.md) 以深入瞭解。
1. **無法接通閘道 (錯誤碼： 11) **。 連接的閘道電腦已關機。 確認在閘道電腦上是否執行 [POWER BI](https://msit.powerbi.com/) 處理常式。
2. **驗證錯誤 (錯誤碼： 12) **。 用來建立連線的認證到期或不再有效。 若要解決此錯誤，請輸入有效的認證。
3. **內部錯誤 (錯誤碼：11或 12) **以外的任何專案。 連接器基礎結構中有錯誤。 請參閱 [回饋](connectors-feedback.md) 文章，以瞭解如何報告這些錯誤。

## <a name="limitations"></a>限制
檔案共用連接器在預覽版本中有下列限制：
* 您只能使用固定的屬性（而非具有自訂屬性的檔案）來索引檔案。
* 目前不支援檔案共用存取控制清單 (ACLs) 。 只支援 NTFS 檔 ACLs。
* 不支援外部身分識別。 這些識別碼必須對應至 [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/) 身分識別。
