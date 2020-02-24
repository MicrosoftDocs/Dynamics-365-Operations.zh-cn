---
title: 启用基于位置的商店检测
description: 此主题介绍如何为 Dynamics 365 Commerce 站点开启基于位置的商店检测。
author: brianshook
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: 304d8d2f05916295b9c6320561d6a25ff40df955
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003084"
---
# <a name="enable-location-based-store-detection"></a>启用基于位置的商店检测


[!include [banner](includes/banner.md)]

此主题介绍如何为 Dynamics 365 Commerce 站点开启基于位置的商店检测。

## <a name="overview"></a>概览

可通过 Commerce 中基于位置的商店检测基于客户的位置向客户提供相关站点内容。 开启基于位置的商店检测之后，Commerce 呈现服务使用客户 Web 浏览器 IP 地址的国家/区域信息将客户重定向到可用的最佳地理站点配置。

## <a name="privacy-notice"></a>隐私声明

如果开启基于位置的商店检测功能，将把客户浏览器的信息发送到 Microsoft 位置服务。 然后使用此信息提供与其位置有关的客户内容。 从客户浏览器发送的信息和返回给客户的基于位置的信息应遵守隐私和 cookie 合规性政策。

## <a name="turn-on-location-based-store-detection"></a>开启基于位置的商店检测

若要在 Commerce 中开启基于位置的商店检测，请执行以下步骤。

1. 在创作工具中，转到您的站点。
1. 在左侧的导航窗格中，选择**站点管理**。
1. 选择**站点设置**。
1. 将**启用基于位置的商店检测**选项设置为**开**。

## <a name="additional-resources"></a>其他资源

[配置域名](configure-your-domain-name.md)

[部署新的电子商务站点](deploy-ecommerce-site.md)

[创建电子商务站点](create-ecommerce-site.md)

[将在线站点与渠道关联](associate-site-online-store.md)

[管理 robots.txt 文件](manage-robots-txt-files.md)

[设置用户登录自定义页面](custom-pages-user-logins.md)

[添加对内容交付网络 (CDN) 的支持](add-cdn-support.md)
