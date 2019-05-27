---
title: 測試單一登入
ms.author: dawholl
author: dawholl
manager: kellis
ms.date: 09/11/2018
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Priority
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: a220c1bf-7cee-448a-90a3-310284d03e81
description: 減少您的 Windows 10 使用者登入 Microsoft Search 和 Office 365 的提示次數
ms.openlocfilehash: 4eb38901ecda4a3c18d779946a73e6ef7c25c18a
ms.sourcegitcommit: 3e91a6e70b48a0100adfed1b62ba79f2fd1735d2
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/13/2019
ms.locfileid: "34425632"
---
# <a name="test-single-sign-on"></a><span data-ttu-id="28c3d-103">測試單一登入</span><span class="sxs-lookup"><span data-stu-id="28c3d-103">Test single sign-on</span></span>

> [!IMPORTANT]
> <span data-ttu-id="28c3d-104">Bing 設定中的 Microsoft Search 現在可以在 Microsoft 365 管理中心中使用。</span><span class="sxs-lookup"><span data-stu-id="28c3d-104">Microsoft Search in Bing settings are now available in the Microsoft 365 admin center.</span></span> <span data-ttu-id="28c3d-105">從系統管理中心的 [指派搜尋系統管理員](https://docs.microsoft.com/zh-TW/microsoftsearch/setup-microsoft-search#step-2-assign-search-admin-and-search-editor) 開始。</span><span class="sxs-lookup"><span data-stu-id="28c3d-105">Get started by [assigning search admins](https://docs.microsoft.com/en-us/microsoftsearch/setup-microsoft-search#step-2-assign-search-admin-and-search-editor) in your admin center.</span></span>
    
<span data-ttu-id="28c3d-106">單一登入可以減少系統提示使用者登入的次數。</span><span class="sxs-lookup"><span data-stu-id="28c3d-106">Single sign-on reduces the number of times users are prompted to sign in.</span></span> <span data-ttu-id="28c3d-107">透過一小群使用者來測試單一登入能協助找出任何造成阻礙的設定問題。</span><span class="sxs-lookup"><span data-stu-id="28c3d-107">Testing single sign-on with a small group of users will help identify any blocking configuration issues.</span></span> 
  
<span data-ttu-id="28c3d-108">針對 Windows 10 上的 Chrome 使用者，必須先安裝適用於 Chrome 的 Windows 10 和 AAD 登入擴充功能，才能單一登入使用。 </span><span class="sxs-lookup"><span data-stu-id="28c3d-108">For Chrome users on Windows 10, single sign-on will only work if the Windows 10 and AAD sign-in extension for Chrome is installed.</span></span> 
  
## <a name="download-the-windows-10-and-aad-sign-in-extension-for-chrome"></a><span data-ttu-id="28c3d-109">下載適用於 Chrome 的 Windows 10 和 AAD 登入擴充功能</span><span class="sxs-lookup"><span data-stu-id="28c3d-109">Download the Windows 10 and AAD sign-in extension for Chrome</span></span>

<span data-ttu-id="28c3d-110">我們建議您建立群組原則以自動安裝此擴充功能。</span><span class="sxs-lookup"><span data-stu-id="28c3d-110">We recommend that you create a group policy to automatically install this extension.</span></span>
  
1. <span data-ttu-id="28c3d-111">移至Microsoft Search 系統管理入口網站</span><span class="sxs-lookup"><span data-stu-id="28c3d-111">Go to the Microsoft Search Admin portal</span></span>
    
2. <span data-ttu-id="28c3d-112">按一下瀏覽窗格中的 **[工具]**</span><span class="sxs-lookup"><span data-stu-id="28c3d-112">In the navigation pane, click **ADSI Edit**.</span></span>
    
3. <span data-ttu-id="28c3d-113">在 [工具] 清單中，下載**適用於 Chrome 的 Windows 10 和 AAD 登入擴充功能**</span><span class="sxs-lookup"><span data-stu-id="28c3d-113">In the Tools list, download the **Windows 10 and AAD sign-in extension for Chrome**</span></span>
    
4. <span data-ttu-id="28c3d-114">與 Windows 10 上的 Chrome 使用者共用擴充功能</span><span class="sxs-lookup"><span data-stu-id="28c3d-114">Share the extension with Chrome users on Windows 10</span></span>

  

