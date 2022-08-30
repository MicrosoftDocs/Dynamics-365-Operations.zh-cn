---
title: 成本计算级别
description: 本文介绍名为“成本计算级别”的物料清单 (BOM) 级别。 此物料清单级别从计算中排除了生产订单和批次订单。
author: JennySong-SH
ms.date: 08/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: e63a868696e36c1d4f5d19ea87bdf4d682c39f8c
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334946"
---
# <a name="cost-calculation-level"></a>成本计算级别

[!include [banner](../includes/banner.md)]

名为 **成本计算级别** 的物料清单 (BOM) 级别从计算中排除生产订单和批次订单。 系统在成本核算版本中运行成本计算时将使用此级别。 在重新计算和库存结转等流程中，系统改用 **成本核算级别** 物料清单级别。

## <a name="turn-the-cost-calculation-level-feature-on-or-off"></a>打开或关闭成本计算级别功能

要使用此功能，必须为您的系统打开它。 从 Supply Chain Management 版本 10.0.29 开始，此功能默认开启。 管理员可以通过在 [功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区搜索 *成本计算级别* 功能来打开或关闭此功能。

## <a name="example-scenario"></a>示例场景

以下简单场景显示了 **成本计算级别** 物料清单级别和 **成本核算级别** 物料清单级别。

您有三个产品：A、B 和 C。产品 C 是产品 B 的组件，产品 B 是产品 A 的组件。

- **成本核算级别** 分配以下物料清单级别：

    - **产品 A：** 0
    - **产品 B：** 1
    - **产品 C：** 2

- **成本计算级别** 分配以下物料清单级别：

    - **产品 A：** 0
    - **产品 B：** 1
    - **产品 C：** 2

随后将创建产品 C 的生产订单，并将产品 A 添加到生产订单物料清单。 估计订单后，物料清单级别将以以下方式更新：

- **成本核算级别** 分配以下物料清单级别：

    - **产品 B：** 1
    - **产品 C：** 2
    - **产品 A：** 3

- **成本计算级别** 分配以下物料清单级别：

    - **产品 A：** 0
    - **产品 B：** 1
    - **产品 C：** 2

此行为可确保对生产订单物料单的更改不会影响后续的成本计算。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]