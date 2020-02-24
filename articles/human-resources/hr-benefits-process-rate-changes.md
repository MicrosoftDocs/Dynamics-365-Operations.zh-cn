---
title: 处理比率更改
description: 处理当新的或现有的福利计划的资格规则设置发生更改时，Microsoft Dynamics 365 Human Resources 中的福利比率更改。
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
ms.openlocfilehash: 9ebe5cfc2bdf7790770d27ece2dc67f7677db593
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008181"
---
# <a name="process-rate-changes"></a><span data-ttu-id="5262b-103">处理比率更改</span><span class="sxs-lookup"><span data-stu-id="5262b-103">Process rate changes</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="5262b-104">处理当新的或现有的福利计划的资格规则设置发生更改时，Microsoft Dynamics 365 Human Resources 中的福利比率更改。</span><span class="sxs-lookup"><span data-stu-id="5262b-104">Process benefit rate changes in Microsoft Dynamics 365 Human Resources when a new or existing benefit plan has a change in eligibility rule settings.</span></span> <span data-ttu-id="5262b-105">如果创建了新的资格规则并将其分配给计划，这将提示系统重新运行工作人员资格，以根据新的资格选项检查工作人员现在是否有资格享受计划。</span><span class="sxs-lookup"><span data-stu-id="5262b-105">If a new eligibility rule is created and assigned to the plan, this prompts the system to re-run worker eligibility to check if workers may now be eligible for the plan based on new eligibility options.</span></span> 

1. <span data-ttu-id="5262b-106">在**福利管理**工作区中，在**处理**下，选择**比率更改更新处理**。</span><span class="sxs-lookup"><span data-stu-id="5262b-106">In the **Benefits management** workspace, under **Processing**, select **Rate change update processing**.</span></span>

2. <span data-ttu-id="5262b-107">在**运行福利比率更新流程**对话框中，为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="5262b-107">In the **Run benefit rate update process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="5262b-108">字段</span><span class="sxs-lookup"><span data-stu-id="5262b-108">Field</span></span> | <span data-ttu-id="5262b-109">说明</span><span class="sxs-lookup"><span data-stu-id="5262b-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="5262b-110">登记期间</span><span class="sxs-lookup"><span data-stu-id="5262b-110">Enrollment period</span></span> | <span data-ttu-id="5262b-111">要处理其间的比率更改的登记期间。</span><span class="sxs-lookup"><span data-stu-id="5262b-111">The enrollment period to process rate changes for.</span></span> |

3. <span data-ttu-id="5262b-112">如果要在后台运行此流程，请选择**在后台运行**并执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="5262b-112">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="5262b-113">输入流程的信息。</span><span class="sxs-lookup"><span data-stu-id="5262b-113">Enter information for the process.</span></span>

   2. <span data-ttu-id="5262b-114">要设置重复性作业，请选择**重复**，输入重复信息，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="5262b-114">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="5262b-115">要设置作业预警，请选择**预警**，选择要接收的预警，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="5262b-115">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="5262b-116">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="5262b-116">Select **OK**.</span></span> <span data-ttu-id="5262b-117">流程将使用您设置的参数运行。</span><span class="sxs-lookup"><span data-stu-id="5262b-117">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="5262b-118">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="5262b-118">Select **OK**.</span></span>
