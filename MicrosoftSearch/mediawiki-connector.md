---
title: Microsoft Search MediaWiki 連接器
ms.author: v-pamcn
author: monaray
manager: mnirkhe
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 設定 Microsoft Search MediaWiki 連接器
ms.openlocfilehash: 2aa0ef494aa42b1a7364ec68f6532dec737b9c25
ms.sourcegitcommit: 21361af7c244ffd6ff8689fd0ff0daa359bf4129
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/14/2019
ms.locfileid: "38626961"
---
# <a name="mediawiki-connector"></a>MediaWiki 連接器

MediaWiki 連接器後，您的組織可以探索與索引資料從 wiki 建立使用 MediaWiki 軟體。 此連接器索引指定成 Microsoft Search 和支援定期編目保持最新狀態索引內容。

本文適用於 Microsoft 365 系統管理員或人設定、 執行，並監視 MediaWiki 連接器。 本文說明如何設定連接器，連接器功能、 限制和疑難排解技巧。

## <a name="connect-to-a-data-source"></a>連線至資料來源
輸入您 MediaWiki URL 與認證來驗證連線。 您將需要下列資訊：**租用戶識別碼**、**資源識別碼**、**用戶端識別碼**和**用戶端密碼**。

## <a name="manage-the-search-schema"></a>管理搜尋結構描述
成功連線之後，設定的搜尋結構描述對應。 您可以選擇要讓屬性**設為可查詢**、**可搜尋**，並**可擷取**。

## <a name="manage-search-permissions"></a>管理搜尋的權限
MediaWiki 連接器僅支援搜尋權限以**供其他人**。 已編製索引的資料會出現在搜尋結果，並在組織中的所有使用者都都能看到。

## <a name="set-the-refresh-schedule"></a>設定重新整理排程 
此排程重新整理已編製索引的資料，以便 wiki 的變更會反映在 Microsoft Search。 所有新的頁面、 刪除的頁面、 頁面內容或中繼資料變更指定的重新整理間隔之後出現在搜尋結果。 編目時間 」 是 wiki 的大小而定。 目前連接器會在大約 50 頁面每分鐘編目。

## <a name="limitations"></a>限制 
MediaWiki 連接器預覽版本中有這些限制：
* 支援僅雲端式 wiki。
* 支援僅 [基本] 或 [使用 Azure Active Directory 或 Azure 驗證的 OAuth 2.0。
* 不支援索引編製的命名空間的選取範圍。 編製索引只有**主要**、**類別**及**檔案**的命名空間。
* 不支援存取控制清單 (Acl)。 因此，已編製索引的頁面都可以看見組織中的所有使用者。
