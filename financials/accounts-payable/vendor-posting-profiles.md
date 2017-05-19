---
title: "供应商过帐模板"
description: "供应商过帐模板控制将供应商交易记录过帐到总帐。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: VendPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 3354fb9a724c46c296e7cc9fad179a50704520bf
ms.contentlocale: zh-cn
ms.lasthandoff: 04/25/2017


---

# <a name="vendor-posting-profiles"></a>供应商过帐模板

[!include[banner](../includes/banner.md)]


供应商过帐模板控制将供应商交易记录过帐到总帐。

<a name="vendor-posting-profiles"></a>供应商过帐模板
-----------------------

供应商过帐模板能让您将总帐科目和文档设置分配给所有供应商、一组供应商或单个供应商。 这些设置将在您创建采购订单、供应商发票和现金付款时使用。 对于某些交易记录，您可以选择不同于在此页面中为交易记录设置的模板的其他过帐模板，并且您选择的过帐模板优先。 默认过帐模板是在“应付帐款参数”页上的“分类帐”和“销售税”快速选项卡中定义的。 然后，默认过帐模板自动包括到新文档的标题中，在那里您可以根据需要将其更改为不同的过帐模板。

您还可以将过帐定义与“交易记录过帐定义”页中的交易记录过帐类型关联。 过帐定义控制到总帐的供应商交易记录过帐，而不是过帐模板。

## <a name="creating-a-posting-profile"></a>创建过帐模板
### <a name="setup"></a>**设置**

指定在使用所选过帐模板对交易记录进行过帐时所使用的会计科目。 为所选的过帐模板选择帐户编码；只要可能，还选择帐户/组编号。 在过帐过程中，定位每个交易记录的最合适过帐模板的方法是搜索针对性最强的帐户编码、帐号或组编号组合，其优先级如下：

| **“帐户编码”**字段值 | **“帐户/组编号”**字段值        | 搜索优先级 |
|------------------------------|---------------------------------------------|-----------------|
| **表**                    | 特定供应商帐户                     | 1               |
| **组**                    | 分配给供应商的供应商组 | 2               |
| **全部**                      | 空白                                       | 3               |

如果您希望所有供应商交易记录具有相同的过帐模板，请在“帐户编码”字段中使用“全部”，从而仅建立一个过帐模板。 指定以下值设置您的过帐模板：

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>字段</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>过帐模板</strong></td>
<td>输入过帐模板的代码。 例如，您可以创建两个过帐模板以便用本国币种获取供应商余额的一个科目，用外币获取供应商余额的另一个科目。 您可以对本国币种调用一个科目，对外币调用另一个科目。</td>
</tr>
<tr class="even">
<td><strong>描述</strong></td>
<td>输入过帐模板的描述。</td>
</tr>
<tr class="odd">
<td><strong>帐户编码</strong></td>
<td>指定过帐模板是应用于特定供应商、一组供应商还是所有供应商：
<ul>
<li><strong>表</strong> – 过帐模板应用于单个供应商。 在“帐户/组编号”字段中选择供应商帐户。</li>
<li><strong>组</strong> – 过帐模板应用于供应商组。 在“帐户/组编号”字段中选择供应商组。</li>
<li><strong>全部</strong> – 过帐模板应用于所有供应商。 将“帐户/组编号”字段留空。</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>帐户/组编号</strong></td>
<td>如果在“帐户编码”字段中选择了“表”，请选择与该过帐模板相关的供应商的帐号。 如果选择“组”，则选择一个供应商组。 如果选择“全部”，则将此字段保留为空。</td>
</tr>
<tr class="odd">
<td><strong>汇总科目</strong></td>
<td>选择将用作该过帐模板所关联到的供应商的汇总科目的会计科目。
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Note" alt="Note" id="alert_note" class="cl_IC101471" /><strong>注意</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>如果“使用过帐定义”开关在“总帐参数”页中处于选定状态，则会使用供应商发票的交易记录过帐定义，而不是汇总科目。</td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><strong>结算科目</strong></td>
<td>选择用于现金流量预测的流动性会计科目。 只有启用现金流量预测时，此字段才可用。</td>
</tr>
<tr class="odd">
<td><strong>销售税预付款</strong></td>
<td>选择预付款的销售税帐户。
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Note" alt="Note" id="alert_note" class="cl_IC101471" /><strong>注意</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>在付款标记为预付款时使用的过帐模板在“应付帐款参数”页的“分类帐和销售税”区域中的“具有预付款日记帐凭证的过帐模板”字段中处于选定状态。</td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><strong>到达</strong></td>
<td>选择有关未审核的供应商发票信息过帐到的会计科目编号。 在发票登记簿日记帐中输入此信息。 例如，在发票登记簿中接收供应商发票时，用户输入与发票有关的最基本信息。 在过帐发票登记簿时，交易记录被过帐到在此处输入的科目以及“对方科目”字段中的科目。 在审核发票时，债务将从“到达”科目转移到供应商汇总科目。</td>
</tr>
<tr class="odd">
<td><strong>对方科目</strong></td>
<td>选择用于抵消通过发票登记簿更新的未核准供应商发票的会计科目。 对方科目充当过帐到到达科目的交易记录的对方科目。 因此，该科目包含还未审核的供应商采购。</td>
</tr>
</tbody>
</table>
 

### <a name="table-restrictions"></a>**表限制**

对于具有所选过帐模板的交易记录，指定交易记录是否将自动结算、是否计算利息、是否签发催款单。 您还可以选择对具有所选过帐模板的交易记录进行结算时所使用的帐户。

指定以下值设置您的过帐模板：

| 字段          | 描述                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **结算** | 选择此选项可启用具有此过帐模板的交易记录的自动结算。 如果清除此选项，您必须通过使用“结算未结交易记录”页来手动结算交易记录。 |
| **取消**     | 如果您希望能够取消具有此过帐模板的交易记录，请选择此选项。                                                                                                               |
| **关闭**      | 选择在您关闭具有此过帐模板的交易记录时希望更改为的过帐模板。 在完全结算某一交易记录后，该交易记录被视为已关闭。                                       |






