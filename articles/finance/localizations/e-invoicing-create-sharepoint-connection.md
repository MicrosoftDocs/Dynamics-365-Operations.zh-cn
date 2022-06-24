---
title: 配置 SharePoint 连接
description: 本文说明如何配置连接，以使电子开票可以访问 Microsoft SharePoint 站点。
author: dkalyuzh
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fb4258190b9480c1302060dd7b75145f80bb7f18
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856571"
---
# <a name="configure-a-sharepoint-connection"></a>配置 SharePoint 连接

[!include [banner](../includes/banner.md)]

电子开票服务可以读取 Microsoft SharePoint 文件夹中的文件并将文件上载到 SharePoint。 为确保电子开票可以访问特定的 SharePoint 站点，您必须向电子开票服务提供站点凭据。 此外，为确保安全存储凭据，请勿直接提供凭据。 而是将其存储在 Azure 密钥保管库中，并提供 Azure 密钥保管库机密。

## <a name="grant-access-to-a-sharepoint-folder"></a>授予对 SharePoint 文件夹的访问权限

1. 在安装了 Regulatory Configuration Service (RCS) 的租户中创建应用注册。

    1. 登录 [Azure 门户](https://portal.azure.com/)。
    2. 转到 **应用注册**。
    3. 选择 **新注册**。
    4. 输入名称，如 **用于电子开票的 SharePoint 应用**，然后完成注册
    5. 选择新的应用注册。
    6. 在 **身份验证** 选项卡上，启用 **允许公共客户端流** 选项。
    4. 在 **证书和机密** 选项卡上，选择 **新建客户端密码** 创建客户端密码。
    5. 复制创建的机密的值。

    请遵照以下准则：

    - 不要对不同的服务使用相同的应用注册。
    - 执行[密码政策建议](/microsoft-365/admin/misc/password-policy-recommendations?view=o365-worldwide)。
    - 设置密码轮换。 在轮换期间，为应用注册创建新的客户端密码，更新密钥保管库，然后删除旧密码。

2. 在电子开票环境设置中将 **应用注册机密** 和 **应用程序（客户端）ID** 值作为两个新机密保存在密钥保管库中。
3. 在 RCS 中的电子发票环境的设置中将您创建的机密添加到 Key Vault 参数中。
4. 在 Azure 门户中，授予对 SharePoint 的访问权限。 此步骤应由租户管理员完成。

    1. 选择您创建的应用注册。
    2. 在 **API 权限** 选项卡上，选择 **添加权限**。
    3. 选择 **Microsoft graph (应用程序权限)** \> **Sites.Selected**。
    4. 选择 **为 \<user&nbsp;name\> 授予管理员同意**。
    5. 查看 **状态** 字段，确保已授予权限。

        ![API 权限选项卡上的已授予权限。](media/configured-permissions.jpg)

    6. 打开 [Graph 浏览器 - Microsoft Graph](https://developer.microsoft.com/graph/graph-explorer) 并登录。
    7. 在左侧窗格中的 **示例查询** 选项卡上，在 **SharePoint 站点** 下，选择 **根据站点的相对路径获取 SharePoint 站点**。
    8. 填写 **\{host-name\}** 和 **\{server-relative-path\}** 参数。 例如，**\{host-name\}** 填写 `<domain>.sharepoint.com`，**\{server-relative-path\}** 填写 `sites/<siteName>`。

        > [!NOTE]
        > 对于默认网站，将 **\{server-relative-path\}** 参数留空。

    9. 选择 **运行查询**，并保存结果。
    10. 配置以下查询。

        `POST https://graph.microsoft.com/v1.0/sites/{site-id}/permissions`

        在此查询中，**\{site-id\}** 是上一个查询响应中 **id** 节点的值。

        以下是请求正文。

        ```json
        {
            "roles": [
                "read",
                "write"
            ],
            "grantedToIdentities": [
                {
                    "application": {
                        "id": "{app-id}",
                        "displayName": "{app-name}"
                    }
                }
            ]
        }
        ```

        在此请求正文中，**\{app-id\}** 是 **应用程序（客户端）ID** 值，**\{app-name\}** 是 **应用程序名称** 值。

        ![POST 查询。](media/app-id-query.jpg)

    11. 在 **修改权限** 选项卡上，选择 **打开权限面板**，然后选择 **站点** \> **Sites.FullControl.All** \> **同意**。
    12. 选择 **运行查询**。

电子开票服务现在已经有权访问您的 SharePoint 站点了。
