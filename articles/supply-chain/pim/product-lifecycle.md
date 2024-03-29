---
title: 产品生命周期状态概览
description: 产品生命周期状态记载已发布产品或产品变型的生命周期状态。
author: t-benebo
ms.date: 01/06/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductLifecycleState, EcoResReleasedProductLifecycleStateChanges
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: 5d1ea1517c75393b1c8d7c95c8aa2405042b4532
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850632"
---
# <a name="product-lifecycle-state-overview"></a>产品生命周期状态概览

[!include [banner](../includes/banner.md)]

产品生命周期状态记载已发布产品或产品变型的生命周期状态。 产品生命周期状态由用户定义，通常是产品经理或产品主数据经理。 特定业务流程，例如主计划，可能受特定生命周期状态的影响。

已发布产品或产品变型可以与记载特定产品或变型目前所处生命周期状态的产品生命周期状态关联。 您可以通过指定状态名称和描述的方式定义任何数量的产品生命周期状态。 您可以选择一个生命周期状态作为新发布产品的默认状态。 已发布产品变型在创建时从它们已发布的基础产品继承其产品生命周期状态。 在已发布基础产品上更改生命周期状态时，您可以选择更新具有相同原始状态的所有现有变型。  

## <a name="create-a-new-product-lifecycle-state"></a>创建新产品生命周期状态

- 要创建新的产品生命周期状态，请参阅[创建新的产品生命周期状态](tasks/new-product-lifecycle-state.md)。

- 要创建默认产品生命周期状态，请参阅[创建默认产品生命周期状态](tasks/default-product-lifecycle-state.md)。

## <a name="associate-product-lifecycle-states-to-released-products"></a>将产品生命周期状态关联到发布的产品  

有多种方式将产品生命周期状态关联到发布的产品或产品变型。

- 在创建新发布产品时，自动分配默认的 **产品生命周期状态**。
- 在将产品发布到法人时，自动分配默认的 **产品生命周期状态**。
- 在将产品变型发布到法人时，与该法人中的已发布产品变型关联的 **产品生命周期状态** 自动分配到新的变型。

您可以使用以下方式手动更新产品生命周期状态：

- **已发布产品** 列表页或 **详细信息视图**。
- **已发布的产品变型** 列表页或 **详细信息视图**。
- 基于需求查找过时的产品或产品变型并关联生命周期状态。  

有关详细信息：

- 要将产品生命周期状态关联到已发布的基础产品，请参阅[对已发布的基础产品分配产品生命周期状态](tasks/product-lifecycle-state-released-product-master.md)。

- 要将产品生命周期状态关联到发布产品，请参阅[对已发布产品分配产品生命周期状态](tasks/product-lifecycle-state-released-product.md)。

## <a name="impact-on-master-planning"></a>对主计划的影响

产品生命周期状态只有一个控制标志：**对于计划有效**。 默认情况下对所有创建的产品生命周期状态设置为 **是**，但可以更改为 **否**。 设置为 **否** 时，关联的已发布产品或已发布产品变型为：

- 从主计划排除。
- 从物料清单级别计算中排除。

有关如何使用产品生命周期状态从主计划和物料清单级别计算中排除产品的详细信息，请参阅[创建产品生命周期状态以从主计划中排除产品](tasks/exclude-products-master-planning.md)

> [!NOTE]
> 由于性能原因，强烈建议使用对主计划禁用的产品生命周期状态关联所有过时的已发布产品或产品变型，尤其是当使用不可重复使用的产品配置变型时。  

## <a name="default-migration-import-and-export"></a>默认迁移、导入和导出

产品生命周期状态受数据实体的支持，生命周期状态可以通过已发布产品的数据实体或已发布变型的数据实体设置为可变状态。

## <a name="find-obsolete-products-and-products-variants"></a>查找过时的产品和产品变型

您可以运行模拟分析以查找过时的已发布产品或产品变型，然后更新它们的产品生命周期状态。 要查找过时的产品，请参阅[查找过时的产品变型并分配产品生命周期状态](tasks/obsolete-product-variants.md)。 本文介绍如何查找过时的已发布产品或产品变型以及如何将产品生命周期状态关联到过时的产品。 它还显示如何查看模拟结果以及评估在不通过模拟运行更新时有多少产品和产品变型将与新产品生命周期状态关联。  

通过在模拟模式中运行分析，标识为过时的产品和产品变型显示在特定窗体中，可以轻松地查看。 分析过程将搜索交易记录和特定主数据，以识别在特定可变期间内没有需求且没有可以产生需求的主数据的产品。 在可变期间内新发布的产品可以从分析中排除。 当分析模拟返回预期结果时，用户可以运行分析并对在分析过程中识别为过时的所有产品设置新的产品生命周期状态。  

> [!NOTE]
> 请注意，所有分析和更新必须在相同法人内进行。  

## <a name="criteria-to-select-and-update-released-products-or-product-variants"></a>选择和更新已发布产品或产品变型的条件

使用以下条件选择和更新已发布的产品和产品变型：

- 产品或产品变型的产品生命周期状态必须不同于新的所需状态。
- 产品或产品变型基于您在选择对话框中输入的天数提前几天创建。
- 没有针对该产品或产品变型的开放生产订单（= 状态 < 已结束）。
- 没有针对该产品或产品变型的开放库存交易记录（= 状态发货 ReservPhysical 到 QuotationIssue 或状态收货已登记到 QuotationReceipt）。
- 在过去几天内没有针对该产品或产品变型的库存交易记录。
- 没有针对该产品或产品变型的未来需求或供应预测。  
- 在物料覆盖范围中没有针对该产品或产品变型设定最低存货水平。
- 没有针对该产品或产品变型的有效固定数量看板规则。  
- 没有针对该产品或产品变型的服务订单行。
- 没有针对该产品或产品变型的活跃或未来销售或购买协议行。
- 产品或产品变型在与对于计划有效的产品或变型的未过期的已核准的物料清单版本关联的物料清单中不使用。

## <a name="related-articles"></a>相关文章

- [创建新产品生命周期状态](tasks/new-product-lifecycle-state.md)
- [创建默认产品生命周期状态](tasks/default-product-lifecycle-state.md)
- [为已发布的基础产品分配产品生命周期状态](tasks/product-lifecycle-state-released-product-master.md)
- [为已发布的产品分配产品生命周期状态](tasks/product-lifecycle-state-released-product.md)
- [查找过时的产品变型并分配产品生命周期状态](tasks/obsolete-product-variants.md)
- [创建产品生命周期状态以从主计划中排除产品](tasks/exclude-products-master-planning.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]