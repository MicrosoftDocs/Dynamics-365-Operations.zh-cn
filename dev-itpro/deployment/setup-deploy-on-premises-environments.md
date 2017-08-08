---
title: "设置并部署本地环境"
description: "本主题提供关于如何计划、设置和部署本地环境的信息。"
author: kfend
manager: AnnBe
ms.date: 06/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: sarvanisathish
ms.search.validFrom: 2016-08-30T00:00:00.000Z
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 3e9a2e33d9579769f6808b598f865d75f072c450
ms.openlocfilehash: 7caf033ab2de5afd6a2d88fa2d41631df4542cbe
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---

# <a name="set-up-and-deploy-on-premises-environments"></a>设置并部署本地环境

本文档介绍如何计划你的部署、设置基础结构和部署 Microsoft Dynamics 365 for Finance and Operations Enterprise 版本（本地）。

## <a name="finance-and-operations-components"></a>Finance and Operations 组件

Finance and Operations 应用程序由三个主要组件构成：

- 应用程序对象服务器(AOS)
- 商业智能 (BI)
- 财务报告/Management Reporter

这些组件依赖于以下系统软件：

- Microsoft Windows Server 2016
- Microsoft SQL Server 2016 SP1，具有以下功能：

    - 启用了全文索引搜索。
    - SQL Server Reporting Services (SSRS)。
    - SQL Server Integration Services (SSIS)。
    
     > [!NOTE]
     > 如果未启用全文搜索，应用程序就不能运行。

