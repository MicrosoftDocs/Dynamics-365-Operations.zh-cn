---
title: Dynamics 365 for Talent（2019 年 5 月 13 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 for Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 05/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-05-13
ms.dyn365.ops.version: Talent
ms.openlocfilehash: dac453ee83492655b6681b9784af4712bf39fc2a
ms.sourcegitcommit: 2bbc0eeca6826c529fb729b82d16f287c1ce05bb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/16/2019
ms.locfileid: "1591494"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-may-13-2019"></a><span data-ttu-id="ae820-103">Dynamics 365 for Talent（2019 年 5 月 13 日）中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="ae820-103">What's new or changed in Dynamics 365 for Talent (May 13, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ae820-104">此主题介绍了 Dynamics 365 for Talent 中的新增功能和更改的功能。</span><span class="sxs-lookup"><span data-stu-id="ae820-104">This topic describes features that are either new or changed in Dynamics 365 for Talent.</span></span>

## <a name="coming-soon-in-attract"></a><span data-ttu-id="ae820-105">Attract 中即将推出</span><span class="sxs-lookup"><span data-stu-id="ae820-105">Coming soon in Attract</span></span>

### <a name="job-approvals-on-home-page"></a><span data-ttu-id="ae820-106">主页中的工作审核</span><span class="sxs-lookup"><span data-stu-id="ae820-106">Job approvals on home page</span></span>

<span data-ttu-id="ae820-107">仪表板的**审核**部分中将显示审核。</span><span class="sxs-lookup"><span data-stu-id="ae820-107">Approvals appear in an **Approvals** section on the dashboard.</span></span> <span data-ttu-id="ae820-108">审核人可以在**已分配给您**（其中显示工作 ID、头衔、其他审核人和分配的日期）下查看自己的审核。</span><span class="sxs-lookup"><span data-stu-id="ae820-108">Approvers can review their approvals under **Assigned to you**, which displays the job ID, title, other approvers, and date assigned.</span></span> <span data-ttu-id="ae820-109">提交工作共审核的用户可以在**您请求的**（其中显示仍然需要审核提交的工作的审核者）下查看自己的工作。</span><span class="sxs-lookup"><span data-stu-id="ae820-109">Users who submit a job for approval can review their jobs under **Requested by you**, which displays the approvers who still need to approve the submitted job.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="ae820-110">Onboard 中的更改</span><span class="sxs-lookup"><span data-stu-id="ae820-110">Changes in Onboard</span></span>

<span data-ttu-id="ae820-111">本版本中包含 Dynamics 365 Talent: Onboard 的小缺陷修复。</span><span class="sxs-lookup"><span data-stu-id="ae820-111">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="ae820-112">Core HR 中的更改</span><span class="sxs-lookup"><span data-stu-id="ae820-112">Changes in Core HR</span></span>

<span data-ttu-id="ae820-113">本部分中的更改适用于内部版本号 8.1.2297。</span><span class="sxs-lookup"><span data-stu-id="ae820-113">Changes described in this section apply to build number 8.1.2297.</span></span> <span data-ttu-id="ae820-114">某些标题中括号内的数字是 Microsoft Dynamics Lifecycle Services (LCS) 中的支持号码。</span><span class="sxs-lookup"><span data-stu-id="ae820-114">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="indicate-instance-type-when-provisioning-talent"></a><span data-ttu-id="ae820-115">配置 Talent 时指示实例类型</span><span class="sxs-lookup"><span data-stu-id="ae820-115">Indicate instance type when provisioning Talent</span></span>

