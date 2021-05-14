---
title: 质量管理测试
description: 本主题介绍如何在 Microsoft Dynamics 365 Supply Chain Management 中创建可用于质检订单的测试。
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b88011f486b6582db4727b85d021868899c6abe1
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956563"
---
# <a name="quality-management-tests"></a><span data-ttu-id="c2252-103">质量管理测试</span><span class="sxs-lookup"><span data-stu-id="c2252-103">Quality management tests</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c2252-104">本主题介绍如何在 Microsoft Dynamics 365 Supply Chain Management 中创建可用于质检订单的测试。</span><span class="sxs-lookup"><span data-stu-id="c2252-104">This topic describes how to create tests that can be used for quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="c2252-105">您将使用 **测试** 页定义和查看用于确定产品是否符合质量规范的各个测试。</span><span class="sxs-lookup"><span data-stu-id="c2252-105">You use the **Tests** page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="c2252-106">您可以将一个或多个单独测试分配给测试组。</span><span class="sxs-lookup"><span data-stu-id="c2252-106">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="c2252-107">在这种情况下，您还可以指定测试特定信息，例如可接受的度量值。</span><span class="sxs-lookup"><span data-stu-id="c2252-107">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="c2252-108">度量值用于定量测试。</span><span class="sxs-lookup"><span data-stu-id="c2252-108">Measurement values are used for quantitative tests.</span></span> <span data-ttu-id="c2252-109">对于定性测试，将使用测试变量。</span><span class="sxs-lookup"><span data-stu-id="c2252-109">For qualitative tests, test variables are used.</span></span>

- <span data-ttu-id="c2252-110">对于定量测试，**类型** 字段将设置为 *整数* 或 *分数*。</span><span class="sxs-lookup"><span data-stu-id="c2252-110">For quantitative tests, the **Type** field is set to *Integer* or *Fraction*.</span></span> <span data-ttu-id="c2252-111">另外还将指定度量单位。</span><span class="sxs-lookup"><span data-stu-id="c2252-111">A unit of measure is also specified.</span></span> <span data-ttu-id="c2252-112">质量规范和测试结果表示为数字。</span><span class="sxs-lookup"><span data-stu-id="c2252-112">Quality specifications and test results are expressed as numbers.</span></span>
- <span data-ttu-id="c2252-113">对于定性测试，**类型** 字段将设置为 *选项*。</span><span class="sxs-lookup"><span data-stu-id="c2252-113">For qualitative tests, the **Type** field is set to *Option*.</span></span> <span data-ttu-id="c2252-114">定性测试需要有关要度量的质量变量及其枚举选项的附加信息。</span><span class="sxs-lookup"><span data-stu-id="c2252-114">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="c2252-115">质量规范和测试结果根据结果表示。</span><span class="sxs-lookup"><span data-stu-id="c2252-115">Quality specifications and test results are expressed according to an outcome.</span></span>

<span data-ttu-id="c2252-116">您可以选择将测试仪器分配给测试。</span><span class="sxs-lookup"><span data-stu-id="c2252-116">You can optionally assign a test instrument to a test.</span></span> <span data-ttu-id="c2252-117">不过，创建和使用针对质检订单的测试不需要测试仪器。</span><span class="sxs-lookup"><span data-stu-id="c2252-117">However, test instruments aren't required to create and use tests with quality orders.</span></span> <span data-ttu-id="c2252-118">有关详细信息，请参阅[质量管理测试仪器](quality-test-instruments.md)。</span><span class="sxs-lookup"><span data-stu-id="c2252-118">For more information, see [Quality management test instruments](quality-test-instruments.md).</span></span>

<span data-ttu-id="c2252-119">您还可以选择为测试指定单位，来指示记录测试结果所使用的度量单位。</span><span class="sxs-lookup"><span data-stu-id="c2252-119">You can also optionally specify a unit for a test, to indicate the unit of measure that test results are recorded in.</span></span> <span data-ttu-id="c2252-120">例如，针对温度的测试可能包含华氏度或摄氏度单位。</span><span class="sxs-lookup"><span data-stu-id="c2252-120">For example, a test for temperature might include a unit of either degrees Fahrenheit or degrees Celsius.</span></span>

## <a name="example-of-a-test"></a><span data-ttu-id="c2252-121">测试示例</span><span class="sxs-lookup"><span data-stu-id="c2252-121">Example of a test</span></span>

