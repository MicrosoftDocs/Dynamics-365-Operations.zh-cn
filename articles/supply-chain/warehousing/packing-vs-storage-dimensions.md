---
title: 设置不同的包装和存储维度
description: 本主题说明如何指定每个指定维度用于哪个流程（包装、存储或嵌套包装）。
author: mirzaab
manager: tfehr
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPhysDimUOM
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 004d9b4522335b481b640ef0fe35f4db66e3c9f5
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/28/2021
ms.locfileid: "5078238"
---
# <a name="set-different-dimensions-for-packing-and-storage"></a>设置不同的包装和存储维度

[!include [banner](../includes/banner.md)]

有些物料的包装或存储方式会让您有可能需要针对多个不同流程中的每个流程进行不同的物理维度跟踪。 *包装产品维度* 功能可让您为每个产品设置一种或几种维度。 每个维度类型提供一组物理度量（重量、宽度、深度和高度），并建立应用这些物理度量值的流程。 启用此功能后，您的系统将支持以下维度类型：

- *存储* - 存储维度与库位容量一起用于确定各个仓库位置可以存储每种物料的数量。
- *包装* - 包装维度用来在集装化和手动包装流程中确定适合各个集装箱类型的每种物料的数量。
- *嵌套包装* - 嵌套包装维度在包装流程包含多个级别时使用。

即使未启用 *包装产品维度* 功能，也支持 *存储* 维度。 您使用 Supply Chain Management 中的 **物理维度** 页设置这些维度。 这些维度由所有未指定包装维度和嵌套包装维度的流程使用。

*包装* 和 *嵌套包装* 维度使用 **物理产品维度** 页设置，在您启用 *包装产品维度* 功能时添加。
本主题提供了一个场景来说明如何使用此功能。

## <a name="turn-on-the-packaging-product-dimensions-feature"></a>打开包装产品维度功能

此功能只有在系统中开启之后才能使用。 管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区检查功能状态和开启功能（如果需要）。 在那里，此功能以以下方式列出：

- **模块**：*仓库管理*
- **功能名称**：*包装产品维度*

## <a name="example-scenario"></a>示例场景

### <a name="set-up-the-scenario"></a>设置场景

在运行示例场景之前，您必须按照本节所述准备您的系统。

#### <a name="enable-demo-data"></a>启用演示数据

若要使用此处指定的演示记录和值完成此场景，使用的系统中必须已安装标准[演示数据](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md)。 此外，开始前，还必须选择 *USMF* 法人。

#### <a name="add-a-new-physical-dimension-to-a-product"></a>为产品添加新物理维度

执行以下操作为产品添加新的物理维度：

1. 转到 **产品信息管理 \> 产品 \> 已发布产品**。
1. 选择具有 **物料编号** *A0001* 的产品。
1. 在操作窗格上，打开 **管理库存** 选项卡，从 **仓库** 组，选择 **物理产品维度**。
1. **物理产品维度** 页将打开。 在操作窗格上，选择 **新建** 来使用以下设置向网格添加新维度：
    - **物理维度类型** - *包装*
    - **物理单位** - *件*
    - **重量** - *4*
    - **重量单位** - *千克*
    - **深度** - *3*
    - **高度** - *4*
    - **宽度** - *3*
    - **长度** - *厘米*
    - **体积单位** - *立方厘米*

**体积** 字段根据您的 **深度**、**高度** 和 **宽度** 设置自动计算。

#### <a name="create-a-new-container-type"></a>创建新集装箱类型

转到 **仓库管理 \> 设置 \> 集装箱 \> 集装箱类型**，然后使用以下设置创建新记录：

- **集装箱类型代码** - *Short Box*
- **描述** - *短箱*
- **最大净重** - *50*
- **体积** - *144*
- **长度** - *6*
- **宽度** - *6*
- **高度** - *4*

#### <a name="create-a-container-group"></a>创建集装箱组

转到 **仓库管理 \> 设置 \> 集装箱 \> 集装箱组**，然后使用以下设置创建新记录：

- **集装箱组 ID** - *Short Box*
- **描述** - *短箱*

在 **详细信息** 部分添加新行。 将 **集装箱类型** 设置为 *短箱*。

#### <a name="set-up-a-container-build-template"></a>设置集装箱生成模板

转到 **仓库管理 \> 设置 \> 集装箱 \> 集装箱生成模板**，选择 **箱**。 将 **集装箱组 ID** 更改为 *短箱*。

### <a name="run-the-scenario"></a>运行场景

如上一节所述准备好系统后，即可按下一节所述运行场景。

#### <a name="create-a-sales-order-and-create-a-shipment"></a>创建销售订单与创建装运

在此流程中，您将根据物料 *包装* 维度创建装运，其高度小于 3。

1. 转到 **销售和营销 \> 销售订单 \> 所有销售订单**。
1. 在操作窗格上，选择 **新建**。
1. 在 **创建销售订单** 对话框中，设置以下值：

    - **客户帐户**：*US-001*
    - **仓库**：*63*

1. 选择 **确定** 创建销售订单，然后关闭对话框。
1. 将打开新销售订单。 **销售订单行** 快速选项卡上的网格中应包含一个新的空行。 在这个行中，设置以下值：

    - **物料编号：***A0001*
    - **数量：** *5*

1. 在 **销售订单行** 快速选项卡上，选择 **库存 \> 预留**。
1. 在 **预留** 页面的“操作窗格”中，选择 **预留批次** 预留库存。
1. 关闭该页面。
1. 在操作窗格上，打开 **仓库** 选项卡，选择 **发放到仓库** 为仓库创建工作。
1. 在 **销售订单行** 快速选项卡上，选择 **仓库 \> 装运详细信息**。
1. 在操作窗格上，打开 **运输** 选项卡，选择 **查看集装箱**。 确认物料已装入两个 *短箱* 集装箱中。

#### <a name="place-an-item-into-storage"></a>将物料放入存储

1. 打开移动设备，登录到仓库 63，转到 **库存 \> 调入**。
1. 输入 **Loc** = *SHORT-01*。 制作 **物料** = *A0001*、**数量** = *1 件* 的新牌照。
1. 选择 **确定**。 您将收到错误“位置 SHORT-01 失败，因为物料 A0001 不适合位置的指定维度。” 这是因为产品的 *存储* 类型维度大于位置模板中指定的维度。
