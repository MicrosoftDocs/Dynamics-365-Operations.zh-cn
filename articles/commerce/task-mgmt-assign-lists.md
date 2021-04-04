---
title: 将任务列表分配给商店或员工
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中将任务列表分配给商店或员工。
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 3d249809f15b50c59620d69a901a427dc3ecb2f0
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477576"
---
# <a name="assign-task-lists-to-stores-or-employees"></a>将任务列表分配给商店或员工

[!include [banner](includes/banner.md)]

此主题介绍如何在 Microsoft Dynamics 365 Commerce 中将任务列表分配给商店或员工。

可通过 Dynamics 365 Commerce 中的任务管理将任务列表分配给多个商店或员工，或分配给商店和员工的组合。 例如，一位 20 家商店的地区经理可能希望将 **假日准备** 任务列表分配给所有 20 商店。

## <a name="start-the-task-list-assignment-process"></a>开始任务列表分配流程

若要开始分配任务列表流程，请执行以下步骤。

1. 转到 **Retail 和 Commerce \> 任务管理 \> 任务管理管理**。
1. 选择要分配的任务列表。
1. 选择 **启动流程**。
1. 在 **启动流程** 对话框的 **常规** 选项卡上 **流程名称** 字段中，输入名称（例如，**东部商店**）。
1. 在 **目标日期** 字段中，指定一个日期。
1. 若要将任务列表分配给商店，请在 **商店** 选项卡上，使用 **组织层次结构** 筛选器查找和选择商店。

    若要将任务列表分配给工作人员，请在 **工作人员** 选项卡上，找到和选择员工。

1. 选择 **确定** 开始执行流程。 将把任务列表分配给所选商店或员工。

下图显示如何在 **启动流程** 对话框中查找和选择商店的示例。

![在“启动流程”对话框中查找和选择商店](media/HQ-Assign-Tasks-Lists.png)

## <a name="assign-task-lists-on-a-recurring-basis"></a>在重复执行基础上分配任务列表

零售商有时会有重复执行任务，如“星期四歇业核对清单”或“月初核对清单”。 因此，他们可能希望在重复执行基础上分配任务列表。

1. 转到 **Retail 和 Commerce \> 任务管理 \> 任务管理管理**。
1. 选择要分配的任务列表。
1. 选择 **启动流程**。
1. 在 **启动流程** 对话框的 **常规** 选项卡上 **流程名称** 字段中，输入名称。
1. 将 **重复执行** 选项设置为 **是**。
1. 在 **以天为单位的重复执行目标日期偏置** 字段中，输入天数。 例如，如果输入 **4**，则目标日期为重复执行日期加上四天。
1. 在 **在后台运行** 选项卡上，选择 **重复执行**。
1. 在 **定义重复执行** 对话框中，输入频率条件，然后选择 **确定**。

下图显示如何在 **定义重复执行** 对话框中输入频率条件的示例。

![在“定义重复执行”对话框中输入频率条件](media/HQ-Assign-Tasks-Lists-Recurrently.png)

## <a name="track-task-list-status"></a>跟踪任务列表状态

如果您是区域经理或商店经理，您可能需要跟踪已分配给多家商店或员工的任务列表的状态。 然后可以跟进未及时完成所分配任务的商店或工作人员。 Commerce 后端让您可以查看任务列表的状态，重新分配任务，或更改任务的状态。

若要跟踪所有任务的任务列表状态，请执行以下步骤。

1. 转到 **Retail 和 Commerce \> 任务管理 \> 任务管理流程**。
1. 选择 **所有任务列表** 选项卡以查看分配给各商店的所有任务列表的状态。

若要跟踪分配给您的所有任务的任务列表状态，请执行以下步骤。

1. 转到 **Retail 和 Commerce \> 任务管理 \> 任务管理流程**。
1. 选择 **我的任务** 或 **所有任务** 选项卡以查看或更新分配给您的任务的状态。

## <a name="additional-resources"></a>其他资源

[任务管理概述](task-mgmt-overview.md)

[配置任务管理](task-mgmt-configure.md)

[创建任务列表和添加任务](task-mgmt-create-lists.md)

[POS 中的任务管理](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
