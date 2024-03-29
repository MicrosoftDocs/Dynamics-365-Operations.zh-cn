---
title: 创建成本分摊策略并将其分配到成本控制单元
description: 此过程用于创建和分配成本分配政策，以及为成本控制单元分配相应规则。
author: twheeloc
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostAccountingLedgerPolicyAssignment
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5082f4e80958ddb1e4a79bfe46df4a621f10fc40
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734238"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a>创建成本分摊策略并将其分配到成本控制单元

[!include [banner](../../includes/banner.md)]

此过程用于创建和分配成本分配政策，以及为成本控制单元分配相应规则。 此录制使用 USP2 演示数据公司。


## <a name="create-a-policy"></a>创建政策
1. 转到 **成本核算 > 政策 > 成本分配政策**。
2. 单击 **新建**。
3. 在 **政策名称** 字段中，键入一个值。
4. 在 **成本对象维度层次结构** 字段中，输入或选择一个值。
    * 选择“组织”。  
5. 在 **统计维度** 字段中，输入或选择一个值。
6. 单击 **保存**。

## <a name="create-allocation-rules"></a>创建分配规则
1. 单击 **新建**。
2. 在列表中，标记所选的行。
3. 在 **成本对象维度层次结构节点** 字段中，输入或选择一个值。
4. 在 **成本行为** 字段中选择“总计”。
5. 在 **分配基准** 字段中，输入或选择一个值。
6. 单击 **新建**。
7. 在列表中，标记所选的行。
8. 在 **成本对象维度层次结构节点** 字段中，输入或选择一个值。
9. 在 **成本行为** 字段中选择“总计”。
10. 在 **分配基准** 字段中，输入或选择一个值。
11. 单击 **新建**。
12. 在列表中，标记所选的行。
13. 在 **成本对象维度层次结构节点** 字段中，输入或选择一个值。
14. 在 **成本行为** 字段中选择“总计”。
15. 在 **分配基准** 字段中，输入或选择一个值。
    * 继续操作，直到创建了所有规则。  
16. 单击 **保存**。

## <a name="assign-the-policy-to-a-cost-control-unit"></a>为成本控制单元分配政策
1. 单击 **成本控制单元的政策分配**。
2. 单击 **新建**。
3. 在列表中，标记所选的行。
4. 在 **核算生效日期** 字段中输入日期。
    * 规则具有时效性。 创建了更新版本时，用户或系统可让规则到期。  
5. 在 **成本控制单元** 字段中，输入或选择一个值。
6. 单击 **保存**。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
