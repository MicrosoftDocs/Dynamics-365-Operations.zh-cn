---
title: 创建平价医疗法案 (ACA) 报告
description: 平价医疗法案 (ACA) 报告生成表单 1095-B 和 1095-C，来支持平价医疗法案的 **雇主授权单** 部分。
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 055de1f0ff3f8fd4fadba0a685fd703b9d19d918
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805986"
---
# <a name="generate-aca-reports"></a><span data-ttu-id="cb548-103">生成 ACA 报表</span><span class="sxs-lookup"><span data-stu-id="cb548-103">Generate ACA reports</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="cb548-104">平价医疗法案 (ACA) 报告生成表单 1095-B 和 1095-C，来支持平价医疗法案的 **雇主授权单** 部分。</span><span class="sxs-lookup"><span data-stu-id="cb548-104">Affordable Care Act (ACA) reporting generates forms 1095-B and 1095-C in support of the **Employer Mandate** portion of the Affordable Care Act.</span></span>

> [!NOTE]
> <span data-ttu-id="cb548-105">ACA 报告仅对美国的法人启用。</span><span class="sxs-lookup"><span data-stu-id="cb548-105">ACA reporting is only enabled for legal entities in the United States.</span></span>

## <a name="getting-started"></a><span data-ttu-id="cb548-106">入门</span><span class="sxs-lookup"><span data-stu-id="cb548-106">Getting started</span></span>

<span data-ttu-id="cb548-107">要跟踪表单 1095-B 和 1095-C 的信息，必须先创建一个或多个平价医疗保险范围组。</span><span class="sxs-lookup"><span data-stu-id="cb548-107">To track information for forms 1095-B and 1095-C, you must first create one or more Affordable care coverage groups.</span></span> <span data-ttu-id="cb548-108">平价医疗保险范围组指示：</span><span class="sxs-lookup"><span data-stu-id="cb548-108">Affordable Care coverage groups indicate:</span></span>

- <span data-ttu-id="cb548-109">为员工提供的保险范围</span><span class="sxs-lookup"><span data-stu-id="cb548-109">The offer of coverage for an employee</span></span>
- <span data-ttu-id="cb548-110">如果成本高于联邦贫困线，员工应承担的最低成本每月保费的份额</span><span class="sxs-lookup"><span data-stu-id="cb548-110">The employee’s share of the lowest cost monthly premium, if the cost is above the federal poverty line</span></span>
- <span data-ttu-id="cb548-111">雇主使用的安全港（如果适用）</span><span class="sxs-lookup"><span data-stu-id="cb548-111">Safe Harbor used by the employer, if applicable</span></span>

<span data-ttu-id="cb548-112">平价医疗保险范围组让您可以管理这些字段的信息，而无需更改条件相同的每个员工记录。</span><span class="sxs-lookup"><span data-stu-id="cb548-112">Affordable Care coverage groups allow you to manage the information for these fields without changing every employee record where the conditions are the same.</span></span> <span data-ttu-id="cb548-113">您可以使用页面上的 **成批分配** 选项轻松地将平价医疗保险范围组分配给一个或多个员工。</span><span class="sxs-lookup"><span data-stu-id="cb548-113">You can easily assign Affordable Care coverage groups to one or more employees by using the **Mass assign** option on the page.</span></span>

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a><span data-ttu-id="cb548-114">维护保险范围组的多个版本</span><span class="sxs-lookup"><span data-stu-id="cb548-114">Maintaining multiple versions of a coverage group</span></span>

<span data-ttu-id="cb548-115">您可以任何维护保险范围组的多个版本。</span><span class="sxs-lookup"><span data-stu-id="cb548-115">You can maintain multiple versions of any coverage group.</span></span> <span data-ttu-id="cb548-116">此功能让您可以进行更改，而无需创建新组，然后将员工重新分配到组中。</span><span class="sxs-lookup"><span data-stu-id="cb548-116">This functionality allows you to make changes without having to create a new group and reassign employees to it.</span></span> 

<span data-ttu-id="cb548-117">创建 ACA 保险范围组后，您可以使用 **成批分配** 选项将组分配给员工。</span><span class="sxs-lookup"><span data-stu-id="cb548-117">After you’ve created ACA coverage groups, you can mass assign the groups to employees with the **Mass assignment** option.</span></span> <span data-ttu-id="cb548-118">您还可以单独指示是否跟踪和报告 ACA 信息，以及将员工分配到平价医疗保险范围组。</span><span class="sxs-lookup"><span data-stu-id="cb548-118">You can also individually indicate whether to track and report ACA information, and assign an employee to an Affordable Care coverage group.</span></span>

