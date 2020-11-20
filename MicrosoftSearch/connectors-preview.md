---
title: 連接器預覽
ms.author: monaray
author: monaray97
manager: shohara
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: 瞭解 microsoft 搜尋的 Microsoft Graph 連接器預覽。
ms.openlocfilehash: 592e108fe0333e4faf8ff2e4618f9d5216847b8a
ms.sourcegitcommit: 59cdd3f0f82b7918399bf44d27d9891076090f4f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2020
ms.locfileid: "49367665"
---
# <a name="microsoft-graph-connectors-preview-release-and-features"></a><span data-ttu-id="5cd27-103">Microsoft Graph 連接器預覽發行及功能</span><span class="sxs-lookup"><span data-stu-id="5cd27-103">Microsoft Graph connectors preview release and features</span></span>

<span data-ttu-id="5cd27-104">現在一般會提供 microsoft Graph 連接器和 Microsoft Search APIs。</span><span class="sxs-lookup"><span data-stu-id="5cd27-104">Microsoft Graph connectors and Microsoft Search APIs are now generally available.</span></span> <span data-ttu-id="5cd27-105">最初的首展將是針對目標版本設定的客戶。</span><span class="sxs-lookup"><span data-stu-id="5cd27-105">The initial rollout will be to customers configured for Targeted Release.</span></span> <span data-ttu-id="5cd27-106">完成所有租使用者的部署時，連接器內容的索引配額利用率會變成計費。</span><span class="sxs-lookup"><span data-stu-id="5cd27-106">Upon rollout completion to all tenants, index quota utilization from connectors content will become subject to billing.</span></span> <span data-ttu-id="5cd27-107">如需詳細資訊，請參閱 [授權需求和定價](licensing.md) 。</span><span class="sxs-lookup"><span data-stu-id="5cd27-107">See [Licensing requirements and pricing](licensing.md) for more information.</span></span>

## <a name="set-up-targeted-release"></a><span data-ttu-id="5cd27-108">設定目標版本</span><span class="sxs-lookup"><span data-stu-id="5cd27-108">Set up Targeted release</span></span>

<span data-ttu-id="5cd27-109">如果您想要在展示期間在租使用者中使用圖形連接器，則必須選擇已目標的版本。</span><span class="sxs-lookup"><span data-stu-id="5cd27-109">If you want to use Graph connectors in your tenant during rollout, you must opt into Targeted release.</span></span> <span data-ttu-id="5cd27-110">若要深入瞭解目標發行選項及設定方式，請參閱 [在 Office 365 中設定標準或目標發行選項](https://docs.microsoft.com/office365/admin/manage/release-options-in-office-365?view=o365-worldwide)。</span><span class="sxs-lookup"><span data-stu-id="5cd27-110">To learn more about the Targeted release option and how to set it, see [Set up the Standard or Targeted release options in Office 365](https://docs.microsoft.com/office365/admin/manage/release-options-in-office-365?view=o365-worldwide).</span></span>

## <a name="preview-features"></a><span data-ttu-id="5cd27-111">預覽功能</span><span class="sxs-lookup"><span data-stu-id="5cd27-111">Preview features</span></span>

<span data-ttu-id="5cd27-112">雖然現在一般會提供 Microsoft Graph 連接器和 Microsoft Search APIs，但有許多功能仍會保留在預覽中。</span><span class="sxs-lookup"><span data-stu-id="5cd27-112">Although Microsoft Graph connectors and Microsoft Search APIs are now generally available, there are several features that will remain in preview.</span></span>

<span data-ttu-id="5cd27-113">預覽中的連接器和功能組包括：</span><span class="sxs-lookup"><span data-stu-id="5cd27-113">The set of connectors and features in preview include:</span></span>

* [<span data-ttu-id="5cd27-114">Azure DevOps 連接器</span><span class="sxs-lookup"><span data-stu-id="5cd27-114">Azure DevOps connector</span></span>](azure-devops-connector.md)
* [<span data-ttu-id="5cd27-115">Salesforce 連接器</span><span class="sxs-lookup"><span data-stu-id="5cd27-115">Salesforce connector</span></span>](salesforce-connector.md)
* <span data-ttu-id="5cd27-116">具有使用來源 ACLs 之搜尋許可權的[ServiceNow 連接器](servicenow.md)</span><span class="sxs-lookup"><span data-stu-id="5cd27-116">[ServiceNow connector](servicenow.md) with search permissions that use source ACLs</span></span>
* [<span data-ttu-id="5cd27-117">管理結果叢集</span><span class="sxs-lookup"><span data-stu-id="5cd27-117">Manage result cluster</span></span>](result-cluster.md)