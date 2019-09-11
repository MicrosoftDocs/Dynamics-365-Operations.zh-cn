---
title: 维护工人日历和排产
description: 本主题介绍资产管理中与排产有关的维护工人。
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3f86f6475e5226443f5e4d43fb91acafe2afdbb9
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887380"
---
# <a name="maintenance-worker-calendar-and-scheduling"></a><span data-ttu-id="43955-103">维护工人日历和排产</span><span class="sxs-lookup"><span data-stu-id="43955-103">Maintenance worker calendar and scheduling</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="43955-104">为工作订单排产时，请为维护工人、工具和资产创建计划。</span><span class="sxs-lookup"><span data-stu-id="43955-104">When you schedule work orders, you create a schedule for maintenance workers, tools, and assets.</span></span> <span data-ttu-id="43955-105">必须为每位维护工人设置日历，才能对维护工人执行排产。</span><span class="sxs-lookup"><span data-stu-id="43955-105">In order to carry out scheduling on maintenance workers, a calendar must be set up for each maintenance worker.</span></span> <span data-ttu-id="43955-106">将把维护工人与资源关联，并为资源设置工作时间日历。</span><span class="sxs-lookup"><span data-stu-id="43955-106">Maintenance workers are related to a resource, and working time calendars are set up on resoures.</span></span> <span data-ttu-id="43955-107">在**资产管理** > **设置** > **工人** > **工人**中设置与工人关联的资源和日历，[维护工人和工人组](../setup-for-objects/workers-and-worker-groups.md)中对此进行了介绍。</span><span class="sxs-lookup"><span data-stu-id="43955-107">You set up the resource and calendar related to a worker in **Asset management** > **Setup** > **Workers** > **Workers**, which is described in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).</span></span>

<span data-ttu-id="43955-108">下面的屏幕截图显示与使用工作时间日历“生产”的资源关联的维护工人的示例。</span><span class="sxs-lookup"><span data-stu-id="43955-108">The screenshot below shows an example of a maintenance worker who is related to a resource that uses the working time calendar "Production".</span></span>

![图 1](media/01-work-order-scheduling.png)

<span data-ttu-id="43955-110">与工作订单排产关联时，不需要为工具和资产设置日历。</span><span class="sxs-lookup"><span data-stu-id="43955-110">Calendar setup for tools and assets is not needed in relation to work order scheduling.</span></span> <span data-ttu-id="43955-111">假设工具和资产全天候可用，以便进行维护。</span><span class="sxs-lookup"><span data-stu-id="43955-111">The assumption is that tools and assets are available 24 hours a day for maintenance.</span></span>

