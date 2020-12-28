---
title: 移动平均回退成本序列
description: 此主题介绍 Microsoft Dynamics 365 Supply Chain Management 中的移动平均回退成本计算顺序。
author: AndersGirke
manager: tfehr
ms.date: 03/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-03-25
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 0538701588b9c71dff4c538711606913a359de6a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423185"
---
# <a name="moving-average-fallback-cost-sequence"></a>移动平均回退成本序列

库存成本的一种计算方法是使用 _移动平均_。 可以为每项库存物料最多关联三个成本值：

- **最后发货** – 库存变负前分配的最后发货成本
- **有效成本** – 成本计算版本中最后激活的成本
- **物料价格** – 为发布的产品指定的成本

为了确定在移动平均计算中应该使用这些成本值中的哪一个，系统使用 _回退成本序列_ 建立值的首选顺序。 如果首选成本值不可用，系统将使用下一个首选值，依此类推。

在 Microsoft Dynamics 365 Supply Chain Management 的早期版本中，系统使用固定回退成本序列（_最后发货 – 有效成本 – 物料价格_）。 在版本 10.0.11 中，此序列仍然是默认序列。 但是，也可以开启在三个可用回退成本序列中进行选择的功能。 尤其可以将此功能用于定期使用负库存值的组织。

若要为回退成本序列使用选择器，您（或管理员）必须使用 [功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)开启名称为 _移动平均回退成本序列_ 的功能。

若要选择移动平均回退成本计算序列，请执行以下步骤。

1. 打开 **参数** 页面。
2. 在 **库存会计** 选项卡的 **移动平均** 部分中，将 **回退成本序列** 字段设置为以下值之一：

    - **最后发货 – 有效成本 – 物料价格** – 此序列是默认序列。 这是未开启 _移动平均回退成本序列_ 功能时使用的同一个序列。
    - **有效成本 - 上次发货**
    - **有效成本 – 物料价格** – 组织使用的业务流程中库存定期变负，并且同时交易量极高，组织可能会遇到性能问题。 此设置有助于缓解这些性能问题。

![库存会计参数](media/inventory-accounting-parameters.png "库存会计参数")
