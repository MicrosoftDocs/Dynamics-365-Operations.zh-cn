---
title: 混合牌照接收并非支持所有处置代码
description: 当处置代码的操作字段设置为贷记或报废时，您只能使用混合牌照接收菜单项来处理退回物料。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b762255bc5ef6a1e15688a9c635940e92e67db3c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475713"
---
# <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-but-credit"></a>混合牌照接收不使用“贷记”以外的任何处置代码

## <a name="symptoms"></a>故障特征

当处置代码的 **操作** 字段设置为 *贷记* 或 *报废* 时，您只能使用[混合牌照接收](/dynamics365/supply-chain/warehousing/mixed-license-plate-receiving)菜单项来处理退回物料。

## <a name="resolution"></a>解决方法

Microsoft 已评估此问题，确定了这是一项功能限制。 当前，混合牌照接收仅支持将 **操作** 字段设置为 *贷记* 或 *报废* 的[处置代码](/dynamics365/supply-chain/service-management/set-up-disposition-codes)。
