---
title: Dynamics 365 Human Resources（2020 年 6 月 11 日）新增功能或更改
description: 此主题介绍了 2020 年 6 月 11 日 Microsoft Dynamics 365 Human Resources - Core HR 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 06/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-06-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0720b2024a865fcd42cd80fd905586d626388f8f
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/20/2020
ms.locfileid: "3711786"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-11-2020"></a><span data-ttu-id="fd322-103">Dynamics 365 Human Resources（2020 年 6 月 11 日）新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="fd322-103">What's new or changed in Dynamics 365 Human Resources (June 11, 2020)</span></span>

<span data-ttu-id="fd322-104">本文介绍 Dynamics 365 Human Resources 中的新增功能或更改的功能。</span><span class="sxs-lookup"><span data-stu-id="fd322-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="fd322-105">更改适用于内部版本号 8.1.3316。</span><span class="sxs-lookup"><span data-stu-id="fd322-105">Changes apply to build number 8.1.3316.</span></span> <span data-ttu-id="fd322-106">某些标题中括号内的数字是 LCS 支持号码，供您参考。</span><span class="sxs-lookup"><span data-stu-id="fd322-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="streamlined-employee-form-sometimes-causes-child-form-close-x-buttons-to-stop-working-442369"></a><span data-ttu-id="fd322-107">简化的员工窗体有时导致子窗体关闭 (X) 按钮停止工作 (442369)</span><span class="sxs-lookup"><span data-stu-id="fd322-107">Streamlined employee form sometimes causes child form close (X) buttons to stop working (442369)</span></span>

<span data-ttu-id="fd322-108">当新的**工作人员**窗体启用后，关闭 (**X**) 按钮有时对子窗体不起作用。</span><span class="sxs-lookup"><span data-stu-id="fd322-108">When the new **Worker** form was enabled, the close (**X**) button occasionally didn't work on child forms.</span></span> <span data-ttu-id="fd322-109">此问题是间歇性的。</span><span class="sxs-lookup"><span data-stu-id="fd322-109">This problem was intermittent.</span></span> <span data-ttu-id="fd322-110">您可以在离开然后返回窗体后关闭窗体。</span><span class="sxs-lookup"><span data-stu-id="fd322-110">You could close the form after leaving and coming back to it.</span></span> <span data-ttu-id="fd322-111">例如，您可以选择左侧的菜单项，然后导航回**工作人员**窗体将其关闭。</span><span class="sxs-lookup"><span data-stu-id="fd322-111">For example, you could select a menu item on the left, and navigate back to the **Worker** form, and then close it.</span></span> <span data-ttu-id="fd322-112">本周的发布将解决此问题。</span><span class="sxs-lookup"><span data-stu-id="fd322-112">This week's release fixes this problem.</span></span> 

## <a name="the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-a-parent-relationship-type"></a><span data-ttu-id="fd322-113">工作人员个人联系人实体不能导出具有父关系类型的个人联系人</span><span class="sxs-lookup"><span data-stu-id="fd322-113">The Worker personal contact person entity doesn't export personal contacts with a parent relationship type</span></span>

<span data-ttu-id="fd322-114">通过此发布，**工作人员个人联系人**实体可以导出所有关系类型。</span><span class="sxs-lookup"><span data-stu-id="fd322-114">With this release, the **Worker personal contact person** entity exports all relationship types.</span></span>

## <a name="the-hcmpositionworkerassignmentv2entity-should-be-part-of-the-ceridian-payroll-integration-package-by-default-448506"></a><span data-ttu-id="fd322-115">默认情况下，HcmPositionWorkerAssignmentV2Entity 应该是 Ceridian 工资单集成包的一部分 (448506)</span><span class="sxs-lookup"><span data-stu-id="fd322-115">The HcmPositionWorkerAssignmentV2Entity should be part of the Ceridian payroll integration package by default (448506)</span></span>

<span data-ttu-id="fd322-116">通过此更改，**HcmPositionWorkerAssignmentV2Entity** 将包含在 Ceridian 工资单集成包中。</span><span class="sxs-lookup"><span data-stu-id="fd322-116">With this change, the **HcmPositionWorkerAssignmentV2Entity** is included in the Ceridian payroll integration package.</span></span>

## <a name="in-preview"></a><span data-ttu-id="fd322-117">预览模式</span><span class="sxs-lookup"><span data-stu-id="fd322-117">In preview</span></span>

