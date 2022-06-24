---
title: 配置技能
description: 您可以在 Dynamics 365 Human Resources 中跟踪工作人员的技能。 您还可以指定特定工作所需的技能。
author: twheeloc
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: acb632042cdb535bea0dd625531f22d284653294
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893749"
---
# <a name="configure-skills"></a>配置技能

> [!IMPORTANT]
> 本文中说明的功能当前对 Finance 基础结构上的 Human Resources 客户可用。  


您可以在 Dynamics 365 Human Resources 中跟踪工作人员的技能。 您还可以指定特定工作所需的技能。

您可以跟踪的技能示例包括：

- 监督能力 - 监督其他人的工作的能力。
- 领导能力 - 在员工和业务领域中起领导作用的能力。
- 计划 – 能够预测未来、建立愿景，并能够深入理解。
- HTML – 编写 HTML 代码的能力。

如果尚未设置技能类型和评级模型，您需要在创建技能之前添加一部分。

以下人员可以为工作人员输入技能：

- 工作人员可以在员工自助服务中为自己输入技能。 这些技能需要经理审核。
- 经理可以为他的工作人员输入技能。 您可以创建自动审核这些技能的工作流。

## <a name="create-a-skill-type"></a>创建技能类型

技能类型是各个技能所属的类别，如管理或销售。

1. 在 **员工发展** 工作区中，选择 **链接**。

2. 在 **能力设置** 下，选择 **技能类型**。

3. 选择 **新建**。

4. 完成以下字段：

   - **技能类型**：为技能类型输入名称。
   - **描述**：为技能类型输入描述。

5. 选择 **保存**。

## <a name="create-a-rating-model"></a>创建评级模型

评级模型帮助评估人员的实际技能级别，应达到的级别或工作需要的技能级别。 评级模型中的每个级别都会被分配一个系数。

1. 在 **员工发展** 工作区中，选择 **链接**。

2. 在 **能力设置** 下，选择 **评级模型**。

3. 选择 **新建**。

4. 完成以下字段：

   - **评级**：为评级模型输入名称，如 **技能**。
   - **描述**：为评级模型输入描述，如 **技能评级**。

5. 在 **级别** 部分，选择 **新建**。 对于要添加的每个级别，填写以下字段：

   - **级别**：为级别输入名称。
   - **描述**：为级别输入描述。
   - **系数**：输入一个 0 到 9 的系数值。 系数帮助标准化使用不同评级模型的技能分数。 每个级别必须有一个唯一系数。 用更高系数值的级别在评级模型中更有重量。

   继续根据需要添加级别。 最多可以为每个评级模型输入 10 个级别。

6. 选择 **保存**。

## <a name="create-a-skill"></a>创建技能

您必须先在 **技能** 页上输入有关技能的信息，然后才能够分配技能或创建技能映射搜索或技能模板。 对于每个技能，您可以选择技能类型和评级模型。

1. 在 **员工发展** 工作区中，选择 **链接**。

2. 在 **能力设置** 下，选择 **技能**。

3. 选择 **新建**。

4. 完成以下字段：

   - **技能**：为技能输入名称。
   - **描述**：为技能输入描述。
   - **评级**：选择您要用于此技能的评级模型。
   - **技能类型**：从技能类型列表中选择。

5. 选择 **保存**。

## <a name="see-also"></a>请参阅

[输入技能](hr-develop-enter-skills.md)<br>
[映射技能](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
