---
title: 必须为此库位指定牌照
description: 如果在为启用 WMS 的仓库创建转移单后收到此错误，说明中转仓库的默认收货库位为空。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 2e562ad2b41dd149f215adc83bd2d54e55dccc05
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475655"
---
# <a name="license-plate-specification-error-when-confirming-shipment-for-a-transfer-order"></a>确认转移单的装运时牌照规格错误

## <a name="symptoms"></a>故障特征

如果您使用启用了高级仓库管理 (WMS) 的仓库创建转移单，然后在工作完成后尝试确认装运，可能会收到以下错误消息：

> 必须为此库位指定牌照。

## <a name="cause"></a>原因

原因是 **默认收货位置** 字段在“来源”仓库的中转仓库中是空白的。

## <a name="resolution"></a>解决方法

要解决此问题，请在中转仓库中指定默认收货位置。 请确保此位置是由牌照控制的。
