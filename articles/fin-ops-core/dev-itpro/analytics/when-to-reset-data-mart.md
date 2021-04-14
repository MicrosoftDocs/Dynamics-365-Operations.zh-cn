---
title: 何时重置数据市场
description: 本主题列出了重置数据市场可能会有所改进的情况，以及重置数据市场不太可能有帮助的情况。
author: jinniew
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: c88994a336528650bf8ab6e239c873fa6cd36c46
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754136"
---
# <a name="when-to-reset-a-data-mart"></a>何时重置数据市场

重置数据市场可能很耗时。 根据具体情况，此操作可能不是所需的解决方案。 本主题列出了重置数据市场可能会有所改进的情况，以及重置数据市场不太可能有帮助的情况。  

## <a name="when-do-you-need-to-do-a-data-mart-reset"></a>何时需要进行数据市场重置？
在重置数据市场之前，请考虑以下问题。 有一个或多个问题的回答为“是”，可能表明您的组织可以从重置数据市场中受益。

- 应用程序数据库已还原，但数据市场数据库未还原。
- 您看到一个会计期间的数据不正确，这不是报表设计问题导致的结果。
- 您看到一个会计期间的数据不正确，并且记录在“报表设计器”中 **集成状态** 页的“集成尝试次数”下列出（启动“报表设计器”，选择 **工具 > 集成状态**）。
- 您开启了一个支持事件，支持工程师已指导您在故障排除步骤中重置数据市场。
 
## <a name="when-its-not-appropriate-to-reset-a-data-mart"></a>何时不适合重置数据市场？
在有些情况下，我们不建议您重置数据市场。 包括以下情况。 

- 只要不是本主题列出的原因。
- 您遇到与数据同步相关的性能问题。在这种情况下，重置数据市场可能无济于事。
- 如果您由于以下任一原因而使用定期重置模式： 
  - **缺少数据** - 首先，消除报表设计问题和数据同步计时问题，例如，您观察到事实地图自缺少数据发布以来一直未运行。
  - **卡住的集成状态** - 如果集成速度慢或似乎卡住了，重置数据市场不太可能解决问题。
  - **尝试未成功的重置** - 如果已多次尝试完成重置，但由于缺少数据而未能成功，我们建议开启支持事件，在再次尝试重置数据市场前与支持工程师一起分析您的情况。
  - **过时记录** - 过时记录本身并不一定证明重置数据市场是合理的。 如果数据集较大，重置过程将需要一些时间来运行，但不太可能有改进作用。
 
## <a name="what-a-data-mart-reset-does-not-do"></a>数据市场重置不会做的事  
- 重置仅在现有任务完成时开始。 这样可以确保不会插入旧数据。 此时，您可能会看到一条消息，如“由于有活动任务，无法处理数据市场重置。 请稍后重试。”
- 重置将禁用集成任务并删除所有数据市场数据。 集成将被重新启用。

> [!NOTE]
> 以下几点指定重置数据市场 *不* 会做的两件事。 <br>
> - 重置不会清除报表设计。 <br>
> - 除非选择，否则重置不会清除公司数据或用户数据。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]