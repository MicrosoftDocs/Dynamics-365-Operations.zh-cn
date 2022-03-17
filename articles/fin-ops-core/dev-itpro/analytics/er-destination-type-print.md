---
title: 打印机 ER 目标类型
description: 本主题说明如何为电子报告 (ER) 格式的每个文件夹或文件组件配置打印机目标。
author: NickSelin
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 2513fc4f86519c71602089cd46e9757813b1a708
ms.sourcegitcommit: b80692c3521dad346c9cbec8ceeb9612e4e07d64
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/05/2022
ms.locfileid: "8388280"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a>打印机目标

[!include [banner](../includes/banner.md)]

您可以将生成的文档直接发送到网络打印机以进行直接打印。

## <a name="prerequisites"></a>先决条件

在开始之前，您必须安装和配置文档路线选择代理，然后注册网络打印机。 有关详细信息，请参阅[安装文档路线选择代理以启用网络打印](./install-document-routing-agent.md)。

## <a name="make-the-printer-destination-available"></a>使打印机目标可用

为了使 **打印机** 目标在 Microsoft Dynamics 365 Finance 的当前实例中可用，请转到 **功能管理** 工作区，并按以下顺序打开以下功能：

1. 将电子申报传出文档从 Microsoft Office 格式转换为 PDF
2. 将文档路线选择代理作为传出文档的电子申报目标

[![在功能管理中打开 ER 打印机目标功能。](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)

### <a name="applicability"></a>适用性

#### <a name="pdf-printing"></a>PDF 打印

在版本 10.0.18 之前的 Finance 版本中，只能对用于以可打印 PDF 格式（**PDF 合并器** 或 **PDF 文件** 格式元素）或 Microsoft Office Excel 和 Word 格式（**Excel 文件** 格式元素）生成输出的文件组件配置 **打印机** 目标。 以 PDF 格式生成输出时，会将其发送到打印机。 当使用 **Excel 文件** 格式元素以 Office 格式生成输出时，它会自动转换为 PDF 格式，然后被发送到打印机。

但是，从版本 10.0.18 开始，您可以为 **常见文件** 格式元素配置 **打印机** 目标。 此格式元素主要用于生成 TXT 或 XML 格式的输出。 您可以配置包含 **常见文件** 格式元素作为根格式元素，以及包含 **二进制内容** 格式元素作为其下唯一嵌套元素的 ER 格式。 在这种情况下，**常见文件** 格式元素将以您为 **二进制内容** 格式元素配置的绑定指定的格式生成输出。 例如，您可以将此绑定配置为用 PDF 或 Office（Excel 或 Word）格式的[文档管理](../../fin-ops/organization-administration/configure-document-management.md)附件的内容[填充](tasks/er-document-management-files-5.md#modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format)此元素。 您可以使用配置的 **打印机** 目标打印输出。 

> [!NOTE]
> 当您选择 **Common\\File** 格式元素来配置 **打印机** 目标时，无法保证在设计时所选元素会生成 PDF 格式的输出或可转换为 PDF 格式的输出。 因此，您会收到以下警告消息：“请确保所选格式组件生成的输出可以转换为 PDF。 否则，请取消选中‘转换为 PDF’选项。” 当在运行时提供非 PDF 或非 PDF 可转换输出进行打印时，您必须采取措施帮助防止出现运行时问题。 如果您预期会接收 Office（Excel 或 Word）格式的输出，则必须选择 **转换为 PDF** 选项。
>
> 在 10.0.26 及更高版本中，要使用 **转换为 PDF** 选项，您必须为配置的 **打印机** 目标的 **文档路线类型** 参数选择 **PDF**。

#### <a name="zpl-printing"></a>ZPL 打印

在 10.0.26 及更高版本中，您可以通过为 **文档路线类型** 选择 **ZPL** 来为 **Common\\File** 格式元素配置 **打印机** 目标。 在这种情况下，**转换为 PDF** 选项在运行时将被忽略，TXT 或 XML 输出将通过使用[文档路线选择代理 (DRA)](install-document-routing-agent.md) 的 Zebra 编程语言 (ZPL) 合同被直接发送到选定的打印机。 将此功能用于表示 ZPL II 标签布局的 ER 格式可以打印各种标签。

[![在目标设置对话框中设置文档路线类型参数。](./media/ER_Destinations-SetDocumentRoutingType.png)](./media/ER_Destinations-SetDocumentRoutingType.png)

有关此功能的详细信息，请参阅[设计新的 ER 解决方案打印 ZPL 标签](er-design-zpl-labels.md)。

### <a name="limitations"></a>限制

系统仅针对云部署实施了 **打印机** 目标。

### <a name="use-the-printer-destination"></a>使用打印机目标

1. 将 **已启用** 选项设置为 **是** 以将生成的文档发送到打印机。
2. 在 **打印机名称** 字段中，选择所需的网络打印机。
3. 将 **是否在打印存档文件中保存?** 设置为 **是**，以将生成的输出存储在打印存档文件中，以便将来可以进行打印。 要稍后访问存档的输出，请转到 **组织管理** \> **查询和报告** \> **报表存档**。

[![使用打印机目标。](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)

> [!NOTE]
> 如果配置 **打印机** 目标，则不必打开 **转换成 PDF** 选项。 即使关闭该选项，也会进行用于打印用途的 PDF 转换。

要在以 Excel 格式打印传出文档时使用特定的 [页面方向](electronic-reporting-destinations.md#SelectPdfPageOrientation)，必须打开 **转换为 PDF** 选项。 当您将 **转换为 PDF** 选项设置为 **是** 时，**页面方向** 字段将可用。 在 **页面方向** 字段中，您可以选择页面方向。

## <a name="additional-resources"></a>其他资源

- [电子报告 (ER) 概览](general-electronic-reporting.md)
- [电子报告 (ER) 目标](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
