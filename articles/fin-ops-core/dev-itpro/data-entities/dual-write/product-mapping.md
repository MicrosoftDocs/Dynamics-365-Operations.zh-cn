---
title: 统一的产品体验
description: 本主题介绍 Finance and Operations 应用与 Dataverse 之间的产品数据集成。
author: t-benebo
manager: AnnBe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 46f2f846f1259d433630a69f17f7b8db9514e6fa
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680040"
---
# <a name="unified-product-experience"></a>统一的产品体验

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

当业务生态系统由 Dynamics 365 应用程序（例如 Finance、Supply Chain Management 和 Sales）组成时，企业往往会使用这些应用程序来获取产品数据。 这是因为这些应用提供了强大的产品基础架构，并辅以完善的定价概念和准确的现有库存数据。 使用外部产品生命周期管理 (PLM) 系统来获取产品数据的企业可以将产品从 Finance and Operations 应用导入其他 Dynamics 365 应用。 统一的产品体验将集成的产品数据模型引入 Dataverse，以便包括 Power Platform 用户在内的所有应用程序用户都可以利用来自 Finance and Operations 应用的丰富产品数据。

这是来自 Sales 的产品数据模型。

![CE 中的产品数据模型](media/dual-write-product-4.jpg)

这是来自 Finance and Operations 应用的产品数据模型。

![Finance and Operations 中的产品数据模型](media/dual-write-products-5.jpg)

如下所示，这两个产品数据模型已集成到 Dataverse 中。

![Dynamics 365 应用中的产品数据模型](media/dual-write-products-6.jpg)

产品的双写入表映射设计为仅单向流动数据，实时地从 Finance and Operations 应用流动到 Dataverse。 但是，如果需要，产品基础结构已经开放，可以实现双向。 虽然您可以进行自定义，但需自担风险，因为 Microsoft 不建议使用此方法。

## <a name="templates"></a>模板

产品信息包含与产品及其定义有关的所有信息，例如产品维度或跟踪维度和存储维度。 如下表所示，将创建表映射的集合以同步产品和相关信息。

Finance and Operations 应用 | 其他 Dynamics 365 应用 | 说明
-----------------------|--------------------------------|---
已发布产品 V2 | msdyn\_sharedproductdetails | **msdyn\_sharedproductdetails** 实体包含来自 Finance and Operations 应用的字段，这些字段定义产品，并包含产品的财务和管理信息。 
Dataverse 发布的独特产品 | 产品 | **产品** 实体包含定义产品的字段。 它包括单个产品（具有子类型产品的产品）和产品变型。 下表显示了映射。
产品编号标识条形码 | msdyn\_productbarcodes | 产品条形码用于唯一标识产品。
默认订单设置 | msdyn\_productdefaultordersettings
产品特定默认订单设置 | msdyn_productdefaultordersettings
产品维度组 | msdyn\_productdimensiongroups | 产品维度组定义了哪些产品维度定义产品。 
存储维度组 | msdyn\_productstoragedimensiongroups | 产品存储维度组表示用于定义产品在仓库中的位置的方法。
跟踪维度组 | msdyn\_producttrackingdimensiongroups | 产品跟踪维组表示用于跟踪库存中产品的方法。
颜色 | msdyn\_productcolors
大小 | msdyn\_productsizes
样式 | msdyn\_productsytles
配置 | msdyn\_productconfigurations
基础产品颜色 | msdyn_sharedproductcolors | **共享产品颜色** 实体表示特定基础产品可以具有的颜色。 此概念已迁移到 Dataverse 以保持数据一致。
基础产品大小 | msdyn_sharedproductsizes | **共享产品尺寸** 实体表示特定基础产品可以具有的尺寸。 此概念已迁移到 Dataverse 以保持数据一致。
基础产品样式 | msdyn_sharedproductstyles | **共享产品样式** 实体表示特定基础产品可以具有的样式。 此概念已迁移到 Dataverse 以保持数据一致。
基础产品配置 | msdyn_sharedproductconfigurations | **共享产品配置** 实体表示特定基础产品可以具有的配置。 此概念已迁移到 Dataverse 以保持数据一致。
所有产品 | msdyn_globalproducts | 所有产品实体都包含 Finance and Operations 应用中可用的所有产品，包括已发放产品和未发放产品。
单位 | uoms
单位换算 | msdyn_ unitofmeasureconversions
产品特定度量单位转换 | msdyn_productspecificunitofmeasureconversion
产品类别 | msdyn_productcategories | 每个产品类别以及有关其结构和特征的信息都包含在产品类别实体中。 
产品类别层次结构 | msdyn_productcategoryhierarhies | 您可以使用产品层次结构来对产品进行分类或分组。 使用产品类别层次结构实体，类别层次结构在 Dataverse 中可用。 
产品类别层次结构角色 | msdyn_productcategoryhierarchies | 产品层次结构可用于 D365 Finance and Operations 中的不同角色。 它们指定使用产品类别角色实体的每个角色中使用的类别。 
产品类别分配 | msdyn_productcategoryassignments | 要将产品分配给类别，可以使用产品类别分配实体。

