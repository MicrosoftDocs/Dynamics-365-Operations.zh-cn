---
title: "站点和仓库覆盖范围主计划，仓库不是必需的"
description: "此主题介绍如何计划将站点和仓库作为覆盖范围维度的物料。 仓库维度不是必填的。"
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9c7b13a7a018ce584c877fed6212abc3c2913903
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a>站点和仓库覆盖范围主计划，仓库不是必需的

[!include[banner](../includes/banner.md)]


此主题介绍如何计划将站点和仓库作为覆盖范围维度的物料。 仓库维度不是必填的。

此主计划方案涉及以下情况：

-   站点维度设置为必填，必须在需求交易记录上输入。 不能修改此设置。
-   仓库维度未设置为必填的。 仓库可能已知，但是它不在主计划计算中使用。
-   为覆盖范围计划设置站点和仓库维度。 还可能为覆盖范围计划设置其他维度。 但是，它们不受多站点功能的影响。

下图说明如何继续主计划。 图中引用的参数及其位置如下所示：
-   仓库设置为“手动”。 单击**库存管理 &gt; 设置 &gt; 库存细分 &gt; 仓库**。 在**“主计划”**快速选项卡上，查看**“手动”**字段。
-   为物料定义物料覆盖范围。 单击**产品信息管理 &gt; 产品 &gt; 已发布产品**。 选择该物料，然后在“操作窗格”上，在**计划**选项卡上单击**物料覆盖范围**。
-   为仓库定义重填关系。 单击**库存管理 &gt; 设置 &gt; 库存细分 &gt; 仓库**。 在**“主计划”**快速选项卡上，查看**“主仓库”**字段组。
-   默认订单类型设置为“生产”、“采购订单”或“看板”。 单击**产品信息管理 &gt; 产品 &gt; 已发布产品**。 选择该物料，然后在“操作窗格”上，在**计划**选项卡上单击**默认订单设置**。 在**“默认订单设置”**窗体中，查看**“默认订单类型”**。

![站点和仓库需求（仓库非必需）](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)

 
-



<a name="see-also"></a>请参阅
--------

[主计划和多站点功能](master-plan-multisite-functionality.md)

[主计划 - 站点和仓库覆盖范围，仓库是必需的](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[主计划 - 站点覆盖范围，仓库是必需的](master-plan-site-coverage-warehouse-mandatory.md)

[主计划 - 站点覆盖范围，仓库非必需](master-plan-site-coverage-warehouse-not-mandatory.md)

[主计划 - 如何确定物料清单版本](master-plan-bom-version-determined.md)




