---
title: 挪威收银机功能
description: 本文概述 Microsoft Dynamics 365 Commerce 中适用于挪威的收银机功能，并提供关于设置此功能的指南。
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2017-10-31
ms.openlocfilehash: 778a947f03866518219e9c0fa44660d66f19f53a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906691"
---
# <a name="cash-register-functionality-for-norway"></a>挪威收银机功能

[!include[banner](../includes/banner.md)]

本文概述 Dynamics 365 Commerce 中适用于挪威的收银机功能。 它还提供关于设置此功能的指南。 该功能由以下部分组成：

- 适用于所有国家或地区中的客户的通用销售点 (POS) 功能。 示例包括一个可防止多次打印收据副本的选项。
- 特定于挪威的功能，例如销售交易的数字签名。

## <a name="overview-of-cash-register-functionality-for-norway"></a>挪威的收银机功能概览

### <a name="common-pos-features"></a>通用 POS 功能

要了解适用于所有国家或地区中的客户的 POS 功能，请参阅 [Dynamics 365 Retail 的“帮助”资源](../index.md)。

以前实施并提供给所有国家或地区中的客户的以下 POS 本地化功能现在可以专门用于挪威：

- **以大字体大小打印收据上的文本字段。** 您可以使用收据格式设计器中的 **字体大小** 参数来指定应该将大字体大小用于收据格式中的字段。 （大字体大小大约是通常字体大小的两倍。）例如，您可以使用此参数在收据副本上以大字符打印“副本”指示符。
- **在 POS 审计事件日志中登记收据副本的打印。** 您可以使用 POS 功能配置文件中的 **审核** 参数来启用要打印的收据副本和要登记的其他 POS 审计事件。 审计事件在渠道数据库和 Headquarters 中登记。 您可以在 **审计事件** 页面上查看审计事件。
- **防止多次打印收据副本。** 启用 POS 功能配置文件中的 **审核** 参数后，**允许打印收据副本** POS 权限将控制是否可以打印收据副本。 还有一个可防止多次打印收据副本的选项。

此外，以下 POS 功能已为挪威实施，但可供所有国家或地区中的客户使用：

- **在 POS 审计事件日志中注册其他事件。** 如果启用了 POS 功能配置文件中的 **审核** 参数，则会在 POS 审计事件日志中注册以下事件：

    - 价格查询
    - 税覆盖
    - 对行数量的更正
    - 从渠道数据库中清除交易

### <a name="norway-specific-pos-features"></a>特定于挪威的 POS 功能

当 POS 功能配置文件中的 **ISO 代码** 参数设置为 **否** 时，将启用以下特定于挪威的 POS 功能。

#### <a name="digital-signing-of-sales-transactions"></a>销售交易的数字签名

每笔交易都会经过数字签名。 签名在交易完成时创建并记录在 POS 交易日记帐中。 签名也可用于为审计目的而导出的日记帐中。

仅签署现金销售交易。 以下是签名过程中不包括的一些交易示例：

- 预付款（客户帐户存款）
- 销售订单的预付款（客户订单保证金）
- 发放礼品卡
- 非销售交易（浮动条目、支付方式删除等）

已签名的数据是由以下数据字段组成的文本字符串。 数据字段用分号分隔。

1. 同一 POS 的上一个签名（第一个交易使用了零 \[**0**\]。）
2. 交易日期
3. 交易记录时间
4. 连续签名的交易编号
5. 含税的交易金额
6. 不含税的交易金额

数字签名流程使用具有 SHA-1 哈希功能 (RSA-SHA1-1024) 的 RSA 1024 位密钥。 在 Commerce Scale Unit 上安装的证书用于签名。 证书的唯一标识符（占用情况）与签名一起记录。

签名与交易数据一起存储在商店数据库和 Headquarters (HQ) 数据库中。 您可以在 **商店交易** 页面的 **会计交易** 快速选项卡上查看交易签名以及用于生成此签名的交易数据。

#### <a name="receipts"></a>收货

挪威收据可以包括通过使用自定义字段实现的其他信息：

