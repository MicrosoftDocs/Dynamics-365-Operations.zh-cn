---
title: Dynamics 365 Talent（2019 年 4 月 23 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 04/23/2019
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
ms.search.validFrom: 2019-04-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 53faf972759c8f770017fcd3a87920410988e626
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527167"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-23-2019"></a><span data-ttu-id="65ad6-103">Dynamics 365 Talent（2019 年 4 月 23 日）中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="65ad6-103">What's new or changed in Dynamics 365 Talent (April 23, 2019)</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="65ad6-104">此主题介绍了 Dynamics 365 Talent 中的新增功能和更改的功能。</span><span class="sxs-lookup"><span data-stu-id="65ad6-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="65ad6-105">Attract 中的更改</span><span class="sxs-lookup"><span data-stu-id="65ad6-105">Changes in Attract</span></span>
<span data-ttu-id="65ad6-106">本版本中包含 Dynamics 365 Talent: Attract 的小缺陷修复。</span><span class="sxs-lookup"><span data-stu-id="65ad6-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="65ad6-107">Onboard 中的更改</span><span class="sxs-lookup"><span data-stu-id="65ad6-107">Changes in Onboard</span></span>
<span data-ttu-id="65ad6-108">本版本中包含 Dynamics 365 Talent: Onboard 的小缺陷修复。</span><span class="sxs-lookup"><span data-stu-id="65ad6-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="65ad6-109">Core HR 中的更改</span><span class="sxs-lookup"><span data-stu-id="65ad6-109">Changes in Core HR</span></span>
<span data-ttu-id="65ad6-110">本部分中的更改适用于内部版本号 8.1.2253。</span><span class="sxs-lookup"><span data-stu-id="65ad6-110">Changes described in this section apply to build number 8.1.2253.</span></span> <span data-ttu-id="65ad6-111">括号内的数字是 Lifecycle Services (LCS) 中的支持号码。</span><span class="sxs-lookup"><span data-stu-id="65ad6-111">Numbers in parentheses refer to support numbers in Lifecycle Services (LCS).</span></span>

### <a name="common-data-service-entity-support-for-custom-fields"></a><span data-ttu-id="65ad6-112">Common Data Service 实体对自定义字段的支持</span><span class="sxs-lookup"><span data-stu-id="65ad6-112">Common Data Service entity support for custom fields</span></span>
<span data-ttu-id="65ad6-113">安装本周的版本后，下列实体支持自定义字段：薪酬级别、福利选项、技能类型和薪酬区域。</span><span class="sxs-lookup"><span data-stu-id="65ad6-113">With this week's release, the following entities support custom fields: Compensation level, Benefit option, Skill type, and Compensation region.</span></span>

### <a name="additional-odata-entities-302992"></a><span data-ttu-id="65ad6-114">其他 OData 实体 (302992)</span><span class="sxs-lookup"><span data-stu-id="65ad6-114">Additional OData entities (302992)</span></span>
<span data-ttu-id="65ad6-115">OData 内现在支持下列实体：工作人员工作经验和工作人员教育。</span><span class="sxs-lookup"><span data-stu-id="65ad6-115">The following entities are now supported within OData: Worker professional experience and Worker education.</span></span>
   
### <a name="performance-journal-attachments-for-managers-and-employees-308248"></a><span data-ttu-id="65ad6-116">经理和员工的绩效日记帐附件 (308248)</span><span class="sxs-lookup"><span data-stu-id="65ad6-116">Performance journal attachments for managers and employees (308248)</span></span>
<span data-ttu-id="65ad6-117">在此版本中，创建和更新绩效日记帐条目时，可以为经理和员工添加附件。</span><span class="sxs-lookup"><span data-stu-id="65ad6-117">With this release, attachments are now available for both managers and employees when creating and updating performance journal entries.</span></span>

### <a name="employee-rehire-flag-always-available-310047"></a><span data-ttu-id="65ad6-118">员工重新聘用标签始终可用 (310047)</span><span class="sxs-lookup"><span data-stu-id="65ad6-118">Employee rehire flag always available (310047)</span></span>
<span data-ttu-id="65ad6-119">现在可在解除雇用流程外更新员工重新雇用选项。</span><span class="sxs-lookup"><span data-stu-id="65ad6-119">The employee rehire option is now available for updating outside of the termination process.</span></span> 

### <a name="cannot-change-the-name-of-my-payment-method-308815"></a><span data-ttu-id="65ad6-120">不能更改 **我的付款方式** 的名称 (308815)</span><span class="sxs-lookup"><span data-stu-id="65ad6-120">Cannot change the name of **My payment method** (308815)</span></span>
<span data-ttu-id="65ad6-121">已启用了个性化，允许在员工自助服务中更改 **我的付款方式** 标签。</span><span class="sxs-lookup"><span data-stu-id="65ad6-121">Personalization has been enabled to allow for the **My payment method** label to be changed in Employee self-service.</span></span>

### <a name="financial-dimensions-against-a-position-cant-be-deleted-293908"></a><span data-ttu-id="65ad6-122">不能删除针对职位的财务维度 (293908)</span><span class="sxs-lookup"><span data-stu-id="65ad6-122">Financial dimensions against a Position can't be deleted (293908)</span></span>
<span data-ttu-id="65ad6-123">请求更改现有跨公司范围的职位和财务维度时，现在可删除财务维度。</span><span class="sxs-lookup"><span data-stu-id="65ad6-123">Financial dimensions can now be removed when requesting a change for an existing position and the financial dimensions cross company boundaries.</span></span> 

