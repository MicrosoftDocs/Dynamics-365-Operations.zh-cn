---
title: Dynamics 365 Talent（2019 年 3 月 26 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 03/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-03-26
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d4b59183116784f44f45fddacdfa4aa954383ecd
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2019
ms.locfileid: "2023876"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-march-26-2019"></a><span data-ttu-id="970cd-103">Dynamics 365 Talent（2019 年 3 月 26 日）中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="970cd-103">What's new or changed in Dynamics 365 Talent (March 26, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="970cd-104">此主题介绍了 Dynamics 365 Talent 中的新增功能和更改的功能。</span><span class="sxs-lookup"><span data-stu-id="970cd-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="970cd-105">Attract 中的更改</span><span class="sxs-lookup"><span data-stu-id="970cd-105">Changes in Attract</span></span>

### <a name="enhancements-to-interview-scheduling"></a><span data-ttu-id="970cd-106">面试计划增强</span><span class="sxs-lookup"><span data-stu-id="970cd-106">Enhancements to interview scheduling</span></span>
<span data-ttu-id="970cd-107">面试计划进行了以下增强。</span><span class="sxs-lookup"><span data-stu-id="970cd-107">The following enhancements are available in interview scheduling.</span></span>

- <span data-ttu-id="970cd-108">招聘人员或招聘经理现在可手动为面试官触发提交反馈提醒。</span><span class="sxs-lookup"><span data-stu-id="970cd-108">Recruiters or hiring managers can now manually trigger a reminder for an interviewer to submit their feedback.</span></span> <span data-ttu-id="970cd-109">还可以为提醒配置关联的电子邮件模板。</span><span class="sxs-lookup"><span data-stu-id="970cd-109">The associated email template for the reminder is configurable as well.</span></span>
- <span data-ttu-id="970cd-110">与应聘者共享面试摘要时，面试安排人员可选择隐藏面试官的姓名，还可以选择在面试摘要视图中隐藏行。</span><span class="sxs-lookup"><span data-stu-id="970cd-110">While sharing the interview summary with the candidate, the interview scheduler can choose to hide the names of the interviewers and also choose to hide rows from the interview summary view.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="970cd-111">Onboard 中的更改</span><span class="sxs-lookup"><span data-stu-id="970cd-111">Changes in Onboard</span></span>

### <a name="embedded-images-in-activities"></a><span data-ttu-id="970cd-112">活动中的嵌入图像</span><span class="sxs-lookup"><span data-stu-id="970cd-112">Embedded images in activities</span></span>
<span data-ttu-id="970cd-113">现在可直接在活动中嵌入图像。</span><span class="sxs-lookup"><span data-stu-id="970cd-113">You can now embed images directly into activities.</span></span> <span data-ttu-id="970cd-114">除了可以复制和粘贴来自 Web 的图像，还可以从本地文件系统上传图像。</span><span class="sxs-lookup"><span data-stu-id="970cd-114">In addition to being able to copy and paste images from the web, you can upload images from your local file system.</span></span> <span data-ttu-id="970cd-115">图像的大小限制为 1 MB。</span><span class="sxs-lookup"><span data-stu-id="970cd-115">The size of the activity is limited to 1 MB.</span></span> <span data-ttu-id="970cd-116">如果图像过大，请调整其大小，然后再次尝试上传。</span><span class="sxs-lookup"><span data-stu-id="970cd-116">If the image is too large, resize and try to upload again.</span></span>

<span data-ttu-id="970cd-117">[![地理信息](./media/embedimages.png)](./media/embedimages.png)</span><span class="sxs-lookup"><span data-stu-id="970cd-117">[![Mapping](./media/embedimages.png)](./media/embedimages.png)</span></span>

