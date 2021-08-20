---
title: 检查存货可用性
description: 此过程显示如何检查特定物料编号的现有和实际现有库存量。
author: ShylaThompson
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand, InventOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 894c153761dc29e3d5d9fc22900d96a50ae33b6d5db92623118e229a9aedafe4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758632"
---
# <a name="check-the-availability-of-stock"></a>检查库存可用性

[!include [banner](../../includes/banner.md)]

此过程显示如何检查特定物料编号的现有和实际现有库存量。 它还向您显示如何获取有关物料的供应信息。 实际现有库存量为可用现有库存量，即购买、接收和登记的库存量。 现有库存量不仅包括可用的现有库存量，而且还包括已经订购但尚未收到或登记的库存量。 您可以使用演示数据公司 USMF 或您自己的数据浏览此程序。 如果您正在使用 USMF，则可以使用显示的示例值。 这些任务通常由仓库工作人员完成。


## <a name="check-on-hand-inventory-for-an-item"></a>检查物料的现有库存量
1. 转到 **导航窗格 > 模块 > 库存管理 > 查询和报表 > 现有库存量**。
2. 选择 **物料编号** 行。 要按物料编号查询现有库存量，请选择“表”设置为 **现有库存量** 和“字段”设置为 **物料** 编号的行。
3. 在 **标准** 字段中，选择要查询的物料。 如果您正在使用 USMF 演示数据公司，则可以选择“M9201”。  
4. 单击 **确定**。
5. 在 **操作窗格** 上，单击 **维度**。 **维度** 选项卡允许您选择您要查看的现有库存信息的详细程度。 如果您需要有关预留的数据，则必须显示使用高级仓库程序 (WMS) 物料的所有库存维度。
6. 单击 **确定**。
7. 在 **操作窗格** 上，单击 **相关信息**。 如果未看到此选项，则需要单击省略号按钮 (…) 以查看其他的操作窗格选项。
8. 单击 **供给概览**。 **供给概览** 选项卡提供了特定物料的供应信息，例如现有数量、提前期和供应商信息。  
9. 展开 **现有量** 部分。
10. 展开 **供应商** 部分。
11. 关闭该页面。
12. 关闭该页面。

## <a name="check-physical-on-hand-inventory"></a>检查实际现有库存
1. 转到 **导航窗格 > 模块 > 仓库管理 > 查询和报表 > 实际现有库存量**。
2. 在 **项目编号** 字段中，键入一个值。 您可以使用“站点和仓库”字段筛选物料列表。 
3. 刷新该页面。
4. 在 **操作窗格** 上单击 **显示维度**。 “维度显示”选项卡允许您选择您要查看的现有库存信息的详细程度。
5. 单击 **确定**。
6. 关闭该页面。

## <a name="check-on-hand-inventory-by-location"></a>按库位查看现有库存量
1. 转到 **导航窗格 > 模块 > 仓库管理 > 查询和报表 > 按库位显示的现有量**。
2. 在 **仓库** 字段中，键入一个值。 如果您正在使用 USMF 演示数据公司，则可以使用“51”。  
3. 刷新该页面。
4. 单击 **显示维度**。
5. 单击 **确定**。
6. 关闭该页面。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]