## <a name="database-logging"></a><span data-ttu-id="fd322-118">数据库记录</span><span class="sxs-lookup"><span data-stu-id="fd322-118">Database logging</span></span>

<span data-ttu-id="fd322-119">数据库日志记录功能让您可以确定要监视哪些表和字段。</span><span class="sxs-lookup"><span data-stu-id="fd322-119">The database logging feature allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="fd322-120">它还让您能够确定应该触发更改跟踪的事件。</span><span class="sxs-lookup"><span data-stu-id="fd322-120">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="fd322-121">您可以使用数据库日志记录功能来查看一段时间内的更改。</span><span class="sxs-lookup"><span data-stu-id="fd322-121">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="fd322-122">有关详细信息，请参阅[配置和管理数据库日志记录](hr-admin-database-logging.md)。</span><span class="sxs-lookup"><span data-stu-id="fd322-122">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="fd322-123">Teams 中的 Human Resources 应用程序</span><span class="sxs-lookup"><span data-stu-id="fd322-123">Human Resources application in Teams</span></span>

<span data-ttu-id="fd322-124">员工可以在 Microsoft Teams 中查看和请求离岗时间。</span><span class="sxs-lookup"><span data-stu-id="fd322-124">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="fd322-125">他们可以与机器人交互来创建休假请求。</span><span class="sxs-lookup"><span data-stu-id="fd322-125">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="fd322-126">有关详细信息，请参阅 [Teams 中的 Human Resources 应用](https://go.microsoft.com/fwlink/?linkid=2127841)。</span><span class="sxs-lookup"><span data-stu-id="fd322-126">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="fd322-127">用于福利管理的数据管理框架 (DMF) 实体</span><span class="sxs-lookup"><span data-stu-id="fd322-127">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="fd322-128">福利管理实体即将发布。</span><span class="sxs-lookup"><span data-stu-id="fd322-128">Benefits management entities are releasing.</span></span> <span data-ttu-id="fd322-129">DMF 实体允许导入和导出数据，以轻松配置福利管理。</span><span class="sxs-lookup"><span data-stu-id="fd322-129">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="fd322-130">福利管理模板可用于移动数据。</span><span class="sxs-lookup"><span data-stu-id="fd322-130">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="fd322-131">模板按顺序导出和导入数据，以保持数据依赖关系。</span><span class="sxs-lookup"><span data-stu-id="fd322-131">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="fd322-132">购买和出售休假</span><span class="sxs-lookup"><span data-stu-id="fd322-132">Buy and sell leave</span></span> 

<span data-ttu-id="fd322-133">一些组织提供允许员工购买和出售其休假的福利。</span><span class="sxs-lookup"><span data-stu-id="fd322-133">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="fd322-134">此流程通常通过手动管理。</span><span class="sxs-lookup"><span data-stu-id="fd322-134">This process is often managed manually.</span></span> <span data-ttu-id="fd322-135">此功能可自动管理人力资源部门的策略和请求。</span><span class="sxs-lookup"><span data-stu-id="fd322-135">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="fd322-136">它将简化休假管理流程，并帮助消除错误。</span><span class="sxs-lookup"><span data-stu-id="fd322-136">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="fd322-137">有关详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="fd322-137">For more information, see:</span></span>

- [<span data-ttu-id="fd322-138">管理购买和出售休假策略</span><span class="sxs-lookup"><span data-stu-id="fd322-138">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="fd322-139">购买和出售休假</span><span class="sxs-lookup"><span data-stu-id="fd322-139">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="fd322-140">单个公司或单个计划的休假假期额度</span><span class="sxs-lookup"><span data-stu-id="fd322-140">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="fd322-141">客户可以处理单个公司或单个休假和缺勤计划的应计项目。</span><span class="sxs-lookup"><span data-stu-id="fd322-141">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="fd322-142">此功能为具有不同休假年限或休假应计政策的客户提供清晰的应计流程。</span><span class="sxs-lookup"><span data-stu-id="fd322-142">This ability provides clarity into the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="fd322-143">有关详细信息，请参阅[按公司或按休假计划累积休假](hr-leave-and-absence-accrue.md)。</span><span class="sxs-lookup"><span data-stu-id="fd322-143">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="fd322-144">将附件添加到休假请求</span><span class="sxs-lookup"><span data-stu-id="fd322-144">Add attachments to time off requests</span></span>

<span data-ttu-id="fd322-145">在当前的 COVID-19 环境中，向批准的休假请求添加附件的功能至关重要。</span><span class="sxs-lookup"><span data-stu-id="fd322-145">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="fd322-146">员工现在可以添加这些附件。</span><span class="sxs-lookup"><span data-stu-id="fd322-146">Employees can now add these attachments.</span></span> <span data-ttu-id="fd322-147">他们还将对休假请求进行了怎样的更新有更多了解。</span><span class="sxs-lookup"><span data-stu-id="fd322-147">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="fd322-148">有关详细信息，请参阅[将附件添加到现有请求](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request)。</span><span class="sxs-lookup"><span data-stu-id="fd322-148">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="fd322-149">将原因代码添加到应计暂停</span><span class="sxs-lookup"><span data-stu-id="fd322-149">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="fd322-150">原因代码已添加到应计暂停。</span><span class="sxs-lookup"><span data-stu-id="fd322-150">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="fd322-151">结转规则</span><span class="sxs-lookup"><span data-stu-id="fd322-151">Carry forward rules</span></span> 

<span data-ttu-id="fd322-152">可为转移了结转调整的结转余额指定结转休假类型。</span><span class="sxs-lookup"><span data-stu-id="fd322-152">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="fd322-153">例如，如果员工结转 10 天，则可为这 10 天选择其他休假类型。</span><span class="sxs-lookup"><span data-stu-id="fd322-153">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="fd322-154">有关详细信息，请参阅[配置休假和缺勤类型](hr-leave-and-absence-types.md)。</span><span class="sxs-lookup"><span data-stu-id="fd322-154">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="fd322-155">暂停指定休假类型的休假应计</span><span class="sxs-lookup"><span data-stu-id="fd322-155">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="fd322-156">您可以创建一个规则，以针对输入了无薪假休假请求的员工暂停休假应计。</span><span class="sxs-lookup"><span data-stu-id="fd322-156">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="fd322-157">无薪假可以是一种类型，但不是必须的。</span><span class="sxs-lookup"><span data-stu-id="fd322-157">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="fd322-158">您可以根据其他休假类型暂停任何休假。</span><span class="sxs-lookup"><span data-stu-id="fd322-158">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="fd322-159">可用于暂停应计的 DMF 实体</span><span class="sxs-lookup"><span data-stu-id="fd322-159">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="fd322-160">DMF 实体现在可用于暂停应计。</span><span class="sxs-lookup"><span data-stu-id="fd322-160">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="fd322-161">即将到期</span><span class="sxs-lookup"><span data-stu-id="fd322-161">Coming soon</span></span>

## <a name="new-platform-capabilities"></a><span data-ttu-id="fd322-162">新平台功能</span><span class="sxs-lookup"><span data-stu-id="fd322-162">New platform capabilities</span></span> 

<span data-ttu-id="fd322-163">您将可以通过使用个性化将字段设为必填字段。</span><span class="sxs-lookup"><span data-stu-id="fd322-163">You'll be able to make fields mandatory by using personalization.</span></span> <span data-ttu-id="fd322-164">此功能需要您启用**已保存视图**。</span><span class="sxs-lookup"><span data-stu-id="fd322-164">This feature will require you to enable **Saved views**.</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="fd322-165">配置员工自助服务的名称</span><span class="sxs-lookup"><span data-stu-id="fd322-165">Configure the name of Employee self-service</span></span>

<span data-ttu-id="fd322-166">人力资源参数中将提供一个新选项，可以将“员工自助服务”工作区的名称更新为“自助服务”。</span><span class="sxs-lookup"><span data-stu-id="fd322-166">A new option will be available in Human Resources parameters to update the name of the Employee self service workspace to Self service.</span></span> 

## <a name="see-also"></a><span data-ttu-id="fd322-167">请参阅</span><span class="sxs-lookup"><span data-stu-id="fd322-167">See also</span></span>

[<span data-ttu-id="fd322-168">Human Resources 中新增或更改的功能</span><span class="sxs-lookup"><span data-stu-id="fd322-168">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="fd322-169">Dynamics 365 Human Resources 2019 发布第 2 波概述</span><span class="sxs-lookup"><span data-stu-id="fd322-169">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="fd322-170">更新流程</span><span class="sxs-lookup"><span data-stu-id="fd322-170">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="fd322-171">管理功能</span><span class="sxs-lookup"><span data-stu-id="fd322-171">Manage features</span></span>](hr-admin-manage-features.md)