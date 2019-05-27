---
title: 启用考勤管理的工资流程
description: 此程序说明如何根据工时与出勤率来生成工资。
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgPayTable, JmgPayRate, JmgPayAgreementTable, JmgPayAgreementLine, HcmWorker
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0174f438396d814d153befe4a59a79b6eebb2288
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560174"
---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a><span data-ttu-id="18cf7-103">启用考勤管理的工资流程</span><span class="sxs-lookup"><span data-stu-id="18cf7-103">Enable the payroll process for time and attendance</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="18cf7-104">此程序说明如何根据工时与出勤率来生成工资。</span><span class="sxs-lookup"><span data-stu-id="18cf7-104">This procedure shows how to enable the payroll process for time and attendance.</span></span> <span data-ttu-id="18cf7-105">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="18cf7-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-pay-type-with-a-related-pay-rate"></a><span data-ttu-id="18cf7-106">创建一个具有相关付薪比率的支付类型</span><span class="sxs-lookup"><span data-stu-id="18cf7-106">Create a pay type with a related pay rate</span></span>
1. <span data-ttu-id="18cf7-107">“工时与出勤率”>“设置”>“工资单”>“支付类型”</span><span class="sxs-lookup"><span data-stu-id="18cf7-107">Time and attendance > Setup > Payroll > Pay types</span></span>
2. <span data-ttu-id="18cf7-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="18cf7-108">Click New.</span></span>
3. <span data-ttu-id="18cf7-109">在“支付类型”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="18cf7-109">In the Pay type field, type a value.</span></span>
4. <span data-ttu-id="18cf7-110">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="18cf7-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="18cf7-111">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="18cf7-111">Click Save.</span></span>
6. <span data-ttu-id="18cf7-112">单击“利率”。</span><span class="sxs-lookup"><span data-stu-id="18cf7-112">Click Rates.</span></span>
    * <span data-ttu-id="18cf7-113">利率支付的类型根据具体的时间间隔设置，个人利率是为员工创建的。</span><span class="sxs-lookup"><span data-stu-id="18cf7-113">Rates for pay types are set up for specific time intervals, and individual rates can be created for workers.</span></span> <span data-ttu-id="18cf7-114">通常没有必要根据工时与出勤率创建支付利率类型。</span><span class="sxs-lookup"><span data-stu-id="18cf7-114">It is not always necessary to create rates for pay types in time and attendance.</span></span> <span data-ttu-id="18cf7-115">此信息可能已存于劳资管理系统，用于生成工资。</span><span class="sxs-lookup"><span data-stu-id="18cf7-115">This information may already exist in the payroll system that is used to generate wages.</span></span>  
7. <span data-ttu-id="18cf7-116">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="18cf7-116">Click New.</span></span>
8. <span data-ttu-id="18cf7-117">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="18cf7-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="18cf7-118">在“利率”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="18cf7-118">In the Rate field, enter a number.</span></span>
10. <span data-ttu-id="18cf7-119">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="18cf7-119">Click Save.</span></span>

## <a name="create-a-pay-agreement"></a><span data-ttu-id="18cf7-120">创建付薪协议</span><span class="sxs-lookup"><span data-stu-id="18cf7-120">Create a pay agreement</span></span>
1. <span data-ttu-id="18cf7-121">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="18cf7-121">Close the page.</span></span>
2. <span data-ttu-id="18cf7-122">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="18cf7-122">Close the page.</span></span>
3. <span data-ttu-id="18cf7-123">转到“支付协议”。</span><span class="sxs-lookup"><span data-stu-id="18cf7-123">Go to Pay agreements.</span></span>
    * <span data-ttu-id="18cf7-124">“工时与出勤率”>“设置”>“付薪协议”</span><span class="sxs-lookup"><span data-stu-id="18cf7-124">Time and attendance > Setup > Pay agreements</span></span>  
4. <span data-ttu-id="18cf7-125">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="18cf7-125">Click New.</span></span>
5. <span data-ttu-id="18cf7-126">在“支付协议”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="18cf7-126">In the Pay agreement field, type a value.</span></span>
6. <span data-ttu-id="18cf7-127">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="18cf7-127">In the Description field, type a value.</span></span>
7. <span data-ttu-id="18cf7-128">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="18cf7-128">Click Save.</span></span>
8. <span data-ttu-id="18cf7-129">单击“协议”。</span><span class="sxs-lookup"><span data-stu-id="18cf7-129">Click Agreement lines.</span></span>
9. <span data-ttu-id="18cf7-130">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="18cf7-130">Click New.</span></span>
10. <span data-ttu-id="18cf7-131">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="18cf7-131">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="18cf7-132">在“档案类型”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="18cf7-132">In the Profile type field, enter or select a value.</span></span>
12. <span data-ttu-id="18cf7-133">在“支付类型”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="18cf7-133">In the Pay type field, enter or select a value.</span></span>

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a><span data-ttu-id="18cf7-134">设置时间登记工作员工的支付协议</span><span class="sxs-lookup"><span data-stu-id="18cf7-134">Set up pay agreement for time and registration worker</span></span>
1. <span data-ttu-id="18cf7-135">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="18cf7-135">Close the page.</span></span>
2. <span data-ttu-id="18cf7-136">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="18cf7-136">Close the page.</span></span>
3. <span data-ttu-id="18cf7-137">转到“时间登记工作员工”。</span><span class="sxs-lookup"><span data-stu-id="18cf7-137">Go to Time registration workers.</span></span>
    * <span data-ttu-id="18cf7-138">“工时与出勤率”>“设置”>“时间登记工作人员”</span><span class="sxs-lookup"><span data-stu-id="18cf7-138">Time and attendance > Setup > Time registration workers</span></span>  
4. <span data-ttu-id="18cf7-139">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="18cf7-139">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="18cf7-140">单击“雇用”选项卡。</span><span class="sxs-lookup"><span data-stu-id="18cf7-140">Click the Employment tab.</span></span>
6. <span data-ttu-id="18cf7-141">展开“时间登记”部分。</span><span class="sxs-lookup"><span data-stu-id="18cf7-141">Expand the Time registration section.</span></span>
7. <span data-ttu-id="18cf7-142">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="18cf7-142">Click Edit.</span></span>
8. <span data-ttu-id="18cf7-143">在“支付协议”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="18cf7-143">In the Pay agreement field, enter or select a value.</span></span>

