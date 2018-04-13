--- 
title: "创建基础产品"
description: "为预定义变型创建基础产品。"
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f944258e7efdd5c9eba7daf9a80c67058a6cc055
ms.openlocfilehash: 6e5cf92f7736523faf25ac97278a8a273e14ff88
ms.contentlocale: zh-cn
ms.lasthandoff: 10/25/2017

---
# <a name="create-a-product-master"></a>创建基础产品

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

为预定义变型创建基础产品。 创建此程序的演示数据公司是 USMF。 此过程专门针对产品设计人员。


## <a name="create-a-new-product-master"></a>新建基础产品
1. 转到“产品信息管理”>“产品”>“基础产品”。
2. 单击“新建”。
3. 在“产品编号”字段中，键入一个值。
    * 其编号必须是唯一的。 可在“产品编号”字段设置编号顺序。 在这种情况下，用户不必输入一个值。  
4. 在“产品名称”字段中，键入一个值。
    * 输入产品的描述性名称。 该值默认为搜索名称，不过用户可以更改。  
5. 在“产品维度组”字段中，单击下拉按钮以打开查找。
    * 产品维度组确定可用于创建产品变型的 4 个产品维度。 此示例使用颜色和大小组。  
6. 在列表中，找到并选择所需记录。
7. 在列表中，单击所选行中的链接。
    * 默认配置技术是预定义变型。 这将在此示例中使用。  
8. 单击“确定”。

## <a name="select-product-dimension-groups"></a>选择产品维度组
1. 在“颜色组”字段中，单击下拉按钮以打开查找。
2. 在列表中，找到并选择所需记录。
3. 在列表中，单击所选行中的链接。
4. 在“大小组”字段中，单击下拉按钮以打开查找。
5. 在列表中，找到并选择所需记录。
6. 在列表中，单击所选行中的链接。

## <a name="add-dimension-groups"></a>添加维度组
1. 在操作窗格上，单击“产品”。
2. 单击“维度组”以打开下拉对话框。
3. 在“存储维度组”字段中，单击下拉按钮以打开查找。
    * 存储维度帮助您控制物料存储方式和库存提取方式。 例如，存储维度可包括站点和仓库。  
4. 在列表中，找到并选择所需记录。
5. 在列表中，单击所选行中的链接。
6. 在“跟踪维度组”字段中，单击下拉按钮以打开查找。
    * 跟踪维度组确定可以添加到产品中的跟踪维度。 例如，批号和序列号用于跟踪库存物料。  
7. 在列表中，找到并选择所需记录。
8. 在列表中，单击所选行中的链接。
9. 单击“确定”。
10. 单击“保存”。
11. 关闭该页面。


