---
title: Dynamics 365 Talent（2019 年 1 月 31 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 01/31/2019
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
ms.search.validFrom: 2019-01-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: fbbecd4e0f205c2f09ec30548756ff1a43872644
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/06/2019
ms.locfileid: "2899097"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-31-2019"></a><span data-ttu-id="8d9f0-103">Dynamics 365 Talent（2019 年 1 月 31 日）中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="8d9f0-103">What's new or changed in Dynamics 365 Talent (January 31, 2019)</span></span>

<span data-ttu-id="8d9f0-104">此主题介绍了 Dynamics 365 Talent 中的新增功能和更改的功能。</span><span class="sxs-lookup"><span data-stu-id="8d9f0-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

<span data-ttu-id="8d9f0-105">**内部版本 8.1.2128**</span><span class="sxs-lookup"><span data-stu-id="8d9f0-105">**Build 8.1.2128**</span></span>

## <a name="core-hr-changes"></a><span data-ttu-id="8d9f0-106">Core HR 更改</span><span class="sxs-lookup"><span data-stu-id="8d9f0-106">Core HR Changes</span></span>

### <a name="time-off-taken-on-leave-people-card-doesnt-consider-leave-plan-dates"></a><span data-ttu-id="8d9f0-107">在休假人员卡上请下的休假不考虑休假计划日期</span><span class="sxs-lookup"><span data-stu-id="8d9f0-107">Time off taken on leave people card doesn't consider leave plan dates</span></span>
<span data-ttu-id="8d9f0-108">对于有在日历年不运行的休假计划的员工，**已请假**卡现在显示在计划定义的休假年中获得的休假。</span><span class="sxs-lookup"><span data-stu-id="8d9f0-108">For those that have leave plans that don’t run on a calendar year, the **Taken** card now displays time off that’s been taken in the plan-defined leave year.</span></span> <span data-ttu-id="8d9f0-109">例如，如果组织的休假年是 6 月 1 到 5 月 30 日，并且员工在 12 月获得了 3 天休假，1 月 15 日的**已请假**卡将显示 3 天。</span><span class="sxs-lookup"><span data-stu-id="8d9f0-109">For example, if an organization’s leave year is June 1 through May 30 and an employee has taken 3 days off in December, the **Taken** card on January 15, will display 3 days.</span></span> 

### <a name="accrual-amounts-not-matching-tier-date-basis"></a><span data-ttu-id="8d9f0-110">应计金额与等级日期基础不匹配</span><span class="sxs-lookup"><span data-stu-id="8d9f0-110">Accrual amounts not matching tier date basis</span></span>
<span data-ttu-id="8d9f0-111">已向休假和缺勤（**人力资源**参数）添加了新选项来允许客户确定员工的服务月日期何时有效。</span><span class="sxs-lookup"><span data-stu-id="8d9f0-111">New options have been added to leave and absence (**Human resources** parameters) to enable customers to determine when employees’ months of service date are effective.</span></span> <span data-ttu-id="8d9f0-112">对于某些组织，此日期是当月的月底，但对于其他组织，可能是下个月的月初。</span><span class="sxs-lookup"><span data-stu-id="8d9f0-112">For some organizations, the date is the end of the month, but for others it may be the start of the next month.</span></span> <span data-ttu-id="8d9f0-113">例如，一个组织可能在 12 月 31 日奖励休假，而另一个组织则可能在 1 月 1 日奖励休假。</span><span class="sxs-lookup"><span data-stu-id="8d9f0-113">For example, one organization may award time off on December 31, while another may award time off on January 1.</span></span> <span data-ttu-id="8d9f0-114">此选项允许您选择应在何时进行奖励。</span><span class="sxs-lookup"><span data-stu-id="8d9f0-114">This option will allow you to choose when the award should occur.</span></span> 

### <a name="worker-hire-actions-are-stuck-in-workflow-complete-state"></a><span data-ttu-id="8d9f0-115">工作人员雇用操作卡在“工作流已完成”状态</span><span class="sxs-lookup"><span data-stu-id="8d9f0-115">Worker hire actions are stuck in "Workflow complete" state</span></span>
<span data-ttu-id="8d9f0-116">已进行更改来更正少数工作流的完成状态为“工作流已完成”的问题。</span><span class="sxs-lookup"><span data-stu-id="8d9f0-116">Changes have been made to correct an issue where a small number of workflows finished with a "Workflow complete" status.</span></span> <span data-ttu-id="8d9f0-117">新工作流现在在工作流完成时应移到“已完成”状态。</span><span class="sxs-lookup"><span data-stu-id="8d9f0-117">New workflows should now move to a "Completed" state when the workflow finishes.</span></span> <span data-ttu-id="8d9f0-118">工作流已完成状态的所有工作流都将转入错误状态以允许在需要时更新或删除。</span><span class="sxs-lookup"><span data-stu-id="8d9f0-118">Any workflows in a workflow completed status will be transitioned to an error status to allow for updating or removal if required.</span></span> 
