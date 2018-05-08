---
title: "计算物料消耗量"
description: "本文提供有关与物料消耗量的计算相关的不同选项的信息。"
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMDesignerEditBOM, BOMTable, ProdBOM
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 53401
ms.assetid: 9cff88e4-0425-4707-9178-3c2cb10df7c2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f674a1f0051ee4b228b8a92f717ef5348a452bed
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="calculate-material-consumption"></a>计算物料消耗量

[!include [banner](../includes/banner.md)]

本文提供有关与物料消耗量的计算相关的不同选项的信息。 

与物料消耗量计算相关的以下选项在**物料清单**页的**行明细**快速选项卡的**设置**和**步骤消耗量**选项卡上可用。

## <a name="variable-and-constant-consumption"></a>变量和常量消耗量
在**消耗量**字段中，您可以选择是否应将消耗量计算为一个常量数量或一个变量数量。 如果生产需要固定数量或量，选择**常量**，不论生产的数量是多少。 如果成品中需要的物料金额与生产的成品的数量成比例，则选择**变量**，这是默认设置。

## <a name="calculating-consumption-from-a-formula"></a>通过公式计算消耗量
在**公式**字段中，您可以设置计算物料消耗量的各个公式。 如果您使用默认值**标准**，消耗量不会从公式进行计算。 以下公式与**高度**、**宽度**、**深度**、**密度**和**常量**字段一起使用：

-   高度 \* 常量
-   高度 \* 宽度 \* 常量
-   高度 \* 宽度 \* 深度 \* 常量
-   (高度 \* 宽度 \* 深度/密度) \* 常量

## <a name="rounding-up-and-multiples"></a>进位和倍数
**进位**和**倍数**字段共同让您舍入物料消耗量价值。 例如，您可以根据在其中为生产领取物料的物料处理单元舍入该值。 以下选项在**舍入**字段中可用：**数量**、**度量**和**消耗量**。

### <a name="quantity"></a>数量

如果您选择**数量**作为舍入机制，数量必须是指定数量的倍数。 例如，需要整数时，在**倍数**字段中选择 **1**。 数字然后舍入到被 1 整除的数量。

### <a name="measurement"></a>量化指标

通常，当原材料采用特定尺寸时，选择**度量**作为舍入机制。 例如，成品需要一条 2 米金属管，金属管存储为 4.5 米长度。 在这种情况下，**度量**舍入机制可用于计算生产特定件数的成品需要多少个金属管。 对于此示例，**公式**字段设置为**高度 \* 常量**。 **高度**字段设置为 **2**，指示成品所需的管的长度。 **倍数**字段设置为 **4.5** 指示领取 4.5 米长的管。 计算如下：

1.  10 件成品需要的倍数数：10 ÷ 2 = 5 件
2.  总消耗量：4.5 × 5 = 22.5 米金属管

假定消耗每五个管报废 0.5 米管。

### <a name="consumption"></a>消耗量法

通常，当必须领取产品特定物料处理单元的完整数量的原材料时，选择**消耗量**作为舍入机制。 例如，2 夸脱涂料用于生产一件成品，涂料使用 25 夸脱罐领取。 在这种情况下，**消耗量**舍入机制可用于将消耗量舍入为 25 夸脱罐的整数。 如果必须生产 180 件成品，所需涂料数量计算为：

1.  所需涂料，不包括废料：180 × 2 = 360 夸脱
2.  罐数：360 ÷ 25 = 14.4，舍入为 15
3.  所需涂料，包括废料：15 × 25 = 375 夸脱

## <a name="step-consumption"></a>步骤消耗量
步骤消耗量用于计算数量间隔的常量消耗量。 如果在**设置**选项卡的**公式**字段中选择**步骤消耗量**，您可以在**步骤消耗量**选项卡上添加有关步骤的信息。固定消耗数量可以在生产数量的间隔中设置。 例如，如下表中所示设置步骤消耗量。

| 开始系列 | 数量 |
|-------------|----------|
| 0.00        | 10.0000  |
| 100.00      | 20.0000  |
| 200.00      | 40.0000  |

物料清单 (BOM) 数量为 1，生产数量为 110。 消耗量的公式为开始系列（数量）= 消耗量。 由于生产数量为 110，则落入“从 100 系列”。 因此数量为 20。




