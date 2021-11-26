---
title: 使用计划分发调查表
description: 调查表编制计划允许您将调查表分发给多个回应者。
author: twheeloc
ms.date: 10/28/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMKnowledgeCollectorPlanningTable, KMKnowledgeCollectorPlanningMulti, SysQueryForm, HcmPersonLookup, KMKnowledgeCollectorPlanning, HcmLearningWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2336cafe7e2c914c2592c91c888b1e0ae1bc608
ms.sourcegitcommit: e91a1797192fd9bc4048b445bb5c1ad5d333d87d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/01/2021
ms.locfileid: "7728668"
---
# <a name="distribute-questionnaires-using-scheduling"></a>使用计划分发调查表

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

调查表编制计划允许您将调查表分发给多个回应者。 创建此程序的演示数据公司是 USMF。

## <a name="create-a-questionnaire-schedule"></a>创建调查表计划

1. 转到 **调查表** > **分配** > **调查表计划**。

2. 单击 **新建**。

3. 在 **计划** 字段中，键入一个值。

4. 在 **描述** 字段中，键入一个值。
    * 如果响应应记录，而无需关联的名称，则将计划设置为 **匿名**。  
    * 必须首先在“HR 参数”中设置允许匿名结果。  

5. 在 **类型** 字段中，选择计划类型。  在此示例中，我们将使用 **满意度** 类型。

6. 在列表中，找到并选择所需记录。

7. 在列表中，单击所选行中的链接。

8. 在 **日期** 字段中，输入一个日期。

9. 展开 **员工自助服务的电子邮件** 部分。

10. 在 **主题** 字段中，键入一个值。

    * 示例：可用的调查表  

11. 在 **文本** 字段中，键入电子邮件的正文。 请注意，此变量可用于替换系统中的值。

    * 示例：尊敬的 %P%，请登录“员工自助服务”填写《员工健康》调查表。  Contoso  

12. 单击 **保存**。

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a>使用设置详细信息选择要回答的调查表，以及用于选择回应者的任何查询。

1. 单击 **设置详细信息**。

2. 在列表中，选择用于搜索系统以查找调查表回应者的查询。

    * 示例：工作人员  

3. 单击 **查看或修改查询** 来选择特定人员或调整查询来查找满足特定条件的人员。

    * 请注意，所有回应者还必须是系统中的用户。  

4. 在列表中，标记“人员”的行。

5. 在 **标准** 字段中，输入或选择一个值。

    * 选择“Julia Funderburk”  

6. 在列表中，选择“Julia Funderburk”

7. 单击 **确定**。

8. 单击 **调查表** 选项卡。

9. 在树中，展开类型为 **满意度调查** 的调查表的节点。

10. 在树中，选中“员工健康评估”。

11. 单击 **确定**。

12. 单击 **计划应答期**。

    * 请注意，**计划应答期** 已为每个所选/查询用户创建。  

13. 关闭该页面。

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a>开始调查表计划以使调查表可供回应者完成。

1. 单击 **功能**。

2. 单击 **开始**。

3. 单击 **确定**。

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a>发送电子邮件通知可用调查表的回应者。

1. 单击 **功能**。

2. 单击 **发送电子邮件**。

3. 单击 **取消**。

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a>使用“计划应答期”监控谁需要完成调查表。

1. 单击 **计划应答期**。

    * 在您可以结束计划会话时，删除所有其余计划应答期。  

2. 单击 **删除**。

3. 单击 **是**。

4. 关闭该页面。

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a>当所有回应者均已完成调查表且/或已删除其余所有计划应答期时结束计划。

1. 单击 **功能**。
2. 单击 **结束**。
3. 单击 **确定**。



[!INCLUDE[footer-include](../includes/footer-banner.md)]
