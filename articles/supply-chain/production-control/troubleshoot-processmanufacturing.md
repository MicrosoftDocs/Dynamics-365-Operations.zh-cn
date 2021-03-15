---
title: 流程制造疑难解答
description: 此主题介绍如何解决使用流程制造时可能遇到的问题。
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: d999c91aa1cc14f29ebfa6be8e456e45ef0d3fa4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966172"
---
# <a name="troubleshoot-process-manufacturing"></a>流程制造疑难解答

此主题介绍如何解决使用流程制造时可能遇到的问题。

## <a name="when-i-use-the-job-card-device-to-report-a-partial-quantity-on-the-last-job-in-a-production-order-all-the-previous-jobs-on-that-order-that-have-a-status-of-in-progress-are-automatically-ended"></a>当我使用作业卡设备报告生产订单中最后一个作业的部分数量时，该订单上状态为“进行中”的所有先前的作业会自动结束。

此为有意行为。 在 **生产订单默认值** 页上的 **完工入库** 选项卡上，有一个名为 **带结束标记的工艺路线** 选项。 如果此主题设置为 *是*，当工作人员使用作业卡设备或作业卡终端报告最后一道工序时，将过帐工艺卡日记帐。 此日记帐将所有操作标记为已完成，并结束所有生产作业。 当 **带结束标记的工艺路线** 选项设置为 *是* 时，系统不会考虑工作人员报告最后一道工序时选择的作业状态。 系统也不会考虑工作人员报告的是全部还是部分数量。

## <a name="when-i-attempt-a-stock-closing-i-receive-the-following-warning-message-no-execution-of-backflush-costing-calculation-with-a-date-1-matching-period-end-has-been-registered"></a>当我尝试库存结转时，收到以下警告消息：“其日期 %1 与期间结束匹配的倒冲成本计算法计算未执行已登记。”

在版本 10.0.13 之前的版本中，如果您不使用精益生产成本计算流程，在库存结转期间会收到以下错误的警告消息：

> 您将要执行日期为 %1 的库存结转。 其日期 %1 与期间结束匹配的倒冲成本计算法计算未执行已登记。 请记住执行其日期 %1 与期间结束匹配的倒冲成本计算法计算。 执行之前，子分类帐或总帐中的库存、所售货物成本和差异评估可能不正确。

此问题在版本 10.0.13 和更高版本中已修复。 有关详细信息，请参阅 [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296)。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]