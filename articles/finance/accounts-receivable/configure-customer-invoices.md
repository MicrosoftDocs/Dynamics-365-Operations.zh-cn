---
title: 创建客户发票
description: 销售订单的客户发票是与销售相关的、组织提供给客户的单据。
author: ShivamPandey-msft
ms.date: 02/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.custom: 77772
ms.assetid: 00b4b40c-1576-4098-9aed-ac376fdeb8c5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d408ca5265802cf17a53dd5cb004f707f6f7855b
ms.sourcegitcommit: 7893ffb081c36838f110fadf29a183f9bdb72dd3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/02/2022
ms.locfileid: "8087415"
---
# <a name="create-a-customer-invoice"></a>创建客户发票

[!include [banner](../includes/banner.md)]

**销售订单的客户发票** 是与销售相关的、组织提供给客户的单据。 此类型的客户发票是基于销售订单创建的，其中包括订单行和物料编号。 在分类帐中指定和过帐物料编号。 子分类日志条目为销售订单的客户发票不可用。 有关详细信息，请参阅[创建销售订单发票](tasks/create-sales-order-invoices.md)。

**普通发票** 与销售订单无关。 它包含包括会计科目、自由文本描述和您输入的销售额的订单行。 您无法在此类发票上输入物料编号。 您必须输入相应的增值税信息。 销售的主科目在每个发票行上指示，这样可以通过单击 **普通发票** 页上的 **分摊金额** 分配给多个会计科目。 此外，将客户余额从用于普通发票的过帐模板过帐到汇总科目。

有关详细信息，请参阅: 

[创建普通发票](../accounts-receivable/create-free-text-invoice-new.md)

[创建普通发票模板](../accounts-receivable/create-free-text-invoice-template-new.md)

[将普通发票模板分配给客户](tasks/assign-free-text-invoice-template-customer.md)

[生成和过帐重复执行普通发票](tasks/post-recurring-free-text-invoices.md)


**估价单** 是一种在过帐发票前作为对实际发票金额的评估而准备的发票。 您可为用于销售订单的客户发票或普通发票打印估价单。

## <a name="using-sales-order-customer-invoice-data-entities"></a>使用销售订单客户发票数据实体
您可以使用数据实体导入和导出有关销售订单的客户发票的信息。 对于销售发票标头和销售发票行上的信息，存在不同的实体。

以下实体可用于销售发票标头上的信息：

- **销售发票日记帐标头** 实体 (SalesInvoiceJournalHeaderEntity)
- **销售发票标头 V2** 实体 (SalesInvoiceHeaderV2Entity)

我们建议您使用 **销售发票日记帐标头** 实体，因为它为销售标头导入和导出提供更高效的体验。 此实体不包含 **销售税金额** (INVOICEHEADERTAXAMOUNT) 列，此列表示销售发票标头上的销售税值。 如果您的业务场景需要该信息，请使用 **销售发票标头 V2** 实体导入和导出销售发票抬头信息。

以下实体可用于销售发票行上的信息：

- **客户发票行** 实体 (BusinessDocumentSalesInvoiceLineItemEntity)
- **销售发票行 V3** 实体 (SalesInvoiceLineV3Entity)

在确定要用于导出的行实体时，请考虑是使用完全推送还是增量推送。 此外，还应考虑数据构成。 **销售发票行 V3** 实体支持更复杂的场景（例如，映射到库存字段）。 另外还支持完全推送导出场景。 对于增量推送，我们建议您使用 **客户发票行** 实体。 此实体包含的数据构成比 **销售发票行 V3** 实体简单得多，因而是首选选择，特别是在不需要库存字段集成的情况下。 由于行实体之间的映射支持差异，**客户发票行** 实体的性能通常高于 **销售发票行 V3** 实体。

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-sales-orders"></a>过帐并打印基于销售订单的各个客户发票
使用此流程创建基于销售订单的发票。 如果您决定在交付货物或服务之前给客户开发票，您可以执行此操作。 

