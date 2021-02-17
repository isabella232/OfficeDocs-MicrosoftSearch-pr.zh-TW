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
ms.openlocfilehash: bd5212d42fe21583aa6a4e0dc8060d5e191a7292
ms.sourcegitcommit: 35b4246cb3e38c6fe21540686e28fe54154b33f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/16/2021
ms.locfileid: "50259427"
---
# <a name="graph-connector-agent"></a><span data-ttu-id="2d5d2-103">圖形連接器代理程式</span><span class="sxs-lookup"><span data-stu-id="2d5d2-103">Graph connector agent</span></span>

<span data-ttu-id="2d5d2-104">使用部署圖形連接器時，需要安裝 *Graph 連接器代理程式* 軟體。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-104">Using on-prem Graph connectors require you to install *Graph connector agent* software.</span></span> <span data-ttu-id="2d5d2-105">它可讓內部部署資料與圖形連接器之間的安全資料傳輸 APIs。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-105">It allows for secure data transfer between on-premises data and the Graph connector APIs.</span></span> <span data-ttu-id="2d5d2-106">本文將引導您完成安裝和設定代理程式的步驟。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-106">This article guides you through the installing and configuring the agent.</span></span>

## <a name="installation"></a><span data-ttu-id="2d5d2-107">安裝</span><span class="sxs-lookup"><span data-stu-id="2d5d2-107">Installation</span></span>

