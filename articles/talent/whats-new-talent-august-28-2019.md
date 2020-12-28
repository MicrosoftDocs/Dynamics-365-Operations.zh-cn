---
title: Dynamics 365 for Talent 的新增功能或更改（2019 年 8 月 27 日）
description: 此主题介绍了 Microsoft Dynamics 365 for Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 8/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: andreabichsel
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-08-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 8965636e539345be5ef0ad591f7017938efd322d
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529796"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-august-27-2019"></a><span data-ttu-id="f247d-103">Dynamics 365 for Talent 的新增功能或更改（2019 年 8 月 27 日）</span><span class="sxs-lookup"><span data-stu-id="f247d-103">What's new or changed in Dynamics 365 for Talent (August 27, 2019)</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="f247d-104">此主题介绍了 Dynamics 365 for Talent 中的新增功能和更改的功能。</span><span class="sxs-lookup"><span data-stu-id="f247d-104">This topic describes features that are either new or changed in Dynamics 365 for Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="f247d-105">Attract 中的更改</span><span class="sxs-lookup"><span data-stu-id="f247d-105">Changes in Attract</span></span>

<span data-ttu-id="f247d-106">本版本中包含 Dynamics 365 Talent: Attract 的小缺陷修复。</span><span class="sxs-lookup"><span data-stu-id="f247d-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="f247d-107">Onboard 中的更改</span><span class="sxs-lookup"><span data-stu-id="f247d-107">Changes in Onboard</span></span>

<span data-ttu-id="f247d-108">本版本中包含 Dynamics 365 Talent: Onboard 的小缺陷修复。</span><span class="sxs-lookup"><span data-stu-id="f247d-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="f247d-109">Core HR 中的更改</span><span class="sxs-lookup"><span data-stu-id="f247d-109">Changes in Core HR</span></span>

<span data-ttu-id="f247d-110">本部分中的更改适用于内部版本号 8.1.2447。</span><span class="sxs-lookup"><span data-stu-id="f247d-110">Changes described in this section apply to build number 8.1.2447.</span></span> <span data-ttu-id="f247d-111">某些标题中括号内的数字是 Microsoft Dynamics Lifecycle Services (LCS) 中的支持号码。</span><span class="sxs-lookup"><span data-stu-id="f247d-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a><span data-ttu-id="f247d-112">只有沙盒实例中才会启用预览功能</span><span class="sxs-lookup"><span data-stu-id="f247d-112">Preview features are enabled only in sandbox instances</span></span>

<span data-ttu-id="f247d-113">配置新的 Talent 实例时，可指定实例类型为生产还是沙盒。</span><span class="sxs-lookup"><span data-stu-id="f247d-113">When you provision a new instance of Talent, you can specify whether the instance type is Production or Sandbox.</span></span> <span data-ttu-id="f247d-114">沙盒类型的实例可用于提前测试新功能。</span><span class="sxs-lookup"><span data-stu-id="f247d-114">Instances of the Sandbox type allow for early testing of new features.</span></span> <span data-ttu-id="f247d-115">将把所有现有 Talent 实例更新为生产实例类型。</span><span class="sxs-lookup"><span data-stu-id="f247d-115">All existing Talent instances will be updated to the Production instance type.</span></span> <span data-ttu-id="f247d-116">如果需要将现有实例之一更新为沙盒实例类型，请联系支持以发起更改请求。</span><span class="sxs-lookup"><span data-stu-id="f247d-116">If you want one of your existing instances to be updated to the Sandbox instance type, contact Support to initiate the change request.</span></span>

<span data-ttu-id="f247d-117">有关如何发布更改的详细信息，请参阅[配置 Talent](./provisioning-talent.md)。</span><span class="sxs-lookup"><span data-stu-id="f247d-117">For more information about how changes are published, see [Provision Talent](./provisioning-talent.md).</span></span>

### <a name="view-extended-information-for-performance-in-manager-self-service"></a><span data-ttu-id="f247d-118">在经理自助服务中查看绩效的更多信息</span><span class="sxs-lookup"><span data-stu-id="f247d-118">View extended information for performance in manager self-service</span></span>

