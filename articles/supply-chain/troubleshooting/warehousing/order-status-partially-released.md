---
title: 订单在开票后状态仍然为“部分下达”
description: 在某些情况下，即使订单开票之后，销售订单的下达状态仍是“部分下达”。 此页面介绍原因和可行解决方法。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8bfe7ecfd4beb6e77e8dd1e23ccd896d067bdb51
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475698"
---
# <a name="order-status-remains-partially-released-even-after-the-sales-order-is-invoiced"></a>即使销售订单开票之后订单状态仍是“部分下达”

## <a name="symptoms"></a>故障特征

销售订单是一个交货订单，但其中的一个或多个商品有不同的交货方式。 订单开票后，其下达状态仍为 *部分下达*。

例如，一个销售订单有两个商品：一个要交货，一个要提货。 交货和提货都已完成。 因此，这两行都已开票。 但是，下达状态仍显示为 *部分下达*，这有一定误导性。

## <a name="workaround"></a>解决方法

下达状态仅适用于物料已启用仓库管理的订单行。 因此，在这种情况下，下达状态仍为 *部分下达*。 Microsoft 已评估此问题，确定了这是一项功能限制。 可以作为装箱单和开发票流程的一部分添加扩展，来更新下达状态。
