---
title: 无法在 Power Apps 管理中心内创建环境
description: 本主题说明如果管理员无法在 Microsoft Power Apps 管理中心创建环境该做什么。
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 5923c59ab5dde13fed0483972e76634031404fd8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773211"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="e2312-103">无法在 Power Apps 管理中心内创建环境</span><span class="sxs-lookup"><span data-stu-id="e2312-103">Can't create an environment in the Power Apps Admin center</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e2312-104">**发货**</span><span class="sxs-lookup"><span data-stu-id="e2312-104">**Issue**</span></span>

- <span data-ttu-id="e2312-105">租户/环境管理员无法在 Microsoft Power Apps 管理中心创建环境。</span><span class="sxs-lookup"><span data-stu-id="e2312-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="e2312-106">授予用户执行环境创建步骤权限的许可证未直接分配给执行该步骤的用户。</span><span class="sxs-lookup"><span data-stu-id="e2312-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="e2312-107">**解决方案**</span><span class="sxs-lookup"><span data-stu-id="e2312-107">**Solution**</span></span>

<span data-ttu-id="e2312-108">确保租户管理员已将有效的 Power Apps P2 许可证直接分配给将执行环境创建步骤的用户。</span><span class="sxs-lookup"><span data-stu-id="e2312-108">Make sure that the tenant admin has assigned a valid Power Apps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="e2312-109">这里是提供该权限的 Microsoft Dynamics 服务计划。</span><span class="sxs-lookup"><span data-stu-id="e2312-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="e2312-110">整个产品库存单位 (SKU)</span><span class="sxs-lookup"><span data-stu-id="e2312-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="e2312-111">Power Apps P2 服务计划</span><span class="sxs-lookup"><span data-stu-id="e2312-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="e2312-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="e2312-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="e2312-113">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="e2312-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="e2312-114">Microsoft Dynamics 365 计划 Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="e2312-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="e2312-115">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="e2312-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="e2312-116">请注意，各个 Microsoft Office SKU 也提供权限，以及独立的 Power Apps 计划 2 SKU。</span><span class="sxs-lookup"><span data-stu-id="e2312-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="e2312-117">重点是这些 SKU 中的一个必须存在。</span><span class="sxs-lookup"><span data-stu-id="e2312-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="e2312-118">转到 [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments)。</span><span class="sxs-lookup"><span data-stu-id="e2312-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="e2312-119">按照[配置 Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) 中的说明创建环境。</span><span class="sxs-lookup"><span data-stu-id="e2312-119">Create the environments by following the instructions in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
