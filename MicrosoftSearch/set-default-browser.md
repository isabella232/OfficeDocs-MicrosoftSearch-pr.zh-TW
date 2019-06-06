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
# <a name="set-default-browser"></a><span data-ttu-id="3c858-103">設定預設瀏覽器</span><span class="sxs-lookup"><span data-stu-id="3c858-103">Set default browser</span></span>

  
<span data-ttu-id="3c858-104">設定預設瀏覽器、預設搜尋引擎和預設首頁將可協助您的使用者探索 Microsoft Search 功能，鼓勵更常使用，並提供更順暢的體驗。</span><span class="sxs-lookup"><span data-stu-id="3c858-104">Configuring the default browser, default search engine, and default homepage will help your users discover Microsoft Search capabilities, encourage more usage, and provide a smoother experience.</span></span>
  
<span data-ttu-id="3c858-105">若要為您的組織設定預設瀏覽器，請依照以下步驟進行。</span><span class="sxs-lookup"><span data-stu-id="3c858-105">To set the default browser for your organization, follow the steps below.</span></span>
  
## <a name="windows-8-and-above"></a><span data-ttu-id="3c858-106">Windows 8 和更新版本</span><span class="sxs-lookup"><span data-stu-id="3c858-106">Windows 8 and above</span></span>

<span data-ttu-id="3c858-107">若要將 Internet Explorer 或 Microsoft Edge 設為預設瀏覽器中，請依照下列步驟進行：</span><span class="sxs-lookup"><span data-stu-id="3c858-107">To set Internet Explorer or Microsoft Edge as the default browser, follow these steps:</span></span>
  
### <a name="create-default-associations-file"></a><span data-ttu-id="3c858-108">建立預設關聯檔案</span><span class="sxs-lookup"><span data-stu-id="3c858-108">Create default associations file</span></span>

1. <span data-ttu-id="3c858-109">開啟系統管理 PowerShell 主控台。</span><span class="sxs-lookup"><span data-stu-id="3c858-109">Open an administrative PowerShell console.</span></span>
    
2.  `New-Item -Path "\\$env:USERDOMAIN\SYSVOL\$env:USERDNSDOMAIN" -Type Directory -Name "Settings"`
    
3.  `$SettingsPath="\\$env:USERDOMAIN\SYSVOL\$env:USERDNSDOMAIN\Settings"`
    
4.  `Start-Process Dism.exe -PassThru "/Online /Export-DefaultAppAssociations:$SettingsPath\AppAssoc.xml"`
    
<span data-ttu-id="3c858-110">這些步驟會在網域控制站的 SYSVOL 資料夾中嘗試並建立預設關聯檔案。</span><span class="sxs-lookup"><span data-stu-id="3c858-110">These steps try and create the default associations file in the SYSVOL folder of the domain controller.</span></span>
  
### <a name="add-or-edit-the-default-associations-file"></a><span data-ttu-id="3c858-111">新增或編輯預設關聯檔案</span><span class="sxs-lookup"><span data-stu-id="3c858-111">Add or edit the default associations file</span></span>

1. `Notepad "$SettingsPath\AppAssoc.xml"`
    
2. <span data-ttu-id="3c858-112">編輯下列項目 (.htm、.html、.http、.https)，然後將不需要的其他項目移除。</span><span class="sxs-lookup"><span data-stu-id="3c858-112">Edit the following entries (.htm, .html, http, https), and remove other entries if they're not needed.</span></span>
    
  - <span data-ttu-id="3c858-113">**Microsoft Edge**</span><span class="sxs-lookup"><span data-stu-id="3c858-113">**Microsoft Edge**</span></span>
    
     `<Association Identifier=".htm" ProgId="AppX4hxtad77fbk3jkkeerkrm0ze94wjf3s9" ApplicationName="Microsoft Edge" />`
  
     `<Association Identifier=".html" ProgId="AppX4hxtad77fbk3jkkeerkrm0ze94wjf3s9" ApplicationName="Microsoft Edge" />`
  
     `<Association Identifier="http" ProgId="AppXq0fevzme2pys62n3e0fbqa7peapykr8v" ApplicationName="Microsoft Edge" />`
    
  - <span data-ttu-id="3c858-114">**Internet Explorer**</span><span class="sxs-lookup"><span data-stu-id="3c858-114">**Internet Explorer**</span></span>
    
     `<Association Identifier=".htm" ProgId="htmlfile" ApplicationName="Internet Explorer" />`
  
     `<Association Identifier=".html" ProgId="htmlfile" ApplicationName="Internet Explorer" />`
  
     `<Association Identifier="http" ProgId="IE.HTTP" ApplicationName="Internet Explorer" />`
  
     `<Association Identifier="https" ProgId="IE.HTTPS" ApplicationName="Internet Explorer" />`
    
3. <span data-ttu-id="3c858-115">開啟 [群組原則管理] 主控台 (gpmc.msc)，然後切換以編輯任何現有原則或建立新原則。</span><span class="sxs-lookup"><span data-stu-id="3c858-115">Open Group Policy Management Console (gpmc.msc) and switch to editing any existing policy or creating a new one.</span></span>
    
