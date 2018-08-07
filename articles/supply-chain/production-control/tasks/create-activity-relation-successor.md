--- 
title: "创建活动关系 - 后续活动"
description: "精益生产流的活动流通过活动关系记录。"
author: cvocph
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 75a76252cc3cb6f3e7516309a7d9a6f2d1934ccd
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="create-activity-relation-successor"></a>创建活动关系：后续活动

[!include [task guide banner](../../includes/task-guide-banner.md)]

精益生产流的活动流通过活动关系记录。 此记录显示如何创建活动关系。

先决条件：

- 一个生产流程和草稿模式的版本。 

- 创建了在生产流中彼此衔接的两个活动，但两者不相关。


## <a name="find-the-production-flow-version"></a>找到生产流版本 
1. 转到“生产控制”>“设置”>“精益生产流程”>“生产流程”。
2. 在列表中，找到并选择所需记录。
3. 在列表中，单击所选行中的链接。
4. 在列表中，标记所选的行。
5. 在列表中，选择一个草稿版本。
    * 可在生产流的草稿或有效版本中添加活动关系。  

## <a name="open-the-activity-overview"></a>打开活动概览
1. 单击“活动”。
    * 请注意，窗体显示生产流的所有活动分配到您正在操作的生产流版本中。  

## <a name="add-a-successor"></a>添加后续活动
1. 单击“添加后续活动”。
2. 在“活动”字段中，单击下拉按钮以打开查找。
3. 在列表中，找到并选择所需记录。
4. 在列表中，单击所选行中的链接。
5. 选择“约束”复选框。
6. 在“约束值”字段中，输入一个数字。
    * 约束时间是在前导活动的计划结束时间（到期日期和时间）和后续的计划开始时间之间安排的时间。  
7. 在“单位”字段中，键入一个值。
8. 在“周期时间比率”字段中，输入一个数字。
    * 如果两个活动以相同的单位产品生产时间运行，周期时间比率应为 1。 如果前导活动以后续活动的两倍速度运行，比率应为 2。   周期时间比率用于计算生产流活动的单个周期时间。  
9. 单击“确定”。
10. 关闭该页面。
11. 单击“网格面板”选项卡。
12. 关闭该页面。
13. 刷新该页面。