- SQL Server Management Studio
- 独立 Microsoft Azure Service Fabric
- Windows PowerShell 5.0 或更高版本
- Windows Server 2016 上的 Active Directory 联合身份验证服务 (AD FS)

  域控制器必须是具有 2012 R2 域功能级别或更高级别的 Windows Server 2012 R2 或更高版本

  有关域功能级别的详细信息，请参阅： 
  - [什么是 Active Directory 功能级别](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
  - [了解 Active Directory 域服务功能级别](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)


## <a name="lifecycle-services"></a>Lifecycle Services

Finance and Operations 位通过 Microsoft Dynamics Lifecycle Services (LCS) 分布。 在可以部署之前，你必须通过[企业协议](https://www.microsoft.com/en-us/Licensing/licensing-programs/enterprise.aspx) 通道购买许可证密钥和在 LCS 中设置本地项目。 部署仅可通过 LCS 启动。 有关如何在 LCS 中设置本地项目的详细信息，请参阅[在 Lifecycle Services 中创建本地项目](../lifecycle-services/lbd-create-lcs-on-prem-project.md)。

## <a name="authentication"></a>身份验证

本地应用程序与 AD FS 一起使用。 若要与 LCS 交互，还必须配置 Azure Active Directory (Azure AD)。

## <a name="standalone-service-fabric"></a>独立 Service Fabric

Finance and Operations 使用独立 Service Fabric。 有关详细信息，请参阅 [Service Fabric 文档](/azure/service-fabric/)。

## <a name="infrastructure"></a>基础结构

Finance and Operations 用于在超聚合体系结构上使用。 硬件配置包括以下组件：

- 基于 Windows Server 2016 虚拟机 (VM) 的独立 Service Fabric 群集
- SQL Server（同时支持群集 SQL 和 Always-On）
- 用于身份验证的 AD FS
- 用于存储的服务器消息块 (SMB) 版本 3 文件共享
- 可选：Microsoft Office Server 2017

有关详细信息，请参阅[系统要求](../get-started/system-requirements.md) 和规模调整指南。

### <a name="hardware-layout"></a>硬件布局

基于[针对本地环境的硬件规模调整](../get-started/hardware-sizing-on-premises-environments.md) 中建议的规模调整计划你的基础结构和 Service Fabric 群集。 有关如何计划 Service Fabric 群集的详细信息，请参阅[计划和准备你的 Service Fabric 独立群集部署](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation)。

下表显示硬件布局的示例。 本主题中使用此例对设置进行说明。

> [!NOTE]
> Service Fabric 群集的主节点都必须至少有三个节点。 在此示例中，**OrchestratorType** 指定为主节点类型。

| 计算机用途                                 | 计算机名称    | IP 地址    |
|-------------------------------------------------|-----------------|---------------|
| 域控制器                               | DAX7SQLAODC1    | 10.179.108.2  |
| AD FS                                           | DAX7SQLAOADFS1  | 10.179.108.3  |
| 文件服务器                                     | DAX7SQLAOFILE1  | 10.179.108.4  |
| SQL Always-On 群集                           | DAX7SQLAOSQLA01 | 10.179.108.5  |
|                                                 | DAX7SQLAOSQLA02 | 10.179.108.6  |
|                                                 | DAX7SQLAOSQLA   | 10.179.108.9  |
| 客户                                          | SQLAOCLIENT1    | 10.179.108.11 |
| Service Fabric 群集/AOS 1                    | SQLAOSF1AOS1    | 10.179.108.12 |
| Service Fabric 群集/AOS 2                    | SQLAOSF1AOS2    | 10.179.108.13 |
| Service Fabric 群集/AOS 3                    | SQLAOSF1AOS3    | 10.179.108.14 |
| Service Fabric 群集/Orchestrator 1           | SQLAOSF1ORCH1   | 10.179.108.15 |
| Service Fabric 群集/Orchestrator 2           | SQLAOSF1ORCH2   | 10.179.108.16 |
| Service Fabric 群集/Orchestrator 3           | SQLAOSF1ORCH3   | 10.179.108.17 |
| Service Fabric 群集/Management Reporter 节点 | SQLAOSMR1       | 10.179.108.18 |
| Service Fabric 群集/SSRS 节点                | SQLAOSFBIN1     | 10.179.108.10 |

## <a name="setup"></a>设置

### <a name="prerequisites"></a>必备项

在开始设置之前，必须满足以下先决条件。 这些先决条件的设置超出了本文档的范围。

- 在你的网络中安装和配置 Active Directory 域服务 (AD DS)。
- 部署 AD FS。
- 安装 SQL Server、SSRS 和 Management Studio。

### <a name="overview"></a>概览

要设置 Finance and Operations 的基础结构，必须完成以下步骤。

1. 计划你的域名和 DNS 区域
2. 计划和购置你的证书
3. 计划你的用户和服务帐户
4. 创建 DNS 区域并添加 A 记录
5. 将 VM 加入到域
6. 将必备软件添加到 VM
7. 从 LCS 下载安装脚本
8. 描述你的配置
9. 安装证书
10. 设置独立 Service Fabric 群集
11. 为租户配置 LCS 连接
12. 设置文件存储
13. 设置 SQL Server
14. 配置数据库
15. 加密凭据
16. 设置 SSRS
17. 配置 AD FS

### <a name="plan-your-domain-name-and-dns-zones"></a>计划你的域名和 DNS 区域

我们建议你为 AOS 的生产安装使用公开注册的域名。 这样，如果需要外部访问，可以在外部网络访问。

例如，如果你公司的域是 contoso.com，你的 Finance and Operations（本地）区域可能是 d365ffo.onprem.contoso.com，主机名可能如下：

- ax.d365ffo.onprem.contoso.com，适用于 AOS 计算机
- sf.d365ffo.onprem.contoso.com，适用于 Service Fabric 群集

### <a name="plan-and-acquire-your-certificates"></a>计划和购置你的证书

要保护 Service Fabric 群集和部署的所有应用程序的安全，需要使用安全套接字层 (SSL) 证书。 对于你的生产和沙盒工作负荷，我们建议从证书颁发机构 (CA) 获取证书，例如 [DigiCert](https://www.digicert.com/ssl-certificate/)、[Comodo](https://ssl.comodo.com/)、[Symantec](https://www.websecurity.symantec.com/ssl-certificate)、[GoDaddy](https://www.godaddy.com/web-security/ssl-certificate) 或 [GlobalSign](https://www.globalsign.com/en/ssl/)。 如果你使用 [Active Directory 证书服务](https://technet.microsoft.com/en-us/library/cc772393(v=ws.10).aspx) (AD CS) 设置域，可以通过 AD CS 创建证书。 每个证书都必须包含一个为密钥交换而创建的私钥，而且它必须可导出到个人信息交换 (.pfx) 文件。

自签名证书仅可用于测试目的。 为了方便起见，安装脚本包括生成和导出自签名证书的脚本。 正如我们指出的，这些证书仅可用于测试目的。

| 目的                                      | 摘要 | 其他要求 |
|----------------------------------------------|-------------|-------------------------|
| SQL Server SSL 证书                   | 此证书用于加密通过网络在 SQL Server 实例和客户端应用程序之间传输的数据。 | <p>此证书的域名应与 SQL Server 实例或侦听程序的完全限定的域名 (FQDN) 匹配。</p><p>例如，如果 SQL 侦听程序在计算机 DAX7SQLAOSQLA 上进行托管，则证书的 DNS 名称为 DAX7SQLAOSQLA.onprem.contoso.com。</p> |
| Service Fabric Server 证书            | 此证书用于帮助保护 Service Fabric 节点之间的节点间通信的安全。 此证书也用作显示给连接到群集的客户端的服务器证书。 | <p>证书的域名必须与托管 AOS 和 Service Fabric 的 DNS 区域匹配。</p><p>例如，证书的域名可以是 \*.onprem.contoso.com 或 \*.contoso.com。</p><p>如果你使用通配符证书，通配符仅应用于一个级别。 如果是多个级别，必须将子域，主题备用名称 (SAN)，应用到证书，例如上一个示例中的 \*.contoso.com。</p> |
| Service Fabric 客户端证书            | 客户端使用此证书查看和管理 Service Fabric 群集。 | |
| 加密证书                     | 此证书用于加密敏感信息，例如 SQL Server 密码和用户帐户密码。 | <p>证书密钥使用必须包括数据加密 (10)，且不得包括服务器身份验证或客户端身份验证。</p><p>有关详细信息，请参阅[管理 Service Fabric 应用程序中的密钥](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-application-secret-management)。</p> |
| AOS SSL 证书                          | <p>此证书用作显示给 AOS 网站客户端的服务器证书。 它还用于启用 Windows Communication Foundation (WCF)/简单对象访问协议 (SOAP) 证书。</p><p>如果是通配符证书，在此处可使用 Service Fabric 服务器证书。</p> | <p>证书的域名必须与托管 AOS 和 Service Fabric 的 DNS 区域匹配。</p><p>例如，证书的域名可以是 \*.d365ffo.onprem.contoso.com、\*.onprem.contoso.com 或 \*.contoso.com。</p><p>如果你使用通配符证书，通配符仅应用于一个级别。 如果是多个级别，必须将子域 SAN 应用到证书，例如上一个示例中的 \*.contoso.com。</p> |
| 会话身份验证证书           | AOS 使用此证书帮助保护用户会话信息的安全。 | 这也是在从 LCS 进行部署时使用的**文件共享**证书。 |
| 数据加密和数据签名证书 | AOS 使用这些证书加密敏感信息。 | |
| 财务报告客户端证书       | 此证书用于帮助保护财务报告服务与 AOS 之间通信的安全。 | |
| 报告证书                        | 此证书用于帮助保护 SSRS 与 AOS 之间通信的安全。 | |
| 本地代理证书           | <p>此证书用于帮助保护本地托管的本地代理和 LCS 之间通信的安全。</p><p>此证书使本地代理可以代表你的 Azure AD 租户执行操作以及与 LCS 进行通信以协调和监控部署。</p> | |

### <a name="plan-your-users-and-service-accounts"></a>计划你的用户和服务帐户

你必须创建若干用户或服务帐户以使 Finance and Operations（本地）工作。 你必须创建组托管服务帐户 (gMSA)、域帐户和 SQL 帐户的组合。 下表显示用户帐户、其目的和将在本主题中使用的示例名称。

| 用户帐户                                            | 类型           | 目的 | 用户名 |
|---------------------------------------------------------|----------------|---------|-----------|
| 财务报告应用程序服务帐户         | gMSA           |         | Contoso\\svc-FRAS$ |
| 财务报告流程服务帐户             | gMSA           |         | Contoso\\svc-FRPS$ |
| 财务报告 Click Once 设计器服务帐户 | gMSA           |         | Contoso\\svc-FRCO$ |
| AOS 服务帐户                                     | gMSA           | 应创建此用户以供将来检验。 我们计划在即将推出的版本中让 AOS 与 gMSA 一起使用。 通过在设置时创建此用户，你将帮助保证顺利过渡到 gMSA。 | Contoso\\svc-AXSF$ |
| AOS 服务帐户                                     | 域科目 | AOS 在 GA 版本中使用此用户。 | Contoso\\AXServiceUser |
| AOS SQL DB 管理员用户                                   | SQL 用户       | Finance and Operations 使用此用户通过 SQL\* 进行身份验证。 此用户在即将推出的版本中还将被 gMSA 替代。 | AXDBAdmin |
| 本地部署代理服务帐户                  | gMSA           | 本地代理使用此帐户协调不同节点的部署。 | Contoso\\Svc-LocalAgent$ |

\* 用于 SQL 身份验证的 SQL 用户名和密码受到安全保护，因为它们已加密并存储在文件共享中。

### <a name="create-dns-zones-and-add-a-records"></a>创建 DNS 区域并添加 A 记录

DNS 与 AD DS 集成，让你能够组织、管理和查找网络中的资源。 为 AOS 主机名和 Service Fabric 群集创建一个 DNS 正向搜索区域和 A 记录。 在此示例设置中，DNS 区域名称是 d365ffo.onprem.contoso.com，A 记录/主机名如下所示：

- **ax**.d365ffo.onprem.contoso.com，适用于 AOS 计算机
- **sf**.d365ffo.onprem.contoso.com，适用于 Service Fabric 群集

#### <a name="add-a-dns-zone"></a>添加 DNS 区域

使用以下过程来添加 DNS 区域。

1. 登录到域控制器计算机，单击**开始**，并键入 **dnsmgmt.msc** 启动 DNS 管理器。
2. 右键单击域控制器名称，然后单击**新建区域** \> **下一步**。
3. 选择**主要区域**。
4. 选中**将区域存储在 Active Directory 中（仅当 DNS 服务器为可写入域控制器时才可用**复选框，然后单击**下一步**。
5. 选择**针对在此域：Contoso.com 中运行域控制器的所有 DNS 服务器**，然后单击**下一步**。
6. 选择**正向搜索区域**，然后单击**下一步**。
7. 为你的设置输入区域名称，然后单击**下一步**。 例如，输入 **d365ffo.onprem.contoso.com**。
8. 选择**不允许动态更新**，然后单击**下一步**。

#### <a name="set-up-an-a-record-for-aos"></a>为 AOS 设置 A 记录

在新的 DNS 区域中，为 **AOSNodeType** 类型的**每个** Service Fabric 群集节点创建一个命名为 **ax.d365ffo.onprem.contoso.com** 的 A 记录。 不要为其他节点类型创建 A 记录。

1. 右键单击新区域，然后单击**新主机**。
2. 输入 Service Fabric 节点（例如，10.179.108.12）的名称和 IP 地址，然后单击**添加新主机**。

#### <a name="set-up-an-a-record-for-the-orchestrator"></a>为 orchestrator 设置 A 记录

在新的 DNS 区域中，为 **OrchestratorType** 类型的**每个** Service Fabric 群集节点创建一个命名为 **sf.d365ffo.onprem.contoso.com** 的 A 记录。 不要为其他节点类型创建 A 记录。

1. 右键单击新区域，然后单击**新主机**。
2. 输入 Service Fabric 节点（例如，10.179.108.15）的名称和 IP 地址，然后单击**添加新主机**。

#### <a name="join-vms-to-the-domain"></a>将 VM 加入到域

通过完成[如何将 Windows Server 2016 加入到 Active Directory 域](http://www.tomsitpro.com/articles/join-windows-server-2016-to-ad-domain,2-1063.html) 中的步骤将每个 VM 加入到域。 或者，还可以使用 Windows PowerShell 脚本。

```
$domainName = Read-Host -Prompt 'Specify domain name (ex: contoso.com)'
Add-Computer -DomainName $domainName -Credential (Get-Credential -Message 'Enter domain credential')
Restart-Computer
```
一旦 VM 加入到域，将 AOS 服务帐户 (Contoso\svc-AXSF$, Contoso\svc-AXSF$) 添加到本地管理员组。 你可以查看[添加成员到本地组](https://technet.microsoft.com/en-us/library/cc772524(v=ws.11).aspx) 文章了解如何执行此操作。

#### <a name="disable-user-access-control"></a>禁用用户访问控制 

执行以下脚本以禁用**每个** Service Fabric 节点上的用户访问控制。
```
$RegPath = "HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System"
New-ItemProperty -Path $RegPath -Name "EnableLUA" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "ConsentPromptBehaviorAdmin" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "EnableUIADesktopToggle" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "LocalAccountTokenFilterPolicy" -Value 1 -PropertyType "DWORD" -Force
```
> [!IMPORTANT]
> 在脚本成功完成后，你必须重新启动节点。

#### <a name="add-prerequisite-software-to-vms"></a>将必备软件添加到 VM

下表列出必须应用到每个节点类型的计算机的必备软件。

> [!NOTE]
> 安装组件后，你必须重新启动你的计算机。

| 节点类型 | 组分 | 命令 |
|-----------|-----------|---------|
| AOS       | SNAC – ODBC 驱动程序 | 请参阅 [Microsoft ODBC Driver 13.1 for SQL Server - Windows + Linux](https://www.microsoft.com/en-us/download/details.aspx?id=53339)。 |
| AOS       | Microsoft .NET Framework 版本 2.0 - 3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| AOS       | Microsoft .NET Framework 版本 4.0 - 4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| AOS       | Internet 信息服务 (IIS) | `Add-WindowsFeature WAS, WAS-Process-Model, WAS-NET-Environment, WAS-Config-APIs`<br>`# Windows Process Activation Service`<br>`Add-WindowsFeature Web-Server, Web-WebServer, Web-Security, Web-Filtering, Web-App-Dev, Web-Net-Ext, Web-Mgmt-Tools, Web-Mgmt-Console` |
| AOS       | Microsoft SQL Server Management Studio 2016 | |
| AOS       | Microsoft Visual C++ Redistributable Packages for Microsoft Visual Studio 2013 | 请参阅 [Microsoft Visual C++ Redistributable Packages for Visual Studio 2013](https://support.microsoft.com/en-us/help/3179560)。 |
| AOS       | Microsoft Access 数据库引擎 2010 可再发行软件包 | 请参阅 [Microsoft Access 数据库引擎 2010 可再发行软件包](https://www.microsoft.com/en-us/download/details.aspx?id=13255) |
| BI        | .NET Framework 版本 2.0 - 3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| BI        | .NET Framework 版本 4.0 - 4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| BI        | Microsoft SQL Server 2016 SP1 | |
| BI        | Management Studio 2016 | |
| BI        | **本机**模式下的 SQL Server Reporting Services 2016 | |
| MR        | .NET Framework 版本 2.0 - 3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| MR        | .NET Framework 版本 4.0 - 4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| MR        | Visual C++ Redistributable Packages for Visual Studio 2013 | 请参阅 [Microsoft Visual C++ Redistributable Packages for Visual Studio 2013](https://support.microsoft.com/en-us/help/3179560)。 |

#### <a name="download-setup-scripts-from-lcs"></a>从 LCS 下载安装脚本

我们提供了若干脚本以帮助提高安装体验。 执行以下步骤以从 LCS 下载安装脚本。

1. 登录到 LCS (<https://lcs.dynamics.com/v2>)。
2. 在仪表板上，单击**共用资产库**磁贴。
3. 单击**模型**选项卡。
4. 在网格中，选择 **Dynamics 365 for Operations - 本地部署脚本**行。
5. 单击**版本**，并下载脚本的最新版本。

### <a name="describe-your-configuration"></a>描述你的配置

本节提供有关你必须运行的脚本的信息。 脚本按照你必须运行它们的顺序进行讨论。 若要运行脚本，则在 $(downloadPath)\\ConfigTemplate.xml 填写模板文件。 ConfigTemplate.xml 文件描述 Service Fabric 群集、用于配置它们的证书，以及必须授予对相关证书的访问权限的帐户。 在提供的示例中，填写的是用于本主题描述的示例基础结构的值。 模板文件用于下一部分。

#### <a name="create-the-domain-account-for-a-service-user"></a>为服务用户创建域帐户

运行以下命令，以创建域用户帐户，contoso\\AXServiceUser。

```
New-ADUser -Name 'AXServiceUser' `
    -AccountPassword (Read-Host -Prompt 'Specify User Password' -AsSecureString) `
    -PasswordNeverExpires $true -ChangePasswordAtLogon $false `
    -Enabled $true -UserPrincipalName 'AXServiceUser@contoso.com'
```

#### <a name="create-gmsas"></a>创建 gMSA

1. 将目录更改到 **$(DownloadPath)**，然后运行以下 Windows PowerShell 命令。

    > [!NOTE]
    > 此脚本不创建用户。 而是打印必须在域控制器计算机上手动运行的命令。

    ```
    # Generate gMSA account creation script (shows in console):
    .\Get-NewGMSAInDomainScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

2. 将命令的输出复制到 Windows PowerShell 窗口。 确保删除换行符，并使用提高的权限（右键单击，然后右键单击**以管理员身份运行**）在 Active Directory 域控制器计算机上运行行。
3. 在 Active Directory 域控制器计算机上运行以下脚本以验证帐户已成功创建。 确保你更换模式后运行与服务帐户的命名约定匹配的脚本。

    ```
    #Use this command to validate the gMSA accounts are added to AD.
    #Ensure to replace the Filter parameter with the pattern used to create your accounts.
    Get-ADServiceAccount -Filter { samAccountName -like "svc-*" }
    ```

4. 在客户端计算机上运行 Export-AddGMSAsONVMScript.ps1 脚本。 此脚本生成在每个 Service Fabric VM 上运行的脚本并将它们添加到对应于每个 VM 名称的文件夹。

    ```
    # Exports a script for installing gMSA on VM nodes into a directory VMs\<VMName>, again feed from XML
    .\Export-AddGMSAsOnVMScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

#### <a name="stop-iis"></a>停止 IIS

使用远程桌面协议 (RDP) 连接到每个 Service Fabric VM 并完成[开始或停止 Web 服务器 (IIS 7)](https://technet.microsoft.com/en-us/library/cc732317(v=ws.10).aspx) 中的手动步骤。 或者，也可以通过使用 RDP 使用以下 Windows PowerShell 脚本连接到每个 Service Fabric VM。

```
$ServiceName = "WAS"
$wasService = Get-Service $ServiceName -ErrorAction SilentlyContinue
if($wasService)
{
    $wasService.DependentServices | Stop-Service -Force -ErrorAction Continue
    $wasService | Stop-Service -ErrorAction Continue
    Set-Service $ServiceName -StartupType Disabled
}

$ServiceName = 'W3SVC'
$w3svc = Get-Service $ServiceName -ErrorAction SilentlyContinue
if($w3svc)
{
    $w3svc.DependentServices | Stop-Service -Force -ErrorAction Continue
    $w3svc | Stop-Service -ErrorAction Continue
    Set-Service $ServiceName -StartupType Disabled
}
```
_IIS 功能应安装但被禁用，因为产品中有 IIS dll 的某些依赖项。_

### <a name="install-certificates"></a>安装证书

1. 如果你从有效的 CA 购买了本主题中先前列出的证书，请填写 ConfigTemplate.xml 文件中的证书的 .pfx 文件名和指纹。 将 **generateSelfSignedCert** 属性设置为 **False**，将**可导出**属性设置为 **False**。 将 .pfx 文件复制到 $(DownloadPath)\\InfrastructureScripts\\Certs 文件夹。
2. 如果你使用自签名证书（仅为了测试目的），请运行以下脚本。 若要创建自签名证书，在 ConfigTemplate.xml 文件中，确保 **generateSelfSignedCert** 设置为 **True**，**可导出**设置为 **True**。 脚本将使用证书的指纹更新 XML。

    ```
    # Create self-signed certs (optionally, use -Display if you only want to see commands):
    # Note: this script is completely driven off ConfigTemplate.xml
    .\New-SelfSignedCertificates.ps1 -InputXml .\ConfigTemplate.xml
    ```

3. 导出具有私钥的新证书（.pfx 文件）。 使用以下脚本在 Windows PowerShell 中生成和运行导出命令。 .pfx 文件将放到 Certs 文件夹。

    ```
    # Exports Pfx files into a directory VMs\<VMName>, all the certs will reside in a folder named Certs\
    # Feeds from XML, if certs don't have passwords then you are prompted to enter one
    .\Export-PfxFiles.ps1 -InputXml .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > 证书必须已安装并在 cert:\\CurrentUser\\My 中存在。 证书也必须可导出。

    如果你使用自签名证书，请跳到下一部分。 你无需完成此过程。

4. 将 .pfx 文件导出或复制到 $(DownloadPath)\\InfrastructureScripts\\Certs 文件夹后，运行以下命令以生成将被放入对应于 VM 的文件夹中的脚本。

    ```
    # Exports script for adding ACLs to certs into a directory VMs\<VMName>
    .\Export-CertificateAclsForVMs.ps1 -InputXml .\ConfigTemplate.xml
    
    # Exports Import-PfxFiles.ps1 script for importing PFXs on VM nodes into a directory VMS\<VMname>:
    .\Export-ImportPfxFilesScript.ps1 -InputXml .\ConfigTemplate.xml
    
    .\Export-UnblockStrongNameScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

5. 将每个文件夹中的脚本复制到对应于文件夹名称的 VM。
6. 在每个 VM 上，按照其显示的顺序运行以下脚本。

    ```
    #Run this script only if it exists
    .\Add-GMSAOnVM.ps1
    
    .\Import-PfxFiles.ps1
    
    .\Set-CertificateAcls.ps1
    
    #Run this script only if it exists
    .\Unblock-StrongName.ps1
    ```

### <a name="set-up-a-standalone-service-fabric-cluster"></a>设置独立 Service Fabric 群集

1. 运行以下命令以生成 ClusterConfig.json 文件。

    ```
    .\New-SFClusterConfig.ps1 -InputXml .\ConfigTemplate.xml
    ```

    有关详细信息，请参阅[步骤 1B：创建多计算机群集](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster)、[使用 X.509 证书保护 Windows 上独立群集的安全](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-windows-cluster-x509-security) 和[创建在 Windows Server 上运行的独立群集](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster)。

2. 将 [Service Fabric 独立安装包](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#download-the-service-fabric-standalone-package) 下载到你的其中一个 Service Fabric 节点。 在下载 zip 文件后，请通过右键单击 zip 文件然后单击**属性**的方式解锁。 在对话框中，选择右下方的**解锁**复选框。
3. 将压缩文件复制到 Service Fabric 群集的其中一个节点，并解压缩它。
4. 运行以下命令以在所有节点的端口 443 和 445 上创建传入防火墙规则。

    ```
    #Create inbound Rule
    New-NetFirewallRule -DisplayName "SFInbound443445" -LocalPort 135, 137, 138, 139, 445, 443 -Direction Inbound -Enabled True -Protocol TCP
    
    #Test inbound Rule
    Get-NetFirewallRule -DisplayName "SFInbound443445"
    ```

5. 运行以下命令以在仅 SSRS 节点的端口 80 上创建传入防火墙规则。

    ```
    #Create inbound Rule
    New-NetFirewallRule -DisplayName "Reporting80" -LocalPort 80 -Direction Inbound -Enabled True -Protocol TCP
    
    #Test inbound Rule
    Get-NetFirewallRule -DisplayName "Reporting80"
    ```

6. 将你的 ClusterConfig.json 文件复制到独立 Service Fabric 的解压缩安装位置。
7. 使用提高的权限导航到 Windows PowerShell 中的解压缩安装位置，并且运行以下命令以测试 ClusterConfig。

    ```
    .\TestConfiguration.ps1 -ClusterConfigFilePath .\clusterConfig.json
    ```

8. 如果测试成功，请运行以下命令部署群集。

    ```
    .\CreateServiceFabricCluster.ps1 -ClusterConfigFilePath .\ClusterConfig.json
    ```

9. 在创建群集后，在任何客户端计算机上打开 Service Fabric 管理器以验证安装：

    1. 如果尚未安装，则在 CurrentUser\\My 中安装 Service Fabric 客户端证书。
    2. 转到 **IE 设置** \> **兼容性模式**，然后清除**显示兼容性模式中的 Intranet 站点**复选框。
    3. 转到 `https://sf.d365ffo.onprem.contoso.com:19080`，其中 sf.d365ffo.onprem.contoso.com 是区域中指定的 Service Fabric 群集的主机名。 如果没有配置 DNS 名称解析，请使用计算机的 IP 地址。
    4. 选择客户端证书。 此时将显示 **Service Fabric 管理器**页面。

### <a name="configure-lcs-connectivity-for-the-tenant"></a>为租户配置 LCS 连接

Finance and Operations 的部署和服务使用本地代理通过 LCS 进行协调。 若要建立从 LCS 到 Finance and Operations 租户的连接，必须配置证书以使本地代理能够代表你的 Azure AD 租户执行操作（如 Contoso.Onmicrosoft.com）。

使用你从 CA 获取的本地代理证书或你使用脚本生成的自签名证书。

仅具有全局管理员目录角色的用户帐户可以添加证书以授权 LCS。 默认情况下，为你的组织注册 Microsoft Office 365 的人员将是目录的全局管理员。

> [!NOTE]
> 必须一次对一位租户准确配置证书。 所有本地环境可以使用相同证书与 LCS 连接。

1. 在客户端计算机上下载和安装 Azure PowerShell 的最新版本。 有关详细信息，请参阅[安装和配置 Azure PowerShell](https://docs.microsoft.com/en-us/powershell/azure/install-azurerm-ps?view=azurermps-4.1.0&viewFallbackFrom=azurermps-4.0.0)。
2. 登录到[客户的 Azure 门户](https://portal.azure.com) 以验证你是否具有全局管理员目录角色。
3. 运行来自 $(DownloadPath)\\InfrastructureScripts 的以下脚本。

   ```
   .\AddCertToServicePrincipal.ps1 -CertificateThumbprint <OnPremLocalAgent Certificate Thumbprint>
   ```

### <a name="set-up-file-storage"></a>设置文件存储

必须设置两个高可用性的 SMB 3.0 文件存储。 有关如何启用 SMB 3.0 的信息，请参阅 [SMB 安全增强功能](https://technet.microsoft.com/en-us/library/dn551363(v=ws.11).aspx#BKMK_disablesmb1)。
安全的方言协商无法检测或阻止从 SMB 2.0 或 3.0 降级到 SMB 1.0。 因此，为了充分利用 SMB 加密的完整功能，我们强烈建议你禁用 SMB 1.0 服务器

> [!NOTE]
> 为了帮助保障你的数据在你的环境中处于静态时受到保护，必须在每一台计算机上启用 BitLocker 驱动器加密。 有关如何启用 BitLocker 的信息，请参阅 [BitLocker：如何在 Windows Server 2012 及更高版本上部署](https://docs.microsoft.com/en-us/windows/device-security/bitlocker/bitlocker-how-to-deploy-on-windows-server)。

- 存储上载到 AOS 的用户文档的文件共享（例如，\\\\DAX7SQLAOFILE1\\aos-storage）。
- 存储最新内部版本和配置文件以协调部署的文件共享（例如，\\\\DAX7SQLAOFILE1\\agent））

    > [!NOTE]
    > 保持此文件共享路径尽量短以避免超出将存入共享的文件的最大路径长度。

1. 在文件共享计算机上，运行以下命令。

    ```
    Install-WindowsFeature -Name FS-FileServer -IncludeAllSubFeature -IncludeManagementTools
    ```
#### <a name="set-up-the-dax7sqlaofile1aos-storage-file-share"></a>设置 \\\\DAX7SQLAOFILE1\\aos-storage 文件共享

2. 在服务器管理器中，选择**文件和存储服务** \> **共享**。
3. 单击**任务** \> **新的共享**以创建名称为 **aos-storage** 的新共享。
4. 在除 **OrchestratorNodeType** 以外的 Service Fabric 群集中为每台计算机授予**修改**权限。
5. 为用户 AOS 域用户 (contoso\\AXServiceUser) 和 gMSA 用户 (contoso\\svc-AXSF) 授予**修改**权限。

#### <a name="set-up-the-dax7sqlaofile1agent-file-share"></a>设置 \\\\DAX7SQLAOFILE1\\agent 文件共享

6. 返回到服务器管理器中，选择**文件和存储服务** \> **共享**。
7. 单击**任务** \> **新的共享**以连接名称为**代理**的新共享。
8. 为本地部署代理的 gMSA 用户 (contoso\\svc-LocalAgent$) 授予**完全控制**权限。

### <a name="set-up-sql-server"></a>设置 SQL Server

1. 安装高可用性的 SQL Server 2016 SP1，可以作为包括存储区域网络 (SAN) 的 SQL 群集或在 Always-On 配置中。  验证**数据库引擎、Reporting Services、全文搜索**和**管理工具**是否已安装。
> [!NOTE]
> 请确保根据[选择初始数据同步页（Always On 可用性组向导）](https://docs.microsoft.com/en-us/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards) 设置 SQL Always On 并按照[手动准备辅助数据库](https://docs.microsoft.com/en-us/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards#PrepareSecondaryDbs) 执行操作
2. 作为域用户运行 SQL Service。
3. 从 CA 获取 SSL 证书以配置 Finance and Operations。 为了测试目的，你可以创建和使用自签名证书。

**用于群集 SQL 实例的自签名证书**
   ```
   New-SelfSignedCertificate -CertStoreLocation "cert:\CurrentUser\My" -DnsName "DAX7SQLAOSQLA.contososqlao.com" -Provider "Microsoft Enhanced RSA and AES Cryptographic Provider" -Subject "DAX7SQLAOSQLA.contososqlao.com"
   ```
**用于 Always-On SQL 实例的自签名证书**
```
#https://www.derekseaman.com/2014/11/sql-2014-alwayson-ag-pt-13-ssl.html

# Create certificate for each SQL Node (i.e. 2 nodes = 2 certificates)
# Run script on each node
$computerName = $env:COMPUTERNAME.ToLower() 
$domain = $env:USERDNSDOMAIN.ToLower()
$listenerName = 'dax7sqlaosqla' 
$cert = New-SelfSignedCertificate -Subject "$computerName.$domain" -DnsName "$listenerName.$domain", $listenerName, $computerName -Provider 'Microsoft Enhanced RSA and AES Cryptographic Provider'

```
4. 使用证书，完成[如何使用微软管理终端程序为 SQL Server 的实例启用 SSL 加密](https://support.microsoft.com/en-us/help/316898/how-to-enable-ssl-encryption-for-an-instance-of-sql-server-by-using-microsoft-management-console) 中的步骤以对 SQL Server 配置 SSL。
5. 对于群集的每个节点，请执行以下步骤。 确保你对非活动节点进行更改并在进行更改后失败。

    1. 将证书导入 LocalMachine\\My。
    2. 向用于运行 SQL 服务的服务帐户授予证书权限。 在微软管理终端程序 (MMC) 中，右键单击证书 (certlm.msc)，然后单击**任务** \> **管理私钥**。
    3. 将证书指纹添加到 HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Microsoft SQL Server\\*MSSQL.x*\\MSSQLServer\\SuperSocketNetLib\\Certificate。
    4. 在 Microsoft SQL Server 配置管理器中，将 **ForceEncryption** 设置为**是**。

6. 导出证书的公钥（.cer 文件），并将其安装在每个 Service Fabric 节点的受信任的根。

### <a name="configure-the-orchestratordata-database"></a>配置 OrchestratorData 数据库

1.  创建一个空数据库，并命名为 **OrchestratorData**。 本地代理使用此数据库协调部署。
2.  授予本地代理在数据库上的 gMSA (svc-LocalAgent$) **db\_owner** 权限：

    1. 在树中，展开服务器名称，展开**安全性** \> **登录名**，然后右键单击，并单击**新建登录名**。

        ![新建登录名命令](./media/OPSetup_01_NewLogin.png)


    2. 查找 **svc-LocalAgent$** 服务帐户。 单击**位置**，并且选择**整个目录**，然后单击**对象类型**，并且选择**服务帐户**。

        ![选择用户、服务帐户或组对话框](./media/OPSetup_02_SelectUserServiceAccountOrGroupDialogBox.png)

    3. 将**分配 ServerRole** 设置为**公共**。
    4. 将 **db\_owner** 数据库角色权限分配到 OrchestratorData 数据库。

### <a name="configure-the-finance-and-operations-database"></a>配置 Finance and Operations 数据库

1. 登录到 LCS (<https://lcs.dynamics.com/v2>)。
2. 在仪表板上，单击**共用资产库**磁贴。
3. 单击**模型**选项卡 
4. 在网格中，单击 **Dynamics 365 for Operations 本地 Enterprise 版本 - 演示数据**行以下载 zip。
5. 邮政编码包含空的和演示数据 .bak 文件。 基于你的需要选择适当的 .bak 文件。 例如，如果你需要演示数据，则还原 AxBootstrapDB_Demodata.bak 文件。 
6. 还原 AxBootstrapDB_DemoData.bak 数据库。
7. 对数据库 **AXDBRAIN** 重命名。
8. 在还原的数据库上运行以下查询。

    ```
    ALTER DATABASE AXDBRAIN
    SET READ_COMMITTED_SNAPSHOT ON
    GO
    
    ALTER DATABASE AXDBRAIN
    SET ALLOW_SNAPSHOT_ISOLATION ON
    GO
    ```

4. 更新数据库文件：

    1. 右键单击数据库，然后单击**属性**。
    2. 单击**文件**以更改数据库文件属性。
    3. 在**初始大小 (MB)** 字段中，输入大于 5,120 的值。

        ![数据库属性对话框](./media/OPSetup_03_DatabasePropertiesDialogBox.png)

    4. 对于 **AXDBBuild\_Data**，将 **Autogrowth/Maximize** 字段设置为 **200** 兆字节 (MB)。
    5. 对于 **AXDBBuild\_Log**，将 **Autogrowth/Maximize** 字段设置为 **500** MB。

        ![更改 Autogrowth 对话框](./media/OPSetup_04_ChangeAutogrowthDialogBox.png)

5. 创建启用 SQL 身份验证的新用户 (axdbadmin)。
6. 使用下表中的信息映射用户和数据库角色。

    | 用户             | 类型    | 数据库角色 |
    |------------------|---------|---------------|
    | svc-AXSF$        | gMSA    | db\_owner     |
    | svc-LocalAgent$  | gMSA    | db\_owner     |
    | svc-FRPS$        | gMSA    | db\_owner     |
    | svc-FRAS$        | gMSA    | db\_owner     |
    | axdbadmin        | SqlUser | db\_owner     |

7. 授予 svc-AXSF$ 用户和 axdbadmin SQL 用户对 tempdb 数据库中的以下角色的访问权限：

    - db\_datareader
    - db\_datawriter
    - db\_ddladmin

8. 在 Management Studio 中，运行以下 Transact SQL (T-SQL) 命令：

    ```
    GRANT VIEW SERVER STATE TO axdbadmin
    GRANT VIEW SERVER STATE TO [contososqlao\svc-AXSF$]
    ```
9. 运行以下命令：
```
.\Reset-DatabaseUsers.ps1 -DatabaseServer ‘<FQDN of the SQL server>’ -DatabaseName '<AX database name>'
```

### <a name="configure-the-financial-reporting-database"></a>配置财务报告数据库

1.  创建一个空数据库，并命名为 **FinancialReporting**。
2.  使用下表中的信息映射用户和数据库角色。

    | 用户             | 类型 | 数据库角色 |
    |------------------|------|---------------|
    | svc-LocalAgent$  | gMSA | db\_owner     |
    | svc-FRPS$        | gMSA | db\_owner     |
    | svc-FRAS$        | gMSA | db\_owner     |

### <a name="encrypt-credentials"></a>加密凭据

1. 在任何客户端计算机上，请在 LocalMachine\\My 证书存储中安装加密证书。
2. 授予当前用户对此证书的私钥的读取访问权限。
3. 按照此处所示创建 Credentials.json 文件。

    ```
    {
        "AosPrincipal": {
            "AccountPassword": "<encryptedDomainUserPassword>"
        },
        "AosSqlAuth": {
            "SqlUser": "<encryptedSqlUser>",
            "SqlPwd": "<encryptedSqlPassword>"
        }
    }
    ```

    - **AccountPassword** 是 AOS 域用户 (contoso\\axserviceuser) 的加密的域用户密码。
    - **SqlUser** 是有权访问 Finance and Operations 数据库 (AXDBRAIN) 的加密的 SQL 用户 (axdbadmin)，**SqlPassword** 是加密的 SQL 密码。

4. 将 .json 文件复制到 SMB 文件共享，\\\\AX7SQLAOFILE1\\agent\\Credentials\\Credentials.json。
5. 使用加密的值更新 Credentials.json 文件。

    ```
    # Service fabric API to encrypt text and copy it to the clipboard.
    Invoke-ServiceFabricEncryptText -Text '<textToEncrypt>' -CertThumbprint '<DataEncipherment Thumbprint>' -CertStore -StoreLocation LocalMachine -StoreName My | clip
    ```

    1. 在 Credentials.json 中，使用加密的域密码替换 **\<encryptedDomainUserPassword\>**。
    2. 使用加密的 Finance and Operations SQL 用户替换 **\<encryptedSqlUser\>**。
    3. 使用 Finance and Operations SQL 密码替换 **\<encryptedSqlPassword\>**。
    
### <a name="set-up-ssrs"></a>设置 SSRS

1.  在你开始前，请确保已安装本主题开头列出的先决条件。
2.  按照步骤[为本地部署配置 SQL Server Reporting Services](../analytics/configure-ssrs-on-premises.md)。

### <a name="configure-ad-fs"></a>配置 AD FS

在你可以完成此过程之前，必须在 Windows Server 2016 上部署 AD FS。 有关如何部署 AD FS 的信息，请参阅[部署指南 Windows Server 2016 和 2012 R2 AD FS 部署指南](https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/deployment/windows-server-2012-r2-ad-fs-deployment-guide)。

Finance and Operations 要求超出 AD FS 的默认现成配置的额外配置。 对于以下步骤，Windows PowerShell 在安装了 AD FS 角色服务的计算机上运行。 用户帐户必须具有足够的权限管理 AD FS。 例如，用户必须拥有域管理员帐户。

1. 配置 AD FS 标识符，使其与 AD FS 令牌颁发者匹配。

    ```
    $adfsProperties = Get-AdfsProperties
    Set-AdfsProperties -Identifier $adfsProperties.IdTokenIssuer
    ```

2. 除非已经为混合环境配置 AD FS，否则应对内部网身份验证连接禁用 Windows 集成的身份验证 (WIA)。 有关如何配置 WIA 使其与 AD FS 一起使用的详细信息，请参阅[配置浏览器以将 Windows 集成的身份验证 (WIA) 与 AD FS 一起使用](https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/operations/configure-ad-fs-browser-wia)。

   ```
   Set-AdfsGlobalAuthenticationPolicy -PrimaryIntranetAuthenticationProvider FormsAuthentication, MicrosoftPassportAuthentication
   ```

3. 对于登录，用户的电子邮件地址必须是可接受的身份验证输入。

   ```
   Add-Type -AssemblyName System.Net
   $fdqn = ([System.Net.Dns]::GetHostEntry('localhost').HostName).ToLower()
   $domainName = $fdqn.Substring($fdqn.IndexOf('.')+1)
   Set-AdfsClaimsProviderTrust -TargetIdentifier 'AD AUTHORITY' -AlternateLoginID mail -LookupForests $domainName
   ```

为了使 AD FS 可以信任 Finance and Operations 用于身份验证交换，必须在 AD FS 应用程序组下的 AD FS 中注册不同的应用程序条目。 为了加快设置流程和帮助减少发生错误，可以使用以下脚本进行注册。 将 Publish-ADFSApplicationGroup.ps1 脚本和 D365FO-OP 目录复制到安装了 AD FS 角色服务的计算机。 然后使用具有足够权限管理 AD FS 的用户帐户（例如，管理员帐户）运行脚本。 有关如何使用脚本的详细信息，请参阅在脚本中列出的文档。 记下在输出中指定的客户端 ID，因为在 LCS 中的以后的某个步骤中将要求提供此信息。

```
# Host URL is your DNS record\host name for accessing the AOS
.\Publish-ADFSApplicationGroup.ps1 -HostUrl 'ax.d365ffo.onprem.contoso.com'
```

AD FS 管理控制台应类似于下面的示意图。 若要打开服务器管理器，请单击**工具** \> **AD FS 管理**，然后在左侧树视图的底部，单击**应用程序组**。 双击应用程序组以查看更多详细信息。

![应用程序组属性](./media/OPSetup_05_ApplicatioGroupProperties.png)

最后，为了进行健全性检查，请确保可以通过在 Web 浏览器中转到 `https://<adfs-dns-name>/adfs/.well-known/openid-configuration` 的方式访问 **AOSNodeType** 类型的 Service Fabric 节点上的 AD FS OpenID 配置 URL。 如果收到消息指出该站点不安全，说明你未将 AD FS SSL 证书添加到可信根证书主管机构存储。 此步骤在 AD FS 部署指南中进行描述。 如果你成功访问 URL，则返回包含你的 AD FS 配置的 JavaScript 对象表示法 (JSON)，且你将看到你的 AD FS URL 可信。

此时，基础结构的设置完成。 以下各节描述如何导航到 [LCS](https://lcs.dynamics.com) 以设置你的连接器和部署 Dynamics 365 for Finance and Operations 环境。

## <a name="configure-connector-and-install-on-premises-local-agent"></a>配置连接器和安装本地代理

1. 登录到 [LCS](https://lcs.dynamics.com/) 并打开本地实施项目。
2. 在汉堡包菜单上，单击**项目设置**。

    ![项目设置命令](./media/OPSetup_06_ProjectSettings.png)

3. 单击 **On-premises 连接器**。
4. 单击**添加**以创建新连接器。
5. 在**安装主机基础结构**选项卡上，下载代理安装程序。

    ![下载安装主机基础结构选项卡上的代理安装程序按钮。](./media/OPSetup_07_DownloadAgentInstaller.png)

6. 验证 zip 文件是否未锁定。 右键单击文件，单击**属性**，然后选择**解锁**。
7. 解压缩其中一个 **OrchestratorType** 类型的 Service Fabric 节点上的代理应用程序。
8. 在**配置代理**选项卡上，请输入配置设置。
9. 保存该配置，然后单击**下载配置**以下载 localagent-config.json 配置文件。

    ![下载配置代理选项卡上的配置按钮](./media/OPSetup_08_DownloadConfigurations.png)

10. 将 localagent-config.json 文件复制到代理安装程序包所在的计算机。
11. 在命令提示符窗口中，通过导航到包含代理安装程序的文件夹运行以下命令。

    ```
    LocalAgentCLI.exe Install <path to config.json>
    ```

    > [!NOTE]
    > 运行此命令的用户必须具有对 OrchestratorData 数据库的 **db\_owner** 权限。
    
12. 一旦本地代理安装成功，则导航回你在 LCS 中的本地连接器。
13. 在**验证安装**选项卡上，单击**消息代理**按钮。 这将测试与你的本地代理的 LCS 连接。 成功建立连接时，页面外观类似于下图。

     ![验证代理](./media/ValidateAgent.PNG)

## <a name="deploy-your-dynamics-365-for-finance-and-operations-on-premises-environment"></a>部署你的 Dynamics 365 for Finance and Operations（本地）环境

1. 导航到你在 LCS 中的本地项目，转到**环境**、**沙盒**，然后单击**配置**
2. 选择你的**环境拓扑**并浏览你的向导以启动部署。
3. 本地代理将提取部署请求、开始部署并在就绪后往回通信到 LCS。

