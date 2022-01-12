---
title: 奥地利会计登记服务整合示例的部署准则（旧版）
description: 本主题提供从 Microsoft Dynamics 365 Commerce Retail 软件开发套件 (SDK) 部署奥地利会计整合示例的指南。
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: c038773dc7c1c475f5852f0f0272b59516140593
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944655"
---
# <a name="deployment-guidelines-for-the-fiscal-registration-service-integration-sample-for-austria-legacy"></a>奥地利会计登记服务整合示例的部署准则（旧版）

[!include [banner](../includes/banner.md)]

本主题提供了从 Microsoft Dynamics Lifecycle Services (LCS) 内开发人员虚拟机 (VM) 上的 Microsoft Dynamics 365 Commerce Retail 软件开发套件 (SDK) 中部署奥地利会计登记服务整合示例的指南。 有关此会计整合示例的详细信息，请参阅[奥地利会计登记服务整合示例](emea-aut-fi-sample.md)。 

奥地利会计整合示例是 Retail SDK 的一部分。 有关如何安装和使用 SDK 的信息，请参阅 [Retail 软件开发套件 (SDK) 体系结构](../dev-itpro/retail-sdk/retail-sdk-overview.md)。 会计整合示例由 Commerce Runtime (CRT)、Hardware Station 和销售点 (POS) 的扩展组成。 若要运行此示例，您必须修改和生成 CRT、Hardware Station 和 POS 项目。 我们建议您使用未修改的 Retail SDK 进行此主题中描述的更改。 我们还建议您使用尚未更改任何文件的源代码管理系统，如 Azure DevOps。

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
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsAustria" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventAustria" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.XZReportsAustria" />
    ```

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

### <a name="enable-modern-pos-extension-components"></a>启用 Modern POS 扩展组件

1. 在 **RetailSdk\\POS** 下打开 **ModernPOS.sln** 解决方案，并确保可以在不出错的情况下编译它。 此外，请确保您可以使用 **运行** 命令从 Visual Studio 运行 Modern POS。

    > [!NOTE]
    > 不得自定义 Modern POS。 您必须启用用户帐户控制 (UAC)，并且必须根据需要卸载以前安装的 Modern POS 实例。

2. 通过在 **extensions.json** 文件中添加以下行来启用扩展。

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.AT"
            }
        ]
    }
    ```

    > [!NOTE]
    > 有关详细信息，以及用于显示如何包括源代码文件夹和允许加载扩展的示例，请参阅 **Pos.Extensions** 项目内 readme.md 文件中的说明。

3. 重新生成解决方案。
4. 在调试器中运行 Modern POS 并测试功能。

### <a name="enable-cloud-pos-extension-components"></a>启用 Cloud POS 扩展组件

1. 在 **RetailSdk\\POS** 下打开 **CloudPOS.sln** 解决方案，并确保可以在不出错的情况下编译它。
2. 通过在 **extensions.json** 文件中添加以下行来启用扩展。

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.AT"
            }
        ]
    }
    ```

    > [!NOTE]
    > 有关详细信息，以及用于显示如何包括源代码文件夹和允许加载扩展的示例，请参阅 **Pos.Extensions** 项目内 readme.md 文件中的说明。

3. 重新生成解决方案。
4. 使用 **运行** 命令并执行 Retail SDK 手册中的步骤来运行解决方案。

## <a name="production-environment"></a>生产环境

上一个过程启用了作为会计登记服务集成示例组件的扩展。 此外，若要创建包含 Commerce 组件的可部署包，并在生产环境中应用这些包，则必须按照以下步骤操作。

1. 在 **RetailSdk\\Assets** 文件夹下的包配置文件中进行以下更改：

    - 在 **commerceruntime.ext.config** 和 **CommerceRuntime.MPOSOffline.Ext.config** 配置文件中，将以下行添加到 **构成** 部分中。

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsAustria" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventAustria" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.XZReportsAustria" />
        ```

    - 在 **HardwareStation.Extension.config** 配置文件中，将以下行添加到 **构成** 部分。

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        ```

2. 在 **BuildTools** 文件夹下的 **Customization.settings** 包自定义配置文件中进行以下更改：

    - 添加以下行以在可部署包中包括 CRT 扩展。

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

    - 添加以下行以在可部署包中包括 Hardware Station 扩展。

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

3. 启动 Visual Studio 实用程序的 MSBuild 命令提示符，然后在 Retail SDK 文件夹下运行 **msbuild** 以创建可部署包。
4. 通过 LCS 或手动应用包。 有关详细信息，请参阅[创建可部署包](../dev-itpro/retail-sdk/retail-sdk-packaging.md)。
5. 完成在[设置适用于奥地利的 Commerce](emea-aut-fi-sample.md#set-up-commerce-for-austria) 中描述的所有必需的设置任务。

## <a name="design-of-extensions"></a>扩展设计

奥地利的会计登记服务集成示例基于[会计整合功能](fiscal-integration-for-retail-channel.md)。 有关会计整合解决方案设计的详细信息，请参阅 [会计整合示例设计概览](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices)。

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime 扩展设计

作为会计单据提供程序的扩展的目的是生成特定于服务的单据并处理会计登记服务的响应。

CRT 扩展为 **Runtime.Extensions.DocumentProvider.EFRSample**。

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

配置文件位于扩展项目的 **Configuration** 文件夹中：

- **DocumentProviderFiscalEFRSampleAustria** - 用于会计单据。
- **DocumentProviderNonFiscalEFRSampleAustria** - 用于非会计单据。

这些文件的目的是启用要从 Commerce Headquarters 配置的单据提供程序的设置。 文件格式符合会计集成配置的要求。 添加了以下设置：

- 增值税税率映射

### <a name="hardware-station-extension-design"></a>Hardware Station 扩展设计

作为会计连接器的扩展的目的是与会计登记服务通信。

Hardware Station 扩展是 **HardwareStation.Extension.EFRSample**。 它使用 HTTP 协议将 CRT 扩展生成的单据提交到会计登记服务。 它还处理从会计登记服务收到的响应。

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
- **超时** - 驱动程序等待会计登记服务响应的以毫秒为单位的时长。
