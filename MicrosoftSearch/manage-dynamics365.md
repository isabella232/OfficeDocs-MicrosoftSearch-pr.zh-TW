---
title: 'Dynamics 365 同盟搜尋 (預覽) '
ms.author: dawholl
author: dawholl
manager: kellis
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
description: 管理在搜尋結果中顯示 Dynamics 365 內容的方式
ms.openlocfilehash: 5f642bcb026358e57258e5e736fc263616fc4b05
ms.sourcegitcommit: f07a2e578b6c9ed5a1a3b22266cca371782870a7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/22/2021
ms.locfileid: "53067930"
---
# <a name="dynamics-365-federation-search-preview"></a><span data-ttu-id="4d4ed-103">Dynamics 365 同盟搜尋 (預覽) </span><span class="sxs-lookup"><span data-stu-id="4d4ed-103">Dynamics 365 federation search (preview)</span></span>

## <a name="microsoft-search-federation-and-connectors"></a><span data-ttu-id="4d4ed-104">Microsoft 搜尋同盟和連接器</span><span class="sxs-lookup"><span data-stu-id="4d4ed-104">Microsoft Search Federation and connectors</span></span>

<span data-ttu-id="4d4ed-105">為了讓 Microsoft 搜尋更有用，我們正在引進 Microsoft 搜尋同盟。</span><span class="sxs-lookup"><span data-stu-id="4d4ed-105">To help make Microsoft Search more useful, we're introducing Microsoft Search Federation.</span></span> <span data-ttu-id="4d4ed-106">透過同盟搜尋，組織可以在 Microsoft 搜尋中存取這些案例中的資料：</span><span class="sxs-lookup"><span data-stu-id="4d4ed-106">With federated search, organizations can make data in these scenarios accessible in Microsoft Search:</span></span>

* <span data-ttu-id="4d4ed-107">系統中遵循嚴格合規性需求的資料</span><span class="sxs-lookup"><span data-stu-id="4d4ed-107">Data in systems that are subject to strict compliance requirements</span></span>
* <span data-ttu-id="4d4ed-108">無法留下系統界限的資料</span><span class="sxs-lookup"><span data-stu-id="4d4ed-108">Data that can't leave system boundaries</span></span>
* <span data-ttu-id="4d4ed-109">儲存在部署上的敏感性資料，您的組織不想要在雲端上建立索引</span><span class="sxs-lookup"><span data-stu-id="4d4ed-109">Sensitive data stored on-prem that your organization doesn’t want indexed on the cloud</span></span>

