---
title: 运输管理概览
description: 本主题提供 Supply Chain Management 中运输管理功能的概览。
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSParameters,TMSRateRouteWorkbench, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 30251
ms.assetid: d4e3550c-bca8-469c-82df-56ac0083e4ac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa59a8e6e4744c776ec0e1dc84b1f004dbd796f6
ms.sourcegitcommit: 0099fb24f5f40ff442020b488ef4171836c35c48
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/23/2019
ms.locfileid: "2653571"
---
# <a name="transportation-management-overview"></a>运输管理概览

[!include [banner](../includes/banner.md)]

本主题提供 Supply Chain Management 中运输管理功能的概览。

“运输管理”能让您使用公司的运输，还能让您为进货和出货订单标识供应商和路线解决方法。 例如，您可以标识装运的最快路线或最便宜费率。 下表描述使用运输管理的主要情况。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>场景</th>
<th>运输管理如何提供帮助</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>为运输活动使用外部物流提供商。</td>
<td>为入站和/或出站运使用运输管理。</td>
</tr>
<tr class="even">
<td>公司自己的车队可用于交货/装货，交货费用向客户收取。</td>
<td>对于出站流程，您可以使用运输管理来确定运输费用并将费用传递给客户。 不过，不需要承运人发票对帐流程。</td>
</tr>
<tr class="odd">
<td>公司自己的车队可用于交货/装货，但交货费用不由客户承担，因为产品价格包括运输费用。</td>
<td>不需要大量运输管理功能。 但是，您可以使用运输管理来确定运输费率和相应调整销售价格。</td>
</tr>
<tr class="even">
<td>物流服务由同一公司的另一法人提供。</td>
<td><ul>
<li>您可以通过将其他法人视为任何其他装运承运人来使用运输管理。 您不能将法人之间的经济交易记录自动化。 因此，您必须手动处理这些交易记录（例如，通过创建采购订单）。</li>
<li>在提供物流服务的法人中，运输管理可用于确定运输费用。</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="planning-transportation-in-supply-chain-management"></a>在 Supply Chain Management 中计划运输
在运输管理中， 运输计划可以基于订单或基于根据这些订单创建的装运。 装运在某个时间点上始终存在，但对运输计划不是必需的。 转移单是出站方案的一部分，并且可以与销售订单一起计划。 

![装载图](./media/Load-drawing1-1024x477.jpg)

## <a name="inbound-transportation"></a>入站运输
当您从供应商订购物料，且物料必须交付至您的仓库，您可能想要亲自安排物料的运输。 您可以使用 Supply Chain Management 来计划运输和入站负荷的收货。 下图显示了计划入站负荷的运输的业务流程。 

![入站装载运输的业务流程](./media/Businessprocessflowforinboundloadtransportation.jpg)

## <a name="outbound-transportation"></a>出站运输
您可以计划和处理一个出站负荷来将指定物料从公司仓库装运至客户。 您可以使用 Supply Chain Management 来计划运输和出站负荷的装运。 下图显示了计划和处理装运的出站负荷的业务流程。 

![计划和处理出站装载](./media/Planningandprocessingoutboundloads.jpg)

## <a name="load-building"></a>装载计划
Supply Chain Management 提供称作“基于容量的装载计划策略”的装载计划策略。 此策略允许您在装载模板上为高度和重量指定最大值，或您可以通过输入新的值来覆盖设置。 若要使用此策略，请在**装载计划工作台**页中**设置**快速选项卡上的**装载计划策略**字段中选择。 此外，可以在应用程序对象树 (AOT) 中创建新类添加您自己的负荷创建策略。



