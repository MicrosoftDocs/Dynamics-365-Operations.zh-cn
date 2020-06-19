---
title: 设置付款频率
description: Microsoft Dynamics 365 Human Resources 使用付款频率来计算年度福利薪金，确定员工在每个付款期间支付的福利金金额，以及提供商的付款频率。
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a5d562b64a161891bf34b0dfa94fbf68325e21b5
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429949"
---
# <a name="set-up-payment-frequencies"></a><span data-ttu-id="5063f-103">设置付款频率</span><span class="sxs-lookup"><span data-stu-id="5063f-103">Set up payment frequencies</span></span>

<span data-ttu-id="5063f-104">Microsoft Dynamics 365 Human Resources 使用付款频率来计算年度福利薪金，确定员工在每个付款期间支付的福利金金额，以及提供商的付款频率。</span><span class="sxs-lookup"><span data-stu-id="5063f-104">Microsoft Dynamics 365 Human Resources uses payment frequencies to calculate the annual benefit salary, determine the benefit premium amount an employee pays each pay period, and how often providers are paid.</span></span>

<span data-ttu-id="5063f-105">福利付款频率使用换算系数转换每月、每半月、每两周、每周和每天付款频率之间的福利付款期间。</span><span class="sxs-lookup"><span data-stu-id="5063f-105">Benefit payment frequencies use conversion factors to convert benefit payment periods between monthly, semi-monthly, biweekly, weekly, and daily payment frequencies.</span></span> <span data-ttu-id="5063f-106">这使公司可以定义福利计划中付款频率之间的相关性。</span><span class="sxs-lookup"><span data-stu-id="5063f-106">This allows companies to define the interdependence between the payment frequencies within a benefit plan.</span></span>

<span data-ttu-id="5063f-107">换算系数字段标识从付款频率到标准付款期间的换算系数，允许系统在付款频率之间进行计算。</span><span class="sxs-lookup"><span data-stu-id="5063f-107">The conversion factors fields identify the conversion factor from the payment frequency to the standard payment periods and allow the system to do calculations between payment frequencies.</span></span> <span data-ttu-id="5063f-108">换算系数金额还确定员工按每个支付频率应该支付的福利金金额。</span><span class="sxs-lookup"><span data-stu-id="5063f-108">The conversion factor amount also determines the benefit premium amount that an employee should pay each pay frequency.</span></span>

1. <span data-ttu-id="5063f-109">在**福利管理**工作区中，在**设置**下，选择**付款频率**。</span><span class="sxs-lookup"><span data-stu-id="5063f-109">In the **Benefits management** workspace, under **Setup**, select **Payment frequencies**.</span></span>

2. <span data-ttu-id="5063f-110">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="5063f-110">Select **New**.</span></span>

