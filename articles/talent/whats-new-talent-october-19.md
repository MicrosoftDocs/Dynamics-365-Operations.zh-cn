---
title: "Dynamics 365 for Talent Core HR（2018 年 10 月 16 日）中的新增功能或更改的功能"
description: "此主题介绍了 Microsoft Dynamics 365 for Talent Core HR 中的新功能和更改的功能。"
author: Darinkramer
manager: AnnBe
ms.date: 10/22/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-22
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: 2eb46f436305a4c81ea99553e4dc07288ee74008
ms.openlocfilehash: 7da597a682006cddb44ff9354813b07c15c1a449
ms.contentlocale: zh-cn
ms.lasthandoff: 10/22/2018

---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-19-2018"></a><span data-ttu-id="6d39c-103">Dynamics 365 for Talent Core HR（2018 年 10 月 19 日）中的新增功能或更改的功能</span><span class="sxs-lookup"><span data-stu-id="6d39c-103">What's new or changed in Dynamics 365 for Talent Core HR (October 19, 2018)</span></span>

[!include[banner](includes/banner.md)]

<span data-ttu-id="6d39c-104">**内部版本 8.1.1067**</span><span class="sxs-lookup"><span data-stu-id="6d39c-104">**Build 8.1.1067**</span></span>

<span data-ttu-id="6d39c-105">此主题介绍了 Core HR 中的新增功能和更改的功能。</span><span class="sxs-lookup"><span data-stu-id="6d39c-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="allow-managers-to-update-time-off-requests"></a><span data-ttu-id="6d39c-106">允许经理更新休假请求</span><span class="sxs-lookup"><span data-stu-id="6d39c-106">Allow managers to update time off requests</span></span>

<span data-ttu-id="6d39c-107">员工休假请求在通过工作流审批后可能需要更新。</span><span class="sxs-lookup"><span data-stu-id="6d39c-107">Employee time off requests may need to be updated after they are approved through the workflow.</span></span> <span data-ttu-id="6d39c-108">在大多数情况下，经理代表员工进行这些更新。</span><span class="sxs-lookup"><span data-stu-id="6d39c-108">In many cases, the manager makes these updates on the employee’s behalf.</span></span> <span data-ttu-id="6d39c-109">此新功能为经理提供代表其员工更新休假或取消休假请求的能力。</span><span class="sxs-lookup"><span data-stu-id="6d39c-109">This new feature provides the ability for managers to update time off or cancel time off requests on behalf of their employees.</span></span> <span data-ttu-id="6d39c-110">此功能由**代为工作**参数控制，此参数可以在**人力资源参数**页设置。</span><span class="sxs-lookup"><span data-stu-id="6d39c-110">This capability is controlled by the **Work on behalf** parameter that can be set on the **Human Resource Parameters** page.</span></span> 
 
## <a name="allow-hr-to-update-time-off-requests"></a><span data-ttu-id="6d39c-111">允许人力资源更新休假请求</span><span class="sxs-lookup"><span data-stu-id="6d39c-111">Allow HR to update time off requests</span></span>

<span data-ttu-id="6d39c-112">与上述功能类似，员工休假请求之前在通过工作流审批后可能需要由人力资源更新。</span><span class="sxs-lookup"><span data-stu-id="6d39c-112">Similar to the feature above, employee time off requests may need to be updated by HR after they have been previously approved through the workflow.</span></span> <span data-ttu-id="6d39c-113">此功能为人力资源用户提供更新休假请求的能力。</span><span class="sxs-lookup"><span data-stu-id="6d39c-113">This feature provides the ability for HR users to update time off requests.</span></span> <span data-ttu-id="6d39c-114">此功能在**人员**工作区和**工作人员**页面使用称为**查看休假**的新选项启用。</span><span class="sxs-lookup"><span data-stu-id="6d39c-114">The capability is enabled in the **People** workspace and on the **Worker** page, using a new option called **View time off**.</span></span> <span data-ttu-id="6d39c-115">在这些页面上，人力资源用户可以查看请求并更新休假交易记录，类似于经理执行这些操作的方式。</span><span class="sxs-lookup"><span data-stu-id="6d39c-115">On those pages, HR users can view requests and update time off transactions, similar to how managers can perform these actions.</span></span>

<span data-ttu-id="6d39c-116">控制此功能的访问的安全责任是：</span><span class="sxs-lookup"><span data-stu-id="6d39c-116">The security duty that controls access to this functionality is:</span></span>
- <span data-ttu-id="6d39c-117">责任：维护特定工作人员休假和缺勤的流程。</span><span class="sxs-lookup"><span data-stu-id="6d39c-117">Duty: Maintain worker-specific leave and absence processes.</span></span>
- <span data-ttu-id="6d39c-118">权限：维护所有工作人员的休假和缺勤请求。</span><span class="sxs-lookup"><span data-stu-id="6d39c-118">Privilege: Maintain leave and absence requests for all workers.</span></span>

## <a name="other-changes"></a><span data-ttu-id="6d39c-119">其他更改</span><span class="sxs-lookup"><span data-stu-id="6d39c-119">Other changes</span></span>
<span data-ttu-id="6d39c-120">此版本已进行以下更新：</span><span class="sxs-lookup"><span data-stu-id="6d39c-120">The following updates have been made in this release:</span></span>
- <span data-ttu-id="6d39c-121">更改了工作人员招聘操作，以便操作不会再被“卡”在**工作流已完成**状态。</span><span class="sxs-lookup"><span data-stu-id="6d39c-121">Changes to worker hire actions so that they are no longer "stuck" in **Workflow complete** state.</span></span>
- <span data-ttu-id="6d39c-122">雇用记录现在可以创建，其中没有雇用开始日期。</span><span class="sxs-lookup"><span data-stu-id="6d39c-122">Employment record can now be created without an employment start date.</span></span>
- <span data-ttu-id="6d39c-123">在员工自助服务中显示的课程的 Dynamics 365 Talent 登记日期现在将时区偏移应用到日期。</span><span class="sxs-lookup"><span data-stu-id="6d39c-123">The Dynamics 365 Talent registration date for a course shown in Employee self-service now applies the time zone offset to the date.</span></span>
- <span data-ttu-id="6d39c-124">使用**员工实体**可以没有任何错误地多次导入 Excel 文件。</span><span class="sxs-lookup"><span data-stu-id="6d39c-124">Excel files can be imported multiple times without any errors using **Employee Entity**.</span></span>

## <a name="known-issue"></a><span data-ttu-id="6d39c-125">已知问题</span><span class="sxs-lookup"><span data-stu-id="6d39c-125">Known issue</span></span>

- <span data-ttu-id="6d39c-126">**问题**：在将新附件添加到工作人员时，**新建**和**编辑**按钮变灰。</span><span class="sxs-lookup"><span data-stu-id="6d39c-126">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="6d39c-127">**解决方法：** 打开附件页面之前，确保已关闭**工作人员**页面中的速见表。</span><span class="sxs-lookup"><span data-stu-id="6d39c-127">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="6d39c-128">如果加载**工作人员**页面时速见表已关闭，将启用附件按钮。</span><span class="sxs-lookup"><span data-stu-id="6d39c-128">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="6d39c-129">（下一个平台更新中将解决这个问题。）</span><span class="sxs-lookup"><span data-stu-id="6d39c-129">(This issue will be fixed in the next platform update.)</span></span>

