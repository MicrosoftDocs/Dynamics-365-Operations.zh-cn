---
title: 用于零售商店的用户定义的证书配置文件
description: 本文概述了在 Microsoft Dynamics 365 Commerce 中可用的证书配置文件。
author: josaw1
ms.date: 09/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: v-chgriffin
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.search.industry: Retail
ms.search.form: RetailFormLayout, RetailParameters
ms.openlocfilehash: 5baf043a43210d819b605546089e981c86922ca9
ms.sourcegitcommit: 4f28f262cfb8f047cb5c0070261aa0748835e74b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/21/2022
ms.locfileid: "9558429"
---
# <a name="user-defined-certificate-profiles-for-retail-stores"></a>用于零售商店的用户定义的证书配置文件

[!include [banner](../includes/banner.md)]

本文概述了在 Microsoft Dynamics 365 Commerce 中可用的证书配置文件。 此功能通过添加对本地证书的支持扩展了[管理零售渠道机密](../dev-itpro/manage-secrets.md)功能。

销售点 (POS) 在脱机模式下运行，它无法访问存储在 Microsoft Azure Key Vault 中的证书。 应该改为使用本地证书。 支持以下功能：

- 在 Key Vault 后备方案中使用本地证书
- 使用本地证书，但不在 Key Vault 中（例如，在本地安装中）
- 逐步更新证书，其中一些商店和终端使用证书的新版本，而其他商店和终端继续使用以前的版本

证书配置文件功能使您可以指定默认证书，并设置搜索同一证书配置文件中的证书的顺序。 此功能还为本地证书和密钥保管库证书提供了类似的设置方法。 您可以为证书添加公司特定的设置，但是可以在 Commerce 渠道中使用每个证书的唯一跨公司标识符。

### <a name="scenarios"></a>方案

在 Commerce 渠道中，证书配置文件功能支持以下方案：

- 在 Key Vault 后备方案中使用本地证书。 以下是这些后备方案的一些示例：

    - 无法访问密钥保管库存储。
    - 在密钥保管库存储中找不到证书。
    - POS 在脱机模式下运行。

- 使用本地证书，但不将它们存储在 Key Vault 中（例如，在本地安装中）。
- 逐步更新证书，其中证书的新版本仅在已经有新版本的商店或终端中使用。
- 在多家公司中使用相同的证书。

## <a name="set-up-certificate-profiles"></a>设置证书配置文件

以下过程说明了如何设置证书配置文件。

### <a name="set-up-key-vault"></a>设置 Key Vault

必须先完成以下步骤，然后您才能使用存储在 Key Vault 中的数字证书。

1. 创建 Key Vault 存储帐户。 我们建议您将存储帐户与 Commerce Scale Unit 部署在同一地理区域中。
1. 将数字证书上载到 Key Vault 存储帐户。
1. 向应用程序对象服务器 (AOS) 应用程序授予从 Key Vault 存储帐户读取机密的权限。

有关如何使用密钥保管库的详细信息，请参阅[开始使用 Azure 密钥保管库](/azure/key-vault/key-vault-get-started)。

### <a name="set-up-system-parameters"></a>设置系统参数

在 Commerce 渠道中配置证书配置文件之前，您必须允许 Commerce 使用存储在 Key Vault 中的证书和证书配置文件。

要在 Commerce headquarters 中设置系统参数，请按照以下步骤操作。

1. 在 **系统参数** 页面，将 **使用高级证书存储** 选项设置为 **是**。
1. 在 **功能管理** 工作区中，打开 **零售商店的用户定义的证书配置文件** 功能。

### <a name="set-up-key-vault-parameters"></a>设置 Key Vault 参数

在 **Key Vault 参数** 页面，您必须指定以下用于访问 Key Vault 存储的参数：

- **名称** 和 **说明** - Key Vault 存储帐户的名称和说明。
- **Key Vault URL** – Key Vault 存储帐户的 URL。
- **Key Vault 客户端** – 与用于进行身份验证的 Key Vault 存储帐户关联的 Azure Active Directory (Azure AD) 应用程序的交互式客户端 ID。 此客户端应有权从存储帐户中读取密钥。
- **Key Vault 密钥** – 与 Key Vault 存储帐户中用于进行身份验证的 Azure AD 应用程序关联的密钥。
- **名称**、**描述** 和 **密钥引用** - 证书的名称、描述和密钥引用。

有关详细信息，请参阅[设置 Azure Key Vault 客户端](../../finance/localizations/setting-up-azure-key-vault-client.md)。

### <a name="configure-a-certificate-profile"></a>配置证书配置文件

要在 Commerce Headquarters 中配置证书配置文件，请按照下列步骤操作。

1. 转到 **系统管理 \> 设置 \> 证书配置文件**。
1. 在操作窗格上，选择 **新建** 创建记录。
1. 在 **证书配置文件**、**名称** 和 **说明** 字段中输入值。

    > [!NOTE]
    > 证书配置文件是跨所有公司和 Commerce 组件的证书的唯一标识符。

