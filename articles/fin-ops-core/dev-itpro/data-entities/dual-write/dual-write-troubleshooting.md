---
title: 数据集成疑难解答指南
description: 本主题提供 Finance and Operations 应用与 Common Data Service 之间的数据集成的疑难解答信息。
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
ms.openlocfilehash: 87bdb72024c1c3844ff61e832a92f7edcc77c5d6
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019661"
---
# <a name="troubleshooting-guide-for-data-integration"></a>数据集成疑难解答指南

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

## <a name="enable-plug-in-trace-logs-in-common-data-service-and-inspect-the-dual-write-plug-in-error-details"></a>在 Common Data Service 中启用插件跟踪日志和检查双写入插件错误详细信息

如果在双写入同步期间遇到问题或错误，请执行以下步骤在跟踪日志中检查这些错误。

1. 必须先启用插件跟踪日志，才能检查这些错误。 有关说明，请参阅[教程：编写和注册插件](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs)中的“查看跟踪日志”部分。

    现在可以检查错误。

2. 登录到 Microsoft Dynamics 365 Sales。
3. 选择**设置**按钮（齿轮符号），然后选择**高级设置**。
4. 在**设置**菜单中，选择**自定义 \> 插件跟踪日志**。
5. 为类型名称选择 **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** 以显示错误详细信息。

## <a name="inspect-dual-write-synchronization-errors"></a>检查双写入同步错误

执行以下步骤以在测试期间检查错误。

1. 登录 Microsoft Dynamics Lifecycle Services (LCS)。
2. 打开要为其执行双写入测试的 LCS 项目。
3. 选择**云托管的环境**。
4. 使用 LCS 中显示的本地帐户建立与应用程序虚拟机 (VM) 之间的远程桌面连接。
5. 打开事件查看器。 
6. 转到**应用程序和服务日志 \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**。 将显示错误和详细信息。

## <a name="unlink-one-common-data-service-environment-from-the-application-and-link-another-environment"></a>取消一个 Common Data Service 环境与应用程序之间的链接并链接另一个环境

执行以下步骤以更新链接。

1. 转到应用程序环境。
2. 打开数据管理
3. 选择**链接到面向应用程序的 CDS**。
4. 选择正在运行的所有映射，然后选择**停止**。
5. 选择所有映射，然后选择**删除**。

    > [!NOTE]
    > 如果选择 **CustomerV3-Account** 模板，则**删除**选项不可用。 根据需要取消选择此模板。 **CustomerV3-Account** 是较早设置的模板，支持目标客户到现金解决方案。 因为是全局发布的，所以在所有模板下都显示。

6. 选择**取消链接环境**。
7. 选择**是**以确认操作。
8. 若要链接新的环境，请执行[安装指南](https://aka.ms/dualwrite-docs)中的步骤。
