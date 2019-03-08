---
title: 产品配置的求解器策略
description: 此主题介绍如何使用求解器策略改进产品配置的性能。
author: cvocph
manager: AnnBe
ms.date: 01/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCCreateProductConfigurationModel, PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d0abb9313ec62cfdfe3bf7c810e2143dcf502bf9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "351140"
---
# <a name="solver-strategy-for-product-configuration"></a>产品配置的求解器策略

[!include [banner](../includes/banner.md)]

此主题介绍如何使用求解器策略改进产品配置的性能。

求解器这一概念最初是在 Microsoft Dynamics AX 2012 R2 的累积更新 7 (CU7) 中引入的。 并在 Microsoft Dynamics AX 2012 R3 的累积更新 8 (CU8) 和 Microsoft Dynamics 365 for Finance and Operations Enterprise edition 7.3 中得以延伸。

求解器策略概念现在包含以下策略：

- 默认
- 最小域数量优先
- 自上而下
- Z3

## <a name="solver-strategy"></a>求解器策略 

可将产品配置模型编制为[约束满足问题 (CSP)](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf)。 Microsoft Solver Foundation (MSF) 提供两种类型的求解器策略来解决可从产品配置模型使用的 CSP。 这些求解器策略依赖于[启发](https://techterms.com/definition/heuristic)，启发用于确定解决问题时考虑 CSP 变量的顺序。 解决一个问题或一类问题时，启发可显著影响性能。

在 Finance and Operations 中，产品配置模型的求解器策略确定启发使用哪个求解器。 **默认**、**最小域数量优先**和**自上而下**策略使用 MSF 中的两个求解器，而 **Z3** 策略则使用 Z3 求解器。 

真实的客户实施研究已表明产品配置模型的求解器策略中的更改可将响应时间从以分钟计缩短到以毫秒计。 因此，值得努力尝试不同求解器策略以找出对产品配置模型效率最高的策略。

## <a name="change-the-settings-for-the-solver-strategy"></a>更改求解器策略的设置

若要更改求解器策略，请在**配置产品模型**页面中的操作窗格上，选择**模型属性**。 然后，在**编辑模型详细信息**对话框中，选择求解器策略。

[![更改求解器策略](./media/solver-strategy.png)](./media/solver-strategy.png)

目前不存在自动检测哪个求解器策略对基于约束的产品配置效率最高的逻辑。 因此，必须逐一尝试求解器策略。

下表提供有关各种方案中要使用的求解器策略的建议。

| 求解器策略      | 策略的使用方案 |
|----------------------|-----------------------------------|
| 默认              | **默认**策略已经过优化，可解决依赖于表约束的模型。 客户实施研究已表明，在广泛使用表约束的方案中，此策略效率最高。 |
| 最小域数量优先 | **最小域数量优先**和**自上而下**策略之间的关系非常密切。 客户实施研究已表明 CU8 中引入的**自上而下**策略比**最小域数量优先**策略更优秀。 但是，产品中仍然保留了**最小域数量优先**策略，以提供向后兼容。 研究已表明，在求解其中包含多个不使用表约束的算术表达式的模型时，这两种求解器策略的效率更高。 但是在某些情况下，**默认**策略比这两个策略更优秀。 因此，请务必尝试每个策略。 |
| 自上而下             | **最小域数量优先**和**自上而下**策略之间的关系非常密切。 客户实施研究已表明 CU8 中引入的**自上而下**策略比**最小域数量优先**策略更优秀。 但是，产品中仍然保留了**最小域数量优先**策略，以提供向后兼容。 研究已表明，在求解其中包含多个不使用表约束的算术表达式的模型时，这两种求解器策略的效率更高。 但是在某些情况下，**默认**策略比这两个策略更优秀。 因此，请务必尝试每个策略。 |
| Z3                   | 建议您将 **Z3** 策略用作默认求解器策略。 如果您注重性能和可扩展性，则可评估其他策略。 |

## <a name="additional-resources"></a>其他资源

[生成产品配置模型](build-product-configuration-model.md)

[启发](https://techterms.com/definition/heuristic)

[约束满足问题](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf)
