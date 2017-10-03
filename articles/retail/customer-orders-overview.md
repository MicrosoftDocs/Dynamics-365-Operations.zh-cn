---
title: "客户订单概览"
description: "此主题提供有关 Retail Modern POS (MPOS) 中的客户订单的信息。 客户订单也称为特殊订单。 此主题中包含对相关参数和交易记录流的讨论。"
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 89e79c7227e05eec539d9bb142b8f41de092f01b
ms.contentlocale: zh-cn
ms.lasthandoff: 06/20/2017



---

# <a name="customer-orders-overview"></a>客户订单概览

[!include[banner](includes/banner.md)]


此主题提供有关 Retail Modern POS (MPOS) 中的客户订单的信息。 客户订单也称为特殊订单。 此主题中包含对相关参数和交易记录流的讨论。

在 omni 渠道零售环境中，许多零售商提供客户订单（即特殊订单）选项，以满足各种产品和履行要求。 下面是一些典型方案：

-   客户希望将产品在特定日期发到特定地址。
-   客户希望从非购买产品的商店或位置取货。
-   客户希望其他人取自己购买的产品。

零售商也可以使用客户订单将库存不足可能导致的失单降到最低，因为可以在其他时间或位置发货或取货。

## <a name="set-up-customer-orders"></a>设置客户订单
下面是一些可在**零售参数**页面中设置来定义如何履行客户订单的参数。

-   **默认保证金百分比** – 指定确认订单前客户必须以存款的形式支付的金额。 默认保证金金额为订单值的百分比。 售货员可能可以根据其权限通过使用**保证金覆盖**来覆盖该金额。
-   **取消费百分比** – 如果取消客户订单时需要收取费用，请指定这笔费用的金额。
-   **取消费代码** – 如果取消客户订单时需要收取费用，将在销售订单内的收费代码下体现这笔费用。 可使用此参数定义取消费代码。
-   **装运费用代码** – 零售商可为将商品装运到客户再收取一笔费用。 销售订单内的收费代码下将体现这笔装运费用的金额。 可使用此参数将装运费用代码映射到客户订单中的装运费用。
-   **退回装运费用** – 指定是否可退回客户订单关联的装运费用。
-   **未经审核的最大金额** – 如果装运费用可退回，指定退货单中的最大装运费用退款金额。 如果超过了此金额，需要经历覆盖才能继续退款。 为了满足以下方案，装运费用的退款可能超过最初支付的金额。
    -   费用在销售订单抬头级别实施，并且如果退回了某个产品行的一定数量，则不能按照适合所有零售客户的方式确定为这些产品和数量允许的最大装运费用退款。
    -   每次运货都会产生装运费用。 如果客户多次退货，而零售商的政策规定由零售商承担退货装运费用的成本，退货装运费用将超过实际装运费用。

## <a name="transaction-flow-for-customer-orders"></a>客户订单的交易记录流
### <a name="create-a-customer-order-in-retail-modern-pos"></a>在 Retail Modern POS 中创建客户订单

1.  将客户添加到交易记录。
2.  向购物车添加产品
3.  单击**创建客户订单**，然后选择订单类型。 订单类型可以是**客户订单**或**报价**。
4.  单击**装运所选产品**或**全部装运**，将产品装运到客户订单中的地址，指定请求的装运日期，然后指定装运费用。
5.  单击**提取所选产品**或**全部提货**，选择将在特定日期从当前商店或其他商店提取的产品。
6.  如果需要保证金，收取保证金。

### <a name="edit-an-existing-customer-order"></a>编辑现有客户订单

1.  在主页中，单击**查找订单**。
2.  查找并选择要编辑的订单。 在页面底部，单击**编辑**。

### <a name="pick-up-an-order"></a>订单拣货

1.  在主页中，单击**查找订单**。
2.  选择要拣货的订单。 在页面底部，单击**领料和装箱**。
3.  单击**提货**。

### <a name="cancel-an-order"></a>取消订单

1.  在主页中，单击**查找订单**。
2.  选择要取消的订单。 在页面底部，单击**取消**。

#### <a name="create-a-return-order"></a>创建退货单

1.  在主页中，单击**查找订单**。
2.  选择要退货的订单，选择订单的发票，然后选择要退货的商品的产品行。
3.  在页面底部，单击**退货单**。

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>客户订单的异步交易记录流
可以在同步模式或异步模式下，从销售点 (POS) 客户端创建客户订单。

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>将客户订单设置为可在异步模式下创建

1.  单击**零售** &gt; **渠道设置** &gt; **POS 设置** &gt; **POS 配置文件** &gt; **功能配置文件**。
2.  在**常规**快速选项卡上，将**在异步模式下创建客户订单**选项设置为**是**。

当**在异步模式下创建客户订单**选项设置为**是**，将始终在异步模式下创建客户订单，即使 Retail Transaction Service (RTS) 可用。 如果将此选项设置为**否**，将始终通过使用 RTS 在同步模式下创建客户订单。 在异步模式下创建客户订单时，将通过提取 (P) 作业提取客户订单并插入到 Retail 中。 手动或通过批处理流程运行**同步订单**时，将在 Retail 中创建相应销售订单。

<a name="see-also"></a>请参阅
--------

[混合客户订单](hybrid-customer-orders.md)




