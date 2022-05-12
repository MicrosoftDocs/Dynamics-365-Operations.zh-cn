---
title: 捷克共和国会计登记服务整合示例的部署准则（旧版）。
description: 本主题提供从 Microsoft Dynamics 365 Commerce Retail 软件开发套件 (SDK) 部署捷克共和国会计打印机整合示例的指南。
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: aaa894ccfd77a5522a3696e20987b9e67f3abee0
ms.sourcegitcommit: 7faf82fa7ce269c0201abb8473af861ef7ce00bf
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/19/2022
ms.locfileid: "8613953"
---
# <a name="deployment-guidelines-for-the-fiscal-registration-service-integration-sample-for-the-czech-republic-legacy"></a>捷克共和国会计登记服务整合示例的部署准则（旧版）。

[!include [banner](../includes/banner.md)]

本主题提供了从 Microsoft Dynamics Lifecycle Services (LCS) 内开发人员虚拟机 (VM) 上的 Microsoft Dynamics 365 Commerce Retail 软件开发套件 (SDK) 中部署捷克共和国会计登记服务整合示例的指南。 有关此会计整合示例的详细信息，请参阅[捷克共和国会计登记服务整合示例](emea-cze-fi-sample.md)。 

捷克共和国会计整合示例是 Retail SDK 的一部分。 有关如何安装和使用 SDK 的信息，请参阅 [Retail 软件开发套件 (SDK) 体系结构](../dev-itpro/retail-sdk/retail-sdk-overview.md)。 此示例由 Commerce Runtime (CRT) 和 Hardware Station 的扩展组成。 若要运行此示例，您必须修改和生成 CRT 和 Hardware Station 项目。 我们建议您使用未修改的 Retail SDK 进行此主题中描述的更改。 我们还建议您使用尚未更改任何文件的源代码管理系统，如 Azure DevOps。

## <a name="development-environment"></a>开发环境

执行以下步骤以设置开发环境，以便您可以测试和扩展示例。

### <a name="enable-commerce-runtime-extensions"></a>启用 Commerce Runtime 扩展

CRT 示例中包含 CRT 扩展组件。 若要完成以下过程，请在 **RetailSdk\\SampleExtensions\\CommerceRuntime** 下面打开 **CommerceRuntimeSamples.sln** 解决方案。

#### <a name="documentproviderefrsample-component"></a>DocumentProvider.EFRSample 组件

1. 查找 **Runtime.Extensions.DocumentProvider.EFRSample** 项目并生成它。
2. 在 **Runtime.Extensions.DocumentProvider.EFRSample\\bin\\Debug** 文件夹中，查找 **Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll** 程序集文件。
3. 将程序集文件复制到 CRT 扩展文件夹：

    - **Commerce Scale Unit：** 将文件复制到 Internet Information Services (IIS) Commerce Scale Unit 站点位置下的 **\\bin\\ext** 文件夹。
    - **Modern POS 上的本地 CRT：** 将文件复制到本地 CRT 客户端代理位置下的 **\\ext** 文件夹。

4. 查找 CRT 的扩展配置文件：

    - **Commerce Scale Unit：** 该文件名为 **commerceruntime.ext.config**，它位于 IIS Commerce Scale Unit 站点位置下的 **bin\\ext** 文件夹中。
    - **Modern POS 上的本地 CRT：** 该文件名为 **CommerceRuntime.MPOSOffline.Ext.config**，位于本地 CRT 客户端代理位置下。

5. 注册扩展配置文件中的 CRT 更改。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
    ```

#### <a name="documentproviderdatamodelefr-component"></a>DocumentProvider.DataModelEFR 组件

1. 查找 **Runtime.Extensions.DocumentProvider.DataModelEFR** 项目并生成它。
2. 在 **Runtime.Extensions.DocumentProvider.DataModelEFR\\bin\\Debug** 文件夹中，查找 **Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll** 程序集文件。
3. 将程序集文件复制到 CRT 扩展文件夹：

    - **Commerce Scale Unit：** 将文件复制到 IIS Commerce Scale Unit 站点位置下的 **\\bin\\ext** 文件夹。
    - **Modern POS 上的本地 CRT：** 将文件复制到本地 CRT 客户端代理位置下的 **\\ext** 文件夹。

4. 查找 CRT 的扩展配置文件：

    - **Commerce Scale Unit：** 该文件名为 **commerceruntime.ext.config**，它位于 IIS Commerce Scale Unit 站点位置下的 **bin\\ext** 文件夹中。
    - **Modern POS 上的本地 CRT：** 该文件名为 **CommerceRuntime.MPOSOffline.Ext.config**，位于本地 CRT 客户端代理位置下。

5. 注册扩展配置文件中的 CRT 更改。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
    ```

