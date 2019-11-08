---
title: 取消仓库工作以进行异常处理
description: 本主题介绍“取消工作”功能，该功能使仓库主管可以处理被阻止的工作。
author: omulvad
manager: AnnBe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSTroubIeshootingSeIfService
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6aa073f72a3ece81d945f75b32f906d5846f7ce9
ms.sourcegitcommit: bc9b65b73bf6443581c2869a9ecfd0675f0be566
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/15/2019
ms.locfileid: "2625849"
---
# <a name="cancel-warehouse-work-for-exception-handling"></a>取消仓库工作以进行异常处理

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management 中的“取消工作”功能使管理员用户可以取消当前正在进行的特定仓库工作，但是由于特殊情况，该工作已被系统阻止或无法完成。 此功能是修复不一致数据的 SQL 纠正脚本的一种有吸引力且安全的替代方法。 不过，尽管这些脚本通常是从 IT 专业人员那里索要的，但具有管理员权限的公司中的用户可以使用“取消工作”功能。

您可以在**仓库管理** \> **定期任务** \> **清除 \> 取消工作**中访问“取消工作”功能。 在**取消工作**对话框中，指定要取消的工作的工作 ID，然后选择**确定**。

## <a name="warehouse-work-that-can-be-canceled"></a>可以取消的仓库工作

在仓库领料工序期间，工作人员可能会遇到这样的情况，即他们已经将从存储位置领取的数量登记到用户位置，但是他们无法登记放置操作。 仓库数据不一致通常是（但并非总是）造成工作被阻止的原因。

与可以使用工作标题上的**取消**按钮访问的常规“取消”功能不同，“取消工作”功能不需要最后完成的工作行是**放置**类型的工作行。 换言之，对于“取消工作”功能，即使工作行上的物料数量在用户位置，也可以运行取消逻辑。

> [!NOTE]
> 对于由于操作原因必须取消的工作，仓库用户必须继续使用工作页面上的常规“取消”功能。

使用“取消工作”功能只能取消**销售**、**转移发货**、**原材料领料**或**补货**类型的工作。 对于锁定的原材料领料工作或可以使用常规“取消”功能取消的工作，不会运行取消逻辑（请参见前面的说明）。

要取消阻止工作，系统会取消所有其余工作行并修复与用户指定的工作 ID 关联的仓库数据。 然后可以恢复涉及受影响物料数量的任何常规仓库处理操作。

要在取消工作后将受影响的物料放置在特定位置，用户必须在移动设备上使用库存变动或数量调整操作。
