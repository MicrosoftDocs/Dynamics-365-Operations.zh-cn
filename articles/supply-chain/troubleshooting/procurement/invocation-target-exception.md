---
title: 过帐供应商发票时发生异常
description: 过帐供应商发票时发生“调用目标引发异常”异常。
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: ecc63cb7d0d2392105d8e4290f8e837945ae0781
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475684"
---
# <a name="an-exception-occurs-during-vendor-invoice-posting"></a>过帐供应商发票时发生异常


## <a name="symptoms"></a>故障特征

过帐供应商发票时遇到了以下异常：

> 调用目标引发异常

## <a name="cause"></a>原因

发生此问题可能是由于采购订单分配不一致。

## <a name="resolution"></a>解决方法

要解决此问题并将采购订单重置为 *草稿* 状态，请转到 **采购 \> 定期任务 \> 清除 \> 采购订单分配重置**。 有关详细信息，请参阅以下博客文章：[解决 Dynamics 365 Supply Chain Management 中的采购订单分配错误](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/)。
