---
title: 采购订单故障排除
description: 本主题介绍如何解决在使用采购订单时可能遇到的问题。
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 7b65c23fc7ac04fc30c0001bee9541a475026018
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007483"
---
# <a name="troubleshoot-purchase-orders"></a>采购订单故障排除

本主题介绍如何解决在使用采购订单时可能遇到的问题。

## <a name="an-action-can-be-completed-only-after-the-line-number-is-fully-distributed"></a>仅在完全分配行号之后才能完成操作。

发生此问题可能是由于采购订单分配不一致。

要解决此问题并将采购订单重置为 *草稿* 状态，请转到 **采购 \> 定期任务 \> 清除 \> 采购订单分配重置**。 有关详细信息，请参阅以下博客文章：[解决 Dynamics 365 Supply Chain Management 中的采购订单分配错误](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/)。

## <a name="when-purchase-orders-are-imported-through-data-management-purchase-order-line-numbers-dont-follow-the-increment-that-defined-in-system-parameters"></a>通过数据管理导入采购订单时，采购订单行号不遵循系统参数中定义的增量。

### <a name="issue-description"></a>问题描述

默认情况下，通过 *采购订单行 V2* 数据实体导入的采购订单行的自动生成的行号不使用系统参数中指定的系统行号增量。 如果您手动创建采购订单并通过用户界面 (UI) 添加行，行号会正确递增。 但是，如果您使用数据管理框架 (DMF)，则不会正确递增。

发生此问题的原因是，当您通过 DMF 导入行时，如果在导入的实体中尚未分配行号，系统将使用 DMF 的方法进行分配。 该方法始终将行号加 1。

### <a name="issue-workaround"></a>问题解决方法

导入采购订单行时，请确保已在数据实体行号字段中提供了所需的行号。 在这种情况下，DMF 不会覆盖行号。

## <a name="a-default-tax-group-and-a-default-cash-discount-arent-filled-in-from-the-invoice-account"></a>未在发票帐户中填充默认税组和默认现金折扣。

如果您使用与客户帐户不同的发票帐户，在创建采购订单时不会在发票帐户中填充默认税组和默认现金折扣。

此为有意行为。 税组、现金折扣和其他价格信息的默认值基于客户帐户，而不是发票帐户。

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a>我在采购订单确认期间收到“未设置对象引用”错误，或在供应商发票过帐期间发生了“调用目标引发异常”异常。

发生此问题可能是由于采购订单分配不一致。

要解决此问题并将采购订单重置为 *草稿* 状态，请转到 **采购 \> 定期任务 \> 清除 \> 采购订单分配重置**。 有关详细信息，请参阅以下博客文章：[解决 Dynamics 365 Supply Chain Management 中的采购订单分配错误](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/)。

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a>一个或多个会计分配分配过多或分配不足。

### <a name="issue-description"></a>问题描述

您收到以下错误：“一个或多个会计分配分配过多或分配不足。”

### <a name="issue-resolution"></a>解决问题

发生此问题可能是由于采购订单分配不一致。

要解决此问题并将采购订单重置为 *草稿* 状态，请转到 **采购 \> 定期任务 \> 清除 \> 采购订单分配重置**。 有关详细信息，请参阅以下博客文章：[解决 Dynamics 365 Supply Chain Management 中的采购订单分配错误](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/)。

## <a name="can-i-show-only-purchase-orders-that-i-created"></a>我可以只显示我创建的采购订单吗？

此功能当前不可用。

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a>我可以针对采购订单上的已登记库存预留库存和创建交易吗？

### <a name="issue-description"></a>问题描述

即使物料在采购订单上处于 *已登记* 状态，您仍然可以预留库存。 换言之，您可以针对已登记的库存创建交易记录。

### <a name="reproduce-the-issue"></a>重现问题

以下过程显示了一种重现此问题的方法。

1. 创建采购订单。
2. 登记采购订单行。
3. 请注意，您可以针对已登记的库存生成预留或交易。

### <a name="issue-resolution"></a>解决问题

此为有意行为。 预期是已登记的物料已实际到达仓库或库存，因此可以预留。

## <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a>采购订单不反映法人的语言设置。

### <a name="issue-description"></a>问题描述

采购订单上的产品名称以系统语言显示，而不是为创建采购订单的法人设置的语言。

### <a name="reproduce-the-issue"></a>重现问题

以下过程显示了一种重现此问题的方法。

1. 将系统语言设置为 *EN-US*（美国英语）。
1. 确保有一个产品保留了 *EN-US* 和 *DE*（德语）语言来翻译产品名称。
1. 将法人的语言更改为 *DE*。
1. 在将 *DE* 设置为语言的法人中，创建包含该产品的采购订单。
1. 请注意，产品名称仍以美国英语（系统语言）显示。

### <a name="issue-resolution"></a>解决问题

此为有意行为。 在采购订单上，产品始终以系统语言显示。 创建确认日记帐时将使用采购订单语言。

## <a name="the-approved-vendor-list-by-product-entity-doesnt-allow-the-effective-date-to-be-changed"></a>按产品实体列出的核准供应商列表不允许更改生效日期。

### <a name="issue-description"></a>问题描述

例如，产品有生效日期为 2018 年 1 月 11 日 (*01/11/2018*)，到期日期为 *从不* 的核准供应商。 如果您尝试将生效日期更改为 2018 年 1 月 10 日 (*01/10/2018*) 或 2018 年 1 月 12 日 (*01/12/2018*)，将收到以下错误：

> 无法在核准供应商列表 (PdsApproveVendorList) 中创建记录。 “到期”值必须大于或等于“生效”值。

### <a name="issue-resolution"></a>解决问题

您只能延长供应商的核准期限。 下列规则适用：

- 要更改生效日期，使其早于物料供应商的任何现有记录（期限），新期间的到期日期必须早于现有记录中的所有到期日期。
- 若要更改到期日期，使其晚于任何现有期限，生效日期必须在任何现有记录中的最新到期日期之后。
- 要减少供应商的总核准期限，必须删除或修改现有记录。 或者，您可以在导入期间使用 **截断** 切换。 此切换按物料删除表中核准供应商的所有现有记录。

对于问题描述中描述的示例场景：记录的生效日期为 *01/11/2018*，到期日期为 *从不*，可以导入生效日期为 *01/10/2018*、到期日期为 *从不* 的新记录。 但是，您无法通过数据管理缩短期限，让生效日期更新为 *01/12/2018*。 您必须通过 UI 进行此更改。

## <a name="after-i-change-the-delivery-address-on-a-purchase-order-header-the-delivery-name-isnt-synced"></a>我更改采购订单标题上的交货地址后，交货名称没有同步。

### <a name="issue-description"></a>问题描述

采购订单标题上的地址将更新为不是交货地址的地址。 虽然地址在采购订单上已更新，但交货名称不会根据更新的地址进行更新。

### <a name="issue-resolution"></a>解决问题

此为有意行为。 所选地址必须分类为交货地址。 否则，交货名称不会根据所选地址更新。

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a>我可以找到取消采购订单的用户吗？

仅当采购订单接受更改管理时，才会跟踪此信息。 如果使用更改管理，您可以查看谁提交了更改（取消）以及谁批准了更改。
