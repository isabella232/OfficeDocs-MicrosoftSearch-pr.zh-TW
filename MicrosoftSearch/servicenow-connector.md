---
title: Microsoft 搜尋的 ServiceNow 連接器
ms.author: monaray
author: monaray97
manager: jameslau
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 設定 Microsoft 搜尋的 ServiceNow 連接器
ms.openlocfilehash: 29e8e490f114ce8537ddb973ed16ccb34f24f82f
ms.sourcegitcommit: 988c37610e71f9784b486660400aecaa7bed40b0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "47422863"
---
# <a name="servicenow-connector"></a><span data-ttu-id="efe4f-103">ServiceNow 連接器</span><span class="sxs-lookup"><span data-stu-id="efe4f-103">ServiceNow connector</span></span>

<span data-ttu-id="efe4f-104">使用 ServiceNow 連接器，您的組織可以為組織內所有使用者顯示的知識庫文章編制索引。</span><span class="sxs-lookup"><span data-stu-id="efe4f-104">With the ServiceNow connector, your organization can index knowledge-base articles that are visible to all users within your organization.</span></span> <span data-ttu-id="efe4f-105">從 ServiceNow 設定連接器和索引內容之後，使用者可以從任何 Microsoft 搜尋用戶端搜尋這些文章。</span><span class="sxs-lookup"><span data-stu-id="efe4f-105">After you configure the connector and index content from ServiceNow, end users can search for those articles from any Microsoft Search client.</span></span>  

<span data-ttu-id="efe4f-106">本文適用于 Microsoft 365 系統管理員或任何設定、執行及監視 ServiceNow 連接器的人員。</span><span class="sxs-lookup"><span data-stu-id="efe4f-106">This article is for Microsoft 365 administrators or anyone who configures, runs, and monitors a ServiceNow connector.</span></span> <span data-ttu-id="efe4f-107">它說明如何設定連接器和連接器功能、限制及疑難排解技術。</span><span class="sxs-lookup"><span data-stu-id="efe4f-107">It explains how to configure your connector and connector capabilities, limitations, and troubleshooting techniques.</span></span>

## <a name="connect-to-a-data-source"></a><span data-ttu-id="efe4f-108">連接到資料來源</span><span class="sxs-lookup"><span data-stu-id="efe4f-108">Connect to a data source</span></span>

<span data-ttu-id="efe4f-109">若要連線至您的 ServiceNow 資料，您需要組織的 **ServiceNow 實例 URL**、此帳戶的認證，以及 OAuth 驗證的用戶端識別碼和用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="efe4f-109">To connect to your ServiceNow data, you need your organization's **ServiceNow instance URL**, credentials for this account, and the Client ID and Client Secret for OAuth authentication.</span></span>  

<span data-ttu-id="efe4f-110">組織的 **ServiceNow 實例 URL** 一般會類似 **HTTPs:// &lt; 您的組織網域> service-now.com**。</span><span class="sxs-lookup"><span data-stu-id="efe4f-110">Your organization’s **ServiceNow instance URL** typically looks like **https://&lt;your-organization-domain>.service-now.com**.</span></span> <span data-ttu-id="efe4f-111">除了此 URL 之外，您還需要一個帳戶，用以設定 ServiceNow 的連線，以及允許 Microsoft 搜尋依重新整理排程，定期更新 ServiceNow 中的文章。</span><span class="sxs-lookup"><span data-stu-id="efe4f-111">Along with this URL, you will need an account for setting up the connection to ServiceNow as well as for allowing Microsoft Search to periodically update the articles from ServiceNow based on the refresh schedule.</span></span>

<span data-ttu-id="efe4f-112">若要驗證及同步處理 ServiceNow 中的內容，請選擇兩個支援的方法之一：</span><span class="sxs-lookup"><span data-stu-id="efe4f-112">To authenticate and sync content from ServiceNow, choose one of two supported methods:</span></span>

