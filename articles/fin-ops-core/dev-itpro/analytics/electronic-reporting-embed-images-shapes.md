---
title: 使用 ER 在您生成的文档中嵌入图像和形状
description: 本文说明如何使用电子报告工具生成具有嵌入图像和形状的业务文档。
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: fe0e6d6def50670566f44cfb5cd6bb4abe5faf15
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851039"
---
# <a name="embed-images-and-shapes-in-documents-that-you-generate-by-using-er"></a>使用 ER 在您生成的文档中嵌入图像和形状

[!include [banner](../includes/banner.md)]

您可以使用电子报告 (ER) 工具设计可运行以生成所需电子文档的报表。 您可以使用 Microsoft Excel 或 Microsoft Word 文档指定报表的布局。 ER 操作设计器使您可以将 Excel 或 Word 文档附加为报表的模板。 附加模板中的命名元素与 ER 报表的格式元素相关联。 报表的格式元素将绑定到数据源。 这些元素指定在运行时将在生成的文档中输入的数据。

此新功能超越了用于采用 Microsoft Office 格式创建文档的现有 ER 功能。 有关详细信息，请参阅以下任务指南。 您可以在 7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677) 业务流程下找到这些任务指南。

- ER 设计以 OPENXML 格式生成报表的配置
- ER 设计用于生成 Microsoft WORD 格式的报表的配置

## <a name="embed-an-image-in-an-excel-document"></a>在 Excel 文档中嵌入图像

### <a name="embed-an-image-in-an-excel-worksheet"></a>在 Excel 工作表中嵌入图像

首先，您必须为 Excel 文档中的图像添加占位符。 打开 Excel 工作簿，然后添加图片作为稍后将添加的图像的占位符。 然后，使用 ER 工具添加新的 ER 格式配置以包含您正在设计的报表。 将 Excel 工作薄附加为报表格式的模板，然后将工作薄的内容导入为 ER 格式。 格式定义将自动创建。 您添加的图像占位符将作为 **CELL** 元素包括在 ER 格式定义中。

> [!NOTE]
> 您可以手动指定格式定义，而不是导入它。 保存更改时，将验证格式。

