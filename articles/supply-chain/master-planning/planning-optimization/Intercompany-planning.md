---
title: 内部公司计划
description: 本主题介绍内部公司计划，并说明如何在 Microsoft Dynamics 365 Supply Chain Management 中使用计划优化配置内部公司计划。
author: t-benebo
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: de9f9679bfaf9491c6b69c11448306627c8a42f9
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468487"
---
# <a name="intercompany-planning"></a>内部公司计划

[!include [banner](../../includes/banner.md)]

对于某些组织，物流工序取决于组织中的其他法人（公司）。 由于每个法人都有单独的会计科目表，因此使用内部公司销售和采购来处理这些工序。

本主题介绍内部公司计划，并说明如何在 Microsoft Dynamics 365 Supply Chain Management 中使用计划优化配置内部公司计划。

本主题使用以下重要的内部公司术语：

- **上游** – 公司或供应链中的相对参考。 它指示以原材料供应商的方向变动。
- **下游** – 公司或供应链中的相对参考。 它指示以客户的方向变动。
- **计划内部公司需求** – 公司的产品的计划需求，基于下游公司的产品的计划需求。

在主计划中，一家公司的计划可以包括与另一家公司计划的计划订单相关的计划内部公司需求。 此功能非常有用，因为它可以全面了解公司之间的计划订单。 它还可以确保创建所有必需的计划供应订单，但无需为内部公司需求确定计划订单。

如果从包含计划下游需求的主计划中运行主计划，来自相关内部公司供应商的计划采购订单将作为需求包括在计划中。

## <a name="required-setup"></a>所需的设置

若要使用内部公司计划，必须按照以下方式准备系统：

1. 必须在所有相关公司中发布相关产品。 有关详细信息，请参阅 Microsoft Learn 上的[在 Dynamics 365 Supply Chain Management 中配置和使用内部公司交易](/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/)。
1. 下游需求必须通过与上游公司具有内部公司关系以及具有客户的相关默认库存维度（站点和仓库）的供应商购买来满足。 有关详细信息，请参阅 Microsoft Learn 上的[在 Dynamics 365 Supply Chain Management 中配置和使用内部公司交易](/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/)。
1. 上游公司的主计划必须包括计划的下游需求，并且相关公司和主计划必须在下游计划中指定。

## <a name="include-planned-downstream-demand"></a>包括计划的下游需求

按照以下步骤配置主计划以使其包括计划的下游需求。

1. 转到 **主计划 \> 设置 \> 计划 \> 主计划**。
1. 选择或创建主计划。
1. 在 **内部公司计划** 快速选项卡上，设置以下字段：

    - **包括计划的下游需求** – 将此选项设置为 *是* 以为主计划启用内部公司计划。
    - **下游计划** – 如果将 **包括计划的下游需求** 选项设置为 *是*，使用工具栏和网格从其他公司添加所需的主规划。

## <a name="peg-across-companies-by-using-multilevel-pegging"></a>使用多级限定标准跨公司限定

在多级限定标准中，您可以查看跨公司限定标准，以查看供应所涵盖的初始需求来源。

若要查看多级限定标准信息，请按照下列步骤操作。

1. 转到 **主计划 \> 主计划 \> 计划订单**。
1. 选择或打开计划订单。
1. 在操作窗格的 **视图** 选项卡上，在 **要求** 组中，选择 **多级限定标准**。

### <a name="intercompany-example-that-involves-two-companies"></a>涉及两家公司的内部公司示例

对于此示例，在 USMF 公司中创建计划生产订单以覆盖 DEMF 公司中的销售订单。 在 USMF 中，直接需求是计划内部公司需求。 若要使此需求显示在 USMF 中，请先在 DEMF 中运行主规划，然后再在 USMF 中运行。

下图显示此示例如何显示在计划生产订单的 **多级限定标准** 页面上。

![涉及两家公司的内部公司示例。](media/IntercompanyPlanning1.png)

### <a name="intercompany-example-that-involves-three-companies"></a>涉及三家公司的内部公司示例

对于此示例，在 USMF 公司中创建计划采购订单以覆盖 FRRT 公司中的销售订单。 在 DEMF 和 USMF 公司中，直接需求是计划内部公司需求。 若要使此需求显示在 USMF 中，请先在 FRRT 中运行主规划，然后再在 DEMF 中运行，最后在 USMF 中运行。

下图显示此示例如何显示在计划生产订单的 **多级限定标准** 页面上。

![涉及三家公司的内部公司示例。](media/IntercompanyPlanning2.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]