---
title: 针对标准成本的先决条件概览
description: 本主题介绍使用标准成本的基本步骤。
author: AndersGirke
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventStdCostConv, CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee676afbde465c1abb4fe4ae94e9f162f695d994
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263462"
---
# <a name="prerequisites-for-standard-costs-overview"></a>针对标准成本的先决条件概览

[!include [banner](../includes/banner.md)]

本主题介绍使用标准成本的基本步骤。 后续步骤取决于公司的运营。 例如，对于非制造环境、不使用工艺路线的制造环境和使用工艺路线的制造环境，这些步骤有所不同。 

若要设置标准成本，请执行以下步骤。

**1. 为标准成本创建一个物料模型组。**

使用 **物料模型组** 页面为标准成本创建一个新组，并且分配 **标准成本** 的库存模型。 该物料模型组的标识符应该有意义，例如 **标准成本**。 选中复选框以指示该组应该允许财务负库存，并且应该过帐物理库存和财务库存。 此标准成本组将分配给物料。

**2. 定义与标准成本差异相关的会计科目。** 

使用 **会计科目表** 页面可以定义与标准成本差异相关的会计科目。 这些会计科目必须首先定义，然后才能在 **过帐** 页面中分配它们。 这些会计科目可以反映物料组和成本组。

**3. 将会计科目分配到与标准成本差异相关的物料过帐。** 

使用 **过帐** 页面可以分配与标准成本差异相关的会计科目。 您可以按物料（或者物料组）和按成本组（或者成本组类型）指定某一差异的会计科目，或者指定该会计科目应用于所有物料和所有成本组。 这些选项对应于针对表、组和全部的成本关系。 

定义物料过帐规则前，可使用 **交易记录组合** 页启用成本关系（针对表、组和全部）。

**4. 定义与标准成本差异相关的库存参数。** 

-  使用 **库存会计政策设置 > 参数** 页面中的 **库存会计** 选项卡可以定义与标准成本有关的两个成本控制参数。

    -  在 **成本细分** 字段中，选择 **无** 或 **子分类帐**。 如果选择 **子分类帐**，则该成本分解为 *有效* 成本分解。 对于跨标准成本物料的多级产品结构计算、保留和查看成本组细分，有效成本细分十分重要。 在成本细分有效时，您可以采用单个级别、多个级别或总计格式，报告和分析每个成本组的库存、在制品 (WIP) 和所售货物成本 (COGS)。 成本分解有效时，如果激活制造物料的成本，将把成本组分解存储在物料的成本记录内。 

    -  如果选择 **无**，将不为标准成本物料维护成本组分解。 也就是说，制造物料的标准成本将不进行成本组分解，而是作为单一金额计算和维护。 制造组件的成本组成将聚合为这个单一金额。

-  在 **与标准的差异** 字段中，选择 **汇总** 或 **按成本组**。 如果选择 **按成本组**，您可以按成本组标识采购价差异和生产差异。 也可以帮您标识四类生产差异：批次规模、数量、价格和替换差异。 如果选择 **汇总**，则不能按成本组标识差异，也不能标识四种类型的生产差异。 只能查看汇总的生产差异。

-  与标准差异有关的策略独立于成本细分策略。 也就是说，您可以选择 **没有** 成本细分策略，并且选择按成本组差异，以便仍将捕获按成本组的生产差异。

**5. 为标准成本创建成本计算版本。** 

使用 **成本计算版本设置** 页面可为标准成本创建一个或多个成本计算版本。 每一成本计算版本都必须用 **标准成本** 的成本计算类型指定，并且必须允许内容包括成本数据。

**6. 准备现有客户以使用标准成本。** 

想要将其现有物料更改为标准成本库存模型的客户必须使用 **标准成本转换** 页面。


<a name="related-topics"></a>相关主题
--------

[标准成本转换概览](standard-cost-conversion-overview.md)

### <a name="blogs"></a>博客

#### <a name="community-blogs"></a>社区博客

- [如何在 Dynamics 365 for Finance and Operations 中为直接材料设置标准成本](https://financefunction.tech/2018/06/07/how-to-set-up-standard-costs-for-direct-materials-in-dynamics-365-for-finance-and-operations)
- [Dynamics 365 for Finance and Operations 中的标准直接人工成本](https://financefunction.tech/2018/07/16/standard-direct-labor-cost-in-dynamics-365-for-finance-and-operations)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]