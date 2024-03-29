---
title: 覆盖范围设置
description: 本文提供有关主计划编制用于计算物料要求的覆盖范围设置的信息。
author: t-benebo
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard, ReqItemTableSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fcbf053a32ef2921aab9a81de68e5844f5cb6527
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740240"
---
# <a name="coverage-settings"></a>覆盖范围设置

[!include [banner](../includes/banner.md)]

主计划编制使用覆盖范围设置计算物料需求。

您可以通过以下几种方式指定覆盖范围设置：

- 为覆盖范围组指定覆盖范围设置。

    您可以创建一个覆盖范围组，它包含与该组关联的所有产品的设置。 若要创建覆盖范围组，请转到 **主计划 &gt; 设置 &gt; 覆盖范围 &gt; 覆盖范围组**。 您可以将覆盖范围组与某个产品链接。 如果链接特定于站点、仓库或产品维度，请使用 **物料覆盖范围** 页的 **覆盖范围组** 字段。 如果链接是通用的，无论产品维度如何，请使用 **产品详细信息** 页的 **计划** 快速选项卡上的 **覆盖范围组** 字段。 默认情况下，如果您没有将某一覆盖范围组与某一产品关联，则主计划将使用在 **主计划参数** 页中指定的一般覆盖范围组作为默认覆盖范围组。

- 为产品指定覆盖范围设置。

    您可为特定产品创建覆盖范围设置。 转到 **产品信息管理 &gt; 产品 &gt; 已发布产品**。 选择产品，然后在操作窗格上的 **计划** 选项卡中 **覆盖范围组** 中，选择 **物料覆盖范围** 打开 **物料覆盖范围** 页。 如果该产品已链接到某一覆盖范围组，则您可以使用 **覆盖** 字段覆盖该覆盖范围组设置。 **物料覆盖范围** 页上的覆盖范围设置优先于 **覆盖范围组** 页上的设置。

- 使用向导为产品指定覆盖范围设置。

    此向导将引导您逐步执行主物料覆盖范围参数设置流程。 在 **物料覆盖范围** 页上的操作窗格中，选择 **向导** 打开 **物料覆盖范围向导**。

- 为维度组指定覆盖范围设置。

    转到 **产品信息管理 &gt; 产品 &gt; 已发布产品**。 在 **已发布产品详细信息** 页上，在 **常规** 快速选项卡上，在 **管理** 部分中，选择 **存储维度组** 字段中的链接。 在 **存储维度组** 页，选择 **按维度的覆盖范围计划** 复选框为存储维度组中的维度创建覆盖范围设置。 必须为所有产品维度（如配置、颜色、尺寸和样式）选择 **按维度的覆盖范围计划** 字段。


## <a name="coverage-codes"></a>覆盖范围代码

主计划可以配置为使用不同的补货方法。 补货方法或批次规模方法是系统用于确定已购买或已生产物料的批次大小的技术。 

每个补货方法都分配了以下覆盖范围代码之一：

- **手动** - 系统不为物料建议采购订单、转移单或生产订单的批次规模方法。 物料规划员将负责为物料补货创建所需订单。
- **根据需求** - 系统根据需求为物料创建计划采购订单、转移单或生产订单的批次规模方法。 通常用于具有间断需求的昂贵物料。  
- **根据期间** - 将一个期间的所有需求合并为物料的一个订单的批次规模方法。 订单将期间的第一天进行计划，其数量将在确定的期间内满足净需求。 期间从物料的第一个需求开始，覆盖定义的时间长度。 下一个期间将从物料的下一个需求开始。
- **最小/最大** - 当预计的现有量低于阈值时，将库存补货提高到某个级别的批次规模方法。 补货数量将是最大级别与预计现有量级别之间的差值。


## <a name="additional-resources"></a>其他资源

- [主计划概览](master-plans.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]