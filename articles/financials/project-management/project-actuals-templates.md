---
title: "将项目实际值从 Project Service Automation 直接同步到 Finance and Operations 中的项目集成日记帐进行过帐"
description: "本主题介绍用于将项目实际值直接从 Microsoft Dynamics 365 for Project Service Automation 同步到 Dynamics 365 for Finance and Operations 的模板和基础任务。"
author: KimANelson
manager: AnnBe
ms.date: 05/21/2018
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
ms.openlocfilehash: 85ff049852e0b00623f47a12fb66e2c9bb9c4151
ms.contentlocale: zh-cn
ms.lasthandoff: 05/29/2018

---
# <a name="synchronize-project-actuals-from-project-service-automation-directly-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a><span data-ttu-id="6db04-103">将项目实际值从 Project Service Automation 直接同步到 Finance and Operations 中的项目集成日记帐进行过帐</span><span class="sxs-lookup"><span data-stu-id="6db04-103">Synchronize project actuals from Project Service Automation directly to the project integration journal for posting in Finance and Operations</span></span>

<span data-ttu-id="6db04-104">本主题介绍用于将项目实际值直接从 Microsoft Dynamics 365 for Project Service Automation 同步到 Dynamics 365 for Finance and Operations 的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="6db04-104">This topic describes the templates and underlying tasks that are used to synchronize project actuals directly from Microsoft Dynamics 365 for Project Service Automation to Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="6db04-105">此模板将交易记录从 Project Service Automation 同步到 Finance and Operations 中的暂存表内。</span><span class="sxs-lookup"><span data-stu-id="6db04-105">The template syncs transactions from Project Service Automation into a staging table in Finance and Operations.</span></span> <span data-ttu-id="6db04-106">同步完成后，必须从暂存表导入集成日记帐。</span><span class="sxs-lookup"><span data-stu-id="6db04-106">After synchronization is complete, you must import from the staging table to the integration journal.</span></span>

> [!NOTE]
> <span data-ttu-id="6db04-107">Dynamics 365 for Finance and Operations 版本 8.01 中支持项目实际值集成。</span><span class="sxs-lookup"><span data-stu-id="6db04-107">Project actuals integration is available in Dynamics 365 for Finance and Operations version 8.01.</span></span>

> [!NOTE]
> <span data-ttu-id="6db04-108">如果要在 Project Service Automation 中输入时间或支出交易记录的销售税金额，则必须安装 Project Service Automation 更新 7。</span><span class="sxs-lookup"><span data-stu-id="6db04-108">If you are entering sales tax amounts on time or expense transactions in Project Service Automation, you must install the Project Service Automation Update 7.</span></span> <span data-ttu-id="6db04-109">如果不安装此更新，将不会把税金实际值链接到关联的时间或支出实际值，因此不会同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="6db04-109">If this update is not installed, the tax actuals will not be linked to the associated time or expense actuals and will not be synced to Finance and Operations.</span></span> <span data-ttu-id="6db04-110">联系支持以获取详细信息。</span><span class="sxs-lookup"><span data-stu-id="6db04-110">Contact Support for more information.</span></span>


## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="6db04-111">Project Service Automation 到 Finance and Operations 的数据传输</span><span class="sxs-lookup"><span data-stu-id="6db04-111">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="6db04-112">Project Service Automation 到 Finance and Operations 集成解决方案使用数据集成功能在 Project Service Automation 和 Finance and Operations 的实例之间同步数据。</span><span class="sxs-lookup"><span data-stu-id="6db04-112">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="6db04-113">可通过数据集成功能提供的集成模板将有关项目实际值的数据从 Project Service Automation 传输到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="6db04-113">The integration templates that are available with the Data integration feature enable the flow of data about project actuals from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="6db04-114">下图显示 Project Service Automation 与 Finance and Operations 之间中如何同步数据。</span><span class="sxs-lookup"><span data-stu-id="6db04-114">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="6db04-115">[![Project Service Automation 与 Finance and Operations 集成的数据传输](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)</span><span class="sxs-lookup"><span data-stu-id="6db04-115">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)</span></span>


## <a name="templates-and-tasks"></a><span data-ttu-id="6db04-116">模板和任务</span><span class="sxs-lookup"><span data-stu-id="6db04-116">Templates and tasks</span></span>

<span data-ttu-id="6db04-117">若要访问可用模板，请在 Microsoft PowerApps 管理员中心中选择**项目**，然后在右上角中选择**新建项目**以选择公共模板。</span><span class="sxs-lookup"><span data-stu-id="6db04-117">To access the available templates, in the Microsoft PowerApps Admin Center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="6db04-118">以下模板和基础任务用于将项目实际值从 Project Service Automation 同步到 Finance and Operations：</span><span class="sxs-lookup"><span data-stu-id="6db04-118">The following template and underlying tasks are used to synchronize project actuals from Project Service Automation to Finance and Operations:</span></span>

