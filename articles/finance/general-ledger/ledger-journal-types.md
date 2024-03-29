---
title: 分类帐日记帐类型
description: 本文介绍可以为财务日记帐设置的日记帐类型。
author: kweekley
ms.date: 10/10/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup
audience: Application User
ms.reviewer: kfend
ms.custom: 15631
ms.assetid: 81613b31-bc3c-43a0-8474-e01c9a482c40
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 883c54b84ed31384a28c31c8b814c75d340d020e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901304"
---
# <a name="ledger-journal-types"></a>分类帐日记帐类型

[!include [banner](../includes/banner.md)]

本文介绍可以为财务日记帐设置的日记帐类型。 使用 **日记帐名称** 页可以设置可在 Dynamics 365 Finance 中全程使用的日记帐。

| 日记帐类型                      | 目的                       | 在此页面上输入交易记录                                |
|-----------------------------------|-------------------------------|----------------------------------------------------------------|
| 分配                        | 在分配日志中创建分配交易记录。 您必须先在 **分类帐分配规则** 页上创建分配规则，然后才能创建分配日记帐。      | 处理分配请求             |
| 审核                          | 将已审核的供应商发票过帐到适当会计科目。  | 发票审核日记帐                                       |
| 银行支票冲销               | 冲销已过帐支票。 要使用此日记帐类型，请选择 **现金和银行管理参数** 页上的 **对付款冲销使用审核过程** 选项。   | 支票冲销、付款冲销                   |
| 银行存款单取消    | 取消存款单。 要使用此日记帐类型，请选择 **现金和银行管理参数** 页上的 **对存款单付款取消使用审核过程** 选项。   | 存款单付款取消            |
| 预算                            | 处理预算拨款。 要使用此日记帐类型，请选择 **总帐参数** 页上的 **启用预算拨款**。 预算日记帐分录将包含基于在 **过帐定义** 页上定义的会计科目的信息。                                                        |                                                                |
| 客户接收汇票  | 创建汇票的客户接受交易记录。             | 划拨汇票日记帐、重新签发汇票日记帐 |
| 客户银行汇款          | 创建可发送到您的组织的银行的汇票汇款文件。 要使用此日记帐类型，请清除 **应收** 帐 **款参数** 页上的 **自动结算** 选项。            | 汇款                                                     |
| 客户签发汇票    | 创建客户签发汇票交易记录。 要使用此日记帐类型，请清除 **付款方式 - 客户** 页上的 **过帐发票时，自动创建和过帐借支日记帐** 选项。   | 划拨汇票日记帐                                  |
| 客户 - 付款                  | 创建客户付款交易记录。                             | 付款日记帐             |
| 客户拒付汇票 | 创建客户拒付汇票交易记录。                    | 拒付汇票日记帐                               |
| 客户重新签发汇票  | 创建客户重新签发汇票交易记录。                     | 重新签发汇票日记帐                                |
| 客户结算汇票  | 创建客户结算汇票交易记录。                       | 结算汇票日记帐                                |
| 日常                             | 在普通记帐日志中创建每日交易记录。                          | 普通日记帐                                                |
| 清除                       | 在清除日志中创建清除交易记录中。 要使用此日记帐类型，请选择 **法人** 页上的 **用于财务清除过程** 和 **用于财务合并过程** 选项。 您必须先在 **分类帐清除规则** 页上创建分类帐清除规则，然后才能使用此日记帐类型。 | 清除                                                    |
| 固定资产预算                | 创建固定资产预算登记分录。                                                                                                                                                                                                                                                                                                                 | 固定资产预算                                             |
| 发票登记簿                  | 登记有关供应商发票的基本信息。                                                                                                                                                                                                                                                                                                           | 发票登记簿                                               |
| 工资付款              | 基于工资单付款报表发放款项。 无法在此日记帐中手动输入交易记录。 必须先生成付款报表，然后再提交。                                                                                                                                                              |                                                                |
| 定期                          | 为期间日志创建期间交易记录。                                                                                                                                                                                                                                                                                                      | 期间日记帐                                              |
| 固定资产记帐                 | 过帐固定资产交易记录。                                                                                                                                                                                                                                                                                                                              | 固定资产                                                   |
| 项目 - 支出                | 创建项目支出交易记录。                                                                                                                                                                                                                                                                                                                        | Expense                                                        |
| 申报币种调整     | 使用申报币种为会计科目中的余额创建调整。               | 申报币种调整日记帐                         |
| 汇总交易记录            | 创建统计交易记录。                                                                                                                                                                                                                                                                                                                            |                                                                |
| 供应商银行汇款            | 创建可发送到您的组织的银行的本票汇款文件。                                                                                                                                                                                                                                                                      | 汇款日记帐                                             |
| 供应商 - 付款               | 创建供应商付款交易记录。                                                                                                                                                                                                                                                                                                                    | 付款日记帐                                                |
| 供应商签发本票       | 签发供应商本票作为付款方式。 要使用此日记帐类型，请清除 **付款方式 - 供应商** 页上的 **过帐发票时，自动创建和过帐借支日记帐** 选项。                                                                                                                                          | 签发本票日记帐                                   |
| 不包括过帐的供应商发票池 | 创建尚未过帐到临时到达帐户的供应商发票交易记录。                                                                                                                                                                                                                                                             | 供应商发票池(不包括过帐)详细信息                  |
| 供应商发票池               | 创建供应商发票池交易记录。                                                                                                                                                                                                                                                                                                                    |                                                                |
| 供应商发票记录          | 过帐日记帐中的供应商发票                                                                                                                                                                                                                                                                                                                 | 发票日记帐                                                |
| 供应商重新签发本票     | 重新签发以前已由您组织的银行承兑的本票。                                                                                                                                                                                                                                                                      | 重新签发本票日记帐                                 |
| 供应商结算本票     | 创建供应商结算本票交易记录。                                                                                                                                                                                                                                                                                                          | 结算本票日记帐                                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
