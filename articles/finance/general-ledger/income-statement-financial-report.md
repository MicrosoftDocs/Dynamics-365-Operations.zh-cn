---
title: 收入报表财务报表
description: 本文介绍默认收入报表。 还介绍此报表的关联构建块。
author: jcart1106
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: twheeloc
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e9a1f20ed5e2a84e0d18101ede46ffffef4230c7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868451"
---
# <a name="income-statement-financial-report"></a>收入报表财务报表

[!include [banner](../includes/banner.md)]

本文介绍默认收入报表。 还介绍此报表的关联构建块。 

## <a name="default-income-statement-report"></a>默认收入报表

| 默认报表             | 作用                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| 收入报表 – 默认 | 提供组织当前期间以及本年迄今收益率的视图。 |

## <a name="building-blocks"></a>构建基块
收入报表财务报表使用以下构建基块。

| 默认报表             | 行定义                     | 列定义          |
|----------------------------|------------------------------------|----------------------------|
| 收入报表 - 默认 | 收入报表汇总 - 默认 | 定期和 YTD - 默认 |

### <a name="row-definition"></a>行定义

行定义，收入报表汇总 – 默认，包含每个传统收入报表部分的一个部分。 主科目类别维度用于创建此行定义。 因此，任何人都可以生成报表，而不必进行任何修改。

### <a name="column-definition"></a>列定义

列定义包含不同的列类型以提供不同级别的详细信息和财务数据。

-   **定期和 YTD – 默认列类型：**
    -   **DESC** – 行定义的描述
    -   **FD** – 当前期间的财务数据
    -   **FD** – 本年迄今的财务数据



## <a name="additional-resources"></a>其他资源

[财务报告概览](financial-reporting-getting-started.md)

[查看财务报表](view-financial-reports.md)

[Dynamics 财务申报博客](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
