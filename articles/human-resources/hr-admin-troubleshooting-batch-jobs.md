---
title: 通过将批处理作业安排到非营业时间优化性能
description: 此主题介绍如何通过将批处理作业安排到非营业时间来解决 Microsoft Dynamics 365 Human Resources 的性能问题。
author: andreabichsel
manager: tfehr
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 219537aab2015469b6ca6ebed5c00af0190c5187
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111664"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a>通过将批处理作业安排到非营业时间优化性能

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a>发货

如果在典型营业时间长时间运行批处理作业，Microsoft Dynamics 365 Human Resources 可能会遇到性能问题。

## <a name="resolution"></a>解决方法

将以下批处理作业安排到非工作时间。 我们还建议检查频繁运行的批处理作业的频率。 如果可以，减少批处理作业的周期。 在许多情况下，默认频率就足够了。

以下批处理作业应该在夜间或非营业时间运行。 务必检查这些定期批处理作业的时区。 某些批处理作业可能使用太平洋标准时间 (PST)。

| 批处理作业 | 本币 |
| --- | --- |
| 批处理作业历史记录清理 | 每月 1 次 |
| 出口暂存清除 | 每天 1 次 |
| Common Data Service 集成缺失的请求同步 | 每天 1 次 |
| 需要在非工作时间定期运行的数据库压缩系统作业 | 每天 1 次 |
| 需要在非工作时间定期运行的数据库索引重建系统作业 | 每天 1 次 |

1. 在 Human Resources 中，选择 **系统管理**。

2. 在 **搜索** 栏中，搜索上面的一个批处理作业。

3. 选择 **在后台运行**，然后选择 **重复执行**。

   ![设置重复执行](media/talent-batch-history-cleanup-recurrence.png)

4. 在 **定义重复项** 下，将 **开始日期** 和 **开始时间** 设置为在下班时间或周末进行。 选择 **无结束日期**。 

   ![定义重复执行的开始日期和时间](media/talent-batch-history-cleanup-define-recurrence.png)

5. 选择 **确定**。

6. 如果需要，更改 **在后台运行** 下的其他任何参数，然后选择 **确定**。

## <a name="additional-resources"></a>其他资源

[使用自动清理任务优化性能](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]