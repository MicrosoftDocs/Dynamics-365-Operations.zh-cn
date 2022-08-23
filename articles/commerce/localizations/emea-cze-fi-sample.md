---
title: 捷克共和国的会计登记服务集成示例
description: 本文提供 Microsoft Dynamics 365 Commerce 中捷克共和国的会计整合示例。
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: dc7ef27954de2bb10bbaf91fc5a3aa14d6ee6ffd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280325"
---
# <a name="fiscal-registration-service-integration-sample-for-the-czech-republic"></a>捷克共和国的会计登记服务集成示例

[!include[banner](../includes/banner.md)]

本文提供 Microsoft Dynamics 365 Commerce 中捷克共和国的会计整合示例。

为了满足捷克共和国收银机的当地会计要求，适用于捷克共和国的 Dynamics 365 Commerce 功能将包括销售点 (POS) 与外部会计登记服务集成的示例。 该示例扩展了[会计整合功能](fiscal-integration-for-retail-channel.md)。 它基于 [EFSTA](https://efsta.org/) 中的 [EFR（电子会计登记簿）](https://efsta.org/sicherheitsloesungen/)解决方案，并允许通过 HTTPS 协议与 EFR 服务通信。 EFR 服务可确保实现电子销售登记 (EET - Elektronická evidence tržeb)，即将销售数据在线传输到税务机关的会计 Web 服务。

EFR 服务应托管在 Commerce Hardware Station 或可从 Hardware Station 连接到的单独计算机上。 该示例以源代码的形式提供，是 Retail 软件开发工具包 (SDK) 的一部分。

Microsoft 不会从 EFSTA 发布任何硬件、软件或文档。 有关如何获取 EFR 解决方案并对其进行操作的信息，请与 [EFSTA](https://efsta.org/kontakt/) 联系。

## <a name="scenarios"></a>方案

捷克共和国的会计登记服务集成示例涵盖以下方案：

- 在会计登记服务中登记现金交易。

    - 将详细交易数据发送到会计登记服务。 此数据包括销售行信息以及有关折扣、付款和税款的信息。 会计登记服务会进一步将数据发送到税务主管机构的 Web 服务，并从中接收包括交易的会计标识代码的确认。
    - 捕获来自会计登记服务的响应。 此响应包括会计数据，如交易的会计标识代码和安全代码等。
    - 打印收据上已登记交易的会计数据。

- 在会计登记服务中登记礼品卡操作和客户存款。

    - 发放礼品卡或为礼品卡充值。
    - 登记客户帐户存款。
    - 创建客户订单并登记订单的保证金。
    - 编辑客户订单并替代订单的保证金。
    - 取消客户订单并退还订单的保证金。

- 错误处理，如以下选项。

    - 如果可以重试，例如，如果会计登记服务不可用、未准备好或未响应，则重试会计登记。
    - 推迟会计登记。
    - 跳过会计登记，或将交易标记为已登记，并包括信息代码以捕获失败的原因和其他信息。
    - 在新销售交易打开或完成销售交易之前，检查会计登记服务的可用性。

### <a name="gift-cards"></a>礼品卡

会计登记服务集成示例实施与礼品卡相关的以下规则。

- 在会计登记服务中登记交易时，销售交易中与 *签发礼品卡* 或 *添加到礼品卡* 操作相关的销售行标有特殊属性。
- 在会计登记服务中登记交易时，用礼品卡进行的付款被视为常规付款，并且标有特殊属性。

### <a name="customer-account-deposits-and-customer-order-deposits"></a>客户帐户存款和客户订单保证金

会计登记服务集成示例实施与客户帐户存款和客户订单保证金相关的以下规则。

- 与客户帐户存款或客户订单保证金相关的交易在会计登记服务中登记为单行交易，并且标有特殊属性。 在此行中指定了存款增值税组。
- 创建混合客户订单时，即包含客户可以从店内自提的产品以及以后将拣货或装运的产品的客户订单，会计登记服务中登记的交易包含自提产品行以及订单保证金行。
- 在会计登记服务中登记交易时，客户帐户付款被视为常规付款，并且标有特殊属性。
- 在会计登记服务中登记交易时，应用于客户订单提货操作的客户订单保证金金额被视为常规付款，并且标有特殊属性。

### <a name="offline-registration"></a>脱机登记

如果会计登记服务无法将交易数据传输到税务主管机构的会计 Web 服务（例如，由于响应超时），并且无法从 Web 服务接收确认（即交易的会计标识代码），则它将生成交易的本地签名，并在响应中包括该签名和特殊错误代码。 在还原网络连接后，会计登记服务将立即按原始顺序在后台重新发送交易。

### <a name="limitations-of-the-sample"></a>示例的限制

会计登记服务仅支持价格中包含销售税的方案。 因此，必须针对商店和客户将 **价格包括销售税** 选项设置为 **是**。

## <a name="set-up-commerce-for-the-czech-republic"></a>设置适用于捷克共和国的 Commerce

本节介绍特定于捷克共和国并针对捷克共和国推荐的 Commerce 设置。 有关详细信息，请参阅 [Commerce 主页](../index.md)。

若要使用特定于捷克的功能，您必须指定以下设置。

- 在法人的主要地址中，将 **国家/地区** 字段设置为 **CZE**（捷克共和国）。
- 在位于捷克共和国的每个商店的 POS 功能配置文件中，将 **ISO 代码** 字段设置为 **CZ**（捷克共和国）。

您还必须为捷克共和国指定以下设置。 请注意，您必须在完成设置后运行适当的配送作业。

### <a name="set-up-vat-per-czech-republic-requirements"></a>根据捷克共和国要求设置增值税


您必须创建销售税代码、销售税组和物料销售税组。 您还必须设置产品和服务的销售税信息。 有关如何设置和使用销售税功能的详细信息，请参阅[销售税概述](../../finance/general-ledger/indirect-taxes-overview.md)。

### <a name="set-up-stores"></a>设置商店

在 **所有商店** 页面上，更新商店详细信息。 具体而言，设置以下参数。

- 在 **销售税组** 字段中，指定应该用于向默认客户进行的销售的销售税组。
- 将 **价格含销售税** 选项设置为 **是**。
- 将 **名称** 字段设置为公司名称。 此更改有助于确保公司名称显示在销售收据上。 或者，您可以将公司名称以自由格式文本形式添加到销售收据布局中。
- 将 **纳税标识号 (TIN)** 字段设置为公司标识号。 此更改有助于确保公司标识号显示在销售收据上。 或者，您可以将公司标识号以自由格式文本形式添加到销售收据布局中。

### <a name="set-up-functionality-profiles"></a>设置功能配置文件

设置 POS 功能配置文件。

- 在 **收据编号** 快速选项卡上，通过创建或更新 **销售**、**销售订单** 和 **退货** 收据交易类型的记录来设置收据编号。

### <a name="set-up-registration-numbers"></a>设置登记编号

1. 转到 **组织管理 \> 全球通讯簿 \> 登记类型 \> 登记类型**。 创建新登记类型。 将 **国家/地区** 字段指定为 **CZE**（捷克共和国），并将其限制为组织。
2. 转到 **组织管理 \> 全球通讯簿 \> 登记类型 \> 登记类别**。 新建登记类别。 从上一步中选择登记类型，并将 **登记类别** 设置为 **事务所 ID**。
3. 转到 **组织管理 \> 组织 \> 运营单位**。 对于位于捷克共和国的每个商店，请选择与商店相关的单位。 在 **地址** 快速选项卡上，展开 **更多选项** 下拉列表，然后选择 **高级**。 
4. 在打开的 **管理地址** 页面上，必须指定以下设置。

    - 在 **地址** 快速选项卡上，将 **国家/地区** 字段设置为 **CZE**。
    - 在 **登记 ID** 快速选项卡上创建新记录。 选择之前创建的登记类型并设置登记编号。

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>配置自定义字段，以便可以在销售收据中以收据格式使用这些字段

您可以配置以 POS 收据格式使用的语言文本和自定义字段。 创建收据设置的用户的默认公司应是在其中创建语言文本设置的同一法人。 或者，应在用户的默认公司和为其创建设置的商店的法人中创建相同的语言文本。

在 **语言文本** 页面上，为收据布局的自定义字段的标签添加以下记录。 请注意，表中显示的 **语言 ID**、**文本 ID** 和 **文本** 值只是示例。 您可以更改它们以满足您的要求。 但是，您使用的 **文本 ID** 值必须是唯一的，并且它们必须等于或大于 900001。

从表中将以下 POS 标签添加到 **语言文本** 的 **POS 部分**：

| 语言 ID | 文本 ID | 文本                   |
|-------------|---------|------------------------|
| zh-Hans       | 900001  | ID provozovny/pokladny |
| zh-Hans       | 900002  | BKP                    |
| zh-Hans       | 900003  | PKP                    |
| zh-Hans       | 900004  | FIK                    |
| zh-Hans       | 900005  | 信息                   |
| zh-Hans       | 900006  | 序列号        |

在 **自定义字段** 页面上，为收据布局的自定义字段添加以下记录。 请注意，**标题文本 ID** 值必须与您在 **语言文本** 页面上指定的 **文本 ID** 值相对应：

| Name                 | 类型    | 标题文本 ID |
|----------------------|---------|-----------------|
| TLT                  | 收货 | 900001          |
| SEC                  | 收货 | 900002          |
| SIGN                 | 收货 | 900003          |
| FISCAL               | 收货 | 900004          |
| INFO                 | 收货 | 900005          |
| CONTINUOUSNUMBER     | 收货 | 900006          |

> [!NOTE]
> 您必须指定前一表中列出的正确自定义字段名称。 不正确的自定义字段名称将导致收据中缺少数据。

### <a name="configure-receipt-formats"></a>配置收据格式

对于每个必需的收据格式，请将 **打印行为** 字段的值更改为 **始终打印**。

在收据格式设计器中，将以下自定义字段添加到适当的收据部分。 请注意，字段名称与您在上一节中定义的语言文本相对应。

- **标题：** 添加以下字段。

    - **商店名称** 和 **税标识号**：这些字段用于在收据上打印公司名称和标识号。 或者，您可以将公司名称和标识编号以自由格式文本形式添加到布局中。
    - **商店地址**、**日期**、**时间 24H**、**收据编号** 和 **登记编号**。
    - **序列号**：此字段标识会计登记服务中的现金交易记录的编号。

- **行：** 添加以下字段。

    - **物料名称**
    - **数量**
    - **总价（含税）**

- **页脚：** 添加以下字段。

    - 付款字段，以便打印每个付款方式的付款金额。 例如，将 **支付名称** 和 **支付金额** 字段添加到布局的一行中。
    - **ID provozovny/pokladny**：此字段打印事务所和收银机的标识符。
    - **BKP**：此字段打印由会计登记服务分配的纳税人的安全代码。
    - **FIK**：此字段打印由税务主管机构的 Web 服务在成功进行在线登记时分配的交易的会计标识代码。
    - **PKP**：此字段打印纳税人的签名代码，该代码由会计登记服务在脱机登记时生成。
    - **信息**：此字段打印会计登记服务的其他信息。

有关如何使用收据格式的详细信息，请参阅[设置和设计收据格式](../receipt-templates-printing.md)。

## <a name="set-up-fiscal-integration-for-the-czech-republic"></a>设置适用于捷克共和国的会计整合

捷克共和国的会计登记服务集成示例基于[会计整合功能](fiscal-integration-for-retail-channel.md)，是 Retail SDK 的一部分。 该示例位于 [Dynamics 365 Commerce 解决方案](https://github.com/microsoft/Dynamics365Commerce.Solutions/)存储库的 **src\\FiscalIntegration\\Efr** 文件夹中（例如[版本/9.33 中的示例](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)）。 该示例[包含](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services)一个会计单据提供程序（即 Commerce Runtime (CRT) 的扩展），以及一个会计连接器（即 Commerce Hardware Station 的扩展）。 有关如何使用 Retail SDK 的详细信息，请参阅 [Retail SDK 体系结构](../dev-itpro/retail-sdk/retail-sdk-overview.md)和[设置独立包装 SDK 的生成管道](../dev-itpro/build-pipeline.md)。

> [!WARNING]
> 由于[新的独立包装和扩展模型](../dev-itpro/build-pipeline.md)的限制，它当前无法用于此会计整合示例。 您必须在 Microsoft Dynamics Lifecycle Services (LCS) 中的开发人员虚拟机 (VM) 上使用先前版本的 Retail SDK。 有关详细信息，请参阅[捷克共和国会计整合示例的部署准则（旧版）](emea-cze-fi-sample-sdk.md)。
>
> 以后的版本计划支持会计整合示例的新独立包装和扩展模型。

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
    1. 下载 **Configurations \> DocumentProviders \> DocumentProviderFiscalEFRSampleCzech.xml** 中的会计单据提供程序配置文件（例如，[版本/9.33 的文件](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders/DocumentProviderFiscalEFRSampleCzech.xml)）。
    1. 下载 **Configurations \> Connectors \> ConnectorEFRSample.xml** 中的会计连接器配置文件（例如，[版本/9.33 的文件](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml)）。

    > [!WARNING]
    > 由于[新的独立包装和扩展模型](../dev-itpro/build-pipeline.md)的限制，它当前无法用于此会计整合示例。 您必须在 LCS 中的开发人员 VM 上使用先前版本的 Retail SDK。 此会计整合示例的配置文件位于 LCS 中开发人员 VM 上 Retail SDK 的以下文件夹中：
    >
    > - **会计单据提供程序配置文件：** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.EFRSample\\Configuration\\DocumentProviderFiscalEFRSampleCzech.xml
    > - **会计连接器配置文件：** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.EFRSample\\Configuration\\ConnectorEFRSample.xml
    > 
    > 以后的版本计划支持会计整合示例的新独立包装和扩展模型。

1. 转到 **Retail 和 Commerce \> Headquarters 设置 \> 参数 \> Commerce 共享参数**。 在 **常规** 选项卡上，将 **启用会计整合** 选项设置为 **是**。
1. 转到 **Retail 和 Commerce \> 渠道设置 \> 会计整合 \> 会计单据提供程序**，并加载您之前下载的会计单据提供程序配置文件。
1. 转到 **Retail 和 Commerce \> 渠道设置 \> 会计整合 \> 会计连接器**，并加载您之前下载的会计连接器配置文件。
1. 转至 **Retail 和 Commerce \> 渠道设置 \> 会计整合 \> 连接器功能配置文件**。 创建一个新的连接器功能配置文件。 选择您之前加载的文档提供程序和连接器。 根据需要更新[数据映射设置](#default-data-mapping)。
1. 转至 **Retail 和 Commerce \> 渠道设置 \> 会计整合 \> 连接器技术配置文件**。 创建新的连接器技术配置文件，并选择您之前加载的会计连接器。 根据需要更新[连接器设置](#fiscal-connector-settings)。
1. 转至 **Retail 和 Commerce \> 渠道设置 \> 会计整合 \> 会计连接器组**。 为您之前创建的连接器功能配置文件创建一个新的会计连接器组。
1. 转至 **Retail 和 Commerce \> 渠道设置 \> 会计整合 \> 会计登记流程**。 创建新的会计登记流程和一个会计登记流程步骤，并选择您之前创建的会计连接器组。
1. 转至 **Retail 和 Commerce \> 渠道设置 \> POS 设置 \> POS 配置文件 \> 功能配置文件**。 选择链接到应在其中激活登记流程的商店的功能配置文件。 在 **会计登记流程** 快速选项卡上，选择您之前创建的会计登记流程。
1. 转至 **Retail 和 Commerce \> 渠道设置 \> POS 设置 \> POS 配置文件 \> 硬件配置文件**。 选择链接到会计打印机将连接到的 Hardware Station 的硬件配置文件。 在 **会计外围设备** 快速选项卡上，选择您之前创建的连接器技术配置文件。
1. 打开配送计划（**Retail 和 Commerce \> Retail 和 Commerce IT \> 配送计划**），选择作业 **1070** 和 **1090** 以将数据传输到渠道数据库。

#### <a name="default-data-mapping"></a>默认数据映射

作为会计整合示例的一部分提供的会计单据提供程序配置中包含以下默认数据映射：

- **增值税 (VAT) 费率映射** - 为销售税代码设置的纳税百分比值到请求中发送到会计服务的 **TaxG**（税组）属性值的映射。 以下是默认映射：

    ```
    A: 21.00; B: 15.00; C: 10.00; Z: 0.00
    ```

    每个对中的第一个组件都表示 EFR 会计登记服务支持的增值税组。 第二个组件表示相应的增值税税率。 有关 EFR 支持的捷克共和国增值税组的详细信息，请参阅 [EFR 参考](https://public.efsta.net/efr/)。

- **默认增值税组映射** - 无法映射到其中一个预先确定的增值税组的任何增值税金额都将属于默认（基本）增值税组。 以下是默认映射：

    ```
    A
    ```

- **存款增值税组映射** - 客户存款金额和客户订单保证金金额将属于存款增值税组。 以下是默认映射：

    ```
    Z
    ```

#### <a name="fiscal-connector-settings"></a>会计连接器设置

作为会计整合示例的一部分提供的会计连接器配置中包含以下设置：

- **终结点地址** - 会计登记服务的 URL。
- **超时** - 会计连接器等待会计登记服务响应的时长（毫秒）。

### <a name="configure-channel-components"></a>配置渠道组件

> [!WARNING]
> 由于[新的独立包装和扩展模型](../dev-itpro/build-pipeline.md)的限制，它当前无法用于此会计整合示例。 您必须在 LCS 中的开发人员 VM 上使用先前版本的 Retail SDK。 有关详细信息，请参阅[捷克共和国会计整合示例的部署准则（旧版）](emea-cze-fi-sample-sdk.md)。
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
        1. 通过运行以下命令从命令行启动扩展安装程序。

            ```Console
            Contoso.PosFiscalConnectorSample.StoreCommerce.Installer.exe install --verbosity 0
            ```

#### <a name="production-environment"></a>生产环境

按照[为会计整合示例设置生成管道](fiscal-integration-sample-build-pipeline.md)中的步骤生成和发布会计整合示例的 Cloud Scale Unit 和自助可部署包。 可在 [Dynamics 365 Commerce 解决方案](https://github.com/microsoft/Dynamics365Commerce.Solutions)存储库的 **Pipeline\\YAML_Files** 文件夹中找到 **EFR build-pipeline.yml** 模板 YAML 文件。

## <a name="design-of-extensions"></a>扩展设计

捷克共和国的会计登记服务集成示例基于[会计整合功能](fiscal-integration-for-retail-channel.md)，是 Retail SDK 的一部分。 该示例位于 [Dynamics 365 Commerce 解决方案](https://github.com/microsoft/Dynamics365Commerce.Solutions/)存储库的 **src\\FiscalIntegration\\Efr** 文件夹中（例如[版本/9.33 中的示例](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)）。 该示例[包含](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services)一个会计单据提供程序（即 CRT 的扩展），以及一个会计连接器（即 Commerce Hardware Station 的扩展）。 有关如何使用 Retail SDK 的详细信息，请参阅 [Retail SDK 体系结构](../dev-itpro/retail-sdk/retail-sdk-overview.md)和[设置独立包装 SDK 的生成管道](../dev-itpro/build-pipeline.md)。

> [!WARNING]
> 由于[新的独立包装和扩展模型](../dev-itpro/build-pipeline.md)的限制，它当前无法用于此会计整合示例。 您必须在 LCS 中的开发人员 VM 上使用先前版本的 Retail SDK。 有关详细信息，请参阅[捷克共和国会计整合示例的部署准则（旧版）](emea-cze-fi-sample-sdk.md)。 以后的版本计划支持会计整合示例的新独立包装和扩展模型。

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime 扩展设计

作为会计单据提供程序的扩展的目的是生成特定于服务的单据并处理会计登记服务的响应。

#### <a name="request-handler"></a>请求处理程序

单据提供程序有一个 **DocumentProviderEFRFiscalCZE** 请求处理程序，该处理程序用于为会计登记服务生成会计单据。

此处理程序继承自 **INamedRequestHandler** 接口。 **HandlerName** 方法负责返回处理程序的名称。 处理程序名称应与 Commerce Headquarters 中指定的连接器文档提供程序名称匹配。

此连接器支持以下请求。

- **GetFiscalDocumentDocumentProviderRequest** - 此请求包含有关应生成的具体单据的信息。 它返回应在会计登记服务中登记的特定于服务的单据。
- **GetSupportedRegistrableEventsDocumentProviderRequest** - 此请求返回要订阅的事件列表。 当前，支持以下事件：销售、客户帐户存款和客户订单保证金。
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** - 此请求返回会计登记服务的响应。 此响应已序列化以形成字符串，以便可以保存。

#### <a name="configuration"></a>配置

会计单据提供程序的配置文件位于 [Dynamics 365 Commerce 解决方案](https://github.com/microsoft/Dynamics365Commerce.Solutions/)存储库内的 **src\\FiscalIntegration\\Efr\\Configurations\\DocumentProviders\\DocumentProviderFiscalEFRSampleCzech.xml** 中。 此文件的目的是启用要从 Commerce Headquarters 配置的会计单据提供程序的设置。 文件格式符合会计集成配置的要求。

### <a name="hardware-station-extension-design"></a>Hardware Station 扩展设计

作为会计连接器的扩展的目的是与会计登记服务通信。 Hardware Station 扩展使用 HTTP 协议将 CRT 扩展生成的单据提交到会计登记服务。 它还处理从会计登记服务收到的响应。

#### <a name="request-handler"></a>请求处理程序

**EFRHandler** 请求处理程序是处理请求进入会计登记服务的入口点。

此处理程序继承自 **INamedRequestHandler** 接口。 **HandlerName** 方法负责返回处理程序的名称。 处理程序名称应与 Commerce Headquarters 中指定的会计连接器名称匹配。

此连接器支持以下请求。

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
