---
title: 适用于挪威的收银机的部署指南（旧版）
description: 本文是一个部署指南，介绍如何针对挪威启用 Microsoft Dynamics 365 Commerce 本地化。
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2018-2-28
ms.openlocfilehash: 7a6450215f152779428d3b0fd83bf09761e2ad98
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894454"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway-legacy"></a>适用于挪威的收银机的部署指南（旧版）

[!include [banner](../includes/banner.md)]

本文是一个部署指南，介绍如何针对挪威启用 Microsoft Dynamics 365 Commerce 本地化。 本地化由多个 Commerce 组件扩展组成。 例如，这些扩展允许您在收据上打印自定义字段；在销售点 (POS) 中登记附加审计事件、销售交易和付款交易；对销售交易进行数字签名；以及以本地格式打印 X 和 Z 报表。 有关挪威本地化的详细信息，请参阅[挪威收银机功能](./emea-nor-cash-registers.md)。

此示例是 Retail 软件开发配套件 (SDK) 的一部分。 有关 SDK 的信息，请参阅 [Retail 软件开发套件 (SDK) 体系结构](../dev-itpro/retail-sdk/retail-sdk-overview.md)。

此示例由 Commerce runtime (CRT)、Retail Server 和 POS 的扩展组成。 若要运行此示例，您必须修改和生成 CRT、Retail Server 和 POS 项目。 我们建议您使用未修改的 Retail SDK 进行本文中描述的更改。 我们还建议您使用尚未更改任何文件的源代码管理系统，如 Microsoft Visual Studio Online (VSO)。

> [!NOTE]
> 在 Commerce 10.0.8 及以上版本中，Retail Server 称为 Commerce Scale Unit。 由于本文适用于应用的多个先前版本，因此在整个文章中使用的都是 *Retail Server*。
>
> 本文介绍的过程中的某些步骤有所不同，具体取决于您使用的 Commerce 版本。 有关详细信息，请参阅 [Dynamics 365 Retail 中的新增功能或更改](../get-started/whats-new.md)。

### <a name="using-certificate-profiles-in-commerce-channels"></a>在 Commerce 渠道中使用证书配置文件

在 Commerce 版本 10.0.15 及更高版本中，您可以使用[用于零售商店的用户定义的证书配置文件](./certificate-profiles-for-retail-stores.md)功能，在密钥保管库或 Commerce Headquarters 不可用时，该功能支持故障转移到脱机。 此功能扩展[管理零售渠道机密](../dev-itpro/manage-secrets.md)功能。

要在 CRT 扩展中应用此功能，请按照下列步骤操作。

1. 创建新的 CRT 扩展项目（C# 类库项目类型）。 使用 Retail 软件开发套件 (SDK) (RetailSDK\SampleExtensions\CommerceRuntime) 中的示例模板。

2. 在 SequentialSignatureRegister 项目中为 CertificateSignatureServiceRequest 添加自定义处理程序。

3. 将构造函数与 profileId 参数配合使用来读取密钥调用 `GetUserDefinedSecretCertificateServiceRequest`。 这将启动使用证书配置文件中的设置的功能。 根据设置，将从 Azure 密钥保管库或本地计算机存储中检索证书。

    ```csharp
    GetUserDefinedSecretCertificateServiceRequest getUserDefinedSecretCertificateServiceRequest = new GetUserDefinedSecretCertificateServiceRequest(profileId: "ProfileId", secretName: null, thumbprint: null, expirationInterval: null);
    GetUserDefinedSecretCertificateServiceResponse getUserDefinedSecretCertificateServiceResponse = request.RequestContext.Execute<GetUserDefinedSecretCertificateServiceResponse>(getUserDefinedSecretCertificateServiceRequest);

    X509Certificate2 Certificate = getUserDefinedSecretCertificateServiceResponse.Certificate;
    ```

4. 检索证书后，继续进行数据签名。

5. 生成 CRT 扩展项目。

6. 复制输出类库并将其粘贴到 ...\RetailServer\webroot\bin\Ext 以进行手动测试。

7. 在 CommerceRuntime.Ext.config 文件中，使用自定义库信息更新扩展构成部分。

## <a name="development-environment"></a>开发环境

完成这些步骤以设置开发环境，以便您可以测试和扩展示例。

### <a name="the-crt-extension-components"></a>CRT 扩展组件

CRT 示例中包含 CRT 扩展组件。 若要完成以下过程，请在 **RetailSdk\\SampleExtensions\\CommerceRuntime** 下面打开 CRT 解决方案 **CommerceRuntimeSamples.sln**。

#### <a name="receiptsnorway-component"></a>ReceiptsNorway 组件

1. 查找 **Runtime.Extensions.ReceiptsNorway** 项目并生成它。
2. 在 **Extensions.ReceiptsNorway\\bin\\Debug** 文件夹中，查找 **Contoso.Commerce.Runtime.ReceiptsNorway.dll** 程序集文件。
3. 将程序集文件复制到 CRT 扩展文件夹：

    - **Retail Server：** 将程序集复制到 Microsoft Internet Information Services (IIS) Retail Server 站点位置下的 **\\bin\\ext** 文件夹。
    - **Modern POS 上的本地 CRT：** 将程序集复制到本地 CRT 客户端代理位置下的 **\\ext** 文件夹。

4. 查找 CRT 的扩展配置文件：

    - **Retail Server：** 该文件名为 **Commerceruntime.ext.config**，它位于 IIS Retail Server 站点位置下的 **bin\\ext** 文件夹中。
    - **Modern POS 上的本地 CRT：** 该文件名为 **CommerceRuntime.MPOSOffline.Ext.config**，位于本地 CRT 客户端代理位置下。

5. 注册扩展配置文件中的 CRT 更改。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
    ```

    > [!WARNING]
    > 请 **勿** 编辑 commerceruntime.config 和 CommerceRuntime.MPOSOffline.config 文件。 这些文件不适用于任何自定义项。

#### <a name="salespaymenttransext-component"></a>SalesPaymentTransExt 组件

1. 查找 **Runtime.Extensions.SalesPaymentTransExt** 项目并生成它。
2. 在 **Extensions.SalesPaymentTransExt\\bin\\Debug** 文件夹中，查找 **Contoso.Commerce.Runtime.SalesPaymentTransExt.dll** 程序集文件。
3. 将程序集文件复制到 CRT 扩展文件夹：

    - **Retail Server：** 将程序集复制到 IIS Retail Server 站点位置下的 **\\bin\\ext** 文件夹。
    - **Modern POS 上的本地 CRT：** 将程序集复制到本地 CRT 客户端代理位置下的 **\\ext** 文件夹。

4. 查找 CRT 的扩展配置文件：

    - **Retail Server：** 该文件名为 **Commerceruntime.ext.config**，它位于 IIS Retail Server 站点位置下的 **bin\\ext** 文件夹中。
    - **Modern POS 上的本地 CRT：** 该文件名为 **CommerceRuntime.MPOSOffline.Ext.config**，位于本地 CRT 客户端代理位置下。

5. 注册扩展配置文件中的 CRT 更改。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
    ```

    > [!WARNING]
    > 请 **勿** 编辑 commerceruntime.config 和 CommerceRuntime.MPOSOffline.config 文件。 这些文件不适用于任何自定义项。

