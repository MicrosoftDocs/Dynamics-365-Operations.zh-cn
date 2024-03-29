---
title: Dynamics 365 Commerce 中的域
description: 本文介绍如何在 Microsoft Dynamics 365 Commerce 中处理域。
author: BrianShook
ms.date: 11/08/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: BrShoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: f1a2de7984aad7d291b8a4dc68f5690d57ebe6cc
ms.sourcegitcommit: 2b654e60e2553a5835ab5790db4ccfa58828fae7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/08/2022
ms.locfileid: "9750672"
---
# <a name="domains-in-dynamics-365-commerce"></a>Dynamics 365 Commerce 中的域

[!include [banner](includes/banner.md)]

本文介绍如何在 Microsoft Dynamics 365 Commerce 中处理域。

域是用于在 Web 浏览器中导航到 Dynamics 365 Commerce 站点的 Web 地址。 请使用所选域名服务器 (DNS) 提供商管理域。 发布站点时，整个 Dynamics 365 Commerce 站点构建器中都引用域协调站点的访问方法。 本文介绍在 Commerce 站点的整个开发和启动生命周期中如何处理和引用域。

> [!NOTE]
> 自 2022 年 5 月 6 日起，在 Dynamics 365 Commerce 中创建的所有环境都将使用 `.dynamics365commerce.ms` 域进行预配，取代早期的 `.commerce.dynamics.com` 模式。 使用 `.commerce.dynamics.com` 域预配的现有环境将继续工作。

## <a name="provisioning-and-supported-host-names"></a>预配和支持的主机名

在 [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/) 中预配电子商务环境时，电子商务预配屏幕上的 **支持的主机名** 框用于输入将与部署的 Commerce 环境关联的域。 这些域将是托管电子商务网站且面向客户的域名服务器 (DNS) 名称。 在此阶段输入域不会将该域的流量转移到 Dynamics 365 Commerce。 DNS CNAME 记录更新为对 Commerce 终结点使用某个域时，将把该域的流量仅路由到该 Commerce 终结点。

> [!NOTE]
> 可以在 **支持的主机名** 框中输入多个域，并使用分号分隔。

下图显示 LCS 电子商务预配屏幕，其中突出显示了 **支持的主机名** 框。 

![LCS 电子商务预配屏幕，其中突出显示了**支持的主机名**框。](./media/Domains_ProvisioningeCommerceScreen_publish.png)

如果已进行了预配，可以创建服务请求以向环境添加更多域。 若要在 LCS 中创建服务请求，请在环境中转到 **支持 \> 支持问题**，然后选择 **提交事件**。

## <a name="commerce-generated-urls"></a>Commerce 生成的 URL

在预配 Dynamics 365 Commerce 电子商务环境时，Commerce 将生成充当环境的工作地址的 URL。 预配环境后，将在 LCS 中显示的电子商务站点链接中引用该 URL。 Commerce 生成的 URL 的格式为 `https://<e-commerce tenant name>.dynamics365commerce.ms`，其中，电子商务租户名称为在 LCS 中为 Commerce 环境输入的名称。

也可以在沙盒环境中使用生产站点主机名。 在将站点从沙盒环境复制到生产时，此选项为理想选项。

## <a name="site-setup"></a>站点设置

预配电子商务环境后，必须在 Commerce 站点构建器中设置站点，以将站点关联到工作 URL。

首次在站点构建器中设置站点时，将显示 **设置您的站点** 对话框。

下图显示在您首次在站点构建器中访问名称为“default”的站点时，该站点的 **设置您的站点** 对话框。

![**设置您的站点**对话框。](./media/Domains_SetupyoursiteScreen.png)

可在站点构建器中使用 **选择域** 框将 LCS 中为您的站点提供的一个支持的主机名关联到您的站点。

可以将 **路径** 框保留为空，也可以添加将在工作 URL 中体现的一个额外的路径字符串。 如果将 **路径** 框保留为空，将把 Commerce 生成的基 URL 与站点构建器中正在设置的站点关联。 每个站点/域对的路径必须唯一。 在所选站点和域中，环境中只有一个站点可以使用空路径或与唯一路径字符串关联。 在设置站点期间添加到 **路径** 字段的所有字符串都将成为由 Commerce 生成且用于在 Web 浏览器中访问站点的基 URL 的子集。

> [!NOTE]
> 在站点构建器的 **站点设置 \> 渠道** 配置部分中添加渠道时，此路径也称为 **匹配路径**。

例如，如果站点构建器中有一个站点在电子商务租户“xyz”中称为“fabrikam”，并且为该站点设置空路径，则可以通过在 Web 浏览器中直接转到 Commerce 生成的基 URL 来访问发布的站点内容：

