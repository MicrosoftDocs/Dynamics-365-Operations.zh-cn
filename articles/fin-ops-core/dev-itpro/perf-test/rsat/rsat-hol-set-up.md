---
title: Regression Suite Automation Tool 设置和安装教程
description: 本主题是演示如何设置和安装 Regression Suite Automation Tool (RSAT) 的教程。
author: robinarh
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 21761, NotInToc
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2019-05-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 725bce4b3aa7feb61bd7d7ded1be07f803424e57
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745189"
---
# <a name="set-up-and-install-regression-suite-automation-tool-tutorial"></a>Regression Suite Automation Tool 设置和安装教程

本主题是帮助您设置和开始使用 RSAT 以及与使用 RSAT 有关的工具的教程。

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> 可使用 Internet 浏览器工具下载此页并以 PDF 格式保存。

## <a name="key-concepts"></a>重要概念

- 了解支持 Regression Suite Automation Tool (RSAT) 的各种应用程序所需的安装和先决条件设置。
- 了解如何使用任务录制器功能和 Microsoft Dynamics Lifecycle Services (LCS) 与 Microsoft Azure DevOps 创建、配置、运行、调查和报告测试用例。
- 让功能用户可以通过使用任务录制器录制业务任务，然后将任务录制转换为一套自动化测试，而不必编写源代码。

## <a name="before-you-begin"></a>开始之前

### <a name="prerequisites"></a>先决条件

- 此教程需要运行 Microsoft Dynamics 365 for Finance and Operations 版本 10.0（2019 年 4 月）或更高版本的环境。 也支持运行 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.3 平台更新 20 (PU20) 或更高版本的客户。
- 用户必须具有环境的管理员权限。
- 您必须有权访问客户租户 LCS 和 Azure DevOps（以前称为 Microsoft Visual Studio Team Services \[VSTS\]）。
- 要创建和管理测试套件的用户必须拥有 Azure DevOps 测试计划或测试管理许可证。 以下许可证也为您提供测试计划的访问权限：
    - Visual Studio Enterprise 许可证
    - Visual Studio Test Professional 许可证
    - MSDN 平台订户许可证
- RSAT 必须可以通过 Web 浏览器访问测试环境。
- 若要生成和编辑测试参数，必须安装 Microsoft Excel。

## <a name="configure-azure-devops"></a>配置 Azure DevOps

### <a name="user-eligibility"></a>用户资格

