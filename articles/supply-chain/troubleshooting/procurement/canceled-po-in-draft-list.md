---
title: 取消的采购订单将显示在工作区的草稿列表中
description: 取消的采购订单将显示在“采购订单准备”工作区的草稿列表中
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
ms.openlocfilehash: f1dc23cd7e5b4b99cb7a9440d7d4666d8396511f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475710"
---
# <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-workspace"></a>取消的采购订单将显示在工作区的草稿列表中

## <a name="symptoms"></a>故障特征

取消处于 *已确认* 状态的采购订单后，取消的采购订单仍会出现在 **采购订单准备** 工作区中的草稿采购订单列表中。

## <a name="resolution"></a>解决方法

仅需要接受更改管理的采购订单会发生此问题。 发生这种情况是因为取消被认为是必须进行审批的更改。 审批可以由系统自动完成。 因此，流程是将取消的采购订单提交到审批工作流，让它可以进入 *已批准* 状态。 此时，采购订单将不再出现在 **采购订单准备** 工作区中的草稿采购订单列表中。
