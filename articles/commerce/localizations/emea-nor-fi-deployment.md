---
title: 适用于挪威的收银机的部署指南
description: 本主题提供有关如何针对挪威 Microsoft Dynamics 365 Commerce 本地化启用收银机功能的指南。
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: c7e64dbfe6a300c097b5b3711ac4310f3386df11
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944732"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway"></a>适用于挪威的收银机的部署指南

[!include[banner](../includes/banner.md)]

本主题提供有关如何针对挪威 Microsoft Dynamics 365 Commerce 本地化启用收银机功能的指南。 本地化由多个组件扩展组成。 这些扩展允许您执行一些操作，例如在收据上打印自定义字段；在销售点 (POS) 中登记附加审计事件、销售交易和付款交易；对销售交易进行数字签名；以及以本地格式打印报告。 有关挪威本地化的详细信息，请参阅[挪威收银机功能](./emea-nor-cash-registers.md)。 有关如何为挪威配置 Commerce 的更多信息，请参阅[为挪威设置 Commerce](./emea-nor-cash-registers.md#setting-up-commerce-for-norway)。

> [!WARNING]
> 由于[新的独立包装和扩展模型](../dev-itpro/build-pipeline.md)的限制，它当前无法用于此本地化功能。 您必须在 Microsoft Dynamics Lifecycle Services (LCS) 中开发人员虚拟机 (VM) 上以前版本的 Retail 软件开发配套件 (SDK) 中使用挪威的数字签名示例版本。 有关详细信息，请参阅[适用于挪威的收银机的部署指南（旧版）](./emea-nor-loc-deployment-guidelines.md)。
>
> 以后的版本计划支持会计整合示例的新独立包装和扩展模型。

## <a name="set-up-fiscal-registration-for-norway"></a>设置挪威会计登记

挪威的会计登记示例基于[会计整合功能](fiscal-integration-for-retail-channel.md)，是 Retail SDK 的一部分。 该示例位于 [Dynamics 365 Commerce 解决方案](https://github.com/microsoft/Dynamics365Commerce.Solutions/)存储库的 **src\\FiscalIntegration\\SequentialSignatureNorway** 文件夹中（例如[版本/9.34 中的示例](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.34/src/FiscalIntegration/SequentialSignatureNorway)）。 该示例[包含](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices)一个会计单据提供程序和一个会计连接器（即 Commerce Runtime (CRT) 的扩展）。 有关如何使用 Retail SDK 的详细信息，请参阅 [Retail SDK 体系结构](../dev-itpro/retail-sdk/retail-sdk-overview.md)和[设置独立包装 SDK 的生成管道](../dev-itpro/build-pipeline.md)。

完成[设置 Commerce 渠道的会计整合](./setting-up-fiscal-integration-for-retail-channel.md)中所述的会计登记设置步骤：

1. [设置会计登记流程](./setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process)。 请务必记下[特定于挪威](#configure-the-fiscal-registration-process)的会计登记流程的设置。
1. [设置错误处理设置](./setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings)。
1. [启用已推迟会计登记的手动执行](./setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration)。
1. [配置渠道组件](#configure-channel-components)。

### <a name="configure-the-fiscal-registration-process"></a>配置会计登记流程

按照以下步骤在 Commerce Headquarters 启用挪威会计登记流程。

1. 从 Commerce SDK 中下载会计单据提供程序和会计连接器的配置文件：

    1. 打开 [Dynamics 365 Commerce 解决方案](https://github.com/microsoft/Dynamics365Commerce.Solutions/)存储库。
    1. 打开上一个可用版本分支（例如 **[版本/9.34](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.34)**）。
    1. 打开 **src \> FiscalIntegration \> SequentialSignatureNorway \> CommerceRuntime**。
    1. 下载 **DocumentProvider.SequentialSignNorway \> Configuration \> DocumentProviderSequentialSignatureNorwaySample.xml** 中的会计单据提供程序配置文件（例如，[版本/9.34 的文件](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.34/src/FiscalIntegration/SequentialSignatureNorway/CommerceRuntime/DocumentProvider.SequentialSignNorway/Configuration/DocumentProviderSequentialSignatureNorwaySample.xml)）。
    1. 下载 **Connector.SequentialSignNorway \> Configuration \> ConnectorSequentialSignatureNorwaySample.xml** 中的会计连接器配置文件（例如，[版本/9.34 的文件](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.34/src/FiscalIntegration/SequentialSignatureNorway/CommerceRuntime/Connector.SequentialSignNorway/Configuration/ConnectorSequentialSignatureNorwaySample.xml)）。

1. 转到 **Retail 和 Commerce \> Headquarters 设置 \> 参数 \> 共享参数**。 在 **常规** 选项卡上，将 **启用会计整合** 选项设置为 **是**。
1. 转到 **Retail 和 Commerce \> 渠道设置 \> 会计整合 \> 会计连接器**，并加载您之前下载的会计连接器配置文件。
1. 转到 **Retail 和 Commerce \> 渠道设置 \> 会计整合 \> 会计单据提供程序**，并加载您之前下载的会计单据提供程序配置文件。
1. 转至 **Retail 和 Commerce \> 渠道设置 \> 会计整合 \> 连接器功能配置文件**。 创建新的连接器功能配置文件，并选择您之前加载的单据提供程序和连接器。
1. 转至 **Retail 和 Commerce \> 渠道设置 \> 会计整合 \> 连接器技术配置文件**。 创建新的连接器技术配置文件，并选择您之前加载的连接器。 将连接器类型设置为 **内部**。
1. 转到 **Retail 和 Commerce \> 渠道设置 \> 会计整合 \> 会计连接器组**，并为您之前创建的连接器功能配置文件创建一个新的会计连接器组。
1. 转至 **Retail 和 Commerce \> 渠道设置 \> 会计整合 \> 会计登记流程**。 创建新的会计登记流程和一个会计登记流程步骤，并选择您之前创建的会计连接器组。
1. 转至 **Retail 和 Commerce \> 渠道设置 \> POS 设置 \> POS 配置文件 \> 功能配置文件**。 选择链接到应在其中激活登记流程的商店的功能配置文件。 在 **会计登记流程** 快速选项卡上，选择您之前创建的会计登记流程。 在 **会计服务** 快速选项卡上，选择您之前创建的连接器技术配置文件。 
1. 转到 **Retail 和 Commerce \> Retail 和 Commerce IT \> 分配计划**。 打开配送计划，然后选择作业 **1070** 和 **1090** 以将数据传输到渠道数据库。

### <a name="configure-the-digital-signature-parameters"></a>配置数字签名参数

您必须配置将用于在商店中对销售交易进行数字签名的证书。 存储在 Azure 密钥保管库中的数字证书用于进行签名。 对于 Modern POS 的离线模式，还可以使用存储在安装 Modern POS 的计算机的本地存储区中的数字证书进行签名。

您必须先完成以下步骤，然后才能使用存储在密钥保管库存储中的数字证书。

1. 必须创建密钥保管库存储。 我们建议您将存储与 Commerce Scale Unit 部署在同一地理区域中。
1. 必须将证书作为 base64 字符串密钥上传到密钥保管库存储。
1. 应用程序对象服务器 (AOS) 应用程序必须有权从密钥保管库存储中读取密钥。

有关如何使用密钥保管库的详细信息，请参阅[开始使用 Azure 密钥保管库](/azure/key-vault/key-vault-get-started)。

接下来，在 **密钥保管库参数** 页上，您必须指定用于访问密钥保管库存储的参数：

- **名称** 和 **说明** - 密钥保管库存储的名称和描述。
- **密钥保管库 URL** - 密钥保管库存储的 URL。
- **密钥保管库客户端** - 与用于进行身份验证的密钥保管库存储关联的 Azure Active Directory (Azure AD) 应用程序的交互式客户端 ID。 此客户端应有权从存储中读取密钥。
- **密钥保管库密钥** - 与密钥保管库存储中用于进行身份验证的 Azure AD 应用程序关联的密钥。
- **名称**、**描述** 和 **密钥引用** - 证书的名称、描述和密钥引用。

接下来，您必须为存储在密钥保管库或本地证书存储中的证书配置连接器。 此连接器用于在渠道端进行签名。

1. 转至 **Retail 和 Commerce \> 渠道设置 \> 会计整合 \> 连接器技术配置文件**。
1. 在 **设置** 快速选项卡上，为数字签名指定以下参数：

    - **密钥名称** - 选择您之前在 **密钥保管库参数** 页上配置的密钥名称。
    - **本地证书指纹** - 为本地存储的证书提供指纹。
    - **哈希算法** - 指定 Microsoft .NET 支持的一个加密哈希算法，如 **SHA1**。
    - **证书存储名称** - 此字段为可选字段。 使用它来指定应该用于搜索本地证书的默认存储名称。
    - **证书存储位置** - 此字段为可选字段。 使用它来指定应该用于搜索本地证书的默认存储位置。
    - **首先试用本地证书** - 选择此选项可默认使用本地存储中的证书（而不是密钥保管库中的证书）对数据进行签名。
    - **激活运行状况检查** - 有关运行状况检查功能的详细信息，请参阅[会计登记运行状况检查](./fiscal-integration-for-retail-channel.md#fiscal-registration-health-check)。

> [!NOTE]
> - 挪威当前仅可接受 **SHA1** 加密哈希算法。
> - 添加默认存储名称和存储位置，以简化在 CRT 中搜索本地证书的过程。 X509StoreProvider 具有存储证书的文件夹列表。 如果未指定默认存储名称和默认存储位置，则 X509StoreProvider 会尝试在其列表上的所有文件夹中查找证书。

### <a name="configure-channel-components"></a>配置渠道组件

### <a name="development-environment"></a>开发环境

执行以下步骤以设置开发环境，以便您可以测试和扩展示例。

1. 克隆或下载 [Dynamics 365 Commerce 解决方案](https://github.com/microsoft/Dynamics365Commerce.Solutions)存储库。 根据您的 SDK/应用程序版本选择正确的发布分支版本。 有关详细信息，请参阅[从 GitHub 和 NuGet 下载 Retail SDK 示例和引用包](../dev-itpro/retail-sdk/sdk-github.md)。
1. 在 **Dynamics365Commerce.Solutions\\FiscalIntegration\\SequentialSignatureNorway** 下打开 **SequentialSignatureNorway.sln** 解决方案，并生成它。
1. 安装 CRT 扩展：

    1. 查找 CRT 扩展安装程序：

        - **Commerce Scale Unit：** 在 **SequentialSignatureNorway\\ScaleUnit\\ScaleUnit.SequentialSignNorway.Installer\\bin\\Debug\\net461** 文件夹中，查找 **ScaleUnit.SequentialSignNorway.Installer** 安装程序。
        - **Modern POS 上的本地 CRT：** 在 **SequentialSignatureNorway\\ModernPOS\\ModernPos.SequentialSignNorway.Installer\\bin\\Debug\\net461** 文件夹中，查找 **ModernPos.SequentialSignNorway.Installer** 安装程序。

    1. 从命令行启动 CRT 扩展安装程序：

        - **Commerce Scale Unit：**

            ```Console
            ScaleUnit.SequentialSignNorway.Installer.exe install --verbosity 0
            ```

        - **Modern POS 上的本地 CRT：**

            ```Console
            ModernPOS.SequentialSignNorway.Installer.exe install --verbosity 0
            ```

### <a name="production-environment"></a>生产环境

按照[为会计整合示例设置生成管道](fiscal-integration-sample-build-pipeline.md)中的步骤生成和发布会计整合示例的 Cloud Scale Unit 和自助可部署包。 可在 [Dynamics 365 Commerce 解决方案](https://github.com/microsoft/Dynamics365Commerce.Solutions)存储库的 **Pipeline\\YAML_Files** 文件夹中找到 **SequentialSignatureNorway build-pipeline.yaml** 模板 YAML 文件。

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a>允许 Modern POS 在脱机模式下进行数字签名

若要允许 Modern POS 在脱机模式进行数字签名，您必须在新设备上激活 Modern POS 后执行这些步骤。

1. 登录 POS。
1. 在 **数据库连接状态** 页上，确保脱机数据库完全同步。 当 **待定下载** 字段的值为 **0**（零）时，数据库将完全同步。
1. 注销 POS。
1. 等待脱机数据库完全同步。
1. 登录 POS。
1. 在 **数据库连接状态** 页上，确保脱机数据库完全同步。 当 **脱机数据库中的待定交易记录** 字段的值为 **0**（零）时，数据库将完全同步。
1. 重新打开 Modern POS。
