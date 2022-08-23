---
title: 使用电子报告格式的数据收集数据源
description: 本文说明如何使用电子报告 (ER) 格式的数据集合数据源。
author: kfend
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.16
ms.custom: 58771
ms.assetid: ''
ms.search.form: EROperationDesigner
ms.openlocfilehash: 221cefc1880cdd88a952140424daf24975a575aa
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286170"
---
# <a name="use-data-collection-data-sources-in-electronic-reporting-formats"></a>使用电子报告格式的数据收集数据源

[!include [banner](../includes/banner.md)]

您可以使用[电子报告 (ER)](general-electronic-reporting.md) 框架的工序设计器，以配置用于生成其他格式出站文档的 ER 解决方案的格式组件。 配置的格式组件的层次结构由各种类型的格式元素组成。 这些格式元素用于在运行时用所需的信息填充生成的文档。 默认情况下，当您运行 ER 格式时，格式元素的运行顺序与它们在格式层次结构中的显示顺序相同：从上到下一个接一个。

当 ER 运行包含绑定的格式元素时，会运行该绑定的公式，并且格式元素会将值添加到生成的文档中。 例如，绑定可以将数据模型字段的值传递到格式元素。 您可以配置数据集合数据源以在运行时收集数据模型字段的值，进行值求和，并使用收集的值填充生成的文档。 要使用此方法，请更改初始绑定，以便使用配置的数据集合数据源将数据模型字段的值传递给格式元素。 通过数据集合数据源传递值，您可以收集所需的详细信息以供进一步使用。

配置数据集合数据源时，请指定将在数据源中管理的值类型。 当前为收集值支持以下[数据类型](er-formula-supported-data-types-primitive.md)：

- 布尔
- 日期
- 日期时间
- GUID
- Int64
- 整数
- 实数
- 字符串
- 时间

您可以使用数据收集数据源的 `Collect(Value)` 方法将值传递到数据源以进行收集。 在此方法中，`Value` 参数是相关数据类型的数据源字段的常量或有效路径。

