---
title: 质量管理测试变量
description: 本主题介绍如何创建可用于在 Microsoft Dynamics 365 Supply Chain Management 中对质检订单进行定性测试的测试变量。
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
ms.openlocfilehash: 1e94972b41baf3f59a633fa7bbc7434abfb90460
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956564"
---
# <a name="quality-management-test-variables"></a><span data-ttu-id="cb95f-103">质量管理测试变量</span><span class="sxs-lookup"><span data-stu-id="cb95f-103">Quality management test variables</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb95f-104">本主题介绍如何创建可用于在 Microsoft Dynamics 365 Supply Chain Management 中对质检订单进行定性测试的测试变量。</span><span class="sxs-lookup"><span data-stu-id="cb95f-104">This topic describes how to create test variables that can be used for qualitative tests on quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="cb95f-105">对于 **测试** 页上定义的每个定性测试，您必须定义一个测试变量及其可能的结果。</span><span class="sxs-lookup"><span data-stu-id="cb95f-105">For every qualitative test that is defined on the **Tests** page, you must define a test variable and its possible outcomes (results).</span></span> <span data-ttu-id="cb95f-106">（对于定性测试，将 **测试** 页上的 **类型** 字段设置为 *选项*。）</span><span class="sxs-lookup"><span data-stu-id="cb95f-106">(For qualitative tests, the **Type** field on the **Tests** page is set to *Option*.)</span></span>

<span data-ttu-id="cb95f-107">您将使用 **测试变量** 页设置、编辑和查看与定性测试关联的测试变量的可能结果。</span><span class="sxs-lookup"><span data-stu-id="cb95f-107">You use the **Test variables** page to set up, edit, and view the possible outcomes for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="cb95f-108">对于每个结果，您将分配 *通过* 或 *失败* 结果状态，来指示测试在选择该结果作为测试结果时是通过还是失败。</span><span class="sxs-lookup"><span data-stu-id="cb95f-108">For each outcome, you assign an outcome status of either *Pass* or *Fail* to indicate whether the test is passed or failed when that outcome is selected as a test result.</span></span> <span data-ttu-id="cb95f-109">您将使用 **测试组** 页将测试变量及其默认结果分配给单独的定性测试。</span><span class="sxs-lookup"><span data-stu-id="cb95f-109">You use the **Test groups** page to assign a test variable and a default outcome for it to an individual qualitative test.</span></span>

<span data-ttu-id="cb95f-110">对于每个测试变量，我们建议您至少定义两个结果：一个结果状态为 *通过*，另一个结果状态为 *失败*。</span><span class="sxs-lookup"><span data-stu-id="cb95f-110">For every test variable, we recommend that you define at least two outcomes: one that has an outcome status of *Pass* and one that has an outcome status of *Fail*.</span></span> <span data-ttu-id="cb95f-111">可定义的变量或结果的总数没有限制。</span><span class="sxs-lookup"><span data-stu-id="cb95f-111">There is no limit on the total number of variables or outcomes that can be defined.</span></span> <span data-ttu-id="cb95f-112">此外，多个测试可以使用相同的测试变量来记录结果。</span><span class="sxs-lookup"><span data-stu-id="cb95f-112">Additionally, multiple tests can use the same test variables to record results.</span></span>

## <a name="examples-of-test-variables"></a><span data-ttu-id="cb95f-113">测试变量示例</span><span class="sxs-lookup"><span data-stu-id="cb95f-113">Examples of test variables</span></span>

### <a name="example-1"></a><span data-ttu-id="cb95f-114">示例 1</span><span class="sxs-lookup"><span data-stu-id="cb95f-114">Example 1</span></span>

<span data-ttu-id="cb95f-115">一家制造公司对制造的材料执行两项测试。</span><span class="sxs-lookup"><span data-stu-id="cb95f-115">A manufacturing company performs two tests on manufactured materials.</span></span> <span data-ttu-id="cb95f-116">在一项测试中，pH 值与色条关联。</span><span class="sxs-lookup"><span data-stu-id="cb95f-116">In one test, the pH level is associated with a color strip.</span></span> <span data-ttu-id="cb95f-117">可接受的 pH 值以浅色显示，不可接受的 pH 值以深色显示。</span><span class="sxs-lookup"><span data-stu-id="cb95f-117">Acceptable pH levels are in lighter colors, and unacceptable pH levels are in darker colors.</span></span> <span data-ttu-id="cb95f-118">在另一项测试中，执行了多次外观检查，质量工作人员根据自己的判断来确定物料是否通过外观检查。</span><span class="sxs-lookup"><span data-stu-id="cb95f-118">In another test, multiple visual inspections are performed, and quality workers use their judgement to determine whether the item passes or fails the visual inspection.</span></span>

### <a name="example-2"></a><span data-ttu-id="cb95f-119">示例 2</span><span class="sxs-lookup"><span data-stu-id="cb95f-119">Example 2</span></span>

