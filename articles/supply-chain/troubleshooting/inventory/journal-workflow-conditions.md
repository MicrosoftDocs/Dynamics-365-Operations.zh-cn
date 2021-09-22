---
title: 库存日记帐工作流条件在日记帐级别应用，不在行级别应用
description: 库存日记帐工作流条件只能在日记帐级别应用，不能在行级别应用。
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 46bdde7f09c639fbefd46162431762b056d521ae
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475687"
---
# <a name="inventory-journal-workflow-conditions-apply-at-the-journal-level-not-line-level"></a>库存日记帐工作流条件在日记帐级别应用，不在行级别应用

## <a name="symptoms"></a>故障特征

比如，如果您尝试对成本金额设置库存日记帐工作流条件，可能会遇到此问题。 您设置此条件，让步骤 1 仅在成本金额小于 100 时运行。 然后设置另一个条件，让步骤 2 仅在成本金额大于或等于 100 时运行。 然后，在工作流运行时，工作流历史记录将仅显示一行，第一个条件始终计算为 *true*，无论提交什么值。

## <a name="workaround"></a>解决方法

在当前版本中，日记帐工作流条件只在日记帐级别应用，不在行级别应用。 此为有意行为。 我们建议您仅对日记帐级属性设置条件。
