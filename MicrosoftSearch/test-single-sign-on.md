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
ROBOTS: NOINDEX
description: 減少您的 Windows 10 使用者登入 Microsoft Search 和 Office 365 的提示次數
ms.openlocfilehash: c05a8ffcc973926add551bdbb20273b41ea23bc0
ms.sourcegitcommit: be2e837d9b087bffe6ce40d72d7ae58a8fcdf3fe
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/30/2019
ms.locfileid: "34591042"
---
# <a name="test-single-sign-on"></a><span data-ttu-id="7b2f3-103">測試單一登入</span><span class="sxs-lookup"><span data-stu-id="7b2f3-103">Test single sign-on</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7b2f3-104">本文章適用 Bing 系統管理入口網站中的 Microsoft Search。</span><span class="sxs-lookup"><span data-stu-id="7b2f3-104">This article applies to the Microsoft Search in Bing admin portal.</span></span> <span data-ttu-id="7b2f3-105">我們正在將入口網站移至 Microsoft 365 系統管理中心，完成之後入口網站將會移除。</span><span class="sxs-lookup"><span data-stu-id="7b2f3-105">We’re moving the portal to the Microsoft 365 admin center, and then it will be removed.</span></span> <span data-ttu-id="7b2f3-106">我們建議您使用 Microsoft 365 系統管理中心開始。</span><span class="sxs-lookup"><span data-stu-id="7b2f3-106">We recommend that you use the Microsoft 365 admin center to get started.</span></span> <span data-ttu-id="7b2f3-107">[Microsoft Search 概觀](overview-microsoft-search.md)。</span><span class="sxs-lookup"><span data-stu-id="7b2f3-107">[Overview of Microsoft Graph](overview-microsoft-search.md)</span></span>
    
<span data-ttu-id="7b2f3-108">單一登入可以減少系統提示使用者登入的次數。</span><span class="sxs-lookup"><span data-stu-id="7b2f3-108">Single sign-on reduces the number of times users are prompted to sign in.</span></span> <span data-ttu-id="7b2f3-109">透過一小群使用者來測試單一登入能協助找出任何造成阻礙的設定問題。</span><span class="sxs-lookup"><span data-stu-id="7b2f3-109">Testing single sign-on with a small group of users will help identify any blocking configuration issues.</span></span> 
  
<span data-ttu-id="7b2f3-110">針對 Windows 10 上的 Chrome 使用者，必須先安裝適用於 Chrome 的 Windows 10 和 AAD 登入擴充功能，才能單一登入使用。 </span><span class="sxs-lookup"><span data-stu-id="7b2f3-110">For Chrome users on Windows 10, single sign-on will only work if the Windows 10 and AAD sign-in extension for Chrome is installed.</span></span> 
  
## <a name="download-the-windows-10-and-aad-sign-in-extension-for-chrome"></a><span data-ttu-id="7b2f3-111">下載適用於 Chrome 的 Windows 10 和 AAD 登入擴充功能</span><span class="sxs-lookup"><span data-stu-id="7b2f3-111">Download the Windows 10 and AAD sign-in extension for Chrome</span></span>

<span data-ttu-id="7b2f3-112">我們建議您建立群組原則以自動安裝此擴充功能。</span><span class="sxs-lookup"><span data-stu-id="7b2f3-112">We recommend that you create a group policy to automatically install this extension.</span></span>
  
1. <span data-ttu-id="7b2f3-113">移至Microsoft Search 系統管理入口網站</span><span class="sxs-lookup"><span data-stu-id="7b2f3-113">Go to the Microsoft Search Admin portal</span></span>
    
2. <span data-ttu-id="7b2f3-114">按一下瀏覽窗格中的 **[工具]**</span><span class="sxs-lookup"><span data-stu-id="7b2f3-114">In the navigation pane, click **ADSI Edit**.</span></span>
    
3. <span data-ttu-id="7b2f3-115">在 [工具] 清單中，下載**適用於 Chrome 的 Windows 10 和 AAD 登入擴充功能**</span><span class="sxs-lookup"><span data-stu-id="7b2f3-115">In the Tools list, download the **Windows 10 and AAD sign-in extension for Chrome**</span></span>
    
4. <span data-ttu-id="7b2f3-116">與 Windows 10 上的 Chrome 使用者共用擴充功能</span><span class="sxs-lookup"><span data-stu-id="7b2f3-116">Share the extension with Chrome users on Windows 10</span></span>

  

