---
title: 自动更新资产计数器
description: 本主题介绍如何在资产管理中自动更新资产计数器。
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
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
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 005b04bd4c3476356f30ba8e97564f83307a64c7
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811730"
---
# <a name="automatic-update-of-asset-counters"></a>自动更新资产计数器

[!include [banner](../../includes/banner.md)]

有关手动登记资产计数器的信息，请参阅[手动更新资产计数器](../work-orders/manual-update-of-asset-counters.md)。 有关如何设置资产计数器的信息，请参阅[计数器](../setup-for-objects/counters.md)。

也可以根据生产工时或生产数量（即生产的数量）自动从生产登记更新计数器值。 此更新在**更新资产计数器**页面上完成。 可以通过设置**开始日期**参数更新一个或多个资产。 此参数指定生产登记的开始日期（生产工时或生产数量）。 换言之，它指定应该更新计数器值的日期。

自动更新中将包括与资源关联*且*具有（为了基于生产工时或生产数量进行更新而设置的）资产计数器的所有资产。 新的计数器值将创建。

对于基于生产数量的计数器，计数包括已登记的完好数量和残次数量。 如果用于生产数量登记的单位与用于计数器的单位不同，将转换数量，以便其与计数器单位一致。

正如上面的介绍，可以从生产登记更新自动计数器。 因此，必须将要自动更新其计数器的资产与资源（机器）关联。 为资源登记生产数量或生产工时之后，可更新关联的资产计数器。

1. 选择**资产管理** > **定期** > **资产** > **更新资产计数器**。

2. 在**开始日期**字段中，选择自动更新的开始日期。

    >[!NOTE]
    >此字段中的日期是来自**工艺路线交易记录**（**生产控制** > **查询和报表** > **生产** > **工艺路线交易记录** > **实际日期**字段）的“在制品”日期。

3. 在**要包括的记录**快速选项卡上，您可以选择特定资产、资产类型或资源来进行自动更新。 选择**筛选器**，然后进行相关选择。

4. 在**在后台运行**快速选项卡上，可根据需要将自动更新设置为批处理作业。

    下图显示了**更新资产计数器**对话框的示例。

    ![图 1](media/12-work-orders.png)

5. 选择**确定**。 

自动资产计数器更新完成后，您可以在**资产计数器**页面上查看与资产相关的计数器登记。 选择**资产管理** > **通用** > **资产** > **所有资产**，选择资产，然后在操作窗格上的**资产**选项卡上，在**预防**组中，选择**计数器**。

在**资产汇总值**页面，可获取已为所有资产的所有计数器类型创建的最新登记的概览。 选择**资产管理** > **查询** > **资产** > **资产汇总值**。 此页面类似于**资产计数器**页面，但是您无法添加或编辑登记。 它仅供概览。

下图显示了**资产汇总值**页面的示例。

![图 2](media/13-work-orders.png)

请注意以下点：

- 您仍然可以为自动更新的计数器类型手动创建计数器值登记。 有关详细信息，请参阅[手动更新资产计数器](../work-orders/manual-update-of-asset-counters.md)。

- 您可以设置与另一个计数器相关的计数器。 这样，当更新计数器时，相关的计数器会同时自动更新。 有关如何设置相关计数器的详细信息，请参阅[计数器](../setup-for-objects/counters.md)。

