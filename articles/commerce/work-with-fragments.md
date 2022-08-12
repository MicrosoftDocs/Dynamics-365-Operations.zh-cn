---
title: 使用片段
description: 本文介绍在 Microsoft Dynamics 365 Commerce 中使用片段的原因、时间和方法。
author: phinneyridge
ms.date: 02/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f911c5ee209cfcde5d2b2aef2c8f7343eb694cd3
ms.sourcegitcommit: 9cfccb5c260ce56a3457f9ea12e80f54ea55a3b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183281"
---
# <a name="work-with-fragments"></a>使用片段 

[!include [banner](includes/banner.md)]

本文介绍在 Microsoft Dynamics 365 Commerce 中使用片段的原因、时间和方法。

片段为必须在整个站点中重复使用的模块配置提供集中式创作体验。 例如，页眉、页脚和横幅通常配置为片段，因为它们在许多页面之间共享。 可以将片段视为可插入站点中的其他页面的微型页面。 片段有自己的生命周期。 换句话说，它们在创作工具中作为独立实体创建、引用和删除。

配置后的片段可以在您的站点结构中任何可使用模块的位置使用。 可以在页面、布局、模板和其他片段中引用片段。

> [!NOTE]
> 片段在其他片段内的嵌套深度最高可达十一级。

例如，如果要在站点中的多个页面开展季节促销活动，可以使用片段。 创建新片段的流程中，第一步是选择基础模块类型。 在本示例中，可以基于主图模块生成片段。

> [!NOTE]
> 可以基于任何模块类型生成片段。

然后可以为主图片段配置特定促销内容。 也可以根据需要本地化。 然后可以在整个站点中将新的独立主图片段用作预配置的模块。 可以将其轻松添加到模板、特定页面或包含主图模块的其他片段。

在其中添加了该片段的所有位置都是对您创建的中心主图片段的引用。 如果发布对该片段的更改，将立即在站点中引用该片段的所有位置体现这些更改。 因此，片段是在站点中重复使用和集中管理模块配置的强大、高效的方法。 通过有效利用它们，您可以大大提升灵活性，并帮助降低站点内容的管理成本。

下图显示如何使用片段在电子商务站点中集中创作共享模块配置。

![显示如何使用片段在电子商务站点中集中创作共享模块配置的图示。](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a>创建片段

可以创建新片段，也可以将现有模块配置另存为片段。

### <a name="save-an-existing-module-configuration-as-a-fragment"></a>将现有模块配置另存为片段

若要在 Commerce 站点构建器中将以前配置的模块转换为可重复使用的片段，请执行以下步骤。

1. 打开其中包含要将片段转换为的模块的页面或模板。
1. 在左侧的大纲窗格中或直接在可视页面构建器中，选择以前配置的模块。
1. 在大纲窗格中或可视页面构建器中所选模块的工具栏上，选择模块名称旁边的省略号 (**...**)。 
1. 选择 **共享为片段**。 
1. 在 **另存为片段** 对话框中，输入片段的名称。
1. 选择 **确定** 将模块配置保存为可添加到其他页面的片段。
<!-- The following image shows how to save a module configuration as a fragment.-->
<!--![A screen capture of how to save a module configuration as a fragment.](./media/save-as-fragment.png)-->

### <a name="create-a-new-fragment"></a>创建新片段

若要在 Commerce 站点构建器中创建新片段，请执行以下步骤。

1. 在左侧的导航窗格中，选择 **片段**。
1. 选择 **新建**。 将显示 **新建片段** 对话框，其中显示所有可用的模块类型。 前文中介绍过，可以基于任何模块类型创建片段。
1. 选择片段的模块类型。

<!-- The following image shows where to create a new fragment.-->
<!-- ![A screen capture of where to create a new fragment.](./media/fragment-nav-menu.png)-->
> [!TIP]
> 如果需要在以后更新和配置片段，则选择通用容器模块类型的灵活性最大。

## <a name="add-remove-or-edit-fragments-on-a-page"></a>在页面中添加，删除或编辑片段

以下过程介绍如何添加，删除和编辑片段。

### <a name="add-a-fragment"></a>添加片段

若要在 Commerce 站点构建器中将片段添加到页面，请执行以下步骤。

1. 在左侧的大纲窗格中或直接在可视页面构建器中，选择可向其添加子模块的容器或插槽。
1. 选择容器或插槽名称旁边的省略号 (**...**)。  或者，如果使用可视页面构建器，请选择加号 (**+**)。  
1. 选择 **添加片段**。
    <!-- ![A screen capture of how to add an existing fragment to a slot or container.](./media/add-fragment.png)-->
 
    > [!NOTE]
    > 如果容器或插槽不支持新的子模块，则 **添加片段** 选项不可用。
    
1. 在 **选择片段** 对话框中，搜索并选择要添加的片段。 如果未列出可用片段，可能必须先基于所选容器或插槽支持的模块类型创建片段。
1. 选择所需的片段以将其添加到页面上的容器或插槽中。
<!--    ![A screen capture of the fragment picker modal window.](./media/fragment-picker.png)-->

> [!NOTE]
> 容器或插槽中允许的模块由页面的模板或模块自己的定义定义。

### <a name="remove-a-fragment"></a>删除片段

若要在 Commerce 站点构建器中从页面上的插槽或容器中删除片段，请执行以下步骤。

1. 在左侧大纲窗格中，选择要删除的片段的名称旁边的省略号 (**...**)，然后选择垃圾桶符号。  此外，您可以在可视页面构建器中选择片段，然后在片段的工具栏中选择垃圾桶符号。
1. 系统提示确认要删除片段时，选择 **确定**。

> [!NOTE]
> 从页面中删除片段时，仅从页面中删除对该片段的引用。 切 **勿** 从站点中删除片段。 若要从站点中删除片段，必须使用片段检查器用户界面 (UI)。 只能删除当前没有任何页面、模板或其他片段正在引用的片段。

### <a name="edit-a-fragment"></a>编辑片段

若要编辑片段，必须使用片段编辑器 UI。 这是设计制订的限制。 这样有助于确保作者不会混淆特定页面的模块编辑流程和可能在多个页面之间共享的片段的编辑流程。

若要在 Commerce 站点构建器中编辑片段，请执行以下步骤。

1. 在左侧的导航窗格中，选择 **片段**。
1. 在 **片段** 下，选择要编辑的片段。
1. 根据需要编辑片段的模块属性和结构。 此流程类似在页面编辑器视图中编辑模块的流程。

也可以通过在页面、模板或父片段中打开片段，然后在右侧属性窗格中选择 **编辑片段** 来编辑片段。

### <a name="rename-a-fragment"></a>重命名片段

要在站点构建器中重命名现有片段，请执行以下步骤。

1. 在左侧导航窗格中，选择 **片段**。
1. 选择您想要重命名的片段的片段名称。
1. 选择 **编辑** 开始编辑片段。 请注意，如果其他人已在编辑片段，您将无法编辑该片段。
1. 在片段属性窗格中，选择片段名称旁边的笔符号。
1. 根据需要编辑片段名称。
1. 选择复选标记确认名称更改。
1. 选择 **完成编辑**。

您可以在创建片段后重命名片段，方法是对其进行编辑，然后在属性窗格中选择片段名称旁边的笔符号。

## <a name="additional-resources"></a>其他资源

[模板和布局概览](templates-layouts-overview.md)

[使用模板](work-with-templates.md)

[使用预设布局](work-with-layouts.md)

[使用发布组](publish-groups.md)

[查看版本历史记录以还原页面和片段](version-history-revert.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
