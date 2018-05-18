---
title: "检查存货可用性"
description: "此过程显示如何检查特定物料编号的现有和实际现有库存量。"
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 62338fe11c30781f264e626fad835a2ba9dca837
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="check-the-availability-of-stock"></a>检查库存可用性

[!include [task guide banner](../../includes/task-guide-banner.md)]

此过程显示如何检查特定物料编号的现有和实际现有库存量。 它还向您显示如何获取有关物料的供应信息。 实际现有库存量为可用现有库存量，即购买、接收和登记的库存量。 现有库存量不仅包括可用的现有库存量，而且还包括已经订购但尚未收到或登记的库存量。 您可以使用演示数据公司 USMF 或您自己的数据浏览此程序。 如果您正在使用 USMF，则可以使用显示的示例值。 这些任务通常由仓库工作人员完成。


## <a name="check-on-hand-inventory-for-an-item"></a>检查物料的现有库存量
1. 转到“库存管理”>“查询和报表”>“现有库存量”。
2. 选择物料编号行。
    * 要按物料编号查询现有库存量，请选择“表”设置为现有库存量和“字段”设置为物料编号的行。  
3. 在“标准”字段中，选择要查询的物料。
    * 如果您正在使用 USMF 演示数据公司，则可以选择“M9201”。  
4. 单击“确定”。
5. 单击“维度”。
    * “维度”选项卡允许您选择您要查看的现有库存信息的详细程度。 如果您需要有关预留的数据，则必须显示使用高级仓库程序 (WHS) 物料的所有库存维度。  
6. 单击“确定”。
7. 在“操作”窗格上，单击“相关信息”。
    * 如果未看到它，则需要单击省略号按钮 (…) 以查看其他的操作窗格选项。  
8. 单击“供给概览”。
    * “供应概览”选项卡提供了特定物料的供应信息，例如现有数量、提前期和供应商信息。  
9. 展开“现有量”部分。
10. 展开“供应商”部分。
11. 关闭该页面。
12. 关闭该页面。

## <a name="check-physical-on-hand-inventory"></a>检查实际现有库存
1. 转到“库存管理”>“查询和报表”>“实际现有库存量”。
2. 在“项目编号”字段中，输入一个值。
    * 您可以使用“站点和仓库”字段筛选物料列表。  
3. 刷新该页面。
4. 单击“显示维度”。
    * “维度显示”选项卡允许您选择您要查看的现有库存信息的详细程度。  
5. 单击“确定”。
6. 关闭该页面。

## <a name="check-on-hand-inventory-by-location"></a>按库位查看现有库存量
1. 转到“仓库管理”>“查询和报表”>“现有库位”。
2. 在“仓库”字段中，键入一个值。
    * 如果您正在使用 USMF 演示数据公司，则可以使用“51”。  
3. 刷新该页面。
4. 单击“显示维度”。
5. 单击“确定”。
6. 关闭该页面。

