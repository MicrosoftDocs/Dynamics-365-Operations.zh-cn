---
title: 配置 SharePoint 通道
description: 本文说明如何配置 Microsoft SharePoint 通道以处理传入的电子发票。
author: dkalyuzh
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 89538adde4d14212fb0deccad05f828d146f16db
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910032"
---
# <a name="configure-a-sharepoint-channel"></a>配置 SharePoint 通道

[!include [banner](../includes/banner.md)]

作为配置 Microsoft SharePoint 通道以处理传入文档的先决条件，请完成[配置 SharePoint 连接](e-invoicing-create-sharepoint-connection.md)中所述的步骤。

然后，您可以使用 SharePoint 通道从存储在 SharePoint 文件夹中的文件中导入电子供应商发票。

1. 在您的 SharePoint 站点上，创建以下文件夹：

    - **主文件夹** – 服务将从其处理文件的文件夹。
    - **存档文件夹** – 将存储已处理文件的文件夹。
    - **错误文件夹** – 如果处理失败，系统会将文件移动到的文件夹。

2. 在 Regulatory Configuration Service (RCS) 中，选择您创建的电子开票功能。 确保您选择具有 **草稿** 状态的版本。
3. 在 **设置** 选项卡上，选择 **添加**。
4. 在 **创建功能设置** 下拉对话框中的 **新** 字段组中，选择 **自定义设置** 选项。
5. 在 **设置类型** 字段组中，选择 **数据渠道** 选项。
6. 在 **选择数据渠道** 字段中，选择 **SharePoint 文件夹**。
7. 选择 **创建**。
8. 选择您创建的行，然后选择 **编辑**。
9. 在 **数据渠道** 选项卡上，在 **参数** 部分，设置以下必填字段。

    | 字段                 | Description |
    |-----------------------|-------------|
    | 数据渠道          | 输入一个唯一名称来标识数据渠道。 名称最多可以包含 10 个字符。 它将被在适用性规则以及在通信过程中在连接的应用程序中引用。 |
    | SharePoint 地址    | 输入 SharePoint URL。 例如，输入 `<domain>.sharepoint.com`。 |
    | 应用程序 ID        | 输入包含 SharePoint 用户帐户 ID 的 Azure Key Vault 机密的名称。 此机密必须在 Key Vault 中创建，并且必须在您的服务环境中设置。 此值是来自 [配置 SharePoint 连接](e-invoicing-create-sharepoint-connection.md)的 **应用程序（客户端）ID** 值。 |
    | 应用程序密钥    | 输入包含 SharePoint 用户帐户密码的 Key Vault 机密的名称。 此值是来自 [配置 SharePoint 连接](e-invoicing-create-sharepoint-connection.md)的 **应用注册机密** 值。 |
    | 站点名称             | 输入 SharePoint 站点的名称。 |
    | 文档库名称 | 输入 SharePoint 文档库的名称。 |
    | 超时               | 输入系统应等待响应的最长时间，以毫秒 (ms) 为单位。 默认值为 10,000 毫秒（10 秒）。 |
    | 主文件夹           | 指定文件导入源，或服务应处理的文件所来自的文件夹。 |
    | 存档文件夹        | 指定应存储已处理文件的文件夹。 |
    | 错误文件夹          | 指定处理失败时系统应将文件移动到的文件夹。 |
    | 最大文件大小         | 输入处理的单个文件的最大大小，以字节为单位。 默认值为 20,000,000 字节。 |
    | 最大文件数      | 输入单个操作可处理的最大文件数。 如果您不想限制文件数量，将值设置为 **0**（零）。 |
    | 文件筛选器           | 输入字符串以按文件名进行筛选。 此字段为可选字段。 支持简单的掩码，如 **\*smth\*.ext**，其中的每个星号 (\*) 表示字符出现零次或多次。 例如，输入 **\*.pdf** 来配置读取 PDF 文件的渠道。 |
    | 自定义文件名      | 输入来自客户端的自定义文件名。 |

10. 根据需要，在 **适用性规则** 选项卡上查看和更新条件。 **渠道** 字段的值必须等于您在上一步中在 **数据渠道** 字段中输入的值。
11. 选择 **保存**，然后关闭页面。
