---
title: 使用合并装运页面手动合并装运
description: 此主题提供以下方案：使用“合并装运”页将多个订单发放到仓库，以后再合并。
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
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: ac60bef797d8e0bbe0d20f1585d5c3c0163f8788
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986784"
---
# <a name="consolidate-shipments-manually-by-using-the-consolidate-shipments-page"></a>使用合并装运页面手动合并装运

[!include [banner](../includes/banner.md)]

此主题提供以下方案：使用**合并装运**页将多个订单发放到仓库，以后再合并。

## <a name="make-demo-data-available"></a>提供演示数据

此主题中的方案引用为 Microsoft Dynamics 365 Supply Chain Management 提供的标准演示数据中包含的值和记录。 如果要在进行此练习时使用此处提供的值，请务必在安装了演示数据的环境中操作，并且在开始前将法人设置为 **USMF**。

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>设置装运合并策略和产品筛选器

此处介绍的方案假设已经开启了此功能，完成了[配置装运合并策略](configure-shipment-consolidation-policies.md)中的练习，并创建了其中介绍的策略和其他记录。 务必先完成这些练习，再继续完成此方案。

## <a name="create-the-sales-orders-for-this-scenario"></a>为此方案创建销售订单

首先创建可以使用的销售订单的集合。 必须使用为高级仓库 (WMS) 流程启用的仓库。 除非明确提及其他仓库，否则必须为下面的每组订单使用同一个仓库。

转到**应收帐款 \> 订单 \> 所有销售订单**，然后创建具有以下小节中介绍的设置的销售订单的集合。

### <a name="create-sales-orders-1-and-2"></a>创建销售订单 1 和 2

1. 创建具有以下设置的两个相同销售订单：

    - **客户帐户**：*US-007*
    - **池**：*ShipCons*

1. 添加具有以下设置的订单行：

    - **物料编号**：*A0001*（未为其分配**代码 4** 筛选器的物料）
    - **数量：** *1.00*

1. 选择**库存 \> 预留**，然后在操作窗格上选择**预留批次**预留订单行。

### <a name="create-sales-orders-3-and-4"></a>创建销售订单 3 和 4

1. 创建具有以下设置的两个相同销售订单：

    - **客户帐户**：*US-007*
    - **池**：保持此字段为空。

1. 添加具有以下设置的订单行：

    - **物料编号**：*A0001*（未为其分配**代码 4** 筛选器的物料）
    - **数量：** *1.00*

1. 选择**库存 \> 预留**，然后在操作窗格上选择**预留批次**预留订单行。

## <a name="release-the-orders-to-the-warehouse"></a>将订单发放到仓库

请按照以下步骤将您为此方案创建的每个销售订单发放到仓库。

1. 转到**应收帐款 \> 订单 \> 全部采购订单**。
1. 查找并选择要发放的销售订单。
1. 在“操作窗格”上的**仓库**选项卡上，选择**操作 \> 发放到仓库**发放所选销售订单。
1. 对为此方案创建的其他每个销售订单集重复此过程。

## <a name="consolidate-shipments"></a>合并装运

1. 转到**仓库管理 \> 装运 \> 所有装运**。
1. 找到并选择将销售订单 1 发放到仓库时创建的装运。 （其**装运合并策略**字段应设置为*订单池*。）
1. 在“操作”窗格上的**装运**选项卡中，选择**装运 \> 合并装运**。
1. 验证建议合并的装运。 只应建议合并策略相同的一个装运。
1. 关闭**装运合并**页。
1. 找到并选择将销售订单 3 发放到仓库时创建的装运。 （其**装运合并策略**字段应设置为*默认*。）
1. 在“操作”窗格上的**装运**选项卡中，选择**装运 \> 合并装运**。
1. 验证没有建议要合并的装运。
1. 选择**显示筛选器**。
1. 在**筛选器**窗格中，移除**订单编号**筛选器，然后选择**应用**。
1. 验证建议合并的装运。 只应建议合并策略相同的一个装运。

## <a name="additional-resources"></a>其他资源

- [装运合并政策](about-shipment-consolidation-policies.md)
- [配置装运合并策略](configure-shipment-consolidation-policies.md)