---
title: 自动交易记录帐户
description: 本文说明如何使用自动交易帐户通过 Microsoft Dynamics 365 进行过帐，并提供自动交易关键帐户的示例。
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerSystemAccounts
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74e72840fea1f5d89c908b00e2cf572bce6befbe
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880750"
---
# <a name="accounts-for-automatic-transactions"></a>自动交易记录帐户

**自动交易科目** 页面（**总帐 &gt; 过帐设置 &gt; 自动交易科目**）用于定义用于系统中的每种过账类型的默认主科目。 虽然大多数过帐类型可在特定于模块或特定功能的页面上配置，但某些过帐类型只能在 **自动交易科目** 页上配置。

例如，您可以在 **客户过帐模板** 页面上的 **摘要** 字段中指定用于 **客户余额** 过帐类型的主科目，并对每个客户模板使用不同的主科目。 这样，您可以更精细地控制过帐。 另一方面，您只能在 **自动交易科目** 页面上指定容错科目。

在新法人中打开 **自动交易科目** 页面时，科目列表将为空。 您可以通过选择 **创建默认类型** 按钮来添加页面上应配置的最常见过帐类型。 然后，对于每个行，您都可以在 **主科目** 字段中选择主科目。 如果对过帐类型将 **主科目** 字段留空，并且您尚未在特定于模块或特定于功能的页面上配置主科目，则在过帐使用此过帐类型的交易时，您将收到错误消息。 通常，消息将为“找不到\[过帐类型\]的科目”。

## <a name="default-posting-types"></a>默认过帐类型

下表显示了在 **自动交易科目** 页面上选择 **创建默认类型** 时创建的默认过帐类型的示例。 它显示了示例主科目和描述。 “借方/贷方？” 列指示交易通常是过帐借方还是贷方。 在某些情况下，交易可以过帐借方或贷方。 “结算帐户”列指示过帐类型是否为结算帐户。 如果过收类型是结算帐户，则在过帐以后的交易记录时，将自动冲销此帐户中过帐的金额。

| 过帐类型 | 主帐户示例 | 主帐户名称示例 | 帐户类型 | 借方/贷方？ | 结算帐户 | Description |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| 以申报币种表示的尾差 | 618160 | 杂项费用 | 支出 | 两者都有 | 否 | 将外币交易金额转换为申报币种过程中出现尾差时，使用此过帐类型。 |
| 以记帐币种表示的尾差 | 618160 | 杂项费用 | 支出 | 两者都有 | 否 | 将外币交易金额转换为记帐币种过程中出现尾差时，使用此过帐类型。 |
| 容错帐户 | 999999 | 容错科目 | 支出 | 两者都有 | 否 | 系统中发生错误时使用此过帐类型。 应在每个期间验证此科目，并且应解决任何错误。 |
| 年结 | 300160 | 留存收益 | 权益 | 两者都有 | 否 | 运行年终结算流程以将 **损益** 类型的帐户余额移到为年终结果选择的主科目中时，使用此过帐类型。 |
| 客户现金折扣 | 不适用 | 不适用 | 不适用 | 不适用 | 否 | 未使用在 **自动交易科目** 页面上定义的过帐类型。 在应收帐款中配置现金折扣时，需要主科目。|
| 供应商现金折扣 | 不适用 | 不适用 | 不适用 | 不适用 | 否 | 未使用在 **自动交易科目** 页面上定义的过帐类型。 在应付帐款中配置现金折扣时，需要主科目。 |

## <a name="additional-posting-types"></a>其他过帐类型

下表显示在计划使用相关功能时必须配置的其他过帐类型的示例。 对于这些过帐类型，其他模块中没有可用的过帐模板配置。 “借方/贷方？” 列指示交易通常是过帐借方还是贷方。 在某些情况下，交易可以过帐借方或贷方。 “结算帐户”列指示过帐类型是否为结算帐户。 如果过收类型是结算帐户，则在过帐以后的交易记录时，将自动冲销此帐户中过帐的金额。

| 过帐类型 | 主帐户示例 | 主帐户名称示例 | 帐户类型 | 借方/贷方？ | 结算帐户 | Description |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| 合并差额的余额帐户 | 801200 | 损益 - 重估 | 支出 | 两者都有 | 否 | 当您执行涉及货币重估的合并，并且重估期间出现尾差时，使用此过帐类型。 |
| 对应合并差异的损益帐户 | 801200 | 损益 - 重估 | 支出 | 两者都有 | 否 | 当您执行涉及货币重估的合并，并且重估期间出现尾差时，使用此过帐类型。 |
| 单位间 - 借方 | 133500 | 单位间应收帐款 | 资产 | 借记 | 否 | 当您在 **分类帐** 页面上选择平衡维度，并且该维度在已过帐的交易中不平衡时，使用此过帐类型。 |
| 单位间 - 借方 | 233500 | 单位间应付帐款 | 负债 | 信用 | 否 | 当您在 **分类帐** 页面上选择平衡维度，并且该维度在已过帐的交易中不平衡时，使用此过帐类型。 |
