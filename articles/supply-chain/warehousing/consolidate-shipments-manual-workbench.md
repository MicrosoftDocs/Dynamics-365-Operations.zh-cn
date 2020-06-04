---
title: 使用装运合并工作台合并装运
description: 此主题提供以下方案：使用装运合并工作台将多个订单发放到仓库，以后再合并到装运中。
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
ms.author: v-olbara
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: b1a2c9506b4444fc98a9e4f0389cbd69db4ce052
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383721"
---
# <a name="consolidate-shipments-by-using-the-shipment-consolidation-workbench"></a>使用装运合并工作台合并装运

[!include [banner](../includes/banner.md)]

此主题提供以下方案：使用装运合并工作台将多个订单发放到仓库，以后再合并到装运中。

## <a name="make-demo-data-available"></a>提供演示数据

此主题中的方案引用为 Microsoft Dynamics 365 Supply Chain Management 提供的标准演示数据中包含的值和记录。 如果要在进行此练习时使用此处提供的值，请务必在安装了演示数据的环境中操作，并且在开始前将法人设置为 **USMF**。

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>设置装运合并策略和产品筛选器

此处介绍的方案假设已经开启了此功能，完成了[配置装运合并策略](configure-shipment-consolidation-policies.md)中的练习，并创建了其中介绍的策略和其他记录。 务必先完成这些练习，再继续完成此方案。

## <a name="turn-on-the-manual-shipment-consolidation-feature"></a>开启手动合并装运功能

*手动合并装运*功能必须先在系统中开启，才能使用。 管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查功能状态和开启功能。 在**功能管理**工作区中，此功能按照下面的方式列出：

- **模块**：*仓库管理*
- **功能名称**：*手动合并装运*

[配置装运合并策略](configure-shipment-consolidation-policies.md)中已说明，还必须先开启*合并装运*功能，才能创建策略。 但是，您应该已经完成了该步骤。

## <a name="create-the-sales-orders-for-this-scenario"></a>为此方案创建销售订单

首先创建可以使用的销售订单的集合。 必须使用为高级仓库 (WMS) 流程启用的仓库。 除非明确提及其他仓库，否则必须为下面的每组订单使用同一个仓库。

转到**应收帐款 \> 订单 \> 所有销售订单**，然后创建具有以下小节中介绍的设置的销售订单的集合。

### <a name="create-order-set-1"></a>创建订单集 1

#### <a name="sales-orders-1-1-and-1-2"></a>销售订单 1-1 和 1-2

1. 创建具有以下设置的两个相同销售订单：

    - **客户帐户**：*US-001*
    - **交货方式**：*航空公司-航运*

1. 添加具有以下设置的订单行：

    - **物料编号**：*A0001*（未为其分配**代码 4** 筛选器的物料）
    - **数量：** *1.00*

1. 选择**库存 \> 预留**，然后在操作窗格上选择**预留批次**预留订单行。

#### <a name="sales-order-1-3"></a>销售订单 1-3

1. 创建具有以下设置的销售订单：

    - **客户帐户**：*US-001*
    - **交货方式**：*10*

1. 添加具有以下设置的订单行：

    - **物料编号**：*A0001*（未为其分配**代码 4** 筛选器的物料）
    - **数量：** *1.00*

1. 选择**库存 \> 预留**，然后在操作窗格上选择**预留批次**预留订单行。
1. 添加第二个具有以下设置的订单行：

    - **物料编号**：*A0002*（未为其分配**代码 4** 筛选器的物料）
    - **数量：** *1.00*
    - **交货方式**：*航空公司-航运*

1. 选择**库存 \> 预留**，然后在操作窗格上选择**预留批次**预留第二个订单行。

### <a name="create-order-set-2"></a>创建订单集 2

#### <a name="sales-orders-2-1-and-2-2"></a>销售订单 2-1 和 2-2

1. 创建具有以下设置的两个相同销售订单：

    - **客户帐户**：*US-002*
    - **交货方式**：*航空公司-航运*

1. 添加具有以下设置的订单行：

    - **物料编号**：*M9200*（其中的**代码 4** 筛选器设置为*易燃*的物料）
    - **数量：** *1.00*

1. 选择**库存 \> 预留**，然后在操作窗格上选择**预留批次**预留订单行。
1. 添加第二个具有以下设置的订单行：

    - **物料编号**：*M9201*（其中的**代码 4** 筛选器设置为*易爆*的物料）
    - **数量：** *1.00*
    - **交货方式**：*航空公司-航运*

1. 选择**库存 \> 预留**，然后在操作窗格上选择**预留批次**预留第二个订单行。

### <a name="create-order-set-3"></a>创建订单集 3

#### <a name="sales-orders-3-1-and-3-2"></a>销售订单 3-1 和 3-2

1. 创建具有以下设置的两个相同销售订单：

    - **客户帐户**：*US-001*
    - **客户申请**：*1*

1. 添加具有以下设置的订单行：

    - **物料编号**：*A0001*（未为其分配**代码 4** 筛选器的物料）
    - **数量：** *1.00*

1. 选择**库存 \> 预留**，然后在操作窗格上选择**预留批次**预留订单行。

