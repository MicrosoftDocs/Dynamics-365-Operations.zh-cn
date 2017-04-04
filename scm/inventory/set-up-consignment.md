---
title: "安装进行托运时使用。"
description: "本主题介绍如何配置入站托运库存工序。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventJournalOwnershipChange, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 220804
ms.assetid: 88822f78-4de5-462c-a55f-1f766c572719
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: afa59439e06aad9d669eb352a9837a013f447249
ms.openlocfilehash: 48e3f7f33bedf33bee5a7c2882e90743feac8687
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-consignment"></a>安装进行托运时使用。

本主题介绍如何配置入站托运库存工序。 

托运库存是由供应商所拥有，但存储在您的站点的库存。 在您准备好消耗或使用库存时，您接过库存的所有权。 此主题介绍启用托运流程所需的设置。 有关托运流程的详细信息，请参阅“[托运](consignment.md)”。

## <a name="inventory-owners"></a>库存所有者
要记录实际入站托运库存，您需要定义供应商所有者。 此操作在“**库存所有者**”页完成。 当您选择一个“**供应商帐户**”后，将为“**名称**”和“**所有者**”字段生成默认值。 “**所有者**”字段中的值将对供应商可见，因此如果您的供应商帐户名称不易被外部人员识别，则您可能要更改该名称。 可以编辑“**所有者**”字段，但仅在您保存“**库存所有者**”记录时。 “**名称**”字段使用供应商帐户关联的当事方的名称进行填充，并且无法更改。 

[] (库存![所有者。/media/inventory-owners.png)](。/media/inventory-owners.png)

## <a name="tracking-dimension-group"></a>跟踪维度组
要在托运流程中使用的物料必须与“**所有者**”维度设置为“**活动**”的“**跟踪维度组**”相关联。 所有者维度始终选择了“**实际库存**”和“**财务库存**”选项。 从不选择“**按维度的覆盖范围计划**”。 

[] (![跟踪维度组。/media/tracking 维度 group.png)](。/media/tracking 维度 group.png)

## <a name="inventory-ownership-change-journal"></a>库存所有权更改日记帐
“**库存所有权更改**”日记帐用于记录托运库存所有权从供应商转移到消耗它的法人。 同任何库存日记帐一样，它必须使用库存日记帐名称进行标识。 这些名称在“**库存日记帐名称**”页上创建，且“**日记帐类型**”必须设置为“**所有权更改**”。 

[![更改所有权] (库存日志。/media/inventory 更改所有权 journal.png)](。/media/inventory 更改所有权 journal.png)

## <a name="vendor-collaboration-in-consignment-processes"></a>托运流程中的供应商协作
如果您的供应商使用供应商协作界面，他们可以使用该界面监控您的站点的库存的消耗量。 有关设置供应商使用供应商协作的详细信息，请参阅“[为供应商协作用户配置安全性](../procurement/configure-security-vendor-portal-users.md)”。


