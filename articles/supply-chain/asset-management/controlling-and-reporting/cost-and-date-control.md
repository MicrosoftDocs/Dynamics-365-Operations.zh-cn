---
title: 成本和日期控制
description: 本主题介绍资产管理中的成本和日期控制。
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2bcd1584f6a858f7589387fbfe96267b7c16176a
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918387"
---
# <a name="cost-and-date-control"></a><span data-ttu-id="5fca2-103">成本和日期控制</span><span class="sxs-lookup"><span data-stu-id="5fca2-103">Cost and date control</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="5fca2-104">在资产管理中，可计算成本，以便获取资产、功能位置和工作订单的实际成本与预算成本的比较概览。</span><span class="sxs-lookup"><span data-stu-id="5fca2-104">In Asset Management, you can calculate costs to get an overview of actual costs compared to budget costs on assets, functional locations, and work orders.</span></span> <span data-ttu-id="5fca2-105">实际成本基于过帐的交易记录。</span><span class="sxs-lookup"><span data-stu-id="5fca2-105">Actual costs are based on posted transactions.</span></span> <span data-ttu-id="5fca2-106">如果要将工作订单的计划开始日期和结束日期与实际开始日期和结束日期进行比较，也可以创建日期计算。</span><span class="sxs-lookup"><span data-stu-id="5fca2-106">You can also make a date calculation if you want to compare scheduled start and end dates to actual start and end dates on work orders.</span></span>

## <a name="cost-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="5fca2-107">资产、功能位置和工作订单的成本控制</span><span class="sxs-lookup"><span data-stu-id="5fca2-107">Cost control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="5fca2-108">为资产、功能位置和工作订单创建的计算几乎相同。</span><span class="sxs-lookup"><span data-stu-id="5fca2-108">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="5fca2-109">唯一区别是，对于资产和功能位置，还可以在计算中包括子资产和子位置。</span><span class="sxs-lookup"><span data-stu-id="5fca2-109">Only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="5fca2-110">日期是记录登记时的交易记录日期。</span><span class="sxs-lookup"><span data-stu-id="5fca2-110">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="5fca2-111">单击**资产管理** > **查询** > **资产** > **资产成本控制**或**功能位置成本控制**，或**资产管理** > **查询** > **工作订单** > **工作订单成本控制**。</span><span class="sxs-lookup"><span data-stu-id="5fca2-111">Click **Asset management** > **Inquiries** > **Assets** > **Asset cost control** or **Functional location cost control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order cost control**.</span></span>

2. <span data-ttu-id="5fca2-112">在**资产成本控制** / **功能位置成本控制** / **工作订单成本控制**对话框中，选择要计算的期间。</span><span class="sxs-lookup"><span data-stu-id="5fca2-112">In the **Asset cost control** / **Functional location cost control** / **Work order cost control** dialog, select a period to be calculated.</span></span>

3. <span data-ttu-id="5fca2-113">如果需要，选择计算中要包括的财务维度集。</span><span class="sxs-lookup"><span data-stu-id="5fca2-113">If required, select a financial dimension set to be included in the calculation.</span></span>

4. <span data-ttu-id="5fca2-114">如果不希望显示包含零成本的结果，请在**忽略零**切换按钮上选择“是”。</span><span class="sxs-lookup"><span data-stu-id="5fca2-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="5fca2-115">可使用**级别**字段指示要与功能位置有关的成本控制行的详细程度。</span><span class="sxs-lookup"><span data-stu-id="5fca2-115">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> <span data-ttu-id="5fca2-116">例如，如果在字段中插入数字“1”，并且采用了多级别功能位置层次结构，则将在最上级别显示某个功能位置的所有成本控制行，因此，可以从较低级别的功能位置叠加行中的工时。</span><span class="sxs-lookup"><span data-stu-id="5fca2-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="5fca2-117">如果在**级别**字段中插入数字“0”，将看到详细结果，其中显示其关联的所有功能位置级别的所有成本控制行。</span><span class="sxs-lookup"><span data-stu-id="5fca2-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all cost control lines on all the functional location level to which they are related.</span></span>

6. <span data-ttu-id="5fca2-118">如果要在计算中包括该列，请在**显示未结承诺成本**切换按钮上选择“是”。</span><span class="sxs-lookup"><span data-stu-id="5fca2-118">Select "Yes" on the **Show open committed cost** toggle button if you want to include that column in the calculation.</span></span>

