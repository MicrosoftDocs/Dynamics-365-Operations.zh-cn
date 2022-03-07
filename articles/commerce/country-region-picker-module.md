---
title: 国家/地区选取器模块
description: 此主题描述国家/地区选取器模块，以及如何在 Microsoft Dynamics 365 Commerce 中配置此模块。
author: stuharg
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2021-08-12
ms.dyn365.ops.version: Release 10.0.22
ms.openlocfilehash: 3134e10c096525ec2d82365a25eff16a3c5d5e11
ms.sourcegitcommit: d420b96d37093c26f0e99c548f036eb49a15ec30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/03/2021
ms.locfileid: "7472573"
---
# <a name="countryregion-picker-module"></a>国家/地区选取器模块

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

此主题描述国家/地区选取器模块，以及如何在 Microsoft Dynamics 365 Commerce 中配置此模块。

国家/地区选取器模块使用 Dynamics 365 Commerce 中的[地理检测和重定向](geo-detection-redirection.md)功能向请求未与其国家或地区关联的电子商务站点 URL 的客户显示推荐的 URL。

例如，加拿大客户请求未与加拿大关联的站点 URL。 在此示例中，国家/地区选取器模块显示一个对话框，其中推荐与加拿大关联的站点 URL。 下图显示国家/地区选取器对话框的示例。

![主页上的国家/地区选取器对话框的示例。](./media/Geo_country-region-module-insitu.png)

## <a name="countryregion-picker-module-properties"></a>国家/地区选取器模块属性

| 属性名称              | 值       | 说明 |
| -------------------------- | ----------- | ----------- |
| 标题                    | 文本        | 显示在对话框顶部的标题。 |
| 副标题                 | 文本        | 显示在标题下方的副标题。 |
| 国家/地区：显示字符串    | 文本        | URL 选项的显示名称（例如，“加拿大”）。 |
| 国家/地区：显示子字符串 | 文本        | URL 选项的可选显示子字符串（例如，“英语”或“法语”）。 |
| 国家/地区：国家/地区图像     | 媒体资产 | 与 URL 选项关联的可选图像（例如，加拿大标志的图像）。 |
| 国家/地区：国家/地区 URL       | 文本        | 与在 Commerce 站点生成器中的 **渠道** 页面（**站点设置 \> 渠道**）上为国家或地区配置的渠道和区域设置对应的 URL。 此 URL 必须与在 **渠道** 页面上配置的 URL 完全匹配。 |
| 操作链接                | 操作链接 | 在对话框底部显示的可选链接。 例如，此链接可以指向提供站点支持的所有国家和地区的列表的内部页面。 |

## <a name="add-a-countryregion-picker-module-to-a-page"></a>向页面添加国家/地区选取器模块

可以直接或通过共享片段向标题模块添加国家/地区选取器模块。 有关标题模块的详细信息，请参阅[标题模块](author-header-module.md)。

## <a name="configure-the-countryregion-picker-module-in-commerce-site-builder"></a>在 Commerce 站点生成器中配置国家/地区选取器模块

> [!NOTE]
> 您向客户推荐的 URL 必须配置为国家/地区选取器模块中的国家/地区对象。

对于要向客户显示和推荐的每个 URL，请在 Commerce 站点生成器中执行以下步骤。

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

[页眉模块](author-header-module.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
