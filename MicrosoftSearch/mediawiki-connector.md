---
title: Microsoft 搜尋的 MediaWiki 連接器
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
description: 設定 Microsoft 搜尋的 MediaWiki 連接器
ms.openlocfilehash: b9c8d80ae5cb8e86b0f6341bfe9231b709569e7a
ms.sourcegitcommit: 988c37610e71f9784b486660400aecaa7bed40b0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "47423016"
---
# <a name="mediawiki-connector"></a>MediaWiki 連接器

透過 MediaWiki 連接器，您的組織可以從使用 MediaWiki 軟體所建立的 wiki 探索和編制資料。 此連接器會將指定的內容索引至 Microsoft 搜尋中，並支援定期編目，使索引保持在最新狀態。

本文適用于 Microsoft 365 系統管理員或任何設定、執行及監視 MediaWiki 連接器的人員。 它說明如何設定連接器和連接器功能、限制及疑難排解技術。

## <a name="connect-to-a-data-source"></a>連接到資料來源

輸入您的 MediaWiki URL 和認證以驗證連線。 您將需要下列資訊： **租使用者識別碼**、 **資源識別碼**、 **用戶端識別碼**和 **用戶端密碼**。

## <a name="manage-the-search-schema"></a>管理搜尋結構描述

成功連接後，請設定搜尋架構對應。 您可以選擇哪些屬性可供**查詢**、可搜尋及可**供****檢索**。

## <a name="manage-search-permissions"></a>管理搜尋許可權

MediaWiki 連接器只支援 **所有人都**能看見的搜尋許可權。 已編制索引的資料會顯示在搜尋結果中，並對組織中的所有使用者顯示。

## <a name="set-the-refresh-schedule"></a>設定重新整理排程

此排程會重新整理已編制索引的資料，因此 wiki 的變更會反映在 Microsoft 搜尋中。 所有新頁面、刪除的頁面、頁面內容或中繼資料變更都會出現在搜尋結果中指定的重新整理間隔之後。 編目時間取決於 wiki 的大小。 目前的連接器會在每分鐘50頁面的周圍進行編目。

## <a name="limitations"></a>限制

MediaWiki 連接器在預覽版本中有下列限制：

* 僅支援雲端型 wiki。
* 使用 Azure Active Directory 或 Azure 驗證，僅支援 Basic 或 OAuth 2.0。
* 不支援索引的命名空間選取。 僅索引 **主要**、 **類別**和檔案 **命名空間** 。
* 不支援 (ACLs) 的存取控制清單。 因此，組織中的所有使用者都能看到索引頁面。