<span data-ttu-id="ae820-116">配置新的 Talent 时，可以指示实例类型为**生产**还是**沙盒**，这样就可以提前测试新功能。</span><span class="sxs-lookup"><span data-stu-id="ae820-116">When provisioning a new instance of Talent, you can indicate whether the instance type is **Production** or **Sandbox**, which allows for early testing of new features.</span></span> <span data-ttu-id="ae820-117">将把所有现有 Talent 实例更新为**生产**实例类型。</span><span class="sxs-lookup"><span data-stu-id="ae820-117">All existing Talent instances will be updated to the **Production** instance type.</span></span> <span data-ttu-id="ae820-118">如果需要将现有实例之一更新为**沙盒**实例类型，请联系[支持](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/talent-support)以发起更改请求。</span><span class="sxs-lookup"><span data-stu-id="ae820-118">If you want one of your existing instances to be updated to the **Sandbox** instance type, please contact [Support](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/talent-support) to initiate the change request.</span></span>

### <a name="common-data-service-entity-support-for-custom-fields"></a><span data-ttu-id="ae820-119">Common Data Service 实体对自定义字段的支持</span><span class="sxs-lookup"><span data-stu-id="ae820-119">Common Data Service entity support for custom fields</span></span>

<span data-ttu-id="ae820-120">在本周的发布中，下列 Common Data Service 实体现在支持自定义字段：雇用、福利计算频率、福利计算比率、工作日历、工作日历假日和标识类型。</span><span class="sxs-lookup"><span data-stu-id="ae820-120">In this week's release, the following Common Data Service entities now support custom fields: Employment, Benefit calc frequency, Benefit calc rate, Work calendar holiday, and Identification type.</span></span>

### <a name="common-data-service-integration-page"></a><span data-ttu-id="ae820-121">Common Data Service 集成页</span><span class="sxs-lookup"><span data-stu-id="ae820-121">Common Data Service integration page</span></span>

<span data-ttu-id="ae820-122">此版本在**系统管理 > 链接 > 集成 > Common Data Service 配置**中提供一个新选项。</span><span class="sxs-lookup"><span data-stu-id="ae820-122">This release provides a new option in **System Administration > Links > Integrations > Common Data Service configuration**.</span></span> <span data-ttu-id="ae820-123">**Common Data Service 配置**选项为管理员或数据管理管理员提供了一些灵活性和对 Common Data Service 的见解。</span><span class="sxs-lookup"><span data-stu-id="ae820-123">The **Common Data Service configuration** option allows an administrator or data management administrator some flexibility and insights with the Common Data Service.</span></span> <span data-ttu-id="ae820-124">在此版本中，您可以启用或禁用 Common Data Service 与 Talent 实例的集成，以及查看 Talent 实例与 Common Data Service 之间的同步细节。</span><span class="sxs-lookup"><span data-stu-id="ae820-124">With this option, you can enable or disable Common Data Service integration with a Talent instance and view the sync details between the Talent instance and the Common Data Service.</span></span>

### <a name="import-performance-data-with-final-employee-rating-316710"></a><span data-ttu-id="ae820-125">导入绩效数据和最终员工评级 (316710)</span><span class="sxs-lookup"><span data-stu-id="ae820-125">Import performance data with final employee rating (316710)</span></span>

<span data-ttu-id="ae820-126">在此版本中，可以导入员工评级历史数据。</span><span class="sxs-lookup"><span data-stu-id="ae820-126">In this release, you can import historical employee rating data.</span></span> <span data-ttu-id="ae820-127">**FinalEmployeeRatingId** 字段现在拥有写入权限。</span><span class="sxs-lookup"><span data-stu-id="ae820-127">The **FinalEmployeeRatingId** field now has write permission.</span></span>

### <a name="cant-create-worker-address-in-common-data-service-and-sync-it-with-talent-317555"></a><span data-ttu-id="ae820-128">不能在 Common Data Service 中创建工作人员地址并与 Talent 同步 (317555)</span><span class="sxs-lookup"><span data-stu-id="ae820-128">Can't create Worker address in Common Data Service and sync it with Talent (317555)</span></span>

<span data-ttu-id="ae820-129">此更改允许将 Common Data Service 中创建的地址数据与 Talent 同步。</span><span class="sxs-lookup"><span data-stu-id="ae820-129">This change allows address data created in Common Data Service to sync with Talent.</span></span>

