---
title: 設定預設搜尋引擎
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
ms.assetid: ee40010e-5d7f-4ba8-a3f8-d240dab3af6d
ROBOTS: NOINDEX
description: 了解如何將 Bing 設定為公司使用 Microsoft Search 的預設搜尋引擎。
ms.openlocfilehash: 77a8ea884f4df26fc8f7661fb9a9b8791b2f0f18
ms.sourcegitcommit: be2e837d9b087bffe6ce40d72d7ae58a8fcdf3fe
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/30/2019
ms.locfileid: "34591114"
---
# <a name="set-default-search-engine"></a>設定預設搜尋引擎

> [!IMPORTANT]
> 本文章適用 Bing 系統管理入口網站中的 Microsoft Search。 我們正在將入口網站移至 Microsoft 365 系統管理中心，完成之後入口網站將會移除。 我們建議您使用 Microsoft 365 系統管理中心開始。 [Microsoft Search 概觀](overview-microsoft-search.md)。
    
設定預設瀏覽器、預設搜尋引擎和預設首頁將可協助您的使用者探索 Microsoft Search 功能，鼓勵更常使用，並提供更順暢的體驗。
  
若要為您的組織設定預設搜尋引擎，請依照以下步驟進行。
  
## <a name="internet-explorer"></a>Internet Explorer

### <a name="internet-explorer-11"></a>Internet Explorer 11

設定此原則之後，使用者將能夠變更搜尋提供者。
  
#### <a name="1-configure-the-local-machine-that-will-be-used-to-set-the-gpo"></a>1. 設定將用來設定 GPO 的本機電腦

將下列文字貼上到 reg (\*.reg) 檔案中。
  
Windows 登錄編輯程式 5.00 版
  
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
  
按兩下所建立的檔案，然後按照步驟操作以匯入檔案。 成功匯入後應該會出現下列對話方塊：
  
![登錄編輯程式成功匯入訊息](media/ea3686b9-f6d7-481e-9a0d-2c96891bc501.png)
  
#### <a name="2-open-the-group-policy-management-console-gpmcmsc-and-switch-to-editing-an-existing-policy-or-creating-a-new-one"></a>2. 開啟 [群組原則管理主控台] (gpmc.msc)，然後切換以編輯現有原則或建立新原則

1. 瀏覽至 [使用者設定]\[原則]\[喜好設定]\[Windows 設定]****。
    
2. 以滑鼠右鍵按一下 [登錄]\[新增]****，然後選取 [登錄精靈]****。 從 [登錄瀏覽器] 視窗中，選取 [本機電腦]****，然後按 [下一步]****。
    
3. 瀏覽至 **HKEY_CURRENT_USER\SOFTWARE\Microsoft\Internet Explorer\SearchScopes**。
    
4. 請務必從此機碼選取 DefaultScope。
    
    ![選取了 DefaultScope 的登錄瀏覽器](media/ec5a450d-0cba-4e9c-acba-1a09e8e90bad.png)
  
5. 選取包含 Bing 中 Microsoft Search 的 GUID 的所有子機碼，以及該機碼下的所有值，但不要選取任何使用者設定檔的路徑。 向下捲動以選取其他項目。
    
    ![選取了其他值的登錄瀏覽器](media/7eef7690-8bc5-46cf-9cd8-bd134fc77a02.png)
  
6. 按一下 [完成] 以完成此組態。
    
#### <a name="3-set-up-user-preferences-to-help-eliminate-a-warning-the-user-may-get-when-defaultscope-search-is-enforced"></a>3.設定 User Preferences (使用者喜好設定) 以協助減少強制執行 DefaultScope 時使用者會收到的警告。

此警告是預設的設計，目的是要警示使用者有某個程式正在嘗試修改他們的設定。
  
1. 在同一個 GPO 內，以滑鼠右鍵按一下 [登錄]\[新增]**** 然後選取 [登錄精靈]****。
    
2. 瀏覽至 **HKEY_CURRENT_USER\SOFTWARE\Microsoft\Internet Explorer\User Preferences**。
    
3. 選取 **User Preferences** 機碼。
    
4. 按一下 [完成]****。
    
5. 按一下新建立的物件。 在右側窗格中，於 User Preferences (使用者喜好設定) 物件上按兩下，將 [動作]**** 變更成 [刪除]****，然後儲存。
    
將結果 GPO 連結到適當網域以強制執行結果 GPO。
  
## <a name="microsoft-edge"></a>Microsoft Edge

### <a name="windows-10-version-1703-or-later"></a>Windows 10 (1703 版或更新版本)

設定此原則之後，使用者將能夠變更搜尋提供者。
  
