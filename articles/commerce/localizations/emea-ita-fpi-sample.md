---
title: 意大利税控打印机集成示例
description: 本文提供 Microsoft Dynamics 365 Commerce 中意大利的会计整合示例。
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2018-11-1
ms.openlocfilehash: 2aa1851fe5fe447ba2dd4640be9881b37e54216e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909382"
---
# <a name="fiscal-printer-integration-sample-for-italy"></a>意大利税控打印机集成示例

[!include[banner](../includes/banner.md)]

本文提供 Microsoft Dynamics 365 Commerce 中意大利的会计整合示例。

意大利的 Commerce 功能包括销售点 (POS) 与会计打印机的示例集成。 该示例将扩展[会计整合功能](fiscal-integration-for-retail-channel.md)，以便它使用 Epson 的 [Epson FP-90III 系列](https://www.epson.it/products/sd/pos-printer/epson-fp-90iii-series)打印机，它可以使用会计 ePOS-Print API 通过 EpsonFPMate 网络服务在 Web 服务器模式下与财务打印机进行通信。 该示例仅支持 Registratore Telematico (RT) 模式。 该示例以源代码的形式提供，是 Retail 软件开发工具包 (SDK) 的一部分。

Microsoft 不会从 Epson 发布任何硬件、软件或文档。 有关如何获取会计打印机并对其进行操作的信息，请与 [Epson Italia S.p.A](https://www.epson.it) 联系。

## <a name="scenarios"></a>方案

意大利的会计打印机集成示例涵盖以下方案：

- 销售方案：

    - 打印现金和结转销售和退货的会计收据。
    - 从会计打印机捕获响应并将其存储到渠道数据库中。
    - 税金:

        - 映射到会计打印机的税码（部门）。
        - 将映射的税务数据转移到会计打印机。
        - 打印会计收据上的税金。

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

    - 打印会计收据上的收据编号的条码。
    - 打印为会计收据上的销售交易指定的[客户信息](emea-ita-customer-information.md)。 此信息的一个示例是客户的抽奖代码。 

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
- 每日报表（会计 X 和会计 Z）是使用嵌入在会计打印机固件中的格式打印的。
- 会计打印机不支持混合交易。 在 POS 功能配置文件中，**禁止在一份收据中混合销售和退货** 选项应设置为 **是**。
- 该示例仅支持与在 Registratore Telematico (RT)) 模式下工作的会计打印机集成。

## <a name="set-up-fiscal-integration-for-italy"></a>设置意大利的会计整合

意大利的会计打印机集成示例基于[会计整合功能](fiscal-integration-for-retail-channel.md)，是 Retail SDK 的一部分。 该示例位于 [Dynamics 365 Commerce 解决方案](https://github.com/microsoft/Dynamics365Commerce.Solutions/)存储库的 **src\\FiscalIntegration\\EpsonFP90IIISample** 文件夹中（例如[版本/9.33 中的示例](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/EpsonFP90IIISample)）。 该示例[包含](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services)一个会计单据提供程序（即 Commerce Runtime (CRT) 的扩展），以及一个会计连接器（即 Commerce Hardware Station 的扩展）。 有关如何使用 Retail SDK 的详细信息，请参阅 [Retail SDK 体系结构](../dev-itpro/retail-sdk/retail-sdk-overview.md)和[设置独立包装 SDK 的生成管道](../dev-itpro/build-pipeline.md)。

> [!WARNING]
> 由于[新的独立包装和扩展模型](../dev-itpro/build-pipeline.md)的限制，它当前无法用于此会计整合示例。 您必须在 Microsoft Dynamics Lifecycle Services (LCS) 中的开发人员虚拟机 (VM) 上使用先前版本的 Retail SDK。 有关详细信息，请参阅[意大利会计打印机整合示例的部署准则（旧版）](emea-ita-fpi-sample-sdk.md)。
>
> 以后的版本计划支持会计整合示例的新独立包装和扩展模型。

完成会计整合设置步骤，如[设置 Commerce 渠道的会计整合](setting-up-fiscal-integration-for-retail-channel.md)中所述。

1. [设置会计登记流程](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process)。 此外，请记下[特定于此会计打印机整合示例](#set-up-the-registration-process)的会计登记流程的设置。
1. [设置折扣的会计文本](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-texts-for-discounts)。
1. [设置错误处理设置](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings)。
1. [从 POS 设置会计 X/Z 报表](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos)。
1. [启用已推迟会计登记的手动执行](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration)。
1. [设置 POS 中的客户信息管理功能](emea-ita-customer-information.md#setup)。
1. [配置渠道组件](#configure-channel-components)。

### <a name="set-up-the-registration-process"></a>设置登记流程

要启用登记流程，请按照以下步骤设置 Commerce Headquarters。 有关详细信息，请参阅[设置 Commerce 渠道的会计整合](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process)。

1. 下载会计单据提供程序和会计连接器的配置文件：

    1. 打开 [Dynamics 365 Commerce 解决方案](https://github.com/microsoft/Dynamics365Commerce.Solutions/)存储库。
    1. 根据您的 SDK/应用程序版本（例如 **[版本/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**）选择正确的发布分支版本。
    1. 打开 **src \> FiscalIntegration \> EpsonFP90IIISample**。
    1. 下载 **CommerceRuntime \> DocumentProvider.EpsonFP90IIISample \> Configuration \> DocumentProviderEpsonFP90IIISample.xml** 中的会计单据提供程序配置文件（例如，[版本/9.33 的文件](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/EpsonFP90IIISample/CommerceRuntime/DocumentProvider.EpsonFP90IIISample/Configuration/DocumentProviderEpsonFP90IIISample.xml)）。
    1. 下载 **HardwareStation \> EpsonFP90IIIFiscalDeviceSample \> Configuration \> ConnectorEpsonFP90IIISample.xml** 中的会计连接器配置文件（例如，[版本/9.33 的文件](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/EpsonFP90IIISample/HardwareStation/EpsonFP90IIIFiscalDeviceSample/Configuration/ConnectorEpsonFP90IIISample.xml)）。

    > [!WARNING]
    > 由于[新的独立包装和扩展模型](../dev-itpro/build-pipeline.md)的限制，它当前无法用于此会计整合示例。 您必须在 LCS 中的开发人员 VM 上使用先前版本的 Retail SDK。 此会计整合示例的配置文件位于 LCS 中开发人员 VM 上 Retail SDK 的以下文件夹中：
    >
    > - **会计单据提供程序配置文件：** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extension.DocumentProvider.EpsonFP90IIISample\\Configuration\\DocumentProviderEpsonFP90IIISample.xml
    > - **会计连接器配置文件：** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.EpsonFP90IIIFiscalDeviceSample\\Configuration\\ConnectorEpsonFP90IIISample.xml
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

- **支付方式映射** - 为商店配置的付款方式到会计打印机支持的付款类型的映射。 以下示例显示默认映射。

    ```JSON
    {"PaymentMethods": [
        {"StorePaymentMethod":"1", "PrinterPaymentType":"0", "PrinterPaymentIndex":"00"},
        {"StorePaymentMethod":"3", "PrinterPaymentType":"2", "PrinterPaymentIndex":"00"},
        {"StorePaymentMethod":"4", "PrinterPaymentType":"2", "PrinterPaymentIndex":"01"},
        {"StorePaymentMethod":"6", "PrinterPaymentType":"0", "PrinterPaymentIndex":"01"},
        {"StorePaymentMethod":"8", "PrinterPaymentType":"6", "PrinterPaymentIndex":"01"}
        ],
        "DepositPaymentMethod": {"PrinterPaymentType":"2", "PrinterPaymentIndex":"00"}}
    ```

    下面是对这个映射中的属性的解释：

    - **StorePaymentMethod** 是在 **Retail 和 Commerce \> 渠道设置 \> 付款方式 \> 付款方式** 中为商店设置的付款方式。
    - **PrinterPaymentType** 和 **PrinterPaymentIndex** 是 Epson 会计打印机文档中定义的相应付款类型和索引。
    - **DepositPaymentMethod** 用于为通过客户订单保证金结算的部分客户订单提货金额指定打印机的付款类型和索引。

    下表显示了付款方式的示例映射如何对应于标准演示数据中配置的商店付款方式。

    | 付款方式 | 付款方式名称 |
    |----------------|---------------------|
    | 1              | 现金                |
    | 3              | 卡                |
    | 4              | 客户帐户    |
    | 6              | 货币            |
    | 8              | 礼品卡           |

    您必须根据应用程序中配置的付款方式修改示例映射。

- **收据编号的条码类型** - 用于在会计收据上显示收据编号的条码的类型。 默认映射是 **CODE128**。
- **在收据标题中打印会计数据** - 如果启用此参数，则将在会计收据上打印商店信息。 此信息包括商店的名称、地址和纳税标识号以及出纳的姓名。
- **会计打印机部门映射** - 会计打印机的部门到增值税 (VAT) 税率、增值税免税性质和产品类型的映射。 以下示例显示默认映射。

    ```JSON
    {"Departments": [
        {"VATRate":"2200", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"01"},
        {"VATRate":"2200", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"02"},
        {"VATRate":"1000", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"03"},
        {"VATRate":"1000", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"04"},
        {"VATRate":"0500", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"05"},
        {"VATRate":"0500", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"06"},
        {"VATRate":"0400", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"07"},
        {"VATRate":"0400", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"08"},
        {"VATRate":"0000", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"09"},
        {"VATRate":"0000", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"10"},
        {"VATRate":"0000", "VATExemptNature":"NS", "ProductType":"0", "DepartmentNumber":"99"}]}
    ```

    下面是对这个映射中的属性的解释：

    - **VATRate** 是一种已配置为销售税代码的受支持增值税税率。 映射中的值具有两个小数位，但没有小数分隔符。 例如 **2200** 表示 22%，**1000** 表示 10%。
    - **VATExemptNature** 仅适用于增值税税率为 0（零）的案例，包括无税的案例。 当前，仅礼品卡支持 **VATExemptNature**，映射中的值应与 XML 配置文件中的 **VATExemptNatureForGiftCard** 属性的值相对应。
    - **ProductType** 是产品类型。 值 **0** 表示商品，值 **1** 表示服务。
    - **DepartmentNumber** 是打印机中配置的部门编号，与前三个属性相对应。

    您必须根据应用程序中配置的增值税率以及在会计打印机中配置的相应部门修改示例映射。

- **礼品卡的增值税免税性质** - 在签发或充值礼品卡时应该应用的增值税免税性质。 该值应与会计打印机部门映射中的某些条目相对应。 默认映射是 **NS**。
- **启用免费物料** - 如果启用此参数，将启用具有 100% 折扣的物料的特殊 *omaggio* 折扣调整类型。
- **退货来源的信息代码** - 如果未提供原始销售收据，则是用于捕获退货交易来源的信息代码。 此参数与 **原始销售日期的信息代码** 和 **退货来源映射** 参数一起使用，以在会计收据中生成有关退货交易记录来源的正确消息（如果不存在原始销售交易）。 

    应配置此信息代码以使用户能够在商店中选择或输入可能的退货来源之一。 例如，可以将其配置为子代码列表（如 **从站点返回** 或 **从售货台返回**）。 然后，**退货来源映射** 参数用于将信息代码的值转换为会计打印机的命令。

    为 **退货来源的信息代码** 选择的信息代码应配置为一个必需的信息代码，每个销售交易都会启动一次该代码。 应在 POS 功能配置文件中将其指定为 **退回产品** 信息代码，以便在运行 **退回产品** 操作时启动此代码。

    没有为此映射指定默认值。 您必须选择在应用程序中配置的信息代码。

- **原始销售日期的信息代码** - 如果未提供原始销售收据，则是用于捕获退货交易原始销售日期的信息代码。 此参数与 **退货来源的信息代码** 和 **退货来源映射** 参数一起使用，以在会计收据中生成有关退货交易记录来源的正确消息（如果不存在原始销售交易）。

    应配置信息代码，以便将 **输入类型** 字段设置为 **日期**。 它应配置为一个必需的信息代码，每个销售交易都会启动一次该代码。 还应该针对为 **退货来源信息代码** 参数选择的信息代码将该代码指定为 **链接的信息代码**，以便一个接一个地启动这两个信息代码。

    没有为此映射指定默认值。 您必须选择在应用程序中配置的信息代码。

- **退货来源映射** - 如果未提供原始销售收据，则是用于打印退货交易来源的退货来源映射。 此参数与 **退货来源的信息代码** 和 **原始销售日期的信息代码** 参数一起使用，以在会计收据中生成有关退货交易记录来源的正确消息（如果不存在原始销售交易）。 以下示例显示默认映射。

    ```JSON
    {"ReturnOrigins": [
        {"ReturnOrigin":"1", "PrinterReturnOrigin":"POS"},
        {"ReturnOrigin":"2", "PrinterReturnOrigin":"ND"}
        ],
        "PrinterReturnOriginWithoutFiscalData":"POS"}
    ```

    下面是对这个映射中的属性的解释：

    - **ReturnOrigin** 是商店中可能的退货来源之一。 该值应与 **退货来源的信息代码** 参数的值相对应。
    - **PrinterReturnOrigin** 是会计打印机接受的退货来源之一 （**POS**、**VR** 或 **ND**）。
    - **PrinterReturnOriginWithoutFiscalData** 是会计打印机接受的退货来源，它对应于链接到原始销售交易的退货交易，原始销售交易没有链接的会计数据，因为它不是通过会计打印机登记的。 在这种情况下，原始销售日期被标识为原始销售交易的日期。

以下默认数据映射已过时，仅为向后兼容性进行保留：

- 增值税 (VAT) 代码映射
- 存款付款类型

#### <a name="fiscal-connector-settings"></a>会计连接器设置

作为会计整合示例的一部分提供的会计连接器配置中包含以下设置：

- **终结点地址** - 打印机的 URL。
- **日期和时间同步** - 一个指定打印机的日期和时间是否必须与连接的 Hardware Station 同步的值。

### <a name="configure-channel-components"></a>配置渠道组件

> [!WARNING]
> 由于[新的独立包装和扩展模型](../dev-itpro/build-pipeline.md)的限制，它当前无法用于此会计整合示例。 您必须在 LCS 中的开发人员 VM 上使用先前版本的 Retail SDK。 有关详细信息，请参阅[意大利会计打印机整合示例的部署准则（旧版）](emea-ita-fpi-sample-sdk.md)。
>
> 以后的版本计划支持会计整合示例的新独立包装和扩展模型。

#### <a name="set-up-the-development-environment"></a>设置开发环境

若要设置开发环境以测试和扩展示例，请按照以下步骤操作。

1. 克隆或下载 [Dynamics 365 Commerce 解决方案](https://github.com/microsoft/Dynamics365Commerce.Solutions)存储库。 根据您的 SDK/应用程序版本选择正确的发布分支版本。 有关详细信息，请参阅[从 GitHub 和 NuGet 下载 Retail SDK 示例和引用包](../dev-itpro/retail-sdk/sdk-github.md)。
1. 在 **Dynamics365Commerce.Solutions\\FiscalIntegration\\EpsonFP90IIISample\\EpsonFP90IIISample.sln** 中打开会计打印机集成解决方案，然后构建它。
1. 安装 CRT 扩展：

    1. 查找 CRT 扩展安装程序：

        - **Commerce Scale Unit：** 在 **EpsonFP90IIISample\\ScaleUnit\\ScaleUnit.EpsonFP90III.Installer\\bin\\Debug\\net461** 文件夹中，查找 **ScaleUnit.EpsonFP90III.Installer** 安装程序。
        - **Modern POS 上的本地 CRT：** 在 **EpsonFP90IIISample\\ModernPOS\\ModernPOS.EpsonFP90III.Installer\\bin\\Debug\\net461** 文件夹中，查找 **ModernPOS.EpsonFP90III.Installer** 安装程序。

    1. 从命令行启动 CRT 扩展安装程序：

        - **Commerce Scale Unit：**

            ```Console
            ScaleUnit.EpsonFP90III.Installer.exe install --verbosity 0
            ```

        - **Modern POS 上的本地 CRT：**

            ```Console
            ModernPOS.EpsonFP90III.Installer.exe install --verbosity 0
            ```

1. 安装 Hardware Station 扩展：

    1. 在 **EpsonFP90IIISample\\HardwareStation\\HardwareStation.EpsonFP90III.Installer\\bin\\Debug\\net461** 文件夹中，查找 **HardwareStation.EpsonFP90III.Installer** 安装程序。
    1. 从命令行启动扩展安装程序：

        ```Console
        HardwareStation.EpsonFP90III.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>生产环境

按照[为会计整合示例设置生成管道](fiscal-integration-sample-build-pipeline.md)中的步骤生成和发布会计整合示例的 Cloud Scale Unit 和自助可部署包。 可在 [Dynamics 365 Commerce 解决方案](https://github.com/microsoft/Dynamics365Commerce.Solutions)存储库的 **Pipeline\\YAML_Files** 文件夹中找到 **EpsonFP90III build-pipeline.yml** 模板 YAML 文件。

## <a name="design-of-extensions"></a>扩展设计

意大利的会计打印机集成示例基于[会计整合功能](fiscal-integration-for-retail-channel.md)，是 Retail SDK 的一部分。 该示例位于 [Dynamics 365 Commerce 解决方案](https://github.com/microsoft/Dynamics365Commerce.Solutions/)存储库的 **src\\FiscalIntegration\\EpsonFP90IIISample** 文件夹中（例如[版本/9.33 中的示例](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/EpsonFP90IIISample)）。 该示例[包含](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services)一个会计单据提供程序（即 CRT 的扩展），以及一个会计连接器（即 Commerce Hardware Station 的扩展）。 有关如何使用 Retail SDK 的详细信息，请参阅 [Retail SDK 体系结构](../dev-itpro/retail-sdk/retail-sdk-overview.md)和[设置独立包装 SDK 的生成管道](../dev-itpro/build-pipeline.md)。

> [!WARNING]
> 由于[新的独立包装和扩展模型](../dev-itpro/build-pipeline.md)的限制，它当前无法用于此会计整合示例。 您必须在 LCS 中的开发人员 VM 上使用先前版本的 Retail SDK。 有关详细信息，请参阅[意大利会计打印机整合示例的部署准则（旧版）](emea-ita-fpi-sample-sdk.md)。 以后的版本计划支持会计整合示例的新独立包装和扩展模型。

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime 扩展设计

作为会计单据提供程序的扩展的目的是生成特定于打印机的单据并处理会计打印机的响应。

#### <a name="request-handler"></a>请求处理程序

**DocumentProviderEpsonFP90III** 请求处理程序是关于从会计打印机生成单据的请求的入口点。

此处理程序继承自 **INamedRequestHandler** 接口。 **HandlerName** 方法负责返回处理程序的名称。 处理程序名称应与 Commerce Headquarters 中指定的连接器文档提供程序名称匹配。

此连接器支持以下请求：

- **GetFiscalDocumentDocumentProviderRequest** - 此请求包含有关应生成的具体单据的信息。 它返回应在会计打印机中登记的特定于打印机的单据。
- **GetSupportedRegistrableEventsDocumentProviderRequest** - 此请求返回要订阅的事件列表。 当前，支持以下事件：销售、打印 X 报表和打印 Z 报表。

#### <a name="configuration"></a>配置

会计单据提供程序的配置文件位于 [Dynamics 365 Commerce 解决方案](https://github.com/microsoft/Dynamics365Commerce.Solutions/)存储库内的 **src\\FiscalIntegration\\EpsonFP90IIISample\\CommerceRuntime\\DocumentProvider.EpsonFP90IIISample\\Configuration\\DocumentProviderEpsonFP90IIISample.xml** 中。 此文件的目的是启用要从 Commerce Headquarters 配置的单据提供程序的设置。 文件格式符合会计集成配置的要求。

### <a name="hardware-station-extension-design"></a>Hardware Station 扩展设计

作为会计连接器的扩展的目的是与会计打印机通信。 此扩展使用 HTTP 协议将 CRT 扩展生成的单据提交到会计打印机。 它还处理从会计打印机收到的响应。

#### <a name="request-handler"></a>请求处理程序

**EpsonFP90IIISample** 请求处理程序是用于处理发送给会计外围设备的请求的入口点。

此处理程序继承自 **INamedRequestHandler** 接口。 **HandlerName** 方法负责返回处理程序的名称。 处理程序名称应与 Commerce Headquarters 中指定的会计连接器名称匹配。

此连接器支持以下请求：

- **SubmitDocumentFiscalDeviceRequest** - 此请求将单据发送到打印机并返回会计打印机的响应。
- **IsReadyFiscalDeviceRequest** - 此请求用于检查设备运行状况。
- **InitializeFiscalDeviceRequest** - 此请求用于打印机初始化。

#### <a name="configuration"></a>配置

会计连接器的配置文件位于 [Dynamics 365 Commerce 解决方案](https://github.com/microsoft/Dynamics365Commerce.Solutions/)存储库内的 **src\\FiscalIntegration\\EpsonFP90IIISample\\HardwareStation\\EpsonFP90IIIFiscalDeviceSample\\Configuration\\ConnectorEpsonFP90IIISample.xml** 中。 此文件的目的是启用要从 Commerce Headquarters 配置的连接器的设置。 文件格式符合会计集成配置的要求。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
