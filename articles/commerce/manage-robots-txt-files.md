---
title: 管理 robots.txt 文件
description: 本文介绍如何在 Microsoft Dynamics 365 Commerce 中管理 robots.txt 文件。
author: BrianShook
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4ccb09cfce00ba838cb5358afef9b7acc5c61d8d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896971"
---
# <a name="manage-robotstxt-files"></a>管理 robots.txt 文件

[!include [banner](includes/banner.md)]

本文介绍如何在 Microsoft Dynamics 365 Commerce 中管理 robots.txt 文件。

机器人排除标准或 robots.txt 是网站用于与 Web 机器人通信的标准。 它通知 Web 机器人有关网站上不应访问的区域的信息。 机器人经常被搜索引擎用来为网站建立索引。

要从服务器中排除机器人，请在服务器上创建一个文件。 在此文件中，指定机器人的访问策略。 此文件必须可以通过 HTTP 在本地 URL **/robots.txt** 访问。 robots.txt 文件可帮助搜索引擎将您站点上的内容编入索引。

Dynamics 365 Commerce 可让您为您的域上载 robots.txt 文件。 对于您的 Commerce 环境中的每个域，您可以上载一个 robots.txt 文件并将其与该域相关联。

有关 robots.txt 文件的详细信息，请访问 [Web 机器人页面](https://www.robotstxt.org/)。

## <a name="upload-a-robotstxt-file"></a>上载 robots.txt 文件

根据[机器人排除标准](https://www.robotstxt.org/orig.html)创建并编辑 robots.txt 文件后，请确保可以在要使用 Commerce 创作工具的计算机上访问该文件。 文件必须命名为 **robots.txt**。 为了获得最佳结果，必须采用标准中注明的格式。 每个 Commerce 客户负责验证和维护其 robots.txt 文件的内容。 要上载 robots.txt 文件，您必须以系统管理员身份登录到 Commerce。

要在 Commerce 中上载 robots.txt 文件，请按照下列步骤操作。

1. 以系统管理员身份登录到 Commerce。
2. 在左侧导航窗格中，选择 **租户设置**（在齿轮符号旁边）将其展开。
3. 在 **租户设置** 下，选择 **Robots.txt**。 与您的环境关联的所有域的列表将显示在窗口的主要部分。
4. 选择 **管理** 为您环境中的域上载 robots.txt 文件。
5. 在右侧菜单上，选择与 robots.txt 文件关联的域旁边的 **上载** 按钮（向上箭头）。 将出现一个文件浏览器对话框。
6. 在对话框中，浏览并选择要为关联的域上载的 robots.txt 文件，然后选择 **打开** 完成上载。

> [!NOTE] 
> 在上载期间，Commerce 会验证该文件是否是文本文件，但不会验证文件的内容。

## <a name="download-a-robotstxt-file"></a>下载 robots.txt 文件

要在 Commerce 中下载 robots.txt 文件，请按照下列步骤操作。

1. 以系统管理员身份登录到 Commerce。
2. 在左侧导航窗格中，选择 **租户设置**（在齿轮符号旁边）将其展开。
3. 在 **租户设置** 下，选择 **Robots.txt**。 与您的环境关联的所有域的列表将显示在窗口的主要部分。
4. 选择 **管理** 为您环境中的域下载 robots.txt 文件。
5. 在右侧菜单上，选择与 robots.txt 文件关联的域旁边的 **下载** 按钮（向下箭头）。 将出现一个文件浏览器对话框。
6. 在对话框中，转到本地驱动器上的所需位置，确认或输入文件名，然后选择 **保存** 完成下载。

> [!NOTE]
> 此过程只能用于下载以前通过 Commerce 创作工具上载的 robots.txt 文件。

## <a name="delete-a-robotstxt-file"></a>删除 robots.txt 文件

要在 Commerce 中删除 robots.txt 文件，请按照下列步骤操作。

1. 以系统管理员身份登录到 Commerce。
2. 在左侧导航窗格中，选择 **租户设置**（在齿轮符号旁边）将其展开。
3. 在 **租户设置** 下，选择 **Robots.txt**。 与您的环境关联的所有域的列表将显示在窗口的主要部分。
4. 选择 **管理** 为您环境中的域删除 robots.txt 文件。
5. 在右侧菜单上，选择与 robots.txt 文件关联的域旁边的 **删除** 按钮（垃圾桶符号）。 将出现一个文件浏览器窗口。
6. 在文件浏览器窗口中，浏览并选择要为域删除的 robots.txt 文件，然后选择 **打开**。 将出现警告消息框。
7. 在消息框中，选择 **删除** 确认删除 robots.txt 文件。

> [!NOTE] 
> 此过程只能用于删除以前通过 Commerce 创作工具上载的 robots.txt 文件。

## <a name="additional-resources"></a>其他资源

[配置域名](configure-your-domain-name.md)

[部署新的电子商务租户](deploy-ecommerce-site.md)

[创建电子商务站点](create-ecommerce-site.md)

[将 Dynamics 365 Commerce 站点与在线渠道相关联](associate-site-online-store.md)

[批量上传 URL 重定向](upload-bulk-redirects.md)

[在 Commerce 中设置 B2C 租户](set-up-B2C-tenant.md)

[设置用户登录自定义页面](custom-pages-user-logins.md)

[在 Commerce 环境中配置多个 B2C 租户](configure-multi-B2C-tenants.md)

[添加对内容交付网络 (CDN) 的支持](add-cdn-support.md)

[启用基于位置的商店检测](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
