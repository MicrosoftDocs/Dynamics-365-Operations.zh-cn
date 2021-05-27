---
title: 没有库存的商品可以结帐
description: 本主题提供了故障排除指南，可以在客户将缺货商品添加到购物车并继续进行结帐时提供帮助。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 4fa7769044c45faffd9ff61b3de8e6217a5e0354
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018450"
---
# <a name="items-without-inventory-can-be-checked-out"></a>没有库存的商品可以结帐

[!include [banner](../../includes/banner.md)]

本主题提供了故障排除指南，可以在客户将缺货商品添加到购物车并继续进行结帐时提供帮助。

## <a name="description"></a>说明

即使商店中没有现有库存，用户也可以将商品添加到购物车中，然后进入结帐页面。

## <a name="resolution"></a>解决方法

### <a name="enable-the-show-out-of-stock-errors-property-in-commerce-site-builder"></a>在 Commerce 站点构建器中启用“显示缺货错误”属性

要在 Commerce 站点构建器中启用 **显示缺货错误** 属性，请执行这些步骤。

1. 选择您正在处理的站点。
1. 在左侧导航中，选择 **页面**。
1. 选择 **购物车页面** 打开它。
1. 选择 **购物车 1** 插槽，选择 **编辑**，然后在属性窗格中，选择 **显示缺货错误** 复选框。
1. 保存并发布页面。

## <a name="additional-resources"></a>其他资源

[应用库存设置](../inventory-settings.md)

[计算零售渠道的库存现有量](../calculated-inventory-retail-channels.md)

[配置库存缓冲区和库存级别](../inventory-buffers-levels.md)
