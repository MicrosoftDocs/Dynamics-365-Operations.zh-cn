---
title: 启用考勤管理的工资流程
description: 此程序说明如何根据工时与出勤率来生成工资。
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgPayTable, JmgPayRate, JmgPayAgreementTable, JmgPayAgreementLine, HcmWorker
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72b925feb8f784c257656dd93b48c9c0cc66da5e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5214906"
---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a><span data-ttu-id="3324e-103">启用考勤管理的工资流程</span><span class="sxs-lookup"><span data-stu-id="3324e-103">Enable the payroll process for time and attendance</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3324e-104">此程序说明如何根据工时与出勤率来生成工资。</span><span class="sxs-lookup"><span data-stu-id="3324e-104">This procedure shows how to enable the payroll process for time and attendance.</span></span> <span data-ttu-id="3324e-105">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="3324e-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-pay-type-with-a-related-pay-rate"></a><span data-ttu-id="3324e-106">创建一个具有相关付薪比率的支付类型</span><span class="sxs-lookup"><span data-stu-id="3324e-106">Create a pay type with a related pay rate</span></span>
1. <span data-ttu-id="3324e-107">“工时与出勤率”>“设置”>“工资单”>“支付类型”</span><span class="sxs-lookup"><span data-stu-id="3324e-107">Time and attendance > Setup > Payroll > Pay types</span></span>
2. <span data-ttu-id="3324e-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="3324e-108">Click New.</span></span>
3. <span data-ttu-id="3324e-109">在“支付类型”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="3324e-109">In the Pay type field, type a value.</span></span>
4. <span data-ttu-id="3324e-110">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="3324e-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="3324e-111">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="3324e-111">Click Save.</span></span>
6. <span data-ttu-id="3324e-112">单击“利率”。</span><span class="sxs-lookup"><span data-stu-id="3324e-112">Click Rates.</span></span>
    * <span data-ttu-id="3324e-113">利率支付的类型根据具体的时间间隔设置，个人利率是为员工创建的。</span><span class="sxs-lookup"><span data-stu-id="3324e-113">Rates for pay types are set up for specific time intervals, and individual rates can be created for workers.</span></span> <span data-ttu-id="3324e-114">通常没有必要根据工时与出勤率创建支付利率类型。</span><span class="sxs-lookup"><span data-stu-id="3324e-114">It is not always necessary to create rates for pay types in time and attendance.</span></span> <span data-ttu-id="3324e-115">此信息可能已存于劳资管理系统，用于生成工资。</span><span class="sxs-lookup"><span data-stu-id="3324e-115">This information may already exist in the payroll system that is used to generate wages.</span></span>  
7. <span data-ttu-id="3324e-116">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="3324e-116">Click New.</span></span>
8. <span data-ttu-id="3324e-117">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="3324e-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="3324e-118">在“利率”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="3324e-118">In the Rate field, enter a number.</span></span>
10. <span data-ttu-id="3324e-119">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="3324e-119">Click Save.</span></span>

## <a name="create-a-pay-agreement"></a><span data-ttu-id="3324e-120">创建付薪协议</span><span class="sxs-lookup"><span data-stu-id="3324e-120">Create a pay agreement</span></span>
1. <span data-ttu-id="3324e-121">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="3324e-121">Close the page.</span></span>
2. <span data-ttu-id="3324e-122">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="3324e-122">Close the page.</span></span>
3. <span data-ttu-id="3324e-123">转到“支付协议”。</span><span class="sxs-lookup"><span data-stu-id="3324e-123">Go to Pay agreements.</span></span>
    * <span data-ttu-id="3324e-124">“工时与出勤率”>“设置”>“付薪协议”</span><span class="sxs-lookup"><span data-stu-id="3324e-124">Time and attendance > Setup > Pay agreements</span></span>  
4. <span data-ttu-id="3324e-125">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="3324e-125">Click New.</span></span>
5. <span data-ttu-id="3324e-126">在“支付协议”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="3324e-126">In the Pay agreement field, type a value.</span></span>
6. <span data-ttu-id="3324e-127">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="3324e-127">In the Description field, type a value.</span></span>
7. <span data-ttu-id="3324e-128">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="3324e-128">Click Save.</span></span>
8. <span data-ttu-id="3324e-129">单击“协议”。</span><span class="sxs-lookup"><span data-stu-id="3324e-129">Click Agreement lines.</span></span>
9. <span data-ttu-id="3324e-130">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="3324e-130">Click New.</span></span>
10. <span data-ttu-id="3324e-131">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="3324e-131">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="3324e-132">在“档案类型”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="3324e-132">In the Profile type field, enter or select a value.</span></span>
12. <span data-ttu-id="3324e-133">在“支付类型”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="3324e-133">In the Pay type field, enter or select a value.</span></span>

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a><span data-ttu-id="3324e-134">设置时间登记工作员工的支付协议</span><span class="sxs-lookup"><span data-stu-id="3324e-134">Set up pay agreement for time and registration worker</span></span>
1. <span data-ttu-id="3324e-135">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="3324e-135">Close the page.</span></span>
2. <span data-ttu-id="3324e-136">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="3324e-136">Close the page.</span></span>
3. <span data-ttu-id="3324e-137">转到“时间登记工作员工”。</span><span class="sxs-lookup"><span data-stu-id="3324e-137">Go to Time registration workers.</span></span>
    * <span data-ttu-id="3324e-138">“工时与出勤率”>“设置”>“时间登记工作人员”</span><span class="sxs-lookup"><span data-stu-id="3324e-138">Time and attendance > Setup > Time registration workers</span></span>  
4. <span data-ttu-id="3324e-139">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="3324e-139">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="3324e-140">单击“雇用”选项卡。</span><span class="sxs-lookup"><span data-stu-id="3324e-140">Click the Employment tab.</span></span>
6. <span data-ttu-id="3324e-141">展开“时间登记”部分。</span><span class="sxs-lookup"><span data-stu-id="3324e-141">Expand the Time registration section.</span></span>
7. <span data-ttu-id="3324e-142">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="3324e-142">Click Edit.</span></span>
8. <span data-ttu-id="3324e-143">在“支付协议”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="3324e-143">In the Pay agreement field, enter or select a value.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]