1. <span data-ttu-id="efe4f-113">基本驗證</span><span class="sxs-lookup"><span data-stu-id="efe4f-113">Basic authentication</span></span>
2. <span data-ttu-id="efe4f-114">OAuth (建議) </span><span class="sxs-lookup"><span data-stu-id="efe4f-114">OAuth (recommended)</span></span>

> [!Note]
> <span data-ttu-id="efe4f-115">若要使用 OAuth 進行驗證，ServiceNow 系統管理員必須布建 ServiceNow 實例中的端點，這樣 Microsoft Search 應用程式才能存取該實例。</span><span class="sxs-lookup"><span data-stu-id="efe4f-115">To use OAuth for authentication, a ServiceNow admin needs to provision an endpoint in your ServiceNow instance, so that the Microsoft Search app can access the instance.</span></span> <span data-ttu-id="efe4f-116">若要深入瞭解，請參閱在 ServiceNow 檔中 [建立用戶端存取實例的端點](https://docs.servicenow.com/bundle/newyork-platform-administration/page/administer/security/task/t_CreateEndpointforExternalClients.html) 。</span><span class="sxs-lookup"><span data-stu-id="efe4f-116">To learn more, see [Create an endpoint for clients to access the instance](https://docs.servicenow.com/bundle/newyork-platform-administration/page/administer/security/task/t_CreateEndpointforExternalClients.html) in the ServiceNow documentation.</span></span>

<span data-ttu-id="efe4f-117">下表提供如何填寫端點建立表單的指導方針：</span><span class="sxs-lookup"><span data-stu-id="efe4f-117">The following table provides guidance on how to fill out the endpoint creation form:</span></span>

<span data-ttu-id="efe4f-118">**Field**</span><span class="sxs-lookup"><span data-stu-id="efe4f-118">**Field**</span></span> | <span data-ttu-id="efe4f-119">**描述**</span><span class="sxs-lookup"><span data-stu-id="efe4f-119">**Description**</span></span> | <span data-ttu-id="efe4f-120">**建議值**</span><span class="sxs-lookup"><span data-stu-id="efe4f-120">**Recommended Value**</span></span>
--- | --- | ---
<span data-ttu-id="efe4f-121">姓名</span><span class="sxs-lookup"><span data-stu-id="efe4f-121">Name</span></span> | <span data-ttu-id="efe4f-122">此唯一值可識別您需要 OAuth 存取的應用程式。</span><span class="sxs-lookup"><span data-stu-id="efe4f-122">This unique value identifies the application that you require OAuth access for.</span></span> | <span data-ttu-id="efe4f-123">Microsoft 搜尋</span><span class="sxs-lookup"><span data-stu-id="efe4f-123">Microsoft Search</span></span>
<span data-ttu-id="efe4f-124">用戶端識別碼</span><span class="sxs-lookup"><span data-stu-id="efe4f-124">Client ID</span></span> | <span data-ttu-id="efe4f-125">應用程式的唯讀、自動產生的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="efe4f-125">A read-only, auto-generated unique ID for the application.</span></span> <span data-ttu-id="efe4f-126">當實例要求存取權杖時，會使用用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="efe4f-126">The instance uses the client ID when it requests an access token.</span></span> | <span data-ttu-id="efe4f-127">NA</span><span class="sxs-lookup"><span data-stu-id="efe4f-127">NA</span></span>
<span data-ttu-id="efe4f-128">用戶端密碼</span><span class="sxs-lookup"><span data-stu-id="efe4f-128">Client secret</span></span> | <span data-ttu-id="efe4f-129">使用此共用的機密字串，ServiceNow 實例和 Microsoft 搜尋會授權彼此間的通訊。</span><span class="sxs-lookup"><span data-stu-id="efe4f-129">With this shared secret string, the ServiceNow instance and Microsoft Search authorize communications with each another.</span></span> | <span data-ttu-id="efe4f-130">請將此視為密碼，遵循安全性最佳作法。</span><span class="sxs-lookup"><span data-stu-id="efe4f-130">Follow security best-practices by treating this as a password.</span></span>
<span data-ttu-id="efe4f-131">重新導向 URL</span><span class="sxs-lookup"><span data-stu-id="efe4f-131">Redirect URL</span></span> | <span data-ttu-id="efe4f-132">授權伺服器重新導向所需的回撥 URL。</span><span class="sxs-lookup"><span data-stu-id="efe4f-132">A required callback URL that the authorization server redirects to.</span></span> | https://gcs.office.com/v1.0/admin/oauth/callback
<span data-ttu-id="efe4f-133">標誌 URL</span><span class="sxs-lookup"><span data-stu-id="efe4f-133">Logo URL</span></span> | <span data-ttu-id="efe4f-134">包含應用程式標誌之圖像的 URL。</span><span class="sxs-lookup"><span data-stu-id="efe4f-134">A URL that contains the image for the application logo.</span></span> | <span data-ttu-id="efe4f-135">NA</span><span class="sxs-lookup"><span data-stu-id="efe4f-135">NA</span></span>
<span data-ttu-id="efe4f-136">作用中</span><span class="sxs-lookup"><span data-stu-id="efe4f-136">Active</span></span> | <span data-ttu-id="efe4f-137">選取此核取方塊，讓應用程式登錄成為使用中。</span><span class="sxs-lookup"><span data-stu-id="efe4f-137">Select the check box to make the application registry active.</span></span> | <span data-ttu-id="efe4f-138">設定為 active</span><span class="sxs-lookup"><span data-stu-id="efe4f-138">Set to active</span></span>
<span data-ttu-id="efe4f-139">重新整理權杖生命週期</span><span class="sxs-lookup"><span data-stu-id="efe4f-139">Refresh token lifespan</span></span> | <span data-ttu-id="efe4f-140">重新整理權杖有效的秒數。</span><span class="sxs-lookup"><span data-stu-id="efe4f-140">The number of seconds that a refresh token is valid.</span></span> <span data-ttu-id="efe4f-141">根據預設，重新整理權杖會在100天內到期 (8640000 秒) 。</span><span class="sxs-lookup"><span data-stu-id="efe4f-141">By default, refresh tokens expire in 100 days (8640000 seconds).</span></span> | <span data-ttu-id="efe4f-142">31536000 (1 年) </span><span class="sxs-lookup"><span data-stu-id="efe4f-142">31,536,000 (1 year)</span></span>
<span data-ttu-id="efe4f-143">存取權杖使用壽命</span><span class="sxs-lookup"><span data-stu-id="efe4f-143">Access token lifespan</span></span> | <span data-ttu-id="efe4f-144">存取權杖有效的秒數。</span><span class="sxs-lookup"><span data-stu-id="efe4f-144">The number of seconds that an access token is valid.</span></span> | <span data-ttu-id="efe4f-145">43200 (12 小時) </span><span class="sxs-lookup"><span data-stu-id="efe4f-145">43,200 (12 hours)</span></span>

## <a name="set-a-sync-filter"></a><span data-ttu-id="efe4f-146">設定同步篩選</span><span class="sxs-lookup"><span data-stu-id="efe4f-146">Set a sync filter</span></span>

<span data-ttu-id="efe4f-147">使用 sync 篩選，您可以指定同步處理文章的條件。</span><span class="sxs-lookup"><span data-stu-id="efe4f-147">With a sync filter, you can specify conditions for syncing articles.</span></span> <span data-ttu-id="efe4f-148">它就像是**SQL Select**語句中的**Where**子句。</span><span class="sxs-lookup"><span data-stu-id="efe4f-148">It's like a **Where** clause in a **SQL Select** statement.</span></span> <span data-ttu-id="efe4f-149">例如，您可以選擇只為發佈和使用中的文章編制索引。</span><span class="sxs-lookup"><span data-stu-id="efe4f-149">For example, you can choose to index only articles that are published and active.</span></span> <span data-ttu-id="efe4f-150">[SyncNow 設定] 頁面會說明如何捕獲和設定同步處理篩選。</span><span class="sxs-lookup"><span data-stu-id="efe4f-150">The SyncNow configuration page describes how to capture and set a sync filter.</span></span>

## <a name="manage-the-search-schema"></a><span data-ttu-id="efe4f-151">管理搜尋結構描述</span><span class="sxs-lookup"><span data-stu-id="efe4f-151">Manage the search schema</span></span>

<span data-ttu-id="efe4f-152">成功連接後，請設定搜尋架構對應。</span><span class="sxs-lookup"><span data-stu-id="efe4f-152">After successful connection, configure the search schema mapping.</span></span> <span data-ttu-id="efe4f-153">您可以選擇哪些屬性可供**查詢**、可搜尋及可**供\*\*\*\*檢索**。</span><span class="sxs-lookup"><span data-stu-id="efe4f-153">You can choose which properties to make **queryable**, **searchable**, and **retrievable**.</span></span>

## <a name="manage-search-permissions"></a><span data-ttu-id="efe4f-154">管理搜尋許可權</span><span class="sxs-lookup"><span data-stu-id="efe4f-154">Manage search permissions</span></span>

<span data-ttu-id="efe4f-155">ServiceNow 連接器只支援 **所有人都**能看見的搜尋許可權。</span><span class="sxs-lookup"><span data-stu-id="efe4f-155">The ServiceNow connector only supports search permissions visible to **Everyone**.</span></span> <span data-ttu-id="efe4f-156">已編制索引的資料會顯示在搜尋結果中，並對組織中的所有使用者顯示。</span><span class="sxs-lookup"><span data-stu-id="efe4f-156">Indexed data appears in the search results and is visible to all users in the organization.</span></span>

## <a name="set-the-refresh-schedule"></a><span data-ttu-id="efe4f-157">設定重新整理排程</span><span class="sxs-lookup"><span data-stu-id="efe4f-157">Set the refresh schedule</span></span>

<span data-ttu-id="efe4f-158">ServiceNow 連接器支援完整和累加編目的更新排程。</span><span class="sxs-lookup"><span data-stu-id="efe4f-158">The ServiceNow connector supports refresh schedules for both full and incremental crawls.</span></span> <span data-ttu-id="efe4f-159">我們建議您同時設定兩者。</span><span class="sxs-lookup"><span data-stu-id="efe4f-159">We recommend that you set both.</span></span>

<span data-ttu-id="efe4f-160">完整編目排程會找到先前同步處理至 Microsoft 搜尋索引的已刪除文章，以及任何移出同步篩選的文章。</span><span class="sxs-lookup"><span data-stu-id="efe4f-160">A full crawl schedule finds deleted articles that were previously synced to the Microsoft Search index and any articles that moved out of the sync filter.</span></span> <span data-ttu-id="efe4f-161">當您第一次連線至 ServiceNow 時，會執行完整編目以同步處理所有知識文庫文章。</span><span class="sxs-lookup"><span data-stu-id="efe4f-161">When you first connect to ServiceNow, a full crawl runs to sync all the knowledge-base articles.</span></span> <span data-ttu-id="efe4f-162">若要同步處理新專案並進行更新，您必須排程累加編目。</span><span class="sxs-lookup"><span data-stu-id="efe4f-162">To sync new items and make updates, you need to schedule incremental crawls.</span></span>

<span data-ttu-id="efe4f-163">建議的預設值為一天的完整編目及四小時為增量編目。</span><span class="sxs-lookup"><span data-stu-id="efe4f-163">The recommended default is one day for a full crawl and four hours for an incremental crawl.</span></span>
