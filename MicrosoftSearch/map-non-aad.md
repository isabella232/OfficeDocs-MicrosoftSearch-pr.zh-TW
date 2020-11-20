---
title: 對應非 AAD 識別碼
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
description: 如何對應非 AAD 身分識別的步驟
ms.openlocfilehash: cd7d0eb17678d69ec1966e4472b38c1f18c30809
ms.sourcegitcommit: 59cdd3f0f82b7918399bf44d27d9891076090f4f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2020
ms.locfileid: "49367656"
---
# <a name="map-your-non-azure-ad-identities"></a><span data-ttu-id="f1dab-103">對應您的非 Azure AD 身分識別</span><span class="sxs-lookup"><span data-stu-id="f1dab-103">Map your non-Azure AD Identities</span></span>  

<span data-ttu-id="f1dab-104">本文將引導您完成將您的非 Azure AD 身分識別對應至 Azure AD 身分識別的步驟，讓您的存取控制清單中的人員 (具有非 Azure AD 身分識別的 ACL) 可以查看其範圍內的連接器搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="f1dab-104">This article walks you through the steps of mapping your non-Azure AD identities to your Azure AD identities so that people in your Access Control List (ACL) with non-Azure AD identities can see connector search results scoped to them.</span></span>

<span data-ttu-id="f1dab-105">這些步驟只與使用「存取此資料來源的人」和「 [Salesforce](salesforce-connector.md)非 AAD」的「搜尋」許可權設定 Microsoft 的「搜尋」許可權[ServiceNow](servicenow-connector.md)設定的搜尋系統管理員相關。</span><span class="sxs-lookup"><span data-stu-id="f1dab-105">These steps are only relevant to search administrators who are setting up a [ServiceNow](servicenow-connector.md) or [Salesforce](salesforce-connector.md) connectors by Microsoft with search permissions for "Only people with access to this data source" and identity type "Non-AAD."</span></span>

>[!NOTE]
><span data-ttu-id="f1dab-106">如果您是在 [搜尋許可權] 畫面上設定 Salesforce 連接器並 **只選取可存取此資料來源** 和身分 **識別類型的** 人員，請參閱 [對應 azure ad](map-aad.md) 身分識別文章，以取得如何對應 azure ad 身分識別的步驟。</span><span class="sxs-lookup"><span data-stu-id="f1dab-106">If you are setting up a Salesforce connector and select **Only people with access to this data source** and identity type **AAD** on the search permissions screen, refer to the [Map your Azure AD Identities](map-aad.md) article for steps on how to map Azure AD identities.</span></span>  

## <a name="steps-for-mapping-your-non-azure-ad-properties"></a><span data-ttu-id="f1dab-107">用於對應非 Azure AD 屬性的步驟</span><span class="sxs-lookup"><span data-stu-id="f1dab-107">Steps for mapping your non-Azure AD properties</span></span>

### <a name="1-select-an-azure-ad-user-property"></a><span data-ttu-id="f1dab-108">1. 選取 Azure AD 使用者屬性</span><span class="sxs-lookup"><span data-stu-id="f1dab-108">1. Select an Azure AD user property</span></span>  

<span data-ttu-id="f1dab-109">您可以選取您要建立對應的 Azure AD 使用者屬性。</span><span class="sxs-lookup"><span data-stu-id="f1dab-109">You can select the Azure AD user property you are creating the mapping for.</span></span> <span data-ttu-id="f1dab-110">這是您想要將非 Azure AD 身分識別對應到的目標屬性。</span><span class="sxs-lookup"><span data-stu-id="f1dab-110">This is the target property you are aiming to map your non-Azure AD identities to.</span></span>  

<span data-ttu-id="f1dab-111">您可以選取下列 Azure AD 屬性之一：</span><span class="sxs-lookup"><span data-stu-id="f1dab-111">You can select one of the following Azure AD properties:</span></span>

