---
title: "项目预测和预算"
description: 
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 32dd89d92a496d6601d1983dbc3c8e7e579ee0b3
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="project-forecasts-and-budgets"></a><span data-ttu-id="729a4-102">项目预测和预算</span><span class="sxs-lookup"><span data-stu-id="729a4-102">Project forecasts and budgets</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="729a4-103">Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 提供两种管理和控制您的项目的方式：项目预测和项目预算。</span><span class="sxs-lookup"><span data-stu-id="729a4-103">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition provides two ways to manage and control your projects: project forecasts and project budgets.</span></span> 

<span data-ttu-id="729a4-104">如果您的组织有操作视角，并且它侧重于产生自特定交易处理的收入和成本，请使用项目预测。</span><span class="sxs-lookup"><span data-stu-id="729a4-104">Use project forecasting if your organization has an operational perspective, and if it focuses on revenues and costs that are derived from specific transactions.</span></span> <span data-ttu-id="729a4-105">如果您的组织注重详细的财务金额，请使用项目预算。</span><span class="sxs-lookup"><span data-stu-id="729a4-105">Use project budgeting if your organization focuses more on the financial amounts.</span></span> 

<span data-ttu-id="729a4-106">项目预测和项目预算使用预测模型包含项目的交易记录金额。</span><span class="sxs-lookup"><span data-stu-id="729a4-106">Both project forecasts and project budgets use forecast models to hold the projected transaction amounts.</span></span> 

<span data-ttu-id="729a4-107">每个方法都有自己的优点。</span><span class="sxs-lookup"><span data-stu-id="729a4-107">Each method has its advantages.</span></span> <span data-ttu-id="729a4-108">您应该在为您的组织选择方法之前考虑以下各点。</span><span class="sxs-lookup"><span data-stu-id="729a4-108">You should consider the following points before you select a method for your organization.</span></span>

