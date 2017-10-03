--- 
title: "创建工作时间模板"
description: "工作时间模板定义一周内的工作时间，可用于生成一段时期的工作时间。"
author: sorenva
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: ff1978f127a014e75619a4bbbb9b6ff3a3ad7c7a
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---
# <a name="create-working-time-templates"></a>创建工作时间模板

[!include[task guide banner](../../includes/task-guide-banner.md)]

工作时间模板定义一周内的工作时间，可用于生成一段时期的工作时间。 该过程说明如何使用对工作时间间隔进行分类的工作时间计划属性定义工作时间模板。 您可以使用演示数据公司 USMF 或您自己的数据浏览此程序。

1. 转到“所有工作区”>“资源周期管理”。
2. 单击“工作时间模板”。

## <a name="create-working-time-template"></a>创建工作时间模板
1. 单击“新建”。
2. 在“工作时间模板”字段中，键入一个值。
3. 在“名称”字段中，键入一个值。
4. 展开“星期一”部分。
5. 单击“添加”。
6. 在“开始”字段中，输入一个时间。
    * 指定上午开始工作的时间。  
7. 在“结束”字段中，输入一个时间。
    * 指定工作人员的午餐时间。  
8. 单击“添加”。
9. 在“开始”字段中，输入一个时间。
    * 指定午餐后重新开始工作的时间。  
10. 在“结束”字段中，输入一个时间。
    * 指定工作日结束的时间。  

## <a name="replicate-working-times-to-all-week-days"></a>复制工作时间到所有工作日
1. 单击“复制此日”。
    * 复制星期一的工作时间定义到星期二。  
2. 单击“确定”。
3. 单击“复制此日”。
    * 复制星期一的工作时间定义到星期三。  
4. 在“结束工作日”字段中，选择一个选项。
5. 单击“确定”。
6. 单击“复制此日”。
    * 复制星期一的工作时间定义到星期四。  
7. 在“结束工作日”字段中，选择一个选项。
8. 单击“确定”。
9. 单击“复制此日”。
    * 复制星期一的工作时间定义到星期五。  
10. 在“结束工作日”字段中，选择一个选项。
11. 单击“确定”。

## <a name="define-time-slots-for-special-operations"></a>定义特殊操作的时隙
1. 展开“星期五”部分。
2. 在列表中，找到并选择所需记录。
3. 在“属性”字段中，输入或选择一个值。
4. 在列表中，找到并选择所需记录。
5. 在“属性”字段中，输入或选择一个值。

## <a name="mark-weekend-days-as-closed-for-pickup"></a>标记周末为装货关闭的时间
1. 展开“星期六”部分。
2. 在“停止装货”字段中选择“是”。
3. 展开“星期日”部分。
4. 在“停止装货”字段中选择“是”。


