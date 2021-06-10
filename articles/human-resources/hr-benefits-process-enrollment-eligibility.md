---
title: 处理登记资格
description: 本文介绍如何运行登记资格流程。
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4dd63e755f0afdbce411b3001410d2e56036e432
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054252"
---
# <a name="process-enrollment-eligibility"></a><span data-ttu-id="de5c9-103">处理登记资格</span><span class="sxs-lookup"><span data-stu-id="de5c9-103">Process enrollment eligibility</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="de5c9-104">本文介绍如何运行登记资格流程。</span><span class="sxs-lookup"><span data-stu-id="de5c9-104">This article explains how to run the enrollment eligibility process.</span></span>

1. <span data-ttu-id="de5c9-105">在 **福利管理** 工作区中，在 **处理** 下，选择 **登记资格处理**。</span><span class="sxs-lookup"><span data-stu-id="de5c9-105">In the **Benefits management** workspace, under **Processing**, select **Enrollment eligibility processing**.</span></span>

2. <span data-ttu-id="de5c9-106">在 **运行福利登记资格流程** 对话框中，为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="de5c9-106">In the **Run benefit enrollment eligibility process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="de5c9-107">字段</span><span class="sxs-lookup"><span data-stu-id="de5c9-107">Field</span></span> | <span data-ttu-id="de5c9-108">说明</span><span class="sxs-lookup"><span data-stu-id="de5c9-108">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="de5c9-109">**登记期间**</span><span class="sxs-lookup"><span data-stu-id="de5c9-109">**Enrollment period**</span></span> | <span data-ttu-id="de5c9-110">要处理其间的登记资格的登记期间。</span><span class="sxs-lookup"><span data-stu-id="de5c9-110">The enrollment period to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="de5c9-111">**法人**</span><span class="sxs-lookup"><span data-stu-id="de5c9-111">**Legal entity**</span></span> | <span data-ttu-id="de5c9-112">要为其处理登记资格的法人。</span><span class="sxs-lookup"><span data-stu-id="de5c9-112">The legal entity to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="de5c9-113">**工作线程**</span><span class="sxs-lookup"><span data-stu-id="de5c9-113">**Worker**</span></span> | <span data-ttu-id="de5c9-114">要为其处理登记资格的工作人员。</span><span class="sxs-lookup"><span data-stu-id="de5c9-114">The worker to process enrollment eligibility for.</span></span> <span data-ttu-id="de5c9-115">如果将此字段留为空白，将处理所有工作人员的登记资格。</span><span class="sxs-lookup"><span data-stu-id="de5c9-115">If you leave this field blank, enrollment eligibility will be processed for all workers.</span></span> |
   | <span data-ttu-id="de5c9-116">**福利计划**</span><span class="sxs-lookup"><span data-stu-id="de5c9-116">**Benefit plan**</span></span> | <span data-ttu-id="de5c9-117">要为其处理登记资格的福利计划。</span><span class="sxs-lookup"><span data-stu-id="de5c9-117">The benefit plan to process enrollment eligibility for.</span></span>

3. <span data-ttu-id="de5c9-118">如果要在后台运行此流程，请选择 **在后台运行** 并执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="de5c9-118">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="de5c9-119">输入流程的信息。</span><span class="sxs-lookup"><span data-stu-id="de5c9-119">Enter information for the process.</span></span>

   2. <span data-ttu-id="de5c9-120">要设置重复性作业，请选择 **重复**，输入重复信息，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="de5c9-120">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="de5c9-121">要设置作业预警，请选择 **预警**，选择要接收的预警，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="de5c9-121">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="de5c9-122">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="de5c9-122">Select **OK**.</span></span> <span data-ttu-id="de5c9-123">流程将使用您设置的参数运行。</span><span class="sxs-lookup"><span data-stu-id="de5c9-123">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="de5c9-124">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="de5c9-124">Select **OK**.</span></span>

## <a name="view-process-results"></a><span data-ttu-id="de5c9-125">查看流程结果</span><span class="sxs-lookup"><span data-stu-id="de5c9-125">View Process Results</span></span>

<span data-ttu-id="de5c9-126">本文介绍如何查看资格流程结果。</span><span class="sxs-lookup"><span data-stu-id="de5c9-126">This article explains how to view eligibility process results.</span></span>

1.  <span data-ttu-id="de5c9-127">在 **福利管理** 工作区中，在 **处理** 下，选择 **流程结果**。</span><span class="sxs-lookup"><span data-stu-id="de5c9-127">In the **Benefits management** workspace, under **Processing**, select **Process results**.</span></span>

