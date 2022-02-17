---
title: 瑞典控制单元整合示例的部署准则（旧版）
description: 本主题提供从 Retail SDK 部署瑞典控制单元整合示例的指南
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: b8d60f32d986dec6bb26d78ebdfe8cee3a6b688a
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2022
ms.locfileid: "8077030"
---
# <a name="deployment-guidelines-for-the-control-unit-integration-sample-for-sweden-legacy"></a>瑞典控制单元整合示例的部署准则（旧版）

[!include [banner](../includes/banner.md)]

本主题提供了从 Microsoft Dynamics Lifecycle Services (LCS) 内开发人员虚拟机 (VM) 上的 Retail 软件开发套件 (SDK) 中部署瑞典控制单元整合示例的指南。 有关此会计整合示例的详细信息，请参阅[瑞典控制单元整合示例](emea-swe-fi-sample.md)。 

瑞典会计整合示例是 Retail SDK 的一部分。 有关如何安装和使用 SDK 的信息，请参阅 [Retail 软件开发套件 (SDK) 体系结构](../dev-itpro/retail-sdk/retail-sdk-overview.md)。 此示例由 Commerce Runtime (CRT)、Hardware Station 和销售点 (POS) 的扩展组成。 若要运行此示例，您必须修改和生成 CRT、Hardware Station 和 POS 项目。 我们建议您使用未修改的 Retail SDK 进行此主题中描述的更改。 我们还建议您使用尚未更改任何文件的源代码管理系统，如 Azure DevOps。

## <a name="development-environment"></a>开发环境

执行以下步骤以设置开发环境，以便您可以测试和扩展示例。

### <a name="enable-crt-extensions"></a>启用 CRT 扩展

CRT 示例中包含 CRT 扩展组件。 若要完成以下过程，请在 **RetailSdk\\SampleExtensions\\CommerceRuntime** 下面打开 **CommerceRuntimeSamples.sln** 解决方案。

#### <a name="documentprovidercleancashsample-component"></a>DocumentProvider.CleanCashSample 组件

1. 查找 **Runtime.Extensions.DocumentProvider.CleanCashSample** 项目并生成它。
2. 在 **Runtime.Extensions.DocumentProvider.CleanCashSample\\bin\\Debug** 文件夹中，查找 **Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll** 程序集文件。
3. 将程序集文件复制到 CRT 扩展文件夹：

    - **Commerce Scale Unit：** 将文件复制到 Internet Information Services (IIS) Commerce Scale Unit 站点位置下的 **\\bin\\ext** 文件夹。
    - **Modern POS 上的本地 CRT：** 将文件复制到本地 CRT 客户端代理位置下的 **\\ext** 文件夹。

4. 查找 CRT 的扩展配置文件：

    - **Commerce Scale Unit：** 该文件名为 **commerceruntime.ext.config**，它位于 IIS Commerce Scale Unit 站点位置下的 **bin\\ext** 文件夹中。
    - **Modern POS 上的本地 CRT：** 该文件名为 **CommerceRuntime.MPOSOffline.Ext.config**，位于本地 CRT 客户端代理位置下。

