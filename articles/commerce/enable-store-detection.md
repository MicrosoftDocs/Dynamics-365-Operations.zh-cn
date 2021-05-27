---
title: 启用基于位置的商店检测
description: 此主题介绍如何为 Dynamics 365 Commerce 站点开启基于位置的商店检测。
author: brianshook
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3e26c3130914ebef5a63b79c477d7d5846fd5b71
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6027592"
---
# <a name="enable-location-based-store-detection"></a>启用基于位置的商店检测

[!include [banner](includes/banner.md)]

此主题介绍如何为 Dynamics 365 Commerce 站点开启基于位置的商店检测。

可通过 Commerce 中基于位置的商店检测基于客户的位置向客户提供相关站点内容。 开启基于位置的商店检测之后，Commerce 呈现服务使用客户 Web 浏览器 IP 地址的国家/区域信息将客户重定向到可用的最佳地理站点配置。

## <a name="privacy-notice"></a>隐私声明

如果开启基于位置的商店检测功能，将把客户浏览器的信息发送到 Microsoft 位置服务。 然后使用此信息提供与客户位置有关的客户内容。 从客户浏览器发送的信息和返回给客户的基于位置的信息应遵守隐私和 cookie 合规性政策。

## <a name="turn-on-location-based-store-detection"></a>开启基于位置的商店检测

若要在 Commerce 中开启基于位置的商店检测，请执行以下步骤。

1. 在创作工具中，转到您的站点。
1. 在左侧的导航窗格中，选择 **站点管理**。
1. 选择 **站点设置**。
1. 将 **启用基于位置的商店检测** 选项设置为 **开**。

## <a name="additional-resources"></a>其他资源

[配置域名](configure-your-domain-name.md)

[部署新的电子商务租户](deploy-ecommerce-site.md)

[创建电子商务站点](create-ecommerce-site.md)

[将 Dynamics 365 Commerce 站点与在线渠道相关联](associate-site-online-store.md)

[管理 robots.txt 文件](manage-robots-txt-files.md)

[批量上传 URL 重定向](upload-bulk-redirects.md)

[在 Commerce 中设置 B2C 租户](set-up-B2C-tenant.md)

[设置用户登录自定义页面](custom-pages-user-logins.md)

[在 Commerce 环境中配置多个 B2C 租户](configure-multi-B2C-tenants.md)

[添加对内容交付网络 (CDN) 的支持](add-cdn-support.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
