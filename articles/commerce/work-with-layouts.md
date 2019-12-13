---
title: 使用预设布局
description: 此主题描述如何在 Microsoft Dynamics 365 Commerce 中使用预设布局。
author: phinneyridge
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
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1f2c0638caa7e4f6f831e592e3f7e3f5ab7d1d81
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697811"
---
# <a name="work-with-preset-layouts"></a>使用预设布局

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

此主题描述如何在 Microsoft Dynamics 365 Commerce 中使用预设布局。

## <a name="overview"></a>概览

完成此主题中的过程之前，务必阅读[预设布局和自定义布局](templates-layouts-overview.md#preset-and-custom-layouts)。 有关一般概述，请参阅[模板和布局概述](templates-layouts-overview.md)。

## <a name="create-a-new-preset-layout"></a>创建新预设布局

创建预设布局有两种方法。 可以将现有自定义布局另存为预设布局，也可以从头创建预设布局。

### <a name="create-a-preset-layout-from-an-existing-custom-layout"></a>基于现有自定义布局创建预设布局

若要基于现有自定义布局创建预设布局，请执行以下步骤。

1. 打开现在不使用预设布局，并且具有您要用于站点中其他页面的模块结构的现有页面。
1. 选择**签出**。
1. 选择**另存为新布局**。 将显示**另存为新布局**对话框。
1. 为预设布局输入名称和描述。 其他作者基于您的布局创建新页面或切换到您的布局时，将对这些作者显示您输入的值。 因此，输入对页面作者有用的值。
1. 选择**确定**。

在您创建新页面或在同一个模板层次结构中为页面选择其他布局时，现在可使用预设布局。

> [!TIP]
> 若要快速查看特定页面当前是否已绑定到预设布局，请在页面列表视图中选择页面，然后检查右侧的属性窗格中的布局元数据。

### <a name="create-a-new-preset-layout"></a>创建新预设布局

若要从头创建预设布局，请执行以下步骤。

1. 在左侧的导航窗格中，选择**布局**。
1. 选择**新建布局**。 将显示**新布局**对话框。
1. 选择要用于预设布局的模板。
1. 为预设布局输入名称和描述。 其他作者基于您的布局创建新页面或切换到您的布局时，将对这些作者显示您输入的值。 因此，输入对页面作者有用的值。
1. 选择**确定**创建新预设布局，然后打开布局编辑器。
1. 在布局编辑器中，使用左侧大纲树和右侧属性窗格添加和配置模块。 （此流程类似在模板编辑器中为模板添加和配置模块的流程。）模块的排列和任何已锁定默认设置将成为使用此预设布局的任何页面的中央模块配置。

## <a name="modify-a-preset-layout"></a>修改预设布局

若要修改预设布局，请执行以下步骤。

1. 在左侧的导航窗格中，选择**布局**。
1. 在布局编辑器中左侧大纲树内，选择要修改的模块。 然后执行以下任何步骤：

    - 若要在模块的父级中上下移动模块，请选择模块的省略号按钮 (**...**)，然后选择**上移**或**下移**。
    - 若要更改模块的默认设置，请使用属性窗格输入默认值，或者选择对所有下游页面选择锁定它们。
    - 若要向容器模块添加模块或片段，请选择省略号按钮，然后选择**添加模块**或**添加片段**。
    - 若要从布局中删除模块，请选择省略号按钮，然后选择**删除**。

## <a name="change-a-preset-layout-theme"></a>更改预设布局主题

典型实践是为使用预设布局的所有页面设置默认主题。

若要设置或更改使用预设布局的所有子页面的主题，请执行以下步骤。

1. 在布局编辑器中左侧大纲树内，选择页面容器模块。 （此模块通常是第二个节点，名称为**默认页**。）
1. 在右侧的属性窗格中**主题**字段内，选择一个主题。

## <a name="save-check-in-preview-and-publish-a-preset-layout"></a>保存，签入，预览和发布预设布局

若要保存和签入预设布局，请执行以下步骤。

1. 选择布局编辑器顶部的**保存**。 保存的更改在签入前，不影响下游页。
1. 选择**签入**。 现在可为下游工作流发现更改。

若要预览更改，请打开使用预设布局的现有页面，或基于布局创建新页面。

预览对预设布局的更改之后，执行以下步骤之一将布局发布到您的活动站点：

* 转到**布局**，选择布局，然后选择**发布**。
* 在布局编辑器中，选择**发布**。
* 发布引用未发布布局的页面。 将自动发布布局。

> [!WARNING]
> 预设布局可以被多个页面引用。 发布预设布局时，请注意，您可能影响多个页面的布局。

## <a name="additional-resources"></a>其他资源

[模板和布局概览](templates-layouts-overview.md)

[使用模板](work-with-templates.md)
