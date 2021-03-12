---
title: 物料清单和配方
description: 本主题提供有关物料清单 (BOM) 和配方的信息，物料清单和配方是产品和产品变型定义的核心部分。
author: cvocph
manager: tfehr
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, BOMTable, EcoResProductProcessManufacturingWorkspace, ProdBOM, ProdJournalTransBOM, ProdBOMCurrent, PmfBOMDesignerEditCoBy, ProdJournalPickingListLineSummary, ProdBOMOverview, PmfCoReqPlanning, EcoResProductProdTypeFormulaNoActiveFormulaFormPart, EcoResItemsMissingActiveRouteVersionFormPart, EcoResItemsProdTypeBOMExpiringBOMFormPart, BOMDesignerBOMVersion, BOMExpandPurch, BOMChangeLine, BOMExpandSales, EcoResItemsProdTypeBOMExpiringRouteFormPart, EngChgEcmBomDesigner, EngChgEcmProductBOMItemIdLookup, EngChgEcmProductBOMConsistOf, EngChgEcmBOMCopyDialog, EngChgEcmBomDesignerEditBom, BOMDesignerFilterDialog, BOMDesignerFilterDialog, BOMPartOf, BOMSetupReportFinish, EcoResItemsMissingActiveBOMVersionFormPart, BOMIdLookup, EcoResProductProdTypeFormulaNoActiveRouteFormPart, BOMExpandPurchRFQ, EngChgCaseRouteTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19331
ms.assetid: c19b437a-2de2-4728-9477-2bcb0c2b1f5e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 01491f15405e28e63e4b83f9a9c7af90c2e4a1b5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966472"
---
# <a name="bills-of-materials-and-formulas"></a>物料清单和配方

[!include [banner](../includes/banner.md)]

本主题提供有关物料清单 (BOM) 和配方的信息，物料清单和配方是产品和产品变型定义的核心部分。 物料清单和配方指定特定产品必需的成分或材料。 配方还指定特定生产环境中接收的联产品和副产品。 

<a name="bills-of-materials"></a>物料清单
------------------

物料清单 (BOM) 用于定义生产产品所需的组件。 这些组件可以是原材料、半成品或成分。 在某些情况下，服务可以在物料清单中引用。 但是，物料清单通常描述的是所需的 *材料资源*。  

当与描述制作产品所需的工序和资源的工艺路线或生产流相结合时，物料清单将构成计算产品的估计成本的基础。  

物料清单是由以下信息说明的单个实体：

-   物料清单 ID
-   物料清单名称
-   描述组件和成分的物料清单行
-   物料清单版本，定义物料清单适用的产品和期间

单个物料清单描述由唯一 ID 标识的单个级别。 组件可能有自己的由物料清单版本引用的 BOM。 您可以在物料清单设计器中显示和编辑特定产品的物料清单的完整层次结构。

### <a name="formulas-co-products-and-by-products"></a>配方、联产品和副产品

配方是通常用于流程制造的物料清单的子类型。 除了组件和成分，配方还描述了联产品和副产品。 在实际版本中，配方的联产品和副产品的定义需要配方版本。 配方通常是为某个特定成品（配方或计划物料）定义的。

### <a name="boms-in-the-product-lifecycle"></a>产品生命周期中的物料清单

在产品生命周期中，可能出于各种原因创建很多类型的物料清单：

-   **草案物料清单** - 此物料清单提供了早期设计阶段中需要的材料的草案估计，并帮助您进行成本和预计产品属性的粗略估计。 此物料清单通常不在企业资源规划 (ERP) 中使用。
-   **工程物料清单** - 此物料清单通常在您设计基于现有产品组合的产品时使用。 工程物料清单在结构上可简化设计流程并将复杂的产品分为若干个工程模块。 对于简单的产品，可以将工程物料清单用于实际的生产流程。 但是，对于其他产品，必须将工程物料清单物料转换为实际生产物料清单。 工程物料清单在物料清单层次结构中通常由虚拟表示。 尽管工程物料清单可用于工序的规划和执行，但此方法可能导致效率低下，尤其是在创建了很多订单的重复性工序中。
-   **计划物料清单** - 此物料清单用于执行物料需求的规划。 组件和成分的需求根据成品的需求来计算。 与成本计算物料清单相似，计划物料清单可能表示某个期间内使用的特定物料组合。
-   **生产物料清单** - 这是用于特定生产的实际物料清单。 生产物料清单必须考虑用于生产产品的实际资源。 创建生产订单、批次订单或看板后，由虚拟表示的多个级别的物料清单将折叠为一个级别并分配到该订单的各个工序。
-   **成本计算物料清单** - 此物料清单用于计算产品的估计成本。 例如，您可以在使用标准成本或计算给定产品的估计计划成本后使用成本计算物料清单。 成本计算物料清单可能引用应使用的物料和资源的特定组合。 因此，您可以使用成本计算物料清单为某个期间创建一个代表性估计成本并帮助避免日后出现差异。

