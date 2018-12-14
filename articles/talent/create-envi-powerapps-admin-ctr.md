---
title: "无法在 PowerApps 管理中心创建环境"
description: "本主题说明如果管理员无法在 Microsoft PowerApps 管理中心创建环境该做什么。"
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 6f9b7ceef6895b295e6ae5a50d8ac7970497efe5
ms.contentlocale: zh-cn
ms.lasthandoff: 12/04/2018

---

# <a name="cant-create-an-environment-in-the-powerapps-admin-center"></a><span data-ttu-id="30c74-103">无法在 PowerApps 管理中心创建环境</span><span class="sxs-lookup"><span data-stu-id="30c74-103">Can't create an environment in the PowerApps Admin center</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="30c74-104">**发货**</span><span class="sxs-lookup"><span data-stu-id="30c74-104">**Issue**</span></span>

- <span data-ttu-id="30c74-105">租户/环境管理员无法在 Microsoft PowerApps 管理中心创建环境。</span><span class="sxs-lookup"><span data-stu-id="30c74-105">The tenant/environment admin can't create an environment in the Microsoft PowerApps Admin center.</span></span>
- <span data-ttu-id="30c74-106">授予用户执行环境创建步骤权限的许可证未直接分配给执行该步骤的用户。</span><span class="sxs-lookup"><span data-stu-id="30c74-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="30c74-107">**解决方案**</span><span class="sxs-lookup"><span data-stu-id="30c74-107">**Solution**</span></span>

<span data-ttu-id="30c74-108">确保租户管理员已将有效的 PowerApps P2 许可证直接分配给将执行环境创建步骤的用户。</span><span class="sxs-lookup"><span data-stu-id="30c74-108">Make sure that the tenant admin has assigned a valid PowerApps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="30c74-109">这里是提供该权限的 Microsoft Dynamics 服务计划。</span><span class="sxs-lookup"><span data-stu-id="30c74-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="30c74-110">整个产品库存单位 (SKU)</span><span class="sxs-lookup"><span data-stu-id="30c74-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="30c74-111">PowerApps P2 服务计划</span><span class="sxs-lookup"><span data-stu-id="30c74-111">PowerApps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="30c74-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="30c74-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="30c74-113">PowerApps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="30c74-113">PowerApps for Dynamics 365</span></span> |
| <span data-ttu-id="30c74-114">Microsoft Dynamics 365 计划 Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="30c74-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="30c74-115">PowerApps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="30c74-115">PowerApps for Dynamics 365</span></span> |

<span data-ttu-id="30c74-116">请注意，各个 Microsoft Office SKU 也提供权限，以及独立的 PowerApps 计划 2 SKU。</span><span class="sxs-lookup"><span data-stu-id="30c74-116">Note that various Microsoft Office SKUs also provide the right, together with standalone PowerApps Plan 2 SKUs.</span></span> <span data-ttu-id="30c74-117">重点是这些 SKU 中的一个必须存在。</span><span class="sxs-lookup"><span data-stu-id="30c74-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="30c74-118">转到 [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments)。</span><span class="sxs-lookup"><span data-stu-id="30c74-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="30c74-119">按照[配置 Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent) 中的说明创建环境。</span><span class="sxs-lookup"><span data-stu-id="30c74-119">Create the environments by following the instructions in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

