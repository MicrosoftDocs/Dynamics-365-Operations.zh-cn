---
title: 工程更改管理概述
description: 此主题概述了工程更改管理，可帮助您计划和管理产品版本控制以及管理产品生命周期和工程更改。
author: t-benebo
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: d9430fe02abe58f37d2bfd1431b4da61527d0834
ms.sourcegitcommit: 588f8343aaa654309d2ff735fd437dba6acd9d46
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115041"
---
# <a name="engineering-change-management-overview"></a><span data-ttu-id="72e22-103">工程更改管理概述</span><span class="sxs-lookup"><span data-stu-id="72e22-103">Engineering change management overview</span></span>

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a><span data-ttu-id="72e22-104">功能汇总</span><span class="sxs-lookup"><span data-stu-id="72e22-104">Feature summary</span></span>

<span data-ttu-id="72e22-105">当今的制造商需要强大的产品数据管理、版本控制和工程更改管理，才能在不断缩短的产品生命周期、不断提高的质量和可靠性要求以及日益增加的产品安全关注的世界中取得成功。</span><span class="sxs-lookup"><span data-stu-id="72e22-105">Today's manufacturers require strong product data management, version control, and engineering change management to succeed in a world of constantly shrinking product lifecycles, increased quality and reliability requirements, and an increased focus on product safety.</span></span>

<span data-ttu-id="72e22-106">工程更改管理为产品数据管理流程带来了结构和规范，让产品能够以工作流支持的受控方式定义、发布和修订。</span><span class="sxs-lookup"><span data-stu-id="72e22-106">Engineering change management brings structure and discipline to the product data management process, and enables products to be defined, released, and revised in a controlled manner that is supported by workflows.</span></span><span data-ttu-id="72e22-107">通过产品版本和工程更改管理，您可以在产品的整个生命周期内记录、评估影响和应用工程更改。</span><span class="sxs-lookup"><span data-stu-id="72e22-107"> Through product versions and engineering change management, you can document, assess the impact of, and apply engineering changes throughout the whole lifecycle of a product.</span></span>

<span data-ttu-id="72e22-108">工程更改管理可帮助您计划和管理产品版本控制以及管理产品生命周期和工程更改。</span><span class="sxs-lookup"><span data-stu-id="72e22-108">Engineering change management helps you plan and manage product versioning, and manage product lifecycles and engineering changes.</span></span> <span data-ttu-id="72e22-109">以下是其主要功能的列表：</span><span class="sxs-lookup"><span data-stu-id="72e22-109">Here is a list of its main features:</span></span>

- <span data-ttu-id="72e22-110">产品版本控制</span><span class="sxs-lookup"><span data-stu-id="72e22-110">Product versioning</span></span>
- <span data-ttu-id="72e22-111">增强的产品发布功能让您可以在一个法人（工程公司）中维护基础产品，然后将完全配置的已发布产品发布到其他法人</span><span class="sxs-lookup"><span data-stu-id="72e22-111">Enhanced product release functionality that lets you maintain product master data in one legal entity (the engineering company) and publish the fully configured released product to other legal entities</span></span>
- <span data-ttu-id="72e22-112">在产品版本激活之前验证是否输入所需信息的规则（准备情况检查）</span><span class="sxs-lookup"><span data-stu-id="72e22-112">Rules for validating that required information is entered before a product version is activated (readiness checks)</span></span>
- <span data-ttu-id="72e22-113">通过对已发布产品可以在特定业务流程中使用的时间进行细粒度控制，改进了产品生命周期管理</span><span class="sxs-lookup"><span data-stu-id="72e22-113">Improved product lifecycle management through fine-grained control over when a released product can be used in specific business processes</span></span>
- <span data-ttu-id="72e22-114">工作流支持的工程更改请求</span><span class="sxs-lookup"><span data-stu-id="72e22-114">Engineering change requests that are supported by workflows</span></span>
- <span data-ttu-id="72e22-115">工作流支持的工程更改订单</span><span class="sxs-lookup"><span data-stu-id="72e22-115">Engineering change orders that are supported by workflows</span></span>

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4HE6B]

