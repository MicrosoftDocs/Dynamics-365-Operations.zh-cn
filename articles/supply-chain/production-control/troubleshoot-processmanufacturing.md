---
title: 流程制造疑难解答
description: 此主题介绍如何解决使用流程制造时可能遇到的问题。
author: SmithaNataraj
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 938820b6cd2bb470b440fea7b70124efc0faf7f8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824982"
---
# <a name="troubleshoot-process-manufacturing"></a><span data-ttu-id="3228e-103">流程制造疑难解答</span><span class="sxs-lookup"><span data-stu-id="3228e-103">Troubleshoot process manufacturing</span></span>

<span data-ttu-id="3228e-104">此主题介绍如何解决使用流程制造时可能遇到的问题。</span><span class="sxs-lookup"><span data-stu-id="3228e-104">This topic describes how to fix issues that you might encounter while you work with process manufacturing.</span></span>

## <a name="when-i-use-the-job-card-device-to-report-a-partial-quantity-on-the-last-job-in-a-production-order-all-the-previous-jobs-on-that-order-that-have-a-status-of-in-progress-are-automatically-ended"></a><span data-ttu-id="3228e-105">当我使用作业卡设备报告生产订单中最后一个作业的部分数量时，该订单上状态为“进行中”的所有先前的作业会自动结束。</span><span class="sxs-lookup"><span data-stu-id="3228e-105">When I use the job card device to report a partial quantity on the last job in a production order, all the previous jobs on that order that have a status of In progress are automatically ended.</span></span>

<span data-ttu-id="3228e-106">此为有意行为。</span><span class="sxs-lookup"><span data-stu-id="3228e-106">This behavior is by design.</span></span> <span data-ttu-id="3228e-107">在 **生产订单默认值** 页上的 **完工入库** 选项卡上，有一个名为 **带结束标记的工艺路线** 选项。</span><span class="sxs-lookup"><span data-stu-id="3228e-107">On the **Production order defaults** page, on the **Report as finished** tab, there is an option that is named **End-mark route**.</span></span> <span data-ttu-id="3228e-108">如果此主题设置为 *是*，当工作人员使用作业卡设备或作业卡终端报告最后一道工序时，将过帐工艺卡日记帐。</span><span class="sxs-lookup"><span data-stu-id="3228e-108">If this topic is set to *Yes*, a route card journal is posted when a worker uses the job card device or job card terminal to report the last operation.</span></span> <span data-ttu-id="3228e-109">此日记帐将所有操作标记为已完成，并结束所有生产作业。</span><span class="sxs-lookup"><span data-stu-id="3228e-109">This journal marks all the operations as completed and ends all the production jobs.</span></span> <span data-ttu-id="3228e-110">当 **带结束标记的工艺路线** 选项设置为 *是* 时，系统不会考虑工作人员报告最后一道工序时选择的作业状态。</span><span class="sxs-lookup"><span data-stu-id="3228e-110">When the **End-mark route** option is set to *Yes*, the system doesn't consider the job status that the worker selected when they reported the last operation.</span></span> <span data-ttu-id="3228e-111">系统也不会考虑工作人员报告的是全部还是部分数量。</span><span class="sxs-lookup"><span data-stu-id="3228e-111">The system also doesn't consider whether the worker is reporting a full or partial quantity.</span></span>

## <a name="when-i-attempt-a-stock-closing-i-receive-the-following-warning-message-no-execution-of-backflush-costing-calculation-with-a-date-1-matching-period-end-has-been-registered"></a><span data-ttu-id="3228e-112">当我尝试库存结转时，收到以下警告消息：“其日期 %1 与期间结束匹配的倒冲成本计算法计算未执行已登记。”</span><span class="sxs-lookup"><span data-stu-id="3228e-112">When I attempt a stock closing, I receive the following warning message: "No execution of Backflush costing calculation with a date %1 matching period end has been registered."</span></span>

<span data-ttu-id="3228e-113">在版本 10.0.13 之前的版本中，如果您不使用精益生产成本计算流程，在库存结转期间会收到以下错误的警告消息：</span><span class="sxs-lookup"><span data-stu-id="3228e-113">In releases before release 10.0.13, if you aren't using the lean production costing flow, you receive the following erroneous warning message during inventory closing:</span></span>

> <span data-ttu-id="3228e-114">您将要执行日期为 %1 的库存结转。</span><span class="sxs-lookup"><span data-stu-id="3228e-114">You are about to execute an Inventory close with a date %1.</span></span> <span data-ttu-id="3228e-115">其日期 %1 与期间结束匹配的倒冲成本计算法计算未执行已登记。</span><span class="sxs-lookup"><span data-stu-id="3228e-115">No execution of Backflush costing calculation with a date %1 matching period end has been registered.</span></span> <span data-ttu-id="3228e-116">请记住执行其日期 %1 与期间结束匹配的倒冲成本计算法计算。</span><span class="sxs-lookup"><span data-stu-id="3228e-116">Please remember to execute a Backflush costing calculation with a date of %1 matching period end.</span></span> <span data-ttu-id="3228e-117">执行之前，子分类帐或总帐中的库存、所售货物成本和差异评估可能不正确。</span><span class="sxs-lookup"><span data-stu-id="3228e-117">The valuation of inventories, cost of goods sold and variances might not be correct in Subledger or General ledger until this has been executed.</span></span>

<span data-ttu-id="3228e-118">此问题在版本 10.0.13 和更高版本中已修复。</span><span class="sxs-lookup"><span data-stu-id="3228e-118">This issue has been fixed in release 10.0.13 and later.</span></span> <span data-ttu-id="3228e-119">有关详细信息，请参阅 [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296)。</span><span class="sxs-lookup"><span data-stu-id="3228e-119">For more information, see [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]