- **收据标题** - 您可以将字段添加到收据格式布局以标识收据的类型。 例如，销售收据将包括文本“销售收据”。
- **已签名交易序列号** - 已签名交易的序列号可以显示在收据上，以便将打印的收据与数据库中的数字签名关联。
- **收据合计** – 收据合计自定义字段从交易总金额中排除非销售金额。 非销售金额包括以下操作的金额：

    - 预付款（客户帐户存款）
    - 销售订单的预付款（客户订单保证金）
    - 发放礼品卡
    - 向礼品卡充值

#### <a name="x-and-z-reports"></a>X 和 Z 报表

X 和 Z 报表中包含的信息基于挪威的要求。 例如，**现金销售总金额** 仅包含现金销售交易的金额，不包含签发礼品卡操作和预付款。 还针对每个物料组和付款方式列出了现金销售总额。 此外，还维护和打印累计 **总销售额** 和 **总退货** 金额。

#### <a name="saf-t-cash-register-audit-file"></a>SAF-T 收银机审计文件

您可以以预定义的标准审计文件 - 税 (SAF-T) 收银机格式导出 POS 交易日记帐。 审计文件包括有关组织的信息、相关主数据（如物料组、物料和税码）、现金销售交易数据以及这些交易的签名、非销售事件数据和结束日期报表数据。

可针对以下方案导出审计文件：

- 每个商店
- 所有商店
- 每个终端
- 所有终端

您也可以代表另一个法人从一个法人发送报表。 在这种情况下，您必须从运营法人运行导出并指定报告法人作为报表的发件人。

使用[电子报告](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md)在 Headquarters 实施 SAF-T 收银机格式。 

## <a name="setting-up-commerce-for-norway"></a>设置适用于挪威的 Commerce

本节介绍特定于挪威并针对挪威推荐的 Commerce 设置。 有关详细信息，请参阅 [Dynamics 365 Retail 的帮助资源](../index.md)。

若要使用特定于挪威的功能，您必须完成以下任务：

- 在法人的主要地址中，将 **国家/地区** 字段设置为 **NOR**（挪威）。
- 在位于挪威的每个商店的 ISO 功能配置文件中，将 **POS 代码** 字段设置为 **NO**（挪威）。

您还必须为挪威指定以下设置。

### <a name="set-up-the-legal-entity"></a>设置法人

确保指定了法人的名称。 此名称将打印在 X 和 Z 报表上。

此外，在 **银行帐户信息** 快速选项卡上的 **银行代号** 字段中，指定组织编号。

### <a name="set-up-value-added-tax-vat-per-norwegian-requirements"></a>根据挪威的要求设置增值税 (VAT)


您必须创建销售税代码、销售税组和物料销售税组。 您还必须设置产品和服务的销售税信息。 有关如何设置和使用销售税的详细信息，请参阅[销售税概述](../../finance/general-ledger/indirect-taxes-overview.md)。

您还必须指定销售税组，并为位于挪威的商店启用 **价格包括销售税** 选项。

### <a name="set-up-functionality-profiles"></a>设置功能配置文件

必须启用审核并设置收据编号。

### <a name="update-pos-permissions-groups-and-individual-permission-settings-for-store-workers"></a>为商店工作人员更新 POS 权限组和个人权限设置

将 **允许打印收据副本** 权限设置为适当的值：

- **始终允许** - 操作员可以多次打印收据副本。
- **只允许一次** - 操作员只能打印一次收据副本。
- **仅允许一次，并且仅当 HQ DB 可用时** - 操作员只能打印一次收据副本，并且仅当通过 Commerce Data Exchange：实时服务提供 HQ 数据库时才能打印，以便系统可以验证以前是否在商店中未打印收据副本。
- **从不** - 操作员无法打印收据副本。

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>配置自定义字段，以便可以在销售收据中以收据格式使用这些字段

在 **语言文本** 页面上，为收据布局的自定义字段的标签添加以下记录。 请注意，表中显示的 **语言 ID**、**文本 ID** 和 **文本** 值只是示例。 您可以更改它们以满足您的要求。

