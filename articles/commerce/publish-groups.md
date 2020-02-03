---
title: 使用发布组
description: 本主题介绍 Microsoft Dynamics 365 Commerce 中的发布组功能。
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
ms.openlocfilehash: 96e55683c46dc196ebac2d0e16f38835c8bfe7df
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915408"
---
# <a name="work-with-publish-groups"></a>使用发布组

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

本主题介绍 Microsoft Dynamics 365 Commerce 中的发布组功能。

## <a name="overview"></a>概览

电子商务网站全年会不断更新新内容。 更新通常是围绕繁忙的电子商务活动（如假期、季节性市场营销活动或促销启动）成批发布。 这些更新通常要求在单个操作中同时筹划、验证和发布网站内容组（例如，页面、图像、片段和模板）。

将项目分组为一起发布项目的逻辑集（每个集都有自己的生命周期）的能力，将为站点作者提供许多好处。 在 Commerce 中，这些逻辑集称为发布组。 他们使站点作者可以将更新集作为自己的可配置、可测试且可发布的实体进行跟踪。

作者可以在筹划好的发布组中预览更新，而不会影响活动站点或其他独立的发布组。 然后，作者可以计划发布操作，以将发布组中的所有项目同时发布到活动站点。 对于许多会通过基于活动的站点更新里程碑获得可观年度收入的企业级公司来说，能够对要发布的更新进行分组、预览和计划非常重要。

公司可能会因无法顺利进行的缓慢或无效的内容发布而产生成本。 发布组有助于确保活动启动能够得到按时地安排、验证和发布。 无论是大是小，发布组都会提供宝贵的工具集，可帮助作者安排和简化正在进行的站点更新任务。

## <a name="when-to-use-publish-groups"></a>何时使用发布组

任何时候当您必须筹划多个文档并要一起发布时，都可以使用发布组。 例如，如果您的网站每个季节更新一次内容，则可以为这些季节性市场营销活动创建发布组。 您的“秋季季节性更新”发布组可以包含新的季节性图像、带有季节性市场营销消息的片段、包含季节性产品集合的页面，或其他季节性网站更新。

发布组的一个优点是您可以并行筹划进行多个更新。 例如，在“秋季季节性更新”发布组更新之后不久，可能会有特定假期周末的内容更新。 在这种情况下，您可以在筹划后续的“秋季假期更新”发布组的内容的同时，筹划“秋季季节性更新”发布组的内容。 每个发布组包含其自己的一组独特页面、图像、片段、模板等。 您可以在并发时间线上独立地筹划、预览和验证这两个发布组。 然后可以计划让每个发布组在特定日期和时间在您的站点上线。

## <a name="turn-on-the-publish-groups-feature"></a>打开发布组功能

发布组功能是可选的，要使用，必须自行为站点打开。

要在 Commerce 创作工具中打开站点的发布组功能，请按照下列步骤操作。

1. 在左侧导航窗格中，选择**站点设置**将其展开。
1. 在**站点设置**下，选择**功能**。
1. 将**发布组**选项设置为**开**。

## <a name="create-a-publish-group"></a>创建发布组

要在 Commerce 创作工具中为站点创建发布组，请按照下列步骤操作。

1. 在左侧导航窗格中，选择**发布组**。
1. 在顶部命令栏中，选择**新建**。
1. 在**创建发布组**对话框中，在**发布组名称**下，输入一个描述性名称。 然后选择**确定**。

## <a name="set-the-publish-group-authoring-context"></a>设置发布组创作上下文

在 Commerce 中，默认的创作上下文是活动站点上下文。 活动站点创作上下文是默认视图，您无需使用发布组即可在其中直接查看和更改网站。 它代表对站点的已发布版本的最新的直接更新。 如果左侧导航窗格中**发布组**下的上下文控件显示名称**活动站点**，说明您正在活动站点创作上下文中工作。 **活动站点**是上下文控件的默认名称。 否则，上下文控件将显示发布组的名称。

要在发布组中工作，必须为其切换到发布组创作上下文。 若要设置发布组上下文，请按照下列步骤之一进行操作。

