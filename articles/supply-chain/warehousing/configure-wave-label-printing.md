---
title: 波次标签打印
description: 本主题介绍了波次标签打印并解释了如何进行设置。
author: perlynne
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate, WHSWaveLabelLayoutRow, WHSDocumentRouting, WHSWaveTableListPage, WHSPostMethod, WHSMobileDisplayWaveLabelListLookup, WHSWaveLabelType, WHSWaveLabelTemplateGroup, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: yyyy-mm-dd
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 14a32f7fc4608ef8910646f80786a188c46dc89d
ms.sourcegitcommit: 0cc89dd42c1924ca0ec735c6566bc56b39cc5f7d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/26/2021
ms.locfileid: "6102606"
---
# <a name="wave-label-printing"></a><span data-ttu-id="1b1ce-103">波次标签打印</span><span class="sxs-lookup"><span data-stu-id="1b1ce-103">Wave label printing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1b1ce-104">波次标签打印通过引入新波次步骤方法提供另一种标签打印方法，让您可以在波次执行过程中直接从波次模板创建和打印标签。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-104">Wave label printing offers an alternative approach to label printing by introducing a new wave step method that lets you create and print labels directly from the wave template during wave execution.</span></span> <span data-ttu-id="1b1ce-105">因此，在工作人员在移动设备上运行工作订单之前，标签已经可用。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-105">Therefore, the labels will already be available before workers run the work order on a mobile device.</span></span> <span data-ttu-id="1b1ce-106">然后，工作人员可以在领料期间而不是领料后附上所需的标签。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-106">Workers can then attach the required labels during picking instead of after picking.</span></span>

<span data-ttu-id="1b1ce-107">波次标签打印使用 Zebra 编程语言 (ZPL) 来创建标签布局。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-107">Wave label printing uses Zebra Programming Language (ZPL) to create label layouts.</span></span> <span data-ttu-id="1b1ce-108">标签布局分为三个部分（页眉、主体和页脚），以允许具有重复结构的标签。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-108">A label layout is divided into three sections (header, body, and footer) to allow for labels that have repeating structure.</span></span> <span data-ttu-id="1b1ce-109">波次标签模板告诉系统要使用的标签布局。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-109">Wave label templates tell the system which label layout to use.</span></span> <span data-ttu-id="1b1ce-110">用户可以指定使用哪台打印机。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-110">Users can specify which printer is used.</span></span> <span data-ttu-id="1b1ce-111">他们还可以根据需要同时在多台打印机上打印标签。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-111">They can also print labels on several printers at the same time, as they require.</span></span> <span data-ttu-id="1b1ce-112">**波次标签历史记录** 页面显示使用此设置创建的所有标签的记录。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-112">The **Wave label history** page shows a record of all labels that have been created by using this setup.</span></span>

<span data-ttu-id="1b1ce-113">您可以根据工作标题打印和逐份打印标签，可以为每个工作标题打印中断标签，还可以打印集装箱内容标签、外箱标签和其他类似标签。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-113">You can print and collate labels based on work headers, you can print break labels per work header, and you can print container content labels, case labels, and other similar labels.</span></span>

> [!NOTE]
> <span data-ttu-id="1b1ce-114">此功能不会替代基于文档路线的现有标签打印功能。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-114">This functionality doesn't replace existing label printing functionality that is based on document routing.</span></span>

<span data-ttu-id="1b1ce-115">波次标签打印提供以下增强功能：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-115">Wave label printing offers the following enhancements:</span></span>

- <span data-ttu-id="1b1ce-116">根据一个工作行上的货箱数量打印标签，无需使用集装化。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-116">Print labels according to the number of cartons on a single work line, without using containerization.</span></span> <span data-ttu-id="1b1ce-117">（“货箱”是在单位序列组行上指定的单位。）</span><span class="sxs-lookup"><span data-stu-id="1b1ce-117">(A "carton" is a unit that is designated on unit sequence group lines.)</span></span>
- <span data-ttu-id="1b1ce-118">打印几个不同的标签序列（例如，货箱和托盘标签）。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-118">Print several different label sequences (for example, carton and pallet labels).</span></span>
- <span data-ttu-id="1b1ce-119">加入标签枚举（例如，1/124、2/124 ... 124/124），并定义枚举的范围（例如，工作行、负荷行或装运）。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-119">Include label enumeration (for example, 1/124, 2/124, ... 124/124), and define the range of enumeration (for example, work line, load line, or shipment).</span></span>
- <span data-ttu-id="1b1ce-120">在生成提单之前，在标签上创建和打印提单 ID。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-120">Create and print a bill of lading ID on labels before the bill of lading is generated.</span></span>
- <span data-ttu-id="1b1ce-121">为每个货箱创建唯一的系列货运集装箱代码 (SSCC)，并将其加入每个标签。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-121">Create a unique serial shipping container code (SSCC) for each carton, and include it on each label.</span></span>
- <span data-ttu-id="1b1ce-122">为提单 ID 和 SSCC 创建符合 GS1 的编号规则。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-122">Create GS1-compliant number sequences for bill of lading IDs and SSCCs.</span></span>
- <span data-ttu-id="1b1ce-123">重新打印来自移动设备和富客户端的标签。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-123">Reprint labels from both mobile devices and the rich client.</span></span>
- <span data-ttu-id="1b1ce-124">取消标签（例如，在领料短缺情景中），然后重新打印。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-124">Void labels (for example, in short pick scenarios), and reprint them.</span></span>
- <span data-ttu-id="1b1ce-125">清除波次标签历史记录。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-125">Clean up the wave label history.</span></span>
- <span data-ttu-id="1b1ce-126">在文档路线布局和波次标签布局之间共享对文档路线布局的改进。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-126">Improvements to document routing layouts are shared between document routing layouts and wave label layouts.</span></span> <span data-ttu-id="1b1ce-127">（有关详细信息，请参阅[牌照的文档路线布局](../warehousing/document-routing-layout-for-license-plates.md)）</span><span class="sxs-lookup"><span data-stu-id="1b1ce-127">(For more information, see [Document routing layout for license plates](../warehousing/document-routing-layout-for-license-plates.md).)</span></span>

<span data-ttu-id="1b1ce-128">这些增强功能让在安装货盘前为货箱附加标签更加高效。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-128">These enhancements make it more efficient to label cartons before palletization.</span></span> <span data-ttu-id="1b1ce-129">它们特别有利于向那些通过分别扫描每个货箱自动确认订单收货的大型零售商发货的公司。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-129">They especially benefit companies that ship to large retailers that automatically confirm order receipts by scanning each carton separately.</span></span>

> [!NOTE]
> <span data-ttu-id="1b1ce-130">您可以根据业务要求单独或组合实现本主题中介绍的配置方案。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-130">You can implement the configuration scenarios that are described in this topic either separately or in combination, depending on your business requirements.</span></span> <span data-ttu-id="1b1ce-131">您可以设计几个按顺序工作的波次标签模板（如方案 3 所示）。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-131">You can design several wave label templates that work in sequence (as illustrated in scenario 3).</span></span> <span data-ttu-id="1b1ce-132">例如，您可以使用方案 1 打印货箱标签，使用方案 2 打印托盘标签（如果存货的托盘在尺寸和构成方面不同）。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-132">For example, you can use scenario 1 to print carton labels and scenario 2 to print pallet labels (if pallets in stock vary in size and composition).</span></span>

## <a name="turn-on-the-wave-label-printing-feature"></a><span data-ttu-id="1b1ce-133">开启波次标签打印功能</span><span class="sxs-lookup"><span data-stu-id="1b1ce-133">Turn on the Wave label printing feature</span></span>

<span data-ttu-id="1b1ce-134">*波次标签打印* 功能只有在系统中开启之后才能使用。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-134">Before you can use the *Wave label printing* feature, it must be turned on in your system.</span></span> <span data-ttu-id="1b1ce-135">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区检查功能状态和开启功能（如果需要）。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-135">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="1b1ce-136">在那里，此功能以以下方式列出：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-136">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="1b1ce-137">**模块**：*仓库管理*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-137">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="1b1ce-138">**功能名称**：*波次标签打印*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-138">**Feature name:** *Wave label printing*</span></span>

## <a name="scenario-1-wave-label-printing-where-a-single-wave-label-is-generated"></a><span data-ttu-id="1b1ce-139">方案 1：生成单个波次标签的波次标签打印</span><span class="sxs-lookup"><span data-stu-id="1b1ce-139">Scenario 1: Wave label printing where a single wave label is generated</span></span>

<span data-ttu-id="1b1ce-140">此方案演示公司如何为通过分别扫描每个货箱来自动确认订单收货的大型零售商打印发货标签。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-140">This scenario shows how a company can print shipping labels for a large retailer that automatically confirms order receipts by scanning each carton separately.</span></span>

<span data-ttu-id="1b1ce-141">此方案演示端到端流。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-141">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="1b1ce-142">提供演示数据</span><span class="sxs-lookup"><span data-stu-id="1b1ce-142">Make demo data available</span></span>

<span data-ttu-id="1b1ce-143">要采取此方案，必须安装演示数据，并且必须选择 **USMF** 法人。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-143">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-the-wave-label-method-is-available"></a><span data-ttu-id="1b1ce-144">确保波次标签方法可用</span><span class="sxs-lookup"><span data-stu-id="1b1ce-144">Make sure that the wave label method is available</span></span>

<span data-ttu-id="1b1ce-145">您可能必须重新生成波次处理方法，才能使波次标签打印方法可用。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-145">You might have to regenerate the wave process methods to make the wave label printing method available.</span></span>

1. <span data-ttu-id="1b1ce-146">转到 **仓库管理 \> 设置 \> 波次 \> 波次处理方法**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-146">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="1b1ce-147">确认 **waveLabelPrinting** 在列表中。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-147">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="1b1ce-148">如果不在，请在操作窗格中选择 **重新生成方法** 添加该方法。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-148">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="configure-a-wave-template"></a><span data-ttu-id="1b1ce-149">配置波次模板</span><span class="sxs-lookup"><span data-stu-id="1b1ce-149">Configure a wave template</span></span>

<span data-ttu-id="1b1ce-150">波次模板使您可以将波次方法的特定实例链接到相应的波次标签模板。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-150">Wave templates let you link specific instances of wave methods to a corresponding wave label template.</span></span>

