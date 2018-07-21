---
title: "从 Project Service Automation 同步项目支出类别"
description: "本主题介绍用于在 Microsoft Dynamics 365 for Finance and Operations 与 Dynamics 365 for Project Service Automation 之间同步项目支出类别的模板和基础任务。"
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: dcdb9b6ec296073d511c069cdceb1c61080b6d97
ms.contentlocale: zh-cn
ms.lasthandoff: 05/29/2018

---

# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="aca45-103">在 Finance and Operations 与 Project Service Automation 之间同步项目支出类别</span><span class="sxs-lookup"><span data-stu-id="aca45-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

<span data-ttu-id="aca45-104">本主题介绍用于在 Microsoft Dynamics 365 for Finance and Operations 与 Dynamics 365 for Project Service Automation 之间同步项目支出类别的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="aca45-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Microsoft Dynamics 365 for Finance and Operations and Dynamics 365 for Project Service Automation.</span></span>

> [!NOTE]
> <span data-ttu-id="aca45-105">Dynamics 365 for Finance and Operations 版本 8.0 中提供项目任务集成、费用交易记录类别、工时估计值、费用估计值和功能锁定。</span><span class="sxs-lookup"><span data-stu-id="aca45-105">Project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Dynamics 365 for Finance and Operations version 8.0.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a><span data-ttu-id="aca45-106">Project Service Automation 和 Finance and Operations 之间的数据传输</span><span class="sxs-lookup"><span data-stu-id="aca45-106">Data flow for Project Service Automation and Finance and Operations</span></span>

<span data-ttu-id="aca45-107">Project Service Automation 与 Finance and Operations 集成解决方案使用数据集成功能在 Project Service Automation 和 Finance and Operations 的实例之间同步数据。</span><span class="sxs-lookup"><span data-stu-id="aca45-107">The Project Service Automation and Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="aca45-108">可通过数据集成功能提供的集成模板在 Finance and Operations 与 Project Service Automation 之间传输有关项目支出交易记录类别的数据。</span><span class="sxs-lookup"><span data-stu-id="aca45-108">The integration templates that are available with the Data integration feature enables the flow of data about project expense transaction categories between Finance and Operations and Project Service Automation.</span></span>

<span data-ttu-id="aca45-109">如果项目支出类别掌握在 Finance and Operations 中，则集成流首先从 Finance and Operations 到 Project Service Automation，然后通过从 Project Service Automation 同步到 Finance and Operations 更新项目支出类别集成 ID。</span><span class="sxs-lookup"><span data-stu-id="aca45-109">If the project expense categories are mastered in Finance and Operations, the integration flow is first from Finance and Operations to Project Service Automation, and then updating the project expense categories integration IDs by synchronizing from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="aca45-110">如果项目支出类别掌握在 Project Service Automation 中，则集成流首先从 Project Service Automation 到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="aca45-110">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance and Operations.</span></span> <span data-ttu-id="aca45-111">从 Project Service Automation 同步之前，必须已在 Finance and Operations 中配置了项目类别。</span><span class="sxs-lookup"><span data-stu-id="aca45-111">The project categories must already be configured in Finance and Operations prior to the synchronization from Project Service Automation.</span></span> <span data-ttu-id="aca45-112">然后从 Finance and Operations 同步回 Project Service Automation，然后再次从 Project Service Automation 同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="aca45-112">Then synchronize from Finance and Operations back to Project Service Automation and then from Project Service Automation to Finance and Operations again.</span></span> <span data-ttu-id="aca45-113">这样就确保了链接类别，并且不创建重复项。</span><span class="sxs-lookup"><span data-stu-id="aca45-113">This ensures the categories are linked and duplicates are not created.</span></span>

> [!NOTE]
> <span data-ttu-id="aca45-114">项目支出类别通常掌握在 Finance and Operations 中。</span><span class="sxs-lookup"><span data-stu-id="aca45-114">Typically, the project expense categories will be mastered in Finance and Operations.</span></span> <span data-ttu-id="aca45-115">如果您的情况不是这样，或者您已经在 Project Service Automation 中创建了支出类别，则必须首先使用项目支出交易记录类别（PSA 到 Fin and Ops）同步，然后使用项目支出交易记录类别（Fin and Ops 到 PSA）同步。</span><span class="sxs-lookup"><span data-stu-id="aca45-115">If that is not your situation, or you already have expense categories created in Project Service Automation, you must first sync using the Project expense transaction categories (PSA to Fin and Ops) and then sync using Project expense transaction categories (Fin and Ops to PSA).</span></span> <span data-ttu-id="aca45-116">然后应该再次运行从 PSA 到 Fin and Ops 的同步。</span><span class="sxs-lookup"><span data-stu-id="aca45-116">You should then run the sync from PSA to Fin and Ops one more time.</span></span>