<span data-ttu-id="4d4ed-110">透過同盟搜尋連線存取的資料不會在 Microsoft 搜尋中編制索引。</span><span class="sxs-lookup"><span data-stu-id="4d4ed-110">Data accessed through a federated search connection isn't indexed in Microsoft Search.</span></span> <span data-ttu-id="4d4ed-111">此外，您也可以使用 Microsoft 的內建連接器，輕鬆設定同盟搜尋連線。</span><span class="sxs-lookup"><span data-stu-id="4d4ed-111">Also, using built-in connectors from Microsoft, it's easy to set up federated search connections.</span></span> <span data-ttu-id="4d4ed-112">我們的 Dynamics 365 connector 目前正在預覽中。</span><span class="sxs-lookup"><span data-stu-id="4d4ed-112">Our Dynamics 365 connector is currently in preview.</span></span> <span data-ttu-id="4d4ed-113">如果您有興趣加入預覽，請在 [aka.ms/D365FederationSearchPreview](https://aka.ms/D365FederationSearchPreview)中告知我們。</span><span class="sxs-lookup"><span data-stu-id="4d4ed-113">If you're interested in joining the preview, let us know at [aka.ms/D365FederationSearchPreview](https://aka.ms/D365FederationSearchPreview).</span></span>

## <a name="dynamics-365-federation-connector"></a><span data-ttu-id="4d4ed-114">Dynamics 365 同盟連接器</span><span class="sxs-lookup"><span data-stu-id="4d4ed-114">Dynamics 365 federation connector</span></span>

<span data-ttu-id="4d4ed-115">Microsoft Dynamics 365 是一線智慧商務應用程式，專為企業資源規劃及客戶關係管理而設計。</span><span class="sxs-lookup"><span data-stu-id="4d4ed-115">Microsoft Dynamics 365 is a line of intelligent business applications designed for enterprise resource planning and customer relationship management.</span></span> <span data-ttu-id="4d4ed-116">透過 Dynamics 365 同盟，Microsoft 搜尋提供無縫的搜尋體驗，讓使用者可以輕鬆地找出 Dynamics 365 中所儲存的最相關客戶和商務資料。</span><span class="sxs-lookup"><span data-stu-id="4d4ed-116">With Dynamics 365 federation, Microsoft Search provides a seamless search experience, enabling users to easily find the most relevant customer and business data stored in Dynamics 365.</span></span> <span data-ttu-id="4d4ed-117">Dynamics 365 同盟連接器提供一些重要優點：</span><span class="sxs-lookup"><span data-stu-id="4d4ed-117">The Dynamics 365 federation connector provides some key benefits:</span></span>

* <span data-ttu-id="4d4ed-118">**易於管理：** 簡化處理以設定及維護 Dynamics 365 實例的搜尋連線。</span><span class="sxs-lookup"><span data-stu-id="4d4ed-118">**Easy to administer:** Streamlined process to configure and maintain the search connection to a Dynamics 365 instance.</span></span>
* <span data-ttu-id="4d4ed-119">**便於使用：** 使用者可以輕鬆快捷地找到以 Dynamics 365 儲存的重要資訊，包括帳戶、連絡人、開啟的機會等等。</span><span class="sxs-lookup"><span data-stu-id="4d4ed-119">**Easy to use:** Users can easily and quickly find key information stored in Dynamics 365, including accounts, contacts, open opportunities, and more.</span></span>
* <span data-ttu-id="4d4ed-120">**更豐富的內容：** 若要讓 Dynamics 365 搜尋結果更有用，包含潛在客戶、連絡人及帳戶詳細資料等重要資訊。</span><span class="sxs-lookup"><span data-stu-id="4d4ed-120">**Richer content:** To make Dynamics 365 search results more useful, they include key information like leads, contacts, and account details.</span></span>
* <span data-ttu-id="4d4ed-121">**內建資料保護：** Dynamics 365 結果只會針對具有連線的實例存取權的使用者顯示。</span><span class="sxs-lookup"><span data-stu-id="4d4ed-121">**Built-in data protection:** Dynamics 365 results will only appear for users that have access to the connected instance.</span></span>
* <span data-ttu-id="4d4ed-122">**整合的搜尋體驗：** 為了維持統一的體驗，Dynamics 365 的結果在所有搜尋專案點間都是一致的。</span><span class="sxs-lookup"><span data-stu-id="4d4ed-122">**Unified search experience:** To maintain a cohesive experience, Dynamics 365 results are consistent across all search entry points.</span></span> <span data-ttu-id="4d4ed-123">不論您在哪裡搜尋，都可以使用相同的外觀與風格取得相同的結果。</span><span class="sxs-lookup"><span data-stu-id="4d4ed-123">Wherever you search, you'll get the same results with the same look and feel.</span></span>

## <a name="what-users-experience"></a><span data-ttu-id="4d4ed-124">使用者經驗</span><span class="sxs-lookup"><span data-stu-id="4d4ed-124">What users experience</span></span>

<span data-ttu-id="4d4ed-125">Dynamics 365 的答案會出現在所有 Microsoft 搜尋畫布上的搜尋結果中，包括 SharePoint 線上、Bing 和 Office。</span><span class="sxs-lookup"><span data-stu-id="4d4ed-125">Dynamics 365 answers appear in search results across all Microsoft Search canvases, including SharePoint Online, Bing, and Office.</span></span>

:::image type="content" alt-text="SharePoint、Bing 及 Office 的 Dynamics 365 回應的螢幕擷取畫面" source="media/dynamics365/dynamics365-answer.png" lightbox="media/dynamics365/dynamics365-answer.png":::

<span data-ttu-id="4d4ed-127">從問題的答案中，使用 [ **更多 dynamics 365 結果** ] 連結可輕鬆查看更多 dynamics 365 搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="4d4ed-127">From the answer, it's easy to see more Dynamics 365 search results by using the **More Dynamics 365 results** link.</span></span> <span data-ttu-id="4d4ed-128">它會將使用者帶到專用的 Dynamics 365 結果頁面，並提供與查詢相關的更多結果。</span><span class="sxs-lookup"><span data-stu-id="4d4ed-128">It takes users to a dedicated Dynamics 365 results page with more results relevant to their query.</span></span>

:::image type="content" alt-text="Dynamics 365 的螢幕擷取畫面及 SharePoint、Bing 及 Office 的結果" source="media/dynamics365/dynamics365-vertical.png" lightbox="media/dynamics365/dynamics365-vertical.png":::

<span data-ttu-id="4d4ed-130">按一下或攻絲任何結果會開啟 Dynamics 365 並顯示詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="4d4ed-130">Clicking or tapping any result opens Dynamics 365 and shows the detailed information.</span></span>

:::image type="content" alt-text="Dynamics 365 中詳細資料頁面的螢幕擷取畫面" source="media/dynamics365/dynamics365-detail-page.png" lightbox="media/dynamics365/dynamics365-detail-page.png":::

<span data-ttu-id="4d4ed-132">不管您的使用者從何處開始搜尋，其經驗都會是一致的，讓他們能夠快速找到最相關的 Dynamics 365 結果。</span><span class="sxs-lookup"><span data-stu-id="4d4ed-132">No matter where your users start their search their experience will be consistent and enable them to quickly find the most relevant Dynamics 365 results.</span></span> <span data-ttu-id="4d4ed-133">請參閱 Microsoft 組建2021影片以取得示範。</span><span class="sxs-lookup"><span data-stu-id="4d4ed-133">Check out our Microsoft Build 2021 video for a demonstration.</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4P83t]

