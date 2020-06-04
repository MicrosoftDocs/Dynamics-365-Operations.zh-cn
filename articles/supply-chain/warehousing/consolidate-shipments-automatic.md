---
title: 使用自动发放销售订单发放到仓库时使用合并
description: 此主题提供以下方案：在同一个自动化发放到仓库定期过程中将多个订单发放到仓库。
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
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 373b6bf6219ef76bacef3c67a816aec4c084c405
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383719"
---
# <a name="consolidate-shipments-when-they-are-released-to-the-warehouse-by-using-automatic-release-of-sales-orders"></a>使用自动发放销售订单发放到仓库时使用合并

[!include [banner](../includes/banner.md)]

此主题提供以下方案：在同一个自动化发放到仓库定期过程中将多个订单发放到仓库。 将根据定义为装运合并策略的规则将订单自动合并到装运中。

在此方案中，将创建多组订单并将每组发放到仓库。 然后根据配置的策略查看装运合并期间创建或更新的装运。

## <a name="make-demo-data-available"></a>提供演示数据

此主题中的方案引用为 Microsoft Dynamics 365 Supply Chain Management 提供的标准演示数据中包含的值和记录。 如果要在进行此练习时使用此处提供的值，请务必在安装了演示数据的环境中操作，并且在开始前将法人设置为 **USMF**。

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>设置装运合并策略和产品筛选器

此处介绍的方案假设已经开启了此功能，完成了[配置装运合并策略](configure-shipment-consolidation-policies.md)中的练习，并创建了其中介绍的策略和其他记录。 务必先完成这些练习，再继续完成此方案。

## <a name="create-the-sales-orders-for-this-scenario"></a>为此方案创建销售订单

首先创建可以使用的销售订单的集合。 必须使用为高级仓库 (WMS) 流程启用的仓库。 除非明确提及其他仓库，否则必须为下面的每组订单使用同一个仓库。

转到**应收帐款 \> 订单 \> 所有销售订单**，然后创建具有以下小节中介绍的设置的销售订单的集合。

### <a name="create-order-set-1"></a>创建订单集 1

#### <a name="sales-order-1-1"></a>销售订单 1-1

1. 创建具有以下设置的销售订单：

    - **客户帐户**：*US-001*
    - **交货方式**：*航空公司-航运*

1. 添加具有以下设置的订单行：

    - **物料编号**：*A0001*（未为其分配**代码 4** 筛选器的物料）
    - **数量：** *1.00*

#### <a name="sales-order-1-2"></a>销售订单 1-2

1. 创建具有以下设置的销售订单：

    - **客户帐户**：*US-001*
    - **交货方式**：*航空公司-航运*

1. 添加具有以下设置的订单行：

    - **物料编号**：*A0001*（未为其分配**代码 4** 筛选器的物料）
    - **数量：** *1.00*

#### <a name="sales-order-1-3"></a>销售订单 1-3

1. 创建具有以下设置的销售订单：

    - **客户帐户**：*US-001*
    - **交货方式**：*10*

1. 添加具有以下设置的订单行：

    - **物料编号**：*A0001*（未为其分配**代码 4** 筛选器的物料）
    - **数量：** *1.00*

1. 添加第二个具有以下设置的订单行：

    - **物料编号**：*A0002*（未为其分配**代码 4** 筛选器的物料）
    - **数量：** *1.00*
    - **交货方式**：*航空公司-航运*

### <a name="create-order-set-2"></a>创建订单集 2

#### <a name="sales-orders-2-1-and-2-2"></a>销售订单 2-1 和 2-2

1. 创建具有以下设置的两个相同销售订单：

    - **客户帐户**：*US-002*

1. 添加具有以下设置的订单行：

    - **物料编号**：*M9200*（其中的**代码 4** 筛选器设置为*易燃*的物料）
    - **数量：** *1.00*

1. 添加第二个具有以下设置的订单行：

    - **物料编号**：*M9201*（其中的**代码 4** 筛选器设置为*易爆*的物料）
    - **数量：** *1.00*
    - **交货方式**：*航空公司-航运*

### <a name="create-order-set-3"></a>创建订单集 3

#### <a name="sales-order-3-1"></a>销售订单 3-1

1. 创建具有以下设置的销售订单：

    - **客户帐户**：*US-002*

