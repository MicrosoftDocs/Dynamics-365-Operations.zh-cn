---
title: 收入确认重新分配 - 方案 3
description: 本主题介绍了一种重新分配方案，在此方案中将一个新行添加到现有的、已开票的销售订单中。 将一个新项目添加到合同中时，既可以将其添加到一个新销售订单，也可以添加到现有销售订单。
author: kweekley
manager: aolson
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 51646d27fe8c343c99360815d22949ffe0757979
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003346"
---
# <a name="revenue-recognition-reallocation--scenario-3"></a>收入确认重新分配 - 方案 3

[!include [banner](../includes/banner.md)]

本主题介绍了一种重新分配方案，在此方案中将一个新行添加到现有的、已开票的销售订单中。 将一个新项目添加到合同中时，既可以将其添加到一个新销售订单，也可以添加到现有销售订单。 此方案还显示了由于重新分配而更新应收帐款时发生的情况。

对于此方案，**总帐参数** 页面的 **收入确认** 选项卡上的 **将账单更正过帐到应收帐款** 选项设置为 **是**（**收入确认 \> 设置 \> 总帐参数**）。

[![“将账单更正过帐到应收帐款”选项设置为“是”](./media/25_rev-rec-scenarios.png)](./media/25_rev-rec-scenarios.png)

为客户 US\_SI\_0003 创建了一个销售订单。 客户正在购买笔记本电脑（项目编号 S0012）和支持计划（项目编号 S0008，“持续的工程服务”）。 将立即确认笔记本电脑的收入。 支持计划的收入将延期并在根据合同中日期范围定义的 12 个月内确认。

[![笔记本电脑和支持计划的销售订单行](./media/26_rev-rec-scenarios.png)](./media/26_rev-rec-scenarios.png)

已确认销售订单。 因为两个项目都是为收入价格分配设置的，所以在确认销售订单时将计算收入价格。 您可以查看将在 **收入价格分配** 页面（在 **销售订单** 页面的操作窗格的 **管理** 选项卡上的 **收入确认** 组中，选择 **收入价格分配**）上确认的收入。 笔记本电脑的收入将以 $1,008.01 的金额过帐到收入帐户。 支持计划的收入将以 $190.99 的金额过帐到延期收入帐户。 收入价格的总和必须等于为获取收入价格分配 ($1,199.00) 而设置的总行数。

[![收入价格分配页面](./media/27_rev-rec-scenarios.png)](./media/27_rev-rec-scenarios.png)

已对销售订单完全开票。 下图显示了针对账单过帐的会计条目。

[![完全开票的销售订单的会计条目](./media/28_rev-rec-scenarios.png)](./media/28_rev-rec-scenarios.png)

此外，还将创建收入确认计划。 经过一段时间（即两个月）后确认了该支持计划的收入。

[![两个月过去之后的收入确认计划页面](./media/29_rev-rec-scenarios.png)](./media/29_rev-rec-scenarios.png)

此时，客户决定添加安装服务（项目编号 S0001）。 此项目已添加到现有销售订单中。 提示客户确认他们要修改已完全开票的销售订单，然后他们选择 **是**。

[![添加安装服务行后的销售订单](./media/30_rev-rec-scenarios.png)](./media/30_rev-rec-scenarios.png)

如果此新项目是对客户合同的唯一更改，则现在可以运行重新分配流程。 在销售订单中，选择 **使用新订单行重新分配价格** 以打开 **使用新订单行重新分配价格** 页面。 选择此销售订单的所有销售订单行，然后选择 **更新重新分配**。 **重新分配的金额** 列显示每个销售订单行的新收入价格。

[![“使用新订单行重新分配价格”页面上的新收入价格](./media/31_rev-rec-scenarios.png)](./media/31_rev-rec-scenarios.png)

接下来，选择 **预期凭证** 以查看会计条目。 由于 **总帐参数** 页面上的 **将账单更正过帐到应收帐款** 选项设置为 **是**，因此这些会计条目将通过贷方凭证过账到总帐，并将在应收帐款中创建一个新账单。

[![预期凭证页面上的会计条目](./media/32_rev-rec-scenarios.png)](./media/32_rev-rec-scenarios.png)

在 **预期凭证** 页面上，最后四行将冲销已过帐账单中的原始会计条目。 前五行是为账单过帐的新会计条目。 务必要了解未向客户显示新账单。 重新分配后，客户仍欠 $1,276.94，这是必须过帐到该新会计条目中的应收帐款的金额。 抵消税及收入或延期收入等于 $995.83 + $188.69 + $77.94 = $1,262.46。 由于重新分配，收入或延期收入金额已更改。 -$14.48 的差额将过帐到部分账单收入结算帐户。 当为已添加到销售订单的新项目过帐账单时，将对此余额进行结算。

要完成重新分配，请选择 **处理**。 输入了过帐日期。 重新分配完成后，**收入价格分配** 页面将显示所有三个项目的价格重新分配。

[![收入价格重新分配页面上的所有三个项目的价格重新分配](./media/33_rev-rec-scenarios.png)](./media/33_rev-rec-scenarios.png)

还根据新的收入重新分配价格更新了收入确认计划。 通过销售订单打开 **收入确认计划** 页面。 以前，项目 S0008 有 13 行（为此项目分配了 12 个月的计划）。 现在有 39 行：13 个原始计划行、13 个冲销计划行和 13 个基于新收入价格的行。

[![更新了收入确认计划页面，其中项目 S0008 有 39 行](./media/34_rev-rec-scenarios.png)](./media/34_rev-rec-scenarios.png)

选择 **凭证** 时，账单日记帐将显示原始会计条目。 要查看销售订单中的冲销条目和新会计条目，请选择操作窗格上的 **收入调整**，然后选择 **凭证**。

接下来，打开 **所有客户** 页面（**应收账款 \> 客户 \> 所有客户**），选择客户 **US\_SI\_0003**，然后选择 **交易**。 **客户交易** 页面显示了原始账单 (000006)、冲销凭证 (000006-1) 和新账单 (000006-2)。 原始账单和冲销凭证将彼此作为依据进行结算，并且余额为 0（零）。 查看每个文档的凭证，以查看总账中的影响。

[![“客户交易”页面上的原始账单、冲销凭证和新账单](./media/35_rev-rec-scenarios.png)](./media/35_rev-rec-scenarios.png)

再次针对添加的项目为销售订单开票。 对客户显示的总账单为 $300.00 + $19.50 (税) = $319.50。 下图显示了已过帐的会计条目。

[![凭证交易页面，其中包含已过帐的会计条目](./media/36_rev-rec-scenarios.png)](./media/36_rev-rec-scenarios.png)

由于收入和销售额的总和超过 $319.50，因此过帐的差额为 $14.48。 此金额将清除部分账单收入结算帐户中的余额。 重新分配后，将在已过帐的新会计条目中更新该余额。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]