---
title: 設定預設瀏覽器
ms.author: dawholl
author: dawholl
manager: kellis
ms.date: 12/20/2018
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: 53e2b71a-348b-4dfe-a504-6e97d573effe
description: 了解如何設定為與 Microsoft Search 貴公司的預設瀏覽器。
ms.openlocfilehash: 13a0a878b3288abeb7b07defdab839a158adc2ac
ms.sourcegitcommit: bf52cc63b75f2e0324a716fe65da47702956b722
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/18/2019
ms.locfileid: "29380078"
---
# <a name="set-default-browser"></a>設定預設瀏覽器

設定預設的瀏覽器、 預設搜尋引擎，以及預設首頁可協助您探索 Microsoft 搜尋功能、 鼓勵更多的使用狀況，並提供更順暢的使用者。
  
若要設定您的組織的預設瀏覽器，請遵循下列步驟。
  
## <a name="windows-8-and-above"></a>Windows 8 及以上

若要為預設瀏覽器設定 Internet Explorer 或 Microsoft Edge，遵循下列步驟：
  
### <a name="create-default-associations-file"></a>建立關聯的預設檔案

1. 開啟 [系統管理的 PowerShell 主控台]。
    
2.  `New-Item -Path "\\$env:USERDOMAIN\SYSVOL\$env:USERDNSDOMAIN" -Type Directory -Name "Settings"`
    
3.  `$SettingsPath="\\$env:USERDOMAIN\SYSVOL\$env:USERDNSDOMAIN\Settings"`
    
4.  `Start-Process Dism.exe -PassThru "/Online /Export-DefaultAppAssociations:$SettingsPath\AppAssoc.xml"`
    
這些步驟嘗試與網域控制站的 SYSVOL 資料夾中建立的預設關聯檔案。
  
### <a name="add-or-edit-the-default-associations-file"></a>新增或編輯預設關聯檔案

1. `Notepad "$SettingsPath\AppAssoc.xml"`
    
2. 編輯下列項目 （.htm、.html、 http、 https） 並不是需要時移除其他項目。
    
  - **Microsoft Edge**
    
     `<Association Identifier=".htm" ProgId="AppX4hxtad77fbk3jkkeerkrm0ze94wjf3s9" ApplicationName="Microsoft Edge" />`
  
     `<Association Identifier=".html" ProgId="AppX4hxtad77fbk3jkkeerkrm0ze94wjf3s9" ApplicationName="Microsoft Edge" />`
  
     `<Association Identifier="http" ProgId="AppXq0fevzme2pys62n3e0fbqa7peapykr8v" ApplicationName="Microsoft Edge" />`
    
  - **Internet Explorer**
    
     `<Association Identifier=".htm" ProgId="htmlfile" ApplicationName="Internet Explorer" />`
  
     `<Association Identifier=".html" ProgId="htmlfile" ApplicationName="Internet Explorer" />`
  
     `<Association Identifier="http" ProgId="IE.HTTP" ApplicationName="Internet Explorer" />`
  
     `<Association Identifier="https" ProgId="IE.HTTPS" ApplicationName="Internet Explorer" />`
    
3. 若要編輯的任何現有原則或建立一個新參數和開啟群組原則管理主控台 （gpmc.msc 取得）。
    
1. 瀏覽至 [**電腦設定系統 Components\File 瀏覽器**
    
2. 連按兩下 [**設定預設的關聯設定檔**、 將它設為 [**已啟用**] 並輸入 AppAssoc.xml 的路徑 (例如 %USERDOMAIN%\SYSVOL\%USERDNSDOMAIN%\Settings\AppAssoc.xml)
    
4. 強制產生 GPO 連結至適當的網域。
    
使用者無法變更瀏覽器之後此原則設定。
  
## <a name="windows-7"></a>Windows 7

1. 設定本機電腦將用來將 GPO 設定。
    
1. 開啟**控制項 Panel\Programs\Default Programs\Set 預設程式**並將 Internet Explorer 設定為預設值。 
    
2. 若要編輯的任何現有原則或建立一個新參數和開啟群組原則管理主控台 （gpmc.msc 取得）。
    
1. 瀏覽至 [**\<電腦/使用者\>Configuration\Policies\Preferences\Windows 設定**。
    
2. 以滑鼠右鍵按一下**Registry\New**並選取 [**登錄精靈**]。
    
3. 從登錄瀏覽器視窗中，選取 [**本機電腦**，並按一下 [**下一步**。
    
4. 瀏覽至 [ **HKEY_CURRENT_USER\Software\Microsoft\Windows\Shell\Associations\UrlAssociations\https**並選取 ProgId 的值。請確定值起來下方： 
    
    ![在 [編輯字串選取 ProgID 的值](media/f6173dcc-b898-4967-8c40-4b0fe411a92b.png)
  
5. 瀏覽至 [ **HKEY_CURRENT_USER\Software\Microsoft\Windows\Shell\Associations\UrlAssociations\https**並選取 ProgId 的值。請確定值如下所示的其中一個下： 
    
    ![選取 [HTTPS 編輯字串中的 [ProgId](media/3519e13b-4fe7-4d15-946c-82fd50fc49bb.png)
  
3. 強制產生 GPO 連結至適當的網域。
    
使用者無法變更瀏覽器之後此原則設定。