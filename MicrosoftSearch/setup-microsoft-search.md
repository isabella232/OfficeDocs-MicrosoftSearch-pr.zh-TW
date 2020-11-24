---
title: 設定 Microsoft Search
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
description: 第一次設定 Microsoft Search。
ms.openlocfilehash: 7d0b8e1b4bbb405e254b2fe2d29b11f081f5b460
ms.sourcegitcommit: ac4e261c01262be747341f810d2d1faf220d3961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/23/2020
ms.locfileid: "49382585"
---
# <a name="set-up-microsoft-search"></a><span data-ttu-id="43a86-103">設定 Microsoft Search</span><span class="sxs-lookup"><span data-stu-id="43a86-103">Set up Microsoft Search</span></span>

<span data-ttu-id="43a86-104">Microsoft 搜尋提供方便使用的介面，可協助使用者尋找諸如檔案和檔、內部網站與商務工具、人員和群組、位置與方向、交談及答案等資訊。</span><span class="sxs-lookup"><span data-stu-id="43a86-104">Microsoft Search provides a user-friendly interface to help users find information like files and documents, internal sites and business tools, people and groups, locations and directions, conversations and answers.</span></span> <span data-ttu-id="43a86-105">這樣做的方式是安全地存取所有資料來源，包括電子郵件、檔案、SharePoint 檔案、OneDrive 內容及其他共用資源。</span><span class="sxs-lookup"><span data-stu-id="43a86-105">It does this by securely accessing all data sources, including emails, files, SharePoint files, OneDrive content, and other shared resources as well.</span></span> <span data-ttu-id="43a86-106">使用 [Bing] 中的 Microsoft 搜尋時，您也可以從網際網路取得搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="43a86-106">With Microsoft Search in Bing you can get search results from the internet as well.</span></span>

<span data-ttu-id="43a86-107">若要深入了解 Microsoft Search 功能，請參閱 [Microsoft Search 概觀](overview-microsoft-search.md)。</span><span class="sxs-lookup"><span data-stu-id="43a86-107">To learn more about Microsoft Search features, see [Microsoft Search Overview](overview-microsoft-search.md).</span></span>

## <a name="get-started"></a><span data-ttu-id="43a86-108">開始使用</span><span class="sxs-lookup"><span data-stu-id="43a86-108">Get Started</span></span>

<span data-ttu-id="43a86-109">Microsoft Search 預設會對支援它的所有 Microsoft 應用程式開啟，成為 Microsoft 365 的一部分。</span><span class="sxs-lookup"><span data-stu-id="43a86-109">Microsoft Search is turned on by default for all Microsoft apps that supports it, as a part of Microsoft 365.</span></span> <span data-ttu-id="43a86-110">不需要進行任何設定，但是您可以透過某些基本的管理工作，來改善 Microsoft 的整體搜尋體驗。</span><span class="sxs-lookup"><span data-stu-id="43a86-110">There is no setup required, but you can improve the overall Microsoft Search experience through some basic administrative tasks.</span></span>

<span data-ttu-id="43a86-111">您可透過 Microsoft 365 系統管理中心來管理 Microsoft 搜尋。</span><span class="sxs-lookup"><span data-stu-id="43a86-111">You manage Microsoft Search from Microsoft 365 admin center.</span></span>

1. <span data-ttu-id="43a86-112">在 Microsoft 365 系統管理中心中，移至 [**設定**]  >  [**搜尋 & 智慧**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch)。</span><span class="sxs-lookup"><span data-stu-id="43a86-112">In Microsoft 365 admin center, go to **Settings** > [**Search & intelligence**](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch).</span></span>

<span data-ttu-id="43a86-113">身為系統管理員，請考慮幾個可讓 Microsoft Search 體驗更有效且對組織使用者更友善的事項。</span><span class="sxs-lookup"><span data-stu-id="43a86-113">As an admin you should consider a few things that can make the Microsoft Search experience efficient and user friendly in your organization.</span></span>

## <a name="step-1-assign-search-admin-and-search-editor"></a><span data-ttu-id="43a86-114">步驟1：指派搜尋管理和搜尋編輯器</span><span class="sxs-lookup"><span data-stu-id="43a86-114">Step 1: Assign Search admin and Search editor</span></span>

<span data-ttu-id="43a86-115">在 Microsoft Search 中，您可以藉由將這兩個角色指派給使用者來管理組織的搜尋設定和內容：</span><span class="sxs-lookup"><span data-stu-id="43a86-115">In Microsoft Search, you can manage your organization’s search settings and content by assigning these roles to users:</span></span>

1. <span data-ttu-id="43a86-116">**搜尋系統管理員：** 此角色可以建立及管理搜尋結果內容，並定義查詢設定，以改善組織內的搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="43a86-116">**Search admin:** This role can create and manage search result content and define query settings for improved search results within the organization.</span></span> <span data-ttu-id="43a86-117">搜尋系統管理員負責管理 Microsoft Search 組態，並可執行搜尋編輯者所能執行的所有內容管理工作。</span><span class="sxs-lookup"><span data-stu-id="43a86-117">Search admin manages the Microsoft Search configuration and can perform all of the content-management tasks a Search editor can.</span></span>
2. <span data-ttu-id="43a86-118">**搜尋編輯者：** 在 Microsoft 365 系統管理中心中建立、管理和刪除 Microsoft Search 的內容。</span><span class="sxs-lookup"><span data-stu-id="43a86-118">**Search editor:** Creates, manages, and deletes content for Microsoft Search in the Microsoft 365 admin center.</span></span> <span data-ttu-id="43a86-119">此角色可以建立及管理編輯性的內容，例如：常見問題集和解答、重要的地點和位置、經常搜尋和使用的網站與應用程式。</span><span class="sxs-lookup"><span data-stu-id="43a86-119">This role can create and manage editorial content, such as frequently asked questions and answers, important places and locations, frequently searched and used sites and apps.</span></span>

