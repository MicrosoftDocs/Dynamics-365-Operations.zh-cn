---
title: "公司会计设置"
description: "本主题说明如何设置公司会计核算，以便您可以在分类帐分配使用内部公司财务日志和日志，如每天供应商日志、发票日志和付款日志。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerInterCompany
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15761
ms.assetid: 1362297b-7a51-4930-b822-2b204a2e3c37
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 5fd279327013f26230146be38e23e9955c6f12c7
ms.lasthandoff: 03/31/2017


---

# <a name="intercompany-accounting-setup"></a>公司会计设置

本主题说明如何设置公司会计核算，以便您可以在分类帐分配使用内部公司财务日志和日志，如每天供应商日志、发票日志和付款日志。

内部公司在日志各种情况下创建，例如用于日常日志、供应商发票日志、分类帐分配和集中付款。 若要启用这些方案，必须设置内部公司会计。

## <a name="define-main-accounts"></a>定义主科目
首先，您必须创建内部公司主科目以用于“应付金额”和“应收金额”会计条目。 最好为每个公司使用唯一主科目，以便简化内部公司会计条目的对帐和清除。 如果您使用一贸易伙伴或副本维度内部公司标识当事方，才能定义此维度为在内部公司会计核算过程中定义的主科目的固定的维度。 在您设置主科目，您应该设置**类型字段主科目** ** ** **资产负债表主科目**的页面。

## <a name="define-journal-names"></a>定义日志名称
其次，必须定义日记帐名称。 **设置日志类型**字段**每日** **日志名称**的页面。 最好为进行内部公司会计使用特定的日记帐名称。

## <a name="define-intercompany-accounting-setup"></a>定义公司会计设置
**公司会计核算**页可以创建能相互处理对的法人。 公司会计设置共享，以便设置是可见的。所有法人的内部。 在创建新的法人对时，请确保您知道法人定义源公司与目标公司。 在输入内部公司交易记录时，该交易记录确定的法人是开始或原始交易记录。 例如，这个公司间往来帐户。USMF (来源) 和 USSI (目标) 中设置。 如果用户是有效的。USSI 并输入与 USMF 的内部公司交易记录，则表示交易记录尚未将过帐，因为公司会计核算为的 USMF 只能定义发起方。 如果任一个公司可以源交易记录，需要创建的内部设置一个对第二个法人。 

**选择借方帐户 (应收) ** **和贷方科目 (到期) **法人的源仓库和目标。 **定义的日志名称**时，将使用交易记录在目标公司中创建。 源公司的日志已已知，因为它由用户选择，在创建内部公司交易记录。 

最后，请选择将接收的法人支持的金额计算，如现金折扣或已有损益集中的付款。 

一相互关系上**公司会计核算**页面可以轻松地创建设置。使用**相互关系**按钮，在第一个法人对创建后。 在对内部创建时，目标公司的信息复制到源公司反之亦然。 为目标公司定义的日志中维护。 大多数组织为自己的日志名称使用相同的命名约定，因此，日志名称相同。 如果日志名称不同，警告将出现在字段通知日志不存在，您和不同的日志可以选择。


