---
title: 税款过帐到凭证中错误的会计科目
description: 本主题提供可以在税款过帐到凭证中错误的会计科目时提供帮助的故障排除信息。
author: qire
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 3d60265df7ff1f447e20866b8b8a447d88db8cc4b3dccedebc0f18ce8f0f70dc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746312"
---
# <a name="tax-is-posted-to-the-wrong-ledger-account-in-the-voucher"></a>税款过帐到凭证中错误的会计科目

[!include [banner](../includes/banner.md)]

过帐期间，税款可能被过帐到凭证中错误的会计科目。 要解决此问题，请根据需要按照以下各节中的步骤操作。 本主题中的示例使用销售订单作为业务文档。

## <a name="find-the-tax-code-of-the-incorrectly-posted-tax-transaction"></a>查找错误过帐的税收交易的税代码

1. 在 **凭证交易** 页上，选择要处理的交易，然后选择 **已过帐销售税**。

    [![“凭证交易”页面上的已过帐销售税按钮。](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)

2. 查看 **销售税代码** 字段中的值。 在此示例中，是 **增值税 19**。

    [![“已过帐销售税”页面上的“销售税代码”字段。](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)

## <a name="check-the-ledger-posting-group-of-the-tax-code"></a>检查税代码的分类帐过帐组

1. 转到 **税** \> **间接税** \> **销售税** \> **销售税代码**。
2. 找到并选择税代码，然后查看 **分类帐过帐组** 字段中的值。 在此示例中，是 **增值税**。

    [![“销售税代码”页面上的“分类帐过帐组”字段。](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)

3. **分类帐过帐组** 字段中的值是一个链接。 要查看组配置的详细信息，选择该链接。 或者，在字段中选择并按住（或右键单击），然后选择 **查看详细信息**。

    [![“查看详细信息”命令。](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)

4. 在 **应付销售税** 字段中，根据交易类型验证科目编号是否正确。 如果不正确，请选择要过帐到的正确科目。 在此示例中，应将销售订单的销售税过帐到应付销售税科目 222200。

    [![“分类帐过帐组”页面上的“应付销售税”字段。](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png)

    下表提供了有关 **分类帐过帐组** 页上每个字段的信息。

    | 字段                  | 说明 |
    |------------------------|-------------|
    | 应付销售税      | 应付给税务主管机构的输出销售税的主科目。 |
    | 应收销售税   | 从税务主管机构收到的进项税的主科目。 |
    | 销项税支出        | 此主科目用于过帐供应商不在欧盟 (EU) 反向计费商品劳务税 (GST)/统一销售税 (HST) 中向税务主管机构要求或报告的可扣减销项税。 必须为在交易中使用的销售税组的销售税代码选择 **销项税**。 如果在 **总帐参数** 页上选择了 **应用销售税纳税规则**，此字段则不可用。 |
    | 应付销项税        | 用于过帐应付给税务主管机构的所得销项税的主科目。 |
    | 结算帐户     | 用于过帐在 **应付销项税** 和 **应收销售税** 字段中指定的会计科目的净余额的主科目。 |
    | 供应商现金折扣   | 用于过帐与此分类帐过帐组关联的销售税代码的现金折扣的主科目。 |
    | 客户折扣 | 用于过帐与此分类帐过帐组关联的销售税代码的现金折扣的主科目。 |

    有关详细信息，请参阅[设置销售税分类帐过帐组](tasks/set-up-ledger-posting-groups-sales-tax.md)

## <a name="debug-in-code-to-check-ledger-dimensions"></a>调试代码以检查分类帐维度

在代码中，过帐科目由分类帐维度确定。 分类帐维度将科目的记录 ID 保存在数据库中。

1. 对于销售订单，在 **Tax::saveAndPost()** 和 **Tax::post()** 方法处添加中断点。 注意 **\_ledgerDimension** 的值。

    [![具有中断点的销售订单代码示例。](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)

    对于采购订单，在 **TaxPost::saveAndPost()** 和 **TaxPost::postToTaxTrans()** 方法处添加中断点。 注意 **\_ledgerDimension** 的值。

    [![具有中断点的采购订单代码示例。](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)

2. 运行以下 SQL 查询，根据分类帐维度保存的记录 ID 在数据库中查找科目的显示值。

    ```sql
    select * from DIMENSIONATTRIBUTEVALUECOMBINATION where recid={the value of _ledgerDimension}
    ```

    [![记录 ID 的显示值。](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)

3. 检查调用堆栈，查找分配 **_ledgerDimension** 值的位置。 通常，此值来自 **TmpTaxWorkTrans**。 在这种情况下，您应该在 **TmpTaxWorkTrans::insert()** 和 **TmpTaxWorkTrans::update()** 处添加中断点来查找分配值的位置。

## <a name="determine-whether-customization-exists"></a>确定是否存在自定义

如果您已经完成了前面几节中的步骤，但未发现问题，请确定是否存在自定义。 如果不存在自定义，请创建 Microsoft 服务请求寻求进一步支持。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
