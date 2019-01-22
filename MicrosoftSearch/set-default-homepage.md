---
title: 設定預設首頁
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
ms.assetid: c020bd72-9906-4dfd-bc77-57287f5927ce
description: 了解如何與 Microsoft Search 公司 Bing 設為預設首頁。
ms.openlocfilehash: 9190e607f5e17a0b898ab131886de12cb300a74c
ms.sourcegitcommit: bf52cc63b75f2e0324a716fe65da47702956b722
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/18/2019
ms.locfileid: "29380037"
---
# <a name="set-default-homepage"></a><span data-ttu-id="4214c-103">設定預設首頁</span><span class="sxs-lookup"><span data-stu-id="4214c-103">Set default homepage</span></span>

<span data-ttu-id="4214c-104">設定預設的瀏覽器、 預設搜尋引擎，以及預設首頁可協助您探索 Microsoft 搜尋功能、 鼓勵更多的使用狀況，並提供更順暢的使用者。</span><span class="sxs-lookup"><span data-stu-id="4214c-104">Configuring the default browser, default search engine, and default homepage will help your users discover Microsoft Search  capabilities, encourage more usage, and provide a smoother experience.</span></span>
  
<span data-ttu-id="4214c-105">若要設定您的組織預設首頁，請遵循下列步驟。</span><span class="sxs-lookup"><span data-stu-id="4214c-105">To set the default homepage for your organization, follow the steps below.</span></span>
  
## <a name="internet-explorer"></a><span data-ttu-id="4214c-106">Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="4214c-106">Internet Explorer</span></span>

### <a name="internet-explorer-50-or-later"></a><span data-ttu-id="4214c-107">Internet Explorer 5.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="4214c-107">Internet Explorer 5.0 or later</span></span>

1. <span data-ttu-id="4214c-108">若要編輯的任何現有原則或建立一個新參數和開啟 「 群組原則管理主控台 （gpmc.msc 取得）。</span><span class="sxs-lookup"><span data-stu-id="4214c-108">Open the Group Policy Management Console (gpmc.msc) and switch to editing any existing policy or creating a new one.</span></span>
    
2. <span data-ttu-id="4214c-109">瀏覽至**使用者 Configuration\Preferences\Control 控制台 Settings\Internet 設定**。</span><span class="sxs-lookup"><span data-stu-id="4214c-109">Navigate to **User Configuration\Preferences\Control Panel Settings\Internet Settings**.</span></span>
    
3. <span data-ttu-id="4214c-110">以滑鼠右鍵按一下**網際網路設定**並選取 [ **Internet Explorer 10**。</span><span class="sxs-lookup"><span data-stu-id="4214c-110">Right-click on **Internet Settings** and select **Internet Explorer 10**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="4214c-111">您必須選取要套用的 Internet Explorer 11 設定為相同的設定會套用至 Internet Explorer 11 Internet Explorer 10 的選項。</span><span class="sxs-lookup"><span data-stu-id="4214c-111">You need to select the option of Internet Explorer 10 to apply the settings for Internet Explorer 11 as the same settings apply to Internet Explorer 11.</span></span> 
  
4. <span data-ttu-id="4214c-p101">這會以紅色加上底線未設定設定在目標電腦，而綠色中以底線標示的設定在目標電腦設定。若要變更底線，使用下列功能鍵：</span><span class="sxs-lookup"><span data-stu-id="4214c-p101">Settings which are underlined in red are not configured at the target machine, while settings underlined in green are configured at the target machine. To change the underlining, use the following function keys:</span></span>
    
    <span data-ttu-id="4214c-114">F5-啟用所有目前的索引標籤上的設定</span><span class="sxs-lookup"><span data-stu-id="4214c-114">F5 - Enable all settings on the current tab</span></span>
    
    <span data-ttu-id="4214c-115">F6-啟用目前選取的設定</span><span class="sxs-lookup"><span data-stu-id="4214c-115">F6 - Enable the currently selected setting</span></span>
    
    <span data-ttu-id="4214c-116">F7-停用目前選取的設定</span><span class="sxs-lookup"><span data-stu-id="4214c-116">F7 - Disable the currently selected setting</span></span>
    
    <span data-ttu-id="4214c-117">F8-停用目前的索引標籤上的所有設定</span><span class="sxs-lookup"><span data-stu-id="4214c-117">F8 - Disable all settings on the current tab</span></span>
    
5. <span data-ttu-id="4214c-p102">按**F8**設定的任何項目之前停用所有設定。螢幕應該看起來如下：</span><span class="sxs-lookup"><span data-stu-id="4214c-p102">Press **F8** to disable all settings before configuring anything. The screen should look like this:</span></span> 
    
    ![Internet Explorer 10 屬性] 對話方塊](media/2fd55755-5007-4e33-a795-c42ce2fcef4a.jpg)
  
