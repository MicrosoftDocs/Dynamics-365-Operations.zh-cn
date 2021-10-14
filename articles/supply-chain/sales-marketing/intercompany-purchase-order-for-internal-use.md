---
title: 创建内部公司采购订单并为其开票供内部使用
description: 本主题说明如何创建内部公司采购订单并为其开票供内部使用
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchLineOpenOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 88a14ff962c5cf0cd1cff24b16cc7a62e9e1c8ce
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548124"
---
# <a name="create-and-invoice-an-intercompany-purchase-order-for-internal-use"></a>创建内部公司采购订单并为其开票供内部使用

[!include [banner](../../includes/banner.md)]

您可以为内部公司供应商创建内部公司采购订单。 这会在内部公司供应商自动创建内部公司销售订单。

![内部公司内部采购流程](media/intercompanypurchaseprocess.png)

## <a name="create-an-intercompany-purchase-order-and-a-corresponding-intercompany-sales-order"></a>创建内部公司采购订单和相应的内部公司销售订单

如示意图中所示，在法人 AAA 中执行以下步骤。

1. 选择 **应付帐款** \> **采购订单** \> **所有采购订单**。
1. 在 **所有采购订单** 列表页，为某一内部公司供应商创建一个采购订单。 将该字段值从供应商帐户复制到采购订单。

    由于您使用内部公司供应商，内部公司销售订单将在相对应的供应商法人中创建。 内部公司销售订单的编号可以与内部公司采购订单的编号相同，它可以包括法人的 ID。 使用的编号结构取决于 **内部公司** 页面内 **销售订单编号** 字段中的选择。 例如，如果您在法人 AAA 中创建采购订单 00029\_064，则法人 BBB 的销售订单编号是 AAA00029\_64。

    会有一则参考消息通知您：已创建内部公司采购订单和内部公司销售订单。 消息包含内部公司销售订单编号，供您参考。

1. 将行物料添加到采购订单。 相应的行物料自动添加到内部公司销售订单。 如果物料不在其他法人中，则将显示消息，并且您不能将物料添加到采购订单中。 为了解决此问题，切换到其他法人并将该产品发布给该法人。 物料将可以添加到该法人销售订单中。 然后，切换回采购订单的法人并继续添加行项。
1. 完成输入采购订单信息时，要进行确认。

## <a name="process-the-intercompany-packing-slip-and-customer-invoice"></a>处理内部公司装箱单和客户发票

如示意图中所示，在法人 BBB 中执行以下步骤。

1. 转到 **应收帐款 \> 销售订单 \> 所有销售订单**。
1. 在 **所有销售订单** 列表页上，选择内部公司销售订单。
1. 在“操作”窗格上，选择 **领料和装箱** 选项卡，然后选择 **装箱单**。
1. 选中 **过帐** 复选框。
1. 选择 **确定**。 在法人 BBB 中过帐装箱单。
1. 在 **所有销售订单** 列表页上，选择内部公司销售订单。
1. 在“操作”窗格上，选择 **发票** 选项卡，然后选择 **发票**。
1. 选中 **过帐** 复选框。
1. 选择 **确定**。

    在法人 BBB 中过帐内部公司销售订单的客户发票。

## <a name="process-the-intercompany-product-receipt-and-vendor-invoice"></a>处理内部公司产品收据和供应商发票

如示意图中所示，在法人 AAA 中执行以下步骤。

1. 转到 **应付帐款 \> 采购订单 \> 所有采购订单**。
1. 在 **所有采购订单** 列表页上，选择内部公司采购订单。
1. 在“操作”窗格上，选择 **收据** 选项卡，然后选择 **产品收据**。 将会创建产品收据。 产品收据编号与内部公司装箱单编号相同。
1. 选中 **过帐** 复选框。
1. 选择 **确定**。
1. 在 **所有采购订单** 列表页上，选择内部公司采购订单。
1. 在操作窗格上，选择 **发票**，然后选择 **发票**。 将会创建供应商发票。 供应商发票编号与内部公司客户发票编号相同。
1. 完成输入供应商发票，然后过帐发票。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
