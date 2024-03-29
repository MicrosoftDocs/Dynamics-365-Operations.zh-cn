---
title: 配置结算
description: 交易记录的结算方式和时间可能非常复杂，因此，您理解并正确定义参数以满足您的业务需求非常重要。 本文介绍用于应付帐款和应收帐款的结算的参数。
author: angelad116
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, CustParameters, VendOpenTrans, VendParameters
audience: Application User
ms.reviewer: kfend
ms.custom: 14601
ms.assetid: 6b61e08c-aa8b-40c0-b904-9bca4e8096e7
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a0aae3d72d35e8c09b2a3dc8d25958be4c523969
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151841"
---
# <a name="configure-settlement"></a>配置结算

[!include [banner](../includes/banner.md)]

交易记录的结算方式和时间可能非常复杂，因此，您理解并正确定义参数以满足您的业务需求非常重要。 本文介绍用于应付帐款和应收帐款的结算的参数。 

以下参数将影响如何在 Microsoft Dynamics 365 Finance 中处理结算。 结算是对照付款或贷方通知单结算发票的流程。 这些参数位于 **应收帐款参数** 和 **应付帐款参数** 页的 **结算** 区域。

- **自动结算** – 如果交易记录在过帐时应自动对照其他未结交易记录结算，则设置此选项为 **是**。 如果此选项设置为 **否**，用户可以使用 **结算交易记录** 页在输入付款或之后手动结算交易记录。
- **现金折扣管理** – 指定[当发票超额支付时如何处理现金折扣](cash-discount-handling-overpayments.md)。 对于超额支付，可以减少现金折扣，可作为差额对待，也可以为供应商或客户在帐户中保留。
  -   **不指定** – 现金折扣金额减去超额支付金额。 此行为始终使用，无论超额支付金额高于还是低于在 **最大超额支付或支付不足** 字段中输入的金额。
  -   **指定** – 超额付款金额或者被过帐到现金折扣差额分类帐帐户或作为余额留在客户或供应商帐户上。 该特定行为取决于超额支付金额是否介于 0.00 和在 **最大超额支付或支付不足** 字段中输入的金额之间，或者超额支付金额是否大于 **最大超额支付或支付不足** 金额。
- **最大尾差** – 输入结算交易记录允许的最大尾差。 如果差异等于或小于此字段中指定的尾差，则该差异将过帐到 **自动交易记录帐户** 页中指定的尾差会计科目。
- **最大超额支付或支付不足** – 输入超额支付和支付不足接受的金额。 若要计算超额支付或支付不足所产生的税金，请在 **总帐参数** 页中，单击 **销售税**，然后选择 **有关超缴或欠缴的销售税** 选项。
  -   如果超额支付或支付不足产生的尾差小于 **最大尾差** 字段中定义的差额，该尾差金额将过帐到尾差科目。
  -   如果超额支付或支付不足产生的尾差大于 **最大尾差** 字段中定义的差额，该差异金额将过帐到为 **自动交易记录帐户** 页的 **客户现金折扣** 或 **供应商现金折扣** 选择的差额科目。
- **计算部分付款的现金折扣** – 将此选项设置为 **是** 允许现金折扣为部分付款自动计算。
  -   此选项的此影响取决于 **结算交易记录** 页的 **使用现金折扣** 字段的值。 如果将此选项设置为 **是**，折扣将在 **使用现金折扣** 字段设置为 **标准** 时执行。 当 **使用现金折扣** 字段设置为 **始终** 时，将始终执行现金折扣，不论此字段如何设置。 当 **使用现金折扣** 字段设置为 **从不** 时，将从不执行现金折扣，不论此字段如何设置。
  -   如果此选项设置为 **是**，用户更改 **结算交易记录** 页上的 **要结算的金额** 字段中的值，则折扣将自动计算，并在 **要提取的现金折扣金额** 字段中显示为默认条目。
  -   如果此选项设置为 **否**，用户更改 **结算交易记录** 页的 **要结算的金额** 字段中的值，则 **要提取的现金折扣金额** 字段中的默认条目为 **0**（零）。
