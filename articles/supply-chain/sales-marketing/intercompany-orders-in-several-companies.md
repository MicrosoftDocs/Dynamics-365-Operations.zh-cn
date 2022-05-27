---
title: 在多个公司中创建内部公司采购订单和销售订单
description: 本主题介绍了如何在多个公司中创建内部公司采购订单或销售订单
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
ms.openlocfilehash: 8458a08c1a2e5e656c496eb74188d0e2e7257020
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673709"
---
# <a name="creating-intercompany-purchase-and-sales-orders-in-several-companies"></a>在多个公司中创建内部公司采购订单和销售订单

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management 并不限于只处理一个生产公司和多个销售公司。 为内部公司设置的所有公司都既可以是贸易公司，也可以是生产公司。

如果可以提供相同物料的公司不止一家，则可以任意选择一家公司来购买。即使一个销售订单变成多个采购订单，也可以进行更新。

使用和自动创建一个内部公司采购订单相同的方法，您可以在公司中创建原始销售订单，然后创建多个内部公司采购订单，通过多个集团内部供应商公司来完成该订单。 Microsoft Dynamics 365 Supply Chain Management 可以在供应商公司中自动创建内部公司销售订单。

要完成此任务，所有公司必须设置为贸易关系。 必须在 Microsoft Dynamics 365 Supply Chain Management 中将供应商公司设置为公司内部供应商，而且它们必须是相关物料的首选供应商。 在销售订单上的 **标题视图** 中，您必须在 **内部公司设置** 快速选项卡上选择 **自动创建内部公司订单** 字段和 **直接交货** 字段。 这是默认设置。

您按照常用的方法创建了销售行。 当您退出记录时，将出现一条消息，通知您已创建内部公司采购订单和内部公司销售订单。 该消息包含到新订单的链接。 若要查看您的供应商公司中创建的内部公司销售订单，请打开原始销售订单，然后在 **常规** 选项卡的 **相关信息** 组中选择 **参考**。

如果打开供应商的内部公司采购订单，您将看到 Microsoft Dynamics 365 Supply Chain Management 会为每个供应商自动填写原始销售订单编号和内部公司销售订单编号。

同样，如果打开供应商的内部公司销售订单，您将看到 Microsoft Dynamics 365 Supply Chain Management 会为每个供应商自动填写原始销售订单编号和内部公司采购订单编号。

> [!NOTE]
> 如果在单物料存在于其中一个内部公司供应商公司中但不存在于其他公司中，则 Microsoft Dynamics 365 Supply Chain Management 将为存在物料的供应商公司创建内部公司订单，但禁止为其他公司创建订单。 出现这种情况时会显示一条通知消息。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
