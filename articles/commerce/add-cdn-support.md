---
title: 添加对内容交付网络 (CDN) 的支持
description: 此主题介绍如何向 Microsoft Dynamics 365 Commerce 环境添加内容交付网络 (CDN)。
author: brianshook
manager: annbe
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 662d26c0157377977bd1031cd7bb13a8e692f37e
ms.sourcegitcommit: 078befcd7f3531073ab2c08b365bcf132d6477b0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/31/2020
ms.locfileid: "3646031"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a>添加对内容交付网络 (CDN) 的支持


[!include [banner](includes/banner.md)]

此主题介绍如何向 Microsoft Dynamics 365 Commerce 环境添加内容交付网络 (CDN)。

## <a name="overview"></a>概览

在 Dynamics 365 Commerce 中设置电子商务环境时，可将其配置为支持 CDN 服务。 

可以在电子商务环境的预配过程中启用自定义域。 也可以在预配过程完成后使用服务请求设置。 电子商务环境的预配过程将生成一个与该环境关联的主机名。 此主机名采用以下格式，其中，\<*e-commerce-tenant-name*\> 是您的环境的名称：

&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com

预配过程中生成的主机名或终结点仅支持 \*.commerce.dynamics.com 采用安全套接字层 (SSL) 证书。 不支持自定义域支持采用 SSL。 因此，必须在 CDN 中终止自定义的 SSL，并将流量从 CDN 转发到 Commerce 生成的主机名或终结点。 

此外，Commerce 生成的终结点 (\*.commerce.dynamics.com) 还将提供*统计信息*（JavaScript 或级联样式表 \[CSS\] 文件）。 仅当将 Commerce 生成的主机名或终结点放在 CDN 后面时，才可以缓存这些统计信息。

## <a name="set-up-ssl"></a>设置 SSL

若要帮助确保设置 SSL，并且缓存统计信息，必须配置 CDN，使其与 Commerce 为您的环境生成的主机名关联。 还必须仅为统计信息缓存以下模式： 

/\_msdyn365/\_scnr/\*

为 Commerce 环境预配了提供自定义域或使用服务请求为环境提供了自定义域之后，请将自定义域指向 Commerce 生成的主机名或终结点。

前面介绍过，生成的主机名或终结点仅支持对 \*.commerce.dynamics.com 使用 SSL 证书。 不支持自定义域支持采用 SSL。

## <a name="cdn-services"></a>CDN 服务

所有 CDN 服务都可以用于 Commerce 环境。 下面是两个示例：

