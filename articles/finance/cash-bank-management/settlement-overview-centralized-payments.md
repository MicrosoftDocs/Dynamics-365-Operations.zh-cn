---
title: 集中付款的结算概览
description: 此主题介绍 Microsoft Dynamics 365 Finance 的集中付款的结算。
author: abruer
manager: AnnBe
ms.date: 08/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 222414
ms.assetid: 610f6858-0f37-4d0f-8c68-bab5a971ef4a
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ea661441c6c810d144d423b054c1bef058cdd9d6
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188226"
---
# <a name="settlement-overview-for-centralized-payments"></a>集中付款的结算概览

[!include [banner](../includes/banner.md)]

包括多个法人的组织可以使用处理所有付款的法人创建和管理付款。 这样，就无需在多个法人分别输入相同的交易记录，通过优化付款方案流程、结算流程、未结交易记录编辑和针对集中式付款的已结算交易记录编辑来节约时间。 

当在一个法人中输入客户或供应商付款，并且用在其他法人中输入的发票结算该付款时，将自动为每个法人生成适用的结算、应付和应收交易记录。 将为该交易记录中每个发票和付款组合创建一个结算记录。 每一个结算记录都分配了一个新的凭证号，它基于在针对客户的**应收账款参数**页和针对供应商的**应付账款参数**页上指定的付款凭证编号规则系列。 

如果为现金折扣、外币汇率重估、尾差、超额付款或支付不足生成附加的结算记录，则向它们分配更晚的付款或发票交易记录日期。 如果结算在过帐付款后发生，则结算记录将使用在**结算未结交易记录**页指定的结算过帐日期。

## <a name="posting-types-transaction-types-and-default-descriptions"></a>过帐类型、交易记录类型和默认描述

内部公司结算凭证交易记录使用内部公司结算过帐类型、内部公司客户结算和内部公司供应商结算交易记录类型。 您可以在**默认描述**页设置与该交易记录类型有关的信息。 

以下交易记录类型可供在单个公司和跨公司结算中使用：

-   结算
-   现金折扣
-   外币重估（包括已实现和未实现的外币重估）
-   尾差
-   超额支付/支付不足

您还可为内部公司结算凭证定义默认描述。

## <a name="currency-exchange-gains-or-losses"></a>币种汇兑损益

用于客户或供应商交易记录的汇率与交易记录一起存储。 币种转换的已有损益过帐到发票法人或付款法人，具体取决于在针对付款法人的**内部公司会计**页的**过帐币种转换损益**字段中选择的选项。 以下示例将使用这些币种：
-   付款记帐币种：EUR
-   发票记帐币种：USD
-   付款交易记录币种：DKK
-   发票交易记录币种：CAD

### <a name="currency-calculations"></a>币种计算

在用在一个法人中输入的付款结算输入到其他法人中的发票时，该付款的交易记录币种 (DKK) 将用以下三个步骤转换：
1.  使用来自付款法人的汇率，转换为付款的记帐币种 (EUR)。
2.  转换为发票的记帐币种 (USD)。
3.  使用来自发票法人的汇率，转换为发票的交易记录币种 (CAD)。

该转换过程使用截至付款日期的汇率。 如果采用发票交易记录币种 (CAD) 的最终付款金额等于发票金额 (CAD)，则该发票将被视为完全支付。 

在未输入付款金额的付款日记帐中打开**结算未结交易记录**页时，基于在**结算未结交易记录**页上选择的要结算的发票计算结算金额。 要结算的金额将通过以下三个步骤转换：
1.  使用付款日期的来自发票法人的汇率，转换为发票的记帐币种 (USD)。
2.  使用付款日期的来自发票法人的汇率，转换为付款的记帐币种 (EUR)。
3.  转换为付款的交易记录币种 (DKK)。

在您关闭**结算未结交易记录**页时，最终的付款金额将转移到付款日志帐行。

### <a name="posting-for-gain-or-loss-because-of-different-accounting-currencies"></a>损益的过帐由于不同的分期付款币种

如果存在币种转换损益，损益将过帐到为付款法人的**内部公司会计**页的**过帐币种转换损益**字段指定的法人。 损益金额换算为损益金额过帐法人的分期付款币种，使用为该法人定义的汇率。

## <a name="cash-discounts"></a>现金折扣

在内部公司结算流程中生成的现金折扣过帐到发票法人或付款法人，具体取决于为付款法人的**内部公司会计**页的**过帐现金折扣**字段选择的选项。 在发票的法人中生成相应的结算交易记录。

## <a name="overpayments-and-underpayments"></a>超额支付和支付不足

超额支付、支付不足和尾差容差基于超额支付的付款法人以及支付不足的发票法人确定。 使用的过帐科目取决于针对客户的**应收账款参数**页的**现金折扣管理**字段和针对供应商的**应付账款参数**页的**现金折扣管理**字段中的设置。

-   如果现金折扣管理设置为“特定”，或者如果设置为“非特定”，且在超额支付的不同法人中过帐适用的现金折扣，则使用“客户现金折扣”、“供应商现金折扣”或“以记帐币种表示的尾差”的自动科目。 您可以在**自动交易记录帐户**页上指定这些科目。
-   如果现金折扣管理设置为“非特定”，并且在与超额支付相同的法人中（付款法人和发票的法人相同）过帐现金折扣，则调整现金折扣帐户。 例如，如果金额为 100.00 的发票（且具有 3.00 的可用现金折扣）使用金额为 98.00 的付款结算，则为 1.00 调整现金折扣帐户。 折扣净额是 2.00。
-   如果现金折扣管理设置为“非特定”，在与超额支付相同的法人中过帐现金折扣，并且用具有现金折扣的多张发票结算超额支付或支付不足，则调整最后一张发票的现金折扣帐户。

如果现金折扣管理选择为“非特定”，则不指定的付款结算规则只适用于以下情况中：
-   存在超额支付。
-   使用具有现金折扣的一张或多张发票结算超额支付。
-   现金折扣在与该超额支付相同的法人中过帐。

在所有其他情况下，超额支付或支付不足过帐到“客户现金折扣”、“供应商现金折扣”或“以记帐币种表示的尾差”的自动科目。

## <a name="sales-tax"></a>增值税
增值税交易记录保留在最初过帐它们的法人中。 

如果已经为某一预付款过帐了增值税，则跨公司结算将冲销预付款法人中针对预付款的增值税。 在税发票的法人保留在发票的法人中。

## <a name="financial-dimensions"></a>财务维度
对于客户付款，付款法人中的应收和应付交易记录使用根据要结算的付款为应收账款汇总科目指定的财务维度。 在发票的法人中，应收和应付交易记录使用根据要结算的发票为应收账款汇总科目指定的财务维度。 

对于供应商付款，付款法人中的应收和应付交易记录使用根据要结算的付款为应付账款汇总科目指定的财务维度。 在发票的法人中，应收和应付交易记录使用根据要结算的发票为应付账款汇总科目指定的财务维度。

## <a name="withholding-tax"></a>预缴税金
与发票关联的供应商帐户用于确定是否应计算预缴税金。 如果预缴税金如果适用，则在与发票关联的法人中计算。 如果使用不同币种法人，则使用来自与发票关联的法人的汇率。