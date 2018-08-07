--- 
title: "生成受约束计划"
description: "此过程显示如何创建涉及物料和产能限制的计划。"
author: ShylaThompson
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 59c6a4a2b239b3fd6b6ddc8f06bfd007f0191f0a
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="generate-a-constrained-plan"></a>生成受约束计划

[!include [task guide banner](../../includes/task-guide-banner.md)]

此过程显示如何创建涉及物料和产能限制的计划。 计划确保，在制造物料可用且资源未超额认购之前，不进行生产。 

创建此程序的演示数据公司是 USMF。 此程序是专为生产规划员设计的。


## <a name="set-up-a-constrained-plan"></a>设置约束计划
1. 单击“主计划”。
2. 单击“主计划”。
3. 在列表中，找到并选择所需记录。
    * 示例：StaticPlan  
4. 在“有限产能”字段中，选择“是”。
5. 在“有限产能时限”字段中，输入“30“。
6. 可以在天数部分，扩展时限。
7. 在“产能”字段中，选择“是”。
8. 在“产能计划时限（以天为单位）”字段中，输入一个数值。
    * 示例：60  
9. 在“计划延迟”字段中选择“是”。
10. 在“计划延迟时限（以天为单位）”字段中，输入一个数值。
    * 示例：60  
11. 展开“计算的延迟”部分。
12. 在“添加计算的延迟到需求日期”字段选择“是”。
13. 在“添加计算的延迟到需求日期”字段选择“是”。
14. 在“添加计算的延迟到需求日期”字段选择“是”。
15. 关闭该页面。

## <a name="create-a-constrained-plan"></a>创建约束计划
1. 单击“运行”。
2. 在“主计划”字段中，输入或选择一个值。
    * 选择您设置约束的计划。  
3. 单击“确定”。
    * 这可能需要花费一段时间。  
4. 单击“计划订单”。