#### <a name="sales-orders-3-3-and-3-4"></a>销售订单 3-3 和 3-4

1. 创建具有以下设置的两个相同销售订单：

    - **客户帐户**：*US-001*
    - **客户申请**：*2*

1. 添加具有以下设置的订单行：

    - **物料编号**：*A0001*（未为其分配**代码 4** 筛选器的物料）
    - **数量：** *1.00*

1. 选择**库存 \> 预留**，然后在操作窗格上选择**预留批次**预留订单行。

### <a name="create-order-set-4"></a>创建订单集 4

#### <a name="sales-orders-4-1-and-4-2"></a>销售订单 4-1 和 4-2

1. 创建具有以下设置的两个相同销售订单：

    - **客户帐户**：*US-003*

1. 添加具有以下设置的订单行：

    - **物料编号**：*A0001*（未为其分配**代码 4** 筛选器的物料）
    - **数量：** *1.00*

1. 选择**库存 \> 预留**，然后在操作窗格上选择**预留批次**预留订单行。

#### <a name="sales-orders-4-3-and-4-4"></a>销售订单 4-3 和 4-4

1. 创建具有以下设置的两个相同销售订单：

    - **客户帐户**：*US-004*

1. 添加具有以下设置的订单行：

    - **物料编号**：*A0001*（未为其分配**代码 4** 筛选器的物料）
    - **数量：** *1.00*

1. 选择**库存 \> 预留**，然后在操作窗格上选择**预留批次**预留订单行。

#### <a name="sales-orders-4-5-and-4-6"></a>销售订单 4-5 和 4-6

1. 创建具有以下设置的两个相同销售订单：

    - **客户帐户**：*US-007*
    - **站点**：*6*
    - **仓库**：*61*
    - **池**：*ShipCons*

1. 添加具有以下设置的订单行：

    - **物料编号**：*A0001*（未为其分配**代码 4** 筛选器的物料）
    - **数量：** *1.00*

1. 选择**库存 \> 预留**，然后在操作窗格上选择**预留批次**预留订单行。

#### <a name="sales-orders-4-7-and-4-8"></a>销售订单 4-7 和 4-8

1. 创建具有以下设置的两个相同销售订单：

    - **客户帐户**：*US-007*
    - **站点**：*6*
    - **仓库**：*61*
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

## <a name="consolidate-the-shipments-by-using-the-shipment-consolidation-workbench"></a>使用装运合并工作台合并装运

1. 转到**仓库管理 \> 发放到仓库 \> 装运合并工作台**。
1. 在操作窗格上，选择**编辑查询**。
1. 在查询编辑器对话框中**范围**选项卡上，选择**添加**向网格添加具有以下设置的行：

    - **表**：*销售订单*
    - **字段**：*销售订单*
    - **条件：** 输入为此方案创建的每个订单集以逗号分隔的销售订单编号列表。

1. 选择**确定**保存查询并关闭对话框。
1. 在操作窗格上选择**合并装运**。
1. 选择所有装运，然后在操作窗格上选择**合并**。

## <a name="verify-the-shipments"></a>验证装运

以下过程用于验证装运合并导致已创建或更新的装运。 将其用于查看您为此方案创建的每个订单集，然后查看后面的小节以确保获取了预期结果。

1. 转到**仓库管理 \> 装运 \> 所有装运**。
1. 找到并选择所需装运。
1. 如果创建或更新装运时使用了合并策略，应该可以在**装运合并策略**字段中看到此策略。

### <a name="related-shipments-for-order-set-1"></a>订单集 1 的相关装运

应该已经创建了两个装运：

- 第一个装运中包含三行，该装运是使用 *CustomerMode* 装运合并策略创建的。
- 第二个装运（该装运不使用*航空公司*交装运输方式）是使用 *CustomerOrderNo* 装运合并策略创建的。

### <a name="related-shipments-for-order-set-2"></a>订单集 2 的相关装运

应该已经创建了三个装运：

- 第一个装运中包含*易燃*物品。
- 其他两个装运每个包含一行，该行有*易爆*物品。

### <a name="related-shipments-for-order-set-3"></a>订单集 3 的相关装运

应该已经创建了两个装运：

- 第一个装运中包含其中的**客户申请**字段设置为 *1* 的销售订单中的订单行。
- 第二个装运中包含其中的**客户申请**字段设置为 *2* 的销售订单中的订单行。

### <a name="related-shipments-for-order-set-4"></a>订单集 4 的相关装运

应该已经创建了四个装运：

- 使用*订单池*装运合并策略将客户 *US-003* 的两个订单的行合并到了一个装运中。
- 使用*订单池*装运合并策略将客户 *US-004* 的两个订单的行合并到了一个装运中。
- 使用*订单池*装运合并策略将客户 *US-007* 的销售订单 4-5 和 4-6 的行合并到了一个装运中。
- 使用*交叉订单*装运合并策略将客户 *US-007* 的销售订单 4-7 和 4-8 的行合并到了一个装运中。

## <a name="additional-resources"></a>其他资源

- [装运合并政策](about-shipment-consolidation-policies.md)
- [配置装运合并策略](configure-shipment-consolidation-policies.md)