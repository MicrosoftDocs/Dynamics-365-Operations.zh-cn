---
title: "跟踪物料或原材料"
description: "该过程演示如何使用物料跟踪确定使用或正在使用物料或原材料的位置。"
author: pjacobse
manager: AnnBe
ms.date: 06/21/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: pjacobse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d7eb282ddf9597385d6660a3fc0ef73f403ab898
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="trace-an-item-or-raw-material"></a>跟踪物料或原材料

[!include [task guide banner](../../includes/task-guide-banner.md)]

该过程演示如何使用物料跟踪确定使用或正在使用物料或原材料的位置。 通过该过程，您可以确定物料，跟踪其来源，然后继续跟踪其生产和成品销售。 该流程可用于调查受影响客户和订单以及其他信息。 该过程使用演示数据公司 USP2。


## <a name="trace-an-item-backwards-using-a-known-batch-number"></a>使用已知批次编号倒推跟踪物料
1. 转到“库存管理”>“查询和报表”>“跟踪维度”>“物料跟踪”。
2. 在“物料数量”字段中，选择 P9100。
3. 在列表中，单击所选行中的链接。
4. 在“正推”或“倒推”字段中，选择“倒推”。
5. 在“批处理号”字段中，选择 as-12-344-01。
6. 在列表中，单击所选行中的链接。
7. 单击“确定”。

## <a name="identify-an-item-trace-it-forward-and-make-an-analysis"></a>标识物料，正推跟踪，然后进行分析
    * 树形图的顶部节点表示所选物料和批次的现有量。 您需要展开树形图结点以查找应对其执行正向跟踪的物料。   
1. 在树结构中，展开“下面介绍的节点，然后选择最后一个节点”。
    * 展开：“P9100 / 1 / 10 / as-12-344-01 ● 2 keg ● 7.00 gal  \P9100 ● 已领料 ● 销售订单 000072 ● 12/22/2015  ● -1 keg ● -4.00 gal ● 站点=1，仓库=10，批处理号=as-12-344-01  \P9100 ● 生产 B-000050 ● 12/9/2015● 7 keg ● 27.00 gal ● 站点=1，仓库=10，批处理号=as-12-344-01 ● 联产品：P9101”，然后选择该节点。     
2. 在树结构中，展开“下面介绍的节点，然后选择该节点”。
    * 从您刚才选择的节点开始，展开“M9103 ● 生产订单行 B-000050 ● 12/9/2015  ● -160.00 lb ● 尺寸=70，颜色=OK，站点=1，仓库=10，批处理号=App01”，然后选择该节点。  
3. 单击“从节点跟踪”。
4. 单击“正推”。
5. 在“操作窗格”上单击“跟踪”。
    * 具有若干跟踪选项，提供有关受您跟踪的物料影响的客户的信息，以及与已装运和尚未装运的物料相关的销售订单的信息。   
6. 单击“客户”。
7. 关闭该页面。
8. 在“操作窗格”上单击“跟踪”。
9. 单击“装运的销售订单”。
10. 关闭该页面。

