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
ROBOTS: NOINDEX
description: 了解如何將 Bing 設定為您的公司使用 Microsoft Search 的預設瀏覽器。
ms.openlocfilehash: 457202ba8dbebf59c5ef6a4630aea98304b9acdb
ms.sourcegitcommit: fe7f3dae4edba97071a4d127e8a27bdf4fa00d81
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/05/2019
ms.locfileid: "34727994"
---
# <a name="set-default-homepage"></a><span data-ttu-id="bf84d-103">設定預設首頁</span><span class="sxs-lookup"><span data-stu-id="bf84d-103">Set default homepage</span></span>

<span data-ttu-id="bf84d-104">設定預設瀏覽器、預設搜尋引擎和預設首頁將可協助您的使用者探索 Microsoft Search 功能，鼓勵更常使用，並提供更順暢的體驗。</span><span class="sxs-lookup"><span data-stu-id="bf84d-104">Configuring the default browser, default search engine, and default homepage will help your users discover Microsoft Search  capabilities, encourage more usage, and provide a smoother experience.</span></span>
  
<span data-ttu-id="bf84d-105">若要為您的組織設定預設首頁，請依照以下步驟進行。</span><span class="sxs-lookup"><span data-stu-id="bf84d-105">To set the default homepage for your organization, follow the steps below.</span></span>
  
## <a name="internet-explorer"></a><span data-ttu-id="bf84d-106">Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="bf84d-106">Internet Explorer</span></span>

### <a name="internet-explorer-50-or-later"></a><span data-ttu-id="bf84d-107">Internet Explorer 5.0 或更新版</span><span class="sxs-lookup"><span data-stu-id="bf84d-107">msoTargetBrowserIE5 . Microsoft Internet Explorer 5.0 or later.</span></span>

1. <span data-ttu-id="bf84d-108">開啟 [群組原則管理主控台] (gpmc.msc)，然後切換以編輯任何現有原則或建立新原則。</span><span class="sxs-lookup"><span data-stu-id="bf84d-108">Open the Group Policy Management Console (gpmc.msc) and switch to editing any existing policy or creating a new one.</span></span>
    
2. <span data-ttu-id="bf84d-109">瀏覽至 [使用者設定]\[喜好設定]\[控制台設定]\[網際網路設定]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="bf84d-109">Navigate to **User Configuration\Preferences\Control Panel Settings\Internet Settings**.</span></span>
    
3. <span data-ttu-id="bf84d-110">以滑鼠右鍵按一下 [網際網路設定]\*\*\*\*，然後選取 [Internet Explorer 10]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="bf84d-110">Right-click on **Internet Settings** and select **Internet Explorer 10**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="bf84d-111">您需要選取 Internet Explorer 10 的選項來為 Internet Explorer 11 套用設定，因為同一個設定也適用 Internet Explorer 11。</span><span class="sxs-lookup"><span data-stu-id="bf84d-111">You need to select the option of Internet Explorer 10 to apply the settings for Internet Explorer 11 as the same settings apply to Internet Explorer 11.</span></span> 
  
4. <span data-ttu-id="bf84d-112">以紅色底線標示的設定表示沒有在目標電腦上設定，以綠色底線標示的設定則表示已經在目標電腦上設定。</span><span class="sxs-lookup"><span data-stu-id="bf84d-112">Settings which are underlined in red are not configured at the target machine, while settings underlined in green are configured at the target machine.</span></span> <span data-ttu-id="bf84d-113">若要變更底線，請使用以下列功能鍵：</span><span class="sxs-lookup"><span data-stu-id="bf84d-113">To change the underlining, use the following function keys:</span></span>
    
    <span data-ttu-id="bf84d-114">F5 - 啟用目前索引標籤上的所有設定</span><span class="sxs-lookup"><span data-stu-id="bf84d-114">F5 - Enable all settings on the current tab</span></span>
    
    <span data-ttu-id="bf84d-115">F6 - 啟用目前選取的設定</span><span class="sxs-lookup"><span data-stu-id="bf84d-115">F6 - Enable the currently selected setting</span></span>
    
    <span data-ttu-id="bf84d-116">F7 - 停用目前選取的設定</span><span class="sxs-lookup"><span data-stu-id="bf84d-116">F7 - Disable the currently selected setting</span></span>
    
    <span data-ttu-id="bf84d-117">F8 - 停用目前索引標籤上的所有設定</span><span class="sxs-lookup"><span data-stu-id="bf84d-117">F8 - Disable all settings on the current tab</span></span>
    
5. <span data-ttu-id="bf84d-118">在進行任何設定之前，請先按 **F8** 以停用所有設定。</span><span class="sxs-lookup"><span data-stu-id="bf84d-118">Press **F8** to disable all settings before configuring anything.</span></span> <span data-ttu-id="bf84d-119">畫面看起來應該像這樣：</span><span class="sxs-lookup"><span data-stu-id="bf84d-119">The screen should look like this:</span></span> 
    
    ![Internet Explorer 10 [內容] 對話方塊](media/2fd55755-5007-4e33-a795-c42ce2fcef4a.jpg)
  
