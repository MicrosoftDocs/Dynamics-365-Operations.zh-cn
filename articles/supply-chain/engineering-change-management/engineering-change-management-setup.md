---
title: 为工程更改管理建立通用值
description: 本主题介绍如何建立用于工程更改管理的各部分中的参数的通用值。
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductParameters, EngChgEcmSeverityTable, EngChgEcmSeverityRuleSet, EngChgEcmSeverityLookup,EngChgEcmSeverityChart,EngChgEcmRequestSeverityChart,EngChgEcmPriorityTable, EngChgEcmPriorityLookup, EngChgEcmPriorityChart, EngChgEcmMaterialDisposition, EngChgEcmEH
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: ee2be7d59f327876b92386c66433aeaf06df489c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5262349"
---
# <a name="establish-common-values-for-engineering-change-management"></a><span data-ttu-id="1c2a2-103">为工程更改管理建立通用值</span><span class="sxs-lookup"><span data-stu-id="1c2a2-103">Establish common values for engineering change management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1c2a2-104">设置工程更改管理时，必须建立多个值集合，它们将用于填充用户界面 (UI) 的其他部分中的下拉列表。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-104">When you set up engineering change management, you must establish several collections of values that will be used to fill in drop-down lists in other parts of the user interface (UI).</span></span> <span data-ttu-id="1c2a2-105">您应该根据生产的产品类型和特定的业务需求指定这些值。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-105">You should specify these values according to the types of products that you produce and your specific business needs.</span></span>

## <a name="engineering-change-categories"></a><span data-ttu-id="1c2a2-106">工程更改类别</span><span class="sxs-lookup"><span data-stu-id="1c2a2-106">Engineering change categories</span></span>

<span data-ttu-id="1c2a2-107">使用工程更改类别组织工程更改订单，以便它们更易于管理和审查。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-107">You use engineering change categories to organize your engineering change orders, so that they are easier to manage and review.</span></span> <span data-ttu-id="1c2a2-108">例如，您可能会发现它在设置工作流时很有用（根据类别），特定部门必须审查提出的更改。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-108">For example, you might find it useful to set up a workflow where, depending on the category, a specific department must review the proposed changes.</span></span> <span data-ttu-id="1c2a2-109">因此，工程更改订单包括 **类别** 字段。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-109">Therefore, the engineering change order includes a **Category** field.</span></span>

<span data-ttu-id="1c2a2-110">若要建立在公司中使用的工程更改类别的集合，请转到 **工程更改管理 \> 设置 \> 工程更改管理 \> 工程更改类别**。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-110">To establish the collection of engineering change categories that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Engineering change categories**.</span></span> <span data-ttu-id="1c2a2-111">然后，您可以使用操作窗格上的按钮添加、删除和编辑值，并将它们按照应在列出它们的下拉列表中显示的顺序排列。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-111">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

## <a name="engineering-change-priorities"></a><span data-ttu-id="1c2a2-112">工程更改优先级</span><span class="sxs-lookup"><span data-stu-id="1c2a2-112">Engineering change priorities</span></span>

<span data-ttu-id="1c2a2-113">使用工程更改优先级来指示工程更改订单的重要性或紧急程度。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-113">You use engineering change priorities to indicate the importance or urgency of an engineering change order.</span></span> <span data-ttu-id="1c2a2-114">它们可以帮助您跟踪工程更改订单的重要性，以便您可以轻松确定应首先处理哪些订单以及处理速度。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-114">They can help you keep track of the importance of an engineering change order, so that you can easily identify which orders should be processed first, and how quickly.</span></span>

<span data-ttu-id="1c2a2-115">若要建立在公司中使用的工程更改优先级的集合，请转到 **工程更改管理 \> 设置 \> 工程更改管理 \> 工程更改优先级**。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-115">To establish the collection of engineering change priorities that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Engineering change priorities**.</span></span> <span data-ttu-id="1c2a2-116">然后，您可以使用操作窗格上的按钮添加、删除和编辑值，并将它们按照应在列出它们的下拉列表中显示的顺序排列。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-116">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

## <a name="engineering-change-reasons"></a><span data-ttu-id="1c2a2-117">工程更改原因</span><span class="sxs-lookup"><span data-stu-id="1c2a2-117">Engineering change reasons</span></span>

<span data-ttu-id="1c2a2-118">工程更改原因指示更改顺序中更改的原因或性质。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-118">Engineering change reasons indicate the cause or nature of the change in the change order.</span></span>

<span data-ttu-id="1c2a2-119">若要建立在公司中使用的工程更改原因的集合，请转到 **工程更改管理 \> 设置 \> 工程更改管理 \> 工程更改原因**。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-119">To establish the collection of engineering change reasons that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Engineering change reasons**.</span></span> <span data-ttu-id="1c2a2-120">然后，您可以使用操作窗格上的按钮添加、删除和编辑值，并将它们按照应在列出它们的下拉列表中显示的顺序排列。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-120">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

