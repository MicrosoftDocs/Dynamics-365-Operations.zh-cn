---
title: 密封 Commerce 自助服务组件批量部署
description: 本主题介绍如何使用自助服务组件安装程序的框架静默安装和维护部署。
author: jashanno
ms.date: 05/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2021-04-30
ms.openlocfilehash: 5cb27fd0ea366d12c8bd6ee1cdb0c6d584375862
ms.sourcegitcommit: d70f66a98eff0a2836e3033351b482466bd9c290
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2022
ms.locfileid: "8741536"
---
# <a name="mass-deployment-of-sealed-commerce-self-service-components"></a>密封 Commerce 自助服务组件批量部署

[!include [banner](../includes/banner.md)]

本主题适用于密封框架，即从 10.0.18 版本开始每月发布的组件安装程序，这些安装程序在 Microsoft Dynamics Lifecycle Services (LCS) 的共用资产库中可用。 请注意，这些新安装程序的前几个版本被指定为 **（预览版）**。 但是，此指定的唯一目的是区分新的安装程序，而 Microsoft 则确定使用这些功能是否存在其他功能要求。 这并不意味着安装程序对生产无效。 根据这些新安装程序的发布，Microsoft 计划在 2023 年 10 月或前后弃用旧的（旧版）安装程序。 

本主题说明如何使用新安装程序通过命令行参数执行静默安装和服务更新。 这些参数允许您以几种不同的方式进行大规模部署。

> [!NOTE]
> Headquarters 中不会提供新的自助式密封安装程序，只能通过 LCS 下载这些程序。

## <a name="delimiters-for-mass-deployment"></a>大规模部署的分隔符

下表显示了可以在命令行执行中使用的分隔符。


