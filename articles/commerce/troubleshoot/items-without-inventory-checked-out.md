---
title: 没有库存的商品可以结帐
description: 本文提供了故障排除指南，可以在客户将缺货商品添加到购物车并继续进行结帐时提供帮助。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 3bc924e44077886b942e19b25a84f0f1d4298c13
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282726"
---
# <a name="items-without-inventory-can-be-checked-out"></a>没有库存的商品可以结帐

[!include [banner](../../includes/banner.md)]

本文提供了故障排除指南，可以在客户将缺货商品添加到购物车并继续进行结帐时提供帮助。

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