## <a name="material-disposal-codes"></a><span data-ttu-id="1c2a2-121">物料处置代码</span><span class="sxs-lookup"><span data-stu-id="1c2a2-121">Material disposal codes</span></span>

<span data-ttu-id="1c2a2-122">使用材料处置代码对成品中使用的材料或必须以特定方式处置或需要进行某些处理的组件进行分类，然后才能将它们添加到常规垃圾箱中。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-122">You use material disposal codes to categorize materials that are used in your finished goods, or components that must be disposed of in a specific way or require some treatment before they can be added to your regular trash.</span></span> <span data-ttu-id="1c2a2-123">将相关产品添加到工程更改订单时，您可以分配处置代码作为更改详细信息的一部分。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-123">When you add a relevant product to an engineering change order, you can assign a disposal code as part of the change details.</span></span>

<span data-ttu-id="1c2a2-124">若要建立在公司中使用的材料处置代码的集合，请转到 **工程更改管理 \> 设置 \> 工程更改管理 \> 材料处置代码**。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-124">To establish the collection of material disposal codes that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Material disposal codes**.</span></span> <span data-ttu-id="1c2a2-125">然后，您可以使用操作窗格上的按钮添加、删除和编辑值，并将它们按照应在列出它们的下拉列表中显示的顺序排列。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-125">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

## <a name="received-customer-approval"></a><span data-ttu-id="1c2a2-126">收到的客户审核</span><span class="sxs-lookup"><span data-stu-id="1c2a2-126">Received customer approval</span></span>

<span data-ttu-id="1c2a2-127">为特定客户设计产品时，通常必须先验证设计和规格，然后才能将产品设置为就绪。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-127">When you design products for a specific customer, the design and specifications often must be validated before the product can be set as ready.</span></span> <span data-ttu-id="1c2a2-128">**获得客户审批** 字段可让您指示产品在客户审批流程中的哪个阶段和/或是否已获得审批。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-128">The **Received customer approval** field lets you indicate how far in the customer approval process the product is and/or whether the approval has been received.</span></span>

<span data-ttu-id="1c2a2-129">若要建立在公司中使用的获得客户审批值的集合，请转到 **工程更改管理 \> 设置 \> 工程更改管理 \> 获得客户审批**。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-129">To establish the collection of received customer approval values that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Received customer approval**.</span></span> <span data-ttu-id="1c2a2-130">然后，您可以使用操作窗格上的按钮添加、删除和编辑值，并将它们按照应在列出它们的下拉列表中显示的顺序排列。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-130">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

## <a name="engineering-change--environmental-health-and-safety-codes"></a><span data-ttu-id="1c2a2-131">工程更改 – 环境健康和安全法规</span><span class="sxs-lookup"><span data-stu-id="1c2a2-131">Engineering change – Environmental health and safety codes</span></span>

<span data-ttu-id="1c2a2-132">如果在制造产品时必须考虑任何标准的环境健康和安全法规或公司特定的法规或程序，您可以使用环境健康和安全法规对其进行定义。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-132">If any standard environmental health and safety regulations, or company-specific regulations or procedures, must be considered in the manufacture of a product, you can use the environmental health and safety codes to define them.</span></span> <span data-ttu-id="1c2a2-133">在工程更改订单中，您可以在编辑受影响产品的详细信息时指示哪些法规适用于产品的制造。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-133">In the engineering change order, you can indicate which codes apply to the manufacture of a product while you edit the details of the affected product.</span></span>

<span data-ttu-id="1c2a2-134">若要建立在公司中使用的健康和安全值的集合，请转到 **工程更改管理 \> 设置 \> 工程更改管理 \> 环境健康和安全法规**。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-134">To establish the collection of health and safety values that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Engineering change - Environmental health and safety codes**.</span></span> <span data-ttu-id="1c2a2-135">然后，您可以使用操作窗格上的按钮添加、删除和编辑值，并将它们按照应在列出它们的下拉列表中显示的顺序排列。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-135">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

## <a name="engineering-change-severities"></a><span data-ttu-id="1c2a2-136">工程更改严重性</span><span class="sxs-lookup"><span data-stu-id="1c2a2-136">Engineering change severities</span></span>

<span data-ttu-id="1c2a2-137">使用工程更改严重性来指示对工程更改订单中的产品应用的影响级别。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-137">You use engineering change severities to indicate the level of impact that applies to the products in an engineering change order.</span></span>

<span data-ttu-id="1c2a2-138">若要建立在公司中使用的工程更改严重性的集合，请转到 **工程更改管理 \> 设置 \> 工程更改管理 \> 工程更改严重性**。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-138">To establish the collection of engineering change severities that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Engineering change severities**.</span></span> <span data-ttu-id="1c2a2-139">然后，您可以使用操作窗格上的按钮添加、删除和编辑值，并将它们按照应在列出它们的下拉列表中显示的顺序排列。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-139">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