| <span data-ttu-id="f1dab-112">Azure AD 屬性</span><span class="sxs-lookup"><span data-stu-id="f1dab-112">Azure AD property</span></span>    | <span data-ttu-id="f1dab-113">定義</span><span class="sxs-lookup"><span data-stu-id="f1dab-113">Definition</span></span>           | <span data-ttu-id="f1dab-114">範例</span><span class="sxs-lookup"><span data-stu-id="f1dab-114">Example</span></span>         |
| :------------------- | :------------------- |:--------------- |
| <span data-ttu-id="f1dab-115">使用者主體名稱 (UPN)</span><span class="sxs-lookup"><span data-stu-id="f1dab-115">User Principal Name (UPN)</span></span>  | <span data-ttu-id="f1dab-116">UPN 是由 UPN 首碼所組成 (使用者帳戶名稱) 和 UPN 尾碼 (DNS 功能變數名稱) 。</span><span class="sxs-lookup"><span data-stu-id="f1dab-116">A UPN consists of a UPN prefix (the user account name) and a UPN suffix (a DNS domain name).</span></span> <span data-ttu-id="f1dab-117">首碼是使用 "@" 符號加入尾碼。</span><span class="sxs-lookup"><span data-stu-id="f1dab-117">The prefix is joined with the suffix using the "@" symbol.</span></span> | <span data-ttu-id="f1dab-118">us1@contoso.onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="f1dab-118">us1@contoso.onmicrosoft.com</span></span> |
| <span data-ttu-id="f1dab-119">Azure AD 識別碼</span><span class="sxs-lookup"><span data-stu-id="f1dab-119">Azure AD ID</span></span>                 | <span data-ttu-id="f1dab-120">指定使用者的 Azure AD 識別碼是使用者的唯一 GUID。</span><span class="sxs-lookup"><span data-stu-id="f1dab-120">An Azure AD ID for a given user is the unique GUID of the user.</span></span>                 | <span data-ttu-id="f1dab-121">58006c96-9e6e-45ea-8c88-4a56851eefad</span><span class="sxs-lookup"><span data-stu-id="f1dab-121">58006c96-9e6e-45ea-8c88-4a56851eefad</span></span>            |
| <span data-ttu-id="f1dab-122">Active Directory 安全性識別碼 (SID) </span><span class="sxs-lookup"><span data-stu-id="f1dab-122">Active Directory Security ID (SID)</span></span>                  | <span data-ttu-id="f1dab-123">SID (的安全性識別碼) 是 Active Directory 用來將物件識別為安全性主體的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="f1dab-123">SID (Security Identifier) is a unique identifier that Active Directory uses to identify objects as security principal.</span></span>                  | <span data-ttu-id="f1dab-124">S-1-5-21-453406510-812318184-4183662089</span><span class="sxs-lookup"><span data-stu-id="f1dab-124">S-1-5-21-453406510-812318184-4183662089</span></span>             |

### <a name="2-select-non-azure-ad-user-properties-to-map"></a><span data-ttu-id="f1dab-125">2. 選取非 Azure AD 使用者屬性以進行對應</span><span class="sxs-lookup"><span data-stu-id="f1dab-125">2. Select non-Azure AD user properties to map</span></span>

<span data-ttu-id="f1dab-126">您可以從您的資料來源中選取要套用正則運算式的非 Azure AD 屬性。</span><span class="sxs-lookup"><span data-stu-id="f1dab-126">You can select non-Azure AD properties pulled from your data source to apply regular expressions on.</span></span> <span data-ttu-id="f1dab-127">若要深入瞭解在資料來源中找到這些屬性的詳細資訊，請參閱 [ServiceNow](servicenow-connector.md) 和 [Salesforce](salesforce-connector.md) 頁面。</span><span class="sxs-lookup"><span data-stu-id="f1dab-127">To learn more about where to find these properties in your data source, see the [ServiceNow](servicenow-connector.md) and [Salesforce](salesforce-connector.md) pages.</span></span>  

