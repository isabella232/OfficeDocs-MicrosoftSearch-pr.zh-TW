---
title: On-Premises 代理程式
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
ROBOTS: NoIndex
description: 部署代理程式
ms.openlocfilehash: 763904f8dd96c5db8b0633e36795443502afe7d0
ms.sourcegitcommit: 0ed8ec8b3c4e0f5f669005081fd8b2219f07b4f0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/25/2020
ms.locfileid: "49420831"
---
# <a name="graph-connector-agent"></a><span data-ttu-id="bb3e3-103">圖形連接器代理程式</span><span class="sxs-lookup"><span data-stu-id="bb3e3-103">Graph connector agent</span></span>

<span data-ttu-id="bb3e3-104">使用部署圖形連接器時，需要安裝 *Graph 連接器代理程式* 軟體。</span><span class="sxs-lookup"><span data-stu-id="bb3e3-104">Using on-prem Graph connectors require you to install *Graph connector agent* software.</span></span> <span data-ttu-id="bb3e3-105">它可讓內部部署資料與圖形連接器之間的安全資料傳輸 APIs。</span><span class="sxs-lookup"><span data-stu-id="bb3e3-105">It allows for secure data transfer between on-premises data and the Graph connector APIs.</span></span> <span data-ttu-id="bb3e3-106">本文將引導您完成安裝和設定代理程式的步驟。</span><span class="sxs-lookup"><span data-stu-id="bb3e3-106">This article guides you through the installing and configuring the agent.</span></span>

## <a name="installation"></a><span data-ttu-id="bb3e3-107">安裝</span><span class="sxs-lookup"><span data-stu-id="bb3e3-107">Installation</span></span>

