---
title: "库存盘点的原因代码"
description: "此主题描述如何为盘点任务设置和应用原因代码。"
author: Mirzaab
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCountingReasonCodePolicy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 2f4332432ad73861cd9b6b6452685d3175ace56b
ms.contentlocale: zh-cn
ms.lasthandoff: 08/07/2018

---

# <a name="reason-codes-for-inventory-counting"></a><span data-ttu-id="d63da-103">库存盘点的原因代码</span><span class="sxs-lookup"><span data-stu-id="d63da-103">Reason codes for inventory counting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d63da-104">原因代码用于分析盘点流程的结果和执行该流程期间出现的任何差异。</span><span class="sxs-lookup"><span data-stu-id="d63da-104">Reason codes let you analyze the results of a counting process and any discrepancies that occur during that process.</span></span> <span data-ttu-id="d63da-105">可指定执行盘点的原因，如货盘损坏或基于库存样本调整存货。</span><span class="sxs-lookup"><span data-stu-id="d63da-105">You can specify the reason for doing the count, such as a broken pallet or a stock adjustment that is based on inventory samples.</span></span>

## <a name="recommendation"></a><span data-ttu-id="d63da-106">建议</span><span class="sxs-lookup"><span data-stu-id="d63da-106">Recommendation</span></span>

<span data-ttu-id="d63da-107">建议在设置系统之前定义原因代码的处理策略。</span><span class="sxs-lookup"><span data-stu-id="d63da-107">Before you set up the system, we recommend that you define a strategy for working with reason codes.</span></span> <span data-ttu-id="d63da-108">例如，尝试回答以下问题：</span><span class="sxs-lookup"><span data-stu-id="d63da-108">For example, try to answer the following questions:</span></span>

- <span data-ttu-id="d63da-109">是否必须为仓库设置原因代码？</span><span class="sxs-lookup"><span data-stu-id="d63da-109">Should reason codes be mandatory on warehouses?</span></span>
- <span data-ttu-id="d63da-110">是否必须为某些物料设置原因代码？</span><span class="sxs-lookup"><span data-stu-id="d63da-110">Should reason codes be mandatory or optional on some items?</span></span>
- <span data-ttu-id="d63da-111">需要多少个原因代码？</span><span class="sxs-lookup"><span data-stu-id="d63da-111">How many reason codes do you require?</span></span>
- <span data-ttu-id="d63da-112">条码扫描仪用户应如何使用原因代码？</span><span class="sxs-lookup"><span data-stu-id="d63da-112">How should users of barcode scanners use reason codes?</span></span> <span data-ttu-id="d63da-113">原因代码应该预选，必需还是不可编辑？</span><span class="sxs-lookup"><span data-stu-id="d63da-113">Should the reason codes be preselected, mandatory, or not editable?</span></span>
- <span data-ttu-id="d63da-114">仓库工作人员是否要求移动扫描仪上采用不同的原因代码行为？</span><span class="sxs-lookup"><span data-stu-id="d63da-114">Do warehouse workers require different reason code behavior on mobile scanners?</span></span> <span data-ttu-id="d63da-115">如果答案为是，则可创建多个菜单项，然后将其分配给不同人员。</span><span class="sxs-lookup"><span data-stu-id="d63da-115">If the answer is yes, you can create more menu items and assign them to different people.</span></span>

## <a name="where-reason-codes-apply"></a><span data-ttu-id="d63da-116">原因代码的应用场景</span><span class="sxs-lookup"><span data-stu-id="d63da-116">Where reason codes apply</span></span>

<span data-ttu-id="d63da-117">可创建多个原因代码策略，并且每个原因代码策略可以有两个盘点原因代码策略。</span><span class="sxs-lookup"><span data-stu-id="d63da-117">You can create multiple reason code policies, and each reason code policy can have two counting reason code policies.</span></span> <span data-ttu-id="d63da-118">可在仓库级别或物料级别使用盘点原因代码。</span><span class="sxs-lookup"><span data-stu-id="d63da-118">The counting reason code policies can be used at the warehouse level or the item level.</span></span>

## <a name="set-up-reason-code-policies"></a><span data-ttu-id="d63da-119">设置原因代码策略</span><span class="sxs-lookup"><span data-stu-id="d63da-119">Set up reason code policies</span></span>

