---
title: 运行内置主计划引擎时收到错误
description: 当您运行已弃用的内置主计划引擎时，将收到一条错误消息。
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: Dialog_ReqCalcScheduleItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c950292a4f43319d21a7deafdfb341b7bef15d8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294021"
---
# <a name="you-receive-an-error-when-running-the-built-in-master-planning-engine"></a>运行内置主计划引擎时收到错误

错误代码：ReqCalcScheduleItemTablePlanningOptimizationFitError

## <a name="symptoms"></a>故障特征

当您使用已弃用的内置主计划引擎运行主计划时，将收到以下错误消息：

> 您收到此错误消息是因为内置主计划引擎用于计划优化所支持的方案。 您现在应该迁移到计划优化，因为当前的内置主计划已弃用。 请注意，此主计划运行已成功完成。 如果您的迁移非常依赖待定功能，可以请求继续使用内置主计划引擎的例外。 请完成以下调查表以开始使用（如果与从迁移到计划优化请求例外相关）。 [计划优化迁移和例外调查表](https://go.microsoft.com/fwlink/?linkid=2144962)

## <a name="cause"></a>原因

如果您运行计划并且不使用生产控制功能，应该考虑迁移到计划优化。 内置主计划引擎将弃用。 因此，如果您想继续使用它而不会收到错误消息，则必须向 Microsoft 申请例外。

## <a name="resolution"></a>解决方法

有关如何迁移到计划优化，或如何申请例外以便可以继续改为使用弃用的内置计划引擎的详细信息，请参阅[主计划的迁移到计划优化](/dynamics365/supply-chain/master-planning/new-master-planning-engine)。