1. <span data-ttu-id="1b1ce-151">转到 **仓库管理 \> 设置 \> 波次 \> 波次模板**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-151">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="1b1ce-152">选择模板，如 **62 装运默认**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-152">Select a template, such as **62 Shipping Default**.</span></span>
1. <span data-ttu-id="1b1ce-153">在 **方法** 快速选项卡上，将 **波次标签打印** 方法移至 **选定方法** 列。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-153">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
1. <span data-ttu-id="1b1ce-154">在 **选定方法** 列中，选择 **波次标签打印** 方法，并将其 **波次步骤代码** 字段设置为 *PrintLabel*。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-154">In the **Selected methods** column, select the **Wave label printing** method, and set its **Wave step code** field to *PrintLabel*.</span></span> <span data-ttu-id="1b1ce-155">有关波次步骤代码的详细信息，请参阅[波次步骤代码](wave-step-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-155">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-a-wave-label-layout"></a><span data-ttu-id="1b1ce-156">创建波次标签布局</span><span class="sxs-lookup"><span data-stu-id="1b1ce-156">Create a wave label layout</span></span>

<span data-ttu-id="1b1ce-157">标签布局控制在标签上打印什么信息以及如何布置信息。在这里，您输入发送到打印机的 ZPL 代码。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-157">The label layout controls what information is printed on the label and how it's laid out. Here, you enter the ZPL code that is sent to the printer.</span></span>

1. <span data-ttu-id="1b1ce-158">转到 **仓库管理 \> 设置 \> 文档路线布局 \> 波次标签布局**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-158">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="1b1ce-159">创建一个具有以下设置的记录：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-159">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="1b1ce-160">**标签布局 ID**：*Carton*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-160">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="1b1ce-161">**描述**：*货箱 (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-161">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="1b1ce-162">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-162">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="1b1ce-163">在操作窗格上，选择 **波次标签行设置**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-163">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="1b1ce-164">**波次标签行设置** 页面将出现。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-164">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="1b1ce-165">在这里，您可以配置标签的动态部分。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-165">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="1b1ce-166">添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-166">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="1b1ce-167">**行 ID**：*WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-167">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="1b1ce-168">**行表名称**：*WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-168">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="1b1ce-169">**行开始位置**：*0*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-169">**Row start position:** *0*</span></span>

        <span data-ttu-id="1b1ce-170">此字段定义行在标签上开始的垂直位置。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-170">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="1b1ce-171">**行高度**：*0*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-171">**Row height:** *0*</span></span>

        <span data-ttu-id="1b1ce-172">此字段根据 ZPL 标准定义每行的高度（以磅为单位）。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-172">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="1b1ce-173">行高度对于水平标签为正，对于垂直标签为负。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-173">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="1b1ce-174">在此示例中因为只有一行，所以您可以将此值设置为 *0*（零）。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-174">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="1b1ce-175">**每页行数**：*1*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-175">**Rows per page:** *1*</span></span>

        <span data-ttu-id="1b1ce-176">此字段定义可以在每个标签上打印的行数。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-176">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="1b1ce-177">使用此设置，将为波次标签表中的每个记录打印一个单独的 ZPL 标签。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-177">This setup will cause a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="1b1ce-178">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-178">Close the page.</span></span>
1. <span data-ttu-id="1b1ce-179">在操作窗格上，选择 **编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-179">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="1b1ce-180">在查询编辑器对话框的 **范围** 选项卡上，添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-180">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="1b1ce-181">**表**：*工作行*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-181">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="1b1ce-182">**派生表**：*工作行*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-182">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="1b1ce-183">**字段**：*工作类型*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-183">**Field:** *Work type*</span></span>
    - <span data-ttu-id="1b1ce-184">**条件**：*领料*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-184">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="1b1ce-185">此查询可确保在标签上仅打印领料类型的工作行，不打印放置类型的工作行。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-185">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="1b1ce-186">如果您希望能够打印提单 ID，请在 **联接** 选项卡上，选择 **工作行** 表，然后将 **装运** 表与其联接。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-186">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="1b1ce-187">关闭查询编辑器对话框。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-187">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="1b1ce-188">**打印机文本布局** 快速选项卡有三个部分，您可以在其中编写打印机代码：**页眉部分**、**主体部分** 和 **页脚部分**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-188">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="1b1ce-189">在 **页眉部分** 的 **标签页眉** 字段中，输入所需页眉的代码。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-189">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="1b1ce-190">例如，如果您使用的是 Zebra 打印机，可以使用以下代码。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-190">For example, if you're using Zebra printers, you can use the following code.</span></span>

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

1. <span data-ttu-id="1b1ce-191">在 **主体部分** 的 **标签主体** 字段中，输入所需主体的 ZPL 代码。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-191">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="1b1ce-192">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-192">Here is an example.</span></span>

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

1. <span data-ttu-id="1b1ce-193">在 **主体部分** 的 **标签页脚** 字段中，输入所需页脚的 ZPL 代码。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-193">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="1b1ce-194">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-194">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="1b1ce-195">此设置将打印每个标签的一个副本。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-195">This setup will print one copy of each label.</span></span> <span data-ttu-id="1b1ce-196">如果需要更多副本（例如，托盘每一面一个副本），请将页脚中 **\^PQn** 部分的 **n** 值设置为所需的副本数。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-196">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="1b1ce-197">例如，每个标签要打印四个副本，请指定 **\^PQ4**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-197">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

<span data-ttu-id="1b1ce-198">您的标签现在可以使用了。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-198">Your label is now ready to use.</span></span>

### <a name="create-a-wave-label-type"></a><span data-ttu-id="1b1ce-199">创建波次标签类型</span><span class="sxs-lookup"><span data-stu-id="1b1ce-199">Create a wave label type</span></span>

<span data-ttu-id="1b1ce-200">波次标签类型用于将波次标签模板链接到单元序列组行上的单元。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-200">Wave label types are used to link wave label templates to a unit on unit sequence group lines.</span></span>

1. <span data-ttu-id="1b1ce-201">转到 **仓库管理 \> 设置 \> 文档路线布局 \> 波次标签类型**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-201">Go to **Warehouse management \> Setup \> Document routing \> Wave label types**.</span></span>
1. <span data-ttu-id="1b1ce-202">添加具有以下设置的波次标签类型：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-202">Add a wave label type that has the following settings:</span></span>

    - <span data-ttu-id="1b1ce-203">**标签类型**：*货箱*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-203">**Label type:** *Carton*</span></span>
    - <span data-ttu-id="1b1ce-204">**描述**：*货箱*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-204">**Description:** *Carton*</span></span>

### <a name="set-up-unit-sequence-groups"></a><span data-ttu-id="1b1ce-205">设置单位序列组</span><span class="sxs-lookup"><span data-stu-id="1b1ce-205">Set up unit sequence groups</span></span>

<span data-ttu-id="1b1ce-206">接下来，设置波次标签类型的单位序列组。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-206">Next, set up the unit sequence group for the wave label type.</span></span>

1. <span data-ttu-id="1b1ce-207">转到 **仓库管理 \> 设置 \> 仓库 \> 单位序列组**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-207">Go to **Warehouse management \> Setup \> Warehouse \> Unit sequence groups**.</span></span>
1. <span data-ttu-id="1b1ce-208">选择 **Ea Box PL** 组。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-208">Select the **Ea Box PL** group.</span></span>
1. <span data-ttu-id="1b1ce-209">对于 **箱** 行，将 **波次级别类型** 字段设置为 *货箱*。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-209">For the **Box** line, set the **Wave level type** field to *Carton*.</span></span>

### <a name="create-a-wave-label-template"></a><span data-ttu-id="1b1ce-210">创建波次标签模板</span><span class="sxs-lookup"><span data-stu-id="1b1ce-210">Create a wave label template</span></span>

<span data-ttu-id="1b1ce-211">接下来，为波次标签类型创建波次标签模板。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-211">Next, create the wave label template for the wave label type.</span></span>

1. <span data-ttu-id="1b1ce-212">转到 **仓库管理 \> 设置 \> 文档路线布局 \> 波次标签模板**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-212">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="1b1ce-213">添加波次级别模板，并在页眉中设置以下值：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-213">Add a wave level template, and set the following values in the header:</span></span>

    - <span data-ttu-id="1b1ce-214">**标签模板名称**：*货箱标签*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-214">**Label template name:** *Carton labels*</span></span>
    - <span data-ttu-id="1b1ce-215">**描述**：*货箱标签*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-215">**Description:** *Carton labels*</span></span>
    - <span data-ttu-id="1b1ce-216">**波次步骤代码**：*PrintLabel*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-216">**Wave step code:** *PrintLabel*</span></span>
    - <span data-ttu-id="1b1ce-217">**仓库**：*62*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-217">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="1b1ce-218">在 **常规** 快速选项卡上，将 **波次标签类型** 字段设置为 *货箱*。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-218">On the **General** FastTab, set the **Wave label type** field to *Carton*.</span></span>
1. <span data-ttu-id="1b1ce-219">在 **波次标签模板详细信息** 快速选项卡上，添加具有以下设置的新行：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-219">On the **Wave label template details** FastTab, add a new row that has the following settings:</span></span>

    - <span data-ttu-id="1b1ce-220">**标签布局 ID**：*Carton*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-220">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="1b1ce-221">**打印机名称：** 选择适当的 ZPL 打印机。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-221">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="1b1ce-222">**运行查询**：*是*（此设置是可选的，但建议使用此设置以获得最佳性能。）</span><span class="sxs-lookup"><span data-stu-id="1b1ce-222">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="1b1ce-223">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-223">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="1b1ce-224">可选：如果要设置客户特定的标签设计，则必须创建查询来查找客户的帐户。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-224">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="1b1ce-225">在 **波次标签模板详细信息** 快速选项卡上，选择 **编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-225">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="1b1ce-226">然后，在查询编辑器对话框的 **范围** 选项卡上，添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-226">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="1b1ce-227">**表**：*装运*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-227">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="1b1ce-228">**派生表**：*装运*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-228">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="1b1ce-229">**字段**：*帐号*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-229">**Field:** *Account number*</span></span>
    - <span data-ttu-id="1b1ce-230">**条件：** 输入相关的客户帐号。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-230">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="1b1ce-231">完成后，选择 **确定** 关闭查询编辑器对话框。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-231">When you've finished, select **OK** to close the query editor dialog box.</span></span>

