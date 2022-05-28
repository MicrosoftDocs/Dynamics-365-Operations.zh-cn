---
title: 成本计算级别
description: 本主题介绍名为“成本计算级别”的物料清单 (BOM) 级别。 此物料清单级别从计算中排除了生产订单和批次订单。
author: JennySong-SH
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 563d866c93e9205914f633f3435ef4b46f85b814
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2022
ms.locfileid: "8679546"
---
# <a name="cost-calculation-level"></a>成本计算级别

[!include [banner](../includes/banner.md)]

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