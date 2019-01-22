---
title: 測試單一登入
ms.author: dawholl
author: dawholl
manager: kellis
ms.date: 09/11/2018
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: a220c1bf-7cee-448a-90a3-310284d03e81
description: 減少系統會提示您 Windows 10 使用者登入 Microsoft 搜尋和 Office 365 的次數
ms.openlocfilehash: 4157707d58ead304449805c8fd16578690ac01a6
ms.sourcegitcommit: bf52cc63b75f2e0324a716fe65da47702956b722
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/18/2019
ms.locfileid: "29380137"
---
# <a name="test-single-sign-on"></a><span data-ttu-id="8686a-103">測試單一登入</span><span class="sxs-lookup"><span data-stu-id="8686a-103">Test single sign-on</span></span>

<span data-ttu-id="8686a-p101">單一登入減少系統會提示使用者登入的次數。單一登入與使用者一小群測試有助於找出任何封鎖的組態問題。</span><span class="sxs-lookup"><span data-stu-id="8686a-p101">Single sign-on reduces the number of times users are prompted to sign in. Testing single sign-on with a small group of users will help identify any blocking configuration issues.</span></span> 
  
<span data-ttu-id="8686a-106">Chrome 上的使用者 Windows 10、 單一登入才有作用安裝 Windows 10 和 AAD 登入副檔名的 Chrome。</span><span class="sxs-lookup"><span data-stu-id="8686a-106">For Chrome users on Windows 10, single sign-on will only work if the Windows 10 and AAD sign-in extension for Chrome is installed.</span></span> 
  
## <a name="download-the-windows-10-and-aad-sign-in-extension-for-chrome"></a><span data-ttu-id="8686a-107">下載 Windows 10 和 AAD 登入副檔名的 Chrome</span><span class="sxs-lookup"><span data-stu-id="8686a-107">Download the Windows 10 and AAD sign-in extension for Chrome</span></span>

<span data-ttu-id="8686a-108">我們建議您建立群組原則會自動安裝此延伸。</span><span class="sxs-lookup"><span data-stu-id="8686a-108">We recommend that you create a group policy to automatically install this extension.</span></span>
  
1. <span data-ttu-id="8686a-109">移至 Microsoft 搜尋系統入口網站</span><span class="sxs-lookup"><span data-stu-id="8686a-109">Go to the Microsoft Search Admin portal</span></span>
    
2. <span data-ttu-id="8686a-110">在功能窗格] 中按一下 [**工具]**</span><span class="sxs-lookup"><span data-stu-id="8686a-110">In the navigation pane, click **Tools**</span></span>
    
3. <span data-ttu-id="8686a-111">在 [工具] 清單中，下載**Windows 10 和 AAD 登入的 Chrome 延伸**</span><span class="sxs-lookup"><span data-stu-id="8686a-111">In the Tools list, download the **Windows 10 and AAD sign-in extension for Chrome**</span></span>
    
4. <span data-ttu-id="8686a-112">與 Windows 10 的 Chrome 使用者共用副檔名</span><span class="sxs-lookup"><span data-stu-id="8686a-112">Share the extension with Chrome users on Windows 10</span></span>

  