1. <span data-ttu-id="1b1ce-232">在操作窗格上，选择 **编辑查询** 打开整个标签模板的查询编辑器对话框。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-232">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="1b1ce-233">在查询编辑器对话框的 **排序** 选项卡上，添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-233">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="1b1ce-234">**表**：*工作行*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-234">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="1b1ce-235">**派生表**：*工作行*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-235">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="1b1ce-236">**字段**：*参考负荷行 ID（记录 ID）*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-236">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="1b1ce-237">**搜索方向**：*升序*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-237">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="1b1ce-238">选择 **确定** 关闭查询编辑器对话框。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-238">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="1b1ce-239">一个消息框将提示您确认分组重置操作。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-239">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="1b1ce-240">选择 **是** 继续。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-240">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="1b1ce-241">在操作窗格上，选择 **波次标签模板组**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-241">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="1b1ce-242">在 **波次标签模板组** 对话框中，选择 **参考字段名称** 字段设置为 *参考负荷行 ID* 的行，然后选择此行的 **标签生成 ID** 复选框。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-242">In the **Wave label template group** dialog box, select the row where the **Reference field name** field is set to *Reference load line id*, and then select the **Label build ID** check box for this row.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1b1ce-243">无论工作分组设置如何，此设置都会在整个波次中为每个负荷行创建一个标签序列（“货箱 1/X”）。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-243">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="1b1ce-244">此标签序列可以打印在标签布局上。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-244">This label sequence can be printed on the label layout.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="1b1ce-245">配置编号规则扩展</span><span class="sxs-lookup"><span data-stu-id="1b1ce-245">Configure number sequence extensions</span></span>

<span data-ttu-id="1b1ce-246">编号规则扩展控制特定编号规则的 GS1 符合性。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-246">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="1b1ce-247">此配置对于当前方案是可选的。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-247">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="1b1ce-248">有关详细信息和配置说明，请参阅[配置编号规则扩展](../warehousing/configure-number-sequence-extensions.md)。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-248">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="1b1ce-249">创建销售订单并将其下达到仓库</span><span class="sxs-lookup"><span data-stu-id="1b1ce-249">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="1b1ce-250">转到 **销售和营销 \> 销售订单 \> 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-250">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="1b1ce-251">创建具有以下设置的销售订单：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-251">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="1b1ce-252">**客户帐户**：*US-001*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-252">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="1b1ce-253">**仓库**：*62*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-253">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="1b1ce-254">添加两个具有以下设置的销售订单行：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-254">Add two sales order lines that have the following settings:</span></span>

    - <span data-ttu-id="1b1ce-255">销售订单行 1：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-255">Sales order line 1:</span></span>

        - <span data-ttu-id="1b1ce-256">\**物料编号：\*\*\*A0001*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-256">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="1b1ce-257">**数量：** *9024*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-257">**Quantity:** *9024*</span></span>
        - <span data-ttu-id="1b1ce-258">**单位**：*个* (9024 个 = 376 箱 = 47 PL)</span><span class="sxs-lookup"><span data-stu-id="1b1ce-258">**Unit:** *ea* (9024 ea = 376 Box = 47 PL)</span></span>

    - <span data-ttu-id="1b1ce-259">销售订单行 2：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-259">Sales order line 2:</span></span>

        - <span data-ttu-id="1b1ce-260">\**物料编号：\*\*\*A0002*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-260">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="1b1ce-261">**数量：** *9016*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-261">**Quantity:** *9016*</span></span>
        - <span data-ttu-id="1b1ce-262">**单位**：*个* (9016 个 = 322 箱 = 46 PL)</span><span class="sxs-lookup"><span data-stu-id="1b1ce-262">**Unit:** *ea* (9016 ea = 322 Box = 46 PL)</span></span>

    > [!NOTE]
    > <span data-ttu-id="1b1ce-263">此处提供的物料和数量仅是示例。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-263">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="1b1ce-264">它们必须使用您先前定义的单位序列组，必须为它们定义从 *个* 到 *箱* 再到 *PL* 的适当单位转换，并且它们在仓库 *62* 中必须有存货。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-264">They must use the unit sequence group that you defined earlier, appropriate unit conversions from *ea* to *Box* to *PL* must be defined for them, and they must have stock in warehouse *62*.</span></span> <span data-ttu-id="1b1ce-265">有关详细信息，请参阅[度量单位和库存策略](unit-measure-stocking-policies.md)。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-265">For more information, see [Unit of measure and stocking policies](unit-measure-stocking-policies.md).</span></span>

1. <span data-ttu-id="1b1ce-266">选择销售订单行 1。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-266">Select sales order line 1.</span></span> <span data-ttu-id="1b1ce-267">然后，在 **销售订单行** 部分的 **库存** 菜单中，选择 **预留**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-267">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="1b1ce-268">在 **预留** 页的操作窗格中，选择 **预留批次**，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-268">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="1b1ce-269">对销售订单行 2 重复步骤 4 和 5。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-269">Repeat steps 4 and 5 for sales order line 2.</span></span>
1. <span data-ttu-id="1b1ce-270">在“操作窗格”上的 **仓库** 选项卡上，选择 **发放到仓库**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-270">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="1b1ce-271">将发生以下事件：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-271">The following events occur:</span></span>

    - <span data-ttu-id="1b1ce-272">系统使用包含标签打印步骤的模板来处理创建的装运。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-272">The system processes the created shipment by using the template that includes the label printing step.</span></span> <span data-ttu-id="1b1ce-273">标签布局将用于定义标签的格式，结果将是在标签模板中选择的打印机上打印的标签。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-273">The label layout will be used to define the format of the label, and the result will be a label that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="1b1ce-274">波次标签将生成并打印。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-274">Wave labels are generated and printed.</span></span> <span data-ttu-id="1b1ce-275">标签数量将等于货箱数量（在此示例中，行 1 是 376 箱标签，行 2 是 322 箱标签）。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-275">The number of labels will equal the number of cartons (in this example, 376 Box labels for line 1 and 322 Box labels for line 2).</span></span>
    - <span data-ttu-id="1b1ce-276">将为装运生成新提单 ID。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-276">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="1b1ce-277">如果您配置了数字序列扩展，波次标签 ID 将采用 **SSCC-18** 数字格式。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-277">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="1b1ce-278">您可以从以下页面查看和重新打印波次标签。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-278">You can view and reprint wave labels from the following pages.</span></span> <span data-ttu-id="1b1ce-279">在每页的“操作窗格”上的 **装运** 选项卡上，在 **相关信息** 组中，选择 **波次标签**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-279">On the Action Pane of each page, on the **Shipments** tab, in the **Related information** group, select **Wave labels**.</span></span>

- <span data-ttu-id="1b1ce-280">所有装运 \> 装运详细信息</span><span class="sxs-lookup"><span data-stu-id="1b1ce-280">All shipments \> Shipment details</span></span>
- <span data-ttu-id="1b1ce-281">所有负荷 \> 负荷详细信息</span><span class="sxs-lookup"><span data-stu-id="1b1ce-281">All loads \> Load details</span></span>
- <span data-ttu-id="1b1ce-282">所有波次</span><span class="sxs-lookup"><span data-stu-id="1b1ce-282">All waves</span></span>
- <span data-ttu-id="1b1ce-283">波次标签</span><span class="sxs-lookup"><span data-stu-id="1b1ce-283">Wave labels</span></span>
- <span data-ttu-id="1b1ce-284">波次标签历史记录</span><span class="sxs-lookup"><span data-stu-id="1b1ce-284">Wave label history</span></span>

## <a name="scenario-2-wave-label-printing-for-containerization-without-wave-label-records"></a><span data-ttu-id="1b1ce-285">方案 2：集装化的波次标签打印（不使用波次标签记录）</span><span class="sxs-lookup"><span data-stu-id="1b1ce-285">Scenario 2: Wave label printing for containerization (without wave label records)</span></span>

<span data-ttu-id="1b1ce-286">此方案使您可以在使用集装化自动将物料拆分到货箱时打印波次标签，因此不需要波次标签记录。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-286">This scenario lets you print wave labels when you use containerization to automatically split items into cartons and therefore don't require a wave label record.</span></span> <span data-ttu-id="1b1ce-287">在这种情况下，集装箱 ID 充当 SSCC 的占位符。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-287">In this case, the container ID acts as a placeholder for the SSCC.</span></span>

<span data-ttu-id="1b1ce-288">以下是此方案与方案 1 之间的主要区别：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-288">Here are the main differences between this scenario and scenario 1:</span></span>

- <span data-ttu-id="1b1ce-289">**波次标签模板：** 您无需在波次标签模板上选择波次标签类型，也不需要标签生成分组。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-289">**Wave label templates:** You won't select a wave label type on the wave label template, and you won't require a label build grouping.</span></span> <span data-ttu-id="1b1ce-290">另外，您将按照方案 1 中所述的相同方式配置波次标签模板并链接到波次模板。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-290">Otherwise, you will configure the wave label template and link to the wave template in the same way that is described in scenario 1.</span></span> <span data-ttu-id="1b1ce-291">您必须将波次标签类型保留为空白，以防止生成波次标签。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-291">You must leave the wave label type blank to prevent wave labels from being generated.</span></span>
- <span data-ttu-id="1b1ce-292">**波次标签布局：** 您将为工作行（而不是波次标签记录）配置波次标签布局行设置。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-292">**Wave label layouts:** You will configure the wave label layout row settings for work lines instead of wave label records.</span></span> <span data-ttu-id="1b1ce-293">您必须使用 **WHSWorkLine** 表而不是 **WHSWaveLabel** 表来配置标签布局的行设置。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-293">You must configure the row setting for the label layout by using the **WHSWorkLine** table instead of the **WHSWaveLabel** table.</span></span> <span data-ttu-id="1b1ce-294">**每页行数** 设置控制主体部分将具有的行数。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-294">The **Rows per page** setting controls the number of rows that the body section will have.</span></span> 

<span data-ttu-id="1b1ce-295">此配置也适用于将多个不同物料包装到一个带标签的箱子或托盘的业务场景，此包装流程可以通过创建工作（例如，按装运分组的工作）定义。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-295">This configuration is also suitable for business scenarios where multiple different items are packed into one labeled box or into a pallet, and this packing process can be defined by work creation (for example, work that is grouped by shipment).</span></span>

