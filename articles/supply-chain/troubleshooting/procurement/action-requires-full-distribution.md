---
title: 只能完成完全分配行号的采购订单操作
description: 只有在完全分配了行号后才能对采购完成操作
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
ms.openlocfilehash: 1ef2a938a2a17bc2dbf38d09918eabdbccca8a28
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475726"
---
# <a name="you-can-only-complete-a-purchase-order-action-for-fully-distributed-line-numbers"></a>只能完成完全分配行号的采购订单操作

## <a name="symptom"></a>问题

只有在完全分配了行号后才能对采购完成操作。

## <a name="cause"></a>原因

发生此问题可能是由于采购订单分配不一致。

## <a name="resolution"></a>解决方法

要解决此问题并将采购订单重置为 *草稿* 状态，请转到 **采购 \> 定期任务 \> 清除 \> 采购订单分配重置**。 有关详细信息，请参阅以下博客文章：[解决 Dynamics 365 Supply Chain Management 中的采购订单分配错误](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/)。