> <span data-ttu-id="aca45-117">如果首先从 Project Service Automation 同步，则必须已在 Finance and Operations 中设置了项目类别，并且必须将需要使用 Project Service Automation 交易记录类别同步的任何项目类别设置为**在日记帐中有效**。</span><span class="sxs-lookup"><span data-stu-id="aca45-117">If synchronizing first from Project Service Automation, the project categories must already be set up in Finance and Operations and any project categories that need to be synched with the Project Service Automation transaction categories must be set up to be **Active in journals**.</span></span>

<span data-ttu-id="aca45-118">下图显示 Project Service Automation 与 Finance and Operations 之间中如何同步数据。</span><span class="sxs-lookup"><span data-stu-id="aca45-118">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="aca45-119">[![Project Service Automation 与 Finance and Operations 集成的数据传输](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="aca45-119">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>


## <a name="templates-and-tasks"></a><span data-ttu-id="aca45-120">模板和任务</span><span class="sxs-lookup"><span data-stu-id="aca45-120">Templates and tasks</span></span>

<span data-ttu-id="aca45-121">若要访问可用模板，请在 Microsoft PowerApps 管理员中心中选择**项目**，然后在右上角中选择**新建项目**以选择公共模板。</span><span class="sxs-lookup"><span data-stu-id="aca45-121">To access available templates, in the Microsoft PowerApps Admin Center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="aca45-122">以下模板和基础任务用于将项目支出类别从 Finance and Operations 同步到 Project Service Automation：</span><span class="sxs-lookup"><span data-stu-id="aca45-122">The following template and underlying task is used to synchronize project expense categories from Finance and Operations to Project Service Automation:</span></span>

-  <span data-ttu-id="aca45-123">**数据集成中的模板名称：** 项目支出交易记录类别（Fin and Ops 到 PSA）</span><span class="sxs-lookup"><span data-stu-id="aca45-123">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
-  <span data-ttu-id="aca45-124">**项目中任务的名称：** 将类别同步到 PSA</span><span class="sxs-lookup"><span data-stu-id="aca45-124">**Name of the task in the project:** Sync categories to PSA</span></span>

## <a name="entity-set"></a><span data-ttu-id="aca45-125">实体集</span><span class="sxs-lookup"><span data-stu-id="aca45-125">Entity set</span></span>

| <span data-ttu-id="aca45-126">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="aca45-126">Finance and Operations</span></span>               | <span data-ttu-id="aca45-127">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="aca45-127">Project Service Automation</span></span>    |
|--------------------------------------|-------------------------------|
| <span data-ttu-id="aca45-128">类别的集成实体</span><span class="sxs-lookup"><span data-stu-id="aca45-128">Integration entity for categories</span></span>    | <span data-ttu-id="aca45-129">交易记录类别</span><span class="sxs-lookup"><span data-stu-id="aca45-129">Transaction categories</span></span>        |

## <a name="entity-flow"></a><span data-ttu-id="aca45-130">实体流</span><span class="sxs-lookup"><span data-stu-id="aca45-130">Entity flow</span></span>

<span data-ttu-id="aca45-131">项目支出类别掌握在 Finance and Operations 中，并且作为交易记录类别同步到 Project Service Automation。</span><span class="sxs-lookup"><span data-stu-id="aca45-131">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span>

## <a name="power-query"></a><span data-ttu-id="aca45-132">Power Query</span><span class="sxs-lookup"><span data-stu-id="aca45-132">Power Query</span></span>

<span data-ttu-id="aca45-133">同步到 Project Service Automation 时，必须使用 Microsoft Power Query 为交易记录类别设置计费类型。</span><span class="sxs-lookup"><span data-stu-id="aca45-133">You must use Microsoft Power Query to set the billing type on the transaction category when synchronizing to Project Service Automation.</span></span> <span data-ttu-id="aca45-134">项目支出交易记录类别（Fin and Ops 到 PSA）模板具有一个默认列，并且已提供了映射。</span><span class="sxs-lookup"><span data-stu-id="aca45-134">The Project expense transaction categories (Fin and Ops to PSA) template has a default column and mapping already provided.</span></span> <span data-ttu-id="aca45-135">如果创建自己的模板，则必须在 Power Query 中添加一个条件列。</span><span class="sxs-lookup"><span data-stu-id="aca45-135">If you create your own template, you must add a conditional column in Power Query.</span></span>
- <span data-ttu-id="aca45-136">从项目支出类别映射任务内打开 “高级查询和筛选”窗体。</span><span class="sxs-lookup"><span data-stu-id="aca45-136">Open the Advance Query and Filtering form from within the mapping of project expense categories task.</span></span>
- <span data-ttu-id="aca45-137">选择**添加条件列**。</span><span class="sxs-lookup"><span data-stu-id="aca45-137">Select **Add Conditional Column**.</span></span>
- <span data-ttu-id="aca45-138">为新列指定名称，如 BillingType。</span><span class="sxs-lookup"><span data-stu-id="aca45-138">Give the new column a name, such as BillingType.</span></span>
- <span data-ttu-id="aca45-139">输入以下条件：if **CATEGORYID not equal to null then 19235001, Otherwise null**。</span><span class="sxs-lookup"><span data-stu-id="aca45-139">Enter the following condition: if **CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
- <span data-ttu-id="aca45-140">在列中单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="aca45-140">Click **OK** on the column.</span></span>
- <span data-ttu-id="aca45-141">请务必在映射页中映射这个新列。</span><span class="sxs-lookup"><span data-stu-id="aca45-141">Be sure to map this new column in the mapping page.</span></span>

<span data-ttu-id="aca45-142">下图显示了数据集成中的模板任务映射的一个示例。</span><span class="sxs-lookup"><span data-stu-id="aca45-142">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="aca45-143">此映射显示将从 Finance and Operations 同步到 Project Service Automation 的字段信息。</span><span class="sxs-lookup"><span data-stu-id="aca45-143">The mapping shows the field information that will be synchronized from Finance and Operations to Project Service Automation.</span></span>

<span data-ttu-id="aca45-144">[![模板映射](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="aca45-144">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

<span data-ttu-id="aca45-145">以下模板和基础任务用于将项目支出类别从 Project Service Automation 同步到 Finance and Operations：</span><span class="sxs-lookup"><span data-stu-id="aca45-145">The following template and underlying task is used to synchronize project expense categories from Project Service Automation to Finance and Operations:</span></span>

<span data-ttu-id="aca45-146">-**项目中的模板名称：** 项目支出交易记录类别（PSA 到 Fin and Ops）-**项目中的任务名称：** 将类别同步到 Fin Ops</span><span class="sxs-lookup"><span data-stu-id="aca45-146">-**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops) -**Name of the task in the project:** Sync categories to Fin Ops</span></span>

## <a name="entity-set"></a><span data-ttu-id="aca45-147">实体集</span><span class="sxs-lookup"><span data-stu-id="aca45-147">Entity set</span></span>

| <span data-ttu-id="aca45-148">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="aca45-148">Project Service Automation</span></span>      | <span data-ttu-id="aca45-149">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="aca45-149">Finance and Operations</span></span>             |
|---------------------------------|------------------------------------|
| <span data-ttu-id="aca45-150">交易记录类别</span><span class="sxs-lookup"><span data-stu-id="aca45-150">Transaction categories</span></span>          | <span data-ttu-id="aca45-151">类别的集成实体</span><span class="sxs-lookup"><span data-stu-id="aca45-151">Integration entity for categories</span></span>  | 

## <a name="entity-flow"></a><span data-ttu-id="aca45-152">实体流</span><span class="sxs-lookup"><span data-stu-id="aca45-152">Entity flow</span></span>

<span data-ttu-id="aca45-153">项目支出类别掌握在 Finance and Operations 中，并且作为交易记录类别同步到 Project Service Automation。</span><span class="sxs-lookup"><span data-stu-id="aca45-153">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="aca45-154">同步回 Finance and Operations 将更新 Finance and Operations 项目类别中来自 Project Service Automation 的集成 ID。</span><span class="sxs-lookup"><span data-stu-id="aca45-154">The synchronization back to Finance and Operations updates the integration ID from Project Service Automation on the Finance and Operations project category.</span></span>

<span data-ttu-id="aca45-155">下图显示了数据集成中的模板任务映射的一个示例。</span><span class="sxs-lookup"><span data-stu-id="aca45-155">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="aca45-156">此映射显示将从 Project Service Automation 同步到 Finance and Operations 的字段信息。</span><span class="sxs-lookup"><span data-stu-id="aca45-156">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="aca45-157">[![模板映射](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="aca45-157">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>

