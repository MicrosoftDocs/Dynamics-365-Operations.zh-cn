---
title: 设置和使用波次标签打印
description: 本主题介绍了波次标签打印并解释了如何进行设置。
author: GarmMSFT
manager: PJacobse
ms.date: 05/01/2020
ms.topic: configure-wave-label-printing
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate
audience: Application User
ms.reviewer: PJacobse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: yyyy-mm-dd
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: e3b04eea7bd7dd689f8a918820ffdb4a72d813dc
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986015"
---
# <a name="set-up-and-use-wave-label-printing"></a><span data-ttu-id="143ca-103">设置和使用波次标签打印</span><span class="sxs-lookup"><span data-stu-id="143ca-103">Set up and use wave label printing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="143ca-104">波次标签打印通过引入新波次步骤方法提供另一种标签打印方法，让您可以在波次执行过程中直接从波次模板创建和打印标签。</span><span class="sxs-lookup"><span data-stu-id="143ca-104">Wave label printing offers an alternative approach to label printing by introducing a new wave step method that lets you create and print labels directly from the wave template during wave execution.</span></span> <span data-ttu-id="143ca-105">因此，在工作人员在移动设备上运行工作订单之前，标签已经可用。</span><span class="sxs-lookup"><span data-stu-id="143ca-105">Therefore, the labels will already be available before workers run the work order on a mobile device.</span></span> <span data-ttu-id="143ca-106">然后，工作人员可以在领料期间而不是领料后附上所需的标签。</span><span class="sxs-lookup"><span data-stu-id="143ca-106">Workers can then attach the required labels during picking instead of after picking.</span></span>

<span data-ttu-id="143ca-107">波次标签打印使用 Zebra 编程语言 (ZPL) 来创建标签布局。</span><span class="sxs-lookup"><span data-stu-id="143ca-107">Wave label printing uses Zebra Programming Language (ZPL) to create label layouts.</span></span> <span data-ttu-id="143ca-108">标签布局分为三个部分（页眉、主体和页脚），以允许具有重复结构的标签。</span><span class="sxs-lookup"><span data-stu-id="143ca-108">A label layout is divided into three sections (header, body, and footer) to allow for labels that have repeating structure.</span></span> <span data-ttu-id="143ca-109">波次标签模板告诉系统要使用的标签布局。</span><span class="sxs-lookup"><span data-stu-id="143ca-109">Wave label templates tell the system which label layout to use.</span></span> <span data-ttu-id="143ca-110">用户可以指定使用哪台打印机。</span><span class="sxs-lookup"><span data-stu-id="143ca-110">Users can specify which printer is used.</span></span> <span data-ttu-id="143ca-111">他们还可以根据需要同时在多台打印机上打印标签。</span><span class="sxs-lookup"><span data-stu-id="143ca-111">They can also print labels on several printers at the same time, as they require.</span></span> <span data-ttu-id="143ca-112">**波次标签历史记录**页面显示使用此设置创建的所有标签的记录。</span><span class="sxs-lookup"><span data-stu-id="143ca-112">The **Wave label history** page shows a record of all labels that have been created by using this setup.</span></span>

<span data-ttu-id="143ca-113">您可以根据工作标题打印和逐份打印标签，可以为每个工作标题打印中断标签，还可以打印集装箱内容标签、外箱标签和其他类似标签。</span><span class="sxs-lookup"><span data-stu-id="143ca-113">You can print and collate labels based on work headers, you can print break labels per work header, and you can print container content labels, case labels, and other similar labels.</span></span>

> [!NOTE]
> <span data-ttu-id="143ca-114">此功能不会替代基于文档路线的现有标签打印功能。</span><span class="sxs-lookup"><span data-stu-id="143ca-114">This functionality doesn't replace existing label printing functionality that is based on document routing.</span></span>

<span data-ttu-id="143ca-115">波次标签打印提供以下增强功能：</span><span class="sxs-lookup"><span data-stu-id="143ca-115">Wave label printing offers the following enhancements:</span></span>

- <span data-ttu-id="143ca-116">根据一个工作行上的货箱数量打印标签，无需使用集装化。</span><span class="sxs-lookup"><span data-stu-id="143ca-116">Print labels according to the number of cartons on a single work line, without using containerization.</span></span> <span data-ttu-id="143ca-117">（“货箱”是在单位序列组行上指定的单位。）</span><span class="sxs-lookup"><span data-stu-id="143ca-117">(A "carton" is a unit that is designated on unit sequence group lines.)</span></span>
- <span data-ttu-id="143ca-118">打印几个不同的标签序列（例如，货箱和托盘标签）。</span><span class="sxs-lookup"><span data-stu-id="143ca-118">Print several different label sequences (for example, carton and pallet labels).</span></span>
- <span data-ttu-id="143ca-119">加入标签枚举（例如，1/124、2/124 ... 124/124），并定义枚举的范围（例如，工作行、负荷行或装运）。</span><span class="sxs-lookup"><span data-stu-id="143ca-119">Include label enumeration (for example, 1/124, 2/124, ... 124/124), and define the range of enumeration (for example, work line, load line, or shipment).</span></span>
- <span data-ttu-id="143ca-120">在生成提单之前，在标签上创建和打印提单 ID。</span><span class="sxs-lookup"><span data-stu-id="143ca-120">Create and print a bill of lading ID on labels before the bill of lading is generated.</span></span>
- <span data-ttu-id="143ca-121">为每个货箱创建唯一的系列货运集装箱代码 (SSCC)，并将其加入每个标签。</span><span class="sxs-lookup"><span data-stu-id="143ca-121">Create a unique serial shipping container code (SSCC) for each carton, and include it on each label.</span></span>
- <span data-ttu-id="143ca-122">为提单 ID 和 SSCC 创建符合 GS1 的编号规则。</span><span class="sxs-lookup"><span data-stu-id="143ca-122">Create GS1-compliant number sequences for bill of lading IDs and SSCCs.</span></span>
- <span data-ttu-id="143ca-123">重新打印来自移动设备和富客户端的标签。</span><span class="sxs-lookup"><span data-stu-id="143ca-123">Reprint labels from both mobile devices and the rich client.</span></span>
- <span data-ttu-id="143ca-124">取消标签（例如，在领料短缺情景中），然后重新打印。</span><span class="sxs-lookup"><span data-stu-id="143ca-124">Void labels (for example, in short pick scenarios), and reprint them.</span></span>
- <span data-ttu-id="143ca-125">清除波次标签历史记录。</span><span class="sxs-lookup"><span data-stu-id="143ca-125">Clean up the wave label history.</span></span>
- <span data-ttu-id="143ca-126">在文档路线布局和波次标签布局之间共享对文档路线布局的改进。</span><span class="sxs-lookup"><span data-stu-id="143ca-126">Improvements to document routing layouts are shared between document routing layouts and wave label layouts.</span></span> <span data-ttu-id="143ca-127">（有关详细信息，请参阅[牌照的文档路线布局](../warehousing/document-routing-layout-for-license-plates.md)）</span><span class="sxs-lookup"><span data-stu-id="143ca-127">(For more information, see [Document routing layout for license plates](../warehousing/document-routing-layout-for-license-plates.md).)</span></span>

<span data-ttu-id="143ca-128">这些增强功能让在安装货盘前为货箱附加标签更加高效。</span><span class="sxs-lookup"><span data-stu-id="143ca-128">These enhancements make it more efficient to label cartons before palletization.</span></span> <span data-ttu-id="143ca-129">它们特别有利于向那些通过分别扫描每个货箱自动确认订单收货的大型零售商发货的公司。</span><span class="sxs-lookup"><span data-stu-id="143ca-129">They especially benefit companies that ship to large retailers that automatically confirm order receipts by scanning each carton separately.</span></span>

> [!NOTE]
> <span data-ttu-id="143ca-130">您可以根据业务要求单独或组合实现本主题中介绍的配置方案。</span><span class="sxs-lookup"><span data-stu-id="143ca-130">You can implement the configuration scenarios that are described in this topic either separately or in combination, depending on your business requirements.</span></span> <span data-ttu-id="143ca-131">您可以设计几个按顺序工作的波次标签模板（如方案 3 所示）。</span><span class="sxs-lookup"><span data-stu-id="143ca-131">You can design several wave label templates that work in sequence (as illustrated in scenario 3).</span></span> <span data-ttu-id="143ca-132">例如，您可以使用方案 1 打印货箱标签，使用方案 2 打印托盘标签（如果存货的托盘在尺寸和构成方面不同）。</span><span class="sxs-lookup"><span data-stu-id="143ca-132">For example, you can use scenario 1 to print carton labels and scenario 2 to print pallet labels (if pallets in stock vary in size and composition).</span></span>

## <a name="turn-on-the-wave-label-printing-feature"></a><span data-ttu-id="143ca-133">开启波次标签打印功能</span><span class="sxs-lookup"><span data-stu-id="143ca-133">Turn on the Wave label printing feature</span></span>

<span data-ttu-id="143ca-134">*波次标签打印*功能只有在系统中开启之后才能使用。</span><span class="sxs-lookup"><span data-stu-id="143ca-134">Before you can use the *Wave label printing* feature, it must be turned on in your system.</span></span> <span data-ttu-id="143ca-135">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区检查功能状态和开启功能（如果需要）。</span><span class="sxs-lookup"><span data-stu-id="143ca-135">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="143ca-136">在那里，此功能以以下方式列出：</span><span class="sxs-lookup"><span data-stu-id="143ca-136">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="143ca-137">**模块**：*仓库管理*</span><span class="sxs-lookup"><span data-stu-id="143ca-137">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="143ca-138">**功能名称**：*波次标签打印*</span><span class="sxs-lookup"><span data-stu-id="143ca-138">**Feature name:** *Wave label printing*</span></span>

## <a name="scenario-1-wave-label-printing-where-a-single-wave-label-is-generated"></a><span data-ttu-id="143ca-139">方案 1：生成单个波次标签的波次标签打印</span><span class="sxs-lookup"><span data-stu-id="143ca-139">Scenario 1: Wave label printing where a single wave label is generated</span></span>

<span data-ttu-id="143ca-140">此方案演示公司如何为通过分别扫描每个货箱来自动确认订单收货的大型零售商打印发货标签。</span><span class="sxs-lookup"><span data-stu-id="143ca-140">This scenario shows how a company can print shipping labels for a large retailer that automatically confirms order receipts by scanning each carton separately.</span></span>

<span data-ttu-id="143ca-141">此方案演示端到端流。</span><span class="sxs-lookup"><span data-stu-id="143ca-141">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="143ca-142">提供演示数据</span><span class="sxs-lookup"><span data-stu-id="143ca-142">Make demo data available</span></span>

<span data-ttu-id="143ca-143">要采取此方案，必须安装演示数据，并且必须选择 **USMF** 法人。</span><span class="sxs-lookup"><span data-stu-id="143ca-143">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-the-wave-label-method-is-available"></a><span data-ttu-id="143ca-144">确保波次标签方法可用</span><span class="sxs-lookup"><span data-stu-id="143ca-144">Make sure that the wave label method is available</span></span>

<span data-ttu-id="143ca-145">您可能必须重新生成波次处理方法，才能使波次标签打印方法可用。</span><span class="sxs-lookup"><span data-stu-id="143ca-145">You might have to regenerate the wave process methods to make the wave label printing method available.</span></span>

1. <span data-ttu-id="143ca-146">转到**仓库管理 \> 设置 \> 波次 \> 波次处理方法**。</span><span class="sxs-lookup"><span data-stu-id="143ca-146">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="143ca-147">确认 **waveLabelPrinting** 在列表中。</span><span class="sxs-lookup"><span data-stu-id="143ca-147">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="143ca-148">如果不在，请在操作窗格中选择**重新生成方法**添加该方法。</span><span class="sxs-lookup"><span data-stu-id="143ca-148">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="configure-a-wave-template"></a><span data-ttu-id="143ca-149">配置波次模板</span><span class="sxs-lookup"><span data-stu-id="143ca-149">Configure a wave template</span></span>

<span data-ttu-id="143ca-150">波次模板使您可以将波次方法的特定实例链接到相应的波次标签模板。</span><span class="sxs-lookup"><span data-stu-id="143ca-150">Wave templates let you link specific instances of wave methods to a corresponding wave label template.</span></span>

