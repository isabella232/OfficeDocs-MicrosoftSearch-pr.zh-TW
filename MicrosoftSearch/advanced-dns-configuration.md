---
title: 進階的 DNS 設定
ms.author: dawholl
author: dawholl
manager: kellis
ms.date: 12/19/2018
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MOE150
- MED150
ms.assetid: 47eedbb9-6da9-47e0-aac5-078d34a7fd8f
description: 確保順利登入經驗使用者藉由設定使用 CNAME DNS 伺服器
ms.openlocfilehash: f08fc4c29c4c4356a1616faab67fdebdd6c85839
ms.sourcegitcommit: bf52cc63b75f2e0324a716fe65da47702956b722
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/18/2019
ms.locfileid: "29380065"
---
# <a name="advanced-dns-configuration"></a>進階的 DNS 設定

為了確保 Bing 可以一律識別組織內的使用者與成功他們登入其工作或學校帳戶，設定您的內部 DNS 伺服器或 proxy 伺服器來解析從`www.bing.com`至`ms.bing.com`。若要這樣做，建立 DNS 項目`www.bing.com`是針對 CNAME `ms.bing.com`。
  
****

|**名稱**|**類型**|**值**|
|:-----|:-----|:-----|
|`www.bing.com`  <br/> |CNAME  <br/> |`ms.bing.com`  <br/> |
   
使用 CNAME 而不是 IP 位址和 ipv6，則自 CNAME 會繼續運作如果 IP 位址變更。進行這項 DNS 變更後，結果會繼續要顯示給使用者像它們來自`www.bing.com`。 
  
這不需要其他設定用戶端機器上的並為使用者提供一致的體驗。當他們移至`bing.com`、 他們將會自動登入多一致，以及如果他們無法簽署自動，他們將會提示您這麼做。
