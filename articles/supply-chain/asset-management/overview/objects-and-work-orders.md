---
title: 资产和工作订单
description: 本主题介绍资产管理中的资产和工作订单。
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5bd55988578be2b0287b399549f17642bfb1693b
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783092"
---
# <a name="assets-and-work-orders"></a>资产和工作订单

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

本主题介绍资产管理中的资产和工作订单。 资产和工作订单是资产管理的最重要部分。 *资产*是需要持续维护和服务的机器或机器部件。 可以按分层结构创建资产，还可以将其与功能位置关联。 可以在资产结构的所有级别计划维护作业。

可以为每个资产设置各种数据，如产品信息和资产规格，以及必需的维护计划。 下图显示资产数据和资产与作业类型之间的隶属关系的概览。 红色文本用于的示例显示继承关系和依赖关系。

![图 1](media/05-overview-image.png)

每个工作订单都有工作订单类型，如预防性维护、修复性维护或检验。 工作订单中包含一个或多个工作订单作业。 每个工作订单作业定义必须对资产执行的作业和关联的作业类型。 关联作业类型的示例包括 10,000 公里、50,000 公里、1 年检修和安全检验。 可以将一个工作订单与多个资产关联。

下图显示工作订单中的关键数据的概览。

![图 2](media/06-overview-image.png)

可以将一个工作订单与另一个工作订单关联，而作业类型中可以包含连续作业，用于创建工作订单。 工作订单之间通常不存在依赖关系。 因此，可以彼此独立地更改其工作订单生命周期状态和为其排产。

可以通过多种方法创建与修复性、预防性或反应性维护关联的工作订单。 也可以手动创建工作订单。 下图显示自动或手动创建工作订单的过程概览。

![图 3](media/07-overview-image.png)

如果希望为工作订单计划和运行维护作业，则必须完成多个步骤。 下图显示工作订单的处理的概览。

![图 4](media/08-overview-image.png)

> [!NOTE]
> 在 Microsoft Dynamics 365 for Finance and Operations 和**资产管理**模块中工作时，通常选择**新建**来创建新记录，选择**编辑**来更新现有记录，以及选择**保存**来保存新数据或编辑后的数据。