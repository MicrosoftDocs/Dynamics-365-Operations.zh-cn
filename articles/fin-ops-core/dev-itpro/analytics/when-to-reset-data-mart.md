---
title: 数据市场重置常见问题解答
description: 本主题提供有关数据市场重置的一些常见问题的解答。
author: jinniew
ms.date: 07/16/2021
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
ms.openlocfilehash: e5a40342306eb9888b456a865ab2220dccfe65f8ccecc67bf8fc16f907e06977
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6767747"
---
# <a name="data-mart-resets-faq"></a>数据市场重置常见问题解答

本主题提供有关数据市场重置的一些常见问题的解答。 数据市场的重置可能是一个耗时的流程，并且可能不是所需的解决方案，视具体情况而定。 因此，本主题包括有关数据市场重置可能有帮助的情况以及不太可能有帮助的情况的信息。

## <a name="what-is-a-data-mart-reset"></a>什么是数据市场重置？

数据市场重置将禁用集成任务，删除所有数据市场数据，然后重新启用集成。

为了确保不插入旧数据，可以仅在完成现有任务后启动数据市场重置。 如果您在所有任务完成之前尝试重置数据市场，您可能会收到一条消息，例如“由于活动任务，无法处理数据市场重置。 请稍后重试。”

## <a name="when-do-i-have-to-do-a-data-mart-reset"></a>何时需要进行数据市场重置？

如果以下一项或多项陈述适用于您的情况，您的组织可以从数据市场重置中受益：

- 应用程序数据库已还原。
- 您打开了一个支持票证，支持工程师已指导您在故障排除步骤中重置数据市场。
 
> [!NOTE]
> 重置数据市场的过程受数据库中的总帐和预算交易数的影响。 根据系统中的交易数，数据市场重置可能只需 15 分钟完成，也可能长达四个小时。 不过，如果您的重置时间超过了四个小时，我们建议您与支持人员联系。
 
## <a name="when-is-a-data-mart-reset-inappropriate"></a>何时进行数据市场重置不合适？

下面是一些不建议重置数据市场的情况：

- 您遇到与数据同步相关的性能问题。
- 您由于以下任一原因而使用定期重置模式：

    - **缺少数据** – 如果您发现缺少数据，请向 Microsoft 开具支持票证，以查看您的报表格式和可能的数据同步问题。
    - **卡住的集成状态**
    - **过时记录** – 过时记录本身并不一定证明数据市场重置是合理的。 如果数据集较大，重置流程将需要一些时间来运行，但不太可能有任何改进作用。

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a>如果重置数据市场，是否会丢失已经设计好的报表？

否。 您的报表存储在不受数据市场重置影响的 SQL 表中。 如果您担心丢失设计好的报表，可以备份不想丢失的设计。 若要备份设计，请打开 Report Designer，转到 **公司 \> 公司 \> 构建基块 \> 导出**。
 
## <a name="do-all-users-have-to-exit-the-system-before-i-can-reset-the-data-mart"></a>是否所有用户都必须退出系统才能重置数据市场？

否。 用户可以在数据市场重置期间在系统中继续工作。 但是，在重置完成之前，用户无法访问使用 Financial Reporter 创建的任何报表。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
