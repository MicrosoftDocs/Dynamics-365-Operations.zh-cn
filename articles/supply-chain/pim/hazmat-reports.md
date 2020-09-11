---
title: 危险物料查询和报表
description: 本主题说明如何处理与危险物料有关的各个报表。 这些报表中有很多是必需的，用来帮助您在装运和存储过程中始终遵守各项危险物料法规。
author: dasani-madipalli
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: a67c8d0795d31464d900eb5aa82a6d93b689950c
ms.sourcegitcommit: c009ec75f53872272f11c92a1ce81a391e3845a2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/18/2020
ms.locfileid: "3699588"
---
# <a name="hazardous-materials-inquiries-and-reports"></a><span data-ttu-id="d02f7-104">危险物料查询和报表</span><span class="sxs-lookup"><span data-stu-id="d02f7-104">Hazardous materials inquiries and reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d02f7-105">Microsoft Dynamics 365 Supply Chain Management 提供与危险物料有关的各个报表。</span><span class="sxs-lookup"><span data-stu-id="d02f7-105">Microsoft Dynamics 365 Supply Chain Management provides various reports that are related to hazardous materials.</span></span> <span data-ttu-id="d02f7-106">这些报表中有很多是必需的，用来帮助您在装运和存储过程中始终遵守各项危险物料法规。</span><span class="sxs-lookup"><span data-stu-id="d02f7-106">Many of these reports are required so that you remain compliant with various hazardous material regulations during shipping and storage.</span></span>

<span data-ttu-id="d02f7-107">除**多模式危险货物**报表外，所有这些报表均使用为装运定义的交货方式来查找应用于打印物料装运文本的法规。</span><span class="sxs-lookup"><span data-stu-id="d02f7-107">All these reports, except the **Multimodal dangerous goods** report, use the mode of delivery that is defined for the shipment to find the regulation that should be used to print the shipping text for items.</span></span> <span data-ttu-id="d02f7-108">交货方式与装运承运人和承运人服务关联。</span><span class="sxs-lookup"><span data-stu-id="d02f7-108">The mode of delivery is associated with the shipping carrier and the carrier service.</span></span> <span data-ttu-id="d02f7-109">因此，您必须设置装运承运人和承运人服务，并将它们链接到交货方式。</span><span class="sxs-lookup"><span data-stu-id="d02f7-109">Therefore, you must set up a shipping carrier and carrier service, and link them to a mode of delivery.</span></span> <span data-ttu-id="d02f7-110">交货方式与危险物料法规有关。</span><span class="sxs-lookup"><span data-stu-id="d02f7-110">The mode of delivery is related to the hazardous materials regulation.</span></span>

<span data-ttu-id="d02f7-111">下图显示了系统生成危险物料报表时发生的活动序列。</span><span class="sxs-lookup"><span data-stu-id="d02f7-111">The following illustration shows the sequence of activities that occur when the system generates hazardous materials reports.</span></span>

<span data-ttu-id="d02f7-112">![危险物料报表的活动序列](media/hazmat-report-sequence.png "危险物料报表的活动序列")</span><span class="sxs-lookup"><span data-stu-id="d02f7-112">![Sequence of activities for hazardous materials reports](media/hazmat-report-sequence.png "Sequence of activities for hazardous materials reports")</span></span>

## <a name="set-up-hazardous-materials-reporting"></a><a name="set-up"></a><span data-ttu-id="d02f7-113">设置危险物料报告</span><span class="sxs-lookup"><span data-stu-id="d02f7-113">Set up hazardous materials reporting</span></span>

<span data-ttu-id="d02f7-114">通常，如果装运包含危险物料的物料，必须生成特定报表以帮助保持安全和遵守危险物料法规。</span><span class="sxs-lookup"><span data-stu-id="d02f7-114">Usually, if you ship items that contain hazardous materials, you must generate specific reports to help preserve safety and comply with hazardous materials regulations.</span></span> <span data-ttu-id="d02f7-115">要设置报表，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="d02f7-115">To set up your reports, follow these steps.</span></span>