## <a name="in-preview"></a><span data-ttu-id="ae820-130">预览模式</span><span class="sxs-lookup"><span data-stu-id="ae820-130">In preview</span></span>

### <a name="new-page-to-validate-position-hierarchy-data"></a><span data-ttu-id="ae820-131">用于验证职位层次结构数据的新页面</span><span class="sxs-lookup"><span data-stu-id="ae820-131">New page to validate position hierarchy data</span></span>

<span data-ttu-id="ae820-132">人力资源 (HR) 和管理员可以验证管理层次结构以查找任何可能已无意导入的循环引用。</span><span class="sxs-lookup"><span data-stu-id="ae820-132">Human resources (HR) and administrators can validate the managerial hierarchy for any circular references that might have been inadvertently imported.</span></span> <span data-ttu-id="ae820-133">可从**组织管理 > 链接 > 职位 > 职位层次结构验证**访问这个新页面。</span><span class="sxs-lookup"><span data-stu-id="ae820-133">You can access this new page from **Organizational administration > Links > Positions > Position hierarchy validation**.</span></span>

### <a name="specify-reason-codes-on-leave-types"></a><span data-ttu-id="ae820-134">指定休假类型的原因代码</span><span class="sxs-lookup"><span data-stu-id="ae820-134">Specify reason codes on leave types</span></span>

<span data-ttu-id="ae820-135">组织可能需要有关休假请求的更多信息。</span><span class="sxs-lookup"><span data-stu-id="ae820-135">Organizations might require additional information about time-off requests.</span></span> <span data-ttu-id="ae820-136">现在可指定休假类型的原因代码，并让员工在休假请求中选择原因代码。</span><span class="sxs-lookup"><span data-stu-id="ae820-136">You can now specify reason codes for leave types and let employees select a reason code on their time-off requests.</span></span>

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a><span data-ttu-id="ae820-137">休假请求中的特定休假类型需要原因代码</span><span class="sxs-lookup"><span data-stu-id="ae820-137">Require reason codes for specific leave types on time-off requests</span></span>

<span data-ttu-id="ae820-138">组织可能会要求当员工提交休假请求时为特定休假类型设置原因代码。</span><span class="sxs-lookup"><span data-stu-id="ae820-138">Organizations might require reason codes for specific leave types when employees submit time-off requests.</span></span> <span data-ttu-id="ae820-139">可能因为公司政策或法规要求导致存在此项要求。</span><span class="sxs-lookup"><span data-stu-id="ae820-139">This requirement might exist because of company policy or regulatory requirements.</span></span> <span data-ttu-id="ae820-140">可以指定哪些休假类型需要原因代码，并且可以要求员工为自己的休假请求中的休假类型提供原因代码。</span><span class="sxs-lookup"><span data-stu-id="ae820-140">You can specify which leave types require a reason code, and you can require that employees provide a reason code for the leave type on their time-off requests.</span></span>

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a><span data-ttu-id="ae820-141">为 HR 提供休假和缺勤交易记录列表</span><span class="sxs-lookup"><span data-stu-id="ae820-141">Provide a leave and absence transaction list for HR</span></span>

<span data-ttu-id="ae820-142">跟踪员工休假和了解休假的计算方法这一功能不仅可以帮助 HR 解答员工的问题，还可以帮助确保员工的休假奖励精确无误。</span><span class="sxs-lookup"><span data-stu-id="ae820-142">The ability to track employee time off and understand how time off is calculated not only helps HR answer employee questions, but also helps ensure accurate time-off awards for employees.</span></span> <span data-ttu-id="ae820-143">HR 现在可以以新的视觉查看交易记录（授权、应计、调整和请求），这样 HR 人员就可以查看休假余额背后的原因。</span><span class="sxs-lookup"><span data-stu-id="ae820-143">HR now has a new view into the transactions (grants, accruals, adjustments, and requests), so that HR staff can view the reasons behind time-off balances.</span></span>
