---
title: "将项目估计值从 Project Service Automation 直接同步到 Finance and Operations 中的项目预测"
description: "本主题介绍用于将项目工时估计值和项目支出估计值直接从 Microsoft Dynamics 365 for Project Service Automation 到 Dynamics 365 for Finance and Operations 的模板和基础任务。"
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
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 90501f40da0fdc66ad087b3bd746c908cc25711b
ms.contentlocale: zh-cn
ms.lasthandoff: 05/29/2018

---
# <a name="synchronize-project-estimates-from-project-service-automation-directly-to-project-forecasts-in-finance-and-operations"></a><span data-ttu-id="b50ee-103">将项目估计值从 Project Service Automation 直接同步到 Finance and Operations 中的项目预测</span><span class="sxs-lookup"><span data-stu-id="b50ee-103">Synchronize project estimates from Project Service Automation directly to project forecasts in Finance and Operations</span></span>

<span data-ttu-id="b50ee-104">本主题介绍用于将项目工时估计值和项目支出估计值直接从 Microsoft Dynamics 365 for Project Service Automation 到 Dynamics 365 for Finance and Operations 的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="b50ee-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Microsoft Dynamics 365 for Project Service Automation to Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="b50ee-105">Dynamics 365 for Finance and Operations 版本 8.0 中提供项目任务集成、费用交易记录类别、工时估计值、费用估计值和功能锁定。</span><span class="sxs-lookup"><span data-stu-id="b50ee-105">Project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Dynamics 365 for Finance and Operations version 8.0.</span></span>


## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="b50ee-106">Project Service Automation 到 Finance and Operations 的数据传输</span><span class="sxs-lookup"><span data-stu-id="b50ee-106">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="b50ee-107">Project Service Automation 到 Finance and Operations 集成解决方案使用数据集成功能在 Project Service Automation 和 Finance and Operations 的实例之间同步数据。</span><span class="sxs-lookup"><span data-stu-id="b50ee-107">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="b50ee-108">可通过数据集成功能提供的集成模板将有关项目工时估计值和项目支出估计值的数据从 Project Service Automation 传输到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="b50ee-108">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="b50ee-109">下图显示 Project Service Automation 与 Finance and Operations 之间中如何同步数据。</span><span class="sxs-lookup"><span data-stu-id="b50ee-109">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="b50ee-110">[![Project Service Automation 与 Finance and Operations 集成的数据传输](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="b50ee-110">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>


## <a name="templates-and-tasks"></a><span data-ttu-id="b50ee-111">模板和任务</span><span class="sxs-lookup"><span data-stu-id="b50ee-111">Templates and tasks</span></span>

<span data-ttu-id="b50ee-112">若要访问可用模板，请在 Microsoft PowerApps 管理员中心中选择**项目**，然后在右上角中选择**新建项目**以选择公共模板。</span><span class="sxs-lookup"><span data-stu-id="b50ee-112">To access the available templates, in the Microsoft PowerApps Admin Center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="b50ee-113">以下模板和基础任务用于将项目工时估计值从 Project Service Automation 同步到 Finance and Operations：</span><span class="sxs-lookup"><span data-stu-id="b50ee-113">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance and Operations:</span></span>

-  <span data-ttu-id="b50ee-114">**数据集成中的模板名称：** 项目工时估计值（PSA 到 Fin and Ops）</span><span class="sxs-lookup"><span data-stu-id="b50ee-114">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>

-  <span data-ttu-id="b50ee-115">**项目中的任务名称：**</span><span class="sxs-lookup"><span data-stu-id="b50ee-115">**Name of the tasks in the project:**</span></span> 
    - <span data-ttu-id="b50ee-116">交易记录关系</span><span class="sxs-lookup"><span data-stu-id="b50ee-116">Transaction relationships</span></span> 
    - <span data-ttu-id="b50ee-117">支出估计值</span><span class="sxs-lookup"><span data-stu-id="b50ee-117">Expense estimates</span></span>

## <a name="entity-set"></a><span data-ttu-id="b50ee-118">实体集</span><span class="sxs-lookup"><span data-stu-id="b50ee-118">Entity set</span></span>

