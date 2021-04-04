---
title: 解决 Finance and Operations 应用中的双写入问题
description: 本主题提供故障排除信息，可以帮助您解决 Finance and Operations 应用中的双写入模块问题。
author: RamaKrishnamoorthy
manager: AnnBe
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
ms.openlocfilehash: 9bff8ad0c5716648dec6eadfb21412a2b17f155e
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561218"
---
# <a name="troubleshoot-dual-write-issues-in-finance-and-operations-apps"></a>解决 Finance and Operations 应用中的双写入问题

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

本主题提供 Finance and Operations 应用与 Dataverse 之间的双写入集成的故障排除信息。 具体来说，提供可以帮助您解决 Finance and Operations 应用中的 **双写入** 模块问题的信息。

> [!IMPORTANT]
> 本主题解决的某些问题可能需要系统管理员角色或 Microsoft Azure Active Directory (Azure AD) 租户管理员凭据。 介绍每个问题的每一节说明了是否需要特定角色或凭据。

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>您无法在 Finance and Operations 应用中加载双写入模块

如果您无法通过选择 **数据管理** 工作区中的 **双写入** 磁贴来打开 **双写入** 页面，则说明数据集成服务可能中断。 请创建支持票证请求重新启动数据集成服务。

## <a name="error-when-you-try-to-create-a-new-table-map"></a>尝试创建新表映射时出错

**解决此问题所需的凭据：** 设置双写入的同一用户。

当您尝试为双写入配置新表时，您可能会收到以下错误消息。 可以创建映射的唯一用户是设置双写入连接的用户。

*响应状态代码未指示成功：401（未授权）*


## <a name="error-when-you-open-the-dual-write-user-interface"></a>打开双写入用户界面时出错

当您尝试从 **数据管理** 工作区访问双写入时，您可能会收到以下错误消息：

*login.microsoftonline.com 拒绝连接。*

要解决此问题，请使用 Microsoft Edge 中的隐私模式窗口、Chromium 中的匿名窗口或 Google Chrome 中的匿名窗口登录。 您还必须取消阻止或清除第三方 Cookie。

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-table-mapping"></a>为双写入链接环境或添加新表映射时出错

**解决此问题所需的角色：** 同时是 Finance and Operations 应用和 Dataverse 的系统管理员。

链接或创建映射时，您可能会遇到以下错误：

*响应状态代码未指示成功：403 (tokenexchange)。<br>会话 ID：\<your session id\><br> 根活动 ID：\<your root activity id\>*

如果您没有足够的权限链接双写入或创建映射，则会发生此错误。 如果在不取消双写入链接的情况下重置了 Dataverse 环境，也会发生此错误。 任何在 Finance and Operations 应用和 Dataverse 中都具有系统管理员角色的用户都可以链接环境。 只有设置双写入连接的用户才可以添加新表映射。 设置后，具有系统管理员角色的任何用户都可以监视状态并编辑映射。

## <a name="error-when-you-stop-the-table-mapping"></a>停止表映射时出错

当您尝试停止表映射时，您可能会收到以下错误消息：

*\[已禁止\]，\[{来自令牌交换的 "status":403,"source":"","message":"Error：不允许用户访问连接 dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\]，远程服务器返回错误：(403) 已禁止。*

当链接的 Dataverse 环境不可用时，将发生此错误。

要解决此问题，请为数据集成团队创建票证。 附加网络跟踪，以便数据集成团队可以在后端将映射标记为 **未运行**。

## <a name="error-while-trying-to-start-a-table-mapping"></a>尝试开始表映射时出错

当您尝试将映射的状态设置为 **正在运行** 时，可能会收到如下错误：

*无法完成初始数据同步。错误：双写入失败 - 插件注册失败：无法建立双写入查找元数据。错误对象引用未设置为对象的实例。*

此错误的解决方法取决于错误原因：

+ 如果映射具有相关映射，请确保启用此表映射的相关映射。
+ 映射可能缺少源或目标列。 如果缺少 Finance and Operations 应用中的列，请按照[映射中缺少表列问题](dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps)一节中的步骤进行操作。 如果缺少 Dataverse 中的列，请单击映射上的 **刷新表** 按钮，让这些列自动填充回映射中。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]