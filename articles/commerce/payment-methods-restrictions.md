---
title: 限制没有收据的退货的付款方式
description: 此主题描述如果在没有收据的情况下退货，如何为退款限制某些付款类型。
author: rapraj
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2019-02-01
ms.dyn365.ops.version: AX 10.0.0, Retail Feb 2019 update
ms.openlocfilehash: 1ff301aa5f88e34ed7ca24aa54df3fdc7daa1bf7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012383"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>限制没有收据的退货的付款方式


[!include [banner](includes/banner.md)]

设置系统时，必须配置零售商接受的每种付款类型。 此主题描述如果在没有收据的情况下退货，如何为退款限制某些付款类型。

## <a name="set-up-payment-methods"></a>设置付款方式

若要设置付款方式，必须完成以下任务。
1. 创建的整个组织收到的付款方式。
2. 创建组织范围的卡类型和卡号。 如果接受信用卡或借记卡，则必须创建一种卡支付方式，然后创建组织范围的卡类型和卡号。
3. 设置商店付款方式。 将付款方式与每个商店，然后输入每个特定于商店设置的付款方式。
4. 为存储设置卡付款方式。 对于商店接收的所有卡支付方式，请完成卡设置。

![商店设置](media/NoReceiptReturns1.png "零售商店设置") 


## <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>限制没有收据的退货的付款方式

对于每个商店付款方式，在 **商店管理** 页上，在 **非收据退货** 下，将 **对没有收据的退货限制** 设置为 **是**。 

切换的默认值为 **否**，这确保退款允许该付款方式。 

在 **对没有收据的退货限制** 设置为 **是** 时，退款将不允许所选付款方式。 

![商店付款方式](media/NoReceiptReturns3.png "零售商店付款方式") 

> [!NOTE]
> 在出纳选择为没有收据的退货限制的付款方式时，将显示一条消息来验证可接受的付款方式。

![可接受的付款方式](media/NoReceiptReturns4.png "可接受的付款方式") 

如果某一交易既有有收据的退货，也有没有收据的退货，由于这类交易将是有收据的退货工作流，因此不强制使用限制条件。 



[!INCLUDE[footer-include](../includes/footer-banner.md)]