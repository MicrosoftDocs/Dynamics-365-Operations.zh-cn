---
title: 产品配置器疑难解答
description: 此主题介绍如何解决使用产品配置器时可能遇到的问题。
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e6cfeb6a2b4166dfa9a5a5cc1b7d3d913b865ce2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999598"
---
# <a name="troubleshoot-the-product-configurator"></a><span data-ttu-id="07433-103">产品配置器疑难解答</span><span class="sxs-lookup"><span data-stu-id="07433-103">Troubleshoot the product configurator</span></span>

<span data-ttu-id="07433-104">此主题介绍如何解决使用产品配置器时可能遇到的问题。</span><span class="sxs-lookup"><span data-stu-id="07433-104">This topic describes how to fix issues that you might encounter while you work with the product configurator.</span></span>

## <a name="item-text-is-overwritten-when-i-configure-a-product-on-a-sales-order-line"></a><span data-ttu-id="07433-105">当我在销售订单行上配置产品时，物料文本会被覆盖。</span><span class="sxs-lookup"><span data-stu-id="07433-105">Item text is overwritten when I configure a product on a sales order line.</span></span>

### <a name="issue-description"></a><span data-ttu-id="07433-106">问题描述</span><span class="sxs-lookup"><span data-stu-id="07433-106">Issue description</span></span>

<span data-ttu-id="07433-107">当您为可配置物料创建销售订单行，然后修改物料文本时，会发生此问题。</span><span class="sxs-lookup"><span data-stu-id="07433-107">This issue occurs when you create a sales order line for a configurable item and then modify the item text.</span></span> <span data-ttu-id="07433-108">当您配置物料，然后选择 **确定** 时，文本会被标准文本覆盖。</span><span class="sxs-lookup"><span data-stu-id="07433-108">When you configure the item and then select **OK**, the text is overwritten with the standard text.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="07433-109">解决问题</span><span class="sxs-lookup"><span data-stu-id="07433-109">Issue resolution</span></span>

<span data-ttu-id="07433-110">此行为是预期的。</span><span class="sxs-lookup"><span data-stu-id="07433-110">This behavior is expected.</span></span> <span data-ttu-id="07433-111">文本字段包含变型名称，仅在您配置行后填充。</span><span class="sxs-lookup"><span data-stu-id="07433-111">The text field includes the variant name, which is filled in only after you configure the line.</span></span> <span data-ttu-id="07433-112">因此，您必须在配置行之后而不是在之前更改文本。</span><span class="sxs-lookup"><span data-stu-id="07433-112">Therefore, you must change the text after you've configured the line, not before.</span></span>

## <a name="integer-attributes-are-incorrectly-rounded-when-product-configuration-models-are-calculated"></a><span data-ttu-id="07433-113">计算产品配置模型时，整数属性舍入不正确。</span><span class="sxs-lookup"><span data-stu-id="07433-113">Integer attributes are incorrectly rounded when product configuration models are calculated.</span></span>

### <a name="issue-description"></a><span data-ttu-id="07433-114">问题描述</span><span class="sxs-lookup"><span data-stu-id="07433-114">Issue description</span></span>

<span data-ttu-id="07433-115">当您执行以下一系列操作时，可能会发生此问题：</span><span class="sxs-lookup"><span data-stu-id="07433-115">This issue can occur when you perform the following series of actions:</span></span>

1. <span data-ttu-id="07433-116">在生产配置模型上设置以下属性：</span><span class="sxs-lookup"><span data-stu-id="07433-116">Set up the following attributes on a production configuration model:</span></span>

    - <span data-ttu-id="07433-117">Input（整数）</span><span class="sxs-lookup"><span data-stu-id="07433-117">Input (integer)</span></span>
    - <span data-ttu-id="07433-118">Percent（十进制）</span><span class="sxs-lookup"><span data-stu-id="07433-118">Percent (decimal)</span></span>
    - <span data-ttu-id="07433-119">Result（整数）</span><span class="sxs-lookup"><span data-stu-id="07433-119">Result (integer)</span></span>

2. <span data-ttu-id="07433-120">创建具有以下表达式的计算：</span><span class="sxs-lookup"><span data-stu-id="07433-120">Create a calculation that has the following expression:</span></span>

    <span data-ttu-id="07433-121">*Result* = *Input* × *Percent* ÷ 100</span><span class="sxs-lookup"><span data-stu-id="07433-121">*Result* = *Input* × *Percent* ÷ 100</span></span>

