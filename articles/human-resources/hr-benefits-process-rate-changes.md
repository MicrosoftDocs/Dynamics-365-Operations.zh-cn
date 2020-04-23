---
title: 处理比率更改
description: 处理当新的或现有的福利计划的资格规则设置发生更改时，Microsoft Dynamics 365 Human Resources 中的福利比率更改。
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
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
ms.openlocfilehash: 850709480326f6a0871f19ea1bb287631cd58b42
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/06/2020
ms.locfileid: "3229924"
---
# <a name="process-rate-changes"></a><span data-ttu-id="085c6-103">处理比率更改</span><span class="sxs-lookup"><span data-stu-id="085c6-103">Process rate changes</span></span>

<span data-ttu-id="085c6-104">处理当新的或现有的福利计划的资格规则设置发生更改时，Microsoft Dynamics 365 Human Resources 中的福利比率更改。</span><span class="sxs-lookup"><span data-stu-id="085c6-104">Process benefit rate changes in Microsoft Dynamics 365 Human Resources when a new or existing benefit plan has a change in eligibility rule settings.</span></span> <span data-ttu-id="085c6-105">如果创建了新的资格规则并将其分配给计划，这将提示系统重新运行工作人员资格，以根据新的资格选项检查工作人员现在是否有资格享受计划。</span><span class="sxs-lookup"><span data-stu-id="085c6-105">If a new eligibility rule is created and assigned to the plan, this prompts the system to rerun worker eligibility to check if workers may now be eligible for the plan based on new eligibility options.</span></span> 

1. <span data-ttu-id="085c6-106">在**福利管理**工作区中，在**处理**下，选择**比率更改更新处理**。</span><span class="sxs-lookup"><span data-stu-id="085c6-106">In the **Benefits management** workspace, under **Processing**, select **Rate change update processing**.</span></span>

2. <span data-ttu-id="085c6-107">在**运行福利比率更新流程**对话框中，为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="085c6-107">In the **Run benefit rate update process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="085c6-108">字段</span><span class="sxs-lookup"><span data-stu-id="085c6-108">Field</span></span> | <span data-ttu-id="085c6-109">说明</span><span class="sxs-lookup"><span data-stu-id="085c6-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="085c6-110">**登记期间**</span><span class="sxs-lookup"><span data-stu-id="085c6-110">**Enrollment period**</span></span> | <span data-ttu-id="085c6-111">要处理其间的比率更改的登记期间。</span><span class="sxs-lookup"><span data-stu-id="085c6-111">The enrollment period to process rate changes for.</span></span> |

3. <span data-ttu-id="085c6-112">如果要在后台运行此流程，请选择**在后台运行**并执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="085c6-112">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="085c6-113">输入流程的信息。</span><span class="sxs-lookup"><span data-stu-id="085c6-113">Enter information for the process.</span></span>

   2. <span data-ttu-id="085c6-114">要设置重复性作业，请选择**重复**，输入重复信息，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="085c6-114">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="085c6-115">要设置作业预警，请选择**预警**，选择要接收的预警，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="085c6-115">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="085c6-116">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="085c6-116">Select **OK**.</span></span> <span data-ttu-id="085c6-117">流程将使用您设置的参数运行。</span><span class="sxs-lookup"><span data-stu-id="085c6-117">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="085c6-118">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="085c6-118">Select **OK**.</span></span>
