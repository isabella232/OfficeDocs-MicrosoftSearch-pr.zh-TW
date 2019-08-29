---
title: 設定預設瀏覽器
ms.author: anfowler
author: adefowler
manager: shohara
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
description: 針對 Microsoft Search 使用者將預設瀏覽器設定為 Microsoft Edge 或 Internet Explorer。
ms.openlocfilehash: ed145a1811aba0b58158ed04dd3bf8dc089a0682
ms.sourcegitcommit: c2c9e66af1038efd2849d578f846680851f9e5d2
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/27/2019
ms.locfileid: "36639737"
---
# <a name="make-microsoft-edge-the-default-browser"></a>讓 Microsoft Edge 成為預設瀏覽器
  
若要讓使用者獲得 Microsoft Search 的最佳體驗，您可以讓 Microsoft Edge 成為預設的瀏覽器。 這只會將 Microsoft Edge 設定為組織中使用者的預設瀏覽器，個別使用者仍可選取不同的瀏覽器。
  
  
## <a name="windows-8-and-later"></a>Windows 8 和更新版本

下列指示將說明如何讓 Microsoft Edge 或 Internet Explorer 成為執行 Windows 8 或更新版本電腦的預設瀏覽器。 設定此原則之後，使用者將能夠變更瀏覽器。
  
### <a name="step-1-create-the-default-associations-file"></a>步驟 1：建立預設關聯檔案
在網域控制站的 SYSVOL 資料夾中建立預設關聯檔案。

1. 開啟系統管理 PowerShell 主控台。
1. `New-Item -Path "\\$env:USERDOMAIN\SYSVOL\$env:USERDNSDOMAIN" -Type Directory -Name "Settings"`
1. `$SettingsPath="\\$env:USERDOMAIN\SYSVOL\$env:USERDNSDOMAIN\Settings"`
1. `Start-Process Dism.exe -PassThru "/Online /Export-DefaultAppAssociations:$SettingsPath\AppAssoc.xml"`
    
  
### <a name="step-2-add-or-edit-the-default-associations-file"></a>步驟 2： 新增或編輯預設關聯檔案

1. `Notepad "$SettingsPath\AppAssoc.xml"`
1. 編輯下列項目 (.htm、.html、.http、.https)，然後將不需要的其他項目移除。
  - **Microsoft Edge**
    - `<Association Identifier=".htm" ProgId="AppX4hxtad77fbk3jkkeerkrm0ze94wjf3s9" ApplicationName="Microsoft Edge" />`
              
    - `<Association Identifier=".html" ProgId="AppX4hxtad77fbk3jkkeerkrm0ze94wjf3s9" ApplicationName="Microsoft Edge" />`
    - `<Association Identifier="http" ProgId="AppXq0fevzme2pys62n3e0fbqa7peapykr8v" ApplicationName="Microsoft Edge" />`
    
  - **Internet Explorer**
    
    - `<Association Identifier=".htm" ProgId="htmlfile" ApplicationName="Internet Explorer" />`        
    - `<Association Identifier=".html" ProgId="htmlfile" ApplicationName="Internet Explorer" />`
    - `<Association Identifier="http" ProgId="IE.HTTP" ApplicationName="Internet Explorer" />`
    - `<Association Identifier="https" ProgId="IE.HTTPS" ApplicationName="Internet Explorer" />`

### <a name="step-3-edit-the-group-policy"></a>步驟 3： 編輯群組原則

1. 開啟 [群組原則管理主控台]**** (gpmc.msc)，然後切換以編輯任何現有原則或建立新原則。
1. 瀏覽至 [電腦設定]\[系統管理範本]\[Windows 元件]\[檔案總管]****。
1. 按兩下 [設定預設關聯設定檔]****，將它設為 [已啟用]****，然後輸入 AppAssoc.xml 的路徑 (例如 %USERDOMAIN%\SYSVOL\%USERDNSDOMAIN%\Settings\AppAssoc.xml)。將結果 GPO 連結到適當網域以強制執行結果 GPO。

  
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
    
