---
title: 設定預設瀏覽器
ms.author: anfowler
author: adefowler
manager: shohara
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: 53e2b71a-348b-4dfe-a504-6e97d573effe
description: 針對 Microsoft Search 使用者將預設瀏覽器設定為 Microsoft Edge 或 Internet Explorer。
ms.openlocfilehash: b99127411d070b37fe34a4f8468449f2354cb6be
ms.sourcegitcommit: 21361af7c244ffd6ff8689fd0ff0daa359bf4129
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/14/2019
ms.locfileid: "38626934"
---
# <a name="make-microsoft-edge-the-default-browser"></a><span data-ttu-id="35a3a-103">讓 Microsoft Edge 成為預設瀏覽器</span><span class="sxs-lookup"><span data-stu-id="35a3a-103">Make Microsoft Edge the default browser</span></span>
  
<span data-ttu-id="35a3a-104">若要讓使用者獲得 Microsoft Search 的最佳體驗，您可以讓 Microsoft Edge 成為預設的瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="35a3a-104">To give your users the best experience with Microsoft Search, you can make Microsoft Edge the default browser.</span></span> <span data-ttu-id="35a3a-105">這只會將 Microsoft Edge 設定為組織中使用者的預設瀏覽器，個別使用者仍可選取不同的瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="35a3a-105">This will only set Microsoft Edge as the default browser for users in your org, individual users can still select a different browser.</span></span>
  
  
## <a name="windows-8-and-later"></a><span data-ttu-id="35a3a-106">Windows 8 和更新版本</span><span class="sxs-lookup"><span data-stu-id="35a3a-106">Windows 8 and later</span></span>

<span data-ttu-id="35a3a-107">下列指示將說明如何讓 Microsoft Edge 或 Internet Explorer 成為執行 Windows 8 或更新版本電腦的預設瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="35a3a-107">These instructions show you how to make Microsoft Edge or Internet Explorer as the default browser for computers running Windows 8 or later.</span></span> <span data-ttu-id="35a3a-108">設定此原則之後，使用者將能夠變更瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="35a3a-108">Users will be able to change the browser after this policy is set.</span></span>
  
### <a name="step-1-create-the-default-associations-file"></a><span data-ttu-id="35a3a-109">步驟 1：建立預設關聯檔案</span><span class="sxs-lookup"><span data-stu-id="35a3a-109">STEP 1: Create the default associations file</span></span>
<span data-ttu-id="35a3a-110">在網域控制站的 SYSVOL 資料夾中建立預設關聯檔案。</span><span class="sxs-lookup"><span data-stu-id="35a3a-110">Create the default associations file in the SYSVOL folder of the domain controller.</span></span>

1. <span data-ttu-id="35a3a-111">開啟系統管理 PowerShell 主控台。</span><span class="sxs-lookup"><span data-stu-id="35a3a-111">Open an administrative PowerShell console.</span></span>
1. `New-Item -Path "\\$env:USERDOMAIN\SYSVOL\$env:USERDNSDOMAIN" -Type Directory -Name "Settings"`
1. `$SettingsPath="\\$env:USERDOMAIN\SYSVOL\$env:USERDNSDOMAIN\Settings"`
1. `Start-Process Dism.exe -PassThru "/Online /Export-DefaultAppAssociations:$SettingsPath\AppAssoc.xml"`
    
  
### <a name="step-2-add-or-edit-the-default-associations-file"></a><span data-ttu-id="35a3a-112">步驟 2：</span><span class="sxs-lookup"><span data-stu-id="35a3a-112">STEP 2.</span></span> <span data-ttu-id="35a3a-113">新增或編輯預設關聯檔案</span><span class="sxs-lookup"><span data-stu-id="35a3a-113">Add or edit the default associations file</span></span>

1. `Notepad "$SettingsPath\AppAssoc.xml"`
1. <span data-ttu-id="35a3a-114">編輯下列項目 (.htm、.html、.http、.https)，然後將不需要的其他項目移除。</span><span class="sxs-lookup"><span data-stu-id="35a3a-114">Edit the following entries (.htm, .html, http, https), and remove other entries if they're not needed.</span></span>
  - <span data-ttu-id="35a3a-115">**Microsoft Edge**</span><span class="sxs-lookup"><span data-stu-id="35a3a-115">**Microsoft Edge**</span></span>
    - `<Association Identifier=".htm" ProgId="AppX4hxtad77fbk3jkkeerkrm0ze94wjf3s9" ApplicationName="Microsoft Edge" />`
              
    - `<Association Identifier=".html" ProgId="AppX4hxtad77fbk3jkkeerkrm0ze94wjf3s9" ApplicationName="Microsoft Edge" />`
    - `<Association Identifier="http" ProgId="AppXq0fevzme2pys62n3e0fbqa7peapykr8v" ApplicationName="Microsoft Edge" />`
    
  - <span data-ttu-id="35a3a-116">**Internet Explorer**</span><span class="sxs-lookup"><span data-stu-id="35a3a-116">**Internet Explorer**</span></span>
    
    - `<Association Identifier=".htm" ProgId="htmlfile" ApplicationName="Internet Explorer" />`        
    - `<Association Identifier=".html" ProgId="htmlfile" ApplicationName="Internet Explorer" />`
    - `<Association Identifier="http" ProgId="IE.HTTP" ApplicationName="Internet Explorer" />`
    - `<Association Identifier="https" ProgId="IE.HTTPS" ApplicationName="Internet Explorer" />`

