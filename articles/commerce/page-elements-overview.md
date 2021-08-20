---
title: 页面模型词汇表
description: 此主题介绍 Microsoft Dynamics 365 Commerce 站点页面中使用的各种元素。
author: phinneyridge
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: intro-internal
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c5ec6dfd9147fd5e054303b4fd612caef78b7467d7f6f4850e46fcc9fb1346f2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758304"
---
# <a name="page-model-glossary"></a>页面模型词汇表


[!include [banner](includes/banner.md)]

此主题介绍 Microsoft Dynamics 365 Commerce 站点页面中使用的各种元素。

## <a name="page-element-definitions"></a>页面元素定义

下表提供更改站点的外观和内容时应该熟悉的术语的汇总。 有关更透彻的说明和过程，请单击链接。

| 术语 | 描述和注释 |
|------|-----------------------|
| [模块](work-with-modules.md) | <p>**定义**：模块是可制作并构成网页主干的构建基块。 例如，页眉、主图和传送模块。</p><p>**选择位置：** 可在站点创作工作流的各阶段（如模板、布局、页眉和片段创作阶段）选择和配置部署的模块。</p><p>**编辑位置：** 自定义模块使用软件开发工具包 (SDK) 以代码的形式创建。 然后上传到您的站点中，在站点中可供选择。</p> |
| 模块属性 | <p>**定义：** 模块属性是模块定义的特定设置。 可以在电子商务制作工具中编辑。 例如，模块属性用于设置横幅模块的标题和背景图像。</p><p>**配置位置：** 模块属性在模板、布局、页面、片段和应用设置的创作环境（编辑器）中显示的属性窗格内选择和配置。</p> |
| [模板](templates-layouts-overview.md) | <p>**定义：** 模板定义应该用于页面类别（如市场营销页、类别页和产品页）的模块组合和选项。</p><p>**选择位置：** 可以在页面或布局创建工作流期间选择模板。</p><p>**编辑位置：** 模板在模板编辑器中制作。 无需代码即可创建或修改模板。</p> |
| [布局](templates-layouts-overview.md) | <p>**定义：** 布局定义父模板的选项集中的模板的最终选择和安排。 可以为单页配置布局（*自定义布局*），也可以多页共享布局（*预设布局*）。</p><p>**选择位置：** 可以在创建新页期间或现有页需要其他布局时选择布局。</p><p>**编辑位置：** 布局在布局编辑器中制作。 无需代码即可创建或修改模板。</p> |
| [页面实例](modify-existing-page.md) | <p>**定义：** 页面实例定义单页的页面特定的最终已本地化内容。 此内容派生自模块属性的值。</p><p>**选择位置：** 页面是在分配 URL 时选择的。</p><p>**编辑位置：** 页面在页面编辑器中编辑。 无需代码即可创建或修改模板。</p> |
| [主题](select-site-theme.md) | <p>**定义：** 主题定义级联样式表 (CSS)，并确定模块在页面中显示时的外观。</p><p>**选择位置：** 使用 Microsoft Dynamics Lifecycle Services (LCS) 将主题上传到您的站点后，可作为页面容器模块的属性选择该主题。</p><p>**编辑位置：** 主题现在使用 SDK 创建和编辑。 然后使用 LCS 上传到您的站点。</p> |
| [片段](work-with-fragments.md) | <p>**定义：** 片段是已本地化了可在多页中重复使用并集中更新的内容的完全配置的模块。 例如，通过页眉模块创建的片段可在您的站点的所有模板中和所有页面中使用，并在一处集中更新。</p><p>**选择位置：** 可在可选择模块的任何位置选择片段。 可用于替代模块来通过可重复使用的集中创作帮助提高效率。</p><p>**编辑位置：** 片段在片段编辑器中编辑。 无需代码即可创建或修改模板。</p> |
| [URL](create-page-URL.md) | <p>**定义：** 统一资源定位器 (URL) 是指向网页或其他 URL 的地址。</p><p>**选择位置：** URL 是在页面之间需要链接的位置选择的。</p><p>**编辑位置：** URL 在 URL 编辑器中编辑。 无需代码即可创建或修改模板。</p> |
| 资产 | <p>**定义：** 资产是扩展名为 .jpg、.docx、.pdf 或 .mpg 的二进制文件。</p><p>**选择位置：** 资产作为需要资产的模块的模块属性选择。</p><p>**编辑位置：** 在资产管理器中上传资产和编辑关联的元数据。</p> |

## <a name="additional-resources"></a>其他资源

[添加内容的方法](add-manage-content.md)

[文档状态和生命周期](document-states-overview.md)

[使用发布组](publish-groups.md)

[启用和使用跨渠道共享](cross-channel-sharing.md)

[使用模块](work-with-modules.md)

[使用片段](work-with-fragments.md)

[模板和布局概览](templates-layouts-overview.md)

[自定义站点导航](customize-site-navigation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]