3. <span data-ttu-id="5063f-111">为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="5063f-111">Specify values for the following fields:</span></span>

   | <span data-ttu-id="5063f-112">字段</span><span class="sxs-lookup"><span data-stu-id="5063f-112">Field</span></span> | <span data-ttu-id="5063f-113">说明</span><span class="sxs-lookup"><span data-stu-id="5063f-113">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="5063f-114">**付款频率**</span><span class="sxs-lookup"><span data-stu-id="5063f-114">**Payment frequency**</span></span> | <span data-ttu-id="5063f-115">唯一的付款频率名称。</span><span class="sxs-lookup"><span data-stu-id="5063f-115">A unique payment frequency name.</span></span> |
   | <span data-ttu-id="5063f-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="5063f-116">**Description**</span></span> | <span data-ttu-id="5063f-117">付款频率的描述。</span><span class="sxs-lookup"><span data-stu-id="5063f-117">A description of the payment frequency.</span></span> |
   | <span data-ttu-id="5063f-118">**期间余额**</span><span class="sxs-lookup"><span data-stu-id="5063f-118">**Period**</span></span> | <span data-ttu-id="5063f-119">与福利提供商和员工付款频率最匹配的合适的期间。</span><span class="sxs-lookup"><span data-stu-id="5063f-119">The appropriate period that best matches the benefit provider’s and employee’s payment frequency.</span></span> <span data-ttu-id="5063f-120">期间列表包含标准付款期间。</span><span class="sxs-lookup"><span data-stu-id="5063f-120">The period list is composed of the standard payment periods.</span></span> |
   | <span data-ttu-id="5063f-121">**付薪期间数**</span><span class="sxs-lookup"><span data-stu-id="5063f-121">**Number of pay periods**</span></span> | <span data-ttu-id="5063f-122">代表福利提供商或员工的支付频率的支付期间数。</span><span class="sxs-lookup"><span data-stu-id="5063f-122">The number of pay periods that represents how often the benefit provider or employees are paid.</span></span> <span data-ttu-id="5063f-123">此数字将用于计算员工的年度福利薪金金额。</span><span class="sxs-lookup"><span data-stu-id="5063f-123">This amount will be used to calculate the employee‘s annual benefit salary amount.</span></span> |
   | <span data-ttu-id="5063f-124">**年度换算系数**</span><span class="sxs-lookup"><span data-stu-id="5063f-124">**Annual conversion factor**</span></span> | <span data-ttu-id="5063f-125">付款频率的年度换算系数。</span><span class="sxs-lookup"><span data-stu-id="5063f-125">The annual conversion factor for the payment frequency.</span></span> <span data-ttu-id="5063f-126">例如，每月支付频率的年度换算系数为：</span><span class="sxs-lookup"><span data-stu-id="5063f-126">For example, the annual conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="5063f-127">（12 次每月付款/1 年）= 12</span><span class="sxs-lookup"><span data-stu-id="5063f-127">(12 monthly payments / 1 year) = 12</span></span> |
   | <span data-ttu-id="5063f-128">**每半年换算系数**</span><span class="sxs-lookup"><span data-stu-id="5063f-128">**Semiannual conversion factor**</span></span> | <span data-ttu-id="5063f-129">付款频率的半年换算系数。</span><span class="sxs-lookup"><span data-stu-id="5063f-129">The semiannual conversion factor for the payment frequency.</span></span> <span data-ttu-id="5063f-130">例如，每月支付频率的半年换算系数为：</span><span class="sxs-lookup"><span data-stu-id="5063f-130">For example, the semiannual conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="5063f-131">（12 次每月付款/一年 2 次）= 6</span><span class="sxs-lookup"><span data-stu-id="5063f-131">(12 monthly payments / 2 times a year) = 6</span></span> |
   | <span data-ttu-id="5063f-132">**季度换算系数**</span><span class="sxs-lookup"><span data-stu-id="5063f-132">**Quarterly conversion factor**</span></span> | <span data-ttu-id="5063f-133">付款频率的季度换算系数。</span><span class="sxs-lookup"><span data-stu-id="5063f-133">The quarterly conversion factor for the payment frequency.</span></span> <span data-ttu-id="5063f-134">例如，每月支付频率的季度换算系数为：</span><span class="sxs-lookup"><span data-stu-id="5063f-134">For example, the quarterly conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="5063f-135">（12 次每月付款/4 个季度）= 3</span><span class="sxs-lookup"><span data-stu-id="5063f-135">(12 monthly payments / 4 quarters) = 3</span></span> |
   | <span data-ttu-id="5063f-136">**每月换算系数**</span><span class="sxs-lookup"><span data-stu-id="5063f-136">**Monthly conversion factor**</span></span> | <span data-ttu-id="5063f-137">付款频率的每月换算系数。</span><span class="sxs-lookup"><span data-stu-id="5063f-137">The monthly conversion factor for the payment frequency.</span></span> <span data-ttu-id="5063f-138">例如，每月支付频率的每月换算系数为：</span><span class="sxs-lookup"><span data-stu-id="5063f-138">For example, the monthly conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="5063f-139">（12 次每月付款/12 个月）= 1</span><span class="sxs-lookup"><span data-stu-id="5063f-139">(12 monthly payments / 12 months) = 1</span></span> |
   | <span data-ttu-id="5063f-140">**每半月换算系数**</span><span class="sxs-lookup"><span data-stu-id="5063f-140">**Semimonthly conversion factor**</span></span> | <span data-ttu-id="5063f-141">付款频率的每半月换算系数。</span><span class="sxs-lookup"><span data-stu-id="5063f-141">The semimonthly conversion factor for the payment frequency.</span></span> <span data-ttu-id="5063f-142">例如，每月支付频率的每半月换算系数为：</span><span class="sxs-lookup"><span data-stu-id="5063f-142">For example, the semimonthly conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="5063f-143">(12 次每月付款/ 24(每月 2 次))= 0.5</span><span class="sxs-lookup"><span data-stu-id="5063f-143">(12 monthly payments / 24 (2x a month)) = 0.5</span></span> | 
   | <span data-ttu-id="5063f-144">**每两周换算系数**</span><span class="sxs-lookup"><span data-stu-id="5063f-144">**Biweekly conversion factor**</span></span> | <span data-ttu-id="5063f-145">付款频率的年度换算系数。</span><span class="sxs-lookup"><span data-stu-id="5063f-145">The annual conversion factor for the payment frequency.</span></span> <span data-ttu-id="5063f-146">例如，每月支付频率的年度换算系数为：</span><span class="sxs-lookup"><span data-stu-id="5063f-146">For example, the annual conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="5063f-147">（12 次每月付款/26 周）= 0.461538</span><span class="sxs-lookup"><span data-stu-id="5063f-147">(12 monthly payments / 26 weeks) = 0.461538</span></span> |
   | <span data-ttu-id="5063f-148">**每周换算系数**</span><span class="sxs-lookup"><span data-stu-id="5063f-148">**Weekly conversion factor**</span></span> | <span data-ttu-id="5063f-149">付款频率的年度换算系数。</span><span class="sxs-lookup"><span data-stu-id="5063f-149">The annual conversion factor for the payment frequency.</span></span> <span data-ttu-id="5063f-150">例如，每月支付频率的年度换算系数为：</span><span class="sxs-lookup"><span data-stu-id="5063f-150">For example, the annual conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="5063f-151">（12 次每月付款/52 周）= 0.230769</span><span class="sxs-lookup"><span data-stu-id="5063f-151">(12 monthly payments / 52 weeks) = 0.230769</span></span> |
   | <span data-ttu-id="5063f-152">**每日换算系数**</span><span class="sxs-lookup"><span data-stu-id="5063f-152">**Daily conversion factor**</span></span> | <span data-ttu-id="5063f-153">付款频率的年度换算系数。</span><span class="sxs-lookup"><span data-stu-id="5063f-153">The annual conversion factor for the payment frequency.</span></span> <span data-ttu-id="5063f-154">例如，每月支付频率的年度换算系数为：</span><span class="sxs-lookup"><span data-stu-id="5063f-154">For example, the annual conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="5063f-155">（12 次每月付款/365 天）= 0.032877</span><span class="sxs-lookup"><span data-stu-id="5063f-155">(12 monthly payments / 365 days) = 0.032877</span></span> |
   | <span data-ttu-id="5063f-156">**每小时换算系数**</span><span class="sxs-lookup"><span data-stu-id="5063f-156">**Hourly conversion factor**</span></span> | <span data-ttu-id="5063f-157">付款频率的年度换算系数。</span><span class="sxs-lookup"><span data-stu-id="5063f-157">The annual conversion factor for the payment frequency.</span></span> <span data-ttu-id="5063f-158">例如，每月支付频率的年度换算系数为：</span><span class="sxs-lookup"><span data-stu-id="5063f-158">For example, the annual conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="5063f-159">（12 次每月付款/2080 小时）= 0.005769</span><span class="sxs-lookup"><span data-stu-id="5063f-159">(12 monthly payments / 2080 hours) = 0.005769</span></span>

4. <span data-ttu-id="5063f-160">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="5063f-160">Select **Save**.</span></span> 