1. <span data-ttu-id="d02f7-116">转到**仓库管理 \> 设置 \> 仓库管理参数**。</span><span class="sxs-lookup"><span data-stu-id="d02f7-116">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
2. <span data-ttu-id="d02f7-117">打开**报表**选项卡。在**危险物料报表参数**快速选项卡上，设置以下字段。</span><span class="sxs-lookup"><span data-stu-id="d02f7-117">Open the **Reports** tab. On the **Hazardous materials report parameter** FastTab, set the following fields.</span></span>

    | <span data-ttu-id="d02f7-118">部分</span><span class="sxs-lookup"><span data-stu-id="d02f7-118">Section</span></span> | <span data-ttu-id="d02f7-119">字段</span><span class="sxs-lookup"><span data-stu-id="d02f7-119">Field</span></span> | <span data-ttu-id="d02f7-120">说明</span><span class="sxs-lookup"><span data-stu-id="d02f7-120">Description</span></span> |
    |---|---|---|
    | <span data-ttu-id="d02f7-121">多模式危险货物</span><span class="sxs-lookup"><span data-stu-id="d02f7-121">Multimodal Dangerous Goods</span></span> | <span data-ttu-id="d02f7-122">监管代码</span><span class="sxs-lookup"><span data-stu-id="d02f7-122">Regulation code</span></span> | <span data-ttu-id="d02f7-123">选择生成**多模式危险货物**报表时应使用的法规。</span><span class="sxs-lookup"><span data-stu-id="d02f7-123">Select the regulation that should be used when a **Multimodal dangerous goods** report is generated.</span></span> |
    | <span data-ttu-id="d02f7-124">危险物料存货限制</span><span class="sxs-lookup"><span data-stu-id="d02f7-124">Hazardous Material stock limits</span></span> | <span data-ttu-id="d02f7-125">监管代码</span><span class="sxs-lookup"><span data-stu-id="d02f7-125">Regulation code</span></span> | <span data-ttu-id="d02f7-126">选择评估存货限制时应使用的法规。</span><span class="sxs-lookup"><span data-stu-id="d02f7-126">Select the regulation that should be used when stock limits are evaluated.</span></span> |
    | <span data-ttu-id="d02f7-127">陆运商品运输</span><span class="sxs-lookup"><span data-stu-id="d02f7-127">Carriage of merchandise by road</span></span> | <span data-ttu-id="d02f7-128">CMR 组产品</span><span class="sxs-lookup"><span data-stu-id="d02f7-128">CMR group product</span></span> | <span data-ttu-id="d02f7-129">CMR 表示“致癌、致突变、对生殖系统有毒性物质”。</span><span class="sxs-lookup"><span data-stu-id="d02f7-129">CMR stands for "carcinogenic, mutagenic, and reprotoxic substances."</span></span> <span data-ttu-id="d02f7-130">将此选项设置为**是**将配置系统来打印与处理这些物质有关的特定警告和消息。</span><span class="sxs-lookup"><span data-stu-id="d02f7-130">Set this option to **Yes** to configure the system to print specific warnings and messages that are related to the handling of these substances.</span></span> |
    | <span data-ttu-id="d02f7-131">陆运商品运输</span><span class="sxs-lookup"><span data-stu-id="d02f7-131">Carriage of merchandise by road</span></span> | <span data-ttu-id="d02f7-132">危险物料组描述</span><span class="sxs-lookup"><span data-stu-id="d02f7-132">Hazardous material group description</span></span> | <span data-ttu-id="d02f7-133">输入与 CMR 和陆运商品运输有关的特定警告的文本。</span><span class="sxs-lookup"><span data-stu-id="d02f7-133">Enter the text of specific warnings that are related to CMR and carriage of merchandise by road.</span></span> <span data-ttu-id="d02f7-134">此文本将包含在报表中。</span><span class="sxs-lookup"><span data-stu-id="d02f7-134">This text will be included on the report.</span></span> |
    | <span data-ttu-id="d02f7-135">发货人申报</span><span class="sxs-lookup"><span data-stu-id="d02f7-135">Shippers declaration</span></span> | <span data-ttu-id="d02f7-136">警告</span><span class="sxs-lookup"><span data-stu-id="d02f7-136">Warning</span></span> | <span data-ttu-id="d02f7-137">输入应打印在发货人的申报单上的警告消息的文本（例如，“警告：危险物品，易燃”）。</span><span class="sxs-lookup"><span data-stu-id="d02f7-137">Enter the text of a warning message that should be printed on the shipper's declaration form (for example, "Warning: Dangerous Goods, Flammable").</span></span> |
    | <span data-ttu-id="d02f7-138">发货人申报</span><span class="sxs-lookup"><span data-stu-id="d02f7-138">Shippers declaration</span></span> | <span data-ttu-id="d02f7-139">页脚声明</span><span class="sxs-lookup"><span data-stu-id="d02f7-139">Footer declaration</span></span> | <span data-ttu-id="d02f7-140">输入应打印在装运申报文档底部的消息的文本。</span><span class="sxs-lookup"><span data-stu-id="d02f7-140">Enter the text of a message that should be printed at the bottom of the shipment declaration document.</span></span> |
    | <span data-ttu-id="d02f7-141">危险货物报表语言</span><span class="sxs-lookup"><span data-stu-id="d02f7-141">Hazardous goods report language</span></span> | <span data-ttu-id="d02f7-142">危险货物国内报表语言</span><span class="sxs-lookup"><span data-stu-id="d02f7-142">Hazardous goods domestic report language</span></span> | <span data-ttu-id="d02f7-143">选择与国内装运关联的危险物料报表的默认语言。</span><span class="sxs-lookup"><span data-stu-id="d02f7-143">Select the default language for hazardous materials reports that are associated with domestic shipments.</span></span> |
    | <span data-ttu-id="d02f7-144">危险货物报表语言</span><span class="sxs-lookup"><span data-stu-id="d02f7-144">Hazardous goods report language</span></span> | <span data-ttu-id="d02f7-145">危险货物出口报表语言</span><span class="sxs-lookup"><span data-stu-id="d02f7-145">Hazardous goods export report language</span></span> | <span data-ttu-id="d02f7-146">选择与国际装运关联的危险物料报表的默认语言。</span><span class="sxs-lookup"><span data-stu-id="d02f7-146">Select the default language for hazardous materials reports that are associated with international shipments.</span></span> |

