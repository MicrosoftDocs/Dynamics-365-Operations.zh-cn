---
title: 站点的搜索引擎优化 (SEO) 注意事项
description: 本文介绍从开发到生产的站点搜索引擎优化 (SEO) 注意事项。
author: psimolin
ms.date: 05/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: 6747df3c56fb05248210f78ebf2176a56ce78329
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896893"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a>站点的搜索引擎优化 (SEO) 注意事项


[!include [banner](includes/banner.md)]

本文介绍从开发到生产的站点搜索引擎优化 (SEO) 注意事项。

## <a name="a-site-that-is-under-development"></a>正在开发的站点

为了确保搜索引擎不为正在开发的站点编制索引，所有站点页面都应具有 **noindex** 和 **nofollow** 元标记。 一个很好的做法是基于包含以下元标记条目的 [MetaTags 模块](metatags-module.md)创建一个片段，并确保将此片段添加到站点上使用的所有模板的 HTML \<head\> 部分中。

```html
<meta name="robots" content="noindex,nofollow" /> 
```

## <a name="soft-launch-of-a-site"></a>软启动站点

“软启动”期间，将在完全启动之前将网站提供给一小部分受众或市场。 如果对网站执行软启动，应考虑保留 **noindex** 元标记。 这样，有助于确保软启动继续仅对您要联系的一小部分受众开放。

## <a name="a-site-that-is-in-production"></a>生产中的站点

站点在生产中时，应确保正确标记所有站点页。 Microsoft Dynamics 365 Commerce 使用为页面输入的信息在该页中显示所有 SEO 信息。 以下模块提供此功能：类别页汇总、列表页汇总和产品页汇总。

为了优化搜索引擎索引编制，呈现框架同时使用 Dynamics 365 Commerce 中配置的 SEO 属性的信息和模块特定的信息。 对于生产中的站点，应确保 robots.txt 文件允许为您的整个站点进行索引编制，并且其中包含您发布的站点地图文档的链接。 您应该在 **站点设置 \> 启用站点地图** 中开启站点地图生成功能。

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a>适用于内部预览、首先受众和所有受众的页面 SEO 设置

因为 Dynamics 365 Commerce 在可视页面构建器中支持已经过身份验证的“所见即所得”(WYSIWYG) 预览，所以作者可以准备自己的页面内容，不必担心信息对站点访问者可见。 如果必须发布某个页面，但是其公开性受到限制，则应采用 **NOINDEX** 元标记，从而让搜索引擎不为其建立索引。 然后，页面准备好对所有受众公开时，应该准备好所有基本 SEO 元数据，以便将搜索引擎索引编制的效率发挥到极致。 此外，还应该删除 **nolimit** 元标记。

## <a name="additional-resources"></a>其他资源

[管理电子商务用户和角色](manage-ecommerce-users-roles.md)

[将脚本代码添加到站点页面以支持遥测](add-telemetry.md)

[管理内容安全策略 (CSP)](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
