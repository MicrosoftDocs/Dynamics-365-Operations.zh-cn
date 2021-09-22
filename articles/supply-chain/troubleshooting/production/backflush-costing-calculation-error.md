---
title: 库存结算期间发生倒冲成本计算法计算错误
description: 在早期版本中，可能在库存结算期间收到倒冲成本计算法计算错误。 此问题已修复。
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ae92b7121998d6b1ba2f08ea5736c55637867fbf
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475673"
---
# <a name="backflush-costing-calculation-error-during-inventory-closing"></a>库存结算期间发生倒冲成本计算法计算错误

## <a name="symptoms"></a>故障特征

在版本 10.0.13 之前的版本中，如果您不使用精益生产成本计算流程，在库存结转期间会收到以下错误的警告消息：

> 您将要执行日期为 %1 的库存结转。 其日期 %1 与期间结束匹配的倒冲成本计算法计算未执行已登记。 请记住执行其日期 %1 与期间结束匹配的倒冲成本计算法计算。 执行之前，子分类帐或总帐中的库存、所售货物成本和差异评估可能不正确。

## <a name="resolution"></a>解决方法

此问题在版本 10.0.13 和更高版本中已修复。 有关详细信息，请参阅 [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296)。
