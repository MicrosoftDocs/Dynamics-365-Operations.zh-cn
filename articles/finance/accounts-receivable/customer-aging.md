---
title: 客户帐龄分析表
description: 客户帐龄分析表显示应收客户余额，按日期间隔或帐龄期间排序。
author: JodiChristiansen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9291299e0b2ee040bc25ef21237a73c3bc0ea412
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995655"
---
# <a name="customer-aging-report"></a>客户帐龄分析表 

**客户帐龄** 分析表显示应收客户余额，按日期间隔或帐龄期间排序。

生成此分析表时，显示下列默认参数。 可使用这些参数筛选将在分析表中显示的数据。 有关详细信息，请参阅[设置收款](set-up-collections.md)。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>字段</p></th>
<th><p>说明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>计费分类</strong></p></td>
<td><p>选择要包括到分析表中的一个或多个计费分类。</p>
<div class="alert">

**注意：** 只有选择了<STRONG>公共部门</STRONG> Configuration Key 后，此控制才可用。</P>


</div></td>
</tr>
<tr class="even">
<td><p><strong>包括没有计费分类的交易记录</strong></p></td>
<td><p>如果选中此复选框，则未获分配计费分类的所有交易都将显示在分析表上。</p>
<div class="alert">

**注意：** 只有选择了<STRONG>公共部门</STRONG> Configuration Key 后，此控制才可用。</P>

</div></td>
</tr>
<tr class="odd">
<td><p><strong>帐龄截至日期</strong></p></td>
<td><p>输入当前帐龄时段使用的日期。</p></td>
</tr>
<tr class="odd">
<td><p><strong>截至该天余额</strong></p></td>
<td><p>输入要查看客户余额的日期。 这也称作交易的截止日期。</p></td>
</tr>
<tr class="even">
<td><p><strong>开始日期</strong></p></td>
<td><p>输入要包括在分析表中的第一个期间间隔或帐龄期间内的日期。</p></td>
</tr>
<tr class="odd">
<td><p><strong>条件</strong></p></td>
<td><p>选择分析表基于的日期类型。</p>
<ul>
<li><p><strong>交易日期</strong> – 交易的过帐日期。 例如，这可能是用于计算截止日期所依据的发票日期。</p></li>
<li><p><strong>截止日期</strong> – 付款期限中规定的交易的截止日期。</p></li>
<li><p><strong>单据日期</strong> – 计算截止日期所依据的用户定义的单据日期。</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>帐龄期间定义</strong></p></td>
<td><p>选择帐龄期间定义。 如果您选择帐龄期间定义，则不使用<strong>间隔</strong>字段。</p>
<p>具有六个以上帐龄期间的帐龄期间定义不可在打印的分析表上使用。</p>
<div class="alert">

**注意：** 您可以在<STRONG>帐龄期间定义</STRONG>页面上设置帐龄期间。</P>


</div></td>
</tr>
<tr class="odd">
<td><p><strong>打印帐龄期间描述</strong></p></td>
<td><p>选择<strong>是</strong>以在分析表中每个帐龄期间列的顶部包括帐龄期间描述。 选择<strong>否</strong>以打印分析表，而无需列标题。</p></td>
</tr>
<tr class="even">
<td><p><strong>间期</strong></p></td>
<td><p>通过输入每个期间中的天或月单位数来定义要使用的期间。 例如，若要按周查看帐龄信息，请在此字段中输入 7 并在<strong>天/月</strong>字段中选择<strong>天</strong>。</p>
<div class="alert">

**注意：** 只有当您未选择帐龄期间定义时，才能使用在此字段中输入的信息。 否则，在帐龄期间定义上定义打印方向。</P>


</div></td>
</tr>
<tr class="odd">
<td><p><strong>天/月</strong></p></td>
<td><p>选择单位<strong>天</strong>或<strong>月</strong>，它用于定义<strong>间隔</strong>字段中的期间。</p></td>
</tr>
<tr class="even">
<td><p><strong>打印方向</strong></p></td>
<td><p>选择是否计算余额，是为过去还是将来期间打印帐龄分析表。 相对于<strong>余额截止日期</strong>字段中选择的日期评估日期。 选择<strong>倒推</strong>以显示过去期间的信息。 选择<strong>正推</strong>以显示将来期间的信息。</p>
<div class="alert">
  
<STRONG>注意：</STRONG>只有当您未选择帐龄期间定义时，才能使用在此字段中输入的信息。</P>


</div></td>
</tr>
<tr class="odd">
<td><p><strong>明细</strong></p></td>
<td><p>选择以列出在分析表上显示的余额所涉及的交易。</p></td>
</tr>
<tr class="even">
<td><p><strong>包括以交易记录币种表示的金额</strong></p></td>
<td><p>选择以包括除以记帐币种表示的金额之外，还包括以交易币种表示的金额。 如果未选中此复选框，则分析表上的金额仅以记帐币种显示。</p></td>
</tr>
<tr class="odd">
<td><p><strong>负数余额</strong></p></td>
<td><p>选择以包括余额为负数的客户帐户。</p></td>
</tr>
<tr class="even">
<td><p><strong>排除零余额科目</strong></p></td>
<td><p>选择以排除余额为零的客户帐户。</p></td>
</tr>
<tr class="odd">
<td><p><strong>付款定位</strong></p></td>
<td><p>选择以显示尚未结算的付款。 这些都显示在分析表的第一列中。</p></td>
</tr>
</tbody>
</table>

