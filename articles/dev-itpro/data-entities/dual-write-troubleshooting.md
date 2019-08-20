---
title: 数据集成疑难解答指南
description: 本主题提供有关 Microsoft Dynamics 365 for Finance and Operations 与 Common Data Service 之间的数据集成的疑难解答信息。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: ca62a6b3aa64ec2383ee3ded3b7bbf4650a41166
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797267"
---
# <a name="troubleshooting-guide-for-data-integration"></a>数据集成疑难解答指南

## <a name="enable-plugin-trace-in-common-data-service-and-check-the-dual-write-plugin-error-details"></a>启用  Common Data Service 中的插件跟踪和检查双写入插件错误详细信息

如果遇到了双写入同步问题或错误，可以在跟踪日志中检查错误：

1. 必须先按照[登记簿插件](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs)中有关启用插件跟踪说明启用插件跟踪，才能检查错误。 现在可以检查错误。
2. 登录到 Dynamics 365 for Sales。
3. 单击“设置”图标（齿轮），然后选择**高级设置**。
4. 在**设置**菜单中，选择**自定义 > 插件跟踪日志**。
5. 单击类型名称 **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** 以显示错误详细信息。

## <a name="check-dual-write-synchronization-errors-in-finance-and-operations"></a>在 Finance and Operations 中检查双写入同步错误

可通过执行以下步骤检查测试期间发生的错误：

+ 登录 LifeCycle Services (LCS)。
+ 打开选择要对其执行双写入测试的 LCS 项目。
+ 转到云托管的环境。
+ 将在 LCS 中显示使用本地帐户的 Finance and Operations VM 的远程桌面。
+ 打开事件查看器。 
+ 导航到**应用程序和服务日志 > Microsoft > Dynamics > AX-DualWriteSync > Operational**。 将显示错误和详细信息。

## <a name="how-to-unlink-and-link-another-common-data-service-environment-from-finance-and-operations"></a>如何从 Finance and Operations 取消链接和链接其他 Common Data Service 环境

可通过执行以下步骤更新链接：

+ 导航到 Finance and Operations 环境。
+ 打开数据管理
+ 单击**链接到面向应用程序的 CDS**。
+ 选择所有正在运行的映射，然后单击**停止**。 
+ 选择所有映射，然后单击**删除**。

    > [!NOTE]
    > 如果选择 **CustomerV3-Account** 模板，则不显示**删除**选项。 如果需要，则不选择。 **CustomerV3-Account** 是较早设置的模板，支持目标客户到现金解决方案。 因为是全局发布的，所以在所有模板下都显示。

+ 单击**取消链接环境**。
+ 单击**是**确认。
+ 若要链接新的环境，请执行[安装指南](https://aka.ms/dualwrite-docs)中的步骤。

