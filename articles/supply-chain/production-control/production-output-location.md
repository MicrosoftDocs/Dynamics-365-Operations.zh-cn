---
title: 生产输出位置
description: 本主题描述用于标识生产输出位置的层次结构。
author: johanhoffmann
manager: tfehr
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 8fa4f7d844c178ee603778fa2f1def6bfc33db97
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209435"
---
# <a name="production-output-location"></a>生产输出位置

[!include [banner](../includes/banner.md)]

本主题描述用于标识生产输出位置的层次结构。

生产输出位置是成品在生产后最先存储的位置。 通常，此位置靠近生产成品的生产流程。 生产输出位置作为物料在移动到装运区域、存储位置、用于下游生产流程的生产输入位置等之前的中间存储。 

在生产订单或批次订单上报告成品时设置默认生产输出位置。 以下层次结构用于标识此输出位置：

1. 使用在生产订单或批次订单标题上定义的输出位置。
2. 如果在那里找不到任何位置，则使用在生产工艺路线中定义的最后一个操作使用的资源上定义的输出位置。
3. 如果在那里找不到任何位置，则使用资源为生产工艺路线中定义的最后一个操作使用的资源组上定义的输出位置。
4. 如果在那里找不到任何位置，则使用在为生产订单定义的仓库上定义的输出位置。

仅对使用高级仓库流程进行设置的产品设置默认生产输出位置。 在此类物料报告为已完工入库时，创建 **成品储存** 或 **联产品和副产品储存** 类型的仓库工作。 此类型工作使用生产输出位置作为领料库位。 储存库位由库位指令确定。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]