<span data-ttu-id="1b1ce-296">此方案演示端到端流。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-296">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="1b1ce-297">提供演示数据</span><span class="sxs-lookup"><span data-stu-id="1b1ce-297">Make demo data available</span></span>

<span data-ttu-id="1b1ce-298">要采取此方案，必须安装演示数据，并且必须选择 **USMF** 法人。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-298">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-the-wave-label-method-is-available"></a><span data-ttu-id="1b1ce-299">确保波次标签方法可用</span><span class="sxs-lookup"><span data-stu-id="1b1ce-299">Make sure that the wave label method is available</span></span>

<span data-ttu-id="1b1ce-300">您可能必须重新生成波次处理方法，才能使波次标签打印方法可用。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-300">You might have to regenerate the wave process methods to make the wave label printing method available.</span></span>

1. <span data-ttu-id="1b1ce-301">转到 **仓库管理 \> 设置 \> 波次 \> 波次处理方法**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-301">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="1b1ce-302">确认 **waveLabelPrinting** 在列表中。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-302">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="1b1ce-303">如果不在，请在操作窗格中选择 **重新生成方法** 添加该方法。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-303">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="1b1ce-304">设置波次模板</span><span class="sxs-lookup"><span data-stu-id="1b1ce-304">Set up a wave template</span></span>

<span data-ttu-id="1b1ce-305">波次模板使您可以将波次方法的特定实例链接到相应的波次标签模板。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-305">Wave templates let you link specific instances of wave methods to a corresponding wave label template.</span></span>

1. <span data-ttu-id="1b1ce-306">转到 **仓库管理 \> 设置 \> 波次 \> 波次模板**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-306">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="1b1ce-307">选择模板，如 **63 集装化**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-307">Select a template, such as **63 Containerization**.</span></span>
1. <span data-ttu-id="1b1ce-308">在 **方法** 快速选项卡上，将 **波次标签打印** 方法移至 **选定方法** 列。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-308">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
1. <span data-ttu-id="1b1ce-309">在 **选定方法** 列中，选择 **波次标签打印** 方法，并将其 **波次步骤代码** 字段设置为 *PrintLabel*。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-309">In the **Selected methods** column, select the **Wave label printing** method, and set its **Wave step code** field to *PrintLabel*.</span></span> <span data-ttu-id="1b1ce-310">有关波次步骤代码的详细信息，请参阅[波次步骤代码](wave-step-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-310">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-a-wave-label-layout"></a><span data-ttu-id="1b1ce-311">创建波次标签布局</span><span class="sxs-lookup"><span data-stu-id="1b1ce-311">Create a wave label layout</span></span>

1. <span data-ttu-id="1b1ce-312">转到 **仓库管理 \> 设置 \> 文档路线布局 \> 波次标签布局**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-312">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="1b1ce-313">创建一个具有以下设置的记录：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-313">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="1b1ce-314">**标签布局 ID**：*Carton*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-314">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="1b1ce-315">**描述**：*货箱 (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-315">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="1b1ce-316">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-316">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="1b1ce-317">在操作窗格上，选择 **波次标签行设置**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-317">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="1b1ce-318">**波次标签行设置** 页面将出现。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-318">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="1b1ce-319">在这里，您可以配置标签的动态部分。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-319">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="1b1ce-320">添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-320">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="1b1ce-321">**行 ID**：*WorkLine*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-321">**Row Id:** *WorkLine*</span></span>
    - <span data-ttu-id="1b1ce-322">**行表名称**：*WHSWorkLine*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-322">**Row table name:** *WHSWorkLine*</span></span>
    - <span data-ttu-id="1b1ce-323">**行开始位置**：*500*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-323">**Row start position:** *500*</span></span>

        <span data-ttu-id="1b1ce-324">此字段定义行在标签上开始的垂直位置。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-324">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="1b1ce-325">**行高度**：*-50*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-325">**Row height:** *-50*</span></span>

        <span data-ttu-id="1b1ce-326">此字段定义每行的高度。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-326">This field defines the height of each row.</span></span> <span data-ttu-id="1b1ce-327">行高度对于水平标签为正，对于垂直标签为负。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-327">The row height is positive for horizontal labels and negative for vertical labels.</span></span>

    - <span data-ttu-id="1b1ce-328">**每页行数**：*5*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-328">**Rows per page:** *5*</span></span>

        <span data-ttu-id="1b1ce-329">此字段定义可以在每个标签上打印的行数。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-329">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="1b1ce-330">此设置将为每个工作打印若干 ZPL 标签，每个页面最多可以保留五个工作行。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-330">This setup will print several ZPL labels per work, where each page can hold up to five work lines.</span></span> <span data-ttu-id="1b1ce-331">例如，如果为具有 12 行的集装箱打印标签，将打印三个标签。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-331">For example, if a label is printed for a container that has 12 lines, three labels will be printed.</span></span> <span data-ttu-id="1b1ce-332">如果要为每个领料行打印单独的标签，请将此值设置为 *1*。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-332">If you want to print a separate label for each pick line, set this value to *1*.</span></span>

1. <span data-ttu-id="1b1ce-333">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-333">Close the page.</span></span>
1. <span data-ttu-id="1b1ce-334">在操作窗格上，选择 **编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-334">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="1b1ce-335">在查询编辑器对话框的 **范围** 选项卡上，添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-335">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="1b1ce-336">**表**：*工作行*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-336">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="1b1ce-337">**派生表**：*工作行*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-337">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="1b1ce-338">**字段**：*工作类型*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-338">**Field:** *Work type*</span></span>
    - <span data-ttu-id="1b1ce-339">**条件**：*领料*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-339">**Criteria:** *Pick*</span></span>

1. <span data-ttu-id="1b1ce-340">如果您希望能够打印提单 ID，请在 **联接** 选项卡上，选择 **工作行** 表，然后将 **装运** 表与其联接。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-340">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="1b1ce-341">关闭查询编辑器对话框。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-341">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="1b1ce-342">**打印机文本布局** 快速选项卡有三个部分，您可以在其中编写打印机代码：**页眉部分**、**主体部分** 和 **页脚部分**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-342">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="1b1ce-343">在 **页眉部分** 的 **标签页眉** 字段中，输入所需页眉的代码。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-343">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="1b1ce-344">例如，如果您使用的是 Zebra 打印机，可以使用以下代码。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-344">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkTable.ContainerId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. <span data-ttu-id="1b1ce-345">在 **主体部分** 的 **标签主体** 字段中，输入所需主体的 ZPL 代码。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-345">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="1b1ce-346">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-346">Here is an example.</span></span>

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

1. <span data-ttu-id="1b1ce-347">在 **主体部分** 的 **标签页脚** 字段中，输入所需页脚的 ZPL 代码。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-347">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="1b1ce-348">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-348">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="1b1ce-349">此设置将打印每个标签的一个副本。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-349">This setup will print one copy of each label.</span></span> <span data-ttu-id="1b1ce-350">如果需要更多副本（例如，托盘每一面一个副本），请将页脚中 **\^PQn** 部分的 **n** 值设置为所需的副本数。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-350">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="1b1ce-351">例如，每个标签要打印四个副本，请指定 **\^PQ4**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-351">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

<span data-ttu-id="1b1ce-352">您的标签现在可以使用了。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-352">Your label is now ready to use.</span></span>

### <a name="create-a-wave-label-template"></a><span data-ttu-id="1b1ce-353">创建波次标签模板</span><span class="sxs-lookup"><span data-stu-id="1b1ce-353">Create a wave label template</span></span>

1. <span data-ttu-id="1b1ce-354">转到 **仓库管理 \> 设置 \> 文档路线布局 \> 波次标签模板**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-354">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="1b1ce-355">添加波次级别模板，并在页眉中设置以下值：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-355">Add a wave level template, and set the following values in the header:</span></span>

    - <span data-ttu-id="1b1ce-356">**标签模板名称**：*集装箱标签*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-356">**Label template name:** *Container labels*</span></span>
    - <span data-ttu-id="1b1ce-357">**描述**：*集装箱标签*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-357">**Description:** *Container labels*</span></span>
    - <span data-ttu-id="1b1ce-358">**波次步骤代码**：*PrintLabel*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-358">**Wave step code:** *PrintLabel*</span></span>
    - <span data-ttu-id="1b1ce-359">**仓库**：*63*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-359">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="1b1ce-360">在 **波次标签模板详细信息** 快速选项卡上，添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-360">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="1b1ce-361">**标签布局 ID**：*Container*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-361">**Label layout ID:** *Container*</span></span>
    - <span data-ttu-id="1b1ce-362">**打印机名称：** 选择适当的 ZPL 打印机。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-362">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="1b1ce-363">**运行查询**：*是*（此设置是可选的，但建议使用此设置以获得最佳性能。）</span><span class="sxs-lookup"><span data-stu-id="1b1ce-363">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="1b1ce-364">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-364">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="1b1ce-365">可选：如果要设置客户特定的标签设计，则必须创建查询来查找客户的帐户。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-365">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="1b1ce-366">在 **波次标签模板详细信息** 快速选项卡上，选择 **编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-366">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="1b1ce-367">然后，在查询编辑器对话框的 **范围** 选项卡上，添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-367">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="1b1ce-368">**表**：*装运*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-368">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="1b1ce-369">**派生表**：*装运*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-369">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="1b1ce-370">**字段**：*帐号*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-370">**Field:** *Account number*</span></span>
    - <span data-ttu-id="1b1ce-371">**条件：** 输入相关的客户帐号。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-371">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="1b1ce-372">完成后，选择 **确定** 关闭查询编辑器对话框。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-372">When you've finished, select **OK** to close the query editor dialog box.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="1b1ce-373">配置编号规则扩展</span><span class="sxs-lookup"><span data-stu-id="1b1ce-373">Configure number sequence extensions</span></span>