1. <span data-ttu-id="d63da-120">选择**库存管理** \> **设置** \> **库存** \> **盘点原因代码策略**，然后创建新的原因代码策略、</span><span class="sxs-lookup"><span data-stu-id="d63da-120">Select **Inventory management** \> **Setup** \> **Inventory** \> **Counting reason code policies**, and create a new reason code policy.</span></span>
2. <span data-ttu-id="d63da-121">在**盘点原因代码类型**字段中，选择**必需**或**可选**以指定是否必须在以下盘点日记帐中选择原因代码：</span><span class="sxs-lookup"><span data-stu-id="d63da-121">In the **Counting reason code type** field, select either **Mandatory** or **Optional** to specify whether selection of a reason code should be an optional or mandatory action in one of the following counting journals:</span></span>

    - <span data-ttu-id="d63da-122">周期盘点（移动设备）</span><span class="sxs-lookup"><span data-stu-id="d63da-122">Cycle Count (mobile device)</span></span>
    - <span data-ttu-id="d63da-123">现货盘点（移动设备）</span><span class="sxs-lookup"><span data-stu-id="d63da-123">Spot Count (mobile device)</span></span>
    - <span data-ttu-id="d63da-124">阈值盘点（移动设备）</span><span class="sxs-lookup"><span data-stu-id="d63da-124">Threshold Count (mobile device)</span></span>
    - <span data-ttu-id="d63da-125">调入（移动设备）</span><span class="sxs-lookup"><span data-stu-id="d63da-125">Adjustment In (mobile device)</span></span>
    - <span data-ttu-id="d63da-126">调出（移动设备）</span><span class="sxs-lookup"><span data-stu-id="d63da-126">Adjustment Out (mobile device)</span></span>
    - <span data-ttu-id="d63da-127">盘点日记帐（富客户端）</span><span class="sxs-lookup"><span data-stu-id="d63da-127">Counting Journal (rich client)</span></span>

<span data-ttu-id="d63da-128">也可以为单个仓库和为产品设置原因代码。</span><span class="sxs-lookup"><span data-stu-id="d63da-128">You can also set up reason codes for individual warehouses and for products.</span></span> <span data-ttu-id="d63da-129">产品的原因代码设置可以忽略仓库的设置。</span><span class="sxs-lookup"><span data-stu-id="d63da-129">The reason code setup for products can disregard the setup for warehouses.</span></span>

## <a name="mandatory-reason-codes"></a><span data-ttu-id="d63da-130">必需原因代码</span><span class="sxs-lookup"><span data-stu-id="d63da-130">Mandatory reason codes</span></span>

<span data-ttu-id="d63da-131">如果在仓库或物料的原因代码配置中设置了**必需**参数，则提供原因代码之前，不能完成和结束盘点日记帐。</span><span class="sxs-lookup"><span data-stu-id="d63da-131">If the **Mandatory** parameter is set in the configuration of reason codes for warehouses or items, the counting journal can't be completed and closed until a reason code is provided.</span></span>

### <a name="set-up-reason-codes-for-warehouses"></a><span data-ttu-id="d63da-132">设置仓库的原因代码</span><span class="sxs-lookup"><span data-stu-id="d63da-132">Set up reason codes for warehouses</span></span>

1. <span data-ttu-id="d63da-133">选择**库存管理** \> **设置** \> **库存细分** \> **仓库**。</span><span class="sxs-lookup"><span data-stu-id="d63da-133">Select **Inventory Management** \> **Setup** \> **Inventory breakdown** \> **Warehouses**.</span></span>
2. <span data-ttu-id="d63da-134">在**仓库**选项卡上的**盘点原因代码策略**字段中，选择以下选项之一：</span><span class="sxs-lookup"><span data-stu-id="d63da-134">On the **Warehouse** tab, in the **Counting reason code policy** field, select one of the following options:</span></span>

    - <span data-ttu-id="d63da-135">**空白** – 为物料设置的参数用于确定盘点日记帐是否是产品必需的。</span><span class="sxs-lookup"><span data-stu-id="d63da-135">**Blank** – The parameter that is set up for the item is used to determine whether counting journals are mandatory for the product.</span></span>
    - <span data-ttu-id="d63da-136">**必需** – 仓库的盘点日记帐始终需要原因代码。</span><span class="sxs-lookup"><span data-stu-id="d63da-136">**Mandatory** – A reason code is always required on counting journals for the warehouse.</span></span>
    - <span data-ttu-id="d63da-137">**可选** – 原因代码不是仓库的盘点日记帐必需的。</span><span class="sxs-lookup"><span data-stu-id="d63da-137">**Optional** – A reason code isn't required on counting journals for the warehouse.</span></span>

### <a name="set-up-reason-codes-for-products"></a><span data-ttu-id="d63da-138">设置产品的原因代码</span><span class="sxs-lookup"><span data-stu-id="d63da-138">Set up reason codes for products</span></span>

