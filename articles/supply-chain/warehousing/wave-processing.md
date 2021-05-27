---
title: 波次创建和处理
description: 本主题介绍如何创建、处理和发放波次来创建负荷、装运、生产订单或看板订单的领料工作。
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, WHSParameters, whswavetablecreatenew, WHSWaveTable, WHSWaveAttributes, WHSKanbanWaveTable, WHSWaveTableListPage, WHSKanbanWaveTableListPage, WHSProdWaveTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 4bf47b15b668a37f12edb3dbb842d19655fac97a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019019"
---
# <a name="wave-creation-and-processing"></a><span data-ttu-id="d3e05-103">波次创建和处理</span><span class="sxs-lookup"><span data-stu-id="d3e05-103">Wave creation and processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d3e05-104">本主题介绍如何创建、处理和发放波次来创建负荷、装运、生产订单或看板订单的领料工作。</span><span class="sxs-lookup"><span data-stu-id="d3e05-104">This topic describes how to create, process, and release a wave to create picking work for a load, shipment, production order, or kanban order.</span></span> <span data-ttu-id="d3e05-105">您可以为以下类型的订单创建波次：</span><span class="sxs-lookup"><span data-stu-id="d3e05-105">You can create waves for the following types of orders:</span></span>

- <span data-ttu-id="d3e05-106">**销售订单** – 使用装运波次来包括销售订单中的行。</span><span class="sxs-lookup"><span data-stu-id="d3e05-106">**Sales orders** – Use shipping waves to include lines from sales orders.</span></span> <span data-ttu-id="d3e05-107">在销售订单发放到仓库时，销售订单行可以包括在波次中。</span><span class="sxs-lookup"><span data-stu-id="d3e05-107">When a sales order is released to the warehouse, the sales order lines can be included in the wave.</span></span>
- <span data-ttu-id="d3e05-108">**生产订单** – 使用生产波次来包括产品的物料清单 (BOM) 中的行。</span><span class="sxs-lookup"><span data-stu-id="d3e05-108">**Production orders** – Use production waves to include lines from the bill of materials (BOM) for a product.</span></span>
- <span data-ttu-id="d3e05-109">**看板订单** – 看板波次包括看板订单中的领料单行。</span><span class="sxs-lookup"><span data-stu-id="d3e05-109">**Kanban orders** – Kanban waves include picking list lines from kanban orders.</span></span>

<span data-ttu-id="d3e05-110">对于销售订单和看板订单，在订单发放到仓库前，必须预留库存。</span><span class="sxs-lookup"><span data-stu-id="d3e05-110">For sales orders and kanban orders, inventory must be reserved before the order is released to the warehouse.</span></span> <span data-ttu-id="d3e05-111">否则，无法在波次中处理物料或分配行。</span><span class="sxs-lookup"><span data-stu-id="d3e05-111">Otherwise, the items or allocation lines can't be processed in a wave.</span></span> <span data-ttu-id="d3e05-112">但是，生产订单稍微更加灵活。</span><span class="sxs-lookup"><span data-stu-id="d3e05-112">However, production orders are slightly more flexible.</span></span> <span data-ttu-id="d3e05-113">对于生产订单，可以选择以下任意选项：</span><span class="sxs-lookup"><span data-stu-id="d3e05-113">For production orders, you can choose either of the following options:</span></span>

- <span data-ttu-id="d3e05-114">需要预留所有物料，然后才能将订单发放到仓库。</span><span class="sxs-lookup"><span data-stu-id="d3e05-114">Require that all materials are reserved before an order can be released to the warehouse.</span></span>
- <span data-ttu-id="d3e05-115">尽管无法预留所有物料，仍允许将生产订单发放到仓库。</span><span class="sxs-lookup"><span data-stu-id="d3e05-115">Allow production orders to be released to the warehouse even though all materials can't be reserved.</span></span> <span data-ttu-id="d3e05-116">如果选择此选项，则当附加材料变为可用时必须手动重复对仓库流程的发放。</span><span class="sxs-lookup"><span data-stu-id="d3e05-116">If you select this option, you must manually repeat the release to warehouse process when the additional materials become available.</span></span> <span data-ttu-id="d3e05-117">例如，如果您有开始生产所需的物料，并且可以等待附加物料变为可用，这很有用。</span><span class="sxs-lookup"><span data-stu-id="d3e05-117">For example, this is useful if you have the materials that you need to start a production, and can wait until the additional materials become available.</span></span>