|                           |                                                                                                                                                                                                                                                         |                                                                                                                                                                         |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                           | <span data-ttu-id="729a4-109">**项目预测**</span><span class="sxs-lookup"><span data-stu-id="729a4-109">**Project forecasting**</span></span>                                                                                                                                                                                                                                 | <span data-ttu-id="729a4-110">**项目预算**</span><span class="sxs-lookup"><span data-stu-id="729a4-110">**Project budgeting**</span></span>                                                                                                                                                   |
| <span data-ttu-id="729a4-111">**期间分配**</span><span class="sxs-lookup"><span data-stu-id="729a4-111">**Period allocation**</span></span>     | <span data-ttu-id="729a4-112">您不能在会计期间内明确分配交易记录。</span><span class="sxs-lookup"><span data-stu-id="729a4-112">You can't explicitly allocate transactions over a fiscal period.</span></span> <span data-ttu-id="729a4-113">预测和预测的控制基于项目的使用年限。</span><span class="sxs-lookup"><span data-stu-id="729a4-113">Instead, the forecast, and the control of the forecast, are based on the life of the project.</span></span> <span data-ttu-id="729a4-114">由于预测基于特定日期，因此您必须从该日期推断期间。</span><span class="sxs-lookup"><span data-stu-id="729a4-114">Because forecasts are based on a specific date, you must infer the period from the date.</span></span> | <span data-ttu-id="729a4-115">您可以在整个项目或会计期间分配交易记录。</span><span class="sxs-lookup"><span data-stu-id="729a4-115">You can allocate transactions over the whole project or a fiscal period.</span></span> <span data-ttu-id="729a4-116">如果您在期间分配，则可以将不使用的金额结转到下一会计期间。</span><span class="sxs-lookup"><span data-stu-id="729a4-116">If you allocate over a period, you can carry unused amounts forward to the next fiscal period.</span></span> |
| <span data-ttu-id="729a4-117">**查看交易记录**</span><span class="sxs-lookup"><span data-stu-id="729a4-117">**Viewing transactions**</span></span>  | <span data-ttu-id="729a4-118">您可以在预测窗体中查看交易记录，在其中您将看到整个公司和所有项目的预测，无论层次结构如何。</span><span class="sxs-lookup"><span data-stu-id="729a4-118">You can view transactions in the forecast forms, where you see the forecasts for the whole company and for all projects, regardless of the hierarchy.</span></span> <span data-ttu-id="729a4-119">若要在特定项目，必须筛选数据。</span><span class="sxs-lookup"><span data-stu-id="729a4-119">To focus on a particular project, you must filter the data.</span></span>                                       | <span data-ttu-id="729a4-120">您可以查看单个项目层次结构的预算交易记录。</span><span class="sxs-lookup"><span data-stu-id="729a4-120">You can view budgeted transactions for a single project hierarchy.</span></span> <span data-ttu-id="729a4-121">因此，您可以查看父级项目及其子级项目的交易记录详细信息。</span><span class="sxs-lookup"><span data-stu-id="729a4-121">Therefore, you can view transaction details for a parent project or its subprojects.</span></span>                 |
| <span data-ttu-id="729a4-122">**交易记录变量**</span><span class="sxs-lookup"><span data-stu-id="729a4-122">**Transaction variables**</span></span> | <span data-ttu-id="729a4-123">当您输入预测交易记录时，您可以使用为实际交易记录而存在的各个属性。</span><span class="sxs-lookup"><span data-stu-id="729a4-123">When you enter forecast transactions, you can use every attribute that exists for an actual transaction.</span></span> <span data-ttu-id="729a4-124">这允许在预测的更高的详细信息。</span><span class="sxs-lookup"><span data-stu-id="729a4-124">This allows for greater detail in the forecast.</span></span> <span data-ttu-id="729a4-125">例如，您可以输入数量的详细信息，工人、物料或记录属性。</span><span class="sxs-lookup"><span data-stu-id="729a4-125">For example, you can enter details for quantities, workers, items, or line properties.</span></span>         | <span data-ttu-id="729a4-126">当您输入预算详细信息时，您只能使用金额、类别和活动。</span><span class="sxs-lookup"><span data-stu-id="729a4-126">When you enter budget details, you can use only amounts, categories, and activities.</span></span>                                                                                    |
| <span data-ttu-id="729a4-127">**安全性**</span><span class="sxs-lookup"><span data-stu-id="729a4-127">**Security**</span></span>              | <span data-ttu-id="729a4-128">预测基于您在预测窗体中输入的交易记录，并且不涉及流程控制机制。</span><span class="sxs-lookup"><span data-stu-id="729a4-128">Forecasting is based on transactions that you enter in the forecast forms and involves no process control mechanism.</span></span> <span data-ttu-id="729a4-129">对预测窗体具有权限的所有工作人员可以修改信息，而无需审核。</span><span class="sxs-lookup"><span data-stu-id="729a4-129">Any worker who has permissions for a forecast form can revise information without approval.</span></span>                                        | <span data-ttu-id="729a4-130">预算使用工作流系统，该系统启用更改管理并让您能够保留版本的历史记录。</span><span class="sxs-lookup"><span data-stu-id="729a4-130">Budgeting uses the workflow system, which enables change management and lets you keep a history of the revisions.</span></span>                                                       |
| <span data-ttu-id="729a4-131">**输入类型**</span><span class="sxs-lookup"><span data-stu-id="729a4-131">**Entry types**</span></span>           | <span data-ttu-id="729a4-132">预测交易记录基于单位的数量和成本和销售单位价格。</span><span class="sxs-lookup"><span data-stu-id="729a4-132">Forecast transaction entries are based on the number of units, and on cost and sales unit prices.</span></span>                                                                                                                                                       | <span data-ttu-id="729a4-133">预算详细信息基于在成本和收入之间拆分的金额。</span><span class="sxs-lookup"><span data-stu-id="729a4-133">Budget details are based on amounts, which are split between costs and revenues.</span></span>                                                                                        |
| <span data-ttu-id="729a4-134">**预测模型**</span><span class="sxs-lookup"><span data-stu-id="729a4-134">**Forecast models**</span></span>       | <span data-ttu-id="729a4-135">因为每个预测必须与一个模型关联，您可以创建多个预测模型，以及设置子模型。</span><span class="sxs-lookup"><span data-stu-id="729a4-135">Because each forecast must be associated with a model, you can create multiple forecast models and also set up submodels.</span></span>                                                                                                                               | <span data-ttu-id="729a4-136">项目预算的限制为预算使用的预测模型。</span><span class="sxs-lookup"><span data-stu-id="729a4-136">Project budgeting limits the forecast models that are used for budgeting.</span></span> <span data-ttu-id="729a4-137">数量预测模型可以帮助提高中的信息的一致性。</span><span class="sxs-lookup"><span data-stu-id="729a4-137">Fewer forecast models can help increase consistency in projections.</span></span>                           |
| <span data-ttu-id="729a4-138">**费用超限**</span><span class="sxs-lookup"><span data-stu-id="729a4-138">**Cost overruns**</span></span>         | <span data-ttu-id="729a4-139">您可以只允许或禁止将生成费用超限的交易记录条目。</span><span class="sxs-lookup"><span data-stu-id="729a4-139">You can only allow or disallow the entry of transactions that will cause a cost overrun.</span></span>                                                                                                                                                                | <span data-ttu-id="729a4-140">项目预算为用户提供附加控件选项。</span><span class="sxs-lookup"><span data-stu-id="729a4-140">Project budgeting provides additional control options for users.</span></span> <span data-ttu-id="729a4-141">您可以允许警告和超限。</span><span class="sxs-lookup"><span data-stu-id="729a4-141">You can allow warnings and overruns.</span></span>                                                                   |
| <span data-ttu-id="729a4-142">**控制**</span><span class="sxs-lookup"><span data-stu-id="729a4-142">**Control**</span></span>               | <span data-ttu-id="729a4-143">通过使用缩减预测，预测进行控制。</span><span class="sxs-lookup"><span data-stu-id="729a4-143">Forecast control is performed by using forecast reduction.</span></span> <span data-ttu-id="729a4-144">实际金额基于预测交易记录余额减去的天数，没有任何审计线索。</span><span class="sxs-lookup"><span data-stu-id="729a4-144">Actual amounts are subtracted from forecast transaction balances without any audit trail.</span></span> <span data-ttu-id="729a4-145">这可能有助于更确定跟踪实际交易记录将出现的位置。</span><span class="sxs-lookup"><span data-stu-id="729a4-145">This can make it more difficult to trace where the actual transactions occurred.</span></span>                   | <span data-ttu-id="729a4-146">在项目预算管理，实际金额。在剩余预算金额中减去的天数。</span><span class="sxs-lookup"><span data-stu-id="729a4-146">In project budget control, actual amounts are subtracted from amounts in the remaining budget.</span></span> <span data-ttu-id="729a4-147">这样更广的审计线索。</span><span class="sxs-lookup"><span data-stu-id="729a4-147">This allows for a clearer audit trail.</span></span>                                   |

