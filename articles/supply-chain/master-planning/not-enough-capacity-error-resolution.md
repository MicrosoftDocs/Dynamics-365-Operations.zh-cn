---
title: 修复“找不到足够的产能”计划编制引擎错误和有限产能
description: 本文提供有关无法为生产订单 %1 计划编制的原因和解决方法的信息。 找不到足够的产能”计划编制引擎错误。
author: t-benebo
ms.date: 7/29/2021
ms.topic: article
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-19
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d4f54c06a07b3cdd0b8fe2cc52614189ff31ba7f
ms.sourcegitcommit: 6b209919de39c15e0ebe4abc9cbcd30618f2af0b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/11/2022
ms.locfileid: "9135590"
---
# <a name="fix-the-not-enough-capacity-could-be-found-scheduling-engine-error"></a>修复“找不到足够的产能”计划编制引擎错误

[!include [banner](../includes/banner.md)]

运行计划编制时，您可能会收到以下错误消息：

> 无法计划生产订单 %1。 找不到足够产能。

计划编制引擎失败并发出此错误消息的原因有几个。 本文提供指南来帮助您找到错误根源，然后加以缓解。

## <a name="review-the-applicable-resources"></a>检查适合的资源

如果没有适合的资源来满足生产订单站点的工序要求，可能会发生此错误。

若要查看使用资源，请执行以下步骤。

1. 转到 **生产控制 \> 生产订单 \> 所有生产订单**，然后打开或选择不能计划编制的生产订单。
1. 在操作窗格上，在 **生产订单** 选项卡的 **生产详细信息** 组中，选择 **工艺路线**。
1. 在 **生产工艺路线** 页面上，选择工序，然后在操作窗格上选择 **适合的资源**。
1. 在 **适合的资源** 对话框中，将 **使用要求** 字段设置为 *工序级计划编制* 或 *作业级计划编制*，具体取决于要使用的计划编制类型。
1. 确保生产订单站点有适合的资源。

## <a name="review-the-calendars-that-are-associated-with-resources"></a>检查与资源关联的日历

如果没有日历与资源或资源组关联，或者未正确设置关联的日历（例如，它没有工作时间或其效率百分比为 0 \[零\]），则可能会出现此错误。

若要验证是否为资源或资源组关联了日历，请执行以下步骤。

1. 转到 **生产控制 \> 生产订单 \> 所有生产订单**，然后打开或选择不能计划编制的生产订单。
1. 在操作窗格上，在 **生产订单** 选项卡的 **生产详细信息** 组中，选择 **工艺路线**。
1. 在 **生产工艺路线** 页面上，选择工序，然后在操作窗格上选择 **适合的资源**。
1. 在 **适合的资源** 对话框中，选择资源，然后选择 **查看资源**。 或者，在 **资源组** 字段中选择并按住（或右键单击），然后选择 **查看详细信息**。
1. 在 **资源** 页面或 **资源组** 页面的 **日历** 快速选项卡中，确保资源或资源组已与日历关联。

> [!NOTE]
> 如果在工序计划编制期间出错，必须确保一个日历与所有适合的资源组关联。

若要查看日历的设置，请执行以下步骤。

1. 转到 **组织管理 \> 设置 \> 日历 \> 日历**，然后选择与资源或资源组关联的日历。
1. 在操作窗格上，选择 **工作时间**。
1. 在 **工作时间** 页面上，请确保页面不为空。 此外，对于您感兴趣的日期，请确保 **控制** 字段未设置为 *已关闭*，存在工作时间，并且 **效率百分比** 字段未设置为 *0*（零）。

如果日历与基础日历关联，您还必须检查基础日历的设置。

> [!NOTE]
> 在工序计划编制中，资源组的日历用于确定每个工序的开始和结束时间和日期。 它还限制系统可以为一个特定资源组中一个特定日期的一个特定工序安排的时间量。 例如，如果某个特定日期一个资源组的工作时间为上午 8:00 到下午 4:00，则一个工序为该资源组施加的负载不能超过八小时内适合安排的负荷，无论该资源组在当天是否有可用产能。 但是，可用产能可以进一步限制负载。

## <a name="review-the-scheduling-parameters"></a>检查计划编制参数

为了确保绩效高，计划编制引擎将仅搜索特定时间量的资源和特定数量的计划编制冲突。

若要查看计划编制参数，请执行以下步骤。

1. 转到 **组织管理 \> 设置 \> 计划编制参数**。
1. 按以下步骤之一：

    - 如果 **计划编制超时已启用** 选项设置为 *否*，请转到步骤 3。
    - 如果 **计划编制超时已启用** 选项设置为 *是*，请增加 **每个序列的最大计划编制时间** 字段的值，以便为处理提供更多完成时间。

