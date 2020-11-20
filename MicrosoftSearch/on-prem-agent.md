---
title: 在部署代理程式上
ms.author: rusamai
author: rsamai
manager: jameslau
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 部署代理程式
ms.openlocfilehash: 30ddf0ac8c6df76d1c598606754066b3d2e93615
ms.sourcegitcommit: 59cdd3f0f82b7918399bf44d27d9891076090f4f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2020
ms.locfileid: "49367730"
---
# <a name="on-prem-agent"></a><span data-ttu-id="dcc02-103">部署代理程式</span><span class="sxs-lookup"><span data-stu-id="dcc02-103">On-Prem Agent</span></span>

## <a name="graph-connector-agent"></a><span data-ttu-id="dcc02-104">圖形連接器代理程式</span><span class="sxs-lookup"><span data-stu-id="dcc02-104">Graph connector agent</span></span>

<span data-ttu-id="dcc02-105">部署圖形連接器需要安裝 *Graph 連接器代理程式* 軟體。</span><span class="sxs-lookup"><span data-stu-id="dcc02-105">On-prem Graph connectors require you to install *Graph connector agent* software.</span></span> <span data-ttu-id="dcc02-106">它允許在內部部署資料和雲端服務之間進行快速且安全的資料傳輸。</span><span class="sxs-lookup"><span data-stu-id="dcc02-106">It allows quick and secure data transfer between on-premises data and cloud services.</span></span> <span data-ttu-id="dcc02-107">本文將引導您完成安裝及設定軟體的步驟。</span><span class="sxs-lookup"><span data-stu-id="dcc02-107">This article guides you through the steps of installing and configuring the software.</span></span> <span data-ttu-id="dcc02-108">設定之後，就可以從 [Microsoft 365 系統管理中心](https://admin.microsoft.com)建立部署資料來源的連線。</span><span class="sxs-lookup"><span data-stu-id="dcc02-108">Once configured, it will be available for creating connections to your on-prem data sources from the [Microsoft 365 admin center](https://admin.microsoft.com).</span></span>

## <a name="installation"></a><span data-ttu-id="dcc02-109">安裝</span><span class="sxs-lookup"><span data-stu-id="dcc02-109">Installation</span></span>

<span data-ttu-id="dcc02-110">使用 [此連結](https://download.microsoft.com/download/d/d/e/dde18236-9c67-437d-a864-894a0a888ef2/AgentPackage.msi) 下載最新版的 Graph connector agent，並使用安裝精靈安裝軟體。</span><span class="sxs-lookup"><span data-stu-id="dcc02-110">Download the latest version of Graph connector agent using [this link](https://download.microsoft.com/download/d/d/e/dde18236-9c67-437d-a864-894a0a888ef2/AgentPackage.msi) and install the software using the installation wizard.</span></span> <span data-ttu-id="dcc02-111">使用下列所述機器的建議設定，軟體可順利處理最多三個連接。</span><span class="sxs-lookup"><span data-stu-id="dcc02-111">With the recommended configuration of the machine described below, the software can seamlessly handle up to three connections.</span></span> <span data-ttu-id="dcc02-112">超過此數目的任何連線可能會降低效能。</span><span class="sxs-lookup"><span data-stu-id="dcc02-112">Any connections beyond that might degrade the performance.</span></span>

<span data-ttu-id="dcc02-113">建議的設定：</span><span class="sxs-lookup"><span data-stu-id="dcc02-113">Recommended configuration:</span></span>

* <span data-ttu-id="dcc02-114">Windows 10、Windows Server 2012 R2 及更新版本</span><span class="sxs-lookup"><span data-stu-id="dcc02-114">Windows 10, Windows Server 2012 R2 and above</span></span>
* <span data-ttu-id="dcc02-115">8核心，3GHz</span><span class="sxs-lookup"><span data-stu-id="dcc02-115">8 cores, 3GHz</span></span>
* <span data-ttu-id="dcc02-116">16GB RAM，1GB 磁碟空間</span><span class="sxs-lookup"><span data-stu-id="dcc02-116">16GB RAM, 1GB Disk Space</span></span>
* <span data-ttu-id="dcc02-117">透過443對資料來源和網際網路的網路存取</span><span class="sxs-lookup"><span data-stu-id="dcc02-117">Network access to data source and internet through 443</span></span>

## <a name="creating-app-for-the-agent"></a><span data-ttu-id="dcc02-118">建立代理程式的應用程式</span><span class="sxs-lookup"><span data-stu-id="dcc02-118">Creating App for the agent</span></span>  

<span data-ttu-id="dcc02-119">在建立連線之前，必須將代理實例送入少數幾個重要參數。</span><span class="sxs-lookup"><span data-stu-id="dcc02-119">The agent instance needs to be fed few critical parameters before you create connections.</span></span> <span data-ttu-id="dcc02-120">這些參數包含使用圖形攝取 APIs 所需的驗證詳細資料。</span><span class="sxs-lookup"><span data-stu-id="dcc02-120">These parameters include authentication details required for using Graph ingestion APIs.</span></span>  

<span data-ttu-id="dcc02-121">建立代理程式之應用程式的步驟。</span><span class="sxs-lookup"><span data-stu-id="dcc02-121">Steps for creating App for the agent.</span></span>

1. <span data-ttu-id="dcc02-122">移至 [Azure 入口網站](https://portal.azure.com) ，並使用系統管理員認證登入以供租使用者使用。</span><span class="sxs-lookup"><span data-stu-id="dcc02-122">Go to the [Azure portal](https://portal.azure.com) and sign in with admin credentials for the tenant.</span></span>
2. <span data-ttu-id="dcc02-123">從功能窗格流覽至 [ **Azure Active Directory**  ->  **應用程式註冊**]，然後選取 [**新增註冊**]。</span><span class="sxs-lookup"><span data-stu-id="dcc02-123">Navigate to **Azure Active Directory** -> **App registrations** from the navigation pane and select **New registration**.</span></span>
3. <span data-ttu-id="dcc02-124">提供應用程式的名稱，然後選取 [ **註冊**]。</span><span class="sxs-lookup"><span data-stu-id="dcc02-124">Provide a name for the app and select **Register**.</span></span>
4. <span data-ttu-id="dcc02-125">記下應用程式 (用戶端) 識別碼。</span><span class="sxs-lookup"><span data-stu-id="dcc02-125">Make a note of the Application (client) ID.</span></span>
5. <span data-ttu-id="dcc02-126">從功能窗格開啟 **API 許可權** ，然後選取 [ **新增許可權**]。</span><span class="sxs-lookup"><span data-stu-id="dcc02-126">Open **API permissions** from the navigation pane and select **Add a permission**.</span></span>
6. <span data-ttu-id="dcc02-127">選取 [ **Microsoft Graph]** ，然後選取 [ **應用程式許可權**]。</span><span class="sxs-lookup"><span data-stu-id="dcc02-127">Select **Microsoft Graph** and then **Application permissions**.</span></span>
7. <span data-ttu-id="dcc02-128">從許可權搜尋 "ReadWrite ExternalItem" 和「Directory. all」，然後選取 [ **新增許可權**]。</span><span class="sxs-lookup"><span data-stu-id="dcc02-128">Search for "ExternalItem.ReadWrite.All" and "Directory.Read.All" from the permissions and select **Add permissions**.</span></span>
8. <span data-ttu-id="dcc02-129">選取 **[授與「TenantName] 的系統管理員同意** ，並選取 [ **是**]。</span><span class="sxs-lookup"><span data-stu-id="dcc02-129">Select **Grant admin consent for [TenantName]** and confirm by selecting **Yes**.</span></span>
9. <span data-ttu-id="dcc02-130">檢查許可權是否處於授與的狀態。</span><span class="sxs-lookup"><span data-stu-id="dcc02-130">Check that the permissions are in the granted state.</span></span>
     <span data-ttu-id="dcc02-131">![顯示為以綠色的右側欄授與的許可權。](media/onprem-agent/granted-state.png)</span><span class="sxs-lookup"><span data-stu-id="dcc02-131">![Permissions shown as granted in green on right hand column.](media/onprem-agent/granted-state.png)</span></span>

## <a name="configuring-graph-connector-agent"></a><span data-ttu-id="dcc02-132">設定圖表連接器代理程式</span><span class="sxs-lookup"><span data-stu-id="dcc02-132">Configuring Graph connector agent</span></span>

<span data-ttu-id="dcc02-133">建立代理程式之後，您必須設定代理程式的適當驗證詳細資料。</span><span class="sxs-lookup"><span data-stu-id="dcc02-133">Once you have created the App for the agent, you must configure the agent with appropriate authentication details.</span></span>

<span data-ttu-id="dcc02-134">您可以在下列其中一個表單中提供驗證詳細資料。</span><span class="sxs-lookup"><span data-stu-id="dcc02-134">Authentication details can be provided in one of the following forms.</span></span>

### <a name="configuring-the-client-secret-for-authentation"></a><span data-ttu-id="dcc02-135">設定 authentation 的用戶端密碼</span><span class="sxs-lookup"><span data-stu-id="dcc02-135">Configuring the client secret for authentation</span></span>

1. <span data-ttu-id="dcc02-136">移至 [Azure 入口網站](https://portal.azure.com) ，並使用系統管理員認證登入以供租使用者使用。</span><span class="sxs-lookup"><span data-stu-id="dcc02-136">Go to the [Azure portal](https://portal.azure.com) and sign in with admin credentials for the tenant.</span></span>
2. <span data-ttu-id="dcc02-137">從功能窗格開啟 **應用程式註冊** ，然後移至適當的應用程式。</span><span class="sxs-lookup"><span data-stu-id="dcc02-137">Open **App Registration** from the navigation pane and go to the appropriate App.</span></span> <span data-ttu-id="dcc02-138">在 [ **管理**] 下，選取 [ **憑證和機密**]。</span><span class="sxs-lookup"><span data-stu-id="dcc02-138">Under **Manage**, select **Certificates and secrets**.</span></span>
3. <span data-ttu-id="dcc02-139">選取 [ **新增用戶端密碼** ]，然後選取密碼到期期限。</span><span class="sxs-lookup"><span data-stu-id="dcc02-139">Select **New Client secret** and select an expiry period for the secret.</span></span> <span data-ttu-id="dcc02-140">複製產生的密碼並加以儲存，因為它不會再次顯示。</span><span class="sxs-lookup"><span data-stu-id="dcc02-140">Copy the generated secret and save it because it will not be shown again.</span></span>
4. <span data-ttu-id="dcc02-141">使用此用戶端密碼和應用程式識別碼來設定代理程式。</span><span class="sxs-lookup"><span data-stu-id="dcc02-141">Use this Client secret along with the Application ID to configure the agent.</span></span> <span data-ttu-id="dcc02-142">請勿在代理程式的 [ **名稱** ] 欄位中使用任何空格。</span><span class="sxs-lookup"><span data-stu-id="dcc02-142">Do not use any blank spaces in the **Name** field of the agent.</span></span> <span data-ttu-id="dcc02-143">會接受字母數位字元。</span><span class="sxs-lookup"><span data-stu-id="dcc02-143">Alpha numeric characters are accepted.</span></span>

## <a name="using-thumbprint-certificate-for-authentication"></a><span data-ttu-id="dcc02-144">使用指紋憑證進行驗證</span><span class="sxs-lookup"><span data-stu-id="dcc02-144">Using thumbprint certificate for authentication</span></span>

<span data-ttu-id="dcc02-145">如果您已透過設定 [authentation 的用戶端密碼](#Configuring-the-client-secret-for-authentication) 來設定驗證詳細資料，您可以將 directy 跳到 [安裝程式概述](configure-connector.md)。</span><span class="sxs-lookup"><span data-stu-id="dcc02-145">If you have already configured the authentication details by following [Configuring the client secret for authentation](#Configuring-the-client-secret-for-authentication) , then you can jump directy to [Setup overview](configure-connector.md).</span></span>

1. <span data-ttu-id="dcc02-146">開啟 **應用程式註冊** ，然後從功能窗格中選取 **憑證和密碼** 。</span><span class="sxs-lookup"><span data-stu-id="dcc02-146">Open **App registration** and select **Certificates and secrets** from the navigation pane.</span></span> <span data-ttu-id="dcc02-147">複製憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="dcc02-147">Copy the certificate thumbprint.</span></span>
<span data-ttu-id="dcc02-148">![在左窗格中選取憑證和密碼時的 thumbrint 憑證清單](media/onprem-agent/certificates.png)</span><span class="sxs-lookup"><span data-stu-id="dcc02-148">![List of thumbrint certificates when Certificates and secrets is selected in the left pane](media/onprem-agent/certificates.png)</span></span>
2. <span data-ttu-id="dcc02-149">使用用戶端密碼或指紋來註冊圖形連接器代理程式。</span><span class="sxs-lookup"><span data-stu-id="dcc02-149">Use either the client secret or thumbprint to register the Graph connector agent.</span></span>
<span data-ttu-id="dcc02-150">![登錄表單要求名稱、應用程式識別碼、憑證類型和憑證](media/onprem-agent/register.png)</span><span class="sxs-lookup"><span data-stu-id="dcc02-150">![Register form asking for name, app id, credential type, and certificate](media/onprem-agent/register.png)</span></span>
