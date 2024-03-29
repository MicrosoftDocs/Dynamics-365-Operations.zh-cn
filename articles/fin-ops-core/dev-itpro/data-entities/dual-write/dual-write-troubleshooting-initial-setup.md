---
title: 解决初始设置过程中的问题
description: 本文提供可以帮助您解决在双写入集成的初始设置期间所发生问题的信息。
author: RamaKrishnamoorthy
ms.date: 08/10/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: d33fc6f4895b53f16cc6957a3a2fc6b1abe90a2f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289505"
---
# <a name="troubleshoot-issues-during-initial-setup"></a>解决初始设置过程中的问题

[!include [banner](../../includes/banner.md)]

本文提供财务和运营应用与 Dataverse 之间的双写入集成的疑难解答信息。 具体来说，提供可以帮助您解决在双写入集成的初始设置期间可能发生的问题的信息。

> [!IMPORTANT]
> 本文解决的某些问题可能需要系统管理员角色或 Microsoft Azure Active Directory (Azure AD) 租户管理员凭据。 介绍每个问题的每一节说明了是否需要特定角色或凭据。

## <a name="you-cant-link-a-finance-and-operations-app-to-dataverse"></a>您无法将财务和运营应用链接到 Dataverse

**设置双写入所需的角色：** 财务和运营应用和 Dataverse 中的系统管理员。

**设置到 Dataverse 的链接** 页面上的错误通常是由不完整的设置或权限问题引起的。 请在 **设置到 Dataverse 的链接** 页面上通过了整个运行状况检查，如下图所示。 除非整个运行状况检查通过，否则您无法链接双写入。

![成功的运行状况检查。](media/health_check.png)

您必须具有 Azure AD 租户管理员凭据才能链接财务和运营和 Dataverse 环境。 链接环境后，用户可以使用其帐户凭据登录并更新现有表映射。

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a>查找可以为双写入链接的法人或公司的数量限制

当您尝试启用映射时，您可能会收到以下错误消息：

*双写入失败 - 插件注册失败：[（无法获取项目的分区映射 DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea。错误超出了映射 DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea 允许的最大分区）]，发生一个或多个错误。*

链接环境时的当前限制约为 40 个法人。 如果您尝试启用映射，并且在环境之间链接了超过 40 个法人，将发生此错误。

## <a name="connection-set-failed-while-linking-environment"></a>链接环境时连接集失败

链接双重写入环境时，操作失败，出现错误消息：

*保存连接集失败！已添加具有相同密钥的物料。*

双重写入不支持具有相同名称的多个法人/公司。 例如，如果您在 Dataverse 中有两个名称为“DAT”的公司，则会收到此错误消息。

若要解锁客户，请从 Dataverse 内的 **cdm_company** 表中删除重复记录。 此外，如果 **cdm_company** 表具有空白名称的记录，请删除或更正这些记录。

## <a name="error-when-opening-the-dual-write-page-in-finance-and-operations-apps"></a>在财务和运营应用中打开双写入页面时出错

当您尝试为双重写入链接 Dataverse 环境时，您可能会收到以下错误消息：

*响应状态代码未指示成功：404（未找到）。*

当应用同意步骤完成时，将发生此错误。 您可以通过使用租户管理员帐户登录 `portal.azure.com` 来验证是否已提供同意，并检查 ID 为 `33976c19-1db5-4c02-810e-c243db79efde` 的第三方应用是否显示在 AAD 的企业应用程序列表中。 如果没有，则按下一节中所述重新运行同意步骤。

### <a name="providing-app-consent"></a>提供应用同意

+ 使用您的管理员凭据启动以下 URL。

    `https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent`

+ 选择 **接受** 以表示同意。 您同意在租户中安装应用（具有 `id=33976c19-1db5-4c02-810e-c243db79efde`）。
+ Dataverse 需要此应用才能与财务和运营应用通信。

    ![初始同步设置疑难解答。](media/Initial-sync-setup-troubleshooting-1.png)

> [!NOTE]
> 如果这不起作用，请在 Microsoft Edge 的专用模式或 Chrome 的匿名模式下启动 URL。

## <a name="finance-and-operations-environment-is-not-discoverable"></a>无法发现财务和运营环境

您可能会收到以下错误消息：

*无法发现财务和运营应用环境 \*\*\*.cloudax.dynamics.com。*

存在两个可能导致环境无法发现的问题：

+ 用于登录的用户与财务和运营实例不在同一租户中。
+ 一些由 Microsoft 托管的旧财务和运营实例存在发现问题。 要解决此问题，请更新财务和运营实例。 通过任何更新，将可以发现环境。

## <a name="403-forbidden-error-while-connections-are-being-created"></a>创建连接时出现 403（禁止）错误

作为双重写入链接流程的一部分，将在链接 Power Apps 环境中代表用户创建两个 Dataverse 连接（也称为 *Apihub* 连接）。 如果客户没有 Power Apps 环境的许可证，则创建 ApiHub 连接将会失败，并且显示 403（禁止）错误。 以下是错误消息的示例：

> MSG=\[无法设置双重写入环境。 错误详细信息：响应状态代码未指示成功：403（已禁止）。 - 响应状态代码未指示成功：403 （已禁止）。\] STACKTRACE=\[   位于 Microsoft.Dynamics.Integrator.ProjectManagementService.DualWrite.DualWriteConnectionSetProcessor.\<CreateDualWriteConnectionSetAsync\>d\_\_29.MoveNext() in X:\\bt\\1158727\\repo\\src\\ProjectManagementService\\DualWrite\\DualWriteConnectionSetProcessor.cs:line 297 --- 从先前引起异常的位置结束堆栈跟踪 --- 位于 System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw() 位于 System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification（任务：任务）位于 Microsoft.Dynamics.Integrator.ProjectManagementService.Controllers.DualWriteEnvironmentManagementController.\<SetupDualWriteEnvironmentAsync\>d\_\_34.MoveNext() in X:\\bt\\1158727\\repo\\src\\ProjectManagementService\\Controllers\\DualWriteEnvironmentManagementController.cs:line 265\]

由于缺少 Power Apps 许可证，出现此错误。 向用户分配适当的许可证（例如 Power Apps 试用版 2 计划），以便用户有权创建连接。 要验证许可证，客户可以转到[我的帐户](https://portal.office.com/account/?ref=MeControl#subscriptions)站点，以查看当前分配给用户的许可证。

有关 Power Apps 许可证的详细信息，请参阅以下文章：

- [向用户分配许可证](/microsoft-365/admin/manage/assign-licenses-to-users?view=o365-worldwide)
- [为组织购买 Power Apps](/power-platform/admin/signup-for-powerapps-admin)

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

