---
title: 在“福利管理”中生成平价医疗法案报告
description: 本主题介绍“福利管理”如何帮助您跟踪平价医疗法案 (ACA) 雇主授权单的表单 1095-B 和表单 1095-C 上报告的信息。
author: andreabichsel
manager: tfehr
ms.date: 12/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 2e4b250f4a059719067a9e19bbf3ce4aecc9bb1f
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111676"
---
# <a name="generate-aca-reports-in-benefits-management"></a><span data-ttu-id="c45e3-103">在“福利管理”中生成 ACA 报告</span><span class="sxs-lookup"><span data-stu-id="c45e3-103">Generate ACA reports in Benefits management</span></span>

<span data-ttu-id="c45e3-104">“福利管理”帮助您跟踪平价医疗法案 (ACA) 雇主授权单的表单 1095-B 和表单 1095-C 上报告的信息。</span><span class="sxs-lookup"><span data-stu-id="c45e3-104">Benefits management helps you track information that is reported on Form 1095-B and Form 1095-C for the Affordable Care Act (ACA) employer mandate.</span></span> <span data-ttu-id="c45e3-105">与旧 **福利** 工作区中的 ACA 报告功能一样，此功能仅适用于美国的法人。</span><span class="sxs-lookup"><span data-stu-id="c45e3-105">Like the ACA reporting capability in the old **Benefits** workspace, this functionality applies only to legal entities in the United States.</span></span>

