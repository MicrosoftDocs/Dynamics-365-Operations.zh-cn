---
title: 设置付款频率
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e5fe0a16c4abbb9241fcdac88fd56e92bf04788c
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008281"
---
# <a name="set-up-payment-frequencies"></a><span data-ttu-id="ca23c-102">设置付款频率</span><span class="sxs-lookup"><span data-stu-id="ca23c-102">Set up payment frequencies</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="ca23c-103">Microsoft Dynamics 365 Human Resources 使用付款频率来计算年度福利薪金，确定员工在每个付款期间支付的福利金金额，并定义向提供商付款的频率。</span><span class="sxs-lookup"><span data-stu-id="ca23c-103">Microsoft Dynamics 365 Human Resources uses payment frequencies to calculate the annual benefit salary, determine the benefit premium amount an employee pays each pay period, and define the frequency payments are made to providers.</span></span>

<span data-ttu-id="ca23c-104">福利付款频率使用换算系数转换每月、每半月、每两周、每周和每天付款频率之间的福利付款期间。</span><span class="sxs-lookup"><span data-stu-id="ca23c-104">Benefit payment frequencies use conversion factors to convert benefit payment periods between monthly, semi-monthly, biweekly, weekly, and daily payment frequencies.</span></span> <span data-ttu-id="ca23c-105">这使公司可以定义福利计划中付款频率之间的相关性。</span><span class="sxs-lookup"><span data-stu-id="ca23c-105">This allows companies to define the interdependence between the payment frequencies within a benefit plan.</span></span>

<span data-ttu-id="ca23c-106">换算系数字段标识从付款频率到标准付款期间的换算系数，允许系统在付款频率之间进行计算。</span><span class="sxs-lookup"><span data-stu-id="ca23c-106">The conversion factors fields identify the conversion factor from the payment frequency to the standard payment periods and allow the system to do calculations between payment frequencies.</span></span> <span data-ttu-id="ca23c-107">换算系数金额还用于确定员工按每个支付频率应该支付的福利金金额。</span><span class="sxs-lookup"><span data-stu-id="ca23c-107">The conversion factor amount is also used to determine the benefit premium amount that an employee should pay each pay frequency.</span></span>

1. <span data-ttu-id="ca23c-108">在**福利管理**工作区中，在**设置**下，选择**付款频率**。</span><span class="sxs-lookup"><span data-stu-id="ca23c-108">In the **Benefits management** workspace, under **Setup**, select **Payment frequencies**.</span></span>

2. <span data-ttu-id="ca23c-109">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="ca23c-109">Select **New**.</span></span>

