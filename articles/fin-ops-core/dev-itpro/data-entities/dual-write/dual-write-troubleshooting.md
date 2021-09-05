---
title: 常规故障排除
description: 本主题提供 Finance and Operations 应用与 Dataverse 之间的双写入集成的常规故障排除信息。
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: b4adc2d83667a05d14a26ace23e5bd8026df4b5f
ms.sourcegitcommit: caa41c076f731f1e02586bc129b9bc15a278d280
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/13/2021
ms.locfileid: "7380204"
---
# <a name="general-troubleshooting"></a>常规故障排除

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

本主题提供 Finance and Operations 应用与 Dataverse 之间的双写入集成的常规故障排除信息。

> [!IMPORTANT]
> 本主题解决的某些问题可能需要系统管理员角色或 Microsoft Azure Active Directory (Azure AD) 租户管理员凭据。 介绍每个问题的每一节说明了是否需要特定角色或凭据。

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

**查看错误所需的角色：** 系统管理员

源自 Dataverse 的双写入错误可能出现在 Finance and Operations 应用中。 要为错误启用详细日志记录，请执行以下步骤：

1. 对于 Finance and Operations 应用中的所有项目配置，**DualWriteProjectConfiguration** 表上有一个 **IsDebugMode** 标志。
2. 使用 Excel 加载项打开 **DualWriteProjectConfiguration**。 若要使用加载项，请在 Finance and Operations Excel 加载项中启用设计模式，并将 **DualWriteProjectConfiguration** 添加到表中。 有关详细信息，请参阅[使用 Excel 查看和更新实体数据](../../office-integration/use-excel-add-in.md)。
3. 针对此项目将 **IsDebugMode** 设置为 **是**。
4. 运行产生错误的方案。
5. 详细日志存储在 **DualWriteErrorLog** 表中。
6. 要查找表浏览器上的数据，请使用以下链接：`https://999aos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`，并根据需要替换 `999`。
7. 在 [KB 4595434](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=98e5dc124ac125c57ad633d885ac612aea3ddb8f4abf9d71ab3aa354f2e06cbe) 后重新更新，该知识库文章可用于平台更新 37 及更高版本。 如果您已安装此修复程序，则调试模式将捕获更多日志。  

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

## <a name="how-to-enable-and-save-network-trace-so-that-traces-can-be-attached-to-support-tickets"></a>如何启用和保存网络跟踪，以便跟踪可以附加到支持票证

支持团队可能需要查看网络跟踪以解决某些问题。 要创建网络跟踪，请按照下列步骤操作：

### <a name="chrome"></a>Chrome

1. 在打开的选项卡中，按 **F12** 或选择 **开发人员工具** 以打开开发人员工具。
2. 打开 **网络** 选项卡并筛选器文本框中键入 **integ**。
3. 运行您的方案并遵守所记录的要求。
4. 右键单击条目，然后选择 **全部另存为包含内容的 HAR**。

### <a name="microsoft-edge"></a>Microsoft Edge

1. 在打开的选项卡中，按 **F12** 或选择 **开发人员工具** 以打开开发人员工具。
2. 打开 **网络** 选项卡。
3. 运行您的方案。
4. 选择 **保存** 以将结果导出为 HAR。

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