## <a name="project-forecasts"></a><span data-ttu-id="729a4-148">项目预测</span><span class="sxs-lookup"><span data-stu-id="729a4-148">Project forecasts</span></span>
<span data-ttu-id="729a4-149">当您使用项目预测时，您可以为每个交易记录类型在预测窗体中输入预测交易记录。</span><span class="sxs-lookup"><span data-stu-id="729a4-149">When you use project forecasting, you can enter forecast transactions in forecast forms for each transaction type.</span></span> <span data-ttu-id="729a4-150">对实际交易记录可用的每个特性都能用于预测交易记录 — 例如，行利润，行特性，工作人员或描述。</span><span class="sxs-lookup"><span data-stu-id="729a4-150">Every attribute that is available for an actual transaction can be used for a forecast transaction—for example, line profitability, line attributes, workers, or descriptions.</span></span> <span data-ttu-id="729a4-151">您也可以计划发生了成本之后你将开发票给客户的时间长短。</span><span class="sxs-lookup"><span data-stu-id="729a4-151">You can also project how long after you incur a cost you will invoice a customer.</span></span> 

<span data-ttu-id="729a4-152">项目预测交易记录是基于单位和金额的。</span><span class="sxs-lookup"><span data-stu-id="729a4-152">Project forecasting transactions are based on units and amounts.</span></span> 