#### <a name="xzreportsnorway-component"></a>XZReportsNorway 组件

1. 查找 **Runtime.Extensions.XZReportsNorway** 项目并生成它。
2. 在 **Extensions.XZReportsNorway\\bin\\Debug** 文件夹中，查找 **Contoso.Commerce.Runtime.XZReportsNorway.dll** 程序集文件。
3. 将程序集文件复制到 CRT 扩展文件夹：

    - **Retail Server：** 将程序集复制到 IIS Retail Server 站点位置下的 **\\bin\\ext** 文件夹。
    - **Modern POS 上的本地 CRT：** 将程序集复制到本地 CRT 客户端代理位置下的 **\\ext** 文件夹。

4. 查找 CRT 的扩展配置文件：

    - **Retail Server：** 该文件名为 **Commerceruntime.ext.config**，它位于 IIS Retail Server 站点位置下的 **bin\\ext** 文件夹中。
    - **Modern POS 上的本地 CRT：** 该文件名为 **CommerceRuntime.MPOSOffline.Ext.config**，位于本地 CRT 客户端代理位置下。

5. 注册扩展配置文件中的 CRT 更改。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
    ```

    > [!WARNING]
    > 请 **勿** 编辑 commerceruntime.config 和 CommerceRuntime.MPOSOffline.config 文件。 这些文件不适用于任何自定义项。

# <a name="application-update-4"></a>[应用程序更新 4](#tab/app-update-4)

#### <a name="registerauditevent-sample-component"></a>RegisterAuditEvent 示例组件

1. 查找 **Runtime.Extensions.RegisterAuditEventSample** 项目并生成它。
2. 在 **Extensions.RegisterAuditEventSample\\bin\\Debug** 文件夹中，查找 **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** 程序集文件。
3. 将程序集文件复制到 CRT 扩展文件夹：

    - **Retail Server：** 将程序集复制到 IIS Retail Server 站点位置下的 **\\bin\\ext** 文件夹。
    - **Modern POS 上的本地 CRT：** 将程序集复制到本地 CRT 客户端代理位置下的 **\\ext** 文件夹。

4. 查找 CRT 的扩展配置文件：

    - **Retail Server：** 该文件名为 **Commerceruntime.ext.config**，它位于 IIS Retail Server 站点位置下的 **bin\\ext** 文件夹中。
    - **Modern POS 上的本地 CRT：** 该文件名为 **CommerceRuntime.MPOSOffline.Ext.config**，位于本地 CRT 客户端代理位置下。

5. 注册扩展配置文件中的 CRT 更改。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > 请 **勿** 编辑 commerceruntime.config 和 CommerceRuntime.MPOSOffline.config 文件。 这些文件不适用于任何自定义项。

#### <a name="salestransactionsignature-sample-component"></a>SalesTransactionSignature 示例组件

1. 查找 **Runtime.Extensions.SalesTransactionSignatureSample** 项目。
2. 通过为应该用于签署销售交易的证书指定指纹、商店位置和商店名称来修改 **App.config** 文件。
3. 构建项目。
4. 在 **Extensions.SalesTransactionSignatureSample\\bin\\Debug** 文件夹中，查找以下文件：

    - **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** 程序集文件
    - **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** 配置文件

5. 将文件复制到 CRT 扩展文件夹：

    - **Retail Server：** 将程序集复制到 IIS Retail Server 站点位置下的 **\\bin\\ext** 文件夹。
    - **Modern POS 上的本地 CRT：** 将程序集复制到本地 CRT 客户端代理位置下的 **\\ext** 文件夹。

6. 查找 CRT 的扩展配置文件：

    - **Retail Server：** 该文件名为 **Commerceruntime.ext.config**，它位于 IIS Retail Server 站点位置下的 **bin\\ext** 文件夹中。
    - **Modern POS 上的本地 CRT：** 该文件名为 **CommerceRuntime.MPOSOffline.Ext.config**，位于本地 CRT 客户端代理位置下。

7. 注册扩展配置文件中的 CRT 更改。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > 请 **勿** 编辑 commerceruntime.config 和 CommerceRuntime.MPOSOffline.config 文件。 这些文件不适用于任何自定义项。

# <a name="application-update-5-and-later"></a>[应用程序更新 5 及更高版本](#tab/app-update-5-and-later)

#### <a name="registerauditevent-sample-component"></a>RegisterAuditEvent 示例组件

1. 查找 **Runtime.Extensions.RegisterAuditEventSample** 项目并生成它。
2. 在 **Extensions.RegisterAuditEventSample\\bin\\Debug** 文件夹中，查找 **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** 程序集文件。
3. 将程序集文件复制到 CRT 扩展文件夹：

    - **Retail Server：** 将程序集复制到 IIS Retail Server 站点位置下的 **\\bin\\ext** 文件夹。
    - **Modern POS 上的本地 CRT：** 将程序集复制到本地 CRT 客户端代理位置下的 **\\ext** 文件夹。

4. 查找 CRT 的扩展配置文件：

    - **Retail Server：** 该文件名为 **Commerceruntime.ext.config**，它位于 IIS Retail Server 站点位置下的 **bin\\ext** 文件夹中。
    - **Modern POS 上的本地 CRT：** 该文件名为 **CommerceRuntime.MPOSOffline.Ext.config**，位于本地 CRT 客户端代理位置下。

5. 注册扩展配置文件中的 CRT 更改。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > 请 **勿** 编辑 commerceruntime.config 和 CommerceRuntime.MPOSOffline.config 文件。 这些文件不适用于任何自定义项。

#### <a name="salestransactionsignature-sample-component"></a>SalesTransactionSignature 示例组件

1. 查找 **Runtime.Extensions.SalesTransactionSignatureSample** 项目。
2. 通过为应该用于签署销售交易的证书指定指纹、商店位置和商店名称来修改 **App.config** 文件。
3. 构建项目。
4. 在 **Extensions.SalesTransactionSignatureSample\\bin\\Debug** 文件夹中，查找以下文件：

    - **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** 程序集文件
    - **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** 配置文件

5. 将文件复制到 CRT 扩展文件夹：

    - **Retail Server：** 将程序集复制到 IIS Retail Server 站点位置下的 **\\bin\\ext** 文件夹。
    - **Modern POS 上的本地 CRT：** 将程序集复制到本地 CRT 客户端代理位置下的 **\\ext** 文件夹。

6. 查找 CRT 的扩展配置文件：

    - **Retail Server：** 该文件名为 **Commerceruntime.ext.config**，它位于 IIS Retail Server 站点位置下的 **bin\\ext** 文件夹中。
    - **Modern POS 上的本地 CRT：** 该文件名为 **CommerceRuntime.MPOSOffline.Ext.config**，位于本地 CRT 客户端代理位置下。

7. 注册扩展配置文件中的 CRT 更改。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > 请 **勿** 编辑 commerceruntime.config 和 CommerceRuntime.MPOSOffline.config 文件。 这些文件不适用于任何自定义项。

#### <a name="salestransactionsignaturesamplemessages-component"></a>SalesTransactionSignatureSample.Messages 组件

1. 查找 **Runtime.Extensions.SalesTransactionSignatureSample.Messages** 项目。
2. 在 **Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** 文件夹中，查找 **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll** 程序集文件。
3. 将程序集文件复制到 CRT 扩展文件夹：

    - **Retail Server：** 将程序集复制到 IIS Retail Server 站点位置下的 **\\bin\\ext** 文件夹。
    - **Modern POS 上的本地 CRT：** 将程序集复制到本地 CRT 客户端代理位置下的 **\\ext** 文件夹。

4. 查找 CRT 的扩展配置文件：

    - **Retail Server：** 该文件名为 **Commerceruntime.ext.config**，它位于 IIS Retail Server 站点位置下的 **bin\\ext** 文件夹中。
    - **Modern POS 上的本地 CRT：** 该文件名为 **CommerceRuntime.MPOSOffline.Ext.config**，位于本地 CRT 客户端代理位置下。

5. 注册扩展配置文件中的 CRT 更改。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
    ```

    > [!WARNING]
    > 请 **勿** 编辑 commerceruntime.config 和 CommerceRuntime.MPOSOffline.config 文件。 这些文件不适用于任何自定义项。

