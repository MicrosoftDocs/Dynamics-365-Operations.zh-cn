--- 
title: "定义精益计划组"
description: "精益计划组被定义为组，可区分看板计划中的产品。"
author: cvocph
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
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: a5bc20c0a9e2396365caebeb3751d2090e4575a4
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="define-lean-schedule-groups"></a>定义精益计划组

[!include[task guide banner](../../includes/task-guide-banner.md)]

精益计划组被定义为组，可区分看板计划中的产品。 每个公司或特定工作单元均可以通过通用关联实现分组。 为了在看板计划列表页具有目视识别特征，每个组都被分配了一个颜色代码。 创建此程序的演示数据公司是 USMF。


## <a name="define-lean-scheduling-group"></a>定义精益计划组
1. 转到“产品信息管理”>“精益制造”>“精益计划组”。
2. 单击“新建”。
3. 在“计划组”字段中，键入一个值。
    * 计划组可以定义为全局组或工作单元的特定组。 在这个简单的例子中，我们定义了一个全局组且工作单元为空。 该组的设置适用于所有无特定计划组的工作单元。  
4. 在颜色选项中选择一种颜色。
    * 颜色用于凸显看板计划清单页或看板流程板上的作业。  
5. 在列表中，标记所选的行。
6. 在列表中，单击所选行中的链接。

## <a name="associate-product"></a>关联产品
1. 关联特定产品
    * 可以采用两种方法将产品与精益计划组相关联：特定产品（物料关系类型 = 物料)或者物料分配参数（物料关系类型 = 组）。    
2. 在“物料关系类型”字段中，选择“物料”。
3. 在“项目编号”字段中，输入一个值。
4. 在“吞吐率”字段中，输入一个数字。
    * 默认吞吐率为 1，这意味着相关产品的资源消耗等于生产流的流程活动中指定的产能。 吞吐率 > 1 的定义是资源消耗高于产能，吞吐率 < 1 的定义是资源消耗低于产能。 该比率用于成本计算以及看板作业消耗量的计算。  

## <a name="associate-item-allocation-key"></a>关联物料分配参数
1. 关联物料分配参数
    * 使用“物料关系类型组”为物料分配参数添加关联。    请注意，该流程需要在您的数据中定义的预测物料分配参数。  
2. 在“物料关系类型”字段中，选择“组”。
3. 在“物料分配参数”字段中，单击下拉按钮以打开查找。
4. 在列表中，单击所选行中的链接。


