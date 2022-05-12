---
title: Dynamics 365 Commerce 电子商务本地化指南
description: 本主题介绍如何将 Microsoft Dynamics 365 Commerce 电子商务站点本地化为其他语言并将该站点配置为支持多个渠道。
author: bicyclingfool
ms.date: 04/29/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 1e9d91036ceeb9161dc8ee903532b2cf3ca435e2
ms.sourcegitcommit: 26c726bd0b00935e3d2c31fdc5a3b2ae03a8a2b0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/30/2022
ms.locfileid: "8661520"
---
# <a name="dynamics-365-commerce-e-commerce-localization-guide"></a>Dynamics 365 Commerce 电子商务本地化指南

[!include [banner](includes/banner.md)]

本主题介绍如何将 Microsoft Dynamics 365 Commerce 电子商务站点本地化为其他语言并将该站点配置为支持多个渠道，还介绍了与流程相关的概念和术语。

Dynamics 365 Commerce 中的电子商务功能旨在实现可针对特定国家/地区和语言定制的在线体验，但同时允许最大限度地重复使用模板、页面、内容和媒体。 您还可以创建一个基本站点，然后通过添加对其他国家/地区和语言的支持来扩展到新市场。

## <a name="definitions"></a>定义

**区域设置、区域设置标识符**：区域设置（也称为区域设置标识符）定义与国家/地区或区域关联的语言。 例如，区域设置标识符“fr-ca”与加拿大法语关联。

**基本语言**：导出站点内容以进行本地化之前开发站点内容所用的语言。

**渠道、在线商店**：渠道（也称为在线商店）定义在线电子商务店面的付款方式、价格组、产品层次结构、分类和产品。

## <a name="concepts"></a>概念

### <a name="url-driven-experience"></a>URL 驱动型体验

Dynamics 365 Commerce 电子商务站点通过渠道和区域设置标识符为客户提供唯一的市场化和本地化体验。 渠道定义了市场的独特产品、类别、货币和支付方式，区域设置标识符决定了客户查看内容所用的语言。 电子商务站点使用 URL 来区分市场化体验和本地化体验。 这些独特的渠道和区域设置体验的站点 URL 是在 Dynamics 365 Commerce 站点生成器中的 **站点设置 \> 渠道** 页面上为站点定义的 URL。

在站点生成器中，URL 是域和路径的组合，用于定义渠道和区域设置的唯一组合的入口点。 在以下示例中，名为 Fabrikam Inc. 的虚构在线商店定义了渠道和区域设置的四种唯一组合，并将每种组合映射到向客户提供内容的唯一 URL。

| 域                     |  路径      | 渠道       |   区域设置     |
|------------------------|--------|--------------------------------|--------|
| `https://fabrikam.com` | /      | Fabrikam 扩展在线商店 | zh-Hans  |
| `https://fabrikam.com` | /es    | Fabrikam 扩展在线商店 | es     |
| `https://fabrikam.ca`  | /      | Contoso 在线商店    | fr-ca  |
| `https://fabrikam.ca`  | /en-ca | Contoso 在线商店    | en-ca  |

#### <a name="domain"></a>域

当您在 Microsoft Dynamics Lifecycle Services (LCS) 中设置您的电子商务站点时，就会建立域。 预配您的电子商务环境后，您可以通过打开服务请求来添加更多域。 有关如何为您的电子商务站点设置域的详细信息，请参阅 [Dynamics 365 Commerce 中的域](domains-commerce.md)。

#### <a name="path"></a>路径

- 路径是一个任意字符串，它与域一起映射到渠道和区域设置的唯一组合。 在前面的示例中，用作路径的字符串与路径映射到的区域设置标识符匹配。 但是，您可以使用其他方法。
- 渠道和区域设置的组合可以映射到域和空路径 ("/")。 在前面的示例中，访问 `https://fabrikam.ca/` 的客户将以加拿大法语形式获得适用于加拿大市场的产品和分类。
- Commerce 站点生成器可防止您创建域和路径的重复组合。 但是，您可以将渠道和区域设置的重复组合映射到域和路径的其他组合。

