---
title: 意大利会计打印机整合示例的部署准则（旧版）
description: 本文提供从 Microsoft Dynamics 365 Commerce Retail 软件开发套件 (SDK) 部署意大利会计打印机整合示例的指南。
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: bb07ca91c9e5bf1a79f672f9ba29b7bcc21688c6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848890"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-italy-legacy"></a>意大利会计打印机整合示例的部署准则（旧版）

[!include[banner](../includes/banner.md)]

本文提供了从 Microsoft Dynamics Lifecycle Services (LCS) 内开发人员虚拟机 (VM) 上的 Microsoft Dynamics 365 Commerce Retail 软件开发套件 (SDK) 中部署意大利会计打印机整合示例的指南。 有关此会计整合示例的详细信息，请参阅[意大利会计打印机整合示例](emea-ita-fpi-sample.md)。 

意大利会计整合示例是 Retail SDK 的一部分。 有关如何安装和使用 SDK 的信息，请参阅 [Retail 软件开发套件 (SDK) 体系结构](../dev-itpro/retail-sdk/retail-sdk-overview.md)。 此示例由 Commerce Runtime (CRT) 和 Hardware Station 的扩展组成。 若要运行此示例，您必须修改和生成 CRT 和 Hardware Station 项目。 我们建议您使用未修改的 Retail SDK 进行本文中描述的更改。 我们还建议您使用尚未更改任何文件的源代码管理系统，如 Azure DevOps。

## <a name="development-environment"></a>开发环境

执行以下步骤以设置开发环境，以便您可以测试和扩展示例。

### <a name="commerce-runtime-extension-components"></a>Commerce Runtime 扩展组件

Retail SDK 中包含 CRT 扩展组件。 若要完成以下过程，请在 **RetailSdk\\SampleExtensions\\CommerceRuntime** 下面打开 **CommerceRuntimeSamples.sln** 解决方案。

1. 查找 **Runtime.Extensions.DocumentProvider.EpsonFP90IIISample** 项目并生成它。
2. 在 **Extensions.DocumentProvider.EpsonFP90IIISample\\bin\\Debug** 文件夹中，查找 **Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.dll** 程序集文件。
3. 将程序集文件复制到 CRT 扩展文件夹：

    - **Commerce Scale Unit：** 将文件复制到 Internet Information Services (IIS) Commerce Scale Unit 站点位置下的 **\\bin\\ext** 文件夹。
    - **Modern POS 上的本地 CRT：** 将文件复制到本地 CRT 客户端代理位置下的 **\\ext** 文件夹。

4. 查找 CRT 的扩展配置文件：

    - **Commerce Scale Unit：** 该文件名为 **commerceruntime.ext.config**，它位于 IIS Commerce Scale Unit 站点位置下的 **bin\\ext** 文件夹中。
    - **Modern POS 上的本地 CRT：** 该文件名为 **CommerceRuntime.MPOSOffline.Ext.config**，位于本地 CRT 客户端代理位置下。

5. 注册扩展配置文件中的 CRT 更改。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
    ```

6. 重启 Commerce Scale Unit：

    - **Commerce Scale Unit：** 从 IIS 管理器重新启动 Commerce Scale Unit 站点。
    - **客户端代理：** 在任务管理器中结束 **dllhost.exe** 进程，然后重新启动 Modern POS。

### <a name="hardware-station-extension-components"></a>Hardware Station 扩展组件

Retail SDK 中包含 Hardware Station 扩展组件。 若要完成以下过程，请在 **RetailSdk\\SampleExtensions\\HardwareStation** 下面打开 **HardwareStationSamples.sln** 解决方案。

1. 查找 **HardwareStation.Extensions.EpsonFP90IIIFiscalDeviceSample** 项目并生成它。
2. 在 **Extensions.EpsonFP90IIIFiscalDeviceSample\\bin\\Debug** 文件夹中，查找 **Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample.dll** 程序集文件。
3. 将程序集文件复制到已部署的 Hardware Station 计算机：

    - **远程 Hardware Station：** 将文件复制到 IIS Hardware Station 站点位置下的 **bin** 文件夹。
    - **本地 Hardware Station：** 将文件复制到 Modern POS 客户端代理位置。

4. 查找 Hardware Station 扩展的配置文件。 该文件名为 **HardwareStation.Extension.config**：

    - **远程 Hardware Station：** 此文件位于 IIS Hardware Station 站点位置中。
    - **本地 Hardware Station：** 此文件位于 Modern POS 客户端代理位置中。

5. 将以下部分添加到配置文件的 **构成** 部分。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
    ```

6. 重新启动 Hardware Station 服务：

    - **远程 Hardware Station：** 从 IIS 管理器重新启动 Hardware Station 站点。
    - **本地 Hardware Station：** 在任务管理器中结束 **dllhost.exe** 进程，然后重新启动 Modern POS。

## <a name="production-environment"></a>生产环境

若要创建包含 Commerce 组件的可部署包，并在生产环境中应用这些包，请按照以下步骤操作。

