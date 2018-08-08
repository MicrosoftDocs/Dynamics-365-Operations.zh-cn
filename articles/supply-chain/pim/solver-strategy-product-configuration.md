---
title: "产品配置的求解器策略"
description: "此主题介绍如何使用求解器策略改进产品配置的性能。"
author: cvocph
manager: AnnBe
ms.date: 01/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCCreateProductConfigurationModel, PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: 
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: d0abb9313ec62cfdfe3bf7c810e2143dcf502bf9
ms.contentlocale: zh-cn
ms.lasthandoff: 08/07/2018

---

# <a name="solver-strategy-for-product-configuration"></a><span data-ttu-id="36e4c-103">产品配置的求解器策略</span><span class="sxs-lookup"><span data-stu-id="36e4c-103">Solver strategy for product configuration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="36e4c-104">此主题介绍如何使用求解器策略改进产品配置的性能。</span><span class="sxs-lookup"><span data-stu-id="36e4c-104">This topic describes how you can use the solver strategy to improve the performance of product configuration.</span></span>

<span data-ttu-id="36e4c-105">求解器这一概念最初是在 Microsoft Dynamics AX 2012 R2 的累积更新 7 (CU7) 中引入的。</span><span class="sxs-lookup"><span data-stu-id="36e4c-105">The concept of solver strategies was first introduced in Cumulative update 7 (CU7) for Microsoft Dynamics AX 2012 R2.</span></span> <span data-ttu-id="36e4c-106">并在 Microsoft Dynamics AX 2012 R3 的累积更新 8 (CU8) 和 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.3 中得以延伸。</span><span class="sxs-lookup"><span data-stu-id="36e4c-106">It was extended in Cumulative update 8 (CU8) for Microsoft Dynamics AX 2012 R3 and Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.</span></span>

<span data-ttu-id="36e4c-107">求解器策略概念现在包含以下策略：</span><span class="sxs-lookup"><span data-stu-id="36e4c-107">The solver strategy concept now consists of the following strategies:</span></span>

- <span data-ttu-id="36e4c-108">默认</span><span class="sxs-lookup"><span data-stu-id="36e4c-108">Default</span></span>
- <span data-ttu-id="36e4c-109">最小域数量优先</span><span class="sxs-lookup"><span data-stu-id="36e4c-109">Minimal domains first</span></span>
- <span data-ttu-id="36e4c-110">自上而下</span><span class="sxs-lookup"><span data-stu-id="36e4c-110">Top-down</span></span>
- <span data-ttu-id="36e4c-111">Z3</span><span class="sxs-lookup"><span data-stu-id="36e4c-111">Z3</span></span>

## <a name="solver-strategy"></a><span data-ttu-id="36e4c-112">求解器策略</span><span class="sxs-lookup"><span data-stu-id="36e4c-112">Solver strategy</span></span> 