`https://xyz.dynamics365commerce.ms`

或者，如果在设置同一个站点期间添加了路径“fabrikam”，则可以通过在 Web 浏览器中使用以下 URL 访问发布的站点内容：

`https://xyz.dynamics365commerce.ms/fabrikam`

## <a name="pages-and-urls"></a>页面和 URL

为站点设置路径之后，站点构建器中与页面关联的所有 URL 将基于站点的工作 URL（即 Commerce 生成的 URL，或 Commerce 生成的 URL 加路径）构建。 如果通过在 **新建 URL** 对话框中从列表选择页面并输入该页面的 URL 路径在站点构建器中创建新 URL（**URLS /> +新建**），将把该 URL 与所选页面关联。 该 URL 路径值然后将追加到站点的工作 URL 以访问该页面，并在站点构建器中 **URL** 页面的 URL 列表内标示为 `./<URL path>`。

下图显示站点构建器中的 **新建 URL** 对话框，并突出显示了一个示例 URL 路径。 

![站点构建器中的**新建 URL** 对话框。](./media/Domains_PageSetup2a.png)

下图显示站点构建器中的 **URL** 页面，并突出显示了列表中的一个示例 URL。

![策略流中的“运行用户流”选项。](./media/Domains_URLsInSiteBuilder2a.png)

## <a name="domains-in-site-builder"></a>站点构建器中的域

设置站点时，可将支持的主机名值作为域关联。 选择支持的主机名值作为域时，可以看到整个站点构建器中引用所选域。 此域仅为 Commerce 环境内的引用，尚未将该域的流量转发到 Dynamics 365 Commerce。

在站点构建器中处理站点时，如果为两个站点设置两个不同域，可以将 **?domain=** 属性追加到工作 URL 以在浏览器中访问发布的站点内容。

例如，已预配了环境“xyz”，并且已经创建了两个站点且已在站点构建器中关联：一个的域为 `www.fabrikam.com`，另一个的域为 `www.constoso.com`。 每个站点都是使用空路径设置的。 然后可以使用 **?domain=** 属性如下所示在 Web 浏览器中访问这两个站点：
- `https://xyz.dynamics365commerce.ms?domain=www.fabrikam.com`
- `https://xyz.dynamics365commerce.ms?domain=www.contoso.com`

如果在提供了多个域的环境中不指定域查询字符串，Commerce 将使用您提供的第一个域。 例如，如果路径“fabrikam”是在站点设置期间提供的第一个路径，则可以使用 URL `https://xyz.dynamics365commerce.ms` 访问为 `www.fabrikam.com` 发布的站点内容站点。

您还可以添加自定义域。 要完成此任务，在环境的项目 Commerce 管理页面上，在 **电子商务** 副标题下，选择 **+ 添加自定义域**。 滑块会显示现有自定义域并提供添加新自定义域的选项。

## <a name="update-which-commerce-scale-unit-is-used"></a>更新所使用的 Commerce Scale Unit

Commerce 使用的 Commerce Scale Unit (CSU) 通常在最初创建环境时选择。 Commerce 允许您更改您的环境使用的 CSU 实例，让您可以通过自助服务功能更好地维护您的体系结构，并减少联系客户支持的需要。 要更新 CSU 实例，转到您的环境的项目 Commerce 管理页面，然后选择 **更新缩放单元**。 使用 **新 Commerce Scale Unit** 滑块从您的环境可用的 CSU 列表中选择新的 CSU 实例。

## <a name="traffic-forwarding-in-production"></a>生产中的流量转发

可以在 commerce.dynamics.com 终结点本身使用域查询字符串参数模拟多个域。 但是如果需要投入生产，则必须将自定义域的流量转发到 `<e-commerce tenant name>.dynamics365commerce.ms` 终结点。

`<e-commerce tenant name>.dynamics365commerce.ms` 终结点不支持自定义域安全套接字层 (SSL)，因此必须使用前门服务或内容交付网络 (CDN) 设置自定义域。 

若要使用前门服务或 CDN 设置自定义域，有两个选择：

- 设置像 Azure Front Door 这样的 Front Door 服务来处理前端流量并连接到您的 Commerce 环境，从而更好地控制域和证书管理以及更精细的安全策略。

- 使用 Commerce 提供的 Azure Front Door 实例，这需要与 Dynamics 365 Commerce 团队协调操作以验证域和获取生产域的 SSL 证书。