| 语言 ID | 文本                   | 文本 ID |
|-------------|------------------------|---------|
| zh-Hans       | 收据标题          | 900011  |
| zh-Hans       | 礼品卡           | 900012  |
| zh-Hans       | 总计(销售)          | 900013  |
| zh-Hans       | 总税款(销售)      | 900014  |
| zh-Hans       | 含税合计(销售) | 900015  |
| zh-Hans       | 纳税金额(销售)     | 900016  |
| zh-Hans       | 现金交易记录 ID    | 900017  |

在 **自定义字段** 页面上，为收据布局的自定义字段添加以下记录。 请注意，**标题文本 ID** 值必须与您在 **语言文本** 页面上指定的 **文本 ID** 值相对应。

| Name                            | 类型    | 标题文本 ID |
|---------------------------------|---------|-----------------|
| ReceiptTitle                    | 收货 | 900011          |
| IsGiftCard                      | 收货 | 900012          |
| SalesTotalExt                   | 收货 | 900013          |
| TaxTotalExt                     | 收货 | 900014          |
| TotalWithTaxExt                 | 收货 | 900015          |
| AmountPerTaxExt                 | 收货 | 900016          |
| CashTransactionSequentialNumber | 收货 | 900017          |

> [!NOTE]
> 您必须指定上表中列出的正确自定义字段名称。 不正确的自定义字段名称将导致收据中缺少数据。

### <a name="configure-receipt-formats"></a>配置收据格式

对于所有必需的收据格式，请针对收据格式将 **打印行为** 字段的值更改为 **始终打印**。

在收据格式设计器中，将以下自定义字段添加到适当的收据部分。 请注意，字段名称与您在上一节中定义的语言文本相对应。

1. 页眉：

    - **收据标题** - 此字段标识收据的类型。
    - **现金交易记录 ID** - 此字段打印已签名现金交易的序列号。

2. 行:

    - **是礼品卡** - 此字段将收据行标记为与“发放礼品卡”或“添加到礼品卡”操作相关。

3. 页脚：

    - **总计（销售）**- 此字段打印收据的总现金销售金额。 此金额不含税。 不包括预付款和礼品卡操作。
    - **税总额（销售）**- 此字段打印收据的总现金销售税金额。 不包括预付款和礼品卡操作。
    - **含税总计（销售）**- 此字段打印收据的总现金销售金额。 此金额含税。 不包括预付款和礼品卡操作。
    - **税额（销售）**- 此字段打印收据的每个税码的总现金销售税金额。 不包括预付款和礼品卡操作。

有关如何使用收据格式的详细信息，请参阅[设置和设计收据格式](../receipt-templates-printing.md)。

### <a name="configure-the-saf-t-cash-register-export-format"></a>配置 SAF-T 收银机导出格式

SAF-T 收银机配置可从 Microsoft Dynamics Lifecycle Services (LCS) 中下载。 有关详细信息，请参阅[导入电子申报配置](../../fin-ops-core/dev-itpro/analytics/electronic-reporting-import-ger-configurations.md)。 您必须下载以下配置：

- **Retail channel data.version.1** – 数据模型配置。
- **DMM Retail channel data.version.1.14** – 数据模型映射配置。
- **NO SAF T Cash Register.version.1.20** – 格式配置。

导入配置后，在 **Commerce 参数** 页面 **电子单据** 选项卡上的 **SAF-T 收银机导出格式** 字段中，选择已导入的格式配置的名称。

您还必须将所需的主数据映射到预定义的 SAF-T 标准代码。 有关详细信息，请参阅由挪威税务管理机构提供的 SAF-T 收银机文档。 若要创建映射，您必须在以下页面上设置新的 **SAF-T 收银机代码** 字段：

- 物料组
- 付款方式
- 销售税代码

### <a name="configure-channel-components"></a>配置渠道组件

若要启用特定于挪威的功能，您必须配置渠道组件。 有关详细信息，请参见[部署指南](emea-nor-fi-deployment.md)。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
