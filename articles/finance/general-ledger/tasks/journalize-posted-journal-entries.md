---
title: 将过帐日记帐条目记入日记帐
description: 该过程显示如何将过帐的日记帐条目记入日记帐。
author: aprilolson
ms.date: 03/09/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8d8fca167563b14c825ebe29874c6488ddfb4d9a
ms.sourcegitcommit: 06acdfbccd7bd213a2397ea7b85d104f01914437
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/10/2022
ms.locfileid: "8400867"
---
# <a name="journalize-posted-journal-entries"></a>将过帐日记帐条目记入日记帐

[!include [banner](../../includes/banner.md)]

总帐中的记入日记帐流程提供了对总帐的已过帐凭证条目进行分组和报告的方法。 根据您提供的条件，该处理过程将生成一个凭证列表，这些凭证使用唯一编号序列并且以总帐 **日记帐编号** 值为参考。

按照这些步骤将过帐的日记帐条目记入日记帐。 此程序使用 **USMF** 演示数据公司。

1. 转到 **总帐** \> **分类帐设置** \> **总帐参数**。
2. 在 **扩展的分类帐日记帐** 字段中，选择一个值。 如果选择 **是**，报表输出将不同。
3. 选择如果尚未运行日记帐分录流程时是否可关闭期间。 如果选择 **是**，则完成期间的日记帐分录流程之前，不能关闭该期间。
4. 关闭该页面。
5. 转到 **总帐** \> **定期任务** \> **日记帐化**，然后选择 **筛选器**。
6. 选择要定义的筛选条件的行。
7. 在 **条件** 字段中，输入或选择筛选条件。
8. 选择 **确定** 关闭页面。
9. 选择 **确定** 开始日记帐化过程。 此流程完成之后将生成一个报告。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
