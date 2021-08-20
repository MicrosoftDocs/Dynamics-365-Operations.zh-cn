---
title: 站点和仓库覆盖范围主计划，仓库是必需的
description: 此主题介绍如何计划将站点和仓库作为覆盖范围维度的物料。 仓库维度是必填的。
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f93602c9f6f5ec1816bd7e81732c6b1d51a6e845f0653b8b561005efdfa52f4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746979"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a>站点和仓库覆盖范围主计划，仓库是必需的

[!include [banner](../includes/banner.md)]

此主题介绍如何计划将站点和仓库作为覆盖范围维度的物料。 仓库维度是必填的。

此主计划方案涉及以下情况：

-   站点维度设置为必填，必须在需求交易记录上输入。
-   仓库维度设置为必填，必须在需求交易记录上输入。
-   为覆盖范围计划设置站点和仓库维度。 还可能为覆盖范围计划设置其他维度。 但是，它们不受多站点功能的影响。

下图说明如何继续主计划。 图中引用的参数及其位置如下所示：
-   仓库设置为 **手动**。 单击 **库存管理 &gt; 设置 &gt; 库存细分 &gt; 仓库**。 在 **主计划** 快速选项卡上，查看 **手动** 字段。
-   为物料定义物料覆盖范围。 单击 **产品信息管理 &gt; 产品 &gt; 已发布产品**。 选择该物料，然后在“操作窗格”上，在 **计划** 选项卡上单击 **物料覆盖范围**。
-   为仓库定义重填关系。 单击 **库存管理 &gt; 设置 &gt; 库存细分 &gt; 仓库**。 在 **主计划** 快速选项卡上，查看 **主仓库** 字段组。
-   默认订单类型设置为“生产”、“采购订单”或“看板”。 单击 **产品信息管理 &gt; 产品 &gt; 已发布产品**。 选择该物料，然后在“操作窗格”上，在 **计划** 选项卡上单击 **默认订单设置**。 在 **默认订单设置** 窗体中，查看 **默认订单类型**。

![需求站点和仓库覆盖范围（仓库必需）。](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



## <a name="additional-resources"></a>其他资源

[主计划和多站点功能概览](master-plan-multisite-functionality.md)

[站点覆盖范围的主计划（仓库必需）](master-plan-site-coverage-warehouse-mandatory.md)

[站点覆盖范围的主计划（仓库非必需）](master-plan-site-coverage-warehouse-not-mandatory.md)

[站点和仓库覆盖范围的主计划（仓库非必需）](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[确定物料清单版本](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]