---
title: 设置弹性信贷项目
description: 您可以在 Microsoft Dynamics 365 Human Resources 中使用弹性信贷项目来根据预先确定的弹性信贷数量为员工登记福利。
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitCreditPrograms, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1dba179e47f586d7fe689b4a021eb9003eb0d9fc
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051849"
---
# <a name="set-up-flex-credit-programs"></a><span data-ttu-id="9e238-103">设置弹性信贷项目</span><span class="sxs-lookup"><span data-stu-id="9e238-103">Set up flex credit programs</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="9e238-104">您可以在 Microsoft Dynamics 365 Human Resources 中使用弹性信贷项目来根据预先确定的弹性信贷数量为员工登记福利。</span><span class="sxs-lookup"><span data-stu-id="9e238-104">You can use flex credit programs in Microsoft Dynamics 365 Human Resources to enroll employees in benefits according to a predetermined number of flex credits.</span></span> <span data-ttu-id="9e238-105">员工可以选择如何分配其弹性信贷。</span><span class="sxs-lookup"><span data-stu-id="9e238-105">Employees can choose how to allocate their flex credits.</span></span> <span data-ttu-id="9e238-106">例如，如果员工在配偶的健康保险计划中受保，他们可能希望将原本用于健康保险的信贷额用于其他福利。</span><span class="sxs-lookup"><span data-stu-id="9e238-106">For example, if an employee is covered under their spouse’s health insurance plan, they may want to use the credits they would have otherwise used on health coverage toward other benefits.</span></span> 

1. <span data-ttu-id="9e238-107">在 **福利管理** 工作区中，在 **计划** 下，选择 **弹性信贷项目**。</span><span class="sxs-lookup"><span data-stu-id="9e238-107">In the **Benefits management** workspace, under **Plans**, select **Flex credit programs**.</span></span>

2. <span data-ttu-id="9e238-108">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="9e238-108">Select **New**.</span></span>

