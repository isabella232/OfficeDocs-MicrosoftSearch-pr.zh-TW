---
title: Microsoft 搜尋的 Azure DevOps 連接器
ms.author: shgrover
author: shakungrover05
manager: jeffkizn
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 設定 Microsoft 搜尋的 Azure DevOps 連接器
ms.openlocfilehash: a0028c3b336c2b5e3d01bb14006ee0debb4524f2
ms.sourcegitcommit: 59435698bece013ae64ca2a68c43455ca10e3fdf
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/05/2020
ms.locfileid: "48927187"
---
# <a name="azure-devops-connector"></a><span data-ttu-id="ba1a1-103">Azure DevOps 連接器</span><span class="sxs-lookup"><span data-stu-id="ba1a1-103">Azure DevOps connector</span></span>

<span data-ttu-id="ba1a1-104">透過 Azure DevOps connector，您的組織可以在其 Azure DevOps 服務實例中編制工作專案的索引。</span><span class="sxs-lookup"><span data-stu-id="ba1a1-104">With the Azure DevOps connector, your organization can index work items in its instance of the Azure DevOps service.</span></span> <span data-ttu-id="ba1a1-105">當您從 Azure DevOps 設定連接器和索引內容之後，使用者就可以在 Microsoft 搜尋中搜尋這些專案。</span><span class="sxs-lookup"><span data-stu-id="ba1a1-105">After you configure the connector and index content from Azure DevOps, end users can search for those items in Microsoft Search.</span></span>

<span data-ttu-id="ba1a1-106">本文適用于 Microsoft 365 系統管理員或任何設定、執行及監視 Azure DevOps 連接器的人員。</span><span class="sxs-lookup"><span data-stu-id="ba1a1-106">This article is for Microsoft 365 administrators or anyone who configures, runs, and monitors an Azure DevOps connector.</span></span> <span data-ttu-id="ba1a1-107">它說明如何設定連接器和連接器功能、限制及疑難排解技術。</span><span class="sxs-lookup"><span data-stu-id="ba1a1-107">It explains how to configure your connector and connector capabilities, limitations, and troubleshooting techniques.</span></span>

>[!IMPORTANT]
><span data-ttu-id="ba1a1-108">Azure DevOps 連接器只支援 Azure DevOps 雲端服務。</span><span class="sxs-lookup"><span data-stu-id="ba1a1-108">The Azure DevOps connector supports only the Azure DevOps cloud service.</span></span> <span data-ttu-id="ba1a1-109">Azure DevOps Server 2019，tfs 2018，tfs 2017，tfs 2015，及 TFS 2013 都不受此連接器支援。</span><span class="sxs-lookup"><span data-stu-id="ba1a1-109">Azure DevOps Server 2019, TFS 2018, TFS 2017, TFS 2015, and TFS 2013 are not supported by this connector.</span></span>

## <a name="connect-to-a-data-source"></a><span data-ttu-id="ba1a1-110">連接到資料來源</span><span class="sxs-lookup"><span data-stu-id="ba1a1-110">Connect to a data source</span></span>

