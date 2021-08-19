---
title: 任务录制的安全诊断
description: 本主题提供有关如何根据任务录制来分析和管理安全许可要求的信息。
author: Peakerbl
ms.date: 05/05/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: ''
ms.dyn365.ops.version: Version 10.0.9
ms.openlocfilehash: 44af35f16f6e9ff89b30bc10eef3f16ecdfaf907c4c6e22aa5775d1941fb6a5d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6745112"
---
# <a name="security-diagnostics-for-task-recordings"></a>任务录制的安全诊断

[!include [banner](../../includes/banner.md)]

## <a name="before-you-begin"></a>开始之前

本主题提供有关如何根据任务录制来分析和管理安全许可要求的信息。 在完成本主题中的步骤之前，您必须具有要分析的业务流程的任务录制。 要录制业务流程，请参阅[任务录制器资源](../../user-interface/task-recorder.md)。 

## <a name="manage-security-for-a-task-recording"></a>管理任务录制的安全性

1. 转到 **系统管理** > **安全** > **任务录制的安全诊断**。
2. 从其位置打开任务录制。 选择 **从此 PC 中打开** 或 **从 Lifecycle Services 中打开**，然后选择 **关闭**。
3. 这将打开 **安全菜单项详细信息** 页面，其中列出了该流程所需的安全对象。

 > [!NOTE]
 > 列表中不包括 **操作** 和 **输出** 菜单项。

4. 在 **用户 ID** 字段中，选择一个用户。 如果用户没有某些菜单项的权限，则 **缺少权限** 字段将更新为 **是**。
  
  ![安全菜单项详细信息页面。](../media/Security-Menu-Item-Details.png)

5. 选择 **添加引用** 以查看安全对象的列表，包括授予缺少的权限的角色、职责和特权。
6. 从列表中选择安全对象：

    - 如果选择了 **角色**，请选择 **为用户添加角色**。 这会打开 **将用户分派给角色** 页。 有关详细信息，请参阅[将用户分派给安全角色](assign-users-security-roles.md)。
    - 如果选择了 **职责**，请选择 **将职责添加到角色**，选择应将职责添加到的角色，然后选择 **确定**。
    - 如果选择了 **特权**，请选择 **将特权添加到职责**，选择应将职责添加到的角色，然后选择 **确定**。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]