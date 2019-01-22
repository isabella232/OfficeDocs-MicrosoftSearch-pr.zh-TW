---
title: 設定預設搜尋引擎
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
ms.assetid: ee40010e-5d7f-4ba8-a3f8-d240dab3af6d
description: 了解如何將 Bing 設為使用 Microsoft 搜尋公司的預設搜尋引擎。
ms.openlocfilehash: 1102c4c58b1e46e450276430a1e79b34964b4ad4
ms.sourcegitcommit: bf52cc63b75f2e0324a716fe65da47702956b722
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/18/2019
ms.locfileid: "29380066"
---
# <a name="set-default-search-engine"></a><span data-ttu-id="6af5d-103">設定預設搜尋引擎</span><span class="sxs-lookup"><span data-stu-id="6af5d-103">Set default search engine</span></span>

<span data-ttu-id="6af5d-104">設定預設的瀏覽器、 預設搜尋引擎，以及預設首頁可協助您探索 Microsoft 搜尋功能、 鼓勵更多的使用狀況，並提供更順暢的使用者。</span><span class="sxs-lookup"><span data-stu-id="6af5d-104">Configuring the default browser, default search engine, and default homepage will help your users discover Microsoft Search capabilities, encourage more usage, and provide a smoother experience.</span></span>
  
<span data-ttu-id="6af5d-105">若要設定預設的搜尋引擎您的組織，請遵循下列步驟。</span><span class="sxs-lookup"><span data-stu-id="6af5d-105">To set the default search engine for your organization, follow the steps below.</span></span>
  
## <a name="internet-explorer"></a><span data-ttu-id="6af5d-106">Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="6af5d-106">Internet Explorer</span></span>

### <a name="internet-explorer-11"></a><span data-ttu-id="6af5d-107">Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="6af5d-107">Internet Explorer 11</span></span>

<span data-ttu-id="6af5d-108">使用者無法變更搜尋提供者之後此原則設定。</span><span class="sxs-lookup"><span data-stu-id="6af5d-108">Users will be able to change the search provider after this policy is set.</span></span>
  
#### <a name="1-configure-the-local-machine-that-will-be-used-to-set-the-gpo"></a><span data-ttu-id="6af5d-109">1.設定本機電腦將用來設定 GPO</span><span class="sxs-lookup"><span data-stu-id="6af5d-109">1. Configure the local machine that will be used to set the GPO</span></span>

<span data-ttu-id="6af5d-110">將下列文字貼到登錄 (\*.reg) 檔案。</span><span class="sxs-lookup"><span data-stu-id="6af5d-110">Paste the following text into a reg(\*.reg) file.</span></span>
  
<span data-ttu-id="6af5d-111">Windows 登錄編輯程式 5.00 版</span><span class="sxs-lookup"><span data-stu-id="6af5d-111">Windows Registry Editor Version 5.00</span></span>
  
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
  
