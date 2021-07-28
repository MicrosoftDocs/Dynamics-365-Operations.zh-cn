---
title: SEPA 贷方转帐概览
description: 此主题提供有关 ISO 20022 贷方转帐（包括单一欧元支付区 (SEPA) 贷方转帐和针对供应商的其他任何电子付款）的一般信息。 SEPA 贷方转帐是从一个公司或个人到另一个公司或个人的一种特定类型的付款（用欧元）。 本主题还讨论如何设置和传输贷方转帐付款文件。
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendInvoice, LedgerJournalTransVendPaym, VendPaymMode
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "11124"
- intro-internal
ms.assetid: 36b0f870-16d4-4bbb-8da5-e747e69b970d
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 03732ecd5a0cd59d15fa1f9f0691571bd0a19606
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/06/2021
ms.locfileid: "6346442"
---
# <a name="sepa-credit-transfer-overview"></a>SEPA 贷方转帐概览

[!include [banner](../includes/banner.md)]

此主题提供有关 ISO 20022 贷方转帐（包括单一欧元支付区 (SEPA) 贷方转帐和针对供应商的其他任何电子付款）的一般信息。 SEPA 贷方转帐是从一个公司或个人到另一个公司或个人的一种特定类型的付款（用欧元）。 本主题还讨论如何设置和传输贷方转帐付款文件。

## <a name="what-is-a-credit-transfer-message"></a>贷方转帐消息是什么？
贷方转帐消息是发起方（您公司）为了将资金从自己的帐户转移到贷方而发出的请求。 贷方转帐消息有大量国家/地区特定和银行特定的实施。 其中一些在一个国家/地区内使用，一些则成为了标准。 一个享有盛誉的全球标准为 ISO 20022 及其初始消息，如“贷方转帐”。 下图显示选定贷方转帐消息的关系和范围。 
![贷方转帐。](./media/credit-transfer.jpg) 贷方转帐消息 

## <a name="what-are-iso-20022-and-sepa-payments"></a>ISO 20022 和 SEPA 付款是什么？
单一欧元支付区 (SEPA) 由欧盟执委会设置，并指示所有电子付款均被视为国内行为，不论个人、企业或者组织和银行所在的国家/地区。 国内付款和跨境付款之间不存在差异。 SEPA 包含 28 个欧盟 (EU) 成员国，以及爱尔兰、列支敦斯登、挪威、瑞士、摩纳哥和圣马力诺。 SEPA 帮助在欧洲经济区域 (EEA) 中形成付款交易记录的单一市场。 最终，SEPA 会减少银行、企业和个人必须使用的支付形式数量。 欧盟执委会通过付款服务规定 (PSD) 建立 SEPA 付款的法律基础。 欧元支付委员会 (EPC) 通过以下活动支持 SEPA:

-   它通过使用 ISO 20022 通用财务行业消息模式 XML 格式，规定 SEPA 电子付款的标准。
-   它确定有关处理欧元付款的规则和基准。

EPC（包括欧洲银行）开发 SEPA 付款设备的商业和技术框架。 使用三种类型的 SEPA 付款：

-   贷方转帐
-   直接借记
-   卡

## <a name="what-is-a-sepa-credit-transfer"></a>SEPA 贷方转帐是什么？
SEPA 贷方转帐是从一个公司或个人付款到另一个公司或个人。 付款必须按欧元，并且必须包括国际银行帐号 (IBAN) 和两个当事方的银行标识符代码 (BIC)。 （BIC 也称为国际银行金融电信协会 \[SWIFT\] 代码。）此外，交易记录必须在两个当事方之间共享。 当事方之间的贷方转帐应使用符合 ISO 20022 付款处理标准的 XML 格式和由 EPC 指定的 XML。

## <a name="how-is-a-credit-transfer-implemented"></a>贷方转帐如何实施？
欧洲国家/地区的贷方转帐付款格式是使用 Microsoft Dynamics 365 Finance 中的电子申报 (ER) 和付款方式功能来实施的。 其他地区使用的一些贷方转帐格式仍在使用传统的付款框架。 在其他许多格式中，有十二种 ISO 20022 贷方转帐文件格式可用。 这些导出格式符合 SEPA ISO 20022 XML 标准。 它们用于按照 EPC 发布的 SEPA Credit Transfer Scheme Rulebook 8.2 版中的规定，为其使用国/地区和欧元付款生成非欧元付款转帐。 在您可以实施贷方转帐前，必须与您的银行联系，以获取加载电子银行文件所需的软件。 您将使用该软件将包含付款订单的 XML 文件转移到您的银行。

## <a name="what-credit-transfer-formats-are-currently-supported"></a>目前支持哪些贷方转帐格式？
应始终转至 Microsoft Dynamics Lifecycle services (LCS) 中的共享资产库，并查看资产类型为 **GER 配置** 的可用文件的最新列表。 下一部分“必须执行哪些设置？”提供一个主题的链接，该主题说明如何创建 LCS 存储库以检查可用配置和导入所选配置。

