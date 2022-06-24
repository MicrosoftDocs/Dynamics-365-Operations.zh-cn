---
title: 产品信息概览
description: 本文提供有关产品信息管理的信息。 产品信息管理使用跨所有法人的共用的产品定义、分类和标识符以及产品的特定配置以适应业务流程。
author: t-benebo
ms.date: 06/01/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductListPage, EcoResProductVariantMaintainWorkspace, EcoResProductVariantPerCompanyImagePart, EcoResProductRelationType,EcoResProductAvailabilityPart,  EcoResProductReleasedSelect, EcoResProductLookup, EcoResProductVariantsPendingReleaseFormPart, EcoResProductSearchLookup, EcoResProductNumberRename, EcoResDimensionBasedConfigWorkspace, EcoResProductVariantImagePart, EcoResProductImagePart, EcoResProductVariantsPerCompanyPart, InventItemIdLookupByDefaultOrderSetting, EcoResProductReleaseSessions, EcoResProductVariantMaintainWorkspaceConfiguration, EcoResProductProcessManufacturingWorkspaceConfiguration, EcoResProductMasterVariantsPart, EcoResProductDiscreteManufacturingWorkspaceConfiguration, EcoResProductVariantAvailabilityPart, EcoResProductInformationFactBox, EcoResProductLookupTest, EcoResProductImageTest, EcoResProductReleasedRecentlyCreatedFormPart, EcoResPhysicalProductDimensions, PdsMRCRegulatedListItem, EcoResProductAvailabilityPart, PdsMRCRestrictionList, InventItemIdLookupAllocationId, EcoResProductAvailability, EcoResProductEntityAttributeTableFieldAssociation, EcoResProductImagePart, EcoResProductRelation, EcoResProductReleaseAddProduct, EcoResProductPerCompanyListPage, EcoResProductParameters, PdsMRCRestrictedItemByCountryState, EngChgCasePreview, InventTablePreview, PdsMRCItemDetails, EngChgCaseAssociate, PdsMRCCustomerHistory, PdsMRCVendorHistory, PdsMRCRestrictedCountryStateByItem, InventItemIdGroupLookup, InventLocationLookup, PdsMRCValidityIntervalbyCountry, PdsMRCValidityIntervalbyCountry, PdsMRCEventTracker, PdsMRCReportingCountry, PdsMRCDocument, PdsMRCReportingList, PdsMRCItemCAS, GraphicsTestForm, EngChgPicklist
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa06e718d2acc44cfced7db842814c48fb210d1e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867860"
---
# <a name="product-information-overview"></a>产品信息概览

[!include [banner](../includes/banner.md)]



本文提供有关产品信息管理的信息。 产品信息管理使用跨所有法人的共用的产品定义、分类和标识符以及产品的特定配置以适应业务流程。 

产品信息是跨所有行业的供应链和商业应用的基石。 它指的是以集中管理产品相关信息为主（例如，跨供应链）的流程和技术。 使用共用的产品定义、文档、属性和标识符十分重要。 在不同的业务解决方案模块中，需要产品的特定信息和配置以管理与特定产品、产品系列或产品类别有关的业务流程。

## <a name="product-definition"></a>产品定义

产品主要由产品编号、名称和描述定义。 但是也需要其他数据以描述产品或服务：

- 产品类型：物料或服务
- 产品子类型：独特产品或基础产品
- 产品变型型号的定义：

     - 产品维度和维度组
     - 产品命名法
     - 产品配置模型

- 产品与一个或多个类别的关联
- 产品定义和类别属性
- 产品图像
- 附件
- 度量单位及相关转换
- 所有名称和描述的翻译

## <a name="distribution-export-and-import-of-product-data"></a>产品数据的分配、导出和导入

可以在 Supply Chain Management 中创建产品定义。 也可以从产品生命周期管理 (PLM)、产品数据管理 (PDM) 或产品信息管理 (PIM) 系统导入。 使用多个 Supply Chain Management 实例时，一个实例通常用于所有其他实例的基础产品数据。 此方法受一组大量数据实体的支持，这些数据实体支持将产品定义数据从一个实例导出和导入到另一个实例。

