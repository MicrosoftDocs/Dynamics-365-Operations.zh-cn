---
title: 使用片段
description: 此主题介绍在 Microsoft Dynamics 365 Commerce 中使用片段的原因、条件和方法。
author: v-chgri
manager: annbe
ms.date: 01/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: retail
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f29046ded47ed9c49a2cc841aa7c1f6492b49aec
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026032"
---
# <a name="work-with-fragments"></a>使用片段 


[!include [banner](includes/banner.md)]

此主题介绍在 Microsoft Dynamics 365 Commerce 中使用片段的原因、条件和方法。

## <a name="overview"></a>概览

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

![显示如何使用片段在电子商务站点中集中创作共享模块配置的插图](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a>创建片段

可以创建新片段，也可以将现有模块配置另存为片段。

### <a name="save-an-existing-module-configuration-as-a-fragment"></a>将现有模块配置另存为片段

若要将以前配置的模块转换为可重复使用的片段，请执行以下步骤。

1. 打开其中包含要将片段转换为的模块的页面或模板。
1. 在左侧的大纲窗格中，选择模块名称旁边的省略号按钮 (**...**)。 
1. 选择**共享为片段**。 
1. 对话框出现 为片段输入名称和元数据。
1. 选择**确定**将模块配置保存为可添加到其他页面的片段。

下图显示了如何将模块配置另存为片段。

![有关如何将模块配置另存为片段的屏幕截图](./media/save-as-fragment.png)

### <a name="create-a-new-fragment"></a>创建新片段

若要创建新片段，请执行以下步骤。

1. 在左侧的导航窗格中，选择**片段**。
1. 选择**新建页面片段**。 将显示一个对话框，其中显示所有可用模块类型。 前文中介绍过，可以基于任何模块类型创建片段。
1. 选择片段的模块类型。

下图显示了在哪里创建新片段。

![关于在哪里创建新片段的屏幕截图](./media/fragment-nav-menu.png)

> [!TIP]
> 如果需要在以后更新和配置片段，则选择通用容器模块类型的灵活性最大。

## <a name="add-remove-or-edit-fragments-on-a-page"></a>在页面中添加，删除或编辑片段

以下过程介绍如何添加，删除和编辑片段。

### <a name="add-a-fragment"></a>添加片段

若要向页面添加片段，请执行以下步骤。

1. 在左侧的大纲窗格中，选择可向其添加子模块的容器或插槽。
1. 选择容器或插槽名称旁边的省略号按钮，然后选择**添加片段**。 对话框出现

    ![有关如何将现有片段添加到插槽或容器的屏幕截图](./media/add-fragment.png)
 
    > [!NOTE]
    > 如果容器或插槽不支持新子模块，则**添加片段**选项不可用。
    
1. 在对话框中，搜索并选择要添加的片段。 如果未列出可用片段，可能必须先基于所选容器或插槽支持的模块类型创建片段。
1. 选择所需的片段以将其添加到页面上的容器或插槽中。

    ![关于片段选择器模式窗口的屏幕截图](./media/fragment-picker.png)

> [!NOTE]
> 容器或插槽中允许的模块由页面的模板或模块自己的定义定义。

### <a name="remove-a-fragment"></a>删除片段

若要从站点中的插槽或容器删除片段，请执行以下步骤。

1. 在左侧大纲窗格中，选择要删除的片段的名称旁边的省略号按钮，然后选择废纸篓按钮。
1. 系统提示确认要删除片段时，选择**确定**。

> [!NOTE]
> 从页面中删除片段时，仅从页面中删除对该片段的引用。 切**勿**从站点中删除片段。 若要从站点中删除片段，必须使用片段检查器用户界面 (UI)。 只能删除当前没有任何页面、模板或其他片段正在引用的片段。

### <a name="edit-a-fragment"></a>编辑片段

若要编辑片段，必须使用片段编辑器 UI。 这是设计制订的限制。 这样有助于确保作者不会混淆特定页面的模块编辑流程和可能在多个页面之间共享的片段的编辑流程。

若要编辑片段，请执行以下步骤。

1. 在左侧的导航窗格中，选择**片段**。
1. 在**片段**下，选择要编辑的片段。
1. 根据需要编辑片段的模块属性和结构。 此流程类似在页面编辑器视图中编辑模块的流程。

也可以通过在页面、模板或父片段中打开片段，然后在右侧属性窗格中选择**编辑片段**来编辑片段。

## <a name="additional-resources"></a>其他资源

[模板和布局概览](templates-layouts-overview.md)

[使用模板](work-with-templates.md)

[使用预设布局](work-with-layouts.md)

[使用发布组](publish-groups.md)