7. <span data-ttu-id="5fca2-119">若要将与子资产关联的成本显示为单独行，请在**包括子资产**切换按钮上选择“是”。</span><span class="sxs-lookup"><span data-stu-id="5fca2-119">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="5fca2-120">如果要限制搜索，可在**要包括的记录**快速选项卡上选择特定资产/功能位置/工作订单。</span><span class="sxs-lookup"><span data-stu-id="5fca2-120">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="5fca2-121">单击**确定**开始计算。</span><span class="sxs-lookup"><span data-stu-id="5fca2-121">Click **OK** to start the calculation.</span></span>

<span data-ttu-id="5fca2-122">下图显示**资产成本控制**对话框的示例。</span><span class="sxs-lookup"><span data-stu-id="5fca2-122">The figure below shows an example of the **Asset cost control** dialog.</span></span>

![图 1](media/01-controlling-and-reporting.png)

10. <span data-ttu-id="5fca2-124">在**资产成本控制**页上的**分组依据**操作窗格组中，单击相关按钮显示计算的所需详细程度。</span><span class="sxs-lookup"><span data-stu-id="5fca2-124">In the **Group by...** action pane groups on the **Asset cost control** page, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="5fca2-125">将突出显示所选操作窗格按钮。</span><span class="sxs-lookup"><span data-stu-id="5fca2-125">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="5fca2-126">单击按钮将其激活或停用。</span><span class="sxs-lookup"><span data-stu-id="5fca2-126">Click on a button to activate or deactivate it.</span></span>

<span data-ttu-id="5fca2-127">下图显示**资产成本控制**中的计算结果的示例。</span><span class="sxs-lookup"><span data-stu-id="5fca2-127">The figure below shows an example of calculation results in **Asset cost control**.</span></span>

![图 2](media/02-controlling-and-reporting.png)

<span data-ttu-id="5fca2-129">另外一种创建成本计算的方法是在**所有资产**或**有效资产**中选择多个资产。</span><span class="sxs-lookup"><span data-stu-id="5fca2-129">Another way of making a cost calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="5fca2-130">然后，单击**常规**选项卡上的**成本控制**按钮。在**资产成本控制**对话框中，将把所选资产自动插入到**要包括的记录**快速选项卡上的**资产**字段中。</span><span class="sxs-lookup"><span data-stu-id="5fca2-130">Then, you click the **Cost control** button on the **General** tab. In the **Asset cost control** dialog, the selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="5fca2-131">单击**确定**，然后将显示所选资产的成本计算。</span><span class="sxs-lookup"><span data-stu-id="5fca2-131">Click **OK**, and a cost calculation for the selected assets is shown.</span></span> <span data-ttu-id="5fca2-132">可以在**所有功能位置**或**有效功能位置**中对功能位置执行同样的过程，也可以在**所有工作订单**或**有效工作订单**中对工作订单执行同样的过程。</span><span class="sxs-lookup"><span data-stu-id="5fca2-132">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>

>[!NOTE]
><span data-ttu-id="5fca2-133">**原始预算**字段显示工作订单预测中的预算成本。</span><span class="sxs-lookup"><span data-stu-id="5fca2-133">The **Original budget** field shows budget costs from the work order forecast.</span></span> <span data-ttu-id="5fca2-134">**承诺成本**字段显示法人自行承诺支付的费用总额。</span><span class="sxs-lookup"><span data-stu-id="5fca2-134">The **Committed cost** field shows the total amount of expenses that a legal entity has committed itself to pay.</span></span> <span data-ttu-id="5fca2-135">**未结承诺成本**字段显示对要为您已订购或收到，但尚未付款的物料、工时和服务的付款承诺。</span><span class="sxs-lookup"><span data-stu-id="5fca2-135">The **Open committed cost** field shows commitments to pay for items, hours, and services you have ordered or received but not yet paid for.</span></span> <span data-ttu-id="5fca2-136">过帐了所有消耗登记之后，**实际成本**字段中将包括相关成本。</span><span class="sxs-lookup"><span data-stu-id="5fca2-136">When all consumption registrations have been posted, the related costs are included in the **Actual cost** field.</span></span>

