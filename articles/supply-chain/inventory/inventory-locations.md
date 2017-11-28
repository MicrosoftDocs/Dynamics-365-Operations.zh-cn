---
title: "库存库位"
description: "库存库位用于与基本仓库 (WMS I) 一同确定物料的存储位置和从 WMS I 仓库领取物料的位置。"
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSLocation
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations
ms.custom: 2134
ms.assetid: 69bf6922-4151-447f-b678-4ba95637f54c
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 186ad9fbf2920ce9cc01a686b133a2de568d7fef
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="inventory-locations"></a>库存库位

[!include[banner](../includes/banner.md)]


库存库位用于与基本仓库 (WMS I) 一同确定物料的存储位置和从 WMS I 仓库领取物料的位置。

此主题适用于库存管理模块中的功能。 它不适用于仓库管理模块中的功能。

术语库位表示提取物料的位置。

对于每个库位，还可以指定插入物料的位置。 在默认情况下，它们是相同的。 通常从库位的同一侧插入和提取物料，但并非始终如此。 例如，保存在鲜活物品货架上的物料从一个通道插入而从另一个通道提取。 主要输入由库存名称给定，该库存名称通常由其坐标（仓库、通道、货架、货位和箱）确定。 例如，在“库存库位”页中，01-02-03-4 表示通道 1、货架 2、货位 3、储料箱 4。
库位属性

库位具有下列特性：
-   尺寸（高度、宽度、深度和体积）
-   仓库、通道、货架、货位和箱位置
-   库位类型（堆放库位、领料库位、进货台、出货台、生产输入位置、检查库位或看板超市）

可以在联机系统中使用检查文本以验证操作员为特定物料选择了正确的库位。 此检查文本可以手动创建，也可以采用默认值。

## <a name="sort-codes"></a>排序代码
使用分类代码优化领料单的处理，领料单介绍了库存中的领取物料以及领料订单所需的信息。 可以按通道和其他坐标指定分类代码，或者将它们手动分配给库位。

## <a name="blocked-locations"></a>锁定的库位
有时，您可能想要指示库位锁定一段时间，例如在进行修理时。 有时，您可能希望指示只锁定输入或输出。

## <a name="tree-structure"></a>树状结构

在“库存库位”页，您可以以基于库存库位坐标的树状结构，以定义的显示格式查看仓库布局。

## <a name="maintain-inventory-locations-via-the-warehouse-form"></a>通过仓库窗体维护库存库位

可以通过向导将库位从一个仓库复制到另一个以及创建库位。 在运行向导之前，应确保您在“仓库”页已定义了默认库位名称。



<a name="see-also"></a>请参阅
--------

[创建新仓库布局（任务指南）](tasks/create-new-warehouse-layout.md)

