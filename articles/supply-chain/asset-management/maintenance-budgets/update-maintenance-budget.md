---
title: 更新维护预算
description: 本主题说明如何在资产管理中更新维护预算。
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8f3b771319eeb602a371500fdc69c68f88afe341
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571729"
---
# <a name="update-maintenance-budgets"></a><span data-ttu-id="a4939-103">更新维护预算</span><span class="sxs-lookup"><span data-stu-id="a4939-103">Update maintenance budgets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="a4939-104">**维护预算行**页显示已经为**维护预算**页中选择的预算创建的所有预算行。</span><span class="sxs-lookup"><span data-stu-id="a4939-104">The **Maintenance budget lines** page shows all the budget lines that have been created for the budget that is selected on the **Maintenance budgets** page.</span></span> <span data-ttu-id="a4939-105">（有关详细信息，请参阅[创建维护预算](create-maintenance-budget.md)。）核准维护预算之前，可重新计算和调整维护预算行。</span><span class="sxs-lookup"><span data-stu-id="a4939-105">(For more information, see [Create maintenance budgets](create-maintenance-budget.md).) You can recalculate and adjust maintenance budget lines until the maintenance budget is approved.</span></span> <span data-ttu-id="a4939-106">预算期间过去，并且已经在资产管理中过帐了成本之后，还可以使用实际成本更新预算行。</span><span class="sxs-lookup"><span data-stu-id="a4939-106">After the budget period has passed, and costs have been posted in Asset Management, you can also update the budget lines with actual costs.</span></span>

## <a name="recalculate-a-maintenance-budget"></a><span data-ttu-id="a4939-107">重新计算维护预算</span><span class="sxs-lookup"><span data-stu-id="a4939-107">Recalculate a maintenance budget</span></span>

<span data-ttu-id="a4939-108">可以在**维护预算行**页中重新计算维护预算。</span><span class="sxs-lookup"><span data-stu-id="a4939-108">You can recalculate a maintenance budget on the **Maintenance budget lines** page.</span></span> <span data-ttu-id="a4939-109">重新计算维护预算时，将删除现有预算行，并完成新计算。</span><span class="sxs-lookup"><span data-stu-id="a4939-109">When you recalculate a maintenance budget, the existing budget lines are deleted, and a new calculation is done.</span></span>

1. <span data-ttu-id="a4939-110">在**维护预算行**页上，选择**重新计算**。</span><span class="sxs-lookup"><span data-stu-id="a4939-110">On the **Maintenance budget lines** page, select **Recalculate**.</span></span>
2. <span data-ttu-id="a4939-111">在**重新计算预算**对话框中，对新计算进行必需的更改，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="a4939-111">In the **Recalculate budget** dialog box, make the required changes for the new calculation, and then select **OK**.</span></span>

<span data-ttu-id="a4939-112">将根据您设置的值创建新预算行。</span><span class="sxs-lookup"><span data-stu-id="a4939-112">New budget lines are created according to the values that you set.</span></span>

## <a name="adjust-budget-lines"></a><span data-ttu-id="a4939-113">调整预算行</span><span class="sxs-lookup"><span data-stu-id="a4939-113">Adjust budget lines</span></span>

<span data-ttu-id="a4939-114">您可以调整与预算成本关联的所选行，而不是重新计算整个维护预算。</span><span class="sxs-lookup"><span data-stu-id="a4939-114">Instead of recalculating the whole maintenance budget, you can adjust selected lines that are related to budget costs.</span></span>

1. <span data-ttu-id="a4939-115">在**维护预算行**页上，选择要更新其预算成本的行。</span><span class="sxs-lookup"><span data-stu-id="a4939-115">On the **Maintenance budget lines** page, select the lines to update the budget cost for.</span></span>
2. <span data-ttu-id="a4939-116">选择**调整**。</span><span class="sxs-lookup"><span data-stu-id="a4939-116">Select **Adjust**.</span></span>
3. <span data-ttu-id="a4939-117">若要向所选行添加金额，请选中**添加成本**复选框，然后在**添加值**字段中输入值。</span><span class="sxs-lookup"><span data-stu-id="a4939-117">To add an amount to the selected lines, select the **Add cost** check box, and then enter the value in the **Add value** field.</span></span>
4. <span data-ttu-id="a4939-118">若要将所选预算行的预算成本乘以系数，请选中**乘以成本**复选框，然后在**乘以值**字段中输入系数。</span><span class="sxs-lookup"><span data-stu-id="a4939-118">To multiply the budget cost on the selected budget lines by a factor, select the **Multiply cost** check box, and enter the factor in the **Multiply value** field.</span></span>

    <span data-ttu-id="a4939-119">例如，如果在**乘以值**字段中输入 **1.2**，则所选行的预算成本增加 20%。</span><span class="sxs-lookup"><span data-stu-id="a4939-119">For example, if you enter **1.2** in the **Multiply value** field, you increase the budget cost on the selected lines by 20 percent.</span></span> <span data-ttu-id="a4939-120">如果输入 **0.7**，则所选行的预算成本减少 30%。</span><span class="sxs-lookup"><span data-stu-id="a4939-120">If you enter **0.7**, you reduce the budget cost on the selected lines by 30 percent.</span></span>