<span data-ttu-id="970cd-118">本版本中包含 Dynamics 365 Talent: Onboard 的小缺陷修复。</span><span class="sxs-lookup"><span data-stu-id="970cd-118">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="970cd-119">Core HR 中的更改</span><span class="sxs-lookup"><span data-stu-id="970cd-119">Changes in Core HR</span></span>
<span data-ttu-id="970cd-120">**内部版本 8.1.2210**</span><span class="sxs-lookup"><span data-stu-id="970cd-120">**Build 8.1.2210**</span></span>

### <a name="custom-field-support-available-for-select-entities-in-common-data-service"></a><span data-ttu-id="970cd-121">在 Common Data Service 中选择实体时支持自定义字段</span><span class="sxs-lookup"><span data-stu-id="970cd-121">Custom field support available for select entities in Common Data Service</span></span> 

<span data-ttu-id="970cd-122">以下 Common Data Service 实体现在支持在 Talent 中创建的客户字段：</span><span class="sxs-lookup"><span data-stu-id="970cd-122">The following Common Data Service entities now support customer fields created in Talent:</span></span>

- <span data-ttu-id="970cd-123">工作线程</span><span class="sxs-lookup"><span data-stu-id="970cd-123">Worker</span></span>
- <span data-ttu-id="970cd-124">所属种族</span><span class="sxs-lookup"><span data-stu-id="970cd-124">Ethnic origin</span></span>
- <span data-ttu-id="970cd-125">退伍军人状态</span><span class="sxs-lookup"><span data-stu-id="970cd-125">Veteran status</span></span>
- <span data-ttu-id="970cd-126">语言代码</span><span class="sxs-lookup"><span data-stu-id="970cd-126">Language code</span></span>
- <span data-ttu-id="970cd-127">职位</span><span class="sxs-lookup"><span data-stu-id="970cd-127">Job</span></span>
- <span data-ttu-id="970cd-128">作业类型</span><span class="sxs-lookup"><span data-stu-id="970cd-128">Job type</span></span>
- <span data-ttu-id="970cd-129">工作职能</span><span class="sxs-lookup"><span data-stu-id="970cd-129">Job function</span></span>
- <span data-ttu-id="970cd-130">位置</span><span class="sxs-lookup"><span data-stu-id="970cd-130">Position</span></span>
- <span data-ttu-id="970cd-131">职位类型</span><span class="sxs-lookup"><span data-stu-id="970cd-131">Position type</span></span>
 
### <a name="employment-history-not-displayed-chronologically"></a><span data-ttu-id="970cd-132">工作经历不能按时间顺序显示</span><span class="sxs-lookup"><span data-stu-id="970cd-132">Employment history not displayed chronologically</span></span>
<span data-ttu-id="970cd-133">经过此项更改，工作经历页面现在独立于公司按时间顺序显示工作记录。</span><span class="sxs-lookup"><span data-stu-id="970cd-133">With this change, the employment history page now displays employment records chronologically, independent of company.</span></span> <span data-ttu-id="970cd-134">也可以使用排序选项按公司排序。</span><span class="sxs-lookup"><span data-stu-id="970cd-134">You can also use sorting options to sort by company.</span></span>

### <a name="fixed-compensation-plans-dont-appear-when-restricting-user-by-company-in-security"></a><span data-ttu-id="970cd-135">在安全中按公司限制用户时不显示固定薪酬计划。</span><span class="sxs-lookup"><span data-stu-id="970cd-135">Fixed compensation plans don't appear when restricting user by company in security.</span></span>
<span data-ttu-id="970cd-136">在此版本中，在安全中按公司限制用户时现在显示固定薪酬计划。</span><span class="sxs-lookup"><span data-stu-id="970cd-136">In this release, fixed compensation plans now appear when restricting users by company in security.</span></span> <span data-ttu-id="970cd-137">将遵守所有安全设置，并且将显示用户有权访问的公司的固定薪酬计划。</span><span class="sxs-lookup"><span data-stu-id="970cd-137">All security settings will be honored, and fixed plans will appear for those companies the user has permissions to access.</span></span> 

