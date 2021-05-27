---
title: 何时重置数据市场
description: 本主题列出了重置数据市场可能会有所改进的情况，以及重置数据市场不太可能有帮助的情况。
author: jinniew
ms.date: 05/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: bc2c4ee490f3bebd6e7c91609a06f8dfedfcb628
ms.sourcegitcommit: 5916ea2a94ab9af7aac21f0fc44e194d5ce82917
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2021
ms.locfileid: "5988984"
---
# <a name="when-to-reset-a-data-mart"></a>何时重置数据市场

重置数据市场可能很耗时。 根据具体情况，此操作可能不是所需的解决方案。 本主题列出了重置数据市场可能会有所改进的情况，以及重置数据市场不太可能有帮助的情况。  

## <a name="when-do-i-need-to-do-a-data-mart-reset"></a>何时需要进行数据市场重置？
在重置数据市场之前，请考虑以下问题。 有一个或多个问题的回答为“是”，可能表明您的组织可以从重置数据市场中受益。

- 应用程序数据库是否已还原？
- 如果您开启了一个支持事件，支持工程师是否已指导您在故障排除步骤中重置数据市场？
 
## <a name="when-is-it-not-appropriate-to-reset-a-data-mart"></a>何时不适合重置数据市场？
在有些情况下，我们不建议您重置数据市场。 包括以下情况。 

- 您遇到与数据同步相关的性能问题。 
- 如果您由于以下任一原因而使用定期重置模式： 
  - **缺少数据** 
  - **卡住的集成状态** 
  - **过时记录** - 过时记录本身并不一定证明重置数据市场是合理的。 如果数据集较大，重置过程将需要一些时间来运行，但不太可能有改进作用。
 
## <a name="what-is-a-data-mart-reset"></a>什么是数据市场重置？
- 重置仅在现有任务完成时开始。 这样可以确保不会插入旧数据。 此时，您可能会看到一条消息，如“由于有活动任务，无法处理数据市场重置。 请稍后重试。”
- 重置将禁用集成任务并删除所有数据市场数据。 集成将被重新启用。

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a>如果重置数据市场，是否会丢失已经设计好的报表？ 
不会，您的报表存储在不受数据市场重置影响的 SQL 表中。 如果您担心丢失设计好的报表，可以备份不想丢失的设计。 要进行备份，请打开报表设计器，转到 **公司 > 公司 > 构建基块 > 导出**。
 
## <a name="is-it-necessary-for-all-users-to-exit-the-system-to-reset-the-data-mart"></a>重置数据市场时是否有必要让所有用户都退出系统？
不需要，用户可以在数据市场重置期间在系统中继续工作。 但是，在重置完成之前，他们无法访问使用 Financial Reporter 创建的任何报表。 

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
