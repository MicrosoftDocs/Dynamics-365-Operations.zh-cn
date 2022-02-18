---
title: 创建费用代码
description: 本主题介绍如何为应付帐款和应收帐款配置费用代码。
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MarkupTable
audience: Application User
ms.reviewer: roschlom
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 034be190890a67fd0921d40fffdc704b9d6d5df7
ms.sourcegitcommit: 5bfd6511d710deb539b4030eb0e9c48d25513595
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/19/2022
ms.locfileid: "8014033"
---
# <a name="create-charges-codes"></a>创建费用代码

本主题介绍如何为应付帐款和应收帐款配置费用代码。 如果您的组织要求跟踪销售金额或采购金额，以及销售订单或采购订单上的行物料，则可以为此目的使用费用代码。 例如，您支付采购订单上的运费和保险费；并且，这些金额在采购订单上单独详细列出。 在此情况下，您可以指定这些金额是已过帐到支出帐户，还是已添加到物料成本。

## <a name="set-up-charges-codes-for-accounts-receivable"></a>设置应收帐款的费用代码

若要为应收帐款创建费用代码，请按照以下步骤操作。

1. 转到 **应收帐款** &gt; **费用设置** &gt; **费用代码**。
2. 选择 **新建**。
3. 在 **费用代码** 字段，输入费用的代码。
3. 在 **描述** 字段中，输入费用的描述。
4. 可选：在 **物料销售税组** 字段中，选择一个销售税组。
5. 在 **过帐** 快速选项卡中，指定应该如何自动借记和贷记费用。
6. 如果选择了 **分类帐科目** 作为借方类型或贷方类型，请在 **过帐** 字段中指定过帐类型，在 **科目** 字段中指定主要科目。

### <a name="example"></a>示例

您的客户支付该费用。 因此，费用会添加到销售订单合计。 您设置以下过帐信息：

- 在 **借记** 部分内的 **类型** 字段中，选择 **客户/供应商** 以将发票费用添加至客户帐户。
- 在 **贷方** 部分内的 **类型** 字段中，选择 **分类帐科目**。 然后，在 **科目** 字段中，从发票费用选择收入的主科目。

> [!NOTE]
> 如果所选代码的借方类型或贷方类型是 **分类帐科目** 或 **物料**，则您可以为费用交易输入不同的货币。

可以使用为客户分配的语言来打印费用文本。 要使用其他语言为费用代码指定文本，请选择 **翻译**。

## <a name="set-up-charges-codes-for-accounts-payable"></a>设置应付帐款的费用代码

若要为应付帐款创建费用代码，请按照以下步骤操作。

1. 按以下步骤之一：

    - 转到 **应付帐款** &gt; **费用设置** &gt; **费用代码**。
    - 转到 **采购** &gt; **设置** &gt; **费用** &gt; **费用代码**。

2. 选择 **新建**。
3. 在 **费用代码** 字段，输入费用的代码。
3. 在 **描述** 字段中，输入费用的描述。
4. 可选：在 **物料销售税组** 字段中，选择一个销售税组。
5. 可选：在 **最大金额** 字段中 – 输入费用代码允许的最大金额。

    此字段用于验证供应商发票的费用。 若要启用费用验证，请在 **应付帐款参数** 页面的 **发票验证** 选项卡上选中 **启用发票匹配验证** 复选框。

    > [!IMPORTANT]
    > 要验证发票费用，您还必须创建基于特定供应商发票策略费用的策略规则类型的实例。

6. 在 **过帐** 快速选项卡中，指定应该如何自动借记和贷记费用。
7. 如果选择了 **分类帐科目** 作为借方类型或贷方类型，请在 **借方过帐** 和 **贷方过帐** 字段中指定过帐类型，在 **借方科目** 和 **贷方科目** 字段中指定主科目。
8. 若要允许为在相应的采购订单头或行上包含费用的发票比较费用值，请选中 **比较销售订单和发票值** 复选框。

### <a name="example"></a>示例

作为采购订单或供应商发票的合计的一部分，您可以记录费用作为支出过帐。 按照以下步骤设置过帐信息。 

- 在 **贷方** 部分内的 **类型** 字段中，选择 **客户/供应商** 以将发票费用添加至供应商帐户。
- 在 **借方** 部分内的 **类型** 字段中，选择 **分类帐科目**。 然后，在 **科目** 字段中，从发票费用选择费用的主科目。

按照这些步骤设置过帐信息，以便将单位费用添加到物料成本中。

- 在 **贷方** 部分内的 **类型** 字段中，选择 **客户/供应商** 以将发票费用添加至供应商帐户。
- 在 **借方** 部分内的 **类型** 字段中，选择 **物料** 以将费用添加到物料成本。

> [!NOTE]
> 您想要使用的货币可能不同于采购订单或发票上指定的货币。 如果所选费用代码的借方类型或贷方类型为 **分类帐科目** 或 **物料**，则可以输入不同的货币。

可以使用为客户分配的语言来打印费用文本。 要使用其他语言为费用代码指定文本，请选择 **翻译**。