---
title: 拆分发票功能
description: 本主题介绍了按交货地址和税务帐号 (TAN) 拆分发票的设置和功能。
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: f1dac8d51c24009dcf0c4acbc49f06f32abf0dec
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2022
ms.locfileid: "8724660"
---
# <a name="split-invoice-functionality"></a>拆分发票功能

[!include [banner](../includes/banner.md)]

本主题介绍了按交货地址和税务帐号 (TAN) 拆分发票的设置和功能。

在 **应付帐款参数** 页面的 **常规** 选项卡上，选中 **产品收据** 或 **发票** 复选框以过帐和拆分在 **采购订单** 页面上具有不同交货地址和 TAN 的产品收据或发票。 然后，按交货地址和 TAN 拆分已过帐的发票。

在 **汇总更新** 选项卡上，在 **拆分依据** 快速选项卡的 **交货信息** 行中，将 **确认**、**领料单**、**装箱单** 或 **发票** 选项设置为 **是**，以过帐和拆分在 **销售订单** 页面上为不同的发票行定义不同的交货地址和 TAN 的确认、领料单、装箱单或发票。 依次按交货地址和 TAN 拆分发票。

> [!IMPORTANT]
> - 如果 **交货信息** 的选项均为设置为 **是**，该发票作为单个发票过帐。 不会进行发票拆分。
> - 若要拆分和过帐发票行具有不同交货地址和 TAN 的装箱单，必须将 **交货信息** 的 **装箱单** 选项设置为 **是**。
> - 若要拆分和过帐发票行具有不同交货地址和 TAN 的发票，必须将 **交货信息** 的 **发票** 选项设置为 **是**。
> - 若要过帐发票行具有不同交货地址，但具有相同 TAN 的发票，必须将 **交货信息** 的 **发票** 选项设置为 **否**。 按交货地址拆分发票。

## <a name="example"></a>示例

在此示例中，在 **应付帐款参数** 页面的 **汇总更新** 选项卡上，将 **交货信息** 的 **发票** 选项设置为 **是**。 过帐在行上对交货地址和 TAN 具有以下设置的采购发票：

- **物料行 1：** 交货地址 1，TAN-ABCD12345A
- **物料行 2：** 交货地址 1，TAN-ABCD12345A
- **物料行 3：** 交货地址 2，TAN-ABCE12345B
- **物料行 4：** 交货地址 3，TAN-ABCD12345A

在此情况下，原始发票将拆分为两个发票，并通过以下方式过帐：

- 针对物料行 1 和物料行 2 过帐发票 1，因为这两行具有相同的交货地址和 TAN。
- 针对物料行 3 过帐发票 2。
- 针对物料行 4 过帐发票 3。
