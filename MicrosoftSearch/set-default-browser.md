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
ms.openlocfilehash: daff7f66bd38bdd56179e44c36092a2c4fd42b42
ms.sourcegitcommit: be2e837d9b087bffe6ce40d72d7ae58a8fcdf3fe
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/30/2019
ms.locfileid: "34591159"
---
# <a name="set-default-browser"></a><span data-ttu-id="7e250-103">設定預設瀏覽器</span><span class="sxs-lookup"><span data-stu-id="7e250-103">Set default browser</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7e250-104">本文章適用 Bing 系統管理入口網站中的 Microsoft Search。</span><span class="sxs-lookup"><span data-stu-id="7e250-104">This article applies to the Microsoft Search in Bing admin portal.</span></span> <span data-ttu-id="7e250-105">我們正在將入口網站移至 Microsoft 365 系統管理中心，完成之後入口網站將會移除。</span><span class="sxs-lookup"><span data-stu-id="7e250-105">We’re moving the portal to the Microsoft 365 admin center, and then it will be removed.</span></span> <span data-ttu-id="7e250-106">我們建議您使用 Microsoft 365 系統管理中心開始。</span><span class="sxs-lookup"><span data-stu-id="7e250-106">We recommend that you use the Microsoft 365 admin center to get started.</span></span> <span data-ttu-id="7e250-107">[Microsoft Search 概觀](overview-microsoft-search.md)。</span><span class="sxs-lookup"><span data-stu-id="7e250-107">[Overview of Microsoft Graph](overview-microsoft-search.md)</span></span>
    
<span data-ttu-id="7e250-108">設定預設瀏覽器、預設搜尋引擎和預設首頁將可協助您的使用者探索 Microsoft Search 功能，鼓勵更常使用，並提供更順暢的體驗。</span><span class="sxs-lookup"><span data-stu-id="7e250-108">Configuring the default browser, default search engine, and default homepage will help your users discover Microsoft Search capabilities, encourage more usage, and provide a smoother experience.</span></span>
  
<span data-ttu-id="7e250-109">若要為您的組織設定預設瀏覽器，請依照以下步驟進行。</span><span class="sxs-lookup"><span data-stu-id="7e250-109">To set the default browser for your organization, follow the steps below.</span></span>
  
## <a name="windows-8-and-above"></a><span data-ttu-id="7e250-110">Windows 8 和更新版本</span><span class="sxs-lookup"><span data-stu-id="7e250-110">Windows 8 and above</span></span>

<span data-ttu-id="7e250-111">若要將 Internet Explorer 或 Microsoft Edge 設為預設瀏覽器中，請依照下列步驟進行：</span><span class="sxs-lookup"><span data-stu-id="7e250-111">To set Internet Explorer or Microsoft Edge as the default browser, follow these steps:</span></span>
  
### <a name="create-default-associations-file"></a><span data-ttu-id="7e250-112">建立預設關聯檔案</span><span class="sxs-lookup"><span data-stu-id="7e250-112">Create default associations file</span></span>

1. <span data-ttu-id="7e250-113">開啟系統管理 PowerShell 主控台。</span><span class="sxs-lookup"><span data-stu-id="7e250-113">Open an administrative PowerShell console.</span></span>
    
2.  `New-Item -Path "\\$env:USERDOMAIN\SYSVOL\$env:USERDNSDOMAIN" -Type Directory -Name "Settings"`
    
3.  `$SettingsPath="\\$env:USERDOMAIN\SYSVOL\$env:USERDNSDOMAIN\Settings"`
    
4.  `Start-Process Dism.exe -PassThru "/Online /Export-DefaultAppAssociations:$SettingsPath\AppAssoc.xml"`
    
<span data-ttu-id="7e250-114">這些步驟會在網域控制站的 SYSVOL 資料夾中嘗試並建立預設關聯檔案。</span><span class="sxs-lookup"><span data-stu-id="7e250-114">These steps try and create the default associations file in the SYSVOL folder of the domain controller.</span></span>
  
### <a name="add-or-edit-the-default-associations-file"></a><span data-ttu-id="7e250-115">新增或編輯預設關聯檔案</span><span class="sxs-lookup"><span data-stu-id="7e250-115">Add or edit the default associations file</span></span>

1. `Notepad "$SettingsPath\AppAssoc.xml"`
    
2. <span data-ttu-id="7e250-116">編輯下列項目 (.htm、.html、.http、.https)，然後將不需要的其他項目移除。</span><span class="sxs-lookup"><span data-stu-id="7e250-116">Edit the following entries (.htm, .html, http, https), and remove other entries if they're not needed.</span></span>
    
  - <span data-ttu-id="7e250-117">**Microsoft Edge**</span><span class="sxs-lookup"><span data-stu-id="7e250-117">**Microsoft Edge**</span></span>
    
     `<Association Identifier=".htm" ProgId="AppX4hxtad77fbk3jkkeerkrm0ze94wjf3s9" ApplicationName="Microsoft Edge" />`
  
     `<Association Identifier=".html" ProgId="AppX4hxtad77fbk3jkkeerkrm0ze94wjf3s9" ApplicationName="Microsoft Edge" />`
  
     `<Association Identifier="http" ProgId="AppXq0fevzme2pys62n3e0fbqa7peapykr8v" ApplicationName="Microsoft Edge" />`
    
  - <span data-ttu-id="7e250-118">**Internet Explorer**</span><span class="sxs-lookup"><span data-stu-id="7e250-118">**Internet Explorer**</span></span>
    
     `<Association Identifier=".htm" ProgId="htmlfile" ApplicationName="Internet Explorer" />`
  
     `<Association Identifier=".html" ProgId="htmlfile" ApplicationName="Internet Explorer" />`
  
     `<Association Identifier="http" ProgId="IE.HTTP" ApplicationName="Internet Explorer" />`
  
     `<Association Identifier="https" ProgId="IE.HTTPS" ApplicationName="Internet Explorer" />`
    