<span data-ttu-id="36e4c-113">可将产品配置模型编制为[约束满足问题 (CSP)](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf)。</span><span class="sxs-lookup"><span data-stu-id="36e4c-113">A product configuration model can be formulated as a [constraint satisfaction problem (CSP)](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf).</span></span> <span data-ttu-id="36e4c-114">Microsoft Solver Foundation (MSF) 提供两种类型的求解器策略来解决可从产品配置模型使用的 CSP。</span><span class="sxs-lookup"><span data-stu-id="36e4c-114">Microsoft Solver Foundation (MSF) provides two types of solver strategies to solve the CSPs that can be used from product configuration models.</span></span> <span data-ttu-id="36e4c-115">这些求解器策略依赖于[启发](https://techterms.com/definition/heuristic)，启发用于确定解决问题时考虑 CSP 变量的顺序。</span><span class="sxs-lookup"><span data-stu-id="36e4c-115">These solver strategies rely on [heuristics](https://techterms.com/definition/heuristic), which are used to determine the order that the variables of the CSPs are considered in when the problem is being solved.</span></span> <span data-ttu-id="36e4c-116">解决一个问题或一类问题时，启发可显著影响性能。</span><span class="sxs-lookup"><span data-stu-id="36e4c-116">Heuristics can significantly affect performance when a problem or class of problems is being solved.</span></span>

<span data-ttu-id="36e4c-117">在 Finance and Operations 中，产品配置模型的求解器策略确定启发使用哪个求解器。</span><span class="sxs-lookup"><span data-stu-id="36e4c-117">In Finance and Operations, the solver strategy for product configuration models determines which solver is used with heuristics.</span></span> <span data-ttu-id="36e4c-118">**默认**、**最小域数量优先**和**自上而下**策略使用 MSF 中的两个求解器，而 **Z3** 策略则使用 Z3 求解器。</span><span class="sxs-lookup"><span data-stu-id="36e4c-118">The **Default**, **Minimal domains first**, and **Top-down** strategies use the two solvers from MSF, whereas the **Z3** strategy uses the Z3 solver.</span></span> 

<span data-ttu-id="36e4c-119">真实的客户实施研究已表明产品配置模型的求解器策略中的更改可将响应时间从以分钟计缩短到以毫秒计。</span><span class="sxs-lookup"><span data-stu-id="36e4c-119">Real customer implementation studies have shown that a change in the solver strategy for a product configuration model can reduce the response time from minutes to milliseconds.</span></span> <span data-ttu-id="36e4c-120">因此，值得努力尝试不同求解器策略以找出对产品配置模型效率最高的策略。</span><span class="sxs-lookup"><span data-stu-id="36e4c-120">Therefore, it's worth the effort to try different solver strategies to find the most efficient strategy for your product configuration model.</span></span>

## <a name="change-the-settings-for-the-solver-strategy"></a><span data-ttu-id="36e4c-121">更改求解器策略的设置</span><span class="sxs-lookup"><span data-stu-id="36e4c-121">Change the settings for the solver strategy</span></span>

<span data-ttu-id="36e4c-122">若要更改求解器策略，请在**配置产品模型**页面中的操作窗格上，选择**模型属性**。</span><span class="sxs-lookup"><span data-stu-id="36e4c-122">To change the solver strategy, on the **Product configuration models** page, on the Action Pane, select **Model properties**.</span></span> <span data-ttu-id="36e4c-123">然后，在**编辑模型详细信息**对话框中，选择求解器策略。</span><span class="sxs-lookup"><span data-stu-id="36e4c-123">Then, in the **Edit the model details** dialog box, select a solver strategy.</span></span>

<span data-ttu-id="36e4c-124">[![更改求解器策略](./media/solver-strategy.png)](./media/solver-strategy.png)</span><span class="sxs-lookup"><span data-stu-id="36e4c-124">[![Changing the solver strategy](./media/solver-strategy.png)](./media/solver-strategy.png)</span></span>

<span data-ttu-id="36e4c-125">目前不存在自动检测哪个求解器策略对基于约束的产品配置效率最高的逻辑。</span><span class="sxs-lookup"><span data-stu-id="36e4c-125">Currently, there is no logic that automatically detects which solver strategy will be the most efficient strategy for constraint-based product configuration.</span></span> <span data-ttu-id="36e4c-126">因此，必须逐一尝试求解器策略。</span><span class="sxs-lookup"><span data-stu-id="36e4c-126">Therefore, you must try the solver strategies one by one.</span></span>

<span data-ttu-id="36e4c-127">下表提供有关各种方案中要使用的求解器策略的建议。</span><span class="sxs-lookup"><span data-stu-id="36e4c-127">The following table provides recommendations about the solver strategy to use in various scenarios.</span></span>

| <span data-ttu-id="36e4c-128">求解器策略</span><span class="sxs-lookup"><span data-stu-id="36e4c-128">Solver strategy</span></span>      | <span data-ttu-id="36e4c-129">策略的使用方案</span><span class="sxs-lookup"><span data-stu-id="36e4c-129">Use the strategy in this scenario</span></span> |
|----------------------|-----------------------------------|
| <span data-ttu-id="36e4c-130">默认</span><span class="sxs-lookup"><span data-stu-id="36e4c-130">Default</span></span>              | <span data-ttu-id="36e4c-131">**默认**策略已经过优化，可解决依赖于表约束的模型。</span><span class="sxs-lookup"><span data-stu-id="36e4c-131">The **Default** strategy has been optimized to solve models that rely on table constraints.</span></span> <span data-ttu-id="36e4c-132">客户实施研究已表明，在广泛使用表约束的方案中，此策略效率最高。</span><span class="sxs-lookup"><span data-stu-id="36e4c-132">Customer implementation studies have shown that this strategy is the most efficient strategy in scenarios where table constraints are used extensively.</span></span> |
| <span data-ttu-id="36e4c-133">最小域数量优先</span><span class="sxs-lookup"><span data-stu-id="36e4c-133">Minimal domain first</span></span> | <span data-ttu-id="36e4c-134">**最小域数量优先**和**自上而下**策略之间的关系非常密切。</span><span class="sxs-lookup"><span data-stu-id="36e4c-134">The **Minimal domain first** and **Top-down** strategies are closely related.</span></span> <span data-ttu-id="36e4c-135">客户实施研究已表明 CU8 中引入的**自上而下**策略比**最小域数量优先**策略更优秀。</span><span class="sxs-lookup"><span data-stu-id="36e4c-135">Customer implementation studies have shown that the **Top-down** strategy, which was introduced in CU8, outperforms the **Minimal domain first** strategy.</span></span> <span data-ttu-id="36e4c-136">但是，产品中仍然保留了**最小域数量优先**策略，以提供向后兼容。</span><span class="sxs-lookup"><span data-stu-id="36e4c-136">However, the **Minimal domain first** strategy is kept in the product for backward compatibility.</span></span> <span data-ttu-id="36e4c-137">研究已表明，在求解其中包含多个不使用表约束的算术表达式的模型时，这两种求解器策略的效率更高。</span><span class="sxs-lookup"><span data-stu-id="36e4c-137">Both these solver strategies have been shown to be more efficient at solving models that contain several arithmetic expressions where no table constraints are used.</span></span> <span data-ttu-id="36e4c-138">但是在某些情况下，**默认**策略比这两个策略更优秀。</span><span class="sxs-lookup"><span data-stu-id="36e4c-138">However, in some cases, the **Default** strategy outperforms these two strategies.</span></span> <span data-ttu-id="36e4c-139">因此，请务必尝试每个策略。</span><span class="sxs-lookup"><span data-stu-id="36e4c-139">Therefore, remember to try each strategy.</span></span> |
| <span data-ttu-id="36e4c-140">自上而下</span><span class="sxs-lookup"><span data-stu-id="36e4c-140">Top-down</span></span>             | <span data-ttu-id="36e4c-141">**最小域数量优先**和**自上而下**策略之间的关系非常密切。</span><span class="sxs-lookup"><span data-stu-id="36e4c-141">The **Minimal domain first** and **Top-down** strategies are closely related.</span></span> <span data-ttu-id="36e4c-142">客户实施研究已表明 CU8 中引入的**自上而下**策略比**最小域数量优先**策略更优秀。</span><span class="sxs-lookup"><span data-stu-id="36e4c-142">Customer implementation studies have shown that the **Top-down** strategy, which was introduced in CU8, outperforms the **Minimal domain first** strategy.</span></span> <span data-ttu-id="36e4c-143">但是，产品中仍然保留了**最小域数量优先**策略，以提供向后兼容。</span><span class="sxs-lookup"><span data-stu-id="36e4c-143">However, the **Minimal domain first** strategy is kept in the product for backward compatibility.</span></span> <span data-ttu-id="36e4c-144">研究已表明，在求解其中包含多个不使用表约束的算术表达式的模型时，这两种求解器策略的效率更高。</span><span class="sxs-lookup"><span data-stu-id="36e4c-144">Both these solver strategies have been shown to be more efficient at solving models that contain several arithmetic expressions where no table constraints are used.</span></span> <span data-ttu-id="36e4c-145">但是在某些情况下，**默认**策略比这两个策略更优秀。</span><span class="sxs-lookup"><span data-stu-id="36e4c-145">However, in some cases, the **Default** strategy outperforms these two strategies.</span></span> <span data-ttu-id="36e4c-146">因此，请务必尝试每个策略。</span><span class="sxs-lookup"><span data-stu-id="36e4c-146">Therefore, remember to try each strategy.</span></span> |
| <span data-ttu-id="36e4c-147">Z3</span><span class="sxs-lookup"><span data-stu-id="36e4c-147">Z3</span></span>                   | <span data-ttu-id="36e4c-148">建议您将 **Z3** 策略用作默认求解器策略。</span><span class="sxs-lookup"><span data-stu-id="36e4c-148">We recommend that you use the **Z3** strategy as the default solver strategy.</span></span> <span data-ttu-id="36e4c-149">如果您注重性能和可扩展性，则可评估其他策略。</span><span class="sxs-lookup"><span data-stu-id="36e4c-149">If you're concerned about performance and scalability, you can evaluate the other strategies.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="36e4c-150">其他资源</span><span class="sxs-lookup"><span data-stu-id="36e4c-150">Additional resources</span></span>

[<span data-ttu-id="36e4c-151">生成产品配置模型</span><span class="sxs-lookup"><span data-stu-id="36e4c-151">Build product configuration model</span></span>](build-product-configuration-model.md)

[<span data-ttu-id="36e4c-152">启发</span><span class="sxs-lookup"><span data-stu-id="36e4c-152">Heuristics</span></span>](https://techterms.com/definition/heuristic)

[<span data-ttu-id="36e4c-153">约束满足问题</span><span class="sxs-lookup"><span data-stu-id="36e4c-153">Constraint Satisfaction Problem</span></span>](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf)

