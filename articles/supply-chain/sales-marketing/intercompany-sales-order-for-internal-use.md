---
title: 创建内部公司销售订单以供内部使用
description: 本主题说明如何创建内部公司销售订单以供内部使用
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
ms.openlocfilehash: 0718a1560ec42df2a0a12e8b81484aa3be46d2d8
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548121"
---
# <a name="create-an-intercompany-sales-order-for-internal-use"></a>创建内部公司销售订单以供内部使用

[!include [banner](../../includes/banner.md)]

通常，基于内部公司采购订单自动创建内部公司销售订单。 也可以手动创建内部公司销售订单，然后在内部公司客户的法人中生成内部公司采购订单。

![内部公司内部销售流程](media/intercompanyinternalsalesprocess.png)

## <a name="create-an-intercompany-sales-order-manually"></a>手动创建内部公司销售订单

如示意图中所示，在法人 B 中执行以下步骤。

1. 转到 **应收帐款 \> 销售订单 \> 所有销售订单**。
1. 在“操作”窗格中，选择 **销售订单** 以创建销售订单。
1. 在 **创建销售订单** 页面上，选择一个客户帐户。 在 **常规** 快速选项卡上，确保选中 **内部公司** 复选框。 这指示所选客户是内部公司客户。
1. 输入或修改信息，选择 **确定**，然后照常完成订单行。

    从内部销售订单头中复制 **交货地址** 字段值到内部公司采购订单头。 **物料编号** 字段值包含产品维度，且 **交付日期** 和 **货币代码** 字段值从内部销售订单行复制到内部公司采购订单行。

1. 在订单头中，选择 **内部公司** 以查看相关的内部公司采购订单。
1. 在订单行，选择 **内部公司** 以查看与内部公司内部交易有关的信息。

> [!TIP]
> 您可以在 **内部公司订单** 页上查看内部公司销售订单。

> [!NOTE]
> 当您与内部公司合作时，我们建议您在 **应收帐款参数** 页面上清除 **开票后删除订单** 复选框。 否则，将删除相关的采购订单。 我们还建议您在 **应付帐款参数** 页面上清除 **开票后删除采购订单** 复选框。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]