## <a name="supported-query-patterns"></a><span data-ttu-id="4d4ed-134">支援的查詢模式</span><span class="sxs-lookup"><span data-stu-id="4d4ed-134">Supported query patterns</span></span>

<span data-ttu-id="4d4ed-135">使用 Microsoft 搜尋來尋找 Dynamics 365 結果時，會支援自然語言和產品名稱查詢。</span><span class="sxs-lookup"><span data-stu-id="4d4ed-135">Both natural language and product name queries are supported when using Microsoft Search to find Dynamics 365 results.</span></span> <span data-ttu-id="4d4ed-136">此外，Dynamics 365 查詢不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="4d4ed-136">Also, Dynamics 365 queries aren't case sensitive.</span></span> <span data-ttu-id="4d4ed-137">使用自然語言模式，透過客戶名稱或位置以及其他經常使用的查詢來尋找連絡人、帳戶及機遇。</span><span class="sxs-lookup"><span data-stu-id="4d4ed-137">Use natural language patterns to find contact, account, and opportunities--by customer name or location--and other frequently used queries.</span></span> <span data-ttu-id="4d4ed-138">以下是一些範例：</span><span class="sxs-lookup"><span data-stu-id="4d4ed-138">Here are a few examples:</span></span>

* <span data-ttu-id="4d4ed-139">神秘是 Contoso 的連絡人</span><span class="sxs-lookup"><span data-stu-id="4d4ed-139">Who is the contact for Contoso</span></span>
* <span data-ttu-id="4d4ed-140">Contoso 的開啟機會</span><span class="sxs-lookup"><span data-stu-id="4d4ed-140">Open opportunities for Contoso</span></span>
* <span data-ttu-id="4d4ed-141">西雅圖的開啟機遇</span><span class="sxs-lookup"><span data-stu-id="4d4ed-141">What are open opportunities in Seattle</span></span>
* <span data-ttu-id="4d4ed-142">西雅圖的帳戶是什麼</span><span class="sxs-lookup"><span data-stu-id="4d4ed-142">What are the accounts in Seattle</span></span>
* <span data-ttu-id="4d4ed-143">西雅圖的連絡人</span><span class="sxs-lookup"><span data-stu-id="4d4ed-143">What are the contacts in Seattle</span></span>
* <span data-ttu-id="4d4ed-144">這個月的潛在客戶即將結束</span><span class="sxs-lookup"><span data-stu-id="4d4ed-144">What are my leads closing this month</span></span>
* <span data-ttu-id="4d4ed-145">高優先順序的通話</span><span class="sxs-lookup"><span data-stu-id="4d4ed-145">High priority phone call</span></span>
* <span data-ttu-id="4d4ed-146">連絡人遺失的電子郵件</span><span class="sxs-lookup"><span data-stu-id="4d4ed-146">Contact missing emails</span></span>

<span data-ttu-id="4d4ed-147">產品名稱模式支援 Dynamics 365 應用程式的範圍，並會觸發 Dynamics 365 的結果，不論其在查詢中的出現位置為何：</span><span class="sxs-lookup"><span data-stu-id="4d4ed-147">Product name patterns support a range of Dynamics 365 applications and will trigger Dynamics 365 results regardless of where they appear in a query:</span></span>

