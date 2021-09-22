---
title: 直接交货无法处理已启用 WMS 的仓库
description: 如果仓库已启用 WMS，则不支持直接交货。 若要使用直接交货，必须选择非 WMS 物料和仓库。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 090e17091e9fb92c2065679bb9b04637214e2eea
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475740"
---
# <a name="direct-delivery-not-able-to-process-for-wms-enabled-warehouse"></a>直接交货无法处理已启用 WMS 的仓库

## <a name="symptoms"></a>故障特征

如果将物料添加到销售行，以便从已启用 Warehouse Management (WMS) 的仓库直接交货，更新该销售行时将收到以下错误消息：

> 直接交货无法为仓库 1% 执行处理，因为它启用了仓库管理。 请指定另一个未启用仓库管理的仓库。

## <a name="resolution"></a>解决方法

Microsoft 已评估此问题，确定了这是一项功能限制。 当前，WMS 不支持直接交货。 因此，要使用直接交货，必须选择非 WMS 物料和仓库。
