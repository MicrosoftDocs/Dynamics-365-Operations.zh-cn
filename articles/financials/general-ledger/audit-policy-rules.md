---
title: "审计策略规则"
description: "您可以使用审核策略对支出报告、供应商发票和采购订单做出评估，从而确保它们都符合您所创建的策略规则。 根据您指定的作业安排，所有与审计策略相关的规则都是以批模式运行的。  每个策略过账都是某个策略规则类型的实例。 对于每个策略规则类型，一次仅有一个策略规则可以有效。"
author: ryansandness
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 12991
ms.assetid: 8d787017-71dc-418f-b8c2-4ea9763d9978
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 6bebe9ce83c4b979ffbb7c86ef67ad03a650e0c2
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="audit-policy-rules"></a>审计策略规则

[!include [banner](../includes/banner.md)]

您可以使用审核策略对支出报告、供应商发票和采购订单做出评估，从而确保它们都符合您所创建的策略规则。 根据您指定的作业安排，所有与审计策略相关的规则都是以批模式运行的。  每个策略过账都是某个策略规则类型的实例。 对于每个策略规则类型，一次仅有一个策略规则可以有效。 

<a name="queries-and-query-types"></a>查询和查询类型
-----------------------

当您创建了审核策略规则时，您要首先选择一个策略规则类型。 该策略规则类型指定 Application Object Tree (AOT) 查询用作创建策略规则的起点。 它还指定用于策略规则的查询类型。 该查询确定了策略规则进行评估的原始凭证。 它还指定了原始凭证中选择文件供审核时使用的标识法人和日期的字段。 查询类型控制查询页和“审计策略规则”页中的默认字段。 下表显示了对审核策略规则可用的查询类型。

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>查询类型</th>
<th>用途</th>
<th>更多信息</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>条件</td>
<td>根据指定值评估原始凭证属性。</td>
<td></td>
</tr>
<tr class="even">
<td>聚合</td>
<td>根据聚合数值策略规则评估多个原始凭证或原始凭证行。</td>
<td></td>
</tr>
<tr class="odd">
<td>抽样</td>
<td>随机选择原始凭证的指定百分比来评估策略违规情况。</td>
<td>当您选择此选项时，使用“审计策略规则”页指定随机选择供审核凭证的百分比。</td>
</tr>
<tr class="even">
<td>复制</td>
<td>评估原始凭证以确定是否在指定的字段中包含重复的条目。</td>
<td>当您选择此选项时，使用“审计策略规则”页指定针对重复条目对凭证进行评估时要添加到凭证选择日期范围的天数。</td>
</tr>
<tr class="odd">
<td>列表搜索</td>
<td>针对特定条目评估原始凭证。</td>
<td>查询的根凭证定义了正被审核的凭证。 查询必须是包括 Dirpartytable 表的参考的列表查询。 此选项只能与以下 AOT 查询一起使用：
<ul>
<li><span class="ui">AuditPolicyExpenseList</span>（支出报表监控的员工）</li>
<li><span class="ui">AuditPolicyPurchList</span>（采购订单监控的供应商）</li>
<li><span class="ui">AuditPolicyVendInvoiceList</span>（供应商发票监控的供应商）</li>
</ul>
当您选择此选项时，在“审计策略规则”页中指定要监控的实体。</td>
</tr>
<tr class="even">
<td>关键字搜索</td>
<td>评估原始凭证以确定它们是否包含某些特定的单词。</td>
<td>当您选择此选项时，在“审计策略规则”页中输入要查找的字词。 “审计策略规则”页中也包含了选项让您指定表和字段用来评估您输入的单词。</td>
</tr>
</tbody>
</table>

## <a name="common-parameters"></a>共同参数
某个特定审核策略的所有策略规则共享相同的批处理参数和相同的凭证选择日期范围。 在“审计策略规则”页中为该策略指定这些参数。



<a name="additional-resources"></a>其他资源
--------

[审计政策违规记录和案例](audit-policy-violations-cases.md)
[定义原始单据的审计策略](tasks/define-audit-policies-source-documents.md)



