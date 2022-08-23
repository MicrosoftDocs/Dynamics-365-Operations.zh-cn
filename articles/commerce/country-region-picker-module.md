---
title: 国家/地区选取器模块
description: 本文描述国家/地区选取器模块，以及如何在 Microsoft Dynamics 365 Commerce 中配置此模块。
author: bicyclingfool
ms.date: 04/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-08-12
ms.dyn365.ops.version: Release 10.0.22
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 203a8e17e075f15b7ae3cceb98d24ced75539a01
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270283"
---
# <a name="countryregion-picker-module"></a>国家/地区选取器模块

[!include [banner](includes/banner.md)]

本文描述国家/地区选取器模块，以及如何在 Microsoft Dynamics 365 Commerce 中配置此模块。

国家/地区选取器模块使用 Dynamics 365 Commerce 中的[地理检测和重定向](geo-detection-redirection.md)功能向请求未与其国家或地区关联的电子商务站点 URL 的客户显示推荐的站点。

例如，加拿大的客户请求与加拿大以外的国家/地区关联的站点 URL。 在此示例中，国家/地区选取器模块显示一个对话框，其中推荐与加拿大关联的站点 URL。 

## <a name="how-it-works"></a>工作原理

为站点启用地理检测和重定向后，在客户请求站点 URL 时，为客户检测到的国家/地区和他们请求的 URL 用于确定该 URL 是否映射到客户所在的国家/地区。 URL 和国家/地区之间的映射在 Commerce 站点构建器的 **站点设置** 下的 **渠道** 页面上定义。 

如果请求 URL 与映射到客户国家/地区的任何 URL 都不匹配，则在响应中返回映射到该国家/地区的一个或多个 URL 的列表。 国家/地区选取器会将该列表中的每个 URL 与在国家/地区模块中配置的 URL 进行比较。 对于找到的每个完全匹配项，国家/地区选取器会呈现该 URL 的显示标题、副标题和图像，并使用 URL 为这些元素建立超链接。

当客户在国家/地区选取器中选择一个选项时，他们会被带到建立超链接的 URL。 该 URL 将被写入 **\_msdyn365\_\_\_site\_** cookie，以可以将其用作客户的站点首选项。 然后，下次客户请求与其国家或地区不关联的 URL 时，他们会被自动重定向到他们的首选国家/地区。 因此，我们建议您在电子商务网站上也使用[站点选取器模块](site-selector.md)，以让客户可以替代或更新他们的站点首选项。 

如果客户关闭国家/地区选取器对话框，则不会写入任何 cookie，客户将停留在当前站点上。 

下图显示国家/地区选取器对话框的示例。

![主页上的国家/地区选取器对话框的示例。](./media/Geo_country-region-module-insitu.png)

## <a name="countryregion-picker-module-properties"></a>国家/地区选取器模块属性

| 属性名称              | 值       | 说明                                                  |
| -------------------------- | ----------- | ------------------------------------------------------------ |
| 标题                    | 文本        | 显示在对话框顶部的标题。       |
| 副标题                 | 文本        | 显示在标题下方的副标题。               |
| 国家/地区：显示字符串    | 文本        | URL 选项的显示名称（例如，“加拿大”）。   |
| 国家/地区：显示子字符串 | 文本        | URL 选项的可选显示子字符串（例如，“英语”或“法语”）。 |
| 国家/地区：国家/地区图像     | 媒体资产 | 与 URL 选项关联的可选图像（例如，加拿大标志的图像）。 |
| 国家/地区：国家/地区 URL       | 文本        | 正在配置的国家/地区的站点 URL。 此 URL 必须与您在 Commerce 站点构建器的 **站点设置** 下的 **渠道** 页面上为此国家/地区指定的 URL 完全匹配。 此外，URL 的域必须是在 **渠道** 页面的 **匹配域** 字段中指定的自定义域，而不是在您创建电子商务环境时 Commerce 提供的站点的工作地址 （例如，URL `https://<yourcompany>.commerce.dynamics.com/`）。 |
| 操作链接                | 操作链接 | 在对话框底部显示的可选链接。 例如，此链接可以指向提供站点支持的所有国家和地区的列表的内部页面。 |

## <a name="add-a-countryregion-picker-module-to-a-page"></a>向页面添加国家/地区选取器模块

可以直接或通过共享片段向标题模块添加国家/地区选取器模块。 有关标题模块的详细信息，请参阅[标题模块](author-header-module.md)。

## <a name="configure-the-countryregion-picker-module-in-commerce-site-builder"></a>在 Commerce 站点生成器中配置国家/地区选取器模块

> [!NOTE]
> 您向客户推荐的 URL 必须配置为国家/地区选取器模块中的国家/地区对象。

对于要向客户显示和推荐的每个站点 URL，请在 Commerce 站点构建器中执行以下步骤。

1. 选择国家/地区选取器模块插槽。
1. 在属性窗格中 **国家/地区列表** 下，选择 **添加国家/地区**。
1. 选择新的 **国家/地区** 框。
1. 在 **显示字符串** 字段中，输入显示名称（例如，**加拿大**）。
1. 可选：在 **显示子字符串** 字段中，输入显示子字符串（例如，**法语** 或 **fr-ca**）。
1. 可选：从媒体库中选择图像。
1. 在 **国家/地区 URL**  字段中，输入以下 URL。 此 URL 必须与 **渠道** 页面上显示的 URL 完全匹配，并且映射到包含与国家/地区或区域设置关联的区域设置的渠道。 
1. 选择 **确定**。
1. 对希望国家/地区选取器模块显示的其他所有国家/地区 URL 重复这些步骤。

## <a name="additional-resources"></a>其他资源

[设置地理检测和重定向](geo-detection-redirection.md)

[模块库概览](starter-kit-overview.md)

[标题模块](author-header-module.md)

[站点选取器模块](site-selector.md)

[痕迹导航模块](add-breadcrumb.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
