---
title: 评估针对多 SKU 库位指令的所有操作
description: 已增加了一项新功能，用于评估针对多条 SKU 库位指令的所有操作。 此页面引导您了解如何开启此功能。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 45995ed6f051cdf6be2b2985ff0e2cb1decf4cf0
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475671"
---
# <a name="multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a>多 SKU 选项无法评估多个库位指令操作

## <a name="symptoms"></a>故障特征

选择了 **多 SKU** 选项时，*销售订单* 工作订单类型和 *放置* 工作类型的位置指令不会评估多个位置指令操作。 只会评估第一个位置指令操作。

## <a name="resolution"></a>解决方法

一项新功能 *评估多 SKU 位置指令的所有操作* 已在版本 10.0.15 中添加（请参阅 [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)）。 此功能可评估多 SKU 位置指令的所有操作。 如果您需要此功能，请使用[功能管理](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)将它打开。