> [!NOTE]
> 如果您使用外部 CDN 或 Front Door 服务，请确保请求以 Commerce 提供的主机名登陆 Commerce 平台，但带有 X-Forwarded-Host (XFH) 标头 \<custom-domain\>。 例如，如果您的 Commerce 终结点是 `xyz.dynamics365commerce.ms`，自定义域是 `www.fabrikam.com`，转发请求的主机头应该是 `xyz.dynamics365commerce.ms`，XFH 标头应该是 `www.fabrikam.com`。

有关如何直接设置 CDN 服务的信息，请参阅[添加对内容交付网络 (CDN) 的支持](add-cdn-support.md)。

若要使用 Commerce 提供的 Azure Front Door 实例，必须创建服务请求以获取 Commerce 入职团队的 CDN 设置协助。 

- 您将需要提供公司名称、生产域、环境 ID 和生产电子商务租户名称。 
- 您将需要确认此服务请求是针对现有域（用于当前活动站点）还是新域。 
- 如果是新域，则一个步骤即可完成域验证和 SSL 证书。 
- 如果是为现有网站提供支持的域，则需要执行多步流程来建立域验证和 SSL 证书。 此流程需要为期 7 个工作日的服务级别协议 (SLA) 以启用域，因为其中包含多个顺序步骤。

若要在 LCS 中创建服务请求，请在环境中转到 **支持 \> 支持问题**，然后选择 **提交事件**。

> [!NOTE]
> 只有生产环境中才支持采用 SSL 的自定义域。 对于沙盒和用户接受度测试 (UAT) 之类非生产环境，请在 Web 浏览器中使用 Commerce 生成的 URL 访问发布的内容。

## <a name="ssl-certificate-process"></a>SSL 证书流程

如果提交了服务请求，Commerce 团队将与您协商以下步骤。

对于新域：
- Commerce 团队将设置 Azure Front Door 实例（由 Commerce 托管）。
- 然后，Commerce 团队将提供 CNAME 记录以指向您的自定义域。
- 更新 CNAME 记录后，Commerce 托管的 Azure Front Door 实例可以验证域所有权和获取 SSL 证书。

对于现有/活动域：
- Commerce 团队将指示您添加要向您的域 DNS 提供商提供的 `afdverify.<custom-domain>` CNAME 记录。
- 完成后，Commerce 团队将把该域添加到 Azure Front Door 实例，并提供可添加到该域的 DNS 的更多 DNS TXT 记录。
- 完成后 TXT 记录之后，Commerce 团队将完成将设置 SSL 证书的域的 Azure Front Door 更新。

## <a name="apex-domains"></a>Apex 域

Commerce 提供的 Azure Front Door 实例不支持 apex 域（其中不包含子域的根域）。 Apex 域需要 IP 地址才能解析，而 Commerce Azure Front Door 实例只能采用虚拟终结点。 若要使用 apex 域，有以下选项：

- **选项 1** - 使用您的 DNS 提供程序将 apex 域重定向到“www”域。 例如，fabrikam.com 重定向到 `www.fabrikam.com`，其中，`www.fabrikam.com` 是指向 Commerce 托管的 Azure Front Door 实例的 CNAME 记录。

- **选项 2** - 如果您的 DNS 提供商支持 ALIAS 记录，您可以将 apex 域指向 Azure Front Door 终结点，从而确保反映终结点的 IP 更改。 您必须自己托管 Azure Front Door 实例。
  
- **选项 3** - 如果您的 DNS 提供商不支持 ALIAS 记录，您必须将 DNS 提供商更改为 Azure DNS，并自己托管 Azure DNS 和 Azure Front Door 实例。

> [!NOTE]
> 如果使用的是 Azure Front Door，还必须在同一订阅中设置 Azure DNS。 Azure DNS 中托管的 apex 域可作为别名记录指向您的 Azure Front Door。 这是唯一解决方案，因为 apex 域必须始终指向 IP 地址。
  
如果您对 Apex 域有任何问题，请联系 [Microsoft 支持部门](https://support.microsoft.com/)。

  ## <a name="additional-resources"></a>其他资源

  [部署新的电子商务租户](deploy-ecommerce-site.md)

  [设置在线商店渠道](./channel-setup-online.md)

  [创建电子商务站点](create-ecommerce-site.md)

  [将 Dynamics 365 Commerce 站点与在线渠道相关联](associate-site-online-store.md)

  [管理 robots.txt 文件](manage-robots-txt-files.md)

  [批量上传 URL 重定向](upload-bulk-redirects.md)

  [在 Commerce 中设置 B2C 租户](set-up-B2C-tenant.md)

  [设置用户登录自定义页面](custom-pages-user-logins.md)

  [在 Commerce 环境中配置多个 B2C 租户](configure-multi-B2C-tenants.md)

  [添加对内容交付网络 (CDN) 的支持](add-cdn-support.md)

  [启用基于位置的商店检测](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
