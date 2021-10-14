---
title: 内部公司主计划编制
description: 本主题介绍了内部公司主计划编制
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: e28051097905503e291e0c15a50e9363b39b2daa
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548125"
---
# <a name="intercompany-master-scheduling"></a>内部公司主计划编制

[!include [banner](../../includes/banner.md)]

内部公司主计划编制是用来计算需求和生成计划的内部公司订单，跨若干内部公司的方式。 内部公司主计划编制按指定数目的重复执行。 若要启用 Microsoft Dynamics 365 Supply Chain Management 执行内部公司主计划编制，您必须在每个集团内公司设置主计划编制。 这就需要 Microsoft Dynamics 365 Supply Chain Management 执行若干次迭代，以自动创建内部公司采购订单。这样将会自动创建内部公司销售订单，从而引发新的需求。

在每个集团内公司的 **主计划** 参数中，可以设置内部公司主计划和内部公司计划订单。

为了在该内部公司业务关系链中传递需求，必须设置参数确保自动确定计划的采购订单，即的时间或数量不能进行更改。 在覆盖范围组上设置 **确认时限**，或在主计划中设置 **确认时限**。 如果 **确认时限** 未设置，内部公司采购订单将不会自动创建。 仅在第一次执行主计划编制时才会产生计划订单。 但是，由于未创建内部公司采购订单，因此未创建内部公司销售订单，因此，不会再创建内部公司采购订单，等等。

启动内部公司主计划编制时，Microsoft Dynamics 365 Supply Chain Management 将在每个集团内公司中执行一次主计划编制，然后在每个集团内公司执行第二次主计划编制，依此类推，直到达到指定的迭代次数为止。 最大迭代次数为 30，但是，选择的迭代次数越多，计划执行的时间就越长。

因为内部公司的主计划编制由内部公司的计划编制顺序（即程序在各个集团内公司之间执行主计划时的先后顺序）控制，所以，可以从任一个集团内公司开始内部公司主计划编制。 由于内部公司计划编制顺序确定了在各个公司执行主计划编制的顺序，因此，内部公司主计划编制的开始位置并不重要。 在每次迭代中，当前公司总是最后一个执行。

> [!NOTE]
> 最好的方法是允许内部公司主计划编制通过一个 Microsoft Dynamics 365 Supply Chain Management 公司启动。

在 **内部公司主计划编制** 页面上，可以启动主计划编制的序列。即：使用更新需求计算时的原则首次执行主计划编制。该原则是为所有内部公司的首次迭代选择的。 后续的迭代将使用为下一次迭代选择的备用原则。此原则将一直适用，直到达到所指定的迭代次数为止。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
