---
title: 产品配置模型计算
description: 本主题介绍如何在产品配置模型中为属性创建计算
author: t-benebo
ms.date: 03/18/2021
ms.topic: article
ms.search.form: PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-18
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f0806a5b36b04e77a5a6d10f3c2eb3d7ba680e75
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356408"
---
# <a name="product-configuration-model-calculations"></a>产品配置模型计算

[!include [banner](../includes/banner.md)]

本主题介绍如何在产品配置模型中为属性创建计算。

## <a name="prerequisites"></a>先决条件

计算用于产品配置模型中以计算产品的配置值。 必须存在相关的产品配置模型，然后才能开始设置计算。 有关配置模型和相关任务的设置流程的概述，请参阅[设置产品配置模型](set-up-maintain-product-configuration-model.md)。

## <a name="create-a-calculation"></a>创建计算

计算由一个表达式和一个目标属性组成。 有关详细信息，请参阅[产品配置模型的计算常见问题解答](calculate-product-configuration-models.md)。

若要为现有产品模型创建计算，请按照下列步骤操作。

1. 转到 **产品信息管理 \> 通用 \> 产品配置模型**。
1. 打开产品配置模型，然后选择 **编辑**。
1. 在 **计算** 快速选项卡上，选择 **添加** 以添加计算，然后设置以下字段：

    - **名称** – 输入计算的名称。
    - **描述** – 输入计算的描述。
    - **目标属性** – 选择要为其进行计算的属性。

1. 选择 **编辑表达式**。
1. 在 **输入计算** 对话框中，将所需的属性、运算符和值添加到表达式。 有关如何处理这些元素的详细信息，请参阅[产品配置模型中的表达式约束和表约束](expression-constraints-table-constraints-product-configuration-models.md)。
1. 当表达式准备就绪时，选择 **确定**。

## <a name="calculation-examples"></a>计算示例

本部分提供一些示例，显示了计算的工作方式。

### <a name="example-1"></a>示例 1

目标属性是布尔，此计算使用以下条件表达式：

`If[(decimalAttribute1 / decimalAttribute2) < 1, True, False]`

如果 `decimalAttribute2` 大于或等于 `decimalAttribute1`，此表达式返回 *True* 值到目标属性。 否则，返回 *False* 值。

### <a name="example-2"></a>示例 2

本示例使用文本属性 `textFixedList` 作为目标属性。 此属性包含以下固定列表。

| 值 | 求解器值 |
|---|---|
| A | 1a |
| B | 2b |
| C | 2c |

以下屏幕截图显示此属性的设置在您的系统中的外观。

![示例 2 的属性类型设置。](media/model-calculations-example2.png "示例 2 的属性类型设置")

在以下条件语句中使用该属性：

`If[integerAttribute < 150, 0, 2]`

如果 `integerAttribute` 小于 150，此语句将返回固定列表中第一条记录的文本值 *A*。否则，它将返回固定列表中第三条记录的文本值 *C*。

> [!NOTE]
> 固定列表等效于从零开始的枚举 (enum)，并且其值由适当的整数值访问。 因此，第一个固定列表值 (*A*) 与 *0* 匹配，第二个值 (*B*) 与 *1* 匹配，第三个值 (*C*) 与 *2* 匹配。

### <a name="example-3"></a>示例 3

本示例使用上一个示例中的 `textFixedList` 目标属性。 它还使用另一个文本属性 `textAttribute`，其中包含以下固定列表。

| 值 | 求解器值 |
|---|---|
| AA | 1aa |
| BB | 2bb |

以下屏幕截图显示此属性的设置在您的系统中的外观。

![示例 3 的属性类型设置。](media/model-calculations-example3.png "示例 3 的属性类型设置")

使用以下条件语句计算 `textFixedList` 属性的值：

`If[textAttribute == "1aa", 0, 2]`

如果 `textAttribute` 值具有等于 *1aa* 的求解值，此表达式将返回 `textFixedList` 固定列表中第一条记录的文本值 *A*。否则，它将返回 `textFixedList` 固定列表中第三条记录的文本值 *C*。

> [!NOTE]
> - 条件语句必须使用属性的求解值。
> - 在计算中只能使用固定列表文本属性。

## <a name="see-also"></a>请参阅

- [产品配置模型的计算常见问题](calculate-product-configuration-models.md)
- [将表达式约束添加到产品配置模型](tasks/add-expression-constraint-product-configuration-model.md)
- [产品配置模型概述](product-configuration-models.md)
