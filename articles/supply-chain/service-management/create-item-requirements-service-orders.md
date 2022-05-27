---
title: 为服务订单创建物料需求
description: 此主题描述如何为服务订单创建物料需求。
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4a92843a82093826822ab9865e43fee07d65e94c
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677805"
---
# <a name="create-item-requirements-for-service-orders"></a>为服务订单创建物料需求

[!include [banner](../includes/banner.md)]

您可以创建服务订单跟踪和管理为您的客户提供的服务。 如果您需要对服务订单预留特定物料，可以创建它的库存物料需求。 物料需求可以从库存立即消耗，或可以启动生产订单的物料。

通过使用物料需求来代替物料交易记录，您可以计划刚好在实际使用物料之前交货，创建采购订单，在贸易协议框架中包括物料，以及在生产计划中包括物料需求。

服务订单创建物料需求通过项目进行处理。 若要创建服务单物料需求，必须将服务订单附加到项目中去。 您为服务订单创建物料需求后，可以在 **项目** 窗体中查看所选项目的物料需求。

## <a name="create-an-item-requirement-for-a-service-order"></a>为服务订单创建物料需求

1. 转到 **服务管理** \> **通用** \> **服务订单** \> **服务订单**。
1. 选择需要创建物料需求的服务订单。
1. 在 **操作窗格** 中的 **发货** 选项卡上选择 **物料需求**。
1. 在 **物料需求** 窗体中输入所需物料的信息。 有关特定字段的更多信息，请参阅[物料需求（窗体）](https://technet.microsoft.com/library/aa552021\(v=ax.60\))。

## <a name="create-an-item-requirement-for-a-service-agreement"></a>为服务协议创建物料需求

1. 转到 **服务管理** \> **通用** \> **服务协议** \> **服务协议**。
1. 打开需要创建物料需求的服务协议。
1. 在 **行** 快速选项卡上，选择 **添加** 创建新行。
1. 在 **交易记录类型** 字段中选择 **物料**。
1. 在 **物料设置** 字段中，选择 **物料需求**。
1. 在 **物料编号** 字段中，选择该服务协议所需的物料。
1. 在 **行明细** 快速选项卡上 **产品维度** 选项卡中的 **站点** 字段内，为物料选择库存站点。
1. 若要从协议行中创建服务订单，请在 **行** 快速选项卡中选择 **创建服务订单**，然后将相关信息输入到 **创建服务订单** 窗体中。

## <a name="see-also"></a>请参阅

[自动创建服务订单](create-service-orders-automatically.md)。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
