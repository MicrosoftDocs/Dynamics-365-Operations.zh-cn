---
title: "计划您的会计科目表"
description: "本文提供将帮助您为您的组织计划会计科目表的信息。"
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9f4d7fdd8cfa7a540fce219f6ae4792e57dfbe44
ms.openlocfilehash: 34425ecd4b78a134c92a2282576d0d7967d870b3
ms.lasthandoff: 03/31/2017


---

# <a name="plan-your-chart-of-accounts"></a>计划您的会计科目表

本文提供将帮助您为您的组织计划会计科目表的信息。

若要跟踪和维护组织的财务信息，您可以设置会计科目表。 会计科目表是定义一个财务框架的帐户的集合。 要进一步跟踪这些帐户中的交易记录，可以添加名为财务维度的段。 例如，支出帐户可能包括名为“部门”、“成本中心”和“用途”的财务维度。 名为科目结构和高级规则的用户定义的规则确定财务维度如何附加到主科目和其他财务维度以及如何输入交易记录。 

会计科目表是法人的总账科目的结构性列表。 此列表用于为主管机构和所有者准备财务报表。 这些科目将分组为不同科目类型，然后进一步合并为更大的类别。 在最一般的级别上，科目按利润和成本（营业科目）以及资产和负债（余额科目）进行分类。 

会计科目表可由组织中的法人共享和使用。 使用法人的会计科目表在会计** **页定义。 

以下是在您计划您的组织的会计科目表的结构时必须考虑的若干因素：

-   您的组织所在的国家/地区的报告要求
-   您的法人的报告要求
-   外部组织和您的组织都需要的规范的程度

在**会计科目表**页创建会计科目表。 主科目可以从**会计科目表**页或**主科目**页创建。 您的主科目不应使用用作会计科目表分隔符的任何特殊字符。 如果您具有与您的会计科目表分隔符相同的特殊字符，您可能遇到不稳定性或在输入帐户和维度组合时需要始终使用查找或浮出。 

最好是将主科目与主科目类别链接，以便您可以利用默认财务报表，而不必进行任何修改。 因此，您可以迅速并轻松地设计和维护报表。 

使用**配置科目结构**页创建科目结构。 科目结构定义有效组合。 这些组合和主科目一起形成了会计科目表。 

**Legal entity overrides** 

并非所有的主科目为法人所有有效，其中某些可能仅与特定时段相关。 在此情况中，”法人覆盖“部分可用于确定主科目应处于暂停状态的公司，谁是所有者，以及维度有效的时段。 共享级别的覆盖不能比法人级别的覆盖更加严格。

有关详细信息，请参阅 dimensions.md [(财务)] 的财务维度。