1. 在 **法人** 快速选项卡上，选择 **添加** 添加一行。
1. 在 **法人** 下，选择应该使用当前证书配置文件的法人（公司）。

    如果证书配置文件应该用于多个法人，重复步骤 4 和 5 为每个其他法人添加一行。

1. 选择 **设置** 以打开 **证书配置文件设置** 页面，您可以在其中为证书配置文件输入公司特定的设置。 指定在 Commerce 渠道中调用当前证书配置文件时可以使用哪些证书。 根据需要添加任意数量的证书，并为它们设置优先级。 如果具有更高优先级的证书不可用，将根据优先级使用下一个证书。 有关详细信息，请参阅[工作流：在 Commerce Runtime 中搜索证书](#workflow-searching-certificates-in-the-commerce-runtime)一节。

    > [!NOTE]
    > **优先级** 字段将自动设置。 值 **1** 表示最高优先级。 当在 **证书配置文件设置** 页面上添加新行时，将其优先级设置为比上一行高一个优先级的数字。 若要更改特定行的优先级，请选择该行，然后选择 **上移** 来提高优先级，或选择 **下移** 来降低优先级。

1. 当您将新行添加到 **证书配置文件设置** 页面时，设置以下字段：

    - **位置类型** – 选择证书的存储位置。 该字段有两个可能的值：**本地证书** 和 **密钥保管库**。
    - **密钥保管库证书** – 如果您将 **位置类型** 设置为 **密钥保管库**，此字段为必填字段。 使用它来指定密钥保管库证书机密。
    - **存储名称** – 该字段是可选字段，仅在您将 **位置类型** 字段设置为 **本地证书** 时才可用。 使用它来指定应该用于搜索本地证书的默认存储名称。
    - **存储位置** – 该字段是可选字段，仅在您将 **位置类型** 字段设置为 **本地证书** 时才可用。 使用它来指定应该用于搜索本地证书的默认存储位置。

        > [!NOTE]
        > 添加默认存储名称和存储位置，以简化在 Commerce Runtime 中搜索本地证书的过程。 X509StoreProvider 具有存储证书的文件夹列表。 如果未指定默认存储名称和默认存储位置，则 X509StoreProvider 会尝试在其列表上的其他文件夹中查找证书。 有关商店名称和商店位置的可用值的更多信息，请参阅 [StoreName 枚举](/dotnet/api/system.security.cryptography.x509certificates.storename)和 [StoreLocation 枚举](//dotnet/api/system.security.cryptography.x509certificates.storelocation)。

    - **指纹** – 此字段是必填字段，仅在您将 **位置类型** 字段设置为 **本地证书** 时才可用。 使用它来指定证书指纹。

        > [!IMPORTANT]
        > 您必须确保运行必须使用本地证书的应用程序（例如，离线模式下的 Modern POS）的用户至少具有对证书私钥的只读访问权限。

    - **注释** – 该字段是可选字段，允许用户输入说明。

## <a name="workflow-searching-certificates-in-the-commerce-runtime"></a>工作流：在 Commerce Runtime 中搜索证书

这是用于在 Commerce Runtime 中调用证书配置文件时搜索证书的基本工作流。

1. 系统识别证书配置文件是否具有当前法人的公司特定设置。
1. 系统尝试通过对 **优先级** 字段设置为 **1** 的行使用 **证书配置文件设置** 页面上的值来查找证书。

    - 如果 **位置类型** 字段设置为 **密钥保管库**，**密钥保险库证书机密** 字段的值将用于搜索 **密钥保管库参数** 页面上的证书。 然后，在密钥保管库存储中搜索证书。
    - 如果 **位置类型** 字段设置为 **本地证书**，如果指定了这些参数，则 X509StoreProvider 首先使用默认存储名称和存储位置搜索证书。 然后，它搜索其文件夹列表上的所有其他文件夹。

1. 如果找不到证书，则针对 **优先级** 字段设置为 **2** 的行重复该过程，以此类推。

> [!NOTE]
> 如果证书配置文件没有当前法人的设置，或者证书搜索对 **证书配置文件设置** 页面上的所有行都不起作用，则找不到证书。

### <a name="caching-the-results-of-certificate-searches"></a>缓存证书搜索的结果

缓存证书搜索的结果。 缓存的默认到期时间为一小时。 但是，该时间可以自定义，并且最大值可以设置为 24 小时。

## <a name="gradual-update"></a>逐步更新

如果引入了新版本的证书，但不能同时在所有商店中更新它，则证书配置文件功能可以逐渐更新证书。

1. 查找证书配置文件和应更新的行，然后选择 **设置**。
1. 添加一行，然后指定与证书的最新版本相关的设置。
1. 增加新行的 **优先级** 值。 使用 **上移** 按钮以移动该行，使其位于同一证书的上一版本的行上方。
> [!NOTE]
> 在 Commerce Runtime 中，将首先调用证书的新版本。 如果尚未在特定商店或特定终端中更新证书，则将调用以前的版本。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
