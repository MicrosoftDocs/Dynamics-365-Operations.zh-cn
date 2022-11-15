---
title: 将 CPOS 配置为使用自定义 Azure AD 应用
description: 本文介绍如何将云 POS (CPOS) 配置为使用自定义 Azure Active Directory (Azure AD) 应用。
author: boycez
ms.date: 11/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: global
ms.author: boycez
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 5e4ff797410e1e94869cc37684e7622ec0d97842
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746252"
---
# <a name="configure-cpos-to-use-a-custom-azure-ad-app"></a>将 CPOS 配置为使用自定义 Azure AD 应用

[!include [banner](includes/banner.md)]

默认情况下，Microsoft Dynamics 365 Commerce 中的云 POS (CPOS) 指向 Azure Active Directory (Azure AD) 中注册的第一方 Microsoft 应用。 因此，您可以使用 CPOS，而无需对 Azure AD 进行任何更改。 但是，您可能需要将 CPOS 实例指向您控制的自定义 Azure AD 应用。 本文介绍如何将 CPOS 配置为使用自定义 Azure AD 应用。

## <a name="set-up-a-custom-retail-server-app-in-azure-ad"></a>在 Azure AD 中设置自定义 Retail Server 应用

若要在 Azure AD 中创建和配置自定义 Retail Server 应用，请执行以下步骤。

