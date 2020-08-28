---
title: 波次期间的高级负荷计划
description: 本主题介绍高级波次负荷计划功能，这会在波次执行期间自动为现有波次分配装运。 因此，可以创建有意义的负荷来表示卡车，而不必使用负荷计划工作台。
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPostMethod,WHSWaveTemplateTable,WHSLoadMixGroup,WHSLoadBuildTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 3bc82c3af2b99303a650f672f2b2ccd48c9889a9
ms.sourcegitcommit: d25d0feb3f8a5a760eba50ba5f46e1db02737d25
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/10/2020
ms.locfileid: "3677426"
---
# <a name="advanced-load-building-during-wave"></a><span data-ttu-id="85496-104">波次期间的高级负荷计划</span><span class="sxs-lookup"><span data-stu-id="85496-104">Advanced load building during wave</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85496-105">高级波次负荷计划功能在波次执行期间自动为现有波次分配装运。</span><span class="sxs-lookup"><span data-stu-id="85496-105">Advanced wave load building automatically assigns shipments to existing waves during wave execution.</span></span> <span data-ttu-id="85496-106">因此，可以创建有意义的负荷来表示卡车，而不必使用负荷计划工作台。</span><span class="sxs-lookup"><span data-stu-id="85496-106">Therefore, you can create meaningful loads that represent trucks without having to use the load planning workbench.</span></span> <span data-ttu-id="85496-107">对于希望使用负荷这个概念来跟踪和规划卡车/拖车中的货物的装运，但是不希望每天手动创建这些负荷的企业，此功能非常有用。</span><span class="sxs-lookup"><span data-stu-id="85496-107">This capability is useful for businesses that want to use the concept of loads to track and plan the shipment of goods in a truck/trailer, but that don't want to manually create those loads every day.</span></span>

<span data-ttu-id="85496-108">在波次处理期间，系统通常为尚未获得负荷的每个装运创建一个新装运。</span><span class="sxs-lookup"><span data-stu-id="85496-108">During wave processing, the system usually creates a new load for each shipment that no load is assigned to.</span></span> <span data-ttu-id="85496-109">但是，如果开启了高级波次负荷计划功能，系统将把每个未分配的装运分配给一个现有负荷（如果存在适合的负荷），并且仅在需要时才创建新负荷。</span><span class="sxs-lookup"><span data-stu-id="85496-109">However, when advanced wave load building is turned on, the system assigns each unassigned shipment to an existing load (if an appropriate load exists), and new loads are created only when they are required.</span></span> <span data-ttu-id="85496-110">高级波次负荷计划功能根据您定义的条件自动创建新负荷。</span><span class="sxs-lookup"><span data-stu-id="85496-110">Advanced wave load building automatically creates the new loads, based on criteria that you define.</span></span>

<span data-ttu-id="85496-111">若要使用此功能，必须按照下面的方法设置系统：</span><span class="sxs-lookup"><span data-stu-id="85496-111">To use the feature, you must set up the system in the following way:</span></span>

- <span data-ttu-id="85496-112">创建其中包含新的 **buildLoads** 方法的*波次模板*。</span><span class="sxs-lookup"><span data-stu-id="85496-112">Create *wave templates* that include the new **buildLoads** method.</span></span> <span data-ttu-id="85496-113">此方法让高级波次负荷计划功能可用于使用这些模板的波次。</span><span class="sxs-lookup"><span data-stu-id="85496-113">This method makes advanced wave load building available for waves that use those templates.</span></span>
- <span data-ttu-id="85496-114">设置*负荷计划模板*，这些模板中的每一个都链接到一个特定波次模板和方法。</span><span class="sxs-lookup"><span data-stu-id="85496-114">Set up *load build templates*, each of which is linked to a specific wave template and method.</span></span> <span data-ttu-id="85496-115">负荷计划模板控制将正在分波次的负荷行添加到哪个（现有或新）负荷。</span><span class="sxs-lookup"><span data-stu-id="85496-115">Load build templates control which load (existing or new) the load lines that are being waved are added to.</span></span> <span data-ttu-id="85496-116">可以根据条件（如负荷行中的负荷模板、设备和其他值）合并或拆分装运。</span><span class="sxs-lookup"><span data-stu-id="85496-116">You can combine or separate shipments, based on criteria such as the load template, equipment, and other field values on the load line.</span></span>
- <span data-ttu-id="85496-117">定义*负荷混合组*以控制应该和不应该将哪些物料合并到单个负荷中。</span><span class="sxs-lookup"><span data-stu-id="85496-117">Define *load mix groups* to control which items should and should not be combined on a single load.</span></span> <span data-ttu-id="85496-118">也可以指定此限制应计划警告还是错误，以及是否应该评估负荷模板的体积限制。</span><span class="sxs-lookup"><span data-stu-id="85496-118">You also specify whether the restriction should produce a warning or an error, and whether the volumetric restriction of the load template should be evaluated.</span></span>

## <a name="turn-on-advanced-wave-load-building-in-your-system"></a><span data-ttu-id="85496-119">在系统中开启高级波次负荷计划功能</span><span class="sxs-lookup"><span data-stu-id="85496-119">Turn on advanced wave load building in your system</span></span>

<span data-ttu-id="85496-120">必须先在系统中开启两项功能，才能使用高级波次负荷计划功能。</span><span class="sxs-lookup"><span data-stu-id="85496-120">Before you can use advanced wave load building, two features must be turned on in your system.</span></span> <span data-ttu-id="85496-121">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查这些功能的状态，并在需要这些功能时将其开启。</span><span class="sxs-lookup"><span data-stu-id="85496-121">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of these features and turn them on if they are required.</span></span> <span data-ttu-id="85496-122">在**功能管理**工作区中，这些功能按照下面的方式列出：</span><span class="sxs-lookup"><span data-stu-id="85496-122">In the **Feature management** workspace, the features are listed in the following way:</span></span>

- <span data-ttu-id="85496-123">波次负荷计划功能：</span><span class="sxs-lookup"><span data-stu-id="85496-123">Wave load building feature:</span></span>

    - <span data-ttu-id="85496-124">**模块**：*仓库管理*</span><span class="sxs-lookup"><span data-stu-id="85496-124">**Module:** *Warehouse management*</span></span>
    - <span data-ttu-id="85496-125">**功能名称**：*波次负荷计划功能*</span><span class="sxs-lookup"><span data-stu-id="85496-125">**Feature name:** *Wave load building feature*</span></span>