<span data-ttu-id="729a4-153">您必须将每个项目预测与某个预测模型相关联。</span><span class="sxs-lookup"><span data-stu-id="729a4-153">You must associate each project forecast with a forecast model.</span></span> <span data-ttu-id="729a4-154">当您输入预测交易记录时， 将自动建议一个预测模型。</span><span class="sxs-lookup"><span data-stu-id="729a4-154">When you enter a forecast transaction, a forecast model is automatically suggested.</span></span> <span data-ttu-id="729a4-155">预测模型充当预测交易记录的容器。</span><span class="sxs-lookup"><span data-stu-id="729a4-155">The forecast model acts as a container for the forecast transactions.</span></span> 

<span data-ttu-id="729a4-156">您可以将预测模型指定为模型的子模型。</span><span class="sxs-lookup"><span data-stu-id="729a4-156">You can designate forecast models as submodels for a model.</span></span> <span data-ttu-id="729a4-157">这能让您按地区、时段或部门预测。</span><span class="sxs-lookup"><span data-stu-id="729a4-157">This lets you forecast by region, time period, or department.</span></span> <span data-ttu-id="729a4-158">您可以复制某个模型中的预测交易记录来创建新模型，并将这些交易记录转移到总帐。</span><span class="sxs-lookup"><span data-stu-id="729a4-158">You can copy the forecast transactions in a model to create a new model, and you can also transfer the transactions to the general ledger.</span></span> <span data-ttu-id="729a4-159">由于在预测和模型之间具有一对一的关系，每个预测模型为项目构成了一个单独的预算。</span><span class="sxs-lookup"><span data-stu-id="729a4-159">Because there is a one-to-one relationship between a forecast and a model, each forecast model makes up a separate budget for a project.</span></span> 

<span data-ttu-id="729a4-160">预测模型可以把预测缩减用作项目的控制结构。</span><span class="sxs-lookup"><span data-stu-id="729a4-160">Forecast models can use forecast reduction as the control mechanism for projects.</span></span> <span data-ttu-id="729a4-161">在预测缩减中，实际交易记录减少预测交易记录余额。</span><span class="sxs-lookup"><span data-stu-id="729a4-161">In forecast reduction, actual transactions reduce forecast transaction balances.</span></span> <span data-ttu-id="729a4-162">但是，因此预测缩减应用于该层次结构中的最高的项目，所以它提供了预测中更改的一个受限查看。</span><span class="sxs-lookup"><span data-stu-id="729a4-162">However, because forecast reduction is applied to the highest project in the hierarchy, it provides a limited view of changes in the forecast.</span></span> <span data-ttu-id="729a4-163">例如，如果工作人员与下级项目相关联，那么该工作人员的实际交易记录已过帐到父项目。</span><span class="sxs-lookup"><span data-stu-id="729a4-163">For example, if a worker is associated with a subproject, the actual transactions for the worker are posted to the parent project.</span></span> <span data-ttu-id="729a4-164">这可能会使跟踪更改很困难，因为您不能很容易地确定子项目在哪一个交易记录中导致预测金额。</span><span class="sxs-lookup"><span data-stu-id="729a4-164">This can make it difficult to track changes, because you can't easily determine which transaction in which subproject caused a reduction to the forecast amount.</span></span> <span data-ttu-id="729a4-165">因此，最好为要使用的预测缩减创建预测模型的副本。</span><span class="sxs-lookup"><span data-stu-id="729a4-165">Therefore, it's a good idea to create a copy of a forecast model for forecast reduction to use.</span></span> <span data-ttu-id="729a4-166">然后，您可以使用报告来查看最初预测的内容。</span><span class="sxs-lookup"><span data-stu-id="729a4-166">You can then use reports to view what was originally forecasted.</span></span> 

