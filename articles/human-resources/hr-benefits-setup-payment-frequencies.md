---
title: 设置付款频率
description: Microsoft Dynamics 365 Human Resources 使用付款频率来计算年度福利薪金，确定员工在每个付款期间支付的福利金金额，以及提供商的付款频率。
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: f5a2ad19d9f9f3a6afa2574d9fdb8841c70d6e6e
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111657"
---
# <a name="set-up-payment-frequencies"></a><span data-ttu-id="b6466-103">设置付款频率</span><span class="sxs-lookup"><span data-stu-id="b6466-103">Set up payment frequencies</span></span>

<span data-ttu-id="b6466-104">Microsoft Dynamics 365 Human Resources 使用付款频率来计算年度福利薪金，确定员工在每个付款期间支付的福利金金额，以及提供商的付款频率。</span><span class="sxs-lookup"><span data-stu-id="b6466-104">Microsoft Dynamics 365 Human Resources uses payment frequencies to calculate the annual benefit salary, determine the benefit premium amount an employee pays each pay period, and how often providers are paid.</span></span>

<span data-ttu-id="b6466-105">福利付款频率使用换算系数转换每月、每半月、每两周、每周和每天付款频率之间的福利付款期间。</span><span class="sxs-lookup"><span data-stu-id="b6466-105">Benefit payment frequencies use conversion factors to convert benefit payment periods between monthly, semi-monthly, biweekly, weekly, and daily payment frequencies.</span></span> <span data-ttu-id="b6466-106">这使公司可以定义福利计划中付款频率之间的相关性。</span><span class="sxs-lookup"><span data-stu-id="b6466-106">This allows companies to define the interdependence between the payment frequencies within a benefit plan.</span></span>

<span data-ttu-id="b6466-107">换算系数字段标识从付款频率到标准付款期间的换算系数，允许系统在付款频率之间进行计算。</span><span class="sxs-lookup"><span data-stu-id="b6466-107">The conversion factors fields identify the conversion factor from the payment frequency to the standard payment periods and allow the system to do calculations between payment frequencies.</span></span> <span data-ttu-id="b6466-108">换算系数金额还确定员工按每个支付频率应该支付的福利金金额。</span><span class="sxs-lookup"><span data-stu-id="b6466-108">The conversion factor amount also determines the benefit premium amount that an employee should pay each pay frequency.</span></span>

1. <span data-ttu-id="b6466-109">在 **福利管理** 工作区中，在 **设置** 下，选择 **付款频率**。</span><span class="sxs-lookup"><span data-stu-id="b6466-109">In the **Benefits management** workspace, under **Setup**, select **Payment frequencies**.</span></span>

2. <span data-ttu-id="b6466-110">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="b6466-110">Select **New**.</span></span>

