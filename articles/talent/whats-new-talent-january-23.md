---
title: Dynamics 365 Talent - Core HR（2019 年 1 月 23 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 Talent - Core HR 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 01/23/2019
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
ms.search.validFrom: 2019-01-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 3c7a389ef4a651135836ce682d7cda95c536011a
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550197"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-january-23-2019"></a><span data-ttu-id="28cd2-103">Dynamics 365 Talent - Core HR（2019 年 1 月 23 日）中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="28cd2-103">What's new or changed in Dynamics 365 Talent - Core HR (January 23, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="28cd2-104">**内部版本 8.1.2121**</span><span class="sxs-lookup"><span data-stu-id="28cd2-104">**Build 8.1.2121**</span></span>

<span data-ttu-id="28cd2-105">此主题介绍了 Core HR 中的新增功能和更改的功能。</span><span class="sxs-lookup"><span data-stu-id="28cd2-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="28cd2-106">更改</span><span class="sxs-lookup"><span data-stu-id="28cd2-106">Changes</span></span>

### <a name="import-of-employee-fixed-compensation-not-working-when-creating-new-fixed-compensation-records"></a><span data-ttu-id="28cd2-107">创建新的固定薪酬记录时导入员工固定薪酬不工作</span><span class="sxs-lookup"><span data-stu-id="28cd2-107">Import of employee fixed compensation not working when creating new fixed compensation records</span></span>
<span data-ttu-id="28cd2-108">对员工固定薪酬实体进行了更改以在导入后检索薪酬级别。</span><span class="sxs-lookup"><span data-stu-id="28cd2-108">A change has been made to the employee fixed compensation entity to retrieve the compensation level upon import.</span></span> <span data-ttu-id="28cd2-109">在此版本前，将显示一条消息，指示需要级别。</span><span class="sxs-lookup"><span data-stu-id="28cd2-109">Prior to this release, a message was displayed indicating that the level was required.</span></span>

### <a name="remove-the-minimum-balance-field-from-the-time-off-request-dialog-box"></a><span data-ttu-id="28cd2-110">从请假对话框中删除最小余额字段</span><span class="sxs-lookup"><span data-stu-id="28cd2-110">Remove the minimum balance field from the time off request dialog box</span></span>
<span data-ttu-id="28cd2-111">已从**请假**对话框中删除了**最小余额**字段。</span><span class="sxs-lookup"><span data-stu-id="28cd2-111">The **Minimum balance** field has been removed from the **Time off request** dialog box.</span></span> <span data-ttu-id="28cd2-112">此更改会影响可以请假的所有区域。</span><span class="sxs-lookup"><span data-stu-id="28cd2-112">This change affects all areas where time off can be requested.</span></span>

### <a name="data-upgrade-for-compensation-levels-not-updating-in-all-scenarios"></a><span data-ttu-id="28cd2-113">薪酬级别的数据升级未在所有方案中更新</span><span class="sxs-lookup"><span data-stu-id="28cd2-113">Data upgrade for compensation levels not updating in all scenarios</span></span>
<span data-ttu-id="28cd2-114">已进行了更改以更新固定薪酬计划中的薪酬级别。</span><span class="sxs-lookup"><span data-stu-id="28cd2-114">A change has been made to update the compensation level on fixed compensation plans.</span></span> <span data-ttu-id="28cd2-115">此更改将填充分配给员工的工作的固定计划中的薪酬级别。</span><span class="sxs-lookup"><span data-stu-id="28cd2-115">This change will populate the compensation level on fixed plans for the job assigned to the employee.</span></span>

### <a name="payroll-information-in-the-manage-changes-page-is-only-available-when-logged-in-as-system-administrator"></a><span data-ttu-id="28cd2-116">管理更改页面的工资单信息仅在作为系统管理员登录后可用</span><span class="sxs-lookup"><span data-stu-id="28cd2-116">Payroll information in the Manage changes page is only available when logged in as System Administrator</span></span>
<span data-ttu-id="28cd2-117">此更改允许具有工资管理员角色的员工在职位的**更改日程表 > 管理更改**页访问工资单信息。</span><span class="sxs-lookup"><span data-stu-id="28cd2-117">This change allows employees with the Payroll Administrator role access to the payroll information on the **Changes timeline > Manage changes** page for the position.</span></span>

### <a name="job-fields-default-to-positions"></a><span data-ttu-id="28cd2-118">工作字段默认为职位</span><span class="sxs-lookup"><span data-stu-id="28cd2-118">Job fields default to positions</span></span>
<span data-ttu-id="28cd2-119">在更改职位中的工作时，工作字段将默认为职位。</span><span class="sxs-lookup"><span data-stu-id="28cd2-119">When changing the job on a position, job fields will default to the position.</span></span> <span data-ttu-id="28cd2-120">预警消息将显示，提供接受默认值或保留这些字段的现有值的选项。</span><span class="sxs-lookup"><span data-stu-id="28cd2-120">An alert message will appear giving an option to accept the default values or keep the existing values for those fields.</span></span>

### <a name="probation-period-and-calendar-are-not-displayed-for-future-hired-employees"></a><span data-ttu-id="28cd2-121">试用期和日历没有为将来雇用的员工显示。</span><span class="sxs-lookup"><span data-stu-id="28cd2-121">Probation period and calendar are not displayed for future hired employees.</span></span>
<span data-ttu-id="28cd2-122">通过此更改，**试用期**和**日历**字段已添加到**管理更改**页以允许将来以及过去员工的数据输入。</span><span class="sxs-lookup"><span data-stu-id="28cd2-122">With this change, **Probation period** and **Calendar** fields have been added to the **Manage changes** page to allow for data entry for future and past employees.</span></span>

### <a name="platform-update-23-for-finance-and-operations"></a><span data-ttu-id="28cd2-123">Finance and Operations 的平台更新 23</span><span class="sxs-lookup"><span data-stu-id="28cd2-123">Platform update 23 for Finance and Operations</span></span>
<span data-ttu-id="28cd2-124">细微缺陷修复作为 Finance and Operations 的平台更新 23 的一部分包括在内。</span><span class="sxs-lookup"><span data-stu-id="28cd2-124">Minor bug fixes have been included as part of Platform update 23 for Finance and Operations.</span></span> <span data-ttu-id="28cd2-125">有关详细信息，请参阅 [Dynamics 365 Finance and Operations 平台更新 23（2019 年 1 月）的新增功能和更改内容](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23)。</span><span class="sxs-lookup"><span data-stu-id="28cd2-125">For more information, see [What's new or changed in Dynamics 365 Finance and Operations platform update 23 (January 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23).</span></span> 
