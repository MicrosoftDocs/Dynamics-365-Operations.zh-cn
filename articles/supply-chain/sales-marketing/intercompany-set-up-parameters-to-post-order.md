---
title: 设置用于过帐内部公司订单的参数
description: 本文说明如何设置用于过帐内部公司订单的参数
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 97ea0061d57beede6350eecfd497c12dd37aea31
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900787"
---
# <a name="set-up-parameters-to-post-an-intercompany-order"></a>设置用于过帐内部公司订单的参数

[!include [banner](../../includes/banner.md)]

在过帐内部公司客户发票时，您可以将它设置为自动过帐内部公司采购订单和原始客户发票。

> [!NOTE]
> 在执行此过程前，请在您的组织中设置打印管理，以指向正确的发票打印机。 这将确保原始销售订单的发票在正确的打印机上打印。

您必须设置以下参数：

1. 转到 **销售和营销 \> 销售订单 \> 所有销售订单**。 选择要处理的销售订单。
1. 在“操作”窗格的销售订单上，选择 **查看标题**，然后选择 **内部公司设置** 快速选项卡并打开。
1. 转到“操作”窗格，在 **销售订单** 选项卡上，选择 **编辑**。
1. 返回 **内部公司设置** 快速选项卡，然后选择 **直接交货** 以实现在整个内部公司业务关系链（所有订单）中直接交货。
1. 选择 **保存** 以保存使用新设置的销售订单。 然后选择 **关闭** 以关闭销售订单。
1. 转到 **采购 \> 供应商 \> 所有供应商**。 在 **常规** 选项卡上，选择 **内部公司**。
1. 在 **内部公司** 页上，选择 **采购订单策略** 链接。 在 **内部公司采购订单（直接交货）** 字段组中，选择 **自动过帐发票**，并从 **自动打印发票** 字段中删除复选标记。
1. 在 **原始销售订单（直接交货）** 字段组中，选择 **自动过帐发票** 字段和 **自动打印发票** 字段。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
