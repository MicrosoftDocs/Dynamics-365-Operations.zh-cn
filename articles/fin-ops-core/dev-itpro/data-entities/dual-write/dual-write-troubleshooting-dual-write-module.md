---
title: 解决 Finance and Operations 应用有关双写入模块的问题
description: 本主题提供故障排除信息，可以帮助您解决 Finance and Operations 应用中的双写入模块问题。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
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
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 34c10e38400a72a670a93f2a72d0aa7a4aed561a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172752"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a>解决 Finance and Operations 应用有关双写入模块的问题

[!include [banner](../../includes/banner.md)]



本主题提供 Finance and Operations 应用与 Common Data Service 之间的双写入集成的故障排除信息。 具体来说，提供可以帮助您解决 Finance and Operations 应用中的**双写入**模块问题的信息。

> [!IMPORTANT]
> 本主题解决的某些问题可能需要系统管理员角色或 Microsoft Azure Active Directory (Azure AD) 租户管理员凭据。 介绍每个问题的每一节说明了是否需要特定角色或凭据。

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>您无法在 Finance and Operations 应用中加载双写入模块

如果您无法通过选择**数据管理**工作区中的**双写入**磁贴来打开**双写入**页面，则说明数据集成服务可能中断。 请创建支持票证请求重新启动数据集成服务。

## <a name="error-when-you-try-to-create-a-new-entity-mapping"></a>尝试创建新的实体映射时出错

**解决此问题所需的凭据：** Azure AD 租户管理员

当您尝试为双写入配置新实体时，您可能会收到以下错误消息：

*响应状态代码未指示成功：401（未授权）*

发生此错误是因为只有 Azure AD 租户管理员可以添加新的实体映射。

要解决此问题，请作为 Azure AD 管理员租户登录到 Finance and Operations 应用。 您还必须转到 web.PowerApps.com 重新验证您的连接。

## <a name="error-when-you-open-the-dual-write-user-interface"></a>打开双写入用户界面时出错

当您尝试从**数据管理**工作区访问双写入时，您可能会收到以下错误消息：

*login.microsoftonline.com 拒绝连接。*

要解决此问题，请使用 Microsoft Edge 中的隐私模式窗口、Chromium 中的匿名窗口或 Google Chrome 中的匿名窗口登录。 您还必须取消阻止或清除第三方 Cookie。

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a>为双写入链接环境或添加新实体映射时出错

**解决此问题所需的凭据：** Azure AD 租户管理员

链接或创建映射时，您可能会遇到以下错误：

*响应状态代码未指示成功：403 (tokenexchange)。<br>会话 ID：\<您的会话 ID\><br>根活动 ID：\<您的根活动 ID\>*

如果您没有足够的权限链接双写入或创建映射，则会发生此错误。 您必须使用 Azure AD 租户管理员帐户链接环境和添加新实体映射。 不过，设置后，您可以使用非管理员帐户监视状态和编辑映射。

## <a name="error-when-you-stop-the-entity-mapping"></a>停止实体映射时出错

当您尝试停止实体映射时，您可能会收到以下错误消息：

*\[已禁止\]，\[{来自令牌交换的 "status":403,"source":"","message":"Error：不允许用户访问连接 dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\]，远程服务器返回错误：(403) 已禁止。*

当链接的 Common Data Service 环境不可用时，将发生此错误。

要解决此问题，请为数据集成团队创建票证。 附加网络跟踪，以便数据集成团队可以在后端将映射标记为**未运行**。
