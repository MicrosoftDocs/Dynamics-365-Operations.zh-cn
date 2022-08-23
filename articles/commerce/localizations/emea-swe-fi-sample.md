---
title: 瑞典的控制单元集成示例
description: 本文提供 Microsoft Dynamics 365 Commerce 中瑞典的会计整合示例。
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-08
ms.openlocfilehash: 3376e6a901b692371a44b5c74c1e6b4afd0cd573
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275058"
---
# <a name="control-unit-integration-sample-for-sweden"></a>瑞典的控制单元集成示例

[!include [banner](../includes/banner.md)]

本文提供 Microsoft Dynamics 365 Commerce 中瑞典的会计整合示例。

> [!NOTE]
> 此示例会计整合功能将取代早期的 [POS 与瑞典的控制单元集成的示例](retail-sdk-control-unit-sample.md)。 早期示例没有利用[会计整合框架](./fiscal-integration-for-retail-channel.md)，并且将在以后的更新中过时。 有关如何从早期示例迁移到与 Dynamics 365 Commerce 版本 **10.0.22 和早期版本** 相对应的示例的信息，请参阅[从早期集成示例迁移](emea-swe-fi-sample-sdk.md#migrating-from-the-earlier-integration-sample)。

瑞典的 Commerce 功能包括销售点 (POS) 与瑞典特定会计设备（称为 *控制单元*）的示例集成。 该示例扩展了[会计集成功能](fiscal-integration-for-retail-channel.md)。 假定控制单元已实际连接到 POS 与之配对的 Hardware Station。 例如，此示例使用零售创新 HTT AB 的 [CleanCash 类型 A](https://www.retailinnovation.se/produkter) 控制单元的应用程序编程界面 (API)。 已使用 CleanCash API 版本 1.1.4。

该示例以源代码的形式提供，是 Retail 软件开发工具包 (SDK) 的一部分。

Microsoft 不会从零售创新 HTT AB 发布任何硬件、软件或文档。 有关如何获取控制单元并对其进行操作的信息，请与[零售创新 HTT AB](https://www.retailinnovation.se/) 联系。

## <a name="scenarios"></a>方案

瑞典的控制单元集成示例包括以下功能：

- 销售、退货和收据副本将自动登记在连接到与 POS 配对的 Hardware Station 的控制单元中。
- 已登记交易的控制单元的控制代码和制造编号从控制单元中捕获并保存在交易中。 此数据也称为 *会计响应*。 可以在 **商店交易** 页上查看会计响应。
- 可将控制代码的自定义字段和控制单元的制造编号添加到收据布局中。 这样，您可以打印收据上交易的会计响应。
- 交易的会计响应显示在 **电子日记帐（瑞典）** 渠道报表上。
- 有多个错误处理选项可用。 下面举了一些示例加以说明：

    - 如果可以重试，则重试会计登记。 如果控制单元未连接、未准备就绪或未响应，则可以重试会计登记。
    - 推迟会计登记。
    - 跳过会计登记，或将交易标记为已登记，并包括信息代码以捕获失败的原因和其他信息。
    - 在新销售交易打开或完成销售交易之前，验证控制单元的可用性。

### <a name="limitations-of-the-sample"></a>示例的限制

瑞典的控制单元集成示例当前不支持客户订单方案。

## <a name="setting-up-the-integration-with-control-units"></a>设置与控制单元的集成

有关瑞典所需的设置的详细信息，请参阅[为瑞典设置 Commerce](./emea-swe-cash-registers.md#setting-up-commerce-for-sweden)。

### <a name="configuring-swedenspecific-receipts"></a>配置特定于瑞典的收据

#### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>配置自定义字段，以便可以在销售收据中以收据格式使用这些字段

您可以配置以 POS 收据格式使用的语言文本和自定义字段。 创建收据设置的用户的默认公司应是在其中创建语言文本设置的同一法人。 或者，应在用户的默认公司和为其创建设置的商店的法人中创建相同的语言文本。

在 **语言文本** 页面上，为收据布局的自定义字段的标签添加以下记录。 请注意，表中显示的 **语言 ID**、**文本 ID** 和 **文本** 值只是示例。 您可以更改它们以满足您的要求。 但是，您使用的 **文本 ID** 值必须是唯一的，并且它们必须等于或大于 900001。

将以下 POS 标签添加到 **语言文本** 页面的 **POS** 部分。

| 语言 ID | 文本 ID | 文本                  |
|-------------|---------|-----------------------|
| zh-Hans       | 900001  | 登记控制代码 |
| zh-Hans       | 900002  | 登记设备       |

在 **自定义字段** 页面上，为收据布局的自定义字段添加以下记录。 请注意，**标题文本 ID** 值必须与您在 **语言文本** 页面上指定的 **文本 ID** 值相对应。

| Name                         | 类型    | 标题文本 ID |
|------------------------------|---------|-----------------|
| SE_FISCALREGISTERCONTROLCODE | 收货 | 900001          |
| SE_FISCALREGISTERID          | 收货 | 900002          |

> [!NOTE]
> 您必须指定上表中列出的正确自定义字段名称。 不正确的自定义字段名称将导致收据中缺少数据。

#### <a name="configure-receipt-formats"></a>配置收据格式

对于每个必需的收据格式，请将 **打印行为** 字段的值更改为 **始终打印**。

在收据格式设计器中，将以下自定义字段添加到 **页脚** 部分。 请注意，字段名称与您在本文上一节中定义的语言文本相对应。

- **登记控制代码** - 此字段打印控制代码。
- **登记设备** - 此字段打印控制单元的制造编号。

有关如何使用收据格式的详细信息，请参阅[收据模板和打印](../receipt-templates-printing.md)。

### <a name="set-up-fiscal-integration-for-sweden"></a>设置瑞典的会计整合

瑞典的控制单元集成示例基于[会计整合功能](fiscal-integration-for-retail-channel.md)，是 Retail SDK 的一部分。 该示例位于 [Dynamics 365 Commerce 解决方案](https://github.com/microsoft/Dynamics365Commerce.Solutions/)存储库的 **src\\FiscalIntegration\\CleanCash** 文件夹中（例如[版本/9.33 中的示例](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/CleanCash)）。 该示例[包含](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services)一个会计单据提供程序（即 Commerce Runtime (CRT) 的扩展），以及一个会计连接器（即 Commerce Hardware Station 的扩展）。 有关如何使用 Retail SDK 的详细信息，请参阅 [Retail SDK 体系结构](../dev-itpro/retail-sdk/retail-sdk-overview.md)和[设置独立包装 SDK 的生成管道](../dev-itpro/build-pipeline.md)。

> [!WARNING]
> 由于[新的独立包装和扩展模型](../dev-itpro/build-pipeline.md)的限制，它当前无法用于此会计整合示例。 您必须在 Microsoft Dynamics Lifecycle Services (LCS) 中的开发人员虚拟机 (VM) 上使用先前版本的 Retail SDK。 有关详细信息，请参阅[瑞典控制单元整合示例的部署准则（旧版）](emea-swe-fi-sample-sdk.md)。
>
> 以后的版本计划支持会计整合示例的新独立包装和扩展模型。

完成会计整合设置步骤，如[设置 Commerce 渠道的会计整合](setting-up-fiscal-integration-for-retail-channel.md)中所述。

1. [设置会计登记流程](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process)。 此外，请记下[特定于此控制单元整合示例](#set-up-the-registration-process)的会计登记流程的设置。
1. [设置错误处理设置](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings)。
1. [启用已推迟会计登记的手动执行](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration)。
1. [配置渠道组件](#configure-channel-components)。

### <a name="set-up-the-registration-process"></a>设置登记流程

要启用登记流程，请按照以下步骤设置 Commerce Headquarters。 有关详细信息，请参阅[设置 Commerce 渠道的会计整合](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process)。

1. 下载会计单据提供程序和会计连接器的配置文件：

    1. 打开 [Dynamics 365 Commerce 解决方案](https://github.com/microsoft/Dynamics365Commerce.Solutions/)存储库。
    1. 根据您的 SDK/应用程序版本（例如 **[版本/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**）选择正确的发布分支版本。
    1. 打开 **src \> FiscalIntegration \> CleanCash**。
    1. 下载 **CommerceRuntime \> DocumentProvider.CleanCashSample \> Configuration \> DocumentProviderFiscalCleanCashSample.xml** 中的会计单据提供程序配置文件（例如，[版本/9.33 的文件](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/CleanCash/CommerceRuntime/DocumentProvider.CleanCashSample/Configuration/DocumentProviderFiscalCleanCashSample.xml)）。
    1. 下载 **HardwareStation \> Connector.CleanCashSample \> Configuration \> ConnectorCleanCashSample.xml** 中的会计连接器配置文件（例如，[版本/9.33 的文件](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/CleanCash/HardwareStation/Connector.CleanCashSample/Configuration/ConnectorCleanCashSample.xml)）。

    > [!WARNING]
    > 由于[新的独立包装和扩展模型](../dev-itpro/build-pipeline.md)的限制，它当前无法用于此会计整合示例。 您必须在 LCS 中的开发人员 VM 上使用先前版本的 Retail SDK。 此会计整合示例的配置文件位于 LCS 中开发人员 VM 上 Retail SDK 的以下文件夹中：
    >
    > - **会计单据提供程序配置文件：** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.CleanCashSample\\Configuration\\DocumentProviderFiscalCleanCashSample.xml
    > - **会计连接器配置文件：** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.CleanCashSample\\Configuration\\ConnectorCleanCashSample.xml
    > 
    > 以后的版本计划支持会计整合示例的新独立包装和扩展模型。

1. 转到 **Retail 和 Commerce \> Headquarters 设置 \> 参数 \> Commerce 共享参数**。 在 **常规** 选项卡上，将 **启用会计整合** 选项设置为 **是**。
1. 转到 **Retail 和 Commerce \> 渠道设置 \> 会计整合 \> 会计单据提供程序**，并加载您之前下载的会计单据提供程序配置文件。
1. 转到 **Retail 和 Commerce \> 渠道设置 \> 会计整合 \> 会计连接器**，并加载您之前下载的会计连接器配置文件。
1. 转至 **Retail 和 Commerce \> 渠道设置 \> 会计整合 \> 连接器功能配置文件**。 创建一个新的连接器功能配置文件。 选择您之前加载的文档提供程序和连接器。 根据需要更新[数据映射设置](#default-data-mapping)。
1. 转至 **Retail 和 Commerce \> 渠道设置 \> 会计整合 \> 连接器技术配置文件**。 创建新的连接器技术配置文件，并选择您之前加载的会计连接器。 根据需要更新[连接器设置](#fiscal-connector-settings)。
6. 转至 **Retail 和 Commerce \> 渠道设置 \> 会计整合 \> 会计连接器组**。 为您之前创建的连接器功能配置文件创建一个新的会计连接器组。
7. 转至 **Retail 和 Commerce \> 渠道设置 \> 会计整合 \> 会计登记流程**。 创建新的会计登记流程和一个会计登记流程步骤，并选择您之前创建的会计连接器组。
8. 转至 **Retail 和 Commerce \> 渠道设置 \> POS 设置 \> POS 配置文件 \> 功能配置文件**。 选择链接到应在其中激活登记流程的商店的功能配置文件。 在 **会计登记流程** 快速选项卡上，选择您之前创建的会计登记流程。
9. 转至 **Retail 和 Commerce \> 渠道设置 \> POS 设置 \> POS 配置文件 \> 硬件配置文件**。 选择链接到会计打印机将连接到的 Hardware Station 的硬件配置文件。 在 **会计外围设备** 快速选项卡上，选择您之前创建的连接器技术配置文件。
10. 打开配送计划（**Retail 和 Commerce \> Retail 和 Commerce IT \> 配送计划**），选择作业 **1070** 和 **1090** 以将数据传输到渠道数据库。

#### <a name="default-data-mapping"></a>默认数据映射

作为会计整合示例的一部分提供的会计单据提供程序配置中包含以下默认数据映射：

- **增值税 (VAT) 代码映射** - 此映射将设备特定的增值税 (VAT) 代码设置为相应的销售税代码。 增值税代码映射应具有以下格式：

    ```
    1 : code1 ; 2 : code2
    ```

    下面是对此格式的说明：

    - *1* 和 *2* 是设备特定的增值税代码。
    - 分号 (;) 用作分隔符。
    - *code1* 和 *code2* 是在 Commerce Headquarters 中配置的销售税代码。 您必须根据应用程序中配置的税码修改示例映射。

    控制单元最多支持四个不同的增值税代码。 因此，可能以以下方式设置增值税代码映射：

    ```
    1 : code1 ; 2 : code2 ; 3 : code3 ; 4 : code4
    ```

    > [!NOTE]
    > 多个销售税代码可以映射到同一设备特定增值税代码。

#### <a name="fiscal-connector-settings"></a>会计连接器设置

作为会计整合示例的一部分提供的会计连接器配置中包含以下设置：

- **连接字符串** - 控制单元连接设置。
- **超时** - 驱动程序等待控制单元响应的时长（毫秒）。

### <a name="configure-channel-components"></a>配置渠道组件

> [!WARNING]
> 由于[新的独立包装和扩展模型](../dev-itpro/build-pipeline.md)的限制，它当前无法用于此会计整合示例。 您必须在 LCS 中的开发人员 VM 上使用先前版本的 Retail SDK。 有关详细信息，请参阅[瑞典控制单元整合示例的部署准则（旧版）](emea-swe-fi-sample-sdk.md)。
>
> 以后的版本计划支持会计整合示例的新独立包装和扩展模型。

#### <a name="set-up-the-development-environment"></a>设置开发环境

若要设置开发环境以测试和扩展示例，请按照以下步骤操作。

1. 克隆或下载 [Dynamics 365 Commerce 解决方案](https://github.com/microsoft/Dynamics365Commerce.Solutions)存储库。 根据您的 SDK/应用程序版本选择正确的发布分支版本。 有关详细信息，请参阅[从 GitHub 和 NuGet 下载 Retail SDK 示例和引用包](../dev-itpro/retail-sdk/sdk-github.md)。
1. 在 **Dynamics365Commerce.Solutions\\FiscalIntegration\\CleanCash\\CleanCash.sln** 中打开控制单元集成解决方案，然后构建它。
1. 安装 CRT 扩展：

    1. 查找 CRT 扩展安装程序：

        - **Commerce Scale Unit：** 在 **CleanCash\\ScaleUnit\\ScaleUnit.CleanCash.Installer\\bin\\Debug\\net461** 文件夹中，查找 **ScaleUnit.CleanCash.Installer** 安装程序。
        - **Modern POS 上的本地 CRT：** 在 **CleanCash\\ModernPOS\\ModernPOS.CleanCash.Installer\\bin\\Debug\\net461** 文件夹中，查找 **ModernPOS.CleanCash.Installer** 安装程序。

    2. 从命令行启动 CRT 扩展安装程序：

        - **Commerce Scale Unit：**

            ```Console
            ScaleUnit.CleanCash.Installer.exe install --verbosity 0
            ```

        - **Modern POS 上的本地 CRT：**

            ```Console
            ModernPOS.CleanCash.Installer.exe install --verbosity 0
            ```

1. 安装 Hardware Station 扩展：

    1. Modern POS 上的本地 ：在 **CleanCash\\HardwareStation\\HardwareStation.CleanCash.Installer\\bin\\Debug\\net461** 文件夹中，查找 **HardwareStation.CleanCash.Installer** 安装程序。
    1. 从命令行启动扩展安装程序：

        ```Console
        HardwareStation.CleanCash.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>生产环境

按照[为会计整合示例设置生成管道](fiscal-integration-sample-build-pipeline.md)中的步骤生成和发布会计整合示例的 Cloud Scale Unit 和自助可部署包。 可在 [Dynamics 365 Commerce 解决方案](https://github.com/microsoft/Dynamics365Commerce.Solutions)存储库的 **Pipeline\\YAML_Files** 文件夹中找到 **CleanCash build-pipeline.yml** 模板 YAML 文件。

## <a name="design-of-the-extensions"></a>扩展设计

瑞典的控制单元集成示例基于[会计整合功能](fiscal-integration-for-retail-channel.md)，是 Retail SDK 的一部分。 该示例位于 [Dynamics 365 Commerce 解决方案](https://github.com/microsoft/Dynamics365Commerce.Solutions/)存储库的 **src\\FiscalIntegration\\CleanCash** 文件夹中（例如[版本/9.33 中的示例](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/CleanCash)）。 该示例[包含](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services)一个会计单据提供程序（即 CRT 的扩展），以及一个会计连接器（即 Commerce Hardware Station 的扩展）。 有关如何使用 Retail SDK 的详细信息，请参阅 [Retail SDK 体系结构](../dev-itpro/retail-sdk/retail-sdk-overview.md)和[设置独立包装 SDK 的生成管道](../dev-itpro/build-pipeline.md)。

> [!WARNING]
> 由于[新的独立包装和扩展模型](../dev-itpro/build-pipeline.md)的限制，它当前无法用于此会计整合示例。 您必须在 LCS 中的开发人员 VM 上使用先前版本的 Retail SDK。 有关详细信息，请参阅[瑞典控制单元整合示例的部署准则（旧版）](emea-swe-fi-sample-sdk.md)。 以后的版本计划支持会计整合示例的新独立包装和扩展模型。

### <a name="crt-extension-design"></a>CRT 扩展设计

作为会计单据提供程序的扩展的目的是生成特定于服务的单据并处理控制单元的响应。

#### <a name="request-handler"></a>请求处理程序

文档提供程序有一个 **DocumentProviderCleanCash** 请求处理程序。 此处理程序用于为控制单元生成会计单据。

此处理程序继承自 **INamedRequestHandler** 接口。 **HandlerName** 方法负责返回处理程序的名称。 处理程序名称应与 Commerce Headquarters 中指定的连接器文档提供程序名称匹配。

此连接器支持以下请求：

- **GetFiscalDocumentDocumentProviderRequest** - 此请求包含有关应生成的具体单据的信息。 它返回应在控制单元中登记的特定于服务的单据。
- **GetSupportedRegistrableEventsDocumentProviderRequest** - 此请求返回要订阅的事件列表。 当前，销售事件和审计事件均受支持。

#### <a name="configuration"></a>配置

会计单据提供程序的配置文件位于 [Dynamics 365 Commerce 解决方案](https://github.com/microsoft/Dynamics365Commerce.Solutions/)存储库内的 **src\\FiscalIntegration\\CleanCash\\CommerceRuntime\\DocumentProvider.CleanCashSample\\Configuration\\DocumentProviderFiscalCleanCashSample.xml** 中。 此文件的目的是启用要从 Commerce Headquarters 配置的单据提供程序的设置。 文件格式符合会计集成配置的要求。

### <a name="hardware-station-extension-design"></a>Hardware Station 扩展设计

作为会计连接器的扩展的目的是与控制单元通信。 它使用 HTTP 协议将 CRT 扩展生成的单据提交到控制单元。 它还处理从控制单元收到的响应。

#### <a name="request-handler"></a>请求处理程序

**CleanCashHandler** 请求处理程序是处理请求进入控制单元的入口点。

此处理程序继承自 **INamedRequestHandler** 接口。 **HandlerName** 方法负责返回处理程序的名称。 处理程序名称应与 Commerce Headquarters 中指定的会计连接器名称匹配。

此连接器支持以下请求：

- **SubmitDocumentFiscalDeviceRequest** - 此请求将单据发送到控制单元并返回控制单元的响应。
- **IsReadyFiscalDeviceRequest** - 此请求用于检查控制单元运行状况。
- **InitializeFiscalDeviceRequest** - 此请求用于初始化控制单元。

#### <a name="configuration"></a>配置

会计连接器的配置文件位于 [Dynamics 365 Commerce 解决方案](https://github.com/microsoft/Dynamics365Commerce.Solutions/)存储库内的 **src\\FiscalIntegration\\CleanCash\\HardwareStation\\Connector.CleanCashSample\\Configuration\\ConnectorCleanCashSample.xml** 中。 此文件的目的是启用要从 Commerce Headquarters 配置的会计连接器的设置。 文件格式符合会计集成配置的要求。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