## <a name="integration-of-products"></a>产品的集成

在此模型中，产品由 Dataverse 中两个表的组合表示：**Product** 和 **msdyn\_sharedproductdetails**。 第一个实体包含产品的定义（产品的唯一标识符、产品名称和说明），而第二个实体包含在产品级别存储的字段。 这两个表的组合用于根据库存单位 (SKU) 的概念定义产品。 每个发放的产品将在提及的表（“产品”和“共享产品详细信息”）中具有其信息。 为了跟踪所有产品（已发放和未发放），使用 **全局产品** 实体。 

由于产品表示为 SKU，因此可以通过以下方式在 Dataverse 中捕获独特产品、基础产品和产品变型的概念：

- **具有子类型产品的产品** 是它们自己定义的产品。 无需定义维度。 一个例子是特定帐簿。 对于这些产品，在 **Product** 实体中创建一个记录，并在 **msdyn\_sharedproductdetails** 实体中创建一个记录。 不创建产品系列记录。
- **基础产品** 用作具有定义和规则的一般产品，这些定义和规则确定业务流程中的行为。 基于这些定义，可以生成称为产品变型的独特产品。 例如，T 恤是基础产品，可以具有颜色和尺寸维度。 可以发布具有这些维度的不同组合的变型，例如小号蓝色 T 恤或中号绿色 T 恤。 在集成中，在产品表中为每个变型创建一个记录。 此记录包含特定于变型的信息，例如不同的维度。 产品的一般信息存储在 **msdyn\_sharedproductdetails** 实体中。 （此一般信息保留在基础产品中。）创建已发放的基础产品后（但在发放变型之前），基础产品信息即同步到 Dataverse。
- **独特产品** 是指所有产品子类型产品和所有产品变型。 

![产品的数据模型](media/dual-write-product.png)

启用双写入功能后，Finance and Operations 中的产品将在其他 Dynamics 365 产品中同步并处于 **草稿** 状态。 它们将以相同的货币添加到第一个价目表中。 换言之，它们将被添加到 Dynamics 365 应用中的第一个价目表中，该应用与在 Finance and Operations 应用中发放产品的法人的货币相匹配。 

默认情况下，Finance and Operations 应用中的产品会以 **草稿** 状态同步到其他 Dynamics 365 应用。 要同步状态为 **活动** 的产品，以便您可以直接在销售订单报价单中使用它，例如，需要选择以下设置：**系统 > 管理 > 系统管理 > 系统设置 > Sales** 选项卡，选择 **创建处于活动状态的产品 = 是**。 

请注意，产品的同步是从 Finance and Operations 应用到 Dataverse。 这意味着可以在 Dataverse 中更改产品实体字段的值，但是当触发同步时（在 Finance and Operations 应用中修改了产品字段时），这将覆盖 Dataverse 中的值。 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [products](includes/EcoResReleasedDistinctProductCDSEntity-products.md)]

[!include [product details](includes/EcoResReleasedProductV2-msdyn-sharedproductdetails.md)]

[!include [global products](includes/EcoResEveryProductEntity-msdyn-globalproducts.md)]

## <a name="product-dimensions"></a>产品维度 

产品维度是标识产品变型的特性。 四个产品维度（颜色、尺寸、样式和配置）也映射到 Dataverse 以定义产品变型。 下图显示了产品维度“颜色”的数据模型。 相同的模型也应用于“尺寸”、“样式”和“配置”。 

![产品维度的数据模型](media/dual-write-product-two.png)

[!include [product colors](includes/EcoResProductColorEntity-msdyn-productcolor.md)]

[!include [product sizes](includes/EcoResProductSizeEntity-msdyn-productsizes.md)]

[!include [product sizes](includes/EcoResProductStyleEntity-msdyn-productstyles.md)]

[!include [product sizes](includes/EcoResProductConfigurationsEntity-msdyn-productconfigurations.md)]

当产品具有不同的产品维度时（例如，基础产品具有“尺寸”和“颜色”产品维度），则将每个独特产品（即每个产品变型）定义为这些产品维度的组合。 例如，产品编号 B0001 是一件超小号黑色 T 恤，产品编号 B0002 是一件小号黑色 T 恤。 在这种情况下，将定义产品维度的现有组合。 例如，前面示例中的 T 恤可以是超小号黑色、小号黑色、中号黑色或大号黑色，但不能是超大号黑色。 换言之，指定了基础产品可以采用的产品维度，并且可以基于这些值发放变型。

