---
title: 让劳动力技能符合业务需要
description: 您可以跟踪工作人员、申请人或联系人具有或应该具有的技能，以有效地履行其角色。 您还可以指定特定工作所需的技能。
author: andreabichsel
manager: tfehr
ms.date: 11/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
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
ms.openlocfilehash: 26493306a8bd810f936b15160b07263ca41f87ae
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115576"
---
# <a name="align-workforce-skills-with-business-needs"></a>让劳动力技能符合业务需要

您可以跟踪工作人员、申请人或联系人具有或应该具有的技能，以有效地履行其角色。 您还可以指定特定工作所需的技能。

您可以跟踪的技能示例包括以下内容：
-   监督能力 - 监督其他人的工作的能力。
-   领导能力 - 在员工和业务领域中起领导作用的能力。
-   计划能力 - 洞察未来发展趋势的能力。
-   HTML – 编写 HTML 代码的能力。

在您可以将技能分配给人员或工作，创建技能表搜索或创建技能模板之前，必须在 **技能** 页上输入有关技能的信息。 对于每个技能，您可以选择技能类型和评级模型。

## <a name="rating-models"></a>评级模型
评级模型帮助评估人员的实际技能级别，应达到的级别或工作需要的技能级别。 您最多可以输入评级模型的 10 个级别。  评级模型中的每个级别都会被分配一个系数。  系数值将用于标准化使用不同评级模型的技能分数。  该系数必须是 0-9 之间的数字，并且每个级别都必须有唯一的系数。  用更高系数值的级别在评级模型中更有重量。

## <a name="specify-job-skills"></a>指定工作技能
在您输入该工作信息时，您可以指定用户在可以承担该职务的工作前应该具有的技能。  此外，您还可以为每个技能指定所需级别以及技能的重要程度。 同一技能对不同工作的重要程度各不相同。

## <a name="enter-skills-for-workers-applicants-or-contacts"></a>输入工作人员、申请人或联系人的技能
您可以输入工作人员、申请人或联系人的目标技能或实际技能。 目标技能是计划达到的技能。 实际技能是当前具有的技能。

## <a name="skill-mapping-and-skill-mapping-profiles"></a>技能表和技能表模板
您可以创建技能表搜索找到有资格执行特定类型任务的工作人员、申请人或联系人。 技能表搜索会跨技能、教育、证书、诚信职位和项目经验进行查找并返回与输入的条件匹配的结果。  例如，知道您的组织中哪些工作人员获得了其 CPA 可能很有用。

技能表模板允许您查找具备具有直接符合业务需要的当前员工或候选人。  例如，您可以为您的组织中的一个空缺职位创建技能表模板。 通过为特定工作创建模板并从该工作将技能、教育和证书复制到模板，您可以迅速搜索与模板中输入的一个或多个条件匹配的工作人员、申请人，并查看其技能最密切匹配该工作所要求的技能的候选人列表。

> **注意** 只有在技能表搜索中包括的所选工作人员、申请人和联系人可以在技能表搜索结果列表中显示或包含在技能模板中。 若要将工作人员、申请人或联系人包括到技能表搜索中，请在以下页面中将 **包括在技能表中** 选择设置为“是”：
> 
> + 工作线程
> + 员工
> + 申请人
> + 联系人

## <a name="skill-gap-analysis-and-skill-profile-analysis"></a>技能差距分析和技能模板分析
您可以创建技能模板分析查看截至特定日期工作人员、申请人或联系人的能力列表。 可以创建一个技能差距分析将人员的技能与某一特定工作所要求的技能加以比较  




[!INCLUDE[footer-include](../includes/footer-banner.md)]