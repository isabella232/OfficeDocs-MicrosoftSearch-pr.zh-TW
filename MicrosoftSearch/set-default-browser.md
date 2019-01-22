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
# <a name="set-default-browser"></a><span data-ttu-id="9ab23-103">設定預設瀏覽器</span><span class="sxs-lookup"><span data-stu-id="9ab23-103">Set default browser</span></span>

<span data-ttu-id="9ab23-104">設定預設的瀏覽器、 預設搜尋引擎，以及預設首頁可協助您探索 Microsoft 搜尋功能、 鼓勵更多的使用狀況，並提供更順暢的使用者。</span><span class="sxs-lookup"><span data-stu-id="9ab23-104">Configuring the default browser, default search engine, and default homepage will help your users discover Microsoft Search capabilities, encourage more usage, and provide a smoother experience.</span></span>
  
<span data-ttu-id="9ab23-105">若要設定您的組織的預設瀏覽器，請遵循下列步驟。</span><span class="sxs-lookup"><span data-stu-id="9ab23-105">To set the default browser for your organization, follow the steps below.</span></span>
  
## <a name="windows-8-and-above"></a><span data-ttu-id="9ab23-106">Windows 8 及以上</span><span class="sxs-lookup"><span data-stu-id="9ab23-106">Windows 8 and above</span></span>

<span data-ttu-id="9ab23-107">若要為預設瀏覽器設定 Internet Explorer 或 Microsoft Edge，遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="9ab23-107">To set Internet Explorer or Microsoft Edge as the default browser, follow these steps:</span></span>
  
### <a name="create-default-associations-file"></a><span data-ttu-id="9ab23-108">建立關聯的預設檔案</span><span class="sxs-lookup"><span data-stu-id="9ab23-108">Create default associations file</span></span>

1. <span data-ttu-id="9ab23-109">開啟 [系統管理的 PowerShell 主控台]。</span><span class="sxs-lookup"><span data-stu-id="9ab23-109">Open an administrative PowerShell console.</span></span>
    
2.  `New-Item -Path "\\$env:USERDOMAIN\SYSVOL\$env:USERDNSDOMAIN" -Type Directory -Name "Settings"`
    
3.  `$SettingsPath="\\$env:USERDOMAIN\SYSVOL\$env:USERDNSDOMAIN\Settings"`
    
4.  `Start-Process Dism.exe -PassThru "/Online /Export-DefaultAppAssociations:$SettingsPath\AppAssoc.xml"`
    
<span data-ttu-id="9ab23-110">這些步驟嘗試與網域控制站的 SYSVOL 資料夾中建立的預設關聯檔案。</span><span class="sxs-lookup"><span data-stu-id="9ab23-110">These steps try and create the default associations file in the SYSVOL folder of the domain controller.</span></span>
  
### <a name="add-or-edit-the-default-associations-file"></a><span data-ttu-id="9ab23-111">新增或編輯預設關聯檔案</span><span class="sxs-lookup"><span data-stu-id="9ab23-111">Add or edit the default associations file</span></span>

1. `Notepad "$SettingsPath\AppAssoc.xml"`
    
2. <span data-ttu-id="9ab23-112">編輯下列項目 （.htm、.html、 http、 https） 並不是需要時移除其他項目。</span><span class="sxs-lookup"><span data-stu-id="9ab23-112">Edit the following entries (.htm, .html, http, https), and remove other entries if they're not needed.</span></span>
    
  - <span data-ttu-id="9ab23-113">**Microsoft Edge**</span><span class="sxs-lookup"><span data-stu-id="9ab23-113">**Microsoft Edge**</span></span>
    
     `<Association Identifier=".htm" ProgId="AppX4hxtad77fbk3jkkeerkrm0ze94wjf3s9" ApplicationName="Microsoft Edge" />`
  
     `<Association Identifier=".html" ProgId="AppX4hxtad77fbk3jkkeerkrm0ze94wjf3s9" ApplicationName="Microsoft Edge" />`
  
     `<Association Identifier="http" ProgId="AppXq0fevzme2pys62n3e0fbqa7peapykr8v" ApplicationName="Microsoft Edge" />`
    
  - <span data-ttu-id="9ab23-114">**Internet Explorer**</span><span class="sxs-lookup"><span data-stu-id="9ab23-114">**Internet Explorer**</span></span>
    
     `<Association Identifier=".htm" ProgId="htmlfile" ApplicationName="Internet Explorer" />`
  
     `<Association Identifier=".html" ProgId="htmlfile" ApplicationName="Internet Explorer" />`
  
     `<Association Identifier="http" ProgId="IE.HTTP" ApplicationName="Internet Explorer" />`
  
     `<Association Identifier="https" ProgId="IE.HTTPS" ApplicationName="Internet Explorer" />`
    
3. <span data-ttu-id="9ab23-115">若要編輯的任何現有原則或建立一個新參數和開啟群組原則管理主控台 （gpmc.msc 取得）。</span><span class="sxs-lookup"><span data-stu-id="9ab23-115">Open Group Policy Management Console (gpmc.msc) and switch to editing any existing policy or creating a new one.</span></span>
    
