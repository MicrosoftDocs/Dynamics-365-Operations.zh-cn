---
title: 工作订单和固定资产
description: 本主题介绍资产管理中的工作订单和固定资产。
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
ms.openlocfilehash: f03b7fa073c4e5338b7b5681ba7b8c9fe00a657b
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875519"
---
# <a name="work-orders-and-fixed-assets"></a>工作订单和固定资产


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


在资产管理中，可将资产与固定资产关联，还可以为这些资产创建工作订单。 如果使用此功能，则可在 Dynamics 365 for Finance and Operations 的**项目管理与核算**模块和**固定资产**模块中获取固定资产、关联的投资项目和为投资项目登记的所有成本的完整概览。

>[!NOTE]
>仅当选择类型“投资”作为工作订单作业项目的项目类型时，才会填写工作订单作业项目的**固定资产编号**字段。

![图 1](media/24-work-orders.png)

以下过程介绍资产、工作订单、工作订单作业项目和固定资产之间的关系。

1. 创建与固定资产关联的资产，如下图中所示。

![图 2](media/25-work-orders.png)

2. 设置工作订单类型（**资产管理** > **设置** > **工作订单** > **工作订单类型**）时，将创建工作订单类型来处理投资。 另请参阅[工作订单类型](../setup-for-work-orders/work-order-types.md)。

![图 3](media/26-work-orders.png)

3. 设置工作订单项目组（**资产管理** > **设置** > **工作订单** > **项目设置** > **项目组**链接）时，将在**项目管理与核算**模块中创建用于投资的工作订单类型与为投资创建的项目组（**项目管理与核算** > **设置** > **过帐** > **项目组**）之间的关联。

![图 4](media/27-work-orders.png)

4. 创建与固定资产项目关联的工作订单时，请选择用于处理投资的工作订单类型，如“投资”。

5. 创建工作订单之后，将在**所有工作订单**中显示关联的工作订单类型。

![图 5](media/28-work-orders.png)

6. 创建工作订单时，将在**项目管理与核算** > **所有项目**中创建与该工作订单关联的项目。 可查看与项目有关的信息，方法是单击工作订单的**项目 ID** 链接（在**资产管理**的“详细信息视图”中打开工作订单 > **行详细信息**快速选项卡 > **常规**选项卡 > **项目 ID** 字段）。

![图 6](media/29-work-orders.png)

7. 在**固定资产**中，可查看与固定资产关联的项目的概览（**固定资产** > **固定资产** > **固定资产** > 在**固定资产编号**字段中单击固定资产 > 查看**相关信息**窗格 > **关联的项目**部分中的内容）。

