---
title: 产品收货和开票故障排除
description: 本主题介绍如何解决使用产品收货和开票时可能遇到的问题。
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: d86fa3df1de13cc0e0fb94449207a326069da25b
ms.sourcegitcommit: 91e101d7a51a8b63bd196ec80e9224e5e6e6fc95
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/22/2020
ms.locfileid: "3834322"
---
# <a name="troubleshoot-product-receipts-and-invoicing"></a>产品收货和开票故障排除

本主题介绍如何解决使用产品收货和开票时可能遇到的问题。

## <a name="i-cant-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a>我无法为有基于类别的物料的采购订单行过帐多个发票。

如果要过帐发票，数量是必填项。 因此，如果仅对一行的全部数量开具了部分金额的发票，您将无法为另一个发票上的其余金额开票。

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a>我在采购订单确认期间收到“未设置对象引用”错误，或在供应商发票过帐期间发生了“调用目标引发异常”异常。

发生此问题可能是由于采购订单分配不一致。

要解决此问题并将采购订单重置为*草稿*状态，请转到**采购 \> 定期任务 \> 清除 \> 采购订单分配重置**。 有关详细信息，请参阅以下博客文章：[解决 Dynamics 365 Supply Chain Management 中的采购订单分配错误](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/)。

## <a name="i-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a>我无法将多个产品收货合并到一个采购订单中。

如果不同的产品收货行具有不同的会计日期，则不能将多个产品收货合并到一个采购订单中。

在早期版本的 Microsoft Dynamics 365 Supply Chain Management 中，这种情况允许合并。 但是，这种做法很容易出错。 创建的采购订单行上的会计日期应与从其创建这些采购订单行的产品收货行上的会计日期相同。 （采购订单行上的会计日期与采购订单标题上的会计日期匹配。）因此，不再允许将多个产品收货合并到一个采购订单中。

例如，会计日期会用于预算预留和保留款。 因此，应在从产品收货到采购订单的转换期间保留此信息。

## <a name="when-product-receipts-are-canceled-transactions-can-be-posted-to-a-suspended-ledger-account"></a>取消产品收货后，可以将交易记录过帐到已暂停的会计科目中。

### <a name="issue-description"></a>问题描述

如果取消了产品收货，系统将允许将交易记录过帐到已暂停的会计科目中，即使主科目已暂停。

### <a name="reproduce-the-issue"></a>重现问题

以下过程显示了一种重现此问题的方法。

1. 在**应付帐款参数**页上的**常规**选项卡上，确保将**在分类帐中对产品收货过帐**选项设置为*是*。
1. 创建一个采购订单，并添加产品数量为 *1,000* 的订单行。
1. 确认采购订单。
1. 过帐产品收货，并检查凭证。
1. 暂停相关的主科目 *200140* 和 *140200*。
1. 取消已过帐的产品收货。
1. 请注意，可以将交易记录过帐到暂停的会计科目中。

### <a name="issue-resolution"></a>解决问题

取消产品收货后，可以将交易记录过帐到已暂停的会计科目中，因为此行为可进行正确过帐。

## <a name="a-product-receipt-voucher-number-is-consumed-even-if-no-financial-voucher-is-generated-during-product-receipt"></a>即使产品收货期间未生成财务凭证，也会使用产品收货凭证号。

如果物料模型组的**产品收货上的应计负债**选项设置为*否*，将不会过帐到总帐。 但是，将在子分类帐中为会计目的记录物理事件，该事件需要凭证号。 此凭证号是库存交易记录中引用的凭证号。

我们建议您将**产品收货上的应计负债**选项设置为*是*，如以下博客文章所述：[在产品收货时过帐杂项费用](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/)。

## <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a>不能打开“过帐到分类帐中的费用帐户”设置。

### <a name="issue-description"></a>问题描述

为采购订单开票时，如果将**应付帐款参数**的**发票**选项卡上的**过帐到分类帐中的费用帐户**选项设置为*是*，将发生此问题。

### <a name="reproduce-the-issue"></a>重现问题

以下过程显示了一种重现此问题的方法。

1. 转到**应付帐款 \>设置 \> 应付帐款参数**。
1. 在**发票**选项卡上，将**过帐到分类帐中的费用帐户**选项设置为*是*。
1. 转到**库存管理 \> 设置 \> 过帐 \> 过帐**。
1. 在**采购订单**选项卡上，确保已删除产品的采购支出中的所有行。
1. 转到**应付帐款 \> 采购订单 \> 所有采购订单**。
1. 创建采购订单。 在**供应商帐户**字段中，选择 *1001 Acme 办公设备*。
1. 添加具有以下设置的采购订单行：

    - **物料编号**：*D0011 激光投影仪*
    - **站点**：*1*
    - **仓库**：*11*
    - **数量：** *4*

1. 在操作窗格的**采购**选项卡上，在**操作**组中，选择**确认**。
1. 在操作窗格的**接收**选项卡上，在**生成**组中，选择**产品收货**。
1. 在**过帐产品收货**对话框中的**产品收货**字段中，输入任意数字，然后选择**确定**。
1. 在操作窗格**发票**选项卡的**常规**组中，选择**发票**。
1. 在**编号**字段中，输入任意数字作为发票编号。
1. 更新匹配状态，然后过帐。
1. 请注意，现在从采购订单生成发票时会收到以下错误：“产品的“采购支出”交易类型的科目编号不存在。”

### <a name="issue-resolution"></a>解决问题

这取决于发票和发票组的参数设置。 有关详细信息，请参阅以下博客文章：[采购费用和库存变化的会计](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/)。
