---
title: 配置 Human Resources 参数
description: 本主题说明如何在 Dynamics 365 Human Resources 中设置特定于公司的参数。
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7c4c93e3d2644a380e3d5d2247961a8b6fb34568
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052401"
---
# <a name="configure-human-resources-parameters"></a><span data-ttu-id="0b4ee-103">配置 Human Resources 参数</span><span class="sxs-lookup"><span data-stu-id="0b4ee-103">Configure Human resources parameters</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="0b4ee-104">某些人力资源参数的设置在公司间共享，而其他参数设置是特定于公司的。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-104">The settings of some Human resources parameters are shared across companies, while the settings of other parameters are company-specific.</span></span> <span data-ttu-id="0b4ee-105">本主题说明如何设置特定于公司的人力资源参数。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-105">This topic explains how to set up company-specific Human resources parameters.</span></span>

<span data-ttu-id="0b4ee-106">提供了两个页面来设置人力资源参数。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-106">Two pages are used to set Human resources parameters.</span></span> <span data-ttu-id="0b4ee-107">对于跨公司共享的参数，您可使用 **人力资源共享参数** 页。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-107">For parameters that are shared across companies, you use the **Human resources shared parameters** page.</span></span> <span data-ttu-id="0b4ee-108">对于特定于公司的参数（换句话说，这些设置将应用于单个公司），您可使用 **人力资源参数** 页。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-108">For parameters that are company-specific (in other words, the settings apply to a single company), you use the **Human resource parameters** page.</span></span>

![转到“人力资源参数”](./media/hr-employee-self-service-human-resources-parameters.png)

<span data-ttu-id="0b4ee-110">在 **人力资源参数** 页上，设置在 6 个选项卡之间分配：</span><span class="sxs-lookup"><span data-stu-id="0b4ee-110">On the **Human resources parameters** page, the settings are divided among six tabs:</span></span>

