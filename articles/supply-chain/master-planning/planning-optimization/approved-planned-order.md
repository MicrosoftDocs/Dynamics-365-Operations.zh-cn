---
title: 审核计划订单
description: 此主题介绍计划优化中支持的计划订单的审核。
author: ChristianRytt
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 6c215a89403f16336caae5c62cde6df469c4091c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825883"
---
# <a name="approve-planned-orders"></a>审核计划订单

[!include [banner](../../includes/banner.md)]

此主题介绍如何在计划优化中更新计划订单的状态。

请注意，审核计划订单为最终从计划订单创建确定订单过程中的可选步骤。 建议批准修改后的计划订单，否则将忽略编辑，并替换为下一个运行计划。

![计划订单流](media/approved-planned-orders-1.png)

**状态** 字段可帮助您使用以下值来确定进度：

- **未处理：** 当主计划生成计划订单时，该计划订单状态为 *未处理*。 此状态的计划订单将在下一次计划运行期间删除。
- **已完成：** 如果您决定不确认计划订单，可以将状态更改为 *已完成* 以表示您已完成对该计划订单的评估。 请注意，系统同等对待 *未处理* 和 *已完成* 状态。
- **已批准：** 如果要保留编辑或计划确定计划订单，请将状态更改为 *已批准*。 主计划将状态为 *已批准* 的计划订单视为已确定和预期供应，所以不会在随后的主计划运行期间修改或删除这些订单。 为此，计划逻辑会在主计划期间将 *已审核* 的计划订单从旧计划版本复制到新计划版本。 请注意，*已批准* 的计划订单在特定主计划内仅视为供应。

您可以从 **主计划** 工作区、**计划订单** 列表或 **计划生产订单**、**计划采购订单** 和 **计划转移** 列表中管理计划订单。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]