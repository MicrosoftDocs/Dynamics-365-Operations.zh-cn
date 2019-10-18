---
title: 已计划执行
description: 本主题介绍资产管理中的已计划执行。
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
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
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8d9c8afc139c96e32efb3161d35fde685b8abcc5
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874662"
---
# <a name="scheduled-execution"></a>已计划执行

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

可使用工作订单服务级别设置已计划执行。 （有关工作订单服务级别的详细信息，请参阅[服务级别和描述](service-level-and-description.md)。）已计划执行可以在为维护工人计划工作时提高灵活性，因为可以为应完成工作订单的期间设置更详细或更通用的要求。 例如，可能可以让一个生产设施中完成作业的速度比预计快的维护工人继续处理附近另一个安排在本周，但不一定当天执行的作业。 这种方法可以优化工人规划和作业完成。

已计划执行的设置与工人有关，可以通用，也可以具体。 可以设置不限制到具体工作订单类型、资产类型等的通用行。 也可以创建应用于具体工作订单类型、资产类型、维护作业类型等的已计划执行行。

1. 选择**资产管理** \> **设置** \> **工作订单** \> **已计划执行**。
2. 选择**新建**以创建已计划执行行。
3. 在**功能位置**、**工作订单类型**、**资产类型**、**制造商**、**型号**、**维护作业类型类别**、**维护作业类型**、**维护作业变型**和**工种**字段中，根据需要选择值。
4. 在**服务级别**字段中，选择一个工作订单服务级别。 如果让此字段保留为空，则创建的是最通用的已计划执行类型。 有关通用行的示例，请参阅下图中的第一个记录。 该行启用未为其安排具体日期和时间的工作订单服务级别的所有工作订单。
5. 在**已计划执行**字段中，输入时间间隔。
6. 选择**保存**。

![图 1](media/20-setup-for-work-orders.png)