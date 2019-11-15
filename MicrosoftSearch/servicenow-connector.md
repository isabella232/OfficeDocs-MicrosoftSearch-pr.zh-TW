---
title: Microsoft Search ServiceNow 連接器
ms.author: v-pamcn
author: TrishaMc1
manager: mnirkhe
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 設定 Microsoft Search ServiceNow 連接器
ms.openlocfilehash: 78b2831e9a52b6bf0204b5a6b2aba147b529b3f5
ms.sourcegitcommit: 21361af7c244ffd6ff8689fd0ff0daa359bf4129
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/14/2019
ms.locfileid: "38626952"
---
# <a name="servicenow-connector"></a><span data-ttu-id="a1494-103">ServiceNow 連接器</span><span class="sxs-lookup"><span data-stu-id="a1494-103">ServiceNow connector</span></span>

<span data-ttu-id="a1494-104">使用 ServiceNow 連接器，您的組織可編製索引之組織內的所有使用者都都能看見知識庫文章。</span><span class="sxs-lookup"><span data-stu-id="a1494-104">With the ServiceNow connector, your organization can index knowledge-base articles that are visible to all users within your organization.</span></span> <span data-ttu-id="a1494-105">您設定的連接器和 ServiceNow 從內容索引之後，使用者可以搜尋任何 Microsoft 搜尋用戶端從這些文章。</span><span class="sxs-lookup"><span data-stu-id="a1494-105">After you configure the connector and index content from ServiceNow, end users can search for those articles from any Microsoft Search client.</span></span>  

<span data-ttu-id="a1494-106">本文適用於 Microsoft 365 系統管理員或人設定、 執行，並監視 ServiceNow 連接器。</span><span class="sxs-lookup"><span data-stu-id="a1494-106">This article is for Microsoft 365 administrators or anyone who configures, runs, and monitors a ServiceNow connector.</span></span> <span data-ttu-id="a1494-107">本文說明如何設定連接器，連接器功能、 限制和疑難排解技巧。</span><span class="sxs-lookup"><span data-stu-id="a1494-107">It explains how to configure your connector and connector capabilities, limitations, and troubleshooting techniques.</span></span>

## <a name="connect-to-a-data-source"></a><span data-ttu-id="a1494-108">連線至資料來源</span><span class="sxs-lookup"><span data-stu-id="a1494-108">Connect to a data source</span></span>
<span data-ttu-id="a1494-109">若要連線至您 ServiceNow 資料，您需要您的組織**ServiceNow 執行個體的 URL**，這個帳戶]，和認證的用戶端識別碼和用戶端密碼的 OAuth 驗證。</span><span class="sxs-lookup"><span data-stu-id="a1494-109">To connect to your ServiceNow data, you need your organization's **ServiceNow instance URL**, credentials for this account, and the Client ID and Client Secret for OAuth authentication.</span></span>  

<span data-ttu-id="a1494-110">您的組織**ServiceNow 執行個體的 URL**通常看起來像**https://&lt;您組織網域>.service now.com**。</span><span class="sxs-lookup"><span data-stu-id="a1494-110">Your organization’s **ServiceNow instance URL** typically looks like **https://&lt;your-organization-domain>.service-now.com**.</span></span> <span data-ttu-id="a1494-111">此 URL，以及您需要帳戶設定以及 ServiceNow 的連線與允許 Microsoft Search 定期更新從 ServiceNow 重新整理排程為基礎的文章。</span><span class="sxs-lookup"><span data-stu-id="a1494-111">Along with this URL, you will need an account for setting up the connection to ServiceNow as well as for allowing Microsoft Search to periodically update the articles from ServiceNow based on the refresh schedule.</span></span>

