---
title: 无法在 PowerApps 管理中心创建环境
description: 本主题说明如果管理员无法在 Microsoft PowerApps 管理中心创建环境该做什么。
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6f9b7ceef6895b295e6ae5a50d8ac7970497efe5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "303475"
---
# <a name="cant-create-an-environment-in-the-powerapps-admin-center"></a><span data-ttu-id="1c8ab-103">无法在 PowerApps 管理员中心内创建环境</span><span class="sxs-lookup"><span data-stu-id="1c8ab-103">Can't create an environment in the PowerApps Admin center</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1c8ab-104">**发货**</span><span class="sxs-lookup"><span data-stu-id="1c8ab-104">**Issue**</span></span>

- <span data-ttu-id="1c8ab-105">租户/环境管理员无法在 Microsoft PowerApps 管理中心创建环境。</span><span class="sxs-lookup"><span data-stu-id="1c8ab-105">The tenant/environment admin can't create an environment in the Microsoft PowerApps Admin center.</span></span>
- <span data-ttu-id="1c8ab-106">授予用户执行环境创建步骤权限的许可证未直接分配给执行该步骤的用户。</span><span class="sxs-lookup"><span data-stu-id="1c8ab-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="1c8ab-107">**解决方案**</span><span class="sxs-lookup"><span data-stu-id="1c8ab-107">**Solution**</span></span>

<span data-ttu-id="1c8ab-108">确保租户管理员已将有效的 PowerApps P2 许可证直接分配给将执行环境创建步骤的用户。</span><span class="sxs-lookup"><span data-stu-id="1c8ab-108">Make sure that the tenant admin has assigned a valid PowerApps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="1c8ab-109">这里是提供该权限的 Microsoft Dynamics 服务计划。</span><span class="sxs-lookup"><span data-stu-id="1c8ab-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="1c8ab-110">整个产品库存单位 (SKU)</span><span class="sxs-lookup"><span data-stu-id="1c8ab-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="1c8ab-111">PowerApps P2 服务计划</span><span class="sxs-lookup"><span data-stu-id="1c8ab-111">PowerApps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="1c8ab-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="1c8ab-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="1c8ab-113">PowerApps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="1c8ab-113">PowerApps for Dynamics 365</span></span> |
| <span data-ttu-id="1c8ab-114">Microsoft Dynamics 365 计划 Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="1c8ab-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="1c8ab-115">PowerApps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="1c8ab-115">PowerApps for Dynamics 365</span></span> |

<span data-ttu-id="1c8ab-116">请注意，各个 Microsoft Office SKU 也提供权限，以及独立的 PowerApps 计划 2 SKU。</span><span class="sxs-lookup"><span data-stu-id="1c8ab-116">Note that various Microsoft Office SKUs also provide the right, together with standalone PowerApps Plan 2 SKUs.</span></span> <span data-ttu-id="1c8ab-117">重点是这些 SKU 中的一个必须存在。</span><span class="sxs-lookup"><span data-stu-id="1c8ab-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="1c8ab-118">转到 [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments)。</span><span class="sxs-lookup"><span data-stu-id="1c8ab-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="1c8ab-119">按照[配置 Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent) 中的说明创建环境。</span><span class="sxs-lookup"><span data-stu-id="1c8ab-119">Create the environments by following the instructions in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
