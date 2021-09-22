---
title: 生产订单没有显示在“标记”页上
description: 有些生产订单不会显示在标记页上。 本主题介绍三种不能进行标记的产品配置。
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 87507e91d3feb2557e7ba771b8e34ff7ca105749
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475634"
---
# <a name="production-orders-arent-shown-on-the-marking-page"></a>生产订单没有显示在“标记”页上

## <a name="symptoms"></a>故障特征

处理谨慎制造时，**标记** 页中不显示某些生产订单。

## <a name="resolution"></a>解决方法

具有以下配置的产品不能进行标记。 因此，它们不会显示在 **标记** 页上：

- 这些产品定义为 *实际称重* 类型的产品。
- 它们已启用高级仓库流程。
- 它们被配置为由 *标准成本* 原则控制。
