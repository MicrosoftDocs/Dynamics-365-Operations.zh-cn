---
title: "SEPA 贷方转帐概览"
description: "该 ISO 文章提供有关的一般信息，包括银行转帐单 20022 欧元支付区 (SEPA) 银行转帐和任何其他电子付款供应商的。 SEPA 是银行转帐付款的特定类型从一个在公司或个体的欧元到其他公司或个体。 主题还说明如何设置和传输银行转帐付款文件。"
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendInvoice, LedgerJournalTransVendPaym, VendPaymMode
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 11124
ms.assetid: 36b0f870-16d4-4bbb-8da5-e747e69b970d
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 848df5e3898f37284d7746c59bff8b38d35ac883
ms.lasthandoff: 03/31/2017


---

# <a name="sepa-credit-transfer-overview"></a>SEPA 贷方转帐概览

该 ISO 文章提供有关的一般信息，包括银行转帐单 20022 欧元支付区 (SEPA) 银行转帐和任何其他电子付款供应商的。 SEPA 是银行转帐付款的特定类型从一个在公司或个体的欧元到其他公司或个体。 主题还说明如何设置和传输银行转帐付款文件。

## <a name="what-is-a-credit-transfer-message"></a>什么是银行转帐消息？
银行转帐消息是起始选方的请求 (您的公司从其自己) 发送到的帐户的资金债权人到移动。 有银行转帐消息的一些特定于国家/地区的银行和特定实施。 某些某一国家/地区内使用，并且是某些类型的标准。 一源远流长是全局的 ISO 标准 20022 和其启动消息，如银行转帐。 下图查看关系和覆盖范围选择的银行转帐的消息。 
![贷方 tansfer](./media/credit-transfer.jpg) 银行转帐\[消息/caption\] 

## <a name="what-are-iso-20022-and-sepa-payments"></a>什么是付款、20022 和 SEPA?
单一欧元支付区 (SEPA) 由欧盟执委会设置，并指示所有电子付款均被视为国内行为，不论个人、企业或者组织和银行所在的国家/地区。 不在国家/地区和付款/入境付款之间的差异。 SEPA 包含欧盟 (EU) 的 (EU) 个，并且各成员国爱尔兰、挪威和瑞士摩纳哥、、圣马力诺。 SEPA 帮助在欧洲经济区域 (EEA) 中形成付款交易记录的单一市场。 最终，SEPA 会减少银行、企业和个人必须使用的支付形式数量。 欧盟执委会通过付款服务规定 (PSD) 建立 SEPA 付款的法律基础。 欧元支付委员会 (EPC) 通过以下活动支持 SEPA:

-   它通过使用 ISO 20022 通用财务行业消息模式 XML 格式，规定 SEPA 电子付款的标准。
-   它确定有关处理欧元付款的规则和基准。

EPC（包括欧洲银行）开发 SEPA 付款设备的商业和技术框架。 使用三种类型的 SEPA 付款：

-   贷方转帐
-   直接借记
-   卡

## <a name="what-is-a-sepa-credit-transfer"></a>SEPA 贷方转帐是什么？
SEPA 贷方转帐是从一个公司或个人付款到另一个公司或个人。 付款必须按欧元，并且必须包括国际银行帐号 (IBAN) 和两个当事方的银行标识符代码 (BIC)。 也称作 BIC (是环球银行金融电信协会 \[SWIFT\] 代码)。此外，必须共享成本交易两个当事方之间。 当事方之间的贷方转帐应使用符合 ISO 20022 付款处理标准的 XML 格式和由 EPC 指定的 XML。

## <a name="how-is-a-credit-transfer-implemented"></a>银行转帐如何实施？
欧洲国家/地区的银行转帐付款格式实施通过电子国家/地区报告的 (ER) 和付款方式函数 Dynamics 中 (ER) 操作。 在其他区域仍的某些银行转帐付款格式使用旧的框架。 {{在：Among}}许多其他格式中，只有将余数 ISO 可用 20022 的银行转帐文件格式。 以下导出格式符合 20022 XML SEPA ISO 标准。 它们用于生成这些 SEPA 在银行转帐架构规则说明指南版本 8.2 中指定使用和付款以欧元 EPC 的国家/地区的非欧元付款转帐。 在您可以实施银行转帐之前，必须与您的银行联系获取要求以电子银行软件上载的文件。 您将使用该软件付款单转移包含到您的银行的 XML 文件。

