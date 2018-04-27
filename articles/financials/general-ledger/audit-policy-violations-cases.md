---
title: "审计策略违规记录和案例"
description: "本文说明如何从审计政策规则违规生成审计案例。 它还包括有关审计策略使用文档选择日期范围的各个方式的信息。"
author: ryansandness
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13091
ms.assetid: e0e66c6d-c396-4a9d-b3b6-3641d130fdc0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 2376a1d6e86eba9f5021cc08dcfaea52f131a3d7
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="audit-policy-violations-and-cases"></a>审计策略违规记录和案例

[!INCLUDE [banner](../includes/banner.md)]

本文说明如何从审计政策规则违规生成审计案例。 它还包括有关审计策略使用文档选择日期范围的各个方式的信息。

<a name="how-audit-cases-are-generated"></a>审核案例如何生成
-----------------------------

审核策略用于标识不符合定义和配置为审核策略规则的业务规则的支出报表、采购订单和供应商发票。 

审核策略以批处理模式运行。 在您运行审核策略时，为该策略的一部分的任何策略规则同时运行。

每个政策规则评估一组文档。 政策规则选择符合文档选择日期范围且符合指定条件的那些文档。 例如，一项策略规则可能选择有超过50.00的餐费的支出报表。 其他政策规则可能选择特定供应商可支付的供应商发票。 系统会针对在一组文档中选择的各个文档生成违规记录。 该违规记录是特定文档不符合政策规则的记录，如发票 12345。 

分组多个跟踪违反记录以及与审核案例相关。 默认情况下，由审核策略规则分组每个审核策略的案例。 如果您需要，可以使用**案例分组条件**页选择其他分组条件。 例如，可以按项目 ID 分组这些费用标题和按供应商帐户分组供应商发票。 在此情况下，具有相同的项目 ID 的所有支出标题违反在同一案例分组，以及具有相同供应商帐户的所有供应商发票在同一案例分组。 

> [!NOTE]
> 对于基于**重复**查询类型的审核政策规则，违规记录不由政策规则或在**案例分组条件**页指定的条件分组。 相反，由建立到审核策略规则的条件对它们进行分组。 例如，如果策略规则评估相同金额、商人 ID 和日期的副本支出的支出报表，在这些字段中具有相同值的所有费用是一个情况。 具有不同值的所有支出将作为单独案例。

在审计案例生成后，使用案例管理的典型流程处理。

## <a name="document-selection-date-ranges"></a>文档选择日期范围
在运行审计策略时，每个策略规则选择具有在文档选择日期范围的一个日期的指定类型的文档。 在**附加选项**页指定文档选择日期范围。 许多文档具有多个与它们相关的日期。 审核政策规则使用的日期字段在**政策规则类型**页上指定。

这是一些审计策略使用文档选择日期范围的其他方式：

-   策略使用在文档选择日期范围的最后一天有效的每个策略规则的版本。 可以在**审计策略**列表页查看每个政策规则的生效日期。
-   策略使用与在单据选择日期范围的最后一天的策略相关的组织节点。 当前与策略相关的组织节点仅在**审计策略**列表页中显示。
-   对于基于**列表搜索**查询类型的策略规则，策略会评估在文档选择日期范围的最后一天有效的已监视实体的文件。


有关类别策略规则的详细信息，请参阅[审计策略规则](audit-policy-rules.md) 。




