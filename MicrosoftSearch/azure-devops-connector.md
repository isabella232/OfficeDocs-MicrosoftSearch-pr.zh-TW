---
title: Microsoft 搜尋的 Azure DevOps 圖形連接器
ms.author: mecampos
author: mecampos
manager: umas
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 設定 Microsoft 搜尋的 Azure DevOps 圖形連接器
ms.openlocfilehash: 3d922a5384de8bf0ef3c6dfd80bd67ad9170eb66
ms.sourcegitcommit: d39113376db26333872d3a2c7baddc3a3a7aea61
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/03/2021
ms.locfileid: "50084936"
---
<!---Previous ms.author: shgrover --->

# <a name="azure-devops-graph-connector-preview"></a><span data-ttu-id="cb232-103">Azure DevOps Graph connector (preview) </span><span class="sxs-lookup"><span data-stu-id="cb232-103">Azure DevOps Graph connector (preview)</span></span>

<span data-ttu-id="cb232-104">Azure DevOps Graph 連接器可讓您的組織為其 Azure DevOps 服務實例中的工作專案編制索引。</span><span class="sxs-lookup"><span data-stu-id="cb232-104">The Azure DevOps Graph connector allows your organization to index work items in its instance of the Azure DevOps service.</span></span> <span data-ttu-id="cb232-105">當您從 Azure DevOps 設定連接器和索引內容之後，使用者就可以在 Microsoft 搜尋中搜尋這些專案。</span><span class="sxs-lookup"><span data-stu-id="cb232-105">After you configure the connector and index content from Azure DevOps, end users can search for those items in Microsoft Search.</span></span>

> [!NOTE]
> <span data-ttu-id="cb232-106">請閱讀 [**您的圖形連接器文章設定**](configure-connector.md) ，以瞭解一般圖表連接器設定程式。</span><span class="sxs-lookup"><span data-stu-id="cb232-106">Read the [**Setup for your Graph connector**](configure-connector.md) article to understand the general Graph connectors setup process.</span></span>

<span data-ttu-id="cb232-107">本文適用于任何設定、執行及監視 ServiceNow 圖形連接器的人員。</span><span class="sxs-lookup"><span data-stu-id="cb232-107">This article is for anyone who configures, runs, and monitors a ServiceNow Graph connector.</span></span> <span data-ttu-id="cb232-108">它會補充一般設定程式，並顯示只適用于 ServiceNow 圖形連接器的指令。</span><span class="sxs-lookup"><span data-stu-id="cb232-108">It supplements the general setup process, and shows instructions that apply only for the ServiceNow Graph connector.</span></span>

>[!IMPORTANT]
><span data-ttu-id="cb232-109">Azure DevOps 連接器只支援 Azure DevOps 雲端服務。</span><span class="sxs-lookup"><span data-stu-id="cb232-109">The Azure DevOps connector supports only the Azure DevOps cloud service.</span></span> <span data-ttu-id="cb232-110">Azure DevOps Server 2019，tfs 2018，tfs 2017，tfs 2015，及 TFS 2013 都不受此連接器支援。</span><span class="sxs-lookup"><span data-stu-id="cb232-110">Azure DevOps Server 2019, TFS 2018, TFS 2017, TFS 2015, and TFS 2013 are not supported by this connector.</span></span>

<!---## Before you get started-->

<!---Insert "Before you get started" recommendations for this data source-->

## <a name="step-1-add-a-graph-connector-in-the-microsoft-365-admin-center"></a><span data-ttu-id="cb232-111">步驟1：在 Microsoft 365 系統管理中心新增圖表連接器</span><span class="sxs-lookup"><span data-stu-id="cb232-111">Step 1: Add a Graph connector in the Microsoft 365 admin center</span></span>

<span data-ttu-id="cb232-112">遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。</span><span class="sxs-lookup"><span data-stu-id="cb232-112">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup 
instructions.-->

## <a name="step-2-name-the-connection"></a><span data-ttu-id="cb232-113">步驟2：命名連線</span><span class="sxs-lookup"><span data-stu-id="cb232-113">Step 2: Name the connection</span></span>

<span data-ttu-id="cb232-114">遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。</span><span class="sxs-lookup"><span data-stu-id="cb232-114">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup 
instructions.-->