- <span data-ttu-id="0b4ee-111">**常规**</span><span class="sxs-lookup"><span data-stu-id="0b4ee-111">**General**</span></span>
- <span data-ttu-id="0b4ee-112">**招聘**（此选项卡不包括在 Dynamics 365 Human Resources 中）</span><span class="sxs-lookup"><span data-stu-id="0b4ee-112">**Recruitment** (this tab isn't included in Dynamics 365 Human Resources)</span></span>
- <span data-ttu-id="0b4ee-113">**薪酬**</span><span class="sxs-lookup"><span data-stu-id="0b4ee-113">**Compensation**</span></span>
- <span data-ttu-id="0b4ee-114">**编号规则**</span><span class="sxs-lookup"><span data-stu-id="0b4ee-114">**Number sequences**</span></span>
- <span data-ttu-id="0b4ee-115">**FMLA**</span><span class="sxs-lookup"><span data-stu-id="0b4ee-115">**FMLA**</span></span>
- <span data-ttu-id="0b4ee-116">**员工自助服务**</span><span class="sxs-lookup"><span data-stu-id="0b4ee-116">**Employee self service**</span></span>
- <span data-ttu-id="0b4ee-117">**经理自助服务**</span><span class="sxs-lookup"><span data-stu-id="0b4ee-117">**Manager self service**</span></span>
- <span data-ttu-id="0b4ee-118">**福利管理**</span><span class="sxs-lookup"><span data-stu-id="0b4ee-118">**Benefits management**</span></span>
- <span data-ttu-id="0b4ee-119">**休假和缺勤**</span><span class="sxs-lookup"><span data-stu-id="0b4ee-119">**Leave and absence**</span></span>
- <span data-ttu-id="0b4ee-120">**付款方式**</span><span class="sxs-lookup"><span data-stu-id="0b4ee-120">**Payment methods**</span></span>

<span data-ttu-id="0b4ee-121">每个选项卡均包含与单个公司有关的信息。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-121">Each tab contains information that pertains to a single company.</span></span>

## <a name="general"></a><span data-ttu-id="0b4ee-122">常规</span><span class="sxs-lookup"><span data-stu-id="0b4ee-122">General</span></span>

<span data-ttu-id="0b4ee-123">**常规** 选项卡上的设置定义有关缺勤、伤害和疾病以及新的雇用的信息的外观。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-123">The settings on the **General** tab define the appearance of information about absence, injury and illness, and new hires.</span></span> <span data-ttu-id="0b4ee-124">此选项卡上的设置还定义在您工作时显示的某些默认条目。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-124">The settings on this tab also define some default entries that appear as you work.</span></span> <span data-ttu-id="0b4ee-125">具体来说，此选项卡可让您：</span><span class="sxs-lookup"><span data-stu-id="0b4ee-125">Specifically, this tab lets you:</span></span>

- <span data-ttu-id="0b4ee-126">选择要应用于未结的缺勤事务的颜色</span><span class="sxs-lookup"><span data-stu-id="0b4ee-126">Select a color to apply to open absence transactions</span></span>
- <span data-ttu-id="0b4ee-127">指定用于报表的样式表</span><span class="sxs-lookup"><span data-stu-id="0b4ee-127">Specify the style sheet to use for reports</span></span>
- <span data-ttu-id="0b4ee-128">启用培训课程和缺勤登记之间的集成</span><span class="sxs-lookup"><span data-stu-id="0b4ee-128">Enable the integration between training courses and absence registration</span></span>
- <span data-ttu-id="0b4ee-129">选择用于控制此集成的缺勤代码。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-129">Select the absence code that is used to control this integration.</span></span>
- <span data-ttu-id="0b4ee-130">指出保留伤害和疾病案例事件的时间。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-130">Indicate how long to keep injury and illness case incidents.</span></span>
- <span data-ttu-id="0b4ee-131">指定雇用新工作人员时显示的默认标识号。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-131">Specify the default identification number shown when a new worker is hired.</span></span>

![常规选项卡](./media/hr-setup-parameters-general.png)

## <a name="recruitment"></a><span data-ttu-id="0b4ee-133">招聘</span><span class="sxs-lookup"><span data-stu-id="0b4ee-133">Recruitment</span></span>

<span data-ttu-id="0b4ee-134">**招聘** 选项卡上的设置定义用于自动发送给申请人的通信的文档类型。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-134">The settings on the **Recruitment** tab define the document types used for correspondence automatically sent to applicants.</span></span> <span data-ttu-id="0b4ee-135">您还可以指出用于主动提供的申请的招聘项目。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-135">You can also indicate the recruitment project used for unsolicited applications.</span></span>

<span data-ttu-id="0b4ee-136">为招聘项目帐龄定义的期间确定包含在 **招聘管理** 工作区中的 **帐龄项目** 磁贴上的招聘项目。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-136">The period defined for recruitment project aging determines the recruitment projects included on the **Aging projects** tile in the **Recruitment management** workspace.</span></span> <span data-ttu-id="0b4ee-137">为申请截止日期警告定义的期间用于显示接近其在 **招聘** 工作区中的 **接近申请截止日期** 磁贴上的申请截止日期的招聘项目。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-137">The period defined for the application deadline warning is used to display recruitment projects that are approaching their application deadline on the **Application deadline approaching** tile in the **Recruitment** workspace.</span></span>

<span data-ttu-id="0b4ee-138">有关招聘的详细信息，请参阅[招聘工作应聘者](hr-personnel-recruit.md)。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-138">For more information about recruiting, see [Recruit job candidates](hr-personnel-recruit.md).</span></span>

## <a name="compensation"></a><span data-ttu-id="0b4ee-139">薪酬</span><span class="sxs-lookup"><span data-stu-id="0b4ee-139">Compensation</span></span>

<span data-ttu-id="0b4ee-140">在 Dynamics 365 Finance 中，**薪酬** 选项卡上的设置定义用户是否必须确认是希望保存固定薪酬计划的信息还是可变薪酬计划的信息。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-140">In Dynamics 365 Finance, the settings on the **Compensation** tab define whether users must confirm that they want to save information for a fixed or variable compensation plan.</span></span> <span data-ttu-id="0b4ee-141">如果您选择 **启用保存验证**，当用户关闭与薪酬相关的页面时，他们将收到一条消息，询问是否需要保存记录。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-141">If you select **Enable save validation**, when users close a compensation-related page, they receive a message that asks whether they want to save the record.</span></span> <span data-ttu-id="0b4ee-142">薪酬管理中的某些页面不允许用户删除信息。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-142">Some pages in Compensation management don't let users delete information.</span></span> <span data-ttu-id="0b4ee-143">通过提示用户验证是否要保存信息，您也许能够限制可保存但稍后无法删除的信息量。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-143">By prompting users to verify that they want to save information, you might be able to limit the amount of information that is saved but can't be deleted later.</span></span> <span data-ttu-id="0b4ee-144">如果清除 **启用保存验证**，将立即保存记录（可能在用户准备就绪之前）。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-144">If you clear **Enable save validation**, records save immediately, possibly before the user is ready.</span></span> <span data-ttu-id="0b4ee-145">如果您使用绩效管理，则也可使用 **薪酬** 选项卡来选择要使用的评级模型，而不是选择在对绩效进行评级时分配给薪酬计划的模型。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-145">If you're using Performance management, the **Compensation** tab also lets you select a rating model to use instead of the model assigned to compensation plans when rating performance.</span></span>

<span data-ttu-id="0b4ee-146">在 Human Resources 中，您可以使用 **薪酬** 选项卡选择限制对薪酬计划的访问和设置默认货币。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-146">In Human Resources, you can use the **Compensation** tab to choose to restrict access to compensation plans and to set a default currency.</span></span>

<span data-ttu-id="0b4ee-147">有关薪酬的详细信息，请参阅[薪酬计划概述](hr-compensation-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-147">For more information about compensation, see [Compensation plans overview](hr-compensation-overview.md).</span></span>

![“薪酬”选项卡](./media/hr-setup-parameters-compensation.png)

## <a name="number-sequences"></a><span data-ttu-id="0b4ee-149">编号规则</span><span class="sxs-lookup"><span data-stu-id="0b4ee-149">Number sequences</span></span>

<span data-ttu-id="0b4ee-150">**编号规则** 选项卡上的设置确定用于为 Human Resources 中的项目自动分配 ID 的序列，如：</span><span class="sxs-lookup"><span data-stu-id="0b4ee-150">The settings on the **Number sequence** tab determine the sequences used to automatically assign IDs to items in Human Resources, such as:</span></span>

- <span data-ttu-id="0b4ee-151">申请表</span><span class="sxs-lookup"><span data-stu-id="0b4ee-151">Applications</span></span>
- <span data-ttu-id="0b4ee-152">缺勤登记</span><span class="sxs-lookup"><span data-stu-id="0b4ee-152">Absence registrations</span></span>
- <span data-ttu-id="0b4ee-153">薪酬流程结果</span><span class="sxs-lookup"><span data-stu-id="0b4ee-153">Compensation process results</span></span>
- <span data-ttu-id="0b4ee-154">案例编号</span><span class="sxs-lookup"><span data-stu-id="0b4ee-154">Case numbers</span></span>
- <span data-ttu-id="0b4ee-155">课程</span><span class="sxs-lookup"><span data-stu-id="0b4ee-155">Courses</span></span>
- <span data-ttu-id="0b4ee-156">课程安排</span><span class="sxs-lookup"><span data-stu-id="0b4ee-156">Course agendas</span></span>

<span data-ttu-id="0b4ee-157">要维护编号规则引用和代码，可使用 **编号规则** 列表页（选择 **组织管理 > 编号规则 > 编号规则**）。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-157">To maintain number sequence references and codes, use the **Number sequences** list page (select **Organization administration > Number sequences > Number sequences**).</span></span>

<span data-ttu-id="0b4ee-158">有关详细信息，请参阅[编号规则概述](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-158">For more information, see [Number sequences overview](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

> [!NOTE]
> <span data-ttu-id="0b4ee-159">工作的小时数不能超过 1,250，雇用时长不能超过 12 个月。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-159">The number of hours that are worked can't exceed 1,250, and the length of employment can't exceed 12 months.</span></span> <span data-ttu-id="0b4ee-160">这些最大值符合美国的联邦法律。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-160">These maximum values are in accordance with federal law in the United States.</span></span>

![“编号规则”选项卡](./media/hr-setup-parameters-number-sequences.png)

## <a name="fmla"></a><span data-ttu-id="0b4ee-162">FMLA</span><span class="sxs-lookup"><span data-stu-id="0b4ee-162">FMLA</span></span>

<span data-ttu-id="0b4ee-163">在 FMLA 选项卡上，设置 FMLA 资格要求和 FMLA 权利时数。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-163">On the FMLA tab, you set FMLA eligibility requirements and FMLA entitlement hours.</span></span> <span data-ttu-id="0b4ee-164">有关详细信息，请参阅[配置休假和缺勤参数](hr-leave-and-absence-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-164">For more information, see [Configure leave and absence parameters](hr-leave-and-absence-parameters.md).</span></span>

![FMLA 选项卡](./media/hr-setup-parameters-fmla.png)

## <a name="employee-self-service"></a><span data-ttu-id="0b4ee-166">员工自助服务</span><span class="sxs-lookup"><span data-stu-id="0b4ee-166">Employee self service</span></span>

<span data-ttu-id="0b4ee-167">**员工自助服务** 选项卡上的设置会影响员工自助服务对员工的显示方式。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-167">The settings on the **Employee self service** tab affect how Employee self service appears to employees.</span></span> <span data-ttu-id="0b4ee-168">在此选项卡上，您可以：</span><span class="sxs-lookup"><span data-stu-id="0b4ee-168">On this tab, you can:</span></span>

- <span data-ttu-id="0b4ee-169">为员工自助服务工作区输入名称</span><span class="sxs-lookup"><span data-stu-id="0b4ee-169">Enter a name for the Employee self service workspace</span></span>
- <span data-ttu-id="0b4ee-170">选择经理可以为员工输入的信息</span><span class="sxs-lookup"><span data-stu-id="0b4ee-170">Select which information a manager can enter for employees</span></span>
- <span data-ttu-id="0b4ee-171">为员工添加有用的链接</span><span class="sxs-lookup"><span data-stu-id="0b4ee-171">Add useful links for employees</span></span>
- <span data-ttu-id="0b4ee-172">限制员工添加或编辑业务联系人详细信息。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-172">Restrict employees from adding or editing business contact details.</span></span> <span data-ttu-id="0b4ee-173">有关详细信息，请参阅[限制对个人信息的编辑](hr-employee-self-service-restrict-editing.md)。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-173">For more information, see [Restrict editing of personal information](hr-employee-self-service-restrict-editing.md).</span></span>

<span data-ttu-id="0b4ee-174">有关设置员工自助服务的详细信息，请参阅[员工和经理自助服务概述](hr-employee-manager-self-service-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-174">For more information about setting up Employee self service, see [Employee and Manager self service overview](hr-employee-manager-self-service-overview.md).</span></span>

![员工自助服务选项卡](./media/hr-setup-parameters-employee-self-service.png)

## <a name="manager-self-service"></a><span data-ttu-id="0b4ee-176">经理自助服务</span><span class="sxs-lookup"><span data-stu-id="0b4ee-176">Manager self service</span></span>

<span data-ttu-id="0b4ee-177">**经理自助服务** 选项卡上的设置会影响经理在经理自助服务中看到的内容。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-177">The settings on the **Manager self service** tab affect what managers see in Manager self service.</span></span> <span data-ttu-id="0b4ee-178">在此选项卡上，您可以配置以下选项：</span><span class="sxs-lookup"><span data-stu-id="0b4ee-178">On this tab, you can configure the following options:</span></span>

- <span data-ttu-id="0b4ee-179">即将过期的记录的范围</span><span class="sxs-lookup"><span data-stu-id="0b4ee-179">The range for expiring records</span></span>
- <span data-ttu-id="0b4ee-180">经理可以在即将过期的记录中查看的信息</span><span class="sxs-lookup"><span data-stu-id="0b4ee-180">Information managers can view in expiring records</span></span>
- <span data-ttu-id="0b4ee-181">经理是否可以查看间接下属空缺职位</span><span class="sxs-lookup"><span data-stu-id="0b4ee-181">Whether managers can view open positions for extended reports</span></span>
- <span data-ttu-id="0b4ee-182">正离职的工作人员视图</span><span class="sxs-lookup"><span data-stu-id="0b4ee-182">Views of exiting workers</span></span>
- <span data-ttu-id="0b4ee-183">对经理有用的链接</span><span class="sxs-lookup"><span data-stu-id="0b4ee-183">Useful links for managers</span></span>

<span data-ttu-id="0b4ee-184">有关设置经理自助服务的详细信息，请参阅[员工和经理自助服务概述](hr-employee-manager-self-service-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-184">For more information about setting up Manager self service, see [Employee and Manager self service overview](hr-employee-manager-self-service-overview.md).</span></span>

![经理自助服务选项卡](./media/hr-setup-parameters-manager-self-service.png)

## <a name="benefits-management"></a><span data-ttu-id="0b4ee-186">福利管理</span><span class="sxs-lookup"><span data-stu-id="0b4ee-186">Benefits management</span></span>

<span data-ttu-id="0b4ee-187">在“福利管理”选项卡上，您可以为“福利管理”配置电子邮件选项。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-187">On the Benefits management tab, you can configure email options for Benefits management.</span></span> <span data-ttu-id="0b4ee-188">有关设置和使用福利管理的信息，请参阅[福利管理概述](hr-benefits-management-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-188">For information about setting up and using Benefits management, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>

![福利管理选项卡](./media/hr-setup-parameters-benefits-management.png)

## <a name="leave-and-absence"></a><span data-ttu-id="0b4ee-190">休假和缺勤</span><span class="sxs-lookup"><span data-stu-id="0b4ee-190">Leave and absence</span></span>

<span data-ttu-id="0b4ee-191">有关设置和使用休假和缺勤的信息，请参阅[休假和缺勤概述](hr-leave-and-absence-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-191">For information about setting up and using Leave and absence, see [Leave and absence overview](hr-leave-and-absence-overview.md).</span></span>

## <a name="payment-methods"></a><span data-ttu-id="0b4ee-192">付款方式</span><span class="sxs-lookup"><span data-stu-id="0b4ee-192">Payment methods</span></span>

<span data-ttu-id="0b4ee-193">在 **付款方式** 选项卡上，您可以选择组织支持的付款方式。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-193">On the **Payment methods** tab, you can select the payment methods supported by your organization.</span></span> <span data-ttu-id="0b4ee-194">有关配置薪酬的详细信息，请参阅[薪酬计划概述](hr-compensation-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="0b4ee-194">For more information about configuring compensation, see [Compensation plans overview](hr-compensation-overview.md).</span></span>

![付款方式选项卡](./media/hr-setup-parameters-payment-methods.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]