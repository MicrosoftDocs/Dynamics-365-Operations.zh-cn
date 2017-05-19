---
title: "产品编号命名法"
description: "本主题介绍您可以如何设置产品编号命名法以替换固定格式，[基础产品编号 - 配置 - 尺寸 - 颜色 - 样式]，其中目标格式包括基础产品编号、有效的产品维度以及您选择的文本分隔符。 您还可以构建命名法以识别由基于约束的产品配置器创建的配置。 这些命名法可包含您选择的属性。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 220104
ms.assetid: 31c9efb4-b5f6-4af3-b884-8f1e128469bd
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: deda2b7986333e0d865aa87e6b34b6acdc8f6a6d
ms.contentlocale: zh-cn
ms.lasthandoff: 04/25/2017


---

# <a name="product-number-nomenclature"></a>产品编号命名法

[!include[banner](../includes/banner.md)]


本主题介绍您可以如何设置产品编号命名法以替换固定格式，[基础产品编号 - 配置 - 尺寸 - 颜色 - 样式]，其中目标格式包括基础产品编号、有效的产品维度以及您选择的文本分隔符。 您还可以构建命名法以识别由基于约束的产品配置器创建的配置。 这些命名法可包含您选择的属性。

新的产品变型编号命名法允许您将细分信息包括在产品变型标识符中。 这些细分信息可能包括基础产品编号、产品维度、编号规则、文本常量和属性。 在您创建销售订单或采购订单时，此功能可以快速查找特定产品变型。

## <a name="nomenclature-of-predefined-product-variants"></a>预定义产品变型命名法
根据以下三种配置技术的其中一种生成基础产品的产品变型：

-   预定义的变型
-   基于约束
-   基于维度

每个产品变型都有一个编号，且产品变型标识命名法允许您选择每个产品变型编号中要使用的细分信息。 您可以选择以下**产品命名法**页面上的细分信息。

-   基础产品编号
-   编号规则值
-   文本常量
-   产品维度
    -   配置
    -   颜色
    -   尺寸
    -   样式

定义产品变型标识命名法后，可与产品维度组相关联。 因此，将根据命名法为引用此产品维度组的所有基础产品分配产品变型编号。 还可以直接对基础产品分配产品变型标识命名法，这种情况下，将根据命名法为属于此基础产品的产品变型分配产品变型编号。

### <a name="example"></a>示例

T 恤衫 (TS1234) 生产 3 种不同尺寸（小码，中码，大码），4 种不同颜色（红色，绿色，蓝色，黄色）和 2 种款式（Polo 衫，V 领衫），总共可能有 24 种产品变型。 使用以下细分信息创建产品变型标识命名法：

1.  基础产品编号
2.  文本常量：'-'
3.  颜色
4.  文本常量：'-'
5.  尺寸
6.  文本常量：'-'
7.  样式

红色小码 Polo 衫的产品变型编号为：TS1234-Red-Small-Polo。

## <a name="nomenclature-of-constraintbased-configurations"></a>基于约束的配置命名法
对于基于约束的配置，可以为配置产品维度构建专门的命名法。 您可以选择以下**产品命名法**页面上的细分信息。

-   编号规则值
-   文本常量
-   属性值 

产品模型配置中的每个组件都可以有自己的配置命名法。 仅可使用属于此组件的属性。 子组件或用户要求的属性不可用。

### <a name="example"></a>示例

产品配置模型有具有两个属性的根组件。

-   材料（塑料，木头，钢）
-   长度 (10…100)

使用以下细分信息定义配置命名法：

1.  属性值：材料
2.  文本常量：'AAA'
3.  属性值：长度

长度为 78 的木质材料的配置 ID 将具有以下配置 ID：WoodAAA78。

## <a name="nomenclature-of-dimensionbased-configurations"></a>基于维度的配置命名法
对于基于维度的配置，可以为配置产品维度构建专门的命名法。 您可以选择以下**产品命名法**页面上的细分信息。

-   编号规则值
-   文本常量
-   配置组项

可以为物料清单 (BOM) 定义配置命名法。