1. 完成本文前面的[开发环境](#development-environment)一节中描述的步骤。
2. 在 **RetailSdk\\Assets** 文件夹下的包配置文件中进行以下更改：

    1. 在 **commerceruntime.ext.config** 和 **CommerceRuntime.MPOSOffline.Ext.config** 配置文件中，将以下行添加到 **构成** 部分中。

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
        ```

    1. 在 **HardwareStation.Extension.config** 配置文件中，将以下行添加到 **构成** 部分。

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
        ```

3. 在 **BuildTools** 文件夹下的 **Customization.settings** 包自定义配置文件中进行以下更改：

    1. 添加以下行以在可部署包中包括 CRT 扩展。

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.dll"/>
        ```

    1. 添加以下行以在可部署包中包括 Hardware Station 扩展。

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample.dll"/>
        ```

4. 在 **Packages\_SharedPackagingProjectComponents** 文件夹下的 **Sdk.ModernPos.Shared.csproj** 文件中进行以下更改，以将意大利的资源文件包含在可部署包中：

    1. 添加一个 **ItemGroup** 部分，其中包含指向所需翻译的资源文件的节点。 确保指定正确的命名空间和示例名称。 以下示例为 **it** 和 **it-CH** 区域设置添加资源节点。

        ```xml
        <ItemGroup>
            <ResourcesIt Include="$(SdkReferencesPath)\it\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
            <ResourcesItCh Include="$(SdkReferencesPath)\it-CH\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
        </ItemGroup>
        ```

    1. 在 **Target Name="CopyPackageFiles"** 部分，为每个区域设置添加一行，如下例所示。

        ```xml
        <Copy SourceFiles="@(ResourcesIt)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\it" SkipUnchangedFiles="true" />
        <Copy SourceFiles="@(ResourcesItCh)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\it-CH" SkipUnchangedFiles="true" />
        ```

5. 在 **Packages\_SharedPackagingProjectComponents** 文件夹下的 **Sdk.RetailServerSetup.proj** 文件中进行以下更改，以将意大利的资源文件包含在可部署包中：

    1. 添加一个 **ItemGroup** 部分，其中包含指向所需翻译的资源文件的节点。 确保指定正确的命名空间和示例名称。 以下示例为 **it** 和 **it-CH** 区域设置添加资源节点。

        ```xml
        <ItemGroup>
            <ResourcesIt Include="$(SdkReferencesPath)\it\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
            <ResourcesItCh Include="$(SdkReferencesPath)\it-CH\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
        </ItemGroup>
        ```

    1. 在 **Target Name="CopyPackageFiles"** 部分，为每个区域设置添加一行，如下例所示。

        ``` xml
        <Copy SourceFiles="@(ResourcesIt)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\it" SkipUnchangedFiles="true" />
        <Copy SourceFiles="@(ResourcesItCh)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\it-CH" SkipUnchangedFiles="true" />
        ```

6. 启动 Visual Studio 实用程序的 MSBuild 命令提示符，然后在 Retail SDK 文件夹下运行 **msbuild** 以创建可部署包。
7. 通过 LCS 或手动应用包。 有关详细信息，请参阅[创建可部署包](../dev-itpro/retail-sdk/retail-sdk-packaging.md)。

## <a name="design-of-extensions"></a>扩展设计

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime 扩展设计

作为会计单据提供程序的扩展的目的是生成特定于打印机的单据并处理会计打印机的响应。

CRT 扩展为 **Runtime.Extensions.DocumentProvider.EpsonFP90IIISample**。

有关会计整合解决方案设计的详细信息，请参阅[会计设备和服务的会计整合流程和会计整合示例](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services)。

#### <a name="request-handler"></a>请求处理程序

**DocumentProviderEpsonFP90III** 请求处理程序是关于从会计打印机生成单据的请求的入口点。

此处理程序继承自 **INamedRequestHandler** 接口。 **HandlerName** 方法负责返回处理程序的名称。 处理程序名称应与 Commerce Headquarters 中指定的连接器文档提供程序名称匹配。

此连接器支持以下请求：

- **GetFiscalDocumentDocumentProviderRequest** - 此请求包含有关应生成的具体单据的信息。 它返回应在会计打印机中登记的特定于打印机的单据。
- **GetSupportedRegistrableEventsDocumentProviderRequest** - 此请求返回要订阅的事件列表。 当前，支持以下事件：销售、打印 X 报表和打印 Z 报表。

#### <a name="configuration"></a>配置

配置文件位于扩展项目的 **Configuration** 文件夹中。 此文件的目的是启用要从 Commerce Headquarters 配置的单据提供程序的设置。 文件格式符合会计集成配置的要求。 添加了以下设置：

- 增值税代码映射
- 增值税税率映射
- 支付方式映射
- 收据编号的条码类型
- 存款付款类型

### <a name="hardware-station-extension-design"></a>Hardware Station 扩展设计

作为会计连接器的扩展的目的是与会计打印机通信。

Hardware Station 扩展是 **HardwareStation.Extension.EpsonFP90IIIFiscalDeviceSample**。 此扩展使用 HTTP 协议将 CRT 扩展生成的单据提交到会计打印机。 它还处理从会计打印机收到的响应。

#### <a name="request-handler"></a>请求处理程序

**EpsonFP90IIISample** 请求处理程序是处理请求进入会计外围设备的入口点。

此处理程序继承自 **INamedRequestHandler** 接口。 **HandlerName** 方法负责返回处理程序的名称。 处理程序名称应与 Commerce Headquarters 中指定的会计连接器名称匹配。

此连接器支持以下请求：

- **SubmitDocumentFiscalDeviceRequest** - 此请求将单据发送到打印机并返回会计打印机的响应。
- **IsReadyFiscalDeviceRequest** - 此请求用于检查设备运行状况。
- **InitializeFiscalDeviceRequest** - 此请求用于打印机初始化。

#### <a name="configuration"></a>配置

配置文件位于扩展项目的 **Configuration** 文件夹中。 此文件的目的是启用要从 Commerce Headquarters 配置的连接器的设置。 文件格式符合会计集成配置的要求。 添加了以下设置：

- **终结点地址** - 打印机的 URL。
- **日期和时间同步** - 一个指定打印机的日期和时间是否必须与连接的 Hardware Station 同步的值。
