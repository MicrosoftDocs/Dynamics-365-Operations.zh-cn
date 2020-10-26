---
title: 创建联产品的物料计划
description: 生产规划员为属于配方联产品的物料规划物料要求。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 14de9a1085ac1cae88ad93c35385dd43c60ed4d1
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982201"
---
# <a name="create-a-material-plan-for-co-products"></a>创建联产品的物料计划

[!include [banner](../../includes/banner.md)]

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
1. 关闭该页面。
2. 关闭该页面。
3. 单击“主计划”。
4. 在“计划”字段中，单击下拉按钮以打开查找。
5. 在列表中，单击所选行中的链接。
    * 示例：主计划  
6. 单击“运行”。
7. 展开或折叠包含部分的“记录”。
8. 单击“筛选器”。
9. 在列表中，选择“字段 = 物料编号”的行。
10. 在“标准”字段中，输入一个值。
    * 示例：P6003  
11. 单击“确定”。
12. 单击“确定”。
13. 单击“计划订单”。
14. 使用“快速筛选器”以查找记录。 例如，使用值“P6000”在“物料编号”字段中进行筛选。
    * 根据配方物料筛选，即含有您已创建销售订单的物料的联产品的配方物料。  
15. 在列表中，标记所选的行。
    * 选择筛选器返回的任何行。  
16. 在列表中，单击所选行中的链接。
17. 展开或折叠“限定”部分。
18. 在列表中，单击所选行中的链接。
    * 计划订单受到联产品销售订单的限定。  
19. 关闭该页面。

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
1. 在“计划”字段中，单击下拉按钮以打开查找。
2. 在列表中，单击所选行中的链接。
    * 示例：主计划  
3. 单击“运行”。
4. 展开或折叠包含部分的“记录”。
5. 单击“筛选器”。
6. 在列表中，选择“字段 = 物料编号”的行。
7. 在“标准”字段中，输入一个值。
    * 示例：P6003  
8. 单击“确定”。
9. 单击“确定”。
10. 单击“计划订单”。
11. 使用“快速筛选器”以查找记录。 例如，使用值“P6000”在“物料编号”字段中进行筛选。
    * 根据配方物料筛选，即含有您已创建销售订单的物料的联产品的配方物料。  
12. 在列表中，标记所选的行。
    * 选择筛选器返回的任何行。  
13. 在列表中，单击所选行中的链接。
14. 展开或折叠“限定”部分。
15. 在列表中，单击所选行中的链接。
    * 计划订单受到联产品销售订单的限定。  
16. 关闭该页面。
17. 单击“主计划”。
18. 转到“主计划”>“设置”>“主计划参数”。
19. 在“禁用所有计划过程”字段中选择“否”。
20. 关闭该页面。

