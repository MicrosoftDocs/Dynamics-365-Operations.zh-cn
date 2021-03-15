---
title: 更新业务文档模板的结构
description: 本主题说明如何通过使用“业务文档管理”功能更新业务文档模板的结构。
author: NickSelin
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-12-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: cb0188e372b5f6275472cf040d10bb796eed1858
ms.sourcegitcommit: 95d2fc0fa7d17d3a96f7969f12c985b018b4ff94
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/12/2020
ms.locfileid: "4728081"
---
# <a name="update-the-structure-of-a-business-document-template"></a>更新业务文档模板的结构 

[!include[banner](../includes/banner.md)]

在 [业务文档管理](er-business-document-management.md)模板编辑器的 **摸板结构** 窗格中，可以通过在 Microsoft Excel 中向模板[添加新字段](er-bdm-add-field-to-excel-template.md)来修改业务文档模板。 然后，在 Dynamics 365 Finance 中自动更新模板的结构，以使其反映您在 **模板结构** 窗格中进行的更改。

您还可以通过使用 Office 365 在线功能修改模板。 例如，您可以将新的命名项目（例如图片或形状）添加到可编辑工作表中。 在这种情况下，模板的结构不会在 Finance 中自动更新，并且您添加的项目不会出现在 **模板结构** 窗格中。 通过选择模板编辑器页面中的 **更新结构**，在 Finance 中更新摸板结构。

有关此功能的详细信息，请完成以下示例。

## <a name="example-update-the-structure-of-a-business-document-template"></a>示例：更新业务文档模板的结构

此示例显示在 Office Online 中修改了模板之后，系统管理员如何在 Finance 中更新业务文档模板的结构。 以下各节说明了其中涉及的步骤。

### <a name="prepare-a-business-document-template-for-editing"></a>准备要编辑的业务文档模板

完成[业务文档管理概述](er-business-document-management.md)中的以下过程。

1. [配置 ER 参数](er-business-document-management.md#configure-er-parameters)
2. [导入 ER 解决方案](er-business-document-management.md#import-er-solutions)
3. [启用业务文档管理](er-business-document-management.md#enable-business-document-management)
4. [配置参数](er-business-document-management.md#configure-parameters)

### <a name="edit-a-business-document-template"></a>编辑业务文档模板

1. 在 **业务文档管理** 工作区中，选择 **新建文档**。
2. 在 **创建新模板** 页面上，选择 **普通发票(ER 示例)(Excel)** 模板。
3. 选择 **创建文档**。
4. 在 **标题** 字段中，输入 **FTI sample Litware**。
5. 选择 **确定** 创建新模板。

    > [!NOTE]
    > 如果您尚未登录 Office Online，将把您[定向到 Office 365 登录页面](er-business-document-management.md#frequently-asked-questions)。 要返回 Finance 环境，请在浏览器中选择 **后退** 按钮。

    将打开新模板，以便在模板编辑器页面上的 Excel Online 嵌入式控件中进行编辑。

[![使用业务文档管理工作区开始编辑业务文档模板](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)

### <a name="review-the-current-structure-of-the-editable-template"></a>查看可编辑模板的当前结构

1. 在 Excel Online 中的功能区上 **视图** 选项卡中 **显示** 组内，选择 **网格线**。
2. 在可编辑模板中，选择模板标题上方的矩形。 这个矩形是一张名为 **rptHeaderCompLogo** 的图片。
3. 如果 **模板结构** 窗格已隐藏，请选择 **显示结构**。
4. 在 **模板结构** 窗格中，展开 **报表 \> 发票 \> rptHeader \> rptHeaderPart1**。
5. 请注意，在 Finance 中的模板结构中，**rptHeaderCompLogo** 项表示为 **报表 \> 发票 \> rptHeader \> rptHeaderPart1** 的一个子项。

[![使用业务文档管理工作区查看可编辑模板的当前结构](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)

### <a name="update-the-structure-of-a-business-document-template-by-deleting-a-picture"></a>通过删除图片更新业务文档模板的结构

1. 在 Excel Online 中的可编辑模板中，选择 **rptHeaderCompLogo** 图片。
2. 请按照以下步骤之一从可编辑模板中删除所选图片：

    - 选择键盘上的 **Delete** 键。
    - 选择并按住（或右键单击）图片，然后选择 **剪切**。

    > [!NOTE]
    > **rptHeaderCompLogo** 项现在仍然留在 Finance 中的模板结构中，虽然 Excel 模板中不再包含此图片。

3. 选择 **更新结构** 同步 Excel 和 Finance 中的可编辑模板结构。
4. 在 **模板结构** 窗格中，展开 **报表 \> 发票 \> rptHeader \> rptHeaderPart1**。
5. 请注意，Finance 中的模板结构中不再包含 **rptHeaderCompLogo** 项。

[![使用业务文档管理工作区从业务文档模板删除图片](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)

### <a name="update-the-structure-of-a-business-document-template-by-adding-a-picture"></a>通过添加图片更新业务文档模板的结构

1. 在 Excel Online 中的功能区上 **插入** 选项卡中 **示意图** 组内，选择 **图片**。
2. 选择 **选择文件**，浏览到要添加的图像，选择它，然后选择 **确定**。
3. 选择 **插入**。
4. 移动新图片，直到到达正确位置。 默认情况下，Excel 会为该图片命名。 例如，它可能将此图片命名为 **Picture 2**。
5. 选择 **更新结构** 同步 Excel 和 Finance 中的可编辑模板结构。
6. 在 **模板结构** 窗格中，展开 **报表 \> 发票 \> rptHeader \> rptHeaderPart1**。
7. 请注意，Finance 中的模板结构中现在包含这个新图片，形式为一个项。

[![使用业务文档管理工作区向业务文档模板添加图片](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)

## <a name="related-links"></a>相关链接

[电子报告 (ER) 概览](general-electronic-reporting.md)

[业务文档管理概览](er-business-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]