<span data-ttu-id="d3e05-118">您可以通过使用 **生产控制参数** 页面上的 **物料预留要求** 字段，指定要使用哪些生产订单选项。</span><span class="sxs-lookup"><span data-stu-id="d3e05-118">You can specify which of these production order options to use by default using the **Requirement for material reservation** field on the **Production control parameters** page.</span></span> <span data-ttu-id="d3e05-119">但是，您可以根据需要更改每个特定生产订单的设置。</span><span class="sxs-lookup"><span data-stu-id="d3e05-119">However, you can change the setting for each specific production order as needed.</span></span> <span data-ttu-id="d3e05-120">有关详细信息，请参阅[波次处理的仓库参数](wave-warehouse-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="d3e05-120">For more information, see [Warehouse parameters for wave processing](wave-warehouse-parameters.md).</span></span>

## <a name="create-and-process-a-wave"></a><span data-ttu-id="d3e05-121">创建和处理波次</span><span class="sxs-lookup"><span data-stu-id="d3e05-121">Create and process a wave</span></span>

<span data-ttu-id="d3e05-122">下图显示了如何创建、处理和发放装运波次的流。</span><span class="sxs-lookup"><span data-stu-id="d3e05-122">The following diagram shows the flow for how shipping waves are created, processed, and released.</span></span> <span data-ttu-id="d3e05-123">这些编号对应于本部分后面的部分。</span><span class="sxs-lookup"><span data-stu-id="d3e05-123">The numbers correspond to the sections later in this section.</span></span>

<span data-ttu-id="d3e05-124">![创建波次的流程](media/wave-processing-diagram.png "创建波次的流程")</span><span class="sxs-lookup"><span data-stu-id="d3e05-124">![Process for creating a wave](media/wave-processing-diagram.png "Process for creating a wave")</span></span>

### <a name="prerequisites"></a><span data-ttu-id="d3e05-125">先决条件</span><span class="sxs-lookup"><span data-stu-id="d3e05-125">Prerequisites</span></span>

<span data-ttu-id="d3e05-126">在开始之前，波次模板必须可用于要创建的波次类型（装运、生产或看板）。</span><span class="sxs-lookup"><span data-stu-id="d3e05-126">Before you start, a wave template must be available for the type of wave you want to create (shipping, production, or kanban).</span></span> <span data-ttu-id="d3e05-127">波次模板确定将如何生成和处理波次的许多设置，包括必须手动和自动完成哪些步骤。</span><span class="sxs-lookup"><span data-stu-id="d3e05-127">The wave template establishes many settings for how the wave will be generated and processed, including which steps must be done manually and which are done automatically.</span></span> <span data-ttu-id="d3e05-128">有关详细信息，请参阅[波次模板](wave-templates.md)。</span><span class="sxs-lookup"><span data-stu-id="d3e05-128">For more information, see [Wave templates](wave-templates.md).</span></span>

### <a name="create-a-wave"></a><span data-ttu-id="d3e05-129">创建波次</span><span class="sxs-lookup"><span data-stu-id="d3e05-129">Create a wave</span></span>

#### <a name="automatically-create-waves-based-on-warehouse-and-order-type"></a><span data-ttu-id="d3e05-130">根据仓库和订单类型自动创建波次</span><span class="sxs-lookup"><span data-stu-id="d3e05-130">Automatically create waves based on warehouse and order type</span></span>

<span data-ttu-id="d3e05-131">若要自动创建波浪，请设置适用于每个相关订单类型和仓库的[波次模板](wave-templates.md)。</span><span class="sxs-lookup"><span data-stu-id="d3e05-131">To create waves automatically, set up [Wave templates](wave-templates.md) that apply for each relevant order type and warehouse.</span></span> <span data-ttu-id="d3e05-132">确保每个模板都将 **自动波次创建** 选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="d3e05-132">Make sure each template has the **Automate wave creation** option set to *Yes*.</span></span>

#### <a name="manually-create-waves"></a><span data-ttu-id="d3e05-133">手动创建波次</span><span class="sxs-lookup"><span data-stu-id="d3e05-133">Manually create waves</span></span>

<span data-ttu-id="d3e05-134">若要手动创建波次，请按照下列步骤操作：</span><span class="sxs-lookup"><span data-stu-id="d3e05-134">To manually create a wave, follow these steps:</span></span>

1. <span data-ttu-id="d3e05-135">确保相关[波次模板](wave-templates.md)没有设置为自动为仓库和订单类型创建波次，因为您希望手动创建。</span><span class="sxs-lookup"><span data-stu-id="d3e05-135">Make sure that the relevant [Wave templates](wave-templates.md) aren't set to automatically create a wave for the warehouse and order types where you want to do so manually.</span></span>
1. <span data-ttu-id="d3e05-136">根据要创建的波次类型，执行以下操作之一：</span><span class="sxs-lookup"><span data-stu-id="d3e05-136">Depending on the type of wave you want to create, do one of the following:</span></span>

    - <span data-ttu-id="d3e05-137">转到 **仓库管理** \> **通用** \> **波次** \> **装运波次** \> **所有波次**。</span><span class="sxs-lookup"><span data-stu-id="d3e05-137">Go to **Warehouse management** \> **Common** \> **Waves** \> **Shipment waves** \> **All waves**.</span></span> <span data-ttu-id="d3e05-138">在操作窗格上，选择 **波次**。</span><span class="sxs-lookup"><span data-stu-id="d3e05-138">On the Action Pane, select **Wave**.</span></span>
    - <span data-ttu-id="d3e05-139">转到 **仓库管理** \> **通用** \> **波次** \> **生产波次** \> **所有生产波次**。</span><span class="sxs-lookup"><span data-stu-id="d3e05-139">Go to **Warehouse management** \> **Common** \> **Waves** \> **Production waves** \> **All production waves**.</span></span> <span data-ttu-id="d3e05-140">在操作窗格上，选择 **生产波次**。</span><span class="sxs-lookup"><span data-stu-id="d3e05-140">On the Action Pane, select **Production wave**.</span></span>
    - <span data-ttu-id="d3e05-141">转到 **仓库管理** \> **通用** \> **波次** \> **看板波次** \> **所有看板波次**。</span><span class="sxs-lookup"><span data-stu-id="d3e05-141">Go to **Warehouse management** \> **Common** \> **Waves** \> **Kanban waves** \> **All kanban waves**.</span></span> <span data-ttu-id="d3e05-142">在操作窗格上，选择 **创建波次**。</span><span class="sxs-lookup"><span data-stu-id="d3e05-142">On the Action Pane, select **Create wave**.</span></span>

1. <span data-ttu-id="d3e05-143">在 **描述** 字段中，输入波次的简短描述。</span><span class="sxs-lookup"><span data-stu-id="d3e05-143">In the **Description** field, enter a short description of the wave.</span></span> <span data-ttu-id="d3e05-144">这应该表明您在波次中处理的内容。</span><span class="sxs-lookup"><span data-stu-id="d3e05-144">This should indicate what you are processing in the wave.</span></span>

1. <span data-ttu-id="d3e05-145">在 **波次模板名称** 字段中，为要创建的波次类型选择波次模板。</span><span class="sxs-lookup"><span data-stu-id="d3e05-145">In the **Wave template name** field, select the wave template for the type of wave to create.</span></span> <span data-ttu-id="d3e05-146">波次模板包含执行诸如为波次创建工作等操作的波次方法。</span><span class="sxs-lookup"><span data-stu-id="d3e05-146">The wave template contains the wave methods that will perform actions such as creating work for the wave.</span></span> <span data-ttu-id="d3e05-147">例如，装运波次的波次模板可以包含用于创建负荷、将行分配到波次、补货和为波次创建领料工作的方法。</span><span class="sxs-lookup"><span data-stu-id="d3e05-147">For example, the wave template for shipping waves can contain methods for creating loads, allocating lines to waves, replenishment, and creating picking work for the wave.</span></span>

1. <span data-ttu-id="d3e05-148">如果您想要将波次属性用作波次的附加查询条件，请在 **波次属性** 字段中选择属性。</span><span class="sxs-lookup"><span data-stu-id="d3e05-148">If you want to use wave attributes as additional query criteria for the wave, select the attributes in the **Wave attributes** fields.</span></span>

### <a name="specify-what-to-include-in-a-wave"></a><span data-ttu-id="d3e05-149">指定要包括在波次中的内容</span><span class="sxs-lookup"><span data-stu-id="d3e05-149">Specify what to include in a wave</span></span>

<span data-ttu-id="d3e05-150">创建波次后，可以开始向其中添加内容。</span><span class="sxs-lookup"><span data-stu-id="d3e05-150">After a wave has been created, you are ready to start adding content to it.</span></span>

> [!NOTE]
> <span data-ttu-id="d3e05-151">如果需要，只要尚未发放，即可在处理后向波次添加行。</span><span class="sxs-lookup"><span data-stu-id="d3e05-151">If needed, you can add lines to a wave even after it has been processed as long as it has not been released.</span></span>

#### <a name="automatically-specify-what-to-include-in-a-wave"></a><span data-ttu-id="d3e05-152">自动指定要包括在波次中的内容</span><span class="sxs-lookup"><span data-stu-id="d3e05-152">Automatically specify what to include in a wave</span></span>

<span data-ttu-id="d3e05-153">若要自动创建波浪，请设置适用于每个相关订单类型和仓库的[波次模板](wave-templates.md)。</span><span class="sxs-lookup"><span data-stu-id="d3e05-153">To create waves automatically, set up [Wave templates](wave-templates.md) that apply for each relevant order type and warehouse.</span></span> <span data-ttu-id="d3e05-154">确保每个模板都将 **自动波次创建** 选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="d3e05-154">Make sure each template has the **Automate wave creation** option set to *Yes*.</span></span> <span data-ttu-id="d3e05-155">另外，如果 **分配给未结波次** 选项设置为 *是*，您的模板可以自动将行分配给任何符合条件的未结波次。</span><span class="sxs-lookup"><span data-stu-id="d3e05-155">Alternatively, your template could automatically assign lines to any qualifying open wave if the **Assign to open waves** option is set to *Yes*.</span></span>

#### <a name="manually-specify-what-to-include-in-a-wave"></a><span data-ttu-id="d3e05-156">手动指定要包括在波次中的内容</span><span class="sxs-lookup"><span data-stu-id="d3e05-156">Manually specify what to include in a wave</span></span>

<span data-ttu-id="d3e05-157">创建了波次但尚未发布时，您可以手动指定要包括在其中的内容。</span><span class="sxs-lookup"><span data-stu-id="d3e05-157">When a wave has been created but not yet released, you can manually specify what to include in it.</span></span> <span data-ttu-id="d3e05-158">若要手动将行添加到波次：</span><span class="sxs-lookup"><span data-stu-id="d3e05-158">To add lines to a wave manually:</span></span>

1. <span data-ttu-id="d3e05-159">根据要将行添加到的波次类型，执行以下操作之一：</span><span class="sxs-lookup"><span data-stu-id="d3e05-159">Depending on the type of wave to add lines to, do one of the following:</span></span>

    - <span data-ttu-id="d3e05-160">转到 **仓库管理** \> **通用** \> **波次** \> **装运波次** \> **所有波次**。</span><span class="sxs-lookup"><span data-stu-id="d3e05-160">Go to **Warehouse management** \> **Common** \> **Waves** \> **Shipment waves** \> **All waves**.</span></span> <span data-ttu-id="d3e05-161">在操作窗格上，选择 **波次**。</span><span class="sxs-lookup"><span data-stu-id="d3e05-161">On the Action Pane, select **Wave**.</span></span>
    - <span data-ttu-id="d3e05-162">转到 **仓库管理** \> **通用** \> **波次** \> **生产波次** \> **所有生产波次**。</span><span class="sxs-lookup"><span data-stu-id="d3e05-162">Go to **Warehouse management** \> **Common** \> **Waves** \> **Production waves** \> **All production waves**.</span></span> <span data-ttu-id="d3e05-163">在操作窗格上，选择 **生产波次**。</span><span class="sxs-lookup"><span data-stu-id="d3e05-163">On the Action Pane, select **Production wave**.</span></span>
    - <span data-ttu-id="d3e05-164">转到 **仓库管理** \> **通用** \> **波次** \> **看板波次** \> **所有看板波次**。</span><span class="sxs-lookup"><span data-stu-id="d3e05-164">Go to **Warehouse management** \> **Common** \> **Waves** \> **Kanban waves** \> **All kanban waves**.</span></span> <span data-ttu-id="d3e05-165">在操作窗格上，选择 **创建波次**。</span><span class="sxs-lookup"><span data-stu-id="d3e05-165">On the Action Pane, select **Create wave**.</span></span>

1. <span data-ttu-id="d3e05-166">选择波次。</span><span class="sxs-lookup"><span data-stu-id="d3e05-166">Select the wave.</span></span> <span data-ttu-id="d3e05-167">在操作窗格上，选择以下项之一：</span><span class="sxs-lookup"><span data-stu-id="d3e05-167">On the Action Pane, select one of the following:</span></span>

      - <span data-ttu-id="d3e05-168">**维护装运**</span><span class="sxs-lookup"><span data-stu-id="d3e05-168">**Maintain shipments**</span></span>
      - <span data-ttu-id="d3e05-169">**维护生产**</span><span class="sxs-lookup"><span data-stu-id="d3e05-169">**Maintain productions**</span></span>
      - <span data-ttu-id="d3e05-170">**维护看板作业领料单**</span><span class="sxs-lookup"><span data-stu-id="d3e05-170">**Maintain kanban job picking lists**</span></span>

1. <span data-ttu-id="d3e05-171">在窗口的上半部分中，选择要添加到波次的行，然后选择 **添加到波次** 。</span><span class="sxs-lookup"><span data-stu-id="d3e05-171">In the upper part of the window, select the line to add to the wave, and then select **Add to wave**.</span></span> <span data-ttu-id="d3e05-172">该行将移动到 **波次行** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="d3e05-172">The line is moved to the **Wave lines** FastTab.</span></span>

    <span data-ttu-id="d3e05-173">针对要添加的每个行重复此步骤。</span><span class="sxs-lookup"><span data-stu-id="d3e05-173">Repeat this step for each line to add.</span></span> <span data-ttu-id="d3e05-174">若要添加所有行，请选择 **全部添加**。</span><span class="sxs-lookup"><span data-stu-id="d3e05-174">To add all lines, select **Add all**.</span></span>

    > [!TIP]
    > <span data-ttu-id="d3e05-175">对于装运波次，您可以通过在 **波次筛选器代码** 字段中选择自定义筛选器来快速查找特定订单。</span><span class="sxs-lookup"><span data-stu-id="d3e05-175">For shipment waves, you can quickly find a specific order by selecting a custom filter in the **Wave filter code** field.</span></span> <span data-ttu-id="d3e05-176">波次筛选器代码包含在 **波次筛选器** 窗体中创建的装运的查询条件。</span><span class="sxs-lookup"><span data-stu-id="d3e05-176">Wave filter codes contain query criteria for shipments, which are created in the **Wave filters** form.</span></span> <span data-ttu-id="d3e05-177">此字段对生产波次或看板波次不可用。</span><span class="sxs-lookup"><span data-stu-id="d3e05-177">This field is not available for production waves or kanban waves.</span></span>
    > <span data-ttu-id="d3e05-178">**在波次上** 列中的绿色复选标记指示该装运已添加到波次。</span><span class="sxs-lookup"><span data-stu-id="d3e05-178">A green check mark in the **On wave** column indicates that the shipment has been added to the wave.</span></span>

### <a name="process-the-wave-to-create-the-picking-work"></a><span data-ttu-id="d3e05-179">处理波次以创建领料工作</span><span class="sxs-lookup"><span data-stu-id="d3e05-179">Process the wave to create the picking work</span></span>

<span data-ttu-id="d3e05-180">在波次已创建并包含所有所需的行之后，您可以处理它以创建相应的领料工作。</span><span class="sxs-lookup"><span data-stu-id="d3e05-180">After a wave has been created and contains all of its required lines, you are ready to process it to create the corresponding picking work.</span></span>

#### <a name="automatically-process-a-wave"></a><span data-ttu-id="d3e05-181">自动处理波次</span><span class="sxs-lookup"><span data-stu-id="d3e05-181">Automatically process a wave</span></span>

<span data-ttu-id="d3e05-182">若要自动处理波次，请使用所需的自动处理选项设置相关的[波次模板](wave-templates.md)。</span><span class="sxs-lookup"><span data-stu-id="d3e05-182">To automatically process a wave, set up the relevant [Wave templates](wave-templates.md) with the automatic processing options required.</span></span>

#### <a name="manually-process-a-wave"></a><span data-ttu-id="d3e05-183">手动处理波次</span><span class="sxs-lookup"><span data-stu-id="d3e05-183">Manually process a wave</span></span>

<span data-ttu-id="d3e05-184">仅在 **波次状态** 为 *已创建* 时才能处理波次。</span><span class="sxs-lookup"><span data-stu-id="d3e05-184">You can process a wave only when the **Wave status** is *Created*.</span></span> <span data-ttu-id="d3e05-185">处理完波次后，**波次状态** 将更改为 *预留*。</span><span class="sxs-lookup"><span data-stu-id="d3e05-185">After you process a wave, the **Wave status** will be changed to *Held*.</span></span>

<span data-ttu-id="d3e05-186">若要手动处理具有所有所需内容的波次，请按照下列步骤操作：</span><span class="sxs-lookup"><span data-stu-id="d3e05-186">To manually process a wave that has all of its required content, follow these steps:</span></span>

1. <span data-ttu-id="d3e05-187">根据要处理的波次类型，执行以下操作之一：</span><span class="sxs-lookup"><span data-stu-id="d3e05-187">Depending on the type of wave to process, do one of the following:</span></span>

    - <span data-ttu-id="d3e05-188">选择 **仓库管理** \> **通用** \> **波次** \> **装运波次** \> **所有波次**。</span><span class="sxs-lookup"><span data-stu-id="d3e05-188">Select **Warehouse management** \> **Common** \> **Waves** \> **Shipment waves** \> **All waves**.</span></span> <span data-ttu-id="d3e05-189">在操作窗格上，选择 **波次**。</span><span class="sxs-lookup"><span data-stu-id="d3e05-189">On the Action Pane, select **Wave**.</span></span>
    - <span data-ttu-id="d3e05-190">选择 **仓库管理** \> **通用** \> **波次** \> **生产波次** \> **所有生产波次**。</span><span class="sxs-lookup"><span data-stu-id="d3e05-190">Select **Warehouse management** \> **Common** \> **Waves** \> **Production waves** \> **All production waves**.</span></span> <span data-ttu-id="d3e05-191">在操作窗格上，选择 **生产波次**。</span><span class="sxs-lookup"><span data-stu-id="d3e05-191">On the Action Pane, select **Production wave**.</span></span>
    - <span data-ttu-id="d3e05-192">选择 **仓库管理** \> **通用** \> **波次** \> **看板波次** \> **所有看板波次**。</span><span class="sxs-lookup"><span data-stu-id="d3e05-192">Select **Warehouse management** \> **Common** \> **Waves** \> **Kanban waves** \> **All kanban waves**.</span></span> <span data-ttu-id="d3e05-193">在操作窗格上，选择 **创建波次**。</span><span class="sxs-lookup"><span data-stu-id="d3e05-193">On the Action Pane, select **Create wave**.</span></span>

1. <span data-ttu-id="d3e05-194">选择要处理的波次。</span><span class="sxs-lookup"><span data-stu-id="d3e05-194">Select the wave to process.</span></span> <span data-ttu-id="d3e05-195">在“操作窗格”上，选择 **流程**。</span><span class="sxs-lookup"><span data-stu-id="d3e05-195">On the Action Pane, select **Process**.</span></span>

### <a name="release-the-wave-to-the-warehouse-to-start-picking-and-packing"></a><span data-ttu-id="d3e05-196">将波次发放到仓库以开始领料和包装</span><span class="sxs-lookup"><span data-stu-id="d3e05-196">Release the wave to the warehouse to start picking and packing</span></span>

<span data-ttu-id="d3e05-197">您必须先处理波次，然后才能发放它。</span><span class="sxs-lookup"><span data-stu-id="d3e05-197">You must process a wave before you can release it.</span></span> <span data-ttu-id="d3e05-198">发放波次后，即可在仓库中进行领料工作。</span><span class="sxs-lookup"><span data-stu-id="d3e05-198">When you release the wave, the picking work is available in the warehouse.</span></span> <span data-ttu-id="d3e05-199">您可以在发放波次后将其取消，添加更多行，但无法更改行。</span><span class="sxs-lookup"><span data-stu-id="d3e05-199">You can cancel a wave after it is released, and add more lines, but you can't change the lines.</span></span>

#### <a name="automatically-release-a-wave"></a><span data-ttu-id="d3e05-200">自动发放波次</span><span class="sxs-lookup"><span data-stu-id="d3e05-200">Automatically release a wave</span></span>

<span data-ttu-id="d3e05-201">若要自动处理波次，请使用所需的自动处理选项设置相关的[波次模板](wave-templates.md)。</span><span class="sxs-lookup"><span data-stu-id="d3e05-201">To automatically process a wave, set up the relevant [Wave templates](wave-templates.md) with the automatic processing options required.</span></span>

#### <a name="manually-release-a-wave"></a><span data-ttu-id="d3e05-202">手动发放波次</span><span class="sxs-lookup"><span data-stu-id="d3e05-202">Manually release a wave</span></span>

<span data-ttu-id="d3e05-203">若要手动发放波次，请按照下列步骤操作：</span><span class="sxs-lookup"><span data-stu-id="d3e05-203">To release a wave manually, follow these steps:</span></span>

1. <span data-ttu-id="d3e05-204">根据要发放的波次类型，执行以下操作之一：</span><span class="sxs-lookup"><span data-stu-id="d3e05-204">Depending on the type of wave to release, do one of the following:</span></span>

      - <span data-ttu-id="d3e05-205">选择 **仓库管理** \> **通用** \> **波次** \> **装运波次** \> **所有波次**。</span><span class="sxs-lookup"><span data-stu-id="d3e05-205">Select **Warehouse management** \> **Common** \> **Waves** \> **Shipment waves** \> **All waves**.</span></span> <span data-ttu-id="d3e05-206">在操作窗格上，选择 **波次**。</span><span class="sxs-lookup"><span data-stu-id="d3e05-206">On the Action Pane, select **Wave**.</span></span>
      - <span data-ttu-id="d3e05-207">选择 **仓库管理** \> **通用** \> **波次** \> **生产波次** \> **所有生产波次**。</span><span class="sxs-lookup"><span data-stu-id="d3e05-207">Select **Warehouse management** \> **Common** \> **Waves** \> **Production waves** \> **All production waves**.</span></span> <span data-ttu-id="d3e05-208">在操作窗格上，选择 **生产波次**。</span><span class="sxs-lookup"><span data-stu-id="d3e05-208">On the Action Pane, select **Production wave**.</span></span>
      - <span data-ttu-id="d3e05-209">选择 **仓库管理** \> **通用** \> **波次** \> **看板波次** \> **所有看板波次**。</span><span class="sxs-lookup"><span data-stu-id="d3e05-209">Select **Warehouse management** \> **Common** \> **Waves** \> **Kanban waves** \> **All kanban waves**.</span></span> <span data-ttu-id="d3e05-210">在操作窗格上，选择 **创建波次**。</span><span class="sxs-lookup"><span data-stu-id="d3e05-210">On the Action Pane, select **Create wave**.</span></span>

1. <span data-ttu-id="d3e05-211">选择要发放的波次。</span><span class="sxs-lookup"><span data-stu-id="d3e05-211">Select the wave to release.</span></span> <span data-ttu-id="d3e05-212">在操作窗格上，选择 **发放波次**。</span><span class="sxs-lookup"><span data-stu-id="d3e05-212">On the Action Pane, select **Release wave**.</span></span>

## <a name="containerize-a-wave"></a><span data-ttu-id="d3e05-213">集装化波次</span><span class="sxs-lookup"><span data-stu-id="d3e05-213">Containerize a wave</span></span>

<span data-ttu-id="d3e05-214">在处理波次时，自动集装化创建集装箱和装运的领料工作。</span><span class="sxs-lookup"><span data-stu-id="d3e05-214">Automated containerization creates containers and the picking work for shipments when a wave is processed.</span></span> <span data-ttu-id="d3e05-215">有关如何设置的详细信息，请参阅[集装化](wave-containerization.md)。</span><span class="sxs-lookup"><span data-stu-id="d3e05-215">For details about how to set it up, see [Containerization](wave-containerization.md).</span></span>

## <a name="work-with-the-scheduled-work-creation"></a><span data-ttu-id="d3e05-216">使用计划工作创建</span><span class="sxs-lookup"><span data-stu-id="d3e05-216">Work with the scheduled work creation</span></span>

<span data-ttu-id="d3e05-217">启用 *计划工作创建* 功能后，波次处理将创建计划工作，其最终将由新工作创建流程使用。</span><span class="sxs-lookup"><span data-stu-id="d3e05-217">When the *Schedule work creation* functionality is enabled, wave processing will create planned work, which will eventually be used by the new work creation process.</span></span> <span data-ttu-id="d3e05-218">在创建工作期间，将使用 *组织范围内的工作锁定* 功能来阻止工作。</span><span class="sxs-lookup"><span data-stu-id="d3e05-218">During work creation, the work will be blocked using the *Organization-wide work blocking* feature.</span></span> <span data-ttu-id="d3e05-219">有关详细信息，请参阅[在波次期间计划工作创建](configure-wave-schedule-work-creation.md)。</span><span class="sxs-lookup"><span data-stu-id="d3e05-219">For more information, see [Schedule work creation during wave](configure-wave-schedule-work-creation.md).</span></span>

<span data-ttu-id="d3e05-220">以下流程图显示了波次处理期间计划工作是如何创建的。</span><span class="sxs-lookup"><span data-stu-id="d3e05-220">The following flowchart shows how planned work is created during wave processing.</span></span>

![计划工作创建](media/schedule-work-creation-process.png)

### <a name="planned-work"></a><span data-ttu-id="d3e05-222">计划的工作</span><span class="sxs-lookup"><span data-stu-id="d3e05-222">Planned work</span></span>

<span data-ttu-id="d3e05-223">**计划工作详细信息** 页面（**仓库管理 \> 工作 \> 计划工作详细信息**）显示有关计划工作的信息，此信息最初在波次处理期间创建。</span><span class="sxs-lookup"><span data-stu-id="d3e05-223">The **Planned work details** page (**Warehouse management \> Work \> Planned work details**) shows information about the planned work, which is initially created during wave processing.</span></span> <span data-ttu-id="d3e05-224">提供以下 **流程状态** 值：</span><span class="sxs-lookup"><span data-stu-id="d3e05-224">The following **Process status** values are available:</span></span>

- <span data-ttu-id="d3e05-225">**已排队** - 计划工作正在等待用于创建工作。</span><span class="sxs-lookup"><span data-stu-id="d3e05-225">**Queued** - The planned work is waiting to be used to create work.</span></span>
- <span data-ttu-id="d3e05-226">**已完成** - 计划工作已用于创建工作。</span><span class="sxs-lookup"><span data-stu-id="d3e05-226">**Completed** - The planned work has been used to create work.</span></span>
- <span data-ttu-id="d3e05-227">**失败** – 波次处理失败。</span><span class="sxs-lookup"><span data-stu-id="d3e05-227">**Failed** – The wave processing has failed.</span></span> <span data-ttu-id="d3e05-228">请注意，无论是否有相关的实际工作，计划工作都可能处于 **失败** 状态。</span><span class="sxs-lookup"><span data-stu-id="d3e05-228">Note that the planned work can be in a **Failed** state with or without related actual work.</span></span> <span data-ttu-id="d3e05-229">当实际工作创建流程失败时，实际工作保持 *已取消* 状态。</span><span class="sxs-lookup"><span data-stu-id="d3e05-229">When the actual work creation process fails, the actual work remains in status *Cancelled*.</span></span>

### <a name="batch-job-for-the-work-creation-process"></a><span data-ttu-id="d3e05-230">工作创建流程的批处理作业</span><span class="sxs-lookup"><span data-stu-id="d3e05-230">Batch job for the work creation process</span></span>

<span data-ttu-id="d3e05-231">要查看处理波次的批处理作业，在 **所有波次** 页上的操作窗格中选择 **批处理作业**。</span><span class="sxs-lookup"><span data-stu-id="d3e05-231">To view the batch jobs for processing waves, select **Batch jobs** on the Action Pane on the **All waves** page.</span></span>

<span data-ttu-id="d3e05-232">从这里，您可以查看每个批处理作业 ID 的所有批处理任务详细信息。</span><span class="sxs-lookup"><span data-stu-id="d3e05-232">From here, you can view all the batch task details for each of the batch job IDs.</span></span>

## <a name="cancel-a-wave"></a><span data-ttu-id="d3e05-233">取消波次</span><span class="sxs-lookup"><span data-stu-id="d3e05-233">Cancel a wave</span></span>

<span data-ttu-id="d3e05-234">如果需要，您可以取消已处理的波次。</span><span class="sxs-lookup"><span data-stu-id="d3e05-234">If needed, you can cancel a wave that has been processed.</span></span> <span data-ttu-id="d3e05-235">若要取消波次和已创建的领料工作，请按照下列步骤操作：</span><span class="sxs-lookup"><span data-stu-id="d3e05-235">To cancel a wave, and the picking work that was created, follow these steps:</span></span>

1. <span data-ttu-id="d3e05-236">根据要取消的波次类型，执行以下操作之一：</span><span class="sxs-lookup"><span data-stu-id="d3e05-236">Depending on the type of wave to cancel, do one of the following:</span></span>

      - <span data-ttu-id="d3e05-237">转到 **仓库管理** \> **通用** \> **波次** \> **装运波次** \> **所有波次**。</span><span class="sxs-lookup"><span data-stu-id="d3e05-237">Go to **Warehouse management** \> **Common** \> **Waves** \> **Shipment waves** \> **All waves**.</span></span>
      - <span data-ttu-id="d3e05-238">转到 **仓库管理** \> **通用** \> **波次** \> **生产波次** \> **所有生产波次**。</span><span class="sxs-lookup"><span data-stu-id="d3e05-238">Go to **Warehouse management** \> **Common** \> **Waves** \> **Production waves** \> **All production waves**.</span></span>
      - <span data-ttu-id="d3e05-239">转到 **仓库管理** \> **通用** \> **波次** \> **看板波次** \> **所有看板波次**。</span><span class="sxs-lookup"><span data-stu-id="d3e05-239">Go to **Warehouse management** \> **Common** \> **Waves** \> **Kanban waves** \> **All kanban waves**.</span></span>

1. <span data-ttu-id="d3e05-240">选择要取消的波次。</span><span class="sxs-lookup"><span data-stu-id="d3e05-240">Select the wave to cancel.</span></span> <span data-ttu-id="d3e05-241">在操作窗格上的 **工作** 选项卡上，选择 **取消**。</span><span class="sxs-lookup"><span data-stu-id="d3e05-241">On the Action Pane, on the **Work** tab, select **Cancel**.</span></span>

## <a name="review-wave-batch-job-details"></a><span data-ttu-id="d3e05-242">查看波次批处理作业详细信息</span><span class="sxs-lookup"><span data-stu-id="d3e05-242">Review wave batch job details</span></span>

<span data-ttu-id="d3e05-243">使用 **波次批处理作业详细信息** 页面以检查与任何波次关联的批处理作业和相关任务。</span><span class="sxs-lookup"><span data-stu-id="d3e05-243">Use the **Wave batch job details** page to inspect the batch jobs and related tasks associated with any wave.</span></span> <span data-ttu-id="d3e05-244">这对于解决已失败的波次特别有用。</span><span class="sxs-lookup"><span data-stu-id="d3e05-244">This is especially useful for troubleshooting a wave that has failed.</span></span> <span data-ttu-id="d3e05-245">如果没有此功能，通常只有管理员才能访问批处理作业详细信息。</span><span class="sxs-lookup"><span data-stu-id="d3e05-245">Without this feature, only administrators will typically have access to batch job details.</span></span> <span data-ttu-id="d3e05-246">**波次批处理作业详细信息** 页面可以供非管理员用户使用，并提供批处理作业和相关任务的只读视图。</span><span class="sxs-lookup"><span data-stu-id="d3e05-246">The **Wave batch job details** page can be made available to non-admin users and provides a read-only view of batch jobs and related tasks.</span></span>

### <a name="enable-the-wave-batch-job-details-page"></a><span data-ttu-id="d3e05-247">启用波次批处理作业详细信息页面</span><span class="sxs-lookup"><span data-stu-id="d3e05-247">Enable the Wave batch job details page</span></span>

<span data-ttu-id="d3e05-248">如果您的系统尚未包括 **波次批处理作业详细信息** 页面，转到 [功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)并打开 *波次批处理作业详细信息* 功能。</span><span class="sxs-lookup"><span data-stu-id="d3e05-248">If your system doesn't already include the **Wave batch job details** page, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the *Wave batch job details* feature.</span></span>

### <a name="use-the-wave-batch-job-details-page"></a><span data-ttu-id="d3e05-249">使用波次批处理作业详细信息页面</span><span class="sxs-lookup"><span data-stu-id="d3e05-249">Use the Wave batch job details page</span></span>

<span data-ttu-id="d3e05-250">**波次批处理作业详细信息** 页面将批处理作业和批处理作业任务相结合，使您可以调查所有波次步骤，无需在单个批处理作业和批处理任务列表之间来回导航。</span><span class="sxs-lookup"><span data-stu-id="d3e05-250">The **Wave batch job details** page combines batch jobs and batch job tasks, which lets you investigate all the wave steps without needing to navigate back and forth between a single batch job and the batch tasks list.</span></span> <span data-ttu-id="d3e05-251">该页面还提供对批处理日志的访问权限，如果您具有必需的权限，则提供指向 **批处理作业** 页面的链接。</span><span class="sxs-lookup"><span data-stu-id="d3e05-251">The page also provides access to the batch log and, if you have the required permissions, provides a link to the **Batch jobs** page.</span></span>

<span data-ttu-id="d3e05-252">若要打开此页面，请在几个不同的波次页面的任一页面上选择波次，然后从操作窗格中选择 **波次批处理作业详细信息**。</span><span class="sxs-lookup"><span data-stu-id="d3e05-252">To open this page, select a wave on any of several different wave pages and then select **Wave batch job details** from the Action Pane.</span></span>

## <a name="review-load-validation-and-error-messages"></a><span data-ttu-id="d3e05-253">查看负荷验证和错误消息</span><span class="sxs-lookup"><span data-stu-id="d3e05-253">Review load validation and error messages</span></span>

<span data-ttu-id="d3e05-254">在波次处理期间，系统会验证并显示波次中每个负荷行的状态。</span><span class="sxs-lookup"><span data-stu-id="d3e05-254">During wave processing, the system validates and displays the status for each load line in the wave.</span></span> <span data-ttu-id="d3e05-255">如果没有出现警告，则继续下一个波次步骤。</span><span class="sxs-lookup"><span data-stu-id="d3e05-255">If no warnings occur, it continues to the next wave step.</span></span> <span data-ttu-id="d3e05-256">如果确实出现警告，在完成验证整个波次后，将改为显示以下错误：</span><span class="sxs-lookup"><span data-stu-id="d3e05-256">If warnings do occur, it instead shows the following error after it has finished validating the entire wave:</span></span>

> <span data-ttu-id="d3e05-257">在波次中找到了无效的负荷行。</span><span class="sxs-lookup"><span data-stu-id="d3e05-257">Found invalid load lines in wave.</span></span> <span data-ttu-id="d3e05-258">请删除无效的负荷行。</span><span class="sxs-lookup"><span data-stu-id="d3e05-258">Please remove the invalid load lines.</span></span>

<span data-ttu-id="d3e05-259">然后，您可以查看波次中每个负荷行的最终状态，并在再次尝试之前更正所有警告。</span><span class="sxs-lookup"><span data-stu-id="d3e05-259">You are then able to review the final status of each load line in the wave and correct all warnings before trying again.</span></span> <span data-ttu-id="d3e05-260">这使您可以在重新处理波次之前，立即解决所有警告。</span><span class="sxs-lookup"><span data-stu-id="d3e05-260">This lets you address all the warnings at once before reprocessing the wave.</span></span> <span data-ttu-id="d3e05-261">（在以前的版本中，系统在第一个警告之后停止处理波次，因此您一次只能修复一个警告。）</span><span class="sxs-lookup"><span data-stu-id="d3e05-261">(In previous releases, the system stopped processing the wave after the first warning, so you could only fix warnings one at a time.)</span></span>

<span data-ttu-id="d3e05-262">系统显示波次处理状态消息的方式取决于您如何设置 **仓库管理参数** 页面上的 **创建波次处理历史记录日志** 选项。</span><span class="sxs-lookup"><span data-stu-id="d3e05-262">The way the system displays your wave processing status messages depends on how you have set the **Create wave processing history log** option on the **Warehouse management parameters** page.</span></span>

- <span data-ttu-id="d3e05-263">当 **创建波次处理历史记录日志** 设置为 *否* 时，负荷行状态消息显示在 **信息日志** 中。</span><span class="sxs-lookup"><span data-stu-id="d3e05-263">When **Create wave processing history log** is set to *No*, the load line status messages are shown in the **Infolog**.</span></span>
- <span data-ttu-id="d3e05-264">当 **创建波次处理历史记录日志** 设置为 *是* 时，负荷行状态消息显示在 **波次处理历史记录日志** 页面上。</span><span class="sxs-lookup"><span data-stu-id="d3e05-264">When **Create wave processing history log** is set to *Yes*, the load line status messages are shown on the **Wave processing history log** page.</span></span> <span data-ttu-id="d3e05-265">若要查看日志，请转到 **仓库管理 \> 出库波次 \> 波次处理历史记录日志**。</span><span class="sxs-lookup"><span data-stu-id="d3e05-265">To view the log, go to **Warehouse management \> Outbound waves \> Wave processing history log**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d3e05-266">其他资源</span><span class="sxs-lookup"><span data-stu-id="d3e05-266">Additional resources</span></span>

- [<span data-ttu-id="d3e05-267">配置波次处理示例</span><span class="sxs-lookup"><span data-stu-id="d3e05-267">Configure wave processing example</span></span>](tasks/configure-wave-processing.md)
- [<span data-ttu-id="d3e05-268">波次模板</span><span class="sxs-lookup"><span data-stu-id="d3e05-268">Wave templates</span></span>](wave-templates.md)
- [<span data-ttu-id="d3e05-269">集装化</span><span class="sxs-lookup"><span data-stu-id="d3e05-269">Containerization</span></span>](wave-containerization.md)