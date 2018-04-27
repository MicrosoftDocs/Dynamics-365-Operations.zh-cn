--- 
title: "使用移动作业设备配置工作人员"
description: "该过程向您显示如何给工作人员的用户帐户分配正确的角色，并使工作人员执行车间登记。"
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: dadf0e87eac8522f61bb094c146e37f46a21fc09
ms.openlocfilehash: f9de2f79c68fead5ede714ff05bba97118874aad
ms.contentlocale: zh-cn
ms.lasthandoff: 02/06/2018

---
# <a name="configure-a-worker-using-the-mobile-job-device"></a>使用移动作业设备配置工作人员

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

该过程向您显示如何给工作人员的用户帐户分配正确的角色，并使工作人员执行车间登记。


## <a name="assign-roles-to-user-account"></a>将角色分配给用户帐户
1. 转到“系统管理”>“用户”>“用户”。
2. 使用“快速筛选器”以筛选用户帐户与机器操作员角色关联的工作人员姓名。 在示例数据中，名称应为“Shannon”。
3. 突出显示用户帐户记录。
4. 在此列表中，单击在所选行的“名称”链接以查看用户帐户的详细信息。
5. 在树形图中，请选择“角色\机器操作员”。
6. 关闭用户帐户详细信息页。
7. 关闭该页面。

## <a name="configure-worker-account"></a>配置工作人员帐户。
1. 转到“人力资源”>“工作人员”>“工作人员”。
2. 使用“快速筛选器”以筛选用户帐户与机器操作员角色关联的工作人员姓名。 在示例数据中，名称应为“Shannon”。
3. 突出显示用户帐户记录。
4. 在此列表中，单击在所选行的“名称”链接以查看用户帐户的详细信息。
5. 单击“雇用”选项卡。
6. 展开“时间登记”快速选项卡并单击“激活登记终端”。
7. 单击“激活登记终端”。
8. 在“计算组”字段中，输入或选择一个值。
9. 在“默认计算组”字段中，输入或选择一个值。
10. 在“批准组”字段中，输入或选择一个值。
11. 在“标准模板”字段中，输入或选择一个值。
12. 在“模板组”字段中，输入或选择一个值。
13. 单击“确定”。
14. 单击“编辑”为新时期登记的工作人员输入一个标记编号。
15. 在“标记 ID”字段中，键入一个值。
16. 单击“保存”。
17. 使用“保存记录”快捷方式。
18. 关闭工作人员详细信息页
19. 关闭该页面。

## <a name="assign-worker-to-device-group"></a>将工作人员分配到设备组。
1. 转到“生产控制”>“设置”>“制造执行”>“为设备配置作业卡”。
2. 单击“添加”。
3. 在列表中，标记所选的行。
4. 单击“确定”。
5. 单击“编辑”。
6. 在“生产单位”字段，您可以设置工作人员的默认筛选器。 这将确保在工作人员登录到设备时，只显示所选生产单位的生产作业。
7. 关闭该页面。