<span data-ttu-id="a1494-112">若要驗證，並從 ServiceNow 內容同步處理，選擇兩種支援的方法之一：</span><span class="sxs-lookup"><span data-stu-id="a1494-112">To authenticate and sync content from ServiceNow, choose one of two supported methods:</span></span> 
1. <span data-ttu-id="a1494-113">基本驗證</span><span class="sxs-lookup"><span data-stu-id="a1494-113">Basic authentication</span></span> 
2. <span data-ttu-id="a1494-114">OAuth （建議使用）</span><span class="sxs-lookup"><span data-stu-id="a1494-114">OAuth (recommended)</span></span>

> [!Note]
> <span data-ttu-id="a1494-115">若要使用 OAuth 進行驗證，ServiceNow 系統管理員必須佈建端點 ServiceNow 執行個體，以便 Microsoft 的搜尋應用程式可以存取執行個體。</span><span class="sxs-lookup"><span data-stu-id="a1494-115">To use OAuth for authentication, a ServiceNow admin needs to provision an endpoint in your ServiceNow instance, so that the Microsoft Search app can access the instance.</span></span> <span data-ttu-id="a1494-116">若要深入了解，請參閱 ServiceNow 文件中的[建立用戶端存取之執行個體的端點](https://docs.servicenow.com/bundle/newyork-platform-administration/page/administer/security/task/t_CreateEndpointforExternalClients.html)。</span><span class="sxs-lookup"><span data-stu-id="a1494-116">To learn more, see [Create an endpoint for clients to access the instance](https://docs.servicenow.com/bundle/newyork-platform-administration/page/administer/security/task/t_CreateEndpointforExternalClients.html) in the ServiceNow documentation.</span></span>

<span data-ttu-id="a1494-117">下表提供如何填寫端點建立表單的指引：</span><span class="sxs-lookup"><span data-stu-id="a1494-117">The following table provides guidance on how to fill out the endpoint creation form:</span></span>

<span data-ttu-id="a1494-118">**Field**</span><span class="sxs-lookup"><span data-stu-id="a1494-118">**Field**</span></span> | <span data-ttu-id="a1494-119">**描述**</span><span class="sxs-lookup"><span data-stu-id="a1494-119">**Description**</span></span> | <span data-ttu-id="a1494-120">**建議的值**</span><span class="sxs-lookup"><span data-stu-id="a1494-120">**Recommended Value**</span></span>
--- | --- | ---
<span data-ttu-id="a1494-121">名稱</span><span class="sxs-lookup"><span data-stu-id="a1494-121">Name</span></span> | <span data-ttu-id="a1494-122">這個唯一的值會識別需要 OAuth 存取的應用程式。</span><span class="sxs-lookup"><span data-stu-id="a1494-122">This unique value identifies the application that you require OAuth access for.</span></span> | <span data-ttu-id="a1494-123">Microsoft 搜尋</span><span class="sxs-lookup"><span data-stu-id="a1494-123">Microsoft Search</span></span>
<span data-ttu-id="a1494-124">用戶端識別碼</span><span class="sxs-lookup"><span data-stu-id="a1494-124">Client ID</span></span> | <span data-ttu-id="a1494-125">唯讀屬性，自動產生唯一識別碼的應用程式。</span><span class="sxs-lookup"><span data-stu-id="a1494-125">A read-only, auto-generated unique ID for the application.</span></span> <span data-ttu-id="a1494-126">要求存取權杖時，執行個體使用的用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="a1494-126">The instance uses the client ID when it requests an access token.</span></span> | <span data-ttu-id="a1494-127">NA</span><span class="sxs-lookup"><span data-stu-id="a1494-127">NA</span></span>
<span data-ttu-id="a1494-128">用戶端密碼</span><span class="sxs-lookup"><span data-stu-id="a1494-128">Client secret</span></span> | <span data-ttu-id="a1494-129">使用此共用的密碼字串，ServiceNow 執行個體和 Microsoft Search 授權與彼此通訊。</span><span class="sxs-lookup"><span data-stu-id="a1494-129">With this shared secret string, the ServiceNow instance and Microsoft Search authorize communications with each another.</span></span> | <span data-ttu-id="a1494-130">藉由將此視為密碼，請遵循安全性最佳作法。</span><span class="sxs-lookup"><span data-stu-id="a1494-130">Follow security best-practices by treating this as a password.</span></span>
<span data-ttu-id="a1494-131">重新導向 URL</span><span class="sxs-lookup"><span data-stu-id="a1494-131">Redirect URL</span></span> | <span data-ttu-id="a1494-132">授權伺服器重新導向至所需的回撥 URL。</span><span class="sxs-lookup"><span data-stu-id="a1494-132">A required callback URL that the authorization server redirects to.</span></span> | <span data-ttu-id="a1494-133">請參閱[OAuth 回呼](https://gcs.office.com/v1.0/admin/oauth/callback)。</span><span class="sxs-lookup"><span data-stu-id="a1494-133">See [OAuth callback](https://gcs.office.com/v1.0/admin/oauth/callback).</span></span>
<span data-ttu-id="a1494-134">標誌 URL</span><span class="sxs-lookup"><span data-stu-id="a1494-134">Logo URL</span></span> | <span data-ttu-id="a1494-135">包含應用程式標誌的影像 URL。</span><span class="sxs-lookup"><span data-stu-id="a1494-135">A URL that contains the image for the application logo.</span></span> | <span data-ttu-id="a1494-136">NA</span><span class="sxs-lookup"><span data-stu-id="a1494-136">NA</span></span>
<span data-ttu-id="a1494-137">作用中</span><span class="sxs-lookup"><span data-stu-id="a1494-137">Active</span></span> | <span data-ttu-id="a1494-138">選取核取方塊，可讓應用程式登錄作用中。</span><span class="sxs-lookup"><span data-stu-id="a1494-138">Select the check box to make the application registry active.</span></span> | <span data-ttu-id="a1494-139">設定為作用中</span><span class="sxs-lookup"><span data-stu-id="a1494-139">Set to active</span></span>
<span data-ttu-id="a1494-140">重新整理 token 期限</span><span class="sxs-lookup"><span data-stu-id="a1494-140">Refresh token lifespan</span></span> | <span data-ttu-id="a1494-141">重新整理權杖是有效的秒數。</span><span class="sxs-lookup"><span data-stu-id="a1494-141">The number of seconds that a refresh token is valid.</span></span> <span data-ttu-id="a1494-142">根據預設，重新整理權杖到期 100 天 （8640000 秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="a1494-142">By default, refresh tokens expire in 100 days (8640000 seconds).</span></span> | <span data-ttu-id="a1494-143">31,536,000 （1 年）</span><span class="sxs-lookup"><span data-stu-id="a1494-143">31,536,000 (1 year)</span></span>
<span data-ttu-id="a1494-144">存取權杖使用壽命</span><span class="sxs-lookup"><span data-stu-id="a1494-144">Access token lifespan</span></span> | <span data-ttu-id="a1494-145">存取權杖是有效的秒數。</span><span class="sxs-lookup"><span data-stu-id="a1494-145">The number of seconds that an access token is valid.</span></span> | <span data-ttu-id="a1494-146">43200 （12 小時）</span><span class="sxs-lookup"><span data-stu-id="a1494-146">43,200 (12 hours)</span></span>

## <a name="set-a-sync-filter"></a><span data-ttu-id="a1494-147">設定同步處理篩選</span><span class="sxs-lookup"><span data-stu-id="a1494-147">Set a sync filter</span></span> 
<span data-ttu-id="a1494-148">使用同步處理篩選，您可以指定條件的同步處理的文章。</span><span class="sxs-lookup"><span data-stu-id="a1494-148">With a sync filter, you can specify conditions for syncing articles.</span></span> <span data-ttu-id="a1494-149">它就像是**Where**子句的**SQL Select**陳述式中。</span><span class="sxs-lookup"><span data-stu-id="a1494-149">It's like a **Where** clause in a **SQL Select** statement.</span></span> <span data-ttu-id="a1494-150">例如，您可以選擇索引發佈且作用中的文章。</span><span class="sxs-lookup"><span data-stu-id="a1494-150">For example, you can choose to index only articles that are published and active.</span></span> <span data-ttu-id="a1494-151">SyncNow 組態] 頁面上說明如何擷取與同步處理篩選設定。</span><span class="sxs-lookup"><span data-stu-id="a1494-151">The SyncNow configuration page describes how to capture and set a sync filter.</span></span>

## <a name="manage-the-search-schema"></a><span data-ttu-id="a1494-152">管理搜尋結構描述</span><span class="sxs-lookup"><span data-stu-id="a1494-152">Manage the search schema</span></span>
<span data-ttu-id="a1494-153">成功連線之後，設定的搜尋結構描述對應。</span><span class="sxs-lookup"><span data-stu-id="a1494-153">After successful connection, configure the search schema mapping.</span></span> <span data-ttu-id="a1494-154">您可以選擇要讓屬性**設為可查詢**、**可搜尋**，並**可擷取**。</span><span class="sxs-lookup"><span data-stu-id="a1494-154">You can choose which properties to make **queryable**, **searchable**, and **retrievable**.</span></span>

## <a name="manage-search-permissions"></a><span data-ttu-id="a1494-155">管理搜尋的權限</span><span class="sxs-lookup"><span data-stu-id="a1494-155">Manage search permissions</span></span>
<span data-ttu-id="a1494-156">ServiceNow 連接器僅支援搜尋權限以**供其他人**。</span><span class="sxs-lookup"><span data-stu-id="a1494-156">The ServiceNow connector only supports search permissions visible to **Everyone**.</span></span> <span data-ttu-id="a1494-157">已編製索引的資料會出現在搜尋結果，並在組織中的所有使用者都都能看到。</span><span class="sxs-lookup"><span data-stu-id="a1494-157">Indexed data appears in the search results and is visible to all users in the organization.</span></span>
 
## <a name="set-the-refresh-schedule"></a><span data-ttu-id="a1494-158">設定重新整理排程</span><span class="sxs-lookup"><span data-stu-id="a1494-158">Set the refresh schedule</span></span> 
<span data-ttu-id="a1494-159">ServiceNow 連接器支援重新整理排程適用於完整與累加編目。</span><span class="sxs-lookup"><span data-stu-id="a1494-159">The ServiceNow connector supports refresh schedules for both full and incremental crawls.</span></span> <span data-ttu-id="a1494-160">我們建議您設定兩者。</span><span class="sxs-lookup"><span data-stu-id="a1494-160">We recommend that you set both.</span></span>

<span data-ttu-id="a1494-161">完整編目排程尋找先前已同步處理至 Microsoft 搜尋索引的已刪除的文章和任何移出同步處理篩選的文章。</span><span class="sxs-lookup"><span data-stu-id="a1494-161">A full crawl schedule finds deleted articles that were previously synced to the Microsoft Search index and any articles that moved out of the sync filter.</span></span> <span data-ttu-id="a1494-162">當您第一次連接至 ServiceNow 時，同步處理所有的知識庫文章會執行完整編目。</span><span class="sxs-lookup"><span data-stu-id="a1494-162">When you first connect to ServiceNow, a full crawl runs to sync all the knowledge-base articles.</span></span> <span data-ttu-id="a1494-163">若要同步處理新項目，並進行更新，您要排程累加編目。</span><span class="sxs-lookup"><span data-stu-id="a1494-163">To sync new items and make updates, you need to schedule incremental crawls.</span></span>

<span data-ttu-id="a1494-164">建議的預設值為一天的完整編目和四個小時的累加編目。</span><span class="sxs-lookup"><span data-stu-id="a1494-164">The recommended default is one day for a full crawl and four hours for an incremental crawl.</span></span>
