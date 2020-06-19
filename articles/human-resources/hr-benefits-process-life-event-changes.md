---
title: 处理生命事件更改
description: 在 Microsoft Dynamics 365 Human Resources 中处理生命事件更改以进行生命事件更改。
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
ms.openlocfilehash: 11809bcf631316a064a3c917926f486ff22cb35a
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429120"
---
# <a name="process-life-event-changes"></a><span data-ttu-id="18cad-103">处理生命事件更改</span><span class="sxs-lookup"><span data-stu-id="18cad-103">Process life event changes</span></span>

<span data-ttu-id="18cad-104">在 Microsoft Dynamics 365 Human Resources 中处理生命事件更改以进行两项生命事件更改：</span><span class="sxs-lookup"><span data-stu-id="18cad-104">Process life event changes in Microsoft Dynamics 365 Human Resources for two life event changes:</span></span>

- <span data-ttu-id="18cad-105">生日更改</span><span class="sxs-lookup"><span data-stu-id="18cad-105">Birthday changes</span></span>
- <span data-ttu-id="18cad-106">资格规则覆盖到期更改</span><span class="sxs-lookup"><span data-stu-id="18cad-106">Eligibility rule override expiration changes</span></span> 

1. <span data-ttu-id="18cad-107">在**福利管理**工作区中，在**处理**下，选择**生命事件更改处理**。</span><span class="sxs-lookup"><span data-stu-id="18cad-107">In the **Benefits management** workspace, under **Processing**, select **Life event change processing**.</span></span>

2. <span data-ttu-id="18cad-108">在**运行生命事件更改流程**对话框中，为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="18cad-108">In the **Run life event change process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="18cad-109">字段</span><span class="sxs-lookup"><span data-stu-id="18cad-109">Field</span></span> | <span data-ttu-id="18cad-110">说明</span><span class="sxs-lookup"><span data-stu-id="18cad-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="18cad-111">登记期间</span><span class="sxs-lookup"><span data-stu-id="18cad-111">Enrollment period</span></span> | <span data-ttu-id="18cad-112">要处理其间的生命事件更改的登记期间。</span><span class="sxs-lookup"><span data-stu-id="18cad-112">The enrollment period to process life event changes for.</span></span> |
   | <span data-ttu-id="18cad-113">法人</span><span class="sxs-lookup"><span data-stu-id="18cad-113">Legal entity</span></span> | <span data-ttu-id="18cad-114">要为其处理生命事件更改的法人。</span><span class="sxs-lookup"><span data-stu-id="18cad-114">The legal entity to process life event changes for.</span></span> |

3. <span data-ttu-id="18cad-115">如果要在后台运行此流程，请选择**在后台运行**并执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="18cad-115">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="18cad-116">输入流程的信息。</span><span class="sxs-lookup"><span data-stu-id="18cad-116">Enter information for the process.</span></span>

   2. <span data-ttu-id="18cad-117">要设置重复性作业，请选择**重复**，输入重复信息，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="18cad-117">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="18cad-118">要设置作业预警，请选择**预警**，选择要接收的预警，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="18cad-118">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="18cad-119">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="18cad-119">Select **OK**.</span></span> <span data-ttu-id="18cad-120">流程将使用您设置的参数运行。</span><span class="sxs-lookup"><span data-stu-id="18cad-120">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="18cad-121">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="18cad-121">Select **OK**.</span></span>
