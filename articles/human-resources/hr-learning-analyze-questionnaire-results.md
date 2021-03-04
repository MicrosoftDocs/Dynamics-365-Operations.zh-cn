---
title: 分析调查表结果
description: 调查表统计可用于计算平均数、总数和基于人口统计数据的百分比。
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMQuestionnaireStatistics, KMQuestionnaireStatisticsLine, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0b8e4fd5d9fabd35de067ab61c1e64156ce4f0ec
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417526"
---
# <a name="analyzing-questionnaire-results"></a>分析调查表结果



调查表统计可用于计算平均数、总数和基于人口统计数据的百分比。 若要启动此过程，请转到“调查表”>“查看和分析结果”>“调查表统计”。 创建此程序的演示数据公司是 USMF。


## <a name="create-a-questionnaire-statistics-record"></a>创建调查表统计记录
1. 转到“调查表统计”。
2. 单击“新建”。
3. 在列表中，标记所选的行。
4. 在“统计”字段中，键入一个值。
5. 在“描述”字段中，键入一个值。
6. 在“调查表”字段中，单击下拉按钮以打开查找。
7. 在列表中，单击所选行中的链接。
8. 单击“常规”选项卡。
    * 如果您想添加匿名结果或工作人员、联系人和申请人的结果，请选择此项。  
9. 选择或取消选择“工作人员”复选框。
    * 如果您将按资历或年龄查看结果，请指定您希望在结构分组时使用的间隔依据。  
    * 在年龄段中输入 5，则将会根据 5 岁年龄段对结果进行分组。  
10. 在“年龄”字段中，输入数字。
    * 如果您想要对整个调查表、每个结果组、每个问题或每个问题行运行计算，请选择此项。  
    * 选择您希望的结果分组方式。  
    * 例如，如果计算每个问题的平均数，您可能想要在查看问题时按结果分组。  
    * 选择进行计算的数据。  
    * 例如，如果您想要查看工作人员调查表的平均百分比和平均分。  
11. 单击“范围”选项卡。
    * 使用范围限制结果，设置为仅满足范围标准的结果。  
12. 单击“分组依据”选项卡。
    * 进行分组，以确定如何显示结果。  
    * 例如，首先按性别将结果分组，然后按年龄分组。  
13. 在列表中，找到并选择所需记录。
    * 将分组移动到所选的一侧，并以期望的顺序排列。  

## <a name="execute-the-statistics-calculation"></a>执行统计计算。
1. 单击“执行”。
    * 选择您想对结果执行的计算方式。  
    * 例如，计算所选组在调查表中的平均百分比，或统计所选组的分数结果。  
2. 选择或取消选择“删除先前搜索”复选框。
3. 单击“确定”。

## <a name="view-the-results-of-the-questionnaire-statistics-run"></a>查看调查表统计运行的结果。
1. 单击“结果”。
2. 单击“结果”。
3. 关闭该页面。



[!INCLUDE[footer-include](../includes/footer-banner.md)]