<span data-ttu-id="1b1ce-374">编号规则扩展控制特定编号规则的 GS1 符合性。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-374">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="1b1ce-375">此配置对于当前方案是可选的。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-375">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="1b1ce-376">有关详细信息和配置说明，请参阅[配置编号规则扩展](../warehousing/configure-number-sequence-extensions.md)。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-376">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="1b1ce-377">创建销售订单并将其下达到仓库</span><span class="sxs-lookup"><span data-stu-id="1b1ce-377">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="1b1ce-378">转到 **销售和营销 \> 销售订单 \> 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-378">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="1b1ce-379">创建具有以下设置的销售订单：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-379">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="1b1ce-380">**客户帐户**：*US-001*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-380">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="1b1ce-381">**仓库**：*63*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-381">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="1b1ce-382">添加五个销售订单行：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-382">Add five sales order lines:</span></span>

    - <span data-ttu-id="1b1ce-383">销售订单行 1：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-383">Sales order line 1:</span></span>

        - <span data-ttu-id="1b1ce-384">\**物料编号：\*\*\*A0001*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-384">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="1b1ce-385">**数量：** *10*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-385">**Quantity:** *10*</span></span>

    - <span data-ttu-id="1b1ce-386">销售订单行 2：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-386">Sales order line 2:</span></span>

        - <span data-ttu-id="1b1ce-387">\**物料编号：\*\*\*A0002*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-387">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="1b1ce-388">**数量：** *20*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-388">**Quantity:** *20*</span></span>

    - <span data-ttu-id="1b1ce-389">销售订单行 3：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-389">Sales order line 3:</span></span>

        - <span data-ttu-id="1b1ce-390">\**物料编号：\*\*\*L0006*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-390">**Item number:** *L0006*</span></span>
        - <span data-ttu-id="1b1ce-391">**数量：** *20*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-391">**Quantity:** *20*</span></span>

    - <span data-ttu-id="1b1ce-392">销售订单行 4：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-392">Sales order line 4:</span></span>

        - <span data-ttu-id="1b1ce-393">\**物料编号：\*\*\*L0100*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-393">**Item number:** *L0100*</span></span>
        - <span data-ttu-id="1b1ce-394">**数量：** *40*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-394">**Quantity:** *40*</span></span>

    - <span data-ttu-id="1b1ce-395">销售订单行 5：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-395">Sales order line 5:</span></span>

        - <span data-ttu-id="1b1ce-396">\**物料编号：\*\*\*L0101*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-396">**Item number:** *L0101*</span></span>
        - <span data-ttu-id="1b1ce-397">**数量：** *50*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-397">**Quantity:** *50*</span></span>

    > [!NOTE]
    > <span data-ttu-id="1b1ce-398">此处提供的物料和数量仅是示例。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-398">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="1b1ce-399">它们必须在指定的仓库中有存货。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-399">They must have stock in the specified warehouse.</span></span>

1. <span data-ttu-id="1b1ce-400">选择销售订单行 1。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-400">Select sales order line 1.</span></span> <span data-ttu-id="1b1ce-401">然后，在 **销售订单行** 部分的 **库存** 菜单中，选择 **预留**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-401">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="1b1ce-402">在 **预留** 页的操作窗格中，选择 **预留批次**，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-402">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="1b1ce-403">对每个其他销售订单行重复步骤 4 和 5。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-403">Repeat steps 4 and 5 for each additional sales order line.</span></span>
1. <span data-ttu-id="1b1ce-404">在“操作窗格”上的 **仓库** 选项卡上，选择 **发放到仓库**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-404">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="1b1ce-405">将发生以下事件：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-405">The following events occur:</span></span>

    - <span data-ttu-id="1b1ce-406">系统使用包含标签打印步骤的模板来处理创建的装运。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-406">The system processes the created shipment using the template that includes the label printing step.</span></span> <span data-ttu-id="1b1ce-407">标签布局将用于定义标签的格式，最终结果将是具有五个行的标签，此标签将在标签模板中选择的打印机上打印。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-407">The label layout will be used to define the format of the label, and the end result will be a label that has five lines and that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="1b1ce-408">将为装运生成新提单 ID。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-408">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="1b1ce-409">如果您配置了数字序列扩展，波次标签 ID 将采用 **SSCC-18** 数字格式。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-409">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="1b1ce-410">您可以转到 **仓库管理 \> 查询和报表 \> 波次标签历史记录**，重新打印这些波次标签。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-410">You can reprint these wave labels by going to **Warehouse management \> Inquiries and reports \> Wave label history**.</span></span>

## <a name="scenario-3-wave-label-printing-for-multi-tiered-labels"></a><span data-ttu-id="1b1ce-411">方案 3：为多层标签打印波次标签</span><span class="sxs-lookup"><span data-stu-id="1b1ce-411">Scenario 3: Wave label printing for multi-tiered labels</span></span>

<span data-ttu-id="1b1ce-412">此方案展示当仓储流程需要几层运输标签时如何使用波次标签打印功能。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-412">This scenario shows how to use the wave label printing functionality when the warehousing processes require several tiers of shipping labels.</span></span> <span data-ttu-id="1b1ce-413">例如，对于货箱和托盘，可能必须打印单独的标签，而对于整个装运，可能必须打印中断标签。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-413">For example, separate labels might have to be printed for cartons and pallets, and a break label might have to be printed for a whole shipment.</span></span> <span data-ttu-id="1b1ce-414">中断标签是一种独立标签，可用作标签卷和集装箱之间的分界，如装运 ID 标签和条形码标签，以便在打印标签后可以轻松进行分类。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-414">Break labels are a separate type of label that can be used as a divider between rolls and containers, such as labels for the shipment ID and a barcode, so that the labels can easily be sorted after they are printed.</span></span>

<span data-ttu-id="1b1ce-415">此方案的配置与方案 1 的配置之间的主要区别在于，除了启用了中断标签之外，还必须将多个波次标签类型与波次标签模板和单位序列组行关联。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-415">The main difference between the configuration of this scenario and the configuration of scenario 1, besides the fact that break labels are enabled, is that multiple wave label types must be associated with wave label templates and unit sequence group lines.</span></span> <span data-ttu-id="1b1ce-416">要完成此配置，请为此方案设置以下元素：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-416">To accomplish this configuration, you set up the following elements for this scenario:</span></span>

- <span data-ttu-id="1b1ce-417">**波次处理方法：** 您将波次标签方法标记为“可重复”，将其两次（或多次）添加到波次模板中，并设置不同的波次步骤代码。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-417">**Wave processing methods:** You will mark the wave label method as "repeatable," add it two (or more) times to the wave template, and set different wave step codes.</span></span>
- <span data-ttu-id="1b1ce-418">**波次标签模板：** 您将配置波次标签模板并将其链接到波次模板。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-418">**Wave label templates:** You will configure the wave label templates and link them to the wave template.</span></span> <span data-ttu-id="1b1ce-419">每个波次标签模板都有其自己的波次标签类型。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-419">Each wave label template has its own wave label type.</span></span>
- <span data-ttu-id="1b1ce-420">**波次标签布局：** 您将创建多个波次标签布局。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-420">**Wave label layouts:** You will create multiple wave label layouts.</span></span> <span data-ttu-id="1b1ce-421">标签的每个“层”将有一个单独的标签布局，并且还将有一个中断标签布局。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-421">There will be a separate label layout for each "tier" of labels, and there will also be a break label layout.</span></span>

<span data-ttu-id="1b1ce-422">此方案演示端到端流。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-422">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="1b1ce-423">提供演示数据</span><span class="sxs-lookup"><span data-stu-id="1b1ce-423">Make demo data available</span></span>

<span data-ttu-id="1b1ce-424">要采取此方案，必须安装演示数据，并且必须选择 **USMF** 法人。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-424">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-wave-process-method"></a><span data-ttu-id="1b1ce-425">设置波次处理方法</span><span class="sxs-lookup"><span data-stu-id="1b1ce-425">Set up a wave process method</span></span>

1. <span data-ttu-id="1b1ce-426">转到 **仓库管理 \> 设置 \> 波次 \> 波次处理方法**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-426">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="1b1ce-427">确认 **waveLabelPrinting** 在列表中。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-427">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="1b1ce-428">如果不在，请在操作窗格中选择 **重新生成方法** 添加该方法。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-428">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>
1. <span data-ttu-id="1b1ce-429">对于 **waveLabelPrinting** 方法，选中 **让方法可重复** 复选框。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-429">For the **waveLabelPrinting** method, select the **Make method repeatable** check box.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="1b1ce-430">设置波次模板</span><span class="sxs-lookup"><span data-stu-id="1b1ce-430">Set up a wave template</span></span>

1. <span data-ttu-id="1b1ce-431">转到 **仓库管理 \> 设置 \> 波次 \> 波次模板**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-431">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
2. <span data-ttu-id="1b1ce-432">选择模板，如 **62 装运默认**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-432">Select a template, such as **62 Shipping Default**.</span></span>
3. <span data-ttu-id="1b1ce-433">在 **方法** 快速选项卡上，将 **波次标签打印** 方法移至 **选定方法** 列。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-433">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
4. <span data-ttu-id="1b1ce-434">在 **选定方法** 列中，将 **波次步骤代码** 值（如 *Carton*）分配给 **波次标签打印** 方法。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-434">In the **Selected methods** column, assign a **Wave step code** value, such as *Carton*, to the **Wave label printing** method.</span></span> <span data-ttu-id="1b1ce-435">有关波次步骤代码的详细信息，请参阅[波次步骤代码](wave-step-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-435">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>
5. <span data-ttu-id="1b1ce-436">再次将 **波次标签打印** 方法移至 **选定方法** 列。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-436">Move the **Wave label printing** method to the **Selected methods** column a second time.</span></span>
6. <span data-ttu-id="1b1ce-437">在 **选定方法** 列中，将不同 **波次步骤代码** 值（如 *Pallet*）分配给第二个 **波次标签打印** 方法。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-437">In the **Selected methods** column, assign a different **Wave step code** value, such as *Pallet*, to the second **Wave label printing** method.</span></span> <span data-ttu-id="1b1ce-438">有关波次步骤代码的详细信息，请参阅[波次步骤代码](wave-step-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-438">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-three-wave-label-layouts"></a><span data-ttu-id="1b1ce-439">创建三个波次标签布局</span><span class="sxs-lookup"><span data-stu-id="1b1ce-439">Create three wave label layouts</span></span>