1. <span data-ttu-id="9ab23-116">瀏覽至 [**電腦設定系統 Components\File 瀏覽器**</span><span class="sxs-lookup"><span data-stu-id="9ab23-116">Navigate to **Computer Configuration\Administrative Templates\Windows Components\File Explorer**</span></span>
    
2. <span data-ttu-id="9ab23-117">連按兩下 [**設定預設的關聯設定檔**、 將它設為 [**已啟用**] 並輸入 AppAssoc.xml 的路徑 (例如 %USERDOMAIN%\SYSVOL\%USERDNSDOMAIN%\Settings\AppAssoc.xml)</span><span class="sxs-lookup"><span data-stu-id="9ab23-117">Double-click **Set a default associations configuration file**, set it to **Enabled**, and enter the path to AppAssoc.xml (for example %USERDOMAIN%\SYSVOL\%USERDNSDOMAIN%\Settings\AppAssoc.xml)</span></span>
    
4. <span data-ttu-id="9ab23-118">強制產生 GPO 連結至適當的網域。</span><span class="sxs-lookup"><span data-stu-id="9ab23-118">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>
    
<span data-ttu-id="9ab23-119">使用者無法變更瀏覽器之後此原則設定。</span><span class="sxs-lookup"><span data-stu-id="9ab23-119">Users will be able to change the browser after this policy is set.</span></span>
  
## <a name="windows-7"></a><span data-ttu-id="9ab23-120">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9ab23-120">Windows 7</span></span>

1. <span data-ttu-id="9ab23-121">設定本機電腦將用來將 GPO 設定。</span><span class="sxs-lookup"><span data-stu-id="9ab23-121">Configure the local machine that will be used to set the GPO.</span></span>
    
1. <span data-ttu-id="9ab23-122">開啟**控制項 Panel\Programs\Default Programs\Set 預設程式**並將 Internet Explorer 設定為預設值。</span><span class="sxs-lookup"><span data-stu-id="9ab23-122">Open **Control Panel\Programs\Default Programs\Set Default Programs** and set Internet Explorer as the default.</span></span> 
    
2. <span data-ttu-id="9ab23-123">若要編輯的任何現有原則或建立一個新參數和開啟群組原則管理主控台 （gpmc.msc 取得）。</span><span class="sxs-lookup"><span data-stu-id="9ab23-123">Open Group Policy Management Console (gpmc.msc) and switch to editing any existing policy or creating a new one.</span></span>
    
1. <span data-ttu-id="9ab23-124">瀏覽至 [**\<電腦/使用者\>Configuration\Policies\Preferences\Windows 設定**。</span><span class="sxs-lookup"><span data-stu-id="9ab23-124">Navigate to **\<Computer/User\> Configuration\Policies\Preferences\Windows Settings**.</span></span>
    
2. <span data-ttu-id="9ab23-125">以滑鼠右鍵按一下**Registry\New**並選取 [**登錄精靈**]。</span><span class="sxs-lookup"><span data-stu-id="9ab23-125">Right-click on **Registry\New** and select **Registry Wizard**.</span></span>
    
3. <span data-ttu-id="9ab23-126">從登錄瀏覽器視窗中，選取 [**本機電腦**，並按一下 [**下一步**。</span><span class="sxs-lookup"><span data-stu-id="9ab23-126">From the Registry Browser window, select **Local Computer** and click **Next**.</span></span>
    
4. <span data-ttu-id="9ab23-p101">瀏覽至 [ **HKEY_CURRENT_USER\Software\Microsoft\Windows\Shell\Associations\UrlAssociations\https**並選取 ProgId 的值。請確定值起來下方：</span><span class="sxs-lookup"><span data-stu-id="9ab23-p101">Navigate to **HKEY_CURRENT_USER\Software\Microsoft\Windows\Shell\Associations\UrlAssociations\https** and select the ProgId value. Make sure the value looks like the one below:</span></span> 
    
    ![在 [編輯字串選取 ProgID 的值](media/f6173dcc-b898-4967-8c40-4b0fe411a92b.png)
  
5. <span data-ttu-id="9ab23-p102">瀏覽至 [ **HKEY_CURRENT_USER\Software\Microsoft\Windows\Shell\Associations\UrlAssociations\https**並選取 ProgId 的值。請確定值如下所示的其中一個下：</span><span class="sxs-lookup"><span data-stu-id="9ab23-p102">Navigate to **HKEY_CURRENT_USER\Software\Microsoft\Windows\Shell\Associations\UrlAssociations\https** and select the ProgId value. Make sure that the value looks like the one below:</span></span> 
    
    ![選取 [HTTPS 編輯字串中的 [ProgId](media/3519e13b-4fe7-4d15-946c-82fd50fc49bb.png)
  
3. <span data-ttu-id="9ab23-133">強制產生 GPO 連結至適當的網域。</span><span class="sxs-lookup"><span data-stu-id="9ab23-133">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>
    
<span data-ttu-id="9ab23-134">使用者無法變更瀏覽器之後此原則設定。</span><span class="sxs-lookup"><span data-stu-id="9ab23-134">Users will be able to change the browser after this policy is set.</span></span>