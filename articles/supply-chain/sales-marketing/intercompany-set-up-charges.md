---
title: 对内部公司订单设置费用
description: 本主题说明如何对内部公司订单设置费用
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: CustTable, VendTable, EcoResProductListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 27633e09bfcf41fbbe5449b0d3b5f283eaf7ee13
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673653"
---
# <a name="set-up-charges-on-intercompany-orders"></a>对内部公司订单设置费用

[!include [banner](../../includes/banner.md)]

您可以设置要添加到内部公司订单中的费用。 当添加某费用到内部公司销售订单时，它将自动同步化到内部公司采购订单。 以两种方式工作—从内部公司销售订单到采购订单，以及另一种方法。

您还可以通过将费用定义为内部公司百分比，使用费用将利润添加到内部公司销售订单。

当您设置应用于内部公司订单的费用时，您启用了来自原始销售订单金额的公司内部销售订单的内部利润的计算。 如果您的内部公司供应商以成本价卖给您，则您可能将要执行此操作。 以下程序介绍了如何针对内部公司客户执行此操作。 针对供应商，您可以使用相同的程序。

1. 转到 **应收帐款 \> 设置 \> 费用 \> 客户费用组**。
1. 创建一个费用组。
1. 转到 **应付帐款 \> 客户 \> 所有客户**。 选择客户帐户链接。 在“操作”窗格上，选择 **客户** 选项卡，然后选择 **销售订单** 快速选项卡。
1. 在“操作”窗格上选择 **编辑** 以启用对字段的编辑。 在 **费用组** 字段中，选择您在第 2 步设置的内部公司费用组。
1. 转到 **应收帐款 \> 设置 \> 费用 \> 自动费用**。
1. 通过填充相关字段，设置费用。
1. 在 **客户关系** 字段中，选择您在第 2 步设置的内部公司费用组。
1. 在 **行** 快速选项卡的 **类别** 字段中，选择 **内部公司百分比**。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
