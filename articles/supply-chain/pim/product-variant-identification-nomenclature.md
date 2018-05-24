---
title: "产品变型编号和名称的命名法"
description: "此主题介绍如何设置产品编号命名法来替换固定的[基础产品编号 - 配置 - 尺寸 - 颜色 - 样式] 格式。"
author: roxanadiaconu
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 3baf1d7313d8ff03ae5ece035b6f3641c0f1d707
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="nomenclature-of-product-variant-numbers-and-names"></a>产品变型编号和名称的命名法

[!include [banner](../includes/banner.md)]

此主题介绍如何设置产品编号命名法来替换固定的[基础产品编号 - 配置 - 尺寸 - 颜色 - 样式] 格式。 新的命名法具有目标格式，包括您选择的基础产品编号、有效产品维度和文本分隔符。 您还可以创建产品名称的命名法。 最后，您可以构建命名法以识别由基于约束的产品配置器创建的配置。 这些命名法可包含您选择的属性。

产品变型编号和产品变型名称的命名法让您可以在产品变型的标识符中包含细分信息。 这些细分信息可能包括基础产品编号和名称、产品维度 ID 和名称、编号规则、文本常量和属性。 在您创建销售订单或采购订单时，此功能可以快速查找特定产品变型。 通过使用**产品命名法**页，您创建产品变型编号和产品变型名称的命名法。 若要打开此页，单击**产品信息管理** &gt; **设置**。

## <a name="nomenclature-of-predefined-product-variants"></a>预定义产品变型命名法
根据以下三种配置技术的其中一种生成基础产品的产品变型：

-   预定义的变型
-   基于约束
-   基于维度

每个产品变型都有一个编号和名称，且产品变型标识命名法允许您选择每个产品变型编号或名称中要使用的细分信息。 您可以选择以下**产品命名法**页面上的细分信息：

-   基础产品编号
-   基础产品名称
-   编号规则值
-   文本常量
-   产品维度
    -   配置 ID 或名称
    -   颜色 ID 或名称
    -   尺寸 ID 或名称
    -   样式 ID 或名称

定义产品变型标识编号命名法后，您可将其与产品维度组关联。 随后将根据命名法为引用此产品维度组的所有基础产品分配产品变型编号。 但是，产品变型名称命名法不能与产品维度组关联。 您还可以将产品变型标识命名法直接分配给基础产品。 在这种情况下，将根据命名法为属于该基础产品的产品变型分配产品变型编号和名称。

### <a name="example"></a>示例

T 恤衫 (TS1234) 生产为三个尺寸（S、M、L）、四种颜色（红色、绿色、蓝色、黄色）和两种款式（Polo、V）。 因此，可能有 24 个产品变型 (= 3 × 4 × 2)。 您创建具有以下细分信息的产品变型编号命名法：

1.  基础产品编号
2.  文本常量："-"
3.  颜色
4.  文本常量："-"
5.  尺寸
6.  文本常量："-"
7.  样式

在这种情况下，红色小码 Polo T 恤衫的产品变型编号为 TS1234-Red-Small-Polo。

## <a name="nomenclature-of-constraint-based-configurations"></a>基于约束的配置命名法
对于基于约束的配置，您可以为配置产品维度构建专门的命名法。 您可以选择以下**产品命名法**页面上的细分信息：

-   编号规则值
-   文本常量
-   属性值

产品模型配置中的每个组件都可以有自己的配置命名法。 仅可使用属于此组件的属性。 子组件或用户要求的属性不能使用。

### <a name="example"></a>示例

产品配置模型有具有两个属性的根组件：

-   材料（塑料，木头，钢）
-   长度 (10…100)

您创建具有以下细分信息的配置命名法：

1.  属性值：材料
2.  文本常量："AAA"
3.  属性值：长度

在这种情况下，长度为 78 的木质材料的配置 ID 将是 WoodAAA78。

## <a name="nomenclature-of-dimension-based-configurations"></a>基于维度的配置命名法
对于基于维度的配置，您可以为配置产品维度构建专门的命名法。 您可以选择以下**产品命名法**页面上的细分信息：