## <a name="hazardous-materials-report"></a><span data-ttu-id="d02f7-147">危险物料报表</span><span class="sxs-lookup"><span data-stu-id="d02f7-147">Hazardous materials report</span></span>

<span data-ttu-id="d02f7-148">**危险物料**报表显示已设置和定义以让它们包含危险货物信息的所有物料的列表。</span><span class="sxs-lookup"><span data-stu-id="d02f7-148">The **Hazardous materials** report shows a list of all items that have been set up and defined so that they have dangerous goods information.</span></span> <span data-ttu-id="d02f7-149">您可以使用此报表来监视和查看必须维护的信息。</span><span class="sxs-lookup"><span data-stu-id="d02f7-149">You can use this report to monitor and review the information that you must maintain.</span></span> <span data-ttu-id="d02f7-150">此报表的页面显示危险物料设置中的限选字段。</span><span class="sxs-lookup"><span data-stu-id="d02f7-150">The page for the report shows a limited selection of fields from the hazardous material setup.</span></span> <span data-ttu-id="d02f7-151">不过，您可以对其进行个性化设置来根据需要添加其他字段。</span><span class="sxs-lookup"><span data-stu-id="d02f7-151">However, you can personalize it to add additional fields as you require.</span></span>

<span data-ttu-id="d02f7-152">查看此报表，请转到**产品信息管理 \> 查询和报表 \> 危险物料装运文档 \> 危险物料**。</span><span class="sxs-lookup"><span data-stu-id="d02f7-152">To view this report, go to **Product information management \> Inquiries and reports \> Hazardous material shipping documentation \> Hazardous materials**.</span></span>

## <a name="hazardous-material-stock-limit-report"></a><a name="stock-limit-report"></a><span data-ttu-id="d02f7-153">危险物料存货限制报表</span><span class="sxs-lookup"><span data-stu-id="d02f7-153">Hazardous material stock limit report</span></span>

<span data-ttu-id="d02f7-154">**危险物料存货限制**报表可让您监视仓库位置中危险物料的库存级别，以确保它们保持在建立的安全限制内。</span><span class="sxs-lookup"><span data-stu-id="d02f7-154">The **Hazardous material stock limit** report lets you monitor the stock levels of the hazardous materials in your warehouse locations, to make sure that they remain under established, safe limits.</span></span> <span data-ttu-id="d02f7-155">这些限制来自为每个已发布产品定义的限制。</span><span class="sxs-lookup"><span data-stu-id="d02f7-155">These limits come from the limits that are defined for each released product.</span></span>

