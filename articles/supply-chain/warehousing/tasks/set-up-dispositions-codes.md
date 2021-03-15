---
title: 设置处置代码
description: 此过程在针对可以在移动设备上用于退货单接收流程的处置代码的设置。
author: ShylaThompson
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSDispositionTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7c98526423b28fcb6c4e00a9f2cfd84d5a9119e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977005"
---
# <a name="set-up-dispositions-codes"></a>设置处置代码

[!include [banner](../../includes/banner.md)]

此过程在针对可以在移动设备上用于退货单接收流程的处置代码的设置。 部署代码是收到物料时可以使用的规则集合。 例如，在工作用户使用设备接收损坏的物料时，用户必须扫描损坏物料的处置代码。 接收的货物的库存状态、工作模板和位置指令可以通过扫描的处置代码确定。 对于采购订单接收流程和生产订单完工入库流程，使用处置代码是可选的。 对于销售订单退货接收流程，如果使用移动设备登记物料，使用处置代码是强制的。  本指南使用演示数据公司 USMF 创建。 该过程专门面向仓库经理。 

1. 转到“仓库管理”>“设置”>“移动设备”>“处置码”。
2. 单击“新建”。
    * 创建新的处置码以供客户退货使用。  
3. 在“处置码”字段中，键入一个值。
4. 在“库存状态”字段中，选择一个显示库存锁定的库存状态。
    * 如果您正在使用 USMF，则选择“锁定”。 您可以将库存状态添加到处置码，以覆写订单行上显示的默认状态。  
5. 在“工作模板”字段中，键入一个值。
    * 选项：选择与退货单相关的一个工作模板代码。 如果没有提供任何数值，请使用系统中配置的标准规则来解决工作模板问题。 选定工作模板将会限制此处置码的使用过程。 例如，如果处置码有一个带采购订单类型的工作指令的工作模板，则其不能用于登记被客户退回的物料。  
6. 在“退货处置码”字段中，键入一个值。
    * 退货处置码可以确定已登记物料的退货单流程的剩余部分。 在本示例中，客户应收到贷方通知单。 添加包含信贷行为的退货处置码。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]