<span data-ttu-id="f247d-119">经理可通过一个新选项查看直接报表和扩展报表的绩效。</span><span class="sxs-lookup"><span data-stu-id="f247d-119">A new option will let managers view the performance of both their direct reports and their extended reports.</span></span> <span data-ttu-id="f247d-120">现在，职能经理可以分配和更新绩效目标和颁发新审核。</span><span class="sxs-lookup"><span data-stu-id="f247d-120">Currently, line managers can assign and update performance goals and issue new reviews.</span></span> <span data-ttu-id="f247d-121">此外，直属经理及其员工可维护和更新绩效日记帐，以帮助确保绩效复查流程顺利进行。</span><span class="sxs-lookup"><span data-stu-id="f247d-121">In addition, direct managers and their employees can maintain and update performance journals to help ensure that the performance review process goes smoothly.</span></span> <span data-ttu-id="f247d-122">实施此更改后，除了直接报表，经理还可以查看和维护与其扩展报表的绩效有关的信息。</span><span class="sxs-lookup"><span data-stu-id="f247d-122">When this change is implemented, managers will be able to view and maintain performance-related information for their extended reports in addition to their direct reports.</span></span>

### <a name="deleting-legal-entities-isnt-allowed-if-employees-exist-within-the-company-339849"></a><span data-ttu-id="f247d-123">如果员工存在于公司内，则不允许删除法人 (339849)</span><span class="sxs-lookup"><span data-stu-id="f247d-123">Deleting legal entities isn't allowed if employees exist within the company (339849)</span></span>

<span data-ttu-id="f247d-124">通过此更改，如果法人存在员工和其他相关数据，则无法移除或删除公司。</span><span class="sxs-lookup"><span data-stu-id="f247d-124">With this change, you can't remove or delete companies if employees and other related data exist for the legal entity.</span></span>

### <a name="compensation-management-business-intelligence-analytics-dont-match-on-the-compensation-workspace-322493"></a><span data-ttu-id="f247d-125">薪酬管理商业智能分析与薪酬工作区不匹配 (322493)</span><span class="sxs-lookup"><span data-stu-id="f247d-125">Compensation management business intelligence analytics don't match on the compensation workspace (322493)</span></span>

<span data-ttu-id="f247d-126">在此版本中，薪酬分析已经过调整，以准确反映分配给员工的计划。</span><span class="sxs-lookup"><span data-stu-id="f247d-126">In this release, compensation analytics have been adjusted to accurately reflect the plans assigned to employees.</span></span>

### <a name="workflow-placeholder-company-displays-dat-when-hiring-employees-through-workflow-343905"></a><span data-ttu-id="f247d-127">工作流占位符 %company% 在通过工作流招聘员工时显示 DAT (343905)</span><span class="sxs-lookup"><span data-stu-id="f247d-127">Workflow placeholder %company% displays DAT when hiring employees through workflow (343905)</span></span>

<span data-ttu-id="f247d-128">在此版本中，公司占位符显示与新员工的雇用相关的法人。</span><span class="sxs-lookup"><span data-stu-id="f247d-128">With this release, the company placeholder displays the legal entity that is associated with the employment of the new employee.</span></span>

### <a name="the-cdsjobposition-entity-displays-an-error-when-valid-to-date-is-set-349387"></a><span data-ttu-id="f247d-129">CDSJobPosition 实体在设置了失效日期时显示错误 (349387)</span><span class="sxs-lookup"><span data-stu-id="f247d-129">The CDSJobPosition entity displays an error when valid to date is set (349387)</span></span>

<span data-ttu-id="f247d-130">在此版本中，**CDSJobPosition** 实体上的 **职位详细信息** 和 **职位持续时间** 数据源允许从 Common Data Service 到 **生效日期** 字段的编辑。</span><span class="sxs-lookup"><span data-stu-id="f247d-130">In this release, the **Position detail** and the **Position duration** data sources on the **CDSJobPosition** entity allow for edits from Common Data Service to the **Date effective** fields.</span></span> 

