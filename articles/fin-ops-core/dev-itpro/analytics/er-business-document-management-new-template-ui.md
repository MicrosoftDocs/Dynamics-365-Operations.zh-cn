---
title: 业务文档管理中的 Microsoft Office 样式用户界面
description: 本主题说明如何在电子报告 (ER) 框架的业务文档管理功能中使用新用户界面。
author: v-anamir
ms.date: 04/12/2021
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
ms.openlocfilehash: e6c5081f71a18dfac83b7aea950395436b42f50e
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881028"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a>业务文档管理中的 Microsoft Office 样式用户界面

[!include [banner](../includes/banner.md)]

业务文档管理使业务用户可以使用 Microsoft 365 服务或相应的 Microsoft Office 桌面应用程序来编辑业务文档模板。 编辑可能包括设计更改或新部署，或者用户可能会添加占位符以包含其他数据，而不必更改源代码。 有关如何使用业务文档管理的更多信息，请参见[业务文档管理概述](er-business-document-management.md)。

新用户界面 (UI) 更清晰，使用起来更舒适。 **业务文档** 区域仅显示当前提供商可用的模板。 在上一个 UI 中，**模板** 选项卡列出了可用于任何提供商的所有模板。 它还显示了由具有相同角色的任何用户创建和编辑的所有模板。

您可以使用 **新建文档** 按钮以其他提供商提供的电子报告 (ER) 格式配置创建和编辑模板。 在本主题的示例中，提供者是 Microsoft。 或者，您可以通过以 Excel 格式上传自己的模板来创建模板。


> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWAVQg]

[使用业务文档管理创建新业务文档](https://youtu.be/gAIYl-mM_pw)视频（如上所示）包含在 YouTube 上可用的 [Finance and Operations 播放列表](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW)中。

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>使业务文档管理中的新文档 UI 可用

要开始使用业务文档管理中的新文档 UI，必须打开 **功能管理** 工作区中的 **类似于 Office 的业务文档管理 UI 体验** 功能。

请按照以下步骤为所有法人启用此功能。

1. 在 **功能管理** 工作区中的 **所有** 选项卡上，选择列表中的 **类似于 Office 的业务文档管理 UI 体验** 功能。
2. 选择 **立即启用** 以打开所选功能。
3. 刷新页面以访问新功能。

## <a name="edit-templates-that-are-owned-by-other-providers"></a>编辑其他提供商拥有的模板

1. 在 **业务文档管理** 工作区中，选择 **新建文档**。

    ![业务文档管理工作区](./media/BDM_overview_new_template1.png)

2. 在 **选择** 选项卡上，选择要用作模板的文档，然后选择 **创建文档**。

    ![业务文档对话框](./media/BDM_overview_new_template2.png)

3. 在此新对话框内的 **标题** 字段中，根据需要更改标题。 标题文本用于命名自动创建的新 ER 格式配置。 此配置 (**Customer FTI report (GER) Copy**) 的草稿版本将包含编辑的模板，并且将用于为当前用户运行此 ER 格式。 将使用来自基本 ER 格式配置的原始模板为每个其他用户运行此 ER 格式。
4. 在 **名称** 字段中，更改将自动创建的可编辑模板第一个修订的名称。
5. 在 **注释** 字段中，更新有关将自动创建的可编辑模板的修订注解。
6. 选择 **确定** 以确认开始执行编辑流程。

    ![文档创建对话框](./media/BDM_overview_new_template3.png)

**新建文件** 按钮用于以其他提供商提供的 ER 格式配置创建和编辑模板。 在本示例中，提供商是 Microsoft。 当您选择 **新建文档** 时，您可以查看当前提供商和其他提供商拥有的所有模板。 选择模板后，将打开它进行编辑。 然后将把编辑后的模板存储在自动生成的新 ER 格式配置中。

## <a name="upload-a-template-that-uses-an-existing-excel-format"></a>上传使用现有 Excel 格式的模板
在上传模板之前，请按照以下步骤提供所需信息。

1. 在 **业务文档管理** 工作区中，选择 **新建文档**。

    ![业务文档管理工作区](./media/BDM_overview_new_template1.png)
    
2. 在 **创建新模板** 页面上，在 **上传** 选项卡的 **模板** 选项卡上，选择 **浏览** 以查找并选择要用作模板的 Excel 文件。 在 **模板** 部分中，将自动填写 **标题** 和 **描述** 字段。 它们指定自动创建的新 ER 格式配置的名称和描述。 可以根据需要编辑这些字段。
3. 在 **文档类型** 部分中，在 **名称** 字段中，指定业务文档的类型。 该值将用于搜索正确的数据源（即 ER 模型配置）。

    ![模板选项卡](./media/BDM_overview_new_UI_import_21.jpg)

4. 在 **数据源** 选项卡上，在 **筛选器** 快速选项卡上，选择 **应用筛选器**。 在 **数据源** 部分中，自动填写 **名称** 字段，或者您可以手动选择值。 您可以使用筛选器按名称、描述、国家/地区代码和业务文档类型搜索适当的数据源名称。

    ![数据源选项卡](./media/BDM_overview_new_UI_import_31.jpg)
    
    > [!NOTE]
    > **筛选器** 快速选项卡用于搜索正确的数据源（即 ER 模型配置）。 您可以编辑所有筛选器字段，以找到最适合您上传的文档的数据源。
    > 
    > 使用 **筛选器** 快速选项卡上的条件作为 **OR** 条件。
    
5. 在 **映射** 选项卡上，选择 **自动检测**。 自动填写 **根定义** 字段，或者您可以手动选择值。 此选项卡显示模板和模型中元素的最终映射。

    ![映射选项卡](./media/BDM_overview_new_UI_import_41.jpg)
    
   > [!NOTE]
   > **模板结构** 部分中的映射使用用户语言的数据源和模板的单元格名称中的标签或描述的完全匹配。

6. 选择 **创建文档** 以确认您要创建模板并开始编辑流程。

有关更多信息，请参见[业务文档管理概述](er-business-document-management.md)。

如果电子报告中没有提供商，您可以创建一个。 如果没有活动的提供商，您可以进行选择以激活一个。

- 若要创建提供商，请在 **名称** 字段中更改提供商的名称，在 **Internet 地址** 字段中更新新提供商的 Internet 地址，然后选择 **确定** 以确认。

    ![在 BDM 中创建新的提供商](./media/bdm_create_provider.png)
    
- 若要激活现有提供商，请在 **配置提供商** 字段中选择提供商的名称，然后选择 **确定** 以将提供商设置为活动状态。

    ![在 BDM 中激活提供商](./media/bdm_choose_provider.png)

> [!NOTE]
> 每个 BDM 模板都将该提供商引用为配置的作者。 这就是为什么模板需要活动的提供商。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