| 分隔符                 | Description |
|---------------------------|-------------|
| --AadTokenIssuerPrefix | Microsoft Azure Active Directory (Azure AD) 令牌颁发者的前缀。 |
| --AsyncClientAadClientId | Async Client 在与 Headquarters 通信期间应使用的 Azure AD 客户端 ID。 |
| --AsyncClientAppInsightsInstrumentationKey | Async Client AppInsights 检测密钥。 |
| --AsyncClientCertFullPath | 完全格式化的 URN 路径，此路径使用指纹作为 Async Client 身份证书位置的搜索指标，此指标应该用于向 Azure AD 进行身份验证以与 Headquarters 通信。 例如，`store://My/LocalMachine?FindByThumbprint=<MyThumbprint>` 是格式正确的 URN。 值 **\<MyThumbprint\>** 将被替换为应使用的证书指纹。 不要将此参数与 **-AsyncClientCertThumbprint** 参数一起使用。 |
| --AsyncClientCertThumbprint | 应该用于向 Azure AD 进行身份验证以与 Headquarters 通信的 Async Client 标识证书的指纹 此指纹将用于搜索 **LocalMachine/我的商店** 位置和名称，以查找要使用的正确证书。 不要将此参数与 **-AsyncClientCertFullPath** 参数一起使用。 |
| --ClientAppInsightsInstrumentationKey | 客户端 AppInsights 检测密钥。 |
| --CloudPosAppInsightsInstrumentationKey | 云 POS AppInsights 检测密钥。 |
| --Config | 安装期间应使用的配置文件。 **Contoso.CommerceScaleUnit.xml** 是文件名的一个示例。 |
| --CposAadClientId | 云 POS 在设备激活期间应使用的 Azure AD 客户端 ID。 本地部署不需要此参数。 |
| --Device | 设备 ID，如 Headquarters 的 **设备** 页面上所示。 |
| --EnvironmentId | 环境 ID。 |
| --HardwareStationAppInsightsInstrumentationKey | Hardware Station AppInsights 检测键。 |
| --Install | 一个指定是否应安装此安装程序提供的组件的参数。 此参数不是必需参数。 |
| --InstallOffline | 对于 Modern POS，此参数指定还应安装和配置脱机数据库。 也使用 **-SQLServerName** 参数。 否则，安装程序将尝试查找满足先决条件的默认实例。 |
| --Port | 应与 Retail Server 虚拟目录关联并由其使用的端口。 如果未设置端口，将使用默认端口 443。 |
| --Register | 收银机 ID，如 Headquarters 的 **收银机** 页面上所示。 |
| --RetailServerAadClientId | Retail Server 在与 Headquarters 通信期间应使用的 Azure AD 客户端 ID。 |
| --RetailServerAadResourceId | 设备激活期间应使用的 Retail Server Azure AD 应用资源 ID。 本地部署不需要此参数。 |
| --RetailServerCertFullPath | 完全格式化的 URN 路径，此路径使用指纹作为 Retail Server 身份证书的搜索指标，此指标应该用于向 Azure AD 进行身份验证以与 Headquarters 通信。 例如，`store://My/LocalMachine?FindByThumbprint=<MyThumbprint>` 是格式正确的 URN，其中，值 **\<MyThumbprint\>** 将被替换为应使用的证书指纹。 不要将此参数与 **-RetailServerCertThumbprint** 参数一起使用。 |
| --RetailServerCertThumbprint | 应该用于向 Azure AD 进行身份验证以与 Headquarters 通信的 Retail Server 标识证书的指纹 此指纹将用于搜索 **LocalMachine/我的商店** 位置和名称，以查找要使用的正确证书。 不要将此参数与 **-RetailServerCertFullPath** 参数一起使用。 |
| --RetailServerURL | 安装程序应使用的 Retail Server URL。 （此 URL 也称为 Commerce Scale Unit \[CSU\] URL。）对于 Modern POS，将在设备激活期间使用此值。 |
| --SkipAadCredentialsCheck| 一个指示是否应跳过 Azure AD 凭据先决条件检查的开关。 默认值为 **false**。 |
| --SkipCertCheck | 一个指示是否应跳过证书先决条件检查的开关。 默认值为 **false**。 |
| --SkipIisCheck | 一个指示是否应跳过 Internet Information Services (IIS) 先决条件检查的开关。 默认值为 **false**。 |
| --SkipNetFrameworkCheck | 一个指示是否应跳过 .NET Framework 先决条件检查的开关。 默认值为 **false**。 |
| --SkipScaleUnitHealthcheck | 一个指示是否应跳过已安装组件的运行状况检查的开关。 默认值为 **false**。 |
| --SkipSChannelCheck | 一个指示是否应跳过安全通道先决条件检查的开关。 默认值为 **false**。 |
| --SkipSqlFullTextCheck | 一个指示是否应跳过需要全文搜索的 SQL Server 先决条件验证的开关。 默认值为 **false**。 |
| --SkipSqlServerCheck | 一个指示是否应跳过 SQL Server 先决条件检查的开关。 默认值为 **false**。 |
| --SqlServerName | SQL Server 名称。 如果未指定名称，安装程序将尝试查找默认实例。 |
| --SslcertFullPath | 完全格式化的 URN 路径，它使用指纹作为证书位置的搜索指标，此指标用于加密到缩放单元的 HTTP 流量。 例如，`store:\/\/My\/LocalMachine\?FindByThumbprint\=\<MyThumbprint\>` 是格式正确的 URN，其中，值 **\<MyThumbprint\>** 将被替换为应使用的证书指纹。 不要将此参数与 **-SslCertThumbprint** 参数一起使用。 |
| --SslCertThumbprint | 应该用于加密到缩放单元的 HTTP 流量的证书指纹。 此指纹将用于搜索 **LocalMachine/我的商店** 位置和名称，以查找要使用的正确证书。 不要将此参数与 **-SslCertFullPath** 参数一起使用。 |
| --StoreSystemAosUrl | Headquarters (AOS) URL。 |
| --StoreSystemChannelDatabaseId | 渠道数据库 ID（名称）。 |
| --TenantId | Azure AD 租户 ID。 |
| --TransactionServiceAzureAuthority | Transaction Service Azure AD 主管机构。 |
| --TransactionServiceAzureResource | Transaction Service Azure AD 资源。 |
| --TrustSqlServerCertificate | 一个指示在建立与 SQL Server 的连接时是否应信任服务器证书的开关。 为了帮助避免安全风险，生产部署绝不应在此处提供 **true** 值。 默认值为 **false**。 |
| --Verbosity | 安装期间请求的日志记录级别。 通常，不应使用此值。 |
| --WindowsPhoneAppInsightsInstrumentationKey | Hardware Station AppInsights 检测键。 |

## <a name="general-overview"></a>一般概览

自助服务安装程序的新框架具有各种功能和改进。 此新框架当前仅为 Modern POS、Hardware Station 和 CSU（自托管）生成安装程序。 了解密封安装程序的基本命令行使用方法非常重要，这应与以下示例中使用的内容相似。 
 
```Console
<Component Installer Name>.exe install --<Parameter Name> "<Parameter Information>"
```

