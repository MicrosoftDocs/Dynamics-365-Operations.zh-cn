--- 
title: "创建生产流版本"
description: "该过程主要讲述创建新的生产流版本。"
author: cvocph
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
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 58b3c9cd265b97a814541315e4ba8378010eb2b2
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-production-flow-version"></a>创建生产流版本

[!include[task guide banner](../../includes/task-guide-banner.md)]

该过程主要讲述创建新的生产流版本。 对于该过程，必须定义的 lean manufacturing 生产参数和上课时间的度量单位。 您还需要定义价值流和生产组。 若要了解更多 lean manufacturing 中生产流程和活动，请参阅 Microsoft Dynamics AX 的 Lean manufacturing 白皮书。 创建此程序的演示数据公司是 USMF。


## <a name="create-a-production-flow"></a>创建生产流
1. 转到“生产控制”>“设置”>“精益生产流程”>“生产流程”。
2. 单击“新建”。
3. 在“名称”字段中，键入一个值。
4. 在“描述”字段中，键入一个值。
5. 在“名称”字段中，单击下拉按钮以打开查找。
6. 在列表中，单击所选行中的链接。
    * 选择值类型价值流图的运营单位。 价值流是跨越价值流的所有活动和流程的运营单位。 在此阶段，运营单位限制为法人实体，但不具有进一步功能。  
7. 在“生产组”字段中，单击下拉按钮以打开查找。
8. 在列表中，单击所选行中的链接。
    * 为生产流选择生产组。 生产组允许为生产流程定义材料、人工和 WIP 帐户。 要将核算生产环境与生产流相联系，必须选择生产组。  
9. 单击“保存”。

## <a name="create-a-production-flow-version"></a>创建生产流版本
1. 单击“添加”。
2. 在“到期日期”字段中，输入日期和时间。
    * 如果需要，请定义版本的“到期日期”。 您可以在任意指定时间更新它，即便为活动版本。 您可以使用它来计划逐步淘汰一个版本。  
3. 单击“确定”。
4. 在列表中，标记所选的行。
5. 在“单位”字段中，键入一个值。
6. 决定“改变单位产品生产时间”。
7. 在“平均单位产品生产时间”字段中，输入一个数字。
    * 定义版本的“平均单位产品生产时间”。 对于生产流版本的间隔控制，定义所针对的单位产品生产时间。 单位产品为每个时间周期内生产的的产品数量。 在本例中，单位产品生产时间为每 10 件 0.2 小时。 工作时间为 8 小时，所对应的日产能为 400 件。  
8. 在“每周期数量”字段中，输入一个数字。
    * 定义“平均单位产品生产时间”周期的数量。  
9. 切换“版本详细信息”部分的展开项。
10. 在“最小单位产品生产时间”字段中，输入一个数字。
    * 定义最小单位产品生产时间。 最小单位产品生产时间必须为小于或等于平均单位产品生产时间。  
11. 在“最大单位产品生产时间”字段中，输入一个数字。
    * 最大单位产品生产时间必须为大于或等于“平均单位产品生产时间”。  
12. 在“实际周期期间”字段中，输入一个数字。
    * 在“周期”中，输入实际的周期天数。 实际周期为从实际分钟数向后计算实际周期时间的合并工作天数。 可以随时更改该值，且该值只能用来计算实际周期时间。  
13. 单击“保存”。


