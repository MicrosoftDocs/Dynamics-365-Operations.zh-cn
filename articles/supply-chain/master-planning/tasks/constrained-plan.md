---
title: 生成受约束计划
description: 此主题介绍如何创建涉及物料和产能限制的计划。
author: ShylaThompson
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c35d5a7465cc6cfe0bc12cb00796eff2aeed1ece
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808008"
---
# <a name="generate-a-constrained-plan"></a>生成受约束计划

[!include [banner](../../includes/banner.md)]

此主题介绍如何创建涉及物料和产能限制的计划。 计划确保，在制造物料可用且资源未超额认购之前，不进行生产。 

创建此程序的演示数据公司是 USMF。 此程序是专为生产规划员设计的。


## <a name="set-up-a-constrained-plan"></a>设置约束计划
1. 在主页中，选择 **主计划** 工作区。
2. 选择工作区最右侧链接列表中的 **主计划**。
3. 在列表中，找到并选择所需记录。 示例：**StaticPlan**  
4. 在 **有限产能** 字段中，选择 **是**。
5. 在 **有限产能时限** 字段中，输入 `30`。
6. 展开 **按天计算的时限** 部分。
7. 在 **产能** 字段中，选择 **是**。
8. 在 **产能计划时限（以天为单位）** 字段中，输入一个数值。 示例: `60`  
9. 在 **计划延迟** 字段中选择 **是**。
10. 在 **计划延迟时限（以天为单位）** 字段中，输入一个数值。 示例: `60` 
11. 展开 **计算的延迟** 部分。
12. 在所有 **添加计算的延迟到需求日期** 字段中选择 **是**。
13. 关闭该页面。

## <a name="create-a-constrained-plan"></a>创建约束计划
1. 选择 **运行**。
2. 在 **主计划** 字段中，输入或选择要为其设置约束的计划。  
3. 选择 **确定**。
4. 选择 **计划订单**。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]