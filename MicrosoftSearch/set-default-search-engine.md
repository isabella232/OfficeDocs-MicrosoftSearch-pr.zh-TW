---
title: 設定預設搜尋引擎
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
ms.assetid: ee40010e-5d7f-4ba8-a3f8-d240dab3af6d
ROBOTS: NOINDEX
description: 了解如何將 Bing 設定為公司使用 Microsoft Search 的預設搜尋引擎。
ms.openlocfilehash: 7c7ec8be726f2ac12a0e07f3d70c4b6515366bf3
ms.sourcegitcommit: 3da22a2e09830672ebf199e05a32fa89b75c083b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/27/2019
ms.locfileid: "37289016"
---
# <a name="make-bing-the-default-search-engine"></a><span data-ttu-id="ba066-103">讓 Bing 成為預設搜尋引擎</span><span class="sxs-lookup"><span data-stu-id="ba066-103">Make Bing the default search engine</span></span>
  
<span data-ttu-id="ba066-104">本文將說明如何讓 Bing 成為 Microsoft Edge、Google Chrome 和 Internet Explorer 的預設搜尋引擎。</span><span class="sxs-lookup"><span data-stu-id="ba066-104">This article explains how to make Bing the default search engine for Microsoft Edge, Google Chrome, and Internet Explorer.</span></span> 
  
## <a name="microsoft-edge-on-windows-10-version-1703-or-later"></a><span data-ttu-id="ba066-105">Windows 10 版本 1703 或更新版本上的 Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ba066-105">Microsoft Edge on Windows 10, Version 1703 or later</span></span>

<span data-ttu-id="ba066-106">雖然您可以將 Bing 設定為預設的搜尋引擎，Microsoft Edge 可讓使用者變更其設定，以使用不同的搜尋引擎。</span><span class="sxs-lookup"><span data-stu-id="ba066-106">Although you'll set Bing as the default search engine, Microsoft Edge allows users to change their settings to use a different search engine.</span></span>
  
