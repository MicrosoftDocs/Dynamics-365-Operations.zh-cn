--- 
title: "创建联产品的物料计划"
description: "生产规划员为属于配方联产品的物料规划物料要求。"
author: YuyuScheller
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
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 4eb36b0de53f40f882950628d55d6ac08ac5fdde
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-material-plan-for-co-products"></a>创建联产品的物料计划

[!include[task guide banner](../../includes/task-guide-banner.md)]

生产规划员为属于配方联产品的物料规划物料要求。 使用 USP2 公司演示数据创建此过程。


## <a name="create-requirement-for-a-co-product"></a>创建联产品的要求
1. 转到“默认仪表板”。
2. 点击“销售订单处理和查询”。
3. 单击“新建”。
4. 单击“销售订单”。
5. 在“客户帐户”字段中，输入一个值。
    * 示例：US-001  
6. 单击“确定”。
7. 在“项目编号”字段中，输入一个值。
    * 示例：P6003  
8. 在“数量”字段中，输入一个数字。
    * 示例：50000  
9. 单击“保存”。

## <a name="create-a-material-plan-for-co-products"></a>创建联产品的物料计划
1. 单击“主计划”。
2. 在“计划”字段中，单击下拉按钮以打开查找。
3. 在列表中，单击所选行中的链接。
    * 示例：主计划  
4. 单击“运行”。
5. 展开或折叠包含部分的“记录”。
6. 单击“筛选器”。
7. 在列表中，选择“字段 = 物料编号”的行。
8. 在“标准”字段中，输入一个值。
    * 示例：P6003  
9. 单击“确定”。
10. 单击“确定”。
11. 单击“计划订单”。
12. 使用“快速筛选器”以查找记录。 例如，使用值“P6000”在“物料编号”字段中进行筛选。
    * 根据配方物料筛选，即含有您已创建销售订单的物料的联产品的配方物料。  
13. 在列表中，标记所选的行。
    * 选择筛选器返回的任何行。  
14. 在列表中，单击所选行中的链接。
15. 展开或折叠“限定”部分。
16. 在列表中，单击所选行中的链接。
    * 计划订单受到联产品销售订单的限定。  
17. 关闭该页面。


