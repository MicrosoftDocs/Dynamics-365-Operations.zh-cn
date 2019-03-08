---
title: 在工作流中委托工作项
description: 如果您计划外出一段时间或无法对工作项进行操作，则您可以将您的工作项委托或重新分配给其他用户。
author: jasongre
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: f85a1318822ceaf829134bf2eb3581e350d5bea4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "346241"
---
# <a name="delegate-work-items-in-a-workflow"></a>在工作流中委托工作项

[!include [task guide banner](../../includes/task-guide-banner.md)]

如果您计划外出一段时间或无法对工作项进行操作，则您可以将您的工作项委托或重新分配给其他用户。 此过程帮助您配置系统以自动将您的工作项委托给其他用户。



创建此程序的演示数据公司是 USMF。


## <a name="set-up-automatic-delegation"></a>设置自动委托
1. 转到“常规 > 设置 > 用户选项”。
2. 单击“工作流”选项卡。
    * 确保已展开“委托”部分。    要将系统配置为自动将您的工作项委托给其他用户，则您必须创建委托规则，指定何时委托特定类型的工作项。 按照以下步骤创建委托规则。  
3. 单击“添加”。
4. 在“范围”字段中，选择一个选项。
    * “所有”- 委托所有分配给您的所有工作项。    模块 – 仅委托与特定类型的工作流有关的工作项。 如果您选择此选项，则必须在“名称”字段中选择工作流的类型。    工作流 – 仅委托与特定工作流有关的工作项。 如果您选择此选项，则必须在“名称”字段中选择工作流。  
5. 在“委托”字段中，选择要将工作项委托给的用户。
    * 使用“开始日期/时间”和“结束日期/时间”字段指定希望自动委托工作项的时间。  
6. 在“开始日期/时间”字段中，输入日期和时间。
7. 在“结束日期/时间”字段中输入日期和时间。
8. 选中“启用”复选框以启用该委托规则。
    * 如果已将“模块”选择为“范围”，则必须在“名称”字段中选择该模块。    如果已将“工作流”选择为“范围”，则必须在“名称”字段中选择要委托的具体工作流。  
9. 在“注释”字段中，输入说明您委托工作项的原因的注释。

