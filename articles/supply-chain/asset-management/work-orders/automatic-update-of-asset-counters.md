---
title: 自动更新资产计数器
description: 本主题介绍如何在资产管理中自动更新资产计数器。
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
ms.openlocfilehash: 97e6912cd37d6f82d8bf022141f04645a3364ee1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875532"
---
# <a name="automatic-update-of-asset-counters"></a>自动更新资产计数器

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

上一部分中介绍了手动登记资产计数器。 [计数器](../setup-for-objects/counters.md)中介绍了设置资产计数器。

也可以根据生产工时或生产数量自动从生产登记更新计数器值。 这在**更新资产计数器**中执行。 可以通过插入**开始日期**参数更新一个或多个资产。 此参数指定生产登记（工时数或生产数量）的开始日期，即应开始更新计数器值的日期。

自动更新中将包括与资源关联*且*具有（为了基于生产的数量或生产工时进行更新而设置的）资产计数器的所有资产，并且将创建新的计数器值。

计数中将包括基于登记的生产数量、良品数量和错误数量的相关计数器。 如果用于生产数量登记的单位不是计数器使用的单位，将转换数量，以便与计数器单位一致。

正如上面的介绍，可以从生产登记更新自动计数器。 因此，必须将要自动更新其计数器的资产与资源（机器）关联。 下面的说明提供有关设置和处理生产订单（在**生产控制**模块中）的概览，而此类设置和处理则是在**资产管理**模块中自动更新资产的计数器的基础。

为资源登记生产数量或生产工时之后，可更新关联的资产计数器。

1. 单击**资产管理** > **定期** > **资产** > **更新资产计数器**。

2. 在**开始日期**字段中选择自动更新的开始日期。

>[!NOTE]
>此字段中的日期是来自**工艺路线交易记录**（**生产控制** > **查询和报表** > **生产** > **工艺路线交易记录** > **实际日期**字段）的“在制品”日期。

3. 如果要选择特定资产、资产类型或资源以进行自动更新，请单击**要包括的记录**快速选项卡上的**筛选**，然后进行相关选择。

4. 如果需要，可以在**在后台运行**快速选项卡上将自动更新设置为批处理作业。

![图 1](media/12-work-orders.png)

5. 单击 **确定**。 完成了资产计数器自动更新之后，可以在**资产计数器**（**资产管理** > **常用** > **资产** > **所有资产** > 选择资产 > **计数器**按钮）中查看与资产关联的计数器登记。

在**资产计数器总计**中，可获取为所有资产的所有计数器类型创建的最新登记的概览。 单击**资产管理** > **查询** > **资产** > **资产汇总值**。 该值类似**资产计数器**，但是您不能在**资产汇总值**中添加或编辑登记。 它仅供概览。

![图 2](media/13-work-orders.png)


- 您仍然可以为自动更新的计数器类型手动创建计数器值登记。 有关详细信息，请参阅“手动更新资产计数器”。
- 可设置与其他计数器关联的计数器，这意味着更新计数器时，同时将自动更新关联的计数器。 有关设置关联的计数器，请参阅[计数器](../setup-for-objects/counters.md)。
