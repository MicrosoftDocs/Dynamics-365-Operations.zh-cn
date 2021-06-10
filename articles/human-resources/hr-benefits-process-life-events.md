---
title: 处理生命事件
description: 在 Microsoft Dynamics 365 Human Resources 中的员工生命周期中，每个员工可能会遇到各种生命事件的变化。
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: beac0d6666055a278cab0be9080e49c51885671d
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6057806"
---
# <a name="process-life-events"></a><span data-ttu-id="ec41f-103">处理生命事件</span><span class="sxs-lookup"><span data-stu-id="ec41f-103">Process life events</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ec41f-104">在 Microsoft Dynamics 365 Human Resources 中的员工生命周期中，每个员工可能会遇到各种生命事件的变化。</span><span class="sxs-lookup"><span data-stu-id="ec41f-104">During the employee lifecycle in Microsoft Dynamics 365 Human Resources, each employee may encounter various life event changes.</span></span> <span data-ttu-id="ec41f-105">例如，婚姻、就业变化或依赖方/受益人变化。</span><span class="sxs-lookup"><span data-stu-id="ec41f-105">For example, marriage, change in employment, or dependent/beneficiary change.</span></span> <span data-ttu-id="ec41f-106">要使用生命事件，必须在福利参数窗体中启用生命事件，设置生命事件类型，并为计划类型设置生命事件选项。</span><span class="sxs-lookup"><span data-stu-id="ec41f-106">To use life events, you must enable life events in the benefits parameters form, set up life event types, and set up life event options for plan types.</span></span>

<span data-ttu-id="ec41f-107">您必须在招聘时间范围内至少已经运行了一次开放登记，之后才能够处理生命事件。</span><span class="sxs-lookup"><span data-stu-id="ec41f-107">Before you can process life events, you must have already run open enrollment at least once during a hiring time frame.</span></span> <span data-ttu-id="ec41f-108">在美国，开放登记通常每年一次。</span><span class="sxs-lookup"><span data-stu-id="ec41f-108">In the United States, open enrollment is typically once per year.</span></span> <span data-ttu-id="ec41f-109">在美国以外地区，开放登记可以在雇用时进行。</span><span class="sxs-lookup"><span data-stu-id="ec41f-109">Outside the United States, open enrollment may be run at the time of hire.</span></span> <span data-ttu-id="ec41f-110">工作人员无需选择福利计划即可让生命事件被处理，但需要将其包括在开放登记处理中。</span><span class="sxs-lookup"><span data-stu-id="ec41f-110">A worker does not need to select a benefit plan in order for life events to be processed, but they need to have been included in open enrollment processing.</span></span> 

<span data-ttu-id="ec41f-111">当您的工作人员有将在未来发生的生命事件时，请使用生命事件处理。</span><span class="sxs-lookup"><span data-stu-id="ec41f-111">Use life event processing when you have workers who have life events that take place on a future date.</span></span> <span data-ttu-id="ec41f-112">此事件将处理所有尚未处理的生命事件（例如，未来的生命事件或已添加的并非针对任何一个工作人员的生命事件 – 一个例子是一项新的福利）。</span><span class="sxs-lookup"><span data-stu-id="ec41f-112">This event will process all life events that have not been processed (like future life events, or life events that have been added that are not specific to any one worker – one example is a new benefit).</span></span> <span data-ttu-id="ec41f-113">实时生命事件是隐藏的。</span><span class="sxs-lookup"><span data-stu-id="ec41f-113">Real-time life events are hidden.</span></span>

<span data-ttu-id="ec41f-114">例如，如果今天是 2 月 1 日，而工作人员 Joe Smith 在 2 月 14 日计划了要更改法人，如果您为 2 月 15 日运行了生命事件处理，系统将处理 2 月 15 日以前的所有事件。</span><span class="sxs-lookup"><span data-stu-id="ec41f-114">For example, if today is February 1, and on February 14 worker Joe Smith is scheduled to change legal entities, if you run life event processing for February 15, the system processes all events up until February 15.</span></span> 

1. <span data-ttu-id="ec41f-115">在 **福利管理** 工作区中，在 **处理** 下，选择 **生命事件处理**。</span><span class="sxs-lookup"><span data-stu-id="ec41f-115">In the **Benefits management** workspace, under **Processing**, select **Life event processing**.</span></span>

2. <span data-ttu-id="ec41f-116">在 **运行生命事件流程** 对话框中，为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="ec41f-116">In the **Run life event process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="ec41f-117">字段</span><span class="sxs-lookup"><span data-stu-id="ec41f-117">Field</span></span> | <span data-ttu-id="ec41f-118">说明</span><span class="sxs-lookup"><span data-stu-id="ec41f-118">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="ec41f-119">**登记期间**</span><span class="sxs-lookup"><span data-stu-id="ec41f-119">**Enrollment period**</span></span> | <span data-ttu-id="ec41f-120">要处理其间的生命事件的登记期间。</span><span class="sxs-lookup"><span data-stu-id="ec41f-120">The enrollment period to process life events for.</span></span> |
   | <span data-ttu-id="ec41f-121">**法人**</span><span class="sxs-lookup"><span data-stu-id="ec41f-121">**Legal entity**</span></span> | <span data-ttu-id="ec41f-122">要为其处理生命事件的法人。</span><span class="sxs-lookup"><span data-stu-id="ec41f-122">The legal entity to process life events for.</span></span> |
   | <span data-ttu-id="ec41f-123">**生命事件日期**</span><span class="sxs-lookup"><span data-stu-id="ec41f-123">**Life event date**</span></span> | <span data-ttu-id="ec41f-124">系统将处理在登记期间直到该日期为止的所有事件。</span><span class="sxs-lookup"><span data-stu-id="ec41f-124">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="ec41f-125">**工作线程**</span><span class="sxs-lookup"><span data-stu-id="ec41f-125">**Worker**</span></span> | <span data-ttu-id="ec41f-126">要为其处理生命事件的工作人员。</span><span class="sxs-lookup"><span data-stu-id="ec41f-126">The worker to process life events for.</span></span> <span data-ttu-id="ec41f-127">如果将此字段留为空白，将处理所有工作人员的生命事件。</span><span class="sxs-lookup"><span data-stu-id="ec41f-127">If you leave this field blank, life events will be processed for all workers.</span></span> |

3. <span data-ttu-id="ec41f-128">如果要在后台运行此流程，请选择 **在后台运行** 并执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="ec41f-128">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="ec41f-129">输入流程的信息。</span><span class="sxs-lookup"><span data-stu-id="ec41f-129">Enter information for the process.</span></span>

   2. <span data-ttu-id="ec41f-130">要设置重复性作业，请选择 **重复**，输入重复信息，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="ec41f-130">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="ec41f-131">要设置作业预警，请选择 **预警**，选择要接收的预警，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="ec41f-131">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="ec41f-132">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="ec41f-132">Select **OK**.</span></span> <span data-ttu-id="ec41f-133">流程将使用您设置的参数运行。</span><span class="sxs-lookup"><span data-stu-id="ec41f-133">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="ec41f-134">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="ec41f-134">Select **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]