---
title: 无法在 Power Apps 管理中心内创建环境
description: 本文说明如果管理员无法在 Microsoft Power Apps 管理中心创建环境该做什么。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 68e6dbcbbc9811211570e968047f5faa8a2c8bd0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417435"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="3d4d2-103">无法在 Power Apps 管理中心内创建环境</span><span class="sxs-lookup"><span data-stu-id="3d4d2-103">Can't create an environment in the Power Apps Admin center</span></span>

<span data-ttu-id="3d4d2-104">**发货**</span><span class="sxs-lookup"><span data-stu-id="3d4d2-104">**Issue**</span></span>

- <span data-ttu-id="3d4d2-105">租户/环境管理员无法在 Microsoft Power Apps 管理中心创建环境。</span><span class="sxs-lookup"><span data-stu-id="3d4d2-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="3d4d2-106">授予用户执行环境创建步骤权限的许可证未直接分配给执行该步骤的用户。</span><span class="sxs-lookup"><span data-stu-id="3d4d2-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="3d4d2-107">**解决方案**</span><span class="sxs-lookup"><span data-stu-id="3d4d2-107">**Solution**</span></span>

<span data-ttu-id="3d4d2-108">确保租户管理员已将有效的 Power Apps P2 许可证直接分配给将执行环境创建步骤的用户。</span><span class="sxs-lookup"><span data-stu-id="3d4d2-108">Make sure that the tenant admin has assigned a valid Power Apps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="3d4d2-109">这里是提供该权限的 Microsoft Dynamics 服务计划。</span><span class="sxs-lookup"><span data-stu-id="3d4d2-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="3d4d2-110">整个产品库存单位 (SKU)</span><span class="sxs-lookup"><span data-stu-id="3d4d2-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="3d4d2-111">Power Apps P2 服务计划</span><span class="sxs-lookup"><span data-stu-id="3d4d2-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="3d4d2-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="3d4d2-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="3d4d2-113">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="3d4d2-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="3d4d2-114">Microsoft Dynamics 365 计划 Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="3d4d2-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="3d4d2-115">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="3d4d2-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="3d4d2-116">请注意，各个 Microsoft Office SKU 也提供权限，以及独立的 Power Apps 计划 2 SKU。</span><span class="sxs-lookup"><span data-stu-id="3d4d2-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="3d4d2-117">重点是这些 SKU 中的一个必须存在。</span><span class="sxs-lookup"><span data-stu-id="3d4d2-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="3d4d2-118">转到 [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments)。</span><span class="sxs-lookup"><span data-stu-id="3d4d2-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="3d4d2-119">按照[配置 Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) 中的说明创建环境。</span><span class="sxs-lookup"><span data-stu-id="3d4d2-119">Create the environments by following the instructions in [Provision Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
