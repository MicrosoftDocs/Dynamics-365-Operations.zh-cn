---
title: 奥地利的会计登记服务集成示例
description: 此主题提供 Microsoft Dynamics 365 Commerce 中奥地利的会计整合示例。
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: 826c1cb0fba7025b16dadbfa6157683392945103
ms.sourcegitcommit: 7faf82fa7ce269c0201abb8473af861ef7ce00bf
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/19/2022
ms.locfileid: "8614143"
---
# <a name="fiscal-registration-service-integration-sample-for-austria"></a>奥地利的会计登记服务集成示例

[!include[banner](../includes/banner.md)]

此主题提供 Microsoft Dynamics 365 Commerce 中奥地利的会计整合示例。

为了满足奥地利收银机的当地会计要求，适用于奥地利的 Dynamics 365 Retail 功能将包括销售点 (POS) 与外部会计登记服务集成的示例。 该示例扩展了[会计整合功能](fiscal-integration-for-retail-channel.md)。 它基于 [EFSTA](https://www.efsta.eu/at/) 中的 [EFR（电子会计登记簿）](https://www.efsta.eu/at/fiskalloesungen/oesterreich)解决方案，并允许通过 HTTPS 协议与 EFR 服务通信。 EFR 服务应托管在 Retail Hardware Station 或可从 Hardware Station 连接到的单独计算机上。 该示例以源代码的形式提供，是 Retail 软件开发工具包 (SDK) 的一部分。

Microsoft 不会从 EFSTA 发布任何硬件、软件或文档。 有关如何获取 EFR 解决方案并对其进行操作的信息，请与 [EFSTA](https://www.efsta.eu/at/kontakt) 联系。

## <a name="scenarios"></a>方案

奥地利的会计登记服务集成示例涵盖以下方案：

- 在会计登记服务中登记现金交易：

    - 将详细交易数据发送到会计登记服务。 此数据包括销售行信息以及有关折扣、付款和税款的信息。
    - 捕获来自会计登记服务的响应。 此响应包括数字签名和指向已登记交易的链接。
    - 登记税款并将其映射到会计登记服务的税码。
    - 打印收据上已登记交易的 QR 码。

- 在会计登记服务中将礼品卡操作和客户存款登记为非现金交易：

    - 发放礼品卡或为礼品卡充值。
    - 登记客户帐户存款。
    - 登记客户订单保证金。

- 在会计登记服务中将非销售交易和事件登记为非现金交易：

    - 打开班次，然后关闭班次
    - 起始金额、浮动条目和支付方式删除
    - 价格覆盖
    - 税金覆盖
    - 打印收据副本
    - 开银箱
    - 打印 X 报表
    - 打印 Z 报表

- 打印具有特定于奥地利的字段的日末对帐单（X/Z 报表）：

    - 交付给客户的产品或服务总数
    - 各税率的销售明细
    - 各出纳员/收银机操作员的付款明细
    - 降低每日销售额的价格折扣和退货
    - 零销售（赠品）

- 错误处理，如以下选项：

    - 如果可以重试，例如，如果会计登记服务不可用、未准备好或未响应，则重试会计登记。
    - 推迟会计登记。
    - 跳过会计登记，或将交易标记为已登记，并包括信息代码以捕获失败的原因和其他信息。
    - 在新销售交易打开或完成销售交易之前，检查会计登记服务的可用性。

### <a name="gift-cards"></a>礼品卡

会计登记服务集成示例实施与礼品卡相关的以下规则：

- 从现金交易中排除与 *签发礼品卡* 和 *添加到礼品卡* 操作相关的销售行。 不是将这些行登记为现金交易的一部分，而是在会计登记服务中将这些行登记为单独的非现金交易。
- 如果收据仅包含礼品卡行，则不要在收据上打印税组明细和 QR 码。
- 与收据上的现金交易金额分开打印交易中签发或重新计费的礼品卡的总金额。
- 参考相应的会计交易，在渠道数据库中保存付款行的计算调整。
- 用礼品卡进行的付款被视为常规付款。

### <a name="customer-deposits-and-customer-order-deposits"></a>客户存款和客户订单保证金

会计登记服务集成示例实施与客户存款和客户订单保证金相关的以下规则：

- 如果交易是客户存款，则登记非现金交易。
- 如果交易仅包含客户订单保证金或客户订单保证金退款，则登记非现金交易。
- 创建混合客户订单时，从付款行中扣除客户订单保证金金额。
- 参考混合客户订单的会计交易，在渠道数据库中保存付款行的计算调整。

### <a name="limitations-of-the-sample"></a>示例的限制

会计登记服务仅支持价格中包含销售税的方案。 因此，必须针对商店和客户将 **价格包括销售税** 选项设置为 **是**。

## <a name="set-up-commerce-for-austria"></a>设置适用于奥地利的 Commerce

本节介绍特定于奥地利并针对奥地利推荐的 Commerce 设置。 有关设置的详细信息，请参阅 [Commerce 主页](../index.md)。

若要使用特定于奥地利的功能，您必须指定以下设置：

- 在法人的主要地址中，将 **国家/地区** 字段设置为 **AUT（奥地利）**。
- 在位于奥地利的每个商店的 POS 功能配置文件中，将 **ISO 代码** 字段设置为 **AT（奥地利）**。

您还必须为奥地利指定以下设置。 请注意，您必须在完成设置后运行适当的配送作业。

### <a name="set-up-vat-per-austrian-requirements"></a>根据奥地利要求设置增值税

您必须创建销售税代码、销售税组和物料销售税组。 您还必须设置产品和服务的销售税信息。 有关如何设置和使用销售税功能的详细信息，请参阅[销售税概述](../../finance/general-ledger/indirect-taxes-overview.md)。

在销售收据上，您可以打印销售税代码的缩写代码（例如“A”或“B”）。 若要使此功能可用，请在 **销售税代码** 页面上设置 **打印代码** 字段。

### <a name="set-up-stores"></a>设置商店

在 **所有商店** 页面上，更新商店详细信息。 具体而言，设置以下参数：

- 在 **销售税组** 字段中，指定应该用于向默认客户进行的销售的销售税组。
- 将 **价格含销售税** 选项设置为 **是**。
- 将 **名称** 字段设置为公司名称。 此更改有助于确保公司名称显示在销售收据上。 或者，您可以将公司名称以自由格式文本形式添加到销售收据布局中。
- 将 **纳税标识号 (TIN)** 字段设置为公司标识号。 此更改有助于确保公司标识号显示在销售收据上。 或者，您可以将公司标识号以自由格式文本形式添加到销售收据布局中。

### <a name="set-up-functionality-profiles"></a>设置功能配置文件

设置 POS 功能配置文件：

- 在 **收据编号** 快速选项卡上，通过创建或更新 **销售**、**销售订单** 和 **退货** 收据交易类型的记录来设置收据编号。

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>配置自定义字段，以便可以在销售收据中以收据格式使用这些字段

您可以配置以 POS 收据格式使用的语言文本和自定义字段。 创建收据设置的用户的默认公司应是在其中创建语言文本设置的同一法人。 或者，应在用户的默认公司和为其创建设置的商店的法人中创建相同的语言文本。

在 **语言文本** 页面上，为收据布局的自定义字段的标签添加以下记录。 请注意，表中显示的 **语言 ID**、**文本 ID** 和 **文本** 值只是示例。 您可以更改它们以满足您的要求。 但是，您使用的 **文本 ID** 值必须是唯一的，并且它们必须等于或大于 900001。

从表中将以下 POS 标签添加到 **语言文本** 的 **POS 部分**：

| 语言 ID | 文本 ID | 文本                      |
|-------------|---------|---------------------------|
| zh-Hans       | 900001  | QR 码                   |
| zh-Hans       | 900002  | 连续编号         |
| zh-Hans       | 900003  | 税零售打印代码     |
| zh-Hans       | 900004  | 总计(销售)             |
| zh-Hans       | 900005  | 总税款（销售）         |
| zh-Hans       | 900006  | 含税总额（销售） |
| zh-Hans       | 900007  | 税额（销售）        |
| zh-Hans       | 900008  | 课税标准（销售）         |

在 **自定义字段** 页面上，为收据布局的自定义字段添加以下记录。 请注意，**标题文本 ID** 值必须与您在 **语言文本** 页面上指定的 **文本 ID** 值相对应：

| Name                 | 类型    | 标题文本 ID |
|----------------------|---------|-----------------|
| QRCODE               | 收货 | 900001          |
| CONTINUOUSNUMBER     | 收货 | 900002          |
| RETAILPRINTCODE      | 收货 | 900003          |
| SALESTOTAL           | 收货 | 900004          |
| SALESTOTALTAX        | 收货 | 900005          |
| SALESTOTALINCLUDETAX | 收货 | 900006          |
| SALESTAXAMOUNT       | 收货 | 900007          |
| SALESTAXBASIS        | 收货 | 900008          |

> [!NOTE]
> 您必须指定前一表中列出的正确自定义字段名称。 不正确的自定义字段名称将导致收据中缺少数据。

### <a name="configure-receipt-formats"></a>配置收据格式

对于每个必需的收据格式，请将 **打印行为** 字段的值更改为 **始终打印**。

在收据格式设计器中，将以下自定义字段添加到适当的收据部分。 请注意，字段名称与您在上一节中定义的语言文本相对应。

- **标题：** 添加以下字段：

    - **商店名称** 和 **税标识号** 字段，用于在收据上打印公司名称和标识号。 或者，您可以将公司名称和标识编号以自由格式文本形式添加到布局中。
    - **商店地址**、**日期**、**时间 24H**、**收据编号** 和 **登记编号** 字段。
    - **连续编号** 字段，用于标识会计登记服务中的现金交易记录的编号。

- **行：** 添加以下字段：

    - **物料名称**。
    - **数量**。
    - **总价（含税）**。
    - **税零售打印代码**，用于打印与适用于物料的销售税代码相对应的缩写代码。

- **页脚：** 添加以下字段：

    - 付款字段，以便打印每个付款方式的付款金额。 例如，将 **支付名称** 和 **支付金额** 字段添加到布局的一行中。
    - **销售额总计** 字段组：

        - **总计（销售）** 字段，用于打印收据的总现金销售金额。 此金额不含税。 不包括预付款和礼品卡操作。
        - **含税总额（销售）** 字段，用于打印收据的总现金销售金额。 此金额含税。 不包括预付款和礼品卡操作。
        - **含税总额（销售）** 字段，用于打印收据的现金销售总税额。 不包括预付款和礼品卡操作。

    - **税目明细** 字段组。 此字段组中的所有字段都必须打印在一个单独的行上。

        - **纳税人标识号** 字段，这是一个标准字段，可以对每个销售税代码打印销售税汇总。 该字段必须添加到新行中。
        - **纳税百分比** 字段，这是用于打印销售税代码的有效税率的标准字段。
        - **课税标准（销售）** 字段，用于打印收据的销售税代码的现金销售总额。 不包括预付款和礼品卡操作。
        - **税额（销售）** 字段，用于打印收据的销售税代码的现金销售税额。
        - **税零售打印代码** 字段，用于打印与销售税代码相对应的缩写代码。

    - **QR 码** 字段，用于以 QR 码形式打印已登记现金交易的参考。

        > [!NOTE]
        > 从会计登记簿响应检索 **QR 码** 值。 只有在 EFSTA 文档中描述 EFR 配置中的 **属性** 字段的值时，EFR 才会返回其响应中的 QR 码。 EFR 配置中的 **属性** 字段中的 QR 码格式必须设置为 **BMP**。

有关如何使用收据格式的详细信息，请参阅[设置和设计收据格式](../receipt-templates-printing.md)。

## <a name="set-up-fiscal-integration-for-austria"></a>设置奥地利的会计整合

奥地利的会计登记服务集成示例基于[会计整合功能](fiscal-integration-for-retail-channel.md)，是 Retail SDK 的一部分。 该示例位于 [Dynamics 365 Commerce 解决方案](https://github.com/microsoft/Dynamics365Commerce.Solutions/)存储库的 **src\\FiscalIntegration\\Efr** 文件夹中（例如[版本/9.33 中的示例](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)）。 该示例[包含](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services)一个会计单据提供程序（即 Commerce Runtime (CRT) 的扩展），以及一个会计连接器（即 Commerce Hardware Station 的扩展）。 有关如何使用 Retail SDK 的详细信息，请参阅 [Retail SDK 体系结构](../dev-itpro/retail-sdk/retail-sdk-overview.md)和[设置独立包装 SDK 的生成管道](../dev-itpro/build-pipeline.md)。

> [!WARNING]
> 由于[新的独立包装和扩展模型](../dev-itpro/build-pipeline.md)的限制，它当前无法用于此会计整合示例。 您必须在 Microsoft Dynamics Lifecycle Services (LCS) 中的开发人员虚拟机 (VM) 上使用先前版本的 Retail SDK。 有关详细信息，请参阅[奥地利会计整合示例的部署准则（旧版）](emea-aut-fi-sample-sdk.md)。 以后的版本计划支持会计整合示例的新独立包装和扩展模型。

完成会计整合设置步骤，如[设置 Commerce 渠道的会计整合](setting-up-fiscal-integration-for-retail-channel.md)中所述：

1. [设置会计登记流程](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process)。 此外，请记下[特定于此会计登记服务整合示例](#set-up-the-registration-process)的会计登记流程的设置。
1. [设置错误处理设置](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings)。
1. [启用已推迟会计登记的手动执行](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration)。
1. [配置渠道组件](#configure-channel-components)。

### <a name="set-up-the-registration-process"></a>设置登记流程

要启用登记流程，请按照以下步骤设置 Commerce Headquarters。 有关详细信息，请参阅[设置 Commerce 渠道的会计整合](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process)。

1. 下载会计单据提供程序和会计连接器的配置文件：

    1. 打开 [Dynamics 365 Commerce 解决方案](https://github.com/microsoft/Dynamics365Commerce.Solutions/)存储库。
    1. 根据您的 SDK/应用程序版本（例如 **[版本/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**）选择正确的发布分支版本。
    1. 打开 **src \> FiscalIntegration \> Efr**。
    1. 打开 **配置 \>DocumentProviders** 并下载会计单据提供程序配置文件：**DocumentProviderFiscalEFRSampleAustria.xml** 和 **DocumentProviderNonFiscalEFRSampleAustria.xml**（例如，[版本/9.33 的文件的位置](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders)）。
    1. 下载 **Configurations \> Connectors \> ConnectorEFRSample.xml** 中的会计连接器配置文件（例如，[版本/9.33 的文件](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml)）。

    > [!WARNING]
    > 由于[新的独立包装和扩展模型](../dev-itpro/build-pipeline.md)的限制，它当前无法用于此会计整合示例。 您必须在 LCS 中的开发人员 VM 上使用先前版本的 Retail SDK。 此会计整合示例的配置文件位于 LCS 中开发人员 VM 上 Retail SDK 的以下文件夹中：
    >
    > - **会计单据提供程序配置文件：** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.EFRSample\\Configuration
    > - **会计连接器配置文件：** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.EFRSample\\Configuration
    > 
    > 以后的版本计划支持会计整合示例的新独立包装和扩展模型。

1. 转到 **Retail 和 Commerce \> Headquarters 设置 \> 参数 \> Commerce 共享参数**。 在 **常规** 选项卡上，将 **启用会计整合** 选项设置为 **是**。
1. 转到 **Retail 和 Commerce \> 渠道设置 \> 会计整合 \> 会计单据提供程序**，并加载您之前下载的会计单据提供程序配置文件。
1. 转到 **Retail 和 Commerce \> 渠道设置 \> 会计整合 \> 会计连接器**，并加载您之前下载的会计连接器配置文件。
1. 转至 **Retail 和 Commerce \> 渠道设置 \> 会计整合 \> 连接器功能配置文件**。 创建两个新的连接器功能配置文件（分别用于您之前加载的每个会计单据提供程序），并选择您之前加载的会计连接器。 根据需要更新[数据映射设置](#default-data-mapping)。
1. 转至 **Retail 和 Commerce \> 渠道设置 \> 会计整合 \> 连接器技术配置文件**。 创建新的连接器技术配置文件，并选择您之前加载的会计连接器。 根据需要更新[连接器设置](#fiscal-connector-settings)。
1. 转至 **Retail 和 Commerce \> 渠道设置 \> 会计整合 \> 会计连接器组**。 创建两个新的会计连接器组，用于您之前创建的每个连接器功能配置文件。
1. 转至 **Retail 和 Commerce \> 渠道设置 \> 会计整合 \> 会计登记流程**。 创建新的会计登记流程和两个会计登记流程步骤，并选择您之前创建的会计连接器组。
1. 转至 **Retail 和 Commerce \> 渠道设置 \> POS 设置 \> POS 配置文件 \> 功能配置文件**。 选择链接到应在其中激活登记流程的商店的功能配置文件。 在 **会计登记流程** 快速选项卡上，选择您之前创建的会计登记流程。 若要允许在 POS 上登记非会计事件，请在 **功能** 快速选项上的 **POS** 下面，将 **审计** 选项设置为 **是**。
1. 转至 **Retail 和 Commerce \> 渠道设置 \> POS 设置 \> POS 配置文件 \> 硬件配置文件**。 选择链接到会计打印机将连接到的 Hardware Station 的硬件配置文件。 在 **会计外围设备** 快速选项卡上，选择您之前创建的连接器技术配置文件。
1. 打开配送计划（**Retail 和 Commerce \> Retail 和 Commerce IT \> 配送计划**），选择作业 **1070** 和 **1090** 以将数据传输到渠道数据库。

#### <a name="default-data-mapping"></a>默认数据映射

作为会计整合示例的一部分提供的会计单据提供程序配置中包含以下默认数据映射：

- **增值税 (VAT) 费率映射** - 为销售税代码设置的纳税百分比值到请求中发送到会计服务的 **TaxG**（税组）属性值的映射。 以下是默认映射：

    ```
    A: 20.00; B: 10.00; C: 13.00; D: 0.00; E: 19.00; F: 7.00
    ```

    每个对中的第一个组件都表示 EFR 会计登记服务支持的增值税组。 第二个组件表示相应的增值税税率。 有关 EFR 支持的奥地利增值税组的详细信息，请参阅 [EFR 参考](https://public.efsta.net/efr/)。

#### <a name="fiscal-connector-settings"></a>会计连接器设置

作为会计整合示例的一部分提供的会计连接器配置中包含以下设置：

- **终结点地址** - 会计登记服务的 URL。
- **设备超时** - 会计连接器等待会计登记服务响应的时长（毫秒）。
- **显示会计登记通知** - 此标记控制是否应向操作员显示会计登记服务返回的通知。

### <a name="configure-channel-components"></a>配置渠道组件

> [!WARNING]
> 由于[新的独立包装和扩展模型](../dev-itpro/build-pipeline.md)的限制，它当前无法用于此会计整合示例。 您必须在 LCS 中的开发人员 VM 上使用先前版本的 Retail SDK。 有关详细信息，请参阅[奥地利会计整合示例的部署准则（旧版）](emea-aut-fi-sample-sdk.md)。
>
> 以后的版本计划支持会计整合示例的新独立包装和扩展模型。

#### <a name="set-up-the-development-environment"></a>设置开发环境

若要设置开发环境以测试和扩展示例，请按照以下步骤操作。

1. 克隆或下载 [Dynamics 365 Commerce 解决方案](https://github.com/microsoft/Dynamics365Commerce.Solutions)存储库。 根据您的 SDK/应用程序版本选择正确的发布分支版本。 有关详细信息，请参阅[从 GitHub 和 NuGet 下载 Retail SDK 示例和引用包](../dev-itpro/retail-sdk/sdk-github.md)。
1. 在 **Dynamics365Commerce.Solutions\\FiscalIntegration\\Efr\\EFR.sln** 打开 EFR 解决方案，并构建它。
1. 安装 CRT 扩展：

    1. 查找 CRT 扩展安装程序：

        - **Commerce Scale Unit：** 在 **Efr\\ScaleUnit\\ScaleUnit.EFR.Installer\\bin\\Debug\\net461** 文件夹中，查找 **ScaleUnit.EFR.Installer** 安装程序。
        - **Modern POS 上的本地 CRT：** 在 **Efr\\ModernPOS\\ModernPOS.EFR.Installer\\bin\\Debug\\net461** 文件夹中，查找 **ModernPOS.EFR.Installer** 安装程序。

    1. 从命令行启动 CRT 扩展安装程序：

        - **Commerce Scale Unit：**

            ```Console
            ScaleUnit.EFR.Installer.exe install --verbosity 0
            ```

        - **Modern POS 上的本地 CRT：**

            ```Console
            ModernPOS.EFR.Installer.exe install --verbosity 0
            ```

1. 安装会计连接器扩展：

    您可以在[硬件工作站](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station)或 [POS 收银机](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-or-service-in-the-local-network)上安装会计连接器扩展。

    1. 安装 Hardware Station 扩展：

        1. 在 **Efr\\HardwareStation\\HardwareStation.EFR.Installer\\bin\\Debug\\net461** 文件夹中，查找 **HardwareStation.EFR.Installer** 安装程序。
        1. 通过运行以下命令从命令行启动扩展安装程序。

            ```Console
            HardwareStation.EFR.Installer.exe install --verbosity 0
            ```

    1. 安装 POS 扩展：

        1. 在 **Dynamics365Commerce.Solutions\\FiscalIntegration\\PosFiscalConnectorSample\\Contoso.PosFiscalConnectorSample.sln** 打开 POS 会计连接器示例解决方案，然后构建它。
        1. 在 **PosFiscalConnectorSample\\StoreCommerce.Installer\\bin\\Debug\\net461** 文件夹中，找到 **Contoso.PosFiscalConnectorSample.StoreCommerce.Installer** 安装程序。
        1. 从运行以下命令的命令行启动扩展安装程序。

            ```Console
            Contoso.PosFiscalConnectorSample.StoreCommerce.Installer.exe install --verbosity 0
            ```

#### <a name="production-environment"></a>生产环境

按照[为会计整合示例设置生成管道](fiscal-integration-sample-build-pipeline.md)中的步骤生成和发布会计整合示例的 Cloud Scale Unit 和自助可部署包。 可在 [Dynamics 365 Commerce 解决方案](https://github.com/microsoft/Dynamics365Commerce.Solutions)存储库的 **Pipeline\\YAML_Files** 文件夹中找到 **EFR build-pipeline.yml** 模板 YAML 文件。

## <a name="design-of-extensions"></a>扩展设计

奥地利的会计登记服务集成示例基于[会计整合功能](fiscal-integration-for-retail-channel.md)，是 Retail SDK 的一部分。 该示例位于 [Dynamics 365 Commerce 解决方案](https://github.com/microsoft/Dynamics365Commerce.Solutions/)存储库的 **src\\FiscalIntegration\\Efr** 文件夹中（例如[版本/9.33 中的示例](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)）。 该示例[包含](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services)一个会计单据提供程序（即 CRT 的扩展），以及一个会计连接器（即 Commerce Hardware Station 的扩展）。 有关如何使用 Retail SDK 的详细信息，请参阅 [Retail SDK 体系结构](../dev-itpro/retail-sdk/retail-sdk-overview.md)和[设置独立包装 SDK 的生成管道](../dev-itpro/build-pipeline.md)。

> [!WARNING]
> 由于[新的独立包装和扩展模型](../dev-itpro/build-pipeline.md)的限制，它当前无法用于此会计整合示例。 您必须在 LCS 中的开发人员 VM 上使用先前版本的 Retail SDK。 有关详细信息，请参阅[奥地利会计整合示例的部署准则（旧版）](emea-aut-fi-sample-sdk.md)。 以后的版本计划支持会计整合示例的新独立包装和扩展模型。

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime 扩展设计 

作为会计单据提供程序的扩展的目的是生成特定于服务的单据并处理会计登记服务的响应。

#### <a name="request-handler"></a>请求处理程序

文档提供程序有两个请求处理程序：

- **DocumentProviderEFRFiscalAUT** - 此处理程序用于为会计登记服务生成会计单据。
- **DocumentProviderEFRNonFiscalAUT** - 此处理程序用于为会计登记服务生成非会计单据。

这些处理程序继承自 **INamedRequestHandler** 接口。 **HandlerName** 方法负责返回处理程序的名称。 处理程序名称应与 Commerce Headquarters 中指定的连接器文档提供程序名称匹配。

此连接器支持以下请求：

- **GetFiscalDocumentDocumentProviderRequest** - 此请求包含有关应生成的具体单据的信息。 它返回应在会计登记服务中登记的特定于服务的单据。
- **GetNonFiscalDocumentDocumentProviderRequest** - 此请求包含有关应生成的具体非会计单据的信息。 它返回应在会计登记服务中登记的特定于服务的单据。
- **GetSupportedRegistrableEventsDocumentProviderRequest** - 此请求返回要订阅的事件列表。 当前，支持以下事件：销售、打印 X 报表、打印 Z 报表、客户帐户存款、客户订单保证金、审计事件和非销售交易。
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** - 此请求返回会计登记服务的响应。 此响应已序列化以形成字符串，以便可以保存。

#### <a name="configuration"></a>配置

会计单据提供程序的配置文件位于 [Dynamics 365 Commerce 解决方案](https://github.com/microsoft/Dynamics365Commerce.Solutions/)存储库的 **src\\FiscalIntegration\\Efr\\Configurations\\DocumentProviders** 文件夹中：

- **DocumentProviderFiscalEFRSampleAustria** - 会计单据的会计单据提供程序的配置文件。
- **DocumentProviderNonFiscalEFRSampleAustria** - 非会计单据的会计单据提供程序的配置文件。

这些文件的目的是启用要从 Commerce Headquarters 配置的会计单据提供程序的设置。 文件格式符合会计集成配置的要求。

### <a name="hardware-station-extension-design"></a>Hardware Station 扩展设计

会计连接器扩展的目的是与会计登记服务通信。 硬件工作站扩展使用 HTTP 和 HTTPS 协议将 CRT 扩展生成的单据提交到会计登记服务。 它还处理从会计登记服务收到的响应。

#### <a name="request-handler"></a>请求处理程序

**EFRHandler** 请求处理程序是处理请求进入会计登记服务的入口点。

此处理程序继承自 **INamedRequestHandler** 接口。 **HandlerName** 方法负责返回处理程序的名称。 处理程序名称应与 Commerce Headquarters 中指定的会计连接器名称匹配。

会计连接器支持以下请求：

- **SubmitDocumentFiscalDeviceRequest** - 此请求将单据发送到会计登记服务并返回此服务的响应。
- **IsReadyFiscalDeviceRequest** - 此请求用于检查会计登记服务的运行状况。
- **InitializeFiscalDeviceRequest** - 此请求用于初始化会计登记服务。

#### <a name="configuration"></a>配置

会计连接器的配置文件位于 [Dynamics 365 Commerce 解决方案](https://github.com/microsoft/Dynamics365Commerce.Solutions/)存储库内的 **src\\FiscalIntegration\\Efr\\Configurations\\Connectors\\ConnectorEFRSample.xml** 中。 此文件的目的是启用要从 Commerce Headquarters 配置的会计连接器的设置。 文件格式符合会计集成配置的要求。

### <a name="pos-fiscal-connector-extension-design"></a>POS 会计连接器扩展的设计

POS 会计连接器扩展的目的是与 POS 的会计登记服务通信。 它使用 HTTPS 协议进行通信。

#### <a name="fiscal-connector-factory"></a>会计连接器工厂

会计连接器工厂将连接器名称映射到会计连接器实现，它位于 **Pos.Extension\\Connectors\\FiscalConnectorFactory.ts** 文件中。 连接器名称应与 Commerce Headquarters 中指定的会计连接器名称匹配。

#### <a name="efr-fiscal-connector"></a>EFR 会计连接器

EFR 会计连接器位于 **Pos.Extension\\Connectors\\Efr\\EfrFiscalConnector.ts** 文件中。 它实现支持以下请求的 **IFiscalConnector** 接口：

- **FiscalRegisterSubmitDocumentClientRequest** – 此请求将单据发送到会计登记服务并返回此服务的响应。
- **FiscalRegisterIsReadyClientRequest** – 此请求用于检查会计登记服务的运行状况。
- **FiscalRegisterInitializeClientRequest** – 此请求用于初始化会计登记服务。

#### <a name="configuration"></a>配置

配置文件位于 [Dynamics 365 Commerce 解决方案](https://github.com/microsoft/Dynamics365Commerce.Solutions/)存储库的 **src\\FiscalIntegration\\Efr\\Configurations\\Connectors** 文件夹中。 此文件的目的是启用要从 Commerce Headquarters 配置的会计连接器的设置。 文件格式符合会计集成配置的要求。 添加了以下设置：

- **终结点地址** - 会计登记服务的 URL。
- **超时** – 连接器等待会计登记服务响应的以毫秒为单位的时长。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
