---
title: "创建和管理属性"
description: "文章此工序中 Microsoft Dynamics 365 中描述各属性。 属性可让您通过用户定义字段描述产品及其特征。"
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16461
ms.assetid: 2b85491c-f830-4e79-a2cb-681b7ced6988
ms.search.region: global
ms.search.industry: Retail
ms.author: prabhup
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 26c628e10aaa5f47bc87d7510ca8f41ab3630204
ms.lasthandoff: 03/31/2017


---

# <a name="create-and-manage-attributes"></a>创建和管理属性

文章此工序中 Microsoft Dynamics 365 中描述各属性。 属性可让您通过用户定义字段描述产品及其特征。

属性可让您通过用户定义字段描述产品及其特征。 例如，您可以指定产品的内存大小硬盘容量，并指示产品是否符合能源之星计划。 可以将属性与各种零售实体（如产品类别和零售通道）关联，并且可以为属性设置默认值。 当产品与产品类别或销售渠道关联时，产品将继承其属性以及这些属性的默认值。 默认值可在单个产品的级别、在零售渠道级别或在零售目录中覆盖。

#### <a name="examples"></a>示例

类别

属性

允许的值

默认值

电视和视频

品牌

任何有效的**品牌**值

无

电视

屏幕尺寸

**20"**–**80"**

无

垂直行业解决方案

**480i**、**720p**、**1080i** 或 **1080p**

** 1080p **

屏幕刷新率

**60hz**、**120hz** 或 **240hz**

** 60hz **

HDMI 输入

**0**–**10**

**3**

DVI 输入

**0**–**10**

**1**

复合输入

**0**–**10**

**2**

组件输入

**0**–**10**

**1**

LCD

3D 已就绪

**是**或**否**

**是**

3D 已启用

**是**或**否**

**否**

等离子

最低工作温度

**32**–**110** 度

**32**

最高工作温度

**32**–**110** 度

**100**

投影

投影管保修

**6**、**12** 或 **18** 个月

**12**

对当前\#

**1**–**5**

**3**

## <a name="attribute-type"></a>属性类型
  [] (固定![属性复制。/media/attributes 固定 copy.png)](。/media/attributes 固定的 copy.png 属性) 基于各属性类型。 属性类型用于确定可为特定属性输入的数据的类型。 目前，工序 365 的 Microsoft Dynamics 支持以下属性类型：

-   **货币** - 此属性类型支持货币值。 它可以受约束（即，它可以支持某个值范围），也可以保持开放。
-   **日期时间** - 此属性类型支持日期和时间值。 它可以受约束（即，它可以支持某个值范围），也可以保持开放。
-   **小数** - 此属性类型支持包括小数位的数字值。 它还支持度量单位。 它可以受约束（即，它可以支持某个值范围），也可以保持开放。
-   **整数** - 此属性类型支持数字值。 它还支持度量单位。 它可以受约束（即，它可以支持某个值范围），也可以保持开放。
-   **文本** - 此属性类型支持文本值。 它还支持预定义的一组可能值（枚举）。
-   **布尔型** –此属性类型支持二进制值 (** **请为/** **错误)。
-   **引用**。

## <a name="attribute"></a>属性
  [] (![createandmanageattribute-8。/media/createandmanageattribute-8.png)](。除了/media/createandmanageattribute-8.png) 名称、友好名称、描述和帮助文本，一个或多个之外下列信息类型可用于捕获属性：

-   默认值
-   属性元数据（如指示是否可对属性进行搜索、细化或排序的元数据）

## <a name="attribute-group"></a>属性组
  [] (![createandmanageattribute-10。/media/createandmanageattribute-10.png)](。/media/createandmanageattribute-10.png)，然后定义属性后，可以组合为属性组。 属性组提供了各个属性的分组，并可以分配到零售类别或零售渠道。

## <a name="assigning-attribute-groups-to-retail-categories"></a>将属性组分配到零售类别
  [] (![createandmanageattribute-12。/media/createandmanageattribute-12.png)](。/media/createandmanageattribute-12.png) 一个或多个属性组可同时与产品类别在"零售层次结构的类别节点。 为产品分类后，这些产品将继承属性组中包含的属性。

## <a name="assigning-attribute-groups-to-retail-stores"></a>将属性组分配到零售商店
  [] (![createandmanageattribute-13-1024x576。/media/createandmanageattribute-13-1024x576.png)](。/media/createandmanageattribute-13-1024x576.png) 一个或多个属性组可同时与在零售店层次结构中有一个或多个零售店。 为特定零售商店丰富产品后，这些产品将继承属性组中包含的属性。

## <a name="overriding-attribute-values"></a>覆盖属性值
### <a name="at-the-product-level"></a>在产品级别

  [] (![createandmanageattribute-14-1024x576。/media/createandmanageattribute-14-1024x576.png)](。/media/createandmanageattribute-14-1024x576.png) 的默认属性值可以覆盖在产品级别 (即为单独的产品)。

### <a name="in-a-retail-catalog"></a>在零售目录中

  [] (![createandmanageattribute-2。/media/createandmanageattribute-2.png)](。/media/createandmanageattribute-2.png) 的默认属性值。针对为特定零售通道面向的特定的覆盖单独的产品目录。

### <a name="at-the-retail-channel-level"></a>在零售渠道级别

  [] (![createandmanageattribute-1。/media/createandmanageattribute-1.jpg)](。/media/createandmanageattribute-1.jpg) 的默认属性值。针对为特定零售通道面向的特定的覆盖单独的产品目录。