### <a name="cant-delete-job-records-using-open-in-excel-option-in-talent"></a><span data-ttu-id="970cd-138">在 Talent 中不能使用“在 Excel 中打开”选项删除工作记录</span><span class="sxs-lookup"><span data-stu-id="970cd-138">Can't delete Job records using Open in Excel option in Talent</span></span>
<span data-ttu-id="970cd-139">在此版本中，现在可在 Talent 中通过使用**在 Excel 中打开**选项删除工作记录。</span><span class="sxs-lookup"><span data-stu-id="970cd-139">With this release, you can now remove job records by using the **Open in Excel** option in Talent.</span></span>

### <a name="upgrade-to-common-data-service"></a><span data-ttu-id="970cd-140">升级到 Common Data Service</span><span class="sxs-lookup"><span data-stu-id="970cd-140">Upgrade to Common Data Service</span></span>
<span data-ttu-id="970cd-141">很快将到达 Common Data Service 的升级截止时间。</span><span class="sxs-lookup"><span data-stu-id="970cd-141">Deadlines to upgrade to Common Data Service are quickly approaching.</span></span> <span data-ttu-id="970cd-142">请登录 PowerApps 管理员中心以确定是否需要升级您的数据库。</span><span class="sxs-lookup"><span data-stu-id="970cd-142">Sign in to the PowerApps Admin center to determine if your database needs to be upgraded.</span></span> <span data-ttu-id="970cd-143">有关截止时间和必要升级步骤的详细信息，请参阅[升级到 Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds)。</span><span class="sxs-lookup"><span data-stu-id="970cd-143">For more information about deadlines and necessary steps to upgrade, see [Upgrade to Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).</span></span>

## <a name="in-preview"></a><span data-ttu-id="970cd-144">预览模式</span><span class="sxs-lookup"><span data-stu-id="970cd-144">In preview</span></span>

<span data-ttu-id="970cd-145">有关启用预览功能的信息，请参阅[访问 Talent 中的预览功能](./access-preview-feature.md)。</span><span class="sxs-lookup"><span data-stu-id="970cd-145">For information about enabling preview features, see [Access preview features in Talent](./access-preview-feature.md).</span></span>

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a><span data-ttu-id="970cd-146">允许为休假类型指定原因代码</span><span class="sxs-lookup"><span data-stu-id="970cd-146">Allow reason codes to be specified on leave types</span></span>
<span data-ttu-id="970cd-147">组织可能需要与休假请求有关的更多信息。</span><span class="sxs-lookup"><span data-stu-id="970cd-147">Organizations might need additional information related to time off requests.</span></span> <span data-ttu-id="970cd-148">若要获取此信息，需要员工在休假请求中加入原因代码。</span><span class="sxs-lookup"><span data-stu-id="970cd-148">To get this information, employees need to include a reason code on their time off requests.</span></span> <span data-ttu-id="970cd-149">在此版本中，现在可指定与给定休假类型关联的原因代码，并让员工在休假请求中选择原因代码。</span><span class="sxs-lookup"><span data-stu-id="970cd-149">With this release, you can now specify the reason codes associated with a given leave type and enable employees to select a reason code on their time off requests.</span></span>

### <a name="configure-reason-codes-to-be-required-when-submitting-time-off-for-certain-leave-types"></a><span data-ttu-id="970cd-150">配置提交特定休假类型的请假时需要的原因代码。</span><span class="sxs-lookup"><span data-stu-id="970cd-150">Configure reason codes to be required when submitting time off for certain leave types</span></span>
<span data-ttu-id="970cd-151">组织可能会要求当员工提交请假时为特定休假类型设置原因代码。</span><span class="sxs-lookup"><span data-stu-id="970cd-151">Organizations might require reason codes to be set on specific leave types when employees submit time off.</span></span> <span data-ttu-id="970cd-152">这可能是基于国家/地区的法规或公司政策的要求。</span><span class="sxs-lookup"><span data-stu-id="970cd-152">This may be required based on a regulatory requirement in their country/region or a company policy.</span></span> <span data-ttu-id="970cd-153">在此版本中，HR 可以指定哪些休假类型需要原因代码。</span><span class="sxs-lookup"><span data-stu-id="970cd-153">This release provides the ability for HR to specify which leave types require a reason code.</span></span> <span data-ttu-id="970cd-154">当员工提交的休假请求需要原因代码时，将实施此规则。</span><span class="sxs-lookup"><span data-stu-id="970cd-154">This will be enforced when employees submit time off requests where the leave requires a reason code.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="970cd-155">即将到期</span><span class="sxs-lookup"><span data-stu-id="970cd-155">Coming soon</span></span>

