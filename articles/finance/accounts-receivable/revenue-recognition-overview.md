---
title: 收入确认概览（包含视频）
description: 本文提供有关收入确认功能的信息。 此功能提供了灵活框架，供您定义特定于公司的多元素订单收入价格和收入计划确认规则。
author: bking
ms.date: 03/15/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: bking
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 5bf07356b5613f438034f8dabac7db197e69a6c8
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2022
ms.locfileid: "9644022"
---
# <a name="revenue-recognition-overview"></a>收入确认概览

[!include [banner](../includes/banner.md)]

>[!NOTE]
>此功能将于 2023 年 10 月弃用，新用户应使用订阅计费。

如果公司销售多种元素，例如产品、服务、订阅等，则必须能够分解多元素订单，以便根据一组特定于公司和行业的准则来确认收入。

不支持在 Commerce 渠道（电子商务、POS、呼叫中心）中使用收入确认，包括捆绑功能。 配置了收入确认的项目不应添加到在 Commerce 渠道中创建的订单或交易记录中。

一般来说，收入确认流程可用于执行以下任务：

* 分配收入，以确保根据多元素订单上的组件价值来确认合理的收入价格。
* 基于体现合同时间范围以及该段时间内收入确认百分比的收入计划来延期收入。

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE44iER]

[如何在 Dynamics 365 Finance 中使用收入确认](https://youtu.be/v3amIsiqvoo)视频（如上所示）包括在 YouTube 上可用的[财务和运营播放列表](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW)中。

收入确认功能提供了灵活框架，供您定义特定于公司的收入价格和收入计划确认规则。

已发布产品用于支持销售订单文档的收入确认。 已发布产品包含确定收入价格和收入计划所需的设置。 销售订单可能源自时间和材料项目。

公司可在不使用收入价格功能的情况下使用收入计划功能。 因此，销售订单行上的价格将作为收入或延期收入。 如果销售订单行上存在收入计划，则销售订单行上的价格将递延。 如果销售订单行上存在收入计划，则销售订单行上的价格将在开票时过帐至收入帐户。

收入价格在确认销售订单或过帐发票后进行计算。 如需在发票过帐之前预览收入价格，则必须确认销售订单。

在确认销售订单后，如果任何销售订单行具有收入计划，则还将创建预期收入计划。 在为销售订单开票后，预期收入计划将被删除并被实际收入确认计划替代。

每个销售订单行均维护收入确认计划详细信息。 因此，在完成合同义务后，收入确认经理可以查看详细信息并将销售订单行发放到收入。 每个期间结束时，收入确认经理可以创建收入日记帐来发放任何在其指定的日期当日或之前截止的计划行。 此收入日记帐不会立即过帐。 因此，收入确认经理可验证从延期收入向实际收入发放的金额是否正确。

如果合同发生变化，现有销售订单或新销售订单中添加了新的销售订单行，则可以运行重新分配流程以更正销售订单的所有行中的收入价格。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

