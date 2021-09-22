---
title: 如果设置序列号，维度位置不能为空
description: 如果在为序列物料创建转移单后确认装运时收到此错误，说明“默认收货库位”字段为空。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6f58c72438d5d1d93e59e46525debd65d44d9a76
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475724"
---
# <a name="error-when-confirming-shipment-after-creating-a-transfer-order-for-a-serial-item"></a>为序列物料创建转移单之后确认装运时出错

## <a name="symptoms"></a>故障特征

如果您使用启用了高级仓库管理 (WMS) 的仓库为序列物料创建转移单，然后在工作完成后尝试确认装运，您将收到以下错误消息：

> 如果设置维度序列号，维度位置不能保留为空。

## <a name="cause"></a>原因

原因是 **默认收货位置** 字段在“来源”仓库的中转仓库中是空白的。

## <a name="resolution"></a>解决方法

要解决此问题，请在中转仓库中指定默认收货位置。 请确保此位置是由牌照控制的。