<span data-ttu-id="c2252-122">某个制造公司对采购物料执行两个测试：针对物料质量的定量测试和针对包装损坏的定性测试。</span><span class="sxs-lookup"><span data-stu-id="c2252-122">A manufacturing company performs two tests on purchased material: a quantitative test for material quality and a qualitative test for packaging damage.</span></span> <span data-ttu-id="c2252-123">该公司指定有关质量测试的附加信息来定义测试变量（例如，损坏的包装）及其结果。</span><span class="sxs-lookup"><span data-stu-id="c2252-123">The company specifies additional information about the qualitative test to define the test variable (for example, damaged packaging) and its outcomes.</span></span> <span data-ttu-id="c2252-124">公司使用 **测试组** 页将两个测试分配给一个测试组并指定测试特定信息。</span><span class="sxs-lookup"><span data-stu-id="c2252-124">The company uses the **Test groups** page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="c2252-125">将测试组分配给质检订单，以便公司可以报告这两个测试的测试结果。</span><span class="sxs-lookup"><span data-stu-id="c2252-125">The test group is assigned to a quality order so that the company can report test results for the two tests.</span></span>

## <a name="create-a-test"></a><span data-ttu-id="c2252-126">创建测试</span><span class="sxs-lookup"><span data-stu-id="c2252-126">Create a test</span></span>

<span data-ttu-id="c2252-127">请按照以下步骤创建测试。</span><span class="sxs-lookup"><span data-stu-id="c2252-127">Follow these steps to create a test.</span></span>

1. <span data-ttu-id="c2252-128">转到 **库存管理 \> 设置 \> 质量控制 \> 测试**。</span><span class="sxs-lookup"><span data-stu-id="c2252-128">Go to **Inventory management \> Setup \> Quality control \> Tests**.</span></span>
1. <span data-ttu-id="c2252-129">在操作窗格上，选择 **新建** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="c2252-129">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="c2252-130">然后，针对新行设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="c2252-130">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="c2252-131">**测试** – 为测试输入唯一 ID 或名称。</span><span class="sxs-lookup"><span data-stu-id="c2252-131">**Test** – Enter a unique ID or name for the test.</span></span>
    - <span data-ttu-id="c2252-132">**描述** – 输入测试的详细描述。</span><span class="sxs-lookup"><span data-stu-id="c2252-132">**Description** – Enter a detailed description of the test.</span></span>
    - <span data-ttu-id="c2252-133">**类型** – 选择测试产生的结果类型。</span><span class="sxs-lookup"><span data-stu-id="c2252-133">**Type** – Select the type of results that the test produces.</span></span> <span data-ttu-id="c2252-134">对于定量测试，选择 *分数* 或 *整数*。</span><span class="sxs-lookup"><span data-stu-id="c2252-134">For quantitative tests, select *Fraction* or *Integer*.</span></span> <span data-ttu-id="c2252-135">对于定性测试，选择 *选项*。</span><span class="sxs-lookup"><span data-stu-id="c2252-135">For qualitative tests, select *Option*.</span></span>
    - <span data-ttu-id="c2252-136">**测试仪器** – 选择应用于测试的[测试仪器](quality-test-instruments.md)。</span><span class="sxs-lookup"><span data-stu-id="c2252-136">**Test instrument** – Select a [test instrument](quality-test-instruments.md) that should be used for the test.</span></span>
    - <span data-ttu-id="c2252-137">**单位** – 如果您在 **类型** 字段中选择了 *分数* 或 *整数*（即如果测试是定量测试），则选择记录测试结果应使用的度量单位。</span><span class="sxs-lookup"><span data-stu-id="c2252-137">**Unit** – If you selected *Fraction* or *Integer* in the **Type** field (that is, if the test is a quantitative test), select the unit of measure that test results should be recorded in.</span></span>

1. <span data-ttu-id="c2252-138">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c2252-138">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="c2252-139">保存测试后，您将无法再编辑网格中的 **类型** 字段。</span><span class="sxs-lookup"><span data-stu-id="c2252-139">After you save a test, you can no longer edit the **Type** field in the grid.</span></span> <span data-ttu-id="c2252-140">如果必须更改将为测试记录的测试结果的类型，在操作窗格上选择 **更改质量测试类型**。</span><span class="sxs-lookup"><span data-stu-id="c2252-140">If you must change the type of test results that will be recorded for a test, select **Change quality test type** on the Action Pane.</span></span> <span data-ttu-id="c2252-141">在 **更改质量测试类型** 对话框中，将 **新类型** 字段设置为所需类型，然后选择 **确定** 关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="c2252-141">In the **Change quality test type** dialog box, set the **New type** field to the desired type, and then select **OK** to close the dialog box.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c2252-142">其他资源</span><span class="sxs-lookup"><span data-stu-id="c2252-142">Additional resources</span></span>

- [<span data-ttu-id="c2252-143">质量管理测试仪器</span><span class="sxs-lookup"><span data-stu-id="c2252-143">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="c2252-144">质量管理测试组</span><span class="sxs-lookup"><span data-stu-id="c2252-144">Quality management test groups</span></span>](quality-test-groups.md)
- [<span data-ttu-id="c2252-145">质量管理测试变量</span><span class="sxs-lookup"><span data-stu-id="c2252-145">Quality management test variables</span></span>](quality-test-variables.md)
- [<span data-ttu-id="c2252-146">质量关联</span><span class="sxs-lookup"><span data-stu-id="c2252-146">Quality associations</span></span>](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