## <a name="step-3-configure-the-connection-settings"></a><span data-ttu-id="cb232-115">步驟3：設定連接設定</span><span class="sxs-lookup"><span data-stu-id="cb232-115">Step 3: Configure the connection settings</span></span>

<span data-ttu-id="cb232-116">若要連線至 Azure DevOps 實例，您需要 Azure DevOps [組織](https://docs.microsoft.com/azure/devops/organizations/accounts/create-organization) 名稱、其應用程式識別碼，以及 OAuth 驗證的用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="cb232-116">To connect to your Azure DevOps instance, you need your Azure DevOps [organization](https://docs.microsoft.com/azure/devops/organizations/accounts/create-organization) name, its App ID, and client secret for OAuth authentication.</span></span>

### <a name="register-an-app"></a><span data-ttu-id="cb232-117">註冊應用程式</span><span class="sxs-lookup"><span data-stu-id="cb232-117">Register an app</span></span>

<span data-ttu-id="cb232-118">在 Azure DevOps 中註冊應用程式，以便 Microsoft 搜尋應用程式可以存取實例。</span><span class="sxs-lookup"><span data-stu-id="cb232-118">Register an app in Azure DevOps so that the Microsoft Search app can access the instance.</span></span> <span data-ttu-id="cb232-119">若要深入瞭解，請參閱 Azure DevOps 檔，以瞭解如何 [註冊應用程式](https://docs.microsoft.com/azure/devops/integrate/get-started/authentication/oauth?view=azure-devops#register-your-app&preserve-view=true)。</span><span class="sxs-lookup"><span data-stu-id="cb232-119">To learn more, see Azure DevOps documentation on how to [register an app](https://docs.microsoft.com/azure/devops/integrate/get-started/authentication/oauth?view=azure-devops#register-your-app&preserve-view=true).</span></span>

<span data-ttu-id="cb232-120">下表提供如何填寫 [應用程式註冊] 表單的指導方針：</span><span class="sxs-lookup"><span data-stu-id="cb232-120">The following table provides guidance on how to fill out the app registration form:</span></span>

<span data-ttu-id="cb232-121">必要欄位</span><span class="sxs-lookup"><span data-stu-id="cb232-121">Mandatory Fields</span></span> | <span data-ttu-id="cb232-122">描述</span><span class="sxs-lookup"><span data-stu-id="cb232-122">Description</span></span> | <span data-ttu-id="cb232-123">建議值</span><span class="sxs-lookup"><span data-stu-id="cb232-123">Recommended Value</span></span>
--- | --- | ---
| <span data-ttu-id="cb232-124">公司名稱</span><span class="sxs-lookup"><span data-stu-id="cb232-124">Company Name</span></span>         | <span data-ttu-id="cb232-125">您公司的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb232-125">The name of your company.</span></span> | <span data-ttu-id="cb232-126">使用適當的值</span><span class="sxs-lookup"><span data-stu-id="cb232-126">Use an appropriate value</span></span>   |
| <span data-ttu-id="cb232-127">應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="cb232-127">Application name</span></span>     | <span data-ttu-id="cb232-128">識別您要授權之應用程式的唯一值。</span><span class="sxs-lookup"><span data-stu-id="cb232-128">A unique value that identifies the application that you're authorizing.</span></span>    | <span data-ttu-id="cb232-129">Microsoft 搜尋</span><span class="sxs-lookup"><span data-stu-id="cb232-129">Microsoft Search</span></span>     |
| <span data-ttu-id="cb232-130">應用程式網站</span><span class="sxs-lookup"><span data-stu-id="cb232-130">Application website</span></span>  | <span data-ttu-id="cb232-131">在連接器設定期間要求存取 Azure DevOps 實例之應用程式的 URL。</span><span class="sxs-lookup"><span data-stu-id="cb232-131">The URL of the application that will request access to your Azure DevOps instance during connector setup.</span></span> <span data-ttu-id="cb232-132"> (必要) 。</span><span class="sxs-lookup"><span data-stu-id="cb232-132">(Required).</span></span>  | <span data-ttu-id="cb232-133"> HTTPs://<span>gc。</span>com</span><span class="sxs-lookup"><span data-stu-id="cb232-133">https://<span>gcs.office.</span>com/</span></span>
| <span data-ttu-id="cb232-134">授權回撥 URL</span><span class="sxs-lookup"><span data-stu-id="cb232-134">Authorization callback URL</span></span>        | <span data-ttu-id="cb232-135">授權伺服器重新導向所需的回撥 URL。</span><span class="sxs-lookup"><span data-stu-id="cb232-135">A required callback URL that the authorization server redirects to.</span></span> | <span data-ttu-id="cb232-136"> HTTPs://<span>gc。</span>com/v 1.0/admin/oauth/callback</span><span class="sxs-lookup"><span data-stu-id="cb232-136">https://<span>gcs.office.</span>com/v1.0/admin/oauth/callback</span></span>|
| <span data-ttu-id="cb232-137">授權範圍</span><span class="sxs-lookup"><span data-stu-id="cb232-137">Authorized scopes</span></span> | <span data-ttu-id="cb232-138">應用程式的存取範圍</span><span class="sxs-lookup"><span data-stu-id="cb232-138">The scope of access for the application</span></span> | <span data-ttu-id="cb232-139">選取下列範圍： Identity (讀取) 、工作專案 (讀取) 、變數群組 (讀取) 、專案和團隊 (讀取) 、圖形 (讀取) </span><span class="sxs-lookup"><span data-stu-id="cb232-139">Select the following scopes: Identity (read), Work Items (read), Variable Groups (read), Project and team (read), Graph (read)</span></span>|

<span data-ttu-id="cb232-140">在註冊具有上述詳細資料的應用程式時，您會取得將用來設定連接器的 **應用程式識別碼** 和 **用戶端密碼** 。</span><span class="sxs-lookup"><span data-stu-id="cb232-140">On registering the app with the details above, you'll get the **App ID** and **Client Secret** that will be used to configure the connector.</span></span>

>[!NOTE]
><span data-ttu-id="cb232-141">若要撤銷對 Azure DevOps 中註冊的任何應用程式的存取權，請移至 Azure DevOps 實例右邊的 [使用者設定]。</span><span class="sxs-lookup"><span data-stu-id="cb232-141">To revoke access to any app registered in Azure DevOps, go to User settings at the right top of your Azure DevOps instance.</span></span> <span data-ttu-id="cb232-142">選取 [設定檔]，然後選取側邊窗格的 [安全性] 區段中的 [授權]。</span><span class="sxs-lookup"><span data-stu-id="cb232-142">Select Profile and then select Authorizations in the Security section of the side pane.</span></span> <span data-ttu-id="cb232-143">將游標移到授權的 OAuth 應用程式上，以查看應用程式詳細資料右下角的 [撤銷] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="cb232-143">Hover over an authorized OAuth app to see the Revoke button at the corner of the app details.</span></span>

### <a name="connection-settings"></a><span data-ttu-id="cb232-144">連接設定</span><span class="sxs-lookup"><span data-stu-id="cb232-144">Connection settings</span></span>

<span data-ttu-id="cb232-145">在使用 Azure DevOps 註冊 Microsoft Search 應用程式之後，您可以完成 [連線設定] 步驟。</span><span class="sxs-lookup"><span data-stu-id="cb232-145">After registering the Microsoft Search app with Azure DevOps, you can complete the connection settings step.</span></span> <span data-ttu-id="cb232-146">輸入您的組織名稱、應用程式識別碼和用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="cb232-146">Enter your organization name, App ID, and Client secret.</span></span>

![連接應用程式設定](media/ADO_Connection_settings_2.png)

### <a name="configure-data-select-projects-and-fields"></a><span data-ttu-id="cb232-148">設定資料：選取專案和欄位</span><span class="sxs-lookup"><span data-stu-id="cb232-148">Configure data: select projects and fields</span></span>

<span data-ttu-id="cb232-149">您可以選擇建立整個組織或特定專案之索引的連線。</span><span class="sxs-lookup"><span data-stu-id="cb232-149">You can choose for the connection to index either the entire organization or specific projects.</span></span>

<span data-ttu-id="cb232-150">如果您選擇編制整個組織的索引，組織中所有專案中的專案將會獲得索引。</span><span class="sxs-lookup"><span data-stu-id="cb232-150">If you choose to index the entire organization, items in all projects in the organization will get indexed.</span></span> <span data-ttu-id="cb232-151">新專案和專案會在建立後的下一個編目期間編制索引。</span><span class="sxs-lookup"><span data-stu-id="cb232-151">New projects and items will be indexed during the next crawl after they're created.</span></span>

<span data-ttu-id="cb232-152">如果您選擇個別專案，則只有那些專案中的工作專案將會編制索引。</span><span class="sxs-lookup"><span data-stu-id="cb232-152">If you choose individual projects, only work items in those projects will be indexed.</span></span>

![設定資料](media/ADO_Configure_data.png)

<span data-ttu-id="cb232-154">接下來，選取您要連線索引及預覽這些欄位中資料的欄位，然後再繼續進行。</span><span class="sxs-lookup"><span data-stu-id="cb232-154">Next, select which fields you want the connection to index and preview data in these fields before proceeding.</span></span>

![選擇屬性](media/ADO_choose_properties.png)

## <a name="step-4-manage-search-permissions"></a><span data-ttu-id="cb232-156">步驟4：管理搜尋許可權</span><span class="sxs-lookup"><span data-stu-id="cb232-156">Step 4: Manage search permissions</span></span>

<span data-ttu-id="cb232-157">Azure DevOps 連接器只支援可供  **存取此資料來源** 或 **所有人** 的使用者看到的搜尋許可權。</span><span class="sxs-lookup"><span data-stu-id="cb232-157">The Azure DevOps connector supports search permissions visible to  **Only people with access to this data source** or **Everyone**.</span></span> <span data-ttu-id="cb232-158">如果您選擇 [ **只有可存取此資料來源的人員**]，針對 Azure DevOps 中組織、專案或區域路徑層級的使用者或群組的許可權，針對其存取權的使用者，將會在搜尋結果中顯示索引的資料。</span><span class="sxs-lookup"><span data-stu-id="cb232-158">If you choose **Only people with access to this data source**, indexed data will appear in the search results for users who have access to them based on permissions to users or groups at the Organization, Project or Area path level in Azure DevOps.</span></span> <span data-ttu-id="cb232-159">如果您選擇 [ **任何人**]，索引資料將會出現在所有使用者的搜尋結果中。</span><span class="sxs-lookup"><span data-stu-id="cb232-159">If you choose **Everyone**, indexed data will appear in the search results for all users.</span></span>

## <a name="step-5-assign-property-labels"></a><span data-ttu-id="cb232-160">步驟5：指派屬性標籤</span><span class="sxs-lookup"><span data-stu-id="cb232-160">Step 5: Assign property labels</span></span>

<span data-ttu-id="cb232-161">遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。</span><span class="sxs-lookup"><span data-stu-id="cb232-161">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>

## <a name="step-6-manage-schema"></a><span data-ttu-id="cb232-162">步驟6：管理架構</span><span class="sxs-lookup"><span data-stu-id="cb232-162">Step 6: Manage schema</span></span>

<span data-ttu-id="cb232-163">遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。</span><span class="sxs-lookup"><span data-stu-id="cb232-163">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>

## <a name="step-7-choose-refresh-settings"></a><span data-ttu-id="cb232-164">步驟7：選擇重新整理設定</span><span class="sxs-lookup"><span data-stu-id="cb232-164">Step 7: Choose refresh settings</span></span>

<span data-ttu-id="cb232-165">Azure DevOps 連接器支援完整和累加編目的更新排程。</span><span class="sxs-lookup"><span data-stu-id="cb232-165">The Azure DevOps connector supports refresh schedules for both full and incremental crawls.</span></span>
<span data-ttu-id="cb232-166">建議的排程為一小時用於增量編目，而一天則是完整編目。</span><span class="sxs-lookup"><span data-stu-id="cb232-166">The recommended schedule is one hour for an incremental crawl and one day for a full crawl.</span></span>

## <a name="step-8-review-connection"></a><span data-ttu-id="cb232-167">步驟8：檢查連線</span><span class="sxs-lookup"><span data-stu-id="cb232-167">Step 8: Review connection</span></span>

<span data-ttu-id="cb232-168">遵循一般 [設定指示](https://docs.microsoft.com/microsoftsearch/configure-connector)。</span><span class="sxs-lookup"><span data-stu-id="cb232-168">Follow the general [setup instructions](https://docs.microsoft.com/microsoftsearch/configure-connector).</span></span>
<!---If the above phrase does not apply, delete it and insert specific details for your data source that are different from general setup 
instructions.-->

<!---## Troubleshooting-->
<!---Insert troubleshooting recommendations for this data source-->

<!---## Limitations-->
<!---Insert limitations for this data source-->
