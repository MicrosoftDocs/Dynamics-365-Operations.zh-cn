---
title: 手动更新资产计数器
description: 本主题介绍如何在资产管理中手动更新资产计数器。
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1e7c5ec288404c18b00f9dcd0e66f50744d0aa2f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875527"
---
# <a name="manual-update-of-asset-counters"></a>手动更新资产计数器

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


计数器用于创建与资产有关的登记，例如，运行小时数或生产数量数。

如果为计数器选择的计数器类型设置为继承计数器值（**资产管理** > **设置** > **资产类型** > **计数器** > **常规**快速选项卡 > **继承资产计数器值**切换按钮设置为“是”），则当您新建该类型的计数器行时，将自动更新使用同一个计数器类型的所有子资产。

在**所有资产**中，将根据资产的读数为资产创建工时或数量计数器登记。

1. 单击**资产管理** > **常用** > **资产** > **所有资产**。

2. 在列表中选择资产，然后单击**计数器**。 在**资产计数器**窗体中，可以查看所选资产的之前全部计数器登记的列表。

3. 单击**新建**以创建新的登记。 将自动插入资产 ID。

4. 在**计数器**字段中选择相关计数器。 只有与为资产选择的资产类型关联的计数器才可用。 将在**单位**字段中自动插入关联的单位。

5. 为计数器登记选择日期和时间。

6. 在**值**字段中，插入上一个计数器登记后的数字，或者在**汇总值**字段中插入计数总数。

- 如果以物理方式为资产安装新的计数器，则需要在**资产计数器**中登记资产的更改。 接下来，必须创建两个具有相同时间戳的登记行，然后在与新计数器有关的行中，选中**计数器重置**复选框。 创建这两个登记行时，第一行必须针对要替换的计数器。 **总计**字段中的计数总数是为该计数器类型登记的所有值的计数器总计之和。  
- 如果为使用其间隔类型为“从... 开始”或“到达...”的维护计划的资产选中**计数器重置**复选框，该计数器对新计数器行仍然有效，因为您创建的是单独的计数器行，并且是从新计数器重新开始。

![图 1](media/11-work-orders.png)


如果要为多个资产创建计数器登记，可以在**资产管理** > **查询** > **资产** > **资产计数器**中进行。

>[!NOTE]
>可以设置范围来定义手动计数器登记中的偏差，以及登记超出定义的范围时应该显示的消息类型。 有关设置计数器的信息，请参阅[计数器](../setup-for-objects/counters.md)主题。
