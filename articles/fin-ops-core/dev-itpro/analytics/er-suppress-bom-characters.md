---
title: 设计 ER 配置以在生成的文件中禁止 BOM 字符
description: 本文说明如何配置电子报告 (ER) 格式以生成禁止字节顺序标记 (BOM) 字符的报表。
author: kfend
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: EROperationDesigner
ms.openlocfilehash: a2ea132b51f2f451fbe81a9c7869bea84bf4017a
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2022
ms.locfileid: "9324010"
---
# <a name="design-er-configurations-to-suppress-bom-characters-in-generated-files"></a>设计 ER 配置以在生成的文件中禁止 BOM 字符

[!include [banner](../includes/banner.md)]

可以设计[电子报告 (ER)](general-electronic-reporting.md) [解决方案](er-quick-start1-new-solution.md)来生成传出文档。 要将文档生成为文本文件或 XML 文件，解决方案必须包括包含 ER 格式组件的 ER [配置](general-electronic-reporting.md#Configuration)。 若要指定表示生成文件中字符集的 [字符编码](/windows/win32/intl/character-sets)，ER 格式必须包含 **Common\\File** 格式元素。 要配置 ER 格式组件，在 ER 格式设计器中打开 ER 配置的草稿版本，添加 **Common\\File** 元素。 在 **编码** 字段中，指定使用此组件在运行时生成的传出文件的编码。

> [!NOTE]
> 如果格式包含错误的编码名称，将更改保存到格式设置时会引发错误。

![在“格式设计器”页面上添加根元素。](./media/er-suppress-bom-characters-image1.gif)

如果您指定 **UTF-8**、**UTF-16** 或 **UTF-32** 作为编码，**禁止 BOM 表字符** 选项将变为可用。 将此选项设置为 **是**，将禁止在可编辑 ER 格式运行时在运行时生成的传出文件中的[字节顺序标记 (BOM) 字符](/globalization/encoding/byte-order-mark)。

> [!NOTE]
> 如果将 **编码** 字段留空，将使用默认的 **UTF-8** 编码。

![在“格式设计器”页面上设置“禁止物料清单字符”选项。](./media/er-suppress-bom-characters-image2.gif)

要在运行时查看功能，请完成相应的过程。 例如，完成[推迟执行 ER 格式的 XML 元素](er-defer-xml-element.md)一文中的步骤。 完成该文章的[修改格式，以便根据生成的输出来进行计算](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output)一节中的步骤后，请执行以下其他步骤。

1. 指定 UTF 编码：

    1. 选择 **Common\\File** 类型的 **报表** 元素。
    2. 在 **编码** 字段中，指定 **UTF-8** 编码。

2. 生成包含 BOM 字符的 XML 文件：

    1. 将 **禁止 BOM 字符** 选项设置为 **否** 以在生成的 XML 文件中包含 BOM 字符。
    2. 完成 [推迟执行 ER 格式的 XML 元素](er-defer-xml-element.md)一文的 [推迟执行汇总 XML 元素，以便使用计算出的总和](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used)一节中的步骤，并将生成的文件另存为 **SampleXmlReport.xml**。

3. 生成不包含 BOM 字符的 XML 文件：

    1. 将 **禁止 BOM 字符** 选项设置为 **是** 以在生成的 XML 文件中禁止 BOM 字符。
    2. 完成 [推迟执行 ER 格式的 XML 元素](er-defer-xml-element.md)一文的 [推迟执行汇总 XML 元素，以便使用计算出的总和](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used)一节中的步骤，并将生成的文件另存为 **SampleXmlReport (1).xml**。

4. 在文件比较实用程序中，比较生成的文件。

    您将注意到的第一个区别是在文件标题中。 SampleXmlReport.xml 文件包含 BOM 字符，而 SampleXmlReport (1).xml 文件不包含。

    ![使用文件比较实用程序比较生成的文件。](./media/er-suppress-bom-characters-image3.png)

## <a name="see-also"></a>请参阅

- [推迟执行电子报告格式的 XML 元素](er-defer-xml-element.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