<span data-ttu-id="43a86-120">目前，搜尋系統管理員和搜尋編輯者角色都必須由全域系統管理員來指派。如需詳細資訊，請參閱[指派系統管理員角色](https://docs.microsoft.com/office365/admin/add-users/assign-admin-roles?view=o365-worldwide)。</span><span class="sxs-lookup"><span data-stu-id="43a86-120">Currently, the Search admin and Search editor roles must be assigned by a global admin. For more information, see [Assign admin roles](https://docs.microsoft.com/office365/admin/add-users/assign-admin-roles?view=o365-worldwide).</span></span>

<span data-ttu-id="43a86-121">搜尋系統管理員會直接影響使用者的搜尋體驗。</span><span class="sxs-lookup"><span data-stu-id="43a86-121">Search administrators directly influence the search experience for end users.</span></span> <span data-ttu-id="43a86-122">這包括選擇想要呈現給使用者的結果類型。</span><span class="sxs-lookup"><span data-stu-id="43a86-122">This includes choosing the types of results you want to surface to your users.</span></span> <span data-ttu-id="43a86-123">由一個人針對組織中使用者所搜尋的許多不同主題選擇並建立授權內容，可能很困難。</span><span class="sxs-lookup"><span data-stu-id="43a86-123">It may be difficult for one person to choose and create authoritative content on many different topics that users search for in an organization.</span></span> <span data-ttu-id="43a86-124">建議您運用主題專家 (SME) 與其他使用者的專業技術與知識 (將他們新增為搜尋編輯者)。</span><span class="sxs-lookup"><span data-stu-id="43a86-124">We recommend that you leverage the expertise and knowledge of subject matter experts (SME) and other users by adding them as Search editors.</span></span>

## <a name="step-2-create-answers"></a><span data-ttu-id="43a86-125">步驟2：建立答案</span><span class="sxs-lookup"><span data-stu-id="43a86-125">Step 2: Create answers</span></span>

<span data-ttu-id="43a86-126">Microsoft Search 會提供工具給系統管理員，讓其用來為使用者建立功能強大的搜尋體驗。</span><span class="sxs-lookup"><span data-stu-id="43a86-126">Microsoft Search provides administrators with tools that they can use to build a robust search experience for their users.</span></span> <span data-ttu-id="43a86-127">在 Microsoft Search 中，系統管理員有三個不同的搜尋內容可以建立，以取得更好的搜尋體驗，並改善內容的 "findability"：</span><span class="sxs-lookup"><span data-stu-id="43a86-127">In Microsoft Search, administrators have three different search contents that they can create for a better search experience and to improve the "findability" of content:</span></span>

<span data-ttu-id="43a86-128">書簽是最常使用的答案類型。</span><span class="sxs-lookup"><span data-stu-id="43a86-128">Bookmarks are the most commonly used answer type.</span></span> <span data-ttu-id="43a86-129">他們會將使用者查詢的最佳結果提升至搜尋結果的最上層，讓使用者能輕鬆找到他們所要尋找的專案。</span><span class="sxs-lookup"><span data-stu-id="43a86-129">They promote the best possible results for your users’ queries to the top of the search results and make it easy for your users to find what they are looking for.</span></span>
<span data-ttu-id="43a86-130">可供所有人使用的資訊性內容;例如，有關公司的資訊、Windows 和 Office 應用程式的相關資訊等等。組織中的人員一般會在日常工作中搜尋的內容。</span><span class="sxs-lookup"><span data-stu-id="43a86-130">Informational content that is available for everyone; for example, information about the company, help for Windows and Office apps, etc. Content that people in the organization generally search for in their day-to-day work.</span></span> <span data-ttu-id="43a86-131">常見的工作相關搜尋包括員工福利、時間與支出報告、提交訂購單和取得 IT 服務協助等。</span><span class="sxs-lookup"><span data-stu-id="43a86-131">Common work-related searches include employee benefits, time and expense reporting, submitting purchase orders, and getting help from IT services.</span></span>

<span data-ttu-id="43a86-132">若要建立及管理答案，請參閱 [規劃您的內容](plan-your-content.md)。</span><span class="sxs-lookup"><span data-stu-id="43a86-132">For creating and managing answers, see [Plan your content](plan-your-content.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="43a86-133">後續步驟</span><span class="sxs-lookup"><span data-stu-id="43a86-133">Next steps</span></span>

<span data-ttu-id="43a86-134">如果您想要深入瞭解您的使用者如何使用 Microsoft 搜尋，請參閱下列文章：</span><span class="sxs-lookup"><span data-stu-id="43a86-134">If you'd like to learn more about how your users will use Microsoft Search, see the following articles:</span></span>

- [<span data-ttu-id="43a86-135">在 Office 中使用 Microsoft Search 找到所需的內容</span><span class="sxs-lookup"><span data-stu-id="43a86-135">Find what you need with Microsoft Search in Office</span></span>](https://support.office.com/article/find-what-you-need-with-microsoft-search-in-office-2457d4d8-48a8-4ad4-ab89-5a0657aa8446)
- [<span data-ttu-id="43a86-136">Office 365 訓練中心</span><span class="sxs-lookup"><span data-stu-id="43a86-136">Office 365 Training Center</span></span>](https://support.office.com/office-training-center)
- [<span data-ttu-id="43a86-137">Microsoft 搜尋中心</span><span class="sxs-lookup"><span data-stu-id="43a86-137">Microsoft Search Center</span></span>](https://support.office.com/article/-working-title-microsoft-search-center-b8bf5a2c-7515-40a9-9a6a-b8ed382c86bc)
