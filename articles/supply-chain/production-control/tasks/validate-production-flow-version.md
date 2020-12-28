---
title: 验证生产流和版本
description: 该过程显示如何创建新的生产流以及 lean manufacturing 的第一个版本。
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c30947d01cfb85ea3dbf1aa3e4ea8e092efd18cb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423097"
---
# <a name="validate-a-production-flow-and-version"></a>验证生产流和版本

[!include [banner](../../includes/banner.md)]

该过程显示如何创建新的生产流以及 lean manufacturing 的第一个版本。 先决条件：必须定义 Lean manufacturing 的生产参数以及类别时间的度量单位。 您需要定义“价值流”和“生产组”。 请参阅 Lean manufacturing 白皮书，以了解生产流和活动的概念。 该过程在演示数据中使用的是 USMF 法人。 但是，如果已配置 Lean manufacturing 的法人，则可使用其他法人。


## <a name="create-a-production-flow"></a>创建生产流
1. 转到“生产控制”>“设置”>“精益生产流程”>“生产流程”。
2. 单击“新建”。
3. 在“名称”字段中，键入一个值。
4. 在“描述”字段中，键入一个值。
5. 在“名称”字段中，单击下拉按钮以打开查找。
6. 在列表中，单击所选行中的链接。
    * 价值流是跨越价值流的所有活动和流程的运营单位。   在此阶段，运营单位限制为法人实体，但不具有进一步功能。  
7. 在“生产组”字段中，单击下拉按钮以打开查找。
8. 在列表中，单击所选行中的链接。
    * 生产组允许为生产流程定义材料、人工和 WIP 帐户。 要将核算生产环境与生产流相联系，必须选择生产组。  
9. 单击“保存”。

## <a name="create-a-production-flow-version"></a>创建生产流版本
1. 单击“添加”。
2. 在“到期日期”字段中，输入日期和时间。
    * 您可以在指定时间更新该版本，甚至是有效版本的“到期日期”。 使用该版本的到期日期，以作出版本淘汰计划。  
3. 单击“确定”。
4. 在列表中，标记所选的行。
5. 在“单位”字段中，键入一个值。
6. 选择“单位产品生产时间单位”。
7. 在“平均单位产品生产时间”字段中，输入一个数字。
    * 对于生产流版本的间隔控制，定义所针对的单位产品生产时间。   单位产品为每个时间周期内生产的产品数量。  在给定示例中，单位产品生产时间为每 10 件 0.2 小时。 工作时间为 8 小时，所对应的日产能为 400 件。  
8. 在“每周期数量”字段中，输入一个数字。
9. 展开或折叠“版本详细信息”部分。
10. 在“最小单位产品生产时间”字段中，输入一个数字。
    * 最小单位产品生产时间必须为小于或等于平均单位产品生产时间。  
11. 在“最大单位产品生产时间”字段中，输入一个数字。
    * 最大单位产品生产时间必须为大于或等于“平均单位产品生产时间”。  
12. 在“期间”中输入实际周期时间的天数
    * 实际周期为从实际分钟数向后计算实际周期时间的合并工作天数。 可以随时更改该值，且该值只能用来计算实际周期时间。  
13. 单击“保存”。