1. 添加具有以下设置的订单行：

    - **物料编号**：*M9200*（其中的**代码 4** 筛选器设置为*易燃*的物料）
    - **数量：** *1.00*

1. 添加第二个具有以下设置的订单行：

    - **物料编号**：*M9201*（其中的**代码 4** 筛选器设置为*易爆*的物料）
    - **数量：** *1.00*
    - **交货方式**：*航空公司-航运*

> [!NOTE]
> 此订单与为订单集 2 创建的两个订单相同。 但是，其作为自己的订单集列出，因为后面将在此方案中单独发放。

### <a name="create-order-set-4"></a>创建订单集 4

#### <a name="sales-order-4-1"></a>销售订单 4-1

1. 创建具有以下设置的销售订单：

    - **客户帐户**：*US-001*
    - **客户申请**：*1*

1. 添加具有以下设置的订单行：

    - **物料编号**：*A0001*（未为其分配**代码 4** 筛选器的物料）
    - **数量：** *1.00*

### <a name="create-order-set-5"></a>创建订单集 5

#### <a name="sales-orders-5-1-and-5-2"></a>销售订单 5-1 和 5-2

1. 创建具有以下设置的两个相同销售订单：

    - **客户帐户**：*US-001*
    - **客户申请**：*2*

1. 添加具有以下设置的订单行：

    - **物料编号**：*A0001*（未为其分配**代码 4** 筛选器的物料）
    - **数量：** *1.00*

#### <a name="sales-order-5-3"></a>销售订单 5-3

1. 创建具有以下设置的销售订单：

    - **客户帐户**：*US-001*
    - **客户申请**：*1*

1. 添加具有以下设置的订单行：

    - **物料编号**：*A0001*（未为其分配**代码 4** 筛选器的物料）
    - **数量：** *1.00*

### <a name="create-order-set-6"></a>创建订单集 6

#### <a name="sales-orders-6-1-and-6-2"></a>销售订单 6-1 和 6-2

1. 创建具有以下设置的两个相同销售订单：

    - **客户帐户**：*US-003*
    - **客户申请**：*2*

1. 添加具有以下设置的订单行：

    - **物料编号**：*A0001*（未为其分配**代码 4** 筛选器的物料）
    - **数量：** *1.00*

#### <a name="sales-orders-6-3-and-6-4"></a>销售订单 6-3 和 6-4

1. 创建具有以下设置的两个相同销售订单：

    - **客户帐户**：*US-004*
    - **客户申请**：*1*

1. 添加具有以下设置的订单行：

    - **物料编号**：*A0001*（未为其分配**代码 4** 筛选器的物料）
    - **数量：** *1.00*

#### <a name="sales-orders-6-5-and-6-6"></a>销售订单 6-5 和 6-6

1. 创建具有以下设置的两个相同销售订单：

    - **客户帐户**：*US-007*
    - **站点**：*6*
    - **仓库**：*61*
    - **池**：*ShipCons*

1. 添加具有以下设置的订单行：

    - **物料编号**：*A0001*（未为其分配**代码 4** 筛选器的物料）
    - **数量：** *1.00*

#### <a name="sales-orders-6-7-and-6-8"></a>销售订单 6-7 和 6-8

1. 创建具有以下设置的两个相同销售订单：

    - **客户帐户**：*US-007*
    - **站点**： *6*
    - **仓库**：*61*
    - **池**：保持此字段为空。

1. 添加具有以下设置的订单行：

    - **物料编号**：*A0001*（未为其分配**代码 4** 筛选器的物料）
    - **数量：** *1.00*

## <a name="automatic-release-of-sales-orders-to-the-warehouse"></a>将销售订单自动发放到仓库

