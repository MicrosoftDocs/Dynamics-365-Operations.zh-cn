---
title: 无法将库存移动到牌照控制的库位
description: 在早期版本中，您不能减少负荷上的已领料数量。 但是，现在您可以取消牌照控制的库位的领料。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: fdb6ee2cff184c5dd53ce33133e4935d00caf3db
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475733"
---
# <a name="cant-move-inventory-to-a-location-that-is-license-plate-controlled"></a>无法将库存移动到牌照控制的库位

## <a name="symptoms"></a>故障特征

您不能减少负荷上的已领料数量。

## <a name="resolution"></a>解决方法

在早期版本中，您不能减少负荷上的已领料数量。 但是，现在您可以取消牌照控制的库位的领料。 您必须在 **减少领料数量** 页上为负荷行指定 **位置** 值和 **牌照** 值。
