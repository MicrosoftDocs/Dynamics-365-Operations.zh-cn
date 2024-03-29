---
title: 手动更新资产计数器
description: 本文介绍如何在资产管理中手动更新资产计数器。
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetCounter
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 30c672286c16a4353556a507019960edb93f8b1b
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016585"
---
# <a name="manual-update-of-asset-counters"></a>手动更新资产计数器

[!include [banner](../../includes/banner.md)]



计数器用于在资产上创建登记，如有关资产已运行小时数或已生产数量的登记。

可以将为计数器选择的计数器类型设置为继承计数器值。 换言之，在 **计数器** 页面的 **常规** 快速选项卡上，**继承资产计数器值** 选项设置为 **是**（**资产管理** > **设置** > **资产类型** > **计数器**）。 在这种情况下，当您创建该类型的新计数器行时，使用相同计数器类型的每个子资产都会自动更新。

在 **所有资产** 页面上，将根据资产的读数为资产创建工时或数量计数器登记。

1. 选择 **资产管理** > **资产** > **所有资产**。

2. 选择资产，然后在“操作窗格”上，在 **资产** 选项卡上的 **预防** 组中，选择 **计数器**。 **资产计数器** 页面显示所选资产之前进行的全部计数器登记的列表。

3. 选择 **新建** 以创建登记。 将在 **资产** 字段中自动输入资产 ID。

4. 在 **计数器** 字段中选择相关计数器。 只有与为资产选择的资产类型关联的计数器可供选择。 将在 **单位** 字段中自动输入关联的单位。

5. 在 **已登记** 字段中，为计数器登记选择日期和时间。

6. 在 **值** 字段中，输入自上次计数器登记以来的数量。 或者，在 **汇总值** 字段中，输入总计数量。

请注意以下点：

- 如果以物理方式为资产安装新的计数器，则必须在 **资产计数器** 页面登记资产的更改。 接下来，您必须创建两个具有相同时间戳的登记行。 第一行必须是要替换的计数器。 在与新计数器相关的行上，选中 **计数器重置** 复选框。 **总计** 字段中的计数总数是为该计数器类型登记的所有值的计数器总计之和。

- 如果为使用其间隔类型为“从... 开始”或“到达...”的维护计划的资产选中 **计数器重置** 复选框，该计数器对新计数器行仍然有效，因为您创建的是单独的计数器行，并且是从新计数器重新开始。

下图显示了 **资产计数器** 页面的示例。

![图 1.](media/11-work-orders.png)

在 **资产计数器** 页面上（**资产管理** > **查询** > **资产** > **资产计数器**），您可以根据需要同时对多个资产进行计数器登记。

>[!NOTE]
>您可以设置范围来定义手动计数器登记的偏差。 如果登记超出定义的范围，您还可以指定显示的消息类型。 有关如何设置计数器的详细信息，请参阅[计数器](../setup-for-objects/counters.md)。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]