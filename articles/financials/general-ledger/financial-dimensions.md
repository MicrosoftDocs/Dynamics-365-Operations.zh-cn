---
title: "财务维度"
description: "本主题介绍财务维度的不同类型以及如何设置。"
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ems.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3950dc3fcd1e293802c88bf2616a27e139b48399
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="financial-dimensions"></a>财务维度

[!include[banner](../includes/banner.md)]

本主题说明财务维度的不同类型以及如何设置。

使用**财务维度**页可创建可用作会计科目表的科目段的财务维度。 有两类财务维度：自定义维度和实体支持的维度。 自定义维度在法人之间共享，并且值由用户输入和维护。 对于实体支持的维度，其值在系统的其他地方进行定义，如客户或商店实体。 有些实体支持的维度在法人间共享，而有些实体支持的维度则特定于公司。 

在您创建了财务维度之后，使用**财务维度值**页给每个财务维度分配附加属性。 

您可以使用财务维度代表法人。 您不必在 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 中创建实体。 但是，财务维度不用来解决法人的运营或业务需求。 将 Finance and Operations 中的单位间核算功能设计成仅满足由每个交易记录所创建的会计条目。 

在将财务维度设置为法人之前，评估您的业务流程中的以下区域以确定此设置是否适用于您的组织：

- 库存
- 财务维度和法人之间的销售和采购
- 计算和申报销售税
- 操作报告

这是一些限制：

- 您只可以以法人身份使用销售纳税仅功能，但是不可以凭财务维度使用此功能。
- 有些报表不包括财务维度。 因此，要按财务维度进行报告，您可能必须修改报表。

## <a name="custom-dimensions"></a>自定义维度

若要创建用户定义的财务维度，在**使用以下来源中的值**字段中，选择**&lt;自定义维度&gt;**。 您还可以指定科目掩码以限制您为维度值输入的金额和信息类型。 您可以输入保持不变的每个维度值的信息，例如字母或连字符 (-)。 还可以输入数字标志 (\#) 和和符号 (&) 作为每次要更改的字母和数字的占位符创建维度值。 使用一个数字标志 (\#) 作为编号占位符和符号 (&) 作为信函的占位符。 只有在**&lt;使用以下来源中的值&gt;**字段中选择**自定义维度**后，用于格式掩码的字段才可用。

**示例**

若要限制维度值到“CC”和三个数字，输入 **CC-\#\#\#** 作为格式掩码。

## <a name="entity-backed-dimensions"></a>实体支持的维度

若要创建实体支持的财务维度，在**使用以下来源中的值**字段中，选择财务维度所基于的系统定义的实体。 随后将从此实体创建财务维度值。 例如，要为项目创建维度值，请选择**项目**。 将为每个项目名称将创建维度值。 **财务维度值**页显示实体的值。 如果这些值是公司特定的，则页面上还显示公司。

## <a name="activating-dimensions"></a>激活维度

在您启用财务维度时，表进行更新，使其包含财务维度的名称。 删除被移除的维度。 启用财务维度前，您可以输入维度值。 不过，在启用财务维度前，无法在任何地方使用财务维度。 例如，到启用财务维度以前，您不能将财务维度添加到科目结构。 在您单击**启用**后，所有维度更新并显示状态更改。 

## <a name="translations"></a>翻译

在**文本翻译**页，可为所选财务维度输入不同语言的文本。 在**主科目翻译**页，可为主科目输入不同语言的文本。 

## <a name="legal-entity-overrides"></a>法人覆盖

并非所有的维度都对所有法人有效。 此外，某些维度可能仅针对特定的期间有关。 在这些情况下，您可以使用**法人覆盖**部分指定将为其暂停维度的公司、所有者以及维度有效的期间。

## <a name="deleting-financial-dimensions"></a>删除财务维度

为了帮助维护数据的引用完整性，很少删除财务维度。 如果要删除财务维度，则评估以下条件：

- 财务维度是否在已过帐或未过帐的交易记录或任何类型的维度值组合上使用？
- 财务维度是否在任何活动的科目结构、高级规则结构或财务维度集中使用？
- 财务维度是否是默认维度集成格式的一部分？
- 财务维度是否已设置为默认维度？

如果满足任何条件，则不能删除财务维度。


有关详细信息，请参阅以下主题：
- [定义财务维度](tasks/define-financial-dimensions.md)
- [维护财务维度默认模板](tasks/maintain-financial-dimension-default-templates.md)

