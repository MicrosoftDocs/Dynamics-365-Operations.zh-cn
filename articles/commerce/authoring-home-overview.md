---
title: 创作页面概览
description: 本文提供 Microsoft Dynamics 365 Commerce 中的创作页面的概述。
author: brendans
ms.date: 10/31/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application USer
ms.reviewer: v-chgri
ms.assetid: ''
ms.search.region: Global
ms.author: brendans
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: bc8cdbc0a521f3aa444a3af0d0230f8567729694
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854996"
---
# <a name="authoring-page-overview"></a>创作页面概览

  
 [!include [banner](includes/banner.md)]

本文提供 Microsoft Dynamics 365 Commerce 中的创作页面的概述。

可创建网站以支持各种业务需要。 它们可表示整体业务，提供单一业务渠道，或将特定对象或对象细分设置为目标。 例如，一家服装厂可能有一个网站用于展示其拥有的所有品牌。 然后，同一个服装厂的这些品牌每个有一个单独的网站，还有一系列网站专门介绍奢侈品、户外服装和童装。

Dynamics 365 Commerce 支持创建和管理多个网站，每个网站可以有自己的外观和内容。 创作页面充当这些网站的公共接入点。 可将其用于登录和注销系统，或创建新网站。

现在，创作页面由以下部分组成。

- **上栏** – 上栏在创作页面顶部显示。 它可用于轻松访问电子商务工具、通知、支持链接和用户登录。
- **命令栏** – 命令栏在上栏下方显示。 它可用于新建网站。
- –**站点列表** – 站点列表占据命令栏下方的所有空间。 它提供丰富的网站及与其关联的域的列表。

下图显示创作页面。

![Dynamics 365 Commerce 创作页面。](../commerce/media/authoring_tools_01.png)

## <a name="use-the-home-button-to-select-a-tool"></a>使用“主页”按钮选择工具

**主页** 按钮位于创作页面左上角。 它可用于轻松访问其他电子商务工具。 如果选择此按钮，将打开可使用的工具的菜单。 如果选择一个工具，将关闭此菜单，并且在浏览器中加载所选工具。

## <a name="view-and-clear-notifications"></a>查看和清除通知

**通知** 按钮是创作页面右上角的一个按钮。 看起来是一个钟。 可通过选择此按钮查看已发给您的所有通知。

创作工具中使用通知通知您已完成了操作。 例如，通知的内容为“已发布了您的页面”，以便通知您发布操作已成功。

通知也可以告知您执行操作时遇到了错误。 选择错误通知打开其消息。 此消息中的信息可帮助您解决错误。

可通过选择通知消息底部的 **删除** 清除通知菜单中的通知。 若要批量清除通知，请选择通知菜单底部的 **全部删除**。

## <a name="get-help-with-the-authoring-tool"></a>获取有关创作工具的帮助

**帮助** 按钮是创作页面右上角的另一个按钮。 它看起来象一个问号。 如果选择此按钮，将打开以下预定义选项的菜单：

- **站点开发帮助** – 如果选择此选项，将在新的浏览器标签页中打开有关创建新网站的文档。
- **反馈和支持** – 选择此选项将打开 Microsoft Yammer 渠道，可在其中留下有关创作工具的反馈或请求支持。
- **隐私和 cookies** – 如果选择此选项，将在新浏览器标签页中打开 Microsoft 隐私声明。
- **关于** – 选择此选项将打开一个消息框，其中包含有关您正在使用的创作工具和版本的信息。

## <a name="sign-in-to-and-out-of-the-authoring-tool"></a>登录和注销创作工具

**我的帐户** 按钮是创作页面右上角的另一个按钮。 它看起来象一个彩色圆环。 通过选择此按钮，可查看使用了哪个帐户登录，也可以根据需要注销该帐户。

若要登录或注销创作工具，请执行以下步骤之一。

- 如果尚未登录创作工具，请选择 **我的帐户** \> **登录** 以登录。
- 如果已经登录，但是希望注销，请选择 **我的帐户** \> **注销**。

## <a name="change-the-display-language-of-the-authoring-tool"></a>更改创作工具的显示语言

也可以使用 **我的帐户** 按钮更改创作工具中显示的文本字符串的语言。

若要更改显示语言，请执行以下步骤。

1. 选择 **我的帐户** \> **更改语言**。 对话框出现
1. 选择一种用户语言，然后选择 **保存**。

## <a name="create-a-new-website"></a>创建新网站

Dynamics 365 Commerce 支持创建和管理多个网站，每个网站可以有自己的外观和内容。

若要创建新网站，请执行以下步骤。

1. 在命令栏中，选择 **新建网站**。 对话框出现
2. 输入新网站的以下必需信息：

    - **站点名称** – 输入网站的名称。 此名称不对网站客户显示。 而是在站点列表和创作工具中的其他位置使用。
    - **站点管理安全组** – 输入其中包含应该具有网站的管理访问权限的用户的 Microsoft Azure Active Directory (Azure AD) 安全组的全名。 可以在创建网站之后更改网站的管理组名称和网站的其他权限。
    - **默认渠道** – 输入应该与网站关联的默认促销渠道。 默认渠道决定可通过网站出售的产品。
    - **默认语言** – 指定默认渠道之后，选择渠道的默认语言。 默认渠道定义客户不指定首选语言时用于显示产品的语言。
    - **默认市场** – 输入网站的默认市场。 默认市场定义当客户不指定首选市场时显示的市场。
    - **域** – 选择应该与网站关联的 Web 域。 此域是网站将在其浏览器中转到的域。

1. 选择 **确定**。 此时会创建新网站。

> [!NOTE]
> 创建新网站最多可能需要 60 秒钟。 完成此过程之后，将在通知区域显示通知。 此外，此网站也会显示在站点列表中，并且采用您输入的站点名称。

## <a name="select-a-website-to-author"></a>选择要创作的网站

站点列表提供与电子商务系统关联的丰富网站的列表。 将按字母顺序显示网站。 还将显示与每个网站关联的域。 若要查看网站的内容和开始创作页面，请选择网站的名称。 将加载网站的创作工具和内容。

加载创作工具之后，可选择 **主页** 回到创作页面。

## <a name="additional-resources"></a>其他资源

[管理电子商务用户和角色](manage-ecommerce-users-roles.md)

[站点的搜索引擎优化 (SEO) 注意事项](search-engine-optimization-considerations.md)

[管理内容安全策略 (CSP)](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
