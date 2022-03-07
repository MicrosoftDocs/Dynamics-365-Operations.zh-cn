---
title: 创建联产品的物料计划
description: 生产规划员为属于配方联产品的物料规划物料要求。
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: deae0d7e0295aa02f5ad512f67e9e3d2148c2e33
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578288"
---
# <a name="create-a-material-plan-for-co-products"></a>创建联产品的物料计划

[!include [banner](../../includes/banner.md)]

生产规划员为属于配方联产品的物料规划物料要求。 使用 USP2 公司演示数据创建此过程。

## <a name="create-requirement-for-a-co-product"></a>创建联产品的要求

1. 转到 **销售和市场营销 \> 工作区 \> 销售订单处理和查询**。
1. 选择 **新建**。
1. 选择 **销售订单**。
1. 在 **客户帐户** 字段中，键入一个值。
    * 示例：US-001  
1. 选择 **确定**。
1. 在 **项目编号** 字段中，键入一个值。
    * 示例：P6003  
1. 在 **数量** 字段中，输入一个数字。
    * 示例：50000  
1. 选择 **保存**。

## <a name="create-a-material-plan-for-co-products"></a>创建联产品的物料计划

1. 关闭该页面。
1. 关闭该页面。
1. 选择 **主计划**。
1. 在 **计划** 字段中，选择下拉按钮以打开查找。
1. 在列表中，选择所选择行中的链接。
    * 示例：主计划  
1. 选择 **运行**。
1. 展开或折叠 **要包括的记录** 部分。
1. 选择 **筛选器**。
1. 在列表中，选择 **字段** = *物料编号* 的行。
1. 在 **条件** 字段中，输入一个值。
    * 示例：P6003  
1. 选择 **确定**。
1. 选择 **确定**。
1. 选择 **计划订单**。
1. 使用“快速筛选器”以查找记录。 例如，使用值“P6000”在 **物料编号** 字段中进行筛选。
    * 根据配方物料筛选，即含有您已创建销售订单的物料的联产品的配方物料。  
1. 在列表中，标记所选的行。
    * 选择筛选器返回的任何行。  
1. 在列表中，选择所选择行中的链接。
1. 展开 **限定标准** 部分。
1. 在列表中，选择所选择行中的链接。
    * 计划订单受到联产品销售订单的限定。  
1. 关闭该页面。

## <a name="create-a-second-requirement-for-a-co-product"></a>为联产品创建第二个要求

1. 转到 **销售和市场营销 \> 工作区 \> 销售订单处理和查询**。
1. 选择 **新建**。
1. 选择 **销售订单**。
1. 在 **客户帐户** 字段中，键入一个值。
    * 示例：US-001  
1. 选择 **确定**。
1. 在 **项目编号** 字段中，键入一个值。
    * 示例：P6003  
1. 在 **数量** 字段中，输入一个数字。
    * 示例：50000  
1. 选择 **保存**。

## <a name="create-a-second-material-plan-for-co-products"></a>为联产品创建第二个物料计划

1. 在 **计划** 字段中，选择下拉按钮以打开查找。
2. 在列表中，选择所选择行中的链接。
    * 示例：主计划  
3. 选择 **运行**。
4. 展开或折叠 **要包括的记录** 部分。
5. 选择 **筛选器**。
6. 在列表中，选择 **字段** = *物料编号* 的行。
7. 在 *条件* 字段中，输入一个值。
    * 示例：P6003  
8. 选择 **确定**。
9. 选择 **确定**。
10. 选择 **计划订单**。
11. 使用“快速筛选器”以查找记录。 例如，使用值“P6000”在 **物料编号** 字段中进行筛选。
    * 根据配方物料筛选，即含有您已创建销售订单的物料的联产品的配方物料。  
12. 在列表中，标记所选的行。
    * 选择筛选器返回的任何行。  
13. 在列表中，选择所选择行中的链接。
14. 展开或折叠 **限定标准** 部分。
15. 在列表中，选择所选择行中的链接。
    * 计划订单受到联产品销售订单的限定。  
16. 关闭该页面。
17. 选择 **主计划**。
18. 转到 **主计划 \> 设置 \> 主计划参数**。
19. 在 **禁用所有计划流程** 字段中选择 *否*。
20. 关闭该页面。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]