3. <span data-ttu-id="b6466-111">为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="b6466-111">Specify values for the following fields:</span></span>

   | <span data-ttu-id="b6466-112">字段</span><span class="sxs-lookup"><span data-stu-id="b6466-112">Field</span></span> | <span data-ttu-id="b6466-113">说明</span><span class="sxs-lookup"><span data-stu-id="b6466-113">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="b6466-114">**付款频率**</span><span class="sxs-lookup"><span data-stu-id="b6466-114">**Payment frequency**</span></span> | <span data-ttu-id="b6466-115">唯一的付款频率名称。</span><span class="sxs-lookup"><span data-stu-id="b6466-115">A unique payment frequency name.</span></span> |
   | <span data-ttu-id="b6466-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="b6466-116">**Description**</span></span> | <span data-ttu-id="b6466-117">付款频率的描述。</span><span class="sxs-lookup"><span data-stu-id="b6466-117">A description of the payment frequency.</span></span> |
   | <span data-ttu-id="b6466-118">**期间余额**</span><span class="sxs-lookup"><span data-stu-id="b6466-118">**Period**</span></span> | <span data-ttu-id="b6466-119">与福利提供商和员工付款频率最匹配的合适的期间。</span><span class="sxs-lookup"><span data-stu-id="b6466-119">The appropriate period that best matches the benefit provider’s and employee’s payment frequency.</span></span> <span data-ttu-id="b6466-120">期间列表包含标准付款期间。</span><span class="sxs-lookup"><span data-stu-id="b6466-120">The period list is composed of the standard payment periods.</span></span> |
   | <span data-ttu-id="b6466-121">**付薪期间数**</span><span class="sxs-lookup"><span data-stu-id="b6466-121">**Number of pay periods**</span></span> | <span data-ttu-id="b6466-122">代表福利提供商或员工的支付频率的支付期间数。</span><span class="sxs-lookup"><span data-stu-id="b6466-122">The number of pay periods that represents how often the benefit provider or employees are paid.</span></span> <span data-ttu-id="b6466-123">此数字将用于计算员工的年度福利薪金金额。</span><span class="sxs-lookup"><span data-stu-id="b6466-123">This amount will be used to calculate the employee‘s annual benefit salary amount.</span></span> |
   | <span data-ttu-id="b6466-124">**年度换算系数**</span><span class="sxs-lookup"><span data-stu-id="b6466-124">**Annual conversion factor**</span></span> | <span data-ttu-id="b6466-125">付款频率的年度换算系数。</span><span class="sxs-lookup"><span data-stu-id="b6466-125">The annual conversion factor for the payment frequency.</span></span> <span data-ttu-id="b6466-126">例如，每月支付频率的年度换算系数为：</span><span class="sxs-lookup"><span data-stu-id="b6466-126">For example, the annual conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="b6466-127">（12 次每月付款/1 年）= 12</span><span class="sxs-lookup"><span data-stu-id="b6466-127">(12 monthly payments / 1 year) = 12</span></span> |
   | <span data-ttu-id="b6466-128">**每半年换算系数**</span><span class="sxs-lookup"><span data-stu-id="b6466-128">**Semiannual conversion factor**</span></span> | <span data-ttu-id="b6466-129">付款频率的半年换算系数。</span><span class="sxs-lookup"><span data-stu-id="b6466-129">The semiannual conversion factor for the payment frequency.</span></span> <span data-ttu-id="b6466-130">例如，每月支付频率的半年换算系数为：</span><span class="sxs-lookup"><span data-stu-id="b6466-130">For example, the semiannual conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="b6466-131">（12 次每月付款/一年 2 次）= 6</span><span class="sxs-lookup"><span data-stu-id="b6466-131">(12 monthly payments / 2 times a year) = 6</span></span> |
   | <span data-ttu-id="b6466-132">**季度换算系数**</span><span class="sxs-lookup"><span data-stu-id="b6466-132">**Quarterly conversion factor**</span></span> | <span data-ttu-id="b6466-133">付款频率的季度换算系数。</span><span class="sxs-lookup"><span data-stu-id="b6466-133">The quarterly conversion factor for the payment frequency.</span></span> <span data-ttu-id="b6466-134">例如，每月支付频率的季度换算系数为：</span><span class="sxs-lookup"><span data-stu-id="b6466-134">For example, the quarterly conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="b6466-135">（12 次每月付款/4 个季度）= 3</span><span class="sxs-lookup"><span data-stu-id="b6466-135">(12 monthly payments / 4 quarters) = 3</span></span> |
   | <span data-ttu-id="b6466-136">**每月换算系数**</span><span class="sxs-lookup"><span data-stu-id="b6466-136">**Monthly conversion factor**</span></span> | <span data-ttu-id="b6466-137">付款频率的每月换算系数。</span><span class="sxs-lookup"><span data-stu-id="b6466-137">The monthly conversion factor for the payment frequency.</span></span> <span data-ttu-id="b6466-138">例如，每月支付频率的每月换算系数为：</span><span class="sxs-lookup"><span data-stu-id="b6466-138">For example, the monthly conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="b6466-139">（12 次每月付款/12 个月）= 1</span><span class="sxs-lookup"><span data-stu-id="b6466-139">(12 monthly payments / 12 months) = 1</span></span> |
   | <span data-ttu-id="b6466-140">**每半月换算系数**</span><span class="sxs-lookup"><span data-stu-id="b6466-140">**Semimonthly conversion factor**</span></span> | <span data-ttu-id="b6466-141">付款频率的每半月换算系数。</span><span class="sxs-lookup"><span data-stu-id="b6466-141">The semimonthly conversion factor for the payment frequency.</span></span> <span data-ttu-id="b6466-142">例如，每月支付频率的每半月换算系数为：</span><span class="sxs-lookup"><span data-stu-id="b6466-142">For example, the semimonthly conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="b6466-143">(12 次每月付款/ 24(每月 2 次))= 0.5</span><span class="sxs-lookup"><span data-stu-id="b6466-143">(12 monthly payments / 24 (2x a month)) = 0.5</span></span> | 
   | <span data-ttu-id="b6466-144">**每两周换算系数**</span><span class="sxs-lookup"><span data-stu-id="b6466-144">**Biweekly conversion factor**</span></span> | <span data-ttu-id="b6466-145">付款频率的年度换算系数。</span><span class="sxs-lookup"><span data-stu-id="b6466-145">The annual conversion factor for the payment frequency.</span></span> <span data-ttu-id="b6466-146">例如，每月支付频率的年度换算系数为：</span><span class="sxs-lookup"><span data-stu-id="b6466-146">For example, the annual conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="b6466-147">（12 次每月付款/26 周）= 0.461538</span><span class="sxs-lookup"><span data-stu-id="b6466-147">(12 monthly payments / 26 weeks) = 0.461538</span></span> |
   | <span data-ttu-id="b6466-148">**每周换算系数**</span><span class="sxs-lookup"><span data-stu-id="b6466-148">**Weekly conversion factor**</span></span> | <span data-ttu-id="b6466-149">付款频率的年度换算系数。</span><span class="sxs-lookup"><span data-stu-id="b6466-149">The annual conversion factor for the payment frequency.</span></span> <span data-ttu-id="b6466-150">例如，每月支付频率的年度换算系数为：</span><span class="sxs-lookup"><span data-stu-id="b6466-150">For example, the annual conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="b6466-151">（12 次每月付款/52 周）= 0.230769</span><span class="sxs-lookup"><span data-stu-id="b6466-151">(12 monthly payments / 52 weeks) = 0.230769</span></span> |
   | <span data-ttu-id="b6466-152">**每日换算系数**</span><span class="sxs-lookup"><span data-stu-id="b6466-152">**Daily conversion factor**</span></span> | <span data-ttu-id="b6466-153">付款频率的年度换算系数。</span><span class="sxs-lookup"><span data-stu-id="b6466-153">The annual conversion factor for the payment frequency.</span></span> <span data-ttu-id="b6466-154">例如，每月支付频率的年度换算系数为：</span><span class="sxs-lookup"><span data-stu-id="b6466-154">For example, the annual conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="b6466-155">（12 次每月付款/365 天）= 0.032877</span><span class="sxs-lookup"><span data-stu-id="b6466-155">(12 monthly payments / 365 days) = 0.032877</span></span> |
   | <span data-ttu-id="b6466-156">**每小时换算系数**</span><span class="sxs-lookup"><span data-stu-id="b6466-156">**Hourly conversion factor**</span></span> | <span data-ttu-id="b6466-157">付款频率的年度换算系数。</span><span class="sxs-lookup"><span data-stu-id="b6466-157">The annual conversion factor for the payment frequency.</span></span> <span data-ttu-id="b6466-158">例如，每月支付频率的年度换算系数为：</span><span class="sxs-lookup"><span data-stu-id="b6466-158">For example, the annual conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="b6466-159">（12 次每月付款/2080 小时）= 0.005769</span><span class="sxs-lookup"><span data-stu-id="b6466-159">(12 monthly payments / 2080 hours) = 0.005769</span></span>

4. <span data-ttu-id="b6466-160">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="b6466-160">Select **Save**.</span></span> 