#### <a name="channel"></a>渠道

- 渠道（也称为在线商店）定义在线电子商务店面的付款方式、价格组、产品层次结构、分类和产品。
- 渠道是在 Dynamics 365 Commerce Headquarters 中定义、配置和发布的。
- 站点生成器可以检测已在 Commerce Headquarters 配置并可映射到站点的在线商店。

有关渠道的详细信息，请参阅[渠道概览](channels-overview.md)。 有关如何设置在线渠道的详细信息，请参阅[设置在线渠道](channel-setup-online.md)。

#### <a name="locale"></a>区域设置

- 区域设置是在您移交 XML 本地化交换文件格式 (XLIFF) 文件以进行本地化时使用的实际标识符。 为 Commerce Headquarters 中的每个渠道定义和发布了区域设置。 有关如何在站点生成器中配置语言和渠道的信息，请参阅下一节。
- 相同的区域设置可以映射到多个渠道。 这样，可以跨多个市场提供通用语言。

## <a name="configure-languages-and-channels-for-your-e-commerce-site"></a>为您的电子商务站点配置语言和渠道

无论您是从 Fabrikam 演示站点开始还是从头开始创建新站点，所有现成的 Dynamics 365 Commerce 电子商务站点都已配置为使用单一在线渠道和单一语言。

在此配置中，客户和合作伙伴通常会开发将跨国家/地区和跨语言使用的所有资产。 这些资产包括模板、页面、片段、内容和媒体。 所有站点内容均以您为站点选择的第一种语言开发，或者如果您使用 Fabrikam 演示站点，则将以英语开发站点内容。

![现成的 Dynamics 365 Commerce 电子商务站点](media/loc-guide-1.png)

