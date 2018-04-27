---
title: "发票匹配和内部公司采购订单"
description: "涉及内部公司交易的采购法人设置为使用应付账款发票匹配。 在这种情况下，内部公司交易和应付账款发票匹配的过帐需求必须满足（在内部公司供应商过帐发票前）。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchLineMatchingPolicy
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3101
ms.assetid: 9c7c2e44-45f8-4325-b6de-a09fe790f9cf
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 3d0eb5c19c07313f4d4c0bac1b9c48375446afd9
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="invoice-matching-and-intercompany-purchase-orders"></a>发票匹配和内部公司采购订单

[!INCLUDE [banner](../includes/banner.md)]

涉及内部公司交易的采购法人设置为使用应付账款发票匹配。 在这种情况下，内部公司交易和应付账款发票匹配的过帐需求必须满足（在内部公司供应商过帐发票前）。

本主题中的示例为内部交易记录使用以下设置：
-   Fabrikam Purchase 为采购法人。
-   Fabrikam Sales 为销售的法人。
-   客户 4020 存在于 Fabrikam Sales 中。
-   供应商 3024 存在于 Fabrikam Purchase 中。
-   在 Fabrikam Purchase 中，为供应商 3024 指定了内部公司信息。 Fabrikam Sales 指定为客户公司，并且客户 4020 指定为对应于 Fabrikam Purchase 法人的客户帐户。
-   在 Fabrikam Sales 中，为客户 4020 指定了内部公司信息。 Fabrikam Purchase 指定为供应商公司，并且供应商 3024 指定为对应于 Fabrikam Purchase 法人的供应商帐户。

这些示例使用针对 Fabrikam Purchase 的以下应付账款发票匹配设置：
-   当在“应付账款参数”页上，选择了“启用发票匹配验证”选项。
-   在“应付账款参数”页上，“过帐具有差异的发票”选项设置为“要求审核”。
-   法人的价格容差百分比设置为 2。

## <a name="example-price-matching-and-intercompany-trade"></a>示例：具有内部公司交易的价格匹配
内部公司供应商发票和内部公司客户发票的净额必须相等。 此要求优先于所有适用发票匹配审核或价格容差百分比。 例如，您可以执行以下步骤。
1.  在 Fabrikam Purchase 中，为客户 4020 创建销售订单 SO888。 内部公司采购订单 ICPO222 自动在 Fabrikam Purchase 中为供应商 3024 创建，销售订单 ICSO888 自动在 Fabrikam Sales 中创建。
2.  在 Fabrikam Sales 中，登记已接收的物料并且过帐装箱单。 ICSO888 的状态更改为“已交货”。 ICPO222 的状态更改为“已收货”。
3.  在Fabrikam Sales中，为ICSO888执行发票更新。 单位价格是 0.45，并且更新 100 项。
4.  在Fabrikam Purchase中为 ICPO222 创建一个发票。 偶然将净价从 45.00 更改为 54.00。 显示一个图标，指示价差超出 2% 的允许价格容差。
5.  在“发票匹配详细信息”页上，选择该选项以审核具有匹配差异的过帐。 在供应商发票页上，单击“确定”。 如果供应商发票不是内部公司供应商发票，过帐成功。 但是，因此，使用您的内部公司供应商发票时，过帐未获成功。 对于内部交易记录，在内部公司销售订单的发票合计必须等于相应内部公司采购订单上的发票合计。 为了解决此问题，您必须通过将净价更正为发票上的净价默认金额，例如 45.00。

## <a name="example-quantity-matching-with-intercompany-trade"></a>示例：具有内部公司交易的数量匹配
内部公司采购订单和内部公司销售订单数量必须相等。 此要求优先于所有适用的发票匹配审核。 此示例使用以下附加内部公司交易设置：
-   在 Fabrikam Purchase 中为供应商 3024 设置采购订单操作策略，设置为自动过帐原始客户发票和内部公司供应商发票。

此示例使用针对 Fabrikam Purchase 的以下附加的应付账款发票匹配设置：
-   在物料 B-R14 使用的模型组的“物料模型组”页上，选择了“接收要求”选项。
-   物料 B-R14 的现有数量是 0（零）。

例如，您可以执行以下步骤。
1.  在 Fabrikam Purchase 中，为客户 4020 创建销售订单 SO999。 此订单何中包含一个行项：100 节电池（物料 B-R14），单位价格为 1.00。 内部公司采购订单 ICPO333 自动在 Fabrikam Purchase 中为供应商 3024 创建，销售订单 ICSO999 自动在 Fabrikam Sales 中创建。
2.  在 Fabrikam Sales 中，执行 ICSO999 的发票更新。 因为物料库存不足并且尚未收货，过帐时未获成功。 因此，不能更新财务信息。
3.  登记已接收的物料并且为 Fabrikam Sales 中的 ICSO999 过帐装箱单。 ICPO333 的产品收货在 Fabrikam Purchase 中为自动过帐。 在 Fabrikam Purchase 中为物料 B-R14 接收的数量更改为 100。
4.  在 Fabrikam Sales 中，执行 ICSO999 的发票更新。 过帐在两法人中均成功。 在 Fabrikam Purchase 中为物料 B-R14 采购的数量更改为 100。






