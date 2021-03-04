---
title: 财务维度和过帐
description: 在计划和设置会计科目表时，必须考虑过帐单据或日记帐时，各组件如何协同工作。 这些组件包括科目结构、高级规则和平衡与固定维度。 本主题介绍各组件的定义及其协同工作方式。
author: aprilolson
manager: AnnBe
ms.date: 08/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerChartofAccounts,DimensionDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: e65d371486d53d0fe4f039da68fbb4dcc35074d1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440716"
---
# <a name="financial-dimensions-and-posting"></a>财务维度和过帐 

[!include [banner](../includes/banner.md)]

在计划和设置会计科目表时，必须考虑过帐单据或日记帐时，各组件如何协同工作。 这些组件包括科目结构、高级规则和平衡与固定维度。 本主题介绍各组件的定义及其协同工作方式。

## <a name="chart-of-accounts-and-financial-dimension-components"></a>会计科目表和财务维度组件

基于规则的丰富系统用于定义主科目和财务维度值的有效组合。 此部分简介各组件的功能及其位置。

### <a name="account-structures"></a>科目结构

设置分类帐时，需要科目结构。 必须至少定义和启用一个科目结构，并且必须将其分配给分类帐。 科目结构中必须包含主科目。 可以定义最适合业务的细分市场顺序。 定义主科目后，系统可以确定所用科目结构。 通过将主科目放在结构的首位或靠前位置，可以帮助限制值，还可以帮助系统将已知的最后一个有效值作为默认值应用。 科目结构中还可以有最多 10 个财务维度。 科目结构定义哪些维度值在与其他值的组合中有效。 还定义是否必须输入维度值。

### <a name="advanced-rules"></a>高级规则

设置会计科目表时，高级规则是可选组件。 可以根据需要向科目结构添加任意数量的高级规则。 高级规则通常用于处理满足特定条件时必须跟踪更多财务维度的场景。 例如，如果使用路费科目，可能需要跟踪更多信息，如员工出差参加的活动。 如果有多个高级规则，则基于其名称按字母顺序应用。 只能将规则添加的细分市场应用到科目结构的细分市场后。

### <a name="balancing-dimension"></a>平衡维度

可以选择定义平衡财务维度。 在 **分类帐** 页中，可以定义应平衡的财务维度。 然后，只要将交易过帐到该财务维度，系统都将自动创建条目并过帐，以便平衡该财务维度。

### <a name="defaultfixed-financial-dimensions-on-the-main-account"></a>主科目中的默认/固定财务维度

默认维度来自各种位置，如主记录（如客户或供应商记录）、单据抬头和主科目。 本主题重点介绍主科目中按法人分类的默认维度。 可以为分类帐的所有科目结构中使用的各财务维度定义主科目具有 **非固定** 还是 **固定** 值。 如果财务维度 **非固定**，则使用默认值，但不能改写该值。 此行为适用于系统中的所有默认值，即使来自主记录的默认值也不例外。 如果财务维度设置为 **固定** 值，无论该值与默认值来自同一位置还是用户输入的。都将始终应用该值。

## <a name="order-in-which-default-dimensions-are-applied-during-posting"></a>过帐期间默认维度的应用顺序

大家经常好奇各种组件的运行顺序。 请务必了解默认维度的应用顺序，因为此行为影响你设置时采用的方法。

> [!NOTE]
> 此信息仅适用于应用程序中默认维度的应用。 如果通过使用 Microsoft Excel 或数据管理 Framework 导入数据，则行为不同。

### <a name="example-1"></a>示例 1

**科目结构**

| 主科目            | 业务单位           | 部门              | 成本中心             |
|-------------------------|-------------------------|-------------------------|-------------------------|
| 允许所有值。 | 允许所有值。 | 允许所有值。 | 允许所有值。 |

**主科目**

| 主科目 | 姓名          | 法人 | 部门                                 |
|--------------|---------------|--------------|--------------------------------------------|
| 401100       | 产品销售 | USMF         | 固定 - 022 销售和市场营销部门 |

下图显示主科目 401100 中设置的默认固定维度。

