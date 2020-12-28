---
title: 基于采购订单创建资产
description: 本主题说明如何在资产管理中创建资产物料的列表，这些资产物料可充当为维护作业创建资产的基础。
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectItem, EntAssetPendingAssets
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 54c129d93e13e032cc5526a91c73d3363ed183db
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4422945"
---
# <a name="create-assets-based-on-purchase-orders"></a>基于采购订单创建资产

[!include [banner](../../includes/banner.md)]

 

本主题说明如何在资产管理中创建资产物料的列表，这些资产物料可充当为维护作业创建资产的基础。 可根据资产物料查看已经为这些物料创建的采购订单行的列表。 此功能的作用是在资产管理中基于采购订单轻松创建资产。

首先，在 **资产物料** 中设置要用于通过采购订单创建资产的物料。 创建采购订单行之后，在 **暂挂资产** 中创建资产。 可以决定应该在采购订单的哪个阶段创建资产。


## <a name="select-asset-items"></a>选择资产物料

1. 单击 **资产管理** > **设置** > **资产** > **物料**。
2. 单击 **新建** 创建新资产物料。
3. 在 **物料编号** 字段中选择物料。 离开该字段时，将在 **产品名** 字段中自动插入物料名称。
4. 在 **常规** 快速选项卡上，选择物料的资产类型。
5. 选择物料的资产制造商和模型。
6. 保存该物料。


## <a name="create-assets-from-pending-assets"></a>通过暂挂资产创建资产

1. 单击 **资产管理** > **常用** > **资产** > **暂挂资产**。
2. 将看到基于 **资产物料** 中所选物料更新后的采购订单列表。
3. 可筛选采购订单状态，以便选择应该在哪个生命周期状态创建资产。 例如，您可能希望仅当在采购订单中过帐了产品收据时才创建资产。
4. 在采购订单行中选择 **参考编号** 链接，以便查看有关物料的详细信息。
5. 如果要编辑 **库存维度** 快速选项卡上显示哪些维度，请单击 **显示维度** 按钮，然后进行选择。
6. 如果要基于采购订单行创建资产，请选中列表页上 **标记** 列中该行的复选框，然后单击 **创建资产**。 将显示消息，告知您资产 ID。
7. 在 **所有资产** 列表中选择资产，然后单击 **编辑** 向资产添加更多信息。
8. 如果因为不希望创建资产而要删除行，请选中 **暂挂资产** 中 **标记** 列内该行的复选框，然后单击 **放弃暂挂资产**。 将显示消息，告知您资产 ID。 您将不删除采购订单或销售订单，而是仅删除本该用于在 **资产管理** 中创建资产的记录。

>[!NOTE]
>将把所有产品维度（尺寸、颜色、配置等）自动转给资产属性。 创建资产时，将直接为资产创建跟踪维度（序列号）。


## <a name="find-pending-assets"></a>查找暂挂资产

可运行 **暂挂资产盘点** 以检查是否有暂挂资产。 例如，可使用此功能在每次准备好将暂挂资产创建为资产时接收通知。

1. 单击 **资产管理** > **定期** > **资产** > **暂挂资产盘点**。
2. 单击 **确定** 运行作业并更新 **暂挂资产** 中的列表。
3. 可以将此作业设置为批处理作业，例如，每天一次。

**注意：** 如果在创建资产 *之后* 根据适合物料更改了采购订单中的数据，将不会在资产上体现这些更改。
