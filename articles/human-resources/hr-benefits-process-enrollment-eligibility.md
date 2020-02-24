---
title: 处理登记资格
description: 本文介绍如何运行登记资格流程。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0344c48460a7d1540481e09ba106526e119de72b
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008169"
---
# <a name="process-enrollment-eligibility"></a><span data-ttu-id="a234d-103">处理登记资格</span><span class="sxs-lookup"><span data-stu-id="a234d-103">Process enrollment eligibility</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="a234d-104">本文介绍如何运行登记资格流程。</span><span class="sxs-lookup"><span data-stu-id="a234d-104">This article explains how to run the enrollment eligibility process.</span></span>

1. <span data-ttu-id="a234d-105">在**福利管理**工作区中，在**处理**下，选择**登记资格处理**。</span><span class="sxs-lookup"><span data-stu-id="a234d-105">In the **Benefits management** workspace, under **Processing**, select **Enrollment eligibility processing**.</span></span>

2. <span data-ttu-id="a234d-106">在**运行福利登记资格流程**对话框中，为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="a234d-106">In the **Run benefit enrollment eligibility process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="a234d-107">字段</span><span class="sxs-lookup"><span data-stu-id="a234d-107">Field</span></span> | <span data-ttu-id="a234d-108">说明</span><span class="sxs-lookup"><span data-stu-id="a234d-108">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="a234d-109">登记期间</span><span class="sxs-lookup"><span data-stu-id="a234d-109">Enrollment period</span></span> | <span data-ttu-id="a234d-110">要处理其间的登记资格的登记期间。</span><span class="sxs-lookup"><span data-stu-id="a234d-110">The enrollment period to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="a234d-111">法人</span><span class="sxs-lookup"><span data-stu-id="a234d-111">Legal entity</span></span> | <span data-ttu-id="a234d-112">要为其处理登记资格的法人。</span><span class="sxs-lookup"><span data-stu-id="a234d-112">The legal entity to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="a234d-113">工作线程</span><span class="sxs-lookup"><span data-stu-id="a234d-113">Worker</span></span> | <span data-ttu-id="a234d-114">要为其处理登记资格的工作人员。</span><span class="sxs-lookup"><span data-stu-id="a234d-114">The worker to process enrollment eligibility for.</span></span> <span data-ttu-id="a234d-115">如果将此字段留为空白，将处理所有工作人员的登记资格。</span><span class="sxs-lookup"><span data-stu-id="a234d-115">If you leave this field blank, enrollment eligibility will be processed for all workers.</span></span> |
   | <span data-ttu-id="a234d-116">福利计划</span><span class="sxs-lookup"><span data-stu-id="a234d-116">Benefit plan</span></span> | <span data-ttu-id="a234d-117">要为其处理登记资格的福利计划。</span><span class="sxs-lookup"><span data-stu-id="a234d-117">The benefit plan to process enrollment eligibility for.</span></span>

3. <span data-ttu-id="a234d-118">如果要在后台运行此流程，请选择**在后台运行**并执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="a234d-118">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="a234d-119">输入流程的信息。</span><span class="sxs-lookup"><span data-stu-id="a234d-119">Enter information for the process.</span></span>

   2. <span data-ttu-id="a234d-120">要设置重复性作业，请选择**重复**，输入重复信息，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="a234d-120">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="a234d-121">要设置作业预警，请选择**预警**，选择要接收的预警，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="a234d-121">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="a234d-122">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="a234d-122">Select **OK**.</span></span> <span data-ttu-id="a234d-123">流程将使用您设置的参数运行。</span><span class="sxs-lookup"><span data-stu-id="a234d-123">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="a234d-124">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="a234d-124">Select **OK**.</span></span>
