---
title: 处理分配
description: 本文提供有关分配、在 Microsoft Dynamics 365 Finance 中处理分配的选项，以及如何在预算计划中使用它们的信息。 分配用于跨多个会计科目组合分配金额。 它们帮助确保向核算的正确对象计入费用或收入。
author: kweekley
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: kfend
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0629b32d39f4d74ec37eebe92b92e0b186b5fce2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877974"
---
# <a name="process-allocations"></a>处理分配

[!include [banner](../includes/banner.md)]

本文提供有关分配、处理分配的选项，以及如何在预算计划中使用它们的信息。 分配用于跨多个会计科目组合分配金额。 它们帮助确保向核算的正确对象计入费用或收入。

以下功能支持此流程：

-   通过在会计分配中使用“分解”操作，或者通过将财务维度默认模板应用到文档，手动分配交易记录金额。 有关详细信息，请参阅[会计分配](../accounts-payable/accounting-distributions.md)。
-   将基于在单个主科目中定义的分配期限自动分配交易记录。 分配科目条目将基于百分比和目标会计科目为每个日记帐生成，只要会计条目满足定义为源会计科目的条件。 有关详细信息，请参阅[主科目分摊条件](../general-ledger/main-account-allocation-terms.md)
-   将基于分类帐分配规则自动分配分类帐余额或固定金额。 使用分配日记帐定期处理分类帐分配规则。 有关详细信息，请参阅[分配规则](../general-ledger/ledger-allocation-rules.md)。

###  <a name="allocations-in-budget-planning"></a>预算计划中的分配

分类帐分配规则可以为预算计划使用。 当您在预算计划中使用分类帐分配规则时，分配规则的作用方式与其在分类帐中相同，但是源数据和目标数据来自预算计划。 您可以手动选择分类帐分配规则供预算计划使用。 或者，您可以使用作为工作流程的一部分运行的分配计划。

> [!NOTE]
> 您不能为预算计划使用内部公司的分类帐分配规则。



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
