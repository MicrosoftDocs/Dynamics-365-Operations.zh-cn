---
title: 平衡单位间核算的日记帐
description: 本文显示当在分类帐页中选择平衡财务维度时日记帐如何自动平衡。
author: kweekley
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: kfend
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 38a7d88602dcd0121eb331dab8bf35a815287f8c
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/05/2022
ms.locfileid: "8712305"
---
# <a name="balanced-journals-for-interunit-accounting"></a>平衡单位间核算的日记帐

[!include [banner](../includes/banner.md)]

本文显示当在分类帐页中选择平衡财务维度时日记帐如何自动平衡。 

如果在财务维度值的级别处的科目分录不平衡，则附加的科目分录将自动创建以平衡日记帐。 这些科目分录使用 **自动交易记录帐户** 页上的 **单位间 - 借方** 和 **单位间 - 贷方** 过帐类型来确定主科目。 例如，业务单位，是会计科目的二级细分，被选择作为平衡财务维度，以下会计分录即将创建。

| &nbsp;               | &nbsp;    |
|----------------------|-----------|
| 6100 – MSP – OU\_256 | 100.00 DR |
| 6100 – NY – OU\_249  | 100.00 DR |
| 2100 – MSP – OU\_256 | 200.00 CR |

在这种情况下，以下余额确定：

-   对于业务单位 MSP = 100.00 CR
-   对于业务单位 NY = 100.00 DR

因此，以下会计分录将自动创建，以在财务维度值级别平衡日记帐。

| &nbsp;                            | &nbsp;    |
|-----------------------------------|-----------|
| （单位间借方）– MSP – OU\_256 | 100.00 DR |
| （单位间贷方）– NY – OU\_249 | 100.00 CR |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
