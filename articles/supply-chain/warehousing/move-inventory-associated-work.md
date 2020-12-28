---
title: 仓库管理中关联工作的库存变动
description: 此主题描述如何从移动设备设置和应用单件领料确认。
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorker
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2aee3af8da6610c16fc2d98091bfa3f01f1bd0f5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4422962"
---
# <a name="movement-of-inventory-with-associated-work-in-warehouse-management"></a>仓库管理中关联工作的库存变动

[!include [banner](../includes/banner.md)]

使用库存变动可以决定允许哪些仓库工作人员移动预留的库存。 您可以灵活地在受管制的仓库中决定不允许工作人员为已经创建的领料工作选择新的领料库位。 它还允许仓库经理控制一些缺乏经验的工作人员应具有哪些功能。

灵活地管理仓库工作人员的日常操作在有些场景中很有用，例如：

## <a name="scenario-1"></a>方案 1
一家公司拥有一个相对较小的收货区，那里塞满了等待入库的托盘和箱子。 当天计划要装运大批货物，因此收货职员决定将部分托盘移到辅助入库暂存区，以便将收货区清理出来。

## <a name="scenario-2"></a>方案 2
一位经验丰富的仓库工作人员注意到仓库中可以将物料合并到一个库位，而不是分成很少的数量存入 3 个彼此相邻的库位。 该工作人员要合并这些数量，将每个库位的物料移动到同一个库位和牌照上。

## <a name="scenario-3"></a>方案 3
托盘正在暂存库位（例如 BAYDOOR01 附近的 STAGE01）等待装运。 但是，由于计划更改，卡车预计将抵达 BAYDOOR04。 装运职员了解这一情况，因此需要确保卡车不必等待从 STAGE01 装货。 装运职员决定将要装运的物料从 STAGE01 移动到离新的目的地更近的 STAGE04。

### <a name="current-limitations"></a>当前限制

您可以移动的工作预留限于销售订单、转移单发货、转移单收货、采购订单和补货工作。

移动物料受到限制，以防止拆分工作行。 这意味着，如果一个工作行中有来自库位 Loc1 的 100 件物料 A，则您无法仅将其中的 30 件物料 A 移动到另一个库位。 这将导致现有工作行被拆分为 30 和 70，因为现在的库位不相同。

对于暂存方案，您要将货物移出来的牌照或您要将货物移进去的牌照设置为工作订单的目标 LP，仅允许移动整个 LP，以免分解目标 LP。
目前仅支持临时变动。 这意味着您无法通过模板移动设备菜单项的移动来移动预留的库存。

### <a name="set-up-permission-to-move-reserved-inventory-for-individual-workers"></a>为单个工作人员设置移动预留库存的权限

对于应允许其移动预留库存的工作人员，选择 **仓库管理** > **设置** > **工作人员** 下的 **允许包含关联工作的库存移动** 复选框。  

### <a name="backported"></a>往回移植

此功能也已往回移植到 Microsoft Dynamics AX 2012 R3，并将作为 CU12 的一部分提供。
也可以通过 KB 编号 3192548 单独下载。 

