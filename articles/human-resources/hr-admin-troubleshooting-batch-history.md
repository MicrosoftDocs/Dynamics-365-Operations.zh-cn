---
title: 使用自动清理任务优化性能
description: 此主题介绍如何通过清理批处理作业历史记录来提升 Microsoft Dynamics 365 Human Resources 中的性能。
author: twheeloc
ms.date: 08/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: a293b128364b8b0b293da03495d55e46f6b01fd6
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066085"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a>使用自动清理任务优化性能


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**发货**

如果批处理作业历史记录变得太大，Microsoft Dynamics 365 Human Resources 可能遇到性能问题。

**原因**

经常运行的批处理作业可能导致批处理作业历史记录增长到无法持续。 这可能导致性能问题。 

**解决方法**

安排自动任务以清理批处理作业历史记录。 建议将任务设置为每周运行一次，但是您的清理频率可能需要更大或更小，具体取决于您的环境。 以下过程中包含我们建议的设置，但是您可以根据自己的需要更改这些设置。

1. 在 Human Resources 中，选择 **系统管理**。

2. 在 **搜索** 栏中，输入 **批处理作业历史记录清理**。

   ![搜索批处理作业历史记录清理。](media/talent-batch-history-cleanup-search-bar.png)

3. 在 **历史记录限制(天)** 中，输入 **30**。

   ![将历史记录限制设置为 30。](media/talent-batch-history-cleanup-history-limit.png)

4. 选择 **在后台运行**，然后选择 **重复执行**。

   ![设置重复执行。](media/talent-batch-history-cleanup-recurrence.png)

5. 在 **定义重复项** 下，将 **开始日期** 和 **开始时间** 设置为在下班时间或周末进行，然后选择 **无结束日期**。 

   ![定义重复执行的开始日期和时间。](media/talent-batch-history-cleanup-define-recurrence.png)

6. 在 **重复执行模式** 下，选择 **天**，然后将 **指定间隔过后重复** 设置为 **7**。

   ![设置每周重复清理。](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. 选择 **确定**。

8. 根据需要更改 **在后台运行** 下的其他任何参数，然后选择 **确定**。



[!INCLUDE[footer-include](../includes/footer-banner.md)]
