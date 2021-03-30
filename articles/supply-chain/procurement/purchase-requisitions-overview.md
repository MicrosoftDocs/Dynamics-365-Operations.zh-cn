---
title: 采购申请概览
description: 此主题介绍了采购申请工作流和采购申请可能具有的不同状态。
author: RichardLuan
manager: tfehr
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqConsolidation, PurchReqCreate, PurchReqCreatePurchDetails, PurchReqCreatePurchListPage, PurchReqTable, PurchReqTableListPage, PurchReqConsolidationPartByVendor, PurchReqConsolidationLineDetail, PurchReqConsolidationCreate, PurchReqConsolidationBulkEdit, PurchReqConsolidationAddLine
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2174
ms.assetid: 77d07119-4d9f-4c0e-acbe-d319203571ab
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6d3cc8043062fe304ef8127a2abbaeb787c4761f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5215929"
---
# <a name="purchase-requisition-overview"></a>采购申请概览

[!include [banner](../includes/banner.md)]

此主题介绍了采购申请工作流和采购申请可能具有的不同状态。

根据您的组织的设置，您可以创建您组织使用的产品的采购申请。 采购申请是授权采购部门购买物料或服务的内部文档。  

在审核采购申请后，其可用于生成采购订单。 采购订单是采购部门提交给供应商的外部文档。

## <a name="creating-purchase-requisitions"></a>创建采购申请
您可以在 **我的采购申请** 页上创建采购申请并选择您所需的物料和服务。 通过选择采购类别和输入产品详细信息，您可以从组织创建的采购目录中选择物料，或请求目录中未找到的物料。  

在可提交采购申请供查看前，必须配置工作流。 您使用工作流通过审核流程移动采购申请，从 **草稿** 的初始状态到 **已审核** 最终状态。

### <a name="purchase-requisition-statuses"></a>采购申请状态

当您创建了一个采购申请时，为它分配一个状态。 您添加到采购申请的每个行也会获分配状态。 当您提交采购申请到工作流以供审核时，在这些行在工作流程中移动时更新采购申请的状态和每一行的状态。  

您可以将采购申请工作流流程配置为使采购申请以单个文档的形式通过审核流程。 或者，在采购申请上的行可单独传送给相应审核人。 如果单独审查采购申请行，可以当该行在审查流程中移动时更新每个采购申请行的状态。 当所有行完成了审查流程，而且采购申请没有剩余审查步骤时，将会更新整个采购申请的状态。

### <a name="purchase-requisition-workflow"></a>采购申请工作流

下图显示了分配给采购申请和采购申请行的状态（当它们在工作流程中移动时）。  

[![采购申请标题和行状态](./media/purchasereq_headerline_statuses.jpg)](./media/purchasereq_headerline_statuses.jpg)

### <a name="purchase-requisition-header-and-line-status-relationships"></a>采购申请标头和行状态关系

该采购申请的整体状态由采购申请行确定。 因此，在整个采购申请的审查流程完成前，必须完成所有采购申请行的审查流程。 下表描述了当采购申请在工作流程中移动时分配给采购申请标头和行的状态。