# <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

#### <a name="registerauditevent-sample-component"></a>RegisterAuditEvent 示例组件

1. 查找 **Runtime.Extensions.RegisterAuditEventSample** 项目并生成它。
2. 在 **Extensions.RegisterAuditEventSample\\bin\\Debug** 文件夹中，查找 **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** 程序集文件。
3. 将程序集文件复制到 CRT 扩展文件夹：

    - **Retail Server：** 将程序集复制到 IIS Retail Server 站点位置下的 **\\bin\\ext** 文件夹。
    - **Modern POS 上的本地 CRT：** 将程序集复制到本地 CRT 客户端代理位置下的 **\\ext** 文件夹。

4. 查找 CRT 的扩展配置文件：

    - **Retail Server：** 该文件名为 **Commerceruntime.ext.config**，它位于 IIS Retail Server 站点位置下的 **bin\\ext** 文件夹中。
    - **Modern POS 上的本地 CRT：** 该文件名为 **CommerceRuntime.MPOSOffline.Ext.config**，位于本地 CRT 客户端代理位置下。

5. 注册扩展配置文件中的 CRT 更改。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > 请 **勿** 编辑 commerceruntime.config 和 CommerceRuntime.MPOSOffline.config 文件。 这些文件不适用于任何自定义项。

#### <a name="salestransactionsignature-sample-component"></a>SalesTransactionSignature 示例组件

1. 查找 **Runtime.Extensions.SalesTransactionSignatureSample** 项目。
2. 通过为应该用于签署销售交易的证书指定指纹、商店位置和商店名称来修改 **App.config** 文件。
3. 构建项目。
4. 在 **Extensions.SalesTransactionSignatureSample\\bin\\Debug** 文件夹中，查找以下文件：

    - **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** 程序集文件
    - **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** 配置文件

5. 将文件复制到 CRT 扩展文件夹：

    - **Retail Server：** 将程序集复制到 IIS Retail Server 站点位置下的 **\\bin\\ext** 文件夹。
    - **Modern POS 上的本地 CRT：** 将程序集复制到本地 CRT 客户端代理位置下的 **\\ext** 文件夹。

6. 查找 CRT 的扩展配置文件：

    - **Retail Server：** 该文件名为 **Commerceruntime.ext.config**，它位于 IIS Retail Server 站点位置下的 **bin\\ext** 文件夹中。
    - **Modern POS 上的本地 CRT：** 该文件名为 **CommerceRuntime.MPOSOffline.Ext.config**，位于本地 CRT 客户端代理位置下。

7. 注册扩展配置文件中的 CRT 更改。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > 请 **勿** 编辑 commerceruntime.config 和 CommerceRuntime.MPOSOffline.config 文件。 这些文件不适用于任何自定义项。

#### <a name="sequentialsignatureregistercontracts-component"></a>SequentialSignatureRegister.Contracts 组件

1. 查找 **Runtime.Extensions.SequentialSignatureRegister.Contracts** 项目并生成它。
2. 在 **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** 文件夹中，查找 **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** 程序集文件。
3. 将程序集文件复制到 CRT 扩展文件夹：

    - **Retail Server：** 将程序集复制到 IIS Retail Server 站点位置下的 **\\bin\\ext** 文件夹。
    - **Modern POS 上的本地 CRT：** 将程序集复制到本地 CRT 客户端代理位置下的 **\\ext** 文件夹。

# <a name="retail-732-and-later"></a>[Retail 7.3.2 及更高版本](#tab/retail-7-3-2)

#### <a name="registerauditevent-sample-component"></a>RegisterAuditEvent 示例组件

1. 查找 **Runtime.Extensions.RegisterAuditEventSample** 项目并生成它。
2. 在 **Extensions.RegisterAuditEventSample\\bin\\Debug** 文件夹中，查找 **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** 程序集文件。
3. 将程序集文件复制到 CRT 扩展文件夹：

    - **Retail Server：** 将程序集复制到 IIS Retail Server 站点位置下的 **\\bin\\ext** 文件夹。
    - **Modern POS 上的本地 CRT：** 将程序集复制到本地 CRT 客户端代理位置下的 **\\ext** 文件夹。

4. 查找 CRT 的扩展配置文件：

    - **Retail Server：** 该文件名为 **Commerceruntime.ext.config**，它位于 IIS Retail Server 站点位置下的 **bin\\ext** 文件夹中。
    - **Modern POS 上的本地 CRT：** 该文件名为 **CommerceRuntime.MPOSOffline.Ext.config**，位于本地 CRT 客户端代理位置下。

5. 注册扩展配置文件中的 CRT 更改。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > 请 **勿** 编辑 commerceruntime.config 和 CommerceRuntime.MPOSOffline.config 文件。 这些文件不适用于任何自定义项。

#### <a name="sequentialsignatureregister-component"></a>SequentialSignatureRegister 组件

