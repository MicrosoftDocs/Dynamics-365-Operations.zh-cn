---
title: 处理 CSS 覆盖文件
description: 本主题介绍为什么、何时以及如何在 Microsoft Dynamics 365 Commerce 中使用级联样式表 (CSS) 覆盖文件。
author: phinneyridge
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b5a50fc0c9060117cdddc0875446afc2edc12a11
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915431"
---
# <a name="work-with-css-override-files"></a>处理 CSS 覆盖文件

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

本主题介绍为什么、何时以及如何在 Microsoft Dynamics 365 Commerce 中使用级联样式表 (CSS) 覆盖文件。

## <a name="overview"></a>概览

永久站点样式通常应该通过站点主题进行处理。 主题为站点的任何一个页面上的模块提供基本 CSS 和样式设置。 主题是使用 Dynamics 365 Commerce 联机软件开发套件 (SDK) 创建的，可以通过 Microsoft Dynamics Lifecycle Services (LCS) 部署到您的网站。 SDK 中的主题调试功能和模块接口配置可帮助站点开发人员创建可自定义且紧密结合的站点设计包。 将这些设计包部署到站点时，站点作者可以专注于创建、编辑和发布内容，而不是站点开发。

考虑到主题的一般生命周期，在某些情况下，依赖开发人员通过 SDK 和 LCS 部署管道进行样式更改可能会被禁止。 如果未配置 SDK，或者您没有时间等待 LCS 部署完成，站点原型或修补程序似乎会很难处理。

在这些情况下，CSS 覆盖文件可以提供帮助。 在 Commerce 创作工具中，经过身份验证的用户可以上载 CSS 文件，对其进行预览，然后将其激活来覆盖站点的主题。 SDK 或 LCS 部署不需要开销。 CSS 覆盖文件中指定的覆盖可以小至对一个文本样式的更改，也可以广到完整的品牌调整。

使用 CSS 覆盖文件之前，请注意以下限制：

- 站点上一次只能有一个 CSS 覆盖文件处于活动状态。 因此，所有活动覆盖都必须在一个覆盖文件中。
- 尽管您可以在 Commerce 创作工具中预览覆盖，但是并没有专用的调试功能来帮助发现覆盖所引起的错误。 换句话说，当您使用 CSS 覆盖文件时，您没有与 SDK 为模块和创作验证提供的相同的工具集。

不过，CSS 覆盖文件提供了一种在开发和部署完整主题更新之前快速设计原型或实现修补程序的方法。

## <a name="create-a-css-override-file"></a>新建 CSS 覆盖文件

创建 CSS 覆盖文件，您可以使用任何一个集成开发环境 (IDE)、文本编辑器或源代码编辑器。 一种典型的方法是在浏览器中使用标准 Web 调试器，来在现有站点上确定样式选择器、属性和值。 大多数浏览器允许您在调试器中更改值并预览它们。 确定要进行的更改后，可以将其保存到您自己的 CSS 文件。

## <a name="upload-a-css-override-file"></a>上载 CSS 覆盖文件

要将 CSS 文件上载到 Commerce 中的站点，请按照下列步骤操作。

1. 在创作工具中，转到您的站点。
1. 在左侧的导航窗格中，选择**设计**。

    > [!NOTE]
    > 根据您使用的 Commerce 的创作工具的版本，您可能需要在导航窗格中展开**设置**，然后才能选择**设计**。

1. 在主设计窗格的顶部，选择 **CSS 覆盖**选项卡（如果尚未选择）。
1. 在**可用 CSS 覆盖**下，选择**上载 CSS 文件**。 将出现一个“文件资源管理器”窗口。
1. 在“文件资源管理器”中，浏览并选择一个 CSS 文件，然后选择**打开**。 上载的 CSS 文件现在显示在**可用 CSS 覆盖**下。

## <a name="preview-a-css-override-file"></a>预览 CSS 覆盖文件

若要预览 CSS 覆盖文件，然后在活动站点上将其激活，请按照以下步骤操作。

1. 在左侧的导航窗格中，选择**设计**，然后在 **CSS 覆盖**选项卡上，在**可用 CSS 覆盖**下，找到您要预览的 CSS 文件。
1. 在 CSS 文件名旁边，选择**预览站点**。
1. 在**选择 URL** 对话框中，选择应用了覆盖的站点的 URL，然后选择**确定**。
1. 如果所选 URL 有多个变型，请在出现的**预览变型**对话框中选择所需的变型。

将打开一个新的浏览器选项卡或窗口，您可以在其中验证针对您的网站的样式覆盖。 然后，您可以与其他经过身份验证的 Commerce 用户共享该 URL，以进行查看和反馈。

## <a name="activate-a-css-override-file-on-your-live-site"></a>在您的活动站点上激活 CSS 覆盖文件

预览并批准后 CSS 覆盖文件，您可以在活动站点上激活它。

> [!NOTE]
> 您的站点上一次只能有一个 CSS 覆盖文件处于活动状态。 如果激活新的覆盖文件，先前的覆盖文件将被禁用。 因此，请确保所有必需的覆盖都存在于一个 CSS 覆盖文件中。

若要激活 CSS 覆盖文件，请执行以下步骤。

1. 在左侧的导航窗格中，选择**设计**，然后在 **CSS 覆盖**选项卡上，在**可用 CSS 覆盖**下，找到您要激活的 CSS 文件。
1. 在 CSS 文件名下，选择**激活**。 覆盖文件将立即在您的活动站点上变为活动状态。

## <a name="deactivate-a-css-override-file-on-your-live-site"></a>在您的活动站点上禁用 CSS 覆盖文件

要在您的站点上禁用 CSS 覆盖文件，请按照以下步骤操作。

1. 在左侧的导航窗格中，选择**设计**，然后在 **CSS 覆盖**选项卡上，在**可用 CSS 覆盖**下，找到您要禁用的 CSS 文件。
1. 在 CSS 文件名下，选择**禁用**。 覆盖文件将立即在您的活动站点上变为停用状态。

> [!TIP]
> 要访问 CSS 覆盖文件的其他选项，请选择 CSS 文件名旁边的省略号 (**...**)。 **下载**、**重命名**和**替换**选项可用于快速更改现有的 CSS 覆盖文件。

## <a name="additional-resources"></a>其他资源

[添加徽标](add-logo.md)

[选择站点主题](select-site-theme.md)

[添加收藏夹图标](add-favicon.md)

[添加欢迎消息](add-welcome-message.md)

[添加版权声明](add-copyright-notice.md)

[向站点添加语言](add-languages-to-site.md)

[将脚本代码添加到站点页面以支持遥测](add-telemetry.md)
