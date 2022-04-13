---
title: 无法过帐已停止销售订单行的装箱单
description: 您无法过帐已停止销售订单行的装箱单
author: smithanataraj
ms.date: 03/07/2022
ms.topic: article
ms.search.form: WHSLoadTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2022-03-07
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 115cfe79e075eb36f73203818acdbb5e31fc0bad
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462844"
---
# <a name="cant-post-packing-slip-for-a-stopped-a-sales-order-line"></a>无法过帐已停止销售订单行的装箱单

错误代码：SYS13203

## <a name="symptoms"></a>故障特征

当您尝试过帐负荷的装箱单时，系统显示以下错误消息：

> 确认出站装运后停止销售订单行时无法过帐装箱单。无法领取数量。

## <a name="cause"></a>原因

可能会停止一个或多个相关的销售订单行，这意味着系统将阻止进一步处理该销售订单。 除此之外，这还意味着系统不会过帐订单的装箱单。

例如，用户可能决定停止一个或多个订单行，因为客户回电取消了他们的订单。 但是，如果出站装运已经确认，说明包含销售订单的装运已经实际离开了仓库，这意味着停止销售订单行不会产生任何影响。 因为不能再实际停止装运，您也可以取消停止行，以便可以过帐装箱单。 然后，您需要将取消的订单作为退货处理。

## <a name="resolution"></a>解决方法

要能够过帐装箱单，请通过执行以下步骤确保没有停止任何相关的销售订单行。

1. 转到 **所有销售订单 \> 销售和市场营销 \> 所有销售订单**。
1. 查找并打开您遇到问题的销售订单。
1. 在 **销售订单行** 快速选项卡上，选择一个销售订单行。
1. 在 **行明细** 快速选项卡上，打开 **常规** 选项卡，确保将 **停止** 字段设置为 *否*。
1. 继续工作，直到所有相关销售行不再停止。
1. 再次尝试过帐负荷或销售订单的装箱单。