6. <span data-ttu-id="bf84d-121">在首頁設定上按下 **F6**，然後輸入 `https://www.bing.com/business?form=BFBSPR`</span><span class="sxs-lookup"><span data-stu-id="bf84d-121">Press **F6** on the Home page setting and enter `https://www.bing.com/business?form=BFBSPR`</span></span>
    
7. <span data-ttu-id="bf84d-122">將結果 GPO 連結到適當網域以強制執行結果 GPO。</span><span class="sxs-lookup"><span data-stu-id="bf84d-122">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>
    
> [!NOTE]
> <span data-ttu-id="bf84d-123">設定此原則之後，使用者仍可變更首頁。</span><span class="sxs-lookup"><span data-stu-id="bf84d-123">Users can still change the homepage after this policy is set.</span></span> 
  
## <a name="microsoft-edge"></a><span data-ttu-id="bf84d-124">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="bf84d-124">Microsoft Edge</span></span>

### <a name="windows-10-version-1511-or-later"></a><span data-ttu-id="bf84d-125">Windows 10 (版本 1511 或更新版本)</span><span class="sxs-lookup"><span data-stu-id="bf84d-125">Windows 10, Version 1511 or later</span></span>

1. <span data-ttu-id="bf84d-126">開啟 [群組原則管理主控台] (gpmc.msc)，然後切換以編輯任何現有原則或建立新原則。</span><span class="sxs-lookup"><span data-stu-id="bf84d-126">Open the Group Policy Management Console (gpmc.msc) and switch to editing any existing policy or creating a new one.</span></span>
    
2. <span data-ttu-id="bf84d-127">瀏覽至 [系統管理範本]\[Windows 元件]\[Microsoft Edge]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="bf84d-127">Navigate to **Administrative Templates\Windows Components\Microsoft Edge**</span></span>
    
1. <span data-ttu-id="bf84d-128">按兩下 [設定起始頁面]\*\*\*\*，將它設為 [已啟用]\*\*\*\*，然後輸入 `https://www.bing.com/business`</span><span class="sxs-lookup"><span data-stu-id="bf84d-128">Double-click **Configure Start pages**, set it to **Enabled**, and enter `https://www.bing.com/business`</span></span>
    
3. <span data-ttu-id="bf84d-129">將結果 GPO 連結到適當網域以強制執行結果 GPO。</span><span class="sxs-lookup"><span data-stu-id="bf84d-129">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>
    
> [!CAUTION]
> <span data-ttu-id="bf84d-130">設定此原則之後，使用者將無法變更搜尋提供者。</span><span class="sxs-lookup"><span data-stu-id="bf84d-130">Users won't be able to change the search provider after this policy is set.</span></span> 
  
## <a name="google-chrome"></a><span data-ttu-id="bf84d-131">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="bf84d-131">Google Chrome</span></span>

### <a name="windows-xp-sp2-or-later"></a><span data-ttu-id="bf84d-132">Windows XP SP2 或更新版本</span><span class="sxs-lookup"><span data-stu-id="bf84d-132">Windows XP SP2 or later</span></span>