1. <span data-ttu-id="d63da-139">选择**产品信息管理** \> **产品** \> **已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="d63da-139">Select **Product information management** \> **Products** \> **Released products**.</span></span>
2. <span data-ttu-id="d63da-140">在**产品**选项卡上，选择**盘点原因代码策略**，然后选择以下选项之一：</span><span class="sxs-lookup"><span data-stu-id="d63da-140">On the **Product** tab, select **Counting reason code policy**, and then select one of the following options:</span></span>

    - <span data-ttu-id="d63da-141">**空白** – 为仓库设置的参数用于确定盘点日记帐是否是产品必需的。</span><span class="sxs-lookup"><span data-stu-id="d63da-141">**Blank** – The parameter that is set up for the warehouse is used to determine whether counting journals are mandatory for the product.</span></span>
    - <span data-ttu-id="d63da-142">**必需** – 产品的盘点日记帐始终需要原因代码。</span><span class="sxs-lookup"><span data-stu-id="d63da-142">**Mandatory** – A reason code is always required on counting journals for the product.</span></span> <span data-ttu-id="d63da-143">此设置替代仓库级别的所有原因代码设置。</span><span class="sxs-lookup"><span data-stu-id="d63da-143">This setting overrides any reason code setting at the warehouse level.</span></span>
    - <span data-ttu-id="d63da-144">**可选** – 原因代码不是产品的盘点日记帐必需的。</span><span class="sxs-lookup"><span data-stu-id="d63da-144">**Optional** – A reason code isn't required on counting journals for the product.</span></span> <span data-ttu-id="d63da-145">此设置替代仓库级别的所有原因代码设置。</span><span class="sxs-lookup"><span data-stu-id="d63da-145">This setting overrides any reason code setting at the warehouse level.</span></span>

### <a name="use-reason-codes-in-counting-journals"></a><span data-ttu-id="d63da-146">在盘点日记帐中使用原因代码</span><span class="sxs-lookup"><span data-stu-id="d63da-146">Use reason codes in counting journals</span></span>

<span data-ttu-id="d63da-147">在盘点日记帐中，可为以下类型的盘点添加原因代码：</span><span class="sxs-lookup"><span data-stu-id="d63da-147">In a counting journal, you can add reason codes for counts of the following types:</span></span>

- <span data-ttu-id="d63da-148">周期盘点</span><span class="sxs-lookup"><span data-stu-id="d63da-148">Cycle Count</span></span>
- <span data-ttu-id="d63da-149">现货盘点</span><span class="sxs-lookup"><span data-stu-id="d63da-149">Spot Count</span></span>
- <span data-ttu-id="d63da-150">阈值盘点</span><span class="sxs-lookup"><span data-stu-id="d63da-150">Threshold Count</span></span>
- <span data-ttu-id="d63da-151">调入</span><span class="sxs-lookup"><span data-stu-id="d63da-151">Adjustment In</span></span>
- <span data-ttu-id="d63da-152">调出</span><span class="sxs-lookup"><span data-stu-id="d63da-152">Adjustment Out</span></span>

<span data-ttu-id="d63da-153">将把原因代码添加到**盘点日记帐**类型的盘点日记帐中的日记帐行。</span><span class="sxs-lookup"><span data-stu-id="d63da-153">Reason codes are added to the journal lines in counting journals of the **Counting journal** type.</span></span>

1. <span data-ttu-id="d63da-154">选择**库存管理** \> **日记帐条目** \> **物料盘点** \> **盘点**。</span><span class="sxs-lookup"><span data-stu-id="d63da-154">Select **Inventory management** \> **Journal entries** \> **Item counting** \> **Counting**.</span></span>
2. <span data-ttu-id="d63da-155">在盘点日记帐行明细的**盘点原因代码**字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="d63da-155">In the line details of the counting journal, in the **Counting reason code** field, select an option.</span></span>

### <a name="view-the-counting-history-as-its-recorded-by-reason-codes"></a><span data-ttu-id="d63da-156">查看原因代码记录的盘点历史记录。</span><span class="sxs-lookup"><span data-stu-id="d63da-156">View the counting history as it's recorded by reason codes</span></span>

- <span data-ttu-id="d63da-157">选择**库存管理** \> **查询和报表** \> **盘点历史记录**，然后在**盘点原因代码**字段中查看已通过原因代码记录的盘点历史记录。</span><span class="sxs-lookup"><span data-stu-id="d63da-157">Select **Inventory management** \> **Inquiries and reports** \> **Counting history**, and then, in the **Counting reason code** field, view the counting history that has been recorded through a reason code.</span></span>

