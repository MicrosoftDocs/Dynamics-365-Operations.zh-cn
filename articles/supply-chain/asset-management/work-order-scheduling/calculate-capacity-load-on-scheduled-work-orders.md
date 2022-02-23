---
title: 对计划的工作订单计算产能负荷
description: 本主题介绍如何在资产管理中对计划的工作订单计算产能负荷。
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7b7e4a20ed56b1eac29d16d527693d6e455cdc37
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021646"
---
# <a name="calculate-capacity-load-on-scheduled-work-orders"></a>对计划的工作订单计算产能负荷

[!include [banner](../../includes/banner.md)]

 

可以对计划的工作订单计算产能负荷，以便获取资源在特定期间的工作负荷。 可以对以下资源进行计算：维护工人、工人组、工具和资产。

1. 单击 **资产管理** > **查询** > **计划** > **产能负荷**。

2. 在 **计算产能负荷** 对话框 > **显示** 字段中，选择要计算的负荷类型：**产能**、**预留** 或 **余额**。

3. 如果不希望显示包含零的结果，请在 **忽略零** 切换按钮上选择 **是**。

4. 通过在相关切换按钮上选择 **是**，选择要为其计算产能负荷的资源类型：**工人**、**维护工人组**、**工具** 和 **资产**。

5. 在 **开始日期** 字段中选择计算的开始日期。

6. 在 **间隔类型** 字段中，选择计算的间隔：**天**、**周**、**月** 或 **季度**。

7. 在 **期间频率** 字段中，插入要计算的间隔的数量。 例如，如果选择的间隔类型为 **天**，并且在此字段中输入数字“5”，将从开始日期之后五天进行计算。

8. 单击 **确定** 开始计算。

下图显示的计算结果涵盖三天的负荷类型 **预留**。

![图 1](media/08-work-order-scheduling.png)

[!NOTE]
如果为计算选择 **产能** 或 **余额**，并且在所选期间没有为资源进行预留，将显示相同的结果。

有关如何对维护安排行，而不是计划的工作订单计算产能负荷的信息，请参阅[计算产能负荷](../capacity-planning/calculate-capacity-load.md)。