使用数据集合数据源的 `Result` 属性访问收集的值列表。 此属性返回[记录列表](er-formula-supported-data-types-composite.md#record-list)。 记录列表的记录包含可用于访问所收集值的 `Value` 字段。

默认情况下，数据集合数据源仅收集唯一值。

若要收集所有值，请将配置的数据集合数据源的 **收集所有值** 字段设置为 **是**。 当 **收集所有值** 字段设置为 **是** 时，`Sum(Flag)` 参数化属性将变得可用。 您可以使用此属性获取当前收集的所有值的总金额。 在此属性中，`Flag` 参数是一个用于指示是否必须重置总值的[布尔值](er-formula-supported-data-types-primitive.md#boolean)。

- 提供 **False** 值后，将从先前收集的金额中继续进行合计。
- 提供 **True** 值后，将开始新的合计。

合计当前支持以下数据类型：

- Int64
- 整数
- 实数

若要了解有关此功能的详细信息，请完成以下示例。

## <a name="example-configure-an-er-format-to-do-counting-and-summing-by-using-a-data-collection-data-source"></a>示例：配置 ER 格式以使用数据集合数据源进行盘点和合计

此示例显示系统管理员或电子报告功能顾问角色的用户如何配置具有数据集合数据源的 ER 格式，该数据源用于计算正在运行的总计和收集汇总值。

在 Microsoft Dynamics 365 Finance 中，本示例中的过程可以在 USMF 公司完成。

### <a name="upload-and-use-the-provided-er-solution"></a>上传并使用提供的 ER 解决方案

1. [导入示例 ER 配置](er-defer-sequence-element.md#import-the-sample-er-configurations)。
2. [激活配置提供程序](er-defer-sequence-element.md#activate-a-configurations-provider)。
3. [查看导入的模型映射](er-defer-sequence-element.md#review-the-imported-model-mapping)。
4. [查看导入的格式](er-defer-sequence-element.md#review-the-imported-format)。
5. [运行导入的格式](er-defer-sequence-element.md#run-the-imported-format)。

### <a name="run-the-format-of-the-provided-er-solution"></a>运行提供的 ER 解决方案的格式

1. 在 **格式设计器** 页上，选择 **运行**。
2. 在 **电子申报参数** 对话框中，选择 **确定**。
3. 下载并查看 Web 浏览器提供的文件。

    ![包含初始格式执行结果的已下载文件](./media/er-data-collection-data-sources-01.png)

### <a name="modify-the-format-of-the-er-solution-to-calculate-the-running-tax-total"></a>修改 ER 解决方案的格式以计算税款累计总和

如果交易记录量远大于当前示例中的交易记录量，则求和查询时间可能会增加并导致性能问题。 通过更改格式设置，可以帮助防止这些性能问题。 因为您访问税收值以将其包括在生成的报表中，所以您可以重复使用此信息来求税收值总计。

1. 在 **格式设计器** 页中 **映射** 选项卡上，选择 **添加根**。
2. 在 **添加数据源** 对话框中，选择 **函数** \> **数据集合**。
3. 在 **数据集合的数据源属性** 对话框中，按照以下步骤操作：

    1. 在 **名称** 字段中，输入 **CollectedTaxValues**。
    2. 在 **物料类型** 字段中，选择 **实际**。
    3. 在 **收集所有值** 字段中，选择 **是**。
    4. 选择 **确定**。

4. 选择 **报表\\行\\记录\\TaxAmount** 数字格式元素。

    > [!NOTE]
    > 当前，已为此元素配置 `@.Value` 绑定。 因此，如果用 `model.Data.List.Value` 字段中的税值填写了生成的文档。

5. 选择 **编辑公式**。
6. 在 **公式设计器** 页上，执行以下步骤：

    1. 在 **公式** 字段中，将 `@.Value` 替换为 `CollectedTaxValues.Collect(@.Value)`。
    2. 保存更改并关闭页面。

    > [!NOTE]
    > 新绑定会将相同的税值传递给生成的文档。 但是，也将在 **CollectedTaxValues** 数据源中收集这些值。

7. 选择 **报表\\行\\记录\\RunningTotal** 数字格式元素。
8. 选择 **编辑公式**。
9. 在 **公式设计器** 页上，执行以下步骤：

    1. 在 **公式** 字段中，输入 `CollectedTaxValues.Sum(false)`。
    2. 保存更改并关闭页面。

    > [!NOTE]
    > 新的绑定将传递到生成的文档，即已输入的税值的总金额。

    ![已在“格式设计器”页面上更新绑定的数字元素](./media/er-data-collection-data-sources-02.png)

10. 选择 **保存**，然后选择 **运行**。
11. 在 **电子申报参数** 对话框中，选择 **确定**。
12. 下载并查看 Web 浏览器提供的文件。

    ![包含已修改格式执行结果的已下载文件](./media/er-data-collection-data-sources-03.png)

### <a name="modify-the-format-to-evaluate-the-list-of-collected-tax-values"></a>修改格式以评估所收集的税值列表

1. 在 **格式设计器** 页面上的 **格式** 选项卡上，选择 **报表\\行\\记录 \\RunningTotal** 数值格式元素，然后按照以下步骤操作：

    1. 在 **数字类型** 字段中，将值从 **实时** 更改为 **整数**。
    2. 在 **数值格式** 字段中，将值从 **F2** 更改为 **F0**。

3. 在 **映射** 选项卡上，选择 **编辑公式**。
4. 在 **公式设计器** 页上，执行以下步骤：

    1. 在 **公式** 字段中，输入 `COUNT(CollectedTaxValues.Result)`。
    2. 保存更改并关闭页面。

    > [!NOTE]
    > 新绑定会将收集税金值的列表中的记录数传递到生成的文档中。

5. 选择 **保存**，然后选择 **运行**。
6. 在 **电子申报参数** 对话框中，选择 **确定**。
7. 下载并查看 Web 浏览器提供的文件。

    ![包含其他已修改格式执行结果的已下载文件](./media/er-data-collection-data-sources-04.png)

## <a name="frequently-asked-questions"></a>常见问题解答

### <a name="if-i-have-to-calculate-running-totals-and-collect-data-what-is-the-difference-between-using-a-data-collection-data-source-and-using-the-built-in-data-collection-functions"></a>如果必须计算累计总和并收集数据，则使用数据集合数据源与使用内置数据集合功能有什么区别？

数据集合数据源和内置[数据集合](er-functions-category-data-collection.md)函数均可根据传递到所生成出站文档的信息用于数据收集、求和以及盘点。 但是，当您尝试决定要使用哪种技术时，您必须考虑以下几点。

| 数据源 | 内置函数 |
|-------------| ------------------ |
| 仅收集值。 | <p>收集指定的值。 因此，可以为单独的值组计算合计。</p><p>此外，可将组作为列表提取。</p><p>也可以收集文本值。</p> |
| 将自动收集唯一值。 | 需要其他设置才能从收集的值中提取唯一值的列表。 |
| 性能取决于所收集值的数量。 | 实际上，性能并不取决于所收集值的数量。 |
| 此技术适用于所有类型的出站文档。 | 此技术仅适用于文本和 XML 文档。 |

## <a name="additional-resources"></a>其他资源

- [配置格式以执行计数和合计](./tasks/er-format-counting-summing-1.md)
- [推迟执行电子报告格式的序列元素](er-defer-sequence-element.md#Example)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