### <a name="for-employee-termination-the-last-day-worked-is-populated-on-assignment-end-date-332496"></a><span data-ttu-id="f247d-131">对于员工终止雇用，工作的最后一天将在分配结束日期填充 (332496)</span><span class="sxs-lookup"><span data-stu-id="f247d-131">For employee termination, the last day worked is populated on Assignment end date (332496)</span></span>

<span data-ttu-id="f247d-132">此更改现在将职位的 **分配结束日期** 默认为 **雇用结束日期**。</span><span class="sxs-lookup"><span data-stu-id="f247d-132">This change now defaults the position **Assignment end date** to the **Employment end date**.</span></span> <span data-ttu-id="f247d-133">您可以在输入数据时更改这些默认值。</span><span class="sxs-lookup"><span data-stu-id="f247d-133">You can change these defaults while entering data.</span></span>

### <a name="legal-entities-arent-limited-with-hire-338871"></a><span data-ttu-id="f247d-134">法人不受雇用限制 (338871)</span><span class="sxs-lookup"><span data-stu-id="f247d-134">Legal entities aren't limited with hire (338871)</span></span>
 
<span data-ttu-id="f247d-135">此更改将招聘流程限制为仅显示用户有权访问的法人。</span><span class="sxs-lookup"><span data-stu-id="f247d-135">This change restricts the hiring process to only show those legal entities the user has access to.</span></span>  

## <a name="in-preview"></a><span data-ttu-id="f247d-136">预览模式</span><span class="sxs-lookup"><span data-stu-id="f247d-136">In preview</span></span>

### <a name="streamlined-employee-entry-and-navigation"></a><span data-ttu-id="f247d-137">简化的员工条目和导航</span><span class="sxs-lookup"><span data-stu-id="f247d-137">Streamlined employee entry and navigation</span></span>

<span data-ttu-id="f247d-138">此功能现在可在沙盒和试用环境中使用。</span><span class="sxs-lookup"><span data-stu-id="f247d-138">This functionality is now available in sandbox and trial environments.</span></span> <span data-ttu-id="f247d-139">要打开此功能，请导航至 **系统管理 > 链接 > 设置 > 系统参数 > 预览功能**。</span><span class="sxs-lookup"><span data-stu-id="f247d-139">To turn this feature on, navigate to **System administration > Links > Setup > System parameters > Preview features**.</span></span> <span data-ttu-id="f247d-140">选择 **增强的工作人员窗体和导航**。</span><span class="sxs-lookup"><span data-stu-id="f247d-140">Select **Enhanced worker form and navigation**.</span></span> <span data-ttu-id="f247d-141">这为所有用户启用了这些更改。</span><span class="sxs-lookup"><span data-stu-id="f247d-141">This enables these changes for all users.</span></span> <span data-ttu-id="f247d-142">您可以随时关闭此选项。</span><span class="sxs-lookup"><span data-stu-id="f247d-142">You can turn this option off at any time.</span></span>

<span data-ttu-id="f247d-143">有关详细信息，请参阅[简化的员工输入和导航](./streamlined-employee-entry.md)。</span><span class="sxs-lookup"><span data-stu-id="f247d-143">For more information, see [Streamlined employee entry and navigation](./streamlined-employee-entry.md).</span></span>

## <a name="coming-soon"></a><span data-ttu-id="f247d-144">即将到期</span><span class="sxs-lookup"><span data-stu-id="f247d-144">Coming soon</span></span>

### <a name="platform-update-29"></a><span data-ttu-id="f247d-145">平台 update 29</span><span class="sxs-lookup"><span data-stu-id="f247d-145">Platform update 29</span></span>

<span data-ttu-id="f247d-146">有关平台更新 29 的其他详细信息，请参阅 [Dynamics 365 for Finance and Operations 平台更新 29（2019 年 10 月）中的预览功能](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-29)。</span><span class="sxs-lookup"><span data-stu-id="f247d-146">For more details about Platform update 29, see [Preview features in Dynamics 365 for Finance and Operations platform update 29 (October 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-29).</span></span>