<span data-ttu-id="cb548-119">您不需要跟踪某些 ACA 保险范围信息，如兼职员工的信息。</span><span class="sxs-lookup"><span data-stu-id="cb548-119">You don't need to track some ACA coverage information, such as for part-time employees.</span></span> <span data-ttu-id="cb548-120">在这种情况下，将 **报告保险范围** 字段设置为 **否**。</span><span class="sxs-lookup"><span data-stu-id="cb548-120">In this case, set the **Report coverage** field to **No**.</span></span> <span data-ttu-id="cb548-121">虽然您必须将每个具有可追踪 ACA 信息的员工分配到平价医疗保险范围组，但您仍可以在几个月内使用不同的值更改以下选项：</span><span class="sxs-lookup"><span data-stu-id="cb548-121">Although you must assign each employee with trackable ACA information to an Affordable Care coverage group, you can still change the following options for months with different values:</span></span>

- <span data-ttu-id="cb548-122">**提供的保险范围**</span><span class="sxs-lookup"><span data-stu-id="cb548-122">**Offer of coverage**</span></span>
- <span data-ttu-id="cb548-123">**员工承担的成本比例**</span><span class="sxs-lookup"><span data-stu-id="cb548-123">**Employee share of cost**</span></span>
- <span data-ttu-id="cb548-124">**安全港**</span><span class="sxs-lookup"><span data-stu-id="cb548-124">**Safe Harbor**</span></span>

<span data-ttu-id="cb548-125">要输入平价医疗保险范围组值的例外，选择 **工作人员详细信息** 页上的 **平价医疗保险范围** 链接，该链接位于 **雇用选项卡** 上的 **附加信息** 部分下。</span><span class="sxs-lookup"><span data-stu-id="cb548-125">To enter exceptions for Affordable Care coverage group values, select the **Affordable Care Coverage** link on the **Worker detail** page under the **Additional information** section on the **Employment tab**.</span></span>

## <a name="reporting-health-care-coverage"></a><span data-ttu-id="cb548-126">报告医疗保险范围</span><span class="sxs-lookup"><span data-stu-id="cb548-126">Reporting health care coverage</span></span>

<span data-ttu-id="cb548-127">除了跟踪已向全职员工提供的健康保险范围以外，如果雇主为登记的员工（无论其雇佣状态是否为全职或兼职）提供由雇主赞助的自保型保险健康保险范围，则需要在 1095-C 上报告附加信息。</span><span class="sxs-lookup"><span data-stu-id="cb548-127">In addition to tracking health insurance coverage offered to full-time employees, if the employer offers employer-sponsored self-insured health coverage for which the employee is enrolled (regardless of whether their employment status is full-time or part-time), additional information needs to be reported on the 1095-C.</span></span> <span data-ttu-id="cb548-128">由雇主赞助的福利计划涵盖的每位员工（包括依赖方）需要包含在保险的月份的报表上。</span><span class="sxs-lookup"><span data-stu-id="cb548-128">Each employee (including dependents) covered by the employer-sponsored benefit plans needs to be included on the report for the months they were covered.</span></span> 

<span data-ttu-id="cb548-129">您可以通过选择 **ACA 可报告** 复选框指示是否必须报告每个福利计划。</span><span class="sxs-lookup"><span data-stu-id="cb548-129">You can indicate whether or not each benefit plan must be reported by selecting the **ACA reportable** check box.</span></span>

<span data-ttu-id="cb548-130">此外，如果员工已选择将其任何依赖方涵盖在福利下，您可以在 **维护福利** 页上指示为每位员工的依赖方投保的日期。</span><span class="sxs-lookup"><span data-stu-id="cb548-130">In addition, if employees have chosen to have any of their dependents covered under a benefit, you can indicate the dates the dependent was covered for each employee on the **Maintain benefits** page.</span></span> <span data-ttu-id="cb548-131">要指示依赖方是否涵盖在福利下，选择 **依赖方** 快速选项卡的操作窗格中的 **编辑** 按钮。</span><span class="sxs-lookup"><span data-stu-id="cb548-131">To indicate that the dependent is covered under the benefit, select the **Edit** button in the action pane of the **Dependents** fast tab.</span></span>

<span data-ttu-id="cb548-132">在 **依赖方保险范围日期管理器** 页面，可以指示福利涵盖依赖方的日期。</span><span class="sxs-lookup"><span data-stu-id="cb548-132">On the **Dependent coverage date manager** page, you can indicate the dates the dependent was covered by the benefit.</span></span> <span data-ttu-id="cb548-133">在此页面上输入日期将自动选择 **维护福利** 页面上的 **已涵盖** 复选框。</span><span class="sxs-lookup"><span data-stu-id="cb548-133">Entering dates on this page will automatically select the **Covered** checkbox on the **Maintain benefits** page.</span></span>

## <a name="generate-1095-b-and-1095-c-forms"></a><span data-ttu-id="cb548-134">生成 1095-B 和 1095-C 表单</span><span class="sxs-lookup"><span data-stu-id="cb548-134">Generate 1095-B and 1095-C forms</span></span>

<span data-ttu-id="cb548-135">您还可以从产品内部生成 1095-B 和 1095-C 表单，并将其分配给每个员工。</span><span class="sxs-lookup"><span data-stu-id="cb548-135">You can also generate 1095-B and 1095-C forms from within the product, and distribute them to each of your employees.</span></span> <span data-ttu-id="cb548-136">系统还可以电子生成 1095-C 表单和 1094-C IRS 传送单。</span><span class="sxs-lookup"><span data-stu-id="cb548-136">The system can also electronically generate 1095-C forms and the 1094-C IRS transmittal files.</span></span>  

