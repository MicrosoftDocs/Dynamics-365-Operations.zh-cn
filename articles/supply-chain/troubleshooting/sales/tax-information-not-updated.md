---
title: 更改销售订单位置时不更新税务信息
description: 如果在销售订单标题更改了站点、仓库或交货地址，不更新行中的案例税务信息。 必须手动执行此操作。
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 77a73a787ff8a174c575f3b4f75694ded45d5712
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475692"
---
# <a name="tax-information-isnt-updated-if-location-on-a-sales-order-header-is-changed"></a>更改销售订单标题上的位置时不更新税务信息

## <a name="symptoms"></a>故障特征

如果在销售订单标题更改了站点、仓库或交货地址，不更新行中的案例税务信息。

## <a name="resolution"></a>解决方法

此为有意行为。 发生此问题是因为交货地址、站点和仓库未在行级别自动更改。 您必须手动更新它们。