<span data-ttu-id="f1dab-128">您可以從下拉式清單中選取非 Azure AD 使用者屬性，並提供在這些使用者屬性值上套用正則運算式。</span><span class="sxs-lookup"><span data-stu-id="f1dab-128">You can select a non-Azure AD user property from the dropdown and provide a regular expression to be applied on those user property values.</span></span> <span data-ttu-id="f1dab-129">若要深入瞭解正則運算式，請參閱 [正則運算式參考]( https://docs.microsoft.com/dotnet/standard/base-types/regular-expression-language-quick-reference)。</span><span class="sxs-lookup"><span data-stu-id="f1dab-129">To learn more about regular expressions, see [regular expression reference]( https://docs.microsoft.com/dotnet/standard/base-types/regular-expression-language-quick-reference).</span></span>  

<span data-ttu-id="f1dab-130">以下是一些正則運算式範例及其輸出套用至範例字串的範例：</span><span class="sxs-lookup"><span data-stu-id="f1dab-130">Below are some examples of regular expressions and their outputs applied to a sample string:</span></span> 

| <span data-ttu-id="f1dab-131">範例字串</span><span class="sxs-lookup"><span data-stu-id="f1dab-131">Sample String</span></span>                  | <span data-ttu-id="f1dab-132">正則運算式</span><span class="sxs-lookup"><span data-stu-id="f1dab-132">Regular expression</span></span>                 | <span data-ttu-id="f1dab-133">範例字串上正則運算式的輸出</span><span class="sxs-lookup"><span data-stu-id="f1dab-133">Output of regular expression on sample string</span></span>           |
| :------------------- | :------------------- |:---------------|
| <span data-ttu-id="f1dab-134">Alexis Vasquez</span><span class="sxs-lookup"><span data-stu-id="f1dab-134">Alexis Vasquez</span></span>  | <span data-ttu-id="f1dab-135">.\*</span><span class="sxs-lookup"><span data-stu-id="f1dab-135">.\*</span></span> | <span data-ttu-id="f1dab-136">Alexis Vasquez</span><span class="sxs-lookup"><span data-stu-id="f1dab-136">Alexis Vasquez</span></span> |
| <span data-ttu-id="f1dab-137">Alexis Vasquez</span><span class="sxs-lookup"><span data-stu-id="f1dab-137">Alexis Vasquez</span></span>                 | <span data-ttu-id="f1dab-138">..$</span><span class="sxs-lookup"><span data-stu-id="f1dab-138">..$</span></span>                 | <span data-ttu-id="f1dab-139">Ez</span><span class="sxs-lookup"><span data-stu-id="f1dab-139">ez</span></span>            |
| <span data-ttu-id="f1dab-140">Alexis Vasquez</span><span class="sxs-lookup"><span data-stu-id="f1dab-140">Alexis Vasquez</span></span>                  | <span data-ttu-id="f1dab-141"> ( \w +) $</span><span class="sxs-lookup"><span data-stu-id="f1dab-141">(\w+)$</span></span>                  | <span data-ttu-id="f1dab-142">Vasquez</span><span class="sxs-lookup"><span data-stu-id="f1dab-142">Vasquez</span></span>             |

<span data-ttu-id="f1dab-143">您可以新增任意數目的非 Azure AD 使用者屬性（如您想要的運算式）。</span><span class="sxs-lookup"><span data-stu-id="f1dab-143">You can add as many non-Azure AD user properties as you would like expressions for.</span></span> <span data-ttu-id="f1dab-144">您可以將不同的正則運算式套用至相同的使用者屬性（如果您的最後一個公式保證這樣做）。</span><span class="sxs-lookup"><span data-stu-id="f1dab-144">You can apply different regular expressions to the same user property if your final formula warrants that.</span></span>  

### <a name="3-create-formula-to-complete-mapping"></a><span data-ttu-id="f1dab-145">3. 建立完成對應的公式</span><span class="sxs-lookup"><span data-stu-id="f1dab-145">3. Create formula to complete mapping</span></span>

<span data-ttu-id="f1dab-146">您可以將套用至每個非 Azure AD 使用者屬性之正則運算式的輸出組合在一起，以形成步驟1中所選取的 Azure AD 屬性。</span><span class="sxs-lookup"><span data-stu-id="f1dab-146">You can combine the outputs of the regular expressions applied to each of your non-Azure AD user properties to form the Azure AD property selected in step 1.</span></span>

<span data-ttu-id="f1dab-147">在 [公式] 方塊中，" {0} " 對應于正則運算式的輸出，該正則運算式套用到您選取的 *第一個* 非 Azure AD 屬性。</span><span class="sxs-lookup"><span data-stu-id="f1dab-147">In the formula box, "{0}" corresponds to the output of the regular expression applied to the *first* non-Azure AD property you selected.</span></span> <span data-ttu-id="f1dab-148">" {1} " 對應于正則運算式的輸出，此正則運算式套用到您選取的 *第二個* 非 Azure AD 屬性。</span><span class="sxs-lookup"><span data-stu-id="f1dab-148">"{1}" corresponds to the output of the regular expression applied to the *second* non-Azure AD property you selected.</span></span> <span data-ttu-id="f1dab-149">" {2} " 對應于套用至 *第三個* 非 Azure AD 屬性等正則運算式的輸出。</span><span class="sxs-lookup"><span data-stu-id="f1dab-149">"{2}" corresponds to the output of the regular expression applied to the *third* non-Azure AD property, and so on.</span></span>  

<span data-ttu-id="f1dab-150">以下是一些具有範例正則運算式輸出和公式輸出的公式範例：</span><span class="sxs-lookup"><span data-stu-id="f1dab-150">Below are some examples of formulas with sample regular expression outputs and formula outputs:</span></span> 

| <span data-ttu-id="f1dab-151">範例公式</span><span class="sxs-lookup"><span data-stu-id="f1dab-151">Sample formula</span></span>                  | <span data-ttu-id="f1dab-152">{0}範例使用者的值</span><span class="sxs-lookup"><span data-stu-id="f1dab-152">Value of {0} on sample user</span></span>                 | <span data-ttu-id="f1dab-153">{1}範例使用者的值</span><span class="sxs-lookup"><span data-stu-id="f1dab-153">Value of {1} on sample user</span></span>           | <span data-ttu-id="f1dab-154">公式的輸出</span><span class="sxs-lookup"><span data-stu-id="f1dab-154">Output of formula</span></span>                  |
| :------------------- | :------------------- |:---------------|:---------------|
| <span data-ttu-id="f1dab-155">{0}.{1}@contoso .com</span><span class="sxs-lookup"><span data-stu-id="f1dab-155">{0}.{1}@contoso.com</span></span>  | <span data-ttu-id="f1dab-156">firstname</span><span class="sxs-lookup"><span data-stu-id="f1dab-156">firstname</span></span> | <span data-ttu-id="f1dab-157">姓氏</span><span class="sxs-lookup"><span data-stu-id="f1dab-157">lastname</span></span> |<span data-ttu-id="f1dab-158">firstname.lastname@contoso.com</span><span class="sxs-lookup"><span data-stu-id="f1dab-158">firstname.lastname@contoso.com</span></span>
| <span data-ttu-id="f1dab-159">{0}@domain .com</span><span class="sxs-lookup"><span data-stu-id="f1dab-159">{0}@domain.com</span></span>                 | <span data-ttu-id="f1dab-160">userid</span><span class="sxs-lookup"><span data-stu-id="f1dab-160">userid</span></span>                 |             |<span data-ttu-id="f1dab-161">userid@domain.com</span><span class="sxs-lookup"><span data-stu-id="f1dab-161">userid@domain.com</span></span>

<span data-ttu-id="f1dab-162">在您提供公式後，您可以選擇性地按一下 [ **預覽** ]，以查看資料來源中5個隨機使用者的預覽，並套用各自的使用者對應。</span><span class="sxs-lookup"><span data-stu-id="f1dab-162">After you provide your formula, you can optionally click **Preview** to see a preview of 5 random users from your data source with their respective user mappings applied.</span></span> <span data-ttu-id="f1dab-163">預覽的輸出包含在步驟2中為該使用者所選取的非 Azure AD 使用者屬性值，以及在步驟3中為該使用者提供的最後一個公式的輸出。</span><span class="sxs-lookup"><span data-stu-id="f1dab-163">The output of the preview includes the value of the non-Azure AD user properties selected in step 2 for those users and the output of the final formula provided in step 3 for that user.</span></span> <span data-ttu-id="f1dab-164">此外，它也會指出是否可以透過 "Success" 或 "Failed" 圖示，將公式的輸出解析為您租使用者中的 Azure AD 使用者。</span><span class="sxs-lookup"><span data-stu-id="f1dab-164">It also indicates whether the output of the formula could be resolved to an Azure AD user in your tenant via a "Success" or "Failed" icon.</span></span>  

>[!NOTE]
><span data-ttu-id="f1dab-165">按一下 [ **預覽**] 之後，如果有一或多個使用者對應的「失敗」狀態，您仍然可以繼續建立連接。</span><span class="sxs-lookup"><span data-stu-id="f1dab-165">You can still proceed with creating your connection if one or more user mappings have a "Failed" status after you click **Preview**.</span></span> <span data-ttu-id="f1dab-166">預覽會顯示5個隨機使用者，以及其從您的資料來源對應的映射。</span><span class="sxs-lookup"><span data-stu-id="f1dab-166">The preview shows 5 random users and their mappings from your data source.</span></span> <span data-ttu-id="f1dab-167">如果您提供的對應未對應所有使用者，您可能會遇到此案例。</span><span class="sxs-lookup"><span data-stu-id="f1dab-167">If the mapping you provide does not map all users, you may experience this case.</span></span>

## <a name="sample-non-azure-ad-mapping"></a><span data-ttu-id="f1dab-168">非 Azure AD 對應範例</span><span class="sxs-lookup"><span data-stu-id="f1dab-168">Sample non-Azure AD mapping</span></span>

<span data-ttu-id="f1dab-169">請參閱下方的快照，以取得非 Azure AD 的範例對應。</span><span class="sxs-lookup"><span data-stu-id="f1dab-169">See the snapshot below for a sample non-Azure AD mapping.</span></span>

![如何填寫非 Azure AD 對應頁面的範例快照](media/non-aad-mapping.png)

## <a name="limitations"></a><span data-ttu-id="f1dab-171">限制</span><span class="sxs-lookup"><span data-stu-id="f1dab-171">Limitations</span></span>  

- <span data-ttu-id="f1dab-172">所有使用者只支援一個對應。</span><span class="sxs-lookup"><span data-stu-id="f1dab-172">Only one mapping is supported for all users.</span></span> <span data-ttu-id="f1dab-173">不支援條件式對應。</span><span class="sxs-lookup"><span data-stu-id="f1dab-173">Conditional mappings are not supported.</span></span>  

- <span data-ttu-id="f1dab-174">發佈連線後，就無法變更對應。</span><span class="sxs-lookup"><span data-stu-id="f1dab-174">You cannot change your mapping once the connection is published.</span></span>  

- <span data-ttu-id="f1dab-175">目前只有對非 AAD 使用者屬性的 RegEx 型運算式支援轉換。</span><span class="sxs-lookup"><span data-stu-id="f1dab-175">Only regex-based expressions against the non-AAD user properties are currently supported for the transformation.</span></span>

- <span data-ttu-id="f1dab-176">只有3個 Azure AD 身分識別您可以選擇對應 (UPN、Azure AD ID 及 AD SID) 。</span><span class="sxs-lookup"><span data-stu-id="f1dab-176">There are only 3 Azure AD identities you can choose to map to (UPN, Azure AD ID, and AD SID).</span></span>