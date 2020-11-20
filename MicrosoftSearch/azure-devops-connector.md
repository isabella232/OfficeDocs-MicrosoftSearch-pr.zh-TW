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
ms.openlocfilehash: b9c566e3e07bfca6d4d25b14915f0160f3928b15
ms.sourcegitcommit: 59cdd3f0f82b7918399bf44d27d9891076090f4f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2020
ms.locfileid: "49367548"
---
# <a name="azure-devops-connector-preview"></a><span data-ttu-id="032e4-103">Azure DevOps connector (preview) </span><span class="sxs-lookup"><span data-stu-id="032e4-103">Azure DevOps connector (preview)</span></span>

<span data-ttu-id="032e4-104">透過 Azure DevOps connector，您的組織可以在其 Azure DevOps 服務實例中編制工作專案的索引。</span><span class="sxs-lookup"><span data-stu-id="032e4-104">With the Azure DevOps connector, your organization can index work items in its instance of the Azure DevOps service.</span></span> <span data-ttu-id="032e4-105">當您從 Azure DevOps 設定連接器和索引內容之後，使用者就可以在 Microsoft 搜尋中搜尋這些專案。</span><span class="sxs-lookup"><span data-stu-id="032e4-105">After you configure the connector and index content from Azure DevOps, end users can search for those items in Microsoft Search.</span></span>

<span data-ttu-id="032e4-106">本文適用于 Microsoft 365 系統管理員或任何設定、執行及監視 Azure DevOps 連接器的人員。</span><span class="sxs-lookup"><span data-stu-id="032e4-106">This article is for Microsoft 365 administrators or anyone who configures, runs, and monitors an Azure DevOps connector.</span></span> <span data-ttu-id="032e4-107">它說明如何設定連接器和連接器功能、限制及疑難排解技術。</span><span class="sxs-lookup"><span data-stu-id="032e4-107">It explains how to configure your connector and connector capabilities, limitations, and troubleshooting techniques.</span></span>

>[!IMPORTANT]
><span data-ttu-id="032e4-108">Azure DevOps 連接器只支援 Azure DevOps 雲端服務。</span><span class="sxs-lookup"><span data-stu-id="032e4-108">The Azure DevOps connector supports only the Azure DevOps cloud service.</span></span> <span data-ttu-id="032e4-109">Azure DevOps Server 2019，tfs 2018，tfs 2017，tfs 2015，及 TFS 2013 都不受此連接器支援。</span><span class="sxs-lookup"><span data-stu-id="032e4-109">Azure DevOps Server 2019, TFS 2018, TFS 2017, TFS 2015, and TFS 2013 are not supported by this connector.</span></span> 

## <a name="connect-to-a-data-source"></a><span data-ttu-id="032e4-110">連接到資料來源</span><span class="sxs-lookup"><span data-stu-id="032e4-110">Connect to a data source</span></span>

