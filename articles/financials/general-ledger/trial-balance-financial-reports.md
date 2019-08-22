---
title: 试算平衡表财务报表
description: 本文介绍试算平衡表的默认报表。 它还介绍这些报表的关联构建块，以及如何修改这些报表以符合您的业务需求。
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 842eecf68f5a658be6cdc7a05c365a18fe7d91dc
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846091"
---
# <a name="trial-balance-financial-reports"></a>试算平衡表财务报表

[!include [banner](../includes/banner.md)]

本文介绍试算平衡表的默认报表。 它还介绍这些报表的关联构建块，以及如何修改这些报表以符合您的业务需求。 

<a name="default-trial-balance-reports"></a>默认试算平衡表
-----------------------------

三个试算平衡表可用于 Microsoft Dynamics 365 for Finance and Operations 的财务报表。

| 默认报表                                 | 作用                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 试算平衡表(明细) - 默认               | 提供所有帐户的余额信息，包括借方和贷方余额，以及这些余额的净值，还有交易记录日期、凭证和日记帐描述。                  |
| 试算平衡表汇总 – 默认                | 提供所有帐户的余额信息，包括期初和期末余额，以及借方和贷方余额还有其净差额。                                        |
| 各年汇总试算余额表 – 默认 | 提供所有帐户的余额信息，包括期初和期末余额，以及借方和贷方余额还有当年和过去一年的净差额。 |

## <a name="building-blocks"></a>构建基块
试算平衡表财务报表使用以下构建基块。

| 默认报表                                 | 行定义          | 列定义                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| 试算平衡表(明细) - 默认               | 试算平衡表 - 默认 | 试算平衡表(明细) - 默认               |
| 试算平衡表汇总 – 默认                | 试算平衡表 - 默认 | 试算平衡表汇总 - 默认                |
| 各年汇总试算余额表 – 默认 | 试算平衡表 - 默认 | 各年汇总试算余额表 - 默认 |

### <a name="row-definition"></a>行定义

行定义，试算平衡表 – 默认，包含拉取所有主科目的单行 因此，任何人都可以生成报表，而不必进行任何修改。 在您查看报表时，您深化到单个行可以查看有关每个科目的详细信息。 您可以修改行定义，以便包括更多详细信息。 若要修改“试算平衡表 – 默认”行定义，以便包括所有科目的行，请执行以下步骤。

1.  单击**编辑**，然后单击**从维度插入行**。 **从维度插入行**命令允许您选择希望哪些维度在您的行定义中。 对于此行定义，则使用**主科目**。
2.  确保**主科目**包含所有符号 (&)，然后单击**确定**。

行定义现在包含默认法人的所有主科目。

### <a name="column-definition"></a>列定义

每个试算平衡表使用不同的列定义。 这些列定义包含不同的列类型以提供不同级别的详细信息和财务数据。

-   **试算平衡表 – 默认列类型：**
    -   **DESC** – 行定义的描述
    -   **ACCT** – 科目代码
    -   **ATTR (3)** – 属性：
        -   交易记录日期
        -   凭证
        -   日记帐描述
    -   **FD** – 只包含借方的财务数据
    -   **FD** – 只包含贷方的财务数据
    -   **CALC** – 净差额
-   **试算平衡表汇总 – 默认列类型：**
    -   **ACCT** – 科目代码
    -   **DESC** – 行定义的描述
    -   **ATTR** – 属性：
        -   凭证
    -   **FD** – 期初余额财务数据
    -   **FD** – 只包含借方的财务数据
    -   **FD** – 只包含贷方的财务数据
    -   **CALC** – 净差额
    -   **CALC** – 期末余额
-   **各年汇总试算余额表 – 默认：**
    -   **ACCT** – 科目代码
    -   **DESC** – 行定义的描述
    -   **ATTR** – 属性
        -   凭证
    -   **FD** – 当前年度的期初余额财务数据
    -   **FD** – 只包含当前年度的借方的财务数据
    -   **FD** – 只包含当前年度的贷方的财务数据
    -   **CALC** – 净差额
    -   **CALC** – 期末余额
    -   **FD** – 只包含上一年度的借方的财务数据
    -   **FD** – 只包含上一年度的贷方的财务数据



<a name="additional-resources"></a>其他资源
--------

[财务申报](financial-reporting-getting-started.md)

[查看财务报表](view-financial-reports.md)

[Dynamics 财务申报博客](https://blogs.msdn.com/b/dynamics_financial_reporting/)



