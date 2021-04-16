---
title: 创建成本分配政策并将其分配到成本控制单元
description: 成本分配规则用于分配集体成本中心中已财务盘点的成本。
author: ShylaThompson
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostDistributionRule
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 736b537958f65fb54d0829cfbcc819fd315b530c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810118"
---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a>创建成本分配政策并将其分配到成本控制单元

[!include [banner](../../includes/banner.md)]

成本分配规则用于分配集体成本中心中已财务盘点的成本。 成本会计师确保根据所选分配基数将成本分配给成本中心。 将为成本控制单元分配政策和相应规则。 此任务指南使用示例显示如何创建成本分配政策和相应规则。


## <a name="create-a-policy"></a>创建政策
1. 转到“成本核算”>“政策”>“成本分配政策”。
2. 单击“新建”。
3. 在“政策名称”字段中，键入一个值。
4. 在“描述”字段中，键入一个值。
5. 在“成本对象维度层次结构”字段中，输入或选择一个值。
    * 选择“组织”。  
6. 在“成本元素维度层次结构”字段中，输入或选择一个值。
    * 选择“CDS P/L”。  
7. 在“统计维度”字段中，输入或选择一个值。
    * 选择“统计元素”。  
8. 单击“保存”。

## <a name="create-rules-for-the-policy"></a>为政策创建规则
1. 单击“新建”。
2. 在列表中，标记所选的行。
3. 在“成本对象维度层次结构节点”字段中，输入或选择一个值。
    * 展开层次结构以选择“094”。  
4. 在“成本元素维度层次结构节点”字段中，输入或选择一个值。
    * 选择“其他运营费用”，然后选择“605110 清洁”。  
5. 在“成本行为”字段中，选择一个选项。
    * 选择“固定成本”。  
6. 在“分配基准”字段中，输入或选择一个值。
7. 单击“新建”。
8. 在列表中，标记所选的行。
9. 在“成本对象维度层次结构节点”字段中，输入或选择一个值。
    * 展开层次结构以选择“094”。  
10. 在“成本元素维度层次结构节点”字段中，输入或选择一个值。
    * 选择“其他运营费用”，然后选择“605150 租金”。  
11. 在“成本行为”字段中，选择一个选项。
    * 选择“固定成本”。  
12. 在“分配基准”字段中，输入或选择一个值。
13. 单击“保存”。

## <a name="assign-rules-to-a-cost-control-unit"></a>为成本控制单元分配规则
1. 单击“成本控制单元的政策分配”。
2. 单击“新建”。
3. 在列表中，标记所选的行。
4. 在“核算生效日期”字段中输入日期。
    * 在“有效会计年度”中选择“9 月 1 日”。  
5. 在“成本控制单元”字段中，输入或选择一个值。
6. 单击“保存”。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]