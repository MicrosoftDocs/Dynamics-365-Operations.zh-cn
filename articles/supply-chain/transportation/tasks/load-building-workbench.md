---
title: 装载计划工作台
description: 本主题介绍如何使用负荷构建工作台。
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSLoadBuildWorkbench,TMSLoadBuildTemplateCreate,TMSLoadBuildStrategy,TMSLoadBuildTemplateApply
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d1ed91adba5c7accf9a18d7a754d33b2b35b848f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974214"
---
# <a name="load-building-workbench"></a>装载计划工作台

负荷构建工作台可让您在创建负荷时应用负荷构建策略。

## <a name="create-a-load-building-strategy"></a>创建负荷构建策略

使用负荷构建策略自动构建负荷。 在以下情况下，此功能可能会很有用：

- 如果您定期装运一组特定产品，负荷策略有助于节省时间，因为您不必每次都构建相同的负荷。
- 如果要避免半满负荷以最大程度地提高效率，负荷策略可以帮助尽可能多地填充每个负荷。

名为 `TMSLoadBuildingVolumeStrategy` 的负荷构建策略类提供名为 *基于体积的负荷构建策略* 的负荷构建策略。 此策略允许您在装载模板上为高度和重量指定最大值，或您可以通过输入新的值来覆盖设置。 此策略是随附开箱即用的唯一策略。 （但是，您可能有一些自定义策略。）

若要使用开箱即用的 *基于体积的负荷构建策略* 策略，请在 **负荷构建工作台** 页面（**运输管理 &gt; 计划 &gt; 负荷构建工作台**）上的 **负荷构建策略** 字段中选择它。

若要创建负荷构建策略，请执行以下步骤。

1. 转到 **运输管理 &gt; 设置 &gt; 负荷构建 &gt; 负荷构建策略**。
1. 在操作窗格上，选择 **生成类列表** 以确保您具有所有可用类的最新版本。
1. 在操作窗格上，选择 **新建**。
1. 输入策略的唯一名称，为其选择负荷构建策略类，然后输入描述。
1. 在操作窗格上，选择 **保存**。
1. 在操作窗格中，选择 **参数**。
1. 在 **负荷构建策略参数** 页面上，在列表中选择 **体积容量**，然后在 **值** 字段中，输入应该应用于新负荷构建策略的负荷总体积容量的百分比。
1. 在列表中选择 **重量容量**，然后在 **值** 字段中，输入应该应用于新负荷构建策略的负荷总重量容量的百分比。
1. 关闭 **负荷构建策略参数** 页面。
1. 关闭 **负荷构建策略** 页面。

现在，您可以将负荷构建策略分配给负荷构建模板。 或者，您可以直接在负荷计划工作台中使用它。

## <a name="use-a-load-building-strategy-in-the-load-building-workbench"></a>在负荷构建工作台中使用负荷构建策略

1. 转到 **运输管理 &gt; 计划 &gt; 负荷构建工作台**。
1. 按以下步骤之一：

    - 在 **负荷构建策略** 字段中选择策略。
    - 如果您已定义负荷构建模板并已向其分配负荷构建策略，请在操作窗格的 **管理模板** 选项卡上，选择 **应用模板**。 然后，在 **应用负荷构建模板** 下拉对话框中，在 **负荷构建模板名称** 字段中选择模板。

1. 在 **负荷模板序列** 快速选项卡上，选择一个或多个[负荷模板](load-template.md)。 工作台将尝试按此处指定的顺序将负荷装入这些类型的容器中。 通常，应将最小的容器放在列表顶部，以确保首先选择可能的最小容器。
1. 在操作窗格上，选择 **建议负荷**。
1. 查看建议的负荷和建议的负荷行。
1. 在操作窗格上，选择 **创建负荷** 以创建基于 **建议的负荷行** 快速选项卡上的源单据行的负荷。
1. 关闭 **负荷构建工作台** 页面。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]