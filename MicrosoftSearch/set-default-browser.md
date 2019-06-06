---
title: 設定預設瀏覽器
ms.author: dawholl
author: dawholl
manager: kellis
ms.date: 12/20/2018
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Priority
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: 53e2b71a-348b-4dfe-a504-6e97d573effe
ROBOTS: NOINDEX
description: 了解如何為您的公司設定使用 Microsoft Search 的預設瀏覽器。
ms.openlocfilehash: 08c61bf6dd68f8044f3f79a0b22829a8f7f6b8ef
ms.sourcegitcommit: fe7f3dae4edba97071a4d127e8a27bdf4fa00d81
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/05/2019
ms.locfileid: "34727841"
---
# <a name="set-default-browser"></a>設定預設瀏覽器

  
設定預設瀏覽器、預設搜尋引擎和預設首頁將可協助您的使用者探索 Microsoft Search 功能，鼓勵更常使用，並提供更順暢的體驗。
  
若要為您的組織設定預設瀏覽器，請依照以下步驟進行。
  
## <a name="windows-8-and-above"></a>Windows 8 和更新版本

若要將 Internet Explorer 或 Microsoft Edge 設為預設瀏覽器中，請依照下列步驟進行：
  
### <a name="create-default-associations-file"></a>建立預設關聯檔案

1. 開啟系統管理 PowerShell 主控台。
    
2.  `New-Item -Path "\\$env:USERDOMAIN\SYSVOL\$env:USERDNSDOMAIN" -Type Directory -Name "Settings"`
    
3.  `$SettingsPath="\\$env:USERDOMAIN\SYSVOL\$env:USERDNSDOMAIN\Settings"`
    
4.  `Start-Process Dism.exe -PassThru "/Online /Export-DefaultAppAssociations:$SettingsPath\AppAssoc.xml"`
    
這些步驟會在網域控制站的 SYSVOL 資料夾中嘗試並建立預設關聯檔案。
  
### <a name="add-or-edit-the-default-associations-file"></a>新增或編輯預設關聯檔案

1. `Notepad "$SettingsPath\AppAssoc.xml"`
    
2. 編輯下列項目 (.htm、.html、.http、.https)，然後將不需要的其他項目移除。
    
  - **Microsoft Edge**
    
     `<Association Identifier=".htm" ProgId="AppX4hxtad77fbk3jkkeerkrm0ze94wjf3s9" ApplicationName="Microsoft Edge" />`
  
     `<Association Identifier=".html" ProgId="AppX4hxtad77fbk3jkkeerkrm0ze94wjf3s9" ApplicationName="Microsoft Edge" />`
  
     `<Association Identifier="http" ProgId="AppXq0fevzme2pys62n3e0fbqa7peapykr8v" ApplicationName="Microsoft Edge" />`
    
  - **Internet Explorer**
    
     `<Association Identifier=".htm" ProgId="htmlfile" ApplicationName="Internet Explorer" />`
  
     `<Association Identifier=".html" ProgId="htmlfile" ApplicationName="Internet Explorer" />`
  
     `<Association Identifier="http" ProgId="IE.HTTP" ApplicationName="Internet Explorer" />`
  
     `<Association Identifier="https" ProgId="IE.HTTPS" ApplicationName="Internet Explorer" />`
    
3. 開啟 [群組原則管理] 主控台 (gpmc.msc)，然後切換以編輯任何現有原則或建立新原則。
    
1. 瀏覽至 [電腦設定]\[系統管理範本]\[Windows 元件]\[檔案總管]****
    
2. 按兩下 [設定預設關聯設定檔]****，將它設為 [已啟用]****，然後輸入 AppAssoc.xml 的路徑 (例如 %USERDOMAIN%\SYSVOL\%USERDNSDOMAIN%\Settings\AppAssoc.xml)
    
4. 將結果 GPO 連結到適當網域以強制執行結果 GPO。
    
設定此原則之後，使用者將能夠變更瀏覽器。
  
## <a name="windows-7"></a>Windows 7

1. 設定將用來設定 GPO 的本機電腦。
    
1. 開啟 [控制台]\[程式集]\[預設程式]\[設定預設程式]****，然後將 Internet Explorer 設為預設值。 
    
2. 開啟 [群組原則管理] 主控台 (gpmc.msc)，然後切換以編輯任何現有原則或建立新原則。
    
1. 瀏覽至 [\<電腦/使用者\>設定]\[原則]\[喜好設定]\[Windows 設定]****。
    
2. 以滑鼠右鍵按一下 [登錄]\[新增]****，然後選取 [登錄精靈]****。
    
3. 從 [登錄瀏覽器] 視窗中，選取 [本機電腦]****，然後按 [下一步]****。
    
4. 瀏覽至 **HKEY_CURRENT_USER\Software\Microsoft\Windows\Shell\Associations\UrlAssociations\https**，然後選取 ProgId 值。 確定此值看起來與畫面中的值類似： 
    
    ![在 [編輯字串] 中選取 ProgID 值](media/f6173dcc-b898-4967-8c40-4b0fe411a92b.png)
  
5. 瀏覽至 **HKEY_CURRENT_USER\Software\Microsoft\Windows\Shell\Associations\UrlAssociations\https**，然後選取 ProgId 值。 確定此值看起來與畫面中的值類似： 
    
    ![在 [編輯字串] 中針對 HTTPS 選取 ProgId](media/3519e13b-4fe7-4d15-946c-82fd50fc49bb.png)
  
3. 將結果 GPO 連結到適當網域以強制執行結果 GPO。
    
設定此原則之後，使用者將能夠變更瀏覽器。