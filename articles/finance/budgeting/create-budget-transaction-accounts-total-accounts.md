---
title: 从交易记录科目和合计科目创建预算
description: 本文提供基于合计科目创建预算的流程的概览。 还说明如果需要预算控制，如何启用合计科目的预算控制。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetControlConfiguration, BudgetPlanGenerate
audience: Application User
ms.reviewer: roschlom
ms.custom: 13051
ms.assetid: fb1bb2d3-445c-402f-a9a3-aa6503eed78e
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 085bc12433616d2da2bda40a8412fb88e40db3b9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210185"
---
# <a name="create-a-budget-from-transaction-accounts-and-total-accounts"></a>从交易记录科目和合计科目创建预算

[!include [banner](../includes/banner.md)]

本文提供基于合计科目创建预算的流程的概览。 还说明如果需要预算控制，如何启用合计科目的预算控制。

预算计划和预算登记条目文档允许对具有 **合计** 主科目类型的主科目编制预算。 实际只能过帐到交易记录主科目。 

对于 **从总帐生成预算计划** 定期流程，在 **源** 选项卡上，您指定 **合计** 主科目类型作为条件。 在这种情况下，每个总计主科目将包括在目标预算计划中，并且，金额将等于所选主科目范围的总金额。 

您可以激活 **合计** 类型的主科目的预算控制。 此功能通过使用预算组受支持。 对于每个总计主科目，应为预算组控制的预算必须在 **预算控制配置** 页创建。 您指定的条件必须包括总计主科目和科目范围。 若要加快创建预算组的过程，您可以利用预算控制组数据实体。 

在报告中（例如在财务报表中）使用预算时，总计科目的预算总和由以下金额组成：

-   在合计科目间隔中的每个交易记录会计科目中创建的预算。
-   直接在合计科目上输入的预算金额。

因此，您可以为合计科目间隔中最重要的交易记录科目创建单独的预算，然后将剩余预算金额添加到合计科目。





[!INCLUDE[footer-include](../../includes/footer-banner.md)]