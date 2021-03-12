---
title: 计算化整折旧金额
description: 本文讨论在“帐簿设置”页找到的“化整折旧”字段。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 01c8662f0731abd089c9039c16bb77e39c1d3e51
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976007"
---
# <a name="round-off-amount-for-depreciation-calculations"></a>计算化整折旧金额

[!include [banner](../includes/banner.md)]

本文讨论在“帐簿设置”页找到的“化整折旧”字段。

将为每个帐簿设置化差折扣金额。 化整折旧金额用于固定资产折旧图（显示固定资产的未来折旧和价值），也用于折旧方案。 输入此帐簿允许的最低折旧金额。 

不管使用的是什么化整设置，系统都不会化整最近折旧期间的折旧金额。 在最近折旧期间结束时，如果使用残值，则固定资产的值必须为 0（零）或残值。

### <a name="example"></a>示例

没有化整的折旧计算为 2,444.44。 如下表中所示，根据设置的化整方式，建议的金额将不同。

| 化整方法 | 折旧金额 |
|-----------------|---------------------|
| 化整 0.1    | 2,444.40            |
| 化整 1.00   | 2,444.00            |
| 化整 10.00  | 2,440.00            |
| 化整 100.00 | 2,400.00            |





