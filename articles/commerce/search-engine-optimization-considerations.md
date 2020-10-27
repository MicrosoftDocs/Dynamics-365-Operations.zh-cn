---
title: 站点的搜索引擎优化 (SEO) 注意事项
description: 此主题介绍从开发到生产的站点搜索引擎优化 (SEO) 注意事项。
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6ffc772addb330abe7205007662a3f3e08a3e47f
ms.sourcegitcommit: f16db76c1c235dfa445b50614bcee9219782d6dc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961578"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a>站点的搜索引擎优化 (SEO) 注意事项


[!include [banner](includes/banner.md)]

此主题介绍从开发到生产的站点搜索引擎优化 (SEO) 注意事项。

## <a name="a-site-that-is-under-development"></a>正在开发的站点

正在开发某个站点时，所有站点页面应该具有 **NOINDEX** 和 **NOFOLLOW** 元标记，这样搜索引擎才不会为这些页面建立索引和将您的站点的开发版本存储到其缓存中。 若要执行此配置，必须向站点页模板添加默认元标记模块。 然后，默认元标记属性在页面编辑器中 SEO 属性部分内仍然可用。 可使用这些属性管理元标记。

## <a name="soft-launch-of-a-site"></a>软启动站点

“软启动”期间，将在完全启动之前将网站提供给一小部分受众或市场。 如果对网站执行软启动，应考虑保留 **NOINDEX** 元标记。 这样，有助于确保软启动继续仅对您要联系的一小部分受众开放。

## <a name="a-site-that-is-in-production"></a>生产中的站点

站点在生产中时，应确保正确标记所有站点页。 Microsoft Dynamics 365 Commerce 使用为页面输入的信息在该页中显示所有 SEO 信息。 以下模块提供此功能：类别页汇总、列表页汇总和产品页汇总。

为了优化搜索引擎索引编制，呈现框架同时使用 Dynamics 365 Commerce 中配置的 SEO 属性的信息和模块特定的信息。 对于生产中的站点，应确保 robots.txt 文件允许为您的整个站点进行索引编制，并且其中包含您发布的站点地图文档的链接。 您应该在**站点设置 \> 启用站点地图**中开启站点地图生成功能。

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a>适用于内部预览、首先受众和所有受众的页面 SEO 设置

因为 Dynamics 365 Commerce 在可视页面构建器中支持已经过身份验证的“所见即所得”(WYSIWYG) 预览，所以作者可以准备自己的页面内容，不必担心信息对站点访问者可见。 如果必须发布某个页面，但是其公开性受到限制，则应采用 **NOINDEX** 元标记，从而让搜索引擎不为其建立索引。 然后，页面准备好对所有受众公开时，应该准备好所有基本 SEO 元数据，以便将搜索引擎索引编制的效率发挥到极致。 此外，还应该删除 **NOLIMIT** 元标记。

## <a name="additional-resources"></a>其他资源

[管理电子商务用户和角色](manage-ecommerce-users-roles.md)

[将脚本代码添加到站点页面以支持遥测](add-telemetry.md)

[管理内容安全策略 (CSP)](manage-csp.md)