1. <span data-ttu-id="1b1ce-440">转到 **仓库管理 \> 设置 \> 文档路线布局 \> 波次标签布局**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-440">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="1b1ce-441">创建一个具有以下设置的记录：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-441">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="1b1ce-442">**标签布局 ID**：*Carton*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-442">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="1b1ce-443">**描述**：*货箱 (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-443">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="1b1ce-444">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-444">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="1b1ce-445">在操作窗格上，选择 **波次标签行设置**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-445">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="1b1ce-446">**波次标签行设置** 页面将出现。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-446">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="1b1ce-447">在这里，您可以配置标签的动态部分。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-447">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="1b1ce-448">添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-448">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="1b1ce-449">**行 ID**：*WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-449">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="1b1ce-450">**行表名称**：*WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-450">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="1b1ce-451">**行开始位置**：*0*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-451">**Row start position:** *0*</span></span>

        <span data-ttu-id="1b1ce-452">此字段定义行在标签上开始的垂直位置。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-452">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="1b1ce-453">**行高度**：*0*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-453">**Row height:** *0*</span></span>

        <span data-ttu-id="1b1ce-454">此字段根据 ZPL 标准定义每行的高度（以磅为单位）。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-454">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="1b1ce-455">行高度对于水平标签为正，对于垂直标签为负。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-455">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="1b1ce-456">在此示例中因为只有一行，所以您可以将此值设置为 *0*（零）。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-456">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="1b1ce-457">**每页行数**：*1*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-457">**Rows per page:** *1*</span></span>

        <span data-ttu-id="1b1ce-458">此字段定义可以在每个标签上打印的行数。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-458">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="1b1ce-459">使用此设置，将为波次标签表中的每个记录打印一个单独的 ZPL 标签。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-459">This setup will cause a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="1b1ce-460">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-460">Close the page.</span></span>
1. <span data-ttu-id="1b1ce-461">在操作窗格上，选择 **编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-461">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="1b1ce-462">在查询编辑器对话框的 **范围** 选项卡上，添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-462">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="1b1ce-463">**表**：*工作行*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-463">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="1b1ce-464">**派生表**：*工作行*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-464">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="1b1ce-465">**字段**：*工作类型*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-465">**Field:** *Work type*</span></span>
    - <span data-ttu-id="1b1ce-466">**条件**：*领料*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-466">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="1b1ce-467">此查询可确保在标签上仅打印领料类型的工作行，不打印放置类型的工作行。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-467">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="1b1ce-468">如果您希望能够打印提单 ID，请在 **联接** 选项卡上，选择 **工作行** 表，然后将 **装运** 表与其联接。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-468">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span> 
1. <span data-ttu-id="1b1ce-469">关闭查询编辑器对话框。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-469">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="1b1ce-470">**打印机文本布局** 快速选项卡有三个部分，您可以在其中编写打印机代码：**页眉部分**、**主体部分** 和 **页脚部分**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-470">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="1b1ce-471">在 **页眉部分** 的 **标签页眉** 字段中，输入所需页眉的代码。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-471">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="1b1ce-472">例如，如果您使用的是 Zebra 打印机，可以使用以下代码。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-472">For example, if you're using Zebra printers, you can use the following code.</span></span>


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

1. <span data-ttu-id="1b1ce-473">在 **主体部分** 的 **标签主体** 字段中，输入所需主体的 ZPL 代码。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-473">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="1b1ce-474">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-474">Here is an example.</span></span>

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

1. <span data-ttu-id="1b1ce-475">在 **主体部分** 的 **标签页脚** 字段中，输入所需页脚的 ZPL 代码。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-475">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="1b1ce-476">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-476">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="1b1ce-477">此设置将打印每个标签的一个副本。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-477">This setup will print one copy of each label.</span></span> <span data-ttu-id="1b1ce-478">如果需要更多副本（例如，托盘每一面一个副本），请将页脚中 **\^PQn** 部分的 **n** 值设置为所需的副本数。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-478">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="1b1ce-479">例如，每个标签要打印四个副本，请指定 **\^PQ4**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-479">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

1. <span data-ttu-id="1b1ce-480">第一个标签现在可以使用了。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-480">The first label is now ready to use.</span></span>
1. <span data-ttu-id="1b1ce-481">创建具有以下设置的第二个布局记录：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-481">Create a second layout record that has the following settings:</span></span>

    - <span data-ttu-id="1b1ce-482">**标签布局 ID**：*Pallet*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-482">**Label layout ID:** *Pallet*</span></span>
    - <span data-ttu-id="1b1ce-483">**描述**：*托盘*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-483">**Description:** *Pallet*</span></span>

1. <span data-ttu-id="1b1ce-484">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-484">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="1b1ce-485">在操作窗格上，选择 **波次标签行设置**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-485">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="1b1ce-486">**波次标签行设置** 页面将出现。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-486">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="1b1ce-487">在这里，您可以配置标签的动态部分。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-487">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="1b1ce-488">添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-488">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="1b1ce-489">**行 ID**：*WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-489">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="1b1ce-490">**行表名称**：*WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-490">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="1b1ce-491">**行开始位置**：*0*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-491">**Row start position:** *0*</span></span>

        <span data-ttu-id="1b1ce-492">此字段定义行在标签上开始的垂直位置。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-492">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="1b1ce-493">**行高度**：*0*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-493">**Row height:** *0*</span></span>

        <span data-ttu-id="1b1ce-494">此字段根据 ZPL 标准定义每行的高度（以磅为单位）。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-494">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="1b1ce-495">行高度对于水平标签为正，对于垂直标签为负。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-495">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="1b1ce-496">在此示例中因为只有一行，所以您可以将此值设置为 *0*（零）。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-496">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="1b1ce-497">**每页行数**：*1*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-497">**Rows per page:** *1*</span></span>

        <span data-ttu-id="1b1ce-498">此字段定义可以在每个标签上打印的行数。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-498">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="1b1ce-499">使用此设置，将为波次标签表中的每个记录打印一个单独的 ZPL 标签。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-499">This setup causes a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="1b1ce-500">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-500">Close the page.</span></span>
1. <span data-ttu-id="1b1ce-501">在操作窗格上，选择 **编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-501">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="1b1ce-502">在查询编辑器对话框的 **范围** 选项卡上，添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-502">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="1b1ce-503">**表**：*工作行*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-503">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="1b1ce-504">**派生表**：*工作行*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-504">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="1b1ce-505">**字段**：*工作类型*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-505">**Field:** *Work type*</span></span>
    - <span data-ttu-id="1b1ce-506">**条件**：*领料*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-506">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="1b1ce-507">此查询可确保在标签上仅打印领料类型的工作行，不打印放置类型的工作行。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-507">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="1b1ce-508">如果您希望能够打印提单 ID，请在 **联接** 选项卡上，选择 **工作行** 表，然后将 **装运** 表与其联接。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-508">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="1b1ce-509">关闭查询编辑器对话框。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-509">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="1b1ce-510">**打印机文本布局** 快速选项卡有三个部分，您可以在其中编写打印机代码：**页眉部分**、**主体部分** 和 **页脚部分**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-510">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="1b1ce-511">在 **页眉部分** 的 **标签页眉** 字段中，输入所需页眉的代码。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-511">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="1b1ce-512">例如，如果您使用的是 Zebra 打印机，可以使用以下代码。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-512">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWaveLabel.WaveLabelId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. <span data-ttu-id="1b1ce-513">在 **主体部分** 的 **标签主体** 字段中，输入所需主体的 ZPL 代码。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-513">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="1b1ce-514">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-514">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWaveLabel.LabelItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWaveLabel.QtyWork$ ^FS
    </Row>
    ```

1. <span data-ttu-id="1b1ce-515">在 **主体部分** 的 **标签页脚** 字段中，输入所需页脚的 ZPL 代码。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-515">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="1b1ce-516">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-516">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="1b1ce-517">此设置将打印每个标签的一个副本。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-517">This setup will print one copy of each label.</span></span> <span data-ttu-id="1b1ce-518">如果需要更多副本（例如，托盘每一面一个副本），请将页脚中 **\^PQn** 部分的 **n** 值设置为所需的副本数。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-518">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="1b1ce-519">例如，每个标签要打印四个副本，请指定 **\^PQ4**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-519">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

1. <span data-ttu-id="1b1ce-520">第二个标签现在可以使用了。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-520">The second label is now ready to use.</span></span>
1. <span data-ttu-id="1b1ce-521">创建具有以下设置的第三个布局记录：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-521">Create a third layout record that has the following settings:</span></span>

    - <span data-ttu-id="1b1ce-522">**标签布局 ID**：*Break*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-522">**Label layout ID:** *Break*</span></span>
    - <span data-ttu-id="1b1ce-523">**描述**：*中断标签*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-523">**Description:** *Break label*</span></span>

1. <span data-ttu-id="1b1ce-524">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-524">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="1b1ce-525">**打印机文本布局** 快速选项卡有三个部分，您可以在其中编写打印机代码：**页眉部分**、**主体部分** 和 **页脚部分**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-525">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="1b1ce-526">在 **页眉部分** 的 **标签页眉** 字段中，输入所需页眉的 ZPL 代码。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-526">In the **Header section** section, in the **Label header** field, enter ZPL code for the required header.</span></span> <span data-ttu-id="1b1ce-527">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-527">Here is an example.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ```

1. <span data-ttu-id="1b1ce-528">这次，不需要人工。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-528">This time, no body is required.</span></span> <span data-ttu-id="1b1ce-529">因此，只需在 **页脚部分** 部分输入所需文本。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-529">Therefore, just enter the required text in the **Footer section** section.</span></span> <span data-ttu-id="1b1ce-530">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-530">Here is an example.</span></span>

    ```plaintext
    ^XZ
    ```

    <span data-ttu-id="1b1ce-531">第三个标签现在可以使用了。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-531">The third label is now ready to use.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1b1ce-532">第三个标签是中断标签，将用作标签卷之间的分界。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-532">This third label is a break label that will be used as a divider between label rolls.</span></span>

### <a name="create-two-wave-label-types"></a><span data-ttu-id="1b1ce-533">创建两个波次标签类型</span><span class="sxs-lookup"><span data-stu-id="1b1ce-533">Create two wave label types</span></span>

