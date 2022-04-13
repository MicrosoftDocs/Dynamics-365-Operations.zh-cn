---
title: 检测被放弃的购物车并向客户发送通知
description: 本主题介绍如何自定义 Microsoft Dynamics 365 Commerce 被放弃购物车连接器示例应用，以检测被放弃的购物车并向客户发送提醒电子邮件通知。
author: bicyclingfool
ms.date: 02/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 1db4e988653aa55db2b18fb201edeafc4d16a1bc
ms.sourcegitcommit: ab690bc897699ff8a4c489e749251fe0367050ca
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/26/2022
ms.locfileid: "8489022"
---
# <a name="detect-abandoned-carts-and-send-notifications-to-customers"></a>检测被放弃的购物车并向客户发送通知

[!include [banner](../includes/banner.md)]

本主题介绍如何自定义 Microsoft Dynamics 365 Commerce 被放弃购物车连接器示例应用，以检测被放弃的购物车并向客户发送提醒电子邮件通知。

通过被放弃购物车通知恢复收入和留住客户的能力是 Dynamics 365 Commerce 支持的一项重要功能。 通过自定义 Commerce 被放弃购物车连接器示例应用，零售商可以访问 Retail Server 上在零售商定义的时间窗口内未修改的购物车。 然后这些购物车可以被检索，利用产品和客户数据扩增，并被传递给可以生成电子邮件通知并将通知发送给客户的第三方电子邮件市场营销提供商。

客户收到的被放弃购物车电子邮件通知可以包含以下信息：

- 客户的名字。
- 客户的姓氏。
- 客户的电子邮件地址。
- 将客户返回到购物车的 URL。
- 交易币种。
- 客户购物车中的产品列表。 对于每个产品，包括以下信息：

    - 产品的显示名称
    - 产品 ID（用于组合产品描述页面的 URL）
    - 可以自动调整大小以适应不同视区大小的产品图像
    - 产品图像的替代文本
    - 产品的单价

## <a name="abandoned-cart-connector-sample"></a>被放弃购物车连接器示例