## <a name="what-credit-transfer-formats-are-currently-supported-in-dynamics-365-for-operations"></a>在转帐银行格式当前支持工序中 Dynamics 365?
您始终应以 Microsoft Dynamics 的生命期服务共享 (LCS) 资产的库和查看其中有一个资产类型。可用文件的最新的列表热镇** **配置。 下一部分，“我必须设置哪些方面？”提供一个链接，指向介绍如何创建知识库 LCS 查看可用配置并导入所选配置的主题。

## <a name="what-do-i-have-to-set-up"></a>我必须设置什么？
-   在您可以创建银行转帐文件导入之前，必须至少有效银行转帐配置到您的 ER 配置。 有关说明，请参阅从 Lifecycle Services [] (https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs) 的下载电子申报 Configuration 国家/地区。
-   在配置应付帐款付款方式时，请选择报告** **一般电子复选框，并选择适当的银行转帐格式 (例如银行转帐**，ISO 20022 (AT **))。配置导出格式。
-   还必须设置在 Dynamics 365 的法人和银行账户工序的信息。
-   银行和帐号、IBANs 有时候 SWIFT 代码 (BICs) 其他要求或 ID 为了创建有效的银行转帐付款。 因此，您必须为它们用于为供应商银行帐账户和银行账户为请求进行传输的组织的。
-   附加信息可能是必需的，例如增值税 (VAT) 编号。在银行转帐消息参考的当事方。 将申请时设置此信息，必须为供应商和为法人。
-   某些应付帐款付款方式，主要 ISO 20022 基于付款方式，可能需要附加的设置。**付款格式代码字码集** **，例如服务类型 = ** ** = SLEV **。 在付款处理期间，这些代码将根据其他标记的付款交易记录。 默认付款值代码，就像**类别目的**费用，**持票人** **，当地**仪器，然后** **服务级别都可按以下两位置设置。 第一位是**应付帐款付款日志标题**，第二是** **应付帐款付款的方法。 进行付款日志行创建付款，在付款日志标题设置的代码值转移到日志行，如果未设置，付款方式使用的值。

## <a name="what-parameters-are-available-for-generating-credit-transfer-payments"></a>哪些参数为银行转帐付款可生成？
特定参数的列表取决于格式银行转帐。 下表显示可用的参数，当您生成一 20022、德国的银行转帐付款文件供应商付款日志)。 通过使用上提供的选项**请在后台运行**选项卡上，您可以以批处理方式运行生成付款。

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
<li><strong>Strd</strong>，在一付款行已结算一发票时，–选择此选项将使用构建的格式。 此选项用于法国、德国或荷兰的特定于国家/地区的导出格式不可用。</li>
<li><strong>Ustrd</strong> – 选择此选项可在针对多个发票结算一个付款时使用未结构化的格式。 已结算发票的发票编号连接到一起，并且用作汇款信息。 {{与：In_compliance_with}} ISO 一致 20022 准则，非结构化汇款信息不能超过 140 个字符。</li>
</ul></td>
</tr>
<tr class="even">
<td>发票数</td>
<td>输入报表打印 <strong>付款通知</strong> 发票的数量。</td>
</tr>
<tr class="odd">
<td>序列号</td>
<td>输入序列号以标识文件。 序列号在 <strong>显示注释</strong> 报表上显示。</td>
</tr>
<tr class="even">
<td>打印出席单</td>
<td>选中此复选框可打印<strong>“出席单”</strong>报表。</td>
</tr>
<tr class="odd">
<td>打印控制报表</td>
<td>选中此复选框可打印包含付款信息的报表。</td>
</tr>
<tr class="even">
<td>打印随函</td>
<td>选中此复选框可打印<strong>“付款通知”</strong>报表。</td>
</tr>
</tbody>
</table>

## <a name="what-are-ibans-and-bics"></a>IBAN 和 BIC 是什么？
国际银行帐号 (IBAN) 和银行标识符代码 (BIC) 在许多国家/地区标识用于全球所有帐户。 包括 34 个 SEPA 国家/地区。 **在伊班族**字段中输入。BIC **的 SWIFT 代码**字段和伊班族。 对于债权人的银行账户和客户的银行账户，这些字段在"银行账户** **页面的**银行账户** **选项卡的其他标识** FastTab 中。 使用 SEPA BIC 的付款不中再次执行。

## <a name="how-do-i-transmit-a-payment-file-to-the-bank"></a>如何将付款文件发送到银行？
在您生成付款时，付款文件生成，并且请求，您{{从中：from}}您的浏览器中到所有具有空位置。 下一步是将 XML 文件发送到您的银行。 此流程根据银行的不同而变。 按照您的银行的说明将文件提交给银行以进行处理。


