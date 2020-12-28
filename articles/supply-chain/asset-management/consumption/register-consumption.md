---
title: 登记消耗
description: 本主题介绍如何在资产管理中登记消耗。
author: josaw1
manager: tfehr
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderJournal, EntAssetWorkOrderAddSparePart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2c9bbd51da23ea412bc124f932f73876a9506d47
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423112"
---
# <a name="register-consumption"></a><span data-ttu-id="0a0d6-103">登记消耗</span><span class="sxs-lookup"><span data-stu-id="0a0d6-103">Register consumption</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="0a0d6-104">为工作订单完成了维护作业之后，下一步是创建消耗登记和过帐日记帐。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-104">When a maintenance job has been completed on a work order, the next step is to make consumption registrations and post the journals.</span></span> <span data-ttu-id="0a0d6-105">可以为以下消耗类型创建登记：工时、物料和费用。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-105">You can make registrations on the following consumption types: Hours, items, and expenses.</span></span> <span data-ttu-id="0a0d6-106">将在 **工作订单日记帐** 页面中登记和过帐不同消耗类型。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-106">The different consumption types are registered and posted on the **Work order journals** page.</span></span> <span data-ttu-id="0a0d6-107">**资产管理** 中的日记帐设置用于在 **项目管理与核算** 模块中为工时、物料和费用分别创建和过帐日记帐。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-107">The journal setup in **Asset Management** is used for creating and posting separate journals for hours, items, and expenses in the **Project management and accounting** module.</span></span>

<span data-ttu-id="0a0d6-108">有些情况下，您可能可以在工作订单中添加或删除预测行。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-108">In some cases, you may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="0a0d6-109">对工作订单生命周期状态、关联的项目类型和与项目类型关联的阶段规则的设置决定是否可以添加或编辑日记帐行。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-109">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determine if you are able to add or edit journal lines.</span></span> <span data-ttu-id="0a0d6-110">在[预测、工作订单和项目](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md)中了解有关工作订单生命周期状态和相关的项目阶段的详细信息。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-110">Read more about work order lifecycle states and related project stages in [Forecasts, work orders, and projects](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

>[!NOTE]
><span data-ttu-id="0a0d6-111">可以为工作订单生命周期状态设置日记帐自动过帐。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-111">It is possible to set up automatic posting of journals on a work order lifecycle state.</span></span> <span data-ttu-id="0a0d6-112">有关详细信息，请参阅[工作订单生命周期状态](../setup-for-work-orders/work-order-lifecycle-states.md)。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-112">Refer to [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md) for more information.</span></span>

1. <span data-ttu-id="0a0d6-113">单击 **资产管理** > **常用** > **工作订单** > **所有工作订单** 或 **有效工作订单**。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-113">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="0a0d6-114">选择工作订单，然后单击 **日记帐**。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-114">Select the work order, and click **Journals**.</span></span>

3. <span data-ttu-id="0a0d6-115">单击 **从预测复制** 以传输可能与该工作订单关联的所有预测行。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-115">Click **Copy from forecast** to transfer any forecast lines that may be connected to the work order.</span></span> <span data-ttu-id="0a0d6-116">可以选择要传输哪些消耗类型。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-116">You can select which consumption types you want to transfer.</span></span>

4. <span data-ttu-id="0a0d6-117">如有必要，可通过单击 **添加行** 并在行中填写数据，在相关快速选项卡上添加更多消耗行。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-117">If necessary, you can add more consumption lines on the relevant FastTab by clicking **Add line** and filling out data on the line.</span></span>

5. <span data-ttu-id="0a0d6-118">单击 **验证日记帐**，以便在过帐前验证日记帐行。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-118">Click **Validate journals** to validate the journal lines before posting.</span></span>

6. <span data-ttu-id="0a0d6-119">单击 **日记帐过帐** 以过帐日记帐行。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-119">Click **Post journals** to post the journal lines.</span></span>

7. <span data-ttu-id="0a0d6-120">过帐消耗量日记帐后，您可以更新工作订单生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-120">After you've posted the consumption journals, you can update the work order lifecycle state.</span></span> <span data-ttu-id="0a0d6-121">例如，要指示工作订单已完成，可以将生命周期状态更新为“已结束”。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-121">For example, to indicate that the work order has been completed, you can update the lifecycle state to "Ended".</span></span>

    - <span data-ttu-id="0a0d6-122">在 **工作订单日记帐** 页顶部的 **显示** 字段中，选择要查看哪些日记帐行：**所有**、**未过帐** 或 **已过帐**。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-122">In the **Show** field at the top of the **Work order journals** page, select which journal lines you want to see: **All**, **Not posted**, or **Posted**.</span></span> <span data-ttu-id="0a0d6-123">已过帐日记帐在 **已过帐** 复选框中具有选中标记。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-123">Posted journals have a check mark in the **Posted** check box.</span></span>  
    - <span data-ttu-id="0a0d6-124">在工作订单日记帐中创建物料行之后，将把与物料关联的产品维度和跟踪维度自动传输到这个日记帐行。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-124">When item lines are created in the work order journal, product dimensions and tracking dimensions related to the item are automatically transferred to the journal line.</span></span>  