在您过帐该发票时，每个物料的 **未开票数量** 都用来自所选销售订单的已开发票的数量的总数更新。 如果销售订单上所有物料的 **未开票数量** 和 **剩余交货量** 均为 0（零），则该销售订单的状态将更改为 **已开票**。 如果 **未开票数量** 不为 0（零），则该销售订单的状态将不更改，并且可为其输入其他发票。

您可以在 **所有销售订单** 列表页上查看销售订单的状态。 使用 **未结客户发票** 列表页可查看您过帐了的发票。

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-packing-slips-and-the-date"></a>过帐和打印基于装箱单和日期的各个客户发票
当一个或多个装箱单已针对销售订单过帐时，请使用此流程。 客户发票基于这些装箱单并反映来自这些装箱单的数量。 该发票的财务信息基于在您过帐该发票时输入的信息。 

您可以创建基于迄今已发运的装箱单行物料的客户发票，即使尚未发运特定销售订单的所有物料。 例如，如果您的法人每个月为每个客户签发一张支票，该支票涵盖您在该月中发运的所有交货，则可以执行上述操作。 每个装箱单都表示该销售订单上物料的部分或全部交货。 

在您过帐该发票时，每个物料的 **未开票数量** 都用来自所选装箱单的已交货数量的总数更新。 如果销售订单上所有物料的 **未开票数量** 和 **剩余交货量** 均为 0（零），则该销售订单的状态将更改为 **已开票**。 如果 **未开票数量** 不为 0（零），则该销售订单的状态将不更改，并且可为其输入其他发票。 

库存交易记录用发票编号更新，并且销售订单上的 **行状态** 字段中的状态将更改为 **已开票**。 

在 **所有销售订单** 列表页中查看销售订单的状态。

## <a name="consolidate-sales-orders-or-packing-slips-for-posting"></a>合并销售订单或装箱单以进行过帐
当一个或多个销售订单已做好开票准备，并且您希望将其合并到一张发票时，使用此流程。 

您可以在 **销售订单** 列表页上选择多个发票，然后使用 **生成发票** 来合并它们。 在 **过帐发票** 页上，可以更改 **汇总订单** 设置以便按订单编号汇总（其中单个销售订单有多个装箱单）或按发票帐户汇总（其中单个发票帐户有多个销售订单）。 使用 **排列** 按钮可基于 **汇总订单** 设置将销售订单合并到单个发票。

