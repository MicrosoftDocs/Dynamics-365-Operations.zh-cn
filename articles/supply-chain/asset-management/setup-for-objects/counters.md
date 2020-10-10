---
title: 资产度量
description: 本主题介绍如何在资产管理中创建资产度量类型。
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectCounterPart, EntAssetObjectCounterLookup, EntAssetCounterType, EntAssetObjectCounterTotals
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: adadb1df7b41488fad496f937ecbc24e0761e42d
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889761"
---
# <a name="counters"></a>计数器

[!include [banner](../../includes/banner.md)]

本主题介绍如何在资产管理中创建计数器类型。 计数器类型用于创建资产的计数器登记，如有关资产的生产工时数或生产数量。 资产类型与计数器类型关联。 这表示如果为资产使用的资产类型设置了计数器，则该计数器只能用于这个资产。

创建资产的计数器登记时，请首先在**计数器**中创建要使用的计数器类型。 然后，在**计数器**中创建资产的计数器登记。 

可以在维护计划中使用计数器。 维护计划行的类型可以为“计数器”，例如，与生产工时数或生产数量有关。 

可以根据生产工或生产的数量手动或自动更新计数器登记。 可设置计数器以使用三种更新方法之一（在**计数器**中**更新**字段内所选）：
  
- 手动 - 必须手动登记计数器值。  
- 生产工时 - 根据生产工时数自动更新计数器。  
- 生产数量 - 根据生产数量自动更新计数器。  

>[!NOTE]
>如果使用生产数量，则计数器登记中包含*所有*已登记物料、良品数量，以及错误数量。 如果需要，始终可以手动登记计数器。

## <a name="create-counter-types-for-asset-counter-registrations"></a>为资产计数器登记创建计数器类型

1. 选择**资产管理** > **设置** > **资产类型** > **计数器**。
2. 选择**新建**以创建新计数器类型。
3. 在**计数器**字段中插入 ID，在**名称**字段中插入计数器名称。
4. 在**常规**快速选项卡上的**单位**字段中选择计数器单位。
5. 在**更新**字段中，选择要用于计数器的更新方法。
6. 如果资产结构中的子资产应该自动继承为父资产创建的计数器登记，请在**继承计数器值**切换按钮上选择“是”。
7. 在**聚合总计**字段中，选择要用于使用此计数器类型的计数器的汇总方法。 “求和”是用于将登记的值连续相加到总和值中的标准选择。 如果设置计数器以监视阈值（如资产的相关温度、振动或磨损），可使用“平均值”。 
8. 在**偏差上限**字段中，插入以百分比表示的上限，以便验证手动计数器登记是否未超过预期范围。 此项验证基于现有计数器登记中的线性增加。
9. 在**偏差下限**字段中，插入以百分比表示的下限，以便验证手动计数器登记是否未超过预期范围。 此项验证基于现有计数器登记中的线性减少。
10. 在**类型**字段中，选择如果偏差超出在创建手动计数器登记时定义的范围，要显示的消息类型（参考、警告、错误）。
11. 在**资产类型**快速选项卡上，添加应该可以使用计数器的资产类型。
12. 在**关联的资产计数器**快速选项卡上，添加当更新此计数器时要自动更新的计数器。


>[!NOTE]
>仅当关联的计数器具有在计数器设置中与其关联的资产类型，才会自动更新此计数器。 例如：为“生产工时”设置计数器，并添加资产类型“卡车引擎”。 更新该计数器时，也将使用相同的计数器值更新关联的计数器“燃油”。 **计数器**中的设置包含“工时”的设置。 此外，在“燃油”计数器中，应该将资产类型“卡车引擎”添加到**资产类型**快速选项卡上，以确保计数器关联。 有关“工时”和“燃油”计数器的设置示例，请参见下面的屏幕截图。

在**计数器**中向计数器类型添加资产类型时，将把该计数器自动添加到[资产类型](../setup-for-objects/object-types.md)中**计数器**快速选项卡上的资产类型。

![图 1](media/071-setup-for-objects.png)

