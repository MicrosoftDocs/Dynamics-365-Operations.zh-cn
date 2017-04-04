---
title: "单位的余额会计核算日志"
description: "本文显示当在分类帐页中选择平衡财务维度时日记帐如何自动平衡。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 8b6fda79222905b0df211a0b944aca9e4dc76850
ms.lasthandoff: 03/31/2017


---

# <a name="balanced-journals-for-interunit-accounting"></a>单位的余额会计核算日志

本文显示当在分类帐页中选择平衡财务维度时日记帐如何自动平衡。 

如果在财务维度值的级别处的科目分录不平衡，则附加的科目分录将自动创建以平衡日记帐。 这些科目分录使用**自动交易记录帐户**页上的**单位间 - 借方**和**单位间 - 贷方**过帐类型来确定主科目。 例如，分支，是会计科目的二级细分，被选择作为平衡财务维度，以下会计分录即将创建。

|                      |           |
|----------------------|-----------|
| 6100 – MSP – OU\_ | 100.00 " DR " |
| 6100 – NY – OU\_  | 100.00 " DR " |
| 2100 – MSP – OU\_ | 并 200.00 |

在这种情况下，以下余额确定：

-   对于分支 MSP = 100.00 CR
-   对于分支 NY = 100.00 DR

因此，以下会计分录将自动创建，以在财务维度值级别平衡日记帐。

|                                   |           |
|-----------------------------------|-----------|
| (Interunit 借方) – MSP – OU\_ | 100.00 " DR " |
| (Interunit 贷方) – NY – OU\_ | 并 100.00 |




