---
title: 业务文档管理中的 Microsoft Office 样式用户界面（包含视频）
description: 本文说明如何在电子报告 (ER) 框架的业务文档管理功能中使用新用户界面。
author: v-anamir
ms.date: 01/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 208cfc91f11d4893785538ce4874e85a5725e993
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/01/2022
ms.locfileid: "9109251"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a>业务文档管理中的 Microsoft Office 样式用户界面

[!include [banner](../includes/banner.md)]

业务文档管理使业务用户可以使用 Microsoft Office 365 服务或相应的 Microsoft Office 桌面应用程序来编辑业务文档模板。 编辑可能包括设计更改或新部署，或者用户可能会添加占位符以包含其他数据，而不必更改源代码。 有关如何使用业务文档管理的更多信息，请参见[业务文档管理概述](er-business-document-management.md)。

新用户界面 (UI) 更清晰，使用起来更舒适。 **业务文档** 区域仅显示当前[活动](tasks/er-configuration-provider-mark-it-active-2016-11.md)的[提供程序](general-electronic-reporting.md#Provider)负责的位于 Dynamics 365 Finance 的当前实例中的模板。 在上一个 UI 中，**模板** 选项卡列出了可用于任何提供程序的所有模板。 它还显示了由具有相同角色的任何用户创建和编辑的所有模板。

您可以使用 **业务文档管理** 工作区中的 **新建文档** 按钮在[电子报告 (ER)](general-electronic-reporting.md) 格式[配置](general-electronic-reporting.md#Configuration)中创建和编辑由其他提供程序提供、位于当前 Finance 实例中的模板，或从 Excel 工作簿上载新模板。 此外，在版本 10.0.25 及更高版本中，您可以使用 **新建文档** 按钮以存储在[全局存储库](general-electronic-reporting.md#Repository)中的 ER 格式配置创建和编辑模板。

在本文中的示例中，活动提供程序是 Contoso，您使用它创建基于 Microsoft 提供的模板的模板。 或者，您可以通过以 Excel 格式上传自己的模板来创建模板。

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RWAVQg]

[使用业务文档管理创建新业务文档](https://youtu.be/gAIYl-mM_pw)视频（如上所示）包含在 YouTube 上可用的[财务和运营播放列表](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW)中。

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>使业务文档管理中的新文档 UI 可用

要开始使用业务文档管理中的新文档 UI，必须打开 **功能管理** 工作区中的 **类似于 Office 的业务文档管理 UI 体验** 功能。

请按照以下步骤为所有法人启用此功能。

1. 在 **功能管理** 工作区中的 **所有** 选项卡上，选择列表中的 **类似于 Office 的业务文档管理 UI 体验** 功能。
2. 选择 **立即启用** 以打开所选功能。
3. 刷新页面以访问新功能。

## <a name="add-or-activate-a-provider"></a>添加或激活提供程序

业务文档的每个模板存储在电子报告格式配置，该配置标记为由特定配置提供程序负责。 创建新模板时，将创建新的 ER 格式配置来保留该模板。 因此，必须为该配置确定提供程序。 ER 框架的活动提供程序用于此目的。 如果 ER 中没有提供程序，您可以创建一个。 如果没有 *活动* 提供程序，您可以激活现有提供程序中的一个。 在需要时用于添加或激活提供程序的对话将打开，您在那里开始添加新模板。

### <a name="add-a-new-provider"></a>添加新提供程序

要创建新提供程序，在 **配置提供程序** 对话上执行以下步骤：

1.  在 **选择配置提供程序** 选项卡上，在 **名称** 字段中输入新提供程序的名称。
2.  在 **Internet 地址** 字段中，输入新提供程序的 Internet 地址 (URL)。 
3.  选择 **确定**。

    ![在业务文档管理中创建新提供程序。](./media/bdm_create_provider.png)

添加的提供程序将自动激活。

### <a name="activate-a-provider"></a>激活提供程序

要激活提供程序，在 **配置提供程序** 对话上执行以下步骤：

1.  在 **选择配置提供程序** 选项卡上，在 **配置提供程序** 字段中选择提供程序。
2.  选择 **确定**。

    ![在业务文档管理中激活提供程序。](./media/bdm_choose_provider.png)

所选择的提供程序将被激活。

> [!NOTE]
> 每个业务文档管理模板位于 ER 格式配置中，该配置将提供程序称为配置作者。 因此，每个模板都需要一个活动的提供程序。

## <a name="edit-a-template-that-is-owned-by-another-provider"></a>编辑归其他提供程序所有的模板

此示例显示如何使用 **业务文档管理** 工作区中的 **新建文档** 按钮在 ER 格式配置中创建和编辑由其他提供程序提供、位于当前 Finance 实例中的模板。 在此示例中，活动提供程序是 Contoso，它使用 Microsoft 提供的 ER 格式配置。 选择 **新建文档** 后，**创建新模板** 页面上的 **选择** 选项卡将显示当前 Finance 实例的归当前提供程序和其他提提供程序所有的全部模板。 选择一个模板将其打开。 然后，您可以创建一个新的可编辑的模板副本。 编辑后的模板将存储在自动生成的新 ER 格式配置中。

1. 在 **业务文档管理** 工作区中，选择 **新建文档**。

    ![业务文档管理工作区。](./media/BDM_overview_new_template1.png)

2. 在 **创建新模板** 页面上，在 **选择** 选项卡上，选择要用作模板的文档，然后选择 **创建文档**。

    ![业务文档对话框。](./media/BDM_overview_new_template2.png)

3. 在此新对话框内的 **标题** 字段中，根据需要更改标题。 标题文本用于命名自动创建的新 ER 格式配置。 此配置 (**Customer FTI report (GER) Copy**) 的草稿版本将包含编辑的模板，并且将用于为当前用户运行此 ER 格式。 将使用来自基本 ER 格式配置的原始模板为每个其他用户运行此 ER 格式。
4. 在 **名称** 字段中，更改将自动创建的可编辑模板第一个修订的名称。
5. 在 **注释** 字段中，更新有关将自动创建的可编辑模板的修订注解。
6. 选择 **确定** 以确认开始执行编辑流程。

    ![文档创建对话框。](./media/BDM_overview_new_template3.png)

## <a name="upload-a-template-that-uses-an-existing-excel-workbook"></a>上载使用现有 Excel 工作簿的模板

此示例显示如何使用 **业务文档管理** 工作区中的 **新建文档** 按钮基于可用 Excel 工作簿在 ER 格式配置中创建和编辑模板。 在此示例中，活动提供程序是 Contoso，您使用 Microsoft 提供的 ER [数据模型](er-overview-components.md#data-model-component)和 ER [模型映射](er-overview-components.md#model-mapping-component)配置。 选择 **新建文档** 后，在 **创建新模板** 页面上选择 **上载** 选项卡。 在那里，您可以指定 Excel 工作簿上载的详细信息。 上载 Excel 工作簿后，它将转换为已经打开以进行编辑的业务文档模板。 编辑后的模板将存储在自动生成的新 ER 格式配置中。

在上传模板之前，请按照以下步骤提供所需信息。

1. 在 **业务文档管理** 工作区中，选择 **新建文档**。
2. 在 **创建新模板** 页面上，在 **上传** 选项卡的 **模板** 选项卡上，选择 **浏览** 以查找并选择要用作模板的 Excel 文件。 在 **模板** 部分中，将自动填写 **标题** 和 **描述** 字段。 它们指定自动创建的新 ER 格式配置的名称和描述。 可以根据需要编辑这些字段。
3. 在 **文档类型** 部分中，在 **名称** 字段中，指定业务文档的类型。 该值将用于搜索正确的数据源（即 ER 模型配置）。

    ![“创建新模板”页面的“上载”选项卡上的“模板”选项卡。](./media/BDM_overview_new_UI_import_21.jpg)

4. 在 **数据源** 选项卡上，在 **筛选器** 快速选项卡上，选择 **应用筛选器**。 在 **数据源** 部分中，自动填写 **名称** 字段，或者您可以手动选择值。 您可以使用筛选器按名称、描述、国家/地区代码和业务文档类型搜索适当的数据源名称。

    ![“创建新模板”页面的“上载”选项卡上的“数据源”选项卡。](./media/BDM_overview_new_UI_import_31.jpg)

    > [!NOTE]
    > **筛选器** 快速选项卡用于搜索正确的数据源（即 ER 模型配置）。 您可以编辑所有筛选器字段，以找到最适合您上传的文档的数据源。
    > 
    > 使用 **筛选器** 快速选项卡上的条件作为 **OR** 条件。

5. 在 **映射** 选项卡上，选择 **自动检测**。 自动填写 **根定义** 字段，或者您可以手动选择值。 此选项卡显示模板和模型中元素的最终映射。

    ![“创建新模板”页面的“上载”选项卡上的“映射”选项卡。](./media/BDM_overview_new_UI_import_41.jpg)

    > [!NOTE]
    > **模板结构** 部分中的映射使用用户语言的数据源和模板的单元格名称中的标签或描述的完全匹配。

6. 选择 **创建文档** 以确认您要创建模板并开始编辑流程。

有关更多信息，请参见[业务文档管理概述](er-business-document-management.md)。

## <a name="upload-a-template-from-the-global-repository"></a>从全局存储库上载模板

此示例显示如何使用 **业务文档管理** 工作区中的 **新建文档** 按钮在 ER 格式配置中创建和编辑由 Microsoft 提供、位于全局存储库中的模板。 在此示例中，活动提供程序是 Contoso，它使用 Microsoft 提供的 ER 格式配置。 选择 **新建文档** 后，**创建新模板** 页面上的 **从全局存储库导入** 选项卡将显示存储在全局存储库中但当前 Finance 实例中缺少的所有业务文档模板。 选择模板后，该模板将被从全局存储库导入到当前 Finance 实例中，以创建新的可编辑副本。 编辑后的模板将存储在自动生成的新 ER 格式配置中。

1. 在 **业务文档管理** 工作区中，选择 **新建文档**。
2. 在 **创建新模板** 页面上，在 **从全局存储库导入** 选项卡上，选择要用作模板的文档，然后选择 **创建文档**。

    ![“创建新模板”页面上的“从全局存储库导入”选项卡。](./media/BDM_overview_new_template22.png)

3. 在消息框中，选择 **是** 确认您要将所选文档从全局存储库导入到当前 Finance 实例中。 如果系统提示您提供授权，请按照屏幕上的说明操作。
4. 在此新对话框内的 **标题** 字段中，根据需要更改标题。 标题文本用于命名自动创建的新 ER 格式配置。 此配置（**催款单 (Excel) 副本**）的草稿版本将包含编辑的模板，并且将用于为当前用户运行此 ER 格式。 将使用来自基本 ER 格式配置的原始模板为每个其他用户运行此 ER 格式。
5. 在 **名称** 字段中，更改将自动创建的可编辑模板第一个修订的名称。
6. 在 **注释** 字段中，更新有关将自动创建的可编辑模板的修订注解。
7. 选择 **确定** 以确认开始执行编辑流程。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

