---
title: 管理自訂篩選
ms.author: rodhb
author: rodhb
manager: jeffkizn
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 管理自訂篩選
ms.openlocfilehash: 75273035a7825683f626464df7bbc8e294b41b6f
ms.sourcegitcommit: 59435698bece013ae64ca2a68c43455ca10e3fdf
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/05/2020
ms.locfileid: "48927378"
---
# <a name="create-custom-filters"></a>建立自訂篩選

您可以建立篩選，以自訂使用者在 Microsoft [SharePoint](https://sharepoint.com/)、microsoft [Office](https://office.com)和 microsoft search in [Bing](https://bing.com)中搜尋時所看到的搜尋體驗。 篩選可讓使用者從其搜尋查詢快速縮小結果的集合。

自訂的篩選可以在以 connection 屬性為基礎的垂直內部建立。 例如，您可以在自訂垂直內為 ServiceNow 連接建立 **已發佈的 On** filter。

## <a name="things-to-consider"></a>考慮事項

1. 若要在線上內容來源上建立自訂篩選，還會提供一些其他功能：
- 您也可以在 connector 來源屬性的別名上建立篩選
- 如果您的垂直具有多個連線，您可以在這些連線建立通用篩選。 若要完成此工作，您可以在通用別名上建立篩選，而這些別名來源屬性會在不同的連線。 例如，您可以建立別名 **，使其** 跨越 ServiceNow & Jira 連線，如下所示：

| 連線 | 屬性	 | 別名 |
| --- | --- | --- |
| 服務現在 | 擁有者 | 作者 |
| Jira | 發行者 | 作者 |

2. 篩選器存在於垂直範圍內。 因此  
- 如果篩選是以組織層級的垂直方式建立，則篩選只會顯示在組織層級
- 如果篩選是以位於網站層級的垂直方式建立，則篩選只會顯示在網站層級。

## <a name="steps-to-create-custom-filter"></a>建立自訂篩選的步驟

### <a name="create-filter-in-organizational-level-vertical"></a>在組織層級中建立篩選：

若要在 Microsoft 搜尋上建立篩選，請遵循下列步驟：

1. 在 Microsoft 365 系統管理中心中，移至 [ [縱向](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/verticals) ] 頁面。
2. 建立/編輯您要建立篩選的垂直方向
3. 流覽至嚮導中的 [篩選器] 步驟
4. 按一下 [新增篩選] 並在新增篩選後開始，您可以查看並儲存該垂直。

## <a name="known-limitations"></a>已知限制

1. 您目前只能在 String & Date type managed 屬性上建立篩選。
2. 您無法建立分級篩選

## <a name="resources"></a>資源

[自訂搜尋結果頁面](customize-search-page.md)