-   编号规则值
-   文本常量
-   配置组项

您可以为物料清单 (BOM) 定义配置命名法。

### <a name="example"></a>示例

物料清单具有可分为两个配置组的四个物料清单行：

-   物料清单行：M0007，标准机柜
    -   配置组：机柜
-   物料清单行：M0008，高端机柜
    -   配置组：机柜
-   物料清单行：M0021，前格栅布料
    -   配置组：前格栅
-   物料清单行：M0022，前格栅金属
    -   配置组：前格栅

您创建具有以下细分信息的配置命名法：

1.  配置组：机柜
2.  文本常量："&"
3.  配置组：前格栅

在这种情况下，具有布料前格栅的标准机柜的配置 ID 将为 M0007&M0021。

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a>产品变型和配置组合的命名法
使用基于约束的配置技术或基于维度的配置技术配置基础产品的产品变型时，产品变型的产品变型编号可以包括来自配置维度的命名法。 请执行以下步骤配置变型。

1.  在**产品命名法**页面上，定义包括配置维度的产品变型编号命名法。
2.  将此命名法分配给具有配置维度的产品维度组。
3.  定义要用于配置产品变型的组件或物料清单的配置命名法。

您还可以创建产品变型名称的命名法。 产品变型名称可以配置为包括配置 ID 或名称。

### <a name="example-for-constraint-based-configurations"></a>基于约束的配置示例

对于此示例，您使用包括以下细分信息的产品变型编号命名法：

1.  基础产品编号
2.  文本常量 "\_"
3.  配置

配置命名法由以下细分信息组成：

1.  属性值：材料
2.  文本常量："AAA"
3.  属性值：长度

您输入以下细分信息的值：

-   基础产品编号 = **M0099**
-   材料 = **塑料**
-   长度 = **12**

在这种情况下，产品变型编号将为 M0099\_PlasticAAA12。

### <a name="example-for-dimension-based-configurations"></a>基于维度的配置示例

对于此示例，您使用包括以下细分信息的产品变型编号命名法：

1.  基础产品编号
2.  文本常量 "//"
3.  配置

配置命名法由以下细分信息组成：

1.  配置组：机柜
2.  文本常量："&"
3.  配置组：前格栅

您输入以下细分信息的值：

-   基础产品编号 = **D0123**
-   机柜 = **M0008**
-   前格栅 = **M0022**

在这种情况下，产品变型编号将为 D0123//M0008&M0022。

## <a name="numbering-conflicts"></a>编号冲突
在有些情况下，设置的产品变型编号命名法可能不会产生唯一的产品变型编号。 例如，如果一个有效的产品维度不包括在使用预定义的变型配置技术的基础产品的命名法中，产品变型编号则可能不是唯一的。 您处理冲突的方法因配置技术而异。

### <a name="predefined-variants"></a>预定义的变型

如果您试图手动创建或自动生成产品变型，且多个产品变型末尾为相同的产品变型编号，则将发生错误。 若要避免此情况，应在产品维度组中使用所有活动产品维度。 或者，包括编号规则以帮助保证产品变型编号是唯一的。

### <a name="constraint-based-configurations"></a>基于约束的配置

根据命名法，系统可能尝试为配置分配一个非唯一的产品变型编号。 在这种情况下，系统将使用配置维度的编号规则作为产品变型编号，您将收到警告。 若要避免此情况，您应在命名法中包括足够的属性以帮助保证唯一的产品变型编号。 您还应确保为此组件启用**重复使用**选项。

### <a name="dimension-based-configurations"></a>基于维度的配置

在配置流程的一个步骤中，系统将根据命名法建议一个配置值。 在此步骤中，您可以手动更改配置值。 当您保存配置时，系统将确认配置值是否唯一。 如果您输入的值不是唯一的，您将收到错误消息。 若要保存配置，您必须输入唯一配置值。

<a name="additional-resources"></a>其他资源
--------

[为预定义的产品变型创建产品编号命名法](tasks/create-product-number-nomenclature-predefined-variants-2016-11.md)

[为配置的产品变型创建产品编号命名法](tasks/create-product-number-nomenclature-product-variants_2016_11.md)