2.  <span data-ttu-id="de5c9-128">在 **流程结果** 窗体中，指定了以下字段：</span><span class="sxs-lookup"><span data-stu-id="de5c9-128">In the **Process results** form, the following fields are specified:</span></span>

   | <span data-ttu-id="de5c9-129">字段</span><span class="sxs-lookup"><span data-stu-id="de5c9-129">Field</span></span> | <span data-ttu-id="de5c9-130">说明</span><span class="sxs-lookup"><span data-stu-id="de5c9-130">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="de5c9-131">**流程 ID**</span><span class="sxs-lookup"><span data-stu-id="de5c9-131">**Process ID**</span></span> | <span data-ttu-id="de5c9-132">工作人员、法人和运行的流程的组合的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="de5c9-132">The unique ID for the combination of Worker, Legal entity, and process run.</span></span> |
   | <span data-ttu-id="de5c9-133">**进程类型**</span><span class="sxs-lookup"><span data-stu-id="de5c9-133">**Process type**</span></span> | <span data-ttu-id="de5c9-134">这用于标识运行的流程。</span><span class="sxs-lookup"><span data-stu-id="de5c9-134">This identifies the process that was run.</span></span> <span data-ttu-id="de5c9-135">例如：登记。</span><span class="sxs-lookup"><span data-stu-id="de5c9-135">For example:  Enrollment.</span></span> |
   | <span data-ttu-id="de5c9-136">**时间戳**</span><span class="sxs-lookup"><span data-stu-id="de5c9-136">**Time stamp**</span></span> | <span data-ttu-id="de5c9-137">资格流程的运行时间。</span><span class="sxs-lookup"><span data-stu-id="de5c9-137">The time that the eligibility process was run.</span></span> |
   | <span data-ttu-id="de5c9-138">**法人**</span><span class="sxs-lookup"><span data-stu-id="de5c9-138">**Legal entity**</span></span> | <span data-ttu-id="de5c9-139">登记流程中指定的法人。</span><span class="sxs-lookup"><span data-stu-id="de5c9-139">The legal entity specified during the enrollment process.</span></span> |
   | <span data-ttu-id="de5c9-140">**工作线程**</span><span class="sxs-lookup"><span data-stu-id="de5c9-140">**Worker**</span></span> | <span data-ttu-id="de5c9-141">处理的工作人员。</span><span class="sxs-lookup"><span data-stu-id="de5c9-141">The worker who was processed.</span></span> |
   | <span data-ttu-id="de5c9-142">\*\*计划</span><span class="sxs-lookup"><span data-stu-id="de5c9-142">\*\*Plan</span></span> | <span data-ttu-id="de5c9-143">尝试的登记所属福利计划。</span><span class="sxs-lookup"><span data-stu-id="de5c9-143">The Benefit plan that enrollment was attempted for.</span></span> |
   | <span data-ttu-id="de5c9-144">**资格规则**</span><span class="sxs-lookup"><span data-stu-id="de5c9-144">**Eligibility rule**</span></span> | <span data-ttu-id="de5c9-145">处理的资格规则。</span><span class="sxs-lookup"><span data-stu-id="de5c9-145">The eligibility rule that was processed.</span></span> <span data-ttu-id="de5c9-146">如果在运行资格前遇到了错误，此字段将为空。</span><span class="sxs-lookup"><span data-stu-id="de5c9-146">If an error was encountered before eligibility was run, this will be blank.</span></span> <span data-ttu-id="de5c9-147">例如，如果尚未为某个工作人员定义薪酬，将不会运行资格流程，并且此字段将保留为空。</span><span class="sxs-lookup"><span data-stu-id="de5c9-147">For example: If compensation hasn't been defined for a worker, the eligibility process won't run, and this field will be left blank.</span></span> |
   | <span data-ttu-id="de5c9-148">**结果状态**</span><span class="sxs-lookup"><span data-stu-id="de5c9-148">**Result status**</span></span> | <span data-ttu-id="de5c9-149">将为“合格”或“不合格”。</span><span class="sxs-lookup"><span data-stu-id="de5c9-149">This will be Eligible or Ineligible.</span></span> <span data-ttu-id="de5c9-150">如果工作人员不满足资格规则条件，工作人员缺少必需信息（如付款频率或固定薪酬），或福利计划中缺少的信息导致无法登记工作人员，结果状态将为“不合格”。</span><span class="sxs-lookup"><span data-stu-id="de5c9-150">The result status will be Ineligible if the worker didn’t meet the eligibility rule criteria, if the worker is missing required information such as a pay frequency or fixed compensation, or if there is information missing on the benefit plan that prevents workers from being enrolled.</span></span> |
   | <span data-ttu-id="de5c9-151">**结果消息**</span><span class="sxs-lookup"><span data-stu-id="de5c9-151">**Result message**</span></span> | <span data-ttu-id="de5c9-152">指示工作人员为何不符合福利计划的资格或是否通过了资格规则。</span><span class="sxs-lookup"><span data-stu-id="de5c9-152">Indicates why a worker is ineligible for a benefit plan or if the eligibility rule passed.</span></span> |



[!INCLUDE[footer-include](../includes/footer-banner.md)]