为了支持将产品数据分配到多个实例，Supply Chain Management 允许您使用 Microsoft Dataverse。 产品定义可以从 Supply Chain Management 的一个实例导出到 Microsoft Dataverse。 然后可以使用产品定义提供其他具有产品数据的业务应用，例如 Dynamics 365 Sales。

请注意，在动态和敏捷的组织中，产品信息数据每天都会更改。 因此，维护准确和真实的产品数据本身就是一个重要的业务流程。

## <a name="product-masters-and-product-variants"></a>基础产品和产品变型

在一个敏捷的世界中，产品必须快速适应客户要求，因此产品定义指定一组产品，而不是独特产品。 在 Supply Chain Management 中，这些一般产品被称为 *基础产品*。 基础产品拥有定义和规则，指定独特产品在业务流程中的描述和行为方式。 基于这些定义，可生成独特产品。 这些独特产品被称为 *产品变型*。

基础产品与产品维度组和配置技术相关联以指定业务规则。 产品维度（颜色、大小、样式和配置）是一组特定的属性，可在整个应用中使用以定义和跟踪关联产品的特定行为。 这些维度还有助于用户搜索和标识产品。

## <a name="configuration-technologies"></a>配置技术

您可以在三种配置技术中进行选择：

- 预定义的变型由预定义产品维度定义。 变型定义包括特定的有效维度组合（例如颜色、样式和大小）的定义。 各组合生成一个独特产品变型。
- 基于维度的配置通常在制造方案中使用，让您能够在物料清单 (BOM) 的定义中使用配置维度。 选择特定配置后，系统使用对该配置有效 BOM 行的子集进行计划和生产。 该概念也被称为 *全局 BOM*，因为一个共用 BOM 用于一个产品的所有配置。
- 基于约束的配置使用产品配置模型以描述必需的所有可能的属性和组件以描述在一个模型中的产品的所有可能变型。 属性组合的约束可以通过正则表达式或基于表的约束进行描述。 配置模型和配置器在产品信息管理中越来越重要，且跨所有行业使用。

在计划 Supply Chain Management 的实现时，为业务流程选择正确的配置技术十分重要。 在实现后，产品不能从一个模型转换为其他模型。

## <a name="product-variant-model-definition-workspace"></a>产品变型模型定义工作区

**产品变型模型定义** 工作区提供基础产品的概览。 它还显示基础产品和相关变型发布到特定法人的状态。

## <a name="released-products"></a>已发布产品

已发布到特定法人的产品被称为 *已发布产品*。 产品可以一次性批量发布给一个或多个法人。 可能必须按法人添加产品的不同特征和属性，因此 **已发布产品的维护** 工作区让您能够监控和完成各法人中或法人的子组织中最近发布的产品。

### <a name="released-product-maintenance-workspace"></a>已发布产品的维护工作区

您可以从 **配置我的工作区** 菜单项配置 **已发布产品的维护** 工作区。 选择筛选工作区时所依据的类别层次结构和类别。 要调整工作区中的相关产品数据，您还可以以天数为单位定义 **最新发布的产品** 和 **已停止的已发布产品** 的时限。

工作区包括图块和两个列表的汇总。 **未结案例** 列表显示在所选产品类别层次结构中有未完成和关闭的产品的产品更改案例。 **最近发布** 列表显示在工作区配置中设定的时限范围内已发布的产品。 对于列表中的每个物料，运行验证，且显示验证状态。 此状态可能指示法人的所需配置未完成。 从列表中可以直接访问 **已发布产品详细信息**、**产品属性维护**、**产品类别维护**、**默认订单设置** 和 **文本翻译** 页以完成所需的产品配置。

### <a name="manually-creating-a-new-released-product"></a>手动创建新发布的产品

您可以根据组织的业务流程和关于是否应使用此功能的任何规则在单次运行中手动创建已发布的产品。 此功能创建新产品并自动将其发布到当前法人。 要创建新产品，单击 **已发布的产品维护** 工作区中或 **已发布的产品** 列表页上的 **已发布的产品**。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]