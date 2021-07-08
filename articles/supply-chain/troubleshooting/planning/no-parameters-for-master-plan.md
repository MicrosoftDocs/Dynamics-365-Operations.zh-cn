---
title: 主计划的参数不存在
description: 当您尝试确认计划订单时，将收到一条错误消息，表明主计划不存在任何参数。
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d4b64af2e30109b8560d40c4c532504611528bbe
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294022"
---
# <a name="parameters-for-the-master-plan-dont-exist"></a>主计划的参数不存在

错误代码：SYS25368

## <a name="symptoms"></a>故障特征

当您尝试确认计划订单时，将收到以下错误消息：

> 主计划 %1 的参数不存在。

## <a name="cause"></a>原因

由于配置问题，系统找不到指定计划的设置。

## <a name="resolution"></a>解决方法

- 转到 **主计划 \> 设置 \> 计划 \> 主计划**，并确保存在具有指定名称的计划。
