---
title: "客户订单概览"
description: "此主题提供与客户有关订单的信息。Retail Modern POS (MPOS)。 也称作客户订单是特殊订单。 主题包括单个交易相关参数和记录流程的方式。"
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 2f466dfe53ccf0be15ed0793b4a6dd371bdacc0d
ms.lasthandoff: 03/31/2017


---

# <a name="customer-orders-overview"></a>客户订单概览

此主题提供与客户有关订单的信息。Retail Modern POS (MPOS)。 也称作客户订单是特殊订单。 主题包括单个交易相关参数和记录流程的方式。

在 Omni 渠道零售通用，零售商提供许多客户订单或特殊订单的选项，以满足各种产品和履行要求。 这是一些典型的情况：

-   客户所希望交付产品到特定日期的特定一个地址。
-   客户希望领取不同于商店或库位客户采购这些产品的商店或位置的产品。
-   客户所希望领取他人客户采购的产品。

零售商也使用客户订单将库存停机否则可能导致的交易的增值，因为该商品可以在不同的时间或地点交货或已领取。

## <a name="set-up-customer-orders"></a>安装客户订单
这是在的某些键**零售参数**页可以将客户定义订单如何完成：

-   **存款**默认百分比–指定客户必须支付的金额，然后，向订单可以确认之前。 默认的存款金额相对于订单，计算值。 权限，根据商店关联可以覆盖金额可能使用**存款**覆盖。
-   ** **注销费百分比–费用，则将应用，当客户订单取消时，金额指定该费用。
-   **注销费用代码** –费用，则将应用，当客户订单中删除，则该费用将反映在"销售订单的费用代码下在 Microsoft Dynamics AX。 使用此参数定义注销费用代码。
-   **装运费用代码** –零售商可以收取装运的货物的一种附加费用到客户。 金额该装运费用将反映在"销售订单的费用代码下 Dynamics AX。 使用此参数可以映射装运费用代码到客户订单的装运费用。
-   **退款装运费用** –指定与客户订单的装运费用。可为偿还的。
-   **未审核的最大金额– **，则装运费用中，装运费用的偿还指定最大金额退款在退货单上。 如果多用于经理覆盖此金额，要求以继续退款。 要使用以下方案，则装运费用凭证可以超出最初的支付金额：
    -   费用应用在销售订单标题的级别，因此，如果产品系列的一定数量均已返回时，允许产品和数量装运费用的最大退款不能确定以该方式为所有零售作业。
    -   装运费用用于装运导致每个实例。 如果客户退回产品多个时间，并且，零售商的策略指定该零售商负担成本将退货装运费用，退货装运费用的实际装运费用将大于。

## <a name="transaction-flow-for-customer-orders"></a>客户订单的交易记录流程
### <a name="create-a-customer-order-in-retail-modern-pos"></a>创建在 Retail Modern POS 的客户订单

1.  将客户添加到交易记录。
2.  产品添加到购物车。
3.  **单击创建客户订单**，然后选择订单类型。 **或订单类型可以是客户或订单** ** **询价。
4.  **单击所选装运**或**请装运所有**装运产品到客户帐户的地址，指定日期发送请求，并且指定装运费用。
5.  **请单击领取所** **或领取所有**请选择从当前商店或不同的商店将领取日期的特定产品。
6.  如果需要，缴纳的存款金额存入银行。

### <a name="edit-an-existing-customer-order"></a>编辑现有客户订单

1.  在"主页，请单击**查找**订单。
2.  查找并选择要编辑的订单。 在页面底端，请单击** **编辑。

### <a name="pick-up-an-order"></a>领取订单

1.  在"主页，请单击**查找**订单。
2.  选择订单安排。 在页面底端**，单击"领料和包装**。
3.  ** **请单击"排列。

### <a name="cancel-an-order"></a>取消订单

1.  在"主页，请单击**查找**订单。
2.  选择取消订单。 在页面底端，请单击** **取消。

#### <a name="create-a-return-order"></a>创建退货单

1.  在"主页，请单击**查找**订单。
2.  选择订单返回，选择订单的发票，然后选择该商品的产品系列退回。
3.  在页面底端，请单击** **请返回订单。

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>客户订单的异步流量的交易记录
客户订单同步情况下可以从或的异步模式销售点 (POS) 客户。

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>启用在异步模式创建客户订单

1.  在 Dynamics AX，请单击**零售和商务** &gt; **的设置渠道** &gt; **的设置 POS ** &gt; ** POS 模板** &gt; ** **功能配置文件。
2.  ** **在"常规"选项卡上 FastTab，设置该**创建在 async 模式的客户订单**是** **选项。

在启用多**创建在 async 模式的客户订单**选项设置** **为客户订单，在异步模式始终创建，即使 Retail Transaction Service (RTS) 才可用。 如果将此选项设置** **不使用 RTS，客户，始终在订单同步方式创建。 当客户订单在异步模式时，申请并插入到 Dynamics AX。拉出 (P) 作业。 相应的销售订单在 Dynamics AX，请创建在** **运行同步订单时手动或通过批次流程。

<a name="see-also"></a>请参阅
--------

较 [客户订单 orders.md 较] (客户)


