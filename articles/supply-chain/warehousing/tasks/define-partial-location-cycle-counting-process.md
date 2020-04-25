---
title: 定义部分库位周期盘点流程
description: 使用周期盘点计划创建盘点工作时，可以通过请求仅盘点特定产品和产品变型，而不是盘点库位中的所有现成库存，指导实际盘点操作。
author: ShylaThompson
manager: tfehr
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3d80171ec524e3401d7971cb743d73abdda87ff
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3217026"
---
# <a name="define-partial-location-cycle-counting-process"></a>定义部分库位周期盘点流程 

[!include [banner](../../includes/banner.md)]

使用周期盘点计划创建盘点工作时，可以通过请求仅盘点特定产品和产品变型，而不是盘点库位中的所有现成库存，指导实际盘点操作。 通过筛选特定产品，仓库经理可以降低审核开销，帮助避免合并错误和节省时间。 通常，仓库管理员执行设置任务。 您可以在 USMF 演示数据公司或您自己的数据中了解该过程。


## <a name="create-a-cycle-counting-work-template"></a>创建周期盘点工作模板
1. 转到“仓库管理”>“设置”>“工作”>“工作模板”。
2. 在“工作订单类型”字段中，选择“周期盘点”。
3. 单击“新建”。
4. 在“序列号”字段中，输入一个数字。
    * 排序顺序是从最小数字到最大数字。 值必须大于 0（零）。  
5. 在列表中，标记所选的行。
6. 在“工作模板”字段中，键入一个值。
7. 在“工作模板描述”字段中，键入一个值。
8. 在“工作池 ID”字段中，输入或选择一个值。
9. 在“工作优先级”字段中，输入一个数字。
10. 单击“保存”。
11. 单击“新建”。
12. 在列表中，标记所选的行。
13. 在“工作类型”字段中，选择“盘点”。
14. 在“工作类 ID”字段中，输入或选择一个值。
15. 单击“保存”。
16. 单击“工作行中断”。
17. 单击“新建”。
18. 在“序列号”字段中，输入一个数字。
    * 排序顺序是从最小数字到最大数字。 值必须大于 0（零）。  
19. 单击“保存”。
20. 关闭该页面。
21. 关闭该页面。

## <a name="create-a-cycle-counting-plan"></a>创建周期盘点计划
1. 转到“仓库管理”>“设置”>“周期盘点”>“周期盘点计划”。
2. 单击“新建”。
3. 在“周期盘点计划 ID ”字段中，键入一个值。
4. 在“描述”字段中，键入一个值。
5. 在“周期盘点最大数”字段中，输入一个数字。
6. 在“工作模板”字段中，输入或选择一个值。
7. 单击“新建”。
8. 在“序列号”字段中，输入一个数字。
    * 排序顺序是从最小数字到最大数字。 值必须大于 0（零）。  
9. 在“描述”字段中，键入一个值。
10. 单击“保存”。
11. 单击“定义产品查询”。
12. 在列表中，标记所选的行。
13. 在“标准”字段中，输入或选择一个值。
14. 单击“确定”。
15. 关闭该页面。