实际用于某个实施的物料清单的类型取决于该实施以及业务方案和要求。 在简单实施中，计划物料清单、生产物料清单和成本计算物料清单可作为一个物料清单进行建模。 在工程变更频繁并具有多条备用工艺路线的环境中，可能需要更大的一组物料清单。

### <a name="approval-of-boms-and-formulas"></a>物料清单和配方的审核

每个物料清单和配方可以单独地获得批准或取消批准。 通常，物料清单或配方的审核在第一个相关物料清单版本获得批准时进行。 但是，在某些企业方案中，这些审核可能是流程中的不同步骤，并可能涉及不同的流程负责人。  

请注意，如果物料清单未获得批准，所有相关物料清单版本也将未获得批准。

## <a name="bom-and-formula-versions"></a>物料清单和配方版本
要将特定物料清单或配方与可生产的产品变型关联，您必须创建物料清单版本或配方版本。 物料清单版本和配方版本的有效性可能受到期间、数量、站点、特定物料维度和其他条件的约束。 配方版本具有其他重要属性，如产出、联产品和副产品定义以及配方的成本分配说明。

### <a name="approval-of-bom-and-formula-versions"></a>物料清单和配方版本的审核

必须先审核物料清单版本，然后才能在计划或制造流程中使用它。 在审核物料清单版本后，也可以审核相关物料清单，版本具体取决于用户的选择和身份验证权利。 请注意，仅在审核相关物料清单后才能审核物料清单版本。

### <a name="activation-of-the-default-bom-or-formula-version"></a>默认物料清单或配方版本的启用

要将特定物料清单或配方设置为将由主计划使用的或用于创建生产订单的默认物料清单版本或配方版本，您必须启用该版本。 在启用某个版本后，将验证该版本针对给定约束（例如，期间、站点或数量）的唯一性。 如果您尝试启用的版本与已生效的版本相冲突，您将收到一条错误消息。 您随后必须停用冲突的版本或修改版本约束（通常是期间）以防止不明确的启用。

### <a name="product-change-with-case-management"></a>带案例管理的产品变更

适用于新的或已更改的物料清单和物料清单版本的产品变更案例提供了一个查看物料清单版本约束的简单方法。 您还可以审核和启用与一个启用日期的特定更改相关的所有物料清单和配方。

### <a name="alternative-bom-versions"></a>备用物料清单版本

有时候，有效的物料清单版本或配方版本不应在预测、销售或父产品中使用。 在这种情况下，如果备用物料清单或配方已存在获得批准的物料清单版本和配方版本，您可以选择特定的获得批准的物料清单作为需求（预测行、销售行或物料清单行）的一部分。  

在创建计划订单、生产订单或看板后，规划员或车间主管可使用在请求的计划生产日期生效的任何获得批准的物料清单版本来计划或生产特定产品。 所使用的物料清单版本不必作为默认物料清单版本启用。

## <a name="bom-and-formula-lines"></a>物料清单和配方行
将为每个物料、服务或成分创建物料清单行。 该行定义了指定产品变型的计划消耗量，还定义了与计划消耗量相关的各种属性。  

物料清单行可以具有以下行类型：**物料**、**虚拟**、**限定供应**、**供应商**。

### <a name="item"></a>物料

为直接消耗但不需要进一步分解或限定供应的物料和服务选择 **物料** 行类型。

### <a name="phantom"></a>虚拟

当您要分解在物料清单行上包含的任何更低级别的物料清单物料时，请选择 **虚拟**。 在主计划编制中，在计划成本计算中，或者在使用 **虚拟** 类型的物料清单行的生产订单的估计中，引用具有虚拟物料清单的产品变型的父物料清单行将替换为在该物料清单中作为物料清单行列出的构成物料（由该产品变型的适用的有效物料清单版本确定）。 如果产品变型具有适用的有效工艺路线，该工艺路线的工序将合并到父工艺路线中。  

请注意，虚拟通常用于简化工程流程。 在多个级别广泛使用虚拟物料清单会影响性能，尤其是在高度重复的制造方案中。 为了提高性能，您应该避免为虚拟设置较深的层次结构。 相反，您应使用预先分解的生产物料清单和工艺路线。

### <a name="pegged-supply"></a>限定供应

当您要创建子生产、创建物料清单行事件看板或创建物料清单行引用的任何产品变型的直接采购订单时，请选择 **限定供应**。 子生产、事件看板或采购订单在您估计生产订单时创建。 将自动为消耗生产订单预留所需的物料数量。

### <a name="vendor"></a>供应商

如果生产流程利用了某个转包商，并且您想要自动为该转包商创建子生产或采购订单，请选择 **供应商** 行类型。  

**有关物料清单中的转包工序的注释：** 由转包商执行的服务或工作必须作为在库存中跟踪的服务项创建。 您必须将服务项作为物料清单行附加到父项。 工艺路线必须包含分配给转包商的运营资源。



