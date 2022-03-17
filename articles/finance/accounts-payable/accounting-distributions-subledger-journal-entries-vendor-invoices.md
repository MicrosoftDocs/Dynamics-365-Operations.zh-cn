---
title: 会计分配和供应商发票的日记帐条目
description: 会计分配用于定义将如何对帐金额，例如将如何对帐普通发票中的收入、税金或费用。 普通发票已记入日记帐时，必须对帐的每笔金额都将具有一个或多个会计分配。
author: sunfzam
ms.date: 02/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendEditInvoice
audience: Application User
ms.reviewer: twheeloc
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f10ddf113f59da4800a97a48300ab1310bfb42dd
ms.sourcegitcommit: 9cbff8a2cdeaf606488fb0044b3de4ab4409c9dc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/26/2022
ms.locfileid: "8358158"
---
# <a name="accounting-distributions-and-journal-entries-for-vendor-invoices"></a>会计分配和供应商发票的日记帐条目

[!include [banner](../includes/banner.md)]

会计分配用于定义将如何对帐金额，例如将如何对帐普通发票中的收入、税金或费用。 普通发票已记入日记帐时，必须对帐的每笔金额都将具有一个或多个会计分配。 

## <a name="accounting-distributions"></a>会计分配 

您可以使用“供应商发票”页中的以下按钮查看和修改普通发票的每笔金额的会计分配。
-   **分摊金额**– 查看和修改单独行和任何子行的会计分配，例如税金或费用。 您还可以直接从 **销售税交易记录** 页或 **费用交易记录** 页查看和修改子行的会计分配。
    -   修改普通发票抬头金额，如费用或币种化整金额。
    -   修改供应商发票行金额。
-   **查看分配** – 查看文档中所有行的会计分配。 您无法从此视图修改会计分配。
    -   查看标题和单行金额。

如果供应商发票参考采购订单，才能拆分和修改包含一个物料未库存行的会计分配。 如果供应商发票行不参考采购订单行，还可以删除会计分配。 您不能拆分或删除费用、税和单行折扣行。 您可以修改会计科目，不过，您不能更改金额或百分比。
> [!NOTE]                                                                                                                                 
> 如果父行包含贮存的物料和拆分的会计分配，将自动拆分该子行以与父行的财务维度匹配。 无法进一步拆分或删除子行的会计分配，但根据子行的设置，您可能能够为子行的会计分配修改会计科目。

