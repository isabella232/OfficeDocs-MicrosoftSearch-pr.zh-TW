---
title: Microsoft 搜尋的檔案共用連接器
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
description: 設定 Microsoft 搜尋的檔案共用連接器。
ms.openlocfilehash: 2349ad753508d5f19a70648d9cbf1df495b27108
ms.sourcegitcommit: 7eda9b621def0659d7e7bc8b989f8adc929cce93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2020
ms.locfileid: "44861092"
---
# <a name="file-share-connector"></a><span data-ttu-id="b10ec-103">檔共用連接器</span><span class="sxs-lookup"><span data-stu-id="b10ec-103">File share connector</span></span>

<span data-ttu-id="b10ec-104">您的組織中的使用者可以使用檔案共用連接器，來搜尋內部部署檔案共用。</span><span class="sxs-lookup"><span data-stu-id="b10ec-104">With the file share connector, users in your organization can search on-premises file shares.</span></span> <span data-ttu-id="b10ec-105">這些共用的搜尋結果會合並來自[SharePoint](http://sharepoint.com/)和[商務 OneDrive 公司](https://onedrive.live.com/about/business/)的結果。</span><span class="sxs-lookup"><span data-stu-id="b10ec-105">The search results from these shares merge with the results from [SharePoint](http://sharepoint.com/) and [Microsoft OneDrive for Business](https://onedrive.live.com/about/business/).</span></span>

<span data-ttu-id="b10ec-106">本文適用于[Microsoft 365](https://www.microsoft.com/microsoft-365)系統管理員或任何設定、執行及監視檔案共用連接器的人員。</span><span class="sxs-lookup"><span data-stu-id="b10ec-106">This article is for [Microsoft 365](https://www.microsoft.com/microsoft-365) administrators or anyone who configures, runs, and monitors a file share connector.</span></span> <span data-ttu-id="b10ec-107">它說明如何設定連接器和連接器功能、限制及疑難排解技術。</span><span class="sxs-lookup"><span data-stu-id="b10ec-107">It explains how to configure your connector and connector capabilities, limitations, and troubleshooting techniques.</span></span>

## <a name="install-a-data-gateway"></a><span data-ttu-id="b10ec-108">安裝資料閘道</span><span class="sxs-lookup"><span data-stu-id="b10ec-108">Install a data gateway</span></span>
<span data-ttu-id="b10ec-109">為了存取協力廠商資料，您必須安裝和設定[Microsoft POWER BI](https://msit.powerbi.com/)閘道。</span><span class="sxs-lookup"><span data-stu-id="b10ec-109">In order to access your third-party data, you must install and configure a [Microsoft Power BI](https://msit.powerbi.com/) gateway.</span></span> <span data-ttu-id="b10ec-110">請參閱[安裝內部部署閘道](https://docs.microsoft.com/data-integration/gateway/service-gateway-install)以深入瞭解。</span><span class="sxs-lookup"><span data-stu-id="b10ec-110">See [Install an on-premises gateway](https://docs.microsoft.com/data-integration/gateway/service-gateway-install) to learn more.</span></span>  

## <a name="content-requirements"></a><span data-ttu-id="b10ec-111">內容需求</span><span class="sxs-lookup"><span data-stu-id="b10ec-111">Content requirements</span></span>
<span data-ttu-id="b10ec-112">**檔案類型**。</span><span class="sxs-lookup"><span data-stu-id="b10ec-112">**File types**.</span></span> <span data-ttu-id="b10ec-113">只有這些格式的檔案可以進行索引及搜尋： DOC，.DOCM，.DOCX，點，DOTX，.EML，GIF，HTML，JPEG，.MHT，MHTML，MSG，NWS，OBD，OBT，ODP，ODS，ODT，ONE，PDF，.POT，PPS，PPTM，XLB，XLS，.XLSX，.XLT，.xlc，XML，XPS，和 ZIP。</span><span class="sxs-lookup"><span data-stu-id="b10ec-113">Only files in these formats can be indexed and searched: DOC, DOCM, DOCX, DOT, DOTX, EML, GIF, HTML, JPEG, MHT, MHTML, MSG, NWS, OBD, OBT, ODP, ODS, ODT, ONE, PDF, POT, PPS, PPT, PPTM, PPTX, TXT, XLB, XLC, XLSB, XLS, XLSX, XLT, XLXM, XML, XPS, and ZIP.</span></span> <span data-ttu-id="b10ec-114">只會為這些格式的文字內容編制索引。</span><span class="sxs-lookup"><span data-stu-id="b10ec-114">Only the textual content of these formats is indexed.</span></span> <span data-ttu-id="b10ec-115">會忽略所有多媒體內容。</span><span class="sxs-lookup"><span data-stu-id="b10ec-115">All multimedia content is ignored.</span></span>
 
<span data-ttu-id="b10ec-116">**檔案大小限制**。</span><span class="sxs-lookup"><span data-stu-id="b10ec-116">**File size limits**.</span></span> <span data-ttu-id="b10ec-117">支援的檔案大小上限為 100 MB。</span><span class="sxs-lookup"><span data-stu-id="b10ec-117">The maximum supported file size is 100 MB.</span></span> <span data-ttu-id="b10ec-118">從索引中略過超過 100 MB 的檔案。</span><span class="sxs-lookup"><span data-stu-id="b10ec-118">Files that exceed 100 MB are skipped from indexing.</span></span> <span data-ttu-id="b10ec-119">後處理的最大大小限制為 4 MB。</span><span class="sxs-lookup"><span data-stu-id="b10ec-119">The maximum post-processed size limit is 4 MB.</span></span> <span data-ttu-id="b10ec-120">當檔案大小達到 4 MB 時，處理便會停止。</span><span class="sxs-lookup"><span data-stu-id="b10ec-120">Processing stops when a file's size reaches 4 MB.</span></span> <span data-ttu-id="b10ec-121">因此，檔案中所提供的部分片語可能無法用於搜尋。</span><span class="sxs-lookup"><span data-stu-id="b10ec-121">As a result, some phrases present in the file might not work for search.</span></span>

## <a name="connect-to-a-data-source"></a><span data-ttu-id="b10ec-122">連接到資料來源</span><span class="sxs-lookup"><span data-stu-id="b10ec-122">Connect to a data source</span></span>
<span data-ttu-id="b10ec-123">在 [連線**至資料來源]** 頁面上，選取 [檔案**共用**]，並提供名稱、連線識別碼及描述。</span><span class="sxs-lookup"><span data-stu-id="b10ec-123">On the **Connect to data source** page, select **File share** and provide the name, connection ID, and description.</span></span> <span data-ttu-id="b10ec-124">在下一個頁面上，提供檔案共用的路徑，然後選取您先前安裝的閘道。</span><span class="sxs-lookup"><span data-stu-id="b10ec-124">On the next page, provide the path to the file share and select your previously installed gateway.</span></span> <span data-ttu-id="b10ec-125">輸入[Microsoft Windows](https://microsoft.com/windows)使用者帳戶的認證，該帳戶具有共用中所有檔案的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="b10ec-125">Enter the credentials for a [Microsoft Windows](https://microsoft.com/windows) user account with read access to all the files in the share.</span></span> <span data-ttu-id="b10ec-126">請移至其餘的設定，併發布連接。</span><span class="sxs-lookup"><span data-stu-id="b10ec-126">Go through the rest of the settings and publish the connection.</span></span>

## <a name="set-the-refresh-schedule"></a><span data-ttu-id="b10ec-127">設定重新整理排程</span><span class="sxs-lookup"><span data-stu-id="b10ec-127">Set the refresh schedule</span></span>
<span data-ttu-id="b10ec-128">建議的預設重新整理排程間隔為15分鐘，但您可以將它變更為您想要的其他間隔。</span><span class="sxs-lookup"><span data-stu-id="b10ec-128">The recommended default refresh schedule interval is 15 minutes, but you can change it to another interval that you prefer.</span></span>

## <a name="set-up-your-search-results-page"></a><span data-ttu-id="b10ec-129">設定您的搜尋結果頁面</span><span class="sxs-lookup"><span data-stu-id="b10ec-129">Set up your search results page</span></span>
<span data-ttu-id="b10ec-130">若要在 [**全部** **] 和**[檔案] 索引標籤中顯示不同的檔案連線結果，您必須設定[SharePoint](http://sharepoint.com/)的「搜尋引擎結果」頁面：</span><span class="sxs-lookup"><span data-stu-id="b10ec-130">To display different file connection results in the **All** and **Files** tabs, you need to set up a [SharePoint](http://sharepoint.com/) search engine results page:</span></span>
- <span data-ttu-id="b10ec-131">[ **All** ] （全部）表格會顯示檔案連線、SharePoint 檔案、 [OneDrive](https://onedrive.live.com/about/business/)檔案及 SharePoint 網站的合併結果。</span><span class="sxs-lookup"><span data-stu-id="b10ec-131">The **All** table shows combined results from your file connections, SharePoint files, [OneDrive](https://onedrive.live.com/about/business/) files, and SharePoint sites.</span></span> 
- <span data-ttu-id="b10ec-132">**檔**會顯示所有來自您的連線、SharePoint 及 OneDrive 的檔案結果。</span><span class="sxs-lookup"><span data-stu-id="b10ec-132">The **Files** vertical shows all file results from your connections, SharePoint, and OneDrive.</span></span>
<span data-ttu-id="b10ec-133">在 [**全部**] 和 [檔案] 的行業**中，會**將來自檔連線的結果新增至現有的結果。</span><span class="sxs-lookup"><span data-stu-id="b10ec-133">Results from file connections are added to already existing results in both the **All** and **Files** verticals.</span></span>

<span data-ttu-id="b10ec-134">若要設定搜尋結果頁面，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="b10ec-134">To set up your search results page, take these steps:</span></span>
1. <span data-ttu-id="b10ec-135">使用現代搜尋頁面建立 SharePoint 網站集合。</span><span class="sxs-lookup"><span data-stu-id="b10ec-135">Create a SharePoint site collection with a modern search page.</span></span>

2. <span data-ttu-id="b10ec-136">安裝[SharePoint 線上管理命令](https://www.microsoft.com/download/details.aspx?id=35588)介面。</span><span class="sxs-lookup"><span data-stu-id="b10ec-136">Install a [SharePoint Online Management Shell](https://www.microsoft.com/download/details.aspx?id=35588).</span></span>

3. <span data-ttu-id="b10ec-137">以系統管理員身分開啟 SharePoint 線上管理命令介面，然後匯入出現**Microsoft.SharePoint.Client.dll**模組 `C:\Windows\Microsoft.NET\assembly\GAC_MSIL\Microsoft.SharePoint.Client\v4.0_16.0.0.0__71e9bce111e9429c\Microsoft.SharePoint.Client.dll` 。</span><span class="sxs-lookup"><span data-stu-id="b10ec-137">Open SharePoint Online Management Shell as an administrator and import the **Microsoft.SharePoint.Client.dll** module present at `C:\Windows\Microsoft.NET\assembly\GAC_MSIL\Microsoft.SharePoint.Client\v4.0_16.0.0.0__71e9bce111e9429c\Microsoft.SharePoint.Client.dll`.</span></span>

> [!NOTE]
> <span data-ttu-id="b10ec-138">所有使用者的此路徑可能並不相同。</span><span class="sxs-lookup"><span data-stu-id="b10ec-138">This path might not be the same for all users.</span></span>

<span data-ttu-id="b10ec-139">若要匯入模組，請在[SharePoint 線上管理命令](https://www.microsoft.com/download/details.aspx?id=35588)介面中執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="b10ec-139">To import the module, run this command in [SharePoint Online Management Shell](https://www.microsoft.com/download/details.aspx?id=35588):</span></span>
```bash
Import-Module "C:\Windows\Microsoft.NET\assembly\GAC_MSIL\Microsoft.SharePoint.Client\v4.0_16.0.0.0__71e9bce111e9429c\Microsoft.SharePoint.Client.dll" 
```

4. <span data-ttu-id="b10ec-140">現在執行此腳本：</span><span class="sxs-lookup"><span data-stu-id="b10ec-140">Now run this script:</span></span>
```bash
$orgName = Read-Host -prompt 'Please enter your org name'
$userName = Read-Host -prompt 'Enter user name'
$userCreds = Get-Credential -UserName $userName -Message "Type the password"
Connect-SPOService -Url https://$orgName-admin.sharepoint.com -Credential $userCreds

$url = Read-Host -Prompt 'Please enter the site url'
$site = Get-SPOSite -Identity $url
Set-SPOSite $url -DenyAddAndCustomizePages 0

$pwd = Read-Host -AsSecureString 'type the password'
$context = New-Object Microsoft.SharePoint.Client.ClientContext($url)
$credential = New-Object Microsoft.SharePoint.Client.SharePointOnlineCredentials($userName, $pwd)
$context.Credentials = $credential
$web = $context.Web
$context.Load($web)
$web.AllProperties["AllVerticalContent"] = "Combined"
$web.Update()
$context.ExecuteQuery()
$web.AllProperties["FilesVerticalContent"] = "ConnectorsOnly"
$web.Update()
$context.ExecuteQuery()
Set-SPOSite $url -DenyAddAndCustomizePages 1

Write-Host "Success" -ForegroundColor Cyan
Read-Host -Prompt 'Press enter to exit'
```

5. <span data-ttu-id="b10ec-141">在[Microsoft PowerShell](https://microsoft.com/powershell)中輸入必要的值，例如組織名稱、使用者名稱、密碼和網站 URL。</span><span class="sxs-lookup"><span data-stu-id="b10ec-141">Enter the required values in [Microsoft PowerShell](https://microsoft.com/powershell), such as organization name, username, password, and site URL.</span></span> <span data-ttu-id="b10ec-142">**舉例來說**，如果您的系統管理員認證為 `admin@a830edad9050849823J19081300.onmicrosoft.com` ，則您的組織名稱是**a830edad9050849823J19081300**，而您的網站 URL 是 `https:// a830edad9050849823J19081300.sharepoint.com` 。</span><span class="sxs-lookup"><span data-stu-id="b10ec-142">As an **example**, if your admin credentials are `admin@a830edad9050849823J19081300.onmicrosoft.com`, then your organization name is **a830edad9050849823J19081300**, and your site URL is `https:// a830edad9050849823J19081300.sharepoint.com`.</span></span>

> [!NOTE]
> <span data-ttu-id="b10ec-143">**AllProperties**設定只可在網站集合層級（團隊/Comms 網站）上進行。</span><span class="sxs-lookup"><span data-stu-id="b10ec-143">The **AllProperties** setting can only be done at a site collection level (Teams/Comms site).</span></span>

6. <span data-ttu-id="b10ec-144">現在您可以搜尋已編制索引的檔案 **，並在**[**全部**] 和 [檔案] 索引標籤中查看結果。</span><span class="sxs-lookup"><span data-stu-id="b10ec-144">Now you can search for indexed files and see results in both the **All** and **Files** tabs.</span></span>

## <a name="search-for-file-share-content-in-the-search-results-page"></a><span data-ttu-id="b10ec-145">在搜尋結果頁面中搜尋檔案共用內容</span><span class="sxs-lookup"><span data-stu-id="b10ec-145">Search for file share content in the search results page</span></span>
<span data-ttu-id="b10ec-146">若要搜尋已編制索引的內容，請移至測試租使用者的[SharePoint](http://sharepoint.com/)首頁。</span><span class="sxs-lookup"><span data-stu-id="b10ec-146">To search for indexed content, go to the [SharePoint](http://sharepoint.com/) home page of your test tenant.</span></span> <span data-ttu-id="b10ec-147">結果會顯示在 [**全部** **] 和**[檔案] 索引標籤中。</span><span class="sxs-lookup"><span data-stu-id="b10ec-147">Results will be displayed in the **All** and **Files** tabs.</span></span>

<span data-ttu-id="b10ec-148">由於瀏覽器限制，您無法選取檔結果以查看或開啟本機檔案共用搜尋中的檔案。</span><span class="sxs-lookup"><span data-stu-id="b10ec-148">Because of browser restrictions, you can't select a file result to view or open files from local file share searches.</span></span> <span data-ttu-id="b10ec-149">若要開啟這些檔案，請複製檔結果的連結，並將其貼到系統瀏覽器的 [位址] 欄中。</span><span class="sxs-lookup"><span data-stu-id="b10ec-149">To open these files, copy the file result's link and paste it into the address bar of your system's browser.</span></span> <span data-ttu-id="b10ec-150">若為[windows](https://microsoft.com/windows)，請使用 windows Explorer。</span><span class="sxs-lookup"><span data-stu-id="b10ec-150">For [Windows](https://microsoft.com/windows), use Windows Explorer.</span></span> <span data-ttu-id="b10ec-151">然後，您就可以在系統上開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="b10ec-151">Then you can open the file on your system.</span></span>

![使用 [複製連結] 對話方塊開啟搜尋 SharePoint。](media/fileshare-search.png)

## <a name="troubleshooting"></a><span data-ttu-id="b10ec-153">疑難排解</span><span class="sxs-lookup"><span data-stu-id="b10ec-153">Troubleshooting</span></span>
<span data-ttu-id="b10ec-154">如果連接發生嚴重錯誤，其狀態會顯示為 [**失敗**]。</span><span class="sxs-lookup"><span data-stu-id="b10ec-154">If something is critically wrong with a connection, its status shows as **failed**.</span></span> <span data-ttu-id="b10ec-155">若要取得三種錯誤類型的詳細資訊，請移至**錯誤詳細資料**頁面並選取失敗的連線。</span><span class="sxs-lookup"><span data-stu-id="b10ec-155">To get more information on the three types of errors, go to the **error details** page and select the failing connection.</span></span> <span data-ttu-id="b10ec-156">請參閱[管理您的連接器](manage-connector.md)以深入瞭解。</span><span class="sxs-lookup"><span data-stu-id="b10ec-156">See [Manage your connector](manage-connector.md) to learn more.</span></span>
1. <span data-ttu-id="b10ec-157">**無法連線閘道（錯誤碼：11）**。</span><span class="sxs-lookup"><span data-stu-id="b10ec-157">**Gateway not reachable (error code: 11)**.</span></span> <span data-ttu-id="b10ec-158">連接的閘道電腦已關機。</span><span class="sxs-lookup"><span data-stu-id="b10ec-158">The gateway machine for the connection is down.</span></span> <span data-ttu-id="b10ec-159">確認在閘道電腦上是否執行[POWER BI](https://msit.powerbi.com/)處理常式。</span><span class="sxs-lookup"><span data-stu-id="b10ec-159">Verify if the [Power BI](https://msit.powerbi.com/) process runs on the gateway machine.</span></span>
2. <span data-ttu-id="b10ec-160">**驗證錯誤（錯誤碼：12）**。</span><span class="sxs-lookup"><span data-stu-id="b10ec-160">**Authentication error (error code: 12)**.</span></span> <span data-ttu-id="b10ec-161">用來建立連線的認證到期或不再有效。</span><span class="sxs-lookup"><span data-stu-id="b10ec-161">The credentials that were used for creating the connection expired or are no longer valid.</span></span> <span data-ttu-id="b10ec-162">若要解決此錯誤，請輸入有效的認證。</span><span class="sxs-lookup"><span data-stu-id="b10ec-162">To resolve this error, enter valid credentials.</span></span>
3. <span data-ttu-id="b10ec-163">**內部錯誤（錯誤碼：11或 12**以外的任何專案）。</span><span class="sxs-lookup"><span data-stu-id="b10ec-163">**Internal error (error code: anything other than 11 or 12)**.</span></span> <span data-ttu-id="b10ec-164">連接器基礎結構中有錯誤。</span><span class="sxs-lookup"><span data-stu-id="b10ec-164">There's an error in the connector infrastructure.</span></span> <span data-ttu-id="b10ec-165">請參閱[回饋](connectors-feedback.md)文章，以瞭解如何報告這些錯誤。</span><span class="sxs-lookup"><span data-stu-id="b10ec-165">See the [Feedback](connectors-feedback.md) article to find out how to report these errors.</span></span>

## <a name="limitations"></a><span data-ttu-id="b10ec-166">限制</span><span class="sxs-lookup"><span data-stu-id="b10ec-166">Limitations</span></span>
<span data-ttu-id="b10ec-167">檔案共用連接器在預覽版本中有下列限制：</span><span class="sxs-lookup"><span data-stu-id="b10ec-167">The file share connector has these limitations in the preview release:</span></span>
* <span data-ttu-id="b10ec-168">您只能使用固定的屬性（而非具有自訂屬性的檔案）來索引檔案。</span><span class="sxs-lookup"><span data-stu-id="b10ec-168">You can only index files with fixed properties, not files with custom properties.</span></span>
* <span data-ttu-id="b10ec-169">目前不支援檔案共用存取控制清單（ACLs）。</span><span class="sxs-lookup"><span data-stu-id="b10ec-169">File share Access Control Lists (ACLs) aren't currently supported.</span></span> <span data-ttu-id="b10ec-170">只支援 NTFS 檔 ACLs。</span><span class="sxs-lookup"><span data-stu-id="b10ec-170">Only file NTFS ACLs are supported.</span></span>
* <span data-ttu-id="b10ec-171">不支援外部身分識別。</span><span class="sxs-lookup"><span data-stu-id="b10ec-171">External identities aren't supported.</span></span> <span data-ttu-id="b10ec-172">這些識別碼必須對應至[Azure Active Directory](https://docs.microsoft.com/azure/active-directory/)身分識別。</span><span class="sxs-lookup"><span data-stu-id="b10ec-172">They must be mapped to [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/) identities.</span></span>
