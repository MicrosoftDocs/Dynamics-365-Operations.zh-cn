---
title: 常规故障排除
description: 本主题提供 Finance and Operations 应用与 Dataverse 之间的双写入集成的常规故障排除信息。
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 779cc80d4cb510e79885919f1c705824ab6ad58b3e2fe1bab7bbec0511d08951
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736294"
---
# <a name="general-troubleshooting"></a>常规故障排除

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



本主题提供 Finance and Operations 应用与 Dataverse 之间的双写入集成的常规故障排除信息。

> [!IMPORTANT]
> 本主题解决的某些问题可能需要系统管理员角色或 Microsoft Azure Active Directory (Azure AD) 租户管理员凭据。 介绍每个问题的每一节说明了是否需要特定角色或凭据。

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a>当您尝试使用 Package Deployer 工具安装双写入包时，没有显示可用的解决方案

某些版本的 Package Deployer 工具与双写入解决方案包不兼容。 要成功安装包，请务必使用[版本 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) 或更高版本的 Package Deployer 工具。

安装 Package Deployer 工具后，请按照以下步骤安装解决方案包。

1. 从 Yammer.com 下载最新的解决方案包文件。 下载包 zip 文件后，右键单击它，然后选择 **属性**。 选择 **解锁** 复选框，然后选择 **应用**。 如果看不到 **解锁** 复选框，则说明 zip 文件已被解锁，您可以跳过此步骤。

    ![属性对话框。](media/unblock_option.png)

2. 提取包 zip 文件，然后将所有文件复制到 **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438** 文件夹中。

    ![Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438 文件夹的内容。](media/extract_package.png)

3. 将所有复制的文件粘贴到 Package Deployer 工具的 **工具** 文件夹中。 
4. 运行 **PackageDeployer.exe** 以选择 Dataverse 环境并安装解决方案。

    ![“工具”文件夹的内容。](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a>在 Dataverse 中启用和查看插件跟踪日志以查看错误详细信息

**打开跟踪日志和查看错误所需的角色：** 系统管理员

若要打开跟踪日志，请执行以下步骤。

1. 登录到 Customer Engagement 应用，打开 **设置** 页面，然后在 **系统** 下，选择 **管理**。
2. 在 **管理** 页面中，选择 **系统设置**。
3. 在 **自定义** 选项卡上，在 **插件和自定义工作流活动跟踪** 列中，选择 **所有** 启用插件跟踪日志。 如果只想在发生异常时记录跟踪日志，则可以改为选择 **异常**。


若要查看跟踪日志，请执行以下步骤。

1. 登录到 Customer Engagement 应用，打开 **设置** 页面，然后在 **自定义** 下，选择 **插件跟踪日志**。
2. 找到 **类型名称** 列设置为 **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin** 的跟踪日志。
3. 双击一个项目查看完整日志，然后在 **执行** 快速选项卡上，查看 **消息块** 文本。

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>启用调试模式来解决 Finance and Operations 应用中的实时同步问题

**查看错误所需的角色：** 系统管理员，源自 Dataverse 的双写入错误可能会出现在 Finance and Operations 应用中。 在某些情况下，错误消息的完整文本不可用，因为消息太长或包含个人身份信息 (PII)。 您可以按照以下步骤打开详细错误日志记录。

1. Finance and Operations 应用中的所有项目配置在 **DualWriteProjectConfiguration** 表中均具有 **IsDebugMode** 属性。 使用 Excel 加载项打开 **DualWriteProjectConfiguration** 表。

    > [!TIP]
    > 打开表的一种简单方法是在 Excel 加载项中打开 **设计** 模式，然后将 **DualWriteProjectConfigurationEntity** 添加到工作表。 有关详细信息，请参阅[在 Excel 中打开表数据并使用 Excel 加载项更新](../../office-integration/use-excel-add-in.md)。

2. 将项目的 **IsDebugMode** 属性设置为 **是**。
3. 运行产生错误的方案。
4. 详细日志在 DualWriteErrorLog 表中提供。 要在表浏览器中查找数据，请使用以下 URL（根据需要替换 **XXX**）：

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a>检查 Finance and Operations 应用的虚拟机上的同步错误

**查看错误所需的角色：** 系统管理员

1. 登录 Microsoft Dynamics Lifecycle Services (LCS)。
2. 打开选择要对其进行双写入测试的 LCS 项目。
3. 选择 **云托管的环境** 磁贴。
4. 使用远程桌面登录到 Finance and Operations 应用的虚拟机 (VM)。 使用 LCS 中显示的本地帐户。
5. 打开事件查看器。
6. 选择 **应用程序和服务日志 \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**。
7. 查看最近错误的列表。

## <a name="unlink-and-link-another-dataverse-environment-from-a-finance-and-operations-app"></a>从 Finance and Operations 应用取消链接并链接另一个 Dataverse 环境

**取消环境链接所需的角色：** Finance and Operations 应用或 Dataverse 的系统管理员。

1. 登录到 Finance and Operations 应用。
2. 转到 **工作区 \> 数据管理**，然后选择 **双写入** 磁贴。
3. 选择所有正在运行的映射，然后选择 **停止**。
4. 选择 **取消链接环境**。
5. 选择 **是** 以确认操作。

现在，您可以链接新环境。

## <a name="unable-to-view-the-sales-order-line-information-form"></a>无法查看销售订单行“信息”窗体 

在 Dynamics 365 Sales 中创建销售订单时，单击 **+ 添加产品** 可能会将您重定向到 Dynamics 365 Project Operations 订单行窗体。 从该窗体无法查看销售订单行 **信息** 窗体。 **信息** 选项未出现在 **新订单行** 下方的下拉菜单中。 发生这种情况是因为您的环境中已经安装了 Project Operations。

要重新启用 **信息** 窗体选项，请按照下列步骤操作：
1. 导航到 **订单行** 表。
2. 在窗体节点下找到 **信息** 窗体。 
3. 选择 **信息** 窗体并单击 **启用安全角色**。 
4. 将安全设置更改为 **向所有人显示**。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]