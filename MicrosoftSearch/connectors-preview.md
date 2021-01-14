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
ms.openlocfilehash: 47f7e1e417222c948f2916c70626278f9fe5b44a
ms.sourcegitcommit: 469be70ad295a5837978d75babf5243115257f77
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/13/2021
ms.locfileid: "49847508"
---
# <a name="microsoft-graph-connectors-preview-release-and-features"></a><span data-ttu-id="7b1e9-103">Microsoft Graph 連接器預覽發行及功能</span><span class="sxs-lookup"><span data-stu-id="7b1e9-103">Microsoft Graph connectors preview release and features</span></span>

<span data-ttu-id="7b1e9-104">現在一般會提供 microsoft Graph 連接器和 Microsoft Search APIs。</span><span class="sxs-lookup"><span data-stu-id="7b1e9-104">Microsoft Graph connectors and Microsoft Search APIs are now generally available.</span></span> <span data-ttu-id="7b1e9-105">最初的首展將是針對目標版本設定的客戶。</span><span class="sxs-lookup"><span data-stu-id="7b1e9-105">The initial rollout will be to customers configured for Targeted Release.</span></span> <span data-ttu-id="7b1e9-106">此首展會在2月2021結束之前開始。</span><span class="sxs-lookup"><span data-stu-id="7b1e9-106">This rollout will go on until the end of February 2021.</span></span> <span data-ttu-id="7b1e9-107">完成所有租使用者的部署時，連接器內容的索引配額利用率會變成計費。</span><span class="sxs-lookup"><span data-stu-id="7b1e9-107">Upon rollout completion to all tenants, index quota utilization from connectors content will become subject to billing.</span></span> <span data-ttu-id="7b1e9-108">如需詳細資訊，請參閱 [授權需求和定價](licensing.md) 。</span><span class="sxs-lookup"><span data-stu-id="7b1e9-108">See [Licensing requirements and pricing](licensing.md) for more information.</span></span>

## <a name="set-up-targeted-release"></a><span data-ttu-id="7b1e9-109">設定目標版本</span><span class="sxs-lookup"><span data-stu-id="7b1e9-109">Set up Targeted release</span></span>

<span data-ttu-id="7b1e9-110">如果您想要在展示期間在租使用者中使用圖形連接器，則 **必須** 選擇已目標的版本。</span><span class="sxs-lookup"><span data-stu-id="7b1e9-110">If you want to use Graph connectors in your tenant during rollout, you **must** opt into Targeted release.</span></span> <span data-ttu-id="7b1e9-111">若要深入瞭解目標發行選項及設定方式，請參閱 [在 Office 365 中設定標準或目標發行選項](https://docs.microsoft.com/office365/admin/manage/release-options-in-office-365?view=o365-worldwide&preserve-view=true)。</span><span class="sxs-lookup"><span data-stu-id="7b1e9-111">To learn more about the Targeted release option and how to set it, see [Set up the Standard or Targeted release options in Office 365](https://docs.microsoft.com/office365/admin/manage/release-options-in-office-365?view=o365-worldwide&preserve-view=true).</span></span>

## <a name="preview-features"></a><span data-ttu-id="7b1e9-112">預覽功能</span><span class="sxs-lookup"><span data-stu-id="7b1e9-112">Preview features</span></span>

<span data-ttu-id="7b1e9-113">雖然現在一般會提供 Microsoft Graph 連接器和 Microsoft Search APIs，但有許多功能仍會保留在預覽中。</span><span class="sxs-lookup"><span data-stu-id="7b1e9-113">Although Microsoft Graph connectors and Microsoft Search APIs are now generally available, there are several features that will remain in preview.</span></span>

<span data-ttu-id="7b1e9-114">預覽中的連接器和功能組包括：</span><span class="sxs-lookup"><span data-stu-id="7b1e9-114">The set of connectors and features in preview include:</span></span>

* [<span data-ttu-id="7b1e9-115">Azure DevOps 連接器</span><span class="sxs-lookup"><span data-stu-id="7b1e9-115">Azure DevOps connector</span></span>](azure-devops-connector.md)
* [<span data-ttu-id="7b1e9-116">Salesforce 連接器</span><span class="sxs-lookup"><span data-stu-id="7b1e9-116">Salesforce connector</span></span>](salesforce-connector.md)
* <span data-ttu-id="7b1e9-117">具有使用來源 ACLs 之搜尋許可權的[ServiceNow 連接器](servicenow-connector.md)</span><span class="sxs-lookup"><span data-stu-id="7b1e9-117">[ServiceNow connector](servicenow-connector.md) with search permissions that use source ACLs</span></span>
* [<span data-ttu-id="7b1e9-118">管理結果叢集</span><span class="sxs-lookup"><span data-stu-id="7b1e9-118">Manage result cluster</span></span>](result-cluster.md)