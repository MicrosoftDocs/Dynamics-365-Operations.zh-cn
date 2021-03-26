---
title: 收入确认重新分配 - 方案 4
description: 本主题介绍了一种重新分配方案，在此方案中从现有的、已部分开票的销售订单中删除一行。 无论从销售订单中删除该行还是将该行设置为已取消状态，此方案都将产生相同的结果。
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
ms.openlocfilehash: 50a2d0d2ca28d9b62713502700f2c4bd2e42751e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238296"
---
# <a name="revenue-recognition-reallocation--scenario-4"></a>收入确认重新分配 - 方案 4

[!include [banner](../includes/banner.md)]

本主题介绍了一种重新分配方案，在此方案中从现有的、已部分开票的销售订单中删除一行。 无论从销售订单中删除该行还是将该行设置为已取消状态，此方案都将产生相同的结果。

对于此方案，**总帐参数** 页面的 **收入确认** 选项卡上的 **将账单更正过帐到应收帐款** 选项设置为 **否**（**收入确认 \> 设置 \> 总帐参数**）。

[![“将账单更正过帐到应收帐款”选项设置为“否”](./media/37_rev-rec-scenarios.png)](./media/37_rev-rec-scenarios.png)

为客户 US\_SI\_0003 创建了一个销售订单。 客户正在购买笔记本电脑（项目编号 S0012）、安装服务（项目编号 S0001）和针对笔记本电脑的支持计划（项目编号 S0008，“持续的工程服务”）。 将立即确认笔记本电脑和安装服务的收入。 支持计划的收入将延期并在根据合同中日期范围定义的 12 个月内确认。

[![笔记本电脑、安装服务和支持计划的销售订单行](./media/38_rev-rec-scenarios.png)](./media/38_rev-rec-scenarios.png)

已确认销售订单。 因为所有三个项目都是为收入价格分配设置的，所以在确认销售订单时将计算收入价格。 您可以查看将在 **收入价格分配** 页面（在 **销售订单** 页面的操作窗格的 **管理** 选项卡上的 **收入确认** 组中，选择 **收入价格分配**）上确认的收入。 笔记本电脑的收入将以 $995.84 的金额过帐到收入帐户。 安装服务的收入也将以 $314.47 的金额过帐到收入帐户。 支持计划的收入将以 $188.69 的金额过帐到延期收入帐户。 收入价格的总和必须等于为获取收入价格分配 ($1,499.00) 而设置的总行数。

[![收入价格分配页面](./media/39_rev-rec-scenarios.png)](./media/39_rev-rec-scenarios.png)

针对笔记本电脑和支持计划为客户进行了开票，但未针对安装服务开票。 下图显示了针对账单过帐的会计条目。

[![已开票的销售订单的会计条目](./media/40_rev-rec-scenarios.png)](./media/40_rev-rec-scenarios.png)

会计条目将 $1,276.94 过账至应收帐款。 但是，由于此账单为部分账单，因此收入或延期收入加上税款不等于应收帐款金额。 -$14.47 的差额将过帐到部分账单收入结算帐户。

此外，还将创建收入确认计划。

[![部分账单的收入确认计划页面](./media/41_rev-rec-scenarios.png)](./media/41_rev-rec-scenarios.png)

后来，客户决定不购买安装服务。 因此，从销售订单中删除了该行。 请注意，无法再次确认销售订单，因为只有已开票的行保留在销售订单上。

[![删除安装服务行后的销售订单](./media/42_rev-rec-scenarios.png)](./media/42_rev-rec-scenarios.png)

即使无法确认销售订单，也可以对其重新分配。 在销售订单中，选择 **使用新订单行重新分配价格** 以打开 **使用新订单行重新分配价格** 页面。 选择剩余的两个销售订单行，然后选择 **更新重新分配**。 **重新分配的金额** 列显示每个剩余的销售订单行的新收入价格。

[![“使用新订单行重新分配价格”页面上的新收入价格](./media/43_rev-rec-scenarios.png)](./media/43_rev-rec-scenarios.png)

接下来，选择 **预期凭证** 以查看会计条目。

[![预期凭证页面上的会计条目](./media/44_rev-rec-scenarios.png)](./media/44_rev-rec-scenarios.png)

在 **预期凭证** 页面上，最后五行将冲销已过帐账单中的原始会计条目。 前四行是为账单过帐的新会计条目。 务必要了解未向客户显示新账单。 重新分配后，客户仍欠 $1,276.94，这是必须过帐到该新会计条目中的应收帐款的金额。 新收入或延期收入加上税款等于 $1,276.94。 因此，不必过帐到部分账单收入结算帐户。

要完成重新分配，请选择 **处理**。 输入了过帐日期。 重新分配完成后，**收入价格分配** 页面将显示剩余两个项目的价格重新分配。

[![收入价格重新分配页面上的剩余项目的价格重新分配](./media/45_rev-rec-scenarios.png)](./media/45_rev-rec-scenarios.png)

还根据新的收入重新分配价格更新了收入确认计划。 通过销售订单打开 **收入确认计划** 页面。 以前，项目 S0008 有 13 行（为此项目分配了 12 个月的计划）。 现在有 39 行：13 个原始计划行、13 个冲销计划行和 13 个基于新收入价格的行。

[![更新了收入确认计划页面，其中项目 S0008 有 39 行](./media/46_rev-rec-scenarios.png)](./media/46_rev-rec-scenarios.png)

选择 **凭证** 时，账单日记帐将显示原始会计条目。 要查看销售订单中的冲销条目和新会计条目，请选择操作窗格上的 **收入调整**，然后选择 **凭证**。

接下来，打开 **所有客户** 页面（**应收账款 \> 客户 \> 所有客户**），选择客户 **US\_SI\_0003**，然后选择 **交易**。 **客户交易** 页面仅显示了原始账单 (000008) 以及原始会计条目。 由于 **总帐参数** 页面上的 **将账单更正过帐到应收帐款** 选项设置为 **否**，因此仅更新了总帐。 所以，未显示冲销和更新的会计条目。 请注意，显示了在[方案 3](rev-rec-reallocation-scenario-3.md)中创建的收入调整交易记录。

[![客户交易页面上的原始会计条目](./media/47_rev-rec-scenarios.png)](./media/47_rev-rec-scenarios.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]