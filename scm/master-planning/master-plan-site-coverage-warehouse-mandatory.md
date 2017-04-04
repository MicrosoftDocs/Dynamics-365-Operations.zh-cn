---
title: "涉及站点覆盖范围 (仓库的，必需的主计划"
description: "此主题介绍如何计划将站点作为覆盖范围维度的物料。 仓库是必填维度。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 4c595aa9809e37ba752b76f559ef909c071eb303
ms.lasthandoff: 03/31/2017


---

# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a>涉及站点覆盖范围 (仓库的，必需的主计划

此主题介绍如何计划将站点作为覆盖范围维度的物料。 仓库是必填维度。

此主计划方案涉及以下情况：

-   站点维度设置为必填，必须在需求交易记录上输入。 不能修改此设置。
-   仓库维度设置为必填，必须在需求交易记录上输入。
-   为覆盖范围计划设置站点维度。 还可能为覆盖范围计划设置其他维度。 但是，它们不受多站点功能的影响。
-   不为覆盖范围计划设置仓库维度。 因此，按站点和还可能按其他覆盖范围计划维度聚合供应和需求。

下图说明如何继续主计划。 图中引用的参数及其位置如下所示：
-   为物料定义物料覆盖范围。 **单击产品信息管理 &gt; 产品&gt; 发放**产品。 选择某个项目，然后单击** **请计划 &gt; 物料覆盖范围。
-   为仓库定义重填关系。 **单击"库存 &gt; 管理设置 &gt; 库存仓库**细分 &gt;。 在**主计划**选项卡上，查看**主仓库**字段组。
-   默认订单类型设置为“生产”、“采购订单”或“看板”。 **单击产品信息管理 &gt; 产品&gt; 发放**产品。 选择某个项目，然后单击**请计划 &gt; **默认订单设置。 在**“默认订单设置”**窗体中，查看**“默认订单类型”**。

![站点需求（覆盖范围仓库必需）](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



<a name="see-also"></a>请参阅
--------

[Master planning and multisite functionality](master-plan-multisite-functionality.md)

[主计划 - 站点和仓库覆盖范围，仓库是必需的](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[主计划-站点覆盖范围。必需的仓库] (主计划涉及站点覆盖范围 (仓库 mandatory.md)

[主计划 - 站点和仓库覆盖范围，仓库不是必需的](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[主计划 - 如何确定物料清单版本](master-plan-bom-version-determined.md)


