---
title: 常规疑难解答
description: 本文提供财务和运营应用与 Dataverse 之间的双写入集成的一般故障排除信息。
author: RamaKrishnamoorthy
ms.date: 04/18/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2f263e331d23ce0ddf60a4abc2467513aa342445
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/02/2022
ms.locfileid: "9112355"
---
# <a name="general-troubleshooting"></a>常规疑难解答

[!include [banner](../../includes/banner.md)]



本文提供财务和运营应用与 Dataverse 之间的双写入集成的一般故障排除信息。

> [!IMPORTANT]
> 本文解决的某些问题可能需要系统管理员角色或 Microsoft Azure Active Directory (Azure AD) 租户管理员凭据。 介绍每个问题的每一节说明了是否需要特定角色或凭据。

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a>在 Dataverse 中启用和查看插件跟踪日志以查看错误详细信息

在对财务和运营和 Dataverse 之间的双写入实时同步问题进行故障排除时，跟踪日志会非常有用。 这些日志可以向为 Dynamics 365 提供技术和工程支持的团队提供具体的详细信息。 本文介绍如何启用跟踪日志以及如何查看这些日志。 跟踪日志在 Dynamics 365 设置页面进行管理，需要管理员级别的特权才能更改和查看。 

**打开跟踪日志和查看错误所需的角色：** 系统管理员

### <a name="turn-on-the-trace-log"></a>打开跟踪日志
若要打开跟踪日志，请执行以下步骤。

1.  登录到 Dynamics 365，然后在顶部导航栏中选择 **设置**。 在系统页面上，单击 **管理**。
2.  在管理页面，单击 **系统设置**。
3.  选择 **自定义** 选项卡和插件，然后在自定义工作流活动跟踪部分，将下拉列表更改为 **所有**。 这将跟踪所有活动，并为必须审查潜在问题的团队提供一组全面的数据。

> [!NOTE]
> 将下拉列表设置为 **异常** 只会在发生异常（错误）时提供跟踪信息。

启用后，将继续收集插件跟踪日志，除非返回此位置，选择 **关** 手动将其关闭。

### <a name="view-the-trace-log"></a>查看跟踪日志
若要查看跟踪日志，请执行以下步骤。

1. 在 Dynamics 365 设置页面上，在顶部导航栏中选择 **设置**。 
2. 在页面的 **自定义** 部分选择 **插件跟踪日志**。
3. 您可以根据类型名称和/或消息名称在跟踪日志列表中查找条目。
4. 打开所需条目可以查看完整日志。 “执行”部分的消息块将为插件提供可用信息。 如果有，还将提供异常详细信息。 

您可以复制跟踪日志的内容并将其粘贴到其他应用程序（如记事本或其他工具）中，来查看日志或文本文件，以便更轻松地查看所有内容。 

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>启用调试模式来解决财务和运营应用中的实时同步问题

**查看错误所需的角色：** 系统管理员

源自 Dataverse 的双写入错误可能出现在财务和运营应用中。 要为错误启用详细日志记录，请执行以下步骤：

1. 对于财务和运营应用中的所有项目配置，**DualWriteProjectConfiguration** 表上有一个 **IsDebugMode** 标志。
2. 使用 Excel 加载项打开 **DualWriteProjectConfiguration**。 若要使用加载项，请在财务和运营 Excel 加载项中启用设计模式，并将 **DualWriteProjectConfiguration** 添加到表中。 有关详细信息，请参阅[使用 Excel 查看和更新实体数据](../../office-integration/use-excel-add-in.md)。
3. 针对此项目将 **IsDebugMode** 设置为 **是**。
4. 运行产生错误的方案。
5. 详细日志存储在 **DualWriteErrorLog** 表中。
6. 要查找表浏览器上的数据，请使用以下链接：`https://999aos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`，并根据需要替换 `999`。
7. 在 [KB 4595434](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=98e5dc124ac125c57ad633d885ac612aea3ddb8f4abf9d71ab3aa354f2e06cbe) 后重新更新，该知识库文章可用于平台更新 37 及更高版本。 如果您已安装此修复程序，则调试模式将捕获更多日志。  

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a>检查财务和运营应用的虚拟机上的同步错误

**查看错误所需的角色：** 系统管理员

1. 登录 Microsoft Dynamics Lifecycle Services (LCS)。
2. 打开选择要对其进行双写入测试的 LCS 项目。
3. 选择 **云托管的环境** 磁贴。
4. 使用远程桌面登录到财务和运营应用的虚拟机 (VM)。 使用 LCS 中显示的本地帐户。
5. 打开事件查看器。
6. 选择 **应用程序和服务日志 \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**。
7. 查看最近错误的列表。

## <a name="dual-write-ui-landing-page-showing-blank"></a>双写入 UI 登陆页面显示空白
在 Microsoft Edge 或 Google Chrome 浏览器中打开双写入页面时，主页无法加载，您会看到空白页面或“出现问题”等错误。
在 Devtools 中，您在控制台日志中看到错误：

