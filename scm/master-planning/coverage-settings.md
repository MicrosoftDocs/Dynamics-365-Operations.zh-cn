---
title: "覆盖范围设置"
description: "主计划编制使用覆盖范围设置计算物料需求。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: b42f0515823bd42ec260aa1d175855a923162b62
ms.contentlocale: zh-cn
ms.lasthandoff: 05/25/2017

---

# <a name="coverage-settings"></a>覆盖范围设置

[!include[banner](../includes/banner.md)]


主计划编制使用覆盖范围设置计算物料需求。 

您可以通过以下几种方式指定覆盖范围设置：

-   为覆盖范围组指定覆盖范围设置。 您可以创建一个覆盖范围组，它包含与该组关联的所有产品的设置。 单击**主计划 &gt; 设置 &gt; 覆盖范围 &gt; 覆盖范围组**以创建覆盖范围组。 您可以将覆盖范围组与某个产品链接。 如果链接特定于站点、仓库或产品维度，请使用**物料覆盖范围**页的**覆盖范围组**字段。 如果链接是通用的，无论产品维度如何，请使用**产品详细信息**页中**计划**快速选项卡上的**覆盖范围组**。 如果您没有将某一覆盖范围组与某一产品关联，则主计划将使用在**主计划参数**页中指定的**一般覆盖范围组**作为默认覆盖范围组。

-   为产品指定覆盖范围设置。 您可为特定产品创建覆盖范围设置。 单击**产品信息管理 &gt; 产品 &gt; 已发布产品**。 选择产品，在**操作窗格**上的**计划**选项卡中**覆盖范围组**中，单击**物料覆盖范围**打开**物料覆盖范围**页。 如果该产品已链接到某一覆盖范围组，则您可以使用**覆盖**字段覆盖该覆盖范围组设置。 **物料覆盖范围**页上的覆盖范围设置优先于**覆盖范围组**页上的设置。

<!-- -->

-   使用向导为产品指定覆盖范围设置。 该向导为设置主物料覆盖范围参数提供分步指导。 在**物料覆盖范围**页上，单击**向导**打开**物料覆盖范围向导**。

<!-- -->

-   为维度组指定覆盖范围设置。 单击**产品信息管理 &gt; 通用 &gt; 已发布产品**。 在 **已发布产品详细信息** 页上，在**常规**选项卡上，在**管理**组中，单击**存储维度组**链接。 在**存储维度组**页，选择**按维度的覆盖范围计划**字段为存储维度组中的维度创建覆盖范围设置。 所有产品维度，例如配置、颜色、尺寸、样式，必须选择**按维度的覆盖范围计划**字段。



<a name="see-also"></a>请参阅
--------

[主计划](master-plans.md)