<span data-ttu-id="ba066-107">如需適用於其他版本 Windows 的最新 ADMX 檔案，請參閱[如何在 Windows 中建立和管理群組原則系統管理範本的集中存放區](https://support.microsoft.com/help/3087759/how-to-create-and-manage-the-central-store-for-group-policy-administra)。</span><span class="sxs-lookup"><span data-stu-id="ba066-107">For the latest ADMX files for various versions of Windows, see [How to create and manage the Central Store for Group Policy Administrative Templates in Windows](https://support.microsoft.com/help/3087759/how-to-create-and-manage-the-central-store-for-group-policy-administra).</span></span>
  
<span data-ttu-id="ba066-108">如果在 GPMC 中找不到本節中描述的設定，請下載適當的 ADMX 並將它們複製到集中存放區。</span><span class="sxs-lookup"><span data-stu-id="ba066-108">If the setting described in this section cannot be found inside of GPMC, download the appropriate ADMX and copy them to the central store.</span></span> <span data-ttu-id="ba066-109">如需詳細資訊，請參閱使用 [ADMX 檔案編輯網域型 GPO](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-vista/cc748955%28v%3dws.10%29)。</span><span class="sxs-lookup"><span data-stu-id="ba066-109">For more information, see [Editing Domain-Based GPOs Using ADMX Files](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-vista/cc748955%28v%3dws.10%29).</span></span> <span data-ttu-id="ba066-110">控制器上的集中存放區是使用下列命名慣例的資料夾：</span><span class="sxs-lookup"><span data-stu-id="ba066-110">Central store on the controller is a folder with the following naming convention:</span></span>
  
 <span data-ttu-id="ba066-111">**%systemroot%\sysvol\\<domain\>\policies\PolicyDefinitions**</span><span class="sxs-lookup"><span data-stu-id="ba066-111">**%systemroot%\sysvol\\<domain\>\policies\PolicyDefinitions**</span></span>
  
<span data-ttu-id="ba066-112">控制站處理的每個網域都應該有個別的資料夾。</span><span class="sxs-lookup"><span data-stu-id="ba066-112">Each domain that your controller handles should get a separate folder.</span></span> <span data-ttu-id="ba066-113">可以透過命令提示字元使用下列命令來複製 ADMX 檔案：</span><span class="sxs-lookup"><span data-stu-id="ba066-113">The following command can be used to copy the ADMX file from the command prompt:</span></span>
  
 `Copy <path_to_ADMX.ADMX> %systemroot%\sysvol\<domain>\policies\PolicyDefinitions`
  
1. <span data-ttu-id="ba066-114">開啟 [群組原則管理主控台] (gpmc.msc)，然後切換以編輯現有原則或建立新原則。</span><span class="sxs-lookup"><span data-stu-id="ba066-114">Open the Group Policy Management Console (gpmc.msc) and switch to editing an existing policy or creating a new one.</span></span>
    
2. <span data-ttu-id="ba066-115">瀏覽至 **[電腦/使用者設定]&lt;&gt;\[系統管理範本]\[Windows 元件]\[Microsoft Edge]**。</span><span class="sxs-lookup"><span data-stu-id="ba066-115">Navigate to **&lt;Computer/User Configuration&gt;\Administrative Templates\Windows Components\Microsoft Edge**.</span></span>
    
1. <span data-ttu-id="ba066-116">按兩下 [設定預設搜索引擎]\*\*\*\*，將它設為 [已啟用]\*\*\*\*，然後輸入 `https://www.bing.com/sa/osd/bfb.xml`</span><span class="sxs-lookup"><span data-stu-id="ba066-116">Double-click **Set default search engine**, set to **Enabled**, and enter `https://www.bing.com/sa/osd/bfb.xml`</span></span>
    
3. <span data-ttu-id="ba066-117">將結果 GPO 連結到適當網域以強制執行結果 GPO。</span><span class="sxs-lookup"><span data-stu-id="ba066-117">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>


## <a name="google-chrome-on-windows-xp-sp2-or-later"></a><span data-ttu-id="ba066-118">Windows XP SP2 或更新版本上的 Google Chrome</span><span class="sxs-lookup"><span data-stu-id="ba066-118">Google Chrome on Windows XP SP2 or later</span></span>

<span data-ttu-id="ba066-119">設定此原則之後，使用者將無法變更預設的搜尋引擎。</span><span class="sxs-lookup"><span data-stu-id="ba066-119">Users won't be able to change the default search engine after this policy is set.</span></span>
  
<span data-ttu-id="ba066-120">Chrome 隨附自己的一組群組原則設定，您可以從 [Google Chrome Enterprise 說明](https://support.google.com/chrome/a/answer/187202)以 ADMX 檔案的格式下載。</span><span class="sxs-lookup"><span data-stu-id="ba066-120">Chrome comes with its own set of group policy settings which can be downloaded in the form of an ADMX file from [Google Chrome Enterprise Help](https://support.google.com/chrome/a/answer/187202).</span></span> <span data-ttu-id="ba066-121">如果使用 Windows Vista/Server 2008 或更新版本的作業系統來管理網域的 GPO，則此套件中提供的 ADMX 檔案將會管理 Windows XP SP2 或更新版本上的 Chrome 設定。</span><span class="sxs-lookup"><span data-stu-id="ba066-121">If operating systems Windows Vista/Server 2008 or later are used to manage GPO's for the domain, the ADMX file provided in this package takes care of Chrome settings on Windows XP SP2 or later.</span></span>
  
<span data-ttu-id="ba066-122">針對網域控制站上的 ADMX 檔案，將範本檔案複製到集中存放區。</span><span class="sxs-lookup"><span data-stu-id="ba066-122">Copy the template file to a central store for ADMX files on the domain controller.</span></span> <span data-ttu-id="ba066-123">如需詳細資訊，請參閱使用 [ADMX 檔案編輯網域型 GPO](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-vista/cc748955%28v%3dws.10%29)。</span><span class="sxs-lookup"><span data-stu-id="ba066-123">For more information, see [Editing Domain-Based GPOs Using ADMX Files](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-vista/cc748955%28v%3dws.10%29).</span></span> <span data-ttu-id="ba066-124">控制器上的集中存放區是使用下列命名慣例的資料夾：</span><span class="sxs-lookup"><span data-stu-id="ba066-124">Central store on the controller is a folder with the following naming convention:</span></span>
  
 <span data-ttu-id="ba066-125">**%systemroot%\sysvol\\<domain\>\policies\PolicyDefinitions**</span><span class="sxs-lookup"><span data-stu-id="ba066-125">**%systemroot%\sysvol\\<domain\>\policies\PolicyDefinitions**</span></span>
  
<span data-ttu-id="ba066-126">控制站處理的每個網域都應該有個別的資料夾。</span><span class="sxs-lookup"><span data-stu-id="ba066-126">Each domain that your controller handles should get a separate folder.</span></span> <span data-ttu-id="ba066-127">可以透過命令提示字元使用下列命令來複製 ADMX 檔案：</span><span class="sxs-lookup"><span data-stu-id="ba066-127">The following command can be used to copy the ADMX file from the command prompt:</span></span>
  
 `Copy <path_to_Chrome.ADMX> %systemroot%\sysvol\<domain>\policies\PolicyDefinitions`
  
1. <span data-ttu-id="ba066-128">開啟 [群組原則管理主控台] (gpmc.msc)，然後切換以編輯任何現有原則或建立新原則。</span><span class="sxs-lookup"><span data-stu-id="ba066-128">Open the Group Policy Management Console (gpmc.msc) and switch to editing any existing policy or creating a new one.</span></span>
    
2. <span data-ttu-id="ba066-129">確定在 [使用者設定]/[電腦設定] 中的 [系統管理範本] 區段中都有下列資料夾：Google Chrome 和 Google Chrome - 預設設定。</span><span class="sxs-lookup"><span data-stu-id="ba066-129">Make sure the following folders appear in the Administrative Templates section of both User/Computer Configuration: Google Chrome and Google Chrome - Default Settings.</span></span>
    
  - <span data-ttu-id="ba066-130">第一個區段的設定是固定的，而且本機系統管理員無法在瀏覽器中變更它們。</span><span class="sxs-lookup"><span data-stu-id="ba066-130">The settings of the first section are fixed and local administrators won't be able to change them in the browser.</span></span>
    
  - <span data-ttu-id="ba066-131">使用者可以在瀏覽器設定中變更原則後面區段的設定。</span><span class="sxs-lookup"><span data-stu-id="ba066-131">The settings of the latter section of policies can be changed by users in the browser settings.</span></span>
    
3. <span data-ttu-id="ba066-132">瀏覽至 [\<電腦/使用者\>設定]\[系統管理範本]\[Google Chrome]\[預設搜尋引擎]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="ba066-132">Navigate to **\<Computer/User\> Configuration\Administrative Templates\Google Chrome\Default search provider**</span></span>
    
4. <span data-ttu-id="ba066-133">按兩下 [啟用預設搜尋引擎]\*\*\*\*，然後設為 [已啟用]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="ba066-133">Double-click **Enable the default search provider**, and set it to **Enabled**.</span></span>
    
5. <span data-ttu-id="ba066-134">按兩下 [預設搜尋提供者圖示]\*\*\*\*，將它設為 [已啟用]\*\*\*\*，然後輸入 `https://www.bing.com/sa/simg/bb.ico`</span><span class="sxs-lookup"><span data-stu-id="ba066-134">Double-click **Default search provider icon**, set it to **Enabled**, and enter `https://www.bing.com/sa/simg/bb.ico`</span></span>
    
6. <span data-ttu-id="ba066-135">按兩下 [預設搜尋提供者立即 URL]\*\*\*\*，然後輸入 `https://www.bing.com/business/search?q={searchTerms}&amp;form=BFBSPR`</span><span class="sxs-lookup"><span data-stu-id="ba066-135">Double-click **Default search provider instant URL**, and enter `https://www.bing.com/business/search?q={searchTerms}&amp;form=BFBSPR`</span></span>
    
7. <span data-ttu-id="ba066-136">按兩下 [預設搜尋引擎名稱]\*\*\*\*，將它設為 [已啟用]，然後輸入「Bing 中的 Microsoft Search」</span><span class="sxs-lookup"><span data-stu-id="ba066-136">Double-click **Default search provider name**, set it to Enabled, and enter 'Microsoft Search in Bing'</span></span>
    
8. <span data-ttu-id="ba066-137">按兩下 [預設搜尋提供者搜尋 URL]\*\*\*\*，將它設為 [已啟用]\*\*\*\*，然後輸入 `https://www.bing.com/business/search?q={searchTerms}&amp;form=BFBSPR`</span><span class="sxs-lookup"><span data-stu-id="ba066-137">Double-click **Default search provider search URL**, set it to **Enabled**, and enter `https://www.bing.com/business/search?q={searchTerms}&amp;form=BFBSPR`</span></span>
    
9. <span data-ttu-id="ba066-138">按兩下 [預設搜尋提供者建議 URL]\*\*\*\*，將它設為 [已啟用]\*\*\*\*，然後輸入 `https://business.bing.com/api/v2/browser/suggest?q={searchTerms}&amp;form=BFBSPA`</span><span class="sxs-lookup"><span data-stu-id="ba066-138">Double-click **Default search provider suggest URL**, set it to **Enabled**, and enter `https://business.bing.com/api/v2/browser/suggest?q={searchTerms}&amp;form=BFBSPA`</span></span>
    
10. <span data-ttu-id="ba066-139">將結果 GPO 連結到適當網域以強制執行結果 GPO。</span><span class="sxs-lookup"><span data-stu-id="ba066-139">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>
    
<span data-ttu-id="ba066-140">設定預設搜尋引擎會在瀏覽器網址列中加入 Microsoft Search 搜尋建議功能。</span><span class="sxs-lookup"><span data-stu-id="ba066-140">Setting the default search engine will add the Microsoft Search search suggestions feature in the browser address bar.</span></span> <span data-ttu-id="ba066-141">此功能目前只支援書籤。</span><span class="sxs-lookup"><span data-stu-id="ba066-141">Currently, this supports bookmarks only.</span></span> <span data-ttu-id="ba066-142">當使用者在網址列中輸入時，將會在公用網路建議的上方看到最熱門的兩個書籤建議。</span><span class="sxs-lookup"><span data-stu-id="ba066-142">Users will see the top two bookmark suggestions above public web suggestions as they type in the address bar.</span></span>

## <a name="internet-explorer-11-or-later"></a><span data-ttu-id="ba066-143">Internet Explorer 11 或更新版本</span><span class="sxs-lookup"><span data-stu-id="ba066-143">Internet Explorer 11 or later versions</span></span>

<span data-ttu-id="ba066-144">設定此原則之後，使用者將能夠變更搜尋提供者。</span><span class="sxs-lookup"><span data-stu-id="ba066-144">Users will be able to change the search provider after this policy is set.</span></span>
  
### <a name="step-1-configure-the-local-machine-that-will-be-used-to-set-the-gpo"></a><span data-ttu-id="ba066-145">步驟 1：</span><span class="sxs-lookup"><span data-stu-id="ba066-145">Step 1</span></span> <span data-ttu-id="ba066-146">設定將用來設定 GPO 的本機電腦</span><span class="sxs-lookup"><span data-stu-id="ba066-146">Configure the local machine that will be used to set the GPO</span></span>

<span data-ttu-id="ba066-147">將下列文字貼上到 reg (\*.reg) 檔案中。</span><span class="sxs-lookup"><span data-stu-id="ba066-147">Paste the following text into a reg(\*.reg) file.</span></span>
  
<span data-ttu-id="ba066-148">Windows 登錄編輯程式 5.00 版</span><span class="sxs-lookup"><span data-stu-id="ba066-148">Windows Registry Editor Version 5.00</span></span>
  
<pre>[HKEY_CURRENT_USER\Software\Microsoft\Internet Explorer\SearchScopes]
"DefaultScope"="{D54CD0C8-C007-4BC4-B2DD-1E4896B8406D}"
[HKEY_CURRENT_USER\Software\Microsoft\Internet Explorer\SearchScopes\{D54CD0C8-C007-4BC4-B2DD-1E4896B8406D}]
"Codepage"=dword:0000fde9
"DisplayName"="Microsoft Search in Bing"
"OSDFileURL"="https://www.bing.com/sa/osd/bfb.xml"
"FaviconURL"="https://www.bing.com/sa/simg/bb.ico"
"SuggestionsURL_JSON"="https://business.ing.com/api/v2/browser/suggest?q={searchTerms}&amp;form=BFBSPA"
"ShowSearchSuggestions"=dword:00000001
"URL"="https://www.bing.com/business/search?q={searchTerms}&amp;form=BFBSPR"</pre>
  
<span data-ttu-id="ba066-149">按兩下所建立的檔案，然後按照步驟操作以匯入檔案。</span><span class="sxs-lookup"><span data-stu-id="ba066-149">Double-click the file created and follow the steps to import the file.</span></span> <span data-ttu-id="ba066-150">成功匯入後應該會出現下列對話方塊：</span><span class="sxs-lookup"><span data-stu-id="ba066-150">A successful import should result in the following dialog:</span></span>
  
![登錄編輯程式成功匯入訊息](media/ea3686b9-f6d7-481e-9a0d-2c96891bc501.png)
  
### <a name="step-2-open-the-group-policy-management-console-gpmcmsc-and-switch-to-editing-an-existing-policy-or-creating-a-new-one"></a><span data-ttu-id="ba066-152">步驟 2：</span><span class="sxs-lookup"><span data-stu-id="ba066-152">Step 2</span></span> <span data-ttu-id="ba066-153">開啟 [群組原則管理主控台] (gpmc.msc)，然後切換以編輯現有原則或建立新原則</span><span class="sxs-lookup"><span data-stu-id="ba066-153">Open the Group Policy Management Console (gpmc.msc) and switch to editing an existing policy or creating a new one</span></span>

1. <span data-ttu-id="ba066-154">瀏覽至 [使用者設定]\[原則]\[喜好設定]\[Windows 設定]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="ba066-154">Navigate to **User Configuration\Policies\Preferences\Windows Settings**.</span></span>
    
2. <span data-ttu-id="ba066-155">以滑鼠右鍵按一下 [登錄]\[新增]\*\*\*\*，然後選取 [登錄精靈]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="ba066-155">Right-click on **Registry\New** and select **Registry Wizard**.</span></span> <span data-ttu-id="ba066-156">從 [登錄瀏覽器] 視窗中，選取 [本機電腦]\*\*\*\*，然後按 [下一步]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="ba066-156">From the Registry Browser window, select **Local Computer** and click **Next**.</span></span>
    
3. <span data-ttu-id="ba066-157">瀏覽至 **HKEY_CURRENT_USER\SOFTWARE\Microsoft\Internet Explorer\SearchScopes**。</span><span class="sxs-lookup"><span data-stu-id="ba066-157">Navigate to **HKEY_CURRENT_USER\SOFTWARE\Microsoft\Internet Explorer\SearchScopes**.</span></span>
    
4. <span data-ttu-id="ba066-158">請務必從此機碼選取 DefaultScope。</span><span class="sxs-lookup"><span data-stu-id="ba066-158">From this key, make sure to select DefaultScope.</span></span>
    
    ![選取了 DefaultScope 的登錄瀏覽器](media/ec5a450d-0cba-4e9c-acba-1a09e8e90bad.png)
  
5. <span data-ttu-id="ba066-160">選取包含 Bing 中 Microsoft Search 的 GUID 的所有子機碼，以及該機碼下的所有值，但不要選取任何使用者設定檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="ba066-160">Check all sub keys containing the GUID for Microsoft Search in Bing and every value under the key except any path to user profiles.</span></span> <span data-ttu-id="ba066-161">向下捲動以選取其他項目。</span><span class="sxs-lookup"><span data-stu-id="ba066-161">Scroll down to select other items.</span></span>
    
    ![選取了其他值的登錄瀏覽器](media/7eef7690-8bc5-46cf-9cd8-bd134fc77a02.png)
  
6. <span data-ttu-id="ba066-163">按一下 [完成] 以完成此組態。</span><span class="sxs-lookup"><span data-stu-id="ba066-163">Click Finish to complete this configuration.</span></span>
    
### <a name="step-3-set-up-user-preferences-to-help-eliminate-a-warning-the-user-may-get-when-defaultscope-search-is-enforced"></a><span data-ttu-id="ba066-164">步驟 3：</span><span class="sxs-lookup"><span data-stu-id="ba066-164">Step 3</span></span> <span data-ttu-id="ba066-165">設定使用者喜好設定以協助減少強制執行 DefaultScope 時使用者會收到的警告</span><span class="sxs-lookup"><span data-stu-id="ba066-165">Set up User Preferences to help eliminate a warning the user may get when DefaultScope search is enforced</span></span>

<span data-ttu-id="ba066-166">此警告是預設的設計，目的是要警示使用者有某個程式正在嘗試修改他們的設定。</span><span class="sxs-lookup"><span data-stu-id="ba066-166">This warning is by design and alerts users of a program trying to modify their settings.</span></span>
  
1. <span data-ttu-id="ba066-167">在同一個 GPO 內，以滑鼠右鍵按一下 [登錄]\[新增]\*\*\*\* 然後選取 [登錄精靈]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="ba066-167">Within the same GPO, right click on **Registry\New** and select **Registry Wizard**.</span></span>
    
2. <span data-ttu-id="ba066-168">瀏覽至 **HKEY_CURRENT_USER\SOFTWARE\Microsoft\Internet Explorer\User Preferences**。</span><span class="sxs-lookup"><span data-stu-id="ba066-168">Navigate to **HKEY_CURRENT_USER\SOFTWARE\Microsoft\Internet Explorer\User Preferences**.</span></span>
    
3. <span data-ttu-id="ba066-169">選取 **User Preferences** 機碼。</span><span class="sxs-lookup"><span data-stu-id="ba066-169">Select the **User Preference** key.</span></span>
    
4. <span data-ttu-id="ba066-170">按一下 [完成]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="ba066-170">Click **Finish**.</span></span>
    
5. <span data-ttu-id="ba066-171">按一下新建立的物件。</span><span class="sxs-lookup"><span data-stu-id="ba066-171">Click on the newly created object.</span></span> <span data-ttu-id="ba066-172">在右側窗格中，於 User Preferences (使用者喜好設定) 物件上按兩下，將 [動作]\*\*\*\* 變更成 [刪除]\*\*\*\*，然後儲存。</span><span class="sxs-lookup"><span data-stu-id="ba066-172">On the right-side pane double click on the User Preferences object, change the **Action** to **Delete and Save**.</span></span>
1. <span data-ttu-id="ba066-173">將結果 GPO 連結到適當網域以強制執行結果 GPO。</span><span class="sxs-lookup"><span data-stu-id="ba066-173">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>