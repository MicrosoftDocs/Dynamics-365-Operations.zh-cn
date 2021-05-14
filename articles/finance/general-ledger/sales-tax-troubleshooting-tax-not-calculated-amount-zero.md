---
title: 未计算税款或税额为零
description: 本主题提供可以在税额为 0（零）或未计算税款时提供帮助的故障排除信息。
author: shtao
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: ead979081692d4dcee9812c89f5f10c7879d3f7e
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947602"
---
# <a name="tax-isnt-calculated-or-the-tax-amount-is-zero"></a>未计算税款或税额为零

[!include [banner](../includes/banner.md)]

交易的行金额可能存在不是 0（零），但未计算税款或计算出的税额为 0 的情况。 要解决此问题，请根据需要按照以下各节中的步骤操作。

## <a name="verify-that-tax-codes-are-correctly-selected-by-the-transaction"></a>验证交易是否正确选择了税代码

如果交易未选择正确的税代码，或者未选择任何税代码，将不会计算税款。 请按照以下步骤验证交易是否正确选择了税代码。 

1. 在交易行的 **行详细信息** 快速选项卡上，在 **设置** 选项卡的 **销售税** 部分，验证是否在 **物料销售税组** 和 **销售税组** 字段中选择了正确的税组。 如果未选择正确的税组，请进行选择。

    [![“物料销售税组”和“销售税组”字段](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)

2. 转到 **税** \> **间接税** \> **销售税** \> **销售税组**。
3. 选择适当的销售税组，然后在 **设置** 快速选项卡上，记下 **销售税代码** 字段中的税代码。

    [![销售税组页面](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)

4. 转到 **税** \> **间接税** \> **销售税** \> **物料销售税组**。
5. 选择适当的物料销售税组，然后在 **设置** 快速选项卡上，验证 **销售税代码** 字段中的税代码与销售税组的税代码是否匹配。

    [![物料销售税组页面](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)

6. 如果税代码不匹配，更新其中一个组的销售税代码。

## <a name="verify-that-the-selected-tax-codes-arent-exempt-and-that-they-have-the-correct-tax-rate-value"></a>确认所选的税代码不免税并具有正确的税率值

如果税代码免税，或者税率是 0（零），税款计算结果将是 0。 请按照以下步骤确定所选的税代码是否免税，并验证是否对它们应用了正确的税率。

1. 转到 **税** \> **间接税** \> **销售税** \> **销售税组**。
2. 选择适当的销售税组，然后，在 **设置** 快速选项卡上，验证 **免税** 复选框是否清除。 如果已选中，请清除。

    [![“销售税组”页上的“免税”复选框](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)

3. 转到 **税** \> **间接税** \> **销售税** \> **销售税代码**。
4. 选择适当的销售税代码，然后验证 **值** 字段中的税率值是否不为 0（零）。 如果为 0，更新该字段，将其设置为正确的税率。

    [![销售税代码值页面上的“值”字段](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)

## <a name="determine-whether-zero-is-the-correct-tax-amount"></a>确定零是否是正确的税额

在有些情况下，税额为 0（零）是正确的。 请按照以下步骤确定 0 是否是您的交易的正确税额。

1. 转到 **总帐** \> **分类帐设置** \> **总帐参数**。
2. 在 **销售税** 选项卡上，在 **计算方法** 字段中，确认选择了 **总计**。

    [![“总帐参数”页上的“计算方法”字段](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)

3. 转到 **税** \> **间接税** \> **销售税** \> **销售税代码**。
4. 选择适当的销售税代码，选择 **计算**\>**边际基数**，确认边际基数设置为 **发票余额的净额** 或 **包括其他销售税金额的发票合计**。 有关详细信息，请参阅[包括其他销售税金额的发票合计](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts)。
5. 如果在步骤 2 和 4 中设置了正确的值，请确定交易的总金额是否为 0（零）。 如果总金额为 0，税额为 0 则是预期结果。 因为税款计算基于发票余额的总金额，并且该金额不是逐行计算的，所以税额 0 将在税款计算后分配给每一行。

## <a name="determine-whether-customization-exists"></a>确定是否存在自定义

如果您已经完成了前面几节中的步骤，但未发现问题，请确定是否存在自定义。 如果不存在自定义，请创建 Microsoft 服务请求寻求进一步支持。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
