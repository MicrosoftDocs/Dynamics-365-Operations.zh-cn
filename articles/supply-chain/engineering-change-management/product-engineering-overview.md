---
title: 工程更改管理概述
description: 此主题概述了工程更改管理，可帮助您计划和管理产品版本控制以及管理产品生命周期和工程更改。
author: t-benebo
manager: tfehr
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: f1aa04b472eaef7ed398f08a05d46bac2d589561
ms.sourcegitcommit: 9f32389715b226c11e74c53547527e0a8b51e300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/12/2020
ms.locfileid: "4514342"
---
# <a name="engineering-change-management-overview"></a><span data-ttu-id="384ee-103">工程更改管理概述</span><span class="sxs-lookup"><span data-stu-id="384ee-103">Engineering change management overview</span></span>

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a><span data-ttu-id="384ee-104">功能汇总</span><span class="sxs-lookup"><span data-stu-id="384ee-104">Feature summary</span></span>

<span data-ttu-id="384ee-105">当今的制造商需要强大的产品数据管理、版本控制和工程更改管理，才能在不断缩短的产品生命周期、不断提高的质量和可靠性要求以及日益增加的产品安全关注的世界中取得成功。</span><span class="sxs-lookup"><span data-stu-id="384ee-105">Today's manufacturers require strong product data management, version control, and engineering change management to succeed in a world of constantly shrinking product lifecycles, increased quality and reliability requirements, and an increased focus on product safety.</span></span>

<span data-ttu-id="384ee-106">工程更改管理为产品数据管理流程带来了结构和规范，让产品能够以工作流支持的受控方式定义、发布和修订。</span><span class="sxs-lookup"><span data-stu-id="384ee-106">Engineering change management brings structure and discipline to the product data management process, and enables products to be defined, released, and revised in a controlled manner that is supported by workflows.</span></span><span data-ttu-id="384ee-107">通过产品版本和工程更改管理，您可以在产品的整个生命周期内记录、评估影响和应用工程更改。</span><span class="sxs-lookup"><span data-stu-id="384ee-107"> Through product versions and engineering change management, you can document, assess the impact of, and apply engineering changes throughout the whole lifecycle of a product.</span></span>

<span data-ttu-id="384ee-108">工程更改管理可帮助您计划和管理产品版本控制以及管理产品生命周期和工程更改。</span><span class="sxs-lookup"><span data-stu-id="384ee-108">Engineering change management helps you plan and manage product versioning, and manage product lifecycles and engineering changes.</span></span> <span data-ttu-id="384ee-109">以下是其主要功能的列表：</span><span class="sxs-lookup"><span data-stu-id="384ee-109">Here is a list of its main features:</span></span>

- <span data-ttu-id="384ee-110">产品版本控制</span><span class="sxs-lookup"><span data-stu-id="384ee-110">Product versioning</span></span>
- <span data-ttu-id="384ee-111">增强的产品发布功能让您可以在一个法人（工程公司）中维护基础产品，然后将完全配置的已发布产品发布到其他法人</span><span class="sxs-lookup"><span data-stu-id="384ee-111">Enhanced product release functionality that lets you maintain product master data in one legal entity (the engineering company) and publish the fully configured released product to other legal entities</span></span>
- <span data-ttu-id="384ee-112">在产品版本激活之前验证是否输入所需信息的规则（准备情况检查）</span><span class="sxs-lookup"><span data-stu-id="384ee-112">Rules for validating that required information is entered before a product version is activated (readiness checks)</span></span>
- <span data-ttu-id="384ee-113">通过对已发布产品可以在特定业务流程中使用的时间进行细粒度控制，改进了产品生命周期管理</span><span class="sxs-lookup"><span data-stu-id="384ee-113">Improved product lifecycle management through fine-grained control over when a released product can be used in specific business processes</span></span>
- <span data-ttu-id="384ee-114">工作流支持的工程更改请求</span><span class="sxs-lookup"><span data-stu-id="384ee-114">Engineering change requests that are supported by workflows</span></span>
- <span data-ttu-id="384ee-115">工作流支持的工程更改订单</span><span class="sxs-lookup"><span data-stu-id="384ee-115">Engineering change orders that are supported by workflows</span></span>

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4HE6B]

<span data-ttu-id="384ee-116">前面的视频（[Dynamics 365 Supply Chain Management 中的更改管理功能](https://youtu.be/N313FqvRuBc)）包含在 YouTube 上的 [Finance and Operations 播放列表](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW)中。</span><span class="sxs-lookup"><span data-stu-id="384ee-116">The preceding video ([Change management capabilities in Dynamics 365 Supply Chain Management](https://youtu.be/N313FqvRuBc)) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="turn-on-engineering-change-management-for-your-system"></a><span data-ttu-id="384ee-117">为系统开启工程更改管理</span><span class="sxs-lookup"><span data-stu-id="384ee-117">Turn on engineering change management for your system</span></span>

<span data-ttu-id="384ee-118">首先，按照以下步骤开启工程更改管理。</span><span class="sxs-lookup"><span data-stu-id="384ee-118">First, turn on engineering change management by following these steps.</span></span>

1. <span data-ttu-id="384ee-119">转到[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="384ee-119">Go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
1. <span data-ttu-id="384ee-120">检查更新。</span><span class="sxs-lookup"><span data-stu-id="384ee-120">Check for updates.</span></span>
1. <span data-ttu-id="384ee-121">开启名为 **工程更改管理** 的功能。</span><span class="sxs-lookup"><span data-stu-id="384ee-121">Turn on the feature that is named **Engineering Change Management**.</span></span>

<span data-ttu-id="384ee-122">接下来，按照以下步骤打开 **工程更改管理** 配置密钥。</span><span class="sxs-lookup"><span data-stu-id="384ee-122">Next, turn on the **Engineering Change Management** configuration key by following these steps.</span></span>

1. <span data-ttu-id="384ee-123">将您的系统置于维护模式下，如[维护模式](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="384ee-123">Put your system into maintenance mode, as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
1. <span data-ttu-id="384ee-124">转到 **系统管理 \> 设置 \> 许可证配置**。</span><span class="sxs-lookup"><span data-stu-id="384ee-124">Go to **System administration \> Setup \> License configuration**.</span></span>
1. <span data-ttu-id="384ee-125">展开 **贸易** 节点，选择 **工程更改管理** 复选框。</span><span class="sxs-lookup"><span data-stu-id="384ee-125">Expand the **Trade** node, and select the **Engineering Change Management** check box.</span></span>
1. <span data-ttu-id="384ee-126">关闭维护模式，如[维护模式](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="384ee-126">Turn off maintenance mode, as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
