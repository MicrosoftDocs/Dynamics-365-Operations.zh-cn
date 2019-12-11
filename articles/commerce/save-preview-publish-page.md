---
title: 保存、预览和发布页面
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中保存、预览和发布页面。
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
ms.openlocfilehash: 8c1b82b1b8423c63d442ee581ed0cc8789ee63fd
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697880"
---
# <a name="save-preview-and-publish-a-page"></a>保存、预览和发布页面

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

此主题介绍如何在 Microsoft Dynamics 365 Commerce 中保存、预览和发布页面。

## <a name="save-a-page"></a>保存页面

若要保存页面，必须先将其签出给您自己，然后在页面编辑器中打开。 应该在修改页面之后立即保存页面，以帮助确保存储更改。

保存页面时，更改仅对您显示。 保存操作应该主要用于在页面尚未准备好签入时存储更改。 修改完页面后，建议将其签入，这样就可以对其他人显示更改。 此时，其他必须修改页面的用户也可以签出该页面。

## <a name="preview-a-page"></a>预览页面

创作工具提供两种预览功能：页面编辑器中的“所见即所得”(WYSIWYG) 预览窗格和单独的预览窗口。

使用页面编辑器时，中央窗格中将显示“所见即所得”(WYSIWYG) 预览。 只要保存页面，都将自动更新此预览。 也可以通过选择命令栏中的**刷新**手动更新。 WYSIWYG 预览呈现的页面和站点用户看到的完全一样，但是创作帮助器在顶部显示。

修改完页面之后，您可能希望预览页面以查看客户将看到的效果。 若要预览页面，请在命令栏中选择**预览**。 将在一个单独的浏览器窗口中显示预览。 预览窗口中显示的页面和站点用户将看到的完全一样。 可以调整窗口大小以确保所有查看端口中都正确显示响应模块。

> [!NOTE]
> 需要身份验证和正确的权限才能预览未发布的内容。 因此，如果与某用户共享预览的 URL，该用户必须具有正确的权限才能访问内容。

## <a name="publish-a-page"></a>发布页面

页面准备就绪之后，下一步是发布，以便外部用户查看内容。 页面只有在签入后，才能发布。

可从页面检查器或页面编辑器发布和取消发布页面。 页面检查器显示页面列表，并允许执行批量操作。 页面编辑器只能用于发布或取消发布其中打开的单个页面。

若要从页面检查器发布一个或多个页面，请选择页面，确保已签入这些页面，然后在命令栏中选择**发布**。 将发布这些页面，而您会在创作工具中收到有关此操作的通知。

从页面编辑器发布单个页面的过程相似。 在页面编辑器中打开页面后，确保已签入该页面，然后在命令栏中选择**发布**。 将发布此页面，而您会收到有关此操作的通知。

发布页面时，仅发布页面内容。 仅当为该页面关联了 URL，您和其他用户才可以转到该页面并查看。 URL 必须单独发布。

> [!IMPORTANT]
> 必须已经发布了页面引用的所有图像或片段，才能发布页面。

## <a name="save-preview-and-publish-a-home-page"></a>保存、预览和发布主页

若要保存，预览和发布主页，请执行以下步骤。

1. 在**站点**下，选择 **Fabrikam**（或您的站点的名称）。
1. 在左侧的导航窗格中，选择**页面**。
1. 转到并选择主页在页面编辑器中将其打开。
1. 选择**签出**。
1. 根据需要修改页面。
1. 选择**保存**，然后选择**签入**。
1. 在**注释**字段中，输入有关您所做更改的注释，然后选择**确定**。
1. 选择**预览**预览您的页面。 完成后，关闭预览标签页回到创作工具。
1. 选择**发布**。

## <a name="publish-a-url"></a>发布 URL

若要发布 URL，请执行以下步骤。

1. 在**站点**下，选择 **Fabrikam**（或您的站点的名称）。
1. 在左侧的导航窗格中，选择 **URL**。
1. 找到并选择要发布的 URL。
1. 在命令栏中，选择**发布**。

## <a name="additional-resources"></a>其他资源

[修改现有的站点页面](modify-existing-page.md)

[添加新的站点页面](add-new-page.md)

[选择页面布局](select-page-layouts.md)

[管理 SEO 元数据](manage-seo-metadata.md)

[丰富产品页面](enrich-product-page.md)

[丰富类别登陆页面](enrich-category-page.md)