<span data-ttu-id="d02f7-156">查看此报表，请转到**产品信息管理 \> 查询和报表 \> 危险装运文档 \> 危险物料存货限制**。</span><span class="sxs-lookup"><span data-stu-id="d02f7-156">To view this report, go to **Product information management \> Inquiries and reports \> Hazardous shipping documentation \> Hazardous material stock limits**.</span></span>

<span data-ttu-id="d02f7-157">有关如何设置已发布产品的存货限制的详细信息，请参阅[设置危险产品的存货限制](hazmat-items.md#stock-limits)。</span><span class="sxs-lookup"><span data-stu-id="d02f7-157">For more information about how to set stock limits on a released product, see [Set stock limits for hazardous products](hazmat-items.md#stock-limits).</span></span>

<span data-ttu-id="d02f7-158">用于存货限制的法规在**仓库管理参数**页面定义。</span><span class="sxs-lookup"><span data-stu-id="d02f7-158">The regulation that is used for stock limits is defined on the **Warehouse management parameters** page.</span></span> <span data-ttu-id="d02f7-159">转到**仓库管理 \> 设置 \> 仓库管理参数**，然后在**报表**选项卡上，在**危险物料存货限制**中，指定法规代码。</span><span class="sxs-lookup"><span data-stu-id="d02f7-159">Go to **Warehouse management \> Setup \> Warehouse management parameters**, and then, on the **Reports** tab, in the **Hazardous materials stock limit**, specify a regulation code.</span></span> <span data-ttu-id="d02f7-160">有关详细信息，请参阅本主题前面的[设置危险物料报告](#set-up)一节。</span><span class="sxs-lookup"><span data-stu-id="d02f7-160">For more information, see the [Set up hazardous materials reporting](#set-up) section earlier in this topic.</span></span>

## <a name="verified-gross-mass-report"></a><span data-ttu-id="d02f7-161">已验证总重报表</span><span class="sxs-lookup"><span data-stu-id="d02f7-161">Verified gross mass report</span></span>

<span data-ttu-id="d02f7-162">**已验证总重**报表可让您打印有关装运重量的信息。</span><span class="sxs-lookup"><span data-stu-id="d02f7-162">The **Verified gross mass** report lets you print information about the weight of a shipment.</span></span>

<span data-ttu-id="d02f7-163">要生成并打印此报表，请转到**仓库管理 \> 装运 \> 所有装运**，打开相关装运。</span><span class="sxs-lookup"><span data-stu-id="d02f7-163">To generate and print this report, go to **Warehouse management \> Shipments \> All shipments**, and open the relevant shipment.</span></span> <span data-ttu-id="d02f7-164">然后，在操作窗格上，在**装运**选项卡上，在**危险物料文档**组中，选择**已验证总重**。</span><span class="sxs-lookup"><span data-stu-id="d02f7-164">Then, on the Action Pane, on the **Shipments** tab, in the **Hazardous materials document** group, select **Verified gross mass**.</span></span>

## <a name="multimodal-dangerous-goods-report"></a><span data-ttu-id="d02f7-165">多模式危险货物报表</span><span class="sxs-lookup"><span data-stu-id="d02f7-165">Multimodal dangerous goods report</span></span>

<span data-ttu-id="d02f7-166">对于必须使用多种运输方法组合的装运，将提供**多模式危险货物**报表。</span><span class="sxs-lookup"><span data-stu-id="d02f7-166">The **Multimodal dangerous goods** report is provided for shipments that must be moved by using a combination of transport methods.</span></span> <span data-ttu-id="d02f7-167">通常在装运首先通过陆运然后通过海运运输时使用。</span><span class="sxs-lookup"><span data-stu-id="d02f7-167">It's typically used when a shipment is moved first by road and later by sea.</span></span>

<span data-ttu-id="d02f7-168">要生成并打印此报表，请转到**仓库管理 \> 装运 \> 所有装运**，打开相关装运。</span><span class="sxs-lookup"><span data-stu-id="d02f7-168">To generate and print this report, go to **Warehouse management \> Shipments \> All shipments**, and open the relevant shipment.</span></span> <span data-ttu-id="d02f7-169">然后，在操作窗格上，在**装运**选项卡上，在**危险物料文档**组中，选择**多模式危险货物**。</span><span class="sxs-lookup"><span data-stu-id="d02f7-169">Then, on the Action Pane, on the **Shipments** tab, in the **Hazardous materials document** group, select **Multi model dangerous goods**.</span></span>

<span data-ttu-id="d02f7-170">生成此报表时，将保存信息，让您可以编辑和/或在必要时重新打印报表。</span><span class="sxs-lookup"><span data-stu-id="d02f7-170">When you generate this report, the information is saved so that you can edit it and/or reprint the report if you must.</span></span> <span data-ttu-id="d02f7-171">要编辑生成的报表，请转到**仓库管理 \> 查询和报表 \> 危险物料装运文档 \> 多模式危险货物**，然后在列表中找到相关报表。</span><span class="sxs-lookup"><span data-stu-id="d02f7-171">To edit a generated report, go to **Warehouse management \> Inquiries and reports \> Hazardous materials shipping documentation \> Multimodal dangerous goods**, and find the relevant report in the list.</span></span> <span data-ttu-id="d02f7-172">根据需要完成内容的编辑后，在操作窗格上选择**打印**来打印报表。</span><span class="sxs-lookup"><span data-stu-id="d02f7-172">After you've finished editing the content as you require, select **Print** on the Action Pane to print the report.</span></span>

## <a name="shippers-declaration-report"></a><span data-ttu-id="d02f7-173">发货人申报报表</span><span class="sxs-lookup"><span data-stu-id="d02f7-173">Shippers declaration report</span></span>

<span data-ttu-id="d02f7-174">**发货人申报**报表可让您打印与装运中所包含物料的申报有关的信息。</span><span class="sxs-lookup"><span data-stu-id="d02f7-174">The **Shippers declaration** report lets you print information that is related to a declaration of the materials that are included in the shipment.</span></span>

<span data-ttu-id="d02f7-175">要生成并打印此报表，请转到**仓库管理 \> 装运 \> 所有装运**，打开相关装运。</span><span class="sxs-lookup"><span data-stu-id="d02f7-175">To generate and print this report, go to **Warehouse management \> Shipments \> All shipments**, and open the relevant shipment.</span></span> <span data-ttu-id="d02f7-176">然后，在操作窗格上，在**装运**选项卡上，在**危险物料文档**组中，选择**发货人申报**。</span><span class="sxs-lookup"><span data-stu-id="d02f7-176">Then, on the Action Pane, on the **Shipments** tab, in the **Hazardous materials document** group, select **Shippers declaration**.</span></span>

## <a name="carriage-of-merchandise-by-road-report"></a><span data-ttu-id="d02f7-177">陆运商品运输报表</span><span class="sxs-lookup"><span data-stu-id="d02f7-177">Carriage of merchandise by road report</span></span>

<span data-ttu-id="d02f7-178">**陆运商品运输**报表类似于提单，但此报表通常根据关于《国际陆运危险货物运输 (ADR)》法规的协议，用于欧洲的陆运运输。</span><span class="sxs-lookup"><span data-stu-id="d02f7-178">The **Carriage of merchandise by road** report resembles a bill of lading but is typically used for road transportation in Europe under the Agreement concerning the International Carriage of Dangerous Goods by Road (ADR) regulations.</span></span> <span data-ttu-id="d02f7-179">除非您在**仓库管理参数**页面上设置了**危险物料组描述**字段，否则此报表使用物料的装运打印文本。</span><span class="sxs-lookup"><span data-stu-id="d02f7-179">This report uses the shipping print text for an item unless you set the **Hazardous material group description** field on the **Warehouse management parameters** page.</span></span>

<span data-ttu-id="d02f7-180">要生成并打印此报表，请转到**仓库管理 \> 装运 \> 所有装运**，打开相关装运。</span><span class="sxs-lookup"><span data-stu-id="d02f7-180">To generate and print this report, go to **Warehouse management \> Shipments \> All shipments**, and open the relevant shipment.</span></span> <span data-ttu-id="d02f7-181">然后，在操作窗格上，在**装运**选项卡上，在**危险物料文档**组中，选择**陆运商品运输**。</span><span class="sxs-lookup"><span data-stu-id="d02f7-181">Then, on the Action Pane, on the **Shipments** tab, in the **Hazardous materials document** group, select **Carriage of merchandise by road**.</span></span>

<span data-ttu-id="d02f7-182">生成此报表时，将保存信息，让您可以编辑和/或在必要时重新打印报表。</span><span class="sxs-lookup"><span data-stu-id="d02f7-182">When you generate this report, the information is saved so that you can edit it and/or reprint the report if you must.</span></span> <span data-ttu-id="d02f7-183">要编辑生成的报表，请转到**仓库管理 \> 查询和报表 \> 危险物料装运文档 \> 陆运商品运输**，然后在列表中找到相关报表。</span><span class="sxs-lookup"><span data-stu-id="d02f7-183">To edit a generated report, go to **Warehouse management \> Inquiries and reports \> Hazardous materials shipping documentation \> Carriage of merchandise by road**, and find the relevant report in the list.</span></span> <span data-ttu-id="d02f7-184">根据需要完成内容的编辑后，在操作窗格上选择**打印**来打印报表。</span><span class="sxs-lookup"><span data-stu-id="d02f7-184">After you've finished editing the content as you require, select **Print** on the Action Pane to print the report.</span></span>

## <a name="shipment-summary-report"></a><span data-ttu-id="d02f7-185">装运摘要报表</span><span class="sxs-lookup"><span data-stu-id="d02f7-185">Shipment summary report</span></span>

<span data-ttu-id="d02f7-186">**装运摘要**报表提供按与已发布物料相关的运输类别汇总的信息。</span><span class="sxs-lookup"><span data-stu-id="d02f7-186">The **Shipment summary** report provides information that is summarized by the transport category that is related to the released items.</span></span>

<span data-ttu-id="d02f7-187">要生成并打印此报表，请转到**仓库管理 \> 装运 \> 所有装运**，打开相关装运。</span><span class="sxs-lookup"><span data-stu-id="d02f7-187">To generate and print this report, go to **Warehouse management \> Shipments \> All shipments**, and open the relevant shipment.</span></span> <span data-ttu-id="d02f7-188">然后，在操作窗格上，在**装运**选项卡上，在**危险物料文档**组中，选择**装运摘要**。</span><span class="sxs-lookup"><span data-stu-id="d02f7-188">Then, on the Action Pane, on the **Shipments** tab, in the **Hazardous materials document** group, select **Shipment summary**.</span></span>

## <a name="bill-of-lading-report"></a><span data-ttu-id="d02f7-189">提单报表</span><span class="sxs-lookup"><span data-stu-id="d02f7-189">bill of lading report</span></span>

<span data-ttu-id="d02f7-190">当系统中的危险物料功能打开时，**提单**报表中将包含一个**危险物料**列，指示负荷中是否包含危险物料。</span><span class="sxs-lookup"><span data-stu-id="d02f7-190">When the hazardous materials feature is turned on in your system, the **bill of lading** report includes a **Hazardous materials** column that indicates whether a load includes hazardous materials.</span></span> <span data-ttu-id="d02f7-191">与以往一样，可从**所有负荷**页面获得此报表。</span><span class="sxs-lookup"><span data-stu-id="d02f7-191">This report is available from the **All loads** page, as usual.</span></span>

## <a name="packing-list-report"></a><span data-ttu-id="d02f7-192">装箱单报表</span><span class="sxs-lookup"><span data-stu-id="d02f7-192">Packing list report</span></span>

<span data-ttu-id="d02f7-193">在系统中打开危险物料功能后，装箱单中将包含与物料的装运打印文本有关的其他信息。</span><span class="sxs-lookup"><span data-stu-id="d02f7-193">When the hazardous materials feature is turned on in your system, packing lists include additional information that is related to the shipping print text for an item.</span></span> <span data-ttu-id="d02f7-194">与以往一样，可从**所有负荷**页面获得此报表。</span><span class="sxs-lookup"><span data-stu-id="d02f7-194">This report is available from the **All loads** page, as usual.</span></span>
