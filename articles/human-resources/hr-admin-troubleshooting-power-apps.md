---
title: 无法在 Power Apps 管理中心内创建环境
description: 本文说明如果管理员无法在 Microsoft Power Apps 管理中心创建环境该做什么。
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: 664c644c9b34e3489b4134040e165d26202dbd38
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111633"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="4ca7a-103">无法在 Power Apps 管理中心内创建环境</span><span class="sxs-lookup"><span data-stu-id="4ca7a-103">Can't create an environment in the Power Apps Admin center</span></span>

<span data-ttu-id="4ca7a-104">**发货**</span><span class="sxs-lookup"><span data-stu-id="4ca7a-104">**Issue**</span></span>

- <span data-ttu-id="4ca7a-105">租户/环境管理员无法在 Microsoft Power Apps 管理中心创建环境。</span><span class="sxs-lookup"><span data-stu-id="4ca7a-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="4ca7a-106">用户没有授予创建环境权限的许可证。</span><span class="sxs-lookup"><span data-stu-id="4ca7a-106">The user doesn't have a license that gives the right to create environments.</span></span>

<span data-ttu-id="4ca7a-107">**解决方案**</span><span class="sxs-lookup"><span data-stu-id="4ca7a-107">**Solution**</span></span>

<span data-ttu-id="4ca7a-108">确保租户管理员已向创建环境的用户分配了有效的 Power Apps P2 许可证。</span><span class="sxs-lookup"><span data-stu-id="4ca7a-108">Make sure the tenant admin has assigned a valid Power Apps P2 license to the user creating the environment.</span></span> <span data-ttu-id="4ca7a-109">以下 Microsoft Dynamics 服务计划提供创建环境的权限：</span><span class="sxs-lookup"><span data-stu-id="4ca7a-109">The following Microsoft Dynamics service plans provide permissions to create environments:</span></span>

| <span data-ttu-id="4ca7a-110">整个产品库存单位 (SKU)</span><span class="sxs-lookup"><span data-stu-id="4ca7a-110">Overall product stockkeeping unit (SKU)</span></span>       | <span data-ttu-id="4ca7a-111">Power Apps P2 服务计划</span><span class="sxs-lookup"><span data-stu-id="4ca7a-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="4ca7a-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="4ca7a-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="4ca7a-113">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="4ca7a-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="4ca7a-114">Microsoft Dynamics 365 计划 Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="4ca7a-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="4ca7a-115">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="4ca7a-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="4ca7a-116">请注意，各个 Microsoft Office SKU 也提供权限，以及独立的 Power Apps 计划 2 SKU。</span><span class="sxs-lookup"><span data-stu-id="4ca7a-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="4ca7a-117">重点是这些 SKU 中的一个必须存在。</span><span class="sxs-lookup"><span data-stu-id="4ca7a-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="4ca7a-118">转到 [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments)。</span><span class="sxs-lookup"><span data-stu-id="4ca7a-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="4ca7a-119">按照[配置 Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) 中的说明创建环境。</span><span class="sxs-lookup"><span data-stu-id="4ca7a-119">Create the environments by following the instructions in [Provision Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