-  <span data-ttu-id="6db04-119">**数据集成中的模板名称：** 项目实际值（PSA 到 Fin and Ops）</span><span class="sxs-lookup"><span data-stu-id="6db04-119">**Name of the template in Data integration:** Project actuals (PSA to Fin and Ops)</span></span>

-  <span data-ttu-id="6db04-120">**项目中的任务名称：**</span><span class="sxs-lookup"><span data-stu-id="6db04-120">**Name of the tasks in the project:**</span></span> 
    - <span data-ttu-id="6db04-121">实际值</span><span class="sxs-lookup"><span data-stu-id="6db04-121">Actuals</span></span> 
    - <span data-ttu-id="6db04-122">TransactionConnections</span><span class="sxs-lookup"><span data-stu-id="6db04-122">TransactionConnections</span></span>

## <a name="entity-set"></a><span data-ttu-id="6db04-123">实体集</span><span class="sxs-lookup"><span data-stu-id="6db04-123">Entity set</span></span>

| <span data-ttu-id="6db04-124">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="6db04-124">Project Service Automation</span></span>      | <span data-ttu-id="6db04-125">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6db04-125">Finance and Operations</span></span>                                      |
|---------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="6db04-126">实际值</span><span class="sxs-lookup"><span data-stu-id="6db04-126">Actuals</span></span>                         | <span data-ttu-id="6db04-127">项目实际值的集成实体</span><span class="sxs-lookup"><span data-stu-id="6db04-127">Integration entity for project actuals</span></span>                      |
| <span data-ttu-id="6db04-128">交易记录连接</span><span class="sxs-lookup"><span data-stu-id="6db04-128">Transaction Connections</span></span>         | <span data-ttu-id="6db04-129">项目交易记录关系的集成实体</span><span class="sxs-lookup"><span data-stu-id="6db04-129">Integration entity for project transaction relationships</span></span>    |

## <a name="entity-flow"></a><span data-ttu-id="6db04-130">实体流</span><span class="sxs-lookup"><span data-stu-id="6db04-130">Entity flow</span></span>

<span data-ttu-id="6db04-131">项目实际值在 Project Service Automation 中管理，并同步到 Finance and Operations，再同步到项目集成日记帐。</span><span class="sxs-lookup"><span data-stu-id="6db04-131">Project actuals are managed in Project Service Automation, and they are synchronized to Finance and Operations to the project ingetration journal.</span></span> <span data-ttu-id="6db04-132">将根据默认财务维度和过帐设置应用核算。</span><span class="sxs-lookup"><span data-stu-id="6db04-132">The accounting will be applied based on default financial dimensions and posting setup.</span></span>

## <a name="preconditions"></a><span data-ttu-id="6db04-133">前提条件</span><span class="sxs-lookup"><span data-stu-id="6db04-133">Preconditions</span></span>

<span data-ttu-id="6db04-134">必须先配置 Project Service Automation 集成参数并同步项目、项目任务和项目支出类别，才能同步实际值。</span><span class="sxs-lookup"><span data-stu-id="6db04-134">Before synchronization of actuals can occur, you must configure the Project Service Automation integration parameters and synchronize projects, project tasks, and project expense transaction categories.</span></span>

## <a name="power-query"></a><span data-ttu-id="6db04-135">Power Query</span><span class="sxs-lookup"><span data-stu-id="6db04-135">Power Query</span></span>

