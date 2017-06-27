---
title: "维护计划订单"
description: "本文提供有关如何管理计划订单的信息。 介绍如何更新计划订单的状态，确定计划订单，并筛选与所选计划订单具有相同状态的计划订单。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 94f6f28ec4b255930f84a27eb5394503ff59e4c0
ms.contentlocale: zh-cn
ms.lasthandoff: 05/25/2017


---

# <a name="maintain-planned-orders"></a>维护计划订单

[!include[banner](../includes/banner.md)]


本文提供有关如何管理计划订单的信息。 介绍如何更新计划订单的状态，确定计划订单，并筛选与所选计划订单具有相同状态的计划订单。

您可以从**“主计划”**工作区、**“计划订单”**列表或**“计划生产订单”**、**“计划采购订单”**和**“计划转移”**列表中管理计划订单。 您可以使用**“状态”**字段帮助跟踪您的进度。 使用了以下值：

-   当主计划生成计划订单时，该计划订单状态为“**未处理**”。
-   如果您决定不确认某一计划订单，则可以给予其状态“**已完成**”。
-   当您决定确认某一计划订单时，可以给予其状态“**已审核**”。 此状态表示您核准确认该计划订单，但它尚未被确认。

**注释：**已核准的计划订单将以当前状态转移到下一主计划计算中。 可以通过单击“**确认**”确认计划订单。 您可以确认以下计划订单：

-   选择的计划订单。
-   多个计划订单。
-   从“**分解**”页中由分解生成的计划订单。 单击“**计划订单**”，选择计划订单，然后单击“**确认**”。

确认计划订单时，该订单将移至相关模块的订单部分。 **注释：**可以右键单击具有特定状态的某一计划订单并筛选具有相同状态的其他计划订单。 此功能很有用，例如，您希望针对所有状态为**“已审核”**的计划订单进行筛选，然后可以确定它们。

<a name="see-also"></a>请参阅
--------

[主计划](master-plans.md)




