---
title: 在工作流中委托工作项
description: 如果您计划外出一段时间或无法对工作项进行操作，则您可以将您的工作项委托或重新分配给其他用户。
author: ChrisGarty
ms.date: 07/07/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed21f6d32cdcf74eb153daba32c20b7cef94d4e4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747361"
---
# <a name="delegate-work-items-in-a-workflow"></a>在工作流中委托工作项

[!include [banner](../../includes/banner.md)]

## <a name="manually-delegate-a-work-item"></a>手动委托工作项

若要委托单个工作项，请在 **工作流** 菜单中选择 **委托** 选项，然后输入要委托给的用户和注释。 这将把该工作项重新分配给该用户，以便该用户完成此工作项。

## <a name="manually-delegate-multiple-work-items"></a>手动委托多个工作项

可以从 **分配给我的工作项** 页一并委托多个工作项。 以下工作流类型支持批量委托：采购协议审核工作流、采购订单工作流、采购申请审核和供应商账单工作流。 **委托多个工作项** 功能默认已禁用，可以在 **工作区 > 功能管理** 中启用。 请与系统管理员联系，获取启用此功能的帮助。
1.  转到 **通用 > 通用 > 工作项 > 分配给我的工作项**。
2.  选择将委托的工作项。
3.  单击 **委托工作项** 菜单。
4.  在 **用户** 字段中，选择要将工作项委托给的用户。
5.  在 **注释** 字段中，输入说明您委托工作项的原因的注释。
6.  单击 **委托工作项** 按钮完成工作项委托。

## <a name="automatically-delegate-work-items"></a>自动委托工作项

如果您计划外出或一段时间无法对工作项进行操作，可以使用 **用户选项** 页面将新工作项自动委托给其他用户。

### <a name="set-up-automatic-delegation"></a>设置自动委托
1. 转到 **常规 > 设置 > 用户选项**。
2. 单击 **工作流** 选项卡。确保展开“委托”部分。 要将系统配置为自动将您的工作项委托给其他用户，则您必须创建委托规则，指定何时委托特定类型的工作项。 按照以下步骤创建委托规则。  
3. 单击 **添加**。
4. 在 **范围** 字段中，选择一个选项：
    - “所有”- 委托所有分配给您的所有工作项。
    - 模块 – 仅委托与特定类型的工作流有关的工作项。 如果您选择此选项，则必须在 **名称** 字段中选择工作流的类型。
    - 工作流 – 仅委托与特定工作流有关的工作项。 如果您选择此选项，则必须在 **名称** 字段中选择工作流。  
5. 在 **名称** 字段中：
    - 对于 **模块** 范围，选择目标模块。
    - 对于 **工作流** 范围，选择目标工作流。
6. 在 **委托** 字段中，选择要将工作项委托给的用户。 使用 **开始日期/时间** 和 **结束日期/时间** 字段指定希望自动委托工作项的时间。  
7. 在 **开始日期/时间** 字段中，输入日期和时间。
8. 在 **结束日期/时间** 字段中输入日期和时间。
9. 选中 **启用** 复选框以启用该委托规则。 
10. 在 **注释** 字段中，输入说明您委托工作项的原因的注释。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]