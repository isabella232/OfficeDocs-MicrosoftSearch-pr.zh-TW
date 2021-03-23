---
title: 設定預設搜尋引擎
ms.author: jeffkizn
author: jeffkizn
manager: parulm
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: ee40010e-5d7f-4ba8-a3f8-d240dab3af6d
description: 了解如何將 Bing 設定為公司使用 Microsoft Search 的預設搜尋引擎。
ms.openlocfilehash: 346bf3bf2da10178a8bd19390920db2d9de2629e
ms.sourcegitcommit: 5df252e6d0bd67bb1b4c59418aceca8369f5fe42
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/23/2021
ms.locfileid: "51031753"
---
# <a name="make-bing-the-default-search-engine"></a><span data-ttu-id="80a20-103">讓 Bing 成為預設搜尋引擎</span><span class="sxs-lookup"><span data-stu-id="80a20-103">Make Bing the default search engine</span></span>
  
<span data-ttu-id="80a20-104">本文將說明如何讓 Bing 成為 Microsoft Edge、Google Chrome 和 Internet Explorer 的預設搜尋引擎。</span><span class="sxs-lookup"><span data-stu-id="80a20-104">This article explains how you can make Bing the default search engine for Microsoft Edge, Google Chrome, and Internet Explorer.</span></span> 
  
## <a name="microsoft-edge-on-windows-10-version-1703-or-later"></a><span data-ttu-id="80a20-105">Windows 10 版本 1703 或更新版本上的 Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="80a20-105">Microsoft Edge on Windows 10, Version 1703 or later</span></span>

<span data-ttu-id="80a20-106">雖然您可以將 Bing 設定為預設的搜尋引擎，Microsoft Edge 可讓使用者變更其設定，以使用不同的搜尋引擎。</span><span class="sxs-lookup"><span data-stu-id="80a20-106">Although you'll set Bing as the default search engine, Microsoft Edge allows users to change their settings to use a different search engine.</span></span>
  
