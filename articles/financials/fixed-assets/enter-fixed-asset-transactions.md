---
title: 固定资产交易记录选项
description: 本主题介绍可用来创建固定资产交易记录的不同方法。
author: ShylaThompson
manager: AnnBe
ms.date: 02/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6362a63bca43b5ac8da14becf6b966e459365ce1
ms.sourcegitcommit: 68df883200b5c477ea1799cc28d3ef467cd29202
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/07/2019
ms.locfileid: "377174"
---
# <a name="fixed-asset-transaction-options"></a>固定资产交易记录选项

[!include [banner](../includes/banner.md)]

本主题介绍可用来创建固定资产交易记录的不同方法。

您可以使用应收账款、应付账款、采购和源，以及总帐设置集成的固定资产。 如果您要在内部使用这些物料，您还可以将库存管理中的物料转移到固定资产。

## <a name="accounts-payable"></a>应付账款
您可以在“日记帐凭证”页中输入固定资产交易记录。 此页可以从“发票日记帐”页中打开。 您还可以从“发票审核日记帐”页中打开“日记帐凭证”页。 在“对方科目类型”字段中，选择“固定资产”。 然后，在“对方科目”字段中，选择一个固定资产编号作。 在“固定资产”选项卡上，在“交易记录类型”和“帐簿”字段中输入值。

## <a name="accounts-receivable"></a>应收账款
您可以在“普通发票”页中输入固定资产交易记录。  在“普通发票”页中的“发票行”窗格中，选择一个行项。 单击“行明细”快速选项卡。 为处置交易记录输入固定资产编号和帐簿。 对于普通发票，固定资产交易记录的类型始终是“处置 - 出售”。

## <a name="procurement-and-sourcing"></a>采购
您可以在“采购订单”页中输入固定资产交易记录。 输入必需的信息创建采购订单，然后单击“确定”。 在“采购订单”页中，单击“行明细”快速选项卡。 然后，在“固定资产”选项卡上，输入有关固定资产的信息。 

若要过帐现有固定资产的购置交易记录，请指定固定资产编号、帐簿和交易记录类型。 如果缺少此信息中任何信息，则不能过帐固定资产。 若要过帐新的固定资产的购置交易记录，请选择“是否新建固定资产?”选项，然后选择要将新资产分配到的固定资产组。 但是，如果物料处于使用标准成本库存模型的库存模型组中，则对于某一行将没有固定资产字段可用。 此外，在“固定资产参数”页中定义的选项确定是否可以过帐来自采购模块的购置交易记录。 

将采购订单或存货转为固定资产日记帐用于购置固定资产时，将会影响库存成本。

## <a name="general-ledger"></a>总帐
任何一种固定资产交易记录类型都可以在“普通日记帐”页中过帐。 您还可以在固定资产中使用日志过帐固定资产交易记录。

## <a name="options-for-entering-fixed-asset-transaction-types"></a>用于输入固定资产交易记录类型的选项


| 交易记录类型                    | 模块                   | 期权                                   |
|-------------------------------------|--------------------------|-------------------------------------------|
| 购置、购置调整 | 固定资产             | 固定资产、库存转为固定资产   |
|                                     | 总帐           | 普通日记帐                           |
|                                     | 应付账款         | 发票日记帐、发票审核日记帐 |
|                                     | 采购 | 采购订单                            |
| 折旧                        | 固定资产             | 固定资产                              |
|                                     | 总帐           | 普通日记帐                           |
| 处置                            | 固定资产             | 固定资产                              |
| ** **                               | 总帐           | 普通日记帐                           |
| ** **                               | 应收帐款      | 普通发票                         |


固定资产的折旧期间剩余值在通过数据实体手动创建或导入折旧交易记录类型日记帐行时不更新。 在折旧方案流程用于创建日记帐行时，此值将更新。

有关详细信息，请参阅[固定资产集成](fixed-asset-integration.md)。
