---
title: 资产负债表财务报表
description: 本文介绍资产负债表的默认报表。 还介绍这些报表的关联构建块。
author: jinniew
ms.date: 10/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinanicalReports
audience: Application User
ms.reviewer: twheeloc
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4aad297f401143388d682da175a6b14727a8f2f0
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2022
ms.locfileid: "9643815"
---
# <a name="balance-sheet-financial-reports"></a>资产负债表财务报表

[!include [banner](../includes/banner.md)]

本文介绍资产负债表的默认报表。 还介绍这些报表的关联构建块。 

## <a name="default-balance-sheet-reports"></a>默认资产负债表

有两个默认的资产负债表。 在一个报表中，这些部分堆积起来。 在另一个报表中，这些部分是并行的。

| 默认报表                       | 作用                                                                                                                           |
|--------------------------------------|--------------------------------------------------------------------------------------|
| 资产负债表 – 默认              | 提供组织的年度财务状况视图。                    |
| 资产负债表和收入报表并排 – 默认 | 并列提供组织的年度财务状况视图。 |

## <a name="building-blocks"></a>构建基块
资产负债表财务报表使用以下构建基块。

| 默认报表                       | 行定义                       | 列定义             |
|--------------------------------------|--------------------------------------|-------------------------------|
| 资产负债表 - 默认              | 资产负债表 - 默认              | YTD 和差异 - 默认    |
| 资产负债表和收入报表并排 – 默认 | 资产负债表和收入报表并排 – 默认 | 本年迄今列 - 默认 |

### <a name="row-definition"></a>行定义

两个资产负债表的行定义包含传统资产负债表中每个部分的部分。 并排报表包括分列符，以使债务和所有者权益显示在资产旁边。 主科目类别维度用于构建两个行定义。 因此，任何人都可以生成报表，而不必进行任何修改。

### <a name="column-definition"></a>列定义

列定义包含不同的列类型以提供不同级别的详细信息和财务数据。

-   **YTD 和差异 – 默认列类型：**
    -   **DESC** – 行定义的描述
    -   **FD** – 当前年度的本年迄今财务数据
    -   **FD** – 上一年度的本年迄今财务数据
    -   **CALC** – 从今年减去去年所得的差异

<!-- -->

-   **本年迄今列 – 默认：**
    -   **DESC** – 行定义的描述
    -   **FD** – 当前年度的本年迄今财务数据



## <a name="additional-resources"></a>其他资源

[财务报告概览](financial-reporting-getting-started.md)

[查看财务报表](view-financial-reports.md)

[Dynamics 财务申报博客](https://blogs.msdn.com/b/dynamics_financial_reporting/)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
