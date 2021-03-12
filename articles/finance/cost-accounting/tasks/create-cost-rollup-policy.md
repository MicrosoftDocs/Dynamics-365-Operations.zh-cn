---
title: 创建成本累积政策
description: 此过程显示如何创建成本累积政策并为其创建规则。
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0a648984a8b4aaa314707e72a615f516116a193
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990734"
---
# <a name="create-a-cost-rollup-policy"></a>创建成本累积政策

[!include [banner](../../includes/banner.md)]

此过程显示如何创建成本累积政策并为其创建规则。 使用 USP2 演示数据创建此过程。


## <a name="create-a-policy"></a>创建政策
1. 转到“成本核算”>“政策”>“成本累积政策”。
2. 单击“新建”。
3. 在“政策名称”字段中，键入一个值。
4. 在“描述”字段中，键入一个值。
5. 在“成本对象维度层次结构”字段中，输入或选择一个值。
    * 选择“成本累积 CC”。  
6. 在“成本元素维度层次结构”字段中，输入或选择一个值。
    * 选择“成本累积 CC”。  
7. 单击“保存”。

## <a name="create-rules-for-the-cost-rollup-policy"></a>为成本累积政策创建规则
1. 单击“新建”。
2. 在列表中，标记所选的行。
3. 在“成本对象维度层次结构节点”字段中，输入或选择一个值。
    * 选择“007”。  
4. 在“成本元素维度层次结构节点”字段中，输入或选择一个值。
    * 选择“成本累积 CE”。  
5. 在“辅助成本元素维度”字段中，输入或选择一个值。
    * 在此示例中，将辅助成本元素 CC-007 映射到成本中心。  
6. 单击“新建”。
7. 在列表中，标记所选的行。
8. 在“成本对象维度层次结构节点”字段中，输入或选择一个值。
    * 选择“008”。  
9. 在“成本元素维度层次结构节点”字段中，输入或选择一个值。
    * 选择“成本累积 CE”。  
10. 在“辅助成本元素维度”字段中，输入或选择一个值。
    * 在此示例中，将辅助成本元素 CC-008 映射到成本中心。  
11. 单击“新建”。
12. 在列表中，标记所选的行。
13. 在“成本对象维度层次结构节点”字段中，输入或选择一个值。
    * 选择“009”。  
14. 在“成本元素维度层次结构节点”字段中，输入或选择一个值。
    * 选择“成本累积 CE”。  
15. 在“辅助成本元素维度”字段中，输入或选择一个值。
    * 在此示例中，将辅助成本元素 CC-009 映射到成本中心。  
    * 继续操作，直到所有成本中心均已映射到其相应辅助成本元素。  
16. 单击“保存”。

