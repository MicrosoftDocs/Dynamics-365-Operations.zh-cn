---
title: 设计电子报告格式以将行保持在同一 Excel 页面上
description: 本文说明如何设计一种电子报告 (ER) 格式，将行保持在同一 Microsoft Excel 页面上。
author: kfend
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2022-03-01
ms.dyn365.ops.version: Version 10.0.26
ms.custom: 220314
ms.assetid: ''
ms.search.form: EROperationDesigner
ms.openlocfilehash: 7ecc4358a0d4d9ae9e729393bd3ac4cefbf15ad2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287949"
---
# <a name="design-an-er-format-to-keep-rows-together-on-the-same-excel-page"></a>设计电子报告格式以将行保持在同一 Excel 页面上

[!include [banner](../includes/banner.md)]


本文说明系统管理员或电子报告功能顾问角色的用户如何配置[电子报告 (ER)](general-electronic-reporting.md) [格式](er-overview-components.md#format-component)，以在 Microsoft Excel 中生成传出文档并管理文档分页，以让创建的行保持在同一页面上。

在此示例中，您将修改 Microsoft 提供的用于在 Excel 中打印普通发票的 ER 格式。 您的修改将使您能够管理生成的普通发票报表的分页，以尽可能将单个发票行的所有行保持在同一页面上。

本文中的过程可以在 **USMF** 公司完成。 无需进行编码。

在此示例中，将为示例公司 **Litware, Inc.** 创建所需 ER [配置](general-electronic-reporting.md#Configuration)。 确保为 ER 框架列出了 **Litware, Inc.** (`http://www.litware.com`) 示例公司的配置提供程序，并且它被标记为 **活动**。 如果未列出此配置提供程序，或者未将其标记为 **活动** 状态，请按照[创建一个配置提供程序，并标记其为活动状态](tasks/er-configuration-provider-mark-it-active-2016-11.md)中的步骤操作。

## <a name="enter-a-new-free-text-invoice"></a>输入新的普通发票

1. 按照[创建普通发票](../../../finance/accounts-receivable/create-free-text-invoice-new.md#create-a-free-text-invoice-1)中的步骤添加普通发票。

    1. 在发票中添加一行。
    2. 为发票行添加五个注释。

    ![查看附件页面上的发票行注释。](./media/er-keep-excel-rows-together-notes.png)

2. 按照[复制行](../../../finance/accounts-receivable/create-free-text-invoice-new.md#copy-lines)中的步骤创建五个额外的发票行，以复制您在上一步中添加的发票行。

    ![查看普通发票页面上的普通发票行。](./media/er-keep-excel-rows-together-invoice.png)

## <a name="configure-the-er-framework"></a>配置 ER 框架

按照[配置电子报告框架](er-quick-start2-customize-report.md#ConfigureFramework)中的步骤设置最低限度的电子报告参数集。 在开始使用电子报告框架设计标准电子报告格式的自定义版本之前，您必须完成此设置。

## <a name="import-the-standard-er-format-configuration"></a>导入标准电子报告格式配置

按照[导入标准电子报告格式配置](er-quick-start2-customize-report.md#ImportERSolution1)中的步骤将标准电子报告配置添加到您当前的 Dynamics 365 Finance 实例。 例如，导入 **普通发票 (Excel)** 格式配置的 **252.116** 版本。 基本 **发票模型** 配置的基本版本 **252** 与所需的 **发票模型映射** 配置一起自动从存储库中导入。

## <a name="set-up-print-management-to-use-the-standard-er-format"></a>设置打印管理以使用标准 ER 格式

按照 [设置打印管理](er-embed-images-header-footer-excel-reports.md#ConfigurePrintManagement1)中的步骤为 **应收帐款** 模块配置打印管理，以使用标准 ER 格式打印普通发票。

## <a name="configure-a-format-destination-for-the-standard-er-format"></a>为标准 ER 格式配置格式目标

按照[为屏幕预览配置格式目标](er-quick-start1-new-solution.md#ConfigureDestination)中的步骤配置标准 ER 格式的[屏幕](er-destination-type-screen.md) ER 目标，以将生成的报表转换为 PDF 格式并在新的浏览器选项卡上预览。

## <a name="print-a-free-text-invoice-by-using-the-standard-er-format"></a>使用标准 ER 格式打印普通发票

1. 按照[打印普通发票](er-embed-images-header-footer-excel-reports.md#ProcessInvoice1)中的步骤使用标准 ER 格式为添加的发票生成 Excel 格式的普通发票报表。
2. 下载生成的 Excel 工作簿，在 Excel 桌面应用程序中进行查看。

    请注意，发票的第六行从报表的第一页开始，在第二页继续。 最后一个注释出现在第二页，没有明显显示它属于第六发票行。 因此，发票行内容中间的分页符使此单据更难阅读。

    ![在 Excel 桌面应用程序中查看生成的普通发票的分页。](./media/er-keep-excel-rows-together-invoice1.gif)

本文中的其余过程展示了如何调整标准 ER 格式，以通过将单个发票行的所有内容保留在同一页面上来改进发票报表的外观和可读性。

## <a name="create-a-custom-format"></a>创建自定义格式

按照 [创建自定义格式](er-embed-images-header-footer-excel-reports.md#DeriveProvidedFormat)中的步骤从导入的 ER 格式派生格式，并创建可进行编辑和修改的 **普通发票 (Excel) 自定义** ER 配置。

## <a name="edit-the-custom-format"></a>编辑自定义格式

1. 按照[创建自定义格式](er-embed-images-header-footer-excel-reports.md#ConfigureDerivedFormat)中的步骤打开派生的 ER 格式以在 ER 格式设计器中进行编辑。
2. 在 **格式设计器** 页面，在左侧窗格的格式组件树中，展开 **普通发票 \> 工作表 \> InvoiceLines**，选择 **InvoiceLines_Values** 组件。
3. 在 **格式** 选项卡上，将 **行保持在一起** 选项设置为 **是**。

    ![在格式设计器页面上为可编辑的 ER 格式设置“行保持在一起”选项。](./media/er-keep-excel-rows-together-format.png)

4. 选择 **保存**，然后关闭页面。

## <a name="mark-the-custom-format-as-runnable"></a>将自定义格式标记为可运行

按照[将自定义格式标记为可运行](er-embed-images-header-footer-excel-reports.md#MarkFormatRunnable)中的步骤，使修改后的自定义 ER 格式版本可运行。

## <a name="set-up-print-management-to-use-the-custom-er-format"></a>设置打印管理以使用自定义 ER 格式

按照 [设置打印管理](er-embed-images-header-footer-excel-reports.md#ConfigurePrintManagement2)中的步骤为 **应收帐款** 模块配置打印管理，以使用自定义 ER 格式打印普通发票。

## <a name="configure-a-format-destination-for-the-custom-er-format"></a>为自定义 ER 格式配置格式目标

按照 [为屏幕预览配置格式目标](er-quick-start1-new-solution.md#ConfigureDestination)中的步骤配置自定义 ER 格式的 **屏幕** ER 目标，以将生成的报表转换为 PDF 格式并在新的浏览器选项卡上预览。

## <a name="print-a-free-text-invoice-by-using-the-custom-er-format"></a>使用自定义 ER 格式打印普通发票

1. 按照[打印普通发票](er-embed-images-header-footer-excel-reports.md#ProcessInvoice2)中的步骤使用自定义 ER 格式为添加的发票生成 Excel 格式的普通发票报表。
2. 下载生成的 Excel 工作簿，在 Excel 桌面应用程序中进行查看。

    请注意，发票的第六行从第二页开始，代表此发票行的所有 Excel 行会一起出现在该页上。

    ![在 Excel 桌面应用程序中查看更新后的生成的普通发票的分页。](./media/er-keep-excel-rows-together-invoice2.gif)

## <a name="additional-resources"></a>其他资源

[设计配置以生成 Excel 格式的文档](er-fillable-excel.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
