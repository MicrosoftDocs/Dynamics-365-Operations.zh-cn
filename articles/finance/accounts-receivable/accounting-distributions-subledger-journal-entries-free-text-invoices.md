---
title: 会计分配和普通发票的日记帐条目
description: 会计分配用于定义将如何对帐金额，例如将如何对帐普通发票中的收入、税金或费用。 普通发票已记入日记帐时，必须对帐的每笔金额都将具有一个或多个会计分配。
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: roschlom
ms.custom: 3141
ms.assetid: fecd17a2-d7b4-4a20-ac81-eb71abbfa9d1
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: da1d1b41c4da1fafcf20246022c4020b60152917f5df85f8e003e23aaef9433c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6728929"
---
# <a name="accounting-distributions-and-subledger-entries-for-free-text-invoices"></a>会计分配和普通发票的子分类帐条目

[!include [banner](../includes/banner.md)]

会计分配用于定义将如何对帐金额，例如将如何对帐普通发票中的收入、税金或费用。 普通发票已记入日记帐时，必须对帐的每笔金额都将具有一个或多个会计分配。

## <a name="accounting-distributions"></a>会计分配

您可以使用“普通发票”页中的以下按钮查看和更改普通发票的每笔金额的会计分配。

-   **分摊金额** — 查看和更改单独行和任何子行的会计分配，例如税金或费用。 您还可以直接从“销售税交易记录”页或“费用交易记录”页查看和更改子行的会计分配。
    -   更改普通发票抬头金额，如费用或币种化整金额。
    -   更改普通发票行金额。
-   **查看分配** - 查看文档中所有行的会计分配。 您无法从此视图更改会计分配。
    -   查看标题和单行金额。

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
<th>货币金额的类型</th>
<th>主科目显示的位置。</th>
<th>优先级顺序确定显示的默认财务维度</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>普通发票行</td>
<td>普通发票行的会计科目。</td>
<td><ol>
<li>如果主科目是分配帐户，则使用分配帐户定义中的默认值。</li>
<li>如果主科目不是分配帐户，则使用普通发票行的财务维度默认模板。</li>
<li>在普通发票行使用默认的财务维度值。</li>
<li>使用“会计科目表”页中会计科目中的默认财务维度值。</li>
</ol></td>
</tr>
<tr class="even">
<td>固定资产编号和价值模型组合的普通发票行
<div class="alert">
<table>
<thead>
<tr class="header">
<th><strong>注意</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>普通发票行的主科目将为固定资产处置科目。</td>
</tr>
</tbody>
</table>
</div></td>
<td>普通发票行的会计科目。</td>
<td><ol>
<li>在普通发票行使用默认的财务维度值。</li>
<li>使用“会计科目表”页中会计科目中的默认财务维度值。</li>
</ol></td>
</tr>
<tr class="odd">
<td>普通发票折扣金额</td>
<td>“现金折扣”页面上的“客户折扣的主科目”字段。</td>
<td><ol>
<li>如果主科目是分配帐户，则使用分配帐户定义中的默认值。</li>
<li>如果主科目不是分配帐户，则使用普通发票行的财务维度默认模板。</li>
<li>在普通发票行使用默认的财务维度值。</li>
<li>使用“会计科目表”页中会计科目中的默认财务维度值。</li>
</ol></td>
</tr>
<tr class="even">
<td>普通发票销售税总额</td>
<td>“分类帐记帐组”页中的“应付销售税”字段。</td>
<td><ol>
<li>使用普通发票单行金额或费用行金额的分配中定义的财务维度。</li>
<li>在普通发票行使用默认的财务维度值。</li>
<li>使用“会计科目表”页中会计科目中的默认财务维度值。</li>
</ol></td>
</tr>
<tr class="odd">
<td>普通发票费用行金额</td>
<td>“费用代码”页中的“贷方科目”字段。</td>
<td><ol>
<li>如果主科目是分配帐户，则使用分配帐户定义中的默认值。</li>
<li>如果主科目不是分配帐户，则使用普通发票行的财务维度默认模板。</li>
<li>在普通发票行使用默认的财务维度值。</li>
<li>使用“会计科目表”页中会计科目中的默认财务维度值。</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="distributing-taxes"></a>分配税
无法在计算税金之前创建税金会计分配。 若要计算增值税，必须完成“普通发票”窗体中的以下任务之一：
-   查看增值税。
-   查看发票合计。
-   查看现金流。
-   查看整个普通发票的会计分配。
-   – 查看子分类日记帐。

## <a name="subledger-journals-for-free-text-invoices"></a>普通发票的子分类日记帐
将普通发票过帐前，您可以查看发票的完整的会计条目，包括借方和贷方，以验证发票已过帐到正确的帐户。 完整的会计条目的此视图称作子分类日记帐。 如果子分类日记帐条目不正确，在预览后，分录普通发票前，您无法更改子分类日记帐条目。 相反，您必须更改会计分配或过帐模板。 会计分配用于定义会计条目、借方或贷方的这一侧。 抵销子分类日记帐科目分录从过帐模板创建，如从客户帐户或税金。





[!INCLUDE[footer-include](../../includes/footer-banner.md)]