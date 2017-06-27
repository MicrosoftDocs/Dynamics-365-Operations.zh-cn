---
title: "财务报表设计器中的报表定义"
description: "本文提供了有关报表定义的信息。 报表定义是使用行定义、列定义和可选报告结构树定义创建报表的报表组件（或构建基块）。 报表定义还提供自定义报表的选项和设置。"
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: Management Reporter, Core
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 86b527b72ef0c9af71e70fe280bcdfe3992a36b1
ms.contentlocale: zh-cn
ms.lasthandoff: 05/25/2017


---

# <a name="report-definitions-in-financial-report-designer"></a>财务报表设计器中的报表定义

[!include[banner](../includes/banner.md)]


本文提供了有关报表定义的信息。 报表定义是使用行定义、列定义和可选报告结构树定义创建报表的报表组件（或构建基块）。 报表定义还提供自定义报表的选项和设置。 

报表定义是使用行定义、列定义和可选报告结构树定义创建报表的报表组件（或构建基块）。 报表定义还提供了可以用于自定义报表的其他选项和设置。 在定义行定义和列定义后，您必须在报表定义中组合它们。 此时，您还将定义定义的其他方面，如详细程度和报表日期。 然后您可保存和生成报表。 财务报告提供下列详细级别：

-   财务
-   财务和科目
-   财务、科目和交易记录

但是，根据数据在 Microsoft Dynamics ERP 系统中的存储方式，交易记录明细在报表中可能不可用。

## <a name="create-a-report-definition"></a>创建报表定义
1.  在报表设计器的**“文件”**菜单上，单击**“新建”**，然后选择**“报表定义”**。
2.  在**“报表”**、**“输出和分配”**、**“页眉和页脚”**以及**“设置”**选项卡上指定相应信息。

## <a name="contents-of-a-report-definition"></a>报表定义的内容
下表描述报表定义中的选项卡以及这些信息的使用方式。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>制表符</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>报表</td>
<td>创建报表、配置报表或修改现有报表。</td>
</tr>
<tr class="even">
<td>输出和分配</td>
<td>更改报表的输出类型和目标。</td>
</tr>
<tr class="odd">
<td>页眉和页脚</td>
<td>为报表定义页眉和页脚并设置页眉和页脚的格式。 例如，您可向页眉或页脚添加文本或图像。 对于图像，财务报告支持 .bmp、.jpg 和 .png 文件。 您还可添加自动图文集代码以插入其他信息（如公司名称、报表名称或页码）。</td>
</tr>
<tr class="even">
<td>设置</td>
<td>指定报表定义设置，如下列设置：
<ul>
<li>格式和化整金额</li>
<li>设置明细报表的格式</li>
<li>设置报告结构树的格式</li>
<li>生成异常报表</li>
<li>指定货币转换</li>
<li>对科目详细信息进行小计和筛选</li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a>请参阅
--------

[财务申报](financial-reporting-intro.md)




