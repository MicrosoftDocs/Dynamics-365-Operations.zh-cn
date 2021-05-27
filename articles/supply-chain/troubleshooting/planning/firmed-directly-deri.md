---
title: 直接派生的确认订单被正在审核工作流处理
description: 直接派生的确认订单被状态为“正在审核”的工作流处理。
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: d54985707d82df2b947a7cb615fc25f90aa31702
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026311"
---
# <a name="directly-derived-firmed-orders-are-processed-by-an-in-review-workflow"></a>直接派生的确认订单被正在审核工作流处理

知识库编号：4612450

## <a name="symptoms"></a>故障特征

直接派生的确认订单被状态为 *正在审核* 的工作流处理。

## <a name="resolution"></a>解决方法

启用更改跟踪后，状态为 *正在审核* 将被分配给确认的派生订单（分包合同采购订单）。 因此，如果派生了采购订单（分包合同采购订单），会仅将该采购订单提交给工作流。 如果采购订单是确认的计划采购订单，将会自动获得批准，以确保计划引擎不会在采购订单仍处于 *草稿* 状态时创建新的计划订单。