#### <a name="extension-configuration-file"></a>扩展配置文件

1. 查找 CRT 的扩展配置文件：

    - **Commerce Scale Unit：** 该文件名为 **commerceruntime.ext.config**，它位于 IIS Commerce Scale Unit 站点位置下的 **bin\\ext** 文件夹中。
    - **Modern POS 上的本地 CRT：** 该文件名为 **CommerceRuntime.MPOSOffline.Ext.config**，位于本地 CRT 客户端代理位置下。

2. 注册扩展配置文件中的 CRT 更改。

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsCzechia" />
    ```

### <a name="enable-fiscal-connector-extensions"></a>启用会计连接器扩展

您可以在[硬件工作站](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station)或 [POS 收银机](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-or-service-in-the-local-network)上启用会计连接器扩展。

### <a name="enable-hardware-station-extensions"></a>启用 Hardware Station 扩展

Hardware Station 示例中包含 Hardware Station 扩展组件。 若要完成以下过程，请在 **RetailSdk\\SampleExtensions\\HardwareStation** 下面打开 **HardwareStationSamples.sln** 解决方案。

#### <a name="efrsample-component"></a>EFRSample 组件

1. 查找 **HardwareStation.Extension.EFRSample** 项目并生成它。
2. 在 **Extension.EFRSample\\bin\\Debug** 文件夹中，查找以下程序集文件：

    - Contoso.Commerce.HardwareStation.EFRSample.dll
    - Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll

3. 将程序集文件复制到 Hardware Station 扩展文件夹：

    - **共享的 Hardware Station：** 将文件复制到 IIS Hardware Station 站点位置下的 **bin** 文件夹。
    - **Modern POS 上的专用 Hardware Station：** 将此文件复制到 Modern POS 客户端代理位置下。

4. 查找 Hardware Station 扩展的扩展配置文件。 该文件名为 **HardwareStation.Extension.config**。

    - **共享的 Hardware Station：** 此文件位于 IIS Hardware Station 站点位置中。
    - **Modern POS 上的专用 Hardware Station：** 此文件位于 Modern POS 客户端代理位置下。

5. 将以下行添加到配置文件的 **构成** 部分。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample.dll" />
    ```

#### <a name="enable-pos-extensions"></a>启用 POS 扩展

