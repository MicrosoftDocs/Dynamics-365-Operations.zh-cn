---
title: 工作订单和固定资产
description: 本主题介绍资产管理中的工作订单和固定资产。
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ca7a5d88de4308d7be9c1bc749b9dbf1da027c2c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423207"
---
# <a name="work-orders-and-fixed-assets"></a>工作订单和固定资产

[!include [banner](../../includes/banner.md)]


在资产管理中，可将资产与固定资产关联，还可以为这些资产创建工作订单。 如果使用此功能，则可在 Microsoft Dynamics 365 for Finance and Operations 的 **项目管理与核算** 和 **固定资产** 模块中获取在投资项目中登记的固定资产、关联的投资项目和成本的完整概览。

>[!NOTE]
>仅当选择 **投资** 作为工作订单作业项目的项目类型时，才会设置工作订单作业项目的 **固定资产编号** 字段。

下图显示 **项目管理与核算** 模块中的投资项目与工作订单作业项目之间的关系。

![图 1](media/24-work-orders.png)

以下过程介绍资产、工作订单、工作订单作业项目和固定资产之间的关系。

1. 您将创建与固定资产相关的资产。

![图 2](media/25-work-orders.png)

2. 在 **工作订单类型** 页面设置工作订单类型（**资产管理** > **设置** > **工作订单** > **工作订单类型**）时，将创建工作订单类型来处理投资。 另请参阅[工作订单类型](../setup-for-work-orders/work-order-types.md)。

![图 3](media/26-work-orders.png)

3. 在 **工作订单项目设置** 页面的 **项目组** 选项卡上设置工作订单项目组（**资产管理** > **设置** > **工作订单** > **项目设置**）时，将在 **项目管理与核算** 模块中 **项目组** 页面上在用于投资的工作订单类型与为投资创建的项目组之间创建关系（**项目管理与核算** > **设置** > **过帐** > **项目组**）。

![图 4](media/27-work-orders.png)

4. 创建与固定资产项目关联的工作订单时，请选择用于处理投资的工作订单类型，如 **投资**。

5. 创建工作订单之后，将在 **所有工作订单** 页面显示关联的工作订单类型。

![图 5](media/28-work-orders.png)

6. 创建工作订单后，将在 **项目管理与核算** 模块中的 **所有项目** 页面创建与工作订单关联的项目（**项目管理与核算** > **项目** > **所有项目**）。 要查看与项目相关的信息，请在 **资产管理** 模块中 **所有工作订单** 页面的详细信息视图中，在 **行明细** 快速选项卡上的 **常规** 选项卡上，在 **项目 ID** 字段中选择链接（**资产管理** > **公用** > **工作订单** > **所有工作订单**）。

![图 6](media/29-work-orders.png)

7. 要查看与固定资产关联的项目的概览，请选择 **固定资产** > **固定资产** > **固定资产**，然后在 **固定资产编号** 字段中，选择固定资产的链接打开详细信息视图。 展开页面右侧的 **相关信息** 窗格，然后选择 **关联项目** 快速选项卡。