1. 查找 **Runtime.Extensions.SequentialSignatureRegister** 项目。
2. 通过为应该用于签署销售交易的证书指定指纹、商店位置和商店名称来修改 **App.config** 文件。
3. 构建项目。
4. 在 **Extensions.SequentialSignatureRegister\\bin\\Debug** 文件夹中，查找以下文件：

    - **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** 程序集文件
    - **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** 配置文件

5. 将文件复制到 CRT 扩展文件夹：

    - **Retail Server：** 将程序集复制到 IIS Retail Server 站点位置下的 **\\bin\\ext** 文件夹。
    - **Modern POS 上的本地 CRT：** 将程序集复制到本地 CRT 客户端代理位置下的 **\\ext** 文件夹。

6. 查找 CRT 的扩展配置文件：

    - **Retail Server：** 该文件名为 **Commerceruntime.ext.config**，它位于 IIS Retail Server 站点位置下的 **bin\\ext** 文件夹中。
    - **Modern POS 上的本地 CRT：** 该文件名为 **CommerceRuntime.MPOSOffline.Ext.config**，位于本地 CRT 客户端代理位置下。

7. 注册扩展配置文件中的 CRT 更改。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > 请 **勿** 编辑 commerceruntime.config 和 CommerceRuntime.MPOSOffline.config 文件。 这些文件不适用于任何自定义项。

#### <a name="salestransactionsignaturenorway-component"></a>SalesTransactionSignatureNorway 组件

1. 查找 **Runtime.Extensions.SalesTransactionSignatureNorway** 项目。
2. 在 **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** 文件夹中，查找 **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** 程序集文件。
3. 将程序集文件复制到 CRT 扩展文件夹：

    - **Retail Server：** 将程序集复制到 IIS Retail Server 站点位置下的 **\\bin\\ext** 文件夹。
    - **Modern POS 上的本地 CRT：** 将程序集复制到本地 CRT 客户端代理位置下的 **\\ext** 文件夹。

4. 查找 CRT 的扩展配置文件：

    - **Retail Server：** 该文件名为 **Commerceruntime.ext.config**，它位于 IIS Retail Server 站点位置下的 **bin\\ext** 文件夹中。
    - **Modern POS 上的本地 CRT：** 该文件名为 **CommerceRuntime.MPOSOffline.Ext.config**，位于本地 CRT 客户端代理位置下。

5. 注册扩展配置文件中的 CRT 更改。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > 请 **勿** 编辑 commerceruntime.config 和 CommerceRuntime.MPOSOffline.config 文件。 这些文件不适用于任何自定义项。

#### <a name="sequentialsignatureregistercontracts-component"></a>SequentialSignatureRegister.Contracts 组件

1. 查找 **Runtime.Extensions.SequentialSignatureRegister.Contracts** 项目并生成它。
2. 在 **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** 文件夹中，查找 **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** 程序集文件。
3. 将程序集文件复制到 CRT 扩展文件夹：

    - **Retail Server：** 将程序集复制到 IIS Retail Server 站点位置下的 **\\bin\\ext** 文件夹。
    - **Modern POS 上的本地 CRT：** 将程序集复制到本地 CRT 客户端代理位置下的 **\\ext** 文件夹。

#### <a name="salespaymenttransextnorway-component"></a>SalesPaymentTransExtNorway 组件

1. 查找 **Runtime.Extensions.SalesPaymentTransExtNorway** 项目并生成它。
2. 在 **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** 文件夹中，查找 **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** 程序集文件。
3. 将程序集文件复制到 CRT 扩展文件夹：

    - **Retail Server：** 将程序集复制到 IIS Retail Server 站点位置下的 **\\bin\\ext** 文件夹。
    - **Modern POS 上的本地 CRT：** 将程序集复制到本地 CRT 客户端代理位置下的 **\\ext** 文件夹。

4. 查找 CRT 的扩展配置文件：

    - **Retail Server：** 该文件名为 **Commerceruntime.ext.config**，它位于 IIS Retail Server 站点位置下的 **bin\\ext** 文件夹中。
    - **Modern POS 上的本地 CRT：** 该文件名为 **CommerceRuntime.MPOSOffline.Ext.config**，位于本地 CRT 客户端代理位置下。

5. 注册扩展配置文件中的 CRT 更改。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > 请 **勿** 编辑 commerceruntime.config 和 CommerceRuntime.MPOSOffline.config 文件。 这些文件不适用于任何自定义项。

# <a name="retail-735-and-later"></a>[Retail 7.3.5 及更高版本](#tab/retail-7-3-5)

#### <a name="registerauditeventnorway-component"></a>RegisterAuditEventNorway 组件

1. 查找 CRT 的扩展配置文件：

    - **Retail Server：** 该文件名为 **Commerceruntime.ext.config**，它位于 IIS Retail Server 站点位置下的 **bin\\ext** 文件夹中。
    - **Modern POS 上的本地 CRT：** 该文件名为 **CommerceRuntime.MPOSOffline.Ext.config**，位于本地 CRT 客户端代理位置下。

