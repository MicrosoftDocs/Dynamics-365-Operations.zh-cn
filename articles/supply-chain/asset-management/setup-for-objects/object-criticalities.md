---
title: 资产关键性类型
description: 本主题介绍资产管理中的资产关键性类型。
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetCriticality, EntAssetObjectCriticality
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b7d6e3dea1b3c1ef47490df678f639c036cdd5c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4422908"
---
# <a name="asset-criticality-types"></a><span data-ttu-id="e5f5f-103">资产关键性类型</span><span class="sxs-lookup"><span data-stu-id="e5f5f-103">Asset criticality types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="e5f5f-104">本主题介绍资产管理中的资产关键性类型。</span><span class="sxs-lookup"><span data-stu-id="e5f5f-104">The topic explains asset criticality types in Asset Management.</span></span> <span data-ttu-id="e5f5f-105">资产关键性与资产关联，并转移到工作订单。</span><span class="sxs-lookup"><span data-stu-id="e5f5f-105">Asset criticality is related to assets and is transferred to work orders.</span></span> <span data-ttu-id="e5f5f-106">不能在工作订单中更改。</span><span class="sxs-lookup"><span data-stu-id="e5f5f-106">It can't be changed on a work order.</span></span> <span data-ttu-id="e5f5f-107">资产关键性用于在计划工作订单时计算工作订单关键性。</span><span class="sxs-lookup"><span data-stu-id="e5f5f-107">Asset criticality is used to calculate work order criticality during work order scheduling.</span></span> <span data-ttu-id="e5f5f-108">换句话说，用于计算资产的维护作业对公司中的生产计划和生产效率的影响程度。</span><span class="sxs-lookup"><span data-stu-id="e5f5f-108">In other words, it's used to calculate the extent to which a maintenance job on an asset affects the production schedule and productivity in your company.</span></span> <span data-ttu-id="e5f5f-109">有关与计算工作订单排产的等级评分关联的设置的详细信息，请参阅[资产管理参数](../setup-for-objects/enterprise-asset-management-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="e5f5f-109">For more information about the setup that is related to the calculation of rating scores for work order scheduling, see [Asset Management parameters](../setup-for-objects/enterprise-asset-management-parameters.md).</span></span>

<span data-ttu-id="e5f5f-110">若要设置关键性，首先创建资产设置中应该使用的关键性类型。</span><span class="sxs-lookup"><span data-stu-id="e5f5f-110">To set up criticality, you first create the criticality types that should be used in the asset setup.</span></span> <span data-ttu-id="e5f5f-111">然后设置资产关键性。</span><span class="sxs-lookup"><span data-stu-id="e5f5f-111">You then set up asset criticalities.</span></span>

## <a name="set-up-criticality-types"></a><span data-ttu-id="e5f5f-112">设置关键性类型</span><span class="sxs-lookup"><span data-stu-id="e5f5f-112">Set up criticality types</span></span>

1. <span data-ttu-id="e5f5f-113">选择 **资产管理** \> **设置** \> **资产** \> **关键性类型**。</span><span class="sxs-lookup"><span data-stu-id="e5f5f-113">Select **Asset management** \> **Setup** \> **Assets** \> **Criticality types**.</span></span>
2. <span data-ttu-id="e5f5f-114">选择 **新建** 创建记录。</span><span class="sxs-lookup"><span data-stu-id="e5f5f-114">Select **New** to create a record.</span></span>
3. <span data-ttu-id="e5f5f-115">在 **关键性** 字段中，输入用于表示关键性的数字。</span><span class="sxs-lookup"><span data-stu-id="e5f5f-115">In the **Criticality** field, enter a number that indicates the criticality.</span></span>
4. <span data-ttu-id="e5f5f-116">在 **名称** 字段中，输入关键性类型的名称。</span><span class="sxs-lookup"><span data-stu-id="e5f5f-116">In the **Name** field, enter a name for the criticality type.</span></span>
5. <span data-ttu-id="e5f5f-117">在 **系数** 字段中，输入一个系数。</span><span class="sxs-lookup"><span data-stu-id="e5f5f-117">In the **Factor** field, enter a factor.</span></span> <span data-ttu-id="e5f5f-118">此系数在计算工作订单排产时用于确定应使用的关键性记录。</span><span class="sxs-lookup"><span data-stu-id="e5f5f-118">This factor is used during the calculation of work order scheduling to determine the criticality record that should be used.</span></span> <span data-ttu-id="e5f5f-119">（始终使用系数最大的记录。）如果创建的关键性行具有相同的关键性值（如下图所示），则此设置相关。</span><span class="sxs-lookup"><span data-stu-id="e5f5f-119">(The record that has the highest factor is always used.) This setting is relevant if, as shown in the following illustration, criticality lines are created that have the same criticality value.</span></span>

    ![关键性类型页面](media/23-setup-for-objects.png)

## <a name="set-up-asset-criticalities"></a><span data-ttu-id="e5f5f-121">设置资产关键性</span><span class="sxs-lookup"><span data-stu-id="e5f5f-121">Set up asset criticalities</span></span>