### <a name="customer-is-unable-to-publish-back-data-into-talent-when-opening-the-data-from-excel-302955"></a><span data-ttu-id="65ad6-124">从 Excel 打开数据时，客户不能将数据发布回 Talent (302955)</span><span class="sxs-lookup"><span data-stu-id="65ad6-124">Customer is unable to publish back data into Talent when opening the data from Excel (302955)</span></span>
<span data-ttu-id="65ad6-125">此项更改解决了使用相关表时的发布问题。</span><span class="sxs-lookup"><span data-stu-id="65ad6-125">This change corrects a publishing issue when using related tables.</span></span>

## <a name="in-preview"></a><span data-ttu-id="65ad6-126">预览模式</span><span class="sxs-lookup"><span data-stu-id="65ad6-126">In preview</span></span>

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a><span data-ttu-id="65ad6-127">允许为休假类型指定原因代码</span><span class="sxs-lookup"><span data-stu-id="65ad6-127">Allow reason codes to be specified on leave types</span></span>
<span data-ttu-id="65ad6-128">组织可能需要有关休假请求的更多信息。</span><span class="sxs-lookup"><span data-stu-id="65ad6-128">Organizations might need additional information about time-off requests.</span></span> <span data-ttu-id="65ad6-129">现在可指定休假类型的原因代码，并让员工在休假请求中选择原因代码。</span><span class="sxs-lookup"><span data-stu-id="65ad6-129">You can now specify reason codes for leave types and enable employees to select a reason code on their time-off requests.</span></span>

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a><span data-ttu-id="65ad6-130">休假请求中的特定休假类型需要原因代码</span><span class="sxs-lookup"><span data-stu-id="65ad6-130">Require reason codes for certain leave types on time-off requests</span></span>
<span data-ttu-id="65ad6-131">组织可能会要求当员工提交请假时为特定休假类型设置原因代码。</span><span class="sxs-lookup"><span data-stu-id="65ad6-131">Organizations might require reason codes for specific leave types when employees submit time off.</span></span> <span data-ttu-id="65ad6-132">可能是因为公司政策或法规要求所致。</span><span class="sxs-lookup"><span data-stu-id="65ad6-132">This might be due to company policy or regulatory requirements.</span></span> <span data-ttu-id="65ad6-133">现在可以指定哪些休假类型需要原因代码，并且可以要求员工为自己的休假请求中的休假类型提供原因代码。</span><span class="sxs-lookup"><span data-stu-id="65ad6-133">You can now specify which leave types require a reason code, and you can require employees to provide a reason code for the leave type on their time-off requests.</span></span>

### <a name="provide-leave-and-absence-transaction-list-for-hr"></a><span data-ttu-id="65ad6-134">为 HR 提供休假和缺勤交易记录列表</span><span class="sxs-lookup"><span data-stu-id="65ad6-134">Provide leave and absence transaction list for HR</span></span>
<span data-ttu-id="65ad6-135">跟踪员工休假和了解休假的计算方法不仅可以帮助 HR 解答员工的问题，还可以确保员工的休假奖励精确无误。</span><span class="sxs-lookup"><span data-stu-id="65ad6-135">Tracking employee time off and understanding how time off is calculated not only helps HR answer employee questions, but also ensures accurate time-off awards for employees.</span></span> <span data-ttu-id="65ad6-136">HR 现在可以以新的视觉查看交易记录（授权、应计、调整和请求），以查看余额背后的原因。</span><span class="sxs-lookup"><span data-stu-id="65ad6-136">HR now has a new view into the transactions (grants, accruals, adjustments, and requests) to see the reasons behind balances.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="65ad6-137">即将到期</span><span class="sxs-lookup"><span data-stu-id="65ad6-137">Coming soon</span></span>

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a><span data-ttu-id="65ad6-138">改进了用户界面中的重复员工检查</span><span class="sxs-lookup"><span data-stu-id="65ad6-138">Improvements to the user interface for duplicate employee check</span></span>
<span data-ttu-id="65ad6-139">借助此更改，输入名称字段时可检测重复项，而状态将显示找到的重复项数量。</span><span class="sxs-lookup"><span data-stu-id="65ad6-139">With this change, duplicates are detected as you enter name fields, and a status displays the number of duplicates found.</span></span> <span data-ttu-id="65ad6-140">您可以选择提供的链接以打开一个新的页面来评估是否要使用检测到的匹配项。</span><span class="sxs-lookup"><span data-stu-id="65ad6-140">You can select the provided link to open a new page to evaluate whether to use the detected match.</span></span> <span data-ttu-id="65ad6-141">为了避免中断数据输入，重复项窗体不会自动打开。</span><span class="sxs-lookup"><span data-stu-id="65ad6-141">To avoid interrupting data entry, the duplicates form doesn't automatically open.</span></span>
## <a name="known-issues"></a><span data-ttu-id="65ad6-142">已知问题</span><span class="sxs-lookup"><span data-stu-id="65ad6-142">Known issues</span></span>

### <a name="email-support-for-alerts"></a><span data-ttu-id="65ad6-143">警报的电子邮件支持</span><span class="sxs-lookup"><span data-stu-id="65ad6-143">Email support for alerts</span></span>
<span data-ttu-id="65ad6-144">安装 Finance and Operations 的平台更新 26 之后，用户可创建警报规则，用于在被事件触发后自动向联系人发送电子邮件通知。</span><span class="sxs-lookup"><span data-stu-id="65ad6-144">With Platform update 26 for Finance and Operations, users can create alert rules that automatically send email notifications to contacts when triggered by an event.</span></span>
