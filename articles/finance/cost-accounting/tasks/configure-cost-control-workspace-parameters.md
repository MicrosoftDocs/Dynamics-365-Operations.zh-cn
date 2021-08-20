---
title: 配置成本控制工作区参数
description: 此过程用于配置“成本控制”工作区，以便组织中各级经理可洞察自己的成本对象，如成本中心和产品组。
author: ShylaThompson
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostControlWorkspaceConfigurationPerUser
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8ecc775019445bbe97dd5a0e9198b9c605b1c65322006d912a95a5bb1fbdf879
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766926"
---
# <a name="configure-cost-control-workspace-parameters"></a>配置成本控制工作区参数

[!include [banner](../../includes/banner.md)]

此过程用于配置“成本控制”工作区，以便组织中各级经理可洞察自己的成本对象，如成本中心和产品组。 USP2 演示公司用于创建此录制。

1. 转至“成本核算”>“设置”>“成本控制工作区配置”。
2. 单击“新建”。
3. 在“名称”字段中，键入一个值。
4. 在“描述”字段中，键入一个值。
5. 在“已发布”字段中选择“是”。
    * 如果将此选项设置为“是”，为其分配了以下角色之一的用户可查看“成本控制”工作区中的报表：成本核算经理、成本会计师、成本核算师和成本对象总监。 如果将此选项设置为“否”，只有为其分配了以下角色之一的用户可查看“成本控制”工作区中的报表：成本核算经理、成本会计师或成本核算师。  
6. 展开“数据筛选”部分。
7. 在“成本控制单元”字段中，输入或选择一个值。
8. 在“预算原始版本”字段中，输入或选择一个值。
9. 在“成本元素维度层次结构”字段中，输入或选择一个值。
10. 在“成本对象维度层次结构”字段中，输入或选择一个值。
11. 展开“分配计算记录”部分。
12. 单击“新建”。
13. 在列表中，标记所选的行。
14. 在“会计日历期间”字段中，输入或选择一个值。
15. 在“实际版本”字段中，输入或选择一个值。
16. 展开“每列的会计期间”部分。
17. 在“当前期间”字段中选择“是”。
18. 展开“为成本显示的列”部分。
19. 在“固定成本”字段中选择“是”。
20. 在“可变成本”字段中选择“是”。
21. 在“总成本”字段中选择“是”。
22. 单击“保存”。
23. 关闭该页面。
24. 转至“成本核算”>“工作区”>“成本控制”。
25. 选择报表以查看所选会计期间的固定成本、可变成本、总成本和未分类的成本。
26. 在“会计日历期间”字段中，输入或选择一个值。
27. 在“成本对象维度层次结构节点”字段中，输入或选择一个值。
    * 选择“成本对象维度层次结构”之后，展开“成本元素维度层次结构”以查看所需成本值。 例如，可以将层次结构展开到“制造开销”以查看值。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]