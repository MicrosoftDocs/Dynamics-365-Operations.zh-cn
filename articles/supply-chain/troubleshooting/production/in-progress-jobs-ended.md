---
title: 报告上一个作业的部分数量时正在进行的作业结束
description: 当使用作业卡设备报告生产订单中最后一个作业的部分数量时，状态为“进行中”的所有先前的作业会结束。
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 11511d4ac7524facdd0d647e9bc38fe09c282be1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475730"
---
# <a name="previous-in-progress-jobs-are-ended-when-reporting-partial-quantity-on-last-job"></a>报告上一个作业的部分数量时正在进行的先前作业结束

## <a name="symptoms"></a>故障特征

使用作业卡设备报告生产订单中最后一个作业的部分数量时，该订单上状态为“进行中”的所有先前的作业会自动结束。

## <a name="resolution"></a>解决方法

此为有意行为。 在 **生产订单默认值** 页上的 **完工入库** 选项卡上，有一个名为 **带结束标记的工艺路线** 选项。 如果此主题设置为 *是*，当工作人员使用作业卡设备或作业卡终端报告最后一道工序时，将过帐工艺卡日记帐。 此日记帐将所有操作标记为已完成，并结束所有生产作业。 当 **带结束标记的工艺路线** 选项设置为 *是* 时，系统不会考虑工作人员报告最后一道工序时选择的作业状态。 系统也不会考虑工作人员报告的是全部还是部分数量。