###  <a name="advanced-compensation-security-fixed-and-variable"></a><span data-ttu-id="970cd-156">高级薪酬安全（固定和可变）</span><span class="sxs-lookup"><span data-stu-id="970cd-156">Advanced compensation security (fixed and variable)</span></span>
<span data-ttu-id="970cd-157">在许多组织中，薪酬和福利经理可能只能访问特定薪酬记录。</span><span class="sxs-lookup"><span data-stu-id="970cd-157">In many organizations, compensation and benefits managers might only have access to certain compensation records.</span></span> <span data-ttu-id="970cd-158">这些记录可能是有关管理层或地区员工的记录。</span><span class="sxs-lookup"><span data-stu-id="970cd-158">These could be for executives or regional employees.</span></span> <span data-ttu-id="970cd-159">通过此更改，HR 可以管理和维护组织中不同员工组的薪酬计划。</span><span class="sxs-lookup"><span data-stu-id="970cd-159">With this change, HR can manage and maintain the compensation plans for different employee groups in the organization.</span></span> <span data-ttu-id="970cd-160">您可以为固定计划和可变计划分配安全角色，用于决定这些计划和与其有关的员工数据（例如，工资和奖金记录）的访问权限。</span><span class="sxs-lookup"><span data-stu-id="970cd-160">You can assign security roles to fixed and variable plans that determine access to the plans and the employee data related to the plans, such as salary or bonus records.</span></span> <span data-ttu-id="970cd-161">只有授予了访问权限的角色才能处理这些员工的薪酬。</span><span class="sxs-lookup"><span data-stu-id="970cd-161">Only the roles granted with access can process compensation for these employees.</span></span>

###  <a name="email-support-for-alerts"></a><span data-ttu-id="970cd-162">警报的电子邮件支持</span><span class="sxs-lookup"><span data-stu-id="970cd-162">Email support for alerts</span></span>
<span data-ttu-id="970cd-163">安装 Finance and Operations 的平台更新 25 之后，用户可创建警报规则，用于在被事件触发后自动为联系人派遣电子邮件通知。</span><span class="sxs-lookup"><span data-stu-id="970cd-163">With Platform update 25 for Finance and Operations, users can create alert rules that automatically dispatch email notifications to contacts when triggered by an event.</span></span> 

### <a name="duplicate-employee-checks-user-interface-changes"></a><span data-ttu-id="970cd-164">重复员工检查：用户界面更改</span><span class="sxs-lookup"><span data-stu-id="970cd-164">Duplicate employee checks: User interface changes</span></span>
<span data-ttu-id="970cd-165">借助此更改，输入名称字段时可检测重复项，而状态将显示找到的重复项数量。</span><span class="sxs-lookup"><span data-stu-id="970cd-165">With this change, duplicates are detected as you enter name fields, and a status displays the number of duplicates found.</span></span> <span data-ttu-id="970cd-166">您可以选择提供的链接以打开一个新的页面来评估是否要使用检测到的匹配项。</span><span class="sxs-lookup"><span data-stu-id="970cd-166">You can select the provided link to open a new page to evaluate whether to use the detected match.</span></span> <span data-ttu-id="970cd-167">为了避免中断数据输入，不会自动打开重复项窗体。</span><span class="sxs-lookup"><span data-stu-id="970cd-167">To avoid interrupting data entry, the duplicates form doesn't open automatically.</span></span>
