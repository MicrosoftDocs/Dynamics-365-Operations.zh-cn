---
title: 库存状态
description: 本文介绍如何使用库存状态来分类和跟踪库存。
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, WHSInventStatus
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 21331
ms.assetid: b35f495f-de4f-48a0-9d09-4d06781d7650
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e96ed6d01e22ee2cbc5b3b2be8168fbb43904c89
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212702"
---
# <a name="inventory-statuses"></a>库存状态

[!include [banner](../includes/banner.md)]

本文介绍如何使用库存状态来分类和跟踪库存。

您可以使用库存状态对库存分类。 您然后可以开始相应的操作，例如补货或入库工作。

这是您可以使用库存状态的方式的一些示例：

-   创建现有库存量、进货交易记录和出货交易记录的库存状态。
-   为仓库交易记录指定默认库存状态。
-   在物料到达前、到达时或在库存移动期间储存物料时，更改物料的库存状态。
-   使用库存状态为退回的物料定价，并在主计划期间计划物料覆盖范围。

库存状态是存储维度组中的一个维度。 库存状态可归类为可用或不可用，您可以使用**库存锁定**参数锁定具有不可用库存状态的物料。 具有锁定状态的物料被视为实际库存，并且不能在生产订单、销售订单、转移定单或出货交易记录中使用。

您可以为进货工作使用具有可用或不可用库存状态的仓库物料。 例如，您创建名为**就绪**的可用状态，名为**已损坏**的不可用状态，和名为**已锁定**的锁定状态。 在您创建已接收或退回物料的采购订单时，如果任何物料已损坏或已中断，您可以在采购订单行上更改这些物料的库存状态为**已损坏**。 在这些物料接收后，状态自动设置为**已锁定**。 如果您通过使用移动设备扫描已损坏的物料，Supply Chain Management 可以使用位置指令和工作模板来显示有关您可以将这些物料入库的适当位置或位置范围的信息。 对于退回的物料，在**库存交易记录**页中创建**预留**的发货类型。

对于出货工作，使用具有个可用库存状态的物料。 如果您有处于**已中断**状态的物料，并且主计划运行这些物料，则将物料视为缺失，库存会自动补货。

在设置库存状态后，您可以为站点、物料和仓库设置默认库存状态。 您还可以设置销售、转移和采购订单的默认状态。 销售订单和出货转移单的默认状态不能将**库存锁定**选项设置为**是**。 从站点、仓库、物料、采购订单、转移单或销售订单的默认设置继承的库存状态可通过使用移动设备，或者在采购订单、销售订单或转移单行上更改。

若要计划具有可用库存状态的物料的覆盖范围，则在**存储维度组**页为存储维度选择**按维度的覆盖范围计划**选项。 当您打开**物料覆盖范围**向导时，具有可用状态的物料显示在**状态**页。 若要创建这些物料的覆盖范围设置，请为可用库存状态选择库存状态 ID。 基于覆盖范围设置，在主计划期间您可以计算物料需求并预测可用物料的供应和需求。 您无法创建具有锁定库存状态的物料覆盖范围设置。 或者，使用**物料覆盖范围**页来创建或修改物料覆盖范围参数。
