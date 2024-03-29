---
title: 创建电子商务站点
description: 本文介绍在 Dynamics 365 Commerce 站点构建器中创建新电子商务站点所需的步骤和信息。
author: bicyclingfool
ms.date: 03/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: ea9afd89ce9ff79edbe5bff609b9843026005493
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270229"
---
# <a name="create-an-e-commerce-site"></a>创建电子商务站点

[!include [banner](includes/banner.md)]

本文介绍在 Dynamics 365 Commerce 站点构建器中创建新电子商务站点所需的步骤和信息。

在许可 Dynamics 365 Commerce 功能时，将为站点构建器预配可用作您自己站点的基础的入门站点。 但是，如果要从头开始或要建立第二个站点，则需要在站点创作环境中建立一个新站点。 

## <a name="site-creation-prerequisites"></a>站点创建先决条件

站点构建器用户必须具有 Microsoft Azure Active Directory (Azure AD) 用户帐户，该帐户包含在为电子商务系统管理员分配的 Azure AD 安全组中。 有关详细信息，请参阅[部署新的电子商务租户](deploy-ecommerce-site.md)。

> [!NOTE]
> Azure AD 来宾用户在您的 Azure AD 租户中可能具有不同的访问权限。 即使包含在为电子商务系统管理员分配的 Azure AD 安全组中，来宾用户也可能需要调整 Azure AD **外部用户** 权限设置才能在 Commerce 中创建电子商务站点。 

要调整 Azure AD **外部用户** 设置，请按照这些步骤操作。

1. 在 Azure 门户中，导航到您的 Azure AD 租户。
1. 转到 **用户设置 \> 外部用户**，选择 **管理外部协作设置** 链接。 这将打开 **外部协作设置** 页面，可以在其中设置来宾用户访问、来宾邀请设置和协作限制。 
1. 根据您的公司的安全策略调整外部协作设置。 

## <a name="set-up-your-site"></a>设置站点

若要设置站点，请执行以下操作。

1. 打开站点构建器环境。 您可以在 Commerce 环境功能页面内的 Microsoft Lifecycle Services (LCS) 中查找指向站点构建器的链接。
1. 在站点创作环境的主页中，选择 **新建站点**。
1. 在 **新站点** 对话框中，提供以下信息。

| 字段                               | 说明 |
|-------------------------------------|-------------|
| 站点名称                           | 输入应该在站点创作环境中用于站点的显示名称。 此名称仅在创作环境中显示，不对客户显示。 |
| 站点管理员的安全组 | 指定用于管理在此站点中具有站点管理员角色的用户的 Microsoft Azure Active Directory (Azure AD) 安全组。 |
| 默认渠道(运营单位编号) | 选择此站点将充当其 Web 店面的在线商店。 如果您希望电子商务站点支持多个在线商店，必须在设置站点后在 **站点设置** 中将商店与站点关联。 |
| 默认语言                            | 指定此在线商店和市场的默认语言。 在线商店可支持多种语言。 如果希望此在线商店或其他在线商店支持多种语言，可在设置站点后在 **站点设置** 中配置此项支持。  |
| 域                              | 选择将充当此在线商店的域的域名。 如果尚未在 LCS 中配置任何域，可将此字段保留为空。 在 LCS 中配置域之后，必须在 **站点设置** 中将其添加到您的在线商店。  |
| 路径                              | 如果您的站点支持对给定域名使用多种语言，请使用路径字段为该域和语言的组合创建唯一站点。 如果在 **默认语言** 中指定的语言是此域将支持的唯一语言，或将在将站点本地化为更多语言后继续充当默认语言，建议您将此字段保留为空。 |

创建站点之后，可通过选择 **产品** 选项卡将其与在线商店关联。应该可以查看已经分配给在线商店的产品的分类。 还可以使用页面左上角的下拉菜单按类别访问分配的产品。

## <a name="rename-your-site"></a>重命名您的站点

要在站点构建器中重命名您的站点，请按照以下步骤操作。

1. 要打开站点列表视图，在右上角选择 **站点切换器**，然后选择 **管理站点**。 
1. 选中要重命名的站点旁边的复选框，然后在命令栏上选择 **重命名**。
1. 在 **新建站点名称** 对话框中，输入新站点名称，然后选择 **确定**。 站点列表将更新，显示站点的新名称。

## <a name="delete-a-site"></a>删除站点

要在站点生成器中删除站点，请执行以下步骤。

1. 要打开站点列表视图，在右上角选择 **站点切换器**，然后选择 **管理站点**。
1. 选择要删除的站点，然后在命令栏上选择 **删除**。
1. 在 **删除 \<site name\>** 对话框中，输入站点名称，然后选择 **删除**。

## <a name="additional-resources"></a>其他资源

[配置域名](configure-your-domain-name.md)

[部署新的电子商务租户](deploy-ecommerce-site.md)

[将 Dynamics 365 Commerce 站点与在线渠道相关联](associate-site-online-store.md)

[管理 robots.txt 文件](manage-robots-txt-files.md)

[批量上传 URL 重定向](upload-bulk-redirects.md)

[在 Commerce 中设置 B2C 租户](set-up-B2C-tenant.md)

[设置用户登录自定义页面](custom-pages-user-logins.md)

[在 Commerce 环境中配置多个 B2C 租户](configure-multi-B2C-tenants.md)

[添加对内容交付网络 (CDN) 的支持](add-cdn-support.md)

[启用基于位置的商店检测](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