安装程序需要使用参数 **install**（或用于删除安装的 **uninstall**）和特定于该安装的任何参数。 **参数名称** 应包含所需的任何参数，如收银机、CSU URL 或证书信息。 **参数信息** 应包含有关参数的任何附加信息。

已创建密封框架以允许进行以下更改：
- **已密封** - 新的安装程序框架将 Microsoft 分配的基础组件安装程序与基于扩展性的自定义项完全分开。 之后将安装自定义项，但随后将不受更新限制（因此仅允许更新 Microsoft 基本组件、自定义项或两者都允许更新）。
- **无 GUI** - 不再存在用户界面 (UI)。 相反，每个组件安装程序都有完全由命令行驱动的可执行项。 此更改是用于聚焦新安装程序框架以用于批量部署的多个关键更改或功能之一。
- **更深入的日志记录** - 增强的安装程序日志允许更好地验证安装是否完成或失败、执行的步骤以及生成的任何警告或错误。
- **清除** - 在新框架中，组件安装程序通过在安装较新组件之前清除组件文件夹的全部内容，更加努力地保持安装目录的清洁。 此清理可确保没有可能导致问题并阻止成功安装的剩余文件。

三个组件尚未迁移到新框架：虚拟外围设备模拟器、Async Server Connector service（用于 Dynamics AX 2012 R3 支持）和 Real-time Service 替换（用于 Dynamics AX 2012 R3 支持）。

> [!NOTE]
> 安装程序在本地存储并保留。  随着时间的推移，管理或删除保留的安装程序以免浪费磁盘空间非常重要。 建议保留基本组件的当前安装程序和最新版本的任何扩展安装程序，以便从极端情况中恢复。

## <a name="migration"></a>迁移

从旧的自助服务框架组件安装程序迁移到新的框架组件安装程序需要卸载旧组件。

- **Modern POS** - 新的安装程序框架使应用程序接收到一个新的应用程序签名 ID。 因此，在安装新框架 Modern POS 组件之前，需要完全卸载旧组件。 由于需要完全卸载，因此需要再次激活设备。 （此设备重新激活是一次性要求，前提是不再发生卸载。）
- **Hardware station** – 作为 IIS 网站，新的安装程序框架要求对基本文件夹结构进行重新设计。 因此，在安装新框架 Hardware station 组件之前，需要完全卸载旧组件。
- **Commerce Scale Unit（CSU，自托管）** - 作为一系列 IIS 网站，新的安装程序框架要求对基本文件夹结构进行重新设计。  因此，在安装新框架 CSU（自托管）组件之前，需要完全卸载旧组件。

## <a name="modern-pos"></a>Modern POS

### <a name="before-you-begin"></a>开始之前

删除旧的自助服务 Modern POS 组件至关重要。 有关详细信息，请参阅本主题中前面的迁移步骤。

### <a name="examples-of-silent-deployment"></a>静默部署示例

本节显示用于安装 Modern POS 的命令示例。

#### <a name="silently-install-modern-pos"></a>静默安装 Modern POS

以下命令将静默安装（或更新）Modern POS。 它具有标准命令结构，此结构用于对当前安装的组件进行静默维护。 该结构使用 **&lt;InstallerName&gt;.exe** 的基本值。

如果请求安装，则以下基本命令将展示可用选项。 强烈建议在首次测试或使用安装程序时使用此命令。

```Console
CommerceModernPOS.exe --help install
```

> [!NOTE]
> Modern POS 不需要配置文件。 安装程序现在具有在设备激活期间使用的各种值的参数（如本主题前面所示）。

以下命令指定安装 Modern POS 应用程序后在设备激活期间应使用的所有参数。 此示例使用 **Houston-3** 收银机，它是 Dynamics 365 Commerce 演示数据中常用的值。

```Console
CommerceModernPOS.exe install --Register "Houston-3" --Device "Houston-3" --RetailServerURL "https://MyDynamics365CommerceURL.dynamics.com/Commerce"
```

以下命令指定应该用于安装和配置脱机数据库的参数。 SQL Server 与应该使用的配置文件一起指定。

```Console
CommerceModernPOS.exe install --InstallOffline --SQLServerName "SQLExpress" --Config "ModernPOS.Houston-3.xml"
```

您可以混合搭配这些概念，以达到您想要的安装效果。

## <a name="hardware-station"></a>硬件工作站

### <a name="before-you-begin"></a>开始之前

