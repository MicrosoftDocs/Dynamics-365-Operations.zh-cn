---
title: 为外部客户创建内部公司销售订单，并为这些订单开票
description: 本主题说明如何为外部客户创建内部公司销售订单，并为这些订单开票
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 72273a125da2e6c4a2fc16b449cd5077f3d767df
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548119"
---
# <a name="create-and-invoice-an-intercompany-sales-order-for-an-external-customer"></a>为外部客户创建内部公司销售订单，并为这些订单开票

[!include [banner](../../includes/banner.md)]

您可以使用内部公司交易来记录从一个法人到在同一组织中的其他法人的产品销售金额。

在您创建原始销售订单时，您可以为内部公司供应商自动创建内部公司采购订单。 这会在内部公司供应商的法人中自动创建内部公司销售订单。

下图显示当您为外部客户创建销售订单时的交易记录流，但是，必须从您的组织中的不同的法人订购产品，然后才能将产品提供给客户。 在这种情况下，将为代表其他法人的供应商帐户创建内部公司采购订单。 然后，在其他法人中为代表您法人的客户帐户创建内部公司销售订单。 当内部公司采购订单已开票，自动过账原始销售订单的发票（如果它是直接交运）。

![内部公司外部销售流程](media/intercompanyexternalsalesprocess.png)

如果您在使用直接交运，并且在 **过帐发票** 页面上的 **数量** 字段中选择了 **装箱单**，则内部公司供应商发票基于以前已过帐的内部公司产品收货。

## <a name="prerequisites"></a>先决条件

在您开始前，请确保满足以下先决条件以自动过帐和并打印内部公司发票。

1. 转到 **销售和市场营销 \> 客户 \> 所有客户**。
1. 在操作窗格上的 **常规** 选项卡中，选择 **内部公司**。
1. 转到 **采购 \> 供应商 \> 所有供应商**。
1. 在操作窗格上的 **常规** 选项卡中，选择 **内部公司**。
1. 在供应商或客户的 **内部公司** 页面上，在 **采购订单策略** 区域内的 **内部公司采购订单（直接交运）** 字段组中，选中 **自动过帐发票** 复选框。
1. 在 **采购订单策略** 区域内的 **原始销售订单（直接交货）** 字段组中，选中 **自动过帐发票** 复选框。 如果要在您过帐内部公司供应商发票时，自动打印原始销售订单的发票，选择此复选框。

> [!NOTE]
> 发票的打印设置由 **打印管理设置** 页上的模块、文档或交易记录的设置所决定。

## <a name="create-an-original-sales-order-for-an-external-customer"></a>为外部客户创建一个原始销售订单

在法人 A 中执行以下步骤。此过程对应于该图中的框 1。

1. 转到 **应收帐款 \> 销售订单 \> 所有销售订单**。
1. 从 **所有销售订单** 列表页中，创建原始销售订单。 字段值来自销售订单的客户帐户的副本。
1. 在 **销售订单** 页面上，选择“操作”窗格上的 **标题视图**。
1. 在 **内部公司设置** 快速选项卡上，选择 **自动创建内部公司订单** 复选框。
1. 如果要使内部公司供应商直接向外部客户交付物料，请选中 **直接交货** 复选框。
1. 在您完成输入销售订单时，关闭 **销售订单** 页。

系统会为具有分配的内部公司供应商的所有物料自动创建内部公司采购订单，然后创建内部公司销售订单。 会有一则参考消息通知您：已创建内部公司采购订单和内部公司销售订单。 消息还包含指向这些订单的链接。 如果找不到物料，则显示红色警告，这意味着未完成订单创建流程。

> [!NOTE]
> 如果要创建分属不同法人的订单，并且在其中某个法人中未找到物料，订单创建流程将会停止，即便对于可以履行其订单的法人也是如此。

## <a name="invoice-an-intercompany-sales-order"></a>内部公司销售订单开发票

当内部公司销售订单开票后，为相应的内部公司采购订单自动开票。 然后，如果原始销售订单是直接交运订单，则对原始销售订单自动开票。

在法人 B 中执行以下步骤。此过程对应于该图中的框 2。

1. 转到 **应收帐款 \> 销售订单 \> 所有销售订单**。
1. 在 **所有销售订单** 列表页上，选择内部公司销售订单。
1. 在“操作”窗格上，选择 **发票** 选项卡，然后选择 **发票**。
1. 选中 **过帐** 复选框。
1. 选择销售订单，然后选择 **确定**。

内部公司销售订单的客户发票自动过帐到法人 B 中。然后在法人 A 中自动创建和过账内部公司供应商发票。如果原始销售订单设置为直接交运，在法人 A 中为原始销售订单创建客户发票。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]