---
title: 库存锁定
description: 本主题提供库存锁定的概览，这是 Supply Chain Management 中质量检查流程的一部分。 您可以使用库存锁定来阻止处理或消耗物料。
author: yufeihuang
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventQualityOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2094
ms.assetid: 1968e32f-eff9-4c17-8f7f-a870f0c38fbc
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 606bc23f552b57d0f4e3fdad28d1144cdf43e5d5
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103530"
---
# <a name="inventory-blocking"></a>库存锁定

[!include [banner](../includes/banner.md)]

本主题提供库存锁定的概览，这是 Supply Chain Management 中质量检查流程的一部分。 您可以使用库存锁定来阻止处理或消耗物料。

您可以按照以下方法锁定库存物料：

- 手动
- 通过创建质量订单
- 通过使用生成质量订单的流程
- 使用库存状态锁定

## <a name="blocking-items-manually"></a>手动锁定物料

您可以通过在 **库存锁定** 页中创建交易记录来锁定物料的数量。 只有作为现有库存可用的物料可以被手动锁定。 对于手动锁定的数量，您必须决定计划活动是否作为预期的现有数量包括预期收货。 预期收货锁定您希望在检查完成后作为现有库存可用的物料。 您可以维护预期日期。 默认情况下，**预期收货** 选项为通过质检订单锁定的物料选中。 您可以通过删除 **库存锁定** 页中的交易记录取消数量的手动锁定。

## <a name="blocking-items-by-creating-a-quality-order"></a>通过创建质检订单锁定物料

您可以通过在 **质检订单** 页上创建质检订单来指定必须检查的物料。 当您创建一个质量订单时，将锁定您为物料指定的数量。 与质检订单控制关联的抽样计划只控制必须检查的物料的数量，而不控制被锁定的数量。 在质检订单上输入的数量是已锁定的数量，不管抽样计划指定的数量是否应发送供检查。

> [!NOTE]
> 主计划不支持同时使用批处理到期日期和锁定库存状态功能。 这可能会导致现有库存量的双重排除，这有可能在主计划期间发生。 我们建议您使用批处置代码（而不是库存状态）来锁定到期的批处理。

## <a name="blocking-items-by-using-a-process-that-generates-a-quality-order"></a>通过使用生成质检订单流程锁定物料

如果质量流程指定必须检查物料，则物料数量将被自动锁定。 因此，当自动生成质检订单时，与该质检订单相关联的物料抽样计划同时控制锁定的物料的数量和必须检查的数量。 如果选择了 **物料抽样** 页中的 **完全锁定** 选项，则不管物料抽样数量，在检查期间锁定采购订单行等的整个数量。

### <a name="example"></a>示例

在以下的示例中，过账采购订单的装箱单时生成了一个质量订单。 在 **质量关联** 页中，您指定了采购订单装箱单的过帐为激活质量订单的流程。

|设置 |用户操作 |结果 |
|----|---|---|
| 质量关联指定在采购订单装箱单过帐时必须生成质检订单。 质检订单的物料抽样设置指定必须检查 10% 的采购订单行数量。 此外，由于在物料抽样设置中选择了 **完全锁定** 选项，因此不管发送以供检查的数量，在检查期间必须锁定采购订单行的整个数量。 | 过账装箱单。 | 生成质量订单。 将物料的 10% 的采购订单数量送检。 锁定该采购订单行的整个数量。 |

## <a name="blocking-items-by-using-inventory-status-blocking"></a>通过使用库存状态锁定锁定物料

您可以使用 **库存状态** 页上的 **锁定库存** 参数指定哪些库存状态是锁定状态。 您不能使用库存状态作为生产订单、销售订单、转移单、传出交易记录或项目集成的锁定状态。 对于出货工作，使用具有个可用库存状态的物料。 如果物料具有 **中断** 状态，并且主计划在这些物料上运行，则将物料视为缺失，库存会自动补货。

## <a name="take-care-when-blocking-items-that-use-both-inventory-status-blocking-and-quality-order-blocking"></a>锁定同时使用库存状态锁定和质检订单锁定的物料时要当心

