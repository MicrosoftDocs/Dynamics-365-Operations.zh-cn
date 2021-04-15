---
title: 在可变薪酬计划中登记员工
description: “薪酬福利经理”招聘可变薪酬计划的雇员，需要计算雇员的现金和非现金奖金。
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRMCompVarEnrollEmpl, HcmCompensationWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f31790dc9389eaed125f69e4039d06a8b28bcc8b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793721"
---
# <a name="enroll-an-employee-in-a-variable-compensation-plan"></a><span data-ttu-id="8bdf0-103">在可变薪酬计划中登记员工</span><span class="sxs-lookup"><span data-stu-id="8bdf0-103">Enroll an employee in a variable compensation plan</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="8bdf0-104">“薪酬福利经理”招聘可变薪酬计划的雇员，需要计算雇员的现金和非现金奖金。</span><span class="sxs-lookup"><span data-stu-id="8bdf0-104">The Compensation and Benefits manager can enroll employees in variable compensation plans to calculate cash and non-cash awards for employees.</span></span> <span data-ttu-id="8bdf0-105">此程序假设已经创建了一个可变薪酬计划，且该计划的资格规定也已经创建完成，在“招聘能力”字段中设置为“是”。</span><span class="sxs-lookup"><span data-stu-id="8bdf0-105">This procedure assumes that a variable compensation plan has been created with the Enable enrolment field set to Yes, and that eligibility rules have been created for that variable compensation plan.</span></span> <span data-ttu-id="8bdf0-106">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="8bdf0-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="8bdf0-107">启动该过程，请转到“人力资源”>“工作人员”>“雇员”>“薪酬”>“可变薪酬计划招聘”</span><span class="sxs-lookup"><span data-stu-id="8bdf0-107">To begin this procedure, go to Human resources > Workers > Employees > Compensation > Variable plan enrolment</span></span>

1. <span data-ttu-id="8bdf0-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="8bdf0-108">Click New.</span></span>
2. <span data-ttu-id="8bdf0-109">在“计划”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="8bdf0-109">In the Plan field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="8bdf0-110">计划查找筛选后，仅显示固定薪酬计划符合资格规定的雇员。</span><span class="sxs-lookup"><span data-stu-id="8bdf0-110">The plan lookup will be filtered to only show the variable compensation plans that the employee is eligible for based on the eligibility rules.</span></span>  
3. <span data-ttu-id="8bdf0-111">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="8bdf0-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="8bdf0-112">切换“概况”部分的扩展。</span><span class="sxs-lookup"><span data-stu-id="8bdf0-112">Toggle the expansion of the General section.</span></span>
5. <span data-ttu-id="8bdf0-113">在“有效日期”字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="8bdf0-113">In the Effective date field, enter a date.</span></span>
6. <span data-ttu-id="8bdf0-114">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="8bdf0-114">Click Save.</span></span>
7. <span data-ttu-id="8bdf0-115">切换“覆盖”部分的扩展。</span><span class="sxs-lookup"><span data-stu-id="8bdf0-115">Toggle the expansion of the Overrides section.</span></span>
    * <span data-ttu-id="8bdf0-116">或者，如果雇用规则详细说明了“百分比”选择性的可变薪酬计划，设置一个雇用规定日期覆盖雇用日期。</span><span class="sxs-lookup"><span data-stu-id="8bdf0-116">Optionally, a hire rule date can be set to override the hire date for an employee when the hire rule specified for the selected variable plan is Percent.</span></span>  
    * <span data-ttu-id="8bdf0-117">如果该雇员的可变薪酬计划是一个百分比基数计划，则可以用奖金百分比覆盖。</span><span class="sxs-lookup"><span data-stu-id="8bdf0-117">If the variable plan is a percent of basis plan, the award percentage can be overridden for the employee.</span></span> <span data-ttu-id="8bdf0-118">如果该雇员的可变薪酬计划是由多个单元组成的计划，可以用单元薪酬的数目覆盖。</span><span class="sxs-lookup"><span data-stu-id="8bdf0-118">If the variable compensation plan is a number of units plan, the number of units can be overridden for the employee.</span></span>  
    * <span data-ttu-id="8bdf0-119">如果该雇员获得了一笔统一金额的奖金，该奖金数目可以在此设置。</span><span class="sxs-lookup"><span data-stu-id="8bdf0-119">If the employee should be given a flat amount for their award, the amount can be set here.</span></span>  
8. <span data-ttu-id="8bdf0-120">切换“组织覆盖”部分的扩展。</span><span class="sxs-lookup"><span data-stu-id="8bdf0-120">Toggle the expansion of the Organizational overrides section.</span></span>
    * <span data-ttu-id="8bdf0-121">如果需要考虑该雇员的绩效，不同部门的绩效或者同一个部门但是非其指派职位的绩效，可以用部门绩效覆盖。</span><span class="sxs-lookup"><span data-stu-id="8bdf0-121">If the employee's performance should take into consideration, the performance of different departments, or a department other than the one assigned on the employee's position, the department can be overridden.</span></span> <span data-ttu-id="8bdf0-122">“百分比”栏总分为 100 。</span><span class="sxs-lookup"><span data-stu-id="8bdf0-122">The Percent column should total 100.</span></span>  



[!INCLUDE[footer-include](../includes/footer-banner.md)]