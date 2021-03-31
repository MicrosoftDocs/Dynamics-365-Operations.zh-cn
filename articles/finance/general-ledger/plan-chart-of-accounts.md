---
title: 计划您的会计科目表
description: 本主题提供将帮助您为您的组织计划会计科目表的信息。
author: aprilolson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 29e5328043a4259b464b272983e11061ade1724c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230362"
---
# <a name="plan-your-chart-of-accounts"></a>计划您的会计科目表

[!include [banner](../includes/banner.md)]

本主题提供将帮助您为您的组织计划会计科目表的信息。

若要跟踪和维护组织的财务信息，您可以设置会计科目表。 会计科目表是定义一个财务框架的帐户的集合。 若要进一步跟踪这些科目中的交易记录，可添加细分市场。 这些细分市场称为财务维度。 例如，支出帐户可能包括名为“部门”、“成本中心”和“用途”的财务维度。 用户定义的规则确定财务维度如何附加到主科目和其他财务维度以及如何输入交易记录。 这些用户定义的规则称为科目结构和高级规则。

会计科目表是法人的总帐科目的结构性列表。 此列表用于为主管机构和所有者准备财务报表。 这些科目首先将分组为不同科目类型，然后进一步合并为更大的类别。 在最一般的级别上，科目按利润和成本（营业科目）以及资产和负债（余额科目）进行分类。

会计科目表可由组织中的法人共享和使用。 法人使用的会计科目表在 **分类帐** 页中定义。

以下是在您计划您的组织的会计科目表的结构时必须考虑的若干因素：

- 您的组织所在的国家或地区的报告要求
- 您的法人的报告要求
- 外部组织和您的组织都需要的规范的程度

在 **会计科目表** 页创建会计科目表。 可以从 **会计科目表** 页或 **主科目** 页创建主科目。 您的主科目不应使用用作会计科目表分隔符的任何特殊字符。 否则，您可能遇到不稳定性，或者可能在输入科目和维度的组合时必须使用查找或对话框。 有关详细信息，请参阅[创建主科目](tasks/create-main-account.md)。

> [!NOTE]
> 在 Dynamics 365 for Finance and Operations 版本 8.0（2018 年 4 月）中，可从 **总帐参数** 页修改会计科目表分隔符。

最好是将主科目与主科目类别链接，以便您可以利用默认财务报表，而不必进行任何修改。 因此，您可以迅速并轻松地设计和维护报表。

在 **配置科目结构** 页创建科目结构。 科目结构定义有效组合。 这些组合和主科目一起形成了会计科目表。 有关详细信息，请参阅[创建科目结构](tasks/create-account-structures.md)。

**法人覆盖**

并非所有主科目对所有法人均有效，部分主科目可能只与特定时段相关。 在这种情况下，您可以使用 **法人替代** 部分识别应为其暂停主科目的公司、所有者以及维度有效的期间。 共享级别的替代不能比法人级别的替代更加严格。

有关详细信息，请参阅以下主题：

- [财务维度](financial-dimensions.md)
- [创建和分配高级规则结构](tasks/create-assign-advanced-rule-structures.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]