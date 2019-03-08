---
title: 在固定薪酬计划中登记员工
description: 薪酬福利经理可以指派不同雇员不同的固定薪酬计划以确定其各自的基本工资。
author: kherr75
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMCompFixedEmpl, HRMCompFixedEmplActionDialog, HcmPositionLookup, HRMCompRefPointLookup
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c9c11292feec06a53cd4426a25bfb2aaac7de3e8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "353325"
---
# <a name="enroll-an-employee-in-a-fixed-compensation-plan"></a><span data-ttu-id="2880c-103">在固定薪酬计划中登记员工</span><span class="sxs-lookup"><span data-stu-id="2880c-103">Enroll an employee in a fixed compensation plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2880c-104">薪酬福利经理可以指派不同雇员不同的固定薪酬计划以确定其各自的基本工资。</span><span class="sxs-lookup"><span data-stu-id="2880c-104">The compensation and benefits manager can assign employees to fixed compensation plans to manage their base pay.</span></span> <span data-ttu-id="2880c-105">此程序假设已经创建了一个有效的固定薪酬计划，且该计划的资格规定也已经设置完成。</span><span class="sxs-lookup"><span data-stu-id="2880c-105">This procedure assumes that a fixed plan has been created and is active, and that eligibility rules have been set for the plan.</span></span> <span data-ttu-id="2880c-106">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="2880c-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="2880c-107">启动该程序，请转到“人力资源”>“工作人员”>“雇员”>“薪酬”>“固定计划”</span><span class="sxs-lookup"><span data-stu-id="2880c-107">To begin the procedure, go to Human resources > Workers > Employees > Compensation > Fixed plan</span></span>

1. <span data-ttu-id="2880c-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="2880c-108">Click New.</span></span>
2. <span data-ttu-id="2880c-109">在“操作”字段中，选择一个“固定薪酬”操作类型“雇用 / 再雇用”，说明雇员薪酬的变化。</span><span class="sxs-lookup"><span data-stu-id="2880c-109">In the Action field, select a Fixed compensation action of type Hire/Rehire to describe the change in the employee's compensation.</span></span>
3. <span data-ttu-id="2880c-110">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="2880c-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="2880c-111">在“职位”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="2880c-111">In the Position field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="2880c-112">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="2880c-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="2880c-113">该标准是根据“工作职位”的“薪酬水平”呈现的。</span><span class="sxs-lookup"><span data-stu-id="2880c-113">The level that's displayed is from the Compensation Level of the Job on the Position.</span></span> <span data-ttu-id="2880c-114">该工作标准必须在付给雇员薪酬之前设置。</span><span class="sxs-lookup"><span data-stu-id="2880c-114">The level must be set on the Job before compensation can be assigned to the employee.</span></span>  
6. <span data-ttu-id="2880c-115">在“计划”字段中，为该雇员选择“固定薪酬计划”。</span><span class="sxs-lookup"><span data-stu-id="2880c-115">In the Plan field, select the fixed compensation plan for the employee.</span></span> <span data-ttu-id="2880c-116">“计划查找”仅显示经过筛选后固定薪酬计划符合“资格规定”的雇员。</span><span class="sxs-lookup"><span data-stu-id="2880c-116">The Plan lookup is filtered to show only the plans that the employee is eligible for based on the Eligibility rules.</span></span>
7. <span data-ttu-id="2880c-117">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="2880c-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2880c-118">薪酬“生效日期”与“截止日期”默认为指派工作人员职位的开始日期与结束日期。</span><span class="sxs-lookup"><span data-stu-id="2880c-118">The Effective and Expiration dates for the compensation default from the start and end dates for the worker's position assignment.</span></span> <span data-ttu-id="2880c-119">可以根据需要更改相关日期。</span><span class="sxs-lookup"><span data-stu-id="2880c-119">You can adjust these dates as needed.</span></span>  
    * <span data-ttu-id="2880c-120">如果该雇员的“固定薪酬计划”是一步计划，则选择包含相应工资标准的薪酬阶梯。</span><span class="sxs-lookup"><span data-stu-id="2880c-120">If the Fixed compensation plan is a step plan, select the step containing the correct pay rate for the employee.</span></span> <span data-ttu-id="2880c-121">如果该雇员的固定薪酬计划是根据等级或期间设置，输入其工资标准。</span><span class="sxs-lookup"><span data-stu-id="2880c-121">If the fixed compensation plan is a grade or a band plan, enter the pay rate for the employee.</span></span> <span data-ttu-id="2880c-122">该工资标准将验证该薪酬计划设置的可行性程度，以及该工作薪酬水平的最小和最大参考值。</span><span class="sxs-lookup"><span data-stu-id="2880c-122">The pay rate will be validated against the tolerance settings for the plan, and the minimum and maximum reference points for the job's compensation level.</span></span>  
8. <span data-ttu-id="2880c-123">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="2880c-123">Click OK.</span></span>