<table>
<thead>
<tr class="header">
<th>采购申请状态</th>
<th>采购申请行状态</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>草案</td>
<td>草案</td>
<td>已创建采购申请和采购申请行，但是尚未提交以供审查。 可以修改具有状态<strong>草稿</strong>的采购申请和采购申请行。 采购申请或采购申请行也可以具有状态<strong>草稿</strong>（如果它已被撤回，但未被提交以供审核）。 <strong>注意：</strong>您可在单据级别提交或撤回采购申请。 但是，您无法提交或撤回单个采购申请行。</td>
</tr>
<tr class="even">
<td>正在审核</td>
<td><ul>
<li>正在审核</li>
<li>已拒绝</li>
</ul></td>
<td>如果已将工作流配置为将采购申请行传送给各个审核者，则每个行都可以具有状态<strong>正在审核</strong>或<strong>已拒绝</strong>。 为所有采购申请行完成了审查流程，而且没有针对采购申请的剩余审查步骤时，将会更新该采购申请状态。
<ul>
<li><strong>正在审核</strong> – 已提交采购申请行以供审查。 当为采购申请行完成了工作流流程时，该行将保持为状态<strong>正在审核</strong>，直到审查了所有其余采购申请行。</li>
<li><strong>已拒绝</strong> – 已拒绝采购申请行。 已拒绝的采购申请行可以修改和重新提交。</li>
</ul>
如果您重新提交已被拒绝的采购申请行，将针对仍处于审核状态的采购申请行中的所有行重新开始审查流程。 </br><strong>注意：</strong>您可以撤回已提交的采购申请。 当您撤回了某个采购申请时，也撤回了所有其他采购申请行。 可以删除已被撤回的采购申请行。</td>
</tr>
<tr class="odd">
<td>已拒绝</td>
<td>已拒绝</td>
<td>已拒绝采购申请和所有采购申请行。 可以重新提交已拒绝的采购申请和采购申请行。</td>
</tr>
<tr class="even">
<td>已审核</td>
<td><ul>
<li>已审核</li>
<li>已取消</li>
<li>已结束</li>
</ul></td>
<td>所有采购申请行都已完成了审查流程，并且针对该采购申请，没有更多的审查步骤。
<ul>
<li><strong>已审核</strong> – 已完成了采购申请行的审查流程，并已审核该行。</li>
<li><strong>已取消</strong> – 该采购申请行已审核，但是因为不再需要它，所以已被取消。 只取消进行审核的采购申请行。</li>
<li><strong>已关闭</strong> – 已审核采购申请行，并且已根据申请用途生成单据。
<ul>
<li>如果申请目的是消耗量，则采购申请的采购订单已生成。</li>
<li>如果申请目的是补货，则已生成一个或多个履行文档。</li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td>已取消</td>
<td>已取消</td>
<td>已取消采购申请和所有采购申请行。</br> <strong>注意：</strong>如果您不再需要在采购申请行上的物料，则您必须取消采购申请行（如果它已被审核）。 只取消进行审核的采购申请行。 如果每个采购申请行都在审查中，则该采购申请也将拥有状态<strong>正在审核</strong>。 在这种情况下，您可以撤回该采购申请，并删除相应的采购申请行。</td>
</tr>
<tr class="even">
<td>已结束</td>
<td><ul>
<li>已结束</li>
<li>已取消</li>
</ul></td>
<td>采购申请已关闭，并已生成一个或多个履行文档。
<ul>
<li><strong>已关闭</strong> – 已审核采购申请行，并且已根据申请用途生成单据。
<ul>
<li>如果申请目的是消耗量，则采购申请的采购订单已生成。</li>
<li>如果申请目的是补货，则已生成一个或多个履行文档。</li>
</ul></li>
<li><strong>已取消</strong> – 该采购申请行已审核，但是因为不再需要它，所以已被取消。 只取消进行审核的采购申请行。</li>
</ul>
<strong>注意：</strong>如果您不再需要已关闭的采购申请行上的物料，则您必须取消为采购申请行生成的履行文档上的行。</td>
</tr>
</tbody>
</table>

## <a name="distributing-costs-to-multiple-financial-accounts"></a>多个财务科目的分摊成本
您可以将包括在采购申请中的产品的成本分摊到多个财务科目。 如果您的组织使用维度，如成本中心和部门，则您可以将产品的成本分摊到财务账户的维度。

## <a name="requisition-purposes"></a>申请用途
申请用途让履行申请需求的流程更灵活。 在您创建申请时，可以将两个目的之一分配给它：消耗量或补货。 根据申请用途和您的组织设置，申请需求可通过采购订单、转移单、生产订单或看板履行。  

在采购政策中，当为您的组织创建申请时，您可以控制可用的申请目的。

### <a name="requisitions-that-have-a-purpose-of-consumption"></a>申请具有消耗量的目标