<span data-ttu-id="729a4-167">您可以修订、复制、删除或转移项目预测到总帐预算。</span><span class="sxs-lookup"><span data-stu-id="729a4-167">You can revise, copy, delete, or transfer project forecasts to a general ledger budget.</span></span> <span data-ttu-id="729a4-168">但是，没有流程控制。</span><span class="sxs-lookup"><span data-stu-id="729a4-168">However, there is no process control.</span></span> <span data-ttu-id="729a4-169">对预测窗体有权限的任何工作人员可以进行修订而不复查。</span><span class="sxs-lookup"><span data-stu-id="729a4-169">Any worker who has permission for a forecast form can make revisions without review.</span></span>

-   <span data-ttu-id="729a4-170">**修订** – 您可以在与创建原始条目相同的窗体中修订预测交易记录。</span><span class="sxs-lookup"><span data-stu-id="729a4-170">**Revise **– You can revise a forecast transaction in the same forms where the original entries were made.</span></span>
-   <span data-ttu-id="729a4-171">**复制或删除** – 当您复制预测交易记录时，您将一个预测模型的交易记录行复制到了另外一个预测模型。</span><span class="sxs-lookup"><span data-stu-id="729a4-171">**Copy or delete** – When you copy forecast transactions, you copy the transaction lines of one forecast model to another forecast model.</span></span> <span data-ttu-id="729a4-172">当您删除预测时，您把预测交易记录从预测模型中删除。</span><span class="sxs-lookup"><span data-stu-id="729a4-172">When you delete a forecast, you delete the forecast transactions from a forecast model.</span></span> <span data-ttu-id="729a4-173">为了限制要复制或删除的预测交易记录，请选择特定交易记录类型和日期。</span><span class="sxs-lookup"><span data-stu-id="729a4-173">To limit the forecast transactions that are copied or deleted, select specific transaction types and dates.</span></span> <span data-ttu-id="729a4-174">这能让您仅复制或删除某个预测的特定部分。</span><span class="sxs-lookup"><span data-stu-id="729a4-174">This lets you copy or delete only specific parts of a forecast.</span></span>
-   <span data-ttu-id="729a4-175">**转移** – 当您将项目预测转移到总帐预算中时，您将预测模型的预测交易记录转移到了总帐预算。</span><span class="sxs-lookup"><span data-stu-id="729a4-175">**Transfer** – When you transfer a project forecast to a general ledger budget, you transfer the forecast transactions of a forecast model to a general ledger budget.</span></span> <span data-ttu-id="729a4-176">您可以覆盖您将转移项目预测所到的总帐预算中的任何先前已转移的交易记录。</span><span class="sxs-lookup"><span data-stu-id="729a4-176">You can overwrite any previously transferred transactions in the general ledger budget that you transfer your project forecast to.</span></span>

## <a name="project-budgets"></a><span data-ttu-id="729a4-177">项目预算</span><span class="sxs-lookup"><span data-stu-id="729a4-177">Project budgets</span></span>
<span data-ttu-id="729a4-178">项目预算是比项目预测更简单的方法，尽管项目预算与预测模型相集成。</span><span class="sxs-lookup"><span data-stu-id="729a4-178">Project budgeting is a simpler method than forecasting, although it does integrate with forecast models.</span></span> <span data-ttu-id="729a4-179">它将单个条目窗体用于原始预算明细和修订，而且它只允许基于金额、类别或活动的计划。</span><span class="sxs-lookup"><span data-stu-id="729a4-179">It uses a single entry form for original budget details and revisions, and allows for projections that are based only on amount, category, or activity.</span></span> 