<span data-ttu-id="72e22-116">前面的视频（[Dynamics 365 Supply Chain Management 中的更改管理功能](https://youtu.be/N313FqvRuBc)）包含在 YouTube 上的 [Finance and Operations 播放列表](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW)中。</span><span class="sxs-lookup"><span data-stu-id="72e22-116">The preceding video ([Change management capabilities in Dynamics 365 Supply Chain Management](https://youtu.be/N313FqvRuBc)) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="turn-on-the-engineering-change-management-and-version-dimension-features-for-your-system"></a><span data-ttu-id="72e22-117">为系统打开工程更改管理和版本维度功能</span><span class="sxs-lookup"><span data-stu-id="72e22-117">Turn on the engineering change management and version dimension features for your system</span></span>

<span data-ttu-id="72e22-118">必须同时启用 *工程更改管理* 功能及其配置密钥，然后才能够使用工程更改管理。</span><span class="sxs-lookup"><span data-stu-id="72e22-118">Before you can use engineering change management, you must enable both the *Engineering Change Management* feature and its configuration key.</span></span> <span data-ttu-id="72e22-119">如果您还想要跟踪交易中产品的版本维度（可选），还必须启用 *产品版本维度* 功能及其配置密钥。</span><span class="sxs-lookup"><span data-stu-id="72e22-119">If you also want to track the version dimension of products in transactions (optional), then you must also enable the *Product version dimension* feature and its configuration key.</span></span>

<span data-ttu-id="72e22-120">首先，按照以下步骤打开这些功能。</span><span class="sxs-lookup"><span data-stu-id="72e22-120">First, turn on the features by following these steps.</span></span>

1. <span data-ttu-id="72e22-121">转到[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区。</span><span class="sxs-lookup"><span data-stu-id="72e22-121">Go to the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace.</span></span>
1. <span data-ttu-id="72e22-122">检查更新。</span><span class="sxs-lookup"><span data-stu-id="72e22-122">Check for updates.</span></span>
1. <span data-ttu-id="72e22-123">开启名为 *工程更改管理* 的功能。</span><span class="sxs-lookup"><span data-stu-id="72e22-123">Turn on the feature that is named *Engineering Change Management*.</span></span>
1. <span data-ttu-id="72e22-124">如果要使用它，还要打开名为 *产品维度版本* 的功能。</span><span class="sxs-lookup"><span data-stu-id="72e22-124">If you want to use it, also turn on the feature that is named *Product dimension version*.</span></span>

<span data-ttu-id="72e22-125">接下来，按照以下步骤打开配置密钥。</span><span class="sxs-lookup"><span data-stu-id="72e22-125">Next, turn on the configuration keys by following these steps.</span></span>

1. <span data-ttu-id="72e22-126">将您的系统置于维护模式下，如[维护模式](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="72e22-126">Put your system into maintenance mode, as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
1. <span data-ttu-id="72e22-127">转到 **系统管理 \> 设置 \> 许可证配置**。</span><span class="sxs-lookup"><span data-stu-id="72e22-127">Go to **System administration \> Setup \> License configuration**.</span></span>
1. <span data-ttu-id="72e22-128">展开 **贸易** 节点。</span><span class="sxs-lookup"><span data-stu-id="72e22-128">Expand the **Trade** node.</span></span>
1. <span data-ttu-id="72e22-129">选中 **工程更改管理** 复选框，启用主要功能的 Configuration Key。</span><span class="sxs-lookup"><span data-stu-id="72e22-129">Enable the configuration key for the main feature by selecting the **Engineering Change Management** checkbox.</span></span>
1. <span data-ttu-id="72e22-130">展开 **工程更改管理** 节点，根据需要选择或清除以下复选框（取决于您要使用的功能）：</span><span class="sxs-lookup"><span data-stu-id="72e22-130">Expand the **Engineering Change Management** node, and select or clear the following checkboxes as required (depending on the features that you want to use):</span></span>

    - <span data-ttu-id="72e22-131">**属性搜索** – 选中此复选框将启用[属性搜索功能](engineering-attributes-and-search.md)。</span><span class="sxs-lookup"><span data-stu-id="72e22-131">**Attribute search** – Select this checkbox to enable the [attribute search feature](engineering-attributes-and-search.md).</span></span> <span data-ttu-id="72e22-132">我们建议启用此功能，但是如果您不使用它，可以清除此复选框。</span><span class="sxs-lookup"><span data-stu-id="72e22-132">We recommend enabling this feature, but you can clear this checkbox if you won't use it.</span></span>
    - <span data-ttu-id="72e22-133">**处理制造的更改管理** – 如果要使用工程更改管理功能管理处理制造配方的更改，请选中此复选框。</span><span class="sxs-lookup"><span data-stu-id="72e22-133">**Change management for process manufacturing** – Select this checkbox if you want to use Engineering change management features to manage changes in formulas for process manufacturing.</span></span> <span data-ttu-id="72e22-134">如果您不必管理配方，可以清除此复选框。</span><span class="sxs-lookup"><span data-stu-id="72e22-134">If you don't have to manage formulas, you can clear this checkbox.</span></span> <span data-ttu-id="72e22-135">有关详细信息，请参阅[管理配方及其成分的更改](manage-formula-changes.md)。</span><span class="sxs-lookup"><span data-stu-id="72e22-135">For more information, see [Manage changes in formulas and their ingredients](manage-formula-changes.md).</span></span>

1. <span data-ttu-id="72e22-136">如果您还想使用版本维度，还要选中 **产品维度 - 版本** 复选框。</span><span class="sxs-lookup"><span data-stu-id="72e22-136">If you also want to use the version dimension, then select the **Product dimension - Version** checkbox.</span></span> <span data-ttu-id="72e22-137">（此复选框在列表再下面，不是嵌套在 **工程更改管理** 节点下。）</span><span class="sxs-lookup"><span data-stu-id="72e22-137">(This checkbox is further down the list, not nested under the **Engineering Change Management** node.)</span></span>
1. <span data-ttu-id="72e22-138">关闭维护模式，如[维护模式](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="72e22-138">Turn off maintenance mode, as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="72e22-139">从 2022 年 4 月开始，默认情况下，所有新安装的 **工程更改管理** 和 **产品维度 - 版本** 的许可证密钥都将启用，但是如果需要，您仍然可以将其禁用。</span><span class="sxs-lookup"><span data-stu-id="72e22-139">Starting in April 2022, the license keys for both **Engineering Change Management** and **Product dimension - Version** will be enabled by default for all new installations, but you will still be able to disable them if needed.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