3. <span data-ttu-id="7e250-119">開啟 [群組原則管理] 主控台 (gpmc.msc)，然後切換以編輯任何現有原則或建立新原則。</span><span class="sxs-lookup"><span data-stu-id="7e250-119">Open Group Policy Management Console (gpmc.msc) and switch to editing any existing policy or creating a new one.</span></span>
    
1. <span data-ttu-id="7e250-120">瀏覽至 [電腦設定]\[系統管理範本]\[Windows 元件]\[檔案總管]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="7e250-120">Navigate to **Computer Configuration\Administrative Templates\Windows Components\File Explorer**</span></span>
    
2. <span data-ttu-id="7e250-121">按兩下 [設定預設關聯設定檔]\*\*\*\*，將它設為 [已啟用]\*\*\*\*，然後輸入 AppAssoc.xml 的路徑 (例如 %USERDOMAIN%\SYSVOL\%USERDNSDOMAIN%\Settings\AppAssoc.xml)</span><span class="sxs-lookup"><span data-stu-id="7e250-121">Double-click **Set a default associations configuration file**, set it to **Enabled**, and enter the path to AppAssoc.xml (for example %USERDOMAIN%\SYSVOL\%USERDNSDOMAIN%\Settings\AppAssoc.xml)</span></span>
    
4. <span data-ttu-id="7e250-122">將結果 GPO 連結到適當網域以強制執行結果 GPO。</span><span class="sxs-lookup"><span data-stu-id="7e250-122">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>
    
<span data-ttu-id="7e250-123">設定此原則之後，使用者將能夠變更瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="7e250-123">Users will be able to change the browser after this policy is set.</span></span>
  
## <a name="windows-7"></a><span data-ttu-id="7e250-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7e250-124">Windows 7</span></span>

1. <span data-ttu-id="7e250-125">設定將用來設定 GPO 的本機電腦。</span><span class="sxs-lookup"><span data-stu-id="7e250-125">Configure the local machine that will be used to set the GPO.</span></span>
    
1. <span data-ttu-id="7e250-126">開啟 [控制台]\[程式集]\[預設程式]\[設定預設程式]\*\*\*\*，然後將 Internet Explorer 設為預設值。</span><span class="sxs-lookup"><span data-stu-id="7e250-126">Open **Control Panel\Programs\Default Programs\Set Default Programs** and set Internet Explorer as the default.</span></span> 
    
2. <span data-ttu-id="7e250-127">開啟 [群組原則管理] 主控台 (gpmc.msc)，然後切換以編輯任何現有原則或建立新原則。</span><span class="sxs-lookup"><span data-stu-id="7e250-127">Open Group Policy Management Console (gpmc.msc) and switch to editing any existing policy or creating a new one.</span></span>
    
1. <span data-ttu-id="7e250-128">瀏覽至 [\<電腦/使用者\>設定]\[原則]\[喜好設定]\[Windows 設定]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="7e250-128">Navigate to **\<Computer/User\> Configuration\Policies\Preferences\Windows Settings**.</span></span>
    
2. <span data-ttu-id="7e250-129">以滑鼠右鍵按一下 [登錄]\[新增]\*\*\*\*，然後選取 [登錄精靈]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="7e250-129">Right-click on **Registry\New** and select **Registry Wizard**.</span></span>
    
3. <span data-ttu-id="7e250-130">從 [登錄瀏覽器] 視窗中，選取 [本機電腦]\*\*\*\*，然後按 [下一步]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="7e250-130">From the Registry Browser window, select **Local Computer** and click **Next**.</span></span>
    
4. <span data-ttu-id="7e250-131">瀏覽至 **HKEY_CURRENT_USER\Software\Microsoft\Windows\Shell\Associations\UrlAssociations\https**，然後選取 ProgId 值。</span><span class="sxs-lookup"><span data-stu-id="7e250-131">Navigate to **HKEY_CURRENT_USER\Software\Microsoft\Windows\Shell\Associations\UrlAssociations\https** and select the ProgId value.</span></span> <span data-ttu-id="7e250-132">確定此值看起來與畫面中的值類似：</span><span class="sxs-lookup"><span data-stu-id="7e250-132">Make sure the value looks like the one below:</span></span> 
    
    ![在 [編輯字串] 中選取 ProgID 值](media/f6173dcc-b898-4967-8c40-4b0fe411a92b.png)
  
5. <span data-ttu-id="7e250-134">瀏覽至 **HKEY_CURRENT_USER\Software\Microsoft\Windows\Shell\Associations\UrlAssociations\https**，然後選取 ProgId 值。</span><span class="sxs-lookup"><span data-stu-id="7e250-134">Navigate to **HKEY_CURRENT_USER\Software\Microsoft\Windows\Shell\Associations\UrlAssociations\https** and select the ProgId value.</span></span> <span data-ttu-id="7e250-135">確定此值看起來與畫面中的值類似：</span><span class="sxs-lookup"><span data-stu-id="7e250-135">Make sure that the value looks like the one below:</span></span> 
    
    ![在 [編輯字串] 中針對 HTTPS 選取 ProgId](media/3519e13b-4fe7-4d15-946c-82fd50fc49bb.png)
  
3. <span data-ttu-id="7e250-137">將結果 GPO 連結到適當網域以強制執行結果 GPO。</span><span class="sxs-lookup"><span data-stu-id="7e250-137">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>
    
<span data-ttu-id="7e250-138">設定此原則之後，使用者將能夠變更瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="7e250-138">Users will be able to change the browser after this policy is set.</span></span>