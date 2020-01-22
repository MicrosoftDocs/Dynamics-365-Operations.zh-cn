---
title: 在 Dynamics 365 - Core HR 中嵌入 Power Apps 应用程序
description: 此主题介绍如何解决 Microsoft Power Apps 菜单项从系统管理模块中消失的问题。
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b1dd1756be349d85af8e6d7159623a2a95e75526
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898704"
---
# <a name="embed-power-apps-apps-in-dynamics-365---core-hr"></a>在 Dynamics 365 - Core HR 中嵌入 Power Apps 应用程序

**发货**

**Power Apps** 菜单项从**系统管理**模块中消失。

**原因**

用户界面 (UI) 设计已更改，Microsoft Power Apps 现在包含在标准个性化模型中。

**解决方法**

Power Apps 的嵌入方式已更改。 Power Apps 现在通过个性化模型添加。 您可以将 Power Apps 添加到 Microsoft Dynamics 365 Talent 中的几乎所有页面。

有关如何在 Talent 中嵌入 Power Apps 的信息，请参阅[嵌入 Microsoft Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps)。

在更改前嵌入了应用程序的任何 Power Apps 客户应该已经升级到了新模型。

**Power Apps** 按钮在 Talent 中几乎每个页面的右上角。 您可以使用此按钮插入 Power Apps。

下面是一个示例。

1. 转到**人事管理 \> 链接 \> 工作人员 \> 员工**。
2. 选择 **Power Apps** 按钮，然后选择**插入 PowerApp**。

    ![Power Apps 按钮](media/png.png)

3. 填写**插入 PowerApp** 对话框中的字段。

    ![插入 PowerApp 对话框](media/insert-powerapp.png)

或者，执行以下步骤。

1. 在页面的操作窗格上，在**选项**选项卡上，在**个性化**组中，选择**个性化设置此窗体**。

    ![在“选项”选项卡上个性化设置组](media/options.png)

    个性化设置工具栏将显示。

2. 在工具栏上，选择**插入 \> PowerApp**。

    ![使用个性化设置工具栏插入 Power Apps 应用程序](media/powerapp-bar.png)
