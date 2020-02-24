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
ms.openlocfilehash: f4c75706183a3d6c961852395e464d46ba3ec1f2
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008190"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="c0766-103">无法在 Power Apps 管理中心内创建环境</span><span class="sxs-lookup"><span data-stu-id="c0766-103">Can't create an environment in the Power Apps Admin center</span></span>

<span data-ttu-id="c0766-104">**发货**</span><span class="sxs-lookup"><span data-stu-id="c0766-104">**Issue**</span></span>

- <span data-ttu-id="c0766-105">租户/环境管理员无法在 Microsoft Power Apps 管理中心创建环境。</span><span class="sxs-lookup"><span data-stu-id="c0766-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="c0766-106">授予用户执行环境创建步骤权限的许可证未直接分配给执行该步骤的用户。</span><span class="sxs-lookup"><span data-stu-id="c0766-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="c0766-107">**解决方案**</span><span class="sxs-lookup"><span data-stu-id="c0766-107">**Solution**</span></span>

<span data-ttu-id="c0766-108">确保租户管理员已将有效的 Power Apps P2 许可证直接分配给将执行环境创建步骤的用户。</span><span class="sxs-lookup"><span data-stu-id="c0766-108">Make sure that the tenant admin has assigned a valid Power Apps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="c0766-109">这里是提供该权限的 Microsoft Dynamics 服务计划。</span><span class="sxs-lookup"><span data-stu-id="c0766-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="c0766-110">整个产品库存单位 (SKU)</span><span class="sxs-lookup"><span data-stu-id="c0766-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="c0766-111">Power Apps P2 服务计划</span><span class="sxs-lookup"><span data-stu-id="c0766-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="c0766-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="c0766-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="c0766-113">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="c0766-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="c0766-114">Microsoft Dynamics 365 计划 Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="c0766-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="c0766-115">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="c0766-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="c0766-116">请注意，各个 Microsoft Office SKU 也提供权限，以及独立的 Power Apps 计划 2 SKU。</span><span class="sxs-lookup"><span data-stu-id="c0766-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="c0766-117">重点是这些 SKU 中的一个必须存在。</span><span class="sxs-lookup"><span data-stu-id="c0766-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="c0766-118">转到 [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments)。</span><span class="sxs-lookup"><span data-stu-id="c0766-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="c0766-119">按照[配置 Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) 中的说明创建环境。</span><span class="sxs-lookup"><span data-stu-id="c0766-119">Create the environments by following the instructions in [Provision Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