1. <span data-ttu-id="143ca-151">转到**仓库管理 \> 设置 \> 波次 \> 波次模板**。</span><span class="sxs-lookup"><span data-stu-id="143ca-151">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="143ca-152">选择模板，如 **62 装运默认**。</span><span class="sxs-lookup"><span data-stu-id="143ca-152">Select a template, such as **62 Shipping Default**.</span></span>
1. <span data-ttu-id="143ca-153">在**方法**快速选项卡上，将**波次标签打印**方法移至**选定方法**列。</span><span class="sxs-lookup"><span data-stu-id="143ca-153">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
1. <span data-ttu-id="143ca-154">在**选定方法**列中，选择**波次标签打印**方法，并将其**波次步骤代码**字段设置为 *PrintLabel*。</span><span class="sxs-lookup"><span data-stu-id="143ca-154">In the **Selected methods** column, select the **Wave label printing** method, and set its **Wave step code** field to *PrintLabel*.</span></span> <span data-ttu-id="143ca-155">有关波次步骤代码的详细信息，请参阅[波次步骤代码](wave-step-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="143ca-155">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-a-wave-label-layout"></a><span data-ttu-id="143ca-156">创建波次标签布局</span><span class="sxs-lookup"><span data-stu-id="143ca-156">Create a wave label layout</span></span>

<span data-ttu-id="143ca-157">标签布局控制在标签上打印什么信息以及如何布置信息。在这里，您输入发送到打印机的 ZPL 代码。</span><span class="sxs-lookup"><span data-stu-id="143ca-157">The label layout controls what information is printed on the label and how it's laid out. Here, you enter the ZPL code that is sent to the printer.</span></span>

1. <span data-ttu-id="143ca-158">转到**仓库管理 \> 设置 \> 文档路线布局 \> 波次标签布局**。</span><span class="sxs-lookup"><span data-stu-id="143ca-158">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="143ca-159">创建一个具有以下设置的记录：</span><span class="sxs-lookup"><span data-stu-id="143ca-159">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="143ca-160">**标签布局 ID**：*Carton*</span><span class="sxs-lookup"><span data-stu-id="143ca-160">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="143ca-161">**描述**：*货箱 (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="143ca-161">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="143ca-162">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="143ca-162">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="143ca-163">在操作窗格上，选择**波次标签行设置**。</span><span class="sxs-lookup"><span data-stu-id="143ca-163">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="143ca-164">**波次标签行设置**页面将出现。</span><span class="sxs-lookup"><span data-stu-id="143ca-164">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="143ca-165">在这里，您可以配置标签的动态部分。</span><span class="sxs-lookup"><span data-stu-id="143ca-165">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="143ca-166">添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="143ca-166">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="143ca-167">**行 ID**：*WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="143ca-167">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="143ca-168">**行表名称**：*WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="143ca-168">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="143ca-169">**行开始位置**：*0*</span><span class="sxs-lookup"><span data-stu-id="143ca-169">**Row start position:** *0*</span></span>

        <span data-ttu-id="143ca-170">此字段定义行在标签上开始的垂直位置。</span><span class="sxs-lookup"><span data-stu-id="143ca-170">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="143ca-171">**行高度**：*0*</span><span class="sxs-lookup"><span data-stu-id="143ca-171">**Row height:** *0*</span></span>

        <span data-ttu-id="143ca-172">此字段根据 ZPL 标准定义每行的高度（以磅为单位）。</span><span class="sxs-lookup"><span data-stu-id="143ca-172">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="143ca-173">行高度对于水平标签为正，对于垂直标签为负。</span><span class="sxs-lookup"><span data-stu-id="143ca-173">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="143ca-174">在此示例中因为只有一行，所以您可以将此值设置为 *0*（零）。</span><span class="sxs-lookup"><span data-stu-id="143ca-174">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="143ca-175">**每页行数**：*1*</span><span class="sxs-lookup"><span data-stu-id="143ca-175">**Rows per page:** *1*</span></span>

        <span data-ttu-id="143ca-176">此字段定义可以在每个标签上打印的行数。</span><span class="sxs-lookup"><span data-stu-id="143ca-176">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="143ca-177">使用此设置，将为波次标签表中的每个记录打印一个单独的 ZPL 标签。</span><span class="sxs-lookup"><span data-stu-id="143ca-177">This setup will cause a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="143ca-178">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="143ca-178">Close the page.</span></span>
1. <span data-ttu-id="143ca-179">在操作窗格上，选择**编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="143ca-179">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="143ca-180">在查询编辑器对话框的**范围**选项卡上，添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="143ca-180">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="143ca-181">**表**：*工作行*</span><span class="sxs-lookup"><span data-stu-id="143ca-181">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="143ca-182">**派生表**：*工作行*</span><span class="sxs-lookup"><span data-stu-id="143ca-182">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="143ca-183">**字段**：*工作类型*</span><span class="sxs-lookup"><span data-stu-id="143ca-183">**Field:** *Work type*</span></span>
    - <span data-ttu-id="143ca-184">**条件**：*领料*</span><span class="sxs-lookup"><span data-stu-id="143ca-184">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="143ca-185">此查询可确保在标签上仅打印领料类型的工作行，不打印放置类型的工作行。</span><span class="sxs-lookup"><span data-stu-id="143ca-185">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="143ca-186">如果您希望能够打印提单 ID，请在**联接**选项卡上，选择**工作行**表，然后将**装运**表与其联接。</span><span class="sxs-lookup"><span data-stu-id="143ca-186">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="143ca-187">关闭查询编辑器对话框。</span><span class="sxs-lookup"><span data-stu-id="143ca-187">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="143ca-188">**打印机文本布局**快速选项卡有三个部分，您可以在其中编写打印机代码：**页眉部分**、**主体部分**和**页脚部分**。</span><span class="sxs-lookup"><span data-stu-id="143ca-188">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="143ca-189">在**页眉部分**的**标签页眉**字段中，输入所需页眉的代码。</span><span class="sxs-lookup"><span data-stu-id="143ca-189">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="143ca-190">例如，如果您使用的是 Zebra 打印机，可以使用以下代码。</span><span class="sxs-lookup"><span data-stu-id="143ca-190">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. <span data-ttu-id="143ca-191">在**主体部分**的**标签主体**字段中，输入所需主体的 ZPL 代码。</span><span class="sxs-lookup"><span data-stu-id="143ca-191">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="143ca-192">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="143ca-192">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. <span data-ttu-id="143ca-193">在**主体部分**的**标签页脚**字段中，输入所需页脚的 ZPL 代码。</span><span class="sxs-lookup"><span data-stu-id="143ca-193">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="143ca-194">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="143ca-194">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="143ca-195">此设置将打印每个标签的一个副本。</span><span class="sxs-lookup"><span data-stu-id="143ca-195">This setup will print one copy of each label.</span></span> <span data-ttu-id="143ca-196">如果需要更多副本（例如，托盘每一面一个副本），请将页脚中 **\^PQn** 部分的 **n** 值设置为所需的副本数。</span><span class="sxs-lookup"><span data-stu-id="143ca-196">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="143ca-197">例如，每个标签要打印四个副本，请指定 **\^PQ4**。</span><span class="sxs-lookup"><span data-stu-id="143ca-197">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

<span data-ttu-id="143ca-198">您的标签现在可以使用了。</span><span class="sxs-lookup"><span data-stu-id="143ca-198">Your label is now ready to use.</span></span>

### <a name="create-a-wave-label-type"></a><span data-ttu-id="143ca-199">创建波次标签类型</span><span class="sxs-lookup"><span data-stu-id="143ca-199">Create a wave label type</span></span>

<span data-ttu-id="143ca-200">波次标签类型用于将波次标签模板链接到单元序列组行上的单元。</span><span class="sxs-lookup"><span data-stu-id="143ca-200">Wave label types are used to link wave label templates to a unit on unit sequence group lines.</span></span>

1. <span data-ttu-id="143ca-201">转到**仓库管理 \> 设置 \> 文档路线布局 \> 波次标签类型**。</span><span class="sxs-lookup"><span data-stu-id="143ca-201">Go to **Warehouse management \> Setup \> Document routing \> Wave label types**.</span></span>
1. <span data-ttu-id="143ca-202">添加具有以下设置的波次标签类型：</span><span class="sxs-lookup"><span data-stu-id="143ca-202">Add a wave label type that has the following settings:</span></span>

    - <span data-ttu-id="143ca-203">**标签类型**：*货箱*</span><span class="sxs-lookup"><span data-stu-id="143ca-203">**Label type:** *Carton*</span></span>
    - <span data-ttu-id="143ca-204">**描述**：*货箱*</span><span class="sxs-lookup"><span data-stu-id="143ca-204">**Description:** *Carton*</span></span>

### <a name="set-up-unit-sequence-groups"></a><span data-ttu-id="143ca-205">设置单位序列组</span><span class="sxs-lookup"><span data-stu-id="143ca-205">Set up unit sequence groups</span></span>

<span data-ttu-id="143ca-206">接下来，设置波次标签类型的单位序列组。</span><span class="sxs-lookup"><span data-stu-id="143ca-206">Next, set up the unit sequence group for the wave label type.</span></span>

1. <span data-ttu-id="143ca-207">转到**仓库管理 \> 设置 \> 仓库 \> 单位序列组**。</span><span class="sxs-lookup"><span data-stu-id="143ca-207">Go to **Warehouse management \> Setup \> Warehouse \> Unit sequence groups**.</span></span>
1. <span data-ttu-id="143ca-208">选择 **Ea Box PL** 组。</span><span class="sxs-lookup"><span data-stu-id="143ca-208">Select the **Ea Box PL** group.</span></span>
1. <span data-ttu-id="143ca-209">对于**箱**行，将**波次级别类型**字段设置为*货箱*。</span><span class="sxs-lookup"><span data-stu-id="143ca-209">For the **Box** line, set the **Wave level type** field to *Carton*.</span></span>

### <a name="create-a-wave-label-template"></a><span data-ttu-id="143ca-210">创建波次标签模板</span><span class="sxs-lookup"><span data-stu-id="143ca-210">Create a wave label template</span></span>

<span data-ttu-id="143ca-211">接下来，为波次标签类型创建波次标签模板。</span><span class="sxs-lookup"><span data-stu-id="143ca-211">Next, create the wave label template for the wave label type.</span></span>

1. <span data-ttu-id="143ca-212">转到**仓库管理 \> 设置 \> 文档路线布局 \> 波次标签模板**。</span><span class="sxs-lookup"><span data-stu-id="143ca-212">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="143ca-213">添加波次级别模板，并在页眉中设置以下值：</span><span class="sxs-lookup"><span data-stu-id="143ca-213">Add a wave level template, and set the following values in the header:</span></span>

    - <span data-ttu-id="143ca-214">**标签模板名称**：*货箱标签*</span><span class="sxs-lookup"><span data-stu-id="143ca-214">**Label template name:** *Carton labels*</span></span>
    - <span data-ttu-id="143ca-215">**描述**：*货箱标签*</span><span class="sxs-lookup"><span data-stu-id="143ca-215">**Description:** *Carton labels*</span></span>
    - <span data-ttu-id="143ca-216">**波次步骤代码**：*PrintLabel*</span><span class="sxs-lookup"><span data-stu-id="143ca-216">**Wave step code:** *PrintLabel*</span></span>
    - <span data-ttu-id="143ca-217">**仓库**：*62*</span><span class="sxs-lookup"><span data-stu-id="143ca-217">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="143ca-218">在**常规**快速选项卡上，将**波次标签类型**字段设置为*货箱*。</span><span class="sxs-lookup"><span data-stu-id="143ca-218">On the **General** FastTab, set the **Wave label type** field to *Carton*.</span></span>
1. <span data-ttu-id="143ca-219">在**波次标签模板详细信息**快速选项卡上，添加具有以下设置的新行：</span><span class="sxs-lookup"><span data-stu-id="143ca-219">On the **Wave label template details** FastTab, add a new row that has the following settings:</span></span>

    - <span data-ttu-id="143ca-220">**标签布局 ID**：*Carton*</span><span class="sxs-lookup"><span data-stu-id="143ca-220">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="143ca-221">**打印机名称：** 选择适当的 ZPL 打印机。</span><span class="sxs-lookup"><span data-stu-id="143ca-221">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="143ca-222">**运行查询**：*是*（此设置是可选的，但建议使用此设置以获得最佳性能。）</span><span class="sxs-lookup"><span data-stu-id="143ca-222">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="143ca-223">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="143ca-223">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="143ca-224">可选：如果要设置客户特定的标签设计，则必须创建查询来查找客户的帐户。</span><span class="sxs-lookup"><span data-stu-id="143ca-224">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="143ca-225">在**波次标签模板详细信息**快速选项卡上，选择**编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="143ca-225">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="143ca-226">然后，在查询编辑器对话框的**范围**选项卡上，添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="143ca-226">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="143ca-227">**表**：*装运*</span><span class="sxs-lookup"><span data-stu-id="143ca-227">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="143ca-228">**派生表**：*装运*</span><span class="sxs-lookup"><span data-stu-id="143ca-228">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="143ca-229">**字段**：*帐号*</span><span class="sxs-lookup"><span data-stu-id="143ca-229">**Field:** *Account number*</span></span>
    - <span data-ttu-id="143ca-230">**条件：** 输入相关的客户帐号。</span><span class="sxs-lookup"><span data-stu-id="143ca-230">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="143ca-231">完成后，选择**确定**关闭查询编辑器对话框。</span><span class="sxs-lookup"><span data-stu-id="143ca-231">When you've finished, select **OK** to close the query editor dialog box.</span></span>

1. <span data-ttu-id="143ca-232">在操作窗格上，选择**编辑查询**打开整个标签模板的查询编辑器对话框。</span><span class="sxs-lookup"><span data-stu-id="143ca-232">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="143ca-233">在查询编辑器对话框的**排序**选项卡上，添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="143ca-233">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="143ca-234">**表**：*工作行*</span><span class="sxs-lookup"><span data-stu-id="143ca-234">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="143ca-235">**派生表**：*工作行*</span><span class="sxs-lookup"><span data-stu-id="143ca-235">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="143ca-236">**字段**：*参考负荷行 ID（记录 ID）*</span><span class="sxs-lookup"><span data-stu-id="143ca-236">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="143ca-237">**搜索方向**：*升序*</span><span class="sxs-lookup"><span data-stu-id="143ca-237">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="143ca-238">选择**确定**关闭查询编辑器对话框。</span><span class="sxs-lookup"><span data-stu-id="143ca-238">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="143ca-239">一个消息框将提示您确认分组重置操作。</span><span class="sxs-lookup"><span data-stu-id="143ca-239">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="143ca-240">选择**是**继续。</span><span class="sxs-lookup"><span data-stu-id="143ca-240">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="143ca-241">在操作窗格上，选择**波次标签模板组**。</span><span class="sxs-lookup"><span data-stu-id="143ca-241">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="143ca-242">在**波次标签模板组**对话框中，选择**参考字段名称**字段设置为*参考负荷行 ID* 的行，然后选择此行的**标签生成 ID** 复选框。</span><span class="sxs-lookup"><span data-stu-id="143ca-242">In the **Wave label template group** dialog box, select the row where the **Reference field name** field is set to *Reference load line id*, and then select the **Label build ID** check box for this row.</span></span>

    > [!NOTE]
    > <span data-ttu-id="143ca-243">无论工作分组设置如何，此设置都会在整个波次中为每个负荷行创建一个标签序列（“货箱 1/X”）。</span><span class="sxs-lookup"><span data-stu-id="143ca-243">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="143ca-244">此标签序列可以打印在标签布局上。</span><span class="sxs-lookup"><span data-stu-id="143ca-244">This label sequence can be printed on the label layout.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="143ca-245">配置编号规则扩展</span><span class="sxs-lookup"><span data-stu-id="143ca-245">Configure number sequence extensions</span></span>

<span data-ttu-id="143ca-246">编号规则扩展控制特定编号规则的 GS1 符合性。</span><span class="sxs-lookup"><span data-stu-id="143ca-246">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="143ca-247">此配置对于当前方案是可选的。</span><span class="sxs-lookup"><span data-stu-id="143ca-247">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="143ca-248">有关详细信息和配置说明，请参阅[配置编号规则扩展](../warehousing/configure-number-sequence-extensions.md)。</span><span class="sxs-lookup"><span data-stu-id="143ca-248">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="143ca-249">创建销售订单并将其下达到仓库</span><span class="sxs-lookup"><span data-stu-id="143ca-249">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="143ca-250">转到**销售和营销 \> 销售订单 \> 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="143ca-250">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="143ca-251">创建具有以下设置的销售订单：</span><span class="sxs-lookup"><span data-stu-id="143ca-251">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="143ca-252">**客户帐户**：*US-001*</span><span class="sxs-lookup"><span data-stu-id="143ca-252">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="143ca-253">**仓库**：*62*</span><span class="sxs-lookup"><span data-stu-id="143ca-253">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="143ca-254">添加两个具有以下设置的销售订单行：</span><span class="sxs-lookup"><span data-stu-id="143ca-254">Add two sales order lines that have the following settings:</span></span>

    - <span data-ttu-id="143ca-255">销售订单行 1：</span><span class="sxs-lookup"><span data-stu-id="143ca-255">Sales order line 1:</span></span>

        - <span data-ttu-id="143ca-256">\**物料编号：\*\*\*A0001*</span><span class="sxs-lookup"><span data-stu-id="143ca-256">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="143ca-257">**数量：** *9024*</span><span class="sxs-lookup"><span data-stu-id="143ca-257">**Quantity:** *9024*</span></span>
        - <span data-ttu-id="143ca-258">**单位**：*个* (9024 个 = 376 箱 = 47 PL)</span><span class="sxs-lookup"><span data-stu-id="143ca-258">**Unit:** *ea* (9024 ea = 376 Box = 47 PL)</span></span>

    - <span data-ttu-id="143ca-259">销售订单行 2：</span><span class="sxs-lookup"><span data-stu-id="143ca-259">Sales order line 2:</span></span>

        - <span data-ttu-id="143ca-260">\**物料编号：\*\*\*A0002*</span><span class="sxs-lookup"><span data-stu-id="143ca-260">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="143ca-261">**数量：** *9016*</span><span class="sxs-lookup"><span data-stu-id="143ca-261">**Quantity:** *9016*</span></span>
        - <span data-ttu-id="143ca-262">**单位**：*个* (9016 个 = 322 箱 = 46 PL)</span><span class="sxs-lookup"><span data-stu-id="143ca-262">**Unit:** *ea* (9016 ea = 322 Box = 46 PL)</span></span>

    > [!NOTE]
    > <span data-ttu-id="143ca-263">此处提供的物料和数量仅是示例。</span><span class="sxs-lookup"><span data-stu-id="143ca-263">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="143ca-264">它们必须使用您先前定义的单位序列组，必须为它们定义从*个*到*箱*再到 *PL* 的适当单位转换，并且它们在仓库 *62* 中必须有存货。</span><span class="sxs-lookup"><span data-stu-id="143ca-264">They must use the unit sequence group that you defined earlier, appropriate unit conversions from *ea* to *Box* to *PL* must be defined for them, and they must have stock in warehouse *62*.</span></span> <span data-ttu-id="143ca-265">有关详细信息，请参阅[度量单位和库存策略](unit-measure-stocking-policies.md)。</span><span class="sxs-lookup"><span data-stu-id="143ca-265">For more information, see [Unit of measure and stocking policies](unit-measure-stocking-policies.md).</span></span>

1. <span data-ttu-id="143ca-266">选择销售订单行 1。</span><span class="sxs-lookup"><span data-stu-id="143ca-266">Select sales order line 1.</span></span> <span data-ttu-id="143ca-267">然后，在**销售订单行**部分的**库存**菜单中，选择**预留**。</span><span class="sxs-lookup"><span data-stu-id="143ca-267">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="143ca-268">在**预留**页的操作窗格中，选择**预留批次**，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="143ca-268">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="143ca-269">对销售订单行 2 重复步骤 4 和 5。</span><span class="sxs-lookup"><span data-stu-id="143ca-269">Repeat steps 4 and 5 for sales order line 2.</span></span>
1. <span data-ttu-id="143ca-270">在“操作窗格”上的**仓库**选项卡上，选择**发放到仓库**。</span><span class="sxs-lookup"><span data-stu-id="143ca-270">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="143ca-271">将发生以下事件：</span><span class="sxs-lookup"><span data-stu-id="143ca-271">The following events occur:</span></span>

    - <span data-ttu-id="143ca-272">系统使用包含标签打印步骤的模板来处理创建的装运。</span><span class="sxs-lookup"><span data-stu-id="143ca-272">The system processes the created shipment by using the template that includes the label printing step.</span></span> <span data-ttu-id="143ca-273">标签布局将用于定义标签的格式，结果将是在标签模板中选择的打印机上打印的标签。</span><span class="sxs-lookup"><span data-stu-id="143ca-273">The label layout will be used to define the format of the label, and the result will be a label that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="143ca-274">波次标签将生成并打印。</span><span class="sxs-lookup"><span data-stu-id="143ca-274">Wave labels are generated and printed.</span></span> <span data-ttu-id="143ca-275">标签数量将等于货箱数量（在此示例中，行 1 是 376 箱标签，行 2 是 322 箱标签）。</span><span class="sxs-lookup"><span data-stu-id="143ca-275">The number of labels will equal the number of cartons (in this example, 376 Box labels for line 1 and 322 Box labels for line 2).</span></span>
    - <span data-ttu-id="143ca-276">将为装运生成新提单 ID。</span><span class="sxs-lookup"><span data-stu-id="143ca-276">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="143ca-277">如果您配置了数字序列扩展，波次标签 ID 将采用 **SSCC-18** 数字格式。</span><span class="sxs-lookup"><span data-stu-id="143ca-277">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="143ca-278">您可以从以下页面查看和重新打印波次标签。</span><span class="sxs-lookup"><span data-stu-id="143ca-278">You can view and reprint wave labels from the following pages.</span></span> <span data-ttu-id="143ca-279">在每页的“操作窗格”上的**装运**选项卡上，在**相关信息**组中，选择**波次标签**。</span><span class="sxs-lookup"><span data-stu-id="143ca-279">On the Action Pane of each page, on the **Shipments** tab, in the **Related information** group, select **Wave labels**.</span></span>

- <span data-ttu-id="143ca-280">所有装运 \> 装运详细信息</span><span class="sxs-lookup"><span data-stu-id="143ca-280">All shipments \> Shipment details</span></span>
- <span data-ttu-id="143ca-281">所有负荷 \> 负荷详细信息</span><span class="sxs-lookup"><span data-stu-id="143ca-281">All loads \> Load details</span></span>
- <span data-ttu-id="143ca-282">所有波次</span><span class="sxs-lookup"><span data-stu-id="143ca-282">All waves</span></span>
- <span data-ttu-id="143ca-283">波次标签</span><span class="sxs-lookup"><span data-stu-id="143ca-283">Wave labels</span></span>
- <span data-ttu-id="143ca-284">波次标签历史记录</span><span class="sxs-lookup"><span data-stu-id="143ca-284">Wave label history</span></span>

## <a name="scenario-2-wave-label-printing-for-containerization-without-wave-label-records"></a><span data-ttu-id="143ca-285">方案 2：集装化的波次标签打印（不使用波次标签记录）</span><span class="sxs-lookup"><span data-stu-id="143ca-285">Scenario 2: Wave label printing for containerization (without wave label records)</span></span>

<span data-ttu-id="143ca-286">此方案使您可以在使用集装化自动将物料拆分到货箱时打印波次标签，因此不需要波次标签记录。</span><span class="sxs-lookup"><span data-stu-id="143ca-286">This scenario lets you print wave labels when you use containerization to automatically split items into cartons and therefore don't require a wave label record.</span></span> <span data-ttu-id="143ca-287">在这种情况下，集装箱 ID 充当 SSCC 的占位符。</span><span class="sxs-lookup"><span data-stu-id="143ca-287">In this case, the container ID acts as a placeholder for the SSCC.</span></span>

<span data-ttu-id="143ca-288">以下是此方案与方案 1 之间的主要区别：</span><span class="sxs-lookup"><span data-stu-id="143ca-288">Here are the main differences between this scenario and scenario 1:</span></span>

- <span data-ttu-id="143ca-289">**波次标签模板：** 您无需在波次标签模板上选择波次标签类型，也不需要标签生成分组。</span><span class="sxs-lookup"><span data-stu-id="143ca-289">**Wave label templates:** You won't select a wave label type on the wave label template, and you won't require a label build grouping.</span></span> <span data-ttu-id="143ca-290">另外，您将按照方案 1 中所述的相同方式配置波次标签模板并链接到波次模板。</span><span class="sxs-lookup"><span data-stu-id="143ca-290">Otherwise, you will configure the wave label template and link to the wave template in the same way that is described in scenario 1.</span></span> <span data-ttu-id="143ca-291">您必须将波次标签类型保留为空白，以防止生成波次标签。</span><span class="sxs-lookup"><span data-stu-id="143ca-291">You must leave the wave label type blank to prevent wave labels from being generated.</span></span>
- <span data-ttu-id="143ca-292">**波次标签布局：** 您将为工作行（而不是波次标签记录）配置波次标签布局行设置。</span><span class="sxs-lookup"><span data-stu-id="143ca-292">**Wave label layouts:** You will configure the wave label layout row settings for work lines instead of wave label records.</span></span> <span data-ttu-id="143ca-293">您必须使用 **WHSWorkLine** 表而不是 **WHSWaveLabel** 表来配置标签布局的行设置。</span><span class="sxs-lookup"><span data-stu-id="143ca-293">You must configure the row setting for the label layout by using the **WHSWorkLine** table instead of the **WHSWaveLabel** table.</span></span> <span data-ttu-id="143ca-294">**每页行数**设置控制主体部分将具有的行数。</span><span class="sxs-lookup"><span data-stu-id="143ca-294">The **Rows per page** setting controls the number of rows that the body section will have.</span></span> 

<span data-ttu-id="143ca-295">此配置也适用于将多个不同物料包装到一个带标签的箱子或托盘的业务场景，此包装流程可以通过创建工作（例如，按装运分组的工作）定义。</span><span class="sxs-lookup"><span data-stu-id="143ca-295">This configuration is also suitable for business scenarios where multiple different items are packed into one labeled box or into a pallet, and this packing process can be defined by work creation (for example, work that is grouped by shipment).</span></span>

<span data-ttu-id="143ca-296">此方案演示端到端流。</span><span class="sxs-lookup"><span data-stu-id="143ca-296">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="143ca-297">提供演示数据</span><span class="sxs-lookup"><span data-stu-id="143ca-297">Make demo data available</span></span>

<span data-ttu-id="143ca-298">要采取此方案，必须安装演示数据，并且必须选择 **USMF** 法人。</span><span class="sxs-lookup"><span data-stu-id="143ca-298">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-the-wave-label-method-is-available"></a><span data-ttu-id="143ca-299">确保波次标签方法可用</span><span class="sxs-lookup"><span data-stu-id="143ca-299">Make sure that the wave label method is available</span></span>

<span data-ttu-id="143ca-300">您可能必须重新生成波次处理方法，才能使波次标签打印方法可用。</span><span class="sxs-lookup"><span data-stu-id="143ca-300">You might have to regenerate the wave process methods to make the wave label printing method available.</span></span>

1. <span data-ttu-id="143ca-301">转到**仓库管理 \> 设置 \> 波次 \> 波次处理方法**。</span><span class="sxs-lookup"><span data-stu-id="143ca-301">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="143ca-302">确认 **waveLabelPrinting** 在列表中。</span><span class="sxs-lookup"><span data-stu-id="143ca-302">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="143ca-303">如果不在，请在操作窗格中选择**重新生成方法**添加该方法。</span><span class="sxs-lookup"><span data-stu-id="143ca-303">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="143ca-304">设置波次模板</span><span class="sxs-lookup"><span data-stu-id="143ca-304">Set up a wave template</span></span>

<span data-ttu-id="143ca-305">波次模板使您可以将波次方法的特定实例链接到相应的波次标签模板。</span><span class="sxs-lookup"><span data-stu-id="143ca-305">Wave templates let you link specific instances of wave methods to a corresponding wave label template.</span></span>

1. <span data-ttu-id="143ca-306">转到**仓库管理 \> 设置 \> 波次 \> 波次模板**。</span><span class="sxs-lookup"><span data-stu-id="143ca-306">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="143ca-307">选择模板，如 **63 集装化**。</span><span class="sxs-lookup"><span data-stu-id="143ca-307">Select a template, such as **63 Containerization**.</span></span>
1. <span data-ttu-id="143ca-308">在**方法**快速选项卡上，将**波次标签打印**方法移至**选定方法**列。</span><span class="sxs-lookup"><span data-stu-id="143ca-308">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
1. <span data-ttu-id="143ca-309">在**选定方法**列中，选择**波次标签打印**方法，并将其**波次步骤代码**字段设置为 *PrintLabel*。</span><span class="sxs-lookup"><span data-stu-id="143ca-309">In the **Selected methods** column, select the **Wave label printing** method, and set its **Wave step code** field to *PrintLabel*.</span></span> <span data-ttu-id="143ca-310">有关波次步骤代码的详细信息，请参阅[波次步骤代码](wave-step-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="143ca-310">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-a-wave-label-layout"></a><span data-ttu-id="143ca-311">创建波次标签布局</span><span class="sxs-lookup"><span data-stu-id="143ca-311">Create a wave label layout</span></span>

1. <span data-ttu-id="143ca-312">转到**仓库管理 \> 设置 \> 文档路线布局 \> 波次标签布局**。</span><span class="sxs-lookup"><span data-stu-id="143ca-312">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="143ca-313">创建一个具有以下设置的记录：</span><span class="sxs-lookup"><span data-stu-id="143ca-313">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="143ca-314">**标签布局 ID**：*Carton*</span><span class="sxs-lookup"><span data-stu-id="143ca-314">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="143ca-315">**描述**：*货箱 (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="143ca-315">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="143ca-316">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="143ca-316">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="143ca-317">在操作窗格上，选择**波次标签行设置**。</span><span class="sxs-lookup"><span data-stu-id="143ca-317">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="143ca-318">**波次标签行设置**页面将出现。</span><span class="sxs-lookup"><span data-stu-id="143ca-318">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="143ca-319">在这里，您可以配置标签的动态部分。</span><span class="sxs-lookup"><span data-stu-id="143ca-319">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="143ca-320">添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="143ca-320">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="143ca-321">**行 ID**：*WorkLine*</span><span class="sxs-lookup"><span data-stu-id="143ca-321">**Row Id:** *WorkLine*</span></span>
    - <span data-ttu-id="143ca-322">**行表名称**：*WHSWorkLine*</span><span class="sxs-lookup"><span data-stu-id="143ca-322">**Row table name:** *WHSWorkLine*</span></span>
    - <span data-ttu-id="143ca-323">**行开始位置**：*500*</span><span class="sxs-lookup"><span data-stu-id="143ca-323">**Row start position:** *500*</span></span>

        <span data-ttu-id="143ca-324">此字段定义行在标签上开始的垂直位置。</span><span class="sxs-lookup"><span data-stu-id="143ca-324">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="143ca-325">**行高度**：*-50*</span><span class="sxs-lookup"><span data-stu-id="143ca-325">**Row height:** *-50*</span></span>

        <span data-ttu-id="143ca-326">此字段定义每行的高度。</span><span class="sxs-lookup"><span data-stu-id="143ca-326">This field defines the height of each row.</span></span> <span data-ttu-id="143ca-327">行高度对于水平标签为正，对于垂直标签为负。</span><span class="sxs-lookup"><span data-stu-id="143ca-327">The row height is positive for horizontal labels and negative for vertical labels.</span></span>

    - <span data-ttu-id="143ca-328">**每页行数**：*5*</span><span class="sxs-lookup"><span data-stu-id="143ca-328">**Rows per page:** *5*</span></span>

        <span data-ttu-id="143ca-329">此字段定义可以在每个标签上打印的行数。</span><span class="sxs-lookup"><span data-stu-id="143ca-329">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="143ca-330">此设置将为每个工作打印若干 ZPL 标签，每个页面最多可以保留五个工作行。</span><span class="sxs-lookup"><span data-stu-id="143ca-330">This setup will print several ZPL labels per work, where each page can hold up to five work lines.</span></span> <span data-ttu-id="143ca-331">例如，如果为具有 12 行的集装箱打印标签，将打印三个标签。</span><span class="sxs-lookup"><span data-stu-id="143ca-331">For example, if a label is printed for a container that has 12 lines, three labels will be printed.</span></span> <span data-ttu-id="143ca-332">如果要为每个领料行打印单独的标签，请将此值设置为 *1*。</span><span class="sxs-lookup"><span data-stu-id="143ca-332">If you want to print a separate label for each pick line, set this value to *1*.</span></span>

1. <span data-ttu-id="143ca-333">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="143ca-333">Close the page.</span></span>
1. <span data-ttu-id="143ca-334">在操作窗格上，选择**编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="143ca-334">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="143ca-335">在查询编辑器对话框的**范围**选项卡上，添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="143ca-335">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="143ca-336">**表**：*工作行*</span><span class="sxs-lookup"><span data-stu-id="143ca-336">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="143ca-337">**派生表**：*工作行*</span><span class="sxs-lookup"><span data-stu-id="143ca-337">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="143ca-338">**字段**：*工作类型*</span><span class="sxs-lookup"><span data-stu-id="143ca-338">**Field:** *Work type*</span></span>
    - <span data-ttu-id="143ca-339">**条件**：*领料*</span><span class="sxs-lookup"><span data-stu-id="143ca-339">**Criteria:** *Pick*</span></span>

1. <span data-ttu-id="143ca-340">如果您希望能够打印提单 ID，请在**联接**选项卡上，选择**工作行**表，然后将**装运**表与其联接。</span><span class="sxs-lookup"><span data-stu-id="143ca-340">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="143ca-341">关闭查询编辑器对话框。</span><span class="sxs-lookup"><span data-stu-id="143ca-341">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="143ca-342">**打印机文本布局**快速选项卡有三个部分，您可以在其中编写打印机代码：**页眉部分**、**主体部分**和**页脚部分**。</span><span class="sxs-lookup"><span data-stu-id="143ca-342">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="143ca-343">在**页眉部分**的**标签页眉**字段中，输入所需页眉的代码。</span><span class="sxs-lookup"><span data-stu-id="143ca-343">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="143ca-344">例如，如果您使用的是 Zebra 打印机，可以使用以下代码。</span><span class="sxs-lookup"><span data-stu-id="143ca-344">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkTable.ContainerId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. <span data-ttu-id="143ca-345">在**主体部分**的**标签主体**字段中，输入所需主体的 ZPL 代码。</span><span class="sxs-lookup"><span data-stu-id="143ca-345">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="143ca-346">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="143ca-346">Here is an example.</span></span>

    ```plaintext
    <Row name="WorkLine">
    <Heading>
    //Optional heading for section of rows
    </Heading>
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWorkLine.ItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWorkLine.QtyWork$ ^FS
    </Row>
    ```

1. <span data-ttu-id="143ca-347">在**主体部分**的**标签页脚**字段中，输入所需页脚的 ZPL 代码。</span><span class="sxs-lookup"><span data-stu-id="143ca-347">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="143ca-348">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="143ca-348">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="143ca-349">此设置将打印每个标签的一个副本。</span><span class="sxs-lookup"><span data-stu-id="143ca-349">This setup will print one copy of each label.</span></span> <span data-ttu-id="143ca-350">如果需要更多副本（例如，托盘每一面一个副本），请将页脚中 **\^PQn** 部分的 **n** 值设置为所需的副本数。</span><span class="sxs-lookup"><span data-stu-id="143ca-350">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="143ca-351">例如，每个标签要打印四个副本，请指定 **\^PQ4**。</span><span class="sxs-lookup"><span data-stu-id="143ca-351">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

<span data-ttu-id="143ca-352">您的标签现在可以使用了。</span><span class="sxs-lookup"><span data-stu-id="143ca-352">Your label is now ready to use.</span></span>

### <a name="create-a-wave-label-template"></a><span data-ttu-id="143ca-353">创建波次标签模板</span><span class="sxs-lookup"><span data-stu-id="143ca-353">Create a wave label template</span></span>

1. <span data-ttu-id="143ca-354">转到**仓库管理 \> 设置 \> 文档路线布局 \> 波次标签模板**。</span><span class="sxs-lookup"><span data-stu-id="143ca-354">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="143ca-355">添加波次级别模板，并在页眉中设置以下值：</span><span class="sxs-lookup"><span data-stu-id="143ca-355">Add a wave level template, and set the following values in the header:</span></span>

    - <span data-ttu-id="143ca-356">**标签模板名称**：*集装箱标签*</span><span class="sxs-lookup"><span data-stu-id="143ca-356">**Label template name:** *Container labels*</span></span>
    - <span data-ttu-id="143ca-357">**描述**：*集装箱标签*</span><span class="sxs-lookup"><span data-stu-id="143ca-357">**Description:** *Container labels*</span></span>
    - <span data-ttu-id="143ca-358">**波次步骤代码**：*PrintLabel*</span><span class="sxs-lookup"><span data-stu-id="143ca-358">**Wave step code:** *PrintLabel*</span></span>
    - <span data-ttu-id="143ca-359">**仓库**：*63*</span><span class="sxs-lookup"><span data-stu-id="143ca-359">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="143ca-360">在**波次标签模板详细信息**快速选项卡上，添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="143ca-360">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="143ca-361">**标签布局 ID**：*Container*</span><span class="sxs-lookup"><span data-stu-id="143ca-361">**Label layout ID:** *Container*</span></span>
    - <span data-ttu-id="143ca-362">**打印机名称：** 选择适当的 ZPL 打印机。</span><span class="sxs-lookup"><span data-stu-id="143ca-362">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="143ca-363">**运行查询**：*是*（此设置是可选的，但建议使用此设置以获得最佳性能。）</span><span class="sxs-lookup"><span data-stu-id="143ca-363">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="143ca-364">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="143ca-364">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="143ca-365">可选：如果要设置客户特定的标签设计，则必须创建查询来查找客户的帐户。</span><span class="sxs-lookup"><span data-stu-id="143ca-365">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="143ca-366">在**波次标签模板详细信息**快速选项卡上，选择**编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="143ca-366">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="143ca-367">然后，在查询编辑器对话框的**范围**选项卡上，添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="143ca-367">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="143ca-368">**表**：*装运*</span><span class="sxs-lookup"><span data-stu-id="143ca-368">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="143ca-369">**派生表**：*装运*</span><span class="sxs-lookup"><span data-stu-id="143ca-369">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="143ca-370">**字段**：*帐号*</span><span class="sxs-lookup"><span data-stu-id="143ca-370">**Field:** *Account number*</span></span>
    - <span data-ttu-id="143ca-371">**条件：** 输入相关的客户帐号。</span><span class="sxs-lookup"><span data-stu-id="143ca-371">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="143ca-372">完成后，选择**确定**关闭查询编辑器对话框。</span><span class="sxs-lookup"><span data-stu-id="143ca-372">When you've finished, select **OK** to close the query editor dialog box.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="143ca-373">配置编号规则扩展</span><span class="sxs-lookup"><span data-stu-id="143ca-373">Configure number sequence extensions</span></span>

<span data-ttu-id="143ca-374">编号规则扩展控制特定编号规则的 GS1 符合性。</span><span class="sxs-lookup"><span data-stu-id="143ca-374">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="143ca-375">此配置对于当前方案是可选的。</span><span class="sxs-lookup"><span data-stu-id="143ca-375">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="143ca-376">有关详细信息和配置说明，请参阅[配置编号规则扩展](../warehousing/configure-number-sequence-extensions.md)。</span><span class="sxs-lookup"><span data-stu-id="143ca-376">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="143ca-377">创建销售订单并将其下达到仓库</span><span class="sxs-lookup"><span data-stu-id="143ca-377">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="143ca-378">转到**销售和营销 \> 销售订单 \> 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="143ca-378">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="143ca-379">创建具有以下设置的销售订单：</span><span class="sxs-lookup"><span data-stu-id="143ca-379">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="143ca-380">**客户帐户**：*US-001*</span><span class="sxs-lookup"><span data-stu-id="143ca-380">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="143ca-381">**仓库**：*63*</span><span class="sxs-lookup"><span data-stu-id="143ca-381">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="143ca-382">添加五个销售订单行：</span><span class="sxs-lookup"><span data-stu-id="143ca-382">Add five sales order lines:</span></span>

    - <span data-ttu-id="143ca-383">销售订单行 1：</span><span class="sxs-lookup"><span data-stu-id="143ca-383">Sales order line 1:</span></span>

        - <span data-ttu-id="143ca-384">\**物料编号：\*\*\*A0001*</span><span class="sxs-lookup"><span data-stu-id="143ca-384">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="143ca-385">**数量：** *10*</span><span class="sxs-lookup"><span data-stu-id="143ca-385">**Quantity:** *10*</span></span>

    - <span data-ttu-id="143ca-386">销售订单行 2：</span><span class="sxs-lookup"><span data-stu-id="143ca-386">Sales order line 2:</span></span>

        - <span data-ttu-id="143ca-387">\**物料编号：\*\*\*A0002*</span><span class="sxs-lookup"><span data-stu-id="143ca-387">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="143ca-388">**数量：** *20*</span><span class="sxs-lookup"><span data-stu-id="143ca-388">**Quantity:** *20*</span></span>

    - <span data-ttu-id="143ca-389">销售订单行 3：</span><span class="sxs-lookup"><span data-stu-id="143ca-389">Sales order line 3:</span></span>

        - <span data-ttu-id="143ca-390">\**物料编号：\*\*\*L0006*</span><span class="sxs-lookup"><span data-stu-id="143ca-390">**Item number:** *L0006*</span></span>
        - <span data-ttu-id="143ca-391">**数量：** *20*</span><span class="sxs-lookup"><span data-stu-id="143ca-391">**Quantity:** *20*</span></span>

    - <span data-ttu-id="143ca-392">销售订单行 4：</span><span class="sxs-lookup"><span data-stu-id="143ca-392">Sales order line 4:</span></span>

        - <span data-ttu-id="143ca-393">\**物料编号：\*\*\*L0100*</span><span class="sxs-lookup"><span data-stu-id="143ca-393">**Item number:** *L0100*</span></span>
        - <span data-ttu-id="143ca-394">**数量：** *40*</span><span class="sxs-lookup"><span data-stu-id="143ca-394">**Quantity:** *40*</span></span>

    - <span data-ttu-id="143ca-395">销售订单行 5：</span><span class="sxs-lookup"><span data-stu-id="143ca-395">Sales order line 5:</span></span>

        - <span data-ttu-id="143ca-396">\**物料编号：\*\*\*L0101*</span><span class="sxs-lookup"><span data-stu-id="143ca-396">**Item number:** *L0101*</span></span>
        - <span data-ttu-id="143ca-397">**数量：** *50*</span><span class="sxs-lookup"><span data-stu-id="143ca-397">**Quantity:** *50*</span></span>

    > [!NOTE]
    > <span data-ttu-id="143ca-398">此处提供的物料和数量仅是示例。</span><span class="sxs-lookup"><span data-stu-id="143ca-398">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="143ca-399">它们必须在指定的仓库中有存货。</span><span class="sxs-lookup"><span data-stu-id="143ca-399">They must have stock in the specified warehouse.</span></span>

1. <span data-ttu-id="143ca-400">选择销售订单行 1。</span><span class="sxs-lookup"><span data-stu-id="143ca-400">Select sales order line 1.</span></span> <span data-ttu-id="143ca-401">然后，在**销售订单行**部分的**库存**菜单中，选择**预留**。</span><span class="sxs-lookup"><span data-stu-id="143ca-401">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="143ca-402">在**预留**页的操作窗格中，选择**预留批次**，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="143ca-402">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="143ca-403">对每个其他销售订单行重复步骤 4 和 5。</span><span class="sxs-lookup"><span data-stu-id="143ca-403">Repeat steps 4 and 5 for each additional sales order line.</span></span>
1. <span data-ttu-id="143ca-404">在“操作窗格”上的**仓库**选项卡上，选择**发放到仓库**。</span><span class="sxs-lookup"><span data-stu-id="143ca-404">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="143ca-405">将发生以下事件：</span><span class="sxs-lookup"><span data-stu-id="143ca-405">The following events occur:</span></span>

    - <span data-ttu-id="143ca-406">系统使用包含标签打印步骤的模板来处理创建的装运。</span><span class="sxs-lookup"><span data-stu-id="143ca-406">The system processes the created shipment using the template that includes the label printing step.</span></span> <span data-ttu-id="143ca-407">标签布局将用于定义标签的格式，最终结果将是具有五个行的标签，此标签将在标签模板中选择的打印机上打印。</span><span class="sxs-lookup"><span data-stu-id="143ca-407">The label layout will be used to define the format of the label, and the end result will be a label that has five lines and that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="143ca-408">将为装运生成新提单 ID。</span><span class="sxs-lookup"><span data-stu-id="143ca-408">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="143ca-409">如果您配置了数字序列扩展，波次标签 ID 将采用 **SSCC-18** 数字格式。</span><span class="sxs-lookup"><span data-stu-id="143ca-409">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="143ca-410">您可以转到**仓库管理 \> 查询和报表 \> 波次标签历史记录**，重新打印这些波次标签。</span><span class="sxs-lookup"><span data-stu-id="143ca-410">You can reprint these wave labels by going to **Warehouse management \> Inquiries and reports \> Wave label history**.</span></span>

## <a name="scenario-3-wave-label-printing-for-multi-tiered-labels"></a><span data-ttu-id="143ca-411">方案 3：为多层标签打印波次标签</span><span class="sxs-lookup"><span data-stu-id="143ca-411">Scenario 3: Wave label printing for multi-tiered labels</span></span>

<span data-ttu-id="143ca-412">此方案展示当仓储流程需要几层运输标签时如何使用波次标签打印功能。</span><span class="sxs-lookup"><span data-stu-id="143ca-412">This scenario shows how to use the wave label printing functionality when the warehousing processes require several tiers of shipping labels.</span></span> <span data-ttu-id="143ca-413">例如，对于货箱和托盘，可能必须打印单独的标签，而对于整个装运，可能必须打印中断标签。</span><span class="sxs-lookup"><span data-stu-id="143ca-413">For example, separate labels might have to be printed for cartons and pallets, and a break label might have to be printed for a whole shipment.</span></span> <span data-ttu-id="143ca-414">中断标签是一种独立标签，可用作标签卷和集装箱之间的分界，如装运 ID 标签和条形码标签，以便在打印标签后可以轻松进行分类。</span><span class="sxs-lookup"><span data-stu-id="143ca-414">Break labels are a separate type of label that can be used as a divider between rolls and containers, such as labels for the shipment ID and a barcode, so that the labels can easily be sorted after they are printed.</span></span>

<span data-ttu-id="143ca-415">此方案的配置与方案 1 的配置之间的主要区别在于，除了启用了中断标签之外，还必须将多个波次标签类型与波次标签模板和单位序列组行关联。</span><span class="sxs-lookup"><span data-stu-id="143ca-415">The main difference between the configuration of this scenario and the configuration of scenario 1, besides the fact that break labels are enabled, is that multiple wave label types must be associated with wave label templates and unit sequence group lines.</span></span> <span data-ttu-id="143ca-416">要完成此配置，请为此方案设置以下元素：</span><span class="sxs-lookup"><span data-stu-id="143ca-416">To accomplish this configuration, you set up the following elements for this scenario:</span></span>

- <span data-ttu-id="143ca-417">**波次处理方法：** 您将波次标签方法标记为“可重复”，将其两次（或多次）添加到波次模板中，并设置不同的波次步骤代码。</span><span class="sxs-lookup"><span data-stu-id="143ca-417">**Wave processing methods:** You will mark the wave label method as "repeatable," add it two (or more) times to the wave template, and set different wave step codes.</span></span>
- <span data-ttu-id="143ca-418">**波次标签模板：** 您将配置波次标签模板并将其链接到波次模板。</span><span class="sxs-lookup"><span data-stu-id="143ca-418">**Wave label templates:** You will configure the wave label templates and link them to the wave template.</span></span> <span data-ttu-id="143ca-419">每个波次标签模板都有其自己的波次标签类型。</span><span class="sxs-lookup"><span data-stu-id="143ca-419">Each wave label template has its own wave label type.</span></span>
- <span data-ttu-id="143ca-420">**波次标签布局：** 您将创建多个波次标签布局。</span><span class="sxs-lookup"><span data-stu-id="143ca-420">**Wave label layouts:** You will create multiple wave label layouts.</span></span> <span data-ttu-id="143ca-421">标签的每个“层”将有一个单独的标签布局，并且还将有一个中断标签布局。</span><span class="sxs-lookup"><span data-stu-id="143ca-421">There will be a separate label layout for each "tier" of labels, and there will also be a break label layout.</span></span>

<span data-ttu-id="143ca-422">此方案演示端到端流。</span><span class="sxs-lookup"><span data-stu-id="143ca-422">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="143ca-423">提供演示数据</span><span class="sxs-lookup"><span data-stu-id="143ca-423">Make demo data available</span></span>

<span data-ttu-id="143ca-424">要采取此方案，必须安装演示数据，并且必须选择 **USMF** 法人。</span><span class="sxs-lookup"><span data-stu-id="143ca-424">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-wave-process-method"></a><span data-ttu-id="143ca-425">设置波次处理方法</span><span class="sxs-lookup"><span data-stu-id="143ca-425">Set up a wave process method</span></span>

1. <span data-ttu-id="143ca-426">转到**仓库管理 \> 设置 \> 波次 \> 波次处理方法**。</span><span class="sxs-lookup"><span data-stu-id="143ca-426">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="143ca-427">确认 **waveLabelPrinting** 在列表中。</span><span class="sxs-lookup"><span data-stu-id="143ca-427">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="143ca-428">如果不在，请在操作窗格中选择**重新生成方法**添加该方法。</span><span class="sxs-lookup"><span data-stu-id="143ca-428">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>
1. <span data-ttu-id="143ca-429">对于 **waveLabelPrinting** 方法，选中**让方法可重复**复选框。</span><span class="sxs-lookup"><span data-stu-id="143ca-429">For the **waveLabelPrinting** method, select the **Make method repeatable** check box.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="143ca-430">设置波次模板</span><span class="sxs-lookup"><span data-stu-id="143ca-430">Set up a wave template</span></span>

1. <span data-ttu-id="143ca-431">转到**仓库管理 \> 设置 \> 波次 \> 波次模板**。</span><span class="sxs-lookup"><span data-stu-id="143ca-431">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
2. <span data-ttu-id="143ca-432">选择模板，如 **62 装运默认**。</span><span class="sxs-lookup"><span data-stu-id="143ca-432">Select a template, such as **62 Shipping Default**.</span></span>
3. <span data-ttu-id="143ca-433">在**方法**快速选项卡上，将**波次标签打印**方法移至**选定方法**列。</span><span class="sxs-lookup"><span data-stu-id="143ca-433">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
4. <span data-ttu-id="143ca-434">在**选定方法**列中，将**波次步骤代码**值（如 *Carton*）分配给**波次标签打印**方法。</span><span class="sxs-lookup"><span data-stu-id="143ca-434">In the **Selected methods** column, assign a **Wave step code** value, such as *Carton*, to the **Wave label printing** method.</span></span> <span data-ttu-id="143ca-435">有关波次步骤代码的详细信息，请参阅[波次步骤代码](wave-step-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="143ca-435">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>
5. <span data-ttu-id="143ca-436">再次将**波次标签打印**方法移至**选定方法**列。</span><span class="sxs-lookup"><span data-stu-id="143ca-436">Move the **Wave label printing** method to the **Selected methods** column a second time.</span></span>
6. <span data-ttu-id="143ca-437">在**选定方法**列中，将不同**波次步骤代码**值（如 *Pallet*）分配给第二个**波次标签打印**方法。</span><span class="sxs-lookup"><span data-stu-id="143ca-437">In the **Selected methods** column, assign a different **Wave step code** value, such as *Pallet*, to the second **Wave label printing** method.</span></span> <span data-ttu-id="143ca-438">有关波次步骤代码的详细信息，请参阅[波次步骤代码](wave-step-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="143ca-438">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-three-wave-label-layouts"></a><span data-ttu-id="143ca-439">创建三个波次标签布局</span><span class="sxs-lookup"><span data-stu-id="143ca-439">Create three wave label layouts</span></span>

1. <span data-ttu-id="143ca-440">转到**仓库管理 \> 设置 \> 文档路线布局 \> 波次标签布局**。</span><span class="sxs-lookup"><span data-stu-id="143ca-440">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="143ca-441">创建一个具有以下设置的记录：</span><span class="sxs-lookup"><span data-stu-id="143ca-441">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="143ca-442">**标签布局 ID**：*Carton*</span><span class="sxs-lookup"><span data-stu-id="143ca-442">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="143ca-443">**描述**：*货箱 (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="143ca-443">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="143ca-444">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="143ca-444">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="143ca-445">在操作窗格上，选择**波次标签行设置**。</span><span class="sxs-lookup"><span data-stu-id="143ca-445">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="143ca-446">**波次标签行设置**页面将出现。</span><span class="sxs-lookup"><span data-stu-id="143ca-446">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="143ca-447">在这里，您可以配置标签的动态部分。</span><span class="sxs-lookup"><span data-stu-id="143ca-447">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="143ca-448">添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="143ca-448">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="143ca-449">**行 ID**：*WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="143ca-449">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="143ca-450">**行表名称**：*WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="143ca-450">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="143ca-451">**行开始位置**：*0*</span><span class="sxs-lookup"><span data-stu-id="143ca-451">**Row start position:** *0*</span></span>

        <span data-ttu-id="143ca-452">此字段定义行在标签上开始的垂直位置。</span><span class="sxs-lookup"><span data-stu-id="143ca-452">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="143ca-453">**行高度**：*0*</span><span class="sxs-lookup"><span data-stu-id="143ca-453">**Row height:** *0*</span></span>

        <span data-ttu-id="143ca-454">此字段根据 ZPL 标准定义每行的高度（以磅为单位）。</span><span class="sxs-lookup"><span data-stu-id="143ca-454">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="143ca-455">行高度对于水平标签为正，对于垂直标签为负。</span><span class="sxs-lookup"><span data-stu-id="143ca-455">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="143ca-456">在此示例中因为只有一行，所以您可以将此值设置为 *0*（零）。</span><span class="sxs-lookup"><span data-stu-id="143ca-456">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="143ca-457">**每页行数**：*1*</span><span class="sxs-lookup"><span data-stu-id="143ca-457">**Rows per page:** *1*</span></span>

        <span data-ttu-id="143ca-458">此字段定义可以在每个标签上打印的行数。</span><span class="sxs-lookup"><span data-stu-id="143ca-458">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="143ca-459">使用此设置，将为波次标签表中的每个记录打印一个单独的 ZPL 标签。</span><span class="sxs-lookup"><span data-stu-id="143ca-459">This setup will cause a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="143ca-460">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="143ca-460">Close the page.</span></span>
1. <span data-ttu-id="143ca-461">在操作窗格上，选择**编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="143ca-461">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="143ca-462">在查询编辑器对话框的**范围**选项卡上，添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="143ca-462">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="143ca-463">**表**：*工作行*</span><span class="sxs-lookup"><span data-stu-id="143ca-463">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="143ca-464">**派生表**：*工作行*</span><span class="sxs-lookup"><span data-stu-id="143ca-464">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="143ca-465">**字段**：*工作类型*</span><span class="sxs-lookup"><span data-stu-id="143ca-465">**Field:** *Work type*</span></span>
    - <span data-ttu-id="143ca-466">**条件**：*领料*</span><span class="sxs-lookup"><span data-stu-id="143ca-466">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="143ca-467">此查询可确保在标签上仅打印领料类型的工作行，不打印放置类型的工作行。</span><span class="sxs-lookup"><span data-stu-id="143ca-467">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="143ca-468">如果您希望能够打印提单 ID，请在**联接**选项卡上，选择**工作行**表，然后将**装运**表与其联接。</span><span class="sxs-lookup"><span data-stu-id="143ca-468">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span> 
1. <span data-ttu-id="143ca-469">关闭查询编辑器对话框。</span><span class="sxs-lookup"><span data-stu-id="143ca-469">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="143ca-470">**打印机文本布局**快速选项卡有三个部分，您可以在其中编写打印机代码：**页眉部分**、**主体部分**和**页脚部分**。</span><span class="sxs-lookup"><span data-stu-id="143ca-470">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="143ca-471">在**页眉部分**的**标签页眉**字段中，输入所需页眉的代码。</span><span class="sxs-lookup"><span data-stu-id="143ca-471">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="143ca-472">例如，如果您使用的是 Zebra 打印机，可以使用以下代码。</span><span class="sxs-lookup"><span data-stu-id="143ca-472">For example, if you're using Zebra printers, you can use the following code.</span></span>


    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. <span data-ttu-id="143ca-473">在**主体部分**的**标签主体**字段中，输入所需主体的 ZPL 代码。</span><span class="sxs-lookup"><span data-stu-id="143ca-473">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="143ca-474">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="143ca-474">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. <span data-ttu-id="143ca-475">在**主体部分**的**标签页脚**字段中，输入所需页脚的 ZPL 代码。</span><span class="sxs-lookup"><span data-stu-id="143ca-475">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="143ca-476">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="143ca-476">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="143ca-477">此设置将打印每个标签的一个副本。</span><span class="sxs-lookup"><span data-stu-id="143ca-477">This setup will print one copy of each label.</span></span> <span data-ttu-id="143ca-478">如果需要更多副本（例如，托盘每一面一个副本），请将页脚中 **\^PQn** 部分的 **n** 值设置为所需的副本数。</span><span class="sxs-lookup"><span data-stu-id="143ca-478">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="143ca-479">例如，每个标签要打印四个副本，请指定 **\^PQ4**。</span><span class="sxs-lookup"><span data-stu-id="143ca-479">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

1. <span data-ttu-id="143ca-480">第一个标签现在可以使用了。</span><span class="sxs-lookup"><span data-stu-id="143ca-480">The first label is now ready to use.</span></span>
1. <span data-ttu-id="143ca-481">创建具有以下设置的第二个布局记录：</span><span class="sxs-lookup"><span data-stu-id="143ca-481">Create a second layout record that has the following settings:</span></span>

    - <span data-ttu-id="143ca-482">**标签布局 ID**：*Pallet*</span><span class="sxs-lookup"><span data-stu-id="143ca-482">**Label layout ID:** *Pallet*</span></span>
    - <span data-ttu-id="143ca-483">**描述**：*托盘*</span><span class="sxs-lookup"><span data-stu-id="143ca-483">**Description:** *Pallet*</span></span>

1. <span data-ttu-id="143ca-484">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="143ca-484">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="143ca-485">在操作窗格上，选择**波次标签行设置**。</span><span class="sxs-lookup"><span data-stu-id="143ca-485">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="143ca-486">**波次标签行设置**页面将出现。</span><span class="sxs-lookup"><span data-stu-id="143ca-486">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="143ca-487">在这里，您可以配置标签的动态部分。</span><span class="sxs-lookup"><span data-stu-id="143ca-487">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="143ca-488">添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="143ca-488">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="143ca-489">**行 ID**：*WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="143ca-489">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="143ca-490">**行表名称**：*WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="143ca-490">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="143ca-491">**行开始位置**：*0*</span><span class="sxs-lookup"><span data-stu-id="143ca-491">**Row start position:** *0*</span></span>

        <span data-ttu-id="143ca-492">此字段定义行在标签上开始的垂直位置。</span><span class="sxs-lookup"><span data-stu-id="143ca-492">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="143ca-493">**行高度**：*0*</span><span class="sxs-lookup"><span data-stu-id="143ca-493">**Row height:** *0*</span></span>

        <span data-ttu-id="143ca-494">此字段根据 ZPL 标准定义每行的高度（以磅为单位）。</span><span class="sxs-lookup"><span data-stu-id="143ca-494">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="143ca-495">行高度对于水平标签为正，对于垂直标签为负。</span><span class="sxs-lookup"><span data-stu-id="143ca-495">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="143ca-496">在此示例中因为只有一行，所以您可以将此值设置为 *0*（零）。</span><span class="sxs-lookup"><span data-stu-id="143ca-496">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="143ca-497">**每页行数**：*1*</span><span class="sxs-lookup"><span data-stu-id="143ca-497">**Rows per page:** *1*</span></span>

        <span data-ttu-id="143ca-498">此字段定义可以在每个标签上打印的行数。</span><span class="sxs-lookup"><span data-stu-id="143ca-498">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="143ca-499">使用此设置，将为波次标签表中的每个记录打印一个单独的 ZPL 标签。</span><span class="sxs-lookup"><span data-stu-id="143ca-499">This setup causes a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="143ca-500">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="143ca-500">Close the page.</span></span>
1. <span data-ttu-id="143ca-501">在操作窗格上，选择**编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="143ca-501">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="143ca-502">在查询编辑器对话框的**范围**选项卡上，添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="143ca-502">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="143ca-503">**表**：*工作行*</span><span class="sxs-lookup"><span data-stu-id="143ca-503">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="143ca-504">**派生表**：*工作行*</span><span class="sxs-lookup"><span data-stu-id="143ca-504">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="143ca-505">**字段**：*工作类型*</span><span class="sxs-lookup"><span data-stu-id="143ca-505">**Field:** *Work type*</span></span>
    - <span data-ttu-id="143ca-506">**条件**：*领料*</span><span class="sxs-lookup"><span data-stu-id="143ca-506">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="143ca-507">此查询可确保在标签上仅打印领料类型的工作行，不打印放置类型的工作行。</span><span class="sxs-lookup"><span data-stu-id="143ca-507">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="143ca-508">如果您希望能够打印提单 ID，请在**联接**选项卡上，选择**工作行**表，然后将**装运**表与其联接。</span><span class="sxs-lookup"><span data-stu-id="143ca-508">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="143ca-509">关闭查询编辑器对话框。</span><span class="sxs-lookup"><span data-stu-id="143ca-509">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="143ca-510">**打印机文本布局**快速选项卡有三个部分，您可以在其中编写打印机代码：**页眉部分**、**主体部分**和**页脚部分**。</span><span class="sxs-lookup"><span data-stu-id="143ca-510">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="143ca-511">在**页眉部分**的**标签页眉**字段中，输入所需页眉的代码。</span><span class="sxs-lookup"><span data-stu-id="143ca-511">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="143ca-512">例如，如果您使用的是 Zebra 打印机，可以使用以下代码。</span><span class="sxs-lookup"><span data-stu-id="143ca-512">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWaveLabel.WaveLabelId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. <span data-ttu-id="143ca-513">在**主体部分**的**标签主体**字段中，输入所需主体的 ZPL 代码。</span><span class="sxs-lookup"><span data-stu-id="143ca-513">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="143ca-514">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="143ca-514">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWaveLabel.LabelItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWaveLabel.QtyWork$ ^FS
    </Row>
    ```

1. <span data-ttu-id="143ca-515">在**主体部分**的**标签页脚**字段中，输入所需页脚的 ZPL 代码。</span><span class="sxs-lookup"><span data-stu-id="143ca-515">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="143ca-516">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="143ca-516">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="143ca-517">此设置将打印每个标签的一个副本。</span><span class="sxs-lookup"><span data-stu-id="143ca-517">This setup will print one copy of each label.</span></span> <span data-ttu-id="143ca-518">如果需要更多副本（例如，托盘每一面一个副本），请将页脚中 **\^PQn** 部分的 **n** 值设置为所需的副本数。</span><span class="sxs-lookup"><span data-stu-id="143ca-518">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="143ca-519">例如，每个标签要打印四个副本，请指定 **\^PQ4**。</span><span class="sxs-lookup"><span data-stu-id="143ca-519">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

1. <span data-ttu-id="143ca-520">第二个标签现在可以使用了。</span><span class="sxs-lookup"><span data-stu-id="143ca-520">The second label is now ready to use.</span></span>
1. <span data-ttu-id="143ca-521">创建具有以下设置的第三个布局记录：</span><span class="sxs-lookup"><span data-stu-id="143ca-521">Create a third layout record that has the following settings:</span></span>

    - <span data-ttu-id="143ca-522">**标签布局 ID**：*Break*</span><span class="sxs-lookup"><span data-stu-id="143ca-522">**Label layout ID:** *Break*</span></span>
    - <span data-ttu-id="143ca-523">**描述**：*中断标签*</span><span class="sxs-lookup"><span data-stu-id="143ca-523">**Description:** *Break label*</span></span>

1. <span data-ttu-id="143ca-524">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="143ca-524">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="143ca-525">**打印机文本布局**快速选项卡有三个部分，您可以在其中编写打印机代码：**页眉部分**、**主体部分**和**页脚部分**。</span><span class="sxs-lookup"><span data-stu-id="143ca-525">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="143ca-526">在**页眉部分**的**标签页眉**字段中，输入所需页眉的 ZPL 代码。</span><span class="sxs-lookup"><span data-stu-id="143ca-526">In the **Header section** section, in the **Label header** field, enter ZPL code for the required header.</span></span> <span data-ttu-id="143ca-527">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="143ca-527">Here is an example.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ```

1. <span data-ttu-id="143ca-528">这次，不需要人工。</span><span class="sxs-lookup"><span data-stu-id="143ca-528">This time, no body is required.</span></span> <span data-ttu-id="143ca-529">因此，只需在**页脚部分**部分输入所需文本。</span><span class="sxs-lookup"><span data-stu-id="143ca-529">Therefore, just enter the required text in the **Footer section** section.</span></span> <span data-ttu-id="143ca-530">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="143ca-530">Here is an example.</span></span>

    ```plaintext
    ^XZ
    ```

    <span data-ttu-id="143ca-531">第三个标签现在可以使用了。</span><span class="sxs-lookup"><span data-stu-id="143ca-531">The third label is now ready to use.</span></span>

    > [!NOTE]
    > <span data-ttu-id="143ca-532">第三个标签是中断标签，将用作标签卷之间的分界。</span><span class="sxs-lookup"><span data-stu-id="143ca-532">This third label is a break label that will be used as a divider between label rolls.</span></span>

### <a name="create-two-wave-label-types"></a><span data-ttu-id="143ca-533">创建两个波次标签类型</span><span class="sxs-lookup"><span data-stu-id="143ca-533">Create two wave label types</span></span>

1. <span data-ttu-id="143ca-534">转到**仓库管理 \> 设置 \> 文档路线布局 \> 波次标签类型**。</span><span class="sxs-lookup"><span data-stu-id="143ca-534">Go to **Warehouse management \> Setup \> Document routing \> Wave label types**.</span></span>
1. <span data-ttu-id="143ca-535">创建一个具有以下设置的记录：</span><span class="sxs-lookup"><span data-stu-id="143ca-535">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="143ca-536">**标签类型**：*货箱*</span><span class="sxs-lookup"><span data-stu-id="143ca-536">**Label type:** *Carton*</span></span>
    - <span data-ttu-id="143ca-537">**描述**：*货箱*</span><span class="sxs-lookup"><span data-stu-id="143ca-537">**Description:** *Carton*</span></span>

1. <span data-ttu-id="143ca-538">创建具有以下设置的第二个记录：</span><span class="sxs-lookup"><span data-stu-id="143ca-538">Create a second record that has the following settings:</span></span>

    - <span data-ttu-id="143ca-539">**标签类型**：*托盘*</span><span class="sxs-lookup"><span data-stu-id="143ca-539">**Label type:** *Pallet*</span></span>
    - <span data-ttu-id="143ca-540">**描述**：*托盘*</span><span class="sxs-lookup"><span data-stu-id="143ca-540">**Description:** *Pallet*</span></span>

### <a name="set-up-unit-sequence-groups"></a><span data-ttu-id="143ca-541">设置单位序列组</span><span class="sxs-lookup"><span data-stu-id="143ca-541">Set up unit sequence groups</span></span>

1. <span data-ttu-id="143ca-542">转到**仓库管理 \> 设置 \> 仓库 \> 单位序列组**。</span><span class="sxs-lookup"><span data-stu-id="143ca-542">Go to **Warehouse management \> Setup \> Warehouse \> Unit sequence groups**.</span></span>
1. <span data-ttu-id="143ca-543">选择或创建一个 **Ea Box PL** 组。</span><span class="sxs-lookup"><span data-stu-id="143ca-543">Select or create an **Ea Box PL** group.</span></span>
1. <span data-ttu-id="143ca-544">对于**箱**行，将**波次级别类型**字段设置为*货箱*。</span><span class="sxs-lookup"><span data-stu-id="143ca-544">For the **Box** line, set the **Wave level type** field to *Carton*.</span></span>
1. <span data-ttu-id="143ca-545">对于**托盘**行，将**波次级别类型**字段设置为*托盘*。</span><span class="sxs-lookup"><span data-stu-id="143ca-545">For the **PL** line, set the **Wave level type** field to *Pallet*.</span></span>

### <a name="create-wave-label-templates"></a><span data-ttu-id="143ca-546">创建波次标签模板</span><span class="sxs-lookup"><span data-stu-id="143ca-546">Create wave label templates</span></span>

1. <span data-ttu-id="143ca-547">转到**仓库管理 \> 设置 \> 文档路线布局 \> 波次标签模板**。</span><span class="sxs-lookup"><span data-stu-id="143ca-547">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="143ca-548">创建具有以下设置的标签模板：</span><span class="sxs-lookup"><span data-stu-id="143ca-548">Create a label template that has the following settings:</span></span>

    - <span data-ttu-id="143ca-549">**标签模板名称**：*货箱标签*</span><span class="sxs-lookup"><span data-stu-id="143ca-549">**Label template name:** *Carton labels*</span></span>
    - <span data-ttu-id="143ca-550">**描述**：*货箱标签*</span><span class="sxs-lookup"><span data-stu-id="143ca-550">**Description:** *Carton labels*</span></span>
    - <span data-ttu-id="143ca-551">**波次步骤代码**：*Carton*</span><span class="sxs-lookup"><span data-stu-id="143ca-551">**Wave step code:** *Carton*</span></span>
    - <span data-ttu-id="143ca-552">**仓库**：*62*</span><span class="sxs-lookup"><span data-stu-id="143ca-552">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="143ca-553">在**常规**快速选项卡上，在**波次标签类型**字段中，选择一个值，如*货箱*。</span><span class="sxs-lookup"><span data-stu-id="143ca-553">On the **General** FastTab, in the **Wave label type** field, select a value, such as *Carton*.</span></span>
1. <span data-ttu-id="143ca-554">在**波次标签模板详细信息**快速选项卡上，添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="143ca-554">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="143ca-555">**标签布局 ID**：*Carton*</span><span class="sxs-lookup"><span data-stu-id="143ca-555">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="143ca-556">**打印机名称：** 选择适当的 ZPL 打印机。</span><span class="sxs-lookup"><span data-stu-id="143ca-556">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="143ca-557">**运行查询**：*是*（此设置是可选的，但建议使用此设置以获得最佳性能。）</span><span class="sxs-lookup"><span data-stu-id="143ca-557">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="143ca-558">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="143ca-558">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="143ca-559">可选：如果要设置客户特定的标签设计，则必须创建查询来查找客户的帐户。</span><span class="sxs-lookup"><span data-stu-id="143ca-559">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="143ca-560">在**波次标签模板详细信息**快速选项卡上，选择**编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="143ca-560">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="143ca-561">然后，在查询编辑器对话框的**范围**选项卡上，添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="143ca-561">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="143ca-562">**表**：*装运*</span><span class="sxs-lookup"><span data-stu-id="143ca-562">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="143ca-563">**派生表**：*装运*</span><span class="sxs-lookup"><span data-stu-id="143ca-563">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="143ca-564">**字段**：*帐号*</span><span class="sxs-lookup"><span data-stu-id="143ca-564">**Field:** *Account number*</span></span>
    - <span data-ttu-id="143ca-565">**条件：** 输入相关的客户帐号。</span><span class="sxs-lookup"><span data-stu-id="143ca-565">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="143ca-566">完成后，选择**确定**关闭查询编辑器对话框。</span><span class="sxs-lookup"><span data-stu-id="143ca-566">When you've finished, select **OK** to close the query editor dialog box.</span></span>

1. <span data-ttu-id="143ca-567">在操作窗格上，选择**编辑查询**打开整个标签模板的查询编辑器对话框。</span><span class="sxs-lookup"><span data-stu-id="143ca-567">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="143ca-568">在查询编辑器对话框的**排序**选项卡上，添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="143ca-568">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="143ca-569">**表**：*工作行*</span><span class="sxs-lookup"><span data-stu-id="143ca-569">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="143ca-570">**派生表**：*工作行*</span><span class="sxs-lookup"><span data-stu-id="143ca-570">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="143ca-571">**字段**：*参考负荷行 ID（记录 ID）*</span><span class="sxs-lookup"><span data-stu-id="143ca-571">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="143ca-572">**搜索方向**：*升序*</span><span class="sxs-lookup"><span data-stu-id="143ca-572">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="143ca-573">再添加一个具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="143ca-573">Add a second row that has the following settings:</span></span>

    - <span data-ttu-id="143ca-574">**表**：*工作行*</span><span class="sxs-lookup"><span data-stu-id="143ca-574">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="143ca-575">**派生表**：*工作行*</span><span class="sxs-lookup"><span data-stu-id="143ca-575">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="143ca-576">**字段**：*装运 ID*</span><span class="sxs-lookup"><span data-stu-id="143ca-576">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="143ca-577">**搜索方向**：*升序*</span><span class="sxs-lookup"><span data-stu-id="143ca-577">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="143ca-578">选择**确定**关闭查询编辑器对话框。</span><span class="sxs-lookup"><span data-stu-id="143ca-578">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="143ca-579">一个消息框将提示您确认分组重置操作。</span><span class="sxs-lookup"><span data-stu-id="143ca-579">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="143ca-580">选择**是**继续。</span><span class="sxs-lookup"><span data-stu-id="143ca-580">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="143ca-581">在操作窗格上，选择**波次标签模板组**。</span><span class="sxs-lookup"><span data-stu-id="143ca-581">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="143ca-582">在**波次标签模板组**对话框中，对于**参考字段名称**字段设置为*装运 ID* 的行，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="143ca-582">In the **Wave label template group** dialog box, for the row where the **Reference field name** field is set to *Shipment ID*, set the following values:</span></span>

    - <span data-ttu-id="143ca-583">**打印中断标签：** 选择此复选框。</span><span class="sxs-lookup"><span data-stu-id="143ca-583">**Print break label:** Select this check box.</span></span>
    - <span data-ttu-id="143ca-584">**标签布局 ID：** 选择一个中断标签。</span><span class="sxs-lookup"><span data-stu-id="143ca-584">**Label layout ID:** Select a break label.</span></span> <span data-ttu-id="143ca-585">（例如，选择您在此方案中先前创建的*中断*标签布局。）</span><span class="sxs-lookup"><span data-stu-id="143ca-585">(For example, select the *Break* label layout that you created earlier in this scenario.)</span></span>
    - <span data-ttu-id="143ca-586">**打印机名称：** 选择中断标签的打印机。</span><span class="sxs-lookup"><span data-stu-id="143ca-586">**Printer name:** Select the printer for the break label.</span></span> <span data-ttu-id="143ca-587">（通常，出于分割标签券的目的，您应该选择在**波次标签模板详细信息**上选择的同一台打印机。</span><span class="sxs-lookup"><span data-stu-id="143ca-587">(Typically, for the purpose of splitting label rolls, you should select the same printer that is selected on the **Wave label template details** FastTab.</span></span> <span data-ttu-id="143ca-588">但也可能是其他情况。）</span><span class="sxs-lookup"><span data-stu-id="143ca-588">However, other scenarios are possible.)</span></span>

1. <span data-ttu-id="143ca-589">对于将**参考字段名称**字段设置为*参考负荷行 ID* 的行，选择**标签生成 ID** 复选框。</span><span class="sxs-lookup"><span data-stu-id="143ca-589">For the row where the **Reference field name** field is set to *Reference load line id*, select the **Label build ID** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="143ca-590">无论工作分组设置如何，此设置都会在整个波次中为每个负荷行创建一个标签序列（“货箱 1/X”）。</span><span class="sxs-lookup"><span data-stu-id="143ca-590">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="143ca-591">此标签序列可以打印在标签布局上。</span><span class="sxs-lookup"><span data-stu-id="143ca-591">This label sequence can be printed on a label layout.</span></span> <span data-ttu-id="143ca-592">此外，不同装运的标签将由选定的中断标签分隔。</span><span class="sxs-lookup"><span data-stu-id="143ca-592">Additionally, labels for different shipments will be separated by the selected break label.</span></span>

1. <span data-ttu-id="143ca-593">选择**确定**关闭**波次标签模板组**对话框。</span><span class="sxs-lookup"><span data-stu-id="143ca-593">Select **OK** to close the **Wave label template group** dialog box.</span></span>
1. <span data-ttu-id="143ca-594">再创建一个具有以下设置的标签模板：</span><span class="sxs-lookup"><span data-stu-id="143ca-594">Create a second label template that has the following settings:</span></span>

    - <span data-ttu-id="143ca-595">**标签模板名称**：*托盘标签*</span><span class="sxs-lookup"><span data-stu-id="143ca-595">**Label template name:** *Pallet labels*</span></span>
    - <span data-ttu-id="143ca-596">**描述**：*托盘标签*</span><span class="sxs-lookup"><span data-stu-id="143ca-596">**Description:** *Pallet labels*</span></span>
    - <span data-ttu-id="143ca-597">**波次步骤代码**：*Pallet*</span><span class="sxs-lookup"><span data-stu-id="143ca-597">**Wave step code:** *Pallet*</span></span>
    - <span data-ttu-id="143ca-598">**仓库**：*62*</span><span class="sxs-lookup"><span data-stu-id="143ca-598">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="143ca-599">在**常规**快速选项卡上，在**波次标签类型**字段中，选择一个值，如*托盘*。</span><span class="sxs-lookup"><span data-stu-id="143ca-599">On the **General** FastTab, in the **Wave label type** field, select a value, such as *Pallet*.</span></span>
1. <span data-ttu-id="143ca-600">在**波次标签模板详细信息**快速选项卡上，添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="143ca-600">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="143ca-601">**标签布局 ID**：*Pallet*</span><span class="sxs-lookup"><span data-stu-id="143ca-601">**Label layout ID:** *Pallet*</span></span>
    - <span data-ttu-id="143ca-602">**打印机名称：** 选择适当的 ZPL 打印机。</span><span class="sxs-lookup"><span data-stu-id="143ca-602">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="143ca-603">**运行查询**：*是*（此设置是可选的，但建议使用此设置以获得最佳性能。）</span><span class="sxs-lookup"><span data-stu-id="143ca-603">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="143ca-604">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="143ca-604">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="143ca-605">可选：如果要设置客户特定的标签设计，则必须创建查询来查找客户的帐户。</span><span class="sxs-lookup"><span data-stu-id="143ca-605">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="143ca-606">在**波次标签模板详细信息**快速选项卡上，选择**编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="143ca-606">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="143ca-607">然后，在查询编辑器对话框的**范围**选项卡上，添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="143ca-607">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="143ca-608">**表**：*装运*</span><span class="sxs-lookup"><span data-stu-id="143ca-608">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="143ca-609">**派生表**：*装运*</span><span class="sxs-lookup"><span data-stu-id="143ca-609">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="143ca-610">**字段**：*帐号*</span><span class="sxs-lookup"><span data-stu-id="143ca-610">**Field:** *Account number*</span></span>
    - <span data-ttu-id="143ca-611">**条件：** 输入相关的客户帐号。</span><span class="sxs-lookup"><span data-stu-id="143ca-611">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="143ca-612">完成后，选择**确定**关闭查询编辑器对话框。</span><span class="sxs-lookup"><span data-stu-id="143ca-612">When you've finished, select **OK** to close the query editor dialog box.</span></span> 

1. <span data-ttu-id="143ca-613">在操作窗格上，选择**编辑查询**打开整个标签模板的查询编辑器对话框。</span><span class="sxs-lookup"><span data-stu-id="143ca-613">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="143ca-614">在查询编辑器对话框的**排序**选项卡上，添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="143ca-614">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="143ca-615">**表**：*工作行*</span><span class="sxs-lookup"><span data-stu-id="143ca-615">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="143ca-616">**派生表**：*工作行*</span><span class="sxs-lookup"><span data-stu-id="143ca-616">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="143ca-617">**字段**：*参考负荷行 ID（记录 ID）*</span><span class="sxs-lookup"><span data-stu-id="143ca-617">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="143ca-618">**搜索方向**：*升序*</span><span class="sxs-lookup"><span data-stu-id="143ca-618">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="143ca-619">再添加一个具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="143ca-619">Add a second row that has the following settings:</span></span>

    - <span data-ttu-id="143ca-620">**表**：*工作行*</span><span class="sxs-lookup"><span data-stu-id="143ca-620">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="143ca-621">**派生表**：*工作行*</span><span class="sxs-lookup"><span data-stu-id="143ca-621">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="143ca-622">**字段**：*装运 ID*</span><span class="sxs-lookup"><span data-stu-id="143ca-622">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="143ca-623">**搜索方向**：*升序*</span><span class="sxs-lookup"><span data-stu-id="143ca-623">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="143ca-624">选择**确定**关闭查询编辑器对话框。</span><span class="sxs-lookup"><span data-stu-id="143ca-624">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="143ca-625">一个消息框将提示您确认分组重置操作。</span><span class="sxs-lookup"><span data-stu-id="143ca-625">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="143ca-626">选择**是**继续。</span><span class="sxs-lookup"><span data-stu-id="143ca-626">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="143ca-627">在操作窗格上，选择**波次标签模板组**。</span><span class="sxs-lookup"><span data-stu-id="143ca-627">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="143ca-628">在**波次标签模板组**对话框中，对于**参考字段名称**字段设置为*装运 ID* 的行，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="143ca-628">In the **Wave label template group** dialog box, for the row where the **Reference field name** field is set to *Shipment ID*, set the following values:</span></span>

    - <span data-ttu-id="143ca-629">**打印中断标签：** 选择此复选框。</span><span class="sxs-lookup"><span data-stu-id="143ca-629">**Print break label:** Select this check box.</span></span>
    - <span data-ttu-id="143ca-630">**标签布局 ID：** 选择一个中断标签。</span><span class="sxs-lookup"><span data-stu-id="143ca-630">**Label layout ID:** Select a break label.</span></span> <span data-ttu-id="143ca-631">（例如，选择您在此方案中先前创建的*中断*标签布局。）</span><span class="sxs-lookup"><span data-stu-id="143ca-631">(For example, select the *Break* label layout that you created earlier in this scenario.)</span></span>
    - <span data-ttu-id="143ca-632">**打印机名称：** 选择中断标签的打印机。</span><span class="sxs-lookup"><span data-stu-id="143ca-632">**Printer name:** Select the printer for the break label.</span></span> <span data-ttu-id="143ca-633">（通常，出于分割标签券的目的，您应该选择在**波次标签模板详细信息**上选择的同一台打印机。</span><span class="sxs-lookup"><span data-stu-id="143ca-633">(Typically, for the purpose of splitting label rolls, you should select the same printer that is selected on the **Wave label template details** FastTab.</span></span> <span data-ttu-id="143ca-634">但也可能是其他情况。）</span><span class="sxs-lookup"><span data-stu-id="143ca-634">However, other scenarios are possible.)</span></span>

1. <span data-ttu-id="143ca-635">对于将**参考字段名称**字段设置为*参考负荷行 ID* 的行，选择**标签生成 ID** 复选框。</span><span class="sxs-lookup"><span data-stu-id="143ca-635">For the row where the **Reference field name** field is set to *Reference load line id*, select the **Label build ID** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="143ca-636">无论工作分组设置如何，此设置都会在整个波次中为每个负荷行创建一个标签序列（“货箱 1/X”）。</span><span class="sxs-lookup"><span data-stu-id="143ca-636">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="143ca-637">此标签序列可以打印在标签布局上。</span><span class="sxs-lookup"><span data-stu-id="143ca-637">This label sequence can be printed on a label layout.</span></span> <span data-ttu-id="143ca-638">此外，不同装运的标签将由选定的中断标签分隔。</span><span class="sxs-lookup"><span data-stu-id="143ca-638">Additionally, labels for different shipments will be separated by the selected break label.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="143ca-639">配置编号规则扩展</span><span class="sxs-lookup"><span data-stu-id="143ca-639">Configure number sequence extensions</span></span>

<span data-ttu-id="143ca-640">编号规则扩展控制特定编号规则的 GS1 符合性。</span><span class="sxs-lookup"><span data-stu-id="143ca-640">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="143ca-641">此配置对于当前方案是可选的。</span><span class="sxs-lookup"><span data-stu-id="143ca-641">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="143ca-642">有关详细信息和配置说明，请参阅[配置编号规则扩展](../warehousing/configure-number-sequence-extensions.md)。</span><span class="sxs-lookup"><span data-stu-id="143ca-642">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="143ca-643">创建销售订单并将其下达到仓库</span><span class="sxs-lookup"><span data-stu-id="143ca-643">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="143ca-644">转到**销售和营销 \> 销售订单 \> 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="143ca-644">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="143ca-645">创建具有以下设置的销售订单：</span><span class="sxs-lookup"><span data-stu-id="143ca-645">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="143ca-646">**客户帐户**：*US-001*</span><span class="sxs-lookup"><span data-stu-id="143ca-646">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="143ca-647">**仓库**：*62*</span><span class="sxs-lookup"><span data-stu-id="143ca-647">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="143ca-648">添加两个销售订单行：</span><span class="sxs-lookup"><span data-stu-id="143ca-648">Add two sales order lines:</span></span>

    - <span data-ttu-id="143ca-649">销售订单行 1：</span><span class="sxs-lookup"><span data-stu-id="143ca-649">Sales order line 1:</span></span>

        - <span data-ttu-id="143ca-650">\**物料编号：\*\*\*A0001*</span><span class="sxs-lookup"><span data-stu-id="143ca-650">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="143ca-651">**数量：** *9024*</span><span class="sxs-lookup"><span data-stu-id="143ca-651">**Quantity:** *9024*</span></span>
        - <span data-ttu-id="143ca-652">**单位**：*个* (9024 个 = 376 箱 = 47 PL)</span><span class="sxs-lookup"><span data-stu-id="143ca-652">**Unit:** *ea* (9024 ea = 376 Box = 47 PL)</span></span>

    - <span data-ttu-id="143ca-653">销售订单行 2：</span><span class="sxs-lookup"><span data-stu-id="143ca-653">Sales order line 2:</span></span>

        - <span data-ttu-id="143ca-654">\**物料编号：\*\*\*A0002*</span><span class="sxs-lookup"><span data-stu-id="143ca-654">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="143ca-655">**数量：** *9016*</span><span class="sxs-lookup"><span data-stu-id="143ca-655">**Quantity:** *9016*</span></span>
        - <span data-ttu-id="143ca-656">**单位**：*个* (9016 个 = 322 箱 = 46 PL)</span><span class="sxs-lookup"><span data-stu-id="143ca-656">**Unit:** *ea* (9016 ea = 322 Box = 46 PL)</span></span>

    > [!NOTE]
    > <span data-ttu-id="143ca-657">此处提供的物料和数量仅是示例。</span><span class="sxs-lookup"><span data-stu-id="143ca-657">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="143ca-658">它们必须使用您先前定义的单位序列组，必须为它们定义从*个*到*箱*再到 *PL* 的适当单位转换，并且它们在仓库 *62* 中必须有存货。</span><span class="sxs-lookup"><span data-stu-id="143ca-658">They must use the unit sequence group that you defined earlier, appropriate unit conversions from *ea* to *Box* to *PL* must be defined for them, and they must have stock in warehouse *62*.</span></span> <span data-ttu-id="143ca-659">有关详细信息，请参阅[度量单位和库存策略](unit-measure-stocking-policies.md)。</span><span class="sxs-lookup"><span data-stu-id="143ca-659">For more information, see [Unit of measure and stocking policies](unit-measure-stocking-policies.md).</span></span>

1. <span data-ttu-id="143ca-660">选择销售订单行 1。</span><span class="sxs-lookup"><span data-stu-id="143ca-660">Select sales order line 1.</span></span> <span data-ttu-id="143ca-661">然后，在**销售订单行**部分的**库存**菜单中，选择**预留**。</span><span class="sxs-lookup"><span data-stu-id="143ca-661">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="143ca-662">在**预留**页的操作窗格中，选择**预留批次**，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="143ca-662">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="143ca-663">对销售订单行 2 重复步骤 4 和 5。</span><span class="sxs-lookup"><span data-stu-id="143ca-663">Repeat steps 4 and 5 for sales order line 2.</span></span>
1. <span data-ttu-id="143ca-664">在“操作窗格”上的**仓库**选项卡上，选择**发放到仓库**。</span><span class="sxs-lookup"><span data-stu-id="143ca-664">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="143ca-665">将发生以下事件：</span><span class="sxs-lookup"><span data-stu-id="143ca-665">The following events occur:</span></span> 

    - <span data-ttu-id="143ca-666">系统使用包含标签打印步骤的模板来处理创建的装运。</span><span class="sxs-lookup"><span data-stu-id="143ca-666">The system processes the created shipment by using the template that includes the label printing step.</span></span> <span data-ttu-id="143ca-667">标签布局将用于定义标签的格式，结果将是在标签模板中选择的打印机上打印的标签。</span><span class="sxs-lookup"><span data-stu-id="143ca-667">The label layout will be used to define the format of the label, and the result will be a label that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="143ca-668">波次标签将生成并打印。</span><span class="sxs-lookup"><span data-stu-id="143ca-668">Wave labels are generated and printed.</span></span> <span data-ttu-id="143ca-669">标签数量将等于货箱数量（在此示例中，行 1 是 376 箱标签，行 2 是 322 箱标签，行 1 是 47 PL 标签，行 2 是 47 PL 标签，以及两个具有装运 ID 的中断标签）。</span><span class="sxs-lookup"><span data-stu-id="143ca-669">The number of labels will equal the number of cartons (in this example, 376 Box labels for line 1, 322 Box labels for line 2, 47 PL labels for line 1, 47 PL labels for line 2, and two break labels that have the shipment ID).</span></span>
    - <span data-ttu-id="143ca-670">将为装运生成新提单 ID。</span><span class="sxs-lookup"><span data-stu-id="143ca-670">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="143ca-671">如果您配置了数字序列扩展，波次标签 ID 将采用 **SSCC-18** 数字格式。</span><span class="sxs-lookup"><span data-stu-id="143ca-671">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="143ca-672">您可以从以下页面查看和重新打印波次标签：</span><span class="sxs-lookup"><span data-stu-id="143ca-672">You can view and reprint wave labels from the following pages:</span></span>

- <span data-ttu-id="143ca-673">所有装运 \> 装运详细信息</span><span class="sxs-lookup"><span data-stu-id="143ca-673">All shipments \> Shipment details</span></span>
- <span data-ttu-id="143ca-674">所有负荷 \> 负荷详细信息</span><span class="sxs-lookup"><span data-stu-id="143ca-674">All loads \> Load details</span></span>
- <span data-ttu-id="143ca-675">所有波次</span><span class="sxs-lookup"><span data-stu-id="143ca-675">All waves</span></span>
- <span data-ttu-id="143ca-676">波次标签</span><span class="sxs-lookup"><span data-stu-id="143ca-676">Wave labels</span></span>
- <span data-ttu-id="143ca-677">波次标签历史记录</span><span class="sxs-lookup"><span data-stu-id="143ca-677">Wave label history</span></span>

<span data-ttu-id="143ca-678">对于这些页面中的大多数页面，可以通过在“操作窗格”的**装运**选项卡上的**相关信息**组中选择**波次标签**来查找相关功能。</span><span class="sxs-lookup"><span data-stu-id="143ca-678">For most of these pages, you can find the relevant function by selecting **Wave labels** in the **Related information** group on the **Shipments** tab of the Action Pane.</span></span>