将为之前创建的每组销售订单完成自动发放到仓库过程。 在每个示例中，将完成此处提供的[发放到仓库基本过程](#release-procedure)。

### <a name="basic-release-to-warehouse-procedure"></a><a name="release-procedure"></a>发放到仓库基本过程

为之前创建的每组销售订单完成以下小节中概述的三个过程。

#### <a name="update-the-wave-template-that-will-be-used-during-release"></a>更新发放期间将使用的波次模板

1. 转到**仓库管理 \> 设置 \> 波次 \> 波次模板**。
1. 将**波次模板类型**字段设置为*装运*。
1. 找到并选择与为此方案创建的订单集中所用仓库关联的波次模板。 例如，如果使用了仓库 *24*，请选择 **24 装运默认值**波次模板。 如果使用了仓库 *61*，请选择 **61 装运**波次模板。
1. 在操作窗格上，选择**编辑**。
1. 设置**在发放到仓库时处理波次**选项为*否*。

#### <a name="release-to-the-warehouse"></a>发放到仓库

1. 转到**仓库管理 \> 发放到仓库 \> 自动发放销售订单**。
1. 将**要发放的数量**字段设置为*全部*。
1. 在**要包括的记录**快速选项卡上，选择**筛选器**打开查询对话框。
1. 在**范围**选项卡上，选择**添加**向网格添加具有以下设置的行：

    - **表**：*销售订单*
    - **派生表**：*销售订单*
    - **字段**：*销售订单*
    - **条件：** 输入所需订单集中的销售订单编号以逗号分隔的列表。

1. 选择**确定**保存您的查询。
1. 选择**确定**开始*自动发放到仓库*过程。

#### <a name="review-the-shipment-that-is-created-or-updated"></a>查看创建或更新的装运

1. 转到**仓库管理 \> 装运 \> 所有装运**。
1. 找到并选择所需装运。
1. 如果创建或更新装运时使用了合并策略，应该可以在**装运合并策略**字段中看到此策略。

### <a name="release-sales-orders-from-order-set-1"></a>发放订单集 1 中的销售订单

执行[发放到仓库基本过程](#release-procedure)发放订单集 1 中的销售订单。

完成后，您应该可以看到创建了下面两个装运：

- 第一个装运中包含三行，该装运是使用 *CustomerMode* 装运合并策略创建的。
- 第二个装运（该装运不使用*航空公司*交装运输方式）是使用 *CustomerOrderNo* 装运合并策略创建的。

### <a name="release-sales-orders-from-order-set-2"></a>发放订单集 2 中的销售订单

执行[发放到仓库基本过程](#release-procedure)发放订单集 2 中的销售订单。

完成后，您应该可以看到创建了下面三个装运：

- 第一个装运中包含*易燃*物品。
- 其他两个装运每个包含一行，该行有*易爆*物品。

### <a name="release-sales-orders-from-order-set-3"></a>发放订单集 3 中的销售订单

执行[发放到仓库基本过程](#release-procedure)发放订单集 3 中的销售订单。

完成后，应该可以看到发生了以下操作：

- 更新了一个现有装运（订单集 2 发放到仓库时创建的装运）。 添加了一个具有*易燃*物品的行。
- 创建了一个包含*易爆*物品的新装运。

### <a name="release-sales-orders-from-order-set-4"></a>发放订单集 4 中的销售订单

执行[发放到仓库基本过程](#release-procedure)发放订单集 4 中的销售订单。

完成后，应该可以看到更新了一个现有装运（其中的**客户申请**字段设置为 *1*）。 向其添加了一个新行。

### <a name="release-sales-orders-from-order-set-5"></a>发放订单集 5 中的销售订单

执行[发放到仓库基本过程](#release-procedure)发放订单集 5 中的销售订单。

完成后，应该可以看到发生了以下操作：

- 更新了一个现有装运（其中的**客户申请**字段设置为 *1*）。 向其添加了销售订单 5-3（其中的**客户申请**字段设置为 *1*）中的一行。
- 创建了一个新装运，其中销售订单 5-1 和 5-2 的行合并为一个装运。

### <a name="release-sales-orders-from-order-set-6"></a>发放订单集 6 中的销售订单

执行[发放到仓库基本过程](#release-procedure)发放订单集 6 中的销售订单。

完成后，您应该可以看到创建了下面四个装运：

- 使用*订单池*装运合并策略将客户 *US-003* 的两个订单的行合并到了一个装运中。
- 使用*订单池*装运合并策略将客户 *US-004* 的两个订单的行合并到了一个装运中。
- 使用*订单池*装运合并策略将客户 *US-007* 的销售订单 6-5 和 6-6 的行合并到了一个装运中。
- 使用*交叉订单*装运合并策略将客户 *US-007* 的销售订单 6-7 和 6-8 的行合并到了一个装运中。

## <a name="additional-resources"></a>其他资源

- [装运合并政策](about-shipment-consolidation-policies.md)
- [配置装运合并策略](configure-shipment-consolidation-policies.md)