<span data-ttu-id="2d5d2-108">[在這裡](https://aka.ms/gcadownload)下載最新版本的圖形連接器代理程式，並使用安裝精靈安裝軟體。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-108">Download the latest version of Graph connector agent [here](https://aka.ms/gcadownload) and install the software using the installation wizard.</span></span> <span data-ttu-id="2d5d2-109">使用下列所述機器的建議設定，軟體最多可以處理三個連接。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-109">Using the recommended configuration of the machine described below, the software can handle up to three connections.</span></span> <span data-ttu-id="2d5d2-110">超過該數目的任何連線可能會降低代理程式上所有連接的效能。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-110">Any connections beyond that might degrade the performance of all connections on the agent.</span></span>

<span data-ttu-id="2d5d2-111">建議的設定：</span><span class="sxs-lookup"><span data-stu-id="2d5d2-111">Recommended configuration:</span></span>

* <span data-ttu-id="2d5d2-112">Windows 10、Windows Server 2016 R2 及更新版本</span><span class="sxs-lookup"><span data-stu-id="2d5d2-112">Windows 10, Windows Server 2016 R2 and above</span></span>
* [<span data-ttu-id="2d5d2-113">.NET Core Desktop Runtime 3.1 (x64) </span><span class="sxs-lookup"><span data-stu-id="2d5d2-113">.NET Core Desktop Runtime 3.1 (x64)</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)
* <span data-ttu-id="2d5d2-114">8核心，3 GHz</span><span class="sxs-lookup"><span data-stu-id="2d5d2-114">8 cores, 3 GHz</span></span>
* <span data-ttu-id="2d5d2-115">16 GB 的 RAM，2 GB 的磁碟空間</span><span class="sxs-lookup"><span data-stu-id="2d5d2-115">16 GB RAM, 2 GB Disk Space</span></span>
* <span data-ttu-id="2d5d2-116">透過443對資料來源和網際網路的網路存取</span><span class="sxs-lookup"><span data-stu-id="2d5d2-116">Network access to data source and internet through 443</span></span>

<span data-ttu-id="2d5d2-117">安裝代理程式之後，如果您組織的 proxy 伺服器或防火牆封鎖與未知網域的通訊，請將下列專案新增至 [允許] 清單。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-117">After you install the agent, if your organization's proxy servers or firewalls block communication to unknown domains, please add below ones to the allow list.</span></span>

1. <span data-ttu-id="2d5d2-118">\*.servicebus.windows.net</span><span class="sxs-lookup"><span data-stu-id="2d5d2-118">\*.servicebus.windows.net</span></span>
2. <span data-ttu-id="2d5d2-119">events.data.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="2d5d2-119">\*.events.data.microsoft.com</span></span>
3. <span data-ttu-id="2d5d2-120"> https://<span>login.microsoftonline.</span>com</span><span class="sxs-lookup"><span data-stu-id="2d5d2-120">https://<span>login.microsoftonline.</span>com</span></span>
4. <span data-ttu-id="2d5d2-121"> HTTPs://<span>gc。</span>com</span><span class="sxs-lookup"><span data-stu-id="2d5d2-121">https://<span>gcs.office.</span>com/</span></span>
5. <span data-ttu-id="2d5d2-122"> HTTPs://<span>graph。</span>com</span><span class="sxs-lookup"><span data-stu-id="2d5d2-122">https://<span>graph.microsoft.</span>com/</span></span>


## <a name="create-and-configure-an-app-for-the-agent"></a><span data-ttu-id="2d5d2-123">建立及設定代理程式的應用程式</span><span class="sxs-lookup"><span data-stu-id="2d5d2-123">Create and configure an App for the agent</span></span>  

<span data-ttu-id="2d5d2-124">首先，登入並注意，帳戶的必要許可權最低為「搜尋管理員」。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-124">First, sign in and note that the minimum required privilege on the account is search administrator.</span></span> <span data-ttu-id="2d5d2-125">然後，代理程式會要求您提供驗證詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-125">The agent will then ask you to provide authentication details.</span></span> <span data-ttu-id="2d5d2-126">使用下列步驟來建立應用程式，並產生必要的驗證詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-126">Use the steps below to create an app and generate the required authentication details.</span></span>

### <a name="create-an-app"></a><span data-ttu-id="2d5d2-127">建立應用程式</span><span class="sxs-lookup"><span data-stu-id="2d5d2-127">Create an app</span></span>

1. <span data-ttu-id="2d5d2-128">移至 [Azure 入口網站](https://portal.azure.com) ，並使用系統管理員認證登入以供租使用者使用。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-128">Go to the [Azure portal](https://portal.azure.com) and sign in with admin credentials for the tenant.</span></span>
2. <span data-ttu-id="2d5d2-129">從功能窗格流覽至 [ **Azure Active Directory**  ->  **應用程式註冊**]，然後選取 [**新增註冊**]。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-129">Navigate to **Azure Active Directory** -> **App registrations** from the navigation pane and select **New registration**.</span></span>
3. <span data-ttu-id="2d5d2-130">提供應用程式的名稱，然後選取 [ **註冊**]。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-130">Provide a name for the app and select **Register**.</span></span>
4. <span data-ttu-id="2d5d2-131">記下應用程式 (用戶端) 識別碼。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-131">Make a note of the Application (client) ID.</span></span>
5. <span data-ttu-id="2d5d2-132">從功能窗格開啟 **API 許可權** ，然後選取 [ **新增許可權**]。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-132">Open **API permissions** from the navigation pane and select **Add a permission**.</span></span>
6. <span data-ttu-id="2d5d2-133">選取 [ **Microsoft Graph]** ，然後選取 [ **應用程式許可權**]。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-133">Select **Microsoft Graph** and then **Application permissions**.</span></span>
7. <span data-ttu-id="2d5d2-134">從許可權搜尋 "ReadWrite ExternalItem" 和「Directory. all」，然後選取 [ **新增許可權**]。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-134">Search for "ExternalItem.ReadWrite.All" and "Directory.Read.All" from the permissions and select **Add permissions**.</span></span>
8. <span data-ttu-id="2d5d2-135">選取 **[授與「TenantName] 的系統管理員同意** ，並選取 [ **是**]。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-135">Select **Grant admin consent for [TenantName]** and confirm by selecting **Yes**.</span></span>
9. <span data-ttu-id="2d5d2-136">檢查許可權是否處於「授與」狀態。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-136">Check that the permissions are in the "granted" state.</span></span>
     <span data-ttu-id="2d5d2-137">![顯示為以綠色的右側欄授與的許可權。](media/onprem-agent/granted-state.png)</span><span class="sxs-lookup"><span data-stu-id="2d5d2-137">![Permissions shown as granted in green on right hand column.](media/onprem-agent/granted-state.png)</span></span>

### <a name="configure-authentication"></a><span data-ttu-id="2d5d2-138">設定驗證</span><span class="sxs-lookup"><span data-stu-id="2d5d2-138">Configure Authentication</span></span>

<span data-ttu-id="2d5d2-139">您可以使用用戶端密碼或憑證提供驗證詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-139">Authentication details can be provided using a client secret or a certificate.</span></span> <span data-ttu-id="2d5d2-140">遵循您的選擇步驟。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-140">Follow the steps of your choice.</span></span>

#### <a name="configuring-the-client-secret-for-authentication"></a><span data-ttu-id="2d5d2-141">設定用戶端密碼進行驗證</span><span class="sxs-lookup"><span data-stu-id="2d5d2-141">Configuring the client secret for authentication</span></span>

1. <span data-ttu-id="2d5d2-142">移至 [Azure 入口網站](https://portal.azure.com) ，並使用系統管理員認證登入以供租使用者使用。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-142">Go to the [Azure portal](https://portal.azure.com) and sign in with admin credentials for the tenant.</span></span>
2. <span data-ttu-id="2d5d2-143">從功能窗格開啟 **應用程式註冊** ，然後移至適當的應用程式。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-143">Open **App Registration** from the navigation pane and go to the appropriate App.</span></span> <span data-ttu-id="2d5d2-144">在 [ **管理**] 下，選取 [ **憑證和機密**]。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-144">Under **Manage**, select **Certificates and secrets**.</span></span>
3. <span data-ttu-id="2d5d2-145">選取 [ **新增用戶端密碼** ]，然後選取密碼到期期限。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-145">Select **New Client secret** and select an expiry period for the secret.</span></span> <span data-ttu-id="2d5d2-146">複製產生的密碼並加以儲存，因為它不會再次顯示。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-146">Copy the generated secret and save it because it won't be shown again.</span></span>
4. <span data-ttu-id="2d5d2-147">使用此用戶端密碼和應用程式識別碼來設定代理程式。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-147">Use this Client secret along with the Application ID to configure the agent.</span></span> <span data-ttu-id="2d5d2-148">您無法在代理程式的 [ **名稱** ] 欄位中使用空格。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-148">You cannot use blank spaces in the **Name** field of the agent.</span></span> <span data-ttu-id="2d5d2-149">會接受字母數位字元。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-149">Alpha numeric characters are accepted.</span></span>

#### <a name="using-a-certificate-for-authentication"></a><span data-ttu-id="2d5d2-150">使用憑證進行驗證</span><span class="sxs-lookup"><span data-stu-id="2d5d2-150">Using a certificate for authentication</span></span>

<span data-ttu-id="2d5d2-151">使用憑證型驗證有三個簡單的步驟：</span><span class="sxs-lookup"><span data-stu-id="2d5d2-151">There are three simple steps for using certificate-based authentication:</span></span>

1. <span data-ttu-id="2d5d2-152">建立或取得憑證</span><span class="sxs-lookup"><span data-stu-id="2d5d2-152">Create or obtain a certificate</span></span>
1. <span data-ttu-id="2d5d2-153">將憑證上傳至 Azure 入口網站</span><span class="sxs-lookup"><span data-stu-id="2d5d2-153">Upload the certificate to the Azure portal</span></span>
1. <span data-ttu-id="2d5d2-154">將憑證指派給代理程式</span><span class="sxs-lookup"><span data-stu-id="2d5d2-154">Assign the certificate to the agent</span></span>

##### <a name="step-1-get-a-certificate"></a><span data-ttu-id="2d5d2-155">步驟1：取得憑證</span><span class="sxs-lookup"><span data-stu-id="2d5d2-155">Step 1: Get a certificate</span></span>

<span data-ttu-id="2d5d2-156">下列腳本可用於產生自我簽署憑證。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-156">The script below can be used to generate a self-signed certificate.</span></span> <span data-ttu-id="2d5d2-157">您的組織可能不允許自我簽署的憑證。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-157">Your organization may not allow self-signed certificates.</span></span> <span data-ttu-id="2d5d2-158">在此情況下，請使用此資訊來瞭解需求，並根據組織的原則取得憑證。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-158">In that case, use this information to understand the requirements and acquire a certificate in accordance to your organization's policies.</span></span>

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

##### <a name="step-2-upload-the-certificate-in-the-azure-portal"></a><span data-ttu-id="2d5d2-159">步驟2：在 Azure 入口網站中上傳憑證</span><span class="sxs-lookup"><span data-stu-id="2d5d2-159">Step 2: Upload the certificate in the Azure portal</span></span>

1. <span data-ttu-id="2d5d2-160">開啟應用程式，並流覽至左窗格中的 [憑證和機密] 區段</span><span class="sxs-lookup"><span data-stu-id="2d5d2-160">Open the application and navigate to certificates and secrets section from left pane</span></span>
1. <span data-ttu-id="2d5d2-161">選取「上傳憑證」並上傳 .cer 檔案</span><span class="sxs-lookup"><span data-stu-id="2d5d2-161">Select 'Upload certificate' and upload the .cer file</span></span>
1. <span data-ttu-id="2d5d2-162">開啟 **應用程式註冊** ，然後從功能窗格中選取 **憑證和密碼** 。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-162">Open **App registration** and select **Certificates and secrets** from the navigation pane.</span></span> <span data-ttu-id="2d5d2-163">複製憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-163">Copy the certificate thumbprint.</span></span>

![在左窗格中選取憑證和密碼時的 thumbrint 憑證清單](media/onprem-agent/certificates.png)

##### <a name="step-3-assign-the-certificate-to-the-agent"></a><span data-ttu-id="2d5d2-165">步驟3：將憑證指派給代理程式</span><span class="sxs-lookup"><span data-stu-id="2d5d2-165">Step 3: Assign the certificate to the agent</span></span>

<span data-ttu-id="2d5d2-166">如果您使用範例腳本來產生憑證，則可以在腳本中所識別的位置找到 PFX 檔案。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-166">If you used the sample script to generate a certificate, the PFX file can be found in the location identified in the script.</span></span>

1. <span data-ttu-id="2d5d2-167">將憑證 pfx 檔案下載到代理程式電腦上。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-167">Download the certificate pfx file onto the Agent machine.</span></span>
1. <span data-ttu-id="2d5d2-168">連按兩下 pfx 檔，以啟動 [憑證安裝] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-168">Double-click the pfx file to launch the certificate installation dialog.</span></span>
1. <span data-ttu-id="2d5d2-169">在安裝憑證時，選取存放區位置的「本機電腦」。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-169">Select 'Local Machine' for store location while installing the certificate.</span></span>
1. <span data-ttu-id="2d5d2-170">安裝憑證之後，請透過「開始」功能表開啟「管理電腦憑證」</span><span class="sxs-lookup"><span data-stu-id="2d5d2-170">After installing the certificate, open 'Manage computer certificates' through Start menu</span></span>
1. <span data-ttu-id="2d5d2-171">選取「個人」-> ' 憑證 ' 下的新安裝憑證</span><span class="sxs-lookup"><span data-stu-id="2d5d2-171">Select the newly installed certificate under 'Personal' -> 'Certificates'</span></span>
1. <span data-ttu-id="2d5d2-172">在 cert 上按一下滑鼠右鍵，並選取「所有工作」-> ' 管理私密金鑰 ... '</span><span class="sxs-lookup"><span data-stu-id="2d5d2-172">Right click on the cert and select 'All Tasks' -> 'Manage Private Keys…'</span></span> <span data-ttu-id="2d5d2-173">選項</span><span class="sxs-lookup"><span data-stu-id="2d5d2-173">Option</span></span>
1. <span data-ttu-id="2d5d2-174">在 [許可權] 對話方塊中，選取 [新增] 選項。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-174">In the permissions dialog, select add option.</span></span> <span data-ttu-id="2d5d2-175">在 [使用者選擇] 對話方塊中寫入： ' NT Service\GcaHostService '，然後按一下 [確定]。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-175">In the user selection dialog, write: 'NT Service\GcaHostService' and click 'OK'.</span></span> <span data-ttu-id="2d5d2-176">請勿按一下 [檢查名稱] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-176">Don't click the 'Check Names' button.</span></span>
1. <span data-ttu-id="2d5d2-177">在 [許可權] 對話方塊中按一下 [確定]。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-177">Click okay on the permissions dialog.</span></span> <span data-ttu-id="2d5d2-178">代理程式機器現在已設定為讓代理程式使用憑證來產生權杖。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-178">The agent machine is now configured for agent to generate tokens using the certificate.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="2d5d2-179">疑難排解</span><span class="sxs-lookup"><span data-stu-id="2d5d2-179">Troubleshooting</span></span>
1. <span data-ttu-id="2d5d2-180">如果連線失敗，出現錯誤 ' 1011：圖形連接器代理程式無法連線或離線」。 ' 請登入安裝代理程式的機器，如果尚未執行代理程式，請將其啟動。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-180">If a connection fails with the error '1011: The Graph connector agent is not reachable or offline.', log in to the machine where agent is installed and start the agent application if it isn't running already.</span></span> <span data-ttu-id="2d5d2-181">如果連線持續失敗，請確認在註冊期間提供給代理程式的憑證或用戶端密碼未到期且具有必要許可權。</span><span class="sxs-lookup"><span data-stu-id="2d5d2-181">If the connection continues to fail, verify that the certificate or client secret provided to the agent during registration hasn't expired and has required permissions.</span></span>
