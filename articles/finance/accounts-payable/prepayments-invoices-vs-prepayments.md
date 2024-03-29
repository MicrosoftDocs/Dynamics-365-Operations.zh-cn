---
title: 预付款账单与预付款
description: 本文介绍和对比组织可以用于预付款（预先付款）的两种方法。
author: abruer
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, PurchTable
audience: Application User
ms.reviewer: twheeloc
ms.custom: 15871
ms.assetid: a0bb5220-73d4-48ae-84d0-46a171c224fa
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1d123a341a471dd37fcc33e0025ce5e98235a27f
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/23/2022
ms.locfileid: "9804255"
---
# <a name="prepayment-invoices-vs-prepayments"></a>预付款账单与预付款

[!include [banner](../includes/banner.md)]

本文介绍和对比组织可以用于预付款（预先付款）的两种方法。 一种方法用于创建与采购订单相关联的预付款发票。 另一种方法用于通过创建日记帐条目并将它们标记为预付款日记帐凭证来创建预付款日记帐凭证。

组织可能向货物或服务的供应商发布预付款（在满足这些货物或服务之前）。 两种方法可用于向供应商发布预付款。 若要将风险最小化，您可以通过跟踪采购订单上的预付款跟踪这些预付款。 对于此方法，您必须创建与采购订单相关联的预付款发票。 此方法称为预付款开票。 不想那么紧密跟踪预付款或不从供应商那里接收预付款发票的组织可以使用预付款日记帐凭证，而不是预付款开票方法。 您可以通过创建日志条目并将它们标记为预付款日志凭证来创建预付款日志凭证。 对于此方法，您不能跟踪根据那个采购订单对供应商进行哪种预付款。 但是，您可以比对采购订单标记要进行结算的过帐预付款。

## <a name="when-to-use-prepayment-invoicing-vs-prepayments"></a>什么时候使用预付款开票与预付款

| 预付款开票                                                                | 预付款                                                              |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| 在采购订单上定义预付款值。                                    | 在采购订单上未定义预付款值。                    |
| 必须过帐预付款发票和最终发票。                       | 不必过帐预付款发票。                                    |
| 预付款的义务保留在预付款帐户中，不在 AP 帐户中。 | 预付款的义务保留在 AP 帐户中。                  |
| 供应商余额不反映整个流程中的预付款值。     | 供应商余额反映整个流程中的预付款值。 |
| 预付款开票只可用于应付帐款。                         | 预付款可用于应付帐款和应收帐款。    |

## <a name="overview-of-the-prepayment-process"></a>预付款流程的概览
许多国家/地区中的会计实务都要求来自某一客户或向某一供应商的预付款（提前付款）不过帐到该客户或供应商的日常汇总科目中。 这些预付款而是过帐到用于预付款的特殊会计科目中。 当创建销售订单或采购订单时，向客户或从供应商签发发票。 当支付发票时，冲销预付款会计科目上的预付款和销售税预付款凭证，发票金额将自动过帐到日常汇总科目上。 遵循这些步骤创建预付款。

1.  设置预付款的过帐模板。
2.  在应收帐款参数和应付帐款参数中，在 **分类帐和销售税** 下，使用 **具有预付款的付款日记帐的过帐模板** 参数选择新的过帐模板。
3.  创建一个付款日记帐，然后创建新的付款。
4.  您可以将付款标记为预付款。 如果付款标记为预付款，付款会过帐到在过帐模板上定义的会计科目（在步骤 1 和 2 中设置）。 此外，如果付款标记为预付款，则会计算税金。 某些政府需要在记录预付款时支付税金，即使没有发票也是。
5.  过帐预付款。
6.  可选：在创建发票前，您可以比对采购订单或销售订单来结算预付款。 在销售订单或采购订单页上，在操作窗格上，使用 **结算交易记录**。
7.  在供应商提供货物或服务之后，应记录发票。 如果您在第 6 步中已比对采购订单或销售订单结算预付款，则会自动比对您创建的发票来结算预付款。 如果您未比对采购订单或销售订单结算预付款，则可以通过使用客户或供应商页上的 **结算交易记录** 来手动结算它。 然后，预付款金额将暂时冲销到 AP/AR 会计科目之外。 此外，如果计算税金，它们将被冲销，因为发票具有实际税金。

## <a name="overview-of-the-prepayment-invoicing-process"></a>预付款开票流程的概览
预付款发票是一个常见业务实践。 在履行采购订单前，供应商会签发预付款发票以要求为采购存款。 例如，某些供应商要求客户货物或服务的预付款。 如果供应商签发一个请求预付款的发票，您可以使用预付款开票功能。 预付款值可以在采购订单上定义，预付款发票会被记录并支付，然后预付款应用于最终发票。 遵循这些步骤创建预付款。

1.  采购代理创建、确认，然后提交供应商已请求预付款的采购订单。 预付款值是在采购订单上定义的，作为协议的一部分。
2.  供应商提交了一个预付款发票。
3.  应付帐款协调员记录了针对采购订单的预付款发票，然后支付预付款发票。
4.  供应商发送付款请求（称为标准供应商发票）。 在供应商交付了货物或服务并已接收相关的标准供应商发票后，应付帐款协调员将应用针对该标准发票已支付的预付款金额。
5.  应付帐款协调员支付并结算标准发票的剩余金额。

