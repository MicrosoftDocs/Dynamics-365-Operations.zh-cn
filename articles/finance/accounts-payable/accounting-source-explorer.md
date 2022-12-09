---
title: 会计源资源管理器
description: 本文提供有关会计源资源管理器页面的信息，您可用此信息来进行总帐会计条目后源信息的详细分析。
author: RyanCCarlson2
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AccountingSourceExplorer
audience: Application User
ms.reviewer: kfend
ms.custom: 15391
ms.assetid: 57b95899-7298-43c0-8034-45b5d993cbf2
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5bd5580dc0be37ec89e6c7934b47c7d5593d8716
ms.sourcegitcommit: 5f8f042f3f7c3aee1a7303652ea66e40d34216e3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806425"
---
# <a name="accounting-source-explorer"></a>会计源资源管理器

[!include [banner](../includes/banner.md)]

本文提供有关 **会计源资源管理器** 页面的信息，您可用此信息来进行总帐会计条目后源信息的详细分析。

**会计源资源管理器** 页面显示源信息。 您可以使用此页面作为单独的工具或分析总帐会计条目后的详细信息。 例如，您可以使用此页面获取线索余额中余额的或凭证交易记录的最详细来源信息。 您可以使用 **导出到 MS Excel** 功能进一步划分和切分 Microsoft Excel 中的信息（例如，在数据透视表或在数据透视表报表中）。

**会计源资源管理器** 页面始终显示与总帐显示的每个会计科目相同的总金额（例如，在试算平衡表中）。 在试算平衡表中，可以在单独的列显示段。 只需选择适合的财务维度集。 

您可以使用参数定义该分析的日期间隔。 此功能类似于试算平衡表中的功能。

对于使用原始凭证框架的所有凭证，**会计源资源管理器** 页面基于会计分配显示附加信息，如果适用，还显示项目会计分配。 此信息包括 **货币金额类型**、**项目**、**活动**、**类别** 和 **行属性** 值。 下面是您可以执行的分析的一些示例：

- 采购订单和供应商发票之间的差异，因为每个差异由货币金额类型表示，如费用差异
- 每个项目、业务单位和主科目的计费和非计费工时和支出

对于使用原始凭证引用标识概念的原始凭证，**会计源资源管理器** 页面显示更多详细信息，如 **客户**、**供应商**、**工作人员**、**产品**、**数量**、**单位文本** 和 **描述** 值。 下面是您可以执行的分析的一些示例：

- 每个业务单位的酒店支出和会计期间酒店品牌，基于支出报表
- 每个供应商、产品、部门的折扣

对于这些凭证，您还可以导航到 **会计源资源管理器** 页面的实际原始凭证。

> [!NOTE]
> 从版本 10.0.31 开始，功能管理中提供了一个新的 **会计源资源管理器高级筛选** 功能。 此功能取代了 **更新** 按钮，以提供更强大的高级查询体验，类似于 **凭证交易** 页面上提供的功能。 高级筛选器允许您筛选与您在 **凭证交易查询** 页面上找到的字段类似的字段，如 **分类帐科目**、**业务单位**、**成本中心** 和 **部门**。 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