1. 使用任何 Azure AD 用户帐户登录到 [Azure Active Directory 管理中心](https://aad.portal.azure.com)。 用户帐户不必具有管理员权限。
1. 选择 **Azure Active Directory**。
1. 选择 **应用注册**，然后选择 **新注册** 以打开 **注册应用程序** 对话框。
1. 设置以下字段：

    - **名称** – 输入应用的自定义名称。 例如，输入 **自定义零售服务器**。
    - **支持帐户类型** - 选择默认选项，即 **仅此组织目录中的帐户（仅限 Microsoft - 单个租户）**。
    - **重定向 URI** - 此字段为可选字段。 请将其留空。
    - **服务树 ID** - 此字段为可选字段。 请将其留空。
    
1. 选择 **注册**。 此时会显示新注册应用的配置页面。
1. 在 **概览 \> 要素** 部分中，选择 **添加应用程序 ID URI**，然后选择 **应用程序 ID URI** 旁边的 **设置**。 记下建议的值，然后选择 **保存** 以接受该值。 
1. 选择 **添加范围**，然后设置以下字段：

    - **范围名称** - 输入范围的自定义名称。 例如，输入 **Legacy.Access.Full**。
    - **谁可以同意** - 根据您组织的安全策略，指定是管理员和用户还是只有管理员才能表示同意。
    - **管理员同意显示名称** - 输入显示名称。 例如，输入 **访问零售服务器**。
    - **管理员同意描述** - 输入描述。 例如，输入 **提供对零售服务器 API 的访问权限**。

1. 选择 **添加范围** 以完成范围创建流程。

## <a name="set-up-a-custom-cpos-app-in-azure-ad"></a>在 Azure AD 中设置自定义 CPOS 应用

> [!IMPORTANT]
> 如果您要升级在 Commerce 版本 10.0.21 之前创建的现有自定义 CPOS Azure AD 应用，请按照[升级在 Commerce 版本 10.0.21 之前创建的现有自定义 CPOS Azure AD 应用](#upgrade-an-existing-custom-cpos-azure-ad-app-created-before-commerce-version-10021)中的步骤操作。

若要在 Azure AD 中创建和配置自定义 CPOS 应用，请执行以下步骤。

1. 使用任何 Azure AD 用户帐户登录到 [Azure Active Directory 管理中心](https://aad.portal.azure.com)。 用户帐户不必具有管理员权限。
1. 选择 **Azure Active Directory**。
1. 选择 **应用注册**，然后选择 **新注册** 以打开 **注册应用程序** 对话框。
1. 设置以下字段：

    - **名称** – 为应用输入名称。 例如，输入 **自定义云 POS**。
    - **支持帐户类型** - 选择默认选项，即 **仅此组织目录中的帐户（仅限 Microsoft - 单个租户）**。
    - **重定向 URI** - 在下拉列表中选择 **单页应用程序 (SPA)**，然后输入您的 CPOS URI。
    - **服务树 ID** - 此字段为可选字段。 请将其留空。

1. 选择 **注册**。 此时会显示新注册应用的配置页面。
1. 在 **清单** 部分中，将 **oauth2AllowIdTokenImplicitFlow** 和 **oauth2AllowImplicitFlow** 参数设置为 **true**，然后选择 **保存**。
1. 在 **令牌配置** 部分中，按照这些步骤添加两项声明：

    1. 选择 **添加其他声明**。 将 **令牌类型** 字段设置为 **ID**，然后选择 **sid** 声明。 选择 **添加**。
    1. 选择 **添加其他声明**。 将 **令牌类型** 字段设置为 **访问**，然后选择 **sid** 声明。 选择 **添加**。

1. 在 **API 权限** 部分，选择 **添加权限**。
1. 在 **我的组织使用的 API** 选项卡上，搜索您在[在 Azure AD 中设置自定义 Retail Server 应用](#set-up-a-custom-retail-server-app-in-azure-ad)部分中创建的 Retail Server 应用。 然后，选择 **添加权限**。
1. 在 **概览** 部分的 **应用程序（客户端）ID** 字段中记下该值。

### <a name="upgrade-an-existing-custom-cpos-azure-ad-app-created-before-commerce-version-10021"></a>升级在 Commerce 版本 10.0.21 之前创建的现有自定义 CPOS Azure AD 应用

要升级在 Commerce 版本 10.0.21 之前创建的现有自定义 CPOS Azure AD 应用，请按照下列步骤操作。 

1. 在 Azure 门户中打开您的自定义 CPOS Azure AD 应用。
1. 选择 **身份验证** 选项卡。
1. 复制并保存 **Web** 类型的原始重定向 URI，以备以后使用，然后将其删除。
1. 选择 **添加平台**，然后选择 **单页应用程序 (SPA)**。
1. 将上面复制的原始 Web 重定向 URI 添加到 SPA 平台。
1. 在 **令牌配置** 部分中，按照这些步骤添加两项声明：
    1. 选择 **添加其他声明**。 将 **令牌类型** 字段设置为 **ID**，然后选择 **sid** 声明。 选择 **添加**。
    1. 选择 **添加其他声明**。 将 **令牌类型** 字段设置为 **访问**，然后选择 **sid** 声明。 选择 **添加**。

## <a name="update-the-cpos-configuration-file"></a>更新 CPOS 配置文件

打开 CPOS config.json 文件，并在其中进行以下更新。

1. 将 **AADClientId** 键值替换为您在 [在 Azure AD 中设置自定义 CPOS 应用](#set-up-a-custom-cpos-app-in-azure-ad)部分中创建的自定义 CPOS 应用的 **应用程序（客户端）ID** 值。
1. 将 **AADRetailServerResourceId** 键值替换为您在 [在 Azure AD 中设置自定义 Retail Server 应用](#set-up-a-custom-retail-server-app-in-azure-ad)部分中创建的自定义 Retail Server 应用的 **应用程序 ID URI** 值。

CPOS 在向 Azure AD 发送请求以获取安全令牌时将使用这两个参数。

## <a name="update-identity-providers-settings-in-commerce-headquarters"></a>更新 Commerce Headquarters 中的标识提供程序设置

然后，您必须更新 Commerce Headquarters 中的标识提供程序设置。

1. 在 Commerce Headquarters 中，打开 **Commerce 共享参数** 页面。
1. 在 **标识提供程序** 选项卡上的 **标识提供程序** 部分中，选择 **类型** 字段设置为 **Azure Active Directory** 且 **颁发者** 字段指向 Azure AD 租户的行。 此设置声明您将使用子网格，其中包含与 Azure AD 租户对应的标识提供程序相关的数据。
1. 在 **依赖方** 部分中，选择 **添加** 以添加行。
1. 设置以下字段：

    - **ClientId** - 输入您在 [在 Azure AD 中设置自定义 CPOS 应用](#set-up-a-custom-cpos-app-in-azure-ad)部分中创建的自定义 CPOS 应用的 **应用程序（客户端）ID** 值。
    - **类型** – 选择 **公共**。
    - **UserType** - 选择 **工作人员**。

1. 选择您添加的行。 **依赖方** 部分下方的 **服务器资源 ID** 部分显示了您在 **依赖方** 网格中选择的应用可以访问的 Retail Server 应用 ID。
1. 在 **服务器资源 ID** 部分中，选择 **添加** 以添加行。
1. 在 **服务器资源 ID** 字段中，输入您在 [在 Azure AD 中设置自定义 Retail Server 应用](#set-up-a-custom-retail-server-app-in-azure-ad)部分中创建的自定义 Retail Server 应用的 **应用程序 ID URI** 值。

    > [!IMPORTANT]
    > 前面步骤中提及的所有字段都区分大小写。 您输入的值必须与在 Azure AD 管理中心中配置的值完全匹配。

1. 转到 **Retail 和 Commerce IT \> 配送计划**，运行 **1110**（**全局配置**）作业。

现在，您可以使用自己的 Azure AD 应用激活 CPOS 设备。

## <a name="additional-resources"></a>其他资源

[销售点 (POS) 设备激活](dev-itpro/retail-device-activation.md)

[管理激活帐户并验证设备](set-up-activation-accounts-validate-devices-hq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
