--- 
title: "定义生产流模型"
description: "生产流模型描述如何计算并维持精益制造工作单元的产能。"
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LeanProductionFlowModel
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7850a121ca06f25f6c532e49e18c0b6811bd7455
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="define-production-flow-models"></a>定义生产流模型

[!include [task guide banner](../../includes/task-guide-banner.md)]

生产流模型描述如何计算并维持精益制造工作单元的产能。 因此，定义生产流模型是定义工作单元的先决条件。 创建此程序的演示数据公司是 USMF。


## <a name="define-a-production-flow-model"></a>定义生产流模型。 
1. 转到“生产管理”>“设置”>“精益生产流”>“生产流模型”。
2. 单击“新建”。
3. 在“生产流模型”字段中，输入生产流模型的 ID。
4. 在“模型类型”字段中，选择一个选项。
    * 两个模型类型：吞吐量类型和工时类型。 对于使用吞吐量类型生产流模型的工作单元，其产能将通过产品数量进行描述和计算。 对于使用工时类型生产流模型的工作单元，其产能将通过工时数进行描述和计算。 请注意，现有生产流模型的属性无法更改。 工作单元具有产能预留后，其生产流模型将无法更改。  
5. 在“EPE 周期”字段中输入天数。
    * 间隔描述生产流或工作单元的每个部分将至少生产一次的周期。 EPE 循环时间越短，生产流就越灵活。 如果 EPE 周期 = 0，则所有的需求量可在同一天生产出。 EPE 周期用于安排精益流程作业计划。 如果采用 EPE 周期 = 5 计划工作单元中一项作业，则该计划流程将在到期日期 - EPE 周期（到期日期前 5 天）查询该工作单元的产能以确保该产品是否能在该周期内生产。 产品的库存提前期通常等于或大于关联生产流的 EPE 周期。  
6. 在“计划周期类型”字段中，选择一个选项。
    * 工作单元具有产能预留后，其生产流模型将无法更改。 对于此特定工作单元，只能选择与其具有相同周期类型的生产流模型。  
7. 在“计划时限”字段中，输入一个数字。
    * 计划产能时限描述可为相关工作单元提供的产能预留天数。 在“计划时限”中，输入天数。   将不通过自动计划规划不在此期间的看板处理作业。 计划时限通常是生产流或工作单元内所生产产品的平均库存提前期的两倍。 EPE 周期不应超过计划时隙的一半。     
8. 在“产能短缺反应”字段中，选择一个选项。
    * 选项包括：延期 - 将该计划事件的饱和需求量延期至下一个吞吐量的可用生产日。 取消 - 终止该计划事件的自动计划作业，并取消其关联的作业计划。   添加到所要求的日期 - 将其要求的作业安排到所要求的期间内。 这超过当天该工作单元的负荷并需要计划员进行检查和手动交互。   分配到可用期间 - 从第一个可用生产日开始为该计划事件的所有不同作业分配可用生产日。 此最小分配数量就是该看板作业的数量。 每天分配给最小计划数量（看板作业数量）充足可用的吞吐量。  