Microsoft 通过 Retail 软件开发套件 (SDK) 提供的连接器模型支持检索被放弃的购物车信息，并将信息发送给第三方电子邮件市场营销提供商。 此连接器处理与 Retail Server 的通信，使用 Azure Key Vault 确保安全，处理指定时间窗口内的购物车检索计划，以及检索订单和产品数据。 另外还提供与第三方电子邮件市场营销提供商集成的示例实现。 此连接器被构建为天然地可与 [Emarsys](https://emarsys.com) 通信。 但是，可以轻松地对它进行自定义来与其他解决方案集成，如 Constant Contact、Mailchimp 和 SendGrid。

下图显示了被放弃购物车连接器示例应用的组件。

![被放弃购物车连接器示例应用的组件](media/AbandonedCartConnector.png)

> [!IMPORTANT]
> 某些区域要求客户要能够选择不将他们的购物车数据传递给电子邮件市场营销提供商，或要求删除他们的数据。 但是，Microsoft 没有为客户提供这些选项。 因此，如果您计划在有强制要求的区域开展业务，您必须提供所需的基础结构和自定义来跟踪客户的偏好，并根据这些要求阻止客户数据被传递到您的电子邮件平台。 您还必须定义一个流程，来根据客户的请求从您的电子邮件市场营销提供商处清除客户数据。

## <a name="obtain-the-code-sample"></a>获取代码示例

自版本 10.0.16 起，被放弃购物车连接器示例应用包含在 Retail SDK 中。 此代码可以在 **\\RetailSDK\\Code\\SampleExtensions\\RetailServer\\Extensions.AbandonedCartSample** 下找到。 有关 Retail SDK 及其获取位置的详细信息，请参阅 [Retail 软件开发套件 (SDK)](retail-sdk/retail-sdk-overview.md)。

> [!NOTE]
> 虽然示例代码首先在 10.0.16 版本中提供，但它与 Retail Server 的 10.0.13 和更高版本兼容。

## <a name="prerequisites-and-dependencies"></a>先决条件和依赖项

必须先满足以下先决条件，才能部署和配置被放弃购物车连接器示例代。

### <a name="access-to-commerce-resources"></a>对 Commerce 资源的访问权限

要配置和部署被放弃购物车连接器应用，您必须有权访问以下 Commerce 资源：

- 对您的环境的 Commerce Headquarters 的管理员访问权限
- 对您的环境的 Microsoft Dynamics Lifecycle Services (LCS) 项目的访问权限

### <a name="azure-cosmos-db"></a>Azure Cosmos DB

被放弃购物车连接器应用使用 Azure Cosmos DB 来跟踪之前检索到的购物车的 ID 和时间戳。 您可以使用 Azure Cosmos DB 来保留此数据，也可以自定义代码示例来与其他数据存储选项集成。 有关 Azure Cosmos DB 的详细信息，请参阅[欢迎使用 Azure Cosmos DB](/azure/cosmos-db/introduction)。

如果您使用 Azure Cosmos DB，则必须满足以下先决条件才能运行示例：

- 您必须有有效的 Azure Cosmos DB 帐户。 如果您没有帐户，请参阅[创建数据库帐户](/azure/cosmos-db/create-sql-api-dotnet#create-a-database-account)。
- 您必须从您在 Azure 门户中的 Azure Cosmos DB 帐户的 **密钥** 边栏选项卡检索 **URI** 和 **主密钥**（或 **二级密钥**）值。 有关如何检索 Azure Cosmos DB 帐户的终结点和密钥信息的详细信息，请参阅[查看、复制和重新生成访问密钥和密码](/azure/cosmos-db/manage-account#keys)。

### <a name="azure-key-vault"></a>Azure Key Vault

被放弃购物车连接器应用使用 Key Vault 来存储需要安全访问权限的不同组件的名称和机密。

要设置密钥保管库，请按照以下步骤操作。

1. 请按照[使用门户在 Azure Stack Hub 中管理 Key Vault](/azure-stack/user/azure-stack-key-vault-manage-portal?view=azs-2002&preserve-view=true) 中的说明操作。
2. 为以下信息创建机密：

    - Emarsys 应用程序编程接口 (API) 用户名和 API 密码
    - 被放弃购物车应用程序 ID 和机密

被放弃购物车连接器示例代码使用 Azure 默认凭据访问 Key Vault。 您必须为计划用于访问 Key Vault 的身份提供 **列出** 和 **读取** 权限。

有关 Azure 默认凭据的详细信息，请参阅 [DefaultAzureCredential 类](/dotnet/api/azure.identity.defaultazurecredential?view=azure-dotnet&preserve-view=true)。

## <a name="create-an-abandoned-cart-connector-sample-app-application-id-for-the-azure-ad-tenant"></a>为 Azure AD 租户创建被放弃购物车连接器示例应用的应用程序 ID

您必须为 Azure Active Directory (AD) 租户创建被放弃购物车连接器示例应用的应用程序 ID。 有关如何创建应用程序 ID 的信息，请参阅[使用门户创建可访问资源的 Azure AD 应用程序和服务主体](/azure/active-directory/develop/howto-create-service-principal-portal)。

## <a name="add-the-abandoned-cart-connector-sample-app-application-id-to-the-allow-list-for-the-retail-server-api"></a>将被放弃购物车连接器示例应用的应用程序 ID 添加到 Retail Server API 的允许列表

接下来，您必须将被放弃购物车连接器示例应用的应用程序 ID 添加到 Retail Server API 的允许列表。 有关如何将应用程序 ID 添加到 Azure 中的允许列表的信息，请参阅 [Retail Server 中的服务到服务身份验证支持](https://community.dynamics.com/ax/b/axforretail/posts/support-for-service-to-service-authentication-in-retail-server)。

## <a name="configure-the-abandoned-cart-connector-sample-app"></a>配置被放弃购物车连接器示例应用

要配置被放弃购物车连接器示例应用，请修改位于 **AbandonedCartDetectionSample** 目录根目录的 **appSettings.json** 配置文件。 下表介绍了配置文件属性。

### <a name="keyvaultoptions"></a>KeyVaultOptions

| 属性    | Description |
| ----------- | ----------- |
| KeyVaultURI | 您在 Azure 门户中使用的密钥保管库的域名系统 (DNS) 名称。 |

### <a name="retailserverclientoptions"></a>RetailServerClientOptions

| 属性                                      | Description |
| --------------------------------------------- | ----------- |
| TenantId                                      | 您的 Azure 租户的 Azure AD 租户 ID。 |
| RetailServerAudienceId                        | Retail Server 受众 ID。 可以保留默认值。 |
| AppIdKeyVaultSecretName                       | 您为被放弃购物车连接器示例应用的应用程序 ID 创建的机密的名称。 |
| AppSecretKeyVaultSecretName                   | 存储被放弃购物车连接器示例应用应用程序 ID 的应用机密的机密名称。 |
| RetailServerUrl                               | 您的 Retail Server 实例的 URL。 您可以在 LCS 中找到此值。 |
| OperatingUnitNumber                           | 运营单位编号 (OUN)。 您可以在 Commerce headquarters 中找到此值。 |
| IncludeAbandonedCartsModifiedSinceLastMinutes | 您要检索的被放弃购物车的时间窗口的开始时间。 此值以当前时间之前的分钟数表示。 例如，将此属性设置为 **120** 可以检索在 120 分钟前和 **ExcludeAbandonedCartsModifiedSinceLastMinutes** 属性定义的时间窗口结束之间最后修改的所有购物车。 |
| ExcludeAbandonedCartsModifiedSinceLastMinutes | 您要检索的被放弃购物车的时间窗口的结束时间。 此值以当前时间之前的分钟数表示。 例如，如果 **IncludeAbandonedCartsModifiedSinceLastMinutes** 属性设置为 **120**，将此属性设置为 **30** 可以检索在 120 分钟前到 30 分钟前修改的所有购物车。 实际上，此属性定义您希望在正式宣布放弃购物车之前等待的时间量。 |
| ReturnToCartUrl                               | 您的电子商务网站上购物车的 URL，采用 **app.config** 文件中使用的格式。 |

### <a name="azurecosmosoptions"></a>AzureCosmosOptions

被放弃购物车的检索作业状态、购物车 ID 和修改时间戳存储在 Azure Cosmos DB 中。 默认情况下，配置文件中的设置指向 Azure Cosmos DB 的本地模拟器实例。 将连接器部署到生产环境时，必须更新这些设置，让它们指向 Azure 订阅中的 Azure Cosmos DB 实例。 要进行本地测试或沙盒测试，您可以使用 [Azure Cosmos DB Emulator](/azure/cosmos-db/local-emulator)。

| 属性    | Description |
| ----------- | ----------- |
| EndPointUri | Azure 或模拟器提供的终结点 URI。 |
| PrimaryKey  | Azure 或模拟器提供的主密钥。 |
| DatabaseId  | 数据库 ID。 您可以保留默认值或提供您自己的值。 |
| ContainerId | 容器 ID。 您可以保留默认值或提供您自己的值。 |

### <a name="emarsysclientoptions"></a>EmarsysClientOptions

> [!NOTE]
> 如果您与 Emarsys 以外的电子邮件市场营销提供商集成，您必须根据需要扩展 **IEmailProvider** 接口以与该提供商通信。

| 属性                      | Description |
| ----------------------------- | ----------- |
| ApiUrl                        | `https://api.emarsys.net/api/v2/event/{0}/trigger` |
| ExternalEventId               | 在 Emarsys 中创建的外部事件记录的 ID。 您可以在您创建的用于发送被放弃购物车电子邮件通知的市场活动中的 **触发器设置** 下找到此值。 |
| ApiUserNameKeyVaultSecretName | 存储 Emarsys API 用户名的密钥的名称。 |
| ApiSecretKeyVaultSecretName   | 存储 Emarsys API 机密的密钥的名称。 |
| EmarsysContactKeyId           | Emarsys 联系人数据库中电子邮件列的 ID。 默认值为 **3**，不必更改。 |

### <a name="mediaoptions"></a>MediaOptions

如果您在 Commerce 中使用电子商务功能，可以使用 Commerce 数字资产管理来检索产品图像。 有关数字资产管理中的图像大小调整器功能的详细信息，请参阅 [ImageSettings 视区配置](../e-commerce-extensibility/image-component.md#imagesettings-viewport-configuration)。

| 属性                             | Description |
| ------------------------------------ | ----------- |
| ImageServerUrl                       | 您的站点的数字资产管理器的根 URL。 您可以在 Commerce headquarters 的 **Retail 和 Commerce \> 渠道设置 \> 渠道配置文件** 的 **Media Server Base URL** 属性密钥中找到此值。 |
| ImageViewPorts                       | 各个视区配置的容器节点。 |
| ImageViewPorts/viewport              | 视区定义。 使用此属性指定视区的宽度范围，以像素为单位。 有关显示此属性如何使用的示例，请参见 **appSettings.json** 配置文件。 |
| ImageViewPorts/imageWidth            | 视区的图像宽度，以像素为单位。 |
| imageViewPorts/imageHeight           | 视区的图像高度，以像素为单位。 |
| imageViewPorts/useForDefaultImageTag | 一个 **true**/**false** 值，指示如果 Web 浏览器或电子邮件客户端不支持 `<picture>` HTML 标记，是否应使用视区定义的图像维度。 |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