### <a name="use-a-reason-code-for-a-quantity-adjustment"></a><span data-ttu-id="d63da-158">将原因代码用于数量调整</span><span class="sxs-lookup"><span data-stu-id="d63da-158">Use a reason code for a quantity adjustment</span></span>

1. <span data-ttu-id="d63da-159">在**现货库存**页中，选择**调整数量**。</span><span class="sxs-lookup"><span data-stu-id="d63da-159">On the **On-hand inventory** page, select **Adjust quantity**.</span></span> <span data-ttu-id="d63da-160">可通过多种方法打开**现货库存**页。</span><span class="sxs-lookup"><span data-stu-id="d63da-160">You can open the **On-hand inventory** page in several ways.</span></span> <span data-ttu-id="d63da-161">例如，选择**库存管理** \> **查询和报表** \> **现货库存**。</span><span class="sxs-lookup"><span data-stu-id="d63da-161">For example, select **Inventory management** \> **Inquiries and reports** \> **On-hand inventory**.</span></span>
2. <span data-ttu-id="d63da-162">选择**调整数量**，然后在**盘点原因代码**字段中选择一个原因代码。</span><span class="sxs-lookup"><span data-stu-id="d63da-162">Select **Adjust quantity**, and then, in the **Counting reason code** field, select a reason code.</span></span>

### <a name="configure-reason-codes-for-mobile-device-menu-items"></a><span data-ttu-id="d63da-163">为移动设备菜单项配置原因代码</span><span class="sxs-lookup"><span data-stu-id="d63da-163">Configure reason codes for mobile device menu items</span></span>

<span data-ttu-id="d63da-164">可在移动设备菜单项上为任何类型的盘点配置原因代码。</span><span class="sxs-lookup"><span data-stu-id="d63da-164">You can configure reason codes for any type of count on a mobile device menu item.</span></span> <span data-ttu-id="d63da-165">移动设备菜单项的配置中包含以下信息：</span><span class="sxs-lookup"><span data-stu-id="d63da-165">The configuration of the mobile device menu item includes the following information:</span></span>

- <span data-ttu-id="d63da-166">盘点期间是否对移动设备工作人员显示原因代码。</span><span class="sxs-lookup"><span data-stu-id="d63da-166">Whether the reason code is shown to the mobile device worker during counting.</span></span>
- <span data-ttu-id="d63da-167">移动设备菜单项中显示的默认原因代码。</span><span class="sxs-lookup"><span data-stu-id="d63da-167">The default reason code that is shown on a mobile device menu item.</span></span>
- <span data-ttu-id="d63da-168">用户是否可以编辑原因代码。</span><span class="sxs-lookup"><span data-stu-id="d63da-168">Whether the user can edit the reason code.</span></span>

### <a name="set-up-reason-codes-on-a-mobile-device"></a><span data-ttu-id="d63da-169">设置移动设备上的原因代码</span><span class="sxs-lookup"><span data-stu-id="d63da-169">Set up reason codes on a mobile device</span></span>

1. <span data-ttu-id="d63da-170">选择**仓库管理** \> **设置** \> **移动设备** \> **移动设备菜单项**。</span><span class="sxs-lookup"><span data-stu-id="d63da-170">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>
2. <span data-ttu-id="d63da-171">在**周期盘点**选项卡上，选择**周期盘点**。</span><span class="sxs-lookup"><span data-stu-id="d63da-171">On the **Cycle count** tab, select **Cycle counting**.</span></span>
3. <span data-ttu-id="d63da-172">在**默认盘点原因代码**字段中，设置通过使用移动设备菜单项执行盘点时应记录的默认原因代码。</span><span class="sxs-lookup"><span data-stu-id="d63da-172">In the **Default counting reason code** field, set the default reason code that should be recorded when counting is done by using the mobile device menu item.</span></span>
4. <span data-ttu-id="d63da-173">在**显示盘点原因代码**字段中，选择**行**，以便在记录每个变型之后显示原因代码。</span><span class="sxs-lookup"><span data-stu-id="d63da-173">In the **Display counting reason code** field, select **Line** to show the reason code after each variance is recorded.</span></span> <span data-ttu-id="d63da-174">也可以在不应显示原因代码时选择**隐藏**。</span><span class="sxs-lookup"><span data-stu-id="d63da-174">Alternatively, select **Hide** if the reason code shouldn't be shown.</span></span>
5. <span data-ttu-id="d63da-175">将**编辑盘点原因代码**选项设置为**是**或**否**。</span><span class="sxs-lookup"><span data-stu-id="d63da-175">Set the **Edit counting reason code** option to either **Yes** or **No**.</span></span> <span data-ttu-id="d63da-176">如果将此选项设置为**是**，则工作人员可以编辑盘点期间移动设备上显示的原因代码。</span><span class="sxs-lookup"><span data-stu-id="d63da-176">If you set this option to **Yes**, the worker can edit the reason code when it's shown on the mobile device during counting.</span></span>

