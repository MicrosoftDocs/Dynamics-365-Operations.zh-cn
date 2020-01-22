---
title: 修改现有的站点页面
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中修改现有站点页面。
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 50373d3681e269bf6164b2a425bbafebdd93d64f
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945689"
---
# <a name="modify-an-existing-site-page"></a>修改现有的站点页面

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

此主题介绍如何在 Microsoft Dynamics 365 Commerce 中修改现有站点页面。

## <a name="overview"></a>概览

必须修改页面时，第一步是在页面编辑器中打开该页面。 转到其中包含您的页面的站点，然后在页面列表中找到所需页面。 如果找不到此页面，可使用创作工具丰富的搜索功能。 键入精确的页名，或键入页面的前几个字母和星号 (\*)。 将显示筛选后的页面列表。 可使用此列表查找所需页面。 找到正确的页面之后，选择页名在页面编辑器中打开页面。

> [!TIP]
> 如果页面检查器中显示您的页面，可选择该页面，然后将其签出，才能在页面编辑器中打开。 这样就可以同时签出多个页面。

在页面编辑器中打开页面之后，必须确保将其签出给您。 创作工具中的命令栏动态，上下文相关且状态相关。 因此，仅显示当前可在页面中执行的操作。 例如，如果不将页面签出给您，则命令栏中不显示**保存**和**签入**按钮。 窗口右侧还显示页面状态。

如果页面尚未签出给您，请在命令栏中选择**签出**。 命令栏将变化以体现新的页面状态。 您还会收到通知，说明已将页面签出给您。

下一步是进行真正的更改。 通常使用左侧的页面大纲树查找和选择要更改的模块，然后在右侧属性窗格中进行更改。 

但是，您的更改有时涉及添加或删除模块或片段。 若要添加片段或模块，请使用页面大纲树查找要向其添加模块或片段的插槽，然后选择该插槽的省略号按钮 (**...**)。 将显示一个菜单，其中包含用于添加模块或片段的命令。 若要删除模块或片段，请在页面大纲树中找到并选择，选择省略号按钮，然后选择用于删除模块或片段的命令。

> [!TIP]
> 也可以通过直接选择，查看和编辑“所见即所得”(WYSIWYG) 预览中显示的任何模块的属性。

进行更改并预览其效果之后，应该通过选择命令栏中的**签入**签入页面。 

若要立即发布更改，请选择命令栏中的**发布**。 您修改的页面的最新签入版本将发布并可供查看您的站点的外部用户使用。 

## <a name="example-change-the-video-on-the-home-page"></a>示例：更改主页中的视频

以下示例显示如何通过更改视频播放器模块中显示的视频，修改主页。

1. 在**站点**下，选择 **Fabrikam**（或您的站点的名称）。
1. 在左侧的导航窗格中，选择**页面**。
1. 转到并选择主页在页面编辑器中将其打开。
1. 在命令栏中，选择**签出**。
1. 在页面大纲中，选择**主**插槽。
1. 在**主**插槽下，展开所有流体容器模块。
1. 找到并选择视频播放器模块。
1. 在右侧属性窗格中，选择**视频**属性。 将显示资产选取器。
1. 在资产选取器中，选择一个可用视频资产，或选择**上传新资产**上传一个新视频资产。
1. 选择**确定**。
1. 选择**保存**，然后选择**签入**。
1. 在**注释**字段中，输入**已更改视频**，然后选择**确定**。
1. 选择**预览**预览更新后的页面。 完成后，关闭预览标签页回到创作工具。
1. 选择**发布**。

## <a name="additional-resources"></a>其他资源

[添加新的站点页面](add-new-page.md)

[选择页面布局](select-page-layouts.md)

[管理 SEO 元数据](manage-seo-metadata.md)

[保存、预览和发布页面](save-preview-publish-page.md)

[丰富产品页面](enrich-product-page.md)

[丰富类别登陆页面](enrich-category-page.md)

[验证页面内容可访问性](verify-accessibility.md)