- 在左侧导航窗格中，直接在**发布组**下选择上下文控件，然后在显示的选项列表中选择发布组的名称。 上下文控件已被重命名，显示发布组的名称。
- 在左侧导航窗格中，选择**发布组**，然后，在**发布组**下，选择发布组的名称。 上下文控件已被重命名，显示发布组的名称。

设置发布组创作上下文后，您将在预览和编辑站点内容时在该发布组上下文中工作。

若要返回到默认的活动站点创作上下文，请选择上下文控件，然后选择**活动站点**。

## <a name="add-pages-or-other-items-to-a-publish-group"></a>将页面或其他项目添加到发布组

选择发布组创作上下文，并且左侧导航窗格中的上下文控件显示其名称之后，您可以像在默认活动站点上下文中一样创建内容。 您还可以从其他发布组或活动站点上下文添加现有页面或其他项目。

要将现有页面复制到发布组，请按照下列步骤操作。

1. 选择要从其复制的创作上下文，然后在左侧导航窗格中选择**页面**。
1. 选择要添加到发布组的页面。
1. 在命令栏中，选择**复制到发布组**。
1. 在**选择发布组**对话框中，选择要添加页面的发布组，然后选择**确定**。

您可以使用相同的基本步骤来创建自定义的产品页面、URL、模板、布局、片段和媒体库资产，或将这些类型的现有项目添加到发布组。

## <a name="validate-a-publish-group"></a>验证发布组

为确保发布组内容中的所有依赖项都符合要求并且所有验证都能够通过，您可以在计划发布操作之前运行验证来发现必须解决的所有问题。

若要在计划之前验证发布组，请按照下列步骤操作。

1. 在左侧导航窗格中，选择**发布组**。
1. 选择要验证的发布组。
1. 在命令栏中，选择**验证**。

验证对发布组中的所有内容运行。 将阻止发布操作成功的任何问题都会显示在将出现在右上角的通知框中。

> [!NOTE]
> 计划发布组时，将始终自动运行验证。 但是，命令栏中的**验证**按钮很有用，因为它有助于发现在尝试计划发布组上线之前必须解决的问题。

## <a name="schedule-a-publish-group-to-go-live"></a>计划发布组上线

若要计划发布组在您的站点上线，请按照下列步骤操作。

1. 在左侧导航窗格中，选择**发布组**。
1. 在**发布组**下，选择要计划的发布组。
1. 在命令栏中，选择**编辑计划**。 将显示**编辑计划**对话框。
1. 选择发布组应该上线的日期和时间，然后选择**确定**。

要取消对发布组的计划，请遵循相同步骤，但是在**编辑计划**对话框中选择**取消发布组计划**。

> [!NOTE]
> 很大的发布组在计划的发布时间到达时可能需要一到两分钟才能发布。 请注意，发布操作不是即时的，较小的发布组将发布得更快。

## <a name="publish-groups-faq"></a>发布组常见问题

**一个发布组中可以有多少个项目？**

当前，每个发布组限制为 2,000 个项目。 请注意，很大的发布组在计划的发布时间到达时可能需要几分钟才能发布。

**发布组是否像软件开发术语中的代码“分支”？**

是，也不是。 发布组可以被视为站点的分支版本。 这样看，它们的确像分支。 但是，没有在单个项目级别的合并概念。 最后发布的项目会覆盖以前存在的项目，最新的发布操作始终会取代之前的发布操作。

**我可以计划两个发布组同时上线吗？**

编号 出于性能和冲突原因，系统将强制您将计划的发布组的上线错开，中间至少间隔五分钟。

**我可以使用发布组计划折扣和产品更新等全渠道后勤办公室项目吗？**

当前，发布组功能仅支持网站内容。 但是，Microsoft 意识到与后勤办公室促销场景集成，对于全渠道市场活动启动的协调和自动化可能很有价值。

## <a name="additional-resources"></a>其他资源

[添加内容的方法](add-manage-content.md)

[页面模型词汇表](page-elements-overview.md)

[文档状态和生命周期](document-states-overview.md)

[使用模块](work-with-modules.md)

[使用片段](work-with-fragments.md)

[模板和布局概览](templates-layouts-overview.md)

[自定义站点导航](customize-site-navigation.md)