<span data-ttu-id="cb95f-120">一个生产饼干的制造公司对成品使用检查测试。</span><span class="sxs-lookup"><span data-stu-id="cb95f-120">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="cb95f-121">此检查测试具有多个变量。</span><span class="sxs-lookup"><span data-stu-id="cb95f-121">This inspection test has several variables.</span></span> <span data-ttu-id="cb95f-122">一个变量是味道，其可能结果是好和坏。</span><span class="sxs-lookup"><span data-stu-id="cb95f-122">One variable is taste, and the possible outcomes for it are good and bad.</span></span> <span data-ttu-id="cb95f-123">第二个变量是颜色，其可能结果是过暗、过浅和正好。</span><span class="sxs-lookup"><span data-stu-id="cb95f-123">A second variable is color, and the possible outcomes for it are too dark, too light, and correct.</span></span>

## <a name="create-a-test-variable"></a><span data-ttu-id="cb95f-124">创建测试变量</span><span class="sxs-lookup"><span data-stu-id="cb95f-124">Create a test variable</span></span>

<span data-ttu-id="cb95f-125">请按照以下步骤创建测试变量。</span><span class="sxs-lookup"><span data-stu-id="cb95f-125">Follow these steps to create a test variable.</span></span>

1. <span data-ttu-id="cb95f-126">转到 **库存管理 \> 设置 \> 质量控制 \> 测试变量**。</span><span class="sxs-lookup"><span data-stu-id="cb95f-126">Go to **Inventory management \> Setup \> Quality control \> Test variables**.</span></span>
1. <span data-ttu-id="cb95f-127">在操作窗格上，选择 **新建** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="cb95f-127">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="cb95f-128">然后，针对新行设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="cb95f-128">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="cb95f-129">**变量** – 为变量输入唯一 ID 或名称。</span><span class="sxs-lookup"><span data-stu-id="cb95f-129">**Variable** – Enter a unique ID or name for the variable.</span></span>
    - <span data-ttu-id="cb95f-130">**描述** – 输入变量的详细描述。</span><span class="sxs-lookup"><span data-stu-id="cb95f-130">**Description** – Enter a detailed description of the variable.</span></span>

1. <span data-ttu-id="cb95f-131">在仍选择新行的同时，在操作窗格上选择 **结果**。</span><span class="sxs-lookup"><span data-stu-id="cb95f-131">While the new row is still selected, select **Outcomes** on the Action Pane.</span></span>
1. <span data-ttu-id="cb95f-132">在 **测试变量结果** 页上的操作窗格上，选择 **新建** 在网格中添加一行。</span><span class="sxs-lookup"><span data-stu-id="cb95f-132">On the **Test variable outcomes** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="cb95f-133">然后，针对新行设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="cb95f-133">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="cb95f-134">**结果** – 为结果输入唯一 ID 或名称。</span><span class="sxs-lookup"><span data-stu-id="cb95f-134">**Outcome** – Enter a unique ID or name for the outcome.</span></span>
    - <span data-ttu-id="cb95f-135">**描述** – 输入结果的详细描述。</span><span class="sxs-lookup"><span data-stu-id="cb95f-135">**Description** – Enter a detailed description of the outcome.</span></span>
    - <span data-ttu-id="cb95f-136">**结果状态** – 选择 *通过* 或 *失败* 来指示测试在选择该结果作为测试结果时是通过还是失败。</span><span class="sxs-lookup"><span data-stu-id="cb95f-136">**Outcome status** – Select either *Pass* or *Fail* to indicate whether the test is passed or failed when the outcome is selected as a test result.</span></span>

1. <span data-ttu-id="cb95f-137">对其他每个结果重复上一个步骤。</span><span class="sxs-lookup"><span data-stu-id="cb95f-137">Repeat the previous step for each additional outcome.</span></span> <span data-ttu-id="cb95f-138">确保至少一个结果的结果状态为 *通过*，至少一个结果的结果状态为 *失败*。</span><span class="sxs-lookup"><span data-stu-id="cb95f-138">Make sure that at least one outcome has an outcome status of *Pass* and at least one has an outcome status of *Fail*.</span></span>
1. <span data-ttu-id="cb95f-139">关闭页面。</span><span class="sxs-lookup"><span data-stu-id="cb95f-139">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cb95f-140">其他资源</span><span class="sxs-lookup"><span data-stu-id="cb95f-140">Additional resources</span></span>

- [<span data-ttu-id="cb95f-141">质量管理测试仪器</span><span class="sxs-lookup"><span data-stu-id="cb95f-141">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="cb95f-142">质量管理测试</span><span class="sxs-lookup"><span data-stu-id="cb95f-142">Quality management tests</span></span>](quality-tests.md)
- [<span data-ttu-id="cb95f-143">质量管理测试组</span><span class="sxs-lookup"><span data-stu-id="cb95f-143">Quality management test groups</span></span>](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