| <span data-ttu-id="b50ee-119">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="b50ee-119">Project Service Automation</span></span>      | <span data-ttu-id="b50ee-120">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b50ee-120">Finance and Operations</span></span>                          |
|---------------------------------|-------------------------------------------------|
| <span data-ttu-id="b50ee-121">项目任务</span><span class="sxs-lookup"><span data-stu-id="b50ee-121">Project tasks</span></span>                   | <span data-ttu-id="b50ee-122">项目工时估计集成实体</span><span class="sxs-lookup"><span data-stu-id="b50ee-122">Integration entity for project hour estimates</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="b50ee-123">实体流</span><span class="sxs-lookup"><span data-stu-id="b50ee-123">Entity flow</span></span>

<span data-ttu-id="b50ee-124">项目工时估计值在 Project Service Automation 中管理，并同步到 Finance and Operations 中充当项目工时预测。</span><span class="sxs-lookup"><span data-stu-id="b50ee-124">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance and Operations as project hour forecasts.</span></span>

## <a name="preconditions"></a><span data-ttu-id="b50ee-125">前提条件</span><span class="sxs-lookup"><span data-stu-id="b50ee-125">Preconditions</span></span>

<span data-ttu-id="b50ee-126">必须先同步项目、项目任务和项目支出交易记录类别，才能同步项目工时估计值。</span><span class="sxs-lookup"><span data-stu-id="b50ee-126">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

## <a name="power-query"></a><span data-ttu-id="b50ee-127">Power Query</span><span class="sxs-lookup"><span data-stu-id="b50ee-127">Power Query</span></span>

<span data-ttu-id="b50ee-128">必须在项目工时估计值模板中使用 Microsoft Power Query 才能：</span><span class="sxs-lookup"><span data-stu-id="b50ee-128">You must use Microsoft Power Query in the project hour estimates template to:</span></span>
- <span data-ttu-id="b50ee-129">设置将在集成新建工时预测时使用的**预测模型 ID**。</span><span class="sxs-lookup"><span data-stu-id="b50ee-129">Set the **Forecast model ID** that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="b50ee-130">筛选掉任务中所有资源特定的且将导致与工时预测集成失败的记录。</span><span class="sxs-lookup"><span data-stu-id="b50ee-130">Filter out any resource specific records within the task that will fail the integration into hour forecasts</span></span>
- <span data-ttu-id="b50ee-131">筛选掉所有空交易记录类别行。</span><span class="sxs-lookup"><span data-stu-id="b50ee-131">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="b50ee-132">如果失败，可能导致工时预测不正确。</span><span class="sxs-lookup"><span data-stu-id="b50ee-132">Failure to do this may result in incorrect hour forecasts.</span></span>

### <a name="forecast-model-id"></a><span data-ttu-id="b50ee-133">预测模型 ID</span><span class="sxs-lookup"><span data-stu-id="b50ee-133">Forecast model ID</span></span>
<span data-ttu-id="b50ee-134">若要更新模板中的默认预测模型 ID，请单击**映射**箭头打开映射。</span><span class="sxs-lookup"><span data-stu-id="b50ee-134">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="b50ee-135">选择打开“高级查询和筛选”。</span><span class="sxs-lookup"><span data-stu-id="b50ee-135">Select to open the Advanced Query and Filtering.</span></span>
- <span data-ttu-id="b50ee-136">如果在使用默认的 Microsoft 项目工时估计值（PSA 到 Fin and Ops）模板，请在**应用的步骤**部分中选择**插入的条件**。</span><span class="sxs-lookup"><span data-stu-id="b50ee-136">If you are using the default Microsoft Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the **Applied Steps** section.</span></span> <span data-ttu-id="b50ee-137">在**函数**条目中，将 **O_forecast** 替换为集成应使用的**预测模型 ID** 的名称。</span><span class="sxs-lookup"><span data-stu-id="b50ee-137">In the **Function** entry, replace **O_forecast** with the name of the **Forecast model ID** that should be used with the integration.</span></span> <span data-ttu-id="b50ee-138">默认模板中包含来自一个演示数据的预测模型 ID。</span><span class="sxs-lookup"><span data-stu-id="b50ee-138">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="b50ee-139">如果要创建新模板，必须添加此列。</span><span class="sxs-lookup"><span data-stu-id="b50ee-139">If you are creating a new template, you must add this column.</span></span> <span data-ttu-id="b50ee-140">选择**添加条件列**并为列命名，如 ModelID。</span><span class="sxs-lookup"><span data-stu-id="b50ee-140">Select **Add Conditional Column** and give the column a name, such as ModelID.</span></span> <span data-ttu-id="b50ee-141">输入列的条件：if Project task is not null, then<enter the forecast model ID>; else null。</span><span class="sxs-lookup"><span data-stu-id="b50ee-141">Enter the condition for the column where if Project task is not null, then<enter the forecast model ID>; else null.</span></span>

### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="b50ee-142">筛选掉资源特定的记录</span><span class="sxs-lookup"><span data-stu-id="b50ee-142">Filter out resource specific records</span></span>
<span data-ttu-id="b50ee-143">项目工时估计值（PSA 到 Fin and Ops）模板有一个默认筛选器，用于去除资源特定的所有记录。</span><span class="sxs-lookup"><span data-stu-id="b50ee-143">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource specific records.</span></span> <span data-ttu-id="b50ee-144">如果创建自己的模板，则必须添加这个筛选器。</span><span class="sxs-lookup"><span data-stu-id="b50ee-144">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="b50ee-145">在“高级查询和筛选”窗体中，选择将列 **msdyn_islinetask** 筛选为仅包含 **False** 记录。</span><span class="sxs-lookup"><span data-stu-id="b50ee-145">In the Advanced Query and Filtering form, select to filter on the column **msdyn_islinetask** to only include **False** records.</span></span>

### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="b50ee-146">筛选掉空交易记录类别行</span><span class="sxs-lookup"><span data-stu-id="b50ee-146">Filter out empty transaction category rows</span></span>
<span data-ttu-id="b50ee-147">必须添加筛选器以移除交易记录类别为空的所有行。</span><span class="sxs-lookup"><span data-stu-id="b50ee-147">You must add a filter to remove any rows with empty transaction categories.</span></span> <span data-ttu-id="b50ee-148">无论使用默认模板还是创建自己的模板，都需要执行此操作。</span><span class="sxs-lookup"><span data-stu-id="b50ee-148">This is needed regardless if you are using the default template or creating your own template.</span></span> <span data-ttu-id="b50ee-149">此筛选器将移除来自 Project Service Automation 且可能导致 Finance and Operations 中的工时预测不正确的所有汇总行。</span><span class="sxs-lookup"><span data-stu-id="b50ee-149">This filter will remove any summary rows coming from Project Service Automation that could cause the hour forecasts in Finance and Operations to be incorrect.</span></span> <span data-ttu-id="b50ee-150">在“高级查询和筛选”窗体中，选择筛选掉列 **msdyn_transactioncategory_value** 中的空记录。</span><span class="sxs-lookup"><span data-stu-id="b50ee-150">In the Advanced Query and Filtering form, select to filter out the null records in the column **msdyn_transactioncategory_value**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="b50ee-151">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="b50ee-151">Template mapping in Data integration</span></span>

