---
title: 可用预算资金
description: 本文介绍可用预算资金功能，提供可以帮助您配置预算控制以优化组织财务资源的管理的信息。
author: RyanCCarlson2
ms.date: 11/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetControlConfiguration
audience: Application User
ms.reviewer: kfend
ms.custom:
- "60493"
- intro-internal
ms.assetid: be964167-43bc-431d-9adb-48bff32d68d5
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2021-11-28
ms.dyn365.ops.version: AX 10.0.24
ms.openlocfilehash: b6f94931ba3514c1c66d80b64846d882861d555c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898231"
---
# <a name="budget-funds-available"></a>可用预算资金

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

本文介绍可用预算资金功能，提供可以帮助您配置预算控制以优化组织财务资源的管理的信息。

## <a name="enhanced-calculation-feature-for-budget-funds-available"></a>增强的可用预算资金计算功能

**仅跟踪预算资金可用计算中的金额** 功能让您可以根据 **定义预算控制参数** 页面上的设置跟踪基础预算控制表的文档类型和状态。

有些预算控制配置选项必须具有特定设置才能使此功能正常工作。 在 **定义预算控制参数** 页面的 **可用预算资金** 选项卡上选择或清除这些选项。 下表显示了可用预算资金功能所需的设置。

| 如果选择了此选项 | 还必须选择此选项 |
| ------------------------- | -------------------------------- |
| 预留款的预算预留 | 保留款 *和* 实际支出的预算预留 |
| 保留款的预算预留 | 实际支出 |
| 具有采购申请类型文档的保留款的预算预留 | 预留款的预算预留 |

此功能仅影响新文档。 现有文档的金额将被继续跟踪并显示在预算控制统计信息查询中，直到可用预算资金设置更改并且新的预算控制配置被激活。 此时，从可用预算资金计算中删除的文档的预算跟踪数据将被删除。

我们建议您保持清除 **未过帐的实际支出** 选项。 如果选择它，将对未过帐的文档（如待处理的供应商发票）进行耗时的预算控制计算。