* <span data-ttu-id="4d4ed-148">D365</span><span class="sxs-lookup"><span data-stu-id="4d4ed-148">D365</span></span>
* <span data-ttu-id="4d4ed-149">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="4d4ed-149">Dynamics 365</span></span>
* <span data-ttu-id="4d4ed-150">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="4d4ed-150">Dynamics365</span></span>
* <span data-ttu-id="4d4ed-151">Dynamics CRM</span><span class="sxs-lookup"><span data-stu-id="4d4ed-151">Dynamics CRM</span></span>
* <span data-ttu-id="4d4ed-152">Dynamics Sales</span><span class="sxs-lookup"><span data-stu-id="4d4ed-152">Dynamics Sales</span></span>
* <span data-ttu-id="4d4ed-153">Dynamics 客戶服務</span><span class="sxs-lookup"><span data-stu-id="4d4ed-153">Dynamics Customer Service</span></span>
* <span data-ttu-id="4d4ed-154">Dynamics Service</span><span class="sxs-lookup"><span data-stu-id="4d4ed-154">Dynamics Service</span></span>
* <span data-ttu-id="4d4ed-155">Dynamics Field Service</span><span class="sxs-lookup"><span data-stu-id="4d4ed-155">Dynamics Field Service</span></span>

## <a name="configure-the-dynamics-365-connector"></a><span data-ttu-id="4d4ed-156">設定 Dynamics 365 連接器</span><span class="sxs-lookup"><span data-stu-id="4d4ed-156">Configure the Dynamics 365 connector</span></span>

<span data-ttu-id="4d4ed-157">使用此簡單設定，您可以為組織中的人員啟用 Dynamics 365 同盟搜尋體驗。</span><span class="sxs-lookup"><span data-stu-id="4d4ed-157">With this simple configuration, you can enable the Dynamics 365 federation search experience for people in your organization.</span></span>

1. <span data-ttu-id="4d4ed-158">在[Microsoft 365 系統管理中心](https://admin.microsoft.com)中，移至 [[資料來源](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/connectors)]。</span><span class="sxs-lookup"><span data-stu-id="4d4ed-158">In the [Microsoft 365 admin center](https://admin.microsoft.com), go to [Data sources](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/connectors).</span></span>

2. <span data-ttu-id="4d4ed-159">在 [Microsoft 應用程式和服務] 區段的 [Microsoft Dynamics 365] 底下，選取 [ **管理** ] 以開啟 [microsoft dynamics 365] 面板。</span><span class="sxs-lookup"><span data-stu-id="4d4ed-159">In the Microsoft apps and services section, under Microsoft Dynamics 365, select **Manage** to open the Microsoft Dynamics 365 panel.</span></span>

3. <span data-ttu-id="4d4ed-160">為您的組織啟用連接器。</span><span class="sxs-lookup"><span data-stu-id="4d4ed-160">Enable the connector for your organization.</span></span>

4. <span data-ttu-id="4d4ed-161">在 [ **端點** ] 清單中，選取您的 Dynamics 365 環境。</span><span class="sxs-lookup"><span data-stu-id="4d4ed-161">In the **Endpoints** list, select your Dynamics 365 environment.</span></span>

5. <span data-ttu-id="4d4ed-162">在 [連線 **識別碼**] 中，輸入此連線的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="4d4ed-162">In the **Connection ID**, enter a unique ID for this connection.</span></span>

6. <span data-ttu-id="4d4ed-163">檢查並選取 [同意] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="4d4ed-163">Review and select the consent check box.</span></span>

7. <span data-ttu-id="4d4ed-164">選取 [ **儲存** ] 以完成連接設定。</span><span class="sxs-lookup"><span data-stu-id="4d4ed-164">Select **Save** to finish the connection setup.</span></span>

:::image type="content" alt-text="Microsoft 365 系統管理中心中的 Dynamics 365 設定面板的螢幕擷取畫面" source="media/dynamics365/dynamic365-connection-setup.png" lightbox="media/dynamics365/dynamic365-connection-setup.png":::

<span data-ttu-id="4d4ed-166">當設定完成時，只有具有有效 Dynamics 365 授權的使用者和存取互連的 Dynamics 365 環境，才會顯示 Dynamics 365 的答案和垂直。</span><span class="sxs-lookup"><span data-stu-id="4d4ed-166">When the setup is complete, Dynamics 365 answers and vertical will only appear for users with a valid Dynamics 365 license and access to the connected Dynamics 365 environment.</span></span> <span data-ttu-id="4d4ed-167">任何時候，您都可以回到這些設定，並變更連線端點環境或停用連接。</span><span class="sxs-lookup"><span data-stu-id="4d4ed-167">At any time, you can return to these settings and change the connection endpoint environment or deactivate the connection.</span></span>
