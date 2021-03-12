---
title: 补货策略
description: 此主题提供有关补货策略的信息，并说明如何使用波次需求补货模板行上的“补货策略”字段选择补货方式。
author: mirzaab
manager: tfehr
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-29
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 45b3b1a4d2e92a52ee69c17865634a6578181ac7
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646125"
---
# <a name="replenishment-strategies"></a>补货策略

[!include [banner](../includes/banner.md)]

在 **补货模板** 页上定义的模板包括波次需求补货模板行，可用于选择补货的方式。 每一行现在包含一个 **补货策略** 字段。

*波次需求数量* 策略是默认策略。 它是在引入 **补货策略** 字段之前使用的补货策略。 它使用补货位置指令查找可以补货的位置。 然后，为这些位置补货，直到达到需求量。

*最大位置容量* 策略引入了一些新功能。 像 *波次需求数量* 策略一样，此策略使用补货位置指令来查找可以补货的位置，然后为这些位置补货，直到达到需求量。 它不同于 *波次需求数量* 策略，因为所有补货位置将补货到位置库存限制定义的最大容量。 *最大位置容量* 策略尝试创建工作来引入请求的数量以及一些额外数量，以填充要补货的位置。 但是，在有些情况下，该尝试可能失败。 例如，堆放位置可能没有足够的库存来覆盖额外的数量。 在这些情况下，系统会检测到失败，然后尝试恢复。

旺季是 *最大位置容量* 策略优于 *波次需求数量* 策略情况的一个例子。 在旺季，一些物料可能会大量出售。 因此，您可能希望尽可能多地为相关领料位置主动补货，以减少为补货而创建的工作 ID 的数量。

> [!IMPORTANT]
> 要充分利用 *最大位置容量* 策略，您必须重新定义相关位置的库存限制。 否则，此策略就与 *波次需求数量* 策略一样了。

## <a name="turn-on-the-replenish-to-max-based-on-stocking-limits-feature"></a>开启“根据库存限制进行最大补货”功能

此功能只有在系统中开启之后才能使用。 管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区检查此功能的状态和开启功能（如果需要）。 在那里，此功能以以下方式列出：

- **模块**：*仓库管理*
- **功能名称**：*根据库存限制进行最大补货*

## <a name="set-up-replenishment-strategies"></a>设置补货策略

要访问模板，转到 **仓库管理 \> 设置 \> 补货 \> 补货模板**。 在 **概览** 部分，选择或创建波次需求补货模板，其中的 **补货类型** 字段设置为 *波次需求*。 然后在 **补货模板详细信息** 部分设置补货模板行。 对于每一行，在 **补货策略** 字段中，选择要使用的补货策略。

![补货模板页](media/ReplenTempWaveDmdMaxLocCap.png "补货模板页")

如果 **补货策略** 列未出现在 **补货模板详细信息** 部分的网格中，请确保此功能已开启，并且所选补货模板的补货类型为 *波次需求*。

> [!NOTE]
> *波次需求数量* 策略是默认策略。 因此，您只需要更新要使用 *最大位置容量* 策略的补货模板行。

## <a name="example-scenarios"></a>示例方案

### <a name="example-1"></a>示例 1

在此示例中，只有一个补货模板，它只有一个补货模板行。

您为 130 件 (pcs) 物料 A0001 创建了一个销售订单。 在您将订单下达到仓库之前，仓库按以下方式设置：

- 只有一个堆放位置，该位置可用的现有库存量为 500 件。
- 有三个领料位置，每个领料位置的库存限制为 100 件。 （请记住，*最大位置容量* 策略需要有库存限制。）
- 补货放置位置与销售领料位置相同。
- 补货单位是箱（1 箱 = 20 件）。

订购时，以下库存在销售领料位置有现有库存：

- **领料-001：** 20 件（1 箱）
- **领料-002：** 0 件
- **领料-003：** 0 件

最初，补货策略设置为 *波次需求数量*。

将销售订单下达到仓库，波次运行波次处理后，您获得以下补货工作：

- **补货工作 1：** 从堆放位置领取 4 箱，将它们放到位置“领料-001”。
- **补货工作 2：** 从堆放位置领取 2 箱，将它们放到位置“领料-002”。

您将获得两个补货工作 ID，因为您必须为两个位置补货，但不支持多个放置。

如果您将补货策略设置为 *最大位置容量*，您将获得以下补货工作：

- **补货工作 1：** 从堆放位置领取 4 箱，将它们放到位置“领料-001”。
- **补货工作 2：** 从堆放位置领取 5 箱，将它们放到位置“领料-002”。

[![示例 1](media/ReplenTemp_example_1.png "示例 1")](media/ReplenTemp_example_1_large.png)

### <a name="example-2"></a>示例 2

此示例显示了当堆放位置的库存不足以覆盖额外数量时发生的情况。 它使用与示例 1 相同的场景，只是堆放位置有 160 件（8 箱）。

*波次需求数量* 策略创建与示例 1 相同的工作。

但是，由于 *最大位置容量* 策略尝试像示例 1 一样创建工作 ID，这可能会失败。 这时，系统会尝试恢复。

根据补货领料的位置指令上的 **允许拆分** 选项的设置，可能有两种结果：

- 如果 **允许拆分** 选项设置为 *是*，将创建以下补货工作：

    - **补货工作 1：** 从堆放位置领取 4 箱，将它们放到位置“领料-001”。
    - **补货工作 2：** 从堆放位置领取 4 箱，将它们放到位置“领料-002”。

- 如果 **允许拆分** 选项设置为 *否*，将创建以下补货工作：

    - **补货工作 1：** 从堆放位置领取 4 箱，将它们放到位置“领料-001”。
    - **补货工作 2：** 从堆放位置领取 2 箱，将它们放到位置“领料-002”。

结果会因创建工作时可用的信息不同而不同。 当在补货领料的位置指令上将 **允许拆分** 设置为 *是* 时，您知道您最终找到了 160 件。 因此，您可以为该数量创建工作。 但是，当 **允许拆分** 选项设置为 *否* 时，您不知道这 160 件的存在。 因为您决定补货的额外数量是 3 箱，所以您放弃了这个额外数量，再次尝试原始数量。

[![示例 2](media/ReplenTemp_example_2.png "示例 2")](media/ReplenTemp_example_2_large.png)

因此，要为补货位置获得最大数量，应在补货领料的位置指令上将 **允许拆分** 选项设置为 *是*。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]