[![默认财务维度](./media/default-dimensions.png)](./media/default-dimensions.png)

在这个非常基础的示例中，将输入一个普通日记帐，其中的部门维度设置为使用默认值 **023**（操作）。 将输入一个会计科目并过帐。 下图显示总帐标题中的默认财务维度。

[![普通日记帐](./media/general-journal.png)](./media/general-journal.png)

该日记帐标题中的默认维度将导致在销售科目行中默认应用部门 023。 下图显示普通日记帐行，其中应用了来自标题的默认维度值 **023**。

[![日志凭证](./media/journal-voucher.png)](./media/journal-voucher.png)

但是，过帐该行时，将应用固定维度，并将该行过帐到部门 022。 下图显示过帐的凭证，其中为销售科目应用了固定维度。

[![凭证交易记录](./media/voucher-transactions.png)](./media/voucher-transactions.png)

### <a name="example-2"></a>示例 2

此示例使用与第一个示例相同的设置。 但是，将再添加一个组件，并将部门维度用作平衡维度。 在下图中，**部门** 设置为 USMF 分类帐的平衡财务维度。

[![分类帐](./media/ledger.png)](./media/ledger.png)

使用相同的日记帐标题设置并过帐同一个交易时，将首先应用固定维度。 然后应用平衡逻辑以帮助确保每个部门都有一个平衡的条目。 下图显示应用固定维度后包含平衡条目的凭证交易。

[![凭证交易记录](./media/voucher-transactions2.png)](./media/voucher-transactions2.png)

### <a name="example-3"></a>示例 3

在此示例中，我们将添加一条高级规则。 这条高级规则指定，如果使用销售科目 401100 和部门 022（销售和市场营销），系统应再跟踪一个名称为“客户”的细分市场。

因为顺序，此示例非常重要。 科目结构在输入主科目后确定。 如果希望设置科目结构，系统可以确定主科目、业务单位、部门和成本中心相关。 此时尚未触发高级规则，因为过帐期间为日记帐凭证应用默认维度之前，不应用固定维度。 在下图中，无“客户”细分市场，因为尚未满足高级规则的条件。

[![会计科目](./media/drop-down.png)](./media/drop-down.png)

过帐将失败，因为流程结束时应用了固定维度。 维度验证确定如果主科目为 401100 且部门为 022，则需要“科目”细分市场。 验证错误导致不能执行过帐。 下图显示维度验证确定“客户”为必需的细分市场后显示的消息。

[![消息详细信息](./media/message.png)](./media/message.png)

在此示例中，必须覆盖默认值，这样才会触发高级规则，并且可以输入“客户”细分市场。 但是，此解决方案并非始终可行，一些用户甚至不会注意到过帐规则。 因此，设置会计科目表时务必了解默认维度的应用顺序。

若要实现此示例中的目标，可通过多种方法更改配置。 例如，可为销售科目创建新的科目结构，并在该结构中加入“科目”细分市场。 还可以在现有科目结构中添加更多行，并指定主科目和有效的部门值。 然后，在额外的客户结构中，可以发现包含“客户”细分市场的单独销售科目科目结构非常有用。

## <a name="additional-resources"></a>其他资源 

下面的部分资源涉及我们的软件的早期版本。 但是，许多有关默认维度的应用的信息和许多概念在早期版本中是一样的，这些参考材料仍然有效。

[单位间核算的平衡日记帐](example-balanced-journals-interunit-accounting.md)

[计划您的会计科目表](plan-chart-of-accounts.md) 

[“在 AX 2012 中计划会计科目表”博客](https://blogs.msdn.microsoft.com/axsa/2014/06/12/planning-your-chart-of-accounts-in-ax-2012-part-1-of-7/) - 此链接是由七个部分组成的系列中的第一部分。

[会计分配中的维度默认设置](https://blogs.msdn.microsoft.com/ax_gfm_framework_team_blog/2013/12/16/dimension-defaulting-in-accounting-distributions-part-1-introduction/)

[维度框架中的维度默认设置](https://docs.microsoft.com/archive/blogs/ax_gfm_framework_team_blog/dimension-defaulting-part-1-financial-dimensions-discovery)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]