<span data-ttu-id="bb3e3-108">[在這裡](https://aka.ms/gcadownload)下載最新版本的圖形連接器代理程式，並使用安裝精靈安裝軟體。</span><span class="sxs-lookup"><span data-stu-id="bb3e3-108">Download the latest version of Graph connector agent [here](https://aka.ms/gcadownload) and install the software using the installation wizard.</span></span> <span data-ttu-id="bb3e3-109">使用下列所述機器的建議設定，軟體最多可以處理三個連接。</span><span class="sxs-lookup"><span data-stu-id="bb3e3-109">Using the recommended configuration of the machine described below, the software can handle up to three connections.</span></span> <span data-ttu-id="bb3e3-110">超過該數目的任何連線可能會降低代理程式上所有連接的效能。</span><span class="sxs-lookup"><span data-stu-id="bb3e3-110">Any connections beyond that might degrade the performance of all connections on the agent.</span></span>

<span data-ttu-id="bb3e3-111">建議的設定：</span><span class="sxs-lookup"><span data-stu-id="bb3e3-111">Recommended configuration:</span></span>

* <span data-ttu-id="bb3e3-112">Windows 10、Windows Server 2016 R2 及更新版本</span><span class="sxs-lookup"><span data-stu-id="bb3e3-112">Windows 10, Windows Server 2016 R2 and above</span></span>
* <span data-ttu-id="bb3e3-113">8核心，3 GHz</span><span class="sxs-lookup"><span data-stu-id="bb3e3-113">8 cores, 3 GHz</span></span>
* <span data-ttu-id="bb3e3-114">16 GB 的 RAM，2 GB 的磁碟空間</span><span class="sxs-lookup"><span data-stu-id="bb3e3-114">16 GB RAM, 2 GB Disk Space</span></span>
* <span data-ttu-id="bb3e3-115">透過443對資料來源和網際網路的網路存取</span><span class="sxs-lookup"><span data-stu-id="bb3e3-115">Network access to data source and internet through 443</span></span>

## <a name="create-and-configure-an-app-for-the-agent"></a><span data-ttu-id="bb3e3-116">建立及設定代理程式的應用程式</span><span class="sxs-lookup"><span data-stu-id="bb3e3-116">Create and configure an App for the agent</span></span>  

<span data-ttu-id="bb3e3-117">使用代理程式之前，您必須先建立應用程式，並設定驗證詳細資料。</span><span class="sxs-lookup"><span data-stu-id="bb3e3-117">Before using the agent, you must create an app and configure the authentication details.</span></span>

### <a name="create-an-app"></a><span data-ttu-id="bb3e3-118">建立應用程式</span><span class="sxs-lookup"><span data-stu-id="bb3e3-118">Create an app</span></span>

1. <span data-ttu-id="bb3e3-119">移至 [Azure 入口網站](https://portal.azure.com) ，並使用系統管理員認證登入以供租使用者使用。</span><span class="sxs-lookup"><span data-stu-id="bb3e3-119">Go to the [Azure portal](https://portal.azure.com) and sign in with admin credentials for the tenant.</span></span>
2. <span data-ttu-id="bb3e3-120">從功能窗格流覽至 [ **Azure Active Directory**  ->  **應用程式註冊**]，然後選取 [**新增註冊**]。</span><span class="sxs-lookup"><span data-stu-id="bb3e3-120">Navigate to **Azure Active Directory** -> **App registrations** from the navigation pane and select **New registration**.</span></span>
3. <span data-ttu-id="bb3e3-121">提供應用程式的名稱，然後選取 [ **註冊**]。</span><span class="sxs-lookup"><span data-stu-id="bb3e3-121">Provide a name for the app and select **Register**.</span></span>
4. <span data-ttu-id="bb3e3-122">記下應用程式 (用戶端) 識別碼。</span><span class="sxs-lookup"><span data-stu-id="bb3e3-122">Make a note of the Application (client) ID.</span></span>
5. <span data-ttu-id="bb3e3-123">從功能窗格開啟 **API 許可權** ，然後選取 [ **新增許可權**]。</span><span class="sxs-lookup"><span data-stu-id="bb3e3-123">Open **API permissions** from the navigation pane and select **Add a permission**.</span></span>
6. <span data-ttu-id="bb3e3-124">選取 [ **Microsoft Graph]** ，然後選取 [ **應用程式許可權**]。</span><span class="sxs-lookup"><span data-stu-id="bb3e3-124">Select **Microsoft Graph** and then **Application permissions**.</span></span>
7. <span data-ttu-id="bb3e3-125">從許可權搜尋 "ReadWrite ExternalItem" 和「Directory. all」，然後選取 [ **新增許可權**]。</span><span class="sxs-lookup"><span data-stu-id="bb3e3-125">Search for "ExternalItem.ReadWrite.All" and "Directory.Read.All" from the permissions and select **Add permissions**.</span></span>
8. <span data-ttu-id="bb3e3-126">選取 **[授與「TenantName] 的系統管理員同意** ，並選取 [ **是**]。</span><span class="sxs-lookup"><span data-stu-id="bb3e3-126">Select **Grant admin consent for [TenantName]** and confirm by selecting **Yes**.</span></span>
9. <span data-ttu-id="bb3e3-127">檢查許可權是否處於「授與」狀態。</span><span class="sxs-lookup"><span data-stu-id="bb3e3-127">Check that the permissions are in the "granted" state.</span></span>
     <span data-ttu-id="bb3e3-128">![顯示為以綠色的右側欄授與的許可權。](media/onprem-agent/granted-state.png)</span><span class="sxs-lookup"><span data-stu-id="bb3e3-128">![Permissions shown as granted in green on right hand column.](media/onprem-agent/granted-state.png)</span></span>

### <a name="configure-authentication"></a><span data-ttu-id="bb3e3-129">設定驗證</span><span class="sxs-lookup"><span data-stu-id="bb3e3-129">Configure Authentication</span></span>

<span data-ttu-id="bb3e3-130">您可以使用用戶端密碼或憑證提供驗證詳細資料。</span><span class="sxs-lookup"><span data-stu-id="bb3e3-130">Authentication details can be provided using a client secret or a certificate.</span></span> <span data-ttu-id="bb3e3-131">遵循您的選擇的步驟。</span><span class="sxs-lookup"><span data-stu-id="bb3e3-131">Follow the steps for your choice.</span></span>

#### <a name="configuring-the-client-secret-for-authentication"></a><span data-ttu-id="bb3e3-132">設定用戶端密碼進行驗證</span><span class="sxs-lookup"><span data-stu-id="bb3e3-132">Configuring the client secret for authentication</span></span>

1. <span data-ttu-id="bb3e3-133">移至 [Azure 入口網站](https://portal.azure.com) ，並使用系統管理員認證登入以供租使用者使用。</span><span class="sxs-lookup"><span data-stu-id="bb3e3-133">Go to the [Azure portal](https://portal.azure.com) and sign in with admin credentials for the tenant.</span></span>
2. <span data-ttu-id="bb3e3-134">從功能窗格開啟 **應用程式註冊** ，然後移至適當的應用程式。</span><span class="sxs-lookup"><span data-stu-id="bb3e3-134">Open **App Registration** from the navigation pane and go to the appropriate App.</span></span> <span data-ttu-id="bb3e3-135">在 [ **管理**] 下，選取 [ **憑證和機密**]。</span><span class="sxs-lookup"><span data-stu-id="bb3e3-135">Under **Manage**, select **Certificates and secrets**.</span></span>
3. <span data-ttu-id="bb3e3-136">選取 [ **新增用戶端密碼** ]，然後選取密碼到期期限。</span><span class="sxs-lookup"><span data-stu-id="bb3e3-136">Select **New Client secret** and select an expiry period for the secret.</span></span> <span data-ttu-id="bb3e3-137">複製產生的密碼並加以儲存，因為它不會再次顯示。</span><span class="sxs-lookup"><span data-stu-id="bb3e3-137">Copy the generated secret and save it because it won't be shown again.</span></span>
4. <span data-ttu-id="bb3e3-138">使用此用戶端密碼和應用程式識別碼來設定代理程式。</span><span class="sxs-lookup"><span data-stu-id="bb3e3-138">Use this Client secret along with the Application ID to configure the agent.</span></span> <span data-ttu-id="bb3e3-139">您無法在代理程式的 [ **名稱** ] 欄位中使用空格。</span><span class="sxs-lookup"><span data-stu-id="bb3e3-139">You cannot use blank spaces in the **Name** field of the agent.</span></span> <span data-ttu-id="bb3e3-140">會接受字母數位字元。</span><span class="sxs-lookup"><span data-stu-id="bb3e3-140">Alpha numeric characters are accepted.</span></span>

#### <a name="using-a-certificate-for-authentication"></a><span data-ttu-id="bb3e3-141">使用憑證進行驗證</span><span class="sxs-lookup"><span data-stu-id="bb3e3-141">Using a certificate for authentication</span></span>

<span data-ttu-id="bb3e3-142">使用憑證型驗證有三個簡單的步驟：</span><span class="sxs-lookup"><span data-stu-id="bb3e3-142">There are three simple steps for using certificate-based authentication:</span></span>

1. <span data-ttu-id="bb3e3-143">建立或取得憑證</span><span class="sxs-lookup"><span data-stu-id="bb3e3-143">Create or obtain a certificate</span></span>
1. <span data-ttu-id="bb3e3-144">將憑證上傳至 Azure 入口網站</span><span class="sxs-lookup"><span data-stu-id="bb3e3-144">Upload the certificate to the Azure portal</span></span>
1. <span data-ttu-id="bb3e3-145">將憑證指派給代理程式</span><span class="sxs-lookup"><span data-stu-id="bb3e3-145">Assign the certificate to the agent</span></span>

##### <a name="step-1-get-a-certificate"></a><span data-ttu-id="bb3e3-146">步驟1：取得憑證</span><span class="sxs-lookup"><span data-stu-id="bb3e3-146">Step 1: Get a certificate</span></span>

<span data-ttu-id="bb3e3-147">下列腳本可用於產生自我簽署憑證。</span><span class="sxs-lookup"><span data-stu-id="bb3e3-147">The script below can be used to generate a self-signed certificate.</span></span> <span data-ttu-id="bb3e3-148">您的組織可能不允許自我簽署的憑證。</span><span class="sxs-lookup"><span data-stu-id="bb3e3-148">Your organization may not allow self-signed certificates.</span></span> <span data-ttu-id="bb3e3-149">在此情況下，請使用此資訊來瞭解需求，並根據組織的原則取得憑證。</span><span class="sxs-lookup"><span data-stu-id="bb3e3-149">In that case, use this information to understand the requirements and acquire a certificate in accordance to your organization's policies.</span></span>

```Powershell
$dnsName = "<TenantDomain like agent.onmicrosoft.com>" # Your DNS name
$password = "<password>" # Certificate password
$folderPath = "D:\New folder\" # Where do you want the files to get saved to? The folder needs to exist.
$fileName = "agentcert" # What do you want to call the cert files? without the file extension
$yearsValid = 10 # Number of years until you need to renew the certificate
$certStoreLocation = "cert:\LocalMachine\My"
$expirationDate = (Get-Date).AddYears($yearsValid)
$certificate = New-SelfSignedCertificate -DnsName $dnsName -CertStoreLocation $certStoreLocation -NotAfter $expirationDate -KeyExportPolicy Exportable -KeySpec Signature
$certificatePath = $certStoreLocation + '\' + $certificate.Thumbprint
$filePath = $folderPath + '\' + $fileName
$securePassword = ConvertTo-SecureString -String $password -Force -AsPlainText
Export-Certificate -Cert $certificatePath -FilePath ($filePath + '.cer')
Export-PfxCertificate -Cert $certificatePath -FilePath ($filePath + '.pfx') -Password $securePassword
```

##### <a name="step-2-upload-the-certificate-in-the-azure-portal"></a><span data-ttu-id="bb3e3-150">步驟2：在 Azure 入口網站中上傳憑證</span><span class="sxs-lookup"><span data-stu-id="bb3e3-150">Step 2: Upload the certificate in the Azure portal</span></span>

1. <span data-ttu-id="bb3e3-151">開啟應用程式，並流覽至左窗格中的 [憑證和機密] 區段</span><span class="sxs-lookup"><span data-stu-id="bb3e3-151">Open the application and navigate to certificates and secrets section from left pane</span></span>
1. <span data-ttu-id="bb3e3-152">選取「上傳憑證」並上傳 .cer 檔案</span><span class="sxs-lookup"><span data-stu-id="bb3e3-152">Select 'Upload certificate' and upload the .cer file</span></span>
1. <span data-ttu-id="bb3e3-153">開啟 **應用程式註冊** ，然後從功能窗格中選取 **憑證和密碼** 。</span><span class="sxs-lookup"><span data-stu-id="bb3e3-153">Open **App registration** and select **Certificates and secrets** from the navigation pane.</span></span> <span data-ttu-id="bb3e3-154">複製憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="bb3e3-154">Copy the certificate thumbprint.</span></span>

![在左窗格中選取憑證和密碼時的 thumbrint 憑證清單](media/onprem-agent/certificates.png)

##### <a name="step-3-assign-the-certificate-to-the-agent"></a><span data-ttu-id="bb3e3-156">步驟3：將憑證指派給代理程式</span><span class="sxs-lookup"><span data-stu-id="bb3e3-156">Step 3: Assign the certificate to the agent</span></span>

<span data-ttu-id="bb3e3-157">如果您使用範例腳本來產生憑證，則可以在腳本中所識別的位置找到 PFX 檔案。</span><span class="sxs-lookup"><span data-stu-id="bb3e3-157">If you used the sample script to generate a certificate, the PFX file can be found in the location identified in the script.</span></span>

1. <span data-ttu-id="bb3e3-158">將憑證 pfx 檔案下載到代理程式電腦上。</span><span class="sxs-lookup"><span data-stu-id="bb3e3-158">Download the certificate pfx file onto the Agent machine.</span></span>
1. <span data-ttu-id="bb3e3-159">連按兩下 pfx 檔，以啟動 [憑證安裝] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="bb3e3-159">Double-click the pfx file to launch the certificate installation dialog.</span></span>
1. <span data-ttu-id="bb3e3-160">在安裝憑證時，選取存放區位置的「本機電腦」。</span><span class="sxs-lookup"><span data-stu-id="bb3e3-160">Select 'Local Machine' for store location while installing the certificate.</span></span>
1. <span data-ttu-id="bb3e3-161">安裝憑證之後，請透過「開始」功能表開啟「管理電腦憑證」</span><span class="sxs-lookup"><span data-stu-id="bb3e3-161">After installing the certificate, open 'Manage computer certificates' through Start menu</span></span>
1. <span data-ttu-id="bb3e3-162">選取「個人」-> ' 憑證 ' 下的新安裝憑證</span><span class="sxs-lookup"><span data-stu-id="bb3e3-162">Select the newly installed certificate under 'Personal' -> 'Certificates'</span></span>
1. <span data-ttu-id="bb3e3-163">在 cert 上按一下滑鼠右鍵，並選取「所有工作」-> ' 管理私密金鑰 ... '</span><span class="sxs-lookup"><span data-stu-id="bb3e3-163">Right click on the cert and select 'All Tasks' -> 'Manage Private Keys…'</span></span> <span data-ttu-id="bb3e3-164">選項</span><span class="sxs-lookup"><span data-stu-id="bb3e3-164">Option</span></span>
1. <span data-ttu-id="bb3e3-165">在 [許可權] 對話方塊中，選取 [新增] 選項。</span><span class="sxs-lookup"><span data-stu-id="bb3e3-165">In the permissions dialog, select add option.</span></span> <span data-ttu-id="bb3e3-166">在 [使用者選擇] 對話方塊中寫入： ' NT Service\GcaHostService '，然後按一下 [確定]。</span><span class="sxs-lookup"><span data-stu-id="bb3e3-166">In the user selection dialog, write: 'NT Service\GcaHostService' and click 'OK'.</span></span> <span data-ttu-id="bb3e3-167">請勿按一下 [檢查名稱] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="bb3e3-167">Don't click the 'Check Names' button.</span></span>
1. <span data-ttu-id="bb3e3-168">在 [許可權] 對話方塊中按一下 [確定]。</span><span class="sxs-lookup"><span data-stu-id="bb3e3-168">Click okay on the permissions dialog.</span></span> <span data-ttu-id="bb3e3-169">代理程式機器現在已設定為讓代理程式使用憑證來產生權杖。</span><span class="sxs-lookup"><span data-stu-id="bb3e3-169">The agent machine is now configured for agent to generate tokens using the certificate.</span></span>