<span data-ttu-id="cb548-137">在生成 1095-C 表单时，请输入相应的纳税年度并指示是否应隐藏社会保险号。</span><span class="sxs-lookup"><span data-stu-id="cb548-137">When generating the 1095-C form, enter the appropriate tax year and indicate if social security numbers should be masked.</span></span> <span data-ttu-id="cb548-138">如果您为 500 名以上员工打印 1095-C 表单，您将收到多个 PDF 文件。</span><span class="sxs-lookup"><span data-stu-id="cb548-138">If you're printing 1095-C forms for more than 500 employees, you'll receive more than one PDF file.</span></span> <span data-ttu-id="cb548-139">建议您在 **文档管理参数** 窗口中将 **最大文件大小** 增加到 150 MB。</span><span class="sxs-lookup"><span data-stu-id="cb548-139">It’s recommended that you increase the **Maximum file size** in the **Document management parameters** window to 150 MB.</span></span>

## <a name="viewing-information"></a><span data-ttu-id="cb548-140">查看信息</span><span class="sxs-lookup"><span data-stu-id="cb548-140">Viewing information</span></span>

<span data-ttu-id="cb548-141">您可以使用 **工作人员的平价医疗保险范围** 页查看哪些员工已分配到各保险范围组、哪些员工不需要包括在报表上以及哪些员工未分配。</span><span class="sxs-lookup"><span data-stu-id="cb548-141">You can use the **Worker Affordable Care coverage** page to see which employees have been assigned to each coverage group, which employees don’t need to be included on a report, and which employees are unassigned.</span></span>

<span data-ttu-id="cb548-142">如果平价医疗保险范围组的任何默认值已被替代，被更改的值的旁边将显示星号。</span><span class="sxs-lookup"><span data-stu-id="cb548-142">If any of the default values from the Affordable Care coverage group have been overridden, an asterisk will appear next to the value that was changed.</span></span> <span data-ttu-id="cb548-143">如果所有 12 个月的值相同且未被覆盖，该值将打印在 **所有 12 个月** 列。</span><span class="sxs-lookup"><span data-stu-id="cb548-143">If the values for all 12 months are the same and haven’t been overridden, the value will print in the **All 12 months** column.</span></span>

<span data-ttu-id="cb548-144">您还可以使用查询窗口来了解哪些员工被标记为非 ACA 可报告。</span><span class="sxs-lookup"><span data-stu-id="cb548-144">You can also use the inquiry window to understand which employees have been flagged as not ACA reportable.</span></span> <span data-ttu-id="cb548-145">您无需跟踪是否向他们提供了保险范围，也不需要在年底向他们发放 1095-C。</span><span class="sxs-lookup"><span data-stu-id="cb548-145">You don’t need to track whether coverage was offered to them and won't need to issue a 1095-C to them at the end of the year.</span></span> <span data-ttu-id="cb548-146">在 **筛选方式** 字段中选择 **非 ACA 可报告** 将生成不会收到 1095-C 的所有员工的列表。</span><span class="sxs-lookup"><span data-stu-id="cb548-146">Select **Not ACA reportable** in the **Filter by** field to generate a list of all employees who won't receive a 1095-C.</span></span>

<span data-ttu-id="cb548-147">此外，您还可以查看未分配（**ACA 报告保险范围** 字段为空）的任何员工或已分配到平价医疗保险范围组但在 **年度** 字段所选年份到期的任何员工。</span><span class="sxs-lookup"><span data-stu-id="cb548-147">In addition, you can view any employees who are unassigned (the **ACA Report coverage** field is empty) or who have been assigned to an Affordable Care coverage group that is expired for the year selected in the **Year** field.</span></span>

<span data-ttu-id="cb548-148">您可以将使用任何筛选方式生成的员工列表导出到 Excel。</span><span class="sxs-lookup"><span data-stu-id="cb548-148">You can export lists of employees that were generated using any of the filtering options to Excel.</span></span>

<span data-ttu-id="cb548-149">如果由于您提供自保型保险范围而需要报告投保的个人，可以查看标记为 **ACA 可报告** 的福利计划覆盖的任何依赖方。</span><span class="sxs-lookup"><span data-stu-id="cb548-149">If you need to report covered individuals because you provide self-insured coverage, you can view any dependents covered under benefit plans marked as **ACA reportable**.</span></span> <span data-ttu-id="cb548-150">在操作窗格上选择 **查看依赖方保险范围**。</span><span class="sxs-lookup"><span data-stu-id="cb548-150">Select **View Dependent coverage** on the action pane.</span></span>

> [!NOTE]
> <span data-ttu-id="cb548-151">仅标记为 **ACA 可报告** 的福利计划将显示在查询窗口中。</span><span class="sxs-lookup"><span data-stu-id="cb548-151">Only benefit plans marked as **ACA reportable** display in the inquiry window.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]