<span data-ttu-id="c45e3-106">要使用此功能，必须首先打开 **高级福利管理**。</span><span class="sxs-lookup"><span data-stu-id="c45e3-106">To use this functionality, you must first turn on **Advanced Benefits Management**.</span></span> <span data-ttu-id="c45e3-107">有关详细信息，包括有关“福利管理”的重要说明，请参阅[启用或禁用“福利管理”](hr-admin-manage-features.md#enable-or-disable-benefits-management)。</span><span class="sxs-lookup"><span data-stu-id="c45e3-107">For more information, including important caveats about Benefits management, see [Enable or disable Benefits management](hr-admin-manage-features.md#enable-or-disable-benefits-management).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c45e3-108">您只能从 **福利管理** 工作区或旧 **福利** 工作区使用 ACA 报告，不能同时在两个位置使用。</span><span class="sxs-lookup"><span data-stu-id="c45e3-108">You can use ACA reporting only from either the **Benefits management** workspace or the old **Benefits** workspace, not from both.</span></span> <span data-ttu-id="c45e3-109">例如，如果您切换到“福利管理”，则只能从 **福利管理** 工作区使用 ACA 报告，而不能从旧 **福利** 工作区使用。</span><span class="sxs-lookup"><span data-stu-id="c45e3-109">For example, if you switched to Benefits management, ACA reporting is available only from the **Benefits management** workspace, not from the old **Benefits** workspace.</span></span>
>
> <span data-ttu-id="c45e3-110">如果您在注册年份中间切换到“福利管理”，则必须在“福利管理”中为全年正确配置员工数据。</span><span class="sxs-lookup"><span data-stu-id="c45e3-110">If you switch to Benefits management in the middle of an enrollment year, you must correctly configure employee data for the whole year in Benefits management.</span></span> <span data-ttu-id="c45e3-111">这样，可以确保会在全年收到准确的报告信息。</span><span class="sxs-lookup"><span data-stu-id="c45e3-111">In this way, you ensure that you will receive accurate reporting information for the whole year.</span></span>

## <a name="getting-started"></a><span data-ttu-id="c45e3-112">入门</span><span class="sxs-lookup"><span data-stu-id="c45e3-112">Getting started</span></span>

<span data-ttu-id="c45e3-113">要跟踪 1095 表单的信息，首先创建一个或多个平价医疗保险范围组。</span><span class="sxs-lookup"><span data-stu-id="c45e3-113">To track information for 1095 forms, first create one or more Affordable Care coverage groups.</span></span> <span data-ttu-id="c45e3-114">这些组指示以下信息：</span><span class="sxs-lookup"><span data-stu-id="c45e3-114">These groups indicate the following information:</span></span>

- <span data-ttu-id="c45e3-115">提供给员工的保险范围</span><span class="sxs-lookup"><span data-stu-id="c45e3-115">The offer of coverage that was provided to an employee</span></span>
- <span data-ttu-id="c45e3-116">如果成本高于联邦贫困线，员工应承担的最低成本每月保费的份额</span><span class="sxs-lookup"><span data-stu-id="c45e3-116">The employee's share of the lowest-cost monthly premium, if the cost is above the federal poverty line</span></span>
- <span data-ttu-id="c45e3-117">雇主使用的安全港（如果适用）</span><span class="sxs-lookup"><span data-stu-id="c45e3-117">The safe harbor that is used by the employer, if applicable</span></span>

<span data-ttu-id="c45e3-118">平价医疗保险范围组帮助您管理具有相同条件的多个员工记录的这一信息。</span><span class="sxs-lookup"><span data-stu-id="c45e3-118">Affordable Care coverage groups help you manage this information for multiple employee records that have the same conditions.</span></span> <span data-ttu-id="c45e3-119">您可以轻松地将组分配给一个或多个员工。</span><span class="sxs-lookup"><span data-stu-id="c45e3-119">You can easily assign groups to one or more employees.</span></span>

### <a name="create-or-edit-an-affordable-care-coverage-group"></a><span data-ttu-id="c45e3-120">创建或编辑平价医疗保险范围组</span><span class="sxs-lookup"><span data-stu-id="c45e3-120">Create or edit an Affordable Care coverage group</span></span>

1. <span data-ttu-id="c45e3-121">在 **福利管理** 工作区，选择 **平价医疗保险范围组**。</span><span class="sxs-lookup"><span data-stu-id="c45e3-121">In the **Benefits management** workspace, select **Affordable Care coverage group**.</span></span>

    ![选择“平价医疗保险范围组”](./media/hr-benefits-management-aca-coverage-group.png)

2. <span data-ttu-id="c45e3-123">选择 **新建** 创建新的平价医疗保险范围组，或选择 **编辑** 更改现有组。</span><span class="sxs-lookup"><span data-stu-id="c45e3-123">Select **New** to create a new Affordable Care coverage group or **Edit** to change an existing group.</span></span>

    ![选择“新建”或“编辑”](./media/hr-benefits-management-aca-new.png)

3. <span data-ttu-id="c45e3-125">设置以下字段。</span><span class="sxs-lookup"><span data-stu-id="c45e3-125">Set the following fields.</span></span>

    | <span data-ttu-id="c45e3-126">字段</span><span class="sxs-lookup"><span data-stu-id="c45e3-126">Field</span></span> | <span data-ttu-id="c45e3-127">说明</span><span class="sxs-lookup"><span data-stu-id="c45e3-127">Description</span></span> |
    |---|---|
    | <span data-ttu-id="c45e3-128">姓名</span><span class="sxs-lookup"><span data-stu-id="c45e3-128">Name</span></span> | <span data-ttu-id="c45e3-129">为组输入名称。</span><span class="sxs-lookup"><span data-stu-id="c45e3-129">Enter a name for the group.</span></span> |
    | <span data-ttu-id="c45e3-130">说明</span><span class="sxs-lookup"><span data-stu-id="c45e3-130">Description</span></span> | <span data-ttu-id="c45e3-131">输入组的描述。</span><span class="sxs-lookup"><span data-stu-id="c45e3-131">Enter a description of the group.</span></span> |
    | <span data-ttu-id="c45e3-132">提供的保险范围</span><span class="sxs-lookup"><span data-stu-id="c45e3-132">Offer of coverage</span></span> | <span data-ttu-id="c45e3-133">提供给员工、员工配偶或伴侣和员工依赖方的保险范围。</span><span class="sxs-lookup"><span data-stu-id="c45e3-133">The coverage that is offered to employees, their spouse or partner, and their dependents.</span></span> |
    | <span data-ttu-id="c45e3-134">员工承担的成本比例</span><span class="sxs-lookup"><span data-stu-id="c45e3-134">Employee share of cost</span></span> | <span data-ttu-id="c45e3-135">员工负责的金额。</span><span class="sxs-lookup"><span data-stu-id="c45e3-135">The amount that the employee is responsible for.</span></span> |
    | <span data-ttu-id="c45e3-136">适用的部分 4980H 安全港</span><span class="sxs-lookup"><span data-stu-id="c45e3-136">Applicable section 4980H safe harbor</span></span> | <span data-ttu-id="c45e3-137">4980H 安全港或过渡救济代码。</span><span class="sxs-lookup"><span data-stu-id="c45e3-137">The 4980H safe harbor or transition relief code.</span></span> |
    | <span data-ttu-id="c45e3-138">计划开始月份</span><span class="sxs-lookup"><span data-stu-id="c45e3-138">Plan start month</span></span> | <span data-ttu-id="c45e3-139">选择您的福利计划年份开始的日历月。</span><span class="sxs-lookup"><span data-stu-id="c45e3-139">Select the calendar month when your benefit plan year begins.</span></span> |
    | <span data-ttu-id="c45e3-140">组生效日期</span><span class="sxs-lookup"><span data-stu-id="c45e3-140">Group valid from</span></span> | <span data-ttu-id="c45e3-141">此记录有效的第一个日期。</span><span class="sxs-lookup"><span data-stu-id="c45e3-141">The first date when this record is valid.</span></span> |
    | <span data-ttu-id="c45e3-142">组失效日期</span><span class="sxs-lookup"><span data-stu-id="c45e3-142">Group valid through</span></span> | <span data-ttu-id="c45e3-143">此记录有效的最后一个日期。</span><span class="sxs-lookup"><span data-stu-id="c45e3-143">The last date when this record is valid.</span></span> <span data-ttu-id="c45e3-144">如果没有到期日期，输入 **从不**。</span><span class="sxs-lookup"><span data-stu-id="c45e3-144">If there is no expiration date, enter **Never**.</span></span> |

    ![创建覆盖范围组](./media/hr-benefits-management-aca-new-group.png)

4. <span data-ttu-id="c45e3-146">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="c45e3-146">Select **Save**.</span></span>

### <a name="assign-multiple-employees-to-an-affordable-care-coverage-group"></a><span data-ttu-id="c45e3-147">将多个员工分配到平价医疗保险范围组</span><span class="sxs-lookup"><span data-stu-id="c45e3-147">Assign multiple employees to an Affordable Care coverage group</span></span>

1. <span data-ttu-id="c45e3-148">在 **福利管理** 工作区，选择 **平价医疗保险范围组**。</span><span class="sxs-lookup"><span data-stu-id="c45e3-148">In the **Benefits management** workspace, select **Affordable Care coverage group**.</span></span>
2. <span data-ttu-id="c45e3-149">选择要向其中分配员工的组。</span><span class="sxs-lookup"><span data-stu-id="c45e3-149">Select the group to assign employees to.</span></span>
3. <span data-ttu-id="c45e3-150">选择 **成批分配**。</span><span class="sxs-lookup"><span data-stu-id="c45e3-150">Select **Mass assignment**.</span></span>

    ![选择“成批分配”](./media/hr-benefits-management-aca-mass-assignment.png)

4. <span data-ttu-id="c45e3-152">在列表中选择员工，然后选择 **分配**。</span><span class="sxs-lookup"><span data-stu-id="c45e3-152">Select employees in the list, and then select **Assign**.</span></span>

    ![将选定的员工分配到组](./media/hr-benefits-management-aca-assign-coverage-group.png)

## <a name="maintain-multiple-versions-of-coverage-options"></a><span data-ttu-id="c45e3-154">维护保险范围选项的多个版本</span><span class="sxs-lookup"><span data-stu-id="c45e3-154">Maintain multiple versions of coverage options</span></span>

<span data-ttu-id="c45e3-155">您可以任何维护保险范围组的多个版本。</span><span class="sxs-lookup"><span data-stu-id="c45e3-155">You can maintain multiple versions of any coverage group.</span></span> <span data-ttu-id="c45e3-156">当您的组织或所提供的福利发生变化时，您可以保持组的信息为最新，而不必创建新组，然后将员工重新分配到组中。</span><span class="sxs-lookup"><span data-stu-id="c45e3-156">When something changes in your organization or the benefits that are offered, you can keep the group's information up to date without having to create a new group and reassign employees to it.</span></span>

<span data-ttu-id="c45e3-157">创建平价医疗保险范围组后，您可以将员工成批分配到组中。</span><span class="sxs-lookup"><span data-stu-id="c45e3-157">After you've created Affordable Care coverage groups, you can mass-assign employees to them.</span></span> <span data-ttu-id="c45e3-158">您还可以将员工单独分配到组，并指示是否跟踪和报告 ACA 信息。</span><span class="sxs-lookup"><span data-stu-id="c45e3-158">You can also individually assign employees to groups, and indicate whether ACA information is tracked and reported.</span></span>

<span data-ttu-id="c45e3-159">如果您不必跟踪和报告员工的 ACA 信息，可以将 **报告保险范围** 选项设置为 **否**。</span><span class="sxs-lookup"><span data-stu-id="c45e3-159">If you don't have to track and report ACA information for an employee, you can set the **Report coverage** option to **No**.</span></span> <span data-ttu-id="c45e3-160">例如，您可能有不需要 ACA 报告的兼职员工。</span><span class="sxs-lookup"><span data-stu-id="c45e3-160">For example, you might have part-time employees who don't require ACA reporting.</span></span>

### <a name="override-default-values-for-an-employee"></a><span data-ttu-id="c45e3-161">替代员工的默认值</span><span class="sxs-lookup"><span data-stu-id="c45e3-161">Override default values for an employee</span></span>

<span data-ttu-id="c45e3-162">对于分配到平价医疗保险范围组的员工，您可以在需要不同值的任何月份更改以下选项：</span><span class="sxs-lookup"><span data-stu-id="c45e3-162">For employees who are assigned to an Affordable Care coverage group, you can change the following options for any months that require different values:</span></span>

- <span data-ttu-id="c45e3-163">提供的保险范围</span><span class="sxs-lookup"><span data-stu-id="c45e3-163">Offer of coverage</span></span>
- <span data-ttu-id="c45e3-164">员工承担的成本比例</span><span class="sxs-lookup"><span data-stu-id="c45e3-164">Employee share of cost</span></span>
- <span data-ttu-id="c45e3-165">适用的部分 4980H 安全港</span><span class="sxs-lookup"><span data-stu-id="c45e3-165">Applicable section 4980H safe harbor</span></span>

> [!NOTE]
> <span data-ttu-id="c45e3-166">对于 2020 ACA 报告，您必须在表单 1095-C 中报告工作和家庭邮政编码。</span><span class="sxs-lookup"><span data-stu-id="c45e3-166">For 2020 ACA reports, you must report both work and home ZIP Codes on Form 1095-C.</span></span> <span data-ttu-id="c45e3-167">值将根据当前活动位置自动填充。</span><span class="sxs-lookup"><span data-stu-id="c45e3-167">Values are automatically filled in, based on current active locations.</span></span> <span data-ttu-id="c45e3-168">如果一年中的任何时候两个位置都不同，则必须替代此值。</span><span class="sxs-lookup"><span data-stu-id="c45e3-168">If either location was different during any part of the year, you must override the value.</span></span> <span data-ttu-id="c45e3-169">仅当 **提供的保险范围** 代码包含 **1L** 到 **1Q** 时，1095-C 报告的 **邮政编码** 字段（第 17 行）才会填充，如下所示：</span><span class="sxs-lookup"><span data-stu-id="c45e3-169">The **ZIP Code** field (line 17) of the 1095-C report is filled in only if the **Offer of coverage** code contains **1L** through **1Q**, as follows:</span></span>
>
> - <span data-ttu-id="c45e3-170">**1L、1M 或 1N：** 主要住所的邮政编码</span><span class="sxs-lookup"><span data-stu-id="c45e3-170">**1L, 1M, or 1N:** The primary residence ZIP Code</span></span>
> - <span data-ttu-id="c45e3-171">**1O、1P、1Q：** 主要工作邮政编码</span><span class="sxs-lookup"><span data-stu-id="c45e3-171">**1O, 1P, 1Q:** The primary work ZIP Code</span></span>

<span data-ttu-id="c45e3-172">要为平价医疗保险范围组的任何值输入例外，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="c45e3-172">To enter exceptions for any values of an Affordable Care coverage group, follow these steps.</span></span>

1. <span data-ttu-id="c45e3-173">在 **人事管理** 工作区，选择 **链接**，然后选择 **工作人员**。</span><span class="sxs-lookup"><span data-stu-id="c45e3-173">In the **Personnel management** workspace, select **Links**, and then select **Workers**.</span></span>
2. <span data-ttu-id="c45e3-174">在列表中选择员工。</span><span class="sxs-lookup"><span data-stu-id="c45e3-174">Select the employee in the list.</span></span>
3. <span data-ttu-id="c45e3-175">在 **雇用** 选项卡上，在 **更多信息** 部分，选择 **平价医疗保险范围**。</span><span class="sxs-lookup"><span data-stu-id="c45e3-175">On the **Employment** tab, in the **More information** section, select **Affordable Care coverage**.</span></span>

    ![为一个员工更改选项](./media/hr-benefits-management-aca-change-single-employee.png)

4. <span data-ttu-id="c45e3-177">选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="c45e3-177">Select **Edit**.</span></span>
5. <span data-ttu-id="c45e3-178">对于需要更改的每个月份，选中 **替代默认值** 复选框，然后根据需要更改其他值。</span><span class="sxs-lookup"><span data-stu-id="c45e3-178">For each month that requires changes, select the **Override default** check box, and then change the other values as required.</span></span>

    ![替代默认值](./media/hr-benefits-management-aca-override-default.png)

6. <span data-ttu-id="c45e3-180">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="c45e3-180">Select **Save**.</span></span>

## <a name="report-health-care-coverage"></a><span data-ttu-id="c45e3-181">报告健康医疗保险范围</span><span class="sxs-lookup"><span data-stu-id="c45e3-181">Report health care coverage</span></span>

<span data-ttu-id="c45e3-182">您必须跟踪全职和兼职员工的任何雇主赞助的自保型保险健康保险范围。</span><span class="sxs-lookup"><span data-stu-id="c45e3-182">You must track any employer-sponsored, self-insured health care coverage for full-time and part-time employees.</span></span> <span data-ttu-id="c45e3-183">将每个员工及其依赖方包括在保险覆盖月份的 1095-C 报告中。</span><span class="sxs-lookup"><span data-stu-id="c45e3-183">Include each employee, together with their dependents, on the 1095-C report for the months when they were covered.</span></span>

<span data-ttu-id="c45e3-184">要指示是否必须报告福利计划，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="c45e3-184">To indicate whether a benefit plan must be reported, follow these steps.</span></span>

1. <span data-ttu-id="c45e3-185">在 **福利管理** 工作区中，选择 **福利计划**。</span><span class="sxs-lookup"><span data-stu-id="c45e3-185">In the **Benefits management** workspace, select **Benefit plans**.</span></span>
2. <span data-ttu-id="c45e3-186">选择要报告的福利计划。</span><span class="sxs-lookup"><span data-stu-id="c45e3-186">Select the benefit plan to report.</span></span>
3. <span data-ttu-id="c45e3-187">选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="c45e3-187">Select **Edit**.</span></span>
4. <span data-ttu-id="c45e3-188">将 **根据平价医疗法案进行报告** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="c45e3-188">Set the **Reported under the Affordable Care Act** option to **Yes**.</span></span>

    ![报告医疗保险范围](./media/hr-benefits-management-aca-report-coverage.png)

5. <span data-ttu-id="c45e3-190">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="c45e3-190">Select **Save**.</span></span>

<span data-ttu-id="c45e3-191">如果员工为依赖方选择健康医疗保险范围，依赖方的覆盖期间由依赖方登记或删除的日期确定。</span><span class="sxs-lookup"><span data-stu-id="c45e3-191">If an employee chooses health care coverage for a dependent, the dependent's coverage period is determined by the date when the dependent was enrolled or removed.</span></span> <span data-ttu-id="c45e3-192">依赖方的覆盖日期根据登记年中份依赖方在计划中具备资格且处于活动状态的持续期间自动计算。</span><span class="sxs-lookup"><span data-stu-id="c45e3-192">Coverage dates for dependents are automatically calculated based on the period when the dependent was eligible and active in a plan during the enrollment year.</span></span>

## <a name="generate-1095-b-and-1095-c-forms"></a><span data-ttu-id="c45e3-193">生成 1095-B 和 1095-C 表单</span><span class="sxs-lookup"><span data-stu-id="c45e3-193">Generate 1095-B and 1095-C forms</span></span>

<span data-ttu-id="c45e3-194">您可以生成 ACA 1095-B 和 1095-C 表单，然后将其分配给每个员工。</span><span class="sxs-lookup"><span data-stu-id="c45e3-194">You can generate ACA 1095-B and 1095-C forms, and then distribute them to each of your employees.</span></span> <span data-ttu-id="c45e3-195">您还可以电子方式生成表单 1095-C 和相应的 1094-C 传送单，来发送给美国国税局 (IRS)。</span><span class="sxs-lookup"><span data-stu-id="c45e3-195">You can also electronically generate Form 1095-C and the corresponding 1094-C transmittal files to send to the Internal Revenue Service (IRS).</span></span>

1. <span data-ttu-id="c45e3-196">在 **福利管理** 工作区，选择 **ACA 1095-B 表单** 或 **ACA 1095-C 表单**。</span><span class="sxs-lookup"><span data-stu-id="c45e3-196">In the **Benefits management** workspace, select **ACA 1095-B form** or **ACA 1095-C form**.</span></span>
2. <span data-ttu-id="c45e3-197">根据需要更改参数，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="c45e3-197">Change the parameters as required, and then select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c45e3-198">如果您为 500 名以上员工打印 1095-C 表单，您将收到多个 PDF 文件。</span><span class="sxs-lookup"><span data-stu-id="c45e3-198">If you're printing 1095-C forms for more than 500 employees, you will receive more than one PDF file.</span></span> <span data-ttu-id="c45e3-199">我们建议您将 **文档管理参数** 页上的 **最大文件大小(MB)** 字段的值增加到 **150**。</span><span class="sxs-lookup"><span data-stu-id="c45e3-199">We recommend that you increase the value of the **Maximum file size in megabytes** field on the **Document management parameters** page to **150**.</span></span> <span data-ttu-id="c45e3-200">（要快速打开该页面，可以使用导航栏上的搜索字段。）</span><span class="sxs-lookup"><span data-stu-id="c45e3-200">(To quickly open that page, you can use the search field on the navigation bar.)</span></span>
    >
    > ![更改最大文件大小](./media/hr-benefits-management-aca-maximum-file-size.png)

3. <span data-ttu-id="c45e3-202">要检查报告的状态以及查看报告，使用导航栏上的搜索字段打开 **电子报告作业** 页。</span><span class="sxs-lookup"><span data-stu-id="c45e3-202">To check the status of your reports and view them, use the search field on the navigation bar to open the **Electronic reporting jobs** page.</span></span>

    ![搜索电子报告作业页面](./media/hr-benefits-management-aca-search-electronic-reporting-jobs.png)

4. <span data-ttu-id="c45e3-204">选择要查看的报告，然后选择 **显示文件**。</span><span class="sxs-lookup"><span data-stu-id="c45e3-204">Select the report to view, and then select **Show files**.</span></span>

    ![显示文件](./media/hr-benefits-management-aca-show-files.png)

5. <span data-ttu-id="c45e3-206">选择 **打开**。</span><span class="sxs-lookup"><span data-stu-id="c45e3-206">Select **Open**.</span></span>

    ![打开文件](./media/hr-benefits-management-aca-open-file.png)

6. <span data-ttu-id="c45e3-208">从显示在浏览器窗口底部的通知栏中，打开 zip 文件，然后选择报告。</span><span class="sxs-lookup"><span data-stu-id="c45e3-208">From the Notification bar that appears at the bottom of the browser window, open the zip file, and then select the report.</span></span> <span data-ttu-id="c45e3-209">您可以查看或打印 PDF 文件。</span><span class="sxs-lookup"><span data-stu-id="c45e3-209">You can view or print the PDF file.</span></span>

    ![示例 1095-C 表单](./media/hr-benefits-management-aca-1095-c-form.png)

## <a name="view-aca-coverage-information"></a><span data-ttu-id="c45e3-211">查看 ACA 保险范围信息</span><span class="sxs-lookup"><span data-stu-id="c45e3-211">View ACA coverage information</span></span>

<span data-ttu-id="c45e3-212">**工作人员平价医疗保险范围** 页显示以下信息：</span><span class="sxs-lookup"><span data-stu-id="c45e3-212">The **Worker Affordable Care coverage** page shows the following information:</span></span>

- <span data-ttu-id="c45e3-213">分配到每个保险范围组的员工</span><span class="sxs-lookup"><span data-stu-id="c45e3-213">Employees who are assigned to each coverage group</span></span>
- <span data-ttu-id="c45e3-214">不必包含在报告中的员工</span><span class="sxs-lookup"><span data-stu-id="c45e3-214">Employees who don't have to be included on a report</span></span>
- <span data-ttu-id="c45e3-215">未分配的员工</span><span class="sxs-lookup"><span data-stu-id="c45e3-215">Unassigned employees</span></span>

<span data-ttu-id="c45e3-216">若要查看此信息，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="c45e3-216">To view this information, follow these steps.</span></span>

1. <span data-ttu-id="c45e3-217">在 **福利管理** 工作区，选择 **工作人员平价医疗保险范围**。</span><span class="sxs-lookup"><span data-stu-id="c45e3-217">In the **Benefits management** workspace, select **Worker Affordable Care coverage**.</span></span>
2. <span data-ttu-id="c45e3-218">在 **组名称** 字段中，选择一个组。</span><span class="sxs-lookup"><span data-stu-id="c45e3-218">In the **Group name** field, select a group.</span></span>

    ![查看 ACA 保险范围](./media/hr-benefits-management-aca-view-coverage.png)

<span data-ttu-id="c45e3-220">如果平价医疗保险范围组的任何默认值已被替代，被更改的值的旁边将显示星号。</span><span class="sxs-lookup"><span data-stu-id="c45e3-220">If any default values from the Affordable Care coverage group have been overridden, an asterisk appears next to the value that was changed.</span></span> <span data-ttu-id="c45e3-221">如果所有 12 个月的值相同且未被替代，该值将出现在 **所有 12 个月** 列中。</span><span class="sxs-lookup"><span data-stu-id="c45e3-221">If the values for all 12 months are the same and haven't been overridden, the value appears in the **All 12 months** column.</span></span>

<span data-ttu-id="c45e3-222">您可以查看标记为非 ACA 可报告、不需要表单 1095-C 的员工。</span><span class="sxs-lookup"><span data-stu-id="c45e3-222">You can view employees who are marked as not ACA-reportable, and who won't require a Form 1095-C.</span></span> <span data-ttu-id="c45e3-223">在 **筛选方式** 字段中，选择 **非 ACA 可报告**。</span><span class="sxs-lookup"><span data-stu-id="c45e3-223">In the **Filter by** field, select **Not ACA reportable**.</span></span>

<span data-ttu-id="c45e3-224">您可以查看未分配到组的员工，或分配到过期组的员工。</span><span class="sxs-lookup"><span data-stu-id="c45e3-224">You can view employees who aren't assigned to a group, or who are assigned to an expired group.</span></span> <span data-ttu-id="c45e3-225">在 **筛选方式** 字段中，选择 **未分配或过期组**。</span><span class="sxs-lookup"><span data-stu-id="c45e3-225">In the **Filter by** field, select **Unassigned or expired group**.</span></span>

### <a name="export-to-excel"></a><span data-ttu-id="c45e3-226">导出到 Excel</span><span class="sxs-lookup"><span data-stu-id="c45e3-226">Export to Excel</span></span>

<span data-ttu-id="c45e3-227">要将任何列表导出到 Microsoft Excel，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="c45e3-227">To export any of the lists to Microsoft Excel, follow these steps.</span></span>

1. <span data-ttu-id="c45e3-228">选择 **在 Microsoft Office 中打开** 按钮。</span><span class="sxs-lookup"><span data-stu-id="c45e3-228">Select the **Open in Microsoft Office** button.</span></span>
2. <span data-ttu-id="c45e3-229">选择 **供内部使用的 HCM Human Resources 临时表**。</span><span class="sxs-lookup"><span data-stu-id="c45e3-229">Select **HCM Human Resources temporary table for internal use**.</span></span>
3. <span data-ttu-id="c45e3-230">选择 **下载**。</span><span class="sxs-lookup"><span data-stu-id="c45e3-230">Select **Download**.</span></span>

### <a name="view-aca-reportable-dependents"></a><span data-ttu-id="c45e3-231">查看 ACA 可报告依赖方</span><span class="sxs-lookup"><span data-stu-id="c45e3-231">View ACA-reportable dependents</span></span>

<span data-ttu-id="c45e3-232">如果由于您提供自保型保险范围而必须报告投保的个人，可以查看标记为 **ACA 可报告** 的福利计划覆盖的依赖方。</span><span class="sxs-lookup"><span data-stu-id="c45e3-232">If you must report covered individuals because you provide self-insured coverage, you can view dependents who are covered under benefit plans that are marked as **ACA reportable**.</span></span> <span data-ttu-id="c45e3-233">在操作窗格上，选择 **查看依赖方保险范围**。</span><span class="sxs-lookup"><span data-stu-id="c45e3-233">On the Action Pane, select **View Dependent coverage**.</span></span>

![查看依赖方保险范围](./media/hr-benefits-management-aca-view-dependent-coverage.png)

<span data-ttu-id="c45e3-235">员工依赖方的保险范围信息将显示。</span><span class="sxs-lookup"><span data-stu-id="c45e3-235">Coverage information for the employee's dependents is shown.</span></span>

![被抚养人保险范围](./media/hr-benefits-management-aca-dependents.png)

> [!NOTE]
> <span data-ttu-id="c45e3-237">此页面仅显示标记为 **ACA 可报告** 的福利计划。</span><span class="sxs-lookup"><span data-stu-id="c45e3-237">The page shows only benefits plans that are marked as **ACA reportable**.</span></span>