<span data-ttu-id="6db04-136">必须在项目实际值模板中使用 Microsoft Power Query 才能：</span><span class="sxs-lookup"><span data-stu-id="6db04-136">You must use Microsoft Power Query in the project actuals template to:</span></span>
- <span data-ttu-id="6db04-137">将 Project Service Automation **交易记录类型**转换为 Finance and Operations 中的正确**交易记录类型**。</span><span class="sxs-lookup"><span data-stu-id="6db04-137">Transform the Project Service Automation **transaction type** to the correct **transaction type** in Finance and Operations.</span></span> <span data-ttu-id="6db04-138">已经为项目实际值（PSA 到 Fin and Ops）模板定义了此转换。</span><span class="sxs-lookup"><span data-stu-id="6db04-138">The Project actuals (PSA to Fin and Ops) template already has this transformation defined.</span></span>
- <span data-ttu-id="6db04-139">将 Project Service Automation **计费类型**转换为 Finance and Operations 中的正确**计费类型**。</span><span class="sxs-lookup"><span data-stu-id="6db04-139">Transform the Project Service Automation **billing type** to the correct **billing type** in Finance and Operations.</span></span> <span data-ttu-id="6db04-140">已经为项目实际值（PSA 到 Fin and Ops）模板定义了此转换。</span><span class="sxs-lookup"><span data-stu-id="6db04-140">The Project actuals (PSA to Fin and Ops) template already has this transformation defined.</span></span> <span data-ttu-id="6db04-141">然后将根据 Dynamics 365 for Project Service Automation 集成参数窗体中的配置把计费类型映射到**行属性**。</span><span class="sxs-lookup"><span data-stu-id="6db04-141">The billing type is then mapped to the **line property** based on the configuration in the Dynamics 365 for Project Service Automation integration parameters form.</span></span>
- <span data-ttu-id="6db04-142">筛选出要使用此模板同步的特定**资源组织单位**。</span><span class="sxs-lookup"><span data-stu-id="6db04-142">Filter to specific **Resource organizational units** that are to be synced with this template.</span></span>
- <span data-ttu-id="6db04-143">如果**公司间时间或公司间支出实际值**将同步到 Finance and Operations，您必须在 Finance and Operations 中将**合同组织单位**转换为正确的**法人**。</span><span class="sxs-lookup"><span data-stu-id="6db04-143">If **intercompany time or intercompany expense actuals** will be synced to Finance and Operations, you must transform the **contract organizational unit** to the correct **legal entity** in Finance and Operations.</span></span> <span data-ttu-id="6db04-144">已基于演示数据为项目实际值（PSA 到 Fin and Ops）模板定义了一个条件列。</span><span class="sxs-lookup"><span data-stu-id="6db04-144">The Project actuals (PSA to Fin and Ops) template has a conditional column defined based on demo data.</span></span> <span data-ttu-id="6db04-145">必须将最后插入的条件列更新为正确的法人。</span><span class="sxs-lookup"><span data-stu-id="6db04-145">You must update the last inserted condition column to the correct legal entities.</span></span> <span data-ttu-id="6db04-146">否则可能导致集成错误或将不正确的交易记录导入 Finance and Operations 中。</span><span class="sxs-lookup"><span data-stu-id="6db04-146">Failure to do this may result in either an integration error or incorrect actual transactions imported into Finance and Operations.</span></span>
- <span data-ttu-id="6db04-147">如果不将**公司间时间或公司间支出实际值**同步到 Finance and operations，则必须从模板中删除最后插入的条件列。</span><span class="sxs-lookup"><span data-stu-id="6db04-147">If **intercompany time or intercompany expense actuals** will not be synced to Finance and operations, you must delete the last inserted condition column from your template.</span></span> <span data-ttu-id="6db04-148">否则可能导致集成错误或将不正确的交易记录导入 Finance and Operations 中。</span><span class="sxs-lookup"><span data-stu-id="6db04-148">Failure to do this may result in either an integration error or incorrect actual transactions imported into Finance and Operations.</span></span>

### <a name="contract-organizational-unit"></a><span data-ttu-id="6db04-149">合同组织单位</span><span class="sxs-lookup"><span data-stu-id="6db04-149">Contract Organizational Unit</span></span>
<span data-ttu-id="6db04-150">若要更新模板中插入的条件列，请单击**映射**箭头打开映射。</span><span class="sxs-lookup"><span data-stu-id="6db04-150">To update the inserted condition column in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="6db04-151">选择打开“高级查询和筛选”。</span><span class="sxs-lookup"><span data-stu-id="6db04-151">Select to open the Advanced Query and Filtering.</span></span>
- <span data-ttu-id="6db04-152">如果在使用默认的 Microsoft 项目实际值（PSA 到 Fin and Ops）模板，请在**应用的步骤**部分中选择最后一个**插入的条件**。</span><span class="sxs-lookup"><span data-stu-id="6db04-152">If you are using the default Microsoft Project actuals (PSA to Fin and Ops) template, select the lasat **Inserted Condition** in the **Applied Steps** section.</span></span> <span data-ttu-id="6db04-153">在**函数**条目中，将 **USSI** 替换为集成应使用的**法人** 的名称。</span><span class="sxs-lookup"><span data-stu-id="6db04-153">In the **Function** entry, replace **USSI** with the name of the **Legal entity** that should be used with the integration.</span></span> <span data-ttu-id="6db04-154">根据需要向**函数**条目添加更多条件，然后将 **else** 条件从 **USMF** 更新为正确的**法人**。</span><span class="sxs-lookup"><span data-stu-id="6db04-154">Add additional conditions as needed to the **Function** entry and update the **else** condition from **USMF** to the correct **Legal entity**.</span></span>
- <span data-ttu-id="6db04-155">如果要新建模板，必须添加此列来为公司间数据和支出提供支持。</span><span class="sxs-lookup"><span data-stu-id="6db04-155">If you are creating a new template, you must add this column to support intercompany time and expenses.</span></span> <span data-ttu-id="6db04-156">选择**添加条件列**并为列命名，如 LegalEntity。</span><span class="sxs-lookup"><span data-stu-id="6db04-156">Select **Add Conditional Column** and give the column a name, such as LegalEntity.</span></span> <span data-ttu-id="6db04-157">输入列的条件：where if msdyn_contractorganizationalunitid.msdyn_name is <organizational unit>, then <enter the Legal entity>; else null.。</span><span class="sxs-lookup"><span data-stu-id="6db04-157">Enter the condition for the column where if msdyn_contractorganizationalunitid.msdyn_name is <organizational unit>, then <enter the Legal entity>; else null.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="6db04-158">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="6db04-158">Template mapping in Data integration</span></span>