- **Microsoft Azure Front Door Service** – Azure CDN 解决方案。 有关 Azure Front Door Service 的详细信息，请参阅[Azure Front Door Service 文档](https://docs.microsoft.com/azure/frontdoor/)。
- **Akamai Dynamic Site Accelerator** – 有关详细信息，请参阅 [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp)。

## <a name="cdn-setup"></a>CDN 设置

CDN 的设置过程通常包含下面的步骤：

1. 添加前端主机。
1. 配置后端池。
1. 设置传递和缓存规则。

### <a name="add-a-front-end-host"></a>添加前端主机

可使用任何 CDN 服务，但是本主题中的示例则使用 Azure Front Door Service。 

有关如何设置 Azure Front Door Service 的信息，请参阅[快速入门：为高可用全局 Web 应用程序创建 Front Door](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door)。

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a>在 Azure Front Door 服务中配置后端池

若要在 Azure Front Door 服务中配置后端池，请执行以下步骤。

1. 向后端池添加 **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** 充当具有空后端主机标头的自定义主机。
1. 在**负载平衡**下，保留默认值。

下图显示 Azure Front Door 服务中输入了后端主机名的**添加后端**对话框。

![“添加后端池”对话框](./media/CDN_BackendPool.png)

下图显示 Azure Front Door 服务中具有默认负载均衡值的**添加后端池**对话框。

![“添加后端池”对话框（续）](./media/CDN_BackendPool_2.png)

### <a name="set-up-rules-in-azure-front-door-service"></a>在 Azure Front Door Service 中设置规则

若要在 Azure Front Door Service 中设置传递规则，请执行以下步骤。

1. 添加一个传递规则。
1. 在**名称**字段中，输入**默认**。
1. 在**接受的协议**字段中，选择 **HTTP 和 HTTPS**。
1. 在**前端主机**字段中，输入 **dynamics-ecom-tenant-name.azurefd.net**。
1. 在**匹配模式**下的上方字段中，输入 **/\***。
1. 在**传递详细信息**下，将**传递类型**设置为**转发**。
1. 在**后端池**字段中，选择 **ecom-backend**。
1. 在**转发协议**字段组中，选择**匹配请求**选项。 
1. 将 **URL 重写**选项设置为**禁用**。
1. 将**缓存**选项设置为**禁用**。

若要在 Azure Front Door Service 中设置缓存规则，请执行以下步骤。

1. 添加一个缓存规则。
1. 在**名称**字段中，输入**统计信息**。
1. 在**接受的协议**字段中，选择 **HTTP 和 HTTPS**。
1. 在**前端主机**字段中，输入 **dynamics-ecom-tenant-name.azurefd.net**。
1. 在**匹配模式**下的上方字段中，输入 **/\_msdyn365/\_scnr/\***。
1. 在**传递详细信息**下，将**传递类型**设置为**转发**。
1. 在**后端池**字段中，选择 **ecom-backend**。
1. 在**转发协议**字段组中，选择**匹配请求**选项。
1. 将 **URL 重写**选项设置为**禁用**。
1. 将**缓存**选项设置为**禁用**。
1. 在**查询字符串缓存行为**字段中，选择**缓存每个唯一 URL**。
1. 在**动态压缩**字段组中，选择**启用**选项。

下图显示 Azure Front Door Service 中的**添加规则**对话框。

![“添加规则”对话框](./media/CDN_CachingRule.png)

> [!WARNING]
> 如果要使用的域已激活且处于活动状态，请从 [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) 中的**支持**磁贴创建支持票证来获取后续步骤的帮助。 有关详细信息，请参阅[获取对 Finance and Operations 应用或 Lifecycle Services (LCS) 的支持](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md)。

如果您的域是新域，而不是预先存在的活动域，您可以将自定义域添加到 Azure Front Door 服务的配置中。 这将使 Web 流量可以通过 Azure Front Door 实例定向到您的站点。 若要添加自定义域（如 `www.fabrikam.com`），必须为该域配置一个规范名称 (CNAME)。

下图显示 Azure Front Door Service 中的 **CNAME 配置**对话框。

![“CNAME 配置”对话框](./media/CNAME_Configuration.png)

可使用 Azure Front Door Service 管理证书，也可以对自定义域使用您自己的证书。

下图显示 Azure Front Door Service 中的**自定义域 HTTPS** 对话框。

![“自定义域 HTTPS”对话框](./media/Custom_Domain_HTTPS.png)

有关将自定义域添加到 Azure Front Door 的详细说明，请参阅[将自定义域添加到 Front Door](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain)。

现在应该已经正确配置了您的 CDN，可将其用于您的 Commerce 站点。

## <a name="additional-resources"></a>其他资源

[配置域名](configure-your-domain-name.md)

[部署新的电子商务站点](deploy-ecommerce-site.md)

[创建电子商务站点](create-ecommerce-site.md)

[将在线站点与渠道关联](associate-site-online-store.md)

[管理 robots.txt 文件](manage-robots-txt-files.md)

[批量上传 URL 重定向](upload-bulk-redirects.md)

[在 Commerce 中设置 B2C 租户](set-up-B2C-tenant.md)

[设置用户登录自定义页面](custom-pages-user-logins.md)

[在 Commerce 环境中配置多个 B2C 租户](configure-multi-B2C-tenants.md)

[启用基于位置的商店检测](enable-store-detection.md)
