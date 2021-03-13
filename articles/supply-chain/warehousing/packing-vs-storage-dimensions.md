---
title: 设置不同的包装和存储维度
description: 本主题说明如何指定每个指定维度用于哪个流程（包装、存储或嵌套包装）。
author: mirzaab
manager: tfehr
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPhysDimUOM
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 004d9b4522335b481b640ef0fe35f4db66e3c9f5
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/28/2021
ms.locfileid: "5078238"
---
# <a name="set-different-dimensions-for-packing-and-storage"></a><span data-ttu-id="8744e-103">设置不同的包装和存储维度</span><span class="sxs-lookup"><span data-stu-id="8744e-103">Set different dimensions for packing and storage</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8744e-104">有些物料的包装或存储方式会让您有可能需要针对多个不同流程中的每个流程进行不同的物理维度跟踪。</span><span class="sxs-lookup"><span data-stu-id="8744e-104">Some items are packed or stored in such a way that you may need to track physical dimensions differently for each of several different processes.</span></span> <span data-ttu-id="8744e-105">*包装产品维度* 功能可让您为每个产品设置一种或几种维度。</span><span class="sxs-lookup"><span data-stu-id="8744e-105">The *Packaging product dimensions* feature lets you set up one or several types of dimensions for each product.</span></span> <span data-ttu-id="8744e-106">每个维度类型提供一组物理度量（重量、宽度、深度和高度），并建立应用这些物理度量值的流程。</span><span class="sxs-lookup"><span data-stu-id="8744e-106">Each dimension type provides a set of physical measurements (weight, width, depth, and height), and establishes the process where those physical measurement values apply.</span></span> <span data-ttu-id="8744e-107">启用此功能后，您的系统将支持以下维度类型：</span><span class="sxs-lookup"><span data-stu-id="8744e-107">When this feature is enabled, your system will support the following types of dimensions:</span></span>

- <span data-ttu-id="8744e-108">*存储* - 存储维度与库位容量一起用于确定各个仓库位置可以存储每种物料的数量。</span><span class="sxs-lookup"><span data-stu-id="8744e-108">*Storage* - Storage dimensions are used along with location volumetrics to determine how many of each item can be stored in various warehouse locations.</span></span>
- <span data-ttu-id="8744e-109">*包装* - 包装维度用来在集装化和手动包装流程中确定适合各个集装箱类型的每种物料的数量。</span><span class="sxs-lookup"><span data-stu-id="8744e-109">*Packing* - Packing dimensions are used during containerization and the manual packing process to determine how many of each item will fit in various container types.</span></span>
- <span data-ttu-id="8744e-110">*嵌套包装* - 嵌套包装维度在包装流程包含多个级别时使用。</span><span class="sxs-lookup"><span data-stu-id="8744e-110">*Nested packing* - Nested packing dimensions are used when the packing process contains multiple levels.</span></span>

<span data-ttu-id="8744e-111">即使未启用 *包装产品维度* 功能，也支持 *存储* 维度。</span><span class="sxs-lookup"><span data-stu-id="8744e-111">*Storage* dimensions are supported even when the *Packaging product dimensions* feature isn't enabled.</span></span> <span data-ttu-id="8744e-112">您使用 Supply Chain Management 中的 **物理维度** 页设置这些维度。</span><span class="sxs-lookup"><span data-stu-id="8744e-112">You set these up using the **Physical dimension** page in Supply Chain Management.</span></span> <span data-ttu-id="8744e-113">这些维度由所有未指定包装维度和嵌套包装维度的流程使用。</span><span class="sxs-lookup"><span data-stu-id="8744e-113">These dimensions are used by all processes where the packing and nested packing dimensions aren't specified.</span></span>

