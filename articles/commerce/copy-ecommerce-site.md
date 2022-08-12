---
title: 复制电子商务站点
description: 本文介绍如何在 Microsoft Dynamics 365 Commerce 站点构建器中的电子商务环境内或电子商务环境之间复制现有电子商务站点。
author: psimolin
ms.date: 06/03/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: cb53a76b2ebe5b511bf5009727f20f20755e5720
ms.sourcegitcommit: 13c7a1cc4c90417e3e88db59b7d2165b3c40a56c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/04/2022
ms.locfileid: "8935736"
---
# <a name="copy-an-e-commerce-site"></a>复制电子商务站点

[!include [banner](../includes/banner.md)]

本文介绍如何在 Microsoft Dynamics 365 Commerce 站点构建器中的电子商务环境内或电子商务环境之间复制现有电子商务站点。

Dynamics 365 Commerce 支持在 Commerce 站点构建器中作为自助操作复制或克隆站点。 可以在单个电子商务环境中或在两个电子商务环境之间复制站点。 发起站点复制操作的用户必须是源电子商务环境和目标电子商务环境中的租户管理员。

站点复制操作复制源站点的所有电子商务内容。 此内容包括页面、片段、模板、URL 和资产。 新站点必须先通过首次运行体验 (FRE) 流程初始化，然后才能够使用。 渠道可以在站点构建器中在 **站点设置 \> 渠道** 进行映射和管理。

站点复制操作的持续时间主要取决于源站点上的资产数量。 对于特别大的站点，我们建议您考虑改用环境复制操作。 （此操作也称为数据便携操作）。

> [!NOTE]
> - 在站点复制操作期间，源站点为只读。
> - 只会复制已发布的文档版本。 如果未发布任何版本，将只复制最新版本。
> - 目标站点上不会提供内容的版本历史记录。

## <a name="copy-a-site-within-an-e-commerce-environment"></a>在电子商务环境中复制站点

要在电子商务环境中复制站点，请按照这些步骤操作。

1. 登录到要执行复制操作的环境的站点构建器。
1. 选择右上角的 **站点切换器**，然后选择 **管理站点**，打开站点列表视图。
1. 找到您要复制或克隆的站点，通过选中站点名称旁边的复选框选择它。
1. 在命令栏中，选择 **复制站点**。
1. 在 **复制站点** 弹出菜单的 **新建站点名称** 字段中，为新站点输入名称。 新站点名称在电子商务环境中必须是唯一的。 **源租户** 和 **源站点** 字段会自动设置为当前租户和所选站点的信息。
1. 选择 **创建副本**。