5. 注册扩展配置文件中的 CRT 更改。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    ```

#### <a name="extension-configuration-file"></a>扩展配置文件

1. 查找 CRT 的扩展配置文件：

    - **Commerce Scale Unit：** 该文件名为 **commerceruntime.ext.config**，它位于 IIS Commerce Scale Unit 站点位置下的 **bin\\ext** 文件夹中。
    - **Modern POS 上的本地 CRT：** 该文件名为 **CommerceRuntime.MPOSOffline.Ext.config**，位于本地 CRT 客户端代理位置下。

2. 注册扩展配置文件中的 CRT 更改。

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

### <a name="enable-hardware-station-extensions"></a>启用 Hardware Station 扩展

Hardware Station 示例中包含 Hardware Station 扩展组件。 若要完成以下过程，请在 **RetailSdk\\SampleExtensions\\HardwareStation** 下面打开 **HardwareStationSamples.sln** 解决方案。

#### <a name="cleancash-component"></a>CleanCash 组件

1. 查找 **HardwareStation.Extension.CleanCashSample** 项目并生成它。
2. 在 **Extension.CleanCashSample\\bin\\Debug** 文件夹中，查找 **Contoso.Commerce.HardwareStation.CleanCashSample.dll** 和 **Interop.CleanCash\_1\_1.dll** 程序集文件。
3. 将程序集文件复制到 Hardware Station 扩展文件夹：

    - **共享的 Hardware Station：** 将文件复制到 IIS Hardware Station 站点位置下的 **bin** 文件夹。
    - **Modern POS 上的专用 Hardware Station：** 将此文件复制到 Modern POS 客户端代理位置下。

4. 查找 Hardware Station 扩展的扩展配置文件。 该文件名为 **HardwareStation.Extension.config**。

    - **共享 Hardware Station：** 此文件在 IIS Hardware Station 站点位置下。
    - **Modern POS 上的专用 Hardware Station：** 此文件在 Modern POS 客户端代理位置下。

5. 将以下行添加到配置文件的 **构成** 部分。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

### <a name="enable-modern-pos-extension-components"></a>启用 Modern POS 扩展组件

1. 在 **RetailSdk\\POS** 下打开 **ModernPOS.sln** 解决方案，并确保可以在不出错的情况下编译它。 此外，请确保您可以使用 **运行** 命令从 Visual Studio 运行 Modern POS。

    > [!NOTE]
    > 不得自定义 Modern POS。 您必须启用用户帐户控制 (UAC)，并且必须根据需要卸载以前安装的 Modern POS 实例。

2. 启用必须通过在 **extensions.json** 文件中添加以下行来加载的扩展。

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
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
2. 启用必须通过在 **extensions.json** 文件中添加以下行来加载的扩展。

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

    > [!NOTE]
    > 有关详细信息，以及用于显示如何包括源代码文件夹和允许加载扩展的示例，请参阅 **Pos.Extensions** 项目内 readme.md 文件中的说明。

3. 重新生成解决方案。
4. 使用 **运行** 命令并执行 Retail SDK 手册中的步骤来运行解决方案。

## <a name="production-environment"></a>生产环境

上一个过程启用作为控制单元集成示例组件的扩展。 此外，若要创建包含 Commerce 组件的可部署包，并在生产环境中应用这些包，则必须按照以下步骤操作。

1. 在 **RetailSdk\\Assets** 文件夹下的包配置文件中进行以下更改：

    - 在 **commerceruntime.ext.config** 和 **CommerceRuntime.MPOSOffline.Ext.config** 配置文件中，将以下行添加到 **构成** 部分中。

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
        ```

    - 在 **HardwareStation.Extension.config** 配置文件中，将以下行添加到 **构成** 部分。

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
        ```

2. 在 **BuildTools** 文件夹下的 **Customization.settings** 包自定义配置文件中进行以下更改：

    - 添加以下行以在可部署包中包括 CRT 扩展。

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll" />
        ```

    - 添加以下行以在可部署包中包括 Hardware Station 扩展。

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.CleanCashSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Interop.CleanCash_1_1.dll" />
        ```

3. 通过在 **RetailSDK\\POS\\Extensions** 文件夹下的 **extensions.json** 文件中添加以下行来启用 POS 扩展。

    ``` json
    {
        "extensionPackages": [
            {
            "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

4. 启动 Visual Studio 实用程序的 MSBuild 命令提示符，然后在 Retail SDK 文件夹下运行 **msbuild** 以创建可部署包。
5. 通过 LCS 或手动应用包。 有关详细信息，请参阅[创建可部署包](../dev-itpro/retail-sdk/retail-sdk-packaging.md)。
6. 完成在[设置与控制单元的集成](emea-swe-fi-sample.md#setting-up-the-integration-with-control-units)中描述的所有必需设置任务。

## <a name="design-of-the-extensions"></a>扩展设计

### <a name="crt-extension-design"></a>CRT 扩展设计

作为会计单据提供程序的扩展的目的是生成特定于服务的单据并处理控制单元的响应。

CRT 扩展为 **Runtime.Extensions.DocumentProvider.CleanCashSample**。

有关会计整合解决方案设计的详细信息，请参阅[会计设备和服务的会计整合流程和会计整合示例](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services)。

#### <a name="request-handler"></a>请求处理程序

文档提供程序有一个 **DocumentProviderCleanCash** 请求处理程序。 此处理程序用于为控制单元生成会计单据。

此处理程序继承自 **INamedRequestHandler** 接口。 **HandlerName** 方法负责返回处理程序的名称。 处理程序名称应与 Commerce Headquarters 中指定的连接器文档提供程序名称匹配。

此连接器支持以下请求：

- **GetFiscalDocumentDocumentProviderRequest** - 此请求包含有关应生成的具体单据的信息。 它返回应在控制单元中登记的特定于服务的单据。
- **GetSupportedRegistrableEventsDocumentProviderRequest** - 此请求返回要订阅的事件列表。 当前，销售事件和审计事件均受支持。

#### <a name="configuration"></a>配置

**DocumentProviderFiscalCleanCashSample** 配置文件位于扩展项目的 **Configuration** 文件夹中。 此文件的目的是启用要从 Commerce Headquarters 配置的单据提供程序的设置。 文件格式符合会计集成配置的要求。 添加了以下设置：

- 增值税代码映射

### <a name="hardware-station-extension-design"></a>Hardware Station 扩展设计

作为会计连接器的扩展的目的是与控制单元通信。

Hardware Station 扩展是 **HardwareStation.Extension.CleanCashSample**。 它使用 HTTP 协议将 CRT 扩展生成的单据提交到控制单元。 它还处理从控制单元收到的响应。

#### <a name="request-handler"></a>请求处理程序

**CleanCashHandler** 请求处理程序是处理请求进入控制单元的入口点。

此处理程序继承自 **INamedRequestHandler** 接口。 **HandlerName** 方法负责返回处理程序的名称。 处理程序名称应与 Commerce Headquarters 中指定的会计连接器名称匹配。

此连接器支持以下请求：

- **SubmitDocumentFiscalDeviceRequest** - 此请求将单据发送到控制单元并返回控制单元的响应。
- **IsReadyFiscalDeviceRequest** - 此请求用于检查控制单元运行状况。
- **InitializeFiscalDeviceRequest** - 此请求用于初始化控制单元。

#### <a name="configuration"></a>配置

配置文件位于扩展项目的 **Configuration** 文件夹中。 此文件的目的是启用要从 Commerce Headquarters 配置的会计连接器的设置。 文件格式符合会计集成配置的要求。 添加了以下设置：

- **连接字符串** - 控制单元连接设置。
- **超时** - 驱动程序等待控制单元响应的时长（毫秒）。

## <a name="migrating-from-the-earlier-integration-sample"></a>正在从早期集成示例中迁移

如果您使用早期的 [POS 与瑞典的控制单元集成的示例](retail-sdk-control-unit-sample.md)，则您可能必须从该示例迁移到当前集成示例。 为了在未来接受更改并及时接收瑞典功能更新，您可能必须升级、在您构建的扩展中进行小的代码和配置调整，并重新构建您的解决方案。 您创建的扩展逻辑中无需进行重大更改。 如果没有从您那边进行任何更改，则早期集成示例和自定义项将继续正常工作。 因此，您可以针对您的环境进行规划、准备和利用。

### <a name="migration-process"></a>迁移流程

从早期集成示例迁移到当前控制单元集成示例应基于逐步更新的概念。 换言之，在您开始更新 POS 和 Hardware Station 组件之前，应事先已经更新所有 Commerce Headquarters 和 Commerce Scale Unit 组件。

为了帮助防止事件或交易被签名两次（即，由早期扩展和当前扩展进行签名）或者由于缺少配置而无法对事件或交易进行签名的情况，我们建议您关闭所有使用早期示例的 POS 和 Hardware Station 设备，然后同时更新它们。 例如，通过更新商店的功能配置文件和 Hardware Station 的硬件配置文件，可以逐个对商店完成这种同时更新。

迁移过程应包含以下步骤。

1. 更新 Commerce Headquarters 组件。
1. 更新 Commerce Scale Unit 组件并启用当前示例的扩展。
1. 确保从启用脱机的 MPOS 设备同步所有脱机交易。
1. 关闭使用早期示例组件的所有设备。
1. 完成在[设置与控制单元的集成](emea-swe-fi-sample.md#setting-up-the-integration-with-control-units)中描述的所有必需设置任务。
1. 更新 POS 和 Hardware Station 组件，禁用早期示例中的扩展，并启用当前示例的扩展。

    > [!NOTE]
    > 根据环境类型，您可以在此主题的[开发环境中的迁移](#migration-in-a-development-environment)部分或[生产环境中的迁移](#migration-in-a-production-environment)部分中找到有关迁移过程的更多技术细节。

### <a name="migration-in-a-development-environment"></a>开发环境中的迁移

#### <a name="update-crt"></a>更新 CRT

1. 查找 **Runtime.Extensions.DocumentProvider.CleanCashSample** 项目并生成它。
2. 在 **Runtime.Extensions.DocumentProvider.CleanCashSample\\bin\\Debug** 文件夹中，查找 **Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll** 程序集文件。
3. 将程序集文件复制到 CRT 扩展文件夹：

    - **Commerce Scale Unit：** 将文件复制到 IIS Commerce Scale Unit 站点位置下的 **\\bin\\ext** 文件夹。
    - **Modern POS 上的本地 CRT：** 将文件复制到本地 CRT 客户端代理位置下的 **\\ext** 文件夹。

4. 查找 CRT 的扩展配置文件：

    - **Commerce Scale Unit：** 该文件名为 **CommerceRuntime.ext.config**，它位于 IIS Commerce Scale Unit 站点位置下的 **bin\\ext** 文件夹中。
    - **Modern POS 上的本地 CRT** 该文件名为 **CommerceRuntime.MPOSOffline.Ext.config**，位于本地 CRT 客户端代理位置下的 **bin\\ext** 文件夹中。

    > [!WARNING]
    > 请 **勿** 编辑 CommerceRuntime.config 和 CommerceRuntime.MPOSOffline.config 文件。 这些文件不适用于任何自定义项。

5. 从扩展配置文件中查找并删除较早的 CRT 扩展。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
    ```

    > [!WARNING]
    > 在更新使用此 CRT 实例的所有 POS 设备之前，请勿完成此步骤。

6. 通过添加以下行注册扩展配置文件中的当前示例 CRT 扩展。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

#### <a name="update-hardware-station"></a>更新 Hardware Station

1. 查找 **HardwareStation.Extension.CleanCashSample** 项目并生成它。
2. 在 **Extension.CleanCashSample\\bin\\Debug** 文件夹中，查找 **Contoso.Commerce.HardwareStation.CleanCashSample.dll** 和 **Interop.CleanCash\_1\_1.dll** 程序集文件。
3. 将程序集文件复制到 Hardware Station 扩展文件夹：

    - **共享的 Hardware Station：** 将文件复制到 IIS Hardware Station 站点位置下的 **bin** 文件夹。
    - **Modern POS 上的专用 Hardware Station：** 将此文件复制到 Modern POS 客户端代理位置下。

4. 查找 **HardwareStation.Extension.config** 扩展配置文件：

    - **远程 Hardware Station：** 此文件在 IIS Hardware Station 站点位置下。
    - **Modern POS 上的本地 Hardware Station：** 此文件在 Modern POS 客户端代理位置下。

    > [!WARNING]
    > 请 **勿** 编辑 CommerceRuntime.config 和 CommerceRuntime.MPOSOffline.config 文件。 这些文件不适用于任何自定义项。

5. 从扩展配置文件中查找并删除较早的 Hardware Station 扩展。

    # <a name="retail-73-and-earlier"></a>[Retail 7.3 及更早版本](#tab/retail-7-3)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-731-and-later"></a>[Retail 7.3.1 及更高版本](#tab/retail-7-3-1)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-100-and-later"></a>[Retail 10.0 及更高版本](#tab/retail-10-0)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
    ```
    ---

6. 将以下行添加到扩展配置文件的 **构成** 部分。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

#### <a name="update-modern-pos"></a>更新 Modern POS

1. 在 **RetailSdk\\POS** 下打开 **CloudPOS.sln** 解决方案。
2. 通过从 **extensions.json** 文件中删除以下行来禁用早期的 POS 扩展。

    ``` json
    {
        "baseUrl": "FiscalRegisterSample"
    }
    ```

2. 通过在 **extensions.json** 文件中添加以下行来启用当前示例 POS 扩展。

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="update-cloud-pos"></a>更新云 POS

1. 在 **RetailSdk\\POS** 下打开 **ModernPOS.sln** 解决方案。
2. 通过从 **extensions.json** 文件中删除以下行来禁用早期的 POS 扩展。

    ``` json
    {
        "baseUrl": "FiscalRegisterSample"
    }
    ```

2. 通过在 **extensions.json** 文件中添加以下行来启用当前示例 POS 扩展。

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

### <a name="migration-in-a-production-environment"></a>生产环境中的迁移

#### <a name="update-crt"></a>更新 CRT

1. 从 **RetailSdk\\Assets** 资产文件夹下的 **CommerceRuntime.ext.config** 和 **CommerceRuntime.MPOSOffline.Ext.config** 配置文件中删除早期 CRT 扩展。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
    ```

    > [!WARNING]
    > 在更新使用此 CRT 实例的所有 POS 设备之前，请勿完成此步骤。

2. 在 **RetailSdk\\Assets** 资产文件夹下的 **CommerceRuntime.ext.config** 和 **CommerceRuntime.MPOSOffline.Ext.config** 配置文件中进行以下更改，以启用当前示例 CRT 扩展。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

3. 在 **BuildTools** 文件夹下的 **Customization.settings** 包自定义配置文件中，添加以下行以在可部署包中包括当前示例 CRT 扩展。

    ``` xml
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll" />
    ```

#### <a name="update-hardware-station"></a>更新 Hardware Station

1. 通过修改 **HardwareStation.Extension.config** 配置文件，删除较早的 Hardware Station 扩展。

    # <a name="retail-73-and-earlier"></a>[Retail 7.3 及更早版本](#tab/retail-7-3)

    从 **HardwareStation.Shared.config** 和 **HardwareStation.Dedicated.config** 配置文件中删除以下部分。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-731-and-later"></a>[Retail 7.3.1 及更高版本](#tab/retail-7-3-1)

    从 **HardwareStation.Extension.config** 配置文件中删除以下部分。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-100-and-later"></a>[Retail 10.0 及更高版本](#tab/retail-10-0)

    从 **HardwareStation.Extension.config** 配置文件中删除以下部分。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
    ```
    ---

2. 通过将以下行添加到 **HardwareStation.Extension.config** 配置文件中的 **构成** 部分，启用当前示例 Hardware Station 扩展。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

3. 在 **BuildTools** 文件夹下的 **Customization.settings** 包自定义配置文件中进行以下更改：

    - 删除以下行以从可部署包中排除早期的 Hardware Station 扩展。

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample.dll" />
        ```

    - 添加以下行以在可部署包中包括当前示例 Hardware Station 扩展。

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.CleanCashSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Interop.CleanCash_1_1.dll" />
        ```

#### <a name="update-modern-pos"></a>更新 Modern POS

1. 在 **RetailSdk\\POS** 中打开 **CloudPOS.sln** 解决方案。
2. 禁用早期的 POS 扩展：

    - 在 **tsconfig.json** 文件中，将 **FiscalRegisterSample** 文件夹添加到排除列表。
    - 从 **RetailSDK\\POS\\Extensions** 文件夹下的 **extensions.json** 文件中删除以下几行。

        ``` json
        {
            "baseUrl": "FiscalRegisterSample"
        }
        ```

3. 通过在 **RetailSDK\\POS\\Extensions** 文件夹下的 **extensions.json** 文件中添加以下行来启用当前示例 POS 扩展。

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="update-cloud-pos"></a>更新云 POS

1. 在 **RetailSdk\\POS** 下打开 **ModernPOS.sln** 解决方案。
2. 禁用早期的 POS 扩展：

    - 在 **tsconfig.json** 文件中，将 **FiscalRegisterSample** 文件夹添加到排除列表。
    - 从 **RetailSDK\\POS\\Extensions** 文件夹下的 **extensions.json** 文件中删除以下几行。

        ``` json
        {
            "baseUrl": "FiscalRegisterSample"
        }
        ```

3. 通过在 **RetailSDK\\POS\\Extensions** 文件夹下的 **extensions.json** 文件中添加以下行来启用当前示例 POS 扩展。

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="create-deployable-packages"></a>创建可部署包

运行整个 Retail SDK 的 **msbuild** 以创建可部署包。 通过 LCS 或手动应用包。 有关详细信息，请参阅 [Retail SDK 包](../dev-itpro/retail-sdk/retail-sdk-packaging.md)。