删除旧的自助服务 Hardware station 组件至关重要。 有关详细信息，请参阅本主题中前面的迁移步骤。 不再存在商家帐户信息工具。 而是在 POS 终端与 Hardware station 配对时安装商家帐户信息。 首次测试此安装程序时，强烈建议您运行以下命令：

```Console
CommerceHardwareStation.exe --help install
```

### <a name="examples-of-silent-deployment"></a>静默部署示例

本节显示用于安装 Hardware station 的命令示例。

#### <a name="silently-install-hardware-station"></a>静默安装 Hardware Station

以下命令将静默安装（或更新）Hardware Station。 它具有标准命令结构，此结构用于维护当前安装的组件。 该结构使用 **&lt;InstallerName&gt;.exe** 的基本值。

以下基本命令运行可执行文件安装程序。

```Console
HardwareStation.exe install --Port 443 --StoreSystemAOSURL "https://MyDynamics365CommerceURL.dynamics.com/" --StoreSystemChannelDatabaseID "Houston" --SSLCertThumbprint "MySSLCertificateThumbprintOftenHasNumbers"
```

> [!NOTE]
> Hardware Station 不需要配置文件。 安装程序现在具有所需的各种值的参数（如本主题前面所示）。

以下命令指定在标准安装期间跳过先决条件检查所需的所有参数。 

> [!NOTE]
> 如果没有提前进行彻底测试，或者在开发情况下，不建议跳过检查。

```Console
HardwareStation.exe install --SkipFirewallUpdate --SkipOPOSCheck --SkipVersionCheck --SkipURLCheck --Config "HardwareStation.Houston.xml"
```

按照惯例，通常会混合搭配这些概念，以达到您想要的安装效果。

## <a name="commerce-scale-unit-self-hosted"></a>Commerce Scale Unit（自托管）

首次测试此安装程序时，强烈建议您运行以下命令：

```Console
CommerceStoreScaleUnitSetup.exe --help install
```

### <a name="before-you-begin"></a>开始之前

删除旧的自助服务 CSU（自托管）组件至关重要。 有关详细信息，请参阅本主题中前面的迁移步骤。

### <a name="examples-of-silent-deployment"></a>静默部署示例

本节显示用于安装 CSU（自托管）的命令示例。

#### <a name="silently-install-csu-self-hosted"></a>静默安装 CSU（自托管）

以下命令将静默安装（或更新）CSU（自托管）。 它具有标准命令结构，此结构用于对当前安装的组件进行静默维护。 该结构使用 **&lt;InstallerName&gt;.exe** 的基本值。

与其他自助安装程序相比，Commerce Scale Unit (CSU) 更复杂，需要相当多的附加信息。 以下命令是不存在配置文件时运行可执行文件安装程序所需的最少命令（带参数）。

```Console
CommerceScaleUnit.exe install --port 446 --SSLCertThumbprint "MySSLCertificateThumbprintOftenHasNumbers" --RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" --AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" --RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" --CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" --RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" --TrustSqlServerCertificate --Config "Contoso.StoreSystemSetup.xml"
```

> [!NOTE]
> CSU（自托管）仍需要配置文件。

以下命令是一个更彻底的命令，它使用一些替代参数运行可执行文件安装程序。

```Console
CommerceScaleUnit.exe install --Port 446 --SSLCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" --AsyncClientCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" --RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" --AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" --RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" --CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" --RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" --TrustSqlServerCertificate --Verbosity 0 --Config "Contoso.StoreSystemSetup.xml"
```

以下命令指定在标准安装期间跳过先决条件检查所需的参数。 

> [!NOTE]
> 如果没有提前进行彻底测试，或者在开发情况下，不建议跳过检查。


```Console
CommerceScaleUnit.exe installer --skipscaleunithealthcheck --skipcertcheck --skipaadcredentialscheck --skipschannelcheck --skipiischeck --skipnetcorebundlecheck --skipsqlservercheck --skipnetframeworkcheck --skipversioncheck --skipurlcheck --Config "Contoso.StoreSystemSetup.xml" --SSLCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" --AsyncClientCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" --RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" --AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" --RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" --CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" --RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" --TrustSqlServerCertificate
```

您可以混合搭配这些概念，以达到您想要的安装效果。

<!--## Mass deployment examples using InTune

This section will be added in a future update.

## Mass deployment examples using System Center Configuration Manager (SCCM)

This section will be added in a future update.-->

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
