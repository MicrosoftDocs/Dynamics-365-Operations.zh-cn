---
title: 部分下达和部分装运疑难解答
description: 此主题介绍如何解决在 Microsoft Dynamics 365 Supply Chain Management 中处理部分下达和部分装运时可能遇到的常见问题。
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 5534099f81a97a1dcf4908784fd71dd03cf94eaf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828146"
---
# <a name="troubleshoot-partial-releases-and-partial-shipments"></a>部分下达和部分装运疑难解答

[!include [banner](../includes/banner.md)]

此主题介绍如何解决在 Microsoft Dynamics 365 Supply Chain Management 中处理部分下达和部分装运时可能遇到的常见问题。

## <a name="the-release-status-of-a-sales-order-remains-partially-released-even-after-the-sales-order-is-invoiced"></a>即使销售订单开票之后，销售订单的下达状态仍是“部分下达”。

### <a name="issue-description"></a>问题描述

销售订单是一个交货订单，但其中的一个或多个商品有不同的交货方式。 订单开票后，其下达状态仍为 *部分下达*。

例如，一个销售订单有两个商品：一个要交货，一个要提货。 交货和提货都已完成。 因此，这两行都已开票。 但是，下达状态仍显示为 *部分下达*，这有一定误导性。

### <a name="issue-resolution"></a>解决问题

下达状态仅适用于物料已启用仓库管理的订单行。 因此，在这种情况下，下达状态仍为 *部分下达*。 Microsoft 已评估此问题，确定了这是一项功能限制。 可以作为装箱单和开发票流程的一部分添加扩展，来更新下达状态。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]