验证信息后，将有一条通知指示已创建新的站点复制作业。 您可以在 [**租户作业** 页面的右侧窗格](#monitor-the-site-copy-operation)中监视作业的进度。 复制操作成功完成后，新站点将出现在站点列表视图中的站点列表中。

下图显示站点构建器中 **复制站点** 弹出菜单的示例。

![站点构建器中的“复制站点”弹出菜单。](media/site-copy_1.png)

## <a name="copy-a-site-between-two-e-commerce-environments"></a>在两个电子商务环境之间复制站点

要在两个电子商务环境之间复制站点，请执行以下步骤。

1. 登录到目标电子商务环境的站点构建器。
1. 在命令栏中，选择 **复制站点**。
1. 在 **复制站点** 弹出菜单的 **新建站点名称** 字段中，为新站点输入名称。 新站点名称在电子商务环境中必须是唯一的。
1. 在 **源租户** 字段中，选择源租户的名称。
1. 在 **源站点** 字段中，选择源站点。
1. 选择 **创建副本**。

> [!NOTE]
> 源电子商务环境和目标电子商务环境都需要租户管理员权限。

验证信息后，将有一条通知指示已创建新的站点复制作业。 您可以在 [**租户作业** 页面的右侧窗格](#monitor-the-site-copy-operation)中监视作业的进度。 复制操作成功完成后，新站点将出现在站点列表视图中的站点列表中。

## <a name="map-channels-during-the-site-copy-operation-optional"></a>在站点复制操作期间映射渠道（可选）

源渠道和区域设置可以作为站点复制操作的一部分映射到目标渠道和区域设置。 如果渠道映射是作为站点复制操作的一部分完成的，则不需要使用 FRE 流程初始化站点，并且不需要在站点设置中配置渠道。 

要在站点构建器中“按原样”（1 比 1）映射所有渠道和区域设置，请按照这些步骤操作。

1. 选择右上角的 **站点切换器**，然后选择 **管理站点**，打开站点列表视图。
1. 找到您要复制或克隆的站点，通过选中站点名称旁边的复选框选择它。
1. 在命令栏中，选择 **复制站点**。
1. 在 **复制站点** 弹出菜单中，为 **新站点名称**、**源租户** 和 **源站点** 输入值（如果还没有）。
1. 选择 **添加渠道映射**。
1. 在 **配置站点渠道和区域设置** 弹出菜单中，选择 **源渠道**，然后选择源渠道。  
1. 选择 **目标渠道**，然后选择与源渠道相同的渠道。 
1. 选择 **添加区域设置**。
1. 选择 **源区域设置**，然后选择源区域设置。
1. 选择 **目标区域设置**，然后选择与源区域设置相同的区域设置。 
1. 对于 **URL 路径**，输入当前未在目标环境中使用的唯一 URL 路径。
1. 对要为渠道映射的每个区域设置重复步骤 8-11。
1. 选择 **应用**。
1. 对每个源渠道重复步骤 6-11。
1. 选择 **关闭**。
1. 检查配置的准确性，然后选择 **复制站点**。

> [!NOTE]
> 必须映射所有源渠道和区域设置，而且只能映射一次。

## <a name="monitor-the-site-copy-operation"></a>监视站点复制操作

要监视站点复制操作的进度，请按照这些步骤操作。

1. 登录到目标电子商务环境的站点构建器。
1. 在左侧窗格中，选择 **租户作业**。
1. 在 **租户作业** 页面上，在列表中找到并选择站点复制作业。 右侧会出现一个窗格，显示所选作业的状态和详细信息。

您可以取消状态为 **进行中** 的作业。 在列表中选择作业，然后在命令栏上选择 **取消**。

您可以重试状态为 **失败** 或 **已完成，但出现错误** 的作业。 在列表中选择作业，然后在命令栏上选择 **重试**。

> [!NOTE]
> 视频资产的处理可能会在站点复制作业完成后继续。

下图显示了站点构建器中 **租户作业** 页面右侧窗格的示例。

![站点构建器中租户作业页面右侧窗格中的作业详细信息。](media/site-copy_2.png)

## <a name="initialize-a-new-site-by-using-the-fre-process"></a>使用 FRE 流程初始化新站点

新站点必须先通过 FRE 流程初始化，然后才能够使用。

要使用 FRE 流程初始化新站点，请按照这些步骤操作。

1. 登录到新站点的站点构建器。
1. 选择右上角的 **站点切换器**，然后选择 **管理站点**，打开站点列表视图。
1. 查找并选择要初始化的新站点。
1. 在 **设置您的站点** 对话框的 **选择域** 字段中，选择一个域。 初始化期间与电子商务环境关联的所有域都可以选择。
1. 在 **选择默认渠道** 字段中，选择关联的在线商店渠道。 所选渠道将提供存储在 Commerce headquarters 的分类和其他信息。
1. 在 **选择默认语言** 字段中，选择默认创作语言。 为所选在线商店渠道配置的所有语言都可以选择。
1. 在 **路径** 字段中，值由基本域和您可以输入的可选 URL 路径组成。 如果渠道将从域根目录提供，或者您想以后在站点构建器的渠道配置视图中输入此信息，可以将 URL 路径留空。 站点路径在电子商务环境中必须是唯一的。
1. 选择 **确定**。 站点使用您提供的信息进行初始化，您将被定向到站点管理视图。

下图显示站点构建器中 **设置您的站点** 对话框的示例。

![在站点构建器中设置站点对话框。](media/site-copy_3.png)

## <a name="additional-resources"></a>其他资源

[配置域名](configure-your-domain-name.md)

[部署新的电子商务租户](deploy-ecommerce-site.md)

[将 Dynamics 365 Commerce 站点与在线渠道相关联](associate-site-online-store.md)

[管理 robots.txt 文件](manage-robots-txt-files.md)

[批量上传 URL 重定向](upload-bulk-redirects.md)

[在 Commerce 中设置 B2C 租户](set-up-b2c-tenant.md)

[设置用户登录自定义页面](custom-pages-user-logins.md)

[在 Commerce 环境中配置多个 B2C 租户](configure-multi-b2c-tenants.md)

[添加对内容交付网络 (CDN) 的支持](add-cdn-support.md)

[启用基于位置的商店检测](enable-store-detection.md)