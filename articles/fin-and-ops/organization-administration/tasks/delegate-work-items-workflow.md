---
title: 在工作流中委托工作项
description: 如果您计划外出一段时间或无法对工作项进行操作，则您可以将您的工作项委托或重新分配给其他用户。
author: jasongre
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 44dc747543e32b54729d12c89a401b0187e25a61
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916407"
---
# <a name="delegate-work-items-in-a-workflow"></a>在工作流中委托工作项

[!include [task guide banner](../../includes/task-guide-banner.md)]

## <a name="manually-delegate-a-work-item"></a>手动委托工作项

若要委托单个工作项，请在**工作流**菜单中选择**委托**选项，然后输入要委托给的用户和注释。 这将把该工作项重新分配给该用户，以便该用户完成此工作项。

## <a name="automatically-delegate-work-items"></a>自动委托工作项

如果您计划外出或一段时间无法对工作项进行操作，可以使用**用户选项**页面将新工作项自动委托给其他用户。

### <a name="set-up-automatic-delegation"></a>设置自动委托
1. 转到**常规 > 设置 > 用户选项**。
2. 单击**工作流**选项卡。确保展开“委托”部分。 要将系统配置为自动将您的工作项委托给其他用户，则您必须创建委托规则，指定何时委托特定类型的工作项。 按照以下步骤创建委托规则。  
3. 单击**添加**。
4. 在**范围**字段中，选择一个选项。
    - “所有”- 委托所有分配给您的所有工作项。
    - 模块 – 仅委托与特定类型的工作流有关的工作项。 如果您选择此选项，则必须在“名称”字段中选择工作流的类型。
    - 工作流 – 仅委托与特定工作流有关的工作项。 如果您选择此选项，则必须在“名称”字段中选择工作流。  
5. 在**委托**字段中，选择要将工作项委托给的用户。 使用“开始日期/时间”和“结束日期/时间”字段指定希望自动委托工作项的时间。  
6. 在**开始日期/时间**字段中，输入日期和时间。
7. 在**结束日期/时间**字段中输入日期和时间。
8. 选中**启用**复选框以启用该委托规则。 如果已将**模块**选择为“范围”，则必须在“名称”字段中选择该模块。 如果已将**工作流**选择为“范围”，则必须在“名称”字段中选择要委托的具体工作流。  
9. 在**注释**字段中，输入说明您委托工作项的原因的注释。

