---
title: 盘点仓库中的库存
description: 该过程介绍创建和过帐库存盘点日记帐，以盘点仓库一个库位的特定物料的步骤。
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8c0bbfe8f86d27f81b0d577ed89dfa34ebcf3f18
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549877"
---
# <a name="count-inventory-in-a-warehouse"></a>盘点仓库中的库存

[!include [task guide banner](../../includes/task-guide-banner.md)]

该过程介绍创建和过帐库存盘点日记帐，以盘点仓库一个库位的特定物料的步骤。 该过程适用于“基础仓储”功能，在库存管理模块可用，在仓库管理模块的仓储功能不可用。 您可以使用演示数据公司 USMF 或您自己的数据浏览此程序。 如果您使用自己的数据，确保您有产品和库位设置，并且您为盘点日记帐创建了库存日记帐名称。 库存盘点通常由仓管人员执行。


## <a name="create-an-inventory-counting-journal"></a>创建库存盘点日记帐
1. 转到“库存管理”>“日记帐条目”>“物料盘点”>“盘点”。
2. 单击“新建”。
3. 在“名称”字段中，单击下拉按钮以打开查找。
4. 在列表中，单击您要使用的库存盘点日记帐名称
    * 将根据您选择的库存盘点日记帐的设置填充一些其他字段。  
5. 在“工作人员”字段中，单击下拉按钮以打开查找。
6. 在列表中，选择您想要使用的工作人员。
7. 单击“选择”。
8. 单击“确定”。

## <a name="create-journal-lines"></a>创建日记帐行
1. 单击“新建”。
2. 在“物料编号”字段中，单击下拉按钮以打开查找。
3. 在列表中，找到并选择所需记录。
    * 如果您使用演示数据公司 USMF，选择“A0001”。  
4. 在“位置”字段中，单击下拉按钮打开查询。
5. 在列表中，找到并选择所需记录。
    * 如果您使用演示数据公司 USMF，选择站点“2”。  
6. 在“仓库”字段，单击下拉按钮以打开查找。
7. 在列表中，找到并选择所需记录。
    * 如果您使用演示数据公司 USMF，请选择仓库“24”。  
8. 在“地点”字段中，单击下拉按钮以打开查找。
9. 在列表中，找到并选择所需记录。
    * 如果您使用演示数据公司 USMF，选择“散装-001”  
10. 在“已盘点”字段中，输入一个数字。
    * 如果您输入的盘点数字与“现有量”字段显示的数字不同，“数量”字段会更新此差异。  
11. 单击“保存”。

## <a name="post-the-inventory-counting-journal"></a>过帐库存盘点日记帐
1. 单击“过帐”。
    * 在您过帐库存盘点日记帐时，如果盘点数与“现有量”字段报告的数额不同，会过帐库存收货或问题，更改库存水平和价值和生成分类帐交易记录。  
2. 单击“确定”。

## <a name="view-inventory-transactions"></a>查看库存交易记录
1. 单击“库存”。
2. 单击“交易记录”。
    * 在这里，您可以查看过帐库存盘点日记帐时创建的所有相关交易记录。   