## <a name="what-do-i-have-to-set-up"></a>我必须设置什么？
-   在您可以创建贷方转帐文件前，必须导入至少一个有效的贷方转帐配置到您的 ER 配置。 有关说明，请参阅[从 Lifecycle Services 下载电子申报配置](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)。
-   在配置应付帐款付款方式时，请选中 **一般电子申报** 复选框，并选择相应的贷方转帐格式（如 **ISO 20022 贷方转帐 (AT)**）作为导出格式配置。
-   还必须设置法人和银行帐户信息。
-   需要银行帐号、IBAN，有时还需要 SWIFT 代码 (BIC) 或其他 ID，才能创建有效的贷方转帐付款。 必须为供应商银行帐户和请求转帐的银行帐户设置这些信息。
-   可能需要更多信息，如贷方转帐消息中涉及的各方的增值税 (VAT) 号。 如果请求此信息，则必须为供应商和法人设置。
-   某些应付帐款付款方式（大多数为基于 ISO 20022 的付款方式）可能需要为 **付款格式代码集** 执行更多设置，如 **服务类型** = **SLEV**。 这些代码在处理付款期间用作付款交易记录额外的标记。 可在两处设置付款代码的默认值（如 **类别目的**、**费用责任人**、**本地仪器** 和 **服务等级**）。 第一处为 **应付帐款付款日记帐抬头**，第二处为 **应付帐款付款方式**。 创建付款日记帐行之后，将把在付款日记帐抬头中设置的付款代码值转移到日记帐行，如果未设置该值，则使用付款方式中的值。

## <a name="what-parameters-are-available-for-generating-credit-transfer-payments"></a>哪些参数可用于生成贷方转帐付款？
具体参数列表取决于贷方转帐格式。 下表显示了在供应商付款日记帐中为德国生成 ISO 20022 贷方转帐付款文件时可以使用的参数。 通过使用 **在后台运行** 选项卡上的选项，您可以在批处理模式下运行付款生成。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>字段</th>
<th>说明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>批预定</td>
<td>选中此复选框可在 XML 文件中包括批次预订标记。</td>
</tr>
<tr class="even">
<td>处理日期</td>
<td>输入银行应处理付款的日期。</td>
</tr>
<tr class="odd">
<td>格式</td>
<td>根据您的国家/地区或银行的要求，选择汇款信息的格式：
<ul>
<li><strong>Strd</strong> – 选择此选项可在针对一个发票结算一个付款行时使用已结构化的格式。 此选项不可用于法国、德国或荷兰的特定于国家/地区的导出格式。</li>
<li><strong>Ustrd</strong> – 选择此选项可在针对多个发票结算一个付款时使用未结构化的格式。 已结算发票的发票编号连接到一起，并且用作汇款信息。 根据 ISO 20022 指南，非结构化汇款信息不能超过 140 个字符。</li>
</ul></td>
</tr>
<tr class="even">
<td>发票数</td>
<td>输入<strong>付款通知</strong>报表从中打印的发票数量。</td>
</tr>
<tr class="odd">
<td>序列号</td>
<td>输入序列号以标识文件。 序列号显示在<strong>出席单</strong>报表上。</td>
</tr>
<tr class="even">
<td>打印出席单</td>
<td>选中此复选框可打印<strong>出席单</strong>报表。</td>
</tr>
<tr class="odd">
<td>打印控制报表</td>
<td>选中此复选框可打印包含付款信息的报表。</td>
</tr>
<tr class="even">
<td>打印随函</td>
<td>选中此复选框可打印<strong>付款通知</strong>报表。</td>
</tr>
</tbody>
</table>

## <a name="what-are-ibans-and-bics"></a>IBAN 和 BIC 是什么？
国际银行帐号 (IBAN) 和银行标识符代码 (BIC) 用于标识在全球大量国家/地区的任何帐户。 其中包括 34 个 SEPA 国家/地区。 在 **SWIFT 代码** 字段中输入 BIC，在 **IBAN** 字段中输入 IBAN。 对于贷方的银行帐户和客户的银行帐户，这些字段位于 **银行帐户** 页上的 **银行帐户** 选项卡的 **附加标识** 快速选项卡。 不再将 BIC 用于 SEPA 付款。

## <a name="how-do-i-transmit-a-payment-file-to-the-bank"></a>如何将付款文件发送到银行？
在您生成付款时，将生成付款文件，并且，系统会请求您从 Web 浏览器中将其保存到任何可用的位置。 下一步是将该 XML 文件发送到您的银行。 此流程根据银行的不同而变。 按照您的银行的说明将文件提交给银行以进行处理。





[!INCLUDE[footer-include](../../includes/footer-banner.md)]