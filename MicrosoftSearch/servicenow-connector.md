---
title: Microsoft Search ServiceNow 連接器
ms.author: v-pamcn
author: TrishaMc1
manager: mnirkhe
ms.date: 10/08/2019
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 設定 Microsoft Search ServiceNow 連接器
ms.openlocfilehash: b83bf04dc06ffab26a0067d15b36a99496c199a8
ms.sourcegitcommit: bfcab9d42e93addccd1e3875b41bc9cc1b6986cc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2019
ms.locfileid: "37949712"
---
# <a name="servicenow-connector"></a>ServiceNow 連接器

使用 ServiceNow 連接器，您的組織可編製索引之組織內的所有使用者都都能看見知識庫文章。 您設定的連接器和 ServiceNow 從內容索引之後，使用者可以搜尋任何 Microsoft 搜尋用戶端從這些文章。  

本文適用於 Microsoft 365 系統管理員或人設定、 執行，並監視 ServiceNow 連接器。 本文說明如何設定連接器，連接器功能、 限制和疑難排解技巧。

## <a name="connect-to-a-data-source"></a>連線至資料來源
若要連線至您 ServiceNow 資料，您需要您的組織**ServiceNow 執行個體的 URL**，這個帳戶]，和認證的用戶端識別碼和用戶端密碼的 OAuth 驗證。  

您的組織**ServiceNow 執行個體的 URL**通常看起來像**https://&lt;您組織網域>.service now.com**。 此 URL，以及您需要帳戶設定以及 ServiceNow 的連線與允許 Microsoft Search 定期更新從 ServiceNow 重新整理排程為基礎的文章。

若要驗證，並從 ServiceNow 內容同步處理，選擇兩種支援的方法之一： 
1. 基本驗證 
2. OAuth （建議使用）

> [!Note]
> 若要使用 OAuth 進行驗證，ServiceNow 系統管理員必須佈建端點 ServiceNow 執行個體，以便 Microsoft 的搜尋應用程式可以存取執行個體。 若要深入了解，請參閱 ServiceNow 文件中的[建立用戶端存取之執行個體的端點](https://docs.servicenow.com/bundle/newyork-platform-administration/page/administer/security/task/t_CreateEndpointforExternalClients.html)。

下表提供如何填寫端點建立表單的指引：

**Field** | **描述** | **建議的值**
--- | --- | ---
名稱 | 這個唯一的值會識別需要 OAuth 存取的應用程式。 | Microsoft Search
用戶端識別碼 | 唯讀屬性，自動產生唯一識別碼的應用程式。 要求存取權杖時，執行個體使用的用戶端識別碼。 | NA
用戶端密碼 | 使用此共用的密碼字串，ServiceNow 執行個體和 Microsoft Search 授權與彼此通訊。 | 藉由將此視為密碼，請遵循安全性最佳作法。
重新導向 URL | 授權伺服器重新導向至所需的回撥 URL。 | 請參閱[OAuth 回呼](https://gcs.office.com/v1.0/admin/oauth/callback)。
標誌 URL | 包含應用程式標誌的影像 URL。 | NA
作用中 | 選取核取方塊，可讓應用程式登錄作用中。 | 設定為作用中
重新整理 token 期限 | 重新整理權杖是有效的秒數。 根據預設，重新整理權杖到期 100 天 （8640000 秒為單位）。 | 31,536,000 （1 年）
存取權杖使用壽命 | 存取權杖是有效的秒數。 | 43200 （12 小時）

## <a name="set-a-sync-filter"></a>設定同步處理篩選 
使用同步處理篩選，您可以指定條件的同步處理的文章。 它就像是**Where**子句的**SQL Select**陳述式中。 例如，您可以選擇索引發佈且作用中的文章。 SyncNow 組態] 頁面上說明如何擷取與同步處理篩選設定。

## <a name="manage-the-search-schema"></a>管理搜尋結構描述
成功連線之後，設定的搜尋結構描述對應。 您可以選擇要讓屬性**設為可查詢**、**可搜尋**，並**可擷取**。

## <a name="manage-search-permissions"></a>管理搜尋的權限
ServiceNow 連接器僅支援搜尋權限以**供其他人**。 已編製索引的資料會出現在搜尋結果，並在組織中的所有使用者都都能看到。
 
## <a name="set-the-refresh-schedule"></a>設定重新整理排程 
ServiceNow 連接器支援重新整理排程適用於完整與累加編目。 我們建議您設定兩者。

完整編目排程尋找先前已同步處理至 Microsoft 搜尋索引的已刪除的文章和任何移出同步處理篩選的文章。 當您第一次連接至 ServiceNow 時，同步處理所有的知識庫文章會執行完整編目。 若要同步處理新項目，並進行更新，您要排程累加編目。

建議的預設值為一天的完整編目和四個小時的累加編目。
