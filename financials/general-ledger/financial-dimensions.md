---
title: "财务维度"
description: "本文说明财务维度的不同类型，以及如何设置。"
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 25871
ms.assetid: af54621c-c8be-4b72-b6df-dcf886c40ce4
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9f4d7fdd8cfa7a540fce219f6ae4792e57dfbe44
ms.openlocfilehash: f849b98cac88d182875aca88aaf04cd3575ed99f
ms.lasthandoff: 03/31/2017


---

# <a name="financial-dimensions"></a>财务维度

本文说明财务维度的不同类型，以及如何设置。

使用”财务维度“页创建可用作帐户共享图的帐户段的财务维度。 有两类财务维度，自定义维度和实体支持的维度。 自定义维度在法人之间共享，并且值由用户输入和维护。 实体支持的维度是在系统的其他地方定义值的维度，如客户或商店。 有些实体支持的维度在法人间共享，有些实体支持的维度则特定于公司。 

在您创建了财务维度之后，使用”财务维度值“页分配附加属性给每个财务维度。 

尽管您可以在 Microsoft Dynamics 365 中使用法人代表财务维度，不创建工序的法人，财务维度未设计用于处理法人的运营或业务需求。 单位之间核算功能在工序 365 的 Microsoft Dynamics 中设计解决由创建的每个交易记录会计条目。 

在将财务维度设置为法人之前，评估您的业务流程中的以下区域以确定此设置是否为您的组织工作：

-   库存
-   财务维度和法人之间的销售和采购
-   计算和申报销售税
-   操作报告

局限性的例子包括以下内容：

-   您只可以以法人身份使用销售纳税仅功能，但是不可以凭财务维度使用此功能。
-   某些报告没有财务维度，因此，您不能通过财务维度来申报，除非对这些报表做出修改。

**Custom dimensions** 

创建一种用户定义的财务维度，按"字段的值使用自定义，请 &lt; 选择"维度 &gt;。 您还可以指定科目掩码以限制您为维度值输入的金额和信息类型。 您可以输入保持不变的每个维度值的信息，例如的字符的字母或连字符。 还可以输入数字符号 (\#) 和与号 (&)。每次将更改的字母和数字的占位符。创建维度值 将数字符号 (\#) 作为占位符为编号和与号 (&) 作为占位符为字母。 

**示例** 

若要限制维度值。信件 CC 的项目编号，则您输入 CC-\#\#\#，格式掩码。 只有当，您选择自定义维度。从 &lt; 字段的 &gt; 值时，使用此字段才可用。 

**实体在中返回的维度** 

要创建实体返回了财务维度，按"字段的值使用，选择一系统定义的财务维度。根据实体 从此选择创建财务维度值。 例如，若为项目创建维度值，请选择“项目”。 为每个项目名称将创建维度值。 维度值页显示实体的值，如果特定于公司，则为值的公司。 

** **激活维度 

“启用财务维度”更新带有财务维度名称的表格，并移除已删除的维度。 在启用财务维度前，您可以输入维度值，但是财务维度在启用前不能在任何位置消耗。 例如，您不能将财务维度添加到科目结构，直接财务维度已启用。 单击”启动“将更新”更改“状态的所有维度。 

**Translations** 

文本转换页允许您输入所选财务维度的不同语言中显示的文本。 在”主科目翻译“页中，您可以输入为主科目以不同语言显示的文本。 

**Legal entity overrides** 

并非所有的维度。所有法人有效，其中某些可能仅与特定时段相关。 在此情况中，”法人覆盖“部分可用于确定维度应处于暂停状态的公司，谁是所有者，以及维度有效的时段。




