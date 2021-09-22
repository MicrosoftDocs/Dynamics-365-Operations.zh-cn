---
title: 取消订单时无法删除预留
description: 如果取消和冲销与销售订单关联的工作，则不能取消该订单。 为此，请执行以下三步。
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a8d947e64568246dba5eff3c21fd3920b6494b73
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475699"
---
# <a name="reservations-cannot-be-removed-when-canceling-an-order"></a>取消订单时无法删除预留

## <a name="symptoms"></a>故障特征

如果工作与销售订单关联，并且您尝试取消该订单，则会收到以下错误消息：

> 已创建了依赖预留的工作，因此无法删除这些预留。

如果取消和冲销工作，则不能取消销售订单。 即使与销售订单关联的工作已关闭，此要求也适用。

## <a name="resolution"></a>解决方法

若要解决此问题，请按照以下步骤操作：

1. 取消工作，然后将库存放回所需的位置。 转到销售订单的相关负荷，然后在负荷行上选择 **减少领料数量** 或在操作窗格上选择 **冲销工作**。

    现在，工作的状态为 *已取消*，并且已自动创建和处理新的库存变动工作，以在冲销时将库存放回到所述位置。

2. 删除负荷。 装运也会被删除。

3. 您现在应该能够转到销售订单并取消订单。
