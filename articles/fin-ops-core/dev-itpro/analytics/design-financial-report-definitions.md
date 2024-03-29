---
title: 财务报表设计器中的报表定义
description: 本文提供了有关报表定义的信息。
author: aprilolson
ms.date: 11/22/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.form: FinancialReports
ms.openlocfilehash: 2ffef335c694af56486ccd7738818c4edda49b9e
ms.sourcegitcommit: d27fef61593c6d1e9e26d5c9fad21411bc52fabc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/23/2022
ms.locfileid: "9802524"
---
# <a name="report-definitions-in-financial-report-designer"></a>财务报表设计器中的报表定义

[!include [banner](../includes/banner.md)]

本文提供了有关报表定义的信息。 报表定义是使用行定义、列定义和可选报告结构树定义创建报表的报表组件（或构建基块）。 报表定义还提供自定义报表的选项和设置。 

报表定义是使用行定义、列定义和可选报告结构树定义创建报表的报表组件（或构建基块）。 报表定义还提供了可用于自定义报表的选项和设置。 在定义行定义和列定义之后，必须在报表定义中合并这些定义。 此时，您还将定义定义的其他方面，如详细程度和报表日期。 然后您可保存和生成报表。 财务报告提供下列详细级别：

- 财务
- 财务和科目
- 财务、科目和交易记录

但是，根据数据在 Microsoft Dynamics ERP 系统中的存储方式，可能无法在报表中使用交易记录明细。

## <a name="create-a-report-definition"></a>创建报表定义
1. 在 Report designer 的 **文件** 菜单上，单击 **新建**，然后选择 **报表定义**。
2. 在 **报表**、**输出和分配**、**页眉和页脚** 以及 **设置** 选项卡上指定相应信息。

## <a name="contents-of-a-report-definition"></a>报表定义的内容
下表说明了报表定义中的各个选项卡以及如何使用这些信息。

<table>
<thead>
<tr>
<th>选项卡</th>
<th>说明</th>
</tr>
</thead>
<tbody>
<tr>
<td>报表</td>
<td>创建报表、配置报表或修改现有报表。</td>
</tr>
<tr>
<td>输出和分发</td>
<td>更改报表的输出类型和目标。</td>
</tr>
<tr>
<td>页眉和页脚</td>
<td>定义报表的页眉和页脚并设置其格式。 例如，您可向页眉或页脚添加文本或图像。 对于图像，财务报告支持 .bmp、.jpg 和 .png 文件。 您还可添加自动图文集代码以插入其他信息（如公司名称、报表名称或页码）。</td>
</tr>
<tr>
<td>设置</td>
<td>指定报表定义设置，例如以下设置：
<ul>
<li>金额格式和化整金额</li>
<li>设置明细报表的格式</li>
<li>设置报告树的格式</li>
<li>生成异常报表</li>
<li>指定币种转换</li>
<li>小计和筛选会计科目明细</li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>其他资源

[财务申报](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