1. <span data-ttu-id="1b1ce-534">转到 **仓库管理 \> 设置 \> 文档路线布局 \> 波次标签类型**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-534">Go to **Warehouse management \> Setup \> Document routing \> Wave label types**.</span></span>
1. <span data-ttu-id="1b1ce-535">创建一个具有以下设置的记录：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-535">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="1b1ce-536">**标签类型**：*货箱*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-536">**Label type:** *Carton*</span></span>
    - <span data-ttu-id="1b1ce-537">**描述**：*货箱*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-537">**Description:** *Carton*</span></span>

1. <span data-ttu-id="1b1ce-538">创建具有以下设置的第二个记录：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-538">Create a second record that has the following settings:</span></span>

    - <span data-ttu-id="1b1ce-539">**标签类型**：*托盘*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-539">**Label type:** *Pallet*</span></span>
    - <span data-ttu-id="1b1ce-540">**描述**：*托盘*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-540">**Description:** *Pallet*</span></span>

### <a name="set-up-unit-sequence-groups"></a><span data-ttu-id="1b1ce-541">设置单位序列组</span><span class="sxs-lookup"><span data-stu-id="1b1ce-541">Set up unit sequence groups</span></span>

1. <span data-ttu-id="1b1ce-542">转到 **仓库管理 \> 设置 \> 仓库 \> 单位序列组**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-542">Go to **Warehouse management \> Setup \> Warehouse \> Unit sequence groups**.</span></span>
1. <span data-ttu-id="1b1ce-543">选择或创建一个 **Ea Box PL** 组。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-543">Select or create an **Ea Box PL** group.</span></span>
1. <span data-ttu-id="1b1ce-544">对于 **箱** 行，将 **波次级别类型** 字段设置为 *货箱*。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-544">For the **Box** line, set the **Wave level type** field to *Carton*.</span></span>
1. <span data-ttu-id="1b1ce-545">对于 **托盘** 行，将 **波次级别类型** 字段设置为 *托盘*。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-545">For the **PL** line, set the **Wave level type** field to *Pallet*.</span></span>

### <a name="create-wave-label-templates"></a><span data-ttu-id="1b1ce-546">创建波次标签模板</span><span class="sxs-lookup"><span data-stu-id="1b1ce-546">Create wave label templates</span></span>

1. <span data-ttu-id="1b1ce-547">转到 **仓库管理 \> 设置 \> 文档路线布局 \> 波次标签模板**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-547">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="1b1ce-548">创建具有以下设置的标签模板：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-548">Create a label template that has the following settings:</span></span>

    - <span data-ttu-id="1b1ce-549">**标签模板名称**：*货箱标签*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-549">**Label template name:** *Carton labels*</span></span>
    - <span data-ttu-id="1b1ce-550">**描述**：*货箱标签*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-550">**Description:** *Carton labels*</span></span>
    - <span data-ttu-id="1b1ce-551">**波次步骤代码**：*Carton*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-551">**Wave step code:** *Carton*</span></span>
    - <span data-ttu-id="1b1ce-552">**仓库**：*62*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-552">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="1b1ce-553">在 **常规** 快速选项卡上，在 **波次标签类型** 字段中，选择一个值，如 *货箱*。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-553">On the **General** FastTab, in the **Wave label type** field, select a value, such as *Carton*.</span></span>
1. <span data-ttu-id="1b1ce-554">在 **波次标签模板详细信息** 快速选项卡上，添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-554">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="1b1ce-555">**标签布局 ID**：*Carton*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-555">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="1b1ce-556">**打印机名称：** 选择适当的 ZPL 打印机。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-556">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="1b1ce-557">**运行查询**：*是*（此设置是可选的，但建议使用此设置以获得最佳性能。）</span><span class="sxs-lookup"><span data-stu-id="1b1ce-557">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="1b1ce-558">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-558">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="1b1ce-559">可选：如果要设置客户特定的标签设计，则必须创建查询来查找客户的帐户。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-559">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="1b1ce-560">在 **波次标签模板详细信息** 快速选项卡上，选择 **编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-560">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="1b1ce-561">然后，在查询编辑器对话框的 **范围** 选项卡上，添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-561">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="1b1ce-562">**表**：*装运*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-562">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="1b1ce-563">**派生表**：*装运*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-563">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="1b1ce-564">**字段**：*帐号*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-564">**Field:** *Account number*</span></span>
    - <span data-ttu-id="1b1ce-565">**条件：** 输入相关的客户帐号。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-565">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="1b1ce-566">完成后，选择 **确定** 关闭查询编辑器对话框。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-566">When you've finished, select **OK** to close the query editor dialog box.</span></span>

1. <span data-ttu-id="1b1ce-567">在操作窗格上，选择 **编辑查询** 打开整个标签模板的查询编辑器对话框。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-567">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="1b1ce-568">在查询编辑器对话框的 **排序** 选项卡上，添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-568">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="1b1ce-569">**表**：*工作行*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-569">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="1b1ce-570">**派生表**：*工作行*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-570">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="1b1ce-571">**字段**：*参考负荷行 ID（记录 ID）*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-571">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="1b1ce-572">**搜索方向**：*升序*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-572">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="1b1ce-573">再添加一个具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-573">Add a second row that has the following settings:</span></span>

    - <span data-ttu-id="1b1ce-574">**表**：*工作行*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-574">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="1b1ce-575">**派生表**：*工作行*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-575">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="1b1ce-576">**字段**：*装运 ID*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-576">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="1b1ce-577">**搜索方向**：*升序*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-577">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="1b1ce-578">选择 **确定** 关闭查询编辑器对话框。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-578">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="1b1ce-579">一个消息框将提示您确认分组重置操作。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-579">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="1b1ce-580">选择 **是** 继续。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-580">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="1b1ce-581">在操作窗格上，选择 **波次标签模板组**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-581">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="1b1ce-582">在 **波次标签模板组** 对话框中，对于 **参考字段名称** 字段设置为 *装运 ID* 的行，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-582">In the **Wave label template group** dialog box, for the row where the **Reference field name** field is set to *Shipment ID*, set the following values:</span></span>

    - <span data-ttu-id="1b1ce-583">**打印中断标签：** 选择此复选框。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-583">**Print break label:** Select this check box.</span></span>
    - <span data-ttu-id="1b1ce-584">**标签布局 ID：** 选择一个中断标签。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-584">**Label layout ID:** Select a break label.</span></span> <span data-ttu-id="1b1ce-585">（例如，选择您在此方案中先前创建的 *中断* 标签布局。）</span><span class="sxs-lookup"><span data-stu-id="1b1ce-585">(For example, select the *Break* label layout that you created earlier in this scenario.)</span></span>
    - <span data-ttu-id="1b1ce-586">**打印机名称：** 选择中断标签的打印机。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-586">**Printer name:** Select the printer for the break label.</span></span> <span data-ttu-id="1b1ce-587">（通常，出于分割标签券的目的，您应该选择在 **波次标签模板详细信息** 上选择的同一台打印机。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-587">(Typically, for the purpose of splitting label rolls, you should select the same printer that is selected on the **Wave label template details** FastTab.</span></span> <span data-ttu-id="1b1ce-588">但也可能是其他情况。）</span><span class="sxs-lookup"><span data-stu-id="1b1ce-588">However, other scenarios are possible.)</span></span>

1. <span data-ttu-id="1b1ce-589">对于将 **参考字段名称** 字段设置为 *参考负荷行 ID* 的行，选择 **标签生成 ID** 复选框。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-589">For the row where the **Reference field name** field is set to *Reference load line id*, select the **Label build ID** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1b1ce-590">无论工作分组设置如何，此设置都会在整个波次中为每个负荷行创建一个标签序列（“货箱 1/X”）。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-590">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="1b1ce-591">此标签序列可以打印在标签布局上。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-591">This label sequence can be printed on a label layout.</span></span> <span data-ttu-id="1b1ce-592">此外，不同装运的标签将由选定的中断标签分隔。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-592">Additionally, labels for different shipments will be separated by the selected break label.</span></span>

1. <span data-ttu-id="1b1ce-593">选择 **确定** 关闭 **波次标签模板组** 对话框。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-593">Select **OK** to close the **Wave label template group** dialog box.</span></span>
1. <span data-ttu-id="1b1ce-594">再创建一个具有以下设置的标签模板：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-594">Create a second label template that has the following settings:</span></span>

    - <span data-ttu-id="1b1ce-595">**标签模板名称**：*托盘标签*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-595">**Label template name:** *Pallet labels*</span></span>
    - <span data-ttu-id="1b1ce-596">**描述**：*托盘标签*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-596">**Description:** *Pallet labels*</span></span>
    - <span data-ttu-id="1b1ce-597">**波次步骤代码**：*Pallet*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-597">**Wave step code:** *Pallet*</span></span>
    - <span data-ttu-id="1b1ce-598">**仓库**：*62*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-598">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="1b1ce-599">在 **常规** 快速选项卡上，在 **波次标签类型** 字段中，选择一个值，如 *托盘*。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-599">On the **General** FastTab, in the **Wave label type** field, select a value, such as *Pallet*.</span></span>
1. <span data-ttu-id="1b1ce-600">在 **波次标签模板详细信息** 快速选项卡上，添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-600">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="1b1ce-601">**标签布局 ID**：*Pallet*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-601">**Label layout ID:** *Pallet*</span></span>
    - <span data-ttu-id="1b1ce-602">**打印机名称：** 选择适当的 ZPL 打印机。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-602">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="1b1ce-603">**运行查询**：*是*（此设置是可选的，但建议使用此设置以获得最佳性能。）</span><span class="sxs-lookup"><span data-stu-id="1b1ce-603">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="1b1ce-604">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-604">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="1b1ce-605">可选：如果要设置客户特定的标签设计，则必须创建查询来查找客户的帐户。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-605">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="1b1ce-606">在 **波次标签模板详细信息** 快速选项卡上，选择 **编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-606">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="1b1ce-607">然后，在查询编辑器对话框的 **范围** 选项卡上，添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-607">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="1b1ce-608">**表**：*装运*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-608">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="1b1ce-609">**派生表**：*装运*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-609">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="1b1ce-610">**字段**：*帐号*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-610">**Field:** *Account number*</span></span>
    - <span data-ttu-id="1b1ce-611">**条件：** 输入相关的客户帐号。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-611">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="1b1ce-612">完成后，选择 **确定** 关闭查询编辑器对话框。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-612">When you've finished, select **OK** to close the query editor dialog box.</span></span> 

