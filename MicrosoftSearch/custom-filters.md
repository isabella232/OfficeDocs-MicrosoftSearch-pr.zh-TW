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
ms.openlocfilehash: 339c7e96a00860a044a4e1af7382932f8e440e01b8b6d12445c24c1ea9b8cad0
ms.sourcegitcommit: 71ac2a38971ca4452d1bddfc773ff8f45e1ffd77
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/06/2021
ms.locfileid: "54533126"
---
# <a name="manage-custom-filters"></a>管理自訂篩選

您可以使用篩選自訂 Microsoft 搜尋體驗。 篩選可讓使用者從搜尋查詢快速精煉結果集。

自訂的篩選可以在以 connection 屬性為基礎的垂直內部建立。 例如，您可以在垂直方向的 ServiceNow 連接 **上建立已發佈的 On** filter。

## <a name="create-a-filter-in-an-organizational-level-vertical"></a>在組織層級中建立篩選

若要在 Microsoft 搜尋上建立篩選，請遵循下列步驟：

1. 在 Microsoft 365 系統管理中心中，移至 [[縱向](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/verticals)]。
1. 建立/編輯您要建立篩選的垂直方向
1. 流覽至嚮導中的 [篩選器] 步驟
1. 按一下 [新增篩選] 並開始
1. 新增篩選後，您可以檢查並儲存垂直。

## <a name="things-to-consider"></a>考慮事項

1. 線上內容上存在其他篩選功能。

    - 您也可以在 connector 來源屬性的別名上建立篩選
    - 如果垂直具有多個連線，您可以在這些連線建立通用篩選。 若要執行此動作，您可以在通用別名上建立篩選，以在不同的連線中使用別名來源屬性。 例如，您可以建立別名 **篩選 ServiceNow** 和 Jira 連線，如下所示：

    | 連線 | 屬性	 | 別名 |
    | --- | --- | --- |
    | 服務現在 | 擁有者 | 作者 |
    | Jira | Publisher | 作者 |

1. 篩選器存在於垂直範圍內。

    - 如果篩選是以組織層級的垂直方式建立，則篩選只會顯示在組織層級
    - 如果篩選是以位於網站層級的垂直方式建立，則篩選只會顯示在網站層級。

## <a name="known-limitations"></a>已知限制

1. 您目前只能在 string & date type managed 屬性上建立篩選。
1. 您無法建立分級篩選。

## <a name="resources"></a>資源

[管理類別和結果類型](customize-search-page.md)
