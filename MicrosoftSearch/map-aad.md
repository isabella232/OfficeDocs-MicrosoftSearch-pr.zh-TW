---
title: 對應 AAD 身分識別
ms.author: monaray
author: monaray97
manager: jameslau
ms.audience: Admin
ms.topic: article
ms.service: mssearch
ms.localizationpriority: medium
search.appverid:
- BFB160
- MET150
- MOE150
description: 如何對應 AAD 身分識別的步驟
ms.openlocfilehash: d0292d77b3a0936ed60682b8388de1bb82ac43bb
ms.sourcegitcommit: bb99601a7bd0f16dde7b271de516465d134e5bac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2021
ms.locfileid: "58973402"
---
# <a name="map-your-azure-ad-identities"></a>對應您的 Azure AD 身分識別  

本文將引導您完成將 Azure AD 身分識別對應至資料來源的唯一識別碼的步驟 (非 Azure AD 身分識別) ，這樣，您的存取控制清單中的人員) 與非 Azure AD 身分識別的存取控制 (清單中的人員，便可查看限制範圍的連接器搜尋結果。

這些步驟只會與使用「存取此資料來源的人」和「AAD」的「搜尋」許可權的「搜尋」許可權設定為 Microsoft 的 [Salesforce](salesforce-connector.md) 連接器有關的搜尋系統管理員相關。 下列步驟會引導您如何將 Azure AD 使用者屬性對應至使用者的 **同盟 IDs**。

>[!NOTE]
>如果您是在 [搜尋許可權] 畫面上設定 [Salesforce 連接器](salesforce-connector.md) 並 **只選取存取此資料來源的人員** 和身分識別類型 **非 AAD** ，請參閱 [對應您的非 azure ad](map-non-aad.md) 身分識別文章，以取得如何對應非 azure ad 身分識別的步驟。  

## <a name="steps-for-mapping-your-azure-ad-properties"></a>對應 Azure AD 屬性的步驟

### <a name="1-select-azure-ad-user-properties-to-map"></a>1. 選取要對應的 Azure AD 使用者屬性

您可以選取您要對應至同盟識別碼的 Azure AD 屬性。

您可以從下拉式清單中選取 Azure AD 使用者屬性。 您也可以新增您想要的 Azure AD 使用者屬性。若要建立組織的同盟識別碼對應，您也可以像您所需的那樣新增這些屬性。

### <a name="2-create-formula-to-complete-mapping"></a>2. 建立完成對應的公式

您可以組合 Azure AD 使用者屬性的值，以形成唯一的同盟識別碼。

在 [公式] 方塊中，" {0} " 會對應至您所選取的 *第一個* Azure AD 屬性。 " {1} " 對應于您選取的 *第二個* Azure AD 屬性。 " {2} " 會對應至 *協力廠商* Azure AD 屬性等等。  

以下是一些具有範例正則運算式輸出和公式輸出的公式範例：

| 範例公式                  | 範例使用者的屬性值 {0}                 | 範例使用者的屬性值 {1}           | 公式的輸出                  |
| :------------------- | :------------------- |:---------------|:---------------|
| {0}.{1}@contoso .com  | firstname | 姓氏 |firstname.lastname@contoso.com
| {0}@domain .com                 | userid                 |             |userid@domain.com

在您提供公式後，您可以選擇性地按一下 [ **預覽** ]，以查看資料來源中5個隨機使用者的預覽，並套用各自的使用者對應。 預覽的輸出會包含步驟1中為該使用者選取的 Azure AD 使用者屬性值，以及在步驟2中為該使用者提供之最後一個公式的輸出。 此外，它也會指出是否可以透過 "Success" 或 "Failed" 圖示，將公式的輸出解析為您租使用者中的 Azure AD 使用者。  

>[!NOTE]
>按一下 [ **預覽**] 之後，如果有一或多個使用者對應的「失敗」狀態，您仍然可以繼續建立連接。 預覽會顯示5個隨機使用者，以及其從您的資料來源對應的映射。 如果您提供的對應未對應所有使用者，您可能會遇到此案例。

## <a name="sample-azure-ad-mapping"></a>Azure AD 對應範例

如需 Azure AD 對應範例，請參閱下列快照。

![如何填滿 Azure AD 對應頁面的範例快照。](media/aad-mapping.png)

## <a name="limitations"></a>限制  

- 所有使用者只支援一個對應。 不支援條件式對應。  

- 發佈連線後，就無法變更對應。  

- Azure ad 使用者屬性不支援以 Regex 為基礎的運算式，Azure AD to Federation ID 轉換。