接下来，将 ER 格式的 **CELL** 元素绑定到在运行时以二进制格式提供图片数据的格式数据源中的字段。 当将 ER 数据模型用作格式的数据源时，字段的数据类型必须是[容器](er-formula-supported-data-types-composite.md#container)。 当前，具有[容器](er-formula-supported-data-types-composite.md#container)数据类型的 ER 数据模型字段可以绑定到以二进制格式返回图像的几种类型的数据源。 您可以使用文档管理框架访问数据表中的字段和附加到数据表记录的文件。

> [!IMPORTANT]
> - 如果要在使用 Excel 模板创建的文档中填充图像占位符，ER 格式必须包含引用 Excel 模板中命名图片元素的 **CELL** 元素。 否则，报表的输出中将不会显示图像占位符。 如果 **CELL** 元素的绑定在运行时不返回任何数据，生成的文档将显示模板中的图像占位符。 若要在您生成的文档中隐藏图像，请定义 **CELL** 元素，然后指定 **启用** 表达式应返回 **FALSE** 值。
> - 在 Excel 模板中，为每个元素使用唯一名称。 这些元素包括图片和单元格。 如果元素名称重复，则生成的报表内容将不明确且令人困惑。

### <a name="embed-images-in-the-header-and-footer-of-an-excel-worksheet"></a>在 Excel 工作表的页眉和页脚中嵌入图像

使用 Excel 工作簿文档作为模板来指定报表的布局。 工作簿可以包含多个工作表，每个工作表都可以设计为具有页眉和页脚。 Excel 在每个工作表的页眉和页脚中最多支持三个图像。 图像可以左对齐、右对齐或居中对齐。

在 Finance 版本 10.0.21 中，您可以管理由具有 Excel 模板的 ER 解决方案生成的页眉和页脚图像。

如果您希望在生成文档的页眉或页脚中显示默认图片，可以在 ER 模板的工作表的页眉或页脚中添加图像。 若要访问采用 ER 格式的此图像，必须在格式的 [页眉](er-fillable-excel.md#header-component)或 [页脚](er-fillable-excel.md#footer-component)组件下添加 **图片** 组件。 根据需要配置 **图片** 组件的对齐方式。 

您还可以使用 **图片** 组件在运行时将图像放入生成文档的页眉或页脚中，即使模板不包含默认图像。 若要将应放入生成文档的页面或页脚中的媒体内容指定为新图像或默认图像的替代，必须将 **图片** 组件绑定到以二进制格式表示图像的[容器](er-formula-supported-data-types-composite.md#container)类型的数据源。

对于每个支持的对齐方式，每个 **页眉** 或 **页脚** 组件可以保留一个 **图片** 组件：**左对齐**、**居中对齐** 和 **右对齐**。

**图片** 组件的 **缩放高度** 属性允许您使用配置的绑定控制图像的大小：

- 选择 **原始** 以保持图像的初始大小。
- 选择 **相对** 以按比例将图像的高度缩放为保留该图像的页面或页脚的高度。

    - 在这种情况下，图像的高度必须定义为父页眉或页脚的百分比。
    - 如果缩放值超过 100%，图像可能会与相应工作表的数据区域重叠。
    - 如果在应用缩放时更改图像的高度，宽度也会更改以保持图像的原始纵横比。

- 选择 **绝对** 以根据在设计时提供的高度和宽度值（以像素为单位）调整图像大小。

    - 如果指定的高度超过父页眉或页脚的高度，则图像可能与相应工作表的数据区域重叠。

您还可以使用 **图片** 组件的 **已启用** 属性，控制使用此组件放入生成文档中的图像的可见性。

> [!NOTE]
> 您必须使用 ER 格式设计器将 **图片** 组件添加到可编辑 ER 格式。 当使用[业务文档管理](er-business-document-management.md)工作区编辑业务文档的模板时，不能添加组件。

若要了解有关此功能的详细信息，请按照[设计 ER 格式以使用页面页眉或页脚中的嵌入图像生成采用 Excel 格式的报表](er-embed-images-header-footer-excel-reports.md)中的步骤操作。

## <a name="embed-a-shape-in-an-excel-document"></a>在 Excel 文档中嵌入形状

首先，您必须为 Excel 文档中的形状添加占位符。 打开 Excel 工作簿，然后选择 **形状**、**文本框** 或 **艺术字** 作为形状的占位符。 然后，使用 ER 工具添加新的 ER 格式配置以包含您正在设计的报表。 将 Excel 工作薄附加为报表格式的模板，然后将工作薄的内容导入为 ER 格式。 格式定义将自动创建。 您添加的形状占位符将包含在 ER 格式定义中，以作为引用命名 Excel 形状元素的 **CELL** 元素。

> [!NOTE]
> 您可以手动指定格式定义，而不是导入它。 保存更改时，将验证格式。

接下来，将采用 ER 格式的 **CELL** 元素绑定到在运行时提供数据的格式数据源中的字段。 此数据可以转换为文本字符串。 当采用 ER 格式的 **CELL** 元素引用 Excel 模板中支持文本的形状元素时，在运行时通过此绑定提供的文本将显示在生成的文档的形状中。

> [!IMPORTANT]
> - 如果要使用包含形状占位符的 Excel 模板生成新文档，ER 格式必须包含引用 Excel 形状元素的 **CELL** 元素。 否则，报表的输出中将不会显示形状占位符。 如果引用命名 Excel 形状元素的 **CELL** 元素的绑定在运行时不返回任何数据，生成的文档将显示 Excel 模板中形状占位符的文本。 若要在您生成的文档中隐藏形状，请定义引用命名 Excel 形状的 **CELL** 元素，然后指定 **启用** 表达式应返回 **FALSE** 值。
> - 在 Excel 模板中，为每个元素使用唯一名称。 这些元素包括形状和单元格。 如果元素名称重复，则生成的报表内容将不明确且令人困惑。

## <a name="embed-an-image-in-a-word-document"></a>在 Word 文档中嵌入图像
> [!IMPORTANT]
> 您可以重复使用使用 Excel 模板的 ER 格式来创建包含嵌入图像的文档。 在 ER 格式中，确保为引用 Excel 中命名图片元素的 **CELL** 元素指定名称，并绑定到在运行时返回图片的数据源。

首先，您必须配置 Word 文档的布局。 使用 **图片内容** 控件为嵌入图像创建占位符。 若要访问此控件，您必须首先使 **开发人员** 选项卡在 Word 功能区上可见。

接下来，从 ER 格式中删除 Excel 模板，并附加 Word 模板文档。 更新对模板的引用，并保存更改。 当前 ER 格式的结构作为名为 **报表** 的新自定义 XML 部分保存到 Word 模板。

接下来，将当前 ER 格式的 Word 模板保存到本地计算机。 打开模板，然后打开 **XML 映射** 窗格。 查找名为 **报表** 的自定义 XML 部分，然后指向 ER 报表中绑定到以二进制格式返回图像的数据源的 **CELL** 元素。 将此 XML 部分的物料映射到选定 **图片内容** 控件，然后保存更改。

[![嵌入图像。](./media/embed-images-shapes-01.png)](./media/embed-images-shapes-01.png)

最后，从 ER 格式中删除 Word 模板，并附加包含映射的自定义 XML 部分的 Word 文档。 更新对模板的格式引用，并保存对此 ER 格式所做的更改。

## <a name="more-information"></a>更多信息
若要熟悉此功能的详细信息，请参阅任务指南集 **ER 创建包含嵌入图像的 MS Office 格式报表**。 这些任务指南显示如何在 Excel 和 Word 文档中使用 ER 工具生成的付款支票中嵌入公司徽标和授权人员签名的图像。

下表列出了完成 **ER 创建包含嵌入图像的 MS Office 格式报表** 任务指南所需的文件。 下载文件并将其保存到本地计算机上。

| 说明                                          | 文件名                   |
|------------------------------------------------------|-----------------------------|
| ER 数据模型配置                          | [Model for cheques.xml](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)       |
| ER 格式配置                              | [Cheques printing format.xml](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |
| 公司徽标图像                                   | [Company logo.png](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png)            |
| 签名图像                                      | [Signature image.png](https://download.microsoft.com/download/5/0/9/509151b3-06fc-4870-9408-7c9a43b72771/Signatureimage.png)         |
| 替代签名图像                          | [Signature image 2.png](https://download.microsoft.com/download/3/0/0/30045bf1-0ff6-4215-9162-b77c2f5dcc7c/Signatureimage2.png)       |
| 用于打印付款支票的 Microsoft Word 模板  | [Cheque template Word.docx](https://download.microsoft.com/download/4/4/d/44d9d255-9ad1-42fe-87db-23f319fd8e89/ChequetemplateWord.docx)   |
| 用于打印付款支票的 Microsoft Excel 模板 | [Cheque template.xlsx](https://download.microsoft.com/download/1/f/6/1f671963-73aa-48d5-ae69-45f21fe7dfb4/Cheque%20template.xlsx)        |

下图提供了从 Excel 模板生成的付款支票的测试打印输出的示例。

[![付款支票测试打印输出。](./media/embed-images-shapes-02.png)](./media/embed-images-shapes-02.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