<span data-ttu-id="1c2a2-140">您可以建立适用于您创建的每个严重性级别的规则。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-140">You can establish rules that apply to each severity level that you create.</span></span> <span data-ttu-id="1c2a2-141">有关如何分配这些规则的详细信息，请参见下一部分。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-141">For more information about how to assign these rules, see the next section.</span></span>

## <a name="engineering-change-severity-rule-sets"></a><span data-ttu-id="1c2a2-142">工程更改严重性规则集</span><span class="sxs-lookup"><span data-stu-id="1c2a2-142">Engineering change severity rule sets</span></span>

<span data-ttu-id="1c2a2-143">使用工程更改严重性规则集来建立一组规则，可用于根据受影响产品中的更改类型自动计算更改订单的严重性。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-143">You use engineering change severity rule sets to establish a group of rules that you can use to automatically calculate the severity of the change order, based on the type of changes in the affected products.</span></span> <span data-ttu-id="1c2a2-144">若要使用严重性规则，请打开 **工程更改管理参数** 页面，然后将 **严重性规则** 字段设置为 *计算* 或 *自动计算*。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-144">To use the severity rules, open the **Engineering change management parameters** page, and set the **Severity rule** field to *Calculate* or *Calculate automatically*.</span></span>

<span data-ttu-id="1c2a2-145">当系统评估严重性时，它将按照规则在页面上显示的从上到下的顺序处理规则。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-145">When the system evaluates severity, it processes the rules in the order in which they appear on the page, from top to bottom.</span></span> <span data-ttu-id="1c2a2-146">对于要选择且已建立其优先级的规则，必须满足规则集中的所有规则。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-146">For a rule to be selected and have its priority established, all the rules in a rule set must be met.</span></span>

<span data-ttu-id="1c2a2-147">若要设置适用于您定义的每个更改严重性级别的规则，请转到 **工程更改管理 \>设置 \> 工程更改管理 \> 工程更改严重性规则集**。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-147">To set up the rules that apply to each change severity level that you've defined, go to **Engineering change management \> Setup \> Engineering change management \> Engineering change severity rule sets**.</span></span> <span data-ttu-id="1c2a2-148">然后按照以下步骤之一操作。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-148">Then follow one of these steps.</span></span>

- <span data-ttu-id="1c2a2-149">若要创建新规则集，在操作窗格上选择 **新建**，然后按照此部分后面的说明设置字段。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-149">To create a new rule set, select **New** on the Action Pane, and then set the fields as described later in this section.</span></span>
- <span data-ttu-id="1c2a2-150">若要编辑现有规则集，在列表窗格中选择它，在操作窗格上选择 **编辑**，然后按照此部分后面的说明设置字段。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-150">To edit an existing rule set, select it in the list pane, select **Edit** on the Action Pane, and then set the fields as described later in this section.</span></span>
- <span data-ttu-id="1c2a2-151">若要删除现有规则集，在列表窗格中选择它，然后在操作窗格上选择 **删除**。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-151">To delete an existing rule set, select it in the list pane, and then select **Delete** on the Action Pane.</span></span>
- <span data-ttu-id="1c2a2-152">若要重新排列规则集的列表，在列表窗格中选择规则集，然后在操作窗格上使用 **向上** 和 **向下** 按钮来重新放置它。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-152">To rearrange the list of rule sets, select a rule set in the list pane, and then use the **Up** and **Down** buttons on the Action Pane to reposition it.</span></span>

<span data-ttu-id="1c2a2-153">对于每个规则集，设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="1c2a2-153">For each rule set, set the following field:</span></span>

- <span data-ttu-id="1c2a2-154">**严重性** – 选择严重性级别以为其建立规则。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-154">**Severity** – Select the severity level to establish rules for.</span></span> <span data-ttu-id="1c2a2-155">使用 **工程更改严重性** 页面创建和命名级别。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-155">You use the **Engineering change severities** page to create and name the levels.</span></span> <span data-ttu-id="1c2a2-156">（有关详细信息，请参阅上一部分。）</span><span class="sxs-lookup"><span data-stu-id="1c2a2-156">(For more information, see the previous section.)</span></span>

<span data-ttu-id="1c2a2-157">使用 **规则** 快速选项卡上的按钮添加或删除当前严重性设置的规则。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-157">Use the buttons on the **Rules** FastTab to add or remove a rule for the current severity setting.</span></span> <span data-ttu-id="1c2a2-158">每个规则都有 **规则** 字段和 **名称** 字段。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-158">Each rule has a **Rule** field and a **Name** field.</span></span> <span data-ttu-id="1c2a2-159">规则由系统建立，并指示产品可以具有的更改类型。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-159">The rules are established by the system and indicate the types of changes that a product can have.</span></span> <span data-ttu-id="1c2a2-160">名称指示更改的类型。</span><span class="sxs-lookup"><span data-stu-id="1c2a2-160">The name indicates the type of change.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]