如需適用於其他版本 Windows 的最新 ADMX 檔案，請參閱[如何在 Windows 中建立和管理群組原則系統管理範本的集中存放區](https://support.microsoft.com/zh-TW/help/3087759/how-to-create-and-manage-the-central-store-for-group-policy-administra)。
  
如果在 GPMC 中找不到本節中描述的設定，請下載適當的 ADMX 並將它們複製到集中存放區。 如需詳細資訊，請參閱使用 [ADMX 檔案編輯網域型 GPO](https://docs.microsoft.com/zh-TW/previous-versions/windows/it-pro/windows-vista/cc748955%28v%3dws.10%29)。 控制器上的集中存放區是使用下列命名慣例的資料夾：
  
 **%systemroot%\sysvol\\<domain\>\policies\PolicyDefinitions**
  
控制站處理的每個網域都應該有個別的資料夾。 可以透過命令提示字元使用下列命令來複製 ADMX 檔案：
  
 `Copy <path_to_ADMX.ADMX> %systemroot%\sysvol\<domain>\policies\PolicyDefinitions`
  
1. 開啟 [群組原則管理主控台] (gpmc.msc)，然後切換以編輯現有原則或建立新原則。
    
2. 瀏覽至 **[電腦/使用者設定]&lt;&gt;\[系統管理範本]\[Windows 元件]\[Microsoft Edge]**。
    
1. 按兩下 [設定預設搜索引擎]****，將它設為 [已啟用]****，然後輸入 `https://www.bing.com/sa/osd/bfb.xml`
    
3. 將結果 GPO 連結到適當網域以強制執行結果 GPO。
    
## <a name="google-chrome"></a>Google Chrome

### <a name="windows-xp-sp2-or-later"></a>Windows XP SP2 或更新版本

設定此原則之後，使用者將無法變更搜尋提供者。
  
Chrome 隨附自己的一組群組原則設定，您可以從 [Google Chrome Enterprise 說明](https://support.google.com/chrome/a/answer/187202)以 ADMX 檔案的格式下載。 如果使用 Windows Vista/Server 2008 或更新版本的作業系統來管理網域的 GPO，則此套件中提供的 ADMX 檔案將會管理 Windows XP SP2 或更新版本上的 Chrome 設定。
  
針對網域控制站上的 ADMX 檔案，將範本檔案複製到集中存放區。 如需詳細資訊，請參閱使用 [ADMX 檔案編輯網域型 GPO](https://docs.microsoft.com/zh-TW/previous-versions/windows/it-pro/windows-vista/cc748955%28v%3dws.10%29)。 控制器上的集中存放區是使用下列命名慣例的資料夾：
  
 **%systemroot%\sysvol\\<domain\>\policies\PolicyDefinitions**
  
控制站處理的每個網域都應該有個別的資料夾。 可以透過命令提示字元使用下列命令來複製 ADMX 檔案：
  
 `Copy <path_to_Chrome.ADMX> %systemroot%\sysvol\<domain>\policies\PolicyDefinitions`
  
1. 開啟 [群組原則管理主控台] (gpmc.msc)，然後切換以編輯任何現有原則或建立新原則。
    
2. 確定在 [使用者設定]/[電腦設定] 中的 [系統管理範本] 區段中都有下列資料夾：Google Chrome 和 Google Chrome - 預設設定。
    
  - 第一個區段的設定是固定的，而且本機系統管理員無法在瀏覽器中變更它們。
    
  - 使用者可以在瀏覽器設定中變更原則後面區段的設定。
    
3. 瀏覽至 [\<電腦/使用者\>設定]\[系統管理範本]\[Google Chrome]\[預設搜尋引擎]****。
    
4. 按兩下 [啟用預設搜尋引擎]****，然後設為 [已啟用]****。
    
5. 按兩下 [預設搜尋提供者圖示]****，將它設為 [已啟用]****，然後輸入 `https://www.bing.com/sa/simg/bb.ico`
    
6. 按兩下 [預設搜尋提供者立即 URL]****，然後輸入 `https://www.bing.com/business/search?q={searchTerms}&amp;form=BFBSPR`
    
7. 按兩下 [預設搜尋引擎名稱]****，將它設為 [已啟用]，然後輸入「Bing 中的 Microsoft Search」
    
8. 按兩下 [預設搜尋提供者搜尋 URL]****，將它設為 [已啟用]****，然後輸入 `https://www.bing.com/business/search?q={searchTerms}&amp;form=BFBSPR`
    
9. 按兩下 [預設搜尋提供者建議 URL]****，將它設為 [已啟用]****，然後輸入 `https://business.bing.com/api/v2/browser/suggest?q={searchTerms}&amp;form=BFBSPA`
    
10. 將結果 GPO 連結到適當網域以強制執行結果 GPO。
    
設定預設搜尋引擎會在瀏覽器網址列中加入 Microsoft Search 搜尋建議功能。 此功能目前只支援書籤。 當使用者在網址列中輸入時，將會在公用網路建議的上方看到最熱門的兩個書籤建議。