为了跟踪基础产品可以采用的产品维度，在 Dataverse 中为每个产品维度创建并映射了以下表。 有关详细信息，请参阅[产品信息概览](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/pim/product-information)。

[!include [product colors](includes/EcoResProductMasterColorEntity-msdyn-sharedproductcolors.md)]

[!include [product sizes](includes/EcoResProductMasterSize-msdyn-sharedproductsizes.md)]

[!include [product styles](includes/EcoResProductMasterStyleEntity-msdyn-sharedproductstyles.md)]

[!include [product configurations](includes/EcoResProductMasterConfigurationEntity-msdyn-sharedproductconfigurations.md)]

[!include [product bar codes](includes/EcoResProductNumberIdentifiedBarcode-msdyn-productbarcodes.md)]

## <a name="default-order-settings-and-product-specific-default-order-settings"></a>默认订单设置和产品特定的默认订单设置

默认订单设置定义作为物料采购来源或存储物料的站点和仓库，在贸易或库存管理中将要使用的最低量、最高量、倍数和标准量，提前期，停止标志，以及订单承诺方法。 这些信息在 Dataverse 中使用默认订单设置和产品特定的默认订单设置实体提供。 您可以在[默认订单设置主题](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/default-order-settings)中阅读有关此功能的详细信息。

[!include [product sizes](includes/InventProductDefaultOrderSettingsEntity-msdyn-productdefaultordersetting.md)]

[!include [product sizes](includes/InventProductSpecificOrderSettingsV2Entity-msdyn-productspecificdefaultordersetting.md)]

## <a name="unit-of-measure-and-unit-of-measure-conversions"></a>度量单位和度量单位转换

度量单位及其各自的转换按照图中所示的数据模型在 Dataverse 中提供。

![度量单位的数据模型](media/dual-write-product-three.png)

度量单位概念在 Finance and Operations 应用与其他 Dynamics 365 应用之间进行了集成。 对于 Finance and Operations 应用中的每个单位类别，将在 Dynamics 365 应用中创建一个单位组，其中包含属于该单位类别的单位。 另外还为每个单位组创建一个默认基础单位。 

[!include [unit of measure](includes/UnitOfMeasureEntity-uom.md)]

[!include [unit of measure conversions](includes/UnitOfMeasureConversionEntity-msdyn-unitofmeasureconversions.md)]

[!include [product-specific unit of measure conversions](includes/EcoResProductSpecificUnitConversionEntity-msdyn-productspecificunitofmeasureconversions.md)]

## <a name="initial-synchronization-of-units-data-matching-between-finance-and-operations-and-dataverse"></a>Finance and Operations 与 Dataverse 之间的单位数据匹配的初始同步

### <a name="initial-synchronization-of-units"></a>单位的初始同步

启用双写入后，Finance and Operations 应用中的单位将同步到其他 Dynamics 365 应用。 从 Dataverse 中的 Finance and Operations 应用同步的单位组具有一个标志集，指示它们是“外部维护”。

### <a name="matching-units-and-unit-classesgroups-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>匹配来自 Finance and Operations 和其他 Dynamics 365 应用的单位和单位类别/组数据

首先，必须注意，单位的集成密钥是 msdyn_symbol。 因此，此值在 Dataverse 或其他 Dynamics 365 应用中必须是唯一的。 因为在其他 Dynamics 365 应用中，定义单位唯一性的是“单位组 ID”和“名称”对，因此您需要考虑在 Finance and Operations 应用和 Dataverse 之间匹配单位数据的不同场景。

对于 Finance and Operations 应用和其他 Dynamics 365 应用中的单位匹配/重叠：

+ **单位属于其他 Dynamics 365 应用中的单位组，该单位组与 Finance and Operations 应用中的关联单位类别相对应**。 在这种情况下，必须使用 Finance and Operations 应用中的单位符号填充其他 Dynamics 365 应用中的 msdyn_symbol 字段。 因此，在将数据匹配时，在其他 Dynamics 365 应用中会将单位组设置为“外部维护”。
+ **单位属于其他 Dynamics 365 应用中的单位组，该单位组与 Finance and Operations 应用中的关联单位类别不对应（其他 Dynamics 365 应用中的单位类别在 Finance and Operations 应用中没有现有的单位类别）。** 在这种情况下，必须使用随机字符串填充 msdyn_symbol。 请注意，此值在其他 Dynamics 365 应用中必须是唯一的。

对于 Finance and Operations 中其他 Dynamics 365 应用中不存在的单位和单位类别：

作为双写入的一部分，Finance and Operations 应用中的单位组及其对应的单位在其他 Dynamics 365 应用和 Dataverse 中创建并同步，该单位组将设置为“外部维护”。 无需额外的自扩展工作。

对于 Finance and Operations 应用中不存在的其他 Dynamics 365 应用中的单位：