申请具有消耗量的目标表示将通过您的组织内部使用的物料或服务的需求。 通过此类型的申请创建需求始终按采购订单执行。 如果 Supply Chain Management 设置为自动生成采购订单，将在采购申请审核后创建采购订单。

### <a name="requisitions-that-have-a-purpose-of-replenishment"></a>申请具有补货的目标

补货具有补货的目的表示需求以补充库存。 例如，您创建补货物料的申请，以便他们可以在特定的零售位置的指定时间销售。 由此申请创建的需求可以按采购订单、转移单、生产订单或看板执行。  

当申请目的为补货时，需求表示为数量而不是货币金额。 因此，预留款核算、预算控制、固定资产确定的业务规则 (BRAD)，项目核算和任何相关的规则不适用。 已存储和发放到指定法人的产品可以履行补货申请要求。 若要定义在申请用途是补货时可用的产品，请使用 **补货类别访问政策规则** 页。  

若要使用具有补货目的的采购申请，您必须将主计划编制设计为包括申请需求。 将基于在您的组织中为物料设置的供应策略自动确定由此类申请创建的需求的履行方法，并通过使用主计划编制计划。

## <a name="purchase-requisitions-and-requests-for-quotation"></a>采购申请和询价
有时候，您必须开始询价 (RFQ) 流程以确定在采购申请中申请的产品的供应商和价格。 在采购申请正在审核时，可以生成询价。 当您接受出价时，有关供应商、价格等的信息将转移到申请。  

您可以通过选中 **采购申请详细信息** 页上的 **暂停** 复选框来将采购申请置于暂停状态。 处理采购申请只能在您通过清除此复选框删除暂停后继续。  

> [!NOTE]
> 在电子采购中，您的采购申请的询价可能允许供应商添加备选行。 在此情况下，采购申请将反映已审核的备选项。

## <a name="demand-consolidation"></a>需求合并
通过合并来自多个采购申请的采购申请行，您可以增加与您的供应商协商的能力，以实现更好的定价、更低的装运和处理的费用，并降低开销成本。  

仅当以下报表为真时，采购申请行才适用于需求合并：

-   采购申请已审核。
-   采购申请符合手动进行处理和要求合并的采购策略规则条件。

符合手动处理条件的已审核的采购申请行在 **发布已审核的采购申请** 页列出。 如果采购申请行还满足需求合并的条件，可以将该行添加到“合并机会”。  

合并机会是一组组合在一起的采购申请行，以便该采购的专业人员可以与供应商协商最佳交易。 您为合并机会选择的采购申请行上显示在 **采购申请合并** 页。 如果需要更改，您可以在此页修改行。 您还可以为该合并机会添加新行或从中删除现有行。  

在将申请行添加到合并机会并作出所需更改后，您可以为该合并采购申请行创建采购订单。  

> [!NOTE]
> 您为在 **采购申请合并** 页中的某一采购申请行做出的更改反映在您创建的采购订单上。 但是在采购申请中，该行保持不变，以便保留其历史记录。  

若要为没有资格享受需求合并或没有为合并机会选择的采购申请行创建采购订单，您必须手动处理行。

### <a name="consolidating-purchase-requisition-lines"></a>合并采购申请行

在工作流中的采购申请审核时，以及如果为您的组织配置了预算控制，记录预算预留和预留款后，将启动要求合并的流程。 下图显示需求合并的流程。  

[![需求合并的流程流](./media/demand-consolidation.gif)](./media/demand-consolidation.gif)  

若要合并已审核的采购申请行，请执行以下步骤：

1.  查看已审查的申请行，这些申请行为手动处理持有并且适用于需求合并。
2.  选择要添加到合并机会的行。
3.  创建新的合并机会或将申请行添加到现有合并机会。
4.  对申请行进行任何所需更改，然后移除您在合并机会中不再想要包含的申请行物料。
5.  创建合并机会中的合并申请行或采购申请行的采购订单。


<a name="additional-resources"></a>其他资源
--------

[创建消耗量申请](tasks/create-requisition-consumption.md)

[采购申请工作流](purchase-requisitions-workflow.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]