<span data-ttu-id="bf84d-133">您可以在 [Microsoft 支援](https://support.microsoft.com/zh-TW/help/3087759/how-to-create-and-manage-the-central-store-for-group-policy-administra)網站上找到有關管理 ADMX 檔案的 Windows 支援文章和不同版本 Windows 適用的最新 ADMX 檔案。</span><span class="sxs-lookup"><span data-stu-id="bf84d-133">The Windows Support article on managing ADMX files and the latest ADMX files for different versions of Windows can be found [on Microsoft Support](https://support.microsoft.com/en-us/help/3087759/how-to-create-and-manage-the-central-store-for-group-policy-administra).</span></span>

<span data-ttu-id="bf84d-134">您也將需要最新的 Google 原則檔案，可以在 [Google Chrome Enterprise 說明](https://support.google.com/chrome/a/answer/187202)上找到。</span><span class="sxs-lookup"><span data-stu-id="bf84d-134">You'll also need the latest Google policy file, which you can find on [Google Chrome Enterprise Help](https://support.google.com/chrome/a/answer/187202).</span></span>
  
<span data-ttu-id="bf84d-135">如果在 GPMC 中找不到本節中描述的設定，請下載適當的 ADMX 並將它們複製到[集中存放區](https://docs.microsoft.com/zh-TW/previous-versions/windows/it-pro/windows-vista/cc748955%28v%3dws.10%29)。</span><span class="sxs-lookup"><span data-stu-id="bf84d-135">If the settings described in this section can't be found inside of GPMC, download the appropriate ADMX and copy them to the [central store](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-vista/cc748955%28v%3dws.10%29).</span></span> <span data-ttu-id="bf84d-136">控制器上的集中存放區是使用下列命名慣例的資料夾：</span><span class="sxs-lookup"><span data-stu-id="bf84d-136">Central store on the controller is a folder with the following naming convention:</span></span>
  
 <span data-ttu-id="bf84d-137">**%systemroot%\sysvol\\<domain\>\policies\PolicyDefinitions**</span><span class="sxs-lookup"><span data-stu-id="bf84d-137">**%systemroot%\sysvol\\<domain\>\policies\PolicyDefinitions**</span></span>
  
<span data-ttu-id="bf84d-138">控制站處理的每個網域都應該有個別的資料夾。</span><span class="sxs-lookup"><span data-stu-id="bf84d-138">Each domain your controller handles should get a separate folder.</span></span> <span data-ttu-id="bf84d-139">可以透過命令提示字元使用下列命令來複製 ADMX 檔案：</span><span class="sxs-lookup"><span data-stu-id="bf84d-139">The following command can be used to copy the ADMX file from the command prompt:</span></span>
  
 `Copy <path_to_ADMX.ADMX> %systemroot%\sysvol\<domain>\policies\PolicyDefinitions`
  
1. <span data-ttu-id="bf84d-140">開啟 [群組原則管理主控台] (gpmc.msc)，然後切換以編輯任何現有原則或建立新原則。</span><span class="sxs-lookup"><span data-stu-id="bf84d-140">Open the Group Policy Management Console (gpmc.msc) and switch to editing any existing policy or creating a new one.</span></span>
    
2. <span data-ttu-id="bf84d-141">確定在 [使用者設定]/[電腦設定]\*\* 中的 [系統管理範本]\*\*\*\* 區段中都有下列資料夾：Google Chrome 和 Google Chrome - 預設設定 (使用者可以覆寫)。</span><span class="sxs-lookup"><span data-stu-id="bf84d-141">Make sure the following folders appear in the **Administrative Templates** section of both *User/Computer Configuration*: Google Chrome and Google Chrome - Default Settings (users can override).</span></span>
    
   - <span data-ttu-id="bf84d-142">第一個區段的設定是固定的，而且本機系統管理員無法變更它們。</span><span class="sxs-lookup"><span data-stu-id="bf84d-142">The settings of the first section are fixed and the local administrator won't be able to change them.</span></span>
    
   - <span data-ttu-id="bf84d-143">使用者可以在瀏覽器設定中變更原則後面區段的設定。</span><span class="sxs-lookup"><span data-stu-id="bf84d-143">The settings of the latter section of policies can be changed by users in their browser settings.</span></span>
   <span data-ttu-id="bf84d-144">您應該決定使用者是否可以覆寫您的預設設定。</span><span class="sxs-lookup"><span data-stu-id="bf84d-144">You should decide if users can override your default setting.</span></span> <span data-ttu-id="bf84d-145">在以下步驟中，在與您的組織政策和需求對應資料夾中的設定進行變更。</span><span class="sxs-lookup"><span data-stu-id="bf84d-145">In the following steps, change in the setting in the folder that corresponds to your organization policy and needs.</span></span> <span data-ttu-id="bf84d-146">以下步驟會使用 Google Chrome - 預設設定做為預設值。</span><span class="sxs-lookup"><span data-stu-id="bf84d-146">The steps below use the Google Chrome - Default Settings as the default.</span></span>
    
3. <span data-ttu-id="bf84d-147">瀏覽至 [&gt;電腦/使用者設定**]>\[系統管理範本]\[Google Chrome - 預設設定]\[首頁]**&lt;。</span><span class="sxs-lookup"><span data-stu-id="bf84d-147">Navigate to **&lt;Computer/User Configuration&gt;\Administrative Templates\Google Chrome - Default Settings\Home Page**.</span></span>
    
4. <span data-ttu-id="bf84d-148">按兩下 [將新分頁設為首頁]\*\*\*\*，然後將它設為 [已啟用]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="bf84d-148">Double-click **Use New Tab Page as homepage**, and set it to **Enabled**.</span></span>
    
5. <span data-ttu-id="bf84d-149">瀏覽至 [&lt;電腦/使用者設定&gt;]\[系統管理範本]\[Google Chrome - 預設設定]\[新分頁]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="bf84d-149">Navigate to **&lt;Computer/User Configuration&gt;\Administrative Templates\Google Chrome - Default Settings\New Tab Page**.</span></span>
    
6. <span data-ttu-id="bf84d-150">按兩下 [設定新分頁 URL]\*\*\*\*，將它設為 [已啟用]\*\*\*\*，然後輸入 `https://www.bing.com/business?form=BFBSPR`</span><span class="sxs-lookup"><span data-stu-id="bf84d-150">Double-click **Configure the New Tab Page URL**, set it to **Enabled**, and enter `https://www.bing.com/business?form=BFBSPR`</span></span>
    
7. <span data-ttu-id="bf84d-151">將結果 GPO 連結到適當網域以強制執行結果 GPO。</span><span class="sxs-lookup"><span data-stu-id="bf84d-151">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>
    
<span data-ttu-id="bf84d-152">設定此原則之後，使用者將能夠變更首頁。</span><span class="sxs-lookup"><span data-stu-id="bf84d-152">Users will be able to change the home page after this policy is set.</span></span>