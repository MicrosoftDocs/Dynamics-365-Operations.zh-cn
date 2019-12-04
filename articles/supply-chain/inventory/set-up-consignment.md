---
title: 设置托运
description: 本主题介绍如何配置入站托运库存工序。
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventJournalOwnershipChange, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 220804
ms.assetid: 88822f78-4de5-462c-a55f-1f766c572719
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 04b3fb3038a1373e203ec240a0163cf67de655cc
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813826"
---
# <a name="set-up-consignment"></a>设置托运

[!include [banner](../includes/banner.md)]

本主题介绍如何配置入站托运库存工序。

托运库存是由供应商所拥有，但存储在您的站点的库存。 在您准备好消耗或使用库存时，您接过库存的所有权。 此主题介绍启用托运流程所需的设置。 有关托运流程的详细信息，请参阅[设置托运](consignment.md)。

## <a name="inventory-owners"></a>库存所有者
要记录实际入站托运库存，您需要定义供应商所有者。 此操作在**库存所有者**页完成。 当您选择一个**供应商帐户**后，将为**名称**和**所有者**字段生成默认值。 **所有者**字段中的值将对供应商可见，因此如果您的供应商帐户名称不易被外部人员识别，则您可能要更改该名称。 可以编辑**所有者**字段，但仅在您保存**库存所有者**记录时。 **名称**字段使用供应商帐户关联的当事方的名称进行填充，并且无法更改。

[![库存所有者](./media/inventory-owners.png)](./media/inventory-owners.png)

## <a name="tracking-dimension-group"></a>跟踪维度组
要在托运流程中使用的物料必须与**所有者**维度设置为**活动**的**跟踪维度组**相关联。 所有者维度始终选择了**实际库存**和**财务库存**选项。 从不选择**按维度的覆盖范围计划**。

[![跟踪维度组](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)

## <a name="inventory-ownership-change-journal"></a>库存所有权更改日记帐
**库存所有权更改**日记帐用于记录托运库存所有权从供应商转移到消耗它的法人。 同任何库存日记帐一样，它必须使用库存日记帐名称进行标识。 这些名称在**库存日记帐名称**页上创建，且**日记帐类型**必须设置为**所有权更改**。

[![库存所有权更改日记帐](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)

## <a name="vendor-collaboration-in-consignment-processes"></a>托运流程中的供应商协作
如果您的供应商使用供应商协作界面，他们可以使用该界面监控您的站点的库存的消耗量。 有关设置供应商使用供应商协作的详细信息，请参阅[供应商门户用户安全性](../procurement/configure-security-vendor-portal-users.md)。
