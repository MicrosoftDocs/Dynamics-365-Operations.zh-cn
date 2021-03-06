---
title: 打印机 ER 目标类型
description: 本主题说明如何为电子报告 (ER) 格式的每个文件夹或文件组件配置打印机目标。
author: NickSelin
ms.date: 02/24/2021
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
ms.openlocfilehash: 7749a458020de664d00e81ccf0e480ae459da617
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893996"
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

[![在功能管理中打开 ER 打印机目标功能](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)

### <a name="applicability"></a>适用性

只能对用于以可打印 PDF 格式（PDF 合并器或 PDF 文件格式元素）或 Microsoft Office Excel/Word 格式（Excel 文件）生成输出的文件组件配置 **打印机** 目标。 以 PDF 格式生成输出时，会将其发送到打印机。 以 Microsoft Office 格式生成输出时，它会自动转换为 PDF 格式，然后发送到打印机。

### <a name="limitations"></a>限制

系统仅针对云部署实施了 **打印机** 目标。

### <a name="use-the-printer-destination"></a>使用打印机目标

1. 将 **已启用** 选项设置为 **是** 以将生成的文档发送到打印机。
2. 在 **打印机名称** 字段中，选择所需的网络打印机。
3. 将 **是否在打印存档文件中保存?** 设置为 **是**，以将生成的输出存储在打印存档文件中，以便将来可以进行打印。 要稍后访问存档的输出，请转到 **组织管理** \> **查询和报告** \> **报表存档**。

[![使用打印机目标](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)

> [!NOTE]
> 如果配置 **打印机** 目标，则不必打开 **转换成 PDF** 选项。 即使关闭该选项，也会进行用于打印用途的 PDF 转换。

要在以 Excel 格式打印传出文档时使用特定的 [页面方向](electronic-reporting-destinations.md#SelectPdfPageOrientation)，必须打开 **转换为 PDF** 选项。 当您将 **转换为 PDF** 选项设置为 **是** 时，**页面方向** 字段将可用。 在 **页面方向** 字段中，您可以选择页面方向。

## <a name="additional-resources"></a>其他资源

- [电子报告 (ER) 概览](general-electronic-reporting.md)
- [电子报告 (ER) 目标](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]