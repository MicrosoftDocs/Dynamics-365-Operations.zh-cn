---
title: 信用卡设置、授权和捕获
description: 本文提供 Microsoft Dynamics 365 Finance 中的信用卡授权的概览。 其中包含有关如何设置付款服务，添加信用卡到销售订单和取消授权的信息。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CreditCardProcessors, CustTable, SalesTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 3041
ms.assetid: 678f6899-bfa5-439b-aaca-b4affcc338ba
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0de35934e8bdb160f68f68dab118997d0141bf29
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440619"
---
# <a name="credit-card-setup-authorization-and-capture"></a>信用卡设置、授权和捕获

[!include [banner](../includes/banner.md)]

本文提供 Microsoft Dynamics 365 Finance 中的信用卡授权的概览。 其中包含有关如何设置付款服务，添加信用卡到销售订单和取消授权的信息。

<a name="setting-up-the-credit-card-payment-service"></a>设置信用卡付款服务
------------------------------------------

若要使用信用卡，您必须设置并激活付款服务页的付款服务。 付款服务充当您的法人和处理客户信用卡费用的银行之间的桥梁。 您必须使用在“付款连接器”字段中列出的信用卡提供商，并在该提供商那里设置帐户。 然后必须在“付款服务”页设置其他选项，在“信用卡类型”页上设置信用卡类型为 American Express、Discover、MasterCard 和 Discover，并激活提供商为默认提供商。 您还必须按照下面的步骤完成您的设置：
-   在“应收帐款参数”页，指定用于信用卡授权的参数。
-   在“付款期限”页，设置信用卡的付款期限。 在“付款类型”字段中，选择“信用卡”。
-   在“客户信用卡”页，输入客户的信用卡信息。

## <a name="adding-a-new-credit-card"></a>添加新的信用卡
通过使用“客户”、“设置”、“信用卡”在“客户”页创建新的信用卡记录。 在“销售订单”页输入销售订单时，还可以通过使用“管理”、“客户”、“信用卡”、“登记”创建信用卡记录。

<a name="adding-a-credit-card-to-a-sales-order"></a>将信用卡添加到销售订单
-------------------------------------

您可以添加信用卡到销售订单，方法是通过在“销售订单”页的“价格和折扣”快速选项卡上的信用卡查找中选择信用卡。 若要开始授权流程，在“操作窗格”，在“管理”选项卡上，选择“信用卡和授权”。

<a name="authorizing-a-credit-card"></a>授权信用卡
-------------------------

在对某一信用卡进行授权时，验证信用卡号和持卡人的名字，并且确认可用的信用卡余额。 或者，验证卡验证值和持卡人的地址。 然后，从该客户的可用信用卡余额中减去发票金额。 付款服务将发送信用卡已核准或拒绝的信息。 在给销售订单开票时，按发票金额对信用卡计费（已捕获）。

### <a name="card-verification-value"></a>卡验证值

您可以要求卡验证值，此值有时候称作卡的安全代码。 对于美国运通，这是一个四位数值。 对于 Discover、MasterCard 和 Visa，它是一个三位数字的值。

### <a name="address-verification"></a>地址验证

地址验证信息始终发送到付款提供商。 您可以决定交易记录需要的信息量以接受交易记录。 请确保向您的提供商确定其是否可以接受此信息。 这是地址验证的选项：
-   **始终接受交易记录** – 无论地址验证结果，接受交易记录。
-   **帐户持有人** – 将交易记录的持卡人的姓名与公司信息进行比较。
-   **帐单地址** – 将交易记录的持卡人姓名和帐单地址与信用卡公司的信息进行比较。
-   **帐单邮政编码** – 将交易记录的持卡人姓名、帐单地址和邮政编码与信用卡公司的信息进行比较。

## <a name="data-support"></a>数据支持
对于支持的每个信用卡类型，您可以指定数据支持的级别。 级别控制将交易记录的多少信息转移到付款服务。 请确保向您的提供商确定其是否可以提供此信息。 这是数据支持级别的选项：
-   **级别 1** – 转移交易记录日期、交易记录金额和描述。
-   **级别 2** – 转移所有级别 1 信息，以及装运和商人地址和税务信息。
-   **级别 3** – 转移所有级别 2 信息，以及订单行信息。

## <a name="partial-payments"></a>部分付款
如果发送部分订单，捕获部分订单的金额，并且授权关闭，该授权针对整个订单的金额 然后，新的权限针对尚未装运订单的余额提交。

## <a name="voiding-an-authorization"></a>取消授权
若要取消信用卡授权，您可以将付款方法更改为没有“信用卡类型”的其他方法。







[!INCLUDE[footer-include](../../includes/footer-banner.md)]