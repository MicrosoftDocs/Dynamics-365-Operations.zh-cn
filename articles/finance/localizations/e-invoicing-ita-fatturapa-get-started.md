---
title: 设置意大利 FatturaPA 与 SDI 的直接集成
description: 本文提供的信息将帮助您开始使用适用于意大利的电子开票功能，并设置意大利 FatturaPA 与 Exchange 系统 (SDI) 的直接集成。
author: abaryshnikov
ms.date: 07/27/2022
ms.topic: article
audience: Application User, Developer
ms.reviewer: kfend
ms.search.region: Global
ms.author: abaryshnikov
ms.search.validFrom: 2021-10-18
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 363b7b5e3d5abbb990fea8f8ad4d0c1bebf80102
ms.sourcegitcommit: 6d9fcb52d723ac5022a3002e0ced8e7b56e9bc2a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/27/2022
ms.locfileid: "9203160"
---
# <a name="set-up-direct-integration-of-italian-fatturapa-with-sdi"></a>设置意大利 FatturaPA 与 SDI 的直接集成

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> 适用于意大利的电子开票当前可能不支持 Microsoft Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 中可用于电子发票的所有功能。

本文提供的信息将帮助您开始使用 Finance 和 Supply Chain Management 中适用于意大利的电子开票功能。 指导您完成 Regulatory Configuration Services (RCS) 中与国家/地区相关的配置步骤。 这些步骤补充了[开始使用电子开票](e-invoicing-get-started.md)中描述的步骤。

## <a name="prerequisites"></a>先决条件

在完成本文中的步骤之前，必须满足以下先决条件：

