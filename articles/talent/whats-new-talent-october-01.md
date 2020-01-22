---
title: Dynamics 365 Talent - Core HR（2018 年 10 月 1 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 Talent - Core HR 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 10/01/2018
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
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: Talent
ms.openlocfilehash: f872b0907e0f48e0b734c87f0b8fb1a4cfe20cb0
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896673"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-core-hr-october-1-2018"></a><span data-ttu-id="d4152-103">Dynamics 365 Talent: Core HR（2018 年 10 月 1 日）中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="d4152-103">What's new or changed in Dynamics 365 Talent: Core HR (October 1, 2018)</span></span>

<span data-ttu-id="d4152-104">**内部版本 8.1.1035.0**</span><span class="sxs-lookup"><span data-stu-id="d4152-104">**Build 8.1.1035.0**</span></span>

<span data-ttu-id="d4152-105">此主题介绍了 Core HR 中的新增功能和更改的功能。</span><span class="sxs-lookup"><span data-stu-id="d4152-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="turn-off-electronic-payment-validation"></a><span data-ttu-id="d4152-106">关闭电子付款验证</span><span class="sxs-lookup"><span data-stu-id="d4152-106">Turn off electronic payment validation</span></span>

<span data-ttu-id="d4152-107">如果通过**员工自助服务**工作区 (ESS) 或直接在员工窗体上为直接存款设置付款，将进行电子付款信息验证。</span><span class="sxs-lookup"><span data-stu-id="d4152-107">Electronic payment information validation occurs if you set up disbursements for direct deposit either through **Employee self-service** workspace (ESS) or directly on the employee form.</span></span> <span data-ttu-id="d4152-108">此选项让您在不需要对金额和剩余数量值进行验证检查时灵活地去除验证。</span><span class="sxs-lookup"><span data-stu-id="d4152-108">This option gives you the flexibility to remove that validation if you do not require the validation checks for amounts and remainder values.</span></span> <span data-ttu-id="d4152-109">如果要与具有不同要求的外部工资系统集成，此功能非常有用。</span><span class="sxs-lookup"><span data-stu-id="d4152-109">This feature is helpful if you're integrating with an external payroll system that has different requirements.</span></span>

## <a name="manager-self-service---add-goals-for-team-members-through-the-team-performance-goals-tile"></a><span data-ttu-id="d4152-110">经理自助服务 - 通过“团队绩效目标”磁贴为团队成员添加目标</span><span class="sxs-lookup"><span data-stu-id="d4152-110">Manager self-service - Add goals for team members through the Team performance goals tile</span></span>

<span data-ttu-id="d4152-111">在此版本之前，经理可通过与各员工关联的绩效目标分别向员工添加目标。</span><span class="sxs-lookup"><span data-stu-id="d4152-111">Prior to this release, managers can add goals to their employees individually through the performance goals associated to each employee.</span></span> <span data-ttu-id="d4152-112">通过此更新，经理可访问**团队绩效目标**磁贴并通过选择直接报告新建目标。</span><span class="sxs-lookup"><span data-stu-id="d4152-112">With this update, managers can access the **Team performance goals** tile and create new goals by selecting any of their direct reports.</span></span>

## <a name="manager-self-service---add-reviews-for-team-members-through-the-team-performance-reviews-tile"></a><span data-ttu-id="d4152-113">经理自助服务 - 通过“团队绩效审核”磁贴为团队成员添加审核</span><span class="sxs-lookup"><span data-stu-id="d4152-113">Manager self-service - Add reviews for team members through the Team performance reviews tile</span></span>

<span data-ttu-id="d4152-114">在此版本之前，经理可通过与各员工关联的审核分别向员工添加审核。</span><span class="sxs-lookup"><span data-stu-id="d4152-114">Prior to this release, managers can add reviews to their employees individually through the reviews associated to each employee.</span></span> <span data-ttu-id="d4152-115">通过此更新，经理可访问**团队绩效审核**磁贴并通过选择直接报告新建审核。</span><span class="sxs-lookup"><span data-stu-id="d4152-115">With this update, managers can access the **Team performance reviews** tile and create new reviews by selecting any of their direct reports.</span></span>

## <a name="configure-proration-options-by-leave-plan"></a><span data-ttu-id="d4152-116">根据离职计划配置按比例分配选项</span><span class="sxs-lookup"><span data-stu-id="d4152-116">Configure proration options by leave plan</span></span>

<span data-ttu-id="d4152-117">组织根据员工加入和离开公司的时间以不同的方式奖励休假。</span><span class="sxs-lookup"><span data-stu-id="d4152-117">Organizations award time off differently based on when employees join and leave the company.</span></span> <span data-ttu-id="d4152-118">某些组织的员工从加入公司时即开始全额享受奖励，而其他组织的员工则按比例享受奖励。</span><span class="sxs-lookup"><span data-stu-id="d4152-118">For some organizations, employees are awarded their full allocation on their start date while others prorate the award.</span></span> <span data-ttu-id="d4152-119">此版本中提供了新选项，用于选择如何为加入组织的人员和离开组织的人员按比例分配奖励和进行累积。</span><span class="sxs-lookup"><span data-stu-id="d4152-119">New options are provided in this release to choose how to prorate the awards and accruals for joiners and leavers in an organization.</span></span> <span data-ttu-id="d4152-120">选项包括：“按比例分配”、“完全累积”和“不累积”。</span><span class="sxs-lookup"><span data-stu-id="d4152-120">Options include: Prorated, Full accrual, and No accrual.</span></span>

## <a name="other-changes"></a><span data-ttu-id="d4152-121">其他更改</span><span class="sxs-lookup"><span data-stu-id="d4152-121">Other changes</span></span>

-   <span data-ttu-id="d4152-122">员工实体更新 - 现在可使用 Excel 加载项/数据管理更新**人员**磁贴。</span><span class="sxs-lookup"><span data-stu-id="d4152-122">Employee entity updated - The **Personal** title can now be updated using the Excel add-in/data management.</span></span>

-   <span data-ttu-id="d4152-123">安全更改中允许删除员工自助服务中有关付款信息的**删除**和**停用**按钮。</span><span class="sxs-lookup"><span data-stu-id="d4152-123">Security change to allow removal of the **Delete** and **Deactivate** buttons in employee self-service for payment information.</span></span>

## <a name="known-issue"></a><span data-ttu-id="d4152-124">已知问题</span><span class="sxs-lookup"><span data-stu-id="d4152-124">Known issue</span></span>

-   <span data-ttu-id="d4152-125">**问题：** 向工作人员添加新附件时，**新建**和**编辑**按钮灰显。**解决方法：** 打开附件页面之前，确保已关闭**工作人员**页面中的速见表。</span><span class="sxs-lookup"><span data-stu-id="d4152-125">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="d4152-126">如果加载**工作人员**页面时速见表已关闭，将启用**附件**按钮。</span><span class="sxs-lookup"><span data-stu-id="d4152-126">If the FactBoxes are closed when the **Worker** page is loaded, the **Attachments** buttons will be enabled.</span></span> <span data-ttu-id="d4152-127">（下一个平台更新中将解决这个问题。）</span><span class="sxs-lookup"><span data-stu-id="d4152-127">(This issue will be fixed in the next platform update.)</span></span>
