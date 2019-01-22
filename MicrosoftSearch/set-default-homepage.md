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
# <a name="set-default-homepage"></a>設定預設首頁

設定預設的瀏覽器、 預設搜尋引擎，以及預設首頁可協助您探索 Microsoft 搜尋功能、 鼓勵更多的使用狀況，並提供更順暢的使用者。
  
若要設定您的組織預設首頁，請遵循下列步驟。
  
## <a name="internet-explorer"></a>Internet Explorer

### <a name="internet-explorer-50-or-later"></a>Internet Explorer 5.0 或更新版本

1. 若要編輯的任何現有原則或建立一個新參數和開啟 「 群組原則管理主控台 （gpmc.msc 取得）。
    
2. 瀏覽至**使用者 Configuration\Preferences\Control 控制台 Settings\Internet 設定**。
    
3. 以滑鼠右鍵按一下**網際網路設定**並選取 [ **Internet Explorer 10**。
    
    > [!NOTE]
    > 您必須選取要套用的 Internet Explorer 11 設定為相同的設定會套用至 Internet Explorer 11 Internet Explorer 10 的選項。 
  
4. 這會以紅色加上底線未設定設定在目標電腦，而綠色中以底線標示的設定在目標電腦設定。若要變更底線，使用下列功能鍵：
    
    F5-啟用所有目前的索引標籤上的設定
    
    F6-啟用目前選取的設定
    
    F7-停用目前選取的設定
    
    F8-停用目前的索引標籤上的所有設定
    
5. 按**F8**設定的任何項目之前停用所有設定。螢幕應該看起來如下： 
    
    ![Internet Explorer 10 屬性] 對話方塊](media/2fd55755-5007-4e33-a795-c42ce2fcef4a.jpg)
  
6. 在首頁] 頁面上設定按**F6** ，然後輸入`https://www.bing.com/business?form=BFBSPR`
    
7. 強制產生 GPO 連結至適當的網域。
    
> [!NOTE]
> 使用者仍然可以變更首頁後此原則設定。 
  
## <a name="microsoft-edge"></a>Microsoft Edge

### <a name="windows-10-version-1511-or-later"></a>Windows 10、 1511 或更新版本

1. 若要編輯的任何現有原則或建立一個新參數和開啟 「 群組原則管理主控台 （gpmc.msc 取得）。
    
2. 瀏覽至 [**系統管理範本 \windows 元件 \ \microsoft Edge**
    
1. 按兩下 [**頁面設定起始**、 將它設為 [**已啟用**] 並輸入`https://www.bing.com/business`
    
3. 強制產生 GPO 連結至適當的網域。
    
> [!CAUTION]
> 使用者將無法設定此原則之後變更搜尋提供者。 
  
## <a name="google-chrome"></a>Google Chrome

### <a name="windows-xp-sp2-or-later"></a>Windows XP SP2 或更新版本

[Microsoft 技術支援人員上](https://support.microsoft.com/en-us/help/3087759/how-to-create-and-manage-the-central-store-for-group-policy-administra)可以找到上管理 ADMX 檔案和最新 ADMX 檔案的不同版本的 Windows 作業系統支援文章。

您也需要最新的 Google 原則檔，您可以找到[Google Chrome 企業](https://support.google.com/chrome/a/answer/187202)協助。
  
如果內部 GPMC 找不到此節所述的設定，下載適當的 ADMX，並將其複製到[集中存放區](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-vista/cc748955%28v%3dws.10%29)。控制站上的集中存放區已有下列的命名慣例的資料夾：
  
 **%systemroot%\sysvol\\<domain\>\policies\PolicyDefinitions**
  
每個網域控制站控點應取得個別的資料夾。若要從命令提示字元中 ADMX 檔案複製可用下列命令：
  
 `Copy <path_to_ADMX.ADMX> %systemroot%\sysvol\<domain>\policies\PolicyDefinitions`
  
1. 若要編輯的任何現有原則或建立一個新參數和開啟 「 群組原則管理主控台 （gpmc.msc 取得）。
    
2. 請確定下列資料夾會出現在 [**系統管理範本**] 區段中的*使用者/電腦設定*這兩種： Google Chrome 及 Google Chrome-預設設定 （使用者可以覆寫）。
    
   - 修正第一個區段的設定和本機系統管理員將無法對其進行變更。
    
   - 在其瀏覽器設定的使用者可以變更的後面] 區段中的原則設定。您應該先決定使用者可以覆寫預設設定。下列步驟，在對應的資料夾中的設定變更為您的組織原則和需求。下列步驟使用的 Google Chrome-預設設定為預設值。
    
3. 瀏覽至 [**&lt;電腦/使用者設定&gt;\Administrative Templates\Google Chrome-預設 Settings\Home 頁面**。
    
4. 連按兩下 [**首頁以使用新索引標籤頁面**，並將它設為 [**已啟用**。
    
5. 瀏覽至 [**&lt;電腦/使用者設定&gt;\Administrative Templates\Google Chrome-預設 Settings\New] 索引標籤] 頁面上**。
    
6. 按兩下 [**設定新的索引標籤頁面 URL**，將它設為 [**已啟用**] 並輸入`https://www.bing.com/business?form=BFBSPR`
    
7. 強制產生 GPO 連結至適當的網域。
    
使用者無法變更 [首頁] 頁面上設定此原則之後。