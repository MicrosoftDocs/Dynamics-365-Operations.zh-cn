---
title: 维护工人和工人组
description: 本主题介绍资产管理中的维护工人和工人组。
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetWorkerGroupCopyFromResourceGroup, EntAssetWorkerGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b81de02f144712786704a46d2096dfb510d5ce68
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/16/2021
ms.locfileid: "5017384"
---
# <a name="maintenance-workers-and-worker-groups"></a>维护工人和工人组

[!include [banner](../../includes/banner.md)]

 

本主题介绍资产管理中的维护工人和工人组。 在资产管理中，可将维护工人连接到功能位置。 （有关功能位置的详细信息，请参阅[创建功能位置](../functional-locations/create-functional-locations.md)。）此功能在如下场景中可能非常有用：您对功能位置 01 中的机器安排了维护作业，而您希望分配同一个位置的维护工人执行该作业。

也可以创建维护工人组并为其关联维护工人。 如果要执行简单工作订单安排，并且希望为工作订单安排一组维护工人，此功能非常有用。 可使用维护工人和维护工人组设置首选维护工人和负责的维护工人。 


## <a name="create-workers"></a>创建工作人员

1. 选择 **资产管理** \> **设置** \> **工人** \> **工人**。
2. 选择 **新建** 向列表添加工人。
3. 在 **工人** 字段中，选择工人。
4. 将 **活动** 选项设置为 **是**，以便为工作订单安排工人。

    如果已经为工人选择了资源，将自动填写 **常规** 快速选项卡上的 **资源** 和 **说明** 字段。 也将自动填写 **常规** 字段，前提是已将工人设置为资源，并且已在 **资源** 页（**组织管理** \> **资源** \> **资源**）上为该资源分配了日历。

5. 在 **组** 快速选项卡上，选择 **添加**，然后为工人选择维护工人组。 一个工人可以隶属多个组。
6. 在标准设置中，工人与组之间的隶属关系从添加组的日期开始生效，从不过期。 此日期在 **生效** 字段中显示。 若要查看 **生效** 字段，请选择 **查看** \> **所有**。 如果工人与组之间的隶属关系应该限制到特定期间，请使用 **生效** 和 **到期** 字段定义该期间。
7. 在 **功能位置** 快速选项卡上，选择 **添加**，然后为维护工人选择功能位置。 并且指定哪个位置是工人的主功能位置。

    > [!NOTE]
    > 向工人添加功能位置时，将在各菜单项（如 **我的有效资产** 和 **我的有效功能位置**）上显示与这些功能位置有关的所有有效资产。 还在当您新建资产、维护请求或工作订单时显示的资产查找中显示。

    **详细信息** 快速选项卡上的字段显示与所选维护工人关联的维护工人组和功能位置的数量。

## <a name="create-worker-groups"></a>创建工人组

1. 选择 **资产管理** \> **设置** \> **工人** \> **维护工人组**。
2. 选择 **新建** 向列表添加工人组。
3. 在 **维护工人组** 字段中，输入组 ID。
4. 在 **名称** 字段中输入名称。
5. 在 **工人** 快速选项卡上，选择 **添加**，然后为工人组选择维护工人。 有关 **生效** 和 **到期** 字段的信息，请参见上一过程中的步骤 6。
6. 如果应将资源组与所选维护工人组关联，请选择 **从资源组复制**。 在 **组** 字段中，选择要从中复制日历设置的资源组。 然后，在 **工人组** 字段中，选择要将资源组的日历设置复制到的工人组。 仅当希望在执行工作订单计划期间维护工人使用与资源（工作中心）关联的日历，此步骤才相关。

    **详细信息** 快速选项卡上的字段显示已经为所选维护工人组设置的维护工人的数量。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]