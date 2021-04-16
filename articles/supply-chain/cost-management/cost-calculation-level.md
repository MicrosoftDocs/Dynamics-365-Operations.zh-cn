---
title: 成本计算级别
description: 本主题介绍名为“成本计算级别”的物料清单 (BOM) 级别。 此物料清单级别从计算中排除了生产订单和批次订单。
author: AndersGirke
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f7cde239107528a6bc2aeb0e424d024d4f3fb2a6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839479"
---
# <a name="cost-calculation-level"></a>成本计算级别

名为 **成本计算级别** 的物料清单 (BOM) 级别从计算中排除生产订单和批次订单。 系统在成本核算版本中运行成本计算时将使用此级别。 在重新计算和库存结转等流程中，系统改用 **成本核算级别** 物料清单级别。

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