---
title: 覆盖了装运合并策略时从“发放到仓库”页合并装运
description: 此主题提供了以下方案：必须从“发放到仓库”页将一个或多个销售行手动发放到仓库，并且发布前必须已覆盖系统定义的装运合并策略。
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-olbara
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 23379b76367336157edad1bf2e534bf0f10799cb
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383724"
---
# <a name="consolidate-shipments-when-the-shipment-consolidation-policy-is-overridden-from-the-release-to-warehouse-page"></a><span data-ttu-id="adcab-103">覆盖了装运合并策略时从“发放到仓库”页合并装运</span><span class="sxs-lookup"><span data-stu-id="adcab-103">Consolidate shipments when the shipment consolidation policy is overridden from the Release to warehouse page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="adcab-104">此主题提供了以下方案：必须从**发放到仓库**页将一个或多个销售行手动发放到仓库，并且发布前必须已覆盖系统定义的装运合并策略。</span><span class="sxs-lookup"><span data-stu-id="adcab-104">This topic presents a scenario where one or more sales lines must be manually released to the warehouse from the **Release to warehouse** page, and the system-defined shipment consolidation policy must be overridden before the release.</span></span> <span data-ttu-id="adcab-105">例如，以下情况下可能需要覆盖装运合并策略：必须将通常不与未结装运合并的订单与未结装运合并。</span><span class="sxs-lookup"><span data-stu-id="adcab-105">An override of the shipment consolidation policy might be required if, for example, an order that isn't usually consolidated with open shipments must be consolidated with open shipments.</span></span>

<span data-ttu-id="adcab-106">在此方案中，将创建一组销售订单，然后在将这些订单发放到仓库之前覆盖默认装运合并策略。</span><span class="sxs-lookup"><span data-stu-id="adcab-106">During the scenario, you will create a set of sales orders and then override the default shipment consolidation policy before you release the orders to the warehouse.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="adcab-107">提供演示数据</span><span class="sxs-lookup"><span data-stu-id="adcab-107">Make demo data available</span></span>

<span data-ttu-id="adcab-108">此主题中的方案引用为 Microsoft Dynamics 365 Supply Chain Management 提供的标准演示数据中包含的值和记录。</span><span class="sxs-lookup"><span data-stu-id="adcab-108">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="adcab-109">如果要在进行此练习时使用此处提供的值，请务必在安装了演示数据的环境中操作，并且在开始前将法人设置为 **USMF**。</span><span class="sxs-lookup"><span data-stu-id="adcab-109">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="adcab-110">设置装运合并策略和产品筛选器</span><span class="sxs-lookup"><span data-stu-id="adcab-110">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="adcab-111">此处介绍的方案假设已经开启了此功能，完成了[配置装运合并策略](configure-shipment-consolidation-policies.md)中的练习，并创建了其中介绍的策略和其他记录。</span><span class="sxs-lookup"><span data-stu-id="adcab-111">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="adcab-112">务必先完成这些练习，再继续完成此方案。</span><span class="sxs-lookup"><span data-stu-id="adcab-112">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="adcab-113">为此方案创建销售订单</span><span class="sxs-lookup"><span data-stu-id="adcab-113">Create the sales orders for this scenario</span></span>

1. <span data-ttu-id="adcab-114">转到**应收帐款 \> 订单 \> 所有销售订单**，然后创建具有以下设置的三个相同销售订单：</span><span class="sxs-lookup"><span data-stu-id="adcab-114">Go to **Accounts receivable \> Orders \> All sales orders**, and create three identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="adcab-115">**客户帐户**：*US-002*</span><span class="sxs-lookup"><span data-stu-id="adcab-115">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="adcab-116">添加具有以下设置的订单行：</span><span class="sxs-lookup"><span data-stu-id="adcab-116">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="adcab-117">**物料编号**：*A0001*（未为其分配**代码 4** 筛选器的物料）</span><span class="sxs-lookup"><span data-stu-id="adcab-117">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="adcab-118">**数量：** *1.00*</span><span class="sxs-lookup"><span data-stu-id="adcab-118">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="adcab-119">选择**库存 \> 预留**，然后在操作窗格上选择**预留批次**预留订单行。</span><span class="sxs-lookup"><span data-stu-id="adcab-119">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-sales-orders-from-the-release-to-warehouse-page"></a><span data-ttu-id="adcab-120">从“发放到仓库”页发放销售订单</span><span class="sxs-lookup"><span data-stu-id="adcab-120">Release the sales orders from the Release to warehouse page</span></span>

<span data-ttu-id="adcab-121">发放到仓库期间执行以下步骤覆盖装运合并策略。</span><span class="sxs-lookup"><span data-stu-id="adcab-121">Follow these steps to override the shipment consolidation policy during the release to the warehouse.</span></span>

