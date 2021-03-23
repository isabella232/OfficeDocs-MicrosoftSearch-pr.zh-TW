---
title: 線上和 Microsoft 搜尋 SharePoint 中的傳統頁面
ms.author: keremy
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
description: 在傳統的 SharePoint 頁面上使用 Microsoft 搜尋
ms.openlocfilehash: 33215c730d34c14f8ce1d55e93730615688f1e2a
ms.sourcegitcommit: 5df252e6d0bd67bb1b4c59418aceca8369f5fe42
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/23/2021
ms.locfileid: "51031429"
---
# <a name="classic-pages-and-microsoft-search"></a>傳統頁面和 Microsoft 搜尋

SharePoint 現代網站之前建立的網站使用傳統搜尋方塊和傳統搜尋結果體驗。 我們將推出使用 Microsoft Search 的新式搜尋體驗來開始使用預設傳統頁面的功能，其可提供具有較高相關性的個人化結果。

針對所有網站（包括傳統）都建議使用 Microsoft Search，但是如果您的傳統網站使用自訂主版頁面和/或您已自訂傳統的搜尋結果體驗，我們將會自動偵測這些自訂，而不會切換至 Microsoft 搜尋。

## <a name="classic-sites-that-will-automatically-switch-to-microsoft-search"></a>將會自動切換至 Microsoft 搜尋的傳統網站

當下列所有條件皆為真時，傳統網站會開始使用 Microsoft Search：

* 網站是以小組網站範本為基礎， (例如 STS#0 和 STS # 1) 。
* 網站未開啟發佈功能。
* 網站不會使用自訂主版頁面 (不同的主版頁面，而不是 oslo 或西雅圖。主圖形) 。
* 在預設結果來源上，除了為網站、網站集合或租使用者新增升級的結果之外，還沒有任何使用中的查詢規則。
* 預設結果來源上沒有網站或網站集合的自訂結果類型。
* 使用下列所述的 *SearchBoxInNavBar* 設定，不會選擇網站或網站集合的參數。

切換至 Microsoft 搜尋後，網站中的傳統頁面會開始顯示套件導覽列中的 [搜尋] 方塊，並移除頁面上的 [傳統搜尋] 方塊。 然後，當使用者搜尋字詞時，結果會以 Microsoft 搜尋的新式搜尋體驗來顯示。

## <a name="staying-with-the-classic-search-experience"></a>保持傳統搜尋體驗

如果您的網站符合以上所列的準則，但您不想要切換至 Microsoft 搜尋體驗，您可以選擇以網站或網站集合擁有者的身分使用下列命令。

您可以在切換之前或之後的任何時間使用此命令，這樣就能輕鬆回到先前所用的搜尋體驗。

若要執行下列命令，您會使用 PowerShell 搭配 SharePoint PnP PowerShell 擴充。 您可以安裝並深入瞭解如何開始 [這裡](/powershell/sharepoint/sharepoint-pnp/sharepoint-pnp-cmdlets?view=sharepoint-ps)。 您將使用下列命令登入您的網站或網站集合：

```powershell
Connect-PnPOnline -Url <yoursiteurl> -UseWebLogin
# this will prompt you to sign in to your site. Use the site owner credentials.
```

若要保持網站的傳統搜尋體驗，請執行下列命令：

```powershell
Set-PnPSearchSettings -Scope Web -SearchBoxInNavBar ModernOnly
# ModernOnly | Inherit
```

或者，如果您想要為網站集合中的所有網站設定它，您可以使用此命令：

```powershell
Set-PnPSearchSettings -Scope Site -SearchBoxInNavBar ModernOnly
# ModernOnly | Inherit
```

## <a name="opting-into-microsoft-search"></a>加入 Microsoft 搜尋

針對不符合以上列出之準則的網站，或針對選擇要保持傳統之網站集合中的特定網站，您可以手動啟用 Microsoft 搜尋體驗。

若要變更特定網站的此設定，您可以使用此命令：

```powershell
Set-PnPSearchSettings -Scope Web -SearchBoxInNavBar AllPages
# AllPages | Inherit
```

若要為網站集合中的所有網站設定它，您可以使用此命令：

```powershell
Set-PnPSearchSettings -Scope Site -SearchBoxInNavBar AllPages
# AllPages | Inherit
```

> [!NOTE]
> 您可以針對包含 "STS"、"CMSPUBLISHING"、"BLANKINTERNET" 和「GROUP」 ) 的小組網站或發佈網站 (範本識別碼，手動啟用 Microsoft Search。