2. 注册扩展配置文件中的 CRT 更改。

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
    ```

    > [!WARNING]
    > 请 **勿** 编辑 commerceruntime.config 和 CommerceRuntime.MPOSOffline.config 文件。 这些文件不适用于任何自定义项。

#### <a name="sequentialsignatureregister-component"></a>SequentialSignatureRegister 组件

1. 查找 **Runtime.Extensions.SequentialSignatureRegister** 项目。
2. 通过为应该用于签署销售交易的证书指定指纹、商店位置和商店名称来修改 **App.config** 文件。
3. 构建项目。
4. 在 **Extensions.SequentialSignatureRegister\\bin\\Debug** 文件夹中，查找以下文件：

    - **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** 程序集文件
    - **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** 配置文件

5. 将文件复制到 CRT 扩展文件夹：

    - **Retail Server：** 将程序集复制到 IIS Retail Server 站点位置下的 **\\bin\\ext** 文件夹。
    - **Modern POS 上的本地 CRT：** 将程序集复制到本地 CRT 客户端代理位置下的 **\\ext** 文件夹。

6. 查找 CRT 的扩展配置文件：

    - **Retail Server：** 该文件名为 **Commerceruntime.ext.config**，它位于 IIS Retail Server 站点位置下的 **bin\\ext** 文件夹中。
    - **Modern POS 上的本地 CRT：** 该文件名为 **CommerceRuntime.MPOSOffline.Ext.config**，位于本地 CRT 客户端代理位置下。

7. 注册扩展配置文件中的 CRT 更改。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > 请 **勿** 编辑 commerceruntime.config 和 CommerceRuntime.MPOSOffline.config 文件。 这些文件不适用于任何自定义项。

#### <a name="salestransactionsignaturenorway-component"></a>SalesTransactionSignatureNorway 组件

1. 查找 **Runtime.Extensions.SalesTransactionSignatureNorway** 项目。
2. 在 **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** 文件夹中，查找 **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** 程序集文件。
3. 将程序集文件复制到 CRT 扩展文件夹：

    - **Retail Server：** 将程序集复制到 IIS Retail Server 站点位置下的 **\\bin\\ext** 文件夹。
    - **Modern POS 上的本地 CRT：** 将程序集复制到本地 CRT 客户端代理位置下的 **\\ext** 文件夹。

4. 查找 CRT 的扩展配置文件：

    - **Retail Server：** 该文件名为 **Commerceruntime.ext.config**，它位于 IIS Retail Server 站点位置下的 **bin\\ext** 文件夹中。
    - **Modern POS 上的本地 CRT：** 该文件名为 **CommerceRuntime.MPOSOffline.Ext.config**，位于本地 CRT 客户端代理位置下。

5. 注册扩展配置文件中的 CRT 更改。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > 请 **勿** 编辑 commerceruntime.config 和 CommerceRuntime.MPOSOffline.config 文件。 这些文件不适用于任何自定义项。

#### <a name="sequentialsignatureregistercontracts-component"></a>SequentialSignatureRegister.Contracts 组件

1. 查找 **Runtime.Extensions.SequentialSignatureRegister.Contracts** 项目并生成它。
2. 在 **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** 文件夹中，查找 **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** 程序集文件。
3. 将程序集文件复制到 CRT 扩展文件夹：

    - **Retail Server：** 将程序集复制到 IIS Retail Server 站点位置下的 **\\bin\\ext** 文件夹。
    - **Modern POS 上的本地 CRT：** 将程序集复制到本地 CRT 客户端代理位置下的 **\\ext** 文件夹。

#### <a name="salespaymenttransextnorway-component"></a>SalesPaymentTransExtNorway 组件

1. 查找 **Runtime.Extensions.SalesPaymentTransExtNorway** 项目并生成它。
2. 在 **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** 文件夹中，查找 **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** 程序集文件。
3. 将程序集文件复制到 CRT 扩展文件夹：

    - **Retail Server：** 将程序集复制到 IIS Retail Server 站点位置下的 **\\bin\\ext** 文件夹。
    - **Modern POS 上的本地 CRT：** 将程序集复制到本地 CRT 客户端代理位置下的 **\\ext** 文件夹。

4. 查找 CRT 的扩展配置文件：

    - **Retail Server：** 该文件名为 **Commerceruntime.ext.config**，它位于 IIS Retail Server 站点位置下的 **bin\\ext** 文件夹中。
    - **Modern POS 上的本地 CRT：** 该文件名为 **CommerceRuntime.MPOSOffline.Ext.config**，位于本地 CRT 客户端代理位置下。

5. 注册扩展配置文件中的 CRT 更改。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > 请 **勿** 编辑 commerceruntime.config 和 CommerceRuntime.MPOSOffline.config 文件。 这些文件不适用于任何自定义项。

# <a name="retail-811-and-later"></a>[Retail 8.1.1 及更高版本](#tab/retail-8-1-1)

#### <a name="registerauditeventnorway-component"></a>RegisterAuditEventNorway 组件

1. 查找 CRT 的扩展配置文件：

    - **Retail Server：** 该文件名为 **Commerceruntime.ext.config**，它位于 IIS Retail Server 站点位置下的 **bin\\ext** 文件夹中。
    - **Modern POS 上的本地 CRT：** 该文件名为 **CommerceRuntime.MPOSOffline.Ext.config**，位于本地 CRT 客户端代理位置下。

2. 注册扩展配置文件中的 CRT 更改。

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
    ```

    > [!WARNING]
    > 请 **勿** 编辑 commerceruntime.config 和 CommerceRuntime.MPOSOffline.config 文件。 这些文件不适用于任何自定义项。

#### <a name="sequentialsignatureregister-component"></a>SequentialSignatureRegister 组件

1. 查找 **Runtime.Extensions.SequentialSignatureRegister** 项目。
2. 通过为应该用于签署销售交易的证书指定指纹、商店位置和商店名称来修改 **App.config** 文件。
3. 构建项目。
4. 在 **Extensions.SequentialSignatureRegister\\bin\\Debug** 文件夹中，查找以下文件：

    - **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** 程序集文件
    - **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** 配置文件

5. 将文件复制到 CRT 扩展文件夹：

    - **Retail Server：** 将程序集复制到 IIS Retail Server 站点位置下的 **\\bin\\ext** 文件夹。
    - **Modern POS 上的本地 CRT：** 将程序集复制到本地 CRT 客户端代理位置下的 **\\ext** 文件夹。

6. 查找 CRT 的扩展配置文件：

    - **Retail Server：** 该文件名为 **Commerceruntime.ext.config**，它位于 IIS Retail Server 站点位置下的 **bin\\ext** 文件夹中。
    - **Modern POS 上的本地 CRT：** 该文件名为 **CommerceRuntime.MPOSOffline.Ext.config**，位于本地 CRT 客户端代理位置下。

7. 注册扩展配置文件中的 CRT 更改。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > 请 **勿** 编辑 commerceruntime.config 和 CommerceRuntime.MPOSOffline.config 文件。 这些文件不适用于任何自定义项。

#### <a name="salestransactionsignaturenorway-component"></a>SalesTransactionSignatureNorway 组件

1. 查找 **Runtime.Extensions.SalesTransactionSignatureNorway** 项目。
2. 在 **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** 文件夹中，查找 **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** 程序集文件。
3. 将程序集文件复制到 CRT 扩展文件夹：

    - **Retail Server：** 将程序集复制到 IIS Retail Server 站点位置下的 **\\bin\\ext** 文件夹。
    - **Modern POS 上的本地 CRT：** 将程序集复制到本地 CRT 客户端代理位置下的 **\\ext** 文件夹。

4. 查找 CRT 的扩展配置文件：

    - **Retail Server：** 该文件名为 **Commerceruntime.ext.config**，它位于 IIS Retail Server 站点位置下的 **bin\\ext** 文件夹中。
    - **Modern POS 上的本地 CRT：** 该文件名为 **CommerceRuntime.MPOSOffline.Ext.config**，位于本地 CRT 客户端代理位置下。

5. 注册扩展配置文件中的 CRT 更改。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > 请 **勿** 编辑 commerceruntime.config 和 CommerceRuntime.MPOSOffline.config 文件。 这些文件不适用于任何自定义项。

#### <a name="sequentialsignatureregistercontracts-component"></a>SequentialSignatureRegister.Contracts 组件

1. 查找 **Runtime.Extensions.SequentialSignatureRegister.Contracts** 项目并生成它。
2. 在 **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** 文件夹中，查找 **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** 程序集文件。
3. 将程序集文件复制到 CRT 扩展文件夹：

    - **Retail Server：** 将程序集复制到 IIS Retail Server 站点位置下的 **\\bin\\ext** 文件夹。
    - **Modern POS 上的本地 CRT：** 将程序集复制到本地 CRT 客户端代理位置下的 **\\ext** 文件夹。

