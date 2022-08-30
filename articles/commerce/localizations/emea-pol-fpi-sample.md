---
title: 波兰税控打印机集成示例
description: 本文提供 Microsoft Dynamics 365 Commerce 中波兰的会计整合示例。
author: EvgenyPopovMBS
ms.date: 08/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-02-01.
ms.openlocfilehash: 52710252d78d34c444de2d40e16423868b12b5c1
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336637"
---
# <a name="fiscal-printer-integration-sample-for-poland"></a>波兰税控打印机集成示例

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

本文提供 Microsoft Dynamics 365 Commerce 中波兰的会计整合示例。

波兰的 Dynamics 365 Commerce 功能包括销售点 (POS) 与会计打印机的示例集成。 该示例扩展[会计整合功能](fiscal-integration-for-retail-channel.md)，并支持 [Posnet Polska S.A](https://www.posnet.com.pl) 中会计打印机的 POSNET 2.02 协议。该示例允许使用本机软件驱动程序与通过 COM 端口连接的会计打印机进行通信。 它是通过使用 Posnet 为 Posnet Thermal HD FV EJ 会计打印机提供的软件模拟器来实现和测试的。 该示例以源代码的形式提供，是 Commerce 软件开发工具包 (SDK) 的一部分。

Microsoft 不会从 Posnet 发布任何硬件、软件或文档。 有关如何获取会计打印机并对其进行操作的信息，请与 [Posnet Polska S.A](https://www.posnet.com.pl) 联系

## <a name="scenarios"></a>方案

波兰的会计打印机集成示例涵盖以下方案：

- 销售方案：

    - 打印现金和结转销售和退货的会计收据。
    - 从会计打印机捕获响应并将其存储到渠道数据库中。
    - 税金:

        - 映射到会计打印机的税码（部门）。
        - 将映射的税务数据转移到会计打印机。

    - 付款：

        - 映射到会计打印机的付款方式。
        - 打印会计收据上的付款。
        - 打印更改信息。

    - 打印行折扣。
    - 礼品卡:

        - 从销售会计收据中排除已签发/充值的礼品卡行。
        - 打印使用礼品卡作为常规付款方式的付款。

    - 打印客户订单操作的会计收据：

        - 不打印客户订单保证金的会计收据。
        - 打印混合客户订单的结转行的会计收据。
        - 打印客户订单的提货操作的会计收据。
        - 打印退货单的会计收据。

    - 打印为会计收据上的销售交易指定的[客户信息](emea-pol-customer-information.md)。 此信息的一个示例是客户的增值税编号。

- 日末对帐单（会计 X 和会计 Z 报表）。
- 错误处理，如以下选项：

    - 如果可以重试，请重试会计登记，例如，如果会计打印机未连接、未准备好或未响应，打印机缺纸或卡纸。
    - 推迟会计登记。
    - 跳过会计登记，或将交易标记为已登记，并包括信息代码以捕获失败的原因和其他信息。
    - 在新销售交易打开或完成销售交易之前，检查会计打印机的可用性。

### <a name="gift-cards"></a>礼品卡

会计打印机集成示例实施与礼品卡相关的以下规则：

- 从会计收据中排除与 *签发礼品卡* 和 *添加到礼品卡* 操作相关的销售行。
- 如果会计收据仅由礼品卡行构成，则不打印会计收据。
- 从会计收据付款行中扣除交易中签发或充值的礼品卡的总金额。
- 参考相应的会计交易，在渠道数据库中保存付款行的计算调整。
- 用礼品卡进行的付款被视为常规付款。

### <a name="customer-deposits-and-customer-order-deposits"></a>客户存款和客户订单保证金

会计打印机集成示例实施与客户存款和客户订单保证金相关的以下规则：

- 如果交易是客户存款，则不打印会计收据。
- 如果交易仅包含客户订单保证金或客户订单保证金退款，则不打印会计收据。
- 打印客户订单提货操作会计收据上以前支付的保证金金额。
- 创建混合客户订单时，从付款行中扣除客户订单保证金金额。
- 参考混合客户订单的会计交易，在渠道数据库中保存付款行的计算调整。

### <a name="limitations-of-the-sample"></a>示例的限制

- 会计打印机仅支持价格中包含销售税的方案。 因此，必须针对商店和客户将 **价格包括销售税** 选项设置为 **是**。
- 使用嵌入式 *班次报表* 格式打印每日报表（会计 X 和会计 Z）。
- 在会计收据上打印条码被认为是一种可能的自定义项，因为嵌入式格式不支持此功能，并且只能使用可自定义的 **超级格式** 报表来实现此功能。
- 会计打印机不支持混合交易。 在 POS 功能配置文件中，**禁止在一份收据中混合销售和退货** 选项应设置为 **是**。

## <a name="set-up-fiscal-integration-for-poland"></a>设置波兰的会计整合

波兰的会计打印机集成示例基于[会计整合功能](fiscal-integration-for-retail-channel.md)，是 Commerce SDK 的一部分。 示例位于 [Dynamics 365 Commerce 解决方案](https://github.com/microsoft/Dynamics365Commerce.Solutions/)存储库的 **src\\FiscalIntegration\\Posnet** 文件夹中。 [示例](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services)中包含一个会计单据提供程序（即 Commerce Runtime (CRT) 的扩展），以及一个会计连接器（即 Commerce Hardware Station 的扩展）。 有关如何使用 Commerce SDK 的详细信息，请参阅[从 GitHub 和 NuGet 下载 Commerce SDK 示例和引用包](../dev-itpro/retail-sdk/sdk-github.md)和[设置独立包装 SDK 的生成管道](../dev-itpro/build-pipeline.md)。

> [!NOTE]
> 从 Commerce 版本 10.0.29 开始，可以在 Commerce SDK 中找到波兰的会计打印机集成示例。 在 Commerce 版本 10.0.28 或更早版本中，您必须在 Microsoft Dynamics Lifecycle Services (LCS) 中的开发人员虚拟机 (VM) 上使用先前版本的 Retail SDK。 有关详细信息，请参阅[波兰会计打印机整合示例的部署准则（旧版）](emea-pol-fpi-sample-sdk.md)。

完成会计整合设置步骤，如[设置 Commerce 渠道的会计整合](setting-up-fiscal-integration-for-retail-channel.md)中所述。

1. [设置会计登记流程](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process)。 此外，请记下[特定于此会计打印机整合示例](#set-up-the-registration-process)的会计登记流程的设置。
1. [设置错误处理设置](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings)。
1. [从 POS 设置会计 X/Z 报表](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos)。
1. [启用已推迟会计登记的手动执行](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration)。
1. [配置渠道组件](#configure-channel-components)。

### <a name="set-up-the-registration-process"></a>设置登记流程

要启用登记流程，请按照以下步骤设置 Commerce Headquarters。 有关详细信息，请参阅[设置 Commerce 渠道的会计整合](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process)。

1. 下载会计单据提供程序和会计连接器的配置文件：

    1. 打开 [Dynamics 365 Commerce 解决方案](https://github.com/microsoft/Dynamics365Commerce.Solutions/)存储库。
    1. 根据您的 SDK/应用程序版本选择正确的发布分支版本。
    1. 打开 **src \> FiscalIntegration \> Posnet**。
    1. 下载 **CommerceRuntime \> DocumentProvider.PosnetSample \> 配置 \> DocumentProviderPosnetSample.xml** 中的会计单据提供程序配置文件。
    1. 下载 **HardwareStation \> ThermalDeviceSample \> 配置 \> ConnectorPosnetThermalFVEJ.xml** 中的会计连接器配置文件。

    > [!NOTE]
    > 在 Commerce 版本 10.0.28 或更早版本中，您必须在 LCS 中的开发人员 VM 上使用先前版本的 Retail SDK。 此会计整合示例的配置文件位于 LCS 中开发人员 VM 上 Retail SDK 的以下文件夹中：
    >
    > - **会计单据提供程序配置文件：** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extension.DocumentProvider.PosnetSample\\Configuration\\DocumentProviderPosnetSample.xml
    > - **会计连接器配置文件：** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.Posnet.ThermalDeviceSample\\Configuration\\ConnectorPosnetThermalFVEJ.xml

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

- **增值税 (VAT) 费率映射** - 为销售税代码设置的纳税百分比值到会计打印机特定增值税税率的映射。 以下是默认映射：

    ```
    0 : 23.00 ; 1 : 8.00 ; 2 : 5.00 ; 3 : 0.00
    ```

    每个对中的第一个组件都表示会计打印机中配置的增值税税率数字。 第二个组件表示相应的增值税税率。 有关会计打印机增值税税率配置的详细信息，请参阅 POSNET 驱动程序文档。

- **支付方式映射** - 为商店配置的付款方式到会计打印机支持的付款形式的映射。 以下是默认映射：

    ```
    0 : 0 ; 1 : 0 ; 2 : 2 ; 3 : 2 ; 4 : 0 ; 5 : 0 ; 6 : 0 ; 7 : 2 ; 8 : 0
    ```

    每个对中的第一个组件都表示为商店设置的付款方式。 第二个组件表示会计打印机支持的相应付款形式。 有关会计打印机支持的付款形式的详细信息，请参阅 POSNET 驱动程序文档。 您必须根据应用程序中配置的付款方式修改示例映射。

#### <a name="fiscal-connector-settings"></a>会计连接器设置

作为会计整合示例的一部分提供的会计连接器配置中包含以下设置：

- **连接字符串** - 一个以驱动程序支持的格式描述设备连接详细信息的字符串。 有关详细信息，请参阅 POSNET 驱动程序文档。
- **日期和时间同步** - 一个指定打印机的日期和时间是否必须与连接的 Hardware Station 同步的值。
- **设备超时** - 驱动程序等待设备响应的时长（毫秒）。 有关详细信息，请参阅 POSNET 驱动程序文档。

### <a name="configure-channel-components"></a>配置渠道组件

> [!NOTE]
> - 从 Commerce 版本 10.0.29 开始，可以在 Commerce SDK 中找到波兰的会计打印机集成示例。 在 Commerce 版本 10.0.28 或更早版本中，您必须在 LCS 中的开发人员 VM 上使用先前版本的 Retail SDK。 有关详细信息，请参阅[波兰会计打印机整合示例的部署准则（旧版）](emea-pol-fpi-sample-sdk.md)。
> - 当您将服务或质量更新应用于 Commerce 组件时，部署在您的环境中的 Commerce 示例不会自动更新。 您必须手动更新所需示例。

#### <a name="set-up-the-development-environment"></a>设置开发环境

若要设置开发环境以测试和扩展示例，请按照以下步骤操作。

1. 克隆或下载 [Dynamics 365 Commerce 解决方案](https://github.com/microsoft/Dynamics365Commerce.Solutions)存储库。 根据您的 SDK/应用程序版本选择正确的发布分支版本。 有关详细信息，请参阅[从 GitHub 和 NuGet 下载 Commerce SDK 示例和引用包](../dev-itpro/retail-sdk/sdk-github.md)。
1. 在 **Dynamics365Commerce.Solutions\\FiscalIntegration\\Posnet\\Posnet.sln** 中打开会计打印机集成解决方案，然后构建它。
1. 安装 CRT 扩展：

    1. 查找 CRT 扩展安装程序：

        - **Commerce Scale Unit：** 在 **Posnet\\ScaleUnit\\ScaleUnit.Posnet.Installer\\bin\\Debug\\net461** 文件夹中，查找 **ScaleUnit.Posnet.Installer** 安装程序。
        - **Modern POS 上的本地 CRT：** 在 **Posnet\\ModernPOS\\ModernPOS.Posnet.Installer\\bin\\Debug\\net461** 文件夹中，查找 **ModernPOS.Posnet.Installer** 安装程序。

    1. 从命令行启动 CRT 扩展安装程序：

        - **Commerce Scale Unit：**

            ```Console
            ScaleUnit.Posnet.Installer.exe install --verbosity 0
            ```

        - **Modern POS 上的本地 CRT：**

            ```Console
            ModernPOS.Posnet.Installer.exe install --verbosity 0
            ```

1. 安装 Hardware Station 扩展：

    1. 在 **Posnet\\HardwareStation\\HardwareStation.PosnetThermalFVFiscalPrinter.Installer\\bin\\Debug\\net461** 文件夹中，查找 **HardwareStation.PosnetThermalFVFiscalPrinter.Installer** 安装程序。
    1. 从命令行启动扩展安装程序：

        ```Console
        HardwareStation.PosnetThermalFVFiscalPrinter.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>生产环境

按照[为会计整合示例设置生成管道](fiscal-integration-sample-build-pipeline.md)中的步骤生成和发布会计整合示例的 Cloud Scale Unit 和自助可部署包。 可在 [Dynamics 365 Commerce 解决方案](https://github.com/microsoft/Dynamics365Commerce.Solutions)存储库的 **Pipeline\\YAML_Files** 文件夹中找到 **Posnet build-pipeline.yml** 模板 YAML 文件。

## <a name="design-of-extensions"></a>扩展设计

波兰的会计打印机集成示例基于[会计整合功能](fiscal-integration-for-retail-channel.md)，是 Commerce SDK 的一部分。 示例位于 [Dynamics 365 Commerce 解决方案](https://github.com/microsoft/Dynamics365Commerce.Solutions/)存储库的 **src\\FiscalIntegration\\Posnet** 文件夹中。 [示例](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services)中包含一个会计单据提供程序（即 CRT 的扩展），以及一个会计连接器（即 Commerce 硬件工作站的扩展）。 有关如何使用 Commerce SDK 的详细信息，请参阅[从 GitHub 和 NuGet 下载 Commerce SDK 示例和引用包](../dev-itpro/retail-sdk/sdk-github.md)和[设置独立包装 SDK 的生成管道](../dev-itpro/build-pipeline.md)。

> [!NOTE]
> 从 Commerce 版本 10.0.29 开始，可以在 Commerce SDK 中找到波兰的会计打印机集成示例。 在 Commerce 版本 10.0.28 或更早版本中，您必须在 LCS 中的开发人员 VM 上使用先前版本的 Retail SDK。 有关详细信息，请参阅[波兰会计打印机整合示例的部署准则（旧版）](emea-pol-fpi-sample-sdk.md)。

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime 扩展设计

作为会计单据提供程序的扩展的目的是生成特定于打印机的单据并处理会计打印机的响应。 此扩展以 POSNET 规格 19-3678 定义的 JavaScript 对象表示法 (JSON) 格式生成一组特定于打印机的命令。

#### <a name="request-handler"></a>请求处理程序

**DocumentProviderPosnetProtocol** 请求处理程序是关于从会计打印机生成单据的请求的入口点。

此处理程序继承自 **INamedRequestHandler** 接口。 **HandlerName** 方法负责返回处理程序的名称。 处理程序名称应与 Commerce Headquarters 中指定的连接器文档提供程序名称匹配。

此连接器支持以下请求：

- **GetFiscalDocumentDocumentProviderRequest** - 此请求包含有关应生成的具体单据的信息。 它返回应在会计打印机中登记的特定于打印机的单据。
- **GetSupportedRegistrableEventsDocumentProviderRequest** - 此请求返回要订阅的事件列表。 当前，支持以下事件：销售、打印 X 报表和打印 Z 报表。

#### <a name="configuration"></a>配置

会计单据提供程序的配置文件位于 [Dynamics 365 Commerce 解决方案](https://github.com/microsoft/Dynamics365Commerce.Solutions/)存储库内的 **src\\FiscalIntegration\\Posnet\\CommerceRuntime\\DocumentProvider.PosnetSample\\Configuration\\DocumentProviderPosnetSample.xml** 中。 此文件的目的是启用要从 Commerce Headquarters 配置的会计单据提供程序的设置。 文件格式符合会计集成配置的要求。

### <a name="hardware-station-extension-design"></a>Hardware Station 扩展设计

作为会计连接器的扩展的目的是与会计打印机通信。 此扩展调用 POSNET 驱动程序的函数以将 CRT扩展生成的命令提交到会计打印机。 它还处理设备错误。

#### <a name="request-handler"></a>请求处理程序

**FiscalPrinterHandler** 请求处理程序是用于处理发送给会计外围设备的请求的入口点。

此处理程序继承自 **INamedRequestHandler** 接口。 **HandlerName** 方法负责返回处理程序的名称。 处理程序名称应与 Commerce Headquarters 中指定的会计连接器名称匹配。

此连接器支持以下请求：

- **SubmitDocumentFiscalDeviceRequest** - 此请求将单据发送到打印机并返回会计打印机的响应。
- **IsReadyFiscalDeviceRequest** - 此请求用于检查设备运行状况。
- **InitializeFiscalDeviceRequest** - 此请求用于打印机初始化。

#### <a name="configuration"></a>配置

会计连接器的配置文件位于 [Dynamics 365 Commerce 解决方案](https://github.com/microsoft/Dynamics365Commerce.Solutions/)存储库内的 **src\\FiscalIntegration\\Posnet\\HardwareStation\\ThermalDeviceSample\\Configuration\\ConnectorPosnetThermalFVEJ.xml** 中。 此文件的目的是启用要从 Commerce Headquarters 配置的会计连接器的设置。 文件格式符合会计集成配置的要求。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
