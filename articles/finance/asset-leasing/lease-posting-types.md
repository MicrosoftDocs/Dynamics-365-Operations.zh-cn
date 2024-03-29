---
title: 租赁过帐类型
description: 本文描述用于资产租赁交易的过帐类型。
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 26917ed0017e43c2be5ee53e472ad57d12db0978
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889053"
---
# <a name="lease-posting-types"></a>租赁过帐类型

[!include [banner](../includes/banner.md)]

本文描述用于资产租赁交易的过帐类型。

## <a name="lease-asset"></a>租赁资产

该科目与使用权 (ROU) 资产相关联。 当根据新的租赁会计标准、会计准则编纂专题 842 (ASC 842) 和国际财务报告准则 16 (IFRS 16) 最初确认租赁时，将从此科目借记。 对于修改后的租赁，根据修改是增加还是减少租赁负债，可以将该科目记入借方或贷方。

**示例日记帐条目：** 初始确认<br>
**借记：** 租赁资产 XXX<br>
**贷记：** 租赁负债 XXX

## <a name="lease-liability"></a>租赁负债

该科目与根据新的 IFRS 16 和 ASC 842 标准对付款进行折现时发生的租赁负债相关。 根据新准则最初确认租赁时，该科目会记入贷方。 它从租赁付款中扣除，并在应计利息中入帐。

**示例日记帐条目：** 初始确认<br>
**借记：** 租赁资产 XXX<br>
**贷记：** 租赁负债 XXX

**示例日记帐条目：** 应计利息<br>
**借记：** 利息费用 XXX<br>
**贷记：** 租赁负债 XXX

**示例日记帐条目：** 租赁付款<br>
**贷记：** 租赁负债 XXX<br>
**贷记：** 卖方应付/租赁付款 XXX

## <a name="short-term-lease-liability"></a>短期租赁负债

过帐短期租赁负债重新分类日记帐条目时，该科目与短期租赁负债相关联。 该科目在每月的最后一天从摊销计划贷记短期负债。 但是，下个月的第一天将借记同一金额。

**示例日记帐条目：** 短期租赁负债重新分类<br>
**贷记：** 租赁负债 XXX<br>
**贷记：** 短期租赁负债 XXX<br>
**借记：** 短期租赁负债 XXX<br>
**贷记：** 租赁负债 XXX

## <a name="depreciation-expense"></a>折旧支出

该科目与与 IFRS 16、ASC 842 和 IAS 17 与 ASC 840 下的财务租赁下折旧 使用权资产有关的费用关联。 每月对使用权资产进行折旧时会借记此科目。

**示例日记帐条目：** 应计折旧<br>
**贷记：** 折旧费用 XXX<br>
**贷记：** 累计折旧 XXX

## <a name="gainloss-on-lease-modification"></a>租赁修改的损益

该科目与因租赁修改而产生的任何损益关联。 如果修改使租赁负债减少的金额超出使用权资产的帐面价值，则在租赁修改期间可能会产生收益。

例如，一个租赁的租赁负债当前帐面价值为 150,000 美元，而使用权资产的帐面价值为 100,000 美元。 修改租赁，并且此修改将产生 40,000 美元的未来最低租赁付款 (PVFMLP) 新现值。 因此，将在租赁负债中借记 110,000 美元 ($150,000 – $40,000)。 由于使用权资产仅为 100,000 美元，因此减少 110,000 美元将导致资产减少到低于 0（零）。 因此，会计指南说明应将余额记入收益科目。 在这种情况下，最终日记帐条目将为 110,000 美元的租赁负债的借方，100,000 美元的租赁资产的贷方，以及 10,000 美元的收益科目的贷方。

**示例日记帐条目：** 租赁修改<br>
**贷记：** 租赁负债 XXX<br>
**贷记：** 租赁资产 XXX<br>
**贷记：** 收益 XXX

## <a name="accumulated-depreciation"></a>累计折旧

该科目与使用权资产的对冲资产科目相关联。 在过帐折扣费用时贷记此科目。

**示例日记帐条目：** 应计折旧<br>
**贷记：** 折旧费用 XXX<br>
**贷记：** 累计折旧 XXX

## <a name="variable-payment"></a>可变付款

该科目与根据 ASC 842，ASC 840 和 IAS 17 租赁的指数重估产生的可变租赁付款关联。 在租赁付款计划中，可变付款包含在 **可变付款** 列中。 当针对包含可变付款的付款计划行创建发票时，将借记此科目。

**示例日记帐条目：** 租赁付款<br>
**贷记：** 租赁负债 XXX<br>
**借记：** 可变付款 XXX<br>
**贷记：** 卖方应付/租赁付款 XXX

## <a name="deferred-rent-asset-liability"></a>延期租金资产(负债)

该科目与由延期租金处理租赁产生的延期租金资产或负债相关联。 如果发票付款金额大于该期间的直线租金费用，则在针对延期租金处理租赁过帐发票时借记该科目。 如果租赁付款额少于期间的直线租金费用，则贷记。

**示例日记帐条目：** 租赁付款（延期租金处理租赁）<br>
**借记：** 租赁费用 XXX<br>
**贷记：** 延期租金负债 XXX<br>
**贷记：** 卖方应付/租赁付款 XXX

## <a name="lease-expense"></a>租赁支出

如果将租赁分类为延期租金租金处理租赁，则科目与租赁费用关联。 当针对延期租金处理租赁过帐发票时，将借记此科目。

**示例日记帐条目：** 租赁付款（延期租金处理租赁）<br>
**借记：** 租赁费用 XXX<br>
**贷记：** 延期租金负债 XXX<br>
**贷记：** 卖方应付/租赁付款 XXX

## <a name="impairment-expense"></a>减损支出

在减损租赁时，将过帐科目。 将借记此科目，而使用权资产科目则直接贷记。

**示例日记帐条目：** 租赁付款<br>
**借记：** 减损费用 XXX<br>
**贷记：** 使用权资产 XXX

## <a name="lease-payment"></a>租赁付款

如果 **向供应商付款** 参数已关闭，则过帐科目。 如果关闭该参数，则贷记该科目，而不是贷记供应商应付款。

**示例日记帐条目：** 租赁付款<br>
**贷记：** 租赁负债 XXX<br>
**贷记：** 租赁付款 XXX

## <a name="expense-type-postings"></a>费用类型过帐

为每种费用类型生成付款时，将借记为费用类型选择的科目。 例如，只要从执行成本计划为保险费用创建发票或付款日记帐条目，都将借记为 **保险** 费用类型指定的科目。

**示例日记帐条目：** 保险付款<br>
**借方：** 保险费用类型科目 XXX<br>
**贷方：** 对方科目 XXX

> [!NOTE]
> 将在执行成本付款计划的行中租赁级别选择对方科目。 此对方科目可以与供应商或分类帐科目关联。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