1. 按以下步骤之一：

    - 如果 **计划编制优化超时已启用** 选项设置为 *否*，请转到步骤 4。
    - 如果 **计划编制优化超时已启用** 选项设置为 *是*，请增加 **优化尝试超时** 字段的值，以便为处理提供更多完成时间。

1. 如果更改了此页面上的任何设置，请重新安排订单以重试。

## <a name="review-capacity"></a>检查产能

执行有限计划编制时可能出错，无空闲产能。

若要执行无限产能计划编制，请执行以下步骤。

1. 转到 **生产控制 \> 生产订单 \> 所有生产订单**，然后选择或打开不能计划编制的生产订单。
1. 在操作窗格的 **计划** 选项卡上 **生产订单** 组中，选择 **计划工序** 或 **计划作业**。
1. 在 **工序级计划编制** 或 **作业级计划编制** 对话框中，将 **有限产能** 选项设置为 *否*。
1. 选择 **确定** 为订单排产。

若要查看资源的可用产能，请执行以下步骤。

1. 转到 **组织管理 \> 资源 \> 资源**，然后选择适合不能排产的订单的资源。
1. 在操作窗格上 **资源** 选项卡中 **视图** 组内，选择 **产能负荷** 或 **产能负荷，图形方式**，然后确保有可用产能。

若要查看资源组的可用产能，请执行以下步骤。

1. 转到 **组织管理 \> 资源 \> 资源组**，然后选择适合不能排产的订单的资源组。
1. 在操作窗格上 **资源组** 选项卡中 **视图** 组内，选择 **产能负荷** 或 **产能负荷，图形方式**，然后确保有可用产能。

## <a name="master-planning-books-a-resource-when-the-resource-calendar-is-closed"></a>关闭资源日历时主计划会预订资源

使用工序计划时，主计划将根据主要资源组的日历来计划产能。 它与主要工序同时预订次要工序，并且不考虑次要工序的日历或产能。 这可能导致在已关闭日历上或在次要工序不可用（日历已关闭，无产能）时计划生产订单。

在使用作业计划时，主计划将在计划订单时同时考虑主要工序和次要工序的产能和日历。 要计划订单，这两个工序的资源的日历都必须为“开启”且具有可用产能。

## <a name="maximum-job-lead-time-is-too-short"></a>最长工作提前期太短

如果为您的站点设置的 **最长作业提前期** 小于在其默认订单设置或覆盖范围设置中为物料指定的提前期，则计划引擎将无法计划订单。

若要查看或编辑站点的 **最长作业提前期** 设置，请转到 **生产控制 \> 设置 \> 生产控制参数**，并打开 **常规** 选项卡。

若要查看或编辑物料的默认订单设置，请按照下列步骤操作：

1. 转到 **产品信息管理 \> 产品 \> 已发布产品**。
1. 在列表中查找并选择相关产品。
1. 在操作窗格上，打开 **管理库存** 选项卡，并选择 **默认订单设置**。
1. 展开 **库存** 快速选项卡并根据需要查看或编辑 **库存提前期** 设置。

若要查看或编辑物料的覆盖范围设置，请按照下列步骤操作：

1. 转到 **产品信息管理 \> 产品 \> 已发布产品**。
1. 在列表中查找并选择相关产品。
1. 在操作窗格上，打开 **计划** 选项卡并选择 **物料覆盖范围**。
1. 打开 **提前期** 选项卡，并根据需要查看或编辑 **生产时间** 值。

## <a name="excessive-quantity-of-required-resources"></a>所需资源数量过多

在计划过程中，引擎会根据工序资源需求，尝试将为工艺路线工序设置的所需资源数量与适用的资源相匹配。 设置的资源数量过高可能会导致工艺路线不可行，这将导致计划错误。

使用以下过程检查所选产品、工艺路线和工艺路线工序的指定数量和适用资源：

1. 转到 **产品信息管理 \> 产品 \> 已发布产品**。
1. 在网格中查找并选择相关产品。
1. 在操作窗格上，打开 **工程师** 选项卡，然后选择 **工艺路线**。
1. 在网格中查找并选择相关的工艺路线。
1. 打开到页面底部的 **概览** 选项卡。
1. 从所选工艺路线工序列表中选择一个工序。
1. 选择 **适用资源** 以打开对话框，您可以在其中查看所选工艺路线工序的适用资源。
1. 打开 **资源负荷** 选项卡。此处的 **数量** 字段显示所选工艺路线工序所需的资源数量。 根据需要查看和/或编辑它。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