6. <span data-ttu-id="4214c-121">在首頁] 頁面上設定按**F6** ，然後輸入`https://www.bing.com/business?form=BFBSPR`</span><span class="sxs-lookup"><span data-stu-id="4214c-121">Press **F6** on the Home page setting and enter `https://www.bing.com/business?form=BFBSPR`</span></span>
    
7. <span data-ttu-id="4214c-122">強制產生 GPO 連結至適當的網域。</span><span class="sxs-lookup"><span data-stu-id="4214c-122">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>
    
> [!NOTE]
> <span data-ttu-id="4214c-123">使用者仍然可以變更首頁後此原則設定。</span><span class="sxs-lookup"><span data-stu-id="4214c-123">Users can still change the homepage after this policy is set.</span></span> 
  
## <a name="microsoft-edge"></a><span data-ttu-id="4214c-124">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4214c-124">Microsoft Edge</span></span>

### <a name="windows-10-version-1511-or-later"></a><span data-ttu-id="4214c-125">Windows 10、 1511 或更新版本</span><span class="sxs-lookup"><span data-stu-id="4214c-125">Windows 10, Version 1511 or later</span></span>

1. <span data-ttu-id="4214c-126">若要編輯的任何現有原則或建立一個新參數和開啟 「 群組原則管理主控台 （gpmc.msc 取得）。</span><span class="sxs-lookup"><span data-stu-id="4214c-126">Open the Group Policy Management Console (gpmc.msc) and switch to editing any existing policy or creating a new one.</span></span>
    
