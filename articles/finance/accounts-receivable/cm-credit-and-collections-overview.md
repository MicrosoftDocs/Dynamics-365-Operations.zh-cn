---
title: 信用和收款概览
description: 此主题概要介绍信用和收款的功能。
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: ade76b822904f49135e07dfe0a39d2227dd1dd77
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992977"
---
# <a name="credit-and-collections-overview"></a>信用和收款概览

[!include [banner](../includes/banner.md)]

您可以管理客户的信用额度，并在必要时执行收款活动。

## <a name="credit-management"></a>信用管理

客户信用管理使您可以根据创建的信用规则通过过帐流程管理信用限额和控制销售订单流程。

信用管理流程可以包括以下任何步骤：

- 更新客户的信用属性，以提供有关其信用价值的其他信息。
- 使用信用额度调整为客户创建信用额度。
- 使用信用额度调整为客户创建临时信用额度。 这样，您可以根据业务需求临时增加或减少客户信用额度。
- 添加可能影响信用额度的信息，例如有关保险和担保的信息。
- 创建将客户联系在一起的客户信用组，以便他们共享一个信用额度。
- 为客户分配风险评分，然后使用评分通过信用额度调整为这些客户自动生成信用额度。
- 根据风险、付款条件、信用额度、逾期金额和已用信用额度的百分比等因素，创建阻止规则，以在一个或多个过帐流程中暂停订单。
- 管理暂停的销售订单列表，查看暂停的原因并缓解问题。
- 下达销售订单，以便它们继续完成过帐流程。
- 设置工作流来管理对信用额度更改和销售订单下达的批准。

## <a name="collections-management"></a>收款管理

**收款** 页会提供集中式视图，可在其中管理应收帐款收集信息。 收款经理可以使用该集中式视图来管理收款。 收款代理可以从使用预定义收款条件生成的客户列表或从 **客户** 页开始收款流程。

在开始设置或使用收款前，应了解以下概念：

- 客户帐龄快照包含特定时间点的帐龄余额信息。
- 收款客户池帮助您组织您的工作。
- 收款代理可以有自己的客户池。
- 列表页组织收款客户、活动和案例。
- 客户的所有收款信息均在一个页面上，且您可以从该页面执行行动。
- 可以在一个步骤中停征、复征或冲销利息和费用。
- 可以在一个步骤中创建勾销交易记录。
- 可以在一个步骤中处理资金不足 (NSF) 付款。

有关这些概念的说明，请参见[收款管理关键概念](./cm-collections-concepts.md)。

## <a name="additional-resources"></a>其他资源

[客户信用管理参数设置](./cm-credit-mgmt-setup.md)

[客户信用管理设置信息](./cm-setup-information.md)

[为客户添加信用管理信息](./cm-add-credit-mgmt-information-customer.md)

[客户信用组](./cm-customer-credit-groups.md)

[客户信用额度调整](./cm-credit-limit-adjustments.md)

[销售订单的信用保留](./cm-sales-order-credit-holds.md)

[客户信用管理定期任务](./cm-periodic-tasks.md)
