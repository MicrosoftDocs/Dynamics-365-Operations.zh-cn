---
title: 自动创建服务订单
description: 您可以为某个服务协议或若干服务协议创建服务订单。
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9bcb9611fd5e59cbfafbc8419a421ad0905e8b9f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001441"
---
# <a name="create-service-orders-automatically"></a>自动创建服务订单    

[!include [banner](../includes/banner.md)]


您可以为某个服务协议或若干服务协议创建服务订单。 在创建服务订单时，可以在 **服务订单** 窗体中查看您的服务订单。

只能为有效期间的服务协议创建服务订单。 如果您在 **创建服务订单** 窗体中指定的间隔在服务协议的开始日期间或在服务协议的结束日期后，则只能为属于该服务协议日期内的时间间隔部分创建服务订单。

当您手动或自动从服务协议行创建服务订单时，该服务订单必须在该行的开始和结束日期定义的时间间隔内，除非您不指定该行的结束日期。

## <a name="create-service-orders-automatically-for-a-service-agreement"></a>为服务协议自动创建服务订单

1.  单击 **服务管理** \> **常用** \> **服务协议** \> **服务协议**。

2.  选择某一服务协议。

3.  单击 **交货** 选项卡，然后单击 **计划服务订单**。

4.  在 **开始日期** 字段和 **结束日期** 字段中指定日期，以便定义服务期间。

5.  选中 **显示消息日志** 复选框，以便显示创建的服务订单列表。

6.  在 **包括交易记录类型** 字段组中选择交易记录类型。 交易记录类型表示在服务协议中创建的行，并且根据在服务协议行上指定的服务间隔，您选择的每个交易记录类型都将生成若干服务订单。

7.  若要创建在一系列连续服务订单内缺少的所有服务订单，请选中 **连续** 复选框。

8.  单击 **确定**。

## <a name="create-service-orders-automatically-for-several-service-agreements"></a>为若干服务协议自动创建服务订单

1.  单击 **服务管理** \> **定期** \> **服务订单** \> **创建服务订单**。

2.  单击 **选择** 以做出选择，添加或移除要用于创建服务订单的条件。

3.  单击 **确定**。

## <a name="see-also"></a>请参阅

[服务订单](service-orders.md)

[自动创建服务订单](auto-create-service-orders.md)

  


