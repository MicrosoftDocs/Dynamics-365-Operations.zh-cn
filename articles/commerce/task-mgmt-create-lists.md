---
title: 创建任务列表和添加任务
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建任务列表和向其添加任务。
author: gvrmohanreddy
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: e7964181a739a8138011abca77d0321d819e0a98
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/06/2021
ms.locfileid: "6354485"
---
# <a name="create-task-lists-and-add-tasks"></a>创建任务列表并添加任务

[!include [banner](includes/banner.md)]

此主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建任务列表和向其添加任务。

*任务* 定义某人必须在指定日期或之前完成的一份工作或一个操作。 在 Dynamics 365 Commerce 中，任务中可以包含详细说明和有关联系人的信息。 还可以包含后勤运营、销售点 (POS) 操作或站点页的链接，以便帮助提高生产力和提供任务负责人高效完成任务所需上下文。

*任务列表* 是业务流程中必须完成的任务的集合。 例如，有一个任务列表是新工作人员在入职期间必须完成的，有一个任务列表针对夜班工作的收银员，还有一个任务列表是为商店准备即将到来的假日需要完成的。 在 Commerce 中，可以将具有目标日期的每个任务列表分配给任意数量的商店或员工，并且可以将其配置为重复任务列表。

经理和工作人员都可以在 Commerce 后端创建任务列表，然后将其分配给一组商店。

## <a name="create-a-task-list"></a>创建任务列表

若要创建任务列表，请执行以下步骤。

1. 转到 **Retail 和 Commerce \> 任务管理 \> 任务管理管理**。
1. 选择 **新建**，然后在 **名称**、**描述** 和 **负责人** 字段中输入值。
1. 选择 **保存**。

## <a name="add-tasks-to-a-task-list"></a>向任务列表添加任务

若要向任务列表添加任务，请执行以下步骤。
 
1. 在现有任务列表的 **任务** 快速选项卡上，选择 **新建** 添加任务。
1. 在 **创建新任务** 对话框的 **名称** 字段中，输入任务的名称。
1. 在 **从目标日期算起的到期日期偏置** 字段中，输入正整数或负整数值。 例如，如果任务应该在任务列表到期日期之前两天完成，则输入 **-2**。
1. 在 **注释** 字段中，输入详细说明。
1. 在 **联系人** 字段中，输入任务负责人在需要帮助时可以联系的主题专家的姓名。
1. 在 **任务链接** 字段中，根据任务的性质输入链接。

> [!TIP]
> 虽然在创建任务列表时可以使用 **分配到** 字段将任务分配给某人，我们还是建议您避免在创建任务列表期间分配任务。 而是在针对单个商店实例化了列表之后分配任务。

## <a name="use-task-links-to-help-improve-worker-productivity"></a>使用任务列表帮助提高工作人员的生产力

Commerce 让您可以将任务链接到特定 POS 操作，如运行销售报表，查看面向新员工的在线培训视频，或执行后端操作。 此功能帮助任务负责人获取有关高效完成任务所需信息。

若要在创建任务时添加任务链接，请执行以下步骤。

1. 在现有任务列表的 **任务** 快速选项卡上，选择 **编辑**。
1. 在 **编辑任务** 对话框的 **任务链接** 字段中，选择以下选项中的一个或多个：

    - 选择 **菜单项** 配置后端操作，例如“产品套件”。
    - 选择 **POS 操作** 配置 POS 操作，例如“销售报表”。
    - 选择 **URL** 配置绝对 URL。

下图显示 **编辑任务** 对话框中的任务链接的选择情况。

![在“编辑任务”对话框中选择任务链接。](media/HQ-POS-Tasks-Linking.png)

### <a name="configure-a-pos-operation-so-that-it-can-be-linked-to-a-task"></a>配置 POS 操作以使其可链接到任务

若要配置 POS 操作以使其可链接到任务，请执行以下步骤。

1. 转到 **Retail 和 Commerce \> 渠道设置 \> POS 设置 \> POS \> POS 操作**。
1. 选择 **编辑**，找到 POS 操作，然后选中其 **启用任务管理** 复选框。

## <a name="additional-resources"></a>其他资源

[任务管理概述](task-mgmt-overview.md)

[配置任务管理](task-mgmt-configure.md)

[将任务列表分配给商店或员工](task-mgmt-assign-lists.md)

[POS 中的任务管理](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