1. <span data-ttu-id="adcab-122">转到**仓库管理 \> 发放到仓库 \> 发放到仓库**。</span><span class="sxs-lookup"><span data-stu-id="adcab-122">Go to **Warehouse management \> Release to warehouse \> Release to warehouse**.</span></span>
1. <span data-ttu-id="adcab-123">在上方窗格中，选择为此方案创建的第一个销售订单。</span><span class="sxs-lookup"><span data-stu-id="adcab-123">In the upper pane, select the first sales order that you created for this scenario.</span></span>
1. <span data-ttu-id="adcab-124">选择**添加**将行添加到“发放到仓库”。</span><span class="sxs-lookup"><span data-stu-id="adcab-124">Select **Add** to add the line to the release to the warehouse.</span></span> <span data-ttu-id="adcab-125">请注意，底部窗格中应用了*默认*装运合并策略。</span><span class="sxs-lookup"><span data-stu-id="adcab-125">Notice that the *Default* shipment consolidation policy is applied in the bottom pane.</span></span>
1. <span data-ttu-id="adcab-126">在底部窗格中，选择**选择新装运合并策略**。</span><span class="sxs-lookup"><span data-stu-id="adcab-126">In the bottom pane, select **Select new shipment consolidation policy**.</span></span>
1. <span data-ttu-id="adcab-127">选择允许与相同策略的其他未结装运合并的策略。</span><span class="sxs-lookup"><span data-stu-id="adcab-127">Select a policy that allows for consolidation with other open shipments of the same policy.</span></span> <span data-ttu-id="adcab-128">例如，选择 *CustomerOrderNo* 策略。</span><span class="sxs-lookup"><span data-stu-id="adcab-128">For example, select the *CustomerOrderNo* policy.</span></span>
1. <span data-ttu-id="adcab-129">选择**发放到仓库**。</span><span class="sxs-lookup"><span data-stu-id="adcab-129">Select **Release to warehouse**.</span></span>
1. <span data-ttu-id="adcab-130">选择为此方案创建的第二个和第三个销售订单。</span><span class="sxs-lookup"><span data-stu-id="adcab-130">Select the second and third sales orders that you created for this scenario.</span></span>
1. <span data-ttu-id="adcab-131">选择**添加**将这些行添加到“发放到仓库”。</span><span class="sxs-lookup"><span data-stu-id="adcab-131">Select **Add** to add the lines to the release to the warehouse.</span></span> <span data-ttu-id="adcab-132">请注意，底部窗格中应用了*默认*策略。</span><span class="sxs-lookup"><span data-stu-id="adcab-132">Notice that the *Default* policy is applied in the bottom pane.</span></span>
1. <span data-ttu-id="adcab-133">选择第二行，然后在**选择新装运合并策略**字段中选择 *CustomerOrderNo* 策略。</span><span class="sxs-lookup"><span data-stu-id="adcab-133">Select the second line, and then, in the **Select new shipment consolidation policy** field, select the *CustomerOrderNo* policy.</span></span>
1. <span data-ttu-id="adcab-134">为两行都选择**发放到仓库**。</span><span class="sxs-lookup"><span data-stu-id="adcab-134">Select **Release to warehouse** for both lines.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="adcab-135">验证装运</span><span class="sxs-lookup"><span data-stu-id="adcab-135">Verify the shipments</span></span>

<span data-ttu-id="adcab-136">应该已经创建了两个装运：</span><span class="sxs-lookup"><span data-stu-id="adcab-136">Two shipments should have been created:</span></span>

- <span data-ttu-id="adcab-137">第一个装运中包含两行，该装运是使用 *CustomerOrderNo* 装运合并策略创建的。</span><span class="sxs-lookup"><span data-stu-id="adcab-137">The first shipment contains two lines and was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>
- <span data-ttu-id="adcab-138">第二个装运中包含一行，该装运是使用*默认*装运合并策略创建的。</span><span class="sxs-lookup"><span data-stu-id="adcab-138">The second shipment contains one line and was created by using the *Default* shipment consolidation policy.</span></span>

<span data-ttu-id="adcab-139">请执行以下步骤查看创建的装运。</span><span class="sxs-lookup"><span data-stu-id="adcab-139">Follow these steps to review the shipments that were created.</span></span>

1. <span data-ttu-id="adcab-140">转到**仓库管理 \> 装运 \> 所有装运**。</span><span class="sxs-lookup"><span data-stu-id="adcab-140">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="adcab-141">找到并选择所需装运。</span><span class="sxs-lookup"><span data-stu-id="adcab-141">Find and select the required shipment.</span></span>
1. <span data-ttu-id="adcab-142">在**装运合并策略**字段中，查看创建装运时使用的合并策略。</span><span class="sxs-lookup"><span data-stu-id="adcab-142">In the **Shipment consolidation policy** field, review the consolidation policy that was used when the shipment was created.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="adcab-143">其他资源</span><span class="sxs-lookup"><span data-stu-id="adcab-143">Additional resources</span></span>

- [<span data-ttu-id="adcab-144">装运合并政策</span><span class="sxs-lookup"><span data-stu-id="adcab-144">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="adcab-145">配置装运合并策略</span><span class="sxs-lookup"><span data-stu-id="adcab-145">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