5. <span data-ttu-id="a4939-121">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="a4939-121">Select **OK**.</span></span>

<span data-ttu-id="a4939-122">将根据在步骤 3 或 4 中设置的值更新所选预算行。</span><span class="sxs-lookup"><span data-stu-id="a4939-122">The selected budget lines are updated according to the values that you set in step 3 or 4.</span></span>

## <a name="update-actual-costs"></a><span data-ttu-id="a4939-123">更新实际成本</span><span class="sxs-lookup"><span data-stu-id="a4939-123">Update actual costs</span></span>

<span data-ttu-id="a4939-124">预算行的日期过去，并且已经在资产管理中过帐了实际成本之后，可以更新维护预算的实际成本。</span><span class="sxs-lookup"><span data-stu-id="a4939-124">After the dates on the budget lines have passed, and actual costs have been posted in Asset Management, you can update the actual costs on the maintenance budget.</span></span>

1. <span data-ttu-id="a4939-125">在**维护预算行**页上，选择**更新成本**。</span><span class="sxs-lookup"><span data-stu-id="a4939-125">On the **Maintenance budget lines** page, select **Update cost**.</span></span>
2. <span data-ttu-id="a4939-126">在**计算实际成本**对话框中，选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="a4939-126">In the **Calculate actual cost** dialog box, select **OK**.</span></span>

<span data-ttu-id="a4939-127">如果已过帐实际成本，将更新预算行的**实际成本**字段。</span><span class="sxs-lookup"><span data-stu-id="a4939-127">The **Actual cost** fields on the budget lines are updated if actual costs have been posted.</span></span> <span data-ttu-id="a4939-128">如果在创建预算之后创建了新的资产类型，并且如果已经对为其创建了工作订单且为其过帐了关联的成本的资产使用了这些资产类型，可能会生成新预算行。</span><span class="sxs-lookup"><span data-stu-id="a4939-128">New budget lines might be generated if new asset types have been created since you created the budget, and if those asset types have been used on assets that work orders have been created for and related costs have been posted for.</span></span> <span data-ttu-id="a4939-129">新预算行仅显示实际成本，因为没有为其计算任何预算成本。</span><span class="sxs-lookup"><span data-stu-id="a4939-129">New budget lines show only actual costs, because no budget costs were calculated for them.</span></span>

> [!NOTE]
> <span data-ttu-id="a4939-130">若要查看拆分为预防性成本、纠正成本和投资成本的实际成本的概览，可以在**资产成本控制**页中为相同期间执行计算。</span><span class="sxs-lookup"><span data-stu-id="a4939-130">To see an overview of actual costs divided into preventive, corrective, and investment costs, you can do a calculation for the same period on the **Asset cost control** page.</span></span> 

## <a name="manually-add-budget-lines"></a><span data-ttu-id="a4939-131">手动添加预算行</span><span class="sxs-lookup"><span data-stu-id="a4939-131">Manually add budget lines</span></span>

<span data-ttu-id="a4939-132">在**维护预算行**页中，可通过选择**新建**，然后行中进行选择，手动添加新的预算行。</span><span class="sxs-lookup"><span data-stu-id="a4939-132">On the **Maintenance budget lines** page, you can manually add a new budget line by selecting **New** and then making selections on the line.</span></span> <span data-ttu-id="a4939-133">下面是这种方法可能有用的情况的一些示例：</span><span class="sxs-lookup"><span data-stu-id="a4939-133">Here are some examples of situations where this approach might be useful:</span></span>

- <span data-ttu-id="a4939-134">您知道某些资产的整修正处于规划阶段，但是尚未在资产管理中创建关联的作业。</span><span class="sxs-lookup"><span data-stu-id="a4939-134">You know that refurbishment of some assets is currently in the planning phase, but related jobs haven't yet been created in Asset Management.</span></span> <span data-ttu-id="a4939-135">但是，您希望维护预算中包括这些作业的预算成本。</span><span class="sxs-lookup"><span data-stu-id="a4939-135">However, you want budget costs for those jobs to be included in the maintenance budget.</span></span>
- <span data-ttu-id="a4939-136">在您创建维护预算之后已创建了新的资产或资产类型，但是尚未为这些资产或资产类型设置维护计划。</span><span class="sxs-lookup"><span data-stu-id="a4939-136">New assets or asset types have been created since you made the maintenance budget, but maintenance plans haven't yet been set up on those assets or asset types.</span></span> <span data-ttu-id="a4939-137">但是，您希望维护预算中包括这些资产类型的预算成本。</span><span class="sxs-lookup"><span data-stu-id="a4939-137">However, you want budget costs for those asset types to be included in the maintenance budget.</span></span>