<span data-ttu-id="b50ee-152">下图显示了数据集成中的模板任务映射的一个示例。</span><span class="sxs-lookup"><span data-stu-id="b50ee-152">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="b50ee-153">此映射显示将从 Project Service Automation 同步到 Finance and Operations 的字段信息。</span><span class="sxs-lookup"><span data-stu-id="b50ee-153">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="b50ee-154">[![模板映射](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="b50ee-154">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

<span data-ttu-id="b50ee-155">以下模板和基础任务用于将项目支出估计值从 Project Service Automation 同步到 Finance and Operations：</span><span class="sxs-lookup"><span data-stu-id="b50ee-155">The following template and underlying task is used to synchronize project expense estimates from Project Service Automation to Finance and Operations:</span></span>

-  <span data-ttu-id="b50ee-156">**数据集成中的模板名称：** 项目支出估计值（PSA 到 Fin and Ops）</span><span class="sxs-lookup"><span data-stu-id="b50ee-156">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
-  <span data-ttu-id="b50ee-157">**项目中的任务名称：**</span><span class="sxs-lookup"><span data-stu-id="b50ee-157">**Name of the tasks in the project:**</span></span> 
     - <span data-ttu-id="b50ee-158">交易记录关系</span><span class="sxs-lookup"><span data-stu-id="b50ee-158">Transaction relationships</span></span> 
     - <span data-ttu-id="b50ee-159">支出估计值</span><span class="sxs-lookup"><span data-stu-id="b50ee-159">Expense estimates</span></span>

## <a name="entity-set"></a><span data-ttu-id="b50ee-160">实体集</span><span class="sxs-lookup"><span data-stu-id="b50ee-160">Entity set</span></span>

| <span data-ttu-id="b50ee-161">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="b50ee-161">Project Service Automation</span></span>      | <span data-ttu-id="b50ee-162">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b50ee-162">Finance and Operations</span></span>                                     |
|---------------------------------|------------------------------------------------------------|
| <span data-ttu-id="b50ee-163">交易记录连接</span><span class="sxs-lookup"><span data-stu-id="b50ee-163">Transaction Connections</span></span>         | <span data-ttu-id="b50ee-164">项目交易记录关系的集成实体。</span><span class="sxs-lookup"><span data-stu-id="b50ee-164">Integration entity for project transaction relationships.</span></span>   |
| <span data-ttu-id="b50ee-165">估计值行</span><span class="sxs-lookup"><span data-stu-id="b50ee-165">Estimate Lines</span></span>                  | <span data-ttu-id="b50ee-166">项目费用估计值的集成实体。</span><span class="sxs-lookup"><span data-stu-id="b50ee-166">Integration entity for project expense estimates.</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="b50ee-167">实体流</span><span class="sxs-lookup"><span data-stu-id="b50ee-167">Entity flow</span></span>

<span data-ttu-id="b50ee-168">项目支出估计值在 Project Service Automation 中管理，并同步到 Finance and Operations 中充当项目支出预测。</span><span class="sxs-lookup"><span data-stu-id="b50ee-168">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance and Operations as project expense forecasts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b50ee-169">必备项</span><span class="sxs-lookup"><span data-stu-id="b50ee-169">Prerequisites</span></span>

<span data-ttu-id="b50ee-170">必须先同步项目、项目任务和项目支出交易记录类别，才能同步项目支出估计值。</span><span class="sxs-lookup"><span data-stu-id="b50ee-170">Before synchronization of project expense estimates can occur, you must synchronize Projects, Project tasks and Project expense transaction categories.</span></span>

## <a name="power-query"></a><span data-ttu-id="b50ee-171">Power Query</span><span class="sxs-lookup"><span data-stu-id="b50ee-171">Power Query</span></span>

<span data-ttu-id="b50ee-172">必须在项目支出估计值模板中使用 Microsoft Power Query 才能：</span><span class="sxs-lookup"><span data-stu-id="b50ee-172">You must use Microsoft Power Query in the project expense estimates template to:</span></span>
- <span data-ttu-id="b50ee-173">筛选为仅包含支出估计值行记录</span><span class="sxs-lookup"><span data-stu-id="b50ee-173">Filter to include only expense estimate line records</span></span>
- <span data-ttu-id="b50ee-174">设置将在集成新建工时预测时使用的**预测模型 ID**。</span><span class="sxs-lookup"><span data-stu-id="b50ee-174">Set the **Forecast model ID** that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="b50ee-175">转换计费类型。</span><span class="sxs-lookup"><span data-stu-id="b50ee-175">Transform the billing types.</span></span>
- <span data-ttu-id="b50ee-176">转换交易记录类型。</span><span class="sxs-lookup"><span data-stu-id="b50ee-176">Transform the transaction types.</span></span>

### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="b50ee-177">筛选为仅包含支出估计值行</span><span class="sxs-lookup"><span data-stu-id="b50ee-177">Filter to include only expense estimate lines</span></span>
<span data-ttu-id="b50ee-178">项目支出估计值（PSA 到 Fin and Ops）模板有一个默认筛选器，用于筛选为集成中仅包含支出行。</span><span class="sxs-lookup"><span data-stu-id="b50ee-178">The Project expense estimates (PSA to Fin and Ops) template has a default filter to only include expense lines in the integration.</span></span> <span data-ttu-id="b50ee-179">如果创建自己的模板，则必须添加这个筛选器。</span><span class="sxs-lookup"><span data-stu-id="b50ee-179">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="b50ee-180">选择“交易记录关系”任务，然后单击**映射**箭头。</span><span class="sxs-lookup"><span data-stu-id="b50ee-180">Select the Transaction relationships task and click the **Map** arrow.</span></span> <span data-ttu-id="b50ee-181">选择**高级查询和筛选**。</span><span class="sxs-lookup"><span data-stu-id="b50ee-181">Select **Advanced Query and filtering**.</span></span> <span data-ttu-id="b50ee-182">将 **msdyn_transactiontype1**列筛选为仅包含 **msdyn_estimateline**。</span><span class="sxs-lookup"><span data-stu-id="b50ee-182">Filter the **msdyn_transactiontype1** column to include only **msdyn_estimateline**.</span></span>

### <a name="forecast-model-id"></a><span data-ttu-id="b50ee-183">预测模型 ID</span><span class="sxs-lookup"><span data-stu-id="b50ee-183">Forecast model ID</span></span>
<span data-ttu-id="b50ee-184">若要更新模板中的默认预测模型 ID，对于“支出估计值”任务，请单击**映射**箭头打开映射。</span><span class="sxs-lookup"><span data-stu-id="b50ee-184">To update the default forecast model ID in the template, for the Expense estimates task, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="b50ee-185">选择打开“高级查询和筛选”。</span><span class="sxs-lookup"><span data-stu-id="b50ee-185">Select to open the Advanced Query and Filtering.</span></span>
- <span data-ttu-id="b50ee-186">如果在使用默认的 Microsoft 项目支出估计值（PSA 到 Fin and Ops）模板，请在**应用的步骤**部分中选择第一个**插入的条件**。</span><span class="sxs-lookup"><span data-stu-id="b50ee-186">If you are using the default Microsoft Project expense estimates (PSA to Fin and Ops) template, select the first **Inserted Condition** in the **Applied Steps** section.</span></span> <span data-ttu-id="b50ee-187">在**函数**条目中，将 **O_forecast** 替换为集成应使用的**预测模型 ID** 的名称。</span><span class="sxs-lookup"><span data-stu-id="b50ee-187">In the **Function** entry, replace **O_forecast** with the name of the **Forecast model ID** that should be used with the integration.</span></span> <span data-ttu-id="b50ee-188">默认模板中包含来自一个演示数据的预测模型 ID。</span><span class="sxs-lookup"><span data-stu-id="b50ee-188">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="b50ee-189">如果要创建新模板，必须添加此列。</span><span class="sxs-lookup"><span data-stu-id="b50ee-189">If you are creating a new template, you must add this column.</span></span> <span data-ttu-id="b50ee-190">选择**添加条件列**并为列命名，如 ModelID。</span><span class="sxs-lookup"><span data-stu-id="b50ee-190">Select **Add Conditional Column** and give the column a name, such as ModelID.</span></span> <span data-ttu-id="b50ee-191">输入列的条件：如果估计值行 ID 非空，则 < enter the forecast model ID >；否则为空。</span><span class="sxs-lookup"><span data-stu-id="b50ee-191">Enter the condition for the column where if Estimate line ID is not null, then < enter the forecast model ID >; else null.</span></span>

### <a name="transform-the-billing-types"></a><span data-ttu-id="b50ee-192">转换计费类型</span><span class="sxs-lookup"><span data-stu-id="b50ee-192">Transform the billing types</span></span>
<span data-ttu-id="b50ee-193">项目支出估计值（PSA 到 Fin and Ops）模板增加了一个条件列，用于转换集成期间从 Project Service Automation 收到的计费类型。</span><span class="sxs-lookup"><span data-stu-id="b50ee-193">The Project expense estimates (PSA to Fin and Ops) template has a conditional column added to transform the billing types received from Project Service Automation during the integration.</span></span>
- <span data-ttu-id="b50ee-194">如果创建自己的模板，则必须添加这个条件列。</span><span class="sxs-lookup"><span data-stu-id="b50ee-194">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="b50ee-195">在"高级查询和筛选"窗体中，选择**添加条件列**。</span><span class="sxs-lookup"><span data-stu-id="b50ee-195">In the Advanced Query and Filtering form, select **Add Conditional Column**.</span></span> <span data-ttu-id="b50ee-196">为该列指定名称，如“BillingType”。</span><span class="sxs-lookup"><span data-stu-id="b50ee-196">Give the column a name, such as "BillingType".</span></span> <span data-ttu-id="b50ee-197">要输入的条件如下所示：</span><span class="sxs-lookup"><span data-stu-id="b50ee-197">The condition to enter is as follows:</span></span>

    <span data-ttu-id="b50ee-198">If **msdyn_billingtype** = 192350000, then **NonChargeable** else if **msdyn_billingtype** = 192350001, then **Chargeable** else if **msdyn_billingtype** = 192350002, then **Complimentary** else **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="b50ee-198">If **msdyn_billingtype** = 192350000, then **NonChargeable** else if **msdyn_billingtype** = 192350001, then **Chargeable** else if **msdyn_billingtype** = 192350002, then **Complimentary** else **NotAvailable**</span></span>

### <a name="transform-the-transaction-types"></a><span data-ttu-id="b50ee-199">转换交易记录类型</span><span class="sxs-lookup"><span data-stu-id="b50ee-199">Transform the transaction types</span></span>
<span data-ttu-id="b50ee-200">项目支出估计值（PSA 到 Fin and Ops）模板增加了一个条件列，用于转换集成期间从 Project Service Automation 收到的交易记录类型。</span><span class="sxs-lookup"><span data-stu-id="b50ee-200">The Project expense estimates (PSA to Fin and Ops) template has a conditional column added to transform the transaction types received from Project Service Automation during the integration.</span></span>
- <span data-ttu-id="b50ee-201">如果创建自己的模板，则必须添加这个条件列。</span><span class="sxs-lookup"><span data-stu-id="b50ee-201">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="b50ee-202">在"高级查询和筛选"窗体中，选择**添加条件列**。</span><span class="sxs-lookup"><span data-stu-id="b50ee-202">In the Advanced Query and Filtering form, select **Add Conditional Column**.</span></span> <span data-ttu-id="b50ee-203">为该列指定名称，如“TransactionType”。</span><span class="sxs-lookup"><span data-stu-id="b50ee-203">Give the column a name, such as "TransactionType".</span></span> <span data-ttu-id="b50ee-204">要输入的条件如下所示：**msdyn_transactiontypecode** = 192350000, then **Cost** else if **msdyn_transactiontypecode** = 192350005, then **Sales** else **null**</span><span class="sxs-lookup"><span data-stu-id="b50ee-204">The condition to enter is as follows: If **msdyn_transactiontypecode** = 192350000, then **Cost** else if **msdyn_transactiontypecode** = 192350005, then **Sales** else **null**</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="b50ee-205">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="b50ee-205">Template mapping in Data integration</span></span>

<span data-ttu-id="b50ee-206">下图显示了数据集成中的模板任务映射的示例。</span><span class="sxs-lookup"><span data-stu-id="b50ee-206">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="b50ee-207">此映射显示将从 Project Service Automation 同步到 Finance and Operations 的字段信息。</span><span class="sxs-lookup"><span data-stu-id="b50ee-207">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="b50ee-208">[![模板映射](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="b50ee-208">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="b50ee-209">[![模板映射](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="b50ee-209">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>