## <a name="set-up-parameters-to-enable-the-prepayment-invoicing-process"></a>设置参数以启用预付款开票流程
必须在 **库存过帐** 页面的 **采购订单** 选项卡上定义预付款帐户（**库存管理 \> 设置 \> 过帐 \> 过帐**）。 当过帐预付款发票时，将更新（通常借记）预付款帐户。 当过帐应用到预付款发票的标准发票时，将冲销预付款帐户中的余额。 如果在将预付款发票应用到标准发票之前，您没有将预付款发票结算到付款，当过帐标准发票时，将冲销已过帐预付款发票中的会计条目。

在 **供应商过帐** 配置文件上定义抵消汇总应付帐款帐户。 若要定义默认的过帐配置文件，请单击 **应付帐款 \> 设置 \> 应付帐款参数 \> 分类帐和销售税选项卡 \> 具有预付款供应商发票的过帐配置文件**。

**预付款申请策略** 指示已结算预付款发票是否自动应用到手动创建的最终发票。 使用数据实体创建的发票不引用 **预付款申请策略**。 您将需要手动将已结算预付款发票应用到使用数据实体创建的发票。 若要定义该策略，请转到 **应付帐款 \> 设置 \> 应付帐款参数 \> 分类帐和销售税选项卡 \> 预付款申请策略**。 如果 **预付款申请策略** 字段设置为 **自动**，将针对具有最终发票的结算自动标记预付款发票。 如果该字段设置为 **通知**，当创建最终发票时，将显示预付款发票可供申请的可视指示。

## <a name="create-a-purchase-order-that-contains-prepayment-invoice-information"></a>创建包含预付款发票信息的采购订单
当供应商告诉您他们要求对采购订单中包含的商品和服务进行预付款时，您必须为关联的采购订单定义预付款值。 转到 **应付帐款 \> 常用 \> 采购订单 \> 所有采购订单**，然后找到供应商的采购订单。 在操作窗格上，选择 **采购** 选项卡，然后选择 **预付款**。 输入预付款的信息，包括描述、预付款的值、预付款是固定金额还是百分比，以及预付款类别 ID。 

> [!Note] 
> 采购订单上不允许多个预付款定义。 如果需要在采购订单上允许多个预付款，请使用付款日记帐而不是预付款发票过帐付款。

可以从采购订单中删除预付款，除非您已针对已过帐预付款发票结算付款或已过帐标准发票。 若要从采购订单中删除预付款信息，请选择 **应付帐款 \> 常用 \> 采购订单 \> 所有采购订单**，然后找到供应商的采购订单。 在操作窗格上，选择 **采购** 选项卡，然后选择 **删除预付款**。

## <a name="create-and-post-a-prepayment-invoice"></a>创建和过帐预付款发票
若要记录供应商的预付款发票，请通过在 **采购订单** 页面上选择 **预付款发票** 选项转到 **供应商发票** 选项（**应付帐款 \> 常用 \> 采购订单 \> 所有采购订单 \> 发票选项卡 \> 预付款发票**）。 输入预付款发票的信息，包括发票编号。 无法更改预付款发票的数量。 如果供应商开具了在采购订单上定义的部分预付款值金额的发票，您可以更新单价以反映部分值。

当过帐预付款发票时，将更新供应商余额和预付款帐户。 还将更新采购订单上包含的预付款定义上的 **预付款申请** 值。 将从采购订单上的标题信息中获取已过帐预付款凭证的默认财务维度条目。

如果启用 **功能管理** 页面上的 **锁定供应商预付款发票上发票行的财务维度** 功能，则无法更新预付款标题或行中的维度。 

## <a name="post-and-settle-payments-for-the-prepayment-invoice"></a>过帐和结算预付款发票的付款
接下来，从 **付款日记帐** 页面中支付预付款发票。 若要访问付款日记帐，请单击 **应付帐款 \> 日记帐 \> 付款 \> 付款日记帐**。 在将付款结算过帐到预付款发票后，将更新采购订单的 **剩余预付款申请** 值。

在过帐预付款发票的标准发票之前，您可以从预付款发票中冲销付款的结算。 但是，在将标准发票应用到预付款发票之后，无法从预付款发票中冲销付款结算。

## <a name="post-the-standard-vendor-invoice-for-the-purchase-order-and-apply-the-prepayment-invoice-to-the-standard-invoice"></a>过帐采购订单的标准供应商发票，并将预付款发票应用到标准发票
记录从供应商处接收的标准发票。 作为此流程的一部分，您可以将结算的预付款发票应用到供应商发票，以便从已支付的金额中减去发票的值。 将预付款发票应用到供应商发票将确保冲销预付款发票中的会计条目。

## <a name="application-of-the-prepayment-invoice-after-posting-the-standard-invoice"></a>在过帐标准发票后申请预付款发票
如果您在过帐供应商发票时忘记将预付款应用到标准供应商发票，结算的发票将可用于通过 **供应商** 页面应用到此供应商的其他发票（**应付帐款 \> 常用 \> 供应商 \> 所有供应商 \> 发票选项卡 \> 应用**）。

## <a name="reversal-of-the-prepayment-application-process"></a>冲销预付款申请流程
如果您需要从标准发票中取消结算或冲销预付款发票的申请，请从 **供应商** 页面中选择 **冲销** 操作（**应付帐款 \> 常用 \> 供应商 \> 所有供应商 \> 发票选项卡 \> 冲销**）。 冲销应付款申请后，您可以将预付款应用到其他标准发票。 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
