---
title: "客户过帐模板"
description: "客户过帐模板控制将客户交易记录过帐到总帐。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: da750645612c2a0a7650edfd933d707618d9f9ce
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="customer-posting-profiles"></a>客户过帐模板

[!include[banner](../includes/banner.md)]


客户过帐模板控制将客户交易记录过帐到总帐。

<a name="customer-posting-profiles"></a>客户过帐模板
-------------------------

客户过帐模板能让您将总帐科目和文档设置分配给所有客户、一组客户或单个客户。 这些设置将在您创建销售订单、普通发票、现金付款、催款单、利息单和注销时使用。 对于某些交易记录，您可以选择不同于在此页面中为交易记录设置的模板的其他过帐模板，并且您选择的过帐模板优先。 

默认过帐模板是在“应收账款参数”页上的“分类帐”和“销售税”快速选项卡中定义的。 然后，默认过帐模板自动包括到新文档的标题中，在那里您可以根据需要将其更改为不同的过帐模板。

您还可以将过帐定义与“交易记录过帐定义”页中的交易记录过帐类型关联。 过帐定义控制到总帐的客户交易记录过帐，而不是过帐模板。

## <a name="creating-a-posting-profile"></a>创建过帐模板
指定在使用所选过帐模板对交易记录进行过帐时所使用的会计科目。 为所选的过帐模板选择帐户编码；只要可能，还选择帐户/组编号。 在过帐过程中，定位每个交易记录的最合适过帐模板的方法是搜索针对性最强的帐户编码、帐号或组编号组合，其优先级如下：

| **“帐户编码”**字段值 | **“帐户/组编号”**字段值            | 搜索优先级 |
|------------------------------|-------------------------------------------------|-----------------|
| **表**                    | 特定的客户帐户                       | 1               |
| **组**                    | 分配到客户的客户组 | 2               |
| **全部**                      | 空白                                           | 3               |

如果您希望所有客户交易记录具有相同的过帐模板，请在“帐户编码”字段中使用“全部”，从而仅建立一个过帐模板。 指定以下值设置您的过帐模板：

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
<td>输入过帐模板的代码。 例如，您可以创建两个过帐模板以便用本国币种获取客户余额的一个科目，用外币获取客户余额的另一个科目。 您可以对本国币种调用一个科目，对外币调用另一个科目。</td>
</tr>
<tr class="even">
<td><strong>描述</strong></td>
<td>输入过帐模板的描述。 这仅用于当您在该页面中查看过帐模板时，更好地标识它。</td>
</tr>
<tr class="odd">
<td><strong>帐户编码</strong></td>
<td>指定该过帐模板是应用于单个客户、一组客户还是所有客户：
<ul>
<li><strong>表</strong> – 过帐模板应用于单个客户。 在“帐户/组编号”字段中选择客户帐户。</li>
<li><strong>组</strong> – 过帐模板应用于客户组。 在“帐户/组编号”字段中选择客户组。</li>
<li><strong>全部</strong> – 过帐模板应用于所有客户。 将“帐户/组编号”字段留空。</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>帐户/组编号</strong></td>
<td>如果在“帐户编码”字段中选择了“表”，请选择与该过帐模板相关的客户的帐号。 如果选择了“组”，请选择客户组。 如果选择“全部”，则将此字段保留为空。</td>
</tr>
<tr class="odd">
<td><strong>汇总科目</strong></td>
<td>选择将用作与该过帐模板相关的客户的客户汇总科目。</td>
</tr>
<tr class="even">
<td><strong>结算科目</strong></td>
<td>选择用于现金流量预测的流动性会计科目。 此字段只有在启用现金流量预测时才出现。</td>
</tr>
<tr class="odd">
<td><strong>销售税预付款</strong></td>
<td>选择预付款的销售税帐户。
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="注意" alt="Note" id="alert_note" class="cl_IC101471" /><strong>注释</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>使用“应收账款参数”页指定在将付款标记为预付款过帐模板时使用的过帐模板。</td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><strong>折扣负债科目</strong></td>
<td>选择折扣负债科目。</td>
</tr>
<tr class="odd">
<td><strong>催款单序列</strong></td>
<td>选择的催款单序列的标识，以用于过帐模板分配到的客户。</td>
</tr>
<tr class="even">
<td><strong>利息代码</strong></td>
<td>选择利息代码，以用于为过帐模板分配到的客户计算利息。</td>
</tr>
</tbody>
</table>

### 

### <a name="table-restrictions"></a>**表限制**

对于具有所选过帐模板的交易记录，指定交易记录是否将自动结算、是否计算利息、是否签发催款单。 您还可以选择对具有所选过帐模板的交易记录进行结算时所使用的帐户。

指定以下值设置您的过帐模板：

| 字段                 | 描述                                                                                                                                                                                                                                        |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **结算**        | 选择此开关可启用具有此过帐模板的交易记录的自动结算。 如果清除此开关，您必须通过使用“结算未结交易记录”页或“输入客户付款”页来手动结算交易记录。 |
| **兴趣**          | 如果利息应对使用此模板的客户帐户的未清余额进行计算，则选择此开关。 如果清除此开关，将不为这些客户计算利息。                                           |
| **催款单** | 如果催款单应为使用此模板的客户帐户而生成，则选择此开关。 如果清除此开关，将不为这些客户生成催款单。                                                 |
| **关闭**             | 选择在您关闭具有此过帐模板的交易记录时希望更改为的过帐模板。 在完全结算某一交易记录后，该交易记录被视为已关闭。                                                                           |



有关详细信息，请参阅[客户付款概览](../cash-bank-management/tasks/customer-payment-overview.md)。


