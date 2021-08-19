---
title: 产品因交易而暂停
description: 在确认计划订单后，您将收到一条错误消息，指示物料因交易而暂停。
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8e012a65041c2f32e21d2631eda18eea488e28e35f6a53bbe9a67c08159765e1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752602"
---
# <a name="product-is-on-hold-for-transactions"></a>产品因交易而暂停

错误代码：SYS13295

## <a name="symptoms"></a>故障特征

在确定计划订单后，您将收到以下错误消息：

> 物料 %1 正在等待用于 %2 中的交易记录。

## <a name="cause"></a>原因

在描述锁定的物料时，系统可交换使用术语 *已锁定*、*已停止* 和 *暂停*。 此错误意味着物料在其默认订单设置中设置为 **已停止**。

如果物料已锁定，并且您将其添加到采购订单或销售订单行，您将收到一条警告消息。 当物料已锁定时，将不能修改与采购订单或销售订单行相关的库存交易（例如，当过帐装箱单或发票时）。 您可以锁定已采购物料并同时出售此物料。 在这种情况下，在采购订单上选中 **已停止** 复选框，但未在库存或销售订单上锁定物料。

以下是一些可能导致物料编号锁定而无法出售的条件：

- 物料仍在开发或制造中。 因此，您不希望将其出售或预留。
- 您收到了许多有缺陷的物料，必须更正缺陷才能出售物料。

在这种情况下，您可以锁定此物料，直到解决问题。

如果物料已锁定，并且您创建一个退货单行，您将收到一条消息。 您不能锁定一系列物料或一批物料。 如果必须锁定部分物料，可以通过移动库存或锁定该期间物料的全部存货来锁定它们。

## <a name="resolution"></a>解决方法

- 打开物料的 **默认订单设置** 页面，并清除 **已停止** 复选框。
