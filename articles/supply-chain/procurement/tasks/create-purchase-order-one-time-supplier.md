---
title: 创建零星供应商的采购订单
description: 此过程演示如何为零星供应商创建采购订单。
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d1abd942da608bc221a7a66e03b5269fa30e2c20
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212022"
---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a>创建零星供应商的采购订单

[!include [banner](../../includes/banner.md)]

此过程演示如何为零星供应商创建采购订单。 供应商随采购订单自动创建，而不必手动创建供应商帐户。 采购订单通常由采购代理创建。 可以在 USMF 演示数据公司中使用本指南中的示例。 前提是已在“应付账款参数”页中设置了零星供应商帐户。


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a>创建零星供应商的采购订单
1. 转到“采购”>“采购订单”>“所有采购订单”。
2. 单击“新建”。
3. 在“零星供应商”字段中，选择“是”。
    * 将自动创建供应商帐户并分配给采购订单。 供应商帐户基于“应付账款参数”页中“常规”选项卡上指定的模板创建供应商帐户。  
4. 在“名称”字段中，键入该供应商的名称。
5. 单击“确定”。
    * 采购订单现在可以和其他任何订单一样完成和处理。 方法没有任何特别特征。 发票将记录供应商帐户中随订单创建的到期交易，然后处理付款。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]