1. <span data-ttu-id="3c858-116">瀏覽至 [電腦設定]\[系統管理範本]\[Windows 元件]\[檔案總管]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="3c858-116">Navigate to **Computer Configuration\Administrative Templates\Windows Components\File Explorer**</span></span>
    
2. <span data-ttu-id="3c858-117">按兩下 [設定預設關聯設定檔]\*\*\*\*，將它設為 [已啟用]\*\*\*\*，然後輸入 AppAssoc.xml 的路徑 (例如 %USERDOMAIN%\SYSVOL\%USERDNSDOMAIN%\Settings\AppAssoc.xml)</span><span class="sxs-lookup"><span data-stu-id="3c858-117">Double-click **Set a default associations configuration file**, set it to **Enabled**, and enter the path to AppAssoc.xml (for example %USERDOMAIN%\SYSVOL\%USERDNSDOMAIN%\Settings\AppAssoc.xml)</span></span>
    
4. <span data-ttu-id="3c858-118">將結果 GPO 連結到適當網域以強制執行結果 GPO。</span><span class="sxs-lookup"><span data-stu-id="3c858-118">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>
    
<span data-ttu-id="3c858-119">設定此原則之後，使用者將能夠變更瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="3c858-119">Users will be able to change the browser after this policy is set.</span></span>
  
## <a name="windows-7"></a><span data-ttu-id="3c858-120">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3c858-120">Windows 7</span></span>

1. <span data-ttu-id="3c858-121">設定將用來設定 GPO 的本機電腦。</span><span class="sxs-lookup"><span data-stu-id="3c858-121">Configure the local machine that will be used to set the GPO.</span></span>
    
1. <span data-ttu-id="3c858-122">開啟 [控制台]\[程式集]\[預設程式]\[設定預設程式]\*\*\*\*，然後將 Internet Explorer 設為預設值。</span><span class="sxs-lookup"><span data-stu-id="3c858-122">Open **Control Panel\Programs\Default Programs\Set Default Programs** and set Internet Explorer as the default.</span></span> 
    
2. <span data-ttu-id="3c858-123">開啟 [群組原則管理] 主控台 (gpmc.msc)，然後切換以編輯任何現有原則或建立新原則。</span><span class="sxs-lookup"><span data-stu-id="3c858-123">Open Group Policy Management Console (gpmc.msc) and switch to editing any existing policy or creating a new one.</span></span>
    
1. <span data-ttu-id="3c858-124">瀏覽至 [\<電腦/使用者\>設定]\[原則]\[喜好設定]\[Windows 設定]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="3c858-124">Navigate to **\<Computer/User\> Configuration\Policies\Preferences\Windows Settings**.</span></span>
    
2. <span data-ttu-id="3c858-125">以滑鼠右鍵按一下 [登錄]\[新增]\*\*\*\*，然後選取 [登錄精靈]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="3c858-125">Right-click on **Registry\New** and select **Registry Wizard**.</span></span>
    
3. <span data-ttu-id="3c858-126">從 [登錄瀏覽器] 視窗中，選取 [本機電腦]\*\*\*\*，然後按 [下一步]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="3c858-126">From the Registry Browser window, select **Local Computer** and click **Next**.</span></span>
    
4. <span data-ttu-id="3c858-127">瀏覽至 **HKEY_CURRENT_USER\Software\Microsoft\Windows\Shell\Associations\UrlAssociations\https**，然後選取 ProgId 值。</span><span class="sxs-lookup"><span data-stu-id="3c858-127">Navigate to **HKEY_CURRENT_USER\Software\Microsoft\Windows\Shell\Associations\UrlAssociations\https** and select the ProgId value.</span></span> <span data-ttu-id="3c858-128">確定此值看起來與畫面中的值類似：</span><span class="sxs-lookup"><span data-stu-id="3c858-128">Make sure the value looks like the one below:</span></span> 
    
    ![在 [編輯字串] 中選取 ProgID 值](media/f6173dcc-b898-4967-8c40-4b0fe411a92b.png)
  
5. <span data-ttu-id="3c858-130">瀏覽至 **HKEY_CURRENT_USER\Software\Microsoft\Windows\Shell\Associations\UrlAssociations\https**，然後選取 ProgId 值。</span><span class="sxs-lookup"><span data-stu-id="3c858-130">Navigate to **HKEY_CURRENT_USER\Software\Microsoft\Windows\Shell\Associations\UrlAssociations\https** and select the ProgId value.</span></span> <span data-ttu-id="3c858-131">確定此值看起來與畫面中的值類似：</span><span class="sxs-lookup"><span data-stu-id="3c858-131">Make sure that the value looks like the one below:</span></span> 
    
    ![在 [編輯字串] 中針對 HTTPS 選取 ProgId](media/3519e13b-4fe7-4d15-946c-82fd50fc49bb.png)
  
3. <span data-ttu-id="3c858-133">將結果 GPO 連結到適當網域以強制執行結果 GPO。</span><span class="sxs-lookup"><span data-stu-id="3c858-133">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>
    
<span data-ttu-id="3c858-134">設定此原則之後，使用者將能夠變更瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="3c858-134">Users will be able to change the browser after this policy is set.</span></span>