#### <a name="salespaymenttransextnorway-component"></a>SalesPaymentTransExtNorway 组件

1. 查找 **Runtime.Extensions.SalesPaymentTransExtNorway** 项目并生成它。
2. 在 **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** 文件夹中，查找 **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** 程序集文件。
3. 将程序集文件复制到 CRT 扩展文件夹：

    - **Retail Server：** 将程序集复制到 IIS Retail Server 站点位置下的 **\\bin\\ext** 文件夹。
    - **Modern POS 上的本地 CRT：** 将程序集复制到本地 CRT 客户端代理位置下的 **\\ext** 文件夹。

4. 查找 CRT 的扩展配置文件：

    - **Retail Server：** 该文件名为 **Commerceruntime.ext.config**，它位于 IIS Retail Server 站点位置下的 **bin\\ext** 文件夹中。
    - **Modern POS 上的本地 CRT：** 该文件名为 **CommerceRuntime.MPOSOffline.Ext.config**，位于本地 CRT 客户端代理位置下。

5. 注册扩展配置文件中的 CRT 更改。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > 请 **勿** 编辑 commerceruntime.config 和 CommerceRuntime.MPOSOffline.config 文件。 这些文件不适用于任何自定义项。

---

### <a name="the-retail-server-extension-components"></a>Retail Server 扩展组件

#### <a name="salestransactionsignature-retail-server-sample-component"></a>SalesTransactionSignature Retail Server 示例组件

1. 在 **RetailSDK\\SampleExtensions\\RetailServer\\RetailServer.Extensions.SalesTransactionSignatureSample** 文件夹中，查找 **RetailServer.Extensions.SalesTransactionSignatureSample** 项目并构建它。
2. 在 **RetailServer\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** 文件夹中，查找 **Contoso.RetailServer.SalesTransactionSignatureSample.dll** 程序集文件。
3. 将程序集文件复制到 Retail Server 扩展文件夹。

    # <a name="application-update-4"></a>[应用程序更新 4](#tab/app-update-4)

    该文件夹是 IIS Retail Server 站点位置下的 **\\bin** 文件夹。

    # <a name="application-update-5-and-later"></a>[应用程序更新 5 及更高版本](#tab/app-update-5-and-later)

    该文件夹是 IIS Retail Server 站点位置下的 **\\bin** 文件夹。

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    该文件夹是 IIS Retail Server 站点位置下的 **\\bin\\ext** 文件夹。

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 及更高版本](#tab/retail-7-3-2)

    该文件夹是 IIS Retail Server 站点位置下的 **\\bin\\ext** 文件夹。

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 及更高版本](#tab/retail-7-3-5)

    该文件夹是 IIS Retail Server 站点位置下的 **\\bin\\ext** 文件夹。

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 及更高版本](#tab/retail-8-1-1)

    该文件夹是 IIS Retail Server 站点位置下的 **\\bin\\ext** 文件夹。

    ---

4. 查找 Retail Server 的配置文件。 该文件名为 **web.config**，它位于 IIS Retail Server 站点位置下的根文件夹中。
5. 注册配置文件的 **extensionComposition** 部分中的 Retail Server 扩展。

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

6. 注册 Retail Server 扩展的依赖项。

    # <a name="application-update-4"></a>[应用程序更新 4](#tab/app-update-4/)

    1. 在 **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** 文件夹中，查找以下文件：

        - **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** 程序集文件
        - **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** 配置文件

    2. 将这些文件复制到 IIS Retail Server 站点位置下的 **\\bin** 文件夹。
    3. 注册 CRT 的扩展配置文件中的 CRT 更改。 该文件名为 **commerceruntime.ext.config**，它位于 IIS Retail Server 站点位置下的 **bin** 文件夹中。

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        ```

    # <a name="application-update-5-and-later"></a>[应用程序更新 5 及更高版本](#tab/app-update-5-and-later/)

    1. 在 **CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** 文件夹中，查找 **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll** 程序集文件。
    2. 将此文件复制到 IIS Retail Server 站点位置下的 **\\bin** 文件夹。
    3. 注册 CRT 的扩展配置文件中的 CRT 更改。 该文件名为 **commerceruntime.ext.config**，它位于 IIS Retail Server 站点位置下的 **bin** 文件夹中。

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
        ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > 不需要执行操作。

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 及更高版本](#tab/retail-7-3-2)

    > [!NOTE]
    > 不需要执行操作。

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 及更高版本](#tab/retail-7-3-5)

    > [!NOTE]
    > 不需要执行操作。

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 及更高版本](#tab/retail-8-1-1)

    > [!NOTE]
    > 不需要执行操作。

    ---

### <a name="the-modern-pos-extension-components"></a>Modern POS 扩展组件

#### <a name="implement-the-proxy-code-for-offline-mode"></a>实施脱机模式的代理代码

此部件等效于 Retail Server 控制器，但它扩展客户端未连接时所使用的本地 CRT。

1. 在 **customization.settings** 文件中，更改 **@(RetailServerLibraryPathForProxyGeneration)** 部分，以便使用新的 Retail Server 程序集进行代理生成。
2. 在 **StoreOperationsManager** 类中实施以下接口方法。 对于第一次迭代，请添加以下代码：

    # <a name="application-update-4"></a>[应用程序更新 4](#tab/app-update-4)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady()
    {
        throw new NotImplementedException();
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        throw new NotImplementedException();
    }
    ```

    # <a name="application-update-5-and-later"></a>[应用程序更新 5 及更高版本](#tab/app-update-5-and-later)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady(string correlationId)
    {
        throw new NotImplementedException();
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        throw new NotImplementedException();
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > 此步骤不适用于此版本。

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 及更高版本](#tab/retail-7-3-2)

    > [!NOTE]
    > 此步骤不适用于此版本。

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 及更高版本](#tab/retail-7-3-5)

    > [!NOTE]
    > 此步骤不适用于此版本。

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 及更高版本](#tab/retail-8-1-1)

    > [!NOTE]
    > 此步骤不适用于此版本。

    ---

3. 若要重新生成代理代码，请使用 **msbuild /t:Rebuild** 命令从命令行生成 **Proxies** 文件夹。
4. 解析 **Proxies.RetailProxy** 项目依赖项：

    # <a name="application-update-4"></a>[应用程序更新 4](#tab/app-update-4)

    打开 **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj**，将 **RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\CommerceRuntime.Extensions.SalesTransactionSignatureSample** 项目添加到解决方案中，并向 **RetailProxy** 项目添加项目引用，以引用 **SalesTransactionSignatureSample**。

    # <a name="application-update-5-and-later"></a>[应用程序更新 5 及更高版本](#tab/app-update-5-and-later)

    打开 **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj**，将 **RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\CommerceRuntime.Extensions.SalesTransactionSignatureSample.Messages** 项目添加到解决方案中，并向 **RetailProxy** 项目添加项目引用，以引用 **SalesTransactionSignatureSample.Messages**。

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > 此步骤不适用于此版本。

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 及更高版本](#tab/retail-7-3-2)

    > [!NOTE]
    > 此步骤不适用于此版本。

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 及更高版本](#tab/retail-7-3-5)

    > [!NOTE]
    > 此步骤不适用于此版本。

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 及更高版本](#tab/retail-8-1-1)

    > [!NOTE]
    > 此步骤不适用于此版本。

    ---

5. 在 **StoreOperationsManager** 类中调整接口方法：

    # <a name="application-update-4"></a>[应用程序更新 4](#tab/app-update-4)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady()
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<SalesTransactionSignatureServiceIsReadyResponse>(new SalesTransactionSignatureServiceIsReadyRequest(), null).IsReady);
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<GetLastFiscalTransactionResponse>(new GetLastFiscalTransactionRequest(), null).FiscalTransaction);
    }
    ```

    # <a name="application-update-5-and-later"></a>[应用程序更新 5 及更高版本](#tab/app-update-5-and-later)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady(string correlationId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<SalesTransactionSignatureServiceIsReadyResponse>(new SalesTransactionSignatureServiceIsReadyRequest(), null).IsReady);
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<GetLastFiscalTransactionResponse>(new GetLastFiscalTransactionRequest(), null).FiscalTransaction);
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > 此步骤不适用于此版本。

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 及更高版本](#tab/retail-7-3-2)

    > [!NOTE]
    > 此步骤不适用于此版本。

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 及更高版本](#tab/retail-7-3-5)

    > [!NOTE]
    > 此步骤不适用于此版本。

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 及更高版本](#tab/retail-8-1-1)

    > [!NOTE]
    > 此步骤不适用于此版本。

    ---

6. 更新 **dllhost.exe.config** 文件，以便客户端代理加载新的 RetailProxy 程序集。

    ``` xml
    <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy" />
    <add key="AdaptorCallerFullTypeName" value="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller" />
    ```

#### <a name="retail-proxy-extension-component-retail-731-and-later"></a>Retail 代理扩展组件（Retail 7.3.1 及更高版本）

仅在您使用 Retail 7.3.1 及更高版本时才完成以下过程。

1. 在 **RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample** 文件夹中，查找 **RetailServer.Extensions.SalesTransactionSignatureSample** 项目并构建它。
2. 在 **RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample\\bin\\Debug** 文件夹中，查找 **Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample** 程序集文件。
3. 将程序集文件复制到本地 CRT 客户端代理位置下的 **\\ext** 文件夹。
4. 注册扩展配置文件中的 Retail 代理更改。 该文件名为 **RetailProxy.MPOSOffline.ext.config**，位于本地 CRT 客户端代理位置下。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
    ```

