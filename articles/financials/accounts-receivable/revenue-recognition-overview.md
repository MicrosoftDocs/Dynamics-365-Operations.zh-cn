---
title: 收入确认概览
description: 本主题提供有关收入确认功能的信息。 此功能提供了灵活框架，供您定义特定于公司的多元素订单收入价格和收入计划确认规则。
author: kweekley
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: d52a9c7315cccf668a8b9bcf7ba5cad7039e186e
ms.sourcegitcommit: 299e20b59ebefa584ed46a13da3f1a7ff709e43c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2019
ms.locfileid: "1863555"
---
# <a name="revenue-recognition-overview"></a>收入确认概览

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!NOTE]
> 收入确认功能不能通过功能管理来启用。 目前，您必须使用 Configuration Key 启用该功能。

如果公司销售多种元素，例如产品、服务、订阅等，则必须能够分解多元素订单，以便根据一组特定于公司和行业的准则来确认收入。

一般来说，收入确认流程可用于执行以下任务：

* 分配收入，以确保根据多元素订单上的组件价值来确认合理的收入价格。
* 基于体现合同时间范围以及该段时间内收入确认百分比的收入计划来递延收入。

收入确认功能提供了灵活框架，供您定义特定于公司的收入价格和收入计划确认规则。

已发布产品用于支持销售订单文档的收入确认。 已发布产品包含确定收入价格和收入计划所需的设置。 销售订单可能源自时间和材料项目。

公司可在不使用收入价格功能的情况下使用收入计划功能。 因此，销售订单行上的价格将作为收入或延期收入。 如果销售订单行上存在收入计划，则销售订单行上的价格将递延。 如果销售订单行上存在收入计划，则销售订单行上的价格将在开票时过帐至收入帐户。

收入价格在确认销售订单或过帐发票后进行计算。 如需在发票过帐之前预览收入价格，则必须确认销售订单。

在确认销售订单后，如果任何销售订单行包含收入计划，则还将创建预期收入计划。 在为销售订单开票后，预期收入计划将被删除并被实际收入确认计划替代。

每个销售订单行均维护收入确认计划详细信息。 因此，在完成合同义务后，收入确认经理可以查看详细信息并将销售订单行发放到收入。 每个阶段结束时，收入确认经理可以创建收入日记帐来发放任何在其指定的日期当日或之前截止的计划行。 此收入日记帐不会立即过帐。 因此，收入确认经理可验证从延期收入向实际收入发放的金额是否正确。

如果合同发生变化，现有销售订单或新销售订单中添加了新的销售订单行，则可以运行重新分配流程以更正所有销售订单行中的收入价格。
