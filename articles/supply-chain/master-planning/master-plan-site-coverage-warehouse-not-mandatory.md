---
title: 站点覆盖范围的主计划，仓库非必需
description: 此主题介绍如何计划为覆盖范围设置站点维度的物料。
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f4cde5c570148ca58c4ea583a8f538a72d4957d
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2020
ms.locfileid: "3987038"
---
# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a>站点覆盖范围的主计划，仓库非必需

[!include [banner](../includes/banner.md)]

此主题介绍如何计划为覆盖范围设置站点维度的物料。

此主计划方案涉及以下情况：

-   站点维度设置为必填，必须在需求交易记录上输入。
-   仓库维度未设置为必填的。 仓库可能已知，但是它不在主计划计算中使用。
-   为覆盖范围计划设置站点维度。
-   不为覆盖范围计划设置仓库维度。 因此，按站点和还可能按其他覆盖范围计划维度聚合供应和需求。

下图说明如何继续主计划。 图中引用的参数及其位置如下所示：
-   为物料定义物料覆盖范围。 单击**产品信息管理 &gt; 产品 &gt; 已发布产品**。 选择物料，然后单击**计划 &gt; 物料覆盖范围**。
-   为仓库定义重填关系。 单击**库存管理 &gt; 设置 &gt; 库存细分 &gt; 仓库**。 在**主计划**选项卡上，查看**主仓库**字段组。
-   默认订单类型设置为“生产”、“采购订单”或“看板”。 单击**产品信息管理 &gt; 产品 &gt; 已发布产品**。 选择物料，然后依次单击**计划 &gt; 默认订单设置**。 在**默认订单设置**窗体中，查看**默认订单类型**字段。

![站点需求（覆盖范围仓库非必需）](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a>其他资源
--------

[主计划和多站点功能概览](master-plan-multisite-functionality.md)

[站点和仓库覆盖范围的主计划（仓库必需）](master-plan-site-coverage-warehouse-mandatory.md)

[站点覆盖范围的主计划（仓库必需）](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[站点覆盖范围的主计划（仓库非必需）](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[确定物料清单版本](master-plan-bom-version-determined.md)