- **计算贷方通知单的现金折扣** – 将此选项设置为 **是** 以自动计算贷方通知单的现金折扣。 在应收帐款中，贷方通知单交易记录是在 **普通发票** 页的 **发票** 字段中具有值的负交易记录，或在 **销售订单** 页上的退货。
  - 此选项的此影响取决于<strong>结算交易记录</strong>页的<strong>使用现金折扣</strong>字段的值。 如果将此选项设置为 <strong>是</strong>，折扣将在 *<strong><em>使用现金折扣</em></strong>* 字段设置为<strong>标准</strong>时执行。 当 *<strong><em>使用现金折扣</em></strong>* 字段设置为<strong>始终</strong>时，将始终执行现金折扣，不论此字段如何设置。 当 *<strong><em>使用现金折扣</em></strong>* 字段设置为<strong>从不</strong>时，将从不执行现金折扣，不论此字段如何设置。
  - 如果此选项设置为 **是**，并且在 **结算未结交易记录** 页中标记了贷方通知单，则折扣将自动计算，并在 **要提取的现金折扣金额** 字段中显示为默认条目。
  - 如果此选项设置为 **否**，并且在 **结算未结交易记录** 页中标记了贷方通知单，则 **要提取的现金折扣金额** 字段中的默认条目为 **0**（零）。

- **折扣对方科目（仅应付帐款）**– 定义应为现金折扣的会计条目使用的默认现金折扣会计科目。
  -   **使用供应商折扣的主科目** – 现金折扣过帐到在 **现金折扣设置** 页上定义的主科目。
  -   **发票行上的科目** – 现金折扣过帐到原始发票的会计科目。
- **普通发票和利息单上的标记行（仅应收帐款）** – 此选项设置为 **是** 启用 **输入客户付款**、**付款日记帐凭证** 和 **结算交易记录** 页的 **标记发票行** 按钮。 此按钮允许用户标记结算的各行。
- **设置结算的优先级（仅应收帐款）** – 设置此选项为 **是** 将启用 **输入客户付款** 和 **结算交易记录** 页的 **按优先级标记** 按钮。 此按钮允许用户分配预先确定的结算订单到交易记录。  在结算订单应用于交易记录后，订单和付款分配可以在过帐前进行修改。
- **使用自动结算的优先级** – 将此选项设置为 **是** 以在交易记录自动结算时使用定义的优先级顺序。 只有当 **设置结算的优先级** 和 **自动结算** 选项设置为 **是** 时，此字段才可用。

## <a name="fixed-dimensions-on-accounts-receivableaccounts-payable-main-accounts"></a>应收帐款/应付帐款主科目中的固定维度

如果应收帐款/应付帐款主科目中使用固定维度，结算流程将过帐更多会计条目和另外两个供应商交易记录。 结算将比较来自发票和付款的应收帐款/应付帐款会计科目。  如果付款和结算同时完成（这种情况非常典型），则结算流程也完成之前，不会将付款的会计条目过帐到总帐。 由于事件的处理顺序的关系，结算不能根据付款的会计条目确定实际应收帐款/应付帐款会计科目。 结算将为付款重构会计科目。 如果对应收帐款/应付帐款主科目使用固定维度，这将成为问题。

为了重构会计科目，将按照付款日记帐中的定义从过帐模板检索应收帐款/应付帐款主科目，从付款的供应商交易记录记录检索财务维度。 付款日记帐中默认不采用固定维度，而是在过帐流程的最后一步将其应用于主科目。 结果，供应商交易记录中可能不包含固定维度值，除非其默认来自另一个源，如供应商。 重构的科目将不包含固定维度。 结算处理将确定必须创建调整条目，因为使用固定维度值和重构的付款科目过帐的发票中不包含调整条目。  在结算继续过帐调整条目时，过帐的最后一步是应用固定维度。 通过将固定维度添加到调整条目，就将其通过借项和贷项过帐到同一个会计科目。 结算不能回滚会计条目。

若要避免同一个会计科目中有更多会计条目、借项和贷项，应考虑采用下面的解决方案，具体取决于您的业务需求。 

-   组织通常使用固定维度为不需要的固定维度填零。 应收帐款/应付帐款之类资产负债表科目经常出现这种情况。 不能将科目结构用于跟踪典型填零的财务维度。  可移除资产负债表科目的财务维度，以杜绝对使用固定维度的需要。
-   如果组织的应收帐款/应付帐款主科目中需要固定维度，请想办法在付款中默认使用固定维度，以便将固定维度值存储到付款的供应商交易记录中。 这样系统就可以重构应收帐款/应付帐款主科目，以便包含固定维度值。 可在付款日记帐的供应商或日记帐名称中将固定维度值定义为默认值。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
