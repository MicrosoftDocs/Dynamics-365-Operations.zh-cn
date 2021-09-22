---
title: 在不结转库存的情况下更改分类帐期间状态时显示警告或错误
description: 在不结转库存的情况下更改分类帐期间状态时显示警告或错误
author: AndersGirke
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 05851753e29da75f014d2cc77e2b8df259620eee
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475674"
---
# <a name="warnings-or-errors-on-changing-ledger-period-status-without-closing-inventory"></a>在不结转库存的情况下更改分类帐期间状态时显示警告或错误

Microsoft 引入了以下验证，以防止由于围绕成本计算的不正确期间结束流程而导致的问题。 如果遇到以下任何错误消息，请参阅 [KB 4561987](https://fix.lcs.dynamics.com/Issue/Details?kb=4561987&bugId=445351&dbType=3&qc=f514f2adcddcddceec43af58c26ae8a9020effdc7cdfe085d9d0deeb8cc7b6a3) 了解如何解决这些问题的详细信息。

- 您将要执行日期为 %1 (10-02-2019) 的重新计算。 上次登记的重新计算已在日期为 %2 (20-01-2019) 的上一个期间内执行。 其日期 %3 (31-01-2019) 与期间结束匹配的库存结转未执行已登记。 请记住在与期间结束匹配的 %3 (31-01-2019) 前执行库存结转。 执行之前，子分类帐或总帐中的库存、所售货物成本和差异评估可能不正确。

- 您即将将分类帐期间 %1 的状态更改为 %2。 其日期 %3 与期间结束匹配的库存结转未执行已登记。 请在更改状态之前在与期间结束匹配的 %3 前执行库存结转。 执行之前，子分类帐或总帐中的库存、所售货物成本和差异评估可能不正确。 从法人 %4 报告。 现在，它只是提供信息，但将来会要求您执行此类操作。

- 科目结构 %1 已更改。 一个或多个主科目 %2 不再存在。 这些主科目是日期为 %4 的 %3 所需要的。 请先将这些主科目添加到科目结构 %1 中，然后才能继续 %3 作业。 现在，它只是提供信息，但将来会要求您执行此类操作。

- 您将要执行日期为 %1 (31-01-2019) 的库存结转。 其日期 %2 (31-01-2019) 与期间结束匹配的倒冲成本计算法计算未执行已登记。 请记住执行其日期 %3 (31-01-2019) 与期间结束匹配的倒冲成本计算法计算。 执行之前，子分类帐或总帐中的库存、所售货物成本和差异评估可能不正确。

- 您将要执行日期为 %1 (28-02-2019) 的倒冲成本计算法计算。 上次登记的倒冲成本计算法计算已在日期为 %2 (31-01-2019) 的上一个期间内执行。 其日期 %3 (31-01-2019) 与期间结束匹配的库存结转未执行已登记。

请记住在与期间结束匹配的 %3 (31-01-2019) 前执行库存结转。 执行库存结转之前，子分类帐或总帐中的库存、所售货物成本和差异评估可能不正确。