<span data-ttu-id="032e4-111">若要連線至 Azure DevOps 實例，您需要 Azure DevOps [組織](https://docs.microsoft.com/azure/devops/organizations/accounts/create-organization) 名稱、其應用程式識別碼，以及 OAuth 驗證的用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="032e4-111">To connect to your Azure DevOps instance, you need your Azure DevOps [organization](https://docs.microsoft.com/azure/devops/organizations/accounts/create-organization) name, its App ID, and client secret for OAuth authentication.</span></span>

### <a name="register-an-app"></a><span data-ttu-id="032e4-112">註冊應用程式</span><span class="sxs-lookup"><span data-stu-id="032e4-112">Register an app</span></span>

<span data-ttu-id="032e4-113">您必須在 Azure DevOps 中註冊應用程式，Microsoft 搜尋應用程式才能存取實例。</span><span class="sxs-lookup"><span data-stu-id="032e4-113">You must register an app in Azure DevOps so that the Microsoft Search app can access the instance.</span></span> <span data-ttu-id="032e4-114">若要深入瞭解，請參閱 Azure DevOps 檔，以瞭解如何 [註冊應用程式](https://docs.microsoft.com/azure/devops/integrate/get-started/authentication/oauth?view=azure-devops#register-your-app)。</span><span class="sxs-lookup"><span data-stu-id="032e4-114">To learn more, see Azure DevOps documentation on how to [register an app](https://docs.microsoft.com/azure/devops/integrate/get-started/authentication/oauth?view=azure-devops#register-your-app).</span></span> 

<span data-ttu-id="032e4-115">下表提供如何填寫 [應用程式註冊] 表單的指導方針：</span><span class="sxs-lookup"><span data-stu-id="032e4-115">The following table provides guidance on how to fill out the app registration form:</span></span>

 <span data-ttu-id="032e4-116">**必要欄位**</span><span class="sxs-lookup"><span data-stu-id="032e4-116">**Mandatory Fields**</span></span> | <span data-ttu-id="032e4-117">**描述**</span><span class="sxs-lookup"><span data-stu-id="032e4-117">**Description**</span></span>      | <span data-ttu-id="032e4-118">**建議值**</span><span class="sxs-lookup"><span data-stu-id="032e4-118">**Recommended Value**</span></span> 
--- | --- | --- 
| <span data-ttu-id="032e4-119">公司名稱</span><span class="sxs-lookup"><span data-stu-id="032e4-119">Company Name</span></span>         | <span data-ttu-id="032e4-120">這是您公司的名稱。</span><span class="sxs-lookup"><span data-stu-id="032e4-120">This is the name of your company.</span></span> | <span data-ttu-id="032e4-121">使用適當的值</span><span class="sxs-lookup"><span data-stu-id="032e4-121">Use an appropriate value</span></span>   | 
| <span data-ttu-id="032e4-122">應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="032e4-122">Application name</span></span>     | <span data-ttu-id="032e4-123">此唯一值可識別您要授權的應用程式。</span><span class="sxs-lookup"><span data-stu-id="032e4-123">This unique value identifies the application that you're authorizing.</span></span>    | <span data-ttu-id="032e4-124">Microsoft 搜尋</span><span class="sxs-lookup"><span data-stu-id="032e4-124">Microsoft Search</span></span>     | 
| <span data-ttu-id="032e4-125">應用程式網站</span><span class="sxs-lookup"><span data-stu-id="032e4-125">Application website</span></span>  | <span data-ttu-id="032e4-126">此必要欄位是在連接器設定期間要求存取 Azure DevOps 實例之應用程式的 URL。</span><span class="sxs-lookup"><span data-stu-id="032e4-126">This required field is the URL of the application that will request access to your Azure DevOps instance during connector setup.</span></span>  | <https://gcs.office.com/>                | 
| <span data-ttu-id="032e4-127">授權回撥 URL</span><span class="sxs-lookup"><span data-stu-id="032e4-127">Authorization callback URL</span></span>        | <span data-ttu-id="032e4-128">授權伺服器重新導向所需的回撥 URL。</span><span class="sxs-lookup"><span data-stu-id="032e4-128">A required callback URL that the authorization server redirects to.</span></span> | <https://gcs.office.com/v1.0/admin/oauth/callback>| 
| <span data-ttu-id="032e4-129">授權範圍</span><span class="sxs-lookup"><span data-stu-id="032e4-129">Authorized scopes</span></span> | <span data-ttu-id="032e4-130">這是應用程式的存取範圍</span><span class="sxs-lookup"><span data-stu-id="032e4-130">This is the scope of access for the application</span></span> | <span data-ttu-id="032e4-131">選取下列範圍： Identity (讀取) 、工作專案 (讀取) 、變數群組 (讀取) 、專案和團隊 (讀取) 、圖形 (讀取) </span><span class="sxs-lookup"><span data-stu-id="032e4-131">Select the following scopes: Identity (read), Work Items (read), Variable Groups (read), Project and team (read), Graph (read)</span></span>| 

<span data-ttu-id="032e4-132">在註冊具有上述詳細資料的應用程式時，您會取得將用來設定連接器的 **應用程式識別碼** 和 **用戶端密碼** 。</span><span class="sxs-lookup"><span data-stu-id="032e4-132">On registering the app with the details above, you will get the **App ID** and **Client Secret** that will be used to configure the connector.</span></span>

>[!NOTE]
><span data-ttu-id="032e4-133">若要撤銷對 Azure DevOps 中註冊的任何應用程式的存取權，請移至 Azure DevOps 實例右邊的 [使用者設定]。</span><span class="sxs-lookup"><span data-stu-id="032e4-133">To revoke access to any app registered in Azure DevOps, go to User settings at the right top of your Azure DevOps instance.</span></span> <span data-ttu-id="032e4-134">按一下 [設定檔]，然後按一下側邊窗格 [安全性] 區段中的 [授權]。</span><span class="sxs-lookup"><span data-stu-id="032e4-134">Click on Profile and then click on Authorizations in the Security section of the side pane.</span></span> <span data-ttu-id="032e4-135">將游標移到授權的 OAuth 應用程式上，以查看應用程式詳細資料右下角的 [撤銷] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="032e4-135">Hover over an authorized OAuth app to see the Revoke button at the corner of the app details.</span></span>

### <a name="connection-settings"></a><span data-ttu-id="032e4-136">連接設定</span><span class="sxs-lookup"><span data-stu-id="032e4-136">Connection settings</span></span>

<span data-ttu-id="032e4-137">在使用 Azure DevOps 註冊 Microsoft Search 應用程式之後，您可以完成 [連線設定] 步驟。</span><span class="sxs-lookup"><span data-stu-id="032e4-137">After registering the Microsoft Search app with Azure DevOps, you can complete the connection settings step.</span></span> <span data-ttu-id="032e4-138">輸入您的組織名稱、應用程式識別碼和用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="032e4-138">Enter your organization name, App ID, and Client secret.</span></span>

![連接應用程式設定](media/ADO_Connection_settings_2.png)

## <a name="select-projects-and-fields"></a><span data-ttu-id="032e4-140">選取專案和欄位</span><span class="sxs-lookup"><span data-stu-id="032e4-140">Select projects and fields</span></span>

<span data-ttu-id="032e4-141">您可以選擇建立整個組織或特定專案之索引的連線。</span><span class="sxs-lookup"><span data-stu-id="032e4-141">You can choose for the connection to index either the entire organization or specific projects.</span></span>

<span data-ttu-id="032e4-142">如果您選擇編制整個組織的索引，組織中所有專案中的專案將會獲得索引。</span><span class="sxs-lookup"><span data-stu-id="032e4-142">If you choose to index the entire organization, items in all projects in the organization will get indexed.</span></span> <span data-ttu-id="032e4-143">新專案和專案會在建立後的下一個編目期間編制索引。</span><span class="sxs-lookup"><span data-stu-id="032e4-143">New projects and items will be indexed during the next crawl after they are created.</span></span> <span data-ttu-id="032e4-144">如果您選擇個別專案，則只有那些專案中的工作專案將會編制索引。</span><span class="sxs-lookup"><span data-stu-id="032e4-144">If you choose individual projects, only work items in those projects will be indexed.</span></span>

![設定資料](media/ADO_Configure_data.png)

<span data-ttu-id="032e4-146">接下來，選取您要連線索引及預覽這些欄位中資料的欄位，然後再繼續進行。</span><span class="sxs-lookup"><span data-stu-id="032e4-146">Next, select which fields you want the connection to index and preview data in these fields before proceeding.</span></span>

![選擇屬性](media/ADO_choose_properties.png)

## <a name="manage-search-permissions"></a><span data-ttu-id="032e4-148">管理搜尋許可權</span><span class="sxs-lookup"><span data-stu-id="032e4-148">Manage search permissions</span></span>

<span data-ttu-id="032e4-149">Azure DevOps 連接器只支援可供  **存取此資料來源** 或 **所有人** 的使用者看到的搜尋許可權。</span><span class="sxs-lookup"><span data-stu-id="032e4-149">The Azure DevOps connector supports search permissions visible to  **Only people with access to this data source** or **Everyone**.</span></span> <span data-ttu-id="032e4-150">如果您選擇 [ **只有可存取此資料來源的人員**]，針對 Azure DevOps 中組織、專案或區域路徑層級的使用者或群組的許可權，針對其存取權的使用者，將會在搜尋結果中顯示索引的資料。</span><span class="sxs-lookup"><span data-stu-id="032e4-150">If you choose **Only people with access to this data source**,indexed data will appear in the search results for users who have access to them based on permissions to users or groups at the Organization, Project or Area path level in Azure DevOps.</span></span> <span data-ttu-id="032e4-151">如果您選擇 [ **任何人**]，索引資料將會出現在所有使用者的搜尋結果中。</span><span class="sxs-lookup"><span data-stu-id="032e4-151">If you choose **Everyone**, indexed data will appear in the search results for all users.</span></span>

## <a name="assign-property-labels"></a><span data-ttu-id="032e4-152">指派屬性標籤</span><span class="sxs-lookup"><span data-stu-id="032e4-152">Assign property labels</span></span>

<span data-ttu-id="032e4-153">您可以從選項的功能表中選擇，將 source 屬性指派給每個標籤。</span><span class="sxs-lookup"><span data-stu-id="032e4-153">You can assign a source property to each label by choosing from a menu of options.</span></span> <span data-ttu-id="032e4-154">雖然這個步驟不是必要的，但具有一些屬性標籤會提升搜尋相關性，並可確保使用者更準確的搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="032e4-154">While this step is not mandatory, having some property labels will improve the search relevance and ensure more accurate search results for end users.</span></span>

## <a name="manage-schema"></a><span data-ttu-id="032e4-155">管理架構</span><span class="sxs-lookup"><span data-stu-id="032e4-155">Manage schema</span></span>

<span data-ttu-id="032e4-156">在 [**管理架構**] 畫面上，您可以選擇變更架構屬性 (可 **查詢**、**可搜尋、可\*\*\*\*檢索** 及 **可精簡搜尋**) 相關聯的屬性、新增選用的別名，然後選擇 **Content** 屬性。</span><span class="sxs-lookup"><span data-stu-id="032e4-156">On the **Manage Schema** screen, you have the option to change the schema attributes (**queryable**, **searchable**, **retrievable**, and **refinable**) associated with the properties, add optional aliases, and choose the **Content** property.</span></span>

## <a name="set-the-refresh-schedule"></a><span data-ttu-id="032e4-157">設定重新整理排程</span><span class="sxs-lookup"><span data-stu-id="032e4-157">Set the refresh schedule</span></span>

<span data-ttu-id="032e4-158">Azure DevOps 連接器支援完整和累加編目的更新排程。</span><span class="sxs-lookup"><span data-stu-id="032e4-158">The Azure DevOps connector supports refresh schedules for both full and incremental crawls.</span></span> <span data-ttu-id="032e4-159">完整編目會找到先前同步處理至 Microsoft 搜尋索引的已刪除工作專案。</span><span class="sxs-lookup"><span data-stu-id="032e4-159">A full crawl finds deleted work items that were previously synced to the Microsoft Search index.</span></span> <span data-ttu-id="032e4-160">會執行完整編目，以同步處理所有工作專案。</span><span class="sxs-lookup"><span data-stu-id="032e4-160">A full crawl runs to sync all the work items.</span></span> <span data-ttu-id="032e4-161">若要將新的工作專案和更新同步到現有的工作專案，您必須排程累加編目。</span><span class="sxs-lookup"><span data-stu-id="032e4-161">To sync new work items and updates to existing work items, you need to schedule incremental crawls.</span></span>

<span data-ttu-id="032e4-162">建議的排程為一小時用於增量編目，而一天則是完整編目。</span><span class="sxs-lookup"><span data-stu-id="032e4-162">The recommended schedule is one hour for an incremental crawl and one day for a full crawl.</span></span> 