---
title: 无法在 Power Apps 管理中心内创建环境
description: 本文说明如果管理员无法在 Microsoft Power Apps 管理中心创建环境该做什么。
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 26a228229a09e74809a048675a3ff90025f2a26c
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892219"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="6b8cd-103">无法在 Power Apps 管理中心内创建环境</span><span class="sxs-lookup"><span data-stu-id="6b8cd-103">Can't create an environment in the Power Apps Admin center</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="6b8cd-104">**发货**</span><span class="sxs-lookup"><span data-stu-id="6b8cd-104">**Issue**</span></span>

- <span data-ttu-id="6b8cd-105">租户/环境管理员无法在 Microsoft Power Apps 管理中心创建环境。</span><span class="sxs-lookup"><span data-stu-id="6b8cd-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="6b8cd-106">用户没有授予创建环境权限的许可证。</span><span class="sxs-lookup"><span data-stu-id="6b8cd-106">The user doesn't have a license that gives the right to create environments.</span></span>

<span data-ttu-id="6b8cd-107">**解决方案**</span><span class="sxs-lookup"><span data-stu-id="6b8cd-107">**Solution**</span></span>

<span data-ttu-id="6b8cd-108">确保租户管理员已向创建环境的用户分配了有效的 Power Apps P2 许可证。</span><span class="sxs-lookup"><span data-stu-id="6b8cd-108">Make sure the tenant admin has assigned a valid Power Apps P2 license to the user creating the environment.</span></span> <span data-ttu-id="6b8cd-109">以下 Microsoft Dynamics 服务计划提供创建环境的权限：</span><span class="sxs-lookup"><span data-stu-id="6b8cd-109">The following Microsoft Dynamics service plans provide permissions to create environments:</span></span>

| <span data-ttu-id="6b8cd-110">整个产品库存单位 (SKU)</span><span class="sxs-lookup"><span data-stu-id="6b8cd-110">Overall product stockkeeping unit (SKU)</span></span>       | <span data-ttu-id="6b8cd-111">Power Apps P2 服务计划</span><span class="sxs-lookup"><span data-stu-id="6b8cd-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="6b8cd-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="6b8cd-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="6b8cd-113">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="6b8cd-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="6b8cd-114">Microsoft Dynamics 365 计划 Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="6b8cd-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="6b8cd-115">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="6b8cd-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="6b8cd-116">请注意，各个 Microsoft Office SKU 也提供权限，以及独立的 Power Apps 计划 2 SKU。</span><span class="sxs-lookup"><span data-stu-id="6b8cd-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="6b8cd-117">重点是这些 SKU 中的一个必须存在。</span><span class="sxs-lookup"><span data-stu-id="6b8cd-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="6b8cd-118">转到 [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments)。</span><span class="sxs-lookup"><span data-stu-id="6b8cd-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="6b8cd-119">按照[配置 Human Resources](/dynamics365/unified-operations/talent/provisioning-talent) 中的说明创建环境。</span><span class="sxs-lookup"><span data-stu-id="6b8cd-119">Create the environments by following the instructions in [Provision Human Resources](/dynamics365/unified-operations/talent/provisioning-talent).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]