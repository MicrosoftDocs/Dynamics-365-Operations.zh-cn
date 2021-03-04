---
title: 设置 IoT 智能的 Azure 资源
description: 此主题介绍如何创建和配置 IoT 智能所需 Microsoft Azure 资源。
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1277d2ab8bb1f2925874f7469250e164f6bde62d
ms.sourcegitcommit: 092ef6a45f515b38be2a4481abdbe7518a636f85
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4423312"
---
# <a name="set-up-azure-resources-for-iot-intelligence"></a>设置 IoT 智能的 Azure 资源

[!include [banner](../../includes/banner.md)]

此主题介绍如何创建和配置 IoT 智能所需 Microsoft Azure 资源。

## <a name="create-azure-resources"></a>创建 Azure 资源

执行以下步骤创建 Microsoft Dynamics 365 Supply Chain Management 可访问的 IoT 中心、Redis 缓存和密钥保管库。

### <a name="verify-that-the-microsoft-dynamics-erp-microservices-first-party-app-id-is-in-your-tenant"></a>验证租户中是否有 Microsoft Dynamics ERP Microservices 第一方应用 ID

若要验证租户中是否有 Microsoft Dynamics ERP Microservices 第一方应用的应用 ID，请执行以下步骤。

1. 登录 Azure 门户，地址为 <https://portal.azure.com>。
2. 转到 **Azure Active Directory**。
3. 转到 **企业应用程序**。
4. 在 **应用程序类型** 字段中，选择 **Microsoft 应用程序**。
5. 在搜索字段中，输入 **Microsoft Dynamics ERP Microservices**。
6. 验证列表中是否有 **Microsoft Dynamics ERP Microservices**。 其他应用程序的名称类似。 因此，请务必查找正确的应用程序。 应用 ID 为 **0cdb527f-a8d1-4bf8-9436-b352c68682b2**。

    如果列表中无此应用程序，则必须将其添加到您的租户中：

    1. 在 Azure 门户中工具栏上，选择按钮打开 Azure Cloud Shell。
    2. 运行命令 **Install-Module AzureAD**。 输入 **Y** 安装此模块。
    3. 运行命令 **Get-InstalledModule -Name "AzureAD"** 验证是否安装了此模块。
    4. 运行 **Connect-AzureAD -Confirm** 运行身份验证。
    5. 运行命令 **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**。

    现在可重复步骤 1 到 6 验证租户中是否有此应用 ID。

### <a name="create-a-key-vault-resource"></a>创建密钥保管库资源

若要创建密钥保管库资源，请执行以下步骤。

1. 在 Azure 门户中，创建或转到资源组。
2. 选择 **添加**。
3. 在 **新建** 页的搜索字段中，输入 **密钥保管库**。 然后选择 **创建**。
4. 在 **创建密钥保管库** 页的 **密钥保管库名称** 字段中，输入一个名称。
5. 查看默认值，然后选择 **查看 + 创建**。
6. 选择 **创建**。

将在后台创建密钥保管库。

### <a name="create-an-iot-hub-resource"></a>创建 IoT 中心资源

若要创建 IoT 中心资源，请执行以下步骤。

1. 创建或转到一个资源组。
2. 选择 **添加**。
3. 在 **新建** 页的搜索字段中，输入 **IoT 中心**。 然后选择 **创建**。
4. 在 **IoT 中心名称** 字段中输入名称。
5. 查看默认值，然后选择 **查看 + 创建**。
6. 选择 **创建**。

将在后台创建 IoT 中心。

> [!NOTE]
> 建议仅为每个环境创建一个 IoT 中心资源。

### <a name="create-a-redis-cache-resource"></a>创建 Redis 缓存资源

若要创建 Redis 缓存资源，请执行以下步骤。

1. 创建或转到一个资源组。
2. 选择 **添加**。
3. 在 **新建** 页的搜索字段中，输入 **Redis 的 Azure 缓存**。 然后选择 **创建**。
4. 在 **DNS 名称** 字段中输入名称。
5. 查看默认值，然后选择 **创建**。

将在后台创建 Redis 缓存。

> [!NOTE]
> 建议仅为每个环境创建一个 Redis 缓存。

现在已经创建了所有资源。

## <a name="configure-the-azure-resources"></a>配置 Azure 资源

### <a name="configure-the-iot-hub"></a>配置 IoT 中心

若要配置 IoT 中心，请执行以下步骤。

1. 在资源中，选择 IoT 中心资源。
2. 在左侧导航窗格中，选择 **内置终结点**。
3. 在 **用户组** 下，粘贴以下用户组。 这些用户组对应于现成方案。

    + microsoft.dynamics.iotintelligence-1
    + microsoft.dynamics.iotintelligence-2
    + microsoft.dynamics.iotintelligence-3

### <a name="configure-the-key-vault"></a>配置密钥保管库

若要配置密钥保管库，请执行以下步骤。

1. 在资源中，选择密钥保管库资源。
2. 在左侧导航窗格中，选择 **访问策略**。
3. 选择 **添加访问策略**。
4. 在 **添加访问策略** 页面的 **选择权限** 字段中，选择 **获取** 和 **列表**。
5. 在 **选择主体** 中单击。
6. 在 **主体** 对话框中，搜索并选择 **Microsoft Dynamics ERP Microservices**。 然后选择 **选择**。
7. 选择 **添加**。
8. 选择 **保存**。

此应用现在可访问密钥保管库中的密码。

### <a name="save-the-iot-hub-connection-string-secret"></a>保存 IoT 中心连接字符串密码

若要保存 IoT 中心连接字符串的密码，请执行以下步骤。

1. 在资源中，选择 IoT 中心资源。
2. 在左侧导航窗格中，选择 **内置终结点**。
3. 复制 **事件中心兼容的终结点** 字段中的值，
4. 转到密钥保管库资源。
5. 在左侧导航窗格中，选择 **密码**。
6. 选择 **生成/导入**。
7. 在 **名称** 字段中输入名称。
8. 在 **值** 字段中，粘贴您之前复制的终结点值。
9. 选择 **创建**。

### <a name="save-the-redis-cache-connection-string-secret"></a>保存 Redis 缓存连接字符串密码

若要保存 Redis 缓存连接字符串的密码，请执行以下步骤。

1. 在资源中，选择 Redis 缓存资源。
2. 选择 **访问密钥**。
3. 复制 **主连接字符串** 字段中的值。
4. 转到密钥保管库资源。
5. 在左侧导航窗格中，选择 **密码**。
6. 选择 **生成/导入**。
7. 在 **名称** 字段中输入名称。
8. 在 **值** 字段中，粘贴您之前复制的连接字符串。
9. 选择 **创建**。

> [!NOTE]
> 只要更新其中一个连接字符串，必须也更新密码值。

现在已预配完了所需 Azure 资源。 下一步是[在 Microsoft Dynamics Lifecycle Services (LCS) 中安装 IoT 智能加载项](iot-lcs-setup.md)。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]