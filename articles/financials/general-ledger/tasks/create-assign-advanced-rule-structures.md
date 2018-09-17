--- 
title: "创建和分配高级规则结构"
description: "此任务指南介绍创建高级规则结构并分配至帐户结构的步骤。"
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: ebad4ec9ec6242978a26007a64416ae1b2af5c28
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-assign-advanced-rule-structures"></a>创建和分配高级规则结构

[!include [task guide banner](../../includes/task-guide-banner.md)]

此任务指南介绍创建高级规则结构并分配至帐户结构的步骤。 此指南使用演示公司 USMF。


## <a name="create-an-advanced-rule-structure"></a>创建高级规则结构
1. 转到“总帐”>“会计科目表”>“结构”>“高级规则结构”。
2. 单击“新建”，以打开对话框。
3. 在“高级规则结构”字段中，输入描述规则结构的名称。
4. 在“描述”字段中，输入描述结构的值。
5. 单击“确定”。
6. 单击“添加分部”。
7. 在“分部”列表中，选择财务维度。
    * 例如：商店。  
8. 单击“添加分部”。
9. 在列表中，单击高级规则结构的链接以进行查看。
10. 单击“启用”。
11. 单击“启用”。

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a>应用高级规则结构到科目结构中
1. 关闭窗体。
2. 关闭该页面。
3. 转到“总帐”>“会计科目表”>“结构”>“配置科目结构”。
4. 在列表中，找到并选择您想应用高级规则的科目结构。
5. 单击科目结构的名称，以打开该科目结构。
6. 单击“编辑”。
    * 您还可以点击“高级规则”，将会提示您将科目结构设置为草稿模式。  
7. 单击“高级规则”。
8. 单击“新建”，以打开对话框。
9. 在“高级规则”字段中，键入一个值。
10. 在“名称”字段中，键入一个值。
11. 单击“创建”。
12. 单击“添加新条件”。
13. 在“目标位置”字段中，选择主科目或财务维度。
14. 在“运算符”字段中，选择一个选项，例如“介于并包含”。
15. 在“值”字段中，键入一个值。
16. 在“范围”字段中，键入一个值。
17. 单击“添加”以打开下拉对话框。
18. 在列表中，找到满足您输入的条件时使用的高级规则结构。
19. 单击“添加”。
20. 关闭该页面。
21. 单击“启用”。
22. 单击“启用”。


