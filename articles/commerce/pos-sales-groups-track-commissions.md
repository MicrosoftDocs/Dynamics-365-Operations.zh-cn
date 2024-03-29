---
title: 使用销售组跟踪销售点 (POS) 中的佣金
description: 零售业中经常由与客户打交道的销售员跟踪销售 — 提供协助、追加销售、交叉销售和处理交易记录。
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.industry: Retail
ms.openlocfilehash: 5a5cdf57d8c920b105e7f4a457b064cb2ceba242
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272787"
---
# <a name="track-commissions-in-the-point-of-sale-pos-by-using-sales-groups"></a>使用销售组跟踪销售点 (POS) 中的佣金

[!include [banner](includes/banner.md)]

零售业中经常由与客户打交道的销售员跟踪销售 — 提供协助、追加销售、交叉销售和处理交易记录。

销售代表跟踪销售是销售员销售能力的一种度量，而收银员销售则是速度和效率的度量。 通常也通过销售代表跟踪的销售来计算佣金或其他激励。

## <a name="configuring-a-worker-to-be-a-sales-representative-in-pos"></a>在 POS 中将工作人员配置为销售代表

将工作人员添加到销售组时，其即可享受佣金，并可以在系统中识别为销售代表。 不属于销售组的工作人员没有资格享受佣金，并且不能在销售点 (POS) 应用程序中的作为销售代表列出。 在 POS 中，销售代表列表派生自至少包含一个为商店分配的工作人员的所有销售组。 此列表在 POS 中显示为销售组 ID 和名称的组合（ID：名称）。 可以为工作人员配置默认销售组，以便支持满足以下条件的方案：零售商选择自动在 POS 行中设置销售代表。 用户可从工作人员所属任何销售组进行选择。

## <a name="functionality-profile-settings"></a>功能配置文件设置

商店有一些功能配置文件设置可用于确定 POS 中涉及销售代表的流和流程。

<table>
<thead>
<tr>
<th>配置文件</th>
<th>说明</th>
</tr>
</thead>
<tbody>
<tr>
<td>默认为出纳(如果可用)</td>
<td>如果启用此选项，POS 将自动使用当前收银员的默认销售组填充交易记录行。 如果不为收银员指定默认销售组，则不设置此值。 用户仍然可以通过使用 POS 按钮网格按钮手动设置销售组。</td>
</tr>
<tr>
<td>销售代表的提示</td>
<td>此选项包含三个可能的值：
<ul>
<li><strong>否</strong> – 如果选择此选项，则不提示用户选择销售组。 仍然可以通过使用收银员的默认销售组设置此值，或通过使用 POS 按钮网格按钮手动设置。</li>
<li><strong>交易记录开始</strong> – 如果选择此选项，并且不启用<strong>默认为收银员</strong>选项或当前收银员无默认销售组，将在每个交易记录开始时提示用户选择销售组。 从该提示选择销售组将把所有后续行默认设置为所选销售组。 用户仍然可以通过使用 POS 按钮网格按钮手动设置销售组。</li>
<li><strong>对于每行</strong> – 如果选择此选项，并且不启用<strong>默认为收银员</strong>选项或当前收银员无默认销售组，将在添加每行后提示用户选择销售组。 用户仍然可以通过使用 POS 按钮网格按钮手动设置销售组。</li>
</ul>
</td>
</tr>
<tr>
<td>需要</td>
<td>此选项仅适用于 POS 配置为提示需要指定销售代表时。 如果启用，将要求用户先选择销售组，才能继续操作。 否则，将提示用户，但是可以取消并在不进行选择的情况下继续操作。 添加行之后，拥有足够权限的用户仍然可以从行中删除销售组。 此方案中不实施“需要销售代表”。</td>
</tr>
</tbody>
</table>

## <a name="displaying-the-sales-representative-information-on-the-pos-transactions-screen"></a>在 POS 交易记录屏幕中显示销售代表信息

可使用屏幕布局设计器和为商店、收银机或工作人员指定的屏幕布局配置 POS 交易记录屏幕布局和内容。 可将 **销售代表** 字段添加到“收据”窗格的“行”选项卡。  这将为交易记录屏幕中的各行显示指定销售组的 ID。

## <a name="adding-sales-representative-operations-to-pos-button-grids"></a>向 POS 按钮网格添加销售代表操作

POS 允许用户配置按钮网格，按钮网格包含在屏幕布局中，用于访问 POS 操作。 可将以下 POS 操作分配给属于销售代表的按钮网格按钮。

| 工序                                 | 说明 |
|-------------------------------------------|-------------|
| 设置行上的销售代表          | 此 POS 操作显示符合商店条件的销售组（ID：名称）的列表。 从此列表中选择一个销售组将在当前交易记录行中设置值。 |
| 清除行上的销售代表        | 此 POS 操作从当前交易记录行删除当前销售组值。 |
| 设置交易记录上的销售代表   | 此 POS 操作显示符合商店条件的销售组（ID：名称）的列表。 从此列表中选择一个销售组将在当前交易记录中设置默认值。 将设置未为其分配销售组的任何现有行，以及以后添加的任何行。 |
| 清除交易记录上的销售代表 | 此 POS 操作从当前交易记录删除当前默认销售组值。 不影响交易记录中已有的任何行。 |

## <a name="calculating-commissions"></a>计算佣金

对账单过帐或销售订单过帐时，将为指定销售组中的工作人员计算佣金。 将根据交易记录中客户和/或产品的销售组和关联佣金计算设置中定义的工作人员佣金份额，确定佣金金额。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