## <a name="work-order-date-control"></a><span data-ttu-id="5fca2-137">工作订单日期控制</span><span class="sxs-lookup"><span data-stu-id="5fca2-137">Work order date control</span></span>

<span data-ttu-id="5fca2-138">此页用于获取工作订单的预计开始日期和结束日期与实际开始日期和结束日期的比较概览。</span><span class="sxs-lookup"><span data-stu-id="5fca2-138">Use this page to get an overview of expected start and end dates compared to actual start and end dates on work orders.</span></span>

1. <span data-ttu-id="5fca2-139">单击**资产管理** > **查询** > **工作订单** > **工作订单日期控制**。</span><span class="sxs-lookup"><span data-stu-id="5fca2-139">Click **Asset management** > **Inquiries** > **Work orders** > **Work order date control**.</span></span>

2. <span data-ttu-id="5fca2-140">单击**计算**。</span><span class="sxs-lookup"><span data-stu-id="5fca2-140">Click **Calculate**.</span></span>

3. <span data-ttu-id="5fca2-141">在**功能位置**字段中选择一个功能位置。</span><span class="sxs-lookup"><span data-stu-id="5fca2-141">Select a functional location in the **Functional location** field.</span></span>

4. <span data-ttu-id="5fca2-142">在**开始日期**和**结束日期**字段中插入要为其创建计算的期间。</span><span class="sxs-lookup"><span data-stu-id="5fca2-142">Insert the period for which you want to make the calculation in the **From date** and **To date** fields.</span></span> <span data-ttu-id="5fca2-143">将包括预计在该期间开始的所有工作订单。</span><span class="sxs-lookup"><span data-stu-id="5fca2-143">All work orders with expected start within the period will be included.</span></span>

5. <span data-ttu-id="5fca2-144">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="5fca2-144">Click **OK**.</span></span>

6. <span data-ttu-id="5fca2-145">在**分组依据**操作窗格组中，单击相关按钮显示所需成本计算详细程度。</span><span class="sxs-lookup"><span data-stu-id="5fca2-145">In the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="5fca2-146">将突出显示所选操作窗格按钮。</span><span class="sxs-lookup"><span data-stu-id="5fca2-146">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="5fca2-147">单击按钮将其激活或停用。</span><span class="sxs-lookup"><span data-stu-id="5fca2-147">Click on a button to activate or deactivate it.</span></span>

<span data-ttu-id="5fca2-148">下图显示**工作订单日期控制**中的计算结果的示例。</span><span class="sxs-lookup"><span data-stu-id="5fca2-148">The figure below shows an example of calculation results in **Work order date control**.</span></span>

![图 3](media/03-controlling-and-reporting.png)

- <span data-ttu-id="5fca2-150">**平均开始延迟**字段显示工作订单的计划开始日期与实际开始日期之间的天数。</span><span class="sxs-lookup"><span data-stu-id="5fca2-150">The **Avg. start delay** field shows the difference in days between scheduled start date for a work order compared to actual start date.</span></span> <span data-ttu-id="5fca2-151">例如，如果实际开始日期在计划开始日期的两天前，则此字段中将显示“-2”。</span><span class="sxs-lookup"><span data-stu-id="5fca2-151">If, for example, the actual start date was two days before the scheduled start date, "-2" will be displayed in this field.</span></span>  
- <span data-ttu-id="5fca2-152">**平均结束延迟**字段显示工作订单的计划结束日期与实际结束日期之间的天数。</span><span class="sxs-lookup"><span data-stu-id="5fca2-152">The **Avg. end delay** field shows the difference in days between scheduled end date for a work order compared to actual end date.</span></span> <span data-ttu-id="5fca2-153">例如，如果实际结束日期在计划结束日期的三天后，则此字段中将显示“3”。</span><span class="sxs-lookup"><span data-stu-id="5fca2-153">If, for example, the actual end date was three days after the scheduled end date, "3" will be displayed in this field.</span></span>  
- <span data-ttu-id="5fca2-154">**发生次数**字段显示工作订单的计划开始日期与实际开始日期之间和计划结束日期与实际结束日期之间发生偏差的次数。</span><span class="sxs-lookup"><span data-stu-id="5fca2-154">The **Occurrences** fields show the number of times deviations occur in relation to scheduled and actual start date, and scheduled and actual end date on the work order.</span></span>