> [!NOTE]
> 您可以为 Fabrikam 演示站点配置其他语言，以便可以使用该语言完成内容开发。 有关如何向站点和渠道添加新语言的信息，请参阅本主题后面的[为您的站点配置其他语言](#configure-an-additional-language-for-your-site)部分。

但是，Dynamics 365 Commerce 电子商务站点的内容管理系统 (CMS) 和页面模型旨在实现向新市场和区域扩展。 因此，通过单个电子商务站点，您可以管理跨多个市场和语言的在线商店的资产。

![跨越多个市场和语言的 Dynamics 365 Commerce 电子商务站点](media/loc-guide-2.png)

### <a name="configure-an-additional-language-for-your-site"></a>为您的站点配置其他语言

为电子商务站点配置新语言的过程包括三个步骤。

#### <a name="step-1-add-the-language-to-your-channel-online-store-in-commerce-headquarters"></a>第 1 步：将语言添加到 Commerce Headquarters 中的渠道（在线商店）

1. 在 Commerce Headquarters 中，转到要将新语言添加到的渠道。 要查找您在 Commerce Headquarters 配置的渠道列表，请转到 **Retail 和 Commerce \> 渠道 \> 在线商店**。
1. 通过选择其 **零售渠道 ID** 值来打开映射到站点的在线商店。 您可以通过在 Commerce 站点生成器中打开 **渠道** 站点设置页面并查看 **渠道** 列中的在线商店名称，来验证映射到您的站点的在线商店。 
1. 在 **语言** 快速选项卡上，选择 **添加**。 在 **语言** 字段中，选择新语言的区域设置代码。 然后选择 **保存**。
1. 转到 **Retail 和 Commerce \> Retail 和 Commerce IT \> 配送计划**，运行作业 **1070 渠道配置**。 在作业运行完后，您可以继续执行第 2 步并将语言添加到站点生成器中的站点渠道。

![Commerce Headquarters 中在线商店的语言快速选项卡](media/loc-guide-3.png)

#### <a name="step-2-add-the-language-to-a-channel-in-site-builder"></a>第 2 步：在站点生成器中将语言添加到渠道

要在站点生成器中将语言添加到渠道，请按照下列步骤操作。

1. 在 Commerce 站点生成器中，打开您的站点，然后在站点设置中打开 **渠道** 页面。
1. 选择要将语言添加到的通道的名称。
1. 从右窗格中，选择 **添加区域设置**。
1. 在 **添加区域设置** 对话框中，在 **添加区域设置** 下面，为之前添加到 Commerce Headquarters 渠道的语言选择区域设置。
1. 选择客户请求的域和路径以该渠道和语言查看您的站点。
1. 如果您希望语言是用于查看、创建和更新站点生成器页面和片段的默认语言，请选中 **用作默认创作渠道语言** 复选框。 
    > [!NOTE]
    > 此设置仅影响站点生成器。 这不会影响客户的已发布站点体验。
1. 选择 **确定**。
1. 选择 **保存并发布**。

#### <a name="step-3-localize-your-site-content"></a>第 3 步：本地化站点内容

当您返回 Commerce 站点生成器中的 **页面** 视图时，新语言将在右上角的渠道和区域设置选择器中可用。 您现在可以使用您的基本语言创建页面的本地化版本。

本主题后面的[本地化电子商务站点内容](#localize-e-commerce-site-content)部分介绍了本地化页面和片段内容的流程。

### <a name="configure-a-new-channel-for-your-site"></a>为您的站点配置新渠道

Dynamics 365 Commerce 电子商务站点可以提供在 Commerce Headquarters 中配置的多个在线渠道中定义的体验。 站点使用多种渠道向客户显示付款方式、价格组、产品层次结构、分类和一组产品的独特配置。 渠道通常用于配置这些维度，以符合与各个国家/地区相关的体验的要求和偏好。 但是，此方法是客户做出的业务决策。 这不是要求。

与设置渠道（在线商店）相关的先决条件和任务超出了本文档的范围。 有关如何在 Commerce headquarters 中设置在线渠道的详细信息，请参阅[渠道设置基础知识](channels-overview.md#channel-setup-basics)。 有关特定于在线渠道的步骤和要求的信息，请参阅[设置在线渠道](channel-setup-online.md)。

要在站点生成器中将渠道添加到您的站点，请按照以下步骤操作。

1. 在 Commerce 站点生成器中，转到 **站点设置 \> 渠道**。 
1. 选择 **添加渠道**。
1. 在 **添加渠道** 对话框中的 **渠道** 下面，选择要添加的渠道。 
    > [!NOTE]
    > 您只能添加尚未添加到站点的渠道。
1. 选择渠道的默认区域设置。 如果将新语言添加到渠道，则可以将默认语言更改为其中一种新语言。
1. 指定将构成针对渠道和语言组合提供内容和体验的 URL 的域和路径。
1. 选择 **确定**。
1. 选择 **保存并发布**。

## <a name="localize-e-commerce-site-content"></a>本地化电子商务站点内容

### <a name="xliff-basics"></a>XLIFF 基础知识

XLIFF 是一种行业标准文件格式，用于在内容管理工具之间传递可本地化的内容。 Commerce 站点生成器使用 XLIFF 文件格式导出页面、片段和图像元数据内容，以便能够对其进行本地化和重新导入。

Microsoft Dynamics 客户通常与第三方本地化供应商（如 [Translated.com](https://translated.com/welcome)）合作，将他们的 XLIFF 文件翻译为所需的语言。

### <a name="localize-assets-in-site-builder"></a>在站点生成器中本地化资产

可以在站点生成器中本地化以下电子商务站点资产：

- 页面
- 片段
- 媒体资产
- 模块

所有新页面、片段和媒体资产都是在当前在渠道和区域设置选择器中选择的渠道和语言上下文中创建的。 该语言通常是您的“基础语言”，前提是您没有配置其他语言或渠道。 在配置了多个渠道和语言的站点上，“基本语言”由您在站点设置中的 **渠道** 页面上设置为默认值的频道和区域设置进行定义。

页面、片段和媒体资产内容的本地化步骤相似。 以下部分中将指出例外和差异。 但是，本地化模块内容的步骤不同。 有关详细信息，请参阅本主题后面的[本地化模块](#localize-modules)一节。

#### <a name="step-1-export-an-xliff-file"></a>步骤 1：导出 XLIFF 文件

要在站点生成器中导出页面、片段或图像的 XLIFF 文件，请执行以下步骤。

1. 打开要为其导出基本语言内容的资产，以便能够对其进行本地化。
1. 在命令栏上，选择 **本地化 \> 导出 XLIFF**。
    > [!NOTE]
    > 仅当资产处于 **编辑** 状态时，**本地化** 选项才可见。

名为 **\<assetname\>.xlf** 的 XLIFF 文件将下载到浏览器的下载文件夹。 此 XLIFF 文件特定于您要本地化的资产。 您将为要本地化的每一个资产导出一个 XLIFF 文件。

#### <a name="step-2-localize-the-xliff-file"></a>步骤 2：本地化 XLIFF 文件

在大多数情况下，您将与本地化供应商一起翻译 XLIFF 文件。 但是，如果您要在内部本地化资产，或者如果只想测试本地化流程，则必须对 XLIFF 文件进行以下更改：

- 将目标语言属性添加到 /xliff/file 元素，并将值设置为您要本地化为的语言的区域设置标识符。 
    > [!NOTE]
    > 此区域设置标识符必须与站点设置内的 **渠道** 页面中的区域设置标识符匹配。
- 对于每个 //源元素，请添加一个目标元素同级项，其中文本值是该源元素内容的本地化版本。

有关控制 XLIFF 文件的架构的信息，请参阅 [XLIFF 1.2 规范](http://docs.oasis-open.org/xliff/xliff-core/xliff-core.html)。

> [!NOTE]
> 要将资产本地化为多种语言，您必须为每种语言创建一个本地化的 XLIFF 文件。

#### <a name="step-3-import-the-localized-xliff-file"></a>步骤 3：导入本地化的 XLIFF 文件

要导入资产的 XLIFF 文件，请按照以下步骤操作。

1. 在 Commerce 站点生成器中，打开要为其导入 XLIFF 文件的资产。
1. 在右上角的渠道和区域设置选择器中，选择您要为其导入本地化内容的渠道和语言。
1. 在命令栏上，选择 **本地化 \> 导入 XLIFF**。 然后浏览到并选择所选资产和语言的本地化 XLIFF 文件。

在成功导入 XLIFF 文件后，将创建页面、片段或资产的“变型”。 从那时起，对本地化变体所做的所有更改将仅影响该变体。 它们不会影响变型派生自的基础资产。 同样，对基础资产所做的更改将不会影响该资产的变体。 

但是，对于页面，您可以通过修改这些页面绑定到的模板或布局来跨变体进行更改。 同样，对片段所做的更改将影响依赖该变型的所有页面。

### <a name="images"></a>图像

仅当与这些图像关联的内容元数据已本地化时，才能在页面或模块变体中呈现图像。 当前，媒体资产中的以下元数据可本地化：

- 替代文本
- Description
- 标题

当前，您无法本地化数字资产（如图像或视频）的二进制文件。 Dynamics 365 Commerce 产品团队当前正在使用此功能。

### <a name="localize-modules"></a>本地化模块

作为模块本身的一部分呈现的字符串（例如，轮播模块中的“上一个”和“下一个”）与模块内容分开进行本地化。 有关说明，请参阅[本地化模块](e-commerce-extensibility/localize-module.md)。

## <a name="additional-resources"></a>其他资源

[页面模型词汇表](page-elements-overview.md)

[跨渠道共享](cross-channel-sharing.md)

[本地化模块](e-commerce-extensibility/localize-module.md)

[模块定义文件](e-commerce-extensibility/module-definition-file.md)

[本地化 Commerce 扩展资源和标签文件](dev-itpro/extension-resource-localization.md)

[使用 CultureInfoFormatter 类对模块进行全局化](e-commerce-extensibility/globalize-modules.md)

[应用设置：主题](e-commerce-extensibility/app-settings.md#themes-section)
