---
title: 覆盖了装运合并策略时从“发放到仓库”页合并装运
description: 此主题提供了以下方案：必须从“发放到仓库”页将一个或多个销售行手动发放到仓库，并且发布前必须已覆盖系统定义的装运合并策略。
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 406ff268eede4a9d448b3b9c1729a00fcec8f21e
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986736"
---
# <a name="consolidate-shipments-when-the-shipment-consolidation-policy-is-overridden-from-the-release-to-warehouse-page"></a>覆盖了装运合并策略时从“发放到仓库”页合并装运

[!include [banner](../includes/banner.md)]

此主题提供了以下方案：必须从**发放到仓库**页将一个或多个销售行手动发放到仓库，并且发布前必须已覆盖系统定义的装运合并策略。 例如，以下情况下可能需要覆盖装运合并策略：必须将通常不与未结装运合并的订单与未结装运合并。

在此方案中，将创建一组销售订单，然后在将这些订单发放到仓库之前覆盖默认装运合并策略。

## <a name="make-demo-data-available"></a>提供演示数据

此主题中的方案引用为 Microsoft Dynamics 365 Supply Chain Management 提供的标准演示数据中包含的值和记录。 如果要在进行此练习时使用此处提供的值，请务必在安装了演示数据的环境中操作，并且在开始前将法人设置为 **USMF**。

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>设置装运合并策略和产品筛选器

此处介绍的方案假设已经开启了此功能，完成了[配置装运合并策略](configure-shipment-consolidation-policies.md)中的练习，并创建了其中介绍的策略和其他记录。 务必先完成这些练习，再继续完成此方案。

## <a name="create-the-sales-orders-for-this-scenario"></a>为此方案创建销售订单

1. 转到**应收帐款 \> 订单 \> 所有销售订单**，然后创建具有以下设置的三个相同销售订单：

    - **客户帐户**：*US-002*

1. 添加具有以下设置的订单行：

    - **物料编号**：*A0001*（未为其分配**代码 4** 筛选器的物料）
    - **数量：** *1.00*

1. 选择**库存 \> 预留**，然后在操作窗格上选择**预留批次**预留订单行。

## <a name="release-the-sales-orders-from-the-release-to-warehouse-page"></a>从“发放到仓库”页发放销售订单

发放到仓库期间执行以下步骤覆盖装运合并策略。

1. 转到**仓库管理 \> 发放到仓库 \> 发放到仓库**。
1. 在上方窗格中，选择为此方案创建的第一个销售订单。
1. 选择**添加**将行添加到“发放到仓库”。 请注意，底部窗格中应用了*默认*装运合并策略。
1. 在底部窗格中，选择**选择新装运合并策略**。
1. 选择允许与相同策略的其他未结装运合并的策略。 例如，选择 *CustomerOrderNo* 策略。
1. 选择**发放到仓库**。
1. 选择为此方案创建的第二个和第三个销售订单。
1. 选择**添加**将这些行添加到“发放到仓库”。 请注意，底部窗格中应用了*默认*策略。
1. 选择第二行，然后在**选择新装运合并策略**字段中选择 *CustomerOrderNo* 策略。
1. 为两行都选择**发放到仓库**。

## <a name="verify-the-shipments"></a>验证装运

应该已经创建了两个装运：

- 第一个装运中包含两行，该装运是使用 *CustomerOrderNo* 装运合并策略创建的。
- 第二个装运中包含一行，该装运是使用*默认*装运合并策略创建的。

请执行以下步骤查看创建的装运。

1. 转到**仓库管理 \> 装运 \> 所有装运**。
1. 找到并选择所需装运。
1. 在**装运合并策略**字段中，查看创建装运时使用的合并策略。

## <a name="additional-resources"></a>其他资源

- [装运合并政策](about-shipment-consolidation-policies.md)
- [配置装运合并策略](configure-shipment-consolidation-policies.md)
