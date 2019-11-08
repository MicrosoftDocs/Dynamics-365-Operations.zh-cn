---
title: 行动消息
description: 行动消息是系统生成的关于更改现有计划订单或确定订单的建议。
author: ChristianRytt
manager: AnnBe
ms.date: 10/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19411
ms.assetid: 52b46d93-7d02-46b5-aad1-9fd08206bf9d
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a74feeaf61e93ed2802b5f45941d7e15e947b615
ms.sourcegitcommit: 574309903f15eeab7911091114885b5c7279d22a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/24/2019
ms.locfileid: "2658944"
---
# <a name="action-messages"></a>行动消息

[!include [banner](../includes/banner.md)]

行动消息是系统生成的关于更改现有计划订单或确定订单的建议。

## <a name="introduction"></a>简介

行动消息由主计划计算生成，以响应变化的需求。 例如，装运日期或数量可能已在您已在其上创建了采购订单以满足需求的销售订单上发生了更改。 在这种情况下，一个或多个行动消息由主计划计算生成以更新采购订单。 您决定是否进行所建议的更改。

您可以设置如何为附加到物料的覆盖范围组计算行动消息。

## <a name="select-action-messages"></a>选择行动消息

在**覆盖范围组**页上，您可以选择您希望系统生成的行动消息和消息适用的覆盖范围组或物料。 您可以选择以下行动消息。

| 消息             | 描述                                                                                                                                                                                                                                              |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **提前**         | 如果您选择此消息，系统将在需要时生成行动消息，以将订单移动到更早的日期。 在**提前宽限期**字段中，您还可以指定无提前行动的收货与发货之间的最大天数。 |
| **延期**        | 如果您选择此消息，系统将在需要时生成行动消息，以将订单移动到更晚的日期。 在**延长宽限期**字段中，您还可以指定无延迟行动的收货与发货之间的最大天数。       |
| **减少**        | 如果您选择此消息，则生产订单、采购订单或其他收货交易记录应减少，以避免超出库存水平。                                                                                                   |
| **增加**        | 如果您选择此消息，则生产订单、采购订单或其他收货交易记录应增加，以避免库存出现短缺。                                                                                                    |
| **派生的行动** | 如果选择此消息，则会为派生的需求创建行动消息，例如，针对组件订单满足生产的行动。                                                                                                   |





