---
title: "调整仓库中的库存级别（基本仓库）"
description: "该过程向您介绍创建和过帐库存调整日记帐以调整仓库中的产品库存水平。"
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9ca5841fe857990cae8d9551ccf79c3c0fd490ae
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# 调整仓库中的库存级别（基本仓库）

[!include[task guide banner](../../includes/task-guide-banner.md)]

该过程向您介绍创建和过帐库存调整日记帐以调整仓库中的产品库存水平。 在开始前，您需要为库存调整设置一个库存日记帐名称。 您可以使用演示数据公司 USMF 或您自己的数据浏览此程序。 这些任务通常由仓库员工完成。


## 创建一个库存调整日记帐
1. 转到“库存管理”>“日记帐条目”>“物料”>“库存调整”。
2. 单击“新建”。
3. 在“名称”字段中，单击下拉按钮以打开查找。
4. 在列表中，单击您要使用的库存调整日记帐名称。
    * 其他一些字段将根据您所选择的库存调整日记帐名称的设置填充数据。  
5. 单击“确定”。

## 创建日记帐行
1. 单击“新建”。
2. 在列表中，标记该物料编号字段。
3. 在“物料编号”字段中，选择一个物料。 如果您使用演示数据公司 USMF，键入 "D0001"。
4. 在“位置”字段中，单击下拉按钮打开查询。
5. 在列表中，选择一个站点。
6. 在“仓库”字段，单击下拉按钮以打开查找。
7. 在列表中，选择一个仓库。
    * 如果您选择了一个强制性库存维度物料，就必须在此指定该库位。  
8. 在“数量”字段中，输入一个数字。
    * 成本价格字段详细说明了库存收入每个单元的成本。 如果该物料数目的成本没有指定，或者需要手动更改，请在此输入。  

## 验证并过帐库存调整日记帐
1. 单击“验证”。
2. 单击“确定”。
3. 单击“过帐”。
    * 过帐此类日记帐时，将过帐库存收货或发货单，更改库存水平及其值，同时生成分类帐交易记录。  
4. 单击“确定”。
5. 关闭窗体。
6. 关闭该页面。