3. <span data-ttu-id="ca23c-110">为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="ca23c-110">Specify values for the following fields:</span></span>

   | <span data-ttu-id="ca23c-111">字段</span><span class="sxs-lookup"><span data-stu-id="ca23c-111">Field</span></span> | <span data-ttu-id="ca23c-112">说明</span><span class="sxs-lookup"><span data-stu-id="ca23c-112">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="ca23c-113">付款频率</span><span class="sxs-lookup"><span data-stu-id="ca23c-113">Payment frequency</span></span> | <span data-ttu-id="ca23c-114">唯一的付款频率名称。</span><span class="sxs-lookup"><span data-stu-id="ca23c-114">A unique payment frequency name.</span></span> |
   | <span data-ttu-id="ca23c-115">说明</span><span class="sxs-lookup"><span data-stu-id="ca23c-115">Description</span></span> | <span data-ttu-id="ca23c-116">付款频率的描述。</span><span class="sxs-lookup"><span data-stu-id="ca23c-116">A description of the payment frequency.</span></span> |
   | <span data-ttu-id="ca23c-117">期间余额</span><span class="sxs-lookup"><span data-stu-id="ca23c-117">Period</span></span> | <span data-ttu-id="ca23c-118">与福利提供商和员工付款频率最匹配的合适的期间。</span><span class="sxs-lookup"><span data-stu-id="ca23c-118">The appropriate period that best matches the benefit provider’s and employee’s payment frequency.</span></span> <span data-ttu-id="ca23c-119">期间列表包含标准付款期间。</span><span class="sxs-lookup"><span data-stu-id="ca23c-119">The period list is composed of the standard payment periods.</span></span> |
   | <span data-ttu-id="ca23c-120">付薪期间数</span><span class="sxs-lookup"><span data-stu-id="ca23c-120">Number of pay periods</span></span> | <span data-ttu-id="ca23c-121">代表福利提供商或员工的支付频率的支付期间数。</span><span class="sxs-lookup"><span data-stu-id="ca23c-121">The number of pay periods that represents how often the benefit provider or employees are paid.</span></span> <span data-ttu-id="ca23c-122">此数字将用于计算员工的年度福利薪金金额。</span><span class="sxs-lookup"><span data-stu-id="ca23c-122">This amount will be used to calculate the employee‘s annual benefit salary amount.</span></span> |
   | <span data-ttu-id="ca23c-123">年度换算系数</span><span class="sxs-lookup"><span data-stu-id="ca23c-123">Annual conversion factor</span></span> | <span data-ttu-id="ca23c-124">付款频率的年度换算系数。</span><span class="sxs-lookup"><span data-stu-id="ca23c-124">The annual conversion factor for the payment frequency.</span></span> <span data-ttu-id="ca23c-125">例如，每月支付频率的年度换算系数为：</span><span class="sxs-lookup"><span data-stu-id="ca23c-125">For example, the annual conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="ca23c-126">（12 次每月付款/1 年）= 12</span><span class="sxs-lookup"><span data-stu-id="ca23c-126">(12 monthly payments / 1 year) = 12</span></span> |
   | <span data-ttu-id="ca23c-127">每半年换算系数</span><span class="sxs-lookup"><span data-stu-id="ca23c-127">Semiannual conversion factor</span></span> | <span data-ttu-id="ca23c-128">付款频率的半年换算系数。</span><span class="sxs-lookup"><span data-stu-id="ca23c-128">The semiannual conversion factor for the payment frequency.</span></span> <span data-ttu-id="ca23c-129">例如，每月支付频率的半年换算系数为：</span><span class="sxs-lookup"><span data-stu-id="ca23c-129">For example, the semiannual conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="ca23c-130">（12 次每月付款/一年 2 次）= 6</span><span class="sxs-lookup"><span data-stu-id="ca23c-130">(12 monthly payments / 2 times a year) = 6</span></span> |
   | <span data-ttu-id="ca23c-131">季度换算系数</span><span class="sxs-lookup"><span data-stu-id="ca23c-131">Quarterly conversion factor</span></span> | <span data-ttu-id="ca23c-132">付款频率的季度换算系数。</span><span class="sxs-lookup"><span data-stu-id="ca23c-132">The quarterly conversion factor for the payment frequency.</span></span> <span data-ttu-id="ca23c-133">例如，每月支付频率的季度换算系数为：</span><span class="sxs-lookup"><span data-stu-id="ca23c-133">For example, the quarterly conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="ca23c-134">（12 次每月付款/4 个季度）= 3</span><span class="sxs-lookup"><span data-stu-id="ca23c-134">(12 monthly payments / 4 quarters) = 3</span></span> |
   | <span data-ttu-id="ca23c-135">每月换算系数</span><span class="sxs-lookup"><span data-stu-id="ca23c-135">Monthly conversion factor</span></span> | <span data-ttu-id="ca23c-136">付款频率的每月换算系数。</span><span class="sxs-lookup"><span data-stu-id="ca23c-136">The monthly conversion factor for the payment frequency.</span></span> <span data-ttu-id="ca23c-137">例如，每月支付频率的每月换算系数为：</span><span class="sxs-lookup"><span data-stu-id="ca23c-137">For example, the monthly conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="ca23c-138">（12 次每月付款/12 个月）= 1</span><span class="sxs-lookup"><span data-stu-id="ca23c-138">(12 monthly payments / 12 months) = 1</span></span> |
   | <span data-ttu-id="ca23c-139">每半月换算系数</span><span class="sxs-lookup"><span data-stu-id="ca23c-139">Semimonthly conversion factor</span></span> | <span data-ttu-id="ca23c-140">付款频率的每半月换算系数。</span><span class="sxs-lookup"><span data-stu-id="ca23c-140">The semimonthly conversion factor for the payment frequency.</span></span> <span data-ttu-id="ca23c-141">例如，每月支付频率的每半月换算系数为：</span><span class="sxs-lookup"><span data-stu-id="ca23c-141">For example, the semimonthly conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="ca23c-142">（12 次每月付款/ 24（每月 2 次））= 0.5</span><span class="sxs-lookup"><span data-stu-id="ca23c-142">(12 monthly payments / 24 (2x a month)) = .5</span></span> | 
   | <span data-ttu-id="ca23c-143">每两周换算系数</span><span class="sxs-lookup"><span data-stu-id="ca23c-143">Biweekly conversion factor</span></span> | <span data-ttu-id="ca23c-144">付款频率的年度换算系数。</span><span class="sxs-lookup"><span data-stu-id="ca23c-144">The annual conversion factor for the payment frequency.</span></span> <span data-ttu-id="ca23c-145">例如，每月支付频率的年度换算系数为：</span><span class="sxs-lookup"><span data-stu-id="ca23c-145">For example, the annual conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="ca23c-146">（12 次每月付款/26 周）= 0.461538</span><span class="sxs-lookup"><span data-stu-id="ca23c-146">(12 monthly payments / 26 weeks) = 0.461538</span></span> |
   | <span data-ttu-id="ca23c-147">每周换算系数</span><span class="sxs-lookup"><span data-stu-id="ca23c-147">Weekly conversion factor</span></span> | <span data-ttu-id="ca23c-148">付款频率的年度换算系数。</span><span class="sxs-lookup"><span data-stu-id="ca23c-148">The annual conversion factor for the payment frequency.</span></span> <span data-ttu-id="ca23c-149">例如，每月支付频率的年度换算系数为：</span><span class="sxs-lookup"><span data-stu-id="ca23c-149">For example, the annual conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="ca23c-150">（12 次每月付款/52 周）= 0.230769</span><span class="sxs-lookup"><span data-stu-id="ca23c-150">(12 monthly payments / 52 weeks) = 0.230769</span></span> |
   | <span data-ttu-id="ca23c-151">每日换算系数</span><span class="sxs-lookup"><span data-stu-id="ca23c-151">Daily conversion factor</span></span> | <span data-ttu-id="ca23c-152">付款频率的年度换算系数。</span><span class="sxs-lookup"><span data-stu-id="ca23c-152">The annual conversion factor for the payment frequency.</span></span> <span data-ttu-id="ca23c-153">例如，每月支付频率的年度换算系数为：</span><span class="sxs-lookup"><span data-stu-id="ca23c-153">For example, the annual conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="ca23c-154">（12 次每月付款/365 天）= 0.032877</span><span class="sxs-lookup"><span data-stu-id="ca23c-154">(12 monthly payments / 365 days) = 0.032877</span></span> |

4. <span data-ttu-id="ca23c-155">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="ca23c-155">Select **Save**.</span></span> 