<span data-ttu-id="8744e-114">*包装* 和 *嵌套包装* 维度使用 **物理产品维度** 页设置，在您启用 *包装产品维度* 功能时添加。</span><span class="sxs-lookup"><span data-stu-id="8744e-114">*Packing* and *nested packing* dimensions are set up using the **Physical product dimensions** page, which is added when you enable the *Packaging product dimensions* feature.</span></span>
<span data-ttu-id="8744e-115">本主题提供了一个场景来说明如何使用此功能。</span><span class="sxs-lookup"><span data-stu-id="8744e-115">This topic provides a scenario that illustrates how to use this feature.</span></span>

## <a name="turn-on-the-packaging-product-dimensions-feature"></a><span data-ttu-id="8744e-116">打开包装产品维度功能</span><span class="sxs-lookup"><span data-stu-id="8744e-116">Turn on the packaging product dimensions feature</span></span>

<span data-ttu-id="8744e-117">此功能只有在系统中开启之后才能使用。</span><span class="sxs-lookup"><span data-stu-id="8744e-117">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="8744e-118">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区检查功能状态和开启功能（如果需要）。</span><span class="sxs-lookup"><span data-stu-id="8744e-118">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="8744e-119">在那里，此功能以以下方式列出：</span><span class="sxs-lookup"><span data-stu-id="8744e-119">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="8744e-120">**模块**：*仓库管理*</span><span class="sxs-lookup"><span data-stu-id="8744e-120">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="8744e-121">**功能名称**：*包装产品维度*</span><span class="sxs-lookup"><span data-stu-id="8744e-121">**Feature name:** *Packaging product dimensions*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="8744e-122">示例场景</span><span class="sxs-lookup"><span data-stu-id="8744e-122">Example scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="8744e-123">设置场景</span><span class="sxs-lookup"><span data-stu-id="8744e-123">Set up the scenario</span></span>

<span data-ttu-id="8744e-124">在运行示例场景之前，您必须按照本节所述准备您的系统。</span><span class="sxs-lookup"><span data-stu-id="8744e-124">Before you can run the example scenario, you must prepare your system as described in this section.</span></span>

#### <a name="enable-demo-data"></a><span data-ttu-id="8744e-125">启用演示数据</span><span class="sxs-lookup"><span data-stu-id="8744e-125">Enable demo data</span></span>