1. <span data-ttu-id="1b1ce-613">在操作窗格上，选择 **编辑查询** 打开整个标签模板的查询编辑器对话框。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-613">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="1b1ce-614">在查询编辑器对话框的 **排序** 选项卡上，添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-614">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="1b1ce-615">**表**：*工作行*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-615">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="1b1ce-616">**派生表**：*工作行*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-616">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="1b1ce-617">**字段**：*参考负荷行 ID（记录 ID）*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-617">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="1b1ce-618">**搜索方向**：*升序*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-618">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="1b1ce-619">再添加一个具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-619">Add a second row that has the following settings:</span></span>

    - <span data-ttu-id="1b1ce-620">**表**：*工作行*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-620">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="1b1ce-621">**派生表**：*工作行*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-621">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="1b1ce-622">**字段**：*装运 ID*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-622">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="1b1ce-623">**搜索方向**：*升序*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-623">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="1b1ce-624">选择 **确定** 关闭查询编辑器对话框。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-624">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="1b1ce-625">一个消息框将提示您确认分组重置操作。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-625">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="1b1ce-626">选择 **是** 继续。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-626">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="1b1ce-627">在操作窗格上，选择 **波次标签模板组**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-627">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="1b1ce-628">在 **波次标签模板组** 对话框中，对于 **参考字段名称** 字段设置为 *装运 ID* 的行，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-628">In the **Wave label template group** dialog box, for the row where the **Reference field name** field is set to *Shipment ID*, set the following values:</span></span>

    - <span data-ttu-id="1b1ce-629">**打印中断标签：** 选择此复选框。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-629">**Print break label:** Select this check box.</span></span>
    - <span data-ttu-id="1b1ce-630">**标签布局 ID：** 选择一个中断标签。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-630">**Label layout ID:** Select a break label.</span></span> <span data-ttu-id="1b1ce-631">（例如，选择您在此方案中先前创建的 *中断* 标签布局。）</span><span class="sxs-lookup"><span data-stu-id="1b1ce-631">(For example, select the *Break* label layout that you created earlier in this scenario.)</span></span>
    - <span data-ttu-id="1b1ce-632">**打印机名称：** 选择中断标签的打印机。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-632">**Printer name:** Select the printer for the break label.</span></span> <span data-ttu-id="1b1ce-633">（通常，出于分割标签券的目的，您应该选择在 **波次标签模板详细信息** 上选择的同一台打印机。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-633">(Typically, for the purpose of splitting label rolls, you should select the same printer that is selected on the **Wave label template details** FastTab.</span></span> <span data-ttu-id="1b1ce-634">但也可能是其他情况。）</span><span class="sxs-lookup"><span data-stu-id="1b1ce-634">However, other scenarios are possible.)</span></span>

1. <span data-ttu-id="1b1ce-635">对于将 **参考字段名称** 字段设置为 *参考负荷行 ID* 的行，选择 **标签生成 ID** 复选框。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-635">For the row where the **Reference field name** field is set to *Reference load line id*, select the **Label build ID** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1b1ce-636">无论工作分组设置如何，此设置都会在整个波次中为每个负荷行创建一个标签序列（“货箱 1/X”）。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-636">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="1b1ce-637">此标签序列可以打印在标签布局上。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-637">This label sequence can be printed on a label layout.</span></span> <span data-ttu-id="1b1ce-638">此外，不同装运的标签将由选定的中断标签分隔。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-638">Additionally, labels for different shipments will be separated by the selected break label.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="1b1ce-639">配置编号规则扩展</span><span class="sxs-lookup"><span data-stu-id="1b1ce-639">Configure number sequence extensions</span></span>

<span data-ttu-id="1b1ce-640">编号规则扩展控制特定编号规则的 GS1 符合性。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-640">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="1b1ce-641">此配置对于当前方案是可选的。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-641">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="1b1ce-642">有关详细信息和配置说明，请参阅[配置编号规则扩展](../warehousing/configure-number-sequence-extensions.md)。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-642">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="1b1ce-643">创建销售订单并将其下达到仓库</span><span class="sxs-lookup"><span data-stu-id="1b1ce-643">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="1b1ce-644">转到 **销售和营销 \> 销售订单 \> 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-644">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="1b1ce-645">创建具有以下设置的销售订单：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-645">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="1b1ce-646">**客户帐户**：*US-001*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-646">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="1b1ce-647">**仓库**：*62*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-647">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="1b1ce-648">添加两个销售订单行：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-648">Add two sales order lines:</span></span>

    - <span data-ttu-id="1b1ce-649">销售订单行 1：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-649">Sales order line 1:</span></span>

        - <span data-ttu-id="1b1ce-650">\**物料编号：\*\*\*A0001*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-650">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="1b1ce-651">**数量：** *9024*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-651">**Quantity:** *9024*</span></span>
        - <span data-ttu-id="1b1ce-652">**单位**：*个* (9024 个 = 376 箱 = 47 PL)</span><span class="sxs-lookup"><span data-stu-id="1b1ce-652">**Unit:** *ea* (9024 ea = 376 Box = 47 PL)</span></span>

    - <span data-ttu-id="1b1ce-653">销售订单行 2：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-653">Sales order line 2:</span></span>

        - <span data-ttu-id="1b1ce-654">\**物料编号：\*\*\*A0002*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-654">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="1b1ce-655">**数量：** *9016*</span><span class="sxs-lookup"><span data-stu-id="1b1ce-655">**Quantity:** *9016*</span></span>
        - <span data-ttu-id="1b1ce-656">**单位**：*个* (9016 个 = 322 箱 = 46 PL)</span><span class="sxs-lookup"><span data-stu-id="1b1ce-656">**Unit:** *ea* (9016 ea = 322 Box = 46 PL)</span></span>

    > [!NOTE]
    > <span data-ttu-id="1b1ce-657">此处提供的物料和数量仅是示例。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-657">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="1b1ce-658">它们必须使用您先前定义的单位序列组，必须为它们定义从 *个* 到 *箱* 再到 *PL* 的适当单位转换，并且它们在仓库 *62* 中必须有存货。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-658">They must use the unit sequence group that you defined earlier, appropriate unit conversions from *ea* to *Box* to *PL* must be defined for them, and they must have stock in warehouse *62*.</span></span> <span data-ttu-id="1b1ce-659">有关详细信息，请参阅[度量单位和库存策略](unit-measure-stocking-policies.md)。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-659">For more information, see [Unit of measure and stocking policies](unit-measure-stocking-policies.md).</span></span>

1. <span data-ttu-id="1b1ce-660">选择销售订单行 1。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-660">Select sales order line 1.</span></span> <span data-ttu-id="1b1ce-661">然后，在 **销售订单行** 部分的 **库存** 菜单中，选择 **预留**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-661">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="1b1ce-662">在 **预留** 页的操作窗格中，选择 **预留批次**，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-662">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="1b1ce-663">对销售订单行 2 重复步骤 4 和 5。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-663">Repeat steps 4 and 5 for sales order line 2.</span></span>
1. <span data-ttu-id="1b1ce-664">在“操作窗格”上的 **仓库** 选项卡上，选择 **发放到仓库**。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-664">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="1b1ce-665">将发生以下事件：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-665">The following events occur:</span></span> 

    - <span data-ttu-id="1b1ce-666">系统使用包含标签打印步骤的模板来处理创建的装运。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-666">The system processes the created shipment by using the template that includes the label printing step.</span></span> <span data-ttu-id="1b1ce-667">标签布局将用于定义标签的格式，结果将是在标签模板中选择的打印机上打印的标签。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-667">The label layout will be used to define the format of the label, and the result will be a label that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="1b1ce-668">波次标签将生成并打印。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-668">Wave labels are generated and printed.</span></span> <span data-ttu-id="1b1ce-669">标签数量将等于货箱数量（在此示例中，行 1 是 376 箱标签，行 2 是 322 箱标签，行 1 是 47 PL 标签，行 2 是 47 PL 标签，以及两个具有装运 ID 的中断标签）。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-669">The number of labels will equal the number of cartons (in this example, 376 Box labels for line 1, 322 Box labels for line 2, 47 PL labels for line 1, 47 PL labels for line 2, and two break labels that have the shipment ID).</span></span>
    - <span data-ttu-id="1b1ce-670">将为装运生成新提单 ID。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-670">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="1b1ce-671">如果您配置了数字序列扩展，波次标签 ID 将采用 **SSCC-18** 数字格式。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-671">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="1b1ce-672">您可以从以下页面查看和重新打印波次标签：</span><span class="sxs-lookup"><span data-stu-id="1b1ce-672">You can view and reprint wave labels from the following pages:</span></span>

- <span data-ttu-id="1b1ce-673">所有装运 \> 装运详细信息</span><span class="sxs-lookup"><span data-stu-id="1b1ce-673">All shipments \> Shipment details</span></span>
- <span data-ttu-id="1b1ce-674">所有负荷 \> 负荷详细信息</span><span class="sxs-lookup"><span data-stu-id="1b1ce-674">All loads \> Load details</span></span>
- <span data-ttu-id="1b1ce-675">所有波次</span><span class="sxs-lookup"><span data-stu-id="1b1ce-675">All waves</span></span>
- <span data-ttu-id="1b1ce-676">波次标签</span><span class="sxs-lookup"><span data-stu-id="1b1ce-676">Wave labels</span></span>
- <span data-ttu-id="1b1ce-677">波次标签历史记录</span><span class="sxs-lookup"><span data-stu-id="1b1ce-677">Wave label history</span></span>

<span data-ttu-id="1b1ce-678">对于这些页面中的大多数页面，可以通过在“操作窗格”的 **装运** 选项卡上的 **相关信息** 组中选择 **波次标签** 来查找相关功能。</span><span class="sxs-lookup"><span data-stu-id="1b1ce-678">For most of these pages, you can find the relevant function by selecting **Wave labels** in the **Related information** group on the **Shipments** tab of the Action Pane.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1b1ce-679">其他资源</span><span class="sxs-lookup"><span data-stu-id="1b1ce-679">Additional resources</span></span>

- [<span data-ttu-id="1b1ce-680">重新打印波次标签并使之无效</span><span class="sxs-lookup"><span data-stu-id="1b1ce-680">Reprint and void wave labels</span></span>](reprint-and-void-wave-labels.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]