您可以创建与库存状态启用了 **库存锁定** 参数的库存关联的质检订单。 在这种情况下，除了库存状态创建的记录外，质检订单还将生成额外的库存锁定记录。 由于质检订单库存锁定将启用参数 **预期收货**，因此会生成额外的 *已订购库存* 交易，该交易也按其库存状态被锁定。 此组合可能会导致难以理解所生成的库存交易的含义，因为看起来好像总锁定数量超过了现有总数量。 我们以接收 10 件物料 A0001 的示例为例检查交易，并生成质检订单来抽样检查 1 件。 此行为还将取决于是否在 **库存和仓库管理参数** 页上启用了选项 **预留已订购物料**。

>[!NOTE]
>如果您将库存状态锁定和质检订单一起使用，我们强烈建议启用 **预留已订购物料** 选项。

### <a name="example-with-reserve-ordered-items-enabled"></a>启用“预留已订购物料”的示例

**预留已订购物料** 启用时，所有库存锁定交易的状态要么为 *实际预留*，要么为 *订购预留*。

| 库存交易参考 | 收货 | 签发 | 数量 | 站点 | 仓库 | 库存状态 | 库位 | 牌照 | 注释 |
|---|---|---|---|---|---|---|---|---|---|
| 采购订单 | 已采购 | | 10 件 | 2 | 24 | 锁定 | RECV | receiptLp1 | | 
| 库存锁定 | | 实际预留 | -9 件 | 2 | 24 | 锁定 | | | 库存状态锁定生成的交易 |
| 库存锁定 | | 实际预留 | -1 件 | 2 | 24 | 锁定 | RECV | receiptLp1 | 质检订单抽样锁定生成的交易 |
| 库存锁定 | 订购时间 | | 1 件 | 2 | 24 | 锁定 | RECV | receiptLp1 | 来自质检订单抽样锁定的预期收货 |
| 库存锁定 | | 订购预留 | 1 件 | 2 | 24 | 锁定 | | | 库存状态锁定生成的交易

### <a name="example-with-reserve-ordered-items-disabled"></a>禁用“预留已订购物料”的示例

**预留已订购物料** 禁用时，由于状态为 *已订购*，所以预期收货无法预留，因此有些锁定仍然处于 *在单* 状态。

| 库存交易参考 | 收货 | 签发 | 数量 | 站点 | 仓库 | 库存状态 | 库位 | 牌照 | 注释 |
|---|---|---|---|---|---|---|---|---|---|
| 采购订单 | 已采购 | | 10 件 | 2 | 24 | 锁定 | RECV | receiptLp1 | |
| 库存锁定 | | 实际预留 | -9 件 | 2 | 24 | 锁定 | | | 库存状态锁定生成的交易 |
| 库存锁定 | | 实际预留 | -1 件 | 2 | 24 | 锁定 | RECV | receiptLp1 | 质检订单抽样锁定生成的交易 |
| 库存锁定 | 订购时间 | | 1 件 | 2 | 24 | 锁定 | RECV | receiptLp1 | 来自质检订单抽样锁定的预期收货 |
| 库存锁定 | | 在单 | 1 件 | 2 | 24 | 锁定 | RECV | receiptLp1 | 库存状态锁定生成的交易

注意两种情况之间交易状态和维度的差异。 出于此原因，我们建议启用 **预留已订购物料** 选项。

### <a name="disable-expected-receipts-from-quality-orders-that-sample-blocked-inventory-feature"></a>禁用从锁定库存取样的质检订单的预期收货功能

为在由于库存状态导致对库存取样的质检订单被锁定时简化库存交易记录，系统提供了一项可禁用此类质检订单的预期收货的功能。 由于预期收货因库存状态为锁定状态而被锁定，因此不会因为此更改而减少现有库存量。

此功能默认关闭。 管理员可以通过在 [功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区中搜索 *禁用从锁定库存取样的质检订单的预期收货* 功能来打开或关闭此功能。

## <a name="additional-resources"></a>其他资源

[创建和维护库存锁定](tasks/create-maintain-inventory-blocking.md)

[质量管理流程](quality-management-processes.md)

[检查货物的质量](tasks/inspect-quality-goods.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]