<span data-ttu-id="6af5d-p101">按兩下 [建立的檔案並遵循的步驟來匯入檔案。成功匯入應該會導致下列對話方塊：</span><span class="sxs-lookup"><span data-stu-id="6af5d-p101">Double-click the file created and follow the steps to import the file. A successful import should result in the following dialog:</span></span>
  
![登錄編輯程式成功匯入訊息](media/ea3686b9-f6d7-481e-9a0d-2c96891bc501.png)
  
#### <a name="2-open-the-group-policy-management-console-gpmcmsc-and-switch-to-editing-an-existing-policy-or-creating-a-new-one"></a><span data-ttu-id="6af5d-115">2.開啟 「 群組原則管理主控台 （gpmc.msc 取得） 並切換至編輯現有的原則或建立一個新</span><span class="sxs-lookup"><span data-stu-id="6af5d-115">2. Open the Group Policy Management Console (gpmc.msc) and switch to editing an existing policy or creating a new one</span></span>

1. <span data-ttu-id="6af5d-116">瀏覽至**使用者 Configuration\Policies\Preferences\Windows 設定**。</span><span class="sxs-lookup"><span data-stu-id="6af5d-116">Navigate to **User Configuration\Policies\Preferences\Windows Settings**.</span></span>
    
2. <span data-ttu-id="6af5d-p102">以滑鼠右鍵按一下**Registry\New**並選取 [**登錄精靈**]。從登錄瀏覽器視窗中，選取 [**本機電腦**，並按一下 [**下一步**。</span><span class="sxs-lookup"><span data-stu-id="6af5d-p102">Right-click on **Registry\New** and select **Registry Wizard**. From the Registry Browser window, select **Local Computer** and click **Next**.</span></span>
    
3. <span data-ttu-id="6af5d-119">瀏覽至**HKEY_CURRENT_USER\SOFTWARE\Microsoft\Internet Explorer\SearchScopes**。</span><span class="sxs-lookup"><span data-stu-id="6af5d-119">Navigate to **HKEY_CURRENT_USER\SOFTWARE\Microsoft\Internet Explorer\SearchScopes**.</span></span>
    
4. <span data-ttu-id="6af5d-120">從此機碼，請務必選取 DefaultScope。</span><span class="sxs-lookup"><span data-stu-id="6af5d-120">From this key, make sure to select DefaultScope.</span></span>
    
    ![使用選取的 DefaultScope 登錄瀏覽器](media/ec5a450d-0cba-4e9c-acba-1a09e8e90bad.png)
  
5. <span data-ttu-id="6af5d-p103">檢查所有子機碼包含 Microsoft Search Bing 和使用者設定檔的任何路徑以外的機碼底下的每個值中的 GUID。若要選取其他項目向下捲動。</span><span class="sxs-lookup"><span data-stu-id="6af5d-p103">Check all sub keys containing the GUID for Microsoft Search in Bing and every value under the key except any path to user profiles. Scroll down to select other items.</span></span>
    
    ![選取其他值的登錄瀏覽器](media/7eef7690-8bc5-46cf-9cd8-bd134fc77a02.png)
  
6. <span data-ttu-id="6af5d-125">按一下 [完成] 來完成此設定。</span><span class="sxs-lookup"><span data-stu-id="6af5d-125">Click Finish to complete this configuration.</span></span>
    
#### <a name="3-set-up-user-preferences-to-help-eliminate-a-warning-the-user-may-get-when-defaultscope-search-is-enforced"></a><span data-ttu-id="6af5d-126">3.設定使用者喜好設定來協助避免使用者可能會收到一則警告訊息時 DefaultScope 搜尋會強制執行</span><span class="sxs-lookup"><span data-stu-id="6af5d-126">3. Set up User Preferences to help eliminate a warning the user may get when DefaultScope search is enforced</span></span>

<span data-ttu-id="6af5d-127">這則警告是根據設計和提醒程式嘗試要修改其設定的使用者。</span><span class="sxs-lookup"><span data-stu-id="6af5d-127">This warning is by design and alerts users of a program trying to modify their settings.</span></span>
  
1. <span data-ttu-id="6af5d-128">在相同的 GPO、 **Registry\New**上按一下滑鼠右鍵並選取**登錄精靈**]。</span><span class="sxs-lookup"><span data-stu-id="6af5d-128">Within the same GPO, right click on **Registry\New** and select **Registry Wizard**.</span></span>
    
2. <span data-ttu-id="6af5d-129">瀏覽至**HKEY_CURRENT_USER\SOFTWARE\Microsoft\Internet Explorer\User 喜好設定**。</span><span class="sxs-lookup"><span data-stu-id="6af5d-129">Navigate to **HKEY_CURRENT_USER\SOFTWARE\Microsoft\Internet Explorer\User Preferences**.</span></span>
    
3. <span data-ttu-id="6af5d-130">選取的**使用者喜好設定**索引鍵。</span><span class="sxs-lookup"><span data-stu-id="6af5d-130">Select the **User Preference** key.</span></span>
    
4. <span data-ttu-id="6af5d-131">按一下 [完成]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="6af5d-131">Click **Finish**.</span></span>
    
5. <span data-ttu-id="6af5d-p104">按一下 [在新建立的物件。右側邊窗格按兩下 [使用者喜好設定物件上，**刪除**並儲存變更**巨集指令**。</span><span class="sxs-lookup"><span data-stu-id="6af5d-p104">Click on the newly created object. On the right-side pane double click on the User Preferences object, change the **Action** to **Delete and Save**.</span></span>
    
<span data-ttu-id="6af5d-134">強制產生 GPO 連結至適當的網域。</span><span class="sxs-lookup"><span data-stu-id="6af5d-134">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>
  
## <a name="microsoft-edge"></a><span data-ttu-id="6af5d-135">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="6af5d-135">Microsoft Edge</span></span>

### <a name="windows-10-version-1703-or-later"></a><span data-ttu-id="6af5d-136">Windows 10、 1703 或更新版本</span><span class="sxs-lookup"><span data-stu-id="6af5d-136">Windows 10, Version 1703 or later</span></span>

<span data-ttu-id="6af5d-137">使用者無法變更搜尋提供者之後此原則設定。</span><span class="sxs-lookup"><span data-stu-id="6af5d-137">Users will be able to change the search provider after this policy is set.</span></span>
  
<span data-ttu-id="6af5d-138">各版本 Windows 的最新的 ADMX 檔案，請參閱 ＜[如何建立和管理群組原則系統管理範本 Windows 中的中央存放區](https://support.microsoft.com/en-us/help/3087759/how-to-create-and-manage-the-central-store-for-group-policy-administra)。</span><span class="sxs-lookup"><span data-stu-id="6af5d-138">For the latest ADMX files for various versions of Windows, see [How to create and manage the Central Store for Group Policy Administrative Templates in Windows](https://support.microsoft.com/en-us/help/3087759/how-to-create-and-manage-the-central-store-for-group-policy-administra).</span></span>
  
<span data-ttu-id="6af5d-p105">如果內部 GPMC 找不到此節所述的設定，下載適當的 ADMX，並將其複製到集中存放區。如需詳細資訊，請參閱[參閱 Gpo 使用 ADMX 檔案](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-vista/cc748955%28v%3dws.10%29)。控制站上的集中存放區已有下列的命名慣例的資料夾：</span><span class="sxs-lookup"><span data-stu-id="6af5d-p105">If the setting described in this section cannot be found inside of GPMC, download the appropriate ADMX and copy them to the central store. For more information, see [Editing Domain-Based GPOs Using ADMX Files](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-vista/cc748955%28v%3dws.10%29). Central store on the controller is a folder with the following naming convention:</span></span>
  
 <span data-ttu-id="6af5d-142">**%systemroot%\sysvol\\<domain\>\policies\PolicyDefinitions**</span><span class="sxs-lookup"><span data-stu-id="6af5d-142">**%systemroot%\sysvol\\<domain\>\policies\PolicyDefinitions**</span></span>
  
<span data-ttu-id="6af5d-p106">您控制站會處理每個網域應取得個別的資料夾。若要從命令提示字元中 ADMX 檔案複製可用下列命令：</span><span class="sxs-lookup"><span data-stu-id="6af5d-p106">Each domain that your controller handles should get a separate folder. The following command can be used to copy the ADMX file from the command prompt:</span></span>
  
 `Copy <path_to_ADMX.ADMX> %systemroot%\sysvol\<domain>\policies\PolicyDefinitions`
  
1. <span data-ttu-id="6af5d-145">若要編輯現有的原則或建立一個新參數和開啟 「 群組原則管理主控台 （gpmc.msc 取得）。</span><span class="sxs-lookup"><span data-stu-id="6af5d-145">Open the Group Policy Management Console (gpmc.msc) and switch to editing an existing policy or creating a new one.</span></span>
    
2. <span data-ttu-id="6af5d-146">瀏覽至 [**&lt;電腦/使用者設定&gt;\Administrative Templates\Windows \microsoft Edge**。</span><span class="sxs-lookup"><span data-stu-id="6af5d-146">Navigate to **&lt;Computer/User Configuration&gt;\Administrative Templates\Windows Components\Microsoft Edge**.</span></span>
    
1. <span data-ttu-id="6af5d-147">按兩下 [**設定預設搜尋引擎**、 設為 [**已啟用**] 並輸入`https://www.bing.com/sa/osd/bfb.xml`</span><span class="sxs-lookup"><span data-stu-id="6af5d-147">Double-click **Set default search engine**, set to **Enabled**, and enter `https://www.bing.com/sa/osd/bfb.xml`</span></span>
    
3. <span data-ttu-id="6af5d-148">強制產生 GPO 連結至適當的網域。</span><span class="sxs-lookup"><span data-stu-id="6af5d-148">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>
    
## <a name="google-chrome"></a><span data-ttu-id="6af5d-149">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="6af5d-149">Google Chrome</span></span>

### <a name="windows-xp-sp2-or-later"></a><span data-ttu-id="6af5d-150">Windows XP SP2 或更新版本</span><span class="sxs-lookup"><span data-stu-id="6af5d-150">Windows XP SP2 or later</span></span>

<span data-ttu-id="6af5d-151">使用者將無法設定此原則之後變更搜尋提供者。</span><span class="sxs-lookup"><span data-stu-id="6af5d-151">Users won't be able to change the search provider after this policy is set.</span></span>
  
<span data-ttu-id="6af5d-p107">Chrome 隨附的群組原則設定可供下載的格式從[Google Chrome 企業協助](https://support.google.com/chrome/a/answer/187202)ADMX 檔案並將其專屬設定。如果作業系統 Windows Vista/2008年或更新版本的伺服器可用來管理 GPO 的網域，則此套件中所提供的 ADMX 檔案負責的 Chrome 設定在 Windows XP SP2 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="6af5d-p107">Chrome comes with its own set of group policy settings which can be downloaded in the form of an ADMX file from [Google Chrome Enterprise Help](https://support.google.com/chrome/a/answer/187202). If operating systems Windows Vista/Server 2008 or later are used to manage GPO's for the domain, the ADMX file provided in this package takes care of Chrome settings on Windows XP SP2 or later.</span></span>
  
<span data-ttu-id="6af5d-p108">將範本檔案複製到 ADMX 檔案的網域控制站上集中存放區。如需詳細資訊，請參閱[參閱 Gpo 使用 ADMX 檔案](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-vista/cc748955%28v%3dws.10%29)。控制站上的集中存放區已有下列的命名慣例的資料夾：</span><span class="sxs-lookup"><span data-stu-id="6af5d-p108">Copy the template file to a central store for ADMX files on the domain controller. For more information, see [Editing Domain-Based GPOs Using ADMX Files](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-vista/cc748955%28v%3dws.10%29). Central store on the controller is a folder with the following naming convention:</span></span>
  
 <span data-ttu-id="6af5d-157">**%systemroot%\sysvol\\<domain\>\policies\PolicyDefinitions**</span><span class="sxs-lookup"><span data-stu-id="6af5d-157">**%systemroot%\sysvol\\<domain\>\policies\PolicyDefinitions**</span></span>
  
<span data-ttu-id="6af5d-p109">您控制站會處理每個網域應取得個別的資料夾。若要從命令提示字元中 ADMX 檔案複製可用下列命令：</span><span class="sxs-lookup"><span data-stu-id="6af5d-p109">Each domain that your controller handles should get a separate folder. The following command can be used to copy the ADMX file from the command prompt:</span></span>
  
 `Copy <path_to_Chrome.ADMX> %systemroot%\sysvol\<domain>\policies\PolicyDefinitions`
  
1. <span data-ttu-id="6af5d-160">若要編輯的任何現有原則或建立一個新參數和開啟 「 群組原則管理主控台 （gpmc.msc 取得）。</span><span class="sxs-lookup"><span data-stu-id="6af5d-160">Open the Group Policy Management Console (gpmc.msc) and switch to editing any existing policy or creating a new one.</span></span>
    
2. <span data-ttu-id="6af5d-161">請確定下列資料夾會出現在 [系統管理範本] 區段中的兩個使用者/電腦設定： Google Chrome 及 Google Chrome-預設設定。</span><span class="sxs-lookup"><span data-stu-id="6af5d-161">Make sure the following folders appear in the Administrative Templates section of both User/Computer Configuration: Google Chrome and Google Chrome - Default Settings.</span></span>
    
  - <span data-ttu-id="6af5d-162">修正第一個區段的設定和本機系統管理員將無法在瀏覽器中加以變更。</span><span class="sxs-lookup"><span data-stu-id="6af5d-162">The settings of the first section are fixed and local administrators won't be able to change them in the browser.</span></span>
    
  - <span data-ttu-id="6af5d-163">在瀏覽器設定的使用者可以變更的後面] 區段中的原則設定。</span><span class="sxs-lookup"><span data-stu-id="6af5d-163">The settings of the latter section of policies can be changed by users in the browser settings.</span></span>
    
3. <span data-ttu-id="6af5d-164">瀏覽至 [**\<電腦/使用者\>\ 系統管理範本 Templates\Google Chrome\Default 搜尋提供者**</span><span class="sxs-lookup"><span data-stu-id="6af5d-164">Navigate to **\<Computer/User\> Configuration\Administrative Templates\Google Chrome\Default search provider**</span></span>
    
4. <span data-ttu-id="6af5d-165">按兩下 [**啟用的預設搜尋提供者**，並將它設為 [**已啟用**。</span><span class="sxs-lookup"><span data-stu-id="6af5d-165">Double-click **Enable the default search provider**, and set it to **Enabled**.</span></span>
    
5. <span data-ttu-id="6af5d-166">按兩下 [**預設搜尋提供者] 圖示**、 將它設為 [**已啟用**] 並輸入`https://www.bing.com/sa/simg/bb.ico`</span><span class="sxs-lookup"><span data-stu-id="6af5d-166">Double-click **Default search provider icon**, set it to **Enabled**, and enter `https://www.bing.com/sa/simg/bb.ico`</span></span>
    
6. <span data-ttu-id="6af5d-167">按兩下 [**預設的搜尋提供者立即 URL**，然後輸入`https://www.bing.com/business/search?q={searchTerms}&amp;form=BFBSPR`</span><span class="sxs-lookup"><span data-stu-id="6af5d-167">Double-click **Default search provider instant URL**, and enter `https://www.bing.com/business/search?q={searchTerms}&amp;form=BFBSPR`</span></span>
    
7. <span data-ttu-id="6af5d-168">按兩下 [**預設的搜尋提供者名稱**、 將它設為 [啟用] 並輸入 ' Microsoft 搜尋中 Bing'</span><span class="sxs-lookup"><span data-stu-id="6af5d-168">Double-click **Default search provider name**, set it to Enabled, and enter 'Microsoft Search in Bing'</span></span>
    
8. <span data-ttu-id="6af5d-169">按兩下 [**預設搜尋提供者搜尋 URL**、 將它設為 [**已啟用**] 並輸入`https://www.bing.com/business/search?q={searchTerms}&amp;form=BFBSPR`</span><span class="sxs-lookup"><span data-stu-id="6af5d-169">Double-click **Default search provider search URL**, set it to **Enabled**, and enter `https://www.bing.com/business/search?q={searchTerms}&amp;form=BFBSPR`</span></span>
    
9. <span data-ttu-id="6af5d-170">按兩下 [**預設搜尋提供者建議 URL**、 將它設為 [**已啟用**] 並輸入`https://business.bing.com/api/v2/browser/suggest?q={searchTerms}&amp;form=BFBSPA`</span><span class="sxs-lookup"><span data-stu-id="6af5d-170">Double-click **Default search provider suggest URL**, set it to **Enabled**, and enter `https://business.bing.com/api/v2/browser/suggest?q={searchTerms}&amp;form=BFBSPA`</span></span>
    
10. <span data-ttu-id="6af5d-171">強制產生 GPO 連結至適當的網域。</span><span class="sxs-lookup"><span data-stu-id="6af5d-171">Enforce the resultant GPO by linking it to the appropriate domain.</span></span>
    
<span data-ttu-id="6af5d-p110">設定預設的搜尋引擎會新增 Microsoft Search 搜尋建議功能在瀏覽器網址列中。目前這支援僅書籤。當他們在網址列中輸入使用者會看到公用 web 建議上方的頂端兩個書籤建議。</span><span class="sxs-lookup"><span data-stu-id="6af5d-p110">Setting the default search engine will add the Microsoft Search search suggestions feature in the browser address bar. Currently, this supports bookmarks only. Users will see the top two bookmark suggestions above public web suggestions as they type in the address bar.</span></span>