> [!NOTE]
> <span data-ttu-id="d63da-177">可在可执行盘点的任何移动设备菜单项上启用**周期盘点**按钮。</span><span class="sxs-lookup"><span data-stu-id="d63da-177">The **Cycle counting** button can be enabled on any mobile device menu item where counting can be done.</span></span> <span data-ttu-id="d63da-178">例如，现场盘点、用户导向的工作和系统导向的工作的菜单项。</span><span class="sxs-lookup"><span data-stu-id="d63da-178">Example include the menu items for spot counts, user-directed work, and system-directed work.</span></span>

## <a name="cycle-count-approvals"></a><span data-ttu-id="d63da-179">周期盘点审核</span><span class="sxs-lookup"><span data-stu-id="d63da-179">Cycle count approvals</span></span>

<span data-ttu-id="d63da-180">审核盘点之前，用户可更改与盘点关联的原因代码。</span><span class="sxs-lookup"><span data-stu-id="d63da-180">Before a count is approved, the user can change the reason code that is associated with the count.</span></span> <span data-ttu-id="d63da-181">审核盘点时，将把原因代码输入盘点日记帐行中。</span><span class="sxs-lookup"><span data-stu-id="d63da-181">When the count is approved, the reason code is entered on the counting journal lines.</span></span>

### <a name="modify-cycle-count-approvals"></a><span data-ttu-id="d63da-182">修改周期盘点审核</span><span class="sxs-lookup"><span data-stu-id="d63da-182">Modify cycle count approvals</span></span>

1. <span data-ttu-id="d63da-183">选择**仓库管理** \> **周期盘点** \> **周期盘点工作待审阅**。</span><span class="sxs-lookup"><span data-stu-id="d63da-183">Select **Warehouse management** \> **Cycle counting** \> **Cycle count work pending review**.</span></span>
2. <span data-ttu-id="d63da-184">选择**周期盘点**，然后在**原因代码**字段中选择一个新原因代码。</span><span class="sxs-lookup"><span data-stu-id="d63da-184">Select **Cycle counting**, and then, in the **Reason code** field, select a new reason code.</span></span>

### <a name="modify-the-mobile-device-menu-item-for-adjustment-in-and-adjustment-out"></a><span data-ttu-id="d63da-185">修改调入和调出的移动设备菜单项</span><span class="sxs-lookup"><span data-stu-id="d63da-185">Modify the mobile device menu item for Adjustment in and Adjustment out</span></span>

1. <span data-ttu-id="d63da-186">选择**仓库管理** \> **设置** \> **移动设备** \> **移动设备菜单项**，然后选择**调入和调出**。</span><span class="sxs-lookup"><span data-stu-id="d63da-186">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**, and then select **Adjustment in and out**.</span></span>
2. <span data-ttu-id="d63da-187">将**使用现有工作**选项设置为**否**。</span><span class="sxs-lookup"><span data-stu-id="d63da-187">Set the **Use existing work** option to **No**.</span></span>
3. <span data-ttu-id="d63da-188">在**工作创建流程**字段中，选择**调入**。</span><span class="sxs-lookup"><span data-stu-id="d63da-188">In the **Work creation process** field, select **Adjustment in**.</span></span>

<span data-ttu-id="d63da-189">工作创建流程中选择了**调入**或**调出**时，将把以下字段添加到移动设备菜单项：</span><span class="sxs-lookup"><span data-stu-id="d63da-189">The following fields will be added to the mobile device menu item when **Adjustment in** or **Adjustment out** is selected during the work creation process:</span></span>

- <span data-ttu-id="d63da-190">默认盘点原因代码</span><span class="sxs-lookup"><span data-stu-id="d63da-190">Default counting reason code</span></span>
- <span data-ttu-id="d63da-191">显示盘点原因代码</span><span class="sxs-lookup"><span data-stu-id="d63da-191">Display counting reason code</span></span>
- <span data-ttu-id="d63da-192">编辑盘点原因代码</span><span class="sxs-lookup"><span data-stu-id="d63da-192">Edit counting reason code</span></span>

