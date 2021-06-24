---
title: 输入技能
description: 工作人员和经理可以在 Dynamics 365 Human Resources 中输入技能。
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 5a65f1884ea87bbf2519cc94e4c52a40ac1a91bd
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193969"
---
# <a name="enter-skills"></a>输入技能

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

您可以在 Dynamics 365 Human Resources 中输入工作人员、申请人或联系人的目标技能或实际技能。 目标技能是计划达到的技能。 实际技能是当前具有的技能。

## <a name="create-a-workflow-to-auto-approve-skills"></a>创建工作流来自动审核技能

要输入技能而无需审核，您必须创建一个工作流来自动审核技能。

> [!NOTE]
> 工作人员输入的技能始终需要经理审核。 此工作流仅自动审核经理代表其工作人员输入的技能。

1. 在 **人事管理** 工作区中，选择 **链接**。

2. 在 **设置** 下，选择 **人力资源工作流**。

3. 选择 **新建**。

4. 在 **创建工作流** 窗格中，选择 **工作人员技能**。

   [![选择工作人员技能工作流](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)

5. 在 **打开此文件?** 对话中，选择 **打开**。 出现提示时，输入您的凭据。

6. 在工作流编辑器中，选择 **审核技能** 工作流元素并将其拖到画布上。

   [![选择审核技能工作流元素](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)

7. 将 **开始** 元素连接到 **审核技能 1** 元素，然后将 **审核技能 1** 元素连接到 **结束** 元素。 您可能需要向下滚动来查看 **结束** 元素。 您可以将其拖到更靠近其他元素的位置。

   [![连接工作流元素](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)

8. 双击 **审核技能 1** 工作流元素，然后右键单击 **步骤 1** 元素。 右键单击 **步骤 1** 元素，然后选择 **属性**。

9. 在 **属性** 窗口中，在左侧导航栏上选择 **条件**。

10. 选择 **仅当满足以下条件时运行此步骤**。

11. 选择 **添加条件**。 在 **位置** 之后，选择 **员工自助服务技能**，然后选择 **员工自助服务技能.人员**。 在 **是** 之后，选择 **现场**，然后选择 **用户与人员的关系.人员**。

    [![指定条件](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)

12. 在左侧导航栏上选择 **分配**。

13. 在 **分配类型** 选项卡上，选择 **层次结构**。

14. 在 **层次结构选择** 选项卡上，在 **层次结构类型:** 字段中，选择 **管理层次结构**。

    [![指定管理层次结构](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)

15. 选择 **关闭**，在画布痕迹导航中选择 **工作流**，然后选择 **保存并关闭**。

有关创建工作流的详细信息，请参阅[工作流系统概述](../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md?toc=/dynamics365/human-resources/toc.json)。

## <a name="enter-skills-for-a-worker"></a>输入工作人员的技能

1. 选择一个工作人员。

2. 在 **工作人员** 页面的操作栏中，选择 **人员**，然后选择 **技能**。

3. 在 **技能** 页面上，为每个技能完成以下字段：

   - **技能**：选择一项技能。
   - **级别类型**：对于工作人员已有的技能，选择 **实际**，对于工作人员正在努力掌握的技能，选择 **目标**。
   - **级别**：为工作人员的技能选择级别。
   - **级别日期**：在日历工具中选择一个日期。
   - **主考人**：如果适用，从列表中选择主考人。 您可以对搜索进行筛选。
   - **年资**：输入拥有经验的年数。
   - **已验证**：如果技能已经过验证，选中此框。
   - **验证人**：输入验证者的姓名。

4. 输入技能后，选择 **保存**。

## <a name="see-also"></a>请参阅

[配置技能](hr-develop-skills.md)<br>
[映射技能](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]