---
title: Core HR 中的嵌入 PowerApps 应用
description: 此主题介绍如何解决 PowerApps 菜单项从系统管理模块中消失的问题。
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
ms.openlocfilehash: e3b20e1d0a873c32b8f6f5e28f786febf62db355
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517476"
---
# <a name="embed-powerapps-apps-in-core-hr"></a>Core HR 中的嵌入 PowerApps 应用

[!include [banner](includes/banner.md)]

**发货**

**PowerApps** 菜单项从**系统管理**模块中消失。

**原因**

用户界面 (UI) 设计已更改，Microsoft PowerApps 现在包含在标准个性化模型中。

**分辨率**

PowerApps 应用的嵌入方式已更改。 PowerApps 应用现在通过个性化模型添加。 您可以将 PowerApps 应用添加到 Microsoft Dynamics 365 for Talent 中的几乎所有页面。

有关如何在 Talent 中嵌入 PowerApps 应用的信息，请参阅[嵌入 PowerApps 应用](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps)。

在更改前嵌入了应用的任何 PowerApps 客户应该已经升级到了新模型。

**PowerApps** 按钮在 Talent 中几乎每个页面的右上角。 您可以使用此按钮插入 PowerApps 应用。

下面是一个示例。

1. 转到**人事管理 \> 链接 \> 工作人员 \> 员工**。
2. 选择 **PowerApps** 按钮，然后选择**插入 PowerApp**。

    ![PowerApps 按钮](media/png.png)

3. 填写**插入 PowerApp** 对话框中的字段。

    ![插入 PowerApp 对话框](media/insert-powerapp.png)

或者，执行以下步骤。

1. 在页面的操作窗格上，在**选项**选项卡上，在**个性化**组中，选择**个性化设置此窗体**。

    ![在“选项”选项卡上个性化设置组](media/options.png)

    个性化设置工具栏将显示。

2. 在工具栏上，选择**插入 \> PowerApp**。

    ![使用个性化设置工具栏插入 PowerApps 应用](media/powerapp-bar.png)
