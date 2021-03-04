---
title: 社交共享模块
description: 此主题介绍社交共享模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 82a8795360f453cdee19fa6e9e376a42e8276849
ms.sourcegitcommit: 510ca8b14d8b5334e50aca1b15d636c65fcc9888
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4410616"
---
# <a name="social-share-module"></a>社交共享模块

[!include [banner](includes/banner.md)]

此主题介绍社交共享模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。

## <a name="overview"></a>概览

用户可通过社交共享模块在 Facebook、Twitter、Pinterest 和 LinkedIn 之类社交媒体上共享电子商务站点页面 URL。  也可以通过电子邮件共享站点页面 URL。 社交共享模块通常在产品详细信息页 (PDP) 上用于帮助用户共享产品信息。

每个社交共享模块都是一个社交共享项模块容器。 每个社交共享项模块配置为指向特定社交媒体站点。 自带支持集成 Facebook、Twitter、Pinterest、LinkedIn 和电子邮件。 当站点用户选择社交媒体符号时，将为相应的社交媒体站点启动 HTML iframe。 在该 iframe 中，用户可以登录和发布自己正在查看的页面内容。

每个社交媒体平台都可能跟踪 cookie，因此此模块需要用户接受 cookie 同意通知消息。 如果不接受 cookie 同意，页面中将隐藏此模块。 有关详细信息，请参阅 [Cookie 合规性](cookie-compliance.md)。

下图突出显示产品详细信息页中使用的社交共享模块的示例。

![社交共享模块的示例](./media/ecommerce-socialshare.png)

## <a name="social-share-module-properties"></a>社交共享模块属性

| 属性名称             | 值                 | 说明 |
|---------------------------|-----------------------|-------------|
| 标题                  | 文本 | 此属性指定模块的标题。 |
| 方向 | **水平** 或 **垂直**  | 此属性定义社交共享项的布局属性。 |

## <a name="social-share-item-module-properties"></a>社交共享项模块属性
| 属性名称             | 值                 | 说明 |
|---------------------------|-----------------------|-------------|
| 社交媒体              | **Facebook**、**Twitter**、**Pinterest**、**LinkedIn**、**Mail** | 一个带有社交媒体平台列表的下拉菜单。 |
| 图标 |头像    | 这将是将对相应社交媒体显示的图像。 最佳实践是参阅社交媒体平台的 SDK 以获取各平台推荐各平台使用的图像。 |

## <a name="add-a-social-share-module-to-a-buy-box-module"></a>向购买框模块添加社交共享模块

若要向购买框模块添加社交共享模块，请执行以下步骤。

1. 在 Fabrikam 站点中，选择 **页面**，然后选择 **DefaultPDP** 页面打开产品详细信息页。 
1. 在 **购买框(必填)** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。
1. 在 **添加模块** 对话框中，选择 **社交共享** 模块，然后选择 **确定**。
1. 在 **社交共享** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。
1. 在 **添加模块** 对话框中，选择 **SocialShare** 模块，然后选择 **确定**。
1. 在 **SocialShare** 模块属性窗格中 **方向** 下，选择 **水平**。 根据需要添加标题。
1. 在 **SocialShare** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。
1. 在 **添加模块** 对话框中，选择 **SocialShareItem** 模块，然后选择 **确定**。
1. 在 **SocialShareItem** 模块属性窗格中的 **社交媒体** 下，选择 **Facebook**。
1. 在 **SocialShareItem** 模块属性窗格中的 **图标** 下，选择 **+ 添加图像**。
1. 在 **媒体选择器** 对话框中，选择 Facebook 徽标图像，然后选择 **确定**。 如果无 Facebook 徽标图像，请选择 **上载新媒体项** 上载一个。
1. 根据需要添加和配置更多 **SocialShareItem** 模块。
1. 选择 **保存**，然后选择 **预览** 以预览页面。 该页面将显示社交共享模块。
1. 选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。

## <a name="additional-resources"></a>其他资源

[模块库概述](starter-kit-overview.md)

[购买框模块](add-buy-box.md)

[Cookie 合规性](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]