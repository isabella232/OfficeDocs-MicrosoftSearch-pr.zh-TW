---
title: 對應 AAD 身分識別
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
ROBOTS: NOINDEX, NOFOLLOW
description: 如何對應 AAD 身分識別的步驟
ms.openlocfilehash: e373302314e3044f6bd6b874a341c8a1ada77556
ms.sourcegitcommit: 77ec27736f3c8434b2ac47e10897ac2606ee8a03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/11/2020
ms.locfileid: "48992864"
---
# <a name="map-your-azure-ad-identities"></a><span data-ttu-id="e06d9-103">對應 Azure AD 身分識別</span><span class="sxs-lookup"><span data-stu-id="e06d9-103">Map your Azure AD Identities</span></span>  

<span data-ttu-id="e06d9-104">本文將引導您完成將 Azure AD 身分識別對應至資料來源的唯一識別碼的步驟 (非 Azure AD 身分識別) ，這樣，您的存取控制清單中的人員) 與非 Azure AD 身分識別的存取控制 (清單中的人員，便可查看限制範圍的連接器搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="e06d9-104">This article walks you through the steps of mapping your Azure AD identities to a unique identifier for your data source (non-Azure AD identity) so that people in your Access Control List (ACL) with non-Azure AD identities can see connector search results scoped to them.</span></span>

<span data-ttu-id="e06d9-105">這些步驟只會與使用「存取此資料來源的人」和「AAD」的「搜尋」許可權的「搜尋」許可權設定為 Microsoft 的 [Salesforce](salesforce-connector.md) 連接器有關的搜尋系統管理員相關。</span><span class="sxs-lookup"><span data-stu-id="e06d9-105">These steps are only relevant to search administrators who are setting up a [Salesforce](salesforce-connector.md) connector by Microsoft with search permissions for "Only people with access to this data source" and identity type "AAD."</span></span> <span data-ttu-id="e06d9-106">下列步驟會引導您如何將 Azure AD 使用者屬性對應至使用者的 **同盟 IDs** 。</span><span class="sxs-lookup"><span data-stu-id="e06d9-106">The following steps walk you through how to map your Azure AD user properties to your users' **Federation IDs**.</span></span>

>[!NOTE]
><span data-ttu-id="e06d9-107">如果您是在 [搜尋許可權] 畫面上設定 [Salesforce 連接器](salesforce-connector.md) 並 **只選取存取此資料來源的人員** 和身分識別類型 **非 AAD** ，請參閱 [對應您的非 azure ad](map-non-aad.md) 身分識別文章，以取得如何對應非 azure ad 身分識別的步驟。</span><span class="sxs-lookup"><span data-stu-id="e06d9-107">If you are setting up a [Salesforce connector](salesforce-connector.md) and select **Only people with access to this data source** and identity type **non-AAD** on the search permissions screen, refer to the [Map your non-Azure AD Identities](map-non-aad.md) article for steps on how to map non-Azure AD identities.</span></span>  

## <a name="steps-for-mapping-your-azure-ad-properties"></a><span data-ttu-id="e06d9-108">對應 Azure AD 屬性的步驟</span><span class="sxs-lookup"><span data-stu-id="e06d9-108">Steps for mapping your Azure AD properties</span></span>

### <a name="1-select-azure-ad-user-properties-to-map"></a><span data-ttu-id="e06d9-109">1. 選取要對應的 Azure AD 使用者屬性</span><span class="sxs-lookup"><span data-stu-id="e06d9-109">1. Select Azure AD user properties to map</span></span>

<span data-ttu-id="e06d9-110">您可以選取您要對應至同盟識別碼的 Azure AD 屬性。</span><span class="sxs-lookup"><span data-stu-id="e06d9-110">You can select the Azure AD properties you need to map to the Federation ID.</span></span>

<span data-ttu-id="e06d9-111">您可以從下拉式清單中選取 Azure AD 使用者屬性。</span><span class="sxs-lookup"><span data-stu-id="e06d9-111">You can select an Azure AD user property from the dropdown.</span></span> <span data-ttu-id="e06d9-112">您也可以新增您想要的 Azure AD 使用者屬性。若要建立組織的同盟識別碼對應，您也可以像您所需的那樣新增這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e06d9-112">You can also add as many Azure AD user properties as you would like if these properties are necessary to create the Federation ID mapping for your organization.</span></span>

### <a name="2-create-formula-to-complete-mapping"></a><span data-ttu-id="e06d9-113">2. 建立完成對應的公式</span><span class="sxs-lookup"><span data-stu-id="e06d9-113">2. Create formula to complete mapping</span></span>

<span data-ttu-id="e06d9-114">您可以組合 Azure AD 使用者屬性的值，以形成唯一的同盟識別碼。</span><span class="sxs-lookup"><span data-stu-id="e06d9-114">You can combine the values of the Azure AD user properties to form the unique Federation ID.</span></span>

<span data-ttu-id="e06d9-115">在 [公式] 方塊中，" {0} " 會對應至您所選取的 *第一個* Azure AD 屬性。</span><span class="sxs-lookup"><span data-stu-id="e06d9-115">In the formula box, "{0}" corresponds to the *first* Azure AD property you selected.</span></span> <span data-ttu-id="e06d9-116">" {1} " 對應于您選取的 *第二個* Azure AD 屬性。</span><span class="sxs-lookup"><span data-stu-id="e06d9-116">"{1}" corresponds to the *second* Azure AD property you selected.</span></span> <span data-ttu-id="e06d9-117">" {2} " 會對應至 *協力廠商* Azure AD 屬性等等。</span><span class="sxs-lookup"><span data-stu-id="e06d9-117">"{2}" corresponds to the *third* Azure AD property, and so on.</span></span>  

<span data-ttu-id="e06d9-118">以下是一些具有範例正則運算式輸出和公式輸出的公式範例：</span><span class="sxs-lookup"><span data-stu-id="e06d9-118">Below are some examples of formulas with sample regular expression outputs and formula outputs:</span></span>

| <span data-ttu-id="e06d9-119">範例公式</span><span class="sxs-lookup"><span data-stu-id="e06d9-119">Sample formula</span></span>                  | <span data-ttu-id="e06d9-120">範例使用者的屬性值 {0}</span><span class="sxs-lookup"><span data-stu-id="e06d9-120">Value of property {0} for a sample user</span></span>                 | <span data-ttu-id="e06d9-121">範例使用者的屬性值 {1}</span><span class="sxs-lookup"><span data-stu-id="e06d9-121">Value of property {1} for a sample user</span></span>           | <span data-ttu-id="e06d9-122">公式的輸出</span><span class="sxs-lookup"><span data-stu-id="e06d9-122">Output of formula</span></span>                  |
| :------------------- | :------------------- |:---------------|:---------------|
| <span data-ttu-id="e06d9-123">{0}.{1}@contoso .com</span><span class="sxs-lookup"><span data-stu-id="e06d9-123">{0}.{1}@contoso.com</span></span>  | <span data-ttu-id="e06d9-124">firstname</span><span class="sxs-lookup"><span data-stu-id="e06d9-124">firstname</span></span> | <span data-ttu-id="e06d9-125">姓氏</span><span class="sxs-lookup"><span data-stu-id="e06d9-125">lastname</span></span> |<span data-ttu-id="e06d9-126">firstname.lastname@contoso.com</span><span class="sxs-lookup"><span data-stu-id="e06d9-126">firstname.lastname@contoso.com</span></span>
| <span data-ttu-id="e06d9-127">{0}@domain .com</span><span class="sxs-lookup"><span data-stu-id="e06d9-127">{0}@domain.com</span></span>                 | <span data-ttu-id="e06d9-128">userid</span><span class="sxs-lookup"><span data-stu-id="e06d9-128">userid</span></span>                 |             |<span data-ttu-id="e06d9-129">userid@domain.com</span><span class="sxs-lookup"><span data-stu-id="e06d9-129">userid@domain.com</span></span>

<span data-ttu-id="e06d9-130">在您提供公式後，您可以選擇性地按一下 [ **預覽** ]，以查看資料來源中5個隨機使用者的預覽，並套用各自的使用者對應。</span><span class="sxs-lookup"><span data-stu-id="e06d9-130">After you provide your formula, you can optionally click **Preview** to see a preview of 5 random users from your data source with their respective user mappings applied.</span></span> <span data-ttu-id="e06d9-131">預覽的輸出會包含步驟1中為該使用者選取的 Azure AD 使用者屬性值，以及在步驟2中為該使用者提供之最後一個公式的輸出。</span><span class="sxs-lookup"><span data-stu-id="e06d9-131">The output of the preview includes the value of the Azure AD user properties selected in step 1 for those users and the output of the final formula provided in step 2 for that user.</span></span> <span data-ttu-id="e06d9-132">此外，它也會指出是否可以透過 "Success" 或 "Failed" 圖示，將公式的輸出解析為您租使用者中的 Azure AD 使用者。</span><span class="sxs-lookup"><span data-stu-id="e06d9-132">It also indicates whether the output of the formula could be resolved to an Azure AD user in your tenant via a "Success" or "Failed" icon.</span></span>  

>[!NOTE]
><span data-ttu-id="e06d9-133">按一下 [ **預覽** ] 之後，如果有一或多個使用者對應的「失敗」狀態，您仍然可以繼續建立連接。</span><span class="sxs-lookup"><span data-stu-id="e06d9-133">You can still proceed with creating your connection if one or more user mappings have a "Failed" status after you click **Preview**.</span></span> <span data-ttu-id="e06d9-134">預覽會顯示5個隨機使用者，以及其從您的資料來源對應的映射。</span><span class="sxs-lookup"><span data-stu-id="e06d9-134">The preview shows 5 random users and their mappings from your data source.</span></span> <span data-ttu-id="e06d9-135">如果您提供的對應未對應所有使用者，您可能會遇到此案例。</span><span class="sxs-lookup"><span data-stu-id="e06d9-135">If the mapping you provide does not map all users, you may experience this case.</span></span>

## <a name="sample-azure-ad-mapping"></a><span data-ttu-id="e06d9-136">Azure AD 對應範例</span><span class="sxs-lookup"><span data-stu-id="e06d9-136">Sample Azure AD mapping</span></span>

<span data-ttu-id="e06d9-137">如需 Azure AD 對應範例，請參閱下列快照。</span><span class="sxs-lookup"><span data-stu-id="e06d9-137">See the snapshot below for a sample Azure AD mapping.</span></span>

![如何填滿 Azure AD 對應頁面的範例快照](media/aad-mapping.png)

## <a name="limitations"></a><span data-ttu-id="e06d9-139">限制</span><span class="sxs-lookup"><span data-stu-id="e06d9-139">Limitations</span></span>  

- <span data-ttu-id="e06d9-140">所有使用者只支援一個對應。</span><span class="sxs-lookup"><span data-stu-id="e06d9-140">Only one mapping is supported for all users.</span></span> <span data-ttu-id="e06d9-141">不支援條件式對應。</span><span class="sxs-lookup"><span data-stu-id="e06d9-141">Conditional mappings are not supported.</span></span>  

- <span data-ttu-id="e06d9-142">發佈連線後，就無法變更對應。</span><span class="sxs-lookup"><span data-stu-id="e06d9-142">You cannot change your mapping once the connection is published.</span></span>  

- <span data-ttu-id="e06d9-143">Azure ad 使用者屬性不支援以 Regex 為基礎的運算式，Azure AD to Federation ID 轉換。</span><span class="sxs-lookup"><span data-stu-id="e06d9-143">Regex-based expressions against the Azure AD user properties are not supported for the Azure AD to Federation ID transformation.</span></span>