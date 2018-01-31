---
title: "创建平价医疗法案报告"
description: "功能可用于协助需要跟踪表单 1095-B 和 1095-C 上申报的信息的雇主支持平价医疗法案的雇主授权单。请注意，仅可为美国的法人启用此功能。"
author: kherr75
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: e41f14d60b6cb4c6091f8b0f7c82d9c56edeee35
ms.contentlocale: zh-cn
ms.lasthandoff: 01/31/2018

---
# <a name="generate-affordable-care-act-reports"></a><span data-ttu-id="c8a1e-103">创建平价医疗法案报告</span><span class="sxs-lookup"><span data-stu-id="c8a1e-103">Generate Affordable Care Act reports</span></span>
<span data-ttu-id="c8a1e-104">功能可用于协助需要跟踪表单 1095-B 和 1095-C 上申报的信息的雇主支持平价医疗法案的**雇主授权单**。请注意，仅可为美国的法人启用此功能。</span><span class="sxs-lookup"><span data-stu-id="c8a1e-104">Functionality is available to assist employers that need to track the information reported on forms 1095-B and 1095-C in support of the **Employer Mandate** portion of the Affordable Care Act. Note this functionality is only enabled for legal entities in the United States.</span></span>

## <a name="getting-started"></a><span data-ttu-id="c8a1e-105">入门</span><span class="sxs-lookup"><span data-stu-id="c8a1e-105">Getting started</span></span>
<span data-ttu-id="c8a1e-106">开始跟踪表单 1095-B 和 1095-C 上报告的信息时，必须先创建一个或多个平价医疗保险范围组。</span><span class="sxs-lookup"><span data-stu-id="c8a1e-106">When beginning to track information to report on forms 1095-B and 1095-C, you must first create one or more Affordable Care coverage groups.</span></span> <span data-ttu-id="c8a1e-107">这些平价医疗保险范围组将用于指示提供给员工的保险范围、最低成本的月保险费中由员工承担的比例（如果成本高于联邦贫困线）以及雇主使用的安全港（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="c8a1e-107">These Affordable Care coverage groups will be used to indicate the offer of coverage that was provided to an employee, the employee’s share of the lowest cost monthly premium (if the cost is above the federal poverty line) as well as Safe Harbor used by the employer, if applicable.</span></span> <span data-ttu-id="c8a1e-108">使用平价医疗法案组可以管理这些字段的信息，无需涉及条件相同的每个员工记录。</span><span class="sxs-lookup"><span data-stu-id="c8a1e-108">Using Affordable Care Act groups enables you to manage the information for these fields without needing to touch every employee record where the conditions are the same.</span></span> <span data-ttu-id="c8a1e-109">此外，使用页面上的成批分配功能可以轻松地将平价医疗保险范围组分配给一个或多个员工。</span><span class="sxs-lookup"><span data-stu-id="c8a1e-109">In addition, Affordable Care coverage groups can easily be assigned to one or more employees using the Mass assign functionality on the page.</span></span>

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a><span data-ttu-id="c8a1e-110">维护保险范围组的多个版本</span><span class="sxs-lookup"><span data-stu-id="c8a1e-110">Maintaining multiple versions of a coverage group</span></span>
<span data-ttu-id="c8a1e-111">您可以维护任何保险范围组的多个版本，允许您进行更改以保持组的信息为最新信息，而不必在您的组织或提供的福利发生变更时创建新组和重新为其分配员工。</span><span class="sxs-lookup"><span data-stu-id="c8a1e-111">You can maintain multiple versions of any coverage group, which allows you to make changes that keep the group’s information current, without having to create a new group and reassign employees to it when something changes in your organization or in the benefits that are offered.</span></span> 

<span data-ttu-id="c8a1e-112">创建您需要的平价医疗保险范围组后，您可以使用页面上的**成批分配**功能选择将组成批分配到员工，或者可以转到每个员工并指示是否需要为该员工跟踪和报告 ACA 信息以及将员工分配到平价医疗保险范围组。</span><span class="sxs-lookup"><span data-stu-id="c8a1e-112">After you’ve created the Affordable Care coverage groups that you need, you can choose to mass assign the groups to employees using the **Mass assignment** functionality on the page, or you can go to each employee and indicate whether ACA information needs to tracked and reported for that employee as well as assigning the employee to an Affordable Care coverage group.</span></span>

<span data-ttu-id="c8a1e-113">如果不需要为员工跟踪和报告平价医疗保险范围组，例如如果是兼职员工，可以将**报告保险范围**字段设置为否。</span><span class="sxs-lookup"><span data-stu-id="c8a1e-113">If affordable care coverage information doesn’t need to be tracked or reported for an employee, for example if they are a part-time employee, the **Report coverage** field could be set to No.</span></span> <span data-ttu-id="c8a1e-114">尽管需要跟踪和报告其 ACA 信息的每位员工均需分配到平价医疗保险范围组，您仍可以更改任何一个月或多个月的**提供的保险范围**、**员工承担的成本比例**和**安全港**选项（可能需要与平价医疗保险范围组输入的值不同的值）。</span><span class="sxs-lookup"><span data-stu-id="c8a1e-114">Although each employee for which ACA information needs to be tracked needs to be assigned to an Affordable Care coverage group, you can still change the **Offer of coverage**, **Employee share of cost** and **Safe Harbor** options for any month – or months – that may need different values than those entered in the Affordable Care coverage group.</span></span>