## <a name="additional-settings-that-change-the-posting-behavior"></a>更改过帐行为的附加设置
以下字段更改过帐流程的行为。

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
<td>数量</td>
<td>选择过帐单据所基于的数量。 可用的选项取决于正在过帐的单据类型，如装箱单或发票。
<ul>
<li><strong>当前交货量</strong> – 选择在<strong>当前交货量</strong>字段中输入的所有数量。 使用此选项可以确认或交货部分订单。</li>
<li><strong>已领料</strong> – 选择已领取的全部数量。</li>
<li><strong>全部</strong> – 选择尚未按当前文件类型进行更新的全部销售订单的数量。</li>
<li><strong>装箱单</strong> – 选择装箱单已更新的所有数量。</li>
<li><strong>领料数量和未贮存产品</strong> – 选择领料的全部数量以及未贮存产品的全部数量。</li>
</ul></td>
</tr>
<tr class="even">
<td>过帐</td>
<td><ul>
<li>选择此选项可将销售订单记入日记帐。</li>
<li>清除此选项可以打印估价销售订单。 <strong>注释：</strong>如果已就付款计划签订协议，付款计划不会显示在估价销售订单上。 付款计划只显示在实际销售订单上。</li>
</ul></td>
</tr>
<tr class="odd">
<td>后期选择</td>
<td>选择此选项可稍后应用所选查询。 此选项用于批处理作业。 在批处理作业运行时，查询会运行。</td>
</tr>
<tr class="even">
<td>缩减数量</td>
<td>选择此选项可以在过帐单据时自动减少已交货数量，以便已交货数量等于可用库存。</td>
</tr>
<tr class="odd">
<td>打印</td>
<td>选择打印单据的时间：
<ul>
<li><strong>当前</strong> – 在更新每张发票后打印单据。</li>
<li><strong>之后</strong> – 在更新所有发票后打印单据。</li>
</ul>
<strong>注释：</strong>只有在选择<strong>打印发票</strong>、<strong>打印确认单</strong>、<strong>打印领料单</strong>或<strong>打印装箱单</strong>选项后，<strong>打印</strong>字段才可用。 例如，在<strong>窗体排序</strong>页上，您已将系统设置为按照发票帐户对信息进行排序。 然后您可以选择<strong>之后</strong>以打印按发票帐户进行排序的批次中的单据。 否则，会在完成处理之前打印单据，并且单据不会按<strong>窗体排序</strong>页上指定的顺序进行排序。</td>
</tr>
<tr class="even">
<td>打印发票</td>
<td>选择此选项可以打印发票。 如果该选项已关闭，您可以过帐发票而不打印它。</td>
</tr>
<tr class="odd">
<td>发送电子邮件</td>
<td>选择此选项可以在过帐发票后将销售订单的发票作为电子邮件附件发送给客户。 附件将作为 PDF 和 XML 文件发送。 只有当您在<strong>电子发票参数</strong>页上选择<strong>启用 CFD (电子发票)</strong>选项时，此选项才可用。 <strong>注释：</strong>(MEX) 此控件仅对主地址在墨西哥的法人可用。</td>
</tr>
<tr class="even">
<td>使用打印管理目标</td>
<td>选择此选项可以使用在<strong>打印管理设置</strong>页上为交易记录、单据或模块指定的打印设置。</td>
</tr>
<tr class="odd">
<td>检查信用额度</td>
<td>选择在执行信用额度检查时分析的内容。
<ul>
<li><strong>无</strong> - 对于信用额度检查没有要求。</li>
<li><strong>余额</strong> - 对客户余额检查信用额度。</li>
<li><strong>余额+装箱单或产品收据</strong> – 通过客户余额和交货情况检查信用额度。</li>
<li><strong>余额+所有</strong> - 对客户余额、交货和未结订单检查信用额度。</li>
</ul></td>
</tr>
<tr class="even">
<td>信用更正</td>
<td>选择此选项可以将贷方通知单显示为凭证交易记录中的借记。</td>
</tr>
<tr class="odd">
<td>贷方剩余数量</td>
<td>如果过帐的是贷方通知单，请选中此选项以保留订单上的剩余数量。 如果清除此选项，剩余数量将设置为 0（零）。</td>
</tr>
<tr class="even">
<td>汇总更新</td>
<td>选择汇总多个销售订单将使用的方法：
<ul>
<li><strong>无</strong> – 不汇总销售订单。 例如，对于每个销售订单创建单独的发票。</li>
<li><strong>发票帐户</strong> – 根据在<strong>汇总更新参数</strong>页上设置的条件，汇总所选的所有订单。</li>
<li><strong>订单</strong> – 将所选范围内的订单汇总到指定的一张订单中。 将根据在<strong>汇总更新参数</strong>页上设置的条件对所选订单进行汇总。 如果选择此选项，则必须在<strong>销售订单</strong>字段中选择一个值。</li>
<li><strong>自动汇总</strong> – 如果已在<strong>汇总更新</strong>页上指定了汇总更新，则根据在<strong>汇总更新参数</strong>页上设置的条件对所选的所有订单进行汇总。 如果未指定汇总更新，则将单独过帐订单。</li>
<li><strong>装箱单</strong> – 对于每张装箱单，将所选范围内的订单汇总到一张发票中。 仅当在<strong>数量</strong>字段中选择<strong>装箱单</strong>后，此选项才可用。</li>
</ul></td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