#### <a name="modern-pos-extension-components"></a>Modern POS 扩展组件

1. 在 **RetailSdk\\POS\\ModernPOS.sln** 下打开此解决方案，并确保可以在不出错的情况下编译它。 此外，请确保您可以使用 **运行** 命令从 Microsoft Visual Studio 运行 Modern POS。

    > [!NOTE]
    > 不得自定义 Modern POS。 您必须启用用户帐户控制 (UAC)，并且必须根据需要卸载以前安装的 Modern POS 实例。

2. 在 **Pos.Extensions** 项目中包括以下现有源代码文件夹。

    # <a name="application-update-4"></a>[应用程序更新 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[应用程序更新 5 及更高版本](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 及更高版本](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 及更高版本](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 及更高版本](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

3. 通过从排除列表中删除以下文件夹，启用要在 **tsconfig.json** 中编译的扩展。

    # <a name="application-update-4"></a>[应用程序更新 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[应用程序更新 5 及更高版本](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 及更高版本](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 及更高版本](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 及更高版本](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

4. 通过在合适的位置中添加以下行来允许在 **extensions.json** 中加载扩展。

    # <a name="application-update-4"></a>[应用程序更新 4](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-later"></a>[应用程序更新 5 及更高版本](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 及更高版本](#tab/retail-7-3-2)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 及更高版本](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 及更高版本](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    ---

    > [!NOTE]
    > 有关详细信息，以及用于显示如何包括源代码文件夹和允许加载扩展的示例，请参阅 **Pos.Extensions** 项目内 readme.md 文件中的说明。

5. 重新生成解决方案。
6. 在调试器中运行 Modern POS 并测试功能。

### <a name="cloud-pos-extension-components"></a>Cloud POS 扩展组件

1. 在 **RetailSdk\\POS\\CloudPOS.sln** 下打开此解决方案，并确保可以在不出错的情况下编译它。
2. 在 **Pos.Extensions** 项目中包括以下现有源代码文件夹。

    # <a name="application-update-4"></a>[应用程序更新 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[应用程序更新 5 及更高版本](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 及更高版本](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 及更高版本](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 及更高版本](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

3. 通过从排除列表中删除以下文件夹，启用要在 **tsconfig.json** 中编译的扩展。

    # <a name="application-update-4"></a>[应用程序更新 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[应用程序更新 5 及更高版本](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 及更高版本](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 及更高版本](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 及更高版本](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

4. 通过在合适的位置中添加以下行来允许在 **extensions.json** 中加载扩展。

    # <a name="application-update-4"></a>[应用程序更新 4](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-later"></a>[应用程序更新 5 及更高版本](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 及更高版本](#tab/retail-7-3-2)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 及更高版本](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 及更高版本](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    ---

    > [!NOTE]
    > 有关详细信息，以及用于显示如何包括源代码文件夹和允许加载扩展的示例，请参阅 **Pos.Extensions** 项目内 readme.md 文件中的说明。

5. 重新生成解决方案。
6. 使用 **运行** 命令并执行 Retail SDK 手册中的步骤来运行解决方案。
7. 测试此功能。

### <a name="set-up-required-parameters-in-headquarters"></a>在 Headquarters 中设置必需参数

有关详细信息，请参阅[挪威收银机功能](./emea-nor-cash-registers.md)。

## <a name="production-environment"></a>生产环境

若要创建包含 Commerce 组件的可部署包，并在生产环境中应用这些包，请按照以下步骤操作。