<span data-ttu-id="07433-122">在这种情况下，整数结果并不总是会正确舍入。</span><span class="sxs-lookup"><span data-stu-id="07433-122">In this case, the integer result isn't always correctly rounded.</span></span> <span data-ttu-id="07433-123">例如，输入为 1,000，百分比为 2.40。</span><span class="sxs-lookup"><span data-stu-id="07433-123">For example, the input is 1,000, and the percentage is 2.40.</span></span> <span data-ttu-id="07433-124">因此，整数结果应为 24，因为 1,000 的 2.40% 为 24（或十进制形式的 24.00）。</span><span class="sxs-lookup"><span data-stu-id="07433-124">Therefore, you expect the integer result to be 24, because 2.40 percent of 1,000 is 24 (or 24.00 in decimal form).</span></span> <span data-ttu-id="07433-125">而结果显示为 23。</span><span class="sxs-lookup"><span data-stu-id="07433-125">Instead, the result is shown as 23.</span></span> <span data-ttu-id="07433-126">但是，当百分比为 2.39 时，计算将舍入到 24 而不是 23。</span><span class="sxs-lookup"><span data-stu-id="07433-126">However, when the percentage is 2.39, the calculation is rounded to 24 instead of 23.</span></span> <span data-ttu-id="07433-127">当百分比为 2.50 时，计算将按预期舍入到 25。</span><span class="sxs-lookup"><span data-stu-id="07433-127">When the percentage is 2.50, the calculation is rounded to 25, as expected.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="07433-128">解决问题</span><span class="sxs-lookup"><span data-stu-id="07433-128">Issue resolution</span></span>

<span data-ttu-id="07433-129">发生此问题的原因是 Microsoft Solver Foundation 内部使用分数表示数字。</span><span class="sxs-lookup"><span data-stu-id="07433-129">This issue occurs because of the way that Microsoft Solver Foundation internally represents numbers by using fractions.</span></span> <span data-ttu-id="07433-130">对于前面的示例，百分比为 2.40 的计算结果表示为 27021597764222975 ÷ 1125899906842624 = 23.99999999999999911182158029987476766109466552734375。</span><span class="sxs-lookup"><span data-stu-id="07433-130">For the preceding example, the result of the calculation where the percentage is 2.40 is represented as 27021597764222975 ÷ 1125899906842624 = 23.99999999999999911182158029987476766109466552734375.</span></span> <span data-ttu-id="07433-131">当 .NET 将此值计算为整数时，将返回 23。</span><span class="sxs-lookup"><span data-stu-id="07433-131">When .NET casts this value as an integer, it will return 23.</span></span>

<span data-ttu-id="07433-132">此行为将不会更改，因为其他场景要依赖于此行为。</span><span class="sxs-lookup"><span data-stu-id="07433-132">This behavior won't be changed, because other scenarios depend on it.</span></span> <span data-ttu-id="07433-133">对于前面的示例，您可以通过引入其他十进制属性和计算来解决此问题。</span><span class="sxs-lookup"><span data-stu-id="07433-133">For the preceding example, you can fix the issue by introducing an additional decimal attribute and a calculation.</span></span>

<span data-ttu-id="07433-134">例如，您可以在生产配置模型上设置以下属性：</span><span class="sxs-lookup"><span data-stu-id="07433-134">For example, you can set up the following attributes on a production configuration model:</span></span>

- <span data-ttu-id="07433-135">Input（整数）</span><span class="sxs-lookup"><span data-stu-id="07433-135">Input (integer)</span></span>
- <span data-ttu-id="07433-136">Percent（十进制）</span><span class="sxs-lookup"><span data-stu-id="07433-136">Percent (decimal)</span></span>
- <span data-ttu-id="07433-137">ResultDecimal（十进制）</span><span class="sxs-lookup"><span data-stu-id="07433-137">ResultDecimal (decimal)</span></span>
- <span data-ttu-id="07433-138">ResultInteger（整数）</span><span class="sxs-lookup"><span data-stu-id="07433-138">ResultInteger (integer)</span></span>

<span data-ttu-id="07433-139">然后，您可以添加以下计算：</span><span class="sxs-lookup"><span data-stu-id="07433-139">You can then add the following calculations:</span></span>

- <span data-ttu-id="07433-140">*ResultDecimal* = *Input* × *Percent* ÷ 100</span><span class="sxs-lookup"><span data-stu-id="07433-140">*ResultDecimal* = *Input* × *Percent* ÷ 100</span></span>
- <span data-ttu-id="07433-141">*ResultInteger* = *ResultDecimal*</span><span class="sxs-lookup"><span data-stu-id="07433-141">*ResultInteger* = *ResultDecimal*</span></span>