<span data-ttu-id="6db04-159">下图显示了数据集成中的模板任务映射的一个示例。</span><span class="sxs-lookup"><span data-stu-id="6db04-159">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="6db04-160">此映射显示将从 Project Service Automation 同步到 Finance and Operations 的字段信息。</span><span class="sxs-lookup"><span data-stu-id="6db04-160">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="6db04-161">[![模板映射](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="6db04-161">[![Template mapping](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)</span></span>

<span data-ttu-id="6db04-162">[![模板映射](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)</span><span class="sxs-lookup"><span data-stu-id="6db04-162">[![Template mapping](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)</span></span>

## <a name="import-from-staging-table"></a><span data-ttu-id="6db04-163">从临时表导入</span><span class="sxs-lookup"><span data-stu-id="6db04-163">Import from staging table</span></span>

<span data-ttu-id="6db04-164">将实际值从 Project Service Automation 同步到 Finance and Operations 之后，必须运行“从暂存表导入”定期流程。</span><span class="sxs-lookup"><span data-stu-id="6db04-164">The Import from staging table perioidic process must be run after the sychronization of actuals from Project Service Automation to Finance and Operations.</span></span> <span data-ttu-id="6db04-165">此流程将把项目交易记录从暂存表导入 Project Service Automation 集成日记帐中，可在其中应用核算和过帐导入的交易记录。</span><span class="sxs-lookup"><span data-stu-id="6db04-165">This process will import the project transactions from the staging table into the Project Service Automation integration journal, where the accounting is applied and the imported transactions can be posted.</span></span> <span data-ttu-id="6db04-166">建议以批处理模式运行此流程，也可以选择将其设置为以重复执行的批处理运行。</span><span class="sxs-lookup"><span data-stu-id="6db04-166">It is recommended that you run this process in batch mode and optionally can be set up to run as a recurring batch.</span></span>

## <a name="update-actuals"></a><span data-ttu-id="6db04-167">更新实际值</span><span class="sxs-lookup"><span data-stu-id="6db04-167">Update Actuals</span></span>

<span data-ttu-id="6db04-168">以下模板和基础任务用于将所过帐项目交易记录的凭证号和销售税从 Finance and Operations 同步到 Project Service Automation。</span><span class="sxs-lookup"><span data-stu-id="6db04-168">The following template and underlying tasks are used to synchronize the voucher number and sales taxes for posted project transactions from Finance and Operations to Project Service Automation:</span></span>

-  <span data-ttu-id="6db04-169">**数据集成中的模板名称：** 项目实际值更新（Fin Ops 到 PSA）</span><span class="sxs-lookup"><span data-stu-id="6db04-169">**Name of the template in Data integration:** Project actuals update (Fin Ops to PSA)</span></span>
-  <span data-ttu-id="6db04-170">**项目中的任务名称：**</span><span class="sxs-lookup"><span data-stu-id="6db04-170">**Name of the tasks in the project:**</span></span> 
     - <span data-ttu-id="6db04-171">实际值</span><span class="sxs-lookup"><span data-stu-id="6db04-171">Actuals</span></span> 
     - <span data-ttu-id="6db04-172">TransactionConnections</span><span class="sxs-lookup"><span data-stu-id="6db04-172">TransactionConnections</span></span>

## <a name="entity-set"></a><span data-ttu-id="6db04-173">实体集</span><span class="sxs-lookup"><span data-stu-id="6db04-173">Entity set</span></span>

| <span data-ttu-id="6db04-174">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6db04-174">Finance and Operations</span></span>                                         | <span data-ttu-id="6db04-175">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="6db04-175">Project Service Automation</span></span>        |
|----------------------------------------------------------------|-----------------------------------|
| <span data-ttu-id="6db04-176">项目实际值的集成实体</span><span class="sxs-lookup"><span data-stu-id="6db04-176">Integration entity for project actuals</span></span>                         | <span data-ttu-id="6db04-177">实际值</span><span class="sxs-lookup"><span data-stu-id="6db04-177">Actuals</span></span>                           |
| <span data-ttu-id="6db04-178">项目交易记录关系的集成实体</span><span class="sxs-lookup"><span data-stu-id="6db04-178">Integration entity for project transaction relationships</span></span>       | <span data-ttu-id="6db04-179">交易记录连接</span><span class="sxs-lookup"><span data-stu-id="6db04-179">Transaction Connections</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="6db04-180">实体流</span><span class="sxs-lookup"><span data-stu-id="6db04-180">Entity flow</span></span>

<span data-ttu-id="6db04-181">项目实际值在 Project Service Automation 中管理，并同步到 Finance and Operations，再同步到项目集成日记帐。</span><span class="sxs-lookup"><span data-stu-id="6db04-181">Project actuals are managed in Project Service Automation, and they are synchronized to Finance and Operations to the project integration journal.</span></span> <span data-ttu-id="6db04-182">实际值在 Finance and Operations 中过帐之后，将在 Project Service Automation 中使用来自 Finance and Operations 的凭证号更新。</span><span class="sxs-lookup"><span data-stu-id="6db04-182">Once posted in Finance and Operations, actuals are updated in Project Service Automation with the voucher number from Finance and Operations.</span></span> <span data-ttu-id="6db04-183">如果在 Finance and Operations 中添加了销售税，将在 PRoject Service Automation 中创建新的税金实际值。</span><span class="sxs-lookup"><span data-stu-id="6db04-183">If sales taxes were added in Finance and Operations, new tax actuals will be created in PRoject Service Automation.</span></span>

## <a name="power-query"></a><span data-ttu-id="6db04-184">Power Query</span><span class="sxs-lookup"><span data-stu-id="6db04-184">Power Query</span></span>

<span data-ttu-id="6db04-185">必须在项目实际值更新模板中使用 Microsoft Power Query 才能：</span><span class="sxs-lookup"><span data-stu-id="6db04-185">You must use Microsoft Power Query in the project actuals update template to:</span></span>
- <span data-ttu-id="6db04-186">将 Finance and Operations **交易记录类型**转换为 Project Service Automation 中的正确**交易记录类型**。</span><span class="sxs-lookup"><span data-stu-id="6db04-186">Transform the Finance and Operations **transaction type** to the correct **transaction type** in Project Service Automation.</span></span> <span data-ttu-id="6db04-187">已经为项目实际值更新（Fin Ops 到 PSA）模板定义了此转换。</span><span class="sxs-lookup"><span data-stu-id="6db04-187">The Project actuals update (Fin Ops to PSA) template already has this transformation defined.</span></span>
- <span data-ttu-id="6db04-188">将 Finance and Operations **计费类型**转换为 Project Service Automation 中的正确**计费类型**。</span><span class="sxs-lookup"><span data-stu-id="6db04-188">Transform the Finance and Operations **billing type** to the correct **billing type** in Project Service Automation.</span></span> <span data-ttu-id="6db04-189">已经为项目实际值更新（Fin Ops 到 PSA）模板定义了此转换。</span><span class="sxs-lookup"><span data-stu-id="6db04-189">The Project actuals update (Fin Ops to PSA) template already has this transformation defined.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="6db04-190">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="6db04-190">Template mapping in Data integration</span></span>

<span data-ttu-id="6db04-191">下图显示了数据集成中的模板任务映射的示例。</span><span class="sxs-lookup"><span data-stu-id="6db04-191">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="6db04-192">此映射显示将从 Finance and Operations 同步到 Project Service Automation 的字段信息。</span><span class="sxs-lookup"><span data-stu-id="6db04-192">The mapping shows the field information that will be synchronized from Finance and Operations to Project Service Automation.</span></span>

<span data-ttu-id="6db04-193">[![模板映射](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="6db04-193">[![Template mapping](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)</span></span>

<span data-ttu-id="6db04-194">[![模板映射](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)</span><span class="sxs-lookup"><span data-stu-id="6db04-194">[![Template mapping](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)</span></span>