<span data-ttu-id="8744e-126">若要使用此处指定的演示记录和值完成此场景，使用的系统中必须已安装标准[演示数据](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="8744e-126">To work through this scenario using the demo records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="8744e-127">此外，开始前，还必须选择 *USMF* 法人。</span><span class="sxs-lookup"><span data-stu-id="8744e-127">Additionally, you must select the *USMF* legal entity before you begin.</span></span>

#### <a name="add-a-new-physical-dimension-to-a-product"></a><span data-ttu-id="8744e-128">为产品添加新物理维度</span><span class="sxs-lookup"><span data-stu-id="8744e-128">Add a new physical dimension to a product</span></span>

<span data-ttu-id="8744e-129">执行以下操作为产品添加新的物理维度：</span><span class="sxs-lookup"><span data-stu-id="8744e-129">Add a new physical dimension for a product by doing the following:</span></span>

1. <span data-ttu-id="8744e-130">转到 **产品信息管理 \> 产品 \> 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="8744e-130">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="8744e-131">选择具有 **物料编号** *A0001* 的产品。</span><span class="sxs-lookup"><span data-stu-id="8744e-131">Select the product with **Item number** *A0001*.</span></span>
1. <span data-ttu-id="8744e-132">在操作窗格上，打开 **管理库存** 选项卡，从 **仓库** 组，选择 **物理产品维度**。</span><span class="sxs-lookup"><span data-stu-id="8744e-132">On the Action Pane, open the **Manage inventory** tab and, from the **Warehouse** group, select **Physical product dimensions**.</span></span>
1. <span data-ttu-id="8744e-133">**物理产品维度** 页将打开。</span><span class="sxs-lookup"><span data-stu-id="8744e-133">The **Physical product dimensions** page opens.</span></span> <span data-ttu-id="8744e-134">在操作窗格上，选择 **新建** 来使用以下设置向网格添加新维度：</span><span class="sxs-lookup"><span data-stu-id="8744e-134">On the Action Pane, select **New** to add a new dimension to the grid with the following settings:</span></span>
    - <span data-ttu-id="8744e-135">**物理维度类型** - *包装*</span><span class="sxs-lookup"><span data-stu-id="8744e-135">**Physical dimension type** - *Packing*</span></span>
    - <span data-ttu-id="8744e-136">**物理单位** - *件*</span><span class="sxs-lookup"><span data-stu-id="8744e-136">**Physical unit** - *pcs*</span></span>
    - <span data-ttu-id="8744e-137">**重量** - *4*</span><span class="sxs-lookup"><span data-stu-id="8744e-137">**Weight** - *4*</span></span>
    - <span data-ttu-id="8744e-138">**重量单位** - *千克*</span><span class="sxs-lookup"><span data-stu-id="8744e-138">**Weight unit** - *kg*</span></span>
    - <span data-ttu-id="8744e-139">**深度** - *3*</span><span class="sxs-lookup"><span data-stu-id="8744e-139">**Depth** - *3*</span></span>
    - <span data-ttu-id="8744e-140">**高度** - *4*</span><span class="sxs-lookup"><span data-stu-id="8744e-140">**Height** - *4*</span></span>
    - <span data-ttu-id="8744e-141">**宽度** - *3*</span><span class="sxs-lookup"><span data-stu-id="8744e-141">**Width** - *3*</span></span>
    - <span data-ttu-id="8744e-142">**长度** - *厘米*</span><span class="sxs-lookup"><span data-stu-id="8744e-142">**Length** - *cm*</span></span>
    - <span data-ttu-id="8744e-143">**体积单位** - *立方厘米*</span><span class="sxs-lookup"><span data-stu-id="8744e-143">**Volume unit** - *cm3*</span></span>

<span data-ttu-id="8744e-144">**体积** 字段根据您的 **深度**、**高度** 和 **宽度** 设置自动计算。</span><span class="sxs-lookup"><span data-stu-id="8744e-144">The **Volume** field is automatically calculated based on your **Depth**, **Height**, and **Width** settings.</span></span>

#### <a name="create-a-new-container-type"></a><span data-ttu-id="8744e-145">创建新集装箱类型</span><span class="sxs-lookup"><span data-stu-id="8744e-145">Create a new container type</span></span>

<span data-ttu-id="8744e-146">转到 **仓库管理 \> 设置 \> 集装箱 \> 集装箱类型**，然后使用以下设置创建新记录：</span><span class="sxs-lookup"><span data-stu-id="8744e-146">Go to **Warehouse management \> Setup \> Containers \> Container types** and create a new record with the following settings:</span></span>

- <span data-ttu-id="8744e-147">**集装箱类型代码** - *Short Box*</span><span class="sxs-lookup"><span data-stu-id="8744e-147">**Container type code** - *Short Box*</span></span>
- <span data-ttu-id="8744e-148">**描述** - *短箱*</span><span class="sxs-lookup"><span data-stu-id="8744e-148">**Description** - *Short Box*</span></span>
- <span data-ttu-id="8744e-149">**最大净重** - *50*</span><span class="sxs-lookup"><span data-stu-id="8744e-149">**Maximum net weight** - *50*</span></span>
- <span data-ttu-id="8744e-150">**体积** - *144*</span><span class="sxs-lookup"><span data-stu-id="8744e-150">**Volume** - *144*</span></span>
- <span data-ttu-id="8744e-151">**长度** - *6*</span><span class="sxs-lookup"><span data-stu-id="8744e-151">**Length** - *6*</span></span>
- <span data-ttu-id="8744e-152">**宽度** - *6*</span><span class="sxs-lookup"><span data-stu-id="8744e-152">**Width** - *6*</span></span>
- <span data-ttu-id="8744e-153">**高度** - *4*</span><span class="sxs-lookup"><span data-stu-id="8744e-153">**Height** - *4*</span></span>

#### <a name="create-a-container-group"></a><span data-ttu-id="8744e-154">创建集装箱组</span><span class="sxs-lookup"><span data-stu-id="8744e-154">Create a container group</span></span>

<span data-ttu-id="8744e-155">转到 **仓库管理 \> 设置 \> 集装箱 \> 集装箱组**，然后使用以下设置创建新记录：</span><span class="sxs-lookup"><span data-stu-id="8744e-155">Go to **Warehouse management \> Setup \> Containers \> Container groups** and create a new record with the following settings:</span></span>

- <span data-ttu-id="8744e-156">**集装箱组 ID** - *Short Box*</span><span class="sxs-lookup"><span data-stu-id="8744e-156">**Container group ID** - *Short Box*</span></span>
- <span data-ttu-id="8744e-157">**描述** - *短箱*</span><span class="sxs-lookup"><span data-stu-id="8744e-157">**Description** - *Short Box*</span></span>

<span data-ttu-id="8744e-158">在 **详细信息** 部分添加新行。</span><span class="sxs-lookup"><span data-stu-id="8744e-158">Add a new line to the **Details** section.</span></span> <span data-ttu-id="8744e-159">将 **集装箱类型** 设置为 *短箱*。</span><span class="sxs-lookup"><span data-stu-id="8744e-159">Set the **Container type** to *Short Box*.</span></span>

#### <a name="set-up-a-container-build-template"></a><span data-ttu-id="8744e-160">设置集装箱生成模板</span><span class="sxs-lookup"><span data-stu-id="8744e-160">Set up a container build template</span></span>

<span data-ttu-id="8744e-161">转到 **仓库管理 \> 设置 \> 集装箱 \> 集装箱生成模板**，选择 **箱**。</span><span class="sxs-lookup"><span data-stu-id="8744e-161">Go to **Warehouse management \> Setup \> Containers \> Container build templates** and select **Boxes**.</span></span> <span data-ttu-id="8744e-162">将 **集装箱组 ID** 更改为 *短箱*。</span><span class="sxs-lookup"><span data-stu-id="8744e-162">Change the **Container group ID** to *Short Box*.</span></span>

### <a name="run-the-scenario"></a><span data-ttu-id="8744e-163">运行场景</span><span class="sxs-lookup"><span data-stu-id="8744e-163">Run the scenario</span></span>

<span data-ttu-id="8744e-164">如上一节所述准备好系统后，即可按下一节所述运行场景。</span><span class="sxs-lookup"><span data-stu-id="8744e-164">After you have prepared your system as described in the previous section, you are ready to run the scenario as described in the next section.</span></span>

#### <a name="create-a-sales-order-and-create-a-shipment"></a><span data-ttu-id="8744e-165">创建销售订单与创建装运</span><span class="sxs-lookup"><span data-stu-id="8744e-165">Create a sales order and create a shipment</span></span>

<span data-ttu-id="8744e-166">在此流程中，您将根据物料 *包装* 维度创建装运，其高度小于 3。</span><span class="sxs-lookup"><span data-stu-id="8744e-166">In this process you will create a shipment based on the item *packing* dimensions, for which the height is less than 3.</span></span>

1. <span data-ttu-id="8744e-167">转到 **销售和营销 \> 销售订单 \> 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="8744e-167">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="8744e-168">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="8744e-168">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="8744e-169">在 **创建销售订单** 对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="8744e-169">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="8744e-170">**客户帐户**：*US-001*</span><span class="sxs-lookup"><span data-stu-id="8744e-170">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="8744e-171">**仓库**：*63*</span><span class="sxs-lookup"><span data-stu-id="8744e-171">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="8744e-172">选择 **确定** 创建销售订单，然后关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="8744e-172">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="8744e-173">将打开新销售订单。</span><span class="sxs-lookup"><span data-stu-id="8744e-173">The new sales order is opened.</span></span> <span data-ttu-id="8744e-174">**销售订单行** 快速选项卡上的网格中应包含一个新的空行。</span><span class="sxs-lookup"><span data-stu-id="8744e-174">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="8744e-175">在这个行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="8744e-175">On this line, set the following values:</span></span>

    - <span data-ttu-id="8744e-176">\**物料编号：\*\*\*A0001*</span><span class="sxs-lookup"><span data-stu-id="8744e-176">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="8744e-177">**数量：** *5*</span><span class="sxs-lookup"><span data-stu-id="8744e-177">**Quantity:** *5*</span></span>

1. <span data-ttu-id="8744e-178">在 **销售订单行** 快速选项卡上，选择 **库存 \> 预留**。</span><span class="sxs-lookup"><span data-stu-id="8744e-178">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="8744e-179">在 **预留** 页面的“操作窗格”中，选择 **预留批次** 预留库存。</span><span class="sxs-lookup"><span data-stu-id="8744e-179">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="8744e-180">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="8744e-180">Close the page.</span></span>
1. <span data-ttu-id="8744e-181">在操作窗格上，打开 **仓库** 选项卡，选择 **发放到仓库** 为仓库创建工作。</span><span class="sxs-lookup"><span data-stu-id="8744e-181">On the Action Pane, open the **Warehouse** tab and select **Release to warehouse** to create work for the warehouse.</span></span>
1. <span data-ttu-id="8744e-182">在 **销售订单行** 快速选项卡上，选择 **仓库 \> 装运详细信息**。</span><span class="sxs-lookup"><span data-stu-id="8744e-182">On the **Sales order lines** FastTab, select **Warehouse \> Shipment details**.</span></span>
1. <span data-ttu-id="8744e-183">在操作窗格上，打开 **运输** 选项卡，选择 **查看集装箱**。</span><span class="sxs-lookup"><span data-stu-id="8744e-183">On the Action Pane, open the **Transportation** tab and select **View containers**.</span></span> <span data-ttu-id="8744e-184">确认物料已装入两个 *短箱* 集装箱中。</span><span class="sxs-lookup"><span data-stu-id="8744e-184">Confirm that the item was containerized into the two *Short Box* containers.</span></span>

#### <a name="place-an-item-into-storage"></a><span data-ttu-id="8744e-185">将物料放入存储</span><span class="sxs-lookup"><span data-stu-id="8744e-185">Place an item into storage</span></span>

1. <span data-ttu-id="8744e-186">打开移动设备，登录到仓库 63，转到 **库存 \> 调入**。</span><span class="sxs-lookup"><span data-stu-id="8744e-186">Open the mobile device, sign in to warehouse 63 and go to **Inventory \> Adjust In**.</span></span>
1. <span data-ttu-id="8744e-187">输入 **Loc** = *SHORT-01*。</span><span class="sxs-lookup"><span data-stu-id="8744e-187">Enter **Loc** = *SHORT-01*.</span></span> <span data-ttu-id="8744e-188">制作 **物料** = *A0001*、**数量** = *1 件* 的新牌照。</span><span class="sxs-lookup"><span data-stu-id="8744e-188">Make a new license plate with **Item** = *A0001* and **Quantity** = *1 pcs*.</span></span>
1. <span data-ttu-id="8744e-189">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="8744e-189">Select **OK**.</span></span> <span data-ttu-id="8744e-190">您将收到错误“位置 SHORT-01 失败，因为物料 A0001 不适合位置的指定维度。”</span><span class="sxs-lookup"><span data-stu-id="8744e-190">You will receive the error "Location SHORT-01 failed because item A0001 does not fit in location's specified dimensions."</span></span> <span data-ttu-id="8744e-191">这是因为产品的 *存储* 类型维度大于位置模板中指定的维度。</span><span class="sxs-lookup"><span data-stu-id="8744e-191">This is because the *Storage* type dimensions of the product are larger than the dimensions specified on the location profile.</span></span>