### <a name="example"></a>示例

物料清单具有 4 个物料清单行，划分为 2 个配置组。

-   物料清单行：M0007，标准机柜
    -   配置组：机柜
-   物料清单行：M0008，高端机柜
    -   配置组：机柜
-   物料清单行：M0021，前格栅布料
    -   配置组：前格栅
-   物料清单行：M0022，前格栅金属
    -   配置组：前格栅

使用以下细分信息定义配置命名法：

1.  配置组：机柜
2.  文本常量：'&'
3.  配置组：前格栅

布料前格栅的标准机柜的配置 ID 将为：M0007&M0021。

## <a name="nomenclature-of-a-combination-of-product-variants-and-configurations"></a>产品变型和配置组合的命名法
使用基于约束或基于维度的配置技术配置基础产品的产品变型时，产品变型可以获得产品变型编号，其中包括来自配置维度的命名法。 请执行以下步骤配置变型：

1.  定义包括**产品命名法**页面上的配置维度的产品变型编号命名法。
2.  将此命名法分配给具有配置维度的产品维度组。
3.  定义要用于配置产品变型的组件或 BOM 的配置命名法。

### <a name="example-for-constraint-based-configurations"></a>基于约束的配置示例

在此示例中，您可以使用包括以下细分信息的产品变型编号命名法：

1.  基础产品编号
2.  文本常量“\_”
3.  配置

配置命名法可以由以下细分信息组成：

1.  属性值：材料
2.  文本常量：'AAA'
3.  属性值：长度

您可以输入以下细分信息的值：

-   基础产品编号 = M0099
-   材料 = 塑料
-   长度 = 12

产品变型编号将为：M0099\_PlasticAAA12。

### <a name="example-for-dimension-based-configurations"></a>基于维度的配置示例

在此示例中，您可以使用包括以下细分信息的产品变型编号命名法：

1.  基础产品编号
2.  文本常量 '//'
3.  配置

配置命名法可以由以下细分信息组成：

1.  配置组：机柜
2.  文本常量：'&'
3.  配置组：前格栅

您可以输入以下细分信息的值：

-   基础产品编号 = D0123
-   机柜 = M0008
-   前格栅 = M0022

产品变型编号将为：D0123//M0008&M0022。

## <a name="numbering-conflicts"></a>编号冲突
设置产品变型编号命名法可能导致产品变型编号不唯一。 例如，如果一个有效的产品维度不包括在使用预定义的变型配置技术的基础产品的命名法中，则可能发生这种情况。 对于不同的配置技术，处理冲突的方法不同。

### <a name="predefined-variants"></a>预定义的变型

如果您试图手动或自动生成产品变型，其中一个或多个末尾为相同的产品变型编号，则将发生错误。 为避免出现这种情况，您应使用产品维度组中的所有有效的产品维度，或者包括一个编号规则，以确保产品变型编号唯一。

### <a name="constraint-based-configurations"></a>基于约束的配置

根据命名法，系统可能尝试为配置分配一个非唯一的产品变型编号。 在这种情况下，系统将使用配置维度的编号规则作为产品变型编号。 如果发生这种情况，您将收到警告。 为避免出现这种情况，您应在命名法中包含足够的属性，以确保唯一性，且确保打开该组件的“**重复使用**”选项。

### <a name="dimension-based-configurations"></a>基于维度的配置

配置流程包括一个步骤，即系统将根据命名法建议一个配置值。 在此步骤中，您可以手动更改配置值。 当您保存配置时，系统将检查配置值是否唯一。 如果不唯一，将显示错误。 您必须输入唯一配置值以保存该配置。



<a name="see-also"></a>请参阅
--------

[为预定义的产品变型创建产品编号命名法（任务指南）](http://ax.help.dynamics.com/en/wiki/create-a-product-number-nomenclature-for-predefined-product-variants/)

[为配置的产品变型创建产品编号命名法（任务指南）](http://ax.help.dynamics.com/en/wiki/create-a-product-number-nomenclature-for-configured-product-variants/)




