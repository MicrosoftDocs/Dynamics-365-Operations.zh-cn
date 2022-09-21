---
title: 波兰会计打印机整合示例的部署准则（旧版）
description: 本文提供从 Microsoft Dynamics 365 Commerce Retail 软件开发套件 (SDK) 部署波兰会计打印机整合示例的指南。
author: EvgenyPopovMBS
ms.date: 08/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: b19c8d7a80ac772ae238191d1285a1ad80e6f611
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473950"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-poland-legacy"></a>波兰会计打印机整合示例的部署准则（旧版）

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> 仅当您使用 Microsoft Dynamics 365 Commerce 版本 10.0.28 或更早版本时，您才应该遵循本文中的指南。 从 Commerce 版本 10.0.29 开始，可以在 Commerce 软件开发工具包 (SDK) 中找到波兰的会计打印机集成示例。 有关更多信息，请参阅[配置渠道组件](./emea-pol-fpi-sample.md#configure-channel-components)。

本文提供了从 Microsoft Dynamics Lifecycle Services (LCS) 内开发人员虚拟机 (VM) 上的 Dynamics 365 Commerce Retail SDK 中部署波兰会计打印机集成示例的指南。 有关此会计整合示例的详细信息，请参阅[波兰会计打印机整合示例](emea-pol-fpi-sample.md)。 

波兰会计整合示例是 Retail SDK 的一部分。 有关如何安装和使用 SDK 的信息，请参阅 [Retail 软件开发套件 (SDK) 体系结构](../dev-itpro/retail-sdk/retail-sdk-overview.md)。 此示例由 Commerce Runtime (CRT) 和 Hardware Station 的扩展组成。 若要运行此示例，您必须修改和生成 CRT 和 Hardware Station 项目。 我们建议您使用未修改的 Retail SDK 进行本文中描述的更改。 我们还建议您使用尚未更改任何文件的源代码管理系统，如 Azure DevOps。

## <a name="development-environment"></a>开发环境

执行以下步骤以设置开发环境，以便您可以测试和扩展示例。

### <a name="commerce-runtime-extension-components"></a>Commerce Runtime 扩展组件

Retail SDK 中包含 CRT 扩展组件。 若要完成以下过程，请在 **RetailSdk\\SampleExtensions\\CommerceRuntime** 下面打开 **CommerceRuntimeSamples.sln** 解决方案。

1. 查找 **Runtime.Extensions.DocumentProvider.PosnetSample** 项目并生成它。
2. 在 **Extensions.DocumentProvider.PosnetSample\\bin\\Debug** 文件夹中，查找 **Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample.dll** 程序集文件。
3. 将程序集文件复制到 CRT 扩展文件夹：

    - **Commerce Scale Unit：** 将文件复制到 Internet Information Services (IIS) Commerce Scale Unit 站点位置下的 **\\bin\\ext** 文件夹。
    - **Modern POS 上的本地 CRT：** 将文件复制到本地 CRT 客户端代理位置下的 **\\ext** 文件夹。

4. 查找 CRT 的扩展配置文件：

    - **Commerce Scale Unit：** 该文件名为 **commerceruntime.ext.config**，它位于 IIS Commerce Scale Unit 站点位置下的 **bin\\ext** 文件夹中。
    - **Modern POS 上的本地 CRT：** 该文件名为 **CommerceRuntime.MPOSOffline.Ext.config**，位于本地 CRT 客户端代理位置下。

5. 注册扩展配置文件中的 CRT 更改。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample" />
    ```

6. 重新启动 Commerce 服务：

    - **Commerce Scale Unit：** 从 IIS 管理器重新启动 Commerce 服务站点。
    - **客户端代理：** 在任务管理器中结束 **dllhost.exe** 进程，然后重新启动 Modern POS。

### <a name="hardware-station-extension-components"></a>Hardware Station 扩展组件

Retail SDK 中包含 Hardware Station 扩展组件。 若要完成以下过程，请在 **RetailSdk\\SampleExtensions\\HardwareStation** 下面打开 **HardwareStationSamples.sln** 解决方案。

1. 查找 **HardwareStation.Extension.PosnetThermalFVFiscalPrinterSample** 项目并生成它。
2. 在 **Extension.Posnet.ThermalFVFiscalPrinterSample\\bin\\Debug** 文件夹中，查找 **Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample.dll** 程序集文件。
3. 将程序集文件复制到已部署的 Hardware Station 计算机：

    - **远程 Hardware Station：** 将文件复制到 IIS Hardware Station 站点位置下的 **bin** 文件夹。 复制打印机驱动程序库（**libposcmbth.dll**、**libcmbth\_serial.dll** 和 **cmbth\_pl.lng**）。

4. 查找 Hardware Station 扩展的配置文件。 该文件名为 **HardwareStation.Extension.config**：

    - **远程 Hardware Station：** 此文件位于 IIS Hardware Station 站点位置中。

5. 将以下行添加到配置文件的 **构成** 部分。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample" />
    ```

6. 重新启动 Hardware Station 服务：

    - **远程 Hardware Station：** 从 IIS 管理器重新启动 Hardware Station 站点。

## <a name="production-environment"></a>生产环境

在上一个过程中，您启用了作为会计登记服务集成示例组件的扩展。 此外，若要创建包含 Commerce 组件的可部署包，并在生产环境中应用这些包，则必须按照以下步骤操作。

1. 在 **RetailSdk\\Assets** 文件夹下的包配置文件中进行以下更改：

    - 在 **commerceruntime.ext.config** 和 **CommerceRuntime.MPOSOffline.Ext.config** 配置文件中，将以下行添加到 **构成** 部分中。

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample" />
        ```

    - 在 **HardwareStation.Extension.config** 配置文件中，将以下行添加到 **构成** 部分。

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample" />
        ```

1. 在 **BuildTools** 文件夹下的 **Customization.settings** 包自定义配置文件中进行以下更改：

    - 添加以下行以在可部署包中包括 CRT 扩展。

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample.dll"/>
        ```

    - 添加以下行以在可部署包中包括 Hardware Station 扩展。

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample.dll"/>
        ```

1. 启动 Visual Studio 实用程序的 MSBuild 命令提示符，然后在 Retail SDK 文件夹下运行 **msbuild** 以创建可部署包。
1. 通过 LCS 或手动应用包。 有关详细信息，请参阅[创建可部署包](../dev-itpro/retail-sdk/retail-sdk-packaging.md)。

## <a name="design-of-extensions"></a>扩展设计

波兰的会计打印机集成示例基于[会计整合功能](fiscal-integration-for-retail-channel.md)。 有关会计整合解决方案设计的详细信息，请参阅 [会计整合示例设计概览](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services)。

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime 扩展设计

作为会计单据提供程序的扩展的目的是生成特定于打印机的单据并处理会计打印机的响应。

CRT 扩展为 **Runtime.Extensions.DocumentProvider.PosnetSample**。 此扩展以 POSNET 规格 19-3678 定义的 JavaScript 对象表示法 (JSON) 格式生成一组特定于打印机的命令。

有关会计整合解决方案设计的详细信息，请参阅[会计设备和服务的会计整合流程和会计整合示例](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services)。

#### <a name="request-handler"></a>请求处理程序

**DocumentProviderPosnetProtocol** 请求处理程序是关于从会计打印机生成单据的请求的入口点。

此处理程序继承自 **INamedRequestHandler** 接口。 **HandlerName** 方法负责返回处理程序的名称。 处理程序名称应与 Commerce Headquarters 中指定的连接器文档提供程序名称匹配。

此连接器支持以下请求：

- **GetFiscalDocumentDocumentProviderRequest** - 此请求包含有关应生成的具体单据的信息。 它返回应在会计打印机中登记的特定于打印机的单据。
- **GetSupportedRegistrableEventsDocumentProviderRequest** - 此请求返回要订阅的事件列表。 当前，支持以下事件：销售、打印 X 报表和打印 Z 报表。

#### <a name="configuration"></a>配置

配置文件位于扩展项目的 **Configuration** 文件夹中。 此文件的目的是启用要从 Commerce Headquarters 配置的单据提供程序的设置。 文件格式符合会计集成配置的要求。 添加了以下设置：

- 增值税税率映射
- 支付方式映射
- 存款付款类型

### <a name="hardware-station-extension-design"></a>Hardware Station 扩展设计

作为会计连接器的扩展的目的是与会计打印机通信。

Hardware Station 扩展是 **HardwareStation.Extension.PosnetThermalFVFiscalPrinterSample**。 此扩展调用 POSNET 驱动程序的函数以将 CRT扩展生成的命令提交到会计打印机。 它还处理设备错误。

#### <a name="request-handler"></a>请求处理程序

**FiscalPrinterHandler** 请求处理程序是用于处理发送给会计外围设备的请求的入口点。

此处理程序继承自 **INamedRequestHandler** 接口。 **HandlerName** 方法负责返回处理程序的名称。 处理程序名称应与 Commerce Headquarters 中指定的会计连接器名称匹配。

此连接器支持以下请求：

- **SubmitDocumentFiscalDeviceRequest** - 此请求将单据发送到打印机并返回会计打印机的响应。
- **IsReadyFiscalDeviceRequest** - 此请求用于检查设备运行状况。
- **InitializeFiscalDeviceRequest** - 此请求用于打印机初始化。

#### <a name="configuration"></a>配置

配置文件位于扩展项目的 **Configuration** 文件夹中。 此文件的目的是启用要从 Commerce Headquarters 配置的连接器的设置。 文件格式符合会计集成配置的要求。 添加了以下设置：

- **连接字符串** - 一个以驱动程序支持的格式描述设备连接详细信息的字符串。 有关详细信息，请参阅 POSNET 驱动程序文档。
- **日期和时间同步** - 一个指定打印机的日期和时间是否必须与连接的 Hardware Station 同步的值。
- **设备超时** - 驱动程序等待设备响应的时长（毫秒）。 有关详细信息，请参阅 POSNET 驱动程序文档。