- 完成[开始使用电子开票](e-invoicing-get-started.md)中的步骤。
- 将 **意大利 FatturaPA (IT)** 电子开票功能从全局存储库导入到 RCS 中。 有关详细信息，请参阅之前提及的“开始使用电子开票”一文的[从 Microsoft 配置提供者导入电子开票功能](e-invoicing-get-started.md#import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider)一节。
- 将所需证书中的链接添加到服务环境中。 必需的证书包括数字签名证书、证书主管机构 (CA) 证书和客户端证书。 有关详细信息，请参阅“开始使用电子开票服务管理”一文的[创建数字证书机密](e-invoicing-get-started-service-administration.md#create-a-digital-certificate-secret)一节。

## <a name="country-specific-configuration-for-the-italian-fatturapa-it-electronic-invoicing-feature"></a>意大利 FatturaPA (IT) 电子开票功能的国家/地区特定配置

在将应用程序设置部署到连接的 Finance 或 Supply Chain Management 应用之前，请完成以下步骤。

此部分补充“开始使用电子开票”一文中的[应用程序设置的国家/地区特定配置](e-invoicing-get-started.md#country-specific-configuration-of-application-setup)一节。

### <a name="create-a-new-feature"></a>创建新功能

1. 登录 RCS。
2. 在 **电子报告** 工作区内的 **配置提供程序** 部分中，将贵公司的配置提供程序标记为有效。
3. 在 **全球化功能** 工作区的 **功能** 部分中，选择 **电子开票** 磁贴。
4. 在 **电子开票功能** 页面上，选择 **添加** \> **基于现有功能**。
5. 在 **Microsoft 配置提供程序** 下，选择 **意大利 FatturaPA (IT)** 作为基本功能，输入名称，然后选择 **创建功能**。

### <a name="set-up-application-specific-parameters"></a>设置特定于应用程序的参数

1. 在 **电子开票功能** 页面上，选择要编辑的功能。
2. 在 **版本** 选项卡上，验证是否已选择 **草稿** 版本。
3. 在 **配置** 选项卡上，选择配置，然后选择 **应用程序特定参数**。
4. 在 **查找** 部分中，请确保选择了 **Natura 冲销费用子类别的列表** 查找。
5. 在 **条件** 部分，选择 **添加**。
6. 为系统中定义的每个子类别添加特定条件，然后保存更改。

    > [!NOTE]
    > 在 **名称** 列中，您可以选择 **\*空白\*** 或 **\*非空白\*** 占位符值，而不是特定值。

### <a name="configure-a-processing-pipeline-for-export"></a>配置导出的处理管道

1. 在 **电子开票功能** 页面上，选择要编辑的功能。
2. 在 **设置** 选项卡上，选择 **销售发票**，然后选择 **编辑**。
3. 在 **处理管道** 部分中，执行操作并设置所有必填字段：

    - 对于 **对文档签名** 操作，请在 **证书名称** 字段中指定数字签名证书。
    - 对于 **提交** 操作，请设置 **URL 地址** 和 **证书** 字段。 **证书** 字段的值是证书链，其中第一个是根 CA 证书 (caentrate.cer)，第二个为客户端证书。

4. 在 **适用性规则** 部分中，请浏览这些子句，然后查看或设置必填字段：
    - 查看 **LegalEntityID** 子句并使用法人提供的正确值进行更新。

5. 选择 **验证** 以确保已设置所有必填字段。
6. 保存更改并关闭页面。
7. 在 **设置** 选项卡上，选择 **项目发票**，然后选择 **编辑**。
8. 对项目发票重复步骤 3 到 6。

### <a name="configure-the-processing-pipeline-for-import"></a>配置导入的处理管道

1. 在 **电子开票功能** 页面上，选择要编辑的功能。
2. 在 **设置** 选项卡上，选择 **导入发票**，然后选择 **编辑**。
3. 在 **参数** 选项卡上的 **数据渠道** 部分内的 **数据渠道** 字段中，输入字符串值。
4. 在 **适用性规则** 选项卡上，设置此设置的字段。 通过将上一步中为 **数据渠道** 字段设置的值传递到 **值** 字段，您可以使用默认的 **渠道** 子句。

    ![设置适用性规则。](media/e-invoicing-ita-fatturapa-get-started-apprules-setup.png)

5. 选择 **验证** 以确保已设置所有必填字段。

### <a name="deploy-the-feature"></a>部署此功能

1. 对服务环境完成、发布和部署功能。 有关详细信息，请参阅“开始使用电子开票”一文的[将电子开票功能部署到服务环境](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment)一节。
2. 将该功能部署到连接的应用程序。 有关详细信息，请参阅“开始使用电子开票”一文的[将电子开票功能部署到连接的应用程序](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-connected-application)一节。

### <a name="set-up-finance"></a>设置 Finance

1. 登录您的 Finance 环境。
2. 在 **电子报告** 工作区的 **配置提供程序** 部分，选择 **Microsoft** 磁贴。
3. 选择 **存储库** \> **全局** \> **打开**。
4. 选择并导入 **客户发票上下文模型** 和 **供应商发票导入 (IT)** 配置。
5. 转到 **组织管理** \> **设置** \> **电子单据参数**。
6. 在 **功能** 选项卡上，查找并选择 **意大利电子发票** 功能，然后选择 **启用** 复选框。
7. 在 **电子单据** 选项卡上，请确保根据 [配置应用程序设置](e-invoicing-get-started.md#configure-the-application-setup)中的信息设置 **客户发票日记帐** 和 **项目发票** 字段。

### <a name="set-up-vendor-invoice-import"></a>设置供应商发票导入 

1. 在 Finance 中，在 **电子报告** 工作区内的 **配置提供程序** 部分中，将贵公司的配置提供程序标记为有效。
2. 选择 **申报配置**。
3. 选择 **客户发票上下文模型** 然后选择 **创建配置**。
4. 选择 **从名称派生：客户发票上下文模型，Microsoft** 以创建派生配置。
5. 在 **草稿** 版本中，选择 **设计器**。
6. 在 **数据模型** 树中，选择 **映射模型到数据源**。
7. 在 **定义** 树中，选择 **DataChannel**，然后选择 **设计器**。
8. 在 **数据源** 树中，展开 **\$上下文\_渠道** 容器。
9. 在 **值** 字段中，选择 **编辑**。 
10. 输入数据渠道的名称。 名称应最多包含 10 个字符。 它应与 RCS 中电子开单功能的数据渠道的 **数据渠道** 参数的值匹配。
11. 保存您的更改，然后转到 **报告配置** \> **完成配置版本**。
12. 在 **外部渠道** 选项卡上的 **渠道** 部分中，选择 **添加**。
13. 在 **渠道** 字段中，输入 **\$上下文渠道** 值。
14. 在 **说明** 和 **公司** 字段中输入值。
15. 在 **单据上下文** 字段中，选择从 **客户发票上下文模型** 派生的新配置。 映射描述应该为 **数据渠道上下文**。
16. 在 **导入来源** 选项卡上，选择 **添加**，然后设置以下值：

    - **名称：** OutputFile
    - **数据实体名称：** 供应商发票标题（**数据实体：** VendorInvoiceHeaderEntity）
    - **模型映射：** 供应商发票导入 (IT)

> [!NOTE]
> 如果您有从其他源导入供应商发票，则可以创建多个外部渠道和多个具有不同 **\$上下文渠道** 值的派生配置。 例如，您可能需要导入不同法人的供应商发票。

## <a name="proxy-server-setup"></a>代理服务器设置

本节提供的信息将帮助您设置和配置代理服务，以便在 Exchange 系统 (SDI) 和电子开票服务之间进行通信。

### <a name="create-an-app-registration"></a>创建应用注册

1. 使用以下 Windows PowerShell 脚本创建服务对服务 (S2S) 身份验证的自签名证书。

    ```powershell
    $certOutputLocation = "C:\certs\proxytest"
    $certName = "sdiProxyClientS2SCert"
    $certPassword = "123"

    $certCerFile = Join-Path $certOutputLocation "$certName.cer"
    $certPfxFile = Join-Path $certOutputLocation "$certName.pfx"

    $securePassword = ConvertTo-SecureString $certPassword -AsPlainText -Force

    $cert = New-SelfSignedCertificate -KeyLength 2048 -KeyExportPolicy Exportable -FriendlyName "CN=$certName" -CertStoreLocation Cert:\CurrentUser\My -Subject $certName -Provider "Microsoft Enhanced RSA and AES Cryptographic Provider"

    Export-Certificate -Cert $cert -FilePath $certCerFile -type CERT | Out-Null
    Export-PfxCertificate -Cert $cert -FilePath $certPfxFile -Password $securePassword | Out-Null
    ```

2. 将 .pfx 证书文件保存到密钥保管库中，然后删除本地副本。
3. 以管理员身份登录 [Azure 门户](https://portal.azure.com)。
4. 为 SDI 代理服务创建应用注册。

    1. 转到 **应用注册**，创建注册，然后为其设置以下值：

        - **名称：** SDI 代理客户端
        - **支持的帐户类型：** 仅此组织目录中的帐户（单个租户）

    2. 选择 **注册**，然后选择您刚刚创建的应用注册。
    3. 转到 **API 权限**，然后选择 **授权管理员同意**。
    4. 转到 **证书和密钥**，选择 **上传证书**，然后上传用于进行 S2S 身份验证的 .cer 证书文件。
    5. 转到 **企业应用程序**，然后选择您创建的应用。
    6. 保存应用程序的 **应用程序 ID**（客户端 ID）和 **对象 ID** 值。
    7. 发票服务团队必须授予应用对该服务的访问权限。 将以下参数的值发送到 <D365EInvoiceSupport@microsoft.com>：

        - AAD 租户 ID
        - LCS 环境 ID
        - 申请 ID
        - 对象 ID

5. 在 RCS 中，将应用添加到您的服务环境的应用程序列表中。

    1. 转到 **全球化功能** \> **环境** \> **电子开票** \> **服务环境**，然后选择您的环境。
    2. 在 **应用程序** 部分中，将行添加到网格，并输入应用的名称和对象 ID。

        ![将应用程序添加到服务环境。](media/e-invoicing-ita-fatturapa-get-started-add-app-to-env.png)

    3. 选择 **保存**，然后选择 **发布**。

### <a name="create-an-azure-virtual-machine"></a>创建 Azure 虚拟机

1. 在 [Azure 门户](https://portal.azure.com)中，转到 **虚拟机**，然后选择 **新建**。
2. 在 **基础** 选项卡上，选择您的订阅和资源组。 值应为您的密钥保管库和 Blob 存储所在的订阅和资源组。
3. 选择区域。 此值应为部署您的 Finance 环境的区域。
4. 添加管理员的用户名和密码，并将它们保存到密钥保管库。
5. 在 **选择入站端口** 字段中，选择 **HTTPS (443)** 和 **RPD (3389)**。

    > [!NOTE]
    > 我们建议您在系统投入生产时禁用 **RDP (3389)** 端口。 如果您必须连接到虚拟机 (VM) 以进行疑难解答，则可以重新启用它。

    ![在“基础”选项卡上设置字段以创建 Azure VM。](media/e-invoicing-ita-fatturapa-get-started-create-vm-1.png)

6. 在 **磁盘** 选项卡上 **高级** 快速选项卡上，选择 **使用托管磁盘** 复选框。 清除 **临时 OS 磁盘** 复选框。

    ![在“磁盘”选项卡上设置字段以创建 Azure VM。](media/e-invoicing-ita-fatturapa-get-started-create-vm-2.png)

7. 在 **网络** 选项卡上的 **公共 IP** 字段下，选择 **新建**。

    ![在“网络”选项卡上设置字段以创建 Azure VM。](media/e-invoicing-ita-fatturapa-get-started-create-vm-3.png)

8. 在 **创建公共 IP 地址** 对话框内的 **SKU** 字段组中，选择 **标准** 选项。 在 **分配** 字段组中，选择 **静态** 选项。

    ![创建公共 IP 地址。](media/e-invoicing-ita-fatturapa-get-started-create-vm-4.png)

9. 在 **管理** 选项卡上，清除 **自动关闭** 复选框以禁用自动关闭。
10. 将 **来宾 OS 更新** 字段设置为 **手动**，然后设置任何其他策略。
11. 查看并创建 VM。
12. 在新的 VM 中，转到 **标识** \> **系统分配**，并将 **状态** 选项设置为 **开**。
13. 授予 VM 对密钥保管库的访问权限。

    1. 在密钥保管库中，转到 **访问控制 (IAM)** \> **角色分配**。
    2. 选择 **添加角色分配**，然后设置以下字段：

        1. 在 **角色** 字段中，指定 **密钥保管库密钥用户**。
        2. 在 **将访问权限分配到** 字段中，指定 **虚拟机**。
        3. 在 **订阅** 字段中，指定您的订阅。
        4. 在 **选择** 字段中，指定您的 VM。

    3. 转到 **访问政策**。
    4. 选择 **添加访问策略**，然后设置以下字段：

        1. 在 **选择的主体** 字段中，选择您的 VM。
        2. 在 **证书** 部分，选择 **列出** 和 **获取** 权限。

14. 在 [Azure 门户](https://portal.azure.com)中，转到 **公共 IP 地址**，然后选择在 VM 中创建的 IP 地址。
15. 转到 **配置**，然后设置域名系统 (DNS) 名称。

### <a name="prepare-the-proxy-service-environment"></a>准备代理服务环境

在托管代理服务的计算机上执行以下步骤。

1. 使用远程桌面连接连接到 VM。
2. 打开本地计算机证书管理单元。 有关详细信息，请参阅[如何：使用 MMC 管理单元查看证书](/dotnet/framework/wcf/feature-details/how-to-view-certificates-with-the-mmc-snap-in)。
3. 将用于生产的 **caentrate.cer** 证书和用于测试的 **CAEntratetest.cer** 证书导入[受信任的根证书颁发机构商店](/dotnet/framework/wcf/feature-details/working-with-certificates#certificate-stores)。 （**CAEntratetest.cer** 是由主管机构提供的根 CA 证书。）
4. 在控制面板中，**打开或关闭 Windows 功能**，或针对服务器操作系统 (OS) 转到 **服务器管理器** \> **添加角色和功能**，并启用 Internet 信息服务 (IIS) 功能：

    - Web 管理工具
        - IIS 管理控制台
    - 世界范围 Web 服务
        - 应用程序开发功能
            - .NET Extensibility 4.7（或 4.8）
            - ASP
            - ASP.NET 4.7（或 4.8）
            - CGI
            - ISAPI 扩展
            - ISAPI 筛选器
        - 通用 HTTP 功能
            - 默认文档
            - 目录浏览
            - HTTP 错误
            - 静态内容
        - 运行状况和诊断
            - HTTP 日志记录
            - 跟踪
        - 性能功能
            - 静态内容压缩
        - 安全性
            - 请求筛选

    ![开启 IIS 功能。](media/e-invoicing-ita-fatturapa-get-started-turnon-features.png)

### <a name="set-up-the-sdi-proxy-service-in-iis"></a>在 IIS 中设置 SDI 代理服务

1. 在 Microsoft Dynamics Lifecycle Services (LCS) 中，转到共用资产库，选择 **数据包** 作为资产类型。
2. 查找 **电子开票服务 Sdi 代理**，并将其下载到 VM。
3. 配置此服务。

    1. 解压缩您下载的 **电子开票服务 Sdi 代理** 存档文件夹。
    2. 在 **src\\FattureService** 文件夹中，打开 **appsettings.json** 文件，并设置以下参数：

        - **KeyVaultUri** - 指定存储开票服务的客户端证书的密钥保管库的地址。
        - **TenantId** - 指定客户租户的全局唯一标识符 (GUID)。
        - **EnvironmentId** – 指定 LCS 环境的 ID。
        - **ClientId** - 指定客户租户中的中间服务应用注册的应用 ID。
        - **ClientCertificateName** - 指定密钥保管库中的 S2S 证书的名称。
        - **SecurityServiceClientOptions.Endpoint** - 指定安全服务的 URL。
        - **SecurityServiceClientOptions.Resource** - 指定获取令牌的范围。
        - **InvoicingServiceClientOptions.Endpoint** – 指定开票服务的终结点。 此值应与用于 RCS 和 Finance 的终结点相同。
        - **InvoicingServiceClientOptions.ServiceEnvironmentId** – 指定服务环境的名称。 此值应为您的 Finance 环境的名称。
        - **NotificationsFolder** - 指定文件夹以将传入的通知文件保存到其中。

    3. 在 **web.config** 文件中，查找以下行，并添加代理服务器证书的指纹。

        `<serviceCertificate findValue="[certificate thumbprint]" storeLocation="LocalMachine" storeName="My" x509FindType="FindByThumbprint">`

        > [!TIP]
        > 当系统进入生产状态时，您可以更改 web.config 文件中的某些值，以帮助减少收集的日志信息量，并帮助节省磁盘空间。 在 **\<system.diagnostics\>\<source\>** 节点中，将 **switchValue** 的值更改为 **严重，错误**。 有关详细信息，请参阅 [MS 服务跟踪查看器](/dotnet/framework/wcf/service-trace-viewer-tool-svctraceviewer-exe)。

4. 打开 IIS 管理器。 在左边的树中，保留在根节点中。 在右侧，选择 **服务器证书**。

    ![在 IIS 管理器中选择服务证书。](media/e-invoicing-ita-fatturapa-get-started-proxy-cert-1.png)

5. 打开菜单，然后选择 **导入**。
6. 在 **导入证书** 对话框内的 **证书文件 (.pfx)** 字段中，为代理服务器证书指定 .pfx 文件的路径。

    ![指定代理服务证书文件。](media/e-invoicing-ita-fatturapa-get-started-proxy-cert-2.png)

7. 选择并按住（或右键单击）**站点**，然后选择 **添加网站**。
8. 在 **添加网站** 对话框的 **站点名称** 字段中，输入站点的名称。
9. 在 **物理路径** 字段中，指向 **src\\FattureService** 文件夹。
10. 在 **绑定类型** 字段中，选择 **https**。
11. 在 **主机名** 字段中，指定主机名。
12. 将 **IP 地址** 和 **端口** 字段设置为默认值。
13. 确保已清除 **需要服务器名称指示** 复选框，因为 SDI 不支持该技术。
14. 在 **SSL 证书** 字段中，选择您导入的代理服务器证书。
15. 在 **应用程序池** 字段中，为站点指定一个池，并记录其名称（例如 **SdiAppPool**）。

    ![添加网站。](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-1.png)

16. 创建完网站后，请打开 **SSL 设置** 的菜单。

    ![打开 SSL 设置的菜单。](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-2.png)

17. 选中 **需要 SSL** 复选框，然后在 **客户端证书** 字段组中选择 **需要** 选项。

    ![配置 SSL 设置。](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-3.png)

18. 打开 **目录浏览**，然后选择 **启用**。
19. 在任何 Web 浏览器中，转到 **ServerDNS/TrasmissioneFatture.svc**。 必须显示有关该服务的标准页面。

    ![在浏览器中检查服务。](media/e-invoicing-ita-fatturapa-get-started-proxy-open-browser.png)

20. 创建以下文件夹以存储日志和文件：

    - **C:\\Logs\\** – 在此处存储日志文件。 通过 [MS 服务跟踪查看器](/dotnet/framework/wcf/service-trace-viewer-tool-svctraceviewer-exe)可以查看这些文件。
    - **C:\\Files\\** – 将所有响应文件存储在此处。

21. 在文件资源管理器中，授予 **网络服务** 和 **IIS AppPool\\SdiAppPool**（如果您使用的是默认池，则为 **IIS AppPool\\DefaultAppPool**）访问 **Logs** 和 **Files** 文件夹的权限。

    1. 选择并按住（或右键单击）其中一个文件夹，然后选择 **属性**。
    2. 在 **属性** 对话框内的 **安全** 选项卡上，选择 **编辑**。
    3. 如果未列出用户，则添加这些用户。
    4. 对其他文件夹重复步骤 1 到 3。

    ![向服务用户添加权限。](media/e-invoicing-ita-fatturapa-get-started-proxy-add-user.png)

## <a name="privacy-notice"></a>隐私声明 

启用 **意大利电子发票** 功能可能需要发送有限的数据。 此数据包括组织的税务登记 ID。 管理员可以启用和禁用意大利电子发票功能。 若要禁用此功能，请执行以下步骤。

1. 转到 **组织管理** \> **设置** \> **电子单据参数**。
2. 在 **功能** 选项卡上，查找包含 **意大利电子发票** 功能的行，然后选择 **立即禁用**。

从这些外部系统导入到此 Dynamics 365 在线服务的数据受我们的[隐私声明](https://go.microsoft.com/fwlink/?LinkId=512132)的约束。 有关详细信息，请查阅国家/地区特定功能文档中的“隐私声明”部分。

## <a name="additional-resources"></a>其他资源

- [电子开票概览](e-invoicing-service-overview.md)
- [开始使用电子开票服务管理](e-invoicing-get-started-service-administration.md)
- [开始使用电子开票](e-invoicing-get-started.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