<span data-ttu-id="729a4-180">在项目预算中，必须将所有原始预算和修订发送到项目工作流以供审核。</span><span class="sxs-lookup"><span data-stu-id="729a4-180">In project budgeting, all original budgets and revisions must be sent to a project workflow for approval.</span></span> <span data-ttu-id="729a4-181">工作流提供给您对流程的增强了的控制，并创建了一个更改历史记录。</span><span class="sxs-lookup"><span data-stu-id="729a4-181">Workflows give you increased control over the process and create a change history record.</span></span> 

<span data-ttu-id="729a4-182">项目预算类似于总帐预算，但是项目预算更快速、更容易设置。</span><span class="sxs-lookup"><span data-stu-id="729a4-182">Project budgeting resembles general ledger budgeting, but is faster and easier to set up.</span></span> <span data-ttu-id="729a4-183">总账预算中的编号规则或币种等许多选项不必为项目单独设置。</span><span class="sxs-lookup"><span data-stu-id="729a4-183">Many of the options in general ledger budgeting, such as number sequences or currency, do not have to be set up separately for projects.</span></span>

<span data-ttu-id="729a4-184">项目预算自动与两个预测模型相关联，其中一个预测模型是针对原始预算，而另一个预测模型针对剩余预算。</span><span class="sxs-lookup"><span data-stu-id="729a4-184">Project budgets are automatically associated with two forecast models, one for original budget and one for remaining budget.</span></span> <span data-ttu-id="729a4-185">因此，基于预测模型的报告可使用预算数据。</span><span class="sxs-lookup"><span data-stu-id="729a4-185">Therefore, reports that are based on forecast models can use budget data.</span></span> <span data-ttu-id="729a4-186">当承诺了一个项目预算时，系统将基于用于报告和控制目的的相关模型创建预测交易记录。</span><span class="sxs-lookup"><span data-stu-id="729a4-186">When a project budget is committed, the system creates forecast transactions based on the associated models, which are used for reporting and control purposes.</span></span>

## <a name="forecast-models"></a><span data-ttu-id="729a4-187">预测模型</span><span class="sxs-lookup"><span data-stu-id="729a4-187">Forecast models</span></span>
<span data-ttu-id="729a4-188">预测模型具有单层层次结构。</span><span class="sxs-lookup"><span data-stu-id="729a4-188">Forecast models have a single-layer hierarchy.</span></span> <span data-ttu-id="729a4-189">这意味着，一个项目预测必须与一个预测模型相关联。</span><span class="sxs-lookup"><span data-stu-id="729a4-189">This means that one project forecast must be associated with one forecast model.</span></span>

<span data-ttu-id="729a4-190">如果您使用项目预测，您可以标识设计为子模型。</span><span class="sxs-lookup"><span data-stu-id="729a4-190">If you use project forecasting, you can identify models as submodels.</span></span> <span data-ttu-id="729a4-191">然后您可以按部门、时段或地区创建预测。</span><span class="sxs-lookup"><span data-stu-id="729a4-191">You can then create forecasts by department, time period, or region.</span></span> <span data-ttu-id="729a4-192">例如，可以创建一年的预测模型，然后为由地区标题提交的东北部、东南部、西北部和西南部区域预测创建子模型。</span><span class="sxs-lookup"><span data-stu-id="729a4-192">For example, you can create a forecast model for a year, and then create submodels for the Northeast, Southeast, Northwest, and Southwest regional forecasts that regional heads submit.</span></span> <span data-ttu-id="729a4-193">通过在可用报表中选择不同的选项，可以按总预测或由子模型查看信息。</span><span class="sxs-lookup"><span data-stu-id="729a4-193">By selecting different options in the available reports, you can view information by total forecast or by submodel.</span></span>



