---
title: 設定預設首頁
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
ms.assetid: c020bd72-9906-4dfd-bc77-57287f5927ce
description: 了解如何將 Bing 設定為您的公司使用 Microsoft Search 的預設瀏覽器。
ms.openlocfilehash: 72a6ba6737b6aeb7bf5ff852b44092f726ebd7d9
ms.sourcegitcommit: 3e91a6e70b48a0100adfed1b62ba79f2fd1735d2
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/13/2019
ms.locfileid: "34425653"
---
# <a name="set-default-homepage"></a><span data-ttu-id="421d6-103">設定預設首頁</span><span class="sxs-lookup"><span data-stu-id="421d6-103">Set default homepage</span></span>

> [!IMPORTANT]
> <span data-ttu-id="421d6-104">Bing 中的 Microsoft Search 設定現在可在 Microsoft 365 系統管理中心取得。</span><span class="sxs-lookup"><span data-stu-id="421d6-104">Microsoft Search in Bing settings are now available in the Microsoft 365 admin center.</span></span> <span data-ttu-id="421d6-105">從在系統管理中心[指派搜尋系統管理員](https://docs.microsoft.com/zh-TW/microsoftsearch/setup-microsoft-search#step-2-assign-search-admin-and-search-editor)開始。</span><span class="sxs-lookup"><span data-stu-id="421d6-105">Get started by [assigning search admins](https://docs.microsoft.com/en-us/microsoftsearch/setup-microsoft-search#step-2-assign-search-admin-and-search-editor) in your admin center.</span></span>
    
<span data-ttu-id="421d6-106">設定預設瀏覽器、預設搜尋引擎和預設首頁將可協助您的使用者探索 Microsoft Search 功能，鼓勵更常使用，並提供更順暢的體驗。</span><span class="sxs-lookup"><span data-stu-id="421d6-106">Configuring the default browser, default search engine, and default homepage will help your users discover Microsoft Search  capabilities, encourage more usage, and provide a smoother experience.</span></span>
  
<span data-ttu-id="421d6-107">若要為您的組織設定預設首頁，請依照以下步驟進行。</span><span class="sxs-lookup"><span data-stu-id="421d6-107">To set the default homepage for your organization, follow the steps below.</span></span>
  
## <a name="internet-explorer"></a><span data-ttu-id="421d6-108">Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="421d6-108">Internet Explorer</span></span>

### <a name="internet-explorer-50-or-later"></a><span data-ttu-id="421d6-109">Internet Explorer 5.0 或更新版</span><span class="sxs-lookup"><span data-stu-id="421d6-109">msoTargetBrowserIE5 . Microsoft Internet Explorer 5.0 or later.</span></span>

1. <span data-ttu-id="421d6-110">開啟 [群組原則管理主控台] (gpmc.msc)，然後切換以編輯任何現有原則或建立新原則。</span><span class="sxs-lookup"><span data-stu-id="421d6-110">Open the Group Policy Management Console (gpmc.msc) and switch to editing any existing policy or creating a new one.</span></span>
    
2. <span data-ttu-id="421d6-111">瀏覽至 [使用者設定]\[喜好設定]\[控制台設定]\[網際網路設定]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="421d6-111">Navigate to **User Configuration\Preferences\Control Panel Settings\Internet Settings**.</span></span>
    
3. <span data-ttu-id="421d6-112">以滑鼠右鍵按一下 [網際網路設定]\*\*\*\*，然後選取 [Internet Explorer 10]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="421d6-112">Right-click on **Internet Settings** and select **Internet Explorer 10**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="421d6-113">您需要選取 Internet Explorer 10 的選項來為 Internet Explorer 11 套用設定，因為同一個設定也適用 Internet Explorer 11。</span><span class="sxs-lookup"><span data-stu-id="421d6-113">You need to select the option of Internet Explorer 10 to apply the settings for Internet Explorer 11 as the same settings apply to Internet Explorer 11.</span></span> 
  
4. <span data-ttu-id="421d6-114">以紅色底線標示的設定表示沒有在目標電腦上設定，以綠色底線標示的設定則表示已經在目標電腦上設定。</span><span class="sxs-lookup"><span data-stu-id="421d6-114">Settings which are underlined in red are not configured at the target machine, while settings underlined in green are configured at the target machine.</span></span> <span data-ttu-id="421d6-115">若要變更底線，請使用以下列功能鍵：</span><span class="sxs-lookup"><span data-stu-id="421d6-115">To change the underlining, use the following function keys:</span></span>
    
    <span data-ttu-id="421d6-116">F5 - 啟用目前索引標籤上的所有設定</span><span class="sxs-lookup"><span data-stu-id="421d6-116">F5 - Enable all settings on the current tab</span></span>
    
    <span data-ttu-id="421d6-117">F6 - 啟用目前選取的設定</span><span class="sxs-lookup"><span data-stu-id="421d6-117">F6 - Enable the currently selected setting</span></span>
    
    <span data-ttu-id="421d6-118">F7 - 停用目前選取的設定</span><span class="sxs-lookup"><span data-stu-id="421d6-118">F7 - Disable the currently selected setting</span></span>
    
    <span data-ttu-id="421d6-119">F8 - 停用目前索引標籤上的所有設定</span><span class="sxs-lookup"><span data-stu-id="421d6-119">F8 - Disable all settings on the current tab</span></span>
    
5. <span data-ttu-id="421d6-120">在進行任何設定之前，請先按 **F8** 以停用所有設定。</span><span class="sxs-lookup"><span data-stu-id="421d6-120">Press **F8** to disable all settings before configuring anything.</span></span> <span data-ttu-id="421d6-121">畫面看起來應該像這樣：</span><span class="sxs-lookup"><span data-stu-id="421d6-121">The screen should look like this:</span></span> 
    
    ![Internet Explorer 10 [內容] 對話方塊](media/2fd55755-5007-4e33-a795-c42ce2fcef4a.jpg)
  
6. <span data-ttu-id="421d6-123">在首頁設定上按下 **F6**，然後輸入 `https://www.bing.com/business?form=BFBSPR`</span><span class="sxs-lookup"><span data-stu-id="421d6-123">Press **F6** on the Home page setting and enter `https://www.bing.com/business?form=BFBSPR`</span></span>
    
7. <span data-ttu-id="421d6-124">將結果 GPO 連結到適當網域以強制執行結果 GPO。</span><span class="sxs-lookup"><span data-stu-id="421d6-124">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>
    
> [!NOTE]
> <span data-ttu-id="421d6-125">設定此原則之後，使用者仍可變更首頁。</span><span class="sxs-lookup"><span data-stu-id="421d6-125">Users can still change the homepage after this policy is set.</span></span> 
  
## <a name="microsoft-edge"></a><span data-ttu-id="421d6-126">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="421d6-126">Microsoft Edge</span></span>

### <a name="windows-10-version-1511-or-later"></a><span data-ttu-id="421d6-127">Windows 10 (版本 1511 或更新版本)</span><span class="sxs-lookup"><span data-stu-id="421d6-127">Windows 10, Version 1511 or later</span></span>

1. <span data-ttu-id="421d6-128">開啟 [群組原則管理主控台] (gpmc.msc)，然後切換以編輯任何現有原則或建立新原則。</span><span class="sxs-lookup"><span data-stu-id="421d6-128">Open the Group Policy Management Console (gpmc.msc) and switch to editing any existing policy or creating a new one.</span></span>
    
2. <span data-ttu-id="421d6-129">瀏覽至 [系統管理範本]\[Windows 元件]\[Microsoft Edge]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="421d6-129">Navigate to **Administrative Templates\Windows Components\Microsoft Edge**</span></span>
    
1. <span data-ttu-id="421d6-130">按兩下 [設定起始頁面]\*\*\*\*，將它設為 [已啟用]\*\*\*\*，然後輸入 `https://www.bing.com/business`</span><span class="sxs-lookup"><span data-stu-id="421d6-130">Double-click **Configure Start pages**, set it to **Enabled**, and enter `https://www.bing.com/business`</span></span>
    
3. <span data-ttu-id="421d6-131">將結果 GPO 連結到適當網域以強制執行結果 GPO。</span><span class="sxs-lookup"><span data-stu-id="421d6-131">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>
    
> [!CAUTION]
> <span data-ttu-id="421d6-132">設定此原則之後，使用者將無法變更搜尋提供者。</span><span class="sxs-lookup"><span data-stu-id="421d6-132">Users won't be able to change the search provider after this policy is set.</span></span> 
  
## <a name="google-chrome"></a><span data-ttu-id="421d6-133">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="421d6-133">Google Chrome</span></span>

### <a name="windows-xp-sp2-or-later"></a><span data-ttu-id="421d6-134">Windows XP SP2 或更新版本</span><span class="sxs-lookup"><span data-stu-id="421d6-134">Windows XP SP2 or later</span></span>

<span data-ttu-id="421d6-135">您可以在 [Microsoft 支援](https://support.microsoft.com/zh-TW/help/3087759/how-to-create-and-manage-the-central-store-for-group-policy-administra)網站上找到有關管理 ADMX 檔案的 Windows 支援文章和不同版本 Windows 適用的最新 ADMX 檔案。</span><span class="sxs-lookup"><span data-stu-id="421d6-135">The Windows Support article on managing ADMX files and the latest ADMX files for different versions of Windows can be found [on Microsoft Support](https://support.microsoft.com/en-us/help/3087759/how-to-create-and-manage-the-central-store-for-group-policy-administra).</span></span>

<span data-ttu-id="421d6-136">您也將需要最新的 Google 原則檔案，可以在 [Google Chrome Enterprise 說明](https://support.google.com/chrome/a/answer/187202)上找到。</span><span class="sxs-lookup"><span data-stu-id="421d6-136">You'll also need the latest Google policy file, which you can find on [Google Chrome Enterprise Help](https://support.google.com/chrome/a/answer/187202).</span></span>
  
<span data-ttu-id="421d6-137">如果在 GPMC 中找不到本節中描述的設定，請下載適當的 ADMX 並將它們複製到[集中存放區](https://docs.microsoft.com/zh-TW/previous-versions/windows/it-pro/windows-vista/cc748955%28v%3dws.10%29)。</span><span class="sxs-lookup"><span data-stu-id="421d6-137">If the settings described in this section can't be found inside of GPMC, download the appropriate ADMX and copy them to the [central store](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-vista/cc748955%28v%3dws.10%29).</span></span> <span data-ttu-id="421d6-138">控制器上的集中存放區是使用下列命名慣例的資料夾：</span><span class="sxs-lookup"><span data-stu-id="421d6-138">Central store on the controller is a folder with the following naming convention:</span></span>
  
 <span data-ttu-id="421d6-139">**%systemroot%\sysvol\\<domain\>\policies\PolicyDefinitions**</span><span class="sxs-lookup"><span data-stu-id="421d6-139">**%systemroot%\sysvol\\<domain\>\policies\PolicyDefinitions**</span></span>
  
<span data-ttu-id="421d6-140">控制站處理的每個網域都應該有個別的資料夾。</span><span class="sxs-lookup"><span data-stu-id="421d6-140">Each domain your controller handles should get a separate folder.</span></span> <span data-ttu-id="421d6-141">可以透過命令提示字元使用下列命令來複製 ADMX 檔案：</span><span class="sxs-lookup"><span data-stu-id="421d6-141">The following command can be used to copy the ADMX file from the command prompt:</span></span>
  
 `Copy <path_to_ADMX.ADMX> %systemroot%\sysvol\<domain>\policies\PolicyDefinitions`
  
1. <span data-ttu-id="421d6-142">開啟 [群組原則管理主控台] (gpmc.msc)，然後切換以編輯任何現有原則或建立新原則。</span><span class="sxs-lookup"><span data-stu-id="421d6-142">Open the Group Policy Management Console (gpmc.msc) and switch to editing any existing policy or creating a new one.</span></span>
    
2. <span data-ttu-id="421d6-143">確定在 [使用者設定]/[電腦設定]\*\* 中的 [系統管理範本]\*\*\*\* 區段中都有下列資料夾：Google Chrome 和 Google Chrome - 預設設定 (使用者可以覆寫)。</span><span class="sxs-lookup"><span data-stu-id="421d6-143">Make sure the following folders appear in the **Administrative Templates** section of both *User/Computer Configuration*: Google Chrome and Google Chrome - Default Settings (users can override).</span></span>
    
   - <span data-ttu-id="421d6-144">第一個區段的設定是固定的，而且本機系統管理員無法變更它們。</span><span class="sxs-lookup"><span data-stu-id="421d6-144">The settings of the first section are fixed and the local administrator won't be able to change them.</span></span>
    
   - <span data-ttu-id="421d6-145">使用者可以在瀏覽器設定中變更原則後面區段的設定。</span><span class="sxs-lookup"><span data-stu-id="421d6-145">The settings of the latter section of policies can be changed by users in their browser settings.</span></span>
   <span data-ttu-id="421d6-146">您應該決定使用者是否可以覆寫您的預設設定。</span><span class="sxs-lookup"><span data-stu-id="421d6-146">You should decide if users can override your default setting.</span></span> <span data-ttu-id="421d6-147">在以下步驟中，在與您的組織政策和需求對應資料夾中的設定進行變更。</span><span class="sxs-lookup"><span data-stu-id="421d6-147">In the following steps, change in the setting in the folder that corresponds to your organization policy and needs.</span></span> <span data-ttu-id="421d6-148">以下步驟會使用 Google Chrome - 預設設定做為預設值。</span><span class="sxs-lookup"><span data-stu-id="421d6-148">The steps below use the Google Chrome - Default Settings as the default.</span></span>
    
3. <span data-ttu-id="421d6-149">瀏覽至 [&gt;電腦/使用者設定**]>\[系統管理範本]\[Google Chrome - 預設設定]\[首頁]**&lt;。</span><span class="sxs-lookup"><span data-stu-id="421d6-149">Navigate to **&lt;Computer/User Configuration&gt;\Administrative Templates\Google Chrome - Default Settings\Home Page**.</span></span>
    
4. <span data-ttu-id="421d6-150">按兩下 [將新分頁設為首頁]\*\*\*\*，然後將它設為 [已啟用]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="421d6-150">Double-click **Use New Tab Page as homepage**, and set it to **Enabled**.</span></span>
    
5. <span data-ttu-id="421d6-151">瀏覽至 [&lt;電腦/使用者設定&gt;]\[系統管理範本]\[Google Chrome - 預設設定]\[新分頁]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="421d6-151">Navigate to **&lt;Computer/User Configuration&gt;\Administrative Templates\Google Chrome - Default Settings\New Tab Page**.</span></span>
    
6. <span data-ttu-id="421d6-152">按兩下 [設定新分頁 URL]\*\*\*\*，將它設為 [已啟用]\*\*\*\*，然後輸入 `https://www.bing.com/business?form=BFBSPR`</span><span class="sxs-lookup"><span data-stu-id="421d6-152">Double-click **Configure the New Tab Page URL**, set it to **Enabled**, and enter `https://www.bing.com/business?form=BFBSPR`</span></span>
    
7. <span data-ttu-id="421d6-153">將結果 GPO 連結到適當網域以強制執行結果 GPO。</span><span class="sxs-lookup"><span data-stu-id="421d6-153">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>
    
<span data-ttu-id="421d6-154">設定此原則之後，使用者將能夠變更首頁。</span><span class="sxs-lookup"><span data-stu-id="421d6-154">Users will be able to change the home page after this policy is set.</span></span>