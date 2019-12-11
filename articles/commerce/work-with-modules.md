---
title: 使用模块
description: 此主题介绍在 Microsoft Dynamics 365 Commerce 中使用模块的方法和条件。
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 06a26e5dfd35bf229e67ed27213210d0da726bdf
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698065"
---
# <a name="work-with-modules"></a>使用模块

此主题介绍在 Microsoft Dynamics 365 Commerce 中使用模块的方法和条件。

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

## <a name="overview"></a>概览

模块是构成页面结构的逻辑构建基块，其具有多种用途和作用范围。 某些模块是高级别容器，唯一用途是容纳和组织其他模块（子模块）。 其他模块（如简单图像放置模块）具有非常具体的用途。 其他模块（如传送模块）介于这两种类别之间。

默认情况下，Dynamics 365 Commerce 站点中有一个入门套件模块库，用于实现大多数基本的电子商务方案。 仅使用这些模块应该就可以构造端到端的电子商务站点。 但是，您也可能希望自定义这些模块或生成新的自定义模块来满足特定需要。 如果要生成自定义模块，提供了模块设计软件开发工具包 (SDK) 来帮助您创建自定义模块库。

## <a name="container-modules-and-slots"></a>容器模块和插槽

前面介绍过，设计某些模块是为了容纳子模块。 这些模块称为*容器*，并允许嵌套模块层次结构。 容器模块中包含*插槽*。 插槽用于处理容器中子模块的布局和用途。 例如，用于定义多个重要插槽的基本页面容器模块（任何页面的顶级模块）。

- 页眉插槽
- 主体插槽
- 页脚插槽

模块的开发人员定义这些插槽，并确定可以在其中直接放入哪些和多少子模块。 例如，页眉插槽可能仅支持**页眉模块**类型的一个模块，而主体模块支持任何类型任意数量的模块（除了其他页面容器模块）。

在创作工具中，页面作者不必提前了解每个插槽中可以放入哪些模块，不可以放入哪些模块。 当页面作者厇插槽，然后尝试选择要为其添加的模块时，将看到该插槽支持的模块类型筛选后的视图。

## <a name="content-modules"></a>内容模块

内容模块中包含内容和媒体内容，如文本（如标题、段落和链接）或资产引用（如图像、视频和 PDF）。 例如，**主图**、**特色**和**横幅**就是典型的内容模块类型。 这三种类型的模块中可以包含文本或媒体，不需要任何子模块即可在页面中显示内容。

典型日常页面和内容创作活动大部分涉及内容模块，主要是因为这些模块定义其父容器模块中呈现的实际内容。 提供了许多内容模块，这些模块通常是向页面嵌套模块层次结构添加的最后内容。

下图显示父容器模块插槽内如何嵌套模块。

![嵌套模块](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a>添加或删除模块

以下过程介绍如何添加和删除模块。

### <a name="add-a-module"></a>添加模块

若要向页面中的插槽或容器添加模块，请执行以下步骤。

1. 在左侧的大纲窗格中，选择可向其添加子模块的容器或插槽。

    > [!NOTE]
    > 模块设计者定义可添加到特定模块插槽的模块类型的列表。 然后，模板作者可优化允许的模块选项，以便帮助确保基于特定模板生成的所有页面获得一致的搜索引擎优化 (SEO) 和创作效率。

1. 选择模块的省略号按钮 (**...**)，然后选择**添加模块**。 将显示**添加模块**对话框。 将自动筛选此对话框，使其仅显示所选容器或插槽中支持的模块。 模块列表由页面的目标或容器模块定义决定。

    > [!NOTE]
    > 如果容器或插槽不支持新子模块，则**添加模块**选项不可用。

1. 在对话框中，搜索并选择要添加到页面的模块。

    > [!TIP]
    > **特色**和**主图**模块类型非常适合初学者。

1. 选择**确定**将所选模块添加到页面中的所选容器或插槽。

### <a name="remove-a-module"></a>删除模块

若要从站点中的插槽或容器删除模块，请执行以下步骤。

1. 在左侧大纲窗格中，选择要删除的模块的名称旁边的省略号按钮，然后选择废纸篓按钮。
1. 系统提示确认要删除模块时，选择**确定**。

## <a name="configure-modules"></a>配置模块

以下过程介绍如何配置内容模块和容器模块。

### <a name="configure-a-content-module"></a>配置内容模块

若要在页面中配置内容模块，请执行以下步骤。

1. 在左侧的大纲窗格中，选择一个内容模块类型（例如，**特色**、**主图**或**横幅**）。
1. 在右侧的属性窗格中，通过选择标题展开嵌套的控件，然后设置所有必需控件值。
1. 如果属性窗格有**数据配置**部分，请选择该部分将其展开。 否则，转到步骤 5。
1. 如果有**添加数据源**按钮，选择该按钮，然后选择要添加的内容项。
1. 输入所有必需或所需模块控件的设置。
1. 选择**保存**。

### <a name="configure-a-container-module"></a>配置容器模块

若要在页面中配置容器模块，请执行以下步骤。

1. 在页面中选择一个容器模块（例如，传送或流体容器模块）。
1. 在右侧的属性窗格中，通过选择标题展开嵌套的控件，然后设置所有必需控件值。
1. 在左侧大纲窗格中，选择容器或容器内的任何插槽的名称旁边的省略号按钮，然后选择**添加模块**。 然后向所选容器添加子模块。 有关详细信息，请参阅本主题前文的[添加模块](#add-a-module)过程。
1. 如果多个子模块以同级的形式存在于父容器中，可以更改其在父容器中的显示顺序。 选择一个容器的省略号按钮，然后使用向上箭头按钮或向下箭头按钮。

## <a name="additional-resources"></a>其他资源

[模板和布局概览](templates-layouts-overview.md)

[使用模板](work-with-templates.md)

[使用预设布局](work-with-layouts.md)

[使用片段](work-with-fragments.md)

[向页面添加容器模块](add-container-module.md)

[向页面添加内容放置模块](add-content-placement-modules.md)