<span data-ttu-id="c8a1e-115">要输入任何平价医疗保险范围组值的例外，请单击工作人员详细信息页面上找到的平价医疗保险范围链接，该链接位于雇用选项卡上的附加信息部分的下方。</span><span class="sxs-lookup"><span data-stu-id="c8a1e-115">To enter exceptions to any of the Affordable Care coverage group values, click on the Affordable Care Coverage link found on the Worker detail page, which is under the Additional information section on the Employment tab.</span></span>

## <a name="reporting-health-care-coverage"></a><span data-ttu-id="c8a1e-116">报告医疗保险范围</span><span class="sxs-lookup"><span data-stu-id="c8a1e-116">Reporting health care coverage</span></span>
<span data-ttu-id="c8a1e-117">除了跟踪是否已向全职员工提供任何健康保险范围以外，如果雇主为登记的员工（无论其雇佣状态是否为全职或兼职）提供由雇主赞助的自保型保险健康保险范围，则需要在 1095-C 上报告附加信息。</span><span class="sxs-lookup"><span data-stu-id="c8a1e-117">In addition to tracking what if any health insurance coverage was offered to a full-time employee, if the employer offers employer-sponsored self-insured health coverage for which the employee is enrolled (regardless of whether their employment status is full-time or part-time), additional information needs to be reported on the 1095-C.</span></span> <span data-ttu-id="c8a1e-118">由雇主赞助的福利计划涵盖的每位员工（包括依赖方）需要包含在保险的月份的报表上。</span><span class="sxs-lookup"><span data-stu-id="c8a1e-118">Each employee (including dependents) covered by the employer-sponsored benefit plans needs to be included on the report for the months they were covered.</span></span> 

<span data-ttu-id="c8a1e-119">您可以通过选择 **ACA 可申报**复选框指示是否必须申报每个福利计划。</span><span class="sxs-lookup"><span data-stu-id="c8a1e-119">You can indicate whether or not each Benefit plan must be reported by selecting the **ACA reportable** check box.</span></span>

<span data-ttu-id="c8a1e-120">此外，如果员工已选择将其任何依赖方涵盖在福利下，您可以在维护福利页面上指示为每位员工的依赖方投保的日期。</span><span class="sxs-lookup"><span data-stu-id="c8a1e-120">In addition, if employees have chosen to have any of their dependents covered under a benefit you can indicate the dates the dependent was covered for each employee on the Maintain benefits page.</span></span> <span data-ttu-id="c8a1e-121">要指示依赖方是否涵盖在福利下，选择依赖方快速选项卡的操作窗格中的编辑按钮。</span><span class="sxs-lookup"><span data-stu-id="c8a1e-121">To indicate that the dependent is covered under the benefit, choose the Edit button in the action pane of the Dependents FastTab.</span></span>

<span data-ttu-id="c8a1e-122">在**依赖方保险范围日期管理器**页面，可以指示福利涵盖依赖方的日期。</span><span class="sxs-lookup"><span data-stu-id="c8a1e-122">On the **Dependent coverage date manager** page, you can indicate the dates the dependent was covered by the benefit.</span></span> <span data-ttu-id="c8a1e-123">在此页面上输入日期将自动选择**维护福利**页面上的**已涵盖**复选框。</span><span class="sxs-lookup"><span data-stu-id="c8a1e-123">Entering dates on this page will automatically select the **Covered** checkbox on the **Maintain benefits** page.</span></span>

## <a name="generate-1095b-and-1095c-forms"></a><span data-ttu-id="c8a1e-124">生成 1095B 和 1095C 表单</span><span class="sxs-lookup"><span data-stu-id="c8a1e-124">Generate 1095B and 1095C forms</span></span>
<span data-ttu-id="c8a1e-125">您还可以从产品内部生成 109-B 和 109-C 表单，并将其分配到每位员工。</span><span class="sxs-lookup"><span data-stu-id="c8a1e-125">You can also generate 109-B and 1095-C forms from with in the product, and distribute them to each of your employees.</span></span> <span data-ttu-id="c8a1e-126">电子生成 1095-C 和可发送到 IRS 的相应的 1094-C 传送单也可以从系统中生成。</span><span class="sxs-lookup"><span data-stu-id="c8a1e-126">Electronically generating 1095-C and the corresponding 1094-C transmittal files which can be used to send to the IRS, can also be generated from the system.</span></span>  

