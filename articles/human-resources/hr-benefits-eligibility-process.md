---
title: 福利资格处理
description: 该过程显示了福利资格流程的工作原理。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 57e3e1dde4b4c8038b151dabf17af0f911f2ba07
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008243"
---
# <a name="benefit-eligibility-process"></a><span data-ttu-id="151b8-103">福利资格处理</span><span class="sxs-lookup"><span data-stu-id="151b8-103">Benefit eligibility process</span></span>

<span data-ttu-id="151b8-104">该过程显示了福利资格流程的工作原理。</span><span class="sxs-lookup"><span data-stu-id="151b8-104">This procedure shows how the benefit eligibility process works.</span></span> <span data-ttu-id="151b8-105">完成该流程后，您可以查看结果。</span><span class="sxs-lookup"><span data-stu-id="151b8-105">When the process is complete you can view the results.</span></span> <span data-ttu-id="151b8-106">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="151b8-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="151b8-107">转到“人力资源”>“福利”>“福利”。</span><span class="sxs-lookup"><span data-stu-id="151b8-107">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="151b8-108">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="151b8-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="151b8-109">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="151b8-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="151b8-110">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="151b8-110">Click Edit.</span></span>
5. <span data-ttu-id="151b8-111">在“资格”字段中，选择“基于规则”。</span><span class="sxs-lookup"><span data-stu-id="151b8-111">In the Eligibility field, select 'Rule based'.</span></span>
6. <span data-ttu-id="151b8-112">在“规则类型”字段中，选择希望适用于该福利的福利政策规则。</span><span class="sxs-lookup"><span data-stu-id="151b8-112">In the Rule type field, select the benefit policy rule you would like applied to the benefit.</span></span>
7. <span data-ttu-id="151b8-113">在操作窗格上，单击“福利”。</span><span class="sxs-lookup"><span data-stu-id="151b8-113">On the Action Pane, click Benefit.</span></span>
8. <span data-ttu-id="151b8-114">单击“创建资格事件”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="151b8-114">Click Create eligibility event to open the drop dialog.</span></span>
9. <span data-ttu-id="151b8-115">在“事件”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="151b8-115">In the Event field, type a value.</span></span>
10. <span data-ttu-id="151b8-116">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="151b8-116">In the Description field, type a value.</span></span>
11. <span data-ttu-id="151b8-117">在“事件类型”字段中，选择“打开登记”。</span><span class="sxs-lookup"><span data-stu-id="151b8-117">In the Event type field, select 'Open enrollment'.</span></span>
12. <span data-ttu-id="151b8-118">在“覆盖范围开始日期”字段中，输入一个日期和时间。</span><span class="sxs-lookup"><span data-stu-id="151b8-118">In the Coverage start date field, enter a date and time.</span></span>
13. <span data-ttu-id="151b8-119">在“登记周期开始日期”字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="151b8-119">In the Enrollment period start date field, enter a date and time.</span></span>
14. <span data-ttu-id="151b8-120">在“登记天数”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="151b8-120">In the Days to enroll field, enter a number.</span></span>
15. <span data-ttu-id="151b8-121">单击“创建事件”。</span><span class="sxs-lookup"><span data-stu-id="151b8-121">Click Create event.</span></span>
16. <span data-ttu-id="151b8-122">单击“添加到工作人员”快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="151b8-122">Click Add in the Workers FastTab.</span></span>
17. <span data-ttu-id="151b8-123">在“根据类型显示”字段中，选择“员工”。</span><span class="sxs-lookup"><span data-stu-id="151b8-123">In the Show by type field, select 'Employees'.</span></span>
18. <span data-ttu-id="151b8-124">在“根据法人显示”字段中，选择“当前法人”。</span><span class="sxs-lookup"><span data-stu-id="151b8-124">In the Show by legal entity field, select 'Current legal entity'.</span></span>
19. <span data-ttu-id="151b8-125">在列表中，标记或取消标记所有行。</span><span class="sxs-lookup"><span data-stu-id="151b8-125">In the list, mark or unmark all rows.</span></span>
20. <span data-ttu-id="151b8-126">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="151b8-126">Click OK.</span></span>
21. <span data-ttu-id="151b8-127">单击“流程”。</span><span class="sxs-lookup"><span data-stu-id="151b8-127">Click Process.</span></span>
22. <span data-ttu-id="151b8-128">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="151b8-128">Click OK.</span></span>
23. <span data-ttu-id="151b8-129">刷新该页面。</span><span class="sxs-lookup"><span data-stu-id="151b8-129">Refresh the page.</span></span>
24. <span data-ttu-id="151b8-130">单击“显示结果”。</span><span class="sxs-lookup"><span data-stu-id="151b8-130">Click Show results.</span></span>
25. <span data-ttu-id="151b8-131">打开“状态栏筛选器“。</span><span class="sxs-lookup"><span data-stu-id="151b8-131">Open Status column filter.</span></span>
26. <span data-ttu-id="151b8-132">从 A 到 Z 进行排序</span><span class="sxs-lookup"><span data-stu-id="151b8-132">Sort A to Z</span></span>
