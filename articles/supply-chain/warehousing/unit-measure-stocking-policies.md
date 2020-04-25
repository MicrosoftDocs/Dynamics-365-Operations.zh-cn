---
title: 度量单位和库存政策
description: 本文介绍如何在仓库流程中使用默认单位、单位序列和单位换算。
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetails, EcoResProductDetailsExtended, EcoResStorageDimensionGroup, InventItemOrderSetup, UnitOfMeasureConversion, WHSRFMenuItem, WHSUOMSeqGroupTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 29611
ms.assetid: 4b5ca875-9a06-416d-9ac0-cc3ab8f7338e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6bd6a3ea9d7b339df99ffa65f058fc4b98b58b9c
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216681"
---
# <a name="unit-of-measure-and-stocking-policies"></a>度量单位和库存政策

[!include [banner](../includes/banner.md)]

本文介绍如何在仓库流程中使用默认单位、单位序列和单位换算。

单位序列组定义可用于仓库工序的单位序列。 它们在**单位序列组**页上创建。 该序列显示各种单位的关系。 例如，您存储包含包含物料的单独部分的箱的托盘。 在这种情况下，您必须提供三种不同的单位和层的逻辑顺序。 单位序列组可以定义牌照分组策略，以及应为各种仓库流程使用的默认单位。 本文适用于可用于仓库管理的高级仓库解决方案，以及可用于库存管理的更为基本的仓库解决方案。

## <a name="unit-sequence-groups-for-released-products"></a>已发布产品的单位序列组
如果您要在仓库工作流程中使用已发布产品，单位序列组必须分配给它们。 如果您验证与某一存储维度组关联的产品，且**使用仓库管理流程**选项设置为**是**，如果单位序列组 ID 没有为该产品定义，您将收到错误消息。 如果您使用的单位序列组包含多行（因而包含多个单位），则您必须设置在单位之间的单位换算。 您在**单位换算**页上完成此设置。 与已发布产品相关联的序列组中的最小单位必须匹配对相关产品定义的库存单位。 库存单位是用于现有库存量的基本计算的单位。 您还可以使用**启用度量单位转换**选项设置基础产品产品变型的度量单位转换。

## <a name="license-plate-grouping"></a>牌照分组
您可以指定是否应将少于或多于一个特定单位的收据分组到一个牌照中，或划分为适用于每个单位的牌照。 若要设置此行为，请使用**单位序列组**页**行明细**选项卡上的**牌照分组**选项。 如果您要通过使用移动设备在处理工作时使用牌照分组，则必须在**移动设备**菜单项上选择**牌照分组**选项。 例如，您使用一个移动设备登记与具有两行的单位序列组关联的物料。 第一行用于“件”，并且**牌照分组**选项设置为**是**。 第二行用于“托盘单位”，并且**牌照分组**选项设置为**否**。 在这种情况下，系统会自动引导牌照的拆分和创建每 100 件的。

## <a name="units-for-cycle-counting"></a>周期盘点的单位
若要定义如此单位应用作周期盘点流程的一部分，请在**单位序列组**页选择**对周期盘点使用单位**选项。 可以选择序列组中最大的四个单位。 如果您选择的单位超过四个，其他单位将不会显示在移动设备上。

## <a name="default-units-for-mobile-device-receiving-processes"></a>移动设备接收流程的默认单位
若要设置用于移动设备接收流程的默认单位，则可以在**单位序列组**页启用**默认的采购和转移单位**和**默认生产单位**选项。 例如，您可以指定，默认情况下，在使用移动设备接收采购订单现有库存量时系统应使用“托盘数量”，但库存单位应是“件”。 若要获取每个托盘包含的件数的换算，必须定义单位换算，例如 100 件 = 1 PL。

## <a name="default-order-settings"></a>默认订单设置
作为已发布产品创建的一部分，必须选择默认的采购、销售以及库存单位来处理各个订单。 您可以使用**默认订单设置**页和**站点特定的订单设置**页来设置各个原始凭证的默认单位和数量。 您可以从**已发布产品**页访问这些页面。