1. <span data-ttu-id="e5f5f-122">选择 **资产管理** \> **设置** \> **资产关键性**。</span><span class="sxs-lookup"><span data-stu-id="e5f5f-122">Select **Asset management** \> **Setup** \> **Asset criticalities**.</span></span>
2. <span data-ttu-id="e5f5f-123">选择 **新建** 创建记录。</span><span class="sxs-lookup"><span data-stu-id="e5f5f-123">Select **New** to create a record.</span></span>
3. <span data-ttu-id="e5f5f-124">根据所需的资产关键性详细信息级别，在 **功能位置**、**资产类型**、**制造商**、**模型**、**资产**、**作业类型类别**、**作业类型**、**作业类型变体** 和 **作业要求** 字段中进行相关选择。</span><span class="sxs-lookup"><span data-stu-id="e5f5f-124">Depending on the required level of detail for asset criticality, make relevant selections in the **Functional location**, **Asset type**, **Manufacturer**, **Model**, **Asset**, **Job type category**, **Job type**, **Job type variant**, and **Job requirement** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e5f5f-125">选择资产关键性之后，资产管理将检查所有资产关键性记录以查找可能的匹配项。</span><span class="sxs-lookup"><span data-stu-id="e5f5f-125">When an asset criticality is selected, Asset Management goes through all asset criticality records to check for a possible match.</span></span> <span data-ttu-id="e5f5f-126">始终先检查最具体的组合。</span><span class="sxs-lookup"><span data-stu-id="e5f5f-126">It always checks the most specific combination first.</span></span> <span data-ttu-id="e5f5f-127">换句话说，资产管理首先检查 **作业要求**。</span><span class="sxs-lookup"><span data-stu-id="e5f5f-127">In other words, Asset Management first checks **Job requirement**.</span></span> <span data-ttu-id="e5f5f-128">如果未找到匹配项，将检查 **作业类型变体**。</span><span class="sxs-lookup"><span data-stu-id="e5f5f-128">If no match is found, it checks **Job type variant**.</span></span> <span data-ttu-id="e5f5f-129">如果未找到匹配项，将检查 **作业类型变体**，依此类推。</span><span class="sxs-lookup"><span data-stu-id="e5f5f-129">If no match is found, it checks **Job type**, and so on.</span></span> <span data-ttu-id="e5f5f-130">如页面布局中显示，此行为表示为了找到最具体的组合，资产管理从右到左检查每个记录以查找匹配项。</span><span class="sxs-lookup"><span data-stu-id="e5f5f-130">As you can see in the layout of the page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="e5f5f-131">如果未找到匹配项，将使用无可供选择的内容的"默认"记录。</span><span class="sxs-lookup"><span data-stu-id="e5f5f-131">If no match is found, the "default" record that has no selections is used.</span></span>

4. <span data-ttu-id="e5f5f-132">在 **关键性** 字段中，选择在上一个过程中创建的一个关键性值。</span><span class="sxs-lookup"><span data-stu-id="e5f5f-132">In the **Criticality** field, select one of the criticality values that you created in the previous procedure.</span></span>

### <a name="notes-about-criticality-setup"></a><span data-ttu-id="e5f5f-133">有关关键性设置的说明</span><span class="sxs-lookup"><span data-stu-id="e5f5f-133">Notes about criticality setup</span></span>

- <span data-ttu-id="e5f5f-134">如果在此设置中更改已在工作订单中使用过的资产关键性，将不会相应更新工作订单中的关键性。</span><span class="sxs-lookup"><span data-stu-id="e5f5f-134">If you change an asset criticality in this setup after you've already used it on a work order, the criticality on the work order isn't updated accordingly.</span></span>
- <span data-ttu-id="e5f5f-135">只要在工作订单中添加或删除工作订单行，都将重新计算该工作订单中的关键性。</span><span class="sxs-lookup"><span data-stu-id="e5f5f-135">The criticality on a work order is recalculated every time that a work order line is added to or deleted from the work order.</span></span>
- <span data-ttu-id="e5f5f-136">如果一个工作订单中包含多个工作订单作业，则始终在工作订单中使用根据 **关键性类型** 页上的 **系数** 字段的最高关键性。</span><span class="sxs-lookup"><span data-stu-id="e5f5f-136">If a work order contains several work order jobs, the highest criticality, according to the **Factor** field on the **Criticality types** page, is always used on the work order.</span></span>
- <span data-ttu-id="e5f5f-137">资产关键性通常会随时间改变。</span><span class="sxs-lookup"><span data-stu-id="e5f5f-137">Generally, asset criticality can change over a period.</span></span> <span data-ttu-id="e5f5f-138">购买新设备，补货等可能会影响关键性。</span><span class="sxs-lookup"><span data-stu-id="e5f5f-138">Criticality can be affected by the purchase of new equipment, refurbishments, and so on.</span></span> <span data-ttu-id="e5f5f-139">请考虑定期（如每年或每隔一年一次）重新评估资产关键性，以确保关键性定义与当前生产设置匹配。</span><span class="sxs-lookup"><span data-stu-id="e5f5f-139">Consider reevaluating your asset criticalities at regular intervals (for example, once per year or every other year) to make sure that your criticality definitions match your current production setup.</span></span>