确保在 Azure DevOps 中创建用户，并且该用户具有可访问 Azure 测试计划的订阅级别。 仅当用户需要创建和管理测试用例，才需要 Azure DevOps 测试计划许可证号（即并非所有 RSAT 用户都需要此许可证）。 有关许可证要求的信息，请参阅[许可证要求](https://docs.microsoft.com/azure/devops/test/manual-test-permissions#license-requirements)。

### <a name="create-a-new-azure-devops-project"></a>创建新 Azure DevOps 项目

RSAT 对测试用例使用 Azure Devops，以及测试套件管理，报告和调查测试的运行结果。

> [!NOTE]
> 可使用现有 Azure DevOps 项目。 但是，如果已设置的现有 Azure DevOps 项目具有自定义模板，则将业务流程建模器 (BPM) 的测试用例同步到 Azure DevOps 时，会收到“VSTS 同步失败”错误（请参阅[测试从 BPM 到 Azure DevOps 的同步](#test-the-synchronization-from-bpm-to-azure-devops)部分）。 如果已经为该自定义模板实施了以下最佳实践，则可以将测试用例同步到 Azure DevOps。 （错误消息中列出了这些最佳实践。）

- 请勿删除任何工作项类型或现成字段。
- 请勿删除任何工作项类型状态。
- 请勿将任何必填字段添加到工作项类型。

![包含最佳实践列表的错误消息](./media/setup_rsa_tool_02.png)

否则，对于本教程，建议新建 Azure DevOps 项目。 有关详细信息，请参阅[使用自定义 Azure DevOps (VSTS) 流程模板同步到 BPM 时的问题](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/)。

1. 打开 Azure DevOps URL (`https://dev.azure.com/<Azure DevOps Name>`)。
2. 选择 Azure DevOps 页中右上角的 **创建项目**。

    ![“创建项目”按钮](./media/setup_rsa_tool_03.png)

3. 填写以下字段，然后选择 **创建**：

    - **项目名称**
    - **版本控制** – 选择 **Team Foundation 版本控制**。 请注意，不支持默认消息 **Git**。
    - **工作项流程**

    ![“新建项目”对话框](./media/setup_rsa_tool_04.png)

### <a name="create-a-personal-access-token"></a>创建个人访问令牌

本教程中，将使用 LCS 业务流程建模器 (BPM) 创建测试用例库，并将测试用例与 Azure DevOps 同步。 需要个人访问令牌才能将 BPM 与 Azure DevOps 同步。

1. 选择您的 Azure DevOps 项目的页面右上角中的配置文件图标，然后选择 **安全**。

    ![“安全”命令](./media/setup_rsa_tool_05.png)

2. 在左窗格中 **安全** 下，选择 **个人访问令牌**。 然后选择 **新建令牌**。

    ![“用户”设置中“个人访问令牌”选项卡上的“新建令牌”按钮](./media/setup_rsa_tool_06.png)

3. 填写以下字段，然后选择 **创建**：

    - **姓名**
    - **到期 (UTC)** – 选择 **自定义**，然后使用日期选取器选择上一个可用日期。
    - **范围** – 选择 **完全访问权限** 选项。

    ![“新建个人访问令牌”对话框](./media/setup_rsa_tool_07.png)

    > [!NOTE]
    > 记下创建的个人访问令牌。 后面设置 RSAT 配置时需要。

    ![个人访问令牌](./media/setup_rsa_tool_08.png)

## <a name="configure-the-lcs-project"></a>配置 LCS 项目

您的主测试库需要 Lifecycle Services (LCS) 项目。 LCS 业务流程建模器 (BPM) 用作您的测试用例的主库。 BPM 用于为 LCS 项目管理和分发测试库。 例如，构建测试库的 Microsoft 合作伙伴或独立软件供应商 (ISV) 将以 BPM 库的形式发布测试案例。 在 BPM 中，测试用例由业务流程组织。 BPM 不定义测试经过的执行顺序或频率。 这些详细信息在 Azure DevOps 中管理，如本主题后文所述。  

对于 LCS 项目，可使用现有客户实施或合作伙伴项目。

### <a name="update-the-lcs-language"></a>更新 LCS 语言

> [!NOTE]
> 要让用户界面 (UI) 正确显示业务流程，必须将 LCS 首选语言设置为 **语言(美国)**。

1. 转到 LCS 实施项目。
2. 选择页面右上角的 **设置** 按钮（齿轮符号），然后选择 **语言首选项**。

    ![更新语言首选项](./media/setup_rsa_tool_09.png)

3. 在 **首选语言** 字段中，选择 **英语 (美国)**，然后选择 **保存**。

    ![“用户设置”中的“语言首选项”选项卡](./media/setup_rsa_tool_10.png)

### <a name="configure-lcs-to-connect-to-the-azure-devops-project"></a>配置 LCS 以连接到 Azure DevOps 项目

如果前面新建了 Azure DevOps 项目，请配置 LCS 项目以连接到新建的这个项目。 否则，如果已将您的 LCS 项目连接到了 Azure DevOps 项目，则可继续到下一部分。

1. 转到 LCS 实施项目。
2. 选择 **菜单** 按钮，然后选择 **项目设置**。

    ![“项目设置”命令](./media/setup_rsa_tool_11.png)

3. 在左窗格中，选择 **Visual Studio Team Services**，然后选择 **设置 Visual Studio Team Services**。

    ![“项目设置”中的“Visual Studio Team Services”选项卡](./media/setup_rsa_tool_12.png)

4. 在 **Azure DevOps 站点 URL** 字段中，输入 Azure DevOps 站点的 URL。 在 **个人访问令牌** 字段中，输入之前创建的个人访问令牌。

    > [!NOTE]
    > 尽管 VSTS 现在称为 Azure DevOps，要将 LCS 连接到 Azure DevOps 项目，请使用原来的 URL。 例如，本教程中使用的 Azure DevOps URL 为 `https://dev.azure.com/D365FOFastTrack/`。 但是，下图中输入的是 `https://D365FOFastTrack.visualstudio.com/`。

    ![“设置 Visual Studio Team Services”中的步骤 1](./media/setup_rsa_tool_13.png)

5. 选择 **继续**。
6. 在 **Visual Studio Team Services 项目** 字段中，在所选站点上选择要与 LCS 项目链接的 VSTS 项目。 默认情况下，**流程模板** 字段设置为 **Agile**。 对于自定义模板，请参阅[新建 Azure DevOps 项目](#create-a-new-azure-devops-project)部分中的最佳实践指南。 然后选择 **继续**。

    ![“设置 Visual Studio Team Services”中的步骤 2](./media/setup_rsa_tool_14.png)

7. 检查设置，然后选择 **保存**。

    ![“设置 Visual Studio Team Services”中的步骤 3](./media/setup_rsa_tool_15.png)

8. 选择 **授权** 为 LCS 授予代表您访问所配置 Azure DevOps 站点的权限，以便开启与 VSTS 集成的功能。

    ![“授权”按钮](./media/setup_rsa_tool_16.png)

9. 将显示一个消息框，其中说明“您即将重定向到外部站点以授权 LCS 代表您连接到 Visual Studio Team Services。 是否要继续？” 选择 **是**。

    ![消息框](./media/setup_rsa_tool_17.png)

10. 选择 **接受**。

    ![授予访问权限](./media/setup_rsa_tool_18.png)

11. 如果已为您授予用户权限，则 UI 应该会让您回到 LCS 项目设置页。

    ![授权用户](./media/setup_rsa_tool_19.png)

### <a name="create-a-new-bpm-library"></a>创建新的 BPM 库

1. 转到 LCS 实施项目。
2. 选择 **菜单** 按钮，然后选择 **业务流程建模器**。

    ![“业务流程建模器”命令](./media/setup_rsa_tool_20.png)

3. 选择 **新建库**。

    ![“新建库”按钮](./media/setup_rsa_tool_21.png)

4. 在 **库名** 字段中，输入名称，然后选择 **创建**。 对于本教程，请将 BPM 库命名为 **RSAT**。

    ![“新建库”对话框](./media/setup_rsa_tool_22.png)

5. 打开新的 **RSAT** BPM 库。
6. 选择 **示例核心业务流程** 流程，然后选择右侧的 **编辑模式**。

    ![“编辑模式”按钮](./media/setup_rsa_tool_23.png)

7. 将 **名称** 字段和 **说明** 字段的值更改为 **创建产品**。 然后选择 **保存**。

    ![“名称”和“说明”字段](./media/setup_rsa_tool_24.png)

## <a name="environment"></a>环境

### <a name="version-requirement"></a>版本要求

需要运行版本 10 的测试或沙盒环境。 也支持运行版本 7.3 平台更新 20 或更高版本的客户。

> [!NOTE]
> RSAT 必须可以通过 Web 浏览器访问测试环境。

### <a name="user-criteria"></a>用户条件

用户必须具有此环境的管理员权限。

### <a name="set-up-help-settings-to-connect-with-lcs"></a>设置“帮助”设置以连接 LCS

需要执行此步骤才能与 LCS 连接，这样就可以通过客户端将任务录制保存到 LCS 中的相应 BPM 库。

1. 打开客户端。
2. 转到 **系统管理 \> 设置 \> 系统参数**。
3. 在 **帮助** 选项卡上的 **Lifecycle Services 帮助配置** 字段中，选择相关 LCS 项目（本教程中为 **RSAT**）。

    ![“帮助”选项卡上的“Lifecycle Services 帮助配置”字段](./media/setup_rsa_tool_25.png)

    将在相应 LCS 项目下填写 BPM 库。

4. 选择 **保存**。
5. 可能必须刷新浏览器才能查看更新后的帮助内容。

    ![有关刷新浏览器的通知](./media/setup_rsa_tool_26.png)

## <a name="task-recordings"></a>任务录制

> [!NOTE]
> 确保在主仪表板上启动您的所有任务录制。 让各录制简短，并注重一个业务任务，如创建销售订单。

### <a name="create-a-task-recording-and-save-it-to-the-bpm-library"></a>创建任务录制并保存到 BPM 库

创建一个相应任务录制，可将其附加到在新的 BPM 库中创建的简单业务流程。

1. 打开客户端。
2. 在主仪表板上，选择 **设置** 按钮（齿轮符号），然后选择 **任务录制器**。

    ![在“设置”菜单上选择“任务录制器”](./media/setup_rsa_tool_27.png)

3. 选择 **创建录制**。

    ![“创建录制”按钮](./media/setup_rsa_tool_28.png)

4. 填写 **记录名称** 和 **记录说明** 字段，然后选择 **开始**。

    ![“录制名称”和“录制说明”字段](./media/setup_rsa_tool_29.png)

5. 录制用于创建产品的步骤。 完成后，选择 **停止** 以停止录制。

    ![用于创建产品的步骤](./media/setup_rsa_tool_30.png)

6. 选择 **保存到 Lifecycle Services**。

    ![将任务录制保存到 Lifecycle Services](./media/setup_rsa_tool_31.png)

    将从 LCS 加载库信息。

    ![加载库信息](./media/setup_rsa_tool_32.png)

7. 选择要与任务录制关联的 BPM 库。 对于本教程，请选择之前创建的 **RSAT** BPM 库及其下的 **创建产品** 业务流程。 然后选择 **确定**。

    ![将任务录制与 BPM 库和业务流程关联](./media/setup_rsa_tool_33.png)

    将显示“保存到 Lifecycle Services 已成功”消息。

    ![有关成功保存到 LCS 的消息](./media/setup_rsa_tool_34.png)

8. 如果要在本地保存任务录制，然后通过 LCS 上载到 BPM，请执行以下步骤：

    1. 完成录制后，选择 **保存到此 PC**。

        ![保存到此 PC](./media/setup_rsa_tool_35.png)

    2. 在浏览器的通知栏中，选择 **保存** 或 **另存为**，将文件保存到您的本地计算机上。

        ![通知栏](./media/setup_rsa_tool_36.png)

    3. 转到 **RSAT** BPM 库，然后选择要针对其保存任务录制的业务流程。
    4. 在 **概述** 选项卡上，选择 **上载**。

        ![“上载”按钮](./media/setup_rsa_tool_37.png)

    5. 选择 **浏览**，然后选择之前保存的 .axtr 文件。 然后选择 **上载**。

        ![选择要上载的 .axtr 文件](./media/setup_rsa_tool_38.png)

### <a name="test-the-synchronization-from-bpm-to-azure-devops"></a>测试从 BPM 到 Azure DevOps 的同步

由于已向此业务流程附加了任务录制，所以必须验证是否可使用 LCS 中的 VSTS 同步功能将业务流程和关联的任务录制（分别）作为功能和测试用例同步到 Azure DevOps。

> [!NOTE]
> Azure DevOps 中创建的相应工作项类型取决于您在按照[新建 Azure DevOps 项目](#create-a-new-azure-devops-project)部分中的说明使用 Azure DevOps 配置 LCS 项目时选择的流程模板。

1. 转到 BPM 库，然后打开之前创建的 **RSAT** 库。
2. 选择省略号按钮 (**...**)，然后选择 **VSTS 同步**。

    ![省略号菜单中的“VSTS 同步”命令](./media/setup_rsa_tool_39.png)

    完成 VSTS 同步之后，左侧将显示 **要求** 选项卡，其中包含相应 Azure DevOps 工作项。

    > [!NOTE]
    > Azure DevOps 中创建的工作项采用 BPM 库名称充当标题前缀。

    ![“要求”选项卡](./media/setup_rsa_tool_40.png)

3. 刷新该页面。
4. 选择省略号按钮 (**...**)。将再显示一个选项，即 **同步测试用例**。 选择此选项。

    ![省略号菜单中的“同步测试用例”命令](./media/setup_rsa_tool_41.png)

    > [!NOTE]
    > 如果刷新页面之后 **同步测试用例** 选项不可用，请转到 BPM 的主页，然后为整个库本身选择 **同步测试用例**。 这样就可以有效地为整个库强制实施同步。
    >
    > ![为整个库选择同步测试用例](./media/setup_rsa_tool_42.png)

    完成同步测试用例后，将在 **要求** 选项卡上新建一个测试用例。

    ![“要求”选项卡上的“新建测试用例”](./media/setup_rsa_tool_43.png)

5. 转到 Azure DevOps 项目，然后选择 **面板 \> 工作项**。

    ![“面板”下的“工作项”命令](./media/setup_rsa_tool_44.png)

6. 验证是否存在通过 BPM 同步创建的工作项和测试用例。

    ![工作项和测试用例](./media/setup_rsa_tool_45.png)

## <a name="install-and-configure-rsat"></a>安装和配置 RSAT

可将 RSAT 安装到运行 Windows 10 并可通过 Web 浏览器（Internet Explorer 或 Google Chrome）连接到环境的任何计算机上。

> [!NOTE]
> 安装此工具的新版本之前，建议卸载上一个版本。

### <a name="install-an-authentication-certificate"></a>安装身份验证证书

若要启用身份验证，必须生成证书并安装到运行 RSAT 的同一台计算机上。

#### <a name="generate-a-certificate"></a>生成证书

1. 若要生成证书文件，请以管理员身份打开一个 Microsoft Windows PowerShell 窗口，然后运行以下命令。

    ```powershell
    $certificate = New-SelfSignedCertificate -dnsname 127.0.0.1 -CertStoreLocation cert:\LocalMachine\My -FriendlyName "D365 Automated testing certificate" -Provider "Microsoft Strong Cryptographic Provider"
    ```

2. 通过在 **运行** 对话框中输入 **certlm.msc** 打开证书管理器，然后在 **个人 \> 证书** 下确认创建的 **D365 Automated 测试证书** 证书。

    > [!NOTE]
    > 务必输入 **certlm.msc**，不要输入 **certmgr.msc**，因为证书存储在本地计算机上。

    ![“D365 Automated 测试证书”证书](./media/setup_rsa_tool_46.png)

3. 右键单击证书，然后选择 **复制**。
4. 转到 **可信根证书主管机构 \> 证书**。

    ![“可信根证书主管机构”文件夹下的“证书”文件夹](./media/setup_rsa_tool_47.png)

5. 在 **操作** 菜单上，选择 **粘贴** 将证书复制到 **可信根证书主管机构** 位置。

    ![“操作”菜单上的“粘贴”命令](./media/setup_rsa_tool_48.png)

6. 若要获取所安装证书的指纹，但是不包含空间或特殊字符，请以管理员身份打开一个 Windows PowerShell 窗口，然后运行以下命令。

    ```powershell
    cd Cert:\LocalMachine\My

    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

    > [!NOTE]
    > 保存指纹，因为后面更新应用程序对象服务器 (AOS) 的 .wif 文件和设置 RSAT 配置时需要指纹。

#### <a name="configure-the-aos-computer-to-trust-the-connection"></a>将 AOS 计算机配置为信任连接

> [!NOTE]
> 如果环境是二级以上环境，则必须在 wif.config 文件中为环境的 **所有** AOS 计算机更新证书指纹。

1. 建立与 AOS 计算机之间的远程桌面协议 (RDP) 连接。 LCS 中的环境详细信息页中提供登录详细信息。
2. 打开 Microsoft Internet 信息服务 (IIS)，然后在站点列表中找到 **AOSService**。

    ![站点列表中的 AOSService](./media/setup_rsa_tool_49.png)

3. 右键单击 **浏览** 以打开 **\<Drive\>: \\AosService\\WebRoot** 文件夹。 找到 **wif.config** 文件。

    ![WebRoot 文件夹中的 Wif.config 文件](./media/setup_rsa_tool_50.png)

4. 通过添加证书的新主管机构条目和主管机构名称，更新 **wif.config** 文件，如以下示例中所示。

    ```Xml
    <issuerNameRegistry type="Microsoft.Dynamics.AX.Security.SharedUtility.AxIssuerNameRegistry,Microsoft.Dynamics.AX.Security.SharedUtility">
        <authority name="CN=127.0.0.1">
            <keys>
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
            </keys>
            <validIssuers>
                <add name="CN=127.0.0.1" />
            </validIssuers>
        </authority>
    ```

    > [!NOTE]
    > 如果多个用户在使用同一个应用程序，则每个用户必须生成单独的指纹，并且必须将这些指纹全部添加到 **\<keys\>** 部分中。

5. 如果有多台 AOS 计算机，请对其他每台计算机重复执行步骤 3 到 4。

    > [!NOTE]
    > 与原来的二级环境不同，将为新的二级环境部署两个 AOS 实例。

6. 在所有 AOS 计算机上运行 **iisreset**。

    > [!NOTE]
    > 如果没有在一级计算机上运行 **iisreset** 的管理员权限，请在 LCS 中的“环境详细信息”页上，选择“维护 > 重新启动服务”。

#### <a name="tier-2-environment"></a>二级以上环境

如果使用二级以上（标准接受度测试沙盒或更高）的环境，请在安装 RSAT 的计算机上验证或设置以下注册表设置。 需要执行此步骤，是因为可以帮助您避免身份验证或 RSAT 连接错误。

```PowerShell
if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319))
{
    Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false
}
```

### <a name="install-rsat"></a>安装 RSAT

1. 转到 <https://www.microsoft.com/download/details.aspx?id=57357>，然后选择 **下载**。
2. 选择所有文件，然后选择 **下一步**。

    ![选择所有文件](./media/setup_rsa_tool_51.png)

3. 双击 .msi 包运行安装程序。 然后，在安装完成时，选择 **完成**。

    ![RSAT 安装程序文件](./media/setup_rsa_tool_52.png)

### <a name="install-selenium-and-browser-drivers"></a>安装 Selenium 和浏览器驱动程序

在 RSAT 的早期版本中，必须安装 Selenium 和浏览器驱动程序。 因为这些驱动程序会自动安装，所以再也不必安装。

1. 首次打开 RSAT 时，将提示自动下载并安装 Selenium。 有关详细信息，请参阅[配置 RSAT](#configure-rsat) 部分。
2. 将提示您自动下载并安装与 RSAT 配置中所选默认浏览器对应的浏览器驱动程序，之后才能运行测试用例。 有关详细信息，请参阅[加载和运行测试用例](#load-and-run-test-cases)部分。

## <a name="get-started-with-rsat"></a>开始使用 RSAT

### <a name="create-a-test-plan-and-test-suites"></a>创建测试计划和测试套件

1. 转到 Azure DevOps 项目，然后选择 **测试计划**。

    ![“测试计划”命令](./media/setup_rsa_tool_53.png)

2. 选择 **新建测试计划**。

    ![“新建测试计划”按钮](./media/setup_rsa_tool_54.png)

3. 填写 **名称** 字段，然后选择 **创建**。 对于本教程，将测试计划命名为 **RSAT 测试计划**。

    ![“新建测试计划”对话框](./media/setup_rsa_tool_55.png)

4. 选择加号 (**+**)，然后选择 **静态套件** 在新测试计划下创建一个静态套件。 将这个新的测试套件命名为 **T01 – 制造到库存**。

    > [!NOTE]
    > 如果希望将新测试用例从 BPM 自动提取到 RSAT 测试套件中，也可以创建基于查询的套件。

    ![创建静态套件](./media/setup_rsa_tool_56.png)

### <a name="attach-test-cases-to-test-suites"></a>将测试用例附加到测试套件

1. 选择右侧的 **添加现有** 将现有测试用例添加到测试套件。

    ![“添加现有”按钮](./media/setup_rsa_tool_57.png)

2. 在 **将测试用例添加到套件** 页上，选择 **运行查询**，然后选择要添加到测试套件的测试用例。 对于本教程，请选择 **创建新产品** 测试用例。 然后选择页面右下角的 **添加测试用例**（下图中未显示此按钮）。

    ![“运行查询”按钮](./media/setup_rsa_tool_58.png)

    将把测试用例添加到 **T01 - 制造到库存** 测试套件。

    ![测试案例已添加到测试套件](./media/setup_rsa_tool_59.png)

### <a name="configure-rsat"></a>配置 RSAT

1. 打开 RSAT。

    ![“RSAT”图标](./media/setup_rsa_tool_60.png)

2. 将收到警告消息，说明“Regression Suite Automation Tool 需要 Selenium。是否要立即自动下载并安装？”。 选择 **是**。

    ![Regression Suite Automation Tool 需要 Selenium 的警告消息](./media/setup_rsa_tool_61.png)

3. 选择右上角的 **设置** 按钮（齿轮符号），然后填写显示的对话框中的以下字段：

    - **Azure DevOps Url** – 输入您的 Azure DevOps 项目的 URL，如 `https://yourAzureDevOpsUrlHere.visualStudio.com`。
    - **访问令牌** – 输入用于将工具连接到 Azure DevOps 的访问令牌。 使用本教程前面创建的个人访问令牌。 有关详细信息，请参阅[使用个人访问令牌对访问进行身份验证](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate)。
    - **项目名称** – 选择您的 Azure DevOps 项目的名称。
    - **测试计划** – 选择其中包含您的测试用例的 Azure DevOps 测试计划。 有关详细信息，请参阅[创建测试计划和测试套件](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan)。 选择测试计划之后，选择 **测试连接** 以测试您与 Azure DevOps 之间的连接。
    - **主机名** – 输入测试环境的主机名，如 **\<myaos\>.cloudax.dynamics.com**。 请勿在其中包含 **https://** 或 **http://** 前缀。
    - **SOAP 主机名** – 输入测试环境的 SOAP 主机名。 SOAP 主机名通常与主机名相同，但带有 **soap** 后缀。 下面是示例：**\<myaos\>soap.cloudax.dynamics.com**。 请勿在其中包含 **https://** 或 **http://** 前缀。

        > [!NOTE]
        > 若要查找主机名和 SOAP 主机名，请打开 IIS 管理器，右键单击 **站点 \> AOSService**，然后选择 **编辑绑定**。 **主机名** 列中的值提供主机名和 SOAP 主机名（在 URL 中，SOAP 主机名带有后缀 **soap**）。

        ![“主机名”列中的主机名和 SOAP 主机名](./media/setup_rsa_tool_63.png)

    - **管理员用户名** – 输入测试环境中的管理员用户的电子邮件地址。
    - **指纹** – 按照本教程前面的说明输入身份验证证书的指纹。
    - **工作目录** – 指定用于存储测试自动化文件（如 Excel 测试数据文件）的文件夹位置。 例如，输入或选择 **C:\\Temp\\RegressionTool**。

        > [!NOTE]
        > 如果文件夹名称中有空格，则执行将失败，因为找不到该文件夹。 这是已知问题，应该会在该工具的最新版本中解决。

    - **默认浏览器** – 选择 **Internet Explorer** 或 **Google Chrome**。 确保已安装相应的浏览器驱动程序。
    - **测试运行超时** – 为测试运行指定超时时间段（以分钟为单位）。 超时时间段耗尽后，将关闭所有活动窗口，而暂挂的测试用例将失败。
    - **测试操作超时** – 此字段控制 Finance and Operation 环境服务器请求的超时时间段（以分钟为单位）。 默认值（2 分钟）通常应该就足够。 但是，对于较慢的环境，如果发生了与超时有关的错误，可能需要增加该值。
    - **公司名称** – 输入在创建 Excel 参数文件时要用作默认公司的公司名称。 以后可通过编辑 Excel 参数文件更改公司。

    ![“设置”对话框](./media/setup_rsa_tool_62.png)

4. 选择 **应用** 以应用和保存您的设置。

    若要将当前设置保存到计算机上的配置文件，请选择 **另存为**。 若要从计算机上的配置文件还原设置，请选择 **打开**。

5. 选择 **关闭** 关闭对话框。

### <a name="load-and-run-test-cases"></a>加载和运行测试用例

1. 选择 **加载** 从 Azure DevOps 项目加载 **RSAT 测试计划** 测试计划。

    ![“加载”按钮](./media/setup_rsa_tool_64.png)

2. 从测试套件选择 **创建新产品** 测试用例，然后选择 **新建 \> 生成测试执行和参数文件**。

    ![“新建”菜单上的“生成测试执行和参数文件”命令](./media/setup_rsa_tool_65.png)

    将在您在 RSAT 配置中指定的本地文件夹（如 **C:\\Temp\\RegressionTool**）内创建 Excel 参数文件。

    ![已创建 Excel 参数文件](./media/setup_rsa_tool_66.png)

3. 如果要保存参数文件，请选择 **上载**。 将把选择的所有测试用例的测试自动化文件上载到 Azure DevOps 供将来使用。 （这些文件包括 Excel 测试参数文件。）

    这样就可以选择 **加载** 直接从 Azure DevOps 加载测试用例中的参数文件（和自动化文件）。 不必重新生成参数文件。 以后要保留参数文件中的修改，不希望覆盖时，此方法会变得非常重要。

4. 若要验证是否已将自动化文件和参数文件保存到了 Azure DevOps，请转到 Azure DevOps 项目，选择 **面板 \> 工作项**，然后选择 **创建新产品** 测试用例。 在 **附件** 选项卡上，应该可以看到四个文件：

    - **.cs** – C\# 自动化文件
    - **.dll** – 已编译为程序集的自动化文件
    - **.xlsx** – Excel 参数文件
    - **.xml** – 录制文件

    ![“附件”选项卡上的文件](./media/setup_rsa_tool_67.png)

5. 选择要运行的测试用例，然后选择 **运行**。

    > [!NOTE]
    > 如果浏览器使用的是 Internet Explorer，请在运行测试用例之前，确保 **Windows 显示设置 \> 比例和布局** 中的桌面分辨率设置为 **100%**。 如果无法在虚拟机 (VM) 中更改此设置，请在用于访问该 VM 的客户端（笔记本电脑）上更改。 然后，VM 显示设置将继承这些分辨率设置。

    ![桌面分辨率设置为 100%](./media/setup_rsa_tool_68.png)

6. 如果系统中未安装浏览器驱动程序，将收到警告消息，说明“此操作需要 \<browser name\> 驱动程序。 是否要立即自动下载并安装？“ 选择 **是**。

    ![Internet Explorer 的警告消息](./media/setup_rsa_tool_69.png)

    ![Chrome 的警告消息](./media/setup_rsa_tool_70.png)

    > [!NOTE]
    > 如果使用 Chrome 充当浏览器和接收说明因为 Chrome 版本不正确而未创建会话的错误消息，从 <http://chromedriver.chromium.org/downloads> 将最新 Chrome 驱动程序下载到 **C:\\Program Files (x86)\\Regression Suite Automation Tool\\Common\\External\\Selenium** 文件夹。

    ![Chrome 的错误消息](./media/setup_rsa_tool_71.png)

    将运行测试用例，并更新 **结果** 字段。

    ![更新的结果字段](./media/setup_rsa_tool_72.png)

    如果已按照本教程的内容进行了操作，则 **创建新产品** 测试用例将失败，因为用于创建产品的任务录制将产品名另存为了硬编码的值。 如果重新运行同一个测试用例，则应该会收到错误消息，因为已存在该产品。

    ![“结果”字段已设置为“失败”](./media/setup_rsa_tool_72.png)

### <a name="view-the-test-results"></a>查看测试结果

1. 双击失败的测试用例。

    您将收到错误消息。

    ![错误消息](./media/setup_rsa_tool_73.png)

2. 选择 **详细信息** 以查看完整的错误消息。

    ![完整的错误消息](./media/setup_rsa_tool_74.png)

3. 若要在 Azure DevOps 中查看错误消息的详细版本，请选择 **在 Azure DevOps 中打开**。 在 Azure DevOps 中，可查看测试用例的状态和详细错误消息。

    ![Azure DevOps 中的详细错误消息](./media/setup_rsa_tool_75.png)

4. 若要直接在 Azure DevOps 项目中查看测试结果，请转到 **测试计划 \> 测试计划 \> 运行**。 双击要查看其更多详细信息的测试运行。

    ![Azure DevOps 中的测试运行列表](./media/setup_rsa_tool_76.png)

5. **运行摘要** 选项卡指示测试用例失败，但是不提供实际的错误消息。 若要查看详细错误消息，请选择 **测试结果** 选项卡。

    ![“运行摘要”选项卡](./media/setup_rsa_tool_77.png)

    **测试结果** 选项卡提供测试用例信息，以及结果和错误消息。

    ![“测试结果”选项卡](./media/setup_rsa_tool_78.png)

6. 双击相关记录以查看详细错误消息。

    ![详细错误消息](./media/setup_rsa_tool_79.png)

    > [!NOTE]
    > 本地的 **C:\\Users\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt** 中也有所有错误消息。

7. 也可以通过选择 **导出** 导出测试计划级结果。

    ![导出测试计划](./media/setup_rsa_tool_80.png)

### <a name="modify-the-excel-parameter-file"></a>修改 Excel 参数文件

1. 打开 RSAT。
2. 选择测试用例，然后选择 **编辑** 打开 Excel 参数文件。

    请注意，**EcoResProductCreate** 表中的 **产品编号** 字段为硬编码。 必须先将此字段更新为新的产品编号，才能再次运行测试用例。

3. 若要为每次运行生成唯一的产品编号，同时不必每次都重新打开 Excel 参数文件并手动更新产品编号，请使用以下 Excel 公式。

    ```vba
    ="RSAT_"&TEXT(NOW(),"yyymmddhhmm")
    ```

    > [!NOTE]
    > 除了 **常规** 选项卡，测试用例访问的每个窗体页在 Excel 参数文件中都有一个数据选项卡。

    ![“产品编号”字段](./media/setup_rsa_tool_81.png)

4. 选择 **保存**，然后关闭 Excel 工作簿。
5. 选择 **上载** 将 Excel 参数文件保存到 Azure DevOps。

    ![上载成功消息](./media/setup_rsa_tool_82.png)

    > [!NOTE]
    > 若要在特定用户上下文中运行测试用例，请在 Excel 参数文件 **常规** 选项卡上的 **测试用户** 字段中输入用户的电子邮件 ID。 在最新 RSAT 版本中，已更新了 Excel 参数文件中的字段布局，但是概念不变。
    >
    > ![“测试用户”字段](./media/setup_rsa_tool_83.png)

### <a name="validate-the-results"></a>验证结果

- 选择 **运行** 以重新运行测试用例，并且验证测试用例是否已通过。 可按照[查看测试结果](#view-the-test-results)部分中的说明查看测试结果。

    ![“结果”字段已设置为“通过”](./media/setup_rsa_tool_84.png)

### <a name="chaining-of-test-cases"></a>链接测试用例

RSAT 的一项关键功能是链接测试用例（即一个测试将值传递给其他测试这项功能）。 将根据在 Azure DevOps 测试计划中为测试用例定义的顺序运行测试用例。 （也可以在测试工具本身中更新此顺序。）因此，如果要将变量从一个测试用例传递到另一个，则测试顺序务必正确。

此部分中，将在第一个测试用例中创建已保存变量，创建第二个测试用例，然后将已保存变量从第一个测试用例传递到第二个测试用例。 然后将在 RSAT 中把测试用例作为链式测试用例运行。

#### <a name="modify-an-existing-task-recording-to-create-a-saved-variable"></a>修改现有任务录制以创建已保存变量

1. 打开客户端。
2. 选择 **设置** 按钮（齿轮符号），然后选择 **任务录制器**。
3. 选择 **编辑录制**。

    ![“编辑录制”按钮](./media/setup_rsa_tool_85.png)

4. 选择 **从 Lifecycle Services 打开**。

    ![“从 Lifecycle Services 打开”按钮](./media/setup_rsa_tool_86.png)

5. 选择 **选择 Lifecycle Services 库**。

    ![“选择 Lifecycle Services 库”按钮](./media/setup_rsa_tool_87.png)

    将从 LCS 加载 BPM 库。

    ![加载 BPM 库](./media/setup_rsa_tool_88.png)

6. 从 LCS 加载 BPM 库之后，选择任务录制关联的 **RSAT** BPM 库和 **创建新产品** 业务流程。 然后选择 **确定**。

    ![选择 BPM 库和业务流程](./media/setup_rsa_tool_89.png)

7. 将在 **录制名称** 字段中输入相应任务录制的名称。 选择 **开始**。

    ![“录制名称”字段中的任务录制名称](./media/setup_rsa_tool_90.png)

8. 转到 **产品信息管理 \> 产品**，然后选择 **新建** 打开在其中录制了原始任务录制（即 **创建产品**）的页面。
9. 选择 **插入步骤**。

    > [!NOTE]
    > 将在窗格中选择的步骤 **后面** 插入新步骤。

    ![“插入步骤”按钮](./media/setup_rsa_tool_91.png)

10. 右键单击 **产品编号** 字段，然后选择 **任务录制器 \> 复制**。

    ![“复制”命令](./media/setup_rsa_tool_92.png)

11. 将在窗格中添加一个新步骤。 记下 **产品编号** 字段中的值，因为后面需要。

    ![添加了新步骤](./media/setup_rsa_tool_93.png)

12. 选择 **完成编辑**。
13. 选择 **保存到 Lifecycle Services**，然后将新任务录制与原始任务录制关联的相同 BPM 库和业务流程关联。 有关详细信息，请参阅[创建任务录制并保存到 BPM 库](#create-a-task-recording-and-save-it-to-the-bpm-library)部分。
14. 转到 BPM 库，然后选择 **同步测试用例** 以按照[测试从 BPM 到 Azure DevOps 的同步](#test-the-synchronization-from-bpm-to-azure-devops)部分中的说明在 Azure DevOps 中覆盖附加到测试用例的任务录制。
15. 打开 RSAT，然后选择 **加载** 以重新加载测试套件中的所有测试用例。 必须按照 [加载和运行测试用例](#load-and-run-test-cases)部分中的说明为相应测试用例重新生成自动化文件和参数文件，方法是选择测试用例，然后选择 **新建 \> 生成测试执行和参数文件**。

    > [!NOTE]
    > 如果 Excel 参数文件未关闭，重新生成将失败。 因此，生成新的 Excel 参数文件之前，确保关闭测试用例的 Excel 参数文件。

16. 选择 **编辑** 打开新的 Excel 参数文件。 将在行 9 中看到新的 **已保存变量** 条目。 此变量（即 **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}**）将保存到任务录制的 XML 文件，并且可以在后续测试中使用。

    ![“已保存变量”条目](./media/setup_rsa_tool_94.png)

#### <a name="create-a-new-test-case"></a>创建新的测试用例

1. 转到 **RSAT** BPM 库。
2. 选择 **示例支持业务流程** 流程，然后选择右侧的 **编辑模式**。
3. 将 **名称** 字段和 **说明** 字段的值更改为 **发布产品**。 然后选择 **保存**。

    ![“名称”和“说明”已更改为“发布产品”](./media/setup_rsa_tool_95.png)

#### <a name="create-a-new-task-recording-that-has-a-validate-function"></a>创建具有验证功能的新任务录制

- 创建任务录制以将之前创建的产品发布给 USRT 法人。 有关详细信息，请参阅[创建任务录制并保存到 BPM 库](#create-a-task-recording-and-save-it-to-the-bpm-library)部分。

    > [!NOTE]
    > 对于链式测试用例，我们始终建议您通过 *手动键入字段的值* 查找或筛选您需要的记录。 这样，此工具就可以确定后续测试用例中必须对其执行操作的记录。

    ![具有验证功能的新任务录制](./media/setup_rsa_tool_96.png)

    如上图所示，使用快速筛选器找到产品之后，选择 **发布产品** 之前，请验证 **产品编号** 字段的值以确保产品 ID 是之前创建的产品 ID。  若要验证该值，请右键单击 **产品编号** 字段，然后选择 **任务录制器 \> 验证 \> 当前值**。

    ![验证当前值](./media/setup_rsa_tool_97.png)

#### <a name="save-the-task-recording-to-bpm"></a>将任务录制保存到 BPM

1. 完成任务录制后，选择 **保存到 Lifecycle Services**。

    ![将完成的任务录制保存到 Lifecycle Services](./media/setup_rsa_tool_98.png)

2. 将从 LCS 加载库信息。

    ![从 LCS 加载库信息](./media/setup_rsa_tool_99.png)

3. 选择要与任务录制关联的 BPM 库。 对于本教程，请选择之前创建的 **RSAT** BPM 库及其下的 **发布产品** 业务流程。 然后选择 **确定**。

#### <a name="sync-bpm-to-azure-devops"></a>将 BPM 同步到 Azure DevOps

1. 转到 BPM 库，然后打开 **RSAT** 库。
2. 选择 **VSTS 同步**，然后选择 **同步测试用例**。 有关详细信息，请参阅[测试从 BPM 到 Azure DevOps 的同步](#test-the-synchronization-from-bpm-to-azure-devops)部分。

    同步完成后，Azure DevOps 中 **面板 \> 工作项** 内将显示 **发布产品** 业务流程的新工作项和相应测试用例。

#### <a name="add-the-new-test-case-to-the-existing-test-suite"></a>将新测试用例添加到现有测试套件

1. 转到 **测试计划 \> 测试计划**，然后选择 **RSAT 测试计划** 计划。
2. 选择 **添加现有**。
3. 在 **向套件添加测试用例** 页中，选择 **运行查询**。
4. 选择为 **发布产品** 创建的新测试用例，然后选择页面右下角的 **添加测试用例**（下图中未显示此按钮）。

    ![“向套件添加测试用例”页](./media/setup_rsa_tool_100.png)

    此测试套件现在有两个测试用例。

    ![测试套件中的两个测试用例](./media/setup_rsa_tool_101.png)

#### <a name="load-test-cases-into-rsat"></a>将测试用例加载到 RSAT 中

1. 打开 RSAT，然后选择 **加载**。
2. 将加载测试用例，而您会收到警告，说明“此操作将覆盖 Excel 测试数据文件，本地更改将丢失。 是否要继续?” 选择 **是** 以更新本地系统中的 Excel 参数文件，但是不更新上载到 Azure DevOps 的 Excel 参数文件。

    ![此操作将覆盖 Excel 测试数据文件](./media/setup_rsa_tool_102.png)

    将加载这两个测试用例，以及第一个测试用例的 Excel 参数文件。 因为在上一个运行中选择了 **上载**，所以将从 Azure DevOps 提取参数文件。

    ![已加载测试用例](./media/setup_rsa_tool_103.png)

3. 仅选择第二个测试用例，然后选择 **新建 \> 生成测试执行和参数文件**。

#### <a name="edit-the-excel-parameter-file"></a>编辑 Excel 参数文件

1. 仅选择第二个测试用例，然后选择 **编辑** 打开相应 Excel 参数文件。
2. 将已保存变量 **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}**（请参阅[修改现有任务录制以创建已保存变量](#modify-an-existing-task-recording-to-create-a-saved-variable)部分）从第一个测试用例复制到使用产品编号的所有字段中。 在此情况下，将把变量复制到 **EcoResProductListPage** 表的 **产品编号** 和 **验证产品编号** 字段中。

    ![“产品编号”和“验证产品编号”字段](./media/setup_rsa_tool_104.png)

    > [!NOTE]
    > 只有在同一个测试运行期间才能在测试之间传递变量。 变量的名称必须完全匹配。

3. 选择 **保存**，然后关闭 Excel 工作簿。
4. 选择 **上载** 保存对 Excel 参数文件执行的更改。

#### <a name="run-the-chained-test-cases"></a>运行链式测试用例

1. 同时选择这两个测试用例，然后选择 **运行**。
2. 验证这两个测试用例是否均已通过。

    ![两个测试用例的“结果”字段均设置为已通过](./media/setup_rsa_tool_105.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]