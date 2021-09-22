---
title: 如果允许空发货和空收货，则不能移动牌照
description: 如果序列号允许空发货和空收货，则不能移动牌照。 将通过把序列号字段设置为可选来解决此问题。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0047f79aa417c8fc910447505f07963d014f54e7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475680"
---
# <a name="cant-move-license-plate-if-serial-number-has-blank-issue-and-blank-receipt-allowed"></a>如果序列号允许空发货和空收货，则不能移动牌照

## <a name="symptoms"></a>故障特征

如果序列号在跟踪维度组上有 *允许空发货* 和 *允许空收货* 设置，并且同一个位置有多个牌照，其中一些有序列号，另一些则没有，这种情况下您无法使用 **移动** 菜单项移动牌照。

## <a name="resolution"></a>解决方法

此问题将通过 [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687) 中部署的更改修复。 当允许空收货和空发货时，这些更改将使 **序列号** 字段变为可选。