POS 扩展示例位于 [Dynamics 365 Commerce 解决方案](https://github.com/microsoft/Dynamics365Commerce.Solutions/)存储库的 **src\\FiscalIntegration\\PosFiscalConnectorSample** 文件夹中。

要在旧版 SDK 中使用 POS 扩展示例，请执行以下步骤。

1. 将 **Pos.Extension** 文件夹复制到旧版 SDK 的 POS **Extensions** 文件夹（例如，`C:\RetailSDK\src\POS\Extensions`）。
1. 重命名 **Pos.Extension** 文件夹 **PosFiscalConnector** 的副本。
1. 从 **PosFiscalConnector** 文件夹中删除以下文件夹和文件：

    - bin
    - DataService
    - devDependencies
    - 库
    - obj
    - Contoso.PosFiscalConnectorSample.Pos.csproj
    - RetailServerEdmxModel.g.xml
    - tsconfig.json

1. 打开 **CloudPos.sln** 或 **ModernPos.sln** 解决方案。
1. 在 **Pos.Extensions** 项目中，包括 **PosFiscalConnector** 文件夹。
1. 打开 **extensions.json** 文件，添加 **PosFiscalConnector** 扩展。
1. 构建 SDK。

### <a name="production-environment"></a>生产环境

上一个过程启用了作为会计登记服务集成示例组件的扩展。 此外，若要创建包含 Commerce 组件的可部署包，并在生产环境中应用这些包，则必须按照以下步骤操作。

1. 在 **RetailSdk\\Assets** 文件夹下的包配置文件中进行以下更改。

    - 在 **commerceruntime.ext.config** 和 **CommerceRuntime.MPOSOffline.Ext.config** 配置文件中，将以下行添加到 **构成** 部分中。

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsCzechia" />
        ```

    - 在 **HardwareStation.Extension.config** 配置文件中，将以下行添加到 **构成** 部分。

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample" />
        ```

2. 在 **BuildTools** 文件夹下的 **Customization.settings** 包自定义配置文件中进行以下更改。

    - 添加以下行以在可部署包中包括 CRT 扩展。

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

    - 添加以下行以在可部署包中包括 Hardware Station 扩展。

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample" />
        ```

3. 启动 Visual Studio 实用程序的 MSBuild 命令提示符，然后在 Retail SDK 文件夹下运行 **msbuild** 以创建可部署包。
4. 通过 LCS 或手动应用包。 有关详细信息，请参阅[创建可部署包](../dev-itpro/retail-sdk/retail-sdk-packaging.md)。
5. 完成在[设置适用于捷克共和国的 Commerce](emea-cze-fi-sample.md#set-up-commerce-for-the-czech-republic) 中描述的所有必需的设置任务。

## <a name="design-of-extensions"></a>扩展设计

捷克共和国的会计登记服务集成示例基于[会计整合功能](fiscal-integration-for-retail-channel.md)。 有关会计整合解决方案设计的详细信息，请参阅 [会计整合示例设计概览](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services)。

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime 扩展设计

作为会计单据提供程序的扩展的目的是生成特定于服务的单据并处理会计登记服务的响应。

CRT 扩展为 **Runtime.Extensions.DocumentProvider.EFRSample**。

#### <a name="request-handler"></a>请求处理程序

文档提供程序有一个 **DocumentProviderEFRFiscalCZE** 请求处理程序。 此处理程序用于为会计登记服务生成会计单据。

此处理程序继承自 **INamedRequestHandler** 接口。 **HandlerName** 方法负责返回处理程序的名称。 处理程序名称应与 Commerce Headquarters 中指定的连接器文档提供程序名称匹配。

此连接器支持以下请求：

- **GetFiscalDocumentDocumentProviderRequest** - 此请求包含有关应生成的具体单据的信息。 它返回应在会计登记服务中登记的特定于服务的单据。
- **GetSupportedRegistrableEventsDocumentProviderRequest** - 此请求返回要订阅的事件列表。 当前，支持以下事件：销售、客户帐户存款和客户订单保证金。
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** - 此请求返回会计登记服务的响应。 此响应已序列化以形成字符串，以便可以保存。

#### <a name="configuration"></a>配置

**DocumentProviderFiscalEFRSampleCzech** 配置文件位于扩展项目的 **Configuration** 文件夹中。 此文件的目的是启用要从 Commerce Headquarters 配置的单据提供程序的设置。 文件格式符合会计集成配置的要求。 添加了以下设置：

- 增值税税率映射
- 默认增值税组
- 保证金增值税组

### <a name="hardware-station-extension-design"></a>Hardware Station 扩展设计

作为会计连接器的扩展的目的是与会计登记服务通信。

硬件工作站扩展名为 **HardwareStation.Extension.EFRSample**。 它使用 HTTP 或 HTTPS 协议将 CRT 扩展生成的单据提交到会计登记服务。 它还处理从会计登记服务收到的响应。

#### <a name="request-handler"></a>请求处理程序

**EFRHandler** 请求处理程序是处理请求进入会计登记服务的入口点。

此处理程序继承自 **INamedRequestHandler** 接口。 **HandlerName** 方法负责返回处理程序的名称。 处理程序名称应与 Commerce Headquarters 中指定的会计连接器名称匹配。

此连接器支持以下请求：

- **SubmitDocumentFiscalDeviceRequest** - 此请求将单据发送到会计登记服务并返回此服务的响应。
- **IsReadyFiscalDeviceRequest** - 此请求用于检查会计登记服务的运行状况。
- **InitializeFiscalDeviceRequest** - 此请求用于初始化会计登记服务。

#### <a name="configuration"></a>配置

配置文件位于扩展项目的 **Configuration** 文件夹中。 此文件的目的是启用要从 Commerce Headquarters 配置的会计连接器的设置。 文件格式符合会计集成配置的要求。 添加了以下设置：

- **终结点地址** - 会计登记服务的 URL。
- **超时** – 连接器等待会计登记服务响应的以毫秒为单位的时长。

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
