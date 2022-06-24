---
title: 复制环境后缺少产品和类别
description: 本文提供故障排除指南，在环境之间或同一环境中复制站点后缺少产品和类别时，本指南可以提供帮助。
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
ms.openlocfilehash: 0c094f6da7756d2a6a3b80ebdb211d7b78148813
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851097"
---
# <a name="products-and-categories-missing-after-environment-copy"></a>复制环境后缺少产品和类别

[!include [banner](../../includes/banner.md)]

本文提供故障排除指南，在环境之间或同一环境中复制站点后缺少产品和类别时，本指南可以提供帮助。

## <a name="description"></a>说明

将站点从一个环境复制到另一环境或在同一环境中复制后，该站点缺少产品和类别。 电子商务店面和 Commerce 站点构建器中的 **产品** 选项卡缺少产品和类别。

## <a name="resolution"></a>解决方法

### <a name="map-the-channel-operating-unit-number-to-a-newly-copied-site-in-commerce-site-builder"></a>将渠道运营单位编号映射到 Commerce 站点构建器中新复制的站点

要将渠道运营单位编号 (OUN) 映射到 Commerce 站点构建器中新复制的站点，请执行以下步骤。

1. 选择新复制的站点。
1. 在 **站点设置** 下，选择 **渠道**。
1. 在渠道名称旁边，选择省略号 (**...**)，然后选择 **更改在线商店渠道**。
1. 在 **更改在线商店渠道** 对话框中，选择要映射到新复制的站点的渠道，然后选择 **确定**。
1. 选择 **保存并发布**。

## <a name="additional-resources"></a>其他资源

[将 Dynamics 365 Commerce 站点与在线渠道相关联](../associate-site-online-store.md)
