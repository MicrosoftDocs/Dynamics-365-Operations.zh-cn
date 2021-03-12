---
title: 为工程更改管理建立通用值
description: 本主题介绍如何建立用于工程更改管理的各部分中的参数的通用值。
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductParameters, EngChgEcmSeverityTable, EngChgEcmSeverityRuleSet, EngChgEcmSeverityLookup,EngChgEcmSeverityChart,EngChgEcmRequestSeverityChart,EngChgEcmPriorityTable, EngChgEcmPriorityLookup, EngChgEcmPriorityChart, EngChgEcmMaterialDisposition, EngChgEcmEH
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 86de050ef4110e3485a77099440f3402e46cc498
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/29/2020
ms.locfileid: "4423452"
---
# <a name="establish-common-values-for-engineering-change-management"></a>为工程更改管理建立通用值

[!include [banner](../includes/banner.md)]

设置工程更改管理时，必须建立多个值集合，它们将用于填充用户界面 (UI) 的其他部分中的下拉列表。 您应该根据生产的产品类型和特定的业务需求指定这些值。

## <a name="engineering-change-categories"></a>工程更改类别

使用工程更改类别组织工程更改订单，以便它们更易于管理和审查。 例如，您可能会发现它在设置工作流时很有用（根据类别），特定部门必须审查提出的更改。 因此，工程更改订单包括 **类别** 字段。

若要建立在公司中使用的工程更改类别的集合，请转到 **工程更改管理 \> 设置 \> 工程更改管理 \> 工程更改类别**。 然后，您可以使用操作窗格上的按钮添加、删除和编辑值，并将它们按照应在列出它们的下拉列表中显示的顺序排列。

## <a name="engineering-change-priorities"></a>工程更改优先级

使用工程更改优先级来指示工程更改订单的重要性或紧急程度。 它们可以帮助您跟踪工程更改订单的重要性，以便您可以轻松确定应首先处理哪些订单以及处理速度。

若要建立在公司中使用的工程更改优先级的集合，请转到 **工程更改管理 \> 设置 \> 工程更改管理 \> 工程更改优先级**。 然后，您可以使用操作窗格上的按钮添加、删除和编辑值，并将它们按照应在列出它们的下拉列表中显示的顺序排列。

## <a name="engineering-change-reasons"></a>工程更改原因

工程更改原因指示更改顺序中更改的原因或性质。

若要建立在公司中使用的工程更改原因的集合，请转到 **工程更改管理 \> 设置 \> 工程更改管理 \> 工程更改原因**。 然后，您可以使用操作窗格上的按钮添加、删除和编辑值，并将它们按照应在列出它们的下拉列表中显示的顺序排列。

## <a name="material-disposal-codes"></a>物料处置代码

使用材料处置代码对成品中使用的材料或必须以特定方式处置或需要进行某些处理的组件进行分类，然后才能将它们添加到常规垃圾箱中。 将相关产品添加到工程更改订单时，您可以分配处置代码作为更改详细信息的一部分。

若要建立在公司中使用的材料处置代码的集合，请转到 **工程更改管理 \> 设置 \> 工程更改管理 \> 材料处置代码**。 然后，您可以使用操作窗格上的按钮添加、删除和编辑值，并将它们按照应在列出它们的下拉列表中显示的顺序排列。

## <a name="received-customer-approval"></a>收到的客户审核

为特定客户设计产品时，通常必须先验证设计和规格，然后才能将产品设置为就绪。 **获得客户审批** 字段可让您指示产品在客户审批流程中的哪个阶段和/或是否已获得审批。

若要建立在公司中使用的获得客户审批值的集合，请转到 **工程更改管理 \> 设置 \> 工程更改管理 \> 获得客户审批**。 然后，您可以使用操作窗格上的按钮添加、删除和编辑值，并将它们按照应在列出它们的下拉列表中显示的顺序排列。

## <a name="engineering-change--environmental-health-and-safety-codes"></a>工程更改 – 环境健康和安全法规

如果在制造产品时必须考虑任何标准的环境健康和安全法规或公司特定的法规或程序，您可以使用环境健康和安全法规对其进行定义。 在工程更改订单中，您可以在编辑受影响产品的详细信息时指示哪些法规适用于产品的制造。

若要建立在公司中使用的健康和安全值的集合，请转到 **工程更改管理 \> 设置 \> 工程更改管理 \> 环境健康和安全法规**。 然后，您可以使用操作窗格上的按钮添加、删除和编辑值，并将它们按照应在列出它们的下拉列表中显示的顺序排列。

## <a name="engineering-change-severities"></a>工程更改严重性

使用工程更改严重性来指示对工程更改订单中的产品应用的影响级别。

若要建立在公司中使用的工程更改严重性的集合，请转到 **工程更改管理 \> 设置 \> 工程更改管理 \> 工程更改严重性**。 然后，您可以使用操作窗格上的按钮添加、删除和编辑值，并将它们按照应在列出它们的下拉列表中显示的顺序排列。

您可以建立适用于您创建的每个严重性级别的规则。 有关如何分配这些规则的详细信息，请参见下一部分。

## <a name="engineering-change-severity-rule-sets"></a>工程更改严重性规则集

使用工程更改严重性规则集来建立一组规则，可用于根据受影响产品中的更改类型自动计算更改订单的严重性。 若要使用严重性规则，请打开 **工程更改管理参数** 页面，然后将 **严重性规则** 字段设置为 *计算* 或 *自动计算*。

当系统评估严重性时，它将按照规则在页面上显示的从上到下的顺序处理规则。 对于要选择且已建立其优先级的规则，必须满足规则集中的所有规则。

若要设置适用于您定义的每个更改严重性级别的规则，请转到 **工程更改管理 \>设置 \> 工程更改管理 \> 工程更改严重性规则集**。 然后按照以下步骤之一操作。

- 若要创建新规则集，在操作窗格上选择 **新建**，然后按照此部分后面的说明设置字段。
- 若要编辑现有规则集，在列表窗格中选择它，在操作窗格上选择 **编辑**，然后按照此部分后面的说明设置字段。
- 若要删除现有规则集，在列表窗格中选择它，然后在操作窗格上选择 **删除**。
- 若要重新排列规则集的列表，在列表窗格中选择规则集，然后在操作窗格上使用 **向上** 和 **向下** 按钮来重新放置它。

对于每个规则集，设置以下字段：

- **严重性** – 选择严重性级别以为其建立规则。 使用 **工程更改严重性** 页面创建和命名级别。 （有关详细信息，请参阅上一部分。）

使用 **规则** 快速选项卡上的按钮添加或删除当前严重性设置的规则。 每个规则都有 **规则** 字段和 **名称** 字段。 规则由系统建立，并指示产品可以具有的更改类型。 名称指示更改的类型。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]