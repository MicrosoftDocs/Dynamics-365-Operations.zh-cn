---
title: 创建含交货计划的采购订单
description: 此过程显示如何为采购订单创建交货计划。
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchDeliverySchedule, PurchEditLines
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a9b7b233339d41605e1b115bd14a18b706ef226
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "333821"
---
# <a name="create-a-purchase-order-with-a-delivery-schedule"></a>创建含交货计划的采购订单

[!include [task guide banner](../../includes/task-guide-banner.md)]

此过程显示如何为采购订单创建交货计划。 在请求在多个装运中交付订单或日记帐上的数量时，使用交货计划。 可以在 USMF 演示数据公司中使用本指南中的示例。 此过程通常由采购代理完成。


## <a name="create-a-delivery-schedule"></a>创建交货计划
1. 转到“采购”>“采购订单”>“所有采购订单”。
2. 单击“新建”。
3. 在“供应商帐户”字段中输入 US-101。
4. 单击“确定”。
5. 在“物料编号”字段中输入 M0001。
6. 在“数量”字段中，输入 10。
7. 单击“采购订单行”。
8. 单击“交货计划”。
    * “交货计划”页可用于指定装运数量的位置，订单行的总数量从供应商交付。  
    * 默认情况下，系统将复制总数量和原始采购行的交付详细信息到交货计划第一行。 在此示例中，我们为两个装运创建一个计划，第一个装运日期抵消第二个装运日期一周。  
9. 在“数量”字段中，将数量更改为 4。
10. 单击“新建”。
11. 在“数量”字段中，输入 6 作为剩余数量。
    * 在交付日期字段中，选择比第一个交付行的日期晚一周的日期。  
    * 您可以通过查看“总计”和“剩余”字段，跟踪查看分配到交货计划行的总数量。 在剩余数量为零时，原始行的全部数量已分配到计划中。  
12. 展开“费用转换”部分。
    * 此处的选项用于控制如何在交货计划行之间分配费用。 如果选择“复制总额”，将把原始订单行中的费用金额复制到每交付行。 “分配到交货行”选项根据各交付行中的数量划分原始行费用。  
13. 折叠“费用转换”部分。
14. 单击“确定”。
    * 交货计划现在已被应用于订单。  
    * 原始订单行（现在称为业务行）已转换为具有多个交货项的订单行。 其标有不同图标，作为交货行的标头。  
15. 选择第二个订单行，即两个交货行中的第一个。
    * 两个新行，即交货行，构成交货计划。 该订单将处理这些新行，而不是原始行。 如果打印单据（如确认、产品收货日记帐或发票），则只显示交货行。  

## <a name="change-the-delivery-schedule"></a>更改交货计划
    * 您可以更改交货行的数量。 如果更改，业务行将自动更新为交货行中的总数量。  
1. 在第一个交货行的“数量”字段中，将数量从 4 更改为 5。
2. 选择第一个订单行（业务行）。
    * 业务行中的数量已更改为 11。  

## <a name="process-product-receipt-using-delivery-schedules"></a>使用交货计划处理产品收货
    * 必须先确认采购订单，才能处理产品收货。 在此示例中，直接在采购订单上记录收货。 也可以在货物到达仓库时记录收货。  
1. 在操作窗格上，单击“采购”。
2. 单击“确认”。
3. 在操作窗格上，单击“接收”。
4. 单击“产品收据”。
5. 在“物料收货”字段中键入任何值。
    * 此字段用于输入将用作产品收货日记帐的凭证的参考。  
    * 在“数量”字段中，选择“订购数量”。 此选项表示将处理随订单行创建的数量的收货。  
    * 确保“打印产品收货”字段设置为“否”。 此示例中无需打印。  
6. 展开“行”部分。
    * 请注意如何为两个交付行创建产品收货，而不是为原始订单行创建。 如果收货已在仓库中记录，则还会在交货计划行中记录。  
7. 折叠“行”部分。
8. 单击“确定”以过帐收据。