必须为所有单位填充 msdyn_symbol 字段。 单位始终可以在 Finance and Operations 应用中的相应单位类别（如果存在）中创建。 如果单位类别不存在，则必须首先创建与其他 Dynamics 365 应用单位组匹配的单位类别（请注意，如果您在扩展枚举，则除通过扩展外，您无法在 Finance and Operations 应用中创建单位类别）。 然后，您可以创建单位。 请注意，Finance and Operations 应用中的单位符号必须是先前在其他 Dynamics 365 应用中为该单位指定的 msdyn_symbol。

## <a name="product-policies-dimension-tracking-and-storage-groups"></a>产品策略：维度、跟踪和存储组

产品策略是用于定义产品及其库存特性的一组策略。 产品维度组、产品跟踪维度组和存储维度组可以用作产品策略。 

[!include [product dimension group](includes/EcoResProductDimensionGroup-msdyn-productdimensiongroups.md)]

[!include [product tracking dimension group](includes/EcoResTrackingDimensionGroup-msdyn-producttrackingdimensiongroups.md)]

[!include [product storage dimension group](includes/EcoResStorageDimensionGroup-msdyn-productstoragedimensiongroups.md)]

## <a name="product-hierarchies"></a>产品层次结构

[!include [product category hierarchy](includes/EcoResProductCategoryHierarchyEntity-msdyn-productcategoryhierarchy.md)]

[!include [product category](includes/EcoResProductCategoryEntity-msdyn-productcategory.md)]

[!include [product category assignments](includes/EcoResProductCategoryAssignmentEntity-msdyn-productcategoryassignment.md)]

[!include [product category role](includes/EcoResProductCategoryHierarchyRoleEntity-msdyn-productcategoryhierarchyrole.md)]


## <a name="integration-key-for-products"></a>产品的集成密钥 

为了唯一标识 Dynamics 365 for Finance and Operations 和 Dataverse 中的产品之间的产品，使用了集成密钥。 对于产品，**（产品编号）** 是在 Dataverse 中标识产品的唯一密钥。 它由以下各项的串联组成：**（公司, msdyn_产品编号）**。 **公司** 表示 Finance and Operations 中的法人，**msdyn_产品编号** 表示 Finance and Operations 中特定产品的产品编号。 

对于其他 Dynamics 365 应用的用户，产品在 UI 中标识为 **msdyn_productnumber**（请注意，字段的标签为 **产品编号**）。 在产品表单中，同时显示公司和 msydn_产品编号。 但是，没有显示（产品编号）字段，即产品的唯一密钥。 

如果基于 Dataverse 创建应用，则应将 **productnumber**（唯一产品 ID）用作集成密钥。 切勿使用 **msdyn_productnumber**，因为这不是唯一的。 

## <a name="initial-synchronization-of-products-and-migration-of-data-from-dataverse-to-finance-and-operations"></a>产品的初始同步以及数据从 Dataverse 到 Finance and Operations 的迁移

### <a name="initial-synchronization-of-products"></a>产品的初始同步 

启用双写入后，Finance and Operations 应用中的产品将同步到 Dataverse 和 Dynamics 365 中的其他模型驱动应用。 双写入发布之前在 Dataverse 和其他 Dynamics 365 应用中创建的产品将不会更新或与 Finance and Operations 中的产品数据匹配。

### <a name="matching-product-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>匹配 Finance and Operations 和其他 Dynamics 365 应用中的产品数据

如果在 Finance and Operations 中以及在 Dataverse 和其他 Dynamics 365 应用中保留（重叠/匹配）相同的产品，则在启用双写入时，将进行 Finance and Operations 中产品的同步，并且相同产品的重复记录将出现在 Dataverse 中。
为避免上述情况，如果其他 Dynamics 365 应用中的产品与 Finance and Operations 重叠/匹配，则启用双写入的管理员必须在产品进行同步之前自扩展字段 **公司**（例如：“USMF”）和 **msdyn_产品编号**（例如：“1234:Black:S”）。 换言之，Dataverse 中产品中的这两个字段在 Finance and Operations 中必须使用产品需要与之匹配的相应公司及其产品编号填充。 

然后，启用并进行同步后，Finance and Operations 中的产品将与 Dataverse 和其他 Dynamics 365 应用中的匹配产品同步。 这适用于不同的产品和产品变型。 


### <a name="migration-of-product-data-from-other-dynamics-365-apps-to-finance-and-operations"></a>将产品数据从其他 Dynamics 365 应用迁移到 Finance and Operations

如果其他 Dynamics 365 应用具有 Finance and Operations 中不存在的产品，管理员可以首先使用 **EcoResReleasedProductCreationV2Entity** 将这些产品导入 Finance and Operations。 然后，如上所述，匹配 Finance and Operations 和其他 Dynamics 365 应用中的产品数据。 


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]