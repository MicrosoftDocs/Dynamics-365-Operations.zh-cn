---
title: 按分录的销售税明细报表
description: 此主题说明如何使用按分录的销售税明细报表查看和打印有关为其计算销售税的分录的信息。
author: ericwang
manager: Ann Beebe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-19
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 438a640124e778b839c660f5e161efa22c319af0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440605"
---
# <a name="sales-tax-specification-by-ledger-transaction-report"></a>按分录的销售税明细报表
[!include [banner](../includes/banner.md)]

此主题说明如何使用 **按分录的销售税明细** 报表查看和打印有关为其计算销售税的分录的信息。

## <a name="tax-accounts-vs-non-tax-accounts"></a>纳税科目与非纳税科目

**按分录的销售税明细** 报表显示纳税科目和非纳税科目的税收交易记录。 这些科目按以下方法分类：

- **纳税科目** – 在过帐税务交易记录时，科目被视为纳税科目，并且 **销售税** 日记帐行中的主科目也是纳税科目，如应付销售税科目或应收销售税科目。
- **非纳税科目** – 在过帐税务交易记录时，科目被视为非纳税科目，并且原始交易记录中的主科目也是非纳税科目，如收入科目或费用科目。

对于纳税科目，报表中的 **来源**、**应收销售税** 和 **应付销售税** 列显示 **0**（零）。 对于非纳税科目，这些列显示金额。

## <a name="filtering-the-data-on-the-report"></a>筛选报表中的数据

生成此报表时，以下默认字段可用。 可使用这些字段筛选此报表中显示的数据。

| 字段                      | 说明 |
|----------------------------|-------------|
| 日期                       | 使用 **开始** 和 **结束** 部分中的字段为税务交易记录定义日期范围。 |
| 主科目               | 使用 **开始** 和 **结束** 部分中的字段为主科目定义范围。 |
| 增值税代码             | 使用 **开始** 和 **结束** 部分中的字段为销售税代码定义范围。 |
| 分组                   | 选择应该按会计科目还是销售税代码为报表分组。 |
| 小计(按销售税代码) | 如果将此选项设置为 **是**，则按销售税代码显示小计。 |
| 仅合计                | 如果将此选项设置为 **是**，则仅显示合计。 |
| 仅主科目         | 如果将此选项设置为 **是**，则报表中仅包含主科目。 |

## <a name="showing-only-non-tax-accounts-on-the-report"></a>报表中仅显示非纳税科目

若要在报表中仅显示非纳税科目，请设置筛选条件，如星号 (\*)，如下图中所示。

![报表显示非纳税科目](media/taxspecperledgertrans.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]