>bundle.eed39124e62c58ef34d2.js:37 DOMException：无法从“Window”读取“sessionStorage”属性：访问此文档被拒绝。 at t.storeInSessionStorage (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:16:136860 ) at new t (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:69:20103 ) at ci (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:44115 ) at Eo (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:58728 ) at jo (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:65191 ) at Nr (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:84692 ) at Or (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:85076 ) at Ss (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:91750 ) at vs (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:91130 ) at hs (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:90151 )

UI 会使用浏览器“会话存储”来存储一些用于加载主页的属性值。 为此，需要在站点的浏览器中允许第三方 cookie。 此错误指示 UI 无法访问会话存储。 遇到此问题可能有两种情况：

1.  您在 Edge/Chrome 的匿名模式下打开 UI，第三方 Cookie 在匿名模式下被阻止。
2.  您在 Edge/Chrome 中完全阻止了第三方 Cookie。

### <a name="mitigation"></a>减轻
需要在浏览器设置中允许第三方 Cookie。

### <a name="google-chrome-browser"></a>Google Chrome 浏览器
第 1 个选项：
1.  在地址栏中输入 chrome://settings/ 转到设置，然后导航到“隐私和安全 -> Cookie 和其他站点数据”。
2.  选择“允许所有 Cookie”。 如果您不希望使用此方法，请转到第二个选项。

第 2 个选项：
1.  在地址栏中输入 chrome://settings/ 转到设置，然后导航到“隐私和安全 -> Cookie 和其他站点数据”。
2.  如果选择了“在匿名模式下阻止第三方 Cookie”或“阻止第三方 Cookie”，请转到“始终可以使用 Cookie 的站点”，单击 **添加**。 
3.  添加您的财务和运营应用站点名称 - https://<your_FinOp_instance>.cloudax.dynamics.com。 确保选中“所有 Cookie，仅在此站点”复选框。 

### <a name="microsoft-edge-browser"></a>Microsoft Edge 浏览器
1.  导航到“设置 -> 站点权限 -> Cookie 和站点数据”。
2.  关闭“阻止第三方 Cookie”。  

## <a name="unlink-and-link-another-dataverse-environment-from-a-finance-and-operations-app"></a>从财务和运营应用取消链接和链接其他 Dataverse 环境

**取消环境链接所需的角色：** 财务和运营应用或 Dataverse 的系统管理员。

1. 登录财务和运营应用。
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

## <a name="how-to-ensure-data-integration-is-using-the-most-current-finance-and-operations-schema"></a>如何确保数据集成使用的是最新财务和运营架构

如果没有使用最新的架构，您可能会在数据集成中遇到数据问题。 以下步骤将帮助您刷新财务和运营应用中的实体列表以及数据集成器中的实体。

### <a name="refresh-entity-list-in-finance-and-operations-environment"></a>在财务和运营环境中刷新实体列表
1.  登录到您的财务和运营环境。
2.  选择 **数据管理**。
3.  在“数据管理”内，选择 **框架参数**。
4.  在 **数据导入/导出框架参数** 页面上，选择 **实体设置** 选项卡，然后选择 **刷新实体列表**。 这可能需要 30 多分钟才能刷新，具体取决于涉及的实体数。
5.  导航到 **数据管理** 并选择 **数据实体** 以验证是否列出了预期实体。 如果未列出预期实体，请验证实体是否出现在您的财务和运营环境中，并根据需要恢复缺失的实体。

#### <a name="if-the-refresh-fails-to-resolve-the-issue-delete-and-re-add-the-entities"></a>如果刷新无法解决问题，请删除并重新添加实体

> [!NOTE]
> 您可能需要在删除之前停止任何当前正在使用实体的处理组。

1.  在财务和运营环境中选择 **数据管理** 并选择 **数据实体**。
2.  搜索有问题的实体，并记下目标实体、暂存表、实体名称和其他设置。 从列表中删除一个或多个实体。
3.  选择 **新建** 并使用第 2 步中的数据重新添加一个或多个实体。 

#### <a name="refresh-entities-in-data-integrator"></a>刷新数据集成器中的实体
登录到 Power Platform 管理中心并选择 **数据集成**。 打开出现问题的项目，然后选择 **刷新实体**。

## <a name="how-to-enable-and-save-network-trace-so-that-traces-can-be-attached-to-support-tickets"></a>如何启用和保存网络跟踪，以便跟踪可以附加到支持票证

支持团队可能需要查看网络跟踪以解决某些问题。 要创建网络跟踪，请按照下列步骤操作：

### <a name="google-chrome-browser"></a>Google Chrome 浏览器

1. 在打开的选项卡中，按 **F12** 或选择 **开发人员工具** 以打开开发人员工具。
2. 打开 **网络** 选项卡并筛选器文本框中键入 **integ**。
3. 运行您的方案并遵守所记录的要求。
4. 右键单击条目，然后选择 **全部另存为包含内容的 HAR**。

### <a name="microsoft-edge-browser"></a>Microsoft Edge 浏览器

1. 在打开的选项卡中，按 **F12** 或选择 **开发人员工具** 以打开开发人员工具。
2. 打开 **网络** 选项卡。
3. 运行您的方案。
4. 选择 **保存** 以将结果导出为 HAR。

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

