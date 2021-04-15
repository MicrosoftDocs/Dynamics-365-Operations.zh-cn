---
title: 配置域名
description: 此主题介绍如何为 Microsoft Dynamics 365 电子商务站点配置域名。
author: psimolin
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3d41168da44100a09c58b8c05367ab45bbd62a30
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796043"
---
# <a name="configure-your-domain-name"></a>配置域名


[!include [banner](includes/banner.md)]

此主题介绍如何为 Microsoft Dynamics 365 电子商务站点配置域名。 

## <a name="add-domains-during-e-commerce-initialization"></a>在电子商务初始化期间添加域

若要将域与 Dynamics 365 Commerce 电子商务环境关联，请按照[部署新电子商务租户](deploy-ecommerce-site.md)中的说明初始化电子商务。 在初始化期间，系统将要求您提供将用于预配电子商务环境的信息。 在 **支持的主机名** 字段中，添加计划用于此环境的所有域。 应该使用分号分隔多个域。 这样，将在所有必需电子商务组件中配置域，并且在您从内容交付网络 (CDN) 或 Web 服务器切换流量并将其指向电子商务前端时，可以使用这些域。

## <a name="add-domains-after-e-commerce-initialization"></a>在电子商务初始化后添加域

若要在电子商务初始化之后将新域与电子商务环境关联，您必须提交服务请求。

## <a name="additional-resources"></a>其他资源

[部署新的电子商务租户](deploy-ecommerce-site.md)

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