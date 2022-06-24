---
title: 文本块模块
description: 本文介绍文本块模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 48714f172b12bbc10f1f682a9dec8be710748e6b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869216"
---
# <a name="text-block-module"></a>文本块模块

[!include [banner](includes/banner.md)]

本文介绍文本块模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。

文本块模块是用于添加文本内容的模块。 此内容可以是参考内容或促销内容。

文本块模块由内容管理系统 (CMS) 的数据驱动，可放到任何页面中。 它们是不依赖于页面上下文或其他任何模块的独立模块。

## <a name="examples-of-text-block-modules-in-e-commerce"></a>电子商务中的文本块模块示例

可通过以下方式使用文本块模块：

* 在产品详细信息页中展示产品特色。
* 任何页面中起到参考作用。 例如，其可介绍会员计划的优点，描述装运和退货政策，解答常见问题或提供“关于我们”内容。
* 在产品详细信息页中添加自定义消息。 （例如，“订单金额超过 50 美元免运费”）。
* 产品详细信息页、购物车页、结帐页和其他页上的免责声明和联系详细信息（例如，“装运和退货政策应遵守商店政策”）。

下图显示了主页上使用的文本块模块的示例。

![文本块模块的示例。](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a>文本块模块属性

| 属性名称     | 值                                            | 说明 |
|-------------------|--------------------------------------------------|-------------|
| 富文本         | 富文本                                        | 段落文本。 支持某些基本的富文本功能，如加粗，加下划线和斜体文本。 |
| 自定义类名称 | 级联样式表 (CSS) 类名称        | 开发人员提供的用于格式化此模块的自定义 CSS 类的名称。 类名称应在主题包中定义。 |
| 字号         | **小**、**中**、**大** 或 **特大** | 内容的字号。 |

## <a name="add-a-text-block-module-to-a-page"></a>向页面添加文本块模块

若要向新页面添加文本块模块和设置必需的属性，请执行以下步骤。

1. 转到 **模板**，选择 **新建** 创建新模板。
1. 在 **新建模板** 对话框的 **模板名称** 下，输入 **内容模板**。
1. 在 **正文** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。
1. 在 **选择模块** 对话框中，选择 **默认页面** 模块，然后选择 **确定**。
1. 选择 **保存**，选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。
1. 转到 **页面**，选择 **新建** 创建新页面。
1. 在 **创建新页面** 对话框的 **页面名称** 下，输入 **PDP 页面**，然后选择 **下一步**。
1. 在 **选择模板** 下面，选择 **内容模板**，然后选择 **下一步**。
1. 在 **选择布局** 下面，选择页面布局（例如，**灵活布局**），然后选择 **下一步**。
1. 在 **查看并完成** 下面，查看页面配置。 如果您需要编辑页面信息，请选择 **返回**。 如果页面信息正确，请选择 **创建页面**。 
1. 在新页面的 **主** 插槽，选择省略号 (**...**)，然后选择 **添加模块**。
1. 在 **选择模块** 对话框中，选择 **容器** 模块，然后选择 **确定**。
1. 在容器模块的属性窗格中，将 **宽度** 属性设置为 **填充容器**。
1. 在 **容器** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。
1. 在 **选择模块** 对话框中，选择 **文本块** 模块，然后选择 **确定**。 
1. 在文本块模块的属性窗格中，将文本添加到 **富文本** 字段中。
1. 选择 **保存**，然后选择 **预览** 以预览页面。
1. 选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。

## <a name="additional-resources"></a>其他资源

[模块库概述](starter-kit-overview.md)

[促销横幅模块](add-alert.md)

[传送模块](add-carousel.md)

[内容块模块](add-hero-module.md)

[视频播放器模块](add-video-player.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