<span data-ttu-id="80a20-107">如需適用於其他版本 Windows 的最新 ADMX 檔案，請參閱[如何在 Windows 中建立和管理群組原則系統管理範本的集中存放區](https://support.microsoft.com/help/3087759/how-to-create-and-manage-the-central-store-for-group-policy-administra)。</span><span class="sxs-lookup"><span data-stu-id="80a20-107">For the latest ADMX files for various versions of Windows, see [How to create and manage the Central Store for Group Policy Administrative Templates in Windows](https://support.microsoft.com/help/3087759/how-to-create-and-manage-the-central-store-for-group-policy-administra).</span></span>
  
<span data-ttu-id="80a20-108">如果在 GPMC 中找不到本節中描述的設定，請下載適當的 ADMX 並將它們複製到集中存放區。</span><span class="sxs-lookup"><span data-stu-id="80a20-108">If the setting described in this section cannot be found inside of GPMC, download the appropriate ADMX and copy them to the central store.</span></span> <span data-ttu-id="80a20-109">如需詳細資訊，請參閱使用 [ADMX 檔案編輯網域型 GPO](/previous-versions/windows/it-pro/windows-vista/cc748955%28v%3dws.10%29)。</span><span class="sxs-lookup"><span data-stu-id="80a20-109">For more information, see [Editing Domain-Based GPOs Using ADMX Files](/previous-versions/windows/it-pro/windows-vista/cc748955%28v%3dws.10%29).</span></span> <span data-ttu-id="80a20-110">控制器上的中央存放區是具有下列命名慣例的資料夾： **%systemroot%\sysvol \\<網域 \> \policies\PolicyDefinitions**</span><span class="sxs-lookup"><span data-stu-id="80a20-110">Central store on the controller is a folder with the following naming convention: **%systemroot%\sysvol\\<domain\>\policies\PolicyDefinitions**</span></span>
  
<span data-ttu-id="80a20-111">控制站處理的每個網域都應該有個別的資料夾。</span><span class="sxs-lookup"><span data-stu-id="80a20-111">Each domain that your controller handles should get a separate folder.</span></span> <span data-ttu-id="80a20-112">可以透過命令提示字元使用下列命令來複製 ADMX 檔案：</span><span class="sxs-lookup"><span data-stu-id="80a20-112">The following command can be used to copy the ADMX file from the command prompt:</span></span>
  
 `Copy <path_to_ADMX.ADMX> %systemroot%\sysvol\<domain>\policies\PolicyDefinitions`
  
1. <span data-ttu-id="80a20-113">開啟 [群組原則管理主控台] (gpmc.msc)，然後切換以編輯現有原則或建立新原則。</span><span class="sxs-lookup"><span data-stu-id="80a20-113">Open the Group Policy Management Console (gpmc.msc) and switch to editing an existing policy or creating a new one.</span></span>
2. <span data-ttu-id="80a20-114">瀏覽至 **[電腦/使用者設定]&lt;&gt;\[系統管理範本]\[Windows 元件]\[Microsoft Edge]**。</span><span class="sxs-lookup"><span data-stu-id="80a20-114">Navigate to **&lt;Computer/User Configuration&gt;\Administrative Templates\Windows Components\Microsoft Edge**.</span></span>
3. <span data-ttu-id="80a20-115">按兩下 [設定預設搜索引擎]，將它設為 [已啟用]，然後輸入 `https://www.bing.com/sa/osd/bfb.xml`</span><span class="sxs-lookup"><span data-stu-id="80a20-115">Double-click **Set default search engine**, set to **Enabled**, and enter `https://www.bing.com/sa/osd/bfb.xml`</span></span>
4. <span data-ttu-id="80a20-116">將結果 GPO 連結到適當網域以強制執行結果 GPO。</span><span class="sxs-lookup"><span data-stu-id="80a20-116">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>


## <a name="google-chrome-on-windows-10-version-1507-or-later"></a><span data-ttu-id="80a20-117">Windows 10 上的 Google Chrome，版本1507或更新版本</span><span class="sxs-lookup"><span data-stu-id="80a20-117">Google Chrome on Windows 10, Version 1507 or later</span></span>

<span data-ttu-id="80a20-118">設定此原則之後，使用者將無法變更預設的搜尋引擎。</span><span class="sxs-lookup"><span data-stu-id="80a20-118">Users won't be able to change the default search engine after this policy is set.</span></span>
  
<span data-ttu-id="80a20-119">Chrome 隨附自己的一組群組原則設定，您可以從 [Google Chrome Enterprise 說明](https://support.google.com/chrome/a/answer/187202)以 ADMX 檔案的格式下載。</span><span class="sxs-lookup"><span data-stu-id="80a20-119">Chrome comes with its own set of group policy settings which can be downloaded in the form of an ADMX file from [Google Chrome Enterprise Help](https://support.google.com/chrome/a/answer/187202).</span></span>
  
<span data-ttu-id="80a20-120">針對網域控制站上的 ADMX 檔案，將範本檔案複製到集中存放區。</span><span class="sxs-lookup"><span data-stu-id="80a20-120">Copy the template file to a central store for ADMX files on the domain controller.</span></span> <span data-ttu-id="80a20-121">如需詳細資訊，請參閱使用 [ADMX 檔案編輯網域型 GPO](/previous-versions/windows/it-pro/windows-vista/cc748955%28v%3dws.10%29)。</span><span class="sxs-lookup"><span data-stu-id="80a20-121">For more information, see [Editing Domain-Based GPOs Using ADMX Files](/previous-versions/windows/it-pro/windows-vista/cc748955%28v%3dws.10%29).</span></span> <span data-ttu-id="80a20-122">控制器上的中央存放區是具有下列命名慣例的資料夾： **%systemroot%\sysvol \\<網域 \> \policies\PolicyDefinitions**</span><span class="sxs-lookup"><span data-stu-id="80a20-122">Central store on the controller is a folder with the following naming convention: **%systemroot%\sysvol\\<domain\>\policies\PolicyDefinitions**</span></span>
  
<span data-ttu-id="80a20-123">控制站處理的每個網域都應該有個別的資料夾。</span><span class="sxs-lookup"><span data-stu-id="80a20-123">Each domain that your controller handles should get a separate folder.</span></span> <span data-ttu-id="80a20-124">可以透過命令提示字元使用下列命令來複製 ADMX 檔案：</span><span class="sxs-lookup"><span data-stu-id="80a20-124">The following command can be used to copy the ADMX file from the command prompt:</span></span>
  
 `Copy <path_to_Chrome.ADMX> %systemroot%\sysvol\<domain>\policies\PolicyDefinitions`
  
1. <span data-ttu-id="80a20-125">開啟 [群組原則管理主控台] (gpmc.msc)，然後切換以編輯任何現有原則或建立新原則。</span><span class="sxs-lookup"><span data-stu-id="80a20-125">Open the Group Policy Management Console (gpmc.msc) and switch to editing any existing policy or creating a new one.</span></span>
2. <span data-ttu-id="80a20-126">確定在 [使用者設定]/[電腦設定] 中的 [系統管理範本] 區段中都有下列資料夾：Google Chrome 和 Google Chrome - 預設設定。</span><span class="sxs-lookup"><span data-stu-id="80a20-126">Make sure the following folders appear in the Administrative Templates section of both User/Computer Configuration: Google Chrome and Google Chrome - Default Settings.</span></span>

    - <span data-ttu-id="80a20-127">第一個區段的設定是固定的，而且本機系統管理員無法在瀏覽器中變更它們。</span><span class="sxs-lookup"><span data-stu-id="80a20-127">The settings of the first section are fixed and local administrators won't be able to change them in the browser.</span></span>
    - <span data-ttu-id="80a20-128">使用者可以在瀏覽器設定中變更原則後面區段的設定。</span><span class="sxs-lookup"><span data-stu-id="80a20-128">The settings of the latter section of policies can be changed by users in the browser settings.</span></span>

3. <span data-ttu-id="80a20-129">流覽至 **\<Computer/User\> Configuration\Administrative Templates\Google Chrome\Default 搜尋提供者**</span><span class="sxs-lookup"><span data-stu-id="80a20-129">Navigate to **\<Computer/User\> Configuration\Administrative Templates\Google Chrome\Default search provider**</span></span>
4. <span data-ttu-id="80a20-130">按兩下 [啟用預設搜尋引擎]，然後設為 [已啟用]。</span><span class="sxs-lookup"><span data-stu-id="80a20-130">Double-click **Enable the default search provider**, and set it to **Enabled**.</span></span>
5. <span data-ttu-id="80a20-131">按兩下 [預設搜尋提供者圖示]，將它設為 [已啟用]，然後輸入 `https://www.bing.com/sa/simg/bb.ico`</span><span class="sxs-lookup"><span data-stu-id="80a20-131">Double-click **Default search provider icon**, set it to **Enabled**, and enter `https://www.bing.com/sa/simg/bb.ico`</span></span>
6. <span data-ttu-id="80a20-132">按兩下 [預設搜尋提供者立即 URL]，然後輸入 `https://www.bing.com/business/search?q={searchTerms}&amp;form=BFBSPR`</span><span class="sxs-lookup"><span data-stu-id="80a20-132">Double-click **Default search provider instant URL**, and enter `https://www.bing.com/business/search?q={searchTerms}&amp;form=BFBSPR`</span></span>
7. <span data-ttu-id="80a20-133">按兩下 [預設搜尋引擎名稱]，將它設為 [已啟用]，然後輸入「Bing 中的 Microsoft Search」</span><span class="sxs-lookup"><span data-stu-id="80a20-133">Double-click **Default search provider name**, set it to Enabled, and enter 'Microsoft Search in Bing'</span></span>
8. <span data-ttu-id="80a20-134">按兩下 [預設搜尋提供者搜尋 URL]，將它設為 [已啟用]，然後輸入 `https://www.bing.com/business/search?q={searchTerms}&amp;form=BFBSPR`</span><span class="sxs-lookup"><span data-stu-id="80a20-134">Double-click **Default search provider search URL**, set it to **Enabled**, and enter `https://www.bing.com/business/search?q={searchTerms}&amp;form=BFBSPR`</span></span>
9. <span data-ttu-id="80a20-135">將結果 GPO 連結到適當網域以強制執行結果 GPO。</span><span class="sxs-lookup"><span data-stu-id="80a20-135">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>

## <a name="internet-explorer-11-or-later"></a><span data-ttu-id="80a20-136">Internet Explorer 11 或更新版本</span><span class="sxs-lookup"><span data-stu-id="80a20-136">Internet Explorer 11 or later</span></span>

<span data-ttu-id="80a20-137">設定此原則之後，使用者將能夠變更搜尋提供者。</span><span class="sxs-lookup"><span data-stu-id="80a20-137">Users will be able to change the search provider after this policy is set.</span></span>
  
### <a name="step-1-configure-the-local-machine-that-will-be-used-to-set-the-gpo"></a><span data-ttu-id="80a20-138">步驟 1：</span><span class="sxs-lookup"><span data-stu-id="80a20-138">STEP 1.</span></span> <span data-ttu-id="80a20-139">設定將用來設定 GPO 的本機電腦</span><span class="sxs-lookup"><span data-stu-id="80a20-139">Configure the local machine that will be used to set the GPO</span></span>

<span data-ttu-id="80a20-140">將下列文字貼上到 reg (\*.reg) 檔案中。</span><span class="sxs-lookup"><span data-stu-id="80a20-140">Paste the following text into a reg(\*.reg) file.</span></span>
  
<span data-ttu-id="80a20-141">Windows 登錄編輯程式 5.00 版</span><span class="sxs-lookup"><span data-stu-id="80a20-141">Windows Registry Editor Version 5.00</span></span>
  
<pre>[HKEY_CURRENT_USER\Software\Microsoft\Internet Explorer\SearchScopes]
"DefaultScope"="{D54CD0C8-C007-4BC4-B2DD-1E4896B8406D}"
[HKEY_CURRENT_USER\Software\Microsoft\Internet Explorer\SearchScopes\{D54CD0C8-C007-4BC4-B2DD-1E4896B8406D}]
"Codepage"=dword:0000fde9
"DisplayName"="Microsoft Search in Bing"
"OSDFileURL"="https://www.bing.com/sa/osd/bfb.xml"
"FaviconURL"="https://www.bing.com/sa/simg/bb.ico"
"URL"="https://www.bing.com/business/search?q={searchTerms}&amp;form=BFBSPR"</pre>
  
<span data-ttu-id="80a20-142">按兩下所建立的檔案，然後按照步驟操作以匯入檔案。</span><span class="sxs-lookup"><span data-stu-id="80a20-142">Double-click the file created and follow the steps to import the file.</span></span> <span data-ttu-id="80a20-143">成功匯入後應該會出現下列對話方塊：</span><span class="sxs-lookup"><span data-stu-id="80a20-143">A successful import should result in the following dialog:</span></span>
  
![登錄編輯程式成功匯入訊息](media/ea3686b9-f6d7-481e-9a0d-2c96891bc501.png)
  
### <a name="step-2-open-the-group-policy-management-console-gpmcmsc-and-switch-to-editing-an-existing-policy-or-creating-a-new-one"></a><span data-ttu-id="80a20-145">步驟 2：</span><span class="sxs-lookup"><span data-stu-id="80a20-145">STEP 2.</span></span> <span data-ttu-id="80a20-146">開啟 [群組原則管理主控台] (gpmc.msc)，然後切換以編輯現有原則或建立新原則</span><span class="sxs-lookup"><span data-stu-id="80a20-146">Open the Group Policy Management Console (gpmc.msc) and switch to editing an existing policy or creating a new one</span></span>

1. <span data-ttu-id="80a20-147">瀏覽至 [使用者設定]\[原則]\[喜好設定]\[Windows 設定]。</span><span class="sxs-lookup"><span data-stu-id="80a20-147">Navigate to **User Configuration\Policies\Preferences\Windows Settings**.</span></span>
2. <span data-ttu-id="80a20-148">以滑鼠右鍵按一下 [登錄]\[新增]，然後選取 [登錄精靈]。</span><span class="sxs-lookup"><span data-stu-id="80a20-148">Right-click on **Registry\New** and select **Registry Wizard**.</span></span> <span data-ttu-id="80a20-149">從 [登錄瀏覽器] 視窗中，選取 [本機電腦]，然後按 [下一步]。</span><span class="sxs-lookup"><span data-stu-id="80a20-149">From the Registry Browser window, select **Local Computer** and click **Next**.</span></span>
3. <span data-ttu-id="80a20-150">瀏覽至 **HKEY_CURRENT_USER\SOFTWARE\Microsoft\Internet Explorer\SearchScopes**。</span><span class="sxs-lookup"><span data-stu-id="80a20-150">Navigate to **HKEY_CURRENT_USER\SOFTWARE\Microsoft\Internet Explorer\SearchScopes**.</span></span>
4. <span data-ttu-id="80a20-151">請務必從此機碼選取 DefaultScope。</span><span class="sxs-lookup"><span data-stu-id="80a20-151">From this key, make sure to select DefaultScope.</span></span>

    ![選取了 DefaultScope 的登錄瀏覽器](media/ec5a450d-0cba-4e9c-acba-1a09e8e90bad.png)
5. <span data-ttu-id="80a20-153">選取包含 Bing 中 Microsoft Search 的 GUID 的所有子機碼，以及該機碼下的所有值，但不要選取任何使用者設定檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="80a20-153">Check all sub keys containing the GUID for Microsoft Search in Bing and every value under the key except any path to user profiles.</span></span> <span data-ttu-id="80a20-154">向下捲動以選取其他項目。</span><span class="sxs-lookup"><span data-stu-id="80a20-154">Scroll down to select other items.</span></span>
6. <span data-ttu-id="80a20-155">按一下 [完成] 以完成此組態。</span><span class="sxs-lookup"><span data-stu-id="80a20-155">Click Finish to complete this configuration.</span></span>

### <a name="step-3-set-up-user-preferences-to-help-eliminate-a-warning-the-user-may-get-when-defaultscope-search-is-enforced"></a><span data-ttu-id="80a20-156">步驟 3：</span><span class="sxs-lookup"><span data-stu-id="80a20-156">STEP 3.</span></span> <span data-ttu-id="80a20-157">設定使用者喜好設定以協助減少強制執行 DefaultScope 時使用者會收到的警告</span><span class="sxs-lookup"><span data-stu-id="80a20-157">Set up User Preferences to help eliminate a warning the user may get when DefaultScope search is enforced</span></span>

<span data-ttu-id="80a20-158">此警告是預設的設計，目的是要警示使用者有某個程式正在嘗試修改他們的設定。</span><span class="sxs-lookup"><span data-stu-id="80a20-158">This warning is by design and alerts users of a program trying to modify their settings.</span></span>
  
1. <span data-ttu-id="80a20-159">在同一個 GPO 內，以滑鼠右鍵按一下 [登錄]\[新增] 然後選取 [登錄精靈]。</span><span class="sxs-lookup"><span data-stu-id="80a20-159">Within the same GPO, right click on **Registry\New** and select **Registry Wizard**.</span></span>
2. <span data-ttu-id="80a20-160">瀏覽至 **HKEY_CURRENT_USER\SOFTWARE\Microsoft\Internet Explorer\User Preferences**。</span><span class="sxs-lookup"><span data-stu-id="80a20-160">Navigate to **HKEY_CURRENT_USER\SOFTWARE\Microsoft\Internet Explorer\User Preferences**.</span></span>
3. <span data-ttu-id="80a20-161">選取 **User Preferences** 機碼。</span><span class="sxs-lookup"><span data-stu-id="80a20-161">Select the **User Preference** key.</span></span>
4. <span data-ttu-id="80a20-162">按一下 [完成]。</span><span class="sxs-lookup"><span data-stu-id="80a20-162">Click **Finish**.</span></span>
5. <span data-ttu-id="80a20-163">按一下新建立的物件。</span><span class="sxs-lookup"><span data-stu-id="80a20-163">Click on the newly created object.</span></span> <span data-ttu-id="80a20-164">在右側窗格中，於 User Preferences (使用者喜好設定) 物件上按兩下，將 [動作] 變更成 [刪除]，然後儲存。</span><span class="sxs-lookup"><span data-stu-id="80a20-164">On the right-side pane double click on the User Preferences object, change the **Action** to **Delete and Save**.</span></span>
6. <span data-ttu-id="80a20-165">將結果 GPO 連結到適當網域以強制執行結果 GPO。</span><span class="sxs-lookup"><span data-stu-id="80a20-165">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>