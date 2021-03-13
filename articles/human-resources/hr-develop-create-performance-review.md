---
title: 创建绩效审核
description: 此主题介绍如何创建绩效审核和介绍审核各部分的目的。
author: andreabichsel
manager: tfehr
ms.date: 05/05/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EssWorkspace, HcmDiscussionNewDialog, HcmDiscussion, HcmDiscussionChangeSettings, HcmDiscussionAddGoalDialog, HcmTopicCreate, HcmMeasurementDetailDialog, HcmPerfJournalAdd, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e83bcf60e494e6f04387727bedf41175faa07557
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115792"
---
# <a name="create-performance-reviews"></a>创建绩效审核


此主题介绍如何创建绩效审核和介绍审核各部分的目的。 创建该过程的演示数据公司是 USMF。

1. 在主页中，选择 **员工自助服务** 工作区。
2. 选择 **新审核** 创建新审核。
3. 在 **审核类型** 字段中，输入或选择一个值。
4. 在 **绩效期间** 字段中，输入或选择一个值。
5. 在 **结束日期** 字段中，输入日期。
6. 选择 **确定**。 您还可以从模板创建审核。 这是最好的审核创建方法，因为每个部分中都包含启动审核所需信息。  
7. 可以显示或隐藏附件选项卡之类选项卡：

    1. 在操作窗格上，选择 **显示部分** 以打开对话框菜单。
    1. 在 **显示附件** 字段中选择 **是** 或 **否** 以显示或隐藏附件选项卡。
    1. 选择 **保存**。

8. 选择 **添加要审核的目标** 以添加目标。 完成后，选择 **确定**。
9. 选择 **添加能力** 以打开下拉对话框。
10. 在 **标题** 字段中，键入一个值。
11. 在 **描述** 字段中，输入 `Increase customer skills by working with the support team`。
12. 选择 **确定**。
13. 选择 **全部折叠**。
14. 选择 **全部展开**。
15. 选择 **添加注释**。
16. 选择 **过帐**。
17. 选择 **度量** 选项卡。
18. 选择 **添加度量** 以打开对话框菜单。
19. 在 **度量** 字段中，输入或选择一个值。
26. 在 **目标金额** 字段中，输入一个数字。
20. 选择 **确定**。
21. 选择 **活动** 选项卡。
22. 选择 **添加**。
23. 在 **标题** 字段中，键入一个值。
24. 在 **描述** 字段中，键入一个值。
25. 在 **开始日期** 字段中，输入一个日期。
26. 在 **完成日期** 字段中，输入一个日期。
27. 在 **开发计划** 字段中，选择 **是**。
28. 在 **关键字** 字段中，键入一个值。
29. 选择 **保存**。
30. 选择 **等级** 选项卡。  

    - **等级详细信息** 快速选项卡允许员工对自己进行评分，并允许经理对员工进行评分。 如果使用权重，将自动计算分数的权重值。  
    - 要查看此部分，请启用用于显示员工等级的参数设置。  

31. 选择 **签核** 选项卡。如果审核使用工作流，则仅在完成工作流之后，才显示签核。 如果不使用工作流，则同时在此处列出工作人员和经理。 将根据审核类型的设置选中所需复选框。  
32. 选择 **常规** 选项卡。

    - 绩效期间创建默认开始和结束日期。 这些日期可编辑。  
    - 状态控制对审核的访问。 **未开始** 状态允许任何人编辑审核。 **进行中** 状态仅允许员工查看和编辑审核。 **为审核做准备** 仅允许管理员查看和编辑审核。 **最终审核** 状态使员工和经理都可以查看审核，还允许进行编辑（如果在审核类型中进行了设置）。 **已完成** 和 **已取消** 状态会使审核为只读。 如果审核被 **拒绝** 并发回给员工，则员工和经理都可以进行必要的编辑，以便员工可以重新提交。

33. 在 **概述** 字段中，键入一个值。
34. 选择 **审核** 选项卡。随着审核经历这些状态，员工和经理可以为每个目标或能力添加注释。  
35. 选择 **签核** 选项卡。工作人员和经理可以签核审核。 当所有必需签核均已完成时，状态将更改为 **已完成**，并且再也不能执行更改。  

