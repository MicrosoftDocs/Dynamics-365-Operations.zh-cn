---
title: 盘点仓库中的库存
description: 本主题介绍创建和过帐库存盘点日记帐，以盘点仓库一个库位的特定物料的步骤。
author: MarkusFogelberg
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a0909625f31d15fe6b1387ff9ab7fd5d9a9135f4
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836432"
---
# <a name="count-inventory-in-a-warehouse"></a>盘点仓库中的库存

[!include [task guide banner](../../includes/task-guide-banner.md)]

本主题介绍创建和过帐库存盘点日记帐，以盘点仓库一个库位的特定物料的步骤。 该过程适用于“基础仓储”功能，在库存管理模块可用，在仓库管理模块的仓储功能不可用。 您可以使用演示数据公司 USMF 或您自己的数据浏览此程序。 如果您使用自己的数据，确保您有产品和库位设置，并且您为盘点日记帐创建了库存日记帐名称。 库存盘点通常由仓管人员执行。


## <a name="create-an-inventory-counting-journal"></a>创建库存盘点日记帐
1. 转到**导航窗格 > 模块 > 库存管理 > 日记帐条目 > 物料盘点 > 盘点**。
2. 选择**新建**。
3. 在**名称**字段中，从下拉列表选择要使用的库存盘点日记帐名称。 将根据您选择的库存盘点日记帐的设置填充一些其他字段。  
4. 在**工人**字段中，选择下拉按钮以打开查找。
5. 在列表中，**选择**您想要使用的工人。
6. 选择**确定**。

## <a name="create-journal-lines"></a>创建日记帐行
1. 选择**新建**。
2. 在**物料编号**字段中，从下拉列表选择所需记录。 如果您使用演示数据公司 USMF，选择 **A0001**。  
3. 在**站点**字段中，从下拉列表选择所需记录。 如果您使用演示数据公司 USMF，选择站点 **2**。
4. 在**仓库**字段中，从下拉列表选择所需记录。 如果您使用演示数据公司 USMF，请选择仓库 **24**。  
5. 在**位置**字段中，从下拉列表选择所需记录。 如果您使用演示数据公司 USMF，选择 **散装-001**。  
6. 在“已盘点”字段中，输入一个数字。 如果您输入的盘点数字与**现有量**字段显示的数字不同，**数量**字段会更新此差异。  
7. 选择**保存**。

## <a name="post-the-inventory-counting-journal"></a>过帐库存盘点日记帐
1. 选择**过帐**。 在您过帐库存盘点日记帐时，如果盘点数与**现有量**字段报告的数额不同，会过帐库存收货或问题，更改库存水平和价值和生成分类帐交易记录。
2. 选择**确定**。

## <a name="view-inventory-transactions"></a>查看库存交易记录
1. 选择**库存**。
2. 选择**交易记录**。 在这里，您可以查看过帐库存盘点日记帐时创建的所有相关交易记录。   