<span data-ttu-id="ba1a1-111">若要連線至 Azure DevOps 實例，您需要 Azure DevOps [組織](https://docs.microsoft.com/azure/devops/organizations/accounts/create-organization) 名稱、其應用程式識別碼，以及 OAuth 驗證的用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="ba1a1-111">To connect to your Azure DevOps instance, you need your Azure DevOps [organization](https://docs.microsoft.com/azure/devops/organizations/accounts/create-organization) name, its App ID, and client secret for OAuth authentication.</span></span>

### <a name="register-an-app"></a><span data-ttu-id="ba1a1-112">註冊應用程式</span><span class="sxs-lookup"><span data-stu-id="ba1a1-112">Register an app</span></span>

<span data-ttu-id="ba1a1-113">您必須在 Azure DevOps 中註冊應用程式，Microsoft 搜尋應用程式才能存取實例。</span><span class="sxs-lookup"><span data-stu-id="ba1a1-113">You must register an app in Azure DevOps so that the Microsoft Search app can access the instance.</span></span> <span data-ttu-id="ba1a1-114">若要深入瞭解，請參閱 Azure DevOps 檔，以瞭解如何 [註冊應用程式](https://docs.microsoft.com/azure/devops/integrate/get-started/authentication/oauth?view=azure-devops#register-your-app)。</span><span class="sxs-lookup"><span data-stu-id="ba1a1-114">To learn more, see Azure DevOps documentation on how to [register an app](https://docs.microsoft.com/azure/devops/integrate/get-started/authentication/oauth?view=azure-devops#register-your-app).</span></span>

<span data-ttu-id="ba1a1-115">下表提供如何填寫 [應用程式註冊] 表單的指導方針：</span><span class="sxs-lookup"><span data-stu-id="ba1a1-115">The following table provides guidance on how to fill out the app registration form:</span></span>

 <span data-ttu-id="ba1a1-116">**必要欄位**</span><span class="sxs-lookup"><span data-stu-id="ba1a1-116">**Mandatory Fields**</span></span> | <span data-ttu-id="ba1a1-117">**描述**</span><span class="sxs-lookup"><span data-stu-id="ba1a1-117">**Description**</span></span>      | <span data-ttu-id="ba1a1-118">**建議值**</span><span class="sxs-lookup"><span data-stu-id="ba1a1-118">**Recommended Value**</span></span>
--- | --- | ---
| <span data-ttu-id="ba1a1-119">公司名稱</span><span class="sxs-lookup"><span data-stu-id="ba1a1-119">Company Name</span></span>         | <span data-ttu-id="ba1a1-120">這是您公司的名稱。</span><span class="sxs-lookup"><span data-stu-id="ba1a1-120">This is the name of your company.</span></span> | <span data-ttu-id="ba1a1-121">使用適當的值</span><span class="sxs-lookup"><span data-stu-id="ba1a1-121">Use an appropriate value</span></span>   |
| <span data-ttu-id="ba1a1-122">應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="ba1a1-122">Application name</span></span>     | <span data-ttu-id="ba1a1-123">此唯一值可識別您要授權的應用程式。</span><span class="sxs-lookup"><span data-stu-id="ba1a1-123">This unique value identifies the application that you're authorizing.</span></span>    | <span data-ttu-id="ba1a1-124">Microsoft 搜尋</span><span class="sxs-lookup"><span data-stu-id="ba1a1-124">Microsoft Search</span></span>     |
| <span data-ttu-id="ba1a1-125">應用程式網站</span><span class="sxs-lookup"><span data-stu-id="ba1a1-125">Application website</span></span>  | <span data-ttu-id="ba1a1-126">此必要欄位是在連接器設定期間要求存取 Azure DevOps 實例之應用程式的 URL。</span><span class="sxs-lookup"><span data-stu-id="ba1a1-126">This required field is the URL of the application that will request access to your Azure DevOps instance during connector setup.</span></span>  | <https://gcs.office.com/>                |
| <span data-ttu-id="ba1a1-127">授權回撥 URL</span><span class="sxs-lookup"><span data-stu-id="ba1a1-127">Authorization callback URL</span></span>        | <span data-ttu-id="ba1a1-128">授權伺服器重新導向所需的回撥 URL。</span><span class="sxs-lookup"><span data-stu-id="ba1a1-128">A required callback URL that the authorization server redirects to.</span></span> | <https://gcs.office.com/v1.0/admin/oauth/callback>|
| <span data-ttu-id="ba1a1-129">授權範圍</span><span class="sxs-lookup"><span data-stu-id="ba1a1-129">Authorized scopes</span></span> | <span data-ttu-id="ba1a1-130">這是應用程式的存取範圍</span><span class="sxs-lookup"><span data-stu-id="ba1a1-130">This is the scope of access for the application</span></span> | <span data-ttu-id="ba1a1-131">選取下列範圍： Identity (讀取) 、工作專案 (讀取) 、變數群組 (讀取) 、專案和團隊 (讀取) 、圖形 (讀取) </span><span class="sxs-lookup"><span data-stu-id="ba1a1-131">Select the following scopes: Identity (read), Work Items (read), Variable Groups (read), Project and team (read), Graph (read)</span></span>|

<span data-ttu-id="ba1a1-132">在註冊具有上述詳細資料的應用程式時，您會取得將用來設定連接器的 **應用程式識別碼** 和 **用戶端密碼** 。</span><span class="sxs-lookup"><span data-stu-id="ba1a1-132">On registering the app with the details above, you will get the **App ID** and **Client Secret** that will be used to configure the connector.</span></span>

>[!NOTE]
><span data-ttu-id="ba1a1-133">若要撤銷對 Azure DevOps 中註冊的任何應用程式的存取權，請移至 Azure DevOps 實例右邊的 [使用者設定]。</span><span class="sxs-lookup"><span data-stu-id="ba1a1-133">To revoke access to any app registered in Azure DevOps, go to User settings at the right top of your Azure DevOps instance.</span></span> <span data-ttu-id="ba1a1-134">按一下 [設定檔]，然後按一下側邊窗格 [安全性] 區段中的 [授權]。</span><span class="sxs-lookup"><span data-stu-id="ba1a1-134">Click on Profile and then click on Authorizations in the Security section of the side pane.</span></span> <span data-ttu-id="ba1a1-135">將游標移到授權的 OAuth 應用程式上，以查看應用程式詳細資料右下角的 [撤銷] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="ba1a1-135">Hover over an authorized OAuth app to see the Revoke button at the corner of the app details.</span></span>

### <a name="connection-settings"></a><span data-ttu-id="ba1a1-136">連接設定</span><span class="sxs-lookup"><span data-stu-id="ba1a1-136">Connection settings</span></span>

<span data-ttu-id="ba1a1-137">在使用 Azure DevOps 註冊 Microsoft Search 應用程式之後，您可以完成 [連線設定] 步驟。</span><span class="sxs-lookup"><span data-stu-id="ba1a1-137">After registering the Microsoft Search app with Azure DevOps, you can complete the connection settings step.</span></span> <span data-ttu-id="ba1a1-138">輸入您的組織名稱、應用程式識別碼和用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="ba1a1-138">Enter your organization name, App ID, and Client secret.</span></span>

![連接應用程式設定](media/ADO_Connection_settings_2.png)

## <a name="select-projects-and-fields"></a><span data-ttu-id="ba1a1-140">選取專案和欄位</span><span class="sxs-lookup"><span data-stu-id="ba1a1-140">Select projects and fields</span></span>

<span data-ttu-id="ba1a1-141">您可以選擇建立整個組織或特定專案之索引的連線。</span><span class="sxs-lookup"><span data-stu-id="ba1a1-141">You can choose for the connection to index either the entire organization or specific projects.</span></span>

<span data-ttu-id="ba1a1-142">如果您選擇編制整個組織的索引，組織中所有專案中的專案將會獲得索引。</span><span class="sxs-lookup"><span data-stu-id="ba1a1-142">If you choose to index the entire organization, items in all projects in the organization will get indexed.</span></span> <span data-ttu-id="ba1a1-143">新專案和專案會在建立後的下一個編目期間編制索引。</span><span class="sxs-lookup"><span data-stu-id="ba1a1-143">New projects and items will be indexed during the next crawl after they are created.</span></span> <span data-ttu-id="ba1a1-144">如果您選擇個別專案，則只有那些專案中的工作專案將會編制索引。</span><span class="sxs-lookup"><span data-stu-id="ba1a1-144">If you choose individual projects, only work items in those projects will be indexed.</span></span>

![設定資料](media/ADO_Configure_data.png)

<span data-ttu-id="ba1a1-146">接下來，選取您要連線索引及預覽這些欄位中資料的欄位，然後再繼續進行。</span><span class="sxs-lookup"><span data-stu-id="ba1a1-146">Next, select which fields you want the connection to index and preview data in these fields before proceeding.</span></span>

![選擇屬性](media/ADO_choose_properties.png)

## <a name="manage-search-permissions"></a><span data-ttu-id="ba1a1-148">管理搜尋許可權</span><span class="sxs-lookup"><span data-stu-id="ba1a1-148">Manage search permissions</span></span>

<span data-ttu-id="ba1a1-149">Azure DevOps 連接器目前只支援 **所有人皆可看到** 搜尋許可權。</span><span class="sxs-lookup"><span data-stu-id="ba1a1-149">The Azure DevOps connector currently only supports search permissions **Visible to Everyone**.</span></span> <span data-ttu-id="ba1a1-150">已編制索引的資料將會出現在所有使用者的搜尋結果中。</span><span class="sxs-lookup"><span data-stu-id="ba1a1-150">Indexed data will appear in the search results for all users.</span></span>

## <a name="manage-search-schema"></a><span data-ttu-id="ba1a1-151">管理搜尋結構描述</span><span class="sxs-lookup"><span data-stu-id="ba1a1-151">Manage search schema</span></span>

<span data-ttu-id="ba1a1-152">設定搜尋架構對應。</span><span class="sxs-lookup"><span data-stu-id="ba1a1-152">Configure the search schema mapping.</span></span> <span data-ttu-id="ba1a1-153">您可以選擇哪些屬性可供 **查詢** 、可搜尋及可 **供\*\*\*\*檢索** 。</span><span class="sxs-lookup"><span data-stu-id="ba1a1-153">You can choose which properties to make **queryable** , **searchable** and **retrievable**.</span></span>


## <a name="set-refresh-schedule"></a><span data-ttu-id="ba1a1-154">設定重新整理排程</span><span class="sxs-lookup"><span data-stu-id="ba1a1-154">Set refresh schedule</span></span>

<span data-ttu-id="ba1a1-155">Azure DevOps 連接器支援完整和累加編目的更新排程。</span><span class="sxs-lookup"><span data-stu-id="ba1a1-155">The Azure DevOps connector supports refresh schedules for both full and incremental crawls.</span></span> <span data-ttu-id="ba1a1-156">完整編目會找到先前同步處理至 Microsoft 搜尋索引的已刪除工作專案。</span><span class="sxs-lookup"><span data-stu-id="ba1a1-156">A full crawl finds deleted work items that were previously synced to the Microsoft Search index.</span></span> <span data-ttu-id="ba1a1-157">會執行完整編目，以同步處理所有工作專案。</span><span class="sxs-lookup"><span data-stu-id="ba1a1-157">A full crawl runs to sync all the work items.</span></span> <span data-ttu-id="ba1a1-158">若要將新的工作專案和更新同步到現有的工作專案，您必須排程累加編目。</span><span class="sxs-lookup"><span data-stu-id="ba1a1-158">To sync new work items and updates to existing work items, you need to schedule incremental crawls.</span></span>

<span data-ttu-id="ba1a1-159">建議的排程為一小時用於增量編目，而一天則是完整編目。</span><span class="sxs-lookup"><span data-stu-id="ba1a1-159">The recommended schedule is one hour for an incremental crawl and one day for a full crawl.</span></span>
