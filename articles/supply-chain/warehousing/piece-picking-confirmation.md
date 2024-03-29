---
title: 单件领料确认
description: 单件领料允许您通过移动设备上的领料或盘点工作确认单件库存。
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFAutoConfirm, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a925685b80c635cf036f19748e16d415953ed5fdda7b81498baeade35ccbfcab
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765994"
---
# <a name="piece-picking-confirmation"></a>单件领料确认

[!include [banner](../includes/banner.md)]

单件领料允许您通过移动设备上的领料或盘点工作确认单件库存。 对于领料，您可以确认在对要领料的工作指定的数量范围内的待处理工作的数量。 对于盘点工作，您可以扫描您正在盘点的库存和跟踪总金额。

启用单件领料后，将自动选择产品确认。 对于工作类型的领料，您可以设置最大件数。 这允许您将最大数量设置为在工作流程中必须确认的件数。 最大数量基于当前正在处理的工作单位。 盘点工作类型不允许最大数量。

您还可以使用与一个扫描的条码关联的数量和度量单位 (UOM)。 这适用于接收进货流，包括混合牌照接收、采购订单物料、转移单和加载物料。 它还适用于通过扫描条码可将数量添加到在条码上的 UOM 和工作单位之间转换的已确认总件数的单件领料。 当在盘点条码上的 UOM 时，如果确认对序列组上的盘点允许该数量，则该数量将添加到总盘点。

## <a name="where-it-applies"></a>适用情况

单件领料可用于所有盘点工作和任何工作类型的初始领料。 单件领料不适用于物料受序列号控制或从牌照 (LP) 库位领取生产或看板且将物料设置为暂存的情况。

## <a name="set-up-piece-picking"></a>设置单件领料

1.  在移动设备菜单项上，打开工作确认的设置窗体：仓库管理 > **仓库管理** > **设置** > **移动设备** > **移动设备菜单项**。 
2. 从移动设备菜单项打开工作确认设置。

当工作类型为领料或盘点时，以下选项可供选择。


|           选项           |                                                                            说明                                                                            |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 单件领料确认 | 可用于领料和盘点工作类型。 自动选择产品确认。 允许您从移动设备确认每件库存。 |
|  最大件数  |                   如果启用单件领料确认，可用于领料工作。 设置您必须确认的件数限制。                   |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]