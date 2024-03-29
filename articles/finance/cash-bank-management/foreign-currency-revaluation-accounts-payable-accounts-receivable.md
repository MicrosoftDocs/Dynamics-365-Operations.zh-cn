---
title: 应付帐款和应收帐款的货币重估
description: 本文提供有关您运行的以更新应收帐款和应付帐款的未结交易记录的值的外币重估流程的信息。
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustExchRateAdjustment, VendExchRateAdjustment
audience: Application User
ms.reviewer: kfend
ms.custom: 14211
ms.assetid: defb1ea5-1f3e-4859-87d8-3f9954d3f388
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 73f20323ff2eb36c89f4fb2848a056c2cb24ec30
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715713"
---
# <a name="currency-revaluation-for-accounts-payable-and-accounts-receivable"></a>应付帐款和应收帐款的货币重估

[!include [banner](../includes/banner.md)]

汇率波动导致采用外币的未结交易记录的理论价值（帐面价值）在不同时间发生变化。 本文提供有关您运行的以更新应收帐款和应付帐款的未结交易记录的值的外币重估流程的信息。 

采用外币的未结供应商交易记录的理论价值或帐面价值会由于汇率波动在不同时间发生变化。 若要更新应收帐款和应付帐款的未结交易记录的值，请运行外币重估流程。 应付帐款和应收帐款均可运行外币重估。 该流程将在指定日期使用新的汇率重估未结金额。 原始过帐金额与重估金额之间的差额将导致每个未结交易记录的或有损益。 应付帐款和应收帐款子分类帐然后更新以反映或有损益，且会计条目过帐到总帐。

## <a name="simulate-a-foreign-currency-revaluation"></a>模拟外币重估
在您重估未结客户交易记录的外币金额前，可以使用相同的日期和方法运行外币重估的模拟报表。 若要运行模拟报表，在 **外币重估** 页上，单击 **模拟** 按钮。 报表基于为模拟定义的参数提供或有损益金额的预览。

## <a name="process-a-foreign-currency-revaluation"></a>处理外币重估
使用 **定期任务** 下的 **外币重估** 重估未结交易记录。 您可以通过使用批处理实时运行此流程或计划此流程以进行运行。 在您定义重估流程的设置后，请确保验证是否要打印结果报表。 重估报表可以在流程完成后重新打印。 如果您生成外币重估报表，该报表将显示客户/供应商级别和币种级别的各个余额：

-   具有已重估的外币交易记录的客户或供应商的余额。 以下余额显示：
    -   外币显示的原始总计金额。
    -   截至之前重估，采用记帐币种的外币重估总计金额。
    -   截至当前重估，采用记帐币种的外币重估总计金额。
    -   之前重估与当前重估之间的差异。 其他或有损益的差异。
-   每个币种的总计或有损益。

每次运行外币重估时，都将保留记录。 从 **外币评估** 页的记录中，选择 **交易记录** 查看由于重估创建的交易记录的详细列表。 每个凭证交易记录表示已重估的未结交易记录。 如果未结交易记录重估多次，您将看到使用同一个凭证的两个记录。 一个记录将用于以前或有损益的冲销，其他记录用于新的或有损益。 若要运行重估流程，单击 **外币重估** 按钮。 为以下参数定义适当设置：

-   **方法** – 此方法用在所选外币重估作业中：
    -   **标准** – 将外币重估作业过帐，而不考虑结果是盈还是亏。
    -   **最小值** – 仅当结果为亏时过帐外币重估作业。
    -   **发票日期** – 外币重估作业使用交易记录的原始汇率，这一汇率的值将重估为其以记帐币种表示的原始值。 将取消任何先前外币重估的效果。
-   **考虑日期** – 找到所有在该日期具有未结（未结算）金额的交易记录的日期。 外币金额于考虑日期使用在 **币种汇率** 页中输入的汇率重估。 当在考虑日期运行外币金额时，该日期将成为调整的交易记录的最后外币重估日期。 如果您在考虑日期运行外币重估，而该考虑日期早于已调整的交易记录的最后外币重估日期，则定期作业将不调整在较早的考虑日期未结、但具有更晚最后外币重估日期的交易记录。
-   **比率对应日** – 确定用在外币重估的汇率的日期。
-   **使用的过帐模板来自** – 用于输入外币重估交易记录的会计条目的应收帐款或应付帐款的默认主科目的过帐模板：
    -   **过帐** – 使用客户交易记录的过帐模板。
    -   **选择** – 在 **过帐模板** 字段中输入过帐模板。
-   **过帐模板** – 如果在 **使用的过帐模板来自** 字段中选择 **选择**，您在此字段中输入的过帐模板将确定外币重估交易记录的过帐模板。
-   **财务维度** – 在外币重估交易记录的会计条目上过帐的财务维度。 财务维度未根据科目结构的规则进行验证。 过帐发票时所用的科目结构可能与重估完成时所用的规则不同。 重估流程中没有选择特定财务维度的选项，因此将跳过科目结构验证。  
    -   **无** – 不过帐财务维度。 如果您的科目结构中具有所需财务维度，重估流程仍然运行并创建没有财务维度的会计条目。 您首先将收到警告消息，以便您可以取消重估。
    -   **表** – 在外币重估交易记录上过帐的客户帐户或供应商帐户的财务维度。
    -   **过帐** – 在外币重估交易记录上过帐正在重估的交易记录的财务维度。 默认情况下，原始交易记录的 AR/AP 会计科目的财务维度将用于重估交易记录的 AR/AP 主科目，原始交易记录的费用/资产/收入会计科目的财务维度将用于重估交易记录的或有损益主科目。






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
