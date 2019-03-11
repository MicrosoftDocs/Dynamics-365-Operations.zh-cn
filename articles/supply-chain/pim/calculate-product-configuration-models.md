---
title: 产品配置模型的计算常见问题
description: 本主题描述产品配置模型的计算。并说明如何与约束一起使用计算。
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCConstraintEditor, PCProductConfigurationModelDetails, PCRuntimeConfigurator
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19191
ms.assetid: 8993f9a1-d1c0-49f5-afd3-5e1077ded0fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 00e1956950154051d4a916a013c2200029772e37
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "363376"
---
# <a name="calculations-for-product-configuration-models-faq"></a>产品配置模型的计算常见问题

[!include [banner](../includes/banner.md)]

本主题描述产品配置模型的计算。并说明如何与约束一起使用计算。

计算可以用于算术运算或逻辑运算。 它们补充产品配置模型的表达式约束。 您可以在**基于约束的产品配置模型详细信息**页上定义计算，然后在表达式编辑器中构建计算表达式。 有关详细信息，请参阅“创建计算”。

## <a name="what-is-a-calculation"></a>计算是什么？
计算是您在产品配置模型中可以使用的元素。 在您配置产品时，通过能够让您使用小数来计算值，计算可以补充约束。 此外，与约束相比，计算具有更大的可用运算符集。  

与约束相似，计算与产品配置模型中的特定组件关联，且其不能被其他组件重用或共享。 计算和约束之间的重要差异在于计算是必需的（单向），而约束是说明性的（双向）。 有关约束的详细信息，请参阅[表达式约束和表约束](expression-constraints-table-constraints-product-configuration-models.md)。  

计算包含目标属性和计算表达式。

## <a name="what-is-a-target-attribute"></a>目标属性是什么？
目标属性是一种接收计算表达式结果的属性。  

在下面的表达式中，目标属性是桌布度量：  

**表达式：** If\[decimalAttribute1 &lt;= decimalAttribute2, True, False\]  

**DecimalAttribute1** 是桌子长度，而 **decimalAttribute2** 是桌布长度。 如果 **decimalAttribute2** 大于或等于 **decimalAttribute1**，则表达式返回 **True** 值到目标属性。 否则，该表达式返回 **False** 值。 因此，如果桌布长度等于或超过桌子长度，则可接受桌布度量。

## <a name="what-attribute-types-can-be-set-to-target-attributes"></a>对目标属性可以设置何种属性类型？
除了没有固定列表的文本，产品配置器支持的所有属性类型均可设置为目标属性。

## <a name="can-the-value-of-a-target-attribute-restrict-the-values-of-the-input-attributes-in-a-calculation"></a>目标属性的值可以限制计算中输入属性的值吗？
不能，目标属性的值不能限制输入属性的值，因为计算是单向的。 因此，目标属性的值基于输入属性值的更改设置，但是，该目标值的更改不影响输入属性的值。 此行为与约束的行为不同。 约束出现在两个方向。

### <a name="example"></a>示例

在下面的表达式中，计算的目标是电源线的长度，并且输入值为颜色：  

**表达式：**\[If Color == "Green", 1.5, 1.0\]  

果您指定**绿色**为颜色属性的值，则设置电源线的长度为 **1.5**。 如果您指定其他颜色，该长度设置为 **1.0**。 但是，由于计算为单向，如果您指定长度为 **1.5**，计算不能将颜色属性的值设置为**绿色**。

## <a name="what-happens-if-a-calculation-has-a-target-attribute-of-the-integer-type-but-a-calculation-generates-a-decimal-number"></a>如果计算具有整数类型的目标属性，但是计算生成了一个小数，此时将发生什么情况？
如果目标属性是整数类型，不过，计算生成小数，则只返回计算结果的整数部分。 移除小数部分，且不舍入结果。 例如，结果为 12.70 将显示为 12。

## <a name="when-do-calculations-occur"></a>何时出现计算？
在为所有输入属性提供一个值时出现计算。

## <a name="can-i-overwrite-the-value-that-is-calculated-for-the-target-attribute"></a>我可以覆盖为目标属性计算的值吗？
您可以覆盖为目标属性计算的值，除非目标属性被设置为隐藏或只读状态。

## <a name="how-do-i-set-a-target-attribute-as-hidden-or-read-only"></a>当处于隐藏或只读状态时，如何设置目标属性？
若要设置处于隐藏或只读状态的属性，请执行以下步骤。

1.  单击**产品信息管理** &gt; **通用** &gt; **产品配置模型**。
2.  选择产品配置模型，然后在“操作窗格”上，单击 **编辑**。
3.  在**基于约束的产品配置模型详细信息**页上，选择用作目标属性的属性。
4.  在**属性**快速选项卡上，选择**隐藏**或**只读**。

## <a name="can-a-calculation-overwrite-the-values-that-i-set"></a>计算可以覆盖我设置的值吗？
编号 在您配置产品时您设置的值即为所使用的值。 在计算中更改输入值时出现的计算不能覆盖您为特定属性提供的值。

## <a name="what-happens-if-i-remove-an-input-value-in-a-calculation"></a>如果我移除计算中的输入值会发生什么情况？
如果您移除计算中的输入值，目标属性的值也将被移除。

## <a name="why-do-i-receive-an-error-message-that-says-that-my-model-is-in-contradiction"></a>为什么我收到一条错误消息称我的模型处于冲突状态？
在计算包含错误或在一个或多个约束存在冲突时将显示此消息。 有关约束中冲突的详细信息，请参阅[表达式约束和表约束](expression-constraints-table-constraints-product-configuration-models.md)。 这是一些计算中可能出现错误的情况：

-   值除以 0（零）。
-   冲突存在于以下两个元素之间：
    -   可用于属性的值与由约束限制的值
    -   由计算产生的值
-   由计算返回的值超出属性的域之外。 示例是计算为 0 的从 \[1..10\] 的一个整数。

## <a name="why-do-i-receive-an-error-message-even-though-i-successfully-validated-my-product-model"></a>为什么即使在我成功验证了我的产品模型后仍收到错误消息？
验证中并不包括计算。 您必须测试产品配置模型以查找计算中的错误。 若要测试产品配置模型，请按照下面的步骤执行。

1.  单击**产品信息管理** &gt; **通用** &gt; **产品配置模型**。
2.  选择产品配置模型，然后在“操作窗格”上，在**运行**组中单击**测试**。