1. 完成本文前面的 [Cloud POS 扩展组件](#cloud-pos-extension-components)或 [Modern POS 扩展组件](#modern-pos-extension-components)章节中的步骤。
2. 在 **RetailSdk\\Assets** 文件夹下的包配置文件中进行以下更改：

    1. 在 **commerceruntime.ext.config** 和 **CommerceRuntime.MPOSOffline.Ext.config** 配置文件中，将以下行添加到 **构成** 部分中。

        # <a name="application-update-4"></a>[应用程序更新 4](#tab/app-update-4)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="application-update-5-and-later"></a>[应用程序更新 5 及更高版本](#tab/app-update-5-and-later)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 及更高版本](#tab/retail-7-3-2)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 及更高版本](#tab/retail-7-3-5)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 及更高版本](#tab/retail-8-1-1)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        ---

    2. 启用 Commerce 代理自定义：

        # <a name="application-update-4"></a>[应用程序更新 4](#tab/app-update-4)

        在 **dllhost.exe.config** 配置文件中，将以下行添加到 **配置** 部分的 **appSettings** 子部分。

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="application-update-5-and-later"></a>[应用程序更新 5 及更高版本](#tab/app-update-5-and-later)

        在 **dllhost.exe.config** 配置文件中，将以下行添加到 **配置** 部分的 **appSettings** 子部分。

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        在 **RetailProxy.MPOSOffline.ext.config** 配置文件中，将以下行添加到 **构成** 部分：

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 及更高版本](#tab/retail-7-3-2)

        在 **RetailProxy.MPOSOffline.ext.config** 配置文件中，将以下行添加到 **构成** 部分：

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 及更高版本](#tab/retail-7-3-5)

        在 **RetailProxy.MPOSOffline.ext.config** 配置文件中，将以下行添加到 **构成** 部分：

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 及更高版本](#tab/retail-8-1-1)

        在 **RetailProxy.MPOSOffline.ext.config** 配置文件中，将以下行添加到 **构成** 部分：

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        ---

3. 在 **Customization.settings** 包自定义配置文件中进行以下更改：

    1. 启用 Retail 代理自定义。

        # <a name="application-update-4"></a>[应用程序更新 4](#tab/app-update-4)

        将以下行添加到 **&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;** 部分。

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="application-update-5-and-later"></a>[应用程序更新 5 及更高版本](#tab/app-update-5-and-later)

        将以下行添加到 **&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;** 部分。

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        将以下行添加到 **ItemGroup** 部分以在可部署包中包括 Retail 代理扩展：

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 及更高版本](#tab/retail-7-3-2)

        将以下行添加到 **ItemGroup** 部分以在可部署包中包括 Retail 代理扩展：

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 及更高版本](#tab/retail-7-3-5)

        将以下行添加到 **ItemGroup** 部分以在可部署包中包括 Retail 代理扩展：

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 及更高版本](#tab/retail-8-1-1)

        将以下行添加到 **ItemGroup** 部分以在可部署包中包括 Retail 代理扩展：

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        ---

    2. 将以下行添加到 **ItemGroup** 部分以在可部署包中包括 CRT 扩展：

        # <a name="application-update-4"></a>[应用程序更新 4](#tab/app-update-4)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="application-update-5-and-later"></a>[应用程序更新 5 及更高版本](#tab/app-update-5-and-later)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 及更高版本](#tab/retail-7-3-2)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 及更高版本](#tab/retail-7-3-5)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 及更高版本](#tab/retail-8-1-1)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        ---

    3. 将以下行添加到 **ItemGroup** 部分以在可部署包中包括 Retail Server 扩展：

        # <a name="application-update-4"></a>[应用程序更新 4](#tab/app-update-4)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        ```

        # <a name="application-update-5-and-later"></a>[应用程序更新 5 及更高版本](#tab/app-update-5-and-later)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 及更高版本](#tab/retail-7-3-2)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 及更高版本](#tab/retail-7-3-5)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 及更高版本](#tab/retail-8-1-1)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        ---

4. 修改以下文件以将挪威的资源文件包括在可部署包中：
    - Packages\_SharedPackagingProjectComponents\Sdk.ModernPos.Shared.csproj
    - Packages\RetailServer\Sdk.RetailServerSetup.proj
  
  - 对于 **Sdk.ModernPos.Shared.csproj** 文件 
    - 将行添加到 **ItemGroup** 部分
    
        ``` xml
        <<File_name> Include="$(SdkReferencesPath)\nb-NO\*" />
        ```
    > [!Note]
    > 指定资源文件的名称，而不是指定 <File_name>。 此资源文件与下面提供的其他示例相关。
 
    - 将行添加到 **Target Name="CopyPackageFiles"** 部分
       ``` xml
        <Copy SourceFiles="@(<File_name>)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\nb-NO" SkipUnchangedFiles="true" />
        ```
  
  - 对于 **Sdk.RetailServerSetup.proj** 文件 
    - 将行添加到 **ItemGroup** 部分
        ``` xml
        <<File_name> Include="$(SdkReferencesPath)\nb-NO\*" />
        ```    
    - 将行添加到 **Target Name="CopyPackageFiles"** 部分
         ``` xml
        <Copy SourceFiles="@(<File_name>)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\nb-NO" SkipUnchangedFiles="true" />
        ```    

5. 通过为应该用于签署销售交易的证书指定指纹、商店位置和商店名称来修改证书配置文件。 然后将配置文件复制到 **References** 文件夹。

    # <a name="application-update-4"></a>[应用程序更新 4](#tab/app-update-4)

    该文件名为 **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**，它在 **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** 下。

    # <a name="application-update-5-and-later"></a>[应用程序更新 5 及更高版本](#tab/app-update-5-and-later)

    该文件名为 **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**，它在 **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** 下。

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    该文件名为 **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**，它在 **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** 下。

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 及更高版本](#tab/retail-7-3-2)

    该文件名为 **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**，它在 **Extensions.SequentialSignatureRegister\\bin\\Debug** 下。

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 及更高版本](#tab/retail-7-3-5)

    该文件名为 **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**，它在 **Extensions.SequentialSignatureRegister\\bin\\Debug** 下。

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 及更高版本](#tab/retail-8-1-1)

    该文件名为 **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**，它在 **Extensions.SequentialSignatureRegister\\bin\\Debug** 下。

    ---

6. 更新 Retail Server 配置文件。 在 **RetailSDK\\Packages\\RetailServer\\Code\\web.config** 文件中，将以下行添加到 **extensionComposition** 部分。

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

7. 运行整个 Retail SDK 的 **msbuild** 以创建可部署包。
8. 通过 Microsoft Dynamics Lifecycle Services (LCS) 或手动应用包。 有关详细信息，请参阅[创建可部署包](../dev-itpro/retail-sdk/retail-sdk-packaging.md)。

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a>允许 Modern POS 在脱机模式下进行数字签名

若要允许 Modern POS 在脱机模式进行数字签名，您必须在新设备上激活 Modern POS 后执行这些步骤。

1. 登录 POS。
2. 在 **数据库连接状态** 页上，确保脱机数据库完全同步。 当 **待定下载** 字段的值为 **0**（零）时，数据库将完全同步。
3. 注销 POS。
4. 等待脱机数据库完全同步。
5. 登录 POS。
6. 在 **数据库连接状态** 页上，确保脱机数据库完全同步。 当 **脱机数据库中的待定交易记录** 字段的值为 **0**（零）时，数据库将完全同步。
7. 重新启动 Modern POS。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