2. <span data-ttu-id="4214c-127">瀏覽至 [**系統管理範本 \windows 元件 \ \microsoft Edge**</span><span class="sxs-lookup"><span data-stu-id="4214c-127">Navigate to **Administrative Templates\Windows Components\Microsoft Edge**</span></span>
    
1. <span data-ttu-id="4214c-128">按兩下 [**頁面設定起始**、 將它設為 [**已啟用**] 並輸入`https://www.bing.com/business`</span><span class="sxs-lookup"><span data-stu-id="4214c-128">Double-click **Configure Start pages**, set it to **Enabled**, and enter `https://www.bing.com/business`</span></span>
    
3. <span data-ttu-id="4214c-129">強制產生 GPO 連結至適當的網域。</span><span class="sxs-lookup"><span data-stu-id="4214c-129">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>
    
> [!CAUTION]
> <span data-ttu-id="4214c-130">使用者將無法設定此原則之後變更搜尋提供者。</span><span class="sxs-lookup"><span data-stu-id="4214c-130">Users won't be able to change the search provider after this policy is set.</span></span> 
  
## <a name="google-chrome"></a><span data-ttu-id="4214c-131">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="4214c-131">Google Chrome</span></span>

### <a name="windows-xp-sp2-or-later"></a><span data-ttu-id="4214c-132">Windows XP SP2 或更新版本</span><span class="sxs-lookup"><span data-stu-id="4214c-132">Windows XP SP2 or later</span></span>

<span data-ttu-id="4214c-133">[Microsoft 技術支援人員上](https://support.microsoft.com/en-us/help/3087759/how-to-create-and-manage-the-central-store-for-group-policy-administra)可以找到上管理 ADMX 檔案和最新 ADMX 檔案的不同版本的 Windows 作業系統支援文章。</span><span class="sxs-lookup"><span data-stu-id="4214c-133">The Windows Support article on managing ADMX files and the latest ADMX files for different versions of Windows can be found [on Microsoft Support](https://support.microsoft.com/en-us/help/3087759/how-to-create-and-manage-the-central-store-for-group-policy-administra).</span></span>

<span data-ttu-id="4214c-134">您也需要最新的 Google 原則檔，您可以找到[Google Chrome 企業](https://support.google.com/chrome/a/answer/187202)協助。</span><span class="sxs-lookup"><span data-stu-id="4214c-134">You'll also need the latest Google policy file, which you can find on [Google Chrome Enterprise Help](https://support.google.com/chrome/a/answer/187202).</span></span>
  
<span data-ttu-id="4214c-p103">如果內部 GPMC 找不到此節所述的設定，下載適當的 ADMX，並將其複製到[集中存放區](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-vista/cc748955%28v%3dws.10%29)。控制站上的集中存放區已有下列的命名慣例的資料夾：</span><span class="sxs-lookup"><span data-stu-id="4214c-p103">If the settings described in this section can't be found inside of GPMC, download the appropriate ADMX and copy them to the [central store](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-vista/cc748955%28v%3dws.10%29). Central store on the controller is a folder with the following naming convention:</span></span>
  
 <span data-ttu-id="4214c-137">**%systemroot%\sysvol\\<domain\>\policies\PolicyDefinitions**</span><span class="sxs-lookup"><span data-stu-id="4214c-137">**%systemroot%\sysvol\\<domain\>\policies\PolicyDefinitions**</span></span>
  
<span data-ttu-id="4214c-p104">每個網域控制站控點應取得個別的資料夾。若要從命令提示字元中 ADMX 檔案複製可用下列命令：</span><span class="sxs-lookup"><span data-stu-id="4214c-p104">Each domain your controller handles should get a separate folder. The following command can be used to copy the ADMX file from the command prompt:</span></span>
  
 `Copy <path_to_ADMX.ADMX> %systemroot%\sysvol\<domain>\policies\PolicyDefinitions`
  
1. <span data-ttu-id="4214c-140">若要編輯的任何現有原則或建立一個新參數和開啟 「 群組原則管理主控台 （gpmc.msc 取得）。</span><span class="sxs-lookup"><span data-stu-id="4214c-140">Open the Group Policy Management Console (gpmc.msc) and switch to editing any existing policy or creating a new one.</span></span>
    
2. <span data-ttu-id="4214c-141">請確定下列資料夾會出現在 [**系統管理範本**] 區段中的*使用者/電腦設定*這兩種： Google Chrome 及 Google Chrome-預設設定 （使用者可以覆寫）。</span><span class="sxs-lookup"><span data-stu-id="4214c-141">Make sure the following folders appear in the **Administrative Templates** section of both *User/Computer Configuration*: Google Chrome and Google Chrome - Default Settings (users can override).</span></span>
    
   - <span data-ttu-id="4214c-142">修正第一個區段的設定和本機系統管理員將無法對其進行變更。</span><span class="sxs-lookup"><span data-stu-id="4214c-142">The settings of the first section are fixed and the local administrator won't be able to change them.</span></span>
    
   - <span data-ttu-id="4214c-p105">在其瀏覽器設定的使用者可以變更的後面] 區段中的原則設定。您應該先決定使用者可以覆寫預設設定。下列步驟，在對應的資料夾中的設定變更為您的組織原則和需求。下列步驟使用的 Google Chrome-預設設定為預設值。</span><span class="sxs-lookup"><span data-stu-id="4214c-p105">The settings of the latter section of policies can be changed by users in their browser settings. You should decide if users can override your default setting. In the following steps, change in the setting in the folder that corresponds to your organization policy and needs. The steps below use the Google Chrome - Default Settings as the default.</span></span>
    
3. <span data-ttu-id="4214c-147">瀏覽至 [**&lt;電腦/使用者設定&gt;\Administrative Templates\Google Chrome-預設 Settings\Home 頁面**。</span><span class="sxs-lookup"><span data-stu-id="4214c-147">Navigate to **&lt;Computer/User Configuration&gt;\Administrative Templates\Google Chrome - Default Settings\Home Page**.</span></span>
    
4. <span data-ttu-id="4214c-148">連按兩下 [**首頁以使用新索引標籤頁面**，並將它設為 [**已啟用**。</span><span class="sxs-lookup"><span data-stu-id="4214c-148">Double-click **Use New Tab Page as homepage**, and set it to **Enabled**.</span></span>
    
5. <span data-ttu-id="4214c-149">瀏覽至 [**&lt;電腦/使用者設定&gt;\Administrative Templates\Google Chrome-預設 Settings\New] 索引標籤] 頁面上**。</span><span class="sxs-lookup"><span data-stu-id="4214c-149">Navigate to **&lt;Computer/User Configuration&gt;\Administrative Templates\Google Chrome - Default Settings\New Tab Page**.</span></span>
    
6. <span data-ttu-id="4214c-150">按兩下 [**設定新的索引標籤頁面 URL**，將它設為 [**已啟用**] 並輸入`https://www.bing.com/business?form=BFBSPR`</span><span class="sxs-lookup"><span data-stu-id="4214c-150">Double-click **Configure the New Tab Page URL**, set it to **Enabled**, and enter `https://www.bing.com/business?form=BFBSPR`</span></span>
    
7. <span data-ttu-id="4214c-151">強制產生 GPO 連結至適當的網域。</span><span class="sxs-lookup"><span data-stu-id="4214c-151">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>
    
<span data-ttu-id="4214c-152">使用者無法變更 [首頁] 頁面上設定此原則之後。</span><span class="sxs-lookup"><span data-stu-id="4214c-152">Users will be able to change the home page after this policy is set.</span></span>