### <a name="step-3-edit-the-group-policy"></a><span data-ttu-id="35a3a-117">步驟 3：</span><span class="sxs-lookup"><span data-stu-id="35a3a-117">Step 3.</span></span> <span data-ttu-id="35a3a-118">編輯群組原則</span><span class="sxs-lookup"><span data-stu-id="35a3a-118">Edit the Group Policy</span></span>

1. <span data-ttu-id="35a3a-119">開啟 [群組原則管理主控台]\*\*\*\* (gpmc.msc)，然後切換以編輯任何現有原則或建立新原則。</span><span class="sxs-lookup"><span data-stu-id="35a3a-119">Open **Group Policy Management Console** (gpmc.msc) and switch to editing any existing policy or creating a new one.</span></span>
1. <span data-ttu-id="35a3a-120">瀏覽至 [電腦設定]\[系統管理範本]\[Windows 元件]\[檔案總管]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="35a3a-120">Navigate to **Computer Configuration\Administrative Templates\Windows Components\File Explorer**.</span></span>
1. <span data-ttu-id="35a3a-121">按兩下 [設定預設關聯設定檔]\*\*\*\*，將它設為 [已啟用]\*\*\*\*，然後輸入 AppAssoc.xml 的路徑 (例如 %USERDOMAIN%\SYSVOL\%USERDNSDOMAIN%\Settings\AppAssoc.xml)。將結果 GPO 連結到適當網域以強制執行結果 GPO。</span><span class="sxs-lookup"><span data-stu-id="35a3a-121">Double-click **Set a default associations configuration file**, set it to **Enabled**, and enter the path to AppAssoc.xml (for example %USERDOMAIN%\SYSVOL\%USERDNSDOMAIN%\Settings\AppAssoc.xml) Enforce the resultant GPO by linking it to the appropriate domain.</span></span>

  
## <a name="windows-7"></a><span data-ttu-id="35a3a-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="35a3a-122">Windows 7</span></span>

1. <span data-ttu-id="35a3a-123">設定將用來設定 GPO 的本機電腦。</span><span class="sxs-lookup"><span data-stu-id="35a3a-123">Configure the local machine that will be used to set the GPO.</span></span>
    
1. <span data-ttu-id="35a3a-124">開啟 [控制台]\[程式集]\[預設程式]\[設定預設程式]\*\*\*\*，然後將 Internet Explorer 設為預設值。</span><span class="sxs-lookup"><span data-stu-id="35a3a-124">Open **Control Panel\Programs\Default Programs\Set Default Programs** and set Internet Explorer as the default.</span></span> 
    
2. <span data-ttu-id="35a3a-125">開啟 [群組原則管理] 主控台 (gpmc.msc)，然後切換以編輯任何現有原則或建立新原則。</span><span class="sxs-lookup"><span data-stu-id="35a3a-125">Open Group Policy Management Console (gpmc.msc) and switch to editing any existing policy or creating a new one.</span></span>
    
1. <span data-ttu-id="35a3a-126">瀏覽至 [\<電腦/使用者\>設定]\[原則]\[喜好設定]\[Windows 設定]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="35a3a-126">Navigate to **\<Computer/User\> Configuration\Policies\Preferences\Windows Settings**.</span></span>
    
2. <span data-ttu-id="35a3a-127">以滑鼠右鍵按一下 [登錄]\[新增]\*\*\*\*，然後選取 [登錄精靈]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="35a3a-127">Right-click on **Registry\New** and select **Registry Wizard**.</span></span>
    
3. <span data-ttu-id="35a3a-128">從 [登錄瀏覽器] 視窗中，選取 [本機電腦]\*\*\*\*，然後按 [下一步]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="35a3a-128">From the Registry Browser window, select **Local Computer** and click **Next**.</span></span>
    
4. <span data-ttu-id="35a3a-129">瀏覽至 **HKEY_CURRENT_USER\Software\Microsoft\Windows\Shell\Associations\UrlAssociations\https**，然後選取 ProgId 值。</span><span class="sxs-lookup"><span data-stu-id="35a3a-129">Navigate to **HKEY_CURRENT_USER\Software\Microsoft\Windows\Shell\Associations\UrlAssociations\https** and select the ProgId value.</span></span> <span data-ttu-id="35a3a-130">確定此值看起來與畫面中的值類似：</span><span class="sxs-lookup"><span data-stu-id="35a3a-130">Make sure the value looks like the one below:</span></span> 
    
    ![在 [編輯字串] 中選取 ProgID 值](media/f6173dcc-b898-4967-8c40-4b0fe411a92b.png)
  
5. <span data-ttu-id="35a3a-132">瀏覽至 **HKEY_CURRENT_USER\Software\Microsoft\Windows\Shell\Associations\UrlAssociations\https**，然後選取 ProgId 值。</span><span class="sxs-lookup"><span data-stu-id="35a3a-132">Navigate to **HKEY_CURRENT_USER\Software\Microsoft\Windows\Shell\Associations\UrlAssociations\https** and select the ProgId value.</span></span> <span data-ttu-id="35a3a-133">確定此值看起來與畫面中的值類似：</span><span class="sxs-lookup"><span data-stu-id="35a3a-133">Make sure that the value looks like the one below:</span></span> 
    
    ![在 [編輯字串] 中針對 HTTPS 選取 ProgId](media/3519e13b-4fe7-4d15-946c-82fd50fc49bb.png)
  
3. <span data-ttu-id="35a3a-135">將結果 GPO 連結到適當網域以強制執行結果 GPO。</span><span class="sxs-lookup"><span data-stu-id="35a3a-135">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>
    
