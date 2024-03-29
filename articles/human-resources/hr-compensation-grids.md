---
title: 设置薪酬网格
description: 薪酬网格用于定义及维持固定薪酬计划的工资结构。
author: twheeloc
ms.date: 01/03/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRCCompGrid, HRCCompGridView, HcmCompensationWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9119c15cf80b9ebb9bed83ac438f24249aa4aa2f
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691664"
---
# <a name="set-up-compensation-grids"></a>设置薪酬网格


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

薪酬网格用于定义及维持固定薪酬计划的工资结构。 新建薪酬计划时薪酬网格可以在多个计划中共享或复制。  在创建薪酬网格之前，必须设置“级别”和“参考点”。 此示例将使用“级别”和“参考点”演示数据创建新的薪酬网格等级类型。 创建此程序的演示数据公司是 USMF。


## <a name="set-up-information-about-the-compensation-grid"></a>设置有关薪酬网格的信息
1. 转到 **人力资源** > **薪酬** > **固定薪酬** > **薪酬网格**。
2. 单击 **新建**。
3. 在 **网格** 字段中，键入一个值。
4. 在 **描述** 字段中，键入一个值。
5. 在 **类型** 字段中，选择一个选项。
6. 在 **参考** 设置字段中，输入或选择一个值。
7. 在 **货币** 字段中，输入或选择一个值。
8. 在 **生效日期** 字段中，输入日期。

## <a name="add-levels-to-the-compensation-structure"></a>在薪酬结构中添加级别
1. 单击 **薪酬结构**。
2. 在列表中，标记所选的行。
3. 在 **级别** 字段中，输入或选择一个值。
4. 单击 **新建**。
5. 在列表中，标记所选的行。
6. 在 **级别** 字段中，输入或选择一个值。
7. 单击 **新建**。
8. 在列表中，标记所选的行。
9. 在 **级别** 字段中，输入或选择一个值。
10. 单击 **新建**。
11. 在列表中，标记所选的行。
12. 在 **级别** 字段中，输入或选择一个值。
13. 单击 **新建**。
14. 在列表中，标记所选的行。
15. 在 **级别** 字段中，输入或选择一个值。

## <a name="fill-in-the-compensation-structure-with-values"></a>在薪酬结构中填入值
1. 在列表中，标记所选的行。
    * 此时，在该表中，可以在每个字段手动输入薪酬值，或者使用“批量更改功能”轻松填充多个字段并执行基本的计算功能。  
2. 单击 **批量更改**。
    * 此网格表中，我们首先把第一级别的中间点值应用到表中的所有字段中。 这将是薪酬矩阵的基础。  
3. 在 **调整类型** 字段中，选择一个选项。
4. 在 **调整金额** 字段中，输入一个数值。
5. 在列表中，标记或取消标记所有行。
6. 单击 **应用于网格**。
    * 现在我们将使用批量更改功能按照一定的百分比或数目在接下来的每个级别中逐渐增加金额。 在此示例中，每个等级在中间点值的 12.5% 范围内进行调整。  
7. 在 **调整类型** 字段中，选择一个选项。
8. 在 **调整金额** 字段中，输入一个数值。
9. 在列表中，找到并选择所需记录。
10. 单击 **应用于网格**。
    * 现在使用批量更改功能调整每个级别的“最小”与“最大”参考点值。 此示例将使用 50% 的点差，那么其最小参考点值将调整 -20%，而最大参考点值调整 +20%。  
11. 在 **调整金额** 字段中，输入一个数值。
12. 在 **参考点** 字段中，输入或选择一个值。
13. 在列表中，标记或取消标记所有行。
14. 单击 **应用于网格**。
15. 在 **调整金额** 字段中，输入一个数值。
16. 在 **参考点** 字段中，输入或选择一个值。
17. 在列表中，标记或取消标记所有行。
18. 单击 **应用于网格**。



[!INCLUDE[footer-include](../includes/footer-banner.md)]
