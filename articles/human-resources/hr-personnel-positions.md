---
title: 职位
description: 本主题介绍职位可以包含的概念元素。 它还提供展示如何在组织中使用这些元素的示例。
author: andreabichsel
ms.date: 06/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPosition, HcmPersonnelManagementWorkspace
audience: Application User
ms.author: anbichse
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 269054
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c8311df31326faeadd280585115338317b19125d54f3a526b4ccc6ef6684ad2c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6754744"
---
# <a name="positions"></a>职位

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题介绍职位可以包含的概念元素。 它还提供展示如何在组织中使用这些元素的示例。

必须先设置工作，才能创建职位。 某些职位详细信息（例如薪酬区域、工作人员分配、职位持续时间和报告关系）具有生效日期。

## <a name="general-information"></a>一般信息

创建职位时，您必须选择工作。 以下信息将从您选择的工作中自动填写：

- 说明
- 岗位名称
- 全职等价
- 工作系列

职位职称用于引用员工的职称。 （不使用对员工列出的职称。）因此，职位职称应尽可能标准化。

> [!NOTE]
> 工作人员不能在可用于分配日期之间的日期分配到职位。
>
> **Human Resources 共享参数** 页面的 **职位** 选项卡上的参数控制工作人员分配行为。 选择以下值之一：
>
> - **始终** – 创建新的职位时，可将工作人员分配到这些职位。 在创建职位时，**职位** 页的 **常规** 选项卡上的 **可进行分配的日期和时间** 将自动设置为创建日期和时间。
> - **从不** – 创建新的职位时，您无法将工作人员分配到这些职位。 如果选择此选项，必须为每个新职位（当它变为可用时）打开 **职位** 页面。 然后，在 **常规** 选项卡上，输入 **可用于分配** 日期以启用工作人员分配。 如果选择此选项，当尝试分配工作人员时，工作人员分配日期将默认设置为 **从不**。

## <a name="position-duration"></a>职位持续时间

对于引用为持续时间的特定时间段，每个职位都有效。 例如，夏季职位的持续时间可能为 2021 年 5 月 1 日至 2021 年 8 月 31 日。 激活日期是职位在系统中处于活动状态的日期。 退休日期是职位在系统中不再处于活动状态的日期。

请注意，可用于分配日期和工作人员分配日期都不能早于激活日期。 在达到激活日期之前，不会将职位视为活动。 此外，工作人员分配不能超过职位的退休日期。

## <a name="reports-to-position"></a>直接上级职位

职位是更低级别的组织层次结构中的重要元素。 在 **职位** 页面上，您可以指定某个职位向其进行报告的职位。 将工作人员分配到向另一个职位报告的职位时，创建分配给这两个职位的工作人员之间的报告关系。 例如，职位 000220 向职位 000300 报告。 Kim Akers 分配到职位 000220，而 Sanjay Patel 分配到职位 000300。 因此，Kim Akers 向 Sanjay Patel 报告。

> [!TIP]
> 在整个系统中使用直接上级职位以确定谁是员工的经理。 在前面的示例中，如果在系统中将经理角色分配给 Sanjay Patel，他将在经理自助服务中将 Kim Akers 视为直接下属。 创建工作流传递规则和清单任务时也可以使用报告关系。

## <a name="relationships"></a>关系

如果您的组织使用矩阵层次结构或其他自定义层次结构，您可以设置职位层次结构类型。 然后，您可以向您设置的每个层次结构类型的职称添加报告关系。 例如，Lori Penor 是 Adventure Works 的总经理，并分配到 **总经理** 职位。 Lori 管理用于清洗小机械的产品的开发。 她需要一名会计师来帮助她处理财务工作。 因此，她招聘 Kim Akers 成为其会计师。 Kim 直接向 Sanjay Patel 报告，但她还与 Lori Penor 一起从事其与为开发小机械清洗剂融资相关的工作。

对于前面的示例，您必须完成以下任务来设置 Kim Akers 和 Lori Penor 之间的工作关系：

1. 创建一个名为 **小机械** 的自定义职位层次结构类型，以创建包括负责从事小机械清洗剂产品工作的职位的层次结构。
2. 在 **小机械** 层次结构中，将 **总经理** 职位指定为 Kim 职位向其进行报告的职位。
3. 使用职位层次结构查看职位的报告结构。 如果您有多个职位层次结构，则可在职位层次结构中查看每个层次结构类型的层次结构。 您还可以按职位 ID 或分配到职位的工作人员的姓名搜索职位。 职位层次结构的组织层次结构。

## <a name="labor-union"></a>工会

您可以记录该职位是否需要联合协议，以及使用的工会。 您还可以将协议与法人相关联。

## <a name="financial-dimensions"></a>财务维度

为职位创建财务维度时，必须指定法人。 您可以分别为每个维度选择默认维度。 或者，您可以选择一个分配模板来自动填充默认维度。 分配模板还提供了跨多个维度值分配金额的选项。
