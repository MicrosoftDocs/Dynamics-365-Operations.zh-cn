---
title: "将项目估计值从 Project Service Automation 直接同步到 Finance and Operations "
description: "本主题介绍用于将项目工时估计值和项目支出估计值直接从 Microsoft Dynamics 365 for Project Service Automation 到 Microsoft Dynamics 365 for Finance and Operations 的模板和基础任务。"
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 21338b889e0377dbfd5adfd461ea81b39a75baf8
ms.contentlocale: zh-cn
ms.lasthandoff: 08/08/2018

---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="68785-103">将项目估计值从 Project Service Automation 直接同步到 Finance and Operations </span><span class="sxs-lookup"><span data-stu-id="68785-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="68785-104">本主题介绍用于将项目工时估计值和项目支出估计值直接从 Microsoft Dynamics 365 for Project Service Automation 到 Dynamics 365 for Finance and Operations 的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="68785-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Microsoft Dynamics 365 for Project Service Automation to Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="68785-105">Microsoft Dynamics 365 for Finance and Operations 版本 8.0 中提供项目任务集成、费用交易记录类别、工时估计值、费用估计值和功能锁定。</span><span class="sxs-lookup"><span data-stu-id="68785-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.</span></span>
> - <span data-ttu-id="68785-106">Microsoft Dynamics 365 for Finance and Operations 版本 8.0.1 或更高版本中支持实际值集成。</span><span class="sxs-lookup"><span data-stu-id="68785-106">Actuals integration is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.1 or later.</span></span>
> - <span data-ttu-id="68785-107">如果您正在使用 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.3.0，则安装 KB 4132657 和 KB 4132660 之后，可以使用模板集成项目任务、费用交易记录类别、工时估计值、费用估计值和实际值和配置功能锁定。</span><span class="sxs-lookup"><span data-stu-id="68785-107">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="68785-108">如果必须重置会计分配，建议也安装 KB 4131710。</span><span class="sxs-lookup"><span data-stu-id="68785-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="68785-109">Project Service Automation 到 Finance and Operations 的数据传输</span><span class="sxs-lookup"><span data-stu-id="68785-109">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="68785-110">Project Service Automation 到 Finance and Operations 集成解决方案使用数据集成功能在 Project Service Automation 和 Finance and Operations 的实例之间同步数据。</span><span class="sxs-lookup"><span data-stu-id="68785-110">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="68785-111">可通过数据集成功能提供的集成模板将有关项目工时估计值和项目支出估计值的数据从 Project Service Automation 传输到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="68785-111">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="68785-112">下图显示 Project Service Automation 与 Finance and Operations 之间中如何同步数据。</span><span class="sxs-lookup"><span data-stu-id="68785-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="68785-113">[![Project Service Automation 与 Finance and Operations 集成的数据传输](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="68785-113">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="68785-114">项目工时估计值</span><span class="sxs-lookup"><span data-stu-id="68785-114">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="68785-115">模板和任务</span><span class="sxs-lookup"><span data-stu-id="68785-115">Template and tasks</span></span>

<span data-ttu-id="68785-116">若要访问可用模板，请在 Microsoft PowerApps 管理员中心中选择**项目**，然后在右上角中选择**新建项目**以选择公共模板。</span><span class="sxs-lookup"><span data-stu-id="68785-116">To access the available templates, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="68785-117">以下模板和基础任务用于将项目工时估计值从 Project Service Automation 同步到 Finance and Operations：</span><span class="sxs-lookup"><span data-stu-id="68785-117">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="68785-118">**数据集成中的模板名称：** 项目工时估计值（PSA 到 Fin and Ops）</span><span class="sxs-lookup"><span data-stu-id="68785-118">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="68785-119">**项目中的任务名称：**</span><span class="sxs-lookup"><span data-stu-id="68785-119">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="68785-120">交易记录关系</span><span class="sxs-lookup"><span data-stu-id="68785-120">Transaction relationships</span></span>
    - <span data-ttu-id="68785-121">支出估计值</span><span class="sxs-lookup"><span data-stu-id="68785-121">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="68785-122">实体集</span><span class="sxs-lookup"><span data-stu-id="68785-122">Entity set</span></span>

| <span data-ttu-id="68785-123">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="68785-123">Project Service Automation</span></span> | <span data-ttu-id="68785-124">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="68785-124">Finance and Operations</span></span>                        |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="68785-125">项目任务</span><span class="sxs-lookup"><span data-stu-id="68785-125">Project tasks</span></span>              | <span data-ttu-id="68785-126">项目工时估计集成实体</span><span class="sxs-lookup"><span data-stu-id="68785-126">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="68785-127">实体流</span><span class="sxs-lookup"><span data-stu-id="68785-127">Entity flow</span></span>

<span data-ttu-id="68785-128">项目工时估计值在 Project Service Automation 中管理，并同步到 Finance and Operations 中充当项目工时预测。</span><span class="sxs-lookup"><span data-stu-id="68785-128">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance and Operations as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="68785-129">必备项</span><span class="sxs-lookup"><span data-stu-id="68785-129">Prerequisites</span></span>

<span data-ttu-id="68785-130">必须先同步项目、项目任务和项目支出交易记录类别，才能同步项目工时估计值。</span><span class="sxs-lookup"><span data-stu-id="68785-130">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="68785-131">Power Query</span><span class="sxs-lookup"><span data-stu-id="68785-131">Power Query</span></span>

<span data-ttu-id="68785-132">在项目工时估计值模板中，必须使用 Microsoft Power Query for Excel 才能完成以下任务：</span><span class="sxs-lookup"><span data-stu-id="68785-132">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="68785-133">设置将在集成新建工时预测时使用的默认预测模型 ID。</span><span class="sxs-lookup"><span data-stu-id="68785-133">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="68785-134">筛选掉任务中所有资源特定的且将导致与工时预测集成失败的记录。</span><span class="sxs-lookup"><span data-stu-id="68785-134">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="68785-135">筛选掉所有空交易记录类别行。</span><span class="sxs-lookup"><span data-stu-id="68785-135">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="68785-136">如果未能完成此任务，可能导致工时预测不正确。</span><span class="sxs-lookup"><span data-stu-id="68785-136">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="68785-137">设置默认预测模型 ID</span><span class="sxs-lookup"><span data-stu-id="68785-137">Set the default forecast model ID</span></span>

<span data-ttu-id="68785-138">若要更新模板中的默认预测模型 ID，请单击**映射**箭头打开映射。</span><span class="sxs-lookup"><span data-stu-id="68785-138">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="68785-139">选择**高级查询和筛选**链接。</span><span class="sxs-lookup"><span data-stu-id="68785-139">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="68785-140">如果在使用默认项目工时估计值（PSA 到 Fin and Ops）模板，请在**应用的步骤**列表中选择**插入的条件**。</span><span class="sxs-lookup"><span data-stu-id="68785-140">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="68785-141">在**函数**条目中，将 **O\_forecast** 替换为集成应使用的预测模型 ID 的名称。</span><span class="sxs-lookup"><span data-stu-id="68785-141">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="68785-142">默认模板中包含来自一个演示数据的预测模型 ID。</span><span class="sxs-lookup"><span data-stu-id="68785-142">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="68785-143">如果要创建新模板，必须添加此列。</span><span class="sxs-lookup"><span data-stu-id="68785-143">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="68785-144">在 Power Query 中，选择**添加条件列**，然后为新列输入名称，如 **ModelID**。</span><span class="sxs-lookup"><span data-stu-id="68785-144">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="68785-145">输入列的条件：其中，如果项目任务 非空，则 \<enter the forecast model ID\>；否则为空。</span><span class="sxs-lookup"><span data-stu-id="68785-145">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="68785-146">筛选掉资源特定的记录</span><span class="sxs-lookup"><span data-stu-id="68785-146">Filter out resource-specific records</span></span>

<span data-ttu-id="68785-147">项目工时估计值（PSA 到 Fin and Ops）模板有一个默认筛选器，用于去除资源特定的所有记录。</span><span class="sxs-lookup"><span data-stu-id="68785-147">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="68785-148">如果创建自己的模板，则必须添加这个筛选器。</span><span class="sxs-lookup"><span data-stu-id="68785-148">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="68785-149">选择**高级查询和筛选**链接以筛选 **msdyn\_islinetask** 列，以便仅包含 **False** 记录。</span><span class="sxs-lookup"><span data-stu-id="68785-149">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="68785-150">筛选掉空交易记录类别行</span><span class="sxs-lookup"><span data-stu-id="68785-150">Filter out empty transaction category rows</span></span>

<span data-ttu-id="68785-151">必须添加筛选器以移除包含空交易记录类别的所有行。</span><span class="sxs-lookup"><span data-stu-id="68785-151">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="68785-152">无论使用默认模板还是创建自己的模板，都需要执行此任务。</span><span class="sxs-lookup"><span data-stu-id="68785-152">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="68785-153">此筛选器移除来自 Project Service Automation 且可能导致 Finance and Operations 中的工时预测不正确的所有汇总行。</span><span class="sxs-lookup"><span data-stu-id="68785-153">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance and Operations to be incorrect.</span></span> <span data-ttu-id="68785-154">选择**高级查询和筛选**链接以筛选掉 **msdyn\_transactioncategory\_value** 列中的空记录。</span><span class="sxs-lookup"><span data-stu-id="68785-154">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="68785-155">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="68785-155">Template mapping in Data integration</span></span>

<span data-ttu-id="68785-156">下图显示了数据集成中的模板任务映射的一个示例。</span><span class="sxs-lookup"><span data-stu-id="68785-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="68785-157">此映射显示将从 Project Service Automation 同步到 Finance and Operations 的字段信息。</span><span class="sxs-lookup"><span data-stu-id="68785-157">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="68785-158">[![模板映射](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="68785-158">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="68785-159">项目支出估计值</span><span class="sxs-lookup"><span data-stu-id="68785-159">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="68785-160">模板和任务</span><span class="sxs-lookup"><span data-stu-id="68785-160">Template and tasks</span></span>

<span data-ttu-id="68785-161">以下模板和基础任务用于将项目支出估计值从 Project Service Automation 同步到 Finance and Operations：</span><span class="sxs-lookup"><span data-stu-id="68785-161">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="68785-162">**数据集成中的模板名称：** 项目支出估计值（PSA 到 Fin and Ops）</span><span class="sxs-lookup"><span data-stu-id="68785-162">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="68785-163">**项目中的任务名称：**</span><span class="sxs-lookup"><span data-stu-id="68785-163">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="68785-164">交易记录关系</span><span class="sxs-lookup"><span data-stu-id="68785-164">Transaction relationships</span></span> 
    - <span data-ttu-id="68785-165">支出估计值</span><span class="sxs-lookup"><span data-stu-id="68785-165">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="68785-166">实体集</span><span class="sxs-lookup"><span data-stu-id="68785-166">Entity set</span></span>

| <span data-ttu-id="68785-167">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="68785-167">Project Service Automation</span></span> | <span data-ttu-id="68785-168">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="68785-168">Finance and Operations</span></span>                                   |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="68785-169">交易记录连接</span><span class="sxs-lookup"><span data-stu-id="68785-169">Transaction Connections</span></span>    | <span data-ttu-id="68785-170">项目交易记录关系的集成实体</span><span class="sxs-lookup"><span data-stu-id="68785-170">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="68785-171">估计值行</span><span class="sxs-lookup"><span data-stu-id="68785-171">Estimate Lines</span></span>             | <span data-ttu-id="68785-172">项目费用估计值的集成实体</span><span class="sxs-lookup"><span data-stu-id="68785-172">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="68785-173">实体流</span><span class="sxs-lookup"><span data-stu-id="68785-173">Entity flow</span></span>

<span data-ttu-id="68785-174">项目支出估计值在 Project Service Automation 中管理，并同步到 Finance and Operations 中充当项目支出预测。</span><span class="sxs-lookup"><span data-stu-id="68785-174">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance and Operations as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="68785-175">必备项</span><span class="sxs-lookup"><span data-stu-id="68785-175">Prerequisites</span></span>

<span data-ttu-id="68785-176">必须先同步项目、项目任务和项目支出交易记录类别，才能同步项目支出估计值。</span><span class="sxs-lookup"><span data-stu-id="68785-176">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="68785-177">Power Query</span><span class="sxs-lookup"><span data-stu-id="68785-177">Power Query</span></span>

<span data-ttu-id="68785-178">在项目支出估计值模板中，必须使用 Power Query 才能完成以下任务：</span><span class="sxs-lookup"><span data-stu-id="68785-178">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="68785-179">筛选为仅包含支出估计值行记录。</span><span class="sxs-lookup"><span data-stu-id="68785-179">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="68785-180">设置将在集成新建工时预测时使用的默认预测模型 ID。</span><span class="sxs-lookup"><span data-stu-id="68785-180">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="68785-181">转换计费类型。</span><span class="sxs-lookup"><span data-stu-id="68785-181">Transform the billing types.</span></span>
- <span data-ttu-id="68785-182">转换交易记录类型。</span><span class="sxs-lookup"><span data-stu-id="68785-182">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="68785-183">筛选为仅包含支出估计值行</span><span class="sxs-lookup"><span data-stu-id="68785-183">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="68785-184">项目支出估计值（PSA 到 Fin and Ops）模板有一个默认筛选器，用于筛选为集成中仅包含支出行。</span><span class="sxs-lookup"><span data-stu-id="68785-184">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="68785-185">如果创建自己的模板，则必须添加这个筛选器。</span><span class="sxs-lookup"><span data-stu-id="68785-185">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="68785-186">选择**交易记录关系**任务，然后单击**映射**箭头打开映射。</span><span class="sxs-lookup"><span data-stu-id="68785-186">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="68785-187">选择**高级查询和筛选**链接。</span><span class="sxs-lookup"><span data-stu-id="68785-187">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="68785-188">筛选 **msdyn\_transactiontype1** 列，以便其中仅包含 **msdyn\_estimateline**。</span><span class="sxs-lookup"><span data-stu-id="68785-188">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="68785-189">设置默认预测模型 ID</span><span class="sxs-lookup"><span data-stu-id="68785-189">Set the default forecast model ID</span></span>

<span data-ttu-id="68785-190">若要更新模板中的默认预测模型 ID，请选择**支出估计值**任务，然后单击**映射**箭头打开映射。</span><span class="sxs-lookup"><span data-stu-id="68785-190">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="68785-191">选择**高级查询和筛选**链接。</span><span class="sxs-lookup"><span data-stu-id="68785-191">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="68785-192">如果在使用默认的项目支出类别（PSA 到 Fin and Ops）模板，请在 Power Query, 中从**应用的步骤**部分选择第一个**插入的条件**。</span><span class="sxs-lookup"><span data-stu-id="68785-192">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="68785-193">在**函数**条目中，将 **O\_forecast** 替换为集成应使用的预测模型 ID 的名称。</span><span class="sxs-lookup"><span data-stu-id="68785-193">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="68785-194">默认模板中包含来自一个演示数据的预测模型 ID。</span><span class="sxs-lookup"><span data-stu-id="68785-194">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="68785-195">如果要创建新模板，必须添加此列。</span><span class="sxs-lookup"><span data-stu-id="68785-195">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="68785-196">在 Power Query 中，选择**添加条件列**，然后为新列输入名称，如 **ModelID**。</span><span class="sxs-lookup"><span data-stu-id="68785-196">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="68785-197">输入列的条件：如果估计值行 ID 非空，则 \<enter the forecast model ID\>；否则为空。</span><span class="sxs-lookup"><span data-stu-id="68785-197">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="68785-198">转换计费类型</span><span class="sxs-lookup"><span data-stu-id="68785-198">Transform the billing types</span></span>

<span data-ttu-id="68785-199">项目支出估计值（PSA 到 Fin and Ops）模板包含一个条件列，用于转换集成期间从 Project Service Automation 收到的计费类型。</span><span class="sxs-lookup"><span data-stu-id="68785-199">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="68785-200">如果创建自己的模板，则必须添加这个条件列。</span><span class="sxs-lookup"><span data-stu-id="68785-200">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="68785-201">选择**高级查询和筛选**链接，然后选择**添加条件列**。</span><span class="sxs-lookup"><span data-stu-id="68785-201">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="68785-202">为新列输入名称，如 **BillingType**。</span><span class="sxs-lookup"><span data-stu-id="68785-202">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="68785-203">然后输入以下条件：</span><span class="sxs-lookup"><span data-stu-id="68785-203">Then enter the following condition:</span></span>

<span data-ttu-id="68785-204">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="68785-204">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="68785-205">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="68785-205">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="68785-206">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="68785-206">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="68785-207">else **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="68785-207">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="68785-208">转换交易记录类型</span><span class="sxs-lookup"><span data-stu-id="68785-208">Transform the transaction types</span></span>

<span data-ttu-id="68785-209">项目支出估计值（PSA 到 Fin and Ops）模板包含一个条件列，用于转换集成期间从 Project Service Automation 收到的交易记录类型。</span><span class="sxs-lookup"><span data-stu-id="68785-209">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="68785-210">如果创建自己的模板，则必须添加这个条件列。</span><span class="sxs-lookup"><span data-stu-id="68785-210">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="68785-211">选择**高级查询和筛选**链接，然后选择**添加条件列**。</span><span class="sxs-lookup"><span data-stu-id="68785-211">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="68785-212">为新列输入名称，如 **TransactionType**。</span><span class="sxs-lookup"><span data-stu-id="68785-212">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="68785-213">然后输入以下条件：</span><span class="sxs-lookup"><span data-stu-id="68785-213">Then enter the following condition:</span></span>

<span data-ttu-id="68785-214">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span><span class="sxs-lookup"><span data-stu-id="68785-214">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="68785-215">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span><span class="sxs-lookup"><span data-stu-id="68785-215">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="68785-216">else **null**</span><span class="sxs-lookup"><span data-stu-id="68785-216">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="68785-217">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="68785-217">Template mapping in Data integration</span></span>

<span data-ttu-id="68785-218">下图显示了数据集成中的模板任务映射的示例。</span><span class="sxs-lookup"><span data-stu-id="68785-218">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="68785-219">此映射显示将从 Project Service Automation 同步到 Finance and Operations 的字段信息。</span><span class="sxs-lookup"><span data-stu-id="68785-219">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="68785-220">[![模板映射](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="68785-220">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="68785-221">[![模板映射](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="68785-221">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>

