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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 5ee2d132f0b23ceec2a79ee6b0ee33862d6a0518
ms.contentlocale: zh-cn
ms.lasthandoff: 04/25/2017


---

# <a name="financial-dimensions"></a>财务维度

[!include[banner](../includes/banner.md)]


本文说明财务维度的不同类型，以及如何设置。

使用”财务维度“页创建可用作帐户共享图的帐户段的财务维度。 有两类财务维度，自定义维度和实体支持的维度。 自定义维度在法人之间共享，并且值由用户输入和维护。 实体支持的维度是在系统的其他地方定义值的维度，如客户或商店。 有些实体支持的维度在法人间共享，有些实体支持的维度则特定于公司。 

在您创建了财务维度之后，使用”财务维度值“页分配附加属性给每个财务维度。 

尽管在 Microsoft Dynamics 365 for Operations 中您可以不创建法人而是使用财务维度代表法人，但财务维度并不能用于满足法人的运营或业务需要。 将 Microsoft Dynamics 365 for Operations 中的单位间核算功能设计成仅满足由每个交易记录所创建的会计条目。 

在将财务维度设置为法人之前，评估您的业务流程中的以下区域以确定此设置是否为您的组织工作：

-   库存
-   财务维度和法人之间的销售和采购
-   计算和申报销售税
-   操作报告

局限性的例子包括以下内容：

-   您只可以以法人身份使用销售纳税仅功能，但是不可以凭财务维度使用此功能。
-   某些报告没有财务维度，因此，您不能通过财务维度来申报，除非对这些报表做出修改。

**自定义维度** 

若要创建用户定义的财务维度，在”使用以下来源中的值“字段中，选择 &lt;自定义维度&gt;。 您还可以指定科目掩码以限制您为维度值输入的金额和信息类型。 您可以输入保持不变的每个维度值的信息，例如的字符的字母或连字符。 还可以输入数字标志 (\#) 和和符号 (&) 作为每次要更改的字母和数字的占位符创建维度值。 使用一个数字标志 (\#) 作为编号占位符和符号 (&) 作为信函的占位符。 

**示例** 

若要限制维度值到 CC 和三个数字，您输入 CC-\#\#\# 作为格式掩码。 只有在“使用以下来源中的值”字段中选择 &lt;自定义维度&gt; 后，此字段才可用。 

**实体支持的维度** 

若要创建实体支持的财务维度，在”使用以下来源中的值“字段中，选择财务维度所基于的系统定义的实体。 从此选择创建财务维度值。 例如，若为项目创建维度值，请选择“项目”。 为每个项目名称将创建维度值。 维度值页显示实体的值，如果特定于公司，则为值的公司。 

**激活维度** 

“启用财务维度”更新带有财务维度名称的表格，并移除已删除的维度。 在启用财务维度前，您可以输入维度值，但是财务维度在启用前不能在任何位置消耗。 例如，您不能将财务维度添加到科目结构，直接财务维度已启用。 单击”启动“将更新”更改“状态的所有维度。 

**交易记录** 

”文本翻译“页让您可以输入为所选财务维度以不同语言显示的文本。 在”主科目翻译“页中，您可以输入为主科目以不同语言显示的文本。 

**法人覆盖** 

并非所有维度对所有法人均有效，部分维度可能只与特定时段相关。 在此情况中，”法人覆盖“部分可用于确定维度应处于暂停状态的公司，谁是所有者，以及维度有效的时段。






