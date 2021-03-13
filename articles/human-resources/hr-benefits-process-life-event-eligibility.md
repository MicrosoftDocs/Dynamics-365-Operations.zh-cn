---
title: 处理生命事件资格
description: 本文将向您展示如何运行生命事件资格的流程。
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c7e9fda1b5e3dc2c0afdfd4c23bed277b4748bfd
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111659"
---
# <a name="process-life-event-eligibility"></a><span data-ttu-id="73dde-103">处理生命事件资格</span><span class="sxs-lookup"><span data-stu-id="73dde-103">Process life event eligibility</span></span>

<span data-ttu-id="73dde-104">本文将向您展示如何运行生命事件资格的流程。</span><span class="sxs-lookup"><span data-stu-id="73dde-104">This article shows you how to run the process for life event eligibility.</span></span>

1. <span data-ttu-id="73dde-105">在 **福利管理** 工作区中，在 **处理** 下，选择 **生命事件资格处理**。</span><span class="sxs-lookup"><span data-stu-id="73dde-105">In the **Benefits management** workspace, under **Processing**, select **Life event eligibility processing**.</span></span>

2. <span data-ttu-id="73dde-106">在 **运行生命事件资格流程** 对话框中，为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="73dde-106">In the **Run life event eligibility process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="73dde-107">字段</span><span class="sxs-lookup"><span data-stu-id="73dde-107">Field</span></span> | <span data-ttu-id="73dde-108">说明</span><span class="sxs-lookup"><span data-stu-id="73dde-108">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="73dde-109">**登记期间**</span><span class="sxs-lookup"><span data-stu-id="73dde-109">**Enrollment period**</span></span> | <span data-ttu-id="73dde-110">要处理其间的生命事件资格的登记期间。</span><span class="sxs-lookup"><span data-stu-id="73dde-110">The enrollment period to process life event eligibility for.</span></span> |

3. <span data-ttu-id="73dde-111">如果要在后台运行此流程，请选择 **在后台运行** 并执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="73dde-111">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="73dde-112">输入流程的信息。</span><span class="sxs-lookup"><span data-stu-id="73dde-112">Enter information for the process.</span></span>

   2. <span data-ttu-id="73dde-113">要设置重复性作业，请选择 **重复**，输入重复信息，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="73dde-113">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="73dde-114">要设置作业预警，请选择 **预警**，选择要接收的预警，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="73dde-114">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="73dde-115">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="73dde-115">Select **OK**.</span></span> <span data-ttu-id="73dde-116">流程将使用您设置的参数运行。</span><span class="sxs-lookup"><span data-stu-id="73dde-116">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="73dde-117">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="73dde-117">Select **OK**.</span></span>
