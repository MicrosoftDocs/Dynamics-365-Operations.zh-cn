---
title: 未启用评分和评价解决方案时搜索结果和类别页面中显示评分优化器
description: 本主题提供有关在未为电子商务站点启用 Microsoft Dynamics 365 Commerce 评分和评价解决方案时如何在搜索结果和类别页面中隐藏评分优化器的故障排除说明。
author: gvrmohanreddy
manager: annbe
ms.date: 09/02/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-09-03
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: f3438d12f4ffd06b07cbef724cda8fa490a5f4eb
ms.sourcegitcommit: d420b96d37093c26f0e99c548f036eb49a15ec30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/03/2021
ms.locfileid: "7472575"
---
# <a name="ratings-refiner-appears-on-search-results-and-category-pages-when-the-ratings-and-reviews-solution-isnt-enabled"></a>未启用评分和评价解决方案时搜索结果和类别页面中显示评分优化器

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

本主题提供有关在未为电子商务站点启用 Microsoft Dynamics 365 Commerce 评分和评价解决方案时如何在搜索结果和类别页面中隐藏评分优化器的故障排除说明。

## <a name="description"></a>说明

在不使用评分和评价解决方案的电子商务渠道中的搜索结果和类别页面上显示评分优化器。

## <a name="resolution"></a>解决方法

### <a name="enable-the-hide-rating-setting-in-commerce-site-builder"></a>在 Commerce 站点构建器中启用“隐藏评分”设置

若要在 Commerce 站点构建器中启用 **隐藏评分** 设置，以便搜索结果和类别页面中隐藏评分优化器，请执行以下步骤。

1. 转到 **站点设置 \> 扩展**。
1. 在 **评分和评价** 下，选中 **隐藏评分** 复选框。
1. 选择 **保存并发布**。

## <a name="additional-resources"></a>其他资源

[评分和评价概览](../ratings-reviews-overview.md)

[选择使用评分和评价](../opt-in-ratings-reviews.md)