- <span data-ttu-id="85496-126">组织范围内的波次步骤代码：</span><span class="sxs-lookup"><span data-stu-id="85496-126">Organization wide wave step code:</span></span>

    - <span data-ttu-id="85496-127">**模块**：*仓库管理*</span><span class="sxs-lookup"><span data-stu-id="85496-127">**Module:** *Warehouse management*</span></span>
    - <span data-ttu-id="85496-128">**功能名称**：*组织范围内的波次步骤代码*</span><span class="sxs-lookup"><span data-stu-id="85496-128">**Feature name:** *Organization wide wave step code*</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="85496-129">提供示例数据</span><span class="sxs-lookup"><span data-stu-id="85496-129">Make sample data available</span></span>

<span data-ttu-id="85496-130">若要使用此处指定的示例记录和值完成此演示，使用的系统中必须已安装标准[演示数据](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="85496-130">To work through this demo by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="85496-131">此外，开始前，还必须选择 **USMF** 法人。</span><span class="sxs-lookup"><span data-stu-id="85496-131">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="85496-132">使用生产系统时，也可以将此演示用作使用此功能的指导。</span><span class="sxs-lookup"><span data-stu-id="85496-132">You can also use this demo as guidance for using this feature when you work on a production system.</span></span> <span data-ttu-id="85496-133">但是，在此情况下，必须替换为您自己的值，而您可能会缺少标准演示数据提供的某些类型的必需记录。</span><span class="sxs-lookup"><span data-stu-id="85496-133">However, in that case, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="make-sure-that-the-scenario-setup-includes-enough-available-inventory"></a><span data-ttu-id="85496-134">确保场景设置中包含足够的可用库存</span><span class="sxs-lookup"><span data-stu-id="85496-134">Make sure that the scenario setup includes enough available inventory</span></span>

<span data-ttu-id="85496-135">如果要使用 **USMF** 演示数据，必须先确保已将系统设置为每个相关货位有足够的库存。</span><span class="sxs-lookup"><span data-stu-id="85496-135">If you're working with the **USMF** demo data, you must first make sure that your system is set up so that there is enough inventory at each relevant location.</span></span> <span data-ttu-id="85496-136">对于此演示，预计仓库 *62* 中有以下库存：</span><span class="sxs-lookup"><span data-stu-id="85496-136">For this demo, the expectation is that the following inventory is available in warehouse *62*:</span></span>

- <span data-ttu-id="85496-137">**物料 A0001：** 10 件</span><span class="sxs-lookup"><span data-stu-id="85496-137">**Item A0001:** 10 pcs</span></span>
- <span data-ttu-id="85496-138">**物料 A0002：** 10 件</span><span class="sxs-lookup"><span data-stu-id="85496-138">**Item A0002:** 10 pcs</span></span>
- <span data-ttu-id="85496-139">**物料 M9200：** 10 个</span><span class="sxs-lookup"><span data-stu-id="85496-139">**Item M9200:** 10 ea</span></span>

<span data-ttu-id="85496-140">必须将物料 **M9200** 添加到该仓库。</span><span class="sxs-lookup"><span data-stu-id="85496-140">Item **M9200** must be added to the warehouse.</span></span> <span data-ttu-id="85496-141">完成以下小节中的过程以添加物料库存。</span><span class="sxs-lookup"><span data-stu-id="85496-141">Complete the procedures in the following subsections to add the item inventory.</span></span>

#### <a name="create-a-new-license-plate-id"></a><span data-ttu-id="85496-142">创建新的牌照 ID</span><span class="sxs-lookup"><span data-stu-id="85496-142">Create a new license plate ID</span></span>

1. <span data-ttu-id="85496-143">转到**仓库管理** \> **设置** \> **仓库** \> **牌照**。</span><span class="sxs-lookup"><span data-stu-id="85496-143">Go to **Warehouse management** \> **Setup** \> **Warehouse** \> **License plates**.</span></span>
1. <span data-ttu-id="85496-144">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="85496-144">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="85496-145">在新行的**牌照**字段中，输入 *LP6203*。</span><span class="sxs-lookup"><span data-stu-id="85496-145">In the new row, in the **License plate** field, enter *LP6203*.</span></span>
1. <span data-ttu-id="85496-146">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="85496-146">Select **Save**.</span></span>

#### <a name="create-a-standard-cost-for-item-m9200-in-site-6"></a><span data-ttu-id="85496-147">在地点 6 中为物料 M9200 创建标准成本</span><span class="sxs-lookup"><span data-stu-id="85496-147">Create a standard cost for item M9200 in site 6</span></span>

1. <span data-ttu-id="85496-148">转到**产品信息管理** \> **产品** \> **已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="85496-148">Go to **Product information management** \> **Products** \> **Released products**.</span></span>
1. <span data-ttu-id="85496-149">搜索 **M9200**。</span><span class="sxs-lookup"><span data-stu-id="85496-149">Search on **M9200**.</span></span>
1. <span data-ttu-id="85496-150">搜索行以查找该物料，然后在操作窗格中**管理成本**选项卡上**设置**组中，选择**物料价格**。</span><span class="sxs-lookup"><span data-stu-id="85496-150">Select the row for the item, and then, on the Action Pane, on the **Manage costs** tab, in the **Set up** group, select **Item price**.</span></span>
1. <span data-ttu-id="85496-151">在**物料价格**页中，选择**未决价格**选项卡。</span><span class="sxs-lookup"><span data-stu-id="85496-151">On the **Item price** page, select the **Pending prices** tab.</span></span>
1. <span data-ttu-id="85496-152">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="85496-152">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="85496-153">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="85496-153">On the new line, set the following values:</span></span>

    - <span data-ttu-id="85496-154">**成本计算类型**：*计划成本*</span><span class="sxs-lookup"><span data-stu-id="85496-154">**Costing type:** *Planned cost*</span></span>
    - <span data-ttu-id="85496-155">**价格类型**：*成本*</span><span class="sxs-lookup"><span data-stu-id="85496-155">**Price type:** *Cost*</span></span>
    - <span data-ttu-id="85496-156">**版本**：*10*</span><span class="sxs-lookup"><span data-stu-id="85496-156">**Version:** *10*</span></span>
    - <span data-ttu-id="85496-157">**站点**：*6*</span><span class="sxs-lookup"><span data-stu-id="85496-157">**Site:** *6*</span></span>
    - <span data-ttu-id="85496-158">**价格**：*1.60*</span><span class="sxs-lookup"><span data-stu-id="85496-158">**Price:** *1.60*</span></span>

1. <span data-ttu-id="85496-159">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="85496-159">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="85496-160">在操作窗格上，选择**激活未决价格**。</span><span class="sxs-lookup"><span data-stu-id="85496-160">On the Action Pane, select **Activate pending price(s)**.</span></span>
1. <span data-ttu-id="85496-161">选择**有效价格**选项卡以验证是否已添加了地点 *6* 的新成本价。</span><span class="sxs-lookup"><span data-stu-id="85496-161">Select the **Active prices** tab to verify that the new cost price for site *6* has been added.</span></span>

#### <a name="create-inventory-in-warehouse-62"></a><span data-ttu-id="85496-162">创建仓库 62 中的库存</span><span class="sxs-lookup"><span data-stu-id="85496-162">Create inventory in warehouse 62</span></span>

1. <span data-ttu-id="85496-163">转到**库存管理** \> **日记帐条目** \> **物料** \> **库存调整**。</span><span class="sxs-lookup"><span data-stu-id="85496-163">Go to **Inventory management** \> **Journal entries** \> **Items** \> **Inventory adjustment**.</span></span>
1. <span data-ttu-id="85496-164">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="85496-164">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="85496-165">在**创建库存日记帐**对话框中**概览**快速选项卡上的**仓库**字段中，输入 *62*。</span><span class="sxs-lookup"><span data-stu-id="85496-165">In the **Create inventory journal** dialog box, on the **Overview** FastTab, in the **Warehouse** field, enter *62*.</span></span> <span data-ttu-id="85496-166">接受其他所有字段中的默认值。</span><span class="sxs-lookup"><span data-stu-id="85496-166">Accept the default values in all the other fields.</span></span>
1. <span data-ttu-id="85496-167">选择**确定**关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="85496-167">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="85496-168">将打开**库存调整**页。</span><span class="sxs-lookup"><span data-stu-id="85496-168">The **Inventory adjustment** page is opened.</span></span> <span data-ttu-id="85496-169">在**日记帐行**快速选项卡上，选择**新建**添加行。</span><span class="sxs-lookup"><span data-stu-id="85496-169">On the **Journal lines** FastTab, select **New** to add a line.</span></span>
1. <span data-ttu-id="85496-170">在新行中，设置以下值。</span><span class="sxs-lookup"><span data-stu-id="85496-170">On the new line, set the following values.</span></span> <span data-ttu-id="85496-171">接受其他所有字段中的默认值。</span><span class="sxs-lookup"><span data-stu-id="85496-171">Accept the default values in all the other fields.</span></span>

    - <span data-ttu-id="85496-172">\**物料编号：\*\*\*M9200*</span><span class="sxs-lookup"><span data-stu-id="85496-172">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="85496-173">**货位**：*bulk-003*</span><span class="sxs-lookup"><span data-stu-id="85496-173">**Location:** *bulk-003*</span></span>
    - <span data-ttu-id="85496-174">**数量：** 将值更改为 *10*。</span><span class="sxs-lookup"><span data-stu-id="85496-174">**Quantity:** Change the value to *10*.</span></span>

1. <span data-ttu-id="85496-175">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="85496-175">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="85496-176">在操作窗格上，选择**验证**检查是否有错误。</span><span class="sxs-lookup"><span data-stu-id="85496-176">On the Action Pane, select **Validate** to check for errors.</span></span>
1. <span data-ttu-id="85496-177">在**检查日记帐**对话框中，选择**确定**开始进行检查。</span><span class="sxs-lookup"><span data-stu-id="85496-177">In the **Check journal** dialog box, select **OK** to start the check.</span></span> <span data-ttu-id="85496-178">检查完成后，您会收到一条消息。</span><span class="sxs-lookup"><span data-stu-id="85496-178">You receive a message when the check is completed.</span></span>
1. <span data-ttu-id="85496-179">在操作窗格上，选择**过帐**提交库存调整。</span><span class="sxs-lookup"><span data-stu-id="85496-179">On the Action Pane, select **Post** to commit the inventory adjustment.</span></span>
1. <span data-ttu-id="85496-180">在**过帐日记帐**对话框中，选择**确定**开始进行过帐。</span><span class="sxs-lookup"><span data-stu-id="85496-180">In the **Post journal** dialog box, select **OK** to start the posting.</span></span> <span data-ttu-id="85496-181">过帐完成后，您会收到一条消息。</span><span class="sxs-lookup"><span data-stu-id="85496-181">You receive a message when the posting is completed.</span></span>

## <a name="set-up-advanced-wave-load-building"></a><span data-ttu-id="85496-182">设置高级波次负荷计划功能</span><span class="sxs-lookup"><span data-stu-id="85496-182">Set up advanced wave load building</span></span>

### <a name="regenerate-wave-process-methods"></a><span data-ttu-id="85496-183">重新计划波次处理方法</span><span class="sxs-lookup"><span data-stu-id="85496-183">Regenerate wave process methods</span></span>

<span data-ttu-id="85496-184">可能必须重新计划波次处理方法，才能使用负荷计划方法 (**buildLoads**)。</span><span class="sxs-lookup"><span data-stu-id="85496-184">You might have to regenerate your wave process methods to make the load building method (**buildLoads**) available.</span></span>

1. <span data-ttu-id="85496-185">转到**仓库管理** \> **设置** \> **波次** \> **波次处理方法**。</span><span class="sxs-lookup"><span data-stu-id="85496-185">Go to **Warehouse management** \> **Setup** \> **Waves** \> **Wave process methods**.</span></span>
2. <span data-ttu-id="85496-186">验证列表中是否有 **buildLoads**。</span><span class="sxs-lookup"><span data-stu-id="85496-186">Verify that **buildLoads** is present in the list.</span></span> <span data-ttu-id="85496-187">如果没有，请在操作窗格中选择**重新计划方法**添加该方法。</span><span class="sxs-lookup"><span data-stu-id="85496-187">If it isn't present, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="set-up-wave-templates"></a><span data-ttu-id="85496-188">设置波次模板</span><span class="sxs-lookup"><span data-stu-id="85496-188">Set up wave templates</span></span>

<span data-ttu-id="85496-189">每个相关[波次模板](tasks/configure-wave-processing.md)中都必须包含 **buildLoads** 方法，才能利用高级波次负荷计划功能。</span><span class="sxs-lookup"><span data-stu-id="85496-189">To take advantage of advanced wave load building, you must include the **buildLoads** method in each relevant [wave template](tasks/configure-wave-processing.md).</span></span>

1. <span data-ttu-id="85496-190">转到**仓库管理** \> **设置** \> **波次** \> **波次模板**。</span><span class="sxs-lookup"><span data-stu-id="85496-190">Go to **Warehouse management** \> **Setup** \> **Waves** \> **Wave templates**.</span></span>
1. <span data-ttu-id="85496-191">选择一个波次模板。</span><span class="sxs-lookup"><span data-stu-id="85496-191">Select a wave template.</span></span>

    <span data-ttu-id="85496-192">如果在使用 **USMF** 演示数据，请选择 **62 装运默认**模板。</span><span class="sxs-lookup"><span data-stu-id="85496-192">If you're working with the **USMF** demo data, select the **62 Shipping Default** template.</span></span>

1. <span data-ttu-id="85496-193">在操作窗格上，选择**编辑**将页面设置为编辑模式。</span><span class="sxs-lookup"><span data-stu-id="85496-193">On the Action Pane, select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="85496-194">在**方法**快速选项卡上的**其余方法**网格中，选择 **buildLoads** 方法。</span><span class="sxs-lookup"><span data-stu-id="85496-194">On the **Methods** FastTab, in the **Remaining methods** grid, select the **buildLoads** method.</span></span>
1. <span data-ttu-id="85496-195">选择向右箭头按钮将 **buildLoads** 方法移到**已选定方法**网格中。</span><span class="sxs-lookup"><span data-stu-id="85496-195">Select the right arrow button to move the **buildLoads** method to the **Selected methods** grid.</span></span>
1. <span data-ttu-id="85496-196">若要分配 **buildLoads** 方法的**波次步骤代码**值，首先必须在**波次步骤代码**页中创建一个代码。</span><span class="sxs-lookup"><span data-stu-id="85496-196">To assign a **Wave step code** value for the **buildLoads** method, you must first create a code on the **Wave step codes** page.</span></span> <span data-ttu-id="85496-197">可以使用所需的任何值，但请务必记下该值，因为后面需要该值。</span><span class="sxs-lookup"><span data-stu-id="85496-197">You can use any value that you want, but be sure to make a note of it, because you will need it later.</span></span> <span data-ttu-id="85496-198">执行以下步骤创建代码 **WSC2112**：</span><span class="sxs-lookup"><span data-stu-id="85496-198">Follow these steps to create code **WSC2112**:</span></span>

    1. <span data-ttu-id="85496-199">在 **buildLoads** 方法的行中，右键单击**波次步骤代码**字段中的向下箭头，然后选择**查看详细信息**。</span><span class="sxs-lookup"><span data-stu-id="85496-199">In the row for the **buildLoads** method, right-click the down arrow in the **Wave step code** field, and then select **View details**.</span></span>
    1. <span data-ttu-id="85496-200">在**波次步骤代码**页的操作窗格中，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="85496-200">On the **Wave step codes** page, on the Action Pane, select **New**.</span></span>
    1. <span data-ttu-id="85496-201">在**波次步骤代码**字段中，输入 *WSC2112*。</span><span class="sxs-lookup"><span data-stu-id="85496-201">In the **Wave step code** field, enter *WSC2112*.</span></span>
    1. <span data-ttu-id="85496-202">在**波次步骤说明**字段中，输入 *WSC2112*。</span><span class="sxs-lookup"><span data-stu-id="85496-202">In the **Wave step description** field, enter *WSC2112*.</span></span>
    1. <span data-ttu-id="85496-203">在**波次步骤类型**字段中，选择*负荷计划*。</span><span class="sxs-lookup"><span data-stu-id="85496-203">In the **Wave step type** field, select *Load Building*.</span></span>

1. <span data-ttu-id="85496-204">选择**保存**，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="85496-204">Select **Save**, and close the page.</span></span>
1. <span data-ttu-id="85496-205">在 **buildLoads** 方法的行中**波次步骤代码**字段内，选择刚才创建的代码 (**WSC2112**)。</span><span class="sxs-lookup"><span data-stu-id="85496-205">In the row for the **buildLoads** method, in the **Wave step code** field, select the code that you just created (**WSC2112**).</span></span>
1. <span data-ttu-id="85496-206">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="85496-206">On the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="85496-207">波次步骤代码是用户可设置并用于将特定波次方法实例链接到相应模板的代码。</span><span class="sxs-lookup"><span data-stu-id="85496-207">Wave step codes are codes that users can set up and use to link specific instances of wave methods to corresponding templates.</span></span> <span data-ttu-id="85496-208">模板包括用于补货、集装化、标签打印、装载计划和排序的模板。</span><span class="sxs-lookup"><span data-stu-id="85496-208">The templates include templates for replenishment, containerization, label printing, load building, and sorting.</span></span>
>
> <span data-ttu-id="85496-209">如果不使用波次步骤代码，用户必须输入普通文本才能引用来自波次方法实例的特定模板。</span><span class="sxs-lookup"><span data-stu-id="85496-209">When wave step codes aren't used, users must enter free text to reference a specific template from the wave method instance.</span></span> <span data-ttu-id="85496-210">普通文本容易出错，因为用户必须确保其为波次模板中的特定波次步骤方法添加的波次步骤文本与目标模板中的波次步骤文本完全匹配。</span><span class="sxs-lookup"><span data-stu-id="85496-210">Free text is prone to errors, because users must make sure that the wave step text that they add for a specific wave step method in a wave template exactly matches the wave step text in the target template.</span></span>
>
> <span data-ttu-id="85496-211">特定波次步骤类型的波次步骤类型在单独页面中设置。</span><span class="sxs-lookup"><span data-stu-id="85496-211">Wave step codes for a specific wave step type are set up on a separate page.</span></span> <span data-ttu-id="85496-212">必须在下拉列表中为波次模板中每个需要波次步骤代码的波次步骤方法实例选择波次步骤代码。</span><span class="sxs-lookup"><span data-stu-id="85496-212">For every instance of a wave step method in a wave template that requires a wave step code, the wave step code must be selected in a drop-down list.</span></span> <span data-ttu-id="85496-213">在下拉列表中进行的选择将替换普通文本，因此有助于降低人为错误的风险和影响。</span><span class="sxs-lookup"><span data-stu-id="85496-213">Selection in a drop-down list replaces free text entry and helps reduce the risk and impact of human error.</span></span> <span data-ttu-id="85496-214">设置代码用于将波次模板中的波次步骤方法链接到该方法的目标模板。</span><span class="sxs-lookup"><span data-stu-id="85496-214">Setup codes are used to link a wave step method in a wave template to a target template for the method.</span></span>

### <a name="set-up-load-mix-groups"></a><span data-ttu-id="85496-215">设置负荷混合组</span><span class="sxs-lookup"><span data-stu-id="85496-215">Set up load mix groups</span></span>

<span data-ttu-id="85496-216">负荷混合组为可合并到一个负荷中的物料的类型建立规则。</span><span class="sxs-lookup"><span data-stu-id="85496-216">Load mix groups establish rules for the types of items that can be combined on a single load.</span></span> <span data-ttu-id="85496-217">可以根据需要设置任意数量的负荷混合组。</span><span class="sxs-lookup"><span data-stu-id="85496-217">You can set up as many load mix groups as you require.</span></span> <span data-ttu-id="85496-218">但是，若要利用高级波次负荷计划功能，必须至少有一个。</span><span class="sxs-lookup"><span data-stu-id="85496-218">However, to use advanced wave load building, you must have at least one.</span></span> <span data-ttu-id="85496-219">执行以下步骤创建负荷混合组。</span><span class="sxs-lookup"><span data-stu-id="85496-219">Follow these steps to create a load mix group.</span></span>

1. <span data-ttu-id="85496-220">转到**仓库管理** \> **设置** \> **负荷** \> **负荷混合组**。</span><span class="sxs-lookup"><span data-stu-id="85496-220">Go to **Warehouse management** \> **Setup** \> **Load** \> **Load mix groups**.</span></span>
1. <span data-ttu-id="85496-221">在“操作窗格”中，选择**新建**创建负荷组。</span><span class="sxs-lookup"><span data-stu-id="85496-221">On the Action Pane, select **New** to create a load group.</span></span>
1. <span data-ttu-id="85496-222">在**负荷混合组 ID** 字段中，输入新组的名称。</span><span class="sxs-lookup"><span data-stu-id="85496-222">In the **Load mix group ID** field, enter a name for the new group.</span></span>

    <span data-ttu-id="85496-223">如果在使用 **USMF** 演示数据，请设置以下值：</span><span class="sxs-lookup"><span data-stu-id="85496-223">If you're working with the **USMF** demo data, set the following values:</span></span>

    - <span data-ttu-id="85496-224">**负荷混合组 ID**：*TV*</span><span class="sxs-lookup"><span data-stu-id="85496-224">**Load mix group ID:** *TV*</span></span>
    - <span data-ttu-id="85496-225">**说明**：*TV*</span><span class="sxs-lookup"><span data-stu-id="85496-225">**Description:** *TV*</span></span>

1. <span data-ttu-id="85496-226">在操作窗格上，选择**保存**启用**负荷混合组条件**快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="85496-226">On the Action Pane, select **Save** to make the **Load mix group criteria** FastTab available.</span></span>
1. <span data-ttu-id="85496-227">在**负荷混合组条件**快速选项卡上，选择**新建**向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="85496-227">On the **Load mix group criteria** FastTab, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="85496-228">在新行中，在每个字段中设置所需值。</span><span class="sxs-lookup"><span data-stu-id="85496-228">In the new row, set the desired values in each field.</span></span> <span data-ttu-id="85496-229">这些值决定为负荷混合考虑的物料组。</span><span class="sxs-lookup"><span data-stu-id="85496-229">These values determine the item groups that are considered for the load mix.</span></span>

    <span data-ttu-id="85496-230">如果在使用 **USMF** 演示数据，请在**物料组**字段中选择 *TV&Video*。</span><span class="sxs-lookup"><span data-stu-id="85496-230">If you're working with the **USMF** demo data, select *TV&Video* in the **Item group** field.</span></span>

1. <span data-ttu-id="85496-231">在操作窗格上，选择**保存**启用**负荷混合组约束**快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="85496-231">On the Action Pane, select **Save** to make the **Load mix group constraints** FastTab available.</span></span>
1. <span data-ttu-id="85496-232">在**负荷混合组约束**快速选项卡上，选择**新建**向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="85496-232">On the **Load mix group constraints** FastTab, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="85496-233">在新行中，在每个字段中设置所需值。</span><span class="sxs-lookup"><span data-stu-id="85496-233">In the new row, set the desired values in each field.</span></span>

    <span data-ttu-id="85496-234">如果在使用 **USMF** 演示数据，请设置以下值：</span><span class="sxs-lookup"><span data-stu-id="85496-234">If you're working with the **USMF** demo data, set the following values:</span></span>

    - <span data-ttu-id="85496-235">**物料组**：*CarAudio*</span><span class="sxs-lookup"><span data-stu-id="85496-235">**Item group:** *CarAudio*</span></span>
    - <span data-ttu-id="85496-236">**负荷计划操作**：*限制*（此值将阻止属于 **CarAudio** 物料组的物料与属于 **TV&Video** 物料组的物料位于同一个负荷中。）</span><span class="sxs-lookup"><span data-stu-id="85496-236">**Load build action:** *Restrict* (This value will prevent items that belong to the **CarAudio** item group from being on the same load as items that belong to the **TV&Video** item group.)</span></span>

1. <span data-ttu-id="85496-237">继续处理规则，直到添加了负荷混合组需要的所有条件和约束。</span><span class="sxs-lookup"><span data-stu-id="85496-237">Continue to work with the rules until you've added all the criteria and constraints that you require for the load mix group.</span></span>

<span data-ttu-id="85496-238">如果在使用 **USMF** 演示数据，说明已完成了此设置。</span><span class="sxs-lookup"><span data-stu-id="85496-238">If you're working with the **USMF** demo data, you've now finished this setup.</span></span>

### <a name="set-up-load-build-templates"></a><span data-ttu-id="85496-239">设置负荷计划模板</span><span class="sxs-lookup"><span data-stu-id="85496-239">Set up load build templates</span></span>

<span data-ttu-id="85496-240">可以根据需要设置任意数量的负荷计划模板。</span><span class="sxs-lookup"><span data-stu-id="85496-240">You can set up as many load build templates as you require.</span></span> <span data-ttu-id="85496-241">但是，若要利用高级波次负荷计划功能，必须至少有一个。</span><span class="sxs-lookup"><span data-stu-id="85496-241">However, to use advanced wave load building, you must have at least one.</span></span> <span data-ttu-id="85496-242">请执行以下步骤创建负荷计划模板。</span><span class="sxs-lookup"><span data-stu-id="85496-242">Follow these steps to create a load build template.</span></span>

1. <span data-ttu-id="85496-243">转到**仓库管理** \> **设置** \> **负荷** \> **波次负荷计划模板**。</span><span class="sxs-lookup"><span data-stu-id="85496-243">Go to **Warehouse Management** \> **Setup** \> **Load** \> **Wave load building templates**.</span></span>
1. <span data-ttu-id="85496-244">在操作窗格上，选择**新建**向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="85496-244">On the Action Pane, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="85496-245">在新行中，设置以下值。</span><span class="sxs-lookup"><span data-stu-id="85496-245">In the new row, set the following values.</span></span>

    | <span data-ttu-id="85496-246">字段</span><span class="sxs-lookup"><span data-stu-id="85496-246">Field</span></span> | <span data-ttu-id="85496-247">说明</span><span class="sxs-lookup"><span data-stu-id="85496-247">Description</span></span> | <span data-ttu-id="85496-248">USMF 演示数据中的值</span><span class="sxs-lookup"><span data-stu-id="85496-248">Value in the USMF demo data</span></span> |
    |---|---|---|
    | <span data-ttu-id="85496-249">序列号</span><span class="sxs-lookup"><span data-stu-id="85496-249">Sequence number</span></span> | <span data-ttu-id="85496-250">模板的评估顺序。</span><span class="sxs-lookup"><span data-stu-id="85496-250">The order that the template will be evaluated in.</span></span> | <span data-ttu-id="85496-251">*1*</span><span class="sxs-lookup"><span data-stu-id="85496-251">*1*</span></span> |
    | <span data-ttu-id="85496-252">负荷构建模板名称</span><span class="sxs-lookup"><span data-stu-id="85496-252">Load build template name</span></span> | <span data-ttu-id="85496-253">输入负荷计划模板的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="85496-253">Enter the unique identifier of the load build template.</span></span> <span data-ttu-id="85496-254">应该输入此设置中前面创建或更新的模板的名称。</span><span class="sxs-lookup"><span data-stu-id="85496-254">You should enter the name of the template that you created or updated earlier in this setup.</span></span> | <span data-ttu-id="85496-255">*62 装运默认*</span><span class="sxs-lookup"><span data-stu-id="85496-255">*62 Shipping Default*</span></span> |
    | <span data-ttu-id="85496-256">波次步骤代码</span><span class="sxs-lookup"><span data-stu-id="85496-256">Wave step code</span></span> | <span data-ttu-id="85496-257">输入要用于将模板链接到波次方法的波次步骤代码。</span><span class="sxs-lookup"><span data-stu-id="85496-257">Enter the wave step code to use to link the template to a wave method.</span></span> <span data-ttu-id="85496-258">应该输入此设置前面设置波次模板时为 **buildLoads** 方法选择的代码。</span><span class="sxs-lookup"><span data-stu-id="85496-258">You should enter the code that you selected for the **buildLoads** method when you set up the wave template earlier in this setup.</span></span> | <span data-ttu-id="85496-259">*WSC2112*</span><span class="sxs-lookup"><span data-stu-id="85496-259">*WSC2112*</span></span> |
    | <span data-ttu-id="85496-260">负荷模板 ID</span><span class="sxs-lookup"><span data-stu-id="85496-260">Load template ID</span></span> | <span data-ttu-id="85496-261">选择要在创建新负荷时使用和要在分配给现有负荷时对比的负荷模板。</span><span class="sxs-lookup"><span data-stu-id="85496-261">Select the load template to use when new loads are created and to match against when assigning to existing loads.</span></span> <span data-ttu-id="85496-262">负荷模板定义整个负荷允许的最大重量和体积。</span><span class="sxs-lookup"><span data-stu-id="85496-262">The load template defines the maximum weight and volume that are permitted for the whole load.</span></span> | <span data-ttu-id="85496-263">*标准负荷模板*</span><span class="sxs-lookup"><span data-stu-id="85496-263">*Stnd Load Template*</span></span> |
    | <span data-ttu-id="85496-264">设备</span><span class="sxs-lookup"><span data-stu-id="85496-264">Equipment</span></span> | <span data-ttu-id="85496-265">要在分配到现有负荷和在创建的新负荷中输入时匹配的设备。</span><span class="sxs-lookup"><span data-stu-id="85496-265">The equipment to match against when assigning to existing loads and to enter on new loads that are created.</span></span> | <span data-ttu-id="85496-266">保持此字段为空。</span><span class="sxs-lookup"><span data-stu-id="85496-266">Leave this field blank.</span></span> |
    | <span data-ttu-id="85496-267">负荷混合组 ID</span><span class="sxs-lookup"><span data-stu-id="85496-267">Load mix group ID</span></span> | <span data-ttu-id="85496-268">选择当负荷中允许物料时要使用的负荷混合组。</span><span class="sxs-lookup"><span data-stu-id="85496-268">Select the load mix group to use if the item is allowed on the load.</span></span> <span data-ttu-id="85496-269">混合组为可合并到一个负荷中的物料的类型建立规则。</span><span class="sxs-lookup"><span data-stu-id="85496-269">The mix group establishes rules for the types of items that can be combined on a single load.</span></span> <span data-ttu-id="85496-270">应该选择此设置中前面创建的一个混合组。</span><span class="sxs-lookup"><span data-stu-id="85496-270">You should select one of the mix groups that you created earlier in this setup.</span></span> | <span data-ttu-id="85496-271">*TV*</span><span class="sxs-lookup"><span data-stu-id="85496-271">*TV*</span></span> |
    | <span data-ttu-id="85496-272">使用未结负荷</span><span class="sxs-lookup"><span data-stu-id="85496-272">Use open loads</span></span> | <span data-ttu-id="85496-273">选择是否应添加现有未结负荷。</span><span class="sxs-lookup"><span data-stu-id="85496-273">Select whether existing open loads should be added.</span></span> <span data-ttu-id="85496-274">选项如下：</span><span class="sxs-lookup"><span data-stu-id="85496-274">The following options are available:</span></span><ul><li><span data-ttu-id="85496-275">**无** – 不向任何现有负荷添加未结负荷。</span><span class="sxs-lookup"><span data-stu-id="85496-275">**None** – Don't add open loads to any existing loads.</span></span></li><li><span data-ttu-id="85496-276">**任何** – 向对此行有效的任何现有负荷添加未结负荷。</span><span class="sxs-lookup"><span data-stu-id="85496-276">**Any** – Add open loads to any existing loads that are valid for the line.</span></span></li><li><span data-ttu-id="85496-277">**已分配** – 向分配给波次的负荷添加未结负荷。</span><span class="sxs-lookup"><span data-stu-id="85496-277">**Assigned** – Add open loads to the load that is assigned to the wave.</span></span></li></ul> | <span data-ttu-id="85496-278">*任何*</span><span class="sxs-lookup"><span data-stu-id="85496-278">*Any*</span></span> |
    | <span data-ttu-id="85496-279">创建负荷</span><span class="sxs-lookup"><span data-stu-id="85496-279">Create loads</span></span> | <span data-ttu-id="85496-280">指定当任何现有负荷均不符合条件时是否应创建新负荷。</span><span class="sxs-lookup"><span data-stu-id="85496-280">Specify whether new loads should be created if no existing loads match the criteria.</span></span> | <span data-ttu-id="85496-281">已选择（= *是*）</span><span class="sxs-lookup"><span data-stu-id="85496-281">Selected (= *Yes*)</span></span> |
    | <span data-ttu-id="85496-282">允许拆分装运行</span><span class="sxs-lookup"><span data-stu-id="85496-282">Allow shipment line split</span></span> | <span data-ttu-id="85496-283">指定如果一个负荷行整行超过负荷模板的最大产能时，是否允许跨多个负荷拆分该行。</span><span class="sxs-lookup"><span data-stu-id="85496-283">Specify whether a single load line can be split across multiple loads if the full line exceeds the maximum capacity of the load template.</span></span> | <span data-ttu-id="85496-284">已清除（= *否*）</span><span class="sxs-lookup"><span data-stu-id="85496-284">Cleared (= *No*)</span></span> |
    | <span data-ttu-id="85496-285">验证容量</span><span class="sxs-lookup"><span data-stu-id="85496-285">Validate volumetrics</span></span> | <span data-ttu-id="85496-286">指定负荷计划功能是否应在添加每个负荷行时检查重量和体积，以确保遵守负荷模板的体积限制。</span><span class="sxs-lookup"><span data-stu-id="85496-286">Specify whether load building should check the weight and volume as each load line is added, to ensure that the volumetric limits of the load template are respected.</span></span> | <span data-ttu-id="85496-287">已清除（= *否*）</span><span class="sxs-lookup"><span data-stu-id="85496-287">Cleared (= *No*)</span></span> |

1. <span data-ttu-id="85496-288">在操作窗格上，选择**保存**以启用**编辑查询**选项。</span><span class="sxs-lookup"><span data-stu-id="85496-288">On the Action Pane, select **Save** to make the **Edit query** option available.</span></span>
1. <span data-ttu-id="85496-289">在操作窗格上，选择**编辑查询**打开对话框编辑查询。</span><span class="sxs-lookup"><span data-stu-id="85496-289">On the Action Pane, select **Edit query** to open a dialog box for editing the query.</span></span>
1. <span data-ttu-id="85496-290">在对话框的**排序**选项卡中，选择**添加**向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="85496-290">In the dialog box, on the **Sorting** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="85496-291">在新行中，定义要使用的排序规则。</span><span class="sxs-lookup"><span data-stu-id="85496-291">In the new row, define the sorting rules that you want to use.</span></span> <span data-ttu-id="85496-292">例如，设置以下值，以便按订单编号以升序为搜索结果排序：</span><span class="sxs-lookup"><span data-stu-id="85496-292">For example, set the following values to sort the search results in ascending order by order number:</span></span>

    - <span data-ttu-id="85496-293">**表**：*负荷详细信息*</span><span class="sxs-lookup"><span data-stu-id="85496-293">**Table:** *Load details*</span></span>
    - <span data-ttu-id="85496-294">**派生表**：*负荷详细信息*</span><span class="sxs-lookup"><span data-stu-id="85496-294">**Derived table:** *Load details*</span></span>
    - <span data-ttu-id="85496-295">**字段**：*订单编号*</span><span class="sxs-lookup"><span data-stu-id="85496-295">**Field:** *Order number*</span></span>
    - <span data-ttu-id="85496-296">**搜索方向**：*升序*</span><span class="sxs-lookup"><span data-stu-id="85496-296">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="85496-297">选择**确定**保存更改并关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="85496-297">Select **OK** to save your changes and close the dialog box.</span></span>
1. <span data-ttu-id="85496-298">在**拆分依据**快速选项卡上，设置规则以控制如何拆分负荷。</span><span class="sxs-lookup"><span data-stu-id="85496-298">On the **Break by** FastTab, set rules to control how your loads are split up.</span></span> <span data-ttu-id="85496-299">通常可以拆分已延伸到负荷行的自定义字段，如**工艺路线**、**导览**或**运行**。</span><span class="sxs-lookup"><span data-stu-id="85496-299">Typically, you might break on custom fields that have been extended onto the load line, such as **Route**, **Tour**, or **Run**.</span></span> <span data-ttu-id="85496-300">例如，若要为每个订单编号创建一个负荷，请选中具有以下值的行的**拆分依据**复选框：</span><span class="sxs-lookup"><span data-stu-id="85496-300">For example, to create one load per order number, select the **Break by** check box for the row that has the following values:</span></span>

    - <span data-ttu-id="85496-301">**引用表名称**：*负荷详细信息*</span><span class="sxs-lookup"><span data-stu-id="85496-301">**Reference table name:** *Load details*</span></span>
    - <span data-ttu-id="85496-302">**参考字段名称**：*订单编号*</span><span class="sxs-lookup"><span data-stu-id="85496-302">**Reference field name:** *Order number*</span></span>

## <a name="scenario"></a><span data-ttu-id="85496-303">应用场景</span><span class="sxs-lookup"><span data-stu-id="85496-303">Scenario</span></span>

<span data-ttu-id="85496-304">此场景显示在处理销售订单时，本主题前面介绍的设置如何影响仓库操作。</span><span class="sxs-lookup"><span data-stu-id="85496-304">This scenario shows how the settings that were described earlier in this topic affect warehouse operations while a sales order is processed.</span></span> <span data-ttu-id="85496-305">此场景使用 **USMF** 演示数据和这些设置说明中提供的其他演示值。</span><span class="sxs-lookup"><span data-stu-id="85496-305">This scenario uses the **USMF** demo data together with other demo values that are provided in those setup instructions.</span></span>

### <a name="create-sales-orders"></a><span data-ttu-id="85496-306">创建销售订单</span><span class="sxs-lookup"><span data-stu-id="85496-306">Create sales orders</span></span>

1. <span data-ttu-id="85496-307">转到**销售和营销** \> **销售订单** \> **所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="85496-307">Go to **Sales and marketing** \> **Sales orders** \> **All sales orders**.</span></span>
1. <span data-ttu-id="85496-308">在操作窗格上，选择**新建**以打开**创建销售订单**对话框。</span><span class="sxs-lookup"><span data-stu-id="85496-308">On the Action Pane, select **New** to open the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="85496-309">在对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="85496-309">In the dialog box, set the following values:</span></span>

    - <span data-ttu-id="85496-310">在**客户**快速选项卡上，将**客户帐户**字段设置为 *US-007*。</span><span class="sxs-lookup"><span data-stu-id="85496-310">On the **Customer** FastTab, set the **Customer account** field to *US-007*.</span></span>
    - <span data-ttu-id="85496-311">在**常规**快速选项卡上，将**仓库**字段设置为 *62*。</span><span class="sxs-lookup"><span data-stu-id="85496-311">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="85496-312">选择**确定**创建销售订单，然后关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="85496-312">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="85496-313">将打开您的新销售订单。</span><span class="sxs-lookup"><span data-stu-id="85496-313">Your new sales order is opened.</span></span> <span data-ttu-id="85496-314">**销售订单行**快速选项卡上的网格中应包含一个新的空行。</span><span class="sxs-lookup"><span data-stu-id="85496-314">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="85496-315">在这个新行中，将**物料编号**字段设置为 *A0001*，将**数量**字段设置为 *1*。</span><span class="sxs-lookup"><span data-stu-id="85496-315">On this new line, set the **Item number** field to *A0001* and the **Quantity** field to *1*.</span></span>
1. <span data-ttu-id="85496-316">在网格上方的**库存**菜单中，选择**预留**。</span><span class="sxs-lookup"><span data-stu-id="85496-316">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="85496-317">在**预留**页的操作窗格中，选择**预留批次**。</span><span class="sxs-lookup"><span data-stu-id="85496-317">On the **Reservation** page, on the Action Pane, select **Reserve lot**.</span></span>
1. <span data-ttu-id="85496-318">选择页面右上角的**关闭**按钮 (**X**) 回到销售订单。</span><span class="sxs-lookup"><span data-stu-id="85496-318">Select the **Close** button (**X**) in the upper-right corner of the page to return to the sales order.</span></span>
1. <span data-ttu-id="85496-319">在“操作窗格”上的**仓库**选项卡上，在**操作**组中，选择**发放到仓库**。</span><span class="sxs-lookup"><span data-stu-id="85496-319">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span> <span data-ttu-id="85496-320">系统将创建一个装运，然后将其添加到新负荷，因为所有现有负荷中均不包含具有此订单编号的负荷行。</span><span class="sxs-lookup"><span data-stu-id="85496-320">The system creates a shipment and adds it to a new load, because no existing load contains load lines that have this order number.</span></span>

    <span data-ttu-id="85496-321">您将收到指示为此订单创建的工作、波次和装运的参考消息。</span><span class="sxs-lookup"><span data-stu-id="85496-321">You receive informational messages that indicate the work, wave, and shipment that are created for this order.</span></span>

1. <span data-ttu-id="85496-322">若要确认销售行中的负荷、装运和工作详细信息，请选择该行，然后在网格上方的**仓库**菜单中选择**负荷详细信息**、**装运详细信息**或**工作详细信息**。</span><span class="sxs-lookup"><span data-stu-id="85496-322">To confirm the load, shipment, and work details on the sales line, select the line, and then, on the **Warehouse** menu above the grid, select **Load details**, **Shipment details**, or **Work details**.</span></span>
1. <span data-ttu-id="85496-323">在刚才创建的销售订单中的**销售订单行**快速选项卡上，选择**添加行**再添加一行。</span><span class="sxs-lookup"><span data-stu-id="85496-323">In the sales order that you just created, on the **Sales order lines** FastTab, select **Add line** to add another line.</span></span>
1. <span data-ttu-id="85496-324">在新行中，将**物料编号**字段设置为 *A0002*，将**数量**字段设置为 *1*。</span><span class="sxs-lookup"><span data-stu-id="85496-324">On the new line, set the **Item number** field to *A0002* and the **Quantity** field to *1*.</span></span>
1. <span data-ttu-id="85496-325">重复行 6 到 9 预留行并将其发放到仓库。</span><span class="sxs-lookup"><span data-stu-id="85496-325">Repeat lines 6 through 9 to reserve the line and release it to the warehouse.</span></span> <span data-ttu-id="85496-326">系统将为添加的行创建一个**新**装运。</span><span class="sxs-lookup"><span data-stu-id="85496-326">The system creates a **new** shipment for the line that you added.</span></span> <span data-ttu-id="85496-327">但是，因为您在使用高级波次负荷计划功能，因此系统将把该装运和负荷行添加到现有波次。</span><span class="sxs-lookup"><span data-stu-id="85496-327">However, because you're using advanced wave load building, the system adds that shipment and load line to the existing wave.</span></span> <span data-ttu-id="85496-328">如果您未在使用高级波次负荷计划功能，系统将为装运创建新负荷。</span><span class="sxs-lookup"><span data-stu-id="85496-328">If you weren't using advanced wave load building, the system would create a new load for the shipment.</span></span>
1. <span data-ttu-id="85496-329">在刚才创建的销售订单中的**销售订单行**快速选项卡上，选择**添加行**再添加一行。</span><span class="sxs-lookup"><span data-stu-id="85496-329">In the sales order that you just created, on the **Sales order lines** FastTab, select **Add line** to add another line.</span></span>
1. <span data-ttu-id="85496-330">在新行中，将**物料编号**字段设置为 *M9200*，将**数量**字段设置为 *1*。</span><span class="sxs-lookup"><span data-stu-id="85496-330">On the new line, set the **Item number** field to *M9200* and the **Quantity** field to *1*.</span></span>
1. <span data-ttu-id="85496-331">重复行 6 到 9 预留行并将其发放到仓库。</span><span class="sxs-lookup"><span data-stu-id="85496-331">Repeat lines 6 through 9 to reserve the line and release it to the warehouse.</span></span> <span data-ttu-id="85496-332">就像前面一样，系统将为添加的行创建一个**新**装运。</span><span class="sxs-lookup"><span data-stu-id="85496-332">As before, the system creates a **new** shipment for the line that you added.</span></span> <span data-ttu-id="85496-333">但是，因为该物料来自 **CarAudio** 物料组，所以**无法通过为负荷混合组设置的约束**。</span><span class="sxs-lookup"><span data-stu-id="85496-333">However, because the item is from the **CarAudio** item group, it **fails to pass the constraints that you set up for the load mix group**.</span></span> <span data-ttu-id="85496-334">因此，将把其**添加到新负荷**。</span><span class="sxs-lookup"><span data-stu-id="85496-334">Therefore, it's **added to a new load**.</span></span> <span data-ttu-id="85496-335">如果尚未在负荷计划模板中指定负荷混合组，应该已将该装运添加到第一个负荷。</span><span class="sxs-lookup"><span data-stu-id="85496-335">If you hadn't specified a load mix group on the load build template, this shipment would have been added to the first load.</span></span>