## <a name="distributing-amounts"></a>分配金额
当您输入普通发票时，每笔金额将按如下分配。

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>供应商发票行的类型</th>
<th>优先级顺序确定默认主科目显示的位置。</th>
<th>优先级顺序确定显示的默认财务维度</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>贮存的产品</td>
<td><ol>
<li>采购订单行的会计分配。</li>
<li>当在<strong>过帐</strong>页选择“产品采购支出”时的<strong>主科目</strong>字段。</li>
</ol></td>
<td><ol>
<li>如果发票行上引用的采购订单行，为采购订单行使用要分配到的科目。</li>
<li>在普通发票行使用默认的财务维度值。</li>
</ol></td>
</tr>
<tr class="even">
<td>采购类别或未库存的物料</td>
<td><ol>
<li>如果发票行上引用的采购订单行，为采购订单行使用要分配到的科目。</li>
<li>当在<strong>过帐</strong>页选择“支出中的采购支出”时的<strong>主科目</strong>字段。</li>
</ol></td>
<td><ol>
<li>如果发票行上引用的采购订单行，为采购订单行使用要分配到的科目。</li>
<li>如果主科目是分配帐户，则使用分配帐户定义中的默认值。</li>
<li>在普通发票行使用默认的财务维度值。</li>
<li>使用来自采购订单行的财务维度值。</li>
<li>使用<strong>会计科目表</strong>页中主科目中的默认财务维度值。</li>
</ol></td>
</tr>
<tr class="odd">
<td>固定资产</td>
<td><ol>
<li>如果发票行上引用的采购订单行，为采购订单行使用要分配到的科目。</li>
<li>如果在<strong>供应商发票</strong>页面的<strong>交易记录类型</strong>字段中的<strong>购置</strong>，在<strong>固定资产过帐模板</strong>页中选择<strong>购置</strong>时的<strong>主科目</strong>字段。</li>
<li>如果在<strong>交易记录类型</strong>字段中选择<strong>购置调整</strong>，在<strong>固定资产过帐模板</strong>页中选择<strong>购置调整</strong>时的<strong>主科目</strong>字段。</li>
</ol></td>
<td><ol>
<li>如果发票行上引用的采购订单行，为采购订单行使用要分配到的科目。</li>
<li>使用来自采购订单行的财务维度值。</li>
<li>使用<strong>会计科目表</strong>页中主科目中的默认财务维度值。</li>
</ol></td>
</tr>
<tr class="even">
<td>项目定义在供应商发票行</td>
<td><ol>
<li>如果发票行上引用的采购订单行，为采购订单行使用要分配到的科目。</li>
<li>如果在<strong>项目组</strong>页的<strong>过帐成本 - 物料</strong>字段中选择了<strong>余额</strong>，在<strong>分类帐记帐设置</strong>页中选择<strong>成本</strong>时的<strong>主科目</strong>字段。</li>
<li>如果在<strong>项目组</strong>页的<strong>过帐成本 - 物料</strong>字段中选择了<strong>损益</strong>，在<strong>分类帐记帐设置</strong>页中选择<strong>成本 - 物料</strong>时的<strong>主科目</strong>字段。</li>
</ol></td>
<td><ol>
<li>如果发票行上引用的采购订单行，为采购订单行使用要分配到的科目。</li>
</ol></td>
</tr>
<tr class="odd">
<td>单行折扣</td>
<td><ol>
<li>如果发票行上引用的采购订单行，为采购订单行使用要分配到的科目。</li>
<li>在<strong>过帐</strong>页中选择<strong>折扣</strong>时的<strong>主科目</strong>字段。</li>
<li>如果没有在过帐模版上、采购订单行上延伸价格的会计分配中定义主折扣科目。</li>
</ol></td>
<td><ol>
<li>如果发票行上引用的采购订单行，为采购订单行使用要分配到的科目。</li>
<li>用于供应商发票行的总价使用来自会计分配的财务维度。</li>
<li>使用来自采购订单行的财务维度值。</li>
<li>使用<strong>会计科目表</strong>页中主科目中的默认财务维度值。</li>
</ol></td>
</tr>
<tr class="even">
<td>在采购订单行的<strong>价格和折扣</strong>选项卡上输入的采购费用</td>
<td><ol>
<li>如果发票行上引用的采购订单行，为采购订单行使用要分配到的科目。</li>
<li>采购订单行延伸价格的会计分配。</li>
</ol></td>
<td><ol>
<li>如果发票行上引用的采购订单行，为采购订单行使用要分配到的科目。</li>
<li>用于供应商发票行的总价使用来自会计分配的财务维度。</li>
</ol></td>
</tr>
<tr class="odd">
<td>行费用</td>
<td><ol>
<li>如果发票行上引用的采购订单行，为采购订单行使用要分配到的科目。</li>
<li>如果在<strong>费用代码</strong>页面的<strong>借方类型</strong>字段中选择了<strong>会计科目</strong>，<strong>费用代码</strong>页的<strong>借方科目</strong>字段。</li>
<li>如果在<strong>费用代码</strong>页面的<strong>借方类型</strong>字段中选择<strong>物料</strong>，延伸价格的会计分配为采购订单行。</li>
<li>如果在<strong>费用代码</strong>页面的<strong>借方类型</strong>字段中选择了<strong>客户/供应商</strong>，<strong>费用代码</strong>页的<strong>贷方科目</strong>字段。</li>
</ol></td>
<td><ol>
<li>如果发票行上引用的采购订单行，为采购订单行使用要分配到的科目。</li>
<li>用于供应商发票行的总价使用来自会计分配的财务维度。</li>
<li>使用来自采购订单行的财务维度值。</li>
<li>使用<strong>会计科目表</strong>页中主科目中的默认财务维度值。</li>
</ol></td>
</tr>
<tr class="even">
<td>满足以下条件的税金：
<ul>
<li>在<strong>总帐参数</strong>页中选择<strong>应用美国税务规则</strong>选项。</li>
</ul></td>
<td><ol>
<li>如果发票行上引用的采购订单行，为采购订单行使用要分配到的科目。</li>
<li>查看费用的延伸价格或会计分配。</li>
</ol></td>
<td><ol>
<li>如果发票行上引用的采购订单行，为采购订单行使用要分配到的科目。</li>
<li>用于供应商发票行的总价使用来自会计分配的财务维度。</li>
<li>使用来自采购订单行的财务维度值。</li>
</ol></td>
</tr>
<tr class="odd">
<td>满足以下条件的税金：
<ul>
<li>在<strong>总帐参数</strong>页中清除<strong>应用美国税务规则</strong>选项。</li>
<li>在<strong>销售税组</strong>页清除销售税组的<strong>销项税</strong>字段。</li>
</ul></td>
<td><ol>
<li>如果税额应退，<strong>分类帐记帐组</strong>页的<strong>应收销售税</strong>字段。</li>
<li>如果增值税金额不应退，费用的延伸价格或会计分配。</li>
</ol></td>
<td><ol>
<li>如果发票行上引用的采购订单行，为采购订单行使用要分配到的科目。</li>
<li>用于供应商发票行的总价使用来自会计分配的财务维度。</li>
<li>使用来自采购订单行的财务维度值。</li>
<li>使用<strong>会计科目表</strong>页中主科目中的默认财务维度值。</li>
</ol></td>
</tr>
<tr class="even">
<td>满足以下条件的税金：
<ul>
<li>在<strong>总帐参数</strong>页中清除“应用美国税务规则”选项。</li>
<li>在<strong>销售税组</strong>页选择销售税组的<strong>销项税</strong>字段。</li>
</ul></td>
<td><ol>
<li>如果税额应退，<strong>分类帐记帐组</strong>页的<strong>应收销售税</strong>字段。</li>
<li>如果税额不应退，<strong>分类帐记帐组</strong>页的<strong>销项税支出</strong>字段。</li>
</ol></td>
<td><ol>
<li>如果发票行上引用的采购订单行，为采购订单行使用要分配到的科目。</li>
<li>用于供应商发票行的总价使用来自会计分配的财务维度。</li>
<li>使用来自采购订单行的财务维度值。</li>
<li>使用<strong>会计科目表</strong>页中主科目中的默认财务维度值。</li>
</ol></td>
</tr>
<tr class="odd">
<td>标头费用</td>
<td><ol>
<li>如果在<strong>费用代码</strong>页面的<strong>借方类型</strong>字段中选择了<strong>会计</strong>科目，<strong>费用代码</strong>页的<strong>借方科目</strong>字段。</li>
<li>如果在<strong>费用代码</strong>页面的<strong>借方类型</strong>字段中选择了<strong>客户/供应商</strong>，<strong>费用代码</strong>页的<strong>贷方科目</strong>字段。</li>
</ol></td>
<td><ol>
<li>如果发票行上引用的采购订单行，为采购订单行使用要分配到的科目。</li>
<li>如果主科目是分配帐户，则使用分配帐户定义中的默认值。</li>
<li>使用供应商发票抬头的财务维度值默认模板。</li>
<li>使用来自采购订单行的财务维度值。</li>
<li>使用<strong>会计科目表</strong>页中主科目中的默认财务维度值。</li>
</ol></td>
</tr>
<tr class="even">
<td>标题折扣</td>
<td><ol>
<li><strong>自动交易记录帐户</strong>页中<strong>供应商发票折扣过帐类型</strong>的<strong>主科目</strong>字段。</li>
</ol></td>
<td><ol>
<li>如果发票行上引用的采购订单行，为采购订单行使用要分配到的科目。</li>
<li>用于供应商发票行的总价使用来自会计分配的财务维度。</li>
<li>使用来自采购订单行的财务维度值。</li>
<li>使用<strong>会计科目表</strong>页中主科目中的默认财务维度值。</li>
</ol></td>
</tr>
</tbody>
</table>


## <a name="distributing-taxes"></a>分配税

无法在计算税金之前创建税金会计分配。 若要计算增值税，必须完成 **供应商发票** 页中的以下任务之一：
-   查看发票合计。
-   查看增值税。
-   – 查看子分类日记帐。
-   完成供应商发票的会计查看分配。
-   处于暂挂状态的供应商发票。
-   过帐供应商发票。

## <a name="subledger-journals-for-vendor-invoices"></a>供应商发票的子分类日志
将普通发票过帐前，您可以查看发票的完整的会计条目，包括借方和贷方，以验证发票已过帐到正确的帐户。 完整的会计条目的此视图称作子分类日记帐。 

如果子分类日记帐条目不正确，在预览后，分录普通发票前，您无法修改子分类日记帐条目。 相反，您必须修改会计分配或过帐模板。 会计分配用于定义会计条目、借方或贷方的这一侧。 抵销子分类日记帐科目分录从过帐模板创建，如从客户帐户或税金。







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