<span data-ttu-id="c8a1e-127">生成 1095-C 表单时，输入相应的日历或纳税年度以及您是否要打印两页或三页表单。</span><span class="sxs-lookup"><span data-stu-id="c8a1e-127">When generating the 1095-C form enter in the appropriate calendar or tax year as well as if you want to print the two-page or three page form.</span></span> <span data-ttu-id="c8a1e-128">仅当雇主提供自保型保险且员工的投保依赖方（包括自己在内）超过六位时，才需要三页表单。</span><span class="sxs-lookup"><span data-stu-id="c8a1e-128">The three-page form is only needed if the Employer provided self-insured coverage and an employee has more than six covered dependents including themselves.</span></span> <span data-ttu-id="c8a1e-129">生成两页表单时，系统将自动检测员工是否有 6 位以上投保依赖方，且在生成表单时不会包括此员工。</span><span class="sxs-lookup"><span data-stu-id="c8a1e-129">When generating the Two page form the system will automatically detect if an employee has more than 6 covered dependents and will not include that employee when generating the form.</span></span> <span data-ttu-id="c8a1e-130">此外，在生成三页表单时，系统将仅包括有六位以上投保依赖方的员工。</span><span class="sxs-lookup"><span data-stu-id="c8a1e-130">Additionally, when generating the three-page form the system will only include those employees that have more than six covered dependents.</span></span>

## <a name="viewing-information"></a><span data-ttu-id="c8a1e-131">查看信息</span><span class="sxs-lookup"><span data-stu-id="c8a1e-131">Viewing information</span></span>
<span data-ttu-id="c8a1e-132">您可以使用**工作人员的平价医疗保险范围**页查看哪些员工已分配到各保险范围组、哪些员工不需要包括在报表上以及哪些员工未分配。</span><span class="sxs-lookup"><span data-stu-id="c8a1e-132">You can use the **Worker Affordable Care coverage** page to see which employees have been assigned to each coverage group, which employees don’t need to be included on a report, and which employees are unassigned.</span></span>

<span data-ttu-id="c8a1e-133">如果平价医疗保险范围组的任何默认值已被覆盖，被更改的值的旁边将显示星号。</span><span class="sxs-lookup"><span data-stu-id="c8a1e-133">If any of the default values from the Affordable Care coverage group have been overridden an asterisk will appear next to the value that was changed.</span></span> <span data-ttu-id="c8a1e-134">如果所有 12 个月的值相同且未被覆盖，该值将打印在**所有 12 个月**列。</span><span class="sxs-lookup"><span data-stu-id="c8a1e-134">If the values for all 12 months are the same and haven’t been overridden, the value will print in the **All 12 months** column.</span></span>

<span data-ttu-id="c8a1e-135">您还可以使用查询窗口以了解哪些员工被标记为非 ACA 可申报，意味着您无需跟踪是否已向其提供保险范围，且在年终时无需向其签发 1095-C。</span><span class="sxs-lookup"><span data-stu-id="c8a1e-135">You can also use the inquiry window to understand which employees have been flagged as not ACA reportable, meaning you don’t need to track whether coverage was offered to them and will not need to issue a 1095-C to them at the end of the year.</span></span> <span data-ttu-id="c8a1e-136">通过选择**筛选方式**字段中的**非 ACA 可申报**，您可以生成已标记为不接收 1095-C 的所有员工的列表。</span><span class="sxs-lookup"><span data-stu-id="c8a1e-136">By selecting **Not ACA reportable** in the **Filter by** field, you can generate a list of all employees that have been flagged to not receive a 1095-C.</span></span>

<span data-ttu-id="c8a1e-137">除了查看非 ACA 可申报的员工的列表外，您还可以查看未分配（**ACA 申报保险范围**字段为空）的任何员工或已分配到平价医疗保险范围组但在**年度**字段所选年份到期的任何员工。</span><span class="sxs-lookup"><span data-stu-id="c8a1e-137">In addition to viewing a list of employees that are not ACA reportable, you can also view any employees who are unassigned (the **ACA Report coverage** field is empty) or that have been assigned to an Affordable Care coverage group that is expired for the year selected in the **Year** field.</span></span>

<span data-ttu-id="c8a1e-138">您可以将使用任何筛选方式生成的员工列表导出到 Excel。</span><span class="sxs-lookup"><span data-stu-id="c8a1e-138">You can export lists of employees that were generated using any of the filtering options to Excel.</span></span>

<span data-ttu-id="c8a1e-139">如果您需要报告投保的个人，因为作为雇主，您提供自保型保险范围，您还可以通过选择操作窗格条上的查看依赖方保险范围操作查看已标记为 **ACA 可申报**的福利计划下涵盖的任何依赖方。</span><span class="sxs-lookup"><span data-stu-id="c8a1e-139">If you need to report covered individuals because as an employer you provide self-insured coverage you can also view any dependents covered under benefit plans that have been marked as **ACA reportable** by selecting the View Dependent coverage action on the action pane strip.</span></span>

<span data-ttu-id="c8a1e-140">**注意：**仅其计划已标记为 **ACA 可申报**的福利才会显示在查询窗口中。</span><span class="sxs-lookup"><span data-stu-id="c8a1e-140">**Note:** Only benefits whose plan has been marked as **ACA reportable** will display in the inquiry window.</span></span>