3. <span data-ttu-id="9e238-109">为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="9e238-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="9e238-110">字段</span><span class="sxs-lookup"><span data-stu-id="9e238-110">Field</span></span> | <span data-ttu-id="9e238-111">说明</span><span class="sxs-lookup"><span data-stu-id="9e238-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="9e238-112">**福利信贷 ID**</span><span class="sxs-lookup"><span data-stu-id="9e238-112">**Benefit credit ID**</span></span> | <span data-ttu-id="9e238-113">弹性信贷项目的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="9e238-113">The unique identifier of the flex credit program.</span></span> |
   | <span data-ttu-id="9e238-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="9e238-114">**Description**</span></span> | <span data-ttu-id="9e238-115">弹性信贷项目的描述。</span><span class="sxs-lookup"><span data-stu-id="9e238-115">A description of the flex credit program.</span></span> | 
   | <span data-ttu-id="9e238-116">**开始日期**</span><span class="sxs-lookup"><span data-stu-id="9e238-116">**From date**</span></span> | <span data-ttu-id="9e238-117">弹性信贷项目生效的日期。</span><span class="sxs-lookup"><span data-stu-id="9e238-117">The date the flex credit program becomes active.</span></span> |
   | <span data-ttu-id="9e238-118">**截止日期**</span><span class="sxs-lookup"><span data-stu-id="9e238-118">**To date**</span></span> | <span data-ttu-id="9e238-119">弹性信贷项目的结束日期。</span><span class="sxs-lookup"><span data-stu-id="9e238-119">The end date of the flex credit program.</span></span> <span data-ttu-id="9e238-120">您可以保留默认值 (12/31/2154) 来指示弹性信贷项目没有计划的到期时间。</span><span class="sxs-lookup"><span data-stu-id="9e238-120">You can leave the default value (12/31/2154) to indicate that the flex credit program doesn’t have a scheduled expiration.</span></span> |
   | <span data-ttu-id="9e238-121">**信贷值总计**</span><span class="sxs-lookup"><span data-stu-id="9e238-121">**Total credit value**</span></span> | <span data-ttu-id="9e238-122">每位员工必须为自己的福利使用的信贷数量。</span><span class="sxs-lookup"><span data-stu-id="9e238-122">The number of credits each employee will have to use for their benefits.</span></span> |
   | <span data-ttu-id="9e238-123">**按比例分配规则**</span><span class="sxs-lookup"><span data-stu-id="9e238-123">**Prorate rule**</span></span> | <span data-ttu-id="9e238-124">用于在弹性信贷期间的中间雇用员工时按比例分配弹性信贷的规则。</span><span class="sxs-lookup"><span data-stu-id="9e238-124">The rule to use for prorating flex credits when an employee is hired in the middle of the flex credit period.</span></span> </br></br><ul><li><span data-ttu-id="9e238-125">**无** – 如果员工在弹性信贷项目期间开始后被雇用，将不会获得弹性信贷。</span><span class="sxs-lookup"><span data-stu-id="9e238-125">**None** – The employee receives no flex credits if they are hired after the flex credit program period begins.</span></span></li><li><span data-ttu-id="9e238-126">**完整信贷** – 无论员工何时被雇用，员工都会获得全额的弹性信贷。</span><span class="sxs-lookup"><span data-stu-id="9e238-126">**Full credit** – The employee receives the full amount of flex credits, regardless of when they are hired.</span></span></li><li><span data-ttu-id="9e238-127">**按比例分配** – 员工将根据他们的开始日期获得按比例分配的弹性信贷额。</span><span class="sxs-lookup"><span data-stu-id="9e238-127">**Prorate** – The employee receives a prorated amount of flex credits based on their start date.</span></span></li></ul> |
   | <span data-ttu-id="9e238-128">**弹性信贷按比例分配公式**</span><span class="sxs-lookup"><span data-stu-id="9e238-128">**Flex credit prorate formula**</span></span> | <span data-ttu-id="9e238-129">用于为弹性信贷项目福利期间的中间雇用的员工按比例分配弹性信贷的规则。</span><span class="sxs-lookup"><span data-stu-id="9e238-129">The rule to use for prorating flex credits for employees who are hired in the middle of a benefit period for the flex credit program.</span></span> <span data-ttu-id="9e238-130">按比例分配基于雇用开始日期。</span><span class="sxs-lookup"><span data-stu-id="9e238-130">The proration is based on the employment start date.</span></span> <span data-ttu-id="9e238-131">仅当您在 **按比例分配规则** 字段中选择 **按比例分配** 时，才使用此字段。</span><span class="sxs-lookup"><span data-stu-id="9e238-131">This field is only used if you select **Prorate** in the **Prorate rule** field.</span></span> </br></br><ul><li><span data-ttu-id="9e238-132">**每日** – 按比例分配员工按天级别获得的弹性信贷数量。</span><span class="sxs-lookup"><span data-stu-id="9e238-132">**Daily** – Prorates the number of flex credits an employee receives to the day level.</span></span> <span data-ttu-id="9e238-133">弹性信贷的总数除以期间内的天数。</span><span class="sxs-lookup"><span data-stu-id="9e238-133">The total number of flex credits is divided by the number of days in the period.</span></span> <span data-ttu-id="9e238-134">例如，如果您的福利期间为 400 天，系统会将弹性信贷的总数除以 400，来计算员工每天收到的弹性信贷的数量。</span><span class="sxs-lookup"><span data-stu-id="9e238-134">For example, if your benefit period is 400 days, the system will divide the total number of flex credits by 400 to calculate the number of flex credits employees receive per day.</span></span></li><li><span data-ttu-id="9e238-135">**当前月份** – 按比例分配员工按月级别将获得的弹性信贷的数量，舍入到当前月份。</span><span class="sxs-lookup"><span data-stu-id="9e238-135">**Current month** – Prorates the number of flex credits an employee receives to the month level, rounded to the current month.</span></span> <span data-ttu-id="9e238-136">弹性信贷的总数除以期间内的月数。</span><span class="sxs-lookup"><span data-stu-id="9e238-136">The total number of flex credits is divided by the number of months in the period.</span></span> <span data-ttu-id="9e238-137">例如，如果您的福利期间为 15 个月，系统会将弹性信贷的总数除以 15，来计算员工每月收到的弹性信贷的数量。</span><span class="sxs-lookup"><span data-stu-id="9e238-137">For example, if your benefit period is 15 months, the system will divide the total number of flex credits by 15 to calculate the number of flex credits employees receive per month.</span></span></li><li><span data-ttu-id="9e238-138">**下月** – 按比例分配员工按月级别将获得的弹性信贷的数量，舍入到下一个月。</span><span class="sxs-lookup"><span data-stu-id="9e238-138">**Following month** – Prorates the number of flex credits an employee receives to the month level, rounded to the next month.</span></span> <span data-ttu-id="9e238-139">弹性信贷的总数除以期间内的月数。</span><span class="sxs-lookup"><span data-stu-id="9e238-139">The total number of flex credits is divided by the number of months in the period.</span></span> <span data-ttu-id="9e238-140">例如，如果您的福利期间为 15 个月，系统会将弹性信贷的总数除以 15，来计算员工每月收到的弹性信贷的数量。</span><span class="sxs-lookup"><span data-stu-id="9e238-140">For example, if your benefit period is 15 months, the system divides the total number of flex credits by 15 to calculate the number of flex credits employees receive per month.</span></span></li></ul> |
   


[!INCLUDE[footer-include](../includes/footer-banner.md)]