<span data-ttu-id="0a0d6-125">下面的屏幕截图显示 **工作订单日记帐** 中工作订单的工时和物料登记的示例。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-125">The screenshot below shows an example of hour and item registrations on a work order in **Work order journals**.</span></span>

![图 1](media/01-consumption.png)


## <a name="split-hours-on-work-orders-with-several-work-order-jobs"></a><span data-ttu-id="0a0d6-127">拆分具有多个工作订单作业的工作订单</span><span class="sxs-lookup"><span data-stu-id="0a0d6-127">Split hours on work orders with several work order jobs</span></span>

<span data-ttu-id="0a0d6-128">如果工作订单中包含多个工作订单作业，则可使用 **拆分工时** 功能登记工时，这意味着可以将一个工时登记行平均分配给每个工作订单作业。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-128">If a work order contains several work order jobs, you can register work hours using the **Split hours** functionality, meaning one hour registration line can be distributed evenly on each work order job.</span></span>

1. <span data-ttu-id="0a0d6-129">单击 **资产管理** > **常用** > **工作订单** > **所有工作订单** 或 **有效工作订单**。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-129">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="0a0d6-130">选择工作订单，然后单击 **日记帐**。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-130">Select the work order and click **Journals**.</span></span>

3. <span data-ttu-id="0a0d6-131">选择要拆分的工时登记行，然后单击 **拆分工时**。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-131">Select the hour registration line you want to split, and click **Split hours**.</span></span>

4. <span data-ttu-id="0a0d6-132">将在 **拆分工作订单维护作业的工时** 对话框的 **工人** 字段中自动显示已登录工人的姓名。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-132">In the **Split hours on work order maintenance jobs** dialog, the name of the worker who is logged in is automatically shown in the **Worker** field.</span></span> <span data-ttu-id="0a0d6-133">如果需要，可以选择其他工人。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-133">If required, you can select another worker.</span></span>

5. <span data-ttu-id="0a0d6-134">在 **类别** 字段中为工时登记选择类别。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-134">Select a category for the hour registration in the **Category** field.</span></span>

6. <span data-ttu-id="0a0d6-135">在 **工时** 字段中插入要拆分的工时数量。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-135">Insert number of work hours to be split in the **Hours** field.</span></span>

    ![图 2](media/02-consumption.png)

7. <span data-ttu-id="0a0d6-137">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-137">Click **OK**.</span></span>

<span data-ttu-id="0a0d6-138">*示例：* 在下面的屏幕截图中，显示了其中包含三个工作订单作业的工作订单的日记帐行。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-138">*Example:* In the screenshot below, journal lines for a work order containing three work order jobs are shown.</span></span> <span data-ttu-id="0a0d6-139">已拆分第一个行（其中包含三个工时），并为每个工作订单作业登记了一个工时。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-139">The first line, containing three work hours, has been split, and one work hour is registered on each work order job.</span></span> <span data-ttu-id="0a0d6-140">创建这三个工时登记行之后，您可以决定如何处理原始工时登记行（此示例中为第一个行）。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-140">After the three hour registration lines have been created, you decide what to do with the original hour registration line (the first line in the example).</span></span> <span data-ttu-id="0a0d6-141">可以将其保留原样或删除。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-141">You can keep it as is or delete it.</span></span> 

![图 3](media/03-consumption.png)

## <a name="financial-dimensions-on-consumption-registrations"></a><span data-ttu-id="0a0d6-143">消耗登记的财务维度</span><span class="sxs-lookup"><span data-stu-id="0a0d6-143">Financial dimensions on consumption registrations</span></span>

<span data-ttu-id="0a0d6-144">创建消耗登记时，将把与不同登记类型关联的财务维度按特定顺序添加到这些登记。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-144">When you make consumption registrations, financial dimensions related to the different registration types are added to the registrations in a specific sequence.</span></span> 

- <span data-ttu-id="0a0d6-145">*工时和费用登记：* 首先添加来自日记帐标题的财务维度（如果有）。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-145">*Hour and Expense registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="0a0d6-146">接下来添加来自关联的工作订单项目的财务维度。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-146">Next, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="0a0d6-147">最后添加来自资源（工人） 的财务维度。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-147">Finally, financial dimensions from the resource (worker) are added.</span></span>

- <span data-ttu-id="0a0d6-148">*物料登记：* 首先添加来自日记帐标题的财务维度（如果有）。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-148">*Item registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="0a0d6-149">然后添加来自关联的工作订单项目的财务维度。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-149">Then, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="0a0d6-150">接下来添加来自站点的财务维度。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-150">Next, financial dimensions from the site are added.</span></span> <span data-ttu-id="0a0d6-151">最后添加来自物料 的财务维度。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-151">Finally, financial dimensions from the item are added.</span></span>

>[!NOTE]
><span data-ttu-id="0a0d6-152">对于所有三种登记类型，都将验证财务维度组合，并且无效组合将为空。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-152">For all three registration types, the financial dimension combination is validated, and invalid combinations are blanked.</span></span> <span data-ttu-id="0a0d6-153">这是其他 Finance and Operations 应用的标准设置。</span><span class="sxs-lookup"><span data-stu-id="0a0d6-153">This is standard setup with other Finance and Operations apps.</span></span>

