---
title: 使用移动作业设备配置工作人员
description: 本文介绍如何给工人的用户帐户分配正确的角色，并使工人执行车间登记。
author: johanhoffmann
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3f6f51a66d49cafd172ba123bf883fb41cdcb5c3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844296"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a>使用移动作业设备配置工作人员

[!include [banner](../../includes/banner.md)]

本文介绍如何给工人的用户帐户分配正确的角色，并使工人执行车间登记。

## <a name="verify-that-a-worker-is-assigned-a-certain-role"></a>验证是否为工人分配了特定角色。

对于此示例，配置工人帐户之前，验证是否为用户“SHANNON”分配了机器操作员角色。

1. 转到 **导航窗格 > 模块 > 系统管理 > 用户 > 用户**。
2. 在快速筛选器中搜索用户。 在这个例子中，输入 `shannon`。
3. 在显示的用户帐户的 **用户 ID** 列中选择链接。
4. 在 **用户的角色** 树中，选择 **角色 > 机器操作员**。
5. 关闭 **用户详细信息** 和 **用户** 页回到主页。

## <a name="configure-worker-account"></a>配置工人帐户
1. 转到 **导航窗格 > 模块 > 人力资源 > 工人 > 工人**。
2. 在快速筛选器中搜索用户。 在这个例子中，输入 `shannon`。
3. 在显示的用户帐户的 **名称** 列中选择链接。
4. 选择 **时间登记** 选项卡。
5. 选择 **在登记终端上启用**。
6. 在下列字段中输入或选择值：  

    - **计算组**  
    - **默认计算组**  
    - **审核组**  
    - **标准模板**  
    - **模板组**  

7. 选择 **确定**。
8. 选择 **编辑** 为新时期登记的工人输入一个标记编号。 在 **标记 ID** 字段中，输入一个值。
9. 选择 **保存**。
10. 关闭 **工人详细信息** 和 **工人** 页。

## <a name="assign-worker-to-device-group"></a>将工人分配到设备组
1. 转到 **生产控制 > 设置 > 制造执行 > 为设备配置作业卡**。
2. 选择 **添加**。
3. 在列表中，选择所需的工人。 在这个例子中，选择 **SHANNON**。
4. 选择 **确定**。
5. 选择 **编辑**。
6. 在 **生产单位** 字段，您可以设置工人的默认筛选器。 这将确保在工作人员登录到设备时，只显示所选生产单位的生产作业。 输入所需值。
7. 关闭该页面。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]