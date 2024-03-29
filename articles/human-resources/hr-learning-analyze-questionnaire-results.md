---
title: 分析调查表结果
description: 调查表统计可用于计算平均数、总数和基于人口统计数据的百分比。
author: twheeloc
ms.date: 08/26/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMQuestionnaireStatistics, KMQuestionnaireStatisticsLine, HcmLearningWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1da18dd32363308438b7f9da5b2e04e119e840cb
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692910"
---
# <a name="analyzing-questionnaire-results"></a>分析调查表结果


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



调查表统计可用于计算平均数、总数和基于人口统计数据的百分比。 若要启动此过程，请转到 **调查表** > **查看和分析结果** > **调查表统计**。 创建此程序的演示数据公司是 USMF。


## <a name="create-a-questionnaire-statistics-record"></a>创建调查表统计记录
1. 转到 **调查表统计**。
2. 单击 **新建**。
3. 在列表中，标记所选的行。
4. 在 **统计信息** 字段中，键入一个值。
5. 在 **描述** 字段中，键入一个值。
6. 在 **调查表** 字段中，单击下拉按钮以打开查找。
7. 在列表中，单击所选行中的链接。
8. 单击 **常规** 选项卡。
    * 如果您想添加匿名结果或工作人员、联系人和申请人的结果，请选择此项。  
9. 选中或取消选中 **工作人员** 复选框。
    * 如果您将按资历或年龄查看结果，请指定您希望在结构分组时使用的间隔依据。  
    * 在年龄段中输入 5，则将会根据 5 岁年龄段对结果进行分组。  
10. 在 **年龄** 字段中，输入数字。
    * 如果您想要对整个调查表、每个结果组、每个问题或每个问题行运行计算，请选择此项。  
    * 选择您希望的结果分组方式。  
    * 例如，如果计算每个问题的平均数，您可能想要在查看问题时按结果分组。  
    * 选择进行计算的数据。  
    * 例如，如果您想要查看工作人员调查表的平均百分比和平均分。  
11. 单击 **范围** 选项卡。
    * 使用范围限制结果，设置为仅满足范围标准的结果。  
12. 单击 **分组依据** 选项卡。
    * 进行分组，以确定如何显示结果。  
    * 例如，首先按性别将结果分组，然后按年龄分组。  
13. 在列表中，找到并选择所需记录。
    * 将分组移动到 **所选** 一侧，并以期望的顺序排列。  

## <a name="execute-the-statistics-calculation"></a>执行统计计算。
1. 单击 **执行**。
    * 选择您想对结果执行的计算方式。  
    * 例如，计算所选组在调查表中的平均百分比，或统计所选组的分数结果。  
2. 选中或取消选中 **删除先前搜索** 复选框。
3. 单击 **确定**。

## <a name="view-the-results-of-the-questionnaire-statistics-run"></a>查看调查表统计运行的结果。
1. 单击 **结果**。
2. 单击 **结果**。
3. 关闭该